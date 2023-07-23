# Comparing `tmp/nuad-0.4.2.tar.gz` & `tmp/nuad-0.4.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nuad-0.4.2.tar", last modified: Mon May 22 19:29:35 2023, max compression
+gzip compressed data, was "nuad-0.4.3.tar", last modified: Sun Jul 23 17:38:13 2023, max compression
```

## Comparing `nuad-0.4.2.tar` & `nuad-0.4.3.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-22 19:29:35.053551 nuad-0.4.2/
--rw-r--r--   0 runner    (1001) docker     (122)     1091 2023-05-22 19:29:26.000000 nuad-0.4.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (122)       93 2023-05-22 19:29:26.000000 nuad-0.4.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (122)    27499 2023-05-22 19:29:35.053551 nuad-0.4.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (122)    26981 2023-05-22 19:29:26.000000 nuad-0.4.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-22 19:29:35.049551 nuad-0.4.2/nuad/
--rw-r--r--   0 runner    (1001) docker     (122)      150 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/__init__.py
--rw-r--r--   0 runner    (1001) docker     (122)       89 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/__version__.py
--rw-r--r--   0 runner    (1001) docker     (122)   375716 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/constraints.py
--rw-r--r--   0 runner    (1001) docker     (122)     1966 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/json_noindent_serializer.py
--rw-r--r--   0 runner    (1001) docker     (122)     8296 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/modifications.py
--rw-r--r--   0 runner    (1001) docker     (122)    56332 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/np.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-22 19:29:35.053551 nuad-0.4.2/nuad/nupack_viennaRNA_parameter_files/
--rw-r--r--   0 runner    (1001) docker     (122)   251648 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/nupack_viennaRNA_parameter_files/dna_mathews1999.par
--rw-r--r--   0 runner    (1001) docker     (122)   380873 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/nupack_viennaRNA_parameter_files/dna_mathews2004.par
--rw-r--r--   0 runner    (1001) docker     (122)   115196 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/search.py
--rw-r--r--   0 runner    (1001) docker     (122)     6135 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/stopwatch.py
--rw-r--r--   0 runner    (1001) docker     (122)    31830 2023-05-22 19:29:26.000000 nuad-0.4.2/nuad/vienna_nupack.py
-drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-05-22 19:29:35.053551 nuad-0.4.2/nuad.egg-info/
--rw-r--r--   0 runner    (1001) docker     (122)    27499 2023-05-22 19:29:34.000000 nuad-0.4.2/nuad.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (122)      488 2023-05-22 19:29:35.000000 nuad-0.4.2/nuad.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (122)        1 2023-05-22 19:29:34.000000 nuad-0.4.2/nuad.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (122)      137 2023-05-22 19:29:34.000000 nuad-0.4.2/nuad.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (122)        5 2023-05-22 19:29:34.000000 nuad-0.4.2/nuad.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (122)      134 2023-05-22 19:29:26.000000 nuad-0.4.2/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (122)       38 2023-05-22 19:29:35.053551 nuad-0.4.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (122)     2023 2023-05-22 19:29:26.000000 nuad-0.4.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 17:38:13.582938 nuad-0.4.3/
+-rw-r--r--   0 runner    (1001) docker     (122)     1091 2023-07-23 17:38:00.000000 nuad-0.4.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (122)       93 2023-07-23 17:38:00.000000 nuad-0.4.3/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (122)    27612 2023-07-23 17:38:13.582938 nuad-0.4.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (122)    27094 2023-07-23 17:38:00.000000 nuad-0.4.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 17:38:13.578938 nuad-0.4.3/nuad/
+-rw-r--r--   0 runner    (1001) docker     (122)      150 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (122)       89 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/__version__.py
+-rw-r--r--   0 runner    (1001) docker     (122)   371913 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/constraints.py
+-rw-r--r--   0 runner    (1001) docker     (122)     1966 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/json_noindent_serializer.py
+-rw-r--r--   0 runner    (1001) docker     (122)     8296 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/modifications.py
+-rw-r--r--   0 runner    (1001) docker     (122)    56332 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/np.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 17:38:13.582938 nuad-0.4.3/nuad/nupack_viennaRNA_parameter_files/
+-rw-r--r--   0 runner    (1001) docker     (122)   251648 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/nupack_viennaRNA_parameter_files/dna_mathews1999.par
+-rw-r--r--   0 runner    (1001) docker     (122)   380873 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/nupack_viennaRNA_parameter_files/dna_mathews2004.par
+-rw-r--r--   0 runner    (1001) docker     (122)   115198 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/search.py
+-rw-r--r--   0 runner    (1001) docker     (122)     6135 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/stopwatch.py
+-rw-r--r--   0 runner    (1001) docker     (122)    31830 2023-07-23 17:38:00.000000 nuad-0.4.3/nuad/vienna_nupack.py
+drwxr-xr-x   0 runner    (1001) docker     (122)        0 2023-07-23 17:38:13.578938 nuad-0.4.3/nuad.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (122)    27612 2023-07-23 17:38:13.000000 nuad-0.4.3/nuad.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (122)      488 2023-07-23 17:38:13.000000 nuad-0.4.3/nuad.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        1 2023-07-23 17:38:13.000000 nuad-0.4.3/nuad.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (122)      137 2023-07-23 17:38:13.000000 nuad-0.4.3/nuad.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (122)        5 2023-07-23 17:38:13.000000 nuad-0.4.3/nuad.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (122)      134 2023-07-23 17:38:00.000000 nuad-0.4.3/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (122)       38 2023-07-23 17:38:13.582938 nuad-0.4.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (122)     2023 2023-07-23 17:38:00.000000 nuad-0.4.3/setup.py
```

### Comparing `nuad-0.4.2/LICENSE` & `nuad-0.4.3/LICENSE`

 * *Files identical despite different names*

### Comparing `nuad-0.4.2/PKG-INFO` & `nuad-0.4.3/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,20 +1,7 @@
-Metadata-Version: 2.1
-Name: nuad
-Version: 0.4.2
-Summary: nuad stands for "NUcleic Acid Designer". Enables one to specify constraints on a DNA (or RNA) nanostructure made from synthetic DNA/RNA and then attempts to find concrete DNA sequences that satisfy the constraints.
-Home-page: https://github.com/UC-Davis-molecular-computing/nuad
-Author: David Doty
-Author-email: doty@ucdavis.edu
-License: MIT
-Platform: UNKNOWN
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown; variant=GFM
-License-File: LICENSE
-
 # nuad
 
 nuad is a Python library that enables one to specify constraints on a DNA (or RNA) nanostructure made from synthetic DNA/RNA and then attempts to find concrete DNA sequences that satisfy the constraints.
 
 Note: If you are reading this on the PyPI website, many links below won't work. They are relative links intended to be read on the [GitHub README page](https://github.com/UC-Davis-molecular-computing/nuad/tree/main#readme).
 
 ## Table of contents
@@ -147,17 +134,17 @@
 - `Strand`: A `Strand` contains an ordered list `domains` of `Domain`'s, together with an identification of which `Domain`'s are starred in this `Strand`, the latter specified as a set `starred_domain_indices` of indices (starting at 0) into the list `domains`. For example, the `Strand` consisting of `Domain`'s `a`, `b*`, `c`, `b`, `d*`, in that order, would have `domains = [a, b, c, b, d]` and `starred_domain_indices = {1, 4}`.
 
 - `Design`: This describes the whole system. Generally you will have one `Design`, which is composed of a list of `Strand`'s.
 
 - `Constraint`: There are several kinds of constraint objects. Not all of them are related in the type hierarchy. 
 
     - **"hard" constraints on Domain sequences:** 
