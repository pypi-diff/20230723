# Comparing `tmp/processpiper-0.4.1.tar.gz` & `tmp/processpiper-0.4.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "processpiper-0.4.1.tar", last modified: Fri Jun 23 09:11:15 2023, max compression
+gzip compressed data, was "processpiper-0.4.2.tar", last modified: Sun Jul 23 06:15:55 2023, max compression
```

## Comparing `processpiper-0.4.1.tar` & `processpiper-0.4.2.tar`

### file list

```diff
@@ -1,34 +1,34 @@
-drwxrwxrwx   0        0        0        0 2023-06-23 09:11:15.102582 processpiper-0.4.1/
--rw-rw-rw-   0        0        0     1084 2023-01-11 04:26:51.000000 processpiper-0.4.1/LICENSE
--rw-rw-rw-   0        0        0     6885 2023-06-23 09:11:15.101581 processpiper-0.4.1/PKG-INFO
--rw-rw-rw-   0        0        0     6330 2023-06-23 09:06:58.000000 processpiper-0.4.1/README.md
--rw-rw-rw-   0        0        0     1014 2023-06-23 09:06:58.000000 processpiper-0.4.1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-06-23 09:11:15.102582 processpiper-0.4.1/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-06-23 09:11:15.065266 processpiper-0.4.1/src/
-drwxrwxrwx   0        0        0        0 2023-06-23 09:11:15.083582 processpiper-0.4.1/src/processpiper/
--rw-rw-rw-   0        0        0      188 2023-04-09 10:02:01.000000 processpiper-0.4.1/src/processpiper/__init__.py
--rw-rw-rw-   0        0        0     2372 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/activity.py
--rw-rw-rw-   0        0        0    11722 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/colourtheme.py
--rw-rw-rw-   0        0        0     1881 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/constants.py
--rw-rw-rw-   0        0        0    12129 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/event.py
--rw-rw-rw-   0        0        0     2339 2023-04-09 09:10:37.000000 processpiper-0.4.1/src/processpiper/footer.py
--rw-rw-rw-   0        0        0     4359 2023-05-16 08:14:49.000000 processpiper-0.4.1/src/processpiper/gateway.py
--rw-rw-rw-   0        0        0     2849 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/helper.py
--rw-rw-rw-   0        0        0     9263 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/lane.py
--rw-rw-rw-   0        0        0    17162 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/layout.py
--rw-rw-rw-   0        0        0    45124 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/painter.py
--rw-rw-rw-   0        0        0     4946 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/pool.py
--rw-rw-rw-   0        0        0    19547 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/processmap.py
--rw-rw-rw-   0        0        0    39735 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/shape.py
--rw-rw-rw-   0        0        0    11494 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/text2diagram.py
--rw-rw-rw-   0        0        0     2263 2023-05-16 08:14:49.000000 processpiper-0.4.1/src/processpiper/title.py
--rw-rw-rw-   0        0        0     1189 2023-06-23 09:06:58.000000 processpiper-0.4.1/src/processpiper/version.py
-drwxrwxrwx   0        0        0        0 2023-06-23 09:11:15.099580 processpiper-0.4.1/src/processpiper.egg-info/
--rw-rw-rw-   0        0        0     6885 2023-06-23 09:11:15.000000 processpiper-0.4.1/src/processpiper.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      762 2023-06-23 09:11:15.000000 processpiper-0.4.1/src/processpiper.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-06-23 09:11:15.000000 processpiper-0.4.1/src/processpiper.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       14 2023-06-23 09:11:15.000000 processpiper-0.4.1/src/processpiper.egg-info/requires.txt
--rw-rw-rw-   0        0        0       19 2023-06-23 09:11:15.000000 processpiper-0.4.1/src/processpiper.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-06-23 09:11:15.100582 processpiper-0.4.1/src/tests/
--rw-rw-rw-   0        0        0        0 2023-04-09 04:19:21.000000 processpiper-0.4.1/src/tests/__init__.py
--rw-rw-rw-   0        0        0     2170 2023-04-17 09:21:44.000000 processpiper-0.4.1/src/tests/github_action_test.py
+drwxrwxrwx   0        0        0        0 2023-07-23 06:15:55.737678 processpiper-0.4.2/
+-rw-rw-rw-   0        0        0     1084 2023-01-11 04:26:51.000000 processpiper-0.4.2/LICENSE
+-rw-rw-rw-   0        0        0     6654 2023-07-23 06:15:55.737678 processpiper-0.4.2/PKG-INFO
+-rw-rw-rw-   0        0        0     6099 2023-07-23 06:14:11.000000 processpiper-0.4.2/README.md
+-rw-rw-rw-   0        0        0     1030 2023-07-23 06:14:11.000000 processpiper-0.4.2/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 06:15:55.737678 processpiper-0.4.2/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 06:15:55.703677 processpiper-0.4.2/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 06:15:55.725678 processpiper-0.4.2/src/processpiper/
+-rw-rw-rw-   0        0        0      188 2023-04-09 10:02:01.000000 processpiper-0.4.2/src/processpiper/__init__.py
+-rw-rw-rw-   0        0        0     2372 2023-06-23 09:06:58.000000 processpiper-0.4.2/src/processpiper/activity.py
+-rw-rw-rw-   0        0        0    11722 2023-06-23 09:06:58.000000 processpiper-0.4.2/src/processpiper/colourtheme.py
+-rw-rw-rw-   0        0        0     1881 2023-06-23 09:06:58.000000 processpiper-0.4.2/src/processpiper/constants.py
+-rw-rw-rw-   0        0        0    12129 2023-06-23 09:06:58.000000 processpiper-0.4.2/src/processpiper/event.py
+-rw-rw-rw-   0        0        0     2339 2023-04-09 09:10:37.000000 processpiper-0.4.2/src/processpiper/footer.py
+-rw-rw-rw-   0        0        0     4359 2023-05-16 08:14:49.000000 processpiper-0.4.2/src/processpiper/gateway.py
+-rw-rw-rw-   0        0        0     3291 2023-07-23 06:14:11.000000 processpiper-0.4.2/src/processpiper/helper.py
+-rw-rw-rw-   0        0        0     9558 2023-07-23 06:14:11.000000 processpiper-0.4.2/src/processpiper/lane.py
+-rw-rw-rw-   0        0        0    19270 2023-07-23 06:14:11.000000 processpiper-0.4.2/src/processpiper/layout.py
+-rw-rw-rw-   0        0        0    46744 2023-07-23 06:14:11.000000 processpiper-0.4.2/src/processpiper/painter.py
+-rw-rw-rw-   0        0        0     4946 2023-06-23 09:06:58.000000 processpiper-0.4.2/src/processpiper/pool.py
+-rw-rw-rw-   0        0        0    21262 2023-07-23 06:14:11.000000 processpiper-0.4.2/src/processpiper/processmap.py
+-rw-rw-rw-   0        0        0    39089 2023-07-23 06:14:11.000000 processpiper-0.4.2/src/processpiper/shape.py
+-rw-rw-rw-   0        0        0    11494 2023-06-23 09:06:58.000000 processpiper-0.4.2/src/processpiper/text2diagram.py
+-rw-rw-rw-   0        0        0     2263 2023-05-16 08:14:49.000000 processpiper-0.4.2/src/processpiper/title.py
+-rw-rw-rw-   0        0        0     1189 2023-07-23 06:14:11.000000 processpiper-0.4.2/src/processpiper/version.py
+drwxrwxrwx   0        0        0        0 2023-07-23 06:15:55.734678 processpiper-0.4.2/src/processpiper.egg-info/
+-rw-rw-rw-   0        0        0     6654 2023-07-23 06:15:55.000000 processpiper-0.4.2/src/processpiper.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      762 2023-07-23 06:15:55.000000 processpiper-0.4.2/src/processpiper.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 06:15:55.000000 processpiper-0.4.2/src/processpiper.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       27 2023-07-23 06:15:55.000000 processpiper-0.4.2/src/processpiper.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       19 2023-07-23 06:15:55.000000 processpiper-0.4.2/src/processpiper.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 06:15:55.735676 processpiper-0.4.2/src/tests/
+-rw-rw-rw-   0        0        0        0 2023-04-09 04:19:21.000000 processpiper-0.4.2/src/tests/__init__.py
+-rw-rw-rw-   0        0        0     2170 2023-04-17 09:21:44.000000 processpiper-0.4.2/src/tests/github_action_test.py
```

### Comparing `processpiper-0.4.1/LICENSE` & `processpiper-0.4.2/LICENSE`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/pyproject.toml` & `processpiper-0.4.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
     "Programming Language :: Python :: 3.10",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
-dependencies = ['Pillow>=9.5.0']
+dependencies = ['Pillow>=9.5.0', 'rich>=13.4.2']
 
 [project.urls]
 "Homepage" = "https://github.com/csgoh/processpiper"
 "Bug Tracker" = "https://github.com/csgoh/processpiper/issues"
 
 [tool.setuptools.packages.find]
 where = ["src"] # list of folders that contain the packages (["."] by default)
```

