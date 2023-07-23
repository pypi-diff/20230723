# Comparing `tmp/quantflow-0.2.3.tar.gz` & `tmp/quantflow-0.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "quantflow-0.2.3.tar", max compression
+gzip compressed data, was "quantflow-0.2.4.tar", max compression
```

## Comparing `quantflow-0.2.3.tar` & `quantflow-0.2.4.tar`

### file list

```diff
@@ -1,38 +1,38 @@
--rw-r--r--   0        0        0     1461 2023-07-20 16:33:40.739003 quantflow-0.2.3/LICENSE
--rw-r--r--   0        0        0     1874 2023-07-20 16:33:40.747003 quantflow-0.2.3/pyproject.toml
--rw-r--r--   0        0        0       62 2023-07-20 16:33:40.747003 quantflow-0.2.3/quantflow/__init__.py
--rw-r--r--   0        0        0        0 2023-07-20 16:33:40.747003 quantflow-0.2.3/quantflow/data/__init__.py
--rw-r--r--   0        0        0     2840 2023-07-20 16:33:40.747003 quantflow-0.2.3/quantflow/data/client.py
--rw-r--r--   0        0        0     5374 2023-07-20 16:33:40.747003 quantflow-0.2.3/quantflow/data/fmp.py
--rw-r--r--   0        0        0        0 2023-07-20 16:33:40.747003 quantflow-0.2.3/quantflow/options/__init__.py
--rw-r--r--   0        0        0     2032 2023-07-20 16:33:40.747003 quantflow-0.2.3/quantflow/options/bs.py
--rw-r--r--   0        0        0     7289 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/options/calibration.py
--rw-r--r--   0        0        0     1021 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/options/inputs.py
--rw-r--r--   0        0        0     5751 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/options/pricer.py
--rw-r--r--   0        0        0    20309 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/options/surface.py
--rw-r--r--   0        0        0        0 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/py.typed
--rw-r--r--   0        0        0        0 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/__init__.py
--rwxr-xr-x   0        0        0     6495 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/base.py
--rw-r--r--   0        0        0     2479 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/bns.py
--rwxr-xr-x   0        0        0     5307 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/cir.py
--rwxr-xr-x   0        0        0     2079 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/dsp.py
--rw-r--r--   0        0        0     4791 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/heston.py
--rw-r--r--   0        0        0     2862 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/jump_diffusion.py
--rwxr-xr-x   0        0        0     6032 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/ou.py
--rwxr-xr-x   0        0        0     5764 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/poisson.py
--rw-r--r--   0        0        0     1492 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/sp/weiner.py
--rw-r--r--   0        0        0        0 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/__init__.py
--rw-r--r--   0        0        0     1613 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/bins.py
--rw-r--r--   0        0        0      252 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/dates.py
--rw-r--r--   0        0        0     3330 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/distributions.py
--rwxr-xr-x   0        0        0      496 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/functions.py
--rw-r--r--   0        0        0     1265 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/interest_rates.py
--rw-r--r--   0        0        0     9909 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/marginal.py
--rw-r--r--   0        0        0      370 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/numbers.py
--rwxr-xr-x   0        0        0     3689 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/paths.py
--rw-r--r--   0        0        0     4185 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/plot.py
--rw-r--r--   0        0        0     5987 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/transforms.py
--rw-r--r--   0        0        0      721 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/types.py
--rw-r--r--   0        0        0     2091 2023-07-20 16:33:40.751003 quantflow-0.2.3/quantflow/utils/volatility.py
--rw-r--r--   0        0        0     1342 2023-07-20 16:33:40.751003 quantflow-0.2.3/readme.md
--rw-r--r--   0        0        0     2197 1970-01-01 00:00:00.000000 quantflow-0.2.3/PKG-INFO
+-rw-r--r--   0        0        0     1461 2023-07-23 13:31:07.146493 quantflow-0.2.4/LICENSE
+-rw-r--r--   0        0        0     1835 2023-07-23 13:31:07.154493 quantflow-0.2.4/pyproject.toml
+-rw-r--r--   0        0        0       62 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/data/__init__.py
+-rw-r--r--   0        0        0     3046 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/data/client.py
+-rw-r--r--   0        0        0     5303 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/data/fmp.py
+-rw-r--r--   0        0        0        0 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/options/__init__.py
+-rw-r--r--   0        0        0     2032 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/options/bs.py
+-rw-r--r--   0        0        0     7289 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/options/calibration.py
+-rw-r--r--   0        0        0     1021 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/options/inputs.py
+-rw-r--r--   0        0        0     5751 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/options/pricer.py
+-rw-r--r--   0        0        0    20309 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/options/surface.py
+-rw-r--r--   0        0        0        0 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/py.typed
+-rw-r--r--   0        0        0        0 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/__init__.py
+-rwxr-xr-x   0        0        0     6495 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/base.py
+-rw-r--r--   0        0        0     2479 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/bns.py
+-rwxr-xr-x   0        0        0     5452 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/cir.py
+-rwxr-xr-x   0        0        0     1522 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/dsp.py
+-rw-r--r--   0        0        0     4791 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/heston.py
+-rw-r--r--   0        0        0     2896 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/jump_diffusion.py
+-rwxr-xr-x   0        0        0     6008 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/ou.py
+-rwxr-xr-x   0        0        0     5572 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/poisson.py
+-rw-r--r--   0        0        0     1504 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/sp/weiner.py
+-rw-r--r--   0        0        0        0 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/utils/__init__.py
+-rw-r--r--   0        0        0     1674 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/utils/bins.py
+-rw-r--r--   0        0        0      252 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/utils/dates.py
+-rw-r--r--   0        0        0     3330 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/utils/distributions.py
+-rwxr-xr-x   0        0        0      496 2023-07-23 13:31:07.154493 quantflow-0.2.4/quantflow/utils/functions.py
+-rw-r--r--   0        0        0     1265 2023-07-23 13:31:07.158493 quantflow-0.2.4/quantflow/utils/interest_rates.py
+-rw-r--r--   0        0        0     9909 2023-07-23 13:31:07.158493 quantflow-0.2.4/quantflow/utils/marginal.py
+-rw-r--r--   0        0        0      370 2023-07-23 13:31:07.158493 quantflow-0.2.4/quantflow/utils/numbers.py
+-rwxr-xr-x   0        0        0     4045 2023-07-23 13:31:07.158493 quantflow-0.2.4/quantflow/utils/paths.py
+-rw-r--r--   0        0        0     4261 2023-07-23 13:31:07.158493 quantflow-0.2.4/quantflow/utils/plot.py
+-rw-r--r--   0        0        0     5987 2023-07-23 13:31:07.158493 quantflow-0.2.4/quantflow/utils/transforms.py
+-rw-r--r--   0        0        0      721 2023-07-23 13:31:07.158493 quantflow-0.2.4/quantflow/utils/types.py
+-rw-r--r--   0        0        0     2091 2023-07-23 13:31:07.158493 quantflow-0.2.4/quantflow/utils/volatility.py
+-rw-r--r--   0        0        0     1342 2023-07-23 13:31:07.158493 quantflow-0.2.4/readme.md
+-rw-r--r--   0        0        0     2197 1970-01-01 00:00:00.000000 quantflow-0.2.4/PKG-INFO
```

### Comparing `quantflow-0.2.3/LICENSE` & `quantflow-0.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/pyproject.toml` & `quantflow-0.2.4/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "quantflow"
-version = "0.2.3"
+version = "0.2.4"
 description = "quantitative analysis"
 authors = ["Luca <luca@quantmind.com>"]
 license = "BSD-3-Clause"
 readme = "readme.md"
 
 [tool.poetry.urls]
 Homepage = "https://github.com/quantmind/quantflow"
