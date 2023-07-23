# Comparing `tmp/starcatalogquery-0.1.8-py3-none-any.whl.zip` & `tmp/starcatalogquery-0.1.9-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,19 +1,19 @@
-Zip file size: 27770 bytes, number of entries: 17
+Zip file size: 27996 bytes, number of entries: 17
 -rw-r--r--  2.0 unx       33 b- defN 23-May-08 07:01 starcatalogquery/__init__.py
 -rw-r--r--  2.0 unx     6049 b- defN 23-Jun-18 09:44 starcatalogquery/catalog_check.py
 -rw-r--r--  2.0 unx     6727 b- defN 23-Jun-18 09:49 starcatalogquery/catalog_download.py
 -rw-r--r--  2.0 unx    16654 b- defN 23-Jul-03 08:08 starcatalogquery/catalog_query.py
--rw-r--r--  2.0 unx    51269 b- defN 23-Jun-19 23:39 starcatalogquery/classes.py
+-rw-r--r--  2.0 unx    50509 b- defN 23-Jul-22 14:15 starcatalogquery/classes.py
 -rw-r--r--  2.0 unx     3078 b- defN 23-May-12 08:00 starcatalogquery/invariantfeatures.py
 -rw-r--r--  2.0 unx     5684 b- defN 23-Jul-03 14:28 starcatalogquery/tiles_draw.py
 -rw-r--r--  2.0 unx     1978 b- defN 23-May-30 08:00 starcatalogquery/wcs.py
 -rw-r--r--  2.0 unx        1 b- defN 23-May-11 04:20 starcatalogquery/utils/__init__.py
 -rw-r--r--  2.0 unx      612 b- defN 23-May-09 08:08 starcatalogquery/utils/df2info.py
 -rw-r--r--  2.0 unx     4274 b- defN 23-Jun-18 09:43 starcatalogquery/utils/starcatalog_statistic.py
--rw-r--r--  2.0 unx      477 b- defN 23-May-09 08:06 starcatalogquery/utils/try_download.py
--rw-r--r--  2.0 unx     1068 b- defN 23-Jul-03 14:47 starcatalogquery-0.1.8.dist-info/LICENSE
--rw-r--r--  2.0 unx    12582 b- defN 23-Jul-03 14:47 starcatalogquery-0.1.8.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-03 14:47 starcatalogquery-0.1.8.dist-info/WHEEL
--rw-r--r--  2.0 unx       17 b- defN 23-Jul-03 14:47 starcatalogquery-0.1.8.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1510 b- defN 23-Jul-03 14:47 starcatalogquery-0.1.8.dist-info/RECORD
-17 files, 112105 bytes uncompressed, 25250 bytes compressed:  77.5%
+-rw-r--r--  2.0 unx      467 b- defN 23-Jul-21 14:41 starcatalogquery/utils/try_download.py
+-rw-r--r--  2.0 unx     1068 b- defN 23-Jul-22 14:26 starcatalogquery-0.1.9.dist-info/LICENSE
+-rw-r--r--  2.0 unx    12920 b- defN 23-Jul-22 14:26 starcatalogquery-0.1.9.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-22 14:26 starcatalogquery-0.1.9.dist-info/WHEEL
+-rw-r--r--  2.0 unx       17 b- defN 23-Jul-22 14:26 starcatalogquery-0.1.9.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx     1510 b- defN 23-Jul-22 14:26 starcatalogquery-0.1.9.dist-info/RECORD
+17 files, 111673 bytes uncompressed, 25476 bytes compressed:  77.2%
```

## zipnote {}

```diff
@@ -30,23 +30,23 @@
 
 Filename: starcatalogquery/utils/starcatalog_statistic.py
 Comment: 
 
 Filename: starcatalogquery/utils/try_download.py
 Comment: 
 
-Filename: starcatalogquery-0.1.8.dist-info/LICENSE
+Filename: starcatalogquery-0.1.9.dist-info/LICENSE
 Comment: 
 
-Filename: starcatalogquery-0.1.8.dist-info/METADATA
+Filename: starcatalogquery-0.1.9.dist-info/METADATA
 Comment: 
 
-Filename: starcatalogquery-0.1.8.dist-info/WHEEL
+Filename: starcatalogquery-0.1.9.dist-info/WHEEL
 Comment: 
 
-Filename: starcatalogquery-0.1.8.dist-info/top_level.txt
+Filename: starcatalogquery-0.1.9.dist-info/top_level.txt
 Comment: 
 
-Filename: starcatalogquery-0.1.8.dist-info/RECORD
+Filename: starcatalogquery-0.1.9.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## starcatalogquery/classes.py

