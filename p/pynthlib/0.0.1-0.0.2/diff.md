# Comparing `tmp/pynthlib-0.0.1.tar.gz` & `tmp/pynthlib-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pynthlib-0.0.1.tar", last modified: Sat Jul 22 21:53:02 2023, max compression
+gzip compressed data, was "pynthlib-0.0.2.tar", last modified: Sat Jul 22 22:11:10 2023, max compression
```

## Comparing `pynthlib-0.0.1.tar` & `pynthlib-0.0.2.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 21:53:02.873719 pynthlib-0.0.1/
--rw-rw-rw-   0        0        0     1076 2023-01-19 14:17:33.000000 pynthlib-0.0.1/LICENSE.txt
--rw-rw-rw-   0        0        0     3033 2023-07-22 21:53:02.873719 pynthlib-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0     2376 2023-07-22 21:50:28.000000 pynthlib-0.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 21:53:02.847582 pynthlib-0.0.1/pynthlib/
--rw-rw-rw-   0        0        0       22 2023-07-22 21:50:39.000000 pynthlib-0.0.1/pynthlib/__init__.py
--rw-rw-rw-   0        0        0     1929 2023-07-22 21:50:38.000000 pynthlib-0.0.1/pynthlib/eval.py
--rw-rw-rw-   0        0        0    29271 2023-07-22 18:28:51.000000 pynthlib-0.0.1/pynthlib/pynth.py
-drwxrwxrwx   0        0        0        0 2023-07-22 21:53:02.871216 pynthlib-0.0.1/pynthlib.egg-info/
--rw-rw-rw-   0        0        0     3033 2023-07-22 21:53:02.000000 pynthlib-0.0.1/pynthlib.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      261 2023-07-22 21:53:02.000000 pynthlib-0.0.1/pynthlib.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 21:53:02.000000 pynthlib-0.0.1/pynthlib.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       79 2023-07-22 21:53:02.000000 pynthlib-0.0.1/pynthlib.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-07-22 21:53:02.000000 pynthlib-0.0.1/pynthlib.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       86 2023-01-19 14:15:59.000000 pynthlib-0.0.1/pyproject.toml
--rw-rw-rw-   0        0        0      811 2023-07-22 21:53:02.880742 pynthlib-0.0.1/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-22 22:11:10.981271 pynthlib-0.0.2/
+-rw-rw-rw-   0        0        0     1076 2023-01-19 14:17:33.000000 pynthlib-0.0.2/LICENSE.txt
+-rw-rw-rw-   0        0        0     3309 2023-07-22 22:11:10.982778 pynthlib-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0     2652 2023-07-22 22:08:50.000000 pynthlib-0.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-22 22:11:10.956199 pynthlib-0.0.2/pynthlib/
+-rw-rw-rw-   0        0        0       20 2023-07-22 22:05:39.000000 pynthlib-0.0.2/pynthlib/__init__.py
+-rw-rw-rw-   0        0        0     1929 2023-07-22 21:50:38.000000 pynthlib-0.0.2/pynthlib/eval.py
+-rw-rw-rw-   0        0        0    29271 2023-07-22 18:28:51.000000 pynthlib-0.0.2/pynthlib/pynth.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:11:10.980265 pynthlib-0.0.2/pynthlib.egg-info/
+-rw-rw-rw-   0        0        0     3309 2023-07-22 22:11:10.000000 pynthlib-0.0.2/pynthlib.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      261 2023-07-22 22:11:10.000000 pynthlib-0.0.2/pynthlib.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-22 22:11:10.000000 pynthlib-0.0.2/pynthlib.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       79 2023-07-22 22:11:10.000000 pynthlib-0.0.2/pynthlib.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-07-22 22:11:10.000000 pynthlib-0.0.2/pynthlib.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       86 2023-01-19 14:15:59.000000 pynthlib-0.0.2/pyproject.toml
+-rw-rw-rw-   0        0        0      811 2023-07-22 22:11:10.989788 pynthlib-0.0.2/setup.cfg
```

### Comparing `pynthlib-0.0.1/LICENSE.txt` & `pynthlib-0.0.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `pynthlib-0.0.1/PKG-INFO` & `pynthlib-0.0.2/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pynthlib
-Version: 0.0.1
+Version: 0.0.2
 Summary: Intuitive sound synthesis in python.
 Home-page: https://github.com/MatejBevec/pynth
 Author: Matej Bevec
 Author-email: matejbevec98@gmail.com
 License: MIT
 Project-URL: repository, https://github.com/MatejBevec/pynth
 Classifier: Development Status :: 1 - Planning
@@ -13,15 +13,15 @@
 Classifier: Operating System :: MacOS :: MacOS X
 Classifier: Operating System :: Unix
 Classifier: Operating System :: POSIX
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
-![cover](figs/logo.png)
+![cover](https://github.com/MatejBevec/pynth/blob/main/figs/logo.png)
 
 Intuitive sound synthesis in python.
 
 
 
 ## Installation
 
@@ -52,58 +52,58 @@
 for i in range(5):
   out += 0.1 * Sin(100*i)
   
 drawgraph(out)
 showsound(out, t2=0.1)
 out.play(5*SR)
 ```
