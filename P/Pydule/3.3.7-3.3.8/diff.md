# Comparing `tmp/Pydule-3.3.7.tar.gz` & `tmp/Pydule-3.3.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Pydule-3.3.7.tar", last modified: Sun Jul 16 06:08:51 2023, max compression
+gzip compressed data, was "Pydule-3.3.8.tar", last modified: Sun Jul 23 15:46:00 2023, max compression
```

## Comparing `Pydule-3.3.7.tar` & `Pydule-3.3.8.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-07-16 06:08:51.439049 Pydule-3.3.7/
--rw-rw-rw-   0        0        0     2606 2023-07-16 06:08:51.409932 Pydule-3.3.7/PKG-INFO
--rw-rw-rw-   0        0        0     1842 2023-07-09 13:47:24.000000 Pydule-3.3.7/README.md
--rw-rw-rw-   0        0        0       42 2023-07-16 06:08:51.439049 Pydule-3.3.7/setup.cfg
--rw-rw-rw-   0        0        0     1522 2023-07-16 05:21:28.000000 Pydule-3.3.7/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-16 06:08:51.259017 Pydule-3.3.7/src/
-drwxrwxrwx   0        0        0        0 2023-07-16 06:08:51.409932 Pydule-3.3.7/src/Pydule.egg-info/
--rw-rw-rw-   0        0        0     2606 2023-07-16 06:08:50.000000 Pydule-3.3.7/src/Pydule.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      201 2023-07-16 06:08:50.000000 Pydule-3.3.7/src/Pydule.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-16 06:08:50.000000 Pydule-3.3.7/src/Pydule.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      267 2023-07-16 06:08:50.000000 Pydule-3.3.7/src/Pydule.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-07-16 06:08:50.000000 Pydule-3.3.7/src/Pydule.egg-info/top_level.txt
--rw-rw-rw-   0        0        0    51004 2023-07-16 06:04:29.000000 Pydule-3.3.7/src/Pydule.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:46:00.042884 Pydule-3.3.8/
+-rw-rw-rw-   0        0        0     2606 2023-07-23 15:46:00.031782 Pydule-3.3.8/PKG-INFO
+-rw-rw-rw-   0        0        0     1842 2023-07-09 13:47:24.000000 Pydule-3.3.8/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:46:00.042884 Pydule-3.3.8/setup.cfg
+-rw-rw-rw-   0        0        0     1538 2023-07-23 15:40:30.000000 Pydule-3.3.8/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:45:59.882712 Pydule-3.3.8/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 15:46:00.031782 Pydule-3.3.8/src/Pydule.egg-info/
+-rw-rw-rw-   0        0        0     2606 2023-07-23 15:45:59.000000 Pydule-3.3.8/src/Pydule.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      201 2023-07-23 15:45:59.000000 Pydule-3.3.8/src/Pydule.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:45:59.000000 Pydule-3.3.8/src/Pydule.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      275 2023-07-23 15:45:59.000000 Pydule-3.3.8/src/Pydule.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-07-23 15:45:59.000000 Pydule-3.3.8/src/Pydule.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0    51219 2023-07-23 15:31:07.000000 Pydule-3.3.8/src/Pydule.py
```

### Comparing `Pydule-3.3.7/PKG-INFO` & `Pydule-3.3.8/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Pydule
-Version: 3.3.7
+Version: 3.3.8
 Summary: Access ChatGPT,Track Location,Play Songs,Create Qrcode,Copy Text,Translate a Sentence to Other Language and more..
 Author: D.Tamil Mutharasan
 Keywords: python,PyDule,Module,Pydule,pydule,matrix,qrcode,youtube,weather,list,tuple,set,dictionary,clear,color,pick_color,open,app,search,play,mp3,song,restart,system,shutdown,date,time,text_to_speech,text,speech
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Intended Audience :: Education
 Classifier: Operating System :: Microsoft :: Windows :: Windows 10
