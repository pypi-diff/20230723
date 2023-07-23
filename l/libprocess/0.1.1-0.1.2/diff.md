# Comparing `tmp/libprocess-0.1.1.tar.gz` & `tmp/libprocess-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "libprocess-0.1.1.tar", max compression
+gzip compressed data, was "libprocess-0.1.2.tar", max compression
```

## Comparing `libprocess-0.1.1.tar` & `libprocess-0.1.2.tar`

### file list

```diff
@@ -1,25 +1,25 @@
--rw-r--r--   0        0        0    34523 2023-07-19 07:06:26.643795 libprocess-0.1.1/LICENSE
--rw-r--r--   0        0        0      761 2023-07-19 07:06:26.643795 libprocess-0.1.1/README.md
--rw-r--r--   0        0        0      313 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/__init__.py
--rw-r--r--   0        0        0     3187 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/_utils/image.py
--rw-r--r--   0        0        0      517 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/_utils/language.py
--rw-r--r--   0        0        0       90 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/david_rumsey_map_collection/__init__.py
--rw-r--r--   0        0        0     6142 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/david_rumsey_map_collection/_process_metadata.py
--rw-r--r--   0        0        0     1319 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/david_rumsey_map_collection/_querier.py
--rw-r--r--   0        0        0     5919 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/david_rumsey_map_collection/_schema.py
--rw-r--r--   0        0        0       56 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/gallica/__init__.py
--rw-r--r--   0        0        0    10078 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/gallica/_process_metadata.py
--rw-r--r--   0        0        0     1231 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/gallica/_querier.py
--rw-r--r--   0        0        0     5382 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/gallica/_schema.py
--rw-r--r--   0        0        0     1025 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/gallica/_utils.py
--rw-r--r--   0        0        0       72 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/internet_archive/__init__.py
--rw-r--r--   0        0        0    10486 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/internet_archive/_process_metadata.py
--rw-r--r--   0        0        0     1522 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/internet_archive/_querier.py
--rw-r--r--   0        0        0     5961 2023-07-19 07:06:26.643795 libprocess-0.1.1/libprocess/internet_archive/_schema.py
--rw-r--r--   0        0        0       76 2023-07-19 07:06:26.647795 libprocess-0.1.1/libprocess/library_of_congress/__init__.py
--rw-r--r--   0        0        0     8648 2023-07-19 07:06:26.647795 libprocess-0.1.1/libprocess/library_of_congress/_process_metadata.py
--rw-r--r--   0        0        0     1283 2023-07-19 07:06:26.647795 libprocess-0.1.1/libprocess/library_of_congress/_querier.py
--rw-r--r--   0        0        0    10292 2023-07-19 07:06:26.647795 libprocess-0.1.1/libprocess/library_of_congress/_schema.py
--rw-r--r--   0        0        0     3466 2023-07-19 07:06:26.647795 libprocess-0.1.1/libprocess/typing.py
--rw-r--r--   0        0        0      486 2023-07-19 07:06:26.647795 libprocess-0.1.1/pyproject.toml
--rw-r--r--   0        0        0     1455 1970-01-01 00:00:00.000000 libprocess-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0    34523 2023-07-23 16:52:53.349963 libprocess-0.1.2/LICENSE
+-rw-r--r--   0        0        0      761 2023-07-23 16:52:53.349963 libprocess-0.1.2/README.md
+-rw-r--r--   0        0        0      313 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/__init__.py
+-rw-r--r--   0        0        0     3187 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/_utils/image.py
+-rw-r--r--   0        0        0      517 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/_utils/language.py
+-rw-r--r--   0        0        0       90 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/david_rumsey_map_collection/__init__.py
+-rw-r--r--   0        0        0     6252 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/david_rumsey_map_collection/_process_metadata.py
+-rw-r--r--   0        0        0     1590 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/david_rumsey_map_collection/_querier.py
+-rw-r--r--   0        0        0     5919 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/david_rumsey_map_collection/_schema.py
+-rw-r--r--   0        0        0       56 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/gallica/__init__.py
+-rw-r--r--   0        0        0    10264 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/gallica/_process_metadata.py
+-rw-r--r--   0        0        0     1502 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/gallica/_querier.py
+-rw-r--r--   0        0        0     5382 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/gallica/_schema.py
+-rw-r--r--   0        0        0     1025 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/gallica/_utils.py
+-rw-r--r--   0        0        0       72 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/internet_archive/__init__.py
+-rw-r--r--   0        0        0    10791 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/internet_archive/_process_metadata.py
+-rw-r--r--   0        0        0     1626 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/internet_archive/_querier.py
+-rw-r--r--   0        0        0     5961 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/internet_archive/_schema.py
+-rw-r--r--   0        0        0       76 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/library_of_congress/__init__.py
+-rw-r--r--   0        0        0     8754 2023-07-23 16:52:53.349963 libprocess-0.1.2/libprocess/library_of_congress/_process_metadata.py
+-rw-r--r--   0        0        0     1554 2023-07-23 16:52:53.353963 libprocess-0.1.2/libprocess/library_of_congress/_querier.py
+-rw-r--r--   0        0        0    10292 2023-07-23 16:52:53.353963 libprocess-0.1.2/libprocess/library_of_congress/_schema.py
+-rw-r--r--   0        0        0     3466 2023-07-23 16:52:53.353963 libprocess-0.1.2/libprocess/typing.py
+-rw-r--r--   0        0        0      545 2023-07-23 16:52:53.353963 libprocess-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0     1455 1970-01-01 00:00:00.000000 libprocess-0.1.2/PKG-INFO
```

### Comparing `libprocess-0.1.1/LICENSE` & `libprocess-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/README.md` & `libprocess-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/libprocess/_utils/image.py` & `libprocess-0.1.2/libprocess/_utils/image.py`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/libprocess/_utils/language.py` & `libprocess-0.1.2/libprocess/_utils/language.py`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/libprocess/david_rumsey_map_collection/_process_metadata.py` & `libprocess-0.1.2/libprocess/david_rumsey_map_collection/_process_metadata.py`

 * *Files 3% similar despite different names*

```diff
@@ -170,23 +170,27 @@
         # 'publisherAddress': get_first_element(get_attr(field_values, 'Publisher Location')),
         # 'publishTitle': publish_title,
         # 'publishNote': get_first_element(get_attr(field_values, 'Pub Note')),
     }
 
 
 def process_batch(
-    metadata_path: str, img_dir: Union[str, None]
+    metadata_path: str,
+    img_dir: Union[str, None],
+    uuids: Union[List[str], None] = None,
 ) -> List[BaseProcessedMetadataEntry]:
     """
     Process a batch of metadata entries.
     """
 
     metadata = load_jl(metadata_path)
     processed_metadata = [
-        process(d, img_dir) for d in tqdm(metadata, desc="Process Metadata Progress")
+        process(d, img_dir)
+        for d in tqdm(metadata, desc="Process Metadata Progress")
+        if (uuids is None) or (d["uuid"] in uuids)
     ]
 
     if img_dir is None:
         return processed_metadata
     # Ignore the entries where the phash computation failed,
     # meaning that the corresponding image has not been fetched
     # or the fetched image is corrupted.
