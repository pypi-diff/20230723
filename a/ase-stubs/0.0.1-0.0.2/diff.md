# Comparing `tmp/ase_stubs-0.0.1.tar.gz` & `tmp/ase_stubs-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ase_stubs-0.0.1.tar", max compression
+gzip compressed data, was "ase_stubs-0.0.2.tar", max compression
```

## Comparing `ase_stubs-0.0.1.tar` & `ase_stubs-0.0.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0      173 2023-07-22 10:08:40.345131 ase_stubs-0.0.1/.bumpversion.cfg
--rw-r--r--   0        0        0      353 2023-07-21 19:29:35.017542 ase_stubs-0.0.1/.editorconfig
--rw-r--r--   0        0        0      898 2023-07-21 19:29:35.018646 ase_stubs-0.0.1/.pre-commit-config.yaml
--rw-r--r--   0        0        0       55 2023-07-21 19:29:35.019679 ase_stubs-0.0.1/AUTHORS.rst
--rw-r--r--   0        0        0      638 2023-07-22 10:11:28.749318 ase_stubs-0.0.1/CHANGELOG.rst
--rw-r--r--   0        0        0     1346 2023-07-21 19:29:35.020691 ase_stubs-0.0.1/CONTRIBUTING.rst
--rw-r--r--   0        0        0    18092 2023-07-21 19:29:35.021334 ase_stubs-0.0.1/LICENSE
--rw-r--r--   0        0        0      661 2023-07-22 02:51:37.295366 ase_stubs-0.0.1/README.rst
--rw-r--r--   0        0        0     2812 2023-07-22 10:08:29.569391 ase_stubs-0.0.1/pyproject.toml
--rw-r--r--   0        0        0       71 2023-07-21 19:29:35.023949 ase_stubs-0.0.1/src/ase-stubs/__init__.pyi
--rw-r--r--   0        0        0     1175 2023-07-22 06:49:51.995546 ase_stubs-0.0.1/src/ase-stubs/atom.pyi
--rw-r--r--   0        0        0    13464 2023-07-22 10:06:00.064125 ase_stubs-0.0.1/src/ase-stubs/atoms.pyi
--rw-r--r--   0        0        0     1771 2023-07-21 20:10:38.387164 ase_stubs-0.0.1/src/ase-stubs/cell.pyi
--rw-r--r--   0        0        0     1466 2023-07-22 07:13:35.768097 ase_stubs-0.0.1/src/ase-stubs/geometry/geometry.pyi
--rw-r--r--   0        0        0     1559 1970-01-01 00:00:00.000000 ase_stubs-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0      173 2023-07-22 23:19:41.132516 ase_stubs-0.0.2/.bumpversion.cfg
+-rw-r--r--   0        0        0      353 2023-07-21 19:29:35.017542 ase_stubs-0.0.2/.editorconfig
+-rw-r--r--   0        0        0      898 2023-07-21 19:29:35.018646 ase_stubs-0.0.2/.pre-commit-config.yaml
+-rw-r--r--   0        0        0       55 2023-07-21 19:29:35.019679 ase_stubs-0.0.2/AUTHORS.rst
+-rw-r--r--   0        0        0      995 2023-07-22 23:18:16.508291 ase_stubs-0.0.2/CHANGELOG.rst
+-rw-r--r--   0        0        0     1346 2023-07-21 19:29:35.020691 ase_stubs-0.0.2/CONTRIBUTING.rst
+-rw-r--r--   0        0        0    18092 2023-07-21 19:29:35.021334 ase_stubs-0.0.2/LICENSE
+-rw-r--r--   0        0        0      661 2023-07-22 02:51:37.295366 ase_stubs-0.0.2/README.rst
+-rw-r--r--   0        0        0     2812 2023-07-22 23:19:41.132919 ase_stubs-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0       71 2023-07-21 19:29:35.023949 ase_stubs-0.0.2/src/ase-stubs/__init__.pyi
+-rw-r--r--   0        0        0     1175 2023-07-22 06:49:51.995546 ase_stubs-0.0.2/src/ase-stubs/atom.pyi
+-rw-r--r--   0        0        0    13864 2023-07-22 23:18:16.509523 ase_stubs-0.0.2/src/ase-stubs/atoms.pyi
+-rw-r--r--   0        0        0     1771 2023-07-21 20:10:38.387164 ase_stubs-0.0.2/src/ase-stubs/cell.pyi
+-rw-r--r--   0        0        0     2387 2023-07-22 20:23:37.927135 ase_stubs-0.0.2/src/ase-stubs/geometry/geometry.pyi
+-rw-r--r--   0        0        0     1559 1970-01-01 00:00:00.000000 ase_stubs-0.0.2/PKG-INFO
```

### Comparing `ase_stubs-0.0.1/.pre-commit-config.yaml` & `ase_stubs-0.0.2/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `ase_stubs-0.0.1/CONTRIBUTING.rst` & `ase_stubs-0.0.2/CONTRIBUTING.rst`

 * *Files identical despite different names*