@@ -24,31 +24,28 @@
 pytest-cov = "^4.0.0"
 mypy = "^1.4.0"
 ghp-import = "^2.0.2"
 ruff = "^0.0.277"
 pytest-asyncio = "^0.21.1"
 
 
-[tool.poetry.group.bok.dependencies]
-ipywidgets = "^8.0.7"
-
 [tool.poetry.extras]
 data = ["aiohttp"]
 
 [tool.poetry.group.book]
 optional = true
 
 [tool.poetry.group.book.dependencies]
 jupyter-book = "^0.15.1"
 nbconvert = "^6.4.5"
 jupytext = "^1.13.8"
 plotly = "^5.7.0"
 jupyterlab = "^4.0.2"
 sympy = "^1.12"
-
+ipywidgets = "^8.0.7"
 
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.jupytext]
 formats = "ipynb,myst"
```

### Comparing `quantflow-0.2.3/quantflow/data/client.py` & `quantflow-0.2.4/quantflow/data/client.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import json
 import os
+from dataclasses import dataclass
 from typing import Any
 
 from aiohttp import ClientResponse, ClientSession
 from aiohttp.client_exceptions import ContentTypeError
 
 ResponseType = dict | list
 
@@ -24,28 +25,34 @@
     def status(self) -> int:
         return self.response.status
 
     def __str__(self) -> str:
         return json.dumps(self.data, indent=4)
 
 