```

### Comparing `libprocess-0.1.1/libprocess/david_rumsey_map_collection/_querier.py` & `libprocess-0.1.2/libprocess/library_of_congress/_querier.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,42 +1,52 @@
 """
 The entrance to querier class.
 """
 
 import json
 import os
-from typing import Union
+from typing import List, Union
 
 from jsonschema import validate
-from libquery import DavidRumseyMapCollection as _DavidRumseyMapCollection
+from libquery import LibraryOfCongress as _LibraryOfCongress
 from libquery.utils.jsonl import load_jl
 
 from ._process_metadata import process_batch
 from ._schema import schema_metadata
 
 
-def process_metadata(
-    metadata_path: str, img_dir: Union[str, None], processed_metadata_path: str
-) -> None:
-    output_dir = os.path.dirname(processed_metadata_path)
-    if not os.path.exists(output_dir):
-        os.makedirs(output_dir)
-
-    metadata = process_batch(metadata_path, img_dir)
-    with open(processed_metadata_path, "w", encoding="utf-8") as f:
-        f.write(json.dumps(metadata, indent=4, ensure_ascii=False))
-
-
-class DavidRumseyMapCollection(_DavidRumseyMapCollection):
+class LibraryOfCongress(_LibraryOfCongress):
     """
-    The querier for the `David Rumsey Map Collection` data source.
+    The querier for the `Library of Congress` data source.
     """
 
     def validate_metadata(self) -> None:
         metadata = load_jl(self.metadata_path)
         validate(instance=metadata, schema=schema_metadata)
 
