# Comparing `tmp/vmn-0.8.5rc2-py3-none-any.whl.zip` & `tmp/vmn-0.8.5rc3-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,12 +1,12 @@
-Zip file size: 45615 bytes, number of entries: 10
+Zip file size: 46295 bytes, number of entries: 10
 -rw-r--r--  2.0 unx      152 b- defN 21-Jul-06 16:25 version_stamp/__init__.py
--rw-r--r--  2.0 unx    53186 b- defN 23-Jun-11 21:33 version_stamp/stamp_utils.py
--rw-r--r--  2.0 unx       58 b- defN 23-Jun-11 21:54 version_stamp/version.py
--rw-r--r--  2.0 unx   113063 b- defN 23-Jun-11 21:40 version_stamp/vmn.py
--rw-r--r--  2.0 unx    35127 b- defN 23-Jun-11 21:54 vmn-0.8.5rc2.dist-info/LICENSE.txt
--rw-r--r--  2.0 unx      470 b- defN 23-Jun-11 21:54 vmn-0.8.5rc2.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jun-11 21:54 vmn-0.8.5rc2.dist-info/WHEEL
--rw-r--r--  2.0 unx       47 b- defN 23-Jun-11 21:54 vmn-0.8.5rc2.dist-info/entry_points.txt
--rw-r--r--  2.0 unx       14 b- defN 23-Jun-11 21:54 vmn-0.8.5rc2.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      804 b- defN 23-Jun-11 21:54 vmn-0.8.5rc2.dist-info/RECORD
-10 files, 203013 bytes uncompressed, 44245 bytes compressed:  78.2%
+-rw-r--r--  2.0 unx    55785 b- defN 23-Jul-22 19:41 version_stamp/stamp_utils.py
+-rw-r--r--  2.0 unx       60 b- defN 23-Jul-22 23:46 version_stamp/version.py
+-rw-r--r--  2.0 unx   114266 b- defN 23-Jul-22 23:40 version_stamp/vmn.py
+-rw-r--r--  2.0 unx    35127 b- defN 23-Jul-22 23:46 vmn-0.8.5rc3.dist-info/LICENSE.txt
+-rw-r--r--  2.0 unx      470 b- defN 23-Jul-22 23:46 vmn-0.8.5rc3.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-22 23:46 vmn-0.8.5rc3.dist-info/WHEEL
+-rw-r--r--  2.0 unx       47 b- defN 23-Jul-22 23:46 vmn-0.8.5rc3.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx       14 b- defN 23-Jul-22 23:46 vmn-0.8.5rc3.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      804 b- defN 23-Jul-22 23:46 vmn-0.8.5rc3.dist-info/RECORD
+10 files, 206817 bytes uncompressed, 44925 bytes compressed:  78.3%
```

## zipnote {}

```diff
@@ -6,26 +6,26 @@
 
 Filename: version_stamp/version.py
 Comment: 
 
 Filename: version_stamp/vmn.py
 Comment: 
 
-Filename: vmn-0.8.5rc2.dist-info/LICENSE.txt
+Filename: vmn-0.8.5rc3.dist-info/LICENSE.txt
 Comment: 
 
-Filename: vmn-0.8.5rc2.dist-info/METADATA
+Filename: vmn-0.8.5rc3.dist-info/METADATA
 Comment: 
 
-Filename: vmn-0.8.5rc2.dist-info/WHEEL
+Filename: vmn-0.8.5rc3.dist-info/WHEEL
 Comment: 
 
-Filename: vmn-0.8.5rc2.dist-info/entry_points.txt
+Filename: vmn-0.8.5rc3.dist-info/entry_points.txt
 Comment: 
 
-Filename: vmn-0.8.5rc2.dist-info/top_level.txt
+Filename: vmn-0.8.5rc3.dist-info/top_level.txt
 Comment: 
 
-Filename: vmn-0.8.5rc2.dist-info/RECORD
+Filename: vmn-0.8.5rc3.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## version_stamp/stamp_utils.py

