# Comparing `tmp/OneOnOne-0.6937.tar.gz` & `tmp/OneOnOne-0.6938.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "OneOnOne-0.6937.tar", last modified: Sat Jul 22 18:23:12 2023, max compression
+gzip compressed data, was "OneOnOne-0.6938.tar", last modified: Sun Jul 23 17:37:46 2023, max compression
```

## Comparing `OneOnOne-0.6937.tar` & `OneOnOne-0.6938.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-22 18:23:12.301005 OneOnOne-0.6937/
--rw-r--r--   0 sohinib    (501) staff       (20)     1076 2023-07-10 14:29:42.000000 OneOnOne-0.6937/LICENSE
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-22 18:23:12.293937 OneOnOne-0.6937/OneOnOne/
--rw-r--r--   0 sohinib    (501) staff       (20)    52576 2023-07-22 18:23:02.000000 OneOnOne-0.6937/OneOnOne/__init__.py
--rw-r--r--   0 sohinib    (501) staff       (20)  3312680 2023-07-07 06:05:06.000000 OneOnOne-0.6937/OneOnOne/classes.py
--rw-r--r--   0 sohinib    (501) staff       (20)    13595 2023-07-19 15:12:53.000000 OneOnOne-0.6937/OneOnOne/classification.py
--rw-r--r--   0 sohinib    (501) staff       (20)     5894 2023-07-22 03:02:07.000000 OneOnOne-0.6937/OneOnOne/contextdecider.py
--rw-r--r--   0 sohinib    (501) staff       (20)      936 2023-07-19 15:12:54.000000 OneOnOne-0.6937/OneOnOne/htmlparser.py
--rw-r--r--   0 sohinib    (501) staff       (20)     3047 2023-07-19 17:26:04.000000 OneOnOne-0.6937/OneOnOne/questionanswer.py
--rw-r--r--   0 sohinib    (501) staff       (20)    20836 2023-07-19 15:12:54.000000 OneOnOne-0.6937/OneOnOne/sampling.py
-drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-22 18:23:12.299247 OneOnOne-0.6937/OneOnOne.egg-info/
--rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-22 18:23:12.000000 OneOnOne-0.6937/OneOnOne.egg-info/PKG-INFO
--rw-r--r--   0 sohinib    (501) staff       (20)      351 2023-07-22 18:23:12.000000 OneOnOne-0.6937/OneOnOne.egg-info/SOURCES.txt
--rw-r--r--   0 sohinib    (501) staff       (20)        1 2023-07-22 18:23:12.000000 OneOnOne-0.6937/OneOnOne.egg-info/dependency_links.txt
--rw-r--r--   0 sohinib    (501) staff       (20)      139 2023-07-22 18:23:12.000000 OneOnOne-0.6937/OneOnOne.egg-info/requires.txt
--rw-r--r--   0 sohinib    (501) staff       (20)        9 2023-07-22 18:23:12.000000 OneOnOne-0.6937/OneOnOne.egg-info/top_level.txt
--rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-22 18:23:12.300182 OneOnOne-0.6937/PKG-INFO
--rw-r--r--   0 sohinib    (501) staff       (20)     3366 2023-07-22 16:02:47.000000 OneOnOne-0.6937/README.md
--rw-r--r--   0 sohinib    (501) staff       (20)       38 2023-07-22 18:23:12.301317 OneOnOne-0.6937/setup.cfg
--rw-r--r--   0 sohinib    (501) staff       (20)     1941 2023-07-22 18:23:06.000000 OneOnOne-0.6937/setup.py
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 17:37:46.104465 OneOnOne-0.6938/
+-rw-r--r--   0 sohinib    (501) staff       (20)     1076 2023-07-10 14:29:42.000000 OneOnOne-0.6938/LICENSE
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 17:37:46.094571 OneOnOne-0.6938/OneOnOne/
+-rw-r--r--   0 sohinib    (501) staff       (20)    52586 2023-07-23 17:37:26.000000 OneOnOne-0.6938/OneOnOne/__init__.py
+-rw-r--r--   0 sohinib    (501) staff       (20)  3312680 2023-07-07 06:05:06.000000 OneOnOne-0.6938/OneOnOne/classes.py
+-rw-r--r--   0 sohinib    (501) staff       (20)    13595 2023-07-19 15:12:53.000000 OneOnOne-0.6938/OneOnOne/classification.py
+-rw-r--r--   0 sohinib    (501) staff       (20)     5894 2023-07-22 03:02:07.000000 OneOnOne-0.6938/OneOnOne/contextdecider.py
+-rw-r--r--   0 sohinib    (501) staff       (20)      936 2023-07-19 15:12:54.000000 OneOnOne-0.6938/OneOnOne/htmlparser.py
+-rw-r--r--   0 sohinib    (501) staff       (20)     3047 2023-07-19 17:26:04.000000 OneOnOne-0.6938/OneOnOne/questionanswer.py
+-rw-r--r--   0 sohinib    (501) staff       (20)    20836 2023-07-19 15:12:54.000000 OneOnOne-0.6938/OneOnOne/sampling.py
+drwxr-xr-x   0 sohinib    (501) staff       (20)        0 2023-07-23 17:37:46.101983 OneOnOne-0.6938/OneOnOne.egg-info/
+-rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 17:37:45.000000 OneOnOne-0.6938/OneOnOne.egg-info/PKG-INFO
+-rw-r--r--   0 sohinib    (501) staff       (20)      351 2023-07-23 17:37:45.000000 OneOnOne-0.6938/OneOnOne.egg-info/SOURCES.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)        1 2023-07-23 17:37:45.000000 OneOnOne-0.6938/OneOnOne.egg-info/dependency_links.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)      139 2023-07-23 17:37:45.000000 OneOnOne-0.6938/OneOnOne.egg-info/requires.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)        9 2023-07-23 17:37:45.000000 OneOnOne-0.6938/OneOnOne.egg-info/top_level.txt
+-rw-r--r--   0 sohinib    (501) staff       (20)     1578 2023-07-23 17:37:46.103183 OneOnOne-0.6938/PKG-INFO
+-rw-r--r--   0 sohinib    (501) staff       (20)     3395 2023-07-22 18:26:11.000000 OneOnOne-0.6938/README.md
+-rw-r--r--   0 sohinib    (501) staff       (20)       38 2023-07-23 17:37:46.104709 OneOnOne-0.6938/setup.cfg
+-rw-r--r--   0 sohinib    (501) staff       (20)     1941 2023-07-23 17:37:32.000000 OneOnOne-0.6938/setup.py
```

### Comparing `OneOnOne-0.6937/LICENSE` & `OneOnOne-0.6938/LICENSE`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6937/OneOnOne/__init__.py` & `OneOnOne-0.6938/OneOnOne/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1038,15 +1038,15 @@
 
         if self.user_input:
             path=input("Please enter image path in the current directory (str):    ")
             img = Image.open(os.getcwd()+f"{path}")
             img.show()
             img = iio.imread(os.getcwd()+f"{path}")
             processed_image = self.preprocess_image_input(img)
-            self.pred = self.contextmodel.predict(processed_image)
+            self.pred = self.contextmodel.predict_generator(processed_image)
         else:
             # random.randint(1, 3000)
             self.pred = self.contextmodel.predict_generator(self.val_it, random.randint(1, 16))
 
     def preprocess_image_input(self,input_images):
         if self.model_type=="efficientnetb6":
             input_images = input_images.astype('float32')
```