-    def process_metadata(self, path: str) -> None:
-        process_metadata(self.metadata_path, self.img_dir, path)
+    def process_metadata(
+        self,
+        save_path: str,
+        use_img: bool = False,
+        uuids: Union[List[str], None] = None,
+    ) -> None:
+        """
+        Args
+        ----
+        save_path : str
+            The path to save the processing metadata file.
+        use_img : bool
+            Whether to use image to compute metadata.
+        uuids : Union[List[str], None]
+            The uuids of entries whose metadata are to be processed.
+            If uuids = None, all the entries will be processed.
+        """
+
+        output_dir = os.path.dirname(save_path)
+        if not os.path.exists(output_dir):
+            os.makedirs(output_dir)
+
+        img_dir = self.img_dir if use_img else None
+        metadata = process_batch(self.metadata_path, img_dir, uuids)
 
-    def process_metadata_fast(self, path: str) -> None:
-        process_metadata(self.metadata_path, None, path)
+        with open(save_path, "w", encoding="utf-8") as f:
+            f.write(json.dumps(metadata, indent=4, ensure_ascii=False))
```

### Comparing `libprocess-0.1.1/libprocess/david_rumsey_map_collection/_schema.py` & `libprocess-0.1.2/libprocess/david_rumsey_map_collection/_schema.py`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/libprocess/gallica/_process_metadata.py` & `libprocess-0.1.2/libprocess/gallica/_process_metadata.py`

 * *Files 2% similar despite different names*

```diff
@@ -242,15 +242,17 @@
             unit = "mm"
         image_size = {"width": width, "height": height, "unit": unit, "rawString": item}
         return image_size
     return None
 
 
 def process(
-    entry: MetadataEntry, img_dir: Union[str, None]
+    entry: MetadataEntry,
+    img_dir: Union[str, None],
+    uuids: Union[List[str], None] = None,
 ) -> List[BaseProcessedMetadataEntry]:
     """
     Postprocess a metadata entry.
     Create a list of metadata entries from the metadata entry.
     If img directory is not provided, do not compute the image attributes.
 
     Each metadata entry stored in Gallica contains a list of images.
@@ -284,15 +286,18 @@
 
         # Note: use the UUID of each page instead of
         # the UUID of the entire source data.
         uuid = get_image_uuid(page, entry)
         view_url = get_view_url(page, entry)
         download_url = get_image_url(page, entry)
 
-        image_attributes = (
+        if (uuids is not None) and (uuid not in uuids):
+            continue
+
+        image_properties = (
             {}
             if img_dir is None
             else {
                 "md5": get_md5_by_uuid(uuid, img_dir),
                 "phash": get_phash_by_uuid(uuid, img_dir),
                 "resolution": get_shape_by_uuid(uuid, img_dir),
                 "fileSize": get_storage_size_by_uuid(uuid, img_dir),
@@ -303,39 +308,41 @@
             {
                 "uuid": uuid,
                 "authors": authors,
                 "displayName": get_display_name(page, record),
                 "publishDate": publish_date,
                 "viewUrl": view_url,
                 "downloadUrl": download_url,
-                **image_attributes,
+                **image_properties,
                 "languages": languages,
                 "tags": tags,
                 "abstract": abstract,
                 "rights": get_rights(record),
                 "source": source,
-                # 'imageSize': image_size,
+                # "imageSize": image_size,
             }
         )
     return metadata_entries
 
 
 def process_batch(
-    metadata_path: str, img_dir: Union[str, None]
+    metadata_path: str,
+    img_dir: Union[str, None],
+    uuids: Union[List[str], None] = None,
 ) -> List[BaseProcessedMetadataEntry]:
     """
     Postprocess a batch of metadata entries.
     """
 
     metadata = load_jl(metadata_path)
     processed_metadata = []
     for d in tqdm(metadata, desc="Process Metadata Progress"):
         if "pages" not in d["sourceData"]:
             continue
-        processed_metadata += process(d, img_dir)
+        processed_metadata += process(d, img_dir, uuids)
 
     if img_dir is None:
         return processed_metadata
     # Ignore the entries where the phash computation failed,
     # meaning that the corresponding image has not been fetched
     # or the fetched image is corrupted.
     return [d for d in processed_metadata if d["phash"] is not None]
```