```diff
@@ -4,73 +4,83 @@
 import glob
 import logging
 import os
 import pathlib
 import re
 import sys
 import time
-from logging.handlers import RotatingFileHandler
-import io
 from functools import wraps
+from logging.handlers import RotatingFileHandler
 
 import git
 import yaml
 
 INIT_COMMIT_MESSAGE = "Initialized vmn tracking"
 
 # Only used for printing
 VMN_VERSION_FORMAT = (
-    "{major}.{minor}.{patch}[.{hotfix}][-{prerelease}][+{buildmetadata}]"
+    "{major}.{minor}.{patch}[.{hotfix}][-{prerelease}][.{rcn}][+{buildmetadata}]"
 )
 VMN_DEFAULT_TEMPLATE = (
-    "[{major}][.{minor}][.{patch}][.{hotfix}]" "[-{prerelease}][+{buildmetadata}]"
+    "[{major}][.{minor}][.{patch}][.{hotfix}]" "[-{prerelease}][.{rcn}][+{buildmetadata}]"
 )
 
-_SEMVER_VER_REGEX = (
-    "(?P<major>0|[1-9]\d*)\." "(?P<minor>0|[1-9]\d*)\." "(?P<patch>0|[1-9]\d*)"
-)
+_DIGIT_REGEX = r"0|[1-9]\d*"
 
-_SEMVER_PRERELEASE_REGEX = "(?:-(?P<prerelease>(?:0|[1-9]\d*|\d*[a-zA-Z-][0-9a-zA-Z-]*)(?:\.(?:0|[1-9]\d*|\d*[a-zA-Z-][0-9a-zA-Z-]*))*))?"
+_SEMVER_BASE_VER_REGEX = (
+    rf"(?P<major>{_DIGIT_REGEX})\.(?P<minor>{_DIGIT_REGEX})\.(?P<patch>{_DIGIT_REGEX})"
+)
 
+_SEMVER_PRERELEASE_REGEX = rf"(?:-(?P<prerelease>(?:{_DIGIT_REGEX}|\d*[a-zA-Z-][0-9a-zA-Z-]*)(?:\.(?:{_DIGIT_REGEX}|\d*[a-zA-Z-][0-9a-zA-Z-]*))*))?"
+_VMN_PRERELEASE_REGEX = rf"{_SEMVER_PRERELEASE_REGEX[:-2]}\.(?P<rcn>(?:{_DIGIT_REGEX})))?"
 SEMVER_BUILDMETADATA_REGEX = (
-    "(?:\+(?P<buildmetadata>[0-9a-zA-Z-]+(?:\.[0-9a-zA-Z-]+)*))?"
+    r"(?:\+(?P<buildmetadata>[0-9a-zA-Z-]+(?:\.[0-9a-zA-Z-]+)*))?"
 )
 
-SEMVER_REGEX = (
-    f"^{_SEMVER_VER_REGEX}{_SEMVER_PRERELEASE_REGEX}{SEMVER_BUILDMETADATA_REGEX}$"
+# Unused
+__SEMVER_REGEX = (
+    rf"^{_SEMVER_BASE_VER_REGEX}{_SEMVER_PRERELEASE_REGEX}{SEMVER_BUILDMETADATA_REGEX}$"
 )
 
-_VMN_HOTFIX_REGEX = "(?:\.(?P<hotfix>0|[1-9]\d*))?"
+_VMN_HOTFIX_REGEX = rf"(?:\.(?P<hotfix>{_DIGIT_REGEX}))?"
+
+_VMN_BASE_VER_REGEX = rf"{_SEMVER_BASE_VER_REGEX}{_VMN_HOTFIX_REGEX}"
 
-_VMN_VER_REGEX = f"{_SEMVER_VER_REGEX}" f"{_VMN_HOTFIX_REGEX}"
+VMN_BASE_VER_REGEX = rf"^{_VMN_BASE_VER_REGEX}$"
 
-VMN_VER_REGEX = f"^{_VMN_VER_REGEX}$"
+_VMN_OLD_REGEX = (
+    rf"{_VMN_BASE_VER_REGEX}{_SEMVER_PRERELEASE_REGEX}{SEMVER_BUILDMETADATA_REGEX}"
+)
 
 _VMN_REGEX = (
-    f"{_VMN_VER_REGEX}" f"{_SEMVER_PRERELEASE_REGEX}" f"{SEMVER_BUILDMETADATA_REGEX}$"
+    rf"{_VMN_BASE_VER_REGEX}{_VMN_PRERELEASE_REGEX}{SEMVER_BUILDMETADATA_REGEX}"
 )
 
+VMN_OLD_REGEX = rf"^{_VMN_OLD_REGEX}$"
+VMN_OLD_TAG_REGEX = rf"^(?P<app_name>[^\/]+)_{_VMN_OLD_REGEX}$"
+
 # Regex for matching versions stamped by vmn
-VMN_REGEX = f"^{_VMN_REGEX}$"
+VMN_REGEX = rf"^{_VMN_REGEX}$"
 
 # TODO: create an abstraction layer on top of tag names versus the actual Semver versions
-VMN_TAG_REGEX = f"^(?P<app_name>[^\/]+)_{_VMN_REGEX}$"
+VMN_TAG_REGEX = rf"^(?P<app_name>[^\/]+)_{_VMN_REGEX}$"
 
-_VMN_ROOT_REGEX = "(?P<version>0|[1-9]\d*)"
-VMN_ROOT_REGEX = f"^{_VMN_ROOT_REGEX}$"
+_VMN_ROOT_REGEX = rf"(?P<version>{_DIGIT_REGEX})"
+VMN_ROOT_REGEX = rf"^{_VMN_ROOT_REGEX}$"
 
-VMN_ROOT_TAG_REGEX = f"^(?P<app_name>[^\/]+)_{_VMN_ROOT_REGEX}$"
+VMN_ROOT_TAG_REGEX = rf"^(?P<app_name>[^\/]+)_{_VMN_ROOT_REGEX}$"
 
 VMN_TEMPLATE_REGEX = (
-    "^(?:\[(?P<major_template>[^\{\}]*\{major\}[^\{\}]*)\])?"
-    "(?:\[(?P<minor_template>[^\{\}]*\{minor\}[^\{\}]*)\])?"
-    "(?:\[(?P<patch_template>[^\{\}]*\{patch\}[^\{\}]*)\])?"
-    "(?:\[(?P<hotfix_template>[^\{\}]*\{hotfix\}[^\{\}]*)\])?"
-    "(?:\[(?P<prerelease_template>[^\{\}]*\{prerelease\}[^\{\}]*)\])?"
-    "(?:\[(?P<buildmetadata_template>[^\{\}]*\{buildmetadata\}[^\{\}]*)\])?$"
+    r"^(?:\[(?P<major_template>[^\{\}]*\{major\}[^\{\}]*)\])?"
+    r"(?:\[(?P<minor_template>[^\{\}]*\{minor\}[^\{\}]*)\])?"
+    r"(?:\[(?P<patch_template>[^\{\}]*\{patch\}[^\{\}]*)\])?"
+    r"(?:\[(?P<hotfix_template>[^\{\}]*\{hotfix\}[^\{\}]*)\])?"
+    r"(?:\[(?P<prerelease_template>[^\{\}]*\{prerelease\}[^\{\}]*)\])?"
+    r"(?:\[(?P<rcn_template>[^\{\}]*\{rcn\}[^\{\}]*)\])?"
+    r"(?:\[(?P<buildmetadata_template>[^\{\}]*\{buildmetadata\}[^\{\}]*)\])?$"
 )
 
 RELATIVE_TO_CURRENT_VCS_POSITION_TYPE = "current"
 RELATIVE_TO_CURRENT_VCS_BRANCH_TYPE = "branch"
 RELATIVE_TO_GLOBAL_TYPE = "global"
 
 VMN_USER_NAME = "vmn"
@@ -278,75 +288,80 @@
         logger_obj.removeHandler(logger_obj.handlers[0])
     flen = len(logger_obj.filters)
     for f in range(flen):
         logger_obj.removeFilter(logger_obj.filters[0])
 
 
 class VMNBackend(object):
-    def __init__(self, type):
-        self._type = type
+    def __init__(self, btype):
+        self._type = btype
 
     def __del__(self):
         pass
 
     def type(self):
         return self._type
 
     def prepare_for_remote_operation(self):
         return 0
 
-    def get_first_reachable_version_info(
-        self, app_name, root=False, type=RELATIVE_TO_GLOBAL_TYPE
-    ):
-        return {}
-
     def get_active_branch(self):
         return "none"
 
     def remote(self):
         return "none"
 
     def last_user_changeset(self):
         return "none"
 
     @staticmethod
-    def app_name_to_git_tag_app_name(app_name):
+    def app_name_to_tag_name(app_name):
         return app_name.replace("/", "-")
 
     @staticmethod
+    def tag_name_to_app_name(tag_app_name):
+        return tag_app_name.replace("-", "/")
+
+    @staticmethod
     def gen_unique_id(verstr, hash):
         return f"{verstr}+{hash}"
 
     @staticmethod
     def get_utemplate_formatted_version(raw_vmn_version, template, hide_zero_hotfix):
-        match = re.search(VMN_REGEX, raw_vmn_version)
+        props = VMNBackend.deserialize_vmn_version(raw_vmn_version)
 
-        gdict = match.groupdict()
-        if gdict["hotfix"] == "0" and hide_zero_hotfix:
-            gdict["hotfix"] = None
+        if props["hotfix"] == 0 and hide_zero_hotfix:
+            props["hotfix"] = None
 
         octats = (
             "major",
             "minor",
             "patch",
             "hotfix",
             "prerelease",
+            "rcn",
             "buildmetadata",
         )
 
         formatted_version = ""
         for octat in octats:
-            if gdict[octat] is None:
+            if props[octat] is None:
                 continue
 
             if (
                 f"{octat}_template" in template
                 and template[f"{octat}_template"] is not None
             ):
-                d = {octat: gdict[octat]}
+                d = {octat: props[octat]}
+                if 'rcn' in d and props['old_ver_format']:
+                    continue
+
+                if 'prerelease' in d and d['prerelease'] == 'release':
+                    continue
+
                 formatted_version = (
                     f"{formatted_version}"
                     f"{template[f'{octat}_template'].format(**d)}"
                 )
 
         return formatted_version
 
@@ -358,203 +373,211 @@
 
         return "/".join(root_app_name[:-1])
 
     @staticmethod
     @measure_runtime_decorator
     def serialize_vmn_tag_name(
         app_name,
-        version,
-        hide_zero_hotfix,
-        prerelease=None,
-        prerelease_count=None,
-        buildmetadata=None,
+        verstr,
     ):
-        app_name = VMNBackend.app_name_to_git_tag_app_name(app_name)
-
-        verstr = VMNBackend.serialize_vmn_version(
-            version,
-            prerelease,
-            prerelease_count,
-            hide_zero_hotfix,
-            buildmetadata,
-        )
-
-        verstr = f"{app_name}_{verstr}"
+        tag_app_name = VMNBackend.app_name_to_tag_name(app_name)
+        tag_name = f"{tag_app_name}_{verstr}"
 
-        match = re.search(VMN_TAG_REGEX, verstr)
-        if match is None:
-            err = f"Tag {verstr} doesn't comply with: " f"{VMN_TAG_REGEX} format"
+        try:
+            props = VMNBackend.deserialize_tag_name(tag_name)
+            if props['hotfix'] == 0:
+                # tags are always without zero hotfix
+                verstr = VMNBackend.serialize_vmn_version(
+                    verstr, hide_zero_hotfix=True
+                )
+                tag_name = f"{tag_app_name}_{verstr}"
+                props = VMNBackend.deserialize_tag_name(tag_name)
+        except Exception as exc:
+            err = f"Tag {tag_name} doesn't comply with: " f"{VMN_TAG_REGEX} format"
             VMN_LOGGER.error(err)
 
             raise RuntimeError(err)
 
-        return verstr
+        return tag_name
 
     @staticmethod
     def serialize_vmn_version(
-        current_version,
-        prerelease,
-        prerelease_count,
-        hide_zero_hostfix,
+        base_verstr,
+        prerelease=None,
+        rcn=None,
         buildmetadata=None,
+        hide_zero_hotfix=False
     ):
-        vmn_version = VMNBackend.get_base_vmn_version(
-            current_version, hide_zero_hostfix
+        props = VMNBackend.deserialize_vmn_version(base_verstr)
+        base_verstr = VMNBackend.serialize_vmn_base_version(
+            props['major'],
+            props['minor'],
+            props['patch'],
+            props['hotfix'],
+            hide_zero_hotfix=hide_zero_hotfix
         )
 
-        if prerelease is None or prerelease == "release":
-            if buildmetadata is not None:
-                vmn_version = f"{vmn_version}+{buildmetadata}"
+        vmn_version = base_verstr
 
-            return vmn_version
+        if props['prerelease'] != "release":
+            if prerelease is not None:
+                VMN_LOGGER.warning(
+                    f"Tried to serialize verstr containing "
+                    f"prerelease component but also tried to append"
+                    f" another prerelease component. Will ignore it"
+                )
 
-        try:
-            assert prerelease in prerelease_count
-            # TODO: here try to use VMN_VERSION_FORMAT somehow
-            vmn_version = f"{vmn_version}-{prerelease}{prerelease_count[prerelease]}"
+            prerelease = props['prerelease']
+            if not props["old_ver_format"]:
+                rcn = props['rcn']
 
-            match = re.search(VMN_REGEX, vmn_version)
-            if match is None:
-                err = (
-                    f"Tag {vmn_version} doesn't comply with: "
-                    f"{VMN_VERSION_FORMAT} format"
+        if props["buildmetadata"] is not None:
+            if prerelease is not None:
+                VMN_LOGGER.warning(
+                    f"Tried to serialize verstr containing "
+                    f"buildmetadata component but also tried to append"
+                    f" another buildmetadata component. Will ignore it"
                 )
-                VMN_LOGGER.error(err)
 
-                raise RuntimeError(err)
-        except AssertionError:
-            VMN_LOGGER.error(
-                f"{prerelease} doesn't appear in {prerelease_count} "
-                "Turn on debug mode to see traceback"
-            )
-            VMN_LOGGER.debug("Exception info: ", exc_info=True)
+            buildmetadata = props['buildmetadata']
+
+        if prerelease is not None:
+            vmn_version = f"{vmn_version}-{prerelease}"
+
+            if rcn is not None:
+                vmn_version = f"{vmn_version}.{rcn}"
 
         if buildmetadata is not None:
             vmn_version = f"{vmn_version}+{buildmetadata}"
 
-            match = re.search(VMN_REGEX, vmn_version)
-            if match is None:
-                err = (
-                    f"Tag {vmn_version} doesn't comply with: "
-                    f"{VMN_VERSION_FORMAT} format"
-                )
-                VMN_LOGGER.error(err)
-                raise RuntimeError(err)
-
         return vmn_version
 
     @staticmethod
-    def serialize_vmn_version_hotfix(
-        hide_zero_hotfix, major, minor, patch, hotfix=None
+    def serialize_vmn_base_version(
+        major, minor, patch, hotfix=None, hide_zero_hotfix=None
     ):
-        if hide_zero_hotfix and hotfix == "0":
+        if hide_zero_hotfix is not None and hide_zero_hotfix and hotfix == 0:
             hotfix = None
 
         vmn_version = f"{major}.{minor}.{patch}"
         if hotfix is not None:
             vmn_version = f"{vmn_version}.{hotfix}"
 
         return vmn_version
 
     @staticmethod
-    def get_base_vmn_version(current_version, hide_zero_hotfix):
-        match = re.search(VMN_REGEX, current_version)
-        gdict = match.groupdict()
-        if gdict["hotfix"] is None:
-            gdict["hotfix"] = str(0)
-        vmn_version = VMNBackend.serialize_vmn_version_hotfix(
+    def get_base_vmn_version(some_verstr, hide_zero_hotfix=None):
+        props = VMNBackend.deserialize_vmn_version(some_verstr)
+
+        vmn_version = VMNBackend.serialize_vmn_base_version(
+            props["major"],
+            props["minor"],
+            props["patch"],
+            props["hotfix"],
             hide_zero_hotfix,
-            gdict["major"],
-            gdict["minor"],
-            gdict["patch"],
-            gdict["hotfix"],
         )
 
         return vmn_version
 
     @staticmethod
     def deserialize_tag_name(some_tag):
         ret = {
             "app_name": None,
-            "type": "version",
-            "version": None,
+            "old_tag_format": False,
+        }
+
+        match = re.search(VMN_ROOT_TAG_REGEX, some_tag)
+        if match is not None:
+            gdict = match.groupdict()
+            ret["app_name"] = gdict["app_name"]
+        else:
+            match = re.search(VMN_TAG_REGEX, some_tag)
+            old_tag_format = False
+            if match is None:
+                match = re.search(VMN_OLD_TAG_REGEX, some_tag)
+                if match is None:
+                    raise WrongTagFormatException()
+
+                old_tag_format = True
+
+            gdict = match.groupdict()
+            if old_tag_format:
+                ret["old_tag_format"] = True
+
+            ret["app_name"] = VMNBackend.tag_name_to_app_name(gdict["app_name"])
+
+        res = VMNBackend.app_name_to_tag_name(ret['app_name'])
+        ret['verstr'] = some_tag.split(f"{res}_")[1]
+
+        ret.update(
+            VMNBackend.deserialize_vmn_version(ret['verstr'])
+        )
+
+        return ret
+
+    @staticmethod
+    def deserialize_vmn_version(verstr):
+        ret = {
+            "types": {"version"},
             "root_version": None,
             "major": None,
             "minor": None,
             "patch": None,
             "hotfix": None,
-            "prerelease": None,
+            "prerelease": "release",
+            "rcn": None,
             "buildmetadata": None,
+            "old_ver_format": False,
         }
 
-        match = re.search(VMN_ROOT_TAG_REGEX, some_tag)
+        match = re.search(VMN_ROOT_REGEX, verstr)
         if match is not None:
             gdict = match.groupdict()
 
             int(gdict["version"])
             ret["root_version"] = gdict["version"]
-            ret["app_name"] = gdict["app_name"]
-            ret["type"] = "root"
+            ret["types"].add("root")
 
             return ret
 
-        match = re.search(VMN_TAG_REGEX, some_tag)
+        match = re.search(VMN_REGEX, verstr)
+        old_ver_format = False
         if match is None:
-            raise WrongTagFormatException()
+            match = re.search(VMN_OLD_REGEX, verstr)
+            if match is None:
+                raise WrongTagFormatException()
+
+            old_ver_format = True
 
         gdict = match.groupdict()
-        ret["app_name"] = gdict["app_name"].replace("-", "/")
-        ret["version"] = f'{gdict["major"]}.{gdict["minor"]}.{gdict["patch"]}'
-        ret["major"] = gdict["major"]
-        ret["minor"] = gdict["minor"]
-        ret["patch"] = gdict["patch"]
-        ret["hotfix"] = "0"
+        if old_ver_format:
+            gdict["rcn"] = -1
+            ret["old_ver_format"] = True
+
+        ret["major"] = int(gdict["major"])
+        ret["minor"] = int(gdict["minor"])
+        ret["patch"] = int(gdict["patch"])
+        ret["hotfix"] = 0
 
         if gdict["hotfix"] is not None:
-            ret["hotfix"] = gdict["hotfix"]
+            ret["hotfix"] = int(gdict["hotfix"])
 
-        # TODO: Think about what it means that we have the whole
-        #  prerelease string here (with the prerelease count).
-        #  At least rename other prerelease prefixes to
-        #  something like "prerelease mode" or "prerelease prefix"
         if gdict["prerelease"] is not None:
             ret["prerelease"] = gdict["prerelease"]
-            ret["type"] = "prerelease"
+            ret["rcn"] = int(gdict["rcn"])
+            ret["types"].add("prerelease")
 
         if gdict["buildmetadata"] is not None:
             ret["buildmetadata"] = gdict["buildmetadata"]
-            ret["type"] = "buildmetadata"
+            ret["types"].add("buildmetadata")
 
         return ret
 
     @staticmethod
     @measure_runtime_decorator
-    def enhance_ver_info(ver_infos):
-        all_tags = {}
-        for tag, ver_info_c in ver_infos.items():
-            tagd = VMNBackend.deserialize_vmn_tag_name(tag)
-            tagd.update({"tag": tag})
-            tagd["message"] = ver_info_c["ver_info"]
-
-            all_tags[tagd["type"]] = tagd
-
-            # TODO:: Check API commit version
-        # Enhance "raw" ver_infos so all tags will have all info
-        for t, v in ver_infos.items():
-            if "root_app" not in v["ver_info"]["stamping"] and "root" in all_tags:
-                v["ver_info"]["stamping"].update(
-                    all_tags["root"]["message"]["stamping"]
-                )
-            elif "app" not in v["ver_info"]["stamping"] and "version" in all_tags:
-                v["ver_info"]["stamping"].update(
-                    all_tags["version"]["message"]["stamping"]
-                )
-
-    @staticmethod
-    @measure_runtime_decorator
     def deserialize_vmn_tag_name(vmn_tag):
         try:
             return VMNBackend.deserialize_tag_name(vmn_tag)
         except WrongTagFormatException as exc:
             VMN_LOGGER.error(
                 f"Tag {vmn_tag} doesn't comply to vmn version format",
                 exc_info=True,
@@ -619,47 +642,97 @@
 
         latest_file = max(list_of_files, key=os.path.getctime)
 
         with open(latest_file, "r") as f:
             ver_infos["none"]["ver_info"] = yaml.safe_load(f)
             return "none", ver_infos
 
+    def get_latest_available_tag(self, tag_prefix_filter):
+        return None
+
     def get_actual_deps_state(self, vmn_root_path, paths):
         actual_deps_state = {
             ".": {
                 "hash": "0xdeadbeef",
                 "remote": "none",
                 "vcs_type": VMN_BE_TYPE_LOCAL_FILE,
             }
         }
 
         return actual_deps_state
 
     def get_tag_version_info(self, tag_name):
         tagd = VMNBackend.deserialize_vmn_tag_name(tag_name)
-        if tagd["type"] == "root":
+        if "root" in tagd["types"]:
             dir_path = os.path.join(
                 self.repo_path, ".vmn", tagd["app_name"], "root_verinfo"
             )
             path = os.path.join(dir_path, f"{tagd['root_version']}.yml")
         else:
             dir_path = os.path.join(self.repo_path, ".vmn", tagd["app_name"], "verinfo")
-            path = os.path.join(dir_path, f"{tagd['version']}.yml")
+            path = os.path.join(dir_path, f"{tagd['verstr']}.yml")
 
-        ver_infos = {
-            tag_name: {"ver_info": None, "tag_object": None, "commit_object": None}
-        }
+        ver_infos = {}
         try:
             with open(path, "r") as f:
+                ver_infos = {
+                    tag_name: {
+                        "ver_info": None,
+                        "tag_object": None,
+                        "commit_object": None
+                    }
+                }
                 ver_infos[tag_name]["ver_info"] = yaml.safe_load(f)
         except Exception as exc:
-            VMN_LOGGER.error("Logged Exception message:", exc_info=True)
+            VMN_LOGGER.debug("Logged Exception message:", exc_info=True)
 
         return tag_name, ver_infos
 
+    @measure_runtime_decorator
+    def get_latest_stamp_tags(
+            self, app_name, root_context, type=RELATIVE_TO_GLOBAL_TYPE
+    ):
+        if root_context:
+            dir_path = os.path.join(
+                self.repo_path, ".vmn", app_name, "root_verinfo"
+            )
+        else:
+            dir_path = os.path.join(self.repo_path, ".vmn", app_name, "verinfo")
+
+        files = glob.glob(os.path.join(dir_path, '*'))
+
+        # sort the files by modification date
+        files.sort(key=os.path.getmtime, reverse=True)
+
+        ver_infos = {}
+        tag_names = []
+        if files:
+            with open(files[0], "r") as f:
+                data = yaml.safe_load(f)
+                if root_context:
+                    ver = data["stamping"]["root_app"]["version"]
+                else:
+                    ver = data["stamping"]["app"]["_version"]
+
+                tag_name = VMNBackend.serialize_vmn_tag_name(
+                    app_name,
+                    ver
+                )
+                tag_names.append(tag_name)
+                ver_infos = {
+                    tag_name: {
+                        "ver_info": None,
+                        "tag_object": None,
+                        "commit_object": None
+                    }
+                }
+                ver_infos[tag_name]["ver_info"] = data
+
+        return tag_names, None, ver_infos
+
 
 class GitBackend(VMNBackend):
     @measure_runtime_decorator
     def __init__(self, repo_path, inherit_env=False):
         VMNBackend.__init__(self, VMN_BE_TYPE_GIT)
 
         self._be = GitBackend.initialize_git_backend(repo_path, inherit_env)
@@ -756,64 +829,96 @@
         if push and self.remote_active_branch is None:
             raise RuntimeError("Will not push remote branch does not exist")
 
         for tag, message in zip(tags, messages):
             # This is required in order to preserver chronological order when
             # listing tags since the taggerdate field is in seconds resolution
             time.sleep(1.1)
-            self._be.create_tag(tag, ref=ref, message=message)
+
+            ret = self._be.create_tag(tag, ref=ref, message=message)
 
             if not push:
                 continue
 
             try:
-                self.selected_remote.push(refspec=f"refs/tags/{tag}", o="ci.skip")
-            except Exception:
-                self.selected_remote.push(refspec=f"refs/tags/{tag}")
+                ret = self._be.git.execute(["git", "push", "--porcelain", "-o", "ci.skip", self.selected_remote.name, f"refs/tags/{tag}"])
+            except Exception as exc:
+                try:
+                    self._be.git.execute(["git", "push", "--porcelain", self.selected_remote.name, f"refs/tags/{tag}"])
+                except Exception as exc:
+                    tag_err_str = f"Failed to tag {tag}. Reverting.."
+                    VMN_LOGGER.error(tag_err_str)
+
+                    try:
+                        self._be.delete_tag(tag)
+                    except Exception as exc:
+                        err_str = f"Failed to remove tag {tag}"
+                        VMN_LOGGER.info(err_str)
+                        VMN_LOGGER.debug("Exception info: ", exc_info=True)
+
+                    raise RuntimeError(tag_err_str)
 
     @measure_runtime_decorator
     def push(self, tags=()):
         if self.detached_head:
             raise RuntimeError("Will not push from detached head")
 
         if self.remote_active_branch is None:
             raise RuntimeError("Will not push remote branch does not exist")
 
         remote_branch_name_no_remote_name = "".join(
             self.remote_active_branch.split(f"{self.selected_remote.name}/")
         )
 
         try:
-            ret = self.selected_remote.push(
-                refspec=f"refs/heads/{self.active_branch}:{remote_branch_name_no_remote_name}",
-                o="ci.skip",
+            ret = self._be.git.execute(
+                [
+                    "git", "push", "--porcelain", "-o", "ci.skip", self.selected_remote.name,
+                    f"refs/heads/{self.active_branch}:{remote_branch_name_no_remote_name}"
+                ]
             )
         except Exception as exc:
-            ret = self.selected_remote.push(
-                refspec=f"refs/heads/{self.active_branch}:{remote_branch_name_no_remote_name}"
-            )
-
-        if ret[0].old_commit is None:
-            if "up to date" in ret[0].summary:
-                VMN_LOGGER.warning(
-                    "GitPython library has failed to push because we are "
-                    "up to date already. How can it be? "
-                )
-            else:
-                VMN_LOGGER.error("Push has failed. Please verify that 'git push' works")
-                raise Warning(
-                    f"Push has failed because: {ret[0].summary}.\n"
-                    "Please verify that 'git push' works"
+            try:
+                ret = self._be.git.execute(
+                    [
+                        "git",
+                        "push",
+                        "--porcelain",
+                        self.selected_remote.name,
+                        f"refs/heads/{self.active_branch}:{remote_branch_name_no_remote_name}"
+                     ]
                 )
+            except Exception as exc:
+                err_str = "Push has failed. Please verify that 'git push' works"
+                VMN_LOGGER.error(err_str, exc_info=True)
+                raise RuntimeError(err_str)
 
         for tag in tags:
             try:
-                self.selected_remote.push(refspec=f"refs/tags/{tag}", o="ci.skip")
+                ret = self._be.git.execute(
+                    [
+                        "git",
+                        "push",
+                        "--porcelain",
+                        "-o",
+                        "ci.skip",
+                        self.selected_remote.name,
+                        f"refs/tags/{tag}"
+                    ]
+                )
             except Exception:
-                self.selected_remote.push(refspec=f"refs/tags/{tag}")
+                ret = self._be.git.execute(
+                    [
+                        "git",
+                        "push",
+                        "--porcelain",
+                        self.selected_remote.name,
+                        f"refs/tags/{tag}"
+                    ]
+                )
 
     @measure_runtime_decorator
     def pull(self):
         if self.detached_head:
             raise RuntimeError("Will not pull in detached head")
 
         self.selected_remote.pull("--ff-only")
@@ -930,15 +1035,15 @@
             )
             tag_names = []
             for tag_object in tag_objects:
                 tag_names.append(tag_object.name)
 
             return tag_names, cobj, ver_infos
 
-        tag_name_prefix = VMNBackend.app_name_to_git_tag_app_name(app_name)
+        tag_name_prefix = VMNBackend.app_name_to_tag_name(app_name)
         cmd = ["--sort", "taggerdate", "--list", f"{tag_name_prefix}_*"]
         tag_names = self._be.git.tag(*cmd).split("\n")
 
         if len(tag_names) == 1 and tag_names[0] == "":
             tag_names.pop(0)
 
         if not tag_names:
@@ -1009,22 +1114,30 @@
         ver_infos = self.get_all_commit_tags_log_impl(commit_hex, tags, app_name)
 
         cobj = self.get_commit_object_from_commit_hex(commit_hex)
 
         return cobj, ver_infos
 
     @measure_runtime_decorator
-    def get_latest_available_tag(self, tag_prefix_filter):
+    def get_latest_available_tags(self, tag_prefix_filter):
         cmd = ["--sort", "taggerdate", "--list", tag_prefix_filter]
         tag_names = self._be.git.tag(*cmd).split("\n")
 
         if len(tag_names) == 1 and tag_names[0] == "":
             return None
 
-        return tag_names[-1]
+        return tag_names
+
+    @measure_runtime_decorator
+    def get_latest_available_tag(self, tag_prefix_filter):
+        tnames = self.get_latest_available_tags(tag_prefix_filter)
+        if tnames is None:
+            return None
+
+        return tnames[-1]
 
     @measure_runtime_decorator
     def get_commit_object_from_branch_name(self, bname):
         # TODO:: Unfortunately, need to spend o(N) here
         for branch in self._be.branches:
             if bname != branch.name:
                 continue
@@ -1259,15 +1372,15 @@
         if self.remote_active_branch is not None:
             return 0
 
         local_branch_name = self.active_branch
 
         VMN_LOGGER.warning(
             f"No remote branch for local branch: {local_branch_name} "
-            f"was found. Will try to set upstream for it"
+            f"was found for repo {self.repo_path}. Will try to set upstream for it"
         )
 
         out = self._be.git.branch("-r", "--contains", "HEAD")
         out = out.split("\n")[0].strip()
         if not out:
             out = f"{self.selected_remote.name}/{local_branch_name}"
 
@@ -1390,14 +1503,15 @@
     @measure_runtime_decorator
     def last_user_changeset(self):
         p = self._be.head.commit
         if p.author.name == VMN_USER_NAME:
             if p.message.startswith(INIT_COMMIT_MESSAGE):
                 return p.hexsha
 
+            # TODO:: think how to use this tags for later in order to avoid getting all tags again.
             ver_infos = self.get_all_commit_tags(p.hexsha)
             if not ver_infos:
                 VMN_LOGGER.warning(
                     f"Somehow vmn's commit {p.hexsha} has no tags. "
                     f"Check your repo. Assuming this commit is a user commit"
                 )
                 return p.hexsha
@@ -1452,14 +1566,15 @@
                 except Exception as exc:
                     VMN_LOGGER.debug(f"Failed to git reset files: {files}", exc_info=True)
 
                 self._be.index.checkout(files, force=True)
             except Exception as exc:
                 VMN_LOGGER.debug(f"Failed to git checkout files: {files}", exc_info=True)
 
+
     @measure_runtime_decorator
     def revert_vmn_commit(self, prev_changeset, version_files, tags=[]):
         self.revert_local_changes(version_files)
 
         # TODO: also validate that the commit is
         #  currently worked on app name
         if self.changeset() == prev_changeset:
@@ -1469,88 +1584,48 @@
             VMN_LOGGER.error("BUG: Will not revert non-vmn commit.")
             raise RuntimeError()
 
         self._be.git.reset("--hard", "HEAD~1")
         for tag in tags:
             try:
                 self._be.delete_tag(tag)
-            except Exception:
+            except Exception as exc:
                 VMN_LOGGER.info(f"Failed to remove tag {tag}")
                 VMN_LOGGER.debug("Exception info: ", exc_info=True)
 
                 continue
 
         try:
             self._be.git.fetch("--tags")
         except Exception:
             VMN_LOGGER.info("Failed to fetch tags")
             VMN_LOGGER.debug("Exception info: ", exc_info=True)
 
-    @measure_runtime_decorator
-    def get_first_reachable_version_info(
-        self, app_name, root_context=False, type=RELATIVE_TO_GLOBAL_TYPE
-    ):
-        app_tags, cobj, ver_infos = self.get_latest_stamp_tags(
-            app_name, root_context, type
-        )
-
-        if root_context:
-            regex = VMN_ROOT_TAG_REGEX
-        else:
-            regex = VMN_TAG_REGEX
-
-        cleaned_app_tag = None
-        for tag in app_tags:
-            # skip buildmetadata versions
-            if "+" in tag:
-                continue
-
-            match = re.search(regex, tag)
-            if match is None:
-                continue
-
-            gdict = match.groupdict()
-
-            if gdict["app_name"] != app_name.replace("/", "-"):
-                continue
-
-            cleaned_app_tag = tag
-            break
-
-        if cleaned_app_tag is None:
-            return None, {}
-
-        if cleaned_app_tag not in ver_infos:
-            VMN_LOGGER.debug(f"Somehow {cleaned_app_tag} not in ver_infos")
-            return None, {}
-
-        VMNBackend.enhance_ver_info(ver_infos)
-
-        return cleaned_app_tag, ver_infos
 
     @measure_runtime_decorator
     def get_tag_version_info(self, tag_name):
         ver_infos = {}
         tag_name, commit_tag_obj = self.get_commit_object_from_tag_name(tag_name)
+
+        # TODO:: support starting from rc versions
+
         if commit_tag_obj is None:
             VMN_LOGGER.debug(f"Tried to find {tag_name} but with no success")
             return tag_name, ver_infos
 
         if commit_tag_obj.author.name != VMN_USER_NAME:
             VMN_LOGGER.debug(f"Corrupted tag {tag_name}: author name is not vmn")
             return tag_name, ver_infos
 
         # "raw" ver_infos
         ver_infos = self.get_all_brother_tags(tag_name)
         if tag_name not in ver_infos:
             VMN_LOGGER.debug(f"Could not find version info for {tag_name}")
             return tag_name, None
 
-        VMNBackend.enhance_ver_info(ver_infos)
-
         return tag_name, ver_infos
 
     @measure_runtime_decorator
     def parse_tag_message(self, tag_name):
         tag_name, tag_obj = self.get_tag_object_from_tag_name(tag_name)
 
         ret = {"ver_info": None, "tag_object": tag_obj, "commit_object": None}
```