### Comparing `ase_stubs-0.0.1/LICENSE` & `ase_stubs-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `ase_stubs-0.0.1/README.rst` & `ase_stubs-0.0.2/README.rst`

 * *Files identical despite different names*

### Comparing `ase_stubs-0.0.1/pyproject.toml` & `ase_stubs-0.0.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "ase-stubs"
-version = "0.0.1"
+version = "0.0.2"
 description = "Stub files for the Atomic Simulation Environment package."
 authors = [
     "Ugochukwu Nwosu <ugognw@gmail.com>"
     ]
 license = "LGPL-2.1-or-later"
 readme = "README.rst"
 repository = "https://gitlab.com/ugognw/python-comp-chem-utils"
```

### Comparing `ase_stubs-0.0.1/src/ase-stubs/atom.pyi` & `ase_stubs-0.0.2/src/ase-stubs/atom.pyi`

 * *Files identical despite different names*

### Comparing `ase_stubs-0.0.1/src/ase-stubs/atoms.pyi` & `ase_stubs-0.0.2/src/ase-stubs/atoms.pyi`

 * *Files 22% similar despite different names*

```diff
@@ -1,68 +1,55 @@
 from collections.abc import Iterable
 from collections.abc import Iterator
 from collections.abc import Sequence
+import numbers
 from pathlib import PurePath
 from typing import IO
 from typing import Any
 from typing import Literal
+from typing import Self
 from typing import TypedDict
 from typing import TypeVar
 from typing import overload
 
 from _typeshed import Incomplete
-from ase.atom import Atom as Atom
+from ase.atom import Atom
 from ase.calculators.calculator import Calculator
-from ase.cell import Cell as Cell
+from ase.cell import Cell
 from ase.constraints import FixConstraint
-from ase.data import atomic_masses as atomic_masses
-from ase.data import atomic_masses_common as atomic_masses_common
-from ase.geometry import find_mic as find_mic
-from ase.geometry import get_angles as get_angles
-from ase.geometry import get_dihedrals as get_dihedrals
-from ase.geometry import get_distances as get_distances
-from ase.geometry import wrap_positions as wrap_positions
 from ase.outputs import Properties