-<img src="figs/overtones.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/overtones.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463015-5cdd5f04-aa9d-4fe6-bfb3-5fa47394b6f1.mp4
 
 ### Vocal remover
 ```python
 sample, sr = librosa.load("file.wav", mono=False)
 l = Wave(sample[0, :])
 r = Wave(sample[1, :])
 SR = sr
 
 out = 0.5 * (0.5*l - 0.5*r)
 out += 0.5 * MovingAvg(0.5*l + 0.5*r, M=50)
 ```
 
-<img src="figs/vocal.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/vocal.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463075-75020d90-9f85-4ac3-9728-504b07fb9995.mp4
 
 ### Procedural wind
 ```python
 noise = WhiteNoise()
 cutmod = Unipol(.5*Sin(1/3) + .5*Sin(1/5)) * 0.1
 resmod = Unipol((.5*Sin(1) + .5*Sin(.8)) >> 0.3)
 resmod = resmod * 0.4 + 0.1
 out = Scope(Lowpass(noise, cutmod, resmod))
 ```
 
-<img src="figs/wind.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/wind.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463145-76281843-c404-4aa1-a73d-95d23d691cea.mp4
 
 ### Karplus-Strong string emulator
 ```python
 noise = Wave(np.random.rand(4000)-0.5)
 delay = Delay(None, delay=0.005)
 add = noise + delay
 delay.ins["a"] = 0.95 * MovingAvg(add, M=10)
 out = add
 
 frozen = Wave(add.eval(2*SR))
 ```
 
-<img src="figs/karplus.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/karplus.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463212-e894d9f7-7ee3-4b75-9c26-2594c877b96c.mp4
 
 ### User input, envelopes and scopes
 ```python
 import keyboard
 control = Input()
@@ -117,8 +117,8 @@
     control.set(1)
   else:
     control.set(0)
     
 out.play(30*SR, live=True, callback=loop)
 ```
 
-<img src="figs/input.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/input.png" width=900>
```

### Comparing `pynthlib-0.0.1/README.md` & `pynthlib-0.0.2/README.md`

 * *Files 19% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-![cover](figs/logo.png)
+![cover](https://github.com/MatejBevec/pynth/blob/main/figs/logo.png)
 
 Intuitive sound synthesis in python.
 
 
 
 ## Installation
 
@@ -33,58 +33,58 @@
 for i in range(5):
   out += 0.1 * Sin(100*i)
   
 drawgraph(out)
 showsound(out, t2=0.1)
 out.play(5*SR)
 ```
-<img src="figs/overtones.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/overtones.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463015-5cdd5f04-aa9d-4fe6-bfb3-5fa47394b6f1.mp4
 
 ### Vocal remover
 ```python
 sample, sr = librosa.load("file.wav", mono=False)
 l = Wave(sample[0, :])
 r = Wave(sample[1, :])
 SR = sr
 
 out = 0.5 * (0.5*l - 0.5*r)
 out += 0.5 * MovingAvg(0.5*l + 0.5*r, M=50)
 ```
 
-<img src="figs/vocal.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/vocal.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463075-75020d90-9f85-4ac3-9728-504b07fb9995.mp4
 
 ### Procedural wind
 ```python
 noise = WhiteNoise()
 cutmod = Unipol(.5*Sin(1/3) + .5*Sin(1/5)) * 0.1
 resmod = Unipol((.5*Sin(1) + .5*Sin(.8)) >> 0.3)
 resmod = resmod * 0.4 + 0.1
 out = Scope(Lowpass(noise, cutmod, resmod))
 ```
 
-<img src="figs/wind.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/wind.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463145-76281843-c404-4aa1-a73d-95d23d691cea.mp4
 
 ### Karplus-Strong string emulator
 ```python
 noise = Wave(np.random.rand(4000)-0.5)
 delay = Delay(None, delay=0.005)
 add = noise + delay
 delay.ins["a"] = 0.95 * MovingAvg(add, M=10)
 out = add
 
 frozen = Wave(add.eval(2*SR))
 ```
 
-<img src="figs/karplus.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/karplus.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463212-e894d9f7-7ee3-4b75-9c26-2594c877b96c.mp4
 
 ### User input, envelopes and scopes
 ```python
 import keyboard
 control = Input()
@@ -98,8 +98,8 @@
     control.set(1)
   else:
     control.set(0)
     
 out.play(30*SR, live=True, callback=loop)
 ```
 
