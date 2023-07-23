# Comparing `tmp/ephemeral_sh-0.3.1-py3-none-any.whl.zip` & `tmp/ephemeral_sh-0.3.2-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,11 +1,11 @@
-Zip file size: 4310 bytes, number of entries: 9
--rw-r--r--  2.0 unx       22 b- defN 23-Jul-23 18:42 ephemeral/__init__.py
--rw-r--r--  2.0 unx     2431 b- defN 23-Jul-23 18:42 ephemeral/cli.py
--rw-r--r--  2.0 unx     1936 b- defN 23-Jul-23 18:42 ephemeral/model.py
+Zip file size: 4478 bytes, number of entries: 9
+-rw-r--r--  2.0 unx       22 b- defN 23-Jul-23 18:45 ephemeral/__init__.py
+-rw-r--r--  2.0 unx     3006 b- defN 23-Jul-23 18:56 ephemeral/cli.py
+-rw-r--r--  2.0 unx     2022 b- defN 23-Jul-23 18:48 ephemeral/model.py
 -rw-r--r--  2.0 unx     1045 b- defN 23-Jul-23 18:42 ephemeral/view.py
--rw-r--r--  2.0 unx     1135 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/WHEEL
--rw-r--r--  2.0 unx       48 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/entry_points.txt
--rw-r--r--  2.0 unx       10 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      716 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/RECORD
-9 files, 7435 bytes uncompressed, 3074 bytes compressed:  58.7%
+-rw-r--r--  2.0 unx     1135 b- defN 23-Jul-23 19:03 ephemeral_sh-0.3.2.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 19:03 ephemeral_sh-0.3.2.dist-info/WHEEL
+-rw-r--r--  2.0 unx       48 b- defN 23-Jul-23 19:03 ephemeral_sh-0.3.2.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx       10 b- defN 23-Jul-23 19:03 ephemeral_sh-0.3.2.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      716 b- defN 23-Jul-23 19:03 ephemeral_sh-0.3.2.dist-info/RECORD
+9 files, 8096 bytes uncompressed, 3242 bytes compressed:  60.0%
```

## zipnote {}

```diff
@@ -6,23 +6,23 @@
 
 Filename: ephemeral/model.py
 Comment: 
 
 Filename: ephemeral/view.py
 Comment: 
 
-Filename: ephemeral_sh-0.3.1.dist-info/METADATA
+Filename: ephemeral_sh-0.3.2.dist-info/METADATA
 Comment: 
 
-Filename: ephemeral_sh-0.3.1.dist-info/WHEEL
+Filename: ephemeral_sh-0.3.2.dist-info/WHEEL
 Comment: 
 
-Filename: ephemeral_sh-0.3.1.dist-info/entry_points.txt
+Filename: ephemeral_sh-0.3.2.dist-info/entry_points.txt
 Comment: 
 
-Filename: ephemeral_sh-0.3.1.dist-info/top_level.txt
+Filename: ephemeral_sh-0.3.2.dist-info/top_level.txt
 Comment: 
 
-Filename: ephemeral_sh-0.3.1.dist-info/RECORD
+Filename: ephemeral_sh-0.3.2.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## ephemeral/__init__.py

```diff
@@ -1 +1 @@
-__version__ = "0.3.1"
+__version__ = "0.3.2"
```

## ephemeral/cli.py

```diff
@@ -64,21 +64,30 @@
 @app.command()
 def history() -> None:
     """display record of completed tasks"""
     show_history(tracker)
 
 
 @app.command()
-def clear() -> None:
+def clear(
+    all: Annotated[bool, typer.Option("--all", help="clear all information")] = True,
+    task: Annotated[bool, typer.Option("--task", help="clear the current task")] = False,
+    history: Annotated[bool, typer.Option("--history", help="clear the saved history")] = False,
+) -> None:
     """delete all persisted state"""
-    show_current_task(tracker)
-    print(
-        ":exclamation-emoji:  [bold red]You are about to reset ephemeral to a clean slate[/bold red]"
-    )
-    _ = typer.confirm("    Would you like to continue?", abort=True)
-    tracker.clear()
+    if all and not task and not history:
+        print(
+            ":exclamation-emoji:  [bold red]You are about to reset ephemeral to a clean slate[/bold red]"
+        )
+        _ = typer.confirm("    Would you like to continue?", abort=True)
+        task = history = True
+    if task and tracker.current_task is not None:
+        print("    Clearing the current task...")
+    if history and tracker.history:
+        print(f"    Clearing the saved history ({len(tracker.history)} tasks)...")
+    tracker.clear(task=task, history=history)
     print("\n:sparkles-emoji:  [bold blue]Ephemeral has forgotten[/bold blue]  :sparkles-emoji:\n")
     tracker.save()
 
 
 if __name__ == "__main__":
     app()
```

