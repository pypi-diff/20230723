# Comparing `tmp/kanonym4text-0.2.6.tar.gz` & `tmp/kanonym4text-0.2.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "kanonym4text-0.2.6.tar", last modified: Wed Jul 12 14:10:21 2023, max compression
+gzip compressed data, was "kanonym4text-0.2.7.tar", last modified: Sun Jul 23 12:22:58 2023, max compression
```

## Comparing `kanonym4text-0.2.6.tar` & `kanonym4text-0.2.7.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-12 14:10:20.999739 kanonym4text-0.2.6/
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      869 2023-07-12 14:10:20.999739 kanonym4text-0.2.6/PKG-INFO
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     4896 2023-07-09 13:23:33.000000 kanonym4text-0.2.6/README.md
-drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-12 14:10:20.999739 kanonym4text-0.2.6/kanonym4text/
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      119 2023-07-06 09:36:30.000000 kanonym4text-0.2.6/kanonym4text/__init__.py
-drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-12 14:10:20.999739 kanonym4text-0.2.6/kanonym4text/data/
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)    35592 2023-07-01 20:45:19.000000 kanonym4text-0.2.6/kanonym4text/data/5000_most_common_words_by_order.txt
-drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-12 14:10:20.999739 kanonym4text-0.2.6/kanonym4text/objects/
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)       52 2023-07-06 09:06:10.000000 kanonym4text-0.2.6/kanonym4text/objects/__init__.py
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     8241 2023-07-12 13:18:58.000000 kanonym4text-0.2.6/kanonym4text/objects/kanonym.py
-drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-12 14:10:20.999739 kanonym4text-0.2.6/kanonym4text/utils/
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)        0 2023-07-01 20:45:19.000000 kanonym4text-0.2.6/kanonym4text/utils/__init__.py
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)    13287 2023-07-06 10:50:11.000000 kanonym4text-0.2.6/kanonym4text/utils/anonym_utils.py
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     8723 2023-07-06 10:17:19.000000 kanonym4text-0.2.6/kanonym4text/utils/cluster_utils.py
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     6355 2023-07-09 14:30:42.000000 kanonym4text-0.2.6/kanonym4text/utils/llm_utils.py
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      721 2023-07-05 07:09:39.000000 kanonym4text-0.2.6/kanonym4text/utils/models.py
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)    11183 2023-07-12 13:09:40.000000 kanonym4text-0.2.6/kanonym4text/utils/nlp_utils.py
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     3152 2023-07-06 08:40:32.000000 kanonym4text-0.2.6/kanonym4text/utils/utilization_utils.py
-drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-12 14:10:20.999739 kanonym4text-0.2.6/kanonym4text.egg-info/
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      869 2023-07-12 14:10:20.000000 kanonym4text-0.2.6/kanonym4text.egg-info/PKG-INFO
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      576 2023-07-12 14:10:20.000000 kanonym4text-0.2.6/kanonym4text.egg-info/SOURCES.txt
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)        1 2023-07-12 14:10:20.000000 kanonym4text-0.2.6/kanonym4text.egg-info/dependency_links.txt
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      211 2023-07-12 14:10:20.000000 kanonym4text-0.2.6/kanonym4text.egg-info/requires.txt
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)       13 2023-07-12 14:10:20.000000 kanonym4text-0.2.6/kanonym4text.egg-info/top_level.txt
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)       38 2023-07-12 14:10:20.999739 kanonym4text-0.2.6/setup.cfg
--rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     1604 2023-07-12 14:10:04.000000 kanonym4text-0.2.6/setup.py
+drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-23 12:22:58.156183 kanonym4text-0.2.7/
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     6631 2023-07-23 12:22:58.156183 kanonym4text-0.2.7/PKG-INFO
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     4896 2023-07-09 13:23:33.000000 kanonym4text-0.2.7/README.md
+drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-23 12:22:58.148182 kanonym4text-0.2.7/kanonym4text/
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      119 2023-07-06 09:36:30.000000 kanonym4text-0.2.7/kanonym4text/__init__.py
+drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-23 12:22:58.148182 kanonym4text-0.2.7/kanonym4text/data/
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)    35592 2023-07-01 20:45:19.000000 kanonym4text-0.2.7/kanonym4text/data/5000_most_common_words_by_order.txt
+drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-23 12:22:58.148182 kanonym4text-0.2.7/kanonym4text/objects/
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)       52 2023-07-06 09:06:10.000000 kanonym4text-0.2.7/kanonym4text/objects/__init__.py
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     8241 2023-07-12 13:18:58.000000 kanonym4text-0.2.7/kanonym4text/objects/kanonym.py
+drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-23 12:22:58.156183 kanonym4text-0.2.7/kanonym4text/utils/
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)        0 2023-07-01 20:45:19.000000 kanonym4text-0.2.7/kanonym4text/utils/__init__.py
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)    13287 2023-07-06 10:50:11.000000 kanonym4text-0.2.7/kanonym4text/utils/anonym_utils.py
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     8723 2023-07-06 10:17:19.000000 kanonym4text-0.2.7/kanonym4text/utils/cluster_utils.py
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     8091 2023-07-13 06:46:18.000000 kanonym4text-0.2.7/kanonym4text/utils/llm_utils.py
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      721 2023-07-05 07:09:39.000000 kanonym4text-0.2.7/kanonym4text/utils/models.py
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)    11183 2023-07-12 13:09:40.000000 kanonym4text-0.2.7/kanonym4text/utils/nlp_utils.py
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     3152 2023-07-06 08:40:32.000000 kanonym4text-0.2.7/kanonym4text/utils/utilization_utils.py
+drwxrwxr-x   0 neumanh   (1000) neumanh   (1001)        0 2023-07-23 12:22:58.148182 kanonym4text-0.2.7/kanonym4text.egg-info/
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     6631 2023-07-23 12:22:58.000000 kanonym4text-0.2.7/kanonym4text.egg-info/PKG-INFO
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      576 2023-07-23 12:22:58.000000 kanonym4text-0.2.7/kanonym4text.egg-info/SOURCES.txt
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)        1 2023-07-23 12:22:58.000000 kanonym4text-0.2.7/kanonym4text.egg-info/dependency_links.txt
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)      211 2023-07-23 12:22:58.000000 kanonym4text-0.2.7/kanonym4text.egg-info/requires.txt
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)       13 2023-07-23 12:22:58.000000 kanonym4text-0.2.7/kanonym4text.egg-info/top_level.txt
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)       38 2023-07-23 12:22:58.156183 kanonym4text-0.2.7/setup.cfg
+-rw-rw-r--   0 neumanh   (1000) neumanh   (1001)     1753 2023-07-23 12:22:53.000000 kanonym4text-0.2.7/setup.py
```

### Comparing `kanonym4text-0.2.6/README.md` & `kanonym4text-0.2.7/README.md`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/kanonym4text/data/5000_most_common_words_by_order.txt` & `kanonym4text-0.2.7/kanonym4text/data/5000_most_common_words_by_order.txt`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/kanonym4text/objects/kanonym.py` & `kanonym4text-0.2.7/kanonym4text/objects/kanonym.py`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/kanonym4text/utils/anonym_utils.py` & `kanonym4text-0.2.7/kanonym4text/utils/anonym_utils.py`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/kanonym4text/utils/cluster_utils.py` & `kanonym4text-0.2.7/kanonym4text/utils/cluster_utils.py`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/kanonym4text/utils/llm_utils.py` & `kanonym4text-0.2.7/kanonym4text/utils/llm_utils.py`

 * *Files 27% similar despite different names*

