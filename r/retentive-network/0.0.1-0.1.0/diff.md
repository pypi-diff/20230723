# Comparing `tmp/retentive_network-0.0.1.tar.gz` & `tmp/retentive_network-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "retentive_network-0.0.1.tar", max compression
+gzip compressed data, was "retentive_network-0.1.0.tar", max compression
```

## Comparing `retentive_network-0.0.1.tar` & `retentive_network-0.1.0.tar`

### file list

```diff
@@ -1,15 +1,17 @@
--rw-r--r--   0        0        0     1070 2023-07-21 23:49:09.311414 retentive_network-0.0.1/LICENSE
--rw-r--r--   0        0        0      478 2023-07-21 23:49:09.311414 retentive_network-0.0.1/README.md
--rw-r--r--   0        0        0      684 2023-07-21 23:49:09.311414 retentive_network-0.0.1/pyproject.toml
--rw-r--r--   0        0        0       55 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/__init__.py
--rw-r--r--   0        0        0      427 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/exceptions.py
--rw-r--r--   0        0        0        0 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/layers/__init__.py
--rw-r--r--   0        0        0     1724 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/layers/feed_forward.py
--rw-r--r--   0        0        0     1383 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/layers/layer_norm.py
--rw-r--r--   0        0        0     7220 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/layers/multi_scale_retention.py
--rw-r--r--   0        0        0     7003 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/layers/retention.py
--rw-r--r--   0        0        0      687 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/layers/swish_gate.py
--rw-r--r--   0        0        0        0 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/models/__init__.py
--rw-r--r--   0        0        0     9082 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/models/clm.py
--rw-r--r--   0        0        0     4575 2023-07-21 23:49:09.311414 retentive_network-0.0.1/retentive_network/models/network.py
--rw-r--r--   0        0        0     1162 1970-01-01 00:00:00.000000 retentive_network-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0     1070 2023-07-23 19:07:40.954681 retentive_network-0.1.0/LICENSE
+-rw-r--r--   0        0        0     2072 2023-07-23 19:07:40.954681 retentive_network-0.1.0/README.md
+-rw-r--r--   0        0        0      684 2023-07-23 19:07:40.954681 retentive_network-0.1.0/pyproject.toml
+-rw-r--r--   0        0        0       55 2023-07-23 19:07:40.954681 retentive_network-0.1.0/retentive_network/__init__.py
+-rw-r--r--   0        0        0     2521 2023-07-23 19:07:40.954681 retentive_network-0.1.0/retentive_network/exceptions.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:07:40.954681 retentive_network-0.1.0/retentive_network/layers/__init__.py
+-rw-r--r--   0        0        0     1724 2023-07-23 19:07:40.954681 retentive_network-0.1.0/retentive_network/layers/feed_forward.py
+-rw-r--r--   0        0        0     1862 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/layers/group_norm.py
+-rw-r--r--   0        0        0     1654 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/layers/layer_norm.py
+-rw-r--r--   0        0        0    10286 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/layers/multi_scale_retention.py
+-rw-r--r--   0        0        0     1335 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/layers/projection.py
+-rw-r--r--   0        0        0     8206 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/layers/retention.py
+-rw-r--r--   0        0        0      687 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/layers/swish_gate.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/models/__init__.py
+-rw-r--r--   0        0        0    10661 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/models/clm.py
+-rw-r--r--   0        0        0     7488 2023-07-23 19:07:40.958681 retentive_network-0.1.0/retentive_network/models/network.py
+-rw-r--r--   0        0        0     2756 1970-01-01 00:00:00.000000 retentive_network-0.1.0/PKG-INFO
```

### Comparing `retentive_network-0.0.1/LICENSE` & `retentive_network-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `retentive_network-0.0.1/pyproject.toml` & `retentive_network-0.1.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "retentive-network"
-version = "0.0.1"
+version = "0.1.0"
 description = "Unofficial codebase for the \"Retentive Network: A Successor to Transformer for Large Language Models\" paper [https://arxiv.org/pdf/2307.08621.pdf]"
 authors = ["Zach Bloss <zacharybloss@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "retentive_network"}]
 
 [tool.poetry.dependencies]
```

