# Comparing `tmp/Connectome-Utilities-0.3.1.tar.gz` & `tmp/Connectome-Utilities-0.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Connectome-Utilities-0.3.1.tar", last modified: Fri Jun 30 11:43:18 2023, max compression
+gzip compressed data, was "Connectome-Utilities-0.3.2.tar", last modified: Sun Jul 23 15:55:47 2023, max compression
```

## Comparing `Connectome-Utilities-0.3.1.tar` & `Connectome-Utilities-0.3.2.tar`

### file list

```diff
@@ -1,61 +1,23 @@
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:18.442698 Connectome-Utilities-0.3.1/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)       77 2023-06-07 08:34:43.000000 Connectome-Utilities-0.3.1/AUTHORS.txt
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:17.788650 Connectome-Utilities-0.3.1/Connectome_Utilities.egg-info/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    19962 2023-06-30 11:43:17.000000 Connectome-Utilities-0.3.1/Connectome_Utilities.egg-info/PKG-INFO
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     2018 2023-06-30 11:43:17.000000 Connectome-Utilities-0.3.1/Connectome_Utilities.egg-info/SOURCES.txt
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)        1 2023-06-30 11:43:17.000000 Connectome-Utilities-0.3.1/Connectome_Utilities.egg-info/dependency_links.txt
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      145 2023-06-30 11:43:17.000000 Connectome-Utilities-0.3.1/Connectome_Utilities.egg-info/requires.txt
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)       11 2023-06-30 11:43:17.000000 Connectome-Utilities-0.3.1/Connectome_Utilities.egg-info/top_level.txt
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    11353 2023-06-07 11:54:58.000000 Connectome-Utilities-0.3.1/LICENSE
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    19962 2023-06-30 11:43:18.441699 Connectome-Utilities-0.3.1/PKG-INFO
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    19296 2023-06-30 11:34:22.000000 Connectome-Utilities-0.3.1/README.md
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:17.869781 Connectome-Utilities-0.3.1/conntility/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      259 2023-06-07 08:13:49.000000 Connectome-Utilities-0.3.1/conntility/__init__.py
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:17.928128 Connectome-Utilities-0.3.1/conntility/analysis/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      181 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/analysis/__init__.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     6514 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/analysis/analysis.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    11611 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/analysis/analysis_decorators.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     2305 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/analysis/clustering.py
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:17.960662 Connectome-Utilities-0.3.1/conntility/analysis/library/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)       83 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/analysis/library/__init__.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     3238 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/analysis/library/diffusion_mapping.py
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:18.020271 Connectome-Utilities-0.3.1/conntility/circuit_models/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      573 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/__init__.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    29632 2023-06-07 15:46:01.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/connection_matrix.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     4213 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/input_spikes.py
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:18.177213 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      495 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/__init__.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      402 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/defaults.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     5054 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/extra_properties.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     2269 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/from_atlas.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     5683 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/grouping_config.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     6223 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/loader.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     9112 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/make_groups.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     1967 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/sonata_extensions.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    17520 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/neuron_groups/tessellate.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     3441 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/circuit_models/sonata_helpers.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    78736 2023-06-08 09:06:49.000000 Connectome-Utilities-0.3.1/conntility/connectivity.py
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:18.268701 Connectome-Utilities-0.3.1/conntility/flatmapping/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      363 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/flatmapping/__init__.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     4917 2023-06-13 09:42:59.000000 Connectome-Utilities-0.3.1/conntility/flatmapping/_supersample_utility.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     4850 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/flatmapping/flatmap_utility.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     9522 2023-06-12 16:33:16.000000 Connectome-Utilities-0.3.1/conntility/flatmapping/supersampling.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     3387 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/flatmapping/wm_recipe_utility.py
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:18.310642 Connectome-Utilities-0.3.1/conntility/io/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      113 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/io/__init__.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     1519 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/io/logging.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     3026 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/io/sparse_matrices.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    10990 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/multi_scale.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     2743 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/plugins.py
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:18.322999 Connectome-Utilities-0.3.1/conntility/randomization/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)       38 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/randomization/__init__.py
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:18.355817 Connectome-Utilities-0.3.1/conntility/subcellular/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      116 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/subcellular/__init__.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)    11133 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/conntility/subcellular/neuron_morphology_path_distance.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     1105 2023-06-30 10:21:20.000000 Connectome-Utilities-0.3.1/pyproject.toml
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)       38 2023-06-30 11:43:18.443699 Connectome-Utilities-0.3.1/setup.cfg
-drwxrwxrwx   0 reimann   (1000) reimann   (1000)        0 2023-06-30 11:43:18.429644 Connectome-Utilities-0.3.1/tests/
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)      568 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/tests/test_analysis.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     3203 2023-06-07 08:15:28.000000 Connectome-Utilities-0.3.1/tests/test_analysis_decorator.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     7250 2023-06-09 14:26:32.000000 Connectome-Utilities-0.3.1/tests/test_connectivity_matrix.py
--rwxrwxrwx   0 reimann   (1000) reimann   (1000)     1348 2023-06-09 14:55:41.000000 Connectome-Utilities-0.3.1/tests/test_neuron_groups.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:55:47.775704 Connectome-Utilities-0.3.2/
+-rw-r--r--   0 runner    (1001) docker     (123)       77 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/AUTHORS.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:55:47.771704 Connectome-Utilities-0.3.2/Connectome_Utilities.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    19962 2023-07-23 15:55:47.000000 Connectome-Utilities-0.3.2/Connectome_Utilities.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      479 2023-07-23 15:55:47.000000 Connectome-Utilities-0.3.2/Connectome_Utilities.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:55:47.000000 Connectome-Utilities-0.3.2/Connectome_Utilities.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-07-23 15:55:47.000000 Connectome-Utilities-0.3.2/Connectome_Utilities.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-07-23 15:55:47.000000 Connectome-Utilities-0.3.2/Connectome_Utilities.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    11353 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    19962 2023-07-23 15:55:47.771704 Connectome-Utilities-0.3.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    19296 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:55:47.771704 Connectome-Utilities-0.3.2/conntility/
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/conntility/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)    83760 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/conntility/connectivity.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10990 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/conntility/multi_scale.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2743 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/conntility/plugins.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 15:55:47.775704 Connectome-Utilities-0.3.2/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:55:47.771704 Connectome-Utilities-0.3.2/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      568 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/tests/test_analysis.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3203 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/tests/test_analysis_decorator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7250 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/tests/test_connectivity_matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1348 2023-07-23 15:55:39.000000 Connectome-Utilities-0.3.2/tests/test_neuron_groups.py
```

### Comparing `Connectome-Utilities-0.3.1/Connectome_Utilities.egg-info/PKG-INFO` & `Connectome-Utilities-0.3.2/Connectome_Utilities.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Connectome-Utilities
-Version: 0.3.1
+Version: 0.3.2
 Summary: Complex network representation and analysis layer
 Author-email: "Blue Brain Project, EPFL" <conntility.645co@simplelogin.com>
 Project-URL: Homepage, https://github.com/BlueBrain/ConnectomeUtilities
 Project-URL: Bug Tracker, https://github.com/BlueBrain/ConnectomeUtilities/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `Connectome-Utilities-0.3.1/LICENSE` & `Connectome-Utilities-0.3.2/LICENSE`

 * *Files identical despite different names*

