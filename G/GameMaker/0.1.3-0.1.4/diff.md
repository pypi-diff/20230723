# Comparing `tmp/GameMaker-0.1.3.tar.gz` & `tmp/GameMaker-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "GameMaker-0.1.3.tar", last modified: Sun Apr 30 09:40:37 2023, max compression
+gzip compressed data, was "GameMaker-0.1.4.tar", last modified: Sun Jul 23 04:26:24 2023, max compression
```

## Comparing `GameMaker-0.1.3.tar` & `GameMaker-0.1.4.tar`

### file list

```diff
@@ -1,27 +1,28 @@
-drwxrwxrwx   0        0        0        0 2023-04-30 09:40:37.880006 GameMaker-0.1.3/
--rw-rw-rw-   0        0        0     1091 2023-01-15 07:00:47.000000 GameMaker-0.1.3/LICENSE
--rw-rw-rw-   0        0        0      704 2023-04-30 09:40:37.878045 GameMaker-0.1.3/PKG-INFO
--rw-rw-rw-   0        0        0      170 2023-03-21 04:17:13.000000 GameMaker-0.1.3/README.md
--rw-rw-rw-   0        0        0      614 2023-04-30 09:34:48.000000 GameMaker-0.1.3/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-04-30 09:40:37.880006 GameMaker-0.1.3/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-04-30 09:40:37.836424 GameMaker-0.1.3/src/
-drwxrwxrwx   0        0        0        0 2023-04-30 09:40:37.853425 GameMaker-0.1.3/src/GameMaker/
--rw-rw-rw-   0        0        0    10203 2023-04-26 23:19:33.000000 GameMaker-0.1.3/src/GameMaker/Assets.py
--rw-rw-rw-   0        0        0     3019 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/Globals.py
--rw-rw-rw-   0        0        0     1927 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/Helper.py
--rw-rw-rw-   0        0        0     1679 2023-04-24 02:18:39.000000 GameMaker-0.1.3/src/GameMaker/Physics.py
--rw-rw-rw-   0        0        0     2046 2023-04-26 23:33:04.000000 GameMaker-0.1.3/src/GameMaker/__init__.py
-drwxrwxrwx   0        0        0        0 2023-04-30 09:40:37.877002 GameMaker-0.1.3/src/GameMaker/examples/
--rw-rw-rw-   0        0        0      612 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/examples/Demo_Button.py
--rw-rw-rw-   0        0        0      792 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/examples/Demo_Collisions.py
--rw-rw-rw-   0        0        0      908 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/examples/Demo_Gravity.py
--rw-rw-rw-   0        0        0      241 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/examples/Demo_Image.py
--rw-rw-rw-   0        0        0      356 2023-03-29 23:20:58.000000 GameMaker-0.1.3/src/GameMaker/examples/Demo_ImageList.py
--rw-rw-rw-   0        0        0      457 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/examples/Demo_ProgressBar.py
--rw-rw-rw-   0        0        0      574 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/examples/Demo_Text.py
--rw-rw-rw-   0        0        0      135 2023-03-21 23:05:56.000000 GameMaker-0.1.3/src/GameMaker/examples/Demo_Window.py
-drwxrwxrwx   0        0        0        0 2023-04-30 09:40:37.861424 GameMaker-0.1.3/src/GameMaker.egg-info/
--rw-rw-rw-   0        0        0      704 2023-04-30 09:40:37.000000 GameMaker-0.1.3/src/GameMaker.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      618 2023-04-30 09:40:37.000000 GameMaker-0.1.3/src/GameMaker.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-30 09:40:37.000000 GameMaker-0.1.3/src/GameMaker.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       10 2023-04-30 09:40:37.000000 GameMaker-0.1.3/src/GameMaker.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 04:26:24.966738 GameMaker-0.1.4/
+-rw-rw-rw-   0        0        0     1091 2023-01-15 07:00:47.000000 GameMaker-0.1.4/LICENSE
+-rw-rw-rw-   0        0        0      704 2023-07-23 04:26:24.965738 GameMaker-0.1.4/PKG-INFO
+-rw-rw-rw-   0        0        0      170 2023-03-21 04:17:13.000000 GameMaker-0.1.4/README.md
+-rw-rw-rw-   0        0        0      614 2023-07-23 04:26:06.000000 GameMaker-0.1.4/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 04:26:24.966738 GameMaker-0.1.4/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 04:26:24.914739 GameMaker-0.1.4/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 04:26:24.933742 GameMaker-0.1.4/src/GameMaker/
+-rw-rw-rw-   0        0        0    14046 2023-07-23 03:08:12.000000 GameMaker-0.1.4/src/GameMaker/Assets.py
+-rw-rw-rw-   0        0        0     3019 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/Globals.py
+-rw-rw-rw-   0        0        0     1927 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/Helper.py
+-rw-rw-rw-   0        0        0     1679 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/Physics.py
+-rw-rw-rw-   0        0        0     2153 2023-07-22 14:06:17.000000 GameMaker-0.1.4/src/GameMaker/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:26:24.963739 GameMaker-0.1.4/src/GameMaker/examples/
+-rw-rw-rw-   0        0        0      612 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_Button.py
+-rw-rw-rw-   0        0        0      792 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_Collisions.py
+-rw-rw-rw-   0        0        0      908 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_Gravity.py
+-rw-rw-rw-   0        0        0      241 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_Image.py
+-rw-rw-rw-   0        0        0      356 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_ImageList.py
+-rw-rw-rw-   0        0        0      457 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_ProgressBar.py
+-rw-rw-rw-   0        0        0      574 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_Text.py
+-rw-rw-rw-   0        0        0      234 2023-05-18 05:01:45.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_Textbox.py
+-rw-rw-rw-   0        0        0      135 2023-04-30 09:43:10.000000 GameMaker-0.1.4/src/GameMaker/examples/Demo_Window.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:26:24.944739 GameMaker-0.1.4/src/GameMaker.egg-info/
+-rw-rw-rw-   0        0        0      704 2023-07-23 04:26:24.000000 GameMaker-0.1.4/src/GameMaker.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      657 2023-07-23 04:26:24.000000 GameMaker-0.1.4/src/GameMaker.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 04:26:24.000000 GameMaker-0.1.4/src/GameMaker.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       10 2023-07-23 04:26:24.000000 GameMaker-0.1.4/src/GameMaker.egg-info/top_level.txt
```

### Comparing `GameMaker-0.1.3/LICENSE` & `GameMaker-0.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `GameMaker-0.1.3/PKG-INFO` & `GameMaker-0.1.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: GameMaker
-Version: 0.1.3
+Version: 0.1.4
 Summary: pygame Wrapper for drawing/making games
 Author-email: Dennis Yahnov <den.yakhnov@gmail.com>
 Project-URL: Homepage, https://github.com/denyahnov/GameMaker
 Project-URL: Bug Tracker, https://github.com/denyahnov/GameMaker/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `GameMaker-0.1.3/pyproject.toml` & `GameMaker-0.1.4/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "GameMaker"