-from ase.stress import full_3x3_to_voigt_6_stress as full_3x3_to_voigt_6_stress
-from ase.stress import voigt_6_to_full_3x3_stress as voigt_6_to_full_3x3_stress
-from ase.symbols import Symbols as Symbols
-from ase.symbols import symbols2numbers as symbols2numbers
-from ase.utils import deprecated as deprecated
+from ase.symbols import Symbols
 import numpy as np
 from numpy.random import BitGenerator
 from numpy.random import RandomState
 import numpy.typing as npt
 from typing_extensions import Unpack
 
 class Atoms:
     ase_objtype: str
     arrays: Incomplete
     info: Incomplete
     def __init__(
         self,
         symbols: str | Atoms | Sequence[str | Atom] | None = ...,
-        positions: npt.ArrayLike[float] | None = ...,
-        numbers: npt.ArrayLike[int] | None = ...,
-        tags: npt.ArrayLike[int] | None = ...,
-        momenta: npt.ArrayLike[npt.ArrayLike[float]] | None = ...,
-        masses: npt.ArrayLike[float] | None = ...,
-        magmoms: npt.ArrayLike[float]
-        | npt.ArrayLike[npt.ArrayLike[float]]
-        | None = ...,
-        charges: npt.ArrayLike[float] | None = ...,
-        scaled_positions: npt.ArrayLike[float] | None = ...,
-        cell: npt.ArrayLike[float]
-        | npt.ArrayLike[npt.ArrayLike[float]]
-        | None = ...,
+        positions: npt.ArrayLike[numbers.Real] | None = ...,
+        numbers: npt.ArrayLike[numbers.Integral] | None = ...,
+        tags: npt.ArrayLike[numbers.Integral] | None = ...,
+        momenta: npt.ArrayLike[numbers.Real] | None = ...,
+        masses: npt.ArrayLike[numbers.Real] | None = ...,
+        magmoms: npt.ArrayLike[numbers.Real] | None = ...,
+        charges: npt.ArrayLike[numbers.Real] | None = ...,
+        scaled_positions: npt.ArrayLike[numbers.Real] | None = ...,
+        cell: npt.ArrayLike[numbers.Real] | None = ...,
         pbc: bool | None = ...,
-        celldisp: npt.ArrayLike | None = ...,
+        celldisp: npt.ArrayLike[numbers.Real] | None = ...,
         constraint: FixConstraint | None = ...,
         calculator: Calculator | None = ...,
         info: dict | None = ...,
-        velocities: npt.ArrayLike[npt.ArrayLike[float]] | None = ...,
+        velocities: npt.ArrayLike[numbers.Real] | None = ...,
     ) -> None: ...
     @property
     def symbols(self) -> Symbols: ...
     def set_calculator(self, calc: Calculator | None = ...) -> None: ...
     def get_calculator(self) -> Calculator | None: ...
     @property
     def calc(self) -> Calculator | None: ...
@@ -74,319 +61,339 @@
         | tuple[FixConstraint]
         | list[FixConstraint]
         | None = ...,
     ) -> None: ...
     constraints: list[FixConstraint]
     def set_cell(
         self,
-        cell: npt.ArrayLike[float]
-        | npt.ArrayLike[npt.ArrayLike[float]]
-        | None,
+        cell: npt.ArrayLike[numbers.Real] | None,
         scale_atoms: bool = ...,
         apply_constraint: bool = ...,
     ) -> None: ...
-    def set_celldisp(self, celldisp: npt.ArrayLike) -> None: ...
-    def get_celldisp(self) -> npt.ArrayLike: ...
+    def set_celldisp(self, celldisp: npt.ArrayLike[numbers.Real]) -> None: ...
+    def get_celldisp(self) -> npt.NDArray[np.float_]: ...
     def get_cell(self, complete: bool = ...) -> Cell: ...
-    def get_cell_lengths_and_angles(self) -> np.ndarray[np.floating]: ...
+    def get_cell_lengths_and_angles(self) -> npt.NDArray[np.float_]: ...
     def get_reciprocal_cell(self) -> Cell: ...
     @property
