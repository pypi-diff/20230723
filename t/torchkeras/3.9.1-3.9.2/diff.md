# Comparing `tmp/torchkeras-3.9.1.tar.gz` & `tmp/torchkeras-3.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/torchkeras-3.9.1.tar", last modified: Sat Jul  8 13:05:37 2023, max compression
+gzip compressed data, was "dist/torchkeras-3.9.2.tar", last modified: Sun Jul 23 12:17:22 2023, max compression
```

## Comparing `torchkeras-3.9.1.tar` & `torchkeras-3.9.2.tar`

### file list

```diff
@@ -1,42 +1,42 @@
-drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-08 13:05:37.117984 torchkeras-3.9.1/
--rw-r--r--   0 liangyun2   (502) staff       (20)    11325 2023-02-09 16:00:16.000000 torchkeras-3.9.1/LICENSE
--rw-r--r--   0 liangyun2   (502) staff       (20)      357 2023-02-09 16:55:42.000000 torchkeras-3.9.1/MANIFEST.in
--rw-r--r--   0 liangyun2   (502) staff       (20)     6646 2023-07-08 13:05:37.117369 torchkeras-3.9.1/PKG-INFO
--rw-r--r--   0 liangyun2   (502) staff       (20)    12671 2023-07-08 12:32:31.000000 torchkeras-3.9.1/README.md
--rw-r--r--   0 liangyun2   (502) staff       (20)       38 2023-07-08 13:05:37.118093 torchkeras-3.9.1/setup.cfg
--rw-r--r--   0 liangyun2   (502) staff       (20)     1273 2023-06-30 07:06:01.000000 torchkeras-3.9.1/setup.py
-drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-08 13:05:37.083495 torchkeras-3.9.1/torchkeras/
--rw-r--r--   0 liangyun2   (502) staff       (20)      246 2023-07-06 21:29:51.000000 torchkeras-3.9.1/torchkeras/__init__.py
-drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-08 13:05:37.110683 torchkeras-3.9.1/torchkeras/assets/
--rw-r--r--   0 liangyun2   (502) staff       (20) 10043912 2023-02-09 16:00:16.000000 torchkeras-3.9.1/torchkeras/assets/SimHei.ttf
--rw-r--r--   0 liangyun2   (502) staff       (20)  1012077 2023-02-09 16:00:16.000000 torchkeras-3.9.1/torchkeras/assets/park.jpg
--rw-r--r--   0 liangyun2   (502) staff       (20)   168949 2023-02-09 16:00:16.000000 torchkeras-3.9.1/torchkeras/assets/zidane.jpg
-drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-08 13:05:37.113214 torchkeras-3.9.1/torchkeras/chat/
--rw-r--r--   0 liangyun2   (502) staff       (20)       57 2023-07-06 21:05:16.000000 torchkeras-3.9.1/torchkeras/chat/__init__.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     2089 2023-07-08 12:15:46.000000 torchkeras-3.9.1/torchkeras/chat/chatglm.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     4178 2023-05-14 01:50:00.000000 torchkeras-3.9.1/torchkeras/chat/chatgpt.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     8621 2023-06-30 01:34:56.000000 torchkeras-3.9.1/torchkeras/data.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     5222 2023-04-13 09:25:41.000000 torchkeras-3.9.1/torchkeras/eda.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     1628 2023-04-13 07:46:39.000000 torchkeras-3.9.1/torchkeras/email.py
--rw-r--r--   0 liangyun2   (502) staff       (20)    11531 2023-06-25 03:42:54.000000 torchkeras-3.9.1/torchkeras/hugmodel.py
--rw-r--r--   0 liangyun2   (502) staff       (20)    10939 2023-07-06 21:26:00.000000 torchkeras-3.9.1/torchkeras/kerascallbacks.py
--rw-r--r--   0 liangyun2   (502) staff       (20)    13883 2023-07-06 21:28:09.000000 torchkeras-3.9.1/torchkeras/kerasmodel.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     7316 2023-02-22 02:34:47.000000 torchkeras-3.9.1/torchkeras/metrics.py
-drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-08 13:05:37.116401 torchkeras-3.9.1/torchkeras/models/
--rw-r--r--   0 liangyun2   (502) staff       (20)       75 2023-03-10 08:21:36.000000 torchkeras-3.9.1/torchkeras/models/__init__.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     4088 2023-02-24 04:01:48.000000 torchkeras-3.9.1/torchkeras/models/resnet.py
--rw-r--r--   0 liangyun2   (502) staff       (20)    31333 2023-05-20 15:18:08.000000 torchkeras-3.9.1/torchkeras/models/ssd.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     3374 2023-02-21 12:33:54.000000 torchkeras-3.9.1/torchkeras/models/unet.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     5444 2023-06-04 08:48:25.000000 torchkeras-3.9.1/torchkeras/pbar.py
--rw-r--r--   0 liangyun2   (502) staff       (20)    10676 2023-06-10 15:29:22.000000 torchkeras-3.9.1/torchkeras/plots.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     5737 2023-05-12 10:11:52.000000 torchkeras-3.9.1/torchkeras/soup.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     5256 2023-05-28 13:14:40.000000 torchkeras-3.9.1/torchkeras/summary.py
-drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-08 13:05:37.116968 torchkeras-3.9.1/torchkeras/tools/
--rw-r--r--   0 liangyun2   (502) staff       (20)     3740 2023-07-06 21:11:38.000000 torchkeras-3.9.1/torchkeras/tools/catboost.py
--rw-r--r--   0 liangyun2   (502) staff       (20)     3843 2023-06-12 11:38:27.000000 torchkeras-3.9.1/torchkeras/utils.py
-drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-08 13:05:37.090039 torchkeras-3.9.1/torchkeras.egg-info/
--rw-r--r--   0 liangyun2   (502) staff       (20)     6646 2023-07-08 13:05:36.000000 torchkeras-3.9.1/torchkeras.egg-info/PKG-INFO
--rw-r--r--   0 liangyun2   (502) staff       (20)      791 2023-07-08 13:05:37.000000 torchkeras-3.9.1/torchkeras.egg-info/SOURCES.txt
--rw-r--r--   0 liangyun2   (502) staff       (20)        1 2023-07-08 13:05:36.000000 torchkeras-3.9.1/torchkeras.egg-info/dependency_links.txt
--rw-r--r--   0 liangyun2   (502) staff       (20)       16 2023-07-08 13:05:36.000000 torchkeras-3.9.1/torchkeras.egg-info/requires.txt
--rw-r--r--   0 liangyun2   (502) staff       (20)       32 2023-07-08 13:05:36.000000 torchkeras-3.9.1/torchkeras.egg-info/top_level.txt
+drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-23 12:17:22.227069 torchkeras-3.9.2/
+-rw-r--r--   0 liangyun2   (502) staff       (20)    11325 2023-02-09 16:00:16.000000 torchkeras-3.9.2/LICENSE
+-rw-r--r--   0 liangyun2   (502) staff       (20)      357 2023-02-09 16:55:42.000000 torchkeras-3.9.2/MANIFEST.in
+-rw-r--r--   0 liangyun2   (502) staff       (20)     7122 2023-07-23 12:17:22.226632 torchkeras-3.9.2/PKG-INFO
+-rw-r--r--   0 liangyun2   (502) staff       (20)    13125 2023-07-23 04:17:19.000000 torchkeras-3.9.2/README.md
+-rw-r--r--   0 liangyun2   (502) staff       (20)       38 2023-07-23 12:17:22.227177 torchkeras-3.9.2/setup.cfg
+-rw-r--r--   0 liangyun2   (502) staff       (20)     1273 2023-06-30 07:06:01.000000 torchkeras-3.9.2/setup.py
+drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-23 12:17:22.198447 torchkeras-3.9.2/torchkeras/
+-rw-r--r--   0 liangyun2   (502) staff       (20)      246 2023-07-23 03:23:40.000000 torchkeras-3.9.2/torchkeras/__init__.py
+drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-23 12:17:22.218750 torchkeras-3.9.2/torchkeras/assets/
+-rw-r--r--   0 liangyun2   (502) staff       (20) 10043912 2023-02-09 16:00:16.000000 torchkeras-3.9.2/torchkeras/assets/SimHei.ttf
+-rw-r--r--   0 liangyun2   (502) staff       (20)  1012077 2023-02-09 16:00:16.000000 torchkeras-3.9.2/torchkeras/assets/park.jpg
+-rw-r--r--   0 liangyun2   (502) staff       (20)   168949 2023-02-09 16:00:16.000000 torchkeras-3.9.2/torchkeras/assets/zidane.jpg
+drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-23 12:17:22.222030 torchkeras-3.9.2/torchkeras/chat/
+-rw-r--r--   0 liangyun2   (502) staff       (20)       57 2023-07-06 21:05:16.000000 torchkeras-3.9.2/torchkeras/chat/__init__.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     2651 2023-07-15 08:08:54.000000 torchkeras-3.9.2/torchkeras/chat/chatglm.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     4178 2023-05-14 01:50:00.000000 torchkeras-3.9.2/torchkeras/chat/chatgpt.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     8621 2023-06-30 01:34:56.000000 torchkeras-3.9.2/torchkeras/data.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     5222 2023-04-13 09:25:41.000000 torchkeras-3.9.2/torchkeras/eda.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     1628 2023-04-13 07:46:39.000000 torchkeras-3.9.2/torchkeras/email.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)    12561 2023-07-14 01:20:16.000000 torchkeras-3.9.2/torchkeras/hugmodel.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)    11284 2023-07-23 00:40:35.000000 torchkeras-3.9.2/torchkeras/kerascallbacks.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)    13985 2023-07-23 00:24:34.000000 torchkeras-3.9.2/torchkeras/kerasmodel.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     7316 2023-02-22 02:34:47.000000 torchkeras-3.9.2/torchkeras/metrics.py
+drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-23 12:17:22.225432 torchkeras-3.9.2/torchkeras/models/
+-rw-r--r--   0 liangyun2   (502) staff       (20)       75 2023-03-10 08:21:36.000000 torchkeras-3.9.2/torchkeras/models/__init__.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     4088 2023-02-24 04:01:48.000000 torchkeras-3.9.2/torchkeras/models/resnet.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)    31333 2023-05-20 15:18:08.000000 torchkeras-3.9.2/torchkeras/models/ssd.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     3374 2023-02-21 12:33:54.000000 torchkeras-3.9.2/torchkeras/models/unet.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     5592 2023-07-19 10:25:15.000000 torchkeras-3.9.2/torchkeras/pbar.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)    10676 2023-06-10 15:29:22.000000 torchkeras-3.9.2/torchkeras/plots.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     5737 2023-05-12 10:11:52.000000 torchkeras-3.9.2/torchkeras/soup.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     5256 2023-05-28 13:14:40.000000 torchkeras-3.9.2/torchkeras/summary.py
+drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-23 12:17:22.226132 torchkeras-3.9.2/torchkeras/tools/
+-rw-r--r--   0 liangyun2   (502) staff       (20)     3740 2023-07-12 02:27:21.000000 torchkeras-3.9.2/torchkeras/tools/catboost.py
+-rw-r--r--   0 liangyun2   (502) staff       (20)     3845 2023-07-19 10:25:57.000000 torchkeras-3.9.2/torchkeras/utils.py
+drwxr-xr-x   0 liangyun2   (502) staff       (20)        0 2023-07-23 12:17:22.201361 torchkeras-3.9.2/torchkeras.egg-info/
+-rw-r--r--   0 liangyun2   (502) staff       (20)     7122 2023-07-23 12:17:22.000000 torchkeras-3.9.2/torchkeras.egg-info/PKG-INFO
+-rw-r--r--   0 liangyun2   (502) staff       (20)      791 2023-07-23 12:17:22.000000 torchkeras-3.9.2/torchkeras.egg-info/SOURCES.txt
+-rw-r--r--   0 liangyun2   (502) staff       (20)        1 2023-07-23 12:17:22.000000 torchkeras-3.9.2/torchkeras.egg-info/dependency_links.txt
+-rw-r--r--   0 liangyun2   (502) staff       (20)       16 2023-07-23 12:17:22.000000 torchkeras-3.9.2/torchkeras.egg-info/requires.txt
+-rw-r--r--   0 liangyun2   (502) staff       (20)       26 2023-07-23 12:17:22.000000 torchkeras-3.9.2/torchkeras.egg-info/top_level.txt
```

### Comparing `torchkeras-3.9.1/LICENSE` & `torchkeras-3.9.2/LICENSE`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/PKG-INFO` & `torchkeras-3.9.2/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torchkeras
-Version: 3.9.1
+Version: 3.9.2
 Summary: pytorch❤️keras
 Home-page: https://github.com/lyhue1991/torchkeras
 Author: PythonAiRoad, Laugh
 Author-email: lyhue1991@163.com
 Keywords: machine-learning,deep-learning,ML,DL,pytorch,torch,keras
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
@@ -117,30 +117,41 @@
 ### 4, Advanced Examples 
 
 In some using cases, because of the differences  of the model input types, you need to rewrite the StepRunner of 
 KerasModel. Here are some examples.
 
 |example|model library  |notebook |
 |:----|:-----------|:-----------:|
+||||
+|**RL**|||
+|ReinforcementLearning——Q-Learning🔥🔥|- |[Q-learning](./examples/Q-learning.ipynb)|
+|ReinforcementLearning——DQN|- |[DQN](./examples/DQN.ipynb)|
+||||
+|**CV**|||
 |ImageClassification——Resnet|  -  | [Resnet](./examples/ResNet.ipynb) |
 |ImageSegmentation——UNet|  - | [UNet](./examples/UNet.ipynb) |
 |ObjectDetection——SSD| -  | [SSD](./examples/SSD.ipynb) |
 |OCR——CRNN 🔥🔥| -  | [CRNN-CTC](./examples/CRNN_CTC.ipynb) |
-|ReinforcementLearning——Q-Learning🔥🔥|- |[Q-learning](./examples/Q-learning.ipynb)|
-|ReinforcementLearning——DQN|- |[DQN](./examples/DQN.ipynb)|
 |ObjectDetection——FasterRCNN| torchvision  |  [FasterRCNN](./examples/FasterRCNN——vision.ipynb) | 
 |ImageSegmentation——DeepLabV3++ | segmentation_models_pytorch |  [Deeplabv3++](./examples/Deeplabv3plus——smp.ipynb) |
 |InstanceSegmentation——MaskRCNN | detectron2 |  [MaskRCNN](./examples/MaskRCNN——detectron2.ipynb) |
 |ObjectDetection——YOLOv8 🔥🔥| ultralytics |  [YOLOv8](./examples/YOLOv8——ultralytics.ipynb) |
+|ImageClassification——SwinTransformer|timm| [Swin](./examples/SwinTransformer——timm.ipynb)|
+||||
+|**NLP**|||
 |TextClassification——BERT 🔥🔥| transformers |  [BERT](./examples/BERT——transformers.ipynb) |
 |TokenClassification——BERT | transformers |  [BERT_NER](./examples/BERT_NER——transformers.ipynb) |
 |FinetuneLLM——ChatGLM2 🔥🔥🔥| transformers |  [ChatGLM2](./examples/ChatGLM2——transformers.ipynb) |
 |FinetuneLLM——ChatGLM2_LoRA 🔥🔥🔥| transformers,peft |  [ChatGLM2_LoRA](./examples/ChatGLM2_LoRA——transformers.ipynb) |
 |FinetuneLLM——ChatGLM2_AdaLoRA 🔥🔥🔥| transformers,peft |  [ChatGLM2_AdaLoRA](./examples/ChatGLM2_AdaLoRA——transformers.ipynb) |
-|ImageClassification——SwinTransformer|timm| [Swin](./examples/SwinTransformer——timm.ipynb)|
+|FinetuneLLM——ChatGLM2_QLoRA 🔥🔥🔥| transformers |  [ChatGLM2_QLoRA_Kaggle](./examples/ChatGLM2_QLoRA_Kaggle——transformers.ipynb) |
+|FinetuneLLM——BaiChuan13B_QLoRA 🔥🔥🔥| transformers |  [BaiChuan13B_QLoRA](./examples/BaiChuan13B_QLoRA——transformers.ipynb) |
+|FinetuneLLM——BaiChuan13B_NER 🔥🔥🔥| transformers |  [BaiChuan13B_NER](./examples/BaiChuan13B_NER——transformers.ipynb) |
+
+
 
 **If you want to understand or modify some details of this project, feel free to read and change the source code!!!**
 
 Any other questions, you can contact the author form the wechat official account below:
 
 **算法美食屋**
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: torchkeras Version: 3.9.1 Summary:
+Metadata-Version: 2.1 Name: torchkeras Version: 3.9.2 Summary:
 pytorchâ¤ï¸keras Home-page: https://github.com/lyhue1991/torchkeras Author:
 PythonAiRoad, Laugh Author-email: lyhue1991@163.com Keywords: machine-
 learning,deep-learning,ML,DL,pytorch,torch,keras Classifier: Programming
 Language :: Python :: 3 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent Requires-Python: >=3.5
 Description-Content-Type: text/markdown License-File: LICENSE #
 Pytorchâ¤ï¸Keras English | [ç®ä½ä¸­æ](README.md) The torchkeras library
@@ -52,34 +52,41 @@
 | [**torchkeras.KerasModel ddp tpu examples**](https://www.kaggle.com/code/
 lyhue1991/torchkeras-ddp-tpu-examples) |
 [Open_In_Kaggle]
 
 | ### 4, Advanced Examples In some using cases, because of the differences of
 the model input types, you need to rewrite the StepRunner of KerasModel. Here
 are some examples. |example|model library |notebook | |:----|:-----------|:----
--------:| |ImageClassificationââResnet| - | [Resnet](./examples/
-ResNet.ipynb) | |ImageSegmentationââUNet| - | [UNet](./examples/UNet.ipynb)
-| |ObjectDetectionââSSD| - | [SSD](./examples/SSD.ipynb) | |OCRââCRNN
-ð¥ð¥| - | [CRNN-CTC](./examples/CRNN_CTC.ipynb) |
-|ReinforcementLearningââQ-Learningð¥ð¥|- |[Q-learning](./examples/Q-
-learning.ipynb)| |ReinforcementLearningââDQN|- |[DQN](./examples/
-DQN.ipynb)| |ObjectDetectionââFasterRCNN| torchvision | [FasterRCNN](./
-examples/FasterRCNNââvision.ipynb) | |ImageSegmentationââDeepLabV3++ |
-segmentation_models_pytorch | [Deeplabv3++](./examples/
+-------:| |||| |**RL**||| |ReinforcementLearningââQ-Learningð¥ð¥|- |[Q-
+learning](./examples/Q-learning.ipynb)| |ReinforcementLearningââDQN|- |
+[DQN](./examples/DQN.ipynb)| |||| |**CV**||| |ImageClassificationââResnet|
+- | [Resnet](./examples/ResNet.ipynb) | |ImageSegmentationââUNet| - |
+[UNet](./examples/UNet.ipynb) | |ObjectDetectionââSSD| - | [SSD](./
+examples/SSD.ipynb) | |OCRââCRNN ð¥ð¥| - | [CRNN-CTC](./examples/
+CRNN_CTC.ipynb) | |ObjectDetectionââFasterRCNN| torchvision | [FasterRCNN]
+(./examples/FasterRCNNââvision.ipynb) | |ImageSegmentationââDeepLabV3++
+| segmentation_models_pytorch | [Deeplabv3++](./examples/
 Deeplabv3plusââsmp.ipynb) | |InstanceSegmentationââMaskRCNN |
 detectron2 | [MaskRCNN](./examples/MaskRCNNââdetectron2.ipynb) |
 |ObjectDetectionââYOLOv8 ð¥ð¥| ultralytics | [YOLOv8](./examples/
-YOLOv8ââultralytics.ipynb) | |TextClassificationââBERT ð¥ð¥|
-transformers | [BERT](./examples/BERTââtransformers.ipynb) |
-|TokenClassificationââBERT | transformers | [BERT_NER](./examples/
-BERT_NERââtransformers.ipynb) | |FinetuneLLMââChatGLM2 ð¥ð¥ð¥|
-transformers | [ChatGLM2](./examples/ChatGLM2ââtransformers.ipynb) |
-|FinetuneLLMââChatGLM2_LoRA ð¥ð¥ð¥| transformers,peft |
-[ChatGLM2_LoRA](./examples/ChatGLM2_LoRAââtransformers.ipynb) |
-|FinetuneLLMââChatGLM2_AdaLoRA ð¥ð¥ð¥| transformers,peft |
-[ChatGLM2_AdaLoRA](./examples/ChatGLM2_AdaLoRAââtransformers.ipynb) |
+YOLOv8ââultralytics.ipynb) |
 |ImageClassificationââSwinTransformer|timm| [Swin](./examples/
-SwinTransformerââtimm.ipynb)| **If you want to understand or modify some
-details of this project, feel free to read and change the source code!!!** Any
-other questions, you can contact the author form the wechat official account
-below: **ç®æ³ç¾é£å±** ![](https://tva1.sinaimg.cn/large/
-e6c9d24egy1h41m2zugguj20k00b9q46.jpg)
+SwinTransformerââtimm.ipynb)| |||| |**NLP**|||
+|TextClassificationââBERT ð¥ð¥| transformers | [BERT](./examples/
+BERTââtransformers.ipynb) | |TokenClassificationââBERT | transformers |
+[BERT_NER](./examples/BERT_NERââtransformers.ipynb) |
+|FinetuneLLMââChatGLM2 ð¥ð¥ð¥| transformers | [ChatGLM2](./examples/
+ChatGLM2ââtransformers.ipynb) | |FinetuneLLMââChatGLM2_LoRA
+ð¥ð¥ð¥| transformers,peft | [ChatGLM2_LoRA](./examples/
+ChatGLM2_LoRAââtransformers.ipynb) | |FinetuneLLMââChatGLM2_AdaLoRA
+ð¥ð¥ð¥| transformers,peft | [ChatGLM2_AdaLoRA](./examples/
+ChatGLM2_AdaLoRAââtransformers.ipynb) | |FinetuneLLMââChatGLM2_QLoRA
+ð¥ð¥ð¥| transformers | [ChatGLM2_QLoRA_Kaggle](./examples/
+ChatGLM2_QLoRA_Kaggleââtransformers.ipynb) |
+|FinetuneLLMââBaiChuan13B_QLoRA ð¥ð¥ð¥| transformers |
+[BaiChuan13B_QLoRA](./examples/BaiChuan13B_QLoRAââtransformers.ipynb) |
+|FinetuneLLMââBaiChuan13B_NER ð¥ð¥ð¥| transformers |
+[BaiChuan13B_NER](./examples/BaiChuan13B_NERââtransformers.ipynb) | **If
+you want to understand or modify some details of this project, feel free to
+read and change the source code!!!** Any other questions, you can contact the
+author form the wechat official account below: **ç®æ³ç¾é£å±** ![](https://
+tva1.sinaimg.cn/large/e6c9d24egy1h41m2zugguj20k00b9q46.jpg)
```