```diff
@@ -18,25 +18,23 @@
 from .wcs import xy_catalog
 from .invariantfeatures import _generate_invariants
 
 class StarCatalog(object):
 
     def get(sc_name,tile_size=None,dir_to=None):
         """
-        Grab star catalog data files from a remote server.
+        Grab star catalog data files from remote servers.
 
         Usage:
             >>> from starcatalogquery import StarCatalog
-            >>> gaiadr3_raw = StarCatalog.get('gaiadr3',2)
-
+            >>> hygv35_raw = StarCatalog.get('hygv35',5)
         Inputs:
-            sc_name -> [str] Name of the starcatalog to download. Available starcatalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
-            tile_size -> [int,optinal,default=None] size of the tile in [deg]. If None, the size of the tile is automatically assigned a feasible maximum according to the name of the star catalog.
-            dir_to -> [str,optional,default=None] The download path of the star catalog files. If None, the path is automatically assigned to a suitable directory by default.
-
+            sc_name -> [str] Name of the star catalog. Available options include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
+            tile_size -> [int,optinal,default=None] Geometric size of the tile in [deg]. If None, it is assigned an allowed maximum automatically based on the star catalog.
+            dir_to -> [str,optional,default=None] Path of the star catalog files grabbed. If None, the it is assigned to a build-in directory by default.
         Outputs:
             Instance of class StarCatalogRaw
         """
         if sc_name == 'hygv35': # for HYG v35 star catalog
             dir_to,dir_size,file_num,validity,tile_size = hygv35_download(tile_size,dir_to) 
 
         else: # for other star catalogs
@@ -61,67 +59,65 @@
 
     def load(dir_from=None):
         """
         Load the star catalog files from the local database.
 
         Usage:
             >>> from starcatalogquery import StarCatalog
-            >>> # load the raw star catalog GAIADR3
-            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalog/raw/gaiadr3/res2/'
-            >>> gaiadr3_raw = StarCatalog.load(dir_from_raw)
+            >>> # load the raw star catalog HYGv3.5
+            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalogs/raw/hygv35/res5/'
+            >>> hygv35_raw = StarCatalog.load(dir_from_raw)
             >>>
-            >>> # load the reduced star catalog GAIADR3
-            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalog/reduced/gaiadr3/res2/'
-            >>> gaiadr3_reduced = StarCatalog.load(dir_from_reduced)
+            >>> # load the reduced star catalog HYGv3.5
+            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalogs/reduced/hygv35/res5/'
+            >>> hygv35_reduced = StarCatalog.load(dir_from_reduced)
             >>>
-            >>> # load the simplified star catalog GAIADR3
-            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalog/simplified/gaiadr3/res2/mag8.0/epoch2023.0/'
-            >>> gaiadr3_simplified = StarCatalog.load(dir_from_simplified)
+            >>> # load the simplified star catalog HYGv3.5
+            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
+            >>> hygv35_simplified = StarCatalog.load(dir_from_simplified)
         Inputs:
-            dir_from -> [str,optional,default=None] The loading path of the star catalog files. If None, the path is automatically assigned to a suitable directory by default.
+            dir_from -> [str,optional,default=None] Directory of the star catalog files. If None, it is assigned to a build-in directory by default.
         Outputs:
             Instance of class StarCatalog
         """
         _mode,sc_name,tile_size = dir_from.split('starcatalogs/')[1].split('/')[:3]
         tile_size = int(tile_size[3:])
 
-        # _mode -> [str] Types of star catalogs, including 'raw', 'reduced', 'simplified', where
-        # 'raw' represents the original star catalog, which contains all information about the star
-        # 'reduced' represents the reduced star catalog, which contains the position, proper motion, apparent magnitude, epoch of the star
-        # 'simplified' represents the minimalist star catalog, which only includes the position and apparent magnitude of stars at a specific epoch
-        # sc_name -> [str] Name of the starcatalog. Available starcatalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
-        # tile_size -> [int] Size of the tile in [deg]
+        # _mode -> [str] Type of the star catalog. Available options include 'raw', 'reduced', 'simplified', where
+        # 'raw' represents the original star catalog, which covers all information about the stars,
+        # 'reduced' represents the reduced star catalog, which contains the position, proper motion, apparent magnitude, epoch of the stars,
+        # 'simplified' represents the minimalist star catalog, which only includes the position and apparent magnitude of the stars at a specific epoch.
+        # sc_name -> [str] Name of the star catalog. Available options include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
+        # tile_size -> [int] Geometric size of the tile in [deg]
 
         if _mode == 'raw':
             starcatalog = StarCatalogRaw.load(sc_name,tile_size,dir_from)
         elif _mode == 'reduced':
             starcatalog = StarCatalogReduced.load(sc_name,tile_size,dir_from)
         elif _mode == 'simplified':    
-            mag_cutoff,epoch = np.array(dir_from.split('mag')[1][:-1].split('/epoch'),dtype=float) 
-            starcatalog = StarCatalogSimplified.load(sc_name,tile_size,mag_cutoff,epoch,dir_from)
+            mag_threshold,epoch = np.array(dir_from.split('mag')[1][:-1].split('/epoch'),dtype=float) 
+            starcatalog = StarCatalogSimplified.load(sc_name,tile_size,mag_threshold,epoch,dir_from)
 
         return starcatalog 
 
     def read_h5_indices(infile):
         """
-        Read in h5-formatted star catalog file, which records the center pointing of each sky area, the pixel coordinates of the stars, the triangle invariants and the asterism indices.
+        Read and parse the h5-formatted star catalog indicea file, which records the center pointing, pixel coordinates of the stars, triangle invariants and asterism indices of each sky area.
 
         Usage:
             >>> from starcatalogquery import StarCatalog
-            >>> infile_h5 = 'starcatalogs/indices/hygv35/fov20_mag8_mcp40_2023.0.h5'
+            >>> infile_h5 = 'starcatalogs/indices/hygv35/k2_mag9.0_mcp30_2022.0.h5'
             >>> fp_radecs,stars_xy,stars_invariants,stars_asterisms = read_h5_indices(infile_h5)
-        
         Inputs:
-            infile_h5 -> [str] h5-formatted star catalog file  
-
+            infile_h5 -> [str] h5-formatted star catalog indices file  
         Outputs:
-            fp_radecs -> [2d array of float] The center pointing of each sky area in format of [[RA0,DEC0],..[RAn,DECn]] in [deg]
-            stars_xy -> [list of 2d array of float] The pixel coordinates of the stars in each sky area
-            stars_invariants -> [list of 2d array of float] The triangle invariants in each sky area
-            stars_asterisms -> [list of 2d array of int] The asterism indices corresponding to the triangle invariants in each sky area       
+            fp_radecs -> [2d array of float] Center pointing of each sky area in form of [[RA0,DEC0],..[RAn,DECn]] in [deg]
+            stars_xy -> [list of 2d array] Pixel coordinates of stars in each sky area
+            stars_invariants -> [list of 2d array] Triangle invariants in each sky area
+            stars_asterisms -> [list of 2d array] Asterism indices corresponding to the triangle invariants in each sky area       
         """
         fin = h5py.File(infile,'r')
 
         # read data
         fp_radecs = fin['fp_radecs'][:]
         stars_xy,stars_invariants, stars_asterisms = [],[],[]
         for j in range(len(fp_radecs)):
@@ -134,33 +130,32 @@
         return fp_radecs,stars_xy,stars_invariants,stars_asterisms  
 
 class StarCatalogRaw(object):
     """
     Class StarCatalogRaw
 
     Attributes:
-        - tiles_path: Path of the starcatalog tile files. 
-        - sc_size: The size of the star catalog.
+        - tiles_path: Path of the star catalog files. 
         - tiles_num: Total number of the tile files.
-        - validity: The validity of the star catalog.
-        - sc_name: Name of the starcatalog. Available starcatalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
-        - tile_size: Size of the tile in [deg]
-        - _mode: Types of star catalogs, including 'raw', 'reduced', 'simplified', where
-            'raw' represents the original star catalog, which contains all information about the star
-            'reduced' represents the reduced star catalog, which contains the position, proper motion, apparent magnitude, epoch of the star
-            'simplified' represents the minimalist star catalog, which only includes the position and apparent magnitude of stars
+        - tile_size: Geometric size of the tile in [deg]
+        - sc_size: File size of the star catalog.
+        - validity: Validity of the star catalog.
+        - sc_name: Name of the star catalog. Available options include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
+        - _mode: Type of the star catalog. Available options include 'raw', 'reduced', 'simplified', where
+            'raw' represents the original star catalog, which covers all information about the stars,
+            'reduced' represents the reduced star catalog, which contains the position, proper motion, apparent magnitude, epoch of the stars,
+            'simplified' represents the minimalist star catalog, which only includes the position and apparent magnitude of the stars at a specific epoch.
         - stars_num: Total number of stars in the catalog
-        - mag: Apparent magnitude of stars in the catalog
+        - mag: Range of apparent magnitudes for the catalog
         - description: Catalog Summary
-
     Methods:
         - load: Load the raw star catalog files from the local database.
-        - reduce: Reduce the original star catalog so that the reduced star catalog only contains necessary information such as the position, proper motion, apparent magnitude, epoch, etc.
-        - search_box: Perform a rectangle search of stars on the raw star catalog and return an instance of class Stars.
-        - search_cone: Perform a cone search of stars on the raw star catalog and return an instance of class Stars.   
+        - reduce: Reduce the raw star catalog so that it only contains necessary information of stars such as the celestial position, proper motion, apparent magnitude, and epoch, etc.
+        - search_box: Perform a rectangle search on the raw star catalog.
+        - search_cone: Perform a cone search on the raw star catalog.
         - _search_draw: Visualize the scope of the search area and the coverage of the corresponding tiles.    
     """   
     def __init__(self,info):  
 
         self.info = info
 
         for key in info.keys():
@@ -172,23 +167,21 @@
 
     def load(sc_name,tile_size,dir_from=None):
         """
         Load the raw star catalog files from the local database.
 
         Usage:
             >>> from starcatalogquery import StarCatalogRaw
-            >>> # load the raw star catalog GAIADR3
-            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalog/raw/gaiadr3/res2/'
-            >>> gaiadr3_raw = StarCatalogRaw.load('raw','gaiadr3',2,dir_from_raw)
-
-        Inputs:
-            sc_name -> [str] Name of the starcatalog. Available starcatalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
-            tile_size -> [int] Size of the tile in [deg]
-            dir_from -> [str,optional,default=None] The loading path of the star catalog files. If None, the path is automatically assigned to a suitable directory by default.
-
+            >>> # load the raw star catalog HYGv3.5
+            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalogs/raw/hygv35/res5/'
+            >>> hygv35_raw = StarCatalogRaw.load('hygv35',5,dir_from_raw)
+        Inputs:
+            sc_name -> [str] Name of the star catalog. Available options include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
+            tile_size -> [int] Geometric size of the tile in [deg]
+            dir_from -> [str,optional,default=None] Directory of the star catalog files. If None, it is assigned to a build-in directory by default.
         Outputs:
             Instance of class StarCatalogRaw
         """
         if dir_from is None: dir_from = 'starcatalogs/raw/{:s}/res{:d}/'.format(sc_name,tile_size)    
         if not os.path.exists(dir_from): raise Error('The storage directory for the catalog {:s} does not exist.'.format(sc_name))  
 
         # calculate total size and numbers of tile files    
@@ -199,25 +192,23 @@
         dict_keys = 'tiles_path','sc_size','tiles_num','validity','sc_name','tile_size','_mode','stars_num','mag','description'
         info = dict(zip(dict_keys, dict_values))
 
         return StarCatalogRaw(info) 
 
     def reduce(self,dir_reduced=None):
         """
-        Reduce the original star catalog so that the reduced star catalog only contains necessary information such as the position, proper motion, apparent magnitude, epoch, etc.
+        Reduce the raw star catalog so that it only contains necessary information of stars such as the celestial position, proper motion, apparent magnitude, and epoch, etc.
 
         Usage:
             >>> from starcatalogquery import StarCatalogRaw
-            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalog/raw/gaiadr3/res2/'
-            >>> gaiadr3_raw = StarCatalogRaw.load('raw','gaiadr3',2,dir_from_raw)
-            >>> gaiadr3_reduced = gaiadr3_raw.reduce()
-
+            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalogs/raw/hygv35/res5/'
+            >>> hygv35_raw = StarCatalogRaw.load('hygv35',5,dir_from_raw)
+            >>> hygv35_reduced = hygv35_raw.reduce()
         Inputs:
-            dir_reduced -> [str,optional,default=None] The path of the reduced star catalog files to store. If None, the path is automatically assigned to a suitable directory by default.
-
+            dir_reduced -> [str,optional,default=None] Directory of the reduced star catalog files. If None, it is assigned to a build-in directory by default.
         Outputs:
             Instance of class StarCatalogReduced       
         """
         info = self.info.copy()
         tile_size = int(self.tile_size.split(' ')[0])
         tiles_path = self.tiles_path
         if dir_reduced is None:
@@ -229,131 +220,117 @@
         print('Reducing the star catalog {:s}, which may take a considerable amount of time'.format(sc_name))  
 
         if sc_name == 'hygv35':
             j = 1
             for tile_file in file_list:
                 desc = 'Reducing {:s}{:d}{:s} of {:d}'.format(Fore.BLUE,j,Fore.RESET,self.tiles_num)
                 print(desc,end='\r')
-
                 df = pd.read_csv(tile_file,skiprows=1,dtype=str)
                 # units: ra->hourangle, dec->deg, pmra->mas/a, pmdec->mas/a, epoch->2000.0 
                 df_reduced = df.loc[:,['ra','dec','pmra','pmdec','mag']]
                 df_reduced['epoch'] = '2000.0'
                 df_reduced['ra'] = (df_reduced['ra'].astype(float)*15).round(6) # Convert hourangle to deg
                 df_reduced.to_csv(tile_file.replace('raw','reduced'),index=False)
-
                 j += 1
         elif sc_name == 'gsc12':
             j = 1
             for tile_file in file_list:
                 desc = 'Reducing {:s}{:d}{:s} of {:d}'.format(Fore.BLUE,j,Fore.RESET,self.tiles_num)
                 print(desc,end='\r')
-
                 df = pd.read_csv(tile_file,skiprows=1,dtype=str)
                 # units: ra->deg, dec->deg, RApm->arcs/0.1a, Decpm->arcs/0.1a, Epoch->1980.552
                 df_reduced = df.loc[:,['ra','dec','RApm','Decpm','mag','Epoch']]
                 columns_dict = {'RApm':'pmra', 'Decpm':'pmdec', 'Epoch':'epoch'}
                 df_reduced.rename(columns=columns_dict, inplace=True)
                 # Convert to standard proper motion in mas/a
                 df_reduced['pmra'] = (df_reduced['pmra'].astype(float)*1e4).round(2) 
                 df_reduced['pmdec'] = (df_reduced['pmdec'].astype(float)*1e4).round(2)
                 df_reduced.to_csv(tile_file.replace('raw','reduced'),index=False)
-
                 j += 1
         elif sc_name == 'gsc242':
             j = 1
             for tile_file in file_list:
                 desc = 'Reducing {:s}{:d}{:s} of {:d}'.format(Fore.BLUE,j,Fore.RESET,self.tiles_num)
                 print(desc,end='\r')
-
                 df = pd.read_csv(tile_file,skiprows=1,dtype=str)
                 # units: ra->deg, dec->deg, rapm->mas/a, decpm->mas/a, epoch->2012
                 df_reduced = df.loc[:,['ra','dec','rapm','decpm','mag','epoch']]
                 columns_dict = {'rapm':'pmra', 'decpm':'pmdec'}
                 df_reduced.rename(columns=columns_dict, inplace=True)
                 df_reduced.to_csv(tile_file.replace('raw','reduced'),index=False)  
-
                 j += 1
         elif sc_name == 'gaiadr3':
             for tile_file in file_list:
                 df = pd.read_csv(tile_file,skiprows=1,dtype=str)
                 # units: ra->deg, dec->deg, pmra->mas/a, pmdec->mas/a, epoch->2016
                 df_reduced = df.loc[:,['ra','dec','pmra','pmdec','mag','epoch']]
                 df_reduced.to_csv(tile_file.replace('raw','reduced'),index=False)           
         elif sc_name == 'ucac5':
             j = 1
             for tile_file in file_list:
                 desc = 'Reducing {:s}{:d}{:s} of {:d}'.format(Fore.BLUE,j,Fore.RESET,self.tiles_num)
                 print(desc,end='\r')
-
                 df = pd.read_csv(tile_file,skiprows=1,dtype=str)
                 # units: ra->deg, dec->deg, pmur->mas/a, pmud->mas/a, epu->1998.754
                 df_reduced = df.loc[:,['ra','dec','pmur','pmud','mag','epu']]
                 columns_dict = {'pmur':'pmra', 'pmud':'pmdec','epu':'epoch'}
                 df_reduced.rename(columns=columns_dict, inplace=True)
                 df_reduced.to_csv(tile_file.replace('raw','reduced'),index=False)   
-
                 j += 1 
         elif sc_name == 'usnob':
             j = 1
             for tile_file in file_list:
                 desc = 'Reducing {:s}{:d}{:s} of {:d}'.format(Fore.BLUE,j,Fore.RESET,self.tiles_num)
                 print(desc,end='\r')
-
                 df = pd.read_csv(tile_file,skiprows=1,dtype=str)
                 # units: ra->deg, dec->deg, pmRA->mas/a, pmDEC->mas/a, Epoch->1950,mag->unknown
                 df_reduced = df.loc[:,['ra','dec','pmRA','pmDEC','mag','Epoch']]
                 columns_dict = {'pmRA':'pmra', 'pmDEC':'pmdec','Epoch':'epoch'}
                 df_reduced.rename(columns=columns_dict, inplace=True)
                 df_reduced.to_csv(tile_file.replace('raw','reduced'),index=False)  
-
                 j += 1
         elif sc_name == '2mass':
             j = 1
             for tile_file in file_list:
                 desc = 'Reducing {:s}{:d}{:s} of {:d}'.format(Fore.BLUE,j,Fore.RESET,self.tiles_num)
                 print(desc,end='\r')
-
                 df = pd.read_csv(tile_file,skiprows=1,dtype=str)
                 # units: ra->deg, dec->deg, jdate->2451063.6417
                 df_reduced = df.loc[:,['ra','dec','mag']]
                 df_reduced['epoch'] = Time(df['jdate'].astype(float), format='jd').jyear.round(2) 
                 df_reduced.to_csv(tile_file.replace('raw','reduced'),index=False)  
-
                 j += 1
 
         print('\nFinished')                                                   
                     
         file_num,dir_size,validity = tiles_statistic(dir_reduced,tile_size)  
         info['_mode'] = 'reduced'
         info['tiles_path'] = dir_reduced
         info['sc_size'] = dir_size
 
         return StarCatalogReduced(info)  
     
-    def search_box(self,radec_box,mag_threshold,t_pm,max_control_points=None):
+    def search_box(self,radec_box,mag_threshold,t_pm,max_num=None):
         """
-        Perform a rectangle search of stars on the raw star catalog and return an instance of class Stars.
+        Perform a rectangle search of stars on raw star catalogs.
 
         Usage:
             >>> from starcatalogquery import StarCatalogRaw
-            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalog/raw/gaiadr3/res2/'
-            >>> gaiadr3_raw = StarCatalogRaw.load('raw','gaiadr3',2,dir_from_raw)
-            >>> stars = gaiadr3_raw.search_box([20,30,30,40],8,2023.0)
-
+            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalogs/raw/hygv35/res5/'
+            >>> hygv35_raw = StarCatalogRaw.load('hygv35',5,dir_from_raw)
+            >>> stars = hygv35_raw.search_box([20,30,30,40],9,2022.0)
         Inputs:
-            radec_box -> [int,array_like] Rectangular search area in format of [ra_min,dec_min,ra_max,dec_max], where
+            radec_box -> [list] Rectangular search area in form of [ra_min,dec_min,ra_max,dec_max], where
                 ra_min -> [float] Left border of RA in [deg].
                 dec_min -> [float] Lower border of DEC in [deg].
                 ra_max -> [float] Right border of RA in [deg].
                 dec_max -> [float] Upper border of DEC in [deg].
-            mag_threshold -> [float] Apparent magnitude limit of the detector  
-            t_pm -> [float] The epoch when the search was performed
-            max_control_points -> [int,optional,default=None] Number of brightest stars in the search area. If None, it is the number of all stars in the search area by deault.
-
+            mag_threshold -> [float] Apparent magnitude limit  
+            t_pm -> [float] Epoch to which the stars are unified
+            max_num -> [int,optional,default=None] Maxinum number of the stars sorted by brightness for rectangle search. If None, all stars are counted in the search area by deault.
         Outputs:
             Instance of class Stars
         """
         ra_min,dec_min,ra_max,dec_max = radec_box
         tile_size = int(self.tile_size.split()[0])
         sc_path,sc_name = self.tiles_path,self.sc_name
         sc_indices = box2seqs(radec_box,tile_size) 
@@ -389,15 +366,15 @@
             df[['ra','dec','pmra','pmdec','mag','epoch']] = df[['ra', 'dec','pmra','pmdec','mag','epoch']].apply(pd.to_numeric)
         else:    
             df[['ra','dec','mag','epoch']] = df[['ra','dec','mag','epoch']].apply(pd.to_numeric)
 
         mag_flag = (df['mag'] < mag_threshold)
         df = df[mag_flag].sort_values(by=['mag'])
 
-        # calculate proper motion
+        # calculate the proper motion
         dt = float(t_pm) - df['epoch']
 
         if {'pmra', 'pmdec'}.issubset(df.columns):    
             df['ra'] +=  df['pmra']/3.6e6 * dt   
             df['dec'] += df['pmdec']/3.6e6 * dt
         else:
             warnings.warn('Proper motion data for stars in catalog {:s} are not found.'.format(sc_name))
@@ -407,36 +384,34 @@
         dec_flag = np.abs(dec- (dec_min + dec_max)/2) < (dec_max - dec_min)/2
 
         flag = ra_flag & dec_flag 
         df = df[flag]
         df['epoch'] = t_pm
         df.reset_index(drop=True,inplace=True)
 
-        info = df2info(self.sc_name,center,df,max_control_points) 
+        info = df2info(self.sc_name,center,df,max_num) 
         return Stars(info)
 
-    def search_cone(self,center,radius,mag_threshold,t_pm,max_control_points=None):
+    def search_cone(self,center,radius,mag_threshold,t_pm,max_num=None):
         """
-        Perform a cone search of stars on the raw star catalog and return an instance of class Stars.
+        Perform a cone search of stars on raw star catalogs.
 
         Usage:
             >>> from starcatalogquery import StarCatalogRaw
-            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalog/raw/gaiadr3/res2/'
-            >>> gaiadr3_raw = StarCatalogRaw.load('raw','gaiadr3',2,dir_from_raw)
-            >>> stars = gaiadr3_raw.search_cone([20,30],10,8,2023.0)
-
-        Inputs:
-            center -> [int,array_like] Center of the cap in format of [ra_c,dec_c], where
-                ra_c -> [float] RA, in [deg].
-                dec_c -> [float] DEC, in [deg].
-            radius -> [float] Angular radius of the cap, in [deg].
-            mag_threshold -> [float] Apparent magnitude limit of the detector  
-            t_pm -> [float] The epoch when the search was performed
-            max_control_points -> [int,optional,default=None] Number of brightest stars in the search area. If None, it is the number of all stars in the search area by deault.
-
+            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalogs/raw/hygv35/res5/'
+            >>> hygv35_raw = StarCatalogRaw.load('hygv35',5,dir_from_raw)
+            >>> stars = hygv35_raw.search_cone([20,30],10,9,2022.0)
+        Inputs:
+            center -> [list] Center of the cone in form of [ra_c,dec_c], where
+                ra_c -> [float] RA, in [deg]
+                dec_c -> [float] DEC, in [deg]
+            radius -> [float] Angular radius of the cone, in [deg]
+            mag_threshold -> [float] Apparent magnitude limit
+            t_pm -> [float] Epoch to which the stars are unified
+            max_num -> [int,optional,default=None] Maximum mumber of stars sorted by brightness for cone search. If None, all stars are counted in the search area by deault.
         Outputs:
             Instance of class Stars
         """
         ra_c,dec_c = center
         tile_size = int(self.tile_size.split()[0])
         sc_path,sc_name = self.tiles_path,self.sc_name
         sc_indices = cone2seqs(ra_c,dec_c,radius,tile_size) 
@@ -472,15 +447,15 @@
             df[['ra','dec','pmra','pmdec','mag','epoch']] = df[['ra', 'dec','pmra','pmdec','mag','epoch']].apply(pd.to_numeric)
         else:    
             df[['ra','dec','mag','epoch']] = df[['ra','dec','mag','epoch']].apply(pd.to_numeric)
 
         mag_flag = (df['mag'] < mag_threshold)
         df = df[mag_flag].sort_values(by=['mag'])
 
-        # calculate proper motion
+        # calculate the proper motion
         dt = float(t_pm) - df['epoch']
 
         if {'pmra', 'pmdec'}.issubset(df.columns):    
             df['ra'] +=  df['pmra']/3.6e6 * dt   
             df['dec'] += df['pmdec']/3.6e6 * dt
         else:
             warnings.warn('Proper motion data for stars in catalog {:s} are not found.'.format(sc_name))
@@ -491,71 +466,68 @@
         sep = c1.separation(c2).deg
 
         flag = sep < radius 
         df = df[flag]
         df['epoch'] = t_pm
         df.reset_index(drop=True,inplace=True)   
 
-        info = df2info(self.sc_name,center,df,max_control_points) 
+        info = df2info(self.sc_name,center,df,max_num) 
         return Stars(info)
 
     def _search_draw(self,search_area):
         """
         Visualize the scope of the search area and the coverage of the corresponding tiles.
 
         Usage:
             >>> from starcatalogquery import StarCatalogRaw
-            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalog/raw/gaiadr3/res2/'
-            >>> gaiadr3_raw = StarCatalogRaw.load('raw','gaiadr3',2,dir_from_raw)
+            >>> dir_from_raw = '/Volumes/TOSHIBA/starcatalogs/raw/hygv35/res5/'
+            >>> hygv35_raw = StarCatalogRaw.load('hygv35',5,dir_from_raw)
             >>> cone_area = {'cone':[20,30,10]}
-            >>> stars = gaiadr3_raw._search_draw(cone_area)
-
+            >>> stars = hygv35_raw._search_draw(cone_area)
         Inputs:
-            search_area -> [dict] The scope of the search area, such as {'cone':[20,30,10]} or {'box':[20,30,30,40]}, where
+            search_area -> [dict] Scope of the search area, such as {'cone':[20,30,10]} or {'box':[20,30,30,40]}, where
             for {'box':[ra_min,dec_min,ra_max,dec_max]}:
                 ra_min -> [float] Left border of RA in [deg].
                 dec_min -> [float] Lower border of DEC in [deg].
                 ra_max -> [float] Right border of RA in [deg].
                 dec_max -> [float] Upper border of DEC in [deg].
             for {'cone':[ra_c,dec_c,radius]}:
                 ra_c -> [float] RA, in [deg].
                 dec_c -> [float] DEC, in [deg].
                 radius -> [float] Angular radius of the cap, in [deg].  
-
         Outputs:
-            An image that shows the scope of the search area and the coverage of the corresponding tiles.          
+            An image sketching the scope of the search area and the coverage of the corresponding tiles.          
         """
         tile_size = int(self.tile_size.split()[0]) 
         search_draw(tile_size,search_area)       
 
 class StarCatalogReduced(object):
     """
     Class StarCatalogReduced
 
     Attributes:
-        - tiles_path: Path of the starcatalog tile files. 
-        - sc_size: The size of the star catalog.
+        - tiles_path: Path of the star catalog files. 
         - tiles_num: Total number of the tile files.
-        - validity: The validity of the star catalog.
-        - sc_name: Name of the starcatalog. Available starcatalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
-        - tile_size: Size of the tile in [deg]
-        - _mode: Types of star catalogs, including 'raw', 'reduced', 'simplified', where
-            'raw' represents the original star catalog, which contains all information about the star
-            'reduced' represents the reduced star catalog, which contains the position, proper motion, apparent magnitude, epoch of the star
-            'simplified' represents the minimalist star catalog, which only includes the position and apparent magnitude of stars
+        - tile_size: Geometric size of the tile in [deg]
+        - sc_size: File size of the star catalog.
+        - validity: Validity of the star catalog.
+        - sc_name: Name of the star catalog. Available options include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
+        - _mode: Type of the star catalog. Available options include 'raw', 'reduced', 'simplified', where
+            'raw' represents the original star catalog, which covers all information about the stars,
+            'reduced' represents the reduced star catalog, which contains the position, proper motion, apparent magnitude, epoch of the stars,
+            'simplified' represents the minimalist star catalog, which only includes the position and apparent magnitude of the stars at a specific epoch.
         - stars_num: Total number of stars in the catalog
-        - mag: Apparent magnitude of stars in the catalog
+        - mag: Range of apparent magnitudes for the catalog
         - description: Catalog Summary
-
     Methods:
         - load: Load the reduced star catalog files from the local database.
-        - simplify: Simplify the reduced star catalog so that the simplified star catalog only contains key information: the position and apparent magnitude of stars.
-        - search_box: Perform a rectangle search of stars on the reduced star catalog and return an instance of class Stars.
-        - search_cone: Perform a cone search of stars on the reduced star catalog and return an instance of class Stars.   
-        - _search_draw: Visualize the scope of the search area and the coverage of the corresponding tiles.  
+        - simplify: Simplify the reduced star catalog so that it only contains key information of the stars, such as the celetial position and apparent magnitude, etc.
+        - search_box: Perform a rectangle search on the reduced star catalog.
+        - search_cone: Perform a cone search on the reduced star catalog.
+        - _search_draw: Visualize the scope of the search area and the coverage of the corresponding tiles.
     """  
     def __init__(self,info):  
 
         self.info = info
 
         for key in info.keys():
             setattr(self, key, info[key])
@@ -566,55 +538,51 @@
 
     def load(sc_name,tile_size,dir_from=None):
         """
         Load the reduced star catalog files from the local database.
 
         Usage:
             >>> from starcatalogquery import StarCatalogReduced
-            >>> # load the reduced star catalog GAIADR3
-            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalog/reduced/gaiadr3/res2/'
-            >>> gaiadr3_reduced = StarCatalogReduced.load('reduced','gaiadr3',2,dir_from_reduced)
-
-        Inputs:
-            sc_name -> [str] Name of the starcatalog. Available starcatalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
-            tile_size -> [int] Size of the tile in [deg]
-            dir_from -> [str,optional,default=None] The loading path of the star catalog files. If None, the path is automatically assigned to a suitable directory by default.
-
+            >>> # load the reduced star catalog HYGv3.5
+            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalogs/reduced/hygv35/res5/'
+            >>> hygv35_reduced = StarCatalogReduced.load('hygv35',5,dir_from_reduced)
+        Inputs:
+            sc_name -> [str] Name of the star catalog. Available options include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
+            tile_size -> [int] Geometric size of the tile in [deg]
+            dir_from -> [str,optional,default=None] Directory of the star catalog files. If None, it is assigned to a build-in directory by default.
         Outputs:
             Instance of class StarCatalogReduced
         """
         if dir_from is None: dir_from = 'starcatalogs/reduced/{:s}/res{:d}/'.format(sc_name,tile_size)    
         if not os.path.exists(dir_from): raise Exception('Path of the star catalog {:s} does not exist.'.format(sc_name))  
 
-        # calculate total size and numbers of tile files    
+        # calculate the total file size and numbers of tile files    
         file_num,dir_size,validity = tiles_statistic(dir_from,tile_size) 
         stars_num,mag,description = starcatalog_info(sc_name)
 
         dict_values = dir_from,dir_size,file_num,validity,sc_name,'{:d} deg'.format(tile_size),'reduced',stars_num,mag,description
         dict_keys = 'tiles_path','sc_size','tiles_num','validity','sc_name','tile_size','_mode','stars_num','mag','description'
         info = dict(zip(dict_keys, dict_values))
 
         return StarCatalogReduced(info)  
 
     def simplify(self,mag_threshold,t_pm,dir_simplified=None):
         """
-        Simplify the reduced star catalog so that the simplified star catalog only contains key information: the position and apparent magnitude of stars.
+        Simplify the reduced star catalog so that it only contains key information of the stars, such as the celetial position and apparent magnitude of stars.
 
         Usage:
             >>> from starcatalogquery import StarCatalogReduced
-            >>> # load the reduced star catalog GAIADR3
-            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalog/reduced/gaiadr3/res2/'
-            >>> gaiadr3_reduced = StarCatalogReduced.load('reduced','gaiadr3',2,dir_from_reduced)
-            >>> gaiadr3_simplified = gaiadr3_reduced.simplify(9.0,2022.0)
-
-        Inputs:
-            mag_threshold -> [float] Apparent magnitude limit of the detector  
-            t_pm -> [float] The epoch when the search was performed
-            dir_simplified -> [str,optional,default=None] The path of the simplified star catalog files to store. If None, the path is automatically assigned to a suitable directory by default.
-
+            >>> # load the reduced star catalog HYGv3.5
+            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalogs/reduced/hygv35/res5/'
+            >>> hygv35_reduced = StarCatalogReduced.load('hygv35',5,dir_from_reduced)
+            >>> hygv35_simplified = hygv35_reduced.simplify(9.0,2022.0)
+        Inputs:
+            mag_threshold -> [float] Apparent magnitude limit
+            t_pm -> [float] Epoch to which the simplification is unified
+            dir_simplified -> [str,optional,default=None] Directory of the simplified star catalog files. If None, it is assigned to a build-in directory by default.
         Outputs:
             Instance of class StarCatalogSimplified      
         """
         info = self.info.copy()
         tile_size = int(self.tile_size.split(' ')[0])
         tiles_path = self.tiles_path
         if dir_simplified is None:
@@ -642,15 +610,15 @@
             if {'pmra', 'pmdec'}.issubset(df_simplified.columns):    
                 df_simplified['ra'] +=  df_simplified['pmra']/3.6e6 * dt   
                 df_simplified['dec'] += df_simplified['pmdec']/3.6e6 * dt
                 df_simplified = df_simplified.drop(['pmra','pmdec'],axis=1)
             else:
                 warnings.warn('Proper motion data for stars in catalog {:s} are not found.'.format(sc_name))
                     
-            #df_simplified['epoch'] = t_pm
+            # df_simplified['epoch'] = t_pm
             df_simplified.drop(columns=['epoch'],inplace=True)
             df_simplified['ra'] = df_simplified['ra'].round(6)
             df_simplified['dec'] = df_simplified['dec'].round(6)
             df_simplified['mag'] = df_simplified['mag'].round(1)
 
             df_simplified.to_csv(dir_simplified + tile_file.split('/')[-1],index=False)  
 
@@ -658,313 +626,301 @@
 
         print('\nFinished')
 
         file_num,dir_size,validity = tiles_statistic(dir_simplified,tile_size)  
         info['_mode'] = 'simplified'
         info['tiles_path'] = dir_simplified
         info['sc_size'] = dir_size
-        info['mag_cutoff'] = mag_threshold
+        info['mag_threshold'] = mag_threshold
         info['epoch'] = t_pm
 
         return StarCatalogSimplified(info)    
 
-    def search_box(self,radec_box,mag_threshold,t_pm,max_control_points=None):
+    def search_box(self,radec_box,mag_threshold,t_pm,max_num=None):
         """
-        Perform a rectangle search of stars on the reduced star catalog and return an instance of class Stars.
+        Perform a rectangle search of stars on the reduced star catalog.
 
         Usage:
             >>> from starcatalogquery import StarCatalogReduced
-            >>> # load the reduced star catalog GAIADR3
-            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalog/reduced/gaiadr3/res2/'
-            >>> gaiadr3_reduced = StarCatalogReduced.load('reduced','gaiadr3',2,dir_from_reduced)
-            >>> stars = gaiadr3_reduced.search_box([20,30,30,40],8,2023.0)
-
-        Inputs:
-            radec_box -> [int,array_like] Rectangular search area in format of [ra_min,dec_min,ra_max,dec_max], where
-                ra_min -> [float] Left border of RA in [deg].
-                dec_min -> [float] Lower border of DEC in [deg].
-                ra_max -> [float] Right border of RA in [deg].
-                dec_max -> [float] Upper border of DEC in [deg].
-            mag_threshold -> [float] Apparent magnitude limit of the detector  
-            t_pm -> [float] The epoch when the search was performed    
-            max_control_points -> [int,optional,default=None] Number of brightest stars in the search area. If None, it is the number of all stars in the search area by deault.
-
+            >>> # load the reduced star catalog HYGv3.5
+            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalogs/reduced/hygv35/res5/'
+            >>> hygv35_reduced = StarCatalogReduced.load('hygv35',5,dir_from_reduced)
+            >>> stars = hygv35_reduced.search_box([20,30,30,40],9,2022.0)
+        Inputs:
+            radec_box -> [list] Rectangular search area in form of [ra_min,dec_min,ra_max,dec_max], where
+                ra_min -> [float] Left border of RA in [deg]
+                dec_min -> [float] Lower border of DEC in [deg]
+                ra_max -> [float] Right border of RA in [deg]
+                dec_max -> [float] Upper border of DEC in [deg]
+            mag_threshold -> [float] Apparent magnitude limit
+            t_pm -> [float] Epoch to which the stars are unified
+            max_num -> [int,optional,default=None] Maxinum number of the stars sorted by brightness for rectangle search. If None, all stars are counted in the search area by deault.
         Outputs:
             Instance of class Stars
         """
         width = int(self.tile_size.split()[0])
         df = search_box_magpm(radec_box,self.tiles_path,self.sc_name,width,self._mode,mag_threshold,t_pm)
-        info = df2info(self.sc_name,center,df,max_control_points) 
+        info = df2info(self.sc_name,center,df,max_num) 
         return Stars(info)
 
-    def search_cone(self,center,radius,mag_threshold,t_pm,max_control_points=None):   
+    def search_cone(self,center,radius,mag_threshold,t_pm,max_num=None):   
         """
-        Perform a cone search of stars on the reduced star catalog and return an instance of class Stars.
+        Perform a cone search of stars on the reduced star catalog.
 
         Usage:
             >>> from starcatalogquery import StarCatalogReduced
-            >>> # load the reduced star catalog GAIADR3
-            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalog/reduced/gaiadr3/res2/'
-            >>> gaiadr3_reduced = StarCatalogReduced.load('reduced','gaiadr3',2,dir_from_reduced)
-            >>> stars = gaiadr3_reduced.search_cone([20,30],10,8,2023.0)
-
+            >>> # load the reduced star catalog HYGv3.5
+            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalogs/reduced/hygv35/res5/'
+            >>> hygv35_reduced = StarCatalogReduced.load('hygv35',5,dir_from_reduced)
+            >>> stars = hygv35_reduced.search_cone([20,30],10,9,2022.0)
         Inputs:
-            center -> [int,array_like] Center of the cap in format of [ra_c,dec_c], where
+            center -> [list] Center of the cone in form of [ra_c,dec_c], where
                 ra_c -> [float] RA, in [deg].
                 dec_c -> [float] DEC, in [deg].
-            radius -> [float] Angular radius of the cap, in [deg].
-            mag_threshold -> [float] Apparent magnitude limit of the detector  
-            t_pm -> [float] The epoch when the search was performed
-            max_control_points -> [int,optional,default=None] Number of brightest stars in the search area. If None, it is the number of all stars in the search area by deault.
-
+            radius -> [float] Angular radius of the cone, in [deg].
+            mag_threshold -> [float] Apparent magnitude limit  
+            t_pm -> [float] Epoch to which the stars are unified
+            max_num -> [int,optional,default=None] Maxinum number of the stars sorted by brightness for cone search. If None, all stars are counted in the search area by deault.
         Outputs:
             Instance of class Stars
         """
         width = int(self.tile_size.split()[0])
         df = search_cone_magpm(center,radius,self.tiles_path,self.sc_name,width,self._mode,mag_threshold,t_pm)
-        info = df2info(self.sc_name,center,df,max_control_points) 
+        info = df2info(self.sc_name,center,df,max_num) 
         return Stars(info)
 
     def _search_draw(self,search_area):
         """
         Visualize the scope of the search area and the coverage of the corresponding tiles.
 
         Usage:
             >>> from starcatalogquery import StarCatalogReduced
-            >>> # load the reduced star catalog GAIADR3
-            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalog/reduced/gaiadr3/res2/'
-            >>> gaiadr3_reduced = StarCatalogReduced.load('reduced','gaiadr3',2,dir_from_reduced)
+            >>> # load the reduced star catalog HYGv3.5
+            >>> dir_from_reduced = '/Volumes/TOSHIBA/starcatalogs/reduced/hygv35/res5/'
+            >>> hygv35_reduced = StarCatalogReduced.load('hygv35',5,dir_from_reduced)
             >>> cone_area = {'cone':[20,30,10]}
-            >>> stars = gaiadr3_reduced._search_draw(cone_area)
-
+            >>> stars = hygv35_reduced._search_draw(cone_area)
         Inputs:
-            search_area -> [dict] The scope of the search area, such as {'cone':[20,30,10]} or {'box':[20,30,30,40]}, where
+            search_area -> [dict] Scope of the search area, such as {'cone':[20,30,10]} or {'box':[20,30,30,40]}, where
             for {'box':[ra_min,dec_min,ra_max,dec_max]}:
-                ra_min -> [float] Left border of RA in [deg].
-                dec_min -> [float] Lower border of DEC in [deg].
-                ra_max -> [float] Right border of RA in [deg].
-                dec_max -> [float] Upper border of DEC in [deg].
+                ra_min -> [float] Left border of RA in [deg]
+                dec_min -> [float] Lower border of DEC in [deg]
+                ra_max -> [float] Right border of RA in [deg]
+                dec_max -> [float] Upper border of DEC in [deg]
             for {'cone':[ra_c,dec_c,radius]}:
-                ra_c -> [float] RA, in [deg].
-                dec_c -> [float] DEC, in [deg].
-                radius -> [float] Angular radius of the cap, in [deg].  
-
+                ra_c -> [float] RA, in [deg]
+                dec_c -> [float] DEC, in [deg]
+                radius -> [float] Angular radius of the cone, in [deg] 
         Outputs:
-            An image that shows the scope of the search area and the coverage of the corresponding tiles.          
+            An image sketching the scope of the search area and the coverage of the corresponding tiles.          
         """
         width = int(self.tile_size.split()[0]) 
         search_draw(width,search_area)   
 
 class StarCatalogSimplified(object):
     """
     Class StarCatalogSimplified
 
     Attributes:
-        - tiles_path: Path of the starcatalog tile files. 
-        - sc_size: The size of the star catalog.
+        - tiles_path: Path of the star catalog files. 
         - tiles_num: Total number of the tile files.
-        - validity: The validity of the star catalog.
-        - sc_name: Name of the starcatalog. Available starcatalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
-        - tile_size: Size of the tile in [deg]
-        - _mode: Types of star catalogs, including 'raw', 'reduced', 'simplified', where
-            'raw' represents the original star catalog, which contains all information about the star
-            'reduced' represents the reduced star catalog, which contains the position, proper motion, apparent magnitude, epoch of the star
-            'simplified' represents the minimalist star catalog, which only includes the position and apparent magnitude of stars
+        - tile_size: Geometric size of the tile in [deg]
+        - sc_size: File size of the star catalog.
+        - validity: Validity of the star catalog.
+        - sc_name: Name of the star catalog. Available options include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
+        - _mode: Type of the star catalog. Available options include 'raw', 'reduced', 'simplified', where
+            'raw' represents the original star catalog, which covers all information about the stars,
+            'reduced' represents the reduced star catalog, which contains the position, proper motion, apparent magnitude, epoch of the stars,
+            'simplified' represents the minimalist star catalog, which only includes the position and apparent magnitude of the stars at a specific epoch.
         - stars_num: Total number of stars in the catalog
-        - mag: Apparent magnitude of stars in the catalog
+        - mag: Range of apparent magnitudes for the catalog
         - description: Catalog Summary
-
     Methods:
         - load: Load the simplified star catalog files from the local database.
-        - search_box: Perform a rectangle search of stars on the simplified star catalog and return an instance of class Stars.
-        - search_cone: Perform a cone search of stars on the simplified star catalog and return an instance of class Stars.   
-        - _search_draw: Visualize the scope of the search area and the coverage of the corresponding tiles.  
-        - h5_incices: Generate a h5-formatted star catalog file, which records the center pointing of each sky area, the pixel coordinates of the stars, the triangle invariants and the asterism indices.
+        - search_box: Perform a rectangle search on the simplified star catalog.
+        - search_cone: Perform a cone search on the simplified star catalog.
+        - _search_draw: Visualize the scope of the search area and the coverage of the corresponding tiles.
+        - h5_incices: Generate a h5-formatted star catalog indices file, which records the center pointing, pixel coordinates of the stars, triangle invariants and asterism indices of each sky area.
     """    
     def __init__(self,info):  
 
         self.info = info
 
         for key in info.keys():
             setattr(self, key, info[key])
 
     def __repr__(self):
     
         return 'Instance of class StarCatalogSimplified'        
 
-    def load(sc_name,tile_size,mag_cutoff,epoch,dir_from=None):
+    def load(sc_name,tile_size,mag_threshold,epoch,dir_from=None):
         """
         Load the simplified star catalog files from the local database.
 
         Usage:
             >>> from starcatalogquery import StarCatalogSimplified
-            >>> # load the simplified star catalog GAIADR3
-            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalog/simplified/gaiadr3/res2/'
-            >>> gaiadr3_simplified = StarCatalogSimplified.load('simplified','gaiadr3',2,dir_from_simplified)
-
-        Inputs:
-            sc_name -> [str] Name of the starcatalog. Available starcatalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
-            tile_size -> [int] Size of the tile in [deg]
-            mag_cutoff -> [float] The truncated magnitude of the simplified star catalog
-            epoch -> [float] The epoch of the simplified star catalog
-            dir_from -> [str,optional,default=None] The loading path of the star catalog files. If None, the path is automatically assigned to a suitable directory by default.
-
+            >>> # load the simplified star catalog HYGv3.5
+            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
+            >>> hygv35_simplified = StarCatalogSimplified.load('hygv35',5,9,2022,dir_from_simplified)
+        Inputs:
+            sc_name -> [str] Name of the star catalog. Available options include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
+            tile_size -> [int] Geometric size of the tile in [deg]
+            mag_threshold -> [float] Apparent magnitude limit
+            epoch -> [float] Epoch of the star catalog
+            dir_from -> [str,optional,default=None] Diectory of the star catalog files. If None, it is assigned to a build-in directory by default.
         Outputs:
             Instance of class StarCatalogSimplified
         """ 
-        if dir_from is None: dir_from = 'starcatalogs/simplified/{:s}/res{:d}/mag{:.1f}/epoch{:.1f}/'.format(sc_name,tile_size,mag_cutoff,epoch)
+        if dir_from is None: dir_from = 'starcatalogs/simplified/{:s}/res{:d}/mag{:.1f}/epoch{:.1f}/'.format(sc_name,tile_size,mag_threshold,epoch)
         if not os.path.exists(dir_from): raise Exception('Path of the star catalog {:s} does not exist.'.format(sc_name))  
 
         # calculate total size and numbers of tile files    
         file_num,dir_size,validity = tiles_statistic(dir_from,tile_size) 
         stars_num,mag,description = starcatalog_info(sc_name)
 
-        dict_values = dir_from,dir_size,file_num,validity,sc_name,'{:d} deg'.format(tile_size),'simplified',stars_num,mag,description,mag_cutoff,epoch
-        dict_keys = 'tiles_path','sc_size','tiles_num','validity','sc_name','tile_size','_mode','stars_num','mag','description','mag_cutoff','epoch'
+        dict_values = dir_from,dir_size,file_num,validity,sc_name,'{:d} deg'.format(tile_size),'simplified',stars_num,mag,description,mag_threshold,epoch
+        dict_keys = 'tiles_path','sc_size','tiles_num','validity','sc_name','tile_size','_mode','stars_num','mag','description','mag_threshold','epoch'
         info = dict(zip(dict_keys, dict_values))
 
         return StarCatalogSimplified(info)   
 
-    def search_box(self,radec_box,max_control_points=None):
+    def search_box(self,radec_box,max_num=None):
         """
-        Perform a rectangle search of stars on the simplified star catalog and return an instance of class Stars.
+        Perform a rectangle search of stars on the simplified star catalog.
 
         Usage:
             >>> from starcatalogquery import StarCatalogSimplified
-            >>> # load the simplified star catalog GAIADR3
-            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalog/simplified/gaiadr3/res2/'
-            >>> gaiadr3_simplified = StarCatalogSimplified.load('simplified','gaiadr3',2,dir_from_simplified)
-            >>> stars = gaiadr3_simplified.search_box([20,30,30,40])
-
-        Inputs:
-            radec_box -> [int,array_like] Rectangular search area in format of [ra_min,dec_min,ra_max,dec_max], where
-                ra_min -> [float] Left border of RA in [deg].
-                dec_min -> [float] Lower border of DEC in [deg].
-                ra_max -> [float] Right border of RA in [deg].
-                dec_max -> [float] Upper border of DEC in [deg].
-            max_control_points -> [int,optional,default=None] Number of brightest stars in the search area. If None, it is the number of all stars in the search area by deault.
-
+            >>> # load the simplified star catalog HYGv3.5
+            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
+            >>> hygv35_simplified = StarCatalogSimplified.load('hygv35',5,9,2022,dir_from_simplified)
+            >>> stars = hygv35_simplified.search_box([20,30,30,40])
+        Inputs:
+            radec_box -> [list] Rectangular search area in form of [ra_min,dec_min,ra_max,dec_max], where
+                ra_min -> [float] Left border of RA in [deg]
+                dec_min -> [float] Lower border of DEC in [deg]
+                ra_max -> [float] Right border of RA in [deg]
+                dec_max -> [float] Upper border of DEC in [deg]
+            max_num -> [int,optional,default=None] Maxinum number of the stars sorted by brightness for rectangle search. If None, all stars are counted in the search area by deault.
         Outputs:
             Instance of class Stars
         """
         width = int(self.tile_size.split()[0])
         df = search_box(radec_box,self.tiles_path,self.sc_name,width,self._mode) 
-        info = df2info(self.sc_name,center,df,max_control_points) 
+        info = df2info(self.sc_name,center,df,max_num) 
         return Stars(info)
 
-    def search_cone(self,center,radius,max_control_points=None):   
+    def search_cone(self,center,radius,max_num=None):   
         """
-        Perform a cone search of stars on the simplified star catalog and return an instance of class Stars.
+        Perform a cone search of stars on the simplified star catalog.
 
         Usage:
             >>> from starcatalogquery import StarCatalogSimplified
-            >>> # load the simplified star catalog GAIADR3
-            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalog/simplified/gaiadr3/res2/'
-            >>> gaiadr3_simplified = StarCatalogSimplified.load('simplified','gaiadr3',2,dir_from_simplified)
-            >>> stars = gaiadr3_simplified.search_cone([20,30],10)
-
-        Inputs:
-            center -> [int,array_like] Center of the cap in format of [ra_c,dec_c], where
-                ra_c -> [float] RA, in [deg].
-                dec_c -> [float] DEC, in [deg].
-            radius -> [float] Angular radius of the cap, in [deg].
-            max_control_points -> [int,optional,default=None] Number of brightest stars in the search area. If None, it is the number of all stars in the search area by deault.
-
+            >>> # load the simplified star catalog HYGv3.5
+            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
+            >>> hygv35_simplified = StarCatalogSimplified.load('hygv35',5,9,2022,dir_from_simplified)
+            >>> stars = hygv35_simplified.search_cone([20,30],10)
+        Inputs:
+            center -> [int,array_like] Center of the cone in form of [ra_c,dec_c], where
+                ra_c -> [float] RA, in [deg]
+                dec_c -> [float] DEC, in [deg]
+            radius -> [float] Angular radius of the cone, in [deg].
+            max_num -> [int,optional,default=None] Maxinum number of the stars sorted by brightness for rectangle search. If None, all stars are counted in the search area by deault.
         Outputs:
             Instance of class Stars
         """
         width = int(self.tile_size.split()[0])
         df = search_cone(center,radius,self.tiles_path,self.sc_name,width,self._mode)
-        info = df2info(self.sc_name,center,df,max_control_points) 
+        info = df2info(self.sc_name,center,df,max_num) 
         return Stars(info)
 
     def _search_draw(self,search_area):
         """
         Visualize the scope of the search area and the coverage of the corresponding tiles.
 
         Usage:
             >>> from starcatalogquery import StarCatalogSimplified
-            >>> # load the simplified star catalog GAIADR3
-            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalog/simplified/gaiadr3/res2/'
-            >>> gaiadr3_simplified = StarCatalogReduced.load('simplified','gaiadr3',2,dir_from_simplified)
+            >>> # load the simplified star catalog HYGv3.5
+            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
+            >>> hygv35_simplified = StarCatalogReduced.load('hygv35',5,9,2022,dir_from_simplified)
             >>> cone_area = {'cone':[20,30,10]}
-            >>> stars = gaiadr3_simplified._search_draw(cone_area)
-
+            >>> stars = hygv35_simplified._search_draw(cone_area)
         Inputs:
-            search_area -> [dict] The scope of the search area, such as {'cone':[20,30,10]} or {'box':[20,30,30,40]}, where
+            search_area -> [dict] Scope of the search area, such as {'cone':[20,30,10]} or {'box':[20,30,30,40]}, where
             for {'box':[ra_min,dec_min,ra_max,dec_max]}:
-                ra_min -> [float] Left border of RA in [deg].
-                dec_min -> [float] Lower border of DEC in [deg].
-                ra_max -> [float] Right border of RA in [deg].
-                dec_max -> [float] Upper border of DEC in [deg].
+                ra_min -> [float] Left border of RA in [deg]
+                dec_min -> [float] Lower border of DEC in [deg]
+                ra_max -> [float] Right border of RA in [deg]
+                dec_max -> [float] Upper border of DEC in [deg]
             for {'cone':[ra_c,dec_c,radius]}:
-                ra_c -> [float] RA, in [deg].
-                dec_c -> [float] DEC, in [deg].
-                radius -> [float] Angular radius of the cap, in [deg].  
-
+                ra_c -> [float] RA, in [deg]
+                dec_c -> [float] DEC, in [deg]
+                radius -> [float] Angular radius of the cone, in [deg].  
         Outputs:
-            An image that shows the scope of the search area and the coverage of the corresponding tiles.          
+            An image sketching the scope of the search area and the coverage of the corresponding tiles.          
         """
         width = int(self.tile_size.split()[0]) 
         search_draw(width,search_area)   
 
-    def h5_incices(self,fov,pixel_width,max_control_points=60):
+    def h5_incices(self,fov,pixel_width,max_num=30):
         """
-        Generate a h5-formatted star catalog file, which records the center pointing of each sky area, the pixel coordinates of the stars, the triangle invariants and the asterism indices.
+        Generate a h5-formatted star catalog incices file, which records the center pointing, pixel coordinates of the stars, triangle invariants and asterism indices of each sky area.
 
         Usage:
             >>> from starcatalogquery import StarCatalogSimplified
-            >>> # load the simplified star catalog GAIADR3
-            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalog/simplified/gaiadr3/res2/'
-            >>> gaiadr3_simplified = StarCatalogSimplified.load('simplified','gaiadr3',2,dir_from_simplified)
-            >>> outh5 = gaiadr3_simplified.h5_incices(20,0.01)
-
+            >>> # load the simplified star catalog HYGv3.5
+            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
+            >>> hygv35_simplified = StarCatalogSimplified.load('hygv35',5,9,2022,dir_from_simplified)
+            >>> outh5 = hygv35_simplified.h5_incices(8,0.01)
         Inputs:
             fov -> [float] FOV of camera
             pixel_width -> [float] Pixel width in [deg]
-            max_control_points -> [int,optional,default=60] Number of brightest stars in the search area.
-
+            max_num -> [int,optional,default=30] Maxinum number of the stars sorted by brightness used for a sky area.
         Outputs:
-            h5-formatted star catalog file    
+            outh5 -> h5-formatted star catalog indices file    
         """ 
         dir_h5 = 'starcatalogs/indices/{:s}/'.format(self.sc_name)
         Path(dir_h5).mkdir(parents=True, exist_ok=True)  
 
-        outh5 = dir_h5 + 'fov{:d}_mag{:.1f}_mcp{:d}_{:.1f}.h5'.format(fov,self.mag_cutoff,max_control_points,self.epoch)
+        if fov >= 28.4 and fov < 58.6: 
+            k,nside = 0,1
+            search_radius = 37.2
+        elif fov >= 13.4 and fov < 28.4:
+            k,nside = 1,2
+            search_radius = 17.0
+        elif fov >= 6.6 and fov < 13.4:
+            k,nside = 2,4
+            search_radius = 9.3
+        elif fov >= 3.3 and fov < 6.6:
+            k,nside = 3,8
+            search_radius = 4.1  
+        else:
+            raise Exception('FOV should be between 3.3 and 58.6 deg')     
+
+        outh5 = dir_h5 + 'k{:d}_mag{:.1f}_mcp{:d}_{:.1f}.h5'.format(k,self.mag_threshold,max_num,self.epoch)
 
         if os.path.exists(outh5): return outh5 
 
         # write to h5 file
         fout = h5py.File(outh5,'w')
         # create group 
         stars_xy_grp = fout.create_group("stars_xy")
         stars_invariants_grp = fout.create_group("stars_invariants")
         stars_asterisms_grp = fout.create_group("stars_asterisms")
 
-        if fov > 43: 
-            nside = 1
-            search_radius = 34
-        elif fov > 22:
-            nside = 2
-            search_radius = 17
-        else:
-            nside = 4
-            search_radius = 9
-
         npix = hp.nside2npix(nside)
         fp_radecs = []
         for seq in range(npix):
 
-            desc = 'Generating starcatalog sky area index {:s}{:d}{:s} of {:d}'.format(Fore.BLUE,seq+1,Fore.RESET,npix)
+            desc = 'Generating starcatalog sky area index {:s}{:d}{:s} of {:d} for level k{:d}'.format(Fore.BLUE,seq+1,Fore.RESET,npix,k)
             print(desc,end='\r')
 
             fp_radec = hp.pix2ang(nside,seq,lonlat=True)
             fp_radecs.append(fp_radec)
 
-            stars = self.search_cone(fp_radec,search_radius,max_control_points)
+            stars = self.search_cone(fp_radec,search_radius,max_num)
             stars.pixel_xy(pixel_width)
             stars.invariantfeatures()
 
             stars_xy_grp.create_dataset(str(seq), data=stars.xy)
             stars_invariants_grp.create_dataset(str(seq), data=stars.invariants)
             stars_asterisms_grp.create_dataset(str(seq), data=stars.asterisms)  
 
@@ -973,21 +929,20 @@
         return outh5    
             
 class Stars(object):
     """
     Class Stars
 
     Attributes:
-        - sc_name: Name of the starcatalog.
-        - center: Center pointing in format of [ra_c,dec_c] in [deg]
-        - df: Dataframe of the stars
-        - max_control_points: Number of stars in the dataframe
+        - sc_name: Name of the star catalog
+        - center: Center pointing in form of [ra_c,dec_c] in [deg]
+        - df: Pandas dataframe of the stars
+        - max_num: Number of stars in the dataframe
         - xy: Pixel coordinates of stars
         - radec: Celestial coordinates of stars
-
     Methods:
         - pixel_xy: Calculate the pixel coordinates of stars in a sky area.
     """    
 
     def __init__(self,info):  
 
         self.info = info
@@ -1001,23 +956,21 @@
 
     def pixel_xy(self,pixel_width):
         """
         Calculate the pixel coordinates of stars in a sky area.
 
         Usage:
             >>> from starcatalogquery import StarCatalogSimplified
-            >>> # load the simplified star catalog GAIADR3
-            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalog/simplified/gaiadr3/res2/'
-            >>> gaiadr3_simplified = StarCatalogReduced.load('simplified','gaiadr3',2,dir_from_simplified)
-            >>> gaiadr3_simplified_stars = gaiadr3_simplified.search_cone([20,30],10)
-            >>> stars = gaiadr3_simplified_stars.pixel_xy(0.01)
-
+            >>> # load the simplified star catalog HYGv3.5
+            >>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
+            >>> hygv35_simplified = StarCatalogReduced.load(hygv35',5,9,2022,dir_from_simplified)
+            >>> hygv35_simplified_stars = hygv35_simplified.search_cone([20,30],10)
+            >>> stars = hygv35_simplified_stars.pixel_xy(0.01)
         Inputs:
             pixel_width -> [float] Pixel width in [deg]
-
         Outputs:
             Instance of class Stars       
         """
         # Define WCS transformation and convert the celestial coordinates to pixel coordinates
         x,y,wcs = xy_catalog(self.center,self.radec,pixel_width)
 
         df = self.info['df']
```