## version_stamp/version.py

```diff
@@ -1,3 +1,3 @@
 name = "vmn"
-version = "0.8.5-rc2"
-_version = "0.8.5-rc2"
+version = "0.8.5-rc.3"
+_version = "0.8.5-rc.3"
```

## version_stamp/vmn.py

```diff
@@ -9,14 +9,15 @@
 import re
 import sys
 import time
 from multiprocessing import Pool
 from pathlib import Path
 from pprint import pformat
 
+import git
 import jinja2
 import tomlkit
 import yaml
 from filelock import FileLock
 from packaging import version as pversion
 
 CUR_PATH = "{0}/".format(os.path.dirname(__file__))
@@ -79,14 +80,19 @@
 
         self.vcs = VersionControlStamper(self.params)
 
 
 class IVersionsStamper(object):
     @stamp_utils.measure_runtime_decorator
     def __init__(self, arg_params):
+        # actual value will be assigned on handle_ functions
+        self.prerelease = None
+        self.release_mode = None
+        self.dry_run = None
+
         self.app_conf_path = None
         self.params: dict = arg_params
         self.vmn_root_path: str = arg_params["root_path"]
         self.repo_name: str = "."
         self.name: str = arg_params["name"]
         self.be_type = arg_params["be_type"]
 
@@ -242,48 +248,149 @@
                     self.vmn_root_path,
                 )
                 flat_deps[key] = v[repo]
 
         self.configured_deps = flat_deps
 
     @stamp_utils.measure_runtime_decorator
-    def get_version_info_from_verstr(self, verstr):
-        tag_name = self.get_tag_name(verstr)
-        if self.root_context:
-            try:
-                int(verstr)
-            except Exception:
-                stamp_utils.VMN_LOGGER.error(
-                    "wrong version specified: root version must be an integer"
-                )
+    def get_version_number_from_file(self, version_file_path) -> str or None:
+        if not os.path.exists(version_file_path):
+            return None
+
+        with open(version_file_path, "r") as fid:
+            ver_dict = yaml.safe_load(fid)
+            if "version_to_stamp_from" in ver_dict:
+                verstr = ver_dict["version_to_stamp_from"]
+                # 0.8.4
+                if 'prerelease' in ver_dict:
+                    base_verstr = verstr
+                    prerelease = None
+                    if ver_dict['prerelease'] != "release":
+                        prerelease = f"{ver_dict['prerelease']}{ver_dict['prerelease_count'][ver_dict['prerelease']]}"
+                    verstr = stamp_utils.VMNBackend.serialize_vmn_version(
+                        base_verstr,
+                        prerelease=prerelease,
+                        hide_zero_hotfix=self.hide_zero_hotfix,
+                    )
+            else:
+                verstr = ver_dict["last_stamped_version"]
 
-                return tag_name, {}
-        else:
             try:
-                stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag_name)
+                props = stamp_utils.VMNBackend.deserialize_vmn_version(verstr)
             except Exception as exc:
-                stamp_utils.VMN_LOGGER.error(f"Wrong version specified: {verstr}")
-                stamp_utils.VMN_LOGGER.debug(f"Logged exception: ", exc_info=True)
+                err = (
+                    f"Version in version file: {verstr} doesn't comply with: "
+                    f"{stamp_utils.VMN_VERSION_FORMAT} format"
+                )
+                stamp_utils.VMN_LOGGER.error(err)
+
+                raise RuntimeError(err)
+
+            return verstr
+
+    @stamp_utils.measure_runtime_decorator
+    def get_first_reachable_version_info(
+        self, app_name, root_context=False, type=stamp_utils.RELATIVE_TO_GLOBAL_TYPE
+    ):
+        app_tags, cobj, ver_infos = self.backend.get_latest_stamp_tags(
+            app_name, root_context, type
+        )
+
+        cleaned_app_tag = None
+        for tag in app_tags:
+            # skip buildmetadata versions
+            if "+" in tag:
+                continue
+
+            props = stamp_utils.VMNBackend.deserialize_tag_name(tag)
+
+            # can happen in case of a root app
+            if props["app_name"] != app_name:
+                continue
+
+            cleaned_app_tag = tag
+            break
+
+        if cleaned_app_tag is None:
+            return None, {}
+
+        if cleaned_app_tag not in ver_infos:
+            stamp_utils.VMN_LOGGER.debug(f"Somehow {cleaned_app_tag} not in ver_infos")
+            return None, {}
 
-                return tag_name, {}
+        self.enhance_ver_info(ver_infos)
 
-        tag_name, ver_infos = self.backend.get_tag_version_info(tag_name)
+        return cleaned_app_tag, ver_infos
+
+    @stamp_utils.measure_runtime_decorator
+    def enhance_ver_info(self, ver_infos):
+        root_tag = None
+        ver_tag = None
+        for tag, ver_info_c in ver_infos.items():
+            props = stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag)
+            if 'root' in props['types']:
+                root_tag = tag
+                continue
+
+            if props['types'] == {'version'}:
+                ver_tag = tag
+                continue
+
+            # TODO:: Check API commit version
+
+        if root_tag is None:
+            return
+
+        if ver_tag is None:
+            return
+
+        ver_infos[ver_tag]["ver_info"]["stamping"]["root_app"] = \
+            ver_infos[root_tag]["ver_info"]["stamping"]["root_app"]
+
+        ver_infos[root_tag]["ver_info"]["stamping"]["app"] = \
+            ver_infos[ver_tag]["ver_info"]["stamping"]["app"]
+
+    @stamp_utils.measure_runtime_decorator
+    def get_version_info_from_verstr(self, verstr):
+        actual_tag = self.get_tag_name(verstr)
+
+        # tag_name, commit_tag_obj = self.backend.get_commit_object_from_tag_name(tag_name)
+        # if commit_tag_obj is None:
+        #     # Find the last occurrence of '.'
+        #     last_dot_index = tag_name.rfind('.')
+        #     if last_dot_index == -1:
+        #         raise RuntimeError(
+        #             f"No '.' found in tag name {tag_name} "
+        #             f"although it appears to be prerelease tag"
+        #         )
+        #
+        #     # Remove the last dot
+        #     old_tag_name = f"{tag_name[:last_dot_index]}{tag_name[last_dot_index + 1:]}"
+        #     old_tag_name, commit_tag_obj = self.backend.get_commit_object_from_tag_name(old_tag_name)
+
+        try:
+            props = stamp_utils.VMNBackend.deserialize_vmn_version(verstr)
+        except Exception as exc:
+            stamp_utils.VMN_LOGGER.debug(exc_info=True)
+            return actual_tag, {}
+
+        actual_tag, ver_infos = self.backend.get_tag_version_info(actual_tag)
         if not ver_infos:
             stamp_utils.VMN_LOGGER.error(
-                f"Failed to get version info for tag: {tag_name}"
+                f"Failed to get version info for tag: {actual_tag}"
             )
 
-            return tag_name, {}
+            return actual_tag, {}
 
-        if tag_name not in ver_infos or ver_infos[tag_name]["ver_info"] is None:
-            return tag_name, {}
+        if actual_tag not in ver_infos or ver_infos[actual_tag]["ver_info"] is None:
+            return actual_tag, {}
 
-        stamp_utils.VMNBackend.enhance_ver_info(ver_infos)
+        self.enhance_ver_info(ver_infos)
 
-        return tag_name, ver_infos
+        return actual_tag, ver_infos
 
     @stamp_utils.measure_runtime_decorator
     def get_tag_name(self, verstr):
         tag_name = f'{self.name.replace("/", "-")}'
         assert verstr is not None
         tag_name = f"{tag_name}_{verstr}"
 
@@ -315,40 +422,43 @@
         self.actual_deps_state["."]["hash"] = self.last_user_changeset
         self.current_version_info["stamping"]["app"]["changesets"] = copy.deepcopy(
             self.actual_deps_state
         )
 
         self.ver_infos_from_repo = {}
         self.selected_tag = None
-        (
-            initial_version,
-            prerelease,
-            prerelease_count,
-        ) = VersionControlStamper.get_version_number_from_file(self.version_file_path)
-        if initial_version is not None:
-            verstr = stamp_utils.VMNBackend.serialize_vmn_version(
-                initial_version, prerelease, prerelease_count, self.hide_zero_hotfix
-            )
+
+        verstr = self.get_version_number_from_file(self.version_file_path)
+
+        # verstr will be None only when running for the first time or file removed somehow
+        if verstr is not None:
             (
                 self.selected_tag,
                 self.ver_infos_from_repo,
             ) = self.get_version_info_from_verstr(verstr)
-            t = self.get_tag_name(initial_version)
+            base_ver = stamp_utils.VMNBackend.get_base_vmn_version(
+                verstr,
+                self.hide_zero_hotfix,
+            )
+            t = self.get_tag_name(base_ver)
             if t != self.selected_tag and t in self.ver_infos_from_repo:
                 self.selected_tag = t
 
         if not self.ver_infos_from_repo:
             (
                 selected_tag,
                 self.ver_infos_from_repo,
-            ) = self.backend.get_first_reachable_version_info(
+            ) = self.get_first_reachable_version_info(
                 self.name,
                 self.root_context,
                 type=stamp_utils.RELATIVE_TO_CURRENT_VCS_POSITION_TYPE,
             )
+
+            self.enhance_ver_info(self.ver_infos_from_repo)
+
             if selected_tag is not None and selected_tag != self.selected_tag:
                 self.selected_tag = selected_tag
 
         self.tracked = (
             self.selected_tag in self.ver_infos_from_repo
             and self.ver_infos_from_repo[self.selected_tag]["ver_info"] is not None
         )
@@ -394,183 +504,180 @@
 
     def __del__(self):
         if self.backend is not None:
             del self.backend
             self.backend = None
 
     # Note: this function generates a version (including prerelease)
-    def gen_advanced_version(
-        self, initial_version, initialprerelease, initialprerelease_count
-    ):
-        verstr = self.advance_version(initial_version, self.release_mode)
+    def gen_advanced_version(self, verstr):
+        verstr, prerelease_count = self.advance_version(verstr, self.release_mode)
 
-        prerelease = self.prerelease
-        # If user did not specify a change in prerelease,
-        # stay with the previous one
-        if prerelease is None and self.release_mode is None:
-            prerelease = initialprerelease
-        prerelease_count = copy.deepcopy(initialprerelease_count)
-
-        # Continue from last stamp prerelease information as long as
-        # the last version is coherent with what is requested from
-        # the version file or manual version (manual version is not yet implemented)
-        prerelease, prerelease_count = self._advance_prerelease(
-            verstr, prerelease, prerelease_count
-        )
-
-        return verstr, prerelease, prerelease_count
-
-    def _advance_prerelease(self, verstr, prerelease, prerelease_count):
-        if prerelease is None:
-            return None, {}
-        if prerelease == "release":
-            try:
-                raise RuntimeError()
-            except RuntimeError:
-                stamp_utils.VMN_LOGGER.error(
-                    "prerelease equals to 'release' somehow. "
-                    "Turn on debug mode to see traceback"
-                )
-                stamp_utils.VMN_LOGGER.debug("Exception info: ", exc_info=True)
-
-            return None, {}
-
-        prerelease_count = copy.deepcopy(prerelease_count)
-        counter_key = f"{prerelease}"
-        if counter_key not in prerelease_count:
-            prerelease_count[counter_key] = 0
-
-        tag_name_prefix = stamp_utils.VMNBackend.app_name_to_git_tag_app_name(self.name)
-
-        tag_name_prefix = f'{self.name.replace("/", "-")}_{verstr}-{prerelease}*'
-        tag = self.backend.get_latest_available_tag(tag_name_prefix)
-        if tag:
-            props = stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag)
-
-            global_val = int(props["prerelease"].split(prerelease)[1])
-            prerelease_count[counter_key] = max(
-                prerelease_count[counter_key], global_val
-            )
-
-        prerelease_count[counter_key] += 1
+        return verstr, prerelease_count
 
-        if self.release_mode is not None:
-            prerelease_count = {counter_key: 1}
-
-        return counter_key, prerelease_count
-
-    def increase_octet(self, tag_name_prefix: str, version_number_oct: str, release_mode: str, globally: bool) -> str:
+    def increase_octet(self, tag_name_prefix: str, version_number_oct: str, release_mode: str, globally: bool) -> int:
         tag = self.backend.get_latest_available_tag(tag_name_prefix)
         version_number_oct = int(version_number_oct)
         if tag and globally:
             props = stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag)
             version_number_oct = max(version_number_oct, int(props[release_mode]))
         version_number_oct += 1
-        return str(version_number_oct)
+
+        return version_number_oct
 
     def advance_version(self, version, release_mode, globally=True):
-        # TODO: maybe move up the version validity test
-        match = re.search(stamp_utils.VMN_REGEX, version)
-        gdict = match.groupdict()
-        if gdict["hotfix"] is None:
-            gdict["hotfix"] = "0"
+        props = stamp_utils.VMNBackend.deserialize_vmn_version(version)
 
-        major = gdict["major"]
-        minor = gdict["minor"]
-        patch = gdict["patch"]
-        hotfix = gdict["hotfix"]
+        major = props["major"]
+        minor = props["minor"]
+        patch = props["patch"]
+        hotfix = props["hotfix"]
 
         if release_mode == "major":
-            tag_name_prefix = stamp_utils.VMNBackend.app_name_to_git_tag_app_name(
+            tag_name_prefix = stamp_utils.VMNBackend.app_name_to_tag_name(
                 self.name
             )
 
             tag_name_prefix = f"{tag_name_prefix}_*"
             major = self.increase_octet(tag_name_prefix, major, release_mode, globally)
 
-            minor = "0"
-            patch = "0"
-            hotfix = "0"
+            minor = 0
+            patch = 0
+            hotfix = 0
         elif release_mode == "minor":
-            tag_name_prefix = stamp_utils.VMNBackend.app_name_to_git_tag_app_name(
+            tag_name_prefix = stamp_utils.VMNBackend.app_name_to_tag_name(
                 self.name
             )
 
-            tag_name_prefix = f"{tag_name_prefix}_{major}*"
+            # TODO:: use serialize functions here
+            tag_name_prefix = f"{tag_name_prefix}_{major}.*"
             minor = self.increase_octet(tag_name_prefix, minor, release_mode, globally)
 
-            patch = "0"
-            hotfix = "0"
+            patch = 0
+            hotfix = 0
         elif release_mode == "patch":
-            tag_name_prefix = stamp_utils.VMNBackend.app_name_to_git_tag_app_name(
+            tag_name_prefix = stamp_utils.VMNBackend.app_name_to_tag_name(
                 self.name
             )
 
-            tag_name_prefix = f"{tag_name_prefix}_{major}.{minor}*"
+            tag_name_prefix = f"{tag_name_prefix}_{major}.{minor}.*"
             patch = self.increase_octet(tag_name_prefix, patch, release_mode, globally)
 
-            hotfix = "0"
+            hotfix = 0
         elif release_mode == "hotfix":
-            tag_name_prefix = stamp_utils.VMNBackend.app_name_to_git_tag_app_name(
+            tag_name_prefix = stamp_utils.VMNBackend.app_name_to_tag_name(
                 self.name
             )
 
-            tag_name_prefix = f"{tag_name_prefix}_{major}.{minor}.{patch}*"
+            tag_name_prefix = f"{tag_name_prefix}_{major}.{minor}.{patch}.*"
             hotfix = self.increase_octet(tag_name_prefix, hotfix, release_mode, globally)
 
-        return stamp_utils.VMNBackend.serialize_vmn_version_hotfix(
-            self.hide_zero_hotfix,
+        base_version = stamp_utils.VMNBackend.serialize_vmn_base_version(
             major,
             minor,
             patch,
             hotfix,
+            hide_zero_hotfix=self.hide_zero_hotfix,
+        )
+
+        tag_name_prefix = stamp_utils.VMNBackend.serialize_vmn_tag_name(
+            self.name, base_version
         )
+        tag_name_prefix = f"{tag_name_prefix}-*"
+        tag = self.backend.get_latest_available_tag(tag_name_prefix)
+
+        ver_info_c = self.ver_infos_from_repo[self.selected_tag]
+        if tag is not None:
+            t, ver_info_c = self.backend.parse_tag_message(tag)
+
+        initialprerelease = \
+            self.ver_infos_from_repo[self.selected_tag]["ver_info"]["stamping"]["app"]["prerelease"]
+        initialprerelease_count = ver_info_c["ver_info"]["stamping"]["app"]["prerelease_count"]
 
-    def write_version_to_file(
-        self, version_number: str, prerelease: str, prerelease_count: dict
-    ) -> None:
+        prerelease = self.prerelease
+        # If user did not specify a change in prerelease,
+        # stay with the previous one
+        if prerelease is None and release_mode is None:
+            prerelease = initialprerelease
+        prerelease_count = copy.deepcopy(initialprerelease_count)
+
+        if prerelease == "release":
+            return stamp_utils.VMNBackend.serialize_vmn_version(
+                base_version,
+                hide_zero_hotfix=self.hide_zero_hotfix,
+            ), {}
+
+        if prerelease not in prerelease_count:
+            prerelease_count[prerelease] = 0
+
+        res_ver = stamp_utils.VMNBackend.serialize_vmn_version(
+            base_version,
+            prerelease=prerelease,
+        )
+        tag_name_prefix = stamp_utils.VMNBackend.serialize_vmn_tag_name(
+            self.name,
+            res_ver
+        )
+        # TODO:: check if * can be replaced by .+
+        tag_name_prefix = f"{tag_name_prefix}*"
+
+        tag = self.backend.get_latest_available_tag(tag_name_prefix)
+        if tag:
+            tprops = stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag)
+
+            if not tprops["old_tag_format"]:
+                global_val = tprops["rcn"]
+            else:
+                global_val = int(tprops["prerelease"].split(prerelease)[1])
+
+            prerelease_count[prerelease] = max(
+                prerelease_count[prerelease],
+                global_val
+            )
+
+        prerelease_count[prerelease] += 1
+
+        if release_mode is not None:
+            prerelease_count = {prerelease: 1}
+
+        return stamp_utils.VMNBackend.serialize_vmn_version(
+            base_version,
+            prerelease,
+            prerelease_count[prerelease],
+            hide_zero_hotfix=self.hide_zero_hotfix,
+        ), prerelease_count
+
+    def write_version_to_file(self, version_number: str) -> None:
         if self.dry_run:
             stamp_utils.VMN_LOGGER.info(
                 "Would have written to version file:\n"
                 f"version: {version_number}\n"
-                f"prerelease: {prerelease}\n"
-                f"prerelease count: {prerelease_count}"
             )
         else:
-            self._write_version_to_vmn_version_file(
-                prerelease, prerelease_count, version_number
-            )
+            self._write_version_to_vmn_version_file(version_number)
 
         if not self.version_backends:
             return
 
-        verstr = stamp_utils.VMNBackend.serialize_vmn_version(
-            version_number,
-            prerelease,
-            prerelease_count,
-            self.hide_zero_hotfix,
-        )
-        verstr = self.get_be_formatted_version(verstr)
         for backend in self.version_backends:
             try:
                 if backend == "vmn_version_file":
                     stamp_utils.VMN_LOGGER.warning(
                         "Remove vmn_version_file version backend from the configuration"
                     )
                     continue
 
                 handler = getattr(self, f"_write_version_to_{backend}")
                 if self.dry_run:
                     stamp_utils.VMN_LOGGER.info(
                         "Would have written to a version backend file:\n"
                         f"backend: {backend}\n"
-                        f"version: {verstr}"
+                        f"version: {version_number}"
                     )
                 else:
-                    handler(verstr)
+                    handler(version_number)
             except AttributeError:
                 stamp_utils.VMN_LOGGER.warning(f"Unsupported version backend {backend}")
                 continue
 
     def _write_version_to_npm(self, verstr):
         backend_conf = self.version_backends["npm"]
         file_path = os.path.join(self.vmn_root_path, backend_conf["path"])
@@ -626,29 +733,50 @@
             stamp_utils.VMN_LOGGER.debug("Exception info: ", exc_info=True)
 
             raise IOError(e)
         except Exception as e:
             stamp_utils.VMN_LOGGER.debug(e, exc_info=True)
             raise RuntimeError(e)
 
-    def _write_version_to_vmn_version_file(
-        self, prerelease, prerelease_count, version_number
-    ):
+    def _write_version_to_generic(self, verstr):
+        backend_conf = self.version_backends["generic"]
+
+        self.current_version_info["stamping"]["app"]["version"] = \
+            stamp_utils.VMNBackend.get_utemplate_formatted_version(
+            self.current_version_info["stamping"]["app"]["_version"],
+                self.template,
+                self.hide_zero_hotfix
+        )
+
+        self.current_version_info["stamping"]["app"]["base_version"] = \
+            stamp_utils.VMNBackend.get_base_vmn_version(
+            self.current_version_info["stamping"]["app"]["_version"],
+            self.hide_zero_hotfix,
+        )
+
+        for item in backend_conf["paths"]:
+            if len(item) == 2:
+                item.append(None)
+
+            tmplt_value = create_data_dict_for_jinja2(
+                self.current_version_info,
+                os.path.join(self.vmn_root_path, item[2]),
+            )
+
+            gen_jinja2_template_from_data(
+                tmplt_value,
+                os.path.join(self.vmn_root_path, item[0]),
+                os.path.join(self.vmn_root_path, item[1]),
+            )
+
+    def _write_version_to_vmn_version_file(self, verstr):
         file_path = self.version_file_path
-        if prerelease is None:
-            prerelease = "release"
-        # this method will write the stamped ver of an app to a file,
-        # weather the file pre exists or not
         try:
             with open(file_path, "w") as fid:
-                ver_dict = {
-                    "version_to_stamp_from": version_number,
-                    "prerelease": prerelease,
-                    "prerelease_count": prerelease_count,
-                }
+                ver_dict = {"version_to_stamp_from": verstr}
                 yaml.dump(ver_dict, fid)
         except IOError as e:
             stamp_utils.VMN_LOGGER.error(f"Error writing ver file: {file_path}\n")
             stamp_utils.VMN_LOGGER.debug("Exception info: ", exc_info=True)
 
             raise IOError(e)
         except Exception as e:
@@ -715,67 +843,51 @@
 
 class VersionControlStamper(IVersionsStamper):
     @stamp_utils.measure_runtime_decorator
     def __init__(self, arg_params):
         IVersionsStamper.__init__(self, arg_params)
 
     @stamp_utils.measure_runtime_decorator
-    def find_matching_version(self, version, prerelease, prerelease_count):
+    def find_matching_version(self, verstr):
         """
         Try to find any version of the application matching the
         user's repositories local state
-        :param version:
-        :param prerelease:
-        :param prerelease_count:
+        :param verstr:
         :return:
         """
 
-        if version is None:
+        if verstr is None:
             return None
 
-        tag_formatted_app_name = stamp_utils.VMNBackend.serialize_vmn_tag_name(
-            self.name,
-            version,
-            self.hide_zero_hotfix,
-            prerelease,
-            prerelease_count,
-        )
-        props = stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag_formatted_app_name)
-        release_tag_formatted_app_name = stamp_utils.VMNBackend.serialize_vmn_tag_name(
-            self.name, props["version"], self.hide_zero_hotfix
-        )
+        tag_formatted_app_name = stamp_utils.VMNBackend.serialize_vmn_tag_name(self.name, verstr)
+        base_verstr = stamp_utils.VMNBackend.get_base_vmn_version(verstr, self.hide_zero_hotfix)
+        release_tag_formatted_app_name = stamp_utils.VMNBackend.serialize_vmn_tag_name(self.name, base_verstr)
 
-        if self.selected_tag != tag_formatted_app_name:
+        if self.selected_tag != tag_formatted_app_name and self.selected_tag != tag_formatted_app_name.rstrip('.'):
             # Get version info for tag
             tag_formatted_app_name, ver_infos = self.backend.get_tag_version_info(
                 tag_formatted_app_name
             )
             if not ver_infos:
                 stamp_utils.VMN_LOGGER.error(
                     f"Failed to get version info for tag: {tag_formatted_app_name}"
                 )
                 return None
+
+            self.enhance_ver_info(ver_infos)
         else:
             ver_infos = self.ver_infos_from_repo
 
         # TODO:: just a sanity? May be removed?
         if (
             tag_formatted_app_name not in ver_infos
             or ver_infos[tag_formatted_app_name] is None
         ):
             return None
 
-        # means we are trying to find a matching version that is in rc state
-        if prerelease_count:
-            # try to check if there is a release version on it
-            for k, v in ver_infos.items():
-                if v is None:
-                    # TODO: WTF?
-                    raise RuntimeError("Bug")
-
         tmp = ver_infos[tag_formatted_app_name]["ver_info"]
         if release_tag_formatted_app_name in ver_infos:
             tmp = ver_infos[release_tag_formatted_app_name]["ver_info"]
 
         # Can happen if app's name is a prefix of another app
         if tmp["stamping"]["app"]["name"] != self.name:
             return None
@@ -801,105 +913,65 @@
                 break
 
         if found:
             return tmp
 
         return None
 
-    @staticmethod
-    @stamp_utils.measure_runtime_decorator
-    def get_version_number_from_file(version_file_path) -> str or None:
-        if not os.path.exists(version_file_path):
-            return (None, None, None)
-
-        with open(version_file_path, "r") as fid:
-            ver_dict = yaml.safe_load(fid)
-            if "version_to_stamp_from" in ver_dict:
-                if "prerelease" not in ver_dict or "prerelease" not in ver_dict:
-                    # Backward for 0.4.0-rc6
-                    return (ver_dict["version_to_stamp_from"], "release", {})
-
-                return (
-                    ver_dict["version_to_stamp_from"],
-                    ver_dict["prerelease"],
-                    ver_dict["prerelease_count"],
-                )
-
-            # Backward compatible vmn 0.3.9 code
-            if "prerelease" not in ver_dict:
-                return (ver_dict["last_stamped_version"], "release", {})
-
-            return (
-                ver_dict["last_stamped_version"],
-                ver_dict["prerelease"],
-                ver_dict["prerelease_count"],
-            )
-
     @stamp_utils.measure_runtime_decorator
     def release_app_version(self, tag_name, ver_info):
         if ver_info is None:
             stamp_utils.VMN_LOGGER.error(
                 f"Tag {tag_name} doesn't seem to exist. Wrong version specified?"
             )
             raise RuntimeError()
 
         tmp = ver_info["stamping"]["app"]
+        base_verstr = stamp_utils.VMNBackend.get_base_vmn_version(
+            tmp["_version"],
+            hide_zero_hotfix=self.hide_zero_hotfix,
+        )
         release_tag_name = stamp_utils.VMNBackend.serialize_vmn_tag_name(
             self.name,
-            tmp["_version"],
-            self.hide_zero_hotfix,
+            base_verstr,
         )
         ver_info["vmn_info"] = self.current_version_info["vmn_info"]
 
-        props = stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag_name)
-        ver_info["stamping"]["app"]["_version"] = props["version"]
+        ver_info["stamping"]["app"]["_version"] = base_verstr
         ver_info["stamping"]["app"][
             "version"
         ] = stamp_utils.VMNBackend.get_utemplate_formatted_version(
-            props["version"], self.template, self.hide_zero_hotfix
+            base_verstr, self.template, self.hide_zero_hotfix
         )
         ver_info["stamping"]["app"]["prerelease"] = "release"
         ver_info["stamping"]["app"]["release_mode"] = "release"
 
         messages = [yaml.dump(ver_info, sort_keys=True)]
 
-        self.backend.tag(
+        ret = self.backend.tag(
             [release_tag_name],
             messages,
             ref=self.backend.changeset(tag=tag_name),
             push=True,
         )
 
-        return props["version"]
+        return base_verstr
 
     @stamp_utils.measure_runtime_decorator
     def add_metadata_to_version(self, tag_name, ver_info):
-        # TODO:: merge logic with release_app_version and
-        #  publish and handle reverting this way
-        if ver_info is None:
-            stamp_utils.VMN_LOGGER.error(
-                f"Tag {tag_name} doesn't seem to exist. Wrong version specified?"
-            )
-            raise RuntimeError()
-
-        tmp = ver_info["stamping"]["app"]
+        props = stamp_utils.VMNBackend.deserialize_tag_name(tag_name)
         res_ver = stamp_utils.VMNBackend.serialize_vmn_version(
-            tmp["_version"],
-            tmp["prerelease"],
-            tmp["prerelease_count"],
-            self.hide_zero_hotfix,
-            self.params["buildmetadata"],
+            props['verstr'],
+            buildmetadata=self.params["buildmetadata"],
+            hide_zero_hotfix=self.hide_zero_hotfix,
         )
+
         buildmetadata_tag_name = stamp_utils.VMNBackend.serialize_vmn_tag_name(
             self.name,
-            tmp["_version"],
-            self.hide_zero_hotfix,
-            tmp["prerelease"],
-            tmp["prerelease_count"],
-            self.params["buildmetadata"],
+            res_ver,
         )
 
         ver_info["vmn_info"] = self.current_version_info["vmn_info"]
         ver_info["stamping"]["app"]["_version"] = res_ver
         ver_info["stamping"]["app"][
             "version"
         ] = stamp_utils.VMNBackend.get_utemplate_formatted_version(
@@ -918,14 +990,17 @@
             with open(path) as f:
                 ver_info["stamping"]["app"]["version_metadata"] = yaml.safe_load(f)
 
         (
             buildmetadata_tag_name,
             tag_ver_infos,
         ) = self.backend.get_tag_version_info(buildmetadata_tag_name)
+
+        self.enhance_ver_info(tag_ver_infos)
+
         if buildmetadata_tag_name in tag_ver_infos:
             if tag_ver_infos[buildmetadata_tag_name]["ver_info"] != ver_info:
                 stamp_utils.VMN_LOGGER.error(
                     f"Tried to add different metadata for the same version."
                 )
                 raise RuntimeError()
 
@@ -939,100 +1014,96 @@
             ref=self.backend.changeset(tag=tag_name),
             push=True,
         )
 
         return res_ver
 
     @stamp_utils.measure_runtime_decorator
-    def stamp_app_version(
-        self, initial_version, initialprerelease, initialprerelease_count
-    ):
+    def stamp_app_version(self, from_verstr):
+        props = stamp_utils.VMNBackend.deserialize_vmn_version(from_verstr)
+        initialprerelease = props['prerelease']
+
         if initialprerelease == "release" and self.release_mode is None:
             stamp_utils.VMN_LOGGER.error(
                 "When not in release candidate mode, "
                 "a release mode must be specified - use "
                 "-r/--release-mode with one of major/minor/patch/hotfix"
             )
             raise RuntimeError()
 
         if initialprerelease != "release" and self.release_mode is None:
+            base_version = stamp_utils.VMNBackend.get_base_vmn_version(
+                from_verstr,
+                hide_zero_hotfix=self.hide_zero_hotfix,
+            )
             release_tag_formatted_app_name = (
                 stamp_utils.VMNBackend.serialize_vmn_tag_name(
-                    self.name, initial_version, self.hide_zero_hotfix
+                    self.name, base_version
                 )
             )
             (
                 release_tag_formatted_app_name,
                 ver_infos,
             ) = self.backend.get_tag_version_info(release_tag_formatted_app_name)
 
+            self.enhance_ver_info(ver_infos)
+
             if (
                 release_tag_formatted_app_name in ver_infos
                 and ver_infos[release_tag_formatted_app_name] is not None
             ):
+                rel_verstr = \
+                    ver_infos[release_tag_formatted_app_name]["ver_info"]["stamping"]["app"]["_version"]
                 stamp_utils.VMN_LOGGER.error(
-                    f"The version {initial_version} was already released. "
+                    f"The version {rel_verstr} was already released. "
                     "Will refuse to stamp prerelease version"
                 )
                 raise RuntimeError()
 
-        current_version, prerelease, prerelease_count = self.gen_advanced_version(
-            initial_version, initialprerelease, initialprerelease_count
-        )
+        current_version, prerelease_count = self.gen_advanced_version(from_verstr)
 
         info = {}
         if self.extra_info:
             info["env"] = dict(os.environ)
 
         release_mode = self.release_mode
-        if prerelease is not None:
-            release_mode = "prerelease"
+        cur_props = stamp_utils.VMNBackend.deserialize_vmn_version(
+            current_version
+        )
 
-        if prerelease is None:
-            prerelease = "release"
+        if cur_props['prerelease'] != 'release':
+            release_mode = "prerelease"
 
         self.update_stamping_info(
             info,
-            initial_version,
-            initialprerelease,
-            initialprerelease_count,
+            from_verstr,
             current_version,
-            prerelease,
-            prerelease_count,
             release_mode,
+            prerelease_count,
         )
 
-        return current_version, prerelease, prerelease_count
+        return current_version
 
     @stamp_utils.measure_runtime_decorator
     def update_stamping_info(
         self,
         info,
         initial_version,
-        initialprerelease,
-        initialprerelease_count,
         current_version,
-        prerelease,
-        prerelease_count,
         release_mode,
+        prerelease_count,
     ):
-        verstr = stamp_utils.VMNBackend.serialize_vmn_version(
-            current_version, prerelease, prerelease_count, self.hide_zero_hotfix
-        )
-        self.current_version_info["stamping"]["app"]["_version"] = verstr
-        self.current_version_info["stamping"]["app"]["prerelease"] = prerelease
-        initial_verstr = stamp_utils.VMNBackend.serialize_vmn_version(
-            initial_version,
-            initialprerelease,
-            initialprerelease_count,
-            self.hide_zero_hotfix,
-        )
+        props = stamp_utils.VMNBackend.deserialize_vmn_version(current_version)
+
+        self.current_version_info["stamping"]["app"]["_version"] = current_version
+        self.current_version_info["stamping"]["app"]["prerelease"] = props['prerelease']
+
         self.current_version_info["stamping"]["app"][
             "previous_version"
-        ] = initial_verstr
+        ] = initial_version
         self.current_version_info["stamping"]["app"]["release_mode"] = release_mode
         self.current_version_info["stamping"]["app"]["info"] = copy.deepcopy(info)
         self.current_version_info["stamping"]["app"][
             "stamped_on_branch"
         ] = self.backend.active_branch
         self.current_version_info["stamping"]["app"][
             "stamped_on_remote_branch"
@@ -1042,20 +1113,22 @@
         ] = copy.deepcopy(prerelease_count)
 
     @stamp_utils.measure_runtime_decorator
     def stamp_root_app_version(self, override_version=None):
         if self.root_app_name is None:
             return None
 
-        tag_name, ver_infos = self.backend.get_first_reachable_version_info(
+        tag_name, ver_infos = self.get_first_reachable_version_info(
             self.root_app_name,
             root_context=True,
             type=stamp_utils.RELATIVE_TO_CURRENT_VCS_POSITION_TYPE,
         )
 
+        self.enhance_ver_info(ver_infos)
+
         if tag_name not in ver_infos or ver_infos[tag_name]["ver_info"] is None:
             stamp_utils.VMN_LOGGER.error(
                 f"Version information for {self.root_app_name} was not found"
             )
             raise RuntimeError()
 
         # TODO: think about this case
@@ -1103,45 +1176,43 @@
             if path in changed or path in untracked:
                 version_files.append(path)
 
         return version_files
 
     @stamp_utils.measure_runtime_decorator
     def publish_stamp(
-        self, app_version, prerelease, prerelease_count, root_app_version
+        self, app_version, root_app_version
     ):
-        verstr = stamp_utils.VMNBackend.serialize_vmn_version(
-            app_version,
-            prerelease,
-            prerelease_count,
-            self.hide_zero_hotfix,
-        )
         app_msg = {
             "vmn_info": self.current_version_info["vmn_info"],
             "stamping": {"app": self.current_version_info["stamping"]["app"]},
         }
 
         if not self.should_publish:
             return 0
 
-        self.write_version_to_file(
-            version_number=app_version,
-            prerelease=prerelease,
-            prerelease_count=prerelease_count,
-        )
+        self.write_version_to_file(version_number=app_version)
 
         version_files_to_add = self.get_files_to_add_to_index(self.version_files)
 
         for backend in self.version_backends:
             backend_conf = self.version_backends[backend]
+            if backend == "generic":
+                for item in backend_conf["paths"]:
+                    for p in item:
+                        file_path = os.path.join(self.vmn_root_path, p)
+                        version_files_to_add.append(file_path)
+
+                continue
+
             file_path = os.path.join(self.vmn_root_path, backend_conf["path"])
             version_files_to_add.append(file_path)
 
         if self.create_verinfo_files:
-            self.create_verinfo_file(app_msg, version_files_to_add, verstr)
+            self.create_verinfo_file(app_msg, version_files_to_add, app_version)
 
         if self.root_app_name is not None:
             root_app_msg = {
                 "stamping": {
                     "root_app": self.current_version_info["stamping"]["root_app"]
                 },
                 "vmn_info": self.current_version_info["vmn_info"],
@@ -1154,19 +1225,19 @@
             if self.create_verinfo_files:
                 self.create_verinfo_root_file(
                     root_app_msg, root_app_version, version_files_to_add
                 )
 
         commit_msg = None
         if self.current_version_info["stamping"]["app"]["release_mode"] == "init":
-            commit_msg = f"{self.name}: Stamped initial version {verstr}\n\n"
+            commit_msg = f"{self.name}: Stamped initial version {app_version}\n\n"
         else:
             extra_commit_message = self.params["extra_commit_message"]
             commit_msg = (
-                f"{self.name}: Stamped version {verstr}\n{extra_commit_message}\n"
+                f"{self.name}: Stamped version {app_version}\n{extra_commit_message}\n"
             )
 
         self.current_version_info["stamping"]["msg"] = commit_msg
 
         prev_changeset = self.backend.changeset()
 
         try:
@@ -1178,15 +1249,15 @@
                 stamp_utils.VMN_LOGGER.info(f"Would have tried to revert a vmn commit")
             else:
                 self.backend.revert_vmn_commit(prev_changeset, self.version_files)
 
             # TODO:: turn to error codes. This one means - exit without retries
             return 3
 
-        tag = f'{self.name.replace("/", "-")}_{verstr}'
+        tag = f'{self.name.replace("/", "-")}_{app_version}'
         match = re.search(stamp_utils.VMN_TAG_REGEX, tag)
         if match is None:
             stamp_utils.VMN_LOGGER.error(
                 f"Tag {tag} doesn't comply to vmn version format"
                 f"Reverting vmn changes ..."
             )
             if self.dry_run:
@@ -1264,15 +1335,15 @@
                     res = self.backend.check_for_outgoing_changes()
 
                 if count == 5 and res:
                     raise RuntimeError(
                         f"BUG: Somehow we have outgoing changes right "
                         f"after publishing:\n{res}"
                     )
-        except Exception:
+        except Exception as exc:
             stamp_utils.VMN_LOGGER.debug("Logged Exception message:", exc_info=True)
             stamp_utils.VMN_LOGGER.info(f"Reverting vmn changes for tags: {tags} ...")
             if self.dry_run:
                 stamp_utils.VMN_LOGGER.info(
                     f"Would have reverted vmn commit and delete tags:\n{all_tags}"
                 )
             else:
@@ -1294,23 +1365,23 @@
         list_of_files = glob.glob(path)
         branch_conf_path = os.path.join(self.app_dir_path, f"{cur_branch}_conf.yml")
 
         if self.dry_run:
             if list_of_files:
                 stamp_utils.VMN_LOGGER.info(
                     "Would have removed config files:\n"
-                    f"{set(list_of_files) - set([branch_conf_path])}"
+                    f"{set(list_of_files) - {branch_conf_path} }"
                 )
 
             stamp_utils.VMN_LOGGER.info(
                 "Would have created commit with message:\n"
                 f'{self.current_version_info["stamping"]["msg"]}'
             )
         else:
-            for f in set(list_of_files) - set([branch_conf_path]):
+            for f in set(list_of_files) - {branch_conf_path}:
                 try:
                     self.backend._be.index.remove([f], working_tree=True)
                 except Exception as exc:
                     pass
 
                 try:
                     f_to_rem = pathlib.Path(f)
@@ -1363,15 +1434,14 @@
 
             version_files_to_add.append(path)
 
     @stamp_utils.measure_runtime_decorator
     def retrieve_remote_changes(self):
         self.backend.pull()
 
-
 @stamp_utils.measure_runtime_decorator
 def handle_init(vmn_ctx):
     expected_status = {"repos_exist_locally"}
     optional_status = {"deps_synced_with_conf"}
 
     status = _get_repo_status(vmn_ctx.vcs, expected_status, optional_status)
     if status["error"]:
@@ -1444,27 +1514,26 @@
     # For backward compatibility
     if vmn_ctx.vcs.release_mode == "micro":
         vmn_ctx.vcs.release_mode = "hotfix"
 
     assert vmn_ctx.vcs.release_mode is None or vmn_ctx.vcs.optional_release_mode is None
 
     if vmn_ctx.vcs.override_version is not None:
-        match = re.search(stamp_utils.VMN_REGEX, vmn_ctx.vcs.override_version)
-
-        if match is None:
+        try:
+            props = stamp_utils.VMNBackend.deserialize_vmn_version(vmn_ctx.vcs.override_version)
+        except Exception as exc:
             err = (
                 f"Provided override {vmn_ctx.vcs.override_version} doesn't comply with: "
                 f"{stamp_utils.VMN_VERSION_FORMAT} format")
             stamp_utils.VMN_LOGGER.error(err)
 
             raise RuntimeError(err)
 
-        gdict = match.groupdict()
-        assert gdict["prerelease"] is None
-        assert gdict["buildmetadata"] is None
+        assert props["prerelease"] == "release"
+        assert props["buildmetadata"] is None
 
     optional_status = {"modified", "detached"}
     expected_status = {
         "repos_exist_locally",
         "repo_tracked",
         "app_tracked",
         "deps_synced_with_conf",
@@ -1477,19 +1546,18 @@
         )
 
         return 1
 
     if status["matched_version_info"] is not None:
         # Good we have found an existing version matching
         # the actual_deps_state
-        version = vmn_ctx.vcs.get_be_formatted_version(
-            status["matched_version_info"]["stamping"]["app"]["_version"]
-        )
+        version = status["matched_version_info"]["stamping"]["app"]["_version"]
 
-        stamp_utils.VMN_LOGGER.info(version)
+        disp_version = vmn_ctx.vcs.get_be_formatted_version(version)
+        stamp_utils.VMN_LOGGER.info(disp_version)
 
         return 0
 
     if "detached" in status["state"]:
         stamp_utils.VMN_LOGGER.error("In detached head. Will not stamp new version")
         return 1
 
@@ -1504,60 +1572,59 @@
             stamp_utils.VMN_LOGGER.error(
                 "Failed to pull, run with --debug for more details"
             )
             stamp_utils.VMN_LOGGER.debug("Logged Exception message:", exc_info=True)
 
             return 1
 
-    (
-        initial_version,
-        prerelease,
-        prerelease_count,
-    ) = VersionControlStamper.get_version_number_from_file(
+    initial_version = vmn_ctx.vcs.get_version_number_from_file(
         vmn_ctx.vcs.version_file_path
     )
 
     is_release = vmn_ctx.vcs.ver_infos_from_repo[vmn_ctx.vcs.selected_tag]["ver_info"]["stamping"]["app"][
                      "prerelease"] == "release"
 
     if vmn_ctx.vcs.override_version:
+        # TODO:: support version with rc here and check with regex.
         initial_version = vmn_ctx.vcs.override_version
-        prerelease = 'release'
-        prerelease_count = {}
         is_release = True
 
     if vmn_ctx.vcs.optional_release_mode and is_release:
-        verstr = vmn_ctx.vcs.advance_version(initial_version, vmn_ctx.vcs.optional_release_mode, globally=False)
-        tag_name_prefix = f'{vmn_ctx.vcs.name.replace("/", "-")}_{verstr}*'
+        verstr, _ = vmn_ctx.vcs.advance_version(
+            initial_version,
+            vmn_ctx.vcs.optional_release_mode,
+            globally=False
+        )
+        base_verstr = stamp_utils.VMNBackend.get_base_vmn_version(
+            verstr,
+            hide_zero_hotfix=vmn_ctx.vcs.hide_zero_hotfix
+        )
+        tag_name_prefix = f"{stamp_utils.VMNBackend.serialize_vmn_tag_name(vmn_ctx.vcs.name, base_verstr)}*"
         tag = vmn_ctx.vcs.backend.get_latest_available_tag(tag_name_prefix)
         if tag is not None and len(tag) < len(tag_name_prefix):
             tag = None
 
         if not tag:
             vmn_ctx.vcs.release_mode = vmn_ctx.vcs.optional_release_mode
         else:
             props = stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag)
 
-            (_, temp_ver_infos_from_repo) = vmn_ctx.vcs.get_version_info_from_verstr(
-                f"{props['version']}-{props['prerelease']}")
+            (_, temp_ver_infos_from_repo) = vmn_ctx.vcs.get_version_info_from_verstr(f"{props['verstr']}")
 
             vmn_ctx.vcs.ver_infos_from_repo[vmn_ctx.vcs.selected_tag]["ver_info"]["stamping"]["app"]["_version"] = \
                 temp_ver_infos_from_repo[tag]["ver_info"]["stamping"]["app"]["_version"]
             vmn_ctx.vcs.ver_infos_from_repo[vmn_ctx.vcs.selected_tag]["ver_info"]["stamping"]["app"]["prerelease"] = \
                 temp_ver_infos_from_repo[tag]["ver_info"]["stamping"]["app"]["prerelease"]
             vmn_ctx.vcs.ver_infos_from_repo[vmn_ctx.vcs.selected_tag]["ver_info"]["stamping"]["app"][
                 "prerelease_count"] = \
                 temp_ver_infos_from_repo[tag]["ver_info"]["stamping"]["app"]["prerelease_count"]
             vmn_ctx.vcs.ver_infos_from_repo[vmn_ctx.vcs.selected_tag]["ver_info"]["stamping"]["app"]["release_mode"] = \
                 temp_ver_infos_from_repo[tag]["ver_info"]["stamping"]["app"]["release_mode"]
 
             initial_version = verstr
-            if prerelease == "release":
-                prerelease = temp_ver_infos_from_repo[tag]["ver_info"]["stamping"]["app"]["prerelease"]
-                prerelease_count = temp_ver_infos_from_repo[tag]["ver_info"]["stamping"]["app"]["prerelease_count"]
 
     if vmn_ctx.vcs.tracked and vmn_ctx.vcs.release_mode is None:
         vmn_ctx.vcs.current_version_info["stamping"]["app"][
             "release_mode"
         ] = vmn_ctx.vcs.ver_infos_from_repo[vmn_ctx.vcs.selected_tag]["ver_info"][
             "stamping"
         ][
@@ -1568,26 +1635,25 @@
 
     try:
         version = _stamp_version(
             vmn_ctx.vcs,
             vmn_ctx.args.pull,
             vmn_ctx.args.check_vmn_version,
             initial_version,
-            prerelease,
-            prerelease_count,
         )
     except Exception as exc:
         stamp_utils.VMN_LOGGER.debug("Logged Exception message:", exc_info=True)
 
         return 1
 
+    disp_version = vmn_ctx.vcs.get_be_formatted_version(version)
     if vmn_ctx.vcs.dry_run:
-        stamp_utils.VMN_LOGGER.info(f"Would have stamped {version}")
+        stamp_utils.VMN_LOGGER.info(f"Would have stamped {disp_version}")
     else:
-        stamp_utils.VMN_LOGGER.info(f"{version}")
+        stamp_utils.VMN_LOGGER.info(f"{disp_version}")
 
     return 0
 
 
 @stamp_utils.measure_runtime_decorator
 def handle_release(vmn_ctx):
     expected_status = {"repos_exist_locally", "repo_tracked", "app_tracked"}
@@ -1600,31 +1666,27 @@
         )
 
         return 1
 
     ver = vmn_ctx.args.version
 
     if ver:
-        # TODO:: extract method
-        match = re.search(stamp_utils.VMN_REGEX, ver)
-        res = match.groupdict()
-        if res["buildmetadata"]:
+        props = stamp_utils.VMNBackend.deserialize_vmn_version(ver)
+        if props["buildmetadata"] is not None:
             stamp_utils.VMN_LOGGER.error(
                 f"Failed to release {ver}. "
                 f"Releasing metadata versions is not supported"
             )
 
             return 1
 
     if ver is None and status["matched_version_info"] is not None:
         # Good we have found an existing version matching
         # the actual_deps_state
-        ver = vmn_ctx.vcs.get_be_formatted_version(
-            status["matched_version_info"]["stamping"]["app"]["_version"]
-        )
+        ver = status["matched_version_info"]["stamping"]["app"]["_version"]
     elif ver is None:
         stamp_utils.VMN_LOGGER.error(
             "When running vmn release and not on a version commit, "
             "you must specify a specific version using -v flag"
         )
 
         return 1
@@ -1640,15 +1702,14 @@
             ver,
             vmn_ctx.vcs.hide_zero_hotfix,
         )
 
         tag_formatted_app_name = stamp_utils.VMNBackend.serialize_vmn_tag_name(
             vmn_ctx.vcs.name,
             base_ver,
-            vmn_ctx.vcs.hide_zero_hotfix,
         )
 
         if tag_formatted_app_name in ver_infos:
             stamp_utils.VMN_LOGGER.info(base_ver)
             return 0
 
         stamp_utils.VMN_LOGGER.info(vmn_ctx.vcs.release_app_version(tag_name, ver_info))
@@ -1677,31 +1738,27 @@
         )
 
         return 1
 
     ver = vmn_ctx.args.version
 
     if ver:
-        # TODO:: extract method
-        match = re.search(stamp_utils.VMN_REGEX, ver)
-        res = match.groupdict()
-        if res["buildmetadata"]:
+        props = stamp_utils.VMNBackend.deserialize_vmn_version(ver)
+        if props["buildmetadata"] is not None:
             stamp_utils.VMN_LOGGER.error(
                 f"Failed to add to {ver}. "
                 f"Adding metadata versions to metadata versions is not supported"
             )
 
             return 1
 
     if ver is None and status["matched_version_info"] is not None:
         # Good we have found an existing version matching
         # the actual_deps_state
-        ver = vmn_ctx.vcs.get_be_formatted_version(
-            status["matched_version_info"]["stamping"]["app"]["_version"]
-        )
+        ver = status["matched_version_info"]["stamping"]["app"]["_version"]
     elif ver is None:
         stamp_utils.VMN_LOGGER.error(
             "When running vmn add and not on a version commit, "
             "you must specify a specific version using -v flag"
         )
 
         return 1
@@ -1867,22 +1924,16 @@
             # Outgoing changes cannot be in detached head
             # TODO: is it really?
             status["outgoing"] = True
             status["err_msgs"]["outgoing"] = err
             status["state"].add("outgoing")
 
     if "name" in vcs.current_version_info["stamping"]["app"]:
-        (
-            initial_version,
-            prerelease,
-            prerelease_count,
-        ) = VersionControlStamper.get_version_number_from_file(vcs.version_file_path)
-        matched_version_info = vcs.find_matching_version(
-            initial_version, prerelease, prerelease_count
-        )
+        verstr = vcs.get_version_number_from_file(vcs.version_file_path)
+        matched_version_info = vcs.find_matching_version(verstr)
         if matched_version_info is None:
             status["modified"] = True
             status["state"].add("modified")
         else:
             status["matched_version_info"] = matched_version_info
 
         configured_repos = set(vcs.configured_deps.keys())
@@ -1911,16 +1962,16 @@
 
             status["repos"][repo] = copy.deepcopy(default_status)
             full_path = os.path.join(vcs.vmn_root_path, repo)
 
             dep_be, err = stamp_utils.get_client(full_path, vcs.be_type)
             if err:
                 err_str = "Failed to create backend {0}. Exiting".format(err)
-                stamp_utils.VMN_LOGGER.error(err)
-                raise RuntimeError(err)
+                stamp_utils.VMN_LOGGER.error(err_str)
+                raise RuntimeError(err_str)
 
             err = dep_be.check_for_pending_changes()
             if err:
                 status["dirty_deps"] = True
                 status["err_msgs"][
                     "dirty_deps"
                 ] = f"{status['err_msgs']['dirty_deps']}\n{err}"
@@ -2040,27 +2091,30 @@
 
         return 1
 
     versions_be_ifc.create_config_files()
 
     info = {}
     versions_be_ifc.update_stamping_info(
-        info, starting_version, "release", {}, starting_version, "release", {}, "init"
+        info, starting_version, starting_version, "init", {}
     )
 
     versions_be_ifc.backend.perform_cached_fetch()
 
     root_app_version = 0
     services = {}
     if versions_be_ifc.root_app_name is not None:
-        tag_name, ver_infos = versions_be_ifc.backend.get_first_reachable_version_info(
+        tag_name, ver_infos = versions_be_ifc.get_first_reachable_version_info(
             versions_be_ifc.root_app_name,
             root_context=True,
             type=stamp_utils.RELATIVE_TO_GLOBAL_TYPE,
         )
+
+        versions_be_ifc.enhance_ver_info(ver_infos)
+
         if tag_name in ver_infos and ver_infos[tag_name]["ver_info"]:
             root_app_version = (
                 int(ver_infos[tag_name]["ver_info"]["stamping"]["root_app"]["version"])
                 + 1
             )
             root_app = ver_infos[tag_name]["ver_info"]["stamping"]["root_app"]
             services = copy.deepcopy(root_app["services"])
@@ -2074,15 +2128,15 @@
 
         msg_root_app = versions_be_ifc.current_version_info["stamping"]["root_app"]
         msg_app = versions_be_ifc.current_version_info["stamping"]["app"]
         msg_root_app["services"][versions_be_ifc.name] = msg_app["_version"]
 
     try:
         err = versions_be_ifc.publish_stamp(
-            starting_version, "release", {}, root_app_version
+            starting_version, root_app_version
         )
     except Exception as exc:
         stamp_utils.VMN_LOGGER.debug("Logged Exception message: ", exc_info=True)
         versions_be_ifc.backend.revert_local_changes(versions_be_ifc.version_files)
         err = -1
 
     if err:
@@ -2093,23 +2147,20 @@
 
 
 @stamp_utils.measure_runtime_decorator
 def _stamp_version(
     versions_be_ifc,
     pull,
     check_vmn_version,
-    initial_version,
-    initialprerelease,
-    initialprerelease_count,
+    verstr
 ):
     stamped = False
     retries = 3
-    override_initial_version = initial_version
-    override_initialprerelease = initialprerelease
-    override_initialprerelease_count = initialprerelease_count
+    override_verstr = verstr
+
     override_main_current_version = versions_be_ifc.override_root_version
 
     if check_vmn_version:
         newer_stamping = version_mod.version != "0.0.0" and (
             pversion.parse(
                 versions_be_ifc.current_version_info["vmn_info"]["vmn_version"]
             )
@@ -2124,55 +2175,46 @@
 
     if versions_be_ifc.bad_format_template:
         stamp_utils.VMN_LOGGER.warning(versions_be_ifc.template_err_str)
 
     while retries:
         retries -= 1
 
-        (
-            current_version,
-            prerelease,
-            prerelease_count,
-        ) = versions_be_ifc.stamp_app_version(
-            override_initial_version,
-            override_initialprerelease,
-            override_initialprerelease_count,
+        current_version = versions_be_ifc.stamp_app_version(
+            override_verstr
         )
         main_ver = versions_be_ifc.stamp_root_app_version(override_main_current_version)
 
         try:
             err = versions_be_ifc.publish_stamp(
-                current_version, prerelease, prerelease_count, main_ver
+                current_version, main_ver
             )
         except Exception as exc:
             stamp_utils.VMN_LOGGER.error(
                 f"Failed to publish. Will revert local changes {exc}\nFor more details use --debug"
             )
             stamp_utils.VMN_LOGGER.debug("Exception info: ", exc_info=True)
             versions_be_ifc.backend.revert_local_changes(versions_be_ifc.version_files)
             err = -1
 
         if not err:
             stamped = True
             break
 
         if err == 1:
-            override_initial_version = current_version
-            override_initialprerelease = prerelease
-            override_initialprerelease_count = prerelease_count
+            override_verstr = current_version
+
             override_main_current_version = main_ver
 
             stamp_utils.VMN_LOGGER.warning(
                 "Failed to publish. Will try to auto-increase "
                 "from {0} to {1}".format(
                     current_version,
                     versions_be_ifc.gen_advanced_version(
-                        override_initial_version,
-                        override_initialprerelease,
-                        override_initialprerelease_count,
+                        override_verstr
                     )[0],
                 )
             )
         elif err == 2:
             if not pull:
                 break
 
@@ -2185,19 +2227,15 @@
             break
 
     if not stamped:
         err = "Failed to stamp"
         stamp_utils.VMN_LOGGER.error(err)
         raise RuntimeError(err)
 
-    verstr = stamp_utils.VMNBackend.serialize_vmn_version(
-        current_version, prerelease, prerelease_count, versions_be_ifc.hide_zero_hotfix
-    )
-
-    return versions_be_ifc.get_be_formatted_version(verstr)
+    return current_version
 
 
 @stamp_utils.measure_runtime_decorator
 def show(vcs, params, verstr=None):
     dirty_states = None
     ver_infos = vcs.ver_infos_from_repo
     tag_name = vcs.selected_tag
@@ -2258,41 +2296,47 @@
             "version_backends": copy.deepcopy(vcs.version_backends),
         }
 
     if params.get("display_type"):
         data["type"] = ver_info["stamping"]["app"]["prerelease"]
 
     if vcs.root_context:
-        data.update(ver_info["stamping"]["root_app"])
-        if not data:
-            stamp_utils.VMN_LOGGER.info(
-                "App {0} does not have a root app ".format(vcs.name)
+        if "root_app" not in ver_info["stamping"]:
+            err_str = f"App {vcs.name} does not have a root app"
+            stamp_utils.VMN_LOGGER.error(
+                err_str
             )
 
             raise RuntimeError()
 
+        data.update(ver_info["stamping"]["root_app"])
+
         out = None
         if params.get("verbose"):
             out = yaml.dump(data)
         else:
             out = data["version"]
 
         if dirty_states:
             out = yaml.dump(dirty_states)
 
         print(out)
 
         return 0
 
     data.update(ver_info["stamping"]["app"])
+
+    props = stamp_utils.VMNBackend.deserialize_vmn_tag_name(tag_name)
+    verstr = props['verstr']
+
     data["version"] = stamp_utils.VMNBackend.get_utemplate_formatted_version(
-        data["_version"], vcs.template, vcs.hide_zero_hotfix
+        verstr, vcs.template, vcs.hide_zero_hotfix
     )
     data["unique_id"] = stamp_utils.VMNBackend.gen_unique_id(
-        data["_version"], data["changesets"]["."]["hash"]
+        verstr, data["changesets"]["."]["hash"]
     )
 
     if params.get("verbose"):
         if dirty_states:
             data["dirty"] = dirty_states
         out = yaml.dump(data)
     else:
@@ -2391,14 +2435,17 @@
                 f"The repository is not exactly at version: {verstr}. "
                 f"You can use `vmn goto` in order to jump to that version.\n"
                 f"Refusing to gen."
             )
             raise RuntimeError()
 
     data = ver_infos[tag_name]["ver_info"]["stamping"]["app"]
+
+    # With verstr given, we know the supposed to be deps states.
+    # If no verstr given, learn the actual deps state
     if verstr is None:
         data["changesets"] = {}
 
         for k, v in vcs.configured_deps.items():
             if k not in vcs.actual_deps_state:
                 stamp_utils.VMN_LOGGER.error(
                     f"{k} doesn't exist locally. Use vmn goto and rerun"
@@ -2413,50 +2460,67 @@
             elif vcs.repo_name == k:
                 data["changesets"][k]["state"] = dirty_states
 
     data["version"] = stamp_utils.VMNBackend.get_utemplate_formatted_version(
         data["_version"], vcs.template, vcs.hide_zero_hotfix
     )
 
-    tmplt_value = {}
-    tmplt_value.update(data)
-    tmplt_value["base_version"] = stamp_utils.VMNBackend.get_base_vmn_version(
+    data["base_version"] = stamp_utils.VMNBackend.get_base_vmn_version(
         data["_version"],
         vcs.hide_zero_hotfix,
     )
-    if "root_app" in ver_infos[tag_name]["ver_info"]["stamping"]:
-        for key, v in ver_infos[tag_name]["ver_info"]["stamping"]["root_app"].items():
-            tmplt_value[f"root_{key}"] = v
 
-    if params["custom_values"] is not None:
-        with open(params["custom_values"], "r") as f:
+    tmplt_value = create_data_dict_for_jinja2(
+        ver_infos[tag_name]["ver_info"],
+        params["custom_values"],
+    )
+
+    gen_jinja2_template_from_data(
+        tmplt_value,
+        params["jinja_template"],
+        params["output"],
+    )
+
+    return 0
+
+
+def create_data_dict_for_jinja2(ver_info, custom_values_path):
+    tmplt_value = {}
+    tmplt_value.update(ver_info["stamping"]["app"])
+
+    if custom_values_path is not None:
+        with open(custom_values_path, "r") as f:
             ret = yaml.safe_load(f)
             tmplt_value.update(ret)
 
-    with open(params["jinja_template"]) as file_:
+    if "root_app" in ver_info["stamping"]:
+        for key, v in ver_info["stamping"]["root_app"].items():
+            tmplt_value[f"root_{key}"] = v
+
+    return tmplt_value
+
+
+def gen_jinja2_template_from_data(data, jinja_template_path, output_path):
+    with open(jinja_template_path) as file_:
         template = jinja2.Template(file_.read())
 
     stamp_utils.VMN_LOGGER.debug(
-        f"Possible keywords for your Jinja template:\n" f"{pformat(tmplt_value)}"
+        f"Possible keywords for your Jinja template:\n" f"{pformat(data)}"
     )
-    out = template.render(tmplt_value)
-
-    out_path = params["output"]
+    out = template.render(data)
 
-    if os.path.exists(out_path):
-        with open(out_path) as file_:
+    if os.path.exists(output_path):
+        with open(output_path) as file_:
             current_out_content = file_.read()
             if current_out_content == out:
                 return 0
 
-    with open(out_path, "w") as f:
+    with open(output_path, "w") as f:
         f.write(out)
 
-    return 0
-
 
 def get_dirty_states(optional_status, status):
     dirty_states = (optional_status & status["state"]) | {
         "repos_exist_locally",
         "detached",
     }
     dirty_states -= {"detached", "repos_exist_locally", "deps_synced_with_conf"}
@@ -2502,17 +2566,20 @@
 
                 ret = vcs.backend.checkout_branch()
                 assert ret is not None
 
             del vcs
             vcs = VersionControlStamper(params)
 
-        tag_name, ver_infos = vcs.backend.get_first_reachable_version_info(
+        tag_name, ver_infos = vcs.get_first_reachable_version_info(
             vcs.name, vcs.root_context, stamp_utils.RELATIVE_TO_CURRENT_VCS_BRANCH_TYPE
         )
+
+        vcs.enhance_ver_info(ver_infos)
+
         if tag_name not in ver_infos or ver_infos[tag_name]["ver_info"] is None:
             stamp_utils.VMN_LOGGER.error(f"No such app: {vcs.name}")
             return 1
 
         data = ver_infos[tag_name]["ver_info"]["stamping"]["app"]
         deps = copy.deepcopy(vcs.configured_deps)
 
@@ -2712,16 +2779,16 @@
 
     stamp_utils.VMN_LOGGER.info("Cloning {0}..".format(rel_path))
     try:
         if vcs_type == "git":
             stamp_utils.GitBackend.clone(path, remote)
     except Exception as exc:
         try:
-            str = "already exists and is not an empty directory."
-            if str in exc.stderr:
+            s = "already exists and is not an empty directory."
+            if s in str(exc):
                 return {"repo": rel_path, "status": 0, "description": None}
         except Exception:
             pass
 
         err = "Failed to clone {0} repository. " "Description: {1}".format(
             rel_path, exc.args
         )
@@ -2941,16 +3008,16 @@
 
             for repo in common_deps:
                 full_path = os.path.join(vmnc.vcs.vmn_root_path, repo)
 
                 dep_be, err = stamp_utils.get_client(full_path, vmnc.vcs.be_type)
                 if err:
                     err_str = "Failed to create backend {0}. Exiting".format(err)
-                    stamp_utils.VMN_LOGGER.error(err)
-                    raise RuntimeError(err)
+                    stamp_utils.VMN_LOGGER.error(err_str)
+                    raise RuntimeError(err_str)
 
                 dep_be.prepare_for_remote_operation()
                 del dep_be
 
     cmd = vmnc.args.command.replace("-", "_")
     err = getattr(sys.modules[__name__], f"handle_{cmd}")(vmnc)
 
@@ -3086,15 +3153,15 @@
         help="Override current root version with any integer of your choice",
     )
     pstamp.add_argument(
         "--ov",
         "--override-version",
         default=None,
         help=f"Override current version with any version in the "
-        f"format: {stamp_utils.VMN_VER_REGEX}",
+        f"format: {stamp_utils.VMN_BASE_VER_REGEX}",
     )
     pstamp.add_argument("--dry-run", dest="dry", action="store_true")
     pstamp.set_defaults(dry=False)
     pstamp.add_argument("name", help="The application's name")
     pstamp.add_argument(
         "-e",
         "--extra-commit-message",
@@ -3200,24 +3267,17 @@
     padd.add_argument("name", help="The application's name")
 
 
 def verify_user_input_version(args, key):
     if key not in args or getattr(args, key) is None:
         return
 
-    if key == "ov":
-        match = re.search(stamp_utils.VMN_VER_REGEX, getattr(args, key))
-    elif key == "orv":
-        match = re.search(stamp_utils.VMN_ROOT_REGEX, getattr(args, key))
-    elif "root" not in args or not args.root:
-        match = re.search(stamp_utils.VMN_REGEX, getattr(args, key))
-    else:
-        match = re.search(stamp_utils.VMN_ROOT_REGEX, getattr(args, key))
-
-    if match is None:
+    try:
+        props = stamp_utils.VMNBackend.deserialize_vmn_version(getattr(args, key))
+    except Exception as exc:
         if "root" not in args or not args.root:
             err = f"Version must be in format: {stamp_utils.VMN_VERSION_FORMAT}"
         else:
             err = f"Root version must be an integer"
 
         stamp_utils.VMN_LOGGER.error(err)
```