### Comparing `torchkeras-3.9.1/README.md` & `torchkeras-3.9.2/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -269,29 +269,38 @@
 * timm
 
 > 如果你想掌握一个东西，那么就去使用它，如果你想真正理解一个东西，那么尝试去改变它。 ———— 爱因斯坦
 
 
 |example|使用模型库  |notebook |
 |:----|:-----------|:-----------:|
+||||
+|**RL**|||
+|强化学习——Q-Learning 🔥🔥|- |[Q-learning](./examples/Q-learning.ipynb)|
+|强化学习——DQN|- |[DQN](./examples/DQN.ipynb)|
+||||
+|**CV**|||
 |图片分类——Resnet|  -  | [Resnet](./examples/ResNet.ipynb) |
 |语义分割——UNet|  - | [UNet](./examples/UNet.ipynb) |
 |目标检测——SSD| -  | [SSD](./examples/SSD.ipynb) |
 |文字识别——CRNN 🔥🔥| -  | [CRNN-CTC](./examples/CRNN_CTC.ipynb) |
-|强化学习——Q-Learning|- |[Q-learning](./examples/Q-learning.ipynb)|
-|强化学习——DQN|- |[DQN](./examples/DQN.ipynb)|
 |目标检测——FasterRCNN| torchvision  |  [FasterRCNN](./examples/FasterRCNN——vision.ipynb) | 
