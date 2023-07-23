# Comparing `tmp/tokenmonster-1.1.8.tar.gz` & `tmp/tokenmonster-1.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tokenmonster-1.1.8.tar", last modified: Wed Jul 19 04:59:31 2023, max compression
+gzip compressed data, was "tokenmonster-1.1.9.tar", last modified: Sun Jul 23 15:02:25 2023, max compression
```

## Comparing `tokenmonster-1.1.8.tar` & `tokenmonster-1.1.9.tar`

### file list

```diff
@@ -1,11 +1,11 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-19 04:59:31.415657 tokenmonster-1.1.8/
--rw-r--r--   0 root         (0) root         (0)    16030 2023-07-19 04:59:31.415657 tokenmonster-1.1.8/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)    16273 2023-07-19 04:50:36.000000 tokenmonster-1.1.8/README.md
--rw-r--r--   0 root         (0) root         (0)       38 2023-07-19 04:59:31.415657 tokenmonster-1.1.8/setup.cfg
--rw-r--r--   0 root         (0) root         (0)      550 2023-07-19 04:47:07.000000 tokenmonster-1.1.8/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-19 04:59:31.415657 tokenmonster-1.1.8/tokenmonster.egg-info/
--rw-r--r--   0 root         (0) root         (0)    16030 2023-07-19 04:59:31.000000 tokenmonster-1.1.8/tokenmonster.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      178 2023-07-19 04:59:31.000000 tokenmonster-1.1.8/tokenmonster.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-07-19 04:59:31.000000 tokenmonster-1.1.8/tokenmonster.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       13 2023-07-19 04:59:31.000000 tokenmonster-1.1.8/tokenmonster.egg-info/top_level.txt
--rw-r--r--   0 root         (0) root         (0)    48562 2023-07-19 04:51:52.000000 tokenmonster-1.1.8/tokenmonster.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:02:25.630623 tokenmonster-1.1.9/
+-rw-r--r--   0 root         (0) root         (0)    16561 2023-07-23 15:02:25.630623 tokenmonster-1.1.9/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)    16823 2023-07-23 14:59:33.000000 tokenmonster-1.1.9/README.md
+-rw-r--r--   0 root         (0) root         (0)       38 2023-07-23 15:02:25.630623 tokenmonster-1.1.9/setup.cfg
+-rw-r--r--   0 root         (0) root         (0)      550 2023-07-23 15:00:45.000000 tokenmonster-1.1.9/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:02:25.630623 tokenmonster-1.1.9/tokenmonster.egg-info/
+-rw-r--r--   0 root         (0) root         (0)    16561 2023-07-23 15:02:25.000000 tokenmonster-1.1.9/tokenmonster.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      178 2023-07-23 15:02:25.000000 tokenmonster-1.1.9/tokenmonster.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-07-23 15:02:25.000000 tokenmonster-1.1.9/tokenmonster.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       13 2023-07-23 15:02:25.000000 tokenmonster-1.1.9/tokenmonster.egg-info/top_level.txt
+-rw-r--r--   0 root         (0) root         (0)    51547 2023-07-23 14:58:46.000000 tokenmonster-1.1.9/tokenmonster.py
```

### Comparing `tokenmonster-1.1.8/PKG-INFO` & `tokenmonster-1.1.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 Metadata-Version: 2.1
 Name: tokenmonster