## Comparing `vmn-0.8.5rc2.dist-info/LICENSE.txt` & `vmn-0.8.5rc3.dist-info/LICENSE.txt`

 * *Files identical despite different names*

## Comparing `vmn-0.8.5rc2.dist-info/RECORD` & `vmn-0.8.5rc3.dist-info/RECORD`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 version_stamp/__init__.py,sha256=p_9bnBNpi1jHdKDsmBM7tN2Da3N-QOYEe8s09k9NIrk,152
-version_stamp/stamp_utils.py,sha256=-YavcLjR97hx7kXLQPxeZsz1Giv4YFV5bhZcBfrPD00,53186
-version_stamp/version.py,sha256=1f9Ei11VfuhHJctopm0T6YkYXvm6Oz6xdjpdBkYTEk0,58
-version_stamp/vmn.py,sha256=gZSfXOIz96ru49yc1a1m-k7iHYEaJXI67MunvBX_Fp4,113063
-vmn-0.8.5rc2.dist-info/LICENSE.txt,sha256=f6flbA23EQX0tZpqCsQCJesFmHb4XNOAOD99egZuaL4,35127
-vmn-0.8.5rc2.dist-info/METADATA,sha256=mfKE7aeFPFOxMJeCtWYt_A1F7WQNoVF7sGBvJcpj8bs,470
-vmn-0.8.5rc2.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
-vmn-0.8.5rc2.dist-info/entry_points.txt,sha256=8JQYxf_iGN3GSYg7ezJs-P8FM3Ss6Hspgg6QcV_s3uk,47
-vmn-0.8.5rc2.dist-info/top_level.txt,sha256=nVR6dU2EinKSe5A4ZJa7NR1aOPNV7QMXvB5Sm-rWbJs,14
-vmn-0.8.5rc2.dist-info/RECORD,,
+version_stamp/stamp_utils.py,sha256=Znboranu42S-f60D53QVL3NtrPk-75KMwvr-skSw8hg,55785
+version_stamp/version.py,sha256=sKF2QOGioz10_G7x1Ni6Qt2_7ZOTVN6l7hKPuH06Low,60
+version_stamp/vmn.py,sha256=BhUcPWrpyk0UQ0p2YCxBkhR0PDEDVbfIBRZqClAwL_s,114266
+vmn-0.8.5rc3.dist-info/LICENSE.txt,sha256=f6flbA23EQX0tZpqCsQCJesFmHb4XNOAOD99egZuaL4,35127
+vmn-0.8.5rc3.dist-info/METADATA,sha256=l1iK7-PvMHVg_ofVxrrU_gGUdmT0alRzIvS_JhC5seY,470
+vmn-0.8.5rc3.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
+vmn-0.8.5rc3.dist-info/entry_points.txt,sha256=8JQYxf_iGN3GSYg7ezJs-P8FM3Ss6Hspgg6QcV_s3uk,47
+vmn-0.8.5rc3.dist-info/top_level.txt,sha256=nVR6dU2EinKSe5A4ZJa7NR1aOPNV7QMXvB5Sm-rWbJs,14
+vmn-0.8.5rc3.dist-info/RECORD,,
```