-|语义分割——DeepLabV3++ 🔥| segmentation_models_pytorch |  [Deeplabv3++](./examples/Deeplabv3plus——smp.ipynb) |
-|实例分割——MaskRCNN 🔥🔥| detectron2 |  [MaskRCNN](./examples/MaskRCNN——detectron2.ipynb) |
+|语义分割——DeepLabV3++ | segmentation_models_pytorch |  [Deeplabv3++](./examples/Deeplabv3plus——smp.ipynb) |
+|实例分割——MaskRCNN | detectron2 |  [MaskRCNN](./examples/MaskRCNN——detectron2.ipynb) |
 |目标检测——YOLOv8 🔥🔥| ultralytics |  [YOLOv8](./examples/YOLOv8——ultralytics.ipynb) |
-|文本分类——BERT 🔥| transformers |  [BERT](./examples/BERT——transformers.ipynb) |
-|命名实体识别——BERT | transformers |  [BERT_NER](./examples/BERT_NER——transformers.ipynb) |
-|LLM微调——ChatGLM2_LoRA 🔥🔥🔥| transformers,peft |  [ChatGLM2_LoRA](./examples/ChatGLM2_LoRA——transformers.ipynb) |
-|LLM微调——ChatGLM2_AdaLoRA 🔥🔥🔥| transformers,peft |  [ChatGLM2_AdaLoRA](./examples/ChatGLM2_AdaLoRA——transformers.ipynb) |
 |图片分类——SwinTransformer|timm| [Swin](./examples/SwinTransformer——timm.ipynb)|
