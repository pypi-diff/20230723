# Comparing `tmp/w7x-0.5.2-py3-none-any.whl.zip` & `tmp/w7x-0.6.0-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,61 +1,62 @@
-Zip file size: 125091 bytes, number of entries: 59
+Zip file size: 126586 bytes, number of entries: 60
 -rw-r--r--  2.0 unx      571 b- defN 80-Jan-01 00:00 w7x/__init__.py
 -rw-r--r--  2.0 unx     8105 b- defN 80-Jan-01 00:00 w7x/__main__.py
 -rw-r--r--  2.0 unx     3008 b- defN 80-Jan-01 00:00 w7x/compatibility.py
--rw-r--r--  2.0 unx     4839 b- defN 80-Jan-01 00:00 w7x/conf/config.yaml
--rw-r--r--  2.0 unx    24031 b- defN 80-Jan-01 00:00 w7x/config.py
--rw-r--r--  2.0 unx    19830 b- defN 80-Jan-01 00:00 w7x/core.py
+-rw-r--r--  2.0 unx     4858 b- defN 80-Jan-01 00:00 w7x/conf/config.yaml
+-rw-r--r--  2.0 unx    23743 b- defN 80-Jan-01 00:00 w7x/config.py
+-rw-r--r--  2.0 unx    20312 b- defN 80-Jan-01 00:00 w7x/core.py
 -rw-r--r--  2.0 unx       89 b- defN 80-Jan-01 00:00 w7x/lib/__init__.py
 -rw-r--r--  2.0 unx     3866 b- defN 80-Jan-01 00:00 w7x/lib/dataclasses.py
 -rw-r--r--  2.0 unx    17525 b- defN 80-Jan-01 00:00 w7x/lib/equilibrium.py
 -rw-r--r--  2.0 unx    15963 b- defN 80-Jan-01 00:00 w7x/lib/profiles.py
 -rw-r--r--  2.0 unx     7864 b- defN 80-Jan-01 00:00 w7x/lib/tfields.py
 -rw-r--r--  2.0 unx     3221 b- defN 80-Jan-01 00:00 w7x/lib/timeout.py
 -rw-r--r--  2.0 unx      952 b- defN 80-Jan-01 00:00 w7x/lib/utils.py
+-rw-r--r--  2.0 unx     2341 b- defN 80-Jan-01 00:00 w7x/lib/webdav.py
 -rw-r--r--  2.0 unx     6463 b- defN 80-Jan-01 00:00 w7x/merge.py
--rw-r--r--  2.0 unx    40062 b- defN 80-Jan-01 00:00 w7x/model.py
+-rw-r--r--  2.0 unx    41945 b- defN 80-Jan-01 00:00 w7x/model.py
 -rw-r--r--  2.0 unx       42 b- defN 80-Jan-01 00:00 w7x/plotting/__init__.py
 -rw-r--r--  2.0 unx     2402 b- defN 80-Jan-01 00:00 w7x/plotting/extender.py
 -rw-r--r--  2.0 unx     4498 b- defN 80-Jan-01 00:00 w7x/plotting/poincare.py
 -rw-r--r--  2.0 unx     7357 b- defN 80-Jan-01 00:00 w7x/plotting/vmec.py
 -rw-r--r--  2.0 unx      535 b- defN 80-Jan-01 00:00 w7x/setup/presentation.py
--rw-r--r--  2.0 unx     3616 b- defN 80-Jan-01 00:00 w7x/setup/vmec/nn.py
+-rw-r--r--  2.0 unx     1328 b- defN 80-Jan-01 00:00 w7x/setup/vmec/nn.py
 -rw-r--r--  2.0 unx     1170 b- defN 80-Jan-01 00:00 w7x/setup/vmec/stellopt.py
 -rw-r--r--  2.0 unx        0 b- defN 80-Jan-01 00:00 w7x/simulation/__init__.py
 -rw-r--r--  2.0 unx        0 b- defN 80-Jan-01 00:00 w7x/simulation/backends/__init__.py
 -rw-r--r--  2.0 unx        0 b- defN 80-Jan-01 00:00 w7x/simulation/backends/local/__init__.py
 -rw-r--r--  2.0 unx     3451 b- defN 80-Jan-01 00:00 w7x/simulation/backends/local/extender.py
 -rw-r--r--  2.0 unx        0 b- defN 80-Jan-01 00:00 w7x/simulation/backends/mock/__init__.py
 -rw-r--r--  2.0 unx     6951 b- defN 80-Jan-01 00:00 w7x/simulation/backends/mock/flt.py
 -rw-r--r--  2.0 unx     3514 b- defN 80-Jan-01 00:00 w7x/simulation/backends/mock/vmec.py
 -rw-r--r--  2.0 unx     7432 b- defN 80-Jan-01 00:00 w7x/simulation/backends/nn/vmec.py
 -rw-r--r--  2.0 unx       28 b- defN 80-Jan-01 00:00 w7x/simulation/backends/runner/__init__.py
 -rw-r--r--  2.0 unx    13835 b- defN 80-Jan-01 00:00 w7x/simulation/backends/runner/base.py
 -rw-r--r--  2.0 unx     3741 b- defN 80-Jan-01 00:00 w7x/simulation/backends/runner/coils.py
--rw-r--r--  2.0 unx     4604 b- defN 80-Jan-01 00:00 w7x/simulation/backends/runner/vmec.py
+-rw-r--r--  2.0 unx     4914 b- defN 80-Jan-01 00:00 w7x/simulation/backends/runner/vmec.py
 -rw-r--r--  2.0 unx        0 b- defN 80-Jan-01 00:00 w7x/simulation/backends/slurm/__init__.py
 -rw-r--r--  2.0 unx    12845 b- defN 80-Jan-01 00:00 w7x/simulation/backends/slurm/extender.py
 -rw-r--r--  2.0 unx      317 b- defN 80-Jan-01 00:00 w7x/simulation/backends/web_service/__init__.py
 -rw-r--r--  2.0 unx    21784 b- defN 80-Jan-01 00:00 w7x/simulation/backends/web_service/base.py
 -rw-r--r--  2.0 unx     1261 b- defN 80-Jan-01 00:00 w7x/simulation/backends/web_service/coils.py
 -rw-r--r--  2.0 unx    16184 b- defN 80-Jan-01 00:00 w7x/simulation/backends/web_service/components.py