### Comparing `libprocess-0.1.1/libprocess/gallica/_schema.py` & `libprocess-0.1.2/libprocess/gallica/_schema.py`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/libprocess/gallica/_utils.py` & `libprocess-0.1.2/libprocess/gallica/_utils.py`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/libprocess/internet_archive/_process_metadata.py` & `libprocess-0.1.2/libprocess/internet_archive/_process_metadata.py`

 * *Files 5% similar despite different names*

```diff
@@ -161,15 +161,18 @@
 
 
 def filename2uuid(filename: str) -> str:
     return filename.split(".")[0]
 
 
 def process(
-    entry: MetadataEntry, download_dir: str, img_dir: Union[str, None]
+    entry: MetadataEntry,
+    download_dir: str,
+    img_dir: Union[str, None],
+    uuids: Union[List[str], None] = None,
 ) -> List[BaseProcessedMetadataEntry]:
     """
     Postprocess a metadata entry.
     If img directory is not provided, do not compute the image attributes.
     """
 
     id_in_source = entry["idInSource"]
@@ -209,23 +212,25 @@
         image_filenames = [
             d.split("/")[1] for d in relative_paths if not d.endswith("/")
         ]
         entries = []
         uuid2filename = {filename2uuid(d): d for d in os.listdir(img_dir)}
         for image_filename in image_filenames:
             uuid = get_image_uuid(image_filename, entry["source"])
+            if (uuids is not None) and (uuid not in uuids):
+                continue
             if (img_dir is not None) and (uuid not in uuid2filename):
                 continue
             page_index = int(image_filename.split(".")[0].split("_")[-1])
 
             if img_dir is None:
-                image_attributes = {}
+                image_properties = {}
             else:
                 image_path = f"{img_dir}/{uuid2filename[uuid]}"
-                image_attributes = {
+                image_properties = {
                     "md5": get_md5_by_path(image_path),
                     "phash": get_phash_by_path(image_path),
                     "resolution": get_shape_by_path(image_path),
                     "fileSize": get_storage_size_by_path(image_path),
                 }
 
             entries.append(
@@ -235,53 +240,60 @@
                     "displayName": source_data["metadata"]["title"]
                     + f" - Page {page_index}",
                     "viewUrl": f"https://archive.org/details/{identifier}/page/n{page_index}",
                     # 'downloadUrl': f'https://archive.org/download/{identifier}/{filename}',
                     "downloadUrl": get_download_url_for_image_in_zip(
                         filename, image_filename, source_data
                     ),
-                    **image_attributes,
+                    **image_properties,
                 }
             )
         return entries
     else:
+        uuid = get_image_uuid(filename, entry["source"])
+        if (uuids is not None) and (uuid not in uuids):
+            return []
+
         if img_dir is None:
-            image_attributes = {}
+            image_properties = {}
         else:
             image_path = f"{download_dir}/{identifier}/{filename}"
-            image_attributes = {
+            image_properties = {
                 "md5": get_md5_by_path(image_path),
                 "phash": get_phash_by_path(image_path),
                 "resolution": get_shape_by_path(image_path),
                 "fileSize": get_storage_size_by_path(image_path),
             }
 
         return [
             {
                 **partial_entry,
-                "uuid": get_image_uuid(filename, entry["source"]),
+                "uuid": uuid,
                 "displayName": source_data["metadata"]["title"],
                 "viewUrl": f"https://archive.org/details/{identifier}",
                 "downloadUrl": f"https://archive.org/download/{identifier}/{filename}",
-                **image_attributes,
+                **image_properties,
             }
         ]
 
 
 def process_batch(
-    metadata_path: str, download_dir: str, img_dir: Union[str, None]
+    metadata_path: str,
+    download_dir: str,
+    img_dir: Union[str, None],
+    uuids: Union[List[str], None] = None,
 ) -> List[BaseProcessedMetadataEntry]:
     """
     Postprocess a batch of metadata entries.
     """
 
     metadata = load_jl(metadata_path)
     processed_metadata = []
     for d in tqdm(metadata, desc="Process Metadata Progress"):
-        processed_metadata += process(d, download_dir, img_dir)
+        processed_metadata += process(d, download_dir, img_dir, uuids)
 
     if img_dir is None:
         return processed_metadata
     # Ignore the entries where the phash computation failed,
     # meaning that the corresponding image has not been fetched
     # or the fetched image is corrupted.
     return [d for d in processed_metadata if d["phash"] is not None]
```