+||||
+|**NLP**|||
+|文本分类——BERT🔥| transformers |  [BERT](./examples/BERT——transformers.ipynb) |
+|命名实体识别——BERT | transformers |  [BERT_NER](./examples/BERT_NER——transformers.ipynb) |
+|LLM微调——ChatGLM2_LoRA 🔥🔥🔥| transformers |  [ChatGLM2_LoRA](./examples/ChatGLM2_LoRA——transformers.ipynb) |
+|LLM微调——ChatGLM2_AdaLoRA 🔥🔥🔥| transformers |  [ChatGLM2_AdaLoRA](./examples/ChatGLM2_AdaLoRA——transformers.ipynb) |
+|LLM微调——ChatGLM2_QLoRA 🔥🔥🔥| transformers |  [ChatGLM2_QLoRA_Kaggle](./examples/ChatGLM2_QLoRA_Kaggle——transformers.ipynb) |
+|LLM微调——BaiChuan13B_QLoRA 🔥🔥🔥| transformers |  [BaiChuan13B_QLoRA](./examples/BaiChuan13B_QLoRA——transformers.ipynb) |
+|LLM微调——BaiChuan13B_NER 🔥🔥🔥| transformers |  [BaiChuan13B_NER](./examples/BaiChuan13B_NER——transformers.ipynb) |
 
 
 ```python
 
 ```
 
 ## 7，鼓励和联系作者 🎈🎈
```

### Comparing `torchkeras-3.9.1/setup.py` & `torchkeras-3.9.2/setup.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/assets/SimHei.ttf` & `torchkeras-3.9.2/torchkeras/assets/SimHei.ttf`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/assets/park.jpg` & `torchkeras-3.9.2/torchkeras/assets/park.jpg`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/assets/zidane.jpg` & `torchkeras-3.9.2/torchkeras/assets/zidane.jpg`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/chat/chatglm.py` & `torchkeras-3.9.2/torchkeras/chat/chatglm.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,11 +1,13 @@
+from IPython.display import display,clear_output 
 class ChatGLM(object):
     def __init__(self,
                  model,
                  tokenizer,
+                 stream=True,
                  max_chat_rounds=20,
                  history=None,
                  max_length=8192,
                  num_beams=1,
                  do_sample=True,
                  top_p=0.8,
                  temperature=0.8,
@@ -19,29 +21,42 @@
             self.register_magic() 
             print('register magic %%chatglm sucessed ...')
         except Exception as err:
             print('register magic %%chatglm failed ...')
             print(err)
         
         response = self('你好')
-        print(response)
+        if not self.stream:
+            print(response)
         self.history = self.history[:-1]
 
     
     def __call__(self,query):
         len_his = len(self.history)
         if len_his>=self.max_chat_rounds+1:
             self.history = self.history[len_his-self.max_chat_rounds:]
-            
-        response,self.history  = self.model.chat(self.tokenizer,
-            query,self.history,self.max_length,self.num_beams,
+        
+        if not self.stream:
+            response,self.history  = self.model.chat(self.tokenizer,
+             query,self.history,self.max_length,self.num_beams,
+             self.do_sample,self.top_p,self.temperature,
+             self.logits_processor)
+            return response 
+        
+        result = self.model.stream_chat(self.tokenizer,
+            query,self.history,None,self.max_length,
             self.do_sample,self.top_p,self.temperature,
-            self.logits_processor)
-
-        return response 
+            self.logits_processor,None)
+        
+        for response,history in result:
+            print(response)
+            clear_output(wait=True)
+        self.history = history
+        #clear_output(waite=True)
+        return response
     
     def register_magic(self):
         import IPython
         from IPython.core.magic import (Magics, magics_class, line_magic,
                                         cell_magic, line_cell_magic)
         @magics_class
         class ChatGLMMagics(Magics):
```

