# Comparing `tmp/neoscr-1.0.0.tar.gz` & `tmp/neoscr-2.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "neoscr-1.0.0.tar", last modified: Fri Mar 10 22:27:50 2023, max compression
+gzip compressed data, was "neoscr-2.0.0.tar", last modified: Sun Jul 23 20:53:54 2023, max compression
```

## Comparing `neoscr-1.0.0.tar` & `neoscr-2.0.0.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 joaonogueira   (501) staff       (20)        0 2023-03-10 22:27:50.261973 neoscr-1.0.0/
--rw-rw-r--   0 joaonogueira   (501) staff       (20)    11337 2023-01-20 02:50:04.000000 neoscr-1.0.0/LICENSE
--rw-rw-r--   0 joaonogueira   (501) staff       (20)      111 2023-01-20 02:50:04.000000 neoscr-1.0.0/MANIFEST.in
--rw-r--r--   0 joaonogueira   (501) staff       (20)     3736 2023-03-10 22:27:50.261826 neoscr-1.0.0/PKG-INFO
--rw-r--r--   0 joaonogueira   (501) staff       (20)     2942 2023-03-10 22:08:21.000000 neoscr-1.0.0/README.md
-drwxr-xr-x   0 joaonogueira   (501) staff       (20)        0 2023-03-10 22:27:50.260121 neoscr-1.0.0/neoscr/
--rw-r--r--   0 joaonogueira   (501) staff       (20)       22 2023-03-10 22:26:50.000000 neoscr-1.0.0/neoscr/__init__.py
--rw-r--r--   0 joaonogueira   (501) staff       (20)     2083 2023-03-10 22:26:50.000000 neoscr-1.0.0/neoscr/_modidx.py
--rw-r--r--   0 joaonogueira   (501) staff       (20)     2024 2023-03-10 22:26:50.000000 neoscr-1.0.0/neoscr/cli.py
--rw-r--r--   0 joaonogueira   (501) staff       (20)     4773 2023-03-10 22:26:50.000000 neoscr-1.0.0/neoscr/core.py
--rw-r--r--   0 joaonogueira   (501) staff       (20)      838 2023-03-10 22:26:50.000000 neoscr-1.0.0/neoscr/utils.py
-drwxr-xr-x   0 joaonogueira   (501) staff       (20)        0 2023-03-10 22:27:50.261561 neoscr-1.0.0/neoscr.egg-info/
--rw-r--r--   0 joaonogueira   (501) staff       (20)     3736 2023-03-10 22:27:50.000000 neoscr-1.0.0/neoscr.egg-info/PKG-INFO
--rw-r--r--   0 joaonogueira   (501) staff       (20)      344 2023-03-10 22:27:50.000000 neoscr-1.0.0/neoscr.egg-info/SOURCES.txt
--rw-r--r--   0 joaonogueira   (501) staff       (20)        1 2023-03-10 22:27:50.000000 neoscr-1.0.0/neoscr.egg-info/dependency_links.txt
--rw-r--r--   0 joaonogueira   (501) staff       (20)      173 2023-03-10 22:27:50.000000 neoscr-1.0.0/neoscr.egg-info/entry_points.txt
--rw-r--r--   0 joaonogueira   (501) staff       (20)        1 2023-03-10 22:07:48.000000 neoscr-1.0.0/neoscr.egg-info/not-zip-safe
--rw-r--r--   0 joaonogueira   (501) staff       (20)       46 2023-03-10 22:27:50.000000 neoscr-1.0.0/neoscr.egg-info/requires.txt
--rw-r--r--   0 joaonogueira   (501) staff       (20)        7 2023-03-10 22:27:50.000000 neoscr-1.0.0/neoscr.egg-info/top_level.txt
--rw-r--r--   0 joaonogueira   (501) staff       (20)      999 2023-03-10 22:24:23.000000 neoscr-1.0.0/settings.ini
--rw-r--r--   0 joaonogueira   (501) staff       (20)       38 2023-03-10 22:27:50.262019 neoscr-1.0.0/setup.cfg
--rw-rw-r--   0 joaonogueira   (501) staff       (20)     2560 2023-01-20 02:50:04.000000 neoscr-1.0.0/setup.py
+drwxr-xr-x   0 joaonogueira   (501) staff       (20)        0 2023-07-23 20:53:54.626762 neoscr-2.0.0/
+-rw-rw-r--   0 joaonogueira   (501) staff       (20)    11337 2023-01-20 02:50:04.000000 neoscr-2.0.0/LICENSE
+-rw-rw-r--   0 joaonogueira   (501) staff       (20)      111 2023-01-20 02:50:04.000000 neoscr-2.0.0/MANIFEST.in
+-rw-r--r--   0 joaonogueira   (501) staff       (20)     4039 2023-07-23 20:53:54.626615 neoscr-2.0.0/PKG-INFO
+-rw-r--r--   0 joaonogueira   (501) staff       (20)     3245 2023-07-23 20:45:11.000000 neoscr-2.0.0/README.md
+drwxr-xr-x   0 joaonogueira   (501) staff       (20)        0 2023-07-23 20:53:54.624801 neoscr-2.0.0/neoscr/
+-rw-r--r--   0 joaonogueira   (501) staff       (20)       22 2023-07-23 20:50:53.000000 neoscr-2.0.0/neoscr/__init__.py
+-rw-r--r--   0 joaonogueira   (501) staff       (20)     2083 2023-07-23 20:50:53.000000 neoscr-2.0.0/neoscr/_modidx.py
+-rw-r--r--   0 joaonogueira   (501) staff       (20)     2024 2023-07-23 20:50:53.000000 neoscr-2.0.0/neoscr/cli.py
+-rw-r--r--   0 joaonogueira   (501) staff       (20)     5965 2023-07-23 20:50:53.000000 neoscr-2.0.0/neoscr/core.py
+-rw-r--r--   0 joaonogueira   (501) staff       (20)      834 2023-07-23 20:50:53.000000 neoscr-2.0.0/neoscr/utils.py
+drwxr-xr-x   0 joaonogueira   (501) staff       (20)        0 2023-07-23 20:53:54.626386 neoscr-2.0.0/neoscr.egg-info/
+-rw-r--r--   0 joaonogueira   (501) staff       (20)     4039 2023-07-23 20:53:54.000000 neoscr-2.0.0/neoscr.egg-info/PKG-INFO
+-rw-r--r--   0 joaonogueira   (501) staff       (20)      344 2023-07-23 20:53:54.000000 neoscr-2.0.0/neoscr.egg-info/SOURCES.txt
+-rw-r--r--   0 joaonogueira   (501) staff       (20)        1 2023-07-23 20:53:54.000000 neoscr-2.0.0/neoscr.egg-info/dependency_links.txt
+-rw-r--r--   0 joaonogueira   (501) staff       (20)      173 2023-07-23 20:53:54.000000 neoscr-2.0.0/neoscr.egg-info/entry_points.txt
+-rw-r--r--   0 joaonogueira   (501) staff       (20)        1 2023-03-10 22:07:48.000000 neoscr-2.0.0/neoscr.egg-info/not-zip-safe
+-rw-r--r--   0 joaonogueira   (501) staff       (20)       46 2023-07-23 20:53:54.000000 neoscr-2.0.0/neoscr.egg-info/requires.txt
+-rw-r--r--   0 joaonogueira   (501) staff       (20)        7 2023-07-23 20:53:54.000000 neoscr-2.0.0/neoscr.egg-info/top_level.txt
+-rw-r--r--   0 joaonogueira   (501) staff       (20)      999 2023-07-23 20:46:56.000000 neoscr-2.0.0/settings.ini
+-rw-r--r--   0 joaonogueira   (501) staff       (20)       38 2023-07-23 20:53:54.626825 neoscr-2.0.0/setup.cfg
+-rw-rw-r--   0 joaonogueira   (501) staff       (20)     2560 2023-01-20 02:50:04.000000 neoscr-2.0.0/setup.py
```

### Comparing `neoscr-1.0.0/LICENSE` & `neoscr-2.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `neoscr-1.0.0/PKG-INFO` & `neoscr-2.0.0/README.md`

 * *Files 13% similar despite different names*

