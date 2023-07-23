# Comparing `tmp/connex-0.3.2.tar.gz` & `tmp/connex-0.3.3.tar.gz`

## Comparing `connex-0.3.2.tar` & `connex-0.3.3.tar`

### file list

```diff
@@ -1,13 +1,13 @@
--rw-r--r--   0        0        0      237 2020-02-02 00:00:00.000000 connex-0.3.2/connex/__init__.py
--rw-r--r--   0        0        0    33075 2020-02-02 00:00:00.000000 connex-0.3.2/connex/_network.py
--rw-r--r--   0        0        0    46899 2020-02-02 00:00:00.000000 connex-0.3.2/connex/_plasticity.py
--rw-r--r--   0        0        0     1459 2020-02-02 00:00:00.000000 connex-0.3.2/connex/_utils.py
--rw-r--r--   0        0        0       55 2020-02-02 00:00:00.000000 connex-0.3.2/connex/nn/__init__.py
--rw-r--r--   0        0        0     7058 2020-02-02 00:00:00.000000 connex-0.3.2/connex/nn/_dense_mlp.py
--rw-r--r--   0        0        0     6522 2020-02-02 00:00:00.000000 connex-0.3.2/connex/nn/_mlp.py
--rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 connex-0.3.2/connex/nn/_utils.py
--rw-r--r--   0        0        0      136 2020-02-02 00:00:00.000000 connex-0.3.2/.gitignore
--rw-r--r--   0        0        0    11356 2020-02-02 00:00:00.000000 connex-0.3.2/LICENSE
--rw-r--r--   0        0        0     3656 2020-02-02 00:00:00.000000 connex-0.3.2/README.md
--rw-r--r--   0        0        0     1148 2020-02-02 00:00:00.000000 connex-0.3.2/pyproject.toml
--rw-r--r--   0        0        0    17686 2020-02-02 00:00:00.000000 connex-0.3.2/PKG-INFO
+-rw-r--r--   0        0        0      237 2020-02-02 00:00:00.000000 connex-0.3.3/connex/__init__.py
+-rw-r--r--   0        0        0    33083 2020-02-02 00:00:00.000000 connex-0.3.3/connex/_network.py
+-rw-r--r--   0        0        0    46919 2020-02-02 00:00:00.000000 connex-0.3.3/connex/_plasticity.py
+-rw-r--r--   0        0        0     1401 2020-02-02 00:00:00.000000 connex-0.3.3/connex/_utils.py
+-rw-r--r--   0        0        0       55 2020-02-02 00:00:00.000000 connex-0.3.3/connex/nn/__init__.py
+-rw-r--r--   0        0        0     7085 2020-02-02 00:00:00.000000 connex-0.3.3/connex/nn/_dense_mlp.py
+-rw-r--r--   0        0        0     6549 2020-02-02 00:00:00.000000 connex-0.3.3/connex/nn/_mlp.py
+-rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 connex-0.3.3/connex/nn/_utils.py
+-rw-r--r--   0        0        0      136 2020-02-02 00:00:00.000000 connex-0.3.3/.gitignore
+-rw-r--r--   0        0        0    11356 2020-02-02 00:00:00.000000 connex-0.3.3/LICENSE
+-rw-r--r--   0        0        0     3457 2020-02-02 00:00:00.000000 connex-0.3.3/README.md
+-rw-r--r--   0        0        0     1148 2020-02-02 00:00:00.000000 connex-0.3.3/pyproject.toml
+-rw-r--r--   0        0        0    17487 2020-02-02 00:00:00.000000 connex-0.3.3/PKG-INFO
```

### Comparing `connex-0.3.2/connex/_network.py` & `connex-0.3.3/connex/_network.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 import functools as ft
+from collections.abc import Callable, Mapping, Sequence
 from copy import deepcopy
-from typing import Any, Callable, Dict, List, Mapping, Optional, Sequence, Tuple, Union
+from typing import Any, Optional, Union
 
 import jax.nn as jnn
 import jax.numpy as jnp
 import jax.random as jr
 import networkx as nx
 import numpy as np
 from equinox import filter_jit, Module, static_field
@@ -12,41 +13,41 @@
 
 from ._utils import _identity, _invert_dict, _keygen, DiGraphLike
 
 
 class NeuralNetwork(Module):
     """A neural network whose structure is specified by a DAG."""
 
-    _weights_and_biases: List[Array]
+    _weights_and_biases: list[Array]
     _hidden_activation: Callable
     _output_transformation: Callable