### Comparing `Connectome-Utilities-0.3.1/PKG-INFO` & `Connectome-Utilities-0.3.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Connectome-Utilities
-Version: 0.3.1
+Version: 0.3.2
 Summary: Complex network representation and analysis layer
 Author-email: "Blue Brain Project, EPFL" <conntility.645co@simplelogin.com>
 Project-URL: Homepage, https://github.com/BlueBrain/ConnectomeUtilities
 Project-URL: Bug Tracker, https://github.com/BlueBrain/ConnectomeUtilities/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `Connectome-Utilities-0.3.1/README.md` & `Connectome-Utilities-0.3.2/README.md`

 * *Files identical despite different names*

### Comparing `Connectome-Utilities-0.3.1/conntility/connectivity.py` & `Connectome-Utilities-0.3.2/conntility/connectivity.py`

 * *Files 2% similar despite different names*

```diff
@@ -130,84 +130,98 @@
 
 
 class _MatrixEdgeIndexer(object):
     """
     A helper class used to sample filtered versions of a network, i.e. same set of nodes, but a subset of edges.
     Instantiate using ConnectivityMatrix.filter.
     """
-    def __init__(self, parent, prop_name):
+    def __init__(self, parent, prop_name, side=None):
+        # TODO: Enable using an 'edge-associated-node-property' as well.
         self._parent = parent
-        self._prop = parent.edges[prop_name].values
+        self._prop_name = prop_name
+        self._side = side
+        if prop_name in list(parent.edge_properties):
+            self._prop = parent.edges[prop_name]
+        elif prop_name in list(parent.vertex_properties):
+            self._prop = parent.edge_associated_vertex_properties(prop_name)
+            if side is not None:
+                self._prop = self._prop[side]
+        else:
+            raise ValueError("Unknown property: {0}".format(prop_name))
+    
+    def _reduce_(self, idxx):
+        if isinstance(idxx, pd.DataFrame):
+            return self._parent.subedges(np.all(idxx, axis=1))
+        return self._parent.subedges(idxx.values)
 
     def eq(self, other):
         """
         Return network with edges where the value of the indexed property is equal to the provided reference.
         """
         idxx = self._prop == other
-        return self._parent.subedges(idxx)
+        return self._reduce_(idxx)
 
     def isin(self, other):
         """
         Return network with edges where the value of the indexed property is within the list provided as reference.
         """
         idxx = np.isin(self._prop, other)
-        return self._parent.subedges(idxx)
+        return self._reduce_(idxx)
 
     def le(self, other):
         """
         Return network with edges where the value of the indexed property is less or equal to the provided reference.
         """
         idxx = self._prop <= other
-        return self._parent.subedges(idxx)
+        return self._reduce_(idxx)
 
     def lt(self, other):
         """
         Return network with edges where the value of the indexed property is less than the provided reference.
         """
         idxx = self._prop < other
-        return self._parent.subedges(idxx)
+        return self._reduce_(idxx)
 
     def ge(self, other):
         """
         Return network with edges where the value of the indexed property is greater or equal to the provided reference.
         """
         idxx = self._prop >= other
-        return self._parent.subedges(idxx)
+        return self._reduce_(idxx)
 
     def gt(self, other):
         """
         Return network with edges where the value of the indexed property is greater than the provided reference.
         """
         idxx = self._prop > other
-        return self._parent.subedges(idxx)
+        return self._reduce_(idxx)
 
     def full_sweep(self, direction='decreasing'):
         """
         Return ConnectivityGroup representing a filtration with successively decreasing or increasing threshold values for
         the indexed property.
         """
         #  For an actual filtration. Take all values and sweep
         raise NotImplementedError()
     
-    def random_by_vertex_property_ids(self, ref, prop_name, n_bins=None, is_edges=False):
+    def random_by_vertex_property_ids(self, ref, n_bins=None, is_edges=False):
         """
+        TODO: Instead of specifying a node property here, specify it when instantiating this object.
         Return a random subnetwork with the same nodes but only a subset of the edges. The subset is randomly generated 
         based on a reference. 
         The returned subnetwork will match the reference in terms of the distributions of the specified node property for
         source and target nodes of edges.
 
         Args:
           ref: A reference to match. Must represent a sub-network of the base network that contains either all nodes and
           a subset of edges, or a subset of nodes and all edges between them.
           In the first case, it is a list of edge ids (indices of ConnectivityMatrix._edges).
           In the second case it is either a ConnectivityMatrix object or a list of the "gid" node property of the base 
           network.
 
-          prop_name: Must be a node property (ConnectivityMatrix.vertex_properties) to match the distribution of.
-
           n_bins: If provided, the node property will be binned as specified. Node property must then be numerical.
 
           is_edges: If set to True, the reference will be interpreted as edge ids. Otherwise, its nature will be tried
           to be inferred.
 
         Returns:
           A list of edge ids representing the random subnetwork.
@@ -221,41 +235,42 @@
                 try:
                     ref = self._parent.subpopulation(self._parent.__extract_vertex_ids__(ref))
                     print("Interpreting reference as vertex ids. If that is wrong, set is_edges=True")
                 except (AssertionError, IndexError):
                     ref = self._parent.subedges(ref)
                     print("Interpreting reference as edge ids!")
 
-        ref_edges = ref.edge_associated_vertex_properties(prop_name)
-        parent_edges = self._parent.edge_associated_vertex_properties(prop_name)
+        ref_edges = ref.edge_associated_vertex_properties(self._prop_name)
+        if self._side is not None: ref_edges = ref_edges[self._side]
+        parent_edges = self._prop #self._parent.edge_associated_vertex_properties(prop_name)
 
         if n_bins is not None:
             mn, mx = np.min(parent_edges.values.flat), np.max(parent_edges.values.flat)
             bins = np.linspace(mn, mx + (mx - mn) / 1E9, n_bins + 1)
             ref_edges = ref_edges.apply(np.digitize, axis=0, bins=bins)
             parent_edges = parent_edges.apply(np.digitize, axis=0, bins=bins)
 
         ref_counts = ref_edges.value_counts()
-        parent_edges = parent_edges.reset_index().set_index(["row", "col"])["index"]
+        parent_edges = parent_edges.reset_index().set_index(list(ref_counts.index.names))["index"]
 
         out_edges = []
         for _idx, n in ref_counts.items():
             out_edges.extend(np.random.choice(parent_edges[_idx].values, n, replace=False))
         return out_edges
     
-    def random_by_vertex_property(self, ref, prop_name, n_bins=None):
+    def random_by_vertex_property(self, ref, n_bins=None):
         """
         Generates a random subnetwork containing all nodes and a subset of edges. Based on matching
         the distribution of properties of source and target nodes to a reference subnetwork.
         For details, see .random_by_vertex_property_ids
 
         Returns:
           A ConnectivityMatrix object representing the subnetwork.
         """
-        edge_ids = self.random_by_vertex_property_ids(ref, prop_name, n_bins=n_bins)
+        edge_ids = self.random_by_vertex_property_ids(ref, n_bins=n_bins)
         return self._parent.subedges(edge_ids)
 
 
 class _MatrixNeighborhoodIndexer(object):
     """
     A helper class used to generate subnetworks of neighborhoods of nodes, i.e. containing a specified node
     and all nodes connected to it.
@@ -395,25 +410,26 @@
 
     def __len__(self):
         """
         Length of a ConnectivityMatrix is the number of nodes
         """
         return len(self.gids)
 
-    def add_vertex_property(self, new_label, new_values):
+    def add_vertex_property(self, new_label, new_values, overwrite=False):
         """
-        Assign values for a new property to all nodes. Must be a non-existing property.
+        Assign values for a new property to all nodes. Must be a non-existing property or overwrite=True.
 
         Args:
           new_label (str): Name of the new property. No property with this name may already exist.
           new_values (iterable): Values for the new property. Must have same length as this object.
           If provided as a DataFrame, must have the same index as obj._vertex_properties
+          overwrite (bool, default=False)
         """
         assert len(new_values) == len(self), "New values size mismatch"
-        assert new_label not in self._vertex_properties, "Property {0} already exists!".format(new_label)
+        assert overwrite or (new_label not in self._vertex_properties), "Property {0} already exists!".format(new_label)
         self._vertex_properties[new_label] = new_values
     
     def add_edge_property(self, new_label, new_values):
         """
         Assign values for a new property to all edges. Must be a non-existing property.
 
         Args:
@@ -494,15 +510,15 @@
     def vertex_properties(self):
         """
         The names of all available node properties. Properties can be used with obj.index(prop)
         """
         # TODO: Think about adding GID here as well?
         return self._vertex_properties.columns.values
     
-    def edge_associated_vertex_properties(self, prop_name):
+    def edge_associated_vertex_properties(self, prop_name, side=None):
         """
         The list of values of the specified node property associated with all edges. That is, for each edge
         the value of the property is returned for the source and target nodes. 
         Args:
           prop_name: Name of the property to gather. Must be in obj.vertex_properties.
 
         Returns:
@@ -576,29 +592,32 @@
         
         Returns:
           _MatrixNodeIndexer associated with this object.
         """
         assert prop_name in self._vertex_properties, "vertex property should be in " + str(self.vertex_properties)
         return _MatrixNodeIndexer(self, prop_name)
 
-    def filter(self, prop_name=None):
+    def filter(self, prop_name=None, side=None):
         """
         Returns an object for the generation of subnetworks based on values of the specified edge property.
         For details, see _MatrixEdgeIndexer.
 
         Args:
-          prop_name (str): Must be in obj.edge_properties. Name of the property based on which subnetworks
-          are to be sampled. 
+          prop_name (str): Must be in obj.edge_properties or obj.vertex_properties.
+          Name of the property based on which subnetworks are to be sampled. 
+          side (optional, one of "row", "col): Relevant when prop_name is a vertex_property. If "row", then
+          the specified vertex property of the source side of the connection is used. If "col", then the
+          target side is used. If not provided, the combination of both is used.
         
         Returns:
           _MatrixEdgeIndexer associated with this object.
         """
         if prop_name is None:
             prop_name = self._default_edge
-        return _MatrixEdgeIndexer(self, prop_name)
+        return _MatrixEdgeIndexer(self, prop_name, side=side)
 
     def default(self, new_default_property, copy=True):
         """
         Set the default edge property to return. Used in obj.matrix, obj.dense_matrix, obj.array
 
         Args:
           new_default_property (str): Name of the new edge property to use as default. Must be one of
@@ -1171,16 +1190,14 @@
             # Number of potential connections in each module (no autapses!)
             if len(with_respect_to) == 1:
                 npairs = self.vertices[with_respect_to[0]].value_counts().apply(lambda x: x ** 2 - x).sort_index()
             else:
                 npairs = self.vertices[with_respect_to].value_counts().apply(lambda x: x ** 2 - x).sort_index()
             mdlrty = (real.divide(npairs, fill_value=0) ** resolution_param) * mdlrty
         return mdlrty
-    
-
 
     @classmethod
     def from_h5(cls, fn, group_name=None, prefix=None):
         """
         Load a ConnectivityMatrix from a propriatory formatted hdf5 file.
 
         Args:
@@ -1473,83 +1490,148 @@
         edge_properties = pd.DataFrame({default_edge_property: np.ones(len(df), dtype=bool)})
         return cls(df, vertex_labels=vertex_labels, vertex_properties=vertex_properties,
                    edge_properties=edge_properties, default_edge_property=default_edge_property,
                    shape=shape, edge_off=off_dict, edge_on=on_dict)
 
 
 class TimeDependentMatrix(ConnectivityMatrix):
-    """Utility class to get, save, load and hold a time dependent weighted connections matrices"""
+    """
+    A version of ConnectivityMatrix for connectivity that changes over time functionally, i.e.
+    unlike for `StructurallyPlasticMatrix` the presence and absence of edges remains fixed,
+    but their efficacy (or weight) may change.
+    """
     def __init__(self, *args, vertex_labels=None, vertex_properties=None,
                  edge_properties=None, default_edge_property=None, shape=None):
         """Not too intuitive init - please see `from_report()` below"""
         if len(args) == 1 and isinstance(args[0], np.ndarray) or isinstance(args[0], sparse.spmatrix):
             raise ValueError("TimeDependentMatrix can only be initialized by edge indices and edge properties")
         if isinstance(edge_properties, dict):
-            assert np.all([x.columns.dtype==float for x in edge_properties.values()]),\
+            assert np.all([x.columns.dtype == float for x in edge_properties.values()]),\
                  "Index of edge properties must be a float Index"
             edge_properties = pd.concat(edge_properties.values(), keys=edge_properties.keys(), names=["name"], axis=1)
             edge_properties.columns = edge_properties.columns.reorder_levels([1, 0])
         else:
             assert isinstance(edge_properties, pd.DataFrame)
             if isinstance(edge_properties.columns, pd.MultiIndex):
                 assert len(edge_properties.columns.levels) == 2, "Columns must index time and name"
-                if not edge_properties.columns.levels[0].dtype==float:
-                    assert edge_properties.columns.levels[1].dtype==float,\
+                if not edge_properties.columns.levels[0].dtype == float:
+                    assert edge_properties.columns.levels[1].dtype == float,\
                         "Time index must be of type float Index"
                     edge_properties.columns = edge_properties.columns.reorder_levels([1, 0])
                 else:
-                    assert edge_properties.columns.levels[0].dtype==float,\
+                    assert edge_properties.columns.levels[0].dtype == float,\
                         "Time index must be of type float Index"
             else:
-                assert edge_properties.columns.dtype==float,\
+                assert edge_properties.columns.dtype == float,\
                         "Time index must be of type Float64Index"
-                edge_properties = pd.concat([edge_properties], axis=1, copy=False, keys=["data"], names=["name"])
+                edge_properties = pd.concat([edge_properties], axis=1, copy=False, keys=["agg_fn"], names=["name"])
                 edge_properties.columns = edge_properties.columns.reorder_levels([1, 0])
         if default_edge_property is None:
             default_edge_property = edge_properties.columns.levels[1][0]
-        self._time = edge_properties.columns.levels[0].min()
+        self._times = np.unique(edge_properties.columns.get_level_values("time").to_numpy())
+        self._time = self._times.min()
         super().__init__(*args, vertex_labels=vertex_labels, vertex_properties=vertex_properties,
                          edge_properties=edge_properties, default_edge_property=default_edge_property, shape=shape)
-    
+
+    @property
+    def times(self):
+        return self._times
+
     @property
     def edges(self):
         return self._edges[self._time]
     
     def at_time(self, new_time):
         # TODO: Add a copy=True kwarg that acts like in .default
-        if new_time not in self._edges:
+        if new_time == -1:
+            new_time = self._times.max()
+        if new_time not in self._times:
             raise ValueError("No time point at {0} given".format(new_time))  # TODO: interpolate to nearest point?
         self._time = new_time
         return self
-    
-    def add_edge_property(self, new_label, new_values):
-        raise NotImplementedError("Not yet implemented for TimeDependentMatrix")
+
+    def delta(self, t_fr, t_to):
+        """Adds new `edge_property` (called 'delta') as the changes occuring between two time steps."""
+        delta = self._edges[t_to] - self._edges[t_fr]
+        for agg_fn in delta.columns.to_numpy():
+            self.add_edge_property(("delta", agg_fn), delta[agg_fn].to_numpy())
+        return self
     
     def default(self, new_default_property, copy=True):
         ret = super().default(new_default_property, copy=copy)
         if copy: ret._time = self._time
         return ret
     
     @classmethod
-    def from_report(cls, sim, report_cfg, load_cfg=None, presyn_mapping=None):
+    def from_report(cls, sim, report_cfg, load_cfg, presyn_mapping=None):
         """
         A sonata synapse (compartment) report based constructor
-        :param sim: bluepysnap Simulation object
+        :param sim: `bluepysnap.Simulation` object
         :param report_cfg: config dict with report's name, time steps to load,
                            static property name to look up for synapses that aren't reported,
-                           and optionally the names of the aggregation functions to use
+                           and the names of the aggregation functions to use
         :param load_cfg: config dict for loading and filtering neurons from the circuit
         :param presyn_mapping: mapping used to convert report from Neurodamus' post_gid & local_syn_id to
                                pre_gid and post_gid which can then be grouped and aggregated to get weighted connectomes
                                can be: pd.DataFrame with pre & post_gids and Neurodamus' local_syn_idx or
                                        filename of a saved DataFrame like that (loaded with `pd.read_pickle()`) or
                                        None (default) in which case the mapping will be calculated on the fly
         :return: a TimeDependentMatrix object
         """
-        raise NotImplementedError("Instantiation from report currently not available!")
+        from .io.synapse_report import sonata_report, load_report, get_presyn_mapping, reindex_report, aggregate_data
+        from .circuit_models.neuron_groups.grouping_config import load_filter
+
+        nrn = load_filter(sim.circuit, load_cfg)
+        lu_node_idx = pd.Series(range(len(nrn["node_ids"])), index=nrn["node_ids"])
+
+        report, report_node_idx = sonata_report(sim, report_cfg)
+        tgt_report_node_idx = np.intersect1d(nrn["node_ids"], report_node_idx)
+        non_report_node_idx = np.setdiff1d(nrn["node_ids"], tgt_report_node_idx)
+        data = load_report(report, report_cfg, tgt_report_node_idx)  # load only target (postsynaptic) node ids
+
+        if presyn_mapping is None or len(tgt_report_node_idx) < len(report_node_idx):
+            # the saved mapping is usually defined based on the full report, so if only parts are loaded
+            # one would need to filter the mapping as well at which point, it's faster to just recalculate it
+            presyn_mapping = get_presyn_mapping(sim.circuit, report_cfg["edge_population"], data.index)
+        if not isinstance(presyn_mapping, pd.DataFrame):
+            presyn_mapping = pd.read_pickle(presyn_mapping)
+
+        data = reindex_report(data, presyn_mapping)
+        data = data.iloc[data.index.get_level_values(0).isin(nrn["node_ids"])]  # filter to have only target pre_node_idx
+        print("Report read! Starting aggregation of %i data points..." % data.shape[0])
+
+        edges = aggregate_data(data, report_cfg, lu_node_idx)
+
+        if len(non_report_node_idx) > 0:
+            from .circuit_models import circuit_connection_matrix
+            print("Looking up static values for %i non-reported postsynaptic neurons..." % len(non_report_node_idx))
+            agg_funcs = list(edges.columns.levels[0])
+            Ms = circuit_connection_matrix(sim.circuit, connectome=report_cfg["edge_population"],
+                                           for_gids=nrn["node_ids"], for_gids_post=non_report_node_idx,
+                                           edge_property=report_cfg["static_prop_name"], agg_func=agg_funcs)
+            ts = edges.columns.levels[1]
+            stat_edges = [pd.DataFrame.from_dict({t: Ms[agg_func].tocoo().data for t in ts})
+                          for agg_func in agg_funcs]
+            stat_edges = pd.concat(stat_edges, axis=1, copy=False,  keys=agg_funcs)
+            stat_edges.columns.set_names(edges.columns.names, inplace=True)
+            # map (non-reported, local) col idx to node ids and then back to (global) col idx
+            lu_nr_node_idx = pd.Series(non_report_node_idx)
+            stat_col_idx = lu_node_idx[lu_nr_node_idx[Ms[agg_funcs[0]].tocoo().col]].to_numpy()
+            stat_edges.index = pd.MultiIndex.from_arrays(np.array([Ms[agg_funcs[0]].tocoo().row, stat_col_idx]),
+                                                         names=["row", "col"])
+            edges = pd.concat([edges, stat_edges])
+            edges.sort_index(inplace=True)
+
+        # separate the index from the edges (they're needed separately for the class' `init`)
+        new_idx = pd.RangeIndex(len(edges))
+        edge_idx = edges.index.to_frame().set_index(new_idx)
+        edges.set_index(new_idx, inplace=True)
+        edges.index.name = "edge_id"  # stupid pandas
+        return cls(edge_idx, edge_properties=edges, vertex_properties=nrn.set_index("node_ids"),
+                   shape=(len(nrn), len(nrn)))
 
 
 class ConnectivityInSubgroups(ConnectivityMatrix):
     # TODO: This functionality can be in the main ConnectivityMatrix
 
     def __extract_vertex_ids__(self, an_obj):
         if isinstance(an_obj, str):
```

