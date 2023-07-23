# Comparing `tmp/tcod_ecs-3.4.0.tar.gz` & `tmp/tcod_ecs-3.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tcod_ecs-3.4.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "tcod_ecs-3.5.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `tcod_ecs-3.4.0.tar` & `tcod_ecs-3.5.0.tar`

### file list

```diff
@@ -1,7 +1,8 @@
--rw-r--r--   0        0        0     1079 2023-07-13 06:01:45.198624 tcod_ecs-3.4.0/LICENSE
--rw-r--r--   0        0        0     8409 2023-07-13 06:01:45.198624 tcod_ecs-3.4.0/README.md
--rw-r--r--   0        0        0     3499 2023-07-13 06:01:45.198624 tcod_ecs-3.4.0/pyproject.toml
--rw-r--r--   0        0        0    39512 2023-07-13 06:01:45.198624 tcod_ecs-3.4.0/tcod/ecs/__init__.py
--rw-r--r--   0        0        0      160 2023-07-13 06:01:52.738556 tcod_ecs-3.4.0/tcod/ecs/_version.py
--rw-r--r--   0        0        0        0 2023-07-13 06:01:45.198624 tcod_ecs-3.4.0/tcod/ecs/py.typed
--rw-r--r--   0        0        0     9604 1970-01-01 00:00:00.000000 tcod_ecs-3.4.0/PKG-INFO
+-rw-r--r--   0        0        0     1079 2023-07-23 10:27:37.759252 tcod_ecs-3.5.0/LICENSE
+-rw-r--r--   0        0        0    10473 2023-07-23 10:27:37.759252 tcod_ecs-3.5.0/README.md
+-rw-r--r--   0        0        0     3534 2023-07-23 10:27:37.759252 tcod_ecs-3.5.0/pyproject.toml
+-rw-r--r--   0        0        0    44807 2023-07-23 10:27:37.759252 tcod_ecs-3.5.0/tcod/ecs/__init__.py
+-rw-r--r--   0        0        0     1512 2023-07-23 10:27:37.759252 tcod_ecs-3.5.0/tcod/ecs/_converter.py
+-rw-r--r--   0        0        0      160 2023-07-23 10:27:46.603264 tcod_ecs-3.5.0/tcod/ecs/_version.py
+-rw-r--r--   0        0        0        0 2023-07-23 10:27:37.759252 tcod_ecs-3.5.0/tcod/ecs/py.typed
+-rw-r--r--   0        0        0    11727 1970-01-01 00:00:00.000000 tcod_ecs-3.5.0/PKG-INFO
```

### Comparing `tcod_ecs-3.4.0/LICENSE` & `tcod_ecs-3.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `tcod_ecs-3.4.0/README.md` & `tcod_ecs-3.5.0/README.md`

 * *Files 27% similar despite different names*

```diff
@@ -1,28 +1,28 @@
 # About
 
 [![PyPI](https://img.shields.io/pypi/v/tcod-ecs)](https://pypi.org/project/tcod-ecs/)
 [![PyPI - License](https://img.shields.io/pypi/l/tcod-ecs)](https://github.com/HexDecimal/python-tcod-ecs/blob/main/LICENSE)
 [![Documentation Status](https://readthedocs.org/projects/python-tcod-ecs/badge/?version=latest)](https://python-tcod-ecs.readthedocs.io)
 [![codecov](https://codecov.io/gh/HexDecimal/python-tcod-ecs/branch/main/graph/badge.svg?token=4Ak5QpTLZB)](https://codecov.io/gh/HexDecimal/python-tcod-ecs)
 
-This is an [Entity-component-system](https://en.wikipedia.org/wiki/Entity_component_system) implemented in Python.
+`tcod-ecs` is a [Sparse-set](https://skypjack.github.io/2020-08-02-ecs-baf-part-9/) [Entity-component-system](https://en.wikipedia.org/wiki/Entity_component_system) implemented using Python's `dict` and `set` types.
 See the [ECS FAQ](https://github.com/SanderMertens/ecs-faq) for more info.
 
 This implementation focuses on type-hinting, organization, and is designed to work well with Python.
 The following features are currently implemented:
 
-- Entities can have store components which are instances of any Python object. Components are looked up by their type.
-- Entities can have one instance of a type, or multiple instances of a type with a string or other hashable to differentiate them.
-- Components can be registered as abstract, allowing a base type to hold subclasses of that component.
-- Entity tags are distinct from components, tags are any hashable Python object rather than empty class.
+- Entities can store components which are instances of any Python object. Components are looked up by their type.
+- Entities can have one instance of a type, or multiple instances of a type using a hashable tag to differentiate them.
 - Entity relationships are supported, either as many-to-many or many-to-one relationships.
-- ECS Queries can be made to fetch entities having a combination of components/tags/relations or the absence of such.
+- ECS Queries can be made to fetch entities having a combination of components/tags/relations or excluding such.
+- The ECS World object can be serialized with Python's pickle module for easy storage.
 
 A lightweight version which implements only the entity-component framework exists called [tcod-ec](https://pypi.org/project/tcod-ec/).
+`tcod-ec` was geared towards a dynamic-typed-dict style of syntax and is missing a lot of important features such as queries and named components.
 
 # Installation
 
 Use pip to install this library:
 ```
 pip install tcod-ecs
 ```
@@ -38,17 +38,17 @@
 >>> import tcod.ecs
 >>> world = tcod.ecs.World()  # New empty world
 
 ```
 
 ## Entity
 