--rw-r--r--  2.0 unx     6792 b- defN 80-Jan-01 00:00 w7x/simulation/backends/web_service/extender.py
+-rw-r--r--  2.0 unx     6976 b- defN 80-Jan-01 00:00 w7x/simulation/backends/web_service/extender.py
 -rw-r--r--  2.0 unx    32170 b- defN 80-Jan-01 00:00 w7x/simulation/backends/web_service/flt.py
 -rw-r--r--  2.0 unx     5528 b- defN 80-Jan-01 00:00 w7x/simulation/backends/web_service/vmec.py
 -rw-r--r--  2.0 unx      737 b- defN 80-Jan-01 00:00 w7x/simulation/coils.py
 -rw-r--r--  2.0 unx     6258 b- defN 80-Jan-01 00:00 w7x/simulation/components.py
 -rw-r--r--  2.0 unx     5191 b- defN 80-Jan-01 00:00 w7x/simulation/extender.py
 -rw-r--r--  2.0 unx     1016 b- defN 80-Jan-01 00:00 w7x/simulation/fieldlines.py
 -rw-r--r--  2.0 unx     1005 b- defN 80-Jan-01 00:00 w7x/simulation/flavors/__init__.py
 -rw-r--r--  2.0 unx      823 b- defN 80-Jan-01 00:00 w7x/simulation/flavors/equilibrium.py
 -rw-r--r--  2.0 unx    12377 b- defN 80-Jan-01 00:00 w7x/simulation/flavors/field_line_tracer.py
 -rw-r--r--  2.0 unx     6496 b- defN 80-Jan-01 00:00 w7x/simulation/flt.py
--rw-r--r--  2.0 unx    39319 b- defN 80-Jan-01 00:00 w7x/simulation/vmec.py
--rw-r--r--  2.0 unx    18890 b- defN 80-Jan-01 00:00 w7x/state.py
+-rw-r--r--  2.0 unx    41406 b- defN 80-Jan-01 00:00 w7x/simulation/vmec.py
+-rw-r--r--  2.0 unx    19137 b- defN 80-Jan-01 00:00 w7x/state.py
 -rw-r--r--  2.0 unx      422 b- defN 80-Jan-01 00:00 w7x/switches.py
--rw-r--r--  2.0 unx     1076 b- defN 80-Jan-01 00:00 w7x-0.5.2.dist-info/LICENSE.rst
--rw-r--r--  2.0 unx     3643 b- defN 80-Jan-01 00:00 w7x-0.5.2.dist-info/METADATA
--rw-r--r--  2.0 unx       88 b- defN 80-Jan-01 00:00 w7x-0.5.2.dist-info/WHEEL
--rw-r--r--  2.0 unx      164 b- defN 80-Jan-01 00:00 w7x-0.5.2.dist-info/entry_points.txt
-?rw-r--r--  2.0 unx     4983 b- defN 16-Jan-01 00:00 w7x-0.5.2.dist-info/RECORD
-59 files, 418934 bytes uncompressed, 117201 bytes compressed:  72.0%
+-rw-r--r--  2.0 unx     1076 b- defN 80-Jan-01 00:00 w7x-0.6.0.dist-info/LICENSE.rst
+-rw-r--r--  2.0 unx     3643 b- defN 80-Jan-01 00:00 w7x-0.6.0.dist-info/METADATA
+-rw-r--r--  2.0 unx       88 b- defN 80-Jan-01 00:00 w7x-0.6.0.dist-info/WHEEL
+-rw-r--r--  2.0 unx      164 b- defN 80-Jan-01 00:00 w7x-0.6.0.dist-info/entry_points.txt
+?rw-r--r--  2.0 unx     5057 b- defN 16-Jan-01 00:00 w7x-0.6.0.dist-info/RECORD
+60 files, 423985 bytes uncompressed, 118586 bytes compressed:  72.0%
```

## zipnote {}

```diff
@@ -33,14 +33,17 @@
 
 Filename: w7x/lib/timeout.py
 Comment: 
 
 Filename: w7x/lib/utils.py
 Comment: 
 
+Filename: w7x/lib/webdav.py
+Comment: 
+
 Filename: w7x/merge.py
 Comment: 
 
 Filename: w7x/model.py
 Comment: 
 
 Filename: w7x/plotting/__init__.py
@@ -156,23 +159,23 @@
 
 Filename: w7x/state.py
 Comment: 
 
 Filename: w7x/switches.py
 Comment: 
 
-Filename: w7x-0.5.2.dist-info/LICENSE.rst
+Filename: w7x-0.6.0.dist-info/LICENSE.rst
 Comment: 
 
-Filename: w7x-0.5.2.dist-info/METADATA
+Filename: w7x-0.6.0.dist-info/METADATA
 Comment: 
 
-Filename: w7x-0.5.2.dist-info/WHEEL
+Filename: w7x-0.6.0.dist-info/WHEEL
 Comment: 
 
-Filename: w7x-0.5.2.dist-info/entry_points.txt
+Filename: w7x-0.6.0.dist-info/entry_points.txt
 Comment: 
 
-Filename: w7x-0.5.2.dist-info/RECORD
+Filename: w7x-0.6.0.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## w7x/__init__.py

```diff
@@ -1,12 +1,12 @@
 """Top-level module"""
 
 __author__ = """Daniel Böckenhoff"""
 __email__ = "dboe@ipp.mpg.de"
-__version__ = "0.5.2"
+__version__ = "0.6.0"
 import pathlib
 
 __built__ = not pathlib.Path(__file__, "..", "..", "setup.py").resolve().exists()
 
 # from . import simulation
 # from . import diagnostic
 from .switches import distribute, stateful, exposed
```

## w7x/conf/config.yaml

