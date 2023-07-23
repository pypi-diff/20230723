# Comparing `tmp/ephemeral_sh-0.2.1-py3-none-any.whl.zip` & `tmp/ephemeral_sh-0.3.1-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,10 +1,11 @@
-Zip file size: 3263 bytes, number of entries: 8
--rw-r--r--  2.0 unx       22 b- defN 23-Jul-23 16:36 ephemeral/__init__.py
--rw-r--r--  2.0 unx     1685 b- defN 23-Jul-23 16:36 ephemeral/cli.py
--rw-r--r--  2.0 unx     1296 b- defN 23-Jul-23 15:59 ephemeral/model.py
--rw-r--r--  2.0 unx      884 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/WHEEL
--rw-r--r--  2.0 unx       48 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/entry_points.txt
--rw-r--r--  2.0 unx       10 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      641 b- defN 23-Jul-23 16:37 ephemeral_sh-0.2.1.dist-info/RECORD
-8 files, 4678 bytes uncompressed, 2137 bytes compressed:  54.3%
+Zip file size: 4310 bytes, number of entries: 9
+-rw-r--r--  2.0 unx       22 b- defN 23-Jul-23 18:42 ephemeral/__init__.py
+-rw-r--r--  2.0 unx     2431 b- defN 23-Jul-23 18:42 ephemeral/cli.py
+-rw-r--r--  2.0 unx     1936 b- defN 23-Jul-23 18:42 ephemeral/model.py
+-rw-r--r--  2.0 unx     1045 b- defN 23-Jul-23 18:42 ephemeral/view.py
+-rw-r--r--  2.0 unx     1135 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/WHEEL
+-rw-r--r--  2.0 unx       48 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx       10 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      716 b- defN 23-Jul-23 18:42 ephemeral_sh-0.3.1.dist-info/RECORD
+9 files, 7435 bytes uncompressed, 3074 bytes compressed:  58.7%
```

## zipnote {}

```diff
@@ -3,23 +3,26 @@
 
 Filename: ephemeral/cli.py
 Comment: 
 
 Filename: ephemeral/model.py
 Comment: 
 
-Filename: ephemeral_sh-0.2.1.dist-info/METADATA
+Filename: ephemeral/view.py
 Comment: 
 
-Filename: ephemeral_sh-0.2.1.dist-info/WHEEL
+Filename: ephemeral_sh-0.3.1.dist-info/METADATA
 Comment: 
 
-Filename: ephemeral_sh-0.2.1.dist-info/entry_points.txt
+Filename: ephemeral_sh-0.3.1.dist-info/WHEEL
 Comment: 
 
-Filename: ephemeral_sh-0.2.1.dist-info/top_level.txt
+Filename: ephemeral_sh-0.3.1.dist-info/entry_points.txt
 Comment: 
 
-Filename: ephemeral_sh-0.2.1.dist-info/RECORD
+Filename: ephemeral_sh-0.3.1.dist-info/top_level.txt
+Comment: 
+
+Filename: ephemeral_sh-0.3.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## ephemeral/__init__.py

```diff
@@ -1 +1 @@
-__version__ = "0.2.1"
+__version__ = "0.3.1"
```

## ephemeral/cli.py

```diff
@@ -1,57 +1,84 @@
+from typing import Optional
+
 from rich import print
 import typer
+from typing_extensions import Annotated
 
-from ephemeral.model import Task
+from ephemeral import __version__
+from ephemeral.model import Task, Tracker
+from ephemeral.view import show_current_task, show_history
 
 app = typer.Typer()
-tracker = Task.load()
+tracker = Tracker.load()
+
+
+def version_callback(value: bool):
+    if value:
+        print(f"[white not bold]{__package__} {__version__}[/white not bold]")
+        raise typer.Exit()
 
 
 @app.callback(invoke_without_command=True)
-def main(ctx: typer.Context) -> None:
+def main(
+    ctx: typer.Context,
+    version: Annotated[
+        Optional[bool],
+        typer.Option("--version", callback=version_callback, is_eager=True),
+    ] = None,
+) -> None:
     """A simple task tracker with a forgetful history"""
     if ctx.invoked_subcommand is not None:
         return
 
-    if tracker.task is None:
-        print(
-            ":x-emoji:  [bold red]No active task found![/bold red]",
-            ":information-emoji:   Start tracking with [bold green]ephemeral track[/bold green]",
-            sep="\n",
-        )
-        return
-    show_current_task()
+    show_current_task(tracker)
+    if tracker.current_task is None:
+        print(":information-emoji:   Start tracking with [bold green]ephemeral track[/bold green]")
 
 
 @app.command()
 def track() -> None:
     """start tracking a new task, or replace your current task"""
-    if tracker.task is not None:
-        show_current_task()
-        _ = typer.confirm("    Would you like to clear your current task?", abort=True)
+    if tracker.current_task is not None:
+        show_current_task(tracker)
+        _ = typer.confirm("    Would you like to complete your current task?", abort=True)
+        complete()
+
+    _ = typer.confirm("    Would you like to start tracking a new task?")
     new_task = typer.prompt("    What would you like to track?")
-    tracker.update(new_task)
+    tracker.update(Task(new_task))
     print(f":heavy_check_mark-emoji:   Now tracking [bold blue]{new_task}[/bold blue]...")
+    tracker.save()
+
+
+@app.command()
+def complete() -> None:
+    """finish a task and save it in the history"""
+    if tracker.current_task is not None:
+        print(
+            f":tada-emoji:   Completing [bold blue]{tracker.current_task.task}[/bold blue]  :tada-emoji:"
+        )
+    tracker.update(new_task=None)
+    tracker.save()
+
+
+@app.command()
+def history() -> None:
+    """display record of completed tasks"""
+    show_history(tracker)
 
 
 @app.command()
 def clear() -> None:
     """delete all persisted state"""
-    show_current_task()
+    show_current_task(tracker)
     print(
         ":exclamation-emoji:  [bold red]You are about to reset ephemeral to a clean slate[/bold red]"
     )
     _ = typer.confirm("    Would you like to continue?", abort=True)
-    tracker.delete()
+    tracker.clear()
     print("\n:sparkles-emoji:  [bold blue]Ephemeral has forgotten[/bold blue]  :sparkles-emoji:\n")
-
-
-def show_current_task() -> None:
-    if tracker.task is not None:
-        print(
-            f":heavy_check_mark-emoji:   {tracker.task} [bold black](since {tracker.dt:%Y-%m-%d})[/bold black]",
-        )
+    tracker.save()
 
 
 if __name__ == "__main__":
     app()
```