### Comparing `torchkeras-3.9.1/torchkeras/chat/chatgpt.py` & `torchkeras-3.9.2/torchkeras/chat/chatgpt.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/data.py` & `torchkeras-3.9.2/torchkeras/data.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/eda.py` & `torchkeras-3.9.2/torchkeras/eda.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/email.py` & `torchkeras-3.9.2/torchkeras/email.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/hugmodel.py` & `torchkeras-3.9.2/torchkeras/hugmodel.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,15 +1,17 @@
 import torch
 from transformers import Trainer,TrainingArguments,EarlyStoppingCallback,TrainerCallback
+from transformers.modeling_utils import PreTrainedModel
+from transformers.utils import is_peft_available
 import numpy as np
 import pandas as pd 
 import os 
 import matplotlib.pyplot as plt 
-from .utils import is_jupyter
-    
+from torchkeras.utils import is_jupyter
+
 class HugModel(torch.nn.Module):
     def __init__(self, net=None, loss_fn=None, metrics_dict=None, 
                  label_names = None, feature_names = None):
         super().__init__()
         self.net,self.loss_fn = net,loss_fn
         self.metrics_dict = metrics_dict if metrics_dict is not None else {}
         
@@ -47,15 +49,15 @@
                 labels = {k:batch[k] for k in self.label_names}
                 
             loss = self.loss_fn(logits,labels)
             out = {'logits':logits,'loss':loss}
             return out 
 
     
-    #==========================================================================================        
+    #========================================================================================== 
     #The codes below usually need not be changed... 
     #==========================================================================================
     
     def compute_metrics(self, eval_preds):
         logits,labels = eval_preds
         for k,m in self.metrics_dict.items():
             m(torch.from_numpy(logits),torch.from_numpy(labels))
@@ -141,37 +143,52 @@
             eval_dataset=val_data.dataset,
             compute_metrics=self.compute_metrics,
             callbacks = callbacks,
             data_collator=self.get_collate_fn(train_data.collate_fn)
         )
         
         self.trainer.train()
+        
+        #save best ckpt
+        self.ckpt_path = os.path.join(output_dir,'best')
+        self.save_ckpt(self.ckpt_path)
                 
         if wandb:
-            ckpt_path = os.path.join(output_dir,'best.ckpt')
-            self.save_ckpt(ckpt_path)
             arti_model = wb.Artifact('checkpoint', type='model')
-            arti_model.add_file(ckpt_path)
+            arti_model.add_file(self.ckpt_path)
             wb.log_artifact(arti_model)
             wb.finish()
             
-        
     def evaluate(self,val_data,**kwargs):  
         dl_val = self.trainer.get_eval_dataloader(val_data.dataset)
         out = self.trainer.evaluation_loop(dl_val,
             description = self.prefix,prediction_loss_only= False,metric_key_prefix =self.prefix).metrics 
         return out 
     
     
     def save_ckpt(self, ckpt_path):
-        torch.save(self.net.state_dict(),ckpt_path)
-        
+        supported_classes = [PreTrainedModel]
+        if is_peft_available():
+            from peft import PeftModel
+            supported_classes.append(PeftModel)
+        supported_classes = tuple(supported_classes)
+        if isinstance(self.net,supported_classes) and self.trainer is not None:
+            self.trainer.save_model(ckpt_path)
+        else:
+            torch.save(self.net.state_dict(),ckpt_path)
+     
     def load_ckpt(self, ckpt_path):
-        self.net.load_state_dict(torch.load(ckpt_path))
-    
+        if is_peft_available():
+            from peft import PeftModel
+            if isinstance(self.net, PeftModel):
+                self.net = self.net.from_pretrained(self.net.base_model.model,ckpt_path)
+        elif isinstance(self.net,PreTrainedModel):
+            self.net = self.net.from_pretrained(ckpt_path)
+        else:
+            self.net.load_state_dict(torch.load(ckpt_path))
     
     def debug(self):
         # if it raises some errors when fitting model,  these codes are useful to debug.
         trainer = self.trainer
         
         print('step1: check label_names.')
         print('label_names = ', trainer.label_names, '\n')
@@ -195,95 +212,97 @@
         print('loss = ',loss,'\n')
 
         print('step5: check trainer.evaluation_loop')
         out = trainer.evaluation_loop(dl_val,
                  description = self.prefix,metric_key_prefix =self.prefix)
         print('metrics:',out.metrics)
 
-
-
 class VisCallback(TrainerCallback):
     def __init__(self, figsize=(6,4), update_freq=1, monitor=None):
         self.figsize = figsize
         self.update_freq = update_freq
         self.monitor = monitor
 
     def on_train_begin(self, args, state, control, **kwargs):
         metric = args.metric_for_best_model
+        self.greater_is_better = args.greater_is_better 
         self.prefix = 'val_' if self.monitor is None or self.monitor.startswith('val_') else 'eval_'
         self.metric = metric if self.monitor is None else self.monitor
         
         dfhistory = pd.DataFrame()
         x_bounds = [0, args.logging_steps*10]
-        title = f'best {self.metric} = ?'
         self.update_graph(dfhistory, self.metric.replace(self.prefix,''), 
                              x_bounds = x_bounds, 
-                             title=title, 
                              figsize = self.figsize)
         
     def on_evaluate(self, args, state, control, metrics, **kwargs):
         dfhistory = self.get_history(state)
         n = dfhistory['step'].max()
         if n%self.update_freq==0:
             x_bounds = [dfhistory['step'].min(), 
                         10*args.logging_steps+(n//(args.logging_steps*10))*args.logging_steps*10]
-            arr_scores = dfhistory[self.metric]
-            best_score = np.max(arr_scores) if args.greater_is_better==True else np.min(arr_scores)
-
-            title = f'best {self.metric} = {best_score:.4f}'
             self.update_graph(dfhistory, self.metric.replace(self.prefix,''), 
-                              x_bounds = x_bounds, title = title, figsize = self.figsize)
+                              x_bounds = x_bounds, figsize = self.figsize)
             
     def on_train_end(self, args, state, control, **kwargs):
         dfhistory = self.get_history(state)
-        arr_scores = dfhistory[self.metric]
-        best_score = np.max(arr_scores) if args.greater_is_better==True else np.min(arr_scores)
-        title = f'best {self.metric} = {best_score:.4f}'
         self.update_graph(dfhistory, self.metric.replace(self.prefix,''), 
-                             title = title, figsize = self.figsize)
-        plt.close()
+                             figsize = self.figsize)
         
     def get_history(self,state):
         log_history = state.log_history  
         train_history = [x for x in log_history if 'loss' in x.keys()]
         eval_history = [x for x in log_history if 'eval_loss'  in x.keys()]
 
         dfhistory_train = pd.DataFrame(train_history)
         dfhistory_eval = pd.DataFrame(eval_history)  
         dfhistory = dfhistory_train.merge(dfhistory_eval,on=['step','epoch'])
         if self.prefix=='val_':
             dfhistory.columns = [x.replace('eval_','val_') for x in dfhistory.columns]
         return dfhistory
