# Comparing `tmp/pybaiduphoto-2022.8.4.1750.tar.gz` & `tmp/pybaiduphoto-2023.7.23.843.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pybaiduphoto-2022.8.4.1750.tar", last modified: Thu Aug  4 09:50:50 2022, max compression
+gzip compressed data, was "pybaiduphoto-2023.7.23.843.tar", last modified: Sun Jul 23 00:43:52 2023, max compression
```

## Comparing `pybaiduphoto-2022.8.4.1750.tar` & `pybaiduphoto-2023.7.23.843.tar`

### file list

```diff
@@ -1,26 +1,29 @@
-drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2022-08-04 09:50:50.004917 pybaiduphoto-2022.8.4.1750/
--rw-r--r--   0 hengyue    (501) staff       (20)     1062 2022-03-12 06:03:58.000000 pybaiduphoto-2022.8.4.1750/LICENSE
--rw-r--r--   0 hengyue    (501) staff       (20)     5807 2022-08-04 09:50:49.974886 pybaiduphoto-2022.8.4.1750/PKG-INFO
--rw-r--r--   0 hengyue    (501) staff       (20)     5465 2022-08-04 06:20:09.000000 pybaiduphoto-2022.8.4.1750/README.md
-drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2022-08-04 09:50:49.880549 pybaiduphoto-2022.8.4.1750/pybaiduphoto/
--rw-r--r--   0 hengyue    (501) staff       (20)     7294 2022-08-04 03:13:47.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/API.py
--rw-r--r--   0 hengyue    (501) staff       (20)     5364 2022-08-04 02:41:43.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/Album.py
--rw-r--r--   0 hengyue    (501) staff       (20)     8417 2022-08-01 14:17:42.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/General.py
--rw-r--r--   0 hengyue    (501) staff       (20)     1230 2022-08-04 05:58:16.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/Location.py
--rw-r--r--   0 hengyue    (501) staff       (20)     2955 2022-08-04 02:42:02.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/OnlineItem.py
--rw-r--r--   0 hengyue    (501) staff       (20)     2655 2022-08-04 02:42:17.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/Person.py
--rw-r--r--   0 hengyue    (501) staff       (20)     3529 2022-05-13 23:14:24.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/Requests.py
--rw-r--r--   0 hengyue    (501) staff       (20)     1245 2022-08-03 09:18:52.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/Thing.py
--rw-r--r--   0 hengyue    (501) staff       (20)       19 2022-03-12 12:27:01.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/__init__.py
--rw-r--r--   0 hengyue    (501) staff       (20)     1019 2022-08-04 03:13:47.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/apiObject.py
--rw-r--r--   0 hengyue    (501) staff       (20)      547 2022-05-13 23:18:38.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/contribution.py
-drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2022-08-04 09:50:49.972047 pybaiduphoto-2022.8.4.1750/pybaiduphoto/test/
--rw-r--r--   0 hengyue    (501) staff       (20)        0 2019-02-16 07:45:38.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto/test/__init__.py
-drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2022-08-04 09:50:49.969817 pybaiduphoto-2022.8.4.1750/pybaiduphoto.egg-info/
--rw-r--r--   0 hengyue    (501) staff       (20)     5807 2022-08-04 09:50:33.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto.egg-info/PKG-INFO
--rw-r--r--   0 hengyue    (501) staff       (20)      503 2022-08-04 09:50:44.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto.egg-info/SOURCES.txt
--rw-r--r--   0 hengyue    (501) staff       (20)        1 2022-08-04 09:50:35.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto.egg-info/dependency_links.txt
--rw-r--r--   0 hengyue    (501) staff       (20)       31 2022-08-04 09:50:39.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto.egg-info/requires.txt
--rw-r--r--   0 hengyue    (501) staff       (20)       13 2022-08-04 09:50:41.000000 pybaiduphoto-2022.8.4.1750/pybaiduphoto.egg-info/top_level.txt
--rw-r--r--   0 hengyue    (501) staff       (20)       38 2022-08-04 09:50:50.012133 pybaiduphoto-2022.8.4.1750/setup.cfg
--rw-r--r--   0 hengyue    (501) staff       (20)      589 2022-08-04 09:50:26.000000 pybaiduphoto-2022.8.4.1750/setup.py
+drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2023-07-23 00:43:52.265599 pybaiduphoto-2023.7.23.843/
+-rw-r--r--   0 hengyue    (501) staff       (20)     1062 2022-01-13 12:08:41.000000 pybaiduphoto-2023.7.23.843/LICENSE
+-rw-r--r--   0 hengyue    (501) staff       (20)     6473 2023-07-23 00:43:52.264528 pybaiduphoto-2023.7.23.843/PKG-INFO
+-rw-r--r--   0 hengyue    (501) staff       (20)     6151 2023-07-23 00:39:29.000000 pybaiduphoto-2023.7.23.843/README.md
+drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2023-07-23 00:43:52.251127 pybaiduphoto-2023.7.23.843/pybaiduphoto/
+-rw-r--r--   0 hengyue    (501) staff       (20)     6368 2023-06-26 01:53:50.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/API.py
+-rw-r--r--   0 hengyue    (501) staff       (20)     5702 2023-07-23 00:33:53.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/Album.py
+-rw-r--r--   0 hengyue    (501) staff       (20)     8841 2023-06-26 01:53:50.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/General.py
+-rw-r--r--   0 hengyue    (501) staff       (20)     1230 2022-08-04 05:58:16.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/Location.py
+-rw-r--r--   0 hengyue    (501) staff       (20)     2955 2023-05-30 04:11:40.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/OnlineItem.py
+-rw-r--r--   0 hengyue    (501) staff       (20)     2655 2022-08-04 02:42:17.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/Person.py
+-rw-r--r--   0 hengyue    (501) staff       (20)     3529 2022-05-13 23:14:24.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/Requests.py
+-rw-r--r--   0 hengyue    (501) staff       (20)     1245 2022-08-03 09:18:52.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/Thing.py
+-rw-r--r--   0 hengyue    (501) staff       (20)       19 2022-03-12 12:27:01.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/__init__.py
+-rw-r--r--   0 hengyue    (501) staff       (20)     1019 2022-08-04 03:13:47.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/apiObject.py
+-rw-r--r--   0 hengyue    (501) staff       (20)      547 2022-05-13 23:18:38.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/contribution.py
+drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2023-07-23 00:43:52.260388 pybaiduphoto-2023.7.23.843/pybaiduphoto/cooperation/
+-rw-r--r--   0 hengyue    (501) staff       (20)        0 2022-11-04 23:38:57.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/cooperation/__init__.py
+-rw-r--r--   0 hengyue    (501) staff       (20)    11714 2023-06-26 01:53:50.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/cooperation/muyangren907_shoot_time.py
+drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2023-07-23 00:43:52.262642 pybaiduphoto-2023.7.23.843/pybaiduphoto/test/
+-rw-r--r--   0 hengyue    (501) staff       (20)        0 2019-02-16 07:45:38.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto/test/__init__.py
+drwxr-xr-x   0 hengyue    (501) staff       (20)        0 2023-07-23 00:43:52.258158 pybaiduphoto-2023.7.23.843/pybaiduphoto.egg-info/
+-rw-r--r--   0 hengyue    (501) staff       (20)     6473 2023-07-23 00:43:51.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto.egg-info/PKG-INFO
+-rw-r--r--   0 hengyue    (501) staff       (20)      592 2023-07-23 00:43:52.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto.egg-info/SOURCES.txt
+-rw-r--r--   0 hengyue    (501) staff       (20)        1 2023-07-23 00:43:51.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto.egg-info/dependency_links.txt
+-rw-r--r--   0 hengyue    (501) staff       (20)       31 2023-07-23 00:43:51.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto.egg-info/requires.txt
+-rw-r--r--   0 hengyue    (501) staff       (20)       13 2023-07-23 00:43:51.000000 pybaiduphoto-2023.7.23.843/pybaiduphoto.egg-info/top_level.txt
+-rw-r--r--   0 hengyue    (501) staff       (20)       38 2023-07-23 00:43:52.268165 pybaiduphoto-2023.7.23.843/setup.cfg
+-rw-r--r--   0 hengyue    (501) staff       (20)      589 2023-07-23 00:43:51.000000 pybaiduphoto-2023.7.23.843/setup.py
```

### Comparing `pybaiduphoto-2022.8.4.1750/LICENSE` & `pybaiduphoto-2023.7.23.843/LICENSE`

 * *Files identical despite different names*

### Comparing `pybaiduphoto-2022.8.4.1750/PKG-INFO` & `pybaiduphoto-2023.7.23.843/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 Metadata-Version: 2.1
 Name: pybaiduphoto