```

### Comparing `Pydule-3.3.7/README.md` & `Pydule-3.3.8/README.md`

 * *Files identical despite different names*

### Comparing `Pydule-3.3.7/setup.py` & `Pydule-3.3.8/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 import setuptools
 
 with open('README.md','r') as fh:
 	long_description = fh.read()
 
 setup(
 	name='Pydule',
-	version='3.3.7',
+	version='3.3.8',
 	description="Access ChatGPT,Track Location,Play Songs,Create Qrcode,Copy Text,Translate a Sentence to Other Language and more..",
 	author='D.Tamil Mutharasan',
 	long_description=long_description,
 	long_description_content_type='text/markdown',
 	packages=setuptools.find_packages(),
 	keywords=['python','PyDule','Module','Pydule','pydule','matrix','qrcode','youtube','weather','list','tuple','set','dictionary','clear','color','pick_color','open','app','search','play','mp3','song','restart','system','shutdown','date','time','text_to_speech','text','speech'],
 	classifiers=[
@@ -46,11 +46,12 @@
 		'phonenumbers',
 		'SpeechRecognition',
 		'Pillow',
 		'pyinstaller',
 		'pyfiglet',
 		'pygame',
 		'speedtest-cli',
-		'keyboard'
+		'keyboard',
+		'moviepy'
 	]
 
-)
+)
```

### Comparing `Pydule-3.3.7/src/Pydule.egg-info/PKG-INFO` & `Pydule-3.3.8/src/Pydule.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Pydule
-Version: 3.3.7
+Version: 3.3.8
 Summary: Access ChatGPT,Track Location,Play Songs,Create Qrcode,Copy Text,Translate a Sentence to Other Language and more..
 Author: D.Tamil Mutharasan
 Keywords: python,PyDule,Module,Pydule,pydule,matrix,qrcode,youtube,weather,list,tuple,set,dictionary,clear,color,pick_color,open,app,search,play,mp3,song,restart,system,shutdown,date,time,text_to_speech,text,speech
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Intended Audience :: Education
 Classifier: Operating System :: Microsoft :: Windows :: Windows 10
```

### Comparing `Pydule-3.3.7/src/Pydule.py` & `Pydule-3.3.8/src/Pydule.py`

 * *Files 2% similar despite different names*

```diff
@@ -42,15 +42,38 @@
 	if isinstance(num,int):
 
 		return f'{num:,}'
 	
 	else:
 		print(f'{err} Arguments Must {facemoji} Be in int {err}') 
 
-def randict(d:dict) -> dict:
+def shufflelist(l):
+	if isinstance(l,list):
+		import random as r
+
+		ind,n=[],[]
+		
+		while True:
+			ran=r.randint(0,len(l)-1)
+			
+			if len(ind)==len(l):
+				break
+			
+			if ran not in ind:
+				ind+=[ran]
+		
+		for i in ind:
+			n+=[l[i]] 
+		
+		return n
+
+	else:
+		print(f'{err} Arguments Must {facemoji} Be in list {err}')
+
+def shuffledict(d:dict) -> dict:
 	if isinstance(d,dict):
 		import random as r
 
 		nd,l={},[]
 
 		for i in d:
 			l+=[i]
@@ -429,15 +452,15 @@
 		for i in d:
 			n=ord(i)
 			e[n]=d[i]
 
 		for i,j in zip(keys,e):
 			new[keys[i]]=e[j]
 
-		new=randict(new)
+		new=shuffledict(new)
 
 		return s,new
 	
 	else:
 		print(f'{err} Arguments Must {facemoji} Be in str {err}')	
 
 def zipfile(path:str, zip:str):
@@ -650,14 +673,37 @@
 		
 	try:
 		return keyboard.read_key()
 
 	except Exception as e:
 		print(e)	
 
