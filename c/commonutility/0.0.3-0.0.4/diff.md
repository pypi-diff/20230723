# Comparing `tmp/commonUtility-0.0.3-py3-none-any.whl.zip` & `tmp/commonutility-0.0.4-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,8 +1,8 @@
-Zip file size: 3871 bytes, number of entries: 6
--rw-rw-r--  2.0 unx     6562 b- defN 23-Jun-12 12:34 commonutility/__init__.py
--rw-rw-r--  2.0 unx     1073 b- defN 23-Jun-12 12:37 commonUtility-0.0.3.dist-info/LICENCE.txt
--rw-rw-r--  2.0 unx      533 b- defN 23-Jun-12 12:37 commonUtility-0.0.3.dist-info/METADATA
--rw-rw-r--  2.0 unx       92 b- defN 23-Jun-12 12:37 commonUtility-0.0.3.dist-info/WHEEL
--rw-rw-r--  2.0 unx       14 b- defN 23-Jun-12 12:37 commonUtility-0.0.3.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx      501 b- defN 23-Jun-12 12:37 commonUtility-0.0.3.dist-info/RECORD
-6 files, 8775 bytes uncompressed, 2957 bytes compressed:  66.3%
+Zip file size: 3164 bytes, number of entries: 6
+-rw-rw-r--  2.0 unx     2732 b- defN 23-Jul-23 16:22 commonutility/__init__.py
+-rw-rw-r--  2.0 unx     1073 b- defN 23-Jul-23 16:35 commonutility-0.0.4.dist-info/LICENCE.txt
+-rw-rw-r--  2.0 unx      533 b- defN 23-Jul-23 16:35 commonutility-0.0.4.dist-info/METADATA
+-rw-rw-r--  2.0 unx       92 b- defN 23-Jul-23 16:35 commonutility-0.0.4.dist-info/WHEEL
+-rw-rw-r--  2.0 unx       14 b- defN 23-Jul-23 16:35 commonutility-0.0.4.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx      501 b- defN 23-Jul-23 16:35 commonutility-0.0.4.dist-info/RECORD
+6 files, 4945 bytes uncompressed, 2250 bytes compressed:  54.5%
```

## zipnote {}

```diff
@@ -1,19 +1,19 @@
 Filename: commonutility/__init__.py
 Comment: 
 
-Filename: commonUtility-0.0.3.dist-info/LICENCE.txt
+Filename: commonutility-0.0.4.dist-info/LICENCE.txt
 Comment: 
 
-Filename: commonUtility-0.0.3.dist-info/METADATA
+Filename: commonutility-0.0.4.dist-info/METADATA
 Comment: 
 
-Filename: commonUtility-0.0.3.dist-info/WHEEL
+Filename: commonutility-0.0.4.dist-info/WHEEL
 Comment: 
 
-Filename: commonUtility-0.0.3.dist-info/top_level.txt
+Filename: commonutility-0.0.4.dist-info/top_level.txt
 Comment: 
 
-Filename: commonUtility-0.0.3.dist-info/RECORD
+Filename: commonutility-0.0.4.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## commonutility/__init__.py