-version = "0.1.3"
+version = "0.1.4"
 authors = [
   { name="Dennis Yahnov", email="den.yakhnov@gmail.com" },
 ]
 description = "pygame Wrapper for drawing/making games"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `GameMaker-0.1.3/src/GameMaker/Assets.py` & `GameMaker-0.1.4/src/GameMaker/Assets.py`

 * *Files 18% similar despite different names*

```diff
@@ -83,14 +83,16 @@
 
 	def update(self,text):
 		self.text = str(text)
 
 		self.rendered_text = self.font.render(self.text, self.antialias, self.color, self.background)
 		self.rect = self.rendered_text.get_rect()
 
+		self.w, self.h = self.rect.w, self.rect.h
+
 	def draw(self,window):
 		self.rect.center = self.x + ((self.w // 2) * self.center[1]), self. y + ((self.h // 2) * self.center[0])
 		window.blit(self.rendered_text,self.rect)
 
 class Rectangle():
 	def __init__(
 			self,
@@ -184,14 +186,16 @@
 		self.surface.set_colorkey((0, 0, 0))
 		self.surface.fill(self.foreground_color)
 		self.rect = self.surface.get_rect()
 
 		self.collision_mask = self.rect
 
 	def draw(self,window):
+		self.surface.fill(self.foreground_color)
+
 		self.rect.center = (self.x + self.w/2, self.y + self.h/2)
 
 		old_center = self.rect.center
 		new = pg.transform.rotate(self.surface, self.rotation)
 		self.rect = new.get_rect()
 		self.rect.center = old_center
 		window.blit(new, self.rect)
@@ -331,15 +335,148 @@
 			rotation: float = 0.0,
 		):
 
 		self.collision_mask = self.x, self.y, self.w, self.h = position
 		self.rotation = rotation
 		self.color = color
 
+		self.surface = pg.Surface((self.w,self.h))
+		self.surface.set_alpha(self.color[3])
+		self.surface.fill(self.color[0:3])
+		self.rect = self.surface.get_rect()
+
+	def draw(self,window):
+		self.surface.set_alpha(self.color[3])
+
+		rotated = pg.transform.rotate(self.surface, self.rotation)
+
+		self.rect.center = (self.x + self.w/2, self.y + self.h/2)
+		
+		window.blit(rotated,self.rect)
+
+class Slider():
+	def __init__(
+			self,
+			position: list[int,int,int,int],
+			button_width: int = 10,
+			vertical: bool = False,
+		):
+			
+		self.collision_mask = self.x, self.y, self.w, self.h = position
+
+		self.button_width = button_width
+
+		self.vertical = vertical
+
+		if self.vertical:
+			self.button = Button([self.x,self.y,self.w,self.button_width])
+		else:
+			self.button = Button([self.x,self.y,self.button_width,self.h])
+
+		self.background = Rectangle([self.x,self.y,self.w,self.h],foreground_color=(100,100,100))
+
+		self.value = 0
+
+	def draw(self,window):
+		if self.button.status in [PRESSED,HELD]:
+			if self.vertical:
+				self.button.y = pg.mouse.get_pos()[1] - self.button.h / 2
+
+				if self.button.y < self.y: self.button.y = self.y
+
+				if self.button.y + self.button.h > self.y + self.h: self.button.y = self.y + self.h - self.button.h
+			else:
+				self.button.x = pg.mouse.get_pos()[0] - self.button.w / 2
+
+				if self.button.x < self.x: self.button.x = self.x
+
+				if self.button.x + self.button.w > self.x + self.w: self.button.x = self.x + self.w - self.button.w
+
+		if self.vertical:
+			self.value = (self.button.y - self.y) / (self.h - self.button.h)
+		else:
+			self.value = (self.button.x - self.x) / (self.w - self.button.w)
+
+		self.value = round(self.value,2)
+
+		self.background.draw(window)
+		self.button.draw(window)
+
+class Ellipse():
+	def __init__(
+			self,
+			position: list[int,int,int,int],
+			color: tuple[int,int,int] = (200,200,200),
+			width: int = 2,
+		):
+
+		self.color = color
+
+		self.width = width
+
+		self.collision_mask = self.x,self.y,self.w,self.h = position
+
+	def draw(self,window):
+		pg.draw.ellipse(window, self.color, [self.x,self.y,self.w,self.h], self.width)
+
+class Arc():
+	def __init__(
+			self,
+			position: list[int,int,int,int],
+			start_angle: int,
+			stop_angle: int,
+			color: tuple[int,int,int] = (200,200,200),
+			width: int = 2,
+		):
+
+		self.color = color
+
+		self.start_angle = start_angle
+		self.stop_angle = stop_angle
+
+		self.width = width
+
+		self.collision_mask = self.x,self.y,self.w,self.h = position
+
 	def draw(self,window):
-		surface = pg.Surface((self.w,self.h))
-		surface.set_alpha(self.color[3])
-		surface.fill(self.color[0:3])
-		new = pg.transform.rotate(surface, self.rotation)
-		rect = new.get_rect()
-		rect.center = (self.x + self.w/2, self.y + self.h/2)
-		window.blit(new,rect)
+		pg.draw.arc(window, self.color, [self.x,self.y,self.w,self.h], self.start_angle, self.stop_angle, self.width)
+
+class Textbox():
+	def __init__(
+			self,
+			position: list[int,int,int,int],
+			default_text: str = "",
+			text_color: tuple[int,int,int] = (0,0,0),
+			background_color: tuple[int,int,int] = (50,50,50),
+			foreground_color: tuple[int,int,int] = (200,200,200),
+			outline: int = 2,
+			max_length: int = 999,
+		):
+
+		self.background_color = background_color
+		self.foreground_color = foreground_color
+
+		self.text = default_text
+		self.draw_text = Text(self.text,[position[0] + 5, position[1] + position[3] / 2],color=text_color,font_size=position[3]//2,center=[CENTER,LEFT])
+
+		self.outline = outline
+		self.max_length = max_length
+
+		self.collision_mask = self.x,self.y,self.w,self.h = position
+
+	def update(self,window):
+		for e in window.keys_down:
+			if e.key == pg.K_BACKSPACE:
+				self.text = self.text[:-1]
+			else:
+				if len(self.text) <= self.max_length:
+					self.text += e.unicode
+
+		if len(window.keys_down) > 0: self.draw_text.update(self.text)
+
+	def draw(self,window):
+		if self.outline > 0: pg.draw.rect(window, self.background_color, [self.x,self.y,self.w,self.h])
+		pg.draw.rect(window, self.foreground_color, [self.x+self.outline,self.y+self.outline,self.w-self.outline*2,self.h-self.outline*2])
+
+		self.draw_text.x, self.draw_text.y = self.x + 5, self.y + self.h / 2
+
+		self.draw_text.draw(window)
```

