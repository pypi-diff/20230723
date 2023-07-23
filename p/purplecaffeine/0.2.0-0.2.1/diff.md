# Comparing `tmp/purplecaffeine-0.2.0.tar.gz` & `tmp/purplecaffeine-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "purplecaffeine-0.2.0.tar", last modified: Mon Jun 19 21:13:23 2023, max compression
+gzip compressed data, was "purplecaffeine-0.2.1.tar", last modified: Sun Jul 23 20:41:21 2023, max compression
```

## Comparing `purplecaffeine-0.2.0.tar` & `purplecaffeine-0.2.1.tar`

### file list

```diff
@@ -1,33 +1,33 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)     4609 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3731 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/purplecaffeine/
--rw-r--r--   0 runner    (1001) docker     (123)      199 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/purplecaffeine/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    20856 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/purplecaffeine/core.py
--rw-r--r--   0 runner    (1001) docker     (123)       97 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/purplecaffeine/exception.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/purplecaffeine/helpers/
--rw-r--r--   0 runner    (1001) docker     (123)      104 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/purplecaffeine/helpers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      684 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/purplecaffeine/helpers/conf.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/purplecaffeine/utils/
--rw-r--r--   0 runner    (1001) docker     (123)      133 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/purplecaffeine/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1229 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/purplecaffeine/utils/json.py
--rw-r--r--   0 runner    (1001) docker     (123)    12603 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/purplecaffeine/widget.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/purplecaffeine.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4609 2023-06-19 21:13:23.000000 purplecaffeine-0.2.0/purplecaffeine.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      621 2023-06-19 21:13:23.000000 purplecaffeine-0.2.0/purplecaffeine.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-19 21:13:23.000000 purplecaffeine-0.2.0/purplecaffeine.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      138 2023-06-19 21:13:23.000000 purplecaffeine-0.2.0/purplecaffeine.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       21 2023-06-19 21:13:23.000000 purplecaffeine-0.2.0/purplecaffeine.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1442 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/tests/helpers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/tests/helpers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      766 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/tests/helpers/test_conf.py
--rw-r--r--   0 runner    (1001) docker     (123)     4082 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/tests/test_storage.py
--rw-r--r--   0 runner    (1001) docker     (123)     4675 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/tests/test_trial.py
--rw-r--r--   0 runner    (1001) docker     (123)     4325 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/tests/test_widget.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:23.222534 purplecaffeine-0.2.0/tests/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/tests/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1134 2023-06-19 21:13:14.000000 purplecaffeine-0.2.0/tests/utils/test_json.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     4792 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3914 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/purplecaffeine/
+-rw-r--r--   0 runner    (1001) docker     (123)      199 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/purplecaffeine/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21449 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/purplecaffeine/core.py
+-rw-r--r--   0 runner    (1001) docker     (123)       97 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/purplecaffeine/exception.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/purplecaffeine/helpers/
+-rw-r--r--   0 runner    (1001) docker     (123)      104 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/purplecaffeine/helpers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      684 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/purplecaffeine/helpers/conf.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/purplecaffeine/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)      133 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/purplecaffeine/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1229 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/purplecaffeine/utils/json.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12587 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/purplecaffeine/widget.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/purplecaffeine.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4792 2023-07-23 20:41:21.000000 purplecaffeine-0.2.1/purplecaffeine.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      621 2023-07-23 20:41:21.000000 purplecaffeine-0.2.1/purplecaffeine.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 20:41:21.000000 purplecaffeine-0.2.1/purplecaffeine.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      138 2023-07-23 20:41:21.000000 purplecaffeine-0.2.1/purplecaffeine.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       21 2023-07-23 20:41:21.000000 purplecaffeine-0.2.1/purplecaffeine.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1442 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/tests/helpers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/tests/helpers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      766 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/tests/helpers/test_conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4082 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/tests/test_storage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5064 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/tests/test_trial.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4325 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/tests/test_widget.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:21.399161 purplecaffeine-0.2.1/tests/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/tests/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1134 2023-07-23 20:41:14.000000 purplecaffeine-0.2.1/tests/utils/test_json.py
```

### Comparing `purplecaffeine-0.2.0/PKG-INFO` & `purplecaffeine-0.2.1/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: purplecaffeine
-Version: 0.2.0
+Version: 0.2.1
 Summary: PurpleCaffeine: tracking of quantum programs and experiments
 Home-page: UNKNOWN
 License: UNKNOWN
 Keywords: quantum tracking experiments
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
@@ -54,14 +54,15 @@
 
 ```python
 from qiskit.circuit.random import random_circuit
 from qiskit.quantum_info.random import random_pauli
 from qiskit.primitives import Estimator
 
 from purplecaffeine.core import Trial, LocalStorage
+from purplecaffeine.widget import Widget
 
 n_qubits = 4
 depth = 3
 shots = 2000
 
 circuit = random_circuit(n_qubits, depth)
 obs = random_pauli(n_qubits)
@@ -80,15 +81,18 @@
     trial.add_operator("obs", obs)
 
     # run
     exp_value = Estimator().run(circuit, obs, shots=shots).result().values.item()
     
     # track results of run
     trial.add_metric("exp_value", exp_value)
+
+Widget(local_storage).show()
 ```