```diff
@@ -1,32 +1,8 @@
-Metadata-Version: 2.1
-Name: neoscr
-Version: 1.0.0
-Summary: Wrapper to query the SCR api
-Home-page: https://github.com/datarisk-io/neoscr
-Author: João Nogueira
-Author-email: joao.nogueira@datarisk.io
-License: Apache Software License 2.0
-Keywords: nbdev jupyter notebook python
-Platform: UNKNOWN
-Classifier: Development Status :: 4 - Beta
-Classifier: Intended Audience :: Developers
-Classifier: Natural Language :: English
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: License :: OSI Approved :: Apache Software License
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-Provides-Extra: dev
-License-File: LICENSE
-
-neoscr
-================
+# neoscr
 
 <!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! -->
 
 ## Install
 
 ``` sh
 pip install neoscr
@@ -47,43 +23,67 @@
     user=os.environ["SCR_USER"],
     password=os.environ["SCR_PASSWORD"],
     code=os.environ["SCR_CODE"],
     api_key=os.environ["SCR_API_KEY"]
 )
 ```
 
-``` python
-cpf = "000.000.000-00"
-ano_mes = "12_2022"
+<div>
 
-# retorna dois dataframes
-df_cpf_traduzido, df_cpf_modalidade = scr.get_cpf_data(cpf, ano_mes)
-```
+> **Warning**
+>
+> You should have the credentials to access the SCR API stored in your
+> OS environment variables.
+
+</div>
 
 ``` python