-        
+    
+    def get_best_score(self, dfhistory):
+        arr_scores = dfhistory[self.metric]
+        best_score = np.max(arr_scores) if self.greater_is_better==True else np.min(arr_scores)
+        best_step = dfhistory.loc[arr_scores==best_score,'step'].tolist()[0]
+        return (best_step, best_score)
+
     def update_graph(self, dfhistory, metric, x_bounds=None, 
-                     y_bounds=None, title = None, figsize=(6,4)):
+                     y_bounds=None, figsize=(6,4)):
         
         from IPython.display import display
         if not hasattr(self, 'graph_fig'):
             self.graph_fig, self.graph_ax = plt.subplots(1, figsize=figsize)
             self.graph_out = display(self.graph_ax.figure, display_id=True)
 
         self.graph_ax.clear()
         steps = dfhistory['step'] if 'step' in dfhistory.columns else []
 
         m1 = metric
         if  m1 in dfhistory.columns:
             train_metrics = dfhistory[m1]
-            self.graph_ax.plot(steps,train_metrics,'bo--',label= m1)
+            self.graph_ax.plot(steps,train_metrics,'bo--',label= m1,clip_on=False)
 
         m2 = self.prefix+metric
         if m2 in dfhistory.columns:
             val_metrics = dfhistory[m2]
-            self.graph_ax.plot(steps,val_metrics,'ro-',label =m2)
+            self.graph_ax.plot(steps,val_metrics,'co-',label =m2,clip_on=False)
 
         self.graph_ax.set_xlabel("step")
         self.graph_ax.set_ylabel(metric)  
 
-        if title:
-             self.graph_ax.set_title(title)
-
         if m1 in dfhistory.columns or m2 in dfhistory.columns or metric in dfhistory.columns:
             self.graph_ax.legend(loc='best')
-
+            
+        if len(steps)>0:
+            best_step, best_score = self.get_best_score(dfhistory)
+            self.graph_ax.plot(best_step,best_score,'r*',markersize=15,clip_on=False)
+            title = f'best {self.metric} = {best_score:.4f} (@step {best_step})'
+            self.graph_ax.set_title(title)
+        else:
+            title = f'best {self.metric} = ?'
+            self.graph_ax.set_title(title)
+            
         if x_bounds is not None: self.graph_ax.set_xlim(*x_bounds)
         if y_bounds is not None: self.graph_ax.set_ylim(*y_bounds)
-        self.graph_out.update(self.graph_ax.figure);
+        self.graph_out.update(self.graph_ax.figure);
+        plt.close();
```

### Comparing `torchkeras-3.9.1/torchkeras/kerascallbacks.py` & `torchkeras-3.9.2/torchkeras/kerascallbacks.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 import os 
 import sys
 import datetime 
 from copy import deepcopy
 import numpy as np 
 import pandas as pd 
 from argparse import Namespace 
+from torchkeras.utils import is_jupyter
 
 class TensorBoardCallback:
     def __init__(self, save_dir= "runs", model_name="model", 
                  log_weight=False, log_weight_freq=5):
         from torch.utils.tensorboard import SummaryWriter 
         self.__dict__.update(locals())
         nowtime = datetime.datetime.now().strftime('%Y%m%d_%H%M%S')
@@ -150,16 +151,19 @@
     def on_fit_end(self,  model:"KerasModel"):
         dfhistory = pd.DataFrame(model.history)
         if dfhistory['epoch'].max()<model.epochs:
             self.progress.on_interrupt(msg='earlystopping')
         self.progress.display=False
             
 class VisMetric:
-    def __init__(self,figsize = (6,4)):
+    def __init__(self,figsize = (6,4),
+                 save_path='history.png'):
         self.figsize = (6,4)
+        self.save_path = save_path
+        self.in_jupyter = is_jupyter()
         
     def on_fit_start(self,model: 'KerasModel'):
         self.metric =  model.monitor.replace('val_','')
         dfhistory = pd.DataFrame(model.history)
         x_bounds = [0, min(10,model.epochs)]
         title = f'best {model.monitor} = ?'
         self.update_graph(model, title=title, x_bounds = x_bounds)
@@ -193,48 +197,52 @@
         return title
 
     def update_graph(self, model:'KerasModel', title=None, x_bounds=None, y_bounds=None):
         import matplotlib.pyplot as plt
         self.plt = plt
         if not hasattr(self, 'graph_fig'):
             self.graph_fig, self.graph_ax = plt.subplots(1, figsize=self.figsize)
-            self.graph_out = display(self.graph_ax.figure, display_id=True)
+            if self.in_jupyter:
+                self.graph_out = display(self.graph_ax.figure, display_id=True)
         self.graph_ax.clear()
         
         dfhistory = pd.DataFrame(model.history)
         epochs = dfhistory['epoch'] if 'epoch' in dfhistory.columns else []
         
         m1 = "train_"+self.metric
         if  m1 in dfhistory.columns:
             train_metrics = dfhistory[m1]
-            self.graph_ax.plot(epochs,train_metrics,'bo--',label= m1)
+            self.graph_ax.plot(epochs,train_metrics,'bo--',label= m1,clip_on=False)
 
         m2 = 'val_'+self.metric
         if m2 in dfhistory.columns:
             val_metrics = dfhistory[m2]
-            self.graph_ax.plot(epochs,val_metrics,'co-',label =m2)
+            self.graph_ax.plot(epochs,val_metrics,'co-',label =m2,clip_on=False)
 
         if self.metric in dfhistory.columns:
             metric_values = dfhistory[self.metric]
-            self.graph_ax.plot(epochs, metric_values,'co-', label = self.metric)
+            self.graph_ax.plot(epochs, metric_values,'co-', label = self.metric,clip_on=False)
 
         self.graph_ax.set_xlabel("epoch")
         self.graph_ax.set_ylabel(self.metric)  
         if title:
              self.graph_ax.set_title(title)
         if m1 in dfhistory.columns or m2 in dfhistory.columns or self.metric in dfhistory.columns:
             self.graph_ax.legend(loc='best')
             
         if len(epochs)>0:
             best_epoch, best_score = self.get_best_score(model)
-            self.graph_ax.plot(best_epoch,best_score,'r*',markersize=15)
+            self.graph_ax.plot(best_epoch,best_score,'r*',markersize=15,clip_on=False)
 
         if x_bounds is not None: self.graph_ax.set_xlim(*x_bounds)
         if y_bounds is not None: self.graph_ax.set_ylim(*y_bounds)
-        self.graph_out.update(self.graph_ax.figure)
+        if self.in_jupyter:
+            self.graph_out.update(self.graph_ax.figure)
+        else:
+            self.graph_fig.savefig(self.save_path)
         self.plt.close();
         
 
 class VisDisplay:
     def __init__(self,display_fn,model=None,init_display=True,dis_period=1):
         from ipywidgets import Output 
         self.display_fn = display_fn
```

### Comparing `torchkeras-3.9.1/torchkeras/kerasmodel.py` & `torchkeras-3.9.2/torchkeras/kerasmodel.py`

 * *Files 1% similar despite different names*

```diff
@@ -23,15 +23,15 @@
         
         #loss
         with self.accelerator.autocast():
             preds = self.net(features)
             loss = self.loss_fn(preds,labels)
 
         #backward()
-        if self.optimizer is not None and self.stage=="train":
+        if self.stage=="train" and self.optimizer is not None:
             self.accelerator.backward(loss)
             if self.accelerator.sync_gradients:
                 self.accelerator.clip_grad_norm_(self.net.parameters(), 1.0)
             self.optimizer.step()
             if self.lr_scheduler is not None:
                 self.lr_scheduler.step()
             self.optimizer.zero_grad()