### Comparing `OneOnOne-0.6937/OneOnOne/classes.py` & `OneOnOne-0.6938/OneOnOne/classes.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6937/OneOnOne/classification.py` & `OneOnOne-0.6938/OneOnOne/classification.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6937/OneOnOne/contextdecider.py` & `OneOnOne-0.6938/OneOnOne/contextdecider.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6937/OneOnOne/htmlparser.py` & `OneOnOne-0.6938/OneOnOne/htmlparser.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6937/OneOnOne/questionanswer.py` & `OneOnOne-0.6938/OneOnOne/questionanswer.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6937/OneOnOne/sampling.py` & `OneOnOne-0.6938/OneOnOne/sampling.py`

 * *Files identical despite different names*

### Comparing `OneOnOne-0.6937/OneOnOne.egg-info/PKG-INFO` & `OneOnOne-0.6938/OneOnOne.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OneOnOne
-Version: 0.6937
+Version: 0.6938
 Summary: A package for pre-trained image classification and context-decider for question-answering chatbots.
 Author: Sohini Bhattacharya
 Author-email: mail.sohinibhattacharya@gmail.com
 Keywords: python,image-classification,active-learning-sampling,question-answering,pre-trained models,tiny-image-net,cifar10
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `OneOnOne-0.6937/PKG-INFO` & `OneOnOne-0.6938/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OneOnOne
-Version: 0.6937
+Version: 0.6938
 Summary: A package for pre-trained image classification and context-decider for question-answering chatbots.
 Author: Sohini Bhattacharya
 Author-email: mail.sohinibhattacharya@gmail.com
 Keywords: python,image-classification,active-learning-sampling,question-answering,pre-trained models,tiny-image-net,cifar10
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `OneOnOne-0.6937/README.md` & `OneOnOne-0.6938/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -52,14 +52,15 @@
   <dt><span style="color:#FFC0CB">or, download pretrained models with your desired specifications!</span>
 </dl>
 
 ```python
 from OneOnOne import PretrainedModel
 
 pretrained=PretrainedModel(model_type="resnet50", dataset="cifar10", samplingtype="leastconfidence")
+model=pretrained.get_model()
 ```
 
 <h4 align="center">____________________________________________________________________________</h4>
 
 
 <h4>More Examples on NLP use-cases:</h4>
