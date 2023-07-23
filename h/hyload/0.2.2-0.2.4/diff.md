# Comparing `tmp/hyload-0.2.2-py3-none-any.whl.zip` & `tmp/hyload-0.2.4-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,19 +1,19 @@
-Zip file size: 26034 bytes, number of entries: 17
+Zip file size: 27368 bytes, number of entries: 17
 -rw-rw-rw-  2.0 fat      171 b- defN 23-Jul-19 05:41 hyload/__init__.py
--rw-rw-rw-  2.0 fat       17 b- defN 23-Jul-20 14:20 hyload/cfg.py
--rw-rw-rw-  2.0 fat    15612 b- defN 23-Jul-20 02:58 hyload/httpclient.py
--rw-rw-rw-  2.0 fat     2439 b- defN 23-Jul-08 14:54 hyload/logger.py
--rw-rw-rw-  2.0 fat    10760 b- defN 23-Jul-20 12:34 hyload/stats.py
+-rw-rw-rw-  2.0 fat       17 b- defN 23-Jul-22 23:53 hyload/cfg.py
+-rw-rw-rw-  2.0 fat    19401 b- defN 23-Jul-23 00:11 hyload/httpclient.py
+-rw-rw-rw-  2.0 fat     2627 b- defN 23-Jul-23 00:12 hyload/logger.py
+-rw-rw-rw-  2.0 fat    11344 b- defN 23-Jul-23 00:16 hyload/stats.py
 -rw-rw-rw-  2.0 fat      979 b- defN 23-Jul-08 14:54 hyload/util.py
 -rw-rw-rw-  2.0 fat        0 b- defN 23-Jul-08 14:54 hyload/tools/__init__.py
 -rw-rw-rw-  2.0 fat     3667 b- defN 23-Jul-08 14:54 hyload/tools/plotperf.py
 -rw-rw-rw-  2.0 fat     2802 b- defN 23-Jul-08 14:54 hyload/tools/plotresource.py
 -rw-rw-rw-  2.0 fat    39521 b- defN 23-Jul-08 14:54 hyload/tools/puttyagents.py
--rw-rw-rw-  2.0 fat     3940 b- defN 23-Jul-20 08:38 hyload/tools/remoteop.py
+-rw-rw-rw-  2.0 fat     4007 b- defN 23-Jul-21 06:07 hyload/tools/remoteop.py
 -rw-rw-rw-  2.0 fat     7493 b- defN 23-Jul-14 12:12 hyload/tools/statshub.py
--rw-rw-rw-  2.0 fat     1100 b- defN 23-Jul-20 14:21 hyload-0.2.2.dist-info/LICENSE.txt
--rw-rw-rw-  2.0 fat     1482 b- defN 23-Jul-20 14:21 hyload-0.2.2.dist-info/METADATA
--rw-rw-rw-  2.0 fat       92 b- defN 23-Jul-20 14:21 hyload-0.2.2.dist-info/WHEEL
--rw-rw-rw-  2.0 fat        7 b- defN 23-Jul-20 14:21 hyload-0.2.2.dist-info/top_level.txt
--rw-rw-r--  2.0 fat     1311 b- defN 23-Jul-20 14:21 hyload-0.2.2.dist-info/RECORD
-17 files, 91393 bytes uncompressed, 23910 bytes compressed:  73.8%
+-rw-rw-rw-  2.0 fat     1100 b- defN 23-Jul-23 01:45 hyload-0.2.4.dist-info/LICENSE.txt
+-rw-rw-rw-  2.0 fat     1509 b- defN 23-Jul-23 01:45 hyload-0.2.4.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 23-Jul-23 01:45 hyload-0.2.4.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat        7 b- defN 23-Jul-23 01:45 hyload-0.2.4.dist-info/top_level.txt
+-rw-rw-r--  2.0 fat     1311 b- defN 23-Jul-23 01:45 hyload-0.2.4.dist-info/RECORD
+17 files, 96048 bytes uncompressed, 25244 bytes compressed:  73.7%
```

## zipnote {}

```diff
@@ -30,23 +30,23 @@
 
 Filename: hyload/tools/remoteop.py
 Comment: 
 
 Filename: hyload/tools/statshub.py
 Comment: 
 
-Filename: hyload-0.2.2.dist-info/LICENSE.txt
+Filename: hyload-0.2.4.dist-info/LICENSE.txt
 Comment: 
 
-Filename: hyload-0.2.2.dist-info/METADATA
+Filename: hyload-0.2.4.dist-info/METADATA
 Comment: 
 
-Filename: hyload-0.2.2.dist-info/WHEEL
+Filename: hyload-0.2.4.dist-info/WHEEL
 Comment: 
 
-Filename: hyload-0.2.2.dist-info/top_level.txt
+Filename: hyload-0.2.4.dist-info/top_level.txt
 Comment: 
 
-Filename: hyload-0.2.2.dist-info/RECORD
+Filename: hyload-0.2.4.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## hyload/cfg.py

