# Comparing `tmp/OneOnOne-0.6944.tar.gz` & `tmp/OneOnOne-0.6945.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "OneOnOne-0.6944.tar", last modified: Sun Jul 23 18:37:25 2023, max compression
+gzip compressed data, was "OneOnOne-0.6945.tar", last modified: Sun Jul 23 18:46:33 2023, max compression
```

## Comparing `OneOnOne-0.6944.tar` & `OneOnOne-0.6945.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:37:25.834403 OneOnOne-0.6944/
--rw-r--r--   0 sohinib    (501) staff       (20)     1076 2023-07-10 14:29:42.000000 OneOnOne-0.6944/LICENSE
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:37:25.827808 OneOnOne-0.6944/OneOnOne/
--rw-r--r--   0 sohinib    (501) staff       (20)    52686 2023-07-23 18:37:20.000000 OneOnOne-0.6944/OneOnOne/__init__.py
--rw-r--r--   0 sohinib    (501) staff       (20)  3312680 2023-07-07 06:05:06.000000 OneOnOne-0.6944/OneOnOne/classes.py
--rw-r--r--   0 sohinib    (501) staff       (20)    13595 2023-07-19 15:12:53.000000 OneOnOne-0.6944/OneOnOne/classification.py
--rw-r--r--   0 sohinib    (501) staff       (20)     5894 2023-07-22 03:02:07.000000 OneOnOne-0.6944/OneOnOne/contextdecider.py
--rw-r--r--   0 sohinib    (501) staff       (20)      936 2023-07-19 15:12:54.000000 OneOnOne-0.6944/OneOnOne/htmlparser.py
--rw-r--r--   0 sohinib    (501) staff       (20)     3047 2023-07-19 17:26:04.000000 OneOnOne-0.6944/OneOnOne/questionanswer.py
--rw-r--r--   0 sohinib    (501) staff       (20)    20836 2023-07-19 15:12:54.000000 OneOnOne-0.6944/OneOnOne/sampling.py
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:37:25.833207 OneOnOne-0.6944/OneOnOne.egg-info/
--rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:37:25.000000 OneOnOne-0.6944/OneOnOne.egg-info/PKG-INFO
--rw-r--r--   0 sohinib    (501) staff       (20)      351 2023-07-23 18:37:25.000000 OneOnOne-0.6944/OneOnOne.egg-info/SOURCES.txt
--rw-r--r--   0 sohinib    (501) staff       (20)        1 2023-07-23 18:37:25.000000 OneOnOne-0.6944/OneOnOne.egg-info/dependency_links.txt
--rw-r--r--   0 sohinib    (501) staff       (20)      139 2023-07-23 18:37:25.000000 OneOnOne-0.6944/OneOnOne.egg-info/requires.txt
--rw-r--r--   0 sohinib    (501) staff       (20)        9 2023-07-23 18:37:25.000000 OneOnOne-0.6944/OneOnOne.egg-info/top_level.txt
--rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:37:25.833722 OneOnOne-0.6944/PKG-INFO
--rw-r--r--   0 sohinib    (501) staff       (20)     3415 2023-07-23 18:35:25.000000 OneOnOne-0.6944/README.md
--rw-r--r--   0 sohinib    (501) staff       (20)       38 2023-07-23 18:37:25.834606 OneOnOne-0.6944/setup.cfg
--rw-r--r--   0 sohinib    (501) staff       (20)     1941 2023-07-23 18:37:20.000000 OneOnOne-0.6944/setup.py
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:46:33.673183 OneOnOne-0.6945/
+-rw-r--r--   0 sohinib    (501) staff       (20)     1076 2023-07-10 14:29:42.000000 OneOnOne-0.6945/LICENSE
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:46:33.667360 OneOnOne-0.6945/OneOnOne/
+-rw-r--r--   0 sohinib    (501) staff       (20)    52685 2023-07-23 18:46:21.000000 OneOnOne-0.6945/OneOnOne/__init__.py
+-rw-r--r--   0 sohinib    (501) staff       (20)  3312680 2023-07-07 06:05:06.000000 OneOnOne-0.6945/OneOnOne/classes.py
+-rw-r--r--   0 sohinib    (501) staff       (20)    13595 2023-07-19 15:12:53.000000 OneOnOne-0.6945/OneOnOne/classification.py
+-rw-r--r--   0 sohinib    (501) staff       (20)     5894 2023-07-22 03:02:07.000000 OneOnOne-0.6945/OneOnOne/contextdecider.py
+-rw-r--r--   0 sohinib    (501) staff       (20)      936 2023-07-19 15:12:54.000000 OneOnOne-0.6945/OneOnOne/htmlparser.py
+-rw-r--r--   0 sohinib    (501) staff       (20)     3047 2023-07-19 17:26:04.000000 OneOnOne-0.6945/OneOnOne/questionanswer.py
+-rw-r--r--   0 sohinib    (501) staff       (20)    20836 2023-07-19 15:12:54.000000 OneOnOne-0.6945/OneOnOne/sampling.py
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 18:46:33.672173 OneOnOne-0.6945/OneOnOne.egg-info/
+-rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:46:33.000000 OneOnOne-0.6945/OneOnOne.egg-info/PKG-INFO
+-rw-r--r--   0 sohinib    (501) staff       (20)      351 2023-07-23 18:46:33.000000 OneOnOne-0.6945/OneOnOne.egg-info/SOURCES.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)        1 2023-07-23 18:46:33.000000 OneOnOne-0.6945/OneOnOne.egg-info/dependency_links.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)      139 2023-07-23 18:46:33.000000 OneOnOne-0.6945/OneOnOne.egg-info/requires.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)        9 2023-07-23 18:46:33.000000 OneOnOne-0.6945/OneOnOne.egg-info/top_level.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 18:46:33.672706 OneOnOne-0.6945/PKG-INFO
+-rw-r--r--   0 sohinib    (501) staff       (20)     3415 2023-07-23 18:35:25.000000 OneOnOne-0.6945/README.md
+-rw-r--r--   0 sohinib    (501) staff       (20)       38 2023-07-23 18:46:33.673322 OneOnOne-0.6945/setup.cfg
+-rw-r--r--   0 sohinib    (501) staff       (20)     1941 2023-07-23 18:46:25.000000 OneOnOne-0.6945/setup.py
```

### Comparing `OneOnOne-0.6944/LICENSE` & `OneOnOne-0.6945/LICENSE`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6944/OneOnOne/__init__.py` & `OneOnOne-0.6945/OneOnOne/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1042,15 +1042,15 @@
             img = Image.open(os.getcwd() + f"{path}")
             img.show()
 
             img = load_img(os.getcwd() + f"{path}")
             img = img.resize((32, 32))
             img = img_to_array(img)
 
-            img = img.reshape(-1, 32, 32, 3)
+            img = img.reshape(1, 32, 32, 3)
             # img = iio.imread(os.getcwd()+f"{path}")
             self.pred = self.contextmodel.predict_generator(img)
         else:
             # random.randint(1, 3000)
             self.pred = self.contextmodel.predict_generator(self.val_it, random.randint(1, 16))
 
     def preprocess_image_input(self,input_images):
```