-Each Entity is identified by its unique id (`uid`) which can be any hashable object and the `world` it belongs to.
-New unique entities can be created with `World.new_entity` which uses a new `object()` as the `uid`.
-An entity always knows about its assigned world.
+Each Entity is identified by its unique id (`uid`) which can be any hashable object combined with the `world` it belongs.
+New unique entities can be created with `World.new_entity` which uses a new `object()` as the `uid`, this guarantees uniqueness which is not always desireable.
+An entity always knows about its assigned world, which can be access with the `Entity.world` property from any Entity instance.
 Worlds only know about their entities once the entity is assigned a name, component, tag, or relation.
 
 ```py
 >>> entity = world.new_entity()  # Creates a unique entity using `object()` as the uid
 >>> entity
 <Entity(uid=object at ...)>
 >>> entity.world is world  # Worlds can always be accessed from their entity
@@ -56,32 +56,41 @@
 >>> world[entity.uid] is entity  # Entities with the same world/uid are compared using `is`
 True
 
 # Reference an entity with the given uid, can be any hashable object:
 >>> entity = world["MyEntity"]
 >>> entity
 <Entity(uid='MyEntity')>
->>> world["MyEntity"] is entity
+>>> world["MyEntity"] is entity  # Matching entities ALWAYS share a single identity
 True
 
 ```
 
 Use `World.new_entity` to create unique entities and use `World[x]` to reference a global entity or relation with an id.
+`World[None]` is recommend for use as a global entity when you want to store components in the world itself.
+
+Do not save the `uid`'s of entities to be used later with `World[uid]`, this process is slower than holding onto the Entity instance.
 
 ## Serialization
 
-Worlds are normal Python objects and can be pickled as long as all stored components can be pickled.
+Worlds are normal Python objects and can be pickled as long as all stored components are pickleable.
 
 ```py
 >>> import pickle
 >>> pickled_data: bytes = pickle.dumps(world)
 >>> world = pickle.loads(pickled_data)
 
 ```
 