```diff
@@ -43,15 +43,15 @@
     for doc in doc_list:
        input_text = f'{input_text}{i}: {doc}. ' 
        i += 1
     
     # print('doc_list:', doc_list)
     # preprocess the input sentences
     prompt = prompt_builder(doc_list)
-    input_ids = tokenizer.encode(prompt, return_tensors="pt")
+    input_ids = tokenizer.encode(prompt, return_tensors="pt", truncation=True)
 
     # Moving to device
     input_ids = input_ids.to(device)
     gen_model = gen_model.to(device)
 
     # generate the summary sentence
     output_ids = gen_model.generate(input_ids=input_ids, max_length=32, num_beams=4, early_stopping=True)
@@ -109,14 +109,59 @@
     """
     Generating the prompt for document generalization
     """
 
     # Removing /n from documents
     new_docs = []
     for d in docs:
+        new_docs.append(d.replace('\n',' '))
+    
+    # Adding new line and '-' between documents
+    sents = '\n-'.join(new_docs)
+    # Adding '-' before the first document
+    sents = '-' + sents + '\n'
+
+    prompt = f'''Write a general sentence that best represents each of the following sentences and is true to all of them. For example: 
+
+Sentences:
+-the alchemist: sure this is an interesting book. unfortunately the copy we received was written in spanish!
+-immensee: a beautiful story, but the translation from the original language (german) is unbelievably poor.
+Result: 
+Good book, problem with the translation.
+
+Sentences:
+-textbook: book shipped quickly and was in excellent condition as stated. easy transaction would buy again
+-mathbook: excellent condition of book. description is true to the condition of the mathbook.shipped quickly excellent seller.
+-good deal!: used library book, but still in good condition. book came quickly and was cheap. overall good deal!
+Result: 
+Good condition book, good delivery and good seller.
+
+Sentences:
+-great: wishmaster is a fantastic album, that should grace everyone's music collection. innovating and always refreshing. truly a masterpiece.
+-fantastic debut: a great debut record from a band who deserve a lot of attention. buy this record twice.
+-great music, great arrangements and performance.: very satisfied with this cd. cem duruoz is a genius.
+Result: 
+Great music, highly recommended.
+
+Sentences:
+{sents}
+Result:
+'''
+    return prompt
+
+
+
+def long_prompt_builder(docs):
+    """
+    Generating the prompt for document generalization
+    """
+
+    # Removing /n from documents
+    new_docs = []
+    for d in docs:
         new_docs.append(d.replace('\n',' '))
     
     # Adding new line and '-' between documents
     sents = '\n-'.join(new_docs)
     # Adding '-' before the first document
     sents = '-' + sents + '\n'
```

