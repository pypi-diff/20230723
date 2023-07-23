# Comparing `tmp/biliarchiver-0.0.26.tar.gz` & `tmp/biliarchiver-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "biliarchiver-0.0.26.tar", max compression
+gzip compressed data, was "biliarchiver-0.0.9.tar", max compression
```

## Comparing `biliarchiver-0.0.26.tar` & `biliarchiver-0.0.9.tar`

### file list

```diff
@@ -1,20 +1,13 @@
--rw-r--r--   0        0        0      131 2023-07-07 09:38:51.631616 biliarchiver-0.0.26/README.md
--rw-r--r--   0        0        0     9440 2023-07-23 08:18:59.820773 biliarchiver-0.0.26/biliarchiver/_biliarchiver_upload_bvid.py
--rw-r--r--   0        0        0    10033 2023-07-23 08:18:45.472646 biliarchiver-0.0.26/biliarchiver/archive_bvid.py
--rw-r--r--   0        0        0     8198 2023-07-23 08:37:20.622502 biliarchiver-0.0.26/biliarchiver/cli_tools/bili_archive_bvids.py
--rw-r--r--   0        0        0     8092 2023-07-21 19:21:33.570874 biliarchiver-0.0.26/biliarchiver/cli_tools/bili_get_bvids.py
--rw-r--r--   0        0        0     2522 2023-07-23 08:20:04.085341 biliarchiver-0.0.26/biliarchiver/cli_tools/bili_upload.py
--rw-r--r--   0        0        0      413 2023-07-07 09:38:51.635616 biliarchiver-0.0.26/biliarchiver/cli_tools/biliarchiver.py
--rw-r--r--   0        0        0     2221 2023-07-20 09:58:51.188806 biliarchiver-0.0.26/biliarchiver/config.py
--rw-r--r--   0        0        0      375 2023-07-20 10:58:49.404609 biliarchiver-0.0.26/biliarchiver/exception.py
--rw-r--r--   0        0        0     1920 2023-07-20 15:27:30.175094 biliarchiver-0.0.26/biliarchiver/utils/black_list.py
--rw-r--r--   0        0        0     2724 2023-07-20 13:03:56.954965 biliarchiver-0.0.26/biliarchiver/utils/dirLock.py
--rw-r--r--   0        0        0      237 2023-07-07 09:38:51.635616 biliarchiver-0.0.26/biliarchiver/utils/ffmpeg.py
--rw-r--r--   0        0        0     1085 2023-07-18 04:24:04.652661 biliarchiver-0.0.26/biliarchiver/utils/http_patch.py
--rw-r--r--   0        0        0     1278 2023-07-07 09:38:51.635616 biliarchiver-0.0.26/biliarchiver/utils/identifier.py
--rw-r--r--   0        0        0      673 2023-07-23 08:17:41.212078 biliarchiver-0.0.26/biliarchiver/utils/storage.py
--rw-r--r--   0        0        0     1635 2023-07-20 11:10:13.662657 biliarchiver-0.0.26/biliarchiver/utils/version_check.py
--rw-r--r--   0        0        0       32 2023-07-23 08:39:15.159515 biliarchiver-0.0.26/biliarchiver/version.py
--rw-r--r--   0        0        0      665 2023-07-23 08:39:26.203612 biliarchiver-0.0.26/pyproject.toml
--rw-r--r--   0        0        0     1307 1970-01-01 00:00:00.000000 biliarchiver-0.0.26/setup.py
--rw-r--r--   0        0        0      686 1970-01-01 00:00:00.000000 biliarchiver-0.0.26/PKG-INFO
+-rw-r--r--   0        0        0      429 2023-06-06 20:05:41.529385 biliarchiver-0.0.9/README.md
+-rw-r--r--   0        0        0     7575 2023-06-06 19:48:46.123664 biliarchiver-0.0.9/biliarchiver/_biliarchiver_upload_bvid.py
+-rw-r--r--   0        0        0     7157 2023-06-06 19:12:07.431306 biliarchiver-0.0.9/biliarchiver/archive_bvid.py
+-rw-r--r--   0        0        0     4734 2023-06-07 04:48:33.598085 biliarchiver-0.0.9/biliarchiver/bili_archive_bvids.py
+-rw-r--r--   0        0        0     4133 2023-06-06 19:45:06.489235 biliarchiver-0.0.9/biliarchiver/bili_get_bvids.py
+-rw-r--r--   0        0        0     1490 2023-06-07 04:52:11.184454 biliarchiver-0.0.9/biliarchiver/bili_uploade.py
+-rw-r--r--   0        0        0     2018 2023-06-06 19:20:55.302758 biliarchiver-0.0.9/biliarchiver/config.py
+-rw-r--r--   0        0        0     2724 2023-06-06 05:53:18.324384 biliarchiver-0.0.9/biliarchiver/utils/dirLock.py
+-rw-r--r--   0        0        0     1278 2023-06-05 16:41:54.082484 biliarchiver-0.0.9/biliarchiver/utils/string.py
+-rw-r--r--   0        0        0       31 2023-06-06 19:35:41.648702 biliarchiver-0.0.9/biliarchiver/version.py
+-rw-r--r--   0        0        0      530 2023-06-07 04:58:02.482737 biliarchiver-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0     1379 1970-01-01 00:00:00.000000 biliarchiver-0.0.9/setup.py
+-rw-r--r--   0        0        0      892 1970-01-01 00:00:00.000000 biliarchiver-0.0.9/PKG-INFO
```

### Comparing `biliarchiver-0.0.26/biliarchiver/_biliarchiver_upload_bvid.py` & `biliarchiver-0.0.9/biliarchiver/_biliarchiver_upload_bvid.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,53 +1,45 @@
 import json
 import os
 from pathlib import Path
 import time