-Version: 2022.8.4.1750
+Version: 2023.7.23.843
 Summary: A simple API to interact with baidu-photo
 Home-page: https://github.com/HengyueLi/baiduphoto
 Author: Hengyue Li
 Author-email: 305069590@qq.com
 License: LICENSE.md
-Platform: UNKNOWN
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # pybaiduphoto
 一刻相册 API
 
@@ -85,33 +84,33 @@
     list2 = api.get_self_1page(typeName='Item',cursor=cursor_nextpage)
 ```
 可以删除:
 ```
 L[0].delete()
 ```
 
-high level函数`get_self_All(typeName='Item',typemax=-1)`是对`get_self_1page`的一个包装，用于获取所有对象。`max`设定最大获取数量，`max<=0`对应获取全部。注意这可能是比较慢的。例如(注意，内容多的话可能有点慢):
+high level函数`get_self_All(typeName='Item',max=-1)`是对`get_self_1page`的一个包装，用于获取所有对象。`max`设定最大获取数量，`max<=0`对应获取全部。例如(注意，内容多的话可能有点慢):
 ```
 L = api.get_self_All(typeName='Item')
 ```
 则`L[0]`直接就是一个数据对象。
 
 
 
 ## 相册对象
 ```
 list1 = api.get_self_1page(typeName='Album')
 list1.keys()
 >>
 dict_keys(['items', 'has_more', 'cursor'])
 ```
-其中`has_more`, `cursor`意义上同。items中的对象是`相册对象`。可以用过`append`将图片添加到相册。例子: 将最后一张照片添加到第一个相册:
+其中`has_more`, `cursor`意义同上。items中的对象是`相册对象`。可以用过`append`将图片添加到相册。例如: 将最后一张照片添加到第一个相册:
 ```
 ilist = api.get_self_1page(typeName='Item')
