# Comparing `tmp/kerykeion-4.0a5.tar.gz` & `tmp/kerykeion-4.0rc1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "kerykeion-4.0a5.tar", max compression
+gzip compressed data, was "kerykeion-4.0rc1.tar", max compression
```

## Comparing `kerykeion-4.0a5.tar` & `kerykeion-4.0rc1.tar`

### file list

```diff
@@ -1,24 +1,26 @@
--rw-r--r--   0        0        0    18091 2023-01-08 19:26:15.413715 kerykeion-4.0a5/LICENSE
--rw-r--r--   0        0        0     6519 2023-02-15 21:33:35.198498 kerykeion-4.0a5/README.md
--rw-r--r--   0        0        0     3746 2023-02-15 21:33:35.199155 kerykeion-4.0a5/kerykeion/__init__.py
--rw-r--r--   0        0        0      316 2023-02-15 21:33:35.199279 kerykeion-4.0a5/kerykeion/aspects/__init__.py
--rw-r--r--   0        0        0      230 2023-02-15 21:33:35.199380 kerykeion-4.0a5/kerykeion/aspects/aspects_settings.py
--rw-r--r--   0        0        0     2982 2023-02-15 21:33:35.199557 kerykeion-4.0a5/kerykeion/aspects/composite_aspects.py
--rw-r--r--   0        0        0    10625 2023-02-15 21:33:35.199665 kerykeion-4.0a5/kerykeion/aspects/natal_aspects.py
--rw-r--r--   0        0        0      127 2023-02-15 21:33:35.199813 kerykeion-4.0a5/kerykeion/charts/__init__.py
--rwxr-xr-x   0        0        0    67889 2023-02-15 21:33:35.200435 kerykeion-4.0a5/kerykeion/charts/charts_svg.py
--rwxr-xr-x   0        0        0    56546 2023-01-08 19:26:15.412083 kerykeion-4.0a5/kerykeion/charts/templates/basic.xml
--rwxr-xr-x   0        0        0    56733 2023-01-08 19:26:15.412582 kerykeion-4.0a5/kerykeion/charts/templates/extended.xml
--rw-r--r--   0        0        0     4690 2023-02-15 21:33:35.200689 kerykeion-4.0a5/kerykeion/fetch_geonames.py
--rw-r--r--   0        0        0    12446 2023-02-15 21:33:35.200979 kerykeion-4.0a5/kerykeion/kr.config.json
--rw-r--r--   0        0        0    21131 2023-02-15 21:33:35.201333 kerykeion-4.0a5/kerykeion/kr_instance.py
--rw-r--r--   0        0        0      104 2023-02-15 21:33:35.201474 kerykeion-4.0a5/kerykeion/kr_types/__init__.py
--rw-r--r--   0        0        0      337 2023-02-15 21:33:35.201619 kerykeion-4.0a5/kerykeion/kr_types/kerykeion_exception.py
--rw-r--r--   0        0        0     1027 2023-02-15 21:33:35.201725 kerykeion-4.0a5/kerykeion/kr_types/kr_literals.py
--rw-r--r--   0        0        0     3857 2023-02-15 21:33:35.201812 kerykeion-4.0a5/kerykeion/kr_types/kr_models.py
--rw-r--r--   0        0        0     7592 2023-02-15 21:33:35.202022 kerykeion-4.0a5/kerykeion/relationship_score.py
--rw-r--r--   0        0        0     2455 2023-02-15 21:33:35.202207 kerykeion-4.0a5/kerykeion/report.py
--rw-r--r--   0        0        0     6673 2023-02-15 21:33:35.202442 kerykeion-4.0a5/kerykeion/utilities.py
--rw-r--r--   0        0        0     2229 2023-02-15 21:34:49.315701 kerykeion-4.0a5/pyproject.toml
--rw-r--r--   0        0        0     7877 1970-01-01 00:00:00.000000 kerykeion-4.0a5/setup.py
--rw-r--r--   0        0        0     8294 1970-01-01 00:00:00.000000 kerykeion-4.0a5/PKG-INFO
+-rw-r--r--   0        0        0     6613 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/README.md
+-rw-r--r--   0        0        0     3885 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/__init__.py
+-rw-r--r--   0        0        0      292 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/aspects/__init__.py
+-rw-r--r--   0        0        0    10441 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/aspects/natal_aspects.py
+-rw-r--r--   0        0        0     2867 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/aspects/synastry_aspects.py
+-rw-r--r--   0        0        0    21213 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/astrological_subject.py
+-rw-r--r--   0        0        0      127 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/charts/__init__.py
+-rw-r--r--   0        0        0     3124 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/charts/charts_utils.py
+-rwxr-xr-x   0        0        0    66555 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/charts/kerykeion_chart_svg.py
+-rwxr-xr-x   0        0        0    69874 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/charts/templates/chart.xml
+-rw-r--r--   0        0        0     4694 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/fetch_geonames.py
+-rw-r--r--   0        0        0      104 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/kr_types/__init__.py
+-rw-r--r--   0        0        0     2184 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/kr_types/chart_types.py
+-rw-r--r--   0        0        0      314 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/kr_types/kerykeion_exception.py
+-rw-r--r--   0        0        0     1034 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/kr_types/kr_literals.py
+-rw-r--r--   0        0        0     3971 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/kr_types/kr_models.py
+-rw-r--r--   0        0        0     6860 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/relationship_score.py
+-rw-r--r--   0        0        0     2481 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/report.py
+-rw-r--r--   0        0        0       74 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/settings/__init__.py
+-rw-r--r--   0        0        0    13150 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/settings/kerykeion_settings.py
+-rw-r--r--   0        0        0    12167 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/settings/kr.config.json
+-rw-r--r--   0        0        0       73 2023-07-23 15:00:51.479211 kerykeion-4.0rc1/kerykeion/sweph/README.md
+-rw-r--r--   0        0        0   223002 2023-07-23 15:00:51.483211 kerykeion-4.0rc1/kerykeion/sweph/seas_18.se1
+-rw-r--r--   0        0        0     5707 2023-07-23 15:00:51.483211 kerykeion-4.0rc1/kerykeion/utilities.py
+-rw-r--r--   0        0        0     2318 2023-07-23 15:00:51.483211 kerykeion-4.0rc1/pyproject.toml
+-rw-r--r--   0        0        0     8245 1970-01-01 00:00:00.000000 kerykeion-4.0rc1/PKG-INFO
```

### Comparing `kerykeion-4.0a5/README.md` & `kerykeion-4.0rc1/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -22,97 +22,96 @@
 
 &nbsp;
 
 Kerykeion is a python library for Astrology.
 It can calculate all the planet and house position,
 also it can calculate the aspects of a single persone or between two, you can set how many planets you
 need in the settings in the utility module.
-It also can generate an SVG of a birthchart, a composite chart or a transit chart.
+It also can generate an SVG of a birthchart, a synastry chart or a transit chart.
 
 ## Installation
 
-Kerykeion is a *Python 3.9* package, make sure you have *Python 3.9* or above installed on your system.
+Kerykeion is a _Python 3.9_ package, make sure you have _Python 3.9_ or above installed on your system.
 
 ```bash
 pip3 install kerykeion
 ```
 
 ## Usage
 
 Here some examples:
 
 ```python
 
 # Import the main class for creating a kerykeion instance:
-from kerykeion import KrInstance
+from kerykeion import AstrologicalSubject
 
 # Create a kerykeion instance:
 # Args: Name, year, month, day, hour, minuts, city, nation(optional)
-kanye = KrInstance("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
+kanye = AstrologicalSubject("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
 
 # Get the information about the sun in the chart:
 # (The position of the planets always starts at 0)
 kanye.sun
 
 #> {'name': 'Sun', 'quality': 'Mutable', 'element': 'Air', 'sign': 'Gem', 'sign_num': 2, 'pos': 17.598992059774275, 'abs_pos': 77.59899205977428, 'emoji': '♊️', 'house': '12th House', 'retrograde': False}
 
-# Get informations about the first house:
+# Get information about the first house:
 kanye.first_house
 
-#> {'name': 'First House', 'quality': 'Cardinal', 'element': 'Water', 'sign': 'Can', 'sign_num': 3, 'pos': 17.995779673209114, 'abs_pos': 107.99577967320911, 'emoji': '♋️'}
+#> {'name': 'First_House', 'quality': 'Cardinal', 'element': 'Water', 'sign': 'Can', 'sign_num': 3, 'pos': 17.995779673209114, 'abs_pos': 107.99577967320911, 'emoji': '♋️'}
 
 # Get element of the moon sign:
 kanye.moon.get("element")
 
 #> 'Water'
 
 ```
 
 **To avoid connecting to GeoNames (eg. avoiding hourly limit or no internet connection) you should instance kerykeion like this:**
 
 ```python
-kanye = KrInstance(
+kanye = AstrologicalSubject(
     "Kanye", 1977, 6, 8, 8, 45,
     lng=50, lat=50, tz_str="Europe/Rome"
     )
 ```
 
 ## Generate a SVG Chart:
 
 ```python
-from kerykeion import KrInstance, MakeSvgInstance
+from kerykeion import AstrologicalSubject, KerykeionChartSVG
 
-first = KrInstance("Jack", 1990, 6, 15, 15, 15, "Roma")
-second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma")
+first = AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma")
+second = AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma")
 
-# Set the type, it can be Natal, Composite or Transit
+# Set the type, it can be Natal, Synastry or Transit
 
-name = MakeSvgInstance(first, chart_type="Composite", second_obj=second)
+name = KerykeionChartSVG(first, chart_type="Synastry", second_obj=second)
 name.makeSVG()
 print(len(name.aspects_list))
 
 #> Generating kerykeion object for Jack...
 #> Generating kerykeion object for Jane...
 #> Jack birth location: Roma, 41.89193, 12.51133
 #> SVG Generated Correctly
 #> 38
 
 ```
 
-![alt text](http://centuryboy.altervista.org/JackComposite_Chart.svg)
-
+![alt text](http://centuryboy.altervista.org/JackSynastry_Chart.svg)
 
 # Report
 
 To print a report of all the data:
 
 ```python
-from kerykeion import Report, KrInstance
+from kerykeion import Report, AstrologicalSubject
 
-kanye = KrInstance("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
+kanye = AstrologicalSubject("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
 report = Report(kanye)
 report.print_report()
 
 ```
 
 Returns:
 
@@ -122,62 +121,62 @@
 | Date     | Time | Location    | Longitude | Latitude |
 +----------+------+-------------+-----------+----------+
 | 8/6/1977 | 8:45 | Atlanta, US | -84.38798 | 33.749   |
 +----------+------+-------------+-----------+----------+
 +-----------+------+-------+------+----------------+
 | Planet    | Sign | Pos.  | Ret. | House          |
 +-----------+------+-------+------+----------------+
-| Sun       | Gem  | 17.6  | -    | Twelfth House  |
-| Moon      | Pis  | 16.43 | -    | Ninth House    |
-| Mercury   | Tau  | 26.29 | -    | Eleventh House |
-| Venus     | Tau  | 2.03  | -    | Tenth House    |
-| Mars      | Tau  | 1.79  | -    | Tenth House    |
-| Jupiter   | Gem  | 14.61 | -    | Eleventh House |
-| Saturn    | Leo  | 12.8  | -    | Second House   |
-| Uranus    | Sco  | 8.27  | R    | Fourth House   |
-| Neptune   | Sag  | 14.69 | R    | Fifth House    |
-| Pluto     | Lib  | 11.45 | R    | Fourth House   |
-| Mean_Node | Lib  | 21.49 | R    | Fourth House   |
-| True_Node | Lib  | 22.82 | R    | Fourth House   |
+| Sun       | Gem  | 17.6  | -    | Twelfth_House  |
+| Moon      | Pis  | 16.43 | -    | Ninth_House    |
+| Mercury   | Tau  | 26.29 | -    | Eleventh_House |
+| Venus     | Tau  | 2.03  | -    | Tenth_House    |
+| Mars      | Tau  | 1.79  | -    | Tenth_House    |
+| Jupiter   | Gem  | 14.61 | -    | Eleventh_House |
+| Saturn    | Leo  | 12.8  | -    | Second_House   |
+| Uranus    | Sco  | 8.27  | R    | Fourth_House   |
+| Neptune   | Sag  | 14.69 | R    | Fifth_House    |
+| Pluto     | Lib  | 11.45 | R    | Fourth_House   |
+| Mean_Node | Lib  | 21.49 | R    | Fourth_House   |
+| True_Node | Lib  | 22.82 | R    | Fourth_House   |
 +-----------+------+-------+------+----------------+
 +----------------+------+----------+
 | House          | Sign | Position |
 +----------------+------+----------+
-| First House    | Can  | 18.0     |
-| Second House   | Leo  | 9.51     |
-| Third House    | Vir  | 4.02     |
-| Fourth House   | Lib  | 3.98     |
-| Fifth House    | Sco  | 9.39     |
-| Sixth House    | Sag  | 15.68    |
-| Seventh House  | Cap  | 18.0     |
-| Eighth House   | Aqu  | 9.51     |
-| Ninth House    | Pis  | 4.02     |
-| Tenth House    | Ari  | 3.98     |
-| Eleventh House | Tau  | 9.39     |
-| Twelfth House  | Gem  | 15.68    |
+| First_House    | Can  | 18.0     |
+| Second_House   | Leo  | 9.51     |
+| Third_House    | Vir  | 4.02     |
+| Fourth_House   | Lib  | 3.98     |
+| Fifth_House    | Sco  | 9.39     |
+| Sixth_House    | Sag  | 15.68    |
+| Seventh_House  | Cap  | 18.0     |
+| Eighth_House   | Aqu  | 9.51     |
+| Ninth_House    | Pis  | 4.02     |
+| Tenth_House    | Ari  | 3.98     |
+| Eleventh_House | Tau  | 9.39     |
+| Twelfth_House  | Gem  | 15.68    |
 +----------------+------+----------+
 
 ```
 
 And if you want to export it to a file:
 
 ```bash
-$ python3 your_script_name.py > file.txt 
+$ python3 your_script_name.py > file.txt
 ```
 
 ## Other exeples of possibles usecase
 
 ```python
 # Get all aspects between two persons:
 
-from kerykeion import CompositeAspects, KrInstance
-first = KrInstance("Jack", 1990, 6, 15, 15, 15, "Roma")
-second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma")
+from kerykeion import SynastryAspects, AstrologicalSubject
+first = AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma")
+second = AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma")
 
-name = CompositeAspects(first, second)
+name = SynastryAspects(first, second)
 aspect_list = name.get_relevant_aspects()
 print(aspect_list[0])
 
 #> Generating kerykeion object for Jack...
 #> Generating kerykeion object for Jane...
 #> {'p1_name': 'Sun', 'p1_abs_pos': 84.17867971515636, 'p2_name': 'Sun', 'p2_abs_pos': 211.90472999502984, 'aspect': 'trine', 'orbit': 7.726050279873476, 'aspect_degrees': 120, 'color': '#36d100', 'aid': 6, 'diff': 127.72605027987348, 'p1': 0, 'p2': 0}
```

#### html2text {}

```diff
@@ -1,68 +1,70 @@
                             ****** Kerykeion ******
  [contributors] [stars] [forks] [visitors] [Package_version] [Supported_Python
                                    versions]
   Kerykeion is a python library for Astrology. It can calculate all the planet
 and house position, also it can calculate the aspects of a single persone or
 between two, you can set how many planets you need in the settings in the
-utility module. It also can generate an SVG of a birthchart, a composite chart
-or a transit chart. ## Installation Kerykeion is a *Python 3.9* package, make
-sure you have *Python 3.9* or above installed on your system. ```bash pip3
+utility module. It also can generate an SVG of a birthchart, a synastry chart
+or a transit chart. ## Installation Kerykeion is a _Python 3.9_ package, make
+sure you have _Python 3.9_ or above installed on your system. ```bash pip3
 install kerykeion ``` ## Usage Here some examples: ```python # Import the main
-class for creating a kerykeion instance: from kerykeion import KrInstance #
-Create a kerykeion instance: # Args: Name, year, month, day, hour, minuts,
-city, nation(optional) kanye = KrInstance("Kanye", 1977, 6, 8, 8, 45,
-"Atlanta") # Get the information about the sun in the chart: # (The position of
-the planets always starts at 0) kanye.sun #> {'name': 'Sun', 'quality':
-'Mutable', 'element': 'Air', 'sign': 'Gem', 'sign_num': 2, 'pos':
+class for creating a kerykeion instance: from kerykeion import
+AstrologicalSubject # Create a kerykeion instance: # Args: Name, year, month,
+day, hour, minuts, city, nation(optional) kanye = AstrologicalSubject("Kanye",
+1977, 6, 8, 8, 45, "Atlanta") # Get the information about the sun in the chart:
+# (The position of the planets always starts at 0) kanye.sun #> {'name': 'Sun',
+'quality': 'Mutable', 'element': 'Air', 'sign': 'Gem', 'sign_num': 2, 'pos':
 17.598992059774275, 'abs_pos': 77.59899205977428, 'emoji': 'âï¸', 'house':
-'12th House', 'retrograde': False} # Get informations about the first house:
-kanye.first_house #> {'name': 'First House', 'quality': 'Cardinal', 'element':
+'12th House', 'retrograde': False} # Get information about the first house:
+kanye.first_house #> {'name': 'First_House', 'quality': 'Cardinal', 'element':
 'Water', 'sign': 'Can', 'sign_num': 3, 'pos': 17.995779673209114, 'abs_pos':
 107.99577967320911, 'emoji': 'âï¸'} # Get element of the moon sign:
 kanye.moon.get("element") #> 'Water' ``` **To avoid connecting to GeoNames (eg.
 avoiding hourly limit or no internet connection) you should instance kerykeion
-like this:** ```python kanye = KrInstance( "Kanye", 1977, 6, 8, 8, 45, lng=50,
-lat=50, tz_str="Europe/Rome" ) ``` ## Generate a SVG Chart: ```python from
-kerykeion import KrInstance, MakeSvgInstance first = KrInstance("Jack", 1990,
-6, 15, 15, 15, "Roma") second = KrInstance("Jane", 1991, 10, 25, 21, 00,
-"Roma") # Set the type, it can be Natal, Composite or Transit name =
-MakeSvgInstance(first, chart_type="Composite", second_obj=second) name.makeSVG
-() print(len(name.aspects_list)) #> Generating kerykeion object for Jack... #>
-Generating kerykeion object for Jane... #> Jack birth location: Roma, 41.89193,
-12.51133 #> SVG Generated Correctly #> 38 ``` ![alt text](http://
-centuryboy.altervista.org/JackComposite_Chart.svg) # Report To print a report
-of all the data: ```python from kerykeion import Report, KrInstance kanye =
-KrInstance("Kanye", 1977, 6, 8, 8, 45, "Atlanta") report = Report(kanye)
-report.print_report() ``` Returns: ``` +- Kerykeion report for Kanye -+ +------
-----+------+-------------+-----------+----------+ | Date | Time | Location |
-Longitude | Latitude | +----------+------+-------------+-----------+----------
-+ | 8/6/1977 | 8:45 | Atlanta, US | -84.38798 | 33.749 | +----------+------+---
-----------+-----------+----------+ +-----------+------+-------+------+---------
--------+ | Planet | Sign | Pos. | Ret. | House | +-----------+------+-------+--
-----+----------------+ | Sun | Gem | 17.6 | - | Twelfth House | | Moon | Pis |
-16.43 | - | Ninth House | | Mercury | Tau | 26.29 | - | Eleventh House | |
-Venus | Tau | 2.03 | - | Tenth House | | Mars | Tau | 1.79 | - | Tenth House |
-| Jupiter | Gem | 14.61 | - | Eleventh House | | Saturn | Leo | 12.8 | - |
-Second House | | Uranus | Sco | 8.27 | R | Fourth House | | Neptune | Sag |
-14.69 | R | Fifth House | | Pluto | Lib | 11.45 | R | Fourth House | |
-Mean_Node | Lib | 21.49 | R | Fourth House | | True_Node | Lib | 22.82 | R |
-Fourth House | +-----------+------+-------+------+----------------+ +----------
-------+------+----------+ | House | Sign | Position | +----------------+------
-+----------+ | First House | Can | 18.0 | | Second House | Leo | 9.51 | | Third
-House | Vir | 4.02 | | Fourth House | Lib | 3.98 | | Fifth House | Sco | 9.39 |
-| Sixth House | Sag | 15.68 | | Seventh House | Cap | 18.0 | | Eighth House |
-Aqu | 9.51 | | Ninth House | Pis | 4.02 | | Tenth House | Ari | 3.98 | |
-Eleventh House | Tau | 9.39 | | Twelfth House | Gem | 15.68 | +----------------
-+------+----------+ ``` And if you want to export it to a file: ```bash $
-python3 your_script_name.py > file.txt ``` ## Other exeples of possibles
-usecase ```python # Get all aspects between two persons: from kerykeion import
-CompositeAspects, KrInstance first = KrInstance("Jack", 1990, 6, 15, 15, 15,
-"Roma") second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma") name =
-CompositeAspects(first, second) aspect_list = name.get_relevant_aspects() print
+like this:** ```python kanye = AstrologicalSubject( "Kanye", 1977, 6, 8, 8, 45,
+lng=50, lat=50, tz_str="Europe/Rome" ) ``` ## Generate a SVG Chart: ```python
+from kerykeion import AstrologicalSubject, KerykeionChartSVG first =
+AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma") second =
+AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma") # Set the type, it
+can be Natal, Synastry or Transit name = KerykeionChartSVG(first,
+chart_type="Synastry", second_obj=second) name.makeSVG() print(len
+(name.aspects_list)) #> Generating kerykeion object for Jack... #> Generating
+kerykeion object for Jane... #> Jack birth location: Roma, 41.89193, 12.51133
+#> SVG Generated Correctly #> 38 ``` ![alt text](http://
+centuryboy.altervista.org/JackSynastry_Chart.svg) # Report To print a report of
+all the data: ```python from kerykeion import Report, AstrologicalSubject kanye
+= AstrologicalSubject("Kanye", 1977, 6, 8, 8, 45, "Atlanta") report = Report
+(kanye) report.print_report() ``` Returns: ``` +- Kerykeion report for Kanye -
++ +----------+------+-------------+-----------+----------+ | Date | Time |
+Location | Longitude | Latitude | +----------+------+-------------+-----------
++----------+ | 8/6/1977 | 8:45 | Atlanta, US | -84.38798 | 33.749 | +----------
++------+-------------+-----------+----------+ +-----------+------+-------+-----
+-+----------------+ | Planet | Sign | Pos. | Ret. | House | +-----------+------
++-------+------+----------------+ | Sun | Gem | 17.6 | - | Twelfth_House | |
+Moon | Pis | 16.43 | - | Ninth_House | | Mercury | Tau | 26.29 | - |
+Eleventh_House | | Venus | Tau | 2.03 | - | Tenth_House | | Mars | Tau | 1.79 |
+- | Tenth_House | | Jupiter | Gem | 14.61 | - | Eleventh_House | | Saturn | Leo
+| 12.8 | - | Second_House | | Uranus | Sco | 8.27 | R | Fourth_House | |
+Neptune | Sag | 14.69 | R | Fifth_House | | Pluto | Lib | 11.45 | R |
+Fourth_House | | Mean_Node | Lib | 21.49 | R | Fourth_House | | True_Node | Lib
+| 22.82 | R | Fourth_House | +-----------+------+-------+------+---------------
+-+ +----------------+------+----------+ | House | Sign | Position | +----------
+------+------+----------+ | First_House | Can | 18.0 | | Second_House | Leo |
+9.51 | | Third_House | Vir | 4.02 | | Fourth_House | Lib | 3.98 | | Fifth_House
+| Sco | 9.39 | | Sixth_House | Sag | 15.68 | | Seventh_House | Cap | 18.0 | |
+Eighth_House | Aqu | 9.51 | | Ninth_House | Pis | 4.02 | | Tenth_House | Ari |
+3.98 | | Eleventh_House | Tau | 9.39 | | Twelfth_House | Gem | 15.68 | +-------
+---------+------+----------+ ``` And if you want to export it to a file:
+```bash $ python3 your_script_name.py > file.txt ``` ## Other exeples of
+possibles usecase ```python # Get all aspects between two persons: from
+kerykeion import SynastryAspects, AstrologicalSubject first =
+AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma") second =
+AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma") name =
+SynastryAspects(first, second) aspect_list = name.get_relevant_aspects() print
 (aspect_list[0]) #> Generating kerykeion object for Jack... #> Generating
 kerykeion object for Jane... #> {'p1_name': 'Sun', 'p1_abs_pos':
 84.17867971515636, 'p2_name': 'Sun', 'p2_abs_pos': 211.90472999502984,
 'aspect': 'trine', 'orbit': 7.726050279873476, 'aspect_degrees': 120, 'color':
 '#36d100', 'aid': 6, 'diff': 127.72605027987348, 'p1': 0, 'p2': 0} ``` ##
 Documentation Most of the functions and the classes are self documented by the
 types and have docstrings. An auto-generated documentation [is available here]
```

### Comparing `kerykeion-4.0a5/kerykeion/__init__.py` & `kerykeion-4.0rc1/kerykeion/__init__.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,26 +1,27 @@
+# -*- coding: utf-8 -*-
 """
     This is part of Kerykeion (C) 2023 Giacomo Battaglia
 
     Kerykeion is a python library for Astrology.
     It can calculate all the planet and house position,
     also it can calculate the aspects of a single persone or between two, you can set how many planets you
     need in the settings in the utility module.
-    It also can generate an SVG of a birthchart, a composite chart or a transit chart.
+    It also can generate an SVG of a birthchart, a synastry chart or a transit chart.
 
     Here some examples:
 
     ```python
 
     # Import the main class for creating a kerykeion instance:
-    >>> from kerykeion import KrInstance
+    >>> from kerykeion import AstrologicalSubject
 
     # Create a kerykeion instance:
     # Args: Name, year, month, day, hour, minuts, city, nation(optional)
-    >>> kanye = KrInstance("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
+    >>> kanye = AstrologicalSubject("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
 
     # Get the information about the sun in the chart:
     # (The position of the planets always starts at 0)
     >>> kanye.sun
     {'name': 'Sun', 'quality': 'Mutable', 'element': 'Air', 'sign': 'Gem', 'sign_num': 2, 'pos': 17.598992059774275, 'abs_pos': 77.59899205977428, 'emoji': '♊️', 'house': '12th House', 'retrograde': False}
 
     # Get informations about the first house:
@@ -32,45 +33,45 @@
     'Water'
 
     ```
 
     ## Generate a SVG of the birthchart:
 
     ```python
-    >>> from kerykeion import KrInstance, MakeSvgInstance
+    >>> from kerykeion import AstrologicalSubject, KerykeionChartSVG
 
-    >>> first = KrInstance("Jack", 1990, 6, 15, 15, 15, "Roma")
-    >>> second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma")
+    >>> first = AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma")
+    >>> second = AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma")
 
-    # Set the type, it can be Natal, Composite or Transit
+    # Set the type, it can be Natal, Synastry or Transit
 
-    >>> name = MakeSvgInstance(first, chart_type="Composite", second_obj=second)
+    >>> name = KerykeionChartSVG(first, chart_type="Synastry", second_obj=second)
     >>> name.makeSVG()
     >>> print(len(name.aspects_list))
     >>> Generating kerykeion object for Jack...
     Generating kerykeion object for Jane...
     Jack birth location: Roma, 41.89193, 12.51133
     SVG Generated Correctly
     38
 
     ```
 
-    ![alt text](http://centuryboy.altervista.org/JackComposite_Chart.svg)
+    ![alt text](http://centuryboy.altervista.org/JackSynastry_Chart.svg)
 
 
     ## Other exeples of possibles usecase
 
     ```python
     # Get all aspects between two persons:
 
-    >>> from kerykeion import CompositeAspects, KrInstance
-    >>> first = KrInstance("Jack", 1990, 6, 15, 15, 15, "Roma")
-    >>> second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma")
+    >>> from kerykeion import SynastryAspects, AstrologicalSubject
+    >>> first = AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma")
+    >>> second = AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma")
 
-    >>> name = CompositeAspects(first, second)
+    >>> name = SynastryAspects(first, second)
     >>> aspect_list = name.get_relevant_aspects()
     >>> print(aspect_list[0])
 
     Generating kerykeion object for Jack...
     Generating kerykeion object for Jane...
     {'p1_name': 'Sun', 'p1_abs_pos': 84.17867971515636, 'p2_name': 'Sun', 'p2_abs_pos': 211.90472999502984, 'aspect': 'trine', 'orbit': 7.726050279873476, 'aspect_degrees': 120, 'color': '#36d100', 'aid': 6, 'diff': 127.72605027987348, 'p1': 0, 'p2': 0}
 
@@ -92,17 +93,16 @@
     You can clone this repository or download a zip file using the right side buttons.
 
     ## Contributing
 
     Feel free to contribute to the code!
 
 """
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
 
 # Local
-from .kr_instance import KrInstance
-from .charts.charts_svg import MakeSvgInstance
+from .astrological_subject import AstrologicalSubject
+from .charts.kerykeion_chart_svg import KerykeionChartSVG
 from .kr_types import *
 from .relationship_score import RelationshipScore
-from .aspects import CompositeAspects, NatalAspects
+from .aspects import SynastryAspects, NatalAspects
 from .report import Report
+from .settings import KerykeionSettingsModel, get_settings_dict
```

### Comparing `kerykeion-4.0a5/kerykeion/aspects/composite_aspects.py` & `kerykeion-4.0rc1/kerykeion/aspects/synastry_aspects.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,55 +1,44 @@
+# -*- coding: utf-8 -*-
 """
     This is part of Kerykeion (C) 2023 Giacomo Battaglia
 """
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
 
-from kerykeion import KrInstance
+from kerykeion import AstrologicalSubject
 from pathlib import Path
 from typing import Union
 
 from kerykeion.aspects.natal_aspects import NatalAspects
 
 
-class CompositeAspects(NatalAspects):
+class SynastryAspects(NatalAspects):
     """
     Generates an object with all the aspects between two persons.
     """
 
     def __init__(
         self,
-        kr_object_one: KrInstance,
-        kr_object_two: KrInstance,
+        kr_object_one: AstrologicalSubject,
+        kr_object_two: AstrologicalSubject,
         new_settings_file: Union[str, Path, None] = None,
     ):
         self.first_user = kr_object_one
         self.second_user = kr_object_two
 
         self.new_settings_file = new_settings_file
         self._parse_json_settings()
 
-        if not hasattr(self.first_user, "sun"):
-            self.first_user.__get_all()
-
-        if not hasattr(self.second_user, "sun"):
-            self.second_user.__get_all()
-
-        self.first_init_point_list = (
-            self.first_user.planets_list + self.first_user.houses_list
-        )
-        self.second_init_point_list = (
-            self.second_user.planets_list + self.second_user.houses_list
-        )
+        self.first_init_point_list = self.first_user.planets_list + self.first_user.houses_list
+        self.second_init_point_list = self.second_user.planets_list + self.second_user.houses_list
 
     def get_all_aspects(self):
         """
         Return all the aspects of the points in the natal chart in a dictionary,
         first all the individual aspects of each planet, second the aspects
-        whitout repetitions.
+        whiteout repetitions.
         """
 
         f_1 = self.filter_by_settings(self.first_init_point_list)
         f_2 = self.filter_by_settings(self.second_init_point_list)
 
         self.all_aspects_list = []
 
@@ -80,13 +69,17 @@
 
                     self.all_aspects_list.append(d_asp)
 
         return self.all_aspects_list
 
 
 if __name__ == "__main__":
-    john = KrInstance("John", 1940, 10, 9, 10, 30, "Liverpool")
-    yoko = KrInstance("Yoko", 1933, 2, 18, 10, 30, "Tokyo")
+    john = AstrologicalSubject("John", 1940, 10, 9, 10, 30, "Liverpool")
+    yoko = AstrologicalSubject("Yoko", 1933, 2, 18, 10, 30, "Tokyo")
+
+    synastry_aspects = SynastryAspects(john, yoko)
 
-    composite_aspects = CompositeAspects(john, yoko)
+    # All aspects
+    print(synastry_aspects.get_all_aspects())
 
-    print(composite_aspects.get_all_aspects())
+    # Relevant aspects
+    print(synastry_aspects.get_relevant_aspects())
```

### Comparing `kerykeion-4.0a5/kerykeion/aspects/natal_aspects.py` & `kerykeion-4.0rc1/kerykeion/aspects/natal_aspects.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,179 +1,167 @@
+# -*- coding: utf-8 -*-
 """
     This is part of Kerykeion (C) 2023 Giacomo Battaglia
 """
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
 
 import json
 from pathlib import Path
-from kerykeion import KrInstance
+from kerykeion import AstrologicalSubject
 from swisseph import difdeg2n
 from typing import Union
-
-from kerykeion.aspects.aspects_settings import DEFAULT_KR_CONFIG_FILE
+from kerykeion.settings.kerykeion_settings import get_settings_dict
 
 
 class NatalAspects:
     """
     Generates an object with all the aspects of a birthcart.
     """
 
-    def __init__(
-        self, kr_object: KrInstance, new_settings_file: Union[str, Path, None] = None
-    ):
+    def __init__(self, kr_object: AstrologicalSubject, new_settings_file: Union[str, Path, None] = None):
         self.user = kr_object
         self.new_settings_file = new_settings_file
         self._parse_json_settings()
 
-        if not hasattr(self.user, "sun"):
-            self.user.__get_all()
-
         self.init_point_list = self.user.planets_list + self.user.houses_list
 
     def _parse_json_settings(self):
         # Load settings file
 
-        if not self.new_settings_file:
-            settings_file = DEFAULT_KR_CONFIG_FILE
-        else:
-            settings_file = Path(self.new_settings_file)
-
-        with open(settings_file, "r", encoding="utf-8", errors="ignore") as f:
-            settings = json.load(f)
+        settings = get_settings_dict(
+            self.new_settings_file,
+        )
 
-        self.colors_settings = settings["colors"]
         self.planets_settings = settings["celestial_points"]
         self.aspects_settings = settings["aspects"]
-        self.axes_orbit_settings = settings["axes_orbit"]
+        self.axes_orbit_settings = settings["general_settings"]["axes_orbit"]
 
     def asp_calc(self, point_one, point_two):
         """
         Utility function.
         It calculates the aspects between the 2 points.
         Args: first point, second point.
         """
 
         distance = abs(difdeg2n(point_one, point_two))
         diff = abs(point_one - point_two)
 
         if int(distance) <= self.aspects_settings[0]["orb"]:
             name = self.aspects_settings[0]["name"]
             aspect_degrees = self.aspects_settings[0]["degree"]
-            color = self.colors_settings["aspect_0"]
+            color = self.aspects_settings[0]["color"]
             verdict = True
             aid = 0
 
         elif (
             (self.aspects_settings[1]["degree"] - self.aspects_settings[1]["orb"])
             <= int(distance)
             <= (self.aspects_settings[1]["degree"] + self.aspects_settings[1]["orb"])
         ):
             name = self.aspects_settings[1]["name"]
             aspect_degrees = self.aspects_settings[1]["degree"]
-            color = self.colors_settings["aspect_30"]
+            color = self.aspects_settings[1]["color"]
             verdict = True
             aid = 1
 
         elif (
             (self.aspects_settings[2]["degree"] - self.aspects_settings[2]["orb"])
             <= int(distance)
             <= (self.aspects_settings[2]["degree"] + self.aspects_settings[2]["orb"])
         ):
             name = self.aspects_settings[2]["name"]
             aspect_degrees = self.aspects_settings[2]["degree"]
-            color = self.colors_settings["aspect_45"]
+            color = self.aspects_settings[2]["color"]
             verdict = True
             aid = 2
 
         elif (
             (self.aspects_settings[3]["degree"] - self.aspects_settings[3]["orb"])
             <= int(distance)
             <= (self.aspects_settings[3]["degree"] + self.aspects_settings[3]["orb"])
         ):
             name = self.aspects_settings[3]["name"]
             aspect_degrees = self.aspects_settings[3]["degree"]
-            color = self.colors_settings["aspect_60"]
+            color = self.aspects_settings[3]["color"]
             verdict = True
             aid = 3
 
         elif (
             (self.aspects_settings[4]["degree"] - self.aspects_settings[4]["orb"])
             <= int(distance)
             <= (self.aspects_settings[4]["degree"] + self.aspects_settings[4]["orb"])
         ):
             name = self.aspects_settings[4]["name"]
             aspect_degrees = self.aspects_settings[4]["degree"]
-            color = self.colors_settings["aspect_72"]
+            color = self.aspects_settings[4]["color"]
             verdict = True
             aid = 4
 
         elif (
             (self.aspects_settings[5]["degree"] - self.aspects_settings[5]["orb"])
             <= int(distance)
             <= (self.aspects_settings[5]["degree"] + self.aspects_settings[5]["orb"])
         ):
             name = self.aspects_settings[5]["name"]
             aspect_degrees = self.aspects_settings[5]["degree"]
-            color = self.colors_settings["aspect_90"]
+            color = self.aspects_settings[5]["color"]
             verdict = True
             aid = 5
 
         elif (
             (self.aspects_settings[6]["degree"] - self.aspects_settings[6]["orb"])
             <= int(distance)
             <= (self.aspects_settings[6]["degree"] + self.aspects_settings[6]["orb"])
         ):
             name = self.aspects_settings[6]["name"]
             aspect_degrees = self.aspects_settings[6]["degree"]
-            color = self.colors_settings["aspect_120"]
+            color = self.aspects_settings[6]["color"]
             verdict = True
             aid = 6
 
         elif (
             (self.aspects_settings[7]["degree"] - self.aspects_settings[7]["orb"])
             <= int(distance)
             <= (self.aspects_settings[7]["degree"] + self.aspects_settings[7]["orb"])
         ):
             name = self.aspects_settings[7]["name"]
             aspect_degrees = self.aspects_settings[7]["degree"]
-            color = self.colors_settings["aspect_135"]
+            color = self.aspects_settings[7]["color"]
             verdict = True
             aid = 7
 
         elif (
             (self.aspects_settings[8]["degree"] - self.aspects_settings[8]["orb"])
             <= int(distance)
             <= (self.aspects_settings[8]["degree"] + self.aspects_settings[8]["orb"])
         ):
             name = self.aspects_settings[8]["name"]
             aspect_degrees = self.aspects_settings[8]["degree"]
-            color = self.colors_settings["aspect_144"]
+            color = self.aspects_settings[8]["color"]
             verdict = True
             aid = 8
 
         elif (
             (self.aspects_settings[9]["degree"] - self.aspects_settings[9]["orb"])
             <= int(distance)
             <= (self.aspects_settings[9]["degree"] + self.aspects_settings[9]["orb"])
         ):
             name = self.aspects_settings[9]["name"]
             aspect_degrees = self.aspects_settings[9]["degree"]
-            color = self.colors_settings["aspect_150"]
+            color = self.aspects_settings[9]["color"]
             verdict = True
             aid = 9
 
         elif (
             (self.aspects_settings[10]["degree"] - self.aspects_settings[10]["orb"])
             <= int(distance)
             <= (self.aspects_settings[10]["degree"] + self.aspects_settings[10]["orb"])
         ):
             name = self.aspects_settings[10]["name"]
             aspect_degrees = self.aspects_settings[10]["degree"]
-            color = self.colors_settings["aspect_180"]
+            color = self.aspects_settings[10]["color"]
             verdict = True
             aid = 10
 
         else:
             verdict = False
             name = None
             distance = 0
@@ -193,28 +181,28 @@
 
     def p_id_decoder(self, name):
         """
         Check if the name of the planet is the same in the settings and return
         the correct id for the planet.
         """
         str_name = str(name)
-        for a in self.planets_settings:
-            if a["name"] == str_name:
-                result = a["id"]
+        for planet in self.planets_settings:
+            if planet["name"] == str_name:
+                result = planet["id"]
                 return result
 
     def filter_by_settings(self, init_point_list):
         """
         Creates a list of all the desired
         points filtering by the settings.
         """
 
         set_points_name = []
         for p in self.planets_settings:
-            if p["visible"]:
+            if p["is_active"]:
                 set_points_name.append(p["name"])
 
         point_list = []
         for l in init_point_list:
             if l["name"] in set_points_name:
                 point_list.append(l)
 
@@ -268,22 +256,22 @@
         or the numbers of the houses.
         """
 
         self.get_all_aspects()
 
         aspects_filtered = []
         for a in self.all_aspects_list:
-            if self.aspects_settings[a["aid"]]["visible"] == True:
+            if self.aspects_settings[a["aid"]]["is_active"] == True:
                 aspects_filtered.append(a)
 
         axes_list = [
-            "First House",
-            "Tenth House",
-            "Seventh House",
-            "Fourth House",
+            "First_House",
+            "Tenth_House",
+            "Seventh_House",
+            "Fourth_House",
         ]
         counter = 0
 
         aspects_list_subtract = []
         for a in aspects_filtered:
             counter += 1
             name_p1 = str(a["p1_name"])
@@ -293,21 +281,25 @@
                 if abs(a["orbit"]) >= self.axes_orbit_settings:
                     aspects_list_subtract.append(a)
 
             elif name_p2 in axes_list:
                 if abs(a["orbit"]) >= self.axes_orbit_settings:
                     aspects_list_subtract.append(a)
 
-        self.aspects = [
-            item for item in aspects_filtered if item not in aspects_list_subtract
-        ]
+        self.aspects = [item for item in aspects_filtered if item not in aspects_list_subtract]
 
         return self.aspects
 
 
 if __name__ == "__main__":
-    johnny = KrInstance("Johnny Depp", 1963, 6, 9, 0, 0, "Owensboro", "US")
-    aspects = NatalAspects(johnny).get_all_aspects()
+    johnny = AstrologicalSubject("Johnny Depp", 1963, 6, 9, 0, 0, "Owensboro", "US")
 
+    # All aspects
+    aspects = NatalAspects(johnny).get_all_aspects()
     print(aspects)
 
+    print("\n")
+
+    # Relevant aspects
+    aspects = NatalAspects(johnny).get_relevant_aspects()
+    print(aspects)
```

### Comparing `kerykeion-4.0a5/kerykeion/charts/charts_svg.py` & `kerykeion-4.0rc1/kerykeion/charts/kerykeion_chart_svg.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,212 +1,190 @@
-#!/usr/bin/env python3
 # -*- coding: utf-8 -*-
+"""
+    This is part of Kerykeion (C) 2023 Giacomo Battaglia
+"""
 
-# * TODO: Change the label for language in 2 objects, one for IT and one for ENG.
-# * Then change the label for planets like this: planet["label"] => planet[language]
 
-import json
-import math
 import pytz
 
 from datetime import datetime
-from kerykeion.aspects.composite_aspects import CompositeAspects
+from kerykeion.settings.kerykeion_settings import get_settings_dict
+from kerykeion.aspects.synastry_aspects import SynastryAspects
 from kerykeion.aspects.natal_aspects import NatalAspects
-from kerykeion.kr_instance import KrInstance
+from kerykeion.astrological_subject import AstrologicalSubject
 from kerykeion.kr_types import KerykeionException, ChartType
+from kerykeion.kr_types.chart_types import ChartTemplateModel
+from kerykeion.charts.charts_utils import decHourJoin, degreeDiff, offsetToTz, sliceToX, sliceToY
+from logging import getLogger, basicConfig, StreamHandler, DEBUG
 from pathlib import Path
 from string import Template
 from typing import Union
 
-# calculation and svg drawing class
+logger = getLogger(__name__)
+basicConfig(level=DEBUG)
 
 
-class MakeSvgInstance:
+class KerykeionChartSVG:
     """
-    Creates the instance that can genearte the chart with the
+    Creates the instance that can generate the chart with the
     function makeSVG().
 
-    There are 2 templates, the extended (default) which has all the
-    information and the basic, which has just the chart.
-
     Parameters:
         - first_obj: First kerykeion object
-        - chart_type: Natal, Transit, Composite (Default: Type="Natal")
+        - chart_type: Natal, ExternalNatal, Transit, Synastry (Default: Type="Natal").
         - second_obj: Second kerykeion object (Not required if type is Natal)
         - new_output_directory: Set the output directory (default: output_directory)
-        - template_type: set the template type to include or not the aspects grid, default: extended)
         - lang: language settings (default: "EN")
         - new_settings_file: Set the settings file (default: kr.config.json)
     """
 
+    first_obj: AstrologicalSubject
+    second_obj: Union[AstrologicalSubject, None]
+    chart_type: ChartType
+    new_output_directory: Union[str, None]
+    new_settings_file: Union[str, Path, None]
+    output_directory: Path
+
     def __init__(
-            self,
-            first_obj: KrInstance,
-            chart_type: ChartType = "Natal",
-            second_obj: Union[KrInstance, None] = None,
-            new_output_directory: Union[str, None] = None,
-            template_type: str = "extended",
-            lang: str = "EN",
-            new_settings_file: Union[str, Path, None] = None
+        self,
+        first_obj: AstrologicalSubject,
+        chart_type: ChartType = "Natal",
+        second_obj: Union[AstrologicalSubject, None] = None,
+        new_output_directory: Union[str, None] = None,
+        new_settings_file: Union[str, Path, None] = None,
     ):
-
         # Directories:
-        DATADIR = Path(__file__).parent
+        DATA_DIR = Path(__file__).parent
         self.homedir = Path.home()
+        self.new_settings_file = new_settings_file
 
         if new_output_directory:
             self.output_directory = Path(new_output_directory)
         else:
             self.output_directory = self.homedir
 
-        # Template types:
-        if template_type == "basic":
-            self.xml_svg = DATADIR / 'templates/basic.xml'
-        else:
-            self.xml_svg = DATADIR / 'templates/extended.xml'
+        self.xml_svg = DATA_DIR / "templates/chart.xml"
 
         # SVG Width
         self.natal_width = 772.2
         self.full_width = 1200
 
-        # Settings file:
-        if not new_settings_file:
-            self.settings_file = DATADIR.parent / 'kr.config.json'
-        else:
-            self.settings_file = Path(new_settings_file)
-
-        self.parse_json_settings(self.settings_file, lang)
+        self.parse_json_settings(new_settings_file)
         self.chart_type = chart_type
 
         # Kerykeion instance
         self.user = first_obj
-        if not hasattr(self.user, "sun"):
-            print(f"Generating kerykeion object for {self.user.name}...")
-            self.user.__get_all()
 
         # Make a list for the absolute degrees of the points of the graphic.
-
-        self.points_deg_ut = self.user.planets_degrees + [self.user.houses_degree_ut[0],
-                                                          self.user.houses_degree_ut[9], self.user.houses_degree_ut[6],
-                                                          self.user.houses_degree_ut[3]]
+        self.points_deg_ut = self.user.planets_degrees_ut + [
+            self.user.houses_degree_ut[0],
+            self.user.houses_degree_ut[9],
+            self.user.houses_degree_ut[6],
+            self.user.houses_degree_ut[3],
+        ]
 
         # Make a list of the relative degrees of the points in the graphic.
-
         self.points_deg = []
         for planet in self.user.planets_list:
             self.points_deg.append(planet["position"])
 
         self.points_deg = self.points_deg + [
             self.user.houses_list[0]["position"],
             self.user.houses_list[9]["position"],
             self.user.houses_list[6]["position"],
-            self.user.houses_list[3]["position"]
+            self.user.houses_list[3]["position"],
         ]
 
-        # Make list of the poits sign.
-
+        # Make list of the points sign
         self.points_sign = []
 
         for planet in self.user.planets_list:
             self.points_sign.append(planet["sign_num"])
 
         self.points_sign = self.points_sign + [
             self.user.houses_list[0]["sign_num"],
             self.user.houses_list[9]["sign_num"],
             self.user.houses_list[6]["sign_num"],
-            self.user.houses_list[3]["sign_num"]
+            self.user.houses_list[3]["sign_num"],
         ]
 
-        # Make a list of poits if they are retrograde or not.
-
+        # Make a list of points if they are retrograde or not.
         self.points_retrograde = []
 
         for planet in self.user.planets_list:
             self.points_retrograde.append(planet["retrograde"])
 
-        self.points_retrograde = self.points_retrograde + [
-            False,
-            False,
-            False,
-            False
-        ]
+        self.points_retrograde = self.points_retrograde + [False, False, False, False]
 
         # Makes the sign number list.
 
         self.houses_sign_graph = []
         for h in self.user.houses_list:
-            self.houses_sign_graph.append(h['sign_num'])
+            self.houses_sign_graph.append(h["sign_num"])
 
-        if self.chart_type == "Natal":
-            natal_aspects_instance = NatalAspects(
-                self.user, new_settings_file=self.settings_file)
+        if self.chart_type == "Natal" or self.chart_type == "ExternalNatal":
+            natal_aspects_instance = NatalAspects(self.user, new_settings_file=self.new_settings_file)
             self.aspects_list = natal_aspects_instance.get_relevant_aspects()
 
-        if (self.chart_type == "Transit" or self.chart_type == "Composite"):  # TODO: If not second should exit
-
+        # TODO: If not second should exit
+        if self.chart_type == "Transit" or self.chart_type == "Synastry":
             if not second_obj:
-                raise KerykeionException(
-                    "Second object is required for Transit or Composite charts.")
+                raise KerykeionException("Second object is required for Transit or Synastry charts.")
 
             # Kerykeion instance
             self.t_user = second_obj
 
-            if not hasattr(self.t_user, "sun"):
-                print(f"Generating kerykeion object for {self.t_user.name}...")
-                self.t_user.__get_all()
-
             # Make a list for the absolute degrees of the points of the graphic.
 
-            self.t_points_deg_ut = self.t_user.planets_degrees + [
+            self.t_points_deg_ut = self.t_user.planets_degrees_ut + [
                 self.t_user.houses_degree_ut[0],
                 self.t_user.houses_degree_ut[9],
                 self.t_user.houses_degree_ut[6],
-                self.t_user.houses_degree_ut[3]
+                self.t_user.houses_degree_ut[3],
             ]
 
             # Make a list of the relative degrees of the points in the graphic.
 
             self.t_points_deg = []
             for planet in self.t_user.planets_list:
                 self.t_points_deg.append(planet["position"])
 
             self.t_points_deg = self.t_points_deg + [
                 self.t_user.houses_list[0]["position"],
                 self.t_user.houses_list[9]["position"],
                 self.t_user.houses_list[6]["position"],
-                self.t_user.houses_list[3]["position"]
+                self.t_user.houses_list[3]["position"],
             ]
 
             # Make list of the poits sign.
 
             self.t_points_sign = []
 
             for planet in self.t_user.planets_list:
                 self.t_points_sign.append(planet["sign_num"])
 
             self.t_points_sign = self.t_points_sign + [
                 self.t_user.houses_list[0]["sign_num"],
                 self.t_user.houses_list[9]["sign_num"],
                 self.t_user.houses_list[6]["sign_num"],
-                self.t_user.houses_list[3]["sign_num"]
+                self.t_user.houses_list[3]["sign_num"],
             ]
 
             # Make a list of poits if they are retrograde or not.
 
             self.t_points_retrograde = []
 
             for planet in self.t_user.planets_list:
                 self.t_points_retrograde.append(planet["retrograde"])
 
-            self.t_points_retrograde = self.t_points_retrograde + [False,
-                                                                   False, False, False]
+            self.t_points_retrograde = self.t_points_retrograde + [False, False, False, False]
 
             self.t_houses_sign_graph = []
             for h in self.t_user.houses_list:
-                self.t_houses_sign_graph.append(h['sign_num'])
+                self.t_houses_sign_graph.append(h["sign_num"])
 
         # screen size
         if self.chart_type == "Natal":
             self.screen_width = 772.2
         else:
             self.screen_width = 1200
         self.screen_height = 772.2
@@ -214,372 +192,386 @@
         # check for home
         self.home_location = self.user.city
         self.home_geolat = self.user.lat
         self.home_geolon = self.user.lng
         self.home_countrycode = self.user.nation
         self.home_timezonestr = self.user.tz_str
 
-        print(f'{self.user.name} birth location: {self.home_location}, {self.home_geolat}, {self.home_geolon}')
+        print(f"{self.user.name} birth location: {self.home_location}, {self.home_geolat}, {self.home_geolon}")
 
         # default location
         self.location = self.home_location
         self.geolat = float(self.home_geolat)
         self.geolon = float(self.home_geolon)
         self.countrycode = self.home_countrycode
         self.timezonestr = self.home_timezonestr
 
         # current datetime
         now = datetime.now()
 
         # aware datetime object
-        dt_input = datetime(
-            now.year, now.month, now.day, now.hour, now.minute, now.second)
+        dt_input = datetime(now.year, now.month, now.day, now.hour, now.minute, now.second)
         dt = pytz.timezone(self.timezonestr).localize(dt_input)
 
         # naive utc datetime object
-        dt_utc = dt.replace(tzinfo=None) - dt.utcoffset() # type: ignore
+        dt_utc = dt.replace(tzinfo=None) - dt.utcoffset()  # type: ignore
 
         # Default
         self.name = self.user.name
         self.charttype = self.chart_type
         self.year = self.user.utc.year
         self.month = self.user.utc.month
         self.day = self.user.utc.day
-        self.hour = self.user.utc.hour + self.user.utc.minute/100
-        self.timezone = self.__offsetToTz(dt.utcoffset())
+        self.hour = self.user.utc.hour + self.user.utc.minute / 100
+        self.timezone = offsetToTz(dt.utcoffset())
         self.altitude = 25
         self.geonameid = None
 
         # Transit
 
         if self.chart_type == "Transit":
             self.t_geolon = self.geolon
             self.t_geolat = self.geolat
             self.t_altitude = self.altitude
-            self.t_name = self.language_settings['transit_name']
+            self.t_name = self.language_settings["transit_name"]
             self.t_year = dt_utc.year
             self.t_month = dt_utc.month
             self.t_day = dt_utc.day
-            self.t_hour = self.__decHourJoin(
-                dt_utc.hour, dt_utc.minute, dt_utc.second)
-            self.t_timezone = self.__offsetToTz(dt.utcoffset())
+            self.t_hour = decHourJoin(dt_utc.hour, dt_utc.minute, dt_utc.second)
+            self.t_timezone = offsetToTz(dt.utcoffset())
             self.t_altitude = 25
             self.t_geonameid = None
 
         # configuration
         # ZOOM 1 = 100%
         self.zoom = 1
 
-        # 12 zodiacs
-        self.zodiac = ['aries', 'taurus', 'gemini', 'cancer', 'leo', 'virgo',
-                       'libra', 'scorpio', 'sagittarius', 'capricorn', 'aquarius', 'pisces']
-        self.zodiac_short = ['Ari', 'Tau', 'Gem', 'Cnc', 'Leo',
-                             'Vir', 'Lib', 'Sco', 'Sgr', 'Cap', 'Aqr', 'Psc']
-        self.zodiac_color = ['#482900', '#6b3d00', '#5995e7', '#2b4972', '#c54100',
-                             '#2b286f', '#69acf1', '#ffd237', '#ff7200', '#863c00', '#4f0377', '#6cbfff']
-        self.zodiac_element = ['fire', 'earth', 'air', 'water', 'fire',
-                               'earth', 'air', 'water', 'fire', 'earth', 'air', 'water']
-
-        # get color configuration
+        self.zodiac = (
+            {"name": "aries", "element": "fire"},
+            {"name": "taurus", "element": "earth"},
+            {"name": "gemini", "element": "air"},
+            {"name": "cancer", "element": "water"},
+            {"name": "leo", "element": "fire"},
+            {"name": "virgo", "element": "earth"},
+            {"name": "libra", "element": "air"},
+            {"name": "scorpio", "element": "water"},
+            {"name": "sagittarius", "element": "fire"},
+            {"name": "capricorn", "element": "earth"},
+            {"name": "aquarius", "element": "air"},
+            {"name": "pisces", "element": "water"},
+        )
 
         # Immediately generate template.
         self.template = self.makeTemplate()
 
-    # draw transit ring
-    def __transitRing(self, r):
-        out = '<circle cx="%s" cy="%s" r="%s" style="fill: none; stroke: %s; stroke-width: 36px; stroke-opacity: .4;"/>' % (
-            r, r, r-18, self.colors_settings['paper_1'])
-        out += '<circle cx="%s" cy="%s" r="%s" style="fill: none; stroke: %s; stroke-width: 1px; stroke-opacity: .6;"/>' % (
-            r, r, r, self.colors_settings['zodiac_transit_ring_3'])
+    def set_output_directory(self, dir_path):
+        """
+        Sets the output direcotry and returns it's path.
+        """
+        self.output_directory = Path(dir_path)
+        dir_string = f"Output direcotry set to: {self.output_directory}"
+        return print(dir_string)
+
+    def parse_json_settings(self, settings_file):
+        """
+        Parse the settings file.
+        """
+        settings = get_settings_dict(settings_file)
+
+        language = settings["general_settings"]["language"]
+        self.language_settings = settings["language_settings"].get(language, "EN")
+        self.chart_colors_settings = settings["chart_colors"]
+        self.planets_settings = settings["celestial_points"]
+        self.aspects_settings = settings["aspects"]
+        self.planet_in_zodiac_extra_points = settings["general_settings"]["planet_in_zodiac_extra_points"]
+
+    def _transitRing(self, r) -> str:
+        """
+        Draws the transit ring.
+        """
+        radius_offset = 18
+
+        out = f'<circle cx="{r}" cy="{r}" r="{r - radius_offset}" style="fill: none; stroke: {self.chart_colors_settings["paper_1"]}; stroke-width: 36px; stroke-opacity: .4;"/>'
+        out += f'<circle cx="{r}" cy="{r}" r="{r}" style="fill: none; stroke: {self.chart_colors_settings["zodiac_transit_ring_3"]}; stroke-width: 1px; stroke-opacity: .6;"/>'
+
         return out
 
-    # draw degree ring
-    def __degreeRing(self, r):
-        out = ''
+    def _degreeRing(self, r) -> str:
+        """
+        Draws the degree ring.
+        """
+        out = ""
         for i in range(72):
-            offset = float(i*5) - self.houses_degree_ut[6]
+            offset = float(i * 5) - self.user.houses_degree_ut[6]
             if offset < 0:
                 offset = offset + 360.0
             elif offset > 360:
                 offset = offset - 360.0
-            x1 = self.__sliceToX(0, r-self.c1, offset) + self.c1
-            y1 = self.__sliceToY(0, r-self.c1, offset) + self.c1
-            x2 = self.__sliceToX(0, r+2-self.c1, offset) - 2 + self.c1
-            y2 = self.__sliceToY(0, r+2-self.c1, offset) - 2 + self.c1
-            out += '<line x1="%s" y1="%s" x2="%s" y2="%s" style="stroke: %s; stroke-width: 1px; stroke-opacity:.9;"/>' % (
-                x1, y1, x2, y2, self.colors_settings['paper_0'])
+            x1 = sliceToX(0, r - self.c1, offset) + self.c1
+            y1 = sliceToY(0, r - self.c1, offset) + self.c1
+            x2 = sliceToX(0, r + 2 - self.c1, offset) - 2 + self.c1
+            y2 = sliceToY(0, r + 2 - self.c1, offset) - 2 + self.c1
+
+            out += f'<line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}" style="stroke: {self.chart_colors_settings["paper_0"]}; stroke-width: 1px; stroke-opacity:.9;"/>'
+
         return out
 
-    def __degreeTransitRing(self, r):
-        out = ''
+    def _degreeTransitRing(self, r):
+        out = ""
         for i in range(72):
-            offset = float(i*5) - self.houses_degree_ut[6]
+            offset = float(i * 5) - self.user.houses_degree_ut[6]
             if offset < 0:
                 offset = offset + 360.0
             elif offset > 360:
                 offset = offset - 360.0
-            x1 = self.__sliceToX(0, r, offset)
-            y1 = self.__sliceToY(0, r, offset)
-            x2 = self.__sliceToX(0, r+2, offset) - 2
-            y2 = self.__sliceToY(0, r+2, offset) - 2
-            out += '<line x1="%s" y1="%s" x2="%s" y2="%s" style="stroke: #F00; stroke-width: 1px; stroke-opacity:.9;"/>' % (
-                x1, y1, x2, y2)
+            x1 = sliceToX(0, r, offset)
+            y1 = sliceToY(0, r, offset)
+            x2 = sliceToX(0, r + 2, offset) - 2
+            y2 = sliceToY(0, r + 2, offset) - 2
+            out += f'<line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}" style="stroke: #F00; stroke-width: 1px; stroke-opacity:.9;"/>'
+
         return out
 
-    # floating latitude an longitude to string
-    def __lat2str(self, coord):
+    def _lat2str(self, coord):
+        """Converts a floating point latitude to string with
+        degree, minutes and seconds and the appropriate sign
+        (north or south). Eg. 52.1234567 -> 52°7'25" N
+
+        Args:
+            coord (float): latitude in floating point format
+        Returns:
+            str: latitude in string format with degree, minutes,
+             seconds and sign (N/S)
+        """
+
         sign = self.language_settings["north"]
         if coord < 0.0:
             sign = self.language_settings["south"]
             coord = abs(coord)
         deg = int(coord)
         min = int((float(coord) - deg) * 60)
         sec = int(round(float(((float(coord) - deg) * 60) - min) * 60.0))
-        return "%s°%s'%s\" %s" % (deg, min, sec, sign)
+        return f"{deg}°{min}'{sec}\" {sign}"
+
+    def _lon2str(self, coord):
+        """Converts a floating point longitude to string with
+        degree, minutes and seconds and the appropriate sign
+        (east or west). Eg. 52.1234567 -> 52°7'25" E
+
+        Args:
+            coord (float): longitude in floating point format
+        Returns:
+            str: longitude in string format with degree, minutes,
+                seconds and sign (E/W)
+        """
 
-    def __lon2str(self, coord):
         sign = self.language_settings["east"]
         if coord < 0.0:
             sign = self.language_settings["west"]
             coord = abs(coord)
         deg = int(coord)
         min = int((float(coord) - deg) * 60)
         sec = int(round(float(((float(coord) - deg) * 60) - min) * 60.0))
-        return "%s°%s'%s\" %s" % (deg, min, sec, sign)
-
-    # join hour, minutes, seconds, timezone integere to hour float
-    def __decHourJoin(self, inH, inM, inS):
-        dh = float(inH)
-        dm = float(inM)/60
-        ds = float(inS)/3600
-        output = dh + dm + ds
-        return output
-
-    # Datetime offset to float in hours
-    def __offsetToTz(self, dtoffset):
-        dh = float(dtoffset.days * 24)
-        sh = float(dtoffset.seconds / 3600.0)
-        output = dh + sh
-        return output
+        return f"{deg}°{min}'{sec}\" {sign}"
 
-    # degree difference
-    def __degreeDiff(self, a, b):
-        out = float()
-        if a > b:
-            out = a - b
-        if a < b:
-            out = b-a
-        if out > 180.0:
-            out = 360.0-out
-        return out
+    def _dec2deg(self, dec, type="3"):
+        """Coverts decimal float to degrees in format
+        a°b'c".
+        """
 
-    # decimal to degrees (a°b'c")
-    def __dec2deg(self, dec, type="3"):
         dec = float(dec)
         a = int(dec)
-        a_new = (dec-float(a)) * 60.0
+        a_new = (dec - float(a)) * 60.0
         b_rounded = int(round(a_new))
         b = int(a_new)
-        c = int(round((a_new-float(b))*60.0))
+        c = int(round((a_new - float(b)) * 60.0))
         if type == "3":
-            out = '%(#1)02d&#176;%(#2)02d&#39;%(#3)02d&#34;' % {
-                '#1': a, '#2': b, '#3': c}
+            out = f"{a:02d}&#176;{b:02d}&#39;{c:02d}&#34;"
         elif type == "2":
-            out = '%(#1)02d&#176;%(#2)02d&#39;' % {'#1': a, '#2': b_rounded}
+            out = f"{a:02d}&#176;{b_rounded:02d}&#39;"
         elif type == "1":
-            out = '%(#1)02d&#176;' % {'#1': a}
+            out = f"{a:02d}&#176;"
+        else:
+            raise KerykeionException(f"Wrong type: {type}, it must be 1, 2 or 3.")
         return str(out)
 
-    # draw svg aspects: ring, aspect ring, degreeA degreeB
-    def __drawAspect(self, r, ar, degA, degB, color):
-        offset = (int(self.houses_degree_ut[6]) / -1) + int(degA)
-        x1 = self.__sliceToX(0, ar, offset) + (r-ar)
-        y1 = self.__sliceToY(0, ar, offset) + (r-ar)
-        offset = (int(self.houses_degree_ut[6]) / -1) + int(degB)
-        x2 = self.__sliceToX(0, ar, offset) + (r-ar)
-        y2 = self.__sliceToY(0, ar, offset) + (r-ar)
-        out = '            <line x1="'+str(x1)+'" y1="'+str(y1)+'" x2="'+str(x2)+'" y2="'+str(
-            y2)+'" style="stroke: '+color+'; stroke-width: 1; stroke-opacity: .9;"/>'
-        return out
+    def _drawAspect(self, r, ar, degA, degB, color):
+        """
+        Draws svg aspects: ring, aspect ring, degreeA degreeB
+        """
+        offset = (int(self.user.houses_degree_ut[6]) / -1) + int(degA)
+        x1 = sliceToX(0, ar, offset) + (r - ar)
+        y1 = sliceToY(0, ar, offset) + (r - ar)
+        offset = (int(self.user.houses_degree_ut[6]) / -1) + int(degB)
+        x2 = sliceToX(0, ar, offset) + (r - ar)
+        y2 = sliceToY(0, ar, offset) + (r - ar)
+        out = f'            <line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}" style="stroke: {color}; stroke-width: 1; stroke-opacity: .9;"/>'
 
-    def __sliceToX(self, slice, r, offset):
-        plus = (math.pi * offset) / 180
-        radial = ((math.pi/6) * slice) + plus
-        return r * (math.cos(radial)+1)
-
-    def __sliceToY(self, slice, r, offset):
-        plus = (math.pi * offset) / 180
-        radial = ((math.pi/6) * slice) + plus
-        return r * ((math.sin(radial)/-1)+1)
+        return out
 
-    def __zodiacSlice(self, num, r, style,  type):
+    def _zodiacSlice(self, num, r, style, type):
         # pie slices
-        offset = 360 - self.houses_degree_ut[6]
+        offset = 360 - self.user.houses_degree_ut[6]
         # check transit
-        if self.chart_type == "Transit" or self.chart_type == "Composite":
+        if self.chart_type == "Transit" or self.chart_type == "Synastry":
             dropin = 0
         else:
             dropin = self.c1
-        slice = '<path d="M' + str(r) + ',' + str(r) + ' L' + str(dropin + self.__sliceToX(num, r-dropin, offset)) + ',' + str(dropin + self.__sliceToY(num, r-dropin, offset)) + ' A' + str(
-            r-dropin) + ',' + str(r-dropin) + ' 0 0,0 ' + str(dropin + self.__sliceToX(num+1, r-dropin, offset)) + ',' + str(dropin + self.__sliceToY(num+1, r-dropin, offset)) + ' z" style="' + style + '"/>'
+        slice = f'<path d="M{str(r)},{str(r)} L{str(dropin + sliceToX(num, r - dropin, offset))},{str(dropin + sliceToY(num, r - dropin, offset))} A{str(r - dropin)},{str(r - dropin)} 0 0,0 {str(dropin + sliceToX(num + 1, r - dropin, offset))},{str(dropin + sliceToY(num + 1, r - dropin, offset))} z" style="{style}"/>'
+
         # symbols
         offset = offset + 15
         # check transit
-        if self.chart_type == "Transit" or self.chart_type == "Composite":
+        if self.chart_type == "Transit" or self.chart_type == "Synastry":
             dropin = 54
         else:
-            dropin = 18+self.c1
-        sign = '<g transform="translate(-16,-16)"><use x="' + str(dropin + self.__sliceToX(num, r-dropin, offset)) + '" y="' + str(
-            dropin + self.__sliceToY(num, r-dropin, offset)) + '" xlink:href="#' + type + '" /></g>'
-        return slice + '' + sign
+            dropin = 18 + self.c1
+        sign = f'<g transform="translate(-16,-16)"><use x="{str(dropin + sliceToX(num, r - dropin, offset))}" y="{str(dropin + sliceToY(num, r - dropin, offset))}" xlink:href="#{type}" /></g>'
+
+        return slice + "" + sign
 
-    def __makeZodiac(self, r):
+    def _makeZodiac(self, r):
         output = ""
         for i in range(len(self.zodiac)):
-            output = output + self.__zodiacSlice(i, r, "fill:" + self.colors_settings["zodiac_bg_%s" % (
-                i)] + "; fill-opacity: 0.5;", self.zodiac[i]) + ''
+            output = (
+                output
+                + self._zodiacSlice(
+                    i,
+                    r,
+                    f'fill:{self.chart_colors_settings[f"zodiac_bg_{i}"]}; fill-opacity: 0.5;',
+                    self.zodiac[i]["name"],
+                )
+            )
         return output
 
-    def __makeHouses(self, r):
+    def _makeHouses(self, r):
         path = ""
 
         xr = 12
         for i in range(xr):
             # check transit
-            if self.chart_type == "Transit" or self.chart_type == "Composite":
+            if self.chart_type == "Transit" or self.chart_type == "Synastry":
                 dropin = 160
                 roff = 72
                 t_roff = 36
             else:
                 dropin = self.c3
                 roff = self.c1
 
             # offset is negative desc houses_degree_ut[6]
-            offset = (
-                int(self.houses_degree_ut[int(xr/2)]) / -1) + int(self.houses_degree_ut[i])
-            x1 = self.__sliceToX(0, (r-dropin), offset) + dropin
-            y1 = self.__sliceToY(0, (r-dropin), offset) + dropin
-            x2 = self.__sliceToX(0, r-roff, offset) + roff
-            y2 = self.__sliceToY(0, r-roff, offset) + roff
-
-            if i < (xr-1):
-                text_offset = offset + \
-                    int(self.__degreeDiff(self.houses_degree_ut[(
-                        i+1)], self.houses_degree_ut[i]) / 2)
+            offset = (int(self.user.houses_degree_ut[int(xr / 2)]) / -1) + int(self.user.houses_degree_ut[i])
+            x1 = sliceToX(0, (r - dropin), offset) + dropin
+            y1 = sliceToY(0, (r - dropin), offset) + dropin
+            x2 = sliceToX(0, r - roff, offset) + roff
+            y2 = sliceToY(0, r - roff, offset) + roff
+
+            if i < (xr - 1):
+                text_offset = offset + int(degreeDiff(self.user.houses_degree_ut[(i + 1)], self.user.houses_degree_ut[i]) / 2)
             else:
-                text_offset = offset + \
-                    int(self.__degreeDiff(
-                        self.houses_degree_ut[0], self.houses_degree_ut[(xr-1)]) / 2)
+                text_offset = offset + int(degreeDiff(self.user.houses_degree_ut[0], self.user.houses_degree_ut[(xr - 1)]) / 2)
 
             # mc, asc, dsc, ic
             if i == 0:
-                linecolor = self.planets_settings[12]['color']
+                linecolor = self.planets_settings[12]["color"]
             elif i == 9:
-                linecolor = self.planets_settings[13]['color']
+                linecolor = self.planets_settings[13]["color"]
             elif i == 6:
-                linecolor = self.planets_settings[14]['color']
+                linecolor = self.planets_settings[14]["color"]
             elif i == 3:
-                linecolor = self.planets_settings[15]['color']
+                linecolor = self.planets_settings[15]["color"]
             else:
-                linecolor = self.colors_settings['houses_radix_line']
+                linecolor = self.chart_colors_settings["houses_radix_line"]
 
             # Transit houses lines.
-            if self.chart_type == "Transit" or self.chart_type == "Composite":
-
+            if self.chart_type == "Transit" or self.chart_type == "Synastry":
                 # Degrees for point zero.
 
-                zeropoint = 360 - self.houses_degree_ut[6]
-                t_offset = zeropoint + self.t_houses_degree_ut[i]
+                zeropoint = 360 - self.user.houses_degree_ut[6]
+                t_offset = zeropoint + self.t_user.houses_degree_ut[i]
                 if t_offset > 360:
                     t_offset = t_offset - 360
-                t_x1 = self.__sliceToX(0, (r-t_roff), t_offset) + t_roff
-                t_y1 = self.__sliceToY(0, (r-t_roff), t_offset) + t_roff
-                t_x2 = self.__sliceToX(0, r, t_offset)
-                t_y2 = self.__sliceToY(0, r, t_offset)
+                t_x1 = sliceToX(0, (r - t_roff), t_offset) + t_roff
+                t_y1 = sliceToY(0, (r - t_roff), t_offset) + t_roff
+                t_x2 = sliceToX(0, r, t_offset)
+                t_y2 = sliceToY(0, r, t_offset)
                 if i < 11:
-                    t_text_offset = t_offset + \
-                        int(self.__degreeDiff(self.t_houses_degree_ut[(
-                            i+1)], self.t_houses_degree_ut[i]) / 2)
+                    t_text_offset = t_offset + int(degreeDiff(self.t_user.houses_degree_ut[(i + 1)], self.t_user.houses_degree_ut[i]) / 2)
                 else:
-                    t_text_offset = t_offset + \
-                        int(self.__degreeDiff(
-                            self.t_houses_degree_ut[0], self.t_houses_degree_ut[11]) / 2)
+                    t_text_offset = t_offset + int(degreeDiff(self.t_user.houses_degree_ut[0], self.t_user.houses_degree_ut[11]) / 2)
                 # linecolor
                 if i == 0 or i == 9 or i == 6 or i == 3:
                     t_linecolor = linecolor
                 else:
-                    t_linecolor = self.colors_settings['houses_transit_line']
-                xtext = self.__sliceToX(0, (r-8), t_text_offset) + 8
-                ytext = self.__sliceToY(0, (r-8), t_text_offset) + 8
+                    t_linecolor = self.chart_colors_settings["houses_transit_line"]
+                xtext = sliceToX(0, (r - 8), t_text_offset) + 8
+                ytext = sliceToY(0, (r - 8), t_text_offset) + 8
 
                 if self.chart_type == "Transit":
-                    path = path + '<text style="fill: #00f; fill-opacity: 0; font-size: 14px"><tspan x="' + \
-                        str(xtext-3)+'" y="'+str(ytext+3) + \
-                        '">'+str(i+1)+'</tspan></text>'
-                    path = path + '<line x1="'+str(t_x1)+'" y1="'+str(t_y1)+'" x2="'+str(t_x2)+'" y2="'+str(
-                        t_y2)+'" style="stroke: '+t_linecolor+'; stroke-width: 2px; stroke-opacity:0;"/>'
+                    path = path + '<text style="fill: #00f; fill-opacity: 0; font-size: 14px"><tspan x="' + str(xtext - 3) + '" y="' + str(ytext + 3) + '">' + str(i + 1) + "</tspan></text>"
+                    path = f"{path}<line x1='{str(t_x1)}' y1='{str(t_y1)}' x2='{str(t_x2)}' y2='{str(t_y2)}' style='stroke: {t_linecolor}; stroke-width: 2px; stroke-opacity:0;'/>"
 
                 else:
-                    path = path + '<text style="fill: #00f; fill-opacity: .4; font-size: 14px"><tspan x="' + \
-                        str(xtext-3)+'" y="'+str(ytext+3) + \
-                        '">'+str(i+1)+'</tspan></text>'
-                    path = path + '<line x1="'+str(t_x1)+'" y1="'+str(t_y1)+'" x2="'+str(t_x2)+'" y2="'+str(
-                        t_y2)+'" style="stroke: '+t_linecolor+'; stroke-width: 2px; stroke-opacity:.3;"/>'
+                    path = path + '<text style="fill: #00f; fill-opacity: .4; font-size: 14px"><tspan x="' + str(xtext - 3) + '" y="' + str(ytext + 3) + '">' + str(i + 1) + "</tspan></text>"
+                    path = f"{path}<line x1='{str(t_x1)}' y1='{str(t_y1)}' x2='{str(t_x2)}' y2='{str(t_y2)}' style='stroke: {t_linecolor}; stroke-width: 2px; stroke-opacity:.3;'/>"
+
 
             # if transit
-            if self.chart_type == "Transit" or self.chart_type == "Composite":
+            if self.chart_type == "Transit" or self.chart_type == "Synastry":
                 dropin = 84
+            elif self.chart_type == "ExternalNatal":
+                dropin = 100
+            # Natal
+            else:
+                dropin = 48
 
-            dropin = 48
-
-            xtext = self.__sliceToX(
-                0, (r-dropin), text_offset) + dropin  # was 132
-            ytext = self.__sliceToY(
-                0, (r-dropin), text_offset) + dropin  # was 132
-            path = path + '<line x1="'+str(x1)+'" y1="'+str(y1)+'" x2="'+str(x2)+'" y2="'+str(
-                y2)+'" style="stroke: '+linecolor+'; stroke-width: 2px; stroke-dasharray:3,2; stroke-opacity:.4;"/>'
-            path = path + '<text style="fill: #f00; fill-opacity: .6; font-size: 14px"><tspan x="' + \
-                str(xtext-3)+'" y="'+str(ytext+3) + \
-                '">'+str(i+1)+'</tspan></text>'
+            xtext = sliceToX(0, (r - dropin), text_offset) + dropin  # was 132
+            ytext = sliceToY(0, (r - dropin), text_offset) + dropin  # was 132
+            path = f'{path}<line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}" style="stroke: {linecolor}; stroke-width: 2px; stroke-dasharray:3,2; stroke-opacity:.4;"/>'
+            path = path + '<text style="fill: #f00; fill-opacity: .6; font-size: 14px"><tspan x="' + str(xtext - 3) + '" y="' + str(ytext + 3) + '">' + str(i + 1) + "</tspan></text>"
 
         return path
 
-    def __makePlanets(self, r):
+    def _value_element_from_planet(self, i):
+        """
+        Calculate chart element points from a planet.
+        """
 
-        planets_degut = {}
+        # element: get extra points if planet is in own zodiac sign.
+        related_zodiac_signs = self.planets_settings[i]["related_zodiac_signs"]
+        cz = self.points_sign[i]
+        extra_points = 0
+        if related_zodiac_signs != []:
+            for e in range(len(related_zodiac_signs)):
+                if int(related_zodiac_signs[e]) == int(cz):
+                    extra_points = self.planet_in_zodiac_extra_points
+
+        ele = self.zodiac[self.points_sign[i]]["element"]
+        if ele == "fire":
+            self.fire = self.fire + self.planets_settings[i]["element_points"] + extra_points
+
+        elif ele == "earth":
+            self.earth = self.earth + self.planets_settings[i]["element_points"] + extra_points
+
+        elif ele == "air":
+            self.air = self.air + self.planets_settings[i]["element_points"] + extra_points
+
+        elif ele == "water":
+            self.water = self.water + self.planets_settings[i]["element_points"] + extra_points
 
+    def _make_planets(self, r):
+        planets_degut = {}
         diff = range(len(self.planets_settings))
+
         for i in range(len(self.planets_settings)):
-            if self.planets_settings[i]['visible'] == 1:
+            if self.planets_settings[i]["is_active"] == 1:
                 # list of planets sorted by degree
-                planets_degut[self.planets_degree_ut[i]] = i
+                logger.debug(f"planet: {i}, degree: {self.points_deg_ut[i]}")
+                planets_degut[self.points_deg_ut[i]] = i
 
-            # element: get extra points if planet is in own zodiac
-            pz = self.planets_settings[i]['zodiac_relation']
-            cz = self.planets_sign[i]
-            extrapoints = 0
-            if pz != -1:
-                for e in range(len(pz.split(','))):
-                    if int(pz.split(',')[e]) == int(cz):
-                        extrapoints = 10
-
-            # calculate element points for all planets
-            ele = self.zodiac_element[self.planets_sign[i]]
-            if ele == "fire":
-                self.fire = self.fire + \
-                    self.planets_settings[i]['element_points'] + extrapoints
-            elif ele == "earth":
-                self.earth = self.earth + \
-                    self.planets_settings[i]['element_points'] + extrapoints
-            elif ele == "air":
-                self.air = self.air + \
-                    self.planets_settings[i]['element_points'] + extrapoints
-            elif ele == "water":
-                self.water = self.water + \
-                    self.planets_settings[i]['element_points'] + extrapoints
+            self._value_element_from_planet(i)
 
         output = ""
         keys = list(planets_degut.keys())
         keys.sort()
         switch = 0
 
         planets_degrouped = {}
@@ -588,187 +580,203 @@
         planet_drange = 3.4
         # get groups closely together
         group_open = False
         for e in range(len(keys)):
             i = planets_degut[keys[e]]
             # get distances between planets
             if e == 0:
-                prev = self.planets_degree_ut[planets_degut[keys[-1]]]
-                next = self.planets_degree_ut[planets_degut[keys[1]]]
-            elif e == (len(keys)-1):
-                prev = self.planets_degree_ut[planets_degut[keys[e-1]]]
-                next = self.planets_degree_ut[planets_degut[keys[0]]]
+                prev = self.points_deg_ut[planets_degut[keys[-1]]]
+                next = self.points_deg_ut[planets_degut[keys[1]]]
+            elif e == (len(keys) - 1):
+                prev = self.points_deg_ut[planets_degut[keys[e - 1]]]
+                next = self.points_deg_ut[planets_degut[keys[0]]]
             else:
-                prev = self.planets_degree_ut[planets_degut[keys[e-1]]]
-                next = self.planets_degree_ut[planets_degut[keys[e+1]]]
-            diffa = self.__degreeDiff(prev, self.planets_degree_ut[i])
-            diffb = self.__degreeDiff(next, self.planets_degree_ut[i])
+                prev = self.points_deg_ut[planets_degut[keys[e - 1]]]
+                next = self.points_deg_ut[planets_degut[keys[e + 1]]]
+            diffa = degreeDiff(prev, self.points_deg_ut[i])
+            diffb = degreeDiff(next, self.points_deg_ut[i])
             planets_by_pos[e] = [i, diffa, diffb]
-            # print "%s %s %s" % (self.planets_settings[i]['label'],diffa,diffb)
-            if (diffb < planet_drange):
+
+            logger.debug(f'{self.planets_settings[i]["label"]}, {diffa}, {diffb}')
+
+            if diffb < planet_drange:
                 if group_open:
-                    groups[-1].append([e, diffa, diffb,
-                                      self.planets_settings[planets_degut[keys[e]]]["label"]])
+                    groups[-1].append([e, diffa, diffb, self.planets_settings[planets_degut[keys[e]]]["label"]])
                 else:
                     group_open = True
                     groups.append([])
-                    groups[-1].append([e, diffa, diffb,
-                                      self.planets_settings[planets_degut[keys[e]]]["label"]])
+                    groups[-1].append([e, diffa, diffb, self.planets_settings[planets_degut[keys[e]]]["label"]])
             else:
                 if group_open:
-                    groups[-1].append([e, diffa, diffb,
-                                      self.planets_settings[planets_degut[keys[e]]]["label"]])
+                    groups[-1].append([e, diffa, diffb, self.planets_settings[planets_degut[keys[e]]]["label"]])
                 group_open = False
 
-        def zero(x): return 0
+        def zero(x):
+            return 0
+
         planets_delta = list(map(zero, range(len(self.planets_settings))))
 
         # print groups
         # print planets_by_pos
         for a in range(len(groups)):
             # Two grouped planets
             if len(groups[a]) == 2:
-                next_to_a = groups[a][0][0]-1
-                if groups[a][1][0] == (len(planets_by_pos)-1):
+                next_to_a = groups[a][0][0] - 1
+                if groups[a][1][0] == (len(planets_by_pos) - 1):
                     next_to_b = 0
                 else:
-                    next_to_b = groups[a][1][0]+1
+                    next_to_b = groups[a][1][0] + 1
                 # if both planets have room
-                if (groups[a][0][1] > (2*planet_drange)) & (groups[a][1][2] > (2*planet_drange)):
-                    planets_delta[groups[a][0][0]] = - \
-                        (planet_drange-groups[a][0][2])/2
-                    planets_delta[groups[a][1][0]] = + \
-                        (planet_drange-groups[a][0][2])/2
+                if (groups[a][0][1] > (2 * planet_drange)) & (groups[a][1][2] > (2 * planet_drange)):
+                    planets_delta[groups[a][0][0]] = -(planet_drange - groups[a][0][2]) / 2
+                    planets_delta[groups[a][1][0]] = +(planet_drange - groups[a][0][2]) / 2
                 # if planet a has room
-                elif (groups[a][0][1] > (2*planet_drange)):
+                elif groups[a][0][1] > (2 * planet_drange):
                     planets_delta[groups[a][0][0]] = -planet_drange
                 # if planet b has room
-                elif (groups[a][1][2] > (2*planet_drange)):
+                elif groups[a][1][2] > (2 * planet_drange):
                     planets_delta[groups[a][1][0]] = +planet_drange
 
                 # if planets next to a and b have room move them
-                elif (planets_by_pos[next_to_a][1] > (2.4*planet_drange)) & (planets_by_pos[next_to_b][2] > (2.4*planet_drange)):
-                    planets_delta[(next_to_a)] = (
-                        groups[a][0][1]-planet_drange*2)
-                    planets_delta[groups[a][0][0]] = -planet_drange*.5
-                    planets_delta[next_to_b] = - \
-                        (groups[a][1][2]-planet_drange*2)
-                    planets_delta[groups[a][1][0]] = +planet_drange*.5
+                elif (planets_by_pos[next_to_a][1] > (2.4 * planet_drange)) & (planets_by_pos[next_to_b][2] > (2.4 * planet_drange)):
+                    planets_delta[(next_to_a)] = groups[a][0][1] - planet_drange * 2
+                    planets_delta[groups[a][0][0]] = -planet_drange * 0.5
+                    planets_delta[next_to_b] = -(groups[a][1][2] - planet_drange * 2)
+                    planets_delta[groups[a][1][0]] = +planet_drange * 0.5
 
                 # if planet next to a has room move them
-                elif (planets_by_pos[next_to_a][1] > (2*planet_drange)):
-                    planets_delta[(next_to_a)] = (
-                        groups[a][0][1]-planet_drange*2.5)
-                    planets_delta[groups[a][0][0]] = -planet_drange*1.2
+                elif planets_by_pos[next_to_a][1] > (2 * planet_drange):
+                    planets_delta[(next_to_a)] = groups[a][0][1] - planet_drange * 2.5
+                    planets_delta[groups[a][0][0]] = -planet_drange * 1.2
 
                 # if planet next to b has room move them
-                elif (planets_by_pos[next_to_b][2] > (2*planet_drange)):
-                    planets_delta[next_to_b] = - \
-                        (groups[a][1][2]-planet_drange*2.5)
-                    planets_delta[groups[a][1][0]] = +planet_drange*1.2
+                elif planets_by_pos[next_to_b][2] > (2 * planet_drange):
+                    planets_delta[next_to_b] = -(groups[a][1][2] - planet_drange * 2.5)
+                    planets_delta[groups[a][1][0]] = +planet_drange * 1.2
 
             # Three grouped planets or more
             xl = len(groups[a])
             if xl >= 3:
-
                 available = groups[a][0][1]
                 for f in range(xl):
                     available += groups[a][f][2]
-                need = (3*planet_drange)+(1.2*(xl-1)*planet_drange)
+                need = (3 * planet_drange) + (1.2 * (xl - 1) * planet_drange)
                 leftover = available - need
                 xa = groups[a][0][1]
-                xb = groups[a][(xl-1)][2]
+                xb = groups[a][(xl - 1)][2]
 
                 # center
-                if (xa > (need*.5)) & (xb > (need*.5)):
-                    startA = xa - (need*.5)
+                if (xa > (need * 0.5)) & (xb > (need * 0.5)):
+                    startA = xa - (need * 0.5)
                 # position relative to next planets
                 else:
-                    startA = (leftover/(xa+xb))*xa
-                    startB = (leftover/(xa+xb))*xb
+                    startA = (leftover / (xa + xb)) * xa
+                    startB = (leftover / (xa + xb)) * xb
 
                 if available > need:
-                    planets_delta[groups[a][0][0]] = startA - \
-                        groups[a][0][1]+(1.5*planet_drange)
-                    for f in range(xl-1):
-                        planets_delta[groups[a][(
-                            f+1)][0]] = 1.2*planet_drange+planets_delta[groups[a][f][0]]-groups[a][f][2]
+                    planets_delta[groups[a][0][0]] = startA - groups[a][0][1] + (1.5 * planet_drange)
+                    for f in range(xl - 1):
+                        planets_delta[groups[a][(f + 1)][0]] = 1.2 * planet_drange + planets_delta[groups[a][f][0]] - groups[a][f][2]
 
         for e in range(len(keys)):
             i = planets_degut[keys[e]]
 
             # coordinates
-            if self.chart_type == "Transit" or self.chart_type == "Composite":
+            if self.chart_type == "Transit" or self.chart_type == "Synastry":
                 if 22 < i < 27:
                     rplanet = 76
                 elif switch == 1:
                     rplanet = 110
                     switch = 0
                 else:
                     rplanet = 130
                     switch = 1
             else:
                 # if 22 < i < 27 it is asc,mc,dsc,ic (angles of chart)
                 # put on special line (rplanet is range from outer ring)
                 amin, bmin, cmin = 0, 0, 0
+                if self.chart_type == "ExternalNatal":
+                    amin = 74 - 10
+                    bmin = 94 - 10
+                    cmin = 40 - 10
 
                 if 22 < i < 27:
-                    rplanet = 40-cmin
+                    rplanet = 40 - cmin
                 elif switch == 1:
-                    rplanet = 74-amin
+                    rplanet = 74 - amin
                     switch = 0
                 else:
-                    rplanet = 94-bmin
+                    rplanet = 94 - bmin
                     switch = 1
 
             rtext = 45
 
-            offset = (int(self.houses_degree_ut[6]) / -1) + \
-                int(self.planets_degree_ut[i]+planets_delta[e])
-            trueoffset = (
-                int(self.houses_degree_ut[6]) / -1) + int(self.planets_degree_ut[i])
-
-            planet_x = self.__sliceToX(0, (r-rplanet), offset) + rplanet
-            planet_y = self.__sliceToY(0, (r-rplanet), offset) + rplanet
-            if self.chart_type == "Transit" or self.chart_type == "Composite":
-                scale = 0.8
+            offset = (int(self.user.houses_degree_ut[6]) / -1) + int(self.points_deg_ut[i] + planets_delta[e])
+            trueoffset = (int(self.user.houses_degree_ut[6]) / -1) + int(self.points_deg_ut[i])
 
-            scale = 1
+            planet_x = sliceToX(0, (r - rplanet), offset) + rplanet
+            planet_y = sliceToY(0, (r - rplanet), offset) + rplanet
+            if self.chart_type == "Transit" or self.chart_type == "Synastry":
+                scale = 0.8
+                
+            elif self.chart_type == "ExternalNatal":
+                scale = 0.8
+                # line1
+                x1 = sliceToX(0, (r - self.c3), trueoffset) + self.c3
+                y1 = sliceToY(0, (r - self.c3), trueoffset) + self.c3
+                x2 = sliceToX(0, (r - rplanet - 30), trueoffset) + rplanet + 30
+                y2 = sliceToY(0, (r - rplanet - 30), trueoffset) + rplanet + 30
+                color = self.planets_settings[i]["color"]
+                output += (
+                    '<line x1="%s" y1="%s" x2="%s" y2="%s" style="stroke-width:1px;stroke:%s;stroke-opacity:.3;"/>\n'
+                    % (x1, y1, x2, y2, color)
+                )
+                # line2
+                x1 = sliceToX(0, (r - rplanet - 30), trueoffset) + rplanet + 30
+                y1 = sliceToY(0, (r - rplanet - 30), trueoffset) + rplanet + 30
+                x2 = sliceToX(0, (r - rplanet - 10), offset) + rplanet + 10
+                y2 = sliceToY(0, (r - rplanet - 10), offset) + rplanet + 10
+                output += (
+                    '<line x1="%s" y1="%s" x2="%s" y2="%s" style="stroke-width:1px;stroke:%s;stroke-opacity:.5;"/>\n'
+                    % (x1, y1, x2, y2, color)
+                )
+                
+            else:
+                scale = 1
             # output planet
-            output = output + '<g transform="translate(-'+str(12*scale)+',-'+str(12*scale)+')"><g transform="scale('+str(scale)+')"><use x="' + str(
-                planet_x*(1/scale)) + '" y="' + str(planet_y*(1/scale)) + '" xlink:href="#' + self.planets_settings[i]['name'] + '" /></g></g>'
+            output += f'<g transform="translate(-{12 * scale},-{12 * scale})"><g transform="scale({scale})"><use x="{planet_x * (1/scale)}" y="{planet_y * (1/scale)}" xlink:href="#{self.planets_settings[i]["name"]}" /></g></g>'
 
         # make transit degut and display planets
-        if self.chart_type == "Transit" or self.chart_type == "Composite":
+        if self.chart_type == "Transit" or self.chart_type == "Synastry":
             group_offset = {}
             t_planets_degut = {}
             if self.chart_type == "Transit":
-                list_range = len(self.planets_settings)-4
+                list_range = len(self.planets_settings) - 4
             else:
                 list_range = len(self.planets_settings)
             for i in range(list_range):
                 group_offset[i] = 0
-                if self.planets_settings[i]['visible'] == 1:
-                    t_planets_degut[self.t_planets_degree_ut[i]] = i
+                if self.planets_settings[i]["is_active"] == 1:
+                    t_planets_degut[self.t_points_deg_ut[i]] = i
             t_keys = list(t_planets_degut.keys())
             t_keys.sort()
 
             # grab closely grouped planets
             groups = []
             in_group = False
             for e in range(len(t_keys)):
                 i_a = t_planets_degut[t_keys[e]]
-                if e == (len(t_keys)-1):
+                if e == (len(t_keys) - 1):
                     i_b = t_planets_degut[t_keys[0]]
                 else:
-                    i_b = t_planets_degut[t_keys[e+1]]
+                    i_b = t_planets_degut[t_keys[e + 1]]
 
-                a = self.t_planets_degree_ut[i_a]
-                b = self.t_planets_degree_ut[i_b]
-                diff = self.__degreeDiff(a, b)
+                a = self.t_points_deg_ut[i_a]
+                b = self.t_points_deg_ut[i_b]
+                diff = degreeDiff(a, b)
                 if diff <= 2.5:
                     if in_group:
                         groups[-1].append(i_b)
                     else:
                         groups.append([i_a])
                         groups[-1].append(i_b)
                         in_group = True
@@ -798,32 +806,31 @@
                 elif switch == 1:
                     rplanet = 18
                     switch = 0
                 else:
                     rplanet = 26
                     switch = 1
 
-                zeropoint = 360 - self.houses_degree_ut[6]
-                t_offset = zeropoint + self.t_planets_degree_ut[i]
+                zeropoint = 360 - self.user.houses_degree_ut[6]
+                t_offset = zeropoint + self.t_points_deg_ut[i]
                 if t_offset > 360:
                     t_offset = t_offset - 360
-                planet_x = self.__sliceToX(0, (r-rplanet), t_offset) + rplanet
-                planet_y = self.__sliceToY(0, (r-rplanet), t_offset) + rplanet
-                output = output + '<g transform="translate(-6,-6)"><g transform="scale(0.5)"><use x="' + str(
-                    planet_x*2) + '" y="' + str(planet_y*2) + '" xlink:href="#' + self.planets_settings[i]['name'] + '" /></g></g>'
+                planet_x = sliceToX(0, (r - rplanet), t_offset) + rplanet
+                planet_y = sliceToY(0, (r - rplanet), t_offset) + rplanet
+                output += f'<g transform="translate(-6,-6)"><g transform="scale(0.5)"><use x="{planet_x*2}" y="{planet_y*2}" xlink:href="#{self.planets_settings[i]["name"]}" /></g></g>'
+
                 # transit planet line
-                x1 = self.__sliceToX(0, r+3, t_offset) - 3
-                y1 = self.__sliceToY(0, r+3, t_offset) - 3
-                x2 = self.__sliceToX(0, r-3, t_offset) + 3
-                y2 = self.__sliceToY(0, r-3, t_offset) + 3
-                output = output + '<line x1="'+str(x1)+'" y1="'+str(y1)+'" x2="'+str(x2)+'" y2="'+str(
-                    y2)+'" style="stroke: '+self.planets_settings[i]['color']+'; stroke-width: 1px; stroke-opacity:.8;"/>'
+                x1 = sliceToX(0, r + 3, t_offset) - 3
+                y1 = sliceToY(0, r + 3, t_offset) - 3
+                x2 = sliceToX(0, r - 3, t_offset) + 3
+                y2 = sliceToY(0, r - 3, t_offset) + 3
+                output += f'<line x1="{str(x1)}" y1="{str(y1)}" x2="{str(x2)}" y2="{str(y2)}" style="stroke: {self.planets_settings[i]["color"]}; stroke-width: 1px; stroke-opacity:.8;"/>'
 
                 # transit planet degree text
-                rotate = self.houses_degree_ut[0] - self.t_planets_degree_ut[i]
+                rotate = self.user.houses_degree_ut[0] - self.t_points_deg_ut[i]
                 textanchor = "end"
                 t_offset += group_offset[i]
                 rtext = -3.0
 
                 if -90 > rotate > -270:
                     rotate = rotate + 180.0
                     textanchor = "start"
@@ -831,154 +838,140 @@
                     rotate = rotate - 180.0
                     textanchor = "start"
 
                 if textanchor == "end":
                     xo = 1
                 else:
                     xo = -1
-                deg_x = self.__sliceToX(0, (r-rtext), t_offset + xo) + rtext
-                deg_y = self.__sliceToY(0, (r-rtext), t_offset + xo) + rtext
+                deg_x = sliceToX(0, (r - rtext), t_offset + xo) + rtext
+                deg_y = sliceToY(0, (r - rtext), t_offset + xo) + rtext
                 degree = int(t_offset)
-                output += '<g transform="translate(%s,%s)">' % (deg_x, deg_y)
-                output += '<text transform="rotate(%s)" text-anchor="%s' % (
-                    rotate, textanchor)
-                output += '" style="fill: ' + \
-                    self.planets_settings[i]['color']+'; font-size: 10px;">' + \
-                    self.__dec2deg(self.t_planets_degree[i], type="1")
-                output += '</text></g>'
+                output += f'<g transform="translate({deg_x},{deg_y})">'
+                output += f'<text transform="rotate({rotate})" text-anchor="{textanchor}'
+                output += f'" style="fill: {self.planets_settings[i]["color"]}; font-size: 10px;">{self._dec2deg(self.t_points_deg[i], type="1")}'
+                output += "</text></g>"
 
             # check transit
-            if self.chart_type == "Transit" or self.chart_type == "Composite":
+            if self.chart_type == "Transit" or self.chart_type == "Synastry":
                 dropin = 36
             else:
                 dropin = 0
 
             # planet line
-            x1 = self.__sliceToX(0, r-(dropin+3), offset) + (dropin+3)
-            y1 = self.__sliceToY(0, r-(dropin+3), offset) + (dropin+3)
-            x2 = self.__sliceToX(0, (r-(dropin-3)), offset) + (dropin-3)
-            y2 = self.__sliceToY(0, (r-(dropin-3)), offset) + (dropin-3)
-            output = output + '<line x1="'+str(x1)+'" y1="'+str(y1)+'" x2="'+str(x2)+'" y2="'+str(
-                y2)+'" style="stroke: '+self.planets_settings[i]['color']+'; stroke-width: 2px; stroke-opacity:.6;"/>'
+            x1 = sliceToX(0, r - (dropin + 3), offset) + (dropin + 3)
+            y1 = sliceToY(0, r - (dropin + 3), offset) + (dropin + 3)
+            x2 = sliceToX(0, (r - (dropin - 3)), offset) + (dropin - 3)
+            y2 = sliceToY(0, (r - (dropin - 3)), offset) + (dropin - 3)
+
+            output += f'<line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}" style="stroke: {self.planets_settings[i]["color"]}; stroke-width: 2px; stroke-opacity:.6;"/>'
 
             # check transit
-            if self.chart_type == "Transit" or self.chart_type == "Composite":
+            if self.chart_type == "Transit" or self.chart_type == "Synastry":
                 dropin = 160
             else:
                 dropin = 120
 
-            x1 = self.__sliceToX(0, r-dropin, offset) + dropin
-            y1 = self.__sliceToY(0, r-dropin, offset) + dropin
-            x2 = self.__sliceToX(0, (r-(dropin-3)), offset) + (dropin-3)
-            y2 = self.__sliceToY(0, (r-(dropin-3)), offset) + (dropin-3)
-            output = output + '<line x1="'+str(x1)+'" y1="'+str(y1)+'" x2="'+str(x2)+'" y2="'+str(
-                y2)+'" style="stroke: '+self.planets_settings[i]['color']+'; stroke-width: 2px; stroke-opacity:.6;"/>'
+            x1 = sliceToX(0, r - dropin, offset) + dropin
+            y1 = sliceToY(0, r - dropin, offset) + dropin
+            x2 = sliceToX(0, (r - (dropin - 3)), offset) + (dropin - 3)
+            y2 = sliceToY(0, (r - (dropin - 3)), offset) + (dropin - 3)
+            output += f'<line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}" style="stroke: {self.planets_settings[i]["color"]}; stroke-width: 2px; stroke-opacity:.6;"/>'
 
         return output
 
-    def __makePatterns(self):
+    def _makePatterns(self):
         """
         * Stellium: At least four planets linked together in a series of continuous conjunctions.
         * Grand trine: Three trine aspects together.
         * Grand cross: Two pairs of opposing planets squared to each other.
         * T-Square: Two planets in opposition squared to a third.
         * Yod: Two qunicunxes together joined by a sextile.
         """
         conj = {}  # 0
         opp = {}  # 10
         sq = {}  # 5
         tr = {}  # 6
         qc = {}  # 9
         sext = {}  # 3
         for i in range(len(self.planets_settings)):
-            a = self.planets_degree_ut[i]
+            a = self.points_deg_ut[i]
             qc[i] = {}
             sext[i] = {}
             opp[i] = {}
             sq[i] = {}
             tr[i] = {}
             conj[i] = {}
             # skip some points
-            n = self.planets_settings[i]['name']
-            if n == 'earth' or n == 'True_Node' or n == 'osc. apogee' or n == 'intp. apogee' or n == 'intp. perigee':
+            n = self.planets_settings[i]["name"]
+            if n == "earth" or n == "True_Node" or n == "osc. apogee" or n == "intp. apogee" or n == "intp. perigee":
                 continue
-            if n == 'Dsc' or n == 'Ic':
+            if n == "Dsc" or n == "Ic":
                 continue
             for j in range(len(self.planets_settings)):
                 # skip some points
-                n = self.planets_settings[j]['name']
-                if n == 'earth' or n == 'True_Node' or n == 'osc. apogee' or n == 'intp. apogee' or n == 'intp. perigee':
+                n = self.planets_settings[j]["name"]
+                if n == "earth" or n == "True_Node" or n == "osc. apogee" or n == "intp. apogee" or n == "intp. perigee":
                     continue
-                if n == 'Dsc' or n == 'Ic':
+                if n == "Dsc" or n == "Ic":
                     continue
-                b = self.planets_degree_ut[j]
-                delta = float(self.__degreeDiff(a, b))
+                b = self.points_deg_ut[j]
+                delta = float(degreeDiff(a, b))
                 # check for opposition
-                xa = float(self.aspects_settings[10]['degree']) - \
-                    float(self.aspects_settings[10]['orb'])
-                xb = float(self.aspects_settings[10]['degree']) + \
-                    float(self.aspects_settings[10]['orb'])
-                if(xa <= delta <= xb):
+                xa = float(self.aspects_settings[10]["degree"]) - float(self.aspects_settings[10]["orb"])
+                xb = float(self.aspects_settings[10]["degree"]) + float(self.aspects_settings[10]["orb"])
+                if xa <= delta <= xb:
                     opp[i][j] = True
                 # check for conjunction
-                xa = float(self.aspects_settings[0]['degree']) - \
-                    float(self.aspects_settings[0]['orb'])
-                xb = float(self.aspects_settings[0]['degree']) + \
-                    float(self.aspects_settings[0]['orb'])
-                if(xa <= delta <= xb):
+                xa = float(self.aspects_settings[0]["degree"]) - float(self.aspects_settings[0]["orb"])
+                xb = float(self.aspects_settings[0]["degree"]) + float(self.aspects_settings[0]["orb"])
+                if xa <= delta <= xb:
                     conj[i][j] = True
                 # check for squares
-                xa = float(self.aspects_settings[5]['degree']) - \
-                    float(self.aspects_settings[5]['orb'])
-                xb = float(self.aspects_settings[5]['degree']) + \
-                    float(self.aspects_settings[5]['orb'])
-                if(xa <= delta <= xb):
+                xa = float(self.aspects_settings[5]["degree"]) - float(self.aspects_settings[5]["orb"])
+                xb = float(self.aspects_settings[5]["degree"]) + float(self.aspects_settings[5]["orb"])
+                if xa <= delta <= xb:
                     sq[i][j] = True
                 # check for qunicunxes
-                xa = float(self.aspects_settings[9]['degree']) - \
-                    float(self.aspects_settings[9]['orb'])
-                xb = float(self.aspects_settings[9]['degree']) + \
-                    float(self.aspects_settings[9]['orb'])
-                if(xa <= delta <= xb):
+                xa = float(self.aspects_settings[9]["degree"]) - float(self.aspects_settings[9]["orb"])
+                xb = float(self.aspects_settings[9]["degree"]) + float(self.aspects_settings[9]["orb"])
+                if xa <= delta <= xb:
                     qc[i][j] = True
                 # check for sextiles
-                xa = float(self.aspects_settings[3]['degree']) - \
-                    float(self.aspects_settings[3]['orb'])
-                xb = float(self.aspects_settings[3]['degree']) + \
-                    float(self.aspects_settings[3]['orb'])
-                if(xa <= delta <= xb):
+                xa = float(self.aspects_settings[3]["degree"]) - float(self.aspects_settings[3]["orb"])
+                xb = float(self.aspects_settings[3]["degree"]) + float(self.aspects_settings[3]["orb"])
+                if xa <= delta <= xb:
                     sext[i][j] = True
 
         yot = {}
         # check for double qunicunxes
         for k, v in qc.items():
             if len(qc[k]) >= 2:
                 # check for sextile
                 for l, w in qc[k].items():
                     for m, x in qc[k].items():
                         if m in sext[l]:
                             if l > m:
-                                yot['%s,%s,%s' % (k, m, l)] = [k, m, l]
+                                yot["%s,%s,%s" % (k, m, l)] = [k, m, l]
                             else:
-                                yot['%s,%s,%s' % (k, l, m)] = [k, l, m]
+                                yot["%s,%s,%s" % (k, l, m)] = [k, l, m]
         tsquare = {}
         # check for opposition
         for k, v in opp.items():
             if len(opp[k]) >= 1:
                 # check for square
                 for l, w in opp[k].items():
                     for a, b in sq.items():
                         if k in sq[a] and l in sq[a]:
-                            # print 'got tsquare %s %s %s' % (a,k,l)
+                            logger.debug(f"Got tsquare {a} {k} {l}")
                             if k > l:
-                                tsquare['%s,%s,%s' % (a, l, k)] = '%s => %s, %s' % (
-                                    self.planets_settings[a]['label'], self.planets_settings[l]['label'], self.planets_settings[k]['label'])
+                                tsquare[f"{a},{l},{k}"] = f"{self.planets_settings[a]['label']} => {self.planets_settings[l]['label']}, {self.planets_settings[k]['label']}"
+
                             else:
-                                tsquare['%s,%s,%s' % (a, k, l)] = '%s => %s, %s' % (
-                                    self.planets_settings[a]['label'], self.planets_settings[k]['label'], self.planets_settings[l]['label'])
+                                tsquare[f"{a},{k},{l}"] = f"{self.planets_settings[a]['label']} => {self.planets_settings[k]['label']}, {self.planets_settings[l]['label']}"
+
         stellium = {}
         # check for 4 continuous conjunctions
         for k, v in conj.items():
             if len(conj[k]) >= 1:
                 # first conjunction
                 for l, m in conj[k].items():
                     if len(conj[l]) >= 1:
@@ -997,114 +990,117 @@
                                         for r, s in conj[p].items():
                                             # skip conj 1,2,3
                                             if r == k or r == n or r == p:
                                                 continue
 
                                             l = [k, n, p, r]
                                             l.sort()
-                                            stellium['%s %s %s %s' % (l[0], l[1], l[2], l[3])] = '%s %s %s %s' % (
-                                                self.planets_settings[l[0]
-                                                                      ]['label'], self.planets_settings[l[1]]['label'],
-                                                self.planets_settings[l[2]]['label'], self.planets_settings[l[3]]['label'])
+                                            stellium["%s %s %s %s" % (l[0], l[1], l[2], l[3])] = "%s %s %s %s" % (
+                                                self.planets_settings[l[0]]["label"],
+                                                self.planets_settings[l[1]]["label"],
+                                                self.planets_settings[l[2]]["label"],
+                                                self.planets_settings[l[3]]["label"],
+                                            )
         # print yots
         out = '<g transform="translate(-30,380)">'
         if len(yot) >= 1:
             y = 0
             for k, v in yot.items():
-                out += '<text y="%s" style="fill:%s; font-size: 12px;">%s</text>' % (
-                    y, self.colors_settings['paper_0'], ("Yot"))
+                out += f'<text y="{y}" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 12px;">{"Yot"}</text>'
 
                 # first planet symbol
-                out += '<g transform="translate(20,%s)">' % (y)
-                out += '<use transform="scale(0.4)" x="0" y="-20" xlink:href="#%s" /></g>' % (
-                    self.planets_settings[yot[k][0]]['name'])
+                out += f'<g transform="translate(20,{y})">'
+                out += f'<use transform="scale(0.4)" x="0" y="-20" xlink:href="#{self.planets_settings[yot[k][0]]["name"]}" /></g>'
 
                 # second planet symbol
-                out += '<g transform="translate(30,%s)">' % (y)
-                out += '<use transform="scale(0.4)" x="0" y="-20" xlink:href="#%s" /></g>' % (
-                    self.planets_settings[yot[k][1]]['name'])
+                out += f'<g transform="translate(30,{y})">'
+                out += f'<use transform="scale(0.4)" x="0" y="-20" xlink:href="#{self.planets_settings[yot[k][1]]["name"]}" /></g>'
 
                 # third planet symbol
-                out += '<g transform="translate(40,%s)">' % (y)
-                out += '<use transform="scale(0.4)" x="0" y="-20" xlink:href="#%s" /></g>' % (
-                    self.planets_settings[yot[k][2]]['name'])
+                out += f'<g transform="translate(40,{y})">'
+                out += f'<use transform="scale(0.4)" x="0" y="-20" xlink:href="#{self.planets_settings[yot[k][2]]["name"]}" /></g>'
 
-                y = y+14
+                y = y + 14
         # finalize
-        out += '</g>'
+        out += "</g>"
         # return out
-        return ''
+        return ""
 
     # Aspect and aspect grid functions for natal type charts.
-
-    def __makeAspects(self, r, ar):
+    def _makeAspects(self, r, ar):
         out = ""
         for element in self.aspects_list:
-            out += self.__drawAspect(r, ar, element['p1_abs_pos'], element['p2_abs_pos'],
-                                   self.colors_settings[f"aspect_{element['aspect_degrees']}"])
+            out += self._drawAspect(
+                r,
+                ar,
+                element["p1_abs_pos"],
+                element["p2_abs_pos"],
+                self.aspects_settings[element["aid"]]["color"],
+            )
 
         return out
 
-    def __makeAspectGrid(self, r):
-
+    def _makeAspectGrid(self, r):
         out = ""
-        style = 'stroke:%s; stroke-width: 1px; stroke-opacity:.6; fill:none' % (
-            self.colors_settings['paper_0'])
+        style = "stroke:%s; stroke-width: 1px; stroke-opacity:.6; fill:none" % (self.chart_colors_settings["paper_0"])
         xindent = 380
         yindent = 468
         box = 14
         revr = list(range(len(self.planets_settings)))
         revr.reverse()
         counter = 0
         for a in revr:
             counter += 1
-            if self.planets_settings[a]['visible'] == 1:
-                out += '<rect x="'+str(xindent)+'" y="'+str(yindent)+'" width="'+str(
-                    box)+'" height="'+str(box)+'" style="'+style+'"/>'
-                out += '<use transform="scale(0.4)" x="'+str((xindent+2)*2.5)+'" y="'+str(
-                    (yindent+1)*2.5)+'" xlink:href="#'+self.planets_settings[a]['name']+'" />'
+            if self.planets_settings[a]["is_active"] == 1:
+                out += f'<rect x="{xindent}" y="{yindent}" width="{box}" height="{box}" style="{style}"/>'
+                out += f'<use transform="scale(0.4)" x="{(xindent+2)*2.5}" y="{(yindent+1)*2.5}" xlink:href="#{self.planets_settings[a]["name"]}" />'
+
                 xindent = xindent + box
                 yindent = yindent - box
                 revr2 = list(range(a))
                 revr2.reverse()
                 xorb = xindent
                 yorb = yindent + box
                 for b in revr2:
-                    if self.planets_settings[b]['visible'] == 1:
-                        out += '<rect x="'+str(xorb)+'" y="'+str(yorb)+'" width="'+str(
-                            box)+'" height="'+str(box)+'" style="'+style+'"/>'
-                        xorb = xorb+box
+                    if self.planets_settings[b]["is_active"] == 1:
+                        out += f'<rect x="{xorb}" y="{yorb}" width="{box}" height="{box}" style="{style}"/>'
+
+                        xorb = xorb + box
                         for element in self.aspects_list:
-                            if (element['p1'] == a and element['p2'] == b) or (element['p1'] == b and element['p2'] == a):
-                                out += '<use  x="'+str(xorb-box+1)+'" y="'+str(
-                                    yorb+1)+'" xlink:href="#orb'+str(element['aspect_degrees'])+'" />'
+                            if (element["p1"] == a and element["p2"] == b) or (element["p1"] == b and element["p2"] == a):
+                                out += f'<use  x="{xorb-box+1}" y="{yorb+1}" xlink:href="#orb{element["aspect_degrees"]}" />'
 
         return out
 
     # Aspect and aspect grid functions for transit type charts.
 
-    def __makeAspectsTransit(self, r, ar):
+    def _makeAspectsTransit(self, r, ar):
         out = ""
 
-        self.aspects_list = CompositeAspects(
-            self.user, self.t_user, new_settings_file=self.settings_file
-        ).get_relevant_aspects()
+        self.aspects_list = SynastryAspects(self.user, self.t_user, new_settings_file=self.new_settings_file).get_relevant_aspects()
 
         for element in self.aspects_list:
-            out += self.__drawAspect(r, ar, element['p1_abs_pos'], element['p2_abs_pos'],
-                                   self.colors_settings[f"aspect_{element['aspect_degrees']}"])
+            print(element)
+            out += self._drawAspect(
+                r,
+                ar,
+                element["p1_abs_pos"],
+                element["p2_abs_pos"],
+                self.aspects_settings[element["aid"]]["color"],
+            )
 
         return out
 
-    def __makeAspectTransitGrid(self, r):
+    def _makeAspectTransitGrid(self, r):
         out = '<g transform="translate(500,310)">'
-        out += '<text y="-15" x="0" style="fill:%s; font-size: 14px;">%s</text>' % (
-            self.colors_settings['paper_0'], (f"{self.language_settings['aspects']}:"))
+        out += f'<text y="-15" x="0" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 14px;">{self.language_settings["aspects"]}:</text>'
+
         line = 0
         nl = 0
+
         for i in range(len(self.aspects_list)):
             if i == 12:
                 nl = 100
                 # if len(self.aspects_list) > 24:
                 #     line = -1 * ( len(self.aspects_list) - 24) * 14
                 # else:
                 #     line = 0
@@ -1122,240 +1118,187 @@
 
             if i == 36:
                 nl = 300
                 if len(self.aspects_list) > 48:
                     line = -1 * (len(self.aspects_list) - 48) * 14
                 else:
                     line = 0
-            out += '<g transform="translate(%s,%s)">' % (nl, line)
+            out += f'<g transform="translate({nl},{line})">'
             # first planet symbol
-            out += '<use transform="scale(0.4)" x="0" y="3" xlink:href="#%s" />' % (
-                self.planets_settings[self.aspects_list[i]['p1']]['name'])
+
+            # TODO: (next((item for item in self.planets_settings if item["id"] == self.aspects_list[i]["p1"]))) It preventes the use ot numeric ID, but it is not working.
+            out += f'<use transform="scale(0.4)" x="0" y="3" xlink:href="#{self.planets_settings[self.aspects_list[i]["p1"]]["name"]}" />'
+            
             # aspect symbol
-            out += '<use  x="15" y="0" xlink:href="#orb%s" />' % (
-                self.aspects_settings[self.aspects_list[i]['aid']]['degree'])
+            out += f'<use  x="15" y="0" xlink:href="#orb{self.aspects_settings[self.aspects_list[i]["aid"]]["degree"]}" />'
             # second planet symbol
             out += '<g transform="translate(30,0)">'
-            out += '<use transform="scale(0.4)" x="0" y="3" xlink:href="#%s" />' % (
-                self.planets_settings[self.aspects_list[i]['p2']]['name'])
-            out += '</g>'
+            
+            # TODO: (next((item for item in self.planets_settings if item["id"] == self.aspects_list[i]["p3"])))
+            out += '<use transform="scale(0.4)" x="0" y="3" xlink:href="#%s" />' % (self.planets_settings[self.aspects_list[i]["p2"]]["name"]) 
+            
+            out += "</g>"
             # difference in degrees
-            out += '<text y="8" x="45" style="fill:%s; font-size: 10px;">%s</text>' % (
-                self.colors_settings['paper_0'],
-                self.__dec2deg(self.aspects_list[i]['orbit']))
+            out += f'<text y="8" x="45" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;">{self._dec2deg(self.aspects_list[i]["orbit"])}</text>'
             # line
-            out += '</g>'
+            out += "</g>"
             line = line + 14
-        out += '</g>'
+        out += "</g>"
         return out
 
-    def __makeElements(self, r):
+    def _makeElements(self, r):
         total = self.fire + self.earth + self.air + self.water
-        pf = int(round(100*self.fire/total))
-        pe = int(round(100*self.earth/total))
-        pa = int(round(100*self.air/total))
-        pw = int(round(100*self.water/total))
+        pf = int(round(100 * self.fire / total))
+        pe = int(round(100 * self.earth / total))
+        pa = int(round(100 * self.air / total))
+        pw = int(round(100 * self.water / total))
+
         out = '<g transform="translate(-30,79)">'
-        out += '<text y="0" style="fill:#ff6600; font-size: 10px;">' + \
-            self.language_settings['fire']+'  '+str(pf)+'%</text>'
-        out += '<text y="12" style="fill:#6a2d04; font-size: 10px;">' + \
-            self.language_settings['earth']+' '+str(pe)+'%</text>'
-        out += '<text y="24" style="fill:#6f76d1; font-size: 10px;">' + \
-            self.language_settings['air']+'   '+str(pa)+'%</text>'
-        out += '<text y="36" style="fill:#630e73; font-size: 10px;">' + \
-            self.language_settings['water']+' '+str(pw)+'%</text>'
-        out += '</g>'
-        return out
+        out += f'<text y="0" style="fill:#ff6600; font-size: 10px;">{self.language_settings["fire"]}  {str(pf)}%</text>'
+        out += f'<text y="12" style="fill:#6a2d04; font-size: 10px;">{self.language_settings["earth"]} {str(pe)}%</text>'
+        out += f'<text y="24" style="fill:#6f76d1; font-size: 10px;">{self.language_settings["air"]}   {str(pa)}%</text>'
+        out += f'<text y="36" style="fill:#630e73; font-size: 10px;">{self.language_settings["water"]} {str(pw)}%</text>'
+        out += "</g>"
 
-    def __makePlanetGrid(self):
-        out = '<g transform="translate(500,-20)">'
+        return out
 
-        # loop over all planets
+    def _makePlanetGrid(self):
         li = 10
         offset = 0
 
+        out = '<g transform="translate(500,-20)">'
         out += '<g transform="translate(140, -15)">'
-        out += \
-            f'<text text-anchor="end" style="fill:{self.colors_settings["paper_0"]}; font-size: 14px;">{self.language_settings["planets_and_house"]} {self.name}:</text>'
-        out += '</g>'
+        out += f'<text text-anchor="end" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 14px;">{self.language_settings["planets_and_house"]} {self.name}:</text>'
+        out += "</g>"
 
+        end_of_line = None
         for i in range(len(self.planets_settings)):
+            offset_between_lines = 14
+            end_of_line = "</g>"
 
             # Guarda qui !!
             if i == 27:
                 li = 10
                 offset = -120
-            if self.planets_settings[i]['visible'] == 1:
+
+            if self.planets_settings[i]["is_active"] == 1:
                 # start of line
-                out += '<g transform="translate(%s,%s)">' % (offset, li)
+                out += f'<g transform="translate({offset},{li})">'
+
                 # planet text
-                out += f'<text text-anchor="end" style="fill:{self.colors_settings["paper_0"]}; font-size: 10px;">{self.language_settings["celestial_points"][self.planets_settings[i]["label"]]}</text>'
+                out += f'<text text-anchor="end" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;">{self.language_settings["celestial_points"][self.planets_settings[i]["label"]]}</text>'
+
                 # planet symbol
-                out += \
-                    '<g transform="translate(5,-8)"><use transform="scale(0.4)" xlink:href="#' + \
-                    self.planets_settings[i]['name']+'" /></g>'
+                out += f'<g transform="translate(5,-8)"><use transform="scale(0.4)" xlink:href="#{self.planets_settings[i]["name"]}" /></g>'
+
                 # planet degree
-                out += '<text text-anchor="start" x="19" style="fill:%s; font-size: 10px;">%s</text>' % (
-                    self.colors_settings['paper_0'], self.__dec2deg(self.planets_degree[i]))
+                out += f'<text text-anchor="start" x="19" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;">{self._dec2deg(self.points_deg[i])}</text>'
+
                 # zodiac
-                out += '<g transform="translate(60,-8)"><use transform="scale(0.3)" xlink:href="#' + \
-                    self.zodiac[self.planets_sign[i]]+'" /></g>'
+                out += f'<g transform="translate(60,-8)"><use transform="scale(0.3)" xlink:href="#{self.zodiac[self.points_sign[i]]["name"]}" /></g>'
+
                 # planet retrograde
-                if self.planets_retrograde[i]:
-                    out += \
-                        '<g transform="translate(74,-6)"><use transform="scale(.5)" xlink:href="#retrograde" /></g>'
+                if self.points_retrograde[i]:
+                    out += '<g transform="translate(74,-6)"><use transform="scale(.5)" xlink:href="#retrograde" /></g>'
 
                 # end of line
-                out += '</g>'
-                # offset between lines
-                li = li + 14
+                out += end_of_line
 
-        # ----------
-
-        if self.chart_type == "Transit" or self.chart_type == "Composite":
+                li = li + offset_between_lines
 
+        if self.chart_type == "Transit" or self.chart_type == "Synastry":
             if self.chart_type == "Transit":
                 out += '<g transform="translate(320, -15)">'
-                out += \
-                    f'<text text-anchor="end" style="fill:{self.colors_settings["paper_0"]}; font-size: 14px;">{self.t_name}:</text>'
+                out += f'<text text-anchor="end" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 14px;">{self.t_name}:</text>'
             else:
                 out += '<g transform="translate(380, -15)">'
-                out += \
-                    f'<text text-anchor="end" style="fill:{self.colors_settings["paper_0"]}; font-size: 14px;">{self.language_settings["planets_and_house"]} {self.t_user.name}:</text>'
-            out += '</g>'
+                out += f'<text text-anchor="end" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 14px;">{self.language_settings["planets_and_house"]} {self.t_user.name}:</text>'
+
+            out += end_of_line
 
             t_li = 10
             t_offset = 250
 
             for i in range(len(self.planets_settings)):
                 if i == 27:
                     t_li = 10
                     t_offset = -120
-                if self.planets_settings[i]['visible'] == 1:
+
+                if self.planets_settings[i]["is_active"] == 1:
                     # start of line
                     out += f'<g transform="translate({t_offset},{t_li})">'
 
                     # planet text
-                    out += f'<text text-anchor="end" style="fill:{self.colors_settings["paper_0"]}; font-size: 10px;">{self.language_settings["celestial_points"][self.planets_settings[i]["label"]]}</text>'
+                    out += f'<text text-anchor="end" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;">{self.language_settings["celestial_points"][self.planets_settings[i]["label"]]}</text>'
                     # planet symbol
                     out += f'<g transform="translate(5,-8)"><use transform="scale(0.4)" xlink:href="#{self.planets_settings[i]["name"]}" /></g>'
                     # planet degree
-                    out += '<text text-anchor="start" x="19" style="fill:%s; font-size: 10px;">%s</text>' % (
-                        self.colors_settings['paper_0'], self.__dec2deg(self.t_planets_degree[i]))
+                    out += f'<text text-anchor="start" x="19" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;">{self._dec2deg(self.t_points_deg[i])}</text>'
                     # zodiac
-                    out += '<g transform="translate(60,-8)"><use transform="scale(0.3)" xlink:href="#' + \
-                        self.zodiac[self.t_planets_sign[i]]+'" /></g>'
+                    out += f'<g transform="translate(60,-8)"><use transform="scale(0.3)" xlink:href="#{self.zodiac[self.t_points_sign[i]]["name"]}" /></g>'
+
                     # planet retrograde
-                    if self.t_planets_retrograde[i]:
-                        out += \
-                            '<g transform="translate(74,-6)"><use transform="scale(.5)" xlink:href="#retrograde" /></g>'
+                    if self.t_points_retrograde[i]:
+                        out += '<g transform="translate(74,-6)"><use transform="scale(.5)" xlink:href="#retrograde" /></g>'
 
                     # end of line
-                    out += '</g>'
-                    # offset between lines
-                    t_li = t_li + 14
-        out += '</g>'
+                    out += end_of_line
 
-        return out
+                    t_li = t_li + offset_between_lines
 
-    def __makeHousesGrid(self):
+        if end_of_line is None:
+            raise KerykeionException("End of line not found")
 
+        out += end_of_line
+        return out
+
+    def _makeHousesGrid(self):
         out = '<g transform="translate(600,-20)">'
+
         li = 10
         for i in range(12):
             if i < 9:
-                cusp = '&#160;&#160;'+str(i+1)
+                cusp = "&#160;&#160;" + str(i + 1)
             else:
-                cusp = str(i+1)
-            out += '<g transform="translate(0,'+str(li)+')">'
-            out += '<text text-anchor="end" x="40" style="fill:%s; font-size: 10px;">%s %s:</text>' % (
-                self.colors_settings['paper_0'], self.language_settings['cusp'], cusp)
-            out += '<g transform="translate(40,-8)"><use transform="scale(0.3)" xlink:href="#' + \
-                self.zodiac[self.houses_sign[i]]+'" /></g>'
-            out += '<text x="53" style="fill:%s; font-size: 10px;"> %s</text>' % (
-                self.colors_settings['paper_0'], self.__dec2deg(self.houses_list[i]["position"]))
-            out += '</g>'
+                cusp = str(i + 1)
+            out += f'<g transform="translate(0,{li})">'
+            out += f'<text text-anchor="end" x="40" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;">{self.language_settings["cusp"]} {cusp}:</text>'
+            out += f'<g transform="translate(40,-8)"><use transform="scale(0.3)" xlink:href="#{self.zodiac[self.houses_sign_graph[i]]["name"]}" /></g>'
+            out += f'<text x="53" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;"> {self._dec2deg(self.user.houses_list[i]["position"])}</text>'
+            out += "</g>"
             li = li + 14
-        out += '</g>'
 
-        # ----------
+        out += "</g>"
 
-        if self.chart_type == "Composite":
+        if self.chart_type == "Synastry":
             out += '<g transform="translate(840, -20)">'
             li = 10
             for i in range(12):
                 if i < 9:
-                    cusp = '&#160;&#160;'+str(i+1)
+                    cusp = "&#160;&#160;" + str(i + 1)
                 else:
-                    cusp = str(i+1)
-                out += '<g transform="translate(0,'+str(li)+')">'
-                out += '<text text-anchor="end" x="40" style="fill:%s; font-size: 10px;">%s %s:</text>' % (
-                    self.colors_settings['paper_0'], self.language_settings['cusp'], cusp)
-                out += '<g transform="translate(40,-8)"><use transform="scale(0.3)" xlink:href="#' + \
-                    self.zodiac[self.t_houses_sign[i]]+'" /></g>'
-                out += '<text x="53" style="fill:%s; font-size: 10px;"> %s</text>' % (
-                    self.colors_settings['paper_0'], self.__dec2deg(self.t_houses_list[i]["position"]))
-                out += '</g>'
+                    cusp = str(i + 1)
+                out += '<g transform="translate(0,' + str(li) + ')">'
+                out += f'<text text-anchor="end" x="40" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;">{self.language_settings["cusp"]} {cusp}:</text>'
+                out += f'<g transform="translate(40,-8)"><use transform="scale(0.3)" xlink:href="#{self.zodiac[self.t_houses_sign_graph[i]]["name"]}" /></g>'
+                out += f'<text x="53" style="fill:{self.chart_colors_settings["paper_0"]}; font-size: 10px;"> {self._dec2deg(self.t_user.houses_list[i]["position"])}</text>'
+                out += "</g>"
                 li = li + 14
-            out += '</g>'
+            out += "</g>"
 
         return out
 
-    def set_output_directory(self, dir_path):
-        """
-        Sets the output direcotry and returns it's path.
-        """
-        self.output_directory = Path(dir_path)
-        dir_string = f"Output direcotry set to: {self.output_directory}"
-        return (print(dir_string))
-
-    def parse_json_settings(self, settings_file, lang: str):
-        """
-        Parse the settings file.
-        """
-        with open(settings_file, 'r', encoding="utf-8", errors='ignore') as f:
-            settings = json.load(f)
-
-        self.language_settings = settings['language_settings'].get(
-            lang, "EN")
-        self.colors_settings = settings['colors']
-        self.planets_settings = settings['celestial_points']
-        self.aspects_settings = settings['aspects']
-
-    def makeTemplate(self):
+    def _createTemplateDictionary(self):
         # self.chart_type = "Transit"
         # empty element points
         self.fire = 0.0
         self.earth = 0.0
         self.air = 0.0
         self.water = 0.0
 
-        # Transit module data
-        if self.chart_type == "Transit" or self.chart_type == "Composite":
-            # grab transiting module data
-
-            self.t_planets_sign = self.t_points_sign
-            self.t_planets_degree = self.t_points_deg
-            self.t_planets_degree_ut = self.t_points_deg_ut
-            self.t_planets_retrograde = self.t_points_retrograde
-            self.t_houses_list = self.t_user.houses_list
-            self.t_houses_sign = self.t_houses_sign_graph
-            self.t_houses_degree_ut = self.t_user.houses_degree_ut
-
-        # grab normal module data
-        self.planets_sign = self.points_sign
-        self.planets_degree = self.points_deg
-        self.planets_degree_ut = self.points_deg_ut
-        self.planets_retrograde = self.points_retrograde
-        self.houses_list = self.user.houses_list
-        self.houses_sign = self.houses_sign_graph
-        self.houses_degree_ut = self.user.houses_degree_ut
-        self.lunar_phase = self.user.lunar_phase
-        #
-
         # width and height from screen
         ratio = float(self.screen_width) / float(self.screen_height)
         if ratio < 1.3:  # 1280x1024
             wm_off = 130
         else:  # 1024x768, 800x600, 1280x800, 1680x1050
             wm_off = 100
 
@@ -1366,224 +1309,250 @@
         # svgWidth=(770.0*svgHeight)/540.0
         # svgWidth=float(self.screen_width)-25.0
         rotate = "0"
         translate = "0"
         # Defoult:
         # viewbox = '0 0 772.2 546.0' #297mm * 2.6 + 210mm * 2.6
         if self.chart_type == "Natal":
-            viewbox = '0 0 772.2 546.0'  # 297mm * 2.6 + 210mm * 2.6
+            viewbox = "0 0 772.2 546.0"  # 297mm * 2.6 + 210mm * 2.6
         else:
-            viewbox = '0 0 1000 546.0'
+            viewbox = "0 0 1000 546.0"
 
         # template dictionary
-        td = dict()
+        td: ChartTemplateModel = dict()
         r = 240
-        self.c1 = 0
-        self.c2 = 36
-        self.c3 = 120
+
+        if self.chart_type == "ExternalNatal":
+            self.c1 = 56
+            self.c2 = 92
+            self.c3 = 112
+        else:
+            self.c1 = 0
+            self.c2 = 36
+            self.c3 = 120
 
         # transit
-        if self.chart_type == "Transit" or self.chart_type == "Composite":
-            td['transitRing'] = self.__transitRing(r)
-            td['degreeRing'] = self.__degreeTransitRing(r)
+        if self.chart_type == "Transit" or self.chart_type == "Synastry":
+            td["transitRing"] = self._transitRing(r)
+            td["degreeRing"] = self._degreeTransitRing(r)
+
             # circles
-            td['c1'] = 'cx="' + str(r) + '" cy="' + \
-                str(r) + '" r="' + str(r-36) + '"'
-            td['c1style'] = 'fill: none; stroke: %s; stroke-width: 1px; stroke-opacity:.4;' % (
-                self.colors_settings['zodiac_transit_ring_2'])
-            td['c2'] = 'cx="' + str(r) + '" cy="' + \
-                str(r) + '" r="' + str(r-72) + '"'
-            td['c2style'] = 'fill: %s; fill-opacity:.4; stroke: %s; stroke-opacity:.4; stroke-width: 1px' % (
-                self.colors_settings['paper_1'], self.colors_settings['zodiac_transit_ring_1'])
-            td['c3'] = 'cx="' + str(r) + '" cy="' + \
-                str(r) + '" r="' + str(r-160) + '"'
-            td['c3style'] = 'fill: %s; fill-opacity:.8; stroke: %s; stroke-width: 1px' % (
-                self.colors_settings['paper_1'], self.colors_settings['zodiac_transit_ring_0'])
-            td['makeAspects'] = self.__makeAspectsTransit(r, (r-160))
-            td['makeAspectGrid'] = self.__makeAspectTransitGrid(r)
-            td['makePatterns'] = ''
-            td['chart_width'] = self.full_width
+            td["c1"] = f'cx="{r}" cy="{r}" r="{r - 36}"'
+            td["c1style"] = f'fill: none; stroke: {self.chart_colors_settings["zodiac_transit_ring_2"]}; stroke-width: 1px; stroke-opacity:.4;'
+            td["c2"] = 'cx="' + str(r) + '" cy="' + str(r) + '" r="' + str(r - 72) + '"'
+            td["c2style"] = f"fill: {self.chart_colors_settings['paper_1']}; fill-opacity:.4; stroke: {self.chart_colors_settings['zodiac_transit_ring_1']}; stroke-opacity:.4; stroke-width: 1px"
+
+            td["c3"] = 'cx="' + str(r) + '" cy="' + str(r) + '" r="' + str(r - 160) + '"'
+            td["c3style"] = f"fill: {self.chart_colors_settings['paper_1']}; fill-opacity:.8; stroke: {self.chart_colors_settings['zodiac_transit_ring_0']}; stroke-width: 1px"
+
+            td["makeAspects"] = self._makeAspectsTransit(r, (r - 160))
+            td["makeAspectGrid"] = self._makeAspectTransitGrid(r)
+            td["makePatterns"] = ""
+            td["chart_width"] = self.full_width
         else:
-            td['transitRing'] = ""
-            td['degreeRing'] = self.__degreeRing(r)
+            td["transitRing"] = ""
+            td["degreeRing"] = self._degreeRing(r)
+
             # circles
-            td['c1'] = 'cx="' + str(r) + '" cy="' + \
-                str(r) + '" r="' + str(r-self.c1) + '"'
-            td['c1style'] = 'fill: none; stroke: %s; stroke-width: 1px; ' % (
-                self.colors_settings['zodiac_radix_ring_2'])
-            td['c2'] = 'cx="' + str(r) + '" cy="' + \
-                str(r) + '" r="' + str(r-self.c2) + '"'
-            td['c2style'] = 'fill: %s; fill-opacity:.2; stroke: %s; stroke-opacity:.4; stroke-width: 1px' % (
-                self.colors_settings['paper_1'], self.colors_settings['zodiac_radix_ring_1'])
-            td['c3'] = 'cx="' + str(r) + '" cy="' + \
-                str(r) + '" r="' + str(r-self.c3) + '"'
-            td['c3style'] = 'fill: %s; fill-opacity:.8; stroke: %s; stroke-width: 1px' % (
-                self.colors_settings['paper_1'], self.colors_settings['zodiac_radix_ring_0'])
-            td['makeAspects'] = self.__makeAspects(r, (r-self.c3))
-            td['makeAspectGrid'] = self.__makeAspectGrid(r)
-            td['makePatterns'] = self.__makePatterns()
-            td['chart_width'] = self.natal_width
-
-        td['circleX'] = str(0)
-        td['circleY'] = str(0)
-        td['svgWidth'] = str(svgWidth)
-        td['svgHeight'] = str(svgHeight)
-        td['viewbox'] = viewbox
-        if self.chart_type == "Composite":
-            td['stringTitle'] = f"{self.name} {self.language_settings['&']} {self.t_user.name}"
+            td["c1"] = f'cx="{r}" cy="{r}" r="{r - self.c1}"'
+            td["c1style"] = f'fill: none; stroke: {self.chart_colors_settings["zodiac_radix_ring_2"]}; stroke-width: 1px; '
+            td["c2"] = f'cx="{r}" cy="{r}" r="{r - self.c2}"'
+            td["c2style"] = f'fill: {self.chart_colors_settings["paper_1"]}; fill-opacity:.2; stroke: {self.chart_colors_settings["zodiac_radix_ring_1"]}; stroke-opacity:.4; stroke-width: 1px'
+            td["c3"] = f'cx="{r}" cy="{r}" r="{r - self.c3}"'
+            td["c3style"] = f'fill: {self.chart_colors_settings["paper_1"]}; fill-opacity:.8; stroke: {self.chart_colors_settings["zodiac_radix_ring_0"]}; stroke-width: 1px'
+            td["makeAspects"] = self._makeAspects(r, (r - self.c3))
+            td["makeAspectGrid"] = self._makeAspectGrid(r)
+            td["makePatterns"] = self._makePatterns()
+            td["chart_width"] = self.natal_width
+
+        td["circleX"] = str(0)
+        td["circleY"] = str(0)
+        td["svgWidth"] = str(svgWidth)
+        td["svgHeight"] = str(svgHeight)
+        td["viewbox"] = viewbox
+
+        if self.chart_type == "Synastry":
+            td["stringTitle"] = f"{self.name} {self.language_settings['and_word']} {self.t_user.name}"
+
         elif self.chart_type == "Transit":
-            td['stringTitle'] = f"{self.language_settings['transits']} {self.t_user.day}/{self.t_user.month}/{self.t_user.year}"
+            td["stringTitle"] = f"{self.language_settings['transits']} {self.t_user.day}/{self.t_user.month}/{self.t_user.year}"
+
         else:
-            td['stringTitle'] = self.name
+            td["stringTitle"] = self.name
 
         # Tipo di carta
-        if self.chart_type == "Composite" or self.name == "Transit":
-            td['stringName'] = f"{self.name}:"
+        if self.chart_type == "Synastry" or self.name == "Transit":
+            td["stringName"] = f"{self.name}:"
         else:
-            td['stringName'] = f'{self.language_settings["info"]}:'
+            td["stringName"] = f'{self.language_settings["info"]}:'
 
         # bottom left
-
-        td['bottomLeft1'] = ''
-        td['bottomLeft2'] = ''
-        td['bottomLeft3'] = f'{self.language_settings.get("lunar_phase", "Lunar Phase")}: {self.language_settings.get("day", "Day")} {self.lunar_phase.get("moon_phase", "")}'
-        td['bottomLeft4'] = ''
+        td["bottomLeft1"] = ""
+        td["bottomLeft2"] = ""
+        td["bottomLeft3"] = f'{self.language_settings.get("lunar_phase", "Lunar Phase")}: {self.language_settings.get("day", "Day")} {self.user.lunar_phase.get("moon_phase", "")}'
+        td["bottomLeft4"] = ""
 
         # lunar phase
-        deg = self.lunar_phase['degrees_between_s_m']
+        deg = self.user.lunar_phase["degrees_between_s_m"]
 
-        if(deg < 90.0):
+        lffg = None
+        lfbg = None
+        lfcx = None
+        lfr = None
+
+        if deg < 90.0:
             maxr = deg
-            if(deg > 80.0):
-                maxr = maxr*maxr
-            lfcx = 20.0+(deg/90.0)*(maxr+10.0)
-            lfr = 10.0+(deg/90.0)*maxr
-            lffg, lfbg = self.colors_settings["lunar_phase_0"], self.colors_settings["lunar_phase_1"]
-
-        elif(deg < 180.0):
-            maxr = 180.0-deg
-            if(deg < 100.0):
-                maxr = maxr*maxr
-            lfcx = 20.0+((deg-90.0)/90.0*(maxr+10.0))-(maxr+10.0)
-            lfr = 10.0+maxr-((deg-90.0)/90.0*maxr)
-            lffg, lfbg = self.colors_settings["lunar_phase_1"], self.colors_settings["lunar_phase_0"]
-
-        elif(deg < 270.0):
-            maxr = deg-180.0
-            if(deg > 260.0):
-                maxr = maxr*maxr
-            lfcx = 20.0+((deg-180.0)/90.0*(maxr+10.0))
-            lfr = 10.0+((deg-180.0)/90.0*maxr)
-            lffg, lfbg = self.colors_settings["lunar_phase_1"], self.colors_settings["lunar_phase_0"]
-
-        elif(deg < 361):
-            maxr = 360.0-deg
-            if(deg < 280.0):
-                maxr = maxr*maxr
-            lfcx = 20.0+((deg-270.0)/90.0*(maxr+10.0))-(maxr+10.0)
-            lfr = 10.0+maxr-((deg-270.0)/90.0*maxr)
-            lffg, lfbg = self.colors_settings["lunar_phase_0"], self.colors_settings["lunar_phase_1"]
-
-        td['lunar_phase_fg'] = lffg
-        td['lunar_phase_bg'] = lfbg
-        td['lunar_phase_cx'] = lfcx
-        td['lunar_phase_r'] = lfr
-        td['lunar_phase_outline'] = self.colors_settings["lunar_phase_2"]
+            if deg > 80.0:
+                maxr = maxr * maxr
+            lfcx = 20.0 + (deg / 90.0) * (maxr + 10.0)
+            lfr = 10.0 + (deg / 90.0) * maxr
+            lffg = self.chart_colors_settings["lunar_phase_0"]
+            lfbg = self.chart_colors_settings["lunar_phase_1"]
+
+        elif deg < 180.0:
+            maxr = 180.0 - deg
+            if deg < 100.0:
+                maxr = maxr * maxr
+            lfcx = 20.0 + ((deg - 90.0) / 90.0 * (maxr + 10.0)) - (maxr + 10.0)
+            lfr = 10.0 + maxr - ((deg - 90.0) / 90.0 * maxr)
+            lffg = self.chart_colors_settings["lunar_phase_1"]
+            lfbg = self.chart_colors_settings["lunar_phase_0"]
+
+        elif deg < 270.0:
+            maxr = deg - 180.0
+            if deg > 260.0:
+                maxr = maxr * maxr
+            lfcx = 20.0 + ((deg - 180.0) / 90.0 * (maxr + 10.0))
+            lfr = 10.0 + ((deg - 180.0) / 90.0 * maxr)
+            lffg, lfbg = self.chart_colors_settings["lunar_phase_1"], self.chart_colors_settings["lunar_phase_0"]
+
+        elif deg < 361:
+            maxr = 360.0 - deg
+            if deg < 280.0:
+                maxr = maxr * maxr
+            lfcx = 20.0 + ((deg - 270.0) / 90.0 * (maxr + 10.0)) - (maxr + 10.0)
+            lfr = 10.0 + maxr - ((deg - 270.0) / 90.0 * maxr)
+            lffg, lfbg = self.chart_colors_settings["lunar_phase_0"], self.chart_colors_settings["lunar_phase_1"]
+
+        if lffg is None or lfbg is None or lfcx is None or lfr is None:
+            raise KerykeionException("Lunar phase error")
+
+        td["lunar_phase_fg"] = lffg
+        td["lunar_phase_bg"] = lfbg
+        td["lunar_phase_cx"] = lfcx
+        td["lunar_phase_r"] = lfr
+        td["lunar_phase_outline"] = self.chart_colors_settings["lunar_phase_2"]
 
         # rotation based on latitude
-        td['lunar_phase_rotate'] = (-90.0-self.geolat)
+        td["lunar_phase_rotate"] = -90.0 - self.geolat
 
         # stringlocation
         if len(self.location) > 35:
             split = self.location.split(",")
             if len(split) > 1:
-                td['stringLocation'] = split[0]+", "+split[-1]
-                if len(td['stringLocation']) > 35:
-                    td['stringLocation'] = td['stringLocation'][:35]+"..."
+                td["stringLocation"] = split[0] + ", " + split[-1]
+                if len(td["stringLocation"]) > 35:
+                    td["stringLocation"] = td["stringLocation"][:35] + "..."
             else:
-                td['stringLocation'] = self.location[:35]+"..."
+                td["stringLocation"] = self.location[:35] + "..."
         else:
-            td['stringLocation'] = self.location
+            td["stringLocation"] = self.location
 
-        td['stringDateTime'] = f'{self.user.year}-{self.user.month}-{self.user.day} {self.user.hour:02d}:{self.user.minute:02d}'
+        td["stringDateTime"] = f"{self.user.year}-{self.user.month}-{self.user.day} {self.user.hour:02d}:{self.user.minute:02d}"
 
-        if self.chart_type == "Composite":
-            td['stringLat'] = f'{self.t_user.name}: '
-            td['stringLon'] = self.t_user.city
-            td['stringPosition'] = f'{self.t_user.year}-{self.t_user.month}-{self.t_user.day} {self.t_user.hour:02d}:{self.t_user.minute:02d}'
+        if self.chart_type == "Synastry":
+            td["stringLat"] = f"{self.t_user.name}: "
+            td["stringLon"] = self.t_user.city
+            td["stringPosition"] = f"{self.t_user.year}-{self.t_user.month}-{self.t_user.day} {self.t_user.hour:02d}:{self.t_user.minute:02d}"
 
         else:
-            td['stringLat'] = "%s: %s" % (
-                self.language_settings['latitude'], self.__lat2str(self.geolat))
-            td['stringLon'] = "%s: %s" % (
-                self.language_settings['longitude'], self.__lon2str(self.geolon))
-            td['stringPosition'] = f"{self.language_settings['type']}: {self.charttype}"
+            td["stringLat"] = f"{self.language_settings['latitude']}: {self._lat2str(self.geolat)}"
+            td["stringLon"] = f"{self.language_settings['longitude']}: {self._lon2str(self.geolon)}"
+            td["stringPosition"] = f"{self.language_settings['type']}: {self.charttype}"
 
         # paper_color_X
-        td['paper_color_0'] = self.colors_settings["paper_0"]
-        td['paper_color_1'] = self.colors_settings["paper_1"]
+        td["paper_color_0"] = self.chart_colors_settings["paper_0"]
+        td["paper_color_1"] = self.chart_colors_settings["paper_1"]
 
         # planets_color_X
         for i in range(len(self.planets_settings)):
-            td['planets_color_%s' %
-                (i)] = self.colors_settings["planet_%s" % (i)]
+            planet_id = self.planets_settings[i]["id"]
+            td[f"planets_color_{planet_id}"] = self.planets_settings[i]["color"]
 
         # zodiac_color_X
         for i in range(12):
-            td['zodiac_color_%s' %
-                (i)] = self.colors_settings["zodiac_icon_%s" % (i)]
+            td[f"zodiac_color_{i}"] = self.chart_colors_settings[f"zodiac_icon_{i}"]
 
         # orb_color_X
         for i in range(len(self.aspects_settings)):
-            td['orb_color_%s' % (self.aspects_settings[i]['degree'])] = self.colors_settings["aspect_%s" % (
-                self.aspects_settings[i]['degree'])]
+            td[f"orb_color_{self.aspects_settings[i]['degree']}"] = self.aspects_settings[i]['color']
 
         # config
-        td['cfgZoom'] = str(self.zoom)
-        td['cfgRotate'] = rotate
-        td['cfgTranslate'] = translate
+        td["cfgZoom"] = str(self.zoom)
+        td["cfgRotate"] = rotate
+        td["cfgTranslate"] = translate
 
         # functions
-        td['makeZodiac'] = self.__makeZodiac(r)
-        td['makeHouses'] = self.__makeHouses(r)
-        td['makePlanets'] = self.__makePlanets(r)
-        td['makeElements'] = self.__makeElements(r)
-        td['makePlanetGrid'] = self.__makePlanetGrid()
-        td['makeHousesGrid'] = self.__makeHousesGrid()
+        td["makeZodiac"] = self._makeZodiac(r)
+        td["makeHouses"] = self._makeHouses(r)
+        td["makePlanets"] = self._make_planets(r)
+        td["makeElements"] = self._makeElements(r)
+        td["makePlanetGrid"] = self._makePlanetGrid()
+        td["makeHousesGrid"] = self._makeHousesGrid()
+
+        return td
+
+    def makeTemplate(self):
+        """Creates the template for the SVG file"""
+        td = self._createTemplateDictionary()
 
         # read template
-        with open(self.xml_svg, "r", encoding="utf-8", errors='ignore') as output_file:
+        with open(self.xml_svg, "r", encoding="utf-8", errors="ignore") as output_file:
             f = open(self.xml_svg)
             template = Template(f.read()).substitute(td)
 
         # return filename
 
-        return template.replace("\"", "'")
+        logger.debug(f"Template dictionary keys: {td.keys()}")
+
+        self._createTemplateDictionary()
+        return template.replace('"', "'")
 
     def makeSVG(self):
         """Prints out the SVG file in the specifide folder"""
 
         if not (self.template):
             self.template = self.makeTemplate()
 
-        self.chartname = self.output_directory / \
-            f'{self.name}{self.chart_type}Chart.svg'
+        self.chartname = self.output_directory / f"{self.name}{self.chart_type}Chart.svg"
 
-        with open(self.chartname, "w", encoding='utf-8', errors='ignore') as output_file:
+        with open(self.chartname, "w", encoding="utf-8", errors="ignore") as output_file:
             output_file.write(self.template)
 
         return print(f"SVG Generated Correctly in: {self.chartname}")
 
 
 if __name__ == "__main__":
+    first = AstrologicalSubject("John Lennon", 1940, 10, 9, 10, 30, "Liverpool", "GB")
+    second = AstrologicalSubject("Paul McCartney", 1942, 6, 18, 15, 30, "Liverpool", "GB")
+
+    # Internal Natal Chart
+    internal_natal_chart = KerykeionChartSVG(first)
+    internal_natal_chart.makeSVG()
+
+    # External Natal Chart
+    external_natal_chart = KerykeionChartSVG(first, "ExternalNatal", second)
+    external_natal_chart.makeSVG()
+
+    # Synastry Chart
+    synastry_chart = KerykeionChartSVG(first, "Synastry", second)
+    synastry_chart.makeSVG()
+
+    # Transits Chart
+    transits_chart = KerykeionChartSVG(first, "Transit", second)
+    transits_chart.makeSVG()
+
+
+
+
 
-    first = KrInstance("Jack", 1990, 6, 15, 15, 15, "Roma")
-    second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma")
 
-    name = MakeSvgInstance(first, chart_type="Composite",
-                           second_obj=second, lang="IT")
-    # name.output_directory = Path.home() / "charts"
-    template = name.makeTemplate()
-    name.makeSVG()
-    print(name.aspects_list[-1])
-    name.makeSVG()
-    print(template)
```

### Comparing `kerykeion-4.0a5/kerykeion/charts/templates/basic.xml` & `kerykeion-4.0rc1/kerykeion/charts/templates/chart.xml`

 * *Files 24% similar despite different names*

```diff
@@ -1,3535 +1,4368 @@
 00000000: 3c3f 786d 6c20 7665 7273 696f 6e3d 2731  <?xml version='1
 00000010: 2e30 2720 656e 636f 6469 6e67 3d27 5554  .0' encoding='UT
-00000020: 462d 3827 3f3e 3c21 444f 4354 5950 4520  F-8'?><!DOCTYPE 
-00000030: 7376 6720 5055 424c 4943 2027 2d2f 2f57  svg PUBLIC '-//W
-00000040: 3343 2f2f 4454 4420 5356 4720 312e 312f  3C//DTD SVG 1.1/
-00000050: 2f45 4e27 2027 6874 7470 3a2f 2f77 7777  /EN' 'http://www
-00000060: 2e77 332e 6f72 672f 4772 6170 6869 6373  .w3.org/Graphics
-00000070: 2f53 5647 2f31 2e31 2f44 5444 2f73 7667  /SVG/1.1/DTD/svg
-00000080: 3131 2e64 7464 273e 3c21 2d2d 2d20 5468  11.dtd'><!--- Th
-00000090: 6973 2066 696c 6520 6973 2070 6172 7420  is file is part 
-000000a0: 6f66 204b 6572 796b 6569 6f6e 2061 6e64  of Kerykeion and
-000000b0: 2069 7320 6261 7365 6420 6f6e 204f 7065   is based on Ope
-000000c0: 6e41 7374 726f 2e6f 7267 202d 2d3e 3c73  nAstro.org --><s
-000000d0: 7667 2078 6d6c 6e73 3d27 6874 7470 3a2f  vg xmlns='http:/
-000000e0: 2f77 7777 2e77 332e 6f72 672f 3230 3030  /www.w3.org/2000
-000000f0: 2f73 7667 2720 786d 6c6e 733a 786c 696e  /svg' xmlns:xlin
-00000100: 6b3d 2768 7474 703a 2f2f 7777 772e 7733  k='http://www.w3
-00000110: 2e6f 7267 2f31 3939 392f 786c 696e 6b27  .org/1999/xlink'
-00000120: 2077 6964 7468 3d27 3130 3025 2720 6865   width='100%' he
-00000130: 6967 6874 3d27 3130 3025 2720 7669 6577  ight='100%' view
-00000140: 426f 783d 2730 2030 2035 3530 2035 3530  Box='0 0 550 550
-00000150: 2720 7072 6573 6572 7665 4173 7065 6374  ' preserveAspect
-00000160: 5261 7469 6f3d 2778 4d69 6459 4d69 6427  Ratio='xMidYMid'
-00000170: 3e3c 7469 746c 653e 4b65 7279 6b65 696f  ><title>Kerykeio
-00000180: 6e3c 2f74 6974 6c65 3e3c 6720 7472 616e  n</title><g tran
-00000190: 7366 6f72 6d3d 2774 7261 6e73 6c61 7465  sform='translate
-000001a0: 2824 6366 6754 7261 6e73 6c61 7465 2927  ($cfgTranslate)'
-000001b0: 3e3c 6720 7472 616e 7366 6f72 6d3d 2772  ><g transform='r
-000001c0: 6f74 6174 6528 2463 6667 526f 7461 7465  otate($cfgRotate
-000001d0: 2927 3e3c 6720 7472 616e 7366 6f72 6d3d  )'><g transform=
-000001e0: 2773 6361 6c65 2824 6366 675a 6f6f 6d29  'scale($cfgZoom)
-000001f0: 273e 3c72 6563 7420 783d 2730 2720 793d  '><rect x='0' y=
-00000200: 2730 2720 7769 6474 683d 2735 3530 2720  '0' width='550' 
-00000210: 6865 6967 6874 3d27 3535 3027 2073 7479  height='550' sty
-00000220: 6c65 3d27 6669 6c6c 3a20 2470 6170 6572  le='fill: $paper
-00000230: 5f63 6f6c 6f72 5f31 3b27 202f 3e3c 7465  _color_1;' /><te
-00000240: 7874 2078 3d27 3230 2720 793d 2733 3027  xt x='20' y='30'
-00000250: 2073 7479 6c65 3d27 6669 6c6c 3a20 2470   style='fill: $p
-00000260: 6170 6572 5f63 6f6c 6f72 5f30 3b20 666f  aper_color_0; fo
-00000270: 6e74 2d73 697a 653a 2032 3470 7827 3e24  nt-size: 24px'>$
-00000280: 7374 7269 6e67 5469 746c 653c 2f74 6578  stringTitle</tex
-00000290: 743e 3c74 6578 7420 783d 2732 3027 2079  t><text x='20' y
-000002a0: 3d27 3530 2720 7374 796c 653d 2766 696c  ='50' style='fil
-000002b0: 6c3a 2024 7061 7065 725f 636f 6c6f 725f  l: $paper_color_
-000002c0: 303b 2066 6f6e 742d 7369 7a65 3a20 3131  0; font-size: 11
-000002d0: 7078 273e 2473 7472 696e 674e 616d 653c  px'>$stringName<
-000002e0: 2f74 6578 743e 3c74 6578 7420 783d 2732  /text><text x='2
-000002f0: 3027 2079 3d27 3632 2720 7374 796c 653d  0' y='62' style=
-00000300: 2766 696c 6c3a 2024 7061 7065 725f 636f  'fill: $paper_co
-00000310: 6c6f 725f 303b 2066 6f6e 742d 7369 7a65  lor_0; font-size
-00000320: 3a20 3131 7078 273e 2473 7472 696e 674c  : 11px'>$stringL
-00000330: 6f63 6174 696f 6e3c 2f74 6578 743e 3c74  ocation</text><t
-00000340: 6578 7420 783d 2732 3027 2079 3d27 3734  ext x='20' y='74
-00000350: 2720 7374 796c 653d 2766 696c 6c3a 2024  ' style='fill: $
-00000360: 7061 7065 725f 636f 6c6f 725f 303b 2066  paper_color_0; f
-00000370: 6f6e 742d 7369 7a65 3a20 3131 7078 273e  ont-size: 11px'>
-00000380: 2473 7472 696e 6744 6174 6554 696d 653c  $stringDateTime<
-00000390: 2f74 6578 743e 3c74 6578 7420 783d 2732  /text><text x='2
-000003a0: 3027 2079 3d27 3836 2720 7374 796c 653d  0' y='86' style=
-000003b0: 2766 696c 6c3a 2024 7061 7065 725f 636f  'fill: $paper_co
-000003c0: 6c6f 725f 303b 2066 6f6e 742d 7369 7a65  lor_0; font-size
-000003d0: 3a20 3131 7078 273e 2473 7472 696e 674c  : 11px'>$stringL
-000003e0: 6174 3c2f 7465 7874 3e3c 7465 7874 2078  at</text><text x
-000003f0: 3d27 3230 2720 793d 2739 3827 2073 7479  ='20' y='98' sty
-00000400: 6c65 3d27 6669 6c6c 3a20 2470 6170 6572  le='fill: $paper
-00000410: 5f63 6f6c 6f72 5f30 3b20 666f 6e74 2d73  _color_0; font-s
-00000420: 697a 653a 2031 3170 7827 3e24 7374 7269  ize: 11px'>$stri
-00000430: 6e67 4c6f 6e3c 2f74 6578 743e 3c74 6578  ngLon</text><tex
-00000440: 7420 783d 2732 3027 2079 3d27 3131 3027  t x='20' y='110'
-00000450: 2073 7479 6c65 3d27 6669 6c6c 3a20 2470   style='fill: $p
-00000460: 6170 6572 5f63 6f6c 6f72 5f30 3b20 666f  aper_color_0; fo
-00000470: 6e74 2d73 697a 653a 2031 3170 7827 3e24  nt-size: 11px'>$
-00000480: 7374 7269 6e67 506f 7369 7469 6f6e 3c2f  stringPosition</
-00000490: 7465 7874 3e3c 7465 7874 2078 3d27 3230  text><text x='20
-000004a0: 2720 793d 2734 3830 2720 7374 796c 653d  ' y='480' style=
-000004b0: 2766 696c 6c3a 2024 7061 7065 725f 636f  'fill: $paper_co
-000004c0: 6c6f 725f 303b 2066 6f6e 742d 7369 7a65  lor_0; font-size
-000004d0: 3a20 3130 7078 273e 2462 6f74 746f 6d4c  : 10px'>$bottomL
-000004e0: 6566 7431 3c2f 7465 7874 3e3c 7465 7874  eft1</text><text
-000004f0: 2078 3d27 3230 2720 793d 2734 3934 2720   x='20' y='494' 
-00000500: 7374 796c 653d 2766 696c 6c3a 2024 7061  style='fill: $pa
-00000510: 7065 725f 636f 6c6f 725f 303b 2066 6f6e  per_color_0; fon
-00000520: 742d 7369 7a65 3a20 3130 7078 273e 2462  t-size: 10px'>$b
-00000530: 6f74 746f 6d4c 6566 7432 3c2f 7465 7874  ottomLeft2</text
-00000540: 3e3c 7465 7874 2078 3d27 3230 2720 793d  ><text x='20' y=
-00000550: 2735 3038 2720 7374 796c 653d 2766 696c  '508' style='fil
-00000560: 6c3a 2024 7061 7065 725f 636f 6c6f 725f  l: $paper_color_
-00000570: 303b 2066 6f6e 742d 7369 7a65 3a20 3130  0; font-size: 10
-00000580: 7078 273e 2462 6f74 746f 6d4c 6566 7433  px'>$bottomLeft3
-00000590: 3c2f 7465 7874 3e3c 7465 7874 2078 3d27  </text><text x='
-000005a0: 3230 2720 793d 2735 3232 2720 7374 796c  20' y='522' styl
-000005b0: 653d 2766 696c 6c3a 2024 7061 7065 725f  e='fill: $paper_
-000005c0: 636f 6c6f 725f 303b 2066 6f6e 742d 7369  color_0; font-si
-000005d0: 7a65 3a20 3130 7078 273e 2462 6f74 746f  ze: 10px'>$botto
-000005e0: 6d4c 6566 7434 3c2f 7465 7874 3e3c 212d  mLeft4</text><!-
-000005f0: 2d20 4c75 6e61 7220 5068 6173 6520 2d2d  - Lunar Phase --
-00000600: 3e3c 6720 7472 616e 7366 6f72 6d3d 2774  ><g transform='t
-00000610: 7261 6e73 6c61 7465 2832 302c 3531 3829  ranslate(20,518)
-00000620: 273e 3c67 2074 7261 6e73 666f 726d 3d27  '><g transform='
-00000630: 726f 7461 7465 2824 6c75 6e61 725f 7068  rotate($lunar_ph
-00000640: 6173 655f 726f 7461 7465 2032 3020 3130  ase_rotate 20 10
-00000650: 2927 3e3c 6465 6673 3e3c 636c 6970 5061  )'><defs><clipPa
-00000660: 7468 2069 643d 2763 7574 2d6f 6666 2d63  th id='cut-off-c
-00000670: 6972 636c 6527 3e3c 6369 7263 6c65 2063  ircle'><circle c
-00000680: 783d 2732 3027 2063 793d 2731 3027 2072  x='20' cy='10' r
-00000690: 3d27 3130 2720 2f3e 3c2f 636c 6970 5061  ='10' /></clipPa
-000006a0: 7468 3e3c 2f64 6566 733e 3c63 6972 636c  th></defs><circl
-000006b0: 6520 6378 3d27 3230 2720 6379 3d27 3130  e cx='20' cy='10
-000006c0: 2720 723d 2731 3027 2073 7479 6c65 3d27  ' r='10' style='
-000006d0: 6669 6c6c 3a20 246c 756e 6172 5f70 6861  fill: $lunar_pha
-000006e0: 7365 5f62 673b 2720 2f3e 3c63 6972 636c  se_bg;' /><circl
-000006f0: 6520 6378 3d27 246c 756e 6172 5f70 6861  e cx='$lunar_pha
-00000700: 7365 5f63 7827 2063 793d 2731 3027 2072  se_cx' cy='10' r
-00000710: 3d27 246c 756e 6172 5f70 6861 7365 5f72  ='$lunar_phase_r
-00000720: 2720 7374 796c 653d 2766 696c 6c3a 2024  ' style='fill: $
-00000730: 6c75 6e61 725f 7068 6173 655f 6667 2720  lunar_phase_fg' 
-00000740: 636c 6970 2d70 6174 683d 2775 726c 2823  clip-path='url(#
-00000750: 6375 742d 6f66 662d 6369 7263 6c65 2927  cut-off-circle)'
-00000760: 202f 3e3c 6369 7263 6c65 2063 783d 2732   /><circle cx='2
-00000770: 3027 2063 793d 2731 3027 2072 3d27 3130  0' cy='10' r='10
-00000780: 2720 7374 796c 653d 2766 696c 6c3a 206e  ' style='fill: n
-00000790: 6f6e 653b 2073 7472 6f6b 653a 2024 6c75  one; stroke: $lu
-000007a0: 6e61 725f 7068 6173 655f 6f75 746c 696e  nar_phase_outlin
-000007b0: 653b 2073 7472 6f6b 652d 7769 6474 683a  e; stroke-width:
-000007c0: 2030 2e35 7078 3b20 7374 726f 6b65 2d6f   0.5px; stroke-o
-000007d0: 7061 6369 7479 3a20 2e35 3b27 202f 3e3c  pacity: .5;' /><
-000007e0: 2f67 3e3c 2f67 3e3c 212d 2d20 506c 616e  /g></g><!-- Plan
-000007f0: 6574 7320 2832 3478 3234 2920 2d2d 3e3c  ets (24x24) --><
-00000800: 7379 6d62 6f6c 2069 643d 2753 756e 273e  symbol id='Sun'>
-00000810: 3c67 2074 7261 6e73 666f 726d 3d27 7472  <g transform='tr
-00000820: 616e 736c 6174 6528 312c 3429 273e 3c63  anslate(1,4)'><c
-00000830: 6972 636c 6520 6378 3d27 3130 2720 6379  ircle cx='10' cy
-00000840: 3d27 3130 2720 723d 2739 2720 7374 796c  ='10' r='9' styl
-00000850: 653d 2766 696c 6c3a 206e 6f6e 653b 2073  e='fill: none; s
-00000860: 7472 6f6b 653a 2024 706c 616e 6574 735f  troke: $planets_
-00000870: 636f 6c6f 725f 303b 2073 7472 6f6b 652d  color_0; stroke-
-00000880: 7769 6474 683a 2032 7078 3b27 202f 3e3c  width: 2px;' /><
-00000890: 6369 7263 6c65 2063 783d 2731 3027 2063  circle cx='10' c
-000008a0: 793d 2731 3027 2072 3d27 3227 2073 7479  y='10' r='2' sty
-000008b0: 6c65 3d27 6669 6c6c 3a20 2470 6c61 6e65  le='fill: $plane
-000008c0: 7473 5f63 6f6c 6f72 5f30 3b27 202f 3e3c  ts_color_0;' /><
-000008d0: 2f67 3e3c 2f73 796d 626f 6c3e 3c73 796d  /g></symbol><sym
-000008e0: 626f 6c20 6964 3d27 4d6f 6f6e 273e 3c67  bol id='Moon'><g
-000008f0: 2074 7261 6e73 666f 726d 3d27 7472 616e   transform='tran
-00000900: 736c 6174 6528 342c 3329 273e 3c67 2074  slate(4,3)'><g t
-00000910: 7261 6e73 666f 726d 3d27 7363 616c 6528  ransform='scale(
-00000920: 2e38 2927 3e3c 7061 7468 2064 3d27 4d20  .8)'><path d='M 
-00000930: 332e 3636 3339 3139 342c 312e 3033 3038  3.6639194,1.0308
-00000940: 3530 3920 4320 322e 3734 3938 3439 342c  509 C 2.7498494,
-00000950: 312e 3036 3536 3330 3920 312e 3837 3231  1.0656309 1.8721
-00000960: 3339 342c 312e 3231 3339 3230 3920 312e  394,1.2139209 1.
-00000970: 3032 3834 3639 342c 312e 3435 3933 3830  0284694,1.459380
-00000980: 3920 4320 352e 3537 3239 3739 342c 322e  9 C 5.5729794,2.
-00000990: 3739 3939 3630 3920 382e 3839 3139 3739  7999609 8.891979
-000009a0: 342c 372e 3032 3432 3230 3920 382e 3839  4,7.0242209 8.89
-000009b0: 3139 3739 342c 3132 2e30 3031 3139 3120  19794,12.001191 
-000009c0: 4320 382e 3839 3139 3739 342c 3136 2e39  C 8.8919794,16.9
-000009d0: 3738 3136 3120 352e 3537 3239 3739 342c  78161 5.5729794,
-000009e0: 3231 2e32 3032 3431 3120 312e 3032 3834  21.202411 1.0284
-000009f0: 3639 342c 3232 2e35 3433 3030 3120 4320  694,22.543001 C 
-00000a00: 322e 3030 3139 3239 342c 3232 2e38 3236  2.0019294,22.826
-00000a10: 3232 3120 332e 3032 3739 3839 342c 3232  221 3.0279894,22
-00000a20: 2e39 3731 3533 3120 342e 3039 3234 3439  .971531 4.092449
-00000a30: 342c 3232 2e39 3731 3533 3120 4320 3130  4,22.971531 C 10
-00000a40: 2e31 3438 3037 392c 3232 2e39 3731 3533  .148079,22.97153
-00000a50: 3120 3135 2e30 3632 3738 392c 3138 2e30  1 15.062789,18.0
-00000a60: 3536 3832 3120 3135 2e30 3632 3738 392c  56821 15.062789,
-00000a70: 3132 2e30 3031 3139 3120 4320 3135 2e30  12.001191 C 15.0
-00000a80: 3632 3738 392c 352e 3934 3535 3630 3920  62789,5.9455609 
-00000a90: 3130 2e31 3438 3037 392c 312e 3033 3038  10.148079,1.0308
-00000aa0: 3530 3920 342e 3039 3234 3439 342c 312e  509 4.0924494,1.
-00000ab0: 3033 3038 3530 3920 4320 332e 3935 3035  0308509 C 3.9505
-00000ac0: 3139 342c 312e 3033 3038 3530 3920 332e  194,1.0308509 3.
-00000ad0: 3830 3435 3439 342c 312e 3032 3534 3930  8045494,1.025490
-00000ae0: 3920 332e 3636 3339 3139 342c 312e 3033  9 3.6639194,1.03
-00000af0: 3038 3530 3920 7a20 2720 7374 796c 653d  08509 z ' style=
-00000b00: 2773 7472 6f6b 653a 2470 6c61 6e65 7473  'stroke:$planets
-00000b10: 5f63 6f6c 6f72 5f31 3b73 7472 6f6b 652d  _color_1;stroke-
-00000b20: 7769 6474 683a 3270 783b 2066 696c 6c3a  width:2px; fill:
-00000b30: 6e6f 6e65 3b27 202f 3e3c 2f67 3e3c 2f67  none;' /></g></g
-00000b40: 3e3c 2f73 796d 626f 6c3e 3c73 796d 626f  ></symbol><symbo
-00000b50: 6c20 6964 3d27 4d65 7263 7572 7927 3e3c  l id='Mercury'><
-00000b60: 6720 7472 616e 7366 6f72 6d3d 2774 7261  g transform='tra
-00000b70: 6e73 6c61 7465 2833 2c31 2927 3e3c 7061  nslate(3,1)'><pa
-00000b80: 7468 2064 3d27 4d20 3132 2e34 3137 3930  th d='M 12.41790
-00000b90: 382c 3131 2e30 3937 3530 3720 4320 3132  8,11.097507 C 12
-00000ba0: 2e34 3630 3831 382c 3133 2e36 3034 3931  .460818,13.60491
-00000bb0: 3620 3130 2e36 3638 3231 372c 3135 2e39  6 10.668217,15.9
-00000bc0: 3936 3635 3620 382e 3235 3636 3830 352c  96656 8.2566805,
-00000bd0: 3136 2e36 3736 3633 3920 4320 362e 3131  16.676639 C 6.11
-00000be0: 3830 3337 352c 3137 2e33 3232 3532 3220  80375,17.322522 
-00000bf0: 332e 3634 3038 3637 352c 3136 2e36 3131  3.6408675,16.611
-00000c00: 3836 3920 322e 3139 3930 3931 352c 3134  869 2.1990915,14
-00000c10: 2e38 3937 3032 3520 4320 302e 3730 3235  .897025 C 0.7025
-00000c20: 3133 3531 2c31 332e 3138 3538 3934 2030  1351,13.185894 0
-00000c30: 2e33 3437 3035 3535 312c 3130 2e35 3734  .34705551,10.574
-00000c40: 3134 3920 312e 3337 3837 3833 352c 382e  149 1.3787835,8.
-00000c50: 3534 3036 3337 2043 2032 2e33 3330 3930  540637 C 2.33090
-00000c60: 3635 2c36 2e35 3737 3831 3936 2034 2e34  65,6.5778196 4.4
-00000c70: 3434 3839 3235 2c35 2e32 3339 3035 3135  448925,5.2390515
-00000c80: 2036 2e36 3334 3433 3835 2c35 2e32 3830   6.6344385,5.280
-00000c90: 3138 3132 2043 2038 2e37 3433 3634 3835  1812 C 8.7436485
-00000ca0: 2c35 2e32 3830 3831 3834 2031 302e 3739  ,5.2808184 10.79
-00000cb0: 3732 312c 362e 3531 3834 3839 3720 3131  721,6.5184897 11
-00000cc0: 2e37 3535 3634 312c 382e 3430 3134 3232  .755641,8.401422
-00000cd0: 3920 4320 3132 2e31 3838 3730 392c 392e  9 C 12.188709,9.
-00000ce0: 3232 3933 3536 3320 3132 2e34 3231 3932  2293563 12.42192
-00000cf0: 362c 3130 2e31 3632 3536 3820 3132 2e34  6,10.162568 12.4
-00000d00: 3137 3930 382c 3131 2e30 3937 3530 3720  17908,11.097507 
-00000d10: 7a20 4d20 3131 2e35 3337 3534 392c 302e  z M 11.537549,0.
-00000d20: 3739 3437 3737 3536 2043 2031 312e 3336  79477756 C 11.36
-00000d30: 3830 3131 2c32 2e39 3533 3136 3336 2039  8011,2.9531636 9
-00000d40: 2e35 3932 3831 3035 2c34 2e38 3439 3339  .5928105,4.84939
-00000d50: 3420 372e 3435 3238 3435 352c 352e 3137  4 7.4528455,5.17
-00000d60: 3131 3237 2043 2035 2e34 3933 3430 3335  1127 C 5.4934035
-00000d70: 2c35 2e35 3035 3834 3637 2033 2e33 3633  ,5.5058467 3.363
-00000d80: 3435 3035 2c34 2e35 3439 3436 3836 2032  4505,4.5494686 2
-00000d90: 2e33 3935 3831 3335 2c32 2e37 3934 3635  .3958135,2.79465
-00000da0: 3836 2043 2032 2e30 3434 3831 3535 2c32  86 C 2.0448155,2
-00000db0: 2e31 3831 3837 3436 2031 2e38 3237 3537  .1818746 1.82757
-00000dc0: 3535 2c31 2e34 3933 3039 3636 2031 2e37  55,1.4930966 1.7
-00000dd0: 3632 3638 3435 2c30 2e37 3839 3933 3735  626845,0.7899375
-00000de0: 3620 4d20 362e 3630 3339 3632 352c 3136  6 M 6.6039625,16
-00000df0: 2e38 3930 3531 3820 4320 362e 3630 3339  .890518 C 6.6039
-00000e00: 3632 352c 3138 2e39 3937 3033 3120 362e  625,18.997031 6.
-00000e10: 3630 3339 3632 352c 3231 2e31 3033 3534  6039625,21.10354
-00000e20: 3520 362e 3630 3339 3632 352c 3233 2e32  5 6.6039625,23.2
-00000e30: 3130 3035 3820 4d20 332e 3937 3038 3231  10058 M 3.970821
-00000e40: 352c 3230 2e35 3736 3931 3620 4320 352e  5,20.576916 C 5.
-00000e50: 3732 3632 3437 352c 3230 2e35 3736 3931  7262475,20.57691
-00000e60: 3620 372e 3438 3136 3738 352c 3230 2e35  6 7.4816785,20.5
-00000e70: 3736 3931 3620 392e 3233 3731 3034 352c  76916 9.2371045,
-00000e80: 3230 2e35 3736 3931 3627 2073 7479 6c65  20.576916' style
-00000e90: 3d27 7374 726f 6b65 3a24 706c 616e 6574  ='stroke:$planet
-00000ea0: 735f 636f 6c6f 725f 323b 7374 726f 6b65  s_color_2;stroke
-00000eb0: 2d77 6964 7468 3a32 7078 3b20 6669 6c6c  -width:2px; fill
-00000ec0: 3a6e 6f6e 653b 2720 2f3e 3c2f 673e 3c2f  :none;' /></g></
-00000ed0: 7379 6d62 6f6c 3e3c 7379 6d62 6f6c 2069  symbol><symbol i
-00000ee0: 643d 2756 656e 7573 273e 3c67 2074 7261  d='Venus'><g tra
-00000ef0: 6e73 666f 726d 3d27 7472 616e 736c 6174  nsform='translat
-00000f00: 6528 302c 3229 273e 3c67 2074 7261 6e73  e(0,2)'><g trans
-00000f10: 666f 726d 3d27 7363 616c 6528 2e39 2927  form='scale(.9)'
-00000f20: 3e3c 7061 7468 2064 3d27 4d20 3138 2e34  ><path d='M 18.4
-00000f30: 3030 3730 332c 372e 3336 3637 3438 3320  00703,7.3667483 
-00000f40: 4320 3138 2e34 3233 3936 2c39 2e36 3635  C 18.42396,9.665
-00000f50: 3533 3239 2031 372e 3137 3031 3032 2c31  5329 17.170102,1
-00000f60: 312e 3931 3435 3739 2031 352e 3231 3839  1.914579 15.2189
-00000f70: 3732 2c31 332e 3131 3337 3238 2043 2031  72,13.113728 C 1
-00000f80: 332e 3136 3234 3539 2c31 342e 3432 3732  3.162459,14.4272
-00000f90: 3533 2031 302e 3338 3938 3535 2c31 342e  53 10.389855,14.
-00000fa0: 3437 3637 3732 2038 2e32 3837 3136 3633  476772 8.2871663
-00000fb0: 2c31 332e 3233 3937 3039 2043 2036 2e32  ,13.239709 C 6.2
-00000fc0: 3733 3538 3531 2c31 322e 3130 3035 3234  735851,12.100524
-00000fd0: 2034 2e39 3333 3633 332c 392e 3836 3430   4.933633,9.8640
-00000fe0: 3332 3320 342e 3839 3739 3931 352c 372e  323 4.8979915,7.
-00000ff0: 3534 3134 3830 3420 4320 342e 3831 3733  5414804 C 4.8173
-00001000: 3631 372c 352e 3236 3738 3539 3220 352e  617,5.2678592 5.
-00001010: 3938 3535 3139 362c 332e 3030 3930 3030  9855196,3.009000
-00001020: 3120 372e 3837 3238 3830 372c 312e 3735  1 7.8728807,1.75
-00001030: 3330 3437 3120 4320 392e 3838 3033 3931  30471 C 9.880391
-00001040: 352c 302e 3336 3530 3935 3436 2031 322e  5,0.36509546 12.
-00001050: 3634 3839 3036 2c30 2e32 3136 3537 3134  648906,0.2165714
-00001060: 3620 3134 2e37 3934 3834 392c 312e 3337  6 14.794849,1.37
-00001070: 3532 3833 3120 4320 3136 2e38 3639 3737  52831 C 16.86977
-00001080: 322c 322e 3435 3134 3633 3320 3138 2e32  2,2.4514633 18.2
-00001090: 3936 3234 312c 342e 3637 3331 3435 3320  96241,4.6731453 
-000010a0: 3138 2e33 3931 3931 382c 372e 3031 3833  18.391918,7.0183
-000010b0: 3732 3320 4320 3138 2e33 3937 3738 312c  723 C 18.397781,
-000010c0: 372e 3133 3433 3936 3320 3138 2e34 3030  7.1343963 18.400
-000010d0: 3730 332c 372e 3235 3035 3732 3320 3138  703,7.2505723 18
-000010e0: 2e34 3030 3730 332c 372e 3336 3637 3438  .400703,7.366748
-000010f0: 3320 7a20 4d20 3131 2e36 3438 3238 392c  3 z M 11.648289,
-00001100: 3134 2e31 3336 3638 3920 4320 3131 2e36  14.136689 C 11.6
-00001110: 3438 3238 392c 3137 2e30 3038 3736 3420  48289,17.008764 
-00001120: 3131 2e36 3438 3238 392c 3139 2e38 3830  11.648289,19.880
-00001130: 3834 2031 312e 3634 3832 3839 2c32 322e  84 11.648289,22.
-00001140: 3735 3239 3135 204d 2037 2e39 3635 3133  752915 M 7.96513
-00001150: 3333 2c31 392e 3036 3032 3433 2043 2031  33,19.060243 C 1
-00001160: 302e 3432 3035 372c 3139 2e30 3630 3234  0.42057,19.06024
-00001170: 3320 3132 2e38 3736 3030 382c 3139 2e30  3 12.876008,19.0
-00001180: 3630 3234 3320 3135 2e33 3331 3434 342c  60243 15.331444,
-00001190: 3139 2e30 3630 3234 3327 2073 7479 6c65  19.060243' style
-000011a0: 3d27 7374 726f 6b65 3a24 706c 616e 6574  ='stroke:$planet
-000011b0: 735f 636f 6c6f 725f 333b 7374 726f 6b65  s_color_3;stroke
-000011c0: 2d77 6964 7468 3a32 7078 3b20 6669 6c6c  -width:2px; fill
-000011d0: 3a6e 6f6e 653b 2720 2f3e 3c2f 673e 3c2f  :none;' /></g></
-000011e0: 673e 3c2f 7379 6d62 6f6c 3e3c 7379 6d62  g></symbol><symb
-000011f0: 6f6c 2069 643d 274d 6172 7327 3e3c 6720  ol id='Mars'><g 
-00001200: 7472 616e 7366 6f72 6d3d 2774 7261 6e73  transform='trans
-00001210: 6c61 7465 2831 2c33 2927 3e3c 6720 7472  late(1,3)'><g tr
-00001220: 616e 7366 6f72 6d3d 2773 6361 6c65 282e  ansform='scale(.
-00001230: 3929 273e 3c70 6174 6820 643d 274d 2031  9)'><path d='M 1
-00001240: 392e 3833 3638 3238 2c31 2e32 3236 3835  9.836828,1.22685
-00001250: 3835 2043 2031 372e 3432 3434 3232 2c33  85 C 17.424422,3
-00001260: 2e36 3235 3837 3736 2031 352e 3031 3230  .6258776 15.0120
-00001270: 3038 2c36 2e30 3234 3930 3437 2031 322e  08,6.0249047 12.
-00001280: 3539 3935 3934 2c38 2e34 3233 3933 3137  599594,8.4239317
-00001290: 204d 2031 332e 3538 3631 3331 2c31 2e33   M 13.586131,1.3
-000012a0: 3033 3238 3533 2043 2031 352e 3634 3136  032853 C 15.6416
-000012b0: 3232 2c31 2e33 3033 3238 3533 2031 372e  22,1.3032853 17.
-000012c0: 3639 3731 3035 2c31 2e33 3033 3238 3533  697105,1.3032853
-000012d0: 2031 392e 3735 3235 3935 2c31 2e33 3033   19.752595,1.303
-000012e0: 3238 3533 2043 2031 392e 3735 3235 3935  2853 C 19.752595
-000012f0: 2c33 2e33 3437 3336 3836 2031 392e 3735  ,3.3473686 19.75
-00001300: 3236 3033 2c35 2e33 3931 3435 3137 2031  2603,5.3914517 1
-00001310: 392e 3735 3236 3033 2c37 2e34 3335 3533  9.752603,7.43553
-00001320: 3537 2720 7374 796c 653d 2773 7472 6f6b  57' style='strok
-00001330: 653a 2470 6c61 6e65 7473 5f63 6f6c 6f72  e:$planets_color
-00001340: 5f34 3b73 7472 6f6b 652d 7769 6474 683a  _4;stroke-width:
-00001350: 3270 783b 2066 696c 6c3a 6e6f 6e65 3b27  2px; fill:none;'
-00001360: 202f 3e3c 7061 7468 2064 3d27 4d20 3135   /><path d='M 15
-00001370: 2e32 3038 3833 352c 3133 2e31 3337 3731  .208835,13.13771
-00001380: 3120 4320 3135 2e32 3435 3738 372c 3135  1 C 15.245787,15
-00001390: 2e38 3838 3330 3920 3133 2e34 3937 3532  .888309 13.49752
-000013a0: 332c 3138 2e35 3433 3436 2031 302e 3936  3,18.54346 10.96
-000013b0: 3930 3433 2c31 392e 3631 3737 3320 4320  9043,19.61773 C 
-000013c0: 382e 3435 3834 3137 352c 3230 2e37 3439  8.4584175,20.749
-000013d0: 3033 3620 352e 3331 3535 3432 382c 3230  036 5.3155428,20
-000013e0: 2e32 3136 3431 2033 2e33 3233 3633 3036  .21641 3.3236306
-000013f0: 2c31 382e 3331 3238 3433 2043 2031 2e33  ,18.312843 C 1.3
-00001400: 3239 3437 3839 2c31 362e 3530 3236 3836  294789,16.502686
-00001410: 2030 2e35 3534 3636 3132 372c 3133 2e35   0.55466127,13.5
-00001420: 3034 3637 3820 312e 3431 3333 3631 352c  04678 1.4133615,
-00001430: 3130 2e39 3533 3330 3220 4320 322e 3234  10.953302 C 2.24
-00001440: 3835 3732 312c 382e 3238 3333 3435 3220  85721,8.2833452 
-00001450: 342e 3830 3035 3034 332c 362e 3236 3630  4.8005043,6.2660
-00001460: 3037 3520 372e 3539 3532 3138 2c36 2e30  075 7.595218,6.0
-00001470: 3838 3432 3636 2043 2031 302e 3238 3730  884266 C 10.2870
-00001480: 3332 2c35 2e38 3436 3739 3834 2031 332e  32,5.8467984 13.
-00001490: 3032 3233 3438 2c37 2e33 3233 3130 3438  022348,7.3231048
-000014a0: 2031 342e 3331 3338 362c 392e 3639 3338   14.31386,9.6938
-000014b0: 3038 3120 4320 3134 2e39 3031 3136 332c  081 C 14.901163,
-000014c0: 3130 2e37 3339 3936 3720 3135 2e32 3131  10.739967 15.211
-000014d0: 3038 322c 3131 2e39 3338 3139 3620 3135  082,11.938196 15
-000014e0: 2e32 3038 3833 352c 3133 2e31 3337 3731  .208835,13.13771
-000014f0: 3120 7a27 2073 7479 6c65 3d27 7374 726f  1 z' style='stro
-00001500: 6b65 3a24 706c 616e 6574 735f 636f 6c6f  ke:$planets_colo
-00001510: 725f 343b 7374 726f 6b65 2d77 6964 7468  r_4;stroke-width
-00001520: 3a32 7078 3b20 6669 6c6c 3a6e 6f6e 653b  :2px; fill:none;
-00001530: 2720 2f3e 3c2f 673e 3c2f 673e 3c2f 7379  ' /></g></g></sy
-00001540: 6d62 6f6c 3e3c 7379 6d62 6f6c 2069 643d  mbol><symbol id=
-00001550: 274a 7570 6974 6572 273e 3c67 2074 7261  'Jupiter'><g tra
-00001560: 6e73 666f 726d 3d27 7472 616e 736c 6174  nsform='translat
-00001570: 6528 312c 3329 273e 3c67 2074 7261 6e73  e(1,3)'><g trans
-00001580: 666f 726d 3d27 7363 616c 6528 2e39 2927  form='scale(.9)'
-00001590: 3e3c 7061 7468 2064 3d27 4d20 3136 2e39  ><path d='M 16.9
-000015a0: 3033 3030 382c 302e 3939 3834 3931 3537  03008,0.99849157
-000015b0: 204c 2031 362e 3930 3330 3038 2c32 332e   L 16.903008,23.
-000015c0: 3030 3135 3132 204d 2032 302e 3533 3032  001512 M 20.5302
-000015d0: 3738 2c31 372e 3335 3937 3132 204c 2032  78,17.359712 L 2
-000015e0: 2e39 3938 3438 3834 2c31 372e 3335 3937  .9984884,17.3597
-000015f0: 3132 204d 2034 2e38 3132 3131 3834 2c38  12 M 4.8121184,8
-00001600: 2e38 3937 3031 3220 4320 342e 3230 3735  .897012 C 4.2075
-00001610: 3738 342c 382e 3839 3730 3132 2032 2e39  784,8.897012 2.9
-00001620: 3938 3438 3834 2c38 2e33 3332 3833 3220  984884,8.332832 
-00001630: 322e 3939 3834 3838 342c 362e 3037 3631  2.9984884,6.0761
-00001640: 3132 2043 2032 2e39 3938 3438 3834 2c33  12 C 2.9984884,3
-00001650: 2e38 3139 3338 3220 352e 3431 3636 3638  .819382 5.416668
-00001660: 342c 312e 3536 3236 3731 3620 372e 3833  4,1.5626716 7.83
-00001670: 3438 3438 342c 312e 3536 3236 3731 3620  48484,1.5626716 
-00001680: 4320 3130 2e32 3533 3032 382c 312e 3536  C 10.253028,1.56
-00001690: 3236 3731 3620 3132 2e36 3731 3139 382c  26716 12.671198,
-000016a0: 332e 3235 3532 3132 2031 322e 3637 3131  3.255212 12.6711
-000016b0: 3938 2c37 2e32 3034 3437 3220 4320 3132  98,7.204472 C 12
-000016c0: 2e36 3731 3139 382c 3131 2e31 3533 3733  .671198,11.15373
-000016d0: 3220 392e 3634 3834 3738 342c 3137 2e33  2 9.6484784,17.3
-000016e0: 3539 3731 3220 332e 3630 3330 3238 342c  59712 3.6030284,
-000016f0: 3137 2e33 3539 3731 3227 2073 7479 6c65  17.359712' style
-00001700: 3d27 7374 726f 6b65 3a24 706c 616e 6574  ='stroke:$planet
-00001710: 735f 636f 6c6f 725f 353b 7374 726f 6b65  s_color_5;stroke
-00001720: 2d77 6964 7468 3a32 7078 3b20 6669 6c6c  -width:2px; fill
-00001730: 3a6e 6f6e 653b 2720 2f3e 3c2f 673e 3c2f  :none;' /></g></
-00001740: 673e 3c2f 7379 6d62 6f6c 3e3c 7379 6d62  g></symbol><symb
-00001750: 6f6c 2069 643d 2753 6174 7572 6e27 3e3c  ol id='Saturn'><
-00001760: 6720 7472 616e 7366 6f72 6d3d 2774 7261  g transform='tra
-00001770: 6e73 6c61 7465 2831 2c32 2927 3e3c 7061  nslate(1,2)'><pa
-00001780: 7468 2064 3d27 4d20 382e 3338 3434 3334  th d='M 8.384434
-00001790: 392c 302e 3930 3230 3332 3331 204c 2038  9,0.90203231 L 8
-000017a0: 2e33 3834 3433 3439 2c31 382e 3239 3838  .3844349,18.2988
-000017b0: 3532 204d 2035 2e34 3334 3934 3439 2c33  52 M 5.4349449,3
-000017c0: 2e37 3531 3531 3233 204c 2031 322e 3636  .7515123 L 12.66
-000017d0: 3837 3435 2c33 2e37 3531 3531 3233 204d  8745,3.7515123 M
-000017e0: 2031 362e 3832 3338 3735 2c32 312e 3839   16.823875,21.89
-000017f0: 3831 3932 2043 2031 362e 3232 3130 3535  8192 C 16.221055
-00001800: 2c32 322e 3439 3830 3832 2031 352e 3631  ,22.498082 15.61
-00001810: 3832 3335 2c32 332e 3039 3739 3732 2031  8235,23.097972 1
-00001820: 352e 3031 3534 3135 2c32 332e 3039 3739  5.015415,23.0979
-00001830: 3732 2043 2031 342e 3431 3236 3035 2c32  72 C 14.412605,2
-00001840: 332e 3039 3739 3732 2031 332e 3230 3639  3.097972 13.2069
-00001850: 3735 2c32 322e 3439 3830 3832 2031 332e  75,22.498082 13.
-00001860: 3230 3639 3735 2c32 312e 3239 3833 3032  206975,21.298302
-00001870: 2043 2031 332e 3230 3639 3735 2c32 302e   C 13.206975,20.
-00001880: 3039 3835 3232 2031 332e 3830 3937 3835  098522 13.809785
-00001890: 2c31 382e 3839 3837 3432 2031 352e 3031  ,18.898742 15.01
-000018a0: 3534 3135 2c31 372e 3639 3839 3632 2043  5415,17.698962 C
-000018b0: 2031 362e 3232 3130 3535 2c31 362e 3439   16.221055,16.49
-000018c0: 3931 3832 2031 372e 3432 3636 3835 2c31  9182 17.426685,1
-000018d0: 342e 3039 3936 3232 2031 372e 3432 3636  4.099622 17.4266
-000018e0: 3835 2c31 312e 3730 3030 3532 2043 2031  85,11.700052 C 1
-000018f0: 372e 3432 3636 3835 2c39 2e33 3030 3439  7.426685,9.30049
-00001900: 3233 2031 362e 3232 3130 3535 2c36 2e39  23 16.221055,6.9
-00001910: 3030 3933 3233 2031 332e 3830 3937 3835  009323 13.809785
-00001920: 2c36 2e39 3030 3933 3233 2043 2031 312e  ,6.9009323 C 11.
-00001930: 3532 3932 3135 2c36 2e39 3030 3933 3233  529215,6.9009323
-00001940: 2039 2e35 3930 3036 3439 2c38 2e31 3030   9.5900649,8.100
-00001950: 3731 3233 2038 2e33 3834 3433 3439 2c31  7123 8.3844349,1
-00001960: 302e 3530 3032 3832 2720 7374 796c 653d  0.500282' style=
-00001970: 2773 7472 6f6b 653a 2470 6c61 6e65 7473  'stroke:$planets
-00001980: 5f63 6f6c 6f72 5f36 3b73 7472 6f6b 652d  _color_6;stroke-
-00001990: 7769 6474 683a 3270 783b 2066 696c 6c3a  width:2px; fill:
-000019a0: 6e6f 6e65 3b27 202f 3e3c 2f67 3e3c 2f73  none;' /></g></s
-000019b0: 796d 626f 6c3e 3c73 796d 626f 6c20 6964  ymbol><symbol id
-000019c0: 3d27 5572 616e 7573 273e 3c67 2074 7261  ='Uranus'><g tra
-000019d0: 6e73 666f 726d 3d27 7472 616e 736c 6174  nsform='translat
-000019e0: 6528 322c 3429 273e 3c67 2074 7261 6e73  e(2,4)'><g trans
-000019f0: 666f 726d 3d27 7363 616c 6528 2e38 2927  form='scale(.8)'
-00001a00: 3e3c 7061 7468 2064 3d27 4d20 342e 3637  ><path d='M 4.67
-00001a10: 3732 3036 362c 3136 2e30 3937 3432 3320  72066,16.097423 
-00001a20: 4320 332e 3230 3432 3432 362c 3136 2e30  C 3.2042426,16.0
-00001a30: 3937 3432 3320 312e 3733 3132 3737 362c  97423 1.7312776,
-00001a40: 3136 2e30 3937 3432 3320 302e 3235 3833  16.097423 0.2583
-00001a50: 3036 3631 2c31 362e 3039 3734 3233 2043  0661,16.097423 C
-00001a60: 2030 2e33 3231 3835 3036 312c 3135 2e38   0.32185061,15.8
-00001a70: 3934 3837 3920 302e 3131 3939 3536 3631  94879 0.11995661
-00001a80: 2c31 352e 3438 3530 3936 2030 2e33 3739  ,15.485096 0.379
-00001a90: 3736 3336 312c 3135 2e34 3335 3738 3720  76361,15.435787 
-00001aa0: 4320 312e 3138 3039 3732 362c 3135 2e32  C 1.1809726,15.2
-00001ab0: 3335 3438 3520 312e 3938 3231 3832 362c  35485 1.9821826,
-00001ac0: 3135 2e30 3335 3138 3220 322e 3738 3333  15.035182 2.7833
-00001ad0: 3932 362c 3134 2e38 3334 3838 2043 2032  926,14.83488 C 2
-00001ae0: 2e37 3833 3339 3236 2c31 302e 3632 3634  .7833926,10.6264
-00001af0: 3031 2032 2e37 3833 3339 3236 2c36 2e34  01 2.7833926,6.4
-00001b00: 3137 3932 3920 322e 3738 3333 3932 362c  17929 2.7833926,
-00001b10: 322e 3230 3934 3530 3220 4320 312e 3934  2.2094502 C 1.94
-00001b20: 3136 3939 362c 312e 3939 3930 3238 3520  16996,1.9990285 
-00001b30: 312e 3130 3030 3035 362c 312e 3738 3836  1.1000056,1.7886
-00001b40: 3030 3420 302e 3235 3833 3036 3631 2c31  004 0.25830661,1
-00001b50: 2e35 3738 3137 3837 2043 2030 2e33 3233  .5781787 C 0.323
-00001b60: 3830 3736 312c 312e 3339 3135 3234 3320  80761,1.3915243 
-00001b70: 302e 3131 3537 3032 3631 2c30 2e39 3331  0.11570261,0.931
-00001b80: 3236 3433 3220 302e 3338 3335 3030 3631  26432 0.38350061
-00001b90: 2c30 2e39 3436 3930 3732 3220 4320 312e  ,0.94690722 C 1.
-00001ba0: 3831 3437 3337 362c 302e 3934 3639 3037  8147376,0.946907
-00001bb0: 3232 2033 2e32 3435 3936 3936 2c30 2e39  22 3.2459696,0.9
-00001bc0: 3436 3930 3732 3220 342e 3637 3732 3036  4690722 4.677206
-00001bd0: 362c 302e 3934 3639 3037 3232 2043 2034  6,0.94690722 C 4
-00001be0: 2e36 3737 3230 3636 2c35 2e39 3937 3037  .6772066,5.99707
-00001bf0: 3932 2034 2e36 3737 3230 3636 2c31 312e  92 4.6772066,11.
-00001c00: 3034 3732 3531 2034 2e36 3737 3230 3636  047251 4.6772066
-00001c10: 2c31 362e 3039 3734 3233 207a 2027 2073  ,16.097423 z ' s
-00001c20: 7479 6c65 3d27 7374 726f 6b65 3a24 706c  tyle='stroke:$pl
-00001c30: 616e 6574 735f 636f 6c6f 725f 373b 7374  anets_color_7;st
-00001c40: 726f 6b65 2d77 6964 7468 3a31 7078 3b20  roke-width:1px; 
-00001c50: 6669 6c6c 3a24 706c 616e 6574 735f 636f  fill:$planets_co
-00001c60: 6c6f 725f 353b 2720 2f3e 3c70 6174 6820  lor_5;' /><path 
-00001c70: 643d 274d 2031 382e 3536 3531 382c 3136  d='M 18.56518,16
-00001c80: 2e30 3937 3432 3320 4320 3230 2e30 3338  .097423 C 20.038
-00001c90: 3135 312c 3136 2e30 3937 3432 3320 3231  151,16.097423 21
-00001ca0: 2e35 3131 3131 362c 3136 2e30 3937 3432  .511116,16.09742
-00001cb0: 3320 3232 2e39 3834 3038 312c 3136 2e30  3 22.984081,16.0
-00001cc0: 3937 3432 3320 4320 3232 2e39 3230 3534  97423 C 22.92054
-00001cd0: 332c 3135 2e38 3934 3837 3920 3233 2e31  3,15.894879 23.1
-00001ce0: 3232 3433 2c31 352e 3438 3530 3936 2032  2243,15.485096 2
-00001cf0: 322e 3836 3236 3331 2c31 352e 3433 3537  2.862631,15.4357
-00001d00: 3837 2043 2032 322e 3036 3134 3231 2c31  87 C 22.061421,1
-00001d10: 352e 3233 3534 3835 2032 312e 3236 3032  5.235485 21.2602
-00001d20: 3131 2c31 352e 3033 3531 3832 2032 302e  11,15.035182 20.
-00001d30: 3435 3839 3935 2c31 342e 3833 3438 3820  458995,14.83488 
-00001d40: 4320 3230 2e34 3538 3939 352c 3130 2e36  C 20.458995,10.6
-00001d50: 3236 3430 3120 3230 2e34 3538 3939 352c  26401 20.458995,
-00001d60: 362e 3431 3739 3239 2032 302e 3435 3839  6.417929 20.4589
-00001d70: 3935 2c32 2e32 3039 3435 3032 2043 2032  95,2.2094502 C 2
-00001d80: 312e 3330 3036 3934 2c31 2e39 3939 3032  1.300694,1.99902
-00001d90: 3835 2032 322e 3134 3233 3838 2c31 2e37  85 22.142388,1.7
-00001da0: 3838 3630 3034 2032 322e 3938 3430 3831  886004 22.984081
-00001db0: 2c31 2e35 3738 3137 3837 2043 2032 322e  ,1.5781787 C 22.
-00001dc0: 3931 3835 3837 2c31 2e33 3931 3532 3433  918587,1.3915243
-00001dd0: 2032 332e 3132 3636 3931 2c30 2e39 3331   23.126691,0.931
-00001de0: 3236 3433 3220 3232 2e38 3538 3839 332c  26432 22.858893,
-00001df0: 302e 3934 3639 3037 3232 2043 2032 312e  0.94690722 C 21.
-00001e00: 3432 3736 3536 2c30 2e39 3436 3930 3732  427656,0.9469072
-00001e10: 3220 3139 2e39 3936 3431 382c 302e 3934  2 19.996418,0.94
-00001e20: 3639 3037 3232 2031 382e 3536 3531 382c  690722 18.56518,
-00001e30: 302e 3934 3639 3037 3232 2043 2031 382e  0.94690722 C 18.
-00001e40: 3536 3531 382c 352e 3939 3730 3739 3220  56518,5.9970792 
-00001e50: 3138 2e35 3635 3138 2c31 312e 3034 3732  18.56518,11.0472
-00001e60: 3531 2031 382e 3536 3531 382c 3136 2e30  51 18.56518,16.0
-00001e70: 3937 3432 3320 7a20 2720 7374 796c 653d  97423 z ' style=
-00001e80: 2773 7472 6f6b 653a 2470 6c61 6e65 7473  'stroke:$planets
-00001e90: 5f63 6f6c 6f72 5f37 3b73 7472 6f6b 652d  _color_7;stroke-
-00001ea0: 7769 6474 683a 3170 783b 2066 696c 6c3a  width:1px; fill:
-00001eb0: 2470 6c61 6e65 7473 5f63 6f6c 6f72 5f35  $planets_color_5
-00001ec0: 3b27 202f 3e3c 7061 7468 2064 3d27 4d20  ;' /><path d='M 
-00001ed0: 342e 3034 3539 3335 362c 382e 3532 3231  4.0459356,8.5221
-00001ee0: 3635 3220 4320 392e 3039 3631 3037 362c  652 C 9.0961076,
-00001ef0: 382e 3532 3231 3635 3220 3134 2e31 3436  8.5221652 14.146
-00001f00: 3238 2c38 2e35 3232 3136 3532 2031 392e  28,8.5221652 19.
-00001f10: 3139 3634 3532 2c38 2e35 3232 3136 3532  196452,8.5221652
-00001f20: 204d 2031 312e 3632 3131 3934 2c30 2e39   M 11.621194,0.9
-00001f30: 3436 3930 3732 3220 4320 3131 2e36 3231  4690722 C 11.621
-00001f40: 3139 342c 362e 3431 3739 3239 2031 312e  194,6.417929 11.
-00001f50: 3632 3131 3934 2c31 312e 3838 3839 3434  621194,11.888944
-00001f60: 2031 312e 3632 3131 3934 2c31 372e 3335   11.621194,17.35
-00001f70: 3939 3636 204d 2031 342e 3134 3632 3432  9966 M 14.146242
-00001f80: 2c32 302e 3531 3633 3432 2043 2031 342e  ,20.516342 C 14.
-00001f90: 3232 3739 3534 2c32 322e 3230 3131 3035  227954,22.201105
-00001fa0: 2031 322e 3237 3536 3635 2c32 332e 3535   12.275665,23.55
-00001fb0: 3033 3032 2031 302e 3732 3536 3738 2c32  0302 10.725678,2
-00001fc0: 322e 3838 3330 3233 2043 2039 2e31 3339  2.883023 C 9.139
-00001fd0: 3537 3636 2c32 322e 3334 3836 3936 2038  5766,22.348696 8
-00001fe0: 2e35 3532 3034 3636 2c32 302e 3038 3936  .5520466,20.0896
-00001ff0: 3835 2039 2e37 3033 3439 3736 2c31 382e  85 9.7034976,18.
-00002000: 3836 3038 3731 2043 2031 302e 3732 3430  860871 C 10.7240
-00002010: 3735 2c31 372e 3630 3831 3832 2031 322e  75,17.608182 12.
-00002020: 3935 3934 3634 2c31 372e 3734 3634 3831  959464,17.746481
-00002030: 2031 332e 3736 3037 3331 2c31 392e 3137   13.760731,19.17
-00002040: 3438 3038 2043 2031 342e 3031 3133 3339  4808 C 14.011339
-00002050: 2c31 392e 3537 3431 2031 342e 3134 3831  ,19.5741 14.1481
-00002060: 382c 3230 2e30 3434 3634 3420 3134 2e31  8,20.044644 14.1
-00002070: 3436 3234 322c 3230 2e35 3136 3334 3220  46242,20.516342 
-00002080: 7a20 2720 7374 796c 653d 2773 7472 6f6b  z ' style='strok
-00002090: 653a 2470 6c61 6e65 7473 5f63 6f6c 6f72  e:$planets_color
-000020a0: 5f37 3b73 7472 6f6b 652d 7769 6474 683a  _7;stroke-width:
-000020b0: 3270 783b 2066 696c 6c3a 6e6f 6e65 3b27  2px; fill:none;'
-000020c0: 202f 3e3c 2f67 3e3c 2f67 3e3c 2f73 796d   /></g></g></sym
-000020d0: 626f 6c3e 3c73 796d 626f 6c20 6964 3d27  bol><symbol id='
-000020e0: 4e65 7074 756e 6527 3e3c 6720 7472 616e  Neptune'><g tran
-000020f0: 7366 6f72 6d3d 2774 7261 6e73 6c61 7465  sform='translate
-00002100: 2832 2c34 2927 3e3c 6720 7472 616e 7366  (2,4)'><g transf
-00002110: 6f72 6d3d 2773 6361 6c65 282e 3929 273e  orm='scale(.9)'>
-00002120: 3c70 6174 6820 643d 274d 2033 2e38 3836  <path d='M 3.886
-00002130: 3330 372c 322e 3230 3938 3133 3420 4320  307,2.2098134 C 
-00002140: 322e 3237 3238 3234 392c 3133 2e31 3732  2.2728249,13.172
-00002150: 3333 3620 342e 3936 3139 3731 382c 3134  336 4.9619718,14
-00002160: 2e38 3136 3731 3820 3130 2e33 3430 3236  .816718 10.34026
-00002170: 352c 3134 2e38 3136 3731 3820 4320 3135  5,14.816718 C 15
-00002180: 2e37 3138 3536 372c 3134 2e38 3136 3731  .718567,14.81671
-00002190: 3820 3138 2e34 3037 3732 312c 3133 2e31  8 18.407721,13.1
-000021a0: 3732 3333 3620 3136 2e37 3934 3233 312c  72336 16.794231,
-000021b0: 322e 3230 3938 3133 3420 4d20 3130 2e33  2.2098134 M 10.3
-000021c0: 3430 3236 352c 332e 3330 3630 3635 3820  40265,3.3060658 
-000021d0: 4c20 3130 2e33 3430 3236 352c 3233 2e35  L 10.340265,23.5
-000021e0: 3836 3733 3620 4d20 362e 3033 3736 3239  86736 M 6.037629
-000021f0: 2c31 392e 3230 3137 3237 204c 2031 342e  ,19.201727 L 14.
-00002200: 3634 3239 3039 2c31 392e 3230 3137 3237  642909,19.201727
-00002210: 204d 2030 2e39 3131 3830 3032 372c 332e   M 0.91180027,3.
-00002220: 3732 3330 3830 3820 4c20 332e 3936 3335  7230808 L 3.9635
-00002230: 3739 352c 312e 3431 3033 3336 3120 4c20  795,1.4103361 L 
-00002240: 362e 3233 3238 3638 392c 342e 3532 3035  6.2328689,4.5205
-00002250: 3437 3820 4d20 372e 3539 3938 3438 362c  478 M 7.5998486,
-00002260: 362e 3334 3231 3234 3820 4c20 3130 2e32  6.3421248 L 10.2
-00002270: 3539 3035 352c 332e 3537 3133 3130 3820  59055,3.5713108 
-00002280: 4c20 3132 2e39 3737 3831 322c 362e 3238  L 12.977812,6.28
-00002290: 3134 3432 3820 4d20 3134 2e34 3037 3838  14428 M 14.40788
-000022a0: 392c 342e 3731 3230 3532 3820 4c20 3136  9,4.7120528 L 16
-000022b0: 2e37 3135 3934 362c 312e 3633 3136 3038  .715946,1.631608
-000022c0: 3520 4c20 3139 2e37 3338 3530 362c 332e  5 L 19.738506,3.
-000022d0: 3938 3338 3632 3827 2073 7479 6c65 3d27  9838628' style='
-000022e0: 7374 726f 6b65 3a24 706c 616e 6574 735f  stroke:$planets_
-000022f0: 636f 6c6f 725f 383b 7374 726f 6b65 2d77  color_8;stroke-w
-00002300: 6964 7468 3a32 7078 3b20 6669 6c6c 3a6e  idth:2px; fill:n
-00002310: 6f6e 653b 2720 2f3e 3c2f 673e 3c2f 673e  one;' /></g></g>
-00002320: 3c2f 7379 6d62 6f6c 3e3c 7379 6d62 6f6c  </symbol><symbol
-00002330: 2069 643d 2750 6c75 746f 273e 3c67 2074   id='Pluto'><g t
-00002340: 7261 6e73 666f 726d 3d27 7472 616e 736c  ransform='transl
-00002350: 6174 6528 302c 3329 273e 3c67 2074 7261  ate(0,3)'><g tra
-00002360: 6e73 666f 726d 3d27 7363 616c 6528 2e39  nsform='scale(.9
-00002370: 2927 3e3c 7061 7468 2064 3d27 4d20 372e  )'><path d='M 7.
-00002380: 3239 3838 3338 392c 3138 2e31 3639 3637  2988389,18.16967
-00002390: 3120 4c20 3137 2e31 3730 3239 392c 3138  1 L 17.170299,18
-000023a0: 2e31 3639 3637 3120 4d20 3132 2e32 3334  .169671 M 12.234
-000023b0: 3536 392c 3233 2e31 3035 3430 3120 4c20  569,23.105401 L 
-000023c0: 3132 2e32 3334 3536 392c 3132 2e36 3136  12.234569,12.616
-000023d0: 3938 3120 4d20 3136 2e35 3533 3330 392c  981 M 16.553309,
-000023e0: 352e 3231 3333 3630 3920 4320 3136 2e35  5.2133609 C 16.5
-000023f0: 3533 3330 392c 372e 3539 3733 3230 3920  53309,7.5973209 
-00002400: 3134 2e36 3138 3439 392c 392e 3533 3231  14.618499,9.5321
-00002410: 3330 3920 3132 2e32 3334 3533 392c 392e  309 12.234539,9.
-00002420: 3533 3231 3330 3920 4320 392e 3835 3035  5321309 C 9.8505
-00002430: 3838 392c 392e 3533 3231 3330 3920 372e  889,9.5321309 7.
-00002440: 3931 3537 3738 392c 372e 3539 3733 3230  9157789,7.597320
-00002450: 3920 372e 3931 3537 3738 392c 352e 3231  9 7.9157789,5.21
-00002460: 3333 3630 3920 4320 372e 3931 3537 3738  33609 C 7.915778
-00002470: 392c 322e 3832 3934 3130 3920 392e 3835  9,2.8294109 9.85
-00002480: 3035 3838 392c 302e 3839 3436 3030 3837  05889,0.89460087
-00002490: 2031 322e 3233 3435 3339 2c30 2e38 3934   12.234539,0.894
-000024a0: 3630 3038 3720 4320 3134 2e36 3138 3439  60087 C 14.61849
-000024b0: 392c 302e 3839 3436 3030 3837 2031 362e  9,0.89460087 16.
-000024c0: 3535 3333 3039 2c32 2e38 3239 3431 3039  553309,2.8294109
-000024d0: 2031 362e 3535 3333 3039 2c35 2e32 3133   16.553309,5.213
-000024e0: 3336 3039 207a 204d 2031 392e 3633 3831  3609 z M 19.6381
-000024f0: 3339 2c35 2e32 3133 3336 3039 2043 2031  39,5.2133609 C 1
-00002500: 392e 3633 3831 3339 2c39 2e33 3030 3135  9.638139,9.30015
-00002510: 3039 2031 362e 3332 3133 3239 2c31 322e  09 16.321329,12.
-00002520: 3631 3639 3631 2031 322e 3233 3435 3339  616961 12.234539
-00002530: 2c31 322e 3631 3639 3631 2043 2038 2e31  ,12.616961 C 8.1
-00002540: 3437 3735 3839 2c31 322e 3631 3639 3631  477589,12.616961
-00002550: 2034 2e38 3330 3934 3839 2c39 2e33 3030   4.8309489,9.300
-00002560: 3135 3039 2034 2e38 3330 3934 3839 2c35  1509 4.8309489,5
-00002570: 2e32 3133 3336 3039 2043 2034 2e38 3330  .2133609 C 4.830
-00002580: 3934 3839 2c35 2e32 3133 3336 3039 2034  9489,5.2133609 4
-00002590: 2e38 3330 3934 3839 2c35 2e32 3133 3336  .8309489,5.21336
-000025a0: 3039 2034 2e38 3330 3934 3839 2c35 2e32  09 4.8309489,5.2
-000025b0: 3133 3336 3039 2720 7374 796c 653d 2773  133609' style='s
-000025c0: 7472 6f6b 653a 2470 6c61 6e65 7473 5f63  troke:$planets_c
-000025d0: 6f6c 6f72 5f39 3b20 7374 726f 6b65 2d77  olor_9; stroke-w
-000025e0: 6964 7468 3a32 7078 3b20 6669 6c6c 3a6e  idth:2px; fill:n
-000025f0: 6f6e 653b 2720 2f3e 3c2f 673e 3c2f 673e  one;' /></g></g>
-00002600: 3c2f 7379 6d62 6f6c 3e3c 7379 6d62 6f6c  </symbol><symbol
-00002610: 2069 643d 274d 6561 6e5f 4e6f 6465 273e   id='Mean_Node'>
-00002620: 3c67 2074 7261 6e73 666f 726d 3d27 7472  <g transform='tr
-00002630: 616e 736c 6174 6528 302c 3329 273e 3c70  anslate(0,3)'><p
-00002640: 6174 6820 643d 274d 2038 2e38 3039 3630  ath d='M 8.80960
-00002650: 3436 2c30 2e30 3735 3636 3638 3937 2043  46,0.075666897 C
-00002660: 2036 2e34 3135 3735 3336 2c30 2e36 3631   6.4157536,0.661
-00002670: 3233 3936 3220 342e 3337 3637 3736 392c  23962 4.3767769,
-00002680: 322e 3533 3036 3833 3720 332e 3636 3334  2.5306837 3.6634
-00002690: 3635 362c 342e 3930 3037 3531 3420 4320  656,4.9007514 C 
-000026a0: 332e 3035 3336 3037 312c 362e 3638 3039  3.0536071,6.6809
-000026b0: 3236 3420 332e 3638 3638 3638 322c 382e  264 3.6868682,8.
-000026c0: 3632 3338 3930 3120 342e 3538 3738 3938  6238901 4.587898
-000026d0: 382c 3130 2e31 3836 3433 3720 4320 352e  8,10.186437 C 5.
-000026e0: 3133 3233 3939 372c 3131 2e31 3234 3632  1323997,11.12462
-000026f0: 3220 352e 3936 3135 3735 332c 3131 2e39  2 5.9615753,11.9
-00002700: 3038 3935 2036 2e31 3930 3733 3032 2c31  0895 6.1907302,1
-00002710: 332e 3030 3739 3036 2043 2036 2e35 3931  3.007906 C 6.591
-00002720: 3732 3032 2c31 342e 3438 3434 3838 2036  7202,14.484488 6
-00002730: 2e34 3838 3731 3536 2c31 362e 3338 3735  .4887156,16.3875
-00002740: 3233 2035 2e31 3732 3337 3838 2c31 372e  23 5.1723788,17.
-00002750: 3338 3235 3736 2043 2034 2e33 3332 3939  382576 C 4.33299
-00002760: 3734 2c31 382e 3035 3334 3133 2033 2e30  74,18.053413 3.0
-00002770: 3737 3537 3431 2c31 372e 3435 3530 3334  775741,17.455034
-00002780: 2032 2e38 3230 3031 3336 2c31 362e 3438   2.8200136,16.48
-00002790: 3131 3936 2043 2032 2e33 3931 3635 3532  1196 C 2.3916552
-000027a0: 2c31 352e 3130 3037 3933 2033 2e33 3233  ,15.100793 3.323
-000027b0: 3138 3938 2c31 332e 3339 3634 3536 2034  1898,13.396456 4
-000027c0: 2e37 3739 3333 3136 2c31 332e 3136 3338  .7793316,13.1638
-000027d0: 3036 2043 2035 2e35 3135 3738 3631 2c31  06 C 5.5157861,1
-000027e0: 332e 3434 3834 3839 2035 2e37 3336 3233  3.448489 5.73623
-000027f0: 3533 2c31 332e 3030 3833 3331 2034 2e39  53,13.008331 4.9
-00002800: 3838 3035 312c 3132 2e37 3339 3130 3120  88051,12.739101 
-00002810: 4320 332e 3437 3637 3639 362c 3131 2e39  C 3.4767696,11.9
-00002820: 3830 3736 3120 312e 3234 3331 3839 362c  80761 1.2431896,
-00002830: 3132 2e38 3339 3639 2031 2e30 3335 3134  12.83969 1.03514
-00002840: 3736 2c31 342e 3633 3533 3934 2043 2030  76,14.635394 C 0
-00002850: 2e37 3734 3435 3731 352c 3136 2e32 3938  .77445715,16.298
-00002860: 3538 3220 312e 3935 3238 3834 372c 3137  582 1.9528847,17
-00002870: 2e39 3931 3833 3520 332e 3538 3935 3936  .991835 3.589596
-00002880: 332c 3138 2e33 3537 3435 3920 4320 352e  3,18.357459 C 5.
-00002890: 3432 3736 3636 322c 3138 2e39 3934 3136  4276662,18.99416
-000028a0: 3520 372e 3636 3631 3833 392c 3137 2e39  5 7.6661839,17.9
-000028b0: 3638 3533 3420 382e 3239 3739 3033 392c  68534 8.2979039,
-000028c0: 3136 2e31 3130 3136 3220 4320 382e 3835  16.110162 C 8.85
-000028d0: 3731 3032 352c 3134 2e37 3136 3532 3720  71025,14.716527 
-000028e0: 382e 3534 3635 3438 312c 3133 2e31 3836  8.5465481,13.186
-000028f0: 3133 3920 382e 3032 3839 3836 382c 3131  139 8.0289868,11
-00002900: 2e38 3332 3635 3320 4320 372e 3437 3032  .832653 C 7.4702
-00002910: 3838 352c 3130 2e32 3036 3838 3420 362e  885,10.206884 6.
-00002920: 3235 3533 3636 332c 382e 3837 3039 3637  2553663,8.870967
-00002930: 3420 352e 3932 3939 3035 362c 372e 3135  4 5.9299056,7.15
-00002940: 3235 3833 3820 4320 352e 3439 3134 362c  25838 C 5.49146,
-00002950: 352e 3439 3239 3936 3520 352e 3838 3735  5.4929965 5.8875
-00002960: 3439 382c 332e 3537 3335 3632 3920 372e  498,3.5735629 7.
-00002970: 3233 3239 3630 372c 322e 3433 3237 3231  2329607,2.432721
-00002980: 3320 4320 382e 3733 3838 3539 312c 312e  3 C 8.7388591,1.
-00002990: 3031 3334 3435 3120 3131 2e33 3138 3933  0134451 11.31893
-000029a0: 312c 302e 3735 3537 3038 3220 3132 2e39  1,0.7557082 12.9
-000029b0: 3139 3831 382c 322e 3136 3237 3732 3320  19818,2.1627723 
-000029c0: 4320 3134 2e38 3931 3137 342c 332e 3637  C 14.891174,3.67
-000029d0: 3639 3334 3520 3135 2e32 3935 3036 352c  69345 15.295065,
-000029e0: 362e 3536 3932 3032 3820 3134 2e33 3330  6.5692028 14.330
-000029f0: 3233 372c 382e 3736 3731 3933 3320 4320  237,8.7671933 C 
-00002a00: 3133 2e39 3130 3438 342c 392e 3931 3933  13.910484,9.9193
-00002a10: 3635 3820 3133 2e31 3534 3335 332c 3130  658 13.154353,10
-00002a20: 2e39 3032 3637 3920 3132 2e36 3135 3837  .902679 12.61587
-00002a30: 372c 3131 2e39 3931 3239 3920 4320 3132  7,11.991299 C 12
-00002a40: 2e30 3338 3034 352c 3133 2e35 3438 3236  .038045,13.54826
-00002a50: 2031 322e 3038 3035 3939 2c31 352e 3336   12.080599,15.36
-00002a60: 3438 3133 2031 322e 3737 3734 3535 2c31  4813 12.777455,1
-00002a70: 362e 3837 3531 3633 2043 2031 342e 3037  6.875163 C 14.07
-00002a80: 3639 3436 2c31 392e 3131 3039 3433 2031  6946,19.110943 1
-00002a90: 372e 3930 3333 3736 2c31 382e 3934 3530  7.903376,18.9450
-00002aa0: 3333 2031 392e 3034 3230 3738 2c31 362e  33 19.042078,16.
-00002ab0: 3632 3837 3033 2043 2031 392e 3735 3732  628703 C 19.7572
-00002ac0: 3432 2c31 352e 3236 3132 3237 2031 392e  42,15.261227 19.
-00002ad0: 3330 3638 3139 2c31 332e 3234 3439 3239  306819,13.244929
-00002ae0: 2031 372e 3736 3539 2c31 322e 3637 3139   17.7659,12.6719
-00002af0: 3032 2043 2031 362e 3735 3833 352c 3132  02 C 16.75835,12
-00002b00: 2e32 3130 3936 3120 3135 2e34 3632 3039  .210961 15.46209
-00002b10: 332c 3132 2e34 3432 3935 3120 3134 2e37  3,12.442951 14.7
-00002b20: 3239 3336 362c 3133 2e32 3930 3031 3420  29366,13.290014 
-00002b30: 4320 3135 2e36 3739 3834 392c 3133 2e32  C 15.679849,13.2
-00002b40: 3736 3135 3320 3136 2e39 3830 3239 342c  76153 16.980294,
-00002b50: 3133 2e32 3632 3735 3420 3137 2e33 3433  13.262754 17.343
-00002b60: 3530 322c 3134 2e33 3634 3230 3320 4320  502,14.364203 C 
-00002b70: 3137 2e39 3033 3236 332c 3135 2e34 3932  17.903263,15.492
-00002b80: 3637 3920 3137 2e37 3639 3637 372c 3137  679 17.769677,17
-00002b90: 2e33 3035 3937 3220 3136 2e34 3134 3934  .305972 16.41494
-00002ba0: 392c 3137 2e37 3831 3839 3520 4320 3135  9,17.781895 C 15
-00002bb0: 2e32 3138 3431 382c 3138 2e31 3330 3834  .218418,18.13084
-00002bc0: 2031 342e 3135 3033 3033 2c31 362e 3930   14.150303,16.90
-00002bd0: 3239 3437 2031 342e 3039 3231 3834 2c31  2947 14.092184,1
-00002be0: 352e 3738 3136 3636 2043 2031 332e 3738  5.781666 C 13.78
-00002bf0: 3231 3137 2c31 342e 3130 3134 3033 2031  2117,14.101403 1
-00002c00: 342e 3134 3033 3436 2c31 322e 3237 3033  4.140346,12.2703
-00002c10: 3135 2031 352e 3237 3531 392c 3130 2e39  15 15.27519,10.9
-00002c20: 3538 3034 3220 4320 3136 2e35 3139 3839  58042 C 16.51989
-00002c30: 332c 392e 3439 3438 3736 3320 3137 2e32  3,9.4948763 17.2
-00002c40: 3536 3532 352c 372e 3532 3430 3635 3920  56525,7.5240659 
-00002c50: 3136 2e38 3637 3532 362c 352e 3539 3934  16.867526,5.5994
-00002c60: 3735 3120 4320 3136 2e33 3634 3039 2c32  751 C 16.36409,2
-00002c70: 2e35 3635 3732 3439 2031 332e 3630 3530  .5657249 13.6050
-00002c80: 3031 2c30 2e30 3635 3736 3035 3433 2031  01,0.065760543 1
-00002c90: 302e 3530 3733 3039 2c2d 302e 3030 3437  0.507309,-0.0047
-00002ca0: 3534 3732 3635 2043 2039 2e39 3431 3037  547265 C 9.94107
-00002cb0: 332c 2d30 2e30 3135 3833 3036 3932 2039  3,-0.015830692 9
-00002cc0: 2e33 3732 3235 3934 2c30 2e30 3039 3334  .3722594,0.00934
-00002cd0: 3738 3631 3920 382e 3830 3936 3034 362c  78619 8.8096046,
-00002ce0: 302e 3037 3536 3636 3839 3720 7a27 2073  0.075666897 z' s
-00002cf0: 7479 6c65 3d27 6669 6c6c 3a20 2470 6c61  tyle='fill: $pla
-00002d00: 6e65 7473 5f63 6f6c 6f72 5f31 303b 2720  nets_color_10;' 
-00002d10: 2f3e 3c2f 673e 3c2f 7379 6d62 6f6c 3e3c  /></g></symbol><
-00002d20: 7379 6d62 6f6c 2069 643d 2754 7275 655f  symbol id='True_
-00002d30: 4e6f 6465 273e 3c2f 7379 6d62 6f6c 3e3c  Node'></symbol><
-00002d40: 7379 6d62 6f6c 2069 643d 2731 273e 3c74  symbol id='1'><t
-00002d50: 6578 7420 793d 2732 3027 2073 7479 6c65  ext y='20' style
-00002d60: 3d27 666f 6e74 2d73 697a 653a 3232 7078  ='font-size:22px
-00002d70: 3b20 6669 6c6c 3a20 2470 6c61 6e65 7473  ; fill: $planets
-00002d80: 5f63 6f6c 6f72 5f31 323b 273e 4173 3c2f  _color_12;'>As</
-00002d90: 7465 7874 3e3c 2f73 796d 626f 6c3e 3c73  text></symbol><s
-00002da0: 796d 626f 6c20 6964 3d27 3130 273e 3c74  ymbol id='10'><t
-00002db0: 6578 7420 793d 2732 3027 2073 7479 6c65  ext y='20' style
-00002dc0: 3d27 666f 6e74 2d73 697a 653a 3230 7078  ='font-size:20px
-00002dd0: 3b20 6669 6c6c 3a20 2470 6c61 6e65 7473  ; fill: $planets
-00002de0: 5f63 6f6c 6f72 5f31 333b 273e 4d63 3c2f  _color_13;'>Mc</
-00002df0: 7465 7874 3e3c 2f73 796d 626f 6c3e 3c73  text></symbol><s
-00002e00: 796d 626f 6c20 6964 3d27 3727 3e3c 7465  ymbol id='7'><te
-00002e10: 7874 2079 3d27 3230 2720 7374 796c 653d  xt y='20' style=
-00002e20: 2766 6f6e 742d 7369 7a65 3a32 3270 783b  'font-size:22px;
-00002e30: 2066 696c 6c3a 2024 706c 616e 6574 735f   fill: $planets_
-00002e40: 636f 6c6f 725f 3134 3b27 3e44 733c 2f74  color_14;'>Ds</t
-00002e50: 6578 743e 3c2f 7379 6d62 6f6c 3e3c 7379  ext></symbol><sy
-00002e60: 6d62 6f6c 2069 643d 2734 273e 3c74 6578  mbol id='4'><tex
-00002e70: 7420 793d 2732 3027 2073 7479 6c65 3d27  t y='20' style='
-00002e80: 666f 6e74 2d73 697a 653a 3232 7078 3b20  font-size:22px; 
-00002e90: 6669 6c6c 3a20 2470 6c61 6e65 7473 5f63  fill: $planets_c
-00002ea0: 6f6c 6f72 5f31 353b 273e 4963 3c2f 7465  olor_15;'>Ic</te
-00002eb0: 7874 3e3c 2f73 796d 626f 6c3e 3c21 2d2d  xt></symbol><!--
-00002ec0: 205a 6f64 6961 6320 2d2d 3e3c 7379 6d62   Zodiac --><symb
-00002ed0: 6f6c 2069 643d 2761 7269 6573 273e 3c70  ol id='aries'><p
-00002ee0: 6174 6820 643d 274d 2031 342e 3833 3335  ath d='M 14.8335
-00002ef0: 3336 2c33 3120 4320 3134 2e38 3332 3138  36,31 C 14.83218
-00002f00: 362c 3239 2e37 3238 3235 2031 342e 3834  6,29.72825 14.84
-00002f10: 3539 3336 2c32 382e 3435 3538 3420 3134  5936,28.45584 14
-00002f20: 2e37 3830 3334 362c 3237 2e31 3835 3233  .780346,27.18523
-00002f30: 2043 2031 342e 3634 3039 3236 2c32 342e   C 14.640926,24.
-00002f40: 3233 3034 3620 3134 2e32 3731 3932 372c  23046 14.271927,
-00002f50: 3231 2e32 3839 3739 2031 332e 3736 3136  21.28979 13.7616
-00002f60: 3537 2c31 382e 3337 3736 2043 2031 332e  57,18.3776 C 13.
-00002f70: 3332 3139 3837 2c31 352e 3931 3931 3120  321987,15.91911 
-00002f80: 3132 2e37 3837 3738 372c 3133 2e34 3639  12.787787,13.469
-00002f90: 3833 2031 312e 3939 3035 3137 2c31 312e  83 11.990517,11.
-00002fa0: 3130 3037 3520 4320 3131 2e35 3330 3236  10075 C 11.53026
-00002fb0: 372c 392e 3736 3234 3320 3130 2e39 3932  7,9.76243 10.992
-00002fc0: 3838 372c 382e 3434 3931 3220 3130 2e33  887,8.44912 10.3
-00002fd0: 3537 3038 372c 372e 3138 3439 2043 2039  57087,7.1849 C 9
-00002fe0: 2e37 3736 3430 3635 2c36 2e30 3534 2039  .7764065,6.054 9
-00002ff0: 2e31 3134 3334 3635 2c34 2e39 3432 3936  .1143465,4.94296
-00003000: 2038 2e32 3136 3030 3635 2c34 2e30 3334   8.2160065,4.034
-00003010: 3934 2043 2037 2e36 3238 3234 3635 2c33  94 C 7.6282465,3
-00003020: 2e34 3436 3520 362e 3930 3037 3236 352c  .4465 6.9007265,
-00003030: 322e 3934 3533 3520 362e 3036 3439 3736  2.94535 6.064976
-00003040: 352c 322e 3831 3632 3420 4320 352e 3332  5,2.81624 C 5.32
-00003050: 3337 3236 362c 322e 3730 3134 3220 342e  37266,2.70142 4.
-00003060: 3533 3034 3636 362c 322e 3837 3537 3120  5304666,2.87571 
-00003070: 332e 3933 3536 3936 362c 332e 3334 3338  3.9356966,3.3438
-00003080: 3420 4320 332e 3231 3336 3536 352c 332e  4 C 3.2136565,3.
-00003090: 3930 3531 3920 322e 3736 3534 3336 352c  90519 2.7654365,
-000030a0: 342e 3735 3632 3520 322e 3534 3338 3336  4.75625 2.543836
-000030b0: 352c 352e 3633 3238 3920 4320 322e 3330  5,5.63289 C 2.30
-000030c0: 3533 3736 352c 362e 3539 3939 3520 322e  53765,6.59995 2.
-000030d0: 3239 3539 3736 352c 372e 3631 3335 3820  2959765,7.61358 
-000030e0: 322e 3432 3932 3136 352c 382e 3539 3733  2.4292165,8.5973
-000030f0: 2043 2032 2e36 3436 3434 3635 2c31 302e   C 2.6464465,10.
-00003100: 3135 3538 3720 332e 3236 3839 3636 352c  15587 3.2689665,
-00003110: 3131 2e36 3332 3538 2034 2e30 3831 3534  11.63258 4.08154
-00003120: 3636 2c31 322e 3936 3930 3820 4320 332e  66,12.96908 C 3.
-00003130: 3239 3234 3436 352c 3132 2e39 3639 3038  2924465,12.96908
-00003140: 2032 2e35 3033 3334 3635 2c31 322e 3936   2.5033465,12.96
-00003150: 3930 3820 312e 3731 3432 3436 352c 3132  908 1.7142465,12
-00003160: 2e39 3639 3038 2043 2030 2e38 3937 3234  .96908 C 0.89724
-00003170: 3635 312c 3131 2e34 3834 3831 2030 2e32  651,11.48481 0.2
-00003180: 3537 3939 3635 312c 392e 3837 3239 3920  5799651,9.87299 
-00003190: 302e 3036 3032 3536 3531 342c 382e 3137  0.060256514,8.17
-000031a0: 3839 3920 4320 2d30 2e30 3731 3230 3334  899 C -0.0712034
-000031b0: 3836 2c37 2e30 3036 3935 2030 2e30 3033  86,7.00695 0.003
-000031c0: 3731 3635 3133 382c 352e 3739 3930 3320  7165138,5.79903 
-000031d0: 302e 3337 3134 3936 3531 2c34 2e36 3734  0.37149651,4.674
-000031e0: 3231 2043 2030 2e37 3634 3432 3635 312c  21 C 0.76442651,
-000031f0: 332e 3437 3439 3920 312e 3531 3935 3836  3.47499 1.519586
-00003200: 352c 322e 3339 3332 2032 2e35 3233 3235  5,2.3932 2.52325
-00003210: 3635 2c31 2e36 3330 3420 4320 332e 3238  65,1.6304 C 3.28
-00003220: 3039 3636 352c 312e 3035 3437 3820 342e  09665,1.05478 4.
-00003230: 3230 3539 3336 362c 302e 3731 3236 3820  2059366,0.71268 
-00003240: 352e 3135 3139 3436 362c 302e 3633 3738  5.1519466,0.6378
-00003250: 3120 4320 362e 3139 3338 3236 352c 302e  1 C 6.1938265,0.
-00003260: 3534 3439 3620 372e 3236 3130 3436 352c  54496 7.2610465,
-00003270: 302e 3734 3631 3920 382e 3139 3039 3236  0.74619 8.190926
-00003280: 352c 312e 3232 3937 3620 4320 392e 3339  5,1.22976 C 9.39
-00003290: 3938 3636 352c 312e 3835 3032 3120 3130  98665,1.85021 10
-000032a0: 2e33 3633 3637 372c 322e 3835 3934 3420  .363677,2.85944 
-000032b0: 3131 2e31 3435 3237 372c 332e 3935 3736  11.145277,3.9576
-000032c0: 3620 4320 3132 2e31 3930 3334 372c 352e  6 C 12.190347,5.
-000032d0: 3434 3134 3720 3132 2e39 3635 3036 372c  44147 12.965067,
-000032e0: 372e 3130 3130 3120 3133 2e35 3834 3238  7.10101 13.58428
-000032f0: 372c 382e 3830 3338 3220 4320 3134 2e36  7,8.80382 C 14.6
-00003300: 3330 3736 362c 3131 2e37 3137 3620 3135  30766,11.7176 15
-00003310: 2e32 3132 3632 362c 3134 2e37 3738 3631  .212626,14.77861
-00003320: 2031 352e 3537 3531 3436 2c31 372e 3834   15.575146,17.84
-00003330: 3739 3520 4320 3135 2e36 3634 3833 362c  795 C 15.664836,
-00003340: 3138 2e36 3136 3438 2031 352e 3733 3935  18.61648 15.7395
-00003350: 3536 2c31 392e 3338 3637 3520 3135 2e38  56,19.38675 15.8
-00003360: 3031 3434 362c 3230 2e31 3538 3033 2043  01446,20.15803 C
-00003370: 2031 352e 3933 3336 3036 2c32 302e 3135   15.933606,20.15
-00003380: 3830 3320 3136 2e30 3635 3737 362c 3230  803 16.065776,20
-00003390: 2e31 3538 3033 2031 362e 3139 3739 3336  .15803 16.197936
-000033a0: 2c32 302e 3135 3830 3320 4320 3136 2e34  ,20.15803 C 16.4
-000033b0: 3331 3531 362c 3136 2e37 3833 3332 2031  31516,16.78332 1
-000033c0: 362e 3931 3930 3636 2c31 332e 3430 3736  6.919066,13.4076
-000033d0: 3120 3137 2e39 3230 3233 362c 3130 2e31  1 17.920236,10.1
-000033e0: 3730 3239 2043 2031 382e 3533 3637 3436  7029 C 18.536746
-000033f0: 2c38 2e31 3938 3836 2031 392e 3334 3332  ,8.19886 19.3432
-00003400: 3136 2c36 2e32 3733 3320 3230 2e34 3630  16,6.2733 20.460
-00003410: 3130 362c 342e 3533 3230 3920 4320 3231  106,4.53209 C 21
-00003420: 2e32 3332 3936 362c 332e 3334 3234 3620  .232966,3.34246 
-00003430: 3232 2e31 3738 3339 362c 322e 3232 3639  22.178396,2.2269
-00003440: 3120 3233 2e33 3933 3233 362c 312e 3437  1 23.393236,1.47
-00003450: 3437 3320 4320 3234 2e33 3033 3934 362c  473 C 24.303946,
-00003460: 302e 3930 3620 3235 2e33 3735 3430 362c  0.906 25.375406,
-00003470: 302e 3539 3331 3520 3236 2e34 3439 3833  0.59315 26.44983
-00003480: 362c 302e 3631 3734 3420 4320 3237 2e34  6,0.61744 C 27.4
-00003490: 3036 3037 362c 302e 3632 3635 2032 382e  06076,0.6265 28.
-000034a0: 3336 3633 3336 2c30 2e38 3834 3134 2032  366336,0.88414 2
-000034b0: 392e 3137 3333 3836 2c31 2e34 3035 3731  9.173386,1.40571
-000034c0: 2043 2032 392e 3931 3832 3736 2c31 2e38   C 29.918276,1.8
-000034d0: 3834 3137 2033 302e 3533 3637 3236 2c32  8417 30.536726,2
-000034e0: 2e35 3438 3235 2033 312e 3030 3733 3036  .54825 31.007306
-000034f0: 2c33 2e32 3936 3838 2043 2033 312e 3634  ,3.29688 C 31.64
-00003500: 3033 3736 2c34 2e33 3039 3831 2033 312e  0376,4.30981 31.
-00003510: 3934 3237 3836 2c35 2e35 3033 3620 3331  942786,5.5036 31
-00003520: 2e39 3930 3532 362c 362e 3639 3134 3920  .990526,6.69149 
-00003530: 4320 3332 2e30 3634 3336 362c 382e 3234  C 32.064366,8.24
-00003540: 3839 3820 3331 2e37 3030 3330 362c 392e  898 31.700306,9.
-00003550: 3739 3834 3120 3331 2e31 3138 3133 362c  79841 31.118136,
-00003560: 3131 2e32 3334 3039 2043 2033 302e 3837  11.23409 C 30.87
-00003570: 3830 3536 2c31 312e 3832 3737 3420 3330  8056,11.82774 30
-00003580: 2e36 3030 3734 362c 3132 2e34 3035 3834  .600746,12.40584
-00003590: 2033 302e 3239 3637 3936 2c31 322e 3936   30.296796,12.96
-000035a0: 3930 3820 4320 3239 2e35 3033 3830 362c  908 C 29.503806,
-000035b0: 3132 2e39 3639 3038 2032 382e 3731 3038  12.96908 28.7108
-000035c0: 3236 2c31 322e 3936 3930 3820 3237 2e39  26,12.96908 27.9
-000035d0: 3137 3833 362c 3132 2e39 3639 3038 2043  17836,12.96908 C
-000035e0: 2032 382e 3639 3536 3436 2c31 312e 3536   28.695646,11.56
-000035f0: 3832 3520 3239 2e33 3330 3930 362c 3130  825 29.330906,10
-00003600: 2e30 3630 3434 2032 392e 3536 3537 3536  .06044 29.565756
-00003610: 2c38 2e34 3634 3835 2043 2032 392e 3730  ,8.46485 C 29.70
-00003620: 3534 3336 2c37 2e34 3930 3533 2032 392e  5436,7.49053 29.
-00003630: 3638 3939 3736 2c36 2e34 3837 3339 2032  689976,6.48739 2
-00003640: 392e 3436 3937 3336 2c35 2e35 3236 3136  9.469736,5.52616
-00003650: 2043 2032 392e 3236 3635 3836 2c34 2e36   C 29.266586,4.6
-00003660: 3732 3936 2032 382e 3837 3039 3536 2c33  7296 28.870956,3
-00003670: 2e38 3333 3534 2032 382e 3230 3132 3736  .83354 28.201276
-00003680: 2c33 2e32 3530 3739 2043 2032 372e 3731  ,3.25079 C 27.71
-00003690: 3833 3836 2c32 2e38 3232 3633 2032 372e  8386,2.82263 27.
-000036a0: 3037 3834 3636 2c32 2e35 3930 3231 2032  078466,2.59021 2
-000036b0: 362e 3433 3632 3136 2c32 2e35 3834 3436  6.436216,2.58446
-000036c0: 2043 2032 352e 3638 3033 3036 2c32 2e35   C 25.680306,2.5
-000036d0: 3630 3539 2032 342e 3935 3030 3836 2c32  6059 24.950086,2
-000036e0: 2e38 3733 3033 2032 342e 3335 3833 3336  .87303 24.358336
-000036f0: 2c33 2e33 3238 3739 2043 2032 332e 3439  ,3.32879 C 23.49
-00003700: 3435 3536 2c33 2e39 3933 3037 2032 322e  4556,3.99307 22.
-00003710: 3834 3439 3836 2c34 2e38 3931 3938 2032  844986,4.89198 2
-00003720: 322e 3238 3239 3536 2c35 2e38 3136 3739  2.282956,5.81679
-00003730: 2043 2032 312e 3435 3137 3536 2c37 2e32   C 21.451756,7.2
-00003740: 3130 3732 2032 302e 3831 3134 3336 2c38  1072 20.811436,8
-00003750: 2e37 3130 3138 2032 302e 3235 3033 3936  .71018 20.250396
-00003760: 2c31 302e 3233 3132 3420 4320 3139 2e34  ,10.23124 C 19.4
-00003770: 3337 3538 362c 3132 2e34 3938 3032 2031  37586,12.49802 1
-00003780: 382e 3839 3333 3236 2c31 342e 3835 3136  8.893326,14.8516
-00003790: 3620 3138 2e34 3430 3238 362c 3137 2e32  6 18.440286,17.2
-000037a0: 3134 3332 2043 2031 372e 3833 3930 3136  1432 C 17.839016
-000037b0: 2c32 302e 3430 3332 3520 3137 2e34 3133  ,20.40325 17.413
-000037c0: 3231 362c 3233 2e36 3239 3120 3137 2e32  216,23.6291 17.2
-000037d0: 3436 3133 362c 3236 2e38 3731 3520 4320  46136,26.8715 C 
-000037e0: 3137 2e31 3833 3739 362c 3238 2e30 3138  17.183796,28.018
-000037f0: 3537 2031 372e 3137 3339 3636 2c32 392e  57 17.173966,29.
-00003800: 3136 3734 3520 3137 2e31 3737 3531 362c  16745 17.177516,
-00003810: 3330 2e33 3135 3935 2043 2031 372e 3137  30.31595 C 17.17
-00003820: 3735 3136 2c33 302e 3534 3339 3720 3137  7516,30.54397 17
-00003830: 2e31 3737 3531 362c 3330 2e37 3731 3938  .177516,30.77198
-00003840: 2031 372e 3137 3735 3136 2c33 3120 4320   17.177516,31 C 
-00003850: 3136 2e33 3936 3138 362c 3331 2031 352e  16.396186,31 15.
-00003860: 3631 3438 3536 2c33 3120 3134 2e38 3333  614856,31 14.833
-00003870: 3533 362c 3331 207a 2720 7374 796c 653d  536,31 z' style=
-00003880: 2766 696c 6c3a 2024 7a6f 6469 6163 5f63  'fill: $zodiac_c
-00003890: 6f6c 6f72 5f30 3b27 202f 3e3c 2f73 796d  olor_0;' /></sym
-000038a0: 626f 6c3e 3c73 796d 626f 6c20 6964 3d27  bol><symbol id='
-000038b0: 7461 7572 7573 273e 3c70 6174 6820 643d  taurus'><path d=
-000038c0: 274d 2031 312e 3231 3131 3235 2c31 312e  'M 11.211125,11.
-000038d0: 3936 3030 3433 2043 2039 2e39 3835 3631  960043 C 9.98561
-000038e0: 3937 2c31 312e 3438 3230 3835 2038 2e38  97,11.482085 8.8
-000038f0: 3237 3335 3037 2c31 302e 3735 3732 3633  273507,10.757263
-00003900: 2037 2e39 3939 3431 3634 2c39 2e37 3232   7.9994164,9.722
-00003910: 3636 2043 2036 2e39 3534 3035 3834 2c38  66 C 6.9540584,8
-00003920: 2e34 3438 3935 3038 2036 2e32 3131 3935  .4489508 6.21195
-00003930: 3234 2c36 2e39 3639 3630 3937 2035 2e34  24,6.9696097 5.4
-00003940: 3036 3831 3939 2c35 2e35 3432 3235 3135  068199,5.5422515
-00003950: 2043 2034 2e39 3135 3333 3336 2c34 2e36   C 4.9153336,4.6
-00003960: 3433 3539 3331 2034 2e33 3538 3834 3532  435931 4.3588452
-00003970: 2c33 2e37 3630 3431 3238 2033 2e36 3030  ,3.7604128 3.600
-00003980: 3236 3836 2c33 2e30 3630 3130 3336 2043  2686,3.0601036 C
-00003990: 2033 2e30 3837 3733 3731 2c32 2e35 3833   3.0877371,2.583
-000039a0: 3033 3939 2032 2e34 3639 3934 3333 2c32  0399 2.4699433,2
-000039b0: 2e31 3937 3731 3239 2031 2e37 3739 3133  .1977129 1.77913
-000039c0: 3231 2c32 2e30 3436 3231 3738 2043 2031  21,2.0462178 C 1
-000039d0: 2e34 3531 3438 3637 2c31 2e39 3636 3334  .4514867,1.96634
-000039e0: 3531 2031 2e31 3132 3736 3938 2c31 2e39  51 1.1127698,1.9
-000039f0: 3633 3430 3635 2030 2e37 3737 3536 3634  634065 0.7775664
-00003a00: 382c 312e 3936 3933 3230 3320 4320 302e  8,1.9693203 C 0.
-00003a10: 3637 3735 3031 3338 2c31 2e39 3832 3438  67750138,1.98248
-00003a20: 3033 2030 2e35 3938 3333 3530 382c 312e  03 0.59833508,1.
-00003a30: 3937 3437 3539 3520 302e 3633 3336 3930  9747595 0.633690
-00003a40: 3838 2c31 2e38 3532 3833 3333 2043 2030  88,1.8528333 C 0
-00003a50: 2e36 3333 3639 3038 382c 312e 3237 3033  .63369088,1.2703
-00003a60: 3631 3820 302e 3633 3336 3930 3838 2c30  618 0.63369088,0
-00003a70: 2e36 3837 3839 3032 3320 302e 3633 3336  .68789023 0.6336
-00003a80: 3930 3838 2c30 2e31 3035 3430 3034 3420  9088,0.10540044 
-00003a90: 4320 312e 3137 3639 332c 302e 3131 3137  C 1.17693,0.1117
-00003aa0: 3838 3834 2031 2e37 3231 3032 3932 2c30  8884 1.7210292,0
-00003ab0: 2e30 3930 3135 3936 3431 2032 2e32 3633  .090159641 2.263
-00003ac0: 3630 3935 2c30 2e31 3231 3639 3938 3420  6095,0.12169984 
-00003ad0: 4320 332e 3334 3933 3733 392c 302e 3231  C 3.3493739,0.21
-00003ae0: 3230 3835 3934 2034 2e33 3636 3531 3239  208594 4.3665129
-00003af0: 2c30 2e37 3135 3837 3132 3120 352e 3139  ,0.71587121 5.19
-00003b00: 3137 3933 352c 312e 3430 3937 3535 3520  17935,1.4097555 
-00003b10: 4320 362e 3236 3437 3834 342c 322e 3330  C 6.2647844,2.30
-00003b20: 3133 3332 2037 2e30 3838 3837 3534 2c33  1332 7.0888754,3
-00003b30: 2e34 3439 3438 3237 2037 2e37 3931 3136  .4494827 7.79116
-00003b40: 3134 2c34 2e36 3433 3634 3739 2043 2038  14,4.6436479 C 8
-00003b50: 2e32 3931 3330 3334 2c35 2e35 3034 3638  .2913034,5.50468
-00003b60: 3820 382e 3737 3231 3735 372c 362e 3337  8 8.7721757,6.37
-00003b70: 3637 3532 3520 392e 3237 3433 3132 372c  67525 9.2743127,
-00003b80: 372e 3233 3636 3036 3220 4320 392e 3735  7.2366062 C 9.75
-00003b90: 3838 3038 372c 382e 3034 3633 3536 3920  88087,8.0463569 
-00003ba0: 3130 2e33 3037 3634 382c 382e 3832 3437  10.307648,8.8247
-00003bb0: 3836 3520 3130 2e39 3731 3533 392c 392e  865 10.971539,9.
-00003bc0: 3439 3839 3934 3820 4320 3131 2e35 3538  4989948 C 11.558
-00003bd0: 3731 372c 3130 2e30 3934 3639 3920 3132  717,10.094699 12
-00003be0: 2e32 3631 3537 2c31 302e 3538 3639 3637  .26157,10.586967
-00003bf0: 2031 332e 3035 3239 342c 3130 2e38 3731   13.05294,10.871
-00003c00: 3133 3920 4320 3134 2e31 3530 3936 362c  139 C 14.150966,
-00003c10: 3131 2e32 3736 3336 3220 3135 2e33 3339  11.276362 15.339
-00003c20: 3034 362c 3131 2e33 3539 3535 3620 3136  046,11.359556 16
-00003c30: 2e35 3030 3234 342c 3131 2e33 3134 3633  .500244,11.31463
-00003c40: 3720 4320 3137 2e35 3433 3230 342c 3131  7 C 17.543204,11
-00003c50: 2e32 3632 3637 3220 3138 2e36 3032 3036  .262672 18.60206
-00003c60: 382c 3131 2e30 3639 3631 3620 3139 2e35  8,11.069616 19.5
-00003c70: 3239 3739 322c 3130 2e35 3731 3734 3520  29792,10.571745 
-00003c80: 4320 3230 2e34 3031 3333 352c 3130 2e31  C 20.401335,10.1
-00003c90: 3134 3636 3720 3231 2e31 3033 3830 342c  14667 21.103804,
-00003ca0: 392e 3339 3730 3931 3420 3231 2e37 3030  9.3970914 21.700
-00003cb0: 3034 2c38 2e36 3236 3736 3539 2043 2032  04,8.6267659 C 2
-00003cc0: 322e 3338 3530 3837 2c37 2e37 3431 3139  2.385087,7.74119
-00003cd0: 3436 2032 322e 3930 3639 372c 362e 3734  46 22.90697,6.74
-00003ce0: 3737 3333 3120 3233 2e34 3732 372c 352e  77331 23.4727,5.
-00003cf0: 3738 3539 3033 3120 4320 3233 2e39 3733  7859031 C 23.973
-00003d00: 3239 392c 342e 3933 3231 3435 3820 3234  299,4.9321458 24
-00003d10: 2e34 3435 3531 362c 342e 3035 3836 3032  .445516,4.058602
-00003d20: 3820 3235 2e30 3332 3239 312c 332e 3235  8 25.032291,3.25
-00003d30: 3839 3039 3120 4320 3235 2e37 3131 3836  89091 C 25.71186
-00003d40: 362c 322e 3332 3437 3836 3320 3236 2e35  6,2.3247863 26.5
-00003d50: 3136 3633 322c 312e 3435 3538 3234 3720  16632,1.4558247 
-00003d60: 3237 2e35 3037 3736 362c 302e 3834 3539  27.507766,0.8459
-00003d70: 3932 3737 2043 2032 382e 3236 3634 3731  9277 C 28.266471
-00003d80: 2c30 2e33 3833 3233 3839 3420 3239 2e31  ,0.38323894 29.1
-00003d90: 3436 3337 372c 302e 3039 3635 3438 3034  46377,0.09654804
-00003da0: 3120 3330 2e30 3430 3833 322c 302e 3130  1 30.040832,0.10
-00003db0: 3636 3539 3834 2043 2033 302e 3435 3034  665984 C 30.4504
-00003dc0: 3236 2c30 2e31 3032 3036 3032 3420 3330  26,0.10206024 30
-00003dd0: 2e38 3630 3037 342c 302e 3130 3739 3337  .860074,0.107937
-00003de0: 3534 2033 312e 3236 3936 3637 2c30 2e31  54 31.269667,0.1
-00003df0: 3035 3430 3034 3420 4320 3331 2e32 3639  0540044 C 31.269
-00003e00: 3636 372c 302e 3732 3637 3133 3135 2033  667,0.72671315 3
-00003e10: 312e 3236 3936 3637 2c31 2e33 3438 3032  1.269667,1.34802
-00003e20: 3538 2033 312e 3236 3936 3637 2c31 2e39  58 31.269667,1.9
-00003e30: 3639 3332 3033 2043 2033 302e 3833 3635  693203 C 30.8365
-00003e40: 342c 312e 3936 3631 3037 3820 3330 2e33  4,1.9661078 30.3
-00003e50: 3935 3336 312c 312e 3935 3833 3638 3820  95361,1.9583688 
-00003e60: 3239 2e39 3736 3036 382c 322e 3038 3430  29.976068,2.0840
-00003e70: 3535 2043 2032 392e 3131 3939 3334 2c32  55 C 29.119934,2
-00003e80: 2e33 3138 3637 3138 2032 382e 3430 3034  .3186718 28.4004
-00003e90: 3833 2c32 2e38 3932 3536 3436 2032 372e  83,2.8925646 27.
-00003ea0: 3832 3639 3339 2c33 2e35 3531 3736 3933  826939,3.5517693
-00003eb0: 2043 2032 372e 3233 3630 3238 2c34 2e32   C 27.236028,4.2
-00003ec0: 3233 3538 3635 2032 362e 3738 3832 3631  235865 26.788261
-00003ed0: 2c35 2e30 3032 3833 3734 2032 362e 3336  ,5.0028374 26.36
-00003ee0: 3136 3636 2c35 2e37 3834 3336 3939 2043  1666,5.7843699 C
-00003ef0: 2032 352e 3632 3331 312c 372e 3130 3130   25.62311,7.1010
-00003f00: 3831 3920 3234 2e39 3236 3136 382c 382e  819 24.926168,8.
-00003f10: 3435 3433 3920 3233 2e39 3734 3934 362c  45439 23.974946,
-00003f20: 392e 3633 3537 3233 3720 4320 3233 2e35  9.6357237 C 23.5
-00003f30: 3933 3535 342c 3130 2e31 3135 3238 3820  93554,10.115288 
-00003f40: 3233 2e31 3532 3131 382c 3130 2e35 3437  23.152118,10.547
-00003f50: 3831 3620 3232 2e36 3532 3530 362c 3130  816 22.652506,10
-00003f60: 2e39 3034 3334 3120 4320 3232 2e30 3439  .904341 C 22.049
-00003f70: 3831 2c31 312e 3334 3132 3637 2032 312e  81,11.341267 21.
-00003f80: 3338 3333 3735 2c31 312e 3638 3533 3236  383375,11.685326
-00003f90: 2032 302e 3639 3232 3136 2c31 312e 3936   20.692216,11.96
-00003fa0: 3030 3433 2043 2032 322e 3334 3839 3831  0043 C 22.348981
-00003fb0: 2c31 322e 3836 3532 3534 2032 332e 3832  ,12.865254 23.82
-00003fc0: 3833 3038 2c31 342e 3132 3236 3436 2032  8308,14.122646 2
-00003fd0: 342e 3839 3633 3339 2c31 352e 3638 3430  4.896339,15.6840
-00003fe0: 3331 2043 2032 352e 3739 3635 3034 2c31  31 C 25.796504,1
-00003ff0: 362e 3938 3630 3837 2032 362e 3339 3433  6.986087 26.3943
-00004000: 3134 2c31 382e 3439 3931 3538 2032 362e  14,18.499158 26.
-00004010: 3539 3239 3433 2c32 302e 3037 3030 3920  592943,20.07009 
-00004020: 4320 3236 2e37 3836 3633 322c 3231 2e35  C 26.786632,21.5
-00004030: 3532 3135 3120 3236 2e36 3739 3434 382c  52151 26.679448,
-00004040: 3233 2e30 3737 3738 2032 362e 3234 3633  23.07778 26.2463
-00004050: 3934 2c32 342e 3531 3031 3934 2043 2032  94,24.510194 C 2
-00004060: 352e 3739 3431 3235 2c32 352e 3939 3130  5.794125,25.9910
-00004070: 3332 2032 342e 3937 3633 3834 2c32 372e  32 24.976384,27.
-00004080: 3334 3935 3035 2032 332e 3932 3539 3735  349505 23.925975
-00004090: 2c32 382e 3438 3530 3037 2043 2032 322e  ,28.485007 C 22.
-000040a0: 3636 3536 3436 2c32 392e 3836 3631 3520  665646,29.86615 
-000040b0: 3231 2e30 3835 3939 382c 3330 2e39 3834  21.085998,30.984
-000040c0: 3733 3220 3139 2e33 3031 3234 322c 3331  732 19.301242,31
-000040d0: 2e35 3736 3933 3220 4320 3137 2e35 3532  .576932 C 17.552
-000040e0: 3230 382c 3332 2e31 3537 3431 3420 3135  208,32.157414 15
-000040f0: 2e36 3532 3830 322c 3332 2e32 3436 3631  .652802,32.24661
-00004100: 3420 3133 2e38 3436 3038 362c 3331 2e39  4 13.846086,31.9
-00004110: 3032 3735 3620 4320 3132 2e32 3230 3139  02756 C 12.22019
-00004120: 332c 3331 2e35 3834 3438 3920 3130 2e36  3,31.584489 10.6
-00004130: 3835 3736 352c 3330 2e38 3435 3835 2039  85765,30.84585 9
-00004140: 2e34 3030 3837 3637 2c32 392e 3830 3536  .4008767,29.8056
-00004150: 3235 2043 2038 2e33 3030 3134 3234 2c32  25 C 8.3001424,2
-00004160: 382e 3932 3333 3033 2037 2e33 3335 3436  8.923303 7.33546
-00004170: 3934 2c32 372e 3836 3138 3135 2036 2e36  94,27.861815 6.6
-00004180: 3036 3737 3734 2c32 362e 3635 3239 3536  067774,26.652956
-00004190: 2043 2035 2e38 3431 3530 3237 2c32 352e   C 5.8415027,25.
-000041a0: 3337 3532 3331 2035 2e33 3730 3635 3839  375231 5.3706589
-000041b0: 2c32 332e 3932 3334 3135 2035 2e32 3437  ,23.923415 5.247
-000041c0: 3834 3638 2c32 322e 3433 3937 3132 2043  8468,22.439712 C
-000041d0: 2035 2e30 3832 3335 3838 2c32 302e 3539   5.0823588,20.59
-000041e0: 3636 2035 2e33 3933 3939 3135 2c31 382e  66 5.3939915,18.
-000041f0: 3730 3134 3520 362e 3231 3632 3730 342c  70145 6.2162704,
-00004200: 3137 2e30 3337 3231 3220 4320 372e 3131  17.037212 C 7.11
-00004210: 3636 3336 342c 3135 2e31 3931 3336 3220  66364,15.191362 
-00004220: 382e 3536 3433 3232 342c 3133 2e36 3334  8.5643224,13.634
-00004230: 3939 3520 3130 2e32 3833 3534 362c 3132  995 10.283546,12
-00004240: 2e35 3137 3536 3320 4320 3130 2e35 3835  .517563 C 10.585
-00004250: 3239 372c 3132 2e33 3139 3734 3420 3130  297,12.319744 10
-00004260: 2e38 3935 3030 382c 3132 2e31 3334 3036  .895008,12.13406
-00004270: 3220 3131 2e32 3131 3132 352c 3131 2e39  2 11.211125,11.9
-00004280: 3630 3034 3320 7a20 4d20 3135 2e39 3537  60043 z M 15.957
-00004290: 3932 2c32 392e 3630 3533 3035 2043 2031  92,29.605305 C 1
-000042a0: 372e 3436 3936 3734 2c32 392e 3631 3339  7.469674,29.6139
-000042b0: 3338 2031 382e 3939 3537 3033 2c32 392e  38 18.995703,29.
-000042c0: 3232 3830 3634 2032 302e 3237 3739 3734  228064 20.277974
-000042d0: 2c32 382e 3431 3831 3320 4320 3231 2e32  ,28.41813 C 21.2
-000042e0: 3832 3433 312c 3237 2e37 3839 3436 3220  82431,27.789462 
-000042f0: 3232 2e31 3533 3632 372c 3236 2e39 3532  22.153627,26.952
-00004300: 3533 3320 3232 2e38 3337 3934 322c 3235  533 22.837942,25
-00004310: 2e39 3837 3736 3520 4320 3233 2e35 3936  .987765 C 23.596
-00004320: 3430 382c 3234 2e39 3031 3532 3620 3234  408,24.901526 24
-00004330: 2e30 3536 3538 332c 3233 2e36 3132 3739  .056583,23.61279
-00004340: 3520 3234 2e31 3630 3134 342c 3232 2e32  5 24.160144,22.2
-00004350: 3933 3231 3820 4320 3234 2e32 3939 3735  93218 C 24.29975
-00004360: 352c 3230 2e36 3933 3330 3120 3234 2e30  5,20.693301 24.0
-00004370: 3039 3232 322c 3139 2e30 3336 3830 3220  09222,19.036802 
-00004380: 3233 2e32 3133 3230 342c 3137 2e36 3330  23.213204,17.630
-00004390: 3738 3120 4320 3232 2e36 3335 3238 362c  781 C 22.635286,
-000043a0: 3136 2e35 3937 3933 2032 312e 3832 3337  16.59793 21.8237
-000043b0: 3132 2c31 352e 3730 3139 3535 2032 302e  12,15.701955 20.
-000043c0: 3838 3233 3534 2c31 342e 3938 3632 3233  882354,14.986223
-000043d0: 2043 2031 392e 3935 3738 3639 2c31 342e   C 19.957869,14.
-000043e0: 3238 3537 3133 2031 382e 3837 3433 3337  285713 18.874337
-000043f0: 2c31 332e 3739 3635 3636 2031 372e 3733  ,13.796566 17.73
-00004400: 3438 3037 2c31 332e 3537 3239 3139 2043  4807,13.572919 C
-00004410: 2031 362e 3536 3035 3739 2c31 332e 3333   16.560579,13.33
-00004420: 3933 3036 2031 352e 3333 3935 3539 2c31  9306 15.339559,1
-00004430: 332e 3334 3535 3438 2031 342e 3136 3534  3.345548 14.1654
-00004440: 3431 2c31 332e 3537 3630 3737 2043 2031  41,13.576077 C 1
-00004450: 322e 3838 3230 3137 2c31 332e 3833 3634  2.882017,13.8364
-00004460: 3834 2031 312e 3637 3038 3432 2c31 342e  84 11.670842,14.
-00004470: 3432 3830 3039 2031 302e 3637 3132 3334  428009 10.671234
-00004480: 2c31 352e 3237 3131 3820 4320 392e 3433  ,15.27118 C 9.43
-00004490: 3734 3736 372c 3136 2e32 3934 3930 3420  74767,16.294904 
-000044a0: 382e 3436 3930 3838 342c 3137 2e36 3633  8.4690884,17.663
-000044b0: 3936 3420 382e 3032 3933 3535 342c 3139  964 8.0293554,19
-000044c0: 2e32 3131 3738 3820 4320 372e 3635 3331  .211788 C 7.6531
-000044d0: 3539 342c 3230 2e35 3233 3636 3320 372e  594,20.523663 7.
-000044e0: 3631 3333 3338 342c 3231 2e39 3236 3738  6133384,21.92678
-000044f0: 3220 372e 3838 3432 3335 342c 3233 2e32  2 7.8842354,23.2
-00004500: 3632 3534 3920 4320 382e 3135 3039 3431  62549 C 8.150941
-00004510: 342c 3234 2e35 3332 3236 3120 382e 3736  4,24.532261 8.76
-00004520: 3132 3837 372c 3235 2e37 3233 3732 3520  12877,25.723725 
-00004530: 392e 3632 3038 3433 372c 3236 2e36 3935  9.6208437,26.695
-00004540: 3838 3620 4320 3130 2e35 3032 3238 382c  886 C 10.502288,
-00004550: 3237 2e37 3036 3031 3220 3131 2e35 3937  27.706012 11.597
-00004560: 3430 342c 3238 2e35 3530 3338 3820 3132  404,28.550388 12
-00004570: 2e38 3534 3037 332c 3239 2e30 3339 3830  .854073,29.03980
-00004580: 3820 4320 3133 2e38 3338 3037 2c32 392e  8 C 13.83807,29.
-00004590: 3433 3331 3835 2031 342e 3930 3033 3337  433185 14.900337
-000045a0: 2c32 392e 3630 3636 3031 2031 352e 3935  ,29.606601 15.95
-000045b0: 3739 322c 3239 2e36 3035 3330 3520 7a27  792,29.605305 z'
-000045c0: 2073 7479 6c65 3d27 6669 6c6c 3a20 247a   style='fill: $z
-000045d0: 6f64 6961 635f 636f 6c6f 725f 313b 2720  odiac_color_1;' 
-000045e0: 2f3e 3c2f 7379 6d62 6f6c 3e3c 7379 6d62  /></symbol><symb
-000045f0: 6f6c 2069 643d 2767 656d 696e 6927 3e3c  ol id='gemini'><
-00004600: 7061 7468 2064 3d27 4d20 302e 3536 3534  path d='M 0.5654
-00004610: 3932 3932 2c33 3220 4320 302e 3536 3534  9292,32 C 0.5654
-00004620: 3932 3932 2c33 312e 3231 3432 3338 2030  9292,31.214238 0
-00004630: 2e35 3635 3439 3239 322c 3330 2e34 3238  .56549292,30.428
-00004640: 3436 3520 302e 3536 3534 3932 3932 2c32  465 0.56549292,2
-00004650: 392e 3634 3237 3033 2043 2032 2e39 3637  9.642703 C 2.967
-00004660: 3531 3139 2c32 392e 3031 3131 3136 2035  5119,29.011116 5
-00004670: 2e34 3032 3335 3733 2c32 382e 3438 3631  .4023573,28.4861
-00004680: 3535 2037 2e38 3639 3737 3034 2c32 382e  55 7.8697704,28.
-00004690: 3138 3837 3932 2043 2037 2e38 3639 3737  188792 C 7.86977
-000046a0: 3034 2c32 302e 3034 3838 3137 2037 2e38  04,20.048817 7.8
-000046b0: 3639 3737 3034 2c31 312e 3930 3838 3332  697704,11.908832
-000046c0: 2037 2e38 3639 3737 3034 2c33 2e37 3638   7.8697704,3.768
-000046d0: 3835 3731 2043 2035 2e33 3937 3631 3436  8571 C 5.3976146
-000046e0: 2c33 2e35 3338 3935 3731 2032 2e39 3530  ,3.5389571 2.950
-000046f0: 3036 3239 2c33 2e30 3631 3633 3931 2030  0629,3.0616391 0
-00004700: 2e35 3635 3439 3239 322c 322e 3337 3134  .56549292,2.3714
-00004710: 3130 3820 4320 302e 3536 3534 3932 3932  108 C 0.56549292
-00004720: 2c31 2e35 3830 3934 3233 2030 2e35 3635  ,1.5809423 0.565
-00004730: 3439 3239 322c 302e 3739 3034 3733 3920  49292,0.7904739 
-00004740: 302e 3536 3534 3932 3932 2c2d 3565 2d30  0.56549292,-5e-0
-00004750: 3620 4320 342e 3133 3030 3435 392c 302e  6 C 4.1300459,0.
-00004760: 3938 3039 3330 3620 372e 3831 3834 3037  9809306 7.818407
-00004770: 382c 312e 3433 3632 3532 2031 312e 3530  8,1.436252 11.50
-00004780: 3238 3033 2c31 2e36 3432 3836 3935 2043  2803,1.6428695 C
-00004790: 2031 342e 3639 3934 312c 312e 3831 3135   14.69941,1.8115
-000047a0: 3537 3420 3137 2e39 3035 3733 2c31 2e38  574 17.90573,1.8
-000047b0: 3037 3034 3832 2032 312e 3130 3136 3131  070482 21.101611
-000047c0: 2c31 2e36 3234 3037 3538 2043 2032 342e  ,1.6240758 C 24.
-000047d0: 3637 3732 3334 2c31 2e34 3038 3139 3120  677234,1.408191 
-000047e0: 3238 2e32 3534 3734 322c 302e 3935 3235  28.254742,0.9525
-000047f0: 3638 3920 3331 2e37 3134 3432 362c 2d35  689 31.714426,-5
-00004800: 652d 3036 2043 2033 312e 3731 3434 3236  e-06 C 31.714426
-00004810: 2c30 2e37 3930 3437 3339 2033 312e 3731  ,0.7904739 31.71
-00004820: 3434 3236 2c31 2e35 3830 3934 3233 2033  4426,1.5809423 3
-00004830: 312e 3731 3434 3236 2c32 2e33 3731 3431  1.714426,2.37141
-00004840: 3038 2043 2032 392e 3332 3435 3032 2c33  08 C 29.324502,3
-00004850: 2e30 3539 3334 3831 2032 362e 3837 3238  .0593481 26.8728
-00004860: 3239 2c33 2e35 3338 3636 3731 2032 342e  29,3.5386671 24.
-00004870: 3339 3630 3435 2c33 2e37 3638 3835 3731  396045,3.7688571
-00004880: 2043 2032 342e 3339 3630 3435 2c31 312e   C 24.396045,11.
-00004890: 3930 3838 3332 2032 342e 3339 3630 3435  908832 24.396045
-000048a0: 2c32 302e 3034 3838 3137 2032 342e 3339  ,20.048817 24.39
-000048b0: 3630 3435 2c32 382e 3138 3837 3932 2043  6045,28.188792 C
-000048c0: 2032 362e 3836 3830 3335 2c32 382e 3438   26.868035,28.48
-000048d0: 3637 3034 2032 392e 3330 3731 3637 2c32  6704 29.307167,2
-000048e0: 392e 3031 3331 3538 2033 312e 3731 3434  9.013158 31.7144
-000048f0: 3236 2c32 392e 3634 3237 3033 2043 2033  26,29.642703 C 3
-00004900: 312e 3731 3434 3236 2c33 302e 3432 3834  1.714426,30.4284
-00004910: 3635 2033 312e 3731 3434 3236 2c33 312e  65 31.714426,31.
-00004920: 3231 3432 3338 2033 312e 3731 3434 3236  214238 31.714426
-00004930: 2c33 3220 4320 3236 2e30 3731 3737 2c33  ,32 C 26.07177,3
-00004940: 302e 3531 3238 3636 2032 302e 3230 3634  0.512866 20.2064
-00004950: 3332 2c32 392e 3939 3339 3238 2031 342e  32,29.993928 14.
-00004960: 3338 3332 3731 2c33 302e 3132 3932 3738  383271,30.129278
-00004970: 2043 2039 2e37 3238 3135 3336 2c33 302e   C 9.7281536,30.
-00004980: 3234 3031 3936 2035 2e30 3732 3133 3439  240196 5.0721349
-00004990: 2c33 302e 3830 3837 3737 2030 2e35 3635  ,30.808777 0.565
-000049a0: 3439 3239 322c 3332 207a 204d 2031 302e  49292,32 z M 10.
-000049b0: 3730 3430 3533 2c32 382e 3031 3934 3120  704053,28.01941 
-000049c0: 4320 3132 2e39 3834 3434 382c 3237 2e37  C 12.984448,27.7
-000049d0: 3635 3336 3720 3135 2e32 3833 3232 342c  65367 15.283224,
-000049e0: 3237 2e37 3232 3738 3320 3137 2e35 3735  27.722783 17.575
-000049f0: 3533 392c 3237 2e37 3636 3830 3820 4320  539,27.766808 C 
-00004a00: 3138 2e39 3036 3838 362c 3237 2e37 3936  18.906886,27.796
-00004a10: 3931 3220 3230 2e32 3338 3134 2c32 372e  912 20.23814,27.
-00004a20: 3837 3030 3635 2032 312e 3536 3137 3632  870065 21.561762
-00004a30: 2c32 382e 3031 3934 3120 4320 3231 2e35  ,28.01941 C 21.5
-00004a40: 3631 3736 322c 3230 2e30 3031 3736 3620  61762,20.001766 
-00004a50: 3231 2e35 3631 3736 322c 3131 2e39 3834  21.561762,11.984
-00004a60: 3132 3120 3231 2e35 3631 3736 322c 332e  121 21.561762,3.
-00004a70: 3936 3634 3737 3120 4320 3139 2e31 3839  9664771 C 19.189
-00004a80: 3330 382c 342e 3132 3130 3737 3120 3136  308,4.1210771 16
-00004a90: 2e38 3130 3038 312c 342e 3133 3933 3131  .810081,4.139311
-00004aa0: 3120 3134 2e34 3333 3531 352c 342e 3130  1 14.433515,4.10
-00004ab0: 3933 3633 3120 4320 3133 2e31 3839 3532  93631 C 13.18952
-00004ac0: 362c 342e 3039 3030 3832 3120 3131 2e39  6,4.0900821 11.9
-00004ad0: 3435 3530 352c 342e 3035 3032 3034 3120  45505,4.0502041 
-00004ae0: 3130 2e37 3034 3035 332c 332e 3936 3634  10.704053,3.9664
-00004af0: 3737 3120 4320 3130 2e37 3034 3035 332c  771 C 10.704053,
-00004b00: 3131 2e39 3834 3132 3120 3130 2e37 3034  11.984121 10.704
-00004b10: 3035 332c 3230 2e30 3031 3736 3620 3130  053,20.001766 10
-00004b20: 2e37 3034 3035 332c 3238 2e30 3139 3431  .704053,28.01941
-00004b30: 207a 2027 2073 7479 6c65 3d27 6669 6c6c   z ' style='fill
-00004b40: 3a20 247a 6f64 6961 635f 636f 6c6f 725f  : $zodiac_color_
-00004b50: 323b 2720 2f3e 3c2f 7379 6d62 6f6c 3e3c  2;' /></symbol><
-00004b60: 7379 6d62 6f6c 2069 643d 2763 616e 6365  symbol id='cance
-00004b70: 7227 3e3c 7061 7468 2064 3d27 4d20 302c  r'><path d='M 0,
-00004b80: 3235 2e36 3239 3438 3220 4c20 302c 3232  25.629482 L 0,22
-00004b90: 2e39 3038 3130 3120 4320 352e 3234 3739  .908101 C 5.2479
-00004ba0: 3530 392c 3235 2e33 3034 3931 3420 3130  509,25.304914 10
-00004bb0: 2e33 3333 3436 342c 3236 2e34 3930 3833  .333464,26.49083
-00004bc0: 3720 3135 2e32 3331 3535 312c 3236 2e34  7 15.231551,26.4
-00004bd0: 3930 3833 3720 4320 3138 2e34 3432 3739  90837 C 18.44279
-00004be0: 372c 3236 2e34 3930 3833 3720 3231 2e30  7,26.490837 21.0
-00004bf0: 3534 3237 372c 3236 2e30 3738 3838 3420  54277,26.078884 
-00004c00: 3233 2e30 3635 3939 322c 3235 2e32 3432  23.065992,25.242
-00004c10: 3439 3720 4320 3231 2e37 3931 3438 392c  497 C 21.791489,
-00004c20: 3234 2e35 3933 3336 2032 302e 3832 3933  24.59336 20.8293
-00004c30: 3635 2c32 332e 3736 3934 3535 2032 302e  65,23.769455 20.
-00004c40: 3139 3231 3134 2c32 322e 3738 3332 3637  192114,22.783267
-00004c50: 2043 2031 392e 3535 3438 3633 2c32 312e   C 19.554863,21.
-00004c60: 3739 3730 3738 2031 392e 3232 3939 392c  797078 19.22999,
-00004c70: 3230 2e36 3336 3132 3220 3139 2e32 3239  20.636122 19.229
-00004c80: 3939 2c31 392e 3330 3033 3938 2043 2031  99,19.300398 C 1
-00004c90: 392e 3232 3939 392c 3137 2e35 3532 3732  9.22999,17.55272
-00004ca0: 3220 3139 2e38 3637 3234 312c 3136 2e30  2 19.867241,16.0
-00004cb0: 3534 3731 3420 3231 2e31 3239 3234 382c  54714 21.129248,
-00004cc0: 3134 2e37 3933 3839 3120 4320 3232 2e33  14.793891 C 22.3
-00004cd0: 3738 3736 2c31 332e 3534 3535 3531 2032  7876,13.545551 2
-00004ce0: 332e 3930 3331 3635 2c31 322e 3932 3133  3.903165,12.9213
-00004cf0: 3831 2032 352e 3635 3234 3831 2c31 322e  81 25.652481,12.
-00004d00: 3932 3133 3831 2043 2032 372e 3430 3137  921381 C 27.4017
-00004d10: 3938 2c31 322e 3932 3133 3831 2032 382e  98,12.921381 28.
-00004d20: 3838 3837 3138 2c31 332e 3534 3535 3531  888718,13.545551
-00004d30: 2033 302e 3133 3832 332c 3134 2e37 3831   30.13823,14.781
-00004d40: 3430 3720 4320 3331 2e33 3735 3234 362c  407 C 31.375246,
-00004d50: 3136 2e30 3239 3734 3720 3332 2e30 3030  16.029747 32.000
-00004d60: 3030 322c 3137 2e35 3135 3237 3220 3332  002,17.515272 32
-00004d70: 2e30 3030 3030 322c 3139 2e32 3735 3433  .000002,19.27543
-00004d80: 3120 4320 3332 2e30 3030 3030 322c 3232  1 C 32.000002,22
-00004d90: 2e30 3539 3233 2033 302e 3330 3036 3636  .05923 30.300666
-00004da0: 2c32 342e 3338 3131 3432 2032 362e 3838  ,24.381142 26.88
-00004db0: 3934 3938 2c32 362e 3232 3836 3835 2043  9498,26.228685 C
-00004dc0: 2032 332e 3437 3833 3331 2c32 382e 3037   23.478331,28.07
-00004dd0: 3632 3238 2031 392e 3230 352c 3239 2031  6228 19.205,29 1
-00004de0: 342e 3036 3935 3035 2c32 3920 4320 392e  4.069505,29 C 9.
-00004df0: 3632 3132 3432 392c 3239 2034 2e39 3335  6212429,29 4.935
-00004e00: 3537 3239 2c32 372e 3838 3839 3737 2030  5729,27.888977 0
-00004e10: 2c32 352e 3632 3934 3832 207a 204d 2032  ,25.629482 z M 2
-00004e20: 302e 3931 3638 3331 2c31 392e 3331 3238  0.916831,19.3128
-00004e30: 3832 2043 2032 302e 3931 3638 3331 2c32  82 C 20.916831,2
-00004e40: 302e 3538 3631 3838 2032 312e 3337 3931  0.586188 21.3791
-00004e50: 352c 3231 2e36 3834 3732 3820 3232 2e33  5,21.684728 22.3
-00004e60: 3136 3238 342c 3232 2e36 3038 3439 3920  16284,22.608499 
-00004e70: 4320 3233 2e32 3430 3932 332c 3233 2e35  C 23.240923,23.5
-00004e80: 3332 3237 3120 3234 2e33 3635 3438 342c  32271 24.365484,
-00004e90: 3233 2e39 3934 3135 3720 3235 2e36 3532  23.994157 25.652
-00004ea0: 3438 312c 3233 2e39 3934 3135 3720 4320  481,23.994157 C 
-00004eb0: 3236 2e39 3531 3937 342c 3233 2e39 3934  26.951974,23.994
-00004ec0: 3135 3720 3238 2e30 3531 3534 352c 3233  157 28.051545,23
-00004ed0: 2e35 3332 3237 3120 3238 2e39 3633 3638  .532271 28.96368
-00004ee0: 382c 3232 2e36 3435 3934 3920 4320 3239  8,22.645949 C 29
-00004ef0: 2e38 3633 3333 372c 3231 2e37 3437 3134  .863337,21.74714
-00004f00: 3520 3330 2e33 3133 3136 312c 3230 2e36  5 30.313161,20.6
-00004f10: 3438 3630 3520 3330 2e33 3133 3136 312c  48605 30.313161,
-00004f20: 3139 2e33 3530 3333 3220 4320 3330 2e33  19.350332 C 30.3
-00004f30: 3133 3136 312c 3138 2e30 3237 3039 3120  13161,18.027091 
-00004f40: 3239 2e38 3633 3333 372c 3136 2e39 3033  29.863337,16.903
-00004f50: 3538 3520 3238 2e39 3531 3139 332c 3135  585 28.951193,15
-00004f60: 2e39 3739 3831 3420 4320 3238 2e30 3339  .979814 C 28.039
-00004f70: 3034 392c 3135 2e30 3536 3034 3220 3236  049,15.056042 26
-00004f80: 2e39 3339 3437 392c 3134 2e35 3934 3135  .939479,14.59415
-00004f90: 3620 3235 2e36 3339 3938 362c 3134 2e35  6 25.639986,14.5
-00004fa0: 3934 3135 3620 4320 3234 2e33 3237 3939  94156 C 24.32799
-00004fb0: 392c 3134 2e35 3934 3135 3620 3233 2e32  9,14.594156 23.2
-00004fc0: 3135 3933 332c 3135 2e30 3536 3034 3220  15933,15.056042 
-00004fd0: 3232 2e32 3931 3239 342c 3135 2e39 3739  22.291294,15.979
-00004fe0: 3831 3420 4320 3231 2e33 3739 3135 2c31  814 C 21.37915,1
-00004ff0: 362e 3839 3131 3032 2032 302e 3931 3638  6.891102 20.9168
-00005000: 3331 2c31 382e 3030 3231 3235 2032 302e  31,18.002125 20.
-00005010: 3931 3638 3331 2c31 392e 3331 3238 3832  916831,19.312882
-00005020: 207a 204d 2033 322e 3030 3030 3032 2c37   z M 32.000002,7
-00005030: 2e33 3136 3333 3431 204c 2033 322e 3030  .3163341 L 32.00
-00005040: 3030 3032 2c31 302e 3033 3737 3135 2043  0002,10.037715 C
-00005050: 2032 362e 3733 3935 3537 2c37 2e36 3430   26.739557,7.640
-00005060: 3930 3235 2032 312e 3636 3635 3338 2c36  9025 21.666538,6
-00005070: 2e34 3432 3439 3632 2031 362e 3735 3539  .4424962 16.7559
-00005080: 3536 2c36 2e34 3432 3439 3632 2043 2031  56,6.4424962 C 1
-00005090: 332e 3535 3732 3035 2c36 2e34 3432 3439  3.557205,6.44249
-000050a0: 3632 2031 302e 3933 3332 332c 362e 3835  62 10.93323,6.85
-000050b0: 3434 3438 3320 382e 3930 3930 3230 392c  44483 8.9090209,
-000050c0: 372e 3730 3333 3139 3520 4320 3130 2e32  7.7033195 C 10.2
-000050d0: 3038 3531 332c 382e 3335 3234 3536 3320  08513,8.3524563 
-000050e0: 3131 2e31 3730 3633 372c 392e 3137 3633  11.170637,9.1763
-000050f0: 3630 3720 3131 2e37 3935 3339 332c 3130  607 11.795393,10
-00005100: 2e31 3632 3534 3920 4320 3132 2e34 3435  .162549 C 12.445
-00005110: 3134 2c31 312e 3134 3837 3338 2031 322e  14,11.148738 12.
-00005120: 3735 3735 3138 2c31 322e 3330 3936 3934  757518,12.309694
-00005130: 2031 322e 3735 3735 3138 2c31 332e 3634   12.757518,13.64
-00005140: 3534 3138 2043 2031 322e 3735 3735 3138  5418 C 12.757518
-00005150: 2c31 352e 3339 3330 3934 2031 322e 3133  ,15.393094 12.13
-00005160: 3237 3632 2c31 362e 3839 3131 3032 2031  2762,16.891102 1
-00005170: 302e 3837 3037 3535 2c31 382e 3135 3139  0.870755,18.1519
-00005180: 3235 2043 2039 2e36 3038 3734 3639 2c31  25 C 9.6087469,1
-00005190: 392e 3430 3032 3635 2038 2e30 3936 3833  9.400265 8.09683
-000051a0: 3739 2c32 302e 3032 3434 3335 2036 2e33  79,20.024435 6.3
-000051b0: 3335 3032 3539 2c32 302e 3032 3434 3335  350259,20.024435
-000051c0: 2043 2034 2e35 3835 3730 3839 2c32 302e   C 4.5857089,20.
-000051d0: 3032 3434 3335 2033 2e30 3938 3738 3939  024435 3.0987899
-000051e0: 2c31 392e 3431 3237 3439 2031 2e38 3631  ,19.412749 1.861
-000051f0: 3737 3239 2c31 382e 3136 3434 3039 2043  7729,18.164409 C
-00005200: 2030 2e36 3234 3735 362c 3136 2e39 3238   0.624756,16.928
-00005210: 3535 3220 302c 3135 2e34 3330 3534 3420  552 0,15.430544 
-00005220: 302c 3133 2e36 3832 3836 3820 4320 302c  0,13.682868 C 0,
-00005230: 3130 2e38 3836 3538 3620 312e 3639 3933  10.886586 1.6993
-00005240: 3336 342c 382e 3535 3231 3930 3720 352e  364,8.5521907 5.
-00005250: 3131 3035 3033 392c 362e 3730 3436 3437  1105039,6.704647
-00005260: 3520 4320 382e 3530 3931 3736 392c 342e  5 C 8.5091769,4.
-00005270: 3835 3731 3034 3420 3132 2e37 3935 3030  8571044 12.79500
-00005280: 332c 332e 3933 3333 3332 3720 3137 2e39  3,3.9333327 17.9
-00005290: 3330 3439 372c 332e 3933 3333 3332 3720  30497,3.9333327 
-000052a0: 4320 3232 2e33 3738 3736 2c33 2e39 3333  C 22.37876,3.933
-000052b0: 3333 3237 2032 372e 3036 3434 332c 352e  3327 27.06443,5.
-000052c0: 3035 3638 3338 3820 3332 2e30 3030 3030  0568388 32.00000
-000052d0: 322c 372e 3331 3633 3334 3120 7a20 4d20  2,7.3163341 z M 
-000052e0: 3131 2e30 3833 3137 322c 3133 2e36 3332  11.083172,13.632
-000052f0: 3933 3520 4320 3131 2e30 3833 3137 322c  935 C 11.083172,
-00005300: 3132 2e33 3437 3134 3420 3130 2e36 3230  12.347144 10.620
-00005310: 3835 322c 3131 2e32 3438 3630 3520 392e  852,11.248605 9.
-00005320: 3638 3337 3137 392c 3130 2e33 3234 3833  6837179,10.32483
-00005330: 3420 4320 382e 3734 3635 3833 392c 392e  4 C 8.7465839,9.
-00005340: 3431 3335 3435 3320 372e 3632 3230 3232  4135453 7.622022
-00005350: 392c 382e 3935 3136 3539 3520 362e 3332  9,8.9516595 6.32
-00005360: 3235 3330 392c 382e 3935 3136 3539 3520  25309,8.9516595 
-00005370: 4320 352e 3032 3330 3337 392c 382e 3935  C 5.0230379,8.95
-00005380: 3136 3539 3520 332e 3932 3334 3637 392c  16595 3.9234679,
-00005390: 392e 3430 3130 3631 3920 332e 3032 3338  9.4010619 3.0238
-000053a0: 3138 392c 3130 2e32 3939 3836 3720 4320  189,10.299867 C 
-000053b0: 322e 3132 3431 3730 392c 3131 2e31 3938  2.1241709,11.198
-000053c0: 3637 3220 312e 3637 3433 3436 312c 3132  672 1.6743461,12
-000053d0: 2e32 3937 3231 3120 312e 3637 3433 3436  .297211 1.674346
-000053e0: 312c 3133 2e35 3935 3438 3420 4320 312e  1,13.595484 C 1.
-000053f0: 3637 3433 3436 312c 3134 2e39 3138 3732  6743461,14.91872
-00005400: 3520 322e 3133 3636 3635 392c 3136 2e30  5 2.1366659,16.0
-00005410: 3432 3233 3120 332e 3034 3838 3038 392c  42231 3.0488089,
-00005420: 3136 2e39 3636 3030 3220 4320 332e 3934  16.966002 C 3.94
-00005430: 3834 3537 392c 3137 2e38 3839 3737 3420  84579,17.889774 
-00005440: 352e 3036 3035 3233 392c 3138 2e33 3531  5.0605239,18.351
-00005450: 3636 2036 2e33 3630 3031 3539 2c31 382e  66 6.3600159,18.
-00005460: 3335 3136 3620 4320 372e 3635 3935 3038  35166 C 7.659508
-00005470: 392c 3138 2e33 3531 3636 2038 2e37 3834  9,18.35166 8.784
-00005480: 3036 3839 2c31 372e 3838 3937 3734 2039  0689,17.889774 9
-00005490: 2e36 3936 3231 3239 2c31 362e 3936 3630  .6962129,16.9660
-000054a0: 3032 2043 2031 302e 3632 3038 3532 2c31  02 C 10.620852,1
-000054b0: 362e 3034 3232 3331 2031 312e 3038 3331  6.042231 11.0831
-000054c0: 3732 2c31 342e 3933 3132 3038 2031 312e  72,14.931208 11.
-000054d0: 3038 3331 3732 2c31 332e 3633 3239 3335  083172,13.632935
-000054e0: 207a 2027 2073 7479 6c65 3d27 6669 6c6c   z ' style='fill
-000054f0: 3a20 247a 6f64 6961 635f 636f 6c6f 725f  : $zodiac_color_
-00005500: 333b 2720 2f3e 3c2f 7379 6d62 6f6c 3e3c  3;' /></symbol><
-00005510: 7379 6d62 6f6c 2069 643d 276c 656f 273e  symbol id='leo'>
-00005520: 3c70 6174 6820 643d 274d 2032 382e 3032  <path d='M 28.02
-00005530: 3133 3731 2c32 392e 3438 3038 3231 2043  1371,29.480821 C
-00005540: 2032 372e 3337 3833 3339 2c33 302e 3036   27.378339,30.06
-00005550: 3939 3438 2032 362e 3638 3739 3932 2c33  9948 26.687992,3
-00005560: 302e 3631 3233 3932 2032 352e 3933 3336  0.612392 25.9336
-00005570: 3032 2c33 312e 3035 3233 3539 2043 2032  02,31.052359 C 2
-00005580: 352e 3330 3433 3934 2c33 312e 3431 3837  5.304394,31.4187
-00005590: 3031 2032 342e 3632 3734 3239 2c33 312e  01 24.627429,31.
-000055a0: 3731 3230 3931 2032 332e 3931 3530 3232  712091 23.915022
-000055b0: 2c33 312e 3837 3034 3732 2043 2032 332e  ,31.870472 C 23.
-000055c0: 3438 3738 3037 2c33 312e 3936 3620 3233  487807,31.966 23
-000055d0: 2e30 3438 3937 372c 3332 2e30 3130 3236  .048977,32.01026
-000055e0: 3220 3232 2e36 3131 3237 392c 3331 2e39  2 22.611279,31.9
-000055f0: 3937 3939 3820 4320 3231 2e39 3936 3038  97998 C 21.99608
-00005600: 352c 3331 2e39 3834 3135 3720 3231 2e33  5,31.984157 21.3
-00005610: 3830 3334 352c 3331 2e38 3737 3435 3420  80345,31.877454 
-00005620: 3230 2e38 3034 3931 312c 3331 2e36 3536  20.804911,31.656
-00005630: 3432 3620 4320 3230 2e32 3733 3435 392c  426 C 20.273459,
-00005640: 3331 2e34 3533 3739 2031 392e 3738 3034  31.45379 19.7804
-00005650: 322c 3331 2e31 3533 3930 3320 3139 2e33  2,31.153903 19.3
-00005660: 3530 3435 352c 3330 2e37 3832 3032 3820  50455,30.782028 
-00005670: 4320 3139 2e30 3135 3934 2c33 302e 3439  C 19.01594,30.49
-00005680: 3337 3639 2031 382e 3731 3830 3032 2c33  3769 18.718002,3
-00005690: 302e 3136 3237 3537 2031 382e 3436 3737  0.162757 18.4677
-000056a0: 3632 2c32 392e 3739 3838 3436 2043 2031  62,29.798846 C 1
-000056b0: 382e 3135 3837 3831 2c32 392e 3334 3936  8.158781,29.3496
-000056c0: 3333 2031 372e 3932 3937 3832 2c32 382e  33 17.929782,28.
-000056d0: 3834 3537 3339 2031 372e 3739 3437 3235  845739 17.794725
-000056e0: 2c32 382e 3331 3734 3739 2043 2031 372e  ,28.317479 C 17.
-000056f0: 3633 3539 342c 3237 2e37 3030 3837 3120  63594,27.700871 
-00005700: 3137 2e36 3031 3335 352c 3237 2e30 3536  17.601355,27.056
-00005710: 3233 3720 3137 2e36 3538 3839 362c 3236  237 17.658896,26
-00005720: 2e34 3233 3430 3220 4320 3137 2e37 3136  .423402 C 17.716
-00005730: 3438 352c 3235 2e37 3833 3837 3220 3137  485,25.783872 17
-00005740: 2e38 3438 3031 332c 3235 2e31 3533 3330  .848013,25.15330
-00005750: 3620 3138 2e30 3038 3434 392c 3234 2e35  6 18.008449,24.5
-00005760: 3332 3335 3420 4320 3138 2e32 3536 3930  32354 C 18.25690
-00005770: 352c 3233 2e35 3830 3631 3120 3138 2e35  5,23.580611 18.5
-00005780: 3737 3837 332c 3232 2e36 3439 3335 2031  77873,22.64935 1
-00005790: 382e 3932 3834 3931 2c32 312e 3733 3038  8.928491,21.7308
-000057a0: 3733 2043 2031 392e 3434 3439 3538 2c32  73 C 19.444958,2
-000057b0: 302e 3338 3337 3136 2032 302e 3033 3031  0.383716 20.0301
-000057c0: 3734 2c31 392e 3036 3339 3838 2032 302e  74,19.063988 20.
-000057d0: 3634 3439 3731 2c31 372e 3735 3931 3434  644971,17.759144
-000057e0: 2043 2032 312e 3133 3732 3035 2c31 362e   C 21.137205,16.
-000057f0: 3731 3031 3031 2032 312e 3632 3934 3337  710101 21.629437
-00005800: 2c31 352e 3636 3130 3620 3232 2e31 3231  ,15.66106 22.121
-00005810: 3636 392c 3134 2e36 3132 3031 3720 4320  669,14.612017 C 
-00005820: 3232 2e35 3633 3232 372c 3133 2e36 3635  22.563227,13.665
-00005830: 3230 3820 3232 2e39 3635 3734 332c 3132  208 22.965743,12
-00005840: 2e36 3938 3435 2032 332e 3238 3630 3532  .69845 23.286052
-00005850: 2c31 312e 3730 3334 3332 2043 2032 332e  ,11.703432 C 23.
-00005860: 3531 3430 3939 2c31 302e 3939 3037 3120  514099,10.99071 
-00005870: 3233 2e37 3031 3235 352c 3130 2e32 3632  23.701255,10.262
-00005880: 3530 3420 3233 2e38 3031 3138 312c 392e  504 23.801181,9.
-00005890: 3532 3030 3238 3620 4320 3233 2e38 3532  5200286 C 23.852
-000058a0: 3139 362c 392e 3134 3035 3734 3620 3233  196,9.1405746 23
-000058b0: 2e38 3737 3538 372c 382e 3735 3733 3931  .877587,8.757391
-000058c0: 3620 3233 2e38 3639 3331 312c 382e 3337  6 23.869311,8.37
-000058d0: 3434 3736 3620 4320 3233 2e38 3536 3839  44766 C 23.85689
-000058e0: 392c 372e 3538 3639 3331 3420 3233 2e37  9,7.5869314 23.7
-000058f0: 3530 3534 392c 362e 3739 3635 3631 3820  50549,6.7965618 
-00005900: 3233 2e35 3035 3330 312c 362e 3034 3633  23.505301,6.0463
-00005910: 3633 3520 4320 3233 2e33 3031 3035 382c  635 C 23.301058,
-00005920: 352e 3431 3836 3035 2032 322e 3939 3635  5.418605 22.9965
-00005930: 3539 2c34 2e38 3232 3436 3734 2032 322e  59,4.8224674 22.
-00005940: 3539 3734 3031 2c34 2e32 3936 3134 3231  597401,4.2961421
-00005950: 2043 2032 322e 3337 3131 3037 2c33 2e39   C 22.371107,3.9
-00005960: 3937 3138 3831 2032 322e 3131 3538 382c  971881 22.11588,
-00005970: 332e 3732 3033 3533 3220 3231 2e38 3339  3.7203532 21.839
-00005980: 3133 322c 332e 3436 3735 3333 3320 4320  132,3.4675333 C 
-00005990: 3231 2e33 3739 3338 2c33 2e30 3438 3735  21.37938,3.04875
-000059a0: 3332 2032 302e 3834 3836 312c 322e 3730  32 20.84861,2.70
-000059b0: 3832 3432 3420 3230 2e32 3735 3832 362c  82424 20.275826,
-000059c0: 322e 3436 3630 3137 3420 4320 3139 2e36  2.4660174 C 19.6
-000059d0: 3233 3230 312c 322e 3138 3834 3239 2031  23201,2.188429 1
-000059e0: 382e 3932 3133 3531 2c32 2e30 3337 3339  8.921351,2.03739
-000059f0: 3720 3138 2e32 3135 3538 2c31 2e39 3833  7 18.21558,1.983
-00005a00: 3439 3733 2043 2031 372e 3730 3839 3532  4973 C 17.708952
-00005a10: 2c31 2e39 3435 3538 3832 2031 372e 3139  ,1.9455882 17.19
-00005a20: 3836 3931 2c31 2e39 3530 3435 3832 2031  8691,1.9504582 1
-00005a30: 362e 3639 3333 3834 2c32 2e30 3034 3330  6.693384,2.00430
-00005a40: 3534 2043 2031 362e 3031 3834 3435 2c32  54 C 16.018445,2
-00005a50: 2e30 3736 3536 3038 2031 352e 3335 3038  .0765608 15.3508
-00005a60: 3238 2c32 2e32 3434 3737 3636 2031 342e  28,2.2447766 14.
-00005a70: 3733 3431 3731 2c32 2e35 3331 3330 3833  734171,2.5313083
-00005a80: 2043 2031 342e 3137 3731 3035 2c32 2e37   C 14.177105,2.7
-00005a90: 3838 3835 3720 3133 2e36 3635 3034 332c  88857 13.665043,
-00005aa0: 332e 3134 3233 3937 3520 3133 2e32 3234  3.1423975 13.224
-00005ab0: 3331 382c 332e 3536 3933 3437 3920 4320  318,3.5693479 C 
-00005ac0: 3132 2e37 3935 3533 352c 332e 3939 3531  12.795535,3.9951
-00005ad0: 3333 3320 3132 2e34 3335 3435 372c 342e  333 12.435457,4.
-00005ae0: 3439 3132 3431 3820 3132 2e31 3732 3731  4912418 12.17271
-00005af0: 392c 352e 3033 3538 3737 3320 4320 3131  9,5.0358773 C 11
-00005b00: 2e38 3930 3039 342c 352e 3631 3831 3436  .890094,5.618146
-00005b10: 3720 3131 2e37 3139 3634 322c 362e 3235  7 11.719642,6.25
-00005b20: 3133 3038 3120 3131 2e36 3433 3934 372c  13081 11.643947,
-00005b30: 362e 3839 3331 3032 3920 4320 3131 2e35  6.8931029 C 11.5
-00005b40: 3632 3031 372c 372e 3538 3434 3332 3320  62017,7.5844323 
-00005b50: 3131 2e35 3832 3832 2c38 2e32 3835 3733  11.58282,8.28573
-00005b60: 3936 2031 312e 3638 3035 3333 2c38 2e39  96 11.680533,8.9
-00005b70: 3734 3330 3336 2043 2031 312e 3830 3630  743036 C 11.8060
-00005b80: 3831 2c39 2e38 3631 3736 3036 2031 322e  81,9.8617606 12.
-00005b90: 3034 3839 3735 2c31 302e 3732 3931 3532  048975,10.729152
-00005ba0: 2031 322e 3335 3430 3333 2c31 312e 3537   12.354033,11.57
-00005bb0: 3036 3931 2043 2031 322e 3539 3837 3938  0691 C 12.598798
-00005bc0: 2c31 322e 3234 3438 3337 2031 322e 3838  ,12.244837 12.88
-00005bd0: 3534 3939 2c31 322e 3930 3331 3137 2031  5499,12.903117 1
-00005be0: 332e 3139 3833 3938 2c31 332e 3534 3832  3.198398,13.5482
-00005bf0: 3638 2043 2031 332e 3430 3939 3634 2c31  68 C 13.409964,1
-00005c00: 332e 3938 3736 3832 2031 332e 3632 3139  3.987682 13.6219
-00005c10: 3131 2c31 342e 3432 3639 3135 2031 332e  11,14.426915 13.
-00005c20: 3833 3331 3731 2c31 342e 3836 3634 3735  833171,14.866475
-00005c30: 2043 2031 342e 3138 3034 3838 2c31 352e   C 14.180488,15.
-00005c40: 3539 3620 3134 2e35 3037 3836 332c 3136  596 14.507863,16
-00005c50: 2e33 3336 3131 3620 3134 2e37 3831 3734  .336116 14.78174
-00005c60: 2c31 372e 3039 3636 3634 2043 2031 342e  ,17.096664 C 14.
-00005c70: 3935 3436 3339 2c31 372e 3538 3039 3033  954639,17.580903
-00005c80: 2031 352e 3130 3737 3431 2c31 382e 3037   15.107741,18.07
-00005c90: 3338 3938 2031 352e 3230 3436 3634 2c31  3898 15.204664,1
-00005ca0: 382e 3537 3934 3638 2043 2031 352e 3236  8.579468 C 15.26
-00005cb0: 3036 3135 2c31 382e 3837 3434 3034 2031  0615,18.874404 1
-00005cc0: 352e 3239 3539 3035 2c31 392e 3137 3434  5.295905,19.1744
-00005cd0: 3932 2031 352e 3238 3835 3031 2c31 392e  92 15.288501,19.
-00005ce0: 3437 3530 3936 2043 2031 352e 3237 3935  475096 C 15.2795
-00005cf0: 3331 2c32 302e 3132 3030 3634 2031 352e  31,20.120064 15.
-00005d00: 3136 3430 3538 2c32 302e 3736 3435 3735  164058,20.764575
-00005d10: 2031 342e 3933 3633 322c 3231 2e33 3638   14.93632,21.368
-00005d20: 3536 3320 4320 3134 2e37 3032 3536 322c  563 C 14.702562,
-00005d30: 3231 2e39 3932 3933 3820 3134 2e33 3531  21.992938 14.351
-00005d40: 3339 362c 3232 2e35 3730 3337 3720 3133  396,22.570377 13
-00005d50: 2e39 3232 3631 342c 3233 2e30 3739 3732  .922614,23.07972
-00005d60: 3920 4320 3133 2e35 3936 3136 382c 3233  9 C 13.596168,23
-00005d70: 2e34 3636 3736 3820 3133 2e32 3239 3434  .466768 13.22944
-00005d80: 352c 3233 2e38 3230 3330 3520 3132 2e38  5,23.820305 12.8
-00005d90: 3238 3031 2c32 342e 3132 3930 3036 2043  2801,24.129006 C
-00005da0: 2031 322e 3330 3034 3934 2c32 342e 3533   12.300494,24.53
-00005db0: 3436 3533 2031 312e 3730 3730 3231 2c32  4653 11.707021,2
-00005dc0: 342e 3835 3632 3737 2031 312e 3037 3433  4.856277 11.0743
-00005dd0: 352c 3235 2e30 3634 3034 3120 4320 3130  5,25.064041 C 10
-00005de0: 2e34 3238 3035 332c 3235 2e32 3737 3930  .428053,25.27790
-00005df0: 3920 392e 3734 3439 3337 352c 3235 2e33  9 9.7449375,25.3
-00005e00: 3732 3139 3320 392e 3036 3530 3339 392c  72193 9.0650399,
-00005e10: 3235 2e33 3633 3736 3720 4320 382e 3337  25.363767 C 8.37
-00005e20: 3539 3539 332c 3235 2e33 3536 3836 3920  59593,25.356869 
-00005e30: 372e 3638 3535 3031 382c 3235 2e32 3437  7.6855018,25.247
-00005e40: 3539 3120 372e 3033 3535 3831 392c 3235  591 7.0355819,25
-00005e50: 2e30 3135 3535 3720 4320 362e 3432 3232  .015557 C 6.4222
-00005e60: 3433 372c 3234 2e37 3938 3133 3820 352e  437,24.798138 5.
-00005e70: 3834 3839 3638 372c 3234 2e34 3731 3730  8489687,24.47170
-00005e80: 3620 352e 3334 3239 3131 382c 3234 2e30  6 5.3429118,24.0
-00005e90: 3633 3133 3320 4320 352e 3034 3339 3639  63133 C 5.043969
-00005ea0: 352c 3233 2e38 3232 3332 3820 342e 3736  5,23.822328 4.76
-00005eb0: 3737 3439 312c 3233 2e35 3533 3839 3820  77491,23.553898 
-00005ec0: 342e 3531 3233 3537 332c 3233 2e32 3637  4.5123573,23.267
-00005ed0: 3520 4320 342e 3037 3535 3533 312c 3232  5 C 4.0755531,22
-00005ee0: 2e37 3735 3634 3820 332e 3731 3431 3734  .775648 3.714174
-00005ef0: 322c 3232 2e32 3134 3934 3420 332e 3436  2,22.214944 3.46
-00005f00: 3136 3531 382c 3231 2e36 3036 3834 3420  16518,21.606844 
-00005f10: 4320 332e 3230 3337 3737 372c 3230 2e39  C 3.2037777,20.9
-00005f20: 3839 3935 2033 2e30 3539 3433 3738 2c32  8995 3.0594378,2
-00005f30: 302e 3332 3832 3539 2033 2e30 3135 3739  0.328259 3.01579
-00005f40: 3238 2c31 392e 3636 3138 3036 2043 2032  28,19.661806 C 2
-00005f50: 2e39 3639 3330 3138 2c31 382e 3935 3534  .9693018,18.9554
-00005f60: 3333 2033 2e30 3233 3138 3338 2c31 382e  33 3.0231838,18.
-00005f70: 3233 3933 3937 2033 2e32 3037 3731 3034  239397 3.2077104
-00005f80: 2c31 372e 3535 3437 3420 4320 332e 3337  ,17.55474 C 3.37
-00005f90: 3237 3232 352c 3136 2e39 3337 3233 3320  27225,16.937233 
-00005fa0: 332e 3634 3437 3337 332c 3136 2e33 3439  3.6447373,16.349
-00005fb0: 3139 3420 342e 3030 3431 3339 392c 3135  194 4.0041399,15
-00005fc0: 2e38 3230 3930 3120 4320 342e 3330 3237  .820901 C 4.3027
-00005fd0: 3433 2c31 352e 3337 3939 3036 2034 2e36  43,15.379906 4.6
-00005fe0: 3630 3732 3038 2c31 342e 3938 3130 3834  607208,14.981084
-00005ff0: 2035 2e30 3532 3631 3236 2c31 342e 3632   5.0526126,14.62
-00006000: 3132 3733 2043 2035 2e35 3432 3133 3939  1273 C 5.5421399
-00006010: 2c31 342e 3137 3334 3637 2036 2e31 3031  ,14.173467 6.101
-00006020: 3336 3239 2c31 332e 3739 3837 3334 2036  3629,13.798734 6
-00006030: 2e37 3132 3139 3433 2c31 332e 3533 3736  .7121943,13.5376
-00006040: 3733 2043 2037 2e33 3032 3038 3837 2c31  73 C 7.3020887,1
-00006050: 332e 3238 3339 3120 372e 3933 3638 3232  3.28391 7.936822
-00006060: 312c 3133 2e31 3338 3736 3120 382e 3537  1,13.138761 8.57
-00006070: 3731 3632 352c 3133 2e30 3937 3734 3920  71625,13.097749 
-00006080: 4320 382e 3839 3731 3538 342c 3133 2e30  C 8.8971584,13.0
-00006090: 3736 3731 3720 392e 3231 3839 3833 372c  76717 9.2189837,
-000060a0: 3133 2e30 3739 3437 3320 392e 3533 3830  13.079473 9.5380
-000060b0: 3932 332c 3133 2e31 3132 3337 3620 4320  923,13.112376 C 
-000060c0: 3130 2e30 3138 3332 352c 3133 2e31 3630  10.018325,13.160
-000060d0: 3836 3420 3130 2e34 3931 3431 352c 3133  864 10.491415,13
-000060e0: 2e32 3637 3532 2031 302e 3935 3138 3737  .26752 10.951877
-000060f0: 2c31 332e 3431 3038 3531 2043 2031 302e  ,13.410851 C 10.
-00006100: 3437 3636 3738 2c31 322e 3439 3332 3632  476678,12.493262
-00006110: 2031 302e 3035 3639 3531 2c31 312e 3534   10.056951,11.54
-00006120: 3430 3535 2039 2e37 3435 3831 3636 2c31  4055 9.7458166,1
-00006130: 302e 3535 3736 3538 2043 2039 2e34 3931  0.557658 C 9.491
-00006140: 3634 322c 392e 3734 3838 3238 3620 392e  642,9.7488286 9.
-00006150: 3331 3039 3631 392c 382e 3931 3238 3534  3109619,8.912854
-00006160: 3620 392e 3236 3232 3431 362c 382e 3036  6 9.2622416,8.06
-00006170: 3439 3732 3620 4320 392e 3233 3633 3035  49726 C 9.236305
-00006180: 2c37 2e36 3033 3133 3038 2039 2e32 3530  ,7.6031308 9.250
-00006190: 3631 372c 372e 3133 3931 3239 3720 392e  617,7.1391297 9.
-000061a0: 3330 3132 3635 392c 362e 3637 3934 3130  3012659,6.679410
-000061b0: 3720 4320 392e 3338 3632 3530 372c 352e  7 C 9.3862507,5.
-000061c0: 3931 3332 3638 3520 392e 3538 3638 3830  9132685 9.586880
-000061d0: 322c 352e 3135 3832 3033 3820 392e 3931  2,5.1582038 9.91
-000061e0: 3237 3533 372c 342e 3435 3838 3438 3720  27537,4.4588487 
-000061f0: 4320 3130 2e32 3333 3534 372c 332e 3736  C 10.233547,3.76
-00006200: 3634 3839 3620 3130 2e36 3735 3137 312c  64896 10.675171,
-00006210: 332e 3133 3235 3220 3131 2e31 3939 3734  3.13252 11.19974
-00006220: 382c 322e 3537 3933 3138 3820 4320 3131  8,2.5793188 C 11
-00006230: 2e38 3531 3530 312c 312e 3839 3237 3037  .851501,1.892707
-00006240: 3820 3132 2e36 3139 3630 342c 312e 3331  8 12.619604,1.31
-00006250: 3434 3734 3620 3133 2e34 3637 3937 352c  44746 13.467975,
-00006260: 302e 3839 3330 3336 3732 2043 2031 342e  0.89303672 C 14.
-00006270: 3233 3735 3436 2c30 2e35 3039 3130 3738  237546,0.5091078
-00006280: 3220 3135 2e30 3639 3536 372c 302e 3235  2 15.069567,0.25
-00006290: 3631 3731 3432 2031 352e 3931 3833 3931  617142 15.918391
-000062a0: 2c30 2e31 3233 3038 3639 3220 4320 3136  ,0.12308692 C 16
-000062b0: 2e37 3434 3435 392c 2d30 2e30 3037 3233  .744459,-0.00723
-000062c0: 3732 3833 3820 3137 2e35 3835 3435 322c  72838 17.585452,
-000062d0: 2d30 2e30 3236 3938 3737 3834 2031 382e  -0.026987784 18.
-000062e0: 3431 3839 3737 2c30 2e30 3239 3338 3636  418977,0.0293866
-000062f0: 3136 2043 2031 392e 3336 3932 3935 2c30  16 C 19.369295,0
-00006300: 2e30 3935 3336 3739 3136 2032 302e 3331  .095367916 20.31
-00006310: 3534 3834 2c30 2e32 3739 3538 3731 3220  5484,0.27958712 
-00006320: 3231 2e32 3036 3335 382c 302e 3632 3133  21.206358,0.6213
-00006330: 3736 3132 2043 2032 312e 3937 3132 3739  7612 C 21.971279
-00006340: 2c30 2e39 3133 3537 3930 3220 3232 2e36  ,0.91357902 22.6
-00006350: 3931 3634 332c 312e 3332 3338 3037 3520  91643,1.3238075 
-00006360: 3233 2e33 3238 3433 312c 312e 3833 3930  23.328431,1.8390
-00006370: 3835 3620 4320 3233 2e36 3231 3036 322c  856 C 23.621062,
-00006380: 322e 3037 3533 3636 3720 3233 2e38 3937  2.0753667 23.897
-00006390: 3239 312c 322e 3333 3232 3136 3820 3234  291,2.3322168 24
-000063a0: 2e31 3530 3531 332c 322e 3631 3034 3531  .150513,2.610451
-000063b0: 3220 4320 3234 2e36 3835 3335 362c 332e  2 C 24.685356,3.
-000063c0: 3139 3333 3635 3420 3235 2e31 3237 3438  1933654 25.12748
-000063d0: 372c 332e 3836 3132 3637 3420 3235 2e34  7,3.8612674 25.4
-000063e0: 3533 3139 362c 342e 3538 3233 3435 2043  53196,4.582345 C
-000063f0: 2032 352e 3831 3738 3431 2c35 2e33 3835   25.817841,5.385
-00006400: 3738 3035 2032 362e 3033 3833 3437 2c36  7805 26.038347,6
-00006410: 2e32 3530 3332 3632 2032 362e 3134 3037  .2503262 26.1407
-00006420: 3139 2c37 2e31 3235 3432 3832 2043 2032  19,7.1254282 C 2
-00006430: 362e 3230 3134 3538 2c37 2e36 3337 3231  6.201458,7.63721
-00006440: 3731 2032 362e 3232 3038 3439 2c38 2e31  71 26.220849,8.1
-00006450: 3533 3232 3736 2032 362e 3231 3234 352c  532276 26.21245,
-00006460: 382e 3636 3833 3431 3620 4320 3236 2e32  8.6683416 C 26.2
-00006470: 3031 3732 352c 392e 3430 3639 3639 3620  01725,9.4069696 
-00006480: 3236 2e31 3437 3032 332c 3130 2e31 3436  26.147023,10.146
-00006490: 3836 3120 3236 2e30 3131 3035 312c 3130  861 26.011051,10
-000064a0: 2e38 3733 3635 3120 4320 3235 2e39 3537  .873651 C 25.957
-000064b0: 3838 392c 3131 2e31 3538 3134 3220 3235  889,11.158142 25
-000064c0: 2e38 3930 3534 322c 3131 2e34 3339 3937  .890542,11.43997
-000064d0: 3220 3235 2e38 3038 3535 362c 3131 2e37  2 25.808556,11.7
-000064e0: 3137 3533 3820 4320 3235 2e36 3838 3138  17538 C 25.68818
-000064f0: 362c 3132 2e31 3337 3931 3720 3235 2e35  6,12.137917 25.5
-00006500: 3336 3936 382c 3132 2e35 3438 3639 3820  36968,12.548698 
-00006510: 3235 2e33 3739 3231 322c 3132 2e39 3536  25.379212,12.956
-00006520: 3236 3120 4320 3235 2e30 3737 3936 332c  261 C 25.077963,
-00006530: 3133 2e37 3237 3834 3720 3234 2e37 3435  13.727847 24.745
-00006540: 3736 352c 3134 2e34 3836 3930 3820 3234  765,14.486908 24
-00006550: 2e34 3035 3930 382c 3135 2e32 3432 3133  .405908,15.24213
-00006560: 3120 4320 3234 2e32 3438 3631 2c31 352e  1 C 24.24861,15.
-00006570: 3539 3138 3733 2032 342e 3038 3736 3038  591873 24.087608
-00006580: 2c31 352e 3933 3939 3236 2032 332e 3932  ,15.939926 23.92
-00006590: 3639 3539 2c31 362e 3238 3831 3334 2043  6959,16.288134 C
-000065a0: 2032 332e 3537 3339 3332 2c31 372e 3035   23.573932,17.05
-000065b0: 3838 3734 2032 332e 3232 3039 3034 2c31  8874 23.220904,1
-000065c0: 372e 3832 3936 3135 2032 322e 3836 3738  7.829615 22.8678
-000065d0: 3736 2c31 382e 3630 3033 3535 2043 2032  76,18.600355 C 2
-000065e0: 322e 3237 3838 3132 2c31 392e 3838 3030  2.278812,19.8800
-000065f0: 3539 2032 312e 3730 3632 3435 2c32 312e  59 21.706245,21.
-00006600: 3136 3739 2032 312e 3138 3230 372c 3232  1679 21.18207,22
-00006610: 2e34 3735 3733 3120 4320 3230 2e38 3735  .475731 C 20.875
-00006620: 3639 332c 3233 2e32 3434 3235 3220 3230  693,23.244252 20
-00006630: 2e35 3833 3739 362c 3234 2e30 3139 3339  .583796,24.01939
-00006640: 3620 3230 2e33 3339 3634 392c 3234 2e38  6 20.339649,24.8
-00006650: 3130 3230 3720 4320 3230 2e32 3035 3336  10207 C 20.20536
-00006660: 312c 3235 2e32 3530 3632 3720 3230 2e30  1,25.250627 20.0
-00006670: 3833 3338 392c 3235 2e36 3936 3133 3620  83389,25.696136 
-00006680: 3230 2e30 3037 3836 352c 3236 2e31 3530  20.007865,26.150
-00006690: 3832 3420 4320 3139 2e39 3730 3138 362c  824 C 19.970186,
-000066a0: 3236 2e33 3830 3434 3320 3139 2e39 3436  26.380443 19.946
-000066b0: 3532 352c 3236 2e36 3133 3232 3220 3139  525,26.613222 19
-000066c0: 2e39 3534 3233 312c 3236 2e38 3436 3134  .954231,26.84614
-000066d0: 3520 4320 3139 2e39 3633 3837 372c 3237  5 C 19.963877,27
-000066e0: 2e32 3735 3032 3620 3230 2e30 3337 3831  .275026 20.03781
-000066f0: 372c 3237 2e37 3035 3736 2032 302e 3230  7,27.70576 20.20
-00006700: 3235 3233 2c32 382e 3130 3332 3633 2043  2523,28.103263 C
-00006710: 2032 302e 3333 3535 3834 2c32 382e 3432   20.335584,28.42
-00006720: 3638 3036 2032 302e 3532 3932 3137 2c32  6806 20.529217,2
-00006730: 382e 3732 3439 3320 3230 2e37 3639 3136  8.72493 20.76916
-00006740: 382c 3238 2e39 3739 3336 3320 4320 3231  8,28.979363 C 21
-00006750: 2e30 3037 3133 312c 3239 2e32 3434 3334  .007131,29.24434
-00006760: 3820 3231 2e32 3936 3438 392c 3239 2e34  8 21.296489,29.4
-00006770: 3634 3536 3920 3231 2e36 3230 3537 382c  64569 21.620578,
-00006780: 3239 2e36 3133 3338 3420 4320 3231 2e39  29.613384 C 21.9
-00006790: 3636 3631 392c 3239 2e37 3733 3831 3320  66619,29.773813 
-000067a0: 3232 2e33 3437 3234 2c32 392e 3835 3137  22.34724,29.8517
-000067b0: 3334 2032 322e 3732 3734 332c 3239 2e38  34 22.72743,29.8
-000067c0: 3633 3733 3820 4320 3233 2e30 3931 3032  63738 C 23.09102
-000067d0: 362c 3239 2e38 3737 3635 3520 3233 2e34  6,29.877655 23.4
-000067e0: 3535 3036 2c32 392e 3832 3235 3033 2032  5506,29.822503 2
-000067f0: 332e 3830 3335 3737 2c32 392e 3732 3033  3.803577,29.7203
-00006800: 3433 2043 2032 342e 3331 3035 3333 2c32  43 C 24.310533,2
-00006810: 392e 3537 3137 3720 3234 2e37 3836 3330  9.57177 24.78630
-00006820: 332c 3239 2e33 3331 3733 3120 3235 2e32  3,29.331731 25.2
-00006830: 3332 3834 372c 3239 2e30 3532 3034 3420  32847,29.052044 
-00006840: 4320 3235 2e37 3334 3634 382c 3238 2e37  C 25.734648,28.7
-00006850: 3336 3533 3720 3236 2e32 3031 3836 372c  36537 26.201867,
-00006860: 3238 2e33 3638 3737 3920 3236 2e36 3435  28.368779 26.645
-00006870: 3535 312c 3237 2e39 3736 3434 3820 4320  551,27.976448 C 
-00006880: 3237 2e31 3034 3135 382c 3238 2e34 3737  27.104158,28.477
-00006890: 3930 3620 3237 2e35 3632 3736 352c 3238  906 27.562765,28
-000068a0: 2e39 3739 3336 3320 3238 2e30 3231 3337  .979363 28.02137
-000068b0: 312c 3239 2e34 3830 3832 3120 7a20 4d20  1,29.480821 z M 
-000068c0: 342e 3734 3930 3237 352c 3139 2e32 3036  4.7490275,19.206
-000068d0: 3736 3920 4320 342e 3734 3834 3134 322c  769 C 4.7484142,
-000068e0: 3139 2e37 3535 3035 3220 342e 3833 3336  19.755052 4.8336
-000068f0: 3534 342c 3230 2e33 3035 3837 3720 352e  544,20.305877 5.
-00006900: 3032 3435 3132 312c 3230 2e38 3230 3931  0245121,20.82091
-00006910: 2043 2035 2e32 3032 3138 3431 2c32 312e   C 5.2021841,21.
-00006920: 3330 3433 3235 2035 2e34 3732 3537 3234  304325 5.4725724
-00006930: 2c32 312e 3735 3231 3338 2035 2e38 3130  ,21.752138 5.810
-00006940: 3034 3933 2c32 322e 3134 3036 3434 2043  0493,22.140644 C
-00006950: 2036 2e30 3534 3638 3036 2c32 322e 3432   6.0546806,22.42
-00006960: 3334 3737 2036 2e33 3334 3735 3332 2c32  3477 6.3347532,2
-00006970: 322e 3637 3537 3837 2036 2e36 3431 3832  2.675787 6.64182
-00006980: 3831 2c32 322e 3838 3931 3838 2043 2037  81,22.889188 C 7
-00006990: 2e30 3430 3032 3737 2c32 332e 3136 3539  .0400277,23.1659
-000069a0: 3431 2037 2e34 3838 3730 3336 2c32 332e  41 7.4887036,23.
-000069b0: 3336 3938 3133 2037 2e39 3539 3533 3031  369813 7.9595301
-000069c0: 2c32 332e 3438 3630 3739 2043 2038 2e34  ,23.486079 C 8.4
-000069d0: 3233 3034 3734 2c32 332e 3630 3131 3531  230474,23.601151
-000069e0: 2038 2e39 3034 3939 3731 2c32 332e 3633   8.9049971,23.63
-000069f0: 3534 3837 2039 2e33 3830 3936 322c 3233  5487 9.380962,23
-00006a00: 2e36 3033 3536 3420 4320 392e 3836 3731  .603564 C 9.8671
-00006a10: 3536 392c 3233 2e35 3730 3330 3820 3130  569,23.570308 10
-00006a20: 2e33 3438 3831 322c 3233 2e34 3534 3536  .348812,23.45456
-00006a30: 3420 3130 2e37 3932 3332 322c 3233 2e32  4 10.792322,23.2
-00006a40: 3531 3335 2043 2031 312e 3235 3933 3039  5135 C 11.259309
-00006a50: 2c32 332e 3033 3930 3138 2031 312e 3638  ,23.039018 11.68
-00006a60: 3033 3533 2c32 322e 3733 3239 3031 2031  0353,22.732901 1
-00006a70: 322e 3034 3333 3736 2c32 322e 3337 3137  2.043376,22.3717
-00006a80: 3331 2043 2031 322e 3431 3537 3438 2c32  31 C 12.415748,2
-00006a90: 322e 3030 3333 3634 2031 322e 3732 3935  2.003364 12.7295
-00006aa0: 3633 2c32 312e 3537 3331 3638 2031 322e  63,21.573168 12.
-00006ab0: 3934 3931 362c 3231 2e30 3936 3734 3820  94916,21.096748 
-00006ac0: 4320 3133 2e31 3636 3133 362c 3230 2e36  C 13.166136,20.6
-00006ad0: 3239 3435 3520 3133 2e32 3930 3135 342c  29455 13.290154,
-00006ae0: 3230 2e31 3231 3231 3820 3133 2e33 3238  20.121218 13.328
-00006af0: 3036 352c 3139 2e36 3037 3938 3820 4320  065,19.607988 C 
-00006b00: 3133 2e33 3539 3131 2c31 392e 3138 3034  13.35911,19.1804
-00006b10: 3031 2031 332e 3333 3934 3434 2c31 382e  01 13.339444,18.
-00006b20: 3734 3833 3737 2031 332e 3236 3130 3833  748377 13.261083
-00006b30: 2c31 382e 3332 3636 3434 2043 2031 332e  ,18.326644 C 13.
-00006b40: 3136 3935 3333 2c31 372e 3833 3234 3339  169533,17.832439
-00006b50: 2031 322e 3939 3036 3432 2c31 372e 3335   12.990642,17.35
-00006b60: 3431 2031 322e 3733 3034 3134 2c31 362e  41 12.730414,16.
-00006b70: 3932 3338 3633 2043 2031 322e 3534 3637  923863 C 12.5467
-00006b80: 3035 2c31 362e 3631 3932 3236 2031 322e  05,16.619226 12.
-00006b90: 3332 3438 3334 2c31 362e 3333 3739 3720  324834,16.33797 
-00006ba0: 3132 2e30 3734 382c 3136 2e30 3835 3132  12.0748,16.08512
-00006bb0: 3420 4320 3131 2e37 3037 3530 312c 3135  4 C 11.707501,15
-00006bc0: 2e37 3230 3736 3520 3131 2e32 3830 3631  .720765 11.28061
-00006bd0: 352c 3135 2e34 3133 3530 3320 3130 2e38  5,15.413503 10.8
-00006be0: 3038 3130 372c 3135 2e32 3030 3734 2043  08107,15.20074 C
-00006bf0: 2031 302e 3335 3338 3633 2c31 342e 3939   10.353863,14.99
-00006c00: 3436 3135 2039 2e38 3631 3030 3737 2c31  4615 9.8610077,1
-00006c10: 342e 3837 3833 3235 2039 2e33 3633 3839  4.878325 9.36389
-00006c20: 3337 2c31 342e 3834 3439 3439 2043 2038  37,14.844949 C 8
-00006c30: 2e38 3139 3031 3138 2c31 342e 3830 3830  .8190118,14.8080
-00006c40: 3636 2038 2e32 3635 3134 3634 2c31 342e  66 8.2651464,14.
-00006c50: 3835 3835 3334 2037 2e37 3432 3936 3739  858534 7.7429679
-00006c60: 2c31 352e 3032 3236 3334 2043 2037 2e32  ,15.022634 C 7.2
-00006c70: 3830 3134 3231 2c31 352e 3136 3636 3820  801421,15.16668 
-00006c80: 362e 3834 3637 3032 382c 3135 2e34 3030  6.8467028,15.400
-00006c90: 3030 3920 362e 3436 3530 3733 372c 3135  009 6.4650737,15
-00006ca0: 2e36 3938 3231 3320 4320 362e 3035 3836  .698213 C 6.0586
-00006cb0: 3836 382c 3136 2e30 3135 3332 3920 352e  868,16.015329 5.
-00006cc0: 3730 3338 3136 322c 3136 2e33 3939 3137  7038162,16.39917
-00006cd0: 3420 352e 3432 3335 3138 352c 3136 2e38  4 5.4235185,16.8
-00006ce0: 3332 3032 3520 4320 352e 3135 3331 3438  32025 C 5.153148
-00006cf0: 392c 3137 2e32 3439 3233 3320 342e 3935  9,17.249233 4.95
-00006d00: 3932 3938 322c 3137 2e37 3135 3633 3120  92982,17.715631 
-00006d10: 342e 3835 3339 3632 392c 3138 2e32 3031  4.8539629,18.201
-00006d20: 3531 3120 4320 342e 3738 3137 3935 332c  511 C 4.7817953,
-00006d30: 3138 2e35 3331 3335 3620 342e 3734 3839  18.531356 4.7489
-00006d40: 3530 352c 3138 2e38 3639 3238 3820 342e  505,18.869288 4.
-00006d50: 3734 3930 3237 352c 3139 2e32 3036 3736  7490275,19.20676
-00006d60: 3920 7a20 2720 7374 796c 653d 2766 696c  9 z ' style='fil
-00006d70: 6c3a 2024 7a6f 6469 6163 5f63 6f6c 6f72  l: $zodiac_color
-00006d80: 5f34 3b27 202f 3e3c 2f73 796d 626f 6c3e  _4;' /></symbol>
-00006d90: 3c73 796d 626f 6c20 6964 3d27 7669 7267  <symbol id='virg
-00006da0: 6f27 3e3c 7061 7468 2064 3d27 4d20 372e  o'><path d='M 7.
-00006db0: 3136 3332 3835 352c 392e 3734 3838 3336  1632855,9.748836
-00006dc0: 3320 4320 372e 3136 3332 3835 352c 3134  3 C 7.1632855,14
-00006dd0: 2e39 3439 3836 3920 372e 3136 3332 3835  .949869 7.163285
-00006de0: 352c 3230 2e31 3530 3930 3320 372e 3136  5,20.150903 7.16
-00006df0: 3332 3835 352c 3235 2e33 3531 3933 3620  32855,25.351936 
-00006e00: 4320 362e 3333 3130 3534 352c 3235 2e33  C 6.3310545,25.3
-00006e10: 3531 3933 3620 352e 3439 3838 3233 352c  51936 5.4988235,
-00006e20: 3235 2e33 3531 3933 3620 342e 3636 3635  25.351936 4.6665
-00006e30: 3932 352c 3235 2e33 3531 3933 3620 4320  925,25.351936 C 
-00006e40: 342e 3636 3635 3932 352c 3139 2e33 3238  4.6665925,19.328
-00006e50: 3136 3420 342e 3636 3635 3932 352c 3133  164 4.6665925,13
-00006e60: 2e33 3034 3339 3220 342e 3636 3635 3932  .304392 4.666592
-00006e70: 352c 372e 3238 3036 3139 3820 4320 342e  5,7.2806198 C 4.
-00006e80: 3636 3733 3432 352c 362e 3130 3538 3236  6673425,6.105826
-00006e90: 3620 342e 3531 3337 3832 352c 342e 3932  6 4.5137825,4.92
-00006ea0: 3839 3238 3720 342e 3138 3537 3334 352c  89287 4.1857345,
-00006eb0: 332e 3739 3938 3832 2043 2033 2e38 3731  3.799882 C 3.871
-00006ec0: 3837 3935 2c32 2e37 3133 3938 3037 2033  8795,2.7139807 3
-00006ed0: 2e33 3936 3839 3635 2c31 2e36 3735 3736  .3968965,1.67576
-00006ee0: 3036 2032 2e37 3839 3431 3439 2c30 2e37  06 2.7894149,0.7
-00006ef0: 3232 3439 3534 3520 4320 322e 3733 3438  2249545 C 2.7348
-00006f00: 3030 372c 302e 3633 3434 3635 3720 322e  007,0.6344657 2.
-00006f10: 3637 3036 3235 372c 302e 3534 3236 3539  6706257,0.542659
-00006f20: 3139 2032 2e36 3139 3132 3933 2c30 2e34  19 2.6191293,0.4
-00006f30: 3538 3931 3437 2043 2033 2e34 3936 3231  589147 C 3.49621
-00006f40: 3835 2c30 2e34 3538 3931 3437 2034 2e33  85,0.4589147 4.3
-00006f50: 3733 3330 3635 2c30 2e34 3538 3931 3437  733065,0.4589147
-00006f60: 2035 2e32 3530 3339 3635 2c30 2e34 3538   5.2503965,0.458
-00006f70: 3931 3437 2043 2035 2e37 3938 3139 3635  9147 C 5.7981965
-00006f80: 2c31 2e32 3039 3936 3833 2036 2e32 3133  ,1.2099683 6.213
-00006f90: 3937 3435 2c32 2e30 3530 3935 3933 2036  9745,2.0509593 6
-00006fa0: 2e35 3237 3539 3135 2c32 2e39 3234 3030  .5275915,2.92400
-00006fb0: 3733 2043 2036 2e38 3134 3136 3735 2c33  73 C 6.8141675,3
-00006fc0: 2e37 3232 3038 3438 2037 2e30 3137 3731  .7220848 7.01771
-00006fd0: 3435 2c34 2e35 3438 3231 3433 2037 2e31  45,4.5482143 7.1
-00006fe0: 3633 3238 3535 2c35 2e33 3832 3934 3535  632855,5.3829455
-00006ff0: 2043 2037 2e36 3037 3134 3435 2c34 2e32   C 7.6071445,4.2
-00007000: 3935 3936 3133 2038 2e31 3233 3336 3735  959613 8.1233675
-00007010: 2c33 2e32 3335 3530 3632 2038 2e37 3531  ,3.2355062 8.751
-00007020: 3133 3635 2c32 2e32 3431 3834 3035 2043  1365,2.2418405 C
-00007030: 2039 2e31 3439 3339 3635 2c31 2e36 3132   9.1493965,1.612
-00007040: 3436 3031 2039 2e35 3933 3237 3735 2c31  4601 9.5932775,1
-00007050: 2e30 3130 3435 3833 2031 302e 3039 3437  .0104583 10.0947
-00007060: 3237 2c30 2e34 3538 3931 3437 2043 2031  27,0.4589147 C 1
-00007070: 302e 3931 3033 3936 2c30 2e33 3035 3934  0.910396,0.30594
-00007080: 3335 3520 3131 2e37 3236 3036 352c 302e  355 11.726065,0.
-00007090: 3135 3239 3731 3136 2031 322e 3534 3137  15297116 12.5417
-000070a0: 3334 2c34 2e34 3430 3839 3231 652d 3135  34,4.4408921e-15
-000070b0: 2043 2031 332e 3131 3534 3238 2c30 2e37   C 13.115428,0.7
-000070c0: 3337 3632 3335 3520 3133 2e35 3536 3835  3762355 13.55685
-000070d0: 382c 312e 3537 3230 3839 3320 3133 2e38  8,1.5720893 13.8
-000070e0: 3836 3132 392c 322e 3434 3436 3730 3920  86129,2.4446709 
-000070f0: 4320 3134 2e32 3731 3539 352c 332e 3436  C 14.271595,3.46
-00007100: 3630 3335 3220 3134 2e35 3039 3136 2c34  60352 14.50916,4
-00007110: 2e35 3338 3237 3435 2031 342e 3635 3135  .5382745 14.6515
-00007120: 3132 2c35 2e36 3138 3934 3932 2043 2031  12,5.6189492 C 1
-00007130: 342e 3635 3633 3833 2c35 2e36 3536 3032  4.656383,5.65602
-00007140: 3935 2031 342e 3636 3131 3431 2c35 2e36  95 14.661141,5.6
-00007150: 3933 3132 3334 2031 342e 3636 3537 3836  931234 14.665786
-00007160: 2c35 2e37 3330 3233 3233 2043 2031 352e  ,5.7302323 C 15.
-00007170: 3033 3838 3933 2c34 2e35 3534 3836 3439  038893,4.5548649
-00007180: 2031 352e 3539 3035 3731 2c33 2e34 3430   15.590571,3.440
-00007190: 3431 3931 2031 362e 3235 3831 3232 2c32  4191 16.258122,2
-000071a0: 2e34 3034 3737 3236 2043 2031 362e 3639  .4047726 C 16.69
-000071b0: 3636 3336 2c31 2e37 3234 3132 3737 2031  6636,1.7241277 1
-000071c0: 372e 3138 3530 3034 2c31 2e30 3736 3131  7.185004,1.07611
-000071d0: 3636 2031 372e 3730 3930 3139 2c30 2e34  66 17.709019,0.4
-000071e0: 3538 3931 3437 2043 2031 382e 3531 3232  589147 C 18.5122
-000071f0: 3637 2c30 2e33 3035 3934 3335 3520 3139  67,0.30594355 19
-00007200: 2e33 3135 3531 342c 302e 3135 3239 3731  .315514,0.152971
-00007210: 3136 2032 302e 3131 3837 3632 2c34 2e34  16 20.118762,4.4
-00007220: 3430 3839 3231 652d 3135 2043 2032 302e  408921e-15 C 20.
-00007230: 3732 3635 3539 2c30 2e38 3339 3435 3636  726559,0.8394566
-00007240: 3520 3231 2e32 3232 3837 362c 312e 3736  5 21.222876,1.76
-00007250: 3137 3631 3220 3231 2e35 3635 3234 352c  17612 21.565245,
-00007260: 322e 3734 3034 3135 3420 4320 3231 2e38  2.7404154 C 21.8
-00007270: 3938 3136 342c 332e 3638 3732 3033 3520  98164,3.6872035 
-00007280: 3232 2e30 3835 3035 362c 342e 3638 3336  22.085056,4.6836
-00007290: 3333 3920 3232 2e31 3331 3135 372c 352e  339 22.131157,5.
-000072a0: 3638 3536 3039 3620 4320 3232 2e31 3433  6856096 C 22.143
-000072b0: 3630 382c 352e 3932 3730 3336 2032 322e  608,5.927036 22.
-000072c0: 3134 3336 3936 2c36 2e31 3638 3738 3733  143696,6.1687873
-000072d0: 2032 322e 3134 3334 3434 2c36 2e34 3130   22.143444,6.410
-000072e0: 3435 3432 2043 2032 322e 3134 3334 3434  4542 C 22.143444
-000072f0: 2c37 2e39 3234 3238 3233 2032 322e 3134  ,7.9242823 22.14
-00007300: 3334 3434 2c39 2e34 3338 3130 3932 2032  3444,9.4381092 2
-00007310: 322e 3134 3334 3434 2c31 302e 3935 3139  2.143444,10.9519
-00007320: 3337 2043 2032 322e 3438 3133 3439 2c39  37 C 22.481349,9
-00007330: 2e39 3938 3032 3533 2032 322e 3835 3839  .9980253 22.8589
-00007340: 3932 2c39 2e30 3536 3637 3739 2032 332e  92,9.0566779 23.
-00007350: 3330 3936 3539 2c38 2e31 3439 3836 3520  309659,8.149865 
-00007360: 4320 3233 2e35 3936 3334 2c37 2e35 3735  C 23.59634,7.575
-00007370: 3334 3120 3233 2e39 3132 3332 362c 372e  341 23.912326,7.
-00007380: 3031 3339 3737 3920 3234 2e32 3739 3931  0139779 24.27991
-00007390: 372c 362e 3438 3638 3231 3420 4320 3234  7,6.4868214 C 24
-000073a0: 2e39 3637 3233 322c 362e 3233 3436 3235  .967232,6.234625
-000073b0: 3420 3235 2e36 3534 3534 382c 352e 3938  4 25.654548,5.98
-000073c0: 3234 3238 3220 3236 2e33 3431 3836 332c  24282 26.341863,
-000073d0: 352e 3733 3032 3332 3320 4320 3237 2e31  5.7302323 C 27.1
-000073e0: 3436 3434 312c 362e 3937 3036 3736 3220  46441,6.9706762 
-000073f0: 3237 2e38 3036 3735 372c 382e 3330 3830  27.806757,8.3080
-00007400: 3938 3820 3238 2e32 3632 3435 322c 392e  988 28.262452,9.
-00007410: 3731 3534 3437 3520 4320 3238 2e36 3739  7154475 C 28.679
-00007420: 3032 312c 3130 2e39 3937 3132 3820 3238  021,10.997128 28
-00007430: 2e39 3233 3031 372c 3132 2e33 3334 3632  .923017,12.33462
-00007440: 3520 3238 2e39 3833 3837 392c 3133 2e36  5 28.983879,13.6
-00007450: 3830 3739 3820 4320 3239 2e30 3439 3939  80798 C 29.04999
-00007460: 362c 3135 2e31 3531 3836 2032 382e 3931  6,15.15186 28.91
-00007470: 3337 372c 3136 2e36 3333 3937 3620 3238  377,16.633976 28
-00007480: 2e35 3536 3235 342c 3138 2e30 3633 3430  .556254,18.06340
-00007490: 3120 4320 3238 2e31 3539 3634 352c 3139  1 C 28.159645,19
-000074a0: 2e36 3534 3739 3720 3237 2e34 3931 3237  .654797 27.49127
-000074b0: 382c 3231 2e31 3735 3636 2032 362e 3630  8,21.17566 26.60
-000074c0: 3837 3436 2c32 322e 3535 3736 3439 2043  8746,22.557649 C
-000074d0: 2032 352e 3739 3635 3935 2c32 332e 3833   25.796595,23.83
-000074e0: 3136 3732 2032 342e 3831 3139 342c 3234  1672 24.81194,24
-000074f0: 2e39 3930 3533 3220 3233 2e37 3239 3035  .990532 23.72905
-00007500: 332c 3236 2e30 3432 3632 3120 4320 3233  3,26.042621 C 23
-00007510: 2e33 3736 3231 352c 3236 2e33 3835 3433  .376215,26.38543
-00007520: 3820 3233 2e30 3132 3637 382c 3236 2e37  8 23.012678,26.7
-00007530: 3137 3232 3820 3232 2e36 3430 3239 382c  17228 22.640298,
-00007540: 3237 2e30 3338 3735 3820 4320 3232 2e37  27.038758 C 22.7
-00007550: 3330 3930 362c 3237 2e37 3033 3232 3920  30906,27.703229 
-00007560: 3232 2e39 3436 3831 312c 3238 2e33 3435  22.946811,28.345
-00007570: 3238 2032 332e 3232 3537 3831 2c32 382e  28 23.225781,28.
-00007580: 3935 3333 3534 2043 2032 332e 3537 3330  953354 C 23.5730
-00007590: 392c 3239 2e37 3037 3536 3120 3234 2e30  9,29.707561 24.0
-000075a0: 3136 3639 312c 3330 2e34 3133 3939 3820  16691,30.413998 
-000075b0: 3234 2e35 3033 3631 392c 3331 2e30 3835  24.503619,31.085
-000075c0: 3438 3620 4320 3234 2e37 3330 3231 392c  486 C 24.730219,
-000075d0: 3331 2e33 3937 3430 3720 3234 2e39 3637  31.397407 24.967
-000075e0: 3035 392c 3331 2e37 3031 3834 3820 3235  059,31.701848 25
-000075f0: 2e32 3131 3531 392c 3331 2e39 3939 3939  .211519,31.99999
-00007600: 3820 4320 3234 2e32 3334 3337 322c 3331  8 C 24.234372,31
-00007610: 2e39 3939 3939 3820 3233 2e32 3537 3232  .999998 23.25722
-00007620: 362c 3331 2e39 3939 3939 3820 3232 2e32  6,31.999998 22.2
-00007630: 3830 3037 392c 3331 2e39 3939 3939 3820  80079,31.999998 
-00007640: 4320 3231 2e38 3135 3731 362c 3331 2e34  C 21.815716,31.4
-00007650: 3133 3231 3820 3231 2e34 3332 3336 382c  13218 21.432368,
-00007660: 3330 2e37 3636 3331 3720 3231 2e31 3030  30.766317 21.100
-00007670: 3334 352c 3330 2e30 3937 3037 3120 4320  345,30.097071 C 
-00007680: 3230 2e38 3333 3734 362c 3239 2e35 3538  20.833746,29.558
-00007690: 3435 3520 3230 2e36 3030 3735 362c 3239  455 20.600756,29
-000076a0: 2e30 3033 3637 3320 3230 2e33 3932 3033  .003673 20.39203
-000076b0: 322c 3238 2e34 3430 3330 3820 4320 3139  2,28.440308 C 19
-000076c0: 2e33 3936 3432 322c 3239 2e30 3034 3633  .396422,29.00463
-000076d0: 3820 3138 2e33 3233 3339 312c 3239 2e34  8 18.323391,29.4
-000076e0: 3233 3832 3920 3137 2e32 3234 3739 322c  23829 17.224792,
-000076f0: 3239 2e37 3430 3132 3320 4320 3136 2e33  29.740123 C 16.3
-00007700: 3834 3937 312c 3239 2e39 3831 3630 3820  84971,29.981608 
-00007710: 3135 2e35 3238 3631 2c33 302e 3136 3333  15.52861,30.1633
-00007720: 3835 2031 342e 3636 3537 3836 2c33 302e  85 14.665786,30.
-00007730: 3330 3037 3733 2043 2031 342e 3636 3537  300773 C 14.6657
-00007740: 3836 2c32 392e 3538 3936 3632 2031 342e  86,29.589662 14.
-00007750: 3636 3537 3836 2c32 382e 3837 3835 3531  665786,28.878551
-00007760: 2031 342e 3636 3537 3836 2c32 382e 3136   14.665786,28.16
-00007770: 3734 3420 4320 3135 2e38 3132 3530 322c  744 C 15.812502,
-00007780: 3237 2e39 3333 3838 3120 3136 2e39 3436  27.933881 16.946
-00007790: 3630 312c 3237 2e36 3235 3432 3620 3138  601,27.625426 18
-000077a0: 2e30 3336 3536 392c 3237 2e31 3937 3233  .036569,27.19723
-000077b0: 3120 4320 3138 2e36 3831 3438 332c 3236  1 C 18.681483,26
-000077c0: 2e39 3433 3335 3920 3139 2e33 3130 3436  .943359 19.31046
-000077d0: 322c 3236 2e36 3436 3738 3320 3139 2e39  2,26.646783 19.9
-000077e0: 3037 3539 392c 3236 2e32 3934 3537 3220  07599,26.294572 
-000077f0: 4320 3139 2e37 3330 3733 372c 3235 2e31  C 19.730737,25.1
-00007800: 3939 3631 2031 392e 3634 3332 3332 2c32  9961 19.643232,2
-00007810: 342e 3039 3032 3920 3139 2e36 3436 3735  4.09029 19.64675
-00007820: 312c 3232 2e39 3831 3137 3420 4320 3139  1,22.981174 C 19
-00007830: 2e36 3436 3734 2c31 372e 3934 3838 3737  .64674,17.948877
-00007840: 2031 392e 3634 3637 3732 2c31 322e 3931   19.646772,12.91
-00007850: 3635 3738 2031 392e 3634 3637 3335 2c37  6578 19.646735,7
-00007860: 2e38 3834 3238 3131 2043 2031 392e 3634  .8842811 C 19.64
-00007870: 3439 3531 2c36 2e39 3530 3230 3234 2031  4951,6.9502024 1
-00007880: 392e 3539 3730 3236 2c36 2e30 3134 3132  9.597026,6.01412
-00007890: 3820 3139 2e34 3535 3637 372c 352e 3038  8 19.455677,5.08
-000078a0: 3939 3936 3620 4320 3139 2e33 3438 3532  99966 C 19.34852
-000078b0: 322c 342e 3339 3832 3537 3120 3139 2e31  2,4.3982571 19.1
-000078c0: 3838 3935 362c 332e 3731 3132 3437 2031  88956,3.711247 1
-000078d0: 382e 3933 3039 3234 2c33 2e30 3539 3039  8.930924,3.05909
-000078e0: 3537 2043 2031 382e 3833 3030 3736 2c32  57 C 18.830076,2
-000078f0: 2e38 3035 3039 3531 2031 382e 3731 3337  .8050951 18.7137
-00007900: 3938 2c32 2e35 3536 3937 3335 2031 382e  98,2.5569735 18.
-00007910: 3537 3835 3134 2c32 2e33 3139 3337 3938  578514,2.3193798
-00007920: 2043 2031 372e 3733 3839 3737 2c33 2e32   C 17.738977,3.2
-00007930: 3232 3435 3639 2031 372e 3034 3739 3539  224569 17.047959
-00007940: 2c34 2e32 3535 3833 3438 2031 362e 3437  ,4.2558348 16.47
-00007950: 3937 3036 2c35 2e33 3437 3539 3431 2043  9706,5.3475941 C
-00007960: 2031 352e 3832 3434 3239 2c36 2e36 3037   15.824429,6.607
-00007970: 3438 3734 2031 352e 3332 3736 3437 2c37  4874 15.327647,7
-00007980: 2e39 3434 3737 3937 2031 342e 3933 3733  .9447797 14.9373
-00007990: 3633 2c39 2e33 3038 3431 3837 2043 2031  63,9.3084187 C 1
-000079a0: 342e 3834 3034 3939 2c39 2e36 3438 3438  4.840499,9.64848
-000079b0: 3332 2031 342e 3734 3930 3439 2c39 2e39  32 14.749049,9.9
-000079c0: 3930 3239 3433 2031 342e 3636 3537 3836  902943 14.665786
-000079d0: 2c31 302e 3333 3338 3420 4320 3134 2e36  ,10.33384 C 14.6
-000079e0: 3635 3738 362c 3135 2e33 3339 3837 3220  65786,15.339872 
-000079f0: 3134 2e36 3635 3738 362c 3230 2e33 3435  14.665786,20.345
-00007a00: 3930 3420 3134 2e36 3635 3738 362c 3235  904 14.665786,25
-00007a10: 2e33 3531 3933 3620 4320 3133 2e38 3239  .351936 C 13.829
-00007a20: 3431 352c 3235 2e33 3531 3933 3620 3132  415,25.351936 12
-00007a30: 2e39 3933 3034 332c 3235 2e33 3531 3933  .993043,25.35193
-00007a40: 3620 3132 2e31 3536 3637 322c 3235 2e33  6 12.156672,25.3
-00007a50: 3531 3933 3620 4320 3132 2e31 3536 3636  51936 C 12.15666
-00007a60: 312c 3139 2e38 3038 3130 3420 3132 2e31  1,19.808104 12.1
-00007a70: 3536 3639 342c 3134 2e32 3634 3237 3220  56694,14.264272 
-00007a80: 3132 2e31 3536 3635 352c 382e 3732 3034  12.156655,8.7204
-00007a90: 3339 3820 4320 3132 2e31 3534 3836 362c  398 C 12.154866,
-00007aa0: 372e 3639 3539 3633 3620 3132 2e31 3136  7.6959636 12.116
-00007ab0: 3036 352c 362e 3637 3031 3234 3320 3131  065,6.6701243 11
-00007ac0: 2e39 3937 3532 332c 352e 3635 3139 3831  .997523,5.651981
-00007ad0: 3120 4320 3131 2e39 3136 3136 312c 342e  1 C 11.916161,4.
-00007ae0: 3936 3635 3236 3320 3131 2e37 3939 3935  9665263 11.79995
-00007af0: 382c 342e 3238 3330 3339 3820 3131 2e36  8,4.2830398 11.6
-00007b00: 3036 3631 312c 332e 3631 3935 3133 3620  06611,3.6195136 
-00007b10: 4320 3131 2e34 3733 3634 332c 332e 3136  C 11.473643,3.16
-00007b20: 3834 3839 3820 3131 2e33 3035 3033 382c  84898 11.305038,
-00007b30: 322e 3732 3434 3638 3720 3131 2e30 3633  2.7244687 11.063
-00007b40: 3539 322c 322e 3331 3933 3739 3820 4320  592,2.3193798 C 
-00007b50: 3130 2e31 3031 3430 342c 332e 3433 3830  10.101404,3.4380
-00007b60: 3639 3920 392e 3239 3231 3830 352c 342e  699 9.2921805,4.
-00007b70: 3638 3432 3633 3920 382e 3633 3137 3037  6842639 8.631707
-00007b80: 352c 362e 3030 3232 2043 2038 2e30 3239  5,6.0022 C 8.029
-00007b90: 3230 3435 2c37 2e32 3033 3034 3333 2037  2045,7.2030433 7
-00007ba0: 2e35 3437 3631 3135 2c38 2e34 3632 3337  .5476115,8.46237
-00007bb0: 3232 2037 2e31 3633 3238 3535 2c39 2e37  22 7.1632855,9.7
-00007bc0: 3438 3833 3633 207a 204d 2032 322e 3134  488363 z M 22.14
-00007bd0: 3334 3434 2c32 342e 3730 3639 3735 2043  3444,24.706975 C
-00007be0: 2032 332e 3037 3632 3131 2c32 332e 3736   23.076211,23.76
-00007bf0: 3034 3732 2032 332e 3930 3938 3539 2c32  0472 23.909859,2
-00007c00: 322e 3731 3236 3134 2032 342e 3538 3736  2.712614 24.5876
-00007c10: 3138 2c32 312e 3536 3838 3338 2043 2032  18,21.568838 C 2
-00007c20: 342e 3931 3437 3731 2c32 312e 3031 3636  4.914771,21.0166
-00007c30: 3533 2032 352e 3230 3638 3531 2c32 302e  53 25.206851,20.
-00007c40: 3434 3334 3239 2032 352e 3435 3631 3839  443429 25.456189
-00007c50: 2c31 392e 3835 3230 3438 2043 2032 352e  ,19.852048 C 25.
-00007c60: 3932 3934 3839 2c31 382e 3731 3735 3934  929489,18.717594
-00007c70: 2032 362e 3234 3438 3137 2c31 372e 3531   26.244817,17.51
-00007c80: 3830 3936 2032 362e 3339 3531 3533 2c31  8096 26.395153,1
-00007c90: 362e 3239 3834 3736 2043 2032 362e 3439  6.298476 C 26.49
-00007ca0: 3134 3932 2c31 352e 3531 3639 3731 2032  1492,15.516971 2
-00007cb0: 362e 3532 3336 3033 2c31 342e 3732 3735  6.523603,14.7275
-00007cc0: 3031 2032 362e 3439 3039 3032 2c31 332e  01 26.490902,13.
-00007cd0: 3934 3037 3735 2043 2032 362e 3434 3039  940775 C 26.4409
-00007ce0: 3936 2c31 322e 3735 3631 3539 2032 362e  96,12.756159 26.
-00007cf0: 3233 3132 3237 2c31 312e 3537 3838 3032  231227,11.578802
-00007d00: 2032 352e 3837 3237 3933 2c31 302e 3434   25.872793,10.44
-00007d10: 3835 3720 4320 3235 2e36 3836 3038 362c  857 C 25.686086,
-00007d20: 392e 3835 3833 3838 3320 3235 2e34 3539  9.8583883 25.459
-00007d30: 3830 342c 392e 3238 3038 3434 3120 3235  804,9.2808441 25
-00007d40: 2e31 3939 3039 382c 382e 3731 3933 3739  .199098,8.719379
-00007d50: 3420 4320 3234 2e35 3034 3233 322c 392e  4 C 24.504232,9.
-00007d60: 3537 3333 3936 2032 332e 3933 3331 3236  573396 23.933126
-00007d70: 2c31 302e 3532 3230 3939 2032 332e 3434  ,10.522099 23.44
-00007d80: 3839 3931 2c31 312e 3530 3839 3134 2043  8991,11.508914 C
-00007d90: 2032 322e 3932 3632 3839 2c31 322e 3537   22.926289,12.57
-00007da0: 3632 3435 2032 322e 3530 3332 3737 2c31  6245 22.503277,1
-00007db0: 332e 3638 3939 3537 2032 322e 3134 3334  3.689957 22.1434
-00007dc0: 3434 2c31 342e 3832 3137 3034 2043 2032  44,14.821704 C 2
-00007dd0: 322e 3134 3334 3434 2c31 382e 3131 3637  2.143444,18.1167
-00007de0: 3935 2032 322e 3134 3334 3434 2c32 312e  95 22.143444,21.
-00007df0: 3431 3138 3834 2032 322e 3134 3334 3434  411884 22.143444
-00007e00: 2c32 342e 3730 3639 3735 207a 2027 2073  ,24.706975 z ' s
-00007e10: 7479 6c65 3d27 6669 6c6c 3a20 247a 6f64  tyle='fill: $zod
-00007e20: 6961 635f 636f 6c6f 725f 353b 2720 2f3e  iac_color_5;' />
-00007e30: 3c2f 7379 6d62 6f6c 3e3c 7379 6d62 6f6c  </symbol><symbol
-00007e40: 2069 643d 276c 6962 7261 273e 3c70 6174   id='libra'><pat
-00007e50: 6820 643d 274d 202d 352e 3539 3632 3565  h d='M -5.59625e
-00007e60: 2d30 362c 3239 2e31 3930 3730 3920 4320  -06,29.190709 C 
-00007e70: 2d35 2e35 3936 3235 652d 3036 2c32 382e  -5.59625e-06,28.
-00007e80: 3230 3337 3232 202d 352e 3539 3632 3565  203722 -5.59625e
-00007e90: 2d30 362c 3237 2e32 3136 3733 3520 2d35  -06,27.216735 -5
-00007ea0: 2e35 3936 3235 652d 3036 2c32 362e 3232  .59625e-06,26.22
-00007eb0: 3937 3335 2043 2031 302e 3636 3636 3637  9735 C 10.666667
-00007ec0: 2c32 362e 3232 3937 3335 2032 312e 3333  ,26.229735 21.33
-00007ed0: 3333 3237 2c32 362e 3232 3937 3335 2033  3327,26.229735 3
-00007ee0: 322c 3236 2e32 3239 3733 3520 4320 3332  2,26.229735 C 32
-00007ef0: 2c32 372e 3231 3637 3335 2033 322c 3238  ,27.216735 32,28
-00007f00: 2e32 3033 3732 3220 3332 2c32 392e 3139  .203722 32,29.19
-00007f10: 3037 3039 2043 2032 312e 3333 3333 3237  0709 C 21.333327
-00007f20: 2c32 392e 3139 3037 3039 2031 302e 3636  ,29.190709 10.66
-00007f30: 3636 3637 2c32 392e 3139 3037 3039 202d  6667,29.190709 -
-00007f40: 352e 3539 3632 3565 2d30 362c 3239 2e31  5.59625e-06,29.1
-00007f50: 3930 3730 3920 7a20 4d20 3132 2e36 3438  90709 z M 12.648
-00007f60: 3735 2c31 372e 3530 3936 3120 4320 3132  75,17.50961 C 12
-00007f70: 2e36 3438 3735 2c31 382e 3433 3234 3436  .64875,18.432446
-00007f80: 2031 322e 3634 3837 352c 3139 2e33 3535   12.64875,19.355
-00007f90: 3238 3320 3132 2e36 3438 3735 2c32 302e  283 12.64875,20.
-00007fa0: 3237 3831 3333 2043 2038 2e34 3332 3530  278133 C 8.43250
-00007fb0: 3233 2c32 302e 3237 3831 3333 2034 2e32  23,20.278133 4.2
-00007fc0: 3136 3234 3138 2c32 302e 3237 3831 3333  162418,20.278133
-00007fd0: 202d 352e 3539 3632 3565 2d30 362c 3230   -5.59625e-06,20
-00007fe0: 2e32 3738 3133 3320 4320 2d35 2e35 3936  .278133 C -5.596
-00007ff0: 3235 652d 3036 2c31 392e 3238 3631 3736  25e-06,19.286176
-00008000: 202d 352e 3539 3632 3565 2d30 362c 3138   -5.59625e-06,18
-00008010: 2e32 3934 3233 3120 2d35 2e35 3936 3235  .294231 -5.59625
-00008020: 652d 3036 2c31 372e 3330 3232 3836 2043  e-06,17.302286 C
-00008030: 2032 2e39 3535 3831 372c 3137 2e33 3032   2.955817,17.302
-00008040: 3238 3620 352e 3931 3136 3339 362c 3137  286 5.9116396,17
-00008050: 2e33 3032 3238 3620 382e 3836 3734 3632  .302286 8.867462
-00008060: 332c 3137 2e33 3032 3238 3620 4320 372e  3,17.302286 C 7.
-00008070: 3833 3330 3031 392c 3136 2e32 3538 3331  8330019,16.25831
-00008080: 3920 372e 3031 3231 3234 372c 3134 2e39  9 7.0121247,14.9
-00008090: 3730 3432 3620 362e 3636 3235 3137 312c  70426 6.6625171,
-000080a0: 3133 2e35 3333 3630 3820 4320 362e 3336  13.533608 C 6.36
-000080b0: 3531 3036 342c 3132 2e33 3335 3737 3220  51064,12.335772 
-000080c0: 362e 3339 3933 3832 392c 3131 2e30 3733  6.3993829,11.073
-000080d0: 3533 3820 362e 3633 3933 3833 372c 392e  538 6.6393837,9.
-000080e0: 3836 3930 3339 3520 4320 362e 3934 3531  8690395 C 6.9451
-000080f0: 3039 352c 382e 3335 3537 3631 3620 372e  095,8.3557616 7.
-00008100: 3639 3233 3839 392c 362e 3934 3834 3239  6923899,6.948429
-00008110: 3320 382e 3731 3739 3837 392c 352e 3739  3 8.7179879,5.79
-00008120: 3839 3230 3320 4320 392e 3837 3234 3638  89203 C 9.872468
-00008130: 332c 342e 3439 3232 3736 3220 3131 2e33  3,4.4922762 11.3
-00008140: 3435 3434 372c 332e 3433 3933 3935 3720  45447,3.4393957 
-00008150: 3133 2e30 3136 3635 352c 322e 3930 3733  13.016655,2.9073
-00008160: 3932 3720 4320 3134 2e35 3139 3930 392c  927 C 14.519909,
-00008170: 322e 3432 3531 3631 3320 3136 2e31 3430  2.4251613 16.140
-00008180: 3038 312c 322e 3333 3737 3834 3520 3137  081,2.3377845 17
-00008190: 2e36 3935 3237 312c 322e 3538 3934 3636  .695271,2.589466
-000081a0: 3120 4320 3139 2e32 3636 3433 392c 322e  1 C 19.266439,2.
-000081b0: 3834 3532 3732 3620 3230 2e37 3536 3131  8452726 20.75611
-000081c0: 332c 332e 3533 3637 3532 3820 3231 2e39  3,3.5367528 21.9
-000081d0: 3836 3133 322c 342e 3534 3234 3737 3220  86132,4.5424772 
-000081e0: 4320 3233 2e32 3836 3939 382c 352e 3630  C 23.286998,5.60
-000081f0: 3232 3431 3220 3234 2e33 3835 3638 342c  22412 24.385684,
-00008200: 362e 3935 3135 3133 3220 3234 2e39 3836  6.9515132 24.986
-00008210: 3230 312c 382e 3532 3838 3838 3720 4320  201,8.5288887 C 
-00008220: 3235 2e34 3633 3036 322c 392e 3737 3236  25.463062,9.7726
-00008230: 3537 3920 3235 2e36 3430 3132 372c 3131  579 25.640127,11
-00008240: 2e31 3236 3339 3420 3235 2e35 3333 3535  .126394 25.53355
-00008250: 372c 3132 2e34 3532 3136 3620 4320 3235  7,12.452166 C 25
-00008260: 2e34 3136 3637 382c 3133 2e38 3230 3334  .416678,13.82034
-00008270: 3420 3234 2e38 3738 3932 372c 3135 2e31  4 24.878927,15.1
-00008280: 3335 3930 3220 3234 2e30 3631 3435 322c  35902 24.061452,
-00008290: 3136 2e32 3334 3835 3820 4320 3233 2e37  16.234858 C 23.7
-000082a0: 3833 3630 332c 3136 2e36 3132 3531 3120  83603,16.612511 
-000082b0: 3233 2e34 3736 3131 382c 3136 2e39 3638  23.476118,16.968
-000082c0: 3035 3620 3233 2e31 3437 3335 2c31 372e  056 23.14735,17.
-000082d0: 3330 3233 3133 2043 2032 362e 3039 3832  302313 C 26.0982
-000082e0: 3333 2c31 372e 3330 3233 2032 392e 3034  33,17.3023 29.04
-000082f0: 3931 3136 2c31 372e 3330 3233 2033 322c  9116,17.3023 32,
-00008300: 3137 2e33 3032 3238 3620 4320 3332 2c31  17.302286 C 32,1
-00008310: 382e 3239 3432 3331 2033 322c 3139 2e32  8.294231 32,19.2
-00008320: 3836 3137 3620 3332 2c32 302e 3237 3831  86176 32,20.2781
-00008330: 3333 2043 2032 372e 3738 3337 3339 2c32  33 C 27.783739,2
-00008340: 302e 3237 3831 3333 2032 332e 3536 3734  0.278133 23.5674
-00008350: 3932 2c32 302e 3237 3831 3333 2031 392e  92,20.278133 19.
-00008360: 3335 3132 3434 2c32 302e 3237 3831 3333  351244,20.278133
-00008370: 2043 2031 392e 3335 3132 3434 2c31 392e   C 19.351244,19.
-00008380: 3335 3532 3833 2031 392e 3335 3132 3434  355283 19.351244
-00008390: 2c31 382e 3433 3234 3436 2031 392e 3335  ,18.432446 19.35
-000083a0: 3132 3434 2c31 372e 3530 3936 3120 4320  1244,17.50961 C 
-000083b0: 3230 2e34 3736 3437 392c 3136 2e37 3837  20.476479,16.787
-000083c0: 3139 3920 3231 2e34 3639 3834 362c 3135  199 21.469846,15
-000083d0: 2e38 3033 3431 3320 3232 2e30 3238 3135  .803413 22.02815
-000083e0: 2c31 342e 3537 3533 3337 2043 2032 322e  ,14.575337 C 22.
-000083f0: 3538 3436 3033 2c31 332e 3336 3239 3420  584603,13.36294 
-00008400: 3232 2e37 3036 3839 2c31 312e 3937 3432  22.70689,11.9742
-00008410: 3820 3232 2e34 3639 3237 342c 3130 2e36  8 22.469274,10.6
-00008420: 3638 3937 3620 4320 3232 2e32 3339 3735  68976 C 22.23975
-00008430: 322c 392e 3431 3736 3037 3620 3231 2e35  2,9.4176076 21.5
-00008440: 3734 3631 382c 382e 3237 3133 3737 3620  74618,8.2713776 
-00008450: 3230 2e36 3731 3435 312c 372e 3338 3332  20.671451,7.3832
-00008460: 3730 3320 4320 3139 2e37 3531 3536 332c  703 C 19.751563,
-00008470: 362e 3435 3234 3035 2031 382e 3536 3136  6.452405 18.5616
-00008480: 322c 352e 3737 3138 3638 2031 372e 3236  2,5.771868 17.26
-00008490: 3539 3431 2c35 2e35 3430 3936 3639 2043  5941,5.5409669 C
-000084a0: 2031 352e 3732 3832 3431 2c35 2e32 3634   15.728241,5.264
-000084b0: 3430 3620 3134 2e30 3735 3338 332c 352e  406 14.075383,5.
-000084c0: 3438 3634 3139 3820 3132 2e37 3235 3337  4864198 12.72537
-000084d0: 2c36 2e32 3935 3336 3120 4320 3131 2e38  ,6.295361 C 11.8
-000084e0: 3233 3533 332c 362e 3833 3536 3030 3720  23533,6.8356007 
-000084f0: 3131 2e30 3439 3837 342c 372e 3538 3438  11.049874,7.5848
-00008500: 3535 2031 302e 3435 3835 3435 2c38 2e34  55 10.458545,8.4
-00008510: 3531 3537 3033 2043 2039 2e37 3533 3339  515703 C 9.75339
-00008520: 3937 2c39 2e34 3837 3431 3739 2039 2e34  97,9.4874179 9.4
-00008530: 3037 3734 3131 2c31 302e 3734 3637 3839  077411,10.746789
-00008540: 2039 2e34 3331 3339 3539 2c31 312e 3939   9.4313959,11.99
-00008550: 3533 3437 2043 2039 2e34 3336 3637 3432  5347 C 9.4366742
-00008560: 2c31 332e 3139 3838 3720 392e 3736 3931  ,13.19887 9.7691
-00008570: 3330 342c 3134 2e34 3039 3734 3420 3130  304,14.409744 10
-00008580: 2e34 3437 3032 342c 3135 2e34 3130 3937  .447024,15.41097
-00008590: 3920 4320 3131 2e30 3134 3231 352c 3136  9 C 11.014215,16
-000085a0: 2e32 3632 3435 3720 3131 2e37 3932 3736  .262457 11.79276
-000085b0: 322c 3136 2e39 3536 3535 3320 3132 2e36  2,16.956553 12.6
-000085c0: 3438 3735 2c31 372e 3530 3936 3120 7a20  4875,17.50961 z 
-000085d0: 2720 7374 796c 653d 2766 696c 6c3a 2024  ' style='fill: $
-000085e0: 7a6f 6469 6163 5f63 6f6c 6f72 5f36 3b27  zodiac_color_6;'
-000085f0: 202f 3e3c 2f73 796d 626f 6c3e 3c73 796d   /></symbol><sym
-00008600: 626f 6c20 6964 3d27 7363 6f72 7069 6f27  bol id='scorpio'
-00008610: 3e3c 7061 7468 2064 3d27 4d20 322e 3037  ><path d='M 2.07
-00008620: 3137 3735 2c32 352e 3130 3933 3932 2043  1775,25.109392 C
-00008630: 2032 2e30 3731 3735 3432 2c31 392e 3234   2.0717542,19.24
-00008640: 3333 3932 2032 2e30 3731 3831 3636 2c31  3392 2.0718166,1
-00008650: 332e 3337 3733 3932 2032 2e30 3731 3734  3.377392 2.07174
-00008660: 3332 2c37 2e35 3131 3339 3231 2043 2032  32,7.5113921 C 2
-00008670: 2e30 3639 3234 3735 2c36 2e33 3433 3232  .0692475,6.34322
-00008680: 3635 2031 2e39 3538 3339 3937 2c35 2e31  65 1.9583997,5.1
-00008690: 3730 3639 3232 2031 2e36 3737 3136 3231  706922 1.6771621
-000086a0: 2c34 2e30 3335 3236 3236 2043 2031 2e34  ,4.0352626 C 1.4
-000086b0: 3337 3331 3936 2c33 2e30 3636 3235 3735  373196,3.0662575
-000086c0: 2031 2e30 3638 3539 342c 322e 3132 3531   1.068594,2.1251
-000086d0: 3433 3520 302e 3534 3533 3830 3438 2c31  435 0.54538048,1
-000086e0: 2e32 3733 3639 3731 2043 2030 2e33 3739  .2736971 C 0.379
-000086f0: 3537 3230 382c 312e 3030 3335 3036 3220  57208,1.0035062 
-00008700: 302e 3139 3836 3634 3538 2c30 2e37 3432  0.19866458,0.742
-00008710: 3539 3420 302e 3030 3332 3339 3337 3634  594 0.0032393764
-00008720: 2c30 2e34 3933 3036 3531 2043 2030 2e38  ,0.4930651 C 0.8
-00008730: 3834 3530 3839 382c 302e 3439 3330 3635  8450898,0.493065
-00008740: 3120 312e 3736 3537 3738 362c 302e 3439  1 1.7657786,0.49
-00008750: 3330 3635 3120 322e 3634 3730 3438 332c  30651 2.6470483,
-00008760: 302e 3439 3330 3635 3120 4320 332e 3233  0.4930651 C 3.23
-00008770: 3430 3533 332c 312e 3338 3934 3933 3120  40533,1.3894931 
-00008780: 332e 3639 3833 3332 332c 322e 3336 3531  3.6983323,2.3651
-00008790: 3930 3120 342e 3033 3536 3237 332c 332e  901 4.0356273,3.
-000087a0: 3338 3233 3432 3420 4320 342e 3234 3739  3823424 C 4.2479
-000087b0: 3631 332c 342e 3032 3130 3337 3320 342e  613,4.0210373 4.
-000087c0: 3431 3134 3831 332c 342e 3637 3536 3636  4114813,4.675666
-000087d0: 2034 2e35 3331 3938 3633 2c35 2e33 3337   4.5319863,5.337
-000087e0: 3833 3320 4320 352e 3034 3835 3139 332c  833 C 5.0485193,
-000087f0: 342e 3036 3031 3937 3820 352e 3638 3436  4.0601978 5.6846
-00008800: 3439 332c 322e 3832 3638 3338 3920 362e  493,2.8268389 6.
-00008810: 3437 3637 3137 332c 312e 3639 3739 3635  4767173,1.697965
-00008820: 2043 2036 2e37 3639 3933 3933 2c31 2e32   C 6.7699393,1.2
-00008830: 3830 3130 3639 2037 2e30 3834 3336 3333  801069 7.0843633
-00008840: 2c30 2e38 3737 3036 3838 2037 2e34 3230  ,0.8770688 7.420
-00008850: 3539 3233 2c30 2e34 3933 3036 3531 2043  5923,0.4930651 C
-00008860: 2038 2e32 3132 3130 3333 2c30 2e33 3333   8.2121033,0.333
-00008870: 3631 3731 2039 2e30 3033 3631 3333 2c30  6171 9.0036133,0
-00008880: 2e31 3734 3136 3920 392e 3739 3531 3234  .174169 9.795124
-00008890: 332c 302e 3031 3437 3231 3030 3320 4320  3,0.014721003 C 
-000088a0: 3130 2e33 3231 382c 302e 3632 3930 3538  10.3218,0.629058
-000088b0: 3420 3130 2e37 3237 3937 2c31 2e33 3430  4 10.72797,1.340
-000088c0: 3030 3035 2031 312e 3033 3737 3134 2c32  0005 11.037714,2
-000088d0: 2e30 3836 3135 3835 2043 2031 312e 3430  .0861585 C 11.40
-000088e0: 3133 3538 2c32 2e39 3632 3932 3533 2031  1358,2.9629253 1
-000088f0: 312e 3633 3830 3339 2c33 2e38 3838 3030  1.638039,3.88800
-00008900: 3132 2031 312e 3739 3831 3235 2c34 2e38  12 11.798125,4.8
-00008910: 3232 3339 3520 4320 3131 2e38 3431 3937  22395 C 11.84197
-00008920: 322c 352e 3037 3931 3736 3320 3131 2e38  2,5.0791763 11.8
-00008930: 3739 3838 372c 352e 3333 3639 3635 3820  79887,5.3369658 
-00008940: 3131 2e39 3132 3631 392c 352e 3539 3534  11.912619,5.5954
-00008950: 3032 3920 4320 3132 2e33 3430 3832 312c  029 C 12.340821,
-00008960: 342e 3336 3032 3339 3820 3132 2e39 3530  4.3602398 12.950
-00008970: 3534 2c33 2e31 3932 3936 3732 2031 332e  54,3.1929672 13.
-00008980: 3637 3435 3433 2c32 2e31 3036 3930 3032  674543,2.1069002
-00008990: 2043 2031 342e 3034 3635 342c 312e 3534   C 14.04654,1.54
-000089a0: 3837 3337 3620 3134 2e34 3438 3931 372c  87376 14.448917,
-000089b0: 312e 3031 3131 3337 3620 3134 2e38 3734  1.0111376 14.874
-000089c0: 3636 342c 302e 3439 3330 3635 3120 4320  664,0.4930651 C 
-000089d0: 3135 2e36 3832 3439 352c 302e 3333 3336  15.682495,0.3336
-000089e0: 3137 3120 3136 2e34 3930 3332 352c 302e  171 16.490325,0.
-000089f0: 3137 3431 3639 2031 372e 3239 3831 3536  174169 17.298156
-00008a00: 2c30 2e30 3134 3732 3130 3033 2043 2031  ,0.014721003 C 1
-00008a10: 372e 3838 3131 3037 2c30 2e38 3032 3836  7.881107,0.80286
-00008a20: 3239 2031 382e 3334 3634 3732 2c31 2e36  29 18.346472,1.6
-00008a30: 3738 3333 3537 2031 382e 3637 3039 332c  783357 18.67093,
-00008a40: 322e 3630 3430 3237 3420 4320 3139 2e30  2.6040274 C 19.0
-00008a50: 3237 3534 2c33 2e36 3136 3336 3535 2031  2754,3.6163655 1
-00008a60: 392e 3231 3632 3338 2c34 2e36 3834 3131  9.216238,4.68411
-00008a70: 3536 2031 392e 3236 3633 3639 2c35 2e37  56 19.266369,5.7
-00008a80: 3535 3238 3838 2043 2031 392e 3238 3030  552888 C 19.2800
-00008a90: 342c 362e 3032 3231 3532 3120 3139 2e32  4,6.0221521 19.2
-00008aa0: 3831 3434 342c 362e 3238 3933 3737 3320  81444,6.2893773 
-00008ab0: 3139 2e32 3831 3031 322c 362e 3535 3635  19.281012,6.5565
-00008ac0: 3233 3920 4320 3139 2e32 3831 3032 392c  239 C 19.281029,
-00008ad0: 3131 2e36 3237 3038 3120 3139 2e32 3830  11.627081 19.280
-00008ae0: 3937 392c 3136 2e36 3937 3633 3920 3139  979,16.697639 19
-00008af0: 2e32 3831 3033 382c 3231 2e37 3638 3139  .281038,21.76819
-00008b00: 3720 4320 3139 2e32 3832 3337 372c 3232  7 C 19.282377,22
-00008b10: 2e34 3835 3734 3820 3139 2e32 3932 3639  .485748 19.29269
-00008b20: 392c 3233 2e32 3033 3633 3920 3139 2e33  9,23.203639 19.3
-00008b30: 3334 3033 332c 3233 2e39 3230 3132 3520  34033,23.920125 
-00008b40: 4320 3139 2e33 3534 3239 372c 3234 2e32  C 19.354297,24.2
-00008b50: 3439 3633 3320 3139 2e33 3738 3833 312c  49633 19.378831,
-00008b60: 3234 2e35 3739 3432 3820 3139 2e34 3238  24.579428 19.428
-00008b70: 3832 362c 3234 2e39 3035 3934 3320 4320  826,24.905943 C 
-00008b80: 3139 2e34 3434 3439 312c 3235 2e30 3132  19.444491,25.012
-00008b90: 3035 3520 3139 2e34 3732 3237 382c 3235  055 19.472278,25
-00008ba0: 2e31 3135 3931 3420 3139 2e35 3030 3934  .115914 19.50094
-00008bb0: 372c 3235 2e32 3139 3132 2043 2031 392e  7,25.21912 C 19.
-00008bc0: 3539 3938 3834 2c32 352e 3536 3639 3236  599884,25.566926
-00008bd0: 2031 392e 3735 3736 3135 2c32 352e 3839   19.757615,25.89
-00008be0: 3834 3138 2031 392e 3937 3035 322c 3236  8418 19.97052,26
-00008bf0: 2e31 3930 3736 3120 4320 3230 2e30 3533  .190761 C 20.053
-00008c00: 3338 312c 3236 2e33 3034 3030 3220 3230  381,26.304002 20
-00008c10: 2e31 3432 3036 392c 3236 2e34 3133 3339  .142069,26.41339
-00008c20: 3120 3230 2e32 3430 3432 372c 3236 2e35  1 20.240427,26.5
-00008c30: 3133 3533 3220 4320 3230 2e35 3337 3733  13532 C 20.53773
-00008c40: 312c 3236 2e38 3133 3733 3820 3230 2e39  1,26.813738 20.9
-00008c50: 3036 3739 312c 3237 2e30 3335 3139 3920  06791,27.035199 
-00008c60: 3231 2e32 3937 3533 332c 3237 2e31 3930  21.297533,27.190
-00008c70: 3635 2043 2032 312e 3738 3337 3237 2c32  65 C 21.783727,2
-00008c80: 372e 3338 3339 3937 2032 322e 3330 3231  7.383997 22.3021
-00008c90: 3231 2c32 372e 3438 3336 3832 2032 322e  21,27.483682 22.
-00008ca0: 3832 3132 3436 2c32 372e 3533 3432 3632  821246,27.534262
-00008cb0: 2043 2032 332e 3134 3630 3232 2c32 372e   C 23.146022,27.
-00008cc0: 3536 3630 3039 2032 332e 3437 3234 3735  566009 23.472475
-00008cd0: 2c32 372e 3537 3630 3038 2032 332e 3739  ,27.576008 23.79
-00008ce0: 3836 3732 2c32 372e 3537 3437 3034 2043  8672,27.574704 C
-00008cf0: 2032 342e 3237 3135 3631 2c32 372e 3537   24.271561,27.57
-00008d00: 3437 3034 2032 342e 3734 3434 3532 2c32  4704 24.744452,2
-00008d10: 372e 3537 3437 3034 2032 352e 3231 3733  7.574704 25.2173
-00008d20: 3432 2c32 372e 3537 3437 3034 2043 2032  42,27.574704 C 2
-00008d30: 352e 3231 3733 3432 2c32 362e 3735 3239  5.217342,26.7529
-00008d40: 3333 2032 352e 3231 3733 3432 2c32 352e  33 25.217342,25.
-00008d50: 3933 3131 3633 2032 352e 3231 3733 3432  931163 25.217342
-00008d60: 2c32 352e 3130 3933 3932 2043 2032 362e  ,25.109392 C 26.
-00008d70: 3531 3437 3637 2c32 362e 3238 3237 3636  514767,26.282766
-00008d80: 2032 372e 3831 3231 3932 2c32 372e 3435   27.812192,27.45
-00008d90: 3631 3420 3239 2e31 3039 3631 372c 3238  614 29.109617,28
-00008da0: 2e36 3239 3531 3420 4320 3237 2e38 3132  .629514 C 27.812
-00008db0: 3139 322c 3239 2e37 3537 3931 3620 3236  192,29.757916 26
-00008dc0: 2e35 3134 3736 372c 3330 2e38 3836 3331  .514767,30.88631
-00008dd0: 3720 3235 2e32 3137 3334 322c 3332 2e30  7 25.217342,32.0
-00008de0: 3134 3731 3920 4320 3235 2e32 3137 3334  14719 C 25.21734
-00008df0: 322c 3331 2e32 3137 3437 3920 3235 2e32  2,31.217479 25.2
-00008e00: 3137 3334 322c 3330 2e34 3230 3233 3920  17342,30.420239 
-00008e10: 3235 2e32 3137 3334 322c 3239 2e36 3232  25.217342,29.622
-00008e20: 3939 3820 4320 3234 2e34 3439 3833 392c  998 C 24.449839,
-00008e30: 3239 2e36 3232 3933 3120 3233 2e36 3832  29.622931 23.682
-00008e40: 3333 342c 3239 2e36 3233 3133 3420 3232  334,29.623134 22
-00008e50: 2e39 3134 3833 2c32 392e 3632 3238 3935  .91483,29.622895
-00008e60: 2043 2032 322e 3137 3532 3437 2c32 392e   C 22.175247,29.
-00008e70: 3631 3932 3832 2032 312e 3433 3138 3839  619282 21.431889
-00008e80: 2c32 392e 3535 3133 3520 3230 2e37 3134  ,29.55135 20.714
-00008e90: 3535 342c 3239 2e33 3634 3732 3820 4320  554,29.364728 C 
-00008ea0: 3230 2e31 3234 3739 342c 3239 2e32 3131  20.124794,29.211
-00008eb0: 3038 3320 3139 2e35 3532 3433 322c 3238  083 19.552432,28
-00008ec0: 2e39 3732 3039 3320 3139 2e30 3531 3930  .972093 19.05190
-00008ed0: 372c 3238 2e36 3230 3637 3620 4320 3138  7,28.620676 C 18
-00008ee0: 2e36 3837 3535 312c 3238 2e33 3636 3235  .687551,28.36625
-00008ef0: 3720 3138 2e33 3635 3534 332c 3238 2e30  7 18.365543,28.0
-00008f00: 3531 3733 3620 3138 2e31 3030 3938 392c  51736 18.100989,
-00008f10: 3237 2e36 3934 3338 3420 4320 3137 2e37  27.694384 C 17.7
-00008f20: 3235 3331 382c 3237 2e31 3839 3436 3620  25318,27.189466 
-00008f30: 3137 2e34 3630 3135 2c32 362e 3630 3934  17.46015,26.6094
-00008f40: 3520 3137 2e32 3732 3731 342c 3236 2e30  5 17.272714,26.0
-00008f50: 3130 3334 3820 4320 3137 2e30 3433 3832  10348 C 17.04382
-00008f60: 362c 3235 2e32 3736 3236 3620 3136 2e39  6,25.276266 16.9
-00008f70: 3235 3432 382c 3234 2e35 3131 3820 3136  25428,24.5118 16
-00008f80: 2e38 3636 3138 352c 3233 2e37 3436 3336  .866185,23.74636
-00008f90: 3420 4320 3136 2e38 3331 3231 312c 3233  4 C 16.831211,23
-00008fa0: 2e32 3935 3431 3420 3136 2e38 3139 3437  .295414 16.81947
-00008fb0: 392c 3232 2e38 3433 2031 362e 3832 3038  9,22.843 16.8208
-00008fc0: 3031 2c32 322e 3339 3037 3835 2043 2031  01,22.390785 C 1
-00008fd0: 362e 3832 3037 392c 3137 2e34 3733 3530  6.82079,17.47350
-00008fe0: 3320 3136 2e38 3230 3832 332c 3132 2e35  3 16.820823,12.5
-00008ff0: 3536 3232 3120 3136 2e38 3230 3738 352c  56221 16.820785,
-00009000: 372e 3633 3839 3338 3220 4320 3136 2e38  7.6389382 C 16.8
-00009010: 3138 3939 362c 362e 3736 3232 3139 3220  18996,6.7622192 
-00009020: 3136 2e37 3737 3539 332c 352e 3838 3336  16.777593,5.8836
-00009030: 3539 3220 3136 2e36 3530 3937 372c 352e  592 16.650977,5.
-00009040: 3031 3534 3532 3320 4320 3136 2e35 3539  0154523 C 16.559
-00009050: 3437 2c34 2e33 3938 3333 3139 2031 362e  47,4.3983319 16.
-00009060: 3432 3534 3434 2c33 2e37 3834 3431 3237  425444,3.7844127
-00009070: 2031 362e 3230 3339 3433 2c33 2e32 3030   16.203943,3.200
-00009080: 3130 3331 2043 2031 362e 3038 3139 3936  1031 C 16.081996
-00009090: 2c32 2e38 3830 3232 3038 2031 352e 3933  ,2.8802208 15.93
-000090a0: 3236 3332 2c32 2e35 3639 3632 3039 2031  2632,2.5696209 1
-000090b0: 352e 3734 3336 3934 2c32 2e32 3833 3738  5.743694,2.28378
-000090c0: 3934 2043 2031 342e 3831 3533 3135 2c33  94 C 14.815315,3
-000090d0: 2e33 3535 3439 3520 3134 2e30 3338 3538  .355495 14.03858
-000090e0: 392c 342e 3535 3633 3131 3820 3133 2e34  9,4.5563118 13.4
-000090f0: 3230 3839 362c 352e 3833 3236 3436 3920  20896,5.8326469 
-00009100: 4320 3132 2e37 3431 3233 392c 372e 3233  C 12.741239,7.23
-00009110: 3438 3437 3820 3132 2e32 3530 3232 342c  48478 12.250224,
-00009120: 382e 3732 3436 3633 2031 312e 3931 3236  8.724663 11.9126
-00009130: 3139 2c31 302e 3234 3439 3838 2043 2031  19,10.244988 C 1
-00009140: 312e 3931 3236 3139 2c31 352e 3139 3937  1.912619,15.1997
-00009150: 3920 3131 2e39 3132 3631 392c 3230 2e31  9 11.912619,20.1
-00009160: 3534 3539 2031 312e 3931 3236 3139 2c32  5459 11.912619,2
-00009170: 352e 3130 3933 3932 2043 2031 312e 3039  5.109392 C 11.09
-00009180: 3235 3439 2c32 352e 3130 3933 3932 2031  2549,25.109392 1
-00009190: 302e 3237 3234 3738 2c32 352e 3130 3933  0.272478,25.1093
-000091a0: 3932 2039 2e34 3532 3430 3833 2c32 352e  92 9.4524083,25.
-000091b0: 3130 3933 3932 2043 2039 2e34 3532 3339  109392 C 9.45239
-000091c0: 3733 2c31 392e 3537 3433 3139 2039 2e34  73,19.574319 9.4
-000091d0: 3532 3433 3033 2c31 342e 3033 3932 3436  524303,14.039246
-000091e0: 2039 2e34 3532 3339 3233 2c38 2e35 3034   9.4523923,8.504
-000091f0: 3137 3333 2043 2039 2e34 3530 3631 3433  1733 C 9.4506143
-00009200: 2c37 2e35 3034 3430 3832 2039 2e34 3133  ,7.5044082 9.413
-00009210: 3031 3433 2c36 2e35 3033 3231 3138 2039  0143,6.5032118 9
-00009220: 2e32 3935 3636 3933 2c35 2e35 3039 3832  .2956693,5.50982
-00009230: 3936 2043 2039 2e32 3134 3735 3233 2c34  96 C 9.2147523,4
-00009240: 2e38 3338 3232 3720 392e 3039 3836 3034  .838227 9.098604
-00009250: 332c 342e 3136 3835 3638 3520 382e 3930  3,4.1685685 8.90
-00009260: 3337 3838 332c 332e 3531 3939 3831 3620  37883,3.5199816 
-00009270: 4320 382e 3737 3334 3332 332c 332e 3039  C 8.7734323,3.09
-00009280: 3035 3038 3320 382e 3630 3830 3337 332c  05083 8.6080373,
-00009290: 322e 3636 3836 3337 2038 2e33 3735 3330  2.668637 8.37530
-000092a0: 3133 2c32 2e32 3833 3738 3934 2043 2037  13,2.2837894 C 7
-000092b0: 2e34 3333 3534 3433 2c33 2e33 3434 3337  .4335443,3.34437
-000092c0: 3920 362e 3634 3430 3430 332c 342e 3533  9 6.6440403,4.53
-000092d0: 3639 3239 3120 362e 3030 3634 3830 332c  69291 6.0064803,
-000092e0: 352e 3830 3336 3933 3620 4320 352e 3338  5.8036936 C 5.38
-000092f0: 3135 3438 332c 372e 3034 3431 3430 3620  15483,7.0441406 
-00009300: 342e 3839 3837 3035 332c 382e 3335 3338  4.8987053,8.3538
-00009310: 3931 2034 2e35 3331 3938 3633 2c39 2e36  91 4.5319863,9.6
-00009320: 3933 3035 3233 2043 2034 2e35 3331 3938  930523 C 4.53198
-00009330: 3633 2c31 342e 3833 3138 3333 2034 2e35  63,14.831833 4.5
-00009340: 3331 3938 3633 2c31 392e 3937 3036 3132  319863,19.970612
-00009350: 2034 2e35 3331 3938 3633 2c32 352e 3130   4.5319863,25.10
-00009360: 3933 3932 2043 2033 2e37 3131 3931 3533  9392 C 3.7119153
-00009370: 2c32 352e 3130 3933 3932 2032 2e38 3931  ,25.109392 2.891
-00009380: 3834 3534 2c32 352e 3130 3933 3932 2032  8454,25.109392 2
-00009390: 2e30 3731 3737 352c 3235 2e31 3039 3339  .071775,25.10939
-000093a0: 3220 7a27 2073 7479 6c65 3d27 6669 6c6c  2 z' style='fill
-000093b0: 3a20 247a 6f64 6961 635f 636f 6c6f 725f  : $zodiac_color_
-000093c0: 373b 2720 2f3e 3c2f 7379 6d62 6f6c 3e3c  7;' /></symbol><
-000093d0: 7379 6d62 6f6c 2069 643d 2773 6167 6974  symbol id='sagit
-000093e0: 7461 7269 7573 273e 3c70 6174 6820 643d  tarius'><path d=
-000093f0: 274d 2032 392e 3839 3239 3432 2c32 2e30  'M 29.892942,2.0
-00009400: 3935 3837 3036 204c 2033 322c 3137 2e31  958706 L 32,17.1
-00009410: 3136 3237 3620 4c20 3238 2e39 3938 3537  16276 L 28.99857
-00009420: 392c 3137 2e35 3837 3038 3820 4c20 3237  9,17.587088 L 27
-00009430: 2e34 3532 3339 332c 362e 3633 3639 3233  .452393,6.636923
-00009440: 3520 4c20 3133 2e37 3333 3737 362c 3230  5 L 13.733776,20
-00009450: 2e34 3131 3935 3720 4c20 3230 2e31 3931  .411957 L 20.191
-00009460: 3337 392c 3236 2e38 3636 3633 204c 2031  379,26.86663 L 1
-00009470: 382e 3033 3838 3435 2c32 392e 3032 3332  8.038845,29.0232
-00009480: 3531 204c 2031 312e 3538 3132 3432 2c32  51 L 11.581242,2
-00009490: 322e 3535 3333 3920 4c20 322e 3039 3139  2.55339 L 2.0919
-000094a0: 3031 2c33 312e 3939 3939 3935 204c 2031  01,31.999995 L 1
-000094b0: 2e35 652d 3036 2c32 392e 3930 3431 3234  .5e-06,29.904124
-000094c0: 204c 2039 2e34 3734 3138 342c 3230 2e34   L 9.474184,20.4
-000094d0: 3432 3333 3220 4c20 332e 3033 3137 342c  42332 L 3.03174,
-000094e0: 3133 2e39 3732 3437 204c 2035 2e31 3533  13.97247 L 5.153
-000094f0: 3935 372c 3131 2e38 3135 3835 204c 2031  957,11.81585 L 1
-00009500: 312e 3631 3135 362c 3138 2e32 3835 3731  1.61156,18.28571
-00009510: 3120 4c20 3235 2e33 3630 3439 332c 342e  1 L 25.360493,4.
-00009520: 3534 3130 3532 3920 4c20 3134 2e34 3331  5410529 L 14.431
-00009530: 3037 362c 332e 3030 3731 3138 3620 4c20  076,3.0071186 L 
-00009540: 3134 2e39 3030 3939 362c 2d34 2e34 3430  14.900996,-4.440
-00009550: 3839 3231 652d 3136 204c 2032 392e 3839  8921e-16 L 29.89
-00009560: 3239 3432 2c32 2e30 3935 3837 3036 207a  2942,2.0958706 z
-00009570: 2027 2073 7479 6c65 3d27 6669 6c6c 3a20   ' style='fill: 
-00009580: 247a 6f64 6961 635f 636f 6c6f 725f 383b  $zodiac_color_8;
-00009590: 2720 2f3e 3c2f 7379 6d62 6f6c 3e3c 7379  ' /></symbol><sy
-000095a0: 6d62 6f6c 2069 643d 2763 6170 7269 636f  mbol id='caprico
-000095b0: 726e 273e 3c70 6174 6820 643d 274d 2036  rn'><path d='M 6
-000095c0: 2e31 3039 3335 3539 2c31 382e 3930 3437  .1093559,18.9047
-000095d0: 3734 2043 2036 2e31 3039 3233 3932 2c31  74 C 6.1092392,1
-000095e0: 382e 3538 3935 3520 362e 3130 3936 3034  8.58955 6.109604
-000095f0: 322c 3138 2e32 3734 3332 3520 362e 3130  2,18.274325 6.10
-00009600: 3931 3437 332c 3137 2e39 3539 3130 3320  91473,17.959103 
-00009610: 4320 362e 3130 3336 3338 392c 3137 2e31  C 6.1036389,17.1
-00009620: 3436 3233 3420 362e 3033 3634 3538 372c  46234 6.0364587,
-00009630: 3136 2e33 3335 3036 3520 352e 3934 3633  16.335065 5.9463
-00009640: 3936 382c 3135 2e35 3237 3631 3120 4320  968,15.527611 C 
-00009650: 352e 3830 3230 3139 332c 3134 2e32 3534  5.8020193,14.254
-00009660: 3634 3220 352e 3539 3630 3934 332c 3132  642 5.5960943,12
-00009670: 2e39 3839 3436 3520 352e 3336 3635 3331  .989465 5.366531
-00009680: 332c 3131 2e37 3239 3333 3820 4320 352e  3,11.729338 C 5.
-00009690: 3232 3538 3630 342c 3130 2e39 3536 3932  2258604,10.95692
-000096a0: 3720 352e 3037 3034 342c 3130 2e31 3837  7 5.07044,10.187
-000096b0: 3232 2034 2e39 3033 3535 372c 392e 3432  22 4.903557,9.42
-000096c0: 3030 3534 3720 4320 342e 3732 3138 3032  00547 C 4.721802
-000096d0: 372c 382e 3539 3331 3035 3220 342e 3532  7,8.5931052 4.52
-000096e0: 3632 3338 392c 372e 3736 3834 3930 3720  62389,7.7684907 
-000096f0: 342e 3238 3533 3333 362c 362e 3935 3635  4.2853336,6.9565
-00009700: 3234 3720 4320 342e 3135 3332 3033 362c  247 C 4.1532036,
-00009710: 362e 3531 3639 3535 3420 342e 3030 3939  6.5169554 4.0099
-00009720: 3133 392c 362e 3037 3935 3320 332e 3832  139,6.07953 3.82
-00009730: 3531 3333 342c 352e 3635 3838 3835 3620  51334,5.6588856 
-00009740: 4320 332e 3635 3839 3233 342c 352e 3238  C 3.6589234,5.28
-00009750: 3336 3135 3120 332e 3434 3732 3136 382c  36151 3.4472168,
-00009760: 342e 3932 3639 3532 3920 332e 3138 3433  4.9269529 3.1843
-00009770: 3439 392c 342e 3631 3130 3838 3820 4320  499,4.6110888 C 
-00009780: 322e 3930 3039 3230 392c 342e 3237 3030  2.9009209,4.2700
-00009790: 3932 3920 322e 3535 3134 3532 382c 332e  929 2.5514528,3.
-000097a0: 3938 3230 3031 3120 322e 3135 3436 3835  9820011 2.154685
-000097b0: 312c 332e 3738 3233 3634 3120 4320 312e  1,3.7823641 C 1.
-000097c0: 3732 3732 3834 362c 332e 3536 3532 3236  7272846,3.565226
-000097d0: 3120 312e 3235 3139 3834 372c 332e 3435  1 1.2519847,3.45
-000097e0: 3235 3731 3720 302e 3737 3439 3834 3738  25717 0.77498478
-000097f0: 2c33 2e34 3232 3034 3836 2043 2030 2e35  ,3.4220486 C 0.5
-00009800: 3837 3031 3637 372c 332e 3430 3839 3730  8701677,3.408970
-00009810: 3620 302e 3339 3835 3936 3735 2c33 2e34  6 0.39859675,3.4
-00009820: 3132 3937 3238 2030 2e32 3130 3334 3139  129728 0.2103419
-00009830: 2c33 2e34 3132 3239 3520 4320 302e 3134  ,3.412295 C 0.14
-00009840: 3032 3033 3931 2c33 2e34 3132 3239 3520  020391,3.412295 
-00009850: 302e 3037 3030 3634 3638 332c 332e 3431  0.070064683,3.41
-00009860: 3232 3935 202d 372e 3333 3032 3737 652d  2295 -7.330277e-
-00009870: 3035 2c33 2e34 3132 3239 3520 4320 2d37  05,3.412295 C -7
-00009880: 2e33 3330 3237 3765 2d30 352c 322e 3732  .330277e-05,2.72
-00009890: 3935 3333 3520 2d37 2e33 3330 3237 3765  95335 -7.330277e
-000098a0: 2d30 352c 322e 3034 3637 3732 202d 372e  -05,2.046772 -7.
-000098b0: 3333 3032 3737 652d 3035 2c31 2e33 3634  330277e-05,1.364
-000098c0: 3031 3036 2043 2030 2e36 3237 3633 3435  0106 C 0.6276345
-000098d0: 342c 312e 3336 3430 3331 3720 312e 3235  4,1.3640317 1.25
-000098e0: 3533 3432 342c 312e 3336 3339 3639 3620  53424,1.3639696 
-000098f0: 312e 3838 3330 3530 322c 312e 3336 3430  1.8830502,1.3640
-00009900: 3431 3620 4320 322e 3434 3934 3434 2c31  416 C 2.449444,1
-00009910: 2e33 3635 3835 3135 2033 2e30 3231 3039  .3658515 3.02109
-00009920: 392c 312e 3433 3931 3135 3620 332e 3535  9,1.4391156 3.55
-00009930: 3530 3131 2c31 2e36 3334 3332 3935 2043  5011,1.6343295 C
-00009940: 2033 2e39 3833 3636 3934 2c31 2e37 3930   3.9836694,1.790
-00009950: 3130 3731 2034 2e33 3833 3238 3639 2c32  1071 4.3832869,2
-00009960: 2e30 3239 3135 3820 342e 3731 3437 3838  .029158 4.714788
-00009970: 2c32 2e33 3433 3137 3734 2043 2035 2e30  ,2.3431774 C 5.0
-00009980: 3639 3235 3534 2c32 2e36 3736 3438 3035  692554,2.6764805
-00009990: 2035 2e33 3433 3539 3131 2c33 2e30 3838   5.3435911,3.088
-000099a0: 3438 3631 2035 2e35 3434 3233 3439 2c33  4861 5.5442349,3
-000099b0: 2e35 3330 3136 3332 2043 2035 2e38 3437  .5301632 C 5.847
-000099c0: 3136 3038 2c34 2e31 3834 3534 3739 2036  1608,4.1845479 6
-000099d0: 2e30 3836 3334 3734 2c34 2e38 3636 3432  .0863474,4.86642
-000099e0: 3320 362e 3239 3935 3736 342c 352e 3535  3 6.2995764,5.55
-000099f0: 3436 3230 3520 4320 362e 3633 3136 3231  46205 C 6.631621
-00009a00: 342c 362e 3633 3530 3537 2036 2e38 3936  4,6.635057 6.896
-00009a10: 3030 3537 2c37 2e37 3335 3036 3634 2037  0057,7.7350664 7
-00009a20: 2e31 3331 3833 3232 2c38 2e38 3430 3038  .1318322,8.84008
-00009a30: 3836 2043 2037 2e33 3237 3734 3337 2c39  86 C 7.3277437,9
-00009a40: 2e37 3632 3139 3032 2037 2e35 3031 3533  .7621902 7.50153
-00009a50: 3539 2c31 302e 3638 3838 3833 2037 2e36  59,10.688883 7.6
-00009a60: 3631 3534 3833 2c31 312e 3631 3738 3437  615483,11.617847
-00009a70: 2043 2038 2e30 3831 3738 3339 2c39 2e37   C 8.0817839,9.7
-00009a80: 3430 3031 3931 2038 2e36 3532 3137 3233  400191 8.6521723
-00009a90: 2c37 2e38 3931 3038 3132 2039 2e34 3336  ,7.8910812 9.436
-00009aa0: 3530 3531 2c36 2e31 3331 3937 3937 2043  5051,6.1319797 C
-00009ab0: 2031 302e 3132 3236 3635 2c34 2e35 3932   10.122665,4.592
-00009ac0: 3831 3332 2031 302e 3937 3637 3337 2c33  8132 10.976737,3
-00009ad0: 2e31 3233 3832 3333 2031 322e 3032 3333  .1238233 12.0233
-00009ae0: 3732 2c31 2e38 3030 3837 3336 2043 2031  72,1.8008736 C 1
-00009af0: 322e 3134 3234 3432 2c31 2e36 3534 3137  2.142442,1.65417
-00009b00: 3932 2031 322e 3235 3836 392c 312e 3530  92 12.25869,1.50
-00009b10: 3034 3933 3320 3132 2e33 3835 3630 372c  04933 12.385607,
-00009b20: 312e 3336 3239 3732 3820 4320 3133 2e34  1.3629728 C 13.4
-00009b30: 3830 3639 312c 312e 3135 3232 3833 3820  80691,1.1522838 
-00009b40: 3134 2e35 3735 3737 372c 302e 3934 3135  14.575777,0.9415
-00009b50: 3933 3439 2031 352e 3637 3038 3631 2c30  9349 15.670861,0
-00009b60: 2e37 3330 3930 3434 3720 4320 3136 2e30  .73090447 C 16.0
-00009b70: 3130 3439 322c 312e 3530 3135 3635 3920  10492,1.5015659 
-00009b80: 3136 2e32 3734 3838 322c 322e 3330 3331  16.274882,2.3031
-00009b90: 3538 3920 3136 2e35 3034 3732 372c 332e  589 16.504727,3.
-00009ba0: 3131 3236 3339 3720 4320 3136 2e38 3437  1126397 C 16.847
-00009bb0: 3132 332c 342e 3332 3733 3932 3720 3137  123,4.3273927 17
-00009bc0: 2e31 3039 3032 312c 352e 3536 3333 3937  .109021,5.563397
-00009bd0: 3120 3137 2e33 3333 3330 322c 362e 3830  1 17.333302,6.80
-00009be0: 3439 3038 3220 4320 3137 2e34 3635 3638  49082 C 17.46568
-00009bf0: 352c 372e 3533 3932 3134 3520 3137 2e35  5,7.5392145 17.5
-00009c00: 3832 3536 362c 382e 3237 3632 3330 3620  82566,8.2762306 
-00009c10: 3137 2e36 3930 3534 2c39 2e30 3134 3439  17.69054,9.01449
-00009c20: 3139 2043 2031 372e 3834 3130 3131 2c31  19 C 17.841011,1
-00009c30: 302e 3031 3035 3534 2031 372e 3939 3134  0.010554 17.9914
-00009c40: 382c 3131 2e30 3036 3631 3520 3138 2e31  8,11.006615 18.1
-00009c50: 3431 3935 312c 3132 2e30 3032 3637 3620  41951,12.002676 
-00009c60: 4320 3138 2e32 3336 3232 362c 3132 2e36  C 18.236226,12.6
-00009c70: 3831 3938 3220 3138 2e33 3330 3436 382c  81982 18.330468,
-00009c80: 3133 2e33 3631 3334 3920 3138 2e34 3133  13.361349 18.413
-00009c90: 3035 312c 3134 2e30 3432 3139 3520 4320  051,14.042195 C 
-00009ca0: 3138 2e34 3438 3636 392c 3134 2e33 3430  18.448669,14.340
-00009cb0: 3632 3420 3138 2e34 3739 3036 392c 3134  624 18.479069,14
-00009cc0: 2e36 3339 3635 3820 3138 2e35 3137 3334  .639658 18.51734
-00009cd0: 2c31 342e 3933 3737 3734 2043 2031 382e  ,14.937774 C 18.
-00009ce0: 3631 3839 3334 2c31 352e 3734 3537 3038  618934,15.745708
-00009cf0: 2031 382e 3734 3139 3637 2c31 362e 3535   18.741967,16.55
-00009d00: 3137 3935 2031 382e 3931 3639 3837 2c31  1795 18.916987,1
-00009d10: 372e 3334 3733 3831 2043 2031 382e 3939  7.347381 C 18.99
-00009d20: 3632 3334 2c31 372e 3730 3435 3232 2031  6234,17.704522 1
-00009d30: 392e 3038 3631 3431 2c31 382e 3035 3936  9.086141,18.0596
-00009d40: 3133 2031 392e 3139 3734 3432 2c31 382e  13 19.197442,18.
-00009d50: 3430 3832 3220 4320 3139 2e36 3534 3536  40822 C 19.65456
-00009d60: 342c 3137 2e35 3334 3031 3420 3230 2e32  4,17.534014 20.2
-00009d70: 3033 3037 312c 3136 2e37 3031 3237 3520  03071,16.701275 
-00009d80: 3230 2e38 3830 3730 362c 3135 2e39 3831  20.880706,15.981
-00009d90: 3335 3320 4320 3231 2e34 3435 3337 372c  353 C 21.445377,
-00009da0: 3135 2e33 3830 3737 3120 3232 2e31 3034  15.380771 22.104
-00009db0: 3331 382c 3134 2e38 3633 3530 3720 3232  318,14.863507 22
-00009dc0: 2e38 3432 3331 362c 3134 2e34 3932 3538  .842316,14.49258
-00009dd0: 3620 4320 3233 2e35 3138 3433 342c 3134  6 C 23.518434,14
-00009de0: 2e31 3530 3537 3320 3234 2e32 3537 3035  .150573 24.25705
-00009df0: 352c 3133 2e39 3336 3032 3520 3235 2e30  5,13.936025 25.0
-00009e00: 3039 3435 342c 3133 2e38 3530 3330 3420  09454,13.850304 
-00009e10: 4320 3235 2e35 3636 3938 392c 3133 2e37  C 25.566989,13.7
-00009e20: 3837 3336 2032 362e 3133 3232 3138 2c31  8736 26.132218,1
-00009e30: 332e 3738 3438 3639 2032 362e 3638 3934  3.784869 26.6894
-00009e40: 312c 3133 2e38 3533 2043 2032 372e 3337  1,13.853 C 27.37
-00009e50: 3036 3136 2c31 332e 3933 3630 3736 2032  0616,13.936076 2
-00009e60: 382e 3033 3838 3736 2c31 342e 3133 3331  8.038876,14.1331
-00009e70: 2032 382e 3635 3130 3631 2c31 342e 3434   28.651061,14.44
-00009e80: 3431 3639 2043 2032 392e 3233 3431 3837  4169 C 29.234187
-00009e90: 2c31 342e 3733 3837 3133 2032 392e 3736  ,14.738713 29.76
-00009ea0: 3338 3035 2c31 352e 3133 3337 3835 2033  3805,15.133785 3
-00009eb0: 302e 3232 3735 3031 2c31 352e 3539 3238  0.227501,15.5928
-00009ec0: 3437 2043 2033 302e 3731 3731 332c 3136  47 C 30.71713,16
-00009ed0: 2e30 3731 3531 3720 3331 2e31 3333 3830  .071517 31.13380
-00009ee0: 352c 3136 2e36 3238 3231 3220 3331 2e34  5,16.628212 31.4
-00009ef0: 3331 3934 2c31 372e 3234 3536 3632 2043  3194,17.245662 C
-00009f00: 2033 312e 3732 3335 392c 3137 2e38 3435   31.72359,17.845
-00009f10: 3638 3320 3331 2e39 3030 3037 382c 3138  683 31.900078,18
-00009f20: 2e34 3939 3233 3220 3331 2e39 3636 3436  .499232 31.96646
-00009f30: 392c 3139 2e31 3632 3339 3820 4320 3332  9,19.162398 C 32
-00009f40: 2e30 3135 3631 322c 3139 2e36 3531 3836  .015612,19.65186
-00009f50: 3120 3332 2e30 3039 3332 352c 3230 2e31  1 32.009325,20.1
-00009f60: 3436 3335 3820 3331 2e39 3537 3630 342c  46358 31.957604,
-00009f70: 3230 2e36 3335 3333 3620 4320 3331 2e38  20.635336 C 31.8
-00009f80: 3739 3432 2c32 312e 3336 3631 3837 2033  7942,21.366187 3
-00009f90: 312e 3638 3138 3438 2c32 322e 3038 3538  1.681848,22.0858
-00009fa0: 3439 2033 312e 3335 3930 3037 2c32 322e  49 31.359007,22.
-00009fb0: 3734 3639 3838 2043 2033 312e 3033 3534  746988 C 31.0354
-00009fc0: 3432 2c32 332e 3431 3335 3936 2033 302e  42,23.413596 30.
-00009fd0: 3538 3731 3635 2c32 342e 3031 3637 3138  587165,24.016718
-00009fe0: 2033 302e 3035 3736 352c 3234 2e35 3333   30.05765,24.533
-00009ff0: 3939 3720 4320 3239 2e35 3536 3338 342c  997 C 29.556384,
-0000a000: 3235 2e30 3235 3839 3320 3238 2e39 3736  25.025893 28.976
-0000a010: 3931 372c 3235 2e34 3431 3532 3120 3238  917,25.441521 28
-0000a020: 2e33 3337 3938 332c 3235 2e37 3335 3535  .337983,25.73555
-0000a030: 3520 4320 3237 2e37 3230 3433 312c 3236  5 C 27.720431,26
-0000a040: 2e30 3231 3636 3920 3237 2e30 3531 3332  .021669 27.05132
-0000a050: 382c 3236 2e31 3931 3332 3220 3236 2e33  8,26.191322 26.3
-0000a060: 3733 3938 2c32 362e 3235 3132 3731 2043  7398,26.251271 C
-0000a070: 2032 352e 3930 3335 3439 2c32 362e 3239   25.903549,26.29
-0000a080: 3333 3439 2032 352e 3432 3935 3039 2c32  3349 25.429509,2
-0000a090: 362e 3238 3432 3539 2032 342e 3935 3933  6.284259 24.9593
-0000a0a0: 3531 2c32 362e 3234 3332 3333 2043 2032  51,26.243233 C 2
-0000a0b0: 342e 3130 3234 3634 2c32 362e 3136 3638  4.102464,26.1668
-0000a0c0: 3238 2032 332e 3235 3731 3435 2c32 352e  28 23.257145,25.
-0000a0d0: 3935 3532 3237 2032 322e 3436 3834 3531  955227 22.468451
-0000a0e0: 2c32 352e 3631 3039 3931 2043 2032 312e  ,25.610991 C 21.
-0000a0f0: 3631 3036 3332 2c32 352e 3233 3836 3231  610632,25.238621
-0000a100: 2032 302e 3832 3335 3031 2c32 342e 3731   20.823501,24.71
-0000a110: 3335 3437 2032 302e 3132 3630 3635 2c32  3547 20.126065,2
-0000a120: 342e 3039 3236 3033 2043 2031 392e 3932  4.092603 C 19.92
-0000a130: 3130 3434 2c32 332e 3931 3033 3639 2031  1044,23.910369 1
-0000a140: 392e 3732 3333 3336 2c32 332e 3731 3939  9.723336,23.7199
-0000a150: 3531 2031 392e 3533 3237 3136 2c32 332e  51 19.532716,23.
-0000a160: 3532 3237 3234 2043 2031 392e 3131 3138  522724 C 19.1118
-0000a170: 3439 2c32 342e 3632 3536 3932 2031 382e  49,24.625692 18.
-0000a180: 3636 3532 3337 2c32 352e 3731 3938 3434  665237,25.719844
-0000a190: 2031 382e 3135 3731 342c 3236 2e37 3835   18.15714,26.785
-0000a1a0: 3835 2043 2031 372e 3834 3034 312c 3237  85 C 17.84041,27
-0000a1b0: 2e34 3436 3438 3620 3137 2e35 3031 3436  .446486 17.50146
-0000a1c0: 382c 3238 2e30 3938 3037 3520 3137 2e31  8,28.098075 17.1
-0000a1d0: 3036 3831 312c 3238 2e37 3135 3938 3820  06811,28.715988 
-0000a1e0: 4320 3136 2e38 3635 3238 372c 3239 2e30  C 16.865287,29.0
-0000a1f0: 3930 3837 3520 3136 2e36 3033 3938 342c  90875 16.603984,
-0000a200: 3239 2e34 3535 3834 3320 3136 2e32 3934  29.455843 16.294
-0000a210: 3136 372c 3239 2e37 3737 3836 3320 4320  167,29.777863 C 
-0000a220: 3135 2e39 3438 3634 352c 3330 2e31 3337  15.948645,30.137
-0000a230: 3533 3220 3135 2e35 3236 3039 362c 3330  532 15.526096,30
-0000a240: 2e34 3137 3238 2031 352e 3037 3431 3234  .41728 15.074124
-0000a250: 2c33 302e 3632 3530 3533 2043 2031 342e  ,30.625053 C 14.
-0000a260: 3530 3030 3931 2c33 302e 3838 3930 3935  500091,30.889095
-0000a270: 2031 332e 3838 3230 3031 2c33 312e 3034   13.882001,31.04
-0000a280: 3533 3620 3133 2e32 3539 3130 322c 3331  536 13.259102,31
-0000a290: 2e31 3431 3034 3320 4320 3132 2e36 3138  .141043 C 12.618
-0000a2a0: 3332 342c 3331 2e32 3338 3833 2031 312e  324,31.23883 11.
-0000a2b0: 3936 3932 3535 2c33 312e 3237 3134 3636  969255,31.271466
-0000a2c0: 2031 312e 3332 3135 3636 2c33 312e 3236   11.321566,31.26
-0000a2d0: 3839 3633 2043 2031 302e 3539 3832 3631  8963 C 10.598261
-0000a2e0: 2c33 312e 3236 3839 3633 2039 2e38 3734  ,31.268963 9.874
-0000a2f0: 3935 3732 2c33 312e 3236 3839 3633 2039  9572,31.268963 9
-0000a300: 2e31 3531 3635 3239 2c33 312e 3236 3839  .1516529,31.2689
-0000a310: 3633 2043 2039 2e31 3531 3635 3239 2c33  63 C 9.1516529,3
-0000a320: 302e 3537 3739 3235 2039 2e31 3531 3635  0.577925 9.15165
-0000a330: 3239 2c32 392e 3838 3638 3839 2039 2e31  29,29.886889 9.1
-0000a340: 3531 3635 3239 2c32 392e 3139 3538 3531  516529,29.195851
-0000a350: 2043 2039 2e35 3238 3431 3937 2c32 392e   C 9.5284197,29.
-0000a360: 3139 3537 3436 2039 2e39 3035 3138 3737  195746 9.9051877
-0000a370: 2c32 392e 3139 3630 3720 3130 2e32 3831  ,29.19607 10.281
-0000a380: 3935 342c 3239 2e31 3935 3637 3220 4320  954,29.195672 C 
-0000a390: 3130 2e39 3830 3037 352c 3239 2e31 3931  10.980075,29.191
-0000a3a0: 3531 2031 312e 3638 3037 3436 2c32 392e  51 11.680746,29.
-0000a3b0: 3134 3431 3136 2031 322e 3336 3538 3936  144116 12.365896
-0000a3c0: 2c32 392e 3030 3438 3335 2043 2031 322e  ,29.004835 C 12.
-0000a3d0: 3837 3932 3132 2c32 382e 3839 3931 3835  879212,28.899185
-0000a3e0: 2031 332e 3338 3634 3135 2c32 382e 3734   13.386415,28.74
-0000a3f0: 3035 3520 3133 2e38 3436 3137 372c 3238  055 13.846177,28
-0000a400: 2e34 3835 3339 3220 4320 3134 2e31 3830  .485392 C 14.180
-0000a410: 3338 362c 3238 2e33 3030 3039 3720 3134  386,28.300097 14
-0000a420: 2e34 3836 3437 342c 3238 2e30 3539 3435  .486474,28.05945
-0000a430: 2031 342e 3732 3836 382c 3237 2e37 3632   14.72868,27.762
-0000a440: 3639 3720 4320 3134 2e39 3638 3532 392c  697 C 14.968529,
-0000a450: 3237 2e34 3730 3137 2031 352e 3136 3638  27.47017 15.1668
-0000a460: 362c 3237 2e31 3436 3338 3720 3135 2e33  6,27.146387 15.3
-0000a470: 3532 3230 382c 3236 2e38 3137 3434 3820  52208,26.817448 
-0000a480: 4320 3135 2e36 3834 3638 352c 3236 2e32  C 15.684685,26.2
-0000a490: 3230 3732 3820 3135 2e39 3639 3336 312c  20728 15.969361,
-0000a4a0: 3235 2e35 3938 3739 3720 3136 2e32 3337  25.598797 16.237
-0000a4b0: 3930 382c 3234 2e39 3731 3136 3920 4320  908,24.971169 C 
-0000a4c0: 3136 2e36 3939 3632 392c 3233 2e38 3834  16.699629,23.884
-0000a4d0: 3732 3820 3137 2e31 3037 3531 332c 3232  728 17.107513,22
-0000a4e0: 2e37 3736 3237 3420 3137 2e34 3934 3936  .776274 17.49496
-0000a4f0: 352c 3231 2e36 3631 3438 3120 4320 3137  5,21.661481 C 17
-0000a500: 2e35 3538 3131 2c32 312e 3437 3933 3532  .55811,21.479352
-0000a510: 2031 372e 3632 3036 2c32 312e 3239 3639   17.6206,21.2969
-0000a520: 3935 2031 372e 3638 3235 3032 2c32 312e  95 17.682502,21.
-0000a530: 3131 3434 3338 2043 2031 372e 3338 3232  114438 C 17.3822
-0000a540: 3036 2c32 302e 3538 3539 3934 2031 372e  06,20.585994 17.
-0000a550: 3130 3034 3335 2c32 302e 3034 3537 3335  100435,20.045735
-0000a560: 2031 362e 3836 3734 352c 3139 2e34 3833   16.86745,19.483
-0000a570: 3932 3720 4320 3136 2e37 3237 3434 382c  927 C 16.727448,
-0000a580: 3139 2e31 3434 3930 3620 3136 2e36 3036  19.144906 16.606
-0000a590: 3331 362c 3138 2e37 3936 3937 3720 3136  316,18.796977 16
-0000a5a0: 2e35 3237 3133 372c 3138 2e34 3338 3430  .527137,18.43840
-0000a5b0: 3820 4320 3136 2e34 3332 3936 312c 3138  8 C 16.432961,18
-0000a5c0: 2e30 3138 3632 3920 3136 2e33 3632 3630  .018629 16.36260
-0000a5d0: 352c 3137 2e35 3933 3936 3120 3136 2e32  5,17.593961 16.2
-0000a5e0: 3934 3935 342c 3137 2e31 3639 3234 3620  94954,17.169246 
-0000a5f0: 4320 3136 2e31 3435 3136 322c 3136 2e32  C 16.145162,16.2
-0000a600: 3131 3130 3220 3136 2e30 3232 3331 382c  11102 16.022318,
-0000a610: 3135 2e32 3439 2031 352e 3930 3334 3637  15.249 15.903467
-0000a620: 2c31 342e 3238 3636 3132 2043 2031 352e  ,14.286612 C 15.
-0000a630: 3639 3334 3738 2c31 322e 3730 3539 3836  693478,12.705986
-0000a640: 2031 352e 3438 3334 3839 2c31 312e 3132   15.483489,11.12
-0000a650: 3533 3631 2031 352e 3237 3335 2c39 2e35  5361 15.2735,9.5
-0000a660: 3434 3733 3434 2043 2031 352e 3132 3036  447344 C 15.1206
-0000a670: 3736 2c38 2e33 3830 3031 3533 2031 342e  76,8.3800153 14.
-0000a680: 3934 3437 3133 2c37 2e32 3137 3536 3320  944713,7.217563 
-0000a690: 3134 2e37 3039 3535 2c36 2e30 3636 3334  14.70955,6.06634
-0000a6a0: 3635 2043 2031 342e 3536 3535 3934 2c35  65 C 14.565594,5
-0000a6b0: 2e33 3639 3538 3437 2031 342e 3430 3138  .3695847 14.4018
-0000a6c0: 3436 2c34 2e36 3735 3730 3534 2031 342e  46,4.6757054 14.
-0000a6d0: 3138 3238 322c 332e 3939 3833 3039 3220  18282,3.9983092 
-0000a6e0: 4320 3134 2e30 3739 3233 342c 332e 3638  C 14.079234,3.68
-0000a6f0: 3038 3833 3420 3133 2e39 3633 3334 342c  08834 13.963344,
-0000a700: 332e 3336 3638 3335 3520 3133 2e38 3230  3.3668355 13.820
-0000a710: 3634 382c 332e 3036 3437 3037 3320 4320  648,3.0647073 C 
-0000a720: 3133 2e30 3333 3333 322c 332e 3939 3737  13.033332,3.9977
-0000a730: 3132 3120 3132 2e33 3730 3638 352c 352e  121 12.370685,5.
-0000a740: 3033 3033 3937 3520 3131 2e37 3935 3436  0303975 11.79546
-0000a750: 372c 362e 3130 3535 3230 3920 4320 3131  7,6.1055209 C 11
-0000a760: 2e31 3330 3930 322c 372e 3334 3936 3620  .130902,7.34966 
-0000a770: 3130 2e35 3832 3833 2c38 2e36 3533 3133  10.58283,8.65313
-0000a780: 3438 2031 302e 3130 3836 3036 2c39 2e39  48 10.108606,9.9
-0000a790: 3830 3539 3435 2043 2039 2e35 3837 3738  805945 C 9.58778
-0000a7a0: 3535 2c31 312e 3432 3739 3036 2039 2e31  55,11.427906 9.1
-0000a7b0: 3538 3436 3532 2c31 322e 3931 3134 3133  584652,12.911413
-0000a7c0: 2038 2e38 3837 3238 3835 2c31 342e 3432   8.8872885,14.42
-0000a7d0: 3636 3033 2043 2038 2e36 3938 3035 3634  6603 C 8.6980564
-0000a7e0: 2c31 352e 3438 3635 3735 2038 2e35 3838  ,15.486575 8.588
-0000a7f0: 3130 3238 2c31 362e 3536 3234 3837 2038  1028,16.562487 8
-0000a800: 2e35 3932 3836 3337 2c31 372e 3633 3938  .5928637,17.6398
-0000a810: 3535 2043 2038 2e35 3932 3836 3337 2c31  55 C 8.5928637,1
-0000a820: 382e 3036 3134 3935 2038 2e35 3932 3836  8.061495 8.59286
-0000a830: 3337 2c31 382e 3438 3331 3334 2038 2e35  37,18.483134 8.5
-0000a840: 3932 3836 3337 2c31 382e 3930 3437 3734  928637,18.904774
-0000a850: 2043 2037 2e37 3635 3032 3733 2c31 382e   C 7.7650273,18.
-0000a860: 3930 3437 3734 2036 2e39 3337 3139 3232  904774 6.9371922
-0000a870: 2c31 382e 3930 3437 3734 2036 2e31 3039  ,18.904774 6.109
-0000a880: 3335 3539 2c31 382e 3930 3437 3734 207a  3559,18.904774 z
-0000a890: 204d 2032 302e 3039 3135 3035 2c32 312e   M 20.091505,21.
-0000a8a0: 3431 3233 3720 4320 3230 2e37 3033 3938  41237 C 20.70398
-0000a8b0: 392c 3232 2e30 3931 3330 3320 3231 2e33  9,22.091303 21.3
-0000a8c0: 3736 3231 362c 3232 2e37 3232 3032 2032  76216,22.72202 2
-0000a8d0: 322e 3133 3038 3637 2c32 332e 3234 3132  2.130867,23.2412
-0000a8e0: 3036 2043 2032 322e 3736 3032 3736 2c32  06 C 22.760276,2
-0000a8f0: 332e 3637 3336 3820 3233 2e34 3531 3135  3.67368 23.45115
-0000a900: 362c 3234 2e30 3236 3330 3520 3234 2e31  6,24.026305 24.1
-0000a910: 3839 3837 352c 3234 2e32 3238 3137 3920  89875,24.228179 
-0000a920: 4320 3234 2e38 3531 3831 362c 3234 2e34  C 24.851816,24.4
-0000a930: 3130 3430 3620 3235 2e35 3530 3432 392c  10406 25.550429,
-0000a940: 3234 2e34 3634 3634 3120 3236 2e32 3331  24.464641 26.231
-0000a950: 3430 372c 3234 2e33 3732 3538 3620 4320  407,24.372586 C 
-0000a960: 3236 2e37 3433 3531 322c 3234 2e33 3033  26.743512,24.303
-0000a970: 3536 3320 3237 2e32 3434 3335 322c 3234  563 27.244352,24
-0000a980: 2e31 3432 3434 3920 3237 2e36 3934 3733  .142449 27.69473
-0000a990: 372c 3233 2e38 3838 3038 3720 4320 3238  7,23.888087 C 28
-0000a9a0: 2e30 3733 3939 392c 3233 2e36 3735 3337  .073999,23.67537
-0000a9b0: 3420 3238 2e34 3135 3635 392c 3233 2e33  4 28.415659,23.3
-0000a9c0: 3938 3934 3520 3238 2e37 3133 3531 372c  98945 28.713517,
-0000a9d0: 3233 2e30 3832 3835 3720 4320 3239 2e30  23.082857 C 29.0
-0000a9e0: 3833 3438 372c 3232 2e36 3936 3233 3220  83487,22.696232 
-0000a9f0: 3239 2e33 3831 3730 352c 3232 2e32 3430  29.381705,22.240
-0000aa00: 3537 3720 3239 2e35 3832 3530 372c 3231  577 29.582507,21
-0000aa10: 2e37 3434 3335 3220 4320 3239 2e38 3036  .744352 C 29.806
-0000aa20: 3735 362c 3231 2e31 3934 3530 3420 3239  756,21.194504 29
-0000aa30: 2e39 3131 3839 342c 3230 2e36 3030 3736  .911894,20.60076
-0000aa40: 3720 3239 2e39 3234 3637 362c 3230 2e30  7 29.924676,20.0
-0000aa50: 3038 3438 2043 2032 392e 3933 3735 3533  0848 C 29.937553
-0000aa60: 2c31 392e 3531 3531 3536 2032 392e 3837  ,19.515156 29.87
-0000aa70: 3930 3436 2c31 392e 3031 3739 3231 2032  9046,19.017921 2
-0000aa80: 392e 3732 3934 3535 2c31 382e 3534 3637  9.729455,18.5467
-0000aa90: 3536 2043 2032 392e 3537 3637 3039 2c31  56 C 29.576709,1
-0000aaa0: 382e 3036 3035 3538 2032 392e 3332 3638  8.060558 29.3268
-0000aab0: 3431 2c31 372e 3630 3633 3935 2032 392e  41,17.606395 29.
-0000aac0: 3030 3533 342c 3137 2e32 3131 3431 2043  00534,17.21141 C
-0000aad0: 2032 382e 3635 3134 3433 2c31 362e 3737   28.651443,16.77
-0000aae0: 3635 3133 2032 382e 3231 3934 3839 2c31  6513 28.219489,1
-0000aaf0: 362e 3430 3035 3337 2032 372e 3732 3237  6.400537 27.7227
-0000ab00: 3237 2c31 362e 3133 3733 3634 2043 2032  27,16.137364 C 2
-0000ab10: 372e 3238 3531 3735 2c31 352e 3930 3339  7.285175,15.9039
-0000ab20: 3436 2032 362e 3830 3035 3633 2c31 352e  46 26.800563,15.
-0000ab30: 3736 3234 3032 2032 362e 3330 3736 3032  762402 26.307602
-0000ab40: 2c31 352e 3731 3235 3238 2043 2032 352e  ,15.712528 C 25.
-0000ab50: 3633 3835 3239 2c31 352e 3634 3438 3839  638529,15.644889
-0000ab60: 2032 342e 3935 3235 3736 2c31 352e 3732   24.952576,15.72
-0000ab70: 3531 3436 2032 342e 3332 3238 3837 2c31  5146 24.322887,1
-0000ab80: 352e 3936 3338 3936 2043 2032 332e 3733  5.963896 C 23.73
-0000ab90: 3137 3831 2c31 362e 3138 3537 3831 2032  1781,16.185781 2
-0000aba0: 332e 3139 3639 3336 2c31 362e 3534 3134  3.196936,16.5414
-0000abb0: 3220 3232 2e37 3335 3338 2c31 362e 3936  2 22.73538,16.96
-0000abc0: 3935 3432 2043 2032 322e 3137 3031 3937  9542 C 22.170197
-0000abd0: 2c31 372e 3439 3333 3736 2032 312e 3730  ,17.493376 21.70
-0000abe0: 3731 3736 2c31 382e 3131 3832 3633 2032  7176,18.118263 2
-0000abf0: 312e 3331 3235 362c 3138 2e37 3737 3720  1.31256,18.7777 
-0000ac00: 4320 3230 2e38 3135 3938 332c 3139 2e36  C 20.815983,19.6
-0000ac10: 3130 3833 3720 3230 2e34 3234 3337 312c  10837 20.424371,
-0000ac20: 3230 2e35 3032 3638 3720 3230 2e30 3931  20.502687 20.091
-0000ac30: 3530 352c 3231 2e34 3132 3337 207a 2027  505,21.41237 z '
-0000ac40: 2073 7479 6c65 3d27 6669 6c6c 3a20 247a   style='fill: $z
-0000ac50: 6f64 6961 635f 636f 6c6f 725f 393b 2720  odiac_color_9;' 
-0000ac60: 2f3e 3c2f 7379 6d62 6f6c 3e3c 7379 6d62  /></symbol><symb
-0000ac70: 6f6c 2069 643d 2761 7175 6172 6975 7327  ol id='aquarius'
-0000ac80: 3e3c 7061 7468 2064 3d27 4d20 3265 2d30  ><path d='M 2e-0
-0000ac90: 362c 3234 2e37 3031 3635 3720 4c20 392e  6,24.701657 L 9.
-0000aca0: 3637 3731 312c 3138 2e33 3232 3638 3420  67711,18.322684 
-0000acb0: 4c20 3131 2e37 3937 3539 322c 3233 2e32  L 11.797592,23.2
-0000acc0: 3634 3134 3220 4c20 3139 2e32 3839 3936  64142 L 19.28996
-0000acd0: 312c 3138 2e33 3232 3638 3420 4c20 3231  1,18.322684 L 21
-0000ace0: 2e33 3834 3734 2c32 332e 3236 3431 3432  .38474,23.264142
-0000acf0: 204c 2032 382e 3838 3939 362c 3138 2e33   L 28.88996,18.3
-0000ad00: 3232 3638 3420 4c20 3331 2e39 3837 3134  22684 L 31.98714
-0000ad10: 392c 3235 2e36 3030 3130 3420 4c20 3239  9,25.600104 L 29
-0000ad20: 2e39 3832 3333 2c32 362e 3438 3537 3136  .98233,26.485716
-0000ad30: 204c 2032 372e 3931 3332 3533 2c32 312e   L 27.913253,21.
-0000ad40: 3534 3432 3538 204c 2032 302e 3338 3233  544258 L 20.3823
-0000ad50: 332c 3236 2e34 3835 3731 3620 4c20 3138  3,26.485716 L 18
-0000ad60: 2e32 3837 3535 312c 3231 2e35 3434 3235  .287551,21.54425
-0000ad70: 3820 4c20 3130 2e38 3230 3838 352c 3236  8 L 10.820885,26
-0000ad80: 2e34 3835 3731 3620 4c20 382e 3731 3332  .485716 L 8.7132
-0000ad90: 3534 2c32 312e 3534 3432 3538 204c 2031  54,21.544258 L 1
-0000ada0: 2e31 3832 3333 312c 3236 2e34 3835 3731  .182331,26.48571
-0000adb0: 3620 4c20 3265 2d30 362c 3234 2e37 3031  6 L 2e-06,24.701
-0000adc0: 3635 3720 7a20 4d20 302e 3031 3238 3533  657 z M 0.012853
-0000add0: 2c31 312e 3339 3138 3038 204c 2039 2e36  ,11.391808 L 9.6
-0000ade0: 3839 3936 312c 3520 4c20 3131 2e38 3130  89961,5 L 11.810
-0000adf0: 3434 332c 392e 3934 3134 3538 204c 2031  443,9.941458 L 1
-0000ae00: 392e 3331 3536 3634 2c35 204c 2032 312e  9.315664,5 L 21.
-0000ae10: 3431 3034 3433 2c39 2e39 3431 3435 3820  410443,9.941458 
-0000ae20: 4c20 3238 2e39 3032 3831 322c 3520 4c20  L 28.902812,5 L 
-0000ae30: 3332 2c31 322e 3237 3734 3220 4c20 3239  32,12.27742 L 29
-0000ae40: 2e39 3935 3138 312c 3133 2e31 3633 3033  .995181,13.16303
-0000ae50: 3220 4c20 3237 2e39 3236 3130 352c 382e  2 L 27.926105,8.
-0000ae60: 3232 3135 3734 204c 2032 302e 3338 3233  221574 L 20.3823
-0000ae70: 332c 3133 2e31 3633 3033 3220 4c20 3138  3,13.163032 L 18
-0000ae80: 2e32 3837 3535 312c 382e 3232 3135 3734  .287551,8.221574
-0000ae90: 204c 2031 302e 3832 3038 3835 2c31 332e   L 10.820885,13.
-0000aea0: 3136 3330 3332 204c 2038 2e37 3338 3935  163032 L 8.73895
-0000aeb0: 372c 382e 3232 3135 3734 204c 2031 2e32  7,8.221574 L 1.2
-0000aec0: 3038 3033 342c 3133 2e31 3633 3033 3220  08034,13.163032 
-0000aed0: 4c20 302e 3031 3238 3533 2c31 312e 3339  L 0.012853,11.39
-0000aee0: 3138 3038 207a 2027 2073 7479 6c65 3d27  1808 z ' style='
-0000aef0: 6669 6c6c 3a20 247a 6f64 6961 635f 636f  fill: $zodiac_co
-0000af00: 6c6f 725f 3130 3b27 202f 3e3c 2f73 796d  lor_10;' /></sym
-0000af10: 626f 6c3e 3c73 796d 626f 6c20 6964 3d27  bol><symbol id='
-0000af20: 7069 7363 6573 273e 3c70 6174 6820 643d  pisces'><path d=
-0000af30: 274d 2031 332e 3238 3831 3232 2c31 362e  'M 13.288122,16.
-0000af40: 3439 3335 3933 2043 2031 332e 3238 3833  493593 C 13.2883
-0000af50: 3431 2c31 382e 3036 3336 3939 2031 332e  41,18.063699 13.
-0000af60: 3035 3436 382c 3139 2e36 3238 3336 3220  05468,19.628362 
-0000af70: 3132 2e36 3539 3932 352c 3231 2e31 3436  12.659925,21.146
-0000af80: 3135 3620 4320 3132 2e33 3537 3730 342c  156 C 12.357704,
-0000af90: 3232 2e33 3037 3234 3420 3131 2e39 3633  22.307244 11.963
-0000afa0: 3231 332c 3233 2e34 3433 3430 3920 3131  213,23.443409 11
-0000afb0: 2e35 3030 3337 2c32 342e 3534 3939 3538  .50037,24.549958
-0000afc0: 2043 2031 302e 3638 3631 3838 2c32 362e   C 10.686188,26.
-0000afd0: 3437 3834 3933 2039 2e36 3636 3137 3537  478493 9.6661757
-0000afe0: 2c32 382e 3332 3230 3533 2038 2e34 3430  ,28.322053 8.440
-0000aff0: 3731 3937 2c33 302e 3032 3030 3736 2043  7197,30.020076 C
-0000b000: 2037 2e39 3437 3039 3537 2c33 302e 3730   7.9470957,30.70
-0000b010: 3436 3520 372e 3432 3037 3830 372c 3331  465 7.4207807,31
-0000b020: 2e33 3635 3634 3920 362e 3836 3430 3932  .365649 6.864092
-0000b030: 372c 3332 2043 2035 2e37 3535 3435 342c  7,32 C 5.755454,
-0000b040: 3332 2034 2e36 3436 3831 3533 2c33 3220  32 4.6468153,32 
-0000b050: 332e 3533 3831 3736 362c 3332 2043 2035  3.5381766,32 C 5
-0000b060: 2e30 3532 3230 3334 2c33 302e 3430 3430  .0522034,30.4040
-0000b070: 3535 2036 2e34 3039 3739 3237 2c32 382e  55 6.4097927,28.
-0000b080: 3635 3038 3732 2037 2e34 3938 3135 3037  650872 7.4981507
-0000b090: 2c32 362e 3733 3633 3335 2043 2038 2e34  ,26.736335 C 8.4
-0000b0a0: 3332 3530 3437 2c32 352e 3039 3532 3236  325047,25.095226
-0000b0b0: 2039 2e31 3633 3030 3037 2c32 332e 3333   9.1630007,23.33
-0000b0c0: 3438 3936 2039 2e36 3238 3537 3737 2c32  4896 9.6285777,2
-0000b0d0: 312e 3530 3335 3739 2043 2031 302e 3034  1.503579 C 10.04
-0000b0e0: 3632 3338 2c31 392e 3836 3836 3336 2031  6238,19.868636 1
-0000b0f0: 302e 3235 3136 3735 2c31 382e 3138 3037  0.251675,18.1807
-0000b100: 3131 2031 302e 3235 3037 3536 2c31 362e  11 10.250756,16.
-0000b110: 3439 3335 3933 2043 2038 2e30 3839 3136  493593 C 8.08916
-0000b120: 3337 2c31 362e 3439 3335 3933 2035 2e39  37,16.493593 5.9
-0000b130: 3237 3537 3037 2c31 362e 3439 3335 3933  275707,16.493593
-0000b140: 2033 2e37 3635 3937 3931 2c31 362e 3439   3.7659791,16.49
-0000b150: 3335 3933 2043 2033 2e37 3635 3937 3931  3593 C 3.7659791
-0000b160: 2c31 352e 3733 3432 3139 2033 2e37 3635  ,15.734219 3.765
-0000b170: 3937 3931 2c31 342e 3937 3438 3436 2033  9791,14.974846 3
-0000b180: 2e37 3635 3937 3931 2c31 342e 3231 3534  .7659791,14.2154
-0000b190: 3732 2043 2035 2e39 3237 3537 3037 2c31  72 C 5.9275707,1
-0000b1a0: 342e 3231 3534 3732 2038 2e30 3839 3136  4.215472 8.08916
-0000b1b0: 3337 2c31 342e 3231 3534 3732 2031 302e  37,14.215472 10.
-0000b1c0: 3235 3037 3536 2c31 342e 3231 3534 3732  250756,14.215472
-0000b1d0: 2043 2031 302e 3135 3539 3632 2c31 322e   C 10.155962,12.
-0000b1e0: 3439 3739 3931 2039 2e38 3132 3438 3637  497991 9.8124867
-0000b1f0: 2c31 302e 3739 3634 3720 392e 3235 3436  ,10.79647 9.2546
-0000b200: 3438 372c 392e 3137 3030 3433 2043 2038  487,9.170043 C 8
-0000b210: 2e36 3130 3534 3637 2c37 2e32 3836 3420  .6105467,7.2864 
-0000b220: 372e 3638 3632 3130 372c 352e 3530 3536  7.6862107,5.5056
-0000b230: 3931 2036 2e35 3833 3036 3637 2c33 2e38  91 6.5830667,3.8
-0000b240: 3531 3235 3420 4320 352e 3637 3433 3033  51254 C 5.674303
-0000b250: 312c 322e 3438 3739 3038 2034 2e36 3435  1,2.487908 4.645
-0000b260: 3132 352c 312e 3230 3730 3938 3920 332e  125,1.2070989 3.
-0000b270: 3533 3831 3736 362c 3365 2d30 3720 4320  5381766,3e-07 C 
-0000b280: 342e 3538 3630 3638 2c33 652d 3037 2035  4.586068,3e-07 5
-0000b290: 2e36 3333 3935 3933 2c33 652d 3037 2036  .6339593,3e-07 6
-0000b2a0: 2e36 3831 3835 3037 2c33 652d 3037 2043  .6818507,3e-07 C
-0000b2b0: 2038 2e31 3539 3933 3937 2c31 2e35 3735   8.1599397,1.575
-0000b2c0: 3834 3736 2039 2e34 3632 3538 3537 2c33  8476 9.4625857,3
-0000b2d0: 2e33 3231 3635 2031 302e 3530 3433 3335  .32165 10.504335
-0000b2e0: 2c35 2e32 3136 3233 3120 4320 3131 2e34  ,5.216231 C 11.4
-0000b2f0: 3630 3034 342c 362e 3935 3032 3438 2031  60044,6.950248 1
-0000b300: 322e 3139 3330 3536 2c38 2e38 3036 3931  2.193056,8.80691
-0000b310: 3920 3132 2e36 3736 3732 382c 3130 2e37  9 12.676728,10.7
-0000b320: 3236 3938 3520 4320 3132 2e39 3636 3137  26985 C 12.96617
-0000b330: 312c 3131 2e38 3732 3634 3520 3133 2e31  1,11.872645 13.1
-0000b340: 3638 3336 342c 3133 2e30 3430 3030 3620  68364,13.040006 
-0000b350: 3133 2e32 3838 3132 322c 3134 2e32 3135  13.288122,14.215
-0000b360: 3437 3220 4320 3135 2e33 3833 3930 352c  472 C 15.383905,
-0000b370: 3134 2e32 3135 3437 3220 3137 2e34 3739  14.215472 17.479
-0000b380: 3638 382c 3134 2e32 3135 3437 3220 3139  688,14.215472 19
-0000b390: 2e35 3735 3437 2c31 342e 3231 3534 3732  .57547,14.215472
-0000b3a0: 2043 2031 392e 3738 3638 3832 2c31 322e   C 19.786882,12.
-0000b3b0: 3138 3737 3538 2032 302e 3234 3538 3834  187758 20.245884
-0000b3c0: 2c31 302e 3138 3431 3320 3230 2e39 3633  ,10.18413 20.963
-0000b3d0: 3234 392c 382e 3237 3530 3431 2043 2032  249,8.275041 C 2
-0000b3e0: 312e 3637 3034 3239 2c36 2e33 3836 3737  1.670429,6.38677
-0000b3f0: 3220 3232 2e36 3238 3635 352c 342e 3539  2 22.628655,4.59
-0000b400: 3438 3439 2032 332e 3738 3635 3333 2c32  4849 23.786533,2
-0000b410: 2e39 3434 3931 3620 4320 3234 2e35 3133  .944916 C 24.513
-0000b420: 3431 352c 312e 3930 3738 3232 3920 3235  415,1.9078229 25
-0000b430: 2e33 3137 3538 382c 302e 3932 3535 3638  .317588,0.925568
-0000b440: 3720 3236 2e31 3831 3734 322c 3365 2d30  7 26.181742,3e-0
-0000b450: 3720 4320 3237 2e32 3239 3633 332c 3365  7 C 27.229633,3e
-0000b460: 2d30 3720 3238 2e32 3737 3532 352c 3365  -07 28.277525,3e
-0000b470: 2d30 3720 3239 2e33 3235 3431 362c 3365  -07 29.325416,3e
-0000b480: 2d30 3720 4320 3237 2e38 3534 3631 382c  -07 C 27.854618,
-0000b490: 312e 3630 3430 3838 3720 3236 2e35 3138  1.6040887 26.518
-0000b4a0: 3834 392c 332e 3334 3030 3437 2032 352e  849,3.340047 25.
-0000b4b0: 3432 3439 3231 2c35 2e32 3234 3031 3620  424921,5.224016 
-0000b4c0: 4320 3234 2e34 3730 3435 382c 362e 3836  C 24.470458,6.86
-0000b4d0: 3730 3320 3233 2e37 3034 3939 352c 382e  703 23.704995,8.
-0000b4e0: 3632 3534 3938 2032 332e 3231 3531 3735  625498 23.215175
-0000b4f0: 2c31 302e 3436 3333 3634 2043 2032 322e  ,10.463364 C 22.
-0000b500: 3838 3735 3437 2c31 312e 3638 3932 3332  887547,11.689232
-0000b510: 2032 322e 3638 3332 3831 2c31 322e 3934   22.683281,12.94
-0000b520: 3833 3932 2032 322e 3631 3238 3337 2c31  8392 22.612837,1
-0000b530: 342e 3231 3534 3732 2043 2032 342e 3737  4.215472 C 24.77
-0000b540: 3434 3238 2c31 342e 3231 3534 3732 2032  4428,14.215472 2
-0000b550: 362e 3933 3630 3232 2c31 342e 3231 3534  6.936022,14.2154
-0000b560: 3732 2032 392e 3039 3736 3134 2c31 342e  72 29.097614,14.
-0000b570: 3231 3534 3732 2043 2032 392e 3039 3736  215472 C 29.0976
-0000b580: 3134 2c31 342e 3937 3438 3436 2032 392e  14,14.974846 29.
-0000b590: 3039 3736 3134 2c31 352e 3733 3432 3139  097614,15.734219
-0000b5a0: 2032 392e 3039 3736 3134 2c31 362e 3439   29.097614,16.49
-0000b5b0: 3335 3933 2043 2032 362e 3933 3630 3232  3593 C 26.936022
-0000b5c0: 2c31 362e 3439 3335 3933 2032 342e 3737  ,16.493593 24.77
-0000b5d0: 3434 3238 2c31 362e 3439 3335 3933 2032  4428,16.493593 2
-0000b5e0: 322e 3631 3238 3337 2c31 362e 3439 3335  2.612837,16.4935
-0000b5f0: 3933 2043 2032 322e 3631 3135 3931 2c31  93 C 22.611591,1
-0000b600: 382e 3331 3030 3133 2032 322e 3835 3035  8.310013 22.8505
-0000b610: 3434 2c32 302e 3132 3733 3437 2032 332e  44,20.127347 23.
-0000b620: 3333 3434 3534 2c32 312e 3837 3835 3234  334454,21.878524
-0000b630: 2043 2032 332e 3833 3733 3232 2c32 332e   C 23.837322,23.
-0000b640: 3730 3732 3933 2032 342e 3630 3433 3639  707293 24.604369
-0000b650: 2c32 352e 3435 3934 3934 2032 352e 3537  ,25.459494 25.57
-0000b660: 3036 3934 2c32 372e 3039 3031 3035 2043  0694,27.090105 C
-0000b670: 2032 362e 3632 3237 3237 2c32 382e 3836   26.622727,28.86
-0000b680: 3737 3635 2032 372e 3930 3530 3833 2c33  7765 27.905083,3
-0000b690: 302e 3530 3237 3233 2032 392e 3332 3534  0.502723 29.3254
-0000b6a0: 3136 2c33 3220 4320 3238 2e32 3231 3833  16,32 C 28.22183
-0000b6b0: 392c 3332 2032 372e 3131 3832 3634 2c33  9,32 27.118264,3
-0000b6c0: 3220 3236 2e30 3134 3638 372c 3332 2043  2 26.014687,32 C
-0000b6d0: 2032 342e 3639 3434 3335 2c33 302e 3530   24.694435,30.50
-0000b6e0: 3833 3737 2032 332e 3534 3931 3937 2c32  8377 23.549197,2
-0000b6f0: 382e 3836 3333 3135 2032 322e 3539 3733  8.863315 22.5973
-0000b700: 3133 2c32 372e 3131 3338 3231 2043 2032  13,27.113821 C 2
-0000b710: 322e 3130 3432 382c 3236 2e32 3037 3739  2.10428,26.20779
-0000b720: 3820 3231 2e36 3630 3533 332c 3235 2e32  8 21.660533,25.2
-0000b730: 3734 3931 2032 312e 3236 3832 3635 2c32  7491 21.268265,2
-0000b740: 342e 3332 3039 3335 2043 2032 302e 3632  4.320935 C 20.62
-0000b750: 3336 3334 2c32 322e 3733 3737 3339 2032  3634,22.737739 2
-0000b760: 302e 3131 3536 3133 2c32 312e 3039 3337  0.115613,21.0937
-0000b770: 3239 2031 392e 3832 3839 3232 2c31 392e  29 19.828922,19.
-0000b780: 3430 3637 3231 2043 2031 392e 3636 3535  406721 C 19.6655
-0000b790: 3835 2c31 382e 3434 3437 3638 2031 392e  85,18.444768 19.
-0000b7a0: 3537 3534 3032 2c31 372e 3436 3936 3033  575402,17.469603
-0000b7b0: 2031 392e 3537 3534 372c 3136 2e34 3933   19.57547,16.493
-0000b7c0: 3539 3320 4320 3137 2e34 3739 3638 382c  593 C 17.479688,
-0000b7d0: 3136 2e34 3933 3539 3320 3135 2e33 3833  16.493593 15.383
-0000b7e0: 3930 352c 3136 2e34 3933 3539 3320 3133  905,16.493593 13
-0000b7f0: 2e32 3838 3132 322c 3136 2e34 3933 3539  .288122,16.49359
-0000b800: 3320 7a20 2720 7374 796c 653d 2766 696c  3 z ' style='fil
-0000b810: 6c3a 2024 7a6f 6469 6163 5f63 6f6c 6f72  l: $zodiac_color
-0000b820: 5f31 313b 2720 2f3e 3c2f 7379 6d62 6f6c  _11;' /></symbol
-0000b830: 3e3c 212d 2d20 4173 7065 6374 7320 3132  ><!-- Aspects 12
-0000b840: 7831 3220 2d2d 3e3c 7379 6d62 6f6c 2069  x12 --><symbol i
-0000b850: 643d 276f 7262 3027 3e3c 7061 7468 2064  d='orb0'><path d
-0000b860: 3d27 4d20 362e 3036 3937 3533 392c 372e  ='M 6.0697539,7.
-0000b870: 3332 3334 3835 3220 4320 362e 3036 3937  3234852 C 6.0697
-0000b880: 3533 392c 382e 3733 3534 3838 3220 342e  539,8.7354882 4.
-0000b890: 3931 3733 3635 312c 392e 3838 3031 3434  9173651,9.880144
-0000b8a0: 3220 332e 3439 3538 3231 342c 392e 3838  2 3.4958214,9.88
-0000b8b0: 3031 3434 3220 4320 322e 3037 3432 3737  01442 C 2.074277
-0000b8c0: 352c 392e 3838 3031 3434 3220 302e 3932  5,9.8801442 0.92
-0000b8d0: 3138 3838 3537 2c38 2e37 3335 3438 3832  188857,8.7354882
-0000b8e0: 2030 2e39 3231 3838 3835 372c 372e 3332   0.92188857,7.32
-0000b8f0: 3334 3835 3220 4320 302e 3932 3138 3838  34852 C 0.921888
-0000b900: 3537 2c35 2e39 3131 3438 3232 2032 2e30  57,5.9114822 2.0
-0000b910: 3734 3237 3735 2c34 2e37 3636 3832 3732  742775,4.7668272
-0000b920: 2033 2e34 3935 3832 3134 2c34 2e37 3636   3.4958214,4.766
-0000b930: 3832 3732 2043 2034 2e39 3137 3336 3531  8272 C 4.9173651
-0000b940: 2c34 2e37 3636 3832 3732 2036 2e30 3639  ,4.7668272 6.069
-0000b950: 3735 3339 2c35 2e39 3131 3438 3232 2036  7539,5.9114822 6
-0000b960: 2e30 3639 3735 3339 2c37 2e33 3233 3438  .0697539,7.32348
-0000b970: 3532 204c 2036 2e30 3639 3735 3339 2c37  52 L 6.0697539,7
-0000b980: 2e33 3233 3438 3532 207a 204d 2035 2e36  .3234852 z M 5.6
-0000b990: 3235 3236 3039 2c35 2e32 3131 3332 3032  252609,5.2113202
-0000b9a0: 2043 2031 302e 3037 3031 392c 302e 3736   C 10.07019,0.76
-0000b9b0: 3633 3930 3138 2031 302e 3037 3031 392c  639018 10.07019,
-0000b9c0: 302e 3736 3633 3930 3138 2031 302e 3037  0.76639018 10.07
-0000b9d0: 3031 392c 302e 3736 3633 3930 3138 2720  019,0.76639018' 
-0000b9e0: 7374 796c 653d 276f 7061 6369 7479 3a31  style='opacity:1
-0000b9f0: 3b66 696c 6c3a 6e6f 6e65 3b66 696c 6c2d  ;fill:none;fill-
-0000ba00: 6f70 6163 6974 793a 313b 6669 6c6c 2d72  opacity:1;fill-r
-0000ba10: 756c 653a 6e6f 6e7a 6572 6f3b 7374 726f  ule:nonzero;stro
-0000ba20: 6b65 3a20 246f 7262 5f63 6f6c 6f72 5f30  ke: $orb_color_0
-0000ba30: 3b73 7472 6f6b 652d 7769 6474 683a 312e  ;stroke-width:1.
-0000ba40: 3437 3633 3330 3634 3b73 7472 6f6b 652d  47633064;stroke-
-0000ba50: 6c69 6e65 6361 703a 6275 7474 3b73 7472  linecap:butt;str
-0000ba60: 6f6b 652d 6c69 6e65 6a6f 696e 3a6d 6974  oke-linejoin:mit
-0000ba70: 6572 3b73 7472 6f6b 652d 6d69 7465 726c  er;stroke-miterl
-0000ba80: 696d 6974 3a34 3b73 7472 6f6b 652d 6461  imit:4;stroke-da
-0000ba90: 7368 6172 7261 793a 6e6f 6e65 3b73 7472  sharray:none;str
-0000baa0: 6f6b 652d 6f70 6163 6974 793a 3127 202f  oke-opacity:1' /
-0000bab0: 3e3c 2f73 796d 626f 6c3e 3c73 796d 626f  ></symbol><symbo
-0000bac0: 6c20 6964 3d27 6f72 6233 3027 3e3c 7061  l id='orb30'><pa
-0000bad0: 7468 2064 3d27 4d20 302e 3831 3637 3531  th d='M 0.816751
-0000bae0: 3534 2c36 2e31 3334 3233 3938 2043 2031  54,6.1342398 C 1
-0000baf0: 312e 3334 3636 3135 2c36 2e31 3632 3031  1.346615,6.16201
-0000bb00: 3438 2031 312e 3334 3636 3135 2c36 2e31  48 11.346615,6.1
-0000bb10: 3632 3031 3438 2031 312e 3334 3636 3135  620148 11.346615
-0000bb20: 2c36 2e31 3632 3031 3438 204d 2031 302e  ,6.1620148 M 10.
-0000bb30: 3631 3231 3834 2c30 2e37 3539 3935 3737  612184,0.7599577
-0000bb40: 3320 4320 352e 3731 3338 3437 392c 352e  3 C 5.7138479,5.
-0000bb50: 3930 3332 3130 3820 352e 3731 3338 3437  9032108 5.713847
-0000bb60: 392c 352e 3930 3332 3130 3820 352e 3731  9,5.9032108 5.71
-0000bb70: 3338 3437 392c 352e 3930 3332 3130 3820  38479,5.9032108 
-0000bb80: 4d20 312e 3330 3533 3435 312c 302e 3735  M 1.3053451,0.75
-0000bb90: 3939 3537 3733 2043 2035 2e38 3830 3731  995773 C 5.88071
-0000bba0: 3839 2c36 2e31 3932 3531 3638 2035 2e38  89,6.1925168 5.8
-0000bbb0: 3830 3731 3839 2c36 2e31 3932 3531 3638  807189,6.1925168
-0000bbc0: 2035 2e38 3830 3731 3839 2c36 2e31 3932   5.8807189,6.192
-0000bbd0: 3531 3638 2720 7374 796c 653d 276f 7061  5168' style='opa
-0000bbe0: 6369 7479 3a31 3b66 696c 6c3a 6e6f 6e65  city:1;fill:none
-0000bbf0: 3b66 696c 6c2d 6f70 6163 6974 793a 313b  ;fill-opacity:1;
-0000bc00: 6669 6c6c 2d72 756c 653a 6e6f 6e7a 6572  fill-rule:nonzer
-0000bc10: 6f3b 7374 726f 6b65 3a20 246f 7262 5f63  o;stroke: $orb_c
-0000bc20: 6f6c 6f72 5f33 303b 7374 726f 6b65 2d77  olor_30;stroke-w
-0000bc30: 6964 7468 3a31 2e34 3736 3333 3036 343b  idth:1.47633064;
-0000bc40: 7374 726f 6b65 2d6c 696e 6563 6170 3a62  stroke-linecap:b
-0000bc50: 7574 743b 7374 726f 6b65 2d6c 696e 656a  utt;stroke-linej
-0000bc60: 6f69 6e3a 6d69 7465 723b 7374 726f 6b65  oin:miter;stroke
-0000bc70: 2d6d 6974 6572 6c69 6d69 743a 343b 7374  -miterlimit:4;st
-0000bc80: 726f 6b65 2d64 6173 6861 7272 6179 3a6e  roke-dasharray:n
-0000bc90: 6f6e 653b 7374 726f 6b65 2d6f 7061 6369  one;stroke-opaci
-0000bca0: 7479 3a31 2720 2f3e 3c2f 7379 6d62 6f6c  ty:1' /></symbol
-0000bcb0: 3e3c 7379 6d62 6f6c 2069 643d 276f 7262  ><symbol id='orb
-0000bcc0: 3435 273e 3c70 6174 6820 643d 274d 2039  45'><path d='M 9
-0000bcd0: 2e38 3130 3031 3738 2c39 2e35 3932 3139  .8100178,9.59219
-0000bce0: 3636 2043 2036 2e39 3634 3036 3538 2c39  66 C 6.9640658,9
-0000bcf0: 2e35 3932 3139 3536 2034 2e31 3138 3131  .5921956 4.11811
-0000bd00: 3235 2c39 2e35 3932 3139 3636 2031 2e32  25,9.5921966 1.2
-0000bd10: 3732 3136 2c39 2e35 3932 3139 3636 2043  7216,9.5921966 C
-0000bd20: 2032 2e36 3935 3133 3632 2c36 2e37 3436   2.6951362,6.746
-0000bd30: 3234 3431 2034 2e31 3138 3131 3235 2c33  2441 4.1181125,3
-0000bd40: 2e39 3030 3239 3035 2035 2e35 3431 3038  .9002905 5.54108
-0000bd50: 3838 2c31 2e30 3534 3333 3739 2720 7374  88,1.0543379' st
-0000bd60: 796c 653d 276f 7061 6369 7479 3a31 3b66  yle='opacity:1;f
-0000bd70: 696c 6c3a 6e6f 6e65 3b66 696c 6c2d 6f70  ill:none;fill-op
-0000bd80: 6163 6974 793a 313b 6669 6c6c 2d72 756c  acity:1;fill-rul
-0000bd90: 653a 6e6f 6e7a 6572 6f3b 7374 726f 6b65  e:nonzero;stroke
-0000bda0: 3a20 246f 7262 5f63 6f6c 6f72 5f34 353b  : $orb_color_45;
-0000bdb0: 7374 726f 6b65 2d77 6964 7468 3a31 2e34  stroke-width:1.4
-0000bdc0: 3736 3333 3036 343b 7374 726f 6b65 2d6c  7633064;stroke-l
-0000bdd0: 696e 6563 6170 3a62 7574 743b 7374 726f  inecap:butt;stro
-0000bde0: 6b65 2d6c 696e 656a 6f69 6e3a 6d69 7465  ke-linejoin:mite
-0000bdf0: 723b 7374 726f 6b65 2d6d 6974 6572 6c69  r;stroke-miterli
-0000be00: 6d69 743a 343b 7374 726f 6b65 2d64 6173  mit:4;stroke-das
-0000be10: 6861 7272 6179 3a6e 6f6e 653b 7374 726f  harray:none;stro
-0000be20: 6b65 2d6f 7061 6369 7479 3a31 2720 2f3e  ke-opacity:1' />
-0000be30: 3c2f 7379 6d62 6f6c 3e3c 7379 6d62 6f6c  </symbol><symbol
-0000be40: 2069 643d 276f 7262 3630 273e 3c70 6174   id='orb60'><pat
-0000be50: 6820 643d 274d 2030 2e38 3831 3832 3434  h d='M 0.8818244
-0000be60: 312c 302e 3731 3831 3437 3635 2043 2033  1,0.71814765 C 3
-0000be70: 2e33 3830 3638 3732 2c33 2e32 3137 3630  .3806872,3.21760
-0000be80: 3037 2035 2e38 3739 3535 3032 2c35 2e37  07 5.8795502,5.7
-0000be90: 3137 3035 3237 2038 2e33 3738 3431 3332  170527 8.3784132
-0000bea0: 2c38 2e32 3136 3530 3537 204d 2038 2e36  ,8.2165057 M 8.6
-0000beb0: 3131 3933 3632 2c34 2e34 3033 3635 3537  119362,4.4036557
-0000bec0: 2043 2035 2e39 3634 3034 3432 2c34 2e34   C 5.9640442,4.4
-0000bed0: 3033 3635 3537 2033 2e33 3136 3135 3334  036557 3.3161534
-0000bee0: 2c34 2e34 3033 3635 3537 2030 2e36 3638  ,4.4036557 0.668
-0000bef0: 3236 3232 312c 342e 3430 3336 3535 3720  26221,4.4036557 
-0000bf00: 4d20 302e 3834 3932 3537 3831 2c38 2e31  M 0.84925781,8.1
-0000bf10: 3934 3439 3737 2043 2033 2e33 3736 3438  944977 C 3.37648
-0000bf20: 3532 2c35 2e37 3232 3433 3337 2035 2e39  52,5.7224337 5.9
-0000bf30: 3033 3731 3332 2c33 2e32 3530 3337 3037  037132,3.2503707
-0000bf40: 2038 2e34 3330 3934 3032 2c30 2e37 3738   8.4309402,0.778
-0000bf50: 3330 3736 3527 2073 7479 6c65 3d27 6f70  30765' style='op
-0000bf60: 6163 6974 793a 313b 6669 6c6c 3a6e 6f6e  acity:1;fill:non
-0000bf70: 653b 6669 6c6c 2d6f 7061 6369 7479 3a31  e;fill-opacity:1
-0000bf80: 3b66 696c 6c2d 7275 6c65 3a6e 6f6e 7a65  ;fill-rule:nonze
-0000bf90: 726f 3b73 7472 6f6b 653a 2024 6f72 625f  ro;stroke: $orb_
-0000bfa0: 636f 6c6f 725f 3630 3b73 7472 6f6b 652d  color_60;stroke-
-0000bfb0: 7769 6474 683a 312e 3437 3633 3330 3634  width:1.47633064
-0000bfc0: 3b73 7472 6f6b 652d 6c69 6e65 6361 703a  ;stroke-linecap:
-0000bfd0: 6275 7474 3b73 7472 6f6b 652d 6c69 6e65  butt;stroke-line
-0000bfe0: 6a6f 696e 3a6d 6974 6572 3b73 7472 6f6b  join:miter;strok
-0000bff0: 652d 6d69 7465 726c 696d 6974 3a34 3b73  e-miterlimit:4;s
-0000c000: 7472 6f6b 652d 6461 7368 6172 7261 793a  troke-dasharray:
-0000c010: 6e6f 6e65 3b73 7472 6f6b 652d 6f70 6163  none;stroke-opac
-0000c020: 6974 793a 3127 202f 3e3c 2f73 796d 626f  ity:1' /></symbo
-0000c030: 6c3e 3c73 796d 626f 6c20 6964 3d27 6f72  l><symbol id='or
-0000c040: 6237 3227 3e3c 7061 7468 2064 3d27 4d20  b72'><path d='M 
-0000c050: 382e 3931 3635 3034 342c 352e 3634 3137  8.9165044,5.6417
-0000c060: 3433 3820 4320 382e 3931 3635 3034 342c  438 C 8.9165044,
-0000c070: 372e 3936 3837 3636 3320 372e 3237 3432  7.9687663 7.2742
-0000c080: 3834 342c 392e 3835 3531 3839 3320 352e  844,9.8551893 5.
-0000c090: 3234 3835 3033 342c 392e 3835 3531 3839  2485034,9.855189
-0000c0a0: 3320 4320 332e 3232 3237 3232 342c 392e  3 C 3.2227224,9.
-0000c0b0: 3835 3531 3839 3320 312e 3538 3035 3032  8551893 1.580502
-0000c0c0: 372c 372e 3936 3837 3636 3320 312e 3538  7,7.9687663 1.58
-0000c0d0: 3035 3032 372c 352e 3634 3137 3433 3820  05027,5.6417438 
-0000c0e0: 4320 312e 3538 3035 3032 372c 332e 3331  C 1.5805027,3.31
-0000c0f0: 3437 3230 3820 332e 3232 3237 3232 342c  47208 3.2227224,
-0000c100: 312e 3432 3832 3936 3720 352e 3234 3835  1.4282967 5.2485
-0000c110: 3033 342c 312e 3432 3832 3936 3720 4320  034,1.4282967 C 
-0000c120: 372e 3237 3432 3834 342c 312e 3432 3832  7.2742844,1.4282
-0000c130: 3936 3720 382e 3931 3635 3034 342c 332e  967 8.9165044,3.
-0000c140: 3331 3437 3230 3820 382e 3931 3635 3034  3147208 8.916504
-0000c150: 342c 352e 3634 3137 3433 3820 4c20 382e  4,5.6417438 L 8.
-0000c160: 3931 3635 3034 342c 352e 3634 3137 3433  9165044,5.641743
-0000c170: 3820 7a20 4d20 352e 3437 3032 3633 342c  8 z M 5.4702634,
-0000c180: 362e 3734 3633 3335 3820 4320 392e 3035  6.7463358 C 9.05
-0000c190: 3131 3830 342c 3130 2e31 3139 3232 3820  11804,10.119228 
-0000c1a0: 392e 3035 3131 3830 342c 3130 2e31 3139  9.0511804,10.119
-0000c1b0: 3232 3820 392e 3035 3131 3830 342c 3130  228 9.0511804,10
-0000c1c0: 2e31 3139 3232 3827 2073 7479 6c65 3d27  .119228' style='
-0000c1d0: 6f70 6163 6974 793a 313b 6669 6c6c 3a6e  opacity:1;fill:n
-0000c1e0: 6f6e 653b 6669 6c6c 2d6f 7061 6369 7479  one;fill-opacity
-0000c1f0: 3a31 3b66 696c 6c2d 7275 6c65 3a6e 6f6e  :1;fill-rule:non
-0000c200: 7a65 726f 3b73 7472 6f6b 653a 2024 6f72  zero;stroke: $or
-0000c210: 625f 636f 6c6f 725f 3732 3b73 7472 6f6b  b_color_72;strok
-0000c220: 652d 7769 6474 683a 312e 3437 3633 3330  e-width:1.476330
-0000c230: 3634 3b73 7472 6f6b 652d 6c69 6e65 6361  64;stroke-lineca
-0000c240: 703a 6275 7474 3b73 7472 6f6b 652d 6c69  p:butt;stroke-li
-0000c250: 6e65 6a6f 696e 3a6d 6974 6572 3b73 7472  nejoin:miter;str
-0000c260: 6f6b 652d 6d69 7465 726c 696d 6974 3a34  oke-miterlimit:4
-0000c270: 3b73 7472 6f6b 652d 6461 7368 6172 7261  ;stroke-dasharra
-0000c280: 793a 6e6f 6e65 3b73 7472 6f6b 652d 6f70  y:none;stroke-op
-0000c290: 6163 6974 793a 3127 202f 3e3c 2f73 796d  acity:1' /></sym
-0000c2a0: 626f 6c3e 3c73 796d 626f 6c20 6964 3d27  bol><symbol id='
-0000c2b0: 6f72 6239 3027 3e3c 7265 6374 2068 6569  orb90'><rect hei
-0000c2c0: 6768 743d 2738 2e30 3836 3139 3527 2077  ght='8.086195' w
-0000c2d0: 6964 7468 3d27 382e 3731 3538 3133 3627  idth='8.7158136'
-0000c2e0: 2078 3d27 312e 3138 3331 3832 3627 2079   x='1.1831826' y
-0000c2f0: 3d27 312e 3138 3932 3534 3527 2073 7479  ='1.1892545' sty
-0000c300: 6c65 3d27 6f70 6163 6974 793a 313b 6669  le='opacity:1;fi
-0000c310: 6c6c 3a6e 6f6e 653b 6669 6c6c 2d6f 7061  ll:none;fill-opa
-0000c320: 6369 7479 3a31 3b66 696c 6c2d 7275 6c65  city:1;fill-rule
-0000c330: 3a6e 6f6e 7a65 726f 3b73 7472 6f6b 653a  :nonzero;stroke:
-0000c340: 2024 6f72 625f 636f 6c6f 725f 3930 3b73   $orb_color_90;s
-0000c350: 7472 6f6b 652d 7769 6474 683a 312e 3235  troke-width:1.25
-0000c360: 3033 3935 3138 3b73 7472 6f6b 652d 6c69  039518;stroke-li
-0000c370: 6e65 6361 703a 6275 7474 3b73 7472 6f6b  necap:butt;strok
-0000c380: 652d 6c69 6e65 6a6f 696e 3a6d 6974 6572  e-linejoin:miter
-0000c390: 3b73 7472 6f6b 652d 6d69 7465 726c 696d  ;stroke-miterlim
-0000c3a0: 6974 3a34 3b73 7472 6f6b 652d 6461 7368  it:4;stroke-dash
-0000c3b0: 6172 7261 793a 6e6f 6e65 3b73 7472 6f6b  array:none;strok
-0000c3c0: 652d 6f70 6163 6974 793a 3127 202f 3e3c  e-opacity:1' /><
-0000c3d0: 2f73 796d 626f 6c3e 3c73 796d 626f 6c20  /symbol><symbol 
-0000c3e0: 6964 3d27 6f72 6231 3230 273e 3c70 6174  id='orb120'><pat
-0000c3f0: 6820 643d 274d 2031 2e31 3735 3530 3131  h d='M 1.1755011
-0000c400: 2c39 2e34 3937 3937 3320 4320 392e 3039  ,9.497973 C 9.09
-0000c410: 3537 3836 392c 392e 3439 3739 3733 2039  57869,9.497973 9
-0000c420: 2e30 3935 3738 3639 2c39 2e34 3937 3937  .0957869,9.49797
-0000c430: 3320 392e 3039 3537 3836 392c 392e 3439  3 9.0957869,9.49
-0000c440: 3739 3733 204c 2035 2e31 3335 3634 3338  7973 L 5.1356438
-0000c450: 2c31 2e34 3633 3930 3633 2043 2035 2e31  ,1.4639063 C 5.1
-0000c460: 3335 3634 3338 2c31 2e34 3633 3930 3633  356438,1.4639063
-0000c470: 2035 2e31 3335 3634 3338 2c31 2e34 3633   5.1356438,1.463
-0000c480: 3930 3633 2031 2e31 3735 3530 3131 2c39  9063 1.1755011,9
-0000c490: 2e34 3937 3937 3320 7a27 2073 7479 6c65  .497973 z' style
-0000c4a0: 3d27 6669 6c6c 3a6e 6f6e 653b 6669 6c6c  ='fill:none;fill
-0000c4b0: 2d72 756c 653a 6576 656e 6f64 643b 7374  -rule:evenodd;st
-0000c4c0: 726f 6b65 3a20 246f 7262 5f63 6f6c 6f72  roke: $orb_color
-0000c4d0: 5f31 3230 3b73 7472 6f6b 652d 7769 6474  _120;stroke-widt
-0000c4e0: 683a 312e 3139 3635 3436 323b 7374 726f  h:1.1965462;stro
-0000c4f0: 6b65 2d6c 696e 6563 6170 3a62 7574 743b  ke-linecap:butt;
-0000c500: 7374 726f 6b65 2d6c 696e 656a 6f69 6e3a  stroke-linejoin:
-0000c510: 6d69 7465 723b 7374 726f 6b65 2d6d 6974  miter;stroke-mit
-0000c520: 6572 6c69 6d69 743a 343b 7374 726f 6b65  erlimit:4;stroke
-0000c530: 2d64 6173 6861 7272 6179 3a6e 6f6e 653b  -dasharray:none;
-0000c540: 7374 726f 6b65 2d6f 7061 6369 7479 3a31  stroke-opacity:1
-0000c550: 2720 2f3e 3c2f 7379 6d62 6f6c 3e3c 7379  ' /></symbol><sy
-0000c560: 6d62 6f6c 2069 643d 276f 7262 3133 3527  mbol id='orb135'
-0000c570: 3e3c 7061 7468 2064 3d27 4d20 322e 3233  ><path d='M 2.23
-0000c580: 3838 3538 322c 312e 3731 3536 3939 3420  88582,1.7156994 
-0000c590: 4c20 392e 3239 3338 3135 342c 312e 3731  L 9.2938154,1.71
-0000c5a0: 3536 3939 3420 4c20 392e 3239 3338 3135  56994 L 9.293815
-0000c5b0: 342c 372e 3738 3131 3832 3720 4c20 322e  4,7.7811827 L 2.
-0000c5c0: 3233 3838 3538 322c 372e 3738 3131 3832  2388582,7.781182
-0000c5d0: 3720 4c20 322e 3233 3838 3538 322c 312e  7 L 2.2388582,1.
-0000c5e0: 3731 3536 3939 3420 7a20 4d20 362e 3834  7156994 z M 6.84
-0000c5f0: 3631 3130 342c 352e 3537 3334 3236 3720  61104,5.5734267 
-0000c600: 4320 362e 3834 3631 3130 342c 352e 3537  C 6.8461104,5.57
-0000c610: 3334 3236 3720 362e 3834 3631 3130 342c  34267 6.8461104,
-0000c620: 352e 3537 3334 3236 3720 332e 3234 3638  5.5734267 3.2468
-0000c630: 3635 322c 3130 2e33 3732 3432 2043 2038  652,10.37242 C 8
-0000c640: 2e30 3435 3835 3834 2c31 302e 3337 3234  .0458584,10.3724
-0000c650: 3220 382e 3034 3538 3538 342c 3130 2e33  2 8.0458584,10.3
-0000c660: 3732 3432 2038 2e30 3435 3835 3834 2c31  7242 8.0458584,1
-0000c670: 302e 3337 3234 3227 2073 7479 6c65 3d27  0.37242' style='
-0000c680: 6669 6c6c 3a6e 6f6e 653b 6669 6c6c 2d72  fill:none;fill-r
-0000c690: 756c 653a 6576 656e 6f64 643b 7374 726f  ule:evenodd;stro
-0000c6a0: 6b65 3a20 246f 7262 5f63 6f6c 6f72 5f31  ke: $orb_color_1
-0000c6b0: 3335 3b73 7472 6f6b 652d 7769 6474 683a  35;stroke-width:
-0000c6c0: 312e 3139 3635 3436 323b 7374 726f 6b65  1.1965462;stroke
-0000c6d0: 2d6c 696e 6563 6170 3a62 7574 743b 7374  -linecap:butt;st
-0000c6e0: 726f 6b65 2d6c 696e 656a 6f69 6e3a 6d69  roke-linejoin:mi
-0000c6f0: 7465 723b 7374 726f 6b65 2d6d 6974 6572  ter;stroke-miter
-0000c700: 6c69 6d69 743a 343b 7374 726f 6b65 2d64  limit:4;stroke-d
-0000c710: 6173 6861 7272 6179 3a6e 6f6e 653b 7374  asharray:none;st
-0000c720: 726f 6b65 2d6f 7061 6369 7479 3a31 2720  roke-opacity:1' 
-0000c730: 2f3e 3c2f 7379 6d62 6f6c 3e3c 7379 6d62  /></symbol><symb
-0000c740: 6f6c 2069 643d 276f 7262 3134 3427 3e3c  ol id='orb144'><
-0000c750: 7061 7468 2064 3d27 4d20 312e 3432 3435  path d='M 1.4245
-0000c760: 3136 392c 312e 3239 3638 3539 3820 4320  169,1.2968598 C 
-0000c770: 312e 3432 3435 3136 392c 392e 3637 3633  1.4245169,9.6763
-0000c780: 3132 3920 312e 3432 3435 3136 392c 392e  129 1.4245169,9.
-0000c790: 3637 3633 3132 3920 312e 3432 3435 3136  6763129 1.424516
-0000c7a0: 392c 392e 3637 3633 3132 3920 4d20 312e  9,9.6763129 M 1.
-0000c7b0: 3932 3038 3333 312c 352e 3338 3638 3237  9208331,5.386827
-0000c7c0: 3920 4320 322e 3737 3232 3838 362c 352e  9 C 2.7722886,5.
-0000c7d0: 3333 3532 3433 3920 332e 3535 3431 3535  3352439 3.554155
-0000c7e0: 332c 352e 3638 3634 3132 3920 332e 3933  3,5.6864129 3.93
-0000c7f0: 3635 3233 372c 362e 3239 3231 3536 3920  65237,6.2921569 
-0000c800: 4320 342e 3331 3838 3932 2c36 2e38 3937  C 4.318892,6.897
-0000c810: 3930 3039 2034 2e32 3335 3136 3134 2c37  9009 4.2351614,7
-0000c820: 2e36 3532 3731 3239 2033 2e37 3230 3636  .6527129 3.72066
-0000c830: 3232 2c38 2e32 3338 3039 3839 2043 2033  22,8.2380989 C 3
-0000c840: 2e32 3036 3136 3332 2c38 2e38 3233 3438  .2061632,8.82348
-0000c850: 3439 2032 2e33 3530 3531 3031 2c39 2e31  49 2.3505101,9.1
-0000c860: 3337 3438 3239 2031 2e35 3134 3734 3731  374829 1.5147471
-0000c870: 2c39 2e30 3437 3630 3139 204d 2039 2e38  ,9.0476019 M 9.8
-0000c880: 3532 3836 3339 2c35 2e35 3835 3132 3439  528639,5.5851249
-0000c890: 2043 2039 2e38 3533 3034 3439 2c37 2e34   C 9.8530449,7.4
-0000c8a0: 3739 3334 3139 2038 2e38 3634 3936 3939  793419 8.8649699
-0000c8b0: 2c39 2e30 3135 3035 3739 2037 2e36 3436  ,9.0150579 7.646
-0000c8c0: 3035 3339 2c39 2e30 3135 3035 3739 2043  0539,9.0150579 C
-0000c8d0: 2036 2e34 3237 3133 3839 2c39 2e30 3135   6.4271389,9.015
-0000c8e0: 3035 3739 2035 2e34 3339 3036 3239 2c37  0579 5.4390629,7
-0000c8f0: 2e34 3739 3334 3139 2035 2e34 3339 3234  .4793419 5.43924
-0000c900: 3439 2c35 2e35 3835 3132 3439 2043 2035  49,5.5851249 C 5
-0000c910: 2e34 3339 3036 3239 2c33 2e36 3930 3930  .4390629,3.69090
-0000c920: 3838 2036 2e34 3237 3133 3839 2c32 2e31  88 6.4271389,2.1
-0000c930: 3535 3139 3238 2037 2e36 3436 3035 3339  551928 7.6460539
-0000c940: 2c32 2e31 3535 3139 3238 2043 2038 2e38  ,2.1551928 C 8.8
-0000c950: 3634 3936 3939 2c32 2e31 3535 3139 3238  649699,2.1551928
-0000c960: 2039 2e38 3533 3034 3439 2c33 2e36 3930   9.8530449,3.690
-0000c970: 3930 3838 2039 2e38 3532 3836 3339 2c35  9088 9.8528639,5
-0000c980: 2e35 3835 3132 3439 207a 204d 2038 2e32  .5851249 z M 8.2
-0000c990: 3538 3034 3439 2c37 2e32 3632 3739 3539  580449,7.2627959
-0000c9a0: 2043 2031 302e 3139 3832 3536 2c39 2e39   C 10.198256,9.9
-0000c9b0: 3830 3336 3739 2031 302e 3139 3832 3536  803679 10.198256
-0000c9c0: 2c39 2e39 3830 3336 3739 2031 302e 3139  ,9.9803679 10.19
-0000c9d0: 3832 3536 2c39 2e39 3830 3336 3739 2720  8256,9.9803679' 
-0000c9e0: 7374 796c 653d 276f 7061 6369 7479 3a31  style='opacity:1
-0000c9f0: 3b66 696c 6c3a 6e6f 6e65 3b66 696c 6c2d  ;fill:none;fill-
-0000ca00: 6f70 6163 6974 793a 313b 6669 6c6c 2d72  opacity:1;fill-r
-0000ca10: 756c 653a 6e6f 6e7a 6572 6f3b 7374 726f  ule:nonzero;stro
-0000ca20: 6b65 3a20 246f 7262 5f63 6f6c 6f72 5f31  ke: $orb_color_1
-0000ca30: 3434 3b73 7472 6f6b 652d 7769 6474 683a  44;stroke-width:
-0000ca40: 312e 3437 3633 3330 3634 3b73 7472 6f6b  1.47633064;strok
-0000ca50: 652d 6c69 6e65 6361 703a 6275 7474 3b73  e-linecap:butt;s
-0000ca60: 7472 6f6b 652d 6c69 6e65 6a6f 696e 3a6d  troke-linejoin:m
-0000ca70: 6974 6572 3b73 7472 6f6b 652d 6d69 7465  iter;stroke-mite
-0000ca80: 726c 696d 6974 3a34 3b73 7472 6f6b 652d  rlimit:4;stroke-
-0000ca90: 6461 7368 6172 7261 793a 6e6f 6e65 3b73  dasharray:none;s
-0000caa0: 7472 6f6b 652d 6f70 6163 6974 793a 3127  troke-opacity:1'
-0000cab0: 202f 3e3c 2f73 796d 626f 6c3e 3c73 796d   /></symbol><sym
-0000cac0: 626f 6c20 6964 3d27 6f72 6231 3530 273e  bol id='orb150'>
-0000cad0: 3c70 6174 6820 643d 274d 2031 2e31 3737  <path d='M 1.177
-0000cae0: 3134 3736 2c33 2e38 3336 3535 3232 2043  1476,3.8365522 C
-0000caf0: 2034 2e36 3837 3130 322c 332e 3832 3732   4.687102,3.8272
-0000cb00: 3933 3620 382e 3139 3730 3536 322c 332e  936 8.1970562,3.
-0000cb10: 3831 3830 3335 3320 3131 2e37 3037 3031  8180353 11.70701
-0000cb20: 312c 332e 3830 3837 3736 3720 4d20 3130  1,3.8087767 M 10
-0000cb30: 2e39 3732 3537 392c 392e 3231 3038 3334  .972579,9.210834
-0000cb40: 3120 4320 392e 3333 3938 3030 322c 372e  1 C 9.3398002,7.
-0000cb50: 3439 3634 3136 3120 372e 3730 3730 3232  4964161 7.707022
-0000cb60: 322c 352e 3738 3139 3938 3920 362e 3037  2,5.7819989 6.07
-0000cb70: 3432 3433 342c 342e 3036 3735 3831 3320  42434,4.0675813 
-0000cb80: 4d20 312e 3636 3537 3431 2c39 2e32 3130  M 1.665741,9.210
-0000cb90: 3833 3431 2043 2033 2e31 3930 3836 3536  8341 C 3.1908656
-0000cba0: 2c37 2e33 3939 3938 3131 2034 2e37 3135  ,7.3999811 4.715
-0000cbb0: 3939 3034 2c35 2e35 3839 3132 3739 2036  9904,5.5891279 6
-0000cbc0: 2e32 3431 3131 352c 332e 3737 3832 3734  .241115,3.778274
-0000cbd0: 3827 2073 7479 6c65 3d27 6f70 6163 6974  8' style='opacit
-0000cbe0: 793a 313b 6669 6c6c 3a6e 6f6e 653b 6669  y:1;fill:none;fi
-0000cbf0: 6c6c 2d6f 7061 6369 7479 3a31 3b66 696c  ll-opacity:1;fil
-0000cc00: 6c2d 7275 6c65 3a6e 6f6e 7a65 726f 3b73  l-rule:nonzero;s
-0000cc10: 7472 6f6b 653a 2024 6f72 625f 636f 6c6f  troke: $orb_colo
-0000cc20: 725f 3135 303b 7374 726f 6b65 2d77 6964  r_150;stroke-wid
-0000cc30: 7468 3a31 2e34 3736 3333 3036 343b 7374  th:1.47633064;st
-0000cc40: 726f 6b65 2d6c 696e 6563 6170 3a62 7574  roke-linecap:but
-0000cc50: 743b 7374 726f 6b65 2d6c 696e 656a 6f69  t;stroke-linejoi
-0000cc60: 6e3a 6d69 7465 723b 7374 726f 6b65 2d6d  n:miter;stroke-m
-0000cc70: 6974 6572 6c69 6d69 743a 343b 7374 726f  iterlimit:4;stro
-0000cc80: 6b65 2d64 6173 6861 7272 6179 3a6e 6f6e  ke-dasharray:non
-0000cc90: 653b 7374 726f 6b65 2d6f 7061 6369 7479  e;stroke-opacity
-0000cca0: 3a31 2720 2f3e 3c2f 7379 6d62 6f6c 3e3c  :1' /></symbol><
-0000ccb0: 7379 6d62 6f6c 2069 643d 276f 7262 3138  symbol id='orb18
-0000ccc0: 3027 3e3c 7061 7468 2064 3d27 4d20 352e  0'><path d='M 5.
-0000ccd0: 3234 3634 3133 372c 392e 3130 3234 3131  2464137,9.102411
-0000cce0: 3420 4320 352e 3236 3037 3636 372c 3130  4 C 5.2607667,10
-0000ccf0: 2e30 3233 3133 2034 2e36 3432 3430 3437  .02313 4.6424047
-0000cd00: 2c31 302e 3931 3137 3536 2033 2e37 3736  ,10.911756 3.776
-0000cd10: 3736 3637 2c31 312e 3232 3337 3335 2043  7667,11.223735 C
-0000cd20: 2033 2e30 3034 3330 3037 2c31 312e 3531   3.0043007,11.51
-0000cd30: 3435 3232 2032 2e30 3735 3639 3037 2c31  4522 2.0756907,1
-0000cd40: 312e 3334 3537 3133 2031 2e34 3637 3831  1.345713 1.46781
-0000cd50: 3637 2c31 302e 3738 3238 3836 2043 2030  67,10.782886 C 0
-0000cd60: 2e38 3730 3632 3836 372c 3130 2e32 3437  .87062867,10.247
-0000cd70: 3436 2030 2e35 3930 3735 3036 372c 392e  46 0.59075067,9.
-0000cd80: 3338 3138 3039 3220 302e 3737 3730 3735  3818092 0.777075
-0000cd90: 3637 2c38 2e35 3939 3536 3134 2043 2030  67,8.5995614 C 0
-0000cda0: 2e39 3538 3732 3836 372c 372e 3739 3230  .95872867,7.7920
-0000cdb0: 3834 3320 312e 3631 3235 3535 372c 372e  843 1.6125557,7.
-0000cdc0: 3130 3734 3433 3420 322e 3431 3934 3135  1074434 2.419415
-0000cdd0: 372c 362e 3930 3939 3230 3520 4320 332e  7,6.9099205 C 3.
-0000cde0: 3139 3030 3632 372c 362e 3731 3036 3820  1900627,6.71068 
-0000cdf0: 342e 3036 3231 3331 372c 362e 3934 3534  4.0621317,6.9454
-0000ce00: 3936 3620 342e 3631 3030 3837 372c 372e  966 4.6100877,7.
-0000ce10: 3532 3831 3035 3820 4320 352e 3031 3239  5281058 C 5.0129
-0000ce20: 3535 372c 372e 3934 3533 3531 3620 352e  557,7.9453516 5.
-0000ce30: 3235 3137 3934 372c 382e 3532 3130 3139  2517947,8.521019
-0000ce40: 3420 352e 3234 3634 3133 372c 392e 3130  4 5.2464137,9.10
-0000ce50: 3234 3131 3420 7a20 4d20 3131 2e32 3436  24114 z M 11.246
-0000ce60: 3431 342c 332e 3130 3234 3132 3920 4320  414,3.1024129 C 
-0000ce70: 3131 2e32 3630 3736 352c 342e 3032 3331  11.260765,4.0231
-0000ce80: 3331 3720 3130 2e36 3432 3430 342c 342e  317 10.642404,4.
-0000ce90: 3931 3137 3537 3420 392e 3737 3637 3635  9117574 9.776765
-0000cea0: 372c 352e 3232 3337 3336 3120 4320 392e  7,5.2237361 C 9.
-0000ceb0: 3030 3432 3939 372c 352e 3531 3435 3233  0042997,5.514523
-0000cec0: 3820 382e 3037 3536 3839 372c 352e 3334  8 8.0756897,5.34
-0000ced0: 3537 3133 3520 372e 3436 3738 3134 372c  57135 7.4678147,
-0000cee0: 342e 3738 3238 3837 3320 4320 362e 3837  4.7828873 C 6.87
-0000cef0: 3036 3237 372c 342e 3234 3734 3631 3320  06277,4.2474613 
-0000cf00: 362e 3539 3037 3439 372c 332e 3338 3138  6.5907497,3.3818
-0000cf10: 3120 362e 3737 3730 3734 372c 322e 3539  1 6.7770747,2.59
-0000cf20: 3935 3632 3420 4320 362e 3935 3837 3236  95624 C 6.958726
-0000cf30: 372c 312e 3739 3230 3835 3320 372e 3631  7,1.7920853 7.61
-0000cf40: 3235 3534 372c 312e 3130 3734 3434 3520  25547,1.1074445 
-0000cf50: 382e 3431 3934 3134 372c 302e 3930 3939  8.4194147,0.9099
-0000cf60: 3231 3520 4320 392e 3139 3030 3631 372c  215 C 9.1900617,
-0000cf70: 302e 3731 3036 3831 3220 3130 2e30 3632  0.7106812 10.062
-0000cf80: 3133 2c30 2e39 3435 3439 3832 2031 302e  13,0.9454982 10.
-0000cf90: 3631 3030 3837 2c31 2e35 3238 3130 3733  610087,1.5281073
-0000cfa0: 2043 2031 312e 3031 3239 3535 2c31 2e39   C 11.012955,1.9
-0000cfb0: 3435 3335 3239 2031 312e 3235 3137 3934  453529 11.251794
-0000cfc0: 2c32 2e35 3231 3032 3036 2031 312e 3234  ,2.5210206 11.24
-0000cfd0: 3634 3134 2c33 2e31 3032 3431 3239 207a  6414,3.1024129 z
-0000cfe0: 204d 2034 2e35 3038 3234 3937 2c37 2e35   M 4.5082497,7.5
-0000cff0: 3738 3734 3320 4320 352e 3533 3438 3533  78743 C 5.534853
-0000d000: 372c 362e 3539 3435 3232 3620 362e 3536  7,6.5945226 6.56
-0000d010: 3134 3537 372c 352e 3631 3033 3032 3220  14577,5.6103022 
-0000d020: 372e 3538 3830 3631 372c 342e 3632 3630  7.5880617,4.6260
-0000d030: 3831 3827 2073 7479 6c65 3d27 6f70 6163  818' style='opac
-0000d040: 6974 793a 313b 6669 6c6c 3a6e 6f6e 653b  ity:1;fill:none;
-0000d050: 6669 6c6c 2d6f 7061 6369 7479 3a31 3b66  fill-opacity:1;f
-0000d060: 696c 6c2d 7275 6c65 3a6e 6f6e 7a65 726f  ill-rule:nonzero
-0000d070: 3b73 7472 6f6b 653a 2024 6f72 625f 636f  ;stroke: $orb_co
-0000d080: 6c6f 725f 3138 303b 7374 726f 6b65 2d77  lor_180;stroke-w
-0000d090: 6964 7468 3a31 2e34 3736 3333 3036 343b  idth:1.47633064;
-0000d0a0: 7374 726f 6b65 2d6c 696e 6563 6170 3a62  stroke-linecap:b
-0000d0b0: 7574 743b 7374 726f 6b65 2d6c 696e 656a  utt;stroke-linej
-0000d0c0: 6f69 6e3a 6d69 7465 723b 7374 726f 6b65  oin:miter;stroke
-0000d0d0: 2d6d 6974 6572 6c69 6d69 743a 343b 7374  -miterlimit:4;st
-0000d0e0: 726f 6b65 2d64 6173 6861 7272 6179 3a6e  roke-dasharray:n
-0000d0f0: 6f6e 653b 7374 726f 6b65 2d6f 7061 6369  one;stroke-opaci
-0000d100: 7479 3a31 2720 2f3e 3c2f 7379 6d62 6f6c  ty:1' /></symbol
-0000d110: 3e3c 212d 2d20 7265 7472 6f67 7261 6465  ><!-- retrograde
-0000d120: 2073 796d 626f 6c20 2831 3278 3132 2920   symbol (12x12) 
-0000d130: 2d2d 3e3c 7379 6d62 6f6c 2069 643d 2772  --><symbol id='r
-0000d140: 6574 726f 6772 6164 6527 3e3c 7061 7468  etrograde'><path
-0000d150: 2064 3d27 4d20 352e 3136 3935 3038 392c   d='M 5.1695089,
-0000d160: 302e 3036 3531 3433 3037 2043 2033 2e37  0.06514307 C 3.7
-0000d170: 3539 3739 3839 2c30 2e32 3135 3937 3230  597989,0.2159720
-0000d180: 3720 322e 3333 3137 3334 392c 302e 3333  7 2.3317349,0.33
-0000d190: 3134 3930 3037 2030 2e39 3133 3538 3139  149007 0.9135819
-0000d1a0: 312c 302e 3233 3531 3331 3037 2043 2031  1,0.23513107 C 1
-0000d1b0: 2e35 3439 3033 3239 2c30 2e38 3139 3032  .5490329,0.81902
-0000d1c0: 3230 3720 312e 3430 3234 3834 392c 312e  207 1.4024849,1.
-0000d1d0: 3731 3030 3031 3120 312e 3432 3238 3337  7100011 1.422837
-0000d1e0: 392c 322e 3437 3030 3433 3120 4320 312e  9,2.4700431 C 1.
-0000d1f0: 3431 3734 3135 392c 352e 3231 3734 3438  4174159,5.217448
-0000d200: 3120 312e 3433 3337 3730 392c 372e 3936  1 1.4337709,7.96
-0000d210: 3532 3733 3120 312e 3431 3435 3031 392c  52731 1.4145019,
-0000d220: 3130 2e37 3132 3431 3120 4320 312e 3531  10.712411 C 1.51
-0000d230: 3439 3430 392c 3131 2e31 3730 3834 3820  49409,11.170848 
-0000d240: 302e 3936 3739 3937 3931 2c31 312e 3833  0.96799791,11.83
-0000d250: 3434 3731 2030 2e39 3032 3834 3639 312c  4471 0.90284691,
-0000d260: 3131 2e39 3634 3330 3220 4320 312e 3939  11.964302 C 1.99
-0000d270: 3736 3838 392c 3131 2e39 3634 3330 3220  76889,11.964302 
-0000d280: 332e 3039 3235 3239 392c 3131 2e39 3634  3.0925299,11.964
-0000d290: 3330 3220 342e 3138 3733 3731 392c 3131  302 4.1873719,11
-0000d2a0: 2e39 3634 3330 3220 4320 332e 3630 3138  .964302 C 3.6018
-0000d2b0: 3433 392c 3131 2e35 3737 3937 3520 332e  439,11.577975 3.
-0000d2c0: 3635 3130 3932 392c 3130 2e38 3230 3033  6510929,10.82003
-0000d2d0: 3420 332e 3634 3137 3339 392c 3130 2e32  4 3.6417399,10.2
-0000d2e0: 3139 3833 3820 4320 332e 3634 3137 3339  19838 C 3.641739
-0000d2f0: 392c 382e 3839 3734 3630 3120 332e 3634  9,8.8974601 3.64
-0000d300: 3137 3339 392c 372e 3537 3530 3833 3120  17399,7.5750831 
-0000d310: 332e 3634 3137 3339 392c 362e 3235 3237  3.6417399,6.2527
-0000d320: 3035 3120 4320 342e 3530 3236 3235 392c  051 C 4.5026259,
-0000d330: 372e 3339 3732 3931 3120 352e 3336 3335  7.3972911 5.3635
-0000d340: 3130 392c 382e 3534 3138 3737 3120 362e  109,8.5418771 6.
-0000d350: 3232 3433 3935 392c 392e 3638 3634 3633  2243959,9.686463
-0000d360: 3120 4320 352e 3630 3330 3639 392c 3130  1 C 5.6030699,10
-0000d370: 2e30 3133 3034 3920 352e 3037 3231 3433  .013049 5.072143
-0000d380: 392c 3130 2e34 3937 3335 3420 342e 3336  9,10.497354 4.36
-0000d390: 3932 3438 392c 3130 2e36 3732 3339 3320  92489,10.672393 
-0000d3a0: 4320 342e 3537 3533 3736 392c 3130 2e39  C 4.5753769,10.9
-0000d3b0: 3535 3730 3620 342e 3738 3135 3033 392c  55706 4.7815039,
-0000d3c0: 3131 2e32 3339 3032 2034 2e39 3837 3633  11.23902 4.98763
-0000d3d0: 3139 2c31 312e 3532 3233 3333 2043 2035  19,11.522333 C 5
-0000d3e0: 2e34 3933 3932 3139 2c31 312e 3031 3830  .4939219,11.0180
-0000d3f0: 3336 2036 2e31 3432 3633 3839 2c31 302e  36 6.1426389,10.
-0000d400: 3637 3232 3138 2036 2e37 3333 3635 3239  672218 6.7336529
-0000d410: 2c31 302e 3236 3434 3231 2043 2037 2e33  ,10.264421 C 7.3
-0000d420: 3839 3730 3339 2c31 312e 3231 3639 3132  897039,11.216912
-0000d430: 2038 2e34 3639 3734 3739 2c31 322e 3034   8.4697479,12.04
-0000d440: 3833 3932 2039 2e37 3431 3933 3939 2c31  8392 9.7419399,1
-0000d450: 322e 3031 3135 3739 2043 2031 302e 3134  2.011579 C 10.14
-0000d460: 3336 3033 2c31 322e 3030 3231 3939 2031  3603,12.002199 1
-0000d470: 312e 3036 3736 3931 2c31 312e 3838 3538  1.067691,11.8858
-0000d480: 3234 2031 312e 3036 3337 3735 2c31 312e  24 11.063775,11.
-0000d490: 3637 3630 3735 2043 2039 2e39 3030 3439  676075 C 9.90049
-0000d4a0: 3639 2c31 312e 3132 3830 3534 2039 2e30  69,11.128054 9.0
-0000d4b0: 3031 3838 3439 2c31 302e 3137 3930 3835  018849,10.179085
-0000d4c0: 2038 2e34 3036 3932 3239 2c39 2e31 3038   8.4069229,9.108
-0000d4d0: 3530 3431 2043 2038 2e39 3637 3034 3339  5041 C 8.9670439
-0000d4e0: 2c38 2e36 3735 3636 3431 2039 2e35 3035  ,8.6756641 9.505
-0000d4f0: 3632 3839 2c38 2e31 3837 3030 3531 2031  6289,8.1870051 1
-0000d500: 302e 3137 3733 3832 2c37 2e39 3038 3637  0.177382,7.90867
-0000d510: 3331 2043 2031 302e 3431 3938 3831 2c37  31 C 10.419881,7
-0000d520: 2e38 3636 3135 3031 2031 302e 3033 3136  .8661501 10.0316
-0000d530: 3638 2c37 2e35 3736 3335 3731 2039 2e39  68,7.5763571 9.9
-0000d540: 3831 3530 3339 2c37 2e34 3139 3039 3531  815039,7.4190951
-0000d550: 2043 2039 2e37 3839 3630 3839 2c36 2e39   C 9.7896089,6.9
-0000d560: 3036 3239 3331 2039 2e36 3231 3433 3739  062931 9.6214379
-0000d570: 2c37 2e34 3639 3436 3631 2039 2e32 3935  ,7.4694661 9.295
-0000d580: 3038 3339 2c37 2e36 3233 3934 3531 2043  0839,7.6239451 C
-0000d590: 2038 2e38 3435 3339 3839 2c37 2e38 3932   8.8453989,7.892
-0000d5a0: 3736 3831 2038 2e33 3037 3838 3339 2c38  7681 8.3078839,8
-0000d5b0: 2e33 3634 3630 3131 2037 2e38 3631 3434  .3646011 7.86144
-0000d5c0: 3539 2c38 2e34 3435 3433 3531 2043 2037  59,8.4454351 C 7
-0000d5d0: 2e32 3535 3133 3639 2c37 2e35 3839 3836  .2551369,7.58986
-0000d5e0: 3731 2036 2e36 3438 3832 3739 2c36 2e37  71 6.6488279,6.7
-0000d5f0: 3334 3239 3931 2036 2e30 3432 3531 3939  342991 6.0425199
-0000d600: 2c35 2e38 3738 3733 3231 2043 2037 2e32  ,5.8787321 C 7.2
-0000d610: 3435 3139 3339 2c35 2e36 3137 3433 3531  451939,5.6174351
-0000d620: 2038 2e35 3832 3738 3339 2c35 2e30 3835   8.5827839,5.085
-0000d630: 3338 3931 2039 2e30 3730 3434 3039 2c33  3891 9.0704409,3
-0000d640: 2e39 3336 3839 3831 2043 2039 2e34 3036  .9368981 C 9.406
-0000d650: 3331 3339 2c33 2e31 3132 3032 3131 2039  3139,3.1120211 9
-0000d660: 2e32 3633 3733 3339 2c32 2e31 3636 3739  .2637339,2.16679
-0000d670: 3331 2038 2e39 3130 3738 3839 2c31 2e33  31 8.9107889,1.3
-0000d680: 3733 3437 3031 2043 2038 2e31 3638 3438  734701 C 8.16848
-0000d690: 3639 2c30 2e34 3130 3931 3130 3720 362e  69,0.41091107 6.
-0000d6a0: 3836 3932 3034 392c 2d30 2e30 3732 3435  8692049,-0.07245
-0000d6b0: 3139 3331 2035 2e36 3139 3937 3239 2c30  1931 5.6199729,0
-0000d6c0: 2e30 3235 3130 3630 3720 4320 352e 3436  .02510607 C 5.46
-0000d6d0: 3933 3237 392c 302e 3033 3238 3732 3037  93279,0.03287207
-0000d6e0: 2035 2e33 3139 3035 3139 2c30 2e30 3436   5.3190519,0.046
-0000d6f0: 3531 3030 3720 352e 3136 3935 3038 392c  51007 5.1695089,
-0000d700: 302e 3036 3531 3433 3037 204c 2035 2e31  0.06514307 L 5.1
-0000d710: 3639 3530 3839 2c30 2e30 3635 3134 3330  695089,0.0651430
-0000d720: 3720 7a20 4d20 342e 3030 3534 3934 392c  7 z M 4.0054949,
-0000d730: 302e 3938 3330 3738 3036 2043 2034 2e39  0.98307806 C 4.9
-0000d740: 3237 3432 3039 2c30 2e38 3735 3136 3030  274209,0.8751600
-0000d750: 3720 362e 3037 3532 3833 392c 302e 3935  7 6.0752839,0.95
-0000d760: 3635 3934 3036 2036 2e36 3131 3934 3639  659406 6.6119469
-0000d770: 2c31 2e37 3736 3938 3231 2043 2037 2e31  ,1.7769821 C 7.1
-0000d780: 3939 3534 3839 2c32 2e37 3433 3632 3331  995489,2.7436231
-0000d790: 2036 2e39 3737 3137 3739 2c34 2e30 3237   6.9771779,4.027
-0000d7a0: 3732 3431 2036 2e32 3338 3838 3539 2c34  7241 6.2388859,4
-0000d7b0: 2e38 3639 3430 3031 2043 2035 2e36 3035  .8694001 C 5.605
-0000d7c0: 3332 3839 2c35 2e35 3534 3930 3331 2034  3289,5.5549031 4
-0000d7d0: 2e35 3532 3130 3539 2c35 2e36 3738 3037  .5521059,5.67807
-0000d7e0: 3731 2033 2e36 3431 3733 3939 2c35 2e35  71 3.6417399,5.5
-0000d7f0: 3732 3735 3331 2043 2033 2e36 3431 3733  727531 C 3.64173
-0000d800: 3939 2c34 2e30 3635 3532 3731 2033 2e36  99,4.0655271 3.6
-0000d810: 3431 3733 3939 2c32 2e35 3538 3330 3031  417399,2.5583001
-0000d820: 2033 2e36 3431 3733 3939 2c31 2e30 3531   3.6417399,1.051
-0000d830: 3037 3331 2043 2033 2e37 3632 3939 3139  0731 C 3.7629919
-0000d840: 2c31 2e30 3238 3430 3831 2033 2e38 3834  ,1.0284081 3.884
-0000d850: 3234 3239 2c31 2e30 3035 3734 3331 2034  2429,1.0057431 4
-0000d860: 2e30 3035 3439 3439 2c30 2e39 3833 3037  .0054949,0.98307
-0000d870: 3830 3620 7a27 2073 7479 6c65 3d27 6669  806 z' style='fi
-0000d880: 6c6c 3a24 7061 7065 725f 636f 6c6f 725f  ll:$paper_color_
-0000d890: 303b 2720 2f3e 3c2f 7379 6d62 6f6c 3e3c  0;' /></symbol><
-0000d8a0: 6720 7472 616e 7366 6f72 6d3d 2774 7261  g transform='tra
-0000d8b0: 6e73 6c61 7465 2835 302c 3530 2927 3e3c  nslate(50,50)'><
-0000d8c0: 6720 7472 616e 7366 6f72 6d3d 2774 7261  g transform='tra
-0000d8d0: 6e73 6c61 7465 2824 6369 7263 6c65 582c  nslate($circleX,
-0000d8e0: 2463 6972 636c 6559 2927 3e3c 212d 2d20  $circleY)'><!-- 
-0000d8f0: 5a6f 6469 6163 202d 2d3e 246d 616b 655a  Zodiac -->$makeZ
-0000d900: 6f64 6961 633c 212d 2d20 4669 7273 7420  odiac<!-- First 
-0000d910: 4369 7263 6c65 202d 2d3e 3c63 6972 636c  Circle --><circl
-0000d920: 6520 2463 3120 7374 796c 653d 2724 6331  e $c1 style='$c1
-0000d930: 7374 796c 6527 202f 3e3c 212d 2d20 5365  style' /><!-- Se
-0000d940: 636f 6e64 2043 6972 636c 6520 2d2d 3e3c  cond Circle --><
-0000d950: 6369 7263 6c65 2024 6332 2073 7479 6c65  circle $c2 style
-0000d960: 3d27 2463 3273 7479 6c65 2720 2f3e 3c21  ='$c2style' /><!
-0000d970: 2d2d 2054 6869 7264 2043 6972 636c 6520  -- Third Circle 
-0000d980: 2d2d 3e3c 6369 7263 6c65 2024 6333 2073  --><circle $c3 s
-0000d990: 7479 6c65 3d27 2463 3373 7479 6c65 2720  tyle='$c3style' 
-0000d9a0: 2f3e 3c21 2d2d 2054 7261 6e73 6974 5269  /><!-- TransitRi
-0000d9b0: 6e67 202d 2d3e 2474 7261 6e73 6974 5269  ng -->$transitRi
-0000d9c0: 6e67 3c21 2d2d 2044 6567 7265 6520 5269  ng<!-- Degree Ri
-0000d9d0: 6e67 202d 2d3e 2464 6567 7265 6552 696e  ng -->$degreeRin
-0000d9e0: 673c 212d 2d20 486f 7573 6573 202d 2d3e  g<!-- Houses -->
-0000d9f0: 246d 616b 6548 6f75 7365 733c 212d 2d20  $makeHouses<!-- 
-0000da00: 506c 616e 6574 7320 2d2d 3e24 6d61 6b65  Planets -->$make
-0000da10: 506c 616e 6574 733c 212d 2d20 4173 7065  Planets<!-- Aspe
-0000da20: 6374 7320 2d2d 3e24 6d61 6b65 4173 7065  cts -->$makeAspe
-0000da30: 6374 733c 2f67 3e3c 2f67 3e3c 212d 2d20  cts</g></g><!-- 
-0000da40: 7465 7374 696e 6720 7072 696e 7465 723c  testing printer<
-0000da50: 7265 6374 2078 3d27 3027 2079 3d27 3027  rect x='0' y='0'
-0000da60: 2077 6964 7468 3d27 3737 322e 3227 2068   width='772.2' h
-0000da70: 6569 6768 743d 2735 3436 2e30 2720 7374  eight='546.0' st
-0000da80: 796c 653d 2766 696c 6c3a 2024 7061 7065  yle='fill: $pape
-0000da90: 725f 636f 6c6f 725f 313b 2073 7472 6f6b  r_color_1; strok
-0000daa0: 652d 7769 6474 683a 2031 7078 3b20 7374  e-width: 1px; st
-0000dab0: 726f 6b65 3a72 6564 3b27 202f 3e3c 6c69  roke:red;' /><li
-0000dac0: 6e65 2078 313d 2730 2720 7931 3d27 3027  ne x1='0' y1='0'
-0000dad0: 2078 323d 2737 3732 2e32 2720 7932 3d27   x2='772.2' y2='
-0000dae0: 3534 362e 3027 2073 7479 6c65 3d27 6669  546.0' style='fi
-0000daf0: 6c6c 3a6e 6f6e 653b 2073 7472 6f6b 652d  ll:none; stroke-
-0000db00: 7769 6474 683a 2031 7078 3b20 7374 726f  width: 1px; stro
-0000db10: 6b65 3a72 6564 3b27 202f 3e3c 6c69 6e65  ke:red;' /><line
-0000db20: 2078 313d 2737 3732 2e32 2720 7931 3d27   x1='772.2' y1='
-0000db30: 3027 2078 323d 2730 2720 7932 3d27 3534  0' x2='0' y2='54
-0000db40: 362e 3027 2073 7479 6c65 3d27 6669 6c6c  6.0' style='fill
-0000db50: 3a6e 6f6e 653b 2073 7472 6f6b 652d 7769  :none; stroke-wi
-0000db60: 6474 683a 2031 7078 3b20 7374 726f 6b65  dth: 1px; stroke
-0000db70: 3a72 6564 3b27 202f 3e2d 2d3e 3c2f 673e  :red;' />--></g>
-0000db80: 3c2f 673e 3c2f 673e 3c21 2d2d 2074 6573  </g></g><!-- tes
-0000db90: 7469 6e67 2070 7269 6e74 6572 3c72 6563  ting printer<rec
-0000dba0: 7420 783d 2730 2720 793d 2730 2720 7769  t x='0' y='0' wi
-0000dbb0: 6474 683d 2724 7376 6757 6964 7468 2720  dth='$svgWidth' 
-0000dbc0: 6865 6967 6874 3d27 2473 7667 4865 6967  height='$svgHeig
-0000dbd0: 6874 2720 7374 796c 653d 2766 696c 6c3a  ht' style='fill:
-0000dbe0: 6e6f 6e65 3b20 7374 726f 6b65 2d77 6964  none; stroke-wid
-0000dbf0: 7468 3a20 3170 783b 2073 7472 6f6b 653a  th: 1px; stroke:
-0000dc00: 626c 7565 3b27 202f 3e3c 6c69 6e65 2078  blue;' /><line x
-0000dc10: 313d 2730 2720 7931 3d27 3027 2078 323d  1='0' y1='0' x2=
-0000dc20: 2724 7376 6757 6964 7468 2720 7932 3d27  '$svgWidth' y2='
-0000dc30: 2473 7667 4865 6967 6874 2720 7374 796c  $svgHeight' styl
-0000dc40: 653d 2766 696c 6c3a 6e6f 6e65 3b20 7374  e='fill:none; st
-0000dc50: 726f 6b65 2d77 6964 7468 3a20 3170 783b  roke-width: 1px;
-0000dc60: 2073 7472 6f6b 653a 626c 7565 3b27 202f   stroke:blue;' /
-0000dc70: 3e3c 6c69 6e65 2078 313d 2724 7376 6757  ><line x1='$svgW
-0000dc80: 6964 7468 2720 7931 3d27 3027 2078 323d  idth' y1='0' x2=
-0000dc90: 2730 2720 7932 3d27 2473 7667 4865 6967  '0' y2='$svgHeig
-0000dca0: 6874 2720 7374 796c 653d 2766 696c 6c3a  ht' style='fill:
-0000dcb0: 6e6f 6e65 3b20 7374 726f 6b65 2d77 6964  none; stroke-wid
-0000dcc0: 7468 3a20 3170 783b 2073 7472 6f6b 653a  th: 1px; stroke:
-0000dcd0: 626c 7565 3b27 202f 3e2d 2d3e 3c2f 7376  blue;' />--></sv
-0000dce0: 673e                                     g>
+00000020: 462d 3827 3f3e 0a3c 2144 4f43 5459 5045  F-8'?>.<!DOCTYPE
+00000030: 2073 7667 2050 5542 4c49 4320 272d 2f2f   svg PUBLIC '-//
+00000040: 5733 432f 2f44 5444 2053 5647 2031 2e31  W3C//DTD SVG 1.1
+00000050: 2f2f 454e 2720 2768 7474 703a 2f2f 7777  //EN' 'http://ww
+00000060: 772e 7733 2e6f 7267 2f47 7261 7068 6963  w.w3.org/Graphic
+00000070: 732f 5356 472f 312e 312f 4454 442f 7376  s/SVG/1.1/DTD/sv
+00000080: 6731 312e 6474 6427 3e0a 3c21 2d2d 2d0a  g11.dtd'>.<!---.
+00000090: 5468 6973 2066 696c 6520 6973 2070 6172  This file is par
+000000a0: 7420 6f66 204b 6572 796b 6569 6f6e 2061  t of Kerykeion a
+000000b0: 6e64 2069 7320 6261 7365 6420 6f6e 204f  nd is based on O
+000000c0: 7065 6e41 7374 726f 2e6f 7267 202d 2d3e  penAstro.org -->
+000000d0: 0a3c 7376 670a 2020 2020 786d 6c6e 733d  .<svg.    xmlns=
+000000e0: 2268 7474 703a 2f2f 7777 772e 7733 2e6f  "http://www.w3.o
+000000f0: 7267 2f32 3030 302f 7376 6722 0a20 2020  rg/2000/svg".   
+00000100: 2078 6d6c 6e73 3a78 6c69 6e6b 3d22 6874   xmlns:xlink="ht
+00000110: 7470 3a2f 2f77 7777 2e77 332e 6f72 672f  tp://www.w3.org/
+00000120: 3139 3939 2f78 6c69 6e6b 220a 2020 2020  1999/xlink".    
+00000130: 7769 6474 683d 2224 7376 6757 6964 7468  width="$svgWidth
+00000140: 220a 2020 2020 6865 6967 6874 3d22 2473  ".    height="$s
+00000150: 7667 4865 6967 6874 220a 2020 2020 7669  vgHeight".    vi
+00000160: 6577 426f 783d 2224 7669 6577 626f 7822  ewBox="$viewbox"
+00000170: 0a20 2020 2070 7265 7365 7276 6541 7370  .    preserveAsp
+00000180: 6563 7452 6174 696f 3d22 784d 6964 594d  ectRatio="xMidYM
+00000190: 6964 220a 3e0a 2020 2020 3c74 6974 6c65  id".>.    <title
+000001a0: 3e4b 6572 796b 6569 6f6e 3c2f 7469 746c  >Kerykeion</titl
+000001b0: 653e 0a20 2020 203c 6720 7472 616e 7366  e>.    <g transf
+000001c0: 6f72 6d3d 2274 7261 6e73 6c61 7465 2824  orm="translate($
+000001d0: 6366 6754 7261 6e73 6c61 7465 2922 3e0a  cfgTranslate)">.
+000001e0: 2020 2020 2020 2020 3c67 2074 7261 6e73          <g trans
+000001f0: 666f 726d 3d22 726f 7461 7465 2824 6366  form="rotate($cf
+00000200: 6752 6f74 6174 6529 223e 0a20 2020 2020  gRotate)">.     
+00000210: 2020 2020 2020 203c 6720 7472 616e 7366         <g transf
+00000220: 6f72 6d3d 2273 6361 6c65 2824 6366 675a  orm="scale($cfgZ
+00000230: 6f6f 6d29 223e 0a20 2020 2020 2020 2020  oom)">.         
+00000240: 2020 2020 2020 203c 7265 6374 2078 3d22         <rect x="
+00000250: 3022 2079 3d22 3022 2077 6964 7468 3d22  0" y="0" width="
+00000260: 2463 6861 7274 5f77 6964 7468 2220 6865  $chart_width" he
+00000270: 6967 6874 3d22 3534 362e 3022 2073 7479  ight="546.0" sty
+00000280: 6c65 3d22 6669 6c6c 3a20 2470 6170 6572  le="fill: $paper
+00000290: 5f63 6f6c 6f72 5f31 2220 2f3e 0a20 2020  _color_1" />.   
+000002a0: 2020 2020 2020 2020 2020 2020 203c 7465               <te
+000002b0: 7874 2078 3d22 3230 2220 793d 2233 3022  xt x="20" y="30"
+000002c0: 2073 7479 6c65 3d22 6669 6c6c 3a20 2470   style="fill: $p
+000002d0: 6170 6572 5f63 6f6c 6f72 5f30 3b20 666f  aper_color_0; fo
+000002e0: 6e74 2d73 697a 653a 2032 3470 7822 3e24  nt-size: 24px">$
+000002f0: 7374 7269 6e67 5469 746c 653c 2f74 6578  stringTitle</tex
+00000300: 743e 0a20 2020 2020 2020 2020 2020 2020  t>.             
+00000310: 2020 203c 7465 7874 2078 3d22 3230 2220     <text x="20" 
+00000320: 793d 2235 3022 2073 7479 6c65 3d22 6669  y="50" style="fi
+00000330: 6c6c 3a20 2470 6170 6572 5f63 6f6c 6f72  ll: $paper_color
+00000340: 5f30 3b20 666f 6e74 2d73 697a 653a 2031  _0; font-size: 1
+00000350: 3170 7822 3e24 7374 7269 6e67 4e61 6d65  1px">$stringName
+00000360: 3c2f 7465 7874 3e0a 2020 2020 2020 2020  </text>.        
+00000370: 2020 2020 2020 2020 3c74 6578 7420 783d          <text x=
+00000380: 2232 3022 2079 3d22 3632 2220 7374 796c  "20" y="62" styl
+00000390: 653d 2266 696c 6c3a 2024 7061 7065 725f  e="fill: $paper_
+000003a0: 636f 6c6f 725f 303b 2066 6f6e 742d 7369  color_0; font-si
+000003b0: 7a65 3a20 3131 7078 223e 2473 7472 696e  ze: 11px">$strin
+000003c0: 674c 6f63 6174 696f 6e3c 2f74 6578 743e  gLocation</text>
+000003d0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+000003e0: 203c 7465 7874 2078 3d22 3230 2220 793d   <text x="20" y=
+000003f0: 2237 3422 2073 7479 6c65 3d22 6669 6c6c  "74" style="fill
+00000400: 3a20 2470 6170 6572 5f63 6f6c 6f72 5f30  : $paper_color_0
+00000410: 3b20 666f 6e74 2d73 697a 653a 2031 3170  ; font-size: 11p
+00000420: 7822 3e24 7374 7269 6e67 4461 7465 5469  x">$stringDateTi
+00000430: 6d65 3c2f 7465 7874 3e0a 2020 2020 2020  me</text>.      
+00000440: 2020 2020 2020 2020 2020 3c74 6578 7420            <text 
+00000450: 783d 2232 3022 2079 3d22 3836 2220 7374  x="20" y="86" st
+00000460: 796c 653d 2266 696c 6c3a 2024 7061 7065  yle="fill: $pape
+00000470: 725f 636f 6c6f 725f 303b 2066 6f6e 742d  r_color_0; font-
+00000480: 7369 7a65 3a20 3131 7078 223e 2473 7472  size: 11px">$str
+00000490: 696e 674c 6174 3c2f 7465 7874 3e0a 2020  ingLat</text>.  
+000004a0: 2020 2020 2020 2020 2020 2020 2020 3c74                <t
+000004b0: 6578 7420 783d 2232 3022 2079 3d22 3938  ext x="20" y="98
+000004c0: 2220 7374 796c 653d 2266 696c 6c3a 2024  " style="fill: $
+000004d0: 7061 7065 725f 636f 6c6f 725f 303b 2066  paper_color_0; f
+000004e0: 6f6e 742d 7369 7a65 3a20 3131 7078 223e  ont-size: 11px">
+000004f0: 2473 7472 696e 674c 6f6e 3c2f 7465 7874  $stringLon</text
+00000500: 3e0a 2020 2020 2020 2020 2020 2020 2020  >.              
+00000510: 2020 3c74 6578 7420 783d 2232 3022 2079    <text x="20" y
+00000520: 3d22 3131 3022 2073 7479 6c65 3d22 6669  ="110" style="fi
+00000530: 6c6c 3a20 2470 6170 6572 5f63 6f6c 6f72  ll: $paper_color
+00000540: 5f30 3b20 666f 6e74 2d73 697a 653a 2031  _0; font-size: 1
+00000550: 3170 7822 3e24 7374 7269 6e67 506f 7369  1px">$stringPosi
+00000560: 7469 6f6e 3c2f 7465 7874 3e0a 2020 2020  tion</text>.    
+00000570: 2020 2020 2020 2020 2020 2020 3c74 6578              <tex
+00000580: 7420 783d 2232 3022 2079 3d22 3438 3022  t x="20" y="480"
+00000590: 2073 7479 6c65 3d22 6669 6c6c 3a20 2470   style="fill: $p
+000005a0: 6170 6572 5f63 6f6c 6f72 5f30 3b20 666f  aper_color_0; fo
+000005b0: 6e74 2d73 697a 653a 2031 3070 7822 3e24  nt-size: 10px">$
+000005c0: 626f 7474 6f6d 4c65 6674 313c 2f74 6578  bottomLeft1</tex
+000005d0: 743e 0a20 2020 2020 2020 2020 2020 2020  t>.             
+000005e0: 2020 203c 7465 7874 2078 3d22 3230 2220     <text x="20" 
+000005f0: 793d 2234 3934 2220 7374 796c 653d 2266  y="494" style="f
+00000600: 696c 6c3a 2024 7061 7065 725f 636f 6c6f  ill: $paper_colo
+00000610: 725f 303b 2066 6f6e 742d 7369 7a65 3a20  r_0; font-size: 
+00000620: 3130 7078 223e 2462 6f74 746f 6d4c 6566  10px">$bottomLef
+00000630: 7432 3c2f 7465 7874 3e0a 2020 2020 2020  t2</text>.      
+00000640: 2020 2020 2020 2020 2020 3c74 6578 7420            <text 
+00000650: 783d 2232 3022 2079 3d22 3530 3822 2073  x="20" y="508" s
+00000660: 7479 6c65 3d22 6669 6c6c 3a20 2470 6170  tyle="fill: $pap
+00000670: 6572 5f63 6f6c 6f72 5f30 3b20 666f 6e74  er_color_0; font
+00000680: 2d73 697a 653a 2031 3070 7822 3e24 626f  -size: 10px">$bo
+00000690: 7474 6f6d 4c65 6674 333c 2f74 6578 743e  ttomLeft3</text>
+000006a0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+000006b0: 203c 7465 7874 2078 3d22 3230 2220 793d   <text x="20" y=
+000006c0: 2235 3232 2220 7374 796c 653d 2266 696c  "522" style="fil
+000006d0: 6c3a 2024 7061 7065 725f 636f 6c6f 725f  l: $paper_color_
+000006e0: 303b 2066 6f6e 742d 7369 7a65 3a20 3130  0; font-size: 10
+000006f0: 7078 223e 2462 6f74 746f 6d4c 6566 7434  px">$bottomLeft4
+00000700: 3c2f 7465 7874 3e0a 2020 2020 2020 2020  </text>.        
+00000710: 2020 2020 2020 2020 3c21 2d2d 204c 756e          <!-- Lun
+00000720: 6172 2050 6861 7365 202d 2d3e 0a20 2020  ar Phase -->.   
+00000730: 2020 2020 2020 2020 2020 2020 203c 6720               <g 
+00000740: 7472 616e 7366 6f72 6d3d 2274 7261 6e73  transform="trans
+00000750: 6c61 7465 2832 302c 3531 3829 223e 0a20  late(20,518)">. 
+00000760: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000770: 2020 203c 6720 7472 616e 7366 6f72 6d3d     <g transform=
+00000780: 2272 6f74 6174 6528 246c 756e 6172 5f70  "rotate($lunar_p
+00000790: 6861 7365 5f72 6f74 6174 6520 3230 2031  hase_rotate 20 1
+000007a0: 3029 223e 0a20 2020 2020 2020 2020 2020  0)">.           
+000007b0: 2020 2020 2020 2020 2020 2020 203c 6465               <de
+000007c0: 6673 3e0a 2020 2020 2020 2020 2020 2020  fs>.            
+000007d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000007e0: 3c63 6c69 7050 6174 6820 6964 3d22 6375  <clipPath id="cu
+000007f0: 742d 6f66 662d 6369 7263 6c65 223e 0a20  t-off-circle">. 
+00000800: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000810: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+00000820: 6369 7263 6c65 2063 783d 2232 3022 2063  circle cx="20" c
+00000830: 793d 2231 3022 2072 3d22 3130 2220 2f3e  y="10" r="10" />
+00000840: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00000850: 2020 2020 2020 2020 2020 2020 203c 2f63               </c
+00000860: 6c69 7050 6174 683e 0a20 2020 2020 2020  lipPath>.       
+00000870: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000880: 203c 2f64 6566 733e 0a20 2020 2020 2020   </defs>.       
+00000890: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000008a0: 203c 6369 7263 6c65 2063 783d 2232 3022   <circle cx="20"
+000008b0: 2063 793d 2231 3022 2072 3d22 3130 2220   cy="10" r="10" 
+000008c0: 7374 796c 653d 2266 696c 6c3a 2024 6c75  style="fill: $lu
+000008d0: 6e61 725f 7068 6173 655f 6267 2220 2f3e  nar_phase_bg" />
+000008e0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+000008f0: 2020 2020 2020 2020 203c 6369 7263 6c65           <circle
+00000900: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00000910: 2020 2020 2020 2020 2020 2020 2063 783d               cx=
+00000920: 2224 6c75 6e61 725f 7068 6173 655f 6378  "$lunar_phase_cx
+00000930: 220a 2020 2020 2020 2020 2020 2020 2020  ".              
+00000940: 2020 2020 2020 2020 2020 2020 2020 6379                cy
+00000950: 3d22 3130 220a 2020 2020 2020 2020 2020  ="10".          
+00000960: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000970: 2020 723d 2224 6c75 6e61 725f 7068 6173    r="$lunar_phas
+00000980: 655f 7222 0a20 2020 2020 2020 2020 2020  e_r".           
+00000990: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000009a0: 2073 7479 6c65 3d22 6669 6c6c 3a20 246c   style="fill: $l
+000009b0: 756e 6172 5f70 6861 7365 5f66 6722 0a20  unar_phase_fg". 
+000009c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000009d0: 2020 2020 2020 2020 2020 2063 6c69 702d             clip-
+000009e0: 7061 7468 3d22 7572 6c28 2363 7574 2d6f  path="url(#cut-o
+000009f0: 6666 2d63 6972 636c 6529 220a 2020 2020  ff-circle)".    
+00000a00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000a10: 2020 2020 2f3e 0a20 2020 2020 2020 2020      />.         
+00000a20: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+00000a30: 6369 7263 6c65 0a20 2020 2020 2020 2020  circle.         
+00000a40: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000a50: 2020 2063 783d 2232 3022 0a20 2020 2020     cx="20".     
+00000a60: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000a70: 2020 2020 2020 2063 793d 2231 3022 0a20         cy="10". 
+00000a80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000a90: 2020 2020 2020 2020 2020 2072 3d22 3130             r="10
+00000aa0: 220a 2020 2020 2020 2020 2020 2020 2020  ".              
+00000ab0: 2020 2020 2020 2020 2020 2020 2020 7374                st
+00000ac0: 796c 653d 2266 696c 6c3a 206e 6f6e 653b  yle="fill: none;
+00000ad0: 2073 7472 6f6b 653a 2024 6c75 6e61 725f   stroke: $lunar_
+00000ae0: 7068 6173 655f 6f75 746c 696e 653b 2073  phase_outline; s
+00000af0: 7472 6f6b 652d 7769 6474 683a 2030 2e35  troke-width: 0.5
+00000b00: 7078 3b20 7374 726f 6b65 2d6f 7061 6369  px; stroke-opaci
+00000b10: 7479 3a20 302e 3522 0a20 2020 2020 2020  ty: 0.5".       
+00000b20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000b30: 202f 3e0a 2020 2020 2020 2020 2020 2020   />.            
+00000b40: 2020 2020 2020 2020 3c2f 673e 0a20 2020          </g>.   
+00000b50: 2020 2020 2020 2020 2020 2020 203c 2f67               </g
+00000b60: 3e0a 2020 2020 2020 2020 2020 2020 2020  >.              
+00000b70: 2020 3c21 2d2d 2050 6c61 6e65 7473 2028    <!-- Planets (
+00000b80: 3234 7832 3429 202d 2d3e 0a20 2020 2020  24x24) -->.     
+00000b90: 2020 2020 2020 2020 2020 203c 7379 6d62             <symb
+00000ba0: 6f6c 2069 643d 2253 756e 223e 0a20 2020  ol id="Sun">.   
+00000bb0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000bc0: 203c 6720 7472 616e 7366 6f72 6d3d 2274   <g transform="t
+00000bd0: 7261 6e73 6c61 7465 2831 2c34 2922 3e0a  ranslate(1,4)">.
+00000be0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000bf0: 2020 2020 2020 2020 3c63 6972 636c 6520          <circle 
+00000c00: 6378 3d22 3130 2220 6379 3d22 3130 2220  cx="10" cy="10" 
+00000c10: 723d 2239 220a 2020 2020 2020 2020 2020  r="9".          
+00000c20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000c30: 2020 7374 796c 653d 2266 696c 6c3a 206e    style="fill: n
+00000c40: 6f6e 653b 2073 7472 6f6b 653a 2024 706c  one; stroke: $pl
+00000c50: 616e 6574 735f 636f 6c6f 725f 303b 2073  anets_color_0; s
+00000c60: 7472 6f6b 652d 7769 6474 683a 2032 7078  troke-width: 2px
+00000c70: 2220 2f3e 0a20 2020 2020 2020 2020 2020  " />.           
+00000c80: 2020 2020 2020 2020 2020 2020 203c 6369               <ci
+00000c90: 7263 6c65 2063 783d 2231 3022 2063 793d  rcle cx="10" cy=
+00000ca0: 2231 3022 2072 3d22 3222 2073 7479 6c65  "10" r="2" style
+00000cb0: 3d22 6669 6c6c 3a20 2470 6c61 6e65 7473  ="fill: $planets
+00000cc0: 5f63 6f6c 6f72 5f30 2220 2f3e 0a20 2020  _color_0" />.   
+00000cd0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000ce0: 203c 2f67 3e0a 2020 2020 2020 2020 2020   </g>.          
+00000cf0: 2020 2020 2020 3c2f 7379 6d62 6f6c 3e0a        </symbol>.
+00000d00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000d10: 3c73 796d 626f 6c20 6964 3d22 4d6f 6f6e  <symbol id="Moon
+00000d20: 223e 0a20 2020 2020 2020 2020 2020 2020  ">.             
+00000d30: 2020 2020 2020 203c 6720 7472 616e 7366         <g transf
+00000d40: 6f72 6d3d 2274 7261 6e73 6c61 7465 2834  orm="translate(4
+00000d50: 2c33 2922 3e0a 2020 2020 2020 2020 2020  ,3)">.          
+00000d60: 2020 2020 2020 2020 2020 2020 2020 3c67                <g
+00000d70: 2074 7261 6e73 666f 726d 3d22 7363 616c   transform="scal
+00000d80: 6528 2e38 2922 3e0a 2020 2020 2020 2020  e(.8)">.        
+00000d90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000da0: 2020 2020 3c70 6174 680a 2020 2020 2020      <path.      
+00000db0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000dc0: 2020 2020 2020 2020 2020 643d 224d 2033            d="M 3
+00000dd0: 2e36 3633 3931 3934 2c31 2e30 3330 3835  .6639194,1.03085
+00000de0: 3039 2043 2032 2e37 3439 3834 3934 2c31  09 C 2.7498494,1
+00000df0: 2e30 3635 3633 3039 2031 2e38 3732 3133  .0656309 1.87213
+00000e00: 3934 2c31 2e32 3133 3932 3039 2031 2e30  94,1.2139209 1.0
+00000e10: 3238 3436 3934 2c31 2e34 3539 3338 3039  284694,1.4593809
+00000e20: 2043 2035 2e35 3732 3937 3934 2c32 2e37   C 5.5729794,2.7
+00000e30: 3939 3936 3039 2038 2e38 3931 3937 3934  999609 8.8919794
+00000e40: 2c37 2e30 3234 3232 3039 2038 2e38 3931  ,7.0242209 8.891
+00000e50: 3937 3934 2c31 322e 3030 3131 3931 2043  9794,12.001191 C
+00000e60: 2038 2e38 3931 3937 3934 2c31 362e 3937   8.8919794,16.97
+00000e70: 3831 3631 2035 2e35 3732 3937 3934 2c32  8161 5.5729794,2
+00000e80: 312e 3230 3234 3131 2031 2e30 3238 3436  1.202411 1.02846
+00000e90: 3934 2c32 322e 3534 3330 3031 2043 2032  94,22.543001 C 2
+00000ea0: 2e30 3031 3932 3934 2c32 322e 3832 3632  .0019294,22.8262
+00000eb0: 3231 2033 2e30 3237 3938 3934 2c32 322e  21 3.0279894,22.
+00000ec0: 3937 3135 3331 2034 2e30 3932 3434 3934  971531 4.0924494
+00000ed0: 2c32 322e 3937 3135 3331 2043 2031 302e  ,22.971531 C 10.
+00000ee0: 3134 3830 3739 2c32 322e 3937 3135 3331  148079,22.971531
+00000ef0: 2031 352e 3036 3237 3839 2c31 382e 3035   15.062789,18.05
+00000f00: 3638 3231 2031 352e 3036 3237 3839 2c31  6821 15.062789,1
+00000f10: 322e 3030 3131 3931 2043 2031 352e 3036  2.001191 C 15.06
+00000f20: 3237 3839 2c35 2e39 3435 3536 3039 2031  2789,5.9455609 1
+00000f30: 302e 3134 3830 3739 2c31 2e30 3330 3835  0.148079,1.03085
+00000f40: 3039 2034 2e30 3932 3434 3934 2c31 2e30  09 4.0924494,1.0
+00000f50: 3330 3835 3039 2043 2033 2e39 3530 3531  308509 C 3.95051
+00000f60: 3934 2c31 2e30 3330 3835 3039 2033 2e38  94,1.0308509 3.8
+00000f70: 3034 3534 3934 2c31 2e30 3235 3439 3039  045494,1.0254909
+00000f80: 2033 2e36 3633 3931 3934 2c31 2e30 3330   3.6639194,1.030
+00000f90: 3835 3039 207a 2022 0a20 2020 2020 2020  8509 z ".       
+00000fa0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00000fb0: 2020 2020 2020 2020 2073 7479 6c65 3d22           style="
+00000fc0: 7374 726f 6b65 3a20 2470 6c61 6e65 7473  stroke: $planets
+00000fd0: 5f63 6f6c 6f72 5f31 3b20 7374 726f 6b65  _color_1; stroke
+00000fe0: 2d77 6964 7468 3a20 3270 783b 2066 696c  -width: 2px; fil
+00000ff0: 6c3a 206e 6f6e 6522 0a20 2020 2020 2020  l: none".       
+00001000: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001010: 2020 2020 202f 3e0a 2020 2020 2020 2020       />.        
+00001020: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001030: 3c2f 673e 0a20 2020 2020 2020 2020 2020  </g>.           
+00001040: 2020 2020 2020 2020 203c 2f67 3e0a 2020           </g>.  
+00001050: 2020 2020 2020 2020 2020 2020 2020 3c2f                </
+00001060: 7379 6d62 6f6c 3e0a 2020 2020 2020 2020  symbol>.        
+00001070: 2020 2020 2020 2020 3c73 796d 626f 6c20          <symbol 
+00001080: 6964 3d22 4d65 7263 7572 7922 3e0a 2020  id="Mercury">.  
+00001090: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000010a0: 2020 3c67 2074 7261 6e73 666f 726d 3d22    <g transform="
+000010b0: 7472 616e 736c 6174 6528 332c 3129 223e  translate(3,1)">
+000010c0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+000010d0: 2020 2020 2020 2020 203c 7061 7468 0a20           <path. 
+000010e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000010f0: 2020 2020 2020 2020 2020 2064 3d22 4d20             d="M 
+00001100: 3132 2e34 3137 3930 382c 3131 2e30 3937  12.417908,11.097
+00001110: 3530 3720 4320 3132 2e34 3630 3831 382c  507 C 12.460818,
+00001120: 3133 2e36 3034 3931 3620 3130 2e36 3638  13.604916 10.668
+00001130: 3231 372c 3135 2e39 3936 3635 3620 382e  217,15.996656 8.
+00001140: 3235 3636 3830 352c 3136 2e36 3736 3633  2566805,16.67663
+00001150: 3920 4320 362e 3131 3830 3337 352c 3137  9 C 6.1180375,17
+00001160: 2e33 3232 3532 3220 332e 3634 3038 3637  .322522 3.640867
+00001170: 352c 3136 2e36 3131 3836 3920 322e 3139  5,16.611869 2.19
+00001180: 3930 3931 352c 3134 2e38 3937 3032 3520  90915,14.897025 
+00001190: 4320 302e 3730 3235 3133 3531 2c31 332e  C 0.70251351,13.
+000011a0: 3138 3538 3934 2030 2e33 3437 3035 3535  185894 0.3470555
+000011b0: 312c 3130 2e35 3734 3134 3920 312e 3337  1,10.574149 1.37
+000011c0: 3837 3833 352c 382e 3534 3036 3337 2043  87835,8.540637 C
+000011d0: 2032 2e33 3330 3930 3635 2c36 2e35 3737   2.3309065,6.577
+000011e0: 3831 3936 2034 2e34 3434 3839 3235 2c35  8196 4.4448925,5
+000011f0: 2e32 3339 3035 3135 2036 2e36 3334 3433  .2390515 6.63443
+00001200: 3835 2c35 2e32 3830 3138 3132 2043 2038  85,5.2801812 C 8
+00001210: 2e37 3433 3634 3835 2c35 2e32 3830 3831  .7436485,5.28081
+00001220: 3834 2031 302e 3739 3732 312c 362e 3531  84 10.79721,6.51
+00001230: 3834 3839 3720 3131 2e37 3535 3634 312c  84897 11.755641,
+00001240: 382e 3430 3134 3232 3920 4320 3132 2e31  8.4014229 C 12.1
+00001250: 3838 3730 392c 392e 3232 3933 3536 3320  88709,9.2293563 
+00001260: 3132 2e34 3231 3932 362c 3130 2e31 3632  12.421926,10.162
+00001270: 3536 3820 3132 2e34 3137 3930 382c 3131  568 12.417908,11
+00001280: 2e30 3937 3530 3720 7a20 4d20 3131 2e35  .097507 z M 11.5
+00001290: 3337 3534 392c 302e 3739 3437 3737 3536  37549,0.79477756
+000012a0: 2043 2031 312e 3336 3830 3131 2c32 2e39   C 11.368011,2.9
+000012b0: 3533 3136 3336 2039 2e35 3932 3831 3035  531636 9.5928105
+000012c0: 2c34 2e38 3439 3339 3420 372e 3435 3238  ,4.849394 7.4528
+000012d0: 3435 352c 352e 3137 3131 3237 2043 2035  455,5.171127 C 5
+000012e0: 2e34 3933 3430 3335 2c35 2e35 3035 3834  .4934035,5.50584
+000012f0: 3637 2033 2e33 3633 3435 3035 2c34 2e35  67 3.3634505,4.5
+00001300: 3439 3436 3836 2032 2e33 3935 3831 3335  494686 2.3958135
+00001310: 2c32 2e37 3934 3635 3836 2043 2032 2e30  ,2.7946586 C 2.0
+00001320: 3434 3831 3535 2c32 2e31 3831 3837 3436  448155,2.1818746
+00001330: 2031 2e38 3237 3537 3535 2c31 2e34 3933   1.8275755,1.493
+00001340: 3039 3636 2031 2e37 3632 3638 3435 2c30  0966 1.7626845,0
+00001350: 2e37 3839 3933 3735 3620 4d20 362e 3630  .78993756 M 6.60
+00001360: 3339 3632 352c 3136 2e38 3930 3531 3820  39625,16.890518 
+00001370: 4320 362e 3630 3339 3632 352c 3138 2e39  C 6.6039625,18.9
+00001380: 3937 3033 3120 362e 3630 3339 3632 352c  97031 6.6039625,
+00001390: 3231 2e31 3033 3534 3520 362e 3630 3339  21.103545 6.6039
+000013a0: 3632 352c 3233 2e32 3130 3035 3820 4d20  625,23.210058 M 
+000013b0: 332e 3937 3038 3231 352c 3230 2e35 3736  3.9708215,20.576
+000013c0: 3931 3620 4320 352e 3732 3632 3437 352c  916 C 5.7262475,
+000013d0: 3230 2e35 3736 3931 3620 372e 3438 3136  20.576916 7.4816
+000013e0: 3738 352c 3230 2e35 3736 3931 3620 392e  785,20.576916 9.
+000013f0: 3233 3731 3034 352c 3230 2e35 3736 3931  2371045,20.57691
+00001400: 3622 0a20 2020 2020 2020 2020 2020 2020  6".             
+00001410: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+00001420: 7479 6c65 3d22 7374 726f 6b65 3a20 2470  tyle="stroke: $p
+00001430: 6c61 6e65 7473 5f63 6f6c 6f72 5f32 3b20  lanets_color_2; 
+00001440: 7374 726f 6b65 2d77 6964 7468 3a20 3270  stroke-width: 2p
+00001450: 783b 2066 696c 6c3a 206e 6f6e 6522 0a20  x; fill: none". 
+00001460: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001470: 2020 2020 2020 202f 3e0a 2020 2020 2020         />.      
+00001480: 2020 2020 2020 2020 2020 2020 2020 3c2f                </
+00001490: 673e 0a20 2020 2020 2020 2020 2020 2020  g>.             
+000014a0: 2020 203c 2f73 796d 626f 6c3e 0a20 2020     </symbol>.   
+000014b0: 2020 2020 2020 2020 2020 2020 203c 7379               <sy
+000014c0: 6d62 6f6c 2069 643d 2256 656e 7573 223e  mbol id="Venus">
+000014d0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+000014e0: 2020 2020 203c 6720 7472 616e 7366 6f72       <g transfor
+000014f0: 6d3d 2274 7261 6e73 6c61 7465 2830 2c32  m="translate(0,2
+00001500: 2922 3e0a 2020 2020 2020 2020 2020 2020  )">.            
+00001510: 2020 2020 2020 2020 2020 2020 3c67 2074              <g t
+00001520: 7261 6e73 666f 726d 3d22 7363 616c 6528  ransform="scale(
+00001530: 2e39 2922 3e0a 2020 2020 2020 2020 2020  .9)">.          
+00001540: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001550: 2020 3c70 6174 680a 2020 2020 2020 2020    <path.        
+00001560: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001570: 2020 2020 2020 2020 643d 224d 2031 382e          d="M 18.
+00001580: 3430 3037 3033 2c37 2e33 3636 3734 3833  400703,7.3667483
+00001590: 2043 2031 382e 3432 3339 362c 392e 3636   C 18.42396,9.66
+000015a0: 3535 3332 3920 3137 2e31 3730 3130 322c  55329 17.170102,
+000015b0: 3131 2e39 3134 3537 3920 3135 2e32 3138  11.914579 15.218
+000015c0: 3937 322c 3133 2e31 3133 3732 3820 4320  972,13.113728 C 
+000015d0: 3133 2e31 3632 3435 392c 3134 2e34 3237  13.162459,14.427
+000015e0: 3235 3320 3130 2e33 3839 3835 352c 3134  253 10.389855,14
+000015f0: 2e34 3736 3737 3220 382e 3238 3731 3636  .476772 8.287166
+00001600: 332c 3133 2e32 3339 3730 3920 4320 362e  3,13.239709 C 6.
+00001610: 3237 3335 3835 312c 3132 2e31 3030 3532  2735851,12.10052
+00001620: 3420 342e 3933 3336 3333 2c39 2e38 3634  4 4.933633,9.864
+00001630: 3033 3233 2034 2e38 3937 3939 3135 2c37  0323 4.8979915,7
+00001640: 2e35 3431 3438 3034 2043 2034 2e38 3137  .5414804 C 4.817
+00001650: 3336 3137 2c35 2e32 3637 3835 3932 2035  3617,5.2678592 5
+00001660: 2e39 3835 3531 3936 2c33 2e30 3039 3030  .9855196,3.00900
+00001670: 3031 2037 2e38 3732 3838 3037 2c31 2e37  01 7.8728807,1.7
+00001680: 3533 3034 3731 2043 2039 2e38 3830 3339  530471 C 9.88039
+00001690: 3135 2c30 2e33 3635 3039 3534 3620 3132  15,0.36509546 12
+000016a0: 2e36 3438 3930 362c 302e 3231 3635 3731  .648906,0.216571
+000016b0: 3436 2031 342e 3739 3438 3439 2c31 2e33  46 14.794849,1.3
+000016c0: 3735 3238 3331 2043 2031 362e 3836 3937  752831 C 16.8697
+000016d0: 3732 2c32 2e34 3531 3436 3333 2031 382e  72,2.4514633 18.
+000016e0: 3239 3632 3431 2c34 2e36 3733 3134 3533  296241,4.6731453
+000016f0: 2031 382e 3339 3139 3138 2c37 2e30 3138   18.391918,7.018
+00001700: 3337 3233 2043 2031 382e 3339 3737 3831  3723 C 18.397781
+00001710: 2c37 2e31 3334 3339 3633 2031 382e 3430  ,7.1343963 18.40
+00001720: 3037 3033 2c37 2e32 3530 3537 3233 2031  0703,7.2505723 1
+00001730: 382e 3430 3037 3033 2c37 2e33 3636 3734  8.400703,7.36674
+00001740: 3833 207a 204d 2031 312e 3634 3832 3839  83 z M 11.648289
+00001750: 2c31 342e 3133 3636 3839 2043 2031 312e  ,14.136689 C 11.
+00001760: 3634 3832 3839 2c31 372e 3030 3837 3634  648289,17.008764
+00001770: 2031 312e 3634 3832 3839 2c31 392e 3838   11.648289,19.88
+00001780: 3038 3420 3131 2e36 3438 3238 392c 3232  084 11.648289,22
+00001790: 2e37 3532 3931 3520 4d20 372e 3936 3531  .752915 M 7.9651
+000017a0: 3333 332c 3139 2e30 3630 3234 3320 4320  333,19.060243 C 
+000017b0: 3130 2e34 3230 3537 2c31 392e 3036 3032  10.42057,19.0602
+000017c0: 3433 2031 322e 3837 3630 3038 2c31 392e  43 12.876008,19.
+000017d0: 3036 3032 3433 2031 352e 3333 3134 3434  060243 15.331444
+000017e0: 2c31 392e 3036 3032 3433 220a 2020 2020  ,19.060243".    
+000017f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001800: 2020 2020 2020 2020 2020 2020 7374 796c              styl
+00001810: 653d 2273 7472 6f6b 653a 2024 706c 616e  e="stroke: $plan
+00001820: 6574 735f 636f 6c6f 725f 333b 2073 7472  ets_color_3; str
+00001830: 6f6b 652d 7769 6474 683a 2032 7078 3b20  oke-width: 2px; 
+00001840: 6669 6c6c 3a20 6e6f 6e65 220a 2020 2020  fill: none".    
+00001850: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001860: 2020 2020 2020 2020 2f3e 0a20 2020 2020          />.     
+00001870: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001880: 2020 203c 2f67 3e0a 2020 2020 2020 2020     </g>.        
+00001890: 2020 2020 2020 2020 2020 2020 3c2f 673e              </g>
+000018a0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+000018b0: 203c 2f73 796d 626f 6c3e 0a20 2020 2020   </symbol>.     
+000018c0: 2020 2020 2020 2020 2020 203c 7379 6d62             <symb
+000018d0: 6f6c 2069 643d 224d 6172 7322 3e0a 2020  ol id="Mars">.  
+000018e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000018f0: 2020 3c67 2074 7261 6e73 666f 726d 3d22    <g transform="
+00001900: 7472 616e 736c 6174 6528 312c 3329 223e  translate(1,3)">
+00001910: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00001920: 2020 2020 2020 2020 203c 6720 7472 616e           <g tran
+00001930: 7366 6f72 6d3d 2273 6361 6c65 282e 3929  sform="scale(.9)
+00001940: 223e 0a20 2020 2020 2020 2020 2020 2020  ">.             
+00001950: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+00001960: 7061 7468 0a20 2020 2020 2020 2020 2020  path.           
+00001970: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001980: 2020 2020 2064 3d22 4d20 3139 2e38 3336       d="M 19.836
+00001990: 3832 382c 312e 3232 3638 3538 3520 4320  828,1.2268585 C 
+000019a0: 3137 2e34 3234 3432 322c 332e 3632 3538  17.424422,3.6258
+000019b0: 3737 3620 3135 2e30 3132 3030 382c 362e  776 15.012008,6.
+000019c0: 3032 3439 3034 3720 3132 2e35 3939 3539  0249047 12.59959
+000019d0: 342c 382e 3432 3339 3331 3720 4d20 3133  4,8.4239317 M 13
+000019e0: 2e35 3836 3133 312c 312e 3330 3332 3835  .586131,1.303285
+000019f0: 3320 4320 3135 2e36 3431 3632 322c 312e  3 C 15.641622,1.
+00001a00: 3330 3332 3835 3320 3137 2e36 3937 3130  3032853 17.69710
+00001a10: 352c 312e 3330 3332 3835 3320 3139 2e37  5,1.3032853 19.7
+00001a20: 3532 3539 352c 312e 3330 3332 3835 3320  52595,1.3032853 
+00001a30: 4320 3139 2e37 3532 3539 352c 332e 3334  C 19.752595,3.34
+00001a40: 3733 3638 3620 3139 2e37 3532 3630 332c  73686 19.752603,
+00001a50: 352e 3339 3134 3531 3720 3139 2e37 3532  5.3914517 19.752
+00001a60: 3630 332c 372e 3433 3535 3335 3722 0a20  603,7.4355357". 
+00001a70: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001a80: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+00001a90: 7479 6c65 3d22 7374 726f 6b65 3a20 2470  tyle="stroke: $p
+00001aa0: 6c61 6e65 7473 5f63 6f6c 6f72 5f34 3b20  lanets_color_4; 
+00001ab0: 7374 726f 6b65 2d77 6964 7468 3a20 3270  stroke-width: 2p
+00001ac0: 783b 2066 696c 6c3a 206e 6f6e 6522 0a20  x; fill: none". 
+00001ad0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001ae0: 2020 2020 2020 2020 2020 202f 3e0a 2020             />.  
+00001af0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001b00: 2020 2020 2020 2020 2020 3c70 6174 680a            <path.
+00001b10: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001b20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001b30: 643d 224d 2031 352e 3230 3838 3335 2c31  d="M 15.208835,1
+00001b40: 332e 3133 3737 3131 2043 2031 352e 3234  3.137711 C 15.24
+00001b50: 3537 3837 2c31 352e 3838 3833 3039 2031  5787,15.888309 1
+00001b60: 332e 3439 3735 3233 2c31 382e 3534 3334  3.497523,18.5434
+00001b70: 3620 3130 2e39 3639 3034 332c 3139 2e36  6 10.969043,19.6
+00001b80: 3137 3733 2043 2038 2e34 3538 3431 3735  1773 C 8.4584175
+00001b90: 2c32 302e 3734 3930 3336 2035 2e33 3135  ,20.749036 5.315
+00001ba0: 3534 3238 2c32 302e 3231 3634 3120 332e  5428,20.21641 3.
+00001bb0: 3332 3336 3330 362c 3138 2e33 3132 3834  3236306,18.31284
+00001bc0: 3320 4320 312e 3332 3934 3738 392c 3136  3 C 1.3294789,16
+00001bd0: 2e35 3032 3638 3620 302e 3535 3436 3631  .502686 0.554661
+00001be0: 3237 2c31 332e 3530 3436 3738 2031 2e34  27,13.504678 1.4
+00001bf0: 3133 3336 3135 2c31 302e 3935 3333 3032  133615,10.953302
+00001c00: 2043 2032 2e32 3438 3537 3231 2c38 2e32   C 2.2485721,8.2
+00001c10: 3833 3334 3532 2034 2e38 3030 3530 3433  833452 4.8005043
+00001c20: 2c36 2e32 3636 3030 3735 2037 2e35 3935  ,6.2660075 7.595
+00001c30: 3231 382c 362e 3038 3834 3236 3620 4320  218,6.0884266 C 
+00001c40: 3130 2e32 3837 3033 322c 352e 3834 3637  10.287032,5.8467
+00001c50: 3938 3420 3133 2e30 3232 3334 382c 372e  984 13.022348,7.
+00001c60: 3332 3331 3034 3820 3134 2e33 3133 3836  3231048 14.31386
+00001c70: 2c39 2e36 3933 3830 3831 2043 2031 342e  ,9.6938081 C 14.
+00001c80: 3930 3131 3633 2c31 302e 3733 3939 3637  901163,10.739967
+00001c90: 2031 352e 3231 3130 3832 2c31 312e 3933   15.211082,11.93
+00001ca0: 3831 3936 2031 352e 3230 3838 3335 2c31  8196 15.208835,1
+00001cb0: 332e 3133 3737 3131 207a 220a 2020 2020  3.137711 z".    
+00001cc0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001cd0: 2020 2020 2020 2020 2020 2020 7374 796c              styl
+00001ce0: 653d 2273 7472 6f6b 653a 2024 706c 616e  e="stroke: $plan
+00001cf0: 6574 735f 636f 6c6f 725f 343b 2073 7472  ets_color_4; str
+00001d00: 6f6b 652d 7769 6474 683a 2032 7078 3b20  oke-width: 2px; 
+00001d10: 6669 6c6c 3a20 6e6f 6e65 220a 2020 2020  fill: none".    
+00001d20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001d30: 2020 2020 2020 2020 2f3e 0a20 2020 2020          />.     
+00001d40: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001d50: 2020 203c 2f67 3e0a 2020 2020 2020 2020     </g>.        
+00001d60: 2020 2020 2020 2020 2020 2020 3c2f 673e              </g>
+00001d70: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00001d80: 203c 2f73 796d 626f 6c3e 0a20 2020 2020   </symbol>.     
+00001d90: 2020 2020 2020 2020 2020 203c 7379 6d62             <symb
+00001da0: 6f6c 2069 643d 224a 7570 6974 6572 223e  ol id="Jupiter">
+00001db0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00001dc0: 2020 2020 203c 6720 7472 616e 7366 6f72       <g transfor
+00001dd0: 6d3d 2274 7261 6e73 6c61 7465 2831 2c33  m="translate(1,3
+00001de0: 2922 3e0a 2020 2020 2020 2020 2020 2020  )">.            
+00001df0: 2020 2020 2020 2020 2020 2020 3c67 2074              <g t
+00001e00: 7261 6e73 666f 726d 3d22 7363 616c 6528  ransform="scale(
+00001e10: 2e39 2922 3e0a 2020 2020 2020 2020 2020  .9)">.          
+00001e20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001e30: 2020 3c70 6174 680a 2020 2020 2020 2020    <path.        
+00001e40: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001e50: 2020 2020 2020 2020 643d 224d 2031 362e          d="M 16.
+00001e60: 3930 3330 3038 2c30 2e39 3938 3439 3135  903008,0.9984915
+00001e70: 3720 4c20 3136 2e39 3033 3030 382c 3233  7 L 16.903008,23
+00001e80: 2e30 3031 3531 3220 4d20 3230 2e35 3330  .001512 M 20.530
+00001e90: 3237 382c 3137 2e33 3539 3731 3220 4c20  278,17.359712 L 
+00001ea0: 322e 3939 3834 3838 342c 3137 2e33 3539  2.9984884,17.359
+00001eb0: 3731 3220 4d20 342e 3831 3231 3138 342c  712 M 4.8121184,
+00001ec0: 382e 3839 3730 3132 2043 2034 2e32 3037  8.897012 C 4.207
+00001ed0: 3537 3834 2c38 2e38 3937 3031 3220 322e  5784,8.897012 2.
+00001ee0: 3939 3834 3838 342c 382e 3333 3238 3332  9984884,8.332832
+00001ef0: 2032 2e39 3938 3438 3834 2c36 2e30 3736   2.9984884,6.076
+00001f00: 3131 3220 4320 322e 3939 3834 3838 342c  112 C 2.9984884,
+00001f10: 332e 3831 3933 3832 2035 2e34 3136 3636  3.819382 5.41666
+00001f20: 3834 2c31 2e35 3632 3637 3136 2037 2e38  84,1.5626716 7.8
+00001f30: 3334 3834 3834 2c31 2e35 3632 3637 3136  348484,1.5626716
+00001f40: 2043 2031 302e 3235 3330 3238 2c31 2e35   C 10.253028,1.5
+00001f50: 3632 3637 3136 2031 322e 3637 3131 3938  626716 12.671198
+00001f60: 2c33 2e32 3535 3231 3220 3132 2e36 3731  ,3.255212 12.671
+00001f70: 3139 382c 372e 3230 3434 3732 2043 2031  198,7.204472 C 1
+00001f80: 322e 3637 3131 3938 2c31 312e 3135 3337  2.671198,11.1537
+00001f90: 3332 2039 2e36 3438 3437 3834 2c31 372e  32 9.6484784,17.
+00001fa0: 3335 3937 3132 2033 2e36 3033 3032 3834  359712 3.6030284
+00001fb0: 2c31 372e 3335 3937 3132 220a 2020 2020  ,17.359712".    
+00001fc0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00001fd0: 2020 2020 2020 2020 2020 2020 7374 796c              styl
+00001fe0: 653d 2273 7472 6f6b 653a 2024 706c 616e  e="stroke: $plan
+00001ff0: 6574 735f 636f 6c6f 725f 353b 2073 7472  ets_color_5; str
+00002000: 6f6b 652d 7769 6474 683a 2032 7078 3b20  oke-width: 2px; 
+00002010: 6669 6c6c 3a20 6e6f 6e65 220a 2020 2020  fill: none".    
+00002020: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002030: 2020 2020 2020 2020 2f3e 0a20 2020 2020          />.     
+00002040: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002050: 2020 203c 2f67 3e0a 2020 2020 2020 2020     </g>.        
+00002060: 2020 2020 2020 2020 2020 2020 3c2f 673e              </g>
+00002070: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00002080: 203c 2f73 796d 626f 6c3e 0a20 2020 2020   </symbol>.     
+00002090: 2020 2020 2020 2020 2020 203c 7379 6d62             <symb
+000020a0: 6f6c 2069 643d 2253 6174 7572 6e22 3e0a  ol id="Saturn">.
+000020b0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000020c0: 2020 2020 3c67 2074 7261 6e73 666f 726d      <g transform
+000020d0: 3d22 7472 616e 736c 6174 6528 312c 3229  ="translate(1,2)
+000020e0: 223e 0a20 2020 2020 2020 2020 2020 2020  ">.             
+000020f0: 2020 2020 2020 2020 2020 203c 7061 7468             <path
+00002100: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00002110: 2020 2020 2020 2020 2020 2020 2064 3d22               d="
+00002120: 4d20 382e 3338 3434 3334 392c 302e 3930  M 8.3844349,0.90
+00002130: 3230 3332 3331 204c 2038 2e33 3834 3433  203231 L 8.38443
+00002140: 3439 2c31 382e 3239 3838 3532 204d 2035  49,18.298852 M 5
+00002150: 2e34 3334 3934 3439 2c33 2e37 3531 3531  .4349449,3.75151
+00002160: 3233 204c 2031 322e 3636 3837 3435 2c33  23 L 12.668745,3
+00002170: 2e37 3531 3531 3233 204d 2031 362e 3832  .7515123 M 16.82
+00002180: 3338 3735 2c32 312e 3839 3831 3932 2043  3875,21.898192 C
+00002190: 2031 362e 3232 3130 3535 2c32 322e 3439   16.221055,22.49
+000021a0: 3830 3832 2031 352e 3631 3832 3335 2c32  8082 15.618235,2
+000021b0: 332e 3039 3739 3732 2031 352e 3031 3534  3.097972 15.0154
+000021c0: 3135 2c32 332e 3039 3739 3732 2043 2031  15,23.097972 C 1
+000021d0: 342e 3431 3236 3035 2c32 332e 3039 3739  4.412605,23.0979
+000021e0: 3732 2031 332e 3230 3639 3735 2c32 322e  72 13.206975,22.
+000021f0: 3439 3830 3832 2031 332e 3230 3639 3735  498082 13.206975
+00002200: 2c32 312e 3239 3833 3032 2043 2031 332e  ,21.298302 C 13.
+00002210: 3230 3639 3735 2c32 302e 3039 3835 3232  206975,20.098522
+00002220: 2031 332e 3830 3937 3835 2c31 382e 3839   13.809785,18.89
+00002230: 3837 3432 2031 352e 3031 3534 3135 2c31  8742 15.015415,1
+00002240: 372e 3639 3839 3632 2043 2031 362e 3232  7.698962 C 16.22
+00002250: 3130 3535 2c31 362e 3439 3931 3832 2031  1055,16.499182 1
+00002260: 372e 3432 3636 3835 2c31 342e 3039 3936  7.426685,14.0996
+00002270: 3232 2031 372e 3432 3636 3835 2c31 312e  22 17.426685,11.
+00002280: 3730 3030 3532 2043 2031 372e 3432 3636  700052 C 17.4266
+00002290: 3835 2c39 2e33 3030 3439 3233 2031 362e  85,9.3004923 16.
+000022a0: 3232 3130 3535 2c36 2e39 3030 3933 3233  221055,6.9009323
+000022b0: 2031 332e 3830 3937 3835 2c36 2e39 3030   13.809785,6.900
+000022c0: 3933 3233 2043 2031 312e 3532 3932 3135  9323 C 11.529215
+000022d0: 2c36 2e39 3030 3933 3233 2039 2e35 3930  ,6.9009323 9.590
+000022e0: 3036 3439 2c38 2e31 3030 3731 3233 2038  0649,8.1007123 8
+000022f0: 2e33 3834 3433 3439 2c31 302e 3530 3032  .3844349,10.5002
+00002300: 3832 220a 2020 2020 2020 2020 2020 2020  82".            
+00002310: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002320: 7374 796c 653d 2273 7472 6f6b 653a 2024  style="stroke: $
+00002330: 706c 616e 6574 735f 636f 6c6f 725f 363b  planets_color_6;
+00002340: 2073 7472 6f6b 652d 7769 6474 683a 2032   stroke-width: 2
+00002350: 7078 3b20 6669 6c6c 3a20 6e6f 6e65 220a  px; fill: none".
+00002360: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002370: 2020 2020 2020 2020 2f3e 0a20 2020 2020          />.     
+00002380: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+00002390: 2f67 3e0a 2020 2020 2020 2020 2020 2020  /g>.            
+000023a0: 2020 2020 3c2f 7379 6d62 6f6c 3e0a 2020      </symbol>.  
+000023b0: 2020 2020 2020 2020 2020 2020 2020 3c73                <s
+000023c0: 796d 626f 6c20 6964 3d22 5572 616e 7573  ymbol id="Uranus
+000023d0: 223e 0a20 2020 2020 2020 2020 2020 2020  ">.             
+000023e0: 2020 2020 2020 203c 6720 7472 616e 7366         <g transf
+000023f0: 6f72 6d3d 2274 7261 6e73 6c61 7465 2832  orm="translate(2
+00002400: 2c34 2922 3e0a 2020 2020 2020 2020 2020  ,4)">.          
+00002410: 2020 2020 2020 2020 2020 2020 2020 3c67                <g
+00002420: 2074 7261 6e73 666f 726d 3d22 7363 616c   transform="scal
+00002430: 6528 2e38 2922 3e0a 2020 2020 2020 2020  e(.8)">.        
+00002440: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002450: 2020 2020 3c70 6174 680a 2020 2020 2020      <path.      
+00002460: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002470: 2020 2020 2020 2020 2020 643d 224d 2034            d="M 4
+00002480: 2e36 3737 3230 3636 2c31 362e 3039 3734  .6772066,16.0974
+00002490: 3233 2043 2033 2e32 3034 3234 3236 2c31  23 C 3.2042426,1
+000024a0: 362e 3039 3734 3233 2031 2e37 3331 3237  6.097423 1.73127
+000024b0: 3736 2c31 362e 3039 3734 3233 2030 2e32  76,16.097423 0.2
+000024c0: 3538 3330 3636 312c 3136 2e30 3937 3432  5830661,16.09742
+000024d0: 3320 4320 302e 3332 3138 3530 3631 2c31  3 C 0.32185061,1
+000024e0: 352e 3839 3438 3739 2030 2e31 3139 3935  5.894879 0.11995
+000024f0: 3636 312c 3135 2e34 3835 3039 3620 302e  661,15.485096 0.
+00002500: 3337 3937 3633 3631 2c31 352e 3433 3537  37976361,15.4357
+00002510: 3837 2043 2031 2e31 3830 3937 3236 2c31  87 C 1.1809726,1
+00002520: 352e 3233 3534 3835 2031 2e39 3832 3138  5.235485 1.98218
+00002530: 3236 2c31 352e 3033 3531 3832 2032 2e37  26,15.035182 2.7
+00002540: 3833 3339 3236 2c31 342e 3833 3438 3820  833926,14.83488 
+00002550: 4320 322e 3738 3333 3932 362c 3130 2e36  C 2.7833926,10.6
+00002560: 3236 3430 3120 322e 3738 3333 3932 362c  26401 2.7833926,
+00002570: 362e 3431 3739 3239 2032 2e37 3833 3339  6.417929 2.78339
+00002580: 3236 2c32 2e32 3039 3435 3032 2043 2031  26,2.2094502 C 1
+00002590: 2e39 3431 3639 3936 2c31 2e39 3939 3032  .9416996,1.99902
+000025a0: 3835 2031 2e31 3030 3030 3536 2c31 2e37  85 1.1000056,1.7
+000025b0: 3838 3630 3034 2030 2e32 3538 3330 3636  886004 0.2583066
+000025c0: 312c 312e 3537 3831 3738 3720 4320 302e  1,1.5781787 C 0.
+000025d0: 3332 3338 3037 3631 2c31 2e33 3931 3532  32380761,1.39152
+000025e0: 3433 2030 2e31 3135 3730 3236 312c 302e  43 0.11570261,0.
+000025f0: 3933 3132 3634 3332 2030 2e33 3833 3530  93126432 0.38350
+00002600: 3036 312c 302e 3934 3639 3037 3232 2043  061,0.94690722 C
+00002610: 2031 2e38 3134 3733 3736 2c30 2e39 3436   1.8147376,0.946
+00002620: 3930 3732 3220 332e 3234 3539 3639 362c  90722 3.2459696,
+00002630: 302e 3934 3639 3037 3232 2034 2e36 3737  0.94690722 4.677
+00002640: 3230 3636 2c30 2e39 3436 3930 3732 3220  2066,0.94690722 
+00002650: 4320 342e 3637 3732 3036 362c 352e 3939  C 4.6772066,5.99
+00002660: 3730 3739 3220 342e 3637 3732 3036 362c  70792 4.6772066,
+00002670: 3131 2e30 3437 3235 3120 342e 3637 3732  11.047251 4.6772
+00002680: 3036 362c 3136 2e30 3937 3432 3320 7a20  066,16.097423 z 
+00002690: 220a 2020 2020 2020 2020 2020 2020 2020  ".              
+000026a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000026b0: 2020 7374 796c 653d 2273 7472 6f6b 653a    style="stroke:
+000026c0: 2024 706c 616e 6574 735f 636f 6c6f 725f   $planets_color_
+000026d0: 373b 2073 7472 6f6b 652d 7769 6474 683a  7; stroke-width:
+000026e0: 2031 7078 3b20 6669 6c6c 3a20 2470 6c61   1px; fill: $pla
+000026f0: 6e65 7473 5f63 6f6c 6f72 5f35 220a 2020  nets_color_5".  
+00002700: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002710: 2020 2020 2020 2020 2020 2f3e 0a20 2020            />.   
+00002720: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002730: 2020 2020 2020 2020 203c 7061 7468 0a20           <path. 
+00002740: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002750: 2020 2020 2020 2020 2020 2020 2020 2064                 d
+00002760: 3d22 4d20 3138 2e35 3635 3138 2c31 362e  ="M 18.56518,16.
+00002770: 3039 3734 3233 2043 2032 302e 3033 3831  097423 C 20.0381
+00002780: 3531 2c31 362e 3039 3734 3233 2032 312e  51,16.097423 21.
+00002790: 3531 3131 3136 2c31 362e 3039 3734 3233  511116,16.097423
+000027a0: 2032 322e 3938 3430 3831 2c31 362e 3039   22.984081,16.09
+000027b0: 3734 3233 2043 2032 322e 3932 3035 3433  7423 C 22.920543
+000027c0: 2c31 352e 3839 3438 3739 2032 332e 3132  ,15.894879 23.12
+000027d0: 3234 332c 3135 2e34 3835 3039 3620 3232  243,15.485096 22
+000027e0: 2e38 3632 3633 312c 3135 2e34 3335 3738  .862631,15.43578
+000027f0: 3720 4320 3232 2e30 3631 3432 312c 3135  7 C 22.061421,15
+00002800: 2e32 3335 3438 3520 3231 2e32 3630 3231  .235485 21.26021
+00002810: 312c 3135 2e30 3335 3138 3220 3230 2e34  1,15.035182 20.4
+00002820: 3538 3939 352c 3134 2e38 3334 3838 2043  58995,14.83488 C
+00002830: 2032 302e 3435 3839 3935 2c31 302e 3632   20.458995,10.62
+00002840: 3634 3031 2032 302e 3435 3839 3935 2c36  6401 20.458995,6
+00002850: 2e34 3137 3932 3920 3230 2e34 3538 3939  .417929 20.45899
+00002860: 352c 322e 3230 3934 3530 3220 4320 3231  5,2.2094502 C 21
+00002870: 2e33 3030 3639 342c 312e 3939 3930 3238  .300694,1.999028
+00002880: 3520 3232 2e31 3432 3338 382c 312e 3738  5 22.142388,1.78
+00002890: 3836 3030 3420 3232 2e39 3834 3038 312c  86004 22.984081,
+000028a0: 312e 3537 3831 3738 3720 4320 3232 2e39  1.5781787 C 22.9
+000028b0: 3138 3538 372c 312e 3339 3135 3234 3320  18587,1.3915243 
+000028c0: 3233 2e31 3236 3639 312c 302e 3933 3132  23.126691,0.9312
+000028d0: 3634 3332 2032 322e 3835 3838 3933 2c30  6432 22.858893,0
+000028e0: 2e39 3436 3930 3732 3220 4320 3231 2e34  .94690722 C 21.4
+000028f0: 3237 3635 362c 302e 3934 3639 3037 3232  27656,0.94690722
+00002900: 2031 392e 3939 3634 3138 2c30 2e39 3436   19.996418,0.946
+00002910: 3930 3732 3220 3138 2e35 3635 3138 2c30  90722 18.56518,0
+00002920: 2e39 3436 3930 3732 3220 4320 3138 2e35  .94690722 C 18.5
+00002930: 3635 3138 2c35 2e39 3937 3037 3932 2031  6518,5.9970792 1
+00002940: 382e 3536 3531 382c 3131 2e30 3437 3235  8.56518,11.04725
+00002950: 3120 3138 2e35 3635 3138 2c31 362e 3039  1 18.56518,16.09
+00002960: 3734 3233 207a 2022 0a20 2020 2020 2020  7423 z ".       
+00002970: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002980: 2020 2020 2020 2020 2073 7479 6c65 3d22           style="
+00002990: 7374 726f 6b65 3a20 2470 6c61 6e65 7473  stroke: $planets
+000029a0: 5f63 6f6c 6f72 5f37 3b20 7374 726f 6b65  _color_7; stroke
+000029b0: 2d77 6964 7468 3a20 3170 783b 2066 696c  -width: 1px; fil
+000029c0: 6c3a 2024 706c 616e 6574 735f 636f 6c6f  l: $planets_colo
+000029d0: 725f 3522 0a20 2020 2020 2020 2020 2020  r_5".           
+000029e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000029f0: 202f 3e0a 2020 2020 2020 2020 2020 2020   />.            
+00002a00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002a10: 3c70 6174 680a 2020 2020 2020 2020 2020  <path.          
+00002a20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002a30: 2020 2020 2020 643d 224d 2034 2e30 3435        d="M 4.045
+00002a40: 3933 3536 2c38 2e35 3232 3136 3532 2043  9356,8.5221652 C
+00002a50: 2039 2e30 3936 3130 3736 2c38 2e35 3232   9.0961076,8.522
+00002a60: 3136 3532 2031 342e 3134 3632 382c 382e  1652 14.14628,8.
+00002a70: 3532 3231 3635 3220 3139 2e31 3936 3435  5221652 19.19645
+00002a80: 322c 382e 3532 3231 3635 3220 4d20 3131  2,8.5221652 M 11
+00002a90: 2e36 3231 3139 342c 302e 3934 3639 3037  .621194,0.946907
+00002aa0: 3232 2043 2031 312e 3632 3131 3934 2c36  22 C 11.621194,6
+00002ab0: 2e34 3137 3932 3920 3131 2e36 3231 3139  .417929 11.62119
+00002ac0: 342c 3131 2e38 3838 3934 3420 3131 2e36  4,11.888944 11.6
+00002ad0: 3231 3139 342c 3137 2e33 3539 3936 3620  21194,17.359966 
+00002ae0: 4d20 3134 2e31 3436 3234 322c 3230 2e35  M 14.146242,20.5
+00002af0: 3136 3334 3220 4320 3134 2e32 3237 3935  16342 C 14.22795
+00002b00: 342c 3232 2e32 3031 3130 3520 3132 2e32  4,22.201105 12.2
+00002b10: 3735 3636 352c 3233 2e35 3530 3330 3220  75665,23.550302 
+00002b20: 3130 2e37 3235 3637 382c 3232 2e38 3833  10.725678,22.883
+00002b30: 3032 3320 4320 392e 3133 3935 3736 362c  023 C 9.1395766,
+00002b40: 3232 2e33 3438 3639 3620 382e 3535 3230  22.348696 8.5520
+00002b50: 3436 362c 3230 2e30 3839 3638 3520 392e  466,20.089685 9.
+00002b60: 3730 3334 3937 362c 3138 2e38 3630 3837  7034976,18.86087
+00002b70: 3120 4320 3130 2e37 3234 3037 352c 3137  1 C 10.724075,17
+00002b80: 2e36 3038 3138 3220 3132 2e39 3539 3436  .608182 12.95946
+00002b90: 342c 3137 2e37 3436 3438 3120 3133 2e37  4,17.746481 13.7
+00002ba0: 3630 3733 312c 3139 2e31 3734 3830 3820  60731,19.174808 
+00002bb0: 4320 3134 2e30 3131 3333 392c 3139 2e35  C 14.011339,19.5
+00002bc0: 3734 3120 3134 2e31 3438 3138 2c32 302e  741 14.14818,20.
+00002bd0: 3034 3436 3434 2031 342e 3134 3632 3432  044644 14.146242
+00002be0: 2c32 302e 3531 3633 3432 207a 2022 0a20  ,20.516342 z ". 
+00002bf0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002c00: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+00002c10: 7479 6c65 3d22 7374 726f 6b65 3a20 2470  tyle="stroke: $p
+00002c20: 6c61 6e65 7473 5f63 6f6c 6f72 5f37 3b20  lanets_color_7; 
+00002c30: 7374 726f 6b65 2d77 6964 7468 3a20 3270  stroke-width: 2p
+00002c40: 783b 2066 696c 6c3a 206e 6f6e 6522 0a20  x; fill: none". 
+00002c50: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002c60: 2020 2020 2020 2020 2020 202f 3e0a 2020             />.  
+00002c70: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002c80: 2020 2020 2020 3c2f 673e 0a20 2020 2020        </g>.     
+00002c90: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+00002ca0: 2f67 3e0a 2020 2020 2020 2020 2020 2020  /g>.            
+00002cb0: 2020 2020 3c2f 7379 6d62 6f6c 3e0a 2020      </symbol>.  
+00002cc0: 2020 2020 2020 2020 2020 2020 2020 3c73                <s
+00002cd0: 796d 626f 6c20 6964 3d22 4e65 7074 756e  ymbol id="Neptun
+00002ce0: 6522 3e0a 2020 2020 2020 2020 2020 2020  e">.            
+00002cf0: 2020 2020 2020 2020 3c67 2074 7261 6e73          <g trans
+00002d00: 666f 726d 3d22 7472 616e 736c 6174 6528  form="translate(
+00002d10: 322c 3429 223e 0a20 2020 2020 2020 2020  2,4)">.         
+00002d20: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+00002d30: 6720 7472 616e 7366 6f72 6d3d 2273 6361  g transform="sca
+00002d40: 6c65 282e 3929 223e 0a20 2020 2020 2020  le(.9)">.       
+00002d50: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002d60: 2020 2020 203c 7061 7468 0a20 2020 2020       <path.     
+00002d70: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002d80: 2020 2020 2020 2020 2020 2064 3d22 4d20             d="M 
+00002d90: 332e 3838 3633 3037 2c32 2e32 3039 3831  3.886307,2.20981
+00002da0: 3334 2043 2032 2e32 3732 3832 3439 2c31  34 C 2.2728249,1
+00002db0: 332e 3137 3233 3336 2034 2e39 3631 3937  3.172336 4.96197
+00002dc0: 3138 2c31 342e 3831 3637 3138 2031 302e  18,14.816718 10.
+00002dd0: 3334 3032 3635 2c31 342e 3831 3637 3138  340265,14.816718
+00002de0: 2043 2031 352e 3731 3835 3637 2c31 342e   C 15.718567,14.
+00002df0: 3831 3637 3138 2031 382e 3430 3737 3231  816718 18.407721
+00002e00: 2c31 332e 3137 3233 3336 2031 362e 3739  ,13.172336 16.79
+00002e10: 3432 3331 2c32 2e32 3039 3831 3334 204d  4231,2.2098134 M
+00002e20: 2031 302e 3334 3032 3635 2c33 2e33 3036   10.340265,3.306
+00002e30: 3036 3538 204c 2031 302e 3334 3032 3635  0658 L 10.340265
+00002e40: 2c32 332e 3538 3637 3336 204d 2036 2e30  ,23.586736 M 6.0
+00002e50: 3337 3632 392c 3139 2e32 3031 3732 3720  37629,19.201727 
+00002e60: 4c20 3134 2e36 3432 3930 392c 3139 2e32  L 14.642909,19.2
+00002e70: 3031 3732 3720 4d20 302e 3931 3138 3030  01727 M 0.911800
+00002e80: 3237 2c33 2e37 3233 3038 3038 204c 2033  27,3.7230808 L 3
+00002e90: 2e39 3633 3537 3935 2c31 2e34 3130 3333  .9635795,1.41033
+00002ea0: 3631 204c 2036 2e32 3332 3836 3839 2c34  61 L 6.2328689,4
+00002eb0: 2e35 3230 3534 3738 204d 2037 2e35 3939  .5205478 M 7.599
+00002ec0: 3834 3836 2c36 2e33 3432 3132 3438 204c  8486,6.3421248 L
+00002ed0: 2031 302e 3235 3930 3535 2c33 2e35 3731   10.259055,3.571
+00002ee0: 3331 3038 204c 2031 322e 3937 3738 3132  3108 L 12.977812
+00002ef0: 2c36 2e32 3831 3434 3238 204d 2031 342e  ,6.2814428 M 14.
+00002f00: 3430 3738 3839 2c34 2e37 3132 3035 3238  407889,4.7120528
+00002f10: 204c 2031 362e 3731 3539 3436 2c31 2e36   L 16.715946,1.6
+00002f20: 3331 3630 3835 204c 2031 392e 3733 3835  316085 L 19.7385
+00002f30: 3036 2c33 2e39 3833 3836 3238 220a 2020  06,3.9838628".  
+00002f40: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002f50: 2020 2020 2020 2020 2020 2020 2020 7374                st
+00002f60: 796c 653d 2273 7472 6f6b 653a 2024 706c  yle="stroke: $pl
+00002f70: 616e 6574 735f 636f 6c6f 725f 383b 2073  anets_color_8; s
+00002f80: 7472 6f6b 652d 7769 6474 683a 2032 7078  troke-width: 2px
+00002f90: 3b20 6669 6c6c 3a20 6e6f 6e65 220a 2020  ; fill: none".  
+00002fa0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002fb0: 2020 2020 2020 2020 2020 2f3e 0a20 2020            />.   
+00002fc0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00002fd0: 2020 2020 203c 2f67 3e0a 2020 2020 2020       </g>.      
+00002fe0: 2020 2020 2020 2020 2020 2020 2020 3c2f                </
+00002ff0: 673e 0a20 2020 2020 2020 2020 2020 2020  g>.             
+00003000: 2020 203c 2f73 796d 626f 6c3e 0a20 2020     </symbol>.   
+00003010: 2020 2020 2020 2020 2020 2020 203c 7379               <sy
+00003020: 6d62 6f6c 2069 643d 2250 6c75 746f 223e  mbol id="Pluto">
+00003030: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00003040: 2020 2020 203c 6720 7472 616e 7366 6f72       <g transfor
+00003050: 6d3d 2274 7261 6e73 6c61 7465 2830 2c33  m="translate(0,3
+00003060: 2922 3e0a 2020 2020 2020 2020 2020 2020  )">.            
+00003070: 2020 2020 2020 2020 2020 2020 3c67 2074              <g t
+00003080: 7261 6e73 666f 726d 3d22 7363 616c 6528  ransform="scale(
+00003090: 2e39 2922 3e0a 2020 2020 2020 2020 2020  .9)">.          
+000030a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000030b0: 2020 3c70 6174 680a 2020 2020 2020 2020    <path.        
+000030c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000030d0: 2020 2020 2020 2020 643d 224d 2037 2e32          d="M 7.2
+000030e0: 3938 3833 3839 2c31 382e 3136 3936 3731  988389,18.169671
+000030f0: 204c 2031 372e 3137 3032 3939 2c31 382e   L 17.170299,18.
+00003100: 3136 3936 3731 204d 2031 322e 3233 3435  169671 M 12.2345
+00003110: 3639 2c32 332e 3130 3534 3031 204c 2031  69,23.105401 L 1
+00003120: 322e 3233 3435 3639 2c31 322e 3631 3639  2.234569,12.6169
+00003130: 3831 204d 2031 362e 3535 3333 3039 2c35  81 M 16.553309,5
+00003140: 2e32 3133 3336 3039 2043 2031 362e 3535  .2133609 C 16.55
+00003150: 3333 3039 2c37 2e35 3937 3332 3039 2031  3309,7.5973209 1
+00003160: 342e 3631 3834 3939 2c39 2e35 3332 3133  4.618499,9.53213
+00003170: 3039 2031 322e 3233 3435 3339 2c39 2e35  09 12.234539,9.5
+00003180: 3332 3133 3039 2043 2039 2e38 3530 3538  321309 C 9.85058
+00003190: 3839 2c39 2e35 3332 3133 3039 2037 2e39  89,9.5321309 7.9
+000031a0: 3135 3737 3839 2c37 2e35 3937 3332 3039  157789,7.5973209
+000031b0: 2037 2e39 3135 3737 3839 2c35 2e32 3133   7.9157789,5.213
+000031c0: 3336 3039 2043 2037 2e39 3135 3737 3839  3609 C 7.9157789
+000031d0: 2c32 2e38 3239 3431 3039 2039 2e38 3530  ,2.8294109 9.850
+000031e0: 3538 3839 2c30 2e38 3934 3630 3038 3720  5889,0.89460087 
+000031f0: 3132 2e32 3334 3533 392c 302e 3839 3436  12.234539,0.8946
+00003200: 3030 3837 2043 2031 342e 3631 3834 3939  0087 C 14.618499
+00003210: 2c30 2e38 3934 3630 3038 3720 3136 2e35  ,0.89460087 16.5
+00003220: 3533 3330 392c 322e 3832 3934 3130 3920  53309,2.8294109 
+00003230: 3136 2e35 3533 3330 392c 352e 3231 3333  16.553309,5.2133
+00003240: 3630 3920 7a20 4d20 3139 2e36 3338 3133  609 z M 19.63813
+00003250: 392c 352e 3231 3333 3630 3920 4320 3139  9,5.2133609 C 19
+00003260: 2e36 3338 3133 392c 392e 3330 3031 3530  .638139,9.300150
+00003270: 3920 3136 2e33 3231 3332 392c 3132 2e36  9 16.321329,12.6
+00003280: 3136 3936 3120 3132 2e32 3334 3533 392c  16961 12.234539,
+00003290: 3132 2e36 3136 3936 3120 4320 382e 3134  12.616961 C 8.14
+000032a0: 3737 3538 392c 3132 2e36 3136 3936 3120  77589,12.616961 
+000032b0: 342e 3833 3039 3438 392c 392e 3330 3031  4.8309489,9.3001
+000032c0: 3530 3920 342e 3833 3039 3438 392c 352e  509 4.8309489,5.
+000032d0: 3231 3333 3630 3920 4320 342e 3833 3039  2133609 C 4.8309
+000032e0: 3438 392c 352e 3231 3333 3630 3920 342e  489,5.2133609 4.
+000032f0: 3833 3039 3438 392c 352e 3231 3333 3630  8309489,5.213360
+00003300: 3920 342e 3833 3039 3438 392c 352e 3231  9 4.8309489,5.21
+00003310: 3333 3630 3922 0a20 2020 2020 2020 2020  33609".         
+00003320: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003330: 2020 2020 2020 2073 7479 6c65 3d22 7374         style="st
+00003340: 726f 6b65 3a20 2470 6c61 6e65 7473 5f63  roke: $planets_c
+00003350: 6f6c 6f72 5f39 3b20 7374 726f 6b65 2d77  olor_9; stroke-w
+00003360: 6964 7468 3a20 3270 783b 2066 696c 6c3a  idth: 2px; fill:
+00003370: 206e 6f6e 6522 0a20 2020 2020 2020 2020   none".         
+00003380: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003390: 2020 202f 3e0a 2020 2020 2020 2020 2020     />.          
+000033a0: 2020 2020 2020 2020 2020 2020 2020 3c2f                </
+000033b0: 673e 0a20 2020 2020 2020 2020 2020 2020  g>.             
+000033c0: 2020 2020 2020 203c 2f67 3e0a 2020 2020         </g>.    
+000033d0: 2020 2020 2020 2020 2020 2020 3c2f 7379              </sy
+000033e0: 6d62 6f6c 3e0a 2020 2020 2020 2020 2020  mbol>.          
+000033f0: 2020 2020 2020 3c73 796d 626f 6c20 6964        <symbol id
+00003400: 3d22 4d65 616e 5f4e 6f64 6522 3e0a 2020  ="Mean_Node">.  
+00003410: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003420: 2020 3c67 2074 7261 6e73 666f 726d 3d22    <g transform="
+00003430: 7472 616e 736c 6174 6528 302c 3329 223e  translate(0,3)">
+00003440: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00003450: 2020 2020 2020 2020 203c 7061 7468 0a20           <path. 
+00003460: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003470: 2020 2020 2020 2020 2020 2064 3d22 4d20             d="M 
+00003480: 382e 3830 3936 3034 362c 302e 3037 3536  8.8096046,0.0756
+00003490: 3636 3839 3720 4320 362e 3431 3537 3533  66897 C 6.415753
+000034a0: 362c 302e 3636 3132 3339 3632 2034 2e33  6,0.66123962 4.3
+000034b0: 3736 3737 3639 2c32 2e35 3330 3638 3337  767769,2.5306837
+000034c0: 2033 2e36 3633 3436 3536 2c34 2e39 3030   3.6634656,4.900
+000034d0: 3735 3134 2043 2033 2e30 3533 3630 3731  7514 C 3.0536071
+000034e0: 2c36 2e36 3830 3932 3634 2033 2e36 3836  ,6.6809264 3.686
+000034f0: 3836 3832 2c38 2e36 3233 3839 3031 2034  8682,8.6238901 4
+00003500: 2e35 3837 3839 3838 2c31 302e 3138 3634  .5878988,10.1864
+00003510: 3337 2043 2035 2e31 3332 3339 3937 2c31  37 C 5.1323997,1
+00003520: 312e 3132 3436 3232 2035 2e39 3631 3537  1.124622 5.96157
+00003530: 3533 2c31 312e 3930 3839 3520 362e 3139  53,11.90895 6.19
+00003540: 3037 3330 322c 3133 2e30 3037 3930 3620  07302,13.007906 
+00003550: 4320 362e 3539 3137 3230 322c 3134 2e34  C 6.5917202,14.4
+00003560: 3834 3438 3820 362e 3438 3837 3135 362c  84488 6.4887156,
+00003570: 3136 2e33 3837 3532 3320 352e 3137 3233  16.387523 5.1723
+00003580: 3738 382c 3137 2e33 3832 3537 3620 4320  788,17.382576 C 
+00003590: 342e 3333 3239 3937 342c 3138 2e30 3533  4.3329974,18.053
+000035a0: 3431 3320 332e 3037 3735 3734 312c 3137  413 3.0775741,17
+000035b0: 2e34 3535 3033 3420 322e 3832 3030 3133  .455034 2.820013
+000035c0: 362c 3136 2e34 3831 3139 3620 4320 322e  6,16.481196 C 2.
+000035d0: 3339 3136 3535 322c 3135 2e31 3030 3739  3916552,15.10079
+000035e0: 3320 332e 3332 3331 3839 382c 3133 2e33  3 3.3231898,13.3
+000035f0: 3936 3435 3620 342e 3737 3933 3331 362c  96456 4.7793316,
+00003600: 3133 2e31 3633 3830 3620 4320 352e 3531  13.163806 C 5.51
+00003610: 3537 3836 312c 3133 2e34 3438 3438 3920  57861,13.448489 
+00003620: 352e 3733 3632 3335 332c 3133 2e30 3038  5.7362353,13.008
+00003630: 3333 3120 342e 3938 3830 3531 2c31 322e  331 4.988051,12.
+00003640: 3733 3931 3031 2043 2033 2e34 3736 3736  739101 C 3.47676
+00003650: 3936 2c31 312e 3938 3037 3631 2031 2e32  96,11.980761 1.2
+00003660: 3433 3138 3936 2c31 322e 3833 3936 3920  431896,12.83969 
+00003670: 312e 3033 3531 3437 362c 3134 2e36 3335  1.0351476,14.635
+00003680: 3339 3420 4320 302e 3737 3434 3537 3135  394 C 0.77445715
+00003690: 2c31 362e 3239 3835 3832 2031 2e39 3532  ,16.298582 1.952
+000036a0: 3838 3437 2c31 372e 3939 3138 3335 2033  8847,17.991835 3
+000036b0: 2e35 3839 3539 3633 2c31 382e 3335 3734  .5895963,18.3574
+000036c0: 3539 2043 2035 2e34 3237 3636 3632 2c31  59 C 5.4276662,1
+000036d0: 382e 3939 3431 3635 2037 2e36 3636 3138  8.994165 7.66618
+000036e0: 3339 2c31 372e 3936 3835 3334 2038 2e32  39,17.968534 8.2
+000036f0: 3937 3930 3339 2c31 362e 3131 3031 3632  979039,16.110162
+00003700: 2043 2038 2e38 3537 3130 3235 2c31 342e   C 8.8571025,14.
+00003710: 3731 3635 3237 2038 2e35 3436 3534 3831  716527 8.5465481
+00003720: 2c31 332e 3138 3631 3339 2038 2e30 3238  ,13.186139 8.028
+00003730: 3938 3638 2c31 312e 3833 3236 3533 2043  9868,11.832653 C
+00003740: 2037 2e34 3730 3238 3835 2c31 302e 3230   7.4702885,10.20
+00003750: 3638 3834 2036 2e32 3535 3336 3633 2c38  6884 6.2553663,8
+00003760: 2e38 3730 3936 3734 2035 2e39 3239 3930  .8709674 5.92990
+00003770: 3536 2c37 2e31 3532 3538 3338 2043 2035  56,7.1525838 C 5
+00003780: 2e34 3931 3436 2c35 2e34 3932 3939 3635  .49146,5.4929965
+00003790: 2035 2e38 3837 3534 3938 2c33 2e35 3733   5.8875498,3.573
+000037a0: 3536 3239 2037 2e32 3332 3936 3037 2c32  5629 7.2329607,2
+000037b0: 2e34 3332 3732 3133 2043 2038 2e37 3338  .4327213 C 8.738
+000037c0: 3835 3931 2c31 2e30 3133 3434 3531 2031  8591,1.0134451 1
+000037d0: 312e 3331 3839 3331 2c30 2e37 3535 3730  1.318931,0.75570
+000037e0: 3832 2031 322e 3931 3938 3138 2c32 2e31  82 12.919818,2.1
+000037f0: 3632 3737 3233 2043 2031 342e 3839 3131  627723 C 14.8911
+00003800: 3734 2c33 2e36 3736 3933 3435 2031 352e  74,3.6769345 15.
+00003810: 3239 3530 3635 2c36 2e35 3639 3230 3238  295065,6.5692028
+00003820: 2031 342e 3333 3032 3337 2c38 2e37 3637   14.330237,8.767
+00003830: 3139 3333 2043 2031 332e 3931 3034 3834  1933 C 13.910484
+00003840: 2c39 2e39 3139 3336 3538 2031 332e 3135  ,9.9193658 13.15
+00003850: 3433 3533 2c31 302e 3930 3236 3739 2031  4353,10.902679 1
+00003860: 322e 3631 3538 3737 2c31 312e 3939 3132  2.615877,11.9912
+00003870: 3939 2043 2031 322e 3033 3830 3435 2c31  99 C 12.038045,1
+00003880: 332e 3534 3832 3620 3132 2e30 3830 3539  3.54826 12.08059
+00003890: 392c 3135 2e33 3634 3831 3320 3132 2e37  9,15.364813 12.7
+000038a0: 3737 3435 352c 3136 2e38 3735 3136 3320  77455,16.875163 
+000038b0: 4320 3134 2e30 3736 3934 362c 3139 2e31  C 14.076946,19.1
+000038c0: 3130 3934 3320 3137 2e39 3033 3337 362c  10943 17.903376,
+000038d0: 3138 2e39 3435 3033 3320 3139 2e30 3432  18.945033 19.042
+000038e0: 3037 382c 3136 2e36 3238 3730 3320 4320  078,16.628703 C 
+000038f0: 3139 2e37 3537 3234 322c 3135 2e32 3631  19.757242,15.261
+00003900: 3232 3720 3139 2e33 3036 3831 392c 3133  227 19.306819,13
+00003910: 2e32 3434 3932 3920 3137 2e37 3635 392c  .244929 17.7659,
+00003920: 3132 2e36 3731 3930 3220 4320 3136 2e37  12.671902 C 16.7
+00003930: 3538 3335 2c31 322e 3231 3039 3631 2031  5835,12.210961 1
+00003940: 352e 3436 3230 3933 2c31 322e 3434 3239  5.462093,12.4429
+00003950: 3531 2031 342e 3732 3933 3636 2c31 332e  51 14.729366,13.
+00003960: 3239 3030 3134 2043 2031 352e 3637 3938  290014 C 15.6798
+00003970: 3439 2c31 332e 3237 3631 3533 2031 362e  49,13.276153 16.
+00003980: 3938 3032 3934 2c31 332e 3236 3237 3534  980294,13.262754
+00003990: 2031 372e 3334 3335 3032 2c31 342e 3336   17.343502,14.36
+000039a0: 3432 3033 2043 2031 372e 3930 3332 3633  4203 C 17.903263
+000039b0: 2c31 352e 3439 3236 3739 2031 372e 3736  ,15.492679 17.76
+000039c0: 3936 3737 2c31 372e 3330 3539 3732 2031  9677,17.305972 1
+000039d0: 362e 3431 3439 3439 2c31 372e 3738 3138  6.414949,17.7818
+000039e0: 3935 2043 2031 352e 3231 3834 3138 2c31  95 C 15.218418,1
+000039f0: 382e 3133 3038 3420 3134 2e31 3530 3330  8.13084 14.15030
+00003a00: 332c 3136 2e39 3032 3934 3720 3134 2e30  3,16.902947 14.0
+00003a10: 3932 3138 342c 3135 2e37 3831 3636 3620  92184,15.781666 
+00003a20: 4320 3133 2e37 3832 3131 372c 3134 2e31  C 13.782117,14.1
+00003a30: 3031 3430 3320 3134 2e31 3430 3334 362c  01403 14.140346,
+00003a40: 3132 2e32 3730 3331 3520 3135 2e32 3735  12.270315 15.275
+00003a50: 3139 2c31 302e 3935 3830 3432 2043 2031  19,10.958042 C 1
+00003a60: 362e 3531 3938 3933 2c39 2e34 3934 3837  6.519893,9.49487
+00003a70: 3633 2031 372e 3235 3635 3235 2c37 2e35  63 17.256525,7.5
+00003a80: 3234 3036 3539 2031 362e 3836 3735 3236  240659 16.867526
+00003a90: 2c35 2e35 3939 3437 3531 2043 2031 362e  ,5.5994751 C 16.
+00003aa0: 3336 3430 392c 322e 3536 3537 3234 3920  36409,2.5657249 
+00003ab0: 3133 2e36 3035 3030 312c 302e 3036 3537  13.605001,0.0657
+00003ac0: 3630 3534 3320 3130 2e35 3037 3330 392c  60543 10.507309,
+00003ad0: 2d30 2e30 3034 3735 3437 3236 3520 4320  -0.0047547265 C 
+00003ae0: 392e 3934 3130 3733 2c2d 302e 3031 3538  9.941073,-0.0158
+00003af0: 3330 3639 3220 392e 3337 3232 3539 342c  30692 9.3722594,
+00003b00: 302e 3030 3933 3437 3836 3139 2038 2e38  0.0093478619 8.8
+00003b10: 3039 3630 3436 2c30 2e30 3735 3636 3638  096046,0.0756668
+00003b20: 3937 207a 220a 2020 2020 2020 2020 2020  97 z".          
+00003b30: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003b40: 2020 7374 796c 653d 2266 696c 6c3a 2024    style="fill: $
+00003b50: 706c 616e 6574 735f 636f 6c6f 725f 3130  planets_color_10
+00003b60: 220a 2020 2020 2020 2020 2020 2020 2020  ".              
+00003b70: 2020 2020 2020 2020 2020 2f3e 0a20 2020            />.   
+00003b80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003b90: 203c 2f67 3e0a 2020 2020 2020 2020 2020   </g>.          
+00003ba0: 2020 2020 2020 3c2f 7379 6d62 6f6c 3e0a        </symbol>.
+00003bb0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003bc0: 3c73 796d 626f 6c20 6964 3d22 5472 7565  <symbol id="True
+00003bd0: 5f4e 6f64 6522 3e0a 2020 2020 2020 2020  _Node">.        
+00003be0: 2020 2020 2020 2020 2020 2020 3c67 2074              <g t
+00003bf0: 7261 6e73 666f 726d 3d22 7472 616e 736c  ransform="transl
+00003c00: 6174 6528 302c 3329 223e 0a20 2020 2020  ate(0,3)">.     
+00003c10: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003c20: 2020 203c 7061 7468 0a20 2020 2020 2020     <path.       
+00003c30: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00003c40: 2020 2020 2064 3d22 4d20 382e 3830 3936       d="M 8.8096
+00003c50: 3034 362c 302e 3037 3536 3636 3839 3720  046,0.075666897 
+00003c60: 4320 362e 3431 3537 3533 362c 302e 3636  C 6.4157536,0.66
+00003c70: 3132 3339 3632 2034 2e33 3736 3737 3639  123962 4.3767769
+00003c80: 2c32 2e35 3330 3638 3337 2033 2e36 3633  ,2.5306837 3.663
+00003c90: 3436 3536 2c34 2e39 3030 3735 3134 2043  4656,4.9007514 C
+00003ca0: 2033 2e30 3533 3630 3731 2c36 2e36 3830   3.0536071,6.680
+00003cb0: 3932 3634 2033 2e36 3836 3836 3832 2c38  9264 3.6868682,8
+00003cc0: 2e36 3233 3839 3031 2034 2e35 3837 3839  .6238901 4.58789
+00003cd0: 3838 2c31 302e 3138 3634 3337 2043 2035  88,10.186437 C 5
+00003ce0: 2e31 3332 3339 3937 2c31 312e 3132 3436  .1323997,11.1246
+00003cf0: 3232 2035 2e39 3631 3537 3533 2c31 312e  22 5.9615753,11.
+00003d00: 3930 3839 3520 362e 3139 3037 3330 322c  90895 6.1907302,
+00003d10: 3133 2e30 3037 3930 3620 4320 362e 3539  13.007906 C 6.59
+00003d20: 3137 3230 322c 3134 2e34 3834 3438 3820  17202,14.484488 
+00003d30: 362e 3438 3837 3135 362c 3136 2e33 3837  6.4887156,16.387
+00003d40: 3532 3320 352e 3137 3233 3738 382c 3137  523 5.1723788,17
+00003d50: 2e33 3832 3537 3620 4320 342e 3333 3239  .382576 C 4.3329
+00003d60: 3937 342c 3138 2e30 3533 3431 3320 332e  974,18.053413 3.
+00003d70: 3037 3735 3734 312c 3137 2e34 3535 3033  0775741,17.45503
+00003d80: 3420 322e 3832 3030 3133 362c 3136 2e34  4 2.8200136,16.4
+00003d90: 3831 3139 3620 4320 322e 3339 3136 3535  81196 C 2.391655
+00003da0: 322c 3135 2e31 3030 3739 3320 332e 3332  2,15.100793 3.32
+00003db0: 3331 3839 382c 3133 2e33 3936 3435 3620  31898,13.396456 
+00003dc0: 342e 3737 3933 3331 362c 3133 2e31 3633  4.7793316,13.163
+00003dd0: 3830 3620 4320 352e 3531 3537 3836 312c  806 C 5.5157861,
+00003de0: 3133 2e34 3438 3438 3920 352e 3733 3632  13.448489 5.7362
+00003df0: 3335 332c 3133 2e30 3038 3333 3120 342e  353,13.008331 4.
+00003e00: 3938 3830 3531 2c31 322e 3733 3931 3031  988051,12.739101
+00003e10: 2043 2033 2e34 3736 3736 3936 2c31 312e   C 3.4767696,11.
+00003e20: 3938 3037 3631 2031 2e32 3433 3138 3936  980761 1.2431896
+00003e30: 2c31 322e 3833 3936 3920 312e 3033 3531  ,12.83969 1.0351
+00003e40: 3437 362c 3134 2e36 3335 3339 3420 4320  476,14.635394 C 
+00003e50: 302e 3737 3434 3537 3135 2c31 362e 3239  0.77445715,16.29
+00003e60: 3835 3832 2031 2e39 3532 3838 3437 2c31  8582 1.9528847,1
+00003e70: 372e 3939 3138 3335 2033 2e35 3839 3539  7.991835 3.58959
+00003e80: 3633 2c31 382e 3335 3734 3539 2043 2035  63,18.357459 C 5
+00003e90: 2e34 3237 3636 3632 2c31 382e 3939 3431  .4276662,18.9941
+00003ea0: 3635 2037 2e36 3636 3138 3339 2c31 372e  65 7.6661839,17.
+00003eb0: 3936 3835 3334 2038 2e32 3937 3930 3339  968534 8.2979039
+00003ec0: 2c31 362e 3131 3031 3632 2043 2038 2e38  ,16.110162 C 8.8
+00003ed0: 3537 3130 3235 2c31 342e 3731 3635 3237  571025,14.716527
+00003ee0: 2038 2e35 3436 3534 3831 2c31 332e 3138   8.5465481,13.18
+00003ef0: 3631 3339 2038 2e30 3238 3938 3638 2c31  6139 8.0289868,1
+00003f00: 312e 3833 3236 3533 2043 2037 2e34 3730  1.832653 C 7.470
+00003f10: 3238 3835 2c31 302e 3230 3638 3834 2036  2885,10.206884 6
+00003f20: 2e32 3535 3336 3633 2c38 2e38 3730 3936  .2553663,8.87096
+00003f30: 3734 2035 2e39 3239 3930 3536 2c37 2e31  74 5.9299056,7.1
+00003f40: 3532 3538 3338 2043 2035 2e34 3931 3436  525838 C 5.49146
+00003f50: 2c35 2e34 3932 3939 3635 2035 2e38 3837  ,5.4929965 5.887
+00003f60: 3534 3938 2c33 2e35 3733 3536 3239 2037  5498,3.5735629 7
+00003f70: 2e32 3332 3936 3037 2c32 2e34 3332 3732  .2329607,2.43272
+00003f80: 3133 2043 2038 2e37 3338 3835 3931 2c31  13 C 8.7388591,1
+00003f90: 2e30 3133 3434 3531 2031 312e 3331 3839  .0134451 11.3189
+00003fa0: 3331 2c30 2e37 3535 3730 3832 2031 322e  31,0.7557082 12.
+00003fb0: 3931 3938 3138 2c32 2e31 3632 3737 3233  919818,2.1627723
+00003fc0: 2043 2031 342e 3839 3131 3734 2c33 2e36   C 14.891174,3.6
+00003fd0: 3736 3933 3435 2031 352e 3239 3530 3635  769345 15.295065
+00003fe0: 2c36 2e35 3639 3230 3238 2031 342e 3333  ,6.5692028 14.33
+00003ff0: 3032 3337 2c38 2e37 3637 3139 3333 2043  0237,8.7671933 C
+00004000: 2031 332e 3931 3034 3834 2c39 2e39 3139   13.910484,9.919
+00004010: 3336 3538 2031 332e 3135 3433 3533 2c31  3658 13.154353,1
+00004020: 302e 3930 3236 3739 2031 322e 3631 3538  0.902679 12.6158
+00004030: 3737 2c31 312e 3939 3132 3939 2043 2031  77,11.991299 C 1
+00004040: 322e 3033 3830 3435 2c31 332e 3534 3832  2.038045,13.5482
+00004050: 3620 3132 2e30 3830 3539 392c 3135 2e33  6 12.080599,15.3
+00004060: 3634 3831 3320 3132 2e37 3737 3435 352c  64813 12.777455,
+00004070: 3136 2e38 3735 3136 3320 4320 3134 2e30  16.875163 C 14.0
+00004080: 3736 3934 362c 3139 2e31 3130 3934 3320  76946,19.110943 
+00004090: 3137 2e39 3033 3337 362c 3138 2e39 3435  17.903376,18.945
+000040a0: 3033 3320 3139 2e30 3432 3037 382c 3136  033 19.042078,16
+000040b0: 2e36 3238 3730 3320 4320 3139 2e37 3537  .628703 C 19.757
+000040c0: 3234 322c 3135 2e32 3631 3232 3720 3139  242,15.261227 19
+000040d0: 2e33 3036 3831 392c 3133 2e32 3434 3932  .306819,13.24492
+000040e0: 3920 3137 2e37 3635 392c 3132 2e36 3731  9 17.7659,12.671
+000040f0: 3930 3220 4320 3136 2e37 3538 3335 2c31  902 C 16.75835,1
+00004100: 322e 3231 3039 3631 2031 352e 3436 3230  2.210961 15.4620
+00004110: 3933 2c31 322e 3434 3239 3531 2031 342e  93,12.442951 14.
+00004120: 3732 3933 3636 2c31 332e 3239 3030 3134  729366,13.290014
+00004130: 2043 2031 352e 3637 3938 3439 2c31 332e   C 15.679849,13.
+00004140: 3237 3631 3533 2031 362e 3938 3032 3934  276153 16.980294
+00004150: 2c31 332e 3236 3237 3534 2031 372e 3334  ,13.262754 17.34
+00004160: 3335 3032 2c31 342e 3336 3432 3033 2043  3502,14.364203 C
+00004170: 2031 372e 3930 3332 3633 2c31 352e 3439   17.903263,15.49
+00004180: 3236 3739 2031 372e 3736 3936 3737 2c31  2679 17.769677,1
+00004190: 372e 3330 3539 3732 2031 362e 3431 3439  7.305972 16.4149
+000041a0: 3439 2c31 372e 3738 3138 3935 2043 2031  49,17.781895 C 1
+000041b0: 352e 3231 3834 3138 2c31 382e 3133 3038  5.218418,18.1308
+000041c0: 3420 3134 2e31 3530 3330 332c 3136 2e39  4 14.150303,16.9
+000041d0: 3032 3934 3720 3134 2e30 3932 3138 342c  02947 14.092184,
+000041e0: 3135 2e37 3831 3636 3620 4320 3133 2e37  15.781666 C 13.7
+000041f0: 3832 3131 372c 3134 2e31 3031 3430 3320  82117,14.101403 
+00004200: 3134 2e31 3430 3334 362c 3132 2e32 3730  14.140346,12.270
+00004210: 3331 3520 3135 2e32 3735 3139 2c31 302e  315 15.27519,10.
+00004220: 3935 3830 3432 2043 2031 362e 3531 3938  958042 C 16.5198
+00004230: 3933 2c39 2e34 3934 3837 3633 2031 372e  93,9.4948763 17.
+00004240: 3235 3635 3235 2c37 2e35 3234 3036 3539  256525,7.5240659
+00004250: 2031 362e 3836 3735 3236 2c35 2e35 3939   16.867526,5.599
+00004260: 3437 3531 2043 2031 362e 3336 3430 392c  4751 C 16.36409,
+00004270: 322e 3536 3537 3234 3920 3133 2e36 3035  2.5657249 13.605
+00004280: 3030 312c 302e 3036 3537 3630 3534 3320  001,0.065760543 
+00004290: 3130 2e35 3037 3330 392c 2d30 2e30 3034  10.507309,-0.004
+000042a0: 3735 3437 3236 3520 4320 392e 3934 3130  7547265 C 9.9410
+000042b0: 3733 2c2d 302e 3031 3538 3330 3639 3220  73,-0.015830692 
+000042c0: 392e 3337 3232 3539 342c 302e 3030 3933  9.3722594,0.0093
+000042d0: 3437 3836 3139 2038 2e38 3039 3630 3436  478619 8.8096046
+000042e0: 2c30 2e30 3735 3636 3638 3937 207a 220a  ,0.075666897 z".
+000042f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00004300: 2020 2020 2020 2020 2020 2020 7374 796c              styl
+00004310: 653d 2266 696c 6c3a 2024 706c 616e 6574  e="fill: $planet
+00004320: 735f 636f 6c6f 725f 3131 220a 2020 2020  s_color_11".    
+00004330: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00004340: 2020 2020 2f3e 0a20 2020 2020 2020 2020      />.         
+00004350: 2020 2020 2020 2020 2020 203c 2f67 3e0a             </g>.
+00004360: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00004370: 3c2f 7379 6d62 6f6c 3e0a 2020 2020 2020  </symbol>.      
+00004380: 2020 2020 2020 2020 2020 3c73 796d 626f            <symbo
+00004390: 6c20 6964 3d22 4368 6972 6f6e 223e 0a09  l id="Chiron">..
+000043a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000043b0: 3c70 6174 680a 0920 2020 2020 2020 2020  <path..         
+000043c0: 2020 2020 2020 2020 2064 3d22 4d20 3130           d="M 10
+000043d0: 2e30 3139 3837 332c 3133 2e30 3638 3938  .019873,13.06898
+000043e0: 3120 4c20 3130 2e31 3835 3534 322c 302e  1 L 10.185542,0.
+000043f0: 3830 3935 3134 3331 204d 2031 302e 3139  80951431 M 10.19
+00004400: 3535 3931 2c36 2e37 3434 3239 3031 204c  5591,6.7442901 L
+00004410: 2031 352e 3439 3639 3833 2c32 2e32 3731   15.496983,2.271
+00004420: 3234 3038 204d 2031 302e 3231 3438 3331  2408 M 10.214831
+00004430: 2c36 2e36 3332 3137 3236 204c 2031 352e  ,6.6321726 L 15.
+00004440: 3531 3632 3137 2c31 312e 3130 3532 3136  516217,11.105216
+00004450: 204d 2031 372e 3139 3239 3334 2c31 372e   M 17.192934,17.
+00004460: 3939 3837 3734 2043 2031 372e 3139 3239  998774 C 17.1929
+00004470: 3334 2c32 302e 3836 3436 2031 342e 3836  34,20.8646 14.86
+00004480: 3730 3532 2c32 332e 3139 3034 3837 2031  7052,23.190487 1
+00004490: 322e 3030 3132 3236 2c32 332e 3139 3034  2.001226,23.1904
+000044a0: 3837 2043 2039 2e31 3335 3339 3838 2c32  87 C 9.1353988,2
+000044b0: 332e 3139 3034 3837 2036 2e38 3039 3531  3.190487 6.80951
+000044c0: 3238 2c32 302e 3836 3436 2036 2e38 3039  28,20.8646 6.809
+000044d0: 3531 3238 2c31 372e 3939 3837 3734 2043  5128,17.998774 C
+000044e0: 2036 2e38 3039 3531 3238 2c31 352e 3133   6.8095128,15.13
+000044f0: 3239 3533 2039 2e31 3335 3339 3838 2c31  2953 9.1353988,1
+00004500: 322e 3830 3730 3636 2031 322e 3030 3132  2.807066 12.0012
+00004510: 3236 2c31 322e 3830 3730 3636 2043 2031  26,12.807066 C 1
+00004520: 342e 3836 3730 3532 2c31 322e 3830 3730  4.867052,12.8070
+00004530: 3636 2031 372e 3139 3239 3334 2c31 352e  66 17.192934,15.
+00004540: 3133 3239 3533 2031 372e 3139 3239 3334  132953 17.192934
+00004550: 2c31 372e 3939 3837 3734 207a 2022 0a09  ,17.998774 z "..
+00004560: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00004570: 2020 7374 796c 653d 2273 7472 6f6b 653a    style="stroke:
+00004580: 2024 706c 616e 6574 735f 636f 6c6f 725f   $planets_color_
+00004590: 3136 3b73 7472 6f6b 652d 7769 6474 683a  16;stroke-width:
+000045a0: 3270 783b 2066 696c 6c3a 6e6f 6e65 3b22  2px; fill:none;"
+000045b0: 202f 3e0a 2020 2020 2020 2020 2020 2020   />.            
+000045c0: 2020 2020 3c2f 7379 6d62 6f6c 3e0a 2020      </symbol>.  
+000045d0: 2020 2020 2020 2020 2020 2020 2020 3c73                <s
+000045e0: 796d 626f 6c20 6964 3d22 4669 7273 745f  ymbol id="First_
+000045f0: 486f 7573 6522 3e0a 2020 2020 2020 2020  House">.        
+00004600: 2020 2020 2020 2020 2020 2020 3c74 6578              <tex
+00004610: 7420 793d 2232 3022 2073 7479 6c65 3d22  t y="20" style="
+00004620: 666f 6e74 2d73 697a 653a 2032 3270 783b  font-size: 22px;
+00004630: 2066 696c 6c3a 2024 706c 616e 6574 735f   fill: $planets_
+00004640: 636f 6c6f 725f 3132 223e 4173 3c2f 7465  color_12">As</te
+00004650: 7874 3e0a 2020 2020 2020 2020 2020 2020  xt>.            
+00004660: 2020 2020 3c2f 7379 6d62 6f6c 3e0a 2020      </symbol>.  
+00004670: 2020 2020 2020 2020 2020 2020 2020 3c73                <s
+00004680: 796d 626f 6c20 6964 3d22 5465 6e74 685f  ymbol id="Tenth_
+00004690: 486f 7573 6522 3e0a 2020 2020 2020 2020  House">.        
+000046a0: 2020 2020 2020 2020 2020 2020 3c74 6578              <tex
+000046b0: 7420 793d 2232 3022 2073 7479 6c65 3d22  t y="20" style="
+000046c0: 666f 6e74 2d73 697a 653a 2032 3070 783b  font-size: 20px;
+000046d0: 2066 696c 6c3a 2024 706c 616e 6574 735f   fill: $planets_
+000046e0: 636f 6c6f 725f 3133 223e 4d63 3c2f 7465  color_13">Mc</te
+000046f0: 7874 3e0a 2020 2020 2020 2020 2020 2020  xt>.            
+00004700: 2020 2020 3c2f 7379 6d62 6f6c 3e0a 2020      </symbol>.  
+00004710: 2020 2020 2020 2020 2020 2020 2020 3c73                <s
+00004720: 796d 626f 6c20 6964 3d22 5365 7665 6e74  ymbol id="Sevent
+00004730: 685f 486f 7573 6522 3e0a 2020 2020 2020  h_House">.      
+00004740: 2020 2020 2020 2020 2020 2020 2020 3c74                <t
+00004750: 6578 7420 793d 2232 3022 2073 7479 6c65  ext y="20" style
+00004760: 3d22 666f 6e74 2d73 697a 653a 2032 3270  ="font-size: 22p
+00004770: 783b 2066 696c 6c3a 2024 706c 616e 6574  x; fill: $planet
+00004780: 735f 636f 6c6f 725f 3134 223e 4473 3c2f  s_color_14">Ds</
+00004790: 7465 7874 3e0a 2020 2020 2020 2020 2020  text>.          
+000047a0: 2020 2020 2020 3c2f 7379 6d62 6f6c 3e0a        </symbol>.
+000047b0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000047c0: 3c73 796d 626f 6c20 6964 3d22 466f 7572  <symbol id="Four
+000047d0: 7468 5f48 6f75 7365 223e 0a20 2020 2020  th_House">.     
+000047e0: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+000047f0: 7465 7874 2079 3d22 3230 2220 7374 796c  text y="20" styl
+00004800: 653d 2266 6f6e 742d 7369 7a65 3a20 3232  e="font-size: 22
+00004810: 7078 3b20 6669 6c6c 3a20 2470 6c61 6e65  px; fill: $plane
+00004820: 7473 5f63 6f6c 6f72 5f31 3522 3e49 633c  ts_color_15">Ic<
+00004830: 2f74 6578 743e 0a20 2020 2020 2020 2020  /text>.         
+00004840: 2020 2020 2020 203c 2f73 796d 626f 6c3e         </symbol>
+00004850: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00004860: 203c 212d 2d20 5a6f 6469 6163 202d 2d3e   <!-- Zodiac -->
+00004870: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00004880: 203c 7379 6d62 6f6c 2069 643d 2261 7269   <symbol id="ari
+00004890: 6573 223e 0a20 2020 2020 2020 2020 2020  es">.           
+000048a0: 2020 2020 2020 2020 203c 7061 7468 0a20           <path. 
+000048b0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000048c0: 2020 2020 2020 2064 3d22 4d20 3134 2e38         d="M 14.8
+000048d0: 3333 3533 362c 3331 2043 2031 342e 3833  33536,31 C 14.83
+000048e0: 3231 3836 2c32 392e 3732 3832 3520 3134  2186,29.72825 14
+000048f0: 2e38 3435 3933 362c 3238 2e34 3535 3834  .845936,28.45584
+00004900: 2031 342e 3738 3033 3436 2c32 372e 3138   14.780346,27.18
+00004910: 3532 3320 4320 3134 2e36 3430 3932 362c  523 C 14.640926,
+00004920: 3234 2e32 3330 3436 2031 342e 3237 3139  24.23046 14.2719
+00004930: 3237 2c32 312e 3238 3937 3920 3133 2e37  27,21.28979 13.7
+00004940: 3631 3635 372c 3138 2e33 3737 3620 4320  61657,18.3776 C 
+00004950: 3133 2e33 3231 3938 372c 3135 2e39 3139  13.321987,15.919
+00004960: 3131 2031 322e 3738 3737 3837 2c31 332e  11 12.787787,13.
+00004970: 3436 3938 3320 3131 2e39 3930 3531 372c  46983 11.990517,
+00004980: 3131 2e31 3030 3735 2043 2031 312e 3533  11.10075 C 11.53
+00004990: 3032 3637 2c39 2e37 3632 3433 2031 302e  0267,9.76243 10.
+000049a0: 3939 3238 3837 2c38 2e34 3439 3132 2031  992887,8.44912 1
+000049b0: 302e 3335 3730 3837 2c37 2e31 3834 3920  0.357087,7.1849 
+000049c0: 4320 392e 3737 3634 3036 352c 362e 3035  C 9.7764065,6.05
+000049d0: 3420 392e 3131 3433 3436 352c 342e 3934  4 9.1143465,4.94
+000049e0: 3239 3620 382e 3231 3630 3036 352c 342e  296 8.2160065,4.
+000049f0: 3033 3439 3420 4320 372e 3632 3832 3436  03494 C 7.628246
+00004a00: 352c 332e 3434 3635 2036 2e39 3030 3732  5,3.4465 6.90072
+00004a10: 3635 2c32 2e39 3435 3335 2036 2e30 3634  65,2.94535 6.064
+00004a20: 3937 3635 2c32 2e38 3136 3234 2043 2035  9765,2.81624 C 5
+00004a30: 2e33 3233 3732 3636 2c32 2e37 3031 3432  .3237266,2.70142
+00004a40: 2034 2e35 3330 3436 3636 2c32 2e38 3735   4.5304666,2.875
+00004a50: 3731 2033 2e39 3335 3639 3636 2c33 2e33  71 3.9356966,3.3
+00004a60: 3433 3834 2043 2033 2e32 3133 3635 3635  4384 C 3.2136565
+00004a70: 2c33 2e39 3035 3139 2032 2e37 3635 3433  ,3.90519 2.76543
+00004a80: 3635 2c34 2e37 3536 3235 2032 2e35 3433  65,4.75625 2.543
+00004a90: 3833 3635 2c35 2e36 3332 3839 2043 2032  8365,5.63289 C 2
+00004aa0: 2e33 3035 3337 3635 2c36 2e35 3939 3935  .3053765,6.59995
+00004ab0: 2032 2e32 3935 3937 3635 2c37 2e36 3133   2.2959765,7.613
+00004ac0: 3538 2032 2e34 3239 3231 3635 2c38 2e35  58 2.4292165,8.5
+00004ad0: 3937 3320 4320 322e 3634 3634 3436 352c  973 C 2.6464465,
+00004ae0: 3130 2e31 3535 3837 2033 2e32 3638 3936  10.15587 3.26896
+00004af0: 3635 2c31 312e 3633 3235 3820 342e 3038  65,11.63258 4.08
+00004b00: 3135 3436 362c 3132 2e39 3639 3038 2043  15466,12.96908 C
+00004b10: 2033 2e32 3932 3434 3635 2c31 322e 3936   3.2924465,12.96
+00004b20: 3930 3820 322e 3530 3333 3436 352c 3132  908 2.5033465,12
+00004b30: 2e39 3639 3038 2031 2e37 3134 3234 3635  .96908 1.7142465
+00004b40: 2c31 322e 3936 3930 3820 4320 302e 3839  ,12.96908 C 0.89
+00004b50: 3732 3436 3531 2c31 312e 3438 3438 3120  724651,11.48481 
+00004b60: 302e 3235 3739 3936 3531 2c39 2e38 3732  0.25799651,9.872
+00004b70: 3939 2030 2e30 3630 3235 3635 3134 2c38  99 0.060256514,8
+00004b80: 2e31 3738 3939 2043 202d 302e 3037 3132  .17899 C -0.0712
+00004b90: 3033 3438 362c 372e 3030 3639 3520 302e  03486,7.00695 0.
+00004ba0: 3030 3337 3136 3531 3338 2c35 2e37 3939  0037165138,5.799
+00004bb0: 3033 2030 2e33 3731 3439 3635 312c 342e  03 0.37149651,4.
+00004bc0: 3637 3432 3120 4320 302e 3736 3434 3236  67421 C 0.764426
+00004bd0: 3531 2c33 2e34 3734 3939 2031 2e35 3139  51,3.47499 1.519
+00004be0: 3538 3635 2c32 2e33 3933 3220 322e 3532  5865,2.3932 2.52
+00004bf0: 3332 3536 352c 312e 3633 3034 2043 2033  32565,1.6304 C 3
+00004c00: 2e32 3830 3936 3635 2c31 2e30 3534 3738  .2809665,1.05478
+00004c10: 2034 2e32 3035 3933 3636 2c30 2e37 3132   4.2059366,0.712
+00004c20: 3638 2035 2e31 3531 3934 3636 2c30 2e36  68 5.1519466,0.6
+00004c30: 3337 3831 2043 2036 2e31 3933 3832 3635  3781 C 6.1938265
+00004c40: 2c30 2e35 3434 3936 2037 2e32 3631 3034  ,0.54496 7.26104
+00004c50: 3635 2c30 2e37 3436 3139 2038 2e31 3930  65,0.74619 8.190
+00004c60: 3932 3635 2c31 2e32 3239 3736 2043 2039  9265,1.22976 C 9
+00004c70: 2e33 3939 3836 3635 2c31 2e38 3530 3231  .3998665,1.85021
+00004c80: 2031 302e 3336 3336 3737 2c32 2e38 3539   10.363677,2.859
+00004c90: 3434 2031 312e 3134 3532 3737 2c33 2e39  44 11.145277,3.9
+00004ca0: 3537 3636 2043 2031 322e 3139 3033 3437  5766 C 12.190347
+00004cb0: 2c35 2e34 3431 3437 2031 322e 3936 3530  ,5.44147 12.9650
+00004cc0: 3637 2c37 2e31 3031 3031 2031 332e 3538  67,7.10101 13.58
+00004cd0: 3432 3837 2c38 2e38 3033 3832 2043 2031  4287,8.80382 C 1
+00004ce0: 342e 3633 3037 3636 2c31 312e 3731 3736  4.630766,11.7176
+00004cf0: 2031 352e 3231 3236 3236 2c31 342e 3737   15.212626,14.77
+00004d00: 3836 3120 3135 2e35 3735 3134 362c 3137  861 15.575146,17
+00004d10: 2e38 3437 3935 2043 2031 352e 3636 3438  .84795 C 15.6648
+00004d20: 3336 2c31 382e 3631 3634 3820 3135 2e37  36,18.61648 15.7
+00004d30: 3339 3535 362c 3139 2e33 3836 3735 2031  39556,19.38675 1
+00004d40: 352e 3830 3134 3436 2c32 302e 3135 3830  5.801446,20.1580
+00004d50: 3320 4320 3135 2e39 3333 3630 362c 3230  3 C 15.933606,20
+00004d60: 2e31 3538 3033 2031 362e 3036 3537 3736  .15803 16.065776
+00004d70: 2c32 302e 3135 3830 3320 3136 2e31 3937  ,20.15803 16.197
+00004d80: 3933 362c 3230 2e31 3538 3033 2043 2031  936,20.15803 C 1
+00004d90: 362e 3433 3135 3136 2c31 362e 3738 3333  6.431516,16.7833
+00004da0: 3220 3136 2e39 3139 3036 362c 3133 2e34  2 16.919066,13.4
+00004db0: 3037 3631 2031 372e 3932 3032 3336 2c31  0761 17.920236,1
+00004dc0: 302e 3137 3032 3920 4320 3138 2e35 3336  0.17029 C 18.536
+00004dd0: 3734 362c 382e 3139 3838 3620 3139 2e33  746,8.19886 19.3
+00004de0: 3433 3231 362c 362e 3237 3333 2032 302e  43216,6.2733 20.
+00004df0: 3436 3031 3036 2c34 2e35 3332 3039 2043  460106,4.53209 C
+00004e00: 2032 312e 3233 3239 3636 2c33 2e33 3432   21.232966,3.342
+00004e10: 3436 2032 322e 3137 3833 3936 2c32 2e32  46 22.178396,2.2
+00004e20: 3236 3931 2032 332e 3339 3332 3336 2c31  2691 23.393236,1
+00004e30: 2e34 3734 3733 2043 2032 342e 3330 3339  .47473 C 24.3039
+00004e40: 3436 2c30 2e39 3036 2032 352e 3337 3534  46,0.906 25.3754
+00004e50: 3036 2c30 2e35 3933 3135 2032 362e 3434  06,0.59315 26.44
+00004e60: 3938 3336 2c30 2e36 3137 3434 2043 2032  9836,0.61744 C 2
+00004e70: 372e 3430 3630 3736 2c30 2e36 3236 3520  7.406076,0.6265 
+00004e80: 3238 2e33 3636 3333 362c 302e 3838 3431  28.366336,0.8841
+00004e90: 3420 3239 2e31 3733 3338 362c 312e 3430  4 29.173386,1.40
+00004ea0: 3537 3120 4320 3239 2e39 3138 3237 362c  571 C 29.918276,
+00004eb0: 312e 3838 3431 3720 3330 2e35 3336 3732  1.88417 30.53672
+00004ec0: 362c 322e 3534 3832 3520 3331 2e30 3037  6,2.54825 31.007
+00004ed0: 3330 362c 332e 3239 3638 3820 4320 3331  306,3.29688 C 31
+00004ee0: 2e36 3430 3337 362c 342e 3330 3938 3120  .640376,4.30981 
+00004ef0: 3331 2e39 3432 3738 362c 352e 3530 3336  31.942786,5.5036
+00004f00: 2033 312e 3939 3035 3236 2c36 2e36 3931   31.990526,6.691
+00004f10: 3439 2043 2033 322e 3036 3433 3636 2c38  49 C 32.064366,8
+00004f20: 2e32 3438 3938 2033 312e 3730 3033 3036  .24898 31.700306
+00004f30: 2c39 2e37 3938 3431 2033 312e 3131 3831  ,9.79841 31.1181
+00004f40: 3336 2c31 312e 3233 3430 3920 4320 3330  36,11.23409 C 30
+00004f50: 2e38 3738 3035 362c 3131 2e38 3237 3734  .878056,11.82774
+00004f60: 2033 302e 3630 3037 3436 2c31 322e 3430   30.600746,12.40
+00004f70: 3538 3420 3330 2e32 3936 3739 362c 3132  584 30.296796,12
+00004f80: 2e39 3639 3038 2043 2032 392e 3530 3338  .96908 C 29.5038
+00004f90: 3036 2c31 322e 3936 3930 3820 3238 2e37  06,12.96908 28.7
+00004fa0: 3130 3832 362c 3132 2e39 3639 3038 2032  10826,12.96908 2
+00004fb0: 372e 3931 3738 3336 2c31 322e 3936 3930  7.917836,12.9690
+00004fc0: 3820 4320 3238 2e36 3935 3634 362c 3131  8 C 28.695646,11
+00004fd0: 2e35 3638 3235 2032 392e 3333 3039 3036  .56825 29.330906
+00004fe0: 2c31 302e 3036 3034 3420 3239 2e35 3635  ,10.06044 29.565
+00004ff0: 3735 362c 382e 3436 3438 3520 4320 3239  756,8.46485 C 29
+00005000: 2e37 3035 3433 362c 372e 3439 3035 3320  .705436,7.49053 
+00005010: 3239 2e36 3839 3937 362c 362e 3438 3733  29.689976,6.4873
+00005020: 3920 3239 2e34 3639 3733 362c 352e 3532  9 29.469736,5.52
+00005030: 3631 3620 4320 3239 2e32 3636 3538 362c  616 C 29.266586,
+00005040: 342e 3637 3239 3620 3238 2e38 3730 3935  4.67296 28.87095
+00005050: 362c 332e 3833 3335 3420 3238 2e32 3031  6,3.83354 28.201
+00005060: 3237 362c 332e 3235 3037 3920 4320 3237  276,3.25079 C 27
+00005070: 2e37 3138 3338 362c 322e 3832 3236 3320  .718386,2.82263 
+00005080: 3237 2e30 3738 3436 362c 322e 3539 3032  27.078466,2.5902
+00005090: 3120 3236 2e34 3336 3231 362c 322e 3538  1 26.436216,2.58
+000050a0: 3434 3620 4320 3235 2e36 3830 3330 362c  446 C 25.680306,
+000050b0: 322e 3536 3035 3920 3234 2e39 3530 3038  2.56059 24.95008
+000050c0: 362c 322e 3837 3330 3320 3234 2e33 3538  6,2.87303 24.358
+000050d0: 3333 362c 332e 3332 3837 3920 4320 3233  336,3.32879 C 23
+000050e0: 2e34 3934 3535 362c 332e 3939 3330 3720  .494556,3.99307 
+000050f0: 3232 2e38 3434 3938 362c 342e 3839 3139  22.844986,4.8919
+00005100: 3820 3232 2e32 3832 3935 362c 352e 3831  8 22.282956,5.81
+00005110: 3637 3920 4320 3231 2e34 3531 3735 362c  679 C 21.451756,
+00005120: 372e 3231 3037 3220 3230 2e38 3131 3433  7.21072 20.81143
+00005130: 362c 382e 3731 3031 3820 3230 2e32 3530  6,8.71018 20.250
+00005140: 3339 362c 3130 2e32 3331 3234 2043 2031  396,10.23124 C 1
+00005150: 392e 3433 3735 3836 2c31 322e 3439 3830  9.437586,12.4980
+00005160: 3220 3138 2e38 3933 3332 362c 3134 2e38  2 18.893326,14.8
+00005170: 3531 3636 2031 382e 3434 3032 3836 2c31  5166 18.440286,1
+00005180: 372e 3231 3433 3220 4320 3137 2e38 3339  7.21432 C 17.839
+00005190: 3031 362c 3230 2e34 3033 3235 2031 372e  016,20.40325 17.
+000051a0: 3431 3332 3136 2c32 332e 3632 3931 2031  413216,23.6291 1
+000051b0: 372e 3234 3631 3336 2c32 362e 3837 3135  7.246136,26.8715
+000051c0: 2043 2031 372e 3138 3337 3936 2c32 382e   C 17.183796,28.
+000051d0: 3031 3835 3720 3137 2e31 3733 3936 362c  01857 17.173966,
+000051e0: 3239 2e31 3637 3435 2031 372e 3137 3735  29.16745 17.1775
+000051f0: 3136 2c33 302e 3331 3539 3520 4320 3137  16,30.31595 C 17
+00005200: 2e31 3737 3531 362c 3330 2e35 3433 3937  .177516,30.54397
+00005210: 2031 372e 3137 3735 3136 2c33 302e 3737   17.177516,30.77
+00005220: 3139 3820 3137 2e31 3737 3531 362c 3331  198 17.177516,31
+00005230: 2043 2031 362e 3339 3631 3836 2c33 3120   C 16.396186,31 
+00005240: 3135 2e36 3134 3835 362c 3331 2031 342e  15.614856,31 14.
+00005250: 3833 3335 3336 2c33 3120 7a22 0a20 2020  833536,31 z".   
+00005260: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00005270: 2020 2020 2073 7479 6c65 3d22 6669 6c6c       style="fill
+00005280: 3a20 247a 6f64 6961 635f 636f 6c6f 725f  : $zodiac_color_
+00005290: 3022 0a20 2020 2020 2020 2020 2020 2020  0".             
+000052a0: 2020 2020 2020 202f 3e0a 2020 2020 2020         />.      
+000052b0: 2020 2020 2020 2020 2020 3c2f 7379 6d62            </symb
+000052c0: 6f6c 3e0a 2020 2020 2020 2020 2020 2020  ol>.            
+000052d0: 2020 2020 3c73 796d 626f 6c20 6964 3d22      <symbol id="
+000052e0: 7461 7572 7573 223e 0a20 2020 2020 2020  taurus">.       
+000052f0: 2020 2020 2020 2020 2020 2020 203c 7061               <pa
+00005300: 7468 0a20 2020 2020 2020 2020 2020 2020  th.             
+00005310: 2020 2020 2020 2020 2020 2064 3d22 4d20             d="M 
+00005320: 3131 2e32 3131 3132 352c 3131 2e39 3630  11.211125,11.960
+00005330: 3034 3320 4320 392e 3938 3536 3139 372c  043 C 9.9856197,
+00005340: 3131 2e34 3832 3038 3520 382e 3832 3733  11.482085 8.8273
+00005350: 3530 372c 3130 2e37 3537 3236 3320 372e  507,10.757263 7.
+00005360: 3939 3934 3136 342c 392e 3732 3236 3620  9994164,9.72266 
+00005370: 4320 362e 3935 3430 3538 342c 382e 3434  C 6.9540584,8.44
+00005380: 3839 3530 3820 362e 3231 3139 3532 342c  89508 6.2119524,
+00005390: 362e 3936 3936 3039 3720 352e 3430 3638  6.9696097 5.4068
+000053a0: 3139 392c 352e 3534 3232 3531 3520 4320  199,5.5422515 C 
+000053b0: 342e 3931 3533 3333 362c 342e 3634 3335  4.9153336,4.6435
+000053c0: 3933 3120 342e 3335 3838 3435 322c 332e  931 4.3588452,3.
+000053d0: 3736 3034 3132 3820 332e 3630 3032 3638  7604128 3.600268
+000053e0: 362c 332e 3036 3031 3033 3620 4320 332e  6,3.0601036 C 3.
+000053f0: 3038 3737 3337 312c 322e 3538 3330 3339  0877371,2.583039
+00005400: 3920 322e 3436 3939 3433 332c 322e 3139  9 2.4699433,2.19
+00005410: 3737 3132 3920 312e 3737 3931 3332 312c  77129 1.7791321,
+00005420: 322e 3034 3632 3137 3820 4320 312e 3435  2.0462178 C 1.45
+00005430: 3134 3836 372c 312e 3936 3633 3435 3120  14867,1.9663451 
+00005440: 312e 3131 3237 3639 382c 312e 3936 3334  1.1127698,1.9634
+00005450: 3036 3520 302e 3737 3735 3636 3438 2c31  065 0.77756648,1
+00005460: 2e39 3639 3332 3033 2043 2030 2e36 3737  .9693203 C 0.677
+00005470: 3530 3133 382c 312e 3938 3234 3830 3320  50138,1.9824803 
+00005480: 302e 3539 3833 3335 3038 2c31 2e39 3734  0.59833508,1.974
+00005490: 3735 3935 2030 2e36 3333 3639 3038 382c  7595 0.63369088,
+000054a0: 312e 3835 3238 3333 3320 4320 302e 3633  1.8528333 C 0.63
+000054b0: 3336 3930 3838 2c31 2e32 3730 3336 3138  369088,1.2703618
+000054c0: 2030 2e36 3333 3639 3038 382c 302e 3638   0.63369088,0.68
+000054d0: 3738 3930 3233 2030 2e36 3333 3639 3038  789023 0.6336908
+000054e0: 382c 302e 3130 3534 3030 3434 2043 2031  8,0.10540044 C 1
+000054f0: 2e31 3736 3933 2c30 2e31 3131 3738 3838  .17693,0.1117888
+00005500: 3420 312e 3732 3130 3239 322c 302e 3039  4 1.7210292,0.09
+00005510: 3031 3539 3634 3120 322e 3236 3336 3039  0159641 2.263609
+00005520: 352c 302e 3132 3136 3939 3834 2043 2033  5,0.12169984 C 3
+00005530: 2e33 3439 3337 3339 2c30 2e32 3132 3038  .3493739,0.21208
+00005540: 3539 3420 342e 3336 3635 3132 392c 302e  594 4.3665129,0.
+00005550: 3731 3538 3731 3231 2035 2e31 3931 3739  71587121 5.19179
+00005560: 3335 2c31 2e34 3039 3735 3535 2043 2036  35,1.4097555 C 6
+00005570: 2e32 3634 3738 3434 2c32 2e33 3031 3333  .2647844,2.30133
+00005580: 3220 372e 3038 3838 3735 342c 332e 3434  2 7.0888754,3.44
+00005590: 3934 3832 3720 372e 3739 3131 3631 342c  94827 7.7911614,
+000055a0: 342e 3634 3336 3437 3920 4320 382e 3239  4.6436479 C 8.29
+000055b0: 3133 3033 342c 352e 3530 3436 3838 2038  13034,5.504688 8
+000055c0: 2e37 3732 3137 3537 2c36 2e33 3736 3735  .7721757,6.37675
+000055d0: 3235 2039 2e32 3734 3331 3237 2c37 2e32  25 9.2743127,7.2
+000055e0: 3336 3630 3632 2043 2039 2e37 3538 3830  366062 C 9.75880
+000055f0: 3837 2c38 2e30 3436 3335 3639 2031 302e  87,8.0463569 10.
+00005600: 3330 3736 3438 2c38 2e38 3234 3738 3635  307648,8.8247865
+00005610: 2031 302e 3937 3135 3339 2c39 2e34 3938   10.971539,9.498
+00005620: 3939 3438 2043 2031 312e 3535 3837 3137  9948 C 11.558717
+00005630: 2c31 302e 3039 3436 3939 2031 322e 3236  ,10.094699 12.26
+00005640: 3135 372c 3130 2e35 3836 3936 3720 3133  157,10.586967 13
+00005650: 2e30 3532 3934 2c31 302e 3837 3131 3339  .05294,10.871139
+00005660: 2043 2031 342e 3135 3039 3636 2c31 312e   C 14.150966,11.
+00005670: 3237 3633 3632 2031 352e 3333 3930 3436  276362 15.339046
+00005680: 2c31 312e 3335 3935 3536 2031 362e 3530  ,11.359556 16.50
+00005690: 3032 3434 2c31 312e 3331 3436 3337 2043  0244,11.314637 C
+000056a0: 2031 372e 3534 3332 3034 2c31 312e 3236   17.543204,11.26
+000056b0: 3236 3732 2031 382e 3630 3230 3638 2c31  2672 18.602068,1
+000056c0: 312e 3036 3936 3136 2031 392e 3532 3937  1.069616 19.5297
+000056d0: 3932 2c31 302e 3537 3137 3435 2043 2032  92,10.571745 C 2
+000056e0: 302e 3430 3133 3335 2c31 302e 3131 3436  0.401335,10.1146
+000056f0: 3637 2032 312e 3130 3338 3034 2c39 2e33  67 21.103804,9.3
+00005700: 3937 3039 3134 2032 312e 3730 3030 342c  970914 21.70004,
+00005710: 382e 3632 3637 3635 3920 4320 3232 2e33  8.6267659 C 22.3
+00005720: 3835 3038 372c 372e 3734 3131 3934 3620  85087,7.7411946 
+00005730: 3232 2e39 3036 3937 2c36 2e37 3437 3733  22.90697,6.74773
+00005740: 3331 2032 332e 3437 3237 2c35 2e37 3835  31 23.4727,5.785
+00005750: 3930 3331 2043 2032 332e 3937 3332 3939  9031 C 23.973299
+00005760: 2c34 2e39 3332 3134 3538 2032 342e 3434  ,4.9321458 24.44
+00005770: 3535 3136 2c34 2e30 3538 3630 3238 2032  5516,4.0586028 2
+00005780: 352e 3033 3232 3931 2c33 2e32 3538 3930  5.032291,3.25890
+00005790: 3931 2043 2032 352e 3731 3138 3636 2c32  91 C 25.711866,2
+000057a0: 2e33 3234 3738 3633 2032 362e 3531 3636  .3247863 26.5166
+000057b0: 3332 2c31 2e34 3535 3832 3437 2032 372e  32,1.4558247 27.
+000057c0: 3530 3737 3636 2c30 2e38 3435 3939 3237  507766,0.8459927
+000057d0: 3720 4320 3238 2e32 3636 3437 312c 302e  7 C 28.266471,0.
+000057e0: 3338 3332 3338 3934 2032 392e 3134 3633  38323894 29.1463
+000057f0: 3737 2c30 2e30 3936 3534 3830 3431 2033  77,0.096548041 3
+00005800: 302e 3034 3038 3332 2c30 2e31 3036 3635  0.040832,0.10665
+00005810: 3938 3420 4320 3330 2e34 3530 3432 362c  984 C 30.450426,
+00005820: 302e 3130 3230 3630 3234 2033 302e 3836  0.10206024 30.86
+00005830: 3030 3734 2c30 2e31 3037 3933 3735 3420  0074,0.10793754 
+00005840: 3331 2e32 3639 3636 372c 302e 3130 3534  31.269667,0.1054
+00005850: 3030 3434 2043 2033 312e 3236 3936 3637  0044 C 31.269667
+00005860: 2c30 2e37 3236 3731 3331 3520 3331 2e32  ,0.72671315 31.2
+00005870: 3639 3636 372c 312e 3334 3830 3235 3820  69667,1.3480258 
+00005880: 3331 2e32 3639 3636 372c 312e 3936 3933  31.269667,1.9693
+00005890: 3230 3320 4320 3330 2e38 3336 3534 2c31  203 C 30.83654,1
+000058a0: 2e39 3636 3130 3738 2033 302e 3339 3533  .9661078 30.3953
+000058b0: 3631 2c31 2e39 3538 3336 3838 2032 392e  61,1.9583688 29.
+000058c0: 3937 3630 3638 2c32 2e30 3834 3035 3520  976068,2.084055 
+000058d0: 4320 3239 2e31 3139 3933 342c 322e 3331  C 29.119934,2.31
+000058e0: 3836 3731 3820 3238 2e34 3030 3438 332c  86718 28.400483,
+000058f0: 322e 3839 3235 3634 3620 3237 2e38 3236  2.8925646 27.826
+00005900: 3933 392c 332e 3535 3137 3639 3320 4320  939,3.5517693 C 
+00005910: 3237 2e32 3336 3032 382c 342e 3232 3335  27.236028,4.2235
+00005920: 3836 3520 3236 2e37 3838 3236 312c 352e  865 26.788261,5.
+00005930: 3030 3238 3337 3420 3236 2e33 3631 3636  0028374 26.36166
+00005940: 362c 352e 3738 3433 3639 3920 4320 3235  6,5.7843699 C 25
+00005950: 2e36 3233 3131 2c37 2e31 3031 3038 3139  .62311,7.1010819
+00005960: 2032 342e 3932 3631 3638 2c38 2e34 3534   24.926168,8.454
+00005970: 3339 2032 332e 3937 3439 3436 2c39 2e36  39 23.974946,9.6
+00005980: 3335 3732 3337 2043 2032 332e 3539 3335  357237 C 23.5935
+00005990: 3534 2c31 302e 3131 3532 3838 2032 332e  54,10.115288 23.
+000059a0: 3135 3231 3138 2c31 302e 3534 3738 3136  152118,10.547816
+000059b0: 2032 322e 3635 3235 3036 2c31 302e 3930   22.652506,10.90
+000059c0: 3433 3431 2043 2032 322e 3034 3938 312c  4341 C 22.04981,
+000059d0: 3131 2e33 3431 3236 3720 3231 2e33 3833  11.341267 21.383
+000059e0: 3337 352c 3131 2e36 3835 3332 3620 3230  375,11.685326 20
+000059f0: 2e36 3932 3231 362c 3131 2e39 3630 3034  .692216,11.96004
+00005a00: 3320 4320 3232 2e33 3438 3938 312c 3132  3 C 22.348981,12
+00005a10: 2e38 3635 3235 3420 3233 2e38 3238 3330  .865254 23.82830
+00005a20: 382c 3134 2e31 3232 3634 3620 3234 2e38  8,14.122646 24.8
+00005a30: 3936 3333 392c 3135 2e36 3834 3033 3120  96339,15.684031 
+00005a40: 4320 3235 2e37 3936 3530 342c 3136 2e39  C 25.796504,16.9
+00005a50: 3836 3038 3720 3236 2e33 3934 3331 342c  86087 26.394314,
+00005a60: 3138 2e34 3939 3135 3820 3236 2e35 3932  18.499158 26.592
+00005a70: 3934 332c 3230 2e30 3730 3039 2043 2032  943,20.07009 C 2
+00005a80: 362e 3738 3636 3332 2c32 312e 3535 3231  6.786632,21.5521
+00005a90: 3531 2032 362e 3637 3934 3438 2c32 332e  51 26.679448,23.
+00005aa0: 3037 3737 3820 3236 2e32 3436 3339 342c  07778 26.246394,
+00005ab0: 3234 2e35 3130 3139 3420 4320 3235 2e37  24.510194 C 25.7
+00005ac0: 3934 3132 352c 3235 2e39 3931 3033 3220  94125,25.991032 
+00005ad0: 3234 2e39 3736 3338 342c 3237 2e33 3439  24.976384,27.349
+00005ae0: 3530 3520 3233 2e39 3235 3937 352c 3238  505 23.925975,28
+00005af0: 2e34 3835 3030 3720 4320 3232 2e36 3635  .485007 C 22.665
+00005b00: 3634 362c 3239 2e38 3636 3135 2032 312e  646,29.86615 21.
+00005b10: 3038 3539 3938 2c33 302e 3938 3437 3332  085998,30.984732
+00005b20: 2031 392e 3330 3132 3432 2c33 312e 3537   19.301242,31.57
+00005b30: 3639 3332 2043 2031 372e 3535 3232 3038  6932 C 17.552208
+00005b40: 2c33 322e 3135 3734 3134 2031 352e 3635  ,32.157414 15.65
+00005b50: 3238 3032 2c33 322e 3234 3636 3134 2031  2802,32.246614 1
+00005b60: 332e 3834 3630 3836 2c33 312e 3930 3237  3.846086,31.9027
+00005b70: 3536 2043 2031 322e 3232 3031 3933 2c33  56 C 12.220193,3
+00005b80: 312e 3538 3434 3839 2031 302e 3638 3537  1.584489 10.6857
+00005b90: 3635 2c33 302e 3834 3538 3520 392e 3430  65,30.84585 9.40
+00005ba0: 3038 3736 372c 3239 2e38 3035 3632 3520  08767,29.805625 
+00005bb0: 4320 382e 3330 3031 3432 342c 3238 2e39  C 8.3001424,28.9
+00005bc0: 3233 3330 3320 372e 3333 3534 3639 342c  23303 7.3354694,
+00005bd0: 3237 2e38 3631 3831 3520 362e 3630 3637  27.861815 6.6067
+00005be0: 3737 342c 3236 2e36 3532 3935 3620 4320  774,26.652956 C 
+00005bf0: 352e 3834 3135 3032 372c 3235 2e33 3735  5.8415027,25.375
+00005c00: 3233 3120 352e 3337 3036 3538 392c 3233  231 5.3706589,23
+00005c10: 2e39 3233 3431 3520 352e 3234 3738 3436  .923415 5.247846
+00005c20: 382c 3232 2e34 3339 3731 3220 4320 352e  8,22.439712 C 5.
+00005c30: 3038 3233 3538 382c 3230 2e35 3936 3620  0823588,20.5966 
+00005c40: 352e 3339 3339 3931 352c 3138 2e37 3031  5.3939915,18.701
+00005c50: 3435 2036 2e32 3136 3237 3034 2c31 372e  45 6.2162704,17.
+00005c60: 3033 3732 3132 2043 2037 2e31 3136 3633  037212 C 7.11663
+00005c70: 3634 2c31 352e 3139 3133 3632 2038 2e35  64,15.191362 8.5
+00005c80: 3634 3332 3234 2c31 332e 3633 3439 3935  643224,13.634995
+00005c90: 2031 302e 3238 3335 3436 2c31 322e 3531   10.283546,12.51
+00005ca0: 3735 3633 2043 2031 302e 3538 3532 3937  7563 C 10.585297
+00005cb0: 2c31 322e 3331 3937 3434 2031 302e 3839  ,12.319744 10.89
+00005cc0: 3530 3038 2c31 322e 3133 3430 3632 2031  5008,12.134062 1
+00005cd0: 312e 3231 3131 3235 2c31 312e 3936 3030  1.211125,11.9600
+00005ce0: 3433 207a 204d 2031 352e 3935 3739 322c  43 z M 15.95792,
+00005cf0: 3239 2e36 3035 3330 3520 4320 3137 2e34  29.605305 C 17.4
+00005d00: 3639 3637 342c 3239 2e36 3133 3933 3820  69674,29.613938 
+00005d10: 3138 2e39 3935 3730 332c 3239 2e32 3238  18.995703,29.228
+00005d20: 3036 3420 3230 2e32 3737 3937 342c 3238  064 20.277974,28
+00005d30: 2e34 3138 3133 2043 2032 312e 3238 3234  .41813 C 21.2824
+00005d40: 3331 2c32 372e 3738 3934 3632 2032 322e  31,27.789462 22.
+00005d50: 3135 3336 3237 2c32 362e 3935 3235 3333  153627,26.952533
+00005d60: 2032 322e 3833 3739 3432 2c32 352e 3938   22.837942,25.98
+00005d70: 3737 3635 2043 2032 332e 3539 3634 3038  7765 C 23.596408
+00005d80: 2c32 342e 3930 3135 3236 2032 342e 3035  ,24.901526 24.05
+00005d90: 3635 3833 2c32 332e 3631 3237 3935 2032  6583,23.612795 2
+00005da0: 342e 3136 3031 3434 2c32 322e 3239 3332  4.160144,22.2932
+00005db0: 3138 2043 2032 342e 3239 3937 3535 2c32  18 C 24.299755,2
+00005dc0: 302e 3639 3333 3031 2032 342e 3030 3932  0.693301 24.0092
+00005dd0: 3232 2c31 392e 3033 3638 3032 2032 332e  22,19.036802 23.
+00005de0: 3231 3332 3034 2c31 372e 3633 3037 3831  213204,17.630781
+00005df0: 2043 2032 322e 3633 3532 3836 2c31 362e   C 22.635286,16.
+00005e00: 3539 3739 3320 3231 2e38 3233 3731 322c  59793 21.823712,
+00005e10: 3135 2e37 3031 3935 3520 3230 2e38 3832  15.701955 20.882
+00005e20: 3335 342c 3134 2e39 3836 3232 3320 4320  354,14.986223 C 
+00005e30: 3139 2e39 3537 3836 392c 3134 2e32 3835  19.957869,14.285
+00005e40: 3731 3320 3138 2e38 3734 3333 372c 3133  713 18.874337,13
+00005e50: 2e37 3936 3536 3620 3137 2e37 3334 3830  .796566 17.73480
+00005e60: 372c 3133 2e35 3732 3931 3920 4320 3136  7,13.572919 C 16
+00005e70: 2e35 3630 3537 392c 3133 2e33 3339 3330  .560579,13.33930
+00005e80: 3620 3135 2e33 3339 3535 392c 3133 2e33  6 15.339559,13.3
+00005e90: 3435 3534 3820 3134 2e31 3635 3434 312c  45548 14.165441,
+00005ea0: 3133 2e35 3736 3037 3720 4320 3132 2e38  13.576077 C 12.8
+00005eb0: 3832 3031 372c 3133 2e38 3336 3438 3420  82017,13.836484 
+00005ec0: 3131 2e36 3730 3834 322c 3134 2e34 3238  11.670842,14.428
+00005ed0: 3030 3920 3130 2e36 3731 3233 342c 3135  009 10.671234,15
+00005ee0: 2e32 3731 3138 2043 2039 2e34 3337 3437  .27118 C 9.43747
+00005ef0: 3637 2c31 362e 3239 3439 3034 2038 2e34  67,16.294904 8.4
+00005f00: 3639 3038 3834 2c31 372e 3636 3339 3634  690884,17.663964
+00005f10: 2038 2e30 3239 3335 3534 2c31 392e 3231   8.0293554,19.21
+00005f20: 3137 3838 2043 2037 2e36 3533 3135 3934  1788 C 7.6531594
+00005f30: 2c32 302e 3532 3336 3633 2037 2e36 3133  ,20.523663 7.613
+00005f40: 3333 3834 2c32 312e 3932 3637 3832 2037  3384,21.926782 7
+00005f50: 2e38 3834 3233 3534 2c32 332e 3236 3235  .8842354,23.2625
+00005f60: 3439 2043 2038 2e31 3530 3934 3134 2c32  49 C 8.1509414,2
+00005f70: 342e 3533 3232 3631 2038 2e37 3631 3238  4.532261 8.76128
+00005f80: 3737 2c32 352e 3732 3337 3235 2039 2e36  77,25.723725 9.6
+00005f90: 3230 3834 3337 2c32 362e 3639 3538 3836  208437,26.695886
+00005fa0: 2043 2031 302e 3530 3232 3838 2c32 372e   C 10.502288,27.
+00005fb0: 3730 3630 3132 2031 312e 3539 3734 3034  706012 11.597404
+00005fc0: 2c32 382e 3535 3033 3838 2031 322e 3835  ,28.550388 12.85
+00005fd0: 3430 3733 2c32 392e 3033 3938 3038 2043  4073,29.039808 C
+00005fe0: 2031 332e 3833 3830 372c 3239 2e34 3333   13.83807,29.433
+00005ff0: 3138 3520 3134 2e39 3030 3333 372c 3239  185 14.900337,29
+00006000: 2e36 3036 3630 3120 3135 2e39 3537 3932  .606601 15.95792
+00006010: 2c32 392e 3630 3533 3035 207a 220a 2020  ,29.605305 z".  
+00006020: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00006030: 2020 2020 2020 7374 796c 653d 2266 696c        style="fil
+00006040: 6c3a 2024 7a6f 6469 6163 5f63 6f6c 6f72  l: $zodiac_color
+00006050: 5f31 220a 2020 2020 2020 2020 2020 2020  _1".            
+00006060: 2020 2020 2020 2020 2f3e 0a20 2020 2020          />.     
+00006070: 2020 2020 2020 2020 2020 203c 2f73 796d             </sym
+00006080: 626f 6c3e 0a20 2020 2020 2020 2020 2020  bol>.           
+00006090: 2020 2020 203c 7379 6d62 6f6c 2069 643d       <symbol id=
+000060a0: 2267 656d 696e 6922 3e0a 2020 2020 2020  "gemini">.      
+000060b0: 2020 2020 2020 2020 2020 2020 2020 3c70                <p
+000060c0: 6174 680a 2020 2020 2020 2020 2020 2020  ath.            
+000060d0: 2020 2020 2020 2020 2020 2020 643d 224d              d="M
+000060e0: 2030 2e35 3635 3439 3239 322c 3332 2043   0.56549292,32 C
+000060f0: 2030 2e35 3635 3439 3239 322c 3331 2e32   0.56549292,31.2
+00006100: 3134 3233 3820 302e 3536 3534 3932 3932  14238 0.56549292
+00006110: 2c33 302e 3432 3834 3635 2030 2e35 3635  ,30.428465 0.565
+00006120: 3439 3239 322c 3239 2e36 3432 3730 3320  49292,29.642703 
+00006130: 4320 322e 3936 3735 3131 392c 3239 2e30  C 2.9675119,29.0
+00006140: 3131 3131 3620 352e 3430 3233 3537 332c  11116 5.4023573,
+00006150: 3238 2e34 3836 3135 3520 372e 3836 3937  28.486155 7.8697
+00006160: 3730 342c 3238 2e31 3838 3739 3220 4320  704,28.188792 C 
+00006170: 372e 3836 3937 3730 342c 3230 2e30 3438  7.8697704,20.048
+00006180: 3831 3720 372e 3836 3937 3730 342c 3131  817 7.8697704,11
+00006190: 2e39 3038 3833 3220 372e 3836 3937 3730  .908832 7.869770
+000061a0: 342c 332e 3736 3838 3537 3120 4320 352e  4,3.7688571 C 5.
+000061b0: 3339 3736 3134 362c 332e 3533 3839 3537  3976146,3.538957
+000061c0: 3120 322e 3935 3030 3632 392c 332e 3036  1 2.9500629,3.06
+000061d0: 3136 3339 3120 302e 3536 3534 3932 3932  16391 0.56549292
+000061e0: 2c32 2e33 3731 3431 3038 2043 2030 2e35  ,2.3714108 C 0.5
+000061f0: 3635 3439 3239 322c 312e 3538 3039 3432  6549292,1.580942
+00006200: 3320 302e 3536 3534 3932 3932 2c30 2e37  3 0.56549292,0.7
+00006210: 3930 3437 3339 2030 2e35 3635 3439 3239  904739 0.5654929
+00006220: 322c 2d35 652d 3036 2043 2034 2e31 3330  2,-5e-06 C 4.130
+00006230: 3034 3539 2c30 2e39 3830 3933 3036 2037  0459,0.9809306 7
+00006240: 2e38 3138 3430 3738 2c31 2e34 3336 3235  .8184078,1.43625
+00006250: 3220 3131 2e35 3032 3830 332c 312e 3634  2 11.502803,1.64
+00006260: 3238 3639 3520 4320 3134 2e36 3939 3431  28695 C 14.69941
+00006270: 2c31 2e38 3131 3535 3734 2031 372e 3930  ,1.8115574 17.90
+00006280: 3537 332c 312e 3830 3730 3438 3220 3231  573,1.8070482 21
+00006290: 2e31 3031 3631 312c 312e 3632 3430 3735  .101611,1.624075
+000062a0: 3820 4320 3234 2e36 3737 3233 342c 312e  8 C 24.677234,1.
+000062b0: 3430 3831 3931 2032 382e 3235 3437 3432  408191 28.254742
+000062c0: 2c30 2e39 3532 3536 3839 2033 312e 3731  ,0.9525689 31.71
+000062d0: 3434 3236 2c2d 3565 2d30 3620 4320 3331  4426,-5e-06 C 31
+000062e0: 2e37 3134 3432 362c 302e 3739 3034 3733  .714426,0.790473
+000062f0: 3920 3331 2e37 3134 3432 362c 312e 3538  9 31.714426,1.58
+00006300: 3039 3432 3320 3331 2e37 3134 3432 362c  09423 31.714426,
+00006310: 322e 3337 3134 3130 3820 4320 3239 2e33  2.3714108 C 29.3
+00006320: 3234 3530 322c 332e 3035 3933 3438 3120  24502,3.0593481 
+00006330: 3236 2e38 3732 3832 392c 332e 3533 3836  26.872829,3.5386
+00006340: 3637 3120 3234 2e33 3936 3034 352c 332e  671 24.396045,3.
+00006350: 3736 3838 3537 3120 4320 3234 2e33 3936  7688571 C 24.396
+00006360: 3034 352c 3131 2e39 3038 3833 3220 3234  045,11.908832 24
+00006370: 2e33 3936 3034 352c 3230 2e30 3438 3831  .396045,20.04881
+00006380: 3720 3234 2e33 3936 3034 352c 3238 2e31  7 24.396045,28.1
+00006390: 3838 3739 3220 4320 3236 2e38 3638 3033  88792 C 26.86803
+000063a0: 352c 3238 2e34 3836 3730 3420 3239 2e33  5,28.486704 29.3
+000063b0: 3037 3136 372c 3239 2e30 3133 3135 3820  07167,29.013158 
+000063c0: 3331 2e37 3134 3432 362c 3239 2e36 3432  31.714426,29.642
+000063d0: 3730 3320 4320 3331 2e37 3134 3432 362c  703 C 31.714426,
+000063e0: 3330 2e34 3238 3436 3520 3331 2e37 3134  30.428465 31.714
+000063f0: 3432 362c 3331 2e32 3134 3233 3820 3331  426,31.214238 31
+00006400: 2e37 3134 3432 362c 3332 2043 2032 362e  .714426,32 C 26.
+00006410: 3037 3137 372c 3330 2e35 3132 3836 3620  07177,30.512866 
+00006420: 3230 2e32 3036 3433 322c 3239 2e39 3933  20.206432,29.993
+00006430: 3932 3820 3134 2e33 3833 3237 312c 3330  928 14.383271,30
+00006440: 2e31 3239 3237 3820 4320 392e 3732 3831  .129278 C 9.7281
+00006450: 3533 362c 3330 2e32 3430 3139 3620 352e  536,30.240196 5.
+00006460: 3037 3231 3334 392c 3330 2e38 3038 3737  0721349,30.80877
+00006470: 3720 302e 3536 3534 3932 3932 2c33 3220  7 0.56549292,32 
+00006480: 7a20 4d20 3130 2e37 3034 3035 332c 3238  z M 10.704053,28
+00006490: 2e30 3139 3431 2043 2031 322e 3938 3434  .01941 C 12.9844
+000064a0: 3438 2c32 372e 3736 3533 3637 2031 352e  48,27.765367 15.
+000064b0: 3238 3332 3234 2c32 372e 3732 3237 3833  283224,27.722783
+000064c0: 2031 372e 3537 3535 3339 2c32 372e 3736   17.575539,27.76
+000064d0: 3638 3038 2043 2031 382e 3930 3638 3836  6808 C 18.906886
+000064e0: 2c32 372e 3739 3639 3132 2032 302e 3233  ,27.796912 20.23
+000064f0: 3831 342c 3237 2e38 3730 3036 3520 3231  814,27.870065 21
+00006500: 2e35 3631 3736 322c 3238 2e30 3139 3431  .561762,28.01941
+00006510: 2043 2032 312e 3536 3137 3632 2c32 302e   C 21.561762,20.
+00006520: 3030 3137 3636 2032 312e 3536 3137 3632  001766 21.561762
+00006530: 2c31 312e 3938 3431 3231 2032 312e 3536  ,11.984121 21.56
+00006540: 3137 3632 2c33 2e39 3636 3437 3731 2043  1762,3.9664771 C
+00006550: 2031 392e 3138 3933 3038 2c34 2e31 3231   19.189308,4.121
+00006560: 3037 3731 2031 362e 3831 3030 3831 2c34  0771 16.810081,4
+00006570: 2e31 3339 3331 3131 2031 342e 3433 3335  .1393111 14.4335
+00006580: 3135 2c34 2e31 3039 3336 3331 2043 2031  15,4.1093631 C 1
+00006590: 332e 3138 3935 3236 2c34 2e30 3930 3038  3.189526,4.09008
+000065a0: 3231 2031 312e 3934 3535 3035 2c34 2e30  21 11.945505,4.0
+000065b0: 3530 3230 3431 2031 302e 3730 3430 3533  502041 10.704053
+000065c0: 2c33 2e39 3636 3437 3731 2043 2031 302e  ,3.9664771 C 10.
+000065d0: 3730 3430 3533 2c31 312e 3938 3431 3231  704053,11.984121
+000065e0: 2031 302e 3730 3430 3533 2c32 302e 3030   10.704053,20.00
+000065f0: 3137 3636 2031 302e 3730 3430 3533 2c32  1766 10.704053,2
+00006600: 382e 3031 3934 3120 7a20 220a 2020 2020  8.01941 z ".    
+00006610: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00006620: 2020 2020 7374 796c 653d 2266 696c 6c3a      style="fill:
+00006630: 2024 7a6f 6469 6163 5f63 6f6c 6f72 5f32   $zodiac_color_2
+00006640: 220a 2020 2020 2020 2020 2020 2020 2020  ".              
+00006650: 2020 2020 2020 2f3e 0a20 2020 2020 2020        />.       
+00006660: 2020 2020 2020 2020 203c 2f73 796d 626f           </symbo
+00006670: 6c3e 0a20 2020 2020 2020 2020 2020 2020  l>.             
+00006680: 2020 203c 7379 6d62 6f6c 2069 643d 2263     <symbol id="c
+00006690: 616e 6365 7222 3e0a 2020 2020 2020 2020  ancer">.        
+000066a0: 2020 2020 2020 2020 2020 2020 3c70 6174              <pat
+000066b0: 680a 2020 2020 2020 2020 2020 2020 2020  h.              
+000066c0: 2020 2020 2020 2020 2020 643d 224d 2030            d="M 0
+000066d0: 2c32 352e 3632 3934 3832 204c 2030 2c32  ,25.629482 L 0,2
+000066e0: 322e 3930 3831 3031 2043 2035 2e32 3437  2.908101 C 5.247
+000066f0: 3935 3039 2c32 352e 3330 3439 3134 2031  9509,25.304914 1
+00006700: 302e 3333 3334 3634 2c32 362e 3439 3038  0.333464,26.4908
+00006710: 3337 2031 352e 3233 3135 3531 2c32 362e  37 15.231551,26.
+00006720: 3439 3038 3337 2043 2031 382e 3434 3237  490837 C 18.4427
+00006730: 3937 2c32 362e 3439 3038 3337 2032 312e  97,26.490837 21.
+00006740: 3035 3432 3737 2c32 362e 3037 3838 3834  054277,26.078884
+00006750: 2032 332e 3036 3539 3932 2c32 352e 3234   23.065992,25.24
+00006760: 3234 3937 2043 2032 312e 3739 3134 3839  2497 C 21.791489
+00006770: 2c32 342e 3539 3333 3620 3230 2e38 3239  ,24.59336 20.829
+00006780: 3336 352c 3233 2e37 3639 3435 3520 3230  365,23.769455 20
+00006790: 2e31 3932 3131 342c 3232 2e37 3833 3236  .192114,22.78326
+000067a0: 3720 4320 3139 2e35 3534 3836 332c 3231  7 C 19.554863,21
+000067b0: 2e37 3937 3037 3820 3139 2e32 3239 3939  .797078 19.22999
+000067c0: 2c32 302e 3633 3631 3232 2031 392e 3232  ,20.636122 19.22
+000067d0: 3939 392c 3139 2e33 3030 3339 3820 4320  999,19.300398 C 
+000067e0: 3139 2e32 3239 3939 2c31 372e 3535 3237  19.22999,17.5527
+000067f0: 3232 2031 392e 3836 3732 3431 2c31 362e  22 19.867241,16.
+00006800: 3035 3437 3134 2032 312e 3132 3932 3438  054714 21.129248
+00006810: 2c31 342e 3739 3338 3931 2043 2032 322e  ,14.793891 C 22.
+00006820: 3337 3837 362c 3133 2e35 3435 3535 3120  37876,13.545551 
+00006830: 3233 2e39 3033 3136 352c 3132 2e39 3231  23.903165,12.921
+00006840: 3338 3120 3235 2e36 3532 3438 312c 3132  381 25.652481,12
+00006850: 2e39 3231 3338 3120 4320 3237 2e34 3031  .921381 C 27.401
+00006860: 3739 382c 3132 2e39 3231 3338 3120 3238  798,12.921381 28
+00006870: 2e38 3838 3731 382c 3133 2e35 3435 3535  .888718,13.54555
+00006880: 3120 3330 2e31 3338 3233 2c31 342e 3738  1 30.13823,14.78
+00006890: 3134 3037 2043 2033 312e 3337 3532 3436  1407 C 31.375246
+000068a0: 2c31 362e 3032 3937 3437 2033 322e 3030  ,16.029747 32.00
+000068b0: 3030 3032 2c31 372e 3531 3532 3732 2033  0002,17.515272 3
+000068c0: 322e 3030 3030 3032 2c31 392e 3237 3534  2.000002,19.2754
+000068d0: 3331 2043 2033 322e 3030 3030 3032 2c32  31 C 32.000002,2
+000068e0: 322e 3035 3932 3320 3330 2e33 3030 3636  2.05923 30.30066
+000068f0: 362c 3234 2e33 3831 3134 3220 3236 2e38  6,24.381142 26.8
+00006900: 3839 3439 382c 3236 2e32 3238 3638 3520  89498,26.228685 
+00006910: 4320 3233 2e34 3738 3333 312c 3238 2e30  C 23.478331,28.0
+00006920: 3736 3232 3820 3139 2e32 3035 2c32 3920  76228 19.205,29 
+00006930: 3134 2e30 3639 3530 352c 3239 2043 2039  14.069505,29 C 9
+00006940: 2e36 3231 3234 3239 2c32 3920 342e 3933  .6212429,29 4.93
+00006950: 3535 3732 392c 3237 2e38 3838 3937 3720  55729,27.888977 
+00006960: 302c 3235 2e36 3239 3438 3220 7a20 4d20  0,25.629482 z M 
+00006970: 3230 2e39 3136 3833 312c 3139 2e33 3132  20.916831,19.312
+00006980: 3838 3220 4320 3230 2e39 3136 3833 312c  882 C 20.916831,
+00006990: 3230 2e35 3836 3138 3820 3231 2e33 3739  20.586188 21.379
+000069a0: 3135 2c32 312e 3638 3437 3238 2032 322e  15,21.684728 22.
+000069b0: 3331 3632 3834 2c32 322e 3630 3834 3939  316284,22.608499
+000069c0: 2043 2032 332e 3234 3039 3233 2c32 332e   C 23.240923,23.
+000069d0: 3533 3232 3731 2032 342e 3336 3534 3834  532271 24.365484
+000069e0: 2c32 332e 3939 3431 3537 2032 352e 3635  ,23.994157 25.65
+000069f0: 3234 3831 2c32 332e 3939 3431 3537 2043  2481,23.994157 C
+00006a00: 2032 362e 3935 3139 3734 2c32 332e 3939   26.951974,23.99
+00006a10: 3431 3537 2032 382e 3035 3135 3435 2c32  4157 28.051545,2
+00006a20: 332e 3533 3232 3731 2032 382e 3936 3336  3.532271 28.9636
+00006a30: 3838 2c32 322e 3634 3539 3439 2043 2032  88,22.645949 C 2
+00006a40: 392e 3836 3333 3337 2c32 312e 3734 3731  9.863337,21.7471
+00006a50: 3435 2033 302e 3331 3331 3631 2c32 302e  45 30.313161,20.
+00006a60: 3634 3836 3035 2033 302e 3331 3331 3631  648605 30.313161
+00006a70: 2c31 392e 3335 3033 3332 2043 2033 302e  ,19.350332 C 30.
+00006a80: 3331 3331 3631 2c31 382e 3032 3730 3931  313161,18.027091
+00006a90: 2032 392e 3836 3333 3337 2c31 362e 3930   29.863337,16.90
+00006aa0: 3335 3835 2032 382e 3935 3131 3933 2c31  3585 28.951193,1
+00006ab0: 352e 3937 3938 3134 2043 2032 382e 3033  5.979814 C 28.03
+00006ac0: 3930 3439 2c31 352e 3035 3630 3432 2032  9049,15.056042 2
+00006ad0: 362e 3933 3934 3739 2c31 342e 3539 3431  6.939479,14.5941
+00006ae0: 3536 2032 352e 3633 3939 3836 2c31 342e  56 25.639986,14.
+00006af0: 3539 3431 3536 2043 2032 342e 3332 3739  594156 C 24.3279
+00006b00: 3939 2c31 342e 3539 3431 3536 2032 332e  99,14.594156 23.
+00006b10: 3231 3539 3333 2c31 352e 3035 3630 3432  215933,15.056042
+00006b20: 2032 322e 3239 3132 3934 2c31 352e 3937   22.291294,15.97
+00006b30: 3938 3134 2043 2032 312e 3337 3931 352c  9814 C 21.37915,
+00006b40: 3136 2e38 3931 3130 3220 3230 2e39 3136  16.891102 20.916
+00006b50: 3833 312c 3138 2e30 3032 3132 3520 3230  831,18.002125 20
+00006b60: 2e39 3136 3833 312c 3139 2e33 3132 3838  .916831,19.31288
+00006b70: 3220 7a20 4d20 3332 2e30 3030 3030 322c  2 z M 32.000002,
+00006b80: 372e 3331 3633 3334 3120 4c20 3332 2e30  7.3163341 L 32.0
+00006b90: 3030 3030 322c 3130 2e30 3337 3731 3520  00002,10.037715 
+00006ba0: 4320 3236 2e37 3339 3535 372c 372e 3634  C 26.739557,7.64
+00006bb0: 3039 3032 3520 3231 2e36 3636 3533 382c  09025 21.666538,
+00006bc0: 362e 3434 3234 3936 3220 3136 2e37 3535  6.4424962 16.755
+00006bd0: 3935 362c 362e 3434 3234 3936 3220 4320  956,6.4424962 C 
+00006be0: 3133 2e35 3537 3230 352c 362e 3434 3234  13.557205,6.4424
+00006bf0: 3936 3220 3130 2e39 3333 3233 2c36 2e38  962 10.93323,6.8
+00006c00: 3534 3434 3833 2038 2e39 3039 3032 3039  544483 8.9090209
+00006c10: 2c37 2e37 3033 3331 3935 2043 2031 302e  ,7.7033195 C 10.
+00006c20: 3230 3835 3133 2c38 2e33 3532 3435 3633  208513,8.3524563
+00006c30: 2031 312e 3137 3036 3337 2c39 2e31 3736   11.170637,9.176
+00006c40: 3336 3037 2031 312e 3739 3533 3933 2c31  3607 11.795393,1
+00006c50: 302e 3136 3235 3439 2043 2031 322e 3434  0.162549 C 12.44
+00006c60: 3531 342c 3131 2e31 3438 3733 3820 3132  514,11.148738 12
+00006c70: 2e37 3537 3531 382c 3132 2e33 3039 3639  .757518,12.30969
+00006c80: 3420 3132 2e37 3537 3531 382c 3133 2e36  4 12.757518,13.6
+00006c90: 3435 3431 3820 4320 3132 2e37 3537 3531  45418 C 12.75751
+00006ca0: 382c 3135 2e33 3933 3039 3420 3132 2e31  8,15.393094 12.1
+00006cb0: 3332 3736 322c 3136 2e38 3931 3130 3220  32762,16.891102 
+00006cc0: 3130 2e38 3730 3735 352c 3138 2e31 3531  10.870755,18.151
+00006cd0: 3932 3520 4320 392e 3630 3837 3436 392c  925 C 9.6087469,
+00006ce0: 3139 2e34 3030 3236 3520 382e 3039 3638  19.400265 8.0968
+00006cf0: 3337 392c 3230 2e30 3234 3433 3520 362e  379,20.024435 6.
+00006d00: 3333 3530 3235 392c 3230 2e30 3234 3433  3350259,20.02443
+00006d10: 3520 4320 342e 3538 3537 3038 392c 3230  5 C 4.5857089,20
+00006d20: 2e30 3234 3433 3520 332e 3039 3837 3839  .024435 3.098789
+00006d30: 392c 3139 2e34 3132 3734 3920 312e 3836  9,19.412749 1.86
+00006d40: 3137 3732 392c 3138 2e31 3634 3430 3920  17729,18.164409 
+00006d50: 4320 302e 3632 3437 3536 2c31 362e 3932  C 0.624756,16.92
+00006d60: 3835 3532 2030 2c31 352e 3433 3035 3434  8552 0,15.430544
+00006d70: 2030 2c31 332e 3638 3238 3638 2043 2030   0,13.682868 C 0
+00006d80: 2c31 302e 3838 3635 3836 2031 2e36 3939  ,10.886586 1.699
+00006d90: 3333 3634 2c38 2e35 3532 3139 3037 2035  3364,8.5521907 5
+00006da0: 2e31 3130 3530 3339 2c36 2e37 3034 3634  .1105039,6.70464
+00006db0: 3735 2043 2038 2e35 3039 3137 3639 2c34  75 C 8.5091769,4
+00006dc0: 2e38 3537 3130 3434 2031 322e 3739 3530  .8571044 12.7950
+00006dd0: 3033 2c33 2e39 3333 3333 3237 2031 372e  03,3.9333327 17.
+00006de0: 3933 3034 3937 2c33 2e39 3333 3333 3237  930497,3.9333327
+00006df0: 2043 2032 322e 3337 3837 362c 332e 3933   C 22.37876,3.93
+00006e00: 3333 3332 3720 3237 2e30 3634 3433 2c35  33327 27.06443,5
+00006e10: 2e30 3536 3833 3838 2033 322e 3030 3030  .0568388 32.0000
+00006e20: 3032 2c37 2e33 3136 3333 3431 207a 204d  02,7.3163341 z M
+00006e30: 2031 312e 3038 3331 3732 2c31 332e 3633   11.083172,13.63
+00006e40: 3239 3335 2043 2031 312e 3038 3331 3732  2935 C 11.083172
+00006e50: 2c31 322e 3334 3731 3434 2031 302e 3632  ,12.347144 10.62
+00006e60: 3038 3532 2c31 312e 3234 3836 3035 2039  0852,11.248605 9
+00006e70: 2e36 3833 3731 3739 2c31 302e 3332 3438  .6837179,10.3248
+00006e80: 3334 2043 2038 2e37 3436 3538 3339 2c39  34 C 8.7465839,9
+00006e90: 2e34 3133 3534 3533 2037 2e36 3232 3032  .4135453 7.62202
+00006ea0: 3239 2c38 2e39 3531 3635 3935 2036 2e33  29,8.9516595 6.3
+00006eb0: 3232 3533 3039 2c38 2e39 3531 3635 3935  225309,8.9516595
+00006ec0: 2043 2035 2e30 3233 3033 3739 2c38 2e39   C 5.0230379,8.9
+00006ed0: 3531 3635 3935 2033 2e39 3233 3436 3739  516595 3.9234679
+00006ee0: 2c39 2e34 3031 3036 3139 2033 2e30 3233  ,9.4010619 3.023
+00006ef0: 3831 3839 2c31 302e 3239 3938 3637 2043  8189,10.299867 C
+00006f00: 2032 2e31 3234 3137 3039 2c31 312e 3139   2.1241709,11.19
+00006f10: 3836 3732 2031 2e36 3734 3334 3631 2c31  8672 1.6743461,1
+00006f20: 322e 3239 3732 3131 2031 2e36 3734 3334  2.297211 1.67434
+00006f30: 3631 2c31 332e 3539 3534 3834 2043 2031  61,13.595484 C 1
+00006f40: 2e36 3734 3334 3631 2c31 342e 3931 3837  .6743461,14.9187
+00006f50: 3235 2032 2e31 3336 3636 3539 2c31 362e  25 2.1366659,16.
+00006f60: 3034 3232 3331 2033 2e30 3438 3830 3839  042231 3.0488089
+00006f70: 2c31 362e 3936 3630 3032 2043 2033 2e39  ,16.966002 C 3.9
+00006f80: 3438 3435 3739 2c31 372e 3838 3937 3734  484579,17.889774
+00006f90: 2035 2e30 3630 3532 3339 2c31 382e 3335   5.0605239,18.35
+00006fa0: 3136 3620 362e 3336 3030 3135 392c 3138  166 6.3600159,18
+00006fb0: 2e33 3531 3636 2043 2037 2e36 3539 3530  .35166 C 7.65950
+00006fc0: 3839 2c31 382e 3335 3136 3620 382e 3738  89,18.35166 8.78
+00006fd0: 3430 3638 392c 3137 2e38 3839 3737 3420  40689,17.889774 
+00006fe0: 392e 3639 3632 3132 392c 3136 2e39 3636  9.6962129,16.966
+00006ff0: 3030 3220 4320 3130 2e36 3230 3835 322c  002 C 10.620852,
+00007000: 3136 2e30 3432 3233 3120 3131 2e30 3833  16.042231 11.083
+00007010: 3137 322c 3134 2e39 3331 3230 3820 3131  172,14.931208 11
+00007020: 2e30 3833 3137 322c 3133 2e36 3332 3933  .083172,13.63293
+00007030: 3520 7a20 220a 2020 2020 2020 2020 2020  5 z ".          
+00007040: 2020 2020 2020 2020 2020 2020 2020 7374                st
+00007050: 796c 653d 2266 696c 6c3a 2024 7a6f 6469  yle="fill: $zodi
+00007060: 6163 5f63 6f6c 6f72 5f33 220a 2020 2020  ac_color_3".    
+00007070: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00007080: 2f3e 0a20 2020 2020 2020 2020 2020 2020  />.             
+00007090: 2020 203c 2f73 796d 626f 6c3e 0a20 2020     </symbol>.   
+000070a0: 2020 2020 2020 2020 2020 2020 203c 7379               <sy
+000070b0: 6d62 6f6c 2069 643d 226c 656f 223e 0a20  mbol id="leo">. 
+000070c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000070d0: 2020 203c 7061 7468 0a20 2020 2020 2020     <path.       
+000070e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000070f0: 2064 3d22 4d20 3238 2e30 3231 3337 312c   d="M 28.021371,
+00007100: 3239 2e34 3830 3832 3120 4320 3237 2e33  29.480821 C 27.3
+00007110: 3738 3333 392c 3330 2e30 3639 3934 3820  78339,30.069948 
+00007120: 3236 2e36 3837 3939 322c 3330 2e36 3132  26.687992,30.612
+00007130: 3339 3220 3235 2e39 3333 3630 322c 3331  392 25.933602,31
+00007140: 2e30 3532 3335 3920 4320 3235 2e33 3034  .052359 C 25.304
+00007150: 3339 342c 3331 2e34 3138 3730 3120 3234  394,31.418701 24
+00007160: 2e36 3237 3432 392c 3331 2e37 3132 3039  .627429,31.71209
+00007170: 3120 3233 2e39 3135 3032 322c 3331 2e38  1 23.915022,31.8
+00007180: 3730 3437 3220 4320 3233 2e34 3837 3830  70472 C 23.48780
+00007190: 372c 3331 2e39 3636 2032 332e 3034 3839  7,31.966 23.0489
+000071a0: 3737 2c33 322e 3031 3032 3632 2032 322e  77,32.010262 22.
+000071b0: 3631 3132 3739 2c33 312e 3939 3739 3938  611279,31.997998
+000071c0: 2043 2032 312e 3939 3630 3835 2c33 312e   C 21.996085,31.
+000071d0: 3938 3431 3537 2032 312e 3338 3033 3435  984157 21.380345
+000071e0: 2c33 312e 3837 3734 3534 2032 302e 3830  ,31.877454 20.80
+000071f0: 3439 3131 2c33 312e 3635 3634 3236 2043  4911,31.656426 C
+00007200: 2032 302e 3237 3334 3539 2c33 312e 3435   20.273459,31.45
+00007210: 3337 3920 3139 2e37 3830 3432 2c33 312e  379 19.78042,31.
+00007220: 3135 3339 3033 2031 392e 3335 3034 3535  153903 19.350455
+00007230: 2c33 302e 3738 3230 3238 2043 2031 392e  ,30.782028 C 19.
+00007240: 3031 3539 342c 3330 2e34 3933 3736 3920  01594,30.493769 
+00007250: 3138 2e37 3138 3030 322c 3330 2e31 3632  18.718002,30.162
+00007260: 3735 3720 3138 2e34 3637 3736 322c 3239  757 18.467762,29
+00007270: 2e37 3938 3834 3620 4320 3138 2e31 3538  .798846 C 18.158
+00007280: 3738 312c 3239 2e33 3439 3633 3320 3137  781,29.349633 17
+00007290: 2e39 3239 3738 322c 3238 2e38 3435 3733  .929782,28.84573
+000072a0: 3920 3137 2e37 3934 3732 352c 3238 2e33  9 17.794725,28.3
+000072b0: 3137 3437 3920 4320 3137 2e36 3335 3934  17479 C 17.63594
+000072c0: 2c32 372e 3730 3038 3731 2031 372e 3630  ,27.700871 17.60
+000072d0: 3133 3535 2c32 372e 3035 3632 3337 2031  1355,27.056237 1
+000072e0: 372e 3635 3838 3936 2c32 362e 3432 3334  7.658896,26.4234
+000072f0: 3032 2043 2031 372e 3731 3634 3835 2c32  02 C 17.716485,2
+00007300: 352e 3738 3338 3732 2031 372e 3834 3830  5.783872 17.8480
+00007310: 3133 2c32 352e 3135 3333 3036 2031 382e  13,25.153306 18.
+00007320: 3030 3834 3439 2c32 342e 3533 3233 3534  008449,24.532354
+00007330: 2043 2031 382e 3235 3639 3035 2c32 332e   C 18.256905,23.
+00007340: 3538 3036 3131 2031 382e 3537 3738 3733  580611 18.577873
+00007350: 2c32 322e 3634 3933 3520 3138 2e39 3238  ,22.64935 18.928
+00007360: 3439 312c 3231 2e37 3330 3837 3320 4320  491,21.730873 C 
+00007370: 3139 2e34 3434 3935 382c 3230 2e33 3833  19.444958,20.383
+00007380: 3731 3620 3230 2e30 3330 3137 342c 3139  716 20.030174,19
+00007390: 2e30 3633 3938 3820 3230 2e36 3434 3937  .063988 20.64497
+000073a0: 312c 3137 2e37 3539 3134 3420 4320 3231  1,17.759144 C 21
+000073b0: 2e31 3337 3230 352c 3136 2e37 3130 3130  .137205,16.71010
+000073c0: 3120 3231 2e36 3239 3433 372c 3135 2e36  1 21.629437,15.6
+000073d0: 3631 3036 2032 322e 3132 3136 3639 2c31  6106 22.121669,1
+000073e0: 342e 3631 3230 3137 2043 2032 322e 3536  4.612017 C 22.56
+000073f0: 3332 3237 2c31 332e 3636 3532 3038 2032  3227,13.665208 2
+00007400: 322e 3936 3537 3433 2c31 322e 3639 3834  2.965743,12.6984
+00007410: 3520 3233 2e32 3836 3035 322c 3131 2e37  5 23.286052,11.7
+00007420: 3033 3433 3220 4320 3233 2e35 3134 3039  03432 C 23.51409
+00007430: 392c 3130 2e39 3930 3731 2032 332e 3730  9,10.99071 23.70
+00007440: 3132 3535 2c31 302e 3236 3235 3034 2032  1255,10.262504 2
+00007450: 332e 3830 3131 3831 2c39 2e35 3230 3032  3.801181,9.52002
+00007460: 3836 2043 2032 332e 3835 3231 3936 2c39  86 C 23.852196,9
+00007470: 2e31 3430 3537 3436 2032 332e 3837 3735  .1405746 23.8775
+00007480: 3837 2c38 2e37 3537 3339 3136 2032 332e  87,8.7573916 23.
+00007490: 3836 3933 3131 2c38 2e33 3734 3437 3636  869311,8.3744766
+000074a0: 2043 2032 332e 3835 3638 3939 2c37 2e35   C 23.856899,7.5
+000074b0: 3836 3933 3134 2032 332e 3735 3035 3439  869314 23.750549
+000074c0: 2c36 2e37 3936 3536 3138 2032 332e 3530  ,6.7965618 23.50
+000074d0: 3533 3031 2c36 2e30 3436 3336 3335 2043  5301,6.0463635 C
+000074e0: 2032 332e 3330 3130 3538 2c35 2e34 3138   23.301058,5.418
+000074f0: 3630 3520 3232 2e39 3936 3535 392c 342e  605 22.996559,4.
+00007500: 3832 3234 3637 3420 3232 2e35 3937 3430  8224674 22.59740
+00007510: 312c 342e 3239 3631 3432 3120 4320 3232  1,4.2961421 C 22
+00007520: 2e33 3731 3130 372c 332e 3939 3731 3838  .371107,3.997188
+00007530: 3120 3232 2e31 3135 3838 2c33 2e37 3230  1 22.11588,3.720
+00007540: 3335 3332 2032 312e 3833 3931 3332 2c33  3532 21.839132,3
+00007550: 2e34 3637 3533 3333 2043 2032 312e 3337  .4675333 C 21.37
+00007560: 3933 382c 332e 3034 3837 3533 3220 3230  938,3.0487532 20
+00007570: 2e38 3438 3631 2c32 2e37 3038 3234 3234  .84861,2.7082424
+00007580: 2032 302e 3237 3538 3236 2c32 2e34 3636   20.275826,2.466
+00007590: 3031 3734 2043 2031 392e 3632 3332 3031  0174 C 19.623201
+000075a0: 2c32 2e31 3838 3432 3920 3138 2e39 3231  ,2.188429 18.921
+000075b0: 3335 312c 322e 3033 3733 3937 2031 382e  351,2.037397 18.
+000075c0: 3231 3535 382c 312e 3938 3334 3937 3320  21558,1.9834973 
+000075d0: 4320 3137 2e37 3038 3935 322c 312e 3934  C 17.708952,1.94
+000075e0: 3535 3838 3220 3137 2e31 3938 3639 312c  55882 17.198691,
+000075f0: 312e 3935 3034 3538 3220 3136 2e36 3933  1.9504582 16.693
+00007600: 3338 342c 322e 3030 3433 3035 3420 4320  384,2.0043054 C 
+00007610: 3136 2e30 3138 3434 352c 322e 3037 3635  16.018445,2.0765
+00007620: 3630 3820 3135 2e33 3530 3832 382c 322e  608 15.350828,2.
+00007630: 3234 3437 3736 3620 3134 2e37 3334 3137  2447766 14.73417
+00007640: 312c 322e 3533 3133 3038 3320 4320 3134  1,2.5313083 C 14
+00007650: 2e31 3737 3130 352c 322e 3738 3838 3537  .177105,2.788857
+00007660: 2031 332e 3636 3530 3433 2c33 2e31 3432   13.665043,3.142
+00007670: 3339 3735 2031 332e 3232 3433 3138 2c33  3975 13.224318,3
+00007680: 2e35 3639 3334 3739 2043 2031 322e 3739  .5693479 C 12.79
+00007690: 3535 3335 2c33 2e39 3935 3133 3333 2031  5535,3.9951333 1
+000076a0: 322e 3433 3534 3537 2c34 2e34 3931 3234  2.435457,4.49124
+000076b0: 3138 2031 322e 3137 3237 3139 2c35 2e30  18 12.172719,5.0
+000076c0: 3335 3837 3733 2043 2031 312e 3839 3030  358773 C 11.8900
+000076d0: 3934 2c35 2e36 3138 3134 3637 2031 312e  94,5.6181467 11.
+000076e0: 3731 3936 3432 2c36 2e32 3531 3330 3831  719642,6.2513081
+000076f0: 2031 312e 3634 3339 3437 2c36 2e38 3933   11.643947,6.893
+00007700: 3130 3239 2043 2031 312e 3536 3230 3137  1029 C 11.562017
+00007710: 2c37 2e35 3834 3433 3233 2031 312e 3538  ,7.5844323 11.58
+00007720: 3238 322c 382e 3238 3537 3339 3620 3131  282,8.2857396 11
+00007730: 2e36 3830 3533 332c 382e 3937 3433 3033  .680533,8.974303
+00007740: 3620 4320 3131 2e38 3036 3038 312c 392e  6 C 11.806081,9.
+00007750: 3836 3137 3630 3620 3132 2e30 3438 3937  8617606 12.04897
+00007760: 352c 3130 2e37 3239 3135 3220 3132 2e33  5,10.729152 12.3
+00007770: 3534 3033 332c 3131 2e35 3730 3639 3120  54033,11.570691 
+00007780: 4320 3132 2e35 3938 3739 382c 3132 2e32  C 12.598798,12.2
+00007790: 3434 3833 3720 3132 2e38 3835 3439 392c  44837 12.885499,
+000077a0: 3132 2e39 3033 3131 3720 3133 2e31 3938  12.903117 13.198
+000077b0: 3339 382c 3133 2e35 3438 3236 3820 4320  398,13.548268 C 
+000077c0: 3133 2e34 3039 3936 342c 3133 2e39 3837  13.409964,13.987
+000077d0: 3638 3220 3133 2e36 3231 3931 312c 3134  682 13.621911,14
+000077e0: 2e34 3236 3931 3520 3133 2e38 3333 3137  .426915 13.83317
+000077f0: 312c 3134 2e38 3636 3437 3520 4320 3134  1,14.866475 C 14
+00007800: 2e31 3830 3438 382c 3135 2e35 3936 2031  .180488,15.596 1
+00007810: 342e 3530 3738 3633 2c31 362e 3333 3631  4.507863,16.3361
+00007820: 3136 2031 342e 3738 3137 342c 3137 2e30  16 14.78174,17.0
+00007830: 3936 3636 3420 4320 3134 2e39 3534 3633  96664 C 14.95463
+00007840: 392c 3137 2e35 3830 3930 3320 3135 2e31  9,17.580903 15.1
+00007850: 3037 3734 312c 3138 2e30 3733 3839 3820  07741,18.073898 
+00007860: 3135 2e32 3034 3636 342c 3138 2e35 3739  15.204664,18.579
+00007870: 3436 3820 4320 3135 2e32 3630 3631 352c  468 C 15.260615,
+00007880: 3138 2e38 3734 3430 3420 3135 2e32 3935  18.874404 15.295
+00007890: 3930 352c 3139 2e31 3734 3439 3220 3135  905,19.174492 15
+000078a0: 2e32 3838 3530 312c 3139 2e34 3735 3039  .288501,19.47509
+000078b0: 3620 4320 3135 2e32 3739 3533 312c 3230  6 C 15.279531,20
+000078c0: 2e31 3230 3036 3420 3135 2e31 3634 3035  .120064 15.16405
+000078d0: 382c 3230 2e37 3634 3537 3520 3134 2e39  8,20.764575 14.9
+000078e0: 3336 3332 2c32 312e 3336 3835 3633 2043  3632,21.368563 C
+000078f0: 2031 342e 3730 3235 3632 2c32 312e 3939   14.702562,21.99
+00007900: 3239 3338 2031 342e 3335 3133 3936 2c32  2938 14.351396,2
+00007910: 322e 3537 3033 3737 2031 332e 3932 3236  2.570377 13.9226
+00007920: 3134 2c32 332e 3037 3937 3239 2043 2031  14,23.079729 C 1
+00007930: 332e 3539 3631 3638 2c32 332e 3436 3637  3.596168,23.4667
+00007940: 3638 2031 332e 3232 3934 3435 2c32 332e  68 13.229445,23.
+00007950: 3832 3033 3035 2031 322e 3832 3830 312c  820305 12.82801,
+00007960: 3234 2e31 3239 3030 3620 4320 3132 2e33  24.129006 C 12.3
+00007970: 3030 3439 342c 3234 2e35 3334 3635 3320  00494,24.534653 
+00007980: 3131 2e37 3037 3032 312c 3234 2e38 3536  11.707021,24.856
+00007990: 3237 3720 3131 2e30 3734 3335 2c32 352e  277 11.07435,25.
+000079a0: 3036 3430 3431 2043 2031 302e 3432 3830  064041 C 10.4280
+000079b0: 3533 2c32 352e 3237 3739 3039 2039 2e37  53,25.277909 9.7
+000079c0: 3434 3933 3735 2c32 352e 3337 3231 3933  449375,25.372193
+000079d0: 2039 2e30 3635 3033 3939 2c32 352e 3336   9.0650399,25.36
+000079e0: 3337 3637 2043 2038 2e33 3735 3935 3933  3767 C 8.3759593
+000079f0: 2c32 352e 3335 3638 3639 2037 2e36 3835  ,25.356869 7.685
+00007a00: 3530 3138 2c32 352e 3234 3735 3931 2037  5018,25.247591 7
+00007a10: 2e30 3335 3538 3139 2c32 352e 3031 3535  .0355819,25.0155
+00007a20: 3537 2043 2036 2e34 3232 3234 3337 2c32  57 C 6.4222437,2
+00007a30: 342e 3739 3831 3338 2035 2e38 3438 3936  4.798138 5.84896
+00007a40: 3837 2c32 342e 3437 3137 3036 2035 2e33  87,24.471706 5.3
+00007a50: 3432 3931 3138 2c32 342e 3036 3331 3333  429118,24.063133
+00007a60: 2043 2035 2e30 3433 3936 3935 2c32 332e   C 5.0439695,23.
+00007a70: 3832 3233 3238 2034 2e37 3637 3734 3931  822328 4.7677491
+00007a80: 2c32 332e 3535 3338 3938 2034 2e35 3132  ,23.553898 4.512
+00007a90: 3335 3733 2c32 332e 3236 3735 2043 2034  3573,23.2675 C 4
+00007aa0: 2e30 3735 3535 3331 2c32 322e 3737 3536  .0755531,22.7756
+00007ab0: 3438 2033 2e37 3134 3137 3432 2c32 322e  48 3.7141742,22.
+00007ac0: 3231 3439 3434 2033 2e34 3631 3635 3138  214944 3.4616518
+00007ad0: 2c32 312e 3630 3638 3434 2043 2033 2e32  ,21.606844 C 3.2
+00007ae0: 3033 3737 3737 2c32 302e 3938 3939 3520  037777,20.98995 
+00007af0: 332e 3035 3934 3337 382c 3230 2e33 3238  3.0594378,20.328
+00007b00: 3235 3920 332e 3031 3537 3932 382c 3139  259 3.0157928,19
+00007b10: 2e36 3631 3830 3620 4320 322e 3936 3933  .661806 C 2.9693
+00007b20: 3031 382c 3138 2e39 3535 3433 3320 332e  018,18.955433 3.
+00007b30: 3032 3331 3833 382c 3138 2e32 3339 3339  0231838,18.23939
+00007b40: 3720 332e 3230 3737 3130 342c 3137 2e35  7 3.2077104,17.5
+00007b50: 3534 3734 2043 2033 2e33 3732 3732 3235  5474 C 3.3727225
+00007b60: 2c31 362e 3933 3732 3333 2033 2e36 3434  ,16.937233 3.644
+00007b70: 3733 3733 2c31 362e 3334 3931 3934 2034  7373,16.349194 4
+00007b80: 2e30 3034 3133 3939 2c31 352e 3832 3039  .0041399,15.8209
+00007b90: 3031 2043 2034 2e33 3032 3734 332c 3135  01 C 4.302743,15
+00007ba0: 2e33 3739 3930 3620 342e 3636 3037 3230  .379906 4.660720
+00007bb0: 382c 3134 2e39 3831 3038 3420 352e 3035  8,14.981084 5.05
+00007bc0: 3236 3132 362c 3134 2e36 3231 3237 3320  26126,14.621273 
+00007bd0: 4320 352e 3534 3231 3339 392c 3134 2e31  C 5.5421399,14.1
+00007be0: 3733 3436 3720 362e 3130 3133 3632 392c  73467 6.1013629,
+00007bf0: 3133 2e37 3938 3733 3420 362e 3731 3231  13.798734 6.7121
+00007c00: 3934 332c 3133 2e35 3337 3637 3320 4320  943,13.537673 C 
+00007c10: 372e 3330 3230 3838 372c 3133 2e32 3833  7.3020887,13.283
+00007c20: 3931 2037 2e39 3336 3832 3231 2c31 332e  91 7.9368221,13.
+00007c30: 3133 3837 3631 2038 2e35 3737 3136 3235  138761 8.5771625
+00007c40: 2c31 332e 3039 3737 3439 2043 2038 2e38  ,13.097749 C 8.8
+00007c50: 3937 3135 3834 2c31 332e 3037 3637 3137  971584,13.076717
+00007c60: 2039 2e32 3138 3938 3337 2c31 332e 3037   9.2189837,13.07
+00007c70: 3934 3733 2039 2e35 3338 3039 3233 2c31  9473 9.5380923,1
+00007c80: 332e 3131 3233 3736 2043 2031 302e 3031  3.112376 C 10.01
+00007c90: 3833 3235 2c31 332e 3136 3038 3634 2031  8325,13.160864 1
+00007ca0: 302e 3439 3134 3135 2c31 332e 3236 3735  0.491415,13.2675
+00007cb0: 3220 3130 2e39 3531 3837 372c 3133 2e34  2 10.951877,13.4
+00007cc0: 3130 3835 3120 4320 3130 2e34 3736 3637  10851 C 10.47667
+00007cd0: 382c 3132 2e34 3933 3236 3220 3130 2e30  8,12.493262 10.0
+00007ce0: 3536 3935 312c 3131 2e35 3434 3035 3520  56951,11.544055 
+00007cf0: 392e 3734 3538 3136 362c 3130 2e35 3537  9.7458166,10.557
+00007d00: 3635 3820 4320 392e 3439 3136 3432 2c39  658 C 9.491642,9
+00007d10: 2e37 3438 3832 3836 2039 2e33 3130 3936  .7488286 9.31096
+00007d20: 3139 2c38 2e39 3132 3835 3436 2039 2e32  19,8.9128546 9.2
+00007d30: 3632 3234 3136 2c38 2e30 3634 3937 3236  622416,8.0649726
+00007d40: 2043 2039 2e32 3336 3330 352c 372e 3630   C 9.236305,7.60
+00007d50: 3331 3330 3820 392e 3235 3036 3137 2c37  31308 9.250617,7
+00007d60: 2e31 3339 3132 3937 2039 2e33 3031 3236  .1391297 9.30126
+00007d70: 3539 2c36 2e36 3739 3431 3037 2043 2039  59,6.6794107 C 9
+00007d80: 2e33 3836 3235 3037 2c35 2e39 3133 3236  .3862507,5.91326
+00007d90: 3835 2039 2e35 3836 3838 3032 2c35 2e31  85 9.5868802,5.1
+00007da0: 3538 3230 3338 2039 2e39 3132 3735 3337  582038 9.9127537
+00007db0: 2c34 2e34 3538 3834 3837 2043 2031 302e  ,4.4588487 C 10.
+00007dc0: 3233 3335 3437 2c33 2e37 3636 3438 3936  233547,3.7664896
+00007dd0: 2031 302e 3637 3531 3731 2c33 2e31 3332   10.675171,3.132
+00007de0: 3532 2031 312e 3139 3937 3438 2c32 2e35  52 11.199748,2.5
+00007df0: 3739 3331 3838 2043 2031 312e 3835 3135  793188 C 11.8515
+00007e00: 3031 2c31 2e38 3932 3730 3738 2031 322e  01,1.8927078 12.
+00007e10: 3631 3936 3034 2c31 2e33 3134 3437 3436  619604,1.3144746
+00007e20: 2031 332e 3436 3739 3735 2c30 2e38 3933   13.467975,0.893
+00007e30: 3033 3637 3220 4320 3134 2e32 3337 3534  03672 C 14.23754
+00007e40: 362c 302e 3530 3931 3037 3832 2031 352e  6,0.50910782 15.
+00007e50: 3036 3935 3637 2c30 2e32 3536 3137 3134  069567,0.2561714
+00007e60: 3220 3135 2e39 3138 3339 312c 302e 3132  2 15.918391,0.12
+00007e70: 3330 3836 3932 2043 2031 362e 3734 3434  308692 C 16.7444
+00007e80: 3539 2c2d 302e 3030 3732 3337 3238 3338  59,-0.0072372838
+00007e90: 2031 372e 3538 3534 3532 2c2d 302e 3032   17.585452,-0.02
+00007ea0: 3639 3837 3738 3420 3138 2e34 3138 3937  6987784 18.41897
+00007eb0: 372c 302e 3032 3933 3836 3631 3620 4320  7,0.029386616 C 
+00007ec0: 3139 2e33 3639 3239 352c 302e 3039 3533  19.369295,0.0953
+00007ed0: 3637 3931 3620 3230 2e33 3135 3438 342c  67916 20.315484,
+00007ee0: 302e 3237 3935 3837 3132 2032 312e 3230  0.27958712 21.20
+00007ef0: 3633 3538 2c30 2e36 3231 3337 3631 3220  6358,0.62137612 
+00007f00: 4320 3231 2e39 3731 3237 392c 302e 3931  C 21.971279,0.91
+00007f10: 3335 3739 3032 2032 322e 3639 3136 3433  357902 22.691643
+00007f20: 2c31 2e33 3233 3830 3735 2032 332e 3332  ,1.3238075 23.32
+00007f30: 3834 3331 2c31 2e38 3339 3038 3536 2043  8431,1.8390856 C
+00007f40: 2032 332e 3632 3130 3632 2c32 2e30 3735   23.621062,2.075
+00007f50: 3336 3637 2032 332e 3839 3732 3931 2c32  3667 23.897291,2
+00007f60: 2e33 3332 3231 3638 2032 342e 3135 3035  .3322168 24.1505
+00007f70: 3133 2c32 2e36 3130 3435 3132 2043 2032  13,2.6104512 C 2
+00007f80: 342e 3638 3533 3536 2c33 2e31 3933 3336  4.685356,3.19336
+00007f90: 3534 2032 352e 3132 3734 3837 2c33 2e38  54 25.127487,3.8
+00007fa0: 3631 3236 3734 2032 352e 3435 3331 3936  612674 25.453196
+00007fb0: 2c34 2e35 3832 3334 3520 4320 3235 2e38  ,4.582345 C 25.8
+00007fc0: 3137 3834 312c 352e 3338 3537 3830 3520  17841,5.3857805 
+00007fd0: 3236 2e30 3338 3334 372c 362e 3235 3033  26.038347,6.2503
+00007fe0: 3236 3220 3236 2e31 3430 3731 392c 372e  262 26.140719,7.
+00007ff0: 3132 3534 3238 3220 4320 3236 2e32 3031  1254282 C 26.201
+00008000: 3435 382c 372e 3633 3732 3137 3120 3236  458,7.6372171 26
+00008010: 2e32 3230 3834 392c 382e 3135 3332 3237  .220849,8.153227
+00008020: 3620 3236 2e32 3132 3435 2c38 2e36 3638  6 26.21245,8.668
+00008030: 3334 3136 2043 2032 362e 3230 3137 3235  3416 C 26.201725
+00008040: 2c39 2e34 3036 3936 3936 2032 362e 3134  ,9.4069696 26.14
+00008050: 3730 3233 2c31 302e 3134 3638 3631 2032  7023,10.146861 2
+00008060: 362e 3031 3130 3531 2c31 302e 3837 3336  6.011051,10.8736
+00008070: 3531 2043 2032 352e 3935 3738 3839 2c31  51 C 25.957889,1
+00008080: 312e 3135 3831 3432 2032 352e 3839 3035  1.158142 25.8905
+00008090: 3432 2c31 312e 3433 3939 3732 2032 352e  42,11.439972 25.
+000080a0: 3830 3835 3536 2c31 312e 3731 3735 3338  808556,11.717538
+000080b0: 2043 2032 352e 3638 3831 3836 2c31 322e   C 25.688186,12.
+000080c0: 3133 3739 3137 2032 352e 3533 3639 3638  137917 25.536968
+000080d0: 2c31 322e 3534 3836 3938 2032 352e 3337  ,12.548698 25.37
+000080e0: 3932 3132 2c31 322e 3935 3632 3631 2043  9212,12.956261 C
+000080f0: 2032 352e 3037 3739 3633 2c31 332e 3732   25.077963,13.72
+00008100: 3738 3437 2032 342e 3734 3537 3635 2c31  7847 24.745765,1
+00008110: 342e 3438 3639 3038 2032 342e 3430 3539  4.486908 24.4059
+00008120: 3038 2c31 352e 3234 3231 3331 2043 2032  08,15.242131 C 2
+00008130: 342e 3234 3836 312c 3135 2e35 3931 3837  4.24861,15.59187
+00008140: 3320 3234 2e30 3837 3630 382c 3135 2e39  3 24.087608,15.9
+00008150: 3339 3932 3620 3233 2e39 3236 3935 392c  39926 23.926959,
+00008160: 3136 2e32 3838 3133 3420 4320 3233 2e35  16.288134 C 23.5
+00008170: 3733 3933 322c 3137 2e30 3538 3837 3420  73932,17.058874 
+00008180: 3233 2e32 3230 3930 342c 3137 2e38 3239  23.220904,17.829
+00008190: 3631 3520 3232 2e38 3637 3837 362c 3138  615 22.867876,18
+000081a0: 2e36 3030 3335 3520 4320 3232 2e32 3738  .600355 C 22.278
+000081b0: 3831 322c 3139 2e38 3830 3035 3920 3231  812,19.880059 21
+000081c0: 2e37 3036 3234 352c 3231 2e31 3637 3920  .706245,21.1679 
+000081d0: 3231 2e31 3832 3037 2c32 322e 3437 3537  21.18207,22.4757
+000081e0: 3331 2043 2032 302e 3837 3536 3933 2c32  31 C 20.875693,2
+000081f0: 332e 3234 3432 3532 2032 302e 3538 3337  3.244252 20.5837
+00008200: 3936 2c32 342e 3031 3933 3936 2032 302e  96,24.019396 20.
+00008210: 3333 3936 3439 2c32 342e 3831 3032 3037  339649,24.810207
+00008220: 2043 2032 302e 3230 3533 3631 2c32 352e   C 20.205361,25.
+00008230: 3235 3036 3237 2032 302e 3038 3333 3839  250627 20.083389
+00008240: 2c32 352e 3639 3631 3336 2032 302e 3030  ,25.696136 20.00
+00008250: 3738 3635 2c32 362e 3135 3038 3234 2043  7865,26.150824 C
+00008260: 2031 392e 3937 3031 3836 2c32 362e 3338   19.970186,26.38
+00008270: 3034 3433 2031 392e 3934 3635 3235 2c32  0443 19.946525,2
+00008280: 362e 3631 3332 3232 2031 392e 3935 3432  6.613222 19.9542
+00008290: 3331 2c32 362e 3834 3631 3435 2043 2031  31,26.846145 C 1
+000082a0: 392e 3936 3338 3737 2c32 372e 3237 3530  9.963877,27.2750
+000082b0: 3236 2032 302e 3033 3738 3137 2c32 372e  26 20.037817,27.
+000082c0: 3730 3537 3620 3230 2e32 3032 3532 332c  70576 20.202523,
+000082d0: 3238 2e31 3033 3236 3320 4320 3230 2e33  28.103263 C 20.3
+000082e0: 3335 3538 342c 3238 2e34 3236 3830 3620  35584,28.426806 
+000082f0: 3230 2e35 3239 3231 372c 3238 2e37 3234  20.529217,28.724
+00008300: 3933 2032 302e 3736 3931 3638 2c32 382e  93 20.769168,28.
+00008310: 3937 3933 3633 2043 2032 312e 3030 3731  979363 C 21.0071
+00008320: 3331 2c32 392e 3234 3433 3438 2032 312e  31,29.244348 21.
+00008330: 3239 3634 3839 2c32 392e 3436 3435 3639  296489,29.464569
+00008340: 2032 312e 3632 3035 3738 2c32 392e 3631   21.620578,29.61
+00008350: 3333 3834 2043 2032 312e 3936 3636 3139  3384 C 21.966619
+00008360: 2c32 392e 3737 3338 3133 2032 322e 3334  ,29.773813 22.34
+00008370: 3732 342c 3239 2e38 3531 3733 3420 3232  724,29.851734 22
+00008380: 2e37 3237 3433 2c32 392e 3836 3337 3338  .72743,29.863738
+00008390: 2043 2032 332e 3039 3130 3236 2c32 392e   C 23.091026,29.
+000083a0: 3837 3736 3535 2032 332e 3435 3530 362c  877655 23.45506,
+000083b0: 3239 2e38 3232 3530 3320 3233 2e38 3033  29.822503 23.803
+000083c0: 3537 372c 3239 2e37 3230 3334 3320 4320  577,29.720343 C 
+000083d0: 3234 2e33 3130 3533 332c 3239 2e35 3731  24.310533,29.571
+000083e0: 3737 2032 342e 3738 3633 3033 2c32 392e  77 24.786303,29.
+000083f0: 3333 3137 3331 2032 352e 3233 3238 3437  331731 25.232847
+00008400: 2c32 392e 3035 3230 3434 2043 2032 352e  ,29.052044 C 25.
+00008410: 3733 3436 3438 2c32 382e 3733 3635 3337  734648,28.736537
+00008420: 2032 362e 3230 3138 3637 2c32 382e 3336   26.201867,28.36
+00008430: 3837 3739 2032 362e 3634 3535 3531 2c32  8779 26.645551,2
+00008440: 372e 3937 3634 3438 2043 2032 372e 3130  7.976448 C 27.10
+00008450: 3431 3538 2c32 382e 3437 3739 3036 2032  4158,28.477906 2
+00008460: 372e 3536 3237 3635 2c32 382e 3937 3933  7.562765,28.9793
+00008470: 3633 2032 382e 3032 3133 3731 2c32 392e  63 28.021371,29.
+00008480: 3438 3038 3231 207a 204d 2034 2e37 3439  480821 z M 4.749
+00008490: 3032 3735 2c31 392e 3230 3637 3639 2043  0275,19.206769 C
+000084a0: 2034 2e37 3438 3431 3432 2c31 392e 3735   4.7484142,19.75
+000084b0: 3530 3532 2034 2e38 3333 3635 3434 2c32  5052 4.8336544,2
+000084c0: 302e 3330 3538 3737 2035 2e30 3234 3531  0.305877 5.02451
+000084d0: 3231 2c32 302e 3832 3039 3120 4320 352e  21,20.82091 C 5.
+000084e0: 3230 3231 3834 312c 3231 2e33 3034 3332  2021841,21.30432
+000084f0: 3520 352e 3437 3235 3732 342c 3231 2e37  5 5.4725724,21.7
+00008500: 3532 3133 3820 352e 3831 3030 3439 332c  52138 5.8100493,
+00008510: 3232 2e31 3430 3634 3420 4320 362e 3035  22.140644 C 6.05
+00008520: 3436 3830 362c 3232 2e34 3233 3437 3720  46806,22.423477 
+00008530: 362e 3333 3437 3533 322c 3232 2e36 3735  6.3347532,22.675
+00008540: 3738 3720 362e 3634 3138 3238 312c 3232  787 6.6418281,22
+00008550: 2e38 3839 3138 3820 4320 372e 3034 3030  .889188 C 7.0400
+00008560: 3237 372c 3233 2e31 3635 3934 3120 372e  277,23.165941 7.
+00008570: 3438 3837 3033 362c 3233 2e33 3639 3831  4887036,23.36981
+00008580: 3320 372e 3935 3935 3330 312c 3233 2e34  3 7.9595301,23.4
+00008590: 3836 3037 3920 4320 382e 3432 3330 3437  86079 C 8.423047
+000085a0: 342c 3233 2e36 3031 3135 3120 382e 3930  4,23.601151 8.90
+000085b0: 3439 3937 312c 3233 2e36 3335 3438 3720  49971,23.635487 
+000085c0: 392e 3338 3039 3632 2c32 332e 3630 3335  9.380962,23.6035
+000085d0: 3634 2043 2039 2e38 3637 3135 3639 2c32  64 C 9.8671569,2
+000085e0: 332e 3537 3033 3038 2031 302e 3334 3838  3.570308 10.3488
+000085f0: 3132 2c32 332e 3435 3435 3634 2031 302e  12,23.454564 10.
+00008600: 3739 3233 3232 2c32 332e 3235 3133 3520  792322,23.25135 
+00008610: 4320 3131 2e32 3539 3330 392c 3233 2e30  C 11.259309,23.0
+00008620: 3339 3031 3820 3131 2e36 3830 3335 332c  39018 11.680353,
+00008630: 3232 2e37 3332 3930 3120 3132 2e30 3433  22.732901 12.043
+00008640: 3337 362c 3232 2e33 3731 3733 3120 4320  376,22.371731 C 
+00008650: 3132 2e34 3135 3734 382c 3232 2e30 3033  12.415748,22.003
+00008660: 3336 3420 3132 2e37 3239 3536 332c 3231  364 12.729563,21
+00008670: 2e35 3733 3136 3820 3132 2e39 3439 3136  .573168 12.94916
+00008680: 2c32 312e 3039 3637 3438 2043 2031 332e  ,21.096748 C 13.
+00008690: 3136 3631 3336 2c32 302e 3632 3934 3535  166136,20.629455
+000086a0: 2031 332e 3239 3031 3534 2c32 302e 3132   13.290154,20.12
+000086b0: 3132 3138 2031 332e 3332 3830 3635 2c31  1218 13.328065,1
+000086c0: 392e 3630 3739 3838 2043 2031 332e 3335  9.607988 C 13.35
+000086d0: 3931 312c 3139 2e31 3830 3430 3120 3133  911,19.180401 13
+000086e0: 2e33 3339 3434 342c 3138 2e37 3438 3337  .339444,18.74837
+000086f0: 3720 3133 2e32 3631 3038 332c 3138 2e33  7 13.261083,18.3
+00008700: 3236 3634 3420 4320 3133 2e31 3639 3533  26644 C 13.16953
+00008710: 332c 3137 2e38 3332 3433 3920 3132 2e39  3,17.832439 12.9
+00008720: 3930 3634 322c 3137 2e33 3534 3120 3132  90642,17.3541 12
+00008730: 2e37 3330 3431 342c 3136 2e39 3233 3836  .730414,16.92386
+00008740: 3320 4320 3132 2e35 3436 3730 352c 3136  3 C 12.546705,16
+00008750: 2e36 3139 3232 3620 3132 2e33 3234 3833  .619226 12.32483
+00008760: 342c 3136 2e33 3337 3937 2031 322e 3037  4,16.33797 12.07
+00008770: 3438 2c31 362e 3038 3531 3234 2043 2031  48,16.085124 C 1
+00008780: 312e 3730 3735 3031 2c31 352e 3732 3037  1.707501,15.7207
+00008790: 3635 2031 312e 3238 3036 3135 2c31 352e  65 11.280615,15.
+000087a0: 3431 3335 3033 2031 302e 3830 3831 3037  413503 10.808107
+000087b0: 2c31 352e 3230 3037 3420 4320 3130 2e33  ,15.20074 C 10.3
+000087c0: 3533 3836 332c 3134 2e39 3934 3631 3520  53863,14.994615 
+000087d0: 392e 3836 3130 3037 372c 3134 2e38 3738  9.8610077,14.878
+000087e0: 3332 3520 392e 3336 3338 3933 372c 3134  325 9.3638937,14
+000087f0: 2e38 3434 3934 3920 4320 382e 3831 3930  .844949 C 8.8190
+00008800: 3131 382c 3134 2e38 3038 3036 3620 382e  118,14.808066 8.
+00008810: 3236 3531 3436 342c 3134 2e38 3538 3533  2651464,14.85853
+00008820: 3420 372e 3734 3239 3637 392c 3135 2e30  4 7.7429679,15.0
+00008830: 3232 3633 3420 4320 372e 3238 3031 3432  22634 C 7.280142
+00008840: 312c 3135 2e31 3636 3638 2036 2e38 3436  1,15.16668 6.846
+00008850: 3730 3238 2c31 352e 3430 3030 3039 2036  7028,15.400009 6
+00008860: 2e34 3635 3037 3337 2c31 352e 3639 3832  .4650737,15.6982
+00008870: 3133 2043 2036 2e30 3538 3638 3638 2c31  13 C 6.0586868,1
+00008880: 362e 3031 3533 3239 2035 2e37 3033 3831  6.015329 5.70381
+00008890: 3632 2c31 362e 3339 3931 3734 2035 2e34  62,16.399174 5.4
+000088a0: 3233 3531 3835 2c31 362e 3833 3230 3235  235185,16.832025
+000088b0: 2043 2035 2e31 3533 3134 3839 2c31 372e   C 5.1531489,17.
+000088c0: 3234 3932 3333 2034 2e39 3539 3239 3832  249233 4.9592982
+000088d0: 2c31 372e 3731 3536 3331 2034 2e38 3533  ,17.715631 4.853
+000088e0: 3936 3239 2c31 382e 3230 3135 3131 2043  9629,18.201511 C
+000088f0: 2034 2e37 3831 3739 3533 2c31 382e 3533   4.7817953,18.53
+00008900: 3133 3536 2034 2e37 3438 3935 3035 2c31  1356 4.7489505,1
+00008910: 382e 3836 3932 3838 2034 2e37 3439 3032  8.869288 4.74902
+00008920: 3735 2c31 392e 3230 3637 3639 207a 2022  75,19.206769 z "
+00008930: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00008940: 2020 2020 2020 2020 2073 7479 6c65 3d22           style="
+00008950: 6669 6c6c 3a20 247a 6f64 6961 635f 636f  fill: $zodiac_co
+00008960: 6c6f 725f 3422 0a20 2020 2020 2020 2020  lor_4".         
+00008970: 2020 2020 2020 2020 2020 202f 3e0a 2020             />.  
+00008980: 2020 2020 2020 2020 2020 2020 2020 3c2f                </
+00008990: 7379 6d62 6f6c 3e0a 2020 2020 2020 2020  symbol>.        
+000089a0: 2020 2020 2020 2020 3c73 796d 626f 6c20          <symbol 
+000089b0: 6964 3d22 7669 7267 6f22 3e0a 2020 2020  id="virgo">.    
+000089c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000089d0: 3c70 6174 680a 2020 2020 2020 2020 2020  <path.          
+000089e0: 2020 2020 2020 2020 2020 2020 2020 643d                d=
+000089f0: 224d 2037 2e31 3633 3238 3535 2c39 2e37  "M 7.1632855,9.7
+00008a00: 3438 3833 3633 2043 2037 2e31 3633 3238  488363 C 7.16328
+00008a10: 3535 2c31 342e 3934 3938 3639 2037 2e31  55,14.949869 7.1
+00008a20: 3633 3238 3535 2c32 302e 3135 3039 3033  632855,20.150903
+00008a30: 2037 2e31 3633 3238 3535 2c32 352e 3335   7.1632855,25.35
+00008a40: 3139 3336 2043 2036 2e33 3331 3035 3435  1936 C 6.3310545
+00008a50: 2c32 352e 3335 3139 3336 2035 2e34 3938  ,25.351936 5.498
+00008a60: 3832 3335 2c32 352e 3335 3139 3336 2034  8235,25.351936 4
+00008a70: 2e36 3636 3539 3235 2c32 352e 3335 3139  .6665925,25.3519
+00008a80: 3336 2043 2034 2e36 3636 3539 3235 2c31  36 C 4.6665925,1
+00008a90: 392e 3332 3831 3634 2034 2e36 3636 3539  9.328164 4.66659
+00008aa0: 3235 2c31 332e 3330 3433 3932 2034 2e36  25,13.304392 4.6
+00008ab0: 3636 3539 3235 2c37 2e32 3830 3631 3938  665925,7.2806198
+00008ac0: 2043 2034 2e36 3637 3334 3235 2c36 2e31   C 4.6673425,6.1
+00008ad0: 3035 3832 3636 2034 2e35 3133 3738 3235  058266 4.5137825
+00008ae0: 2c34 2e39 3238 3932 3837 2034 2e31 3835  ,4.9289287 4.185
+00008af0: 3733 3435 2c33 2e37 3939 3838 3220 4320  7345,3.799882 C 
+00008b00: 332e 3837 3138 3739 352c 322e 3731 3339  3.8718795,2.7139
+00008b10: 3830 3720 332e 3339 3638 3936 352c 312e  807 3.3968965,1.
+00008b20: 3637 3537 3630 3620 322e 3738 3934 3134  6757606 2.789414
+00008b30: 392c 302e 3732 3234 3935 3435 2043 2032  9,0.72249545 C 2
+00008b40: 2e37 3334 3830 3037 2c30 2e36 3334 3436  .7348007,0.63446
+00008b50: 3537 2032 2e36 3730 3632 3537 2c30 2e35  57 2.6706257,0.5
+00008b60: 3432 3635 3931 3920 322e 3631 3931 3239  4265919 2.619129
+00008b70: 332c 302e 3435 3839 3134 3720 4320 332e  3,0.4589147 C 3.
+00008b80: 3439 3632 3138 352c 302e 3435 3839 3134  4962185,0.458914
+00008b90: 3720 342e 3337 3333 3036 352c 302e 3435  7 4.3733065,0.45
+00008ba0: 3839 3134 3720 352e 3235 3033 3936 352c  89147 5.2503965,
+00008bb0: 302e 3435 3839 3134 3720 4320 352e 3739  0.4589147 C 5.79
+00008bc0: 3831 3936 352c 312e 3230 3939 3638 3320  81965,1.2099683 
+00008bd0: 362e 3231 3339 3734 352c 322e 3035 3039  6.2139745,2.0509
+00008be0: 3539 3320 362e 3532 3735 3931 352c 322e  593 6.5275915,2.
+00008bf0: 3932 3430 3037 3320 4320 362e 3831 3431  9240073 C 6.8141
+00008c00: 3637 352c 332e 3732 3230 3834 3820 372e  675,3.7220848 7.
+00008c10: 3031 3737 3134 352c 342e 3534 3832 3134  0177145,4.548214
+00008c20: 3320 372e 3136 3332 3835 352c 352e 3338  3 7.1632855,5.38
+00008c30: 3239 3435 3520 4320 372e 3630 3731 3434  29455 C 7.607144
+00008c40: 352c 342e 3239 3539 3631 3320 382e 3132  5,4.2959613 8.12
+00008c50: 3333 3637 352c 332e 3233 3535 3036 3220  33675,3.2355062 
+00008c60: 382e 3735 3131 3336 352c 322e 3234 3138  8.7511365,2.2418
+00008c70: 3430 3520 4320 392e 3134 3933 3936 352c  405 C 9.1493965,
+00008c80: 312e 3631 3234 3630 3120 392e 3539 3332  1.6124601 9.5932
+00008c90: 3737 352c 312e 3031 3034 3538 3320 3130  775,1.0104583 10
+00008ca0: 2e30 3934 3732 372c 302e 3435 3839 3134  .094727,0.458914
+00008cb0: 3720 4320 3130 2e39 3130 3339 362c 302e  7 C 10.910396,0.
+00008cc0: 3330 3539 3433 3535 2031 312e 3732 3630  30594355 11.7260
+00008cd0: 3635 2c30 2e31 3532 3937 3131 3620 3132  65,0.15297116 12
+00008ce0: 2e35 3431 3733 342c 342e 3434 3038 3932  .541734,4.440892
+00008cf0: 3165 2d31 3520 4320 3133 2e31 3135 3432  1e-15 C 13.11542
+00008d00: 382c 302e 3733 3736 3233 3535 2031 332e  8,0.73762355 13.
+00008d10: 3535 3638 3538 2c31 2e35 3732 3038 3933  556858,1.5720893
+00008d20: 2031 332e 3838 3631 3239 2c32 2e34 3434   13.886129,2.444
+00008d30: 3637 3039 2043 2031 342e 3237 3135 3935  6709 C 14.271595
+00008d40: 2c33 2e34 3636 3033 3532 2031 342e 3530  ,3.4660352 14.50
+00008d50: 3931 362c 342e 3533 3832 3734 3520 3134  916,4.5382745 14
+00008d60: 2e36 3531 3531 322c 352e 3631 3839 3439  .651512,5.618949
+00008d70: 3220 4320 3134 2e36 3536 3338 332c 352e  2 C 14.656383,5.
+00008d80: 3635 3630 3239 3520 3134 2e36 3631 3134  6560295 14.66114
+00008d90: 312c 352e 3639 3331 3233 3420 3134 2e36  1,5.6931234 14.6
+00008da0: 3635 3738 362c 352e 3733 3032 3332 3320  65786,5.7302323 
+00008db0: 4320 3135 2e30 3338 3839 332c 342e 3535  C 15.038893,4.55
+00008dc0: 3438 3634 3920 3135 2e35 3930 3537 312c  48649 15.590571,
+00008dd0: 332e 3434 3034 3139 3120 3136 2e32 3538  3.4404191 16.258
+00008de0: 3132 322c 322e 3430 3437 3732 3620 4320  122,2.4047726 C 
+00008df0: 3136 2e36 3936 3633 362c 312e 3732 3431  16.696636,1.7241
+00008e00: 3237 3720 3137 2e31 3835 3030 342c 312e  277 17.185004,1.
+00008e10: 3037 3631 3136 3620 3137 2e37 3039 3031  0761166 17.70901
+00008e20: 392c 302e 3435 3839 3134 3720 4320 3138  9,0.4589147 C 18
+00008e30: 2e35 3132 3236 372c 302e 3330 3539 3433  .512267,0.305943
+00008e40: 3535 2031 392e 3331 3535 3134 2c30 2e31  55 19.315514,0.1
+00008e50: 3532 3937 3131 3620 3230 2e31 3138 3736  5297116 20.11876
+00008e60: 322c 342e 3434 3038 3932 3165 2d31 3520  2,4.4408921e-15 
+00008e70: 4320 3230 2e37 3236 3535 392c 302e 3833  C 20.726559,0.83
+00008e80: 3934 3536 3635 2032 312e 3232 3238 3736  945665 21.222876
+00008e90: 2c31 2e37 3631 3736 3132 2032 312e 3536  ,1.7617612 21.56
+00008ea0: 3532 3435 2c32 2e37 3430 3431 3534 2043  5245,2.7404154 C
+00008eb0: 2032 312e 3839 3831 3634 2c33 2e36 3837   21.898164,3.687
+00008ec0: 3230 3335 2032 322e 3038 3530 3536 2c34  2035 22.085056,4
+00008ed0: 2e36 3833 3633 3339 2032 322e 3133 3131  .6836339 22.1311
+00008ee0: 3537 2c35 2e36 3835 3630 3936 2043 2032  57,5.6856096 C 2
+00008ef0: 322e 3134 3336 3038 2c35 2e39 3237 3033  2.143608,5.92703
+00008f00: 3620 3232 2e31 3433 3639 362c 362e 3136  6 22.143696,6.16
+00008f10: 3837 3837 3320 3232 2e31 3433 3434 342c  87873 22.143444,
+00008f20: 362e 3431 3034 3534 3220 4320 3232 2e31  6.4104542 C 22.1
+00008f30: 3433 3434 342c 372e 3932 3432 3832 3320  43444,7.9242823 
+00008f40: 3232 2e31 3433 3434 342c 392e 3433 3831  22.143444,9.4381
+00008f50: 3039 3220 3232 2e31 3433 3434 342c 3130  092 22.143444,10
+00008f60: 2e39 3531 3933 3720 4320 3232 2e34 3831  .951937 C 22.481
+00008f70: 3334 392c 392e 3939 3830 3235 3320 3232  349,9.9980253 22
+00008f80: 2e38 3538 3939 322c 392e 3035 3636 3737  .858992,9.056677
+00008f90: 3920 3233 2e33 3039 3635 392c 382e 3134  9 23.309659,8.14
+00008fa0: 3938 3635 2043 2032 332e 3539 3633 342c  9865 C 23.59634,
+00008fb0: 372e 3537 3533 3431 2032 332e 3931 3233  7.575341 23.9123
+00008fc0: 3236 2c37 2e30 3133 3937 3739 2032 342e  26,7.0139779 24.
+00008fd0: 3237 3939 3137 2c36 2e34 3836 3832 3134  279917,6.4868214
+00008fe0: 2043 2032 342e 3936 3732 3332 2c36 2e32   C 24.967232,6.2
+00008ff0: 3334 3632 3534 2032 352e 3635 3435 3438  346254 25.654548
+00009000: 2c35 2e39 3832 3432 3832 2032 362e 3334  ,5.9824282 26.34
+00009010: 3138 3633 2c35 2e37 3330 3233 3233 2043  1863,5.7302323 C
+00009020: 2032 372e 3134 3634 3431 2c36 2e39 3730   27.146441,6.970
+00009030: 3637 3632 2032 372e 3830 3637 3537 2c38  6762 27.806757,8
+00009040: 2e33 3038 3039 3838 2032 382e 3236 3234  .3080988 28.2624
+00009050: 3532 2c39 2e37 3135 3434 3735 2043 2032  52,9.7154475 C 2
+00009060: 382e 3637 3930 3231 2c31 302e 3939 3731  8.679021,10.9971
+00009070: 3238 2032 382e 3932 3330 3137 2c31 322e  28 28.923017,12.
+00009080: 3333 3436 3235 2032 382e 3938 3338 3739  334625 28.983879
+00009090: 2c31 332e 3638 3037 3938 2043 2032 392e  ,13.680798 C 29.
+000090a0: 3034 3939 3936 2c31 352e 3135 3138 3620  049996,15.15186 
+000090b0: 3238 2e39 3133 3737 2c31 362e 3633 3339  28.91377,16.6339
+000090c0: 3736 2032 382e 3535 3632 3534 2c31 382e  76 28.556254,18.
+000090d0: 3036 3334 3031 2043 2032 382e 3135 3936  063401 C 28.1596
+000090e0: 3435 2c31 392e 3635 3437 3937 2032 372e  45,19.654797 27.
+000090f0: 3439 3132 3738 2c32 312e 3137 3536 3620  491278,21.17566 
+00009100: 3236 2e36 3038 3734 362c 3232 2e35 3537  26.608746,22.557
+00009110: 3634 3920 4320 3235 2e37 3936 3539 352c  649 C 25.796595,
+00009120: 3233 2e38 3331 3637 3220 3234 2e38 3131  23.831672 24.811
+00009130: 3934 2c32 342e 3939 3035 3332 2032 332e  94,24.990532 23.
+00009140: 3732 3930 3533 2c32 362e 3034 3236 3231  729053,26.042621
+00009150: 2043 2032 332e 3337 3632 3135 2c32 362e   C 23.376215,26.
+00009160: 3338 3534 3338 2032 332e 3031 3236 3738  385438 23.012678
+00009170: 2c32 362e 3731 3732 3238 2032 322e 3634  ,26.717228 22.64
+00009180: 3032 3938 2c32 372e 3033 3837 3538 2043  0298,27.038758 C
+00009190: 2032 322e 3733 3039 3036 2c32 372e 3730   22.730906,27.70
+000091a0: 3332 3239 2032 322e 3934 3638 3131 2c32  3229 22.946811,2
+000091b0: 382e 3334 3532 3820 3233 2e32 3235 3738  8.34528 23.22578
+000091c0: 312c 3238 2e39 3533 3335 3420 4320 3233  1,28.953354 C 23
+000091d0: 2e35 3733 3039 2c32 392e 3730 3735 3631  .57309,29.707561
+000091e0: 2032 342e 3031 3636 3931 2c33 302e 3431   24.016691,30.41
+000091f0: 3339 3938 2032 342e 3530 3336 3139 2c33  3998 24.503619,3
+00009200: 312e 3038 3534 3836 2043 2032 342e 3733  1.085486 C 24.73
+00009210: 3032 3139 2c33 312e 3339 3734 3037 2032  0219,31.397407 2
+00009220: 342e 3936 3730 3539 2c33 312e 3730 3138  4.967059,31.7018
+00009230: 3438 2032 352e 3231 3135 3139 2c33 312e  48 25.211519,31.
+00009240: 3939 3939 3938 2043 2032 342e 3233 3433  999998 C 24.2343
+00009250: 3732 2c33 312e 3939 3939 3938 2032 332e  72,31.999998 23.
+00009260: 3235 3732 3236 2c33 312e 3939 3939 3938  257226,31.999998
+00009270: 2032 322e 3238 3030 3739 2c33 312e 3939   22.280079,31.99
+00009280: 3939 3938 2043 2032 312e 3831 3537 3136  9998 C 21.815716
+00009290: 2c33 312e 3431 3332 3138 2032 312e 3433  ,31.413218 21.43
+000092a0: 3233 3638 2c33 302e 3736 3633 3137 2032  2368,30.766317 2
+000092b0: 312e 3130 3033 3435 2c33 302e 3039 3730  1.100345,30.0970
+000092c0: 3731 2043 2032 302e 3833 3337 3436 2c32  71 C 20.833746,2
+000092d0: 392e 3535 3834 3535 2032 302e 3630 3037  9.558455 20.6007
+000092e0: 3536 2c32 392e 3030 3336 3733 2032 302e  56,29.003673 20.
+000092f0: 3339 3230 3332 2c32 382e 3434 3033 3038  392032,28.440308
+00009300: 2043 2031 392e 3339 3634 3232 2c32 392e   C 19.396422,29.
+00009310: 3030 3436 3338 2031 382e 3332 3333 3931  004638 18.323391
+00009320: 2c32 392e 3432 3338 3239 2031 372e 3232  ,29.423829 17.22
+00009330: 3437 3932 2c32 392e 3734 3031 3233 2043  4792,29.740123 C
+00009340: 2031 362e 3338 3439 3731 2c32 392e 3938   16.384971,29.98
+00009350: 3136 3038 2031 352e 3532 3836 312c 3330  1608 15.52861,30
+00009360: 2e31 3633 3338 3520 3134 2e36 3635 3738  .163385 14.66578
+00009370: 362c 3330 2e33 3030 3737 3320 4320 3134  6,30.300773 C 14
+00009380: 2e36 3635 3738 362c 3239 2e35 3839 3636  .665786,29.58966
+00009390: 3220 3134 2e36 3635 3738 362c 3238 2e38  2 14.665786,28.8
+000093a0: 3738 3535 3120 3134 2e36 3635 3738 362c  78551 14.665786,
+000093b0: 3238 2e31 3637 3434 2043 2031 352e 3831  28.16744 C 15.81
+000093c0: 3235 3032 2c32 372e 3933 3338 3831 2031  2502,27.933881 1
+000093d0: 362e 3934 3636 3031 2c32 372e 3632 3534  6.946601,27.6254
+000093e0: 3236 2031 382e 3033 3635 3639 2c32 372e  26 18.036569,27.
+000093f0: 3139 3732 3331 2043 2031 382e 3638 3134  197231 C 18.6814
+00009400: 3833 2c32 362e 3934 3333 3539 2031 392e  83,26.943359 19.
+00009410: 3331 3034 3632 2c32 362e 3634 3637 3833  310462,26.646783
+00009420: 2031 392e 3930 3735 3939 2c32 362e 3239   19.907599,26.29
+00009430: 3435 3732 2043 2031 392e 3733 3037 3337  4572 C 19.730737
+00009440: 2c32 352e 3139 3936 3120 3139 2e36 3433  ,25.19961 19.643
+00009450: 3233 322c 3234 2e30 3930 3239 2031 392e  232,24.09029 19.
+00009460: 3634 3637 3531 2c32 322e 3938 3131 3734  646751,22.981174
+00009470: 2043 2031 392e 3634 3637 342c 3137 2e39   C 19.64674,17.9
+00009480: 3438 3837 3720 3139 2e36 3436 3737 322c  48877 19.646772,
+00009490: 3132 2e39 3136 3537 3820 3139 2e36 3436  12.916578 19.646
+000094a0: 3733 352c 372e 3838 3432 3831 3120 4320  735,7.8842811 C 
+000094b0: 3139 2e36 3434 3935 312c 362e 3935 3032  19.644951,6.9502
+000094c0: 3032 3420 3139 2e35 3937 3032 362c 362e  024 19.597026,6.
+000094d0: 3031 3431 3238 2031 392e 3435 3536 3737  014128 19.455677
+000094e0: 2c35 2e30 3839 3939 3636 2043 2031 392e  ,5.0899966 C 19.
+000094f0: 3334 3835 3232 2c34 2e33 3938 3235 3731  348522,4.3982571
+00009500: 2031 392e 3138 3839 3536 2c33 2e37 3131   19.188956,3.711
+00009510: 3234 3720 3138 2e39 3330 3932 342c 332e  247 18.930924,3.
+00009520: 3035 3930 3935 3720 4320 3138 2e38 3330  0590957 C 18.830
+00009530: 3037 362c 322e 3830 3530 3935 3120 3138  076,2.8050951 18
+00009540: 2e37 3133 3739 382c 322e 3535 3639 3733  .713798,2.556973
+00009550: 3520 3138 2e35 3738 3531 342c 322e 3331  5 18.578514,2.31
+00009560: 3933 3739 3820 4320 3137 2e37 3338 3937  93798 C 17.73897
+00009570: 372c 332e 3232 3234 3536 3920 3137 2e30  7,3.2224569 17.0
+00009580: 3437 3935 392c 342e 3235 3538 3334 3820  47959,4.2558348 
+00009590: 3136 2e34 3739 3730 362c 352e 3334 3735  16.479706,5.3475
+000095a0: 3934 3120 4320 3135 2e38 3234 3432 392c  941 C 15.824429,
+000095b0: 362e 3630 3734 3837 3420 3135 2e33 3237  6.6074874 15.327
+000095c0: 3634 372c 372e 3934 3437 3739 3720 3134  647,7.9447797 14
+000095d0: 2e39 3337 3336 332c 392e 3330 3834 3138  .937363,9.308418
+000095e0: 3720 4320 3134 2e38 3430 3439 392c 392e  7 C 14.840499,9.
+000095f0: 3634 3834 3833 3220 3134 2e37 3439 3034  6484832 14.74904
+00009600: 392c 392e 3939 3032 3934 3320 3134 2e36  9,9.9902943 14.6
+00009610: 3635 3738 362c 3130 2e33 3333 3834 2043  65786,10.33384 C
+00009620: 2031 342e 3636 3537 3836 2c31 352e 3333   14.665786,15.33
+00009630: 3938 3732 2031 342e 3636 3537 3836 2c32  9872 14.665786,2
+00009640: 302e 3334 3539 3034 2031 342e 3636 3537  0.345904 14.6657
+00009650: 3836 2c32 352e 3335 3139 3336 2043 2031  86,25.351936 C 1
+00009660: 332e 3832 3934 3135 2c32 352e 3335 3139  3.829415,25.3519
+00009670: 3336 2031 322e 3939 3330 3433 2c32 352e  36 12.993043,25.
+00009680: 3335 3139 3336 2031 322e 3135 3636 3732  351936 12.156672
+00009690: 2c32 352e 3335 3139 3336 2043 2031 322e  ,25.351936 C 12.
+000096a0: 3135 3636 3631 2c31 392e 3830 3831 3034  156661,19.808104
+000096b0: 2031 322e 3135 3636 3934 2c31 342e 3236   12.156694,14.26
+000096c0: 3432 3732 2031 322e 3135 3636 3535 2c38  4272 12.156655,8
+000096d0: 2e37 3230 3433 3938 2043 2031 322e 3135  .7204398 C 12.15
+000096e0: 3438 3636 2c37 2e36 3935 3936 3336 2031  4866,7.6959636 1
+000096f0: 322e 3131 3630 3635 2c36 2e36 3730 3132  2.116065,6.67012
+00009700: 3433 2031 312e 3939 3735 3233 2c35 2e36  43 11.997523,5.6
+00009710: 3531 3938 3131 2043 2031 312e 3931 3631  519811 C 11.9161
+00009720: 3631 2c34 2e39 3636 3532 3633 2031 312e  61,4.9665263 11.
+00009730: 3739 3939 3538 2c34 2e32 3833 3033 3938  799958,4.2830398
+00009740: 2031 312e 3630 3636 3131 2c33 2e36 3139   11.606611,3.619
+00009750: 3531 3336 2043 2031 312e 3437 3336 3433  5136 C 11.473643
+00009760: 2c33 2e31 3638 3438 3938 2031 312e 3330  ,3.1684898 11.30
+00009770: 3530 3338 2c32 2e37 3234 3436 3837 2031  5038,2.7244687 1
+00009780: 312e 3036 3335 3932 2c32 2e33 3139 3337  1.063592,2.31937
+00009790: 3938 2043 2031 302e 3130 3134 3034 2c33  98 C 10.101404,3
+000097a0: 2e34 3338 3036 3939 2039 2e32 3932 3138  .4380699 9.29218
+000097b0: 3035 2c34 2e36 3834 3236 3339 2038 2e36  05,4.6842639 8.6
+000097c0: 3331 3730 3735 2c36 2e30 3032 3220 4320  317075,6.0022 C 
+000097d0: 382e 3032 3932 3034 352c 372e 3230 3330  8.0292045,7.2030
+000097e0: 3433 3320 372e 3534 3736 3131 352c 382e  433 7.5476115,8.
+000097f0: 3436 3233 3732 3220 372e 3136 3332 3835  4623722 7.163285
+00009800: 352c 392e 3734 3838 3336 3320 7a20 4d20  5,9.7488363 z M 
+00009810: 3232 2e31 3433 3434 342c 3234 2e37 3036  22.143444,24.706
+00009820: 3937 3520 4320 3233 2e30 3736 3231 312c  975 C 23.076211,
+00009830: 3233 2e37 3630 3437 3220 3233 2e39 3039  23.760472 23.909
+00009840: 3835 392c 3232 2e37 3132 3631 3420 3234  859,22.712614 24
+00009850: 2e35 3837 3631 382c 3231 2e35 3638 3833  .587618,21.56883
+00009860: 3820 4320 3234 2e39 3134 3737 312c 3231  8 C 24.914771,21
+00009870: 2e30 3136 3635 3320 3235 2e32 3036 3835  .016653 25.20685
+00009880: 312c 3230 2e34 3433 3432 3920 3235 2e34  1,20.443429 25.4
+00009890: 3536 3138 392c 3139 2e38 3532 3034 3820  56189,19.852048 
+000098a0: 4320 3235 2e39 3239 3438 392c 3138 2e37  C 25.929489,18.7
+000098b0: 3137 3539 3420 3236 2e32 3434 3831 372c  17594 26.244817,
+000098c0: 3137 2e35 3138 3039 3620 3236 2e33 3935  17.518096 26.395
+000098d0: 3135 332c 3136 2e32 3938 3437 3620 4320  153,16.298476 C 
+000098e0: 3236 2e34 3931 3439 322c 3135 2e35 3136  26.491492,15.516
+000098f0: 3937 3120 3236 2e35 3233 3630 332c 3134  971 26.523603,14
+00009900: 2e37 3237 3530 3120 3236 2e34 3930 3930  .727501 26.49090
+00009910: 322c 3133 2e39 3430 3737 3520 4320 3236  2,13.940775 C 26
+00009920: 2e34 3430 3939 362c 3132 2e37 3536 3135  .440996,12.75615
+00009930: 3920 3236 2e32 3331 3232 372c 3131 2e35  9 26.231227,11.5
+00009940: 3738 3830 3220 3235 2e38 3732 3739 332c  78802 25.872793,
+00009950: 3130 2e34 3438 3537 2043 2032 352e 3638  10.44857 C 25.68
+00009960: 3630 3836 2c39 2e38 3538 3338 3833 2032  6086,9.8583883 2
+00009970: 352e 3435 3938 3034 2c39 2e32 3830 3834  5.459804,9.28084
+00009980: 3431 2032 352e 3139 3930 3938 2c38 2e37  41 25.199098,8.7
+00009990: 3139 3337 3934 2043 2032 342e 3530 3432  193794 C 24.5042
+000099a0: 3332 2c39 2e35 3733 3339 3620 3233 2e39  32,9.573396 23.9
+000099b0: 3333 3132 362c 3130 2e35 3232 3039 3920  33126,10.522099 
+000099c0: 3233 2e34 3438 3939 312c 3131 2e35 3038  23.448991,11.508
+000099d0: 3931 3420 4320 3232 2e39 3236 3238 392c  914 C 22.926289,
+000099e0: 3132 2e35 3736 3234 3520 3232 2e35 3033  12.576245 22.503
+000099f0: 3237 372c 3133 2e36 3839 3935 3720 3232  277,13.689957 22
+00009a00: 2e31 3433 3434 342c 3134 2e38 3231 3730  .143444,14.82170
+00009a10: 3420 4320 3232 2e31 3433 3434 342c 3138  4 C 22.143444,18
+00009a20: 2e31 3136 3739 3520 3232 2e31 3433 3434  .116795 22.14344
+00009a30: 342c 3231 2e34 3131 3838 3420 3232 2e31  4,21.411884 22.1
+00009a40: 3433 3434 342c 3234 2e37 3036 3937 3520  43444,24.706975 
+00009a50: 7a20 220a 2020 2020 2020 2020 2020 2020  z ".            
+00009a60: 2020 2020 2020 2020 2020 2020 7374 796c              styl
+00009a70: 653d 2266 696c 6c3a 2024 7a6f 6469 6163  e="fill: $zodiac
+00009a80: 5f63 6f6c 6f72 5f35 220a 2020 2020 2020  _color_5".      
+00009a90: 2020 2020 2020 2020 2020 2020 2020 2f3e                />
+00009aa0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+00009ab0: 203c 2f73 796d 626f 6c3e 0a20 2020 2020   </symbol>.     
+00009ac0: 2020 2020 2020 2020 2020 203c 7379 6d62             <symb
+00009ad0: 6f6c 2069 643d 226c 6962 7261 223e 0a20  ol id="libra">. 
+00009ae0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00009af0: 2020 203c 7061 7468 0a20 2020 2020 2020     <path.       
+00009b00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00009b10: 2064 3d22 4d20 2d35 2e35 3936 3235 652d   d="M -5.59625e-
+00009b20: 3036 2c32 392e 3139 3037 3039 2043 202d  06,29.190709 C -
+00009b30: 352e 3539 3632 3565 2d30 362c 3238 2e32  5.59625e-06,28.2
+00009b40: 3033 3732 3220 2d35 2e35 3936 3235 652d  03722 -5.59625e-
+00009b50: 3036 2c32 372e 3231 3637 3335 202d 352e  06,27.216735 -5.
+00009b60: 3539 3632 3565 2d30 362c 3236 2e32 3239  59625e-06,26.229
+00009b70: 3733 3520 4320 3130 2e36 3636 3636 372c  735 C 10.666667,
+00009b80: 3236 2e32 3239 3733 3520 3231 2e33 3333  26.229735 21.333
+00009b90: 3332 372c 3236 2e32 3239 3733 3520 3332  327,26.229735 32
+00009ba0: 2c32 362e 3232 3937 3335 2043 2033 322c  ,26.229735 C 32,
+00009bb0: 3237 2e32 3136 3733 3520 3332 2c32 382e  27.216735 32,28.
+00009bc0: 3230 3337 3232 2033 322c 3239 2e31 3930  203722 32,29.190
+00009bd0: 3730 3920 4320 3231 2e33 3333 3332 372c  709 C 21.333327,
+00009be0: 3239 2e31 3930 3730 3920 3130 2e36 3636  29.190709 10.666
+00009bf0: 3636 372c 3239 2e31 3930 3730 3920 2d35  667,29.190709 -5
+00009c00: 2e35 3936 3235 652d 3036 2c32 392e 3139  .59625e-06,29.19
+00009c10: 3037 3039 207a 204d 2031 322e 3634 3837  0709 z M 12.6487
+00009c20: 352c 3137 2e35 3039 3631 2043 2031 322e  5,17.50961 C 12.
+00009c30: 3634 3837 352c 3138 2e34 3332 3434 3620  64875,18.432446 
+00009c40: 3132 2e36 3438 3735 2c31 392e 3335 3532  12.64875,19.3552
+00009c50: 3833 2031 322e 3634 3837 352c 3230 2e32  83 12.64875,20.2
+00009c60: 3738 3133 3320 4320 382e 3433 3235 3032  78133 C 8.432502
+00009c70: 332c 3230 2e32 3738 3133 3320 342e 3231  3,20.278133 4.21
+00009c80: 3632 3431 382c 3230 2e32 3738 3133 3320  62418,20.278133 
+00009c90: 2d35 2e35 3936 3235 652d 3036 2c32 302e  -5.59625e-06,20.
+00009ca0: 3237 3831 3333 2043 202d 352e 3539 3632  278133 C -5.5962
+00009cb0: 3565 2d30 362c 3139 2e32 3836 3137 3620  5e-06,19.286176 
+00009cc0: 2d35 2e35 3936 3235 652d 3036 2c31 382e  -5.59625e-06,18.
+00009cd0: 3239 3432 3331 202d 352e 3539 3632 3565  294231 -5.59625e
+00009ce0: 2d30 362c 3137 2e33 3032 3238 3620 4320  -06,17.302286 C 
+00009cf0: 322e 3935 3538 3137 2c31 372e 3330 3232  2.955817,17.3022
+00009d00: 3836 2035 2e39 3131 3633 3936 2c31 372e  86 5.9116396,17.
+00009d10: 3330 3232 3836 2038 2e38 3637 3436 3233  302286 8.8674623
+00009d20: 2c31 372e 3330 3232 3836 2043 2037 2e38  ,17.302286 C 7.8
+00009d30: 3333 3030 3139 2c31 362e 3235 3833 3139  330019,16.258319
+00009d40: 2037 2e30 3132 3132 3437 2c31 342e 3937   7.0121247,14.97
+00009d50: 3034 3236 2036 2e36 3632 3531 3731 2c31  0426 6.6625171,1
+00009d60: 332e 3533 3336 3038 2043 2036 2e33 3635  3.533608 C 6.365
+00009d70: 3130 3634 2c31 322e 3333 3537 3732 2036  1064,12.335772 6
+00009d80: 2e33 3939 3338 3239 2c31 312e 3037 3335  .3993829,11.0735
+00009d90: 3338 2036 2e36 3339 3338 3337 2c39 2e38  38 6.6393837,9.8
+00009da0: 3639 3033 3935 2043 2036 2e39 3435 3130  690395 C 6.94510
+00009db0: 3935 2c38 2e33 3535 3736 3136 2037 2e36  95,8.3557616 7.6
+00009dc0: 3932 3338 3939 2c36 2e39 3438 3432 3933  923899,6.9484293
+00009dd0: 2038 2e37 3137 3938 3739 2c35 2e37 3938   8.7179879,5.798
+00009de0: 3932 3033 2043 2039 2e38 3732 3436 3833  9203 C 9.8724683
+00009df0: 2c34 2e34 3932 3237 3632 2031 312e 3334  ,4.4922762 11.34
+00009e00: 3534 3437 2c33 2e34 3339 3339 3537 2031  5447,3.4393957 1
+00009e10: 332e 3031 3636 3535 2c32 2e39 3037 3339  3.016655,2.90739
+00009e20: 3237 2043 2031 342e 3531 3939 3039 2c32  27 C 14.519909,2
+00009e30: 2e34 3235 3136 3133 2031 362e 3134 3030  .4251613 16.1400
+00009e40: 3831 2c32 2e33 3337 3738 3435 2031 372e  81,2.3377845 17.
+00009e50: 3639 3532 3731 2c32 2e35 3839 3436 3631  695271,2.5894661
+00009e60: 2043 2031 392e 3236 3634 3339 2c32 2e38   C 19.266439,2.8
+00009e70: 3435 3237 3236 2032 302e 3735 3631 3133  452726 20.756113
+00009e80: 2c33 2e35 3336 3735 3238 2032 312e 3938  ,3.5367528 21.98
+00009e90: 3631 3332 2c34 2e35 3432 3437 3732 2043  6132,4.5424772 C
+00009ea0: 2032 332e 3238 3639 3938 2c35 2e36 3032   23.286998,5.602
+00009eb0: 3234 3132 2032 342e 3338 3536 3834 2c36  2412 24.385684,6
+00009ec0: 2e39 3531 3531 3332 2032 342e 3938 3632  .9515132 24.9862
+00009ed0: 3031 2c38 2e35 3238 3838 3837 2043 2032  01,8.5288887 C 2
+00009ee0: 352e 3436 3330 3632 2c39 2e37 3732 3635  5.463062,9.77265
+00009ef0: 3739 2032 352e 3634 3031 3237 2c31 312e  79 25.640127,11.
+00009f00: 3132 3633 3934 2032 352e 3533 3335 3537  126394 25.533557
+00009f10: 2c31 322e 3435 3231 3636 2043 2032 352e  ,12.452166 C 25.
+00009f20: 3431 3636 3738 2c31 332e 3832 3033 3434  416678,13.820344
+00009f30: 2032 342e 3837 3839 3237 2c31 352e 3133   24.878927,15.13
+00009f40: 3539 3032 2032 342e 3036 3134 3532 2c31  5902 24.061452,1
+00009f50: 362e 3233 3438 3538 2043 2032 332e 3738  6.234858 C 23.78
+00009f60: 3336 3033 2c31 362e 3631 3235 3131 2032  3603,16.612511 2
+00009f70: 332e 3437 3631 3138 2c31 362e 3936 3830  3.476118,16.9680
+00009f80: 3536 2032 332e 3134 3733 352c 3137 2e33  56 23.14735,17.3
+00009f90: 3032 3331 3320 4320 3236 2e30 3938 3233  02313 C 26.09823
+00009fa0: 332c 3137 2e33 3032 3320 3239 2e30 3439  3,17.3023 29.049
+00009fb0: 3131 362c 3137 2e33 3032 3320 3332 2c31  116,17.3023 32,1
+00009fc0: 372e 3330 3232 3836 2043 2033 322c 3138  7.302286 C 32,18
+00009fd0: 2e32 3934 3233 3120 3332 2c31 392e 3238  .294231 32,19.28
+00009fe0: 3631 3736 2033 322c 3230 2e32 3738 3133  6176 32,20.27813
+00009ff0: 3320 4320 3237 2e37 3833 3733 392c 3230  3 C 27.783739,20
+0000a000: 2e32 3738 3133 3320 3233 2e35 3637 3439  .278133 23.56749
+0000a010: 322c 3230 2e32 3738 3133 3320 3139 2e33  2,20.278133 19.3
+0000a020: 3531 3234 342c 3230 2e32 3738 3133 3320  51244,20.278133 
+0000a030: 4320 3139 2e33 3531 3234 342c 3139 2e33  C 19.351244,19.3
+0000a040: 3535 3238 3320 3139 2e33 3531 3234 342c  55283 19.351244,
+0000a050: 3138 2e34 3332 3434 3620 3139 2e33 3531  18.432446 19.351
+0000a060: 3234 342c 3137 2e35 3039 3631 2043 2032  244,17.50961 C 2
+0000a070: 302e 3437 3634 3739 2c31 362e 3738 3731  0.476479,16.7871
+0000a080: 3939 2032 312e 3436 3938 3436 2c31 352e  99 21.469846,15.
+0000a090: 3830 3334 3133 2032 322e 3032 3831 352c  803413 22.02815,
+0000a0a0: 3134 2e35 3735 3333 3720 4320 3232 2e35  14.575337 C 22.5
+0000a0b0: 3834 3630 332c 3133 2e33 3632 3934 2032  84603,13.36294 2
+0000a0c0: 322e 3730 3638 392c 3131 2e39 3734 3238  2.70689,11.97428
+0000a0d0: 2032 322e 3436 3932 3734 2c31 302e 3636   22.469274,10.66
+0000a0e0: 3839 3736 2043 2032 322e 3233 3937 3532  8976 C 22.239752
+0000a0f0: 2c39 2e34 3137 3630 3736 2032 312e 3537  ,9.4176076 21.57
+0000a100: 3436 3138 2c38 2e32 3731 3337 3736 2032  4618,8.2713776 2
+0000a110: 302e 3637 3134 3531 2c37 2e33 3833 3237  0.671451,7.38327
+0000a120: 3033 2043 2031 392e 3735 3135 3633 2c36  03 C 19.751563,6
+0000a130: 2e34 3532 3430 3520 3138 2e35 3631 3632  .452405 18.56162
+0000a140: 2c35 2e37 3731 3836 3820 3137 2e32 3635  ,5.771868 17.265
+0000a150: 3934 312c 352e 3534 3039 3636 3920 4320  941,5.5409669 C 
+0000a160: 3135 2e37 3238 3234 312c 352e 3236 3434  15.728241,5.2644
+0000a170: 3036 2031 342e 3037 3533 3833 2c35 2e34  06 14.075383,5.4
+0000a180: 3836 3431 3938 2031 322e 3732 3533 372c  864198 12.72537,
+0000a190: 362e 3239 3533 3631 2043 2031 312e 3832  6.295361 C 11.82
+0000a1a0: 3335 3333 2c36 2e38 3335 3630 3037 2031  3533,6.8356007 1
+0000a1b0: 312e 3034 3938 3734 2c37 2e35 3834 3835  1.049874,7.58485
+0000a1c0: 3520 3130 2e34 3538 3534 352c 382e 3435  5 10.458545,8.45
+0000a1d0: 3135 3730 3320 4320 392e 3735 3333 3939  15703 C 9.753399
+0000a1e0: 372c 392e 3438 3734 3137 3920 392e 3430  7,9.4874179 9.40
+0000a1f0: 3737 3431 312c 3130 2e37 3436 3738 3920  77411,10.746789 
+0000a200: 392e 3433 3133 3935 392c 3131 2e39 3935  9.4313959,11.995
+0000a210: 3334 3720 4320 392e 3433 3636 3734 322c  347 C 9.4366742,
+0000a220: 3133 2e31 3938 3837 2039 2e37 3639 3133  13.19887 9.76913
+0000a230: 3034 2c31 342e 3430 3937 3434 2031 302e  04,14.409744 10.
+0000a240: 3434 3730 3234 2c31 352e 3431 3039 3739  447024,15.410979
+0000a250: 2043 2031 312e 3031 3432 3135 2c31 362e   C 11.014215,16.
+0000a260: 3236 3234 3537 2031 312e 3739 3237 3632  262457 11.792762
+0000a270: 2c31 362e 3935 3635 3533 2031 322e 3634  ,16.956553 12.64
+0000a280: 3837 352c 3137 2e35 3039 3631 207a 2022  875,17.50961 z "
+0000a290: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+0000a2a0: 2020 2020 2020 2020 2073 7479 6c65 3d22           style="
+0000a2b0: 6669 6c6c 3a20 247a 6f64 6961 635f 636f  fill: $zodiac_co
+0000a2c0: 6c6f 725f 3622 0a20 2020 2020 2020 2020  lor_6".         
+0000a2d0: 2020 2020 2020 2020 2020 202f 3e0a 2020             />.  
+0000a2e0: 2020 2020 2020 2020 2020 2020 2020 3c2f                </
+0000a2f0: 7379 6d62 6f6c 3e0a 2020 2020 2020 2020  symbol>.        
+0000a300: 2020 2020 2020 2020 3c73 796d 626f 6c20          <symbol 
+0000a310: 6964 3d22 7363 6f72 7069 6f22 3e0a 2020  id="scorpio">.  
+0000a320: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000a330: 2020 3c70 6174 680a 2020 2020 2020 2020    <path.        
+0000a340: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000a350: 643d 224d 2032 2e30 3731 3737 352c 3235  d="M 2.071775,25
+0000a360: 2e31 3039 3339 3220 4320 322e 3037 3137  .109392 C 2.0717
+0000a370: 3534 322c 3139 2e32 3433 3339 3220 322e  542,19.243392 2.
+0000a380: 3037 3138 3136 362c 3133 2e33 3737 3339  0718166,13.37739
+0000a390: 3220 322e 3037 3137 3433 322c 372e 3531  2 2.0717432,7.51
+0000a3a0: 3133 3932 3120 4320 322e 3036 3932 3437  13921 C 2.069247
+0000a3b0: 352c 362e 3334 3332 3236 3520 312e 3935  5,6.3432265 1.95
+0000a3c0: 3833 3939 372c 352e 3137 3036 3932 3220  83997,5.1706922 
+0000a3d0: 312e 3637 3731 3632 312c 342e 3033 3532  1.6771621,4.0352
+0000a3e0: 3632 3620 4320 312e 3433 3733 3139 362c  626 C 1.4373196,
+0000a3f0: 332e 3036 3632 3537 3520 312e 3036 3835  3.0662575 1.0685
+0000a400: 3934 2c32 2e31 3235 3134 3335 2030 2e35  94,2.1251435 0.5
+0000a410: 3435 3338 3034 382c 312e 3237 3336 3937  4538048,1.273697
+0000a420: 3120 4320 302e 3337 3935 3732 3038 2c31  1 C 0.37957208,1
+0000a430: 2e30 3033 3530 3632 2030 2e31 3938 3636  .0035062 0.19866
+0000a440: 3435 382c 302e 3734 3235 3934 2030 2e30  458,0.742594 0.0
+0000a450: 3033 3233 3933 3736 342c 302e 3439 3330  032393764,0.4930
+0000a460: 3635 3120 4320 302e 3838 3435 3038 3938  651 C 0.88450898
+0000a470: 2c30 2e34 3933 3036 3531 2031 2e37 3635  ,0.4930651 1.765
+0000a480: 3737 3836 2c30 2e34 3933 3036 3531 2032  7786,0.4930651 2
+0000a490: 2e36 3437 3034 3833 2c30 2e34 3933 3036  .6470483,0.49306
+0000a4a0: 3531 2043 2033 2e32 3334 3035 3333 2c31  51 C 3.2340533,1
+0000a4b0: 2e33 3839 3439 3331 2033 2e36 3938 3333  .3894931 3.69833
+0000a4c0: 3233 2c32 2e33 3635 3139 3031 2034 2e30  23,2.3651901 4.0
+0000a4d0: 3335 3632 3733 2c33 2e33 3832 3334 3234  356273,3.3823424
+0000a4e0: 2043 2034 2e32 3437 3936 3133 2c34 2e30   C 4.2479613,4.0
+0000a4f0: 3231 3033 3733 2034 2e34 3131 3438 3133  210373 4.4114813
+0000a500: 2c34 2e36 3735 3636 3620 342e 3533 3139  ,4.675666 4.5319
+0000a510: 3836 332c 352e 3333 3738 3333 2043 2035  863,5.337833 C 5
+0000a520: 2e30 3438 3531 3933 2c34 2e30 3630 3139  .0485193,4.06019
+0000a530: 3738 2035 2e36 3834 3634 3933 2c32 2e38  78 5.6846493,2.8
+0000a540: 3236 3833 3839 2036 2e34 3736 3731 3733  268389 6.4767173
+0000a550: 2c31 2e36 3937 3936 3520 4320 362e 3736  ,1.697965 C 6.76
+0000a560: 3939 3339 332c 312e 3238 3031 3036 3920  99393,1.2801069 
+0000a570: 372e 3038 3433 3633 332c 302e 3837 3730  7.0843633,0.8770
+0000a580: 3638 3820 372e 3432 3035 3932 332c 302e  688 7.4205923,0.
+0000a590: 3439 3330 3635 3120 4320 382e 3231 3231  4930651 C 8.2121
+0000a5a0: 3033 332c 302e 3333 3336 3137 3120 392e  033,0.3336171 9.
+0000a5b0: 3030 3336 3133 332c 302e 3137 3431 3639  0036133,0.174169
+0000a5c0: 2039 2e37 3935 3132 3433 2c30 2e30 3134   9.7951243,0.014
+0000a5d0: 3732 3130 3033 2043 2031 302e 3332 3138  721003 C 10.3218
+0000a5e0: 2c30 2e36 3239 3035 3834 2031 302e 3732  ,0.6290584 10.72
+0000a5f0: 3739 372c 312e 3334 3030 3030 3520 3131  797,1.3400005 11
+0000a600: 2e30 3337 3731 342c 322e 3038 3631 3538  .037714,2.086158
+0000a610: 3520 4320 3131 2e34 3031 3335 382c 322e  5 C 11.401358,2.
+0000a620: 3936 3239 3235 3320 3131 2e36 3338 3033  9629253 11.63803
+0000a630: 392c 332e 3838 3830 3031 3220 3131 2e37  9,3.8880012 11.7
+0000a640: 3938 3132 352c 342e 3832 3233 3935 2043  98125,4.822395 C
+0000a650: 2031 312e 3834 3139 3732 2c35 2e30 3739   11.841972,5.079
+0000a660: 3137 3633 2031 312e 3837 3938 3837 2c35  1763 11.879887,5
+0000a670: 2e33 3336 3936 3538 2031 312e 3931 3236  .3369658 11.9126
+0000a680: 3139 2c35 2e35 3935 3430 3239 2043 2031  19,5.5954029 C 1
+0000a690: 322e 3334 3038 3231 2c34 2e33 3630 3233  2.340821,4.36023
+0000a6a0: 3938 2031 322e 3935 3035 342c 332e 3139  98 12.95054,3.19
+0000a6b0: 3239 3637 3220 3133 2e36 3734 3534 332c  29672 13.674543,
+0000a6c0: 322e 3130 3639 3030 3220 4320 3134 2e30  2.1069002 C 14.0
+0000a6d0: 3436 3534 2c31 2e35 3438 3733 3736 2031  4654,1.5487376 1
+0000a6e0: 342e 3434 3839 3137 2c31 2e30 3131 3133  4.448917,1.01113
+0000a6f0: 3736 2031 342e 3837 3436 3634 2c30 2e34  76 14.874664,0.4
+0000a700: 3933 3036 3531 2043 2031 352e 3638 3234  930651 C 15.6824
+0000a710: 3935 2c30 2e33 3333 3631 3731 2031 362e  95,0.3336171 16.
+0000a720: 3439 3033 3235 2c30 2e31 3734 3136 3920  490325,0.174169 
+0000a730: 3137 2e32 3938 3135 362c 302e 3031 3437  17.298156,0.0147
+0000a740: 3231 3030 3320 4320 3137 2e38 3831 3130  21003 C 17.88110
+0000a750: 372c 302e 3830 3238 3632 3920 3138 2e33  7,0.8028629 18.3
+0000a760: 3436 3437 322c 312e 3637 3833 3335 3720  46472,1.6783357 
+0000a770: 3138 2e36 3730 3933 2c32 2e36 3034 3032  18.67093,2.60402
+0000a780: 3734 2043 2031 392e 3032 3735 342c 332e  74 C 19.02754,3.
+0000a790: 3631 3633 3635 3520 3139 2e32 3136 3233  6163655 19.21623
+0000a7a0: 382c 342e 3638 3431 3135 3620 3139 2e32  8,4.6841156 19.2
+0000a7b0: 3636 3336 392c 352e 3735 3532 3838 3820  66369,5.7552888 
+0000a7c0: 4320 3139 2e32 3830 3034 2c36 2e30 3232  C 19.28004,6.022
+0000a7d0: 3135 3231 2031 392e 3238 3134 3434 2c36  1521 19.281444,6
+0000a7e0: 2e32 3839 3337 3733 2031 392e 3238 3130  .2893773 19.2810
+0000a7f0: 3132 2c36 2e35 3536 3532 3339 2043 2031  12,6.5565239 C 1
+0000a800: 392e 3238 3130 3239 2c31 312e 3632 3730  9.281029,11.6270
+0000a810: 3831 2031 392e 3238 3039 3739 2c31 362e  81 19.280979,16.
+0000a820: 3639 3736 3339 2031 392e 3238 3130 3338  697639 19.281038
+0000a830: 2c32 312e 3736 3831 3937 2043 2031 392e  ,21.768197 C 19.
+0000a840: 3238 3233 3737 2c32 322e 3438 3537 3438  282377,22.485748
+0000a850: 2031 392e 3239 3236 3939 2c32 332e 3230   19.292699,23.20
+0000a860: 3336 3339 2031 392e 3333 3430 3333 2c32  3639 19.334033,2
+0000a870: 332e 3932 3031 3235 2043 2031 392e 3335  3.920125 C 19.35
+0000a880: 3432 3937 2c32 342e 3234 3936 3333 2031  4297,24.249633 1
+0000a890: 392e 3337 3838 3331 2c32 342e 3537 3934  9.378831,24.5794
+0000a8a0: 3238 2031 392e 3432 3838 3236 2c32 342e  28 19.428826,24.
+0000a8b0: 3930 3539 3433 2043 2031 392e 3434 3434  905943 C 19.4444
+0000a8c0: 3931 2c32 352e 3031 3230 3535 2031 392e  91,25.012055 19.
+0000a8d0: 3437 3232 3738 2c32 352e 3131 3539 3134  472278,25.115914
+0000a8e0: 2031 392e 3530 3039 3437 2c32 352e 3231   19.500947,25.21
+0000a8f0: 3931 3220 4320 3139 2e35 3939 3838 342c  912 C 19.599884,
+0000a900: 3235 2e35 3636 3932 3620 3139 2e37 3537  25.566926 19.757
+0000a910: 3631 352c 3235 2e38 3938 3431 3820 3139  615,25.898418 19
+0000a920: 2e39 3730 3532 2c32 362e 3139 3037 3631  .97052,26.190761
+0000a930: 2043 2032 302e 3035 3333 3831 2c32 362e   C 20.053381,26.
+0000a940: 3330 3430 3032 2032 302e 3134 3230 3639  304002 20.142069
+0000a950: 2c32 362e 3431 3333 3931 2032 302e 3234  ,26.413391 20.24
+0000a960: 3034 3237 2c32 362e 3531 3335 3332 2043  0427,26.513532 C
+0000a970: 2032 302e 3533 3737 3331 2c32 362e 3831   20.537731,26.81
+0000a980: 3337 3338 2032 302e 3930 3637 3931 2c32  3738 20.906791,2
+0000a990: 372e 3033 3531 3939 2032 312e 3239 3735  7.035199 21.2975
+0000a9a0: 3333 2c32 372e 3139 3036 3520 4320 3231  33,27.19065 C 21
+0000a9b0: 2e37 3833 3732 372c 3237 2e33 3833 3939  .783727,27.38399
+0000a9c0: 3720 3232 2e33 3032 3132 312c 3237 2e34  7 22.302121,27.4
+0000a9d0: 3833 3638 3220 3232 2e38 3231 3234 362c  83682 22.821246,
+0000a9e0: 3237 2e35 3334 3236 3220 4320 3233 2e31  27.534262 C 23.1
+0000a9f0: 3436 3032 322c 3237 2e35 3636 3030 3920  46022,27.566009 
+0000aa00: 3233 2e34 3732 3437 352c 3237 2e35 3736  23.472475,27.576
+0000aa10: 3030 3820 3233 2e37 3938 3637 322c 3237  008 23.798672,27
+0000aa20: 2e35 3734 3730 3420 4320 3234 2e32 3731  .574704 C 24.271
+0000aa30: 3536 312c 3237 2e35 3734 3730 3420 3234  561,27.574704 24
+0000aa40: 2e37 3434 3435 322c 3237 2e35 3734 3730  .744452,27.57470
+0000aa50: 3420 3235 2e32 3137 3334 322c 3237 2e35  4 25.217342,27.5
+0000aa60: 3734 3730 3420 4320 3235 2e32 3137 3334  74704 C 25.21734
+0000aa70: 322c 3236 2e37 3532 3933 3320 3235 2e32  2,26.752933 25.2
+0000aa80: 3137 3334 322c 3235 2e39 3331 3136 3320  17342,25.931163 
+0000aa90: 3235 2e32 3137 3334 322c 3235 2e31 3039  25.217342,25.109
+0000aaa0: 3339 3220 4320 3236 2e35 3134 3736 372c  392 C 26.514767,
+0000aab0: 3236 2e32 3832 3736 3620 3237 2e38 3132  26.282766 27.812
+0000aac0: 3139 322c 3237 2e34 3536 3134 2032 392e  192,27.45614 29.
+0000aad0: 3130 3936 3137 2c32 382e 3632 3935 3134  109617,28.629514
+0000aae0: 2043 2032 372e 3831 3231 3932 2c32 392e   C 27.812192,29.
+0000aaf0: 3735 3739 3136 2032 362e 3531 3437 3637  757916 26.514767
+0000ab00: 2c33 302e 3838 3633 3137 2032 352e 3231  ,30.886317 25.21
+0000ab10: 3733 3432 2c33 322e 3031 3437 3139 2043  7342,32.014719 C
+0000ab20: 2032 352e 3231 3733 3432 2c33 312e 3231   25.217342,31.21
+0000ab30: 3734 3739 2032 352e 3231 3733 3432 2c33  7479 25.217342,3
+0000ab40: 302e 3432 3032 3339 2032 352e 3231 3733  0.420239 25.2173
+0000ab50: 3432 2c32 392e 3632 3239 3938 2043 2032  42,29.622998 C 2
+0000ab60: 342e 3434 3938 3339 2c32 392e 3632 3239  4.449839,29.6229
+0000ab70: 3331 2032 332e 3638 3233 3334 2c32 392e  31 23.682334,29.
+0000ab80: 3632 3331 3334 2032 322e 3931 3438 332c  623134 22.91483,
+0000ab90: 3239 2e36 3232 3839 3520 4320 3232 2e31  29.622895 C 22.1
+0000aba0: 3735 3234 372c 3239 2e36 3139 3238 3220  75247,29.619282 
+0000abb0: 3231 2e34 3331 3838 392c 3239 2e35 3531  21.431889,29.551
+0000abc0: 3335 2032 302e 3731 3435 3534 2c32 392e  35 20.714554,29.
+0000abd0: 3336 3437 3238 2043 2032 302e 3132 3437  364728 C 20.1247
+0000abe0: 3934 2c32 392e 3231 3130 3833 2031 392e  94,29.211083 19.
+0000abf0: 3535 3234 3332 2c32 382e 3937 3230 3933  552432,28.972093
+0000ac00: 2031 392e 3035 3139 3037 2c32 382e 3632   19.051907,28.62
+0000ac10: 3036 3736 2043 2031 382e 3638 3735 3531  0676 C 18.687551
+0000ac20: 2c32 382e 3336 3632 3537 2031 382e 3336  ,28.366257 18.36
+0000ac30: 3535 3433 2c32 382e 3035 3137 3336 2031  5543,28.051736 1
+0000ac40: 382e 3130 3039 3839 2c32 372e 3639 3433  8.100989,27.6943
+0000ac50: 3834 2043 2031 372e 3732 3533 3138 2c32  84 C 17.725318,2
+0000ac60: 372e 3138 3934 3636 2031 372e 3436 3031  7.189466 17.4601
+0000ac70: 352c 3236 2e36 3039 3435 2031 372e 3237  5,26.60945 17.27
+0000ac80: 3237 3134 2c32 362e 3031 3033 3438 2043  2714,26.010348 C
+0000ac90: 2031 372e 3034 3338 3236 2c32 352e 3237   17.043826,25.27
+0000aca0: 3632 3636 2031 362e 3932 3534 3238 2c32  6266 16.925428,2
+0000acb0: 342e 3531 3138 2031 362e 3836 3631 3835  4.5118 16.866185
+0000acc0: 2c32 332e 3734 3633 3634 2043 2031 362e  ,23.746364 C 16.
+0000acd0: 3833 3132 3131 2c32 332e 3239 3534 3134  831211,23.295414
+0000ace0: 2031 362e 3831 3934 3739 2c32 322e 3834   16.819479,22.84
+0000acf0: 3320 3136 2e38 3230 3830 312c 3232 2e33  3 16.820801,22.3
+0000ad00: 3930 3738 3520 4320 3136 2e38 3230 3739  90785 C 16.82079
+0000ad10: 2c31 372e 3437 3335 3033 2031 362e 3832  ,17.473503 16.82
+0000ad20: 3038 3233 2c31 322e 3535 3632 3231 2031  0823,12.556221 1
+0000ad30: 362e 3832 3037 3835 2c37 2e36 3338 3933  6.820785,7.63893
+0000ad40: 3832 2043 2031 362e 3831 3839 3936 2c36  82 C 16.818996,6
+0000ad50: 2e37 3632 3231 3932 2031 362e 3737 3735  .7622192 16.7775
+0000ad60: 3933 2c35 2e38 3833 3635 3932 2031 362e  93,5.8836592 16.
+0000ad70: 3635 3039 3737 2c35 2e30 3135 3435 3233  650977,5.0154523
+0000ad80: 2043 2031 362e 3535 3934 372c 342e 3339   C 16.55947,4.39
+0000ad90: 3833 3331 3920 3136 2e34 3235 3434 342c  83319 16.425444,
+0000ada0: 332e 3738 3434 3132 3720 3136 2e32 3033  3.7844127 16.203
+0000adb0: 3934 332c 332e 3230 3031 3033 3120 4320  943,3.2001031 C 
+0000adc0: 3136 2e30 3831 3939 362c 322e 3838 3032  16.081996,2.8802
+0000add0: 3230 3820 3135 2e39 3332 3633 322c 322e  208 15.932632,2.
+0000ade0: 3536 3936 3230 3920 3135 2e37 3433 3639  5696209 15.74369
+0000adf0: 342c 322e 3238 3337 3839 3420 4320 3134  4,2.2837894 C 14
+0000ae00: 2e38 3135 3331 352c 332e 3335 3534 3935  .815315,3.355495
+0000ae10: 2031 342e 3033 3835 3839 2c34 2e35 3536   14.038589,4.556
+0000ae20: 3331 3138 2031 332e 3432 3038 3936 2c35  3118 13.420896,5
+0000ae30: 2e38 3332 3634 3639 2043 2031 322e 3734  .8326469 C 12.74
+0000ae40: 3132 3339 2c37 2e32 3334 3834 3738 2031  1239,7.2348478 1
+0000ae50: 322e 3235 3032 3234 2c38 2e37 3234 3636  2.250224,8.72466
+0000ae60: 3320 3131 2e39 3132 3631 392c 3130 2e32  3 11.912619,10.2
+0000ae70: 3434 3938 3820 4320 3131 2e39 3132 3631  44988 C 11.91261
+0000ae80: 392c 3135 2e31 3939 3739 2031 312e 3931  9,15.19979 11.91
+0000ae90: 3236 3139 2c32 302e 3135 3435 3920 3131  2619,20.15459 11
+0000aea0: 2e39 3132 3631 392c 3235 2e31 3039 3339  .912619,25.10939
+0000aeb0: 3220 4320 3131 2e30 3932 3534 392c 3235  2 C 11.092549,25
+0000aec0: 2e31 3039 3339 3220 3130 2e32 3732 3437  .109392 10.27247
+0000aed0: 382c 3235 2e31 3039 3339 3220 392e 3435  8,25.109392 9.45
+0000aee0: 3234 3038 332c 3235 2e31 3039 3339 3220  24083,25.109392 
+0000aef0: 4320 392e 3435 3233 3937 332c 3139 2e35  C 9.4523973,19.5
+0000af00: 3734 3331 3920 392e 3435 3234 3330 332c  74319 9.4524303,
+0000af10: 3134 2e30 3339 3234 3620 392e 3435 3233  14.039246 9.4523
+0000af20: 3932 332c 382e 3530 3431 3733 3320 4320  923,8.5041733 C 
+0000af30: 392e 3435 3036 3134 332c 372e 3530 3434  9.4506143,7.5044
+0000af40: 3038 3220 392e 3431 3330 3134 332c 362e  082 9.4130143,6.
+0000af50: 3530 3332 3131 3820 392e 3239 3536 3639  5032118 9.295669
+0000af60: 332c 352e 3530 3938 3239 3620 4320 392e  3,5.5098296 C 9.
+0000af70: 3231 3437 3532 332c 342e 3833 3832 3237  2147523,4.838227
+0000af80: 2039 2e30 3938 3630 3433 2c34 2e31 3638   9.0986043,4.168
+0000af90: 3536 3835 2038 2e39 3033 3738 3833 2c33  5685 8.9037883,3
+0000afa0: 2e35 3139 3938 3136 2043 2038 2e37 3733  .5199816 C 8.773
+0000afb0: 3433 3233 2c33 2e30 3930 3530 3833 2038  4323,3.0905083 8
+0000afc0: 2e36 3038 3033 3733 2c32 2e36 3638 3633  .6080373,2.66863
+0000afd0: 3720 382e 3337 3533 3031 332c 322e 3238  7 8.3753013,2.28
+0000afe0: 3337 3839 3420 4320 372e 3433 3335 3434  37894 C 7.433544
+0000aff0: 332c 332e 3334 3433 3739 2036 2e36 3434  3,3.344379 6.644
+0000b000: 3034 3033 2c34 2e35 3336 3932 3931 2036  0403,4.5369291 6
+0000b010: 2e30 3036 3438 3033 2c35 2e38 3033 3639  .0064803,5.80369
+0000b020: 3336 2043 2035 2e33 3831 3534 3833 2c37  36 C 5.3815483,7
+0000b030: 2e30 3434 3134 3036 2034 2e38 3938 3730  .0441406 4.89870
+0000b040: 3533 2c38 2e33 3533 3839 3120 342e 3533  53,8.353891 4.53
+0000b050: 3139 3836 332c 392e 3639 3330 3532 3320  19863,9.6930523 
+0000b060: 4320 342e 3533 3139 3836 332c 3134 2e38  C 4.5319863,14.8
+0000b070: 3331 3833 3320 342e 3533 3139 3836 332c  31833 4.5319863,
+0000b080: 3139 2e39 3730 3631 3220 342e 3533 3139  19.970612 4.5319
+0000b090: 3836 332c 3235 2e31 3039 3339 3220 4320  863,25.109392 C 
+0000b0a0: 332e 3731 3139 3135 332c 3235 2e31 3039  3.7119153,25.109
+0000b0b0: 3339 3220 322e 3839 3138 3435 342c 3235  392 2.8918454,25
+0000b0c0: 2e31 3039 3339 3220 322e 3037 3137 3735  .109392 2.071775
+0000b0d0: 2c32 352e 3130 3933 3932 207a 220a 2020  ,25.109392 z".  
+0000b0e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000b0f0: 2020 2020 2020 7374 796c 653d 2266 696c        style="fil
+0000b100: 6c3a 2024 7a6f 6469 6163 5f63 6f6c 6f72  l: $zodiac_color
+0000b110: 5f37 220a 2020 2020 2020 2020 2020 2020  _7".            
+0000b120: 2020 2020 2020 2020 2f3e 0a20 2020 2020          />.     
+0000b130: 2020 2020 2020 2020 2020 203c 2f73 796d             </sym
+0000b140: 626f 6c3e 0a20 2020 2020 2020 2020 2020  bol>.           
+0000b150: 2020 2020 203c 7379 6d62 6f6c 2069 643d       <symbol id=
+0000b160: 2273 6167 6974 7461 7269 7573 223e 0a20  "sagittarius">. 
+0000b170: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000b180: 2020 203c 7061 7468 0a20 2020 2020 2020     <path.       
+0000b190: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000b1a0: 2064 3d22 4d20 3239 2e38 3932 3934 322c   d="M 29.892942,
+0000b1b0: 322e 3039 3538 3730 3620 4c20 3332 2c31  2.0958706 L 32,1
+0000b1c0: 372e 3131 3632 3736 204c 2032 382e 3939  7.116276 L 28.99
+0000b1d0: 3835 3739 2c31 372e 3538 3730 3838 204c  8579,17.587088 L
+0000b1e0: 2032 372e 3435 3233 3933 2c36 2e36 3336   27.452393,6.636
+0000b1f0: 3932 3335 204c 2031 332e 3733 3337 3736  9235 L 13.733776
+0000b200: 2c32 302e 3431 3139 3537 204c 2032 302e  ,20.411957 L 20.
+0000b210: 3139 3133 3739 2c32 362e 3836 3636 3320  191379,26.86663 
+0000b220: 4c20 3138 2e30 3338 3834 352c 3239 2e30  L 18.038845,29.0
+0000b230: 3233 3235 3120 4c20 3131 2e35 3831 3234  23251 L 11.58124
+0000b240: 322c 3232 2e35 3533 3339 204c 2032 2e30  2,22.55339 L 2.0
+0000b250: 3931 3930 312c 3331 2e39 3939 3939 3520  91901,31.999995 
+0000b260: 4c20 312e 3565 2d30 362c 3239 2e39 3034  L 1.5e-06,29.904
+0000b270: 3132 3420 4c20 392e 3437 3431 3834 2c32  124 L 9.474184,2
+0000b280: 302e 3434 3233 3332 204c 2033 2e30 3331  0.442332 L 3.031
+0000b290: 3734 2c31 332e 3937 3234 3720 4c20 352e  74,13.97247 L 5.
+0000b2a0: 3135 3339 3537 2c31 312e 3831 3538 3520  153957,11.81585 
+0000b2b0: 4c20 3131 2e36 3131 3536 2c31 382e 3238  L 11.61156,18.28
+0000b2c0: 3537 3131 204c 2032 352e 3336 3034 3933  5711 L 25.360493
+0000b2d0: 2c34 2e35 3431 3035 3239 204c 2031 342e  ,4.5410529 L 14.
+0000b2e0: 3433 3130 3736 2c33 2e30 3037 3131 3836  431076,3.0071186
+0000b2f0: 204c 2031 342e 3930 3039 3936 2c2d 342e   L 14.900996,-4.
+0000b300: 3434 3038 3932 3165 2d31 3620 4c20 3239  4408921e-16 L 29
+0000b310: 2e38 3932 3934 322c 322e 3039 3538 3730  .892942,2.095870
+0000b320: 3620 7a20 220a 2020 2020 2020 2020 2020  6 z ".          
+0000b330: 2020 2020 2020 2020 2020 2020 2020 7374                st
+0000b340: 796c 653d 2266 696c 6c3a 2024 7a6f 6469  yle="fill: $zodi
+0000b350: 6163 5f63 6f6c 6f72 5f38 220a 2020 2020  ac_color_8".    
+0000b360: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000b370: 2f3e 0a20 2020 2020 2020 2020 2020 2020  />.             
+0000b380: 2020 203c 2f73 796d 626f 6c3e 0a20 2020     </symbol>.   
+0000b390: 2020 2020 2020 2020 2020 2020 203c 7379               <sy
+0000b3a0: 6d62 6f6c 2069 643d 2263 6170 7269 636f  mbol id="caprico
+0000b3b0: 726e 223e 0a20 2020 2020 2020 2020 2020  rn">.           
+0000b3c0: 2020 2020 2020 2020 203c 7061 7468 0a20           <path. 
+0000b3d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000b3e0: 2020 2020 2020 2064 3d22 4d20 362e 3130         d="M 6.10
+0000b3f0: 3933 3535 392c 3138 2e39 3034 3737 3420  93559,18.904774 
+0000b400: 4320 362e 3130 3932 3339 322c 3138 2e35  C 6.1092392,18.5
+0000b410: 3839 3535 2036 2e31 3039 3630 3432 2c31  8955 6.1096042,1
+0000b420: 382e 3237 3433 3235 2036 2e31 3039 3134  8.274325 6.10914
+0000b430: 3733 2c31 372e 3935 3931 3033 2043 2036  73,17.959103 C 6
+0000b440: 2e31 3033 3633 3839 2c31 372e 3134 3632  .1036389,17.1462
+0000b450: 3334 2036 2e30 3336 3435 3837 2c31 362e  34 6.0364587,16.
+0000b460: 3333 3530 3635 2035 2e39 3436 3339 3638  335065 5.9463968
+0000b470: 2c31 352e 3532 3736 3131 2043 2035 2e38  ,15.527611 C 5.8
+0000b480: 3032 3031 3933 2c31 342e 3235 3436 3432  020193,14.254642
+0000b490: 2035 2e35 3936 3039 3433 2c31 322e 3938   5.5960943,12.98
+0000b4a0: 3934 3635 2035 2e33 3636 3533 3133 2c31  9465 5.3665313,1
+0000b4b0: 312e 3732 3933 3338 2043 2035 2e32 3235  1.729338 C 5.225
+0000b4c0: 3836 3034 2c31 302e 3935 3639 3237 2035  8604,10.956927 5
+0000b4d0: 2e30 3730 3434 2c31 302e 3138 3732 3220  .07044,10.18722 
+0000b4e0: 342e 3930 3335 3537 2c39 2e34 3230 3035  4.903557,9.42005
+0000b4f0: 3437 2043 2034 2e37 3231 3830 3237 2c38  47 C 4.7218027,8
+0000b500: 2e35 3933 3130 3532 2034 2e35 3236 3233  .5931052 4.52623
+0000b510: 3839 2c37 2e37 3638 3439 3037 2034 2e32  89,7.7684907 4.2
+0000b520: 3835 3333 3336 2c36 2e39 3536 3532 3437  853336,6.9565247
+0000b530: 2043 2034 2e31 3533 3230 3336 2c36 2e35   C 4.1532036,6.5
+0000b540: 3136 3935 3534 2034 2e30 3039 3931 3339  169554 4.0099139
+0000b550: 2c36 2e30 3739 3533 2033 2e38 3235 3133  ,6.07953 3.82513
+0000b560: 3334 2c35 2e36 3538 3838 3536 2043 2033  34,5.6588856 C 3
+0000b570: 2e36 3538 3932 3334 2c35 2e32 3833 3631  .6589234,5.28361
+0000b580: 3531 2033 2e34 3437 3231 3638 2c34 2e39  51 3.4472168,4.9
+0000b590: 3236 3935 3239 2033 2e31 3834 3334 3939  269529 3.1843499
+0000b5a0: 2c34 2e36 3131 3038 3838 2043 2032 2e39  ,4.6110888 C 2.9
+0000b5b0: 3030 3932 3039 2c34 2e32 3730 3039 3239  009209,4.2700929
+0000b5c0: 2032 2e35 3531 3435 3238 2c33 2e39 3832   2.5514528,3.982
+0000b5d0: 3030 3131 2032 2e31 3534 3638 3531 2c33  0011 2.1546851,3
+0000b5e0: 2e37 3832 3336 3431 2043 2031 2e37 3237  .7823641 C 1.727
+0000b5f0: 3238 3436 2c33 2e35 3635 3232 3631 2031  2846,3.5652261 1
+0000b600: 2e32 3531 3938 3437 2c33 2e34 3532 3537  .2519847,3.45257
+0000b610: 3137 2030 2e37 3734 3938 3437 382c 332e  17 0.77498478,3.
+0000b620: 3432 3230 3438 3620 4320 302e 3538 3730  4220486 C 0.5870
+0000b630: 3136 3737 2c33 2e34 3038 3937 3036 2030  1677,3.4089706 0
+0000b640: 2e33 3938 3539 3637 352c 332e 3431 3239  .39859675,3.4129
+0000b650: 3732 3820 302e 3231 3033 3431 392c 332e  728 0.2103419,3.
+0000b660: 3431 3232 3935 2043 2030 2e31 3430 3230  412295 C 0.14020
+0000b670: 3339 312c 332e 3431 3232 3935 2030 2e30  391,3.412295 0.0
+0000b680: 3730 3036 3436 3833 2c33 2e34 3132 3239  70064683,3.41229
+0000b690: 3520 2d37 2e33 3330 3237 3765 2d30 352c  5 -7.330277e-05,
+0000b6a0: 332e 3431 3232 3935 2043 202d 372e 3333  3.412295 C -7.33
+0000b6b0: 3032 3737 652d 3035 2c32 2e37 3239 3533  0277e-05,2.72953
+0000b6c0: 3335 202d 372e 3333 3032 3737 652d 3035  35 -7.330277e-05
+0000b6d0: 2c32 2e30 3436 3737 3220 2d37 2e33 3330  ,2.046772 -7.330
+0000b6e0: 3237 3765 2d30 352c 312e 3336 3430 3130  277e-05,1.364010
+0000b6f0: 3620 4320 302e 3632 3736 3334 3534 2c31  6 C 0.62763454,1
+0000b700: 2e33 3634 3033 3137 2031 2e32 3535 3334  .3640317 1.25534
+0000b710: 3234 2c31 2e33 3633 3936 3936 2031 2e38  24,1.3639696 1.8
+0000b720: 3833 3035 3032 2c31 2e33 3634 3034 3136  830502,1.3640416
+0000b730: 2043 2032 2e34 3439 3434 342c 312e 3336   C 2.449444,1.36
+0000b740: 3538 3531 3520 332e 3032 3130 3939 2c31  58515 3.021099,1
+0000b750: 2e34 3339 3131 3536 2033 2e35 3535 3031  .4391156 3.55501
+0000b760: 312c 312e 3633 3433 3239 3520 4320 332e  1,1.6343295 C 3.
+0000b770: 3938 3336 3639 342c 312e 3739 3031 3037  9836694,1.790107
+0000b780: 3120 342e 3338 3332 3836 392c 322e 3032  1 4.3832869,2.02
+0000b790: 3931 3538 2034 2e37 3134 3738 382c 322e  9158 4.714788,2.
+0000b7a0: 3334 3331 3737 3420 4320 352e 3036 3932  3431774 C 5.0692
+0000b7b0: 3535 342c 322e 3637 3634 3830 3520 352e  554,2.6764805 5.
+0000b7c0: 3334 3335 3931 312c 332e 3038 3834 3836  3435911,3.088486
+0000b7d0: 3120 352e 3534 3432 3334 392c 332e 3533  1 5.5442349,3.53
+0000b7e0: 3031 3633 3220 4320 352e 3834 3731 3630  01632 C 5.847160
+0000b7f0: 382c 342e 3138 3435 3437 3920 362e 3038  8,4.1845479 6.08
+0000b800: 3633 3437 342c 342e 3836 3634 3233 2036  63474,4.866423 6
+0000b810: 2e32 3939 3537 3634 2c35 2e35 3534 3632  .2995764,5.55462
+0000b820: 3035 2043 2036 2e36 3331 3632 3134 2c36  05 C 6.6316214,6
+0000b830: 2e36 3335 3035 3720 362e 3839 3630 3035  .635057 6.896005
+0000b840: 372c 372e 3733 3530 3636 3420 372e 3133  7,7.7350664 7.13
+0000b850: 3138 3332 322c 382e 3834 3030 3838 3620  18322,8.8400886 
+0000b860: 4320 372e 3332 3737 3433 372c 392e 3736  C 7.3277437,9.76
+0000b870: 3231 3930 3220 372e 3530 3135 3335 392c  21902 7.5015359,
+0000b880: 3130 2e36 3838 3838 3320 372e 3636 3135  10.688883 7.6615
+0000b890: 3438 332c 3131 2e36 3137 3834 3720 4320  483,11.617847 C 
+0000b8a0: 382e 3038 3137 3833 392c 392e 3734 3030  8.0817839,9.7400
+0000b8b0: 3139 3120 382e 3635 3231 3732 332c 372e  191 8.6521723,7.
+0000b8c0: 3839 3130 3831 3220 392e 3433 3635 3035  8910812 9.436505
+0000b8d0: 312c 362e 3133 3139 3739 3720 4320 3130  1,6.1319797 C 10
+0000b8e0: 2e31 3232 3636 352c 342e 3539 3238 3133  .122665,4.592813
+0000b8f0: 3220 3130 2e39 3736 3733 372c 332e 3132  2 10.976737,3.12
+0000b900: 3338 3233 3320 3132 2e30 3233 3337 322c  38233 12.023372,
+0000b910: 312e 3830 3038 3733 3620 4320 3132 2e31  1.8008736 C 12.1
+0000b920: 3432 3434 322c 312e 3635 3431 3739 3220  42442,1.6541792 
+0000b930: 3132 2e32 3538 3639 2c31 2e35 3030 3439  12.25869,1.50049
+0000b940: 3333 2031 322e 3338 3536 3037 2c31 2e33  33 12.385607,1.3
+0000b950: 3632 3937 3238 2043 2031 332e 3438 3036  629728 C 13.4806
+0000b960: 3931 2c31 2e31 3532 3238 3338 2031 342e  91,1.1522838 14.
+0000b970: 3537 3537 3737 2c30 2e39 3431 3539 3334  575777,0.9415934
+0000b980: 3920 3135 2e36 3730 3836 312c 302e 3733  9 15.670861,0.73
+0000b990: 3039 3034 3437 2043 2031 362e 3031 3034  090447 C 16.0104
+0000b9a0: 3932 2c31 2e35 3031 3536 3539 2031 362e  92,1.5015659 16.
+0000b9b0: 3237 3438 3832 2c32 2e33 3033 3135 3839  274882,2.3031589
+0000b9c0: 2031 362e 3530 3437 3237 2c33 2e31 3132   16.504727,3.112
+0000b9d0: 3633 3937 2043 2031 362e 3834 3731 3233  6397 C 16.847123
+0000b9e0: 2c34 2e33 3237 3339 3237 2031 372e 3130  ,4.3273927 17.10
+0000b9f0: 3930 3231 2c35 2e35 3633 3339 3731 2031  9021,5.5633971 1
+0000ba00: 372e 3333 3333 3032 2c36 2e38 3034 3930  7.333302,6.80490
+0000ba10: 3832 2043 2031 372e 3436 3536 3835 2c37  82 C 17.465685,7
+0000ba20: 2e35 3339 3231 3435 2031 372e 3538 3235  .5392145 17.5825
+0000ba30: 3636 2c38 2e32 3736 3233 3036 2031 372e  66,8.2762306 17.
+0000ba40: 3639 3035 342c 392e 3031 3434 3931 3920  69054,9.0144919 
+0000ba50: 4320 3137 2e38 3431 3031 312c 3130 2e30  C 17.841011,10.0
+0000ba60: 3130 3535 3420 3137 2e39 3931 3438 2c31  10554 17.99148,1
+0000ba70: 312e 3030 3636 3135 2031 382e 3134 3139  1.006615 18.1419
+0000ba80: 3531 2c31 322e 3030 3236 3736 2043 2031  51,12.002676 C 1
+0000ba90: 382e 3233 3632 3236 2c31 322e 3638 3139  8.236226,12.6819
+0000baa0: 3832 2031 382e 3333 3034 3638 2c31 332e  82 18.330468,13.
+0000bab0: 3336 3133 3439 2031 382e 3431 3330 3531  361349 18.413051
+0000bac0: 2c31 342e 3034 3231 3935 2043 2031 382e  ,14.042195 C 18.
+0000bad0: 3434 3836 3639 2c31 342e 3334 3036 3234  448669,14.340624
+0000bae0: 2031 382e 3437 3930 3639 2c31 342e 3633   18.479069,14.63
+0000baf0: 3936 3538 2031 382e 3531 3733 342c 3134  9658 18.51734,14
+0000bb00: 2e39 3337 3737 3420 4320 3138 2e36 3138  .937774 C 18.618
+0000bb10: 3933 342c 3135 2e37 3435 3730 3820 3138  934,15.745708 18
+0000bb20: 2e37 3431 3936 372c 3136 2e35 3531 3739  .741967,16.55179
+0000bb30: 3520 3138 2e39 3136 3938 372c 3137 2e33  5 18.916987,17.3
+0000bb40: 3437 3338 3120 4320 3138 2e39 3936 3233  47381 C 18.99623
+0000bb50: 342c 3137 2e37 3034 3532 3220 3139 2e30  4,17.704522 19.0
+0000bb60: 3836 3134 312c 3138 2e30 3539 3631 3320  86141,18.059613 
+0000bb70: 3139 2e31 3937 3434 322c 3138 2e34 3038  19.197442,18.408
+0000bb80: 3232 2043 2031 392e 3635 3435 3634 2c31  22 C 19.654564,1
+0000bb90: 372e 3533 3430 3134 2032 302e 3230 3330  7.534014 20.2030
+0000bba0: 3731 2c31 362e 3730 3132 3735 2032 302e  71,16.701275 20.
+0000bbb0: 3838 3037 3036 2c31 352e 3938 3133 3533  880706,15.981353
+0000bbc0: 2043 2032 312e 3434 3533 3737 2c31 352e   C 21.445377,15.
+0000bbd0: 3338 3037 3731 2032 322e 3130 3433 3138  380771 22.104318
+0000bbe0: 2c31 342e 3836 3335 3037 2032 322e 3834  ,14.863507 22.84
+0000bbf0: 3233 3136 2c31 342e 3439 3235 3836 2043  2316,14.492586 C
+0000bc00: 2032 332e 3531 3834 3334 2c31 342e 3135   23.518434,14.15
+0000bc10: 3035 3733 2032 342e 3235 3730 3535 2c31  0573 24.257055,1
+0000bc20: 332e 3933 3630 3235 2032 352e 3030 3934  3.936025 25.0094
+0000bc30: 3534 2c31 332e 3835 3033 3034 2043 2032  54,13.850304 C 2
+0000bc40: 352e 3536 3639 3839 2c31 332e 3738 3733  5.566989,13.7873
+0000bc50: 3620 3236 2e31 3332 3231 382c 3133 2e37  6 26.132218,13.7
+0000bc60: 3834 3836 3920 3236 2e36 3839 3431 2c31  84869 26.68941,1
+0000bc70: 332e 3835 3320 4320 3237 2e33 3730 3631  3.853 C 27.37061
+0000bc80: 362c 3133 2e39 3336 3037 3620 3238 2e30  6,13.936076 28.0
+0000bc90: 3338 3837 362c 3134 2e31 3333 3120 3238  38876,14.1331 28
+0000bca0: 2e36 3531 3036 312c 3134 2e34 3434 3136  .651061,14.44416
+0000bcb0: 3920 4320 3239 2e32 3334 3138 372c 3134  9 C 29.234187,14
+0000bcc0: 2e37 3338 3731 3320 3239 2e37 3633 3830  .738713 29.76380
+0000bcd0: 352c 3135 2e31 3333 3738 3520 3330 2e32  5,15.133785 30.2
+0000bce0: 3237 3530 312c 3135 2e35 3932 3834 3720  27501,15.592847 
+0000bcf0: 4320 3330 2e37 3137 3133 2c31 362e 3037  C 30.71713,16.07
+0000bd00: 3135 3137 2033 312e 3133 3338 3035 2c31  1517 31.133805,1
+0000bd10: 362e 3632 3832 3132 2033 312e 3433 3139  6.628212 31.4319
+0000bd20: 342c 3137 2e32 3435 3636 3220 4320 3331  4,17.245662 C 31
+0000bd30: 2e37 3233 3539 2c31 372e 3834 3536 3833  .72359,17.845683
+0000bd40: 2033 312e 3930 3030 3738 2c31 382e 3439   31.900078,18.49
+0000bd50: 3932 3332 2033 312e 3936 3634 3639 2c31  9232 31.966469,1
+0000bd60: 392e 3136 3233 3938 2043 2033 322e 3031  9.162398 C 32.01
+0000bd70: 3536 3132 2c31 392e 3635 3138 3631 2033  5612,19.651861 3
+0000bd80: 322e 3030 3933 3235 2c32 302e 3134 3633  2.009325,20.1463
+0000bd90: 3538 2033 312e 3935 3736 3034 2c32 302e  58 31.957604,20.
+0000bda0: 3633 3533 3336 2043 2033 312e 3837 3934  635336 C 31.8794
+0000bdb0: 322c 3231 2e33 3636 3138 3720 3331 2e36  2,21.366187 31.6
+0000bdc0: 3831 3834 382c 3232 2e30 3835 3834 3920  81848,22.085849 
+0000bdd0: 3331 2e33 3539 3030 372c 3232 2e37 3436  31.359007,22.746
+0000bde0: 3938 3820 4320 3331 2e30 3335 3434 322c  988 C 31.035442,
+0000bdf0: 3233 2e34 3133 3539 3620 3330 2e35 3837  23.413596 30.587
+0000be00: 3136 352c 3234 2e30 3136 3731 3820 3330  165,24.016718 30
+0000be10: 2e30 3537 3635 2c32 342e 3533 3339 3937  .05765,24.533997
+0000be20: 2043 2032 392e 3535 3633 3834 2c32 352e   C 29.556384,25.
+0000be30: 3032 3538 3933 2032 382e 3937 3639 3137  025893 28.976917
+0000be40: 2c32 352e 3434 3135 3231 2032 382e 3333  ,25.441521 28.33
+0000be50: 3739 3833 2c32 352e 3733 3535 3535 2043  7983,25.735555 C
+0000be60: 2032 372e 3732 3034 3331 2c32 362e 3032   27.720431,26.02
+0000be70: 3136 3639 2032 372e 3035 3133 3238 2c32  1669 27.051328,2
+0000be80: 362e 3139 3133 3232 2032 362e 3337 3339  6.191322 26.3739
+0000be90: 382c 3236 2e32 3531 3237 3120 4320 3235  8,26.251271 C 25
+0000bea0: 2e39 3033 3534 392c 3236 2e32 3933 3334  .903549,26.29334
+0000beb0: 3920 3235 2e34 3239 3530 392c 3236 2e32  9 25.429509,26.2
+0000bec0: 3834 3235 3920 3234 2e39 3539 3335 312c  84259 24.959351,
+0000bed0: 3236 2e32 3433 3233 3320 4320 3234 2e31  26.243233 C 24.1
+0000bee0: 3032 3436 342c 3236 2e31 3636 3832 3820  02464,26.166828 
+0000bef0: 3233 2e32 3537 3134 352c 3235 2e39 3535  23.257145,25.955
+0000bf00: 3232 3720 3232 2e34 3638 3435 312c 3235  227 22.468451,25
+0000bf10: 2e36 3130 3939 3120 4320 3231 2e36 3130  .610991 C 21.610
+0000bf20: 3633 322c 3235 2e32 3338 3632 3120 3230  632,25.238621 20
+0000bf30: 2e38 3233 3530 312c 3234 2e37 3133 3534  .823501,24.71354
+0000bf40: 3720 3230 2e31 3236 3036 352c 3234 2e30  7 20.126065,24.0
+0000bf50: 3932 3630 3320 4320 3139 2e39 3231 3034  92603 C 19.92104
+0000bf60: 342c 3233 2e39 3130 3336 3920 3139 2e37  4,23.910369 19.7
+0000bf70: 3233 3333 362c 3233 2e37 3139 3935 3120  23336,23.719951 
+0000bf80: 3139 2e35 3332 3731 362c 3233 2e35 3232  19.532716,23.522
+0000bf90: 3732 3420 4320 3139 2e31 3131 3834 392c  724 C 19.111849,
+0000bfa0: 3234 2e36 3235 3639 3220 3138 2e36 3635  24.625692 18.665
+0000bfb0: 3233 372c 3235 2e37 3139 3834 3420 3138  237,25.719844 18
+0000bfc0: 2e31 3537 3134 2c32 362e 3738 3538 3520  .15714,26.78585 
+0000bfd0: 4320 3137 2e38 3430 3431 2c32 372e 3434  C 17.84041,27.44
+0000bfe0: 3634 3836 2031 372e 3530 3134 3638 2c32  6486 17.501468,2
+0000bff0: 382e 3039 3830 3735 2031 372e 3130 3638  8.098075 17.1068
+0000c000: 3131 2c32 382e 3731 3539 3838 2043 2031  11,28.715988 C 1
+0000c010: 362e 3836 3532 3837 2c32 392e 3039 3038  6.865287,29.0908
+0000c020: 3735 2031 362e 3630 3339 3834 2c32 392e  75 16.603984,29.
+0000c030: 3435 3538 3433 2031 362e 3239 3431 3637  455843 16.294167
+0000c040: 2c32 392e 3737 3738 3633 2043 2031 352e  ,29.777863 C 15.
+0000c050: 3934 3836 3435 2c33 302e 3133 3735 3332  948645,30.137532
+0000c060: 2031 352e 3532 3630 3936 2c33 302e 3431   15.526096,30.41
+0000c070: 3732 3820 3135 2e30 3734 3132 342c 3330  728 15.074124,30
+0000c080: 2e36 3235 3035 3320 4320 3134 2e35 3030  .625053 C 14.500
+0000c090: 3039 312c 3330 2e38 3839 3039 3520 3133  091,30.889095 13
+0000c0a0: 2e38 3832 3030 312c 3331 2e30 3435 3336  .882001,31.04536
+0000c0b0: 2031 332e 3235 3931 3032 2c33 312e 3134   13.259102,31.14
+0000c0c0: 3130 3433 2043 2031 322e 3631 3833 3234  1043 C 12.618324
+0000c0d0: 2c33 312e 3233 3838 3320 3131 2e39 3639  ,31.23883 11.969
+0000c0e0: 3235 352c 3331 2e32 3731 3436 3620 3131  255,31.271466 11
+0000c0f0: 2e33 3231 3536 362c 3331 2e32 3638 3936  .321566,31.26896
+0000c100: 3320 4320 3130 2e35 3938 3236 312c 3331  3 C 10.598261,31
+0000c110: 2e32 3638 3936 3320 392e 3837 3439 3537  .268963 9.874957
+0000c120: 322c 3331 2e32 3638 3936 3320 392e 3135  2,31.268963 9.15
+0000c130: 3136 3532 392c 3331 2e32 3638 3936 3320  16529,31.268963 
+0000c140: 4320 392e 3135 3136 3532 392c 3330 2e35  C 9.1516529,30.5
+0000c150: 3737 3932 3520 392e 3135 3136 3532 392c  77925 9.1516529,
+0000c160: 3239 2e38 3836 3838 3920 392e 3135 3136  29.886889 9.1516
+0000c170: 3532 392c 3239 2e31 3935 3835 3120 4320  529,29.195851 C 
+0000c180: 392e 3532 3834 3139 372c 3239 2e31 3935  9.5284197,29.195
+0000c190: 3734 3620 392e 3930 3531 3837 372c 3239  746 9.9051877,29
+0000c1a0: 2e31 3936 3037 2031 302e 3238 3139 3534  .19607 10.281954
+0000c1b0: 2c32 392e 3139 3536 3732 2043 2031 302e  ,29.195672 C 10.
+0000c1c0: 3938 3030 3735 2c32 392e 3139 3135 3120  980075,29.19151 
+0000c1d0: 3131 2e36 3830 3734 362c 3239 2e31 3434  11.680746,29.144
+0000c1e0: 3131 3620 3132 2e33 3635 3839 362c 3239  116 12.365896,29
+0000c1f0: 2e30 3034 3833 3520 4320 3132 2e38 3739  .004835 C 12.879
+0000c200: 3231 322c 3238 2e38 3939 3138 3520 3133  212,28.899185 13
+0000c210: 2e33 3836 3431 352c 3238 2e37 3430 3535  .386415,28.74055
+0000c220: 2031 332e 3834 3631 3737 2c32 382e 3438   13.846177,28.48
+0000c230: 3533 3932 2043 2031 342e 3138 3033 3836  5392 C 14.180386
+0000c240: 2c32 382e 3330 3030 3937 2031 342e 3438  ,28.300097 14.48
+0000c250: 3634 3734 2c32 382e 3035 3934 3520 3134  6474,28.05945 14
+0000c260: 2e37 3238 3638 2c32 372e 3736 3236 3937  .72868,27.762697
+0000c270: 2043 2031 342e 3936 3835 3239 2c32 372e   C 14.968529,27.
+0000c280: 3437 3031 3720 3135 2e31 3636 3836 2c32  47017 15.16686,2
+0000c290: 372e 3134 3633 3837 2031 352e 3335 3232  7.146387 15.3522
+0000c2a0: 3038 2c32 362e 3831 3734 3438 2043 2031  08,26.817448 C 1
+0000c2b0: 352e 3638 3436 3835 2c32 362e 3232 3037  5.684685,26.2207
+0000c2c0: 3238 2031 352e 3936 3933 3631 2c32 352e  28 15.969361,25.
+0000c2d0: 3539 3837 3937 2031 362e 3233 3739 3038  598797 16.237908
+0000c2e0: 2c32 342e 3937 3131 3639 2043 2031 362e  ,24.971169 C 16.
+0000c2f0: 3639 3936 3239 2c32 332e 3838 3437 3238  699629,23.884728
+0000c300: 2031 372e 3130 3735 3133 2c32 322e 3737   17.107513,22.77
+0000c310: 3632 3734 2031 372e 3439 3439 3635 2c32  6274 17.494965,2
+0000c320: 312e 3636 3134 3831 2043 2031 372e 3535  1.661481 C 17.55
+0000c330: 3831 312c 3231 2e34 3739 3335 3220 3137  811,21.479352 17
+0000c340: 2e36 3230 362c 3231 2e32 3936 3939 3520  .6206,21.296995 
+0000c350: 3137 2e36 3832 3530 322c 3231 2e31 3134  17.682502,21.114
+0000c360: 3433 3820 4320 3137 2e33 3832 3230 362c  438 C 17.382206,
+0000c370: 3230 2e35 3835 3939 3420 3137 2e31 3030  20.585994 17.100
+0000c380: 3433 352c 3230 2e30 3435 3733 3520 3136  435,20.045735 16
+0000c390: 2e38 3637 3435 2c31 392e 3438 3339 3237  .86745,19.483927
+0000c3a0: 2043 2031 362e 3732 3734 3438 2c31 392e   C 16.727448,19.
+0000c3b0: 3134 3439 3036 2031 362e 3630 3633 3136  144906 16.606316
+0000c3c0: 2c31 382e 3739 3639 3737 2031 362e 3532  ,18.796977 16.52
+0000c3d0: 3731 3337 2c31 382e 3433 3834 3038 2043  7137,18.438408 C
+0000c3e0: 2031 362e 3433 3239 3631 2c31 382e 3031   16.432961,18.01
+0000c3f0: 3836 3239 2031 362e 3336 3236 3035 2c31  8629 16.362605,1
+0000c400: 372e 3539 3339 3631 2031 362e 3239 3439  7.593961 16.2949
+0000c410: 3534 2c31 372e 3136 3932 3436 2043 2031  54,17.169246 C 1
+0000c420: 362e 3134 3531 3632 2c31 362e 3231 3131  6.145162,16.2111
+0000c430: 3032 2031 362e 3032 3233 3138 2c31 352e  02 16.022318,15.
+0000c440: 3234 3920 3135 2e39 3033 3436 372c 3134  249 15.903467,14
+0000c450: 2e32 3836 3631 3220 4320 3135 2e36 3933  .286612 C 15.693
+0000c460: 3437 382c 3132 2e37 3035 3938 3620 3135  478,12.705986 15
+0000c470: 2e34 3833 3438 392c 3131 2e31 3235 3336  .483489,11.12536
+0000c480: 3120 3135 2e32 3733 352c 392e 3534 3437  1 15.2735,9.5447
+0000c490: 3334 3420 4320 3135 2e31 3230 3637 362c  344 C 15.120676,
+0000c4a0: 382e 3338 3030 3135 3320 3134 2e39 3434  8.3800153 14.944
+0000c4b0: 3731 332c 372e 3231 3735 3633 2031 342e  713,7.217563 14.
+0000c4c0: 3730 3935 352c 362e 3036 3633 3436 3520  70955,6.0663465 
+0000c4d0: 4320 3134 2e35 3635 3539 342c 352e 3336  C 14.565594,5.36
+0000c4e0: 3935 3834 3720 3134 2e34 3031 3834 362c  95847 14.401846,
+0000c4f0: 342e 3637 3537 3035 3420 3134 2e31 3832  4.6757054 14.182
+0000c500: 3832 2c33 2e39 3938 3330 3932 2043 2031  82,3.9983092 C 1
+0000c510: 342e 3037 3932 3334 2c33 2e36 3830 3838  4.079234,3.68088
+0000c520: 3334 2031 332e 3936 3333 3434 2c33 2e33  34 13.963344,3.3
+0000c530: 3636 3833 3535 2031 332e 3832 3036 3438  668355 13.820648
+0000c540: 2c33 2e30 3634 3730 3733 2043 2031 332e  ,3.0647073 C 13.
+0000c550: 3033 3333 3332 2c33 2e39 3937 3731 3231  033332,3.9977121
+0000c560: 2031 322e 3337 3036 3835 2c35 2e30 3330   12.370685,5.030
+0000c570: 3339 3735 2031 312e 3739 3534 3637 2c36  3975 11.795467,6
+0000c580: 2e31 3035 3532 3039 2043 2031 312e 3133  .1055209 C 11.13
+0000c590: 3039 3032 2c37 2e33 3439 3636 2031 302e  0902,7.34966 10.
+0000c5a0: 3538 3238 332c 382e 3635 3331 3334 3820  58283,8.6531348 
+0000c5b0: 3130 2e31 3038 3630 362c 392e 3938 3035  10.108606,9.9805
+0000c5c0: 3934 3520 4320 392e 3538 3737 3835 352c  945 C 9.5877855,
+0000c5d0: 3131 2e34 3237 3930 3620 392e 3135 3834  11.427906 9.1584
+0000c5e0: 3635 322c 3132 2e39 3131 3431 3320 382e  652,12.911413 8.
+0000c5f0: 3838 3732 3838 352c 3134 2e34 3236 3630  8872885,14.42660
+0000c600: 3320 4320 382e 3639 3830 3536 342c 3135  3 C 8.6980564,15
+0000c610: 2e34 3836 3537 3520 382e 3538 3831 3032  .486575 8.588102
+0000c620: 382c 3136 2e35 3632 3438 3720 382e 3539  8,16.562487 8.59
+0000c630: 3238 3633 372c 3137 2e36 3339 3835 3520  28637,17.639855 
+0000c640: 4320 382e 3539 3238 3633 372c 3138 2e30  C 8.5928637,18.0
+0000c650: 3631 3439 3520 382e 3539 3238 3633 372c  61495 8.5928637,
+0000c660: 3138 2e34 3833 3133 3420 382e 3539 3238  18.483134 8.5928
+0000c670: 3633 372c 3138 2e39 3034 3737 3420 4320  637,18.904774 C 
+0000c680: 372e 3736 3530 3237 332c 3138 2e39 3034  7.7650273,18.904
+0000c690: 3737 3420 362e 3933 3731 3932 322c 3138  774 6.9371922,18
+0000c6a0: 2e39 3034 3737 3420 362e 3130 3933 3535  .904774 6.109355
+0000c6b0: 392c 3138 2e39 3034 3737 3420 7a20 4d20  9,18.904774 z M 
+0000c6c0: 3230 2e30 3931 3530 352c 3231 2e34 3132  20.091505,21.412
+0000c6d0: 3337 2043 2032 302e 3730 3339 3839 2c32  37 C 20.703989,2
+0000c6e0: 322e 3039 3133 3033 2032 312e 3337 3632  2.091303 21.3762
+0000c6f0: 3136 2c32 322e 3732 3230 3220 3232 2e31  16,22.72202 22.1
+0000c700: 3330 3836 372c 3233 2e32 3431 3230 3620  30867,23.241206 
+0000c710: 4320 3232 2e37 3630 3237 362c 3233 2e36  C 22.760276,23.6
+0000c720: 3733 3638 2032 332e 3435 3131 3536 2c32  7368 23.451156,2
+0000c730: 342e 3032 3633 3035 2032 342e 3138 3938  4.026305 24.1898
+0000c740: 3735 2c32 342e 3232 3831 3739 2043 2032  75,24.228179 C 2
+0000c750: 342e 3835 3138 3136 2c32 342e 3431 3034  4.851816,24.4104
+0000c760: 3036 2032 352e 3535 3034 3239 2c32 342e  06 25.550429,24.
+0000c770: 3436 3436 3431 2032 362e 3233 3134 3037  464641 26.231407
+0000c780: 2c32 342e 3337 3235 3836 2043 2032 362e  ,24.372586 C 26.
+0000c790: 3734 3335 3132 2c32 342e 3330 3335 3633  743512,24.303563
+0000c7a0: 2032 372e 3234 3433 3532 2c32 342e 3134   27.244352,24.14
+0000c7b0: 3234 3439 2032 372e 3639 3437 3337 2c32  2449 27.694737,2
+0000c7c0: 332e 3838 3830 3837 2043 2032 382e 3037  3.888087 C 28.07
+0000c7d0: 3339 3939 2c32 332e 3637 3533 3734 2032  3999,23.675374 2
+0000c7e0: 382e 3431 3536 3539 2c32 332e 3339 3839  8.415659,23.3989
+0000c7f0: 3435 2032 382e 3731 3335 3137 2c32 332e  45 28.713517,23.
+0000c800: 3038 3238 3537 2043 2032 392e 3038 3334  082857 C 29.0834
+0000c810: 3837 2c32 322e 3639 3632 3332 2032 392e  87,22.696232 29.
+0000c820: 3338 3137 3035 2c32 322e 3234 3035 3737  381705,22.240577
+0000c830: 2032 392e 3538 3235 3037 2c32 312e 3734   29.582507,21.74
+0000c840: 3433 3532 2043 2032 392e 3830 3637 3536  4352 C 29.806756
+0000c850: 2c32 312e 3139 3435 3034 2032 392e 3931  ,21.194504 29.91
+0000c860: 3138 3934 2c32 302e 3630 3037 3637 2032  1894,20.600767 2
+0000c870: 392e 3932 3436 3736 2c32 302e 3030 3834  9.924676,20.0084
+0000c880: 3820 4320 3239 2e39 3337 3535 332c 3139  8 C 29.937553,19
+0000c890: 2e35 3135 3135 3620 3239 2e38 3739 3034  .515156 29.87904
+0000c8a0: 362c 3139 2e30 3137 3932 3120 3239 2e37  6,19.017921 29.7
+0000c8b0: 3239 3435 352c 3138 2e35 3436 3735 3620  29455,18.546756 
+0000c8c0: 4320 3239 2e35 3736 3730 392c 3138 2e30  C 29.576709,18.0
+0000c8d0: 3630 3535 3820 3239 2e33 3236 3834 312c  60558 29.326841,
+0000c8e0: 3137 2e36 3036 3339 3520 3239 2e30 3035  17.606395 29.005
+0000c8f0: 3334 2c31 372e 3231 3134 3120 4320 3238  34,17.21141 C 28
+0000c900: 2e36 3531 3434 332c 3136 2e37 3736 3531  .651443,16.77651
+0000c910: 3320 3238 2e32 3139 3438 392c 3136 2e34  3 28.219489,16.4
+0000c920: 3030 3533 3720 3237 2e37 3232 3732 372c  00537 27.722727,
+0000c930: 3136 2e31 3337 3336 3420 4320 3237 2e32  16.137364 C 27.2
+0000c940: 3835 3137 352c 3135 2e39 3033 3934 3620  85175,15.903946 
+0000c950: 3236 2e38 3030 3536 332c 3135 2e37 3632  26.800563,15.762
+0000c960: 3430 3220 3236 2e33 3037 3630 322c 3135  402 26.307602,15
+0000c970: 2e37 3132 3532 3820 4320 3235 2e36 3338  .712528 C 25.638
+0000c980: 3532 392c 3135 2e36 3434 3838 3920 3234  529,15.644889 24
+0000c990: 2e39 3532 3537 362c 3135 2e37 3235 3134  .952576,15.72514
+0000c9a0: 3620 3234 2e33 3232 3838 372c 3135 2e39  6 24.322887,15.9
+0000c9b0: 3633 3839 3620 4320 3233 2e37 3331 3738  63896 C 23.73178
+0000c9c0: 312c 3136 2e31 3835 3738 3120 3233 2e31  1,16.185781 23.1
+0000c9d0: 3936 3933 362c 3136 2e35 3431 3432 2032  96936,16.54142 2
+0000c9e0: 322e 3733 3533 382c 3136 2e39 3639 3534  2.73538,16.96954
+0000c9f0: 3220 4320 3232 2e31 3730 3139 372c 3137  2 C 22.170197,17
+0000ca00: 2e34 3933 3337 3620 3231 2e37 3037 3137  .493376 21.70717
+0000ca10: 362c 3138 2e31 3138 3236 3320 3231 2e33  6,18.118263 21.3
+0000ca20: 3132 3536 2c31 382e 3737 3737 2043 2032  1256,18.7777 C 2
+0000ca30: 302e 3831 3539 3833 2c31 392e 3631 3038  0.815983,19.6108
+0000ca40: 3337 2032 302e 3432 3433 3731 2c32 302e  37 20.424371,20.
+0000ca50: 3530 3236 3837 2032 302e 3039 3135 3035  502687 20.091505
+0000ca60: 2c32 312e 3431 3233 3720 7a20 220a 2020  ,21.41237 z ".  
+0000ca70: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ca80: 2020 2020 2020 7374 796c 653d 2266 696c        style="fil
+0000ca90: 6c3a 2024 7a6f 6469 6163 5f63 6f6c 6f72  l: $zodiac_color
+0000caa0: 5f39 220a 2020 2020 2020 2020 2020 2020  _9".            
+0000cab0: 2020 2020 2020 2020 2f3e 0a20 2020 2020          />.     
+0000cac0: 2020 2020 2020 2020 2020 203c 2f73 796d             </sym
+0000cad0: 626f 6c3e 0a20 2020 2020 2020 2020 2020  bol>.           
+0000cae0: 2020 2020 203c 7379 6d62 6f6c 2069 643d       <symbol id=
+0000caf0: 2261 7175 6172 6975 7322 3e0a 2020 2020  "aquarius">.    
+0000cb00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000cb10: 3c70 6174 680a 2020 2020 2020 2020 2020  <path.          
+0000cb20: 2020 2020 2020 2020 2020 2020 2020 643d                d=
+0000cb30: 224d 2032 652d 3036 2c32 342e 3730 3136  "M 2e-06,24.7016
+0000cb40: 3537 204c 2039 2e36 3737 3131 2c31 382e  57 L 9.67711,18.
+0000cb50: 3332 3236 3834 204c 2031 312e 3739 3735  322684 L 11.7975
+0000cb60: 3932 2c32 332e 3236 3431 3432 204c 2031  92,23.264142 L 1
+0000cb70: 392e 3238 3939 3631 2c31 382e 3332 3236  9.289961,18.3226
+0000cb80: 3834 204c 2032 312e 3338 3437 342c 3233  84 L 21.38474,23
+0000cb90: 2e32 3634 3134 3220 4c20 3238 2e38 3839  .264142 L 28.889
+0000cba0: 3936 2c31 382e 3332 3236 3834 204c 2033  96,18.322684 L 3
+0000cbb0: 312e 3938 3731 3439 2c32 352e 3630 3031  1.987149,25.6001
+0000cbc0: 3034 204c 2032 392e 3938 3233 332c 3236  04 L 29.98233,26
+0000cbd0: 2e34 3835 3731 3620 4c20 3237 2e39 3133  .485716 L 27.913
+0000cbe0: 3235 332c 3231 2e35 3434 3235 3820 4c20  253,21.544258 L 
+0000cbf0: 3230 2e33 3832 3333 2c32 362e 3438 3537  20.38233,26.4857
+0000cc00: 3136 204c 2031 382e 3238 3735 3531 2c32  16 L 18.287551,2
+0000cc10: 312e 3534 3432 3538 204c 2031 302e 3832  1.544258 L 10.82
+0000cc20: 3038 3835 2c32 362e 3438 3537 3136 204c  0885,26.485716 L
+0000cc30: 2038 2e37 3133 3235 342c 3231 2e35 3434   8.713254,21.544
+0000cc40: 3235 3820 4c20 312e 3138 3233 3331 2c32  258 L 1.182331,2
+0000cc50: 362e 3438 3537 3136 204c 2032 652d 3036  6.485716 L 2e-06
+0000cc60: 2c32 342e 3730 3136 3537 207a 204d 2030  ,24.701657 z M 0
+0000cc70: 2e30 3132 3835 332c 3131 2e33 3931 3830  .012853,11.39180
+0000cc80: 3820 4c20 392e 3638 3939 3631 2c35 204c  8 L 9.689961,5 L
+0000cc90: 2031 312e 3831 3034 3433 2c39 2e39 3431   11.810443,9.941
+0000cca0: 3435 3820 4c20 3139 2e33 3135 3636 342c  458 L 19.315664,
+0000ccb0: 3520 4c20 3231 2e34 3130 3434 332c 392e  5 L 21.410443,9.
+0000ccc0: 3934 3134 3538 204c 2032 382e 3930 3238  941458 L 28.9028
+0000ccd0: 3132 2c35 204c 2033 322c 3132 2e32 3737  12,5 L 32,12.277
+0000cce0: 3432 204c 2032 392e 3939 3531 3831 2c31  42 L 29.995181,1
+0000ccf0: 332e 3136 3330 3332 204c 2032 372e 3932  3.163032 L 27.92
+0000cd00: 3631 3035 2c38 2e32 3231 3537 3420 4c20  6105,8.221574 L 
+0000cd10: 3230 2e33 3832 3333 2c31 332e 3136 3330  20.38233,13.1630
+0000cd20: 3332 204c 2031 382e 3238 3735 3531 2c38  32 L 18.287551,8
+0000cd30: 2e32 3231 3537 3420 4c20 3130 2e38 3230  .221574 L 10.820
+0000cd40: 3838 352c 3133 2e31 3633 3033 3220 4c20  885,13.163032 L 
+0000cd50: 382e 3733 3839 3537 2c38 2e32 3231 3537  8.738957,8.22157
+0000cd60: 3420 4c20 312e 3230 3830 3334 2c31 332e  4 L 1.208034,13.
+0000cd70: 3136 3330 3332 204c 2030 2e30 3132 3835  163032 L 0.01285
+0000cd80: 332c 3131 2e33 3931 3830 3820 7a20 220a  3,11.391808 z ".
+0000cd90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000cda0: 2020 2020 2020 2020 7374 796c 653d 2266          style="f
+0000cdb0: 696c 6c3a 2024 7a6f 6469 6163 5f63 6f6c  ill: $zodiac_col
+0000cdc0: 6f72 5f31 3022 0a20 2020 2020 2020 2020  or_10".         
+0000cdd0: 2020 2020 2020 2020 2020 202f 3e0a 2020             />.  
+0000cde0: 2020 2020 2020 2020 2020 2020 2020 3c2f                </
+0000cdf0: 7379 6d62 6f6c 3e0a 2020 2020 2020 2020  symbol>.        
+0000ce00: 2020 2020 2020 2020 3c73 796d 626f 6c20          <symbol 
+0000ce10: 6964 3d22 7069 7363 6573 223e 0a20 2020  id="pisces">.   
+0000ce20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ce30: 203c 7061 7468 0a20 2020 2020 2020 2020   <path.         
+0000ce40: 2020 2020 2020 2020 2020 2020 2020 2064                 d
+0000ce50: 3d22 4d20 3133 2e32 3838 3132 322c 3136  ="M 13.288122,16
+0000ce60: 2e34 3933 3539 3320 4320 3133 2e32 3838  .493593 C 13.288
+0000ce70: 3334 312c 3138 2e30 3633 3639 3920 3133  341,18.063699 13
+0000ce80: 2e30 3534 3638 2c31 392e 3632 3833 3632  .05468,19.628362
+0000ce90: 2031 322e 3635 3939 3235 2c32 312e 3134   12.659925,21.14
+0000cea0: 3631 3536 2043 2031 322e 3335 3737 3034  6156 C 12.357704
+0000ceb0: 2c32 322e 3330 3732 3434 2031 312e 3936  ,22.307244 11.96
+0000cec0: 3332 3133 2c32 332e 3434 3334 3039 2031  3213,23.443409 1
+0000ced0: 312e 3530 3033 372c 3234 2e35 3439 3935  1.50037,24.54995
+0000cee0: 3820 4320 3130 2e36 3836 3138 382c 3236  8 C 10.686188,26
+0000cef0: 2e34 3738 3439 3320 392e 3636 3631 3735  .478493 9.666175
+0000cf00: 372c 3238 2e33 3232 3035 3320 382e 3434  7,28.322053 8.44
+0000cf10: 3037 3139 372c 3330 2e30 3230 3037 3620  07197,30.020076 
+0000cf20: 4320 372e 3934 3730 3935 372c 3330 2e37  C 7.9470957,30.7
+0000cf30: 3034 3635 2037 2e34 3230 3738 3037 2c33  0465 7.4207807,3
+0000cf40: 312e 3336 3536 3439 2036 2e38 3634 3039  1.365649 6.86409
+0000cf50: 3237 2c33 3220 4320 352e 3735 3534 3534  27,32 C 5.755454
+0000cf60: 2c33 3220 342e 3634 3638 3135 332c 3332  ,32 4.6468153,32
+0000cf70: 2033 2e35 3338 3137 3636 2c33 3220 4320   3.5381766,32 C 
+0000cf80: 352e 3035 3232 3033 342c 3330 2e34 3034  5.0522034,30.404
+0000cf90: 3035 3520 362e 3430 3937 3932 372c 3238  055 6.4097927,28
+0000cfa0: 2e36 3530 3837 3220 372e 3439 3831 3530  .650872 7.498150
+0000cfb0: 372c 3236 2e37 3336 3333 3520 4320 382e  7,26.736335 C 8.
+0000cfc0: 3433 3235 3034 372c 3235 2e30 3935 3232  4325047,25.09522
+0000cfd0: 3620 392e 3136 3330 3030 372c 3233 2e33  6 9.1630007,23.3
+0000cfe0: 3334 3839 3620 392e 3632 3835 3737 372c  34896 9.6285777,
+0000cff0: 3231 2e35 3033 3537 3920 4320 3130 2e30  21.503579 C 10.0
+0000d000: 3436 3233 382c 3139 2e38 3638 3633 3620  46238,19.868636 
+0000d010: 3130 2e32 3531 3637 352c 3138 2e31 3830  10.251675,18.180
+0000d020: 3731 3120 3130 2e32 3530 3735 362c 3136  711 10.250756,16
+0000d030: 2e34 3933 3539 3320 4320 382e 3038 3931  .493593 C 8.0891
+0000d040: 3633 372c 3136 2e34 3933 3539 3320 352e  637,16.493593 5.
+0000d050: 3932 3735 3730 372c 3136 2e34 3933 3539  9275707,16.49359
+0000d060: 3320 332e 3736 3539 3739 312c 3136 2e34  3 3.7659791,16.4
+0000d070: 3933 3539 3320 4320 332e 3736 3539 3739  93593 C 3.765979
+0000d080: 312c 3135 2e37 3334 3231 3920 332e 3736  1,15.734219 3.76
+0000d090: 3539 3739 312c 3134 2e39 3734 3834 3620  59791,14.974846 
+0000d0a0: 332e 3736 3539 3739 312c 3134 2e32 3135  3.7659791,14.215
+0000d0b0: 3437 3220 4320 352e 3932 3735 3730 372c  472 C 5.9275707,
+0000d0c0: 3134 2e32 3135 3437 3220 382e 3038 3931  14.215472 8.0891
+0000d0d0: 3633 372c 3134 2e32 3135 3437 3220 3130  637,14.215472 10
+0000d0e0: 2e32 3530 3735 362c 3134 2e32 3135 3437  .250756,14.21547
+0000d0f0: 3220 4320 3130 2e31 3535 3936 322c 3132  2 C 10.155962,12
+0000d100: 2e34 3937 3939 3120 392e 3831 3234 3836  .497991 9.812486
+0000d110: 372c 3130 2e37 3936 3437 2039 2e32 3534  7,10.79647 9.254
+0000d120: 3634 3837 2c39 2e31 3730 3034 3320 4320  6487,9.170043 C 
+0000d130: 382e 3631 3035 3436 372c 372e 3238 3634  8.6105467,7.2864
+0000d140: 2037 2e36 3836 3231 3037 2c35 2e35 3035   7.6862107,5.505
+0000d150: 3639 3120 362e 3538 3330 3636 372c 332e  691 6.5830667,3.
+0000d160: 3835 3132 3534 2043 2035 2e36 3734 3330  851254 C 5.67430
+0000d170: 3331 2c32 2e34 3837 3930 3820 342e 3634  31,2.487908 4.64
+0000d180: 3531 3235 2c31 2e32 3037 3039 3839 2033  5125,1.2070989 3
+0000d190: 2e35 3338 3137 3636 2c33 652d 3037 2043  .5381766,3e-07 C
+0000d1a0: 2034 2e35 3836 3036 382c 3365 2d30 3720   4.586068,3e-07 
+0000d1b0: 352e 3633 3339 3539 332c 3365 2d30 3720  5.6339593,3e-07 
+0000d1c0: 362e 3638 3138 3530 372c 3365 2d30 3720  6.6818507,3e-07 
+0000d1d0: 4320 382e 3135 3939 3339 372c 312e 3537  C 8.1599397,1.57
+0000d1e0: 3538 3437 3620 392e 3436 3235 3835 372c  58476 9.4625857,
+0000d1f0: 332e 3332 3136 3520 3130 2e35 3034 3333  3.32165 10.50433
+0000d200: 352c 352e 3231 3632 3331 2043 2031 312e  5,5.216231 C 11.
+0000d210: 3436 3030 3434 2c36 2e39 3530 3234 3820  460044,6.950248 
+0000d220: 3132 2e31 3933 3035 362c 382e 3830 3639  12.193056,8.8069
+0000d230: 3139 2031 322e 3637 3637 3238 2c31 302e  19 12.676728,10.
+0000d240: 3732 3639 3835 2043 2031 322e 3936 3631  726985 C 12.9661
+0000d250: 3731 2c31 312e 3837 3236 3435 2031 332e  71,11.872645 13.
+0000d260: 3136 3833 3634 2c31 332e 3034 3030 3036  168364,13.040006
+0000d270: 2031 332e 3238 3831 3232 2c31 342e 3231   13.288122,14.21
+0000d280: 3534 3732 2043 2031 352e 3338 3339 3035  5472 C 15.383905
+0000d290: 2c31 342e 3231 3534 3732 2031 372e 3437  ,14.215472 17.47
+0000d2a0: 3936 3838 2c31 342e 3231 3534 3732 2031  9688,14.215472 1
+0000d2b0: 392e 3537 3534 372c 3134 2e32 3135 3437  9.57547,14.21547
+0000d2c0: 3220 4320 3139 2e37 3836 3838 322c 3132  2 C 19.786882,12
+0000d2d0: 2e31 3837 3735 3820 3230 2e32 3435 3838  .187758 20.24588
+0000d2e0: 342c 3130 2e31 3834 3133 2032 302e 3936  4,10.18413 20.96
+0000d2f0: 3332 3439 2c38 2e32 3735 3034 3120 4320  3249,8.275041 C 
+0000d300: 3231 2e36 3730 3432 392c 362e 3338 3637  21.670429,6.3867
+0000d310: 3732 2032 322e 3632 3836 3535 2c34 2e35  72 22.628655,4.5
+0000d320: 3934 3834 3920 3233 2e37 3836 3533 332c  94849 23.786533,
+0000d330: 322e 3934 3439 3136 2043 2032 342e 3531  2.944916 C 24.51
+0000d340: 3334 3135 2c31 2e39 3037 3832 3239 2032  3415,1.9078229 2
+0000d350: 352e 3331 3735 3838 2c30 2e39 3235 3536  5.317588,0.92556
+0000d360: 3837 2032 362e 3138 3137 3432 2c33 652d  87 26.181742,3e-
+0000d370: 3037 2043 2032 372e 3232 3936 3333 2c33  07 C 27.229633,3
+0000d380: 652d 3037 2032 382e 3237 3735 3235 2c33  e-07 28.277525,3
+0000d390: 652d 3037 2032 392e 3332 3534 3136 2c33  e-07 29.325416,3
+0000d3a0: 652d 3037 2043 2032 372e 3835 3436 3138  e-07 C 27.854618
+0000d3b0: 2c31 2e36 3034 3038 3837 2032 362e 3531  ,1.6040887 26.51
+0000d3c0: 3838 3439 2c33 2e33 3430 3034 3720 3235  8849,3.340047 25
+0000d3d0: 2e34 3234 3932 312c 352e 3232 3430 3136  .424921,5.224016
+0000d3e0: 2043 2032 342e 3437 3034 3538 2c36 2e38   C 24.470458,6.8
+0000d3f0: 3637 3033 2032 332e 3730 3439 3935 2c38  6703 23.704995,8
+0000d400: 2e36 3235 3439 3820 3233 2e32 3135 3137  .625498 23.21517
+0000d410: 352c 3130 2e34 3633 3336 3420 4320 3232  5,10.463364 C 22
+0000d420: 2e38 3837 3534 372c 3131 2e36 3839 3233  .887547,11.68923
+0000d430: 3220 3232 2e36 3833 3238 312c 3132 2e39  2 22.683281,12.9
+0000d440: 3438 3339 3220 3232 2e36 3132 3833 372c  48392 22.612837,
+0000d450: 3134 2e32 3135 3437 3220 4320 3234 2e37  14.215472 C 24.7
+0000d460: 3734 3432 382c 3134 2e32 3135 3437 3220  74428,14.215472 
+0000d470: 3236 2e39 3336 3032 322c 3134 2e32 3135  26.936022,14.215
+0000d480: 3437 3220 3239 2e30 3937 3631 342c 3134  472 29.097614,14
+0000d490: 2e32 3135 3437 3220 4320 3239 2e30 3937  .215472 C 29.097
+0000d4a0: 3631 342c 3134 2e39 3734 3834 3620 3239  614,14.974846 29
+0000d4b0: 2e30 3937 3631 342c 3135 2e37 3334 3231  .097614,15.73421
+0000d4c0: 3920 3239 2e30 3937 3631 342c 3136 2e34  9 29.097614,16.4
+0000d4d0: 3933 3539 3320 4320 3236 2e39 3336 3032  93593 C 26.93602
+0000d4e0: 322c 3136 2e34 3933 3539 3320 3234 2e37  2,16.493593 24.7
+0000d4f0: 3734 3432 382c 3136 2e34 3933 3539 3320  74428,16.493593 
+0000d500: 3232 2e36 3132 3833 372c 3136 2e34 3933  22.612837,16.493
+0000d510: 3539 3320 4320 3232 2e36 3131 3539 312c  593 C 22.611591,
+0000d520: 3138 2e33 3130 3031 3320 3232 2e38 3530  18.310013 22.850
+0000d530: 3534 342c 3230 2e31 3237 3334 3720 3233  544,20.127347 23
+0000d540: 2e33 3334 3435 342c 3231 2e38 3738 3532  .334454,21.87852
+0000d550: 3420 4320 3233 2e38 3337 3332 322c 3233  4 C 23.837322,23
+0000d560: 2e37 3037 3239 3320 3234 2e36 3034 3336  .707293 24.60436
+0000d570: 392c 3235 2e34 3539 3439 3420 3235 2e35  9,25.459494 25.5
+0000d580: 3730 3639 342c 3237 2e30 3930 3130 3520  70694,27.090105 
+0000d590: 4320 3236 2e36 3232 3732 372c 3238 2e38  C 26.622727,28.8
+0000d5a0: 3637 3736 3520 3237 2e39 3035 3038 332c  67765 27.905083,
+0000d5b0: 3330 2e35 3032 3732 3320 3239 2e33 3235  30.502723 29.325
+0000d5c0: 3431 362c 3332 2043 2032 382e 3232 3138  416,32 C 28.2218
+0000d5d0: 3339 2c33 3220 3237 2e31 3138 3236 342c  39,32 27.118264,
+0000d5e0: 3332 2032 362e 3031 3436 3837 2c33 3220  32 26.014687,32 
+0000d5f0: 4320 3234 2e36 3934 3433 352c 3330 2e35  C 24.694435,30.5
+0000d600: 3038 3337 3720 3233 2e35 3439 3139 372c  08377 23.549197,
+0000d610: 3238 2e38 3633 3331 3520 3232 2e35 3937  28.863315 22.597
+0000d620: 3331 332c 3237 2e31 3133 3832 3120 4320  313,27.113821 C 
+0000d630: 3232 2e31 3034 3238 2c32 362e 3230 3737  22.10428,26.2077
+0000d640: 3938 2032 312e 3636 3035 3333 2c32 352e  98 21.660533,25.
+0000d650: 3237 3439 3120 3231 2e32 3638 3236 352c  27491 21.268265,
+0000d660: 3234 2e33 3230 3933 3520 4320 3230 2e36  24.320935 C 20.6
+0000d670: 3233 3633 342c 3232 2e37 3337 3733 3920  23634,22.737739 
+0000d680: 3230 2e31 3135 3631 332c 3231 2e30 3933  20.115613,21.093
+0000d690: 3732 3920 3139 2e38 3238 3932 322c 3139  729 19.828922,19
+0000d6a0: 2e34 3036 3732 3120 4320 3139 2e36 3635  .406721 C 19.665
+0000d6b0: 3538 352c 3138 2e34 3434 3736 3820 3139  585,18.444768 19
+0000d6c0: 2e35 3735 3430 322c 3137 2e34 3639 3630  .575402,17.46960
+0000d6d0: 3320 3139 2e35 3735 3437 2c31 362e 3439  3 19.57547,16.49
+0000d6e0: 3335 3933 2043 2031 372e 3437 3936 3838  3593 C 17.479688
+0000d6f0: 2c31 362e 3439 3335 3933 2031 352e 3338  ,16.493593 15.38
+0000d700: 3339 3035 2c31 362e 3439 3335 3933 2031  3905,16.493593 1
+0000d710: 332e 3238 3831 3232 2c31 362e 3439 3335  3.288122,16.4935
+0000d720: 3933 207a 2022 0a20 2020 2020 2020 2020  93 z ".         
+0000d730: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+0000d740: 7479 6c65 3d22 6669 6c6c 3a20 247a 6f64  tyle="fill: $zod
+0000d750: 6961 635f 636f 6c6f 725f 3131 220a 2020  iac_color_11".  
+0000d760: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000d770: 2020 2f3e 0a20 2020 2020 2020 2020 2020    />.           
+0000d780: 2020 2020 203c 2f73 796d 626f 6c3e 0a20       </symbol>. 
+0000d790: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+0000d7a0: 212d 2d20 4173 7065 6374 7320 3132 7831  !-- Aspects 12x1
+0000d7b0: 3220 2d2d 3e0a 2020 2020 2020 2020 2020  2 -->.          
+0000d7c0: 2020 2020 2020 3c73 796d 626f 6c20 6964        <symbol id
+0000d7d0: 3d22 6f72 6230 223e 0a20 2020 2020 2020  ="orb0">.       
+0000d7e0: 2020 2020 2020 2020 2020 2020 203c 7061               <pa
+0000d7f0: 7468 0a20 2020 2020 2020 2020 2020 2020  th.             
+0000d800: 2020 2020 2020 2020 2020 2064 3d22 4d20             d="M 
+0000d810: 362e 3036 3937 3533 392c 372e 3332 3334  6.0697539,7.3234
+0000d820: 3835 3220 4320 362e 3036 3937 3533 392c  852 C 6.0697539,
+0000d830: 382e 3733 3534 3838 3220 342e 3931 3733  8.7354882 4.9173
+0000d840: 3635 312c 392e 3838 3031 3434 3220 332e  651,9.8801442 3.
+0000d850: 3439 3538 3231 342c 392e 3838 3031 3434  4958214,9.880144
+0000d860: 3220 4320 322e 3037 3432 3737 352c 392e  2 C 2.0742775,9.
+0000d870: 3838 3031 3434 3220 302e 3932 3138 3838  8801442 0.921888
+0000d880: 3537 2c38 2e37 3335 3438 3832 2030 2e39  57,8.7354882 0.9
+0000d890: 3231 3838 3835 372c 372e 3332 3334 3835  2188857,7.323485
+0000d8a0: 3220 4320 302e 3932 3138 3838 3537 2c35  2 C 0.92188857,5
+0000d8b0: 2e39 3131 3438 3232 2032 2e30 3734 3237  .9114822 2.07427
+0000d8c0: 3735 2c34 2e37 3636 3832 3732 2033 2e34  75,4.7668272 3.4
+0000d8d0: 3935 3832 3134 2c34 2e37 3636 3832 3732  958214,4.7668272
+0000d8e0: 2043 2034 2e39 3137 3336 3531 2c34 2e37   C 4.9173651,4.7
+0000d8f0: 3636 3832 3732 2036 2e30 3639 3735 3339  668272 6.0697539
+0000d900: 2c35 2e39 3131 3438 3232 2036 2e30 3639  ,5.9114822 6.069
+0000d910: 3735 3339 2c37 2e33 3233 3438 3532 204c  7539,7.3234852 L
+0000d920: 2036 2e30 3639 3735 3339 2c37 2e33 3233   6.0697539,7.323
+0000d930: 3438 3532 207a 204d 2035 2e36 3235 3236  4852 z M 5.62526
+0000d940: 3039 2c35 2e32 3131 3332 3032 2043 2031  09,5.2113202 C 1
+0000d950: 302e 3037 3031 392c 302e 3736 3633 3930  0.07019,0.766390
+0000d960: 3138 2031 302e 3037 3031 392c 302e 3736  18 10.07019,0.76
+0000d970: 3633 3930 3138 2031 302e 3037 3031 392c  639018 10.07019,
+0000d980: 302e 3736 3633 3930 3138 220a 2020 2020  0.76639018".    
+0000d990: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000d9a0: 2020 2020 7374 796c 653d 220a 2020 2020      style=".    
+0000d9b0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000d9c0: 2020 2020 2020 2020 6f70 6163 6974 793a          opacity:
+0000d9d0: 2031 3b0a 2020 2020 2020 2020 2020 2020   1;.            
+0000d9e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000d9f0: 6669 6c6c 3a20 6e6f 6e65 3b0a 2020 2020  fill: none;.    
+0000da00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000da10: 2020 2020 2020 2020 6669 6c6c 2d6f 7061          fill-opa
+0000da20: 6369 7479 3a20 313b 0a20 2020 2020 2020  city: 1;.       
+0000da30: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000da40: 2020 2020 2066 696c 6c2d 7275 6c65 3a20       fill-rule: 
+0000da50: 6e6f 6e7a 6572 6f3b 0a20 2020 2020 2020  nonzero;.       
+0000da60: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000da70: 2020 2020 2073 7472 6f6b 653a 2024 6f72       stroke: $or
+0000da80: 625f 636f 6c6f 725f 303b 0a20 2020 2020  b_color_0;.     
+0000da90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000daa0: 2020 2020 2020 2073 7472 6f6b 652d 7769         stroke-wi
+0000dab0: 6474 683a 2031 2e34 3736 3333 3036 343b  dth: 1.47633064;
+0000dac0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+0000dad0: 2020 2020 2020 2020 2020 2020 2073 7472               str
+0000dae0: 6f6b 652d 6c69 6e65 6361 703a 2062 7574  oke-linecap: but
+0000daf0: 743b 0a20 2020 2020 2020 2020 2020 2020  t;.             
+0000db00: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+0000db10: 7472 6f6b 652d 6c69 6e65 6a6f 696e 3a20  troke-linejoin: 
+0000db20: 6d69 7465 723b 0a20 2020 2020 2020 2020  miter;.         
+0000db30: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000db40: 2020 2073 7472 6f6b 652d 6d69 7465 726c     stroke-miterl
+0000db50: 696d 6974 3a20 343b 0a20 2020 2020 2020  imit: 4;.       
+0000db60: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000db70: 2020 2020 2073 7472 6f6b 652d 6461 7368       stroke-dash
+0000db80: 6172 7261 793a 206e 6f6e 653b 0a20 2020  array: none;.   
+0000db90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000dba0: 2020 2020 2020 2020 2073 7472 6f6b 652d           stroke-
+0000dbb0: 6f70 6163 6974 793a 2031 3b0a 2020 2020  opacity: 1;.    
+0000dbc0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000dbd0: 2020 2020 220a 2020 2020 2020 2020 2020      ".          
+0000dbe0: 2020 2020 2020 2020 2020 2f3e 0a20 2020            />.   
+0000dbf0: 2020 2020 2020 2020 2020 2020 203c 2f73               </s
+0000dc00: 796d 626f 6c3e 0a20 2020 2020 2020 2020  ymbol>.         
+0000dc10: 2020 2020 2020 203c 7379 6d62 6f6c 2069         <symbol i
+0000dc20: 643d 226f 7262 3330 223e 0a20 2020 2020  d="orb30">.     
+0000dc30: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+0000dc40: 7061 7468 0a20 2020 2020 2020 2020 2020  path.           
+0000dc50: 2020 2020 2020 2020 2020 2020 2064 3d22               d="
+0000dc60: 4d20 302e 3831 3637 3531 3534 2c36 2e31  M 0.81675154,6.1
+0000dc70: 3334 3233 3938 2043 2031 312e 3334 3636  342398 C 11.3466
+0000dc80: 3135 2c36 2e31 3632 3031 3438 2031 312e  15,6.1620148 11.
+0000dc90: 3334 3636 3135 2c36 2e31 3632 3031 3438  346615,6.1620148
+0000dca0: 2031 312e 3334 3636 3135 2c36 2e31 3632   11.346615,6.162
+0000dcb0: 3031 3438 204d 2031 302e 3631 3231 3834  0148 M 10.612184
+0000dcc0: 2c30 2e37 3539 3935 3737 3320 4320 352e  ,0.75995773 C 5.
+0000dcd0: 3731 3338 3437 392c 352e 3930 3332 3130  7138479,5.903210
+0000dce0: 3820 352e 3731 3338 3437 392c 352e 3930  8 5.7138479,5.90
+0000dcf0: 3332 3130 3820 352e 3731 3338 3437 392c  32108 5.7138479,
+0000dd00: 352e 3930 3332 3130 3820 4d20 312e 3330  5.9032108 M 1.30
+0000dd10: 3533 3435 312c 302e 3735 3939 3537 3733  53451,0.75995773
+0000dd20: 2043 2035 2e38 3830 3731 3839 2c36 2e31   C 5.8807189,6.1
+0000dd30: 3932 3531 3638 2035 2e38 3830 3731 3839  925168 5.8807189
+0000dd40: 2c36 2e31 3932 3531 3638 2035 2e38 3830  ,6.1925168 5.880
+0000dd50: 3731 3839 2c36 2e31 3932 3531 3638 220a  7189,6.1925168".
+0000dd60: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000dd70: 2020 2020 2020 2020 7374 796c 653d 220a          style=".
+0000dd80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000dd90: 2020 2020 2020 2020 2020 2020 6f70 6163              opac
+0000dda0: 6974 793a 2031 3b0a 2020 2020 2020 2020  ity: 1;.        
+0000ddb0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ddc0: 2020 2020 6669 6c6c 3a20 6e6f 6e65 3b0a      fill: none;.
+0000ddd0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000dde0: 2020 2020 2020 2020 2020 2020 6669 6c6c              fill
+0000ddf0: 2d6f 7061 6369 7479 3a20 313b 0a20 2020  -opacity: 1;.   
+0000de00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000de10: 2020 2020 2020 2020 2066 696c 6c2d 7275           fill-ru
+0000de20: 6c65 3a20 6e6f 6e7a 6572 6f3b 0a20 2020  le: nonzero;.   
+0000de30: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000de40: 2020 2020 2020 2020 2073 7472 6f6b 653a           stroke:
+0000de50: 2024 6f72 625f 636f 6c6f 725f 3330 3b0a   $orb_color_30;.
+0000de60: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000de70: 2020 2020 2020 2020 2020 2020 7374 726f              stro
+0000de80: 6b65 2d77 6964 7468 3a20 312e 3437 3633  ke-width: 1.4763
+0000de90: 3330 3634 3b0a 2020 2020 2020 2020 2020  3064;.          
+0000dea0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000deb0: 2020 7374 726f 6b65 2d6c 696e 6563 6170    stroke-linecap
+0000dec0: 3a20 6275 7474 3b0a 2020 2020 2020 2020  : butt;.        
+0000ded0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000dee0: 2020 2020 7374 726f 6b65 2d6c 696e 656a      stroke-linej
+0000def0: 6f69 6e3a 206d 6974 6572 3b0a 2020 2020  oin: miter;.    
+0000df00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000df10: 2020 2020 2020 2020 7374 726f 6b65 2d6d          stroke-m
+0000df20: 6974 6572 6c69 6d69 743a 2034 3b0a 2020  iterlimit: 4;.  
+0000df30: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000df40: 2020 2020 2020 2020 2020 7374 726f 6b65            stroke
+0000df50: 2d64 6173 6861 7272 6179 3a20 6e6f 6e65  -dasharray: none
+0000df60: 3b0a 2020 2020 2020 2020 2020 2020 2020  ;.              
+0000df70: 2020 2020 2020 2020 2020 2020 2020 7374                st
+0000df80: 726f 6b65 2d6f 7061 6369 7479 3a20 313b  roke-opacity: 1;
+0000df90: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+0000dfa0: 2020 2020 2020 2020 2022 0a20 2020 2020           ".     
+0000dfb0: 2020 2020 2020 2020 2020 2020 2020 202f                 /
+0000dfc0: 3e0a 2020 2020 2020 2020 2020 2020 2020  >.              
+0000dfd0: 2020 3c2f 7379 6d62 6f6c 3e0a 2020 2020    </symbol>.    
+0000dfe0: 2020 2020 2020 2020 2020 2020 3c73 796d              <sym
+0000dff0: 626f 6c20 6964 3d22 6f72 6234 3522 3e0a  bol id="orb45">.
+0000e000: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e010: 2020 2020 3c70 6174 680a 2020 2020 2020      <path.      
+0000e020: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e030: 2020 643d 224d 2039 2e38 3130 3031 3738    d="M 9.8100178
+0000e040: 2c39 2e35 3932 3139 3636 2043 2036 2e39  ,9.5921966 C 6.9
+0000e050: 3634 3036 3538 2c39 2e35 3932 3139 3536  640658,9.5921956
+0000e060: 2034 2e31 3138 3131 3235 2c39 2e35 3932   4.1181125,9.592
+0000e070: 3139 3636 2031 2e32 3732 3136 2c39 2e35  1966 1.27216,9.5
+0000e080: 3932 3139 3636 2043 2032 2e36 3935 3133  921966 C 2.69513
+0000e090: 3632 2c36 2e37 3436 3234 3431 2034 2e31  62,6.7462441 4.1
+0000e0a0: 3138 3131 3235 2c33 2e39 3030 3239 3035  181125,3.9002905
+0000e0b0: 2035 2e35 3431 3038 3838 2c31 2e30 3534   5.5410888,1.054
+0000e0c0: 3333 3739 220a 2020 2020 2020 2020 2020  3379".          
+0000e0d0: 2020 2020 2020 2020 2020 2020 2020 7374                st
+0000e0e0: 796c 653d 220a 2020 2020 2020 2020 2020  yle=".          
+0000e0f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e100: 2020 6f70 6163 6974 793a 2031 3b0a 2020    opacity: 1;.  
+0000e110: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e120: 2020 2020 2020 2020 2020 6669 6c6c 3a20            fill: 
+0000e130: 6e6f 6e65 3b0a 2020 2020 2020 2020 2020  none;.          
+0000e140: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e150: 2020 6669 6c6c 2d6f 7061 6369 7479 3a20    fill-opacity: 
+0000e160: 313b 0a20 2020 2020 2020 2020 2020 2020  1;.             
+0000e170: 2020 2020 2020 2020 2020 2020 2020 2066                 f
+0000e180: 696c 6c2d 7275 6c65 3a20 6e6f 6e7a 6572  ill-rule: nonzer
+0000e190: 6f3b 0a20 2020 2020 2020 2020 2020 2020  o;.             
+0000e1a0: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+0000e1b0: 7472 6f6b 653a 2024 6f72 625f 636f 6c6f  troke: $orb_colo
+0000e1c0: 725f 3435 3b0a 2020 2020 2020 2020 2020  r_45;.          
+0000e1d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e1e0: 2020 7374 726f 6b65 2d77 6964 7468 3a20    stroke-width: 
+0000e1f0: 312e 3437 3633 3330 3634 3b0a 2020 2020  1.47633064;.    
+0000e200: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e210: 2020 2020 2020 2020 7374 726f 6b65 2d6c          stroke-l
+0000e220: 696e 6563 6170 3a20 6275 7474 3b0a 2020  inecap: butt;.  
+0000e230: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e240: 2020 2020 2020 2020 2020 7374 726f 6b65            stroke
+0000e250: 2d6c 696e 656a 6f69 6e3a 206d 6974 6572  -linejoin: miter
+0000e260: 3b0a 2020 2020 2020 2020 2020 2020 2020  ;.              
+0000e270: 2020 2020 2020 2020 2020 2020 2020 7374                st
+0000e280: 726f 6b65 2d6d 6974 6572 6c69 6d69 743a  roke-miterlimit:
+0000e290: 2034 3b0a 2020 2020 2020 2020 2020 2020   4;.            
+0000e2a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e2b0: 7374 726f 6b65 2d64 6173 6861 7272 6179  stroke-dasharray
+0000e2c0: 3a20 6e6f 6e65 3b0a 2020 2020 2020 2020  : none;.        
+0000e2d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e2e0: 2020 2020 7374 726f 6b65 2d6f 7061 6369      stroke-opaci
+0000e2f0: 7479 3a20 313b 0a20 2020 2020 2020 2020  ty: 1;.         
+0000e300: 2020 2020 2020 2020 2020 2020 2020 2022                 "
+0000e310: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+0000e320: 2020 2020 202f 3e0a 2020 2020 2020 2020       />.        
+0000e330: 2020 2020 2020 2020 3c2f 7379 6d62 6f6c          </symbol
+0000e340: 3e0a 2020 2020 2020 2020 2020 2020 2020  >.              
+0000e350: 2020 3c73 796d 626f 6c20 6964 3d22 6f72    <symbol id="or
+0000e360: 6236 3022 3e0a 2020 2020 2020 2020 2020  b60">.          
+0000e370: 2020 2020 2020 2020 2020 3c70 6174 680a            <path.
+0000e380: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e390: 2020 2020 2020 2020 643d 224d 2030 2e38          d="M 0.8
+0000e3a0: 3831 3832 3434 312c 302e 3731 3831 3437  8182441,0.718147
+0000e3b0: 3635 2043 2033 2e33 3830 3638 3732 2c33  65 C 3.3806872,3
+0000e3c0: 2e32 3137 3630 3037 2035 2e38 3739 3535  .2176007 5.87955
+0000e3d0: 3032 2c35 2e37 3137 3035 3237 2038 2e33  02,5.7170527 8.3
+0000e3e0: 3738 3431 3332 2c38 2e32 3136 3530 3537  784132,8.2165057
+0000e3f0: 204d 2038 2e36 3131 3933 3632 2c34 2e34   M 8.6119362,4.4
+0000e400: 3033 3635 3537 2043 2035 2e39 3634 3034  036557 C 5.96404
+0000e410: 3432 2c34 2e34 3033 3635 3537 2033 2e33  42,4.4036557 3.3
+0000e420: 3136 3135 3334 2c34 2e34 3033 3635 3537  161534,4.4036557
+0000e430: 2030 2e36 3638 3236 3232 312c 342e 3430   0.66826221,4.40
+0000e440: 3336 3535 3720 4d20 302e 3834 3932 3537  36557 M 0.849257
+0000e450: 3831 2c38 2e31 3934 3439 3737 2043 2033  81,8.1944977 C 3
+0000e460: 2e33 3736 3438 3532 2c35 2e37 3232 3433  .3764852,5.72243
+0000e470: 3337 2035 2e39 3033 3731 3332 2c33 2e32  37 5.9037132,3.2
+0000e480: 3530 3337 3037 2038 2e34 3330 3934 3032  503707 8.4309402
+0000e490: 2c30 2e37 3738 3330 3736 3522 0a20 2020  ,0.77830765".   
+0000e4a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e4b0: 2020 2020 2073 7479 6c65 3d22 0a20 2020       style=".   
+0000e4c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e4d0: 2020 2020 2020 2020 206f 7061 6369 7479           opacity
+0000e4e0: 3a20 313b 0a20 2020 2020 2020 2020 2020  : 1;.           
+0000e4f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e500: 2066 696c 6c3a 206e 6f6e 653b 0a20 2020   fill: none;.   
+0000e510: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e520: 2020 2020 2020 2020 2066 696c 6c2d 6f70           fill-op
+0000e530: 6163 6974 793a 2031 3b0a 2020 2020 2020  acity: 1;.      
+0000e540: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e550: 2020 2020 2020 6669 6c6c 2d72 756c 653a        fill-rule:
+0000e560: 206e 6f6e 7a65 726f 3b0a 2020 2020 2020   nonzero;.      
+0000e570: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e580: 2020 2020 2020 7374 726f 6b65 3a20 246f        stroke: $o
+0000e590: 7262 5f63 6f6c 6f72 5f36 303b 0a20 2020  rb_color_60;.   
+0000e5a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e5b0: 2020 2020 2020 2020 2073 7472 6f6b 652d           stroke-
+0000e5c0: 7769 6474 683a 2031 2e34 3736 3333 3036  width: 1.4763306
+0000e5d0: 343b 0a20 2020 2020 2020 2020 2020 2020  4;.             
+0000e5e0: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+0000e5f0: 7472 6f6b 652d 6c69 6e65 6361 703a 2062  troke-linecap: b
+0000e600: 7574 743b 0a20 2020 2020 2020 2020 2020  utt;.           
+0000e610: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e620: 2073 7472 6f6b 652d 6c69 6e65 6a6f 696e   stroke-linejoin
+0000e630: 3a20 6d69 7465 723b 0a20 2020 2020 2020  : miter;.       
+0000e640: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e650: 2020 2020 2073 7472 6f6b 652d 6d69 7465       stroke-mite
+0000e660: 726c 696d 6974 3a20 343b 0a20 2020 2020  rlimit: 4;.     
+0000e670: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e680: 2020 2020 2020 2073 7472 6f6b 652d 6461         stroke-da
+0000e690: 7368 6172 7261 793a 206e 6f6e 653b 0a20  sharray: none;. 
+0000e6a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e6b0: 2020 2020 2020 2020 2020 2073 7472 6f6b             strok
+0000e6c0: 652d 6f70 6163 6974 793a 2031 3b0a 2020  e-opacity: 1;.  
+0000e6d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e6e0: 2020 2020 2020 220a 2020 2020 2020 2020        ".        
+0000e6f0: 2020 2020 2020 2020 2020 2020 2f3e 0a20              />. 
+0000e700: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+0000e710: 2f73 796d 626f 6c3e 0a20 2020 2020 2020  /symbol>.       
+0000e720: 2020 2020 2020 2020 203c 7379 6d62 6f6c           <symbol
+0000e730: 2069 643d 226f 7262 3732 223e 0a20 2020   id="orb72">.   
+0000e740: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e750: 203c 7061 7468 0a20 2020 2020 2020 2020   <path.         
+0000e760: 2020 2020 2020 2020 2020 2020 2020 2064                 d
+0000e770: 3d22 4d20 382e 3931 3635 3034 342c 352e  ="M 8.9165044,5.
+0000e780: 3634 3137 3433 3820 4320 382e 3931 3635  6417438 C 8.9165
+0000e790: 3034 342c 372e 3936 3837 3636 3320 372e  044,7.9687663 7.
+0000e7a0: 3237 3432 3834 342c 392e 3835 3531 3839  2742844,9.855189
+0000e7b0: 3320 352e 3234 3835 3033 342c 392e 3835  3 5.2485034,9.85
+0000e7c0: 3531 3839 3320 4320 332e 3232 3237 3232  51893 C 3.222722
+0000e7d0: 342c 392e 3835 3531 3839 3320 312e 3538  4,9.8551893 1.58
+0000e7e0: 3035 3032 372c 372e 3936 3837 3636 3320  05027,7.9687663 
+0000e7f0: 312e 3538 3035 3032 372c 352e 3634 3137  1.5805027,5.6417
+0000e800: 3433 3820 4320 312e 3538 3035 3032 372c  438 C 1.5805027,
+0000e810: 332e 3331 3437 3230 3820 332e 3232 3237  3.3147208 3.2227
+0000e820: 3232 342c 312e 3432 3832 3936 3720 352e  224,1.4282967 5.
+0000e830: 3234 3835 3033 342c 312e 3432 3832 3936  2485034,1.428296
+0000e840: 3720 4320 372e 3237 3432 3834 342c 312e  7 C 7.2742844,1.
+0000e850: 3432 3832 3936 3720 382e 3931 3635 3034  4282967 8.916504
+0000e860: 342c 332e 3331 3437 3230 3820 382e 3931  4,3.3147208 8.91
+0000e870: 3635 3034 342c 352e 3634 3137 3433 3820  65044,5.6417438 
+0000e880: 4c20 382e 3931 3635 3034 342c 352e 3634  L 8.9165044,5.64
+0000e890: 3137 3433 3820 7a20 4d20 352e 3437 3032  17438 z M 5.4702
+0000e8a0: 3633 342c 362e 3734 3633 3335 3820 4320  634,6.7463358 C 
+0000e8b0: 392e 3035 3131 3830 342c 3130 2e31 3139  9.0511804,10.119
+0000e8c0: 3232 3820 392e 3035 3131 3830 342c 3130  228 9.0511804,10
+0000e8d0: 2e31 3139 3232 3820 392e 3035 3131 3830  .119228 9.051180
+0000e8e0: 342c 3130 2e31 3139 3232 3822 0a20 2020  4,10.119228".   
+0000e8f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e900: 2020 2020 2073 7479 6c65 3d22 0a20 2020       style=".   
+0000e910: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e920: 2020 2020 2020 2020 206f 7061 6369 7479           opacity
+0000e930: 3a20 313b 0a20 2020 2020 2020 2020 2020  : 1;.           
+0000e940: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e950: 2066 696c 6c3a 206e 6f6e 653b 0a20 2020   fill: none;.   
+0000e960: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e970: 2020 2020 2020 2020 2066 696c 6c2d 6f70           fill-op
+0000e980: 6163 6974 793a 2031 3b0a 2020 2020 2020  acity: 1;.      
+0000e990: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e9a0: 2020 2020 2020 6669 6c6c 2d72 756c 653a        fill-rule:
+0000e9b0: 206e 6f6e 7a65 726f 3b0a 2020 2020 2020   nonzero;.      
+0000e9c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000e9d0: 2020 2020 2020 7374 726f 6b65 3a20 246f        stroke: $o
+0000e9e0: 7262 5f63 6f6c 6f72 5f37 323b 0a20 2020  rb_color_72;.   
+0000e9f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ea00: 2020 2020 2020 2020 2073 7472 6f6b 652d           stroke-
+0000ea10: 7769 6474 683a 2031 2e34 3736 3333 3036  width: 1.4763306
+0000ea20: 343b 0a20 2020 2020 2020 2020 2020 2020  4;.             
+0000ea30: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+0000ea40: 7472 6f6b 652d 6c69 6e65 6361 703a 2062  troke-linecap: b
+0000ea50: 7574 743b 0a20 2020 2020 2020 2020 2020  utt;.           
+0000ea60: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ea70: 2073 7472 6f6b 652d 6c69 6e65 6a6f 696e   stroke-linejoin
+0000ea80: 3a20 6d69 7465 723b 0a20 2020 2020 2020  : miter;.       
+0000ea90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000eaa0: 2020 2020 2073 7472 6f6b 652d 6d69 7465       stroke-mite
+0000eab0: 726c 696d 6974 3a20 343b 0a20 2020 2020  rlimit: 4;.     
+0000eac0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ead0: 2020 2020 2020 2073 7472 6f6b 652d 6461         stroke-da
+0000eae0: 7368 6172 7261 793a 206e 6f6e 653b 0a20  sharray: none;. 
+0000eaf0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000eb00: 2020 2020 2020 2020 2020 2073 7472 6f6b             strok
+0000eb10: 652d 6f70 6163 6974 793a 2031 3b0a 2020  e-opacity: 1;.  
+0000eb20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000eb30: 2020 2020 2020 220a 2020 2020 2020 2020        ".        
+0000eb40: 2020 2020 2020 2020 2020 2020 2f3e 0a20              />. 
+0000eb50: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+0000eb60: 2f73 796d 626f 6c3e 0a20 2020 2020 2020  /symbol>.       
+0000eb70: 2020 2020 2020 2020 203c 7379 6d62 6f6c           <symbol
+0000eb80: 2069 643d 226f 7262 3930 223e 0a20 2020   id="orb90">.   
+0000eb90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000eba0: 203c 7265 6374 0a20 2020 2020 2020 2020   <rect.         
+0000ebb0: 2020 2020 2020 2020 2020 2020 2020 2068                 h
+0000ebc0: 6569 6768 743d 2238 2e30 3836 3139 3522  eight="8.086195"
+0000ebd0: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+0000ebe0: 2020 2020 2020 2020 2077 6964 7468 3d22           width="
+0000ebf0: 382e 3731 3538 3133 3622 0a20 2020 2020  8.7158136".     
+0000ec00: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ec10: 2020 2078 3d22 312e 3138 3331 3832 3622     x="1.1831826"
+0000ec20: 0a20 2020 2020 2020 2020 2020 2020 2020  .               
+0000ec30: 2020 2020 2020 2020 2079 3d22 312e 3138           y="1.18
+0000ec40: 3932 3534 3522 0a20 2020 2020 2020 2020  92545".         
+0000ec50: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+0000ec60: 7479 6c65 3d22 0a20 2020 2020 2020 2020  tyle=".         
+0000ec70: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ec80: 2020 206f 7061 6369 7479 3a20 313b 0a20     opacity: 1;. 
+0000ec90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000eca0: 2020 2020 2020 2020 2020 2066 696c 6c3a             fill:
+0000ecb0: 206e 6f6e 653b 0a20 2020 2020 2020 2020   none;.         
+0000ecc0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ecd0: 2020 2066 696c 6c2d 6f70 6163 6974 793a     fill-opacity:
+0000ece0: 2031 3b0a 2020 2020 2020 2020 2020 2020   1;.            
+0000ecf0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ed00: 6669 6c6c 2d72 756c 653a 206e 6f6e 7a65  fill-rule: nonze
+0000ed10: 726f 3b0a 2020 2020 2020 2020 2020 2020  ro;.            
+0000ed20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ed30: 7374 726f 6b65 3a20 246f 7262 5f63 6f6c  stroke: $orb_col
+0000ed40: 6f72 5f39 303b 0a20 2020 2020 2020 2020  or_90;.         
+0000ed50: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ed60: 2020 2073 7472 6f6b 652d 7769 6474 683a     stroke-width:
+0000ed70: 2031 2e32 3530 3339 3531 383b 0a20 2020   1.25039518;.   
+0000ed80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ed90: 2020 2020 2020 2020 2073 7472 6f6b 652d           stroke-
+0000eda0: 6c69 6e65 6361 703a 2062 7574 743b 0a20  linecap: butt;. 
+0000edb0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000edc0: 2020 2020 2020 2020 2020 2073 7472 6f6b             strok
+0000edd0: 652d 6c69 6e65 6a6f 696e 3a20 6d69 7465  e-linejoin: mite
+0000ede0: 723b 0a20 2020 2020 2020 2020 2020 2020  r;.             
+0000edf0: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+0000ee00: 7472 6f6b 652d 6d69 7465 726c 696d 6974  troke-miterlimit
+0000ee10: 3a20 343b 0a20 2020 2020 2020 2020 2020  : 4;.           
+0000ee20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ee30: 2073 7472 6f6b 652d 6461 7368 6172 7261   stroke-dasharra
+0000ee40: 793a 206e 6f6e 653b 0a20 2020 2020 2020  y: none;.       
+0000ee50: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ee60: 2020 2020 2073 7472 6f6b 652d 6f70 6163       stroke-opac
+0000ee70: 6974 793a 2031 3b0a 2020 2020 2020 2020  ity: 1;.        
+0000ee80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000ee90: 220a 2020 2020 2020 2020 2020 2020 2020  ".              
+0000eea0: 2020 2020 2020 2f3e 0a20 2020 2020 2020        />.       
+0000eeb0: 2020 2020 2020 2020 203c 2f73 796d 626f           </symbo
+0000eec0: 6c3e 0a20 2020 2020 2020 2020 2020 2020  l>.             
+0000eed0: 2020 203c 7379 6d62 6f6c 2069 643d 226f     <symbol id="o
+0000eee0: 7262 3132 3022 3e0a 2020 2020 2020 2020  rb120">.        
+0000eef0: 2020 2020 2020 2020 2020 2020 3c70 6174              <pat
+0000ef00: 680a 2020 2020 2020 2020 2020 2020 2020  h.              
+0000ef10: 2020 2020 2020 2020 2020 643d 224d 2031            d="M 1
+0000ef20: 2e31 3735 3530 3131 2c39 2e34 3937 3937  .1755011,9.49797
+0000ef30: 3320 4320 392e 3039 3537 3836 392c 392e  3 C 9.0957869,9.
+0000ef40: 3439 3739 3733 2039 2e30 3935 3738 3639  497973 9.0957869
+0000ef50: 2c39 2e34 3937 3937 3320 392e 3039 3537  ,9.497973 9.0957
+0000ef60: 3836 392c 392e 3439 3739 3733 204c 2035  869,9.497973 L 5
+0000ef70: 2e31 3335 3634 3338 2c31 2e34 3633 3930  .1356438,1.46390
+0000ef80: 3633 2043 2035 2e31 3335 3634 3338 2c31  63 C 5.1356438,1
+0000ef90: 2e34 3633 3930 3633 2035 2e31 3335 3634  .4639063 5.13564
+0000efa0: 3338 2c31 2e34 3633 3930 3633 2031 2e31  38,1.4639063 1.1
+0000efb0: 3735 3530 3131 2c39 2e34 3937 3937 3320  755011,9.497973 
+0000efc0: 7a22 0a20 2020 2020 2020 2020 2020 2020  z".             
+0000efd0: 2020 2020 2020 2020 2020 2073 7479 6c65             style
+0000efe0: 3d22 0a20 2020 2020 2020 2020 2020 2020  =".             
+0000eff0: 2020 2020 2020 2020 2020 2020 2020 2066                 f
+0000f000: 696c 6c3a 206e 6f6e 653b 0a20 2020 2020  ill: none;.     
+0000f010: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f020: 2020 2020 2020 2066 696c 6c2d 7275 6c65         fill-rule
+0000f030: 3a20 6576 656e 6f64 643b 0a20 2020 2020  : evenodd;.     
+0000f040: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f050: 2020 2020 2020 2073 7472 6f6b 653a 2024         stroke: $
+0000f060: 6f72 625f 636f 6c6f 725f 3132 303b 0a20  orb_color_120;. 
+0000f070: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f080: 2020 2020 2020 2020 2020 2073 7472 6f6b             strok
+0000f090: 652d 7769 6474 683a 2031 2e31 3936 3534  e-width: 1.19654
+0000f0a0: 3632 3b0a 2020 2020 2020 2020 2020 2020  62;.            
+0000f0b0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f0c0: 7374 726f 6b65 2d6c 696e 6563 6170 3a20  stroke-linecap: 
+0000f0d0: 6275 7474 3b0a 2020 2020 2020 2020 2020  butt;.          
+0000f0e0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f0f0: 2020 7374 726f 6b65 2d6c 696e 656a 6f69    stroke-linejoi
+0000f100: 6e3a 206d 6974 6572 3b0a 2020 2020 2020  n: miter;.      
+0000f110: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f120: 2020 2020 2020 7374 726f 6b65 2d6d 6974        stroke-mit
+0000f130: 6572 6c69 6d69 743a 2034 3b0a 2020 2020  erlimit: 4;.    
+0000f140: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f150: 2020 2020 2020 2020 7374 726f 6b65 2d64          stroke-d
+0000f160: 6173 6861 7272 6179 3a20 6e6f 6e65 3b0a  asharray: none;.
+0000f170: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f180: 2020 2020 2020 2020 2020 2020 7374 726f              stro
+0000f190: 6b65 2d6f 7061 6369 7479 3a20 313b 0a20  ke-opacity: 1;. 
+0000f1a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f1b0: 2020 2020 2020 2022 0a20 2020 2020 2020         ".       
+0000f1c0: 2020 2020 2020 2020 2020 2020 202f 3e0a               />.
+0000f1d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f1e0: 3c2f 7379 6d62 6f6c 3e0a 2020 2020 2020  </symbol>.      
+0000f1f0: 2020 2020 2020 2020 2020 3c73 796d 626f            <symbo
+0000f200: 6c20 6964 3d22 6f72 6231 3335 223e 0a20  l id="orb135">. 
+0000f210: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f220: 2020 203c 7061 7468 0a20 2020 2020 2020     <path.       
+0000f230: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f240: 2064 3d22 4d20 322e 3233 3838 3538 322c   d="M 2.2388582,
+0000f250: 312e 3731 3536 3939 3420 4c20 392e 3239  1.7156994 L 9.29
+0000f260: 3338 3135 342c 312e 3731 3536 3939 3420  38154,1.7156994 
+0000f270: 4c20 392e 3239 3338 3135 342c 372e 3738  L 9.2938154,7.78
+0000f280: 3131 3832 3720 4c20 322e 3233 3838 3538  11827 L 2.238858
+0000f290: 322c 372e 3738 3131 3832 3720 4c20 322e  2,7.7811827 L 2.
+0000f2a0: 3233 3838 3538 322c 312e 3731 3536 3939  2388582,1.715699
+0000f2b0: 3420 7a20 4d20 362e 3834 3631 3130 342c  4 z M 6.8461104,
+0000f2c0: 352e 3537 3334 3236 3720 4320 362e 3834  5.5734267 C 6.84
+0000f2d0: 3631 3130 342c 352e 3537 3334 3236 3720  61104,5.5734267 
+0000f2e0: 362e 3834 3631 3130 342c 352e 3537 3334  6.8461104,5.5734
+0000f2f0: 3236 3720 332e 3234 3638 3635 322c 3130  267 3.2468652,10
+0000f300: 2e33 3732 3432 2043 2038 2e30 3435 3835  .37242 C 8.04585
+0000f310: 3834 2c31 302e 3337 3234 3220 382e 3034  84,10.37242 8.04
+0000f320: 3538 3538 342c 3130 2e33 3732 3432 2038  58584,10.37242 8
+0000f330: 2e30 3435 3835 3834 2c31 302e 3337 3234  .0458584,10.3724
+0000f340: 3222 0a20 2020 2020 2020 2020 2020 2020  2".             
+0000f350: 2020 2020 2020 2020 2020 2073 7479 6c65             style
+0000f360: 3d22 0a20 2020 2020 2020 2020 2020 2020  =".             
+0000f370: 2020 2020 2020 2020 2020 2020 2020 2066                 f
+0000f380: 696c 6c3a 206e 6f6e 653b 0a20 2020 2020  ill: none;.     
+0000f390: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f3a0: 2020 2020 2020 2066 696c 6c2d 7275 6c65         fill-rule
+0000f3b0: 3a20 6576 656e 6f64 643b 0a20 2020 2020  : evenodd;.     
+0000f3c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f3d0: 2020 2020 2020 2073 7472 6f6b 653a 2024         stroke: $
+0000f3e0: 6f72 625f 636f 6c6f 725f 3133 353b 0a20  orb_color_135;. 
+0000f3f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f400: 2020 2020 2020 2020 2020 2073 7472 6f6b             strok
+0000f410: 652d 7769 6474 683a 2031 2e31 3936 3534  e-width: 1.19654
+0000f420: 3632 3b0a 2020 2020 2020 2020 2020 2020  62;.            
+0000f430: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f440: 7374 726f 6b65 2d6c 696e 6563 6170 3a20  stroke-linecap: 
+0000f450: 6275 7474 3b0a 2020 2020 2020 2020 2020  butt;.          
+0000f460: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f470: 2020 7374 726f 6b65 2d6c 696e 656a 6f69    stroke-linejoi
+0000f480: 6e3a 206d 6974 6572 3b0a 2020 2020 2020  n: miter;.      
+0000f490: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f4a0: 2020 2020 2020 7374 726f 6b65 2d6d 6974        stroke-mit
+0000f4b0: 6572 6c69 6d69 743a 2034 3b0a 2020 2020  erlimit: 4;.    
+0000f4c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f4d0: 2020 2020 2020 2020 7374 726f 6b65 2d64          stroke-d
+0000f4e0: 6173 6861 7272 6179 3a20 6e6f 6e65 3b0a  asharray: none;.
+0000f4f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f500: 2020 2020 2020 2020 2020 2020 7374 726f              stro
+0000f510: 6b65 2d6f 7061 6369 7479 3a20 313b 0a20  ke-opacity: 1;. 
+0000f520: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f530: 2020 2020 2020 2022 0a20 2020 2020 2020         ".       
+0000f540: 2020 2020 2020 2020 2020 2020 202f 3e0a               />.
+0000f550: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f560: 3c2f 7379 6d62 6f6c 3e0a 2020 2020 2020  </symbol>.      
+0000f570: 2020 2020 2020 2020 2020 3c73 796d 626f            <symbo
+0000f580: 6c20 6964 3d22 6f72 6231 3434 223e 0a20  l id="orb144">. 
+0000f590: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f5a0: 2020 203c 7061 7468 0a20 2020 2020 2020     <path.       
+0000f5b0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f5c0: 2064 3d22 4d20 312e 3432 3435 3136 392c   d="M 1.4245169,
+0000f5d0: 312e 3239 3638 3539 3820 4320 312e 3432  1.2968598 C 1.42
+0000f5e0: 3435 3136 392c 392e 3637 3633 3132 3920  45169,9.6763129 
+0000f5f0: 312e 3432 3435 3136 392c 392e 3637 3633  1.4245169,9.6763
+0000f600: 3132 3920 312e 3432 3435 3136 392c 392e  129 1.4245169,9.
+0000f610: 3637 3633 3132 3920 4d20 312e 3932 3038  6763129 M 1.9208
+0000f620: 3333 312c 352e 3338 3638 3237 3920 4320  331,5.3868279 C 
+0000f630: 322e 3737 3232 3838 362c 352e 3333 3532  2.7722886,5.3352
+0000f640: 3433 3920 332e 3535 3431 3535 332c 352e  439 3.5541553,5.
+0000f650: 3638 3634 3132 3920 332e 3933 3635 3233  6864129 3.936523
+0000f660: 372c 362e 3239 3231 3536 3920 4320 342e  7,6.2921569 C 4.
+0000f670: 3331 3838 3932 2c36 2e38 3937 3930 3039  318892,6.8979009
+0000f680: 2034 2e32 3335 3136 3134 2c37 2e36 3532   4.2351614,7.652
+0000f690: 3731 3239 2033 2e37 3230 3636 3232 2c38  7129 3.7206622,8
+0000f6a0: 2e32 3338 3039 3839 2043 2033 2e32 3036  .2380989 C 3.206
+0000f6b0: 3136 3332 2c38 2e38 3233 3438 3439 2032  1632,8.8234849 2
+0000f6c0: 2e33 3530 3531 3031 2c39 2e31 3337 3438  .3505101,9.13748
+0000f6d0: 3239 2031 2e35 3134 3734 3731 2c39 2e30  29 1.5147471,9.0
+0000f6e0: 3437 3630 3139 204d 2039 2e38 3532 3836  476019 M 9.85286
+0000f6f0: 3339 2c35 2e35 3835 3132 3439 2043 2039  39,5.5851249 C 9
+0000f700: 2e38 3533 3034 3439 2c37 2e34 3739 3334  .8530449,7.47934
+0000f710: 3139 2038 2e38 3634 3936 3939 2c39 2e30  19 8.8649699,9.0
+0000f720: 3135 3035 3739 2037 2e36 3436 3035 3339  150579 7.6460539
+0000f730: 2c39 2e30 3135 3035 3739 2043 2036 2e34  ,9.0150579 C 6.4
+0000f740: 3237 3133 3839 2c39 2e30 3135 3035 3739  271389,9.0150579
+0000f750: 2035 2e34 3339 3036 3239 2c37 2e34 3739   5.4390629,7.479
+0000f760: 3334 3139 2035 2e34 3339 3234 3439 2c35  3419 5.4392449,5
+0000f770: 2e35 3835 3132 3439 2043 2035 2e34 3339  .5851249 C 5.439
+0000f780: 3036 3239 2c33 2e36 3930 3930 3838 2036  0629,3.6909088 6
+0000f790: 2e34 3237 3133 3839 2c32 2e31 3535 3139  .4271389,2.15519
+0000f7a0: 3238 2037 2e36 3436 3035 3339 2c32 2e31  28 7.6460539,2.1
+0000f7b0: 3535 3139 3238 2043 2038 2e38 3634 3936  551928 C 8.86496
+0000f7c0: 3939 2c32 2e31 3535 3139 3238 2039 2e38  99,2.1551928 9.8
+0000f7d0: 3533 3034 3439 2c33 2e36 3930 3930 3838  530449,3.6909088
+0000f7e0: 2039 2e38 3532 3836 3339 2c35 2e35 3835   9.8528639,5.585
+0000f7f0: 3132 3439 207a 204d 2038 2e32 3538 3034  1249 z M 8.25804
+0000f800: 3439 2c37 2e32 3632 3739 3539 2043 2031  49,7.2627959 C 1
+0000f810: 302e 3139 3832 3536 2c39 2e39 3830 3336  0.198256,9.98036
+0000f820: 3739 2031 302e 3139 3832 3536 2c39 2e39  79 10.198256,9.9
+0000f830: 3830 3336 3739 2031 302e 3139 3832 3536  803679 10.198256
+0000f840: 2c39 2e39 3830 3336 3739 220a 2020 2020  ,9.9803679".    
+0000f850: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f860: 2020 2020 7374 796c 653d 220a 2020 2020      style=".    
+0000f870: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f880: 2020 2020 2020 2020 6f70 6163 6974 793a          opacity:
+0000f890: 2031 3b0a 2020 2020 2020 2020 2020 2020   1;.            
+0000f8a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f8b0: 6669 6c6c 3a20 6e6f 6e65 3b0a 2020 2020  fill: none;.    
+0000f8c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f8d0: 2020 2020 2020 2020 6669 6c6c 2d6f 7061          fill-opa
+0000f8e0: 6369 7479 3a20 313b 0a20 2020 2020 2020  city: 1;.       
+0000f8f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f900: 2020 2020 2066 696c 6c2d 7275 6c65 3a20       fill-rule: 
+0000f910: 6e6f 6e7a 6572 6f3b 0a20 2020 2020 2020  nonzero;.       
+0000f920: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f930: 2020 2020 2073 7472 6f6b 653a 2024 6f72       stroke: $or
+0000f940: 625f 636f 6c6f 725f 3134 343b 0a20 2020  b_color_144;.   
+0000f950: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f960: 2020 2020 2020 2020 2073 7472 6f6b 652d           stroke-
+0000f970: 7769 6474 683a 2031 2e34 3736 3333 3036  width: 1.4763306
+0000f980: 343b 0a20 2020 2020 2020 2020 2020 2020  4;.             
+0000f990: 2020 2020 2020 2020 2020 2020 2020 2073                 s
+0000f9a0: 7472 6f6b 652d 6c69 6e65 6361 703a 2062  troke-linecap: b
+0000f9b0: 7574 743b 0a20 2020 2020 2020 2020 2020  utt;.           
+0000f9c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000f9d0: 2073 7472 6f6b 652d 6c69 6e65 6a6f 696e   stroke-linejoin
+0000f9e0: 3a20 6d69 7465 723b 0a20 2020 2020 2020  : miter;.       
+0000f9f0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fa00: 2020 2020 2073 7472 6f6b 652d 6d69 7465       stroke-mite
+0000fa10: 726c 696d 6974 3a20 343b 0a20 2020 2020  rlimit: 4;.     
+0000fa20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fa30: 2020 2020 2020 2073 7472 6f6b 652d 6461         stroke-da
+0000fa40: 7368 6172 7261 793a 206e 6f6e 653b 0a20  sharray: none;. 
+0000fa50: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fa60: 2020 2020 2020 2020 2020 2073 7472 6f6b             strok
+0000fa70: 652d 6f70 6163 6974 793a 2031 3b0a 2020  e-opacity: 1;.  
+0000fa80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fa90: 2020 2020 2020 220a 2020 2020 2020 2020        ".        
+0000faa0: 2020 2020 2020 2020 2020 2020 2f3e 0a20              />. 
+0000fab0: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+0000fac0: 2f73 796d 626f 6c3e 0a20 2020 2020 2020  /symbol>.       
+0000fad0: 2020 2020 2020 2020 203c 7379 6d62 6f6c           <symbol
+0000fae0: 2069 643d 226f 7262 3135 3022 3e0a 2020   id="orb150">.  
+0000faf0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fb00: 2020 3c70 6174 680a 2020 2020 2020 2020    <path.        
+0000fb10: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fb20: 643d 224d 2031 2e31 3737 3134 3736 2c33  d="M 1.1771476,3
+0000fb30: 2e38 3336 3535 3232 2043 2034 2e36 3837  .8365522 C 4.687
+0000fb40: 3130 322c 332e 3832 3732 3933 3620 382e  102,3.8272936 8.
+0000fb50: 3139 3730 3536 322c 332e 3831 3830 3335  1970562,3.818035
+0000fb60: 3320 3131 2e37 3037 3031 312c 332e 3830  3 11.707011,3.80
+0000fb70: 3837 3736 3720 4d20 3130 2e39 3732 3537  87767 M 10.97257
+0000fb80: 392c 392e 3231 3038 3334 3120 4320 392e  9,9.2108341 C 9.
+0000fb90: 3333 3938 3030 322c 372e 3439 3634 3136  3398002,7.496416
+0000fba0: 3120 372e 3730 3730 3232 322c 352e 3738  1 7.7070222,5.78
+0000fbb0: 3139 3938 3920 362e 3037 3432 3433 342c  19989 6.0742434,
+0000fbc0: 342e 3036 3735 3831 3320 4d20 312e 3636  4.0675813 M 1.66
+0000fbd0: 3537 3431 2c39 2e32 3130 3833 3431 2043  5741,9.2108341 C
+0000fbe0: 2033 2e31 3930 3836 3536 2c37 2e33 3939   3.1908656,7.399
+0000fbf0: 3938 3131 2034 2e37 3135 3939 3034 2c35  9811 4.7159904,5
+0000fc00: 2e35 3839 3132 3739 2036 2e32 3431 3131  .5891279 6.24111
+0000fc10: 352c 332e 3737 3832 3734 3822 0a20 2020  5,3.7782748".   
+0000fc20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fc30: 2020 2020 2073 7479 6c65 3d22 0a20 2020       style=".   
+0000fc40: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fc50: 2020 2020 2020 2020 206f 7061 6369 7479           opacity
+0000fc60: 3a20 313b 0a20 2020 2020 2020 2020 2020  : 1;.           
+0000fc70: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fc80: 2066 696c 6c3a 206e 6f6e 653b 0a20 2020   fill: none;.   
+0000fc90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fca0: 2020 2020 2020 2020 2066 696c 6c2d 6f70           fill-op
+0000fcb0: 6163 6974 793a 2031 3b0a 2020 2020 2020  acity: 1;.      
+0000fcc0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fcd0: 2020 2020 2020 6669 6c6c 2d72 756c 653a        fill-rule:
+0000fce0: 206e 6f6e 7a65 726f 3b0a 2020 2020 2020   nonzero;.      
+0000fcf0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fd00: 2020 2020 2020 7374 726f 6b65 3a20 246f        stroke: $o
+0000fd10: 7262 5f63 6f6c 6f72 5f31 3530 3b0a 2020  rb_color_150;.  
+0000fd20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fd30: 2020 2020 2020 2020 2020 7374 726f 6b65            stroke
+0000fd40: 2d77 6964 7468 3a20 312e 3437 3633 3330  -width: 1.476330
+0000fd50: 3634 3b0a 2020 2020 2020 2020 2020 2020  64;.            
+0000fd60: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fd70: 7374 726f 6b65 2d6c 696e 6563 6170 3a20  stroke-linecap: 
+0000fd80: 6275 7474 3b0a 2020 2020 2020 2020 2020  butt;.          
+0000fd90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fda0: 2020 7374 726f 6b65 2d6c 696e 656a 6f69    stroke-linejoi
+0000fdb0: 6e3a 206d 6974 6572 3b0a 2020 2020 2020  n: miter;.      
+0000fdc0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fdd0: 2020 2020 2020 7374 726f 6b65 2d6d 6974        stroke-mit
+0000fde0: 6572 6c69 6d69 743a 2034 3b0a 2020 2020  erlimit: 4;.    
+0000fdf0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fe00: 2020 2020 2020 2020 7374 726f 6b65 2d64          stroke-d
+0000fe10: 6173 6861 7272 6179 3a20 6e6f 6e65 3b0a  asharray: none;.
+0000fe20: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fe30: 2020 2020 2020 2020 2020 2020 7374 726f              stro
+0000fe40: 6b65 2d6f 7061 6369 7479 3a20 313b 0a20  ke-opacity: 1;. 
+0000fe50: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fe60: 2020 2020 2020 2022 0a20 2020 2020 2020         ".       
+0000fe70: 2020 2020 2020 2020 2020 2020 202f 3e0a               />.
+0000fe80: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fe90: 3c2f 7379 6d62 6f6c 3e0a 2020 2020 2020  </symbol>.      
+0000fea0: 2020 2020 2020 2020 2020 3c73 796d 626f            <symbo
+0000feb0: 6c20 6964 3d22 6f72 6231 3830 223e 0a20  l id="orb180">. 
+0000fec0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fed0: 2020 203c 7061 7468 0a20 2020 2020 2020     <path.       
+0000fee0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+0000fef0: 2064 3d22 4d20 352e 3234 3634 3133 372c   d="M 5.2464137,
+0000ff00: 392e 3130 3234 3131 3420 4320 352e 3236  9.1024114 C 5.26
+0000ff10: 3037 3636 372c 3130 2e30 3233 3133 2034  07667,10.02313 4
+0000ff20: 2e36 3432 3430 3437 2c31 302e 3931 3137  .6424047,10.9117
+0000ff30: 3536 2033 2e37 3736 3736 3637 2c31 312e  56 3.7767667,11.
+0000ff40: 3232 3337 3335 2043 2033 2e30 3034 3330  223735 C 3.00430
+0000ff50: 3037 2c31 312e 3531 3435 3232 2032 2e30  07,11.514522 2.0
+0000ff60: 3735 3639 3037 2c31 312e 3334 3537 3133  756907,11.345713
+0000ff70: 2031 2e34 3637 3831 3637 2c31 302e 3738   1.4678167,10.78
+0000ff80: 3238 3836 2043 2030 2e38 3730 3632 3836  2886 C 0.8706286
+0000ff90: 372c 3130 2e32 3437 3436 2030 2e35 3930  7,10.24746 0.590
+0000ffa0: 3735 3036 372c 392e 3338 3138 3039 3220  75067,9.3818092 
+0000ffb0: 302e 3737 3730 3735 3637 2c38 2e35 3939  0.77707567,8.599
+0000ffc0: 3536 3134 2043 2030 2e39 3538 3732 3836  5614 C 0.9587286
+0000ffd0: 372c 372e 3739 3230 3834 3320 312e 3631  7,7.7920843 1.61
+0000ffe0: 3235 3535 372c 372e 3130 3734 3433 3420  25557,7.1074434 
+0000fff0: 322e 3431 3934 3135 372c 362e 3930 3939  2.4194157,6.9099
+00010000: 3230 3520 4320 332e 3139 3030 3632 372c  205 C 3.1900627,
+00010010: 362e 3731 3036 3820 342e 3036 3231 3331  6.71068 4.062131
+00010020: 372c 362e 3934 3534 3936 3620 342e 3631  7,6.9454966 4.61
+00010030: 3030 3837 372c 372e 3532 3831 3035 3820  00877,7.5281058 
+00010040: 4320 352e 3031 3239 3535 372c 372e 3934  C 5.0129557,7.94
+00010050: 3533 3531 3620 352e 3235 3137 3934 372c  53516 5.2517947,
+00010060: 382e 3532 3130 3139 3420 352e 3234 3634  8.5210194 5.2464
+00010070: 3133 372c 392e 3130 3234 3131 3420 7a20  137,9.1024114 z 
+00010080: 4d20 3131 2e32 3436 3431 342c 332e 3130  M 11.246414,3.10
+00010090: 3234 3132 3920 4320 3131 2e32 3630 3736  24129 C 11.26076
+000100a0: 352c 342e 3032 3331 3331 3720 3130 2e36  5,4.0231317 10.6
+000100b0: 3432 3430 342c 342e 3931 3137 3537 3420  42404,4.9117574 
+000100c0: 392e 3737 3637 3635 372c 352e 3232 3337  9.7767657,5.2237
+000100d0: 3336 3120 4320 392e 3030 3432 3939 372c  361 C 9.0042997,
+000100e0: 352e 3531 3435 3233 3820 382e 3037 3536  5.5145238 8.0756
+000100f0: 3839 372c 352e 3334 3537 3133 3520 372e  897,5.3457135 7.
+00010100: 3436 3738 3134 372c 342e 3738 3238 3837  4678147,4.782887
+00010110: 3320 4320 362e 3837 3036 3237 372c 342e  3 C 6.8706277,4.
+00010120: 3234 3734 3631 3320 362e 3539 3037 3439  2474613 6.590749
+00010130: 372c 332e 3338 3138 3120 362e 3737 3730  7,3.38181 6.7770
+00010140: 3734 372c 322e 3539 3935 3632 3420 4320  747,2.5995624 C 
+00010150: 362e 3935 3837 3236 372c 312e 3739 3230  6.9587267,1.7920
+00010160: 3835 3320 372e 3631 3235 3534 372c 312e  853 7.6125547,1.
+00010170: 3130 3734 3434 3520 382e 3431 3934 3134  1074445 8.419414
+00010180: 372c 302e 3930 3939 3231 3520 4320 392e  7,0.9099215 C 9.
+00010190: 3139 3030 3631 372c 302e 3731 3036 3831  1900617,0.710681
+000101a0: 3220 3130 2e30 3632 3133 2c30 2e39 3435  2 10.06213,0.945
+000101b0: 3439 3832 2031 302e 3631 3030 3837 2c31  4982 10.610087,1
+000101c0: 2e35 3238 3130 3733 2043 2031 312e 3031  .5281073 C 11.01
+000101d0: 3239 3535 2c31 2e39 3435 3335 3239 2031  2955,1.9453529 1
+000101e0: 312e 3235 3137 3934 2c32 2e35 3231 3032  1.251794,2.52102
+000101f0: 3036 2031 312e 3234 3634 3134 2c33 2e31  06 11.246414,3.1
+00010200: 3032 3431 3239 207a 204d 2034 2e35 3038  024129 z M 4.508
+00010210: 3234 3937 2c37 2e35 3738 3734 3320 4320  2497,7.578743 C 
+00010220: 352e 3533 3438 3533 372c 362e 3539 3435  5.5348537,6.5945
+00010230: 3232 3620 362e 3536 3134 3537 372c 352e  226 6.5614577,5.
+00010240: 3631 3033 3032 3220 372e 3538 3830 3631  6103022 7.588061
+00010250: 372c 342e 3632 3630 3831 3822 0a20 2020  7,4.6260818".   
+00010260: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010270: 2020 2020 2073 7479 6c65 3d22 0a20 2020       style=".   
+00010280: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010290: 2020 2020 2020 2020 206f 7061 6369 7479           opacity
+000102a0: 3a20 313b 0a20 2020 2020 2020 2020 2020  : 1;.           
+000102b0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000102c0: 2066 696c 6c3a 206e 6f6e 653b 0a20 2020   fill: none;.   
+000102d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000102e0: 2020 2020 2020 2020 2066 696c 6c2d 6f70           fill-op
+000102f0: 6163 6974 793a 2031 3b0a 2020 2020 2020  acity: 1;.      
+00010300: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010310: 2020 2020 2020 6669 6c6c 2d72 756c 653a        fill-rule:
+00010320: 206e 6f6e 7a65 726f 3b0a 2020 2020 2020   nonzero;.      
+00010330: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010340: 2020 2020 2020 7374 726f 6b65 3a20 246f        stroke: $o
+00010350: 7262 5f63 6f6c 6f72 5f31 3830 3b0a 2020  rb_color_180;.  
+00010360: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010370: 2020 2020 2020 2020 2020 7374 726f 6b65            stroke
+00010380: 2d77 6964 7468 3a20 312e 3437 3633 3330  -width: 1.476330
+00010390: 3634 3b0a 2020 2020 2020 2020 2020 2020  64;.            
+000103a0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000103b0: 7374 726f 6b65 2d6c 696e 6563 6170 3a20  stroke-linecap: 
+000103c0: 6275 7474 3b0a 2020 2020 2020 2020 2020  butt;.          
+000103d0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000103e0: 2020 7374 726f 6b65 2d6c 696e 656a 6f69    stroke-linejoi
+000103f0: 6e3a 206d 6974 6572 3b0a 2020 2020 2020  n: miter;.      
+00010400: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010410: 2020 2020 2020 7374 726f 6b65 2d6d 6974        stroke-mit
+00010420: 6572 6c69 6d69 743a 2034 3b0a 2020 2020  erlimit: 4;.    
+00010430: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010440: 2020 2020 2020 2020 7374 726f 6b65 2d64          stroke-d
+00010450: 6173 6861 7272 6179 3a20 6e6f 6e65 3b0a  asharray: none;.
+00010460: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010470: 2020 2020 2020 2020 2020 2020 7374 726f              stro
+00010480: 6b65 2d6f 7061 6369 7479 3a20 313b 0a20  ke-opacity: 1;. 
+00010490: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000104a0: 2020 2020 2020 2022 0a20 2020 2020 2020         ".       
+000104b0: 2020 2020 2020 2020 2020 2020 202f 3e0a               />.
+000104c0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+000104d0: 3c2f 7379 6d62 6f6c 3e0a 2020 2020 2020  </symbol>.      
+000104e0: 2020 2020 2020 2020 2020 3c21 2d2d 2072            <!-- r
+000104f0: 6574 726f 6772 6164 6520 7379 6d62 6f6c  etrograde symbol
+00010500: 2028 3132 7831 3229 202d 2d3e 0a20 2020   (12x12) -->.   
+00010510: 2020 2020 2020 2020 2020 2020 203c 7379               <sy
+00010520: 6d62 6f6c 2069 643d 2272 6574 726f 6772  mbol id="retrogr
+00010530: 6164 6522 3e0a 2020 2020 2020 2020 2020  ade">.          
+00010540: 2020 2020 2020 2020 2020 3c70 6174 680a            <path.
+00010550: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010560: 2020 2020 2020 2020 643d 224d 2035 2e31          d="M 5.1
+00010570: 3639 3530 3839 2c30 2e30 3635 3134 3330  695089,0.0651430
+00010580: 3720 4320 332e 3735 3937 3938 392c 302e  7 C 3.7597989,0.
+00010590: 3231 3539 3732 3037 2032 2e33 3331 3733  21597207 2.33173
+000105a0: 3439 2c30 2e33 3331 3439 3030 3720 302e  49,0.33149007 0.
+000105b0: 3931 3335 3831 3931 2c30 2e32 3335 3133  91358191,0.23513
+000105c0: 3130 3720 4320 312e 3534 3930 3332 392c  107 C 1.5490329,
+000105d0: 302e 3831 3930 3232 3037 2031 2e34 3032  0.81902207 1.402
+000105e0: 3438 3439 2c31 2e37 3130 3030 3131 2031  4849,1.7100011 1
+000105f0: 2e34 3232 3833 3739 2c32 2e34 3730 3034  .4228379,2.47004
+00010600: 3331 2043 2031 2e34 3137 3431 3539 2c35  31 C 1.4174159,5
+00010610: 2e32 3137 3434 3831 2031 2e34 3333 3737  .2174481 1.43377
+00010620: 3039 2c37 2e39 3635 3237 3331 2031 2e34  09,7.9652731 1.4
+00010630: 3134 3530 3139 2c31 302e 3731 3234 3131  145019,10.712411
+00010640: 2043 2031 2e35 3134 3934 3039 2c31 312e   C 1.5149409,11.
+00010650: 3137 3038 3438 2030 2e39 3637 3939 3739  170848 0.9679979
+00010660: 312c 3131 2e38 3334 3437 3120 302e 3930  1,11.834471 0.90
+00010670: 3238 3436 3931 2c31 312e 3936 3433 3032  284691,11.964302
+00010680: 2043 2031 2e39 3937 3638 3839 2c31 312e   C 1.9976889,11.
+00010690: 3936 3433 3032 2033 2e30 3932 3532 3939  964302 3.0925299
+000106a0: 2c31 312e 3936 3433 3032 2034 2e31 3837  ,11.964302 4.187
+000106b0: 3337 3139 2c31 312e 3936 3433 3032 2043  3719,11.964302 C
+000106c0: 2033 2e36 3031 3834 3339 2c31 312e 3537   3.6018439,11.57
+000106d0: 3739 3735 2033 2e36 3531 3039 3239 2c31  7975 3.6510929,1
+000106e0: 302e 3832 3030 3334 2033 2e36 3431 3733  0.820034 3.64173
+000106f0: 3939 2c31 302e 3231 3938 3338 2043 2033  99,10.219838 C 3
+00010700: 2e36 3431 3733 3939 2c38 2e38 3937 3436  .6417399,8.89746
+00010710: 3031 2033 2e36 3431 3733 3939 2c37 2e35  01 3.6417399,7.5
+00010720: 3735 3038 3331 2033 2e36 3431 3733 3939  750831 3.6417399
+00010730: 2c36 2e32 3532 3730 3531 2043 2034 2e35  ,6.2527051 C 4.5
+00010740: 3032 3632 3539 2c37 2e33 3937 3239 3131  026259,7.3972911
+00010750: 2035 2e33 3633 3531 3039 2c38 2e35 3431   5.3635109,8.541
+00010760: 3837 3731 2036 2e32 3234 3339 3539 2c39  8771 6.2243959,9
+00010770: 2e36 3836 3436 3331 2043 2035 2e36 3033  .6864631 C 5.603
+00010780: 3036 3939 2c31 302e 3031 3330 3439 2035  0699,10.013049 5
+00010790: 2e30 3732 3134 3339 2c31 302e 3439 3733  .0721439,10.4973
+000107a0: 3534 2034 2e33 3639 3234 3839 2c31 302e  54 4.3692489,10.
+000107b0: 3637 3233 3933 2043 2034 2e35 3735 3337  672393 C 4.57537
+000107c0: 3639 2c31 302e 3935 3537 3036 2034 2e37  69,10.955706 4.7
+000107d0: 3831 3530 3339 2c31 312e 3233 3930 3220  815039,11.23902 
+000107e0: 342e 3938 3736 3331 392c 3131 2e35 3232  4.9876319,11.522
+000107f0: 3333 3320 4320 352e 3439 3339 3231 392c  333 C 5.4939219,
+00010800: 3131 2e30 3138 3033 3620 362e 3134 3236  11.018036 6.1426
+00010810: 3338 392c 3130 2e36 3732 3231 3820 362e  389,10.672218 6.
+00010820: 3733 3336 3532 392c 3130 2e32 3634 3432  7336529,10.26442
+00010830: 3120 4320 372e 3338 3937 3033 392c 3131  1 C 7.3897039,11
+00010840: 2e32 3136 3931 3220 382e 3436 3937 3437  .216912 8.469747
+00010850: 392c 3132 2e30 3438 3339 3220 392e 3734  9,12.048392 9.74
+00010860: 3139 3339 392c 3132 2e30 3131 3537 3920  19399,12.011579 
+00010870: 4320 3130 2e31 3433 3630 332c 3132 2e30  C 10.143603,12.0
+00010880: 3032 3139 3920 3131 2e30 3637 3639 312c  02199 11.067691,
+00010890: 3131 2e38 3835 3832 3420 3131 2e30 3633  11.885824 11.063
+000108a0: 3737 352c 3131 2e36 3736 3037 3520 4320  775,11.676075 C 
+000108b0: 392e 3930 3034 3936 392c 3131 2e31 3238  9.9004969,11.128
+000108c0: 3035 3420 392e 3030 3138 3834 392c 3130  054 9.0018849,10
+000108d0: 2e31 3739 3038 3520 382e 3430 3639 3232  .179085 8.406922
+000108e0: 392c 392e 3130 3835 3034 3120 4320 382e  9,9.1085041 C 8.
+000108f0: 3936 3730 3433 392c 382e 3637 3536 3634  9670439,8.675664
+00010900: 3120 392e 3530 3536 3238 392c 382e 3138  1 9.5056289,8.18
+00010910: 3730 3035 3120 3130 2e31 3737 3338 322c  70051 10.177382,
+00010920: 372e 3930 3836 3733 3120 4320 3130 2e34  7.9086731 C 10.4
+00010930: 3139 3838 312c 372e 3836 3631 3530 3120  19881,7.8661501 
+00010940: 3130 2e30 3331 3636 382c 372e 3537 3633  10.031668,7.5763
+00010950: 3537 3120 392e 3938 3135 3033 392c 372e  571 9.9815039,7.
+00010960: 3431 3930 3935 3120 4320 392e 3738 3936  4190951 C 9.7896
+00010970: 3038 392c 362e 3930 3632 3933 3120 392e  089,6.9062931 9.
+00010980: 3632 3134 3337 392c 372e 3436 3934 3636  6214379,7.469466
+00010990: 3120 392e 3239 3530 3833 392c 372e 3632  1 9.2950839,7.62
+000109a0: 3339 3435 3120 4320 382e 3834 3533 3938  39451 C 8.845398
+000109b0: 392c 372e 3839 3237 3638 3120 382e 3330  9,7.8927681 8.30
+000109c0: 3738 3833 392c 382e 3336 3436 3031 3120  78839,8.3646011 
+000109d0: 372e 3836 3134 3435 392c 382e 3434 3534  7.8614459,8.4454
+000109e0: 3335 3120 4320 372e 3235 3531 3336 392c  351 C 7.2551369,
+000109f0: 372e 3538 3938 3637 3120 362e 3634 3838  7.5898671 6.6488
+00010a00: 3237 392c 362e 3733 3432 3939 3120 362e  279,6.7342991 6.
+00010a10: 3034 3235 3139 392c 352e 3837 3837 3332  0425199,5.878732
+00010a20: 3120 4320 372e 3234 3531 3933 392c 352e  1 C 7.2451939,5.
+00010a30: 3631 3734 3335 3120 382e 3538 3237 3833  6174351 8.582783
+00010a40: 392c 352e 3038 3533 3839 3120 392e 3037  9,5.0853891 9.07
+00010a50: 3034 3430 392c 332e 3933 3638 3938 3120  04409,3.9368981 
+00010a60: 4320 392e 3430 3633 3133 392c 332e 3131  C 9.4063139,3.11
+00010a70: 3230 3231 3120 392e 3236 3337 3333 392c  20211 9.2637339,
+00010a80: 322e 3136 3637 3933 3120 382e 3931 3037  2.1667931 8.9107
+00010a90: 3838 392c 312e 3337 3334 3730 3120 4320  889,1.3734701 C 
+00010aa0: 382e 3136 3834 3836 392c 302e 3431 3039  8.1684869,0.4109
+00010ab0: 3131 3037 2036 2e38 3639 3230 3439 2c2d  1107 6.8692049,-
+00010ac0: 302e 3037 3234 3531 3933 3120 352e 3631  0.072451931 5.61
+00010ad0: 3939 3732 392c 302e 3032 3531 3036 3037  99729,0.02510607
+00010ae0: 2043 2035 2e34 3639 3332 3739 2c30 2e30   C 5.4693279,0.0
+00010af0: 3332 3837 3230 3720 352e 3331 3930 3531  3287207 5.319051
+00010b00: 392c 302e 3034 3635 3130 3037 2035 2e31  9,0.04651007 5.1
+00010b10: 3639 3530 3839 2c30 2e30 3635 3134 3330  695089,0.0651430
+00010b20: 3720 4c20 352e 3136 3935 3038 392c 302e  7 L 5.1695089,0.
+00010b30: 3036 3531 3433 3037 207a 204d 2034 2e30  06514307 z M 4.0
+00010b40: 3035 3439 3439 2c30 2e39 3833 3037 3830  054949,0.9830780
+00010b50: 3620 4320 342e 3932 3734 3230 392c 302e  6 C 4.9274209,0.
+00010b60: 3837 3531 3630 3037 2036 2e30 3735 3238  87516007 6.07528
+00010b70: 3339 2c30 2e39 3536 3539 3430 3620 362e  39,0.95659406 6.
+00010b80: 3631 3139 3436 392c 312e 3737 3639 3832  6119469,1.776982
+00010b90: 3120 4320 372e 3139 3935 3438 392c 322e  1 C 7.1995489,2.
+00010ba0: 3734 3336 3233 3120 362e 3937 3731 3737  7436231 6.977177
+00010bb0: 392c 342e 3032 3737 3234 3120 362e 3233  9,4.0277241 6.23
+00010bc0: 3838 3835 392c 342e 3836 3934 3030 3120  88859,4.8694001 
+00010bd0: 4320 352e 3630 3533 3238 392c 352e 3535  C 5.6053289,5.55
+00010be0: 3439 3033 3120 342e 3535 3231 3035 392c  49031 4.5521059,
+00010bf0: 352e 3637 3830 3737 3120 332e 3634 3137  5.6780771 3.6417
+00010c00: 3339 392c 352e 3537 3237 3533 3120 4320  399,5.5727531 C 
+00010c10: 332e 3634 3137 3339 392c 342e 3036 3535  3.6417399,4.0655
+00010c20: 3237 3120 332e 3634 3137 3339 392c 322e  271 3.6417399,2.
+00010c30: 3535 3833 3030 3120 332e 3634 3137 3339  5583001 3.641739
+00010c40: 392c 312e 3035 3130 3733 3120 4320 332e  9,1.0510731 C 3.
+00010c50: 3736 3239 3931 392c 312e 3032 3834 3038  7629919,1.028408
+00010c60: 3120 332e 3838 3432 3432 392c 312e 3030  1 3.8842429,1.00
+00010c70: 3537 3433 3120 342e 3030 3534 3934 392c  57431 4.0054949,
+00010c80: 302e 3938 3330 3738 3036 207a 220a 2020  0.98307806 z".  
+00010c90: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010ca0: 2020 2020 2020 7374 796c 653d 2266 696c        style="fil
+00010cb0: 6c3a 2024 7061 7065 725f 636f 6c6f 725f  l: $paper_color_
+00010cc0: 3022 0a20 2020 2020 2020 2020 2020 2020  0".             
+00010cd0: 2020 2020 2020 202f 3e0a 2020 2020 2020         />.      
+00010ce0: 2020 2020 2020 2020 2020 3c2f 7379 6d62            </symb
+00010cf0: 6f6c 3e0a 2020 2020 2020 2020 2020 2020  ol>.            
+00010d00: 2020 2020 3c67 2074 7261 6e73 666f 726d      <g transform
+00010d10: 3d22 7472 616e 736c 6174 6528 3530 2c35  ="translate(50,5
+00010d20: 3029 223e 0a20 2020 2020 2020 2020 2020  0)">.           
+00010d30: 2020 2020 2020 2020 203c 6720 7472 616e           <g tran
+00010d40: 7366 6f72 6d3d 2274 7261 6e73 6c61 7465  sform="translate
+00010d50: 2824 6369 7263 6c65 582c 2463 6972 636c  ($circleX,$circl
+00010d60: 6559 2922 3e0a 2020 2020 2020 2020 2020  eY)">.          
+00010d70: 2020 2020 2020 2020 2020 2020 2020 3c21                <!
+00010d80: 2d2d 205a 6f64 6961 6320 2d2d 3e24 6d61  -- Zodiac -->$ma
+00010d90: 6b65 5a6f 6469 6163 203c 212d 2d20 4669  keZodiac <!-- Fi
+00010da0: 7273 7420 4369 7263 6c65 202d 2d3e 0a20  rst Circle -->. 
+00010db0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010dc0: 2020 2020 2020 203c 6369 7263 6c65 2024         <circle $
+00010dd0: 6331 2073 7479 6c65 3d22 2463 3173 7479  c1 style="$c1sty
+00010de0: 6c65 2220 2f3e 0a20 2020 2020 2020 2020  le" />.         
+00010df0: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+00010e00: 212d 2d20 5365 636f 6e64 2043 6972 636c  !-- Second Circl
+00010e10: 6520 2d2d 3e0a 2020 2020 2020 2020 2020  e -->.          
+00010e20: 2020 2020 2020 2020 2020 2020 2020 3c63                <c
+00010e30: 6972 636c 650a 2020 2020 2020 2020 2020  ircle.          
+00010e40: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010e50: 2020 2463 3220 7374 796c 653d 2224 6332    $c2 style="$c2
+00010e60: 7374 796c 6522 202f 3e0a 2020 2020 2020  style" />.      
+00010e70: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010e80: 2020 3c21 2d2d 2054 6869 7264 2043 6972    <!-- Third Cir
+00010e90: 636c 6520 2d2d 3e0a 2020 2020 2020 2020  cle -->.        
+00010ea0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010eb0: 3c63 6972 636c 6520 2463 3320 7374 796c  <circle $c3 styl
+00010ec0: 653d 2224 6333 7374 796c 6522 202f 3e0a  e="$c3style" />.
+00010ed0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010ee0: 2020 2020 2020 2020 3c21 2d2d 2054 7261          <!-- Tra
+00010ef0: 6e73 6974 5269 6e67 202d 2d3e 2474 7261  nsitRing -->$tra
+00010f00: 6e73 6974 5269 6e67 203c 212d 2d20 4465  nsitRing <!-- De
+00010f10: 6772 6565 2052 696e 6720 2d2d 3e24 6465  gree Ring -->$de
+00010f20: 6772 6565 5269 6e67 203c 212d 2d20 486f  greeRing <!-- Ho
+00010f30: 7573 6573 202d 2d3e 0a20 2020 2020 2020  uses -->.       
+00010f40: 2020 2020 2020 2020 2020 2020 2024 6d61               $ma
+00010f50: 6b65 486f 7573 6573 0a20 2020 2020 2020  keHouses.       
+00010f60: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010f70: 203c 212d 2d20 506c 616e 6574 7320 2d2d   <!-- Planets --
+00010f80: 3e24 6d61 6b65 506c 616e 6574 7320 3c21  >$makePlanets <!
+00010f90: 2d2d 2041 7370 6563 7473 202d 2d3e 246d  -- Aspects -->$m
+00010fa0: 616b 6541 7370 6563 7473 203c 2f67 3e0a  akeAspects </g>.
+00010fb0: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00010fc0: 2020 2020 3c21 2d2d 206d 616b 6550 6174      <!-- makePat
+00010fd0: 7465 726e 7320 2d2d 3e24 6d61 6b65 5061  terns -->$makePa
+00010fe0: 7474 6572 6e73 203c 212d 2d20 4173 7065  tterns <!-- Aspe
+00010ff0: 6374 4772 6964 202d 2d3e 0a20 2020 2020  ctGrid -->.     
+00011000: 2020 2020 2020 2020 2020 2020 2020 2024                 $
+00011010: 6d61 6b65 4173 7065 6374 4772 6964 0a20  makeAspectGrid. 
+00011020: 2020 2020 2020 2020 2020 2020 2020 2020                  
+00011030: 2020 203c 212d 2d20 456c 656d 656e 7473     <!-- Elements
+00011040: 202d 2d3e 246d 616b 6545 6c65 6d65 6e74   -->$makeElement
+00011050: 7320 3c21 2d2d 2050 6c61 6e65 7420 4772  s <!-- Planet Gr
+00011060: 6964 202d 2d3e 246d 616b 6550 6c61 6e65  id -->$makePlane
+00011070: 7447 7269 6420 3c21 2d2d 2048 6f75 7365  tGrid <!-- House
+00011080: 7320 4772 6964 202d 2d3e 0a20 2020 2020  s Grid -->.     
+00011090: 2020 2020 2020 2020 2020 2020 2020 2024                 $
+000110a0: 6d61 6b65 486f 7573 6573 4772 6964 0a20  makeHousesGrid. 
+000110b0: 2020 2020 2020 2020 2020 2020 2020 203c                 <
+000110c0: 2f67 3e0a 2020 2020 2020 2020 2020 2020  /g>.            
+000110d0: 3c2f 673e 0a20 2020 2020 2020 203c 2f67  </g>.        </g
+000110e0: 3e0a 2020 2020 3c2f 673e 0a3c 2f73 7667  >.    </g>.</svg
+000110f0: 3e0a                                     >.
```

### Comparing `kerykeion-4.0a5/kerykeion/fetch_geonames.py` & `kerykeion-4.0rc1/kerykeion/fetch_geonames.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
+# -*- coding: utf-8 -*-
 """
     This is part of Kerykeion (C) 2023 Giacomo Battaglia
 """
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
+
 
 from logging import getLogger
 from requests import Request
 from requests_cache import CachedSession
 from typing import Union
 
 
@@ -67,15 +67,15 @@
             timezone_data["timezonestr"] = response_json["timezoneId"]
 
         except Exception as e:
             logger.error(f"Error serializing data maybe wrong username? Details: {e}")
             return {}
 
         if hasattr(response, "from_cache"):
-            timezone_data["from_tz_cache"] = response.from_cache
+            timezone_data["from_tz_cache"] = response.from_cache  # type: ignore
 
         return timezone_data
 
     def __get_contry_data(self, city_name: str, country_code: str) -> dict[str, str]:
         """
         Get the city data *whitout timezone* for a given city and country name
         """
@@ -108,15 +108,15 @@
             city_data_whitout_tz["countryCode"] = response_json["geonames"][0]["countryCode"]
 
         except Exception as e:
             logger.error(f"Error serializing data maybe wrong username? Details: {e}")
             return {}
 
         if hasattr(response, "from_cache"):
-            city_data_whitout_tz["from_country_cache"] = response.from_cache
+            city_data_whitout_tz["from_country_cache"] = response.from_cache  # type: ignore
 
         return city_data_whitout_tz
 
     def get_serialized_data(self) -> dict[str, str]:
         """
         Returns all the data necessary for the Kerykeion calculation.
 
@@ -131,15 +131,15 @@
             logger.error(f"Error in fetching timezone: {e}")
             return {}
 
         return {**timezone_response, **city_data_response}
 
 
 if __name__ == "__main__":
-    from logging import basicConfig, INFO
+    from logging import basicConfig
 
     basicConfig(
         format="%(asctime)s - %(name)s - %(levelname)s - %(message)s",
         level=10,
         force=True,
     )
```

### Comparing `kerykeion-4.0a5/kerykeion/kr.config.json` & `kerykeion-4.0rc1/kerykeion/settings/kr.config.json`

 * *Files 15% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.3602321742267395%*

 * *Differences: {"'aspects'": "{0: {'is_active': 1, 'color': '#5757e2', delete: ['visible']}, 1: {'is_active': 0, "*

 * *              "'color': '#810757', delete: ['visible']}, 2: {'is_active': 0, 'color': '#b14e58', "*

 * *              "delete: ['visible']}, 3: {'is_active': 1, 'color': '#d59e28', delete: ['visible']}, "*

 * *              "4: {'is_active': 1, 'color': '#1f99b3', delete: ['visible']}, 5: {'is_active': 1, "*

 * *              "'color': '#dc0000', delete: ['visible']}, 6: {'is_active': 1, 'color': '#36d100', "*

 * *               […]*

```diff
@@ -1,307 +1,305 @@
 {
     "aspects": [
         {
+            "color": "#5757e2",
             "degree": 0,
+            "is_active": 1,
             "is_major": 1,
             "is_minor": 0,
             "name": "conjunction",
             "orb": 10,
-            "visible": 1,
             "visible_grid": 1
         },
         {
+            "color": "#810757",
             "degree": 30,
+            "is_active": 0,
             "is_major": 0,
             "is_minor": 1,
             "name": "semi-sextile",
             "orb": 1,
-            "visible": 0,
             "visible_grid": 0
         },
         {
+            "color": "#b14e58",
             "degree": 45,
+            "is_active": 0,
             "is_major": 0,
             "is_minor": 1,
             "name": "semi-square",
             "orb": 1,
-            "visible": 0,
             "visible_grid": 0
         },
         {
+            "color": "#d59e28",
             "degree": 60,
+            "is_active": 1,
             "is_major": 1,
             "is_minor": 0,
             "name": "sextile",
             "orb": 6,
-            "visible": 1,
             "visible_grid": 1
         },
         {
+            "color": "#1f99b3",
             "degree": 72,
+            "is_active": 1,
             "is_major": 0,
             "is_minor": 1,
             "name": "quintile",
             "orb": 1,
-            "visible": 1,
             "visible_grid": 1
         },
         {
+            "color": "#dc0000",
             "degree": 90,
+            "is_active": 1,
             "is_major": 1,
             "is_minor": 0,
             "name": "square",
             "orb": 5,
-            "visible": 1,
             "visible_grid": 1
         },
         {
+            "color": "#36d100",
             "degree": 120,
+            "is_active": 1,
             "is_major": 1,
             "is_minor": 0,
             "name": "trine",
             "orb": 8,
-            "visible": 1,
             "visible_grid": 1
         },
         {
+            "color": "#985a10",
             "degree": 135,
+            "is_active": 0,
             "is_major": 0,
             "is_minor": 1,
             "name": "sesquiquadrate",
             "orb": 1,
-            "visible": 0,
             "visible_grid": 0
         },
         {
+            "color": "#7a9810",
             "degree": 144,
+            "is_active": 0,
             "is_major": 0,
             "is_minor": 1,
             "name": "biquintile",
             "orb": 1,
-            "visible": 0,
             "visible_grid": 0
         },
         {
+            "color": "#26bbcf",
             "degree": 150,
+            "is_active": 0,
             "is_major": 0,
             "is_minor": 0,
             "name": "quincunx",
             "orb": 1,
-            "visible": 0,
             "visible_grid": 0
         },
         {
+            "color": "#510060",
             "degree": 180,
+            "is_active": 1,
             "is_major": 1,
             "is_minor": 0,
             "name": "opposition",
             "orb": 10,
-            "visible": 1,
             "visible_grid": 1
         }
     ],
-    "axes_orbit": 1,
     "celestial_points": [
         {
             "color": "#984b00",
             "element_points": 40,
             "id": 0,
+            "is_active": true,
             "label": "Sun",
-            "label_short": "sun",
             "name": "Sun",
-            "visible": 1,
-            "zodiac_relation": "4"
+            "related_zodiac_signs": [
+                "4"
+            ]
         },
         {
             "color": "#150052",
             "element_points": 40,
             "id": 1,
+            "is_active": true,
             "label": "Moon",
-            "label_short": "moon",
             "name": "Moon",
-            "visible": 1,
-            "zodiac_relation": "3"
+            "related_zodiac_signs": [
+                "3"
+            ]
         },
         {
             "color": "#520800",
             "element_points": 15,
             "id": 2,
+            "is_active": true,
             "label": "Mercury",
-            "label_short": "mercury",
             "name": "Mercury",
-            "visible": 1,
-            "zodiac_relation": "2,5"
+            "related_zodiac_signs": [
+                "2",
+                "5"
+            ]
         },
         {
             "color": "#400052",
             "element_points": 15,
             "id": 3,
+            "is_active": true,
             "label": "Venus",
-            "label_short": "venus",
             "name": "Venus",
-            "visible": 1,
-            "zodiac_relation": "1,6"
+            "related_zodiac_signs": [
+                "1",
+                "6"
+            ]
         },
         {
             "color": "#540000",
             "element_points": 15,
             "id": 4,
+            "is_active": true,
             "label": "Mars",
-            "label_short": "mars",
             "name": "Mars",
-            "visible": 1,
-            "zodiac_relation": "0"
+            "related_zodiac_signs": [
+                "0"
+            ]
         },
         {
             "color": "#47133d",
             "element_points": 10,
             "id": 5,
+            "is_active": true,
             "label": "Jupiter",
-            "label_short": "jupiter",
             "name": "Jupiter",
-            "visible": 1,
-            "zodiac_relation": "8"
+            "related_zodiac_signs": [
+                "8"
+            ]
         },
         {
             "color": "#124500",
             "element_points": 10,
             "id": 6,
+            "is_active": true,
             "label": "Saturn",
-            "label_short": "saturn",
             "name": "Saturn",
-            "visible": 1,
-            "zodiac_relation": "9"
+            "related_zodiac_signs": [
+                "9"
+            ]
         },
         {
             "color": "#6f0766",
             "element_points": 10,
             "id": 7,
+            "is_active": true,
             "label": "Uranus",
-            "label_short": "uranus",
             "name": "Uranus",
-            "visible": 1,
-            "zodiac_relation": "10"
+            "related_zodiac_signs": [
+                "10"
+            ]
         },
         {
             "color": "#06537f",
             "element_points": 10,
             "id": 8,
+            "is_active": true,
             "label": "Neptune",
-            "label_short": "neptune",
             "name": "Neptune",
-            "visible": 1,
-            "zodiac_relation": "11"
+            "related_zodiac_signs": [
+                "11"
+            ]
         },
         {
             "color": "#713f04",
             "element_points": 10,
             "id": 9,
+            "is_active": true,
             "label": "Pluto",
-            "label_short": "pluto",
             "name": "Pluto",
-            "visible": 1,
-            "zodiac_relation": "7"
+            "related_zodiac_signs": [
+                "7"
+            ]
         },
         {
             "color": "#4c1541",
             "element_points": 20,
             "id": 10,
-            "label": "North_Node",
-            "label_short": "North_Node",
-            "name": "Mean_Node",
-            "visible": 0,
-            "zodiac_relation": "-1"
+            "is_active": true,
+            "label": "True_Node",
+            "name": "True_Node",
+            "related_zodiac_signs": []
         },
         {
             "color": "#4c1541",
             "element_points": 0,
             "id": 11,
+            "is_active": false,
             "label": "Mean_Node",
-            "label_short": "Mean_Node",
             "name": "Mean_Node",
-            "visible": 0,
-            "zodiac_relation": "-1"
+            "related_zodiac_signs": []
         },
         {
-            "color": "orange",
+            "color": "#ff7e00",
             "element_points": 40,
             "id": 12,
+            "is_active": true,
             "label": "Asc",
-            "label_short": "Asc",
-            "name": "First House",
-            "visible": 1,
-            "zodiac_relation": "-1"
+            "name": "First_House",
+            "related_zodiac_signs": []
         },
         {
             "color": "#FF0000",
             "element_points": 20,
             "id": 13,
+            "is_active": true,
             "label": "Mc",
-            "label_short": "Mc",
-            "name": "Tenth House",
-            "visible": 1,
-            "zodiac_relation": "-1"
+            "name": "Tenth_House",
+            "related_zodiac_signs": []
         },
         {
             "color": "#0000FF",
             "element_points": 0,
             "id": 14,
+            "is_active": false,
             "label": "Dsc",
-            "label_short": "Dsc",
-            "name": "Seventh House",
-            "visible": 0,
-            "zodiac_relation": "-1"
+            "name": "Seventh_House",
+            "related_zodiac_signs": []
         },
         {
             "color": "#000000",
             "element_points": 0,
             "id": 15,
+            "is_active": false,
             "label": "Ic",
-            "label_short": "Ic",
-            "name": "Fourth House",
-            "visible": 0,
-            "zodiac_relation": "-1"
+            "name": "Fourth_House",
+            "related_zodiac_signs": []
+        },
+        {
+            "color": "#666f06",
+            "element_points": 0,
+            "id": 16,
+            "is_active": true,
+            "label": "Chiron",
+            "name": "Chiron",
+            "related_zodiac_signs": []
         }
     ],
-    "colors": {
-        "aspect_0": "#5757e2",
-        "aspect_120": "#36d100",
-        "aspect_135": "#985a10",
-        "aspect_144": "#7a9810",
-        "aspect_150": "#26bbcf",
-        "aspect_180": "#510060",
-        "aspect_30": "#810757",
-        "aspect_45": "#b14e58",
-        "aspect_60": "#d59e28",
-        "aspect_72": "#1f99b3",
-        "aspect_90": "#dc0000",
+    "chart_colors": {
         "houses_radix_line": "#ff0000",
         "houses_transit_line": "#0000ff",
         "lunar_phase_0": "#000000",
         "lunar_phase_1": "#FFFFFF",
         "lunar_phase_2": "#CCCCCC",
         "paper_0": "#000000",
         "paper_1": "#ffffff",
-        "planet_0": "#984b00",
-        "planet_1": "#150052",
-        "planet_10": "#4c1541",
-        "planet_11": "#4c1541",
-        "planet_12": "#ff7e00",
-        "planet_13": "#FF0000",
-        "planet_14": "#0000FF",
-        "planet_15": "#000000",
-        "planet_2": "#520800",
-        "planet_3": "#400052",
-        "planet_4": "#540000",
-        "planet_5": "#47133d",
-        "planet_6": "#124500",
-        "planet_7": "#6f0766",
-        "planet_8": "#06537f",
-        "planet_9": "#713f04",
         "zodiac_bg_0": "#ff7200",
         "zodiac_bg_1": "#6b3d00",
         "zodiac_bg_10": "#69acf1",
         "zodiac_bg_11": "#2b4972",
         "zodiac_bg_2": "#69acf1",
         "zodiac_bg_3": "#2b4972",
         "zodiac_bg_4": "#ff7200",
@@ -326,34 +324,40 @@
         "zodiac_radix_ring_1": "#ff0000",
         "zodiac_radix_ring_2": "#ff0000",
         "zodiac_transit_ring_0": "#ff0000",
         "zodiac_transit_ring_1": "#ff0000",
         "zodiac_transit_ring_2": "#0000ff",
         "zodiac_transit_ring_3": "#0000ff"
     },
+    "general_settings": {
+        "axes_orbit": 1,
+        "language": "EN",
+        "planet_in_zodiac_extra_points": 10
+    },
     "language_settings": {
         "CN": {
-            "&": "\u8207",
             "air": "\u98a8",
+            "and_word": "\u8207",
             "aspects": "\u76f8\u4f4d",
             "celestial_points": {
                 "Asc": "\u4e0a\u5347\u9ede",
+                "Chiron": "\u51f1\u9f8d\u661f",
                 "Dsc": "\u4e0b\u964d\u9ede",
                 "Ic": "\u4e0b\u4e2d\u5929",
                 "Jupiter": "\u6728\u661f",
                 "Mars": "\u706b\u661f",
                 "Mc": "\u4e0a\u4e2d\u5929",
                 "Mean_Node": "\u5e73\u4ea4\u9ede",
                 "Mercury": "\u6c34\u661f",
                 "Moon": "\u6708\u4eae",
                 "Neptune": "\u6d77\u738b\u661f",
-                "North_Node": "\u5317\u4ea4\u9ede",
                 "Pluto": "\u51a5\u738b\u661f",
                 "Saturn": "\u571f\u661f",
                 "Sun": "\u592a\u967d",
+                "True_Node": "\u5317\u4ea4\u9ede",
                 "Uranus": "\u5929\u738b\u661f",
                 "Venus": "\u91d1\u661f"
             },
             "cusp": "\u5bae",
             "day": "\u65e5",
             "earth": "\u571f",
             "east": "\u6771",
@@ -361,76 +365,68 @@
             "info": "\u547d\u76e4\u8cc7\u8a0a",
             "latitude": "\u7def\u5ea6",
             "longitude": "\u7d93\u5ea6",
             "lunar_phase": "\u6708\u76f8",
             "north": "\u5317",
             "planets_and_house": "\u884c\u661f \u8207 \u5bab\u4f4d",
             "south": "\u5357",
-            "transit_name": "\u6d41\u5e74\u661f\u76f8",
+            "transit_name": "\u6d41\u5e74\u540d\u7a31",
             "transits": "\u6d41\u5e74\u5408\u76e4",
             "type": "\u76e4\u578b",
             "water": "\u6c34",
             "west": "\u897f"
         },
         "EN": {
-            "&": "and",
             "air": "Air",
+            "and_word": "and",
             "aspects": "Couple aspects",
             "celestial_points": {
                 "Asc": "Asc",
+                "Chiron": "Chiron",
                 "Dsc": "Dsc",
                 "Ic": "Ic",
                 "Jupiter": "Jupiter",
                 "Mars": "Mars",
                 "Mc": "Mc",
                 "Mean_Node": "Mean Node",
                 "Mercury": "Mercury",
                 "Moon": "Moon",
                 "Neptune": "Neptune",
-                "North_Node": "North Node",
                 "Pluto": "Pluto",
                 "Saturn": "Saturn",
                 "Sun": "Sun",
+                "True_Node": "North Node",
                 "Uranus": "Uranus",
                 "Venus": "Venus"
             },
             "cusp": "Cusp",
             "day": "Day",
             "earth": "Earth",
             "east": "East",
             "fire": "Fire",
             "info": "Info",
             "latitude": "Latitude",
             "longitude": "Longitude",
             "lunar_phase": "Lunar phase",
             "north": "North",
-            "planets_and_house": "Planets and houses for",
+            "planets_and_house": "Points for",
             "south": "South",
-            "transit_name": "Here and now",
+            "transit_name": "At the time of the transit",
             "transits": "Transits for",
             "type": "Type",
             "water": "Water",
             "west": "West"
         },
         "FR": {
-            "&": "et",
             "air": "Air",
+            "and_word": "et",
             "aspects": "Les aspects",
-            "cusp": "Maison",
-            "day": "Jour",
-            "earth": "Terre",
-            "east": "Est",
-            "fire": "Feu",
-            "info": "Informations",
-            "latitude": "Latitude",
-            "longitude": "Longitude",
-            "lunar_phase": "Phase Lunaire",
-            "north": "Nord",
-            "planets": {
+            "celestial_points": {
                 "Asc": "Asc",
+                "Chiron": "Chiron",
                 "Dsc": "Dsc",
                 "Ic": "Ic",
                 "Jupiter": "Jupiter",
                 "Mars": "Mars",
                 "Mc": "Mc",
                 "Mean_Node": "Noeud Moyen",
                 "Mercury": "Mercure",
@@ -439,97 +435,109 @@
                 "North_Node": "Noeud Nord",
                 "Pluto": "Pluton",
                 "Saturn": "Saturne",
                 "Sun": "Soleil",
                 "Uranus": "Uranus",
                 "Venus": "V\u00e9nus"
             },
-            "planets_and_house": "Planetes et Maisons pour",
+            "cusp": "Maison",
+            "day": "Jour",
+            "earth": "Terre",
+            "east": "Est",
+            "fire": "Feu",
+            "info": "Informations",
+            "latitude": "Latitude",
+            "longitude": "Longitude",
+            "lunar_phase": "Phase Lunaire",
+            "north": "Nord",
+            "planets_and_house": "Points pour",
             "south": "Sud",
             "transit_name": "Au moment de la transition",
             "transits": "Transites pour",
             "type": "Type",
             "water": "Eau",
             "west": "Ouest"
         },
         "IT": {
-            "&": "e",
             "air": "Aria",
+            "and_word": "e",
             "aspects": "Aspetti di coppia",
             "celestial_points": {
                 "Asc": "Asc",
+                "Chiron": "Chirone",
                 "Dsc": "Dsc",
                 "Ic": "Ic",
                 "Jupiter": "Giove",
                 "Mars": "Marte",
                 "Mc": "Mc",
-                "Mean_Node": "Mean Node",
+                "Mean_Node": "Nodo Medio",
                 "Mercury": "Mercurio",
                 "Moon": "Luna",
                 "Neptune": "Nettuno",
-                "North_Node": "Nodo Nord",
                 "Pluto": "Plutone",
                 "Saturn": "Saturno",
                 "Sun": "Sole",
+                "True_Node": "Nodo Nord",
                 "Uranus": "Urano",
                 "Venus": "Venere"
             },
             "cusp": "Cuspide",
             "day": "Giorno",
             "earth": "Terra",
             "east": "Est",
             "fire": "Fuoco",
             "info": "Info",
             "latitude": "Latitudine",
             "longitude": "Longitudine",
             "lunar_phase": "Fase lunare",
             "north": "Nord",
-            "planets_and_house": "Pianeti e case per",
+            "planets_and_house": "Punti per",
             "south": "Sud",
-            "transit_name": "Qui ed ora",
+            "transit_name": "Al momento del transito",
             "transits": "Transiti per",
             "type": "Tipo",
             "water": "Acqua",
             "west": "Ovest"
         },
         "PT": {
-            "&": "e",
             "air": "Ar",
+            "and_word": "e",
             "aspects": "Aspectos do casal",
             "celestial_points": {
                 "Asc": "Asc",
+                "Chiron": "Qu\u00edron",
                 "Dsc": "Dsc",
                 "Ic": "Ic",
                 "Jupiter": "J\u00fapiter",
                 "Mars": "Marte",
                 "Mc": "Mc",
                 "Mean_Node": "Nodo M\u00e9dio",
                 "Mercury": "Merc\u00fario",
                 "Moon": "Lua",
                 "Neptune": "Netuno",
-                "North_Node": "Nodo Norte",
                 "Pluto": "Plut\u00e3o",
                 "Saturn": "Saturno",
                 "Sun": "Sol",
+                "True_Node": "Nodo Norte",
                 "Uranus": "Urano",
                 "Venus": "V\u00eanus"
             },
             "cusp": "Casa",
             "day": "Dia",
             "earth": "Terra",
             "east": "Leste",
             "fire": "Fogo",
             "info": "Informa\u00e7\u00f5es",
             "latitude": "Latitude",
             "longitude": "Longitude",
             "lunar_phase": "Fase lunar",
             "north": "Norte",
-            "planets_and_house": "Planetas e casas para",
+            "planets_and_house": "Pontos para",
             "south": "Sul",
-            "transit_name": "Aqui e agora",
+            "transit_name": "No momento do tr\u00e2nsito",
             "transits": "Tr\u00e2nsitos para",
             "type": "Tipo",
             "water": "\u00c1gua",
             "west": "Oeste"
         }
     }
 }
```

### Comparing `kerykeion-4.0a5/kerykeion/kr_instance.py` & `kerykeion-4.0rc1/kerykeion/astrological_subject.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,61 +1,62 @@
+# -*- coding: utf-8 -*-
 """
     This is part of Kerykeion (C) 2023 Giacomo Battaglia
 """
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
 
 import math
 import pytz
 import swisseph as swe
 
 from datetime import datetime
 from logging import getLogger, basicConfig
 from kerykeion.fetch_geonames import FetchGeonames
 from kerykeion.kr_types import (
     KerykeionException,
     ZodiacType,
-    KerykeionSubject,
-    LunarPhaseObject,
-    KerykeionPoint,
+    AstrologicalSubjectModel,
+    LunarPhaseModel,
+    KerykeionPointModel,
 )
 from kerykeion.utilities import get_number_from_name, calculate_position
 from pathlib import Path
 from typing import Union, Literal
 
-# swe.set_ephe_path("/")
-
 
 logger = getLogger(__name__)
 
 
-class KrInstance:
+class AstrologicalSubject:
     """
     Calculates all the astrological information, the coordinates,
     it's utc and julian day and returns an object with all that data.
 
     Args:
     - name (str, optional): _ Defaults to "Now".
     - year (int, optional): _ Defaults to now.year.
     - month (int, optional): _ Defaults to now.month.
     - day (int, optional): _ Defaults to now.day.
     - hour (int, optional): _ Defaults to now.hour.
     - minute (int, optional): _ Defaults to now.minute.
-    - city (str, optional): City or location of birth. Defaults to "London".
+    - city (str, optional): City or location of birth. Defaults to "London", which is GMT time.
+        The city argument is used to get the coordinates and timezone from geonames just in case
+        you don't insert them manually (see _get_tz).
+        If you insert the coordinates and timezone manually, the city argument is not used for calculations
+        but it's still used as a value for the city attribute.
     - nat (str, optional): _ Defaults to "".
     - lng (Union[int, float], optional): _ Defaults to False.
     - lat (Union[int, float], optional): _ Defaults to False.
     - tz_str (Union[str, bool], optional): _ Defaults to False.
     - logger (Union[Logger, None], optional): _ Defaults to None.
     - geonames_username (str, optional): _ Defaults to 'century.boy'.
     - online (bool, optional): Sets if you want to use the online mode (using
         geonames) or not. Defaults to True.
     """
 
-    # User defined
+    # Defined by the user
     name: str
     year: int
     month: int
     day: int
     hour: int
     minute: int
     city: str
@@ -66,108 +67,137 @@
     geonames_username: str
     online: bool
     zodiac_type: ZodiacType
 
     # Generated internally
     city_data: dict[str, str]
     julian_day: Union[int, float]
-    utc_time: datetime
-    local_time: datetime
+    utc_time: float
+    local_time: float
     utc: datetime
     json_dir: Path
 
     # Planets
-    sun: KerykeionPoint
-    moon: KerykeionPoint
-    mercury: KerykeionPoint
-    venus: KerykeionPoint
-    mars: KerykeionPoint
-    jupiter: KerykeionPoint
-    saturn: KerykeionPoint
-    uranus: KerykeionPoint
-    neptune: KerykeionPoint
-    pluto: KerykeionPoint
-    true_node: KerykeionPoint
-    mean_node: KerykeionPoint
+    sun: KerykeionPointModel
+    moon: KerykeionPointModel
+    mercury: KerykeionPointModel
+    venus: KerykeionPointModel
+    mars: KerykeionPointModel
+    jupiter: KerykeionPointModel
+    saturn: KerykeionPointModel
+    uranus: KerykeionPointModel
+    neptune: KerykeionPointModel
+    pluto: KerykeionPointModel
+    true_node: KerykeionPointModel
+    mean_node: KerykeionPointModel
+    chiron: KerykeionPointModel
 
     # Houses
-    first_house: KerykeionPoint
-    second_house: KerykeionPoint
-    third_house: KerykeionPoint
-    fourth_house: KerykeionPoint
-    fifth_house: KerykeionPoint
-    sixth_house: KerykeionPoint
-    seventh_house: KerykeionPoint
-    eighth_house: KerykeionPoint
-    ninth_house: KerykeionPoint
-    tenth_house: KerykeionPoint
-    eleventh_house: KerykeionPoint
-    twelfth_house: KerykeionPoint
+    first_house: KerykeionPointModel
+    second_house: KerykeionPointModel
+    third_house: KerykeionPointModel
+    fourth_house: KerykeionPointModel
+    fifth_house: KerykeionPointModel
+    sixth_house: KerykeionPointModel
+    seventh_house: KerykeionPointModel
+    eighth_house: KerykeionPointModel
+    ninth_house: KerykeionPointModel
+    tenth_house: KerykeionPointModel
+    eleventh_house: KerykeionPointModel
+    twelfth_house: KerykeionPointModel
+
+    # Lists
+    houses: list[KerykeionPointModel]
+    planets: list[KerykeionPointModel]
+    planets_degrees_ut: list[float]
+    houses_degree_ut: list[float]
 
     now = datetime.now()
 
+
     def __init__(
         self,
         name="Now",
         year: int = now.year,
         month: int = now.month,
         day: int = now.day,
         hour: int = now.hour,
         minute: int = now.minute,
-        city: str = "London",
+        city: str = "",
         nation: str = "",
         lng: Union[int, float] = 0,
         lat: Union[int, float] = 0,
         tz_str: str = "",
         geonames_username: str = "century.boy",
         zodiac_type: ZodiacType = "Tropic",
         online: bool = True,
     ) -> None:
         logger.debug("Starting Kerykeion")
 
+        # We set the swisseph path to the current directory
+        swe.set_ephe_path(
+            str(
+                Path(__file__).parent.absolute() / "sweph"
+            )
+        )
+
+
         self.name = name
         self.year = year
         self.month = month
         self.day = day
         self.hour = hour
         self.minute = minute
         self.city = city
         self.nation = nation
         self.lng = lng
         self.lat = lat
         self.tz_str = tz_str
-        self.__geonames_username = geonames_username
+        self._geonames_username = geonames_username
         self.zodiac_type = zodiac_type
         self.online = online
         self.json_dir = Path.home()
 
+        if not self.city:
+            self.city = "London"
+            logger.warning("No city specified, using London as default")
+
+        if not self.nation:
+            self.nation = "GB"
+            logger.warning("No nation specified, using GB as default")
+
         if (not self.online) and (not lng or not lat or not tz_str):
             raise KerykeionException(
                 "You need to set the coordinates and timezone if you want to use the offline mode!"
             )
 
-        self.julian_day = self.__get_jd()
+        # Initialize everything
+        self._get_utc()
+        self._get_jd()
+        self._planets_degrees_lister()
+        self._planets()
+        self._houses()
 
-        # Get all the calculations
-        self.__get_all()
+        self._planets_in_houses()
+        self._lunar_phase_calc()
 
     def __str__(self) -> str:
         return f"Astrological data for: {self.name}, {self.utc} UTC\nBirth location: {self.city}, Lat {self.lat}, Lon {self.lng}"
 
     def __repr__(self) -> str:
         return f"Astrological data for: {self.name}, {self.utc} UTC\nBirth location: {self.city}, Lat {self.lat}, Lon {self.lng}"
 
-    def __get_tz(self) -> str:
+    def _fetch_tz_from_geonames(self) -> None:
         """Gets the nearest time zone for the calculation"""
         logger.debug("Conneting to Geonames...")
 
         geonames = FetchGeonames(
             self.city,
             self.nation,
-            username=self.__geonames_username,
+            username=self._geonames_username,
         )
         self.city_data: dict[str, str] = geonames.get_serialized_data()
 
         if (
             not "countryCode" in self.city_data
             or not "timezonestr" in self.city_data
             or not "lat" in self.city_data
@@ -184,146 +214,131 @@
             self.lat = 66.0
             logger.info("Polar circle override for houses, using 66 degrees")
 
         elif self.lat < -66.0:
             self.lat = -66.0
             logger.info("Polar circle override for houses, using -66 degrees")
 
-        return self.tz_str
-
-    def __get_utc(self):
+    def _get_utc(self) -> None:
         """Converts local time to utc time."""
+
+        # If the coordinates are not set, get them from geonames.
         if (self.online) and (not self.tz_str or not self.lng or not self.lat):
-            tz = self.__get_tz()
-            local_time = pytz.timezone(tz)
-        else:
-            local_time = pytz.timezone(self.tz_str)
+            self._fetch_tz_from_geonames()
+
+        local_time = pytz.timezone(self.tz_str)
 
         naive_datetime = datetime(self.year, self.month, self.day, self.hour, self.minute, 0)
 
         local_datetime = local_time.localize(naive_datetime, is_dst=None)
-        utc_datetime = local_datetime.astimezone(pytz.utc)
-        self.utc = utc_datetime
-        return self.utc
+        self.utc = local_datetime.astimezone(pytz.utc)
 
-    def __get_jd(self):
+    def _get_jd(self) -> None:
         """Calculates julian day from the utc time."""
-        utc = self.__get_utc()
-        self.utc_time = utc.hour + utc.minute / 60
+        self.utc_time = self.utc.hour + self.utc.minute / 60
         self.local_time = self.hour + self.minute / 60
-        self.julian_day = float(swe.julday(utc.year, utc.month, utc.day, self.utc_time))
-
-        return self.julian_day
+        self.julian_day = float(swe.julday(self.utc.year, self.utc.month, self.utc.day, self.utc_time))
 
-    def __houses(self) -> list:
-        """Calculatetype positions and store them in dictionaries"""
+    def _houses(self) -> None:
+        """Calculate positions and store them in dictionaries"""
         point_type: Literal["Planet", "House"] = "House"
         # creates the list of the house in 360°
         self.houses_degree_ut = swe.houses(self.julian_day, self.lat, self.lng)[0]
         # stores the house in singular dictionaries.
-        self.first_house = calculate_position(self.houses_degree_ut[0], "First House", point_type=point_type)
-        self.second_house = calculate_position(self.houses_degree_ut[1], "Second House", point_type=point_type)
-        self.third_house = calculate_position(self.houses_degree_ut[2], "Third House", point_type=point_type)
-        self.fourth_house = calculate_position(self.houses_degree_ut[3], "Fourth House", point_type=point_type)
-        self.fifth_house = calculate_position(self.houses_degree_ut[4], "Fifth House", point_type=point_type)
-        self.sixth_house = calculate_position(self.houses_degree_ut[5], "Sixth House", point_type=point_type)
-        self.seventh_house = calculate_position(self.houses_degree_ut[6], "Seventh House", point_type=point_type)
-        self.eighth_house = calculate_position(self.houses_degree_ut[7], "Eighth House", point_type=point_type)
-        self.ninth_house = calculate_position(self.houses_degree_ut[8], "Ninth House", point_type=point_type)
-        self.tenth_house = calculate_position(self.houses_degree_ut[9], "Tenth House", point_type=point_type)
-        self.eleventh_house = calculate_position(self.houses_degree_ut[10], "Eleventh House", point_type=point_type)
-        self.twelfth_house = calculate_position(self.houses_degree_ut[11], "Twelfth House", point_type=point_type)
-
-        # creates a list of all the dictionaries of thetype.
-
-        houses_degree = [
-            self.first_house["position"],
-            self.second_house["position"],
-            self.third_house["position"],
-            self.fourth_house["position"],
-            self.fifth_house["position"],
-            self.sixth_house["position"],
-            self.seventh_house["position"],
-            self.eighth_house["position"],
-            self.ninth_house["position"],
-            self.tenth_house["position"],
-            self.eleventh_house["position"],
-            self.twelfth_house["position"],
-        ]
+        self.first_house = calculate_position(self.houses_degree_ut[0], "First_House", point_type=point_type)
+        self.second_house = calculate_position(self.houses_degree_ut[1], "Second_House", point_type=point_type)
+        self.third_house = calculate_position(self.houses_degree_ut[2], "Third_House", point_type=point_type)
+        self.fourth_house = calculate_position(self.houses_degree_ut[3], "Fourth_House", point_type=point_type)
+        self.fifth_house = calculate_position(self.houses_degree_ut[4], "Fifth_House", point_type=point_type)
+        self.sixth_house = calculate_position(self.houses_degree_ut[5], "Sixth_House", point_type=point_type)
+        self.seventh_house = calculate_position(self.houses_degree_ut[6], "Seventh_House", point_type=point_type)
+        self.eighth_house = calculate_position(self.houses_degree_ut[7], "Eighth_House", point_type=point_type)
+        self.ninth_house = calculate_position(self.houses_degree_ut[8], "Ninth_House", point_type=point_type)
+        self.tenth_house = calculate_position(self.houses_degree_ut[9], "Tenth_House", point_type=point_type)
+        self.eleventh_house = calculate_position(self.houses_degree_ut[10], "Eleventh_House", point_type=point_type)
+        self.twelfth_house = calculate_position(self.houses_degree_ut[11], "Twelfth_House", point_type=point_type)
 
-        # return self.houses_list
-        return houses_degree
+        self.houses_list = [
+            self.first_house,
+            self.second_house,
+            self.third_house,
+            self.fourth_house,
+            self.fifth_house,
+            self.sixth_house,
+            self.seventh_house,
+            self.eighth_house,
+            self.ninth_house,
+            self.tenth_house,
+            self.eleventh_house,
+            self.twelfth_house,
+        ]
 
-    def __planets_degrees_lister(self):
+    def _planets_degrees_lister(self):
         """Sidereal or tropic mode."""
-        self.__iflag = swe.FLG_SWIEPH + swe.FLG_SPEED
+        self._iflag = swe.FLG_SWIEPH + swe.FLG_SPEED
 
         if self.zodiac_type == "Sidereal":
-            self.__iflag += swe.FLG_SIDEREAL
+            self._iflag += swe.FLG_SIDEREAL
             mode = "SIDM_FAGAN_BRADLEY"
             swe.set_sid_mode(getattr(swe, mode))
 
-        """Calculates the position of the planets and stores it in a list."""
-
-        sun_deg = swe.calc(self.julian_day, 0, self.__iflag)[0][0]
-        moon_deg = swe.calc(self.julian_day, 1, self.__iflag)[0][0]
-        mercury_deg = swe.calc(self.julian_day, 2, self.__iflag)[0][0]
-        venus_deg = swe.calc(self.julian_day, 3, self.__iflag)[0][0]
-        mars_deg = swe.calc(self.julian_day, 4, self.__iflag)[0][0]
-        jupiter_deg = swe.calc(self.julian_day, 5, self.__iflag)[0][0]
-        saturn_deg = swe.calc(self.julian_day, 6, self.__iflag)[0][0]
-        uranus_deg = swe.calc(self.julian_day, 7, self.__iflag)[0][0]
-        neptune_deg = swe.calc(self.julian_day, 8, self.__iflag)[0][0]
-        pluto_deg = swe.calc(self.julian_day, 9, self.__iflag)[0][0]
-        mean_node_deg = swe.calc(self.julian_day, 10, self.__iflag)[0][0]
-        true_node_deg = swe.calc(self.julian_day, 11, self.__iflag)[0][0]
+        # Calculates the position of the planets and stores it in a list.
+        sun_deg = swe.calc(self.julian_day, 0, self._iflag)[0][0]
+        moon_deg = swe.calc(self.julian_day, 1, self._iflag)[0][0]
+        mercury_deg = swe.calc(self.julian_day, 2, self._iflag)[0][0]
+        venus_deg = swe.calc(self.julian_day, 3, self._iflag)[0][0]
+        mars_deg = swe.calc(self.julian_day, 4, self._iflag)[0][0]
+        jupiter_deg = swe.calc(self.julian_day, 5, self._iflag)[0][0]
+        saturn_deg = swe.calc(self.julian_day, 6, self._iflag)[0][0]
+        uranus_deg = swe.calc(self.julian_day, 7, self._iflag)[0][0]
+        neptune_deg = swe.calc(self.julian_day, 8, self._iflag)[0][0]
+        pluto_deg = swe.calc(self.julian_day, 9, self._iflag)[0][0]
+        mean_node_deg = swe.calc(self.julian_day, 10, self._iflag)[0][0]
+        true_node_deg = swe.calc(self.julian_day, 11, self._iflag)[0][0]
+        chiron_deg = swe.calc(self.julian_day, 15, self._iflag)[0][0]
 
-        # print(swe.calc(self.julian_day, 7, self.__iflag)[3])
-
-        self.planets_degrees = [
+        self.planets_degrees_ut = [
             sun_deg,
             moon_deg,
             mercury_deg,
             venus_deg,
             mars_deg,
             jupiter_deg,
             saturn_deg,
             uranus_deg,
             neptune_deg,
             pluto_deg,
             mean_node_deg,
             true_node_deg,
+            chiron_deg,
         ]
 
-        return self.planets_degrees
-
-    def __planets(self) -> None:
+    def _planets(self) -> None:
         """Defines body positon in signs and information and
         stores them in dictionaries"""
-        self.planets_degrees = self.__planets_degrees_lister()
+
         point_type: Literal["Planet", "House"] = "Planet"
         # stores the planets in singular dictionaries.
-        self.sun = calculate_position(self.planets_degrees[0], "Sun", point_type=point_type)
-        self.moon = calculate_position(self.planets_degrees[1], "Moon", point_type=point_type)
-        self.mercury = calculate_position(self.planets_degrees[2], "Mercury", point_type=point_type)
-        self.venus = calculate_position(self.planets_degrees[3], "Venus", point_type=point_type)
-        self.mars = calculate_position(self.planets_degrees[4], "Mars", point_type=point_type)
-        self.jupiter = calculate_position(self.planets_degrees[5], "Jupiter", point_type=point_type)
-        self.saturn = calculate_position(self.planets_degrees[6], "Saturn", point_type=point_type)
-        self.uranus = calculate_position(self.planets_degrees[7], "Uranus", point_type=point_type)
-        self.neptune = calculate_position(self.planets_degrees[8], "Neptune", point_type=point_type)
-        self.pluto = calculate_position(self.planets_degrees[9], "Pluto", point_type=point_type)
-        self.mean_node = calculate_position(self.planets_degrees[10], "Mean_Node", point_type=point_type)
-        self.true_node = calculate_position(self.planets_degrees[11], "True_Node", point_type=point_type)
+        self.sun = calculate_position(self.planets_degrees_ut[0], "Sun", point_type=point_type)
+        self.moon = calculate_position(self.planets_degrees_ut[1], "Moon", point_type=point_type)
+        self.mercury = calculate_position(self.planets_degrees_ut[2], "Mercury", point_type=point_type)
+        self.venus = calculate_position(self.planets_degrees_ut[3], "Venus", point_type=point_type)
+        self.mars = calculate_position(self.planets_degrees_ut[4], "Mars", point_type=point_type)
+        self.jupiter = calculate_position(self.planets_degrees_ut[5], "Jupiter", point_type=point_type)
+        self.saturn = calculate_position(self.planets_degrees_ut[6], "Saturn", point_type=point_type)
+        self.uranus = calculate_position(self.planets_degrees_ut[7], "Uranus", point_type=point_type)
+        self.neptune = calculate_position(self.planets_degrees_ut[8], "Neptune", point_type=point_type)
+        self.pluto = calculate_position(self.planets_degrees_ut[9], "Pluto", point_type=point_type)
+        self.mean_node = calculate_position(self.planets_degrees_ut[10], "Mean_Node", point_type=point_type)
+        self.true_node = calculate_position(self.planets_degrees_ut[11], "True_Node", point_type=point_type)
+        self.chiron = calculate_position(self.planets_degrees_ut[12], "Chiron", point_type=point_type)
 
-    def __planets_in_houses(self):
+    def _planets_in_houses(self) -> None:
         """Calculates the house of the planet and updates
         the planets dictionary."""
-        self.__planets()
-        self.__houses()
 
         def for_every_planet(planet, planet_deg):
             """Function to do the calculation.
             Args: planet dictionary, planet degree"""
 
             def point_between(p1, p2, p3):
                 """Finds if a point is between two other in a circle
@@ -332,88 +347,90 @@
                 p1_p3 = math.fmod(p3 - p1 + 360, 360)
                 if (p1_p2 <= 180) != (p1_p3 > p1_p2):
                     return True
                 else:
                     return False
 
             if point_between(self.houses_degree_ut[0], self.houses_degree_ut[1], planet_deg) == True:
-                planet["house"] = "First House"
+                planet["house"] = "First_House"
             elif point_between(self.houses_degree_ut[1], self.houses_degree_ut[2], planet_deg) == True:
-                planet["house"] = "Second House"
+                planet["house"] = "Second_House"
             elif point_between(self.houses_degree_ut[2], self.houses_degree_ut[3], planet_deg) == True:
-                planet["house"] = "Third House"
+                planet["house"] = "Third_House"
             elif point_between(self.houses_degree_ut[3], self.houses_degree_ut[4], planet_deg) == True:
-                planet["house"] = "Fourth House"
+                planet["house"] = "Fourth_House"
             elif point_between(self.houses_degree_ut[4], self.houses_degree_ut[5], planet_deg) == True:
-                planet["house"] = "Fifth House"
+                planet["house"] = "Fifth_House"
             elif point_between(self.houses_degree_ut[5], self.houses_degree_ut[6], planet_deg) == True:
-                planet["house"] = "Sixth House"
+                planet["house"] = "Sixth_House"
             elif point_between(self.houses_degree_ut[6], self.houses_degree_ut[7], planet_deg) == True:
-                planet["house"] = "Seventh House"
+                planet["house"] = "Seventh_House"
             elif point_between(self.houses_degree_ut[7], self.houses_degree_ut[8], planet_deg) == True:
-                planet["house"] = "Eighth House"
+                planet["house"] = "Eighth_House"
             elif point_between(self.houses_degree_ut[8], self.houses_degree_ut[9], planet_deg) == True:
-                planet["house"] = "Ninth House"
+                planet["house"] = "Ninth_House"
             elif point_between(self.houses_degree_ut[9], self.houses_degree_ut[10], planet_deg) == True:
-                planet["house"] = "Tenth House"
+                planet["house"] = "Tenth_House"
             elif point_between(self.houses_degree_ut[10], self.houses_degree_ut[11], planet_deg) == True:
-                planet["house"] = "Eleventh House"
+                planet["house"] = "Eleventh_House"
             elif point_between(self.houses_degree_ut[11], self.houses_degree_ut[0], planet_deg) == True:
-                planet["house"] = "Twelfth House"
+                planet["house"] = "Twelfth_House"
             else:
                 planet["house"] = "error!"
 
             return planet
 
-        self.sun = for_every_planet(self.sun, self.planets_degrees[0])
-        self.moon = for_every_planet(self.moon, self.planets_degrees[1])
-        self.mercury = for_every_planet(self.mercury, self.planets_degrees[2])
-        self.venus = for_every_planet(self.venus, self.planets_degrees[3])
-        self.mars = for_every_planet(self.mars, self.planets_degrees[4])
-        self.jupiter = for_every_planet(self.jupiter, self.planets_degrees[5])
-        self.saturn = for_every_planet(self.saturn, self.planets_degrees[6])
-        self.uranus = for_every_planet(self.uranus, self.planets_degrees[7])
-        self.neptune = for_every_planet(self.neptune, self.planets_degrees[8])
-        self.pluto = for_every_planet(self.pluto, self.planets_degrees[9])
-        self.mean_node = for_every_planet(self.mean_node, self.planets_degrees[10])
-        self.true_node = for_every_planet(self.true_node, self.planets_degrees[11])
+        self.sun = for_every_planet(self.sun, self.planets_degrees_ut[0])
+        self.moon = for_every_planet(self.moon, self.planets_degrees_ut[1])
+        self.mercury = for_every_planet(self.mercury, self.planets_degrees_ut[2])
+        self.venus = for_every_planet(self.venus, self.planets_degrees_ut[3])
+        self.mars = for_every_planet(self.mars, self.planets_degrees_ut[4])
+        self.jupiter = for_every_planet(self.jupiter, self.planets_degrees_ut[5])
+        self.saturn = for_every_planet(self.saturn, self.planets_degrees_ut[6])
+        self.uranus = for_every_planet(self.uranus, self.planets_degrees_ut[7])
+        self.neptune = for_every_planet(self.neptune, self.planets_degrees_ut[8])
+        self.pluto = for_every_planet(self.pluto, self.planets_degrees_ut[9])
+        self.mean_node = for_every_planet(self.mean_node, self.planets_degrees_ut[10])
+        self.true_node = for_every_planet(self.true_node, self.planets_degrees_ut[11])
+        self.chiron = for_every_planet(self.chiron, self.planets_degrees_ut[12])
 
-        planets_list = [
+        self.planets_list = [
             self.sun,
             self.moon,
             self.mercury,
             self.venus,
             self.mars,
             self.jupiter,
             self.saturn,
             self.uranus,
             self.neptune,
             self.pluto,
             self.mean_node,
             self.true_node,
+            self.chiron
         ]
 
         # Check in retrograde or not:
         planets_ret = []
-        for p in planets_list:
+        for p in self.planets_list:
             planet_number = get_number_from_name(p["name"])
-            if swe.calc(self.julian_day, planet_number, self.__iflag)[0][3] < 0:
+            if swe.calc(self.julian_day, planet_number, self._iflag)[0][3] < 0:
                 p["retrograde"] = True
             else:
                 p["retrograde"] = False
             planets_ret.append(p)
 
-    def __lunar_phase_calc(self) -> None:
+    def _lunar_phase_calc(self) -> None:
         """Function to calculate the lunar phase"""
 
         # If ther's an error:
         moon_phase, sun_phase = None, None
 
         # anti-clockwise degrees between sun and moon
-        moon, sun = self.planets_degrees[1], self.planets_degrees[0]
+        moon, sun = self.planets_degrees_ut[1], self.planets_degrees_ut[0]
         degrees_between = moon - sun
 
         if degrees_between < 0:
             degrees_between += 360.0
 
         step = 360.0 / 28.0
 
@@ -490,63 +507,24 @@
         lunar_phase_dictionary = {
             "degrees_between_s_m": degrees_between,
             "moon_phase": moon_phase,
             "sun_phase": sun_phase,
             "moon_emoji": moon_emoji(moon_phase),
         }
 
-        self.lunar_phase = LunarPhaseObject(**lunar_phase_dictionary)
-
-    def __make_lists(self):
-        """Internal function to generate the lists"""
-        self.planets_list = [
-            self.sun,
-            self.moon,
-            self.mercury,
-            self.venus,
-            self.mars,
-            self.jupiter,
-            self.saturn,
-            self.uranus,
-            self.neptune,
-            self.pluto,
-            self.mean_node,
-            self.true_node,
-        ]
-
-        self.houses_list = [
-            self.first_house,
-            self.second_house,
-            self.third_house,
-            self.fourth_house,
-            self.fifth_house,
-            self.sixth_house,
-            self.seventh_house,
-            self.eighth_house,
-            self.ninth_house,
-            self.tenth_house,
-            self.eleventh_house,
-            self.twelfth_house,
-        ]
-
-    def __get_all(self):
-        """Gets all data from all the functions"""
-
-        self.__planets_in_houses()
-        self.__lunar_phase_calc()
-        self.__make_lists()
+        self.lunar_phase = LunarPhaseModel(**lunar_phase_dictionary)
 
     def json(self, dump=False, destination_folder: Union[str, None] = None) -> str:
         """
         Dumps the Kerykeion object to a json string foramt,
         if dump=True also dumps to file located in destination
         or the home folder.
         """
 
-        KrData = KerykeionSubject(**self.__dict__)
+        KrData = AstrologicalSubjectModel(**self.__dict__)
         json_string = KrData.json(exclude_none=True)
         print(json_string)
 
         if dump:
             if destination_folder:
                 destination_path = Path(destination_folder)
                 json_path = destination_path / f"{self.name}_kerykeion.json"
@@ -556,26 +534,29 @@
 
             with open(json_path, "w", encoding="utf-8") as file:
                 file.write(json_string)
                 logger.info(f"JSON file dumped in {json_path}.")
 
         return json_string
 
-    def model(self) -> KerykeionSubject:
+    def model(self) -> AstrologicalSubjectModel:
         """
         Creates a Pydantic model of the Kerykeion object.
         """
 
-        return KerykeionSubject(**self.__dict__)
+        return AstrologicalSubjectModel(**self.__dict__)
 
 
 if __name__ == "__main__":
     import json
 
     basicConfig(
         format="%(asctime)s - %(name)s - %(levelname)s - %(message)s",
         level=10,
         force=True,
     )
 
-    johnny = KrInstance("Johnny Depp", 1963, 6, 9, 0, 0, "Owensboro", "US")
+    johnny = AstrologicalSubject("Johnny Depp", 1963, 6, 9, 0, 0, "Owensboro", "US")
     print(json.loads(johnny.json(dump=True)))
+
+    print('\n')
+    print(johnny.chiron)
```

### Comparing `kerykeion-4.0a5/kerykeion/kr_types/kr_literals.py` & `kerykeion-4.0rc1/kerykeion/kr_types/kr_literals.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,36 +1,36 @@
+# -*- coding: utf-8 -*-
 """
     This is part of Kerykeion (C) 2023 Giacomo Battaglia
 """
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
+
 
 from typing import Literal
 
 # Zodiac Types:
 ZodiacType = Literal["Tropic", "Sidereal"]
 
 # Sings:
 Sign = Literal[
     "Ari", "Tau", "Gem", "Can", "Leo", "Vir", "Lib", "Sco", "Sag", "Cap", "Aqu", "Pis"
 ]
 
 Houses = Literal[
-    "First House",
-    "Second House",
-    "Third House",
-    "Fourth House",
-    "Fifth House",
-    "Sixth House",
-    "Seventh House",
-    "Eighth House",
-    "Ninth House",
-    "Tenth House",
-    "Eleventh House",
-    "Twelfth House",
+    "First_House",
+    "Second_House",
+    "Third_House",
+    "Fourth_House",
+    "Fifth_House",
+    "Sixth_House",
+    "Seventh_House",
+    "Eighth_House",
+    "Ninth_House",
+    "Tenth_House",
+    "Eleventh_House",
+    "Twelfth_House",
 ]
 
 Planet = Literal[
     "Sun",
     "Moon",
     "Mercury",
     "Venus",
@@ -38,21 +38,21 @@
     "Jupiter",
     "Saturn",
     "Uranus",
     "Neptune",
     "Pluto",
     "Mean_Node",
     "True_Node",
+    "Chiron",
 ]
 
 Element = Literal["Air", "Fire", "Earth", "Water"]
 
 Quality = Literal[
     "Cardinal",
     "Fixed",
     "Mutable",
 ]
 
-
-ChartType = Literal["Natal", "Composite", "Transit"]
+ChartType = Literal["Natal", "ExternalNatal", "Synastry", "Transit"]
 
 LunarPhaseEmoji = Literal["🌑", "🌒", "🌓", "🌔", "🌕", "🌖", "🌗", "🌘"]
```

### Comparing `kerykeion-4.0a5/kerykeion/kr_types/kr_models.py` & `kerykeion-4.0rc1/kerykeion/kr_types/kr_models.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,20 +1,20 @@
+# -*- coding: utf-8 -*-
 """
     This is part of Kerykeion (C) 2023 Giacomo Battaglia
 """
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
+
 
 from typing import Literal, Union, Optional
 from pydantic import BaseModel
 
 from .kr_literals import *
 
 
-class LunarPhaseObject(BaseModel):
+class LunarPhaseModel(BaseModel):
     degrees_between_s_m: Union[int, float]
     moon_phase: int
     sun_phase: int
     moon_emoji: LunarPhaseEmoji
 
     def __str__(self):
         return (
@@ -49,15 +49,15 @@
     def __delitem__(self, key):
         delattr(self, key)
 
     def get(self, key, default):
         return getattr(self, key, default)
 
 
-class KerykeionPoint(BaseModel):
+class KerykeionPointModel(BaseModel):
     """
     Kerykeion Point Model
     """
 
     name: Union[Planet, Houses]
     quality: Quality
     element: Element
@@ -103,15 +103,15 @@
     def __delitem__(self, key):
         delattr(self, key)
 
     def get(self, key, default):
         return getattr(self, key, default)
 
 
-class KerykeionSubject(BaseModel):
+class AstrologicalSubjectModel(BaseModel):
     # Data
     name: str
     year: int
     month: int
     day: int
     hour: int
     minute: int
@@ -122,49 +122,49 @@
     tz_str: str
     zodiac_type: ZodiacType
     local_time: float
     utc_time: float
     julian_day: float
 
     # Planets
-    sun: KerykeionPoint
-    moon: KerykeionPoint
-    mercury: KerykeionPoint
-    venus: KerykeionPoint
-    mars: KerykeionPoint
-    jupiter: KerykeionPoint
-    saturn: KerykeionPoint
-    uranus: KerykeionPoint
-    neptune: KerykeionPoint
-    pluto: KerykeionPoint
+    sun: KerykeionPointModel
+    moon: KerykeionPointModel
+    mercury: KerykeionPointModel
+    venus: KerykeionPointModel
+    mars: KerykeionPointModel
+    jupiter: KerykeionPointModel
+    saturn: KerykeionPointModel
+    uranus: KerykeionPointModel
+    neptune: KerykeionPointModel
+    pluto: KerykeionPointModel
 
     # Houses
-    first_house: KerykeionPoint
-    second_house: KerykeionPoint
-    third_house: KerykeionPoint
-    fourth_house: KerykeionPoint
-    fifth_house: KerykeionPoint
-    sixth_house: KerykeionPoint
-    seventh_house: KerykeionPoint
-    eighth_house: KerykeionPoint
-    ninth_house: KerykeionPoint
-    tenth_house: KerykeionPoint
-    eleventh_house: KerykeionPoint
-    twelfth_house: KerykeionPoint
+    first_house: KerykeionPointModel
+    second_house: KerykeionPointModel
+    third_house: KerykeionPointModel
+    fourth_house: KerykeionPointModel
+    fifth_house: KerykeionPointModel
+    sixth_house: KerykeionPointModel
+    seventh_house: KerykeionPointModel
+    eighth_house: KerykeionPointModel
+    ninth_house: KerykeionPointModel
+    tenth_house: KerykeionPointModel
+    eleventh_house: KerykeionPointModel
+    twelfth_house: KerykeionPointModel
 
     # Nodes
-    mean_node: KerykeionPoint
-    true_node: KerykeionPoint
+    mean_node: KerykeionPointModel
+    true_node: KerykeionPointModel
 
     # Lunar Phase
-    lunar_phase: LunarPhaseObject
+    lunar_phase: LunarPhaseModel
 
 
 if __name__ == "__main__":
-    sun = KerykeionPoint(
+    sun = KerykeionPointModel(
         name="Sun",
         element="Air",
         quality="Fixed",
         sign="Aqu",
         sign_num=1,
         position=0,
         abs_pos=12.123123,
```

### Comparing `kerykeion-4.0a5/kerykeion/relationship_score.py` & `kerykeion-4.0rc1/kerykeion/relationship_score.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,22 +1,26 @@
+# -*- coding: utf-8 -*-
 """
     This is part of Kerykeion (C) 2023 Giacomo Battaglia
 """
-#!/usr/bin/env python3
-# -*- coding: utf-8 -*-
 
-from kerykeion import KrInstance
-from kerykeion.aspects.composite_aspects import CompositeAspects
-from logging import basicConfig, Logger, getLogger
+from kerykeion import AstrologicalSubject
+from kerykeion.aspects.synastry_aspects import SynastryAspects
+from logging import basicConfig, getLogger, DEBUG
 from pathlib import Path
 from typing import Union
 
 
 logger = getLogger(__name__)
 
+basicConfig(
+    format="%(levelname)s - %(message)s",
+    level=DEBUG,
+)
+
 
 class RelationshipScore:
     """
     Calculates the relevance of the relationship of the two subjects according to
     Ciro Discepolo method.
 
     Results:
@@ -26,206 +30,181 @@
         - From 15 to 20 = Very important relationship
         - From 20 to su = Exceptional relationship
 
     Documentation at:
     http://www.cirodiscepolo.it/Articoli/Discepoloele.htm
 
     Args:
-        first_subject (KrInstance): First subject kerykeion instance
-        second_subject (KrInstance): Second subject kerykeion instance
-        logger (Union[Logger, None], optional): Instance of Logger if None creates new one. Defaults to None.
+        first_subject (AstrologicalSubject): First subject kerykeion instance
+        second_subject (AstrologicalSubject): Second subject kerykeion instance
 
     """
 
-    first_subject: KrInstance
-    second_subject: KrInstance
+    first_subject: AstrologicalSubject
+    second_subject: AstrologicalSubject
     score: int
     is_destiny_sign: bool
     relevant_aspects: list
     relevant_default_aspects: list
 
     def __init__(
         self,
-        first_subject: KrInstance,
-        second_subject: KrInstance,
-        logger: Union[Logger, None] = None,
+        first_subject: AstrologicalSubject,
+        second_subject: AstrologicalSubject,
         new_settings_file: Union[str, Path, None] = None,
     ):
         self.first_subject = first_subject
         self.second_subject = second_subject
         self.score = 0
         self.is_destiny_sign = False
         self.relevant_aspects = []
         self.relevant_default_aspects = []
-        self.__all_composite_aspects = CompositeAspects(
+        self.__all_synastry_aspects = SynastryAspects(
             first_subject, second_subject, new_settings_file=new_settings_file
         ).get_all_aspects()
 
         # Calculates all at initialization
-        self.__get_all()
+        self._get_all()
 
     def __str__(self) -> str:
         return f"CuppleScoreInstance: {self.first_subject.name} and {self.second_subject.name}, score: {self.score}"
 
     def __dict__(self):
         return {
             "first_subject_name": self.first_subject.name,
             "second_subject_name": self.second_subject.name,
             "score": self.score,
             "relevant_aspects": self.relevant_aspects,
             "relevant_default_aspects": self.relevant_default_aspects,
             "is_destiny_sign": self.is_destiny_sign,
         }
 
-    def __log_aspect(self, aspect: dict, points: int) -> None:
+    def _log_aspect(self, aspect: dict, points: int) -> None:
         logger.debug(
             f"{points} Points: {aspect['p1_name']} {aspect['aspect']} {aspect['p2_name']}, rounded orbit: {int(aspect['orbit'])}"
         )
 
-    def __evaluate_destiny_sign(self) -> int:
-        """5 points if is a destiny sign:"""
+    def _evaluate_destiny_sign(self) -> int:
+        """
+        5 points if is a destiny sign:
+        """
         if self.first_subject.sun["quality"] == self.second_subject.sun["quality"]:
             logger.debug(
                 f'5 points: Destiny sign, {self.first_subject.sun["sign"]} and {self.second_subject.sun["sign"]}'
             )
             self.is_destiny_sign = True
             return 5
 
         return 0
 
-    def __check_if_sun_sun_aspect(self, aspect: dict, log: bool = True) -> int:
-        """8 points if Sun conjunction/opposition/square to Sun,
-        11 if diff <= 2 degrees:"""
+    def _check_if_sun_sun_aspect(self, aspect: dict, log: bool = True) -> int:
+        """
+        8 points if Sun conjunction/opposition/square to Sun,
+        11 if diff <= 2 degrees:
+        """
         aspect_types = ["conjunction", "opposition", "square"]
 
-        if (aspect["p1_name"] == "Sun" and aspect["p2_name"] == "Sun") and (
-            aspect["aspect"] in aspect_types
-        ):
+        if (aspect["p1_name"] == "Sun" and aspect["p2_name"] == "Sun") and (aspect["aspect"] in aspect_types):
             self.relevant_default_aspects.append(aspect)
 
             if aspect["orbit"] <= 2:
                 score = 11
 
-                if log:
-                    self.__log_aspect(aspect, score)
-                    self.relevant_aspects.append(
-                        self.__create_aspects_dictionary(aspect, score)
-                    )
+                self._log_aspect(aspect, score)
+                self.relevant_aspects.append(self._create_aspects_dictionary(aspect, score))
 
                 return score
             else:
                 score = 8
 
-                if log:
-                    self.__log_aspect(aspect, score)
-                    self.relevant_aspects.append(
-                        self.__create_aspects_dictionary(aspect, score)
-                    )
+                self._log_aspect(aspect, score)
+                self.relevant_aspects.append(self._create_aspects_dictionary(aspect, score))
 
                 return score
 
         return 0
 
-    def __check_if_sun_moon_conjunction(self, aspect: dict, log: bool = True) -> int:
-        """8 points if Moon conjunction/opposition/square to Moon,
-        11 if diff <= 2 degrees:"""
+    def _check_if_sun_moon_conjunction(self, aspect: dict) -> int:
+        """
+        8 points if Moon conjunction/opposition/square to Moon,
+        11 if diff <= 2 degrees:
+        """
         planets = set(["Moon", "Sun"])
 
-        if (
-            set([aspect["p1_name"], aspect["p2_name"]]) == planets
-            and aspect["aspect"] == "conjunction"
-        ):
+        if set([aspect["p1_name"], aspect["p2_name"]]) == planets and aspect["aspect"] == "conjunction":
             self.relevant_default_aspects.append(aspect)
 
             if aspect["orbit"] <= 2:
                 score = 11
 
-                if log:
-                    self.__log_aspect(aspect, score)
-                    self.relevant_aspects.append(
-                        self.__create_aspects_dictionary(aspect, score)
-                    )
+                self._log_aspect(aspect, score)
+                self.relevant_aspects.append(self._create_aspects_dictionary(aspect, score))
 
                 return score
 
             else:
                 score = 8
-                if log:
-                    self.__log_aspect(aspect, score)
-                    self.relevant_aspects.append(
-                        self.__create_aspects_dictionary(aspect, score)
-                    )
+
+                self._log_aspect(aspect, score)
+                self.relevant_aspects.append(self._create_aspects_dictionary(aspect, score))
 
                 return score
 
         return 0
 
-    def __check_if_sun_moon_asc_aspect(self, aspect: dict, log: bool = True) -> int:
-        planets = ["Sun", "Moon", "First House"]
+    def _check_if_sun_moon_asc_aspect(self, aspect: dict) -> int:
+        planets = ["Sun", "Moon", "First_House"]
 
-        if self.__check_if_sun_sun_aspect(
-            aspect, log=False
-        ) or self.__check_if_sun_moon_conjunction(aspect, log=False):
+        if self._check_if_sun_sun_aspect(aspect) or self._check_if_sun_moon_conjunction(aspect):
             return 0
 
         if aspect["p1_name"] in planets and aspect["p2_name"] in planets:
             self.relevant_default_aspects.append(aspect)
             score = 4
 
-            if log:
-                self.__log_aspect(aspect, score)
-                self.relevant_aspects.append(
-                    self.__create_aspects_dictionary(aspect, score)
-                )
+            self._log_aspect(aspect, score)
+            self.relevant_aspects.append(self._create_aspects_dictionary(aspect, score))
 
             return score
 
         return 0
 
-    def __check_if_venus_mars_aspect(self, aspect: dict, log: bool = True) -> int:
+    def _check_if_venus_mars_aspect(self, aspect: dict) -> int:
         planets = set(["Venus", "Mars"])
         if set([aspect["p1_name"], aspect["p2_name"]]) == planets:
             score = 4
             self.relevant_default_aspects.append(aspect)
 
-            if log:
-                self.__log_aspect(aspect, score)
-                self.relevant_aspects.append(
-                    self.__create_aspects_dictionary(aspect, score)
-                )
+            self._log_aspect(aspect, score)
+            self.relevant_aspects.append(self._create_aspects_dictionary(aspect, score))
 
             return score
 
         return 0
 
-    def __create_aspects_dictionary(self, aspect: dict, score: int) -> dict:
+    def _create_aspects_dictionary(self, aspect: dict, score: int) -> dict:
         return {
             "points": score,
             "p1_name": aspect["p1_name"],
             "p2_name": aspect["p2_name"],
             "aspect": aspect["aspect"],
             "orbit": aspect["orbit"],
         }
 
-    def __get_all(self) -> None:
-        self.score += self.__evaluate_destiny_sign()
+    def _get_all(self) -> None:
+        self.score += self._evaluate_destiny_sign()
 
-        for a in self.__all_composite_aspects:
-            self.score += self.__check_if_sun_sun_aspect(a)
-            self.score += self.__check_if_sun_moon_conjunction(a)
-            self.score += self.__check_if_sun_moon_asc_aspect(a)
-            self.score += self.__check_if_venus_mars_aspect(a)
+        for a in self.__all_synastry_aspects:
+            self.score += self._check_if_sun_sun_aspect(a)
+            self.score += self._check_if_sun_moon_conjunction(a)
+            self.score += self._check_if_sun_moon_asc_aspect(a)
+            self.score += self._check_if_venus_mars_aspect(a)
 
 
 if __name__ == "__main__":
-    basicConfig(
-        format="%(asctime)s - %(name)s - %(levelname)s - %(message)s",
-        level=10,
-        force=True,
-    )
-    lui = KrInstance("John", 1975, 10, 10, 21, 15, "Roma", "IT")
-    lei = KrInstance("Sarah", 1978, 2, 9, 15, 50, "Roma", "IT")
+    lui = AstrologicalSubject("John", 1975, 10, 10, 21, 15, "Roma", "IT")
+    lei = AstrologicalSubject("Sarah", 1978, 2, 9, 15, 50, "Roma", "IT")
 
     score = RelationshipScore(lui, lei)
     print(score.__dict__()["score"])
     print(score.__dict__()["is_destiny_sign"])
     print(score.__dict__()["relevant_aspects"][0])
```

### Comparing `kerykeion-4.0a5/kerykeion/report.py` & `kerykeion-4.0rc1/kerykeion/report.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,22 +1,21 @@
-from kerykeion import KrInstance
+from kerykeion import AstrologicalSubject
 from terminaltables import AsciiTable
 
-
 class Report:
     """
     Create a report for a Kerykeion instance.
     """
 
     report_title: str
     data_table: str
     planets_table: str
     houses_table: str
 
-    def __init__(self, instance: KrInstance):
+    def __init__(self, instance: AstrologicalSubject):
         self.instance = instance
 
         self.get_report_title()
         self.get_data_table()
         self.get_planets_table()
         self.get_houses_table()
 
@@ -80,10 +79,10 @@
         Print the report.
         """
 
         print(self.get_full_report())
 
 
 if __name__ == "__main__":
-    john = KrInstance("John", 1975, 10, 10, 21, 15, "Roma", "IT")
+    john = AstrologicalSubject("John", 1975, 10, 10, 21, 15, "Roma", "IT")
     report = Report(john)
     report.print_report()
```

### Comparing `kerykeion-4.0a5/kerykeion/utilities.py` & `kerykeion-4.0rc1/kerykeion/utilities.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,11 +1,8 @@
-import jsonpickle
-import json
-
-from kerykeion.kr_types import KerykeionPoint, KerykeionException
+from kerykeion.kr_types import KerykeionPointModel, KerykeionException
 from pathlib import Path
 from typing import Union, Literal
 from logging import getLogger
 
 logger = getLogger(__name__)
 
 
@@ -30,26 +27,27 @@
     elif name == "uranus":
         return 7
     elif name == "neptune":
         return 8
     elif name == "pluto":
         return 9
     elif name == "mean_node":
-        return 10  # change!
+        return 10
     elif name == "true_node":
         return 11
+    elif name == "chiron":
+        return 15
     else:
         return int(name)
 
 
 def calculate_position(
     degree: Union[int, float], number_name: str, point_type: Literal["Planet", "House"]
-) -> KerykeionPoint:
-    """Utility function to create a dictionary deviding
-    the houses or the planets list."""
+) -> KerykeionPointModel:
+    """Utility function to create a dictionary dividing the houses or the planets list."""
 
     if degree < 30:
         dictionary = {
             "name": number_name,
             "quality": "Cardinal",
             "element": "Fire",
             "sign": "Ari",
@@ -202,41 +200,9 @@
             "abs_pos": degree,
             "emoji": "♓️",
             "point_type": point_type,
         }
     else:
         raise KerykeionException(f"Error in calculating positions! Degrees: {degree}")
 
-    return KerykeionPoint(**dictionary)
-
-
-def dangerous_json_dump(subject, dump=True, new_output_directory=None):
-    """
-    Dumps the Kerykeion object to a json file located in the home folder.
-    This json file allows the object to be recreated with jsonpickle.
-    It's dangerous since it contains local system information.
-    """
-
-    OUTPUT_DIR = Path.home()
-
-    try:
-        subject.sun
-    except:
-        subject.__get_all()
-
-    if new_output_directory:
-        output_directory_path = Path(new_output_directory)
-        json_dir = new_output_directory / f"{subject.name}_kerykeion.json"
-    else:
-        json_dir = f"{subject.name}_kerykeion.json"
+    return KerykeionPointModel(**dictionary)
 
-    json_string = jsonpickle.encode(subject)
-
-    if dump:
-        json_string = json.loads(json_string.replace("'", '"'))
-
-        with open(json_dir, "w", encoding="utf-8") as file:
-            json.dump(json_string, file, indent=4, sort_keys=True)
-            logger.info(f"JSON file dumped in {json_dir}.")
-    else:
-        pass
-    return json_string
```

### Comparing `kerykeion-4.0a5/pyproject.toml` & `kerykeion-4.0rc1/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [tool.poetry]
 name = "kerykeion"
-version = "4.0a5"
+version = "4.0rc1"
 authors = ["Giacomo Battaglia <battaglia.giacomo@yahoo.it>"]
 description = "A python library for astrology."
-license = "GPL-2.0"
+license = "AGPL-3.0"
 homepage = "https://github.com/g-battaglia/kerykeion"
 repository = "https://github.com/g-battaglia/kerykeion"
 keywords = [
     "astrology",
     "ephemeris",
     "astrology library",
     "birtchart",
@@ -36,15 +36,14 @@
     "Typing :: Typed",
 ]
 
 [tool.poetry.dependencies]
 python = "^3.9"
 pyswisseph = "^2.10.3.1"
 pytz = "^2022.7"
-jsonpickle = "^3.0.1"
 requests = "^2.28.1"
 requests-cache = "^0.9.7"
 pydantic = "^1.10.4"
 terminaltables = "^3.1.10"
 
 [tool.poetry.scripts]
 create-docs = "scripts.docs:main"
@@ -54,18 +53,19 @@
 mypy = "^0.991"
 black = "^22.12.0"
 pdoc = "^12.3.0"
 types-requests = "^2.28.11.7"
 types-pytz = "^2022.7.0.0"
 
 # PyPi Publishing
+poethepoet = "^0.19.0"
 [[tool.poetry.source]]
 name = "test"
 url = "https://test.pypi.org/simple/"
-secondary = true
+priority = 'supplemental'
 
 # MyPy Static Analysis
 [tool.mypy]
 ignore_missing_imports = true
 mypy_path = "kerkeion"
 files = "kerykeion"
 
@@ -80,14 +80,14 @@
 log_date_format = "%Y-%m-%d %H:%M:%S"
 log_format = "%(asctime)s %(levelname)s %(message)s"
 
 # Black Code Formatter
 [tool.black]
 line-length = 120
 
-################
-### Scripts: ###
-################
-
-#-poetry run pytest
-# poetry run mypy
-# python -m pdoc kerykeion -o ./docs
+# Task Runner
+[tool.poe.tasks]
+test = "pytest"
+test-no-capture = "poetry run pytest --show-capture no  "
+lint = "mypy"
+docs = "pdoc kerykeion -o ./docs"
+format = "black kerykeion tests --line-length 120"
```

### Comparing `kerykeion-4.0a5/PKG-INFO` & `kerykeion-4.0rc1/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,36 +1,33 @@
 Metadata-Version: 2.1
 Name: kerykeion
-Version: 4.0a5
+Version: 4.0rc1
 Summary: A python library for astrology.
 Home-page: https://github.com/g-battaglia/kerykeion
-License: GPL-2.0
+License: AGPL-3.0
 Keywords: astrology,ephemeris,astrology library,birtchart,svg,zodiac,zodiac-sing,astronomical-algorithms,synastry,astrology-calculator
 Author: Giacomo Battaglia
 Author-email: battaglia.giacomo@yahoo.it
 Requires-Python: >=3.9,<4.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Information Technology
+Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Classifier: License :: OSI Approved :: GNU General Public License (GPL)
-Classifier: License :: OSI Approved :: GNU General Public License v2 (GPLv2)
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3 :: Only
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.9
 Classifier: Topic :: Scientific/Engineering :: Astronomy
 Classifier: Topic :: Software Development
 Classifier: Topic :: Software Development :: Libraries
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Classifier: Typing :: Typed
-Requires-Dist: jsonpickle (>=3.0.1,<4.0.0)
 Requires-Dist: pydantic (>=1.10.4,<2.0.0)
 Requires-Dist: pyswisseph (>=2.10.3.1,<3.0.0.0)
 Requires-Dist: pytz (>=2022.7,<2023.0)
 Requires-Dist: requests (>=2.28.1,<3.0.0)
 Requires-Dist: requests-cache (>=0.9.7,<0.10.0)
 Requires-Dist: terminaltables (>=3.1.10,<4.0.0)
 Project-URL: Repository, https://github.com/g-battaglia/kerykeion
@@ -60,97 +57,96 @@
 
 &nbsp;
 
 Kerykeion is a python library for Astrology.
 It can calculate all the planet and house position,
 also it can calculate the aspects of a single persone or between two, you can set how many planets you
 need in the settings in the utility module.
-It also can generate an SVG of a birthchart, a composite chart or a transit chart.
+It also can generate an SVG of a birthchart, a synastry chart or a transit chart.
 
 ## Installation
 
-Kerykeion is a *Python 3.9* package, make sure you have *Python 3.9* or above installed on your system.
+Kerykeion is a _Python 3.9_ package, make sure you have _Python 3.9_ or above installed on your system.
 
 ```bash
 pip3 install kerykeion
 ```
 
 ## Usage
 
 Here some examples:
 
 ```python
 
 # Import the main class for creating a kerykeion instance:
-from kerykeion import KrInstance
+from kerykeion import AstrologicalSubject
 
 # Create a kerykeion instance:
 # Args: Name, year, month, day, hour, minuts, city, nation(optional)
-kanye = KrInstance("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
+kanye = AstrologicalSubject("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
 
 # Get the information about the sun in the chart:
 # (The position of the planets always starts at 0)
 kanye.sun
 
 #> {'name': 'Sun', 'quality': 'Mutable', 'element': 'Air', 'sign': 'Gem', 'sign_num': 2, 'pos': 17.598992059774275, 'abs_pos': 77.59899205977428, 'emoji': '♊️', 'house': '12th House', 'retrograde': False}
 
-# Get informations about the first house:
+# Get information about the first house:
 kanye.first_house
 
-#> {'name': 'First House', 'quality': 'Cardinal', 'element': 'Water', 'sign': 'Can', 'sign_num': 3, 'pos': 17.995779673209114, 'abs_pos': 107.99577967320911, 'emoji': '♋️'}
+#> {'name': 'First_House', 'quality': 'Cardinal', 'element': 'Water', 'sign': 'Can', 'sign_num': 3, 'pos': 17.995779673209114, 'abs_pos': 107.99577967320911, 'emoji': '♋️'}
 
 # Get element of the moon sign:
 kanye.moon.get("element")
 
 #> 'Water'
 
 ```
 
 **To avoid connecting to GeoNames (eg. avoiding hourly limit or no internet connection) you should instance kerykeion like this:**
 
 ```python
-kanye = KrInstance(
+kanye = AstrologicalSubject(
     "Kanye", 1977, 6, 8, 8, 45,
     lng=50, lat=50, tz_str="Europe/Rome"
     )
 ```
 
 ## Generate a SVG Chart:
 
 ```python
-from kerykeion import KrInstance, MakeSvgInstance
+from kerykeion import AstrologicalSubject, KerykeionChartSVG
 
-first = KrInstance("Jack", 1990, 6, 15, 15, 15, "Roma")
-second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma")
+first = AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma")
+second = AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma")
 
-# Set the type, it can be Natal, Composite or Transit
+# Set the type, it can be Natal, Synastry or Transit
 
-name = MakeSvgInstance(first, chart_type="Composite", second_obj=second)
+name = KerykeionChartSVG(first, chart_type="Synastry", second_obj=second)
 name.makeSVG()
 print(len(name.aspects_list))
 
 #> Generating kerykeion object for Jack...
 #> Generating kerykeion object for Jane...
 #> Jack birth location: Roma, 41.89193, 12.51133
 #> SVG Generated Correctly
 #> 38
 
 ```
 
-![alt text](http://centuryboy.altervista.org/JackComposite_Chart.svg)
-
+![alt text](http://centuryboy.altervista.org/JackSynastry_Chart.svg)
 
 # Report
 
 To print a report of all the data:
 
 ```python
-from kerykeion import Report, KrInstance
+from kerykeion import Report, AstrologicalSubject
 
-kanye = KrInstance("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
+kanye = AstrologicalSubject("Kanye", 1977, 6, 8, 8, 45, "Atlanta")
 report = Report(kanye)
 report.print_report()
 
 ```
 
 Returns:
 
@@ -160,62 +156,62 @@
 | Date     | Time | Location    | Longitude | Latitude |
 +----------+------+-------------+-----------+----------+
 | 8/6/1977 | 8:45 | Atlanta, US | -84.38798 | 33.749   |
 +----------+------+-------------+-----------+----------+
 +-----------+------+-------+------+----------------+
 | Planet    | Sign | Pos.  | Ret. | House          |
 +-----------+------+-------+------+----------------+
-| Sun       | Gem  | 17.6  | -    | Twelfth House  |
-| Moon      | Pis  | 16.43 | -    | Ninth House    |
-| Mercury   | Tau  | 26.29 | -    | Eleventh House |
-| Venus     | Tau  | 2.03  | -    | Tenth House    |
-| Mars      | Tau  | 1.79  | -    | Tenth House    |
-| Jupiter   | Gem  | 14.61 | -    | Eleventh House |
-| Saturn    | Leo  | 12.8  | -    | Second House   |
-| Uranus    | Sco  | 8.27  | R    | Fourth House   |
-| Neptune   | Sag  | 14.69 | R    | Fifth House    |
-| Pluto     | Lib  | 11.45 | R    | Fourth House   |
-| Mean_Node | Lib  | 21.49 | R    | Fourth House   |
-| True_Node | Lib  | 22.82 | R    | Fourth House   |
+| Sun       | Gem  | 17.6  | -    | Twelfth_House  |
+| Moon      | Pis  | 16.43 | -    | Ninth_House    |
+| Mercury   | Tau  | 26.29 | -    | Eleventh_House |
+| Venus     | Tau  | 2.03  | -    | Tenth_House    |
+| Mars      | Tau  | 1.79  | -    | Tenth_House    |
+| Jupiter   | Gem  | 14.61 | -    | Eleventh_House |
+| Saturn    | Leo  | 12.8  | -    | Second_House   |
+| Uranus    | Sco  | 8.27  | R    | Fourth_House   |
+| Neptune   | Sag  | 14.69 | R    | Fifth_House    |
+| Pluto     | Lib  | 11.45 | R    | Fourth_House   |
+| Mean_Node | Lib  | 21.49 | R    | Fourth_House   |
+| True_Node | Lib  | 22.82 | R    | Fourth_House   |
 +-----------+------+-------+------+----------------+
 +----------------+------+----------+
 | House          | Sign | Position |
 +----------------+------+----------+
-| First House    | Can  | 18.0     |
-| Second House   | Leo  | 9.51     |
-| Third House    | Vir  | 4.02     |
-| Fourth House   | Lib  | 3.98     |
-| Fifth House    | Sco  | 9.39     |
-| Sixth House    | Sag  | 15.68    |
-| Seventh House  | Cap  | 18.0     |
-| Eighth House   | Aqu  | 9.51     |
-| Ninth House    | Pis  | 4.02     |
-| Tenth House    | Ari  | 3.98     |
-| Eleventh House | Tau  | 9.39     |
-| Twelfth House  | Gem  | 15.68    |
+| First_House    | Can  | 18.0     |
+| Second_House   | Leo  | 9.51     |
+| Third_House    | Vir  | 4.02     |
+| Fourth_House   | Lib  | 3.98     |
+| Fifth_House    | Sco  | 9.39     |
+| Sixth_House    | Sag  | 15.68    |
+| Seventh_House  | Cap  | 18.0     |
+| Eighth_House   | Aqu  | 9.51     |
+| Ninth_House    | Pis  | 4.02     |
+| Tenth_House    | Ari  | 3.98     |
+| Eleventh_House | Tau  | 9.39     |
+| Twelfth_House  | Gem  | 15.68    |
 +----------------+------+----------+
 
 ```
 
 And if you want to export it to a file:
 
 ```bash
-$ python3 your_script_name.py > file.txt 
+$ python3 your_script_name.py > file.txt
 ```
 
 ## Other exeples of possibles usecase
 
 ```python
 # Get all aspects between two persons:
 
-from kerykeion import CompositeAspects, KrInstance
-first = KrInstance("Jack", 1990, 6, 15, 15, 15, "Roma")
-second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma")
+from kerykeion import SynastryAspects, AstrologicalSubject
+first = AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma")
+second = AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma")
 
-name = CompositeAspects(first, second)
+name = SynastryAspects(first, second)
 aspect_list = name.get_relevant_aspects()
 print(aspect_list[0])
 
 #> Generating kerykeion object for Jack...
 #> Generating kerykeion object for Jane...
 #> {'p1_name': 'Sun', 'p1_abs_pos': 84.17867971515636, 'p2_name': 'Sun', 'p2_abs_pos': 211.90472999502984, 'aspect': 'trine', 'orbit': 7.726050279873476, 'aspect_degrees': 120, 'color': '#36d100', 'aid': 6, 'diff': 127.72605027987348, 'p1': 0, 'p2': 0}
```

#### html2text {}

```diff
@@ -1,92 +1,92 @@
-Metadata-Version: 2.1 Name: kerykeion Version: 4.0a5 Summary: A python library
+Metadata-Version: 2.1 Name: kerykeion Version: 4.0rc1 Summary: A python library
 for astrology. Home-page: https://github.com/g-battaglia/kerykeion License:
-GPL-2.0 Keywords: astrology,ephemeris,astrology
+AGPL-3.0 Keywords: astrology,ephemeris,astrology
 library,birtchart,svg,zodiac,zodiac-sing,astronomical-
 algorithms,synastry,astrology-calculator Author: Giacomo Battaglia Author-
 email: battaglia.giacomo@yahoo.it Requires-Python: >=3.9,<4.0 Classifier:
 Development Status :: 5 - Production/Stable Classifier: Intended Audience ::
 Developers Classifier: Intended Audience :: Information Technology Classifier:
-License :: OSI Approved :: GNU General Public License (GPL) Classifier: License
-:: OSI Approved :: GNU General Public License v2 (GPLv2) Classifier: Operating
-System :: OS Independent Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.9 Classifier: Programming
+License :: OSI Approved :: GNU Affero General Public License v3 Classifier:
+License :: OSI Approved :: GNU General Public License (GPL) Classifier:
+Operating System :: OS Independent Classifier: Programming Language :: Python
+:: 3 Classifier: Programming Language :: Python :: 3.9 Classifier: Programming
 Language :: Python :: 3.10 Classifier: Programming Language :: Python :: 3.11
-Classifier: Programming Language :: Python :: 3 :: Only Classifier: Programming
-Language :: Python :: 3.10 Classifier: Programming Language :: Python :: 3.9
-Classifier: Topic :: Scientific/Engineering :: Astronomy Classifier: Topic ::
-Software Development Classifier: Topic :: Software Development :: Libraries
-Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Classifier: Typing :: Typed Requires-Dist: jsonpickle (>=3.0.1,<4.0.0)
+Classifier: Programming Language :: Python :: 3 :: Only Classifier: Topic ::
+Scientific/Engineering :: Astronomy Classifier: Topic :: Software Development
+Classifier: Topic :: Software Development :: Libraries Classifier: Topic ::
+Software Development :: Libraries :: Python Modules Classifier: Typing :: Typed
 Requires-Dist: pydantic (>=1.10.4,<2.0.0) Requires-Dist: pyswisseph
 (>=2.10.3.1,<3.0.0.0) Requires-Dist: pytz (>=2022.7,<2023.0) Requires-Dist:
 requests (>=2.28.1,<3.0.0) Requires-Dist: requests-cache (>=0.9.7,<0.10.0)
 Requires-Dist: terminaltables (>=3.1.10,<4.0.0) Project-URL: Repository, https:
 //github.com/g-battaglia/kerykeion Description-Content-Type: text/markdown
                             ****** Kerykeion ******
  [contributors] [stars] [forks] [visitors] [Package_version] [Supported_Python
                                    versions]
   Kerykeion is a python library for Astrology. It can calculate all the planet
 and house position, also it can calculate the aspects of a single persone or
 between two, you can set how many planets you need in the settings in the
-utility module. It also can generate an SVG of a birthchart, a composite chart
-or a transit chart. ## Installation Kerykeion is a *Python 3.9* package, make
-sure you have *Python 3.9* or above installed on your system. ```bash pip3
+utility module. It also can generate an SVG of a birthchart, a synastry chart
+or a transit chart. ## Installation Kerykeion is a _Python 3.9_ package, make
+sure you have _Python 3.9_ or above installed on your system. ```bash pip3
 install kerykeion ``` ## Usage Here some examples: ```python # Import the main
-class for creating a kerykeion instance: from kerykeion import KrInstance #
-Create a kerykeion instance: # Args: Name, year, month, day, hour, minuts,
-city, nation(optional) kanye = KrInstance("Kanye", 1977, 6, 8, 8, 45,
-"Atlanta") # Get the information about the sun in the chart: # (The position of
-the planets always starts at 0) kanye.sun #> {'name': 'Sun', 'quality':
-'Mutable', 'element': 'Air', 'sign': 'Gem', 'sign_num': 2, 'pos':
+class for creating a kerykeion instance: from kerykeion import
+AstrologicalSubject # Create a kerykeion instance: # Args: Name, year, month,
+day, hour, minuts, city, nation(optional) kanye = AstrologicalSubject("Kanye",
+1977, 6, 8, 8, 45, "Atlanta") # Get the information about the sun in the chart:
+# (The position of the planets always starts at 0) kanye.sun #> {'name': 'Sun',
+'quality': 'Mutable', 'element': 'Air', 'sign': 'Gem', 'sign_num': 2, 'pos':
 17.598992059774275, 'abs_pos': 77.59899205977428, 'emoji': 'âï¸', 'house':
-'12th House', 'retrograde': False} # Get informations about the first house:
-kanye.first_house #> {'name': 'First House', 'quality': 'Cardinal', 'element':
+'12th House', 'retrograde': False} # Get information about the first house:
+kanye.first_house #> {'name': 'First_House', 'quality': 'Cardinal', 'element':
 'Water', 'sign': 'Can', 'sign_num': 3, 'pos': 17.995779673209114, 'abs_pos':
 107.99577967320911, 'emoji': 'âï¸'} # Get element of the moon sign:
 kanye.moon.get("element") #> 'Water' ``` **To avoid connecting to GeoNames (eg.
 avoiding hourly limit or no internet connection) you should instance kerykeion
-like this:** ```python kanye = KrInstance( "Kanye", 1977, 6, 8, 8, 45, lng=50,
-lat=50, tz_str="Europe/Rome" ) ``` ## Generate a SVG Chart: ```python from
-kerykeion import KrInstance, MakeSvgInstance first = KrInstance("Jack", 1990,
-6, 15, 15, 15, "Roma") second = KrInstance("Jane", 1991, 10, 25, 21, 00,
-"Roma") # Set the type, it can be Natal, Composite or Transit name =
-MakeSvgInstance(first, chart_type="Composite", second_obj=second) name.makeSVG
-() print(len(name.aspects_list)) #> Generating kerykeion object for Jack... #>
-Generating kerykeion object for Jane... #> Jack birth location: Roma, 41.89193,
-12.51133 #> SVG Generated Correctly #> 38 ``` ![alt text](http://
-centuryboy.altervista.org/JackComposite_Chart.svg) # Report To print a report
-of all the data: ```python from kerykeion import Report, KrInstance kanye =
-KrInstance("Kanye", 1977, 6, 8, 8, 45, "Atlanta") report = Report(kanye)
-report.print_report() ``` Returns: ``` +- Kerykeion report for Kanye -+ +------
-----+------+-------------+-----------+----------+ | Date | Time | Location |
-Longitude | Latitude | +----------+------+-------------+-----------+----------
-+ | 8/6/1977 | 8:45 | Atlanta, US | -84.38798 | 33.749 | +----------+------+---
-----------+-----------+----------+ +-----------+------+-------+------+---------
--------+ | Planet | Sign | Pos. | Ret. | House | +-----------+------+-------+--
-----+----------------+ | Sun | Gem | 17.6 | - | Twelfth House | | Moon | Pis |
-16.43 | - | Ninth House | | Mercury | Tau | 26.29 | - | Eleventh House | |
-Venus | Tau | 2.03 | - | Tenth House | | Mars | Tau | 1.79 | - | Tenth House |
-| Jupiter | Gem | 14.61 | - | Eleventh House | | Saturn | Leo | 12.8 | - |
-Second House | | Uranus | Sco | 8.27 | R | Fourth House | | Neptune | Sag |
-14.69 | R | Fifth House | | Pluto | Lib | 11.45 | R | Fourth House | |
-Mean_Node | Lib | 21.49 | R | Fourth House | | True_Node | Lib | 22.82 | R |
-Fourth House | +-----------+------+-------+------+----------------+ +----------
-------+------+----------+ | House | Sign | Position | +----------------+------
-+----------+ | First House | Can | 18.0 | | Second House | Leo | 9.51 | | Third
-House | Vir | 4.02 | | Fourth House | Lib | 3.98 | | Fifth House | Sco | 9.39 |
-| Sixth House | Sag | 15.68 | | Seventh House | Cap | 18.0 | | Eighth House |
-Aqu | 9.51 | | Ninth House | Pis | 4.02 | | Tenth House | Ari | 3.98 | |
-Eleventh House | Tau | 9.39 | | Twelfth House | Gem | 15.68 | +----------------
-+------+----------+ ``` And if you want to export it to a file: ```bash $
-python3 your_script_name.py > file.txt ``` ## Other exeples of possibles
-usecase ```python # Get all aspects between two persons: from kerykeion import
-CompositeAspects, KrInstance first = KrInstance("Jack", 1990, 6, 15, 15, 15,
-"Roma") second = KrInstance("Jane", 1991, 10, 25, 21, 00, "Roma") name =
-CompositeAspects(first, second) aspect_list = name.get_relevant_aspects() print
+like this:** ```python kanye = AstrologicalSubject( "Kanye", 1977, 6, 8, 8, 45,
+lng=50, lat=50, tz_str="Europe/Rome" ) ``` ## Generate a SVG Chart: ```python
+from kerykeion import AstrologicalSubject, KerykeionChartSVG first =
+AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma") second =
+AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma") # Set the type, it
+can be Natal, Synastry or Transit name = KerykeionChartSVG(first,
+chart_type="Synastry", second_obj=second) name.makeSVG() print(len
+(name.aspects_list)) #> Generating kerykeion object for Jack... #> Generating
+kerykeion object for Jane... #> Jack birth location: Roma, 41.89193, 12.51133
+#> SVG Generated Correctly #> 38 ``` ![alt text](http://
+centuryboy.altervista.org/JackSynastry_Chart.svg) # Report To print a report of
+all the data: ```python from kerykeion import Report, AstrologicalSubject kanye
+= AstrologicalSubject("Kanye", 1977, 6, 8, 8, 45, "Atlanta") report = Report
+(kanye) report.print_report() ``` Returns: ``` +- Kerykeion report for Kanye -
++ +----------+------+-------------+-----------+----------+ | Date | Time |
+Location | Longitude | Latitude | +----------+------+-------------+-----------
++----------+ | 8/6/1977 | 8:45 | Atlanta, US | -84.38798 | 33.749 | +----------
++------+-------------+-----------+----------+ +-----------+------+-------+-----
+-+----------------+ | Planet | Sign | Pos. | Ret. | House | +-----------+------
++-------+------+----------------+ | Sun | Gem | 17.6 | - | Twelfth_House | |
+Moon | Pis | 16.43 | - | Ninth_House | | Mercury | Tau | 26.29 | - |
+Eleventh_House | | Venus | Tau | 2.03 | - | Tenth_House | | Mars | Tau | 1.79 |
+- | Tenth_House | | Jupiter | Gem | 14.61 | - | Eleventh_House | | Saturn | Leo
+| 12.8 | - | Second_House | | Uranus | Sco | 8.27 | R | Fourth_House | |
+Neptune | Sag | 14.69 | R | Fifth_House | | Pluto | Lib | 11.45 | R |
+Fourth_House | | Mean_Node | Lib | 21.49 | R | Fourth_House | | True_Node | Lib
+| 22.82 | R | Fourth_House | +-----------+------+-------+------+---------------
+-+ +----------------+------+----------+ | House | Sign | Position | +----------
+------+------+----------+ | First_House | Can | 18.0 | | Second_House | Leo |
+9.51 | | Third_House | Vir | 4.02 | | Fourth_House | Lib | 3.98 | | Fifth_House
+| Sco | 9.39 | | Sixth_House | Sag | 15.68 | | Seventh_House | Cap | 18.0 | |
+Eighth_House | Aqu | 9.51 | | Ninth_House | Pis | 4.02 | | Tenth_House | Ari |
+3.98 | | Eleventh_House | Tau | 9.39 | | Twelfth_House | Gem | 15.68 | +-------
+---------+------+----------+ ``` And if you want to export it to a file:
+```bash $ python3 your_script_name.py > file.txt ``` ## Other exeples of
+possibles usecase ```python # Get all aspects between two persons: from
+kerykeion import SynastryAspects, AstrologicalSubject first =
+AstrologicalSubject("Jack", 1990, 6, 15, 15, 15, "Roma") second =
+AstrologicalSubject("Jane", 1991, 10, 25, 21, 00, "Roma") name =
+SynastryAspects(first, second) aspect_list = name.get_relevant_aspects() print
 (aspect_list[0]) #> Generating kerykeion object for Jack... #> Generating
 kerykeion object for Jane... #> {'p1_name': 'Sun', 'p1_abs_pos':
 84.17867971515636, 'p2_name': 'Sun', 'p2_abs_pos': 211.90472999502984,
 'aspect': 'trine', 'orbit': 7.726050279873476, 'aspect_degrees': 120, 'color':
 '#36d100', 'aid': 6, 'diff': 127.72605027987348, 'p1': 0, 'p2': 0} ``` ##
 Documentation Most of the functions and the classes are self documented by the
 types and have docstrings. An auto-generated documentation [is available here]
```

