# Comparing `tmp/starmatch-0.1.1-py3-none-any.whl.zip` & `tmp/starmatch-0.1.2-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,15 +1,15 @@
-Zip file size: 31322 bytes, number of entries: 13
+Zip file size: 31735 bytes, number of entries: 13
 -rw-r--r--  2.0 unx       41 b- defN 23-May-30 10:47 starmatch/__init__.py
 -rw-r--r--  2.0 unx    22310 b- defN 23-Jun-12 11:07 starmatch/astroalign.py
--rw-r--r--  2.0 unx    41872 b- defN 23-Jun-16 03:10 starmatch/classes.py
--rw-r--r--  2.0 unx     5958 b- defN 23-Jun-12 13:07 starmatch/orientation.py
--rw-r--r--  2.0 unx     3078 b- defN 23-Jun-12 11:33 starmatch/plot.py
+-rw-r--r--  2.0 unx    43275 b- defN 23-Jul-23 14:23 starmatch/classes.py
+-rw-r--r--  2.0 unx     6455 b- defN 23-Jul-23 14:18 starmatch/orientation.py
+-rw-r--r--  2.0 unx     3098 b- defN 23-Jul-14 09:12 starmatch/plot.py
 -rw-r--r--  2.0 unx     1976 b- defN 23-Jun-12 11:32 starmatch/wcs.py
 -rw-r--r--  2.0 unx        0 b- defN 23-May-30 11:01 starmatch/distortion/__init__.py
 -rw-r--r--  2.0 unx    11236 b- defN 23-Jun-15 03:24 starmatch/distortion/distortion_model.py
--rw-r--r--  2.0 unx     1068 b- defN 23-Jun-19 06:35 starmatch-0.1.1.dist-info/LICENSE
--rw-r--r--  2.0 unx    24093 b- defN 23-Jun-19 06:35 starmatch-0.1.1.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jun-19 06:35 starmatch-0.1.1.dist-info/WHEEL
--rw-r--r--  2.0 unx       10 b- defN 23-Jun-19 06:35 starmatch-0.1.1.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1044 b- defN 23-Jun-19 06:35 starmatch-0.1.1.dist-info/RECORD
-13 files, 112778 bytes uncompressed, 29588 bytes compressed:  73.8%
+-rw-r--r--  2.0 unx     1068 b- defN 23-Jul-23 14:33 starmatch-0.1.2.dist-info/LICENSE
+-rw-r--r--  2.0 unx    24634 b- defN 23-Jul-23 14:33 starmatch-0.1.2.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 14:33 starmatch-0.1.2.dist-info/WHEEL
+-rw-r--r--  2.0 unx       10 b- defN 23-Jul-23 14:33 starmatch-0.1.2.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx     1044 b- defN 23-Jul-23 14:33 starmatch-0.1.2.dist-info/RECORD
+13 files, 115239 bytes uncompressed, 30001 bytes compressed:  74.0%
```

## zipnote {}

```diff
@@ -18,23 +18,23 @@
 
 Filename: starmatch/distortion/__init__.py
 Comment: 
 
 Filename: starmatch/distortion/distortion_model.py
 Comment: 
 
-Filename: starmatch-0.1.1.dist-info/LICENSE
+Filename: starmatch-0.1.2.dist-info/LICENSE
 Comment: 
 
-Filename: starmatch-0.1.1.dist-info/METADATA
+Filename: starmatch-0.1.2.dist-info/METADATA
 Comment: 
 
-Filename: starmatch-0.1.1.dist-info/WHEEL
+Filename: starmatch-0.1.2.dist-info/WHEEL
 Comment: 
 
-Filename: starmatch-0.1.1.dist-info/top_level.txt
+Filename: starmatch-0.1.2.dist-info/top_level.txt
 Comment: 
 
-Filename: starmatch-0.1.1.dist-info/RECORD
+Filename: starmatch-0.1.2.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## starmatch/classes.py

