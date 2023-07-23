# Comparing `tmp/babymaycry-0.0.7.tar.gz` & `tmp/babymaycry-0.0.8.tar.gz`

## Comparing `babymaycry-0.0.7.tar` & `babymaycry-0.0.8.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 babymaycry-0.0.7/main.py
--rw-r--r--   0        0        0       41 2020-02-02 00:00:00.000000 babymaycry-0.0.7/src/babymaycry/__init__.py
--rw-r--r--   0        0        0     1544 2020-02-02 00:00:00.000000 babymaycry-0.0.7/src/babymaycry/api.py
--rw-r--r--   0        0        0     3238 2020-02-02 00:00:00.000000 babymaycry-0.0.7/.gitignore
--rw-r--r--   0        0        0       36 2020-02-02 00:00:00.000000 babymaycry-0.0.7/README.md
--rw-r--r--   0        0        0      415 2020-02-02 00:00:00.000000 babymaycry-0.0.7/pyproject.toml
--rw-r--r--   0        0        0      335 2020-02-02 00:00:00.000000 babymaycry-0.0.7/PKG-INFO
+-rw-r--r--   0        0        0       72 2020-02-02 00:00:00.000000 babymaycry-0.0.8/main.py
+-rw-r--r--   0        0        0       41 2020-02-02 00:00:00.000000 babymaycry-0.0.8/src/babymaycry/__init__.py
+-rw-r--r--   0        0        0     1825 2020-02-02 00:00:00.000000 babymaycry-0.0.8/src/babymaycry/api.py
+-rw-r--r--   0        0        0     3238 2020-02-02 00:00:00.000000 babymaycry-0.0.8/.gitignore
+-rw-r--r--   0        0        0       36 2020-02-02 00:00:00.000000 babymaycry-0.0.8/README.md
+-rw-r--r--   0        0        0      415 2020-02-02 00:00:00.000000 babymaycry-0.0.8/pyproject.toml
+-rw-r--r--   0        0        0      335 2020-02-02 00:00:00.000000 babymaycry-0.0.8/PKG-INFO
```

### Comparing `babymaycry-0.0.7/src/babymaycry/api.py` & `babymaycry-0.0.8/src/babymaycry/api.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,40 +1,46 @@
 import pyaudio
 import telegram
 import asyncio
 import audioop
 
 
 class BabyMayCry:
-    def __init__(self, bot_token, chat_id, threadhold=1000, verbose=False):
+    def __init__(self, bot_token, chat_id, threadhold=1000, period=1, verbose=False):
         self.bot_token = bot_token
         self.chat_id = chat_id
         self.threshold = threadhold
+        self.period = period
         self.verbose = verbose
+        self.rate = 44100
+        self.chunk = 1024
         
     def run(self):
         audio = pyaudio.PyAudio()
         stream = audio.open(
             format=pyaudio.paInt16,
             channels=1,
-            rate=44100,
+            rate=self.rate,
             input=True,
-            frames_per_buffer=1024)
+            frames_per_buffer=self.chunk)
 
         print("Listening for baby cry...")
 
         while True:
             try:
-                data = stream.read(1024)
-                rms = audioop.rms(data, 2)
+                max_rms = 0
+                for _ in range(0, int(self.rate / self.chunk * self.period)):
+                    data = stream.read(self.chunk)
+                    rms = audioop.rms(data, 2)
+                    max_rms = max(max_rms, rms)
                 
                 if self.verbose:
-                    print("RMS:", rms)
+                    print("RMS:", max_rms)
 
-                if rms > self.threshold:
+                if max_rms > self.threshold:
                     print("Baby cry detected!")
                     self.send_message("Baby is crying!")
             except Exception as e:
                 stream.stop_stream()
                 stream.close()
                 audio.terminate()
                 raise e
@@ -48,8 +54,7 @@
                 print(e)
                 time.sleep(5)
                 continue
   
     def send_message(self, text):
         bot = telegram.Bot(token=self.bot_token)
         asyncio.run(bot.sendMessage(chat_id=self.chat_id, text=text))
-
```

### Comparing `babymaycry-0.0.7/.gitignore` & `babymaycry-0.0.8/.gitignore`

 * *Files identical despite different names*