-cnpj = "00.000.000/0001-00"
-ano_mes = "12_2022"
+cpf = "867.168.046-09" # fake cpf
+ano = 2022
+mes = 12
 
 # retorna dois dataframes
-df_cnpj_traduzido, df_cnpj_modalidade = scr.get_cnpj_data(cnpj, ano_mes)
+df_cpf_traduzido, df_cpf_modalidade = scr.get_cpf_data(cpf, ano, mes)
 ```
 
-# CLI Interface
+<div>
 
-There is also a CLI interface to query SCR api from the command line.
+> **Note**
+>
+> `neoscr` will save each request made into `.neoscr` folder located at
+> your home directory.
+>
+> For the example above, the saved file will be:
+> `~/.neoscr/00000000000_2022_12.json`
 
-``` sh
-neoscr $SCR_USER $SCR_PASSWORD $SCR_CODE $SCR_API_KEY 000.000.000-00 12_2022 
+</div>
+
+``` python
+cnpj = "79.322.561/0001-67" # fake cnpj
+ano = 2022
+mes = 12
+
+# retorna dois dataframes
+df_cnpj_traduzido, df_cnpj_modalidade = scr.get_cnpj_data(cnpj, ano, mes)
 ```
 
 # Batch Query
 
 Execute the code below to query a list of cpfs or cnpjs (under
 modification) and download the data
 
+<div>
+
+> **Caution**
+>
+> Please don’t just copy and execute the code above. Read it and adapt
+> it to your needs.
+
+</div>
+
 ``` python
 import os
 import logging
 import pandas as pd
 from tqdm import tqdm
 
 from neoscr.utils import let_only_digits
@@ -108,18 +108,19 @@
 file_handler = logging.FileHandler('querylog.log')
 file_handler.setLevel(logging.DEBUG)
 
 # adicionando o file handler ao logger
 logger.addHandler(file_handler)
 
 # iterando sobre a lista de cpfs e enriquecendo
-ano_mes = "12_2022"
+ano = 2022
+mes = 12
 for cpf in tqdm(lista_de_cpfs):
     try:
-        df_traduzido, df_modalidade = scr.get_cpf_data(cpf, ano_mes)                               
+        df_traduzido, df_modalidade = scr.get_cpf_data(cpf, ano, mes)                               
         cpf_only_digits = let_only_digits(cpf)
         df_traduzido.to_csv(f"data/scr/raw/{cpf_only_digits}_traduzido.csv", index=False)
         df_modalidade.to_csv(f"data/scr/raw/{cpf_only_digits}_modalidade.csv", index=False)
     except:
         logger.error(f"Erro no CPF {cpf}")
         continue
 ```
@@ -137,9 +138,7 @@
 
 df_modalidade_full = pd.DataFrame()
 for file in os.listdir(".data/scr/raw"):
     if file.endswith("_modalidade.csv"):
         df_modalidade = pd.read_csv(f"data/scr/raw/{file}")
         df_modalidade_full = pd.concat([df_modalidade_full, df_modalidade])
 ```
-
-
```

### Comparing `neoscr-1.0.0/neoscr/_modidx.py` & `neoscr-2.0.0/neoscr/_modidx.py`

 * *Files identical despite different names*

### Comparing `neoscr-1.0.0/neoscr/cli.py` & `neoscr-2.0.0/neoscr/cli.py`

 * *Files identical despite different names*

### Comparing `neoscr-1.0.0/neoscr/core.py` & `neoscr-2.0.0/neoscr/core.py`

 * *Files 24% similar despite different names*