```diff
@@ -1,12 +1,11 @@
 package:
     resources: ${path:${package.path}/../tests/resources}
 
 general:
-    runner: local
     backend: web_service
     tmp_dir : ${os.home}/tmp
     data: ${os.home}/data
     cache: ${os.home}/.w7x/w7x_cache
     stellopt_dir: ${general.cache}/STELLOPT
 
     user:
@@ -40,27 +39,29 @@
         min: -1.35
         max: 1.35
         num: 181
 
 vmec:
     backend: ${general.backend}
     folder: ${general.tmp_dir}/vmec
-    runner: ${general.runner}
-    mgrid: ${general.data}/vmec/MAKEGRID/mgrid_w7x_nv36_hires.nc
+
+    runner:
+        cache: ${general.cache}/vmec_runner
+        mgrid_url: https://datashare.mpcdf.mpg.de/s/Ba9ZhuZTOZ3cASf
+        mgrid_dir: ${vmec.runner.cache}/mgrid
 
     slurm:
         exe: /bin/xvmec2000
 
     local:
         exe: ${general.stellopt_dir}/VMEC2000/Release/xvmec2000
 
     web_service:
         server: http://esb.ipp-hgw.mpg.de:8280/services/vmec_v8?wsdl
         database: http://svvmec1.ipp-hgw.mpg.de:8080/vmecrest/v1/run/
-        mgrid: mgrid_w7x_nv36_hires.nc
 
     nn:
         cache: ${general.cache}/vmecnn
         model_url: https://datashare.mpcdf.mpg.de/s/HsvafUNo7LggcUv
         model_relative_path: 2022-07-31/14-29-30
         # relative path to model_path and model_url
         checkpoint_relative_path: ${vmec.nn.model_relative_path}/lightning_logs/0_1/checkpoints/epoch=55-step=14000.ckpt
```

## w7x/config.py

```diff
@@ -22,15 +22,14 @@
 from w7x.model import (
     Assembly,
     Component,
     CoilSet,
     Coil,
     Equilibrium,
     PlasmaParameters,
-    MGrid,
 )
 import w7x.merge
 
 
 __config = rna.config.api(
     "w7x",  # in case you move it to __init__.py change to __file__
     rna.path.resolve("~", ".w7x", "config.yaml"),
@@ -485,36 +484,27 @@
         current_profile: Profile = PowerSeries(coefficients=[0.0, 0.0], domain=[0, 1])
         iota_profile: Profile = None
 
         pressure_scale: float = 0.0
         total_toroidal_current: float = 0.0
 
 
-def _get_mgrid_path():
-    """Get mgrid path from config.cfg"""
-    backend = __config.vmec.backend
-    return rna.config.fallback(__config, "vmec", backend, "mgrid")
-
-
 class Equilibria:
     """
     Default equilibrium states.
     """
 
     @dataclasses.dataclass
     class InitialGuess(Equilibrium):
         """
         Good candidate as initial equilibrium.
         """
 
         field_period: int = 5
-        vacuum_field: tfields.TensorGrid = rna.pattern.link.Link(
-            ref=MGrid(path=_get_mgrid_path()),
-            fget=MGrid.to_numpy,
-        )
+        vacuum_field: tfields.TensorGrid = None
         phi: Profile = PowerSeries(coefficients=[0, -2.0])
         flux_surfaces: TensorSeries = TensorSeries(
             Fourier.from_coefficients(
                 cos=[0.0, 0.0, 0.0, 0.0, 5.5496e00, 4.3857e-1, 0.0, 0.0, 0.0]
                 + [0.0] * 36
                 + [
                     1.8275e-03,
```

## w7x/core.py

```diff
@@ -233,14 +233,16 @@
     call_time: datetime = dataclasses.field(default_factory=datetime.now)
     #: module name, auto computed from function on first instantiation (no copies)
     module: typing.Optional[str] = None
     #: version of the module, auto computed from function on first instantiation (no copies)
     version: typing.Optional[str] = None
     #: git hash of the module, auto computed from function on first instantiation (no copies)
     git_hash: typing.Optional[str] = None
+    #: backend, in case the function delegates to a backend
+    backend: typing.Optional[typing.Union[typing.Type, str]] = None
 
     def __post_init__(self):
         if isinstance(self.function, str):
             # nothin to do
             return
         if isinstance(self.function, functools.partial):
             function = self.function.func
@@ -250,14 +252,16 @@
         # first instantiation only a function
         module = inspect.getmodule(function)
         module_name = module.__name__.split(".")[0]
         self.module = module_name
         module = importlib.import_module(module_name)
         self.git_hash = self.get_git_hash(module)
         self.version = self.get_version(module_name)
+        if self.backend is not None:
+            self.backend = self.backend.__module__ + "." + type(self.backend).__name__
         # this will lock everything in place
         self.function = _func_key(function)
 
     @staticmethod
     def get_git_hash(module) -> typing.Optional[str]:
         """
         Returns:
@@ -489,17 +493,22 @@
 
         res = func(state, **parameter_kwargs)
         assert res is not None
 
         if not self._stateless and stateful.enabled():
             if not isinstance(res, Delayed):
                 assert issubclass(type(res), StateComponent), f"Invalid attr {res}"
+            backend = (
+                this.backend if this is not None and isinstance(this, Code) else None
+            )
+            # TODO-2(@dboe): Think about how to handle the user configs.
             call_history = CallHistory(
                 parameters=parameter_kwargs,
                 function=func,
+                backend=backend,
             )
             history = History()
             history.add(call_history)
 
             state = State.merged(state, res, history)
             return state
         return res
```

## w7x/model.py