```diff
@@ -1 +1 @@
-Version = '0.2.2'
+Version = '0.2.4'
```

## hyload/httpclient.py

```diff
@@ -1,114 +1,127 @@
 # byhy performance testing lib: ByClient
 # Author : byhy
 
-import time,http.client,traceback,socket
-from urllib.parse import urlparse,urlencode
+import time, http.client, socket, gzip
+from urllib.parse import urlencode
 from hyload.stats import Stats,bcolors
 from hyload.util import getCurTime
 from hyload.logger import TestLogger
 import json as jsonlib
 from http.cookies import SimpleCookie
+from typing import Union, Dict
 
-
-CommonHeaders = {
+_common_headers = {
     # 'User-Agent' : "hyload tester"
 }
 
-_sending_http_msg = ''
+
+
+# begin ** for patch http built-in funcs
+
+_http_req_msg_buf_cpy = b''
 
 _ori_http_send = http.client.HTTPConnection.send
-def _patch_httplib_funcs(encoding='utf8'):
+
+def _patch_httplib_funcs():
     def new_send(self, data):
-        global _sending_http_msg
+        global _http_req_msg_buf_cpy
         if hasattr(data, "read"):
             return
-        _sending_http_msg += data.decode(encoding)
-        # print(bcolors.OKGREEN + data.decode(encoding) + bcolors.ENDC, end='')
+        _http_req_msg_buf_cpy += data        
         return _ori_http_send(self, data)
     http.client.HTTPConnection.send = new_send
 
 
 def _unpatch_httplib_funcs():
     http.client.HTTPConnection.send = _ori_http_send
 
 
+# end  ** for patch http built-in funcs
+
 
 
 class ErrReponse():
     def __init__(self,errortype):        
         self.errortype = errortype 
 
 
-# HTTPResponse Wraper obj
-# refer to  
-# https://docs.python.org/3/library/http.client.html#httpresponse-objects
+# HTTPResponse Wrapper obj
+# refer to https://docs.python.org/3/library/http.client.html#httpresponse-objects
 class HttpResponse():
     def __init__(self,
-                 httpResponse:http.client.HTTPResponse,
-                 rawBody,
-                 responseTime,
+                 http_response:http.client.HTTPResponse,
+                 raw_body,
+                 response_time,
                  url): # 响应时长毫秒为单位
-        self.httpResponse = httpResponse
-        self.raw = rawBody
-        self.stringBody = None
-        self.jsonObj = None
-        self.responseTime = responseTime
+        self._http_response = http_response
+        self.raw = raw_body
+        self._string_body = None
+        self._json_obj = None
+        self.response_time = response_time
         self.url = url
 
         # 为了兼容错误相应对象 ErrReponse
         # 方便返回判断
         self.errortype = None # 没有错误
-        self.status_code = httpResponse.status
+        self.status_code = http_response.status
     
     def __getattr__(self, attr):
-        return getattr(self.httpResponse, attr) 
+        return getattr(self._http_response, attr) 
 
 
 
     # return decoded string body 
     def string(self,encoding='utf8'):
         try:
-            self.stringBody = self.raw.decode(encoding)
+            self._string_body = self.raw.decode(encoding)
                 
-            return self.stringBody
+            return self._string_body
         except:
             print(f'message body decode with {encoding} failed!!')
             return None
 
     def text(self,encoding='utf8'):
         return self.string(encoding)
     
-    def json(self,encoding='utf8'):
-        try:
-            if self.jsonObj is None:
-                self.jsonObj = jsonlib.loads(self.string(encoding))
+    def json(self,encoding:str='utf8'): 
+        """Parse response body as json
 
-            return self.jsonObj
-        except Exception as e:
-            print('消息体json解码失败!!')
-            print(e)
-            return None
+        Parameters
+        ----------
+        encoding : str, optional
+            _description_, by default 'utf8'
+
+        Returns
+        -------
+        Any
+            Return Python object if parsing successfully, Or raise Exception if parsing failed.
+        """
+        if self._json_obj is None:
+            self._json_obj = jsonlib.loads(self.string(encoding))
+
+        return self._json_obj
+       
 
     
-    def getAllCookies(self):
-        cookiesStr = self.httpResponse.getheader('Set-Cookie')
+    def get_all_cookies(self):
+        cookiesStr = self._http_response.getheader('Set-Cookie')
         if not cookiesStr:
             return {}
             
-        cookieList = self.httpResponse.getheader('Set-Cookie').split(',')
+        cookieList = self._http_response.getheader('Set-Cookie').split(',')
 
         cookieDict = {}
         for c in cookieList:
             kv = c.split(';')[0].split('=')
             cookieDict[kv[0]] = kv[1]
         return cookieDict
 
-    def getCookie(self,cookieName):
-        cookieDict = self.getAllCookies()
+    def get_cookie(self,cookieName):
+        cookieDict = self.get_all_cookies()
         return cookieDict.get(cookieName)
 
 
 
 # refer to https://docs.python.org/3/library/http.client.html#http.client.HTTPConnection
 class HttpClient:
     
@@ -117,19 +130,17 @@
         An HyHTTPConnection instance represents one transaction with an HTTP server.
         """        
         self.timeout     = timeout
         self.proxy       = proxy    # in form of 127.0.0.1:8888
         self._conn       = None     # default HTTPConnection or  HTTPSConnection
         self._conn_table = {}
 
-        self._showAllRawMsg = False
-        self._msgEncodeing = 'utf-8'
         self._httplibPathced = False
 
-    def createConnection(self, protocol, host, port):
+    def create_connection(self, protocol, host, port):
         
         if protocol == 'http':
             connection_class = http.client.HTTPConnection
         elif protocol == 'https':
             connection_class = http.client.HTTPSConnection
         else:
             raise Exception(f'unsupported protocol: {protocol}')
@@ -154,38 +165,34 @@
         except ConnectionRefusedError:
             errInfo = 'connection refused, maybe server not started'
             print('!!! ConnectionRefusedError\n' + errInfo)
             TestLogger.write(f'80|{errInfo}')
             
             raise
 
-        Stats.connectionNumIncreace()
-
+        Stats.connection_num_increace()
 
-    def showRawMsg(self, isShow:bool=True, encoding='utf8'):
-        """
-        show or hide raw http messages
+    @staticmethod
+    def _print_msg(msg :bytes, encoding: str, color=bcolors.OKGREEN, limit=4096):
+        toolong = False
+        if len(msg) > limit:
+            msg = msg[:limit]
+            toolong = True
 
-        Parameters
-        ----------
-        isShow : bool, optional
-            True: show 
-            False: not show
-            
-        encoding : string, optional
-            Message Encoding, default is 'utf8'
-            
-        """
-        self._showAllRawMsg = isShow
-        self._msgEncodeing = encoding
-        if isShow:
-            _patch_httplib_funcs(encoding)
-            self._httplibPathced = True
+        if encoding == 'hex':
+            ostr = msg.hex('\n',-32).upper()           
         else:
-            _unpatch_httplib_funcs()
+            if encoding is None: encoding = 'utf8'
+            ostr = msg.decode(encoding, errors="replace")
+        
+        if toolong:
+            ostr += '\n.................'
+
+        print(color + ostr + bcolors.ENDC, end='')
+
     
 
     @staticmethod
     def _urlAnalyze(url):
         protocol, host, port, path = None, None, None, None
 
         def handleUrlAfterHttpPrefix(url, urlPart, isSecure):
@@ -222,240 +229,314 @@
 
     # send request, https://docs.python.org/3/library/http.client.html#http.client.HTTPConnection.request
     # return HyResponse which is a HTTPResponse Wraper obj
     # args are method, url, body=None, headers=None, 
     def send(self,
             method:str,
             url:str,
-            params=None,
-            data=None, 
+            params:Union[None,Dict[str,str]]=None,
+            headers:Union[None,Dict[str,str]]=None, 
+            data:Union[None,Dict[str,str],str,bytes]=None, 
             json=None,
-            encoding='utf8',
-            headers=None, 
-            duration=None,
-            showRawMsg=False):
+            debug:bool=False,
+            debug_body_print_max_len:int=4096,
+            request_body_encoding:Union[None,str]=None,
+            response_body_encoding:Union[None,str]=None,            
+            # duration:int=None,
+        ):
+        """send HTTP request to server and receive response from server.
+
+        Parameters
+        ----------
+        method : str
+            HTTP method name, like 'GET', 'POST','PUT', 'DELETE','PATCH' ... 
+        url : str
+            HTTP URL for the HTTP request. 
+            The first call must specify protocol/host/port prefix, like 'http://www.abc.com/a/b/c'.
+            The following call could omit that, implying to use previous used protocol/host/port
+        params : 
+            (optional) Dictionary to send in the query string for the HTTP requests.
+        headers : 
+            (optional) Dictionary of HTTP Headers to send with the HTTP requests.
+        data : 
+            (optional) Dictionary, bytes, strings to send in the body of the HTTP requests.
+        json : 
+            (optional) A JSON serializable Python object to send in the body of the HTTP requests.    
+        debug : bool, optional
+            (optional) Whether print whole HTTP request and response, by default False.
+            False : not print
+            True  : print        
+        debug_body_print_max_len : int , optional        
+            (optional) If debug set to True, at most how many chars of HTTP body will be printed. 
+            By default 4096.
+            If body length is larger, the remaining will be replaced with "....."
+        request_body_encoding : str, optional
+            (optional) HTTP request body bytes encoding, all Python char-encoding are supported. 
+            if not specified, hyload will use 'utf8' as text-encoding. 
+        response_body_encoding : str, optional
+            (optional) HTTP response body bytes encoding used for debug print, all Python char-encoding are supported. 
+            if not specified, hyload will try to guess it from `Content-Type`.
+            if no clue in `Content-Type`, it will use 'utf8' as text-encoding.   
+            if set to 'hex', print bytes in hex string format.
+
+        Returns
+        -------
+        _type_
+            _description_
+
+        Raises
+        ------
+        Exception
+            _description_
+        """
         
-        global _sending_http_msg
+        global _http_req_msg_buf_cpy
 
-        if showRawMsg:
+        if debug:
             if not self._httplibPathced:
-                _patch_httplib_funcs(encoding)
+                _patch_httplib_funcs()
                 self._httplibPathced = True
 
         
         protocol, host, port, path = self._urlAnalyze(url)
 
         if not self._conn_table:  # no existing connections
             if protocol is None:
                 raise Exception(f'url error:{url}, should have "http" or "https" as prefix')
             
-            self.createConnection(protocol, host, port)
+            self.create_connection(protocol, host, port)
             # print('no existing connections, create new connection')
 
         else:                     # there are existing connections
 
             if protocol is not None:
                 # print('protocol/host/port specified')
                 self._conn = self._conn_table.get((protocol, host, port))
                 if not self._conn:
                     # print('protocol/host/port not used before, create new connection')
-                    self.createConnection(protocol, host, port)
+                    self.create_connection(protocol, host, port)
                 else:
                     # print('protocol/host/port used before , use old connection')
                     pass
 
             else:
                 # print('protocol/host/port not specified, use default connection self._conn')
                 pass   
              
             
         beforeSendTime = getCurTime()
 
-        
+        # headers 
         if headers is None: 
             headers = {}
-        for k,v in CommonHeaders.items():
+        for k,v in _common_headers.items():
             if k not in headers:
                 headers[k] = v
 
-        # add cookies
+        # cookies
         if len(self._conn.cookie) > 0:
             headers.update({'Cookie':self._conn.cookie.output(header="",attrs=[],sep=';')})
 
-        # url params handle
+        # url params
         if params is not None:
             queryStr = urlencode(params)
             if '?' in path:
                 path += '&' + queryStr
             else:
                 path += '?' + queryStr
 
 
-
+        # body        
         body = None
         # msg body is in format of JSON
         if json is not None:
-            headers['Content-Type'] = 'application/json'
-            body = jsonlib.dumps(json,ensure_ascii=False).encode(encoding)
+            if (request_body_encoding is None): request_body_encoding='utf-8'
+            headers['Content-Type'] = 'application/json; charset=' + request_body_encoding
+            body = jsonlib.dumps(json,ensure_ascii=False).encode(request_body_encoding)
 
         
         # msg body is in format of urlencoded
-        elif data is not None:
+        elif data is not None:                        
             if type(data) == dict:
-                headers['Content-Type'] = 'application/x-www-form-urlencoded'
-                body = urlencode(data).encode(encoding)
+                if (request_body_encoding is None): request_body_encoding='utf-8'
+                headers['Content-Type'] = 'application/x-www-form-urlencoded; charset=' + request_body_encoding
+                body = urlencode(data).encode(request_body_encoding)
             # str类型，编码后放入消息体
             elif type(data) == str:
-                body = data.encode(encoding)
+                if (request_body_encoding is None): request_body_encoding='utf-8'
+                body = data.encode(request_body_encoding)
             # bytes类型，直接放入消息体
             elif type(data) == bytes:
                 body = data
 
         try:
             self._conn.request(method, path, body, headers)
-            if self._showAllRawMsg or showRawMsg:
-                print('\n---------------------------')       
-                print(bcolors.OKGREEN + _sending_http_msg + bcolors.ENDC, end='')
-                _sending_http_msg = ''
+            if debug:
+                print('\n---------------------------')   
+                self._print_msg(
+                    _http_req_msg_buf_cpy, 
+                    request_body_encoding, 
+                    bcolors.OKGREEN, 
+                    debug_body_print_max_len)  
+                _http_req_msg_buf_cpy = b''
                 print('\n---------------------------')    
 
         except ConnectionRefusedError:
             errInfo = 'connection refused, maybe server not started'
             print('!!! ConnectionRefusedError\n' + errInfo)
             TestLogger.write(f'80|{errInfo}')
             
             self._conn.close()
             
             raise
         
         except socket.timeout as e:
             print('!!! socket timeout', e)
-            Stats.oneTimeout()
+            Stats.one_timeout()
 
             self._conn.close()
-            Stats.connectionNumDecreace()
-            # self.createConnection(*self.args, **self.kargs)
+            Stats.connection_num_decreace()
+            # self.create_connection(*self.args, **self.kargs)
 
             TestLogger.write(f'100|time out|{url}')
 
             return ErrReponse(100)
         
         except ConnectionAbortedError as e:
             print('!!! Connection Aborted during sending',e)
-            Stats.oneError()
+            Stats.one_error()
 
             self._conn.close()
-            Stats.connectionNumDecreace()
-            # self.createConnection(*self.args, **self.kargs)
+            Stats.connection_num_decreace()
+            # self.create_connection(*self.args, **self.kargs)
             
             TestLogger.write(f'101|Connection Aborted during sending|{url}')
 
             return ErrReponse(101)
 
-        afterSendTime = Stats.oneSent()
+        afterSendTime = Stats.one_sent()
 
 
         # recv response
         try:
-            httpResponse = self._conn.getresponse()
+            # getresponse() of http.client.Connection only get reponse status line and headers.
+            http_response = self._conn.getresponse()
             
-            if self._showAllRawMsg or showRawMsg:
-                print(bcolors.OKBLUE + f"HTTP/{'1.1' if httpResponse.version==11 else '1.0'} {httpResponse.status} {httpResponse.reason}" + bcolors.ENDC)
-                print(bcolors.OKBLUE + httpResponse.msg.as_string() + bcolors.ENDC,end='')
+            if debug:
+                print(bcolors.OKBLUE + f"HTTP/{'1.1' if http_response.version==11 else '1.0'} {http_response.status} {http_response.reason}" + bcolors.ENDC)
+                print(bcolors.OKBLUE + http_response.msg.as_string() + bcolors.ENDC,end='')
         except socket.timeout as e:
             print('!!! response timeout')
 
-            Stats.oneTimeout()
+            Stats.one_timeout()
 
             self._conn.close()
-            Stats.connectionNumDecreace()
+            Stats.connection_num_decreace()
 
-            # self.createConnection(*self.args, **self.kargs)
+            # self.create_connection(*self.args, **self.kargs)
             
             TestLogger.write(f'110|response time out|{url}')
             return ErrReponse(110)
             
         except ConnectionAbortedError as e:
             print('!!! Connection Aborted during receiving response',e)
-            Stats.oneError()
+            Stats.one_error()
 
             self._conn.close()
-            Stats.connectionNumDecreace()
-            # self.createConnection(*self.args, **self.kargs)
+            Stats.connection_num_decreace()
+            # self.create_connection(*self.args, **self.kargs)
             
             TestLogger.write(f'120|Connection Aborted during receiving response|{url}')
             return ErrReponse(120)
 
         except http.client.RemoteDisconnected as e:
             # 这种情况很可能是 http连接闲置时间过长，服务端断开了连接，尝试重发            
             self._conn.close()
-            Stats.connectionNumDecreace()
+            Stats.connection_num_decreace()
 
-            # self.createConnection(*self.args, **self.kargs)
+            # self.create_connection(*self.args, **self.kargs)
 
             try:
                 self._conn.request(method, path, body, headers)
-                afterSendTime = Stats.oneSent()
-                httpResponse = self._conn.getresponse()
+                afterSendTime = Stats.one_sent()
+                http_response = self._conn.getresponse()
 
                 info = f'* after sending, server closed connection, reconnect and resending succeed|{url}'
                 print(info)
                 TestLogger.write(info)
             except:
-                Stats.oneError()
+                Stats.one_error()
                 self._conn.close()
-                Stats.connectionNumDecreace()
-                # self.createConnection(*self.args, **self.kargs)
+                Stats.connection_num_decreace()
+                # self.create_connection(*self.args, **self.kargs)
                             
                 err = f'130|after sending, server closed connection, reconnect and resending failed|{url}'
                 print(err)
                 TestLogger.write(err)
                 return ErrReponse(130)
                 
 
         # 下面是 可以正常接收响应 情况下 的代码
 
-        recvTime = Stats.oneRecv(afterSendTime)
+        recvTime = Stats.one_recv(afterSendTime)
 
         # check cookie
-        cookieHdrs = httpResponse.getheader('set-cookie')
+        cookieHdrs = http_response.getheader('set-cookie')
         if cookieHdrs:
             # print (cookieHdrs)
             self._conn.cookie.load(cookieHdrs)
 
-        # 如果 有 duration，需要接收完消息后sleep一点时间，确保整体时间为duration
-        if duration:
+        # # 如果 有 duration，需要接收完消息后sleep一点时间，确保整体时间为duration
+        # if duration:
             
-            # print(f'send {beforeSendTime} -- recv {recvTime}')
-            extraWait = duration-(recvTime-beforeSendTime)
-            if extraWait >0:  # 因为小于1ms的sleep通常就是不准确的
-                # print(f'sleep {extraWait}')
-                time.sleep(extraWait)
-
-        
-        rawBody = httpResponse.read()
-        
-        if self._showAllRawMsg or showRawMsg:
-            outputStr = rawBody.decode(self._msgEncodeing)
-            if len(outputStr) > 2048:
-                outputStr = outputStr[:2000] + '\n.................'
-            print(bcolors.OKBLUE + outputStr+ bcolors.ENDC)
+        #     # print(f'send {beforeSendTime} -- recv {recvTime}')
+        #     extraWait = duration-(recvTime-beforeSendTime)
+        #     if extraWait >0:  # 因为小于1ms的sleep通常就是不准确的
+        #         # print(f'sleep {extraWait}')
+        #         time.sleep(extraWait)
+
+        
+        raw_body = http_response.read()
+        
+        if debug:
+            contentEncoding = http_response.getheader('Content-Encoding')
+            if contentEncoding == 'gzip':
+                try: raw_body = gzip.decompress(raw_body)
+                except OSError: pass      
+
+            if response_body_encoding is None:
+                contentType = http_response.getheader('Content-Type')
+                response_body_encoding = self._guessEncodingFromContentType(contentType)
+
+            self._print_msg(
+                raw_body,
+                response_body_encoding, 
+                bcolors.OKBLUE,
+                debug_body_print_max_len)           
             print('\n')
 
 
-        self.response = HttpResponse(httpResponse,
-                                   rawBody,
+        self.response = HttpResponse(http_response,
+                                   raw_body,
                                    int((recvTime-afterSendTime)*1000),
                                    path)
         
      
             
             
         return self.response
     
+    @staticmethod
+    def _guessEncodingFromContentType(contentType):
+        if contentType is not None:
+            for one in contentType.replace(' ','').split(';'):
+                if one.startswith('charset='):
+                    return one[8:]
+        return 'utf-8'
+
 
     def  get(self,*args,**kargs):
         return self.send('GET',*args,**kargs)
         
     def  post(self,*args,**kargs):
         return self.send('POST',*args,**kargs)
```