### Comparing `kanonym4text-0.2.6/kanonym4text/utils/models.py` & `kanonym4text-0.2.7/kanonym4text/utils/models.py`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/kanonym4text/utils/nlp_utils.py` & `kanonym4text-0.2.7/kanonym4text/utils/nlp_utils.py`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/kanonym4text/utils/utilization_utils.py` & `kanonym4text-0.2.7/kanonym4text/utils/utilization_utils.py`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/kanonym4text.egg-info/SOURCES.txt` & `kanonym4text-0.2.7/kanonym4text.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `kanonym4text-0.2.6/setup.py` & `kanonym4text-0.2.7/setup.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,26 +1,31 @@
 from setuptools import setup, find_packages
+from pathlib import Path
 
-VERSION = '0.2.6'
+VERSION = '0.2.7'
 DESCRIPTION = 'k-anonymity for texts'
 LONG_DESCRIPTION = 'A package that takes a dataframe with a corpus and return an anonymized corpus'
 
+# For the README file
+this_directory = Path(__file__).parent
+long_description = (this_directory / "README.md").read_text()
+
 # Setting up
 setup(
     name="kanonym4text",
     version=VERSION,
     author="Lior Trieman, Hadas Neuman",
     author_email="liortr30@gmail.com, hadas.doron@gmail.com",
     url='https://github.com/neumanh/K-anonymity-fot-texts',
 
     download_url='https://github.com/neumanh/K-anonymity-fot-texts/archive/refs/tags/0.2.6.tar.gz',
 
     description=DESCRIPTION,
     long_description_content_type="text/markdown",
-    long_description=LONG_DESCRIPTION,
+    long_description=long_description,
     packages=find_packages(),
     # package_dir={'kanonym4text': 'kanonym4text'},
     install_requires=[
         'numpy==1.23.0',
         'pandas==1.5.3',
         'matplotlib==3.7.1',
         'gensim==4.3.1',
```

