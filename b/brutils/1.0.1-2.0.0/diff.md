# Comparing `tmp/brutils-1.0.1.tar.gz` & `tmp/brutils-2.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/brutils-1.0.1.tar", last modified: Sat Jan 21 19:03:51 2017, max compression
+gzip compressed data, was "brutils-2.0.0.tar", max compression
```

## Comparing `brutils-1.0.1.tar` & `brutils-2.0.0.tar`

### file list

```diff
@@ -1,14 +1,8 @@
-drwxr-xr-x   0 luizfb     (501) staff       (20)        0 2017-01-21 19:03:51.000000 brutils-1.0.1/
-drwxr-xr-x   0 luizfb     (501) staff       (20)        0 2017-01-21 19:03:51.000000 brutils-1.0.1/brutils/
--rw-r--r--   0 luizfb     (501) staff       (20)        0 2017-01-10 07:49:44.000000 brutils-1.0.1/brutils/__init__.py
--rw-r--r--   0 luizfb     (501) staff       (20)     2502 2017-01-10 22:08:54.000000 brutils-1.0.1/brutils/cnpj.py
--rw-r--r--   0 luizfb     (501) staff       (20)     2186 2017-01-10 21:51:41.000000 brutils-1.0.1/brutils/cpf.py
-drwxr-xr-x   0 luizfb     (501) staff       (20)        0 2017-01-21 19:03:51.000000 brutils-1.0.1/brutils.egg-info/
--rw-r--r--   0 luizfb     (501) staff       (20)        1 2017-01-21 19:03:51.000000 brutils-1.0.1/brutils.egg-info/dependency_links.txt
--rw-r--r--   0 luizfb     (501) staff       (20)      869 2017-01-21 19:03:51.000000 brutils-1.0.1/brutils.egg-info/PKG-INFO
--rw-r--r--   0 luizfb     (501) staff       (20)      209 2017-01-21 19:03:51.000000 brutils-1.0.1/brutils.egg-info/SOURCES.txt
--rw-r--r--   0 luizfb     (501) staff       (20)        8 2017-01-21 19:03:51.000000 brutils-1.0.1/brutils.egg-info/top_level.txt
--rw-r--r--   0 luizfb     (501) staff       (20)        1 2017-01-21 19:03:51.000000 brutils-1.0.1/brutils.egg-info/zip-safe
--rw-r--r--   0 luizfb     (501) staff       (20)      869 2017-01-21 19:03:51.000000 brutils-1.0.1/PKG-INFO
--rw-r--r--   0 luizfb     (501) staff       (20)       59 2017-01-21 19:03:51.000000 brutils-1.0.1/setup.cfg
--rw-r--r--   0 luizfb     (501) staff       (20)      959 2017-01-21 19:03:40.000000 brutils-1.0.1/setup.py
+-rw-r--r--   0        0        0     1072 2023-07-23 11:33:33.145801 brutils-2.0.0/LICENSE
+-rw-r--r--   0        0        0     4444 2023-07-23 11:33:33.145801 brutils-2.0.0/README.md
+-rw-r--r--   0        0        0      443 2023-07-23 11:33:33.145801 brutils-2.0.0/brutils/__init__.py
+-rw-r--r--   0        0        0     1421 2023-07-23 11:33:33.145801 brutils-2.0.0/brutils/cep.py
+-rw-r--r--   0        0        0     3309 2023-07-23 11:33:33.145801 brutils-2.0.0/brutils/cnpj.py
+-rw-r--r--   0        0        0     2922 2023-07-23 11:33:33.145801 brutils-2.0.0/brutils/cpf.py
+-rw-r--r--   0        0        0     1289 2023-07-23 11:33:33.145801 brutils-2.0.0/pyproject.toml
+-rw-r--r--   0        0        0     5678 1970-01-01 00:00:00.000000 brutils-2.0.0/PKG-INFO
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `brutils-1.0.1/brutils/cnpj.py` & `brutils-2.0.0/brutils/cnpj.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,76 +1,111 @@
 from itertools import chain
 from random import randint
 
 
 # FORMATTING
 ############
 
+
 def sieve(dirty):  # type: (str) -> str
     """
     Filters out CNPJ formatting symbols. Symbols that are not used
     in the CNPJ formatting are left unfiltered on purpose so that
     if fails other tests, because their presence indicate that the
     input was somehow corrupted.
     """
-    return ''.join(filter(lambda char: char not in './-', dirty))
+    return "".join(filter(lambda char: char not in "./-", dirty))
+
+
+def remove_symbols(dirty):  # type: (str) -> str
+    """Alias to the function `sieve`. Better naming."""
+    return sieve(dirty)
 
 
 def display(cnpj):  # type: (str) -> str
     """
     Will format an adequately formatted numbers-only CNPJ string,
     adding in standard formatting visual aid symbols for display.
     """
-    if not cnpj.isdigit() or len(cnpj) != 14 or len(set(cnpj)) == 1: return None
-    return '{}.{}.{}/{}-{}'.format(cnpj[:2], cnpj[2:5], cnpj[5:8], cnpj[8:12], cnpj[12:])
+    if not cnpj.isdigit() or len(cnpj) != 14 or len(set(cnpj)) == 1:
+        return None
+    return "{}.{}.{}/{}-{}".format(
+        cnpj[:2], cnpj[2:5], cnpj[5:8], cnpj[8:12], cnpj[12:]
+    )
 
 
-# CALCULATORS
-#############
-
-def hashdigit(cnpj, position):  # type: (str, int) -> int
+def format_cnpj(cnpj):  # type: (str) -> str
     """
-    Will compute the given `position` checksum digit for the `cnpj`
-    input. The input needs to contain all elements previous to
-    `position` else computation will yield the wrong result.
+    Will format an adequately formatted numbers-only CNPJ string,
+    adding in standard formatting visual aid symbols for display.
     """
-    weightgen = chain(range(position -8, 1, -1), range(9, 1, -1))
-    val = sum(int(digit) * weight for digit, weight in zip(cnpj, weightgen)) % 11
-    return 0 if val < 2 else 11 - val
 
+    if not is_valid(cnpj):
+        return None
 
-def checksum(basenum):  # type: (str) -> str
-    """
-    Will compute the checksum digits for a given CNPJ base number.
-    `basenum` needs to be a digit-string of adequate length.
-    """
-    verifying_digits = ''
-    verifying_digits += str(hashdigit(basenum, 13))
-    verifying_digits += str(hashdigit(basenum + verifying_digits, 14))
-    return verifying_digits
+    return "{}.{}.{}/{}-{}".format(
+        cnpj[:2], cnpj[2:5], cnpj[5:8], cnpj[8:12], cnpj[12:14]
+    )
 
 
 # OPERATIONS
 ############
 
+
 def validate(cnpj):  # type: (str) -> bool
     """
     Returns whether or not the verifying checksum digits of the
     given `cnpj` match it's base number. Input should be a digit
     string of proper length.
     """
-    if not cnpj.isdigit() or len(cnpj) != 14 or len(set(cnpj)) == 1: return False
-    return all(hashdigit(cnpj, i +13) == int(v) for i, v in enumerate(cnpj[12:]))
+    if not cnpj.isdigit() or len(cnpj) != 14 or len(set(cnpj)) == 1:
+        return False
+    return all(
+        _hashdigit(cnpj, i + 13) == int(v) for i, v in enumerate(cnpj[12:])
+    )
+
+
+def is_valid(cnpj):  # type: (str) -> bool
+    """
+    Returns whether or not the verifying checksum digits of the
+    given `cnpj` match it's base number. Input should be a digit
+    string of proper length.
+    Using this method name to match with the js library  api.
+    Using the same method to ensure backwards compatibility.
+    """
+    return isinstance(cnpj, str) and validate(cnpj)
 
 
 def generate(branch=1):  # type: (int) -> str
     """
     Generates a random valid CNPJ digit string. An optional branch
     number parameter can be given, it defaults to 1.
     """
     branch %= 10000
     branch += int(branch == 0)
     branch = str(branch).zfill(4)
     base = str(randint(0, 99999999)).zfill(8) + branch
-    while len(set(base)) == 1: base = str(randint(0, 99999999)).zfill(8) + branch
-    return base + checksum(base)
 
+    return base + _checksum(base)
+
+
+def _hashdigit(cnpj, position):  # type: (str, int) -> int
+    """
+    Will compute the given `position` checksum digit for the `cnpj`
+    input. The input needs to contain all elements previous to
+    `position` else computation will yield the wrong result.
+    """
+    weightgen = chain(range(position - 8, 1, -1), range(9, 1, -1))
+    val = (
+        sum(int(digit) * weight for digit, weight in zip(cnpj, weightgen)) % 11
+    )
+    return 0 if val < 2 else 11 - val
+
+
+def _checksum(basenum):  # type: (str) -> str
+    """
+    Will compute the checksum digits for a given CNPJ base number.
+    `basenum` needs to be a digit-string of adequate length.
+    """
+    verifying_digits = str(_hashdigit(basenum, 13))
+    verifying_digits += str(_hashdigit(basenum + verifying_digits, 14))
+    return verifying_digits
```

