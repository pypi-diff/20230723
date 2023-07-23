# Comparing `tmp/divideandscan-0.3.8.tar.gz` & `tmp/divideandscan-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "divideandscan-0.3.8.tar", max compression
+gzip compressed data, was "divideandscan-1.0.0.tar", max compression
```

## Comparing `divideandscan-0.3.8.tar` & `divideandscan-1.0.0.tar`

### file list

```diff
@@ -1,19 +1,19 @@
--rw-r--r--   0        0        0     1320 2023-07-21 11:08:15.000629 divideandscan-0.3.8/LICENSE
--rw-r--r--   0        0        0    14973 2023-07-21 11:08:15.000629 divideandscan-0.3.8/README.md
--rw-r--r--   0        0        0       29 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/__init__.py
--rw-r--r--   0        0        0     3895 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/common.py
--rwxr-xr-x   0        0        0    12593 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/divideandscan.py
--rw-r--r--   0        0        0     1406 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/dns.py
--rw-r--r--   0        0        0     7856 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/drawnmap.py
--rw-r--r--   0        0        0     2314 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/parsenmap.py
--rw-r--r--   0        0        0     1737 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/parsers/__init__.py
--rw-r--r--   0        0        0      669 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/parsers/masscan.py
--rw-r--r--   0        0        0      599 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/parsers/naabu.py
--rw-r--r--   0        0        0      868 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/parsers/nimscan.py
--rw-r--r--   0        0        0      648 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/parsers/nmap.py
--rw-r--r--   0        0        0      660 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/parsers/rustscan.py
--rw-r--r--   0        0        0      590 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/parsers/sx.py
--rw-r--r--   0        0        0     9261 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/report.py
--rw-r--r--   0        0        0     7224 2023-07-21 11:08:15.000629 divideandscan-0.3.8/das/scan.py
--rw-r--r--   0        0        0     1139 2023-07-21 11:08:15.004629 divideandscan-0.3.8/pyproject.toml
--rw-r--r--   0        0        0    16143 1970-01-01 00:00:00.000000 divideandscan-0.3.8/PKG-INFO
+-rw-r--r--   0        0        0     1320 2023-07-23 10:57:37.040373 divideandscan-1.0.0/LICENSE
+-rw-r--r--   0        0        0    15194 2023-07-23 10:57:37.040373 divideandscan-1.0.0/README.md
+-rw-r--r--   0        0        0       29 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/__init__.py
+-rw-r--r--   0        0        0     4286 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/common.py
+-rwxr-xr-x   0        0        0    14385 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/divideandscan.py
+-rw-r--r--   0        0        0     2614 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/dns.py
+-rw-r--r--   0        0        0     7856 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/drawnmap.py
+-rw-r--r--   0        0        0     2314 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsenmap.py
+-rw-r--r--   0        0        0     1723 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/__init__.py
+-rw-r--r--   0        0        0      665 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/masscan.py
+-rw-r--r--   0        0        0      596 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/naabu.py
+-rw-r--r--   0        0        0      865 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/nimscan.py
+-rw-r--r--   0        0        0      645 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/nmap.py
+-rw-r--r--   0        0        0      661 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/rustscan.py
+-rw-r--r--   0        0        0      587 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/sx.py
+-rw-r--r--   0        0        0     9261 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/report.py
+-rw-r--r--   0        0        0     7224 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/scan.py
+-rw-r--r--   0        0        0     1139 2023-07-23 10:57:37.040373 divideandscan-1.0.0/pyproject.toml
+-rw-r--r--   0        0        0    16364 1970-01-01 00:00:00.000000 divideandscan-1.0.0/PKG-INFO
```

### Comparing `divideandscan-0.3.8/LICENSE` & `divideandscan-1.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `divideandscan-0.3.8/README.md` & `divideandscan-1.0.0/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 </p>
 
 <p align="center">
   <strong>Divide <strike>Et Impera</strike> And Scan (and also merge the scan results)</strong>
 </p>
 
 <p align="center">
-  <a href="https://github.com/snovvcrash/DivideAndScan/blob/main/pyproject.toml#L3"><img src="https://img.shields.io/badge/version-0.3.8-success" alt="version" /></a>
+  <a href="https://github.com/snovvcrash/DivideAndScan/blob/main/pyproject.toml#L3"><img src="https://img.shields.io/badge/version-1.0.0-success" alt="version" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/search?l=python"><img src="https://img.shields.io/badge/python-3.9-blue?logo=python&logoColor=white" alt="python" /></a>
   <a href="https://www.codacy.com/gh/snovvcrash/DivideAndScan/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=snovvcrash/DivideAndScan&amp;utm_campaign=Badge_Grade"><img src="https://app.codacy.com/project/badge/Grade/35f0bdfece9846d7aab3888b01642813" alt="codacy" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-pypi.yml"><img src="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-pypi.yml/badge.svg" alt="pypi" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-docker-hub.yml"><img src="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-docker-hub.yml/badge.svg" alt="docker" /></a>
 </p>
 
 ---
@@ -100,14 +100,22 @@
 
 ```bash
 sudo mkdir /opt/sx
 sudo eget -s linux/amd64 v-byte-cpu/sx --to /opt/sx
 sudo ln -sv /opt/sx/sx /usr/local/bin/sx
 ```
 
+#### dnsx
+
+```bash
+sudo mkdir /opt/pd
+sudo eget -s linux/amd64 projectdiscovery/dnsx --to /opt/pd
+sudo ln -sv /opt/pd/dnsx /usr/local/bin/dnsx
+```
+
 ### Installation
 
 DivideAndScan is available on PyPI as `divideandscan`, though I recommend installing it from GitHub with [pipx](https://github.com/pipxproject/pipx) in order to always have the bleeding-edge version:
 
 ```console
 ~$ pipx install -f "git+https://github.com/snovvcrash/DivideAndScan.git"
 ~$ das
@@ -316,31 +324,32 @@
 
         return (self.portscan_out, len(hosts))
 ```
 
 ## Help
 
 ```