-<img src="figs/input.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/input.png" width=900>
```

### Comparing `pynthlib-0.0.1/pynthlib/eval.py` & `pynthlib-0.0.2/pynthlib/eval.py`

 * *Files identical despite different names*

### Comparing `pynthlib-0.0.1/pynthlib/pynth.py` & `pynthlib-0.0.2/pynthlib/pynth.py`

 * *Files identical despite different names*

### Comparing `pynthlib-0.0.1/pynthlib.egg-info/PKG-INFO` & `pynthlib-0.0.2/pynthlib.egg-info/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pynthlib
-Version: 0.0.1
+Version: 0.0.2
 Summary: Intuitive sound synthesis in python.
 Home-page: https://github.com/MatejBevec/pynth
 Author: Matej Bevec
 Author-email: matejbevec98@gmail.com
 License: MIT
 Project-URL: repository, https://github.com/MatejBevec/pynth
 Classifier: Development Status :: 1 - Planning
@@ -13,15 +13,15 @@
 Classifier: Operating System :: MacOS :: MacOS X
 Classifier: Operating System :: Unix
 Classifier: Operating System :: POSIX
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
-![cover](figs/logo.png)
+![cover](https://github.com/MatejBevec/pynth/blob/main/figs/logo.png)
 
 Intuitive sound synthesis in python.
 
 
 
 ## Installation
 
@@ -52,58 +52,58 @@
 for i in range(5):
   out += 0.1 * Sin(100*i)
   
 drawgraph(out)
 showsound(out, t2=0.1)
 out.play(5*SR)
 ```
-<img src="figs/overtones.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/overtones.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463015-5cdd5f04-aa9d-4fe6-bfb3-5fa47394b6f1.mp4
 
 ### Vocal remover
 ```python
 sample, sr = librosa.load("file.wav", mono=False)
 l = Wave(sample[0, :])
 r = Wave(sample[1, :])
 SR = sr
 
 out = 0.5 * (0.5*l - 0.5*r)
 out += 0.5 * MovingAvg(0.5*l + 0.5*r, M=50)
 ```
 
-<img src="figs/vocal.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/vocal.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463075-75020d90-9f85-4ac3-9728-504b07fb9995.mp4
 
 ### Procedural wind
 ```python
 noise = WhiteNoise()
 cutmod = Unipol(.5*Sin(1/3) + .5*Sin(1/5)) * 0.1
 resmod = Unipol((.5*Sin(1) + .5*Sin(.8)) >> 0.3)
 resmod = resmod * 0.4 + 0.1
 out = Scope(Lowpass(noise, cutmod, resmod))
 ```
 
-<img src="figs/wind.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/wind.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463145-76281843-c404-4aa1-a73d-95d23d691cea.mp4
 
 ### Karplus-Strong string emulator
 ```python
 noise = Wave(np.random.rand(4000)-0.5)
 delay = Delay(None, delay=0.005)
 add = noise + delay
 delay.ins["a"] = 0.95 * MovingAvg(add, M=10)
 out = add
 
 frozen = Wave(add.eval(2*SR))
 ```
 
-<img src="figs/karplus.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/karplus.png" width=900>
 
 https://user-images.githubusercontent.com/40042371/213463212-e894d9f7-7ee3-4b75-9c26-2594c877b96c.mp4
 
 ### User input, envelopes and scopes
 ```python
 import keyboard
 control = Input()
@@ -117,8 +117,8 @@
     control.set(1)
   else:
     control.set(0)
     
 out.play(30*SR, live=True, callback=loop)
 ```
 
-<img src="figs/input.png" width=900>
+<img src="https://github.com/MatejBevec/pynth/blob/main/figs/input.png" width=900>
```

### Comparing `pynthlib-0.0.1/setup.cfg` & `pynthlib-0.0.2/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2070 796e 7468 6c69 620d 0a76 6572   = pynthlib..ver
-00000020: 7369 6f6e 203d 2030 2e30 2e31 0d0a 6175  sion = 0.0.1..au
+00000020: 7369 6f6e 203d 2030 2e30 2e32 0d0a 6175  sion = 0.0.2..au
 00000030: 7468 6f72 203d 204d 6174 656a 2042 6576  thor = Matej Bev
 00000040: 6563 0d0a 6175 7468 6f72 5f65 6d61 696c  ec..author_email
 00000050: 203d 206d 6174 656a 6265 7665 6339 3840   = matejbevec98@
 00000060: 676d 6169 6c2e 636f 6d0d 0a64 6573 6372  gmail.com..descr
 00000070: 6970 7469 6f6e 203d 2049 6e74 7569 7469  iption = Intuiti
 00000080: 7665 2073 6f75 6e64 2073 796e 7468 6573  ve sound synthes
 00000090: 6973 2069 6e20 7079 7468 6f6e 2e0d 0a6c  is in python...l
```