-    _topo_norm_params: List[Array]
-    _attention_params_topo: List[Array]
-    _attention_params_neuron: List[Array]
-    _adaptive_activation_params: List[Array]
-    _dropout_dict: Dict[Any, float]
+    _topo_norm_params: list[Array]
+    _attention_params_topo: list[Array]
+    _attention_params_neuron: list[Array]
+    _adaptive_activation_params: list[Array]
+    _dropout_dict: dict[Any, float]
     _dropout_array: Array
     _graph: nx.DiGraph = static_field()
-    _adjacency_dict: Dict[Any, List[Any]] = static_field()
-    _adjacency_dict_inv: Dict[Any, List[Any]] = static_field()
-    _neuron_to_id: Dict[Any, int] = static_field()
-    _topo_batches: List[Array] = static_field()
+    _adjacency_dict: dict[Any, list[Any]] = static_field()
+    _adjacency_dict_inv: dict[Any, list[Any]] = static_field()
+    _neuron_to_id: dict[Any, int] = static_field()
+    _topo_batches: list[Array] = static_field()
     _topo_lengths: np.ndarray = static_field()
-    _topo_sizes: List[int] = static_field()
+    _topo_sizes: list[int] = static_field()
     _num_topo_batches: int = static_field()
-    _neuron_to_topo_batch_idx: Dict[int, Tuple[int, int]] = static_field()
-    _topo_sort: List[Any] = static_field()
+    _neuron_to_topo_batch_idx: dict[int, tuple[int, int]] = static_field()
+    _topo_sort: list[Any] = static_field()
     _min_index: np.ndarray = static_field()
     _max_index: np.ndarray = static_field()
-    _masks: List[Array] = static_field()
-    _attention_masks_neuron: List[Array] = static_field()
-    _indices: List[Array] = static_field()
-    _input_neurons: List[Any] = static_field()
-    _output_neurons: List[Any] = static_field()
-    _hidden_neurons: List[Any] = static_field()
+    _masks: list[Array] = static_field()
+    _attention_masks_neuron: list[Array] = static_field()
+    _indices: list[Array] = static_field()
+    _input_neurons: list[Any] = static_field()
+    _output_neurons: list[Any] = static_field()
+    _hidden_neurons: list[Any] = static_field()
     _input_neurons_id: Array = static_field()
     _output_neurons_id: Array = static_field()
     _num_neurons: int = static_field()
     _num_inputs_per_neuron: Array = static_field()
     _use_topo_norm: bool = static_field()
     _use_topo_self_attention: bool = static_field()
     _use_neuron_self_attention: bool = static_field()
@@ -505,15 +506,15 @@
 
     def _set_activations(
         self, hidden_activation: Callable, output_transformation: Callable
     ) -> None:
         """Set the activation functions."""
 
         def _validate_activation_function(
-            activation_func: Callable, input_shape: Tuple[int]
+            activation_func: Callable, input_shape: tuple[int]
         ) -> None:
             x = jnp.zeros(input_shape)
 
             try:
                 y = activation_func(x)
             except Exception as e:
                 raise Exception(
```

### Comparing `connex-0.3.2/connex/_plasticity.py` & `connex-0.3.3/connex/_plasticity.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,23 +1,24 @@
+from collections.abc import Mapping, Sequence
 from copy import deepcopy
-from typing import Any, Mapping, Optional, Sequence, Tuple, Union
+from typing import Any, Optional, Union
 
 import equinox as eqx
 import jax.numpy as jnp
 import jax.random as jr
 import networkx as nx
 import numpy as np
 
 from ._network import NeuralNetwork
 from ._utils import _edges_to_adjacency_dict
 
 
 def _get_id_mappings_old_new(
     old_network: NeuralNetwork, new_network: NeuralNetwork
-) -> Tuple[np.ndarray, np.ndarray]:
+) -> tuple[np.ndarray, np.ndarray]:
     old_neurons, new_neurons = old_network._graph.nodes(), new_network._graph.nodes()
     ids_old_to_new = -np.ones((old_network._num_neurons,), dtype=int)
     for neuron in old_neurons:
         if neuron in new_neurons:
             old_id = old_network._neuron_to_id[neuron]
             new_id = new_network._neuron_to_id[neuron]
             ids_old_to_new[old_id] = new_id
