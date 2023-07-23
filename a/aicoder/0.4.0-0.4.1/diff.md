# Comparing `tmp/aicoder-0.4.0-py3-none-any.whl.zip` & `tmp/aicoder-0.4.1-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,14 +1,14 @@
-Zip file size: 22216 bytes, number of entries: 12
+Zip file size: 22337 bytes, number of entries: 12
 -rw-r--r--  2.0 unx    10950 b- defN 23-Jul-20 09:01 aicoder/AICoder.py
--rw-r--r--  2.0 unx     9432 b- defN 23-Jul-20 09:01 aicoder/AICoderFull.py
+-rw-r--r--  2.0 unx     9533 b- defN 23-Jul-23 15:01 aicoder/AICoderFull.py
 -rw-r--r--  2.0 unx     7157 b- defN 23-Jul-20 09:32 aicoder/AICoderPartial.py
--rw-r--r--  2.0 unx     3777 b- defN 23-Jul-19 22:48 aicoder/AICoderPrompts.py
+-rw-r--r--  2.0 unx     3961 b- defN 23-Jul-23 15:01 aicoder/AICoderPrompts.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jun-29 11:14 aicoder/__init__.py
 -rw-r--r--  2.0 unx    16651 b- defN 23-Jul-20 09:31 aicoder/main.py
--rw-r--r--  2.0 unx    18809 b- defN 23-Jul-20 09:45 aicoder-0.4.0.dist-info/LICENSE
--rw-r--r--  2.0 unx      473 b- defN 23-Jul-20 09:45 aicoder-0.4.0.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-20 09:45 aicoder-0.4.0.dist-info/WHEEL
--rw-r--r--  2.0 unx       46 b- defN 23-Jul-20 09:45 aicoder-0.4.0.dist-info/entry_points.txt
--rw-r--r--  2.0 unx        8 b- defN 23-Jul-20 09:45 aicoder-0.4.0.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      945 b- defN 23-Jul-20 09:45 aicoder-0.4.0.dist-info/RECORD
-12 files, 68340 bytes uncompressed, 20636 bytes compressed:  69.8%
+-rw-r--r--  2.0 unx    18809 b- defN 23-Jul-23 15:05 aicoder-0.4.1.dist-info/LICENSE
+-rw-r--r--  2.0 unx      473 b- defN 23-Jul-23 15:05 aicoder-0.4.1.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 15:05 aicoder-0.4.1.dist-info/WHEEL
+-rw-r--r--  2.0 unx       46 b- defN 23-Jul-23 15:05 aicoder-0.4.1.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 15:05 aicoder-0.4.1.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      945 b- defN 23-Jul-23 15:05 aicoder-0.4.1.dist-info/RECORD
+12 files, 68625 bytes uncompressed, 20757 bytes compressed:  69.8%
```

## zipnote {}

```diff
@@ -12,26 +12,26 @@
 
 Filename: aicoder/__init__.py
 Comment: 
 
 Filename: aicoder/main.py
 Comment: 
 
-Filename: aicoder-0.4.0.dist-info/LICENSE
+Filename: aicoder-0.4.1.dist-info/LICENSE
 Comment: 
 
-Filename: aicoder-0.4.0.dist-info/METADATA
+Filename: aicoder-0.4.1.dist-info/METADATA
 Comment: 
 
-Filename: aicoder-0.4.0.dist-info/WHEEL
+Filename: aicoder-0.4.1.dist-info/WHEEL
 Comment: 
 
-Filename: aicoder-0.4.0.dist-info/entry_points.txt
+Filename: aicoder-0.4.1.dist-info/entry_points.txt
 Comment: 
 
-Filename: aicoder-0.4.0.dist-info/top_level.txt
+Filename: aicoder-0.4.1.dist-info/top_level.txt
 Comment: 
 
-Filename: aicoder-0.4.0.dist-info/RECORD
+Filename: aicoder-0.4.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## aicoder/AICoderFull.py

```diff
@@ -165,19 +165,19 @@
 
         # Get files to generate
         files_to_generate = self.get_files_to_generate()
 
         # Order files to generated from less amount of dependencies to more
         files_to_generate = sorted(files_to_generate, key=lambda x: len(x["dependencies"]))
         
-        # Generate main file
-        files_to_generate = self.generate_main_file(files_to_generate)
+        # Generate main(s) file(s) (There could be several main files)
+        files_to_generate, main_count = self.generate_main_file(files_to_generate)
         
         # Initialize a ThreadPoolExecutor and a progress bar
-        with tqdm(total=len(files_to_generate[1:]), desc="Generating files", unit="file") as pbar:
+        with tqdm(total=len(files_to_generate[main_count:]), desc="Generating files", unit="file") as pbar:
             sleep(0.1) #Allow the progress bar to be displayed
             with ThreadPoolExecutor(max_workers=3) as executor: # 3 is ok, don't oversaturate the server
                 # Submit tasks to the executor
                 futures = {executor.submit(self.generate_file, file, files_to_generate): file for file in files_to_generate[1:]}
 
                 # As the futures complete, update the progress bar
                 for future in concurrent.futures.as_completed(futures):
@@ -197,21 +197,21 @@
         self.try_to_compile()
 
         # Try to run the program
         self.try_to_run()
 
     def generate_main_file(self, files_to_generate):
         # Generate the main file first
-        main_file_found = False
+        main_count = 0
         for file in files_to_generate:
             if "/main." in file["path"].lower():
                 logger.info("Generating main file...")
                 main_file_content = self.generate_file(file, files_to_generate)
                 files_to_generate.remove(file)
                 file["description"] = file["description"] + "\nMain file content:\n" + main_file_content
-                files_to_generate.insert(0, file)
-                main_file_found = True
-                break
+                files_to_generate.insert(main_count, file)
+                main_count += 1
+                # Do not break, there could be seveal mains
         
-        if not main_file_found:
+        if main_count > 0:
             raise Exception("No main file found")
-        return files_to_generate
+        return files_to_generate, main_count
```

## aicoder/AICoderPrompts.py

```diff
@@ -14,14 +14,16 @@
     {
         "path": "./generated/main.py",
         "description": "<This is a description of the content ./generated/main.py>",
         "dependencies": ["./generated/file2.h", "./generated/file3.py"]
     },
 ]
 
+In every file that isn't a main file, add in the depedencies the path to the main file that is relevant for it (notice that several main files could be needed if the program is big).
+
 If needed don't forget headers '.h' and  implementations '.c, .cpp, .m'...
 The response must be only a valid JSON with the structure above, don't add anything else."""
 
 
 GET_FILE_CONTENTS = """These are the files we are generating for the program:\n
 __FILES_JSON__
```

## Comparing `aicoder-0.4.0.dist-info/LICENSE` & `aicoder-0.4.1.dist-info/LICENSE`

 * *Files identical despite different names*