-    These are the strictest constraints, which do not even allow certain `Domain` sequences to be considered. They are applied by a `DomainPool` before allowing a sequence to be returned from `DomainPool.generate_sequence()`. These are of two types: `NumpyConstraint` and `SequenceConstraint`. Each of them indicates whether a DNA sequence is allowed or not; for instance a constraint forbidding 4 G's in a row would permit AGGGTT but forbid AGGGGT. The difference between them is that a `NumpyConstraint` operates on many DNA sequences at a time, representing them as a 2D numpy byte array (e.g., a 1000 &times; 15 array of bytes to represent 1000 sequences, each of length 15), and for operations that numpy is suited for, can evaluate these constraints *much* faster than the equivalent Python code that would loop over each sequence individually. However, if you have a constraint that is not straightforward to express using numpy operations, then a `SequenceConstraint` can be used to express it in plain Python. A `SequenceConstraint` is simply a type alias for a Python function that takes a string as input representing the DNA sequence and returns a Boolean indicating whether the sequence satisfies the constraint. Due to the speed of numpy, it is advised to use `SequenceConstraint`'s only if necessary because it cannot be expressed as a `NumpyConstraint`.
+    These are the strictest constraints, which do not even allow certain `Domain` sequences to be considered, known as "filters". They are applied by a `DomainPool` before allowing a sequence to be returned from `DomainPool.generate_sequence()`, which is the method called whenever the search algorithm wants to try a new DNA sequence for a `Domain`. These are of two types of filters: `NumpyFilter` and `SequenceFilter`. Each of them indicates whether a DNA sequence is allowed or not; for instance a filter forbidding 4 G's in a row would permit AGGGTT but forbid AGGGGT. The difference between them is that a `NumpyFilter` operates on many DNA sequences at a time, representing them as a 2D numpy byte array (e.g., a 1000 &times; 15 array of bytes to represent 1000 sequences, each of length 15), and for operations that numpy is suited for, can evaluate these filters *much* faster than the equivalent Python code that would loop over each sequence individually. However, if you have a filter that is not straightforward to express using numpy operations, then a `SequenceFilter` can be used to express it in plain Python. A `SequenceFilter` is simply a type alias for a Python function that takes a string as input representing the DNA sequence and returns a Boolean indicating whether the sequence satisfies the filter. Due to the speed of numpy, it is advised to use `SequenceFilter`'s only if necessary because it cannot be expressed as a `NumpyFilter`.
 
-    - **"soft" constraints:**  All other constraints are subclasses of the abstract superclass `Constraint`. These constrains are "softer": sequences violating the constraints are allowed to be assigned to `Domain`'s. The sequence design algorithm steadily improves the design by changing sequences until all of these constraints are satisfied. The different subtypes of the base class `Constraint` correspond to different parts of the `Design` that are being evaluated by the `Constraint`. The types are:
+    - **"soft" constraints:**  All other constraints are subclasses of the abstract superclass `Constraint`. These constrains are "softer" than filters as described above: sequences violating the constraints are allowed to be assigned to `Domain`'s. The sequence design algorithm steadily improves the design by changing sequences until all of these constraints are satisfied. The different subtypes of the base class `Constraint` correspond to different parts of the `Design` that are being evaluated by the `Constraint`. The types are:
 
         - `SingularConstraint`: This is an abstract superclass of the following concrete subclasses. The difference with the other abstract superclass `BulkConstraint` is explained in `BulkConstraint` below.
         
             - `DomainConstraint`: This only looks at a single `Domain`. In practice this is not used much, since there's not much information in a `Domain` other than its DNA sequence, so a `SequenceConstraint` or `NumpyConstraint` typically would already have filtered out any DNA sequence not satisfying such a constraint.
 
             - `StrandConstraint`: This evaluates a whole `Strand`. A common example is that NUPACK's `pfunc` should indicate a complex free energy above a certain threshold, indicating the `Strand` has little secondary structure. This example constraint is available in the library by calling [nupack_strand_complex_free_energy_constraint](https://nuad.readthedocs.io/en/latest/#constraints.nupack_strand_complex_free_energy_constraint).
 