```diff
@@ -91,14 +91,15 @@
         History --|> StateLeaf
         History <-- State : histor
 
 """
 
 import typing
 import numpy as np
+import logging
 
 import tfields
 import rna.pattern.link
 
 from w7x.compatibility import sqlalchemy, declared_attr
 from w7x.lib import dataclasses
 from w7x.lib.equilibrium import (
@@ -108,14 +109,17 @@
     TensorSeries,
 )
 from w7x.lib.profiles import Profile
 from w7x.state import Entry, StateComposite, StateLeaf, State
 import w7x.merge
 
 
+LOGGER = logging.getLogger(__name__)
+
+
 # TODO-2(@dboe): resolve conflict between dask and sqlalchemy,
 #                pk field with init=False is primary_key
 # from sqlalchemy.orm import registry
 # mapper_registry = registry()
 
 
 @dataclasses.dataclass
@@ -226,15 +230,15 @@
         """
         Recursively run through coils and coil_sets and join them recursively
 
         Args:
             *args and **kwargs forwarded to ::meth::`rna.pattern.composite.Composite.get_leaves`
             supply_groups: If supply_groups is True, do not flatten the
 
-        TODO-1(@dboe): is groups == independent?
+        TODO-1(@dboe): is groups == independent? Is this flag used at all?
 
         Examples:
             >>> import w7x
             >>> cs = w7x.model.CoilSet(coils=[w7x.model.Coil(id=42), w7x.model.Coil(id=84)])
             >>> [c.id for c in cs.get_coils()]
             [42, 84]
 
@@ -275,14 +279,25 @@
                 if collect_coil_set.children:
                     composites.append(collect_coil_set)
                 return composites
 
             return self.get_leaves(*args, apply_composite=apply_composite, **kwargs)
         return self.get_leaves(*args, **kwargs)
 
+    def equals(self, other, compare_current=True):
+        # TODO-2: this implementation, does not check coil_set properties
+        leaves = self.get_coils(flat=True)
+        other_leaves = other.get_coils(flat=True)
+        if len(leaves) != len(other_leaves):
+            return False
+        for leaf1, leaf2 in zip(leaves, other_leaves):
+            if not leaf1.equals(leaf2, compare_current=compare_current):
+                return False
+        return True
+
     def get_currents(
         self, independent: bool = False, flat: bool = False, **kwargs
     ) -> typing.Union[typing.List[float], typing.List[typing.List[float]]]:
         """
         Corrisponing counterpart to :meth:`set_currents`.
 
         Args:
@@ -563,14 +578,23 @@
         current (float): coil current [A]
     """
 
     PARENT_TYPE = CoilSet  # pylint:disable=invalid-name
     n_windings: int = 1
     current: float = 0.0  # [A] always!
 
+    def equals(self, other, compare_current=True):
+        # TODO-2(@dboe): Is there a better way via dataclass properties?
+        for field in ["id", "n_windings", "current"]:
+            if not compare_current and field == "current":
+                continue
+            if getattr(self, field) != getattr(other, field):
+                return False
+        return True
+
     def set_current(
         self,
         current: float,
         unit: str = "A",
         reference_coil: typing.Optional["Coil"] = None,
     ):
         """
@@ -647,15 +671,15 @@
     """
 
     items: typing.List[typing.Union["Resources", "File"]] = dataclasses.children_alias(
         default_factory=lambda: [],
     )
 
 
-@dataclasses.dataclass
+@dataclasses.dataclass(repr=False)
 class File(StateLeaf, rna.pattern.link.Reference):
     """
     Base class of a file (local, url or other). Objects of this type can be referenced
     with the Reference pattern as links.
     """
 
     PARENT_TYPE = Resources  # pylint:disable=invalid-name
@@ -679,14 +703,21 @@
     def __getstate__(self):
         """
         Required for pickling
         """
         res = {k: v for k, v in self.__dict__.items() if k != "data"}
         return res
 
+    def __repr__(self):
+        ref_repr = [f"({object.__repr__(ref[0])},{ref[1]})" for ref in self._references]
+        return (
+            f"{self.__class__.__name__}(file_id: {self.file_id!r}, path: {self.path!r}"
+            f", data: {self.data!r}, references (types): {ref_repr})"
+        )
+
 
 def _fget_alias(alias):
     """
     Trigger self.load() which will have to set the attribute of the alias.
     """
 
     def fget(self):
@@ -695,15 +726,15 @@
             self.load()
             val = getattr(self, alias)
         return val
 
     return fget
 
 
-@dataclasses.dataclass
+@dataclasses.dataclass(repr=False)
 class MGrid(File):
     """
     Magnetic grid files which are output of e.g., Makegrid (input to VMEC) and EXTENDER.
     """
 
     #: base vectors. Required, if MGrid is only partial (not e.g. TensorGrid)
     base_vectors: typing.Optional[typing.Tuple[tuple]] = dataclasses.alias_field(
@@ -714,43 +745,58 @@
     #: iter_order. Required, if MGrid is only partial (not e.g. TensorGrid)
     iter_order: typing.Optional[typing.List[int]] = dataclasses.alias_field(
         "_iter_order",
         fget=_fget_alias("_iter_order"),
         default=None,
     )
 
+    def __repr__(self):
+        super_repr = super().__repr__()
+        return f"{super_repr}, base_vectors: {self._base_vectors}, iter_order: {self._iter_order}"
+
     def to_numpy(self) -> tfields.TensorFields:
         """
         Return the TensorFields representation of the mgrid.
         """
         data = self.load()
         if isinstance(data, (tfields.TensorFields, tfields.TensorGrid)):
             return data
         if isinstance(data, (tfields.Tensors, np.ndarray)):
-            # TODO(@dboe): default base_vectors and iter order if not given
+            # Note(@dboe): add default base_vectors and iter order if not given?
             return tfields.TensorGrid.empty(
                 *self.base_vectors,
                 fields=[data],
                 iter_order=self.iter_order,
                 coord_sys=tfields.bases.CYLINDER,
             )
         raise NotImplementedError(f"Conversion of {type(data)} to tfields.TensorFields")
 
     def load(self):
         """
         Load and cache data on request
         """
+        if self.path is None:
+            raise ValueError("Path is required but is not set")
         if self.data is None:
             extension = rna.path.extension(self.path)
             if extension in ("npz", "datc"):
                 self.data = tfields.TensorGrid.load(self.path)
-            if extension == "dat":
+            elif extension == "dat":
                 self.data = tfields.Tensors.load(
                     self.path, coord_sys=tfields.bases.PHYSICAL_CYLINDER
                 )
+            elif extension == "nc":
+                # TODO-1(@all): implement loading nc file
+                LOGGER.info(
+                    "Loading Mgrid from extension '%s' not implemented", extension
+                )
+            else:
+                LOGGER.warning(
+                    "Loading Mgrid from extension '%s' not implemented", extension
+                )
         if isinstance(self.data, tfields.TensorGrid):
             self.base_vectors = self.data.base_num_tuples()
             self.iter_order = self.data.iter_order
         return self.data
 
     def to_state(self, field_name="field") -> "State":
         """
```

## w7x/setup/vmec/nn.py