### Comparing `GameMaker-0.1.3/src/GameMaker/Globals.py` & `GameMaker-0.1.4/src/GameMaker/Globals.py`

 * *Files identical despite different names*

### Comparing `GameMaker-0.1.3/src/GameMaker/Helper.py` & `GameMaker-0.1.4/src/GameMaker/Helper.py`

 * *Files identical despite different names*

### Comparing `GameMaker-0.1.3/src/GameMaker/Physics.py` & `GameMaker-0.1.4/src/GameMaker/Physics.py`

 * *Files identical despite different names*

### Comparing `GameMaker-0.1.3/src/GameMaker/__init__.py` & `GameMaker-0.1.4/src/GameMaker/__init__.py`

 * *Files 9% similar despite different names*

```diff
@@ -38,14 +38,15 @@
 
 		self.RUNNING = True
 
 		self.update_title(self.title)
 
 		self.drawlist = [[],[],[]]
 		self.keys_up = []
+		self.keys_down = []
 
 		self.screen.fill(self.background_color)
 
 	def draw(self,item: list,layer: int = FOREGROUND) -> None:
 		if type(item) == list:
 			for i in item:
 				self.drawlist[layer].append(i)
@@ -60,22 +61,25 @@
 		return pg.key.get_pressed()
 
 	def get_key(self,key: int) -> bool:
 		return self.keys()[key]
 
 	def update(self) -> None:
 		self.keys_up = []
+		self.keys_down = []
 		
 		for e in pg.event.get():
 			if e.type == pg.QUIT:
 				pg.quit()
 				self.RUNNING = False
 				return
 			elif e.type == pg.KEYUP:
 				self.keys_up.append(e.key)
+			elif e.type == pg.KEYDOWN:
+				self.keys_down.append(e)
 
 		for layer in self.drawlist:
 			for item in layer:
 				item.draw(self.screen)
 
 		self.drawlist = [[],[],[]]
```

