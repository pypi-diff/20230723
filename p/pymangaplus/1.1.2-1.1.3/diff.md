# Comparing `tmp/pymangaplus-1.1.2.tar.gz` & `tmp/pymangaplus-1.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pymangaplus-1.1.2.tar", last modified: Sun Jun 11 13:01:13 2023, max compression
+gzip compressed data, was "pymangaplus-1.1.3.tar", last modified: Sun Jul 23 15:46:12 2023, max compression
```

## Comparing `pymangaplus-1.1.2.tar` & `pymangaplus-1.1.3.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-06-11 13:01:13.894760 pymangaplus-1.1.2/
--rw-rw-rw-   0        0        0    35823 2023-06-11 11:44:56.000000 pymangaplus-1.1.2/LICENSE
--rw-rw-rw-   0        0        0     3447 2023-06-11 13:01:13.894760 pymangaplus-1.1.2/PKG-INFO
--rw-rw-rw-   0        0        0     2537 2023-06-11 13:01:02.000000 pymangaplus-1.1.2/README.md
-drwxrwxrwx   0        0        0        0 2023-06-11 13:01:13.870335 pymangaplus-1.1.2/pymangaplus/
--rw-rw-rw-   0        0        0       79 2023-06-11 12:58:18.000000 pymangaplus-1.1.2/pymangaplus/__init__.py
--rw-rw-rw-   0        0        0   101493 2023-06-11 11:44:56.000000 pymangaplus-1.1.2/pymangaplus/api_protocol_pb2.py
--rw-rw-rw-   0        0        0     6379 2023-06-11 12:57:34.000000 pymangaplus-1.1.2/pymangaplus/client.py
--rw-rw-rw-   0        0        0      356 2023-06-11 11:44:56.000000 pymangaplus-1.1.2/pymangaplus/constants.py
--rw-rw-rw-   0        0        0      529 2023-06-11 11:44:56.000000 pymangaplus-1.1.2/pymangaplus/utils.py
-drwxrwxrwx   0        0        0        0 2023-06-11 13:01:13.894760 pymangaplus-1.1.2/pymangaplus.egg-info/
--rw-rw-rw-   0        0        0     3447 2023-06-11 13:01:13.000000 pymangaplus-1.1.2/pymangaplus.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      324 2023-06-11 13:01:13.000000 pymangaplus-1.1.2/pymangaplus.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-06-11 13:01:13.000000 pymangaplus-1.1.2/pymangaplus.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-06-11 13:01:13.000000 pymangaplus-1.1.2/pymangaplus.egg-info/requires.txt
--rw-rw-rw-   0        0        0       12 2023-06-11 13:01:13.000000 pymangaplus-1.1.2/pymangaplus.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-06-11 13:01:13.894760 pymangaplus-1.1.2/setup.cfg
--rw-rw-rw-   0        0        0     1201 2023-06-11 12:58:18.000000 pymangaplus-1.1.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:46:12.494943 pymangaplus-1.1.3/
+-rw-rw-rw-   0        0        0    35823 2023-07-23 15:39:11.000000 pymangaplus-1.1.3/LICENSE
+-rw-rw-rw-   0        0        0     3447 2023-07-23 15:46:12.494943 pymangaplus-1.1.3/PKG-INFO
+-rw-rw-rw-   0        0        0     2537 2023-07-23 15:45:57.000000 pymangaplus-1.1.3/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 15:46:12.431925 pymangaplus-1.1.3/pymangaplus/
+-rw-rw-rw-   0        0        0       79 2023-07-23 15:44:19.000000 pymangaplus-1.1.3/pymangaplus/__init__.py
+-rw-rw-rw-   0        0        0    99019 2023-07-23 15:43:28.000000 pymangaplus-1.1.3/pymangaplus/api_protocol_pb2.py
+-rw-rw-rw-   0        0        0     6380 2023-07-23 15:39:55.000000 pymangaplus-1.1.3/pymangaplus/client.py
+-rw-rw-rw-   0        0        0      356 2023-07-23 15:39:11.000000 pymangaplus-1.1.3/pymangaplus/constants.py
+-rw-rw-rw-   0        0        0      529 2023-07-23 15:39:11.000000 pymangaplus-1.1.3/pymangaplus/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:46:12.494943 pymangaplus-1.1.3/pymangaplus.egg-info/
+-rw-rw-rw-   0        0        0     3447 2023-07-23 15:46:12.000000 pymangaplus-1.1.3/pymangaplus.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      324 2023-07-23 15:46:12.000000 pymangaplus-1.1.3/pymangaplus.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:46:12.000000 pymangaplus-1.1.3/pymangaplus.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 15:46:12.000000 pymangaplus-1.1.3/pymangaplus.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 15:46:12.000000 pymangaplus-1.1.3/pymangaplus.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:46:12.494943 pymangaplus-1.1.3/setup.cfg
+-rw-rw-rw-   0        0        0     1201 2023-07-23 15:44:19.000000 pymangaplus-1.1.3/setup.py
```

### Comparing `pymangaplus-1.1.2/LICENSE` & `pymangaplus-1.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `pymangaplus-1.1.2/PKG-INFO` & `pymangaplus-1.1.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pymangaplus
-Version: 1.1.2
+Version: 1.1.3
 Summary: Python client for the MangaPlus API.
 Home-page: https://github.com/hyugogirubato/pymangaplus
 Author: hyugogirubato
 Author-email: hyugogirubato@gmail.com
 License: GPL-3.0-only
 Keywords: client,manga,ebooks,manga-plus
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `pymangaplus-1.1.2/README.md` & `pymangaplus-1.1.3/README.md`

 * *Files identical despite different names*

### Comparing `pymangaplus-1.1.2/pymangaplus/api_protocol_pb2.py` & `pymangaplus-1.1.3/pymangaplus/api_protocol_pb2.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,2454 +1,2454 @@
-# Generated by the protocol buffer compiler.  DO NOT EDIT!
-# source: api_protocol.proto
-
-import sys
-_b=sys.version_info[0]<3 and (lambda x:x) or (lambda x:x.encode('latin1'))
-from google.protobuf.internal import enum_type_wrapper
-from google.protobuf import descriptor as _descriptor
-from google.protobuf import message as _message
-from google.protobuf import reflection as _reflection
-from google.protobuf import symbol_database as _symbol_database
-from google.protobuf import descriptor_pb2
-# @@protoc_insertion_point(imports)
-
-_sym_db = _symbol_database.Default()
-
-
-
-
-DESCRIPTOR = _descriptor.FileDescriptor(
-  name='api_protocol.proto',
-  package='api_protocol',
-  syntax='proto3',
-  serialized_pb=_b('\n\x12\x61pi_protocol.proto\x12\x0c\x61pi_protocol\" \n\x03Sns\x12\x0c\n\x04\x62ody\x18\x01 \x01(\t\x12\x0b\n\x03url\x18\x02 \x01(\t\"P\n\x06\x42\x61nner\x12\x13\n\x0bimageBanner\x18\x01 \x01(\t\x12\x1e\n\x03sns\x18\x02 \x01(\x0b\x32\x11.api_protocol.Sns\x12\x11\n\tviewCount\x18\x03 \x01(\x05\"A\n\x05\x43ount\x12(\n\x08language\x18\x01 \x01(\x0e\x32\x16.api_protocol.Language\x12\x0e\n\x06titles\x18\x02 \x01(\x05\"\xcc\x01\n\x07\x43hapter\x12\x0f\n\x07titleId\x18\x01 \x01(\r\x12\x11\n\tchapterId\x18\x02 \x01(\r\x12\x11\n\ttitleName\x18\x03 \x01(\t\x12\x17\n\x0f\x63hapterSubTitle\x18\x04 \x01(\t\x12\x14\n\x0cthumbnailUrl\x18\x05 \x01(\t\x12\x16\n\x0estartTimeStamp\x18\x06 \x01(\t\x12\x14\n\x0c\x65ndTimeStamp\x18\x07 \x01(\t\x12\x15\n\ralreadyViewed\x18\x08 \x01(\x08\x12\x16\n\x0eisVerticalOnly\x18\t \x01(\x08\"\xa7\x01\n\x05Title\x12\x0f\n\x07titleId\x18\x01 \x01(\r\x12\x11\n\ttitleName\x18\x02 \x01(\t\x12\x0e\n\x06\x61uthor\x18\x03 \x01(\t\x12\x15\n\rimagePortrait\x18\x04 \x01(\t\x12\x16\n\x0eimageLandscape\x18\x05 \x01(\t\x12\x11\n\tviewCount\x18\x06 \x01(\r\x12(\n\x08language\x18\x07 \x01(\x0e\x32\x16.api_protocol.Language\"<\n\x08\x43\x61tegory\x12\x0c\n\x04name\x18\x01 \x01(\t\x12\"\n\x05items\x18\x02 \x03(\x0b\x32\x13.api_protocol.Title\"b\n\x08Response\x12,\n\x07success\x18\x01 \x01(\x0b\x32\x1b.api_protocol.SuccessResult\x12(\n\x05\x65rror\x18\x02 \x01(\x0b\x32\x19.api_protocol.ErrorResult\"\xc7\x02\n\x0b\x45rrorResult\x12/\n\x07\x64\x65\x66\x61ult\x18\x02 \x01(\x0b\x32\x1e.api_protocol.ErrorResult.Item\x12/\n\x07\x64isplay\x18\x03 \x01(\x0b\x32\x1e.api_protocol.ErrorResult.Item\x12\x33\n\x0b\x61llLanguage\x18\x05 \x03(\x0b\x32\x1e.api_protocol.ErrorResult.Item\x1a\xa0\x01\n\x04Item\x12\x0c\n\x04\x63ode\x18\x01 \x01(\t\x12\x0f\n\x07message\x18\x02 \x01(\t\x12\x35\n\x06\x62utton\x18\x05 \x01(\x0b\x32%.api_protocol.ErrorResult.Item.Button\x12(\n\x08language\x18\x06 \x01(\x0e\x32\x16.api_protocol.Language\x1a\x18\n\x06\x42utton\x12\x0e\n\x06\x61\x63tion\x18\x01 \x01(\t\"\x98\x06\n\rSuccessResult\x12\x19\n\x11isFeaturedUpdated\x18\x01 \x01(\x08\x12\x30\n\x0cregisterView\x18\x02 \x01(\x0b\x32\x1a.api_protocol.RegisterView\x12\x30\n\x0c\x66\x65\x61turedView\x18\x04 \x01(\x0b\x32\x1a.api_protocol.FeaturedView\x12.\n\x0brankingView\x18\x06 \x01(\x0b\x32\x19.api_protocol.RankingView\x12@\n\x14subscribedTitlesView\x18\x07 \x01(\x0b\x32\".api_protocol.SubscribedTitlesView\x12\x36\n\x0ftitleDetailView\x18\x08 \x01(\x0b\x32\x1d.api_protocol.TitleDetailView\x12.\n\x0b\x63ommentView\x18\t \x01(\x0b\x32\x19.api_protocol.CommentView\x12.\n\x0bmangaViewer\x18\n \x01(\x0b\x32\x19.api_protocol.MangaViewer\x12.\n\x0bprofileView\x18\r \x01(\x0b\x32\x19.api_protocol.ProfileView\x12:\n\x11updateProfileView\x18\x0e \x01(\x0b\x32\x1f.api_protocol.UpdateProfileView\x12(\n\x08homeView\x18\x18 \x01(\x0b\x32\x16.api_protocol.HomeView\x12&\n\x07\x61llView\x18\x19 \x01(\x0b\x32\x15.api_protocol.AllView\x12\x30\n\x0csettingsView\x18\x1a \x01(\x0b\x32\x1a.api_protocol.SettingsView\x12(\n\x08initView\x18\x1c \x01(\x0b\x32\x16.api_protocol.InitView\x12.\n\x0b\x63ontentView\x18\x1d \x01(\x0b\x32\x19.api_protocol.ContentView\x12\x34\n\x0e\x66reeTitlesView\x18! \x01(\x0b\x32\x1c.api_protocol.FreeTitlesView\"\x84\x01\n\x0b\x43ontentView\x12\'\n\x07\x64\x65\x66\x61ult\x18\x01 \x01(\x0e\x32\x16.api_protocol.Language\x12\'\n\x07\x64isplay\x18\x03 \x01(\x0e\x32\x16.api_protocol.Language\x12#\n\x06\x63ounts\x18\x05 \x03(\x0b\x32\x13.api_protocol.Count\";\n\x14SubscribedTitlesView\x12#\n\x06titles\x18\x01 \x03(\x0b\x32\x13.api_protocol.Title\"2\n\x0bRankingView\x12#\n\x06titles\x18\x01 \x03(\x0b\x32\x13.api_protocol.Title\"2\n\x0b\x43ommentView\x12#\n\x06titles\x18\x01 \x03(\x0b\x32\x13.api_protocol.Title\"\xb6\x04\n\x0bMangaViewer\x12-\n\x05pages\x18\x01 \x03(\x0b\x32\x1e.api_protocol.MangaViewer.Page\x12\x11\n\tchapterId\x18\x02 \x01(\r\x12\'\n\x08\x63hapters\x18\x03 \x03(\x0b\x32\x15.api_protocol.Chapter\x12\x1e\n\x03sns\x18\x04 \x01(\x0b\x32\x11.api_protocol.Sns\x12\x11\n\ttitleName\x18\x05 \x01(\t\x12\x13\n\x0b\x63hapterName\x18\x06 \x01(\t\x12\x18\n\x10numberOfComments\x18\x07 \x01(\r\x12\x16\n\x0eisVerticalOnly\x18\x08 \x01(\x08\x12\x0f\n\x07titleId\x18\t \x01(\r\x12\x16\n\x0estartFromRight\x18\n \x01(\x08\x12\x0f\n\x07\x63ountry\x18\x0b \x01(\t\x1a\x87\x02\n\x04Page\x12\x36\n\x04page\x18\x01 \x01(\x0b\x32(.api_protocol.MangaViewer.Page.MangaPage\x1a\xc6\x01\n\tMangaPage\x12\x11\n\timagePage\x18\x01 \x01(\t\x12\r\n\x05width\x18\x02 \x01(\r\x12\x0e\n\x06height\x18\x03 \x01(\r\x12;\n\x04type\x18\x04 \x01(\x0e\x32-.api_protocol.MangaViewer.Page.MangaPage.Type\x12\x15\n\rencryptionKey\x18\x05 \x01(\t\"3\n\x04Type\x12\n\n\x06SINGLE\x10\x00\x12\x08\n\x04LEFT\x10\x01\x12\t\n\x05RIGHT\x10\x02\x12\n\n\x06\x44OUBLE\x10\x03\"\x8e\x01\n\x0bProfileView\x12-\n\x05icons\x18\x01 \x03(\x0b\x32\x1e.api_protocol.ProfileView.Icon\x12/\n\x07\x64\x65\x66\x61ult\x18\x03 \x01(\x0b\x32\x1e.api_protocol.ProfileView.Icon\x1a\x1f\n\x04Icon\x12\n\n\x02id\x18\x01 \x01(\r\x12\x0b\n\x03url\x18\x02 \x01(\t\"#\n\x11UpdateProfileView\x12\x0e\n\x06status\x18\x01 \x01(\x08\"\x83\x01\n\x0e\x46reeTitlesView\x12\x31\n\x06titles\x18\x01 \x03(\x0b\x32!.api_protocol.FreeTitlesView.Item\x1a>\n\x04Item\x12\"\n\x05title\x18\x01 \x01(\x0b\x32\x13.api_protocol.Title\x12\x12\n\nlastUpdate\x18\x02 \x01(\t\"1\n\x07\x41llView\x12&\n\x06titles\x18\x01 \x03(\x0b\x32\x16.api_protocol.Category\"f\n\x0cSettingsView\x12\x1f\n\x04icon\x18\x01 \x01(\x0b\x32\x11.api_protocol.Sns\x12\x10\n\x08username\x18\x02 \x01(\t\x12#\n\x06\x63ounts\x18\x05 \x03(\x0b\x32\x13.api_protocol.Count\"X\n\x08InitView\x12\'\n\x07\x64\x65\x66\x61ult\x18\x01 \x01(\x0e\x32\x16.api_protocol.Language\x12#\n\x06\x63ounts\x18\x02 \x03(\x0b\x32\x13.api_protocol.Count\"\x1e\n\x0cRegisterView\x12\x0e\n\x06secret\x18\x01 \x01(\t\"\x80\x05\n\x08HomeView\x12%\n\x07\x62\x61nners\x18\x01 \x03(\x0b\x32\x14.api_protocol.Banner\x12.\n\x07updates\x18\x02 \x03(\x0b\x32\x1d.api_protocol.HomeView.Update\x12+\n\x05popup\x18\t \x01(\x0b\x32\x1c.api_protocol.HomeView.Popup\x1a\xd9\x02\n\x06Update\x12\x10\n\x08\x63\x61tegory\x18\x01 \x01(\t\x12\x31\n\x05items\x18\x02 \x03(\x0b\x32\".api_protocol.HomeView.Update.Item\x1a\x89\x02\n\x04Item\x12\x11\n\ttitleName\x18\x01 \x01(\t\x12\x13\n\x0b\x63hapterName\x18\x02 \x01(\t\x12=\n\x08metadata\x18\x03 \x01(\x0b\x32+.api_protocol.HomeView.Update.Item.Metadata\x1a\x99\x01\n\x08Metadata\x12\"\n\x05title\x18\x01 \x03(\x0b\x32\x13.api_protocol.Title\x12\x11\n\tchapterId\x18\x02 \x01(\x05\x12\x13\n\x0b\x63hapterName\x18\x03 \x01(\t\x12\x17\n\x0f\x63hapterSubTitle\x18\x04 \x01(\t\x12(\n\x08language\x18\x05 \x01(\x0e\x32\x16.api_protocol.Language\x1a\x93\x01\n\x05Popup\x12\x37\n\x08resource\x18\x04 \x01(\x0b\x32%.api_protocol.HomeView.Popup.Resource\x12\x11\n\tviewCount\x18\x05 \x01(\x05\x1a>\n\x08Resource\x12\x1e\n\x03sns\x18\x01 \x01(\x0b\x32\x11.api_protocol.Sns\x12\x12\n\nimagePopup\x18\x02 \x01(\t\"\x99\x02\n\x0c\x46\x65\x61turedView\x12\'\n\ttopBanner\x18\x01 \x01(\x0b\x32\x14.api_protocol.Banner\x12%\n\x07topLeft\x18\x02 \x01(\x0b\x32\x14.api_protocol.Banner\x12&\n\x08topRight\x18\x03 \x01(\x0b\x32\x14.api_protocol.Banner\x12\x35\n\x08\x66\x65\x61tured\x18\x04 \x03(\x0b\x32#.api_protocol.FeaturedView.Featured\x1aZ\n\x08\x46\x65\x61tured\x12$\n\x06\x62\x61nner\x18\x01 \x01(\x0b\x32\x14.api_protocol.Banner\x12(\n\x08\x63\x61tegory\x18\x02 \x01(\x0b\x32\x16.api_protocol.Category\"\x8d\t\n\x0fTitleDetailView\x12\"\n\x05title\x18\x01 \x01(\x0b\x32\x13.api_protocol.Title\x12\x12\n\nimageTitle\x18\x02 \x01(\t\x12\x10\n\x08overview\x18\x03 \x01(\t\x12\x17\n\x0fimageBackground\x18\x04 \x01(\t\x12\x15\n\rnextTimeStamp\x18\x05 \x01(\t\x12@\n\x0cupdateTiming\x18\x06 \x01(\x0e\x32*.api_protocol.TitleDetailView.UpdateTiming\x12 \n\x18viewingPeriodDescription\x18\x07 \x01(\t\x12\x19\n\x11nonAppearanceInfo\x18\x08 \x01(\t\x12%\n\x07\x62\x61nners\x18\x0b \x03(\x0b\x32\x14.api_protocol.Banner\x12\x31\n\x14recommendedTitleList\x18\x0c \x03(\x0b\x32\x13.api_protocol.Title\x12\x1e\n\x03sns\x18\r \x01(\x0b\x32\x11.api_protocol.Sns\x12\x1b\n\x13isSimulcastReleased\x18\x0e \x01(\x08\x12\x14\n\x0cisSubscribed\x18\x0f \x01(\x08\x12\x34\n\x06rating\x18\x10 \x01(\x0e\x32$.api_protocol.TitleDetailView.Rating\x12\x1a\n\x12\x63haptersDescending\x18\x11 \x01(\x08\x12\x15\n\rnumberOfViews\x18\x12 \x01(\r\x12*\n\x0ctitleBanners\x18\x14 \x01(\x0b\x32\x14.api_protocol.Banner\x12>\n\x0b\x61llLanguage\x18\x1b \x03(\x0b\x32).api_protocol.TitleDetailView.AllLanguage\x12\x38\n\x08\x63hapters\x18\x1c \x03(\x0b\x32&.api_protocol.TitleDetailView.Chapters\x12\x0f\n\x07\x63ountry\x18\x1e \x01(\t\x1aH\n\x0b\x41llLanguage\x12\x0f\n\x07titleId\x18\x01 \x01(\r\x12(\n\x08language\x18\x02 \x01(\x0e\x32\x16.api_protocol.Language\x1a\xa6\x01\n\x08\x43hapters\x12\r\n\x05\x63ount\x18\x01 \x01(\r\x12/\n\x10\x66irstChapterList\x18\x02 \x03(\x0b\x32\x15.api_protocol.Chapter\x12*\n\x0b\x63hapterList\x18\x03 \x03(\x0b\x32\x15.api_protocol.Chapter\x12.\n\x0flastChapterList\x18\x04 \x03(\x0b\x32\x15.api_protocol.Chapter\"\x86\x01\n\x0cUpdateTiming\x12\x11\n\rNOT_REGULARLY\x10\x00\x12\n\n\x06MONDAY\x10\x01\x12\x0b\n\x07TUESDAY\x10\x02\x12\r\n\tWEDNESDAY\x10\x03\x12\x0c\n\x08THURSDAY\x10\x04\x12\n\n\x06\x46RIDAY\x10\x05\x12\x0c\n\x08SATURDAY\x10\x06\x12\n\n\x06SUNDAY\x10\x07\x12\x07\n\x03\x44\x41Y\x10\x08\"8\n\x06Rating\x12\n\n\x06\x41LLAGE\x10\x00\x12\x08\n\x04TEEN\x10\x01\x12\x0c\n\x08TEENPLUS\x10\x02\x12\n\n\x06MATURE\x10\x03*g\n\x08Language\x12\x0b\n\x07\x45NGLISH\x10\x00\x12\x0b\n\x07SPANISH\x10\x01\x12\n\n\x06\x46RENCH\x10\x02\x12\x0e\n\nINDONESIAN\x10\x03\x12\x0e\n\nPORTUGUESE\x10\x04\x12\x0b\n\x07RUSSIAN\x10\x05\x12\x08\n\x04THAI\x10\x06\x62\x06proto3')
-)
-
-_LANGUAGE = _descriptor.EnumDescriptor(
-  name='Language',
-  full_name='api_protocol.Language',
-  filename=None,
-  file=DESCRIPTOR,
-  values=[
-    _descriptor.EnumValueDescriptor(
-      name='ENGLISH', index=0, number=0,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='SPANISH', index=1, number=1,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='FRENCH', index=2, number=2,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='INDONESIAN', index=3, number=3,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='PORTUGUESE', index=4, number=4,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='RUSSIAN', index=5, number=5,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='THAI', index=6, number=6,
-      options=None,
-      type=None),
-  ],
-  containing_type=None,
-  options=None,
-  serialized_start=5440,
-  serialized_end=5543,
-)
-_sym_db.RegisterEnumDescriptor(_LANGUAGE)
-
-Language = enum_type_wrapper.EnumTypeWrapper(_LANGUAGE)
-ENGLISH = 0
-SPANISH = 1
-FRENCH = 2
-INDONESIAN = 3
-PORTUGUESE = 4
-RUSSIAN = 5
-THAI = 6
-
-
-_MANGAVIEWER_PAGE_MANGAPAGE_TYPE = _descriptor.EnumDescriptor(
-  name='Type',
-  full_name='api_protocol.MangaViewer.Page.MangaPage.Type',
-  filename=None,
-  file=DESCRIPTOR,
-  values=[
-    _descriptor.EnumValueDescriptor(
-      name='SINGLE', index=0, number=0,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='LEFT', index=1, number=1,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='RIGHT', index=2, number=2,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='DOUBLE', index=3, number=3,
-      options=None,
-      type=None),
-  ],
-  containing_type=None,
-  options=None,
-  serialized_start=2699,
-  serialized_end=2750,
-)
-_sym_db.RegisterEnumDescriptor(_MANGAVIEWER_PAGE_MANGAPAGE_TYPE)
-
-_TITLEDETAILVIEW_UPDATETIMING = _descriptor.EnumDescriptor(
-  name='UpdateTiming',
-  full_name='api_protocol.TitleDetailView.UpdateTiming',
-  filename=None,
-  file=DESCRIPTOR,
-  values=[
-    _descriptor.EnumValueDescriptor(
-      name='NOT_REGULARLY', index=0, number=0,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='MONDAY', index=1, number=1,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='TUESDAY', index=2, number=2,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='WEDNESDAY', index=3, number=3,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='THURSDAY', index=4, number=4,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='FRIDAY', index=5, number=5,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='SATURDAY', index=6, number=6,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='SUNDAY', index=7, number=7,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='DAY', index=8, number=8,
-      options=None,
-      type=None),
-  ],
-  containing_type=None,
-  options=None,
-  serialized_start=5246,
-  serialized_end=5380,
-)
-_sym_db.RegisterEnumDescriptor(_TITLEDETAILVIEW_UPDATETIMING)
-
-_TITLEDETAILVIEW_RATING = _descriptor.EnumDescriptor(
-  name='Rating',
-  full_name='api_protocol.TitleDetailView.Rating',
-  filename=None,
-  file=DESCRIPTOR,
-  values=[
-    _descriptor.EnumValueDescriptor(
-      name='ALLAGE', index=0, number=0,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='TEEN', index=1, number=1,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='TEENPLUS', index=2, number=2,
-      options=None,
-      type=None),
-    _descriptor.EnumValueDescriptor(
-      name='MATURE', index=3, number=3,
-      options=None,
-      type=None),
-  ],
-  containing_type=None,
-  options=None,
-  serialized_start=5382,
-  serialized_end=5438,
-)
-_sym_db.RegisterEnumDescriptor(_TITLEDETAILVIEW_RATING)
-
-
-_SNS = _descriptor.Descriptor(
-  name='Sns',
-  full_name='api_protocol.Sns',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='body', full_name='api_protocol.Sns.body', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='url', full_name='api_protocol.Sns.url', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=36,
-  serialized_end=68,
-)
-
-
-_BANNER = _descriptor.Descriptor(
-  name='Banner',
-  full_name='api_protocol.Banner',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='imageBanner', full_name='api_protocol.Banner.imageBanner', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='sns', full_name='api_protocol.Banner.sns', index=1,
-      number=2, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='viewCount', full_name='api_protocol.Banner.viewCount', index=2,
-      number=3, type=5, cpp_type=1, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=70,
-  serialized_end=150,
-)
-
-
-_COUNT = _descriptor.Descriptor(
-  name='Count',
-  full_name='api_protocol.Count',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='language', full_name='api_protocol.Count.language', index=0,
-      number=1, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='titles', full_name='api_protocol.Count.titles', index=1,
-      number=2, type=5, cpp_type=1, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=152,
-  serialized_end=217,
-)
-
-
-_CHAPTER = _descriptor.Descriptor(
-  name='Chapter',
-  full_name='api_protocol.Chapter',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titleId', full_name='api_protocol.Chapter.titleId', index=0,
-      number=1, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterId', full_name='api_protocol.Chapter.chapterId', index=1,
-      number=2, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='titleName', full_name='api_protocol.Chapter.titleName', index=2,
-      number=3, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterSubTitle', full_name='api_protocol.Chapter.chapterSubTitle', index=3,
-      number=4, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='thumbnailUrl', full_name='api_protocol.Chapter.thumbnailUrl', index=4,
-      number=5, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='startTimeStamp', full_name='api_protocol.Chapter.startTimeStamp', index=5,
-      number=6, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='endTimeStamp', full_name='api_protocol.Chapter.endTimeStamp', index=6,
-      number=7, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='alreadyViewed', full_name='api_protocol.Chapter.alreadyViewed', index=7,
-      number=8, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='isVerticalOnly', full_name='api_protocol.Chapter.isVerticalOnly', index=8,
-      number=9, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=220,
-  serialized_end=424,
-)
-
-
-_TITLE = _descriptor.Descriptor(
-  name='Title',
-  full_name='api_protocol.Title',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titleId', full_name='api_protocol.Title.titleId', index=0,
-      number=1, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='titleName', full_name='api_protocol.Title.titleName', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='author', full_name='api_protocol.Title.author', index=2,
-      number=3, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='imagePortrait', full_name='api_protocol.Title.imagePortrait', index=3,
-      number=4, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='imageLandscape', full_name='api_protocol.Title.imageLandscape', index=4,
-      number=5, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='viewCount', full_name='api_protocol.Title.viewCount', index=5,
-      number=6, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='language', full_name='api_protocol.Title.language', index=6,
-      number=7, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=427,
-  serialized_end=594,
-)
-
-
-_CATEGORY = _descriptor.Descriptor(
-  name='Category',
-  full_name='api_protocol.Category',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='name', full_name='api_protocol.Category.name', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='items', full_name='api_protocol.Category.items', index=1,
-      number=2, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=596,
-  serialized_end=656,
-)
-
-
-_RESPONSE = _descriptor.Descriptor(
-  name='Response',
-  full_name='api_protocol.Response',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='success', full_name='api_protocol.Response.success', index=0,
-      number=1, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='error', full_name='api_protocol.Response.error', index=1,
-      number=2, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=658,
-  serialized_end=756,
-)
-
-
-_ERRORRESULT_ITEM_BUTTON = _descriptor.Descriptor(
-  name='Button',
-  full_name='api_protocol.ErrorResult.Item.Button',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='action', full_name='api_protocol.ErrorResult.Item.Button.action', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=1062,
-  serialized_end=1086,
-)
-
-_ERRORRESULT_ITEM = _descriptor.Descriptor(
-  name='Item',
-  full_name='api_protocol.ErrorResult.Item',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='code', full_name='api_protocol.ErrorResult.Item.code', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='message', full_name='api_protocol.ErrorResult.Item.message', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='button', full_name='api_protocol.ErrorResult.Item.button', index=2,
-      number=5, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='language', full_name='api_protocol.ErrorResult.Item.language', index=3,
-      number=6, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_ERRORRESULT_ITEM_BUTTON, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=926,
-  serialized_end=1086,
-)
-
-_ERRORRESULT = _descriptor.Descriptor(
-  name='ErrorResult',
-  full_name='api_protocol.ErrorResult',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='default', full_name='api_protocol.ErrorResult.default', index=0,
-      number=2, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='display', full_name='api_protocol.ErrorResult.display', index=1,
-      number=3, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='allLanguage', full_name='api_protocol.ErrorResult.allLanguage', index=2,
-      number=5, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_ERRORRESULT_ITEM, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=759,
-  serialized_end=1086,
-)
-
-
-_SUCCESSRESULT = _descriptor.Descriptor(
-  name='SuccessResult',
-  full_name='api_protocol.SuccessResult',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='isFeaturedUpdated', full_name='api_protocol.SuccessResult.isFeaturedUpdated', index=0,
-      number=1, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='registerView', full_name='api_protocol.SuccessResult.registerView', index=1,
-      number=2, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='featuredView', full_name='api_protocol.SuccessResult.featuredView', index=2,
-      number=4, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='rankingView', full_name='api_protocol.SuccessResult.rankingView', index=3,
-      number=6, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='subscribedTitlesView', full_name='api_protocol.SuccessResult.subscribedTitlesView', index=4,
-      number=7, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='titleDetailView', full_name='api_protocol.SuccessResult.titleDetailView', index=5,
-      number=8, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='commentView', full_name='api_protocol.SuccessResult.commentView', index=6,
-      number=9, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='mangaViewer', full_name='api_protocol.SuccessResult.mangaViewer', index=7,
-      number=10, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='profileView', full_name='api_protocol.SuccessResult.profileView', index=8,
-      number=13, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='updateProfileView', full_name='api_protocol.SuccessResult.updateProfileView', index=9,
-      number=14, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='homeView', full_name='api_protocol.SuccessResult.homeView', index=10,
-      number=24, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='allView', full_name='api_protocol.SuccessResult.allView', index=11,
-      number=25, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='settingsView', full_name='api_protocol.SuccessResult.settingsView', index=12,
-      number=26, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='initView', full_name='api_protocol.SuccessResult.initView', index=13,
-      number=28, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='contentView', full_name='api_protocol.SuccessResult.contentView', index=14,
-      number=29, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='freeTitlesView', full_name='api_protocol.SuccessResult.freeTitlesView', index=15,
-      number=33, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=1089,
-  serialized_end=1881,
-)
-
-
-_CONTENTVIEW = _descriptor.Descriptor(
-  name='ContentView',
-  full_name='api_protocol.ContentView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='default', full_name='api_protocol.ContentView.default', index=0,
-      number=1, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='display', full_name='api_protocol.ContentView.display', index=1,
-      number=3, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='counts', full_name='api_protocol.ContentView.counts', index=2,
-      number=5, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=1884,
-  serialized_end=2016,
-)
-
-
-_SUBSCRIBEDTITLESVIEW = _descriptor.Descriptor(
-  name='SubscribedTitlesView',
-  full_name='api_protocol.SubscribedTitlesView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titles', full_name='api_protocol.SubscribedTitlesView.titles', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2018,
-  serialized_end=2077,
-)
-
-
-_RANKINGVIEW = _descriptor.Descriptor(
-  name='RankingView',
-  full_name='api_protocol.RankingView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titles', full_name='api_protocol.RankingView.titles', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2079,
-  serialized_end=2129,
-)
-
-
-_COMMENTVIEW = _descriptor.Descriptor(
-  name='CommentView',
-  full_name='api_protocol.CommentView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titles', full_name='api_protocol.CommentView.titles', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2131,
-  serialized_end=2181,
-)
-
-
-_MANGAVIEWER_PAGE_MANGAPAGE = _descriptor.Descriptor(
-  name='MangaPage',
-  full_name='api_protocol.MangaViewer.Page.MangaPage',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='imagePage', full_name='api_protocol.MangaViewer.Page.MangaPage.imagePage', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='width', full_name='api_protocol.MangaViewer.Page.MangaPage.width', index=1,
-      number=2, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='height', full_name='api_protocol.MangaViewer.Page.MangaPage.height', index=2,
-      number=3, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='type', full_name='api_protocol.MangaViewer.Page.MangaPage.type', index=3,
-      number=4, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='encryptionKey', full_name='api_protocol.MangaViewer.Page.MangaPage.encryptionKey', index=4,
-      number=5, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-    _MANGAVIEWER_PAGE_MANGAPAGE_TYPE,
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2552,
-  serialized_end=2750,
-)
-
-_MANGAVIEWER_PAGE = _descriptor.Descriptor(
-  name='Page',
-  full_name='api_protocol.MangaViewer.Page',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='page', full_name='api_protocol.MangaViewer.Page.page', index=0,
-      number=1, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_MANGAVIEWER_PAGE_MANGAPAGE, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2487,
-  serialized_end=2750,
-)
-
-_MANGAVIEWER = _descriptor.Descriptor(
-  name='MangaViewer',
-  full_name='api_protocol.MangaViewer',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='pages', full_name='api_protocol.MangaViewer.pages', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterId', full_name='api_protocol.MangaViewer.chapterId', index=1,
-      number=2, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapters', full_name='api_protocol.MangaViewer.chapters', index=2,
-      number=3, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='sns', full_name='api_protocol.MangaViewer.sns', index=3,
-      number=4, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='titleName', full_name='api_protocol.MangaViewer.titleName', index=4,
-      number=5, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterName', full_name='api_protocol.MangaViewer.chapterName', index=5,
-      number=6, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='numberOfComments', full_name='api_protocol.MangaViewer.numberOfComments', index=6,
-      number=7, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='isVerticalOnly', full_name='api_protocol.MangaViewer.isVerticalOnly', index=7,
-      number=8, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='titleId', full_name='api_protocol.MangaViewer.titleId', index=8,
-      number=9, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='startFromRight', full_name='api_protocol.MangaViewer.startFromRight', index=9,
-      number=10, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='country', full_name='api_protocol.MangaViewer.country', index=10,
-      number=11, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_MANGAVIEWER_PAGE, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2184,
-  serialized_end=2750,
-)
-
-
-_PROFILEVIEW_ICON = _descriptor.Descriptor(
-  name='Icon',
-  full_name='api_protocol.ProfileView.Icon',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='id', full_name='api_protocol.ProfileView.Icon.id', index=0,
-      number=1, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='url', full_name='api_protocol.ProfileView.Icon.url', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2864,
-  serialized_end=2895,
-)
-
-_PROFILEVIEW = _descriptor.Descriptor(
-  name='ProfileView',
-  full_name='api_protocol.ProfileView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='icons', full_name='api_protocol.ProfileView.icons', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='default', full_name='api_protocol.ProfileView.default', index=1,
-      number=3, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_PROFILEVIEW_ICON, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2753,
-  serialized_end=2895,
-)
-
-
-_UPDATEPROFILEVIEW = _descriptor.Descriptor(
-  name='UpdateProfileView',
-  full_name='api_protocol.UpdateProfileView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='status', full_name='api_protocol.UpdateProfileView.status', index=0,
-      number=1, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2897,
-  serialized_end=2932,
-)
-
-
-_FREETITLESVIEW_ITEM = _descriptor.Descriptor(
-  name='Item',
-  full_name='api_protocol.FreeTitlesView.Item',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='title', full_name='api_protocol.FreeTitlesView.Item.title', index=0,
-      number=1, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='lastUpdate', full_name='api_protocol.FreeTitlesView.Item.lastUpdate', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3004,
-  serialized_end=3066,
-)
-
-_FREETITLESVIEW = _descriptor.Descriptor(
-  name='FreeTitlesView',
-  full_name='api_protocol.FreeTitlesView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titles', full_name='api_protocol.FreeTitlesView.titles', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_FREETITLESVIEW_ITEM, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=2935,
-  serialized_end=3066,
-)
-
-
-_ALLVIEW = _descriptor.Descriptor(
-  name='AllView',
-  full_name='api_protocol.AllView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titles', full_name='api_protocol.AllView.titles', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3068,
-  serialized_end=3117,
-)
-
-
-_SETTINGSVIEW = _descriptor.Descriptor(
-  name='SettingsView',
-  full_name='api_protocol.SettingsView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='icon', full_name='api_protocol.SettingsView.icon', index=0,
-      number=1, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='username', full_name='api_protocol.SettingsView.username', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='counts', full_name='api_protocol.SettingsView.counts', index=2,
-      number=5, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3119,
-  serialized_end=3221,
-)
-
-
-_INITVIEW = _descriptor.Descriptor(
-  name='InitView',
-  full_name='api_protocol.InitView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='default', full_name='api_protocol.InitView.default', index=0,
-      number=1, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='counts', full_name='api_protocol.InitView.counts', index=1,
-      number=2, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3223,
-  serialized_end=3311,
-)
-
-
-_REGISTERVIEW = _descriptor.Descriptor(
-  name='RegisterView',
-  full_name='api_protocol.RegisterView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='secret', full_name='api_protocol.RegisterView.secret', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3313,
-  serialized_end=3343,
-)
-
-
-_HOMEVIEW_UPDATE_ITEM_METADATA = _descriptor.Descriptor(
-  name='Metadata',
-  full_name='api_protocol.HomeView.Update.Item.Metadata',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='title', full_name='api_protocol.HomeView.Update.Item.Metadata.title', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterId', full_name='api_protocol.HomeView.Update.Item.Metadata.chapterId', index=1,
-      number=2, type=5, cpp_type=1, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterName', full_name='api_protocol.HomeView.Update.Item.Metadata.chapterName', index=2,
-      number=3, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterSubTitle', full_name='api_protocol.HomeView.Update.Item.Metadata.chapterSubTitle', index=3,
-      number=4, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='language', full_name='api_protocol.HomeView.Update.Item.Metadata.language', index=4,
-      number=5, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3683,
-  serialized_end=3836,
-)
-
-_HOMEVIEW_UPDATE_ITEM = _descriptor.Descriptor(
-  name='Item',
-  full_name='api_protocol.HomeView.Update.Item',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titleName', full_name='api_protocol.HomeView.Update.Item.titleName', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterName', full_name='api_protocol.HomeView.Update.Item.chapterName', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='metadata', full_name='api_protocol.HomeView.Update.Item.metadata', index=2,
-      number=3, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_HOMEVIEW_UPDATE_ITEM_METADATA, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3571,
-  serialized_end=3836,
-)
-
-_HOMEVIEW_UPDATE = _descriptor.Descriptor(
-  name='Update',
-  full_name='api_protocol.HomeView.Update',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='category', full_name='api_protocol.HomeView.Update.category', index=0,
-      number=1, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='items', full_name='api_protocol.HomeView.Update.items', index=1,
-      number=2, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_HOMEVIEW_UPDATE_ITEM, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3491,
-  serialized_end=3836,
-)
-
-_HOMEVIEW_POPUP_RESOURCE = _descriptor.Descriptor(
-  name='Resource',
-  full_name='api_protocol.HomeView.Popup.Resource',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='sns', full_name='api_protocol.HomeView.Popup.Resource.sns', index=0,
-      number=1, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='imagePopup', full_name='api_protocol.HomeView.Popup.Resource.imagePopup', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3924,
-  serialized_end=3986,
-)
-
-_HOMEVIEW_POPUP = _descriptor.Descriptor(
-  name='Popup',
-  full_name='api_protocol.HomeView.Popup',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='resource', full_name='api_protocol.HomeView.Popup.resource', index=0,
-      number=4, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='viewCount', full_name='api_protocol.HomeView.Popup.viewCount', index=1,
-      number=5, type=5, cpp_type=1, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_HOMEVIEW_POPUP_RESOURCE, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3839,
-  serialized_end=3986,
-)
-
-_HOMEVIEW = _descriptor.Descriptor(
-  name='HomeView',
-  full_name='api_protocol.HomeView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='banners', full_name='api_protocol.HomeView.banners', index=0,
-      number=1, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='updates', full_name='api_protocol.HomeView.updates', index=1,
-      number=2, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='popup', full_name='api_protocol.HomeView.popup', index=2,
-      number=9, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_HOMEVIEW_UPDATE, _HOMEVIEW_POPUP, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3346,
-  serialized_end=3986,
-)
-
-
-_FEATUREDVIEW_FEATURED = _descriptor.Descriptor(
-  name='Featured',
-  full_name='api_protocol.FeaturedView.Featured',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='banner', full_name='api_protocol.FeaturedView.Featured.banner', index=0,
-      number=1, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='category', full_name='api_protocol.FeaturedView.Featured.category', index=1,
-      number=2, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=4180,
-  serialized_end=4270,
-)
-
-_FEATUREDVIEW = _descriptor.Descriptor(
-  name='FeaturedView',
-  full_name='api_protocol.FeaturedView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='topBanner', full_name='api_protocol.FeaturedView.topBanner', index=0,
-      number=1, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='topLeft', full_name='api_protocol.FeaturedView.topLeft', index=1,
-      number=2, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='topRight', full_name='api_protocol.FeaturedView.topRight', index=2,
-      number=3, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='featured', full_name='api_protocol.FeaturedView.featured', index=3,
-      number=4, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_FEATUREDVIEW_FEATURED, ],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=3989,
-  serialized_end=4270,
-)
-
-
-_TITLEDETAILVIEW_ALLLANGUAGE = _descriptor.Descriptor(
-  name='AllLanguage',
-  full_name='api_protocol.TitleDetailView.AllLanguage',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='titleId', full_name='api_protocol.TitleDetailView.AllLanguage.titleId', index=0,
-      number=1, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='language', full_name='api_protocol.TitleDetailView.AllLanguage.language', index=1,
-      number=2, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=5002,
-  serialized_end=5074,
-)
-
-_TITLEDETAILVIEW_CHAPTERS = _descriptor.Descriptor(
-  name='Chapters',
-  full_name='api_protocol.TitleDetailView.Chapters',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='count', full_name='api_protocol.TitleDetailView.Chapters.count', index=0,
-      number=1, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='firstChapterList', full_name='api_protocol.TitleDetailView.Chapters.firstChapterList', index=1,
-      number=2, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapterList', full_name='api_protocol.TitleDetailView.Chapters.chapterList', index=2,
-      number=3, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='lastChapterList', full_name='api_protocol.TitleDetailView.Chapters.lastChapterList', index=3,
-      number=4, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[],
-  enum_types=[
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=5077,
-  serialized_end=5243,
-)
-
-_TITLEDETAILVIEW = _descriptor.Descriptor(
-  name='TitleDetailView',
-  full_name='api_protocol.TitleDetailView',
-  filename=None,
-  file=DESCRIPTOR,
-  containing_type=None,
-  fields=[
-    _descriptor.FieldDescriptor(
-      name='title', full_name='api_protocol.TitleDetailView.title', index=0,
-      number=1, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='imageTitle', full_name='api_protocol.TitleDetailView.imageTitle', index=1,
-      number=2, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='overview', full_name='api_protocol.TitleDetailView.overview', index=2,
-      number=3, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='imageBackground', full_name='api_protocol.TitleDetailView.imageBackground', index=3,
-      number=4, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='nextTimeStamp', full_name='api_protocol.TitleDetailView.nextTimeStamp', index=4,
-      number=5, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='updateTiming', full_name='api_protocol.TitleDetailView.updateTiming', index=5,
-      number=6, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='viewingPeriodDescription', full_name='api_protocol.TitleDetailView.viewingPeriodDescription', index=6,
-      number=7, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='nonAppearanceInfo', full_name='api_protocol.TitleDetailView.nonAppearanceInfo', index=7,
-      number=8, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='banners', full_name='api_protocol.TitleDetailView.banners', index=8,
-      number=11, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='recommendedTitleList', full_name='api_protocol.TitleDetailView.recommendedTitleList', index=9,
-      number=12, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='sns', full_name='api_protocol.TitleDetailView.sns', index=10,
-      number=13, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='isSimulcastReleased', full_name='api_protocol.TitleDetailView.isSimulcastReleased', index=11,
-      number=14, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='isSubscribed', full_name='api_protocol.TitleDetailView.isSubscribed', index=12,
-      number=15, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='rating', full_name='api_protocol.TitleDetailView.rating', index=13,
-      number=16, type=14, cpp_type=8, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chaptersDescending', full_name='api_protocol.TitleDetailView.chaptersDescending', index=14,
-      number=17, type=8, cpp_type=7, label=1,
-      has_default_value=False, default_value=False,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='numberOfViews', full_name='api_protocol.TitleDetailView.numberOfViews', index=15,
-      number=18, type=13, cpp_type=3, label=1,
-      has_default_value=False, default_value=0,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='titleBanners', full_name='api_protocol.TitleDetailView.titleBanners', index=16,
-      number=20, type=11, cpp_type=10, label=1,
-      has_default_value=False, default_value=None,
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='allLanguage', full_name='api_protocol.TitleDetailView.allLanguage', index=17,
-      number=27, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='chapters', full_name='api_protocol.TitleDetailView.chapters', index=18,
-      number=28, type=11, cpp_type=10, label=3,
-      has_default_value=False, default_value=[],
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-    _descriptor.FieldDescriptor(
-      name='country', full_name='api_protocol.TitleDetailView.country', index=19,
-      number=30, type=9, cpp_type=9, label=1,
-      has_default_value=False, default_value=_b("").decode('utf-8'),
-      message_type=None, enum_type=None, containing_type=None,
-      is_extension=False, extension_scope=None,
-      options=None, file=DESCRIPTOR),
-  ],
-  extensions=[
-  ],
-  nested_types=[_TITLEDETAILVIEW_ALLLANGUAGE, _TITLEDETAILVIEW_CHAPTERS, ],
-  enum_types=[
-    _TITLEDETAILVIEW_UPDATETIMING,
-    _TITLEDETAILVIEW_RATING,
-  ],
-  options=None,
-  is_extendable=False,
-  syntax='proto3',
-  extension_ranges=[],
-  oneofs=[
-  ],
-  serialized_start=4273,
-  serialized_end=5438,
-)
-
-_BANNER.fields_by_name['sns'].message_type = _SNS
-_COUNT.fields_by_name['language'].enum_type = _LANGUAGE
-_TITLE.fields_by_name['language'].enum_type = _LANGUAGE
-_CATEGORY.fields_by_name['items'].message_type = _TITLE
-_RESPONSE.fields_by_name['success'].message_type = _SUCCESSRESULT
-_RESPONSE.fields_by_name['error'].message_type = _ERRORRESULT
-_ERRORRESULT_ITEM_BUTTON.containing_type = _ERRORRESULT_ITEM
-_ERRORRESULT_ITEM.fields_by_name['button'].message_type = _ERRORRESULT_ITEM_BUTTON
-_ERRORRESULT_ITEM.fields_by_name['language'].enum_type = _LANGUAGE
-_ERRORRESULT_ITEM.containing_type = _ERRORRESULT
-_ERRORRESULT.fields_by_name['default'].message_type = _ERRORRESULT_ITEM
-_ERRORRESULT.fields_by_name['display'].message_type = _ERRORRESULT_ITEM
-_ERRORRESULT.fields_by_name['allLanguage'].message_type = _ERRORRESULT_ITEM
-_SUCCESSRESULT.fields_by_name['registerView'].message_type = _REGISTERVIEW
-_SUCCESSRESULT.fields_by_name['featuredView'].message_type = _FEATUREDVIEW
-_SUCCESSRESULT.fields_by_name['rankingView'].message_type = _RANKINGVIEW
-_SUCCESSRESULT.fields_by_name['subscribedTitlesView'].message_type = _SUBSCRIBEDTITLESVIEW
-_SUCCESSRESULT.fields_by_name['titleDetailView'].message_type = _TITLEDETAILVIEW
-_SUCCESSRESULT.fields_by_name['commentView'].message_type = _COMMENTVIEW
-_SUCCESSRESULT.fields_by_name['mangaViewer'].message_type = _MANGAVIEWER
-_SUCCESSRESULT.fields_by_name['profileView'].message_type = _PROFILEVIEW
-_SUCCESSRESULT.fields_by_name['updateProfileView'].message_type = _UPDATEPROFILEVIEW
-_SUCCESSRESULT.fields_by_name['homeView'].message_type = _HOMEVIEW
-_SUCCESSRESULT.fields_by_name['allView'].message_type = _ALLVIEW
-_SUCCESSRESULT.fields_by_name['settingsView'].message_type = _SETTINGSVIEW
-_SUCCESSRESULT.fields_by_name['initView'].message_type = _INITVIEW
-_SUCCESSRESULT.fields_by_name['contentView'].message_type = _CONTENTVIEW
-_SUCCESSRESULT.fields_by_name['freeTitlesView'].message_type = _FREETITLESVIEW
-_CONTENTVIEW.fields_by_name['default'].enum_type = _LANGUAGE
-_CONTENTVIEW.fields_by_name['display'].enum_type = _LANGUAGE
-_CONTENTVIEW.fields_by_name['counts'].message_type = _COUNT
-_SUBSCRIBEDTITLESVIEW.fields_by_name['titles'].message_type = _TITLE
-_RANKINGVIEW.fields_by_name['titles'].message_type = _TITLE
-_COMMENTVIEW.fields_by_name['titles'].message_type = _TITLE
-_MANGAVIEWER_PAGE_MANGAPAGE.fields_by_name['type'].enum_type = _MANGAVIEWER_PAGE_MANGAPAGE_TYPE
-_MANGAVIEWER_PAGE_MANGAPAGE.containing_type = _MANGAVIEWER_PAGE
-_MANGAVIEWER_PAGE_MANGAPAGE_TYPE.containing_type = _MANGAVIEWER_PAGE_MANGAPAGE
-_MANGAVIEWER_PAGE.fields_by_name['page'].message_type = _MANGAVIEWER_PAGE_MANGAPAGE
-_MANGAVIEWER_PAGE.containing_type = _MANGAVIEWER
-_MANGAVIEWER.fields_by_name['pages'].message_type = _MANGAVIEWER_PAGE
-_MANGAVIEWER.fields_by_name['chapters'].message_type = _CHAPTER
-_MANGAVIEWER.fields_by_name['sns'].message_type = _SNS
-_PROFILEVIEW_ICON.containing_type = _PROFILEVIEW
-_PROFILEVIEW.fields_by_name['icons'].message_type = _PROFILEVIEW_ICON
-_PROFILEVIEW.fields_by_name['default'].message_type = _PROFILEVIEW_ICON
-_FREETITLESVIEW_ITEM.fields_by_name['title'].message_type = _TITLE
-_FREETITLESVIEW_ITEM.containing_type = _FREETITLESVIEW
-_FREETITLESVIEW.fields_by_name['titles'].message_type = _FREETITLESVIEW_ITEM
-_ALLVIEW.fields_by_name['titles'].message_type = _CATEGORY
-_SETTINGSVIEW.fields_by_name['icon'].message_type = _SNS
-_SETTINGSVIEW.fields_by_name['counts'].message_type = _COUNT
-_INITVIEW.fields_by_name['default'].enum_type = _LANGUAGE
-_INITVIEW.fields_by_name['counts'].message_type = _COUNT
-_HOMEVIEW_UPDATE_ITEM_METADATA.fields_by_name['title'].message_type = _TITLE
-_HOMEVIEW_UPDATE_ITEM_METADATA.fields_by_name['language'].enum_type = _LANGUAGE
-_HOMEVIEW_UPDATE_ITEM_METADATA.containing_type = _HOMEVIEW_UPDATE_ITEM
-_HOMEVIEW_UPDATE_ITEM.fields_by_name['metadata'].message_type = _HOMEVIEW_UPDATE_ITEM_METADATA
-_HOMEVIEW_UPDATE_ITEM.containing_type = _HOMEVIEW_UPDATE
-_HOMEVIEW_UPDATE.fields_by_name['items'].message_type = _HOMEVIEW_UPDATE_ITEM
-_HOMEVIEW_UPDATE.containing_type = _HOMEVIEW
-_HOMEVIEW_POPUP_RESOURCE.fields_by_name['sns'].message_type = _SNS
-_HOMEVIEW_POPUP_RESOURCE.containing_type = _HOMEVIEW_POPUP
-_HOMEVIEW_POPUP.fields_by_name['resource'].message_type = _HOMEVIEW_POPUP_RESOURCE
-_HOMEVIEW_POPUP.containing_type = _HOMEVIEW
-_HOMEVIEW.fields_by_name['banners'].message_type = _BANNER
-_HOMEVIEW.fields_by_name['updates'].message_type = _HOMEVIEW_UPDATE
-_HOMEVIEW.fields_by_name['popup'].message_type = _HOMEVIEW_POPUP
-_FEATUREDVIEW_FEATURED.fields_by_name['banner'].message_type = _BANNER
-_FEATUREDVIEW_FEATURED.fields_by_name['category'].message_type = _CATEGORY
-_FEATUREDVIEW_FEATURED.containing_type = _FEATUREDVIEW
-_FEATUREDVIEW.fields_by_name['topBanner'].message_type = _BANNER
-_FEATUREDVIEW.fields_by_name['topLeft'].message_type = _BANNER
-_FEATUREDVIEW.fields_by_name['topRight'].message_type = _BANNER
-_FEATUREDVIEW.fields_by_name['featured'].message_type = _FEATUREDVIEW_FEATURED
-_TITLEDETAILVIEW_ALLLANGUAGE.fields_by_name['language'].enum_type = _LANGUAGE
-_TITLEDETAILVIEW_ALLLANGUAGE.containing_type = _TITLEDETAILVIEW
-_TITLEDETAILVIEW_CHAPTERS.fields_by_name['firstChapterList'].message_type = _CHAPTER
-_TITLEDETAILVIEW_CHAPTERS.fields_by_name['chapterList'].message_type = _CHAPTER
-_TITLEDETAILVIEW_CHAPTERS.fields_by_name['lastChapterList'].message_type = _CHAPTER
-_TITLEDETAILVIEW_CHAPTERS.containing_type = _TITLEDETAILVIEW
-_TITLEDETAILVIEW.fields_by_name['title'].message_type = _TITLE
-_TITLEDETAILVIEW.fields_by_name['updateTiming'].enum_type = _TITLEDETAILVIEW_UPDATETIMING
-_TITLEDETAILVIEW.fields_by_name['banners'].message_type = _BANNER
-_TITLEDETAILVIEW.fields_by_name['recommendedTitleList'].message_type = _TITLE
-_TITLEDETAILVIEW.fields_by_name['sns'].message_type = _SNS
-_TITLEDETAILVIEW.fields_by_name['rating'].enum_type = _TITLEDETAILVIEW_RATING
-_TITLEDETAILVIEW.fields_by_name['titleBanners'].message_type = _BANNER
-_TITLEDETAILVIEW.fields_by_name['allLanguage'].message_type = _TITLEDETAILVIEW_ALLLANGUAGE
-_TITLEDETAILVIEW.fields_by_name['chapters'].message_type = _TITLEDETAILVIEW_CHAPTERS
-_TITLEDETAILVIEW_UPDATETIMING.containing_type = _TITLEDETAILVIEW
-_TITLEDETAILVIEW_RATING.containing_type = _TITLEDETAILVIEW
-DESCRIPTOR.message_types_by_name['Sns'] = _SNS
-DESCRIPTOR.message_types_by_name['Banner'] = _BANNER
-DESCRIPTOR.message_types_by_name['Count'] = _COUNT
-DESCRIPTOR.message_types_by_name['Chapter'] = _CHAPTER
-DESCRIPTOR.message_types_by_name['Title'] = _TITLE
-DESCRIPTOR.message_types_by_name['Category'] = _CATEGORY
-DESCRIPTOR.message_types_by_name['Response'] = _RESPONSE
-DESCRIPTOR.message_types_by_name['ErrorResult'] = _ERRORRESULT
-DESCRIPTOR.message_types_by_name['SuccessResult'] = _SUCCESSRESULT
-DESCRIPTOR.message_types_by_name['ContentView'] = _CONTENTVIEW
-DESCRIPTOR.message_types_by_name['SubscribedTitlesView'] = _SUBSCRIBEDTITLESVIEW
-DESCRIPTOR.message_types_by_name['RankingView'] = _RANKINGVIEW
-DESCRIPTOR.message_types_by_name['CommentView'] = _COMMENTVIEW
-DESCRIPTOR.message_types_by_name['MangaViewer'] = _MANGAVIEWER
-DESCRIPTOR.message_types_by_name['ProfileView'] = _PROFILEVIEW
-DESCRIPTOR.message_types_by_name['UpdateProfileView'] = _UPDATEPROFILEVIEW
-DESCRIPTOR.message_types_by_name['FreeTitlesView'] = _FREETITLESVIEW
-DESCRIPTOR.message_types_by_name['AllView'] = _ALLVIEW
-DESCRIPTOR.message_types_by_name['SettingsView'] = _SETTINGSVIEW
-DESCRIPTOR.message_types_by_name['InitView'] = _INITVIEW
-DESCRIPTOR.message_types_by_name['RegisterView'] = _REGISTERVIEW
-DESCRIPTOR.message_types_by_name['HomeView'] = _HOMEVIEW
-DESCRIPTOR.message_types_by_name['FeaturedView'] = _FEATUREDVIEW
-DESCRIPTOR.message_types_by_name['TitleDetailView'] = _TITLEDETAILVIEW
-DESCRIPTOR.enum_types_by_name['Language'] = _LANGUAGE
-_sym_db.RegisterFileDescriptor(DESCRIPTOR)
-
-Sns = _reflection.GeneratedProtocolMessageType('Sns', (_message.Message,), dict(
-  DESCRIPTOR = _SNS,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.Sns)
-  ))
-_sym_db.RegisterMessage(Sns)
-
-Banner = _reflection.GeneratedProtocolMessageType('Banner', (_message.Message,), dict(
-  DESCRIPTOR = _BANNER,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.Banner)
-  ))
-_sym_db.RegisterMessage(Banner)
-
-Count = _reflection.GeneratedProtocolMessageType('Count', (_message.Message,), dict(
-  DESCRIPTOR = _COUNT,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.Count)
-  ))
-_sym_db.RegisterMessage(Count)
-
-Chapter = _reflection.GeneratedProtocolMessageType('Chapter', (_message.Message,), dict(
-  DESCRIPTOR = _CHAPTER,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.Chapter)
-  ))
-_sym_db.RegisterMessage(Chapter)
-
-Title = _reflection.GeneratedProtocolMessageType('Title', (_message.Message,), dict(
-  DESCRIPTOR = _TITLE,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.Title)
-  ))
-_sym_db.RegisterMessage(Title)
-
-Category = _reflection.GeneratedProtocolMessageType('Category', (_message.Message,), dict(
-  DESCRIPTOR = _CATEGORY,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.Category)
-  ))
-_sym_db.RegisterMessage(Category)
-
-Response = _reflection.GeneratedProtocolMessageType('Response', (_message.Message,), dict(
-  DESCRIPTOR = _RESPONSE,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.Response)
-  ))
-_sym_db.RegisterMessage(Response)
-
-ErrorResult = _reflection.GeneratedProtocolMessageType('ErrorResult', (_message.Message,), dict(
-
-  Item = _reflection.GeneratedProtocolMessageType('Item', (_message.Message,), dict(
-
-    Button = _reflection.GeneratedProtocolMessageType('Button', (_message.Message,), dict(
-      DESCRIPTOR = _ERRORRESULT_ITEM_BUTTON,
-      __module__ = 'api_protocol_pb2'
-      # @@protoc_insertion_point(class_scope:api_protocol.ErrorResult.Item.Button)
-      ))
-    ,
-    DESCRIPTOR = _ERRORRESULT_ITEM,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.ErrorResult.Item)
-    ))
-  ,
-  DESCRIPTOR = _ERRORRESULT,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.ErrorResult)
-  ))
-_sym_db.RegisterMessage(ErrorResult)
-_sym_db.RegisterMessage(ErrorResult.Item)
-_sym_db.RegisterMessage(ErrorResult.Item.Button)
-
-SuccessResult = _reflection.GeneratedProtocolMessageType('SuccessResult', (_message.Message,), dict(
-  DESCRIPTOR = _SUCCESSRESULT,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.SuccessResult)
-  ))
-_sym_db.RegisterMessage(SuccessResult)
-
-ContentView = _reflection.GeneratedProtocolMessageType('ContentView', (_message.Message,), dict(
-  DESCRIPTOR = _CONTENTVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.ContentView)
-  ))
-_sym_db.RegisterMessage(ContentView)
-
-SubscribedTitlesView = _reflection.GeneratedProtocolMessageType('SubscribedTitlesView', (_message.Message,), dict(
-  DESCRIPTOR = _SUBSCRIBEDTITLESVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.SubscribedTitlesView)
-  ))
-_sym_db.RegisterMessage(SubscribedTitlesView)
-
-RankingView = _reflection.GeneratedProtocolMessageType('RankingView', (_message.Message,), dict(
-  DESCRIPTOR = _RANKINGVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.RankingView)
-  ))
-_sym_db.RegisterMessage(RankingView)
-
-CommentView = _reflection.GeneratedProtocolMessageType('CommentView', (_message.Message,), dict(
-  DESCRIPTOR = _COMMENTVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.CommentView)
-  ))
-_sym_db.RegisterMessage(CommentView)
-
-MangaViewer = _reflection.GeneratedProtocolMessageType('MangaViewer', (_message.Message,), dict(
-
-  Page = _reflection.GeneratedProtocolMessageType('Page', (_message.Message,), dict(
-
-    MangaPage = _reflection.GeneratedProtocolMessageType('MangaPage', (_message.Message,), dict(
-      DESCRIPTOR = _MANGAVIEWER_PAGE_MANGAPAGE,
-      __module__ = 'api_protocol_pb2'
-      # @@protoc_insertion_point(class_scope:api_protocol.MangaViewer.Page.MangaPage)
-      ))
-    ,
-    DESCRIPTOR = _MANGAVIEWER_PAGE,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.MangaViewer.Page)
-    ))
-  ,
-  DESCRIPTOR = _MANGAVIEWER,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.MangaViewer)
-  ))
-_sym_db.RegisterMessage(MangaViewer)
-_sym_db.RegisterMessage(MangaViewer.Page)
-_sym_db.RegisterMessage(MangaViewer.Page.MangaPage)
-
-ProfileView = _reflection.GeneratedProtocolMessageType('ProfileView', (_message.Message,), dict(
-
-  Icon = _reflection.GeneratedProtocolMessageType('Icon', (_message.Message,), dict(
-    DESCRIPTOR = _PROFILEVIEW_ICON,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.ProfileView.Icon)
-    ))
-  ,
-  DESCRIPTOR = _PROFILEVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.ProfileView)
-  ))
-_sym_db.RegisterMessage(ProfileView)
-_sym_db.RegisterMessage(ProfileView.Icon)
-
-UpdateProfileView = _reflection.GeneratedProtocolMessageType('UpdateProfileView', (_message.Message,), dict(
-  DESCRIPTOR = _UPDATEPROFILEVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.UpdateProfileView)
-  ))
-_sym_db.RegisterMessage(UpdateProfileView)
-
-FreeTitlesView = _reflection.GeneratedProtocolMessageType('FreeTitlesView', (_message.Message,), dict(
-
-  Item = _reflection.GeneratedProtocolMessageType('Item', (_message.Message,), dict(
-    DESCRIPTOR = _FREETITLESVIEW_ITEM,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.FreeTitlesView.Item)
-    ))
-  ,
-  DESCRIPTOR = _FREETITLESVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.FreeTitlesView)
-  ))
-_sym_db.RegisterMessage(FreeTitlesView)
-_sym_db.RegisterMessage(FreeTitlesView.Item)
-
-AllView = _reflection.GeneratedProtocolMessageType('AllView', (_message.Message,), dict(
-  DESCRIPTOR = _ALLVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.AllView)
-  ))
-_sym_db.RegisterMessage(AllView)
-
-SettingsView = _reflection.GeneratedProtocolMessageType('SettingsView', (_message.Message,), dict(
-  DESCRIPTOR = _SETTINGSVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.SettingsView)
-  ))
-_sym_db.RegisterMessage(SettingsView)
-
-InitView = _reflection.GeneratedProtocolMessageType('InitView', (_message.Message,), dict(
-  DESCRIPTOR = _INITVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.InitView)
-  ))
-_sym_db.RegisterMessage(InitView)
-
-RegisterView = _reflection.GeneratedProtocolMessageType('RegisterView', (_message.Message,), dict(
-  DESCRIPTOR = _REGISTERVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.RegisterView)
-  ))
-_sym_db.RegisterMessage(RegisterView)
-
-HomeView = _reflection.GeneratedProtocolMessageType('HomeView', (_message.Message,), dict(
-
-  Update = _reflection.GeneratedProtocolMessageType('Update', (_message.Message,), dict(
-
-    Item = _reflection.GeneratedProtocolMessageType('Item', (_message.Message,), dict(
-
-      Metadata = _reflection.GeneratedProtocolMessageType('Metadata', (_message.Message,), dict(
-        DESCRIPTOR = _HOMEVIEW_UPDATE_ITEM_METADATA,
-        __module__ = 'api_protocol_pb2'
-        # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Update.Item.Metadata)
-        ))
-      ,
-      DESCRIPTOR = _HOMEVIEW_UPDATE_ITEM,
-      __module__ = 'api_protocol_pb2'
-      # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Update.Item)
-      ))
-    ,
-    DESCRIPTOR = _HOMEVIEW_UPDATE,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Update)
-    ))
-  ,
-
-  Popup = _reflection.GeneratedProtocolMessageType('Popup', (_message.Message,), dict(
-
-    Resource = _reflection.GeneratedProtocolMessageType('Resource', (_message.Message,), dict(
-      DESCRIPTOR = _HOMEVIEW_POPUP_RESOURCE,
-      __module__ = 'api_protocol_pb2'
-      # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Popup.Resource)
-      ))
-    ,
-    DESCRIPTOR = _HOMEVIEW_POPUP,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Popup)
-    ))
-  ,
-  DESCRIPTOR = _HOMEVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.HomeView)
-  ))
-_sym_db.RegisterMessage(HomeView)
-_sym_db.RegisterMessage(HomeView.Update)
-_sym_db.RegisterMessage(HomeView.Update.Item)
-_sym_db.RegisterMessage(HomeView.Update.Item.Metadata)
-_sym_db.RegisterMessage(HomeView.Popup)
-_sym_db.RegisterMessage(HomeView.Popup.Resource)
-
-FeaturedView = _reflection.GeneratedProtocolMessageType('FeaturedView', (_message.Message,), dict(
-
-  Featured = _reflection.GeneratedProtocolMessageType('Featured', (_message.Message,), dict(
-    DESCRIPTOR = _FEATUREDVIEW_FEATURED,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.FeaturedView.Featured)
-    ))
-  ,
-  DESCRIPTOR = _FEATUREDVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.FeaturedView)
-  ))
-_sym_db.RegisterMessage(FeaturedView)
-_sym_db.RegisterMessage(FeaturedView.Featured)
-
-TitleDetailView = _reflection.GeneratedProtocolMessageType('TitleDetailView', (_message.Message,), dict(
-
-  AllLanguage = _reflection.GeneratedProtocolMessageType('AllLanguage', (_message.Message,), dict(
-    DESCRIPTOR = _TITLEDETAILVIEW_ALLLANGUAGE,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.TitleDetailView.AllLanguage)
-    ))
-  ,
-
-  Chapters = _reflection.GeneratedProtocolMessageType('Chapters', (_message.Message,), dict(
-    DESCRIPTOR = _TITLEDETAILVIEW_CHAPTERS,
-    __module__ = 'api_protocol_pb2'
-    # @@protoc_insertion_point(class_scope:api_protocol.TitleDetailView.Chapters)
-    ))
-  ,
-  DESCRIPTOR = _TITLEDETAILVIEW,
-  __module__ = 'api_protocol_pb2'
-  # @@protoc_insertion_point(class_scope:api_protocol.TitleDetailView)
-  ))
-_sym_db.RegisterMessage(TitleDetailView)
-_sym_db.RegisterMessage(TitleDetailView.AllLanguage)
-_sym_db.RegisterMessage(TitleDetailView.Chapters)
-
-
-# @@protoc_insertion_point(module_scope)
+# Generated by the protocol buffer compiler.  DO NOT EDIT!
+# source: api_protocol.proto
+
+import sys
+_b=sys.version_info[0]<3 and (lambda x:x) or (lambda x:x.encode('latin1'))
+from google.protobuf.internal import enum_type_wrapper
+from google.protobuf import descriptor as _descriptor
+from google.protobuf import message as _message
+from google.protobuf import reflection as _reflection
+from google.protobuf import symbol_database as _symbol_database
+from google.protobuf import descriptor_pb2
+# @@protoc_insertion_point(imports)
+
+_sym_db = _symbol_database.Default()
+
+
+
+
+DESCRIPTOR = _descriptor.FileDescriptor(
+  name='api_protocol.proto',
+  package='api_protocol',
+  syntax='proto3',
+  serialized_pb=_b('\n\x12\x61pi_protocol.proto\x12\x0c\x61pi_protocol\" \n\x03Sns\x12\x0c\n\x04\x62ody\x18\x01 \x01(\t\x12\x0b\n\x03url\x18\x02 \x01(\t\"P\n\x06\x42\x61nner\x12\x13\n\x0bimageBanner\x18\x01 \x01(\t\x12\x1e\n\x03sns\x18\x02 \x01(\x0b\x32\x11.api_protocol.Sns\x12\x11\n\tviewCount\x18\x03 \x01(\x05\"A\n\x05\x43ount\x12(\n\x08language\x18\x01 \x01(\x0e\x32\x16.api_protocol.Language\x12\x0e\n\x06titles\x18\x02 \x01(\x05\"\xcc\x01\n\x07\x43hapter\x12\x0f\n\x07titleId\x18\x01 \x01(\r\x12\x11\n\tchapterId\x18\x02 \x01(\r\x12\x11\n\ttitleName\x18\x03 \x01(\t\x12\x17\n\x0f\x63hapterSubTitle\x18\x04 \x01(\t\x12\x14\n\x0cthumbnailUrl\x18\x05 \x01(\t\x12\x16\n\x0estartTimeStamp\x18\x06 \x01(\t\x12\x14\n\x0c\x65ndTimeStamp\x18\x07 \x01(\t\x12\x15\n\ralreadyViewed\x18\x08 \x01(\x08\x12\x16\n\x0eisVerticalOnly\x18\t \x01(\x08\"\xa7\x01\n\x05Title\x12\x0f\n\x07titleId\x18\x01 \x01(\r\x12\x11\n\ttitleName\x18\x02 \x01(\t\x12\x0e\n\x06\x61uthor\x18\x03 \x01(\t\x12\x15\n\rimagePortrait\x18\x04 \x01(\t\x12\x16\n\x0eimageLandscape\x18\x05 \x01(\t\x12\x11\n\tviewCount\x18\x06 \x01(\r\x12(\n\x08language\x18\x07 \x01(\x0e\x32\x16.api_protocol.Language\"<\n\x08\x43\x61tegory\x12\x0c\n\x04name\x18\x01 \x01(\t\x12\"\n\x05items\x18\x02 \x03(\x0b\x32\x13.api_protocol.Title\"b\n\x08Response\x12,\n\x07success\x18\x01 \x01(\x0b\x32\x1b.api_protocol.SuccessResult\x12(\n\x05\x65rror\x18\x02 \x01(\x0b\x32\x19.api_protocol.ErrorResult\"\xc7\x02\n\x0b\x45rrorResult\x12/\n\x07\x64\x65\x66\x61ult\x18\x02 \x01(\x0b\x32\x1e.api_protocol.ErrorResult.Item\x12/\n\x07\x64isplay\x18\x03 \x01(\x0b\x32\x1e.api_protocol.ErrorResult.Item\x12\x33\n\x0b\x61llLanguage\x18\x05 \x03(\x0b\x32\x1e.api_protocol.ErrorResult.Item\x1a\xa0\x01\n\x04Item\x12\x0c\n\x04\x63ode\x18\x01 \x01(\t\x12\x0f\n\x07message\x18\x02 \x01(\t\x12\x35\n\x06\x62utton\x18\x05 \x01(\x0b\x32%.api_protocol.ErrorResult.Item.Button\x12(\n\x08language\x18\x06 \x01(\x0e\x32\x16.api_protocol.Language\x1a\x18\n\x06\x42utton\x12\x0e\n\x06\x61\x63tion\x18\x01 \x01(\t\"\x98\x06\n\rSuccessResult\x12\x19\n\x11isFeaturedUpdated\x18\x01 \x01(\x08\x12\x30\n\x0cregisterView\x18\x02 \x01(\x0b\x32\x1a.api_protocol.RegisterView\x12\x30\n\x0c\x66\x65\x61turedView\x18\x04 \x01(\x0b\x32\x1a.api_protocol.FeaturedView\x12.\n\x0brankingView\x18\x06 \x01(\x0b\x32\x19.api_protocol.RankingView\x12@\n\x14subscribedTitlesView\x18\x07 \x01(\x0b\x32\".api_protocol.SubscribedTitlesView\x12\x36\n\x0ftitleDetailView\x18\x08 \x01(\x0b\x32\x1d.api_protocol.TitleDetailView\x12.\n\x0b\x63ommentView\x18\t \x01(\x0b\x32\x19.api_protocol.CommentView\x12.\n\x0bmangaViewer\x18\n \x01(\x0b\x32\x19.api_protocol.MangaViewer\x12.\n\x0bprofileView\x18\r \x01(\x0b\x32\x19.api_protocol.ProfileView\x12:\n\x11updateProfileView\x18\x0e \x01(\x0b\x32\x1f.api_protocol.UpdateProfileView\x12(\n\x08homeView\x18\x18 \x01(\x0b\x32\x16.api_protocol.HomeView\x12&\n\x07\x61llView\x18\x19 \x01(\x0b\x32\x15.api_protocol.AllView\x12\x30\n\x0csettingsView\x18\x1a \x01(\x0b\x32\x1a.api_protocol.SettingsView\x12(\n\x08initView\x18\x1c \x01(\x0b\x32\x16.api_protocol.InitView\x12.\n\x0b\x63ontentView\x18\x1d \x01(\x0b\x32\x19.api_protocol.ContentView\x12\x34\n\x0e\x66reeTitlesView\x18! \x01(\x0b\x32\x1c.api_protocol.FreeTitlesView\"\x84\x01\n\x0b\x43ontentView\x12\'\n\x07\x64\x65\x66\x61ult\x18\x01 \x01(\x0e\x32\x16.api_protocol.Language\x12\'\n\x07\x64isplay\x18\x03 \x01(\x0e\x32\x16.api_protocol.Language\x12#\n\x06\x63ounts\x18\x05 \x03(\x0b\x32\x13.api_protocol.Count\";\n\x14SubscribedTitlesView\x12#\n\x06titles\x18\x01 \x03(\x0b\x32\x13.api_protocol.Title\"2\n\x0bRankingView\x12#\n\x06titles\x18\x01 \x03(\x0b\x32\x13.api_protocol.Title\"2\n\x0b\x43ommentView\x12#\n\x06titles\x18\x01 \x03(\x0b\x32\x13.api_protocol.Title\"\xb6\x04\n\x0bMangaViewer\x12-\n\x05pages\x18\x01 \x03(\x0b\x32\x1e.api_protocol.MangaViewer.Page\x12\x11\n\tchapterId\x18\x02 \x01(\r\x12\'\n\x08\x63hapters\x18\x03 \x03(\x0b\x32\x15.api_protocol.Chapter\x12\x1e\n\x03sns\x18\x04 \x01(\x0b\x32\x11.api_protocol.Sns\x12\x11\n\ttitleName\x18\x05 \x01(\t\x12\x13\n\x0b\x63hapterName\x18\x06 \x01(\t\x12\x18\n\x10numberOfComments\x18\x07 \x01(\r\x12\x16\n\x0eisVerticalOnly\x18\x08 \x01(\x08\x12\x0f\n\x07titleId\x18\t \x01(\r\x12\x16\n\x0estartFromRight\x18\n \x01(\x08\x12\x0f\n\x07\x63ountry\x18\x0b \x01(\t\x1a\x87\x02\n\x04Page\x12\x36\n\x04page\x18\x01 \x01(\x0b\x32(.api_protocol.MangaViewer.Page.MangaPage\x1a\xc6\x01\n\tMangaPage\x12\x11\n\timagePage\x18\x01 \x01(\t\x12\r\n\x05width\x18\x02 \x01(\r\x12\x0e\n\x06height\x18\x03 \x01(\r\x12;\n\x04type\x18\x04 \x01(\x0e\x32-.api_protocol.MangaViewer.Page.MangaPage.Type\x12\x15\n\rencryptionKey\x18\x05 \x01(\t\"3\n\x04Type\x12\n\n\x06SINGLE\x10\x00\x12\x08\n\x04LEFT\x10\x01\x12\t\n\x05RIGHT\x10\x02\x12\n\n\x06\x44OUBLE\x10\x03\"\x8e\x01\n\x0bProfileView\x12-\n\x05icons\x18\x01 \x03(\x0b\x32\x1e.api_protocol.ProfileView.Icon\x12/\n\x07\x64\x65\x66\x61ult\x18\x03 \x01(\x0b\x32\x1e.api_protocol.ProfileView.Icon\x1a\x1f\n\x04Icon\x12\n\n\x02id\x18\x01 \x01(\r\x12\x0b\n\x03url\x18\x02 \x01(\t\"#\n\x11UpdateProfileView\x12\x0e\n\x06status\x18\x01 \x01(\x08\"\x83\x01\n\x0e\x46reeTitlesView\x12\x31\n\x06titles\x18\x01 \x03(\x0b\x32!.api_protocol.FreeTitlesView.Item\x1a>\n\x04Item\x12\"\n\x05title\x18\x01 \x01(\x0b\x32\x13.api_protocol.Title\x12\x12\n\nlastUpdate\x18\x02 \x01(\t\"1\n\x07\x41llView\x12&\n\x06titles\x18\x01 \x03(\x0b\x32\x16.api_protocol.Category\"f\n\x0cSettingsView\x12\x1f\n\x04icon\x18\x01 \x01(\x0b\x32\x11.api_protocol.Sns\x12\x10\n\x08username\x18\x02 \x01(\t\x12#\n\x06\x63ounts\x18\x05 \x03(\x0b\x32\x13.api_protocol.Count\"X\n\x08InitView\x12\'\n\x07\x64\x65\x66\x61ult\x18\x01 \x01(\x0e\x32\x16.api_protocol.Language\x12#\n\x06\x63ounts\x18\x02 \x03(\x0b\x32\x13.api_protocol.Count\"\x1e\n\x0cRegisterView\x12\x0e\n\x06secret\x18\x01 \x01(\t\"\x80\x05\n\x08HomeView\x12%\n\x07\x62\x61nners\x18\x01 \x03(\x0b\x32\x14.api_protocol.Banner\x12.\n\x07updates\x18\x02 \x03(\x0b\x32\x1d.api_protocol.HomeView.Update\x12+\n\x05popup\x18\t \x01(\x0b\x32\x1c.api_protocol.HomeView.Popup\x1a\xd9\x02\n\x06Update\x12\x10\n\x08\x63\x61tegory\x18\x01 \x01(\t\x12\x31\n\x05items\x18\x02 \x03(\x0b\x32\".api_protocol.HomeView.Update.Item\x1a\x89\x02\n\x04Item\x12\x11\n\ttitleName\x18\x01 \x01(\t\x12\x13\n\x0b\x63hapterName\x18\x02 \x01(\t\x12=\n\x08metadata\x18\x03 \x01(\x0b\x32+.api_protocol.HomeView.Update.Item.Metadata\x1a\x99\x01\n\x08Metadata\x12\"\n\x05title\x18\x01 \x03(\x0b\x32\x13.api_protocol.Title\x12\x11\n\tchapterId\x18\x02 \x01(\x05\x12\x13\n\x0b\x63hapterName\x18\x03 \x01(\t\x12\x17\n\x0f\x63hapterSubTitle\x18\x04 \x01(\t\x12(\n\x08language\x18\x05 \x01(\x0e\x32\x16.api_protocol.Language\x1a\x93\x01\n\x05Popup\x12\x37\n\x08resource\x18\x04 \x01(\x0b\x32%.api_protocol.HomeView.Popup.Resource\x12\x11\n\tviewCount\x18\x05 \x01(\x05\x1a>\n\x08Resource\x12\x1e\n\x03sns\x18\x01 \x01(\x0b\x32\x11.api_protocol.Sns\x12\x12\n\nimagePopup\x18\x02 \x01(\t\"\x99\x02\n\x0c\x46\x65\x61turedView\x12\'\n\ttopBanner\x18\x01 \x01(\x0b\x32\x14.api_protocol.Banner\x12%\n\x07topLeft\x18\x02 \x01(\x0b\x32\x14.api_protocol.Banner\x12&\n\x08topRight\x18\x03 \x01(\x0b\x32\x14.api_protocol.Banner\x12\x35\n\x08\x66\x65\x61tured\x18\x04 \x03(\x0b\x32#.api_protocol.FeaturedView.Featured\x1aZ\n\x08\x46\x65\x61tured\x12$\n\x06\x62\x61nner\x18\x01 \x01(\x0b\x32\x14.api_protocol.Banner\x12(\n\x08\x63\x61tegory\x18\x02 \x01(\x0b\x32\x16.api_protocol.Category\"\x8d\t\n\x0fTitleDetailView\x12\"\n\x05title\x18\x01 \x01(\x0b\x32\x13.api_protocol.Title\x12\x12\n\nimageTitle\x18\x02 \x01(\t\x12\x10\n\x08overview\x18\x03 \x01(\t\x12\x17\n\x0fimageBackground\x18\x04 \x01(\t\x12\x15\n\rnextTimeStamp\x18\x05 \x01(\r\x12@\n\x0cupdateTiming\x18\x06 \x01(\x0e\x32*.api_protocol.TitleDetailView.UpdateTiming\x12 \n\x18viewingPeriodDescription\x18\x07 \x01(\t\x12\x19\n\x11nonAppearanceInfo\x18\x08 \x01(\t\x12%\n\x07\x62\x61nners\x18\x0b \x03(\x0b\x32\x14.api_protocol.Banner\x12\x31\n\x14recommendedTitleList\x18\x0c \x03(\x0b\x32\x13.api_protocol.Title\x12\x1e\n\x03sns\x18\r \x01(\x0b\x32\x11.api_protocol.Sns\x12\x1b\n\x13isSimulcastReleased\x18\x0e \x01(\x08\x12\x14\n\x0cisSubscribed\x18\x0f \x01(\x08\x12\x34\n\x06rating\x18\x10 \x01(\x0e\x32$.api_protocol.TitleDetailView.Rating\x12\x1a\n\x12\x63haptersDescending\x18\x11 \x01(\x08\x12\x15\n\rnumberOfViews\x18\x12 \x01(\r\x12*\n\x0ctitleBanners\x18\x14 \x01(\x0b\x32\x14.api_protocol.Banner\x12>\n\x0b\x61llLanguage\x18\x1b \x03(\x0b\x32).api_protocol.TitleDetailView.AllLanguage\x12\x38\n\x08\x63hapters\x18\x1c \x03(\x0b\x32&.api_protocol.TitleDetailView.Chapters\x12\x0f\n\x07\x63ountry\x18\x1e \x01(\t\x1aH\n\x0b\x41llLanguage\x12\x0f\n\x07titleId\x18\x01 \x01(\r\x12(\n\x08language\x18\x02 \x01(\x0e\x32\x16.api_protocol.Language\x1a\xa6\x01\n\x08\x43hapters\x12\r\n\x05\x63ount\x18\x01 \x01(\r\x12/\n\x10\x66irstChapterList\x18\x02 \x03(\x0b\x32\x15.api_protocol.Chapter\x12*\n\x0b\x63hapterList\x18\x03 \x03(\x0b\x32\x15.api_protocol.Chapter\x12.\n\x0flastChapterList\x18\x04 \x03(\x0b\x32\x15.api_protocol.Chapter\"\x86\x01\n\x0cUpdateTiming\x12\x11\n\rNOT_REGULARLY\x10\x00\x12\n\n\x06MONDAY\x10\x01\x12\x0b\n\x07TUESDAY\x10\x02\x12\r\n\tWEDNESDAY\x10\x03\x12\x0c\n\x08THURSDAY\x10\x04\x12\n\n\x06\x46RIDAY\x10\x05\x12\x0c\n\x08SATURDAY\x10\x06\x12\n\n\x06SUNDAY\x10\x07\x12\x07\n\x03\x44\x41Y\x10\x08\"8\n\x06Rating\x12\n\n\x06\x41LLAGE\x10\x00\x12\x08\n\x04TEEN\x10\x01\x12\x0c\n\x08TEENPLUS\x10\x02\x12\n\n\x06MATURE\x10\x03*g\n\x08Language\x12\x0b\n\x07\x45NGLISH\x10\x00\x12\x0b\n\x07SPANISH\x10\x01\x12\n\n\x06\x46RENCH\x10\x02\x12\x0e\n\nINDONESIAN\x10\x03\x12\x0e\n\nPORTUGUESE\x10\x04\x12\x0b\n\x07RUSSIAN\x10\x05\x12\x08\n\x04THAI\x10\x06\x62\x06proto3')
+)
+
+_LANGUAGE = _descriptor.EnumDescriptor(
+  name='Language',
+  full_name='api_protocol.Language',
+  filename=None,
+  file=DESCRIPTOR,
+  values=[
+    _descriptor.EnumValueDescriptor(
+      name='ENGLISH', index=0, number=0,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='SPANISH', index=1, number=1,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='FRENCH', index=2, number=2,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='INDONESIAN', index=3, number=3,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='PORTUGUESE', index=4, number=4,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='RUSSIAN', index=5, number=5,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='THAI', index=6, number=6,
+      options=None,
+      type=None),
+  ],
+  containing_type=None,
+  options=None,
+  serialized_start=5440,
+  serialized_end=5543,
+)
+_sym_db.RegisterEnumDescriptor(_LANGUAGE)
+
+Language = enum_type_wrapper.EnumTypeWrapper(_LANGUAGE)
+ENGLISH = 0
+SPANISH = 1
+FRENCH = 2
+INDONESIAN = 3
+PORTUGUESE = 4
+RUSSIAN = 5
+THAI = 6
+
+
+_MANGAVIEWER_PAGE_MANGAPAGE_TYPE = _descriptor.EnumDescriptor(
+  name='Type',
+  full_name='api_protocol.MangaViewer.Page.MangaPage.Type',
+  filename=None,
+  file=DESCRIPTOR,
+  values=[
+    _descriptor.EnumValueDescriptor(
+      name='SINGLE', index=0, number=0,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='LEFT', index=1, number=1,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='RIGHT', index=2, number=2,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='DOUBLE', index=3, number=3,
+      options=None,
+      type=None),
+  ],
+  containing_type=None,
+  options=None,
+  serialized_start=2699,
+  serialized_end=2750,
+)
+_sym_db.RegisterEnumDescriptor(_MANGAVIEWER_PAGE_MANGAPAGE_TYPE)
+
+_TITLEDETAILVIEW_UPDATETIMING = _descriptor.EnumDescriptor(
+  name='UpdateTiming',
+  full_name='api_protocol.TitleDetailView.UpdateTiming',
+  filename=None,
+  file=DESCRIPTOR,
+  values=[
+    _descriptor.EnumValueDescriptor(
+      name='NOT_REGULARLY', index=0, number=0,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='MONDAY', index=1, number=1,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='TUESDAY', index=2, number=2,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='WEDNESDAY', index=3, number=3,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='THURSDAY', index=4, number=4,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='FRIDAY', index=5, number=5,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='SATURDAY', index=6, number=6,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='SUNDAY', index=7, number=7,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='DAY', index=8, number=8,
+      options=None,
+      type=None),
+  ],
+  containing_type=None,
+  options=None,
+  serialized_start=5246,
+  serialized_end=5380,
+)
+_sym_db.RegisterEnumDescriptor(_TITLEDETAILVIEW_UPDATETIMING)
+
+_TITLEDETAILVIEW_RATING = _descriptor.EnumDescriptor(
+  name='Rating',
+  full_name='api_protocol.TitleDetailView.Rating',
+  filename=None,
+  file=DESCRIPTOR,
+  values=[
+    _descriptor.EnumValueDescriptor(
+      name='ALLAGE', index=0, number=0,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='TEEN', index=1, number=1,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='TEENPLUS', index=2, number=2,
+      options=None,
+      type=None),
+    _descriptor.EnumValueDescriptor(
+      name='MATURE', index=3, number=3,
+      options=None,
+      type=None),
+  ],
+  containing_type=None,
+  options=None,
+  serialized_start=5382,
+  serialized_end=5438,
+)
+_sym_db.RegisterEnumDescriptor(_TITLEDETAILVIEW_RATING)
+
+
+_SNS = _descriptor.Descriptor(
+  name='Sns',
+  full_name='api_protocol.Sns',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='body', full_name='api_protocol.Sns.body', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='url', full_name='api_protocol.Sns.url', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=36,
+  serialized_end=68,
+)
+
+
+_BANNER = _descriptor.Descriptor(
+  name='Banner',
+  full_name='api_protocol.Banner',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='imageBanner', full_name='api_protocol.Banner.imageBanner', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='sns', full_name='api_protocol.Banner.sns', index=1,
+      number=2, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='viewCount', full_name='api_protocol.Banner.viewCount', index=2,
+      number=3, type=5, cpp_type=1, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=70,
+  serialized_end=150,
+)
+
+
+_COUNT = _descriptor.Descriptor(
+  name='Count',
+  full_name='api_protocol.Count',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='language', full_name='api_protocol.Count.language', index=0,
+      number=1, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='titles', full_name='api_protocol.Count.titles', index=1,
+      number=2, type=5, cpp_type=1, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=152,
+  serialized_end=217,
+)
+
+
+_CHAPTER = _descriptor.Descriptor(
+  name='Chapter',
+  full_name='api_protocol.Chapter',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titleId', full_name='api_protocol.Chapter.titleId', index=0,
+      number=1, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterId', full_name='api_protocol.Chapter.chapterId', index=1,
+      number=2, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='titleName', full_name='api_protocol.Chapter.titleName', index=2,
+      number=3, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterSubTitle', full_name='api_protocol.Chapter.chapterSubTitle', index=3,
+      number=4, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='thumbnailUrl', full_name='api_protocol.Chapter.thumbnailUrl', index=4,
+      number=5, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='startTimeStamp', full_name='api_protocol.Chapter.startTimeStamp', index=5,
+      number=6, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='endTimeStamp', full_name='api_protocol.Chapter.endTimeStamp', index=6,
+      number=7, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='alreadyViewed', full_name='api_protocol.Chapter.alreadyViewed', index=7,
+      number=8, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='isVerticalOnly', full_name='api_protocol.Chapter.isVerticalOnly', index=8,
+      number=9, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=220,
+  serialized_end=424,
+)
+
+
+_TITLE = _descriptor.Descriptor(
+  name='Title',
+  full_name='api_protocol.Title',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titleId', full_name='api_protocol.Title.titleId', index=0,
+      number=1, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='titleName', full_name='api_protocol.Title.titleName', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='author', full_name='api_protocol.Title.author', index=2,
+      number=3, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='imagePortrait', full_name='api_protocol.Title.imagePortrait', index=3,
+      number=4, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='imageLandscape', full_name='api_protocol.Title.imageLandscape', index=4,
+      number=5, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='viewCount', full_name='api_protocol.Title.viewCount', index=5,
+      number=6, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='language', full_name='api_protocol.Title.language', index=6,
+      number=7, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=427,
+  serialized_end=594,
+)
+
+
+_CATEGORY = _descriptor.Descriptor(
+  name='Category',
+  full_name='api_protocol.Category',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='name', full_name='api_protocol.Category.name', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='items', full_name='api_protocol.Category.items', index=1,
+      number=2, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=596,
+  serialized_end=656,
+)
+
+
+_RESPONSE = _descriptor.Descriptor(
+  name='Response',
+  full_name='api_protocol.Response',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='success', full_name='api_protocol.Response.success', index=0,
+      number=1, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='error', full_name='api_protocol.Response.error', index=1,
+      number=2, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=658,
+  serialized_end=756,
+)
+
+
+_ERRORRESULT_ITEM_BUTTON = _descriptor.Descriptor(
+  name='Button',
+  full_name='api_protocol.ErrorResult.Item.Button',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='action', full_name='api_protocol.ErrorResult.Item.Button.action', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=1062,
+  serialized_end=1086,
+)
+
+_ERRORRESULT_ITEM = _descriptor.Descriptor(
+  name='Item',
+  full_name='api_protocol.ErrorResult.Item',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='code', full_name='api_protocol.ErrorResult.Item.code', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='message', full_name='api_protocol.ErrorResult.Item.message', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='button', full_name='api_protocol.ErrorResult.Item.button', index=2,
+      number=5, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='language', full_name='api_protocol.ErrorResult.Item.language', index=3,
+      number=6, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_ERRORRESULT_ITEM_BUTTON, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=926,
+  serialized_end=1086,
+)
+
+_ERRORRESULT = _descriptor.Descriptor(
+  name='ErrorResult',
+  full_name='api_protocol.ErrorResult',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='default', full_name='api_protocol.ErrorResult.default', index=0,
+      number=2, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='display', full_name='api_protocol.ErrorResult.display', index=1,
+      number=3, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='allLanguage', full_name='api_protocol.ErrorResult.allLanguage', index=2,
+      number=5, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_ERRORRESULT_ITEM, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=759,
+  serialized_end=1086,
+)
+
+
+_SUCCESSRESULT = _descriptor.Descriptor(
+  name='SuccessResult',
+  full_name='api_protocol.SuccessResult',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='isFeaturedUpdated', full_name='api_protocol.SuccessResult.isFeaturedUpdated', index=0,
+      number=1, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='registerView', full_name='api_protocol.SuccessResult.registerView', index=1,
+      number=2, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='featuredView', full_name='api_protocol.SuccessResult.featuredView', index=2,
+      number=4, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='rankingView', full_name='api_protocol.SuccessResult.rankingView', index=3,
+      number=6, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='subscribedTitlesView', full_name='api_protocol.SuccessResult.subscribedTitlesView', index=4,
+      number=7, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='titleDetailView', full_name='api_protocol.SuccessResult.titleDetailView', index=5,
+      number=8, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='commentView', full_name='api_protocol.SuccessResult.commentView', index=6,
+      number=9, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='mangaViewer', full_name='api_protocol.SuccessResult.mangaViewer', index=7,
+      number=10, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='profileView', full_name='api_protocol.SuccessResult.profileView', index=8,
+      number=13, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='updateProfileView', full_name='api_protocol.SuccessResult.updateProfileView', index=9,
+      number=14, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='homeView', full_name='api_protocol.SuccessResult.homeView', index=10,
+      number=24, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='allView', full_name='api_protocol.SuccessResult.allView', index=11,
+      number=25, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='settingsView', full_name='api_protocol.SuccessResult.settingsView', index=12,
+      number=26, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='initView', full_name='api_protocol.SuccessResult.initView', index=13,
+      number=28, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='contentView', full_name='api_protocol.SuccessResult.contentView', index=14,
+      number=29, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='freeTitlesView', full_name='api_protocol.SuccessResult.freeTitlesView', index=15,
+      number=33, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=1089,
+  serialized_end=1881,
+)
+
+
+_CONTENTVIEW = _descriptor.Descriptor(
+  name='ContentView',
+  full_name='api_protocol.ContentView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='default', full_name='api_protocol.ContentView.default', index=0,
+      number=1, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='display', full_name='api_protocol.ContentView.display', index=1,
+      number=3, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='counts', full_name='api_protocol.ContentView.counts', index=2,
+      number=5, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=1884,
+  serialized_end=2016,
+)
+
+
+_SUBSCRIBEDTITLESVIEW = _descriptor.Descriptor(
+  name='SubscribedTitlesView',
+  full_name='api_protocol.SubscribedTitlesView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titles', full_name='api_protocol.SubscribedTitlesView.titles', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2018,
+  serialized_end=2077,
+)
+
+
+_RANKINGVIEW = _descriptor.Descriptor(
+  name='RankingView',
+  full_name='api_protocol.RankingView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titles', full_name='api_protocol.RankingView.titles', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2079,
+  serialized_end=2129,
+)
+
+
+_COMMENTVIEW = _descriptor.Descriptor(
+  name='CommentView',
+  full_name='api_protocol.CommentView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titles', full_name='api_protocol.CommentView.titles', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2131,
+  serialized_end=2181,
+)
+
+
+_MANGAVIEWER_PAGE_MANGAPAGE = _descriptor.Descriptor(
+  name='MangaPage',
+  full_name='api_protocol.MangaViewer.Page.MangaPage',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='imagePage', full_name='api_protocol.MangaViewer.Page.MangaPage.imagePage', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='width', full_name='api_protocol.MangaViewer.Page.MangaPage.width', index=1,
+      number=2, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='height', full_name='api_protocol.MangaViewer.Page.MangaPage.height', index=2,
+      number=3, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='type', full_name='api_protocol.MangaViewer.Page.MangaPage.type', index=3,
+      number=4, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='encryptionKey', full_name='api_protocol.MangaViewer.Page.MangaPage.encryptionKey', index=4,
+      number=5, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+    _MANGAVIEWER_PAGE_MANGAPAGE_TYPE,
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2552,
+  serialized_end=2750,
+)
+
+_MANGAVIEWER_PAGE = _descriptor.Descriptor(
+  name='Page',
+  full_name='api_protocol.MangaViewer.Page',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='page', full_name='api_protocol.MangaViewer.Page.page', index=0,
+      number=1, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_MANGAVIEWER_PAGE_MANGAPAGE, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2487,
+  serialized_end=2750,
+)
+
+_MANGAVIEWER = _descriptor.Descriptor(
+  name='MangaViewer',
+  full_name='api_protocol.MangaViewer',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='pages', full_name='api_protocol.MangaViewer.pages', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterId', full_name='api_protocol.MangaViewer.chapterId', index=1,
+      number=2, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapters', full_name='api_protocol.MangaViewer.chapters', index=2,
+      number=3, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='sns', full_name='api_protocol.MangaViewer.sns', index=3,
+      number=4, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='titleName', full_name='api_protocol.MangaViewer.titleName', index=4,
+      number=5, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterName', full_name='api_protocol.MangaViewer.chapterName', index=5,
+      number=6, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='numberOfComments', full_name='api_protocol.MangaViewer.numberOfComments', index=6,
+      number=7, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='isVerticalOnly', full_name='api_protocol.MangaViewer.isVerticalOnly', index=7,
+      number=8, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='titleId', full_name='api_protocol.MangaViewer.titleId', index=8,
+      number=9, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='startFromRight', full_name='api_protocol.MangaViewer.startFromRight', index=9,
+      number=10, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='country', full_name='api_protocol.MangaViewer.country', index=10,
+      number=11, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_MANGAVIEWER_PAGE, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2184,
+  serialized_end=2750,
+)
+
+
+_PROFILEVIEW_ICON = _descriptor.Descriptor(
+  name='Icon',
+  full_name='api_protocol.ProfileView.Icon',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='id', full_name='api_protocol.ProfileView.Icon.id', index=0,
+      number=1, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='url', full_name='api_protocol.ProfileView.Icon.url', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2864,
+  serialized_end=2895,
+)
+
+_PROFILEVIEW = _descriptor.Descriptor(
+  name='ProfileView',
+  full_name='api_protocol.ProfileView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='icons', full_name='api_protocol.ProfileView.icons', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='default', full_name='api_protocol.ProfileView.default', index=1,
+      number=3, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_PROFILEVIEW_ICON, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2753,
+  serialized_end=2895,
+)
+
+
+_UPDATEPROFILEVIEW = _descriptor.Descriptor(
+  name='UpdateProfileView',
+  full_name='api_protocol.UpdateProfileView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='status', full_name='api_protocol.UpdateProfileView.status', index=0,
+      number=1, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2897,
+  serialized_end=2932,
+)
+
+
+_FREETITLESVIEW_ITEM = _descriptor.Descriptor(
+  name='Item',
+  full_name='api_protocol.FreeTitlesView.Item',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='title', full_name='api_protocol.FreeTitlesView.Item.title', index=0,
+      number=1, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='lastUpdate', full_name='api_protocol.FreeTitlesView.Item.lastUpdate', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3004,
+  serialized_end=3066,
+)
+
+_FREETITLESVIEW = _descriptor.Descriptor(
+  name='FreeTitlesView',
+  full_name='api_protocol.FreeTitlesView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titles', full_name='api_protocol.FreeTitlesView.titles', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_FREETITLESVIEW_ITEM, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=2935,
+  serialized_end=3066,
+)
+
+
+_ALLVIEW = _descriptor.Descriptor(
+  name='AllView',
+  full_name='api_protocol.AllView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titles', full_name='api_protocol.AllView.titles', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3068,
+  serialized_end=3117,
+)
+
+
+_SETTINGSVIEW = _descriptor.Descriptor(
+  name='SettingsView',
+  full_name='api_protocol.SettingsView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='icon', full_name='api_protocol.SettingsView.icon', index=0,
+      number=1, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='username', full_name='api_protocol.SettingsView.username', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='counts', full_name='api_protocol.SettingsView.counts', index=2,
+      number=5, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3119,
+  serialized_end=3221,
+)
+
+
+_INITVIEW = _descriptor.Descriptor(
+  name='InitView',
+  full_name='api_protocol.InitView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='default', full_name='api_protocol.InitView.default', index=0,
+      number=1, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='counts', full_name='api_protocol.InitView.counts', index=1,
+      number=2, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3223,
+  serialized_end=3311,
+)
+
+
+_REGISTERVIEW = _descriptor.Descriptor(
+  name='RegisterView',
+  full_name='api_protocol.RegisterView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='secret', full_name='api_protocol.RegisterView.secret', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3313,
+  serialized_end=3343,
+)
+
+
+_HOMEVIEW_UPDATE_ITEM_METADATA = _descriptor.Descriptor(
+  name='Metadata',
+  full_name='api_protocol.HomeView.Update.Item.Metadata',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='title', full_name='api_protocol.HomeView.Update.Item.Metadata.title', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterId', full_name='api_protocol.HomeView.Update.Item.Metadata.chapterId', index=1,
+      number=2, type=5, cpp_type=1, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterName', full_name='api_protocol.HomeView.Update.Item.Metadata.chapterName', index=2,
+      number=3, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterSubTitle', full_name='api_protocol.HomeView.Update.Item.Metadata.chapterSubTitle', index=3,
+      number=4, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='language', full_name='api_protocol.HomeView.Update.Item.Metadata.language', index=4,
+      number=5, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3683,
+  serialized_end=3836,
+)
+
+_HOMEVIEW_UPDATE_ITEM = _descriptor.Descriptor(
+  name='Item',
+  full_name='api_protocol.HomeView.Update.Item',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titleName', full_name='api_protocol.HomeView.Update.Item.titleName', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterName', full_name='api_protocol.HomeView.Update.Item.chapterName', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='metadata', full_name='api_protocol.HomeView.Update.Item.metadata', index=2,
+      number=3, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_HOMEVIEW_UPDATE_ITEM_METADATA, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3571,
+  serialized_end=3836,
+)
+
+_HOMEVIEW_UPDATE = _descriptor.Descriptor(
+  name='Update',
+  full_name='api_protocol.HomeView.Update',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='category', full_name='api_protocol.HomeView.Update.category', index=0,
+      number=1, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='items', full_name='api_protocol.HomeView.Update.items', index=1,
+      number=2, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_HOMEVIEW_UPDATE_ITEM, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3491,
+  serialized_end=3836,
+)
+
+_HOMEVIEW_POPUP_RESOURCE = _descriptor.Descriptor(
+  name='Resource',
+  full_name='api_protocol.HomeView.Popup.Resource',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='sns', full_name='api_protocol.HomeView.Popup.Resource.sns', index=0,
+      number=1, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='imagePopup', full_name='api_protocol.HomeView.Popup.Resource.imagePopup', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3924,
+  serialized_end=3986,
+)
+
+_HOMEVIEW_POPUP = _descriptor.Descriptor(
+  name='Popup',
+  full_name='api_protocol.HomeView.Popup',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='resource', full_name='api_protocol.HomeView.Popup.resource', index=0,
+      number=4, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='viewCount', full_name='api_protocol.HomeView.Popup.viewCount', index=1,
+      number=5, type=5, cpp_type=1, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_HOMEVIEW_POPUP_RESOURCE, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3839,
+  serialized_end=3986,
+)
+
+_HOMEVIEW = _descriptor.Descriptor(
+  name='HomeView',
+  full_name='api_protocol.HomeView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='banners', full_name='api_protocol.HomeView.banners', index=0,
+      number=1, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='updates', full_name='api_protocol.HomeView.updates', index=1,
+      number=2, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='popup', full_name='api_protocol.HomeView.popup', index=2,
+      number=9, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_HOMEVIEW_UPDATE, _HOMEVIEW_POPUP, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3346,
+  serialized_end=3986,
+)
+
+
+_FEATUREDVIEW_FEATURED = _descriptor.Descriptor(
+  name='Featured',
+  full_name='api_protocol.FeaturedView.Featured',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='banner', full_name='api_protocol.FeaturedView.Featured.banner', index=0,
+      number=1, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='category', full_name='api_protocol.FeaturedView.Featured.category', index=1,
+      number=2, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=4180,
+  serialized_end=4270,
+)
+
+_FEATUREDVIEW = _descriptor.Descriptor(
+  name='FeaturedView',
+  full_name='api_protocol.FeaturedView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='topBanner', full_name='api_protocol.FeaturedView.topBanner', index=0,
+      number=1, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='topLeft', full_name='api_protocol.FeaturedView.topLeft', index=1,
+      number=2, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='topRight', full_name='api_protocol.FeaturedView.topRight', index=2,
+      number=3, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='featured', full_name='api_protocol.FeaturedView.featured', index=3,
+      number=4, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_FEATUREDVIEW_FEATURED, ],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=3989,
+  serialized_end=4270,
+)
+
+
+_TITLEDETAILVIEW_ALLLANGUAGE = _descriptor.Descriptor(
+  name='AllLanguage',
+  full_name='api_protocol.TitleDetailView.AllLanguage',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='titleId', full_name='api_protocol.TitleDetailView.AllLanguage.titleId', index=0,
+      number=1, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='language', full_name='api_protocol.TitleDetailView.AllLanguage.language', index=1,
+      number=2, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=5002,
+  serialized_end=5074,
+)
+
+_TITLEDETAILVIEW_CHAPTERS = _descriptor.Descriptor(
+  name='Chapters',
+  full_name='api_protocol.TitleDetailView.Chapters',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='count', full_name='api_protocol.TitleDetailView.Chapters.count', index=0,
+      number=1, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='firstChapterList', full_name='api_protocol.TitleDetailView.Chapters.firstChapterList', index=1,
+      number=2, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapterList', full_name='api_protocol.TitleDetailView.Chapters.chapterList', index=2,
+      number=3, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='lastChapterList', full_name='api_protocol.TitleDetailView.Chapters.lastChapterList', index=3,
+      number=4, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[],
+  enum_types=[
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=5077,
+  serialized_end=5243,
+)
+
+_TITLEDETAILVIEW = _descriptor.Descriptor(
+  name='TitleDetailView',
+  full_name='api_protocol.TitleDetailView',
+  filename=None,
+  file=DESCRIPTOR,
+  containing_type=None,
+  fields=[
+    _descriptor.FieldDescriptor(
+      name='title', full_name='api_protocol.TitleDetailView.title', index=0,
+      number=1, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='imageTitle', full_name='api_protocol.TitleDetailView.imageTitle', index=1,
+      number=2, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='overview', full_name='api_protocol.TitleDetailView.overview', index=2,
+      number=3, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='imageBackground', full_name='api_protocol.TitleDetailView.imageBackground', index=3,
+      number=4, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='nextTimeStamp', full_name='api_protocol.TitleDetailView.nextTimeStamp', index=4,
+      number=5, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='updateTiming', full_name='api_protocol.TitleDetailView.updateTiming', index=5,
+      number=6, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='viewingPeriodDescription', full_name='api_protocol.TitleDetailView.viewingPeriodDescription', index=6,
+      number=7, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='nonAppearanceInfo', full_name='api_protocol.TitleDetailView.nonAppearanceInfo', index=7,
+      number=8, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='banners', full_name='api_protocol.TitleDetailView.banners', index=8,
+      number=11, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='recommendedTitleList', full_name='api_protocol.TitleDetailView.recommendedTitleList', index=9,
+      number=12, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='sns', full_name='api_protocol.TitleDetailView.sns', index=10,
+      number=13, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='isSimulcastReleased', full_name='api_protocol.TitleDetailView.isSimulcastReleased', index=11,
+      number=14, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='isSubscribed', full_name='api_protocol.TitleDetailView.isSubscribed', index=12,
+      number=15, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='rating', full_name='api_protocol.TitleDetailView.rating', index=13,
+      number=16, type=14, cpp_type=8, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chaptersDescending', full_name='api_protocol.TitleDetailView.chaptersDescending', index=14,
+      number=17, type=8, cpp_type=7, label=1,
+      has_default_value=False, default_value=False,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='numberOfViews', full_name='api_protocol.TitleDetailView.numberOfViews', index=15,
+      number=18, type=13, cpp_type=3, label=1,
+      has_default_value=False, default_value=0,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='titleBanners', full_name='api_protocol.TitleDetailView.titleBanners', index=16,
+      number=20, type=11, cpp_type=10, label=1,
+      has_default_value=False, default_value=None,
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='allLanguage', full_name='api_protocol.TitleDetailView.allLanguage', index=17,
+      number=27, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='chapters', full_name='api_protocol.TitleDetailView.chapters', index=18,
+      number=28, type=11, cpp_type=10, label=3,
+      has_default_value=False, default_value=[],
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+    _descriptor.FieldDescriptor(
+      name='country', full_name='api_protocol.TitleDetailView.country', index=19,
+      number=30, type=9, cpp_type=9, label=1,
+      has_default_value=False, default_value=_b("").decode('utf-8'),
+      message_type=None, enum_type=None, containing_type=None,
+      is_extension=False, extension_scope=None,
+      options=None, file=DESCRIPTOR),
+  ],
+  extensions=[
+  ],
+  nested_types=[_TITLEDETAILVIEW_ALLLANGUAGE, _TITLEDETAILVIEW_CHAPTERS, ],
+  enum_types=[
+    _TITLEDETAILVIEW_UPDATETIMING,
+    _TITLEDETAILVIEW_RATING,
+  ],
+  options=None,
+  is_extendable=False,
+  syntax='proto3',
+  extension_ranges=[],
+  oneofs=[
+  ],
+  serialized_start=4273,
+  serialized_end=5438,
+)
+
+_BANNER.fields_by_name['sns'].message_type = _SNS
+_COUNT.fields_by_name['language'].enum_type = _LANGUAGE
+_TITLE.fields_by_name['language'].enum_type = _LANGUAGE
+_CATEGORY.fields_by_name['items'].message_type = _TITLE
+_RESPONSE.fields_by_name['success'].message_type = _SUCCESSRESULT
+_RESPONSE.fields_by_name['error'].message_type = _ERRORRESULT
+_ERRORRESULT_ITEM_BUTTON.containing_type = _ERRORRESULT_ITEM
+_ERRORRESULT_ITEM.fields_by_name['button'].message_type = _ERRORRESULT_ITEM_BUTTON
+_ERRORRESULT_ITEM.fields_by_name['language'].enum_type = _LANGUAGE
+_ERRORRESULT_ITEM.containing_type = _ERRORRESULT
+_ERRORRESULT.fields_by_name['default'].message_type = _ERRORRESULT_ITEM
+_ERRORRESULT.fields_by_name['display'].message_type = _ERRORRESULT_ITEM
+_ERRORRESULT.fields_by_name['allLanguage'].message_type = _ERRORRESULT_ITEM
+_SUCCESSRESULT.fields_by_name['registerView'].message_type = _REGISTERVIEW
+_SUCCESSRESULT.fields_by_name['featuredView'].message_type = _FEATUREDVIEW
+_SUCCESSRESULT.fields_by_name['rankingView'].message_type = _RANKINGVIEW
+_SUCCESSRESULT.fields_by_name['subscribedTitlesView'].message_type = _SUBSCRIBEDTITLESVIEW
+_SUCCESSRESULT.fields_by_name['titleDetailView'].message_type = _TITLEDETAILVIEW
+_SUCCESSRESULT.fields_by_name['commentView'].message_type = _COMMENTVIEW
+_SUCCESSRESULT.fields_by_name['mangaViewer'].message_type = _MANGAVIEWER
+_SUCCESSRESULT.fields_by_name['profileView'].message_type = _PROFILEVIEW
+_SUCCESSRESULT.fields_by_name['updateProfileView'].message_type = _UPDATEPROFILEVIEW
+_SUCCESSRESULT.fields_by_name['homeView'].message_type = _HOMEVIEW
+_SUCCESSRESULT.fields_by_name['allView'].message_type = _ALLVIEW
+_SUCCESSRESULT.fields_by_name['settingsView'].message_type = _SETTINGSVIEW
+_SUCCESSRESULT.fields_by_name['initView'].message_type = _INITVIEW
+_SUCCESSRESULT.fields_by_name['contentView'].message_type = _CONTENTVIEW
+_SUCCESSRESULT.fields_by_name['freeTitlesView'].message_type = _FREETITLESVIEW
+_CONTENTVIEW.fields_by_name['default'].enum_type = _LANGUAGE
+_CONTENTVIEW.fields_by_name['display'].enum_type = _LANGUAGE
+_CONTENTVIEW.fields_by_name['counts'].message_type = _COUNT
+_SUBSCRIBEDTITLESVIEW.fields_by_name['titles'].message_type = _TITLE
+_RANKINGVIEW.fields_by_name['titles'].message_type = _TITLE
+_COMMENTVIEW.fields_by_name['titles'].message_type = _TITLE
+_MANGAVIEWER_PAGE_MANGAPAGE.fields_by_name['type'].enum_type = _MANGAVIEWER_PAGE_MANGAPAGE_TYPE
+_MANGAVIEWER_PAGE_MANGAPAGE.containing_type = _MANGAVIEWER_PAGE
+_MANGAVIEWER_PAGE_MANGAPAGE_TYPE.containing_type = _MANGAVIEWER_PAGE_MANGAPAGE
+_MANGAVIEWER_PAGE.fields_by_name['page'].message_type = _MANGAVIEWER_PAGE_MANGAPAGE
+_MANGAVIEWER_PAGE.containing_type = _MANGAVIEWER
+_MANGAVIEWER.fields_by_name['pages'].message_type = _MANGAVIEWER_PAGE
+_MANGAVIEWER.fields_by_name['chapters'].message_type = _CHAPTER
+_MANGAVIEWER.fields_by_name['sns'].message_type = _SNS
+_PROFILEVIEW_ICON.containing_type = _PROFILEVIEW
+_PROFILEVIEW.fields_by_name['icons'].message_type = _PROFILEVIEW_ICON
+_PROFILEVIEW.fields_by_name['default'].message_type = _PROFILEVIEW_ICON
+_FREETITLESVIEW_ITEM.fields_by_name['title'].message_type = _TITLE
+_FREETITLESVIEW_ITEM.containing_type = _FREETITLESVIEW
+_FREETITLESVIEW.fields_by_name['titles'].message_type = _FREETITLESVIEW_ITEM
+_ALLVIEW.fields_by_name['titles'].message_type = _CATEGORY
+_SETTINGSVIEW.fields_by_name['icon'].message_type = _SNS
+_SETTINGSVIEW.fields_by_name['counts'].message_type = _COUNT
+_INITVIEW.fields_by_name['default'].enum_type = _LANGUAGE
+_INITVIEW.fields_by_name['counts'].message_type = _COUNT
+_HOMEVIEW_UPDATE_ITEM_METADATA.fields_by_name['title'].message_type = _TITLE
+_HOMEVIEW_UPDATE_ITEM_METADATA.fields_by_name['language'].enum_type = _LANGUAGE
+_HOMEVIEW_UPDATE_ITEM_METADATA.containing_type = _HOMEVIEW_UPDATE_ITEM
+_HOMEVIEW_UPDATE_ITEM.fields_by_name['metadata'].message_type = _HOMEVIEW_UPDATE_ITEM_METADATA
+_HOMEVIEW_UPDATE_ITEM.containing_type = _HOMEVIEW_UPDATE
+_HOMEVIEW_UPDATE.fields_by_name['items'].message_type = _HOMEVIEW_UPDATE_ITEM
+_HOMEVIEW_UPDATE.containing_type = _HOMEVIEW
+_HOMEVIEW_POPUP_RESOURCE.fields_by_name['sns'].message_type = _SNS
+_HOMEVIEW_POPUP_RESOURCE.containing_type = _HOMEVIEW_POPUP
+_HOMEVIEW_POPUP.fields_by_name['resource'].message_type = _HOMEVIEW_POPUP_RESOURCE
+_HOMEVIEW_POPUP.containing_type = _HOMEVIEW
+_HOMEVIEW.fields_by_name['banners'].message_type = _BANNER
+_HOMEVIEW.fields_by_name['updates'].message_type = _HOMEVIEW_UPDATE
+_HOMEVIEW.fields_by_name['popup'].message_type = _HOMEVIEW_POPUP
+_FEATUREDVIEW_FEATURED.fields_by_name['banner'].message_type = _BANNER
+_FEATUREDVIEW_FEATURED.fields_by_name['category'].message_type = _CATEGORY
+_FEATUREDVIEW_FEATURED.containing_type = _FEATUREDVIEW
+_FEATUREDVIEW.fields_by_name['topBanner'].message_type = _BANNER
+_FEATUREDVIEW.fields_by_name['topLeft'].message_type = _BANNER
+_FEATUREDVIEW.fields_by_name['topRight'].message_type = _BANNER
+_FEATUREDVIEW.fields_by_name['featured'].message_type = _FEATUREDVIEW_FEATURED
+_TITLEDETAILVIEW_ALLLANGUAGE.fields_by_name['language'].enum_type = _LANGUAGE
+_TITLEDETAILVIEW_ALLLANGUAGE.containing_type = _TITLEDETAILVIEW
+_TITLEDETAILVIEW_CHAPTERS.fields_by_name['firstChapterList'].message_type = _CHAPTER
+_TITLEDETAILVIEW_CHAPTERS.fields_by_name['chapterList'].message_type = _CHAPTER
+_TITLEDETAILVIEW_CHAPTERS.fields_by_name['lastChapterList'].message_type = _CHAPTER
+_TITLEDETAILVIEW_CHAPTERS.containing_type = _TITLEDETAILVIEW
+_TITLEDETAILVIEW.fields_by_name['title'].message_type = _TITLE
+_TITLEDETAILVIEW.fields_by_name['updateTiming'].enum_type = _TITLEDETAILVIEW_UPDATETIMING
+_TITLEDETAILVIEW.fields_by_name['banners'].message_type = _BANNER
+_TITLEDETAILVIEW.fields_by_name['recommendedTitleList'].message_type = _TITLE
+_TITLEDETAILVIEW.fields_by_name['sns'].message_type = _SNS
+_TITLEDETAILVIEW.fields_by_name['rating'].enum_type = _TITLEDETAILVIEW_RATING
+_TITLEDETAILVIEW.fields_by_name['titleBanners'].message_type = _BANNER
+_TITLEDETAILVIEW.fields_by_name['allLanguage'].message_type = _TITLEDETAILVIEW_ALLLANGUAGE
+_TITLEDETAILVIEW.fields_by_name['chapters'].message_type = _TITLEDETAILVIEW_CHAPTERS
+_TITLEDETAILVIEW_UPDATETIMING.containing_type = _TITLEDETAILVIEW
+_TITLEDETAILVIEW_RATING.containing_type = _TITLEDETAILVIEW
+DESCRIPTOR.message_types_by_name['Sns'] = _SNS
+DESCRIPTOR.message_types_by_name['Banner'] = _BANNER
+DESCRIPTOR.message_types_by_name['Count'] = _COUNT
+DESCRIPTOR.message_types_by_name['Chapter'] = _CHAPTER
+DESCRIPTOR.message_types_by_name['Title'] = _TITLE
+DESCRIPTOR.message_types_by_name['Category'] = _CATEGORY
+DESCRIPTOR.message_types_by_name['Response'] = _RESPONSE
+DESCRIPTOR.message_types_by_name['ErrorResult'] = _ERRORRESULT
+DESCRIPTOR.message_types_by_name['SuccessResult'] = _SUCCESSRESULT
+DESCRIPTOR.message_types_by_name['ContentView'] = _CONTENTVIEW
+DESCRIPTOR.message_types_by_name['SubscribedTitlesView'] = _SUBSCRIBEDTITLESVIEW
+DESCRIPTOR.message_types_by_name['RankingView'] = _RANKINGVIEW
+DESCRIPTOR.message_types_by_name['CommentView'] = _COMMENTVIEW
+DESCRIPTOR.message_types_by_name['MangaViewer'] = _MANGAVIEWER
+DESCRIPTOR.message_types_by_name['ProfileView'] = _PROFILEVIEW
+DESCRIPTOR.message_types_by_name['UpdateProfileView'] = _UPDATEPROFILEVIEW
+DESCRIPTOR.message_types_by_name['FreeTitlesView'] = _FREETITLESVIEW
+DESCRIPTOR.message_types_by_name['AllView'] = _ALLVIEW
+DESCRIPTOR.message_types_by_name['SettingsView'] = _SETTINGSVIEW
+DESCRIPTOR.message_types_by_name['InitView'] = _INITVIEW
+DESCRIPTOR.message_types_by_name['RegisterView'] = _REGISTERVIEW
+DESCRIPTOR.message_types_by_name['HomeView'] = _HOMEVIEW
+DESCRIPTOR.message_types_by_name['FeaturedView'] = _FEATUREDVIEW
+DESCRIPTOR.message_types_by_name['TitleDetailView'] = _TITLEDETAILVIEW
+DESCRIPTOR.enum_types_by_name['Language'] = _LANGUAGE
+_sym_db.RegisterFileDescriptor(DESCRIPTOR)
+
+Sns = _reflection.GeneratedProtocolMessageType('Sns', (_message.Message,), dict(
+  DESCRIPTOR = _SNS,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.Sns)
+  ))
+_sym_db.RegisterMessage(Sns)
+
+Banner = _reflection.GeneratedProtocolMessageType('Banner', (_message.Message,), dict(
+  DESCRIPTOR = _BANNER,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.Banner)
+  ))
+_sym_db.RegisterMessage(Banner)
+
+Count = _reflection.GeneratedProtocolMessageType('Count', (_message.Message,), dict(
+  DESCRIPTOR = _COUNT,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.Count)
+  ))
+_sym_db.RegisterMessage(Count)
+
+Chapter = _reflection.GeneratedProtocolMessageType('Chapter', (_message.Message,), dict(
+  DESCRIPTOR = _CHAPTER,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.Chapter)
+  ))
+_sym_db.RegisterMessage(Chapter)
+
+Title = _reflection.GeneratedProtocolMessageType('Title', (_message.Message,), dict(
+  DESCRIPTOR = _TITLE,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.Title)
+  ))
+_sym_db.RegisterMessage(Title)
+
+Category = _reflection.GeneratedProtocolMessageType('Category', (_message.Message,), dict(
+  DESCRIPTOR = _CATEGORY,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.Category)
+  ))
+_sym_db.RegisterMessage(Category)
+
+Response = _reflection.GeneratedProtocolMessageType('Response', (_message.Message,), dict(
+  DESCRIPTOR = _RESPONSE,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.Response)
+  ))
+_sym_db.RegisterMessage(Response)
+
+ErrorResult = _reflection.GeneratedProtocolMessageType('ErrorResult', (_message.Message,), dict(
+
+  Item = _reflection.GeneratedProtocolMessageType('Item', (_message.Message,), dict(
+
+    Button = _reflection.GeneratedProtocolMessageType('Button', (_message.Message,), dict(
+      DESCRIPTOR = _ERRORRESULT_ITEM_BUTTON,
+      __module__ = 'api_protocol_pb2'
+      # @@protoc_insertion_point(class_scope:api_protocol.ErrorResult.Item.Button)
+      ))
+    ,
+    DESCRIPTOR = _ERRORRESULT_ITEM,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.ErrorResult.Item)
+    ))
+  ,
+  DESCRIPTOR = _ERRORRESULT,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.ErrorResult)
+  ))
+_sym_db.RegisterMessage(ErrorResult)
+_sym_db.RegisterMessage(ErrorResult.Item)
+_sym_db.RegisterMessage(ErrorResult.Item.Button)
+
+SuccessResult = _reflection.GeneratedProtocolMessageType('SuccessResult', (_message.Message,), dict(
+  DESCRIPTOR = _SUCCESSRESULT,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.SuccessResult)
+  ))
+_sym_db.RegisterMessage(SuccessResult)
+
+ContentView = _reflection.GeneratedProtocolMessageType('ContentView', (_message.Message,), dict(
+  DESCRIPTOR = _CONTENTVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.ContentView)
+  ))
+_sym_db.RegisterMessage(ContentView)
+
+SubscribedTitlesView = _reflection.GeneratedProtocolMessageType('SubscribedTitlesView', (_message.Message,), dict(
+  DESCRIPTOR = _SUBSCRIBEDTITLESVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.SubscribedTitlesView)
+  ))
+_sym_db.RegisterMessage(SubscribedTitlesView)
+
+RankingView = _reflection.GeneratedProtocolMessageType('RankingView', (_message.Message,), dict(
+  DESCRIPTOR = _RANKINGVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.RankingView)
+  ))
+_sym_db.RegisterMessage(RankingView)
+
+CommentView = _reflection.GeneratedProtocolMessageType('CommentView', (_message.Message,), dict(
+  DESCRIPTOR = _COMMENTVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.CommentView)
+  ))
+_sym_db.RegisterMessage(CommentView)
+
+MangaViewer = _reflection.GeneratedProtocolMessageType('MangaViewer', (_message.Message,), dict(
+
+  Page = _reflection.GeneratedProtocolMessageType('Page', (_message.Message,), dict(
+
+    MangaPage = _reflection.GeneratedProtocolMessageType('MangaPage', (_message.Message,), dict(
+      DESCRIPTOR = _MANGAVIEWER_PAGE_MANGAPAGE,
+      __module__ = 'api_protocol_pb2'
+      # @@protoc_insertion_point(class_scope:api_protocol.MangaViewer.Page.MangaPage)
+      ))
+    ,
+    DESCRIPTOR = _MANGAVIEWER_PAGE,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.MangaViewer.Page)
+    ))
+  ,
+  DESCRIPTOR = _MANGAVIEWER,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.MangaViewer)
+  ))
+_sym_db.RegisterMessage(MangaViewer)
+_sym_db.RegisterMessage(MangaViewer.Page)
+_sym_db.RegisterMessage(MangaViewer.Page.MangaPage)
+
+ProfileView = _reflection.GeneratedProtocolMessageType('ProfileView', (_message.Message,), dict(
+
+  Icon = _reflection.GeneratedProtocolMessageType('Icon', (_message.Message,), dict(
+    DESCRIPTOR = _PROFILEVIEW_ICON,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.ProfileView.Icon)
+    ))
+  ,
+  DESCRIPTOR = _PROFILEVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.ProfileView)
+  ))
+_sym_db.RegisterMessage(ProfileView)
+_sym_db.RegisterMessage(ProfileView.Icon)
+
+UpdateProfileView = _reflection.GeneratedProtocolMessageType('UpdateProfileView', (_message.Message,), dict(
+  DESCRIPTOR = _UPDATEPROFILEVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.UpdateProfileView)
+  ))
+_sym_db.RegisterMessage(UpdateProfileView)
+
+FreeTitlesView = _reflection.GeneratedProtocolMessageType('FreeTitlesView', (_message.Message,), dict(
+
+  Item = _reflection.GeneratedProtocolMessageType('Item', (_message.Message,), dict(
+    DESCRIPTOR = _FREETITLESVIEW_ITEM,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.FreeTitlesView.Item)
+    ))
+  ,
+  DESCRIPTOR = _FREETITLESVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.FreeTitlesView)
+  ))
+_sym_db.RegisterMessage(FreeTitlesView)
+_sym_db.RegisterMessage(FreeTitlesView.Item)
+
+AllView = _reflection.GeneratedProtocolMessageType('AllView', (_message.Message,), dict(
+  DESCRIPTOR = _ALLVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.AllView)
+  ))
+_sym_db.RegisterMessage(AllView)
+
+SettingsView = _reflection.GeneratedProtocolMessageType('SettingsView', (_message.Message,), dict(
+  DESCRIPTOR = _SETTINGSVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.SettingsView)
+  ))
+_sym_db.RegisterMessage(SettingsView)
+
+InitView = _reflection.GeneratedProtocolMessageType('InitView', (_message.Message,), dict(
+  DESCRIPTOR = _INITVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.InitView)
+  ))
+_sym_db.RegisterMessage(InitView)
+
+RegisterView = _reflection.GeneratedProtocolMessageType('RegisterView', (_message.Message,), dict(
+  DESCRIPTOR = _REGISTERVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.RegisterView)
+  ))
+_sym_db.RegisterMessage(RegisterView)
+
+HomeView = _reflection.GeneratedProtocolMessageType('HomeView', (_message.Message,), dict(
+
+  Update = _reflection.GeneratedProtocolMessageType('Update', (_message.Message,), dict(
+
+    Item = _reflection.GeneratedProtocolMessageType('Item', (_message.Message,), dict(
+
+      Metadata = _reflection.GeneratedProtocolMessageType('Metadata', (_message.Message,), dict(
+        DESCRIPTOR = _HOMEVIEW_UPDATE_ITEM_METADATA,
+        __module__ = 'api_protocol_pb2'
+        # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Update.Item.Metadata)
+        ))
+      ,
+      DESCRIPTOR = _HOMEVIEW_UPDATE_ITEM,
+      __module__ = 'api_protocol_pb2'
+      # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Update.Item)
+      ))
+    ,
+    DESCRIPTOR = _HOMEVIEW_UPDATE,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Update)
+    ))
+  ,
+
+  Popup = _reflection.GeneratedProtocolMessageType('Popup', (_message.Message,), dict(
+
+    Resource = _reflection.GeneratedProtocolMessageType('Resource', (_message.Message,), dict(
+      DESCRIPTOR = _HOMEVIEW_POPUP_RESOURCE,
+      __module__ = 'api_protocol_pb2'
+      # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Popup.Resource)
+      ))
+    ,
+    DESCRIPTOR = _HOMEVIEW_POPUP,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.HomeView.Popup)
+    ))
+  ,
+  DESCRIPTOR = _HOMEVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.HomeView)
+  ))
+_sym_db.RegisterMessage(HomeView)
+_sym_db.RegisterMessage(HomeView.Update)
+_sym_db.RegisterMessage(HomeView.Update.Item)
+_sym_db.RegisterMessage(HomeView.Update.Item.Metadata)
+_sym_db.RegisterMessage(HomeView.Popup)
+_sym_db.RegisterMessage(HomeView.Popup.Resource)
+
+FeaturedView = _reflection.GeneratedProtocolMessageType('FeaturedView', (_message.Message,), dict(
+
+  Featured = _reflection.GeneratedProtocolMessageType('Featured', (_message.Message,), dict(
+    DESCRIPTOR = _FEATUREDVIEW_FEATURED,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.FeaturedView.Featured)
+    ))
+  ,
+  DESCRIPTOR = _FEATUREDVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.FeaturedView)
+  ))
+_sym_db.RegisterMessage(FeaturedView)
+_sym_db.RegisterMessage(FeaturedView.Featured)
+
+TitleDetailView = _reflection.GeneratedProtocolMessageType('TitleDetailView', (_message.Message,), dict(
+
+  AllLanguage = _reflection.GeneratedProtocolMessageType('AllLanguage', (_message.Message,), dict(
+    DESCRIPTOR = _TITLEDETAILVIEW_ALLLANGUAGE,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.TitleDetailView.AllLanguage)
+    ))
+  ,
+
+  Chapters = _reflection.GeneratedProtocolMessageType('Chapters', (_message.Message,), dict(
+    DESCRIPTOR = _TITLEDETAILVIEW_CHAPTERS,
+    __module__ = 'api_protocol_pb2'
+    # @@protoc_insertion_point(class_scope:api_protocol.TitleDetailView.Chapters)
+    ))
+  ,
+  DESCRIPTOR = _TITLEDETAILVIEW,
+  __module__ = 'api_protocol_pb2'
+  # @@protoc_insertion_point(class_scope:api_protocol.TitleDetailView)
+  ))
+_sym_db.RegisterMessage(TitleDetailView)
+_sym_db.RegisterMessage(TitleDetailView.AllLanguage)
+_sym_db.RegisterMessage(TitleDetailView.Chapters)
+
+
+# @@protoc_insertion_point(module_scope)
```

### Comparing `pymangaplus-1.1.2/pymangaplus/client.py` & `pymangaplus-1.1.3/pymangaplus/client.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 from pymangaplus.utils import proto2dict
 
 
 class Client:
 
     def __init__(self, language: Language = Language.ENGLISH):
         self.language = language.value