## starcatalogquery/utils/try_download.py

```diff
@@ -1,19 +1,19 @@
 import wget
 
 def wget_download(url,dir_file,desc=None):
     """
-    Download a file using the wget command line.
+    Download files by wget command
 
     Inputs:
         url -> [str] URL of the file to download
-        dir_file -> [str] Path of the file downloaded
+        dir_file -> [str] Path of the file to store
         desc -> [str,optional,default=None] Description of the downloading   
-
     Outputs:
-        wget_out -> [str] Same as the dir_file 
+        wget_out -> [str] Path of the file downloaded
+
     """
     if desc: print(desc)
     wget_out = wget.download(url,dir_file)
     print()
 
     return wget_out
```

## Comparing `starcatalogquery-0.1.8.dist-info/LICENSE` & `starcatalogquery-0.1.9.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `starcatalogquery-0.1.8.dist-info/METADATA` & `starcatalogquery-0.1.9.dist-info/METADATA`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: starcatalogquery
-Version: 0.1.8
+Version: 0.1.9
 Summary: A package to establish an offline star catalog query database
 Home-page: https://github.com/lcx366/STARQUERY
 Author: Chunxiao Li
 Author-email: lcx366@126.com
 License: MIT
 Keywords: StarCatalog
 Classifier: Development Status :: 4 - Beta