### Comparing `GameMaker-0.1.3/src/GameMaker/examples/Demo_Button.py` & `GameMaker-0.1.4/src/GameMaker/examples/Demo_Button.py`

 * *Files identical despite different names*

### Comparing `GameMaker-0.1.3/src/GameMaker/examples/Demo_Collisions.py` & `GameMaker-0.1.4/src/GameMaker/examples/Demo_Collisions.py`

 * *Files identical despite different names*

### Comparing `GameMaker-0.1.3/src/GameMaker/examples/Demo_Gravity.py` & `GameMaker-0.1.4/src/GameMaker/examples/Demo_Gravity.py`

 * *Files identical despite different names*

### Comparing `GameMaker-0.1.3/src/GameMaker/examples/Demo_Text.py` & `GameMaker-0.1.4/src/GameMaker/examples/Demo_Text.py`

 * *Files identical despite different names*

### Comparing `GameMaker-0.1.3/src/GameMaker.egg-info/PKG-INFO` & `GameMaker-0.1.4/src/GameMaker.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: GameMaker
-Version: 0.1.3
+Version: 0.1.4
 Summary: pygame Wrapper for drawing/making games
 Author-email: Dennis Yahnov <den.yakhnov@gmail.com>
 Project-URL: Homepage, https://github.com/denyahnov/GameMaker
 Project-URL: Bug Tracker, https://github.com/denyahnov/GameMaker/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `GameMaker-0.1.3/src/GameMaker.egg-info/SOURCES.txt` & `GameMaker-0.1.4/src/GameMaker.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -13,8 +13,9 @@
 src/GameMaker/examples/Demo_Button.py
 src/GameMaker/examples/Demo_Collisions.py
 src/GameMaker/examples/Demo_Gravity.py
 src/GameMaker/examples/Demo_Image.py
 src/GameMaker/examples/Demo_ImageList.py
 src/GameMaker/examples/Demo_ProgressBar.py
 src/GameMaker/examples/Demo_Text.py
+src/GameMaker/examples/Demo_Textbox.py
 src/GameMaker/examples/Demo_Window.py
```