## hyload/logger.py

```diff
@@ -67,25 +67,32 @@
 
 # 测试日志
 class TestLogger:
 
     logFh  = None
 
     @classmethod
-    def openLog(cls):
+    def open_log(cls):
         dt = datetime.now().strftime("%Y-%m-%d_%H.%M.%S")
 
         logPath = getCommandArg('logPath')
         if logPath is None:
             logPath = './log'
 
         os.makedirs(logPath,exist_ok=True)
         logFile = os.path.join(logPath,f'{dt}.log')
 
         cls.logFh = open(logFile,'w',encoding='utf8',buffering=1) 
     
     @classmethod
-    def write(cls,info):
+    def write(cls,info:str):
+        """write the parameter string into log file.
+
+        Parameters
+        ----------
+        info : str
+            the string to be written into log file.
+        """
         if not cls.logFh:
-            cls.openLog()
+            cls.open_log()
         
         cls.logFh.write(f'{getCurTime():.4f}|{info}\n')
```

## hyload/stats.py

```diff
@@ -1,12 +1,13 @@
 from hyload.util import getCurTime
 import time,sys,json,socket,os,gevent
 import http.client
 from urllib.parse import quote_plus
-
+from .logger import TestLogger
+from typing import Union
 
 class bcolors:
     HEADER = '\033[95m'
     OKBLUE = '\033[94m'
     OKCYAN = '\033[96m'
     OKGREEN = '\033[92m'
     YELLOW = '\033[33m'
@@ -48,15 +49,15 @@
     if statsDir:
         os.makedirs(statsDir,exist_ok=True)
     foStats = open(StatsFile,'wb')
 
 class Stats:
     
     @staticmethod
-    def waitForTasksDone(tasks:list=None):
+    def wait_for_tasks_done(tasks:list=None):
         gevent.wait(tasks) # wait for tasks end
         time.sleep(1) # wait for stats routine to send last second stats
         print('\n==== 运行结束 ====')
 
     @classmethod
     def clear(cls):
         cls.startTime = getCurTime()
@@ -154,15 +155,15 @@
             table.pop(lastSecond)
         else:
             statsOneSecond[tableName] = 0
 
 
     # 一秒结束后的统计处理
     @classmethod
-    def oneSecondDataDoneStats(cls,lastSecond):
+    def _one_second_data_done_stats(cls,lastSecond):
         strLastSecond = time.strftime('%H:%M:%S',time.localtime(lastSecond))
          
         # 如果上一秒没有什么有效信息
         # 表示 要么是上1秒没有收发数据也没有超时错误，要么是 上1秒的统计已经发送出去 
         # 这次都不需要发送统计
         if (lastSecond not in cls.rpsTable) and \
             (lastSecond not in cls.tpsTable) and \
@@ -239,25 +240,27 @@
 
         # 发送到 console的 并发连接数量 数据
         # 目前侦测到连接断开比较麻烦，暂时先不做并发连接的统计
         # cls._sendStatsToConsoleUdp({'connNum':cls.connectionNumber})
 
     @classmethod
     def start(cls):
+        """
+        Run stats routine.
+        """
         cls.clear()
         cls.runFlag = True  # 启动标识
 
-        gevent.spawn(cls.independentCheck)
-
+        gevent.spawn(cls._independent_check)
 
                 
     # 独立检查协程，检查上一秒统计数据是否发出了
     # 应该只对最后一秒有效，主统计协程里面发现到了新一秒会发送上一秒的统计
     @classmethod
-    def independentCheck(cls):
+    def _independent_check(cls):
 
         # 总是发送上一秒的统计，因为当前秒还没有结束，总计发送接收消息数量统计没有结束
         while True:
 
             if not cls.runFlag:
                 break
 
@@ -265,71 +268,74 @@
             time.sleep(0.4)
 
             curTime = getCurTime()
 
             # get last second to measure
             lastSecond = int(curTime) - 1
 
-            cls.oneSecondDataDoneStats(lastSecond)
+            cls._one_second_data_done_stats(lastSecond)
 
 
     @classmethod
     def stop(cls):
+        """
+        Stop stats routine.
+        """
         # wait for more than 1 second, so stats greenlet could count last second
         time.sleep(1.2)
         cls.runFlag = False
 
     # 更新 以秒为单位的统计表
     @classmethod
-    def measurePerSecond(cls, recTable, addAmount, curTime=None):
+    def _measure_per_second(cls, recTable, addAmount, curTime=None):
         
         if curTime is None:
             curTime = getCurTime()
 
         # get cur second to measure
         curSecond = int(curTime)
         # new second to stats
         if curSecond not in recTable:          
             recTable[curSecond] = addAmount
             # 新的一秒，看看前1秒统计有没有总结处理
-            cls.oneSecondDataDoneStats(curSecond-1)
+            cls._one_second_data_done_stats(curSecond-1)
         # add one to  stats
         else:
             recTable[curSecond] += addAmount
         
         return curTime
 
     @classmethod
-    def oneSent(cls):
+    def one_sent(cls):
 
-        sentTime = cls.measurePerSecond(cls.rpsTable,1)
+        sentTime = cls._measure_per_second(cls.rpsTable,1)
         cls.totalSend +=1
 
 
         return sentTime
 
 
     @classmethod
-    def connectionNumIncreace(cls):
+    def connection_num_increace(cls):
         cls.connectionNumber +=1
 
     @classmethod
-    def connectionNumDecreace(cls):
+    def connection_num_decreace(cls):
         cls.connectionNumber -=1
 
 
         
     @classmethod
-    def oneRecv(cls,sentTime):
+    def one_recv(cls,sentTime):
                 
-        recvTime = cls.measurePerSecond(cls.tpsTable,1)
+        recvTime = cls._measure_per_second(cls.tpsTable,1)
         cls.totalRecv +=1
 
         duration = recvTime - sentTime
-        cls.measurePerSecond(cls.responseTimeTable,duration,recvTime)
+        cls._measure_per_second(cls.responseTimeTable,duration,recvTime)
 
         
         if duration < 0.1 :
             cls.resptimeRange['<100ms'] += 1
         elif 0.1<= duration < 0.5 :
             cls.resptimeRange['100-500ms'] += 1
         elif 0.5<= duration < 1 :
@@ -338,24 +344,34 @@
             cls.resptimeRange['1000-3000ms'] += 1
         else :
             cls.resptimeRange['>=3000ms'] += 1
 
         return recvTime
 
     @classmethod
-    def oneTimeout(cls):
+    def one_timeout(cls):
 
-        cls.measurePerSecond(cls.timeoutTable, 1)
+        cls._measure_per_second(cls.timeoutTable, 1)
         cls.totalTimeout += 1
 
         return
 
 
     @classmethod
-    def oneError(cls):
+    def one_error(cls, log_info: Union[None,str] = None):
+        """
+        Add one error to the statistics result, and write the error info to log file if needed.
+
+        Parameters
+        ----------
+        log_info : Union[None,str], optional
+            (Optional) the error info to be written to log file.
+        """
 
-        cls.measurePerSecond(cls.errorTable, 1)
+        cls._measure_per_second(cls.errorTable, 1)
         cls.totalError += 1
 
+        if log_info:
+            TestLogger.write(log_info)
         return
 
 Stats.clear()
```