## ephemeral/model.py

```diff
@@ -51,10 +51,12 @@
         # add current task to history
         if self.current_task is not None:
             self.current_task.end_ts = int(datetime.datetime.now(datetime.timezone.utc).timestamp())
             self.history.append(self.current_task)
         # update current task
         self.current_task = new_task
 
-    def clear(self) -> None:
-        self.current_task = None
-        self.history = []
+    def clear(self, task: bool = True, history: bool = True) -> None:
+        if task:
+            self.current_task = None
+        if history:
+            self.history = []
```

## Comparing `ephemeral_sh-0.3.1.dist-info/METADATA` & `ephemeral_sh-0.3.2.dist-info/METADATA`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ephemeral-sh
-Version: 0.3.1
+Version: 0.3.2
 Summary: A one-task tracker in your terminal with a forgetful history
 Author-email: Mike Moran <mike@mkmrn.dev>
 Project-URL: GitLab, https://gitlab.com/mmoran0032/ephemeral-sh
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Requires-Dist: rich
 Requires-Dist: typer[all]
```

## Comparing `ephemeral_sh-0.3.1.dist-info/RECORD` & `ephemeral_sh-0.3.2.dist-info/RECORD`

 * *Files 15% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-ephemeral/__init__.py,sha256=r4xAFihOf72W9TD-lpMi6ntWSTKTP2SlzKP1ytkjRbI,22
-ephemeral/cli.py,sha256=V16JVG1nDEwmuWCr2GuQebEEWHWl-UewFREyYF8AHvI,2431
-ephemeral/model.py,sha256=xJgN5kWnjdaSNfkqj3AZZ4ga5CKHTll3OJOHPgtCK7w,1936
+ephemeral/__init__.py,sha256=vNiWJ14r_cw5t_7UDqDQIVZvladKFGyHH2avsLpN7Vg,22
+ephemeral/cli.py,sha256=2pfp-YQ7-Kj_NrCc8ASvt2NnLoD4egsJ1KqOlrMb1wo,3006
+ephemeral/model.py,sha256=hAWwthFMKIH2nJBHuCw9ZIOck1q8MngiqHb0zjnpEFE,2022
 ephemeral/view.py,sha256=ctVUFB5_DxSQD4pG9Wvp0ql4UhWied5DbIi83B6HgT8,1045
-ephemeral_sh-0.3.1.dist-info/METADATA,sha256=0bP1ZyVAV3rOhXrDNBU2DbB_RswMJ6LMa8HQps2gmvw,1135
-ephemeral_sh-0.3.1.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-ephemeral_sh-0.3.1.dist-info/entry_points.txt,sha256=tsGPrUEKKKCIkq-fyBaLR0A38uz6dsFvARnwCOMKc_s,48
-ephemeral_sh-0.3.1.dist-info/top_level.txt,sha256=co9Y91lorce33MgIVO2WjvIU2eehcnMreojOFFt4uM8,10
-ephemeral_sh-0.3.1.dist-info/RECORD,,
+ephemeral_sh-0.3.2.dist-info/METADATA,sha256=d84kHhAQjHCsCmqAknHh3LlnAkaWmDEzuQx1TP6SzSo,1135
+ephemeral_sh-0.3.2.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+ephemeral_sh-0.3.2.dist-info/entry_points.txt,sha256=tsGPrUEKKKCIkq-fyBaLR0A38uz6dsFvARnwCOMKc_s,48
+ephemeral_sh-0.3.2.dist-info/top_level.txt,sha256=co9Y91lorce33MgIVO2WjvIU2eehcnMreojOFFt4uM8,10
+ephemeral_sh-0.3.2.dist-info/RECORD,,
```