-from typing import List
 from internetarchive import get_item
 from requests import Response
 from rich import print
-from biliarchiver.exception import VideosBasePathNotFoundError
 
-from biliarchiver.utils.identifier import human_readable_upper_part_map
+from biliarchiver.utils.string import human_readable_upper_part_map
 from biliarchiver.config import BILIBILI_IDENTIFIER_PERFIX, config
 from biliarchiver.utils.dirLock import UploadLock, AlreadyRunningError
 from biliarchiver.version import BILI_ARCHIVER_VERSION
 
-def upload_bvid(bvid: str, *, update_existing: bool = False, collection: str):
+def upload_bvid(bvid):
     try:
         lock_dir = config.storage_home_dir / '.locks' / bvid
         os.makedirs(lock_dir, exist_ok=True)
         with UploadLock(lock_dir): # type: ignore
-            _upload_bvid(bvid, update_existing=update_existing, collection=collection)
+            _upload_bvid(bvid)
     except AlreadyRunningError:
         print(f'已经有一个上传 {bvid} 的进程在运行，跳过')
-    except VideosBasePathNotFoundError:
-        print(f'没有找到 {bvid} 对应的文件夹。可能是因已存在 IA item 而跳过了下载，或者你传入了错误的 bvid')
     except Exception as e:
         print(f'上传 {bvid} 时出错：')
         raise e
 
-def _upload_bvid(bvid: str, *, update_existing: bool = False, collection: str):
+def _upload_bvid(bvid: str):
     access_key, secret_key = read_ia_keys(config.ia_key_file)
 
     # identifier format: BiliBili-{bvid}_p{pid}-{upper_part} 
     upper_part = human_readable_upper_part_map(string=bvid, backward=True)
     OLD_videos_basepath: Path = config.storage_home_dir / 'videos' / bvid
     videos_basepath: Path = config.storage_home_dir / 'videos' / f'{bvid}-{upper_part}'
-
     if os.path.exists(OLD_videos_basepath):
         print(f'检测到旧的视频主目录 {OLD_videos_basepath}，将其重命名为 {videos_basepath}...')
         os.rename(OLD_videos_basepath, videos_basepath)