+def shuffletuple(l):
+	if isinstance(l,tuple):
+		import random as r
+		
+		ind,n=[],tuple()
+		
+		while True:
+			ran=r.randint(0,len(l)-1)
+		
+			if len(ind)==len(l):
+				break
+		
+			if ran not in ind:
+		
+				ind+=[ran]
+		
+		for i in ind:
+			n+=(l[i],) 
+		
+		return n
+	else:
+		print(f'{err} Arguments Must {facemoji} Be in tuple {err}')
+
 def dowhenkeypressed(command:str,func):
 	if isinstance(command,str):
 		import keyboard
 		
 		try:
 			if keyboard.is_pressed(command):
 				func()
@@ -668,15 +714,15 @@
 	else:
 		print(f'{err} Arguments Must {facemoji} Be in str and function {err}')	
 
 def functions():
 	def lower(s):
 		return s.lower()
 
-	l=['dowhenkeypressed()','getkeypressed()','askfiles()','movefiles()','sepednumtoint()','getfilesize()','internetspeed()','Emoji()','zipfile()','inputpassword()','sepnum()','randict()','FIGlet()','pytoexe()','aboutbattery()','GPTGAME1()','percent()','msgbox()','askfolder()','askfile()','delfile()','resizeimg()','GetWebHTML()','TrackLocation()','num()','screenshot()','SpeechtoText()','ChatGPT() Use from Pydule import AI','recintaudio()','recmic()','recscreen()','mulmatrix()','EncryptStr()','DecryptStr()','swapdict()','sepstr()','wjson()','deljsonele()','upjson()','copy()','translate()','cqrcode()','summatrix()','submatrix()','intuple()','instr()','reSet()','reDict()','reTuple()','pickcolor()','search()','playmusic()','restart_system()','shutdown_system()','todaysdate()','timenow()','say()','openfile()','weathernow()','setvoice()','voicerate()']
+	l=['shuffletuple()','shufflelist()','combinevidandaud()','removeaudfromvid()','vidtoaud()','dowhenkeypressed()','getkeypressed()','askfiles()','movefiles()','sepednumtoint()','getfilesize()','internetspeed()','Emoji()','zipfile()','inputpassword()','sepnum()','shuffledict()','FIGlet()','pytoexe()','aboutbattery()','percent()','msgbox()','askfolder()','askfile()','delfile()','resizeimg()','GetWebHTML()','TrackLocation()','num()','screenshot()','SpeechtoText()','ChatGPT() Use from Pydule import AI','recintaudio()','recmic()','recscreen()','mulmatrix()','EncryptStr()','DecryptStr()','swapdict()','sepstr()','wjson()','deljsonele()','upjson()','copy()','translate()','cqrcode()','summatrix()','submatrix()','intuple()','instr()','reSet()','reDict()','reTuple()','pickcolor()','search()','playmusic()','restart_system()','shutdown_system()','todaysdate()','timenow()','say()','openfile()','weathernow()','setvoice()','voicerate()']
 	
 	l1=list(map(lower,l))
 	
 	l2,final=l1.copy(),[]
 	
 	l1.sort()
 
@@ -736,15 +782,30 @@
 
 		translated = GoogleTranslator(source='auto', target=language.lower()).translate(content)
 
 		return translated
 	
 	else:
 		print(f'{err} Arguments Must {facemoji} Be in str and str {err}')	
-	
+
+def combinevidandaud(vpath,apath,result):
+	if isinstance(vpath,str) and isinstance(apath,str) and isinstance(result,str) and result.endswith('.mp4'):
+		import moviepy.editor as mpe
+
+		clip = mpe.VideoFileClip(vpath)
+
+		audio = mpe.AudioFileClip(apath)
+		
+		finalclip = clip.set_audio(audio)
+		
+		finalclip.write_videofile(result,fps=45)
+
+	else:
+		print(f'{err} Arguments Must {facemoji} Be in str and str and str {err}')
+
 def cqrcode(data:str,filename:str):
 	if isinstance(data,str) and filename.endswith('.png') or filename.endswith('.jpg'):
 		import qrcode
 
 		img = qrcode.make(data)
 
 		img.save(filename)