## hyload/tools/remoteop.py

```diff
@@ -25,15 +25,15 @@
 
         print('ok')
 
 
 
     def remoteCmd(self, cmd, printCmd=True,printOutput=True):
         if printCmd:
-            print(f'>> {cmd}')
+            print(f'$ {cmd}')
         stdin, stdout, stderr = self.ssh.exec_command(cmd)
         output = stdout.read().decode('utf8')
         errinfo = stderr.read().decode()
         if printOutput:
             print(output+errinfo)
         return output+errinfo
 
@@ -104,16 +104,21 @@
     os.makedirs(localDir,exist_ok=True)
 
 
     ro = RemoteOp(HOST,PORT,USER, PASSWD, SSHKEY)
 
     # package files 
 
-    ro.remoteCmd(f'cd {remoteDir};rm -rf tmp.tar.gz;tar zcvf tmp.tar.gz {filesStr}')
+    out = ro.remoteCmd(f'cd {remoteDir};rm -rf tmp.tar.gz;tar zcvf tmp.tar.gz {filesStr}')
 
+    if 'Exiting with failure' in out:
+        return
+
+
+ 
 
     localFilePath = os.path.join(localDir,'tmp.tar.gz')
     ro.getFile(remoteDir+'/tmp.tar.gz', localFilePath)
 
 
     import tarfile
     tar = tarfile.open(localFilePath, "r:gz")
```