@@ -184,15 +171,15 @@
     The search algorithm evaluates the constraints, and for each violated constraint, it turns the `excess` value into a "score" by first passing it through the "score transfer function", which by default squares the value, and then multiplies by the value `Constraint.weight` (by default 1). The goal of the search is to minimize the sum of scores across all violated `Constraint`'s. The reason that the score is squared is that this leads the search algorithm to (slightly) favor reducing the excess of constraint violations that are "more in excess", i.e., it would reduce the total score more to reduce an excess from 4 to 3 (reducing the score from 4<sup>2</sup>=16 to 3<sup>2</sup>=9, a reduction of 16-9=7) than to reduce an excess from 2 to 1 (which reduces 2<sup>2</sup>=4 to 1<sup>2</sup>=1, a reduction of only 4-1=3).
 
     The full search algorithm is described in the [API documentation for the function nuad.search.search_for_sequences](https://nuad.readthedocs.io/en/latest/#search.search_for_sequences).
 
 
 ## Constraint evaluations must be pure functions of their inputs
 
-For all constraints, it is critical that the `evaluate` or `evaluate_bulk` functions be *pure* functions of their inputs: the return value should depend only on the parameters passed to the function. For example, a `StrandPairConstraint` takes two strands as input, and its `(excess, summary)` return values should depend *only* on those two strands. Similarly, a `StrandsConstraint`, whose `evaluate_bulk` function takes a list of strands as input, should return a list of tuples, where each tuple represents a violation of a strand that depends only on that strand. This is required because nuad does an optimization in which constraints are only evaluated if they depend on parts of the design that contain the domain(s) that changed in the current iteration.
+For all constraints, it is critical that the `evaluate` or `evaluate_bulk` functions be *pure* functions of their inputs: the return value should depend only on the parameters passed to the function. For example, a `StrandPairConstraint` takes two strands as input, and its `Result` return values should depend *only* on those two strands. Similarly, a `StrandsConstraint`, whose `evaluate_bulk` function takes a list of strands as input, should return a list of tuples, where each tuple represents a violation of a strand that depends only on that strand. This is required because nuad does an optimization in which constraints are only evaluated if they depend on parts of the design that contain the domain(s) that changed in the current iteration.
 
 For example, suppose there are 100 strands, but only 3 strands contain the domain `x`, and `x` is the domain whose DNA sequence is changed in the current search iteration. Then each `StrandConstraint` `s` will be evaluated only on those 3 strands, on the assumption that the other 97 strands would have the same output of the function `s.evaluate` as before. 
 
 In the case of `evaluate_bulk`, the constraint is even stronger. `evaluate_bulk` takes a list of objects as input and returns of list of the same size. The `i`'th element of the returned list should depend only on the `i`'th element of the input list. This is because a similar optimization is done as above. For example, if the changed domain appears in only 3 strands out of 100, a `StrandsConstraint` will pass in only those 3 strands as input to `evaluate_bulk`, not the full list of 100 strands, on the assumption that the other 97 strands would be processed the same by the `evaluate_bulk` function.
 
 ## Examples
 Some example scripts can be found in the [examples/](examples/) subfolder.
@@ -239,9 +226,7 @@
 
 4. Web applications that use the software in source form or binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in online documentation provided with the web application.
 
 Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote derivative works without specific prior written permission.
 
 ### Disclaimer
 This software is provided by the copyright holders and contributors "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed.  In no event shall the copyright holder or contributors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
-
-
```

### Comparing `nuad-0.4.2/README.md` & `nuad-0.4.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,20 @@
+Metadata-Version: 2.1
+Name: nuad
+Version: 0.4.3
+Summary: nuad stands for "NUcleic Acid Designer". Enables one to specify constraints on a DNA (or RNA) nanostructure made from synthetic DNA/RNA and then attempts to find concrete DNA sequences that satisfy the constraints.
+Home-page: https://github.com/UC-Davis-molecular-computing/nuad
+Author: David Doty
+Author-email: doty@ucdavis.edu
+License: MIT
+Platform: UNKNOWN
+Requires-Python: >=3.7
+Description-Content-Type: text/markdown; variant=GFM
+License-File: LICENSE
+
 # nuad
 
 nuad is a Python library that enables one to specify constraints on a DNA (or RNA) nanostructure made from synthetic DNA/RNA and then attempts to find concrete DNA sequences that satisfy the constraints.
 
 Note: If you are reading this on the PyPI website, many links below won't work. They are relative links intended to be read on the [GitHub README page](https://github.com/UC-Davis-molecular-computing/nuad/tree/main#readme).
 
 ## Table of contents
@@ -134,17 +147,17 @@
 - `Strand`: A `Strand` contains an ordered list `domains` of `Domain`'s, together with an identification of which `Domain`'s are starred in this `Strand`, the latter specified as a set `starred_domain_indices` of indices (starting at 0) into the list `domains`. For example, the `Strand` consisting of `Domain`'s `a`, `b*`, `c`, `b`, `d*`, in that order, would have `domains = [a, b, c, b, d]` and `starred_domain_indices = {1, 4}`.
 
 - `Design`: This describes the whole system. Generally you will have one `Design`, which is composed of a list of `Strand`'s.
 
 - `Constraint`: There are several kinds of constraint objects. Not all of them are related in the type hierarchy. 
 
     - **"hard" constraints on Domain sequences:** 
-    These are the strictest constraints, which do not even allow certain `Domain` sequences to be considered. They are applied by a `DomainPool` before allowing a sequence to be returned from `DomainPool.generate_sequence()`. These are of two types: `NumpyConstraint` and `SequenceConstraint`. Each of them indicates whether a DNA sequence is allowed or not; for instance a constraint forbidding 4 G's in a row would permit AGGGTT but forbid AGGGGT. The difference between them is that a `NumpyConstraint` operates on many DNA sequences at a time, representing them as a 2D numpy byte array (e.g., a 1000 &times; 15 array of bytes to represent 1000 sequences, each of length 15), and for operations that numpy is suited for, can evaluate these constraints *much* faster than the equivalent Python code that would loop over each sequence individually. However, if you have a constraint that is not straightforward to express using numpy operations, then a `SequenceConstraint` can be used to express it in plain Python. A `SequenceConstraint` is simply a type alias for a Python function that takes a string as input representing the DNA sequence and returns a Boolean indicating whether the sequence satisfies the constraint. Due to the speed of numpy, it is advised to use `SequenceConstraint`'s only if necessary because it cannot be expressed as a `NumpyConstraint`.
+    These are the strictest constraints, which do not even allow certain `Domain` sequences to be considered, known as "filters". They are applied by a `DomainPool` before allowing a sequence to be returned from `DomainPool.generate_sequence()`, which is the method called whenever the search algorithm wants to try a new DNA sequence for a `Domain`. These are of two types of filters: `NumpyFilter` and `SequenceFilter`. Each of them indicates whether a DNA sequence is allowed or not; for instance a filter forbidding 4 G's in a row would permit AGGGTT but forbid AGGGGT. The difference between them is that a `NumpyFilter` operates on many DNA sequences at a time, representing them as a 2D numpy byte array (e.g., a 1000 &times; 15 array of bytes to represent 1000 sequences, each of length 15), and for operations that numpy is suited for, can evaluate these filters *much* faster than the equivalent Python code that would loop over each sequence individually. However, if you have a filter that is not straightforward to express using numpy operations, then a `SequenceFilter` can be used to express it in plain Python. A `SequenceFilter` is simply a type alias for a Python function that takes a string as input representing the DNA sequence and returns a Boolean indicating whether the sequence satisfies the filter. Due to the speed of numpy, it is advised to use `SequenceFilter`'s only if necessary because it cannot be expressed as a `NumpyFilter`.
 
-    - **"soft" constraints:**  All other constraints are subclasses of the abstract superclass `Constraint`. These constrains are "softer": sequences violating the constraints are allowed to be assigned to `Domain`'s. The sequence design algorithm steadily improves the design by changing sequences until all of these constraints are satisfied. The different subtypes of the base class `Constraint` correspond to different parts of the `Design` that are being evaluated by the `Constraint`. The types are:
+    - **"soft" constraints:**  All other constraints are subclasses of the abstract superclass `Constraint`. These constrains are "softer" than filters as described above: sequences violating the constraints are allowed to be assigned to `Domain`'s. The sequence design algorithm steadily improves the design by changing sequences until all of these constraints are satisfied. The different subtypes of the base class `Constraint` correspond to different parts of the `Design` that are being evaluated by the `Constraint`. The types are:
 
         - `SingularConstraint`: This is an abstract superclass of the following concrete subclasses. The difference with the other abstract superclass `BulkConstraint` is explained in `BulkConstraint` below.
         
             - `DomainConstraint`: This only looks at a single `Domain`. In practice this is not used much, since there's not much information in a `Domain` other than its DNA sequence, so a `SequenceConstraint` or `NumpyConstraint` typically would already have filtered out any DNA sequence not satisfying such a constraint.
 
             - `StrandConstraint`: This evaluates a whole `Strand`. A common example is that NUPACK's `pfunc` should indicate a complex free energy above a certain threshold, indicating the `Strand` has little secondary structure. This example constraint is available in the library by calling [nupack_strand_complex_free_energy_constraint](https://nuad.readthedocs.io/en/latest/#constraints.nupack_strand_complex_free_energy_constraint).
 
@@ -171,15 +184,15 @@
     The search algorithm evaluates the constraints, and for each violated constraint, it turns the `excess` value into a "score" by first passing it through the "score transfer function", which by default squares the value, and then multiplies by the value `Constraint.weight` (by default 1). The goal of the search is to minimize the sum of scores across all violated `Constraint`'s. The reason that the score is squared is that this leads the search algorithm to (slightly) favor reducing the excess of constraint violations that are "more in excess", i.e., it would reduce the total score more to reduce an excess from 4 to 3 (reducing the score from 4<sup>2</sup>=16 to 3<sup>2</sup>=9, a reduction of 16-9=7) than to reduce an excess from 2 to 1 (which reduces 2<sup>2</sup>=4 to 1<sup>2</sup>=1, a reduction of only 4-1=3).
 
     The full search algorithm is described in the [API documentation for the function nuad.search.search_for_sequences](https://nuad.readthedocs.io/en/latest/#search.search_for_sequences).
 
 
 ## Constraint evaluations must be pure functions of their inputs
 
-For all constraints, it is critical that the `evaluate` or `evaluate_bulk` functions be *pure* functions of their inputs: the return value should depend only on the parameters passed to the function. For example, a `StrandPairConstraint` takes two strands as input, and its `(excess, summary)` return values should depend *only* on those two strands. Similarly, a `StrandsConstraint`, whose `evaluate_bulk` function takes a list of strands as input, should return a list of tuples, where each tuple represents a violation of a strand that depends only on that strand. This is required because nuad does an optimization in which constraints are only evaluated if they depend on parts of the design that contain the domain(s) that changed in the current iteration.
+For all constraints, it is critical that the `evaluate` or `evaluate_bulk` functions be *pure* functions of their inputs: the return value should depend only on the parameters passed to the function. For example, a `StrandPairConstraint` takes two strands as input, and its `Result` return values should depend *only* on those two strands. Similarly, a `StrandsConstraint`, whose `evaluate_bulk` function takes a list of strands as input, should return a list of tuples, where each tuple represents a violation of a strand that depends only on that strand. This is required because nuad does an optimization in which constraints are only evaluated if they depend on parts of the design that contain the domain(s) that changed in the current iteration.
 
 For example, suppose there are 100 strands, but only 3 strands contain the domain `x`, and `x` is the domain whose DNA sequence is changed in the current search iteration. Then each `StrandConstraint` `s` will be evaluated only on those 3 strands, on the assumption that the other 97 strands would have the same output of the function `s.evaluate` as before. 
 
 In the case of `evaluate_bulk`, the constraint is even stronger. `evaluate_bulk` takes a list of objects as input and returns of list of the same size. The `i`'th element of the returned list should depend only on the `i`'th element of the input list. This is because a similar optimization is done as above. For example, if the changed domain appears in only 3 strands out of 100, a `StrandsConstraint` will pass in only those 3 strands as input to `evaluate_bulk`, not the full list of 100 strands, on the assumption that the other 97 strands would be processed the same by the `evaluate_bulk` function.
 
 ## Examples
 Some example scripts can be found in the [examples/](examples/) subfolder.
@@ -226,7 +239,9 @@
 
 4. Web applications that use the software in source form or binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in online documentation provided with the web application.
 
 Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote derivative works without specific prior written permission.
 
 ### Disclaimer
 This software is provided by the copyright holders and contributors "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed.  In no event shall the copyright holder or contributors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
+
+
```

### Comparing `nuad-0.4.2/nuad/constraints.py` & `nuad-0.4.3/nuad/constraints.py`

 * *Files 1% similar despite different names*

```diff
@@ -142,15 +142,14 @@
 
     p8634 = "p8634"
     """Variant of M13mp18 that is 8634 bases long. At the time of this writing, not listed as available
     from any biotech vender, but Tilibit will make it for you if you ask. 
     (https://www.tilibit.com/pages/contact-us)
     """
 
-
     def length(self) -> int:
         """
         :return: length of this variant of M13 (e.g., 7249 for variant :data:`M13Variant.p7249`)
         """
         if self is M13Variant.p7249:
             return 7249
         if self is M13Variant.p7560:
@@ -1317,15 +1316,14 @@
 
         raise AssertionError('should be unreachable')
 
     def _generate_random_sequences_passing_numpy_filters(self, rng: np.random.Generator,
                                                          num_to_generate: int) -> nn.DNASeqList:
         bases = self._bases_to_use()
         length = self.length
-        _length_threshold_numpy = math.floor(math.log(num_to_generate, 4))
         seqs = nn.DNASeqList(length=length, alphabet=bases, shuffle=True,
                              num_random_seqs=num_to_generate, rng=rng)
         seqs_passing_numpy_filters = self._apply_numpy_filters(seqs)
         self._log_numpy_generation(length, num_to_generate, len(seqs_passing_numpy_filters))
         return seqs_passing_numpy_filters
 
     @staticmethod
@@ -1409,19 +1407,16 @@
     @abstractmethod
     def individual_parts(self) -> Tuple[Domain, ...] | Tuple[Strand, ...]:
         # if Part represents a tuple, e.g., StrandPair or DomainPair, then returns tuple of
         # individual domains/strands
         pass
 
 
-DomainLabel = TypeVar('DomainLabel')
-
-
 @dataclass
-class Domain(Part, JSONSerializable, Generic[DomainLabel]):
+class Domain(Part, JSONSerializable):
     """
     Represents a contiguous substring of the DNA sequence of a :any:`Strand`, which is intended
     to be either single-stranded, or to bind fully to the Watson-Crick complement of the :any:`Domain`.
 
     If two domains are complementary, they are represented by the same :any:`Domain` object.
     They are distinguished only by whether the :any:`Strand` object containing them has the
     :any:`Domain` in its set :py:data:`Strand.starred_domains` or not.
@@ -1474,23 +1469,20 @@
     """
     Whether this :any:`Domain`'s DNA sequence is fixed, i.e., cannot be changed by the
     search algorithm :py:meth:`search.search_for_dna_sequences`.
 
     Note: If a domain is fixed then all of its subdomains must also be fixed.
     """
 
-    label: DomainLabel | None = None
+    label: str | None = None
     """
-    Optional generic "label" object to associate to this :any:`Domain`.
+    Optional "label" string to associate to this :any:`Domain`.
 
     Useful for associating extra information with the :any:`Domain` that will be serialized, for example,
-    for DNA sequence design. It must be an object (e.g., a dict or primitive type such as str or int)
-    that is naturally JSON serializable. (Calling
-    `json.dumps <https://docs.python.org/3/library/json.html#json.dumps>`_
-    on the object should succeed without having to specify a custom encoder.)
+    for DNA sequence design.
     """
 
     dependent: bool = False
     """
     Whether this :any:`Domain`'s DNA sequence is dependent on others. Usually this is not the case.
     However, domains can be subdivided hierarchically into a tree of domains by setting 
     :data:`Domain.subdomains` to describe the tree. In this case exactly
@@ -1520,15 +1512,15 @@
 
     parent: Domain | None = field(init=False, default=None)
     """Domain of which this is a subdomain. Note, this is not set manually, this is set by the library based 
     on the :data:`Domain.subdomains` of other domains in the same tree.
     """
 
     def __init__(self, name: str, pool: DomainPool | None = None, sequence: str | None = None,
-                 fixed: bool = False, label: DomainLabel | None = None, dependent: bool = False,
+                 fixed: bool = False, label: str | None = None, dependent: bool = False,
                  subdomains: List[Domain] | None = None, weight: float | None = None) -> None:
         if subdomains is None:
             subdomains = []
         self._name = name
         self._starred_name = name + '*'
         self._pool = pool
         self._sequence = sequence
@@ -1598,51 +1590,45 @@
                 dct[fixed_key] = True
         if self.label is not None:
             dct[label_key] = self.label
         return NoIndent(dct) if suppress_indent else dct
 
     @staticmethod
     def from_json_serializable(json_map: Dict[str, Any],
-                               pool_with_name: Dict[str, DomainPool] | None,
-                               label_decoder: Callable[[Any], DomainLabel] = lambda label: label) \
-            -> Domain[DomainLabel]:
+                               pool_with_name: Dict[str, DomainPool] | None) \
+            -> Domain:
         """
         :param json_map:
             JSON serializable object encoding this :any:`Domain`, as returned by
             :py:meth:`Domain.to_json_serializable`.
         :param pool_with_name:
             dict mapping name to :any:`DomainPool` with that name; required to rehydrate :any:`Domain`'s.
             If None, then a DomainPool with no constraints is created with the name and domain length
             found in the JSON.
-        :param label_decoder:
-            Function transforming object deserialized from JSON  (e.g, dict, list, string) into an object
-            of type DomainLabel.
         :return:
             :any:`Domain` represented by dict `json_map`, assuming it was created by
             :py:meth:`Domain.to_json_serializable`.
         """
         name: str = mandatory_field(Domain, json_map, name_key)
         sequence: str | None = json_map.get(sequence_key)
         fixed: bool = json_map.get(fixed_key, False)
 
-        label_json: Any = json_map.get(label_key)
-        label = label_decoder(label_json)
+        label: str = json_map.get(label_key)
 
         pool: DomainPool | None
         pool_name: str | None = json_map.get(domain_pool_name_key)
         if pool_name is not None:
             if pool_with_name is not None:
                 pool = pool_with_name[pool_name] if pool_with_name is not None else None
             else:
                 raise AssertionError()
         else:
             pool = None
 
-        domain: Domain[DomainLabel] = Domain(
-            name=name, sequence=sequence, fixed=fixed, pool=pool, label=label)
+        domain: Domain = Domain(name=name, sequence=sequence, fixed=fixed, pool=pool, label=label)
         return domain
 
     @property
     def name(self) -> str:
         """
         :return: :any:`DomainPool` of this :any:`Domain`
         """
@@ -2255,22 +2241,20 @@
         raise ValueError(f'field {field_name} in IDTFields cannot be None')
     if len(value) == 0:
         raise ValueError(f'field {field_name} in IDTFields cannot be empty')
 
 
 default_strand_group = 'default_strand_group'
 
-StrandLabel = TypeVar('StrandLabel')
-
 
 @dataclass
-class Strand(Part, JSONSerializable, Generic[StrandLabel, DomainLabel]):
+class Strand(Part, JSONSerializable):
     """Represents a DNA strand, made of several :any:`Domain`'s. """
 
-    domains: List[Domain[DomainLabel]]
+    domains: List[Domain]
     """The :any:`Domain`'s on this :any:`Strand`, in order from 5' end to 3' end."""
 
     starred_domain_indices: FrozenSet[int]
     """Set of positions of :any:`Domain`'s in :py:data:`Strand.domains`
     on this :any:`Strand` that are starred."""
 
     group: str
@@ -2319,31 +2303,28 @@
     (e.g., internal Cy3, /iCy3/ from IDT),
     then the index is that of the previous base, 
     e.g., to put a Cy3 between bases at indices 3 and 4, the index should be 3. 
     So for an internal modified base on a sequence of length n, the allowed indices are 0,...,n-1,
     and for an internal modification that goes between bases, the allowed indices are 0,...,n-2.
     """
 
-    label: StrandLabel | None = None
+    label: str | None = None
     """
-    Optional generic "label" object to associate to this :any:`Strand`.
+    Optional generic "label" string to associate to this :any:`Strand`.
 
     Useful for associating extra information with the :any:`Strand` that will be serialized, for example,
-    for DNA sequence design. It must be an object (e.g., a dict or primitive type such as str or int)
-    that is naturally JSON serializable. (Calling
-    `json.dumps <https://docs.python.org/3/library/json.html#json.dumps>`_
-    on the object should succeed without having to specify a custom encoder.)
+    for DNA sequence design.
     """
 
     def __init__(self,
-                 domains: Iterable[Domain[DomainLabel]] | None = None,
-                 starred_domain_indices: Iterable[int] | None = None,
+                 domains: Iterable[Domain] | None = None,
+                 starred_domain_indices: Iterable[int] = (),
                  group: str = default_strand_group,
                  name: str | None = None,
-                 label: StrandLabel | None = None,
+                 label: str | None = None,
                  idt: IDTFields | None = None,
                  ) -> None:
         """
         A :any:`Strand` can be created only by listing explicit :any:`Domain` objects
         via parameter `domains`. To specify a :any:`Strand` by giving domain *names*, see the method
         :meth:`Design.add_strand`.
 
@@ -2370,15 +2351,14 @@
         # Check that each base in the sequence is assigned by exactly one
         # independent subdomain.
         # for d in cast(List[Domain], domains):
         #     d._check_acyclic_subdomain_graph()  # noqa
         #     d._check_subdomain_graph_is_uniquely_assignable()  # noqa
 
         self.domains = list(domains)  # type: ignore
-        starred_domain_indices = [] if starred_domain_indices is None else starred_domain_indices
         self.starred_domain_indices = frozenset(starred_domain_indices)  # type: ignore
         self.label = label
         self.idt = idt
 
         # don't know why we have to do this, but we get a missing attribute error otherwise
         # https://stackoverflow.com/questions/70986725/python-dataclass-attribute-missing-when-using-explicit-init-constructor-and
         self.modifications_int = {}
@@ -2569,66 +2549,64 @@
                 mods_dict[f"{offset}"] = mod.id
             dct[nm.modifications_int_key] = NoIndent(mods_dict) if suppress_indent else mods_dict
 
         return dct
 
     @staticmethod
     def from_json_serializable(json_map: Dict[str, Any],
-                               domain_with_name: Dict[str, Domain[DomainLabel]],
-                               label_decoder: Callable[[Any], StrandLabel] = (lambda label: label),
-                               ) -> Strand[StrandLabel, DomainLabel]:
+                               domain_with_name: Dict[str, Domain],
+                               ) -> Strand:
         """
         :return:
             :any:`Strand` represented by dict `json_map`, assuming it was created by
             :py:meth:`Strand.to_json_serializable`.
         """
         name: str = mandatory_field(Strand, json_map, name_key)
         domain_names_json = mandatory_field(Strand, json_map, domain_names_key)