### Comparing `libprocess-0.1.1/libprocess/internet_archive/_querier.py` & `libprocess-0.1.2/libprocess/gallica/_querier.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,59 +1,52 @@
 """
 The entrance to querier class.
 """
 
 import json
 import os
-from typing import Union
+from typing import List, Union
 
 from jsonschema import validate
-from libquery import InternetArchive as _InternetArchive
+from libquery import Gallica as _Gallica
 from libquery.utils.jsonl import load_jl
 
 from ._process_metadata import process_batch
 from ._schema import schema_metadata
 
 
-def process_metadata(
-    metadata_path: str,
-    download_dir: str,
-    img_dir: Union[str, None],
-    processed_metadata_path: str,
-) -> None:
-    output_dir = os.path.dirname(processed_metadata_path)
-    if not os.path.exists(output_dir):
-        os.makedirs(output_dir)
-
-    metadata = process_batch(
-        metadata_path,
-        download_dir,
-        img_dir,
-    )
-    with open(processed_metadata_path, "w", encoding="utf-8") as f:
-        f.write(json.dumps(metadata, indent=4, ensure_ascii=False))
-
-
-class InternetArchive(_InternetArchive):
+class Gallica(_Gallica):
     """
-    The querier for the `Internet Archive` data source.
+    The querier for the `Gallica` data source.
     """
 
     def validate_metadata(self) -> None:
         metadata = load_jl(self.metadata_path)
         validate(instance=metadata, schema=schema_metadata)
 
-    def process_metadata(self, path: str) -> None:
-        process_metadata(
-            self.metadata_path,
-            self.download_dir,
-            self.img_dir,
-            path,
-        )
-
-    def process_metadata_fast(self, path: str) -> None:
-        process_metadata(
-            self.metadata_path,
-            self.download_dir,
-            None,
-            path,
-        )
+    def process_metadata(
+        self,
+        save_path: str,
+        use_img: bool = False,
+        uuids: Union[List[str], None] = None,
+    ) -> None:
+        """
+        Args
+        ----
+        save_path : str
+            The path to save the processing metadata file.
+        use_img : bool
+            Whether to use image to compute metadata.
+        uuids : Union[List[str], None]
+            The uuids of entries whose metadata are to be processed.
+            If uuids = None, all the entries will be processed.
+        """
+
+        output_dir = os.path.dirname(save_path)
+        if not os.path.exists(output_dir):
+            os.makedirs(output_dir)
+
+        img_dir = self.img_dir if use_img else None
+        metadata = process_batch(self.metadata_path, img_dir, uuids)
+
+        with open(save_path, "w", encoding="utf-8") as f:
+            f.write(json.dumps(metadata, indent=4, ensure_ascii=False))
```

### Comparing `libprocess-0.1.1/libprocess/internet_archive/_schema.py` & `libprocess-0.1.2/libprocess/internet_archive/_schema.py`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/libprocess/library_of_congress/_process_metadata.py` & `libprocess-0.1.2/libprocess/library_of_congress/_process_metadata.py`

 * *Files 2% similar despite different names*