```diff
@@ -3,17 +3,21 @@
 # %% auto 0
 __all__ = ['ConsultaSCR']
 
 # %% ../nbs/00_core.ipynb 3
 import json
 import requests
 import pandas as pd
-from datetime import datetime
 from typing import Tuple
+from pathlib import Path
+from datetime import datetime
+
+from .utils import let_only_digits
 
+# %% ../nbs/00_core.ipynb 4
 class ConsultaSCR:
     def __init__(self, 
                  user: str,     # SCR user
                  password: str, # SCR password
                  code: str,     # SCR code
                  api_key: str   # SCR api key
     ):
@@ -33,77 +37,98 @@
             },
             "consulta": {
                 "Documento": "",
                 "DataBaseMes": "",
                 "DataBaseAno": ""
             }
         }
+
+        self.path_to_store_responses = Path.home() / '.neoscr'
+        self.path_to_store_responses.mkdir(parents=True, exist_ok=True)
         
     def _request(self, 
                  doc: str,    # CPF or CNPJ
-                 ano_mes: str # Year and month to be consulted. Format: MM_YYYY
+                 ano: int,    # Year to be consulted. Format: YYYY
+                 mes: int     # Month to be consulted. Format: MM
     ) -> requests.models.Response:
         "Make a request to the SCR API"
 
+        ano = str(ano)
+        mes = f"{mes:02d}"
         self.params["consulta"]["Documento"] = doc
-        self.params["consulta"]["DataBaseMes"] = ano_mes[:2]
-        self.params["consulta"]["DataBaseAno"] = ano_mes[3:]
-        response = requests.request("POST", self.url, data=json.dumps(self.params), headers=self.headers)
-        return response
+        self.params["consulta"]["DataBaseAno"] = ano
+        self.params["consulta"]["DataBaseMes"] = mes
+
+        # if the request was already made, just load the file from the local home storage folder .neoscr
+        response_filepath = self.path_to_store_responses / f"{let_only_digits(doc)}_{ano}_{mes}.json"
+        if response_filepath.exists():
+            print(f"File already exist, loading it from {response_filepath}")
+            with open(response_filepath) as json_file:
+                response_json = json.load(json_file)
+        else:
+            print(f"Making a request to SCR api ...")
+            response = requests.request("POST", self.url, data=json.dumps(self.params), headers=self.headers)
+            response_json = response.json()
+            print(f"Saving the response to the ~/.neoscr folder ...")
+            with open(response_filepath, 'w') as file:
+                json.dump(response_json, file)
+                print('Response saved successfully.')
+        return response_json
 
     def _get_resumo_cliente_traduzido(self, 
                                       response_json: dict, # Response from the SCR API 
                                       **kwargs: dict       # Keyword arguments
     ) -> pd.DataFrame:
         "Return a DataFrame with the translated client summary"
 
         df = pd.DataFrame(response_json.get("ResumoDoClienteTraduzido"), columns=response_json.get("ResumoDoClienteTraduzido").keys(), index = [0])
-        #df.insert(0, "doc", ''.join(filter(str.isdigit, kwargs.get("doc"))))
         df.insert(0, "doc", kwargs.get("doc"))
         df.insert(1, "data_consulta", kwargs.get("data_consulta"))
-        df.insert(2, "ano_mes", kwargs.get("ano_mes"))
+        df.insert(2, "mes_referencia", kwargs.get("mes_referencia"))
         df.insert(3, "msg", response_json.get("MensagemOperador"))
         return df
     
     def _get_resumo_modalidade(self, 
                                response_json: dict, # Response from the SCR API 
                                **kwargs: dict       # Keyword arguments
     ) -> pd.DataFrame:
         "Return a DataFrame with the modalities client summary"
 
         df = pd.DataFrame(response_json.get("ResumoModalidade"))
         df.insert(0, "doc", kwargs.get("doc"))
         df.insert(1, "data_consulta", kwargs.get("data_consulta"))
-        df.insert(2, "ano_mes", kwargs.get("ano_mes"))
+        df.insert(2, "mes_referencia", kwargs.get("mes_referencia"))
         return df
 
     def get_cpf_data(self, 
-                     cpf: str, # List of CPFs
-                     ano_mes: str,    # Year and month to be consulted. Format: MM_YYYY
+                     cpf: str,      # CPF
+                     ano: int,      # Year to be consulted. Ex: 2022
+                     mes: int       # Month to be consulted. Ex: 8, 10
     ) -> Tuple[pd.DataFrame, pd.DataFrame]:
         "Query CPFs and return a tuple of DataFrames: (df_cpf_resumo_cliente_traduzido, df_cpf_resumo_modalidade)"
         
-        data_consulta = datetime.today().strftime("%d_%m_%Y")
-        response_json = self._request(cpf, ano_mes).json()
+        data_consulta = datetime.today().strftime("%d/%m/%Y")
+        response_json = self._request(cpf, ano, mes)
         if response_json.get("Erro"):
             raise Exception(response_json.get("Msg").strip() + f": {cpf}")
         
-        df_traduzido = self._get_resumo_cliente_traduzido(response_json, doc=cpf, data_consulta=data_consulta, ano_mes=ano_mes)
-        df_modalidade = self._get_resumo_modalidade(response_json, doc=cpf, data_consulta=data_consulta, ano_mes=ano_mes)
+        df_traduzido = self._get_resumo_cliente_traduzido(response_json, doc=cpf, data_consulta=data_consulta, mes_referencia=f"{ano}{mes:02d}")
+        df_modalidade = self._get_resumo_modalidade(response_json, doc=cpf, data_consulta=data_consulta, mes_referencia=f"{ano}{mes:02d}")
         
         return df_traduzido, df_modalidade
 
     
     def get_cnpj_data(self, 
-                      cnpj: str, # List of CNPJs 
-                      ano_mes: str,     # Year and month to be consulted. Format: MM_YYYY
+                      cnpj: str,     # CNPJ
+                      ano: int,      # Year to be consulted. Ex: 2022
+                      mes: int       # Month to be consulted. Ex: 8, 10
     ) -> Tuple[pd.DataFrame, pd.DataFrame]:
         "Query CNPJs and return a tuple of DataFrames: (df_cnpj_resumo_cliente_traduzido, df_cnpj_resumo_modalidade)"
-        data_consulta = datetime.today().strftime("%d_%m_%Y")
-        response_json = self._request(cnpj, ano_mes).json()
+        data_consulta = datetime.today().strftime("%d/%m/%Y")
+        response_json = self._request(cnpj, ano, mes)
         if response_json.get("Erro"):
             raise Exception(response_json.get("Msg").strip() + f": {cnpj}")
         
-        df_traduzido = self._get_resumo_cliente_traduzido(response_json, doc=cnpj, data_consulta=data_consulta, ano_mes=ano_mes)
-        df_modalidade = self._get_resumo_modalidade(response_json, doc=cnpj, data_consulta=data_consulta, ano_mes=ano_mes)
+        df_traduzido = self._get_resumo_cliente_traduzido(response_json, doc=cnpj, data_consulta=data_consulta, mes_referencia=f"{ano}{mes:02d}")
+        df_modalidade = self._get_resumo_modalidade(response_json, doc=cnpj, data_consulta=data_consulta, mes_referencia=f"{ano}{mes:02d}")
 
         return df_traduzido, df_modalidade
```