-        domains: List[Domain[DomainLabel]] = [domain_with_name[name] for name in domain_names_json]
+        domains: List[Domain] = [domain_with_name[name] for name in domain_names_json]
         starred_domain_indices = mandatory_field(Strand, json_map, starred_domain_indices_key)
 
         group = json_map.get(group_key, default_strand_group)
 
-        label_json = json_map.get(label_key)
-        label = label_decoder(label_json)
+        label: str = json_map.get(label_key)
 
         idt_json = json_map.get(idt_key)
         idt = None
         if idt_json is not None:
             idt = IDTFields.from_json_serializable(idt_json)
 
-        strand: Strand[StrandLabel, DomainLabel] = Strand(
+        strand: Strand = Strand(
             domains=domains, starred_domain_indices=starred_domain_indices,
             group=group, name=name, label=label, idt=idt)
         return strand
 
     def __repr__(self) -> str:
         return self.name
 
-    def unstarred_domains(self) -> List[Domain[DomainLabel]]:
+    def unstarred_domains(self) -> List[Domain]:
         """
         :return: list of unstarred :any:`Domain`'s in this :any:`Strand`, in order they appear in
                  :py:data:`Strand.domains`
         """
         return [domain for idx, domain in enumerate(self.domains) if idx not in self.starred_domain_indices]
 
-    def starred_domains(self) -> List[Domain[DomainLabel]]:
+    def starred_domains(self) -> List[Domain]:
         """
         :return: list of starred :any:`Domain`'s in this :any:`Strand`, in order they appear in
                  :py:data:`Strand.domains`
         """
         return [domain for idx, domain in enumerate(self.domains) if idx in self.starred_domain_indices]
 
-    def unstarred_domains_set(self) -> OrderedSet[Domain[DomainLabel]]:
+    def unstarred_domains_set(self) -> OrderedSet[Domain]:
         """
         :return: set of unstarred :any:`Domain`'s in this :any:`Strand`
         """
         return OrderedSet(self.unstarred_domains())
 
-    def starred_domains_set(self) -> OrderedSet[Domain[DomainLabel]]:
+    def starred_domains_set(self) -> OrderedSet[Domain]:
         """
         :return: set of starred :any:`Domain`'s in this :any:`Strand`
         """
         return OrderedSet(self.starred_domains())
 
     def sequence(self, delimiter: str = '') -> str:
         """
@@ -2665,15 +2643,15 @@
             start = end
 
     @property
     def fixed(self) -> bool:
         """True if every :any:`Domain` on this :any:`Strand` has a fixed DNA sequence."""
         return all(domain.fixed for domain in self.domains)
 
-    def unfixed_domains(self) -> Tuple[Domain[DomainLabel]]:
+    def unfixed_domains(self) -> Tuple[Domain]:
         """
         :return: all :any:`Domain`'s in this :any:`Strand` where :py:data:`Domain.fixed` is False
         """
         return tuple(domain for domain in self.domains if not domain.fixed)
 
     @property
     def name(self) -> str:
@@ -2820,15 +2798,15 @@
         for domain in self.domains:
             substring = seq[idx: idx + domain.get_length()]
             domain.set_fixed_sequence(substring)
             idx += domain.get_length()
 
 
 @dataclass
-class DomainPair(Part, Generic[DomainLabel], Iterable[Domain]):
+class DomainPair(Part, Iterable[Domain]):
     domain1: Domain
     domain2: Domain
 
     def __post_init__(self) -> None:
         # make this symmetric so make dict lookups work
         if self.domain1.name > self.domain2.name:
             self.domain1, self.domain2 = self.domain2, self.domain1
@@ -2851,21 +2829,21 @@
     def individual_parts(self) -> Tuple[Domain, ...]:
         return self.domain1, self.domain2
 
     @property
     def fixed(self) -> bool:
         return self.domain1.fixed and self.domain2.fixed
 
-    def __iter__(self) -> Iterator[Strand]:
+    def __iter__(self) -> Iterator[Domain]:
         yield self.domain1
         yield self.domain2
 
 
 @dataclass
-class StrandPair(Part, Generic[StrandLabel, DomainLabel], Iterable[Strand]):
+class StrandPair(Part, Iterable[Strand]):
     strand1: Strand
     strand2: Strand
 
     def __post_init__(self) -> None:
         # make this symmetric so make dict lookups work
         if self.strand1.name > self.strand2.name:
             self.strand1, self.strand2 = self.strand2, self.strand1
@@ -2894,15 +2872,15 @@
 
     def __iter__(self) -> Iterator[Strand]:
         yield self.strand1
         yield self.strand2
 
 
 @dataclass
-class Complex(Part, Generic[StrandLabel, DomainLabel], Iterable[Strand]):
+class Complex(Part, Iterable[Strand]):
     strands: Tuple[Strand, ...]
     """The strands in this complex."""
 
     def __init__(self, *args: Strand) -> None:
         """
         Creates a complex of strands given as arguments, e.g., ``Complex(strand1, strand2)`` creates
         a 2-strand complex.
@@ -3054,42 +3032,42 @@
         elif self is PlateType.wells384:
             return 96
         else:
             raise AssertionError('unreachable')
 
 
 @dataclass
-class Design(Generic[StrandLabel, DomainLabel], JSONSerializable):
+class Design(JSONSerializable):
     """
     Represents a complete design, i.e., a set of DNA :any:`Strand`'s with domains,
     and :any:`Constraint`'s on the sequences
     to assign to them via :py:meth:`search.search_for_dna_sequences`.
     """
 
     __hash__ = super(object).__hash__
     # This lets us use the design as a key for lookups requiring two designs to have distinct associations,
     # for example caching in a Constraint all pairs of domains in the Design, in case the Constraint
     # is reused for multiple designs in the same program.
 
-    strands: List[Strand[StrandLabel, DomainLabel]]
+    strands: List[Strand]
     """List of all :any:`Strand`'s in this :any:`Design`."""
 
     _domains_interned: Dict[str, Domain]
 
     #################################################
     # derived fields, so not specified in constructor
 
-    domains: List[Domain[DomainLabel]] = field(init=False)
+    domains: List[Domain] = field(init=False)
     """
     List of all :any:`Domain`'s in this :any:`Design`. (without repetitions)
 
     Computed from :py:data:`Design.strands`, so not specified in constructor.
     """
 
-    strands_by_group_name: Dict[str, List[Strand[StrandLabel, DomainLabel]]] = field(init=False)
+    strands_by_group_name: Dict[str, List[Strand]] = field(init=False)
     """
     Dict mapping each group name to a list of the :any:`Strand`'s in this :any:`Design` in the group.
 
     Computed from :py:data:`Design.strands`, so not specified in constructor.
     """
 
     domain_pools_to_domain_map: Dict[DomainPool, List[Domain]] = field(init=False)
@@ -3212,87 +3190,62 @@
             extension for filename (default: ``.sc``)
             Mutually exclusive with `filename`
         """
         content = self.to_json()
         sc.write_file_same_name_as_running_python_script(content, extension, directory, filename)
 
     @staticmethod
-    def from_design_file(filename: str,
-                         strand_label_decoder: Callable[[Any], StrandLabel] = lambda label: label,
-                         domain_label_decoder: Callable[[Any], DomainLabel] = lambda label: label,
-                         ) -> Design[StrandLabel, DomainLabel]:
+    def from_design_file(filename: str) -> Design:
         """
         :param filename:
             name of JSON file describing the :any:`Design`
-        :param domain_label_decoder:
-            Function that transforms JSON representation of :py:data:`Domain.label` into the proper type.
-        :param strand_label_decoder:
-            Function that transforms JSON representation of :py:data:`Strand.label` into the proper type.
         :return:
             :any:`Design` described by the JSON file with name `filename`, assuming it was created using
             :py:meth`Design.to_json`.
         """
         with open(filename, 'r') as f:
             json_str = f.read()
-        return Design.from_json(json_str, strand_label_decoder, domain_label_decoder)
+        return Design.from_json(json_str)
 
     @staticmethod
-    def from_json(json_str: str,
-                  strand_label_decoder: Callable[[Any], StrandLabel] = lambda label: label,
-                  domain_label_decoder: Callable[[Any], DomainLabel] = lambda label: label,
-                  ) -> Design[StrandLabel, DomainLabel]:
+    def from_json(json_str: str) -> Design:
         """
         :param json_str:
             The string representing the :any:`Design` as a JSON object.
-        :param domain_label_decoder:
-            Function that transforms JSON representation of :py:data:`Domain.label` into the proper type.
-        :param strand_label_decoder:
-            Function that transforms JSON representation of :py:data:`Strand.label` into the proper type.
         :return:
             :any:`Design` described by this JSON string, assuming it was created using
             :py:meth`Design.to_json`.
         """
         json_map = json.loads(json_str)
-        design: Design[StrandLabel, DomainLabel] = Design.from_json_serializable(
-            json_map, domain_label_decoder=domain_label_decoder, strand_label_decoder=strand_label_decoder)
+        design: Design = Design.from_json_serializable(json_map)
         return design
 
     @staticmethod
-    def from_json_serializable(json_map: Dict[str, Any],
-                               domain_label_decoder: Callable[[Any], DomainLabel] = lambda label: label,
-                               strand_label_decoder: Callable[[Any], StrandLabel] = lambda label: label,
-                               ) -> 'Design[StrandLabel, DomainLabel]':
+    def from_json_serializable(json_map: Dict[str, Any]) -> Design:
         """
         :param json_map:
             JSON serializable object encoding this :any:`Design`, as returned by
             :py:meth:`Design.to_json_serializable`.
-        :param domain_label_decoder:
-            Function that transforms JSON representation of :py:data:`Domain.label` into the proper type.
-        :param strand_label_decoder:
-            Function that transforms JSON representation of :py:data:`Strand.label` into the proper type.
         :return:
             :any:`Design` represented by dict `json_map`, assuming it was created by
             :py:meth:`Design.to_json_serializable`. No constraints are populated.
         """
         pools_json = mandatory_field(Design, json_map, domain_pools_key)
         pools: List[DomainPool] = [DomainPool.from_json_serializable(pool_json) for pool_json in pools_json]
         pool_with_name: Dict[str, DomainPool] = {pool.name: pool for pool in pools}
 
         domains_json = mandatory_field(Design, json_map, domains_key)
         domains: List[Domain] = [
-            Domain.from_json_serializable(domain_json, pool_with_name=pool_with_name,
-                                          label_decoder=domain_label_decoder)
+            Domain.from_json_serializable(domain_json, pool_with_name=pool_with_name)
             for domain_json in domains_json]
         domain_with_name = {domain.name: domain for domain in domains}
 
         strands_json = mandatory_field(Design, json_map, strands_key)
-        strands = [Strand.from_json_serializable(
-            json_map=strand_json, domain_with_name=domain_with_name,
-            label_decoder=strand_label_decoder)
-            for strand_json in strands_json]
+        strands = [Strand.from_json_serializable(json_map=strand_json, domain_with_name=domain_with_name)
+                   for strand_json in strands_json]
 
         # modifications in whole design
         if nm.design_modifications_key in json_map:
             all_mods_json = json_map[nm.design_modifications_key]
             all_mods = {}
             for mod_key, mod_json in all_mods_json.items():
                 mod = nm.Modification.from_json(mod_json)
@@ -3300,19 +3253,19 @@
                 all_mods[mod_key] = mod
             Design.assign_modifications_to_strands(strands, strands_json, all_mods)
 
         return Design(strands=strands)
 
     def add_strand(self,
                    domain_names: List[str] | None = None,
-                   domains: List[Domain[DomainLabel]] | None = None,
+                   domains: List[Domain] | None = None,
                    starred_domain_indices: Iterable[int] | None = None,
                    group: str = default_strand_group,
                    name: str | None = None,
-                   label: StrandLabel | None = None,
+                   label: str | None = None,
                    idt: IDTFields | None = None,
                    ) -> Strand:
         """
         This is an alternative way to create strands instead of calling the :any:`Strand` constructor
         explicitly. It behaves similarly to the :any:`Strand` constructor, but it has an option
         to specify :any:`Domain`'s simply by giving a name.
 
@@ -3630,15 +3583,15 @@
     def domain_pools(self) -> List[DomainPool]:
         """
         :return:
             list of all :any:`DomainPool`'s in this :any:`Design`
         """
         return list(self.domain_pools_to_domain_map.keys())
 
-    def domains_by_pool_name(self, domain_pool_name: str) -> List[Domain[DomainLabel]]:
+    def domains_by_pool_name(self, domain_pool_name: str) -> List[Domain]:
         """
         :param domain_pool_name: name of a :any:`DomainPool`
         :return: the :any:`Domain`'s in `domain_pool`
         """
         domains_in_pool: List[Domain] = []
         for domain in self.domains:
             if domain.pool.name == domain_pool_name:
@@ -3646,15 +3599,15 @@
         return domains_in_pool
 
     @staticmethod
     def from_scadnano_file(
             sc_filename: str,
             fix_assigned_sequences: bool = True,
             ignored_strands: Iterable[Strand] | None = None
-    ) -> Design[StrandLabel, DomainLabel]:
+    ) -> Design:
         """
         Converts a scadnano Design stored in file named `sc_filename` to a a :any:`Design` for doing
         DNA sequence design.
         Each Strand name and Domain name from the scadnano Design are assigned as
         :py:data:`Strand.name` and :py:data:`Domain.name` in the obvious way.
         Assumes each Strand label is a string describing the strand group.
 
@@ -3674,18 +3627,18 @@
         :raises TypeError:
             If any scadnano strand label is not a string.
         """
         sc_design = sc.Design.from_scadnano_file(sc_filename)
         return Design.from_scadnano_design(sc_design, fix_assigned_sequences, ignored_strands)
 
     @staticmethod