-    def pbc(self) -> np.ndarray[bool]: ...
-    def set_pbc(self, pbc: np.ndarray[bool]) -> None: ...
-    def get_pbc(self) -> np.ndarray[bool]: ...
+    def pbc(self) -> npt.NDArray[np.bool_]: ...
+    def set_pbc(self, pbc: npt.NDArray[np.bool_]) -> None: ...
+    def get_pbc(self) -> npt.NDArray[np.bool_]: ...
     @overload
     def new_array(
         self,
         name: Any,
         a: npt.ArrayLike,
         dtype: type = ...,
-        shape: tuple | np.ndarray | None = ...,
+        shape: tuple[int, ...] | None = ...,
     ) -> None: ...
     @overload
     def new_array(
         self,
         name: Any,
-        a: np.ndarray,
+        a: npt.NDArray,
         dtype: Any = ...,
-        shape: tuple | np.ndarray | None = ...,
+        shape: tuple[int, ...] | None = ...,
     ) -> None: ...
-    def get_array(self, name: Any, copy: bool = ...) -> np.ndarray: ...
+    def get_array(self, name: Any, copy: bool = ...) -> npt.NDArray: ...
     @overload
     def set_array(
         self,
         name: Any,
         a: npt.ArrayLike,
         dtype: type = ...,
-        shape: tuple | np.ndarray | None = ...,
+        shape: tuple[int, ...] | None = ...,
     ) -> None: ...
     @overload
     def set_array(
         self,
         name: Any,
-        a: np.ndarray,
+        a: npt.NDArray,
         dtype: Any = ...,
-        shape: tuple | np.ndarray | None = ...,
+        shape: tuple[int, ...] | None = ...,
     ) -> None: ...
     def has(self, name: Any) -> bool: ...
-    def set_atomic_numbers(self, numbers: npt.ArrayLike[int]) -> None: ...
-    def get_atomic_numbers(self) -> np.ndarray[int]: ...
+    def set_atomic_numbers(self, numbers: npt.ArrayLike[numbers.Integral]) -> None: ...
+    def get_atomic_numbers(self) -> npt.NDArray[np.int_]: ...
     def get_chemical_symbols(self) -> list[str]: ...
     def set_chemical_symbols(
-        self, symbols: str | Iterable[str | int]
+        self, symbols: str | Iterable[str | numbers.Integral]
     ) -> None: ...
     def get_chemical_formula(
-        self, mode: str = ..., empirical: bool = ...
+        self,
+        mode: Literal['all', 'reduce', 'hill', 'metal'] = ...,
+        empirical: bool = ...,
     ) -> str: ...
-    def set_tags(self, tags: int | npt.ArrayLike) -> None: ...
-    def get_tags(self) -> np.ndarray[int]: ...
+    def set_tags(self, tags: int | npt.ArrayLike[numbers.Integral]) -> None: ...
+    def get_tags(self) -> npt.NDArray[np.int_]: ...
     def set_momenta(
         self,
-        momenta: npt.ArrayLike[npt.ArrayLike[float]],
+        momenta: npt.ArrayLike[numbers.Real],
         apply_constraint: bool = ...,
     ) -> None: ...
-    def set_velocities(
-        self, velocities: npt.ArrayLike[npt.ArrayLike[float]]
-    ) -> None: ...
-    def get_momenta(self) -> np.ndarray[float]: ...
+    def set_velocities(self, velocities: npt.ArrayLike[numbers.Real]) -> None: ...
+    def get_momenta(self) -> npt.NDArray[np.float_]: ...
     def set_masses(
         self,
         masses: Literal['defaults']
         | Literal['most_common']
-        | Iterable[float | None]
-        | np.ndarray
+        | Iterable[numbers.Real | None]
         | None = ...,
     ) -> None: ...
-    def get_masses(self) -> np.ndarray[float]: ...
+    def get_masses(self) -> npt.NDArray[np.float_]: ...
     def set_initial_magnetic_moments(
         self,
-        magmoms: npt.ArrayLike[float]
-        | npt.ArrayLike[npt.ArrayLike[float]]
-        | None = ...,
+        magmoms: npt.ArrayLike[numbers.Real] | None = ...,
     ) -> None: ...
