# Comparing `tmp/Google-Ads-Transparency-Scraper-1.5.8.tar.gz` & `tmp/Google-Ads-Transparency-Scraper-1.6.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Google-Ads-Transparency-Scraper-1.5.8.tar", last modified: Wed Jul 19 11:09:43 2023, max compression
+gzip compressed data, was "Google-Ads-Transparency-Scraper-1.6.0.tar", last modified: Sun Jul 23 11:39:12 2023, max compression
```

## Comparing `Google-Ads-Transparency-Scraper-1.5.8.tar` & `Google-Ads-Transparency-Scraper-1.6.0.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 fani      (1000) fani      (1000)        0 2023-07-19 11:09:43.403531 Google-Ads-Transparency-Scraper-1.5.8/
-drwxr-xr-x   0 fani      (1000) fani      (1000)        0 2023-07-19 11:09:43.403531 Google-Ads-Transparency-Scraper-1.5.8/GoogleAds/
--rw-r--r--   0 fani      (1000) fani      (1000)       55 2023-07-19 09:38:14.000000 Google-Ads-Transparency-Scraper-1.5.8/GoogleAds/__init__.py
--rw-r--r--   0 fani      (1000) fani      (1000)    10660 2023-07-19 11:07:49.000000 Google-Ads-Transparency-Scraper-1.5.8/GoogleAds/main.py
--rw-r--r--   0 fani      (1000) fani      (1000)    11448 2023-07-19 09:14:20.000000 Google-Ads-Transparency-Scraper-1.5.8/GoogleAds/regions.py
-drwxr-xr-x   0 fani      (1000) fani      (1000)        0 2023-07-19 11:09:43.403531 Google-Ads-Transparency-Scraper-1.5.8/Google_Ads_Transparency_Scraper.egg-info/
--rw-r--r--   0 fani      (1000) fani      (1000)      858 2023-07-19 11:09:43.000000 Google-Ads-Transparency-Scraper-1.5.8/Google_Ads_Transparency_Scraper.egg-info/PKG-INFO
--rw-r--r--   0 fani      (1000) fani      (1000)      363 2023-07-19 11:09:43.000000 Google-Ads-Transparency-Scraper-1.5.8/Google_Ads_Transparency_Scraper.egg-info/SOURCES.txt
--rw-r--r--   0 fani      (1000) fani      (1000)        1 2023-07-19 11:09:43.000000 Google-Ads-Transparency-Scraper-1.5.8/Google_Ads_Transparency_Scraper.egg-info/dependency_links.txt
--rw-r--r--   0 fani      (1000) fani      (1000)       69 2023-07-19 11:09:43.000000 Google-Ads-Transparency-Scraper-1.5.8/Google_Ads_Transparency_Scraper.egg-info/requires.txt
--rw-r--r--   0 fani      (1000) fani      (1000)       10 2023-07-19 11:09:43.000000 Google-Ads-Transparency-Scraper-1.5.8/Google_Ads_Transparency_Scraper.egg-info/top_level.txt
--rw-r--r--   0 fani      (1000) fani      (1000)      858 2023-07-19 11:09:43.403531 Google-Ads-Transparency-Scraper-1.5.8/PKG-INFO
--rw-r--r--   0 fani      (1000) fani      (1000)     5443 2023-07-19 09:44:59.000000 Google-Ads-Transparency-Scraper-1.5.8/README.md
--rw-r--r--   0 fani      (1000) fani      (1000)       79 2023-07-19 11:09:43.403531 Google-Ads-Transparency-Scraper-1.5.8/setup.cfg
--rw-r--r--   0 fani      (1000) fani      (1000)     1273 2023-07-19 11:08:22.000000 Google-Ads-Transparency-Scraper-1.5.8/setup.py
+drwxr-xr-x   0 fani      (1000) fani      (1000)        0 2023-07-23 11:39:12.245537 Google-Ads-Transparency-Scraper-1.6.0/
+drwxr-xr-x   0 fani      (1000) fani      (1000)        0 2023-07-23 11:39:12.241537 Google-Ads-Transparency-Scraper-1.6.0/GoogleAds/
+-rw-r--r--   0 fani      (1000) fani      (1000)       55 2023-07-19 09:38:14.000000 Google-Ads-Transparency-Scraper-1.6.0/GoogleAds/__init__.py
+-rw-r--r--   0 fani      (1000) fani      (1000)    11774 2023-07-23 06:26:08.000000 Google-Ads-Transparency-Scraper-1.6.0/GoogleAds/main.py
+-rw-r--r--   0 fani      (1000) fani      (1000)    11448 2023-07-19 09:14:20.000000 Google-Ads-Transparency-Scraper-1.6.0/GoogleAds/regions.py
+drwxr-xr-x   0 fani      (1000) fani      (1000)        0 2023-07-23 11:39:12.245537 Google-Ads-Transparency-Scraper-1.6.0/Google_Ads_Transparency_Scraper.egg-info/
+-rw-r--r--   0 fani      (1000) fani      (1000)      858 2023-07-23 11:39:12.000000 Google-Ads-Transparency-Scraper-1.6.0/Google_Ads_Transparency_Scraper.egg-info/PKG-INFO
+-rw-r--r--   0 fani      (1000) fani      (1000)      363 2023-07-23 11:39:12.000000 Google-Ads-Transparency-Scraper-1.6.0/Google_Ads_Transparency_Scraper.egg-info/SOURCES.txt
+-rw-r--r--   0 fani      (1000) fani      (1000)        1 2023-07-23 11:39:12.000000 Google-Ads-Transparency-Scraper-1.6.0/Google_Ads_Transparency_Scraper.egg-info/dependency_links.txt
+-rw-r--r--   0 fani      (1000) fani      (1000)       69 2023-07-23 11:39:12.000000 Google-Ads-Transparency-Scraper-1.6.0/Google_Ads_Transparency_Scraper.egg-info/requires.txt
+-rw-r--r--   0 fani      (1000) fani      (1000)       10 2023-07-23 11:39:12.000000 Google-Ads-Transparency-Scraper-1.6.0/Google_Ads_Transparency_Scraper.egg-info/top_level.txt
+-rw-r--r--   0 fani      (1000) fani      (1000)      858 2023-07-23 11:39:12.245537 Google-Ads-Transparency-Scraper-1.6.0/PKG-INFO
+-rw-r--r--   0 fani      (1000) fani      (1000)     5657 2023-07-23 11:33:53.000000 Google-Ads-Transparency-Scraper-1.6.0/README.md
+-rw-r--r--   0 fani      (1000) fani      (1000)       79 2023-07-23 11:39:12.245537 Google-Ads-Transparency-Scraper-1.6.0/setup.cfg
+-rw-r--r--   0 fani      (1000) fani      (1000)     1273 2023-07-23 06:25:44.000000 Google-Ads-Transparency-Scraper-1.6.0/setup.py
```

### Comparing `Google-Ads-Transparency-Scraper-1.5.8/GoogleAds/main.py` & `Google-Ads-Transparency-Scraper-1.6.0/GoogleAds/main.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+import json
 import datetime
 import requests
 from typing import Union
 from bs4 import BeautifulSoup as soap
 from GoogleAds.regions import Regions
 
 HEADERS = {
@@ -41,15 +42,15 @@
             self.reqs.proxies.update(proxy)
 
         self.r_check = True
         if region == "anywhere":
             self.r_check = False
         print((not Regions.get(region)) and self.r_check)
         if (not Regions.get(region)) and self.r_check:
-            raise Exception("Invalid Region Code")
+            raise ValueError(f"Region: {region} is not supported, Please call the show_region_list() function to get supported regions list")
         self.region = region
         self.region_num = Regions[region]["1"] if self.r_check else 0
         self.get_cookies()
 
     def get_cookies(self):
         """Get Cookies from the main url https://adstransparency.google.com/ and store them in requests Session"""
         params = {
@@ -109,48 +110,82 @@
             return {"Advertisor Id": ad["1"], "Name":ad["12"]}
         #if ads := response.json().get("1"):
         #    with open("new.json", "w") as f:
         #        json.dump(ads, f)
         #    return [{"Advertisor Id": ad[1],"Creative Id":ad["2"]} for ad in ads]
         #return []
 
-    def creative_search_by_advertiser_id(self, advertiser_id: str) -> list:    #TODO do region search
-        """Get Creatives or ads by quering given Advertisor Id
-        If no Ad found return []"""
+    def creative_search_by_advertiser_id(self, advertiser_id: str, count: int=40, next_page_id: str="") -> list:    #TODO do region search
+        """Get Creatives or ads by querying given Advertiser Id.
+        If no Ad is found, return an empty list.
+
+        Args:
+            self: The instance of the class.
+            advertiser_id (str): The ID of the advertiser.
+
+        Returns:
+            list: A list of creatives or ads."""
+
         data = {
-            'f.req': '{"2":40,"3":{"12":{"1":"","2":true},"13":{"1":["' + advertiser_id + '"]}}, "7":{"1":1}}',
+            'f.req': {
+                "2": min(count, 100),
+                "3": {"12": {"1": "", "2": True}, "13": {"1": [advertiser_id]}},
+                "7": {"1": 1},
+            }
         }
+        if next_page_id:
+            data['f.req']["4"] = next_page_id
         if self.r_check:
-            data = {
-            'f.req': '{"2":40,"3":{"8":[' + str(self.region_num) + '],"12":{"1":"","2":true},"13":{"1":["' + advertiser_id + '"]}}, "7":{"1":1}}',
-        }
+            data['f.req']["3"]["8"] = [self.region_num]
+
+        data['f.req'] = json.dumps(data['f.req'])
+
+
         response = self.reqs.post(
             'https://adstransparency.google.com/anji/_/rpc/SearchService/SearchCreatives',
             params={'authuser': ''},
             data=data,
         )
-        return [ad["2"] for ad in ads] if (ads := response.json().get("1")) else []
 
-    def get_creative_Ids(self, keyword: str) -> dict:
+        res = response.json()
+        ads = res.get("1", [])
+        ads = [ad["2"] for ad in ads]
+        next_page_id = res.get("2")
+        if count <= 100 or not ads or next_page_id is None:
+            return ads[:count]
+        count -= len(ads)
+        ads.extend(self.creative_search_by_advertiser_id(advertiser_id, count, next_page_id))
+        return ads
+
+    def get_creative_Ids(self, keyword: str, count: int =40) -> dict:
         """Makes search for given keyword and gets the first Suggestion. Then gets the Creatives for that.
         Returns Advertisor Name, Id, Ad count and List of Creatives"""
-        if not (search := self.get_first_search_suggestion(keyword)):
-            return {"Advertisor": "", "Advertisor Id":"", "Ad Count": 0, "Creatives": []}
-        print(search)
-
-        if search.get("2"): 
-            if not (advertisor := self.get_advistisor_by_domain(domain=search["2"]["1"])):
-                return {"Advertisor": "", "Advertisor Id":"", "Ad Count": 0, "Creatives": []}
+        search = self.get_first_search_suggestion(keyword)
+        if not search:
+            return {"Advertisor": "", "Advertisor Id": "", "Ad Count": 0, "Creative_Ids": []}
+
+        if search.get("2"):
+            domain = search["2"]["1"]
+            advertisor = self.get_advistisor_by_domain(domain=domain)
+            if not advertisor:
+                return {"Advertisor": "", "Advertisor Id": "", "Ad Count": 0, "Creative_Ids": []}
             suggestions = self.get_all_search_suggestions(advertisor["Name"])
             search = next((suggestion for suggestion in suggestions if suggestion["1"]["1"] == advertisor["Name"] and suggestion["1"]["2"] == advertisor["Advertisor Id"]), None)
+
         advertisor = search["1"]["1"]
-        Ad_count = search['1']['4']['2']['2'] if search["1"].get("4") else 0
-        if Ad_count:
-            return {"Advertisor": advertisor, "Advertisor Id": search["1"]["2"], "Ad Count": Ad_count, "Creative_Ids": self.creative_search_by_advertiser_id(advertiser_id=search["1"]["2"])}
-        return {"Advertisor": advertisor, "Advertisor Id":search["1"]["2"], "Ad Count": Ad_count, "Creative_Ids": []}
+        advertiser_id = search["1"]["2"]
+        ad_count = search['1']['4']['2']['2'] if search["1"].get("4") else 0
+
+        if ad_count:
+            creative_ids = self.creative_search_by_advertiser_id(advertiser_id, count)
+        else:
+            creative_ids = []
+
+        return {"Advertisor": advertisor, "Advertisor Id": advertiser_id, "Ad Count": ad_count, "Creative_Ids": creative_ids}
+
 
     def get_link_to_video(self, link: str) -> str:
         """Get the JS response from the link given and parse the Video/Image Link. Returns input Link if any error occurs"""
         response = requests.post(link)
         try:
             txt = next((x for x in response.text.split("CDATA[") if "googlevideo.com" in x))
             x = str(txt.split("]")[0]).encode("utf-8").decode("unicode_escape")
@@ -199,32 +234,37 @@
         except Exception:
             ad_title = ""
         return {"Ad Body":ad_body, "Ad Title": ad_title}
 
     def get_detailed_ad(self, advertisor_id: str, creative_id: str) -> dict:
         """Takes the Advertisor Id and Creative ID and returns the details of that particular Ad"""
         ad_detail = self.get_breif_ads(advertisor_id, creative_id)
-        response = self.reqs.get(
-            ad_detail["Ad Link"],
-        )
+        try:
+            response = self.reqs.get(ad_detail["Ad Link"])
+        except Exception:
+            response = "<html></html>"
+            ad_detail["Ad Link"] = "" # TODO check schema: False => add schema, check link: False => link = "" 
         ad_detail.update({"Ad Body":"", "Ad Title": "", "Image URL": "", "Video URL": ""})
         if ad_detail["Ad Format"] == "Text":
             ad_detail.update(self.parse_ad_link(response.text))
         elif ad_detail["Ad Format"] == "Image":
             ad_detail["Image URL"] = ad_detail["Ad Link"]
         else:
             ad_detail["Video URL"] = ad_detail["Ad Link"]
         return ad_detail
 
 if __name__ == '__main__':
     a = GoogleAds()
     keyword = "ibbedesign"
-    keyword = "Google"
-    print(a.get_advistisor_by_domain(keyword), end="\n\n")
-    creatives = a.get_creative_Ids(keyword)
+    keyword = "Google LLC"
+    #print(a.get_detailed_ad('AR05099026886533578753',"CR06021040984983339009"))
+    #exit(0)
+    #print(a.get_advistisor_by_domain(keyword), end="\n\n")
+    creatives = a.get_creative_Ids(keyword, 1000)
+    print(len(creatives["Creative_Ids"]))
     if creatives["Ad Count"]:
         advertisor_id = creatives["Advertisor Id"]
         for creative_id in creatives["Creative_Ids"]:
             #print(a.get_breif_ads(advertisor_id, creative_id))
             print(a.get_detailed_ad(advertisor_id,creative_id))
     else:
         print("Got nothing")
```

### Comparing `Google-Ads-Transparency-Scraper-1.5.8/GoogleAds/regions.py` & `Google-Ads-Transparency-Scraper-1.6.0/GoogleAds/regions.py`

 * *Files identical despite different names*

### Comparing `Google-Ads-Transparency-Scraper-1.5.8/Google_Ads_Transparency_Scraper.egg-info/PKG-INFO` & `Google-Ads-Transparency-Scraper-1.6.0/Google_Ads_Transparency_Scraper.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: Google-Ads-Transparency-Scraper
-Version: 1.5.8
+Version: 1.6.0
 Summary: A scraper for getting Ads from Google Ads Transparency
 Home-page: https://github.com/faniAhmed/GoogleAdsTransparencyScraper
-Download-URL: https://github.com/faniAhmed/GoogleAdsTransparencyScraper/archive/refs/tags/v1.5.8.tar.gz
+Download-URL: https://github.com/faniAhmed/GoogleAdsTransparencyScraper/archive/refs/tags/v1.6.0.tar.gz
 Author: Farhan Ahmed
 Author-email: jattfarhan10@gmail.com
 License: Securely Incorporation
 Keywords: Google,Transparency,Scraper,API,Google Ads,Ads,Google Transparency,Google Transparency Scraper,Google Ads Scraper
 Platform: any
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
```

### Comparing `Google-Ads-Transparency-Scraper-1.5.8/PKG-INFO` & `Google-Ads-Transparency-Scraper-1.6.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: Google-Ads-Transparency-Scraper
-Version: 1.5.8
+Version: 1.6.0
 Summary: A scraper for getting Ads from Google Ads Transparency
 Home-page: https://github.com/faniAhmed/GoogleAdsTransparencyScraper
-Download-URL: https://github.com/faniAhmed/GoogleAdsTransparencyScraper/archive/refs/tags/v1.5.8.tar.gz
+Download-URL: https://github.com/faniAhmed/GoogleAdsTransparencyScraper/archive/refs/tags/v1.6.0.tar.gz
 Author: Farhan Ahmed
 Author-email: jattfarhan10@gmail.com
 License: Securely Incorporation
 Keywords: Google,Transparency,Scraper,API,Google Ads,Ads,Google Transparency,Google Transparency Scraper,Google Ads Scraper
 Platform: any
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Environment :: Console
```

### Comparing `Google-Ads-Transparency-Scraper-1.5.8/README.md` & `Google-Ads-Transparency-Scraper-1.6.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -28,16 +28,16 @@
 from GoogleAds.main import GoogleAds, show_regions_list
 ```
 
 ###### Example Code:
 
 ```
     a = GoogleAds()
-    keyword = "Google"
-    creatives = a.get_creative_Ids(keyword)
+    keyword = "Google LLC"
+    creatives = a.get_creative_Ids(keyword, 200) # Get 200 creatives if available
     if creatives["Ad Count"]:
         advertisor_id = creatives["Advertisor Id"]
         for creative_id in creatives["Creative_Ids"]:
             #print(a.get_breif_ads(advertisor_id, creative_id))
             print(a.get_detailed_ad(advertisor_id,creative_id))
     else:
         print("Got nothing")
@@ -137,35 +137,35 @@
 ##### Get Adverstisor By Domain:
 
 Makes search of domain/url and returns the Company Name and It's Advertisor Id. The
 
 > {'Advertisor Id': 'AR14188379519798214657', 'Name': 'Google LLC'}
 
 ##### Get Creative Ids:
-
+Takes a keyword and a count argument. The count argument tells the number of creatives that need to be extracted
 Makes search for given keyword and gets the first Suggestion. Then gets the Creatives for that.
 
 Returns Advertisor Name, Id, Ad count and List of Creatives
 
 The following is the return format
 
 > {"Advertisor": "", "Advertisor Id":"", "Ad Count": 0, "Creatives": []}
 
 You call this method as follow
 
 ```
-Obj1.get_creative_Ids("Keyword")
+Obj1.get_creative_Ids("Keyword", 200) # count is 40 by default
 ```
 
 ##### Get Creatives by Advertisor Id:
 
 Get list of Creative Ids for given Advertisor Id
 
 ```
-Obj1.creative_search_by_advertiser_id("Advertisor Id")
+Obj1.creative_search_by_advertiser_id("Advertisor Id", 200) # count is 40 by default
 ```
 
 ##### Get Brief Ad Info:
 
 Takes the Advertisor Id and Creative ID and returns the breif info of that particular Ad
 
 ```
```

### Comparing `Google-Ads-Transparency-Scraper-1.5.8/setup.py` & `Google-Ads-Transparency-Scraper-1.6.0/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -2,17 +2,17 @@
 from setuptools import setup, find_packages
 setup(
     name="Google-Ads-Transparency-Scraper",
     author="Farhan Ahmed",
     author_email="jattfarhan10@gmail.com",
     url="https://github.com/faniAhmed/GoogleAdsTransparencyScraper",
     description="A scraper for getting Ads from Google Ads Transparency",
-    version="1.5.8",
+    version="1.6.0",
     packages=find_packages(),
-    download_url= 'https://github.com/faniAhmed/GoogleAdsTransparencyScraper/archive/refs/tags/v1.5.8.tar.gz',
+    download_url= 'https://github.com/faniAhmed/GoogleAdsTransparencyScraper/archive/refs/tags/v1.6.0.tar.gz',
     keywords= ['Google', 'Transparency', 'Scraper', 'API', 'Google Ads', 'Ads', 'Google Transparency', 'Google Transparency Scraper', 'Google Ads Scraper'],
     license='Securely Incorporation',
     install_requires=[
         "setuptools>=45.0",
         "beautifulsoup4>=4.12.2",
         "Requests>=2.31.0",
         "lxml>=4.6.3",
```