@@ -55,16 +55,16 @@
 ### Build an offline star catalog database
 
 Get the star catalog data from the remote server ([MIKULSKI ARCHIVE&
 SPACE TELESCOPES](https://archive.stsci.edu)) , and build an offline star catalog database locally. Currently, available star catalogs include 'hygv35', 'gsc12', 'gsc242', 'gaiadr3', '2mass', 'ucac5', 'usnob', etc.
 
 ```python
 >>> from starcatalogquery import StarCatalog
->>> # Get the star catalog GAIADR3 with the tile size of 2 deg
->>> gaiadr3_raw = StarCatalog.get('gaiadr3',2)
+>>> # Get the star catalog HYGv3.5 with the tile size of 2 deg
+>>> hygv35_raw = StarCatalog.get('hygv35',2)
 ```
 
 We get an instance of class StarCatalogRaw with
 
     Attributes:
         - tiles_path: Path of the starcatalog tile files. 
         - sc_size: The size of the star catalog.
@@ -87,63 +87,63 @@
         - _search_draw: Visualize the scope of the search area and the coverage of the corresponding tiles.  
 
 ### Reduce the raw star catalogs
 
 The original star catalog contains all the catalog information of the stars, which takes up a huge storage space and slows down the speed of star query. Therefore, we need to extract the necessary information of stars from it, and use the method `.reduce()` to build a reduced star catalog database.
 
 ```python
->>> gaiadr3_reduced = gaiadr3_raw.reduce()
+>>> hygv35_reduced = hygv35_raw.reduce()
 ```
 
 The reduced star catalog only contains the celestial position, proper motion, apparent magnitude, and epoch of stars.
 
 ### Simplify the reduced star catalogs
 
 In order to further reduce the size of the star catalog and improve its query efficiency, we filter out the reduced star catalog according to the limit magnitude of the detector, and make proper motion corrections to obtain a minimalist star catalog.
 
 ```python
->>> mag_threshold, t_pm = 9.0,2022.0 
->>> gaiadr3_simplified = gaiadr3_reduced.simplify(mag_threshold,t_pm)
+>>> mag_threshold,t_pm = 9.0,2022.0 
+>>> hygv35_simplified = hygv35_reduced.simplify(mag_threshold,t_pm)
 ```
 
 The simplified(minimalist) star catalog only includes the celetial position and apparent magnitude of stars at a specific epoch.
 
 ### Query information about stars in a specific sky area
 
 Perform a cone search of stars on the raw or reduced star catalog.
 
 ```python
 >>> # Set center pointing in format of [Ra,Dec] in [deg] and search radius in [deg]
 >>> center,radius = [20,30],15 
 >>> # Set cutoff magnitude and observation epoch
->>> mag_threshold,t_pm = 8.0,2023.5
+>>> mag_threshold,t_pm = 9.0,2022.0
 >>> # Set the maximum number of brightest stars to output
 >>> max_control_points = 100 # optinal, default = None
->>> gaiadr3_raw_stars = gaiadr3_raw.search_cone(center,radius,mag_threshold,t_pm,max_control_points)
->>> gaiadr3_reduced_stars = gaiadr3_reduced.search_cone(center,radius,mag_threshold,t_pm,max_control_points)
+>>> hygv35_raw_stars = hygv35_raw.search_cone(center,radius,mag_threshold,t_pm,max_control_points)
+>>> hygv35_reduced_stars = hygv35_reduced.search_cone(center,radius,mag_threshold,t_pm,max_control_points)
 ```
 
 Perform a rectangle search of stars on the raw or reduced star catalog.
 
 ```python
 >>> # Set a rectangular search area in format of [ra_min,dec_min,ra_max,dec_max] in [deg]
 >>> radec_box = [5,15,35,45]
 >>> # Set cutoff magnitude and observation epoch
->>> mag_threshold,t_pm = 8.0,2023.5
+>>> mag_threshold,t_pm = 9.0,2022.0
 >>> # Set the maximum number of brightest stars to output
 >>> max_control_points = 100 # optinal, default = None
->>> gaiadr3_raw_stars = gaiadr3_raw.search_box(radec_box,mag_threshold,t_pm,max_control_points)
->>> gaiadr3_reduced_stars = gaiadr3_reduced.search_box(radec_box,mag_threshold,t_pm,max_control_points)
+>>> hygv35_raw_stars = hygv35_raw.search_box(radec_box,mag_threshold,t_pm,max_control_points)
+>>> hygv35_reduced_stars = hygv35_reduced.search_box(radec_box,mag_threshold,t_pm,max_control_points)
 ```
 
 Perform a cone/rectangle search of stars on the simplified star catalog.
 
 ```python
->>> gaiadr3_simplified_stars = gaiadr3_simplified.search_cone(center,radius,max_control_points)
->>> gaiadr3_simplified_stars = gaiadr3_simplified.search_box(radec_box,max_control_points)
+>>> hygv35_simplified_stars = hygv35_simplified.search_cone(center,radius,max_control_points)
+>>> hygv35_simplified_stars = hygv35_simplified.search_box(radec_box,max_control_points)
 ```
 
 We get an instance of class Stars, with
 
     Attributes:
         - sc_name: Name of the starcatalog.
         - center: Center pointing in format of [ra_c,dec_c] in [deg]
@@ -155,104 +155,111 @@
 
 ### Calculate the pixel coordinates of the filtered stars
 
 Given the pixel width of the detector, calculate the pixel coordinates of the filtered stars using the *TAN* projection in WCS transformations.
 
 ```python
 >>> pixel_width = 0.01 # pixel width in [deg]
->>> gaiadr3_simplified_stars.pixel_xy(0.01)
->>> print(gaiadr3_simplified_stars.xy)
+>>> hygv35_simplified_stars.pixel_xy(0.01)
+>>> print(hygv35_simplified_stars.xy)
 ```
 
 ### Calculate the triangle invariants and the asterism indices of the filtered stars
 
 ```python
->>> gaiadr3_simplified_stars.invariantfeatures()
->>> print(gaiadr3_simplified_stars.invariants,gaiadr3_simplified_stars.asterisms,.kdtree)
+>>> hygv35_simplified_stars.invariantfeatures()
+>>> hygv35_simplified_stars.invariantfeatures()
+>>> print(hygv35_simplified_stars.invariants,hygv35_simplified_stars.asterisms,.kdtree)
 ```
 
 ### Visualization
 
 Visualize the scope of the search area and the coverage of the corresponding catalog tiles.
 
 ```python
 >>> box_area = {'box':[5,15,35,45]} # {'box':[ra_min,dec_min,ra_max,dec_max]}
 >>> cone_area = {'cone':[20,30,15]} # {'cone':[ra_c,dec_c,radius]}
->>> gaiadr3_simplified._search_draw(box_area)
->>> gaiadr3_simplified._search_draw(cone_area)
->>> # ._search_draw is also available for gaiadr3_raw and gaiadr3_reduced
+>>> hygv35_simplified._search_draw(box_area)
+>>> hygv35_simplified._search_draw(cone_area)
+>>> # ._search_draw is also available for hygv35_raw and hygv35_reduced
 ```
 
 <p align="middle">
   <img src="readme_figs/box.png" width="500" />
 </p>
 
 <p align="middle">
   <img src="readme_figs/cone.png" width="500" />
 </p>
 
-### Divide the sky
+### Divide the sky into multiple equal-area sky regions
 
-The celestial sphere can be divided into multiple equal-area sky regions using the HEALPix algorithm. Then a feature library is established in each sky area for blind matching of star maps. 
+For blind matching of star maps, the celestial sphere is pre-divided into multiple equal-area sky regions using the HEALPix algorithm.
 
 <p align="middle">
   <img src="readme_figs/healpix_list.png" width="400" />
 </p>
 
 <p align="middle">
   <img src="readme_figs/healpix_table.png" width="400" />
 </p>
 
-By default, we adopt the following strategy to divide the sky area:
+By default, the following strategy is adopted to divide the sky area:
 
-- For FOV > 43, k = 0, radius of cone search = 34; 
+- For 58.6 > FOV >= 28.4, k = 0, radius of cone search = 37.2; 
 
-- For FOV > 22, k = 1, radius of cone search = 17;
+- For 28.4 > FOV >= 13.4, k = 1, radius of cone search = 17.0;
 
-- Else, k = 2, radius of cone search = 9
+- For 13.4 > FOV >= 6.6, k = 2, radius of cone search = 8.3;
+
+- For 6.6 > FOV >= 3.3, k = 3, radius of cone search = 4.1;
 
 ```python
->>> fov,pixel_width = 20,0.01 # in [deg]
+>>> fov,pixel_width = 8,0.01 # in [deg]
 >>> # Set the maximum number of brightest stars in earch sky area
->>> max_control_points = 40 # optional, default = 60
->>> outh5 = gaiadr3_simplified.h5_incices(fov,pixel_width,max_control_points)
+>>> max_control_points = 30 
+>>> outh5 = hygv35_simplified.h5_incices(fov,pixel_width,max_control_points)
 ```
 
-A h5-formatted star catalog file `outh5`is generated, which records the center pointing of each sky area, the pixel coordinates, the triangle invariants and the asterism indices of the stars.
+A h5-formatted star catalog indices file is generated, which records the center pointing, pixel coordinates of the stars, triangle invariants and asterism indices of each sky area.
 
-### Read in h5-formatted star catalog file
+### Read and parse the h5-formatted star catalog indices file
 
 ```python
 >>> from starcatalogquery import StarCatalog
 >>> infile_h5 = 'starcatalogs/indices/hygv35/fov20_mag8_mcp40_2023.0.h5'
 >>> fp_radecs,stars_xy,stars_invariants,stars_asterisms = StarCatalog.read_h5_indices(infile_h5)
 ```
 
 ### Load the local offline star catalog database
 
 #### Load the raw or reduced star catalog
 
 ```python
 >>> from starcatalogquery import StarCatalog
->>> dir_from_raw = '/Volumes/TOSHIBA/starcatalogs/raw/hygv35/res2/' # Path of the raw starcatalog
+>>> dir_from_raw = '/Volumes/TOSHIBA/starcatalogs/raw/hygv35/res5/' # Path of the raw starcatalog
 >>> hygv35_raw = StarCatalog.load(dir_from_raw)
->>> # dir_from_reduced = '/Volumes/TOSHIBA/starcatalogs/reduced/hygv35/res2/' # Path of the reduced starcatalog
+>>> # dir_from_reduced = '/Volumes/TOSHIBA/starcatalogs/reduced/hygv35/res5/' # Path of the reduced starcatalog
 >>> # hygv35_reduced = StarCatalog.load(dir_from_reduced)
 ```
 
 #### Load the simplified star catalog
 
 ```python
 >>> from starcatalogquery import StarCatalog
->>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag8.0/epoch2023.0/' # Path of the starcatalog
+>>> dir_from_simplified = '/Volumes/TOSHIBA/starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/' # Path of the starcatalog
 >>> hygv35_simplified = StarCatalog.load(dir_from_simplified)
 ```
 
 ## Change log
 
+- **0.1.9 — Jul 22, 2023**
+  
+  - Adjusted the strategy for dividing the celestial sphere into multiple equal-area sky regions using the HEALPix algorithm, as well as the corresponding radius of cone search used for blind matching of star maps.
+
 - **0.1.8 — Jul 03, 2023**
   
   - Get rid of dependency on **pyshtools**
     - Added function `from_cap` to replace `pysh.SHGrid.from_cap` in *catalog_query.py*
     - Using `SphericalCircle` in *astropy* to replace `MakeCircleCoord` in *pyshtools.utils* 
 
 - **0.1.7 — Jun 16, 2023**
```

## Comparing `starcatalogquery-0.1.8.dist-info/RECORD` & `starcatalogquery-0.1.9.dist-info/RECORD`

 * *Files 7% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 starcatalogquery/__init__.py,sha256=F5XhiD_gjaRsVVK_KfSD9ZkmgQnoNiJQqIMoMsceHRY,33
 starcatalogquery/catalog_check.py,sha256=GIjZgERg7Q6qhwyfzHOxut95KjmJGwq-M0SJVUFMLY8,6049
 starcatalogquery/catalog_download.py,sha256=sy316_xRn5CBVsqQAYmXSOSXx5bvBaU9Ewmwxt24vOM,6727
 starcatalogquery/catalog_query.py,sha256=HOilEP_Xyxo9BRDW06gFfu1YgyIO60FZinOBy1bIfDg,16654
-starcatalogquery/classes.py,sha256=ZL5ImjCW2p8Xo05gHXHgqNMJjdzs9iZt7Z4llf1K57s,51269
+starcatalogquery/classes.py,sha256=Af_XqANH3ISI0B8JXB342J2edgSR_Dm5H_dTK0lJdIo,50509
 starcatalogquery/invariantfeatures.py,sha256=iJG2K3R4BcbAqkX0I-P0nQYR4Xeo2UpPaQuEqx4CP58,3078
 starcatalogquery/tiles_draw.py,sha256=GGFtw8GNY67eTS-RzOG_RH-amS0wjlm8Dx844LblYXI,5684
 starcatalogquery/wcs.py,sha256=gtHOyg7Y51Icc3uAfA_uX3YznXqYbhtSKwVDcO1gIcg,1978
 starcatalogquery/utils/__init__.py,sha256=AbpHGcgLb-kRsJGnwFEktk7uzpZOCcBY74-YBdrKVGs,1
 starcatalogquery/utils/df2info.py,sha256=_eQENb_DxX5Q5EGxbanJuo9nQKBm-A6Tz8pEsLFinxI,612
 starcatalogquery/utils/starcatalog_statistic.py,sha256=LSjhB0jEsxzZmkXcB7NoVDXOorWB71DAPYg1HWWUREQ,4274
-starcatalogquery/utils/try_download.py,sha256=cTfNaevU_ELwKP3R9SpYQsiGtEvoBETnsi__EdkLSVE,477
-starcatalogquery-0.1.8.dist-info/LICENSE,sha256=1mo8gGwn9nEfzoruoWYAD1ttN40DofMYGQNef1rsytY,1068
-starcatalogquery-0.1.8.dist-info/METADATA,sha256=JdBIPuVw2qAhdBr2tYdwf2_wo1NseYgqZ4lAmk6OC9k,12582
-starcatalogquery-0.1.8.dist-info/WHEEL,sha256=ewwEueio1C2XeHTvT17n8dZUJgOvyCWCt0WVNLClP9o,92
-starcatalogquery-0.1.8.dist-info/top_level.txt,sha256=xZmWsZTK993L9eaiWI9PM0exXZiKw-64leh_79J2M9U,17
-starcatalogquery-0.1.8.dist-info/RECORD,,
+starcatalogquery/utils/try_download.py,sha256=y9pJKNuJuSR9YOJOneUEDii6rkASSizthKU7BIu5Hn4,467
+starcatalogquery-0.1.9.dist-info/LICENSE,sha256=1mo8gGwn9nEfzoruoWYAD1ttN40DofMYGQNef1rsytY,1068
+starcatalogquery-0.1.9.dist-info/METADATA,sha256=UKw376_2VCJdhBmtz4T9zodx5p-f_c57yuVXa84n3qM,12920
+starcatalogquery-0.1.9.dist-info/WHEEL,sha256=ewwEueio1C2XeHTvT17n8dZUJgOvyCWCt0WVNLClP9o,92
+starcatalogquery-0.1.9.dist-info/top_level.txt,sha256=xZmWsZTK993L9eaiWI9PM0exXZiKw-64leh_79J2M9U,17
+starcatalogquery-0.1.9.dist-info/RECORD,,
```