```

#### html2text {}

```diff
@@ -24,15 +24,16 @@
 ```python from OneOnOne import Classification classifier=Classification
 (validation_split=0.4,early_stopping_patience=20) ```
   or,
 ```python from OneOnOne import Sampling sampling=Sampling("entropy")
 sampling.initial_training() ```
   or, download pretrained models with your desired specifications!
 ```python from OneOnOne import PretrainedModel pretrained=PretrainedModel
-(model_type="resnet50", dataset="cifar10", samplingtype="leastconfidence") ```
+(model_type="resnet50", dataset="cifar10", samplingtype="leastconfidence")
+model=pretrained.get_model() ```
                                       ***
  ____________________________________________________________________________
                                       ***
 *** More Examples on NLP use-cases: ***
   If you want your predicted class(es) of the input image to be used as the
   context for your chatbot, simply run,
 ```python from OneOnOne import ContextDecider decider=ContextDecider
```

### Comparing `OneOnOne-0.6937/setup.py` & `OneOnOne-0.6938/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup, find_packages
 
-VERSION=0.6937
+VERSION=0.6938
 
 DESCRIPTION="A package for pre-trained image classification and context-decider for question-answering chatbots."
 LONG_DESCRIPTION="Your one-stop destination to utilize image-classification models with just one line of code. A library meant to simplify your life by providing you with pre-trained models like ResNet50, EfficientNetVB6, VGG19, etc. You can simply opt for training your own models from scratch by just tweaking a few values. If you want to try popular active-learning sampling methods on image classification, no need to worry! This library has got you covered. Along with that for simple-bridging and basic into NLP, we have context-deciders, HTML parsers and simple chatbot object classes, to create an interface similar to Google Lens. You input an image or item that you are curious about and you can ask one-on-one questions from the chatbot. This is made possible by using the tiny imagenet dataset. This library is being actively updated and new features are being added frequently. New datasets and pre-trained models will be updated soon. Feel free to share your feedback! I would really appreciate it!"
 CLASSIFIERS=[
     'Development Status :: 5 - Production/Stable',
     'Intended Audience :: Education',
     'License :: OSI Approved :: MIT License',
```