-usage: das [-h] [-db DB] {add,scan,dns,report,parse,draw,tree,help} ...
+usage: das [-h] [-db DB] {db,add,scan,dns,report,parse,draw,tree,help} ...
 
  -----------------------------------------------------------------------------------------------
 |  ________  .__      .__    .___        _____              .____________                       |
 |  \______ \ |__|__  _|__| __| _/____   /  _  \   ____    __| _/   _____/ ____ _____    ____    |
 |   |    |  \|  \  \/ /  |/ __ |/ __ \ /  /_\  \ /    \  / __ |\_____  \_/ ___\\__  \  /    \   |
 |   |    `   \  |\   /|  / /_/ \  ___//    |    \   |  \/ /_/ |/        \  \___ / __ \|   |  \  |
 |  /_______  /__| \_/ |__\____ |\___  >____|__  /___|  /\____ /_______  /\___  >____  /___|  /  |
 |          \/                 \/    \/        \/     \/      \/       \/     \/     \/     \/   |
 |  {@snovvcrash}            {https://github.com/snovvcrash/DivideAndScan}             {vX.Y.Z}  |
  -----------------------------------------------------------------------------------------------
 
 positional arguments:
-  {add,scan,dns,report,parse,draw,tree,help}
+  {db,add,scan,dns,report,parse,draw,tree,help}
+    db                  utilities for manual DB manipulations
     add                 run a full port scan and add the output to DB
     scan                run targeted Nmap scans against hosts and ports from DB
-    dns                 resolve "A" domain names into IP addresses and update DB items with them
+    dns                 map domain names from an input file to corresponding IP addresses from the DB
     report              merge separate Nmap outputs into a single report (https://github.com/CBHue/nMap_Merger)
     parse               parse raw Nmap XML reports by service names and print entries in format {service}://{host}:{port}}
     draw                visualize Nmap XML reports (https://github.com/jor6PS/DrawNmap)
     tree                show contents of the ~/.das/ directory using tree
     help                show builtin --help dialog of a selected port scanner
 
 options:
```

#### html2text {}

```diff
@@ -39,37 +39,39 @@
 fe8628396616c4bf7a3e25f2c9d1acc2f36af0c0/rustscan-ports-top1000.toml -O /
 root/.rustscan.toml ``` #### Naabu ```bash sudo mkdir /opt/naabu sudo eget -
 s linux/amd64 projectdiscovery/naabu --to /opt/naabu sudo ln -sv /opt/naabu/
 naabu /usr/local/bin/naabu ``` #### NimScan ```bash sudo mkdir /opt/nimscan
 sudo eget -a NimScan elddy/NimScan --to /opt/nimscan sudo ln -sv /opt/nimscan/
 nimscan /usr/local/bin/nimscan ``` #### sx ```bash sudo mkdir /opt/sx sudo eget
 -s linux/amd64 v-byte-cpu/sx --to /opt/sx sudo ln -sv /opt/sx/sx /usr/local/
-bin/sx ``` ### Installation DivideAndScan is available on PyPI as
-`divideandscan`, though I recommend installing it from GitHub with [pipx]
-(https://github.com/pipxproject/pipx) in order to always have the bleeding-edge
-version: ```console ~$ pipx install -f "git+https://github.com/snovvcrash/
-DivideAndScan.git" ~$ das ``` For debbugging purposes you can set up a dev
-environment with [poetry](https://github.com/python-poetry/poetry): ```console
-~$ git clone --recurse-submodules https://github.com/snovvcrash/DivideAndScan
-~$ cd DivideAndScan ~$ poetry install ~$ poetry run das ``` ð **Note:**
-DivideAndScan uses sudo to run all the port scanners, so it will ask for the
-password when scanning commands are invoked. ### Using from Docker [!
-[dockeri.co](https://dockeri.co/image/snovvcrash/divideandscan)](https://
-hub.docker.com/r/snovvcrash/divideandscan) You can run DivideAndScan in a
-Docker container as follows: ```console ~$ docker run --rm -it --name das -
-v ~/.das:/root/.das -v `pwd`:/app -p 8050:8050 snovvcrash/divideandscan ```
-Since the tool requires some input data and produces some output data, you
-should specify your current working directory as the mount point at `/app`
-within the container. Also publishing port 8050 on host allows to access the
-[Dash](https://github.com/plotly/dash) app used for Nmap reports visualization.
-You may want to set an alias to make the base command shorter: ```console ~$
-alias das='docker run --rm -it --name das -v ~/.das:/root/.das -v `pwd`:/app -
-p 8050:8050 snovvcrash/divideandscan' ~$ das ``` ## How to Use ![how-to-
-use.png](https://user-images.githubusercontent.com/23141800/113610915-6fae9b80-
-9656-11eb-8b1a-db503dd43861.png) ### 1. Filling the DB
+bin/sx ``` #### dnsx ```bash sudo mkdir /opt/pd sudo eget -s linux/amd64
+projectdiscovery/dnsx --to /opt/pd sudo ln -sv /opt/pd/dnsx /usr/local/bin/dnsx
+``` ### Installation DivideAndScan is available on PyPI as `divideandscan`,
+though I recommend installing it from GitHub with [pipx](https://github.com/
+pipxproject/pipx) in order to always have the bleeding-edge version: ```console
+~$ pipx install -f "git+https://github.com/snovvcrash/DivideAndScan.git" ~$ das
+``` For debbugging purposes you can set up a dev environment with [poetry]
+(https://github.com/python-poetry/poetry): ```console ~$ git clone --recurse-
+submodules https://github.com/snovvcrash/DivideAndScan ~$ cd DivideAndScan ~$
+poetry install ~$ poetry run das ``` ð **Note:** DivideAndScan uses sudo to
+run all the port scanners, so it will ask for the password when scanning
+commands are invoked. ### Using from Docker [![dockeri.co](https://dockeri.co/
+image/snovvcrash/divideandscan)](https://hub.docker.com/r/snovvcrash/
+divideandscan) You can run DivideAndScan in a Docker container as follows:
+```console ~$ docker run --rm -it --name das -v ~/.das:/root/.das -v `pwd`:/app
+-p 8050:8050 snovvcrash/divideandscan ``` Since the tool requires some input
+data and produces some output data, you should specify your current working
+directory as the mount point at `/app` within the container. Also publishing
+port 8050 on host allows to access the [Dash](https://github.com/plotly/dash)
+app used for Nmap reports visualization. You may want to set an alias to make
+the base command shorter: ```console ~$ alias das='docker run --rm -it --name
+das -v ~/.das:/root/.das -v `pwd`:/app -p 8050:8050 snovvcrash/divideandscan'
+~$ das ``` ## How to Use ![how-to-use.png](https://user-
+images.githubusercontent.com/23141800/113610915-6fae9b80-9656-11eb-8b1a-
+db503dd43861.png) ### 1. Filling the DB
 Provide the `add` module a command for a fast port scanner to discover open
 ports in a desired range. â ï¸ **Warning:** please, make sure that you
 understand what you're doing, because nearly all port scanning tools [can
 damage the system being tested](https://github.com/RustScan/RustScan/wiki/
 Usage#%EF%B8%8F-warning) if used improperly. ```console # Nmap, -v flag is
 always required for correct parsing! ~$ das add nmap '-v -n -Pn -e eth0 --min-
 rate 1000 -T4 -iL hosts.txt -p1-65535 --open' # Masscan ~$ das add masscan '--