## Comparing `hyload-0.2.2.dist-info/LICENSE.txt` & `hyload-0.2.4.dist-info/LICENSE.txt`

 * *Files identical despite different names*

## Comparing `hyload-0.2.2.dist-info/METADATA` & `hyload-0.2.4.dist-info/METADATA`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hyload
-Version: 0.2.2
+Version: 0.2.4
 Summary: Framework for load testing
 Home-page: http://www.byhy.net
 Download-URL: https://pypi.python.org/pypi/hyload
 Author: baiyueheiyu 白月黑羽
 Author-email: jcyrss@gmail.com
 License: Apache License 2.0
 Keywords: hyload loadtesting
@@ -14,14 +14,15 @@
 Classifier: License :: OSI Approved :: Apache Software License
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 Requires-Dist: gevent (>=20.9.0)
 Requires-Dist: matplotlib
 Requires-Dist: paramiko
+Requires-Dist: websockets
 
 ## Introduction
 
 hyload 是一款性能测试库。目前针对HTTP接口的服务端系统进行性能压力测试。
 
 它提供了一个高效异步收发HTTP消息的库，可以让你使用Python语言自己开发代码。
```

## Comparing `hyload-0.2.2.dist-info/RECORD` & `hyload-0.2.4.dist-info/RECORD`

 * *Files 24% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 hyload/__init__.py,sha256=wXjdLCvcOlQV8a7Mku2cQbyWRXheGf7dGkHfjvBqKu8,171
-hyload/cfg.py,sha256=5FDM-eOsLqzqxqtXBwnVdT4vctBDStFcdQ__igt6HEw,17
-hyload/httpclient.py,sha256=xsbuhB5Pg1to47J-lMcxSh3N2-bFqezK8KsfInoRYOk,15612
-hyload/logger.py,sha256=JR8uUXypCp9eaWvKZRT_pqtUYRbATkC2XCKIB9R_ptM,2439
-hyload/stats.py,sha256=emUBJSTzSWh4mJJBFxzKTY-1ByLcCLsDZoLlqyBYp3M,10760
+hyload/cfg.py,sha256=cdNJF8QEyAN-FijrgwJpayHDazweFlMrOghMDR5x47w,17
+hyload/httpclient.py,sha256=8fjF_T6i8q4Y1HEVKv97Qdn14SgdpqFBnDbup3RtAr4,19401
+hyload/logger.py,sha256=CfxUQM7oPiWuiuXmtiQiD5ViXkdY1t5yo8-SvRWO1q8,2627
+hyload/stats.py,sha256=eiC1a-c-_QBXqE5LUKEbCZcSPQLZyIARwPGk3BKBG74,11344
 hyload/util.py,sha256=lNKVVW4vYFueXcvOC4HoIMIiXFUz6skR9shSA7iPsWU,979
 hyload/tools/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 hyload/tools/plotperf.py,sha256=H1OszxmfgAYAxX4YEp-_aX66w6slynz9tjDGdpraMMo,3667
 hyload/tools/plotresource.py,sha256=9ydos2xFSA__ANhQ4b_fr5ORJPwWVLCgXoYnYdO5cA4,2802
 hyload/tools/puttyagents.py,sha256=NvL3VhYYka69kh7QTdRzjm7dLN3dB5MuU__K1GmGsW8,39521
-hyload/tools/remoteop.py,sha256=yyySauc3rSc03jsJ1n_6dKuIv-Vlo6W-TSC5EOI-VEQ,3940
+hyload/tools/remoteop.py,sha256=eJ7gSwJNzNIZfOU--5F_MNiy8laA9EBqIXtsuE83ZH8,4007
 hyload/tools/statshub.py,sha256=bPyj9h6eewxRJSJmQpqtkx3DFbvoYbQsWpcFvATFang,7493
-hyload-0.2.2.dist-info/LICENSE.txt,sha256=OGhxEO0MAMle3LEQV8Us5uo4C8pk-jWmCBKyQ7U_gCE,1100
-hyload-0.2.2.dist-info/METADATA,sha256=TG_Iioma4bo34bSb4pafU3Ti5L5eecia4LTT4uRj0HM,1482
-hyload-0.2.2.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
-hyload-0.2.2.dist-info/top_level.txt,sha256=ivEyc-v2p5WU0itBl-u9QARFubEqBlHfczIhYbuD_U8,7
-hyload-0.2.2.dist-info/RECORD,,
+hyload-0.2.4.dist-info/LICENSE.txt,sha256=OGhxEO0MAMle3LEQV8Us5uo4C8pk-jWmCBKyQ7U_gCE,1100
+hyload-0.2.4.dist-info/METADATA,sha256=Yx6QaPhZosD0qVlOfbEOXmsnLPcOPP-4ES459-PFQ1o,1509
+hyload-0.2.4.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
+hyload-0.2.4.dist-info/top_level.txt,sha256=ivEyc-v2p5WU0itBl-u9QARFubEqBlHfczIhYbuD_U8,7
+hyload-0.2.4.dist-info/RECORD,,
```