```diff
@@ -1,19 +1,38 @@
 import numpy as np
 from numpy.linalg import norm
 from scipy.spatial import KDTree
 import matplotlib.pyplot as plt
 from matplotlib.ticker import MaxNLocator
 import GPy,copy
+from pathlib import Path
 
 from .orientation import get_orientation,get_orientation_mp
 from .astroalign import invariantfeatures,find_transform_tree,matrix_transform
 from .distortion import distortion_model
 from .plot import show_image
 
+def solidangle_ratio(fov,r):
+    """
+    Calculate the ratio of the solid angles spanned by the square and the cone.
+
+    Usage:
+        >>> ratio = Solid_angles_ratio(8,10)
+    Inputs:
+        fov -> [float] FOV of a camera in [deg] that determines a square
+        r -> [float] Angular radius in [deg] that determines a cone
+    Outputs:
+        ratio -> [float] The ratio of the solid angles spanned by the square and the cone    
+    """
+    fov_rad = np.deg2rad(fov)
+    r_rad = np.deg2rad(r)
+    Omega_square = 4*np.arcsin(np.tan(fov_rad/2)**2) # solid angles spanned by the square
+    Omega_cone = 4*np.pi*np.sin(r_rad/2)**2 # solid angles spanned by the cone
+    return Omega_square/Omega_cone
+
 def radec_res_rms(wcs,xy,catalog_df):
     """
     1. Given the WCS transformation, convert the pixel coordinates of stars to celestial coordinates.
     2. Compare cthe calculated celestial coordinates with those in star catalog, then compute the residual and RMS of Ra and Dec components respectively.
 
     Usage:
         >>> radec_res,radec_rms = radec_res_rms(wcs,xy,catalog_df)
@@ -48,60 +67,81 @@
         for key in info.keys():
             setattr(self, key, info[key])
 
     def __repr__(self):
     
         return self._description
 
+    def to_csv(self,path_catalog=None):
+        """
+        Save catalog_df to a csv file.
+
+        Usage:
+            >>> path_catalog = sources.affine_results.to_csv()
+            >>> path_catalog = sources.match_results.to_csv(path_catalog)
+            >>> path_catalog = sources.calibrate_results.to_csv(path_catalog)
+
+        Inputs:
+            path_catalog -> [str,optional,default=None] Path to save the csv file
+
+        Outputs:
+            path_catalog -> [str] Path of the csv file    
+        """
+        df = self.catalog_df
+
+        if path_catalog is None: path_catalog = 'csv/starmatch.csv' 
+        Path(path_catalog).parent.mkdir(parents=True, exist_ok=True)
+        df.to_csv(path_catalog) # Save the pandas dataframe to a csv-formatted file    
+
+        return path_catalog
+
 class StarMatch(object):
     """
     Class StarMatch, mainly used to generate an instance of class Sources as an entrance to star map matching and astronomical calibration.
     """
 
     def from_sources(xy_raw,flux_raw,camera_params,max_control_points=20,distortion=None):
         """
         Generate an instance of class Sources using pixel coordinates and flux(grayscale value) of sources, as is the entrance to star map matching and astronomical calibration.
 
         Usage:
             >>> # Example 1: No distortion is considered
             >>> from starmatch import StarMatch
             >>> # set the FOV[deg], pixel width[deg], resolution of the camera
-            >>> camera_params = {'fov':10,'pixel_width':0.01,'res':(1024,1024)}
+            >>> camera_params = {'fov':8,'pixel_width':0.01,'res':(1024,1024)}
             >>> # We use the first 20 points to compute the triangle invariants involved in affine transformation. 
             >>> # Usually these points are those sources that are brightest.
             >>> sources1 = StarMatch.from_sources(xy,flux,camera_params,20) # No distortion corrected 
             >>>
             >>> # Example 2: 'Brown–Conrady' distortion is considered
             >>> from starmatch.classes import Distortion
             >>> from starmatch import StarMatch
             >>> model = 'Brown–Conrady'
             >>> coeffs = [[-1e-4,1e-4],[1e-3,1e-3,1e-4,1e-5]]
             >>> dc = [0.1,0.1]
             >>> distortion_scale = 128
             >>> distortion = Distortion(model,coeffs,dc,distortion_scale)
             >>> sources2 = StarMatch.from_sources(xy,flux,camera_params,20,distortion)
-
         Inputs:
             xy_raw -> [2d array] Pixel coordinates of sources
             flux_raw -> [array] Flux(Grayscale value) of sources
-            camera_params -> [dict] The necessary parameters of the camera, such as {'fov':10,'pixel_width':0.01,'res':(1024,1024)}
+            camera_params -> [dict] The necessary parameters of the camera, such as {'fov':8,'pixel_width':0.01,'res':(1024,1024)}
             where 'fov' and 'pixel_width' are in [deg], and 'res' represents the resolution of the camera.
             max_control_points -> [int,optional,default=20] Maximum number of sources used to execute the star map matching
             distortion -> Instance of class Distortion, which defines the distortion model
-
         Outputs:
             sources -> Instance of class Sources, which includes the following attributes:
                 xy_raw -> [2d array, n*2] Pixel coordinates of sources
                 flux_raw -> [array] Flux(Grayscale value) of sources
                 xy -> [2d array, n*2] Pixel coordinates of sources truncated by max_control_points
                 flux -> [array] Flux(Grayscale value) of sources truncated by max_control_points
                 invariants -> [2d array, n*2] Array of (L2/L1,L1/L0), where L2 >= L1 >= L0 are the three sides of the triangle composed of sources.
                 asterisms -> [2d array n*3] Array of the indices of sources that correspond to each invariant triangle.
                 kdtree -> [Instance of class scipy.spatial.KDTree] 2d-tree for quick nearest-neighbor lookup
-                max_control_points -> [int,optional,default=20] Maximum number of sources used to execute the star map matching
+                max_control_points -> [int] Maximum number of sources used to execute the star map matching
                 _fov -> [float] Camera field of view in [deg]
                 _pixel_width -> [float] Camera pixel size in [deg]
                 _res -> [tuple of int] Camera resolution
         Note:
             When truncated by max_control_points, the sources need to be sorted from largest to smallest according to their fulx in advance.        
         """
         fov,pixel_width,res = camera_params['fov'],camera_params['pixel_width'],camera_params['res']
@@ -129,15 +169,15 @@
         - xy_raw -> [2d array(n*2)] Pixel coordinates of sources
         - flux_raw -> [array] Flux(Grayscale value) of sources
         - xy -> [2d array(n*2)] Pixel coordinates of sources truncated by max_control_points
         - flux -> [array] Flux(Grayscale value) of sources truncated by max_control_points
         - invariants -> [2d array(m*2)] Array of (L2/L1,L1/L0), where L2 >= L1 >= L0 are the three sides of the triangle composed of sources.
         - asterisms -> [2d array(m*3)] Array of the indices of sources that correspond to invariant triangles.
         - kdtree -> [Instance of class scipy.spatial.KDTree] 2d-tree of triangel invariants for quick nearest-neighbor lookup
-        - max_control_points -> [int,optional,default=20] Maximum number of sources used to execute the star map matching
+        - max_control_points -> [int] Maximum number of sources used to execute the star map matching
         - _fov -> [float] Field of View of camera in [deg]
         - _pixel_width -> [float] Pixel width of camera in [deg]
         - _res -> [tuple of int] Resolution of camera
         - _wcs -> object of class WCS, which defines the projection relationship between pixel coordinates and celestial coordinates
         - fp_radec_affine -> [array] Center pointing for affine transformations
         - affine_matrix -> [2d array] Affine matrix in form of [[λcosα,λsinα,λtx],[−λsinα,λcosα,λty],[0,0,1]]
         - _affine_translation -> [array] Affine translation in form of [tx,ty]
@@ -230,66 +270,63 @@
             invariants,asterisms,kdtree = invariantfeatures(xy)
 
             self.info.update({'xy':xy,'invariants':invariants,'asterisms':asterisms,'kdtree':kdtree,'max_control_points':max_control_points})
             self.xy,self.invariants,self.asterisms,self.kdtree,self.max_control_points = xy,invariants,asterisms,kdtree,max_control_points
 
         return self   
 
-    def center_pointing(self,catalogfile_h5):
+    def center_pointing(self,simplified_catalog,max_control_points=30):
         """
-        Estimate the center pointing of the camera through blind matching over star maps.
+        Estimate the center pointing and pixel width of the camera through blind matching over star maps.
 
         Usage:
-            >>> # The following star catalog index file can be genarated from the python package starcatalogquery, which can be installed by pip install starextractor. 
-            >>> # For more details, please refer to https://github.com/lcx366/STARQUERY.
-            >>> catalogfile_h5 = 'starcatalogs/indices/hygv3/fov10_mag9.0_mcp20_2022.0.h5'
-            >>> fp_radec = sources1.center_pointing(catalogfile_h5)
+            >>> fp_radec,pixel_width = sources1.center_pointing(simplified_catalog)
         Inputs:
-            catalogfile_h5 -> Star catalog index file in h5 format, which records the center pointing of each sky area, the pixel coordinates, the triangle invariants and the asterism indices of the stars.
+            simplified_catalog -> Instance of class StarCatalogSimplified
+            max_control_points -> [int,optional,default=30] Maxinum number of the stars sorted by brightness used for a sky area.
         Outputs:
-            fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in deg
-        Note:
-            The star catalog index file should be consistent with or close to the camera's field of view, detected star magnitude, and detected time.    
+            fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in [deg]  
+            pixel_width -> [float] Pixel width of camera in [deg]
         """
-        max_control_points = int(catalogfile_h5.split('mcp')[1].split('_')[0])    
-        self.invariantfeatures(max_control_points)
-        fp_radec = get_orientation(self.xy,self.asterisms,self.kdtree,self._pixel_width,catalogfile_h5)
 
-        return fp_radec
+        indices_h5,mcp_ratio = simplified_catalog.h5_incices(self._fov,self._pixel_width,max_control_points)
+        max_control_points = round(max_control_points*mcp_ratio)
+        self.invariantfeatures(max_control_points) 
+        fp_radec,pixel_width_estimate = get_orientation(self.xy,self.asterisms,self.kdtree,self._pixel_width,indices_h5)
+
+        return fp_radec,pixel_width_estimate
 
-    def center_pointing_mp(self,infile_h5):
+    def center_pointing_mp(self,simplified_catalog,max_control_points=30):
         """
         Estimate the center pointing of the camera through blind matching over star maps with the multi-core parallel computing.
 
         Usage:
-            >>> # The following star catalog index file can be genarated from the python package starcatalogquery, which can be installed by pip install starextractor. 
-            >>> # For more details, please refer to https://github.com/lcx366/STARQUERY.
-            >>> catalogfile_h5 = 'starcatalogs/indices/hygv3/fov10_mag9.0_mcp20_2022.0.h5'
-            >>> fp_radec = sources1.center_pointing_mp(catalogfile_h5)
+            >>> fp_radec,pixel_width = sources1.center_pointing_mp(simplified_catalog)
         Inputs:
-            catalogfile_h5 -> Star catalog index file in h5 format, which records the center pointing of each sky area, the pixel coordinates, the triangle invariants and the asterism indices of the stars.
+            simplified_catalog -> Instance of class StarCatalogSimplified
+            max_control_points -> [int,optional,default=30] Maxinum number of the stars sorted by brightness used for a sky area.
         Outputs:
-            fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in deg
-        Note:
-            The star catalog index file should be consistent with or close to the camera's field of view, detected star magnitude, and detected time.  
+            fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in [deg]  
+            pixel_width -> [float] Pixel width of camera in [deg]
         """
-        max_control_points = int(infile_h5.split('mcp')[1].split('_')[0])    
+        indices_h5,mcp_ratio = simplified_catalog.h5_incices(self._fov,self._pixel_width,max_control_points)
+        max_control_points = round(max_control_points*mcp_ratio)  
         self.invariantfeatures(max_control_points)
-        fp_radec = get_orientation_mp(self.xy,self.asterisms,self.kdtree,self._pixel_width,infile_h5)
+        fp_radec,pixel_width_estimate = get_orientation_mp(self.xy,self.asterisms,self.kdtree,self._pixel_width,indices_h5)
 
-        return fp_radec    
+        return fp_radec,pixel_width_estimate
 
     def align(self,fp_radec,simplified_catalog,L=32,calibrate=False):
         """
         Given the approximate center pointing of the camera, find the mapping model between the source image and the star map. 
         The mapping model includes two types: the affine model without considering the geometric distortion and the affine model + distortion model.
         Usage:
             >>> # Example 1: with no distortion on pixel coordinates of sources
             >>> from starmatch import StarMatch
-            >>> camera_params = {'fov':10,'pixel_width':0.01,'res':(1024,1024)}
+            >>> camera_params = {'fov':8,'pixel_width':0.01,'res':(1024,1024)}
             >>> sources1 = StarMatch.from_sources(xy,flux,camera_params)
             >>> # Load the simplified star catalog
             >>> from starcatalogquery import StarCatalog
             >>> dir_from_simplified = 'starcatalogs/simplified/hygv3/res5/mag9.0/epoch2022.0/'
             >>> hygv3_simplified = StarCatalog.load('simplified','hygv3',5,dir_from_simplified)
             >>> # star map matching
             >>> fp_radec = [202,31] # [Ra,Dec] in [deg]
@@ -307,19 +344,21 @@
             For example, if we set the tolerance to 0.2(default), it means the difference within 0.2*32=6.4 for pixel coordinates and 0.2 for magnitude is the correct matching, 
             Another use is associated with the GPR-baed distortion correction. Experience has shown that normalizing the pixel coordinates by L is beneficial to the operation of GPR.
             calibrate -> [bool,optional,default=False] Whether to perform a distortion correction. If False, no distortion correction is applied. If True, the distortion correction will be employed using the nonparametric Gaussian Process Regression(GPR) method.
         Outputs:
             updated self      
         """
         fov,pixel_width,res = self._fov,self._pixel_width,self._res
-        max_control_points = self.max_control_points
+        search_radius = 0.75*fov
+        ratio = solidangle_ratio(fov,search_radius)
+
+        max_control_points = int(self.max_control_points/ratio)
         pixels_camera,flux_camera = self.xy,self.flux
 
         # Query Star Catalog around the fiducial point.
-        search_radius = 0.6*fov
         stars = simplified_catalog.search_cone(fp_radec,search_radius,max_control_points)
         stars.pixel_xy(pixel_width) # Calculate the pixel coordinates of stars
         stars.invariantfeatures() # Calculate the triangle invariants and constructs a 2D Tree of stars; and records the asterism indices for each triangle.
         wcs = stars.wcs # Object of WCS transformation
 
         # Align sources from the camera and from the star catalog
         camera_tuple = (self.xy,self.asterisms,self.kdtree)
@@ -382,16 +421,16 @@
         dict_keys = 'xy','xy_res','xy_rms','mag_res','mag_rms','C','C_sigma','catalog_df','_description','pixels_camera_match','radec_res','radec_rms'
         info_affine_results = dict(zip(dict_keys, dict_values))
         affine_results = Constructor(info_affine_results)
         self.info['affine_results'] = affine_results
         self.affine_results = affine_results
 
         # Basic results for affine transformation
-        dict_values = wcs,fp_radec_affine,affine_matrix,affine_translation,affine_rotation,affine_scale,L
-        dict_keys = '_wcs','fp_radec_affine','affine_matrix','_affine_translation','_affine_rotation','_affine_scale','_L'
+        dict_values = wcs,fp_radec_affine,affine_matrix,affine_translation,affine_rotation,affine_scale,L,pixel_width,fov
+        dict_keys = '_wcs','fp_radec_affine','affine_matrix','_affine_translation','_affine_rotation','_affine_scale','_L','_pixel_width','_fov'
         info_update = dict(zip(dict_keys, dict_values))
         self.info.update(info_update)
         self._wcs = wcs
         self.fp_radec_affine = fp_radec_affine
         self.affine_matrix = affine_matrix
         self._affine_translation = affine_translation
         self._affine_rotation = affine_rotation
@@ -449,14 +488,20 @@
         dict_values = xy,xy_res,xy_rms,mag_res,mag_rms,C,C_sigma,catalog_df,description,pixels_camera_match,radec_res,radec_rms
         dict_keys = 'xy','xy_res','xy_rms','mag_res','mag_rms','C','C_sigma','catalog_df','_description','pixels_camera_match','radec_res','radec_rms'
         info_match_results = dict(zip(dict_keys, dict_values))
         match_results = Constructor(info_match_results)
         self.info['match_results'] = match_results
         self.match_results = match_results
 
+        pixel_width_estimate = pixel_width*affine_scale
+        fov_estimate = pixel_width_estimate * self._res
+        self.pixel_width_estimate = pixel_width_estimate
+        self.fov_estimate = fov_estimate
+        self.info.update(dict(zip(['pixel_width_estimate','fov_estmate'],[pixel_width_estimate,fov_estimate])))
+
         # Distortion correction
         if calibrate:
             # Normalize the coordinates
             xy_L = xy/L
             U_L = xy_res[:,0][:,None]/L
             V_L = xy_res[:,1][:,None]/L
 
@@ -632,15 +677,15 @@
 
             plt.subplots_adjust(wspace=0.3)
         
         if fig_file is None:
             plt.show() 
         else:
             Path(fig_file).parent.mkdir(parents=True, exist_ok=True)
-            plt.savefig(fig_file)      
+            plt.savefig(fig_file,bbox_inches='tight')      
 
     def show_starmatch(self,image_raw,offset,fig_out=None):
         """
         Mark the matching stars on the original image
 
         Usage:
             sources1.show_starmatch(self,image_raw,offset)
@@ -800,8 +845,8 @@
         vx,vy = vx_/ratio,vy_/ratio
 
         ax.quiver(X,Y,vx.reshape(X.shape),vy.reshape(Y.shape),color="C0") # scale=20
         ax.set_aspect('equal', adjustable='box')
         ax.yaxis.set_major_locator(MaxNLocator(integer=True))
         ax.xaxis.set_major_locator(MaxNLocator(integer=True))
         ax.tick_params(axis='both', which='major', labelsize=7)
-        plt.show()
+        plt.show()
```

