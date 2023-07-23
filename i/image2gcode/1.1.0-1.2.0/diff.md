# Comparing `tmp/image2gcode-1.1.0.tar.gz` & `tmp/image2gcode-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "image2gcode-1.1.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "image2gcode-1.2.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `image2gcode-1.1.0.tar` & `image2gcode-1.2.0.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0     1085 2023-06-10 14:42:21.317017 image2gcode-1.1.0/LICENSE
--rw-r--r--   0        0        0     2446 2023-06-10 14:30:07.661442 image2gcode-1.1.0/README.md
--rwxr-xr-x   0        0        0     7812 2023-06-10 14:45:28.000966 image2gcode-1.1.0/image2gcode.py
--rw-r--r--   0        0        0      652 2023-06-10 14:43:51.248920 image2gcode-1.1.0/pyproject.toml
--rw-r--r--   0        0        0     2929 1970-01-01 00:00:00.000000 image2gcode-1.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1085 2023-06-10 14:42:21.317017 image2gcode-1.2.0/LICENSE
+-rw-r--r--   0        0        0     2446 2023-06-11 11:13:43.786854 image2gcode-1.2.0/README.md
+-rwxr-xr-x   0        0        0     7910 2023-07-23 10:46:26.556359 image2gcode-1.2.0/image2gcode.py
+-rw-r--r--   0        0        0      652 2023-06-10 14:43:51.248920 image2gcode-1.2.0/pyproject.toml
+-rw-r--r--   0        0        0     2929 1970-01-01 00:00:00.000000 image2gcode-1.2.0/PKG-INFO
```

### Comparing `image2gcode-1.1.0/LICENSE` & `image2gcode-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `image2gcode-1.1.0/README.md` & `image2gcode-1.2.0/README.md`

 * *Files identical despite different names*

### Comparing `image2gcode-1.1.0/image2gcode.py` & `image2gcode-1.2.0/image2gcode.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python3
 """
 image2gcode: convert an image to gcode.
 """
-__version__ = "1.1.0"
+__version__ = "1.2.0"
 
 import sys
 import argparse
 from argparse import Namespace
 from datetime import datetime
 from PIL import Image
 import numpy as np
@@ -172,27 +172,28 @@
             print("For validation package gcode2image.py must be installed (in $PATH or python install path)")
         else:
             print("For validation a 'gcode filename' argument must be set.")
             parser.print_usage(sys.stderr)
         sys.exit(1)
 
     # load and convert image to B&W
-    narr = loadImage(args.image.name,args.showimage)
+    # flip image updown because Gcode and raster image coordinate system differ
+    narr = np.flipud(loadImage(args.image.name,args.showimage))
 
     print('Area: ' + str(round(narr.shape[1] * args.pixelsize,2)) + "mm x " + str(round(narr.shape[0] * args.pixelsize,2)) + "mm (XY)")
     print('> pixelsize', args.pixelsize, 'mm^2, speed', args.speed, 'mm/min, maxpower ' + str(args.maxpower) + ', offset', args.offset)
 
     # emit gcode for image
     print(image2gcode(narr, args), file=args.gcode)
 
     if args.validate:
         args.gcode.close()
         with open(args.gcode.name, "r") as fgcode:
-            #img = gcode2image(fgcode, narr.shape, args)
-            img = gcode2image(Namespace(gcode = fgcode, offset = False, showG0 = True, grid = False))
+            # flip to raster image coordinate system
+            img = np.flipud(gcode2image(Namespace(gcode = fgcode, offset = False, showG0 = True, grid = False)))
 
             # convert to image
             img = Image.fromarray(img)
 
             # show image
             img.show()
             # write image file (png)
```

### Comparing `image2gcode-1.1.0/pyproject.toml` & `image2gcode-1.2.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `image2gcode-1.1.0/PKG-INFO` & `image2gcode-1.2.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: image2gcode
-Version: 1.1.0
+Version: 1.2.0
 Summary: image2gcode: convert an image to gcode.
 Keywords: engraving,laser,image,laser engraving,PWM,gcode
 Author-email: Johannes Noordanus <mailjohannes.mailnoordanus@gmail.com>
 Requires-Python: >=3.10.6
 Description-Content-Type: text/markdown
 Classifier: License :: OSI Approved :: MIT License
 Requires-Dist: numpy >= 1.24.3
```