### Comparing `brutils-1.0.1/brutils/cpf.py` & `brutils-2.0.0/brutils/cpf.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,68 +1,114 @@
 from random import randint
 
 
 # FORMATTING
 ############
 
+
 def sieve(dirty):  # type: (str) -> str
     """
-    Filters out CPF formatting symbols. Symbols that are not used
-    in the CPF formatting are left unfiltered on purpose so that
-    if fails other tests, because their presence indicate that the
-    input was somehow corrupted.
+    Filters out CPF formatting symbols.
+
+    Symbols that are not used in the CPF formatting are left
+    unfiltered on purpose so that if fails other tests,
+    because their presence indicate that the input was somehow corrupted.
     """
-    return ''.join(filter(lambda char: char not in '.-', dirty))
+
+    return "".join(filter(lambda char: char not in ".-", dirty))
+
+
+def remove_symbols(dirty):  # type: (str) -> str
+    """Alias to the function `sieve`. Better naming."""
+    return sieve(dirty)
 
 
 def display(cpf):  # type: (str) -> str
     """
-    Will format an adequately formatted numbers-only CPF string,
+    Format an adequately formatted numbers-only CPF string,
     adding in standard formatting visual aid symbols for display.
+    Backcompatibility for Version 1.0.1.
     """
-    if not cpf.isdigit() or len(cpf) != 11 or len(set(cpf)) == 1: return None
-    return '{}.{}.{}-{}'.format(cpf[:3], cpf[3:6], cpf[6:9], cpf[9:])
 