```diff
@@ -1,65 +1,11 @@
 import subprocess
-import requests
 import os
 import w7x
-
-
-def download_webdav(
-    url: str, relative_path: str, output: str, password: str = "", is_dir=False
-):
-    """
-    Download a file (folder not possible) via webdav protocol given a public share url
-
-    Args:
-        url (str): Url to public data share repo
-        relative_path (str): Relative path to file within repo
-        output (str): Path to the output. If output.endswith("/") or is_dir relative_path is joined
-        password (str, optional): Password of the share if set. Defaults to ''.
-        is_dir (bool, optional): Flag to mark if output is a directory or file. Defaults to False.
-    """
-    # Assuming url is a public webdav link (e.g. nextCloud)
-    domain, token = url.split("/s/")
-    webdav_url = os.path.join(domain, "public.php/webdav/" + relative_path)
-    if output.endswith("/") or is_dir:
-        # this is understood to be the base path. Prepend the relative_path then.
-        # Otherwise take it as full path
-        output = os.path.join(output, relative_path)
-    username = token
-
-    # TODO-2: In case you have to add the certificate... Dont think it is a problem though
-    # good read: openssl x509 -in server.cer -inform DER -outform PEM  >> consolidate.pem
-    # host = webdav_url.lstrip('https://')
-    # port = 443
-    # cert_path = os.path.join("/tmp", host + ".pem")
-    # # Create a socket and connect to the server
-    # sock = socket.create_connection((host, port))
-    # # Wrap the socket with an SSL context
-    # context = ssl.create_default_context()
-    # with context.wrap_socket(sock, server_hostname=host) as ssock:
-    #     # Get the server's SSL certificate
-    #     cert_bytes = ssock.getpeercert(binary_form=True)
-
-    # pem_cert = ssl.DER_cert_to_PEM_cert(cert_bytes)
-    # # Save the certificate to a file
-    # with open(cert_path, 'w') as f:
-    #     f.write(pem_cert)
-    # verify = cert_path
-    verify = False
-
-    # Perform the HTTPS request and provide the certificate
-    response = requests.get(webdav_url, auth=(username, password), verify=verify)
-
-    if response.status_code == 200:
-        os.makedirs(os.path.dirname(output), exist_ok=True)
-        with open(output, "wb") as f:
-            f.write(response.content)
-            print(f"Downloaded file {output}")
-    else:
-        print(f"Request failed with response {response}")
+from w7x.lib.webdav import download_webdav
 
 
 def install():
     # import w7x just here because it is not working until libs are installed
 
     # Assuming vmecnn installed via pip extras (vmec_nn)
     # We could install vmecnn via poetry with the following in pyproject (and add vmecnn to extra)
```

## w7x/simulation/backends/runner/vmec.py

```diff
@@ -69,14 +69,22 @@
         """
         Compute an equilibrium with VMEC on the HPC.
         """
 
         dry_run = kwargs.pop("dry_run")
 
         vmec_input = VmecInput.from_state(state, **kwargs)
+        vmec_input.provide_mgrid_locally(
+            w7x.config.vmec.runner.mgrid_url, w7x.config.vmec.runner.mgrid_dir
+        )
+        if vmec_input.free_boundary:
+            assert os.path.exists(
+                vmec_input.mgrid_path
+            ), f"mgrid_path {vmec_input.mgrid_path} does not exist"
+
         vmec_id = vmec_input.vmec_id
 
         LOGGER.info(f"Executing {vmec_id} run on the {self.runner} runner.")
         job = Job(
             name=vmec_id,
             cwd=self.folder,
             files=[(vmec_input.to_string(), get_indata_file_name(vmec_id))],
```

## w7x/simulation/backends/web_service/extender.py

```diff
@@ -4,14 +4,15 @@
 TODO-2(@dboe): check that magnetic config is indeed the same as the field used for VMEC!!!
 """
 import os
 import logging
 import requests
 import posixpath
 
+import rna.pattern.link
 import tfields
 import w7x
 import w7x.simulation.flt
 from w7x.simulation.backends.web_service import (
     get_server,
     run_service,
     to_osa_type,
@@ -23,15 +24,22 @@
 WS_SERVER = w7x.config.extender.web_service.server
 
 
 def wout_from_state(state):
     """
     Retrieve the Wout reference from the state
     """
-    wout = state.equilibrium.get_ref("flux_surfaces", "phi")
+    for field_name in ["flux_surfaces", "phi"]:
+        try:
+            wout = state.equilibrium.get_ref(field_name)
+        except rna.pattern.link.LinkNotFoundError:
+            continue
+    else:
+        wout = None
+
     if isinstance(wout, w7x.simulation.vmec.Wout):
         return wout
     LOGGER.warning(
         "No explicit reference to wout file found in equilibrium. "
         "Will take the last Wout file from resources."
     )
```

## w7x/simulation/vmec.py