-
-    if not os.path.exists(videos_basepath):
-        raise VideosBasePathNotFoundError(f'{videos_basepath}')
     for local_identifier in os.listdir(videos_basepath):
         remote_identifier = f'{local_identifier}-{upper_part}'
-        if os.path.exists(f'{videos_basepath}/{local_identifier}/_uploaded.mark') and not update_existing:
+        if os.path.exists(f'{videos_basepath}/{local_identifier}/_uploaded.mark'):
             print(f'{local_identifier} => {remote_identifier} 已经上传过了(_uploaded.mark)')
             continue
         if local_identifier.startswith('_') :
             print(f'跳过 {local_identifier}')
             continue
         if not local_identifier.startswith(BILIBILI_IDENTIFIER_PERFIX):
             print(f'{local_identifier} 不是以 {BILIBILI_IDENTIFIER_PERFIX} 开头的正确 local_identifier')
@@ -57,15 +49,15 @@
             continue
 
         pid = local_identifier.split('_')[-1][1:]
         file_basename = local_identifier[len(BILIBILI_IDENTIFIER_PERFIX)+1:]
 
         print(f'=== 开始上传 {local_identifier} => {remote_identifier} ===')
         item = get_item(remote_identifier)
-        if item.exists and not update_existing:
+        if item.exists:
             print(f'item {remote_identifier} 已存在(item.exists)')
             if item.metadata.get("upload-state") == "uploaded":
                 print(f'{remote_identifier} 已经上传过了，跳过(item.metadata.uploaded)')
                 with open(f'{videos_basepath}/{local_identifier}/_uploaded.mark', 'w', encoding='utf-8') as f:
                     f.write('')
                 continue
         filedict = {} # "remote filename": "local filename"
@@ -78,18 +70,17 @@
 
         for filename in os.listdir(f'{videos_basepath}/{local_identifier}'):
             file = f'{videos_basepath}/{local_identifier}/{filename}'
             if os.path.isfile(file):
                 if os.path.basename(file).startswith('_'):
                     continue
                 if not os.path.isfile(file):
-                   continue
+                    continue
                 filedict[filename] = file
-
-        assert f'{file_basename}.mp4' in filedict
+        
 
         # IA 去重
         for file_in_item in item.files:
             if file_in_item["name"] in filedict:
                 filedict.pop(file_in_item["name"])
                 print(f"File {file_in_item['name']} already exists in {remote_identifier}.")
 
@@ -110,46 +101,27 @@
                 cid = page['cid']
                 p_part = page['part']
                 break
 
         assert cid is not None
         assert p_part is not None
 
-        aid = bv_info['data']['View']['aid']
-        owner_mid = bv_info['data']['View']['owner']['mid']
-        owner_creator: str = bv_info['data']['View']['owner']['name'] # UP 主
-
-        mids: List[int] = [owner_mid]
-        creators: List[str] = [owner_creator]
-        if bv_info['data']['View'].get('staff') is not None:
-            mids = [] # owner_mid 在 staff 也有
-            creators = []
-            for staff in bv_info['data']['View']['staff']:
-                mids.append(staff['mid']) if staff['mid'] not in mids else None
-                creators.append(staff['name']) if staff['name'] not in creators else None
-        external_identifier = [f"urn:bilibili:video:aid:{aid}",
-                               f"urn:bilibili:video:bvid:{bvid}",
-                               f"urn:bilibili:video:cid:{cid}"]
-        for mid in mids:
-            external_identifier.append(f"urn:bilibili:video:mid:{mid}")
-
         md = {
             "mediatype": "movies",
-            "collection": collection,
+            "collection": 'opensource_movies',
             "title": bv_info['data']['View']['title'] + f' P{pid} ' + p_part ,
             "description": remote_identifier + ' uploading...',
-            'creator': creators if len(creators) > 1 else owner_creator, # type: list[str] | str
+            'creator': bv_info['data']['View']['owner']['name'], # UP 主
             # UTC time
-            'date': time.strftime("%Y-%m-%d %H:%M:%S", time.gmtime(pubdate)),
+            'date': time.strftime("%Y-%m-%d", time.gmtime(pubdate)),
             'year': time.strftime("%Y", time.gmtime(pubdate)),
-            # 'aid': aid,
-            # 'bvid': bvid,
-            # 'cid': cid,
-            # 'mid': mid,
-            "external-identifier": external_identifier,
+            'aid': bv_info['data']['View']['aid'],
+            'bvid': bvid,
+            'cid': cid,
+            'mid': bv_info['data']['View']['owner']['mid'],
             "subject": "; ".join(
                 tags
             ),  # Keywords should be separated by ; but it doesn't matter much; the alternative is to set one per field with subject[0], subject[1], ...
             "upload-state": "uploading",
             'originalurl': f'https://www.bilibili.com/video/{bvid}/?p={pid}',
             'scanner': f'biliarchiver v{BILI_ARCHIVER_VERSION} (dev)',
         }
