# Comparing `tmp/aicoder-0.4.3-py3-none-any.whl.zip` & `tmp/aicoder-0.4.4-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,14 +1,14 @@
-Zip file size: 22337 bytes, number of entries: 12
+Zip file size: 22345 bytes, number of entries: 12
 -rw-r--r--  2.0 unx    10951 b- defN 23-Jul-23 15:07 aicoder/AICoder.py
--rw-r--r--  2.0 unx     9535 b- defN 23-Jul-23 15:06 aicoder/AICoderFull.py
+-rw-r--r--  2.0 unx     9562 b- defN 23-Jul-23 15:26 aicoder/AICoderFull.py
 -rw-r--r--  2.0 unx     7159 b- defN 23-Jul-23 15:06 aicoder/AICoderPartial.py
 -rw-r--r--  2.0 unx     3961 b- defN 23-Jul-23 15:01 aicoder/AICoderPrompts.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jun-29 11:14 aicoder/__init__.py
 -rw-r--r--  2.0 unx    16637 b- defN 23-Jul-23 15:06 aicoder/main.py
--rw-r--r--  2.0 unx    18809 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/LICENSE
--rw-r--r--  2.0 unx      473 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/WHEEL
--rw-r--r--  2.0 unx       46 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/entry_points.txt
--rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      945 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/RECORD
-12 files, 68616 bytes uncompressed, 20757 bytes compressed:  69.7%
+-rw-r--r--  2.0 unx    18809 b- defN 23-Jul-23 15:27 aicoder-0.4.4.dist-info/LICENSE
+-rw-r--r--  2.0 unx      473 b- defN 23-Jul-23 15:27 aicoder-0.4.4.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 15:27 aicoder-0.4.4.dist-info/WHEEL
+-rw-r--r--  2.0 unx       46 b- defN 23-Jul-23 15:27 aicoder-0.4.4.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 15:27 aicoder-0.4.4.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      945 b- defN 23-Jul-23 15:27 aicoder-0.4.4.dist-info/RECORD
+12 files, 68643 bytes uncompressed, 20765 bytes compressed:  69.7%
```

## zipnote {}

```diff
@@ -12,26 +12,26 @@
 
 Filename: aicoder/__init__.py
 Comment: 
 
 Filename: aicoder/main.py
 Comment: 
 
-Filename: aicoder-0.4.3.dist-info/LICENSE
+Filename: aicoder-0.4.4.dist-info/LICENSE
 Comment: 
 
-Filename: aicoder-0.4.3.dist-info/METADATA
+Filename: aicoder-0.4.4.dist-info/METADATA
 Comment: 
 
-Filename: aicoder-0.4.3.dist-info/WHEEL
+Filename: aicoder-0.4.4.dist-info/WHEEL
 Comment: 
 
-Filename: aicoder-0.4.3.dist-info/entry_points.txt
+Filename: aicoder-0.4.4.dist-info/entry_points.txt
 Comment: 
 
-Filename: aicoder-0.4.3.dist-info/top_level.txt
+Filename: aicoder-0.4.4.dist-info/top_level.txt
 Comment: 
 
-Filename: aicoder-0.4.3.dist-info/RECORD
+Filename: aicoder-0.4.4.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## aicoder/AICoderFull.py

```diff
@@ -114,15 +114,15 @@
         # Check for todos
         if self.check_for_todos(file_content):
             logger.warning(f"Found TODOs in {file_path}")
             return self.generate_file(file=file, files_to_generate=files_to_generate)
 
         # Ask if main is as expected
         if is_main:
-            print("This is the main file content:\n", file_content)
+            print(f"This is the main file content for {file_path}:\n", file_content)
             print("")
             print("Is this ok or where you expecting something different? (Y/n)")
             user_input = input()
             if user_input.lower() in ["no", "n"]:
                 print("I'll try to generate the files again... Tell me the problem in one line:")
                 extra_content = "\n\nLast time I asked your response was: " + file_content
                 extra_content += "\n\n" + input()
@@ -208,10 +208,11 @@
                 main_file_content = self.generate_file(file, files_to_generate)
                 files_to_generate.remove(file)
                 file["description"] = file["description"] + "\nMain file content:\n" + main_file_content
                 files_to_generate.insert(main_count, file)
                 main_count += 1
                 # Do not break, there could be seveal mains
         
-        if main_count > 0:
+        if main_count <= 0:
             raise Exception("No main file found")
+        
         return files_to_generate, main_count
```

## Comparing `aicoder-0.4.3.dist-info/LICENSE` & `aicoder-0.4.4.dist-info/LICENSE`

 * *Files identical despite different names*

