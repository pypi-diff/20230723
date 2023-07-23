# Comparing `tmp/ktch-0.3.0.tar.gz` & `tmp/ktch-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ktch-0.3.0.tar", max compression
+gzip compressed data, was "ktch-0.3.1.tar", max compression
```

## Comparing `ktch-0.3.0.tar` & `ktch-0.3.1.tar`

### file list

```diff
@@ -1,35 +1,35 @@
--rw-r--r--   0        0        0    11356 2023-06-23 03:21:23.404492 ktch-0.3.0/LICENSE
--rw-r--r--   0        0        0      350 2023-06-26 04:27:07.675589 ktch-0.3.0/README.md
--rw-r--r--   0        0        0      864 2023-07-02 16:48:19.809070 ktch-0.3.0/ktch/__init__.py
--rw-r--r--   0        0        0      661 2023-06-27 10:00:20.339645 ktch-0.3.0/ktch/datasets/__init__.py
--rw-r--r--   0        0        0    11067 2023-07-01 04:29:50.150850 ktch-0.3.0/ktch/datasets/_base.py
--rw-r--r--   0        0        0     2974 2023-06-28 00:54:07.102190 ktch-0.3.0/ktch/datasets/_sample_generator.py
--rw-r--r--   0        0        0        0 2023-06-23 03:21:39.664617 ktch-0.3.0/ktch/datasets/data/__init__.py
--rw-r--r--   0        0        0    46290 2023-06-23 03:21:39.535438 ktch-0.3.0/ktch/datasets/data/data_landmark_mosquito_wings.csv
--rw-r--r--   0        0        0    88299 2023-06-23 03:21:39.553325 ktch-0.3.0/ktch/datasets/data/data_outline_bottles.csv
--rw-r--r--   0        0        0   285403 2023-06-23 03:21:39.537674 ktch-0.3.0/ktch/datasets/data/data_outline_mosquito_wings.csv
--rw-r--r--   0        0        0      799 2023-06-23 03:21:39.538090 ktch-0.3.0/ktch/datasets/data/meta_landmark_mosquito_wings.csv
--rw-r--r--   0        0        0      846 2023-06-23 03:21:39.553737 ktch-0.3.0/ktch/datasets/data/meta_outline_bottles.csv
--rw-r--r--   0        0        0      792 2023-06-23 03:21:39.701830 ktch-0.3.0/ktch/datasets/data/meta_outline_mosquito_wings.csv
--rw-r--r--   0        0        0    18006 2023-06-23 03:21:39.554248 ktch-0.3.0/ktch/datasets/data/test_coef_nharm_6_norm_false_outline_bottles.csv
--rw-r--r--   0        0        0    17900 2023-06-23 03:21:39.554771 ktch-0.3.0/ktch/datasets/data/test_coef_nharm_6_norm_true_outline_bottles.csv
--rw-r--r--   0        0        0        0 2023-06-23 03:21:39.664691 ktch-0.3.0/ktch/datasets/descr/__init__.py
--rw-r--r--   0        0        0       71 2023-06-23 03:21:39.538419 ktch-0.3.0/ktch/datasets/descr/data_landmark_mosquito_wings.rst
--rw-r--r--   0        0        0       68 2023-06-23 03:21:39.555073 ktch-0.3.0/ktch/datasets/descr/data_outline_bottles.rst
--rw-r--r--   0        0        0       68 2023-06-23 03:21:39.538754 ktch-0.3.0/ktch/datasets/descr/data_outline_mosquito_wings.rst
--rw-r--r--   0        0        0      746 2023-06-28 09:51:49.737612 ktch-0.3.0/ktch/io/__init__.py
--rw-r--r--   0        0        0     9697 2023-06-30 10:03:13.720872 ktch-0.3.0/ktch/io/_tps.py
--rw-r--r--   0        0        0     6075 2023-07-02 16:46:57.851454 ktch-0.3.0/ktch/landmark/_Procrustes_analysis.py
--rw-r--r--   0        0        0      835 2023-06-23 03:23:35.051862 ktch-0.3.0/ktch/landmark/__init__.py
--rw-r--r--   0        0        0     3992 2023-06-23 03:21:23.420003 ktch-0.3.0/ktch/landmark/_landmark.py
--rw-r--r--   0        0        0        0 2023-06-23 03:21:39.444203 ktch-0.3.0/ktch/landmark/tests/__init__.py
--rw-r--r--   0        0        0      793 2023-06-23 03:23:59.235815 ktch-0.3.0/ktch/motion/__init__.py
--rw-r--r--   0        0        0     1252 2023-07-01 05:21:21.330953 ktch-0.3.0/ktch/outline/__init__.py
--rw-r--r--   0        0        0    13480 2023-07-01 05:21:04.417578 ktch-0.3.0/ktch/outline/_elliptic_Fourier_analysis.py
--rw-r--r--   0        0        0      690 2023-07-02 16:46:57.852452 ktch-0.3.0/ktch/outline/_plot/reconstructed_shapes.py
--rw-r--r--   0        0        0    12956 2023-06-26 04:27:07.677178 ktch-0.3.0/ktch/outline/_spherical_harmonic_analysis.py
--rw-r--r--   0        0        0        0 2023-06-23 03:21:39.444317 ktch-0.3.0/ktch/outline/tests/__init__.py
--rw-r--r--   0        0        0     1763 2023-06-23 03:23:52.942126 ktch-0.3.0/ktch/outline/tests/test_elliptic_Fourier_analysis.py
--rw-r--r--   0        0        0        0 2021-07-21 14:32:32.343272 ktch-0.3.0/ktch/tests/__init__.py
--rw-r--r--   0        0        0     2370 2023-07-02 16:48:40.747870 ktch-0.3.0/pyproject.toml
--rw-r--r--   0        0        0     1654 1970-01-01 00:00:00.000000 ktch-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0    11356 2023-06-23 03:21:23.404492 ktch-0.3.1/LICENSE
+-rw-r--r--   0        0        0      400 2023-07-07 04:14:02.888693 ktch-0.3.1/README.md
+-rw-r--r--   0        0        0      864 2023-07-02 16:48:19.809070 ktch-0.3.1/ktch/__init__.py
+-rw-r--r--   0        0        0      661 2023-06-27 10:00:20.339645 ktch-0.3.1/ktch/datasets/__init__.py
+-rw-r--r--   0        0        0    11067 2023-07-01 04:29:50.150850 ktch-0.3.1/ktch/datasets/_base.py
+-rw-r--r--   0        0        0     2974 2023-06-28 00:54:07.102190 ktch-0.3.1/ktch/datasets/_sample_generator.py
+-rw-r--r--   0        0        0        0 2023-06-23 03:21:39.664617 ktch-0.3.1/ktch/datasets/data/__init__.py
+-rw-r--r--   0        0        0    46290 2023-06-23 03:21:39.535438 ktch-0.3.1/ktch/datasets/data/data_landmark_mosquito_wings.csv
+-rw-r--r--   0        0        0    88299 2023-06-23 03:21:39.553325 ktch-0.3.1/ktch/datasets/data/data_outline_bottles.csv
+-rw-r--r--   0        0        0   285403 2023-06-23 03:21:39.537674 ktch-0.3.1/ktch/datasets/data/data_outline_mosquito_wings.csv
+-rw-r--r--   0        0        0      799 2023-06-23 03:21:39.538090 ktch-0.3.1/ktch/datasets/data/meta_landmark_mosquito_wings.csv
+-rw-r--r--   0        0        0      846 2023-06-23 03:21:39.553737 ktch-0.3.1/ktch/datasets/data/meta_outline_bottles.csv
+-rw-r--r--   0        0        0      792 2023-06-23 03:21:39.701830 ktch-0.3.1/ktch/datasets/data/meta_outline_mosquito_wings.csv
+-rw-r--r--   0        0        0    18006 2023-06-23 03:21:39.554248 ktch-0.3.1/ktch/datasets/data/test_coef_nharm_6_norm_false_outline_bottles.csv
+-rw-r--r--   0        0        0    17900 2023-06-23 03:21:39.554771 ktch-0.3.1/ktch/datasets/data/test_coef_nharm_6_norm_true_outline_bottles.csv
+-rw-r--r--   0        0        0        0 2023-06-23 03:21:39.664691 ktch-0.3.1/ktch/datasets/descr/__init__.py
+-rw-r--r--   0        0        0       71 2023-06-23 03:21:39.538419 ktch-0.3.1/ktch/datasets/descr/data_landmark_mosquito_wings.rst
+-rw-r--r--   0        0        0       68 2023-06-23 03:21:39.555073 ktch-0.3.1/ktch/datasets/descr/data_outline_bottles.rst
+-rw-r--r--   0        0        0       68 2023-06-23 03:21:39.538754 ktch-0.3.1/ktch/datasets/descr/data_outline_mosquito_wings.rst
+-rw-r--r--   0        0        0      746 2023-06-28 09:51:49.737612 ktch-0.3.1/ktch/io/__init__.py
+-rw-r--r--   0        0        0    10625 2023-07-23 14:43:56.735725 ktch-0.3.1/ktch/io/_tps.py
+-rw-r--r--   0        0        0     7304 2023-07-23 07:27:54.658804 ktch-0.3.1/ktch/landmark/_Procrustes_analysis.py
+-rw-r--r--   0        0        0      835 2023-06-23 03:23:35.051862 ktch-0.3.1/ktch/landmark/__init__.py
+-rw-r--r--   0        0        0     3992 2023-06-23 03:21:23.420003 ktch-0.3.1/ktch/landmark/_landmark.py
+-rw-r--r--   0        0        0        0 2023-06-23 03:21:39.444203 ktch-0.3.1/ktch/landmark/tests/__init__.py
+-rw-r--r--   0        0        0      793 2023-06-23 03:23:59.235815 ktch-0.3.1/ktch/motion/__init__.py
+-rw-r--r--   0        0        0     1252 2023-07-01 05:21:21.330953 ktch-0.3.1/ktch/outline/__init__.py
+-rw-r--r--   0        0        0    13480 2023-07-01 05:21:04.417578 ktch-0.3.1/ktch/outline/_elliptic_Fourier_analysis.py
+-rw-r--r--   0        0        0      690 2023-07-03 02:18:44.724564 ktch-0.3.1/ktch/outline/_plot/reconstructed_shapes.py
+-rw-r--r--   0        0        0    12973 2023-07-07 02:49:45.189581 ktch-0.3.1/ktch/outline/_spherical_harmonic_analysis.py
+-rw-r--r--   0        0        0        0 2023-06-23 03:21:39.444317 ktch-0.3.1/ktch/outline/tests/__init__.py
+-rw-r--r--   0        0        0     1763 2023-06-23 03:23:52.942126 ktch-0.3.1/ktch/outline/tests/test_elliptic_Fourier_analysis.py
+-rw-r--r--   0        0        0        0 2021-07-21 14:32:32.343272 ktch-0.3.1/ktch/tests/__init__.py
+-rw-r--r--   0        0        0     2396 2023-07-23 15:05:49.515341 ktch-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0     1704 1970-01-01 00:00:00.000000 ktch-0.3.1/PKG-INFO
```

### Comparing `ktch-0.3.0/LICENSE` & `ktch-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/__init__.py` & `ktch-0.3.1/ktch/__init__.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/__init__.py` & `ktch-0.3.1/ktch/datasets/__init__.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/_base.py` & `ktch-0.3.1/ktch/datasets/_base.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/_sample_generator.py` & `ktch-0.3.1/ktch/datasets/_sample_generator.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/data/data_landmark_mosquito_wings.csv` & `ktch-0.3.1/ktch/datasets/data/data_landmark_mosquito_wings.csv`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/data/data_outline_bottles.csv` & `ktch-0.3.1/ktch/datasets/data/data_outline_bottles.csv`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/data/data_outline_mosquito_wings.csv` & `ktch-0.3.1/ktch/datasets/data/data_outline_mosquito_wings.csv`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/data/meta_landmark_mosquito_wings.csv` & `ktch-0.3.1/ktch/datasets/data/meta_landmark_mosquito_wings.csv`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/data/meta_outline_bottles.csv` & `ktch-0.3.1/ktch/datasets/data/meta_outline_bottles.csv`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/data/meta_outline_mosquito_wings.csv` & `ktch-0.3.1/ktch/datasets/data/meta_outline_mosquito_wings.csv`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/data/test_coef_nharm_6_norm_false_outline_bottles.csv` & `ktch-0.3.1/ktch/datasets/data/test_coef_nharm_6_norm_false_outline_bottles.csv`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/datasets/data/test_coef_nharm_6_norm_true_outline_bottles.csv` & `ktch-0.3.1/ktch/datasets/data/test_coef_nharm_6_norm_true_outline_bottles.csv`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/io/__init__.py` & `ktch-0.3.1/ktch/io/__init__.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/io/_tps.py` & `ktch-0.3.1/ktch/io/_tps.py`

 * *Files 10% similar despite different names*

```diff
@@ -50,19 +50,42 @@
     def to_numpy(self):
         if self.curves is None:
             return self.landmarks
         else:
             return self.landmarks, self.curves
 
     def to_dataframe(self):