+Stability is a priority but changes may still break older saves.
+Backwards compatibility is not a priority, pickled worlds should not be unpickled with an older version of the library.
+This project follows [Semantic Versioning](https://semver.org/), major version increments will break the API, the save format or both, minor version increments may break backwards compatibility.
+Check the [changelog](https://github.com/HexDecimal/python-tcod-ecs/blob/main/CHANGELOG.md) to be aware of format changes and breaks.
+There should always be a transition period before a format break, so keeping up with the latest version is a good idea.
+
 ## Components
 
 Components are instances of any Python type.
 These can be accessed, assigned, or removed from entities via the dict-like `Entity.components` attribute.
 The type is used as the key to access the component.
 The types used can be custom classes or standard Python types.
 
@@ -93,15 +102,15 @@
 42
 >>> int in entity.components
 True
 >>> del entity.components[int]
 >>> entity.components[int]  # Missing keys raise KeyError
 Traceback (most recent call last):
   ...
-KeyError: <Entity...>
+KeyError: <class 'int'>
 >>> entity.components.get(int, "default")  # Test keys with `.get()` like a dictionary
 'default'
 >>> @attrs.define
 ... class Vector2:
 ...     x: int = 0
 ...     y: int = 0
 >>> entity.components[Vector2] = Vector2(1, 2)
@@ -132,15 +141,15 @@
 
 ```
 
 ## Named Components
 
 Only one component can be assigned unless that component is given a unique name.
 You can name components with the key syntax `(name, type)` when assigning components.
-Names are not limited to strings, and can be any hashable or frozen object.
+Names are not limited to strings, they are a tag equivalent and can be any hashable or frozen object.
 The syntax `[type]` and `[(name, type)]` can be used interchangeably in all places accepting a component key.
 Queries on components access named components with the same syntax and must use names explicitly.
 
 ```py
 >>> entity = world.new_entity()
 >>> entity.components[Vector2] = Vector2(0, 0)
 >>> entity.components[("velocity", Vector2)] = Vector2(1, 1)
@@ -190,19 +199,21 @@
 >>> set(world.Q.all_of(tags=["player"])) == {entity}
 True
 
 ```
 
 ## Relations
 
-Use `Entity.relation_components[component_key][target] = component` to associate a relation with data.
+Use `Entity.relation_components[component_key][target] = component` to associate a target entity with a component.
 Use `Entity.relation_tag[tag] = target` to associate a tag exclusively with a target entity.
 Use `Entity.relation_tags_many[tag].add(target)` to associate a tag with multiple targets.
-Tags and relations share the same space then queried, so tags can not be in the format of a component key.
-Relations are unidirectional.
+
+Relation queries are a little more complex than other queries.
+Relation tags and relation components share the same space then queried, so 'normal' tags should not be in the format of a component key.
+Relations are unidirectional, but you can query either end of a relation.
 
 ```py
 >>> @attrs.define
 ... class OrbitOf:  # OrbitOf component
 ...     dist: int
 >>> LandedOn = "LandedOn"  # LandedOn tag
 >>> star = world.new_entity()
@@ -224,7 +235,17 @@
 True
 >>> set(world.Q.all_of(relations=[(LandedOn, ...)])) == {ship, moon_rock, player}
 True
 >>> set(world.Q.all_of(relations=[(LandedOn, ...)]).none_of(relations=[(LandedOn, moon)])) == {player}
 True
 
 ```
+
+You can use the following table to help with constructing relation queries.
+`tag` is a component key if you are querying for a component relation.
+
+| Includes                                                              | Syntax |
+| --------------------------------------------------------------------- | :----: |
+| Entities with a relation tag to the given target                      | `(tag, target_entity)` |
+| Entities with a relation tag to any target                            | `(tag, ...)` |
+| Entities which are a relation target of a given entity                | `(origin_entity, tag, None)` |
+| Entities which are a target of any entity with the given relation tag | `(..., tag, None)` |
```

### Comparing `tcod_ecs-3.4.0/pyproject.toml` & `tcod_ecs-3.5.0/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -14,15 +14,15 @@
     "Operating System :: OS Independent",
     "Programming Language :: Python :: 3",
     "Topic :: Software Development :: Libraries :: Python Modules",
     "Typing :: Typed",
 ]
 dynamic = ["version", "description"]
 requires-python = ">=3.8"
-dependencies = ["typing-extensions >=4.4.0"]
+dependencies = ["typing-extensions >=4.4.0", "attrs>=23.1.0", "cattrs>=23.1.2"]
 
 [tool.setuptools_scm]
 write_to = "tcod/ecs/_version.py"
 
 [project.optional-dependencies]
 test = [
     "attrs >=22.2.0",
```

### Comparing `tcod_ecs-3.4.0/tcod/ecs/__init__.py` & `tcod_ecs-3.5.0/tcod/ecs/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -4,40 +4,48 @@
 import sys
 import warnings
 from collections import defaultdict
 from typing import (
     TYPE_CHECKING,
     AbstractSet,
     Any,
+    DefaultDict,
+    Dict,
     Final,
     Generic,
     Iterable,
     Iterator,
     Mapping,
     MutableMapping,
     MutableSet,
+    Set,
     Tuple,
     Type,
     TypeVar,
     Union,
     overload,
 )
 from weakref import WeakKeyDictionary, WeakValueDictionary
 
+import attrs
 from typing_extensions import Self
 
+import tcod.ecs._converter
 from tcod.ecs import _version
 
-__version__ = _version.__version__
+if TYPE_CHECKING:
+    from _typeshed import SupportsKeysAndGetItem
 
 if sys.version_info >= (3, 10):  # pragma: no cover
     from types import EllipsisType
 else:  # pragma: no cover
     EllipsisType = Any
 
+__version__ = _version.__version__
+
 T = TypeVar("T")
 _T1 = TypeVar("_T1")
 _T2 = TypeVar("_T2")
 _T3 = TypeVar("_T3")
 _T4 = TypeVar("_T4")
 _T5 = TypeVar("_T5")
 _ComponentKey = Union[Type[T], Tuple[object, Type[T]]]
@@ -330,34 +338,34 @@
             getattr(key, "_TCOD_BASE_COMPONENT", key) is key
         ), "Abstract components must be accessed via the base class."
         return True
 
     def __getitem__(self, key: _ComponentKey[T]) -> T:
         """Return a component belonging to this entity."""
         assert self.__assert_key(key)
-        return self.entity.world._components_by_type[key][self.entity]  # type: ignore[no-any-return]
+        return self.entity.world._components_by_entity[self.entity][key]  # type: ignore[no-any-return]
 
     def __setitem__(self, key: _ComponentKey[T], value: T) -> None:
         """Assign a component to an entity."""
         assert self.__assert_key(key)
+        self.entity.world._components_by_entity[self.entity][key] = value
         self.entity.world._components_by_type[key][self.entity] = value
-        self.entity.world._components_by_entity[self.entity].add(key)
 
     def __delitem__(self, key: type[object] | tuple[object, type[object]]) -> None:
         """Delete a component from an entity."""
         assert self.__assert_key(key)
 
+        del self.entity.world._components_by_entity[self.entity][key]
+        if not self.entity.world._components_by_entity[self.entity]:
+            del self.entity.world._components_by_entity[self.entity]
+
         del self.entity.world._components_by_type[key][self.entity]
         if not self.entity.world._components_by_type[key]:
             del self.entity.world._components_by_type[key]
 
-        self.entity.world._components_by_entity[self.entity].remove(key)
-        if not self.entity.world._components_by_entity[self.entity]:
-            del self.entity.world._components_by_entity[self.entity]
-
     def __contains__(self, key: _ComponentKey[object]) -> bool:  # type: ignore[override]
         """Return True if this entity has the provided component."""
         return key in self.entity.world._components_by_entity.get(self.entity, ())
 
     def __iter__(self) -> Iterator[_ComponentKey[Any]]:
         """Iterate over the component types belonging to this entity."""
         return iter(self.entity.world._components_by_entity.get(self.entity, ()))
@@ -388,37 +396,38 @@
         for key in self:
             if not isinstance(key, tuple):
                 continue
             key_name, key_component = key
             if key_component is component_type and isinstance(key_name, name_type):
                 yield key_name, key_component
 
-    def __ior__(self, value: Mapping[_ComponentKey[Any], Any] | Iterable[tuple[_ComponentKey[Any], Any]]) -> Self:
+    def __ior__(
+        self, value: SupportsKeysAndGetItem[_ComponentKey[Any], Any] | Iterable[tuple[_ComponentKey[Any], Any]]
+    ) -> Self:
         """Update components in-place.
 
         .. versionadded:: 3.4
         """
         self.update(value)
         return self
 
-    if TYPE_CHECKING:  # Type-hinted overrides
-
-        @overload
-        def get(self, __key: _ComponentKey[T]) -> T | None:
-            ...
-
-        @overload
-        def get(self, __key: _ComponentKey[T], __default: T) -> T:
-            ...
-
-        def get(self, __key: _ComponentKey[T], __default: T | None = None) -> T | None:
-            """Return a component, returns None or a default value when the component is missing."""
+    def get(self, __key: _ComponentKey[T], __default: T | None = None) -> T | None:
+        """Return a component, returns None or a default value when the component is missing."""
+        try:
+            return self[__key]
+        except KeyError:
+            return __default
 
-        def setdefault(self, __key: _ComponentKey[T], __default: T) -> T:  # type: ignore[override]
-            """Assign a default value if a component is missing, then returns the current value."""
+    def setdefault(self, __key: _ComponentKey[T], __default: T) -> T:  # type: ignore[override]
+        """Assign a default value if a component is missing, then returns the current value."""
+        try:
+            return self[__key]
+        except KeyError:
+            self[__key] = __default
+            return __default
 
 
 class EntityTags(MutableSet[Any]):
     """A proxy attribute to access an entities tags like a set.
 
     See :any:`Entity.tags`.
     """
@@ -670,19 +679,19 @@
         if not world._relations_lookup[(self.key, target)]:
             del world._relations_lookup[(self.key, target)]
 
         world._relations_lookup[(self.key, ...)].discard(self.entity)
         if not world._relations_lookup[(self.key, ...)]:
             del world._relations_lookup[(self.key, ...)]
 
-        world._relations_lookup[(self.entity, self.key, None)].discard(self.entity)
+        world._relations_lookup[(self.entity, self.key, None)].discard(target)
         if not world._relations_lookup[(self.entity, self.key, None)]:
             del world._relations_lookup[(self.entity, self.key, None)]
 
-        world._relations_lookup[(..., self.key, None)].discard(self.entity)
+        world._relations_lookup[(..., self.key, None)].discard(target)
         if not world._relations_lookup[(..., self.key, None)]:
             del world._relations_lookup[(..., self.key, None)]
 
     def __iter__(self) -> Iterator[Entity]:
         """Iterate over the targets with assigned components."""
         by_entity = self.entity.world._relation_components_by_entity.get(self.entity)
         return iter(()) if by_entity is None else iter(by_entity.get(self.key, ()))
@@ -710,93 +719,148 @@
         """Access relations for this component key as a `{target: component}` dict-like object."""
         return EntityComponentRelationMapping(self.entity, key)
 
     def __delitem__(self, key: _ComponentKey[object]) -> None:
         """Remove all relations associated with this component key."""
         EntityComponentRelationMapping(self.entity, key).clear()
 
+    def __contains__(self, key: _ComponentKey[object]) -> bool:
+        """Return True if this entity contains a relation component for this component key."""
+        return bool(EntityComponentRelationMapping(self.entity, key))
+
 
 def _defaultdict_of_set() -> defaultdict[_T1, set[_T2]]:
     """Return a new defaultdict of sets."""
     return defaultdict(set)
 
 
 def _defaultdict_of_dict() -> defaultdict[_T1, dict[_T2, _T3]]:
     """Return a new defaultdict of dicts."""
     return defaultdict(dict)
 
 
+def _components_by_entity_from(
+    by_type: defaultdict[_ComponentKey[object], dict[Entity, Any]]
+) -> defaultdict[Entity, dict[_ComponentKey[object], Any]]:
+    """Return the component lookup table from the components sparse-set."""
+    by_entity: defaultdict[Entity, dict[_ComponentKey[object], Any]] = defaultdict(dict)
+    for component_key, components in by_type.items():
+        for entity, component in components.items():
+            by_entity[entity][component_key] = component
+    return by_entity
+
+
+def _tags_by_key_from_tags_by_entity(by_entity: defaultdict[Entity, set[object]]) -> defaultdict[object, set[Entity]]:
+    """Return the tag lookup table from the tags sparse-set."""
+    tags_by_key = defaultdict(set)
+    for entity, tags in by_entity.items():
+        for tag in tags:
+            tags_by_key[tag].add(entity)
+    return tags_by_key
+
+
+def _relations_lookup_from(
+    tags_by_entity: defaultdict[Entity, defaultdict[object, set[Entity]]],
+    components_by_entity: defaultdict[Entity, defaultdict[_ComponentKey[object], dict[Entity, Any]]],
+) -> defaultdict[tuple[Any, Entity | EllipsisType] | tuple[Entity | EllipsisType, Any, None], set[Entity]]:
+    """Return the relation lookup table from the relations sparse-sets."""
+    relations_lookup: defaultdict[
+        tuple[Any, Entity | EllipsisType] | tuple[Entity | EllipsisType, Any, None], set[Entity]
+    ] = defaultdict(set)
+    for entity, tags in tags_by_entity.items():
+        for tag, targets in tags.items():
+            for target in targets:
+                relations_lookup[(tag, ...)].add(target)
+                relations_lookup[(tag, entity)].add(target)
+                relations_lookup[(target, tag, None)].add(entity)
+                relations_lookup[(..., tag, None)].add(entity)
+    for entity, components in components_by_entity.items():
+        for component_key, target_components in components.items():
+            for target in target_components:
+                relations_lookup[(component_key, ...)].add(target)
+                relations_lookup[(component_key, entity)].add(target)
+                relations_lookup[(target, component_key, None)].add(entity)
+                relations_lookup[(..., component_key, None)].add(entity)
+
+    return relations_lookup
+
+
+@attrs.define(eq=False)
 class World:
     """A container for entities and components."""
 
-    def __init__(self) -> None:
-        """Initialize a new world."""
-        self._components_by_type: defaultdict[_ComponentKey[object], dict[Entity, Any]] = defaultdict(dict)
-        """Query table entity components.
+    _components_by_entity: defaultdict[Entity, dict[_ComponentKey[object], Any]] = attrs.field(
+        init=False, factory=lambda: defaultdict(dict)
+    )
+    """Random access entity components.
 
-        dict[ComponentKey][Entity] = component_instance
-        """
-        self._components_by_entity: defaultdict[Entity, set[_ComponentKey[object]]] = defaultdict(set)
-        """Random access entity components.
+    dict[Entity][ComponentKey] = component_instance
+    """
+    _components_by_type: defaultdict[_ComponentKey[object], dict[Entity, Any]] = attrs.field(
+        init=False, factory=lambda: defaultdict(dict)
+    )
+    """Query table entity components.
 
-        dict[Entity] = {component_keys_owned_by_entity}
-        """
+    dict[ComponentKey] = {entities_with_component}
+    """
 
-        self._tags_by_key: defaultdict[object, set[Entity]] = defaultdict(set)
-        """Query table entity tags.
+    _tags_by_key: defaultdict[object, set[Entity]] = attrs.field(init=False, factory=lambda: defaultdict(set))
+    """Query table entity tags.
 
-        dict[tag] = {all_entities_with_tag}
-        """
-        self._tags_by_entity: defaultdict[Entity, set[Any]] = defaultdict(set)
-        """Random access entity tags.
-
-        dict[Entity] = {all_tags_for_entity}
-        """
+    dict[tag] = {all_entities_with_tag}
+    """
+    _tags_by_entity: defaultdict[Entity, set[Any]] = attrs.field(init=False, factory=lambda: defaultdict(set))
+    """Random access entity tags.
 
-        self._relation_tags_by_entity: defaultdict[Entity, defaultdict[object, set[Entity]]] = defaultdict(
-            _defaultdict_of_set
-        )
-        """Random access tag multi-relations.
+    dict[Entity] = {all_tags_for_entity}
+    """
 
-        dict[entity][tag] = {target_entities}
-        """
-        self._relation_components_by_entity: defaultdict[
-            Entity, defaultdict[_ComponentKey[object], dict[Entity, Any]]
-        ] = defaultdict(_defaultdict_of_dict)
-        """Random access relations owning components.
+    _relation_tags_by_entity: defaultdict[Entity, defaultdict[object, set[Entity]]] = attrs.field(
+        init=False, factory=lambda: defaultdict(_defaultdict_of_set)
+    )
+    """Random access tag multi-relations.
 
-        dict[entity][ComponentKey][target_entity] = component
-        """
-        self._relations_lookup: defaultdict[
-            tuple[Any, Entity | EllipsisType] | tuple[Entity | EllipsisType, Any, None], set[Entity]
-        ] = defaultdict(set)
-        """Relations query table.  Tags and components are mixed together.
+    dict[entity][tag] = {target_entities}
+    """
+    _relation_components_by_entity: defaultdict[
+        Entity, defaultdict[_ComponentKey[object], dict[Entity, Any]]
+    ] = attrs.field(init=False, factory=lambda: defaultdict(_defaultdict_of_dict))
+    """Random access relations owning components.
 
-        Tag:
-            dict[(tag, this_entity)] = {target_entities_for_entity}
-            dict[(tag, None)] = {target_entities_for_tag}
-            dict[(target_entity, tag, None)] = {origin_entities_for_target}
-            dict[(None, tag, None)] = {all_origen_entities_for_tag}
-        Component:
-            dict[(ComponentKey, target_entity)] = {origin_entities}
-            dict[(ComponentKey, None)] = {all_origin_entities}
-            dict[(origin_entity, ComponentKey, None)] = {target_entities}
-            dict[(None, ComponentKey, None)] = {all_target_entities}
-        """
+    dict[entity][ComponentKey][target_entity] = component
+    """
+    _relations_lookup: defaultdict[
+        tuple[Any, Entity | EllipsisType] | tuple[Entity | EllipsisType, Any, None], set[Entity]
+    ] = attrs.field(init=False, factory=lambda: defaultdict(set))
+    """Relations query table.  Tags and components are mixed together.
+
+    ```
+    Tag:
+        dict[(tag, this_entity)] = {target_entities_for_entity}
+        dict[(tag, None)] = {target_entities_for_tag}
+        dict[(target_entity, tag, None)] = {origin_entities_for_target}
+        dict[(None, tag, None)] = {all_origen_entities_for_tag}
+    Component:
+        dict[(ComponentKey, target_entity)] = {origin_entities}
+        dict[(ComponentKey, None)] = {all_origin_entities}
+        dict[(origin_entity, ComponentKey, None)] = {target_entities}
+        dict[(None, ComponentKey, None)] = {all_target_entities}
+    ```
+    """
 
-        self._names_by_name: dict[object, Entity] = {}
-        """Name query table.
+    _names_by_name: dict[object, Entity] = attrs.field(init=False, factory=dict)
+    """Name query table.
 
-        dict[name] = named_entity
-        """
-        self._names_by_entity: dict[Entity, object] = {}
-        """Name lookup table.
+    dict[name] = named_entity
+    """
+    _names_by_entity: dict[Entity, object] = attrs.field(init=False, factory=dict)
+    """Name lookup table.
 
-        dict[Entity] = entities_name
-        """
+    dict[Entity] = entities_name
+    """
 
     @property
     def global_(self) -> Entity:
         """A unique globally accessible entity.
 
         This can be used to store globally accessible components in the world itself without any extra boilerplate.
         Otherwise this entity is not special and will show up with other entities in queries, etc.
@@ -819,19 +883,75 @@
         )
         return Entity(self, None)
 
     def __setstate__(self, state: dict[str, Any]) -> None:
         """Unpickle this object and handle state migration."""
         global_: Entity | None = state.pop("global_", None)  # Migrate from version <=1.2.0
 
-        self.__dict__.update(state)
+        # These attributes contain redundant data and will be removed
+        REDUNDANT_ATTRIBUTES = frozenset(
+            {
+                "_components_by_entity",  # <=3.4.0
+                "_tags_by_key",  # <=3.4.0
+                "_relations_lookup",  # <=3.4.0
+                "_names_by_entity",  # <=3.4.0
+            }
+        )
+        for ignored in REDUNDANT_ATTRIBUTES:
+            state.pop(ignored, None)
+
+        converter = tcod.ecs._converter._get_converter()
+        # Apply defaultdict types to unpickled dictionaries
+        self._components_by_type = converter.structure(
+            state.pop("_components_by_type"),
+            DefaultDict[Any, Dict[Any, Any]],
+        )
+        self._components_by_entity = _components_by_entity_from(self._components_by_type)
+
+        self._tags_by_entity = converter.structure(
+            state.pop("_tags_by_entity"),
+            DefaultDict[Any, Set[Any]],
+        )
+        self._tags_by_key = _tags_by_key_from_tags_by_entity(self._tags_by_entity)
+
+        self._relation_tags_by_entity = converter.structure(
+            state.pop("_relation_tags_by_entity"),
+            DefaultDict[Any, DefaultDict[Any, Set[Any]]],
+        )
+        self._relation_components_by_entity = converter.structure(
+            state.pop("_relation_components_by_entity"),
+            DefaultDict[Any, DefaultDict[Any, Dict[Any, Any]]],
+        )
+        self._relations_lookup = _relations_lookup_from(
+            self._relation_tags_by_entity, self._relation_components_by_entity
+        )
+
+        self._names_by_name = state.pop("_names_by_name")
+        self._names_by_entity = {entity: name for name, entity in self._names_by_name.items()}
 
         if global_ is not None and global_.uid is not None:  # Migrate from version <=1.2.0
             global_._force_remap(None)
 
+        if state:
+            warnings.warn(f"These attributes were not unpacked {state.keys()}", RuntimeWarning, stacklevel=1)
+
+    def __getstate__(self) -> dict[str, Any]:
+        """Pickle this object."""
+        converter = tcod.ecs._converter._get_converter()
+        # Replace defaultdict types with plain dict when saving
+        return {
+            "_components_by_type": converter.structure(self._components_by_type, Dict[Any, Dict[Any, Any]]),
+            "_tags_by_entity": converter.structure(self._tags_by_entity, Dict[Any, Any]),
+            "_relation_tags_by_entity": converter.structure(self._relation_tags_by_entity, Dict[Any, Dict[Any, Any]]),
+            "_relation_components_by_entity": converter.structure(
+                self._relation_components_by_entity, Dict[Any, Dict[Any, Any]]
+            ),
+            "_names_by_name": self._names_by_name,
+        }
+
     def __getitem__(self, uid: object) -> Entity:
         """Return an entity associated with a unique id.
 
         Example::
 
             >>> world = World()
             >>> foo = world["foo"]  # Referencing a new entity returns a new empty entity
```

### Comparing `tcod_ecs-3.4.0/PKG-INFO` & `tcod_ecs-3.5.0/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 Metadata-Version: 2.1
 Name: tcod-ecs
-Version: 3.4.0
+Version: 3.5.0
 Summary: A type-hinted Entity Component System based on Python dictionaries and sets.
 Author-email: Kyle Benesch <4b796c65+github@gmail.com>
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Typing :: Typed
 Requires-Dist: typing-extensions >=4.4.0
+Requires-Dist: attrs>=23.1.0
+Requires-Dist: cattrs>=23.1.2
 Requires-Dist: attrs >=22.2.0 ; extra == "test"
 Requires-Dist: pytest >=7.2.0 ; extra == "test"
 Requires-Dist: pytest-cov >=4.0.0 ; extra == "test"
 Requires-Dist: pytest-benchmark >=4.0.0 ; extra == "test"
 Requires-Dist: mypy >=1.1.1 ; extra == "test"
 Project-URL: Changelog, https://github.com/HexDecimal/python-tcod-ecs/blob/main/CHANGELOG.md
 Project-URL: Documentation, https://python-tcod-ecs.readthedocs.io
@@ -27,28 +29,28 @@
 # About
 
 [![PyPI](https://img.shields.io/pypi/v/tcod-ecs)](https://pypi.org/project/tcod-ecs/)
 [![PyPI - License](https://img.shields.io/pypi/l/tcod-ecs)](https://github.com/HexDecimal/python-tcod-ecs/blob/main/LICENSE)
 [![Documentation Status](https://readthedocs.org/projects/python-tcod-ecs/badge/?version=latest)](https://python-tcod-ecs.readthedocs.io)
 [![codecov](https://codecov.io/gh/HexDecimal/python-tcod-ecs/branch/main/graph/badge.svg?token=4Ak5QpTLZB)](https://codecov.io/gh/HexDecimal/python-tcod-ecs)
 
-This is an [Entity-component-system](https://en.wikipedia.org/wiki/Entity_component_system) implemented in Python.
+`tcod-ecs` is a [Sparse-set](https://skypjack.github.io/2020-08-02-ecs-baf-part-9/) [Entity-component-system](https://en.wikipedia.org/wiki/Entity_component_system) implemented using Python's `dict` and `set` types.
 See the [ECS FAQ](https://github.com/SanderMertens/ecs-faq) for more info.
 
 This implementation focuses on type-hinting, organization, and is designed to work well with Python.
 The following features are currently implemented:
 
-- Entities can have store components which are instances of any Python object. Components are looked up by their type.
-- Entities can have one instance of a type, or multiple instances of a type with a string or other hashable to differentiate them.
-- Components can be registered as abstract, allowing a base type to hold subclasses of that component.
-- Entity tags are distinct from components, tags are any hashable Python object rather than empty class.
+- Entities can store components which are instances of any Python object. Components are looked up by their type.
+- Entities can have one instance of a type, or multiple instances of a type using a hashable tag to differentiate them.
 - Entity relationships are supported, either as many-to-many or many-to-one relationships.
-- ECS Queries can be made to fetch entities having a combination of components/tags/relations or the absence of such.
+- ECS Queries can be made to fetch entities having a combination of components/tags/relations or excluding such.
+- The ECS World object can be serialized with Python's pickle module for easy storage.
 
 A lightweight version which implements only the entity-component framework exists called [tcod-ec](https://pypi.org/project/tcod-ec/).
+`tcod-ec` was geared towards a dynamic-typed-dict style of syntax and is missing a lot of important features such as queries and named components.
 
 # Installation
 
 Use pip to install this library:
 ```
 pip install tcod-ecs
 ```
@@ -64,17 +66,17 @@
 >>> import tcod.ecs
 >>> world = tcod.ecs.World()  # New empty world
 
 ```
 
 ## Entity
 
-Each Entity is identified by its unique id (`uid`) which can be any hashable object and the `world` it belongs to.
-New unique entities can be created with `World.new_entity` which uses a new `object()` as the `uid`.
-An entity always knows about its assigned world.
+Each Entity is identified by its unique id (`uid`) which can be any hashable object combined with the `world` it belongs.
+New unique entities can be created with `World.new_entity` which uses a new `object()` as the `uid`, this guarantees uniqueness which is not always desireable.
+An entity always knows about its assigned world, which can be access with the `Entity.world` property from any Entity instance.
 Worlds only know about their entities once the entity is assigned a name, component, tag, or relation.
 
 ```py
 >>> entity = world.new_entity()  # Creates a unique entity using `object()` as the uid
 >>> entity
 <Entity(uid=object at ...)>
 >>> entity.world is world  # Worlds can always be accessed from their entity
@@ -82,32 +84,41 @@
 >>> world[entity.uid] is entity  # Entities with the same world/uid are compared using `is`
 True
 
 # Reference an entity with the given uid, can be any hashable object:
 >>> entity = world["MyEntity"]
 >>> entity
 <Entity(uid='MyEntity')>
->>> world["MyEntity"] is entity
+>>> world["MyEntity"] is entity  # Matching entities ALWAYS share a single identity
 True
 
 ```
 
 Use `World.new_entity` to create unique entities and use `World[x]` to reference a global entity or relation with an id.
+`World[None]` is recommend for use as a global entity when you want to store components in the world itself.
+
+Do not save the `uid`'s of entities to be used later with `World[uid]`, this process is slower than holding onto the Entity instance.
 
 ## Serialization
 
-Worlds are normal Python objects and can be pickled as long as all stored components can be pickled.
+Worlds are normal Python objects and can be pickled as long as all stored components are pickleable.
 
 ```py
 >>> import pickle
 >>> pickled_data: bytes = pickle.dumps(world)
 >>> world = pickle.loads(pickled_data)
 
 ```
 
+Stability is a priority but changes may still break older saves.
+Backwards compatibility is not a priority, pickled worlds should not be unpickled with an older version of the library.
+This project follows [Semantic Versioning](https://semver.org/), major version increments will break the API, the save format or both, minor version increments may break backwards compatibility.
+Check the [changelog](https://github.com/HexDecimal/python-tcod-ecs/blob/main/CHANGELOG.md) to be aware of format changes and breaks.
+There should always be a transition period before a format break, so keeping up with the latest version is a good idea.
+
 ## Components
 
 Components are instances of any Python type.
 These can be accessed, assigned, or removed from entities via the dict-like `Entity.components` attribute.
 The type is used as the key to access the component.
 The types used can be custom classes or standard Python types.
 
@@ -119,15 +130,15 @@
 42
 >>> int in entity.components
 True
 >>> del entity.components[int]
 >>> entity.components[int]  # Missing keys raise KeyError
 Traceback (most recent call last):
   ...
-KeyError: <Entity...>
+KeyError: <class 'int'>
 >>> entity.components.get(int, "default")  # Test keys with `.get()` like a dictionary
 'default'
 >>> @attrs.define
 ... class Vector2:
 ...     x: int = 0
 ...     y: int = 0
 >>> entity.components[Vector2] = Vector2(1, 2)
@@ -158,15 +169,15 @@
 
 ```
 
 ## Named Components
 
 Only one component can be assigned unless that component is given a unique name.
 You can name components with the key syntax `(name, type)` when assigning components.
-Names are not limited to strings, and can be any hashable or frozen object.
+Names are not limited to strings, they are a tag equivalent and can be any hashable or frozen object.
 The syntax `[type]` and `[(name, type)]` can be used interchangeably in all places accepting a component key.
 Queries on components access named components with the same syntax and must use names explicitly.
 
 ```py
 >>> entity = world.new_entity()
 >>> entity.components[Vector2] = Vector2(0, 0)
 >>> entity.components[("velocity", Vector2)] = Vector2(1, 1)
@@ -216,19 +227,21 @@
 >>> set(world.Q.all_of(tags=["player"])) == {entity}
 True
 
 ```
 
 ## Relations
 
-Use `Entity.relation_components[component_key][target] = component` to associate a relation with data.
+Use `Entity.relation_components[component_key][target] = component` to associate a target entity with a component.
 Use `Entity.relation_tag[tag] = target` to associate a tag exclusively with a target entity.
 Use `Entity.relation_tags_many[tag].add(target)` to associate a tag with multiple targets.
-Tags and relations share the same space then queried, so tags can not be in the format of a component key.
-Relations are unidirectional.
+
+Relation queries are a little more complex than other queries.
+Relation tags and relation components share the same space then queried, so 'normal' tags should not be in the format of a component key.
+Relations are unidirectional, but you can query either end of a relation.
 
 ```py
 >>> @attrs.define
 ... class OrbitOf:  # OrbitOf component
 ...     dist: int
 >>> LandedOn = "LandedOn"  # LandedOn tag
 >>> star = world.new_entity()
@@ -251,7 +264,17 @@
 >>> set(world.Q.all_of(relations=[(LandedOn, ...)])) == {ship, moon_rock, player}
 True
 >>> set(world.Q.all_of(relations=[(LandedOn, ...)]).none_of(relations=[(LandedOn, moon)])) == {player}
 True
 
 ```
 
+You can use the following table to help with constructing relation queries.
+`tag` is a component key if you are querying for a component relation.
+
+| Includes                                                              | Syntax |
+| --------------------------------------------------------------------- | :----: |
+| Entities with a relation tag to the given target                      | `(tag, target_entity)` |
+| Entities with a relation tag to any target                            | `(tag, ...)` |
+| Entities which are a relation target of a given entity                | `(origin_entity, tag, None)` |
+| Entities which are a target of any entity with the given relation tag | `(..., tag, None)` |
+
```