@@ -163,33 +135,29 @@
                 access_key=access_key,
                 secret_key=secret_key,
                 verbose=True,
                 queue_derive=True,
                 retries=5,
             )
 
-        tries = 100
+        tries = 30
         item = get_item(remote_identifier) # refresh item
         while not item.exists and tries > 0:
             print(f"Waiting for item to be created ({tries})  ...", end='\r')
             time.sleep(30)
             item = get_item(remote_identifier)
             tries -= 1
 
         new_md = {}
         if item.metadata.get("upload-state") != "uploaded":
             new_md.update({"upload-state": "uploaded"})
-        if item.metadata.get("creator") != md['creator']:
-            new_md.update({"creator": md['creator']})
-        if item.metadata.get("description", "") != bv_info['data']['View']['desc']:
+        if item.metadata.get("description") != bv_info['data']['View']['desc']:
             new_md.update({"description": bv_info['data']['View']['desc']})
         if item.metadata.get("scanner") != md['scanner']:
             new_md.update({"scanner": md['scanner']})
-        if item.metadata.get("external-identifier") != md['external-identifier']:
-            new_md.update({"external-identifier": md['external-identifier']})
         if new_md:
             print(f"Updating metadata:")
             print(new_md)
             r = item.modify_metadata(
                 metadata=new_md,
                 access_key=access_key,
                 secret_key=secret_key,
```

### Comparing `biliarchiver-0.0.26/biliarchiver/archive_bvid.py` & `biliarchiver-0.0.9/biliarchiver/archive_bvid.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,26 +1,25 @@
 import asyncio
 import os
 from pathlib import Path
-from typing import Union
 
 import aiofiles
 import httpx
 from bilix.download.utils import raise_api_error, req_retry
 from bilix.exception import APIError
 
 from bilix.sites.bilibili import api
 
 from rich import print
 import json
 
 from bilix.sites.bilibili.downloader import DownloaderBilibili
 from biliarchiver.config import BILIBILI_IDENTIFIER_PERFIX
 from biliarchiver.config import config
-from biliarchiver.utils.identifier import human_readable_upper_part_map
+from biliarchiver.utils.string import human_readable_upper_part_map
 
 @raise_api_error
 async def new_get_subtitle_info(client: httpx.AsyncClient, bvid, cid):
     params = {'bvid': bvid, 'cid': cid}
     res = await req_retry(client, 'https://api.bilibili.com/x/player/v2', params=params)
     info = json.loads(res.text)
     if info['code'] == -400:
@@ -32,27 +31,14 @@
     # lang: zh-CN
 
   # return [[f'http:{i["subtitle_url"]}', i['lan_doc']] for i in info['data']['subtitle']['subtitles']]
     return [[f'http:{i["subtitle_url"]}', i['lan']] for i in info['data']['subtitle']['subtitles']]
 api.get_subtitle_info = new_get_subtitle_info
 
 
-@raise_api_error
-async def new_get_video_info(client: httpx.AsyncClient, url: str):
-    """ 
-    monkey patch 一下，只使用 API 获取 video_info
-    理由：
-        - API 目前只支持一般的 AV/BV 视频，可以预防我们不小心下到了番剧/影视剧之类的版权内容
-        - 如果缺 url 对应的分P，bilix 那边会报 AssertionError(f"没有找到分P: p{selected_page_num}，请检查输入")
-        - 对于一些老视频， _get_video_info_from_html() 只会返回烦人且不稳定的 durl 资源。而 API 只会请求 dash 资源。
-    """
-    # print("using api")
-    return await api._get_video_info_from_api(client, url)
-api.get_video_info = new_get_video_info
-
 async def archive_bvid(d: DownloaderBilibili, bvid: str, logined: bool=False):
     assert d.hierarchy is True, 'hierarchy 必须为 True' # 为保持后续目录结构、文件命名的一致性
     assert d.client.cookies.get('SESSDATA') is not None, 'sess_data 不能为空' # 开个大会员呗，能下 4k 呢。
     assert logined is True, '请先检查 SESSDATA 是否过期，再将 logined 设置为 True' # 防误操作
 
     upper_part = human_readable_upper_part_map(string=bvid, backward=True)
     OLD_videos_basepath: Path = config.storage_home_dir / 'videos' / bvid
@@ -73,32 +59,24 @@
 
     os.makedirs(videos_basepath, exist_ok=True)
 
     pid = 0
     for page in first_video_info.pages:
         pid += 1 # pid 从 1 开始
         if not page.p_url.endswith(f'?p={pid}'):
-            raise NotImplementedError(f'{bvid} 的 P{pid} 不存在 (可能视频被 UP主/B站 删了)，请报告此问题，我们需要这个样本！')
+            print(f'{bvid} 的 P{pid} 不存在 (可能视频被 UP主/B站 删了)')
+            continue
 
         file_basename = f'{bvid}_p{pid}'
         video_basepath = videos_basepath / f'{BILIBILI_IDENTIFIER_PERFIX}-{file_basename}'
         video_extrapath = video_basepath / 'extra'
         if os.path.exists(f'{video_basepath}/_downloaded.mark'):
             print(f'{file_basename}: 已经下载过了')
             continue
 
-        def delete_cache(reason: str = ''):
-            if not os.path.exists(video_basepath):
-                return
-            _files_in_video_basepath = os.listdir(video_basepath)
-            for _file in _files_in_video_basepath:
-                if _file.startswith(file_basename):
-                    print(f'{file_basename}: {reason}，删除缓存: {_file}')
-                    os.remove(video_basepath / _file)
-        delete_cache('为防出错，清空上次未完成的下载缓存')
         video_info = await api.get_video_info(d.client, page.p_url)
         print(f'{file_basename}: {video_info.title}...')
         os.makedirs(video_basepath, exist_ok=True)
         os.makedirs(video_extrapath, exist_ok=True)
 
 
         old_p_name = video_info.pages[video_info.p].p_name
@@ -108,79 +86,51 @@
         video_info.pages[video_info.p].p_name = file_basename # 所以这里覆盖 p_name 为 file_basename
         video_info.h1_title = 'iiiiii' * 50 # 然后假装超长标题
         # 这样 bilix 保存的文件名就是我们想要的了（谁叫 bilix 不支持自定义文件名呢）
         # NOTE: p_name 似乎也不宜过长，否则还是会被 bilix 截断。
         # 但是我们以 {bvid}_p{pid} 作为文件名，这个长度是没问题的。
 
 
+        # 选择编码，优先 hevc，没有的话就 avc
+        # 不选 av0 ，毕竟目前没几个设备能拖得动
         codec = None
-        quality = None
         if video_info.dash:
-            # 选择编码 dvh->hev->avc
-            # 不选 av0 ，毕竟目前没几个设备能拖得动
-            codec_candidates = ['dvh', 'hev', 'avc']
-            for codec_candidate in codec_candidates:
+            for media in video_info.dash.videos:
+                if media.codec.startswith('hev'):
+                    codec = media.codec
+                    print(f'{file_basename}: "{codec}" "{media.quality}" ...')
+                    break
+            if codec is None:
                 for media in video_info.dash.videos:
-                    if media.codec.startswith(codec_candidate):
+                    if media.codec.startswith('avc'):
                         codec = media.codec
-                        quality = media.quality
                         print(f'{file_basename}: "{codec}" "{media.quality}" ...')
                         break
-                if codec is not None:
-                    break
-            assert codec is not None and quality is not None, f'{file_basename}: 没有 dvh、avc 或 hevc 编码的视频'
+            assert codec is not None, f'{file_basename}: 没有 avc 或 hevc 编码的视频'
         elif video_info.other:
-            print(f'{file_basename}: 未解析到 dash 资源，交给 bilix 处理 ...')
+            print(f'{file_basename}: 未解析到dash资源，交给 bilix 处理 ...')
             codec = ''
-            quality = 0
         else:
             raise APIError(f'{file_basename}: 未解析到视频资源', page.p_url)
 
         assert codec is not None
-        assert isinstance(quality, (int, str))
 
         cor1 = d.get_video(page.p_url ,video_info=video_info, path=video_basepath,
-                    quality=quality, # 选择最高画质
+                    quality=0, # 选择最高画质
                     codec=codec, # 编码
                     # 下载 ass 弹幕(bilix 会自动调用 danmukuC 将 pb 弹幕转为 ass)、封面、字幕
                     # 弹幕、封面、字幕都会被放进 extra 子目录里，所以需要 d.hierarchy is True
                     dm=True, image=True, subtitle=True
                     )
         # 下载原始的 pb 弹幕
         cor2 = d.get_dm(page.p_url, video_info=video_info, path=video_extrapath)
         # 下载视频超详细信息（BV 级别，不是分 P 级别）
         cor3 = download_bilibili_video_detail(d.client, bvid, f'{video_extrapath}/{file_basename}.info.json')
         await asyncio.gather(cor1, cor2, cor3)
 
-        if codec.startswith('hev') and not os.path.exists(video_basepath / f'{file_basename}.mp4'):
-
-            # 如果有下载缓存文件（以 file_basename 开头的文件），说明这个 hevc 的 dash 资源存在，只是可能因为网络之类的原因下载中途失败了
-            delete_cache('下载出错')
-
-            # 下载缓存文件都不存在，应该是对应的 dash 资源根本就没有，一些老视频会出现这种情况。
-            # 换 avc 编码
-            print(f'{file_basename}: 视频文件没有被下载？也许是 hevc 对应的 dash 资源不存在，尝试 avc ……')
-            assert video_info.dash is not None
-            for media in video_info.dash.videos:
-                if media.codec.startswith('avc'):
-                    codec = media.codec
-                    print(f'{file_basename}: "{codec}" "{media.quality}" ...')
-                    break
-            cor4 = d.get_video(page.p_url ,video_info=video_info, path=video_basepath,
-                    quality=0, # 选择最高画质
-                    codec=codec, # 编码
-                    # 下载 ass 弹幕(bilix 会自动调用 danmukuC 将 pb 弹幕转为 ass)、封面、字幕
-                    # 弹幕、封面、字幕都会被放进 extra 子目录里，所以需要 d.hierarchy is True
-                    dm=True, image=True, subtitle=True
-                    )
-            await asyncio.gather(cor4)
-
-
-        assert os.path.exists(video_basepath / f'{file_basename}.mp4')
-
         # 还原为了自定义文件名而做的覆盖
         video_info.pages[video_info.p].p_name = old_p_name
         video_info.h1_title = old_h1_title
 
         # 单 p 下好了
         async with aiofiles.open(f'{video_basepath}/_downloaded.mark', 'w', encoding='utf-8') as f:
             await f.write('')
```

### Comparing `biliarchiver-0.0.26/biliarchiver/config.py` & `biliarchiver-0.0.9/biliarchiver/config.py`

 * *Files 6% similar despite different names*

```diff
@@ -12,49 +12,45 @@
     def __call__(cls, *args, **kwargs):
         if cls not in cls._instances:
             cls._instances[cls] = super(singleton, cls).__call__(*args, **kwargs)
         return cls._instances[cls]
 
 
 @dataclass
-class _Config(metaclass=singleton):
+class Config(metaclass=singleton):
     video_concurrency: int = 3 
     part_concurrency: int = 10
     stream_retry: int = 20
     storage_home_dir: Path = Path('bilibili_archive_dir/').expanduser()
     ia_key_file: Path = Path('~/.bili_ia_keys.txt').expanduser()
-    cookies_file: Path = Path('~/.cookies.txt').expanduser()
 
     def __init__(self):
         self.is_right_pwd()
         if not os.path.exists(CONFIG_FILE):
             print(f'{CONFIG_FILE} 不存在，创建中...')
             self.save()
         with open(CONFIG_FILE, 'r', encoding='utf-8') as f:
-            print(f'Loading {CONFIG_FILE} ...')
+            print(f'读取 {CONFIG_FILE}...')
             config_file = json.load(f)
 
         self.video_concurrency: int = config_file['video_concurrency']
         self.part_concurrency: int = config_file['part_concurrency']
         self.stream_retry: int = config_file['stream_retry']
 
         self.storage_home_dir: Path = Path(config_file['storage_home_dir']).expanduser()
         self.ia_key_file: Path = Path(config_file['ia_key_file']).expanduser()
-        self.cookies_file: Path = Path(config_file['cookies_file']).expanduser()
-
 
     def save(self):
         with open(CONFIG_FILE, 'w', encoding='utf-8') as f:
             json.dump({
                 'video_concurrency': self.video_concurrency,
                 'part_concurrency': self.part_concurrency,
                 'stream_retry': self.stream_retry,
                 'storage_home_dir': str(self.storage_home_dir),
                 'ia_key_file': str(self.ia_key_file),
-                'cookies_file': str(self.cookies_file),
             }, f, ensure_ascii=False, indent=4)
 
     def is_right_pwd(self):
         if not os.path.exists('biliarchiver.home'):
             raise Exception('先在当前工作目录创建 biliarchiver.home 文件')
 
-config = _Config()
+config = Config()
```

### Comparing `biliarchiver-0.0.26/biliarchiver/utils/dirLock.py` & `biliarchiver-0.0.9/biliarchiver/utils/dirLock.py`

 * *Files identical despite different names*

### Comparing `biliarchiver-0.0.26/biliarchiver/utils/identifier.py` & `biliarchiver-0.0.9/biliarchiver/utils/string.py`

 * *Files identical despite different names*

### Comparing `biliarchiver-0.0.26/PKG-INFO` & `biliarchiver-0.0.9/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,31 +1,26 @@
 Metadata-Version: 2.1
 Name: biliarchiver
-Version: 0.0.26
+Version: 0.0.9
 Summary: 
 Author: yzqzss
 Author-email: yzqzss@yandex.com
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: bilix (==0.18.4)
-Requires-Dist: browser-cookie3 (>=0.19.1,<0.20.0)
-Requires-Dist: danmakuc (>=0.3.6,<0.4.0)
+Requires-Dist: bilix (==0.18.3)
 Requires-Dist: internetarchive (>=3.5.0,<4.0.0)
 Description-Content-Type: text/markdown
 
 # biliarchiver
 
-> 基于 bilix 的 BiliBili 存档工具
+## 基于 bilix 的 BiliBili 存档工具
 
-## Install
+~~ IA iteam identifier 格式兼容 tubeup ~~。  
+现在不兼容了，Tubeup 不适合存 B 站视频，它的 identifier 设计不科学，大规模存档必定会撞车。
 
-```bash
-pip install biliarchiver
-```
+目前，我可能随时 commit 乱飞且动不动就 git push -f 这个仓库。（为了在我的 vps 和本地之间同步代码）
 
-## Usage
-
-待补充。
+userscript.js 还没适配新换的 identifier 格式。
```