+@dataclass
 class HttpClient:
     session: ClientSession | None = None
     user_agent: str = os.getenv("HTTP_USER_AGENT", "quantflow/data")
     content_type: str = "application/json"
+    session_owner: bool = False
     ResponseError: type[HttpResponseError] = HttpResponseError
-    ok_status = frozenset((200, 201))
+    ok_status: frozenset = frozenset((200, 201))
+
+    def new_session(self, **kwargs: Any) -> ClientSession:
+        return ClientSession(**kwargs)
 
     def get_session(self) -> ClientSession:
         if not self.session:
+            self.session_owner = True
             self.session = ClientSession()
         return self.session
 
     async def close(self) -> None:
-        if self.session:
+        if self.session and self.session_owner:
             await self.session.close()
             self.session = None
 
     async def __aenter__(self) -> "HttpClient":
         return self
 
     async def __aexit__(self, *args: Any) -> None:
@@ -73,17 +80,14 @@
         else:
             data = await self.response_error(response)
             raise self.ResponseError(response, data)
 
     def default_headers(self) -> dict[str, str]:
         return {"user-agent": self.user_agent, "accept": self.content_type}
 
-    def mock(self) -> None:
-        pass
-
     @classmethod
     async def response_error(cls, response: ClientResponse) -> ResponseType:
         try:
             return await cls.response_data(response)
         except ContentTypeError:
             return dict(message=await response.text())
```

### Comparing `quantflow-0.2.3/quantflow/data/fmp.py` & `quantflow-0.2.4/quantflow/data/fmp.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,26 +1,22 @@
 import os
+from dataclasses import dataclass
 from datetime import date, timedelta
 from typing import Any, cast
 
 import pandas as pd
 
-from .client import HttpClient, compact
 from ..utils.dates import isoformat
+from .client import HttpClient, compact
 
 
+@dataclass
 class FMP(HttpClient):
-    def __init__(
-        self,
-        *,
-        url: str = "https://financialmodelingprep.com/api",
-        key: str = "",
-    ) -> None:
-        self.url = url
-        self.key = key or os.environ.get("FMP_API_KEY")
+    url: str = "https://financialmodelingprep.com/api"
+    key: str = os.environ.get("FMP_API_KEY", "")
 
     async def stocks(self, **kw: Any) -> list[dict]:
         return await self.get_path("v3/stock/list", **kw)
 
     async def etfs(self, **kw: Any) -> list[dict]:
         return await self.get_path("v3/etf/list", **kw)
```

### Comparing `quantflow-0.2.3/quantflow/options/bs.py` & `quantflow-0.2.4/quantflow/options/bs.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/options/calibration.py` & `quantflow-0.2.4/quantflow/options/calibration.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/options/inputs.py` & `quantflow-0.2.4/quantflow/options/inputs.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/options/pricer.py` & `quantflow-0.2.4/quantflow/options/pricer.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/options/surface.py` & `quantflow-0.2.4/quantflow/options/surface.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/sp/base.py` & `quantflow-0.2.4/quantflow/sp/base.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/sp/bns.py` & `quantflow-0.2.4/quantflow/sp/bns.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/sp/cir.py` & `quantflow-0.2.4/quantflow/sp/cir.py`

 * *Files 4% similar despite different names*

```diff
@@ -110,25 +110,29 @@
         s2u = iu * sigma2
         c = s2u + (2 * kappa - s2u) * ekt
         b = 2 * kappa * iu / c
         a = 2 * kappa * self.theta * (kt + np.log(2 * kappa / c)) / sigma2
         return -a - b * self.rate
 
     def integrated_log_laplace(self, t: Vector, u: Vector) -> Vector:
-        iu = Im * u
-        sigma = self.sigma
+        """Integrated log Laplace transform of the process
+
+        This is the log of the Laplace transform of the process integrated
+        over time.
+        """
         kappa = self.kappa