### Comparing `retentive_network-0.0.1/retentive_network/layers/feed_forward.py` & `retentive_network-0.1.0/retentive_network/layers/feed_forward.py`

 * *Files identical despite different names*

### Comparing `retentive_network-0.0.1/retentive_network/layers/layer_norm.py` & `retentive_network-0.1.0/retentive_network/layers/group_norm.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,45 +1,68 @@
 import torch
 import torch.nn as nn
 
+from retentive_network.exceptions import ComplexTensorException
 
-class LayerNorm(nn.Module):
+
+class GroupNorm(nn.Module):
     def __init__(
-        self, num_channels: int, eps: float = 1e-5, half_point_precision: bool = False
+        self,
+        number_of_groups: int,
+        number_of_channels: int,
+        eps: float = 1e-5,
+        dtype: torch.dtype = torch.float32,
     ):
-        super(LayerNorm, self).__init__()
-        self.num_channels = num_channels
-        self.eps = eps
+        super(GroupNorm, self).__init__()
 
-        dtype = torch.float16 if half_point_precision else torch.float32
+        self.number_of_groups = number_of_groups
+        self.number_of_channels = number_of_channels
+        self.eps = eps
+        self.dtype = dtype
 
-        self.gamma = nn.Parameter(torch.ones(num_channels, dtype=dtype))
-        self.beta = nn.Parameter(torch.zeros(num_channels, dtype=dtype))
+        self.gamma = nn.Parameter(torch.ones(number_of_channels, dtype=self.dtype))
+        self.beta = nn.Parameter(torch.zeros(number_of_channels, dtype=self.dtype))
 
     def forward(self, x: torch.Tensor) -> torch.Tensor:
         """
-        Applies LayerNorm according to the original paper.
+        Applies Group Normalization on x.
 
         Arguments:
-            x (torch.Tensor): Torch tensor of generic size.
-
+            x (torch.Tensor): Torch tensor of shape [
+                    batch_size,
+                    sequence_length,
+                    hidden_size,
+                ]
         Returns:
-            torch.Tensor: Torch tensor of shape x.shape.
+            torch.Tensor: Torch tensor of shape [
+                    batch_size,
+                    sequence_length,
+                    hidden_size
+                ]
         """
 
+        if x.dtype == torch.complex32 or x.dtype == torch.complex64:
+            raise ComplexTensorException(x)
+
         original_shape = x.shape
 
-        x = x.reshape(-1, original_shape[-1])
         mean = torch.mean(x, dim=1, keepdim=True)
         variance = torch.var(x, dim=1, keepdim=True)
+
         x = (x - mean) / torch.sqrt(variance + self.eps)
+        x = x.reshape(-1, self.number_of_channels)
         x *= self.gamma
         x += self.beta
+
         x = x.reshape(original_shape)
+
+        if x.dtype != self.dtype:
+            x = x.to(self.dtype)
+
         return x
 
 
 if __name__ == "__main__":
-    batch_size, sequence_length, hidden_dim = (4, 8, 32)
-    x: torch.Tensor = torch.randn((batch_size, sequence_length, hidden_dim))
-    layer: nn.Module = LayerNorm(hidden_dim)
-    out: torch.Tensor = layer(x)
+    input_: torch.Tensor = torch.randn([4, 5, 32])
+    layer: nn.Module = GroupNorm(4, 4)
+
+    out: torch.Tensor = layer(input_)
```

### Comparing `retentive_network-0.0.1/retentive_network/layers/retention.py` & `retentive_network-0.1.0/retentive_network/layers/retention.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,110 +1,63 @@
 import torch
 import torch.nn as nn