```diff
@@ -14,17 +14,18 @@
 import logging
 import os
 import typing
 
 from netCDF4 import Dataset
 import numpy as np
 
-from rna.pattern.link import Link
+from rna.pattern.link import Link, LinkNotFoundError
 import w7x
 from w7x.core import Code, Backend, State, StateComponent
+from w7x.lib.webdav import download_webdav
 from w7x.simulation.flavors.equilibrium import EquilibriumMixin
 from w7x.lib.equilibrium import TensorSeries, Cos, Sin, Fourier, FourierTerm
 from w7x.lib.profiles import Profile, PowerSeries
 from w7x.lib.utils import gen_run_id
 
 
 class Status(Enum):
@@ -705,35 +706,26 @@
     def _validate_kwargs(cls, kwargs: dict) -> dict:
         """
         Validate kwargs to subset of cls attributes.
         """
         return {k: v for k, v in kwargs.items() if k in cls.__dataclass_fields__}
 
     @classmethod
-    def default(cls):
-        """
-        Method for fast creation of a VMEC input with a proper default.
-        """
-        return cls.from_state(
-            w7x.config.CoilSets.Ideal(),
-            w7x.config.Plasma.Vacuum(),
-            w7x.config.Equilibria.InitialGuess(),
-        )
-
-    @classmethod
     def from_state(cls, *args: typing.Union[State, StateComponent], **kwargs):
         """
         Factory method for building a VMEC input from state.
 
         Examples:
             >>> import w7x
             >>> vmec_input = w7x.simulation.vmec.VmecInput.from_state(
             ...     w7x.config.CoilSets.Ideal(), w7x.config.Plasma.Vacuum(),
             ...     w7x.config.Equilibria.InitialGuess(),
-            ...     force_tolerance_levels=[1e-3, 1e-5, 1e-9, 1e-12])
+            ...     force_tolerance_levels=[1e-3, 1e-5, 1e-9, 1e-12],
+            ...     free_boundary=True
+            ... )
             >>> vmec_input.gamma
             0
 
             >>> vmec_input.coil_currents[:5]
             [13200.0, 13200.0, 13200.0, 13200.0, 13200.0]
             >>> vmec_input.coil_currents[5:]
             [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0]
@@ -744,20 +736,55 @@
             >>> vmec_input.force_tolerance_levels
             [0.001, 1e-05, 1e-09, 1e-12]
         """
 
         vmec_input = cls(**cls._validate_kwargs(kwargs))
         state = w7x.State.merged(*args)
 
+        assert state.has(
+            w7x.model.CoilSet
+        ), "Building a vmec input requires knowledge about the coil set"
         vmec_input.coil_currents = state.coil_set.coil_currents(unit="A")
 
+        assert (
+            "free_boundary" in kwargs
+        ), "Building a vmec input requires knowledge about the mode"
+        free_boundary = kwargs.get("free_boundary")
         if state.has(w7x.model.Equilibrium):
-            vacuum_field_link = state.equilibrium.get_ref("vacuum_field")
-            if vacuum_field_link is not None:
-                vmec_input.mgrid_path = vacuum_field_link.path
+            if free_boundary:
+                # construct mgrid.
+                # Priorities:
+                #   - equilibrium.vacuum_field
+                #   - coil_set
+                try:
+                    vacuum_field_link = state.equilibrium.get_ref("vacuum_field")
+                except LinkNotFoundError:
+                    if state.equilibrium.vacuum_field is None:
+                        # TODO-1(@dboe): Once this the config is refactored, you dont need to cast
+                        if state.coil_set.equals(
+                            w7x.config.CoilSets.Ideal(), compare_current=False
+                        ):
+                            mgrid = w7x.model.MGrid(path="mgrid_w7x_nv36_hires.nc")
+                        else:
+                            raise NotImplementedError()
+                    else:
+                        raise NotImplementedError()
+                else:
+                    assert isinstance(vacuum_field_link, w7x.model.MGrid)
+                    mgrid = vacuum_field_link
+                    if mgrid.path == "mgrid_w7x_nv36_hires.nc":
+                        assert state.coil_set.equals(
+                            w7x.config.CoilSets.Ideal(), compare_current=False
+                        ), "Inconsistent coil set and mgrid"
+                    else:
+                        raise NotImplementedError()
+
+                assert mgrid.path is not None, "free_boundary mode requires mgrid_path"
+
+                vmec_input.mgrid_path = mgrid.path
 
             if state.equilibrium.field_period is not None:
                 vmec_input.num_field_periods = state.equilibrium.field_period
 
             if state.equilibrium.phi is not None:
                 vmec_input.phi_edge = state.equilibrium.phi_edge
 
@@ -782,21 +809,36 @@
             if state.plasma_parameters.total_toroidal_current is not None:
                 vmec_input.total_toroidal_current = (
                     state.plasma_parameters.total_toroidal_current
                 )
 
         return vmec_input
 
+    def provide_mgrid_locally(self, mgrid_url: str, mgrid_dir: str) -> None:
+        mgrid_relative_path = self.mgrid_path
+        assert mgrid_relative_path is not None
+
+        mgrid_path = os.path.join(mgrid_dir, mgrid_relative_path)
+        self.mgrid_path: str = mgrid_path
+        if os.path.exists(mgrid_path):
+            return
+
+        download_webdav(
+            mgrid_url,
+            mgrid_relative_path,
+            mgrid_dir,
+            is_dir=True,
+        )
+
     def to_string(self):
         """
         Returns vmec input as string.
 
         Note: possibly transcoding could be used here, too
         """
-
         indata = "&INDATA\n"
         indata += get_indata_line("LFREEB", self.free_boundary)
         indata += get_indata_line(
             "MGRID_FILE",
             self.mgrid_path if self.mgrid_path else None,
         )
         indata += get_indata_line("EXTCUR", self.coil_currents)
@@ -1207,14 +1249,19 @@
             ):
                 LOGGER.info(
                     f"Found beta={wout.get_betatotal():5.4f}, "
                     f"b_axis={wout.b_axis(0.0):3.2f}, "
                     f"vol={wout.get_volume_p():.2f}."
                 )
                 break
+        else:
+            try:
+                raise RuntimeError("Could not find the target.")
+            except RuntimeError as err:
+                LOGGER.exception(err)
 
         return wout.to_state()
 
     ###################
     # PRIVATE METHODS #
     ###################
```

## w7x/state.py

```diff
@@ -231,25 +231,33 @@
 
     def __setstate__(self, d):
         """
         Required for pickling
         """
         self.__dict__.update(d)
 
+    # TODO-1: (@dboe): Is this to be done? -> see io tests
+    # def save(self, *args, **kwargs):
+    #     with exposed(True):
+    #         return super().save(*args, **kwargs)
+
 
 # pylint:disable=inherit-non-class
 @dataclasses.dataclass
 class StateComposite(StateComponent.Composite):
     """
     _children can be made an alias for a field with the DataclassPropertyAliaser
     """
 
     @StateComponent.parent.setter  # pylint:disable=no-member
     def parent(self, parent):
-        if (
+        if parent is None:
+            # remove
+            pass
+        elif (
             not parent.origin() is self.PARENT_TYPE
             and not self.origin() is parent.origin()
         ):  # also allow composite pattern
             raise ValueError(
                 f"Incorrect parent type. {self} is child of {self.PARENT_TYPE}"
                 f" but was added to {type(parent)}"
             )
```

## Comparing `w7x-0.5.2.dist-info/LICENSE.rst` & `w7x-0.6.0.dist-info/LICENSE.rst`

 * *Files identical despite different names*

## Comparing `w7x-0.5.2.dist-info/METADATA` & `w7x-0.6.0.dist-info/METADATA`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: w7x
-Version: 0.5.2
+Version: 0.6.0
 Summary: The w7x package is a simulation framework that defines interfaces for simulation codes with interchangeable backends, computation pipelines in a directed acyclic graph that communicate via a central state.
 Home-page: https://gitlab.mpcdf.mpg.de/dboe/w7x
 License: MIT
 Keywords: Wendelstein 7-X,simulation,state,field line tracer,vmec,extender,numerical modeling,distributed computing
 Author: Daniel Böckenhoff
 Author-email: dboe@ipp.mpg.de
 Requires-Python: >=3.8,<4.0