-        sigma2 = sigma * sigma
-        gamma = np.sqrt(kappa * kappa - 2 * iu * sigma2)
+        sigma2 = self.sigma2
+        gamma = np.sqrt(kappa * kappa + 2 * u * sigma2)
+        kts = 2 * kappa * self.theta / sigma2
+        gamma_kappa = gamma + kappa
         egt = np.exp(gamma * t)
-        c = (gamma + kappa) * (1 - egt) - 2 * gamma
-        d = 2 * gamma * np.exp(0.5 * (gamma + kappa) * t)
-        a = 2 * self.theta * kappa * np.log(-d / c) / sigma2
-        b = 2 * iu * (1 - egt) / c
-        return -a - b * self.rate
+        d = 2 * gamma + gamma_kappa * (egt - 1)
+        a = 2 * gamma * np.exp(0.5 * gamma_kappa * t) / d
+        b = 2 * u * (egt - 1) / d
+        return kts * np.log(a) - b * self.rate
 
     def domain_range(self) -> Bounds:
         return Bounds(0, np.inf)
 
     def analytical_mean(self, t: FloatArrayLike) -> FloatArrayLike:
         ekt = self.ekt(t)
         return self.rate * ekt + self.theta * (1 - ekt)
```

### Comparing `quantflow-0.2.3/quantflow/sp/dsp.py` & `quantflow-0.2.4/quantflow/sp/dsp.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import math
 
 import numpy as np
 from pydantic import Field
+from scipy.optimize import Bounds
 
-from ..utils.types import FloatArray, FloatArrayLike, Vector, as_array
-from .base import Im
+from ..utils.types import FloatArray, FloatArrayLike, Vector
 from .cir import CIR, IntensityProcess
 from .poisson import PoissonBase, PoissonProcess, poisson_arrivals
 
 
 class DSP(PoissonBase):
     r"""
     Doubly Stochastic Poisson process.
@@ -19,41 +19,24 @@
     :param intensity: the stochastic intensity of the Poisson
     """
     intensity: IntensityProcess = Field(  # type ignore
         default_factory=CIR, description="intensity process"
     )
     poisson: PoissonProcess = Field(default_factory=PoissonProcess, exclude=True)
 
-    def pdf(self, t: float, n: Vector = 0) -> Vector:
-        """PDF of the number of events at time t.
+    def frequency_range(self, std: float, max_frequency: float | None = None) -> Bounds:
+        """Frequency range of the process"""
+        return Bounds(0, np.pi)
 
-        It is obtained via inverse Fourier transform of the characteristic function
-        """
-        nn = as_array(n)
-        size = nn.shape[0]
-        assert (
-            size > 0 and np.log2(size).is_integer()
-        ), "Must pass a power of two array of integers"
-        u = -2 * np.pi * np.fft.rfftfreq(size)
-        psi = self.characteristic(t, u)
-        return np.fft.irfft(psi)
-
-    def cdf(self, t: float, n: Vector) -> Vector:
-        """CDF of the number of events at time t.
-
-        It is obtained form cumulative summation of :class:`pdf`
-        """
-        return np.cumsum(self.pdf(t, n))
+    def support(self, mean: float, std: float, points: int) -> FloatArray:
+        return np.linspace(0, points, points + 1)
 
     def characteristic_exponent(self, t: FloatArrayLike, u: Vector) -> Vector:
-        return self.poisson.characteristic_exponent(t, u)
-
-    def characteristic(self, t: FloatArrayLike, u: Vector) -> Vector:
-        phi = self.characteristic_exponent(t, u)
-        return np.exp(self.intensity.integrated_log_laplace(t, -Im * phi))
+        phi = self.poisson.characteristic_exponent(t, u)
+        return -self.intensity.integrated_log_laplace(t, phi)
 
     def arrivals(self, t: float = 1) -> list[float]:
         paths = self.intensity.sample(1, t, math.ceil(100 * t)).integrate()
         intensity = paths.data[-1, 0]
         return poisson_arrivals(intensity, t)
 
     def sample_jumps(self, n: int) -> FloatArray:
```

### Comparing `quantflow-0.2.3/quantflow/sp/heston.py` & `quantflow-0.2.4/quantflow/sp/heston.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/sp/jump_diffusion.py` & `quantflow-0.2.4/quantflow/sp/jump_diffusion.py`

 * *Files 2% similar despite different names*

```diff
@@ -21,15 +21,15 @@
 
         where N_t is a compound poisson process with intensity \lambda
         and jump distribution D
     """
     diffusion: WeinerProcess = Field(
         default_factory=WeinerProcess, description="diffusion"
     )
-    jumps: CompoundPoissonProcess[Normal] = Field(description="jump process")
+    jumps: CompoundPoissonProcess[D] = Field(description="jump process")
 
     def characteristic_exponent(self, t: FloatArrayLike, u: Vector) -> Vector:
         return self.diffusion.characteristic_exponent(
             t, u
         ) + self.jumps.characteristic_exponent(t, u)
 
     def sample(self, n: int, time_horizon: float = 1, time_steps: int = 100) -> Paths:
@@ -48,14 +48,16 @@
         return self.diffusion.analytical_mean(t) + self.jumps.analytical_mean(t)
 
     def analytical_variance(self, t: FloatArrayLike) -> FloatArrayLike:
         return self.diffusion.analytical_variance(t) + self.jumps.analytical_variance(t)
 
 
 class Merton(JumpDiffusion[Normal]):
+    """Merton jump-diffusion model"""
+
     @classmethod
     def create(
         cls,
         vol: float = 0.5,
         diffusion_percentage: float = 0.5,
         jump_intensity: float = 100,
         jump_skew: float = 0.0,
```

### Comparing `quantflow-0.2.3/quantflow/sp/ou.py` & `quantflow-0.2.4/quantflow/sp/ou.py`

 * *Files 0% similar despite different names*

```diff
@@ -43,17 +43,16 @@
         kappa = self.kappa
         theta = self.theta
         dt = draws.dt
         sdt = self.bdlp.sigma * np.sqrt(dt)
         paths = np.zeros(draws.data.shape)
         paths[0, :] = self.rate
         for t in range(draws.time_steps):
-            w = sdt * draws.data[t, :]
             x = paths[t, :]
-            dx = kappa * (theta - x) * dt + sdt * w
+            dx = kappa * (theta - x) * dt + sdt * draws.data[t, :]
             paths[t + 1, :] = x + dx
         return Paths(t=draws.t, data=paths)
 
     def domain_range(self) -> Bounds:
         return Bounds(-np.inf, np.inf)
 
     def analytical_mean(self, t: FloatArrayLike) -> FloatArrayLike:
```

### Comparing `quantflow-0.2.3/quantflow/sp/poisson.py` & `quantflow-0.2.4/quantflow/sp/poisson.py`

 * *Files 9% similar despite different names*

```diff
@@ -130,24 +130,16 @@
         """
         k = np.floor(n).astype(int)
         rate = self.intensity
         return np.array([-(rate**k) * np.exp(-rate)]) / factorial(k)
 
 
 class CompoundPoissonProcess(PoissonBase, Generic[D]):
-    r"""
-    1D Poisson process.
+    """Compound Poisson process."""
 
-    It's a process where the inter-arrival time is exponentially distributed
-    with rate :math:`\lambda`
-
-    .. attribute:: rate
-
-        The arrival rate of events. Must be positive.
-    """
     intensity: float = Field(default=1.0, ge=0, description="intensity rate")
     jumps: D = Field(description="Jump size distribution")
 
     def characteristic_exponent(self, t: FloatArrayLike, u: Vector) -> Vector:
         return t * self.intensity * (1 - self.jumps.characteristic(u))
 
     def arrivals(self, time_horizon: float = 1) -> list[float]:
```

### Comparing `quantflow-0.2.3/quantflow/sp/weiner.py` & `quantflow-0.2.4/quantflow/sp/weiner.py`

 * *Files 4% similar despite different names*

```diff
@@ -21,18 +21,18 @@
         return 0.5 * su * su * t
 
     def sample(self, n: int, time_horizon: float = 1, time_steps: int = 100) -> Paths:
         paths = Paths.normal_draws(n, time_horizon, time_steps)
         return self.sample_from_draws(paths)
 
     def sample_from_draws(self, draws: Paths, *args: Paths) -> Paths:
-        self.sigma * np.sqrt(draws.dt)
+        sdt = self.sigma * np.sqrt(draws.dt)
         paths = np.zeros(draws.data.shape)
         paths[1:] = np.cumsum(draws.data[:-1], axis=0)
-        return Paths(t=draws.t, data=paths)
+        return Paths(t=draws.t, data=sdt * paths)
 
     def analytical_mean(self, t: FloatArrayLike) -> FloatArrayLike:
         return 0 * t
 
     def analytical_variance(self, t: FloatArrayLike) -> FloatArrayLike:
         return t * self.sigma2