### Comparing `Connectome-Utilities-0.3.1/conntility/multi_scale.py` & `Connectome-Utilities-0.3.2/conntility/multi_scale.py`

 * *Files identical despite different names*

### Comparing `Connectome-Utilities-0.3.1/conntility/plugins.py` & `Connectome-Utilities-0.3.2/conntility/plugins.py`

 * *Files identical despite different names*

### Comparing `Connectome-Utilities-0.3.1/pyproject.toml` & `Connectome-Utilities-0.3.2/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "Connectome-Utilities"
-version = "0.3.1"
+version = "0.3.2"
 authors = [
   { name="Blue Brain Project, EPFL", email="conntility.645co@simplelogin.com" },
 ]
 description = "Complex network representation and analysis layer"
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
```

### Comparing `Connectome-Utilities-0.3.1/tests/test_analysis.py` & `Connectome-Utilities-0.3.2/tests/test_analysis.py`

 * *Files identical despite different names*

### Comparing `Connectome-Utilities-0.3.1/tests/test_analysis_decorator.py` & `Connectome-Utilities-0.3.2/tests/test_analysis_decorator.py`

 * *Files identical despite different names*

### Comparing `Connectome-Utilities-0.3.1/tests/test_connectivity_matrix.py` & `Connectome-Utilities-0.3.2/tests/test_connectivity_matrix.py`

 * *Files identical despite different names*

### Comparing `Connectome-Utilities-0.3.1/tests/test_neuron_groups.py` & `Connectome-Utilities-0.3.2/tests/test_neuron_groups.py`

 * *Files identical despite different names*