@@ -25,15 +25,15 @@
 Requires-Dist: hydra_core
 Requires-Dist: hyperopt ; extra == "hyperopt"
 Requires-Dist: netCDF4
 Requires-Dist: numpy (>=1.20.0)
 Requires-Dist: osa
 Requires-Dist: pathlib ; python_version < "3.10"
 Requires-Dist: requests
-Requires-Dist: rna[pyqtgraph] (>=0.10.0)
+Requires-Dist: rna[pyqtgraph] (>=0.11.0)
 Requires-Dist: scikit-learn (>0.0)
 Requires-Dist: scipy (>=1.9.2)
 Requires-Dist: tfields[io] (>=0.5.0)
 Project-URL: Documentation, https://dboe.pages.mpcdf.de/w7x
 Project-URL: Repository, https://gitlab.mpcdf.mpg.de/dboe/w7x
 Description-Content-Type: text/x-rst
```

## Comparing `w7x-0.5.2.dist-info/RECORD` & `w7x-0.6.0.dist-info/RECORD`

 * *Files 7% similar despite different names*

```diff
@@ -1,59 +1,60 @@
-w7x/__init__.py,sha256=k2rAOTh5ZGi3jew_0mWBcp0YQs7F5GsjpgDHoFJySu0,571
+w7x/__init__.py,sha256=ah57JI2wNEvsjkQ7gMh0IABwoIxKh2dqDDS22XneQXA,571
 w7x/__main__.py,sha256=LeXgNekQwix4K3x1iR8wVKUqcu6LPakessFaOsn36QE,8105
 w7x/compatibility.py,sha256=seIuE1-Vk3dL4xLSaPQIyaDm6kRZnK8ccMYP8NGkUE0,3008
-w7x/conf/config.yaml,sha256=lpQjlQmi2bAIVXz6DMg4NS8blYOwWWZqBaIPRo4XNes,4839
-w7x/config.py,sha256=X2gfUipk4_aIFX22nDGHa_Pd1Aecjj3vHugz-sUk-cY,24031
-w7x/core.py,sha256=76UqTFzow41VWjP8QSjyE3hO4Xg0WOhxdj-o_zoeBDQ,19830
+w7x/conf/config.yaml,sha256=cxS8Zk-skAqURF69lGCH6TQZZhGwIPti1IS25MXFjNY,4858
+w7x/config.py,sha256=Zm-EfTZUEkxKbFbyDVr4r9f0tf67jTHoWMtGhRbGk9w,23743
+w7x/core.py,sha256=nlFpzhaGZcs_62BGFLMYReogzlcIvfDCnzRgv9GME9o,20312
 w7x/lib/__init__.py,sha256=1uDbAyv2keU_WSu0B2-AN5_E1O6_8nY6nxmwsKIZBcQ,89
 w7x/lib/dataclasses.py,sha256=UoqXyYYEPvUIim6Bue3TQwUwtZfJztGaxbYlF2RnfzE,3866
 w7x/lib/equilibrium.py,sha256=RFoWTQN8jnuDevn4B5GN59E_w_em_Q81relkEBr9C1I,17525
 w7x/lib/profiles.py,sha256=p2ilqT6EcOIY_S0c2LOcZtHcyOCC0oK7dwZcvh9DdzU,15963
 w7x/lib/tfields.py,sha256=v5VImJEiWaDPMlNCGbWQIzHnQqLIn155DMBDu0_aIzk,7864
 w7x/lib/timeout.py,sha256=I_8u2YUTQNfQdv86OiiQg94b6yKdU8VAsWZBP68tT7U,3221
 w7x/lib/utils.py,sha256=cRRvX47AC4YgDN7DzcJ85VxdkebLnqNFkXH4wFwEbKs,952
+w7x/lib/webdav.py,sha256=dBpLdgAotwXZtBBNLrjW_NCbMRHW2cCQq78cT01s_SU,2341
 w7x/merge.py,sha256=QUVjYor-fHrvpgbWxYf9LMLgi9nvmgehnjYP65H29ug,6463
-w7x/model.py,sha256=pR9bFsA7ddQauIK7SZE6xefUHmXs_TphQQbfYBuaLTA,40062
+w7x/model.py,sha256=wkj-9_wmbks42kMY269ugqeE6I-vdZI7cAbW1HIBc1Y,41945
 w7x/plotting/__init__.py,sha256=iQ3wMCVMUf21ew-4S1NXJDn95-w0FCTN5Ln_WmlBep4,42
 w7x/plotting/extender.py,sha256=CyYUVsHu0jj-gqMNRLEAp2flbOp202l-mgqfsJWam6U,2402
 w7x/plotting/poincare.py,sha256=WfMcDtQWrBRtNx0A-glFhVLKAtTZjHa8TFqw1PqKSC4,4498
 w7x/plotting/vmec.py,sha256=u8EQObfiFKlB3qPV_2dUh6byDeNiiKcHZUeAJKjG9uk,7357
 w7x/setup/presentation.py,sha256=PLe8flczwchhKTvPqV7-yQr6mj9aKmMD5OB88qPFlBE,535
-w7x/setup/vmec/nn.py,sha256=KhYk9jw-DfDkGqdaH68OrUavu0OlXt07s7lfV9zcaeI,3616
+w7x/setup/vmec/nn.py,sha256=QKvTzOum0frK9c9HEMYJlG19W7zdRzlw123huuUTPtg,1328
 w7x/setup/vmec/stellopt.py,sha256=DUTRlLQJQu5m9-DEeU3c0e2YM1ibN2KLvjiShG-L6ko,1170
 w7x/simulation/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 w7x/simulation/backends/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 w7x/simulation/backends/local/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 w7x/simulation/backends/local/extender.py,sha256=m631tg_dFm829OA-2S43C30OfSqlM5pbyDElz-9WLA8,3451
 w7x/simulation/backends/mock/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 w7x/simulation/backends/mock/flt.py,sha256=Ose3Mp2Zl9uN_jIPlNRHlbzKKuittIi-8XtPneJas6E,6951
 w7x/simulation/backends/mock/vmec.py,sha256=fVbkLfDK3fXNpdu85M_iwLpaiNCasJ3fEMBUxJs4kBU,3514
 w7x/simulation/backends/nn/vmec.py,sha256=TlIMnPzX7vyPlWhsgFXAsNUgA9l7NlqipSCNQ7VeD-M,7432
 w7x/simulation/backends/runner/__init__.py,sha256=rpH-hhhlCo6H_XfMry1gImGBJvn5PADFy4Iy83Ehufc,28
 w7x/simulation/backends/runner/base.py,sha256=u63xGIA-RjbCPpKJG0cKun0-XZ27sdGM_Oj3zXCr7LM,13835
 w7x/simulation/backends/runner/coils.py,sha256=ukQNeSg6n-aO3Xwgd0mXsjdb-Ifk6xZH9K26FZyyKdM,3741