## starmatch/orientation.py

```diff
@@ -3,24 +3,25 @@
 from colorama import Fore
 
 from .astroalign import find_transform_tree,matrix_transform
 from .wcs import wcs_trans
       
 def get_orientation(camera_xy,camera_asterisms,camera_invariant_tree,pixel_width,catalogfile_h5):
     """
-    Obtain the center pointing of the camera through blind matching of star maps.
+    Obtain the center pointing and pixel width of the camera through blind matching of star maps.
 
     Inputs:
         camera_xy -> [2d array, n*2] Pixel coordinates of sources in camera.
         camera_asterisms -> [2d array, m*3] Array of the indices of sources that correspond to each invariant triangle.
         camera_invariant_tree -> [Instance of class scipy.spatial.KDTree] 2d-tree constructed from array of (L2/L1,L1/L0), where L2 >= L1 >= L0 are the three sides of the triangle composed of sources.
         pixel_width -> [float] Pixel size in deg, such as 0.01
         catalogfile_h5 -> Star catalog index file in h5 format, which records the center pointing of each sky area, the pixel coordinates, the triangle invariants and the asterism indices of the stars.
     Outputs:
-        fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in deg
+        fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in [deg]
+        pixel_width_estimate -> [float] Pixel width of camera in [deg]
     """
 
     # Read the star catalog index file
     fp_radecs,stars_xy,stars_invariants,stars_asterisms = StarCatalog.read_h5_indices(catalogfile_h5)
 
     camera = (camera_xy,camera_asterisms,camera_invariant_tree)
 
@@ -38,32 +39,36 @@
             transf, (pixels_camera_match, pixels_catalog_match),_s,_d = find_transform_tree(camera, stars)
             # Roughly calibrate the center pointing of the camera
             pixels_cc_affine = matrix_transform([0,0],transf.params)  
             pixels_cc_affine_x,pixels_cc_affine_y = pixels_cc_affine[:,0],pixels_cc_affine[:,1]
             wcs = wcs_trans(pixel_width,fp_radecs[i])
             cc_radec_estimate = wcs.pixel_to_world(pixels_cc_affine_x,pixels_cc_affine_y)
             fp_radec = fp_ra,fp_dec = cc_radec_estimate.ra.deg[0],cc_radec_estimate.dec.deg[0]
+            pixel_width_estimate = pixel_width * transf.scale
             break
         except:
-            continue   
+            fp_radec,pixel_width_estimate = None,None
+            continue
+    print('')        
 
-    return fp_radec  
+    return fp_radec,pixel_width_estimate 
 
 def get_orientation_mp(camera_xy,camera_asterisms,camera_invariant_tree,pixel_width,catalogfile_h5):
     """
-    Obtain the center pointing of the camera through blind matching of star maps with the multi-core parallel computing.
+    Obtain the center pointing and pixel width of the camera through blind matching of star maps with the multi-core parallel computing.
 
     Inputs:
         camera_xy -> [2d array, n*2] Pixel coordinates of sources in camera.
         camera_asterisms -> [2d array, m*3] Array of the indices of sources that correspond to each invariant triangle.
         camera_invariant_tree -> [Instance of class scipy.spatial.KDTree] 2d-tree constructed from array of (L2/L1,L1/L0), where L2 >= L1 >= L0 are the three sides of the triangle composed of sources.
         pixel_width -> [float] Pixel size in deg, such as 0.01
         catalogfile_h5 -> Star catalog index file in h5 format, which records the center pointing of each sky area, the pixel coordinates, the triangle invariants and the asterism indices of the stars.
     Outputs:
         fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in deg
+        pixel_width_estimate -> [float] Pixel width of camera in [deg]
     """
     import multiprocessing as mp
     from functools import partial
 
     # set the number of feasible cores
     number_of_cores = mp.cpu_count() - 1
     
@@ -91,16 +96,16 @@
     """
     Accompanying function for get_orientation_mp.
 
     Inputs:
         params -> Parameters that do not need to be allocated to multiple cores
         arg -> Variables that need to be allocated to multiple cores
     Outputs:  
-        fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in deg
-
+        fp_radec -> [tuple of float] Center pointing of the camera in form of [Ra,Dec] in [deg]
+        pixel_width_estimate -> [float] Pixel width of camera in [deg]
     """
     camera_xy,camera_asterisms,camera_invariant_tree,pixel_width = params
     camera = (camera_xy,camera_asterisms,camera_invariant_tree)
     fp_radecs_i,stars_xy_i,stars_asterisms_i,stars_invariants_i = arg
 
     ra_c,dec_c = fp_radecs_i
     catalog_xy = stars_xy_i
@@ -113,10 +118,12 @@
         transf, (pixels_camera_match, pixels_catalog_match),_s,_d = find_transform_tree(camera,stars)
         # Roughly calibrate the center pointing of the camera
         pixels_cc_affine = matrix_transform([0,0],transf.params)  
         pixels_cc_affine_x,pixels_cc_affine_y = pixels_cc_affine[:,0],pixels_cc_affine[:,1]
         wcs = wcs_trans(pixel_width,fp_radecs_i)
         cc_radec_estimate = wcs.pixel_to_world(pixels_cc_affine_x,pixels_cc_affine_y)
         fp_radec = fp_ra,fp_dec = cc_radec_estimate.ra.deg[0],cc_radec_estimate.dec.deg[0]
+        pixel_width_estimate = pixel_width * transf.scale
+        res = (fp_radec,pixel_width_estimate)
     except:
-        fp_radec = None
-    return fp_radec
+        res = None
+    return res
```