### Comparing `processpiper-0.4.1/src/processpiper/activity.py` & `processpiper-0.4.2/src/processpiper/activity.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/colourtheme.py` & `processpiper-0.4.2/src/processpiper/colourtheme.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/constants.py` & `processpiper-0.4.2/src/processpiper/constants.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/event.py` & `processpiper-0.4.2/src/processpiper/event.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/footer.py` & `processpiper-0.4.2/src/processpiper/footer.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/gateway.py` & `processpiper-0.4.2/src/processpiper/gateway.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/helper.py` & `processpiper-0.4.2/src/processpiper/helper.py`

 * *Files 19% similar despite different names*

```diff
@@ -16,29 +16,36 @@
 # IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
 # FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 # AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 # LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 # OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 # SOFTWARE.
 import logging
+from rich.console import Console
+from rich.panel import Panel
 
 
 class Helper:
     show_layout_grid = False
     show_pool_lane = False
     show_x_position = False
     show_y_position = False
     show_draw_position = False
-    show_draw_connection = False
     show_draw = False
+    show_draw_connection = False
     show_general = False
 
     @staticmethod
     def printc(
-        message: str, color: str = "30", end: str = "\n", show_level: str = "general"
+        message: str,
+        color: str = "30",
+        reverse: bool = False,
+        end: str = "\n",
+        rich_type: str = "text",
+        show_level: str = "general",
     ):
         """Print text in color"""
 
         root_logger = logging.getLogger()
 
         if root_logger.getEffectiveLevel() == logging.DEBUG and (
             (show_level == "layout_grid" and Helper.show_layout_grid)
@@ -46,24 +53,30 @@
             or (show_level == "x_position" and Helper.show_x_position)
             or (show_level == "y_position" and Helper.show_y_position)
             or (show_level == "draw_connection" and Helper.show_draw_connection)
             or (show_level == "draw_position" and Helper.show_draw_position)
             or (show_level == "draw" and Helper.show_draw)
             or (show_level == "general" and Helper.show_general)
         ):
-            print(f"\033[1;{color}m{message}\033[0m", end=end)
+            console = Console()
+            if rich_type == "text":
+                style_attribute = "reverse" if reverse else ""
+                console.print(message, end=end, style=style_attribute)
+            elif rich_type == "panel":
+                console.print(Panel(message), style="blue")
 
     @staticmethod
     def print_info(message: str, color: str = "30", end: str = "\n"):
         """Print text in color"""
 
         root_logger = logging.getLogger()
 
         if root_logger.getEffectiveLevel() == logging.INFO:
-            print(f"\033[1;{color}m{message}\033[0m", end=end)
+            console = Console()
+            console.print(f"\033[1;{color}m{message}\033[0m", end=end)
 
     @staticmethod
     def debug_log(message: str):
         """Log debug message"""
         logging.debug(message)
 
     @staticmethod
```

### Comparing `processpiper-0.4.1/src/processpiper/lane.py` & `processpiper-0.4.2/src/processpiper/lane.py`

 * *Files 8% similar despite different names*

```diff
@@ -126,26 +126,14 @@
         type: EventType | ActivityType | GatewayType,
         font: str = "",
         font_size: int = 0,
         font_colour: str = "",
         fill_colour: str = "",
         text_alignment: str = "",
     ) -> Shape:
-        """Add an element to the lane"""
-        # if font == "":
-        #     font = self.painter.element_font
-        # if font_size == 0:
-        #     font_size = self.painter.element_font_size
-        # if font_colour == "":
-        #     font_colour = self.painter.element_font_colour
-        # if fill_colour == "":
-        #     fill_colour = self.painter.element_fill_colour
-        # if text_alignment == "":
-        #     text_alignment = self.painter.element_text_alignment
-
         font = font or self.painter.element_font
         font_size = font_size or self.painter.element_font_size
         font_colour = font_colour or self.painter.element_font_colour
         fill_colour = fill_colour or self.painter.element_fill_colour
         text_alignment = text_alignment or self.painter.element_text_alignment
 
         event_class = globals()[type]
@@ -205,30 +193,49 @@
         ###self.painter.draw_grid()
 
     def draw_shape(self) -> None:
         """Draw the shapes in the lane"""
         if self.shapes:
             for shape in self.shapes:
                 Helper.printc(
-                    f"      Drawing shape: {shape.name}, x={shape.x}, y={shape.y}, w={shape.width}, h={shape.height}",
+                    f"      Drawing shape: [bold][red]\[{shape.name}][/red][/bold], x={shape.x}, y={shape.y}, w={shape.width}, h={shape.height}",
+                    rich_type="text",
                     show_level="draw",
                 )
+
                 shape.draw(self.painter)
 
+    # def _find_start_shape(self) -> Shape:
+    #     """Find the start shape in the process map"""
+    #     if self.shapes:
+    #     for pool in self._pools:
+    #         for lane in pool.lanes:
+    #             for shape in lane.shapes:
+    #                 ### If the shape has no connection_from, it is the start shape
+    #                 Helper.printc(
+    #                     f"{shape.name} - {len(shape.connection_from)}",
+    #                     show_level="layout_grid",
+    #                 )
+    #                 if len(shape.connection_from) == 0:
+    #                     return shape
+    #     return None
+
     def draw_connection(self, all_shapes: list) -> None:
         """Draw the connections in the lane"""
+
+        Helper.printc(
+            f"Lane: {self.name}", show_level="draw_connection", rich_type="panel"
+        )
         if self.shapes:
-            for shape in self.shapes:
-                shape.draw_connection(self.painter, all_shapes)
+            shape = self.shapes[0]
+            shape.draw_connection(self.painter, all_shapes)
 
     def set_draw_position(self, x: int, y: int, layout_grid: Grid) -> None:
         """Set the draw position of the lane"""
 
-        # self.painter = painter
-
         ### Determine the number of rows for the lane
         lane_row_count = layout_grid.get_lane_row_count(self.id)
 
         ### Determine lane x and y position
         self.x = (
             x
             if x > 0
```