-    def from_scadnano_design(sc_design: sc.Design[StrandLabel, DomainLabel],
+    def from_scadnano_design(sc_design: sc.Design,
                              fix_assigned_sequences: bool = True,
                              ignored_strands: Iterable[Strand] | None = None,
-                             warn_existing_domain_labels: bool = True) -> Design[StrandLabel, DomainLabel]:
+                             warn_existing_domain_labels: bool = True) -> Design:
         """
         Converts a scadnano Design `sc_design` to a a :any:`Design` for doing DNA sequence design.
         Each Strand name and Domain name from the scadnano Design are assigned as
         :py:data:`Strand.name` and :py:data:`Domain.name` in the obvious way.
         Assumes each Strand label is a string describing the strand group.
 
         The scadnano package must be importable.
@@ -3754,30 +3707,30 @@
                     assigned = True
             if not assigned:
                 sc_strand_groups[default_strand_group].append(sc_strand)
 
         # make dsd StrandGroups, taking names from Strands and Domains,
         # and assign (and maybe fix) DNA sequences
         strand_names: Set[str] = set()
-        design: Design[StrandLabel, DomainLabel] = Design()
+        design: Design = Design()
         for group, sc_strands in sc_strand_groups.items():
             for sc_strand in sc_strands:
                 # do not include strands with the same name more than once
                 if sc_strand.name in strand_names:
                     logger.debug('In scadnano design, found duplicate instance of strand with name '
                                  f'{sc_strand.name}; skipping all but the first when creating dsd design. '
                                  f'Please ensure that this strand really is supposed to have the same name.')
                     continue
 
                 domain_names: List[str] = [domain.name for domain in sc_strand.domains]
                 sequence = sc_strand.dna_sequence
-                nuad_strand: Strand[StrandLabel, DomainLabel] = design.add_strand(domain_names=domain_names,
-                                                                                  group=group,
-                                                                                  name=sc_strand.name,
-                                                                                  label=sc_strand.label)
+                nuad_strand: Strand = design.add_strand(domain_names=domain_names,
+                                                        group=group,
+                                                        name=sc_strand.name,
+                                                        label=sc_strand.label)
                 # assign sequence
                 if sequence is not None:
                     for dsd_domain, sc_domain in zip(nuad_strand.domains, sc_strand.domains):
                         domain_sequence = sc_domain.dna_sequence
                         # if this is a starred domain,
                         # take the WC complement first so the dsd Domain stores the "canonical" sequence
                         if sc_domain.name[-1] == '*':
@@ -3807,28 +3760,28 @@
         if hasattr(sc_strand.label, group_key):
             return getattr(sc_strand.label, group_key)
         elif isinstance(sc_strand.label, dict) and group_key in sc_strand.label:
             return sc_strand.label[group_key]
         else:
             raise AssertionError(f'label does not have either an attribute or a dict key "{group_key}"')
 
-    def assign_fields_to_scadnano_design(self, sc_design: sc.Design[StrandLabel, DomainLabel],
+    def assign_fields_to_scadnano_design(self, sc_design: sc.Design,
                                          ignored_strands: Iterable[Strand] = (),
                                          overwrite: bool = False):
         """
         Assigns DNA sequence, IDTFields, and StrandGroups (as a key in a scadnano String.label dict
         under key "group").
         TODO: document more
         """
         self.assign_sequences_to_scadnano_design(sc_design, ignored_strands, overwrite)
         self.assign_strand_groups_to_labels(sc_design, ignored_strands, overwrite)
         self.assign_idt_fields_to_scadnano_design(sc_design, ignored_strands, overwrite)
         self.assign_modifications_to_scadnano_design(sc_design, ignored_strands, overwrite)
 
-    def assign_sequences_to_scadnano_design(self, sc_design: sc.Design[StrandLabel, DomainLabel],
+    def assign_sequences_to_scadnano_design(self, sc_design: sc.Design,
                                             ignored_strands: Iterable[Strand] = (),
                                             overwrite: bool = False) -> None:
         """
         Assigns sequences from this :any:`Design` into `sc_design`.
 
         Also writes a label to each scadnano strand. If the label is None a new one is created as
         a dict with a key `group`. The name of the StrandGroup of the nuad design is the value