+    if not cpf.isdigit() or len(cpf) != 11 or len(set(cpf)) == 1:
+        return None
+
+    return "{}.{}.{}-{}".format(cpf[:3], cpf[3:6], cpf[6:9], cpf[9:])
 
-# CALCULATORS
-#############
 
-def hashdigit(cpf, position):  # type: (str, int) -> int
+def format_cpf(cpf):  # type: (str) -> str
     """
-    Will compute the given `position` checksum digit for the `cpf`
-    input. The input needs to contain all elements previous to
-    `position` else computation will yield the wrong result.
+    Format an adequately formatted numbers-only CPF string,
+    Returns a cpf formatted with standard visual aid symbols.
+    Returns None if cpf is invalid.
     """
-    val = sum(int(digit) * weight for digit, weight in zip(cpf, range(position, 1, -1))) % 11
-    return 0 if val < 2 else 11 - val
 
+    if not is_valid(cpf):
+        return None
 
-def checksum(basenum):  # type: (str) -> str
-    """
-    Will compute the checksum digits for a given CPF base number.
-    `basenum` needs to be a digit-string of adequate length.
-    """
-    verifying_digits = ''
-    verifying_digits += str(hashdigit(basenum, 10))
-    verifying_digits += str(hashdigit(basenum + verifying_digits, 11))
-    return verifying_digits
+    return "{}.{}.{}-{}".format(cpf[:3], cpf[3:6], cpf[6:9], cpf[9:11])
 
 
 # OPERATIONS
 ############
 
+
 def validate(cpf):  # type: (str) -> bool
     """
     Returns whether or not the verifying checksum digits of the
     given `cpf` match it's base number. Input should be a digit
     string of proper length.
+
+    Source: https://www.geradorcpf.com/algoritmo_do_cpf.htm
+    Backcompatibility for Version 1.0.1.
+    """
+
+    if not cpf.isdigit() or len(cpf) != 11 or len(set(cpf)) == 1:
+        return False
+
+    return all(_hashdigit(cpf, i + 10) == int(v) for i, v in enumerate(cpf[9:]))
+
+
+def is_valid(cpf):  # type: (str) -> bool
     """
-    if not cpf.isdigit() or len(cpf) != 11 or len(set(cpf)) == 1: return False
-    return all(hashdigit(cpf, i +10) == int(v) for i, v in enumerate(cpf[9:]))
+    Evaluates that cpf is String and calls validate.
+    """
+
+    return isinstance(cpf, str) and validate(cpf)
 
 
 def generate():  # type: () -> str
     """Generates a random valid CPF digit string."""
+
     base = str(randint(1, 999999998)).zfill(9)
-    while len(set(base)) == 1: base = str(randint(1, 999999998)).zfill(9)
-    return base + checksum(base)
 
+    return base + _checksum(base)
+
+
+def _hashdigit(cpf, position):  # type: (str, int) -> int
+    """
+    Will compute the given `position` checksum digit for the `cpf`
+    input. The input needs to contain all elements previous to
+    `position` else computation will yield the wrong result.
+    """
+
+    val = (
+        sum(
+            int(digit) * weight
+            for digit, weight in zip(cpf, range(position, 1, -1))
+        )
+        % 11
+    )
+
+    return 0 if val < 2 else 11 - val
+
+
+def _checksum(basenum):  # type: (str) -> str
+    """
+    Will compute the checksum digits for a given CPF base number.
+    `basenum` needs to be a digit-string of adequate length.
+    """
+
+    verifying_digits = str(_hashdigit(basenum, 10))
+    verifying_digits += str(_hashdigit(basenum + verifying_digits, 11))
+
+    return verifying_digits
```