```

### Comparing `quantflow-0.2.3/quantflow/utils/bins.py` & `quantflow-0.2.4/quantflow/utils/bins.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from typing import Dict, Sequence
 
 import numpy as np
 from pandas import DataFrame
+
 from .types import FloatArray
 
 
 def pdf(
     data: FloatArray,
     num_bins: int | None = None,
     delta: float | None = None,
@@ -13,32 +14,33 @@
     precision: int = 6,
 ) -> DataFrame:
     max_value = np.max(data)
     min_value = np.min(data)
     domain = max(abs(data)) if symmetric is not None else max_value - min_value
     if num_bins is None:
         if not delta:
-            num_bins = num_bins or 50
-            delta_ = round(domain / num_bins, precision)
+            num_bins = 50
+            delta_ = round(domain / (num_bins - 1), precision)
         else:
             delta_ = delta
             num_bins = round(domain / delta_)
     else:
         if delta:
             raise ValueError("Cannot specify both num_bins and delta")
-        delta_ = round(domain / num_bins, precision)
+        if num_bins < 2:
+            raise ValueError("num_bins must be greater than 1")
+        delta_ = round(domain / (num_bins - 1), precision)
     if symmetric is not None:
         b = (num_bins + 0.5) * delta_
         min_value = symmetric - b
         max_value = symmetric + b
     x = np.arange(min_value - delta_, max_value + 2 * delta_, delta_)
     bins = (x[:-1] + x[1:]) * 0.5
-    counts, _ = np.histogram(data, bins=bins)
-    counts = counts / np.sum(counts)
-    return DataFrame(dict(pdf=counts), index=x[1:-1])
+    pdf, _ = np.histogram(data, bins=bins, density=True)
+    return DataFrame(dict(pdf=pdf), index=x[1:-1])
 
 
 def event_density(df: DataFrame, columns: Sequence, num: int = 10) -> Dict:
     """Calculate the probability density of the number of events
     in the dataframe columns
     """
     bins = np.linspace(-0.5, num - 0.5, num + 1)
```

### Comparing `quantflow-0.2.3/quantflow/utils/distributions.py` & `quantflow-0.2.4/quantflow/utils/distributions.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/utils/interest_rates.py` & `quantflow-0.2.4/quantflow/utils/interest_rates.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/utils/marginal.py` & `quantflow-0.2.4/quantflow/utils/marginal.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/utils/paths.py` & `quantflow-0.2.4/quantflow/utils/paths.py`

 * *Files 5% similar despite different names*

```diff
@@ -21,57 +21,62 @@
 
     @property
     def dt(self) -> float:
         return self.t / self.time_steps
 
     @property
     def samples(self) -> int:
+        """Number of samples"""
         return self.data.shape[1]
 
     @property
     def time_steps(self) -> int:
+        """Number of time steps"""
         return self.data.shape[0] - 1
 
     @property
-    def time(self) -> np.ndarray:
+    def time(self) -> FloatArray:
+        """Time as numpy array"""
         return np.linspace(0.0, self.t, num=self.time_steps + 1)
 
     @property
     def df(self) -> pd.DataFrame:
+        """Paths as pandas DataFrame"""
         return pd.DataFrame(self.data, index=self.time)
 
     @property
     def xs(self) -> list[np.ndarray]:
         """Time as list of list (for visualization tools)"""
         return self.samples * [self.time]
 
     @property
     def ys(self) -> list[list[float]]:
         """Paths as list of list (for visualization tools)"""
         return self.data.transpose().tolist()
 
-    def mean(self) -> np.ndarray:
+    def mean(self) -> FloatArray:
         """Mean of paths"""
         return np.mean(self.data, axis=1)
 
-    def std(self) -> np.ndarray:
+    def std(self) -> FloatArray:
         """Standard deviation of paths"""
         return np.std(self.data, axis=1)
 
-    def var(self) -> np.ndarray:
+    def var(self) -> FloatArray:
         """Variance of paths"""
         return np.var(self.data, axis=1)
 
     def integrate(self) -> Paths:
         """Integrate paths"""
         return self.__class__(
             t=self.t, data=cumtrapz(self.data, dx=self.dt, axis=0, initial=0)
         )
 
     def cross_section(self, t: float | None = None) -> FloatArray:
+        """Cross section of paths at time t"""
         index = self.time_steps
         if t is not None:
             index = cast(int, t // self.dt)
         return self.data[index, :]
 
     def pdf(
         self,
@@ -91,29 +96,34 @@
         :param symmetric: optional center of bins
         """
         return bins_pdf(
             self.cross_section(t), num_bins=num_bins, delta=delta, symmetric=symmetric
         )
 
     def plot(self, **kwargs: Any) -> Any:
+        """Plot paths
+
+        It requires plotly installed
+        """
         return plot.plot_lines(self.df, **kwargs)
 
     @classmethod
     def normal_draws(
         cls,
         paths: int,
-        time_horizon: float,
+        time_horizon: float = 1,
         time_steps: int = 1000,
         antithetic_variates: bool = True,
     ) -> Paths:
         """Generate normal draws
 
-        paths: number of paths
-        time_horizon: time horizon
-        time_steps: number of time steps to arrive at horizon
+        :param paths: number of paths
+        :param time_horizon: time horizon
+        :param time_steps: number of time steps to arrive at horizon
+        :param antithetic_variates: whether to use antithetic variates
         """
         time_horizon / time_steps
         odd = 0
         if antithetic_variates:
             odd = paths % 2
             paths = paths // 2
         data = normal(size=(time_steps + 1, paths))
```

### Comparing `quantflow-0.2.3/quantflow/utils/plot.py` & `quantflow-0.2.4/quantflow/utils/plot.py`

 * *Files 2% similar despite different names*

```diff
@@ -33,21 +33,24 @@
     m: Marginal1D,
     n: int | None = None,
     *,
     analytical: str | bool = "lines",
     normal: bool = False,
     marker_size: int = 8,
     marker_color: str = "rgba(30, 186, 64, .5)",
+    label: str = "characteristic PDF",
     log_y: bool = False,
+    fig: Any | None = None,
     **kwargs: Any
 ) -> Any:
     """Plot the marginal pdf on an input support"""
     check_plotly()
     pdf = m.pdf_from_characteristic(n, **kwargs)
-    fig = go.Figure()
+    if fig is None:
+        fig = go.Figure()
     if analytical:
         fig.add_trace(
             go.Scatter(
                 x=pdf.x,
                 y=m.pdf(pdf.x),
                 name="analytical",
                 mode=analytical,
@@ -64,15 +67,15 @@
             )
         )
 
     fig.add_trace(
         go.Scatter(
             x=pdf.x,
             y=pdf.y,
-            name="characteristic PDF",
+            name=label,
             mode="markers",
             marker_color=marker_color,
             marker_size=marker_size,
         )
     )
     if log_y:
         fig.update_yaxes(type="log")
```

### Comparing `quantflow-0.2.3/quantflow/utils/transforms.py` & `quantflow-0.2.4/quantflow/utils/transforms.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/utils/types.py` & `quantflow-0.2.4/quantflow/utils/types.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/quantflow/utils/volatility.py` & `quantflow-0.2.4/quantflow/utils/volatility.py`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/readme.md` & `quantflow-0.2.4/readme.md`

 * *Files identical despite different names*

### Comparing `quantflow-0.2.3/PKG-INFO` & `quantflow-0.2.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: quantflow
-Version: 0.2.3
+Version: 0.2.4
 Summary: quantitative analysis
 License: BSD-3-Clause
 Author: Luca
 Author-email: luca@quantmind.com
 Requires-Python: >=3.10,<3.12
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Programming Language :: Python :: 3
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: quantflow Version: 0.2.3 Summary: quantitative
+Metadata-Version: 2.1 Name: quantflow Version: 0.2.4 Summary: quantitative
 analysis License: BSD-3-Clause Author: Luca Author-email: luca@quantmind.com
 Requires-Python: >=3.10,<3.12 Classifier: License :: OSI Approved :: BSD
 License Classifier: Programming Language :: Python :: 3 Classifier: Programming
 Language :: Python :: 3.10 Classifier: Programming Language :: Python :: 3.11
 Provides-Extra: data Requires-Dist: aiohttp (>=3.8.1,<4.0.0) ; extra == "data"
 Requires-Dist: numpy (>=1.22.3,<2.0.0) Requires-Dist: pandas (>=2.0.1,<3.0.0)
 Requires-Dist: pydantic (>=2.0.2,<3.0.0) Requires-Dist: scipy (>=1.10.1,<2.0.0)
```