-alist = api.get_self_1page(typeName='Album')
+alist = api.get_self_1page(typeName='Album')  
 a = alist['items'][0]
 a.append( ilist['items'][0]  )
 ```
 也可以添加多个对象，`a.append( ilist['items'][0:3]  )`
 
 可以删除该相册:`a.delete()`,默认会删除相册中的子内容。如果只删除相册但是保留子内容，可使用: `a.delete(isWithItems=False)`
 
@@ -128,57 +127,76 @@
 ```
 
 重命名:
 ```
 a.rename(newName)
 ```
 
+设置公告:  
+```
+a.setNotice("balabala...")
+```
+
 ## 人物相册
 用法参考上面的相册对象，只是把`typeName`设置成`Person`。例如获得所有的人物相册的方式：
 ```
 pList = api.get_self_All(typeName='Person')
 ```
 该对象类似与相册对象，不过是百度自动按照人脸分类了。函数类似的还有`get_sub_1page`和`get_sub_All`，用法同上。
 
 ## 地点相册
 用法同上，设置`typeName='Location'`
 
 ## 事物相册
 用法同上，设置`typeName='Thing'`
 
 
+# API 操作
 
-# 上传文件
+## 上传文件
 
 ```
 api.upload_1file(filePath='/Users/XXXX/Desktop/test.png')
 ```
 
-# 创建相册
+若要上传到指定相册
+
+```
+api.upload_1file(filePath='/Users/XXXX/Desktop/test.png', album=a)
+```
+其中`a`是获取相册列表得到的相册，例如`a=api.get_self_1page(typeName='Album')['items'][0]`。
+
+## 创建相册
 创建一个名字为`test`的相册：
 ```
 a = api.createNewAlbum(Name='test')
 ```
 返回的是相册对象（见上面解释）。!!!注意，可以创建名字相同的相册。另外，此处后台来看会用到一个`tid`的信息，来唯一标识一个相册。我不知道这个是怎么生成的，目前用一个18位的随机数来代替测试可行。但这带来一个未来失效的风险。有聪明的同学可以帮我研究研究这个`tid`从哪里来的。
 
+## 搜索相册
+根据关键词搜索满足条件的相册。
+```
+aList = api.albumSearch(keyword="xxxx"，limit=30,start=0)
+```
+返回值包含`aList.keys()`->`dict_keys(['items', 'has_more'])`. 所有满足条件的相册对象包含在`aList['items']`中。因为这是一个新增加的功能，所以官方应该是内部做了什么标记。很早之前创建的相册搜不到，网页版的也搜索不到，没办法解决。
+
 
-# 网络代理
+
+## 网络代理
 在初始化对象的时候加入`proxies`字段,例如
 `api = API(cookies = browser_cookie3.chrome() , proxies = {"https":"socks5://127.0.0.1:1080"} )`。`proxies`的格式同`requests`库需求一致。
 