## starmatch/plot.py

```diff
@@ -64,12 +64,12 @@
     if mask_rectangle is not None:
         lb_bb,width,height = mask_rectangle
         ax.add_patch(Rectangle(lb_bb, width, height,fill=False,lw=1,color='r',ls='dashdot'))   
 
     if 'figname' in kwargs: 
         fig_file = kwargs['figname']
         Path(fig_file).parent.mkdir(parents=True, exist_ok=True)
-        plt.savefig(fig_file) 
+        plt.savefig(fig_file,bbox_inches='tight') 
     else:
         plt.show()
             
     plt.close()
```

## Comparing `starmatch-0.1.1.dist-info/LICENSE` & `starmatch-0.1.2.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `starmatch-0.1.1.dist-info/METADATA` & `starmatch-0.1.2.dist-info/METADATA`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: starmatch
-Version: 0.1.1
+Version: 0.1.2
 Summary: A package to handle the Star map matching and astronomical positioning
 Home-page: https://github.com/lcx366/STARMATCH
 Author: Chunxiao Li
 Author-email: lcx366@126.com
 License: MIT
 Keywords: Star Map Matching,Astronomical positioning,Distortion Correction,pointing calibration
 Classifier: Development Status :: 4 - Beta
@@ -88,46 +88,46 @@
 1. [Distortion_(optics)](https://en.wikipedia.org/wiki/Distortion_(optics))
 2. [imatest distortion-methods](https://www.imatest.com/docs/distortion-methods-and-modules/)
 3. [imatest distortion-models](https://www.imatest.com/support/docs/pre-5-2/geometric-calibration-deprecated/distortion-models/) 
 
 ##### Construct a Standard Radial Distortion Model
 
 ```python
-from starmatch.classes import Distortion
-model = 'RadialStandard' # Type of distortion model
-coeffs = [-1e-4,1e-4] # Coefficients of 5th order SRDM in form of [k1,k2]
-dc = [0.1,0.1] # Pixel coordinates of the distortion center
-distortion_scale = 128 # The length scale of the distortion model, that is, the number of pixels per unit length
-distortion = Distortion(model,coeffs,dc,distortion_scale) # Establish a distortion model
+>>> from starmatch.classes import Distortion
+>>> model = 'RadialStandard' # Type of distortion model
+>>> coeffs = [-1e-4,1e-4] # Coefficients of 5th order SRDM in form of [k1,k2]
+>>> dc = [0.1,0.1] # Pixel coordinates of the distortion center
+>>> distortion_scale = 128 # The length scale of the distortion model, that is, the number of pixels per unit length
+>>> distortion = Distortion(model,coeffs,dc,distortion_scale) # Establish a distortion model
 ```
 
 ##### Compute the distortion-corrected pixel coordinates
 
 ```python
-pixels_xy = [367,125]
-pixels_XY = distortion.apply(pixels_xy)
-print(pixels_XY)
-#Calculate the distortion-corrected pixel coordinates at normalized scale
-#pixels_xy = [[2.8671875, 0.9765625], [1.109375, -0.875]]
-#pixel_scale = 128
-#pixels_XY  = distortion.apply(pixels_xy,pixel_scale)
-#print(pixels_XY)
+>>> pixels_xy = [367,125]
+>>> pixels_XY = distortion.apply(pixels_xy)
+>>> print(pixels_XY)
+>>> #Calculate the distortion-corrected pixel coordinates at normalized scale
+>>> #pixels_xy = [[2.8671875, 0.9765625], [1.109375, -0.875]]
+>>> #pixel_scale = 128
+>>> #pixels_XY  = distortion.apply(pixels_xy,pixel_scale)
+>>> #print(pixels_XY)
 ```
 
     [[369.21610677 125.70199655]]
 
 ##### Sketch the vector plot of distortion
 
 ```python
-xlim,ylim = 512,512
-distortion.sketchmap(xlim,ylim)
-#For normalized pixel coordinates
-#xlim,ylim = 4,4
-#pixel_scale = 128
-#distortion.sketchmap(xlim,ylim,pixel_scale)
+>>> xlim,ylim = 512,512
+>>> distortion.sketchmap(xlim,ylim)
+>>> #For normalized pixel coordinates
+>>> #xlim,ylim = 4,4
+>>> #pixel_scale = 128
+>>> #distortion.sketchmap(xlim,ylim,pixel_scale)
 ```
 
 <p align="middle">
   <img src="readme_figs/output_8_1.png" width="500" />
 </p>
 
 #### Example: Division-mode Radial Distortion Model(DRDM)
@@ -138,46 +138,46 @@
 - The 4th order polynomial in division form: $r_u = r_d /(1+ k_1 * r_d^2 + k_2 * r_d^4)$
 
 Basic formulas for DRDM are same as that for SRDM.
 
 ##### Construct a Division-mode Radial Distortion Model
 
 ```python
-from starmatch.classes import Distortion
-model = 'RadialDivision' # Type of distortion model
-coeffs = [-1e-4,1e-4] # Coefficients of 4th order DRDM in form of [k1,k2]
-dc = [0.1,0.1] # Pixel coordinates of the distortion center
-distortion_scale = 128 # The length scale of the distortion model, that is, the number of pixels per unit length
-distortion = Distortion(model,coeffs,dc,distortion_scale) # Establish a distortion model
+>>> from starmatch.classes import Distortion
+>>> model = 'RadialDivision' # Type of distortion model
+>>> coeffs = [-1e-4,1e-4] # Coefficients of 4th order DRDM in form of [k1,k2]
+>>> dc = [0.1,0.1] # Pixel coordinates of the distortion center
+>>> distortion_scale = 128 # The length scale of the distortion model, that is, the number of pixels per unit length
+>>> distortion = Distortion(model,coeffs,dc,distortion_scale) # Establish a distortion model
 ```
 
 ##### Compute the distortion-corrected pixel coordinates
 
 ```python
-pixels_xy = [367,125]
-pixels_XY = distortion.apply(pixels_xy)
-print(pixels_XY)
-#Calculate the distortion-corrected pixel coordinates at normalized scale
-#pixels_xy = [[2.8671875, 0.9765625], [1.109375, -0.875]]
-#pixel_scale = 128
-#pixels_XY  = distortion.apply(pixels_xy,pixel_scale)
-#print(pixels_XY)
+>>> pixels_xy = [367,125]
+>>> pixels_XY = distortion.apply(pixels_xy)
+>>> print(pixels_XY)
+>>> #Calculate the distortion-corrected pixel coordinates at normalized scale
+>>> #pixels_xy = [[2.8671875, 0.9765625], [1.109375, -0.875]]
+>>> #pixel_scale = 128
+>>> #pixels_XY  = distortion.apply(pixels_xy,pixel_scale)
+>>> #print(pixels_XY)
 ```
 
     [[364.79767243 124.30236829]]
 
 ##### Sketch the vector plot of distortion
 
 ```python
-xlim,ylim = 512,512
-distortion.sketchmap(xlim,ylim)
-#For normalized pixel coordinates
-#xlim,ylim = 4,4
-#pixel_scale = 128
-#distortion.sketchmap(xlim,ylim,pixel_scale)
+>>> xlim,ylim = 512,512
+>>> distortion.sketchmap(xlim,ylim)
+>>> #For normalized pixel coordinates
+>>> #xlim,ylim = 4,4
+>>> #pixel_scale = 128
+>>> #distortion.sketchmap(xlim,ylim,pixel_scale)
 ```
 
 <p align="middle">
   <img src="readme_figs/output_15_1.png" width="500" />
 </p>
 
 #### Example: Tangential Distortion Model(TDM)
@@ -189,46 +189,46 @@
 $x_u = x_d + (P_1 * (r_d^2 + 2*(x_d-x_c)^2) + 2*P_2 * (x_d-x_c)*(y_d-y_c))*(1 + P_3 * r_d^2 + P_4*r_d^4 + ...)$
 
 $y_u = y_d + (P_2 * (r_d^2 + 2*(y_d-y_c)^2) + 2*P_1 * (x_d-x_c)*(y_d-y_c))*(1 + P_3 * r_d^2 + P_4*r_d^4 + ...)$
 
 ##### Construct a Tangential Distortion Model
 
 ```python
-from starmatch.classes import Distortion
-model = 'Tangential' # Type of distortion model
-coeffs = [-1e-4,1e-4] # Coefficients of 2nd order SRDM in form of [P1,P2]
-dc = [0.1,0.1] # Pixel coordinates of the distortion center
-distortion_scale = 128 # The length scale of the distortion model, that is, the number of pixels per unit length
-distortion = Distortion(model,coeffs,dc,distortion_scale) # Establish a distortion model
+>>> from starmatch.classes import Distortion
+>>> model = 'Tangential' # Type of distortion model
+>>> coeffs = [-1e-4,1e-4] # Coefficients of 2nd order SRDM in form of [P1,P2]
+>>> dc = [0.1,0.1] # Pixel coordinates of the distortion center
+>>> distortion_scale = 128 # The length scale of the distortion model, that is, the number of pixels per unit length
+>>> distortion = Distortion(model,coeffs,dc,distortion_scale) # Establish a distortion model
 ```
 
 ##### Compute the distortion-corrected pixel coordinates
 
 ```python
-pixels_xy = [367,125]
-pixels_XY = distortion.apply(pixels_xy)
-print(pixels_XY)
-#Calculate the distortion-corrected pixel coordinates at normalized scale
-#pixels_xy = [[2.8671875, 0.9765625], [1.109375, -0.875]]
-#pixel_scale = 128
-#pixels_XY  = distortion.apply(pixels_xy,pixel_scale)
-#print(pixels_XY)
+>>> pixels_xy = [367,125]
+>>> pixels_XY = distortion.apply(pixels_xy)
+>>> print(pixels_XY)
+>>> #Calculate the distortion-corrected pixel coordinates at normalized scale
+>>> #pixels_xy = [[2.8671875, 0.9765625], [1.109375, -0.875]]
+>>> #pixel_scale = 128
+>>> #pixels_XY  = distortion.apply(pixels_xy,pixel_scale)
+>>> #print(pixels_XY)
 ```
 
     [[366.75821931 125.06542319]]
 
 ##### Sketch the vector plot of distortion
 
 ```python
-xlim,ylim = 512,512
-distortion.sketchmap(xlim,ylim)
-#For normalized pixel coordinates
-#xlim,ylim = 4,4
-#pixel_scale = 128
-#distortion.sketchmap(xlim,ylim,pixel_scale)
+>>> xlim,ylim = 512,512
+>>> distortion.sketchmap(xlim,ylim)
+>>> #For normalized pixel coordinates
+>>> #xlim,ylim = 4,4
+>>> #pixel_scale = 128
+>>> #distortion.sketchmap(xlim,ylim,pixel_scale)
 ```
 
 <p align="middle">
   <img src="readme_figs/output_22_1.png" width="500" />
 </p>
 
 #### Example: Brown–Conrady Distortion Model(BCDM)
@@ -240,46 +240,46 @@
 $x_u = x_d + (x_d - x_c) * (K_1*r_d^2 + K_2*r_d^4 + ...) + (P_1 * (r_d^2 + 2*(x_d-x_c)^2) + 2*P_2 * (x_d-x_c)*(y_d-y_c))*(1 + P_3*r_d^2 + P_4*r_d^4 + ...)$
 
 $y_u = y_d + (y_d - x_c) * (K_1*r_d^2 + K_2*r_d^4 + ...) + (P_2 * (r_d^2 + 2*(y_d-y_c)^2) + 2*P_1 * (x_d-x_c)*(y_d-y_c))*(1 + P_3*r_d^2 + P_4*r+d^4 + ...)$
 
 ##### Construct a Brown–Conrady Distortion Model
 
 ```python
-from starmatch.classes import Distortion
-model = 'Brown–Conrady' # Type of distortion model
-coeffs = [[-1e-4,1e-4],[1e-3,1e-3,1e-4,1e-5]] # Coefficients of Brown–Conrady distortion model in form of [[coeffs_radial],[coeffs_tangential]]
-dc = [0.1,0.1] # Pixel coordinates of the distortion center
-distortion_scale = 128 # The length scale of the distortion model, that is, the number of pixels per unit length
-distortion = Distortion(model,coeffs,dc,distortion_scale) # Establish a distortion model
+>>> from starmatch.classes import Distortion
+>>> model = 'Brown–Conrady' # Type of distortion model
+>>> coeffs = [[-1e-4,1e-4],[1e-3,1e-3,1e-4,1e-5]] # Coefficients of Brown–Conrady distortion model in form of [[coeffs_radial],[coeffs_tangential]]
+>>> dc = [0.1,0.1] # Pixel coordinates of the distortion center
+>>> distortion_scale = 128 # The length scale of the distortion model, that is, the number of pixels per unit length
+>>> distortion = Distortion(model,coeffs,dc,distortion_scale) # Establish a distortion model
 ```
 
 ### Compute the distortion-corrected pixel coordinates
 
 ```python
-pixels_xy = [367,125]
-pixels_XY = distortion.apply(pixels_xy)
-print(pixels_XY)
-#Calculate the distortion-corrected pixel coordinates at normalized scale
-#pixels_xy = [[2.8671875, 0.9765625], [1.109375, -0.875]]
-#pixel_scale = 128
-#pixels_XY  = distortion.apply(pixels_xy,pixel_scale)
-#print(pixels_XY)
+>>> pixels_xy = [367,125]
+>>> pixels_XY = distortion.apply(pixels_xy)
+>>> print(pixels_XY)
+>>> #Calculate the distortion-corrected pixel coordinates at normalized scale
+>>> #pixels_xy = [[2.8671875, 0.9765625], [1.109375, -0.875]]
+>>> #pixel_scale = 128
+>>> #pixels_XY  = distortion.apply(pixels_xy,pixel_scale)
+>>> #print(pixels_XY)
 ```
 
     [[372.88150908 127.60108593]]
 
 ##### Sketch the vector plot of distortion
 
 ```python
-xlim,ylim = 512,512
-distortion.sketchmap(xlim,ylim)
-#For normalized pixel coordinates
-#xlim,ylim = 4,4
-#pixel_scale = 128
-#distortion.sketchmap(xlim,ylim,pixel_scale)
+>>> xlim,ylim = 512,512
+>>> distortion.sketchmap(xlim,ylim)
+>>> #For normalized pixel coordinates
+>>> #xlim,ylim = 4,4
+>>> #pixel_scale = 128
+>>> #distortion.sketchmap(xlim,ylim,pixel_scale)
 ```
 
 <p align="middle">
   <img src="readme_figs/output_29_1.png" width="500" />
 </p>
 
 ### Prelude to star map matching
@@ -287,32 +287,32 @@
 Ahead of star map matching, a set of star catalog index files should be genarated using the python package starcatalogquery, which can be installed by `pip install starcatalogquery`. For more details, please refer to [STARQUERY](https://github.com/lcx366/STARQUERY).
 
 #### Extract sources from images
 
 We use the python package `starextractor` to complete the source extraction, which can be installed by `pip install starextractor`. For more details, please refer to [STAREXTRACTOR](https://github.com/lcx366/STAREXTRACTOR).
 
 ```python
-from starextractor import AstroImage
-imagefile = 'obs/fits/img_00000.fits' #imagefile = 'obs/bmp/img_00000.bmp'
-image = AstroImage.read_image(imagefile)
-sources = image.find_source(fwhm=14,mask=False)
-xy,flux = sources.xy,sources.brightness
+>>> from starextractor import AstroImage
+>>> imagefile = 'obs/fits/img_00000.fits' #imagefile = 'obs/bmp/img_00000.bmp'
+>>> image = AstroImage.read_image(imagefile)
+>>> sources = image.find_source(fwhm=14,mask=False)
+>>> xy,flux = sources.xy,sources.brightness
 ```
 
 Generate an object of `Sources` using pixel coordinates and flux(grayscale value) of sources, as is the entrance to star map matching and astronomical calibration.
 
 #### Load the sources to StarMatch
 
 ```python
-from starmatch import StarMatch
-# set the FOV[deg], pixel width[deg], resolution of the camera
-camera_params = {'fov':10,'pixel_width':0.01,'res':(1024,1024)}
-# We use the first 20 points to compute the triangle invariants involved in affine transformation. 
-# Usually these points are those sources that are brightest.
-sources1 = StarMatch.from_sources(xy,flux,camera_params,20) # No distortion corrected 
+>>> from starmatch import StarMatch
+>>> # set the FOV[deg], pixel width[deg], resolution of the camera
+>>> camera_params = {'fov':8,'pixel_width':0.01,'res':(1024,1024)}
+>>> # We use the first 20 points to compute the triangle invariants involved in affine transformation. 
+>>> # Usually these points are those sources that are brightest.
+>>> sources1 = StarMatch.from_sources(xy,flux,camera_params,20) # No distortion corrected 
 ```
 
 We get an object `sources1`  with
 
 ```
 Attributes:
     - xy_raw -> Pixel coordinates of sources
@@ -324,57 +324,52 @@
     - kdtree -> 2d-tree of triangel invariants for quick nearest-neighbor lookup
     - max_control_points -> Maximum number of sources used to execute the star map matching
     - _fov -> Field of View of camera in [deg]
     - _pixel_width -> Pixel width of camera in [deg]
     - _res -> Resolution of camera
 ```
 
-#### Estimate the center pointing of the camera
-
-We use the HYG v3.5 star catalog(Thanks to [David Nash](https://www.astronexus.com/hyg)) to genarate the h5-format index file according to the camera parameters(field of view, detected magnitude, observation time) with the python package starcatalogquery, which can be installed by `pip install starcatalogquery`. The h5-format index file records the center pointing of each sky area, the pixel coordinates, the triangle invariants and the asterism indices of the stars.
+### Star Map Matching
 
-##### Blind matching over star maps
+Load the simplified HYG v3.5 star catalog.
 
 ```python
-catalogfile_h5 = 'starcatalogs/indices/hygv35/fov10_mag9.0_mcp20_2022.0.h5'
-fp_radec = sources1.center_pointing(catalogfile_h5)
-print(fp_radec)
+>>> from starcatalogquery import StarCatalog
+>>> # The following starcatalog path stores the tile files with size of 5 deg, stars magnitude less than 9.0, and proper motion correction to epoch of 2022.0.
+>>> dir_from_simplified = 'starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
+>>> hygv35_simplified = StarCatalog.load(dir_from_simplified)
 ```
 
-    (204.01793337608683, 36.24740259697955)
+#### Estimate the center pointing of the camera
 
-##### Blind matching over star maps with the multi-core parallel computing
+We use the HYG v3.5 star catalog(Thanks to [David Nash](https://www.astronexus.com/hyg)) to genarate the h5-format index file according to the camera parameters(field of view, detected magnitude, observation time) with the python package starcatalogquery, which can be installed by `pip install starcatalogquery`. The h5-format index file records the center pointing of each sky area, the pixel coordinates, the triangle invariants and the asterism indices of the stars.
+
+##### Blind matching over star maps
 
 ```python
-catalogfile_h5 = 'starcatalogs/indices/hygv35/fov10_mag9.0_mcp20_2022.0.h5'
-fp_radec = sources1.center_pointing_mp(catalogfile_h5)
-print(fp_radec) # (Ra,Dec) in [deg]
+>>> fp_radec,pixel_width_estimate = sources1.center_pointing(hygv35_simplified)
+>>> print(fp_radec,pixel_width_estimate) # (Ra,Dec) in [deg], pixel width in [deg]
+>>> #fov = pixel_width_estimate * sources1._res
 ```
 
-    (204.01793337608683, 36.24740259697955)
-
-### Star Map Matching
-
-Load the simplified HYG v3.5 star catalog.
+##### Blind matching over star maps with the multi-core parallel computing
 
 ```python
-from starcatalogquery import StarCatalog
-# The following starcatalog path stores the tile files with size of 5 deg, stars magnitude less than 9.0, and proper motion correction to epoch of 2022.0.
-dir_from_simplified = 'starcatalogs/simplified/hygv35/res5/mag9.0/epoch2022.0/'
-hygv35_simplified = StarCatalog.load(dir_from_simplified)
+>>> fp_radec,pixel_width_estimate = sources1.center_pointing_mp(hygv35_simplified)
+>>> print(fp_radec,pixel_width_estimate) 
 ```
 
 The actual center pointing of the camera is (204.01706216087143, 36.25274704575726), in order to test the tolerance ability of star map matching, we set the pointing point to [200,30]. 
 
 Note: in process of star map matching, we set **L**(default=32) as the normalized length scale, namely, number of pixels in a unit length. It controls the tolerance of the 3D-Tree composed of (x,y,mag) of sources from camera and stars from catalog. For example, if the tolerance is set to 0.2(default), it means the difference within 0.2\*32=6.4 for pixel coordinates and 0.2 for magnitude is regarded as the correct matching.
 Another use of L is associated with the GPR(Gaussian Process Regression)-based distortion correction bellow. Experience has shown that normalizing the pixel coordinates by L is beneficial to the operation of GPR.
 
 ```python
-fp_radec = [201,31]
-sources1.align(fp_radec,hygv35_simplified,L=32)
+>>> fp_radec = [201,31]
+>>> sources1.align(fp_radec,hygv35_simplified,L=32)
 ```
 
     Instance of class Sources
 
 We get object `sources1` updated with new attributes added:
 
 ```
@@ -425,17 +420,17 @@
 - 'dmag', mag of stars - mag of sources affined
 - 'x_camera', x of sources
 - 'y_camera', y of sources
 
 #### Show the matching stars on map
 
 ```python
-image_raw = sources.image_raw
-offset = sources.offset
-sources1.show_starmatch(image_raw,offset)
+>>> image_raw = sources.image_raw
+>>> offset = sources.offset
+>>> sources1.show_starmatch(image_raw,offset)
 ```
 
 <p align="middle">
   <img src="readme_figs/output_52_0.png" width="500" />
 </p>
 
 The asterisks on the graph are consistent with the `catalog_df`.
@@ -443,62 +438,62 @@
 <p align="middle">
   <img src="readme_figs/catalog_df.png" width="700" />
 </p>
 
 ### Calibrate the orientation of the camera center
 
 ```python
-sources1.fp_calibrate()
-print(sources1.fp_radec_calibrated)
-# [[204.01747112  36.25112389]]
-# Calibration from Astrometry.net is (13h 36m 04.207s,+36° 15' 03.012")
+>>> sources1.fp_calibrate()
+>>> print(sources1.fp_radec_calibrated)
+>>> # [[204.01747112  36.25112389]]
+>>> # Calibration from Astrometry.net is (13h 36m 04.207s,+36° 15' 03.012")
 ```
 
     [[204.01738012  36.25118506]]
 
 ### Astronomical Positioning and Apparent Magnitude Estimation
 
 Estimate the celestial coordinates and magnitudes of unknown targets.
 
 ```python
-xy_target,flux_target = [345,678],1e3 # [[345,678],[-278,521]],[1e3,2e4]
-radec,M_affine,M_match = sources1.apply(xy_target,flux_target)
-print(radec,M_affine,M_match)
-print(sources1.affine_results.mag_rms,sources1.match_results.mag_rms)
+>>> xy_target,flux_target = [345,678],1e3 # [[345,678],[-278,521]],[1e3,2e4]
+>>> radec,M_affine,M_match = sources1.apply(xy_target,flux_target)
+>>> print(radec,M_affine,M_match)
+>>> print(sources1.affine_results.mag_rms,sources1.match_results.mag_rms)
 ```
 
     [[199.83995525  31.44951982]] 8.036101294387004 8.011023843192229
     0.08052914228287848 0.10371476611720697
 
 ### Star Map Matching with geometric distortion considered
 
 #### Add distortion to raw sources
 
 Here, we add a Standard Radial distortion to raw sources to obtain distorted sources.
 
 ```python
-from starmatch.classes import Distortion
-distortion = Distortion('RadialStandard',[1e-3,-1e-3],[0.1,0.1],256)
-xy_distorted = distortion.apply(sources.xy,pixel_scale=1)
+>>> from starmatch.classes import Distortion
+>>> distortion = Distortion('RadialStandard',[1e-3,-1e-3],[0.1,0.1],256)
+>>> xy_distorted = distortion.apply(sources.xy,pixel_scale=1)
 ```
 
 #### Load the distorted sources to StarMatch
 
 Theoretically, for distorted images, a corresponding distortion correction model is usually provided. However, when the distortion model is unknown, we use the non-parametric Gaussian Process Regression(GPR) method to fit the distortion and obtain a non-parametric distortion model.
 
 ```python
-# The following `distortion_correction_model` is the inverse of `distortion`, and the inverse transformation of the distortion model is not yet implemented.
-# sources2 = StarMatch.from_sources(xy_distorted,flux,camera_params,20,distortion_correction_model)
-sources2 = StarMatch.from_sources(xy_distorted,flux,camera_params,20)
+>>> # The following `distortion_correction_model` is the inverse of `distortion`, and the inverse transformation of the distortion model is not yet implemented.
+>>> # sources2 = StarMatch.from_sources(xy_distorted,flux,camera_params,20,distortion_correction_model)
+>>> sources2 = StarMatch.from_sources(xy_distorted,flux,camera_params,20)
 ```
 
 #### Star Map Matching
 
 ```python
-sources2.align(fp_radec,hygv35_simplified,L=32,calibrate=True) 
+>>> sources2.align(fp_radec,hygv35_simplified,L=32,calibrate=True) 
 ```
 
     Instance of class Sources
 
 We get object `sources2` updated with new attributes added:
 
 ```
@@ -524,37 +519,40 @@
 Show the distortion of the camera in modes of vector or contourf.
 
 ##### Vector plot
 
 The vector plot shows the distortion where the sources are located.
 
 ```python
-sources2.show_distortion('vector')
+>>> sources2.show_distortion('vector')
 ```
 
 <p align="middle">
   <img src="readme_figs/output_70_1.png" width="500" />
 </p>
 
 ##### Contour plot
 
 The following contour plot shows the distortion in the x and y directions, respectively.
 
 ```python
-sources2.show_distortion('contourf')
+>>> sources2.show_distortion('contourf')
 ```
 
 <p align="middle">
   <img src="readme_figs/output_73_1.png" width="800" />
 </p>
 
 ## Change log
 
-- **0.1.0 — Jun 16, 2023**
-  
+- **0.1.2 — Jul 23, 2023**
+  - Simplified the use of blind matching.
+  - Added pixel width and field of view estimates for blind matching.
+
+- **0.1.1 — Jun 16, 2023**
   - The ***starmatch*** package was released.
 
 ## Next release
 
 - Add contour plot of distortion models
 - Add aberration and light time correction
 - Find the inverse transformation of distortion models
```

## Comparing `starmatch-0.1.1.dist-info/RECORD` & `starmatch-0.1.2.dist-info/RECORD`

 * *Files 23% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 starmatch/__init__.py,sha256=X6X6VU1p7jv_4VfSAC5ATlNPi_tD4T2vQwwOgcnpaPA,41
 starmatch/astroalign.py,sha256=OymKBKAHvw7_IvlC4mpnTYnQKg987sh0g7TGO17GgYg,22310
-starmatch/classes.py,sha256=Dshs0hnoRCf-zA6Rnqoxa5w7S1TSvbM-h2cPJHrJj-Y,41872
-starmatch/orientation.py,sha256=DRkmfMEd4n8eeqG1daIuN_-5pXunIdLgrglt0wprkL4,5958
-starmatch/plot.py,sha256=K9BIOSlRT7gcO-oiix-4vFwKnTUwNMrBDU8epDa40RE,3078
+starmatch/classes.py,sha256=KbXjyq6Ivfjhtn2PKnQgVzrhFEdlHo4SE91qLOnLMEs,43275
+starmatch/orientation.py,sha256=Ibb4jK6Lj4SG4qpPM0m6Z6k4WFtUCR7xzkb0HgwfDTA,6455
+starmatch/plot.py,sha256=sGB3Ek3iKwYRrEdXqhz7aY1kqoWRUfVTzpeyh4xZOII,3098
 starmatch/wcs.py,sha256=jq5mmLYtXeVbdL7MuBTUEQnwX-FuTn_jcU7KqMaHYOA,1976
 starmatch/distortion/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 starmatch/distortion/distortion_model.py,sha256=bZ05MifpnbIuHE_eVa-0XErwpmZZ_rVZC9QDmmQWQds,11236
-starmatch-0.1.1.dist-info/LICENSE,sha256=1mo8gGwn9nEfzoruoWYAD1ttN40DofMYGQNef1rsytY,1068
-starmatch-0.1.1.dist-info/METADATA,sha256=VTXp45OVukPFI4HRn11BJxAuMZyc38h-tZu0jPa6X5s,24093
-starmatch-0.1.1.dist-info/WHEEL,sha256=ewwEueio1C2XeHTvT17n8dZUJgOvyCWCt0WVNLClP9o,92
-starmatch-0.1.1.dist-info/top_level.txt,sha256=yxZNa5SKsmUHcbN_hI9Aa5_mi6QfdMxAorjQUYkiMiA,10
-starmatch-0.1.1.dist-info/RECORD,,
+starmatch-0.1.2.dist-info/LICENSE,sha256=1mo8gGwn9nEfzoruoWYAD1ttN40DofMYGQNef1rsytY,1068
+starmatch-0.1.2.dist-info/METADATA,sha256=Mb3dHvkjzD4sNkRGBxAXQhlFKSUO5xBjq0vEPayM5EM,24634
+starmatch-0.1.2.dist-info/WHEEL,sha256=ewwEueio1C2XeHTvT17n8dZUJgOvyCWCt0WVNLClP9o,92
+starmatch-0.1.2.dist-info/top_level.txt,sha256=yxZNa5SKsmUHcbN_hI9Aa5_mi6QfdMxAorjQUYkiMiA,10
+starmatch-0.1.2.dist-info/RECORD,,
```