```diff
@@ -1,13 +1,11 @@
 import socket
 
 import os
 import zipfile
-import json
-import loggerutility as logger
 
 
 def get_machine_ip():
     """
     Retrieve the current machine IP address
 
     :return: IP address
@@ -68,95 +66,27 @@
                             <type>E</type>
                         </error>
                     </Errors>
                 </Root>'''
 
     return errorXml
 
-def getTraineModelPath(modelType, modelName, modelScope, enterprise_key=""):
-        modelPath=""
-        logger.log("inside getTraineModelPath","0")
-        logger.log(f"modelScope 78::{modelScope}", "0")
-        modelScope =  "global" if modelScope=="G" or modelScope=="global" or modelScope=="g" else "enterprise"
-        logger.log(f"modelScope 80::{modelScope}", "0")
-        if modelScope=="global":
-            logger.log("inside getTraineModelPath if","0")
-            modelPath = "/proteus-sense/trained_model/" + modelType.lower() + "/" + modelScope.lower() +  "/"+ modelName.lower()
-        else:
-            logger.log("inside getTraineModelPath else ","0")
-            modelPath = "/proteus-sense/trained_model/" +  modelType.lower()  + "/" + modelScope.lower() + "/" + enterprise_key.lower() +  "/"+ modelName.lower()
-        if not os.path.exists(modelPath):
-            os.makedirs(modelPath)
-            logger.log(f"inside getTraineModelPath modelPath::{modelPath}","0")
-        return modelPath
-
-def createModelScope(modelScope, modelType, modelName, enterprise_key=""):
-        path = "/proteus-sense/trained_model"
-        fileName = "modelScope.json"
-        filePath = path + "/" + fileName
-        if os.path.exists(filePath):
-            logger.log(f"File already exists.","0")
-        else:
-            if not os.path.exists(path):
-                os.makedirs(path)   
-            with open (filePath,"w") as file:
-                fileData={}
-                fileData=str(fileData).replace("'", '"')
-                logger.log(f"after{str(fileData)}","0")
-                file.write(fileData)
-                file.close()
-                if os.path.exists(filePath):
-                    logger.log(f"File created","0")
-
-        with open (filePath,"r") as file:
-            FilejsonData = file.read()
-            file.close()
-            logger.log(f"FilejsonData::{FilejsonData},{type(FilejsonData)}","0")
-
-            modelScopefileJson=json.loads(FilejsonData)
-            logger.log(f"parsedJsonData::{modelScopefileJson},{type(modelScopefileJson)}","0")
-        
-        if modelScope == "global":
-            if modelType in modelScopefileJson:
-                if modelScope in modelScopefileJson[modelType]:
-                    if modelName not in modelScopefileJson[modelType][modelScope]:
-                        modelScopefileJson[modelType][modelScope].append(modelName)
-                    else:
-                        logger.log(f"ModelName exists","0")
-                    logger.log(f"if::{modelScopefileJson}","0")
-
-                else:
-                    modelScopefileJson[modelType][modelScope] = [modelName]
-            else:
-                modelScopefileJson[modelType] = {modelScope :[modelName]}
-        
-        elif modelScope == "enterprise":
-            if modelType in modelScopefileJson:
-                if modelScope in modelScopefileJson[modelType]:
-                    if enterprise_key not in modelScopefileJson[modelType][modelScope]:
-                        modelScopefileJson[modelType][modelScope][enterprise_key]=[modelName]
-                    else:    
-                        if not modelName in modelScopefileJson[modelType][modelScope][enterprise_key]:
-                            modelScopefileJson[modelType][modelScope][enterprise_key].append(modelName)
-                        else:
-                            logger.log(f"ModelName exists","0")
-                else:
-                    modelScopefileJson[modelType][modelScope] = {enterprise_key:[modelName]}
-            else:
-                modelScopefileJson[modelType] = {modelScope: {enterprise_key:[modelName]}}
-        else:
-            logger.log(f"Invalid modelScope received:: {modelScope}","0")
-        
-        logger.log(f"data: {modelScopefileJson}","0")
-
-        with open (filePath,"w") as file:
-            logger.log(f"modelScopefileJson in write mode;::: {modelScopefileJson}","0")    
-            modelScopefileJson=str(modelScopefileJson).replace("'", '"')
-            logger.log(f"after line 1198 :: {str(modelScopefileJson)}","0")
-            file.write(modelScopefileJson)
-            file.close()
-            logger.log(f"File updated","0")
-        
-        return "File Updated successfully "
-    
+def getErrorJson(Message,description):
+    errorjson = '''{
+                "Root": {
+                "Header": {
+                    "editFlag": "null"
+                            },
+                "Errors":   [
+                {
+                   "error": {
+                    "message": "'''+Message+'''",
+                    "description": "'''+description+'''",
+                    "type": "E"
+                     }
+                }
+                    ]
+                        }
+                    }'''
+    return errorjson
```

## Comparing `commonUtility-0.0.3.dist-info/LICENCE.txt` & `commonutility-0.0.4.dist-info/LICENCE.txt`

 * *Files identical despite different names*

## Comparing `commonUtility-0.0.3.dist-info/METADATA` & `commonutility-0.0.4.dist-info/METADATA`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: commonUtility
-Version: 0.0.3
+Name: commonutility
+Version: 0.0.4
 Summary: Proteus zipcommon File
 Author: Proteus Technology PVT. LTD.
 Author-email: <apps@baseinformation.com>
 Keywords: python,first package
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Education
 Classifier: Programming Language :: Python :: 2
```