## ephemeral/model.py

```diff
@@ -1,48 +1,60 @@
-from dataclasses import dataclass, field
+from dataclasses import asdict, dataclass, field
 import datetime
 import json
 from pathlib import Path
-
-DATA_FILE = Path.home() / ".config" / "ephemeral"
+from typing import List
+import uuid
 
 
 @dataclass
 class Task:
-    ts: int = int(datetime.datetime.now(datetime.timezone.utc).timestamp())
-    task: str | None = None
-    dt: datetime.datetime = field(init=False)
-
-    def __post_init__(self):
-        self.dt = datetime.datetime.fromtimestamp(self.ts)
-
-    @classmethod
-    def load(self) -> "Task":
-        if not DATA_FILE.is_file():
-            return Task()
-        data = json.loads(DATA_FILE.read_text())
-        return Task(**data)
+    task: str
+    start_ts: int = int(datetime.datetime.now(datetime.timezone.utc).timestamp())
+    end_ts: int | None = None
+    id: uuid.UUID = field(default_factory=uuid.uuid4)
 
     @property
     def json(self) -> dict:
-        return {"ts": self.ts, "task": self.task}
+        data = asdict(self)
+        data["id"] = str(data["id"])
+        return data
 
-    def save(self) -> None:
-        DATA_FILE.write_text(json.dumps(self.json))
 
-    def read(self) -> "Task":
-        try:
-            data = json.loads(DATA_FILE.read_text())
-            self.ts = data.get("ts", 0)
-            self.task = data.get("task", "")
-        except FileNotFoundError:
-            self.ts = 0
-        return self
-
-    def update(self, new_task: str) -> None:
-        self.task = new_task
-        self.ts = int(datetime.datetime.now(datetime.timezone.utc).timestamp())
-        self.save()
-
-    def delete(self) -> None:
-        DATA_FILE.write_text("{}")
-        self.task = None
+class Tracker:
+    def __init__(self) -> None:
+        self.path = Path.home() / ".config" / "ephemeral"
+        self.current_task: Task | None = None
+        self.history: List[Task] = []
+
+    @classmethod
+    def load(self) -> "Tracker":
+        tracker = Tracker()
+        if not tracker.path.is_file():
+            tracker.path.parent.mkdir(exist_ok=True)
+            tracker.path.write_text("{}")
+        data = json.loads(tracker.path.read_text())
+        tracker.current_task = None
+        if data.get("current_task") is not None:
+            tracker.current_task = Task(**data.get("current_task"))
+        _history = data.get("history", [])
+        tracker.history = [Task(**_task) for _task in _history]
+        return tracker
+
+    def save(self) -> None:
+        _history = [_task.json for _task in self.history]
+        data: dict = {"history": _history}
+        if self.current_task is not None:
+            data["current_task"] = self.current_task.json
+        self.path.write_text(json.dumps(data))
+
+    def update(self, new_task: Task | None = None) -> None:
+        # add current task to history
+        if self.current_task is not None:
+            self.current_task.end_ts = int(datetime.datetime.now(datetime.timezone.utc).timestamp())
+            self.history.append(self.current_task)
+        # update current task
+        self.current_task = new_task
+
+    def clear(self) -> None:
+        self.current_task = None
+        self.history = []
```

## Comparing `ephemeral_sh-0.2.1.dist-info/METADATA` & `ephemeral_sh-0.3.1.dist-info/METADATA`

 * *Files 17% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 Metadata-Version: 2.1
 Name: ephemeral-sh
-Version: 0.2.1
+Version: 0.3.1
 Summary: A one-task tracker in your terminal with a forgetful history
 Author-email: Mike Moran <mike@mkmrn.dev>
+Project-URL: GitLab, https://gitlab.com/mmoran0032/ephemeral-sh
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Requires-Dist: rich
 Requires-Dist: typer[all]
 Provides-Extra: dev
 Requires-Dist: black ; extra == 'dev'
 Requires-Dist: isort ; extra == 'dev'
@@ -15,12 +16,16 @@
 Requires-Dist: pytest-cov (>=4.0.0) ; extra == 'dev'
 Requires-Dist: pip-tools (>=6.0.0) ; extra == 'dev'
 
 # ephemeral-sh
 
 A one-task tracker in your terminal with a forgetful history.
 
-`Ephemeral` keeps track of a single task, and when it was started. Once you decide to track something new, the old task is forgotten.
+Ephemeral keeps track of a single task, and when it was started. Once you decide to track something new, the old task is forgotten.
 
 - See your current task: `ephemeral`
+- Complete your current task: `ephemeral complete`
 - Track a new task: `ephemeral track`
+- View your history: `ephemeral history`
 - Clear your history: `ephemeral clear`
+
+All actions are automatically persisted to the filesystem to keep the CLI and the data in sync.
```