@@ -3925,15 +3878,15 @@
                         raise ValueError(f'Cannot assign strand group from nuad strand to scadnano strand '
                                          f'{sc_strand.name} (through its label field) because the '
                                          f'scadnano strand already has a label with group key '
                                          f'\n{sc_strand.label[group_key]}. '
                                          f'Set overwrite to True to force an overwrite.')
                     sc_strand.label[group_key] = nuad_strand.group
 
-    def assign_idt_fields_to_scadnano_design(self, sc_design: sc.Design[StrandLabel, DomainLabel],
+    def assign_idt_fields_to_scadnano_design(self, sc_design: sc.Design,
                                              ignored_strands: Iterable[Strand] = (),
                                              overwrite: bool = False) -> None:
         """
         Assigns :any:`IDTFields` from this :any:`Design` into `sc_design`.
 
         If multiple strands in `sc_design` share the same name, then all of them are assigned the
         IDT fields of the dsd :any:`Strand` with that name.
@@ -3956,15 +3909,15 @@
                     if sc_strand.idt is not None and not overwrite:
                         raise ValueError(f'Cannot assign IDT fields from dsd strand to scadnano strand '
                                          f'{sc_strand.name} because the scadnano strand already has '
                                          f'IDT fields assigned:\n{sc_strand.idt}. '
                                          f'Set overwrite to True to force an overwrite.')
                     sc_strand.idt = nuad_strand.idt.to_scadnano_idt()
 
-    def assign_modifications_to_scadnano_design(self, sc_design: sc.Design[StrandLabel, DomainLabel],
+    def assign_modifications_to_scadnano_design(self, sc_design: sc.Design,
                                                 ignored_strands: Iterable[Strand] = (),
                                                 overwrite: bool = False) -> None:
         """
         Assigns :any:`modifications.Modification`'s from this :any:`Design` into `sc_design`.
 
         If multiple strands in `sc_design` share the same name, then all of them are assigned the
         modifications of the dsd :any:`Strand` with that name.
@@ -4010,16 +3963,16 @@
                                      f'modification assigned at that offset:\n'
                                      f'{sc_strand.modifications_int[offset]} .'
                                      f'Set overwrite to True to force an overwrite.')
                 sc_strand.modifications_int[offset] = mod_int.to_scadnano_modification()
 
     def _assign_to_strand_without_checking_existing_sequence(
             self,
-            sc_strand: sc.Strand[StrandLabel, DomainLabel],
-            sc_design: sc.Design[StrandLabel, DomainLabel]
+            sc_strand: sc.Strand,
+            sc_design: sc.Design
     ) -> None:
         # check types
         if not isinstance(sc_design, sc.Design):
             raise TypeError(f'sc_design must be an instance of scadnano.Design, but it is {type(sc_design)}')
         if not isinstance(sc_strand, sc.Strand):
             raise TypeError(f'sc_strand must be an instance of scadnano.Strand, but it is {type(sc_strand)}')
 