-w7x/simulation/backends/runner/vmec.py,sha256=JKHL4taWhjDV5QALIuHErOqtP954H562uhyNkTJh5NE,4604
+w7x/simulation/backends/runner/vmec.py,sha256=wTAsU89WO997YQjNv5SeZfBboPS0D3X5eM9PgHVpCXM,4914
 w7x/simulation/backends/slurm/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 w7x/simulation/backends/slurm/extender.py,sha256=BwphwIPf14T_2QC3SGPtFPE6I6lFfh85vSlLJiAt5Ds,12845
 w7x/simulation/backends/web_service/__init__.py,sha256=Pn9g0hBLaR6Fq-QjlBZtESicMr6Xsbt29xDVmQeDAEY,317
 w7x/simulation/backends/web_service/base.py,sha256=vV1hDzPAu0hjLnpjAT8-Xil8DlElm15z6jnTgoqUv00,21784
 w7x/simulation/backends/web_service/coils.py,sha256=G4TMPYxnJUvzM9CEe_XVLwWzSbMhpYrojaFc2CBujQ4,1261
 w7x/simulation/backends/web_service/components.py,sha256=ZpPW8eGiw9ld6jQ9UQFHJnXCzMAbx1uCj8pknOhUXzQ,16184
-w7x/simulation/backends/web_service/extender.py,sha256=ZCEmgJL6DhPpYkeSB6kPnREIvY0Cs0aOKHQ2WbHaqF8,6792
+w7x/simulation/backends/web_service/extender.py,sha256=12tjz53zoidmLSrYENBLlfmZPb8K5ljorhU_1cQSAtQ,6976
 w7x/simulation/backends/web_service/flt.py,sha256=Q10xilPV9VmMgGRog0og0MZiqsQTjx32r3-iIKdv0qg,32170
 w7x/simulation/backends/web_service/vmec.py,sha256=dcACknFsy6NhQkKXrwetdzWE8-7KwOuYfiUqcb2zkwM,5528
 w7x/simulation/coils.py,sha256=eNxkmpSDl-5RJe3EJNiyDD65m6zwgLFSlTsPUX1lqWE,737
 w7x/simulation/components.py,sha256=TecRmP7mnLp6xzKcYY10SdS6tBHLvwktY_BwD-9VbFI,6258
 w7x/simulation/extender.py,sha256=_YSsPElSDu3ulvvg-Jew9ZpZma0BfYZLnhGOSuvn9pg,5191
 w7x/simulation/fieldlines.py,sha256=JVre6niSEEXDSF0rh3juBr4WtIXLmc8dSA6xoGugBo8,1016
 w7x/simulation/flavors/__init__.py,sha256=8pqr0kPHIyAy01757ZOLSiv7K2qysR1dNlJkHlpDhXc,1005
 w7x/simulation/flavors/equilibrium.py,sha256=F4Y-LU4tjamSygBZIgR-oMCZ-nLfdYbI1dttcF1KFZc,823
 w7x/simulation/flavors/field_line_tracer.py,sha256=7OXfTbwAevEC1jdY6ZJZzp4EcGddVBrbd_zyKLASVak,12377
 w7x/simulation/flt.py,sha256=0fsI3Uey0okO6Pgs2gxHCu_aLggp4jqwpjQ_LyiMKdM,6496
-w7x/simulation/vmec.py,sha256=k8414loCg-rfHwh3r-B4oM-RmIXryfXRxwUoqQp-ork,39319
-w7x/state.py,sha256=U4O0asB1M3Shwwu0S5WIykrnm07bIpz9lTcVZ-MampU,18890
+w7x/simulation/vmec.py,sha256=nCpD1PFCkSFnX2oznZ_a_Qeww0o72HAEnXAsnK_j_nM,41406
+w7x/state.py,sha256=KddDWEELmaCaFa6d3f_lIULcPUuztVs07VZ_NDO7Xeo,19137
 w7x/switches.py,sha256=WUn7-B3XCD0lHqemPi5VcVWNBAALKs9fgUlReGBoGlM,422
-w7x-0.5.2.dist-info/LICENSE.rst,sha256=dHQrFF0bnLAGSkUSft19a0uglZwuUv5dryNMHAk893o,1076
-w7x-0.5.2.dist-info/METADATA,sha256=pVVap2ZQJYLk1_XIJ2j2qQiMJqVXl_yTJpwLmIuVFGs,3643
-w7x-0.5.2.dist-info/WHEEL,sha256=Zb28QaM1gQi8f4VCBhsUklF61CTlNYfs9YAZn-TOGFk,88
-w7x-0.5.2.dist-info/entry_points.txt,sha256=WpUPZZyA5rcYcLBMS5VVdWAejr4LrRvH9Ef7v-1c0Co,164
-w7x-0.5.2.dist-info/RECORD,,
+w7x-0.6.0.dist-info/LICENSE.rst,sha256=dHQrFF0bnLAGSkUSft19a0uglZwuUv5dryNMHAk893o,1076
+w7x-0.6.0.dist-info/METADATA,sha256=ByeUerJc_yeMfcMJ7dzgrnWfokkPHAxWwjRKxgRcAIc,3643
+w7x-0.6.0.dist-info/WHEEL,sha256=Zb28QaM1gQi8f4VCBhsUklF61CTlNYfs9YAZn-TOGFk,88
+w7x-0.6.0.dist-info/entry_points.txt,sha256=WpUPZZyA5rcYcLBMS5VVdWAejr4LrRvH9Ef7v-1c0Co,164
+w7x-0.6.0.dist-info/RECORD,,
```

