# Comparing `tmp/pygame_ui_controls-1.1.2-py3-none-any.whl.zip` & `tmp/pygame_ui_controls-1.1.3-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 19580 bytes, number of entries: 7
+Zip file size: 19627 bytes, number of entries: 7
 -rw-rw-r--  2.0 unx        0 b- defN 23-Jun-14 20:26 __init__.py
--rw-rw-r--  2.0 unx    33253 b- defN 23-Jul-20 19:39 pygame_ui_controls.py
--rw-rw-r--  2.0 unx    35149 b- defN 23-Jul-20 19:46 pygame_ui_controls-1.1.2.dist-info/LICENSE
--rw-rw-r--  2.0 unx      681 b- defN 23-Jul-20 19:46 pygame_ui_controls-1.1.2.dist-info/METADATA
--rw-rw-r--  2.0 unx       92 b- defN 23-Jul-20 19:46 pygame_ui_controls-1.1.2.dist-info/WHEEL
--rw-rw-r--  2.0 unx        1 b- defN 23-Jul-20 19:46 pygame_ui_controls-1.1.2.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx      584 b- defN 23-Jul-20 19:46 pygame_ui_controls-1.1.2.dist-info/RECORD
-7 files, 69760 bytes uncompressed, 18534 bytes compressed:  73.4%
+-rw-rw-r--  2.0 unx    34007 b- defN 23-Jul-23 16:40 pygame_ui_controls.py
+-rw-rw-r--  2.0 unx    35149 b- defN 23-Jul-23 16:47 pygame_ui_controls-1.1.3.dist-info/LICENSE
+-rw-rw-r--  2.0 unx      681 b- defN 23-Jul-23 16:47 pygame_ui_controls-1.1.3.dist-info/METADATA
+-rw-rw-r--  2.0 unx       92 b- defN 23-Jul-23 16:47 pygame_ui_controls-1.1.3.dist-info/WHEEL
+-rw-rw-r--  2.0 unx        1 b- defN 23-Jul-23 16:47 pygame_ui_controls-1.1.3.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx      584 b- defN 23-Jul-23 16:47 pygame_ui_controls-1.1.3.dist-info/RECORD
+7 files, 70514 bytes uncompressed, 18581 bytes compressed:  73.6%
```

## zipnote {}

```diff
@@ -1,22 +1,22 @@
 Filename: __init__.py
 Comment: 
 
 Filename: pygame_ui_controls.py
 Comment: 
 
-Filename: pygame_ui_controls-1.1.2.dist-info/LICENSE
+Filename: pygame_ui_controls-1.1.3.dist-info/LICENSE
 Comment: 
 
-Filename: pygame_ui_controls-1.1.2.dist-info/METADATA
+Filename: pygame_ui_controls-1.1.3.dist-info/METADATA
 Comment: 
 
-Filename: pygame_ui_controls-1.1.2.dist-info/WHEEL
+Filename: pygame_ui_controls-1.1.3.dist-info/WHEEL
 Comment: 
 
-Filename: pygame_ui_controls-1.1.2.dist-info/top_level.txt
+Filename: pygame_ui_controls-1.1.3.dist-info/top_level.txt
 Comment: 
 
-Filename: pygame_ui_controls-1.1.2.dist-info/RECORD
+Filename: pygame_ui_controls-1.1.3.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## pygame_ui_controls.py