@@ -4037,16 +3990,16 @@
                                      f'{list(self.domains_by_name.keys())}')
             domain_sequence = dsd_domain.concrete_sequence(starred)
             sequence_list.append(domain_sequence)
         strand_sequence = ''.join(sequence_list)
         sc_strand.set_dna_sequence(strand_sequence)
 
     @staticmethod
-    def _assign_to_strand_with_partial_sequence(sc_strand: sc.Strand[StrandLabel, DomainLabel],
-                                                sc_design: sc.Design[StrandLabel, DomainLabel],
+    def _assign_to_strand_with_partial_sequence(sc_strand: sc.Strand,
+                                                sc_design: sc.Design,
                                                 sc_domain_name_tuples: Dict[Tuple[str, ...], Strand]) -> None:
 
         # check types
         if not isinstance(sc_design, sc.Design):
             raise TypeError(f'sc_design must be an instance of scadnano.Design, but it is {type(sc_design)}')
         if not isinstance(sc_strand, sc.Strand):
             raise TypeError(f'sc_strand must be an instance of scadnano.Strand, but it is {type(sc_strand)}')
@@ -4301,15 +4254,14 @@
     
     For example, a common value for excess is the amount by which the NUPACK complex free energy exceeds
     a threshold.
     """
 
     _summary: Optional[str] = None
 
-
     value: pint.Quantity[Decimal] | None = None
     """
     If this is a "numeric" constraint, i.e., checking some number such as the complex free energy of a 
     strand and comparing it to a threshold, this is the "raw" value. It is optional, but if specified,
     then the raw values can be plotted in a Jupyter notebook by the function :meth:`display_report`.
     
     If a ``float``, then no units are assumed. If it is a ``str``, then it is assumed that it can be 
@@ -4351,15 +4303,20 @@
         """
         This string is displayed in the text report on constraints, after the name of the "part" (e.g.,
         strand, pair of domains, pair of strands).
 
         It can be set explicitly, or calculated from :data:`Result.value` if not set explicitly.
         """
         if self._summary is None:
-            return str(self.value)
+            # This formatting is "short pretty": https://pint.readthedocs.io/en/stable/user/formatting.html
+            # e.g., kcal/mol instead of kilocalorie / mol
+            # also 2 decimal places to make numbers line up nicely
+            self.value.default_format = '.2fC~'
+            summary_str = f'{self.value}'
+            return str(summary_str)
         else:
             return self._summary
 
     @summary.setter
     def summary(self, summary: str) -> None:
         self._summary = summary
```

### Comparing `nuad-0.4.2/nuad/json_noindent_serializer.py` & `nuad-0.4.3/nuad/json_noindent_serializer.py`

 * *Files identical despite different names*

### Comparing `nuad-0.4.2/nuad/modifications.py` & `nuad-0.4.3/nuad/modifications.py`

 * *Files identical despite different names*

### Comparing `nuad-0.4.2/nuad/np.py` & `nuad-0.4.3/nuad/np.py`

 * *Files identical despite different names*

### Comparing `nuad-0.4.2/nuad/nupack_viennaRNA_parameter_files/dna_mathews1999.par` & `nuad-0.4.3/nuad/nupack_viennaRNA_parameter_files/dna_mathews1999.par`

 * *Files identical despite different names*

### Comparing `nuad-0.4.2/nuad/nupack_viennaRNA_parameter_files/dna_mathews2004.par` & `nuad-0.4.3/nuad/nupack_viennaRNA_parameter_files/dna_mathews2004.par`

 * *Files identical despite different names*

### Comparing `nuad-0.4.2/nuad/search.py` & `nuad-0.4.3/nuad/search.py`

 * *Files 0% similar despite different names*

```diff
@@ -1920,15 +1920,15 @@
             assert ev.violated
         else:
             assert not ev.violated
 
 
 @dataclass
 class Evaluation(Generic[DesignPart]):
-    # Represents a violation of a single :any:`Constraint` in a :any:`Design`.
+    # Represents an evaluation of a single :any:`Constraint` in a :any:`Design`.
     # The "part" of the :any:`Design` that was evaluated for the constraint is generic type `DesignPart`
     # (e.g., for :any:`StrandPairConstraint`, DesignPart = :any:`Pair` [:any:`Strand`]).
 
     constraint: Constraint
     # :any:`Constraint` that was evaluated to result in this :any:`Evaluation`.
 
     violated: bool
```

### Comparing `nuad-0.4.2/nuad/stopwatch.py` & `nuad-0.4.3/nuad/stopwatch.py`

 * *Files identical despite different names*

### Comparing `nuad-0.4.2/nuad/vienna_nupack.py` & `nuad-0.4.3/nuad/vienna_nupack.py`

 * *Files identical despite different names*

### Comparing `nuad-0.4.2/nuad.egg-info/PKG-INFO` & `nuad-0.4.3/nuad.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nuad
-Version: 0.4.2
+Version: 0.4.3
 Summary: nuad stands for "NUcleic Acid Designer". Enables one to specify constraints on a DNA (or RNA) nanostructure made from synthetic DNA/RNA and then attempts to find concrete DNA sequences that satisfy the constraints.
 Home-page: https://github.com/UC-Davis-molecular-computing/nuad
 Author: David Doty
 Author-email: doty@ucdavis.edu
 License: MIT
 Platform: UNKNOWN
 Requires-Python: >=3.7
@@ -147,17 +147,17 @@
 - `Strand`: A `Strand` contains an ordered list `domains` of `Domain`'s, together with an identification of which `Domain`'s are starred in this `Strand`, the latter specified as a set `starred_domain_indices` of indices (starting at 0) into the list `domains`. For example, the `Strand` consisting of `Domain`'s `a`, `b*`, `c`, `b`, `d*`, in that order, would have `domains = [a, b, c, b, d]` and `starred_domain_indices = {1, 4}`.
 
 - `Design`: This describes the whole system. Generally you will have one `Design`, which is composed of a list of `Strand`'s.
 
 - `Constraint`: There are several kinds of constraint objects. Not all of them are related in the type hierarchy. 
 
     - **"hard" constraints on Domain sequences:** 
-    These are the strictest constraints, which do not even allow certain `Domain` sequences to be considered. They are applied by a `DomainPool` before allowing a sequence to be returned from `DomainPool.generate_sequence()`. These are of two types: `NumpyConstraint` and `SequenceConstraint`. Each of them indicates whether a DNA sequence is allowed or not; for instance a constraint forbidding 4 G's in a row would permit AGGGTT but forbid AGGGGT. The difference between them is that a `NumpyConstraint` operates on many DNA sequences at a time, representing them as a 2D numpy byte array (e.g., a 1000 &times; 15 array of bytes to represent 1000 sequences, each of length 15), and for operations that numpy is suited for, can evaluate these constraints *much* faster than the equivalent Python code that would loop over each sequence individually. However, if you have a constraint that is not straightforward to express using numpy operations, then a `SequenceConstraint` can be used to express it in plain Python. A `SequenceConstraint` is simply a type alias for a Python function that takes a string as input representing the DNA sequence and returns a Boolean indicating whether the sequence satisfies the constraint. Due to the speed of numpy, it is advised to use `SequenceConstraint`'s only if necessary because it cannot be expressed as a `NumpyConstraint`.
+    These are the strictest constraints, which do not even allow certain `Domain` sequences to be considered, known as "filters". They are applied by a `DomainPool` before allowing a sequence to be returned from `DomainPool.generate_sequence()`, which is the method called whenever the search algorithm wants to try a new DNA sequence for a `Domain`. These are of two types of filters: `NumpyFilter` and `SequenceFilter`. Each of them indicates whether a DNA sequence is allowed or not; for instance a filter forbidding 4 G's in a row would permit AGGGTT but forbid AGGGGT. The difference between them is that a `NumpyFilter` operates on many DNA sequences at a time, representing them as a 2D numpy byte array (e.g., a 1000 &times; 15 array of bytes to represent 1000 sequences, each of length 15), and for operations that numpy is suited for, can evaluate these filters *much* faster than the equivalent Python code that would loop over each sequence individually. However, if you have a filter that is not straightforward to express using numpy operations, then a `SequenceFilter` can be used to express it in plain Python. A `SequenceFilter` is simply a type alias for a Python function that takes a string as input representing the DNA sequence and returns a Boolean indicating whether the sequence satisfies the filter. Due to the speed of numpy, it is advised to use `SequenceFilter`'s only if necessary because it cannot be expressed as a `NumpyFilter`.
 
-    - **"soft" constraints:**  All other constraints are subclasses of the abstract superclass `Constraint`. These constrains are "softer": sequences violating the constraints are allowed to be assigned to `Domain`'s. The sequence design algorithm steadily improves the design by changing sequences until all of these constraints are satisfied. The different subtypes of the base class `Constraint` correspond to different parts of the `Design` that are being evaluated by the `Constraint`. The types are:
+    - **"soft" constraints:**  All other constraints are subclasses of the abstract superclass `Constraint`. These constrains are "softer" than filters as described above: sequences violating the constraints are allowed to be assigned to `Domain`'s. The sequence design algorithm steadily improves the design by changing sequences until all of these constraints are satisfied. The different subtypes of the base class `Constraint` correspond to different parts of the `Design` that are being evaluated by the `Constraint`. The types are:
 
         - `SingularConstraint`: This is an abstract superclass of the following concrete subclasses. The difference with the other abstract superclass `BulkConstraint` is explained in `BulkConstraint` below.
         
             - `DomainConstraint`: This only looks at a single `Domain`. In practice this is not used much, since there's not much information in a `Domain` other than its DNA sequence, so a `SequenceConstraint` or `NumpyConstraint` typically would already have filtered out any DNA sequence not satisfying such a constraint.
 
             - `StrandConstraint`: This evaluates a whole `Strand`. A common example is that NUPACK's `pfunc` should indicate a complex free energy above a certain threshold, indicating the `Strand` has little secondary structure. This example constraint is available in the library by calling [nupack_strand_complex_free_energy_constraint](https://nuad.readthedocs.io/en/latest/#constraints.nupack_strand_complex_free_energy_constraint).
 
@@ -184,15 +184,15 @@
     The search algorithm evaluates the constraints, and for each violated constraint, it turns the `excess` value into a "score" by first passing it through the "score transfer function", which by default squares the value, and then multiplies by the value `Constraint.weight` (by default 1). The goal of the search is to minimize the sum of scores across all violated `Constraint`'s. The reason that the score is squared is that this leads the search algorithm to (slightly) favor reducing the excess of constraint violations that are "more in excess", i.e., it would reduce the total score more to reduce an excess from 4 to 3 (reducing the score from 4<sup>2</sup>=16 to 3<sup>2</sup>=9, a reduction of 16-9=7) than to reduce an excess from 2 to 1 (which reduces 2<sup>2</sup>=4 to 1<sup>2</sup>=1, a reduction of only 4-1=3).
 
     The full search algorithm is described in the [API documentation for the function nuad.search.search_for_sequences](https://nuad.readthedocs.io/en/latest/#search.search_for_sequences).
 
 
 ## Constraint evaluations must be pure functions of their inputs
 
-For all constraints, it is critical that the `evaluate` or `evaluate_bulk` functions be *pure* functions of their inputs: the return value should depend only on the parameters passed to the function. For example, a `StrandPairConstraint` takes two strands as input, and its `(excess, summary)` return values should depend *only* on those two strands. Similarly, a `StrandsConstraint`, whose `evaluate_bulk` function takes a list of strands as input, should return a list of tuples, where each tuple represents a violation of a strand that depends only on that strand. This is required because nuad does an optimization in which constraints are only evaluated if they depend on parts of the design that contain the domain(s) that changed in the current iteration.
+For all constraints, it is critical that the `evaluate` or `evaluate_bulk` functions be *pure* functions of their inputs: the return value should depend only on the parameters passed to the function. For example, a `StrandPairConstraint` takes two strands as input, and its `Result` return values should depend *only* on those two strands. Similarly, a `StrandsConstraint`, whose `evaluate_bulk` function takes a list of strands as input, should return a list of tuples, where each tuple represents a violation of a strand that depends only on that strand. This is required because nuad does an optimization in which constraints are only evaluated if they depend on parts of the design that contain the domain(s) that changed in the current iteration.
 
 For example, suppose there are 100 strands, but only 3 strands contain the domain `x`, and `x` is the domain whose DNA sequence is changed in the current search iteration. Then each `StrandConstraint` `s` will be evaluated only on those 3 strands, on the assumption that the other 97 strands would have the same output of the function `s.evaluate` as before. 
 
 In the case of `evaluate_bulk`, the constraint is even stronger. `evaluate_bulk` takes a list of objects as input and returns of list of the same size. The `i`'th element of the returned list should depend only on the `i`'th element of the input list. This is because a similar optimization is done as above. For example, if the changed domain appears in only 3 strands out of 100, a `StrandsConstraint` will pass in only those 3 strands as input to `evaluate_bulk`, not the full list of 100 strands, on the assumption that the other 97 strands would be processed the same by the `evaluate_bulk` function.
 
 ## Examples
 Some example scripts can be found in the [examples/](examples/) subfolder.
```

### Comparing `nuad-0.4.2/setup.py` & `nuad-0.4.3/setup.py`

 * *Files identical despite different names*