```diff
@@ -236,15 +236,15 @@
     Postprocess a metadata entry.
     If img directory is not provided, do not compute the image attributes.
     """
 
     source_data = entry["sourceData"]
     item = source_data["item"]
 
-    image_attributes = (
+    image_properties = (
         {}
         if img_dir is None
         else {
             "md5": get_md5_by_uuid(entry["uuid"], img_dir),
             "phash": get_phash_by_uuid(entry["uuid"], img_dir),
             "resolution": get_shape_by_uuid(entry["uuid"], img_dir),
             "fileSize": get_storage_size_by_uuid(entry["uuid"], img_dir),
@@ -256,37 +256,41 @@
         "authors": item.get("contributors", None),
         "displayName": source_data["title"],
         "publishDate": get_publish_date(source_data),
         "viewUrl": source_data["url"],
         # Note: the image_url stores URLs of the image with different resolution.
         # The last entry of the image_url gives the highest resolution.
         "downloadUrl": source_data["image_url"][-1],
-        **image_attributes,
+        **image_properties,
         "languages": get_languages(source_data),
         "tags": get_tags(source_data),
         "abstract": get_abstract(source_data),
         "rights": get_rights(source_data),
         "source": {
             "name": entry["source"],
             "url": entry["url"],
             "accessDate": entry["accessDate"],
         },
     }
 
 
 def process_batch(
-    metadata_path: str, img_dir: Union[str, None]
+    metadata_path: str,
+    img_dir: Union[str, None],
+    uuids: Union[List[str], None] = None,
 ) -> List[BaseProcessedMetadataEntry]:
     """
     Postprocess a batch of metadata entries.
     """
 
     metadata = load_jl(metadata_path)
     processed_metadata = [
-        process(d, img_dir) for d in tqdm(metadata, desc="Process Metadata Progress")
+        process(d, img_dir)
+        for d in tqdm(metadata, desc="Process Metadata Progress")
+        if (uuids is None) or (d["uuid"] in uuids)
     ]
 
     if img_dir is None:
         return processed_metadata
     # Ignore the entries where the phash computation failed,
     # meaning that the corresponding image has not been fetched
     # or the fetched image is corrupted.
```

### Comparing `libprocess-0.1.1/libprocess/library_of_congress/_schema.py` & `libprocess-0.1.2/libprocess/library_of_congress/_schema.py`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/libprocess/typing.py` & `libprocess-0.1.2/libprocess/typing.py`

 * *Files identical despite different names*

### Comparing `libprocess-0.1.1/PKG-INFO` & `libprocess-0.1.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: libprocess
-Version: 0.1.1
+Version: 0.1.2
 Summary: 
 Author: Yu Zhang
 Author-email: yuzhang94@outlook.com
 Requires-Python: >=3.10,<3.13
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: libprocess Version: 0.1.1 Summary: Author: Yu Zhang
+Metadata-Version: 2.1 Name: libprocess Version: 0.1.2 Summary: Author: Yu Zhang
 Author-email: yuzhang94@outlook.com Requires-Python: >=3.10,<3.13 Classifier:
 Programming Language :: Python :: 3 Classifier: Programming Language :: Python
 :: 3.10 Classifier: Programming Language :: Python :: 3.11 Requires-Dist:
 html2text (>=2020.1.16,<2021.0.0) Requires-Dist: imagehash (>=4.3.1,<5.0.0)
 Requires-Dist: jsonschema (>=4.18.3,<5.0.0) Requires-Dist: langcodes
 (>=3.3.0,<4.0.0) Requires-Dist: langdetect (>=1.0.9,<2.0.0) Requires-Dist:
 language-data (>=1.1,<2.0) Requires-Dist: libquery (>=0.1.1,<0.2.0) Requires-
```