@@ -28,15 +29,15 @@
             old_id = old_network._neuron_to_id[neuron]
             ids_new_to_old[new_id] = old_id
     return ids_old_to_new, ids_new_to_old
 
 
 def add_connections(
     network: NeuralNetwork,
-    connections: Union[Sequence[Tuple[Any, Any]], Mapping[Any, Sequence[Any]]],
+    connections: Union[Sequence[tuple[Any, Any]], Mapping[Any, Sequence[Any]]],
     *,
     key: Optional[jr.PRNGKey] = None,
 ) -> NeuralNetwork:
     """Add connections to the network.
 
     **Arguments:**
 
@@ -272,15 +273,15 @@
             new_adaptive_activation_params,
         ),
     )
 
 
 def remove_connections(
     network: NeuralNetwork,
-    connections: Union[Sequence[Tuple[Any, Any]], Mapping[Any, Sequence[Any]]],
+    connections: Union[Sequence[tuple[Any, Any]], Mapping[Any, Sequence[Any]]],
 ) -> NeuralNetwork:
     """Remove connections from the network.
 
     **Arguments:**
 
     - `network`: A `NeuralNetwork` object.
     - `connections`: The directed edges to remove. Must be a sequence of 2-tuples, or
```

### Comparing `connex-0.3.2/connex/_utils.py` & `connex-0.3.3/connex/_utils.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import time
 import typing
 from collections import defaultdict
-from typing import Any, Dict, List
+from typing import Any
 
 import jax.nn as jnn
 import jax.random as jr
 
 
 # Documentation helpers.
 
@@ -23,15 +23,15 @@
     _identity.__qualname__ = "identity"
 
 DiGraphLike = Any
 
 ###############################################################
 
 
-def _invert_dict(_dict: Dict[Any, List[Any]]) -> Dict[Any, List[Any]]:
+def _invert_dict(_dict):
     _dict_inv = {}
     for (key, vals) in _dict.items():
         for val in vals:
             if val in _dict_inv:
                 _dict_inv[val].append(key)
             else:
                 _dict_inv[val] = [key]
```

### Comparing `connex-0.3.2/connex/nn/_dense_mlp.py` & `connex-0.3.3/connex/nn/_dense_mlp.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,9 @@
-from typing import Any, Callable, Mapping, Optional, Union
+from collections.abc import Callable, Mapping
+from typing import Any, Optional, Union
 
 import jax.nn as jnn
 import jax.random as jr
 import numpy as np
 
 from .._network import NeuralNetwork
 from ._utils import _identity
```

### Comparing `connex-0.3.2/connex/nn/_mlp.py` & `connex-0.3.3/connex/nn/_mlp.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,9 @@
-from typing import Any, Callable, Mapping, Optional, Union
+from collections.abc import Callable, Mapping
+from typing import Any, Optional, Union
 
 import jax.nn as jnn
 import jax.random as jr
 import numpy as np
 
 from .._network import NeuralNetwork
 from ._utils import _identity
```

### Comparing `connex-0.3.2/LICENSE` & `connex-0.3.3/LICENSE`

 * *Files identical despite different names*

### Comparing `connex-0.3.2/README.md` & `connex-0.3.3/README.md`

 * *Files 7% similar despite different names*

```diff
@@ -50,21 +50,20 @@
     adjacency_dict,
     input_neurons, 
     output_neurons,
     jnn.relu
 )
 ```
 
-That's it! A `connex.NeuralNetwork` is a subclass of `equinox.Module`, so it can be trained in the same fashion:
+That's it! A `connex.NeuralNetwork` is a subclass of `equinox.Module`, so it can be trained as such:
 
 ```python
 import equinox as eqx
 import jax
 import jax.numpy as jnp
-import jax.random as jr
 import optax
 
 # Initialize the optimizer
 optim = optax.adam(1e-3)
 opt_state = optim.init(eqx.filter(network, eqx.is_array))
 
 # Define the loss function
@@ -83,18 +82,17 @@
 
 # Toy data
 x = jnp.expand_dims(jnp.linspace(0, 2 * jnp.pi, 250), 1)
 y = jnp.hstack((jnp.cos(x), jnp.sin(x)))
 
 # Training loop
 n_epochs = 500
-key = jr.PRNGKey(0)
 for epoch in range(n_epochs):
     network, opt_state, loss = step(network, opt_state, x, y)
-    print(f"Epoch: {epoch + 1}   Loss: {loss}")
+    print(f"Epoch: {epoch}   Loss: {loss}")
 ```
 
 Now suppose we wish to add connections 1 &rarr; 6 and 2 &rarr; 11, remove neuron 9, and set the dropout probability of all hidden neurons to 0.1:
 
 ```python
 # Add connections
 network = cnx.add_connections(network, [(1, 6), (2, 11)])