### Comparing `processpiper-0.4.1/src/processpiper/layout.py` & `processpiper-0.4.2/src/processpiper/layout.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,8 +1,10 @@
 from dataclasses import dataclass, field
+from rich.console import Console
+from rich.table import Table
 from .shape import Shape
 from .helper import Helper
 
 
 @dataclass
 class Grid:
     _pools: list = field(init=False, default_factory=list)
@@ -34,29 +36,33 @@
         previous_shape: Shape,
         current_shape: Shape,
         index: int = 0,
     ):
         """Set the position of the shapes in the grid"""
         if current_shape.grid_traversed is True:
             Helper.printc(
-                f"{current_shape.name} is already traversed", show_level="layout_grid"
+                f"[orange4]{current_shape.name} is already traversed[/]",
+                show_level="layout_grid",
             )
             return
-        Helper.printc(f"Traversing [{current_shape.name}]", show_level="layout_grid")
+        Helper.printc(
+            f"Traversing [red]{current_shape.name}[/]", show_level="layout_grid"
+        )
         current_shape.grid_traversed = True
         self.add_shape_to_grid(previous_shape, current_shape, index)
         for connection_index, next_connection in enumerate(current_shape.connection_to):
             next_shape = next_connection.target
             Helper.printc(
-                f"    {connection_index}: [{current_shape.name}]->[{next_shape.name}]",
+                f"    [dodger_blue1]{connection_index}: {current_shape.name} -> {next_shape.name}[/]",
                 show_level="layout_grid",
             )
             self.set_shapes_position(current_shape, next_shape, connection_index)
         Helper.printc(
-            f"Done traversing [{current_shape.name}]", show_level="layout_grid"
+            f"Done traversing [:thumbsup: {current_shape.name}]",
+            show_level="layout_grid",
         )
 
     def add_shape_to_grid(
         self, previous_shape: Shape, current_shape: Shape, index: int
     ):
         """Add the shape to the grid"""
         ### If previous_shape is None, it is the start shape