-    def get_initial_magnetic_moments(self) -> np.ndarray[float]: ...
-    def get_magnetic_moments(self) -> np.ndarray[float] | None: ...
-    def get_magnetic_moment(self) -> float | None: ...
+    def get_initial_magnetic_moments(self) -> npt.NDArray[np.float_]: ...
+    def get_magnetic_moments(self) -> npt.NDArray[np.float_] | None: ...
+    def get_magnetic_moment(self) -> numbers.Real | None: ...
     def set_initial_charges(
-        self, charges: npt.ArrayLike[float] | None = ...
+        self, charges: npt.ArrayLike[numbers.Real] | None = ...
     ) -> None: ...
-    def get_initial_charges(self) -> np.ndarray[float]: ...
-    def get_charges(self) -> np.ndarray[float] | None: ...
+    def get_initial_charges(self) -> npt.NDArray[np.float_]: ...
+    def get_charges(self) -> npt.NDArray[np.float_] | None: ...
     def set_positions(
         self,
-        newpositions: npt.ArrayLike[npt.ArrayLike[float]],
+        newpositions: npt.ArrayLike[numbers.Real],
         apply_constraint: bool = ...,
     ) -> None: ...
     def get_positions(
         self,
         wrap: bool = ...,
         **wrap_kw: Unpack[
             TypedDict(
                 'wrap_kw',
                 {
-                    'pbc': bool | npt.ArrayLike[bool],
-                    'center': npt.ArrayLike[float],
+                    'pbc': bool | npt.ArrayLike[bool | np.bool_],
+                    'center': npt.ArrayLike[numbers.Real],
                     'pretty_translation': bool,
                     'eps': float,
                 },
                 total=False,
             )
         ],
-    ) -> np.ndarray[float]: ...
+    ) -> npt.NDArray[np.float_]: ...
     def get_potential_energy(
         self, force_consistent: bool = ..., apply_constraint: bool = ...
-    ) -> float | None: ...
-    def get_properties(
-        self, properties: list[str] | tuple[str]
-    ) -> Properties: ...
-    def get_potential_energies(self) -> np.ndarray[float] | None: ...
-    def get_kinetic_energy(self) -> float: ...
-    def get_velocities(self) -> np.ndarray[float]: ...
-    def get_total_energy(self) -> float: ...
+    ) -> numbers.Real | None: ...
+    def get_properties(self, properties: list[str] | tuple[str]) -> Properties: ...
+    def get_potential_energies(self) -> npt.NDArray[np.float_] | None: ...
+    def get_kinetic_energy(self) -> numbers.Real: ...
+    def get_velocities(self) -> npt.NDArray[np.float_]: ...
+    def get_total_energy(self) -> numbers.Real: ...
     def get_forces(
         self, apply_constraint: bool = ..., md: bool = ...
-    ) -> np.ndarray[float] | None: ...
+    ) -> npt.NDArray[np.float_] | None: ...
     def get_stress(
         self,
         voigt: bool = ...,
         apply_constraint: bool = ...,
         include_ideal_gas: bool = ...,
-    ) -> np.ndarray[float] | None: ...
+    ) -> npt.NDArray[np.float_] | None: ...
     def get_stresses(
         self, include_ideal_gas: bool = ..., voigt: bool = ...
-    ) -> np.ndarray[float] | None: ...
-    def get_dipole_moment(self) -> np.ndarray[float] | None: ...
-    def copy(self) -> Atoms: ...
+    ) -> npt.NDArray[np.float_] | None: ...
+    def get_dipole_moment(self) -> npt.NDArray[np.float_] | None: ...
+    def copy(self) -> Self: ...
     def todict(self) -> dict: ...
     @classmethod
-    def fromdict(cls, dct: dict) -> Atoms: ...
+    def fromdict(cls, dct: dict) -> Self: ...
     def __len__(self) -> int: ...
     def get_number_of_atoms(self) -> int: ...
     def get_global_number_of_atoms(self) -> int: ...
