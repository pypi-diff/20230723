# Comparing `tmp/ephemeral_sh-0.2.0-py3-none-any.whl.zip` & `tmp/ephemeral_sh-0.2.1-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,10 +1,10 @@
-Zip file size: 3266 bytes, number of entries: 8
--rw-r--r--  2.0 unx       22 b- defN 23-Jul-23 16:10 ephemeral/__init__.py
--rw-r--r--  2.0 unx     1675 b- defN 23-Jul-23 16:06 ephemeral/cli.py
+Zip file size: 3263 bytes, number of entries: 8
+-rw-r--r--  2.0 unx       22 b- defN 23-Jul-23 16:36 ephemeral/__init__.py
+-rw-r--r--  2.0 unx     1685 b- defN 23-Jul-23 16:36 ephemeral/cli.py
 -rw-r--r--  2.0 unx     1296 b- defN 23-Jul-23 15:59 ephemeral/model.py
--rw-r--r--  2.0 unx      884 b- defN 23-Jul-23 16:11 ephemeral_sh-0.2.0.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 16:11 ephemeral_sh-0.2.0.dist-info/WHEEL
--rw-r--r--  2.0 unx       48 b- defN 23-Jul-23 16:11 ephemeral_sh-0.2.0.dist-info/entry_points.txt
--rw-r--r--  2.0 unx       10 b- defN 23-Jul-23 16:11 ephemeral_sh-0.2.0.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      641 b- defN 23-Jul-23 16:11 ephemeral_sh-0.2.0.dist-info/RECORD
-8 files, 4668 bytes uncompressed, 2140 bytes compressed:  54.2%
+-rw-r--r--  2.0 unx      884 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/WHEEL
+-rw-r--r--  2.0 unx       48 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx       10 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      641 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/RECORD
+8 files, 4678 bytes uncompressed, 2137 bytes compressed:  54.3%
```

## zipnote {}

```diff
@@ -3,23 +3,23 @@
 
 Filename: ephemeral/cli.py
 Comment: 
 
 Filename: ephemeral/model.py
 Comment: 
 
-Filename: ephemeral_sh-0.2.0.dist-info/METADATA
+Filename: ephemeral_sh-0.2.1.dist-info/METADATA
 Comment: 
 
-Filename: ephemeral_sh-0.2.0.dist-info/WHEEL
+Filename: ephemeral_sh-0.2.1.dist-info/WHEEL
 Comment: 
 
-Filename: ephemeral_sh-0.2.0.dist-info/entry_points.txt
+Filename: ephemeral_sh-0.2.1.dist-info/entry_points.txt
 Comment: 
 
-Filename: ephemeral_sh-0.2.0.dist-info/top_level.txt
+Filename: ephemeral_sh-0.2.1.dist-info/top_level.txt
 Comment: 
 
-Filename: ephemeral_sh-0.2.0.dist-info/RECORD
+Filename: ephemeral_sh-0.2.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## ephemeral/__init__.py

```diff
@@ -1 +1 @@
-__version__ = "0.2.0"
+__version__ = "0.2.1"
```

## ephemeral/cli.py

```diff
@@ -24,23 +24,23 @@
 
 
 @app.command()
 def track() -> None:
     """start tracking a new task, or replace your current task"""
     if tracker.task is not None:
         show_current_task()
-        _ = typer.confirm("Would you like to clear your current task?", abort=True)
-    new_task = typer.prompt("What would you like to track?")
+        _ = typer.confirm("    Would you like to clear your current task?", abort=True)
+    new_task = typer.prompt("    What would you like to track?")
     tracker.update(new_task)
-    print(f":heavy_check_mark-emoji: Now tracking [bold blue]{new_task}[/bold blue]...")
+    print(f":heavy_check_mark-emoji:   Now tracking [bold blue]{new_task}[/bold blue]...")
 
 
 @app.command()
 def clear() -> None:
-    """delete all persisted satet"""
+    """delete all persisted state"""
     show_current_task()
     print(
         ":exclamation-emoji:  [bold red]You are about to reset ephemeral to a clean slate[/bold red]"
     )
     _ = typer.confirm("    Would you like to continue?", abort=True)
     tracker.delete()
     print("\n:sparkles-emoji:  [bold blue]Ephemeral has forgotten[/bold blue]  :sparkles-emoji:\n")
```

## Comparing `ephemeral_sh-0.2.0.dist-info/METADATA` & `ephemeral_sh-0.2.1.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ephemeral-sh
-Version: 0.2.0
+Version: 0.2.1
 Summary: A one-task tracker in your terminal with a forgetful history
 Author-email: Mike Moran <mike@mkmrn.dev>
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Requires-Dist: rich
 Requires-Dist: typer[all]
 Provides-Extra: dev
```