-# 批量下载
+## 批量下载
 通过`url = api.get_batchDownloadLink(items,zipname=None)`可以获得一个下载地址，复制到浏览器回车可以下载一个zip包。这其中`items`是一个标准的Python list,内容是`数据对象`。注意如果要用参数`zipname`的话，后缀名要加上`.zip`，不然报错。
 
 
 
 # Contribution requests
 - ~~批量下载，遇到一些困难，有js比较好的同学可以去[issue](https://github.com/HengyueLi/baiduphoto/issues/4)帮着看看。~~(感谢@foxxorcat)
 
 
 
 # 总结
 虽然只在mac上测试了一下，但是应该其他系统也能用。大致看起来能跑通，基本功能可以实现。有各种问题的话再慢慢研究修复。
 
 # 免责申明
 此脚本（API）仅供学习交流，禁止商业使用。使用软件过程中，发生意外造成的损失由使用者承担。您必须在下载后的24小时内从计算机或其他各种设备中完全删除本项目所有内容。您使用或者复制了以上的任何内容，则视为已接受此声明，请仔细阅读。
-
-
```

### Comparing `pybaiduphoto-2022.8.4.1750/README.md` & `pybaiduphoto-2023.7.23.843/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -72,33 +72,33 @@
     list2 = api.get_self_1page(typeName='Item',cursor=cursor_nextpage)
 ```
 可以删除:
 ```
 L[0].delete()
 ```
 
-high level函数`get_self_All(typeName='Item',typemax=-1)`是对`get_self_1page`的一个包装，用于获取所有对象。`max`设定最大获取数量，`max<=0`对应获取全部。注意这可能是比较慢的。例如(注意，内容多的话可能有点慢):
+high level函数`get_self_All(typeName='Item',max=-1)`是对`get_self_1page`的一个包装，用于获取所有对象。`max`设定最大获取数量，`max<=0`对应获取全部。例如(注意，内容多的话可能有点慢):
 ```
 L = api.get_self_All(typeName='Item')
 ```
 则`L[0]`直接就是一个数据对象。
 
 
 
 ## 相册对象
 ```
 list1 = api.get_self_1page(typeName='Album')
 list1.keys()
 >>
 dict_keys(['items', 'has_more', 'cursor'])
 ```
-其中`has_more`, `cursor`意义上同。items中的对象是`相册对象`。可以用过`append`将图片添加到相册。例子: 将最后一张照片添加到第一个相册:
+其中`has_more`, `cursor`意义同上。items中的对象是`相册对象`。可以用过`append`将图片添加到相册。例如: 将最后一张照片添加到第一个相册:
 ```
 ilist = api.get_self_1page(typeName='Item')
-alist = api.get_self_1page(typeName='Album')
+alist = api.get_self_1page(typeName='Album')  
 a = alist['items'][0]
 a.append( ilist['items'][0]  )
 ```
 也可以添加多个对象，`a.append( ilist['items'][0:3]  )`
 
 可以删除该相册:`a.delete()`,默认会删除相册中的子内容。如果只删除相册但是保留子内容，可使用: `a.delete(isWithItems=False)`
 
@@ -115,48 +115,69 @@
 ```
 
 重命名:
 ```
 a.rename(newName)
 ```
 
+设置公告:  
+```
+a.setNotice("balabala...")
+```
+
 ## 人物相册
 用法参考上面的相册对象，只是把`typeName`设置成`Person`。例如获得所有的人物相册的方式：
 ```
 pList = api.get_self_All(typeName='Person')
 ```
 该对象类似与相册对象，不过是百度自动按照人脸分类了。函数类似的还有`get_sub_1page`和`get_sub_All`，用法同上。
 
 ## 地点相册
 用法同上，设置`typeName='Location'`
 
 ## 事物相册
 用法同上，设置`typeName='Thing'`
 
 
+# API 操作
 
-# 上传文件
+## 上传文件
 
 ```
 api.upload_1file(filePath='/Users/XXXX/Desktop/test.png')
 ```
 
-# 创建相册
+若要上传到指定相册
+
+```
+api.upload_1file(filePath='/Users/XXXX/Desktop/test.png', album=a)
+```
+其中`a`是获取相册列表得到的相册，例如`a=api.get_self_1page(typeName='Album')['items'][0]`。
+
+## 创建相册
 创建一个名字为`test`的相册：
 ```
 a = api.createNewAlbum(Name='test')
 ```
 返回的是相册对象（见上面解释）。!!!注意，可以创建名字相同的相册。另外，此处后台来看会用到一个`tid`的信息，来唯一标识一个相册。我不知道这个是怎么生成的，目前用一个18位的随机数来代替测试可行。但这带来一个未来失效的风险。有聪明的同学可以帮我研究研究这个`tid`从哪里来的。
 
+## 搜索相册
+根据关键词搜索满足条件的相册。
+```
+aList = api.albumSearch(keyword="xxxx"，limit=30,start=0)
+```
+返回值包含`aList.keys()`->`dict_keys(['items', 'has_more'])`. 所有满足条件的相册对象包含在`aList['items']`中。因为这是一个新增加的功能，所以官方应该是内部做了什么标记。很早之前创建的相册搜不到，网页版的也搜索不到，没办法解决。
+
+
 
-# 网络代理
+## 网络代理
 在初始化对象的时候加入`proxies`字段,例如
 `api = API(cookies = browser_cookie3.chrome() , proxies = {"https":"socks5://127.0.0.1:1080"} )`。`proxies`的格式同`requests`库需求一致。
 
-# 批量下载
+## 批量下载
 通过`url = api.get_batchDownloadLink(items,zipname=None)`可以获得一个下载地址，复制到浏览器回车可以下载一个zip包。这其中`items`是一个标准的Python list,内容是`数据对象`。注意如果要用参数`zipname`的话，后缀名要加上`.zip`，不然报错。
 
 
 
 # Contribution requests
 - ~~批量下载，遇到一些困难，有js比较好的同学可以去[issue](https://github.com/HengyueLi/baiduphoto/issues/4)帮着看看。~~(感谢@foxxorcat)
```

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/API.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/API.py`

 * *Files 18% similar despite different names*

```diff
@@ -2,38 +2,21 @@
 import logging
 
 
 from .Requests import Requests
 from .OnlineItem import OnlineItem
 from .Album import Album
 from .General import General
-from .General import getAllItemsBySinglePageFunction
+
+# from .General import getAllItemsBySinglePageFunction
 from .Person import PersonAlbum
 from .Location import Location
 from .Thing import Thing
 
 
-# def get_md5_by_binString(binString):
-#     return hashlib.md5(binString).hexdigest()
-#
-# def get_md5_by_LocalFile(filePath):
-#     with open(filePath,'rb') as f:
-#         return hashlib.md5(f.read()).hexdigest()
-#
-# def get_metadata_localFile(filePath):
-#     return {
-#         'fileName' : os.path.basename(filePath),
-#         'localFilePath' : filePath,
-#         'size' : os.path.getsize(filePath),
-#         'ctime': int(os.path.getctime(filePath)),
-#         'mtime': int(os.path.getmtime(filePath)),
-#         'md5':get_md5_by_LocalFile(filePath),
-#     }
-
-
 class API:
     def __init__(self, cookies, proxies={}):
         self.req = Requests(cookies=cookies, proxies=proxies)
         self.g = General(self.req)
 
     @staticmethod
     def getObjectClass(name):
@@ -45,73 +28,32 @@
             "Thing": Thing,
         }
         if name not in table:
             logging.error("not registrat class by name = [{}]".format(name))
         else:
             return table[name]
 
-    #     def get(self,method,params):
-    #         urlPrefix = 'https://photo.baidu.com/youai/file/v1/'
-    #         data = self.req.getReqJson(url = urlPrefix+method.strip(), params=params)
-    #         return data
-
-    # def get_SinglePage(self, cursor=None) -> dict:
-    #     # info of one page.   contains a list of photon info
-    #     params = {
-    #         "clienttype": 70,
-    #         #     'need_thumbnail':1,
-    #         "need_filter_hidden": 0,
-    #     }
-    #     if cursor is not None:
-    #         params["cursor"] = cursor
-    #     pageInfo = self.req.getReqJson(
-    #         url="https://photo.baidu.com/youai/file/v1/list", params=params
-    #     )
-    #     return {
-    #         "items": [OnlineItem(i, self.req) for i in pageInfo["list"]],
-    #         "has_more": pageInfo["has_more"] == 1,
-    #         "cursor": pageInfo["cursor"],
-    #     }
     def get_self_1page(self, typeName, cursor=None) -> dict:
         cls = self.getObjectClass(typeName)
         return cls.get_self_1page(req=self.req, cursor=cursor)
 
     def get_SinglePage(self, cursor=None) -> dict:
         logging.warning("Deprecated method!!! use get_self_1page instead!")
         return self.get_self_1page(typeName="Item", cursor=cursor)
-        # return OnlineItem.get_self_1page(req=self.req,cursor=cursor)
 
     def get_self_All(self, typeName, max=-1) -> list:
         cls = self.getObjectClass(typeName)
         if cls is None:
             return None
         else:
             return cls.get_self_All(req=self.req, max=max)
 
-    # def getAllItems(self,max=-1) -> list:
-    #     # !!! slow !!!
-    #     r = []
-    #     c = 0
-    #     cursor = None
-    #     while True:
-    #         page = self.get_SinglePage(cursor=cursor)
-    #         # N = len(page['items'])
-    #         if max <= 0:
-    #         r += page['items']
-    #         if page['has_more']:
-    #             cursor = page['cursor']
-    #         else:
-    #             return r
-    # def getAllItems(self, max=-1) -> list:
-    #     fun = self.get_SinglePage
-    #     return getAllItemsBySinglePageFunction(SinglePageFunc=fun, max=max)
     def getAllItems(self, max=-1) -> list:
         logging.warning("Deprecated method!!! use getAllTargetList instead!")
         return self.getAllTargetList(typeName="Item", max=max)
-        # return OnlineItem.get_self_All(req=self.req,max=max)
 
     def getAlbumList(self, limit=30, cursor=None):
         url = "https://photo.baidu.com/youai/album/v1/list"
         params = dict(
             (
                 ("clienttype", "70"),
                 # ('bdstoken', '263...'),
@@ -140,15 +82,15 @@
             albs = self.getAlbumList(cursor=cursor)
             r += albs["items"]
             if albs["has_more"]:
                 cursor = albs["cursor"]
             else:
                 return r
 
-    def upload_1file(self, filePath):
+    def upload_1file_directly(self, filePath):
         preC, reqJson1, reqJson2 = self.g.upload_1file(filePath)
         logging.debug(
             "upload file: preC=\n{}\n,reqJson1=\n{}\n, reqJson2=\n{}\n ".format(
                 preC, reqJson1, reqJson2
             )
         )
         if preC["return_type"] == 1:  # new upload
@@ -157,16 +99,34 @@
             if "fsid" not in info:
                 info["fsid"] = info["fs_id"]
             return OnlineItem(info, self.req)
         elif preC["return_type"] == 3:  # already exist
             logging.warning("upload item already exist on remote")
             return self.getOnlineItem_ByInfo(info=preC["data"])
         else:
+            logging.error(
+                "unknow return_type ={} @upload_1file_directly".format(
+                    preC["return_type"]
+                )
+            )
+            logging.error("full response = [{}]".format(str(preC)))
             return
 
+    def upload_1file(self, filePath, album=None):
+        # consider upload into alumb
+        item = self.upload_1file_directly(filePath=filePath)
+        if album is not None and item is not None:
+            logging.debug(
+                "append item into album. item=[{}],album=[{}]".format(
+                    item.info, album.info
+                )
+            )
+            album.append(item)
+        return item
+
     def createNewAlbum(self, Name, tid=None):
         res = self.g.createNewAlbum(Name, tid)
         return Album(res["info"], req=self.req)
 
     def get_batchDownloadLink(self, items, zipname=None):
         return self.g.getdlLink_batchDonwload(items=items, zipname=zipname)
 
@@ -205,7 +165,27 @@
 
     def getAllPersonList(self, max=-1):
         return self.getPersonList_Onepage()
 
     def loadSelfByInfo(self, typeName, info):
         cls = self.getObjectClass(typeName)
         return cls.loadSelfByInfo(info=info, req=self.req)
+
+    def albumSearch(self, keyword, limit=30, start=0):
+        R = {}
+        params = {
+            "clienttype": "70",
+            "keyword": keyword,
+            "limit": limit,
+            "start": start,
+        }
+        req = self.g.req
+        res = req.getReqJson(
+            url="https://photo.baidu.com/youai/album/v1/search",
+            params=params,
+        )
+        abList = []
+        for info in res["list"]:
+            abList.append(self.getAlbum_ByInfo(info=info))
+        R["items"] = abList
+        R["has_more"] = res["has_more"] == 1
+        return R
```

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/Album.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/Album.py`

 * *Files 4% similar despite different names*

```diff
@@ -161,7 +161,18 @@
             "album_id": self.getID(),
             "tid": self._getTID(),
             "title": newName,
         }
         r = self.req.postReqJson(url, data=data)
         if r["errno"] == 0:
             self.info["title"] = newName
+
+    def setNotice(self,notice):
+        url = "https://photo.baidu.com/youai/album/v1/setnotice"
+        params = {
+            'clienttype': '70',
+            'album_id': self.getID(),
+            'tid': self._getTID(),
+            'notice': notice,
+        }
+        r = self.req.getReqJson(url=url,params=params)
+        return self
```

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/General.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/General.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,14 +2,17 @@
 import io
 import random
 import logging
 import hashlib
 import datetime
 import base64
 
+from .cooperation import muyangren907_shoot_time
+
+
 # import js2py
 from .Requests import Requests
 
 
 def getAllItemsBySinglePageFunction(SinglePageFunc, max=-1):
     # ----------------------------------------------------------------
     # def SinglePageFunc(cursor=None) -> dict:
@@ -38,49 +41,55 @@
         self.req = req
 
     @staticmethod
     def get_file_fullContent(filePath):
         with open(filePath, "rb") as f:
             binString = f.read()
             md5 = hashlib.md5(binString).hexdigest()
+
         return {
             "fileName": os.path.basename(filePath),
             "localFilePath": filePath,
             "size": os.path.getsize(filePath),
             "ctime": int(os.path.getctime(filePath)),
             "mtime": int(os.path.getmtime(filePath)),
             "md5": md5,
             "bin": binString,
+            "media_info": muyangren907_shoot_time.getMediaInfo_interface(filePath),
         }
 
     def upload_step1_preCreate(self, fileFull):
         postdata = {
             "autoinit": "1",
             "block_list": '["{}"]'.format(fileFull["md5"]),
             "isdir": "0",
             "rtype": "1",
             "ctype": "11",  # required
             "path": "/" + fileFull["fileName"],  # required
             "size": fileFull["size"],  # required
             #   'slice-md5': '4fe8d73cf1ee838b...',
+            "slice-md5": fileFull["md5"],
             "content-md5": fileFull["md5"],  # required
             "local_ctime": fileFull["ctime"],
             "local_mtime": fileFull["mtime"],
-            #   'media_info': 'QD1xoOXfdIsFhss...'
+            # "shoot_time": fileFull["shoot_time"],
+            # 'media_info': 'QD1xoOXfdIsFhss...' # 包含shoot_time
+            "media_info": fileFull["media_info"],  # 包含shoot_time
         }
         params = {
             "clienttype": "70",
             #             'bdstoken': self.req.bdstoken, # requird
         }
         logging.debug("upload_step1,postData={}".format(postdata))
         data = self.req.postReqJson(
             url="https://photo.baidu.com/youai/file/v1/precreate",
             params=params,
             data=postdata,
         )
+        # print('upload_step1_preCreate {}'.format(data))
         return data
 
     #         exist: {'data': {'fs_id': 9630...305088, 'size': 14...74, 'md5': '0379955f9bd...002f773217b', 'server_filename': 'Screen.png', 'path': '/youa/web/Screen.png', 'ctime': 16470..., 'mtime': 16470..., 'isdir': 0, 'category': 3, 'server_md5': '9af01bd...7bebeded', 'shoot_time': 1647...309}, 'return_type': 3, 'errno': 0, 'request_id': 48666...003049}
     #         New: {'return_type': 1, 'path': '/youa/web/Screen.png', 'uploadid': 'N1-MTAuNj...DA2MzY3OTQx', 'block_list': [0], 'errno': 0, 'request_id': 48669...67941}
 
     def upload_step2_superfile2(self, preCreateInfo, fileFull):
         params = dict(
@@ -118,14 +127,15 @@
             "size": fileFull["size"],
             "uploadid": preCreateInfo["uploadid"],
             "block_list": '["{}"]'.format(fileFull["md5"]),
             "isdir": "0",
             "rtype": "1",
             "content-md5": fileFull["md5"],
             "ctype": "11",
+            "media_info": fileFull["media_info"]
             #           'media_info': 'QD1xoOX.....'
         }
         logging.debug("upload_step3,postData={}".format(data))
         return self.req.post(
             "https://photo.baidu.com/youai/file/v1/create", params=params, data=data
         ).json()
```

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/Location.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/Location.py`

 * *Files identical despite different names*

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/OnlineItem.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/OnlineItem.py`

 * *Files identical despite different names*

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/Person.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/Person.py`

 * *Files identical despite different names*

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/Requests.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/Requests.py`

 * *Files identical despite different names*

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/Thing.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/Thing.py`

 * *Files identical despite different names*

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/apiObject.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/apiObject.py`

 * *Files identical despite different names*

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto/contribution.py` & `pybaiduphoto-2023.7.23.843/pybaiduphoto/contribution.py`

 * *Files identical despite different names*

### Comparing `pybaiduphoto-2022.8.4.1750/pybaiduphoto.egg-info/PKG-INFO` & `pybaiduphoto-2023.7.23.843/pybaiduphoto.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 Metadata-Version: 2.1
 Name: pybaiduphoto
-Version: 2022.8.4.1750
+Version: 2023.7.23.843
 Summary: A simple API to interact with baidu-photo
 Home-page: https://github.com/HengyueLi/baiduphoto
 Author: Hengyue Li
 Author-email: 305069590@qq.com
 License: LICENSE.md
-Platform: UNKNOWN
 Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # pybaiduphoto
 一刻相册 API
 
@@ -85,33 +84,33 @@
     list2 = api.get_self_1page(typeName='Item',cursor=cursor_nextpage)
 ```
 可以删除:
 ```
 L[0].delete()
 ```
 
-high level函数`get_self_All(typeName='Item',typemax=-1)`是对`get_self_1page`的一个包装，用于获取所有对象。`max`设定最大获取数量，`max<=0`对应获取全部。注意这可能是比较慢的。例如(注意，内容多的话可能有点慢):
+high level函数`get_self_All(typeName='Item',max=-1)`是对`get_self_1page`的一个包装，用于获取所有对象。`max`设定最大获取数量，`max<=0`对应获取全部。例如(注意，内容多的话可能有点慢):
 ```
 L = api.get_self_All(typeName='Item')
 ```
 则`L[0]`直接就是一个数据对象。
 
 
 
 ## 相册对象
 ```
 list1 = api.get_self_1page(typeName='Album')
 list1.keys()
 >>
 dict_keys(['items', 'has_more', 'cursor'])
 ```
-其中`has_more`, `cursor`意义上同。items中的对象是`相册对象`。可以用过`append`将图片添加到相册。例子: 将最后一张照片添加到第一个相册:
+其中`has_more`, `cursor`意义同上。items中的对象是`相册对象`。可以用过`append`将图片添加到相册。例如: 将最后一张照片添加到第一个相册:
 ```
 ilist = api.get_self_1page(typeName='Item')
-alist = api.get_self_1page(typeName='Album')
+alist = api.get_self_1page(typeName='Album')  
 a = alist['items'][0]
 a.append( ilist['items'][0]  )
 ```
 也可以添加多个对象，`a.append( ilist['items'][0:3]  )`
 
 可以删除该相册:`a.delete()`,默认会删除相册中的子内容。如果只删除相册但是保留子内容，可使用: `a.delete(isWithItems=False)`
 
@@ -128,57 +127,76 @@
 ```
 
 重命名:
 ```
 a.rename(newName)
 ```
 
+设置公告:  
+```
+a.setNotice("balabala...")
+```
+
 ## 人物相册
 用法参考上面的相册对象，只是把`typeName`设置成`Person`。例如获得所有的人物相册的方式：
 ```
 pList = api.get_self_All(typeName='Person')
 ```
 该对象类似与相册对象，不过是百度自动按照人脸分类了。函数类似的还有`get_sub_1page`和`get_sub_All`，用法同上。
 
 ## 地点相册
 用法同上，设置`typeName='Location'`
 
 ## 事物相册
 用法同上，设置`typeName='Thing'`
 
 
+# API 操作
 
-# 上传文件
+## 上传文件
 
 ```
 api.upload_1file(filePath='/Users/XXXX/Desktop/test.png')
 ```
 
-# 创建相册
+若要上传到指定相册
+
+```
+api.upload_1file(filePath='/Users/XXXX/Desktop/test.png', album=a)
+```
+其中`a`是获取相册列表得到的相册，例如`a=api.get_self_1page(typeName='Album')['items'][0]`。
+
+## 创建相册
 创建一个名字为`test`的相册：
 ```
 a = api.createNewAlbum(Name='test')
 ```
 返回的是相册对象（见上面解释）。!!!注意，可以创建名字相同的相册。另外，此处后台来看会用到一个`tid`的信息，来唯一标识一个相册。我不知道这个是怎么生成的，目前用一个18位的随机数来代替测试可行。但这带来一个未来失效的风险。有聪明的同学可以帮我研究研究这个`tid`从哪里来的。
 
+## 搜索相册
+根据关键词搜索满足条件的相册。
+```
+aList = api.albumSearch(keyword="xxxx"，limit=30,start=0)
+```
+返回值包含`aList.keys()`->`dict_keys(['items', 'has_more'])`. 所有满足条件的相册对象包含在`aList['items']`中。因为这是一个新增加的功能，所以官方应该是内部做了什么标记。很早之前创建的相册搜不到，网页版的也搜索不到，没办法解决。
+
 
-# 网络代理
+
+## 网络代理
 在初始化对象的时候加入`proxies`字段,例如
 `api = API(cookies = browser_cookie3.chrome() , proxies = {"https":"socks5://127.0.0.1:1080"} )`。`proxies`的格式同`requests`库需求一致。
 
-# 批量下载
+## 批量下载
 通过`url = api.get_batchDownloadLink(items,zipname=None)`可以获得一个下载地址，复制到浏览器回车可以下载一个zip包。这其中`items`是一个标准的Python list,内容是`数据对象`。注意如果要用参数`zipname`的话，后缀名要加上`.zip`，不然报错。
 
 
 
 # Contribution requests
 - ~~批量下载，遇到一些困难，有js比较好的同学可以去[issue](https://github.com/HengyueLi/baiduphoto/issues/4)帮着看看。~~(感谢@foxxorcat)
 
 
 
 # 总结
 虽然只在mac上测试了一下，但是应该其他系统也能用。大致看起来能跑通，基本功能可以实现。有各种问题的话再慢慢研究修复。
 
 # 免责申明
 此脚本（API）仅供学习交流，禁止商业使用。使用软件过程中，发生意外造成的损失由使用者承担。您必须在下载后的24小时内从计算机或其他各种设备中完全删除本项目所有内容。您使用或者复制了以上的任何内容，则视为已接受此声明，请仔细阅读。
-
-
```

### Comparing `pybaiduphoto-2022.8.4.1750/setup.py` & `pybaiduphoto-2023.7.23.843/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 
 import setuptools
 #from setuptools import setup
 
 setuptools.setup(
     name='pybaiduphoto',
     scripts=[] ,
-    version='2022.08.04.1750',
+    version='2023.07.23.0843',
     author='Hengyue Li',
     author_email='305069590@qq.com',
     packages=setuptools.find_packages(),
     license='LICENSE.md',
     description='A simple API to interact with baidu-photo',
     long_description=open('README.md',encoding="utf8").read(),
     long_description_content_type="text/markdown",
```