+        if self.landmarks.shape[1] == 2:
+            columns = ["x", "y"]
+        elif self.landmarks.shape[1] == 3:
+            columns = ["x", "y", "z"]
+        else:
+            raise ValueError("n_dim must be 2 or 3.")
+
+        df_landmarks = pd.DataFrame(
+            self.landmarks,
+            columns=columns,
+            index=pd.MultiIndex.from_tuples(
+                [[self.idx, i] for i in range(len(self.landmarks))],
+                name=["specimen_id", "coord_id"],
+            ),
+        )
         if self.curves is None:
-            return pd.DataFrame(self.landmarks)
+            return df_landmarks
         else:
-            return pd.DataFrame(self.landmarks), [
-                pd.DataFrame(curve) for curve in self.curves
+            return df_landmarks, [
+                pd.DataFrame(
+                    curve,
+                    columns=columns,
+                    index=pd.MultiIndex.from_tuples(
+                        [[self.idx, i] for i in range(len(curve))],
+                        name=["specimen_id", "coord_id"],
+                    ),
+                )
+                for curve in self.curves
             ]
 
 
 ####################################
 # TPS I/O functions
 ####################################
 
@@ -70,14 +93,16 @@
 def read_tps(file_path, as_frame=False):
     """Read TPS file.
 
     Parameters
     ==========
     file_path : str
         Path to the TPS file.
+    as_frame : bool, default=False
+        If True, return pandas.DataFrame. Otherwise, return numpy.ndarray.
 
     Returns
     =======
     landmarks : ndarray
         Landmarks.
     semilandmarks: list[ndarray] or ndarray, optional
         Semilandmarks.
@@ -104,14 +129,15 @@
         if (semilandmark_flag == 0) or (semilandmark_flag == len(tps_data)):
             pass
         else:
             raise ValueError("Some specimens have semilandmarks and others do not.")
         if as_frame:
             if semilandmark_flag == 0:
                 landmarks = [tps_datum.to_dataframe() for tps_datum in tps_data]
+                landmarks = pd.concat(landmarks)
                 return landmarks
             else:
                 landmarks = [tps_datum.to_dataframe()[0] for tps_datum in tps_data]
 
                 semilandmarks = [tps_datum.to_dataframe()[1] for tps_datum in tps_data]
                 return landmarks, semilandmarks
         else:
```

### Comparing `ktch-0.3.0/ktch/landmark/_Procrustes_analysis.py` & `ktch-0.3.1/ktch/landmark/_Procrustes_analysis.py`

 * *Files 18% similar despite different names*

```diff
@@ -14,89 +14,135 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from abc import ABCMeta, abstractmethod
 
 import numpy as np
 import scipy as sp
+import pandas as pd
 
 import numpy.typing as npt
 
 
 from sklearn.base import (
     BaseEstimator,
     TransformerMixin,
-    ClassNamePrefixFeaturesOutMixin,
+    OneToOneFeatureMixin,
 )
 
 
 class GeneralizedProcrustesAnalysis(
-    ClassNamePrefixFeaturesOutMixin, TransformerMixin, BaseEstimator, metaclass=ABCMeta
+    OneToOneFeatureMixin,
+    TransformerMixin,
+    BaseEstimator,
+    metaclass=ABCMeta,
 ):
     r"""
     Generalized Procrustes Analysis (GPA)
 
     Parameters
     ------------
     tol: float, default=10^-7
         Torelance for convergence of Procrustes analysis.
+    n_dim: int, default=2
+        Dimensions of the configurations.
 
     Attributes
     ------------
     mu_: ndarray, shape (n_landmarks, n_dim)
         The mean shape of the aligned shapes.
+    n_dim_: int, 2 or 3
+        Dimensions of the configurations.
 
     Notes
     ------------
     GPA for shape involves translating, rotating, and scaling  the configurations to each other to minimize the sum of the squared distances with respect to positional, rotational, and size parameters, subject to a size constraint [Gower_1975]_, [Goodall_1991]_.
 
     GPA for size-and-shape
 
     References
     ------------
     .. [Gower_1975] Gower, J.C., 1975. Generalized procrustes analysis. Psychometrika 40, 33–51.
     .. [Goodall_1991] Goodall, C., 1991. Procrustes Methods in the Statistical Analysis of Shape. J Royal Statistical Soc Ser B Methodol 53, 285–321.
 
     """
 
-    def __init__(self, tol=10**-7, scaling=True, debug=False):
+    def __init__(self, tol=10**-7, scaling=True, n_dim=2, debug=False):
         self.tol = tol
         self.scaling = scaling
         self.debug = debug
         self.mu_ = None
+        self.n_dim_ = n_dim
+
+    @property
+    def n_dim(self):
+        return self.n_dim_
+
+    @n_dim.setter
+    def n_dim(self, n_dim):
+        if n_dim not in [2, 3]:
+            raise ValueError("n_dim must be 2 or 3.")
+        self.n_dim_ = n_dim
 
     def fit(self, X):
+        """Fit GPA.
+
+        Parameters
+        ----------
+        X : array-like, shape (n_specimens, n_landmarks, n_dim)
+            /DataFrame, shape (n_specimens, n_landmarks * n_dim)
+            Configurations to be aligned.
+
+        Returns
+        -------
+        self : object
+            Returns the instance itself.
+        """
+        self.n_features_in_ = X.shape[1]
+        if hasattr(X, "columns"):
+            self.feature_names_in_ = X.columns
+
         return self
 
-    def transform(self, X):
+    def transform(
+        self,
+        X: npt.ArrayLike,
+    ) -> npt.ArrayLike:
         """GPA for shapes/size-and-shapes.
 
         Parameters
         ----------
-        X : array-like, shape (n_shapes, n_landmarks, n_dim)
+        X : array-like, shape (n_specimens, n_landmarks*n_dim)
             Configurations to be aligned.
 
         scaling: bool, default=True
             If True, the configurations are aligned by translation, rotation, and scaling.
             If False, the configurations are aligned by translation and rotation.
 
         Returns
         -------
-        X_ : ndarray, shape (n_shapes, n_landmarks, n_dim)
+        X_ : ndarray, shape (n_specimens, n_landmarks, n_dim)
             Shapes/Size-and-Shape (aligned configurations)
         """
 
-        scaling = self.scaling
+        X_ = np.array(X)
+        n_specimen = len(X_)
+        n_dim = self.n_dim_
+        if len(X_[0]) % n_dim != 0:
+            raise ValueError("X must be n_specimens x n_landmarks*n_dim.")
+        n_landmarks = int(len(X_[0]) / n_dim)
+        X_ = X_.reshape(n_specimen, n_landmarks, n_dim)
 
+        scaling = self.scaling
         if scaling:
-            X_ = self._transform_shape(X)
+            X_ = self._transform_shape(X_)
         else:
-            X_ = self._transform_size_and_shape(X)
+            X_ = self._transform_size_and_shape(X_)
 
-        return X_
+        return X_.reshape(n_specimen, n_landmarks * n_dim)
 
     def _transform_shape(self, X):
         X_ = np.array(X, dtype=np.double, copy=True)
         X_ = self._center(X_)
         mu = np.sum(X_, axis=0) / len(X_)
         mu = mu / centroid_size(mu)
 
@@ -139,54 +185,47 @@
             mu = np.sum(X_, axis=0) / len(X_)
 
             if self.debug:
                 print("total_disp: ", total_disp, "diff_disp: ", diff_disp)
 
         self.mu_ = mu
 
-        return X_
+        return X_.reshape(self.n_specimen_, self.n_landmarks_ * self.n_dim_)
 
     def fit_transform(self, X):
-        return self.transform(X)
-
-    def _center(self, X):
-        X_centered = np.array([x - np.mean(x, axis=0) for x in X])
-        return X_centered
-
-    def _scale(self, X):
-        X_scaled = np.array([x / centroid_size(x) for x in X])
-        return X_scaled
-
-    def get_feature_names_out(
-        self, input_features: None | npt.ArrayLike = None
-    ) -> np.ndarray:
-        """Get output feature names.
+        """GPA for shapes/size-and-shapes.
 
         Parameters
         ----------
-        input_features : None | npt.ArrayLike, optional
-            Input feature names, by default None
+        X : array-like, shape (n_specimens, n_landmarks * n_dim)
+            /DataFrame, shape (n_specimens, n_landmarks * n_dim)
+            Configurations to be aligned.
 
         Returns
         -------
-        feature_names_out : ndarray of str objects
-            Transformed feature names.
+        X_ : ndarray, shape (n_specimens, n_landmarks, n_dim)
+            Shapes/Size-and-Shape (aligned configurations)
 
         """
-        # x
-        # y
-        # z
+        self.fit(X)
+        X_ = self.transform(X)
+        return X_
 
-        feature_names_out = np.asarray(xn + yn + zn, dtype=str)
-        return feature_names_out
+    def _center(self, X):
+        X_centered = np.array([x - np.mean(x, axis=0) for x in X])
+        return X_centered
 
-    @property
-    def _n_features_out(self):
-        """Number of transformed output features."""
-        return self.n_landmarks * self.n_dim
+    def _scale(self, X):
+        X_scaled = np.array([x / centroid_size(x) for x in X])
+        return X_scaled
+
+    # @property
+    # def _n_features_out(self):
+    #     """Number of transformed output features."""
+    #     return self.n_landmarks_ * self.n_dim_
 
 
 class LandmarkImputer(TransformerMixin, BaseEstimator):
     def __init__(self, missing_values=np.nan):
         pass
```

### Comparing `ktch-0.3.0/ktch/landmark/__init__.py` & `ktch-0.3.1/ktch/landmark/__init__.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/landmark/_landmark.py` & `ktch-0.3.1/ktch/landmark/_landmark.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/motion/__init__.py` & `ktch-0.3.1/ktch/motion/__init__.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/outline/__init__.py` & `ktch-0.3.1/ktch/outline/__init__.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/outline/_elliptic_Fourier_analysis.py` & `ktch-0.3.1/ktch/outline/_elliptic_Fourier_analysis.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/outline/_plot/reconstructed_shapes.py` & `ktch-0.3.1/ktch/outline/_plot/reconstructed_shapes.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/ktch/outline/_spherical_harmonic_analysis.py` & `ktch-0.3.1/ktch/outline/_spherical_harmonic_analysis.py`

 * *Files 0% similar despite different names*

```diff
@@ -434,15 +434,15 @@
 
             if l > len(self.coef):
                 raise ValueError(f"l must be less than {len(self.coef)}")
 
             if abs(m) > l:
                 raise ValueError(f"abs(m) must be less than {l}")
 
-            self.coef[l][l + m] = value
+            self.coef[l][-l + self.n_degree + m] = value
 
         elif type(lm) is int:
             l = lm
 
             if len(value) != 2 * l + 1:
                 raise ValueError(f"len(value) must be {2*l+1}")
```

### Comparing `ktch-0.3.0/ktch/outline/tests/test_elliptic_Fourier_analysis.py` & `ktch-0.3.1/ktch/outline/tests/test_elliptic_Fourier_analysis.py`

 * *Files identical despite different names*

### Comparing `ktch-0.3.0/pyproject.toml` & `ktch-0.3.1/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 description = "ktch is a python package for model-based morphometrics."
 homepage = "https://doc.ktch.dev"
 keywords = ["morphometrics", "theoretical morphology"]
 license = "Apache-2.0"
 name = "ktch"
 readme = "README.md"
 repository = "https://github.com/noshita/ktch"
-version = "0.3.0"
+version = "0.3.1"
 
 [tool.poetry.dependencies]
 numpy = "^1.22"
 pandas = "^1.4"
 python = ">= 3.8, < 3.12"
 scikit-learn = "^1.2"
 scipy = "^1.8"
@@ -66,14 +66,15 @@
 myst-nb = "^0.17.2"
 nbsphinx = "^0.9.2"
 numpydoc = "^1.4.0"
 pydata-sphinx-theme = "^0.12"
 sphinx = "^5.3"
 sphinx-autobuild = "^2021.3"
 sphinx-gallery = "^0.11"
+sphinx-sitemap = "^2.5.0"
 sphinxcontrib-bibtex = "^2.5"
 
 [build-system]
 build-backend = "poetry.core.masonry.api"
 requires = ["poetry-core>=1.0.0"]
 
 [tool.poetry2conda]
```

### Comparing `ktch-0.3.0/PKG-INFO` & `ktch-0.3.1/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ktch
-Version: 0.3.0
+Version: 0.3.1
 Summary: ktch is a python package for model-based morphometrics.
 Home-page: https://doc.ktch.dev
 License: Apache-2.0
 Keywords: morphometrics,theoretical morphology
 Author: Noshita, Koji
 Author-email: noshita@morphometrics.jp
 Requires-Python: >=3.8,<3.12
@@ -37,15 +37,19 @@
 [![codecov](https://codecov.io/gh/noshita/ktch/branch/main/graph/badge.svg?token=SJN66K7KJY)](https://codecov.io/gh/noshita/ktch)
 
 ktch is a python package for model-based morphometrics.
 
 ## Usage
 
 ```sh
+# pip
 pip install ktch
+
+# conda
+conda install -c conda-forge ktch 
 ```
 
 
 ## License
 
 ktch is licensed under the Apache License, Version2.0
```