-    def __add__(self, other: Atom | Atoms) -> Atoms: ...
+    def __add__(self, other: Atom | Atoms) -> Self: ...
     def extend(self, other: Atom | Atoms) -> None: ...
-    def __iadd__(self, other: Atom | Atoms) -> Atoms: ...
+    def __iadd__(self, other: Atom | Atoms) -> Self: ...
     def append(self, atom: Atom | Atoms) -> None: ...
     def __iter__(self) -> Iterator[Atom]: ...
     @overload
-    def __getitem__(self, i: int) -> Atom: ...
+    def __getitem__(self, i: numbers.Integral) -> Atom: ...
     @overload
-    def __getitem__(self, i: slice) -> Atoms: ...
-    def __delitem__(self, i: int | slice) -> None: ...
+    def __getitem__(self, i: slice | npt.ArrayLike[numbers.Integral]) -> Self: ...
+    def __delitem__(
+        self,
+        i: numbers.Integral
+        | slice
+        | list[numbers.Integral]
+        | npt.NDArray[np.bool_]
+        | npt.NDArray[np.integer],
+    ) -> None: ...
     def pop(self, i: int = ...) -> Atom: ...
-    def __imul__(self, m: int | npt.ArrayLike[int]) -> Atoms: ...
-    def repeat(self, rep: int | npt.ArrayLike[int]) -> Atoms: ...
-    def __mul__(self, rep: int | npt.ArrayLike[int]) -> Atoms: ...
+    def __imul__(self, m: int | npt.ArrayLike[numbers.Integral]) -> Self: ...
+    def repeat(self, rep: int | npt.ArrayLike[numbers.Integral]) -> Self: ...
+    def __mul__(self, rep: int | npt.ArrayLike[numbers.Integral]) -> Self: ...
     def translate(
-        self, displacement: float | npt.ArrayLike[float]
+        self, displacement: numbers.Real | npt.ArrayLike[numbers.Real]
     ) -> None: ...
     def center(
         self,
-        vacuum: float | None = ...,
-        axis: int | Iterable[int] = ...,
-        about: npt.ArrayLike[float] | None = ...,
+        vacuum: numbers.Real | None = ...,
+        axis: int | Iterable[numbers.Integral] = ...,
+        about: npt.ArrayLike[numbers.Real] | None = ...,
     ) -> None: ...