+![visualization](https://raw.githubusercontent.com/IceKhan13/purplecaffeine/main/docs/images/visualization.png)
 
 ----------------------------------------------------------------------------------------------------
 
 ### Documentation
 
 Documentation for project is hosted at https://icekhan13.github.io/purplecaffeine/
```

### Comparing `purplecaffeine-0.2.0/README.md` & `purplecaffeine-0.2.1/README.md`

 * *Files 13% similar despite different names*

```diff
@@ -31,14 +31,15 @@
 
 ```python
 from qiskit.circuit.random import random_circuit
 from qiskit.quantum_info.random import random_pauli
 from qiskit.primitives import Estimator
 
 from purplecaffeine.core import Trial, LocalStorage
+from purplecaffeine.widget import Widget
 
 n_qubits = 4
 depth = 3
 shots = 2000
 
 circuit = random_circuit(n_qubits, depth)
 obs = random_pauli(n_qubits)
@@ -57,15 +58,18 @@
     trial.add_operator("obs", obs)
 
     # run
     exp_value = Estimator().run(circuit, obs, shots=shots).result().values.item()
     
     # track results of run
     trial.add_metric("exp_value", exp_value)
+
+Widget(local_storage).show()
 ```
+![visualization](https://raw.githubusercontent.com/IceKhan13/purplecaffeine/main/docs/images/visualization.png)
 
 ----------------------------------------------------------------------------------------------------
 
 ### Documentation
 
 Documentation for project is hosted at https://icekhan13.github.io/purplecaffeine/
```

### Comparing `purplecaffeine-0.2.0/purplecaffeine/core.py` & `purplecaffeine-0.2.1/purplecaffeine/core.py`

 * *Files 3% similar despite different names*

```diff
@@ -9,14 +9,15 @@
 from typing import Optional, Union, List, Any, Dict
 from uuid import uuid4
 
 import boto3
 import numpy as np
 import requests
 from pympler import asizeof
+from qiskit import __qiskit_version__
 from qiskit.circuit import QuantumCircuit
 from qiskit.quantum_info.operators import Operator
 
 from purplecaffeine.exception import PurpleCaffeineException
 from purplecaffeine.helpers import Configuration
 from purplecaffeine.utils import TrialEncoder, TrialDecoder
 
@@ -31,14 +32,15 @@
         circuits (List[(str, QuantumCircuit)]): list of quantum circuit
         operators (List[(str, Operator)]): list of operator, like Pauli operators
         artifacts (List[(str, Any)]): list of artifact, any external files
         texts (List[(str, str)]): list of text, any descriptions
         arrays (List[(str, Union[np.ndarray, List[Any]])]):
             list of array, like quantum circuit results
         tags (List[str]): list of tags in string format
+        versions (List[(str, str)]): list of qiskit version
     """
 
     def __init__(
         self,
         name: str,
         uuid: Optional[str] = None,
         storage: Optional[BaseStorage] = None,
@@ -47,28 +49,30 @@
         parameters: Optional[List[List[str]]] = None,
         circuits: Optional[List[List[Union[str, QuantumCircuit]]]] = None,
         operators: Optional[List[List[Union[str, Operator]]]] = None,
         artifacts: Optional[List[List[str]]] = None,
         texts: Optional[List[List[str]]] = None,
         arrays: Optional[List[List[Union[str, np.ndarray]]]] = None,
         tags: Optional[List[str]] = None,
+        versions: Optional[List[List[str]]] = None,
     ):
         """Trial class for tracking experiments data.
 
         Args:
             description (str): short description of the trial
             metrics (List[(str, Union[int, float])]): list of metric, like number of qubits
             parameters (List[(str, str)]): list of parameter, like env details
             circuits (List[(str, QuantumCircuit)]): list of quantum circuit
             operators (List[(str, Operator)]): list of operator, like Pauli operators
             artifacts (List[(str, Any)]): list of artifact, any external files
             texts (List[(str, str)]): list of text, any descriptions
             arrays (List[(str, Union[np.ndarray, List[Any]])]):
                 list of array, like quantum circuit results
             tags (List[str]): list of tags in string format
+            versions (List[(str, str)]): list of qiskit version
         """
         self.uuid = uuid or str(uuid4())
         self.name = name or os.environ.get("PURPLE_CAFFEINE_TRIAL_NAME")
         if self.name is None:
             raise PurpleCaffeineException(
                 "Please specify name of trial or configure it using env variables"
             )
@@ -97,14 +101,15 @@
         self.texts = texts or []
         self.arrays = arrays or []
         self.tags = tags or (
             os.environ.get("PURPLE_CAFFEINE_TRIAL_TAGS", "").split(",")
             if os.environ.get("PURPLE_CAFFEINE_TRIAL_TAGS")
             else []
         )
+        self.versions = versions or []
 
     def __repr__(self):
         return f"<Trial [{self.name}] {self.uuid}>"
 
     def __enter__(self):
         return self
 
@@ -187,14 +192,23 @@
         """Adds any tag to trial data.
 
         Args:
             tag: word of your tag
         """
         self.tags.append(tag)
 
+    def add_version(self, name: str, value: str):
+        """Adds version to trial data.
+
+        Args:
+            name: name of the package
+            value: version for the package
+        """
+        self.versions.append([name, value])
+
     def save(self):
         """Save into Storage."""
         self.storage.save(trial=self)
 
     def read(self, trial_id: str) -> Trial:
         """Read a trial from Storage.
 
@@ -238,14 +252,16 @@
         filename = os.path.join(path, f"{self.uuid}.json")
         with open(filename, "w", encoding="utf-8") as trial_file:
             json.dump(self.__dict__, trial_file, cls=TrialEncoder, indent=4)
 
         return filename
 
     def __exit__(self, exc_type, exc_val, exc_tb):
+        for key in __qiskit_version__:
+            self.add_version(key, __qiskit_version__[key])
         self.save()
 
 
 class BaseStorage:
     """Base storage class."""
 
     def save(self, trial: Trial):
```

### Comparing `purplecaffeine-0.2.0/purplecaffeine/helpers/conf.py` & `purplecaffeine-0.2.1/purplecaffeine/helpers/conf.py`

 * *Files identical despite different names*

### Comparing `purplecaffeine-0.2.0/purplecaffeine/utils/json.py` & `purplecaffeine-0.2.1/purplecaffeine/utils/json.py`

 * *Files identical despite different names*

### Comparing `purplecaffeine-0.2.0/purplecaffeine/widget.py` & `purplecaffeine-0.2.1/purplecaffeine/widget.py`

 * *Files 0% similar despite different names*

```diff
@@ -366,13 +366,13 @@
         return tab
 
     def show(self):
         """
         Function to assemble all the other
         widgets into one
         """
-        grid = GridspecLayout(10, 3, height="500px")
+        grid = GridspecLayout(10, 3)
         grid[0, :] = self.search()
         grid[1:8, 0:1] = self.list_view
         grid[1:9, 1:] = self.detail_view
         grid[8, :1] = self.pagination_view
         return grid
```

### Comparing `purplecaffeine-0.2.0/purplecaffeine.egg-info/PKG-INFO` & `purplecaffeine-0.2.1/purplecaffeine.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: purplecaffeine
-Version: 0.2.0
+Version: 0.2.1
 Summary: PurpleCaffeine: tracking of quantum programs and experiments
 Home-page: UNKNOWN
 License: UNKNOWN
 Keywords: quantum tracking experiments
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
@@ -54,14 +54,15 @@
 
 ```python
 from qiskit.circuit.random import random_circuit
 from qiskit.quantum_info.random import random_pauli
 from qiskit.primitives import Estimator
 
 from purplecaffeine.core import Trial, LocalStorage
+from purplecaffeine.widget import Widget
 
 n_qubits = 4
 depth = 3
 shots = 2000
 
 circuit = random_circuit(n_qubits, depth)
 obs = random_pauli(n_qubits)
@@ -80,15 +81,18 @@
     trial.add_operator("obs", obs)
 
     # run
     exp_value = Estimator().run(circuit, obs, shots=shots).result().values.item()
     
     # track results of run
     trial.add_metric("exp_value", exp_value)
+
+Widget(local_storage).show()
 ```
+![visualization](https://raw.githubusercontent.com/IceKhan13/purplecaffeine/main/docs/images/visualization.png)
 
 ----------------------------------------------------------------------------------------------------
 
 ### Documentation
 
 Documentation for project is hosted at https://icekhan13.github.io/purplecaffeine/
```

### Comparing `purplecaffeine-0.2.0/purplecaffeine.egg-info/SOURCES.txt` & `purplecaffeine-0.2.1/purplecaffeine.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `purplecaffeine-0.2.0/setup.py` & `purplecaffeine-0.2.1/setup.py`

 * *Files identical despite different names*

### Comparing `purplecaffeine-0.2.0/tests/helpers/test_conf.py` & `purplecaffeine-0.2.1/tests/helpers/test_conf.py`

 * *Files identical despite different names*

### Comparing `purplecaffeine-0.2.0/tests/test_storage.py` & `purplecaffeine-0.2.1/tests/test_storage.py`

 * *Files identical despite different names*

### Comparing `purplecaffeine-0.2.0/tests/test_trial.py` & `purplecaffeine-0.2.1/tests/test_trial.py`

 * *Files 5% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 import os
 import shutil
 from pathlib import Path
 from typing import Optional
 from unittest import TestCase
 
 import numpy as np
-from qiskit import QuantumCircuit
+from qiskit import QuantumCircuit, __qiskit_version__
 from qiskit.circuit.library import XGate
 from qiskit.quantum_info import Operator
 
 from purplecaffeine import Trial, LocalStorage, BaseStorage as TrialStorage
 
 
 def dummy_trial(
@@ -27,14 +27,15 @@
     trial.add_parameter("test_parameter", "parameter")
     trial.add_circuit("test_circuit", QuantumCircuit(2))
     trial.add_operator("test_operator", Operator(XGate()))
     trial.add_text("test_text", "text")
     trial.add_array("test_array", np.array([42]))
     trial.add_tag("qiskit")
     trial.add_tag("test")
+    trial.add_version("numpy", "1.2.3-4")
     return trial
 
 
 class TestTrial(TestCase):
     """TestTrial."""
 
     def setUp(self) -> None:
@@ -49,27 +50,31 @@
         """Test train context."""
         uuid = "some_uuid"
         with Trial(name="test_trial", storage=self.local_storage, uuid=uuid) as trial:
             trial.add_metric("test_metric", 42)
         trial.read(trial_id=uuid)
         self.assertTrue(os.path.isfile(os.path.join(self.save_path, f"{uuid}.json")))
         self.assertEqual(trial.metrics, [["test_metric", 42]])
+        self.assertEqual(
+            trial.versions, [[key, value] for key, value in __qiskit_version__.items()]
+        )
 
     def test_add_trial(self):
         """Test adding stuff into Trial."""
         trial = dummy_trial()
 
         self.assertEqual(trial.description, "Short desc")
         self.assertEqual(trial.metrics, [["test_metric", 42]])
         self.assertEqual(trial.parameters, [["test_parameter", "parameter"]])
         self.assertEqual(trial.circuits, [["test_circuit", QuantumCircuit(2)]])
         self.assertEqual(trial.operators, [["test_operator", Operator(XGate())]])
         self.assertEqual(trial.texts, [["test_text", "text"]])
         self.assertEqual(trial.arrays, [["test_array", np.array([42])]])
         self.assertEqual(trial.tags, ["qiskit", "test"])
+        self.assertEqual(trial.versions, [["numpy", "1.2.3-4"]])
 
     def test_save_read_local_trial(self):
         """Test save and read Trial locally."""
         trial = dummy_trial(storage=self.local_storage)
         trial.save()
 
         self.assertTrue(
@@ -80,14 +85,15 @@
         self.assertEqual(recovered.metrics, [["test_metric", 42]])
         self.assertEqual(recovered.parameters, [["test_parameter", "parameter"]])
         self.assertEqual(recovered.circuits, [["test_circuit", QuantumCircuit(2)]])
         self.assertEqual(recovered.operators, [["test_operator", Operator(XGate())]])
         self.assertEqual(recovered.texts, [["test_text", "text"]])
         self.assertEqual(recovered.arrays, [["test_array", np.array([42])]])
         self.assertEqual(recovered.tags, ["qiskit", "test"])
+        self.assertEqual(recovered.versions, [["numpy", "1.2.3-4"]])
 
     def test_export_import(self):
         """Test export and import Trial from shared file."""
         trial = dummy_trial()
         # Export
         trial.export_to_shared_file(path=self.save_path)
         self.assertTrue(
@@ -101,13 +107,14 @@
         self.assertEqual(new_trial.metrics, [["test_metric", 42]])
         self.assertEqual(new_trial.parameters, [["test_parameter", "parameter"]])
         self.assertEqual(new_trial.circuits, [["test_circuit", QuantumCircuit(2)]])
         self.assertEqual(new_trial.operators, [["test_operator", Operator(XGate())]])
         self.assertEqual(new_trial.texts, [["test_text", "text"]])
         self.assertEqual(new_trial.arrays, [["test_array", np.array([42])]])
         self.assertEqual(new_trial.tags, ["qiskit", "test"])
+        self.assertEqual(new_trial.versions, [["numpy", "1.2.3-4"]])
 
     def tearDown(self) -> None:
         """TearDown Trial object."""
         file_to_remove = os.path.join(self.save_path)
         if os.path.exists(file_to_remove):
             shutil.rmtree(file_to_remove)
```

### Comparing `purplecaffeine-0.2.0/tests/test_widget.py` & `purplecaffeine-0.2.1/tests/test_widget.py`

 * *Files identical despite different names*

### Comparing `purplecaffeine-0.2.0/tests/utils/test_json.py` & `purplecaffeine-0.2.1/tests/utils/test_json.py`

 * *Files identical despite different names*