@@ -151,18 +151,21 @@
         if val_data:
             val_dataloader.size = val_data.size if hasattr(val_data,'size') else len(val_data)
         
         
         self.history = {}
         callbacks = callbacks if callbacks is not None else []
         
-        if bool(plot) and is_jupyter():
-            from torchkeras.kerascallbacks import VisMetric,VisProgress
-            callbacks = [VisMetric(),VisProgress()]+callbacks
-                
+        if bool(plot):
+            if is_jupyter():
+                from torchkeras.kerascallbacks import VisProgress
+                callbacks = [VisProgress()]+callbacks
+            from torchkeras.kerascallbacks import VisMetric
+            callbacks = [VisMetric()]+callbacks
+            
         if wandb!=False:
             from torchkeras.kerascallbacks import WandbCallback
             project = wandb if isinstance(wandb,str) else 'torchkeras'
             callbacks.append(WandbCallback(project=project))
             
         self.callbacks = [self.accelerator.prepare(x) for x in callbacks]
```

### Comparing `torchkeras-3.9.1/torchkeras/metrics.py` & `torchkeras-3.9.2/torchkeras/metrics.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/models/resnet.py` & `torchkeras-3.9.2/torchkeras/models/resnet.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/models/ssd.py` & `torchkeras-3.9.2/torchkeras/models/ssd.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/models/unet.py` & `torchkeras-3.9.2/torchkeras/models/unet.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/pbar.py` & `torchkeras-3.9.2/torchkeras/pbar.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,21 +1,28 @@
 
 '''
 reference from https://github.com/fastai/fastprogress/
 '''
 import time
 from IPython.display import clear_output, display, HTML
 
+
 def format_time(t):
     "Format `t` (in seconds) to (h):mm:ss"
     t = int(t)
     h,m,s = t//3600, (t//60)%60, t%60
     if h!= 0: return f'{h}:{m:02d}:{s:02d}'
     else:     return f'{m:02d}:{s:02d}'
 