@@ -138,33 +140,33 @@
 parsers/DUMMY_SCANNER.py` (see [example](/das/parsers/masscan.py) for masscan):
 ```python from das.parsers import IAddPortscanOutput class AddPortscanOutput
 (IAddPortscanOutput): """Child class for processing DUMMY_SCANNER output."""
 def parse(self): """ DUMMY_SCANNER raw output parser. :return: a pair of values
 (portscan raw output filename, number of hosts added to DB) :rtype: tuple """
 hosts = set() for line in self.portscan_raw: # DUMMY_SCANNER parser
 implementation pass return (self.portscan_out, len(hosts)) ``` ## Help ```
-usage: das [-h] [-db DB] {add,scan,dns,report,parse,draw,tree,help} ... -------
+usage: das [-h] [-db DB] {db,add,scan,dns,report,parse,draw,tree,help} ... ----
 -------------------------------------------------------------------------------
---------- | ________ .__ .__ .___ _____ .____________ | | \______ \ |__|__
+------------ | ________ .__ .__ .___ _____ .____________ | | \______ \ |__|__
 _|__| __| _/____ / _ \ ____ __| _/ _____/ ____ _____ ____ | | | | \| \ \/ / |/
 __ |/ __ \ / /_\ \ / \ / __ |\_____ \_/ ___\\__ \ / \ | | | ` \ |\ /| / /_/ \
 ___// | \ | \/ /_/ |/ \ \___ / __ \| | \ | | /_______ /__| \_/ |__\____ |\___
 >____|__ /___| /\____ /_______ /\___ >____ /___| / | | \/ \/ \/ \/ \/ \/ \/ \/
 \/ \/ | | {@snovvcrash} {https://github.com/snovvcrash/DivideAndScan} {vX.Y.Z}
 | -----------------------------------------------------------------------------
 ------------------ positional arguments:
-{add,scan,dns,report,parse,draw,tree,help} add run a full port scan and add the
-output to DB scan run targeted Nmap scans against hosts and ports from DB dns
-resolve "A" domain names into IP addresses and update DB items with them report
-merge separate Nmap outputs into a single report (https://github.com/CBHue/
-nMap_Merger) parse parse raw Nmap XML reports by service names and print
-entries in format {service}://{host}:{port}} draw visualize Nmap XML reports
-(https://github.com/jor6PS/DrawNmap) tree show contents of the ~/.das/
-directory using tree help show builtin --help dialog of a selected port scanner
-options: -h, --help show this help message and exit -db DB DB name to work with
-Psst, hey buddy... Wanna do some organized p0r7 5c4nn1n6? ``` ## ToDo * [x] Add
-[projectdiscovery/naabu](https://github.com/projectdiscovery/naabu) parser *
-[x] Add [elddy/NimScan](https://github.com/elddy/NimScan) parser * [x] Add [sx]
-(https://github.com/v-byte-cpu/sx) parser * [ ] Add [ZMap](https://github.com/
-zmap/zmap) parser * [x] Store hostnames (if there're any) next to their IP
-values * [x] Add `fuff` switch to automate web directory fuzzing (added `parse`
-module)
+{db,add,scan,dns,report,parse,draw,tree,help} db utilities for manual DB
+manipulations add run a full port scan and add the output to DB scan run
+targeted Nmap scans against hosts and ports from DB dns map domain names from
+an input file to corresponding IP addresses from the DB report merge separate
+Nmap outputs into a single report (https://github.com/CBHue/nMap_Merger) parse
+parse raw Nmap XML reports by service names and print entries in format
+{service}://{host}:{port}} draw visualize Nmap XML reports (https://github.com/
+jor6PS/DrawNmap) tree show contents of the ~/.das/ directory using tree help
+show builtin --help dialog of a selected port scanner options: -h, --help show
+this help message and exit -db DB DB name to work with Psst, hey buddy... Wanna
+do some organized p0r7 5c4nn1n6? ``` ## ToDo * [x] Add [projectdiscovery/naabu]
+(https://github.com/projectdiscovery/naabu) parser * [x] Add [elddy/NimScan]
+(https://github.com/elddy/NimScan) parser * [x] Add [sx](https://github.com/v-
+byte-cpu/sx) parser * [ ] Add [ZMap](https://github.com/zmap/zmap) parser * [x]
+Store hostnames (if there're any) next to their IP values * [x] Add `fuff`
+switch to automate web directory fuzzing (added `parse` module)
```

### Comparing `divideandscan-0.3.8/das/common.py` & `divideandscan-1.0.0/das/common.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 #!/usr/bin/env python3
 
 __author__ = '@snovvcrash'
 __site__ = 'https://github.com/snovvcrash/DivideAndScan'
-__version__ = '0.3.8'
+__version__ = '1.0.0'
 
 import time
+import shlex
+import subprocess
 from datetime import datetime, timedelta
 
 BANNER = """\
 \033[0;37m -----------------------------------------------------------------------------------------------
 \033[0;37m|\033[1;31m  ________  \033[0;37m.__      .__    .___        \033[1;31m_____\033[0;37m              .__\033[1;31m__________\033[0;37m   \033[1;31m                    |
 \033[0;37m|\033[1;31m  \\______ \\ \033[0;37m|__|__  _|__| __| _/____   \033[1;31m/  _  \\\033[0;37m   ____    __| _\033[1;31m/   _____/\033[0;37m ____ _____    ____   \033[1;31m |
 \033[0;37m|\033[1;31m   |    |  \\\033[0;37m|  \\  \\/ /  |/ __ |/ __ \\ \033[1;31m/  /_\\  \\\033[0;37m /    \\  / __ |\033[1;31m\\_____  \\\033[0;37m_/ ___\\\\__  \\  /    \\   \033[1;31m|
@@ -104,7 +106,22 @@
 
 		:param msg: the message to print
 		:type msg: str
 		:param prefix: the prefix string, intended to be a counter when moving to next separated item
 		:type prefix: str
 		"""
 		print(f'\033[0;31m{SEP} \033[0;32m({prefix}) \033[1;32m{msg}\033[0;31m {SEP}\033[0m')
+
+
+def run_command(command):
+    process = subprocess.Popen(shlex.split(command), stdout=subprocess.PIPE)
+
+    result = ''
+    while True:
+        stdout = process.stdout.readline().decode()
+        if stdout == '' and process.poll() is not None:
+            break
+        if stdout:
+            result += stdout
+
+    #result = process.poll()
+    return result
```

### Comparing `divideandscan-0.3.8/das/divideandscan.py` & `divideandscan-1.0.0/das/divideandscan.py`

 * *Files 7% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 import sys
 from pathlib import Path
 from importlib import import_module
 from collections import namedtuple
 from argparse import ArgumentParser, RawTextHelpFormatter, RawDescriptionHelpFormatter
 
 import das.common
+from das.db import DB
 from das.scan import ScanShow, ScanRun
 from das.dns import DNS
 from das.report import NmapMerger
 from das.parsenmap import NmapParser
 from das.common import BANNER, Logger
 
 
@@ -23,14 +24,24 @@
 	:rtype: argparse.ArgumentParser.Namespace
 	"""
 	parser = ArgumentParser(description=BANNER, formatter_class=RawTextHelpFormatter, epilog='Psst, hey buddy... Wanna do some organized p0r7 5c4nn1n6?')
 	parser.add_argument('-db', action='store', type=str, default='main', help='DB name to work with')
 
 	subparser = parser.add_subparsers(dest='subparser')
 
+	db_epilog = """
+	examples:
+	  das -db testdb db scan.txt [-d domains.txt] [--create]
+	""".replace('\t', '')
+	db_parser = subparser.add_parser('db', formatter_class=RawDescriptionHelpFormatter, epilog=db_epilog, help='utilities for manual DB manipulations')
+	db_parser.add_argument('scan_output', action='store', type=str, help='path to a newline-separated text file with scan output to fill the DB with')
+	db_parser.add_argument('-d', '--domains', action='store', type=str, help='path to a newline-separated text file with with domain names to fill the DB with')
+	group_action = db_parser.add_mutually_exclusive_group(required=True)
+	group_action.add_argument('--create', action='store_true', default=False, help='create TinyDB from a generic scan output and (optionally) a list of domain names')
+
 	add_epilog = """
 	examples:
 	  das add nmap '-v -n -Pn -e eth0 --min-rate 1000 -T4 -iL hosts.txt -p1-49151 --open'
 	  das -db testdb add masscan '-e eth0 --rate 1000 -iL hosts.txt -p1-65535 --open'
 	  das add rustscan '-b 1000 -t 2000 -u 5000 -a hosts.txt -r 1-65535 -g --no-config --scan-order "Random"'
 	  das -db testdb add naabu '-interface eth0 -rate 1000 -iL hosts.txt -p - -silent -s s'
 	  das add -rm nimscan '192.168.1.0/24 -vi -p:1-65535 -f:500'
@@ -66,18 +77,21 @@
 	group_action.add_argument('-oG', action='store', type=str, default=None, help='final report filename without extension (grepable format)')
 	group_criteria = scan_parser.add_mutually_exclusive_group(required=True)
 	group_criteria.add_argument('-hosts', action='store', type=str, default=None, help='hosts to scan all their ports which were considered as open (a comma-separated string of IPs and/or CIDRs or a filename; "all" for all hosts in DB)')
 	group_criteria.add_argument('-ports', action='store', type=str, default=None, help='ports to scan on every host where it was considered as open (a comma-separated string of ports or a filename; "all" for all ports in DB)')
 
 	dns_epilog = """
 	examples:
-	  das dns domains.txt
+	  das dns domains.txt [--resolve|--update]
 	""".replace('\t', '')
-	dns_parser = subparser.add_parser('dns', formatter_class=RawDescriptionHelpFormatter, epilog=dns_epilog, help='resolve "A" domain names into IP addresses and update DB items with them')
+	dns_parser = subparser.add_parser('dns', formatter_class=RawDescriptionHelpFormatter, epilog=dns_epilog, help='map domain names from an input file to corresponding IP addresses from the DB')
 	dns_parser.add_argument('domains', action='store', type=str, help='path to a newline-separated text file with domain names to resolve')
+	group_action = dns_parser.add_mutually_exclusive_group(required=True)
+	group_action.add_argument('--resolve', action='store_true', default=False, help='resolve "A" domain names into IP addresses and update DB items with them')
+	group_action.add_argument('--update', action='store_true', default=False, help='update existing DB with new domains names from an input file')
 
 	report_epilog = """
 	examples:
 	  das report -hosts all -show
 	  das report -hosts 192.168.1.0/24,10.10.13.37 -oA report1
 	  das report -ports 22,80,443,445 -oA report2
 	  das report -ports ports.txt -oA report2
@@ -123,24 +137,34 @@
 def main():
 	"""
 	Main function.
 	"""
 	args = parse_args()
 
 	if len(sys.argv) == 1:
-		print('usage: __main__.py [-h] {add,scan,dns,report,parse,draw,tree,help} ...\n')
+		print('usage: __main__.py [-h] {db,add,scan,dns,report,parse,draw,tree,help} ...\n')
 		print(BANNER)
 		sys.exit(0)
 
 	logger = Logger()
 
 	if (args.subparser == 'add' and not Path(args.scanner_args).is_file) or args.subparser == 'scan' and not args.show:
 		logger.start_timer()
 
-	if args.subparser == 'add':
+	if args.subparser == 'db':
+		(Path.home() / '.das' / 'db' / 'raw').mkdir(parents=True, exist_ok=True)
+		P = Path.home() / '.das' / 'db' / f'{args.db}.json'
+
+		db = DB(str(P))
+		if args.create:
+			logger.print_info(f'Creating DB -> {P.resolve()}')
+			num_created = db.create_generic(Path(args.scan_output), Path(args.domains))
+			logger.print_success(f'Successfully created DB with {num_created} hosts')
+
+	elif args.subparser == 'add':
 		(Path.home() / '.das' / 'db' / 'raw').mkdir(parents=True, exist_ok=True)
 
 		module_name = Path(args.scanner_name).name
 		try:
 			AddPortscanOutput = import_module(f'das.parsers.{module_name}', 'AddPortscanOutput').AddPortscanOutput
 		except ModuleNotFoundError:
 			logger.print_error(f"Unsupported port scanner '{module_name}'")
@@ -148,24 +172,24 @@
 		except Exception as e:
 			logger.print_error(f"Unknown error while loading '{module_name}' parser: {str(e)}")
 			sys.exit(1)
 
 		P = Path.home() / '.das' / 'db' / f'{args.db}.json'
 
 		apo = AddPortscanOutput(str(P), args.rm, args.scanner_name, args.scanner_args)
-		portscan_out, num_of_hosts = apo.parse()
+		portscan_out, num_hosts = apo.parse()
 
 		if P.exists():
 			logger.print_info(f'Using DB -> {P.resolve()}')
 
 		P = Path.home() / '.das' / portscan_out
 		if P.exists():
 			logger.print_info(f'Raw port scanner output -> {P.resolve()}')
 
-		logger.print_success(f'Successfully updated DB with {num_of_hosts} hosts')
+		logger.print_success(f'Successfully updated DB with {num_hosts} hosts')
 
 	elif args.subparser == 'scan':
 		if not args.show:
 			(Path.home() / '.das' / f'nmap_{args.db}').mkdir(parents=True, exist_ok=True)
 
 		output = {'oA': args.oA, 'oX': args.oX, 'oN': args.oN, 'oG': args.oG}
 
@@ -194,16 +218,20 @@
 			nm.generate()
 
 	elif args.subparser == 'dns':
 		P = Path.home() / '.das' / 'db' / f'{args.db}.json'
 		if P.exists():
 			logger.print_info(f'Using DB -> {P.resolve()}')
 
-		d = DNS(str(P), Path(args.domains))
-		d.resolve()
+		dns = DNS(str(P), Path(args.domains))
+		if args.resolve:
+			dns.resolve()
+		elif args.update:
+			num_updated = dns.update()
+			logger.print_success(f'Successfully updated {num_updated} hosts from DB with domain names')
 
 	elif args.subparser == 'report':
 		output = {'oA': args.oA, 'oX': args.oX, 'oN': args.oN, 'oG': args.oG}
 
 		if args.show:
 			nm = NmapMerger(args.db, args.hosts, args.ports)
 			nm.show()
```

### Comparing `divideandscan-0.3.8/das/drawnmap.py` & `divideandscan-1.0.0/das/drawnmap.py`

 * *Files identical despite different names*

### Comparing `divideandscan-0.3.8/das/parsenmap.py` & `divideandscan-1.0.0/das/parsenmap.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 from pathlib import Path
 
 import nmap
 from tinydb import TinyDB, Query
 
 from das.common import Logger
 
+
 class NmapParser:
 	"""Class for parsing Nmap XML reports by service names and print entries in format {service}://{host}:{port}}."""
 
 	def __init__(self, db_path, services, dns, raw_output=False):
 		"""
 		Constructor.
 
@@ -23,16 +24,16 @@
 		:type dns: bool
 		:param raw_output: a boolean flag which, when presented, indicates that results must be printed in a raw list (no decorations or colors)
 		:type raw_output: bool
 		:return: class object
 		:rtype: das.report.NmapParser
 		"""
 		self.services = services.split(',')
-		
-		self.db = None
+		self.dns = dns
+
 		if dns:
 			self.db = TinyDB(db_path)
 			self.ip_domains_dict = {}
 			for item in self.db.all():
 				self.ip_domains_dict[item['ip']] = item['domains']
 
 		self.raw_output = raw_output
@@ -54,15 +55,15 @@
 			
 			for ip in nm.all_hosts():
 				if 'tcp' in nm[ip]:
 					for port in nm[ip]['tcp']:
 						if nm[ip]['tcp'][port]['state'] == 'open':
 							service = nm[ip]['tcp'][port]['name']
 							if service in self.services:
-								if self.db:
+								if self.dns:
 									domains = self.ip_domains_dict[ip]
 									if domains:
 										for domain in domains:
 											if not self.raw_output:
 												Logger.print_success(f'IP {ip} -> {service}://{domain}:{port}')
 											else:
 												print(f'{service}://{domain}:{port}')
```

### Comparing `divideandscan-0.3.8/das/parsers/__init__.py` & `divideandscan-1.0.0/das/parsers/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 	"""Base class for updating DB with parsed portscan output."""
 
 	def __init__(self, db_path, rm, scanner_name, scanner_args):
 		"""
 		Constructor.
 
 		:param db_path: a TinyDB database file path
-		:type db_path: pathlib.PosixPath
+		:type db_path: str
 		:param rm: a flag showing if we need to drop the DB before updating its values
 		:type rm: bool
 		:param scanner_name: name of the port scanner to run
 		:type scanner_name: str
 		:param scanner_args: port scanner arguments
 		:type scanner_args: str
 		:return: base class object
```

### Comparing `divideandscan-0.3.8/das/parsers/masscan.py` & `divideandscan-1.0.0/das/parsers/sx.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,29 +1,26 @@
 from das.parsers import IAddPortscanOutput
 
 
 class AddPortscanOutput(IAddPortscanOutput):
-	"""Child class for processing Masscan output."""
+	"""Child class for processing sx output."""
 
 	def parse(self):
 		"""
-		Masscan raw output parser.
+		sx raw output parser.
 
 		:return: a pair of values (portscan raw output filename, number of hosts added to DB)
 		:rtype: tuple
 		"""
-		hosts = set()
+		items, hosts = [], set()
 		for line in self.portscan_raw:
 			try:
-				ip = line.split()[-1]
-				port, proto = line.split()[3].split('/')
+				ip, port = line.split()
 			except Exception:
 				pass
 			else:
-				if proto == 'tcp':
-					item = {'ip': ip, 'port': int(port), 'domains': []}
-					if item not in self.db:
-						self.db.insert(item)
-
+				items.append({'ip': ip, 'port': int(port), 'domains': []})
 				hosts.add(ip)
 
+		self.db.insert_multiple(items)
+
 		return (self.portscan_out, len(hosts))
```

### Comparing `divideandscan-0.3.8/das/parsers/naabu.py` & `divideandscan-1.0.0/das/parsers/naabu.py`

 * *Files 23% similar despite different names*

```diff
@@ -7,21 +7,20 @@
 	def parse(self):
 		"""
 		Naabu raw output parser.
 
 		:return: a pair of values (portscan raw output filename, number of hosts added to DB)
 		:rtype: tuple
 		"""
-		hosts = set()
+		items, hosts = [], set()
 		for line in self.portscan_raw:
 			try:
 				ip, port = line.split(':')
 			except Exception:
 				pass
 			else:
-				item = {'ip': ip, 'port': int(port), 'domains': []}
-				if item not in self.db:
-					self.db.insert(item)
-
+				items.append({'ip': ip, 'port': int(port), 'domains': []})
 				hosts.add(ip)
 
+		self.db.insert_multiple(items)
+
 		return (self.portscan_out, len(hosts))
```

### Comparing `divideandscan-0.3.8/das/parsers/nimscan.py` & `divideandscan-1.0.0/das/parsers/nimscan.py`

 * *Files 14% similar despite different names*

```diff
@@ -7,26 +7,25 @@
 	def parse(self):
 		"""
 		NimScan raw output parser.
 
 		:return: a pair of values (portscan raw output filename, number of hosts added to DB)
 		:rtype: tuple
 		"""
-		hosts = set()
+		items, hosts = [], set()
 		for line in self.portscan_raw:
 			try:
 				ip, port = line.split('==>')[1].split()[0].split(':')
 				# Get rid of ANSII color symbols
 				ip = ''.join([i if 48 <= ord(i) <= 57 or ord(i) == 46 else '' for i in ip])
 				ip = ip.strip('0')
 				port = port.split('[')[0]
 				port = ''.join([i if 48 <= ord(i) <= 57 else '' for i in port])
 			except Exception:
 				pass
 			else:
-				item = {'ip': ip, 'port': int(port), 'domains': []}
-				if item not in self.db:
-					self.db.insert(item)
-
+				items.append({'ip': ip, 'port': int(port), 'domains': []})
 				hosts.add(ip)
 
+		self.db.insert_multiple(items)
+
 		return (self.portscan_out, len(hosts))
```

### Comparing `divideandscan-0.3.8/das/report.py` & `divideandscan-1.0.0/das/report.py`

 * *Files identical despite different names*

### Comparing `divideandscan-0.3.8/das/scan.py` & `divideandscan-1.0.0/das/scan.py`

 * *Files identical despite different names*

### Comparing `divideandscan-0.3.8/pyproject.toml` & `divideandscan-1.0.0/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "divideandscan"
-version = "0.3.8"
+version = "1.0.0"
 description = "Divide full port scan results and use it for targeted Nmap runs"
 authors = ["Sam Freeside <snovvcrash@protonmail.ch>"]
 license = "BSD-2-Clause"
 readme = "README.md"
 homepage = "https://github.com/snovvcrash/DivideAndScan"
 repository = "https://github.com/snovvcrash/DivideAndScan"
 keywords = ["pentest", "scan", "nmap", "masscan", "rustscan"]
```

### Comparing `divideandscan-0.3.8/PKG-INFO` & `divideandscan-1.0.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: divideandscan
-Version: 0.3.8
+Version: 1.0.0
 Summary: Divide full port scan results and use it for targeted Nmap runs
 Home-page: https://github.com/snovvcrash/DivideAndScan
 License: BSD-2-Clause
 Keywords: pentest,scan,nmap,masscan,rustscan
 Author: Sam Freeside
 Author-email: snovvcrash@protonmail.ch
 Requires-Python: >=3.9,<3.12
@@ -33,15 +33,15 @@
 </p>
 
 <p align="center">
   <strong>Divide <strike>Et Impera</strike> And Scan (and also merge the scan results)</strong>
 </p>
 
 <p align="center">
-  <a href="https://github.com/snovvcrash/DivideAndScan/blob/main/pyproject.toml#L3"><img src="https://img.shields.io/badge/version-0.3.8-success" alt="version" /></a>
+  <a href="https://github.com/snovvcrash/DivideAndScan/blob/main/pyproject.toml#L3"><img src="https://img.shields.io/badge/version-1.0.0-success" alt="version" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/search?l=python"><img src="https://img.shields.io/badge/python-3.9-blue?logo=python&logoColor=white" alt="python" /></a>
   <a href="https://www.codacy.com/gh/snovvcrash/DivideAndScan/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=snovvcrash/DivideAndScan&amp;utm_campaign=Badge_Grade"><img src="https://app.codacy.com/project/badge/Grade/35f0bdfece9846d7aab3888b01642813" alt="codacy" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-pypi.yml"><img src="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-pypi.yml/badge.svg" alt="pypi" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-docker-hub.yml"><img src="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-docker-hub.yml/badge.svg" alt="docker" /></a>
 </p>
 
 ---
@@ -130,14 +130,22 @@
 
 ```bash
 sudo mkdir /opt/sx
 sudo eget -s linux/amd64 v-byte-cpu/sx --to /opt/sx
 sudo ln -sv /opt/sx/sx /usr/local/bin/sx
 ```
 
+#### dnsx
+
+```bash
+sudo mkdir /opt/pd
+sudo eget -s linux/amd64 projectdiscovery/dnsx --to /opt/pd
+sudo ln -sv /opt/pd/dnsx /usr/local/bin/dnsx
+```
+
 ### Installation
 
 DivideAndScan is available on PyPI as `divideandscan`, though I recommend installing it from GitHub with [pipx](https://github.com/pipxproject/pipx) in order to always have the bleeding-edge version:
 
 ```console
 ~$ pipx install -f "git+https://github.com/snovvcrash/DivideAndScan.git"
 ~$ das
@@ -346,31 +354,32 @@
 
         return (self.portscan_out, len(hosts))
 ```
 
 ## Help
 
 ```
-usage: das [-h] [-db DB] {add,scan,dns,report,parse,draw,tree,help} ...
+usage: das [-h] [-db DB] {db,add,scan,dns,report,parse,draw,tree,help} ...
 
  -----------------------------------------------------------------------------------------------
 |  ________  .__      .__    .___        _____              .____________                       |
 |  \______ \ |__|__  _|__| __| _/____   /  _  \   ____    __| _/   _____/ ____ _____    ____    |
 |   |    |  \|  \  \/ /  |/ __ |/ __ \ /  /_\  \ /    \  / __ |\_____  \_/ ___\\__  \  /    \   |
 |   |    `   \  |\   /|  / /_/ \  ___//    |    \   |  \/ /_/ |/        \  \___ / __ \|   |  \  |
 |  /_______  /__| \_/ |__\____ |\___  >____|__  /___|  /\____ /_______  /\___  >____  /___|  /  |
 |          \/                 \/    \/        \/     \/      \/       \/     \/     \/     \/   |
 |  {@snovvcrash}            {https://github.com/snovvcrash/DivideAndScan}             {vX.Y.Z}  |
  -----------------------------------------------------------------------------------------------
 
 positional arguments:
-  {add,scan,dns,report,parse,draw,tree,help}
+  {db,add,scan,dns,report,parse,draw,tree,help}
+    db                  utilities for manual DB manipulations
     add                 run a full port scan and add the output to DB
     scan                run targeted Nmap scans against hosts and ports from DB
-    dns                 resolve "A" domain names into IP addresses and update DB items with them
+    dns                 map domain names from an input file to corresponding IP addresses from the DB
     report              merge separate Nmap outputs into a single report (https://github.com/CBHue/nMap_Merger)
     parse               parse raw Nmap XML reports by service names and print entries in format {service}://{host}:{port}}
     draw                visualize Nmap XML reports (https://github.com/jor6PS/DrawNmap)
     tree                show contents of the ~/.das/ directory using tree
     help                show builtin --help dialog of a selected port scanner
 
 options:
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: divideandscan Version: 0.3.8 Summary: Divide full
+Metadata-Version: 2.1 Name: divideandscan Version: 1.0.0 Summary: Divide full
 port scan results and use it for targeted Nmap runs Home-page: https://
 github.com/snovvcrash/DivideAndScan License: BSD-2-Clause Keywords:
 pentest,scan,nmap,masscan,rustscan Author: Sam Freeside Author-email:
 snovvcrash@protonmail.ch Requires-Python: >=3.9,<3.12 Classifier: Environment
 :: Console Classifier: License :: OSI Approved :: BSD License Classifier:
 Programming Language :: Python :: 3 Classifier: Programming Language :: Python
 :: 3.9 Classifier: Programming Language :: Python :: 3.10 Classifier:
@@ -55,37 +55,39 @@
 fe8628396616c4bf7a3e25f2c9d1acc2f36af0c0/rustscan-ports-top1000.toml -O /
 root/.rustscan.toml ``` #### Naabu ```bash sudo mkdir /opt/naabu sudo eget -
 s linux/amd64 projectdiscovery/naabu --to /opt/naabu sudo ln -sv /opt/naabu/
 naabu /usr/local/bin/naabu ``` #### NimScan ```bash sudo mkdir /opt/nimscan
 sudo eget -a NimScan elddy/NimScan --to /opt/nimscan sudo ln -sv /opt/nimscan/
 nimscan /usr/local/bin/nimscan ``` #### sx ```bash sudo mkdir /opt/sx sudo eget
 -s linux/amd64 v-byte-cpu/sx --to /opt/sx sudo ln -sv /opt/sx/sx /usr/local/
-bin/sx ``` ### Installation DivideAndScan is available on PyPI as
-`divideandscan`, though I recommend installing it from GitHub with [pipx]
-(https://github.com/pipxproject/pipx) in order to always have the bleeding-edge
-version: ```console ~$ pipx install -f "git+https://github.com/snovvcrash/
-DivideAndScan.git" ~$ das ``` For debbugging purposes you can set up a dev
-environment with [poetry](https://github.com/python-poetry/poetry): ```console
-~$ git clone --recurse-submodules https://github.com/snovvcrash/DivideAndScan
-~$ cd DivideAndScan ~$ poetry install ~$ poetry run das ``` ð **Note:**
-DivideAndScan uses sudo to run all the port scanners, so it will ask for the
-password when scanning commands are invoked. ### Using from Docker [!
-[dockeri.co](https://dockeri.co/image/snovvcrash/divideandscan)](https://
-hub.docker.com/r/snovvcrash/divideandscan) You can run DivideAndScan in a
-Docker container as follows: ```console ~$ docker run --rm -it --name das -
-v ~/.das:/root/.das -v `pwd`:/app -p 8050:8050 snovvcrash/divideandscan ```
-Since the tool requires some input data and produces some output data, you
-should specify your current working directory as the mount point at `/app`
-within the container. Also publishing port 8050 on host allows to access the
-[Dash](https://github.com/plotly/dash) app used for Nmap reports visualization.
-You may want to set an alias to make the base command shorter: ```console ~$
-alias das='docker run --rm -it --name das -v ~/.das:/root/.das -v `pwd`:/app -
-p 8050:8050 snovvcrash/divideandscan' ~$ das ``` ## How to Use ![how-to-
-use.png](https://user-images.githubusercontent.com/23141800/113610915-6fae9b80-
-9656-11eb-8b1a-db503dd43861.png) ### 1. Filling the DB
+bin/sx ``` #### dnsx ```bash sudo mkdir /opt/pd sudo eget -s linux/amd64
+projectdiscovery/dnsx --to /opt/pd sudo ln -sv /opt/pd/dnsx /usr/local/bin/dnsx
+``` ### Installation DivideAndScan is available on PyPI as `divideandscan`,
+though I recommend installing it from GitHub with [pipx](https://github.com/
+pipxproject/pipx) in order to always have the bleeding-edge version: ```console
+~$ pipx install -f "git+https://github.com/snovvcrash/DivideAndScan.git" ~$ das
+``` For debbugging purposes you can set up a dev environment with [poetry]
+(https://github.com/python-poetry/poetry): ```console ~$ git clone --recurse-
+submodules https://github.com/snovvcrash/DivideAndScan ~$ cd DivideAndScan ~$
+poetry install ~$ poetry run das ``` ð **Note:** DivideAndScan uses sudo to
+run all the port scanners, so it will ask for the password when scanning
+commands are invoked. ### Using from Docker [![dockeri.co](https://dockeri.co/
+image/snovvcrash/divideandscan)](https://hub.docker.com/r/snovvcrash/
+divideandscan) You can run DivideAndScan in a Docker container as follows:
+```console ~$ docker run --rm -it --name das -v ~/.das:/root/.das -v `pwd`:/app
+-p 8050:8050 snovvcrash/divideandscan ``` Since the tool requires some input
+data and produces some output data, you should specify your current working
+directory as the mount point at `/app` within the container. Also publishing
+port 8050 on host allows to access the [Dash](https://github.com/plotly/dash)
+app used for Nmap reports visualization. You may want to set an alias to make
+the base command shorter: ```console ~$ alias das='docker run --rm -it --name
+das -v ~/.das:/root/.das -v `pwd`:/app -p 8050:8050 snovvcrash/divideandscan'
+~$ das ``` ## How to Use ![how-to-use.png](https://user-
+images.githubusercontent.com/23141800/113610915-6fae9b80-9656-11eb-8b1a-
+db503dd43861.png) ### 1. Filling the DB
 Provide the `add` module a command for a fast port scanner to discover open
 ports in a desired range. â ï¸ **Warning:** please, make sure that you
 understand what you're doing, because nearly all port scanning tools [can
 damage the system being tested](https://github.com/RustScan/RustScan/wiki/
 Usage#%EF%B8%8F-warning) if used improperly. ```console # Nmap, -v flag is
 always required for correct parsing! ~$ das add nmap '-v -n -Pn -e eth0 --min-
 rate 1000 -T4 -iL hosts.txt -p1-65535 --open' # Masscan ~$ das add masscan '--
@@ -154,33 +156,33 @@
 parsers/DUMMY_SCANNER.py` (see [example](/das/parsers/masscan.py) for masscan):
 ```python from das.parsers import IAddPortscanOutput class AddPortscanOutput
 (IAddPortscanOutput): """Child class for processing DUMMY_SCANNER output."""
 def parse(self): """ DUMMY_SCANNER raw output parser. :return: a pair of values
 (portscan raw output filename, number of hosts added to DB) :rtype: tuple """
 hosts = set() for line in self.portscan_raw: # DUMMY_SCANNER parser
 implementation pass return (self.portscan_out, len(hosts)) ``` ## Help ```
-usage: das [-h] [-db DB] {add,scan,dns,report,parse,draw,tree,help} ... -------
+usage: das [-h] [-db DB] {db,add,scan,dns,report,parse,draw,tree,help} ... ----
 -------------------------------------------------------------------------------
---------- | ________ .__ .__ .___ _____ .____________ | | \______ \ |__|__
+------------ | ________ .__ .__ .___ _____ .____________ | | \______ \ |__|__
 _|__| __| _/____ / _ \ ____ __| _/ _____/ ____ _____ ____ | | | | \| \ \/ / |/
 __ |/ __ \ / /_\ \ / \ / __ |\_____ \_/ ___\\__ \ / \ | | | ` \ |\ /| / /_/ \
 ___// | \ | \/ /_/ |/ \ \___ / __ \| | \ | | /_______ /__| \_/ |__\____ |\___
 >____|__ /___| /\____ /_______ /\___ >____ /___| / | | \/ \/ \/ \/ \/ \/ \/ \/
 \/ \/ | | {@snovvcrash} {https://github.com/snovvcrash/DivideAndScan} {vX.Y.Z}
 | -----------------------------------------------------------------------------
 ------------------ positional arguments:
-{add,scan,dns,report,parse,draw,tree,help} add run a full port scan and add the
-output to DB scan run targeted Nmap scans against hosts and ports from DB dns
-resolve "A" domain names into IP addresses and update DB items with them report
-merge separate Nmap outputs into a single report (https://github.com/CBHue/
-nMap_Merger) parse parse raw Nmap XML reports by service names and print
-entries in format {service}://{host}:{port}} draw visualize Nmap XML reports
-(https://github.com/jor6PS/DrawNmap) tree show contents of the ~/.das/
-directory using tree help show builtin --help dialog of a selected port scanner
-options: -h, --help show this help message and exit -db DB DB name to work with
-Psst, hey buddy... Wanna do some organized p0r7 5c4nn1n6? ``` ## ToDo * [x] Add
-[projectdiscovery/naabu](https://github.com/projectdiscovery/naabu) parser *
-[x] Add [elddy/NimScan](https://github.com/elddy/NimScan) parser * [x] Add [sx]
-(https://github.com/v-byte-cpu/sx) parser * [ ] Add [ZMap](https://github.com/
-zmap/zmap) parser * [x] Store hostnames (if there're any) next to their IP
-values * [x] Add `fuff` switch to automate web directory fuzzing (added `parse`
-module)
+{db,add,scan,dns,report,parse,draw,tree,help} db utilities for manual DB
+manipulations add run a full port scan and add the output to DB scan run
+targeted Nmap scans against hosts and ports from DB dns map domain names from
+an input file to corresponding IP addresses from the DB report merge separate
+Nmap outputs into a single report (https://github.com/CBHue/nMap_Merger) parse
+parse raw Nmap XML reports by service names and print entries in format
+{service}://{host}:{port}} draw visualize Nmap XML reports (https://github.com/
+jor6PS/DrawNmap) tree show contents of the ~/.das/ directory using tree help
+show builtin --help dialog of a selected port scanner options: -h, --help show
+this help message and exit -db DB DB name to work with Psst, hey buddy... Wanna
+do some organized p0r7 5c4nn1n6? ``` ## ToDo * [x] Add [projectdiscovery/naabu]
+(https://github.com/projectdiscovery/naabu) parser * [x] Add [elddy/NimScan]
+(https://github.com/elddy/NimScan) parser * [x] Add [sx](https://github.com/v-
+byte-cpu/sx) parser * [ ] Add [ZMap](https://github.com/zmap/zmap) parser * [x]
+Store hostnames (if there're any) next to their IP values * [x] Add `fuff`
+switch to automate web directory fuzzing (added `parse` module)
```