+import torch.nn.functional as F
+
+from retentive_network.exceptions import InvalidBatchSizeException
+from retentive_network.layers.projection import Projection
 
 
 class Retention(nn.Module):
     def __init__(
         self,
         hidden_size: int,
+        head_size: int,
         gamma: float,
-        half_point_precision: bool = False,
-        use_complex_numbers: bool = False,
+        chunk_size: int,
+        dtype: torch.dtype = torch.float32,
     ):
         super(Retention, self).__init__()
 
         self.hidden_size: int = hidden_size
+        self.head_size: int = head_size
         self.gamma: float = gamma
-        self.half_point_precision: bool = half_point_precision
-        self.use_complex_numbers: bool = use_complex_numbers
+        self.chunk_size: int = chunk_size
+        self.dtype: torch.dtype = dtype
 
-        self.torch_dtype: torch.dtype = (
-            torch.float16 if self.half_point_precision else torch.float32
+        self.project_q = Projection(
+            hidden_size=self.head_size, bias=False, dtype=self.dtype
         )
-        self.complex_torch_dtype: torch.dtype = (
-            torch.complex32 if self.half_point_precision else torch.complex64
+        self.project_k = Projection(
+            hidden_size=self.head_size, bias=False, dtype=self.dtype
+        )
+        self.project_v = Projection(
+            hidden_size=self.head_size, bias=False, dtype=self.dtype
         )
-
-        self.zero_tensor: torch.Tensor = torch.complex(
-            torch.tensor(0.0), torch.tensor(1.0)
-        ).to(self.complex_torch_dtype)
-        if not self.use_complex_numbers:
-            self.zero_tensor = self.zero_tensor.real
-
-        if self.use_complex_numbers:
-            self.weight_q: nn.Parameter = nn.Parameter(
-                torch.randn(self.hidden_size, self.hidden_size) / self.hidden_size
-            ).to(self.complex_torch_dtype)
-
-            self.weight_k: nn.Parameter = nn.Parameter(
-                torch.randn(self.hidden_size, self.hidden_size) / self.hidden_size
-            ).to(self.complex_torch_dtype)
-
-            self.weight_v: nn.Parameter = nn.Parameter(
-                torch.randn(self.hidden_size, self.hidden_size) / self.hidden_size
-            ).to(self.complex_torch_dtype)
-
-            self.theta: nn.Parameter = nn.Parameter(
-                torch.randn(self.hidden_size) / self.hidden_size
-            ).to(self.complex_torch_dtype)
-        else:
-            self.weight_q: nn.Parameter = nn.Parameter(
-                torch.randn(self.hidden_size, self.hidden_size) / self.hidden_size
-            )
-            self.weight_k: nn.Parameter = nn.Parameter(
-                torch.randn(self.hidden_size, self.hidden_size) / self.hidden_size
-            )
-            self.weight_v: nn.Parameter = nn.Parameter(
-                torch.randn(self.hidden_size, self.hidden_size) / self.hidden_size
-            )
-            self.theta: nn.Parameter = nn.Parameter(
-                torch.randn(self.hidden_size) / self.hidden_size
-            )
 
     def forward(self, x: torch.Tensor) -> torch.Tensor:
         """
         `The Parallel Representation of Retention`
 
         Arguments:
             x (torch.Tensor): Tensor of shape [batch_size, sequence_length, hidden_size]
 
         Returns:
             torch.Tensor: Tensor value after applying parallel retention.
         """
 
+        if x.dtype != self.dtype:
+            x = x.to(self.dtype)
+
         batch_size, sequence_length, hidden_size = x.shape[:3]
         diagonal_matrix: torch.Tensor = self.diagonal_matrix(sequence_length)
 
-        if self.use_complex_numbers:
-            x = x.to(self.complex_torch_dtype)
-
-        thetas = []
-        for seq_dim in range(1, sequence_length + 1):
-            thetas.append(
-                torch.exp(
-                    self.zero_tensor
-                    * torch.tensor(
-                        seq_dim,
-                        dtype=self.complex_torch_dtype
-                        if self.use_complex_numbers
-                        else self.torch_dtype,
-                    )
-                    * self.theta
-                )
-            )
-
-        thetas: torch.Tensor = torch.stack(thetas, dim=0)
-        theta_: torch.Tensor = thetas.conj()
-
-        q: torch.Tensor = torch.matmul(x, self.weight_q) * thetas.unsqueeze(0)
-        k: torch.Tensor = torch.matmul(x, self.weight_k) * theta_.unsqueeze(0)
-        v: torch.Tensor = torch.matmul(x, self.weight_v)
+        q, k, v = self._project_qkv(x)
 
         attention_mask: torch.Tensor = torch.matmul(
-            q, k.permute(0, 2, 1)
+            q, k.transpose(-1, -2)
         ) * diagonal_matrix.unsqueeze(0)
 
         x: torch.Tensor = torch.matmul(attention_mask, v)
         return x
 
     def forward_recurrent(self, x: torch.Tensor, previous_S: torch.Tensor, n: int):
         """
@@ -121,72 +74,183 @@
 
         Returns:
             torch.Tensor: x Tensor value after applying recurrent retention.
             torch.Tensor: s Tensor value to be used in the next
                           recurrent retention forward pass.
         """
 
-        if self.use_complex_numbers:
-            x = x.to(self.complex_torch_dtype)
+        if x.dtype != self.dtype:
+            x = x.to(self.dtype)
 
         n: torch.Tensor = torch.tensor(
             n,
-            dtype=self.complex_torch_dtype
-            if self.use_complex_numbers
-            else self.torch_dtype,
+            dtype=self.dtype,
             requires_grad=False,
         )
-        theta: torch.Tensor = torch.exp(self.zero_tensor * n * self.theta)
-        theta_: torch.Tensor = theta.conj()
 
-        q: torch.Tensor = torch.matmul(x, self.weight_q) * theta
+        q, k, v = self._project_qkv(x)
 
-        k: torch.Tensor = torch.matmul(x, self.weight_k) * theta_
-        v: torch.Tensor = torch.matmul(x, self.weight_v)
-        matmulled = torch.matmul(k.unsqueeze(-1), v.unsqueeze(-2))
+        kv = torch.matmul(k.transpose(-1, -2), v)
 
-        s: torch.Tensor = self.gamma * previous_S + matmulled
+        s: torch.Tensor = self.gamma * previous_S + kv
         x: torch.Tensor = torch.matmul(q.unsqueeze(1), s).squeeze(1)
         return x, s
 
     def diagonal_matrix(self, sequence_length: int) -> torch.Tensor:
         """
         Calculates a diagonal matrix with `1` on the diagonal
         and `gamma ** row` in the lower triangle diagonal row,
-        and returns the matrix as a dtype
-        self.complex_torch_dtype.
+        and returns the matrix as a dtype.
 
         Arguments:
             sequence_length (int): Sequence size.
 
         Returns:
             torch.Tensor: Diagonal Matrix.
 
         """
         x: torch.Tensor = torch.diag(
-            torch.tensor([1.0 for _ in range(sequence_length)], dtype=self.torch_dtype),
+            torch.tensor([1.0 for _ in range(sequence_length)], dtype=self.dtype),
             0,
         )
         for row in range(sequence_length - 1, 0, -1):
             eye: torch.Tensor = torch.tensor(
                 [self.gamma ** (sequence_length - row) for _ in range(sequence_length)],
-                dtype=self.torch_dtype,
+                dtype=self.dtype,
             )
             diagonal: torch.Tensor = torch.diag(eye, sequence_length - row)[
                 :sequence_length, :sequence_length
             ].T
             x += diagonal
 
-        if self.use_complex_numbers:
-            x = x.to(self.complex_torch_dtype)
+        if x.dtype != self.dtype:
+            x = x.to(self.dtype)
 
         return x
 
+    def forward_chunkwise(self, x: torch.Tensor, state: torch.Tensor = None):
+        """
+        Implements a forward pass on a chunk `x` with
+        hidden state `state` and bias `gamma`.
+
+        Arguments:
+            x (torch.Tensor): A Tensor of shape [batch_size, sequence_length, hidden_size].
+            state (torch.Tensor): Torch Tensor of shape [batch_size, hidden_size, hidden_size].
+                                  If None, a zero tensor is created.
+
+        Returns:
+            torch.Tensor: A Tensor of shape [batch_size, sequence_length, hidden_size]
+            torch.Tensor: A Tensor of shape
+                          [batch_size, sequence_length, kv_dim, kv_dim] where kv_dim
+                          is hidden_size // number_of_heads
+
+        """
+
+        if x.dtype != self.dtype:
+            x = x.to(self.dtype)
+
+        batch_size, sequence_length, hidden_size = x.shape
+        if state is None:
+            state = torch.zeros(
+                (batch_size, hidden_size, hidden_size), dtype=self.dtype
+            )
+
+        q, k, v = self._project_qkv(x)
+
+        retention = torch.matmul(q, k.transpose(-1, -2))
+        retention_inner = torch.matmul(retention, v)
+        retention_cross = torch.matmul(q, state)
+
+        out = retention_inner + retention_cross
+
+        # state *= self.gamma
+        kv = torch.matmul(k, v.transpose(-1, -2))
+        kv_dim = hidden_size // sequence_length
+        kv = kv.repeat([1, kv_dim, kv_dim])
+
+        if kv.shape != state.shape:
+            kv = self._pad_kv(kv, state)
+        state += kv
+
+        return out, state
+
+    def _project_qkv(self, x: torch.Tensor) -> torch.Tensor:
+        """
+        Helper method to project Q, K, and V values
+        from x.
+
+        Arguments:
+            x (torch.Tensor): Torch tensor of shape [
+                batch_size, sequence_length,
+                hidden_size, chunk_size
+            ]
+
+        Returns:
+            torch.Tensor: (Q) Torch tensor of shape [
+                batch_size, sequence_length,
+                hidden_size, chunk_size
+            ]
+            torch.Tensor: (K) Torch tensor of shape [
+                batch_size, sequence_length,
+                hidden_size, chunk_size
+            ]
+            torch.Tensor: (V) Torch tensor of shape [
+                batch_size, sequence_length,
+                hidden_size, chunk_size
+            ]
+        """
+
+        q = self.project_q(x)
+        k = self.project_k(x)
+        v = self.project_v(x)
+
+        return q, k, v
+
+    def _pad_kv(self, kv: torch.Tensor, state: torch.Tensor) -> torch.Tensor:
+        """
+        Applies zero-padding to tensor `kv` so that `kv` and `state`
+        become of the same shape. Microsoft may have found a more
+        clever way of doing this in the original codebase, but for
+        now this should not affect the model results.
+
+        Arguments:
+            kv (torch.Tensor): K * V transposed Dot Product.
+            state (torch.Tensor): Current state tensor.
+
+        Returns:
+            torch.Tensor: kv zero-padded to shape of state.
+
+        """
+
+        kv_batch, kv_w, kv_h = kv.shape
+        state_batch, state_w, state_h = state.shape
+
+        if kv_batch != state_batch:
+            raise InvalidBatchSizeException(kv, state)
+
+        else:
+            w_diff = state_w - kv_w
+            h_diff = state_h - kv_h
+            kv = F.pad(input=kv, pad=(0, w_diff, 0, h_diff), mode="constant", value=0)
+
+        return kv
+
 
 if __name__ == "__main__":
-    batch_size, sequence_length, hidden_size = (4, 20, 100)
+    batch_size, sequence_length, hidden_size, chunk_size, head_size = (4, 20, 100, 2, 4)
+    dtype = torch.float32
+
+    input_: torch.Tensor = torch.randn(
+        (batch_size, sequence_length, head_size), dtype=dtype
+    )
+    layer: nn.Module = Retention(
+        hidden_size=hidden_size,
+        head_size=head_size,
+        gamma=0.9,
+        chunk_size=chunk_size,
+    )
+    parallel_out: torch.Tensor = layer(input_)
 
-    input_: torch.Tensor = torch.randn((batch_size, sequence_length, hidden_size))
-    layer: nn.Module = Retention(hidden_size, 0.1, False, False)
-    output: torch.Tensor = layer(input_)
+    recurrent_out, S = layer.forward_recurrent(input_, 0.1234, 2)
+    chunkwise_out, state = layer.forward_chunkwise(x=input_, state=None)
 
-    out, S = layer.forward_recurrent(input_, 0.1234, 2)
+    assert parallel_out.shape == chunkwise_out.shape
```

### Comparing `retentive_network-0.0.1/retentive_network/layers/swish_gate.py` & `retentive_network-0.1.0/retentive_network/layers/swish_gate.py`

 * *Files identical despite different names*

### Comparing `retentive_network-0.0.1/retentive_network/models/clm.py` & `retentive_network-0.1.0/retentive_network/models/clm.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 import torch
 import torch.nn as nn
 
+from retentive_network.exceptions import InvalidTemperatureException
 from retentive_network.models.network import RetentiveNetwork
 
 
 class RetentiveNetworkCLM(nn.Module):
     """
     Huge shoutout to @Jamie-Stirling for
     breaking ground here first. The code below
@@ -18,41 +19,45 @@
     def __init__(
         self,
         number_of_layers: int,
         hidden_size: int,
         number_of_heads: int,
         feed_forward_size: int,
         vocab_size: int,
+        chunk_size: int,
         half_point_precision: bool = False,
         use_complex_numbers: bool = False,
         softmax: bool = False,
     ):
         super(RetentiveNetworkCLM, self).__init__()
 
         self.number_of_layers: int = number_of_layers
         self.hidden_size: int = hidden_size
         self.number_of_heads: int = number_of_heads
         self.feed_forward_size: int = feed_forward_size
         self.vocab_size: int = vocab_size
+        self.chunk_size: int = chunk_size
         self.half_point_precision: bool = half_point_precision
         self.use_complex_numbers: bool = use_complex_numbers
         self.softmax: bool = softmax
 
         self.torch_dtype: torch.dtype = (
             torch.float16 if self.half_point_precision else torch.float32
         )
-        self.complex_torch_dtype: torch.dtype = (
-            torch.complex32 if self.half_point_precision else torch.complex64
-        )
+        if self.use_complex_numbers:
+            self.torch_dtype: torch.dtype = (
+                torch.complex32 if self.half_point_precision else torch.complex64
+            )
 
         self.model: nn.Module = RetentiveNetwork(
             number_of_layers=self.number_of_layers,
             hidden_size=self.hidden_size,
             number_of_heads=self.number_of_heads,
             feed_forward_size=self.feed_forward_size,
+            chunk_size=self.chunk_size,
             half_point_precision=self.half_point_precision,
             use_complex_numbers=self.use_complex_numbers,
         )
         self.embedding_layer: nn.Module = nn.Embedding(self.vocab_size, hidden_size)
         self.projection: torch.Tensor = nn.Parameter(
             torch.randn(hidden_size, self.vocab_size, dtype=self.torch_dtype)
             / hidden_size
@@ -87,14 +92,15 @@
         x: torch.Tensor = self.embedding_layer(x)
         x: torch.Tensor = self.model(x)
         x: torch.Tensor = torch.matmul(x, self.projection.to(x.dtype))
         x: torch.Tensor = x.real
 
         if self.softmax:
             x = self.softmax_layer(x)
+            x = torch.mean(x, dim=-1)
 
         return x
 
     def forward_recurrent(self, x, previous_Ses, n):
         """
         Forward pass includes passing `x` of shape
         [batch_size, sequence_length] and passes it
@@ -123,20 +129,58 @@
         x: torch.Tensor = self.embedding_layer(x)
         x, ses = self.model.forward_recurrent(x, previous_Ses, n)
         x: torch.Tensor = torch.matmul(x, self.projection.to(x.dtype))
         x: torch.Tensor = x.real
 
         if self.softmax:
             x = self.softmax_layer(x)
+            x = torch.mean(x, dim=-1)
 
         return x, ses
 
+    def forward_chunkwise(self, x: torch.Tensor, state: torch.Tensor = None):
+        """
+        Chunkwise forward pass includes passing `x` 
+        of shape [batch_size, sequence_length] and 
+        passes it through an embedding layer to shape
+        [batch_size, sequence_length, hidden_size].
+        This tensor is then passed through the
+        recurrent pass of the RetentiveNetwork
+        model before being projected into a tensor
+        of shape [batch_size, self.vocab_size].
+
+        Arguments:
+            x (torch.Tensor): Tensor of shape [
+                batch_size,
+                sequence_length
+            ].
+            previous_Ses (list): List of floats containing previous S values.
+            n (int): The current nth iteration.
+
+        Returns:
+            torch.Tensor: Tensor of shape [
+                batch_size,
+                self.vocab_size
+            ].
+        """
+
+        x: torch.Tensor = self.embedding_layer(x)
+        x, state = self.model.forward_chunkwise(x, state)
+        x: torch.Tensor = torch.matmul(x, self.projection.to(x.dtype))
+        x: torch.Tensor = x.real
+
+        if self.softmax:
+            x = self.softmax_layer(x)
+            x = torch.mean(x, dim=-1)
+
+        return x, state
+
     def sample(
         self,
-        input_ids: torch.Tensor,
+        x: torch.Tensor,
         sample_length: int,
         temperature: float = 1.0,
         number_of_samples: int = 1,
     ):
         """
         Uses the recurrent pass of the Retentive Network
         model to generate an output id response given
@@ -152,29 +196,28 @@
                                  of the model.
             number_of_samples (int): How many samples to generate from `x`.
 
         Returns:
             torch.Tensor: Tensor of shape [batch_size, `sample_length`]
         """
 
-        assert temperature > 0, f"temperature must be greater than 0"
-        batch_size, sequence_length = input_ids.shape
+        if temperature <= 0 or temperature > 1:
+            raise InvalidTemperatureException(temperature)
+        batch_size, sequence_length = x.shape
 
         previous_Ses = [
             [
                 torch.zeros(batch_size, self.head_size, self.head_size)
                 for _ in range(self.number_of_heads)
             ]
             for _ in range(self.number_of_layers)
         ]
 
         for idx in range(sequence_length):
-            X, previous_Ses = self.forward_recurrent(
-                input_ids[:, idx], previous_Ses, idx + 1
-            )
+            X, previous_Ses = self.forward_recurrent(x[:, idx], previous_Ses, idx + 1)
 
         original_x = self._multinomial_probability_distribution(
             x=X, temperature=temperature, number_of_samples=number_of_samples
         )
 
         samples = []
         for sample_idx in range(number_of_samples):
@@ -232,24 +275,26 @@
     hidden_size = 16
     number_of_heads = 8
     sequence_length = 100
     feed_forward_size = 32
     vocab_size = 10
     sample_length = 20
     number_of_samples = 3
+    chunk_size = 4
     softmax = True
 
     X = torch.randint(0, vocab_size, (batch_size, sequence_length))
 
     model = RetentiveNetworkCLM(
         number_of_layers=number_of_layers,
         hidden_size=hidden_size,
         number_of_heads=number_of_heads,
         feed_forward_size=feed_forward_size,
         vocab_size=vocab_size,
+        chunk_size=chunk_size,
         softmax=softmax,
     )
     parallel_out = model(X)
 
     head_size = model.model.retention_layers[0].head_size
 
     previous_Ses = [
```