-        self.secret = None
+        self._secret = None
         self.api = "https://jumpg-api.tokyo-cdn.com/api"
 
     def _request(self, **kwargs) -> dict:
         headers = {
             "accept": "*/*",
             "user-agent": "okhttp/4.9.0"
         }
```

### Comparing `pymangaplus-1.1.2/pymangaplus/utils.py` & `pymangaplus-1.1.3/pymangaplus/utils.py`

 * *Files identical despite different names*

### Comparing `pymangaplus-1.1.2/pymangaplus.egg-info/PKG-INFO` & `pymangaplus-1.1.3/pymangaplus.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pymangaplus
-Version: 1.1.2
+Version: 1.1.3
 Summary: Python client for the MangaPlus API.
 Home-page: https://github.com/hyugogirubato/pymangaplus
 Author: hyugogirubato
 Author-email: hyugogirubato@gmail.com
 License: GPL-3.0-only
 Keywords: client,manga,ebooks,manga-plus
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `pymangaplus-1.1.2/setup.py` & `pymangaplus-1.1.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="pymangaplus",
-    version="1.1.2",
+    version="1.1.3",
     author="hyugogirubato",
     author_email="hyugogirubato@gmail.com",
     description="Python client for the MangaPlus API.",
     long_description=open("README.md").read(),
     long_description_content_type="text/markdown",
     url="https://github.com/hyugogirubato/pymangaplus",
     packages=find_packages(),
```