### Comparing `neoscr-1.0.0/neoscr/utils.py` & `neoscr-2.0.0/neoscr/utils.py`

 * *Files 12% similar despite different names*

```diff
@@ -2,24 +2,23 @@
 
 # %% auto 0
 __all__ = ['let_only_digits', 'format_cnpj', 'format_cpf', 'fill_zeros']
 
 # %% ../nbs/02_utils.ipynb 2
 def let_only_digits(doc: str) -> str:
     """Remove all non-digit characters from a string"""
-    
     return ''.join(filter(str.isdigit, doc))
 
-# %% ../nbs/02_utils.ipynb 5
+# %% ../nbs/02_utils.ipynb 6
 def format_cnpj(cnpj: str) -> str:
     """Format a CNPJ string"""
     return cnpj[:2] + '.' + cnpj[2:5] + '.' + cnpj[5:8] + '/' + cnpj[8:12] + '-' + cnpj[12:]
 
-# %% ../nbs/02_utils.ipynb 7
+# %% ../nbs/02_utils.ipynb 8
 def format_cpf(cpf: str) -> str:
     """Format a CPF string"""
     return cpf[:3] + '.' + cpf[3:6] + '.' + cpf[6:9] + '-' + cpf[9:]
 
-# %% ../nbs/02_utils.ipynb 9
+# %% ../nbs/02_utils.ipynb 10
 def fill_zeros(doc: str, n: int) -> str:
     """Fill a string with zeros to the left with n characters"""
     return doc.zfill(n)
```