-    def get_center_of_mass(self, scaled: bool = ...) -> np.ndarray[float]: ...
+    def get_center_of_mass(self, scaled: bool = ...) -> npt.NDArray[np.float_]: ...
     def set_center_of_mass(
-        self, com: npt.ArrayLike[float], scaled: bool = ...
+        self, com: npt.ArrayLike[numbers.Real], scaled: bool = ...
     ) -> None: ...
     @overload
     def get_moments_of_inertia(
         self, vectors: Literal[True] = ...
-    ) -> tuple[np.ndarray[float], np.ndarray[float]]: ...
+    ) -> tuple[npt.NDArray[np.float_], npt.NDArray[np.float_]]: ...
     @overload
     def get_moments_of_inertia(
         self, vectors: Literal[False] = ...
-    ) -> np.ndarray[float]: ...
-    def get_angular_momentum(self) -> np.ndarray[float]: ...
+    ) -> npt.NDArray[np.float_]: ...
+    def get_angular_momentum(self) -> npt.NDArray[np.float_]: ...
     def rotate(
         self,
         a: Literal['x']
         | Literal['-x', 'y', '-y', 'z', '-z']
-        | float
-        | np.ndarray[float],
-        v: Literal['-x', 'y', '-y', 'z', '-z'] | np.ndarray[float],
-        center: str | npt.ArrayLike[float] = ...,
+        | numbers.Real
+        | npt.NDArray[np.float_],
+        v: Literal['-x', 'y', '-y', 'z', '-z'] | npt.NDArray[np.float_],
+        center: str | npt.ArrayLike[numbers.Real] = ...,
         rotate_cell: bool = ...,
     ) -> None: ...
     def euler_rotate(
         self,
-        phi: float = ...,
-        theta: float = ...,
-        psi: float = ...,
-        center: npt.ArrayLike[float] = ...,
+        phi: numbers.Real = ...,
+        theta: numbers.Real = ...,
+        psi: numbers.Real = ...,
+        center: npt.ArrayLike[numbers.Real] = ...,
     ) -> None: ...
     def get_dihedral(
-        self, a0: int, a1: int, a2: int, a3: int, mic: bool = ...
+        self,
+        a0: numbers.Integral,
+        a1: numbers.Integral,
+        a2: numbers.Integral,
+        a3: numbers.Integral,
+        mic: bool = ...,
     ) -> float: ...
     def get_dihedrals(
         self, indices: npt.ArrayLike[float], mic: bool = ...
-    ) -> np.ndarray[float]: ...
+    ) -> npt.NDArray[np.float_]: ...
     def set_dihedral(
         self,
-        a1: int,
-        a2: int,
-        a3: int,
-        a4: int,
-        angle: float,
+        a1: numbers.Integral,
+        a2: numbers.Integral,
+        a3: numbers.Integral,
+        a4: numbers.Integral,
+        angle: numbers.Real,
         mask: Sequence[bool] | None = ...,
         indices: Iterable[bool] | None = ...,
     ) -> None: ...
     def rotate_dihedral(
         self,
-        a1: int,
-        a2: int,
-        a3: int,
-        a4: int,
-        angle: float,
+        a1: numbers.Integral,
+        a2: numbers.Integral,
+        a3: numbers.Integral,
+        a4: numbers.Integral,
+        angle: numbers.Real,
         mask: Sequence[bool] | None = ...,
         indices: Iterable[bool] | None = ...,
     ) -> None: ...
     def get_angle(
-        self, a1: int, a2: int, a3: int, mic: bool = ...
+        self,
+        a1: numbers.Integral,
+        a2: numbers.Integral,
+        a3: numbers.Integral,
+        mic: bool = ...,
     ) -> float: ...
     def get_angles(
-        self, indices: npt.ArrayLike[int], mic: bool = ...
-    ) -> np.ndarray[float]: ...
+        self, indices: npt.ArrayLike[numbers.Integral], mic: bool = ...
+    ) -> npt.NDArray[np.float_]: ...
     def set_angle(
         self,
-        a1: int,
-        a2: int | None = ...,
-        a3: int | None = ...,
-        angle: float | None = ...,
+        a1: numbers.Integral,
+        a2: numbers.Integral | None = ...,
+        a3: numbers.Integral | None = ...,
+        angle: numbers.Real | None = ...,
         mask: Sequence[bool] | None = ...,
         indices: Iterable[bool] | None = ...,
         add: bool = ...,
     ) -> None: ...
     def rattle(
         self,
-        stdev: float = ...,
-        seed: int | npt.ArrayLike[int] | BitGenerator | None = ...,
+        stdev: numbers.Real = ...,
+        seed: numbers.Integral
+        | npt.ArrayLike[numbers.Integral]
+        | BitGenerator
+        | None = ...,
         rng: RandomState | None = ...,
     ) -> None: ...
     @overload
     def get_distance(
-        self, a0: int, a1: int, mic: bool = ..., vector: Literal[True] = ...
-    ) -> np.ndarray[float]: ...
+        self,
+        a0: numbers.Integral,
+        a1: numbers.Integral,
+        mic: bool = ...,
+        vector: Literal[True] = ...,
+    ) -> npt.NDArray[np.float_]: ...
     @overload
     def get_distance(
-        self, a0: int, a1: int, mic: bool = ..., vector: Literal[False] = ...
-    ) -> float: ...
+        self,
+        a0: numbers.Integral,
+        a1: numbers.Integral,
+        mic: bool = ...,
+        vector: Literal[False] = ...,
+    ) -> numbers.Real: ...
     def get_distances(
         self,
-        a: int,
-        indices: list[int] | list[bool] | slice | None,
+        a: numbers.Integral,
+        indices: list[numbers.Integral] | slice | None,
         mic: bool = ...,
         vector: bool = ...,
-    ) -> np.ndarray[float]: ...
+    ) -> npt.NDArray[np.float_]: ...
     def get_all_distances(
         self, mic: bool = ..., vector: bool = ...
-    ) -> np.ndarray[float]: ...
+    ) -> npt.NDArray[np.float_]: ...
     def set_distance(
         self,
-        a0: int,
-        a1: int,
-        distance: float,
+        a0: numbers.Integral,
+        a1: numbers.Integral,
+        distance: numbers.Real,
         fix: float = ...,
         mic: bool = ...,
         mask: Sequence[bool] | None = ...,
         indices: Iterable[bool] | None = ...,
         add: bool = ...,
         factor: bool = ...,
     ) -> None: ...