```diff
@@ -490,18 +490,27 @@
         self.center_width = size[0] - 2 * self.radius - 2 * Slider.thickness
 
         if range[0] > value or range[1] < value:
             value = range[1]
         self.value = value
 
         self.appearence = self.appearences()
+    
+    #############
+    #  GETTERS  #
+    #############
+    def get_value(name):
+        return UI.dict[Slider.__name__][name].value
+
+    #############
+    #  SETTERS  #
+    #############
+    def set_on_value_changed(name, function):
+        UI.dict[Slider.__name__][name].on_value_changed = function
 
-    ###############
-    #   SETTERS   #
-    ###############
     def set_ticks(name, ticks):
         self = UI.dict[Slider.__name__][name]
         self.ticks = ticks
         if ticks > 0:
             self.step = (self.max - self.min) / ticks
         
         self.appearence = self.appearences()
@@ -531,17 +540,17 @@
         self.radius = (size[1] - 2 * Slider.thickness) / 2
         self.center_width = size[0] - 2 * self.radius - 2 * Slider.thickness
 
         self.rect = pygame.Rect(self.pos, size)
 
         self.appearence = self.appearences()
 
-    ##################
-    #   APPEARENCE   #
-    ##################
+    ################
+    #  APPEARENCE  #
+    ################
     def appearences(self):
         radius = int(self.radius)
 
         outer_rect = (0, 0, *self.size)
         inner_rect = (Slider.thickness, Slider.thickness, self.size[0] - 2 * Slider.thickness, self.size[1] - 2 * Slider.thickness)
 
         locked = pygame.Surface(self.size, pygame.SRCALPHA)
@@ -564,17 +573,17 @@
         locked = locked.convert_alpha()
         down = down.convert_alpha()
         hovered = hovered.convert_alpha()
         classic = classic.convert_alpha()
 
         return {'locked': locked, 'down': down, 'hovered': hovered, 'classic': classic}
 
-    ##############
-    #   UPDATE   #
-    ##############
+    ############
+    #  UPDATE  #
+    ############
     def on_logic_update(self, x, y):
         if self == UI.focused and not self.locked:
             self.update_value(x)
 
     def display(self, surface):
         x = self.get_button_pos()
 
@@ -721,20 +730,22 @@
     #  SETTERS  #
     #############
     def set_pos(name, pos):
         self = UI.dict[CheckBox.__name__][name]
         self.pos = pos
         self.setup_pos()
         self.rect = pygame.Rect(self.pos, self.size)
+        self.appearence = self.appearences()
     
     def set_size(name, size):
         self = UI.dict[CheckBox.__name__][name]
         self.size = size
         self.setup_pos()
         self.rect = pygame.Rect(self.pos, self.size)
+        self.appearence = self.appearences()
 
     def uncheck(name):
         UI.dict[CheckBox.__name__][name].checked = False
 
     def check(name):
         UI.dict[CheckBox.__name__][name].checked = True
 
@@ -743,14 +754,17 @@
     
     def set_link(name, others):
         self = UI.dict[CheckBox.__name__][name]
         tmp = others.copy()
         tmp.remove(name)
         self.linked = tmp
         self.is_linked = True
+    
+    def set_on_action(name, function):
+        UI.dict[CheckBox.__name__][name].on_action = function
 
     ################
     #  APPEARENCE  #
     ################
     def appearences(self):
         radius = CheckBox.border_radius
 
@@ -813,15 +827,15 @@
             if hasattr(self, 'on_action'):
                 self.on_action(self.checked)
 
     ###########
     #  UTILS  #
     ###########
     def setup_pos(self):
-        self.tick_center = (self.pos[0] + self.size[0] / 2, self.pos[1] + self.size[0] / 2)
+        self.tick_center = (self.pos[0] + self.size[0] / 2, self.pos[1] + self.size[1] / 2)
 
     def uncheck_others(self):
         for name in self.linked:
             UI.dict[CheckBox.__name__][name].checked = False
 
     def checkable(self):
         for name in self.linked:
@@ -855,37 +869,49 @@
     ```python
     Text("text_id", (0, 0), "Hello World !", color=(255, 0, 0), centered=(True, True))
     Text.set_text("text_id", "Hello World !")
     Text.set_text_color("text_id", "#0000ff")
     ```
     """
 
-    def __init__(self, name:str, pos, text="Text", color=None, centered=(False, False)):
+    def __init__(self, name, pos, text="Text", color=None, centered=(False, False)):
         UI.__init__(self, name, pos, size=(0, 0), hoverable=False, locked=False)
 
         self.color = color
         if color == None:
             self.color = (255, 255, 255)
 
         self.text = text
         self.centered = centered
         self.appearence = self.appearences()
+    
+    #############
+    #  GETTERS  #
+    #############
+    def get_text(name):
+        return UI.dict[Text.__name__][name].text
 
     #############
     #  SETTERS  #
     #############
     def set_text(name, text):
         self = UI.dict[Text.__name__][name]
         self.text = text
         self.appearence = self.appearences()
 
     def set_text_color(name, color):
         self = UI.dict[Text.__name__][name]
         self.color = color
         self.appearence = self.appearences()
+    
+    def set_pos(name, pos):
+        self = UI.dict[Text.__name__][name]
+        self.pos = pos
+        self.rect = pygame.Rect(self.pos, self.size)
+        self.appearence = self.appearences()
 
     ################
     #  APPEARENCE  #
     ################
     def appearences(self):
         rendered = UI.FONT.render(self.text, self.color)
         self.size = rendered[0].get_size()
```

## Comparing `pygame_ui_controls-1.1.2.dist-info/LICENSE` & `pygame_ui_controls-1.1.3.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `pygame_ui_controls-1.1.2.dist-info/METADATA` & `pygame_ui_controls-1.1.3.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pygame-ui-controls
-Version: 1.1.2
+Version: 1.1.3
 Summary: Pygame UI controls
 Home-page: https://github.com/ArthurLeFloch/PygameUI
 Author: Arthur Le Floch
 Author-email: alf.github@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
```