@@ -107,15 +113,16 @@
                             current_shape,
                         )
                     else:
                         Helper.printc("Not empty", 34, show_level="layout_grid")
                         self.add_shape_to_lane_rowcolumn(
                             current_shape.lane_id,
                             index + 1,
-                            previous_shape_col_number + 1,
+                            # previous_shape_col_number + 1,
+                            previous_shape_col_number,
                             current_shape,
                         )
             elif index == 0:
                 if self.is_same_pool(previous_shape, current_shape):
                     Helper.printc(
                         f"        ==> {index=}, Same pool, diff lane: add_shape_to_lane [{current_shape.name}], {previous_shape_row_number+1}",
                         show_level="layout_grid",
@@ -327,15 +334,15 @@
         row_number = f"row{row_number}"
         for col_number in range(max_columns + 1):
             for row, col in self._grid[lane_id].items():
                 if row == row_number and col[col_number - 1] is not None:
                     last_column = col_number
         return last_column + 1
 
-    def format_item(self, item, repeat: bool = False):
+    def format_itemX(self, item, repeat: bool = False):
         # sourcery skip: assign-if-exp, simplify-boolean-comparison
         """Format the item"""
         # get the first 20 characters from item
         item = str(item)[:20]
         fixed_length = 20
 
         if repeat is False:
@@ -344,29 +351,46 @@
             spaces = item * fixed_length
 
         if item == "None":
             return f"{spaces}|"
 
         return item + spaces[: fixed_length - len(item)] + "|"
 
+    def format_item(self, item, repeat: bool = False):
+        # sourcery skip: assign-if-exp, simplify-boolean-comparison
+        """Format the item"""
+        # get the first 20 characters from item
+        item = str(item)[:20]
+        fixed_length = 20
+
+        if repeat is False:
+            spaces = " " * fixed_length
+        else:
+            spaces = item * fixed_length
+
+        if item == "None":
+            return f"{spaces}"
+
+        return item + spaces[: fixed_length - len(item)]
+
     def get_max_column_count(self):
         """Get the max number of columns"""
         max_columns = 0
         # calculate max number of columns
         for _, lane in self._grid.items():
             for _, col in lane.items():
                 if len(col) > max_columns:
                     max_columns = len(col)
         return max_columns
 
     def get_lane_row_count(self, lane_id: str):
         """Get the lane row count"""
         return len(self._grid[lane_id])
 
-    def print_header(
+    def print_headerX(
         self,
     ):
         """Print the header"""
         max_columns = self.get_max_column_count()
         # calculate max number of columns
         for _, lane in self._grid.items():
             for _, col in lane.items():
@@ -394,15 +418,49 @@
                     end="",
                     color=33,
                     show_level="layout_grid",
                 )
             Helper.printc("", show_level="layout_grid")
             break
 
+    def print_header(self, table: Table):
+        max_columns = self.get_max_column_count()
+        for _, lane in self._grid.items():
+            for _, col in lane.items():
+                if len(col) > max_columns:
+                    max_columns = len(col)
+
+        for _, lane in self._grid.items():
+            table.add_column("ROW \ COL")
+            for i in range(max_columns):
+                table.add_column(self.format_item(i + 1))
+            break
+
     def print_grid(self):
+        if Helper.show_layout_grid is True:
+            for lane_id, lane in self._grid.items():
+                Helper.printc(f"{lane_id=}", color=33, show_level="layout_grid")
+                console = Console()
+                table = Table(
+                    show_header=True, header_style="bold magenta", show_lines=True
+                )
+                self.print_header(table)
+                for row_number, col in lane.items():
+                    row_data = [self.format_item(row_number)]
+                    for item in col:
+                        if item is not None:
+                            row_data.append(self.format_item(item.name))
+                        else:
+                            row_data.append(self.format_item("None"))
+
+                    table.add_row(*row_data)
+
+                console.print(table)
+
+    def print_gridX(self):
         """Print the grid"""
         for lane_id, lane in self._grid.items():
             Helper.printc(f"{lane_id=}", color=33, show_level="layout_grid")
             self.print_header()
             for row_number, col in lane.items():
                 Helper.printc(
                     f"{self.format_item(row_number)}", end="", show_level="layout_grid"
```

### Comparing `processpiper-0.4.1/src/processpiper/painter.py` & `processpiper-0.4.2/src/processpiper/painter.py`

 * *Files 6% similar despite different names*

```diff
@@ -682,18 +682,18 @@
     ):
         """Get the points to draw a line between two elements"""
         x1, y1 = nearest_points["source_points"]
         x2, y2 = nearest_points["target_points"]
         face_source = nearest_points["source_name"]
         face_target = nearest_points["target_name"]
 
-        Helper.printc(
-            f"      GET_POINTS(): {x1=}, {y1=}, {face_source=}, {x2=}, {y2=}, {face_target=}",
-            show_level="draw_connection",
-        )
+        # Helper.printc(
+        #     f"      GET_POINTS(): {x1=}, {y1=}, {face_source=}, {x2=}, {y2=}, {face_target=}",
+        #     show_level="draw_connection",
+        # )
         points, _ = self.get_connection_points(x1, y1, face_source, x2, y2, face_target)
 
         return points
 
     def draw_right_angle_line(
         self,
         x1: int,
@@ -703,45 +703,54 @@
         y2: int,
         face_target: str,
         connection_style: str,
         connector_line_width: int = 0,
         connector_line_colour: str = "",
     ):
         """Draw a right angle line between two points"""
-        Helper.printc(
-            f"      DRAW_RIGHT_ANGLE_LINE() {x1=}, {y1=}, {face_source=}, {x2=}, {y2=}, {face_target=}",
-            show_level="draw_connection",
-        )
         points, right_angle_points = self.get_connection_points(
             x1, y1, face_source, x2, y2, face_target
         )
+        Helper.printc(
+            f"\t" * 2 + f"DRAW_RIGHT_ANGLE_LINE() {x1=}, {y1=}, {face_source=}, {x2=}, {y2=}, {face_target=}",
+            show_level="draw_connection",
+        )
 
         if connection_style == "dashed":
             self.draw_dashed_line(points, connector_line_width, connector_line_colour)
         else:
             self.__cr.line(
                 points, fill=(connector_line_colour), width=connector_line_width
             )
         return right_angle_points
 
     def get_connection_points(self, x1, y1, face_source, x2, y2, face_target):
         """Get the points to draw a line between two elements"""
+        tab_count = 3
         if x1 == x2 and y1 == y2:
             # Shapes are on top of each other / overlapping. NOTE: This should never happen
             Helper.printc(
-                f"      A: right_angle_line: x1 == x2 and y1 == y2: {x1}, {y1}, {x2}, {y2}",
+                 "\t" * tab_count + "Shapes are on top of each other / overlapping",
+                show_level="draw_connection",
+            )
+            Helper.printc(
+                f"\t" * tab_count + "A: right_angle_line: x1 == x2 and y1 == y2: {x1}, {y1}, {x2}, {y2}",
                 show_level="draw_connection",
             )
             points = [(x1, y1)]
             right_angle_point = points
 
         if x1 != x2 and y1 == y2:
             # Shapes are on the same horizontal line
             Helper.printc(
-                f"      B: right_angle_line: x1 != x2 and y1 == y2: {x1}, {y1}, {x2}, {y2}",
+                 "\t" * tab_count + "Shapes are on the same horizontal line",
+                show_level="draw_connection",
+            )
+            Helper.printc(
+                f"\t" * tab_count + "B: right_angle_line: x1 != x2 and y1 == y2: {x1}, {y1}, {x2}, {y2}",
                 show_level="draw_connection",
             )
             elbow_height = 40
             if face_source.find("top") != -1:
                 points = [
                     (x1, y1),
                     (x1, y1 - elbow_height),
@@ -755,85 +764,112 @@
             else:
                 points = [(x1, y1), (x2, y1)]
                 right_angle_point = [(x1, y1)]
 
         if x1 == x2 and y1 != y2:
             # Shapes are on the same vertical line
             Helper.printc(
-                f"      C: right_angle_line: x1 == x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
+                 "\t" * tab_count + "Shapes are on the same vertical line",
+                show_level="draw_connection",
+            )
+            Helper.printc(
+                f"\t" * tab_count + "C: right_angle_line: x1 == x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
                 show_level="draw_connection",
             )
             points = [(x1, y1), (x1, y2)]
             right_angle_point = [(x1, y1)]
 
         if x1 != x2 and y1 != y2:
             # Shapes are on different horizontal and vertical lines
             # check if face1 string contained the word "right"
+            Helper.printc(
+                "\t" * tab_count + "Shapes are on different horizontal and vertical lines",
+                show_level="draw_connection",
+            )
             if face_source.find("bottom") != -1:
-                Helper.printc(
-                    f"      D-bottom: right_angle_line: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
-                    show_level="draw_connection",
-                )
-                # if so, then the line should be drawn from the bottom side of the box
-                points = [(x1, y1), (x1, y2), (x2, y2)]
-                right_angle_point = [(x1, y2)]
+                if face_target.find("bottom") != -1:
+                    Helper.printc(
+                         "\t" * tab_count + "D-bottom: both bottom",
+                        show_level="draw_connection",
+                    )
+                    # if so, then the line should be drawn from the bottom side of the box
+                    angle_height = 40
+                    points = [
+                        (x1, y1),
+                        (x1, y1 + angle_height),
+                        (x2, y1 + angle_height),
+                        (x2, y2),
+                    ]
+                    right_angle_point = [
+                        (x1, y1 + angle_height),
+                        (x2, y1 + angle_height),
+                    ]
+                else:
+                    Helper.printc(
+                         "\t" * tab_count + "D-bottom: source bottom",
+                        show_level="draw_connection",
+                    )
+                    # if so, then the line should be drawn from the bottom side of the box
+                    points = [
+                        (x1, y1),
+                        (x1, y2),
+                        (x2, y2),
+                    ]
+                    right_angle_point = [(x1, y2)]
             elif face_source.find("right") != -1:
                 Helper.printc(
-                    f"      D-right: right_angle_line: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
+                    f"\t" * tab_count + "D-right: right_angle_line: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
                     show_level="draw_connection",
                 )
                 if face_target.find("left") != -1:
-                    # points = [(x1, y1), (x1, y2), (x2, y2)]
                     elbow_height = 40
                     points = [
                         (x1, y1),
                         (x1 + elbow_height, y1),
                         (x1 + elbow_height, y2),
                         (x2, y2),
                     ]
-                    # right_angle_point = (x1 + elbow_height, y2)
                     right_angle_point = [
                         (x1 + elbow_height, y1),
                         (x1 + elbow_height, y2),
                     ]
                 elif face_target.find("right") != -1:
-                    # points = [(x1, y1), (x2, y1), (x2, y2)]
-                    # right_angle_point = [(x2, y1)]
                     elbow_height = 40
-                    # points = [(x1, y1), (x2, y1), (x2, y2)]
                     ### both faces are right
                     Helper.printc(
-                        "      D-right-right (x1 < x2)", show_level="draw_connection"
+                         "\t" * tab_count + "D-right-right (x1 < x2)",
+                        show_level="draw_connection",
                     )
                     points = [
                         (x1, y1),
                         (x2 + elbow_height, y1),
                         (x2 + elbow_height, y2),
                         (x2, y2),
                     ]
                     right_angle_point = [
                         (x2 + elbow_height, y1),
                         (x2 + elbow_height, y2),
                     ]
                 elif face_target.find("top") != -1:
                     if y1 < y2:
                         Helper.printc(
-                            "      D-right-top (y1 < y2)", show_level="draw_connection"
+                             "\t" * 2 + "D-right-top (y1 < y2)",
+                            show_level="draw_connection",
                         )
                         points = [
                             (x1, y1),
                             (x2, y1),
                             (x2, y2),
                         ]
                         right_angle_point = [
                             (x2, y1),
                         ]
                     else:
                         Helper.printc(
-                            "      D-right-top (y1 >= y2)",
+                             "\t" * tab_count + "D-right-top (y1 >= y2)",
                             show_level="draw_connection",
                         )
                         vertical_elbow_height = 40
                         horizontal_elbow_height = 60
                         points = [
                             (x1, y1),
                             (x2 + horizontal_elbow_height, y1),
@@ -843,69 +879,71 @@
                         ]
                         right_angle_point = [
                             (x2 + horizontal_elbow_height, y1),
                             (x2 + horizontal_elbow_height, y2 - vertical_elbow_height),
                             (x2, y2 - vertical_elbow_height),
                         ]
                 else:
-                    Helper.printc("      D-right-bottom", show_level="draw_connection")
+                    Helper.printc(
+                         "\t" * tab_count + "D-right-bottom", show_level="draw_connection"
+                    )
                     points = [
                         (x1, y1),
                         (x2, y1),
                         (x2, y2),
                     ]
                     right_angle_point = [
                         (x2, y1),
                     ]
             elif face_source.find("top") != -1 and face_target.find("top") != -1:
                 Helper.printc(
-                    f"      D-top: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
+                    f"\t" * tab_count + "D-top: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
                     show_level="draw_connection",
                 )
                 # draw 1 right angle line
                 elbow_height = 40
                 points = [
                     (x1, y1),
                     (x1, y1 - elbow_height),
                     (x2, y1 - elbow_height),
                     (x2, y2),
                 ]
                 # right_angle_point = (x2, y2 - elbow_height)
                 right_angle_point = [(x1, y1 - elbow_height), (x2, y1 - elbow_height)]
             elif face_source.find("top") != -1 and face_target.find("bottom") != -1:
                 Helper.printc(
-                    f"      D-top/bottom: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
+                    f"\t" * tab_count + "D-top/bottom: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
                     show_level="draw_connection",
                 )
                 # draw 1 right angle line
                 elbow_height = 20
                 points = [
                     (x1, y1),
                     (x1, y1 - elbow_height),
                     (x2, y1 - elbow_height),
                     (x2, y2),
                 ]
                 # right_angle_point = (x2, y1 - elbow_height)
                 right_angle_point = [(x1, y1 - elbow_height), (x2, y1 - elbow_height)]
             else:
                 Helper.printc(
-                    f"      D-else: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
+                    f"\t" * tab_count + "D-else: x1 != x2 and y1 != y2: {x1}, {y1}, {x2}, {y2}",
                     show_level="draw_connection",
                 )
                 # if so, then the line should be drawn from the bottom side of the box
                 points = [(x1, y1), (x1, y2), (x2, y2)]
                 right_angle_point = [(x1, y2)]
                 # for point in points:
                 #     self.draw_circle(point[0], point[1], 4, "yellow")
 
         if x1 > x2:
             if y1 <= y2:
                 if abs(y1 - y2) == 10:
                     Helper.printc(
-                        f"      E: x1 > x2 and y1 <= y2: {x1}, {y1}, {x2}, {y2}",
+                        f"\t" * tab_count + "E: x1 > x2 and y1 <= y2: {x1}, {y1}, {x2}, {y2}",
                         show_level="draw_connection",
                     )
                     elbow_height = 40
                     points = [
                         (x1, y1),
                         (x1, y1 - elbow_height),
                         (x2, y1 - elbow_height),
@@ -919,15 +957,15 @@
                 if abs(y1 - y2) >= 100:
                     elbow_height = 40
                     if (
                         face_source.find("bottom") == -1
                         or face_target.find("right") == -1
                     ):
                         Helper.printc(
-                            f"      F2: x1 > x2 and y1 <= y2: {x1}, {y1}, {x2}, {y2}",
+                            f"\t" * tab_count + "F2: x1 > x2 and y1 <= y2: {x1}, {y1}, {x2}, {y2}",
                             show_level="draw_connection",
                         )
                         points = [
                             (x1, y1),
                             (x1, y1 + elbow_height),
                             (x2, y1 + elbow_height),
                             (x2, y2),
@@ -935,26 +973,26 @@
                         # right_angle_point = (x2, y1 - elbow_height)
                         right_angle_point = [
                             (x1, y1 - elbow_height),
                             (x2, y1 - elbow_height),
                         ]
                     else:
                         Helper.printc(
-                            f"      F1: x1 > x2 and y1 <= y2: {x1}, {y1}, {x2}, {y2}",
+                            f"\t" * tab_count + "F1: x1 > x2 and y1 <= y2: {x1}, {y1}, {x2}, {y2}",
                             show_level="draw_connection",
                         )
                         points = [
                             (x1, y1),
                             (x1, y2),
                             (x2, y2),
                         ]
                         right_angle_point = [(x1, y2)]
             elif len(points) == 0:
                 Helper.printc(
-                    f"      G: x1 > x2 and y1 > y2: {x1=}, {y1=}, {x2=}, {y2=}",
+                    f"\t" * tab_count + "G: x1 > x2 and y1 > y2: {x1=}, {y1=}, {x2=}, {y2=}",
                     show_level="draw_connection",
                 )
                 elbow_height = (y1 - y2) / 2
                 points = [
                     (x1, y1),
                     (x1, y1 - elbow_height),
                     (x2, y2 + elbow_height),
@@ -1019,41 +1057,41 @@
         if label_x_pos == x1 and label_y_pos == y1:
             ### There is no right angle point
             label_x_pos = max(x1 + 5, x1 + (((x2 - x1) - label_w) / 2))
             if y1 == y2:
                 label_y_pos = y1 - label_h - 3
             else:
                 label_y_pos = y1 + ((y2 - y1) / 2) - (label_h / 2)
-            Helper.printc(
-                f"        @@@ {label=} No right angle point",
-                35,
-                show_level="draw_connection",
-            )
+            # Helper.printc(
+            #     f"        @@@ {label=} No right angle point",
+            #     35,
+            #     show_level="draw_connection",
+            # )
 
         else:
             label_x_pos += 5
             if y1 == y2 or (abs(y1 - y2) <= 10):
-                Helper.printc(
-                    f"        @@@ {label=} {y1} == {y2}",
-                    35,
-                    show_level="draw_connection",
-                )
+                # Helper.printc(
+                #     f"        @@@ {label=} {y1} == {y2}",
+                #     35,
+                #     show_level="draw_connection",
+                # )
                 label_y_pos = label_y_pos + label_h
             else:
-                Helper.printc(
-                    f"        @@@ {label=} {y1} != {y2}",
-                    35,
-                    show_level="draw_connection",
-                )
+                # Helper.printc(
+                #     f"        @@@ {label=} {y1} != {y2}",
+                #     35,
+                #     show_level="draw_connection",
+                # )
                 label_y_pos = y1 + ((y2 - y1) / 2) - (label_h / 2)
-            Helper.printc(
-                f"        @@@ {label=} With right angle point",
-                35,
-                show_level="draw_connection",
-            )
+            # Helper.printc(
+            #     f"        @@@ {label=} With right angle point",
+            #     35,
+            #     show_level="draw_connection",
+            # )
 
         self.draw_text(
             label_x_pos,
             label_y_pos,
             label,
             connector_font,
             connector_font_size,
@@ -1225,15 +1263,14 @@
         Args:
             width (int): Surface width
             height (int): Surface height
         """
         left, top, right, bottom = 0, 0, width, height
 
         self.__surface = self.__surface.crop((left, top, right, bottom))
-        
 
     def save_surface(self, filename: str) -> None:
         """Save surface to PNG file
 
         Args:
             filename (str): PNG file name
         """
```

### Comparing `processpiper-0.4.1/src/processpiper/pool.py` & `processpiper-0.4.2/src/processpiper/pool.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/processmap.py` & `processpiper-0.4.2/src/processpiper/processmap.py`

 * *Files 4% similar despite different names*

```diff
@@ -16,28 +16,33 @@
 # IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
 # FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 # AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 # LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 # OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 # SOFTWARE.
 from dataclasses import dataclass, field
+from rich.traceback import install
+from rich.console import Console
+from rich.table import Table
 import time
 from .event import *
 from .lane import Lane, ElementType, EventType
 from .pool import Pool
 from .painter import Painter
 from .shape import *
 from .title import Title
 from .footer import Footer
 from .constants import Configs
 from .helper import Helper
 from .layout import Grid
 
 import logging
 
+install()
+
 
 class UnconnectedElementException(Exception):
     pass
 
 
 class EmptyProcessMapException(Exception):
     pass
@@ -60,17 +65,18 @@
     next_shape_x: int = field(init=False, default=0)
 
     lane_y_pos: int = field(init=False, default=0)
     lane_max_width: int = field(init=False, default=0)
 
     def __post_init__(self):
         """Initialise the Process Map Class"""
+
         logging.basicConfig(
             # filename="processpiper.log",
-            level=logging.DEBUG,
+            level=logging.ERROR,
             format="%(asctime)s [%(levelname)s] : %(message)s",
             datefmt="%Y-%m-%d %H:%M:%S",
         )
         self.start_time = time.time()
         self.__painter = Painter(self.width, self.height)
         self.__set_colour_theme(self.colour_theme)
         self.__painter.set_background_colour(self.__painter.background_colour)
@@ -173,89 +179,118 @@
             if pool.name == name:
                 return pool
         return None
 
     def _set_shape_x_position(
         self,
     ):
-        Helper.printc(
-            "~~~ Setting shapes' x position...", "32", show_level="x_position"
-        )
         for lane_id, lane in self._layout_grid.get_grid_items():
-            Helper.printc(f"{lane_id=}", show_level="x_position")
+            this_lane = self._get_lane_by_id(lane_id)
+            Helper.printc(
+                f"{lane_id=}, {this_lane.name=}, {this_lane.x=}, {this_lane.y=}",
+                show_level="x_position",
+            )
             for row_number, col in lane.items():
-                Helper.printc(f"{row_number=}", end=":\n", show_level="x_position")
+                # Helper.printc(f"    {row_number=}", end=":\n", show_level="x_position")
+                table = Table(
+                    title=str(row_number),
+                    show_header=True,
+                    header_style="bold magenta",
+                    show_edge=False,
+                    title_style="bold magenta reverse",
+                )
+                table.add_column("#")
+                table.add_column("item")
+                table.add_column("x")
                 for col_idx, item in enumerate(col):
                     if item is not None:
                         item.x = (
                             Configs.SURFACE_LEFT_MARGIN
                             + Configs.POOL_TEXT_WIDTH
                             + Configs.HSPACE_BETWEEN_POOL_AND_LANE
                             + Configs.LANE_TEXT_WIDTH
                             + Configs.LANE_SHAPE_LEFT_MARGIN
                         ) + (
                             col_idx
                             * (Configs.BOX_WIDTH + Configs.HSPACE_BETWEEN_SHAPES)
                         )
-                        Helper.printc(
-                            f"    {item.name=}, {col_idx+1=}, {item.x=}",
-                            show_level="x_position",
-                        )
-                    else:
-                        Helper.printc("    {'None'}", show_level="x_position")
+                        table.add_row(str(col_idx + 1), item.name, str(item.x))
+                        # Helper.printc(
+                        #     f"      ({col_idx+1}) {item.name},      {item.x=}",
+                        #     show_level="x_position",
+                        # )
+                if Helper.show_x_position:
+                    console = Console()
+                    console.print(table)
             Helper.printc("", show_level="x_position")
 
     def _set_shape_y_position(self):
-        Helper.printc(
-            "~~~ Setting shapes' y position...", "32", show_level="y_position"
-        )
         for lane_id, lane in self._layout_grid.get_grid_items():
-            Helper.printc(f"{lane_id=}", show_level="y_position")
             this_lane = self._get_lane_by_id(lane_id)
             Helper.printc(
-                f"{this_lane.name=}, {this_lane.x=}, {this_lane.y=}",
+                f"{lane_id=}, {this_lane.name=}, {this_lane.x=}, {this_lane.y=}",
                 show_level="y_position",
             )
             for row_number, col in lane.items():
-                Helper.printc(f"{row_number=}", end=":\n", show_level="y_position")
+                table = Table(
+                    title=str(row_number),
+                    show_header=True,
+                    header_style="bold magenta",
+                    show_edge=False,
+                    title_style="bold magenta reverse",
+                )
+                table.add_column("#")
+                table.add_column("item")
+                table.add_column("x")
+                table.add_column("y")
                 row_idx = int(row_number.replace("row", "")) - 1
                 for col_idx, item in enumerate(col):
                     if item is not None:
                         item.y = (
                             this_lane.y
                             + (Configs.LANE_SHAPE_TOP_MARGIN)
                             + (
                                 row_idx
                                 * (Configs.BOX_HEIGHT + Configs.VSPACE_BETWEEN_SHAPES)
                             )
                         )
-
-                        Helper.printc(
-                            f"    {item.name=}, {row_idx=}, {col_idx+1=}, {item.x=}, {item.y=}",
-                            show_level="y_position",
+                        table.add_row(
+                            str(col_idx + 1), item.name, str(item.x), str(item.y)
                         )
+                        # Helper.printc(
+                        #     f"      ({col_idx+1}) {item.name},      {item.x=}, {item.y=}",
+                        #     show_level="y_position",
+                        # )
                         item.set_draw_position(self.__painter)
-                    else:
-                        Helper.printc("    {'None'}", show_level="y_position")
+                if Helper.show_x_position:
+                    console = Console()
+                    console.print(table)
             self.lane_max_width = max(self.lane_max_width, this_lane.width)
             Helper.printc("", show_level="y_position")
 
     def _set_draw_position(self) -> tuple:
         """Set the draw position for the process map"""
         ### Set process map title
         self._title.set_draw_position(
             Configs.SURFACE_LEFT_MARGIN, Configs.SURFACE_TOP_MARGIN, self.__painter
         )
 
         ### Put shapes into grid
+        Helper.printc(
+            "[cadet_blue][bold][  Putting shapes into grid  ]",
+            reverse=True,
+            show_level="layout_grid",
+        )
         self._layout_grid.set_grid(self._pools)
         self._layout_grid.print_grid()
 
         Helper.printc(
-            "~~~ Calculating pool and lane width and height...", show_level="pool_lane"
+            "[cadet_blue][bold][  Calculating pool and lane width and height   ]",
+            reverse=True,
+            show_level="pool_lane",
         )
         x_pos, y_pos = (
             0,
             self._title.y + self._title.height + Configs.VSPACE_BETWEEN_TITLE_AND_POOL,
         )
         for pool in self._pools:
             for lane in pool.lanes:
@@ -268,18 +303,27 @@
             first_lane_y = pool.lanes[0].y
 
             pool.set_draw_position(
                 Configs.SURFACE_LEFT_MARGIN, first_lane_y, self.__painter
             )
 
         ### Set shape x position
-        # start_shape = self._find_start_shape()
+        Helper.printc(
+            "[cadet_blue][bold][  Setting shapes X positions   ]",
+            reverse=True,
+            show_level="pool_lane",
+        )
         self._set_shape_x_position()
 
         ### Set shape y position
+        Helper.printc(
+            "[cadet_blue][bold][  Setting shapes Y positions   ]",
+            reverse=True,
+            show_level="pool_lane",
+        )
         self._set_shape_y_position()
 
         ### Set process map footer
         if self._footer is not None:
             self._footer.set_draw_position(
                 Configs.SURFACE_LEFT_MARGIN,
                 y_pos + Configs.VSPACE_BETWEEN_POOL_AND_FOOTER,
@@ -348,15 +392,15 @@
         for pool in self._pools:
             for lane in pool.lanes:
                 for index, shape in enumerate(lane.shapes):
                     self._replace_signal_element(lane, index, shape)
                     self._replace_conditional_element(lane, index, shape)
                     self._replace_message_element(lane, index, shape)
 
-        ### Set the draw position of pools, lanes, shapes and connections
+        ### Set the draw position of pools, lanes and shapes
         self._set_draw_position()
 
         ### Draw the process map
         self._title.draw()
 
         all_shapes = self._layout_grid.get_all_shapes()
 
@@ -370,23 +414,27 @@
                         lane.draw()
 
             for pool in self._pools:
                 if pool.lanes:
                     ### Then draw the shapes in the lanes
                     for lane in pool.lanes:
                         Helper.printc(
-                            f"Drawing shape for ({pool.name}, {lane.name})",
-                            34,
+                            f"Drawing shape for ({pool.name=}, {lane.name=})",
                             show_level="draw",
                         )
                         lane.draw_shape()
 
-                    ### Finally draw the connections between the shapes
-                    for lane in pool.lanes:
-                        lane.draw_connection(all_shapes)
+            for pool in self._pools:
+                ### Finally draw the connections between the shapes
+                for lane in pool.lanes:
+                    Helper.printc(
+                        f"Drawing connection for ({pool.name=}, {lane.name=})",
+                        show_level="draw_connection",
+                    )
+                    lane.draw_connection(all_shapes)
 
         if self._footer is not None:
             self._footer.draw()
 
         if self.auto_size is True:
             self.__painter.set_surface_size(self.width, self.height)
```

### Comparing `processpiper-0.4.1/src/processpiper/shape.py` & `processpiper-0.4.2/src/processpiper/shape.py`

 * *Files 3% similar despite different names*

```diff
@@ -67,14 +67,15 @@
     points: dict = field(init=False, default_factory=dict)
     incoming_points: list = field(init=False, default_factory=list)
     outgoing_points: list = field(init=False, default_factory=list)
     draw_position_set: bool = field(init=False, default=False)
     x_pos_traversed: bool = field(init=False, default=False)
     y_pos_traversed: bool = field(init=False, default=False)
     grid_traversed: bool = field(init=False, default=False)
+    connection_traversed: bool = field(init=False, default=False)
 
     connection_from: list = field(init=False, default_factory=list)
     connection_to: list = field(init=False, default_factory=list)
 
     painter: Painter = field(init=False, default=None)
 
     def connect(
@@ -120,21 +121,29 @@
         Returns:
             (tuple), (tuple): Nearest connection points between two sets of shapes
         """
         points_source = self.points
         points_target = target_shape.points
         shortest_distance: int = float("inf")
 
+        # Print just the keys of points_source
         Helper.printc(
-            f"        >>>> {points_source=}", 35, show_level="draw_connection"
+            f"        >>>> source: {points_source.keys()}", show_level="draw_connection"
         )
         Helper.printc(
-            f"        >>>> {points_target=}", 35, show_level="draw_connection"
+            f"        >>>> target: {points_target.keys()}", show_level="draw_connection"
         )
 
+        # Helper.printc(
+        #     f"        >>>> {points_source=}", show_level="draw_connection"
+        # )
+        # Helper.printc(
+        #     f"        >>>> {points_target=}", show_level="draw_connection"
+        # )
+
         nearest_points = {}
         (
             source_connection_points,
             target_connection_points,
         ) = self.get_same_lanes_connection_points(
             direction, points_source, points_target
         )
@@ -147,15 +156,17 @@
                     "source_name": source_name,
                     "source_points": source_points,
                     "target_name": target_name,
                     "target_points": target_points,
                     "distance": 0,
                 }
                 Helper.printc(
-                    f"        >>>># {nearest_points=}", 35, show_level="draw_connection"
+                    f"              > source: [green]{nearest_points['source_name']}[/green], target: [cyan]{nearest_points['target_name']}[/cyan]",
+                    35,
+                    show_level="draw_connection",
                 )
                 points = self.painter.get_points(nearest_points)
                 # loop through points, skip one point at a time
                 self.get_collision_names(
                     target_shape,
                     all_shapes,
                     collision_names,
@@ -198,15 +209,16 @@
                     }
 
         ### remove points from source and target shapes once they are used
         del points_source[nearest_points["source_name"]]
         del points_target[nearest_points["target_name"]]
 
         Helper.printc(
-            f"        ### Nearest : {nearest_points}", show_level="draw_connection"
+            f"        >>>> FINAL Nearest : [green]{nearest_points['source_name']}[/green], [cyan]{nearest_points['target_name']}[/cyan]",
+            show_level="draw_connection",
         )
         return (
             nearest_points["source_points"],
             nearest_points["source_name"],
             nearest_points["target_points"],
             nearest_points["target_name"],
         )
@@ -276,19 +288,19 @@
 
         # if uA and uB are between 0-1, lines are colliding
         if uA >= 0 and uA <= 1 and uB >= 0 and uB <= 1:
             # optionally, draw a circle where the lines meet
             intersection_x = x1 + (uA * (x2 - x1))
             intersection_y = y1 + (uA * (y2 - y1))
             ### self.painter.draw_circle(intersectionX, intersectionY, 5, "red")
-            Helper.printc(
-                f"        >>>> intersection ({intersection_x}, {intersection_y})",
-                35,
-                show_level="draw_connection",
-            )
+            # Helper.printc(
+            #     f"        >>>> intersection ({intersection_x}, {intersection_y})",
+            #     35,
+            #     show_level="draw_connection",
+            # )
 
             return True
         return False
 
     def check_shape_collision(self, line_start, line_end, shape: TShape):
         """
         This function checks if a line collides with any of the sides of a given shape.
@@ -353,25 +365,23 @@
         targeted for collision detection.
 
         Returns:
           a boolean value indicating whether a collision was found or not.
         """
         # Helper.printc(f"        >>>>@ {len(shapes)=}", 34)
         collision_found = False
+        collision_shape = ""
         for shape in shapes:
             if self == shape or target_shape == shape:
                 ...
             elif self.check_shape_collision(line_start, line_end, shape):
-                Helper.printc(
-                    f"        >>>> Colliding with [{shape.name}]",
-                    31,
-                    show_level="draw_connection",
-                )
                 collision_found = True
-        return collision_found
+                collision_shape = shape.name
+                break
+        return collision_found, collision_shape
 
     def find_nearest_points_same_pool_diff_lanes(
         self, target_shape, direction: str, all_shapes: list
     ):
         """Find nearest connection points between two sets of shapes
         where source and target shapes are in the same pool but different lanes"""
         points_source = self.points
@@ -450,80 +460,54 @@
         all_shapes,
         collision_names,
         source_name,
         target_name,
         points,
     ):
         collision_found = False
-        for i in range(0, len(points) - 1, 2):
-            Helper.printc(
-                f"        >>>> Line {i=}, {points[i]}->{points[i+1]}",
-                35,
-                show_level="draw_connection",
-            )
-            collision_found = self.check_collision(
+        for i in range(0, len(points) - 1, 1):
+            # Helper.printc(
+            #     f"        >>>> Line {i=}, {points[i]}->{points[i+1]}",
+            #     35,
+            #     show_level="draw_connection",
+            # )
+            collision_found, collision_shape = self.check_collision(
                 points[i], points[i + 1], all_shapes, target_shape
             )
             if collision_found:
                 Helper.printc(
-                    f"        >>>> COLLISION FOUND: {source_name}->{target_name}",
-                    31,
+                    "\t" * 4
+                    + f">>>> [red]***COLLISION FOUND***[/red] [orange4]{collision_shape}[/orange4]: [green]\[{source_name}][/green] -> [cyan]\[{target_name}][cyan]",
                     show_level="draw_connection",
                 )
                 break
         if collision_found:
             # Helper.printc(
             #     f"        >>>> {collision_found=}, [{source_name} {target_name})]",
             #     31,
             # )
             collision_names.append((source_name, target_name))
 
     def get_same_lanes_connection_points(self, direction, points_source, points_target):
-        # match (direction):
-        #     case "down":
-        #         source_connection_points = self.get_top_bottom_points(points_source)
-        #         target_connection_points = self.get_top_bottom_points(points_target)
-        #     case "down_right":
-        #         source_connection_points = points_source
-        #         target_connection_points = points_target
-        #     case "down_left":
-        #         source_connection_points = self.get_top_bottom_points(points_source)
-        #         target_connection_points = self.get_top_bottom_points(points_target)
-        #     case "up":
-        #         source_connection_points = self.get_top_bottom_points(points_source)
-        #         target_connection_points = self.get_top_bottom_points(points_target)
-        #     case "up_right":
-        #         source_connection_points = points_source
-        #         target_connection_points = points_target
-        #         Helper.printc(
-        #             f"        >>>>{direction=} {source_connection_points=} {target_connection_points=}",
-        #             show_level="draw_connection",
-        #         )
-
-        #     case "up_left":
-        #         source_connection_points = points_source
-        #         target_connection_points = points_target
-        #     case "left" | "right":
-        #         source_connection_points = self.get_left_right_points(points_source)
-        #         # target_connection_points = self.get_left_right_points(points_target)
-        #         target_connection_points = points_target
-
-        # if len(source_connection_points) == 0:
-        #     source_connection_points = points_source
-
-        # if len(target_connection_points) == 0:
-        #     target_connection_points = self.get_top_bottom_points(points_target)
-
         source_connection_points = points_source
         target_connection_points = points_target
 
-        Helper.printc(
-            f"        >>>>{direction=} {source_connection_points=} {target_connection_points=}",
-            show_level="draw_connection",
-        )
+        # Helper.printc(
+        #     f"        >>>> {direction=} :",
+        #     show_level="draw_connection",
+        # )
+        # Helper.printc(
+        #     f"                source_connection: {source_connection_points.keys()}",
+        #     show_level="draw_connection",
+        # )
+
+        # Helper.printc(
+        #     f"                target_connection: {target_connection_points.keys()}",
+        #     show_level="draw_connection",
+        # )
 
         return source_connection_points, target_connection_points
 
     def get_diff_lanes_connection_points(self, direction, points_source, points_target):
         match (direction):
             case "down":
                 source_connection_points = self.get_top_bottom_points(points_source)
@@ -685,58 +669,62 @@
             elif self.origin_x < target.origin_x:
                 return "up_right"
             else:
                 return "up_left"
 
     def draw_connection(self, painter: Painter, all_shapes: list):
         """Draw connection between shapes"""
+        if self.connection_traversed:
+            Helper.printc(
+                f"  [orange4]{self.name} is already traversed[/]",
+                show_level="draw_connection",
+            )
+            return
+
+        self.connection_traversed = True
         self.painter = painter
 
         Helper.printc(
-            f"Draw connection for shape: [{self.name}]",
-            36,
+            f"Draw connection for shape: [red]\[{self.name}][/red]",
             show_level="draw_connection",
         )
         if self.connection_to:
             connection_style = "solid"
             for connection in self.connection_to:
                 direction = self.get_connection_direction(connection.target)
 
                 if self.is_same_lane(self, connection.target):
                     Helper.printc(
-                        f"Same lane: Connection between [{self.name}] and [{connection.target.name}], {direction=}",
-                        31,
+                        f"  Same lane: [red]\[{self.name}] -> \[{connection.target.name}][/red], {direction=}",
                         show_level="draw_connection",
                     )
                     (
                         point_from,
                         point_face_from,
                         point_to,
                         point_face_to,
                     ) = self.find_nearest_points(
                         connection.target, direction, all_shapes
                     )
                 elif self.is_same_pool(self, connection.target):
                     Helper.printc(
-                        f"Same Pool: Connection between [{self.name}] and [{connection.target.name}], {direction=}",
-                        32,
+                        f"  Same Pool: \[{self.name}] -> \[{connection.target.name}], {direction=}",
                         show_level="draw_connection",
                     )
                     (
                         point_from,
                         point_face_from,
                         point_to,
                         point_face_to,
                     ) = self.find_nearest_points_same_pool_diff_lanes(
                         connection.target, direction, all_shapes
                     )
                 else:  ### different pool
                     Helper.printc(
-                        f"Diff Pool: Connection between [{self.name}] and [{connection.target.name}]",
-                        33,
+                        f"  Diff Pool: \[{self.name}] -> \[{connection.target.name}]",
                         show_level="draw_connection",
                     )
                     (
                         point_from,
                         point_face_from,
                         point_to,
                         point_face_to,
@@ -760,14 +748,16 @@
                     painter.connector_font_size,
                     painter.connector_font_colour,
                     painter.connector_line_width,
                     painter.connector_line_colour,
                     painter.connector_arrow_colour,
                     painter.connector_arrow_size,
                 )
+                next_shape = connection.target
+                next_shape.draw_connection(painter, all_shapes)
 
 
 @dataclass
 class Box(Shape):
     """Box shape"""
 
     def __post_init__(self):
```

### Comparing `processpiper-0.4.1/src/processpiper/text2diagram.py` & `processpiper-0.4.2/src/processpiper/text2diagram.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/title.py` & `processpiper-0.4.2/src/processpiper/title.py`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/processpiper/version.py` & `processpiper-0.4.2/src/processpiper/version.py`

 * *Files 14% similar despite different names*

```diff
@@ -17,8 +17,8 @@
 # FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 # AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 # LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 # OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 # SOFTWARE.
 
 """Version information for processpiper."""
-__version__ = "v0.4.1"
+__version__ = "v0.4.2"
```

### Comparing `processpiper-0.4.1/src/processpiper.egg-info/SOURCES.txt` & `processpiper-0.4.2/src/processpiper.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `processpiper-0.4.1/src/tests/github_action_test.py` & `processpiper-0.4.2/src/tests/github_action_test.py`

 * *Files identical despite different names*