-    def get_scaled_positions(self, wrap: bool = ...) -> np.ndarray[float]: ...
-    def set_scaled_positions(self, scaled: npt.ArrayLike[float]) -> None: ...
+    def get_scaled_positions(self, wrap: bool = ...) -> npt.NDArray[np.float_]: ...
+    def set_scaled_positions(self, scaled: npt.ArrayLike[numbers.Real]) -> None: ...
     def wrap(
         self,
         **wrap_kw: Unpack[
             TypedDict(
                 'wrap_kw',
                 {
                     'pbc': bool | npt.ArrayLike[bool],
-                    'center': npt.ArrayLike[float],
+                    'center': npt.ArrayLike[numbers.Real],
                     'pretty_translation': bool,
-                    'eps': float,
+                    'eps': numbers.Real,
                 },
                 total=False,
             )
         ],
     ) -> None: ...
-    def get_temperature(self) -> float: ...
+    def get_temperature(self) -> numbers.Real: ...
     def __eq__(self, other: object) -> bool: ...
     def __ne__(self, other: object) -> bool: ...
     def get_volume(self) -> float: ...
-    positions: np.array[float]
+    positions: np.array[numbers.Real]
     numbers: np.array[int]
     @property
     def cell(self) -> Cell: ...
     def write(
         self, filename: str | PurePath | IO, format: str | None = ..., **kwargs
     ) -> None: ...
-    def iterimages(self) -> Iterator[Atoms]: ...
+    def iterimages(self) -> Iterator[Self]: ...
     def edit(self) -> None: ...
 
-def string2vector(v: str | npt.ArrayLike[float]) -> np.ndarray[float]: ...
+def string2vector(v: str | npt.ArrayLike[float]) -> npt.NDArray[np.float_]: ...
 @overload
 def default(data: None, dflt: Any) -> None: ...
 @overload
 def default(data: list | tuple, dflt: Any) -> list | None: ...
 @overload
 def default(data: TypeVar('T'), dflt: Any) -> TypeVar('T'): ...
```

### Comparing `ase_stubs-0.0.1/src/ase-stubs/cell.pyi` & `ase_stubs-0.0.2/src/ase-stubs/cell.pyi`

 * *Files identical despite different names*

### Comparing `ase_stubs-0.0.1/PKG-INFO` & `ase_stubs-0.0.2/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ase-stubs
-Version: 0.0.1
+Version: 0.0.2
 Summary: Stub files for the Atomic Simulation Environment package.
 Home-page: https://gitlab.com/ugognw/python-comp-chem-utils
 License: LGPL-2.1-or-later
 Author: Ugochukwu Nwosu
 Author-email: ugognw@gmail.com
 Requires-Python: >=3.10,<3.12
 Classifier: Development Status :: 5 - Production/Stable
```