@@ -800,89 +861,39 @@
 
 def pickcolor():
 	from tkinter import colorchooser
 
 	c=colorchooser.askcolor(title='Pydule Color Picker \U00002714')
 	copy('\''+str(c[-1])+'\'')
 
-def GPTGAME1():
-	import pygame
-	import random
-
-	pygame.init()
-
-	window_width = 800
-	window_height = 600
-
-	points=0
-
-	black = (0,0,0)
-	white = (255,255,255)
-
-	game_window = pygame.display.set_mode((window_width, window_height))
-	pygame.display.set_caption('Catch the Circle')
-
-	class Star:
-		def __init__(self):
-			self.x = random.randint(0, window_width)
-			self.y = random.randint(0, window_height)
-			self.size = random.randint(15, 30)
-			self.color = (random.randint(0,255),random.randint(0,255),random.randint(0,255))
+def vidtoaud(path:str,filename:str):
+	if isinstance(path,str) and isinstance(filename,str) and filename.endswith('.mp3'):
+		import moviepy.editor as mp
 
-		def draw(self):
-			pygame.draw.circle(game_window, self.color, (self.x, self.y), self.size)
+		clip = mp.VideoFileClip(path)
 
-	class Player:
-		def __init__(self):
-			self.x = window_width // 2
-			self.y = window_height // 2
-			self.size = 20
-			self.color = (255,0,0)
-			self.speed = 5
+		clip.audio.write_audiofile(filename)
 
-		def draw(self):
-			pygame.draw.circle(game_window, self.color, (self.x, self.y), self.size)
-
-		def move(self):
-			keys = pygame.key.get_pressed()
-			if keys[pygame.K_LEFT]:
-				self.x -= self.speed
-			if keys[pygame.K_RIGHT]:
-				self.x += self.speed
-			if keys[pygame.K_UP]:
-				self.y -= self.speed
-			if keys[pygame.K_DOWN]:
-				self.y += self.speed
-
-	star = Star()
-
-	player = Player()
-
-	game_running = True
-	while game_running:
-		game_window.fill(black)
-
-		star.draw()
+	else:
+		print(f'{err} Arguments Must {facemoji} Be in str and str {err}')	
 
-		player.draw()
-		player.move()
+def removeaudfromvid(path:str,filename:str):
+	if isinstance(path,str) and isinstance(filename,str) and filename.endswith('.mp4'):
+		import moviepy.editor as mp
 
-		if abs(star.x - player.x) < (star.size + player.size) // 2 and abs(star.y - player.y) < (star.size + player.size) // 2:
-			points+=1
-			star = Star()
+		videoclip = VideoFileClip(path)
+		
+		new_clip = videoclip.without_audio()
+		
+		new_clip.write_videofile(filename)
 
-		for event in pygame.event.get():
-			if event.type == pygame.QUIT:
-				print(f'You Scored {points} Points !!')
-				game_running = False
+	else:
+		print(f'{err} Arguments Must {facemoji} Be in str and str {err}')	
 
-		pygame.display.update()
 
-	pygame.quit()
-	
 def search(content:str):
 	if isinstance(content,str):
 		import pywhatkit as kt
 
 		kt.search(content)	
 		print('\nSearching \U0001F50E...\n')
 
@@ -1006,14 +1017,15 @@
 			soup = BeautifulSoup(res.text, 'html.parser')
 			time = soup.select('#wob_dts')[0].getText().strip()
 			info = soup.select('#wob_dc')[0].getText().strip()
 			weather = soup.select('#wob_tm')[0].getText().strip()
 			details=['City Name : '+place,info,weather+'°C']
 
 			return details
+			
 		city = place+" weather"
 
 		return weather(city,place)
 	
 	else:
 		print(f'{err} Arguments Must {facemoji} Be in str {err}')
```