### Comparing `neoscr-1.0.0/neoscr.egg-info/PKG-INFO` & `neoscr-2.0.0/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: neoscr
-Version: 1.0.0
+Version: 2.0.0
 Summary: Wrapper to query the SCR api
 Home-page: https://github.com/datarisk-io/neoscr
 Author: João Nogueira
 Author-email: joao.nogueira@datarisk.io
 License: Apache Software License 2.0
 Keywords: nbdev jupyter notebook python
 Platform: UNKNOWN
@@ -17,16 +17,15 @@
 Classifier: Programming Language :: Python :: 3.10
 Classifier: License :: OSI Approved :: Apache Software License
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
-neoscr
-================
+# neoscr
 
 <!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! -->
 
 ## Install
 
 ``` sh
 pip install neoscr
@@ -47,43 +46,67 @@
     user=os.environ["SCR_USER"],
     password=os.environ["SCR_PASSWORD"],
     code=os.environ["SCR_CODE"],
     api_key=os.environ["SCR_API_KEY"]
 )
 ```
 
-``` python
-cpf = "000.000.000-00"
-ano_mes = "12_2022"
+<div>
 
-# retorna dois dataframes
-df_cpf_traduzido, df_cpf_modalidade = scr.get_cpf_data(cpf, ano_mes)
-```
+> **Warning**
+>
+> You should have the credentials to access the SCR API stored in your
+> OS environment variables.
+
+</div>
 
 ``` python
-cnpj = "00.000.000/0001-00"
-ano_mes = "12_2022"
+cpf = "867.168.046-09" # fake cpf
+ano = 2022
+mes = 12
 
 # retorna dois dataframes
-df_cnpj_traduzido, df_cnpj_modalidade = scr.get_cnpj_data(cnpj, ano_mes)
+df_cpf_traduzido, df_cpf_modalidade = scr.get_cpf_data(cpf, ano, mes)
 ```
 
-# CLI Interface
+<div>
 
-There is also a CLI interface to query SCR api from the command line.
+> **Note**
+>
+> `neoscr` will save each request made into `.neoscr` folder located at
+> your home directory.
+>
+> For the example above, the saved file will be:
+> `~/.neoscr/00000000000_2022_12.json`
 
-``` sh
-neoscr $SCR_USER $SCR_PASSWORD $SCR_CODE $SCR_API_KEY 000.000.000-00 12_2022 
+</div>
+
+``` python
+cnpj = "79.322.561/0001-67" # fake cnpj
+ano = 2022
+mes = 12
+
+# retorna dois dataframes
+df_cnpj_traduzido, df_cnpj_modalidade = scr.get_cnpj_data(cnpj, ano, mes)
 ```
 
 # Batch Query
 
 Execute the code below to query a list of cpfs or cnpjs (under
 modification) and download the data
 
+<div>
+
+> **Caution**
+>
+> Please don’t just copy and execute the code above. Read it and adapt
+> it to your needs.
+
+</div>
+
 ``` python
 import os
 import logging
 import pandas as pd
 from tqdm import tqdm
 
 from neoscr.utils import let_only_digits
@@ -108,18 +131,19 @@
 file_handler = logging.FileHandler('querylog.log')
 file_handler.setLevel(logging.DEBUG)
 
 # adicionando o file handler ao logger
 logger.addHandler(file_handler)
 
 # iterando sobre a lista de cpfs e enriquecendo
-ano_mes = "12_2022"
+ano = 2022
+mes = 12
 for cpf in tqdm(lista_de_cpfs):
     try:
-        df_traduzido, df_modalidade = scr.get_cpf_data(cpf, ano_mes)                               
+        df_traduzido, df_modalidade = scr.get_cpf_data(cpf, ano, mes)                               
         cpf_only_digits = let_only_digits(cpf)
         df_traduzido.to_csv(f"data/scr/raw/{cpf_only_digits}_traduzido.csv", index=False)
         df_modalidade.to_csv(f"data/scr/raw/{cpf_only_digits}_modalidade.csv", index=False)
     except:
         logger.error(f"Erro no CPF {cpf}")
         continue
 ```
```

### Comparing `neoscr-1.0.0/settings.ini` & `neoscr-2.0.0/settings.ini`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [DEFAULT]
 repo = neoscr
 lib_name = neoscr
-version = 1.0.0
+version = 2.0.0
 min_python = 3.7
 license = apache2
 black_formatting = False
 doc_path = _docs
 lib_path = neoscr
 nbs_path = nbs
 recursive = True
```

### Comparing `neoscr-1.0.0/setup.py` & `neoscr-2.0.0/setup.py`

 * *Files identical despite different names*