+def format_number(x):
+    if abs(x)<1e-4 or abs(x)>=1e5:
+        return "{:.4e}".format(x)
+    else:
+        return "{:.4f}".format(x)
+
 html_progress_bar_styles = """
 <style>
     /* background: */
     progress::-webkit-progress-bar {background-color: #CDCDCD; width: 100%;}
     progress {background-color: #CDCDCD;}
 
     /* value: */
@@ -133,13 +140,13 @@
             postfix+=format(Bar(ratio,default_len=20))
             postfix+=f'{100 * i/n:.2f}%'
             postfix+=f' [{i}/{n}] '
         if kwargs:
             postfix+='['
             for i,(key,value) in enumerate(kwargs.items()):
                 if isinstance(value,float):
-                    postfix = postfix+f'{key}={value:.5f},'
+                    postfix = postfix+f'{key}={format_number(value)},'
                 else:
                     postfix = postfix+f'{key}={value},'
             postfix = postfix[:-1]+']'
         self.postfix = postfix
         self.on_update(self.last_v,self.comment,self.postfix)
```

### Comparing `torchkeras-3.9.1/torchkeras/plots.py` & `torchkeras-3.9.2/torchkeras/plots.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/soup.py` & `torchkeras-3.9.2/torchkeras/soup.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/summary.py` & `torchkeras-3.9.2/torchkeras/summary.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/tools/catboost.py` & `torchkeras-3.9.2/torchkeras/tools/catboost.py`

 * *Files identical despite different names*

### Comparing `torchkeras-3.9.1/torchkeras/utils.py` & `torchkeras-3.9.2/torchkeras/utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -106,15 +106,15 @@
         if not isinstance(v,Namespace):
             result[k] = v
         else:
             v_dic = namespace2dict(v)
             for v_key,v_value in v_dic.items():
                 result[k+"."+v_key] = v_value
     return result 
-
+  
 
 def is_jupyter():
     import contextlib
     with contextlib.suppress(Exception):
         from IPython import get_ipython
         return get_ipython() is not None
     return False
```

### Comparing `torchkeras-3.9.1/torchkeras.egg-info/PKG-INFO` & `torchkeras-3.9.2/torchkeras.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torchkeras
-Version: 3.9.1
+Version: 3.9.2
 Summary: pytorch❤️keras
 Home-page: https://github.com/lyhue1991/torchkeras
 Author: PythonAiRoad, Laugh
 Author-email: lyhue1991@163.com
 Keywords: machine-learning,deep-learning,ML,DL,pytorch,torch,keras
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
@@ -117,30 +117,41 @@
 ### 4, Advanced Examples 
 
 In some using cases, because of the differences  of the model input types, you need to rewrite the StepRunner of 
 KerasModel. Here are some examples.
 
 |example|model library  |notebook |
 |:----|:-----------|:-----------:|
+||||
+|**RL**|||
+|ReinforcementLearning——Q-Learning🔥🔥|- |[Q-learning](./examples/Q-learning.ipynb)|
+|ReinforcementLearning——DQN|- |[DQN](./examples/DQN.ipynb)|
+||||
+|**CV**|||
 |ImageClassification——Resnet|  -  | [Resnet](./examples/ResNet.ipynb) |
 |ImageSegmentation——UNet|  - | [UNet](./examples/UNet.ipynb) |
 |ObjectDetection——SSD| -  | [SSD](./examples/SSD.ipynb) |
 |OCR——CRNN 🔥🔥| -  | [CRNN-CTC](./examples/CRNN_CTC.ipynb) |
-|ReinforcementLearning——Q-Learning🔥🔥|- |[Q-learning](./examples/Q-learning.ipynb)|
-|ReinforcementLearning——DQN|- |[DQN](./examples/DQN.ipynb)|
 |ObjectDetection——FasterRCNN| torchvision  |  [FasterRCNN](./examples/FasterRCNN——vision.ipynb) | 
 |ImageSegmentation——DeepLabV3++ | segmentation_models_pytorch |  [Deeplabv3++](./examples/Deeplabv3plus——smp.ipynb) |
 |InstanceSegmentation——MaskRCNN | detectron2 |  [MaskRCNN](./examples/MaskRCNN——detectron2.ipynb) |
 |ObjectDetection——YOLOv8 🔥🔥| ultralytics |  [YOLOv8](./examples/YOLOv8——ultralytics.ipynb) |
+|ImageClassification——SwinTransformer|timm| [Swin](./examples/SwinTransformer——timm.ipynb)|
+||||
+|**NLP**|||
 |TextClassification——BERT 🔥🔥| transformers |  [BERT](./examples/BERT——transformers.ipynb) |
 |TokenClassification——BERT | transformers |  [BERT_NER](./examples/BERT_NER——transformers.ipynb) |
 |FinetuneLLM——ChatGLM2 🔥🔥🔥| transformers |  [ChatGLM2](./examples/ChatGLM2——transformers.ipynb) |
 |FinetuneLLM——ChatGLM2_LoRA 🔥🔥🔥| transformers,peft |  [ChatGLM2_LoRA](./examples/ChatGLM2_LoRA——transformers.ipynb) |
 |FinetuneLLM——ChatGLM2_AdaLoRA 🔥🔥🔥| transformers,peft |  [ChatGLM2_AdaLoRA](./examples/ChatGLM2_AdaLoRA——transformers.ipynb) |
-|ImageClassification——SwinTransformer|timm| [Swin](./examples/SwinTransformer——timm.ipynb)|
+|FinetuneLLM——ChatGLM2_QLoRA 🔥🔥🔥| transformers |  [ChatGLM2_QLoRA_Kaggle](./examples/ChatGLM2_QLoRA_Kaggle——transformers.ipynb) |
+|FinetuneLLM——BaiChuan13B_QLoRA 🔥🔥🔥| transformers |  [BaiChuan13B_QLoRA](./examples/BaiChuan13B_QLoRA——transformers.ipynb) |
+|FinetuneLLM——BaiChuan13B_NER 🔥🔥🔥| transformers |  [BaiChuan13B_NER](./examples/BaiChuan13B_NER——transformers.ipynb) |
+
+
 
 **If you want to understand or modify some details of this project, feel free to read and change the source code!!!**
 
 Any other questions, you can contact the author form the wechat official account below:
 
 **算法美食屋**
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: torchkeras Version: 3.9.1 Summary:
+Metadata-Version: 2.1 Name: torchkeras Version: 3.9.2 Summary:
 pytorchâ¤ï¸keras Home-page: https://github.com/lyhue1991/torchkeras Author:
 PythonAiRoad, Laugh Author-email: lyhue1991@163.com Keywords: machine-
 learning,deep-learning,ML,DL,pytorch,torch,keras Classifier: Programming
 Language :: Python :: 3 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent Requires-Python: >=3.5
 Description-Content-Type: text/markdown License-File: LICENSE #
 Pytorchâ¤ï¸Keras English | [ç®ä½ä¸­æ](README.md) The torchkeras library
@@ -52,34 +52,41 @@
 | [**torchkeras.KerasModel ddp tpu examples**](https://www.kaggle.com/code/
 lyhue1991/torchkeras-ddp-tpu-examples) |
 [Open_In_Kaggle]
 
 | ### 4, Advanced Examples In some using cases, because of the differences of
 the model input types, you need to rewrite the StepRunner of KerasModel. Here
 are some examples. |example|model library |notebook | |:----|:-----------|:----
--------:| |ImageClassificationââResnet| - | [Resnet](./examples/
-ResNet.ipynb) | |ImageSegmentationââUNet| - | [UNet](./examples/UNet.ipynb)
-| |ObjectDetectionââSSD| - | [SSD](./examples/SSD.ipynb) | |OCRââCRNN
-ð¥ð¥| - | [CRNN-CTC](./examples/CRNN_CTC.ipynb) |
-|ReinforcementLearningââQ-Learningð¥ð¥|- |[Q-learning](./examples/Q-
-learning.ipynb)| |ReinforcementLearningââDQN|- |[DQN](./examples/
-DQN.ipynb)| |ObjectDetectionââFasterRCNN| torchvision | [FasterRCNN](./
-examples/FasterRCNNââvision.ipynb) | |ImageSegmentationââDeepLabV3++ |
-segmentation_models_pytorch | [Deeplabv3++](./examples/
+-------:| |||| |**RL**||| |ReinforcementLearningââQ-Learningð¥ð¥|- |[Q-
+learning](./examples/Q-learning.ipynb)| |ReinforcementLearningââDQN|- |
+[DQN](./examples/DQN.ipynb)| |||| |**CV**||| |ImageClassificationââResnet|
+- | [Resnet](./examples/ResNet.ipynb) | |ImageSegmentationââUNet| - |
+[UNet](./examples/UNet.ipynb) | |ObjectDetectionââSSD| - | [SSD](./
+examples/SSD.ipynb) | |OCRââCRNN ð¥ð¥| - | [CRNN-CTC](./examples/
+CRNN_CTC.ipynb) | |ObjectDetectionââFasterRCNN| torchvision | [FasterRCNN]
+(./examples/FasterRCNNââvision.ipynb) | |ImageSegmentationââDeepLabV3++
+| segmentation_models_pytorch | [Deeplabv3++](./examples/
 Deeplabv3plusââsmp.ipynb) | |InstanceSegmentationââMaskRCNN |
 detectron2 | [MaskRCNN](./examples/MaskRCNNââdetectron2.ipynb) |
 |ObjectDetectionââYOLOv8 ð¥ð¥| ultralytics | [YOLOv8](./examples/
-YOLOv8ââultralytics.ipynb) | |TextClassificationââBERT ð¥ð¥|
-transformers | [BERT](./examples/BERTââtransformers.ipynb) |
-|TokenClassificationââBERT | transformers | [BERT_NER](./examples/
-BERT_NERââtransformers.ipynb) | |FinetuneLLMââChatGLM2 ð¥ð¥ð¥|
-transformers | [ChatGLM2](./examples/ChatGLM2ââtransformers.ipynb) |
-|FinetuneLLMââChatGLM2_LoRA ð¥ð¥ð¥| transformers,peft |
-[ChatGLM2_LoRA](./examples/ChatGLM2_LoRAââtransformers.ipynb) |
-|FinetuneLLMââChatGLM2_AdaLoRA ð¥ð¥ð¥| transformers,peft |
-[ChatGLM2_AdaLoRA](./examples/ChatGLM2_AdaLoRAââtransformers.ipynb) |
+YOLOv8ââultralytics.ipynb) |
 |ImageClassificationââSwinTransformer|timm| [Swin](./examples/
-SwinTransformerââtimm.ipynb)| **If you want to understand or modify some
-details of this project, feel free to read and change the source code!!!** Any
-other questions, you can contact the author form the wechat official account
-below: **ç®æ³ç¾é£å±** ![](https://tva1.sinaimg.cn/large/
-e6c9d24egy1h41m2zugguj20k00b9q46.jpg)
+SwinTransformerââtimm.ipynb)| |||| |**NLP**|||
+|TextClassificationââBERT ð¥ð¥| transformers | [BERT](./examples/
+BERTââtransformers.ipynb) | |TokenClassificationââBERT | transformers |
+[BERT_NER](./examples/BERT_NERââtransformers.ipynb) |
+|FinetuneLLMââChatGLM2 ð¥ð¥ð¥| transformers | [ChatGLM2](./examples/
+ChatGLM2ââtransformers.ipynb) | |FinetuneLLMââChatGLM2_LoRA
+ð¥ð¥ð¥| transformers,peft | [ChatGLM2_LoRA](./examples/
+ChatGLM2_LoRAââtransformers.ipynb) | |FinetuneLLMââChatGLM2_AdaLoRA
+ð¥ð¥ð¥| transformers,peft | [ChatGLM2_AdaLoRA](./examples/
+ChatGLM2_AdaLoRAââtransformers.ipynb) | |FinetuneLLMââChatGLM2_QLoRA
+ð¥ð¥ð¥| transformers | [ChatGLM2_QLoRA_Kaggle](./examples/
+ChatGLM2_QLoRA_Kaggleââtransformers.ipynb) |
+|FinetuneLLMââBaiChuan13B_QLoRA ð¥ð¥ð¥| transformers |
+[BaiChuan13B_QLoRA](./examples/BaiChuan13B_QLoRAââtransformers.ipynb) |
+|FinetuneLLMââBaiChuan13B_NER ð¥ð¥ð¥| transformers |
+[BaiChuan13B_NER](./examples/BaiChuan13B_NERââtransformers.ipynb) | **If
+you want to understand or modify some details of this project, feel free to
+read and change the source code!!!** Any other questions, you can contact the
+author form the wechat official account below: **ç®æ³ç¾é£å±** ![](https://
+tva1.sinaimg.cn/large/e6c9d24egy1h41m2zugguj20k00b9q46.jpg)
```

### Comparing `torchkeras-3.9.1/torchkeras.egg-info/SOURCES.txt` & `torchkeras-3.9.2/torchkeras.egg-info/SOURCES.txt`

 * *Files identical despite different names*