-Version: 1.1.8
+Version: 1.1.9
 Summary: Tokenize and decode text with TokenMonster vocabularies.
 Home-page: https://github.com/alasdairforsythe/tokenmonster
 Author: Alasdair Forsythe
 Author-email: 77910352+alasdairforsythe@users.noreply.github.com
 License: MIT
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # TokenMonster
 
 1. [Usage](#usage)
 2. Loading & Exporting
     - [tokenmonster.load(path)](#tokenmonsterloadpath)
+    - [tokenmonster.load_multiprocess_safe(path)](#tokenmonsterload_multiprocess_safepath)
     - [tokenmonster.new(yaml)](#tokenmonsternewyaml)
     - [vocab.save(fname)](#vocabsavefname)
     - [vocab.export_yaml(order_by_score=False)](#vocabexport_yamlorder_by_scorefalse)
 3. Tokenization & Detokenization
     - [vocab.tokenize(text)](#vocabtokenizetext)
     - [vocab.tokenize_count(text)](#vocabtokenize_counttext)
     - [vocab.decode(tokens)](#vocabdecodetokens)
@@ -75,14 +76,33 @@
 
 #### Usage
 
 ```python
 vocab = tokenmonster.load("english-32000-balanced-v1")
 ```
 
+### tokenmonster.load_multiprocess_safe(path)
+
+Loads a TokenMonster vocabulary from file, URL or by name.
+It's safe for multiprocessing, but vocabulary modification is disabled and tokenization is slightly slower.
+
+#### Parameters
+
+- `path` (string): A filepath, URL or pre-built vocabulary name.
+
+#### Returns
+
+- `Vocab`: An instance of tokenmonster.Vocab.
+
+#### Usage
+
+```python
+vocab = tokenmonster.load("english-32000-balanced-v1")
+```
+
 ### tokenmonster.new(yaml)
 
 Creates a new vocabulary from a YAML string.
 A sample YAML file can be found here: https://github.com/alasdairforsythe/tokenmonster/yaml_guide
 You should save it in the vocab format with `vocab.save()` for future use.
 
 #### Parameters
@@ -596,8 +616,7 @@
 - `binary_string` (bytes): The binary string to deserialize.
 
 #### Returns
 
 - `np.array`: The deserialized tokens.
 .
 
-
```

### Comparing `tokenmonster-1.1.8/README.md` & `tokenmonster-1.1.9/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 # TokenMonster
 
 1. [Usage](#usage)
 2. Loading & Exporting
     - [tokenmonster.load(path)](#tokenmonsterloadpath)
+    - [tokenmonster.load_multiprocess_safe(path)](#tokenmonsterload_multiprocess_safepath)
     - [tokenmonster.new(yaml)](#tokenmonsternewyaml)
     - [vocab.save(fname)](#vocabsavefname)
     - [vocab.export_yaml(order_by_score=False)](#vocabexport_yamlorder_by_scorefalse)
 3. Tokenization & Detokenization
     - [vocab.tokenize(text)](#vocabtokenizetext)
     - [vocab.tokenize_count(text)](#vocabtokenize_counttext)
     - [vocab.decode(tokens)](#vocabdecodetokens)
@@ -64,14 +65,33 @@
 
 #### Usage
 
 ```python
 vocab = tokenmonster.load("english-32000-balanced-v1")
 ```
 
+### tokenmonster.load_multiprocess_safe(path)
+
+Loads a TokenMonster vocabulary from file, URL or by name.
+It's safe for multiprocessing, but vocabulary modification is disabled and tokenization is slightly slower.
+
+#### Parameters
+
+- `path` (string): A filepath, URL or pre-built vocabulary name.
+
+#### Returns
+
+- `Vocab`: An instance of tokenmonster.Vocab.
+
+#### Usage
+
+```python
+vocab = tokenmonster.load("english-32000-balanced-v1")
+```
+
 ### tokenmonster.new(yaml)
 
 Creates a new vocabulary from a YAML string.
 A sample YAML file can be found here: https://github.com/alasdairforsythe/tokenmonster/yaml_guide
 You should save it in the vocab format with `vocab.save()` for future use.
 
 #### Parameters
@@ -583,8 +603,8 @@
 #### Parameters
 
 - `binary_string` (bytes): The binary string to deserialize.
 
 #### Returns
 
 - `np.array`: The deserialized tokens.
-.
+.
```

### Comparing `tokenmonster-1.1.8/setup.py` & `tokenmonster-1.1.9/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup
 
 with open('README.md', 'r') as f:
     long_description = f.read()
 
 setup(
     name='tokenmonster',
-    version='1.1.8',
+    version='1.1.9',
     py_modules=['tokenmonster'],
     author='Alasdair Forsythe',
     author_email='77910352+alasdairforsythe@users.noreply.github.com',
     description='Tokenize and decode text with TokenMonster vocabularies.',
     url='https://github.com/alasdairforsythe/tokenmonster',
     license='MIT',
     long_description=long_description,
```

### Comparing `tokenmonster-1.1.8/tokenmonster.egg-info/PKG-INFO` & `tokenmonster-1.1.9/tokenmonster.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 Metadata-Version: 2.1
 Name: tokenmonster
-Version: 1.1.8
+Version: 1.1.9
 Summary: Tokenize and decode text with TokenMonster vocabularies.
 Home-page: https://github.com/alasdairforsythe/tokenmonster
 Author: Alasdair Forsythe
 Author-email: 77910352+alasdairforsythe@users.noreply.github.com
 License: MIT
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
 
 # TokenMonster
 
 1. [Usage](#usage)
 2. Loading & Exporting
     - [tokenmonster.load(path)](#tokenmonsterloadpath)
+    - [tokenmonster.load_multiprocess_safe(path)](#tokenmonsterload_multiprocess_safepath)
     - [tokenmonster.new(yaml)](#tokenmonsternewyaml)
     - [vocab.save(fname)](#vocabsavefname)
     - [vocab.export_yaml(order_by_score=False)](#vocabexport_yamlorder_by_scorefalse)
 3. Tokenization & Detokenization
     - [vocab.tokenize(text)](#vocabtokenizetext)
     - [vocab.tokenize_count(text)](#vocabtokenize_counttext)
     - [vocab.decode(tokens)](#vocabdecodetokens)
@@ -75,14 +76,33 @@
 
 #### Usage
 
 ```python
 vocab = tokenmonster.load("english-32000-balanced-v1")
 ```
 
+### tokenmonster.load_multiprocess_safe(path)
+
+Loads a TokenMonster vocabulary from file, URL or by name.
+It's safe for multiprocessing, but vocabulary modification is disabled and tokenization is slightly slower.
+
+#### Parameters
+
+- `path` (string): A filepath, URL or pre-built vocabulary name.
+
+#### Returns
+
+- `Vocab`: An instance of tokenmonster.Vocab.
+
+#### Usage
+
+```python
+vocab = tokenmonster.load("english-32000-balanced-v1")
+```
+
 ### tokenmonster.new(yaml)
 
 Creates a new vocabulary from a YAML string.
 A sample YAML file can be found here: https://github.com/alasdairforsythe/tokenmonster/yaml_guide
 You should save it in the vocab format with `vocab.save()` for future use.
 
 #### Parameters
@@ -596,8 +616,7 @@
 - `binary_string` (bytes): The binary string to deserialize.
 
 #### Returns
 
 - `np.array`: The deserialized tokens.
 .
 
-
```

### Comparing `tokenmonster-1.1.8/tokenmonster.py` & `tokenmonster-1.1.9/tokenmonster.py`

 * *Files 4% similar despite different names*

```diff
@@ -35,14 +35,30 @@
     Usage:
         vocab = tokenmonster.load("english-32000-balanced-v1")
         tokens = vocab.tokenize(str)
         decoded_string = vocab.decode(tokens)
     """
     return Vocab(path)
 
+def load_multiprocess_safe(path):
+    """
+    Loads a TokenMonster vocabulary from file, URL or by name.
+    It's safe for multiprocessing, but vocabulary modification is disabled and tokenization is slightly slower.
+
+    Parameters:
+        path (string): A filepath, URL or pre-built vocabulary name.
+
+    Returns:
+        Vocab: An instance of tokenmonster.Vocab.
+
+    Usage:
+        vocab = tokenmonster.load_multiprocess_safe("english-32000-balanced-v1")
+    """
+    return Vocab(path, True)
+
 def new(yaml):
     """
     Creates a new vocabulary from a YAML string.
     A sample YAML file can be found here: https://github.com/alasdairforsythe/tokenmonster/yaml_guide
     You should save it in the vocab format with `vocab.save()` for future use.
 
     Parameters:
@@ -58,16 +74,18 @@
     if not isinstance(yaml, bytes):
         if isinstance(yaml, str):
             yaml = yaml.encode('utf-8')
         else:
             raise ValueError("TokenMonster: Input to `tokenmonster.New()` must be a YAML string.")
     Vocab._set_local_directory()
     job_type = 18
-    response = Vocab._communicate(job_type, 0, len(yaml), yaml)
     vocab = Vocab.__new__(Vocab)
+    vocab._multiprocess = False
+    vocab.fname = None
+    response = vocab._communicate(job_type, 0, len(yaml), yaml)
     vocab._capcode = response[0]
     vocab._charset = response[1]
     vocab._normalization = response[2]
     vocab._mode = response[3]
     vocab.vocab_size = _read_uint32(response[4:8])
     vocab.id = _read_uint32(response[8:12])
     unk = _read_uint32(response[12:16])
@@ -75,15 +93,14 @@
         vocab.unk = None
     else:
          vocab.unk = unk
     if vocab.vocab_size > 65536:
         vocab.encoding_length = 4
     else:
         vocab.encoding_length = 2
-    vocab.fname = None
     vocab.dictionary = None
     vocab._token_to_id = None
     vocab._modified_id = 0
     vocab._decoders = []
     return vocab
 
 class Vocab:
@@ -107,15 +124,15 @@
             decoder = vocab.decoder()
             decoded_string = decoder.decode(tokens)
             decoded_string += decoder.decode(more_tokens)
         """
 
         def __init__(self, parent):
             self.parent = parent
-            self.id = Vocab._communicate(5, parent.id, 0)
+            self.id = parent._communicate(5, parent.id, 0)
             self._modified_id = parent._modified_id
             parent._decoders.append(self.id)
         
         def decode(self, tokens):
             """
             A decoder object used for decoding token streams.
 
@@ -134,77 +151,78 @@
             Usage:
                 vocab = tokenmonster.Load("english-32000-balanced-v1")
                 decoder = vocab.Decoder()
                 decoded_string = decoder.decode(tokens)
                 decoded_string += decoder.decode(more_tokens)
             """
             if self.parent._modified_id != self._modified_id:
-                raise RuntimeError("Access denied to expired tokenmonster.Decoder instance.")
+                raise RuntimeError("Access denied to tokenmonster.DecoderInstance. The decoder instance has either expired, or it was not created by this multiprocessing thread.")
             if is_iterable(tokens):
                 if len(tokens) == 0:
                     return ''
                 if is_iterable(tokens[0]):
                     raise ValueError("TokenMonster: You can't batch decode on a decoder object, use the vocab decoder for that.")
             else:
                 if isinstance(tokens, int):
                     tokens = [tokens]
                 elif isinstance(tokens, (np.uint16, np.uint32)):
                     tokens = np.array([tokens])
                 else:
-                    raise ValueError("TokenMonster: Decoder decode accepts int or list of ints.")
+                    raise ValueError("TokenMonster: Decoder decode accepts int, list of ints or np.array.")
             payload = self.parent.serialize_tokens(tokens)
             job_type = self.parent.encoding_length + 5
-            response = Vocab._communicate(job_type, self.id, len(payload), payload)
+            response = self.parent._communicate(job_type, self.id, len(payload), payload)
             return self.parent._bytes_to_string(response)
         
         def _unload(self):
             if hasattr(self, 'id'):
                 if self.id is not None:
                     if self.parent._modified_id != -1:
-                        Vocab._communicate(6, self.id, 0)
+                        self.parent._communicate(6, self.id, 0)
         
         def __del__(self):
             try:
                 if not sys.is_finalizing():
                     self._unload()
             except AttributeError:
                 pass
 
-    def __init__(self, path):
+    def __init__(self, path, multiprocess_safe = False):
         Vocab._set_local_directory()
-        if not any(char in path for char in "./\\"):
+        if not any(char in path for char in "./\\"): # if its not a filename or URL
             if Vocab._file_exists(path + ".vocab"):
                 path = os.path.join(Vocab._dir, path + ".vocab")
             else:
                 clean = path.replace("+", "")
                 if Vocab._file_exists(clean + ".vocab"):
                     path = os.path.join(Vocab._dir, clean + ".vocab")
                 else:
                     if _is_prebuilt(clean):
                         path = clean + ".vocab"
                         Vocab._download(_TOKENMONSTER_URL + "vocabs/" + path, path)
                         if Vocab._file_exists(path):
                             path = os.path.join(Vocab._dir, path)
                         else:
                             raise RuntimeError("TokenMonster: Unable to download the prebuilt vocabulary, please check availability at huggingface.co/alasdairforsythe/tokenmonster")
-        elif path.startswith("http://") or path.startswith("https://"):
+        elif path.startswith("http://") or path.startswith("https://"): # it's a URL
             fname = os.path.basename(path)
             if Vocab._file_exists(fname):
                 path = os.path.join(Vocab._dir, fname)
             else:
                 Vocab._download(path, fname)
                 if Vocab._file_exists(fname):
                     path = os.path.join(Vocab._dir, fname)
                 else:
                     raise FileNotFoundError("TokenMonster: Unable to download " + path + " to " + Vocab._dir)
-        elif os.path.isfile(path):
-            pass
-        elif Vocab._file_exists(path):
+        elif os.path.isfile(path): # it's a local filepath relative to the working directory
+            if not os.path.isabs(path):
+                path = os.path.join(os.getcwd(), path)
+        elif Vocab._file_exists(path): # it's a local filepath relative to the _tokenmonster dir
             path = os.path.join(Vocab._dir, path)
-        elif Vocab._file_exists(path + ".vocab"):
+        elif Vocab._file_exists(path + ".vocab"): # it's a local filepath relative to the _tokenmonster dir without file extension
             path = os.path.join(Vocab._dir, path + ".vocab")
         else:
             raise FileNotFoundError("TokenMonster: Unable to locate " + path)
         # Now read the vocabulary header
         with open(path, 'rb') as file:
             vocab_header = file.read(14)
         self._capcode = vocab_header[0]
@@ -217,31 +235,32 @@
         if unk != 16777215:
             self.Unk = unk
         if self.vocab_size > 65536:
             self.encoding_length = 4
         else:
             self.encoding_length = 2
         self.fname = path
-        path_encoded = path.encode("utf-8")
-        if len(path_encoded) > 255:
-            raise RuntimeError("TokenMonster: Vocabulary filepath is too long, it must be less than 256 characters")
-        payload = _write_uint8(len(path_encoded)) + path_encoded
-        self.id = Vocab._communicate(10, 0, len(payload), payload)
         self.dictionary = None
         self._token_to_id = None
         self._modified_id = 0
         self._decoders = []
+        self._multiprocess = multiprocess_safe
+        path_encoded = path.encode("utf-8")
+        if len(path_encoded) > 255:
+            raise RuntimeError("TokenMonster: Vocabulary filepath is too long, the absolute path must be less than 256 characters")
+        payload = _write_uint8(len(path_encoded)) + path_encoded
+        self.id = self._communicate(10, 0, len(payload), payload)
 
     def _unload(self):
         if hasattr(self, 'id'):
             if self.id is not None:
                 if self._modified_id != -1:
                     for _, decoder_id in enumerate(self._decoders):
-                        Vocab._communicate(6, decoder_id, 0)
-                    Vocab._communicate(11, self.id, 0)
+                        self._communicate(6, decoder_id, 0)
+                    self._communicate(11, self.id, 0)
 
     def __del__(self):
         try:
             if not sys.is_finalizing():
                 self._unload()
         except AttributeError:
             pass
@@ -366,15 +385,15 @@
                     payload.append(data)
                     length += len(item) + 8
                 else:
                     raise ValueError("TokenMonster: Input to decode must be an int, list of ints, list of lists, or numpy array.")
         # Send
         job_type = self.encoding_length
         payload[0] = _write_uint32(batch_size)
-        response = Vocab._communicate(job_type, self.id, length, payload)
+        response = self._communicate(job_type, self.id, length, payload)
         batches_reply = _read_uint32(response[0:4])
         if batches_reply != batch_size:
             raise RuntimeError("TokenMonster: batch size from response differs from request")
         decoded = [None] * batches_reply
         offset = 4
         for i in range(batch_size):
             batch_length = _read_uint64(response[offset:offset+8])
@@ -440,15 +459,15 @@
                 else:
                     raise ValueError("TokenMonster: Input to tokenize must be a string or a list of strings.")
         else:
             raise ValueError("TokenMonster: Input to tokenize must be a string or a list of strings.")
         # Send
         job_type = 1
         payload[0] = _write_uint32(batch_size)
-        response = Vocab._communicate(job_type, self.id, length, payload)
+        response = self._communicate(job_type, self.id, length, payload)
         batches_reply = _read_uint32(response[0:4])
         if batches_reply != batch_size:
             raise RuntimeError("TokenMonster: batch size of response differs from request")
         offset = 4
         if single:
             batch_length = _read_uint64(response[offset:offset+8])
             offset += 8
@@ -514,15 +533,15 @@
                 else:
                     raise ValueError("TokenMonster: Input to tokenize must be a string or a list of strings.")
         else:
             raise ValueError("TokenMonster: Input to tokenize must be a string or a list of strings.")
         # Send
         job_type = 20
         payload[0] = _write_uint32(batch_size)
-        response = Vocab._communicate(job_type, self.id, length, payload)
+        response = self._communicate(job_type, self.id, length, payload)
         batches_reply = _read_uint32(response[0:4])
         if batches_reply != batch_size:
             raise RuntimeError("TokenMonster: batch size of response differs from request")
         offset = 4
         if single:
             return _read_uint64(response[offset:offset+8])
         tokens = [0] * batch_size
@@ -555,15 +574,15 @@
             tokens = vocab.get_dictionary()
         """
         if self.dictionary is not None:
             return self.dictionary
         if self._modified_id == -1:
             raise RuntimeError("TokenMonster: Access denied to expired Vocab instance.")
         job_type = 15
-        response = Vocab._communicate(job_type, self.id, 0)
+        response = self._communicate(job_type, self.id, 0)
         size = _read_uint32(response[0:4])
         self.vocab_size = size # it should be already the same
         offset = 4
         self.dictionary = {}
         self._token_to_id = {}
         self.unk = None
         types = ["regular", "single", "special", "unk"]
@@ -681,14 +700,16 @@
         Usage:
             # adds the special token <eos>
             vocab.modify("<eos>")
             # adds the special token <eos> and keep the vocabulary at the current size
             vocab.modify("<eos>", None, None, len(vocab))
         """
         # Parse and format the inputs
+        if self._multiprocess:
+            raise RuntimeError("TokenMonster: Vocabs loaded with load_multiprocess_safe cannot be modified. Please modify it first, save it, then load it with load_multiprocess_safe.")
         if self._modified_id == -1:
             raise RuntimeError("TokenMonster: Access denied to expired Vocab instance.")
         add_special_tokens = self._format_list(add_special_tokens)
         add_regular_tokens = self._format_list(add_regular_tokens)
         delete_tokens = self._format_list(delete_tokens)
         if resize is None:
             resize = 0
@@ -706,15 +727,15 @@
         for _, item in enumerate(delete_tokens):
             payload += _write_uint8(len(item)) + item
         payload += _write_uint32(len(add_special_tokens))
         for _, item in enumerate(add_special_tokens):
             payload += _write_uint8(len(item)) + item
         payload += _write_uint32(resize)
         job_type = 14
-        self.vocab_size = Vocab._communicate(job_type, self.id, len(payload), payload)
+        self.vocab_size = self._communicate(job_type, self.id, len(payload), payload)
         self._modified()
         return self.vocab_size
     
     def modify_from_yaml(self, yaml):
         """
         Modifies the vocabulary using a YAML file.
         A sample YAML file can be found here: https://github.com/alasdairforsythe/tokenmonster/yaml_guide
@@ -728,18 +749,20 @@
         Usage:
             # Example deletes 2 tokens, one with ID 127, and another token ' test'
             vocab.modify_from_yaml("delete:\n  - id: 127\n  - token ' test'")
 
         Returns:
             int: The new size of the vocabulary.
         """
+        if self._multiprocess:
+            raise RuntimeError("TokenMonster: Vocabs loaded with load_multiprocess_safe cannot be modified. Please modify it first, save it, then load it with load_multiprocess_safe.")
         if self._modified_id == -1:
             raise RuntimeError("TokenMonster: Access denied to expired Vocab instance.")
         job_type = 17
-        self.vocab_size = Vocab._communicate(job_type, self.id, len(yaml), yaml)
+        self.vocab_size = self._communicate(job_type, self.id, len(yaml), yaml)
         self._modified()
         return self.vocab_size
 
     def add_token(self, token):
         """
         Add one or more regular tokens.
 
@@ -761,14 +784,16 @@
     def delete_token_by_id(self, id):
         """
         Delete one or more regular or special token by specifying the token ID.
 
         Returns:
             int: The new size of the vocabulary.
         """
+        if self._multiprocess:
+            raise RuntimeError("TokenMonster: Vocabs loaded with load_multiprocess_safe cannot be modified. You can load it normally, modify it, save it, then load the modified version with load_multiprocess_safe.")
         if self._modified_id == -1:
             raise RuntimeError("TokenMonster: Access denied to expired Vocab instance.")
         if isinstance(id, int):
             id = [id]
         elif isinstance(id, (np.uint16, np.uint32)):
             id = np.array([id])
         else:
@@ -776,15 +801,15 @@
                 raise ValueError("TokenMonster: Input to delete_token_by_id must be int or list of ints.")
             if len(id) == 0:
                 return self.vocab_size
             if not is_int(id[0]):
                 raise ValueError("TokenMonster: Input to delete_token_by_id must be int or list of ints.")
         payload = _write_uint32(len(id)) + _pack_32bit_ints(id)
         job_type = 16
-        self.vocab_size = Vocab._communicate(job_type, self.id, len(payload), payload)
+        self.vocab_size = self._communicate(job_type, self.id, len(payload), payload)
         self._modified()
         return self.vocab_size
 
     def add_special_token(self, token):
         """
         Add one or more special tokens.
 
@@ -852,23 +877,27 @@
 
         Returns:
             Nothing (raises error on failure)
 
         Usage:
             vocab.save("test.vocab")
         """
+        if self._multiprocess:
+            raise RuntimeError("TokenMonster: Vocabs loaded with load_multiprocess_safe cannot be saved.")
         if self._modified_id == -1:
             raise RuntimeError("TokenMonster: Access denied to expired Vocab instance.")
         fname_encoded = fname.encode("utf-8")
         if len(fname_encoded) > 255:
             raise RuntimeError("TokenMonster: Vocabulary filepath is too long, it must be less than 256 characters")
         payload = _write_uint8(len(fname_encoded)) + fname_encoded
-        Vocab._communicate(12, 0, len(payload), payload)
+        self._communicate(12, 0, len(payload), payload)
 
     def export_yaml(self, order_by_score = False):
+        if self._multiprocess:
+            raise RuntimeError("TokenMonster: Vocabs loaded with load_multiprocess_safe cannot be exported.")
         """
         Exports the vocabulary as a YAML file, which is returned as a bytes string.
 
         Parameters:
             order_by_score (boolean): If true the tokens are order by score instead of alphabetically.
 
         Returns:
@@ -879,15 +908,15 @@
             with open(file_path, 'wb') as file:
                 file.write(yaml)
         """
         if self._modified_id == -1:
             raise RuntimeError("TokenMonster: Access denied to expired Vocab instance.")
         payload = _write_uint8(int(order_by_score))
         job_type = 19
-        return Vocab._communicate(job_type, self.id, 1, payload)
+        return self._communicate(job_type, self.id, 1, payload)
 
     def deserialize_tokens(self, binary_string):
         """
         Deserializes a binary string into a numpy array of tokens IDs.
         The encoding_length needs to be recorded separetely.
         """
         if self.encoding_length == 2:
@@ -966,15 +995,15 @@
         self.unk = False
         if self.vocab_size > 65536:
             self.encoding_length = 4
         else:
             self.encoding_length = 2
         # Unload all the decoder objects
         for _, decoder_id in enumerate(self._decoders):
-            Vocab._communicate(6, decoder_id, 0)
+            self._communicate(6, decoder_id, 0)
         self._decoders = []
 
     @classmethod
     def _set_local_directory(cls, dir=None):
         if dir is None:
             if cls._dir is not None:
                 return
@@ -1001,25 +1030,36 @@
     def _download(cls, url, fname):
         urllib.request.urlretrieve(url, os.path.join(cls._dir, fname))
 
     @classmethod
     def _file_exists(cls, fname):
         return os.path.exists(os.path.join(cls._dir, fname))
     
-    @classmethod
-    def _communicate(cls, job_type, id, data_length, data = None):
-        cls._connect()
-        cls._process.stdin.write(struct.pack('<BIQ', job_type, id, data_length)[0:12])
+    def _communicate(self, job_type, id, data_length, data = None):
+        if self._multiprocess:
+            if os.getpid() != Vocab._pid: # this is a folked child process
+                Vocab._process = None # don't use the parent's subprocess
+                Vocab._connect() # make a new connection to tokenmonsterserver
+                self._modified_id = Vocab._pid # invalidate decoder instances from parent
+                # Reload the vocabulary from file
+                path_encoded = self.fname.encode("utf-8")
+                payload = _write_uint8(len(path_encoded)) + path_encoded
+                self.id = self._communicate(10, 0, len(payload), payload)
+            else:
+                Vocab._connect()
+        else:
+            Vocab._connect()
+        Vocab._process.stdin.write(struct.pack('<BIQ', job_type, id, data_length)[0:12])
         if data is not None:
             if isinstance(data, bytes):
-                cls._process.stdin.write(data)
+                Vocab._process.stdin.write(data)
             else:
                 for item in data:
-                    cls._process.stdin.write(item)
-        cls._process.stdin.flush()
+                    Vocab._process.stdin.write(item)
+        Vocab._process.stdin.flush()
         response = Vocab._process.stdout.read(9)
         if len(response) == 0: # this happens when the app is shutting down
             return None
         status = response[0]
         if status == 0: # HEADER_IS_LENGTH
             length = _read_uint64(response[1:9])
             return Vocab._process.stdout.read(length)
@@ -1044,17 +1084,18 @@
             raise ValueError("TokenMonster: YAML is invalid")
         else:
             raise RuntimeError("tokenmonsterserver: Data corruption. TokenMonster does not currently supported multithreading, use batches instead.")
 
     @classmethod
     def _start_process(cls):
         exe = os.path.join(cls._dir, cls._bin)
-        pid = str(os.getpid())
+        pid = os.getpid()
+        cls._pid = pid
         try:
-            cls._process = subprocess.Popen([exe, pid], stdin=subprocess.PIPE, stdout=subprocess.PIPE, cwd=cls._dir)
+            cls._process = subprocess.Popen([exe, str(pid)], stdin=subprocess.PIPE, stdout=subprocess.PIPE, cwd=cls._dir)
         except Exception:
             cls._process = None
             return False
         else:
             if cls._process is None:
                 return False
             return True
@@ -1078,30 +1119,37 @@
             except Exception:
                 pass
         if not cls._start_process():
             sep = '=' * 64
             raise RuntimeError("\n"+sep+"\n\n\tTo get started with TokenMonster please enable execute permissions for:\n\t"+exe+"\n\n"+sep+"\n")
 
     @classmethod
+    def _tms_get_version(cls):
+        cls._process.stdin.write(struct.pack('<BIQ', 0, 0, 0)[0:12])
+        Vocab._process.stdin.flush()
+        response = Vocab._process.stdout.read(9)
+        return _read_uint32(response[1:5])
+
+    @classmethod
     def _connect(cls):
         if cls._process is None:
             for i in range(len(cls._vocabs)):
                 cls._vocabs[i]._modified_id = -1
             cls._vocabs = []
             if cls._file_exists(cls._bin):
                 if not cls._start_process():
                     raise RuntimeError("TokenMonster: Unable to start tokenmonsterserver, please give execute permission to " + os.path.join(cls._dir, cls._bin))
             else:
                 cls._install_tokenmonsterserver()
             # Now check verison number
-            tms_version = cls._communicate(0, 0, 0)
+            tms_version = cls._tms_get_version()
             if tms_version < _TMS_VERSION_ID:
                 cls._disconnect()
                 cls._install_tokenmonsterserver()
-                tms_version = cls._communicate(0, 0, 0)
+                tms_version = cls._tms_get_version()
                 if tms_version < _TMS_VERSION_ID:
                     raise RuntimeError("TokenMonster: tokenmonsterserver version does not match Python library version")
             if tms_version > _TMS_VERSION_ID:
                 cls.disconnect()
                 raise RuntimeError("TokenMonster: Version mismatch. Please update tokenmonster with `pip install --upgrade`")
 
     #@classmethod
@@ -1114,14 +1162,15 @@
     #    cls._process.stdout.read()
 
     # class level variables
     _dir = None
     _os = None
     _bin = None
     _process = None
+    _pid = 0
     _vocabs = []
 
 
 ### Helper Functions
 
 def _is_prebuilt(name):
     if name == "gpt2" or name == "llama":
```