### Comparing `OneOnOne-0.6944/OneOnOne/classes.py` & `OneOnOne-0.6945/OneOnOne/classes.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6944/OneOnOne/classification.py` & `OneOnOne-0.6945/OneOnOne/classification.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6944/OneOnOne/contextdecider.py` & `OneOnOne-0.6945/OneOnOne/contextdecider.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6944/OneOnOne/htmlparser.py` & `OneOnOne-0.6945/OneOnOne/htmlparser.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6944/OneOnOne/questionanswer.py` & `OneOnOne-0.6945/OneOnOne/questionanswer.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6944/OneOnOne/sampling.py` & `OneOnOne-0.6945/OneOnOne/sampling.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6944/OneOnOne.egg-info/PKG-INFO` & `OneOnOne-0.6945/OneOnOne.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OneOnOne
-Version: 0.6944
+Version: 0.6945
 Summary: A package for pre-trained image classification and context-decider for question-answering chatbots.
 Author: Sohini Bhattacharya
 Author-email: mail.sohinibhattacharya@gmail.com
 Keywords: python,image-classification,active-learning-sampling,question-answering,pre-trained models,tiny-image-net,cifar10
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `OneOnOne-0.6944/PKG-INFO` & `OneOnOne-0.6945/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OneOnOne
-Version: 0.6944
+Version: 0.6945
 Summary: A package for pre-trained image classification and context-decider for question-answering chatbots.
 Author: Sohini Bhattacharya
 Author-email: mail.sohinibhattacharya@gmail.com
 Keywords: python,image-classification,active-learning-sampling,question-answering,pre-trained models,tiny-image-net,cifar10
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `OneOnOne-0.6944/README.md` & `OneOnOne-0.6945/README.md`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6944/setup.py` & `OneOnOne-0.6945/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION=0.6944
+VERSION=0.6945
 
 DESCRIPTION="A package for pre-trained image classification and context-decider for question-answering chatbots."
 LONG_DESCRIPTION="Your one-stop destination to utilize image-classification models with just one line of code. A library meant to simplify your life by providing you with pre-trained models like ResNet50, EfficientNetVB6, VGG19, etc. You can simply opt for training your own models from scratch by just tweaking a few values. If you want to try popular active-learning sampling methods on image classification, no need to worry! This library has got you covered. Along with that for simple-bridging and basic into NLP, we have context-deciders, HTML parsers and simple chatbot object classes, to create an interface similar to Google Lens. You input an image or item that you are curious about and you can ask one-on-one questions from the chatbot. This is made possible by using the tiny imagenet dataset. This library is being actively updated and new features are being added frequently. New datasets and pre-trained models will be updated soon. Feel free to share your feedback! I would really appreciate it!"
 CLASSIFIERS=[
     'Development Status :: 5 - Production/Stable',
     'Intended Audience :: Education',
     'License :: OSI Approved :: MIT License',
```