@@ -102,15 +100,15 @@
 # Remove neuron
 network = cnx.remove_neurons(network, [9])
 
 # Set dropout probability
 network = cnx.set_dropout_p(network, 0.1)
 ```
 
-That's all there is to it.  The new connections have been initialized with untrained parameters, and the neurons in the original network that have not been removed (along with their respective incoming and outgoing connections) have retained their trained parameters. Furthermore, since a `connex.NeuralNetwork` is an `equinox.Module`, it can seamlessly be used as a submodule inside other Equinox Modules.
+That's all there is to it.  The new connections have been initialized with untrained parameters, and the neurons in the original network that have not been removed (along with their respective incoming and outgoing connections) have retained their trained parameters.
 
 For more information about manipulating connectivity structure and the `NeuralNetwork` base class, please see the API section of the documentation. For examples of subclassing `NeuralNetwork`, please see `connex.nn`.
 
 ## Citation
 
 ```bibtex
 @software{gleyzer2023connex,
```

### Comparing `connex-0.3.2/pyproject.toml` & `connex-0.3.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "connex"
-version = "0.3.2"
+version = "0.3.3"
 description = "Fine-grained, dynamic control of neural network topology in JAX."
 readme = "README.md"
 requires-python ="~=3.9"
 license = {file = "LICENSE"}
 authors = [
   {name = "Leonard Gleyzer", email = "lenny@lenn.ai"},
 ]
```

### Comparing `connex-0.3.2/PKG-INFO` & `connex-0.3.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: connex
-Version: 0.3.2
+Version: 0.3.3
 Summary: Fine-grained, dynamic control of neural network topology in JAX.
 Project-URL: repository, https://github.com/leonard-gleyzer/connex
 Author-email: Leonard Gleyzer <lenny@lenn.ai>
 License:                                  Apache License
                                    Version 2.0, January 2004
                                 http://www.apache.org/licenses/
         
@@ -276,21 +276,20 @@
     adjacency_dict,
     input_neurons, 
     output_neurons,
     jnn.relu
 )
 ```
 
-That's it! A `connex.NeuralNetwork` is a subclass of `equinox.Module`, so it can be trained in the same fashion:
+That's it! A `connex.NeuralNetwork` is a subclass of `equinox.Module`, so it can be trained as such:
 
 ```python
 import equinox as eqx
 import jax
 import jax.numpy as jnp
-import jax.random as jr
 import optax
 
 # Initialize the optimizer
 optim = optax.adam(1e-3)
 opt_state = optim.init(eqx.filter(network, eqx.is_array))
 
 # Define the loss function
@@ -309,18 +308,17 @@
 
 # Toy data
 x = jnp.expand_dims(jnp.linspace(0, 2 * jnp.pi, 250), 1)
 y = jnp.hstack((jnp.cos(x), jnp.sin(x)))
 
 # Training loop
 n_epochs = 500
-key = jr.PRNGKey(0)
 for epoch in range(n_epochs):
     network, opt_state, loss = step(network, opt_state, x, y)
-    print(f"Epoch: {epoch + 1}   Loss: {loss}")
+    print(f"Epoch: {epoch}   Loss: {loss}")
 ```
 
 Now suppose we wish to add connections 1 &rarr; 6 and 2 &rarr; 11, remove neuron 9, and set the dropout probability of all hidden neurons to 0.1:
 
 ```python
 # Add connections
 network = cnx.add_connections(network, [(1, 6), (2, 11)])
@@ -328,15 +326,15 @@
 # Remove neuron
 network = cnx.remove_neurons(network, [9])
 
 # Set dropout probability
 network = cnx.set_dropout_p(network, 0.1)
 ```
 
-That's all there is to it.  The new connections have been initialized with untrained parameters, and the neurons in the original network that have not been removed (along with their respective incoming and outgoing connections) have retained their trained parameters. Furthermore, since a `connex.NeuralNetwork` is an `equinox.Module`, it can seamlessly be used as a submodule inside other Equinox Modules.
+That's all there is to it.  The new connections have been initialized with untrained parameters, and the neurons in the original network that have not been removed (along with their respective incoming and outgoing connections) have retained their trained parameters.
 
 For more information about manipulating connectivity structure and the `NeuralNetwork` base class, please see the API section of the documentation. For examples of subclassing `NeuralNetwork`, please see `connex.nn`.
 
 ## Citation
 
 ```bibtex
 @software{gleyzer2023connex,
```

