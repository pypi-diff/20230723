# Comparing `tmp/neuroconv-0.3.0.tar.gz` & `tmp/neuroconv-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "neuroconv-0.3.0.tar", last modified: Wed Jun  7 21:30:12 2023, max compression
+gzip compressed data, was "neuroconv-0.4.0.tar", last modified: Sun Jul 23 19:19:38 2023, max compression
```

## Comparing `neuroconv-0.3.0.tar` & `neuroconv-0.4.0.tar`

### file list

```diff
@@ -1,218 +1,225 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.865862 neuroconv-0.3.0/
--rw-r--r--   0 runner    (1001) docker     (123)      135 2023-06-07 21:30:07.000000 neuroconv-0.3.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     4407 2023-06-07 21:30:12.865862 neuroconv-0.3.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2896 2023-06-07 21:30:07.000000 neuroconv-0.3.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       74 2023-06-07 21:30:07.000000 neuroconv-0.3.0/base_gin_test_config.json
--rw-r--r--   0 runner    (1001) docker     (123)      458 2023-06-07 21:30:07.000000 neuroconv-0.3.0/codecov.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1533 2023-06-07 21:30:07.000000 neuroconv-0.3.0/license.txt
--rw-r--r--   0 runner    (1001) docker     (123)      183 2023-06-07 21:30:07.000000 neuroconv-0.3.0/make_environment.yml
--rw-r--r--   0 runner    (1001) docker     (123)      513 2023-06-07 21:30:07.000000 neuroconv-0.3.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-06-07 21:30:12.865862 neuroconv-0.3.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     3115 2023-06-07 21:30:07.000000 neuroconv-0.3.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.845861 neuroconv-0.3.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/
--rw-r--r--   0 runner    (1001) docker     (123)      311 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2594 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/basedatainterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     1184 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/baseextractorinterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     3773 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/basetemporalalignmentinterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/converters/
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/converters/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/
--rw-r--r--   0 runner    (1001) docker     (123)     6323 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/audio/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/audio/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10137 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/audio/audiointerface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/deeplabcut/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/deeplabcut/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5220 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/deeplabcut/deeplabcutdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/sleap/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/sleap/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      580 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/sleap/sleap_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3920 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/sleap/sleapdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/video/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/video/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8561 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/video/video_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    22440 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/video/videodatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/alphaomega/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/alphaomega/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1158 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/alphaomega/alphaomegadatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/axona/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/axona/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11273 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/axona/axona_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     5738 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/axona/axonadatainterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     1729 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/baselfpextractorinterface.py
--rw-r--r--   0 runner    (1001) docker     (123)    16333 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/baserecordingextractorinterface.py
--rw-r--r--   0 runner    (1001) docker     (123)    15904 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/basesortingextractorinterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/biocam/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/biocam/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      817 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/biocam/biocamdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/blackrock/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/blackrock/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/blackrock/blackrockdatainterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     4883 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/blackrock/header_tools.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/cellexplorer/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/cellexplorer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6013 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/cellexplorer/cellexplorerdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/edf/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/edf/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2418 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/edf/edfdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/intan/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/intan/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5925 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/intan/intandatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/kilosort/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/kilosort/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      884 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/kilosort/kilosortdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/maxwell/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/maxwell/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3359 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/maxwell/maxonedatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/mcsraw/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/mcsraw/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      817 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/mcsraw/mcsrawdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/mearec/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/mearec/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2311 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/mearec/mearecdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuralynx/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuralynx/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6457 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuralynx/neuralynxdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuroscope/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuroscope/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2897 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuroscope/neuroscope_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    10523 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuroscope/neuroscopedatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4770 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/openephysbinarydatainterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     2030 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/openephysdatainterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     2996 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/openephyslegacydatainterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     1263 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/openephyssortingdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/phy/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/phy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1024 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/phy/phydatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/plexon/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/plexon/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1992 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/plexon/plexondatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spike2/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spike2/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3164 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spike2/spike2datainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikegadgets/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikegadgets/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1749 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikegadgets/spikegadgetsdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3275 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglx_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3817 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxconverter.py
--rw-r--r--   0 runner    (1001) docker     (123)     6035 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxdatainterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     4208 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxnidqinterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/tdt/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/tdt/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1388 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/tdt/tdtdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/icephys/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/icephys/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/icephys/abf/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/icephys/abf/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7939 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/icephys/abf/abfdatainterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     6580 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/icephys/baseicephysinterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4360 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/baseimagingextractorinterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     7049 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/basesegmentationextractorinterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/brukertiff/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/brukertiff/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3179 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/brukertiff/brukertiffdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/caiman/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/caiman/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      602 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/caiman/caimandatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/cnmfe/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/cnmfe/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      447 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/cnmfe/cnmfedatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.853861 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/extract/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/extract/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      883 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/extract/extractdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/hdf5/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/hdf5/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1179 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/hdf5/hdf5datainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/micromanagertiff/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/micromanagertiff/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1975 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/micromanagertiff/micromanagertiffdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/sbx/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/sbx/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      825 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/sbx/sbxdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/scanimage/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/scanimage/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/scanimage/scanimageimaginginterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/sima/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/sima/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      591 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/sima/simadatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/suite2p/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/suite2p/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      705 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/suite2p/suite2pdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/tiff/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/tiff/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      858 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/tiff/tiffdatainterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/csv/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/csv/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      380 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/csv/csvtimeintertervalsinterface.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/excel/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/excel/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      865 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/excel/exceltimeintervalsinterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     6590 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/datainterfaces/text/timeintervalsinterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     9156 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/nwbconverter.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.857862 neuroconv-0.3.0/src/neuroconv/schemas/
--rw-r--r--   0 runner    (1001) docker     (123)     5797 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/schemas/base_metadata_schema.json
--rw-r--r--   0 runner    (1001) docker     (123)    11312 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/schemas/metadata_schema.json
--rw-r--r--   0 runner    (1001) docker     (123)     1352 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/schemas/source_schema.json
--rw-r--r--   0 runner    (1001) docker     (123)     2032 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/schemas/time_series_schema.json
--rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/schemas/yaml_conversion_specification_schema.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.861862 neuroconv-0.3.0/src/neuroconv/tools/
--rw-r--r--   0 runner    (1001) docker     (123)      119 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.861862 neuroconv-0.3.0/src/neuroconv/tools/audio/
--rw-r--r--   0 runner    (1001) docker     (123)       48 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/audio/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3048 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/audio/audio.py
--rw-r--r--   0 runner    (1001) docker     (123)    15556 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/data_transfers.py
--rw-r--r--   0 runner    (1001) docker     (123)     3331 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/figshare.py
--rw-r--r--   0 runner    (1001) docker     (123)     4374 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/hdmf.py
--rw-r--r--   0 runner    (1001) docker     (123)     4311 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/importing.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.861862 neuroconv-0.3.0/src/neuroconv/tools/neo/
--rw-r--r--   0 runner    (1001) docker     (123)      156 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/neo/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    19825 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/neo/neo.py
--rw-r--r--   0 runner    (1001) docker     (123)     7159 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/nwb_helpers.py
--rw-r--r--   0 runner    (1001) docker     (123)     3753 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/path_expansion.py
--rw-r--r--   0 runner    (1001) docker     (123)      904 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/processes.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.861862 neuroconv-0.3.0/src/neuroconv/tools/roiextractors/
--rw-r--r--   0 runner    (1001) docker     (123)      350 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/roiextractors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5671 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/roiextractors/imagingextractordatachunkiterator.py
--rw-r--r--   0 runner    (1001) docker     (123)    45824 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/roiextractors/roiextractors.py
--rw-r--r--   0 runner    (1001) docker     (123)     2225 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/signal_processing.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.861862 neuroconv-0.3.0/src/neuroconv/tools/spikeinterface/
--rw-r--r--   0 runner    (1001) docker     (123)      273 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/spikeinterface/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    67405 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/spikeinterface/spikeinterface.py
--rw-r--r--   0 runner    (1001) docker     (123)     3958 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/spikeinterface/spikeinterfacerecordingdatachunkiterator.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.861862 neuroconv-0.3.0/src/neuroconv/tools/testing/
--rw-r--r--   0 runner    (1001) docker     (123)      217 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/testing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4849 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/testing/_path_expander_demo_ibl_filepaths.txt
--rw-r--r--   0 runner    (1001) docker     (123)    32069 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/testing/data_interface_mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)     1023 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/testing/mock_files.py
--rw-r--r--   0 runner    (1001) docker     (123)     6437 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/testing/mock_interfaces.py
--rw-r--r--   0 runner    (1001) docker     (123)    12328 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/testing/mock_ttl_signals.py
--rw-r--r--   0 runner    (1001) docker     (123)     2074 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/text.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.865862 neuroconv-0.3.0/src/neuroconv/tools/yaml_conversion_specification/
--rw-r--r--   0 runner    (1001) docker     (123)       68 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/yaml_conversion_specification/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6750 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/tools/yaml_conversion_specification/yaml_conversion_specification.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.865862 neuroconv-0.3.0/src/neuroconv/utils/
--rw-r--r--   0 runner    (1001) docker     (123)      590 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      621 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/utils/checks.py
--rw-r--r--   0 runner    (1001) docker     (123)     9587 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/utils/dict.py
--rw-r--r--   0 runner    (1001) docker     (123)    12912 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/utils/json_schema.py
--rw-r--r--   0 runner    (1001) docker     (123)      417 2023-06-07 21:30:07.000000 neuroconv-0.3.0/src/neuroconv/utils/types.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 21:30:12.849861 neuroconv-0.3.0/src/neuroconv.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4407 2023-06-07 21:30:12.000000 neuroconv-0.3.0/src/neuroconv.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8440 2023-06-07 21:30:12.000000 neuroconv-0.3.0/src/neuroconv.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-07 21:30:12.000000 neuroconv-0.3.0/src/neuroconv.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      135 2023-06-07 21:30:12.000000 neuroconv-0.3.0/src/neuroconv.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)     3811 2023-06-07 21:30:12.000000 neuroconv-0.3.0/src/neuroconv.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-06-07 21:30:12.000000 neuroconv-0.3.0/src/neuroconv.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.665921 neuroconv-0.4.0/
+-rw-r--r--   0 runner    (1001) docker     (123)      135 2023-07-23 19:19:32.000000 neuroconv-0.4.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     4455 2023-07-23 19:19:38.665921 neuroconv-0.4.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2896 2023-07-23 19:19:32.000000 neuroconv-0.4.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       74 2023-07-23 19:19:32.000000 neuroconv-0.4.0/base_gin_test_config.json
+-rw-r--r--   0 runner    (1001) docker     (123)      458 2023-07-23 19:19:32.000000 neuroconv-0.4.0/codecov.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1533 2023-07-23 19:19:32.000000 neuroconv-0.4.0/license.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      183 2023-07-23 19:19:32.000000 neuroconv-0.4.0/make_environment.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      513 2023-07-23 19:19:32.000000 neuroconv-0.4.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 19:19:38.665921 neuroconv-0.4.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     3143 2023-07-23 19:19:32.000000 neuroconv-0.4.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.633921 neuroconv-0.4.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.637920 neuroconv-0.4.0/src/neuroconv/
+-rw-r--r--   0 runner    (1001) docker     (123)      311 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3821 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/basedatainterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1184 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/baseextractorinterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3797 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/basetemporalalignmentinterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv/converters/
+-rw-r--r--   0 runner    (1001) docker     (123)      169 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/converters/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv/datainterfaces/
+-rw-r--r--   0 runner    (1001) docker     (123)     6694 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/audio/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/audio/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9658 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/audio/audiointerface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/deeplabcut/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/deeplabcut/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4431 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/deeplabcut/deeplabcutdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/miniscope/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/miniscope/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3979 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/miniscope/miniscopedatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/sleap/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/sleap/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      580 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/sleap/sleap_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3125 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/sleap/sleapdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/video/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/video/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8551 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/video/video_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21369 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/video/videodatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/alphaomega/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/alphaomega/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1158 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/alphaomega/alphaomegadatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/axona/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/axona/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11273 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/axona/axona_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5738 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/axona/axonadatainterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1539 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/baselfpextractorinterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15767 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/baserecordingextractorinterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16091 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/basesortingextractorinterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/biocam/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/biocam/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      817 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/biocam/biocamdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/blackrock/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/blackrock/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/blackrock/blackrockdatainterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4883 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/blackrock/header_tools.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/cellexplorer/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/cellexplorer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23974 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/cellexplorer/cellexplorerdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/edf/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/edf/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2418 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/edf/edfdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/intan/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/intan/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5899 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/intan/intandatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.645921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/kilosort/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/kilosort/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      884 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/kilosort/kilosortdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/maxwell/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/maxwell/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3359 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/maxwell/maxonedatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/mcsraw/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/mcsraw/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      815 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/mcsraw/mcsrawdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/mearec/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/mearec/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2267 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/mearec/mearecdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuralynx/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuralynx/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7432 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuralynx/neuralynxdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuroscope/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuroscope/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3890 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuroscope/neuroscope_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12153 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuroscope/neuroscopedatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4616 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/openephysbinarydatainterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2030 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/openephysdatainterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2996 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/openephyslegacydatainterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/openephyssortingdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/phy/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/phy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      992 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/phy/phydatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/plexon/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/plexon/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1992 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/plexon/plexondatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.649921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spike2/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spike2/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3164 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spike2/spike2datainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikegadgets/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikegadgets/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1723 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikegadgets/spikegadgetsdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3275 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglx_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3817 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxconverter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6035 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxdatainterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4208 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxnidqinterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/tdt/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/tdt/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1388 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/tdt/tdtdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/icephys/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/icephys/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/icephys/abf/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/icephys/abf/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7939 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/icephys/abf/abfdatainterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4696 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/icephys/baseicephysinterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4845 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/baseimagingextractorinterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6694 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/basesegmentationextractorinterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/brukertiff/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/brukertiff/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3179 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/brukertiff/brukertiffdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/caiman/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/caiman/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      602 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/caiman/caimandatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/cnmfe/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/cnmfe/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      447 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/cnmfe/cnmfedatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.653921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/extract/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/extract/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      883 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/extract/extractdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/hdf5/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/hdf5/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1179 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/hdf5/hdf5datainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/micromanagertiff/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/micromanagertiff/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1975 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/micromanagertiff/micromanagertiffdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/miniscope/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/miniscope/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3673 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/miniscope/miniscopeconverter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4119 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/miniscope/miniscopeimagingdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/sbx/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/sbx/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      814 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/sbx/sbxdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/scanimage/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/scanimage/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/scanimage/scanimageimaginginterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/sima/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/sima/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      591 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/sima/simadatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/suite2p/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/suite2p/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      705 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/suite2p/suite2pdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/tiff/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/tiff/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      858 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/tiff/tiffdatainterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/csv/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/csv/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      380 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/csv/csvtimeintertervalsinterface.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.657921 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/excel/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/excel/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      865 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/excel/exceltimeintervalsinterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5813 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/datainterfaces/text/timeintervalsinterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9347 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/nwbconverter.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.661921 neuroconv-0.4.0/src/neuroconv/schemas/
+-rw-r--r--   0 runner    (1001) docker     (123)     5732 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/schemas/base_metadata_schema.json
+-rw-r--r--   0 runner    (1001) docker     (123)    11312 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/schemas/metadata_schema.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1352 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/schemas/source_schema.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2032 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/schemas/time_series_schema.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/schemas/yaml_conversion_specification_schema.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.661921 neuroconv-0.4.0/src/neuroconv/tools/
+-rw-r--r--   0 runner    (1001) docker     (123)      119 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.661921 neuroconv-0.4.0/src/neuroconv/tools/audio/
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/audio/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3048 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/audio/audio.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15556 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/data_transfers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3331 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/figshare.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4374 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/hdmf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4311 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/importing.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.661921 neuroconv-0.4.0/src/neuroconv/tools/neo/
+-rw-r--r--   0 runner    (1001) docker     (123)      176 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/neo/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19744 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/neo/neo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7524 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/nwb_helpers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3743 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/path_expansion.py
+-rw-r--r--   0 runner    (1001) docker     (123)      904 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/processes.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.661921 neuroconv-0.4.0/src/neuroconv/tools/roiextractors/
+-rw-r--r--   0 runner    (1001) docker     (123)      389 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/roiextractors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5671 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/roiextractors/imagingextractordatachunkiterator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    46767 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/roiextractors/roiextractors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/signal_processing.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.665921 neuroconv-0.4.0/src/neuroconv/tools/spikeinterface/
+-rw-r--r--   0 runner    (1001) docker     (123)      309 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/spikeinterface/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    69197 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/spikeinterface/spikeinterface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3925 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/spikeinterface/spikeinterfacerecordingdatachunkiterator.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.665921 neuroconv-0.4.0/src/neuroconv/tools/testing/
+-rw-r--r--   0 runner    (1001) docker     (123)      217 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/testing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4849 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/testing/_path_expander_demo_ibl_filepaths.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    33413 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/testing/data_interface_mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1013 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/testing/mock_files.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6437 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/testing/mock_interfaces.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12328 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/testing/mock_ttl_signals.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2074 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/text.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.665921 neuroconv-0.4.0/src/neuroconv/tools/yaml_conversion_specification/
+-rw-r--r--   0 runner    (1001) docker     (123)       68 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/yaml_conversion_specification/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6750 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/tools/yaml_conversion_specification/yaml_conversion_specification.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.665921 neuroconv-0.4.0/src/neuroconv/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)      590 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      621 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/utils/checks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9587 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/utils/dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13816 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/utils/json_schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)      417 2023-07-23 19:19:32.000000 neuroconv-0.4.0/src/neuroconv/utils/types.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:19:38.641921 neuroconv-0.4.0/src/neuroconv.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4455 2023-07-23 19:19:38.000000 neuroconv-0.4.0/src/neuroconv.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8776 2023-07-23 19:19:38.000000 neuroconv-0.4.0/src/neuroconv.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:19:38.000000 neuroconv-0.4.0/src/neuroconv.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      135 2023-07-23 19:19:38.000000 neuroconv-0.4.0/src/neuroconv.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     4189 2023-07-23 19:19:38.000000 neuroconv-0.4.0/src/neuroconv.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 19:19:38.000000 neuroconv-0.4.0/src/neuroconv.egg-info/top_level.txt
```

### Comparing `neuroconv-0.3.0/PKG-INFO` & `neuroconv-0.4.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,59 +1,61 @@
 Metadata-Version: 2.1
 Name: neuroconv
-Version: 0.3.0
+Version: 0.4.0
 Summary: Convert data from proprietary formats to NWB format.
 Home-page: https://github.com/catalystneuro/neuroconv
 Author: Cody Baker, Szonja Weigl, Heberto Mayorquin, Luiz Tauffer, and Ben Dichter.
 Author-email: ben.dichter@catalystneuro.com
+License: BSD-3-Clause
 Keywords: nwb
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: test
 Provides-Extra: docs
 Provides-Extra: full
 Provides-Extra: ophys
-Provides-Extra: sbx
-Provides-Extra: brukertiff
+Provides-Extra: scanimage
+Provides-Extra: sima
 Provides-Extra: micromanagertiff
-Provides-Extra: caiman
-Provides-Extra: cnmfe
+Provides-Extra: sbx
 Provides-Extra: hdf5
+Provides-Extra: extract
 Provides-Extra: suite2p
-Provides-Extra: sima
-Provides-Extra: scanimage
+Provides-Extra: miniscope
 Provides-Extra: tiff
-Provides-Extra: extract
+Provides-Extra: caiman
+Provides-Extra: cnmfe
+Provides-Extra: brukertiff
 Provides-Extra: ecephys
-Provides-Extra: intan
-Provides-Extra: kilosort
-Provides-Extra: mearec
-Provides-Extra: alphaomega
-Provides-Extra: cellexplorer
-Provides-Extra: phy
-Provides-Extra: spike2
 Provides-Extra: mcsraw
+Provides-Extra: tdt
+Provides-Extra: neuralynx
+Provides-Extra: cellexplorer
+Provides-Extra: alphaomega
+Provides-Extra: blackrock
+Provides-Extra: edf
 Provides-Extra: spikeinterface
 Provides-Extra: maxwell
+Provides-Extra: intan
+Provides-Extra: neuroscope
 Provides-Extra: spikegadgets
-Provides-Extra: edf
+Provides-Extra: axona
 Provides-Extra: spikeglx
-Provides-Extra: blackrock
-Provides-Extra: tdt
+Provides-Extra: spike2
 Provides-Extra: biocam
-Provides-Extra: neuralynx
-Provides-Extra: axona
-Provides-Extra: neuroscope
+Provides-Extra: phy
+Provides-Extra: mearec
+Provides-Extra: kilosort
 Provides-Extra: openephys
 Provides-Extra: plexon
 Provides-Extra: icephys
 Provides-Extra: abf
-Provides-Extra: sleap
-Provides-Extra: behavior
 Provides-Extra: video
+Provides-Extra: behavior
+Provides-Extra: sleap
 Provides-Extra: deeplabcut
 Provides-Extra: audio
 Provides-Extra: csv
 Provides-Extra: excel
 Provides-Extra: text
 License-File: license.txt
```

#### html2text {}

```diff
@@ -1,37 +1,37 @@
-Metadata-Version: 2.1 Name: neuroconv Version: 0.3.0 Summary: Convert data from
+Metadata-Version: 2.1 Name: neuroconv Version: 0.4.0 Summary: Convert data from
 proprietary formats to NWB format. Home-page: https://github.com/catalystneuro/
 neuroconv Author: Cody Baker, Szonja Weigl, Heberto Mayorquin, Luiz Tauffer,
-and Ben Dichter. Author-email: ben.dichter@catalystneuro.com Keywords: nwb
-Requires-Python: >=3.8 Description-Content-Type: text/markdown Provides-Extra:
-test Provides-Extra: docs Provides-Extra: full Provides-Extra: ophys Provides-
-Extra: sbx Provides-Extra: brukertiff Provides-Extra: micromanagertiff
-Provides-Extra: caiman Provides-Extra: cnmfe Provides-Extra: hdf5 Provides-
-Extra: suite2p Provides-Extra: sima Provides-Extra: scanimage Provides-Extra:
-tiff Provides-Extra: extract Provides-Extra: ecephys Provides-Extra: intan
-Provides-Extra: kilosort Provides-Extra: mearec Provides-Extra: alphaomega
-Provides-Extra: cellexplorer Provides-Extra: phy Provides-Extra: spike2
-Provides-Extra: mcsraw Provides-Extra: spikeinterface Provides-Extra: maxwell
-Provides-Extra: spikegadgets Provides-Extra: edf Provides-Extra: spikeglx
-Provides-Extra: blackrock Provides-Extra: tdt Provides-Extra: biocam Provides-
-Extra: neuralynx Provides-Extra: axona Provides-Extra: neuroscope Provides-
-Extra: openephys Provides-Extra: plexon Provides-Extra: icephys Provides-Extra:
-abf Provides-Extra: sleap Provides-Extra: behavior Provides-Extra: video
-Provides-Extra: deeplabcut Provides-Extra: audio Provides-Extra: csv Provides-
-Extra: excel Provides-Extra: text License-File: license.txt [![PyPI version]
-(https://badge.fury.io/py/neuroconv.svg)](https://badge.fury.io/py/
-neuroconv.svg) ![Full Tests](https://github.com/catalystneuro/neuroconv/
-actions/workflows/testing.yml/badge.svg) ![Auto-release](https://github.com/
-catalystneuro/neuroconv/actions/workflows/auto-publish.yml/badge.svg) [!
-[codecov](https://codecov.io/github/catalystneuro/neuroconv/
-coverage.svg?branch=main)](https://codecov.io/github/catalystneuro/
-neuroconv?branch=main) [![documentation](https://readthedocs.org/projects/
-neuroconv/badge/?version=main)](https://neuroconv.readthedocs.io/en/main/) [!
-[License](https://img.shields.io/pypi/l/neuroconv.svg)](https://github.com/
-catalystneuro/neuroconv/license.txt)
+and Ben Dichter. Author-email: ben.dichter@catalystneuro.com License: BSD-3-
+Clause Keywords: nwb Requires-Python: >=3.8 Description-Content-Type: text/
+markdown Provides-Extra: test Provides-Extra: docs Provides-Extra: full
+Provides-Extra: ophys Provides-Extra: scanimage Provides-Extra: sima Provides-
+Extra: micromanagertiff Provides-Extra: sbx Provides-Extra: hdf5 Provides-
+Extra: extract Provides-Extra: suite2p Provides-Extra: miniscope Provides-
+Extra: tiff Provides-Extra: caiman Provides-Extra: cnmfe Provides-Extra:
+brukertiff Provides-Extra: ecephys Provides-Extra: mcsraw Provides-Extra: tdt
+Provides-Extra: neuralynx Provides-Extra: cellexplorer Provides-Extra:
+alphaomega Provides-Extra: blackrock Provides-Extra: edf Provides-Extra:
+spikeinterface Provides-Extra: maxwell Provides-Extra: intan Provides-Extra:
+neuroscope Provides-Extra: spikegadgets Provides-Extra: axona Provides-Extra:
+spikeglx Provides-Extra: spike2 Provides-Extra: biocam Provides-Extra: phy
+Provides-Extra: mearec Provides-Extra: kilosort Provides-Extra: openephys
+Provides-Extra: plexon Provides-Extra: icephys Provides-Extra: abf Provides-
+Extra: video Provides-Extra: behavior Provides-Extra: sleap Provides-Extra:
+deeplabcut Provides-Extra: audio Provides-Extra: csv Provides-Extra: excel
+Provides-Extra: text License-File: license.txt [![PyPI version](https://
+badge.fury.io/py/neuroconv.svg)](https://badge.fury.io/py/neuroconv.svg) ![Full
+Tests](https://github.com/catalystneuro/neuroconv/actions/workflows/
+testing.yml/badge.svg) ![Auto-release](https://github.com/catalystneuro/
+neuroconv/actions/workflows/auto-publish.yml/badge.svg) [![codecov](https://
+codecov.io/github/catalystneuro/neuroconv/coverage.svg?branch=main)](https://
+codecov.io/github/catalystneuro/neuroconv?branch=main) [![documentation](https:
+//readthedocs.org/projects/neuroconv/badge/?version=main)](https://
+neuroconv.readthedocs.io/en/main/) [![License](https://img.shields.io/pypi/l/
+neuroconv.svg)](https://github.com/catalystneuro/neuroconv/license.txt)
                                [NeuroConv logo]
           **** Automatically convert neurophysiology data to NWB ****
                          Explore_our_documentation_Â»
  ## Table of Contents - [About](#about) - [Installation](#installation) -
 [Documentation](#documentation) - [License](#license) ## About NeuroConv is a
 Python package for converting neurophysiology data in a variety of proprietary
 formats to the [Neurodata Without Borders (NWB)](http://nwb.org) standard.
```

### Comparing `neuroconv-0.3.0/README.md` & `neuroconv-0.4.0/README.md`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/license.txt` & `neuroconv-0.4.0/license.txt`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/pyproject.toml` & `neuroconv-0.4.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/setup.py` & `neuroconv-0.4.0/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -43,15 +43,15 @@
 gin_config_file_base = Path("./base_gin_test_config.json")
 gin_config_file_local = Path("./tests/test_on_data/gin_test_config.json")
 if not gin_config_file_local.exists():
     copy(src=gin_config_file_base, dst=gin_config_file_local)
 
 setup(
     name="neuroconv",
-    version="0.3.0",
+    version="0.4.0",
     description="Convert data from proprietary formats to NWB format.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     author="Cody Baker, Szonja Weigl, Heberto Mayorquin, Luiz Tauffer, and Ben Dichter.",
     author_email="ben.dichter@catalystneuro.com",
     url="https://github.com/catalystneuro/neuroconv",
     keywords="nwb",
@@ -63,8 +63,9 @@
     install_requires=install_requires,
     extras_require=extras_require,
     entry_points={
         "console_scripts": [
             "neuroconv = neuroconv.tools.yaml_conversion_specification.yaml_conversion_specification:run_conversion_from_yaml_cli",
         ],
     },
+    license="BSD-3-Clause",
 )
```

### Comparing `neuroconv-0.3.0/src/neuroconv/basedatainterface.py` & `neuroconv-0.4.0/src/neuroconv/basedatainterface.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,49 +1,64 @@
 import uuid
+import warnings
 from abc import ABC, abstractmethod
 from pathlib import Path
 from typing import List, Optional
 
 from pynwb import NWBFile
 
-from .utils import get_schema_from_method_signature, load_dict_from_file
+from .tools.nwb_helpers import make_nwbfile_from_metadata, make_or_load_nwbfile
+from .utils import (
+    dict_deep_update,
+    get_schema_from_method_signature,
+    load_dict_from_file,
+)
 from .utils.dict import DeepDict
 
 
 class BaseDataInterface(ABC):
     """Abstract class defining the structure of all DataInterfaces."""
 
     keywords: List[str] = []
 
     @classmethod
     def get_source_schema(cls):
         """Infer the JSON schema for the source_data from the method signature (annotation typing)."""
         return get_schema_from_method_signature(cls, exclude=["source_data"])
 
-    def __init__(self, **source_data):
+    def __init__(self, verbose: bool = False, **source_data):
+        self.verbose = verbose
         self.source_data = source_data
 
-    def get_conversion_options_schema(self):
+    def get_conversion_options_schema(self) -> dict:
         """Infer the JSON schema for the conversion options from the method signature (annotation typing)."""
-        return get_schema_from_method_signature(self.run_conversion, exclude=["nwbfile", "metadata"])
+        return get_schema_from_method_signature(self.add_to_nwbfile, exclude=["nwbfile", "metadata"])
 
-    def get_metadata_schema(self):
+    def get_metadata_schema(self) -> dict:
         """Retrieve JSON schema for metadata."""
         metadata_schema = load_dict_from_file(Path(__file__).parent / "schemas" / "base_metadata_schema.json")
         return metadata_schema
 
-    def get_metadata(self):
+    def get_metadata(self) -> DeepDict:
         """Child DataInterface classes should override this to match their metadata."""
         metadata = DeepDict()
         metadata["NWBFile"]["session_description"] = "Auto-generated by neuroconv"
         metadata["NWBFile"]["identifier"] = str(uuid.uuid4())
 
         return metadata
 
+    def create_nwbfile(self, metadata=None, **conversion_options) -> NWBFile:
+        nwbfile = make_nwbfile_from_metadata(metadata)
+        self.add_to_nwbfile(nwbfile, metadata=metadata, **conversion_options)
+        return nwbfile
+
     @abstractmethod
+    def add_to_nwbfile(self, nwbfile: NWBFile, **conversion_options) -> None:
+        raise NotImplementedError()
+
     def run_conversion(
         self,
         nwbfile_path: Optional[str] = None,
         nwbfile: Optional[NWBFile] = None,
         metadata: Optional[dict] = None,
         overwrite: bool = False,
         **conversion_options,
@@ -60,8 +75,25 @@
             An in-memory NWBFile object to write to the location.
         metadata : dict, optional
             Metadata dictionary with information used to create the NWBFile when one does not exist or overwrite=True.
         overwrite : bool, default: False
             Whether to overwrite the NWBFile if one exists at the nwbfile_path.
             The default is False (append mode).
         """
-        raise NotImplementedError("The run_conversion method for this DataInterface has not been defined!")
+        if nwbfile_path is None:
+            warnings.warn(
+                "Using DataInterface.run_conversion() without specifying nwbfile_path is deprecated. To create an "
+                "NWBFile object in memory, use DataInterface.create_nwbfile(). To append to an existing NWBFile object,"
+                " use DataInterface.add_to_nwbfile()."
+            )
+
+        if metadata is None:
+            metadata = self.get_metadata()
+
+        with make_or_load_nwbfile(
+            nwbfile_path=nwbfile_path,
+            nwbfile=nwbfile,
+            metadata=metadata,
+            overwrite=overwrite,
+            verbose=getattr(self, "verbose", False),
+        ) as nwbfile_out:
+            self.add_to_nwbfile(nwbfile_out, metadata=metadata, **conversion_options)
```

### Comparing `neuroconv-0.3.0/src/neuroconv/baseextractorinterface.py` & `neuroconv-0.4.0/src/neuroconv/baseextractorinterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/basetemporalalignmentinterface.py` & `neuroconv-0.4.0/src/neuroconv/basetemporalalignmentinterface.py`

 * *Files 2% similar despite different names*

```diff
@@ -36,43 +36,43 @@
             The timestamps for the data stream.
         """
         raise NotImplementedError(
             "Unable to retrieve timestamps for this interface! Define the `get_timestamps` method for this interface."
         )
 
     @abstractmethod
-    def set_aligned_timestamps(self, aligned_timestamps: np.ndarray):
+    def set_aligned_timestamps(self, aligned_timestamps: np.ndarray) -> None:
         """
         Replace all timestamps for this interface with those aligned to the common session start time.
 
         Must be in units seconds relative to the common 'session_start_time'.
 
         Parameters
         ----------
         aligned_timestamps : numpy.ndarray
             The synchronized timestamps for data in this interface.
         """
         raise NotImplementedError(
             "The protocol for synchronizing the timestamps of this interface has not been specified!"
         )
 
-    def set_aligned_starting_time(self, aligned_starting_time: float):
+    def set_aligned_starting_time(self, aligned_starting_time: float) -> None:
         """
         Align the starting time for this interface relative to the common session start time.
 
         Must be in units seconds relative to the common 'session_start_time'.
 
         Parameters
         ----------
         aligned_starting_time : float
             The starting time for all temporal data in this interface.
         """
         self.set_aligned_timestamps(aligned_timestamps=self.get_timestamps() + aligned_starting_time)
 
-    def align_by_interpolation(self, unaligned_timestamps: np.ndarray, aligned_timestamps: np.ndarray):
+    def align_by_interpolation(self, unaligned_timestamps: np.ndarray, aligned_timestamps: np.ndarray) -> None:
         """
         Interpolate the timestamps of this interface using a mapping from some unaligned time basis to its aligned one.
 
         Use this method if the unaligned timestamps of the data in this interface are not directly tracked by a primary
         system, but are known to occur between timestamps that are tracked, then align the timestamps of this interface
         by interpolating between the two.
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/__init__.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 # Behavior
 from .behavior.audio.audiointerface import AudioInterface
 from .behavior.deeplabcut.deeplabcutdatainterface import DeepLabCutInterface
+from .behavior.miniscope.miniscopedatainterface import MiniscopeBehaviorInterface
 from .behavior.sleap.sleapdatainterface import SLEAPInterface
 from .behavior.video.videodatainterface import VideoInterface
 
 # Ecephys
 from .ecephys.alphaomega.alphaomegadatainterface import AlphaOmegaRecordingInterface
 from .ecephys.axona.axonadatainterface import (
     AxonaLFPDataInterface,
@@ -13,15 +14,19 @@
     AxonaUnitRecordingInterface,
 )
 from .ecephys.biocam.biocamdatainterface import BiocamRecordingInterface
 from .ecephys.blackrock.blackrockdatainterface import (
     BlackrockRecordingInterface,
     BlackrockSortingInterface,
 )
-from .ecephys.cellexplorer.cellexplorerdatainterface import CellExplorerSortingInterface
+from .ecephys.cellexplorer.cellexplorerdatainterface import (
+    CellExplorerLFPInterface,
+    CellExplorerRecordingInterface,
+    CellExplorerSortingInterface,
+)
 from .ecephys.edf.edfdatainterface import EDFRecordingInterface
 from .ecephys.intan.intandatainterface import IntanRecordingInterface
 from .ecephys.kilosort.kilosortdatainterface import KiloSortSortingInterface
 from .ecephys.maxwell.maxonedatainterface import MaxOneRecordingInterface
 from .ecephys.mcsraw.mcsrawdatainterface import MCSRawRecordingInterface
 from .ecephys.mearec.mearecdatainterface import MEArecRecordingInterface
 from .ecephys.neuralynx.neuralynxdatainterface import (
@@ -68,14 +73,15 @@
 from .ophys.caiman.caimandatainterface import CaimanSegmentationInterface
 from .ophys.cnmfe.cnmfedatainterface import CnmfeSegmentationInterface
 from .ophys.extract.extractdatainterface import ExtractSegmentationInterface
 from .ophys.hdf5.hdf5datainterface import Hdf5ImagingInterface
 from .ophys.micromanagertiff.micromanagertiffdatainterface import (
     MicroManagerTiffImagingInterface,
 )
+from .ophys.miniscope.miniscopeimagingdatainterface import MiniscopeImagingInterface
 from .ophys.sbx.sbxdatainterface import SbxImagingInterface
 from .ophys.scanimage.scanimageimaginginterface import ScanImageImagingInterface
 from .ophys.sima.simadatainterface import SimaSegmentationInterface
 from .ophys.suite2p.suite2pdatainterface import Suite2pSegmentationInterface
 from .ophys.tiff.tiffdatainterface import TiffImagingInterface
 
 # Text
@@ -93,14 +99,16 @@
     SpikeGLXRecordingInterface,
     SpikeGLXLFPInterface,
     SpikeGLXNIDQInterface,
     SpikeGadgetsRecordingInterface,
     IntanRecordingInterface,
     CEDRecordingInterface,
     CellExplorerSortingInterface,
+    CellExplorerRecordingInterface,
+    CellExplorerLFPInterface,
     BlackrockRecordingInterface,
     BlackrockSortingInterface,
     OpenEphysRecordingInterface,
     OpenEphysBinaryRecordingInterface,
     OpenEphysLegacyRecordingInterface,
     OpenEphysSortingInterface,
     PhySortingInterface,
@@ -128,19 +136,21 @@
     SimaSegmentationInterface,
     SbxImagingInterface,
     TiffImagingInterface,
     Hdf5ImagingInterface,
     ScanImageImagingInterface,
     BrukerTiffImagingInterface,
     MicroManagerTiffImagingInterface,
+    MiniscopeImagingInterface,
     # Behavior
     VideoInterface,
     AudioInterface,
     DeepLabCutInterface,
     SLEAPInterface,
+    MiniscopeBehaviorInterface,
     # Text
     CsvTimeIntervalsInterface,
     ExcelTimeIntervalsInterface,
 ]
 
 interfaces_by_category = dict(
     ecephys={
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/audio/audiointerface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/audio/audiointerface.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,20 +1,24 @@
 import json
 from pathlib import Path
 from typing import List, Literal, Optional
-from warnings import warn
 
 import numpy as np
 import scipy
 from pynwb import NWBFile, TimeSeries
 
 from ....basetemporalalignmentinterface import BaseTemporalAlignmentInterface
 from ....tools.audio import add_acoustic_waveform_series
 from ....tools.nwb_helpers import make_or_load_nwbfile
-from ....utils import FilePathType, get_base_schema, get_schema_from_hdmf_class
+from ....utils import (
+    DeepDict,
+    FilePathType,
+    get_base_schema,
+    get_schema_from_hdmf_class,
+)
 
 
 def _check_audio_names_are_unique(metadata: dict):
     neurodata_names = [neurodata["name"] for neurodata in metadata]
     neurodata_names_are_unique = len(set(neurodata_names)) == len(neurodata_names)
     assert neurodata_names_are_unique, f"Some of the names for Audio metadata are not unique."
 
@@ -143,33 +147,30 @@
         )
 
         self._segment_starting_times = aligned_segment_starting_times
 
     def align_by_interpolation(self, unaligned_timestamps: np.ndarray, aligned_timestamps: np.ndarray):
         raise NotImplementedError("The AudioInterface does not yet support timestamps.")
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: Optional[FilePathType] = None,
-        nwbfile: Optional[NWBFile] = None,
+        nwbfile: NWBFile,
         metadata: Optional[dict] = None,
         stub_test: bool = False,
         stub_frames: int = 1000,
         write_as: Literal["stimulus", "acquisition"] = "stimulus",
         iterator_options: Optional[dict] = None,
         compression_options: Optional[dict] = None,
         overwrite: bool = False,
         verbose: bool = True,
     ):
         """
         Parameters
         ----------
-        nwbfile_path : FilePathType, optional
-            If a file exists at this path, append to it. If not, write the file here.
-        nwbfile : NWBFile, optional
+        nwbfile : NWBFile
             Append to this NWBFile object
         metadata : dict, optional
         stub_test : bool, default: False
         stub_frames : int, default: 1000
         write_as : {'stimulus', 'acquisition'}
             The acoustic waveform series can be added to the NWB file either as
             "stimulus" or as "acquisition".
@@ -200,30 +201,25 @@
         if self._number_of_audio_files > 1 and self._segment_starting_times is None:
             raise ValueError(
                 "If you have multiple audio files, then you must specify each starting time by calling "
                 "'.set_aligned_segment_starting_times(...)'!"
             )
         starting_times = self._segment_starting_times or [0.0]
 
-        with make_or_load_nwbfile(
-            nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata, overwrite=overwrite, verbose=self.verbose
-        ) as nwbfile_out:
-            for file_index, (acoustic_waveform_series_metadata, file_path) in enumerate(
-                zip(audio_metadata, file_paths)
-            ):
-                sampling_rate, acoustic_series = scipy.io.wavfile.read(filename=file_path, mmap=True)
-
-                if stub_test:
-                    acoustic_series = acoustic_series[:stub_frames]
-
-                add_acoustic_waveform_series(
-                    acoustic_series=acoustic_series,
-                    nwbfile=nwbfile_out,
-                    rate=sampling_rate,
-                    metadata=acoustic_waveform_series_metadata,
-                    write_as=write_as,
-                    starting_time=starting_times[file_index],
-                    iterator_options=iterator_options,
-                    compression_options=compression_options,
-                )
+        for file_index, (acoustic_waveform_series_metadata, file_path) in enumerate(zip(audio_metadata, file_paths)):
+            sampling_rate, acoustic_series = scipy.io.wavfile.read(filename=file_path, mmap=True)
+
+            if stub_test:
+                acoustic_series = acoustic_series[:stub_frames]
+
+            add_acoustic_waveform_series(
+                acoustic_series=acoustic_series,
+                nwbfile=nwbfile,
+                rate=sampling_rate,
+                metadata=acoustic_waveform_series_metadata,
+                write_as=write_as,
+                starting_time=starting_times[file_index],
+                iterator_options=iterator_options,
+                compression_options=compression_options,
+            )
 
-        return nwbfile_out
+        return nwbfile
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/deeplabcut/deeplabcutdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/deeplabcut/deeplabcutdatainterface.py`

 * *Files 15% similar despite different names*

```diff
@@ -2,16 +2,15 @@
 from typing import Optional
 
 import numpy as np
 from pynwb.file import NWBFile
 
 from ....basetemporalalignmentinterface import BaseTemporalAlignmentInterface
 from ....tools import get_package
-from ....tools.nwb_helpers import make_or_load_nwbfile
-from ....utils import FilePathType, dict_deep_update
+from ....utils import FilePathType
 
 
 def write_subject_to_nwb(nwbfile: NWBFile, h5file: FilePathType, individual_name: str, config_file: FilePathType):
     """
     Given, subject name, write h5file to an existing nwbfile.
 
     Parameters
@@ -97,41 +96,29 @@
         )
 
     def set_aligned_timestamps(self, aligned_timestamps: np.ndarray):
         raise NotImplementedError(
             "The protocol for synchronizing the timestamps of this interface has not been specified!"
         )
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: Optional[FilePathType] = None,
-        nwbfile: Optional[NWBFile] = None,
+        nwbfile: NWBFile,
         metadata: Optional[dict] = None,
-        overwrite: bool = False,
     ):
         """
         Conversion from DLC output files to nwb. Derived from dlc2nwb library.
 
         Parameters
         ----------
-        nwbfile_path: FilePathType
-            Path for where to write or load (if overwrite=False) the NWBFile.
-            If specified, this context will always write to this location.
         nwbfile: NWBFile
             nwb file to which the recording information is to be added
         metadata: dict
             metadata info for constructing the nwb file (optional).
-        overwrite: bool, optional
-            Whether to overwrite the NWBFile if one exists at the nwbfile_path.
         """
-        base_metadata = self.get_metadata()
-        metadata = dict_deep_update(base_metadata, metadata)
 
-        with make_or_load_nwbfile(
-            nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata, overwrite=overwrite, verbose=self.verbose
-        ) as nwbfile_out:
-            write_subject_to_nwb(
-                nwbfile=nwbfile_out,
-                h5file=str(self.source_data["file_path"]),
-                individual_name=self.subject_name,
-                config_file=str(self.source_data["config_file_path"]),
-            )
+        write_subject_to_nwb(
+            nwbfile=nwbfile,
+            h5file=str(self.source_data["file_path"]),
+            individual_name=self.subject_name,
+            config_file=str(self.source_data["config_file_path"]),
+        )
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/sleap/sleap_utils.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/sleap/sleap_utils.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/sleap/sleapdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/sleap/sleapdatainterface.py`

 * *Files 18% similar despite different names*

```diff
@@ -3,16 +3,15 @@
 
 import numpy as np
 from pynwb.file import NWBFile
 
 from .sleap_utils import extract_timestamps
 from ....basetemporalalignmentinterface import BaseTemporalAlignmentInterface
 from ....tools import get_package
-from ....tools.nwb_helpers import make_or_load_nwbfile
-from ....utils import FilePathType, dict_deep_update
+from ....utils import FilePathType
 
 
 class SLEAPInterface(BaseTemporalAlignmentInterface):
     """Data interface for SLEAP datasets."""
 
     def __init__(
         self,
@@ -54,47 +53,35 @@
     def get_timestamps(self) -> np.ndarray:
         timestamps = self._timestamps if self._timestamps is not None else self.get_original_timestamps()
         return timestamps
 
     def set_aligned_timestamps(self, aligned_timestamps: np.ndarray):
         self._timestamps = aligned_timestamps
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: Optional[FilePathType] = None,
-        nwbfile: Optional[NWBFile] = None,
+        nwbfile: NWBFile,
         metadata: Optional[dict] = None,
-        overwrite: bool = False,
     ):
         """
         Conversion from DLC output files to nwb. Derived from sleap-io library.
 
         Parameters
         ----------
-        nwbfile_path: FilePathType
-            Path for where to write or load (if overwrite=False) the NWBFile.
-            If specified, this context will always write to this location.
         nwbfile: NWBFile
             nwb file to which the recording information is to be added
         metadata: dict
             metadata info for constructing the nwb file (optional).
-        overwrite: bool, optional
-            Whether to overwrite the NWBFile if one exists at the nwbfile_path.
         """
-        base_metadata = self.get_metadata()
-        metadata = dict_deep_update(base_metadata, metadata)
 
         pose_estimation_metadata = dict()
         if self.video_file_path or self._timestamps:
             video_timestamps = self.get_timestamps()
             pose_estimation_metadata.update(video_timestamps=video_timestamps)
 
         if self.video_sample_rate:
             pose_estimation_metadata.update(video_sample_rate=self.video_sample_rate)
 
-        with make_or_load_nwbfile(
-            nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata, overwrite=overwrite, verbose=self.verbose
-        ) as nwbfile_out:
-            labels = self.sleap_io.load_slp(self.file_path)
-            nwbfile_out = self.sleap_io.io.nwb.append_nwb_data(
-                labels=labels, nwbfile=nwbfile_out, pose_estimation_metadata=pose_estimation_metadata
-            )
+        labels = self.sleap_io.load_slp(self.file_path)
+        self.sleap_io.io.nwb.append_nwb_data(
+            labels=labels, nwbfile=nwbfile, pose_estimation_metadata=pose_estimation_metadata
+        )
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/video/video_utils.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/video/video_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from typing import Iterable, Optional, Tuple
+from typing import Optional, Tuple
 
 import numpy as np
 from hdmf.data_utils import GenericDataChunkIterator
 from tqdm import tqdm
 
 from ....tools import get_package
 from ....utils import FilePathType
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/behavior/video/videodatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/behavior/video/videodatainterface.py`

 * *Files 4% similar despite different names*

```diff
@@ -9,16 +9,16 @@
 from pynwb import NWBFile
 from pynwb.image import ImageSeries
 from tqdm import tqdm
 
 from .video_utils import VideoCaptureContext
 from ....basedatainterface import BaseDataInterface
 from ....tools import get_package
-from ....tools.nwb_helpers import get_module, make_or_load_nwbfile
-from ....utils import FilePathType, get_base_schema, get_schema_from_hdmf_class
+from ....tools.nwb_helpers import get_module
+from ....utils import get_base_schema, get_schema_from_hdmf_class
 
 
 class VideoInterface(BaseDataInterface):
     """Data interface for writing videos as ImageSeries."""
 
     def __init__(self, file_paths: list, verbose: bool = False):  # TODO - debug why List[FilePathType] fails
         """
@@ -219,20 +219,18 @@
             )
         else:
             self._segment_starting_times = aligned_segment_starting_times
 
     def align_by_interpolation(self, unaligned_timestamps: np.ndarray, aligned_timestamps: np.ndarray):
         raise NotImplementedError("The `align_by_interpolation` method has not been developed for this interface yet.")
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: Optional[FilePathType] = None,
-        nwbfile: Optional[NWBFile] = None,
+        nwbfile: NWBFile,
         metadata: Optional[dict] = None,
-        overwrite: bool = False,
         stub_test: bool = False,
         external_mode: bool = True,
         starting_frames: Optional[list] = None,
         chunk_data: bool = True,
         module_name: Optional[str] = None,
         module_description: Optional[str] = None,
         compression: Optional[str] = "gzip",
@@ -241,17 +239,14 @@
         """
         Convert the video data files to :py:class:`~pynwb.image.ImageSeries` and write them in the
         :py:class:`~pynwb.file.NWBFile`. Data is written in the :py:class:`~pynwb.image.ImageSeries` container as
         RGB. [times, x, y, 3-RGB].
 
         Parameters
         ----------
-        nwbfile_path : FilePathType, optional
-            Path for where to write or load (if overwrite=False) the NWB file.
-            If specified, this context will always write to this location.
         nwbfile : NWBFile, optional
             nwb file to which the recording information is to be added
         metadata : dict, optional
             Dictionary of metadata information such as names and description of each video.
             Metadata should be passed for each video file passed in the file_paths.
             If storing as 'external mode', then provide duplicate metadata for video files that go in the
             same :py:class:`~pynwb.image.ImageSeries` container.
@@ -267,16 +262,14 @@
                     )
                 )
             and may contain most keywords normally accepted by an ImageSeries
             (https://pynwb.readthedocs.io/en/stable/pynwb.image.html#pynwb.image.ImageSeries).
             The list for the 'Videos' key should correspond one to the video files in the file_paths list.
             If multiple videos need to be in the same :py:class:`~pynwb.image.ImageSeries`, then supply the same value for "name" key.
             Storing multiple videos in the same :py:class:`~pynwb.image.ImageSeries` is only supported if 'external_mode'=True.
-        overwrite : bool, default: False
-            Whether to overwrite the NWBFile if one exists at the nwbfile_path.
         stub_test : bool, default: False
             If ``True``, truncates the write operation for fast testing.
         external_mode : bool, default: True
             :py:class:`~pynwb.image.ImageSeries` may contain either video data or file paths to external video files.
             If True, this utilizes the more efficient method of writing the relative path to the video files (recommended).
         starting_frames : list, optional
             List of start frames for each video written using external mode.
@@ -296,14 +289,16 @@
             Compression strategy to use for :py:class:`hdmf.backends.hdf5.h5_utils.H5DataIO`. For full list of currently
             supported filters, see
             https://docs.h5py.org/en/latest/high/dataset.html#lossless-compression-filters
         compression_options: int, optional
             Parameter(s) for compression filter. Currently, only supports the compression level (integer from 0 to 9) of
             compression="gzip".
         """
+        metadata = metadata or dict()
+
         file_paths = self.source_data["file_paths"]
 
         videos_metadata = metadata.get("Behavior", dict()).get("Videos", None)
         if videos_metadata is None:
             videos_metadata = self.get_metadata()["Behavior"]["Videos"]
 
         assert len(videos_metadata) == self._number_of_files, (
@@ -316,124 +311,119 @@
         any_duplicated_video_names = len(set(videos_name_list)) < len(videos_name_list)
         if any_duplicated_video_names:
             raise ValueError("There are duplicated file names in the metadata!")
 
         # Iterate over unique videos
         stub_frames = 10
         timing_type = self.get_timing_type()
-        with make_or_load_nwbfile(
-            nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata, overwrite=overwrite, verbose=self.verbose
-        ) as nwbfile_out:
-            if external_mode:
-                image_series_kwargs = videos_metadata[0]
-                if self._number_of_files > 1 and starting_frames is None:
-                    raise TypeError(
-                        "Multiple paths were specified for the ImageSeries, but no starting_frames were specified!"
-                    )
-                elif starting_frames is not None and len(starting_frames) != self._number_of_files:
-                    raise ValueError(
-                        f"Multiple paths ({self._number_of_files}) were specified for the ImageSeries, "
-                        f"but the length of starting_frames ({len(starting_frames)}) did not match the number of paths!"
+        if external_mode:
+            image_series_kwargs = videos_metadata[0]
+            if self._number_of_files > 1 and starting_frames is None:
+                raise TypeError(
+                    "Multiple paths were specified for the ImageSeries, but no starting_frames were specified!"
+                )
+            elif starting_frames is not None and len(starting_frames) != self._number_of_files:
+                raise ValueError(
+                    f"Multiple paths ({self._number_of_files}) were specified for the ImageSeries, "
+                    f"but the length of starting_frames ({len(starting_frames)}) did not match the number of paths!"
+                )
+            elif starting_frames is not None:
+                image_series_kwargs.update(starting_frame=starting_frames)
+
+            image_series_kwargs.update(format="external", external_file=file_paths)
+
+            if timing_type == "starting_time and rate":
+                starting_time = self._segment_starting_times[0] if self._segment_starting_times is not None else 0.0
+                with VideoCaptureContext(file_path=str(file_paths[0])) as video:
+                    rate = video.get_video_fps()
+                image_series_kwargs.update(starting_time=starting_time, rate=rate)
+            elif timing_type == "timestamps":
+                image_series_kwargs.update(timestamps=np.concatenate(self._timestamps))
+            else:
+                raise ValueError(f"Unrecognized timing_type: {timing_type}")
+        else:
+            for file_index, (image_series_kwargs, file) in enumerate(zip(videos_metadata, file_paths)):
+                if self._number_of_files > 1:
+                    raise NotImplementedError(
+                        "Multiple file_paths with external_mode=False is not yet supported! "
+                        "Please initialize a separate VideoInterface for each file."
                     )
-                elif starting_frames is not None:
-                    image_series_kwargs.update(starting_frame=starting_frames)
 
-                image_series_kwargs.update(format="external", external_file=file_paths)
+                uncompressed_estimate = Path(file).stat().st_size * 70
+                available_memory = psutil.virtual_memory().available
+                if not chunk_data and not stub_test and uncompressed_estimate >= available_memory:
+                    warn(
+                        f"Not enough memory (estimated {round(uncompressed_estimate/1e9, 2)} GB) to load video file as "
+                        f"array ({round(available_memory/1e9, 2)} GB available)! Forcing chunk_data to True."
+                    )
+                    chunk_data = True
+                with VideoCaptureContext(str(file)) as video_capture_ob:
+                    if stub_test:
+                        video_capture_ob.frame_count = stub_frames
+                    total_frames = video_capture_ob.get_video_frame_count()
+                    frame_shape = video_capture_ob.get_frame_shape()
+
+                maxshape = (total_frames, *frame_shape)
+                tqdm_pos, tqdm_mininterval = (0, 10)
+
+                if chunk_data:
+                    chunks = (1, frame_shape[0], frame_shape[1], 3)  # best_gzip_chunk
+                    video_capture_ob = VideoCaptureContext(str(file))
+                    if stub_test:
+                        video_capture_ob.frame_count = stub_frames
+                    iterable = DataChunkIterator(
+                        data=tqdm(
+                            iterable=video_capture_ob,
+                            desc=f"Copying video data for {Path(file).name}",
+                            position=tqdm_pos,
+                            total=total_frames,
+                            mininterval=tqdm_mininterval,
+                        ),
+                        iter_axis=0,  # nwb standard is time as zero axis
+                        maxshape=maxshape,
+                    )
 
-                if timing_type == "starting_time and rate":
-                    starting_time = self._segment_starting_times[0] if self._segment_starting_times is not None else 0.0
-                    with VideoCaptureContext(file_path=str(file_paths[0])) as video:
-                        rate = video.get_video_fps()
-                    image_series_kwargs.update(starting_time=starting_time, rate=rate)
-                elif timing_type == "timestamps":
-                    image_series_kwargs.update(timestamps=np.concatenate(self._timestamps))
                 else:
-                    raise ValueError(f"Unrecognized timing_type: {timing_type}")
-            else:
-                for file_index, (image_series_kwargs, file) in enumerate(zip(videos_metadata, file_paths)):
-                    if self._number_of_files > 1:
-                        raise NotImplementedError(
-                            "Multiple file_paths with external_mode=False is not yet supported! "
-                            "Please initialize a separate VideoInterface for each file."
-                        )
-
-                    uncompressed_estimate = Path(file).stat().st_size * 70
-                    available_memory = psutil.virtual_memory().available
-                    if not chunk_data and not stub_test and uncompressed_estimate >= available_memory:
-                        warn(
-                            f"Not enough memory (estimated {round(uncompressed_estimate/1e9, 2)} GB) to load video file as "
-                            f"array ({round(available_memory/1e9, 2)} GB available)! Forcing chunk_data to True."
-                        )
-                        chunk_data = True
+                    # Load the video
+                    chunks = None
+                    video = np.zeros(shape=maxshape, dtype="uint8")
                     with VideoCaptureContext(str(file)) as video_capture_ob:
                         if stub_test:
                             video_capture_ob.frame_count = stub_frames
-                        total_frames = video_capture_ob.get_video_frame_count()
-                        frame_shape = video_capture_ob.get_frame_shape()
-
-                    maxshape = (total_frames, *frame_shape)
-                    tqdm_pos, tqdm_mininterval = (0, 10)
+                        with tqdm(
+                            desc=f"Reading video data for {Path(file).name}",
+                            position=tqdm_pos,
+                            total=total_frames,
+                            mininterval=tqdm_mininterval,
+                        ) as pbar:
+                            for n, frame in enumerate(video_capture_ob):
+                                video[n, :, :, :] = frame
+                                pbar.update(1)
+                    iterable = video
+
+                # Wrap data for compression
+                wrapped_io_data = H5DataIO(
+                    iterable,
+                    compression=compression,
+                    compression_opts=compression_options,
+                    chunks=chunks,
+                )
+                image_series_kwargs.update(data=wrapped_io_data)
 
-                    if chunk_data:
-                        chunks = (1, frame_shape[0], frame_shape[1], 3)  # best_gzip_chunk
-                        video_capture_ob = VideoCaptureContext(str(file))
-                        if stub_test:
-                            video_capture_ob.frame_count = stub_frames
-                        iterable = DataChunkIterator(
-                            data=tqdm(
-                                iterable=video_capture_ob,
-                                desc=f"Copying video data for {Path(file).name}",
-                                position=tqdm_pos,
-                                total=total_frames,
-                                mininterval=tqdm_mininterval,
-                            ),
-                            iter_axis=0,  # nwb standard is time as zero axis
-                            maxshape=maxshape,
-                        )
-
-                    else:
-                        # Load the video
-                        chunks = None
-                        video = np.zeros(shape=maxshape, dtype="uint8")
-                        with VideoCaptureContext(str(file)) as video_capture_ob:
-                            if stub_test:
-                                video_capture_ob.frame_count = stub_frames
-                            with tqdm(
-                                desc=f"Reading video data for {Path(file).name}",
-                                position=tqdm_pos,
-                                total=total_frames,
-                                mininterval=tqdm_mininterval,
-                            ) as pbar:
-                                for n, frame in enumerate(video_capture_ob):
-                                    video[n, :, :, :] = frame
-                                    pbar.update(1)
-                        iterable = video
-
-                    # Wrap data for compression
-                    wrapped_io_data = H5DataIO(
-                        iterable,
-                        compression=compression,
-                        compression_opts=compression_options,
-                        chunks=chunks,
+                if timing_type == "starting_time and rate":
+                    starting_time = (
+                        self._segment_starting_times[file_index] if self._segment_starting_times is not None else 0.0
                     )
-                    image_series_kwargs.update(data=wrapped_io_data)
+                    with VideoCaptureContext(file_path=str(file)) as video:
+                        rate = video.get_video_fps()
+                    image_series_kwargs.update(starting_time=starting_time, rate=rate)
+                elif timing_type == "timestamps":
+                    image_series_kwargs.update(timestamps=self._timestamps[file_index])
 
-                    if timing_type == "starting_time and rate":
-                        starting_time = (
-                            self._segment_starting_times[file_index]
-                            if self._segment_starting_times is not None
-                            else 0.0
-                        )
-                        with VideoCaptureContext(file_path=str(file)) as video:
-                            rate = video.get_video_fps()
-                        image_series_kwargs.update(starting_time=starting_time, rate=rate)
-                    elif timing_type == "timestamps":
-                        image_series_kwargs.update(timestamps=self._timestamps[file_index])
-
-            # Attach image series
-            image_series = ImageSeries(**image_series_kwargs)
-            if module_name is None:
-                nwbfile_out.add_acquisition(image_series)
-            else:
-                get_module(nwbfile=nwbfile_out, name=module_name, description=module_description).add(image_series)
+        # Attach image series
+        image_series = ImageSeries(**image_series_kwargs)
+        if module_name is None:
+            nwbfile.add_acquisition(image_series)
+        else:
+            get_module(nwbfile=nwbfile, name=module_name, description=module_description).add(image_series)
 
-        return nwbfile_out
+        return nwbfile
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/alphaomega/alphaomegadatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/alphaomega/alphaomegadatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/axona/axona_utils.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/axona/axona_utils.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/axona/axonadatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/axona/axonadatainterface.py`

 * *Files 1% similar despite different names*

```diff
@@ -141,15 +141,15 @@
     def get_source_schema(cls) -> dict:
         return get_schema_from_method_signature(cls.__init__)
 
     def __init__(self, file_path: str):
         super().__init__(filename=file_path)
         self.source_data(file_path=file_path)
 
-    def run_conversion(self, nwbfile: NWBFile, metadata: dict):
+    def add_to_nwbfile(self, nwbfile: NWBFile, metadata: dict):
         """
         Run conversion for this data interface.
         Parameters
         ----------
         nwbfile : NWBFile
         metadata : dict
         """
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/baselfpextractorinterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/baselfpextractorinterface.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,13 +1,12 @@
 from typing import Literal, Optional
 
 from pynwb import NWBFile
 
 from .baserecordingextractorinterface import BaseRecordingExtractorInterface
-from ...utils import FilePathType
 
 
 class BaseLFPExtractorInterface(BaseRecordingExtractorInterface):
     """Primary class for all LFP data interfaces."""
 
     keywords = BaseRecordingExtractorInterface.keywords + [
         "extracellular electrophysiology",
@@ -15,34 +14,30 @@
         "local field potential",
         "LF",
     ]
 
     def __init__(self, verbose: bool = True, es_key: str = "ElectricalSeriesLFP", **source_data):
         super().__init__(verbose=verbose, es_key=es_key, **source_data)
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: Optional[FilePathType] = None,
         nwbfile: Optional[NWBFile] = None,
         metadata: Optional[dict] = None,
-        overwrite: bool = False,
         stub_test: bool = False,
         starting_time: Optional[float] = None,
         write_as: Literal["raw", "lfp", "processed"] = "lfp",
         write_electrical_series: bool = True,
-        compression: Optional[str] = None,
+        compression: Optional[str] = "gzip",
         compression_opts: Optional[int] = None,
         iterator_type: str = "v2",
         iterator_opts: Optional[dict] = None,
     ):
-        return super().run_conversion(
-            nwbfile_path=nwbfile_path,
+        return super().add_to_nwbfile(
             nwbfile=nwbfile,
             metadata=metadata,
-            overwrite=overwrite,
             stub_test=stub_test,
             starting_time=starting_time,
             write_as=write_as,
             write_electrical_series=write_electrical_series,
             compression=compression,
             compression_opts=compression_opts,
             iterator_type=iterator_type,
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/baserecordingextractorinterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/baserecordingextractorinterface.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,20 +3,15 @@
 
 import numpy as np
 from pynwb import NWBFile
 from pynwb.device import Device
 from pynwb.ecephys import ElectricalSeries, ElectrodeGroup
 
 from ...baseextractorinterface import BaseExtractorInterface
-from ...utils import (
-    FilePathType,
-    NWBMetaDataEncoder,
-    get_base_schema,
-    get_schema_from_hdmf_class,
-)
+from ...utils import NWBMetaDataEncoder, get_base_schema, get_schema_from_hdmf_class
 
 
 class BaseRecordingExtractorInterface(BaseExtractorInterface):
     """Parent class for all RecordingExtractorInterfaces."""
 
     keywords = BaseExtractorInterface.keywords + ["extracellular electrophysiology", "voltage", "recording"]
     ExtractorModuleName = "spikeinterface.extractors"
@@ -262,46 +257,39 @@
             segment.frame_slice(start_frame=0, end_frame=end_frame)
             for segment, end_frame in zip(recording_segments, end_frame_list)
         ]
         recording_extractor = ConcatenateSegmentRecording(recording_segments_stubbed)
 
         return recording_extractor
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: Optional[FilePathType] = None,
-        nwbfile: Optional[NWBFile] = None,
+        nwbfile: NWBFile,
         metadata: Optional[dict] = None,
-        overwrite: bool = False,
         stub_test: bool = False,
         starting_time: Optional[float] = None,
         write_as: Literal["raw", "lfp", "processed"] = "raw",
         write_electrical_series: bool = True,
-        compression: Optional[str] = None,
+        compression: Optional[str] = "gzip",
         compression_opts: Optional[int] = None,
         iterator_type: str = "v2",
         iterator_opts: Optional[dict] = None,
     ):
         """
         Primary function for converting raw (unprocessed) RecordingExtractor data to the NWB standard.
 
         Parameters
         ----------
-        nwbfile_path : FilePathType
-            Path for where to write or load (if overwrite=False) the NWBFile.
-            If specified, this context will always write to this location.
-        nwbfile : NWBFile, optional
+        nwbfile : NWBFile
             NWBFile to which the recording information is to be added
         metadata : dict, optional
             metadata info for constructing the NWB file.
             Should be of the format::
 
                 metadata['Ecephys']['ElectricalSeries'] = dict(name=my_name, description=my_description)
-        overwrite: bool, default: False
-            Whether to overwrite the NWB file if one exists at the nwbfile_path.
         The default is False (append mode).
         starting_time : float, optional
             Sets the starting time of the ElectricalSeries to a manually set value.
         stub_test : bool, default: False
             If True, will truncate the data to run the conversion faster and take up less memory.
         write_as : {'raw', 'lfp', 'processed'}
         write_electrical_series : bool, default: True
@@ -333,28 +321,25 @@
                     Cannot be set if `chunk_mb` is also specified.
                 display_progress : bool, default: False
                     Display a progress bar with iteration rate and estimated completion time.
                 progress_bar_options : dict, optional
                     Dictionary of keyword arguments to be passed directly to tqdm.
                     See https://github.com/tqdm/tqdm#parameters for options.
         """
-        from ...tools.spikeinterface import write_recording
+        from ...tools.spikeinterface import add_recording
 
         if stub_test or self.subset_channels is not None:
             recording = self.subset_recording(stub_test=stub_test)
         else:
             recording = self.recording_extractor
 
-        write_recording(
+        add_recording(
             recording=recording,
-            nwbfile_path=nwbfile_path,
             nwbfile=nwbfile,
             metadata=metadata,
-            overwrite=overwrite,
-            verbose=self.verbose,
             starting_time=starting_time,
             write_as=write_as,
             write_electrical_series=write_electrical_series,
             es_key=self.es_key,
             compression=compression,
             compression_opts=compression_opts,
             iterator_type=iterator_type,
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/basesortingextractorinterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/basesortingextractorinterface.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import numpy as np
 from pynwb import NWBFile
 from pynwb.device import Device
 from pynwb.ecephys import ElectrodeGroup
 
 from .baserecordingextractorinterface import BaseRecordingExtractorInterface
 from ...baseextractorinterface import BaseExtractorInterface
-from ...utils import OptionalFilePathType, get_base_schema, get_schema_from_hdmf_class
+from ...utils import DeepDict, get_base_schema, get_schema_from_hdmf_class
 
 
 class BaseSortingExtractorInterface(BaseExtractorInterface):
     """Primary class for all SortingExtractor interfaces."""
 
     keywords = BaseExtractorInterface.keywords + ["extracellular electrophysiology", "spike sorting"]
 
@@ -222,104 +222,119 @@
                 if any(x)
             ]
         )
         end_frame = 1.1 * max_min_spike_time
         stub_sorting_extractor = self.sorting_extractor.frame_slice(start_frame=0, end_frame=end_frame)
         return stub_sorting_extractor
 
-    def run_conversion(
+    def add_channel_metadata_to_nwb(self, nwbfile: NWBFile, metadata: Optional[DeepDict] = None):
+        """
+        Add channel metadata to an NWBFile object using information extracted from a SortingExtractor and
+        optional metadata.
+
+        This function attempts to add devices, electrode groups, and electrodes to the NWBFile. If a recording is
+        associated with the SortingExtractor, it is used for metadata addition. Otherwise, it attempts to create a dummy
+        NumpyRecording based on the provided metadata. If neither is available, the function warns the user and skips the
+        metadata addition.
+
+        Parameters
+        ----------
+        nwbfile : NWBFile
+            The NWBFile object to which the metadata is added.
+        metadata : Optional[DeepDict]
+            Optional metadata to use for the addition of electrode-related data. If it's provided, it should contain an
+            "Ecephys" field with a nested "Electrodes" field.
+
+        Returns
+        -------
+        None
+
+        Raises
+        ------
+        Warning
+            If there's no recording in the sorting extractor and no electrodes metadata in the provided metadata, a warning
+            is raised and the function returns None.
+
+        Notes
+        -----
+        This function adds metadata to the `nwbfile` in-place, meaning the `nwbfile` object is modified directly.
+        """
+        from ...tools.spikeinterface import (
+            add_devices,
+            add_electrode_groups,
+            add_electrodes,
+        )
+
+        if hasattr(self, "generate_recording_with_channel_metadata"):
+            recording = self.generate_recording_with_channel_metadata()
+
+            add_devices(nwbfile=nwbfile, metadata=metadata)
+            add_electrode_groups(recording=recording, nwbfile=nwbfile, metadata=metadata)
+            add_electrodes(recording=recording, nwbfile=nwbfile, metadata=metadata)
+
+    def add_to_nwbfile(
         self,
-        nwbfile_path: OptionalFilePathType = None,
-        nwbfile: Optional[NWBFile] = None,
-        metadata: Optional[dict] = None,
-        overwrite: bool = False,
+        nwbfile: NWBFile,
+        metadata: Optional[DeepDict] = None,
         stub_test: bool = False,
         write_ecephys_metadata: bool = False,
         write_as: Literal["units", "processing"] = "units",
         units_name: str = "units",
         units_description: str = "Autogenerated by neuroconv.",
     ):
         """
         Primary function for converting the data in a SortingExtractor to NWB format.
 
         Parameters
         ----------
-        nwbfile_path : FilePathType
-            Path for where to write or load (if overwrite=False) the NWBFile.
-            If specified, the context will always write to this location.
-        nwbfile : NWBFile, optional
-            If passed, this function will fill the relevant fields within the NWBFile object.
-            E.g., calling
-                write_recording(recording=my_recording_extractor, nwbfile=my_nwbfile)
-            will result in the appropriate changes to the my_nwbfile object.
-            If neither 'nwbfile_path' nor 'nwbfile' are specified, an NWBFile object will be automatically generated
-            and returned by the function.
-        metadata : dict
+        nwbfile : NWBFile
+            Fill the relevant fields within the NWBFile object.
+        metadata : DeepDict
             Information for constructing the NWB file (optional) and units table descriptions.
             Should be of the format::
 
                 metadata["Ecephys"]["UnitProperties"] = dict(name=my_name, description=my_description)
-        overwrite : bool, optional
-            Whether to overwrite the NWB file if one exists at the nwbfile_path.
-            The default is False (append mode).
         stub_test : bool, default: False
             If True, will truncate the data to run the conversion faster and take up less memory.
         write_ecephys_metadata : bool, default: False
             Write electrode information contained in the metadata.
         write_as : {'units', 'processing'}
             How to save the units table in the nwb file. Options:
             - 'units' will save it to the official NWBFile.Units position; recommended only for the final form of the data.
             - 'processing' will save it to the processing module to serve as a historical provenance for the official table.
         units_name : str, default: 'units'
             The name of the units table. If write_as=='units', then units_name must also be 'units'.
         units_description : str, default: 'Autogenerated by neuroconv.'
         """
-        from spikeinterface import NumpyRecording
+        from ...tools.spikeinterface import add_sorting
 
-        from ...tools.spikeinterface import (
-            add_devices,
-            add_electrode_groups,
-            add_electrodes,
-            write_sorting,
-        )
+        if write_ecephys_metadata:
+            self.add_channel_metadata_to_nwb(nwbfile=nwbfile, metadata=metadata)
 
-        if write_ecephys_metadata and "Ecephys" in metadata:
-            n_channels = max([len(x["data"]) for x in metadata["Ecephys"]["Electrodes"]])
-            recording = NumpyRecording(
-                traces_list=[np.empty(shape=n_channels)],
-                sampling_frequency=self.sorting_extractor.get_sampling_frequency(),
-            )
-            add_devices(recording=recording, nwbfile=nwbfile, metadata=metadata)
-            add_electrode_groups(recording=recording, nwbfile=nwbfile, metadata=metadata)
-            add_electrodes(recording=recording, nwbfile=nwbfile, metadata=metadata)
         if stub_test:
             sorting_extractor = self.subset_sorting()
         else:
             sorting_extractor = self.sorting_extractor
+
         property_descriptions = dict()
-        for metadata_column in metadata.get("Ecephys", dict()).get("UnitProperties", []):
+        for metadata_column in metadata["Ecephys"].get("UnitProperties", []):
             property_descriptions.update({metadata_column["name"]: metadata_column["description"]})
             for unit_id in sorting_extractor.get_unit_ids():
                 # Special condition for wrapping electrode group pointers to actual object ids rather than string names
-                if metadata_column["name"] == "electrode_group":
-                    if nwbfile.electrode_groups:
-                        sorting_extractor.set_unit_property(
-                            unit_id=unit_id,
-                            property_name=metadata_column["name"],
-                            value=nwbfile.electrode_groups[
-                                self.sorting_extractor.get_unit_property(
-                                    unit_id=unit_id, property_name="electrode_group"
-                                )
-                            ],
-                        )
-        write_sorting(
+                if metadata_column["name"] == "electrode_group" and nwbfile.electrode_groups:
+                    value = nwbfile.electrode_groups[
+                        self.sorting_extractor.get_unit_property(unit_id=unit_id, property_name="electrode_group")
+                    ]
+                    sorting_extractor.set_unit_property(
+                        unit_id=unit_id,
+                        property_name=metadata_column["name"],
+                        value=value,
+                    )
+
+        add_sorting(
             sorting_extractor,
-            nwbfile_path=nwbfile_path,
             nwbfile=nwbfile,
-            metadata=metadata,
-            overwrite=overwrite,
-            verbose=self.verbose,
             property_descriptions=property_descriptions,
             write_as=write_as,
             units_name=units_name,
             units_description=units_description,
         )
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/biocam/biocamdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/biocam/biocamdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/blackrock/blackrockdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/blackrock/blackrockdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/blackrock/header_tools.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/blackrock/header_tools.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/edf/edfdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/edf/edfdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/intan/intandatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/intan/intandatainterface.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 from pathlib import Path
-from warnings import warn
 
 from pynwb.ecephys import ElectricalSeries
 
 from ..baserecordingextractorinterface import BaseRecordingExtractorInterface
 from ....tools import get_package
 from ....utils import FilePathType, get_schema_from_hdmf_class
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/kilosort/kilosortdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/kilosort/kilosortdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/maxwell/maxonedatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/maxwell/maxonedatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/mcsraw/mcsrawdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/mcsraw/mcsrawdatainterface.py`

 * *Files 3% similar despite different names*

```diff
@@ -11,14 +11,14 @@
 
     def __init__(self, file_path: FilePathType, verbose: bool = True, es_key: str = "ElectricalSeries"):
         """
         Load and prepare data for MCSRaw.
 
         Parameters
         ----------
-        folder_path: string or Path
+        file_path: string or Path
             Path to the .raw file.
         verbose: bool, default: True
             Allows verbose.
         es_key: str, default: "ElectricalSeries"
         """
         super().__init__(file_path=file_path, verbose=verbose, es_key=es_key)
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/mearec/mearecdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/mearec/mearecdatainterface.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,9 @@
 import json
 
-from pynwb.ecephys import ElectricalSeries
-
 from ..baserecordingextractorinterface import BaseRecordingExtractorInterface
 from ....utils.json_schema import NWBMetaDataEncoder, get_schema_from_hdmf_class
 from ....utils.types import FilePathType
 
 
 class MEArecRecordingInterface(BaseRecordingExtractorInterface):
     """
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuralynx/neuralynxdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuralynx/neuralynxdatainterface.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,24 +1,52 @@
 import json
-from typing import List
+from typing import List, Optional
 
 import numpy as np
 
 from ..baserecordingextractorinterface import BaseRecordingExtractorInterface
 from ..basesortingextractorinterface import BaseSortingExtractorInterface
 from ....utils import FolderPathType
 from ....utils.json_schema import dict_deep_update
 
 
 class NeuralynxRecordingInterface(BaseRecordingExtractorInterface):
     """Primary data interface for converting Neuralynx data. Uses
     :py:class:`~spikeinterface.extractors.NeuralynxRecordingExtractor`."""
 
-    def __init__(self, folder_path: FolderPathType, verbose: bool = True, es_key: str = "ElectricalSeries"):
-        super().__init__(folder_path=folder_path, verbose=verbose, all_annotations=True, es_key=es_key)
+    @classmethod
+    def get_stream_names(cls, folder_path: FolderPathType) -> List[str]:
+        from spikeinterface.extractors import NeuralynxRecordingExtractor
+
+        stream_names, _ = NeuralynxRecordingExtractor.get_streams(folder_path=folder_path)
+        return stream_names
+
+    def __init__(
+        self,
+        folder_path: FolderPathType,
+        stream_name: Optional[str] = None,
+        verbose: bool = False,
+        es_key: str = "ElectricalSeries",
+    ):
+        """
+        Initialize reading of OpenEphys binary recording.
+
+        Parameters
+        ----------
+        folder_path: FolderPathType
+            Path to OpenEphys directory.
+        stream_name : str, optional
+            The name of the recording stream to load; only required if there is more than one stream detected.
+            Call `NeuralynxRecordingInterface.get_stream_names(folder_path=...)` to see what streams are available.
+        verbose : bool, default: False
+        es_key : str, default: "ElectricalSeries"
+        """
+        super().__init__(
+            folder_path=folder_path, stream_name=stream_name, verbose=verbose, all_annotations=True, es_key=es_key
+        )
 
         # convert properties of object dtype (e.g. datetime) and bool as these are not supported by nwb
         for key in self.recording_extractor.get_property_keys():
             value = self.recording_extractor.get_property(key)
             if value.dtype == object or value.dtype == np.bool_:
                 self.recording_extractor.set_property(key, np.asarray(value, dtype=str))
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuroscope/neuroscope_utils.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuroscope/neuroscope_utils.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,8 +1,7 @@
-"""Authors: Cody Baker and Ben Dichter."""
 from datetime import datetime
 from pathlib import Path
 
 from dateutil import parser
 
 from ....tools import get_package
 
@@ -37,24 +36,47 @@
     """Auxiliary function for safe retrieval of keys at multiple depths in lxml tree."""
     for key in keys:
         root = safe_find(root, key)
     if root is not None:
         return root
 
 
-def get_shank_channels(xml_file_path: str) -> list:
+def get_neural_channels(xml_file_path: str) -> list:
     """
-    Retrieve the list of structured shank-only channels.
+    Extracts the channels corresponding to neural data from an XML file.
 
-    These are channels involved into spike detection.
-    These are a subset of channels obtained in`get_channel_goups`.
+    Parameters
+    ----------
+    xml_file_path : str
+        Path to the XML file containing the necessary data.
 
     Returns
     -------
+    list
         List reflecting the group structure of the channels.
+
+    Notes
+    -----
+    This function attempts to extract the channels that correspond to neural data,
+    specifically those that come from the probe. It uses the `spikeDetection` structure
+    in the XML file to identify the channels involved in spike detection. Channels that are
+    not involved in spike detection, such as auxiliary channels from the intan system, are excluded.
+
+    The function returns a list representing the group structure of the channels.
+
+    Example:
+    [[1, 2, 3], [4, 5, 6], [7, 8, 9]
+
+    Where [1, 2, 3] are the channels in the first group, [4, 5, 6] are the channels in the second group, etc.
+
+    Warning:
+    This function assumes that all the channels that correspond to neural data are involved in spike detection.
+    More concretely, it assumes that the channels appear on the `spikeDetection` field of the XML file.
+    If this is not the case, the function will return an incorrect list of neural channels channels.
+    Please report this as an issue if this is the case.
     """
     root = get_xml(xml_file_path)
     channel_groups = safe_find(safe_nested_find(root, ["spikeDetection", "channelGroups"]), "group", findall=True)
     if channel_groups and all([safe_find(group, "channels") is not None for group in channel_groups]):
         shank_channels = [[int(channel.text) for channel in group.find("channels")] for group in channel_groups]
         return shank_channels
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/neuroscope/neuroscopedatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/neuroscope/neuroscopedatainterface.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,37 +1,73 @@
 from pathlib import Path
 from typing import Optional
 
 import numpy as np
 
 from .neuroscope_utils import (
     get_channel_groups,
+    get_neural_channels,
     get_session_start_time,
-    get_shank_channels,
     get_xml_file_path,
 )
 from ..baselfpextractorinterface import BaseLFPExtractorInterface
 from ..baserecordingextractorinterface import BaseRecordingExtractorInterface
 from ..basesortingextractorinterface import BaseSortingExtractorInterface
 from ....tools import get_package
 from ....utils import FilePathType, FolderPathType
 
 
-def subset_shank_channels(recording_extractor, xml_file_path: str):
-    """Attempt to create a SubRecordingExtractor containing only channels related to neural data."""
-    shank_channels = get_shank_channels(xml_file_path=xml_file_path)
-
-    if shank_channels is not None:
-        channel_ids = [channel_id for group in shank_channels for channel_id in group]
-        new_ids = recording_extractor.get_channel_ids()[channel_ids]
-        sub_recording = recording_extractor.channel_slice(new_ids)
+def filter_non_neural_channels(recording_extractor, xml_file_path: str):
+    """
+    Subsets the recording extractor to only use channels corresponding to neural data.
+
+    Parameters
+    ----------
+    recording_extractor : BaseExtractor from spikeinterface
+        The original recording extractor object.
+    xml_file_path : str
+        Path to the XML file containing the Neuroscope metadata.
+
+    Returns
+    -------
+    BaseExtractor from spikeinterface
+        The subset recording extractor object.
+
+    Notes
+    -----
+    This function subsets the given recording extractor to include only channels that
+    correspond to neural data, filtering out auxiliary channels.
+
+    To identify the neural channels, it relies on the `get_neural_channels` function
+    in the `neuroscope_utils.py` module. Please refer to that function for more details and warnings.
+
+    If no neural channels are found o during the process, the original
+    recording extractor is returned unchanged. If all the channels in the original recording extractor are
+    neural channels, then the original recording extractor is returned unchanged as well.
+    """
+
+    neural_channels_as_groups = get_neural_channels(xml_file_path=xml_file_path)
+
+    if neural_channels_as_groups is None:
+        return recording_extractor
     else:
-        sub_recording = recording_extractor
+        # Flat neural channels as groups which is a list of lists and converter to str which is the representation
+        # In spikeinterface of the channel ids
+        neural_channel_ids = [str(channel_id) for group in neural_channels_as_groups for channel_id in group]
+        channel_ids_in_recorder = recording_extractor.get_channel_ids()
+
+        # Get only the channel_ids_in_recorder that are in the neural_channel_ids
+        neural_channel_ids = [channel_id for channel_id in channel_ids_in_recorder if channel_id in neural_channel_ids]
+
+        # If all the channel_ids_in_recorder are in the neural_channel_ids, return the original recording_extractor
+        if len(neural_channel_ids) == len(channel_ids_in_recorder):
+            return recording_extractor
 
-    return sub_recording
+        sub_recording = recording_extractor.channel_slice(channel_ids=neural_channel_ids)
+        return sub_recording
 
 
 def add_recording_extractor_properties(recording_extractor, gain: Optional[float] = None):
     """Automatically add properties to RecordingExtractor object."""
 
     if gain:
         recording_extractor.set_channel_gains(gain)
@@ -108,15 +144,15 @@
             xml_file_path = get_xml_file_path(data_file_path=file_path)
 
         super().__init__(file_path=file_path, verbose=verbose, es_key=es_key)
         self.source_data["xml_file_path"] = xml_file_path
 
         add_recording_extractor_properties(recording_extractor=self.recording_extractor, gain=gain)
 
-        self.recording_extractor = subset_shank_channels(
+        self.recording_extractor = filter_non_neural_channels(
             recording_extractor=self.recording_extractor, xml_file_path=xml_file_path
         )
 
     def get_metadata(self) -> dict:
         session_path = Path(self.source_data["file_path"]).parent
         session_id = session_path.stem
         xml_file_path = self.source_data.get("xml_file_path", str(session_path / f"{session_id}.xml"))
@@ -153,15 +189,15 @@
         """
         Load and prepare lfp data and corresponding metadata from the Neuroscope format (.eeg or .lfp files).
 
         Parameters
         ----------
         file_path : FilePathType
             Path to .dat file.
-        gain : Optional[float], optiona
+        gain : float, optional
             Conversion factors from int16 to Volts are not contained in xml_file_path; set them explicitly here.
             Most common value is 0.195 for an intan recording system.
             The default is None.
         xml_file_path : OptionalFilePathType, optional
             Path to .xml file containing device and electrode configuration.
             If unspecified, it will be automatically set as the only .xml file in the same folder as the .dat file.
             The default is None.
@@ -172,15 +208,15 @@
             xml_file_path = get_xml_file_path(data_file_path=file_path)
 
         super().__init__(file_path=file_path)
         self.source_data["xml_file_path"] = xml_file_path
 
         add_recording_extractor_properties(recording_extractor=self.recording_extractor, gain=gain)
 
-        self.recording_extractor = subset_shank_channels(
+        self.recording_extractor = filter_non_neural_channels(
             recording_extractor=self.recording_extractor, xml_file_path=xml_file_path
         )
 
     def get_metadata(self) -> dict:
         session_path = Path(self.source_data["file_path"]).parent
         session_id = session_path.stem
         xml_file_path = self.source_data.get("xml_file_path", str(session_path / f"{session_id}.xml"))
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/openephysbinarydatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/openephysbinarydatainterface.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,12 @@
 from contextlib import redirect_stdout
 from io import StringIO
 from typing import List, Optional
 
 from ..baserecordingextractorinterface import BaseRecordingExtractorInterface
-from ..basesortingextractorinterface import BaseSortingExtractorInterface
 from ....utils import FolderPathType, get_schema_from_method_signature
 
 
 def _open_with_pyopenephys(folder_path: FolderPathType):
     """
     Defined here to reduce duplication; used twice in the interface below.
 
@@ -62,15 +61,14 @@
         stream_name : str, optional
             The name of the recording stream to load; only required if there is more than one stream detected.
             Call `OpenEphysRecordingInterface.get_stream_names(folder_path=...)` to see what streams are available.
         stub_test : bool, default: False
         verbose : bool, default: True
         es_key : str, default: "ElectricalSeries"
         """
-        from spikeinterface.extractors import OpenEphysBinaryRecordingExtractor
 
         try:
             _open_with_pyopenephys(folder_path=folder_path)
         except Exception as error:
             # Type of error might depend on pyopenephys version and/or platform
             error_case_1 = (
                 type(error) == Exception
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/openephysdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/openephysdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/openephyslegacydatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/openephyslegacydatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/openephys/openephyssortingdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/openephys/openephyssortingdatainterface.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,12 +1,7 @@
-from contextlib import redirect_stdout
-from io import StringIO
-from typing import List, Optional
-
-from ..baserecordingextractorinterface import BaseRecordingExtractorInterface
 from ..basesortingextractorinterface import BaseSortingExtractorInterface
 from ....utils import FolderPathType, get_schema_from_method_signature
 
 
 class OpenEphysSortingInterface(BaseSortingExtractorInterface):
     """Primary data interface class for converting OpenEphys spiking data."""
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/phy/phydatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/phy/phydatainterface.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,9 +1,8 @@
-from typing import List, Optional
-from warnings import warn
+from typing import Optional
 
 from ..basesortingextractorinterface import BaseSortingExtractorInterface
 from ....utils import FolderPathType
 
 
 class PhySortingInterface(BaseSortingExtractorInterface):
     """Primary data interface class for converting Phy data. Uses
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/plexon/plexondatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/plexon/plexondatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spike2/spike2datainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spike2/spike2datainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikegadgets/spikegadgetsdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikegadgets/spikegadgetsdatainterface.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 from typing import Optional
-from warnings import warn
 
 from ..baserecordingextractorinterface import BaseRecordingExtractorInterface
 from ....utils import ArrayType, FilePathType
 
 
 class SpikeGadgetsRecordingInterface(BaseRecordingExtractorInterface):
     """Data interface class for converting data in the SpikeGadgets format.
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglx_utils.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglx_utils.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxconverter.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxconverter.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxnidqinterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/spikeglx/spikeglxnidqinterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ecephys/tdt/tdtdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ecephys/tdt/tdtdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/icephys/abf/abfdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/icephys/abf/abfdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/baseimagingextractorinterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/baseimagingextractorinterface.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 """Author: Ben Dichter."""
-from typing import Optional
+from typing import Literal, Optional
 
 import numpy as np
 from pynwb import NWBFile
 from pynwb.device import Device
-from pynwb.ophys import ImagingPlane, TwoPhotonSeries
+from pynwb.ophys import ImagingPlane, OnePhotonSeries, TwoPhotonSeries
 
 from ...baseextractorinterface import BaseExtractorInterface
 from ...utils import (
-    OptionalFilePathType,
     dict_deep_update,
     fill_defaults,
     get_base_schema,
     get_schema_from_hdmf_class,
 )
 
 
@@ -22,40 +21,56 @@
     ExtractorModuleName = "roiextractors"
 
     def __init__(self, verbose: bool = True, **source_data):
         super().__init__(**source_data)
         self.imaging_extractor = self.get_extractor()(**source_data)
         self.verbose = verbose
 
-    def get_metadata_schema(self) -> dict:
+    def get_metadata_schema(
+        self, photon_series_type: Literal["OnePhotonSeries", "TwoPhotonSeries"] = "TwoPhotonSeries"
+    ) -> dict:
         metadata_schema = super().get_metadata_schema()
 
         metadata_schema["required"] = ["Ophys"]
 
         # Initiate Ophys metadata
         metadata_schema["properties"]["Ophys"] = get_base_schema(tag="Ophys")
-        metadata_schema["properties"]["Ophys"]["required"] = ["Device", "ImagingPlane", "TwoPhotonSeries"]
+        metadata_schema["properties"]["Ophys"]["required"] = ["Device", "ImagingPlane", photon_series_type]
         metadata_schema["properties"]["Ophys"]["properties"] = dict(
             Device=dict(type="array", minItems=1, items={"$ref": "#/properties/Ophys/properties/definitions/Device"}),
             ImagingPlane=dict(
                 type="array", minItems=1, items={"$ref": "#/properties/Ophys/properties/definitions/ImagingPlane"}
             ),
-            TwoPhotonSeries=dict(
-                type="array", minItems=1, items={"$ref": "#/properties/Ophys/properties/definitions/TwoPhotonSeries"}
-            ),
+        )
+        metadata_schema["properties"]["Ophys"]["properties"].update(
+            {
+                photon_series_type: dict(
+                    type="array",
+                    minItems=1,
+                    items={"$ref": f"#/properties/Ophys/properties/definitions/{photon_series_type}"},
+                ),
+            }
         )
 
         # Schema definition for arrays
 
         imaging_plane_schema = get_schema_from_hdmf_class(ImagingPlane)
         imaging_plane_schema["properties"]["optical_channel"].pop("maxItems")
         metadata_schema["properties"]["Ophys"]["properties"]["definitions"] = dict(
             Device=get_schema_from_hdmf_class(Device),
             ImagingPlane=imaging_plane_schema,
-            TwoPhotonSeries=get_schema_from_hdmf_class(TwoPhotonSeries),
+        )
+        photon_series = dict(
+            OnePhotonSeries=OnePhotonSeries,
+            TwoPhotonSeries=TwoPhotonSeries,
+        )[photon_series_type]
+        metadata_schema["properties"]["Ophys"]["properties"]["definitions"].update(
+            {
+                photon_series_type: get_schema_from_hdmf_class(photon_series),
+            }
         )
 
         fill_defaults(metadata_schema, self.get_metadata())
         return metadata_schema
 
     def get_metadata(self) -> dict:
         from ...tools.roiextractors import get_nwb_imaging_metadata
@@ -79,32 +94,29 @@
 
     def get_timestamps(self) -> np.ndarray:
         return self.imaging_extractor.frame_to_time(frames=np.arange(stop=self.imaging_extractor.get_num_frames()))
 
     def set_aligned_timestamps(self, aligned_timestamps: np.ndarray):
         self.imaging_extractor.set_times(times=aligned_timestamps)
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: OptionalFilePathType = None,
-        nwbfile: Optional[NWBFile] = None,
+        nwbfile: NWBFile,
         metadata: Optional[dict] = None,
-        overwrite: bool = False,
+        photon_series_type: Literal["TwoPhotonSeries", "OnePhotonSeries"] = "TwoPhotonSeries",
         stub_test: bool = False,
         stub_frames: int = 100,
     ):
-        from ...tools.roiextractors import write_imaging
+        from ...tools.roiextractors import add_imaging
 
         if stub_test:
             stub_frames = min([stub_frames, self.imaging_extractor.get_num_frames()])
             imaging_extractor = self.imaging_extractor.frame_slice(start_frame=0, end_frame=stub_frames)
         else:
             imaging_extractor = self.imaging_extractor
 
-        write_imaging(
+        add_imaging(
             imaging=imaging_extractor,
-            nwbfile_path=nwbfile_path,
             nwbfile=nwbfile,
             metadata=metadata,
-            overwrite=overwrite,
-            verbose=self.verbose,
+            photon_series_type=photon_series_type,
         )
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/basesegmentationextractorinterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/basesegmentationextractorinterface.py`

 * *Files 5% similar despite different names*

```diff
@@ -3,20 +3,15 @@
 
 import numpy as np
 from pynwb import NWBFile
 from pynwb.device import Device
 from pynwb.ophys import Fluorescence, ImageSegmentation, ImagingPlane, TwoPhotonSeries
 
 from ...baseextractorinterface import BaseExtractorInterface
-from ...utils import (
-    FilePathType,
-    fill_defaults,
-    get_base_schema,
-    get_schema_from_hdmf_class,
-)
+from ...utils import fill_defaults, get_base_schema, get_schema_from_hdmf_class
 
 
 class BaseSegmentationExtractorInterface(BaseExtractorInterface):
     """Parent class for all SegmentationExtractorInterfaces."""
 
     ExtractorModuleName = "roiextractors"
 
@@ -72,38 +67,34 @@
         return self.segmentation_extractor.frame_to_time(
             frames=np.arange(stop=self.segmentation_extractor.get_num_frames())
         )
 
     def set_aligned_timestamps(self, aligned_timestamps: np.ndarray):
         self.segmentation_extractor.set_times(times=aligned_timestamps)
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: Optional[FilePathType] = None,
-        nwbfile: Optional[NWBFile] = None,
+        nwbfile: NWBFile,
         metadata: Optional[dict] = None,
-        overwrite: bool = False,
         stub_test: bool = False,
         stub_frames: int = 100,
         include_roi_centroids: bool = True,
         include_roi_acceptance: bool = True,
-        mask_type: Optional[str] = "image",  # Optional[Literal["image", "pixel", "voxel"]]
+        mask_type: Optional[str] = "image",  # Literal["image", "pixel", "voxel"]
         iterator_options: Optional[dict] = None,
         compression_options: Optional[dict] = None,
     ):
         """
 
         Parameters
         ----------
-        nwbfile_path : FilePathType, optional
-        nwbfile : NWBFile, optional
+        nwbfile : NWBFile
             The NWBFile to add the plane segmentation to.
         metadata : dict, optional
             The metadata for the interface
-        overwrite : bool, default: False
         stub_test : bool, default: False
         stub_frames : int, default: 100
         include_roi_centroids : bool, default: True
             Whether to include the ROI centroids on the PlaneSegmentation table.
             If there are a very large number of ROIs (such as in whole-brain recordings),
             you may wish to disable this for faster write speeds.
         include_roi_acceptance : bool, default: True
@@ -126,28 +117,25 @@
         compression_options : dict, optional
             The options to use when compressing the image masks of the segmentation extractor.
 
         Returns
         -------
 
         """
-        from ...tools.roiextractors import write_segmentation
+        from ...tools.roiextractors import add_segmentation
 
         if stub_test:
             stub_frames = min([stub_frames, self.segmentation_extractor.get_num_frames()])
             segmentation_extractor = self.segmentation_extractor.frame_slice(start_frame=0, end_frame=stub_frames)
         else:
             segmentation_extractor = self.segmentation_extractor
 
-        write_segmentation(
+        add_segmentation(
             segmentation_extractor=segmentation_extractor,
-            nwbfile_path=nwbfile_path,
             nwbfile=nwbfile,
             metadata=metadata,
-            overwrite=overwrite,
-            verbose=self.verbose,
             include_roi_centroids=include_roi_centroids,
             include_roi_acceptance=include_roi_acceptance,
             mask_type=mask_type,
             iterator_options=iterator_options,
             compression_options=compression_options,
         )
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/brukertiff/brukertiffdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/brukertiff/brukertiffdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/caiman/caimandatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/caiman/caimandatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/extract/extractdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/extract/extractdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/hdf5/hdf5datainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/hdf5/hdf5datainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/micromanagertiff/micromanagertiffdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/micromanagertiff/micromanagertiffdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/sbx/sbxdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/sbx/sbxdatainterface.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from ..baseimagingextractorinterface import BaseImagingExtractorInterface
-from ....utils import FilePathType, FloatType
+from ....utils import FilePathType
 
 
 class SbxImagingInterface(BaseImagingExtractorInterface):
     """Data Interface for SbxImagingExtractor."""
 
     def __init__(self, file_path: FilePathType, sampling_frequency: float = None, verbose: bool = True):
         """
```

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/scanimage/scanimageimaginginterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/scanimage/scanimageimaginginterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/sima/simadatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/sima/simadatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/suite2p/suite2pdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/suite2p/suite2pdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/ophys/tiff/tiffdatainterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/ophys/tiff/tiffdatainterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/text/excel/exceltimeintervalsinterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/text/excel/exceltimeintervalsinterface.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/datainterfaces/text/timeintervalsinterface.py` & `neuroconv-0.4.0/src/neuroconv/datainterfaces/text/timeintervalsinterface.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 from abc import abstractmethod
 from typing import Dict, Optional
 
 import numpy as np
 from pynwb import NWBFile
 
 from ...basedatainterface import BaseDataInterface
-from ...tools.nwb_helpers import make_or_load_nwbfile
 from ...tools.text import convert_df_to_time_intervals
 from ...utils.dict import load_dict_from_file
 from ...utils.types import FilePathType
 
 
 class TimeIntervalsInterface(BaseDataInterface):
     """Abstract Interface for time intervals."""
@@ -110,61 +109,46 @@
                 fp=aligned_timestamps,
                 left=2 * aligned_timestamps[0] - aligned_timestamps[1],  # If first or last values are outside alignment
                 right=2 * aligned_timestamps[-1] - aligned_timestamps[-2],  # then use the most recent diff to regress
             ),
             column=column,
         )
 
-    def run_conversion(
+    def add_to_nwbfile(
         self,
-        nwbfile_path: Optional[FilePathType] = None,
-        nwbfile: Optional[NWBFile] = None,
+        nwbfile: NWBFile,
         metadata: Optional[dict] = None,
-        overwrite: bool = False,
         tag: str = "trials",
         column_name_mapping: Dict[str, str] = None,
         column_descriptions: Dict[str, str] = None,
     ) -> NWBFile:
         """
         Run the NWB conversion for the instantiated data interface.
 
         Parameters
         ----------
-        nwbfile_path : FilePathType
-            Path for where to write or load (if overwrite=False) the NWBFile.
-            If specified, the context will always write to this location.
         nwbfile : NWBFile, optional
             An in-memory NWBFile object to write to the location.
         metadata : dict, optional
             Metadata dictionary with information used to create the NWBFile when one does not exist or overwrite=True.
-        overwrite : bool, default: False
-            Whether to overwrite the NWBFile if one exists at the nwbfile_path.
-            The default is False (append mode).
         tag : str, default: "trials"
         column_name_mapping: dict, optional
             If passed, rename subset of columns from key to value.
         column_descriptions: dict, optional
             Keys are the names of the columns (after renaming) and values are the descriptions. If not passed,
             the names of the columns are used as descriptions.
 
-        Returns
-        -------
-        NWBFile
-
         """
         metadata = metadata or self.get_metadata()
-        with make_or_load_nwbfile(
-            nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata, overwrite=overwrite, verbose=self.verbose
-        ) as nwbfile_out:
-            self.time_intervals = convert_df_to_time_intervals(
-                self.dataframe,
-                column_name_mapping=column_name_mapping,
-                column_descriptions=column_descriptions,
-                **metadata["TimeIntervals"][tag],
-            )
-            nwbfile_out.add_time_intervals(self.time_intervals)
+        self.time_intervals = convert_df_to_time_intervals(
+            self.dataframe,
+            column_name_mapping=column_name_mapping,
+            column_descriptions=column_descriptions,
+            **metadata["TimeIntervals"][tag],
+        )
+        nwbfile.add_time_intervals(self.time_intervals)
 
-        return nwbfile_out
+        return nwbfile
 
     @abstractmethod
     def _read_file(self, file_path: FilePathType, **read_kwargs):
         pass
```

### Comparing `neuroconv-0.3.0/src/neuroconv/nwbconverter.py` & `neuroconv-0.4.0/src/neuroconv/nwbconverter.py`

 * *Files 8% similar despite different names*

```diff
@@ -21,28 +21,28 @@
 
 class NWBConverter:
     """Primary class for all NWB conversion classes."""
 
     data_interface_classes = None
 
     @classmethod
-    def get_source_schema(cls):
+    def get_source_schema(cls) -> dict:
         """Compile input schemas from each of the data interface classes."""
         source_schema = get_base_schema(
             root=True,
             id_="source.schema.json",
             title="Source data schema",
             description="Schema for the source data, files and directories",
             version="0.1.0",
         )
         for interface_name, data_interface in cls.data_interface_classes.items():
             source_schema["properties"].update({interface_name: unroot_schema(data_interface.get_source_schema())})
         return source_schema
 
-    def get_conversion_options_schema(self):
+    def get_conversion_options_schema(self) -> dict:
         """Compile conversion option schemas from each of the data interface classes."""
         conversion_options_schema = get_base_schema(
             root=True,
             id_="conversion_options.schema.json",
             title="Conversion options schema",
             description="Schema for the conversion options",
             version="0.1.0",
@@ -64,15 +64,15 @@
         self._validate_source_data(source_data=source_data, verbose=self.verbose)
         self.data_interface_objects = {
             name: data_interface(**source_data[name])
             for name, data_interface in self.data_interface_classes.items()
             if name in source_data
         }
 
-    def get_metadata_schema(self):
+    def get_metadata_schema(self) -> dict:
         """Compile metadata schemas from each of the data interface objects."""
         metadata_schema = load_dict_from_file(Path(__file__).parent / "schemas" / "base_metadata_schema.json")
         for data_interface in self.data_interface_objects.values():
             interface_schema = unroot_schema(data_interface.get_metadata_schema())
             metadata_schema = dict_deep_update(metadata_schema, interface_schema)
 
         default_values = self.get_metadata()
@@ -95,31 +95,38 @@
         decoded_metadata = json.loads(serialized_metadata)
         validate(instance=decoded_metadata, schema=self.get_metadata_schema())
         if self.verbose:
             print("Metadata is valid!")
 
     def validate_conversion_options(self, conversion_options: Dict[str, dict]):
         """Validate conversion_options against Converter conversion_options_schema."""
-        validate(instance=conversion_options, schema=self.get_conversion_options_schema())
+        validate(instance=conversion_options or {}, schema=self.get_conversion_options_schema())
         if self.verbose:
             print("conversion_options is valid!")
 
     def _validate_source_data(self, source_data: Dict[str, dict], verbose: bool = True):
         validate(instance=source_data, schema=self.get_source_schema())
         if verbose:
             print("Source data is valid!")
 
+    def add_to_nwbfile(self, nwbfile: NWBFile, metadata, conversion_options: Optional[dict] = None) -> None:
+        conversion_options = conversion_options or dict()
+        for interface_name, data_interface in self.data_interface_objects.items():
+            data_interface.add_to_nwbfile(
+                nwbfile=nwbfile, metadata=metadata, **conversion_options.get(interface_name, dict())
+            )
+
     def run_conversion(
         self,
         nwbfile_path: Optional[str] = None,
         nwbfile: Optional[NWBFile] = None,
         metadata: Optional[dict] = None,
         overwrite: bool = False,
         conversion_options: Optional[dict] = None,
-    ) -> NWBFile:
+    ) -> None:
         """
         Run the NWB conversion over all the instantiated data interfaces.
         Parameters
         ----------
         nwbfile_path : FilePathType
             Path for where to write or load (if overwrite=False) the NWBFile.
             If specified, the context will always write to this location.
@@ -129,62 +136,57 @@
             Metadata dictionary with information used to create the NWBFile when one does not exist or overwrite=True.
         overwrite : bool, default: False
             Whether to overwrite the NWBFile if one exists at the nwbfile_path.
             The default is False (append mode).
         conversion_options : dict, optional
             Similar to source_data, a dictionary containing keywords for each interface for which non-default
             conversion specification is requested.
-        Returns
-        -------
-        nwbfile: NWBFile
-            The in-memory NWBFile object after all conversion operations are complete.
         """
         if metadata is None:
             metadata = self.get_metadata()
-        self.validate_metadata(metadata=metadata)
 
-        if conversion_options is None:
-            conversion_options = dict()
+        self.validate_metadata(metadata=metadata)
 
         self.validate_conversion_options(conversion_options=conversion_options)
 
+        self.temporally_align_data_interfaces()
+
         with make_or_load_nwbfile(
             nwbfile_path=nwbfile_path,
             nwbfile=nwbfile,
             metadata=metadata,
             overwrite=overwrite,
             verbose=self.verbose,
         ) as nwbfile_out:
-            for interface_name, data_interface in self.data_interface_objects.items():
-                data_interface.run_conversion(
-                    nwbfile=nwbfile_out, metadata=metadata, **conversion_options.get(interface_name, dict())
-                )
+            self.add_to_nwbfile(nwbfile_out, metadata, conversion_options)
 
-        return nwbfile_out
+    def temporally_align_data_interfaces(self):
+        """Override this method to implement custom alignment"""
+        pass
 
 
 class ConverterPipe(NWBConverter):
     """Takes a list or dict of pre-initialized interfaces as arguments to build an NWBConverter class"""
 
-    def get_conversion_options_schema(self):
+    def get_conversion_options_schema(self) -> dict:
         """Compile conversion option schemas from each of the data interface classes."""
         conversion_options_schema = get_base_schema(
             root=True,
             id_="conversion_options.schema.json",
             title="Conversion options schema",
             description="Schema for the conversion options",
             version="0.1.0",
         )
         for interface_name, data_interface in self.data_interface_objects.items():
             conversion_options_schema["properties"].update(
                 {interface_name: unroot_schema(data_interface.get_conversion_options_schema())}
             )
         return conversion_options_schema
 
-    def get_source_schema(self):
+    def get_source_schema(self) -> dict:
         raise NotImplementedError("Source data not available with previously initialized classes")
 
     def validate_source(self):
         raise NotImplementedError("Source data not available with previously initialized classes")
 
     def __init__(self, data_interfaces: Union[List[BaseDataInterface], Dict[str, BaseDataInterface]], verbose=True):
         self.verbose = verbose
```

### Comparing `neuroconv-0.3.0/src/neuroconv/schemas/base_metadata_schema.json` & `neuroconv-0.4.0/src/neuroconv/schemas/base_metadata_schema.json`

 * *Files 1% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9999348958333334%*

 * *Differences: {"'properties'": "{'Subject': {'properties': {'description': {delete: ['default']}, 'sex': "*

 * *                 "{delete: ['default']}}}}"}*

```diff
@@ -123,24 +123,22 @@
                 },
                 "date_of_birth": {
                     "description": "Date of birth of subject. Can be supplied instead of 'age'.",
                     "format": "date-time",
                     "type": "string"
                 },
                 "description": {
-                    "default": "no description",
                     "description": "Description of subject and where subject came from (e.g., breeder, if animal).",
                     "type": "string"
                 },
                 "genotype": {
                     "description": "Genetic strain. If absent, assume Wild Type (WT)",
                     "type": "string"
                 },
                 "sex": {
-                    "default": "U",
                     "enum": [
                         "M",
                         "F",
                         "U",
                         "O"
                     ],
                     "type": "string"
```

### Comparing `neuroconv-0.3.0/src/neuroconv/schemas/metadata_schema.json` & `neuroconv-0.4.0/src/neuroconv/schemas/metadata_schema.json`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/schemas/source_schema.json` & `neuroconv-0.4.0/src/neuroconv/schemas/source_schema.json`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/schemas/time_series_schema.json` & `neuroconv-0.4.0/src/neuroconv/schemas/time_series_schema.json`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/schemas/yaml_conversion_specification_schema.json` & `neuroconv-0.4.0/src/neuroconv/schemas/yaml_conversion_specification_schema.json`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/audio/audio.py` & `neuroconv-0.4.0/src/neuroconv/tools/audio/audio.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/data_transfers.py` & `neuroconv-0.4.0/src/neuroconv/tools/data_transfers.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/figshare.py` & `neuroconv-0.4.0/src/neuroconv/tools/figshare.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/hdmf.py` & `neuroconv-0.4.0/src/neuroconv/tools/hdmf.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/importing.py` & `neuroconv-0.4.0/src/neuroconv/tools/importing.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/neo/neo.py` & `neuroconv-0.4.0/src/neuroconv/tools/neo/neo.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 import distutils.version
 import uuid
 import warnings
-from datetime import datetime
 from pathlib import Path
 from typing import Optional, Tuple
 
 import neo.io.baseio
 import numpy as np
 import pynwb
 from hdmf.backends.hdf5 import H5DataIO
@@ -362,17 +361,17 @@
     # nwbfile.add_icephys_experimental_condition(
     #     repetitions=[
     #         run_index,
     #     ]
     # )
 
 
-def add_all_to_nwbfile(
+def add_neo_to_nwb(
     neo_reader,
-    nwbfile: pynwb.NWBFile = None,
+    nwbfile: pynwb.NWBFile,
     metadata: dict = None,
     compression: Optional[str] = "gzip",
     icephys_experiment_type: str = "voltage_clamp",
     stimulus_type: Optional[str] = None,
     skip_electrodes: Tuple[int] = (),
 ):
     """
@@ -395,16 +394,15 @@
     icephys_experiment_type: str (optional)
         Type of Icephys experiment. Allowed types are: 'voltage_clamp', 'current_clamp' and 'izero'.
         If no value is passed, 'voltage_clamp' is used as default.
     stimulus_type: str, optional
     skip_electrodes: tuple, optional
         Electrode IDs to skip. Defaults to ().
     """
-    if nwbfile is not None:
-        assert isinstance(nwbfile, pynwb.NWBFile), "'nwbfile' should be of type pynwb.NWBFile"
+    assert isinstance(nwbfile, pynwb.NWBFile), "'nwbfile' should be of type pynwb.NWBFile"
 
     add_device_from_metadata(nwbfile=nwbfile, modality="Icephys", metadata=metadata)
 
     add_icephys_electrode(
         neo_reader=neo_reader,
         nwbfile=nwbfile,
         metadata=metadata,
@@ -524,11 +522,11 @@
                     session_description="Auto-generated by NwbRecordingExtractor without description.",
                     identifier=str(uuid.uuid4()),
                 )
                 if metadata is not None and "NWBFile" in metadata:
                     nwbfile_kwargs.update(metadata["NWBFile"])
                 nwbfile = pynwb.NWBFile(**nwbfile_kwargs)
 
-            add_all_to_nwbfile(nwbfile=nwbfile, **kwargs)
+            add_neo_to_nwb(nwbfile=nwbfile, **kwargs)
             io.write(nwbfile)
     else:
-        add_all_to_nwbfile(nwbfile=nwbfile, **kwargs)
+        add_neo_to_nwb(nwbfile=nwbfile, **kwargs)
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/nwb_helpers.py` & `neuroconv-0.4.0/src/neuroconv/tools/nwb_helpers.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,19 +1,22 @@
+import json
 import uuid
 from contextlib import contextmanager
 from datetime import datetime
 from pathlib import Path
 from typing import Optional
 from warnings import warn
 
+import jsonschema
 from pynwb import NWBHDF5IO, NWBFile
 from pynwb.file import Subject
 
 from ..utils import FilePathType, dict_deep_update
-from ..utils.dict import DeepDict
+from ..utils.dict import DeepDict, load_dict_from_file
+from ..utils.json_schema import validate_metadata
 
 
 def get_module(nwbfile: NWBFile, name: str, description: str = None):
     """Check if processing module exists. If not, create it. Then return module."""
     if name in nwbfile.processing:
         if description is not None and nwbfile.processing[name].description != description:
             warn(
@@ -41,30 +44,39 @@
         session_description="no description",
         identifier=str(uuid.uuid4()),
     )
 
     return metadata
 
 
-def make_nwbfile_from_metadata(metadata: dict):
+def make_nwbfile_from_metadata(metadata: dict) -> NWBFile:
     """Make NWBFile from available metadata."""
-    metadata = dict_deep_update(get_default_nwbfile_metadata(), metadata)
+
+    # Validate metadata
+    schema_path = Path(__file__).resolve().parent.parent / "schemas/base_metadata_schema.json"
+    base_metadata_schema = load_dict_from_file(file_path=schema_path)
+    validate_metadata(metadata=metadata, schema=base_metadata_schema)
+
     nwbfile_kwargs = metadata["NWBFile"]
+    # convert ISO 8601 string to datetime
+    if isinstance(nwbfile_kwargs.get("session_start_time"), str):
+        nwbfile_kwargs["session_start_time"] = datetime.fromisoformat(nwbfile_kwargs["session_start_time"])
+    if "session_description" not in nwbfile_kwargs:
+        nwbfile_kwargs["session_description"] = "No description."
+    if "identifier" not in nwbfile_kwargs:
+        nwbfile_kwargs["identifier"] = str(uuid.uuid4())
     if "Subject" in metadata:
+        nwbfile_kwargs["subject"] = metadata["Subject"]
         # convert ISO 8601 string to datetime
-        if "date_of_birth" in metadata["Subject"] and isinstance(metadata["Subject"]["date_of_birth"], str):
-            metadata["Subject"]["date_of_birth"] = datetime.fromisoformat(metadata["Subject"]["date_of_birth"])
-        nwbfile_kwargs.update(subject=Subject(**metadata["Subject"]))
-    # convert ISO 8601 string to datetime
-    assert "session_start_time" in nwbfile_kwargs, (
-        "'session_start_time' was not found in metadata['NWBFile']! Please add the correct start time of the "
-        "session in ISO8601 format (%Y-%m-%dT%H:%M:%S) to this key of the metadata."
-    )
-    if isinstance(nwbfile_kwargs.get("session_start_time", None), str):
-        nwbfile_kwargs["session_start_time"] = datetime.fromisoformat(metadata["NWBFile"]["session_start_time"])
+        if "date_of_birth" in nwbfile_kwargs["subject"] and isinstance(nwbfile_kwargs["subject"]["date_of_birth"], str):
+            nwbfile_kwargs["subject"]["date_of_birth"] = datetime.fromisoformat(
+                nwbfile_kwargs["subject"]["date_of_birth"]
+            )
+        nwbfile_kwargs["subject"] = Subject(**nwbfile_kwargs["subject"])
+
     return NWBFile(**nwbfile_kwargs)
 
 
 def add_device_from_metadata(nwbfile: NWBFile, modality: str = "Ecephys", metadata: dict = None):
     """
     Add device information from metadata to NWBFile object.
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/path_expansion.py` & `neuroconv-0.4.0/src/neuroconv/tools/path_expansion.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """Helpful classes for expanding file or folder paths on a system given a f-string rule for matching patterns."""
 import abc
 import os
 from pathlib import Path
-from typing import Dict, Iterable, List, Optional
+from typing import Dict, Iterable, List
 
 from fparse import parse
 from pydantic import DirectoryPath, FilePath
 
 from ..utils import DeepDict
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/processes.py` & `neuroconv-0.4.0/src/neuroconv/tools/processes.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/roiextractors/imagingextractordatachunkiterator.py` & `neuroconv-0.4.0/src/neuroconv/tools/roiextractors/imagingextractordatachunkiterator.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/roiextractors/roiextractors.py` & `neuroconv-0.4.0/src/neuroconv/tools/roiextractors/roiextractors.py`

 * *Files 2% similar despite different names*

```diff
@@ -474,22 +474,41 @@
         if "buffer_size" not in iterator_options:
             iterator_options.update(buffer_size=10)
         return DataChunkIterator(data=data_generator(imaging), **iterator_options)
 
     return ImagingExtractorDataChunkIterator(imaging_extractor=imaging, **iterator_options)
 
 
+def add_imaging(
+    imaging: ImagingExtractor,
+    nwbfile: NWBFile,
+    metadata: Optional[dict] = None,
+    photon_series_type: Literal["TwoPhotonSeries", "OnePhotonSeries"] = "TwoPhotonSeries",
+    iterator_type: Optional[str] = "v2",
+    iterator_options: Optional[dict] = None,
+):
+    add_devices(nwbfile=nwbfile, metadata=metadata)
+    add_photon_series(
+        imaging=imaging,
+        nwbfile=nwbfile,
+        metadata=metadata,
+        photon_series_type=photon_series_type,
+        iterator_type=iterator_type,
+        iterator_options=iterator_options,
+    )
+
+
 def write_imaging(
     imaging: ImagingExtractor,
     nwbfile_path: OptionalFilePathType = None,
     nwbfile: Optional[NWBFile] = None,
     metadata: Optional[dict] = None,
     overwrite: bool = False,
     verbose: bool = True,
-    iterator_type: Optional[str] = "v2",
+    iterator_type: str = "v2",
     iterator_options: Optional[dict] = None,
     photon_series_type: Literal["TwoPhotonSeries", "OnePhotonSeries"] = "TwoPhotonSeries",
     buffer_size: Optional[int] = None,  # TODO: to be removed
 ):
     """
     Primary method for writing an ImagingExtractor object to an NWBFile.
 
@@ -511,16 +530,14 @@
         Metadata dictionary with information used to create the NWBFile when one does not exist or overwrite=True.
     overwrite: bool, optional
         Whether to overwrite the NWBFile if one exists at the nwbfile_path.
         The default is False (append mode).
     verbose: bool, optional
         If 'nwbfile_path' is specified, informs user after a successful write operation.
         The default is True.
-    num_chunks: int
-        Number of chunks for writing data to file
     iterator_type: {"v2", "v1",  None}, default: 'v2'
         The type of DataChunkIterator to use.
         'v1' is the original DataChunkIterator of the hdmf data_utils.
         'v2' is the locally developed SpikeInterfaceRecordingDataChunkIterator, which offers full control over chunking.
         None: write the TimeSeries with no memory chunking.
     iterator_options : dict, optional
         Dictionary of options for the iterator.
@@ -546,18 +563,17 @@
         metadata = dict()
     if hasattr(imaging, "nwb_metadata"):
         metadata = dict_deep_update(imaging.nwb_metadata, metadata, append_list=False)
 
     with make_or_load_nwbfile(
         nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata, overwrite=overwrite, verbose=verbose
     ) as nwbfile_out:
-        add_devices(nwbfile=nwbfile_out, metadata=metadata)
-        add_photon_series(
+        add_imaging(
             imaging=imaging,
-            nwbfile=nwbfile_out,
+            nwbfile=nwbfile,
             metadata=metadata,
             photon_series_type=photon_series_type,
             iterator_type=iterator_type,
             iterator_options=iterator_options,
         )
     return nwbfile_out
 
@@ -966,36 +982,84 @@
     for img_name, img in images_to_add.items():
         # Note that nwb uses the conversion width x height (columns, rows) and roiextractors uses the transpose
         image_collection.add_image(GrayscaleImage(name=img_name, data=img.T))
 
     return nwbfile
 
 
+def add_segmentation(
+    segmentation_extractor: SegmentationExtractor,
+    nwbfile: NWBFile,
+    metadata: Optional[dict] = None,
+    plane_num: int = 0,
+    include_roi_centroids: bool = True,
+    include_roi_acceptance: bool = True,
+    mask_type: Optional[str] = "image",  # Literal["image", "pixel"]
+    iterator_options: Optional[dict] = None,
+    compression_options: Optional[dict] = None,
+):
+    # Add device:
+    add_devices(nwbfile=nwbfile, metadata=metadata)
+
+    # ImageSegmentation:
+    # image_segmentation_name = (
+    #     "ImageSegmentation" if plane_no_loop == 0 else f"ImageSegmentation_Plane{plane_no_loop}"
+    # )
+    # add_image_segmentation(nwbfile=nwbfile_out, metadata=metadata)
+    # image_segmentation = ophys.data_interfaces.get(image_segmentation_name)
+
+    # Add imaging plane
+    add_imaging_plane(nwbfile=nwbfile, metadata=metadata)
+
+    # PlaneSegmentation:
+    add_plane_segmentation(
+        segmentation_extractor=segmentation_extractor,
+        nwbfile=nwbfile,
+        metadata=metadata,
+        include_roi_centroids=include_roi_centroids,
+        include_roi_acceptance=include_roi_acceptance,
+        mask_type=mask_type,
+        iterator_options=iterator_options,
+        compression_options=compression_options,
+    )
+
+    # Add fluorescence traces:
+    add_fluorescence_traces(
+        segmentation_extractor=segmentation_extractor,
+        nwbfile=nwbfile,
+        metadata=metadata,
+        iterator_options=iterator_options,
+        compression_options=compression_options,
+    )
+
+    # Adding summary images (mean and correlation)
+    images_set_name = "SegmentationImages" if plane_num == 0 else f"SegmentationImages_Plane{plane_num}"
+    add_summary_images(nwbfile=nwbfile, segmentation_extractor=segmentation_extractor, images_set_name=images_set_name)
+
+
 def write_segmentation(
     segmentation_extractor: SegmentationExtractor,
     nwbfile_path: OptionalFilePathType = None,
     nwbfile: Optional[NWBFile] = None,
     metadata: Optional[dict] = None,
     overwrite: bool = False,
     verbose: bool = True,
-    buffer_size: int = 10,
-    plane_num: int = 0,
     include_roi_centroids: bool = True,
     include_roi_acceptance: bool = True,
-    mask_type: Optional[str] = "image",  # Optional[Literal["image", "pixel"]]
+    mask_type: Optional[str] = "image",  # Literal["image", "pixel"]
     iterator_options: Optional[dict] = None,
     compression_options: Optional[dict] = None,
 ) -> NWBFile:
     """
     Primary method for writing an SegmentationExtractor object to an NWBFile.
 
     Parameters
     ----------
     segmentation_extractor: SegmentationExtractor
-        The segentation extractor object to be written to nwb
+        The segmentation extractor object to be written to nwb
     nwbfile_path: FilePathType
         Path for where to write or load (if overwrite=False) the NWBFile.
         If specified, the context will always write to this location.
     nwbfile: NWBFile, optional
         If passed, this function will fill the relevant fields within the NWBFile object.
         E.g., calling
             write_recording(recording=my_recording_extractor, nwbfile=my_nwbfile)
@@ -1070,48 +1134,20 @@
     with make_or_load_nwbfile(
         nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata_base_common, overwrite=overwrite, verbose=verbose
     ) as nwbfile_out:
         _ = get_module(nwbfile=nwbfile_out, name="ophys", description="contains optical physiology processed data")
         for plane_no_loop, (segmentation_extractor, metadata) in enumerate(
             zip(segmentation_extractors, metadata_base_list)
         ):
-            # Add device:
-            add_devices(nwbfile=nwbfile_out, metadata=metadata)
-
-            # ImageSegmentation:
-            # image_segmentation_name = (
-            #     "ImageSegmentation" if plane_no_loop == 0 else f"ImageSegmentation_Plane{plane_no_loop}"
-            # )
-            # add_image_segmentation(nwbfile=nwbfile_out, metadata=metadata)
-            # image_segmentation = ophys.data_interfaces.get(image_segmentation_name)
-
-            # Add imaging plane
-            add_imaging_plane(nwbfile=nwbfile_out, metadata=metadata)
-
-            # PlaneSegmentation:
-            add_plane_segmentation(
+            add_segmentation(
                 segmentation_extractor=segmentation_extractor,
                 nwbfile=nwbfile_out,
                 metadata=metadata,
+                plane_num=plane_no_loop,
                 include_roi_centroids=include_roi_centroids,
                 include_roi_acceptance=include_roi_acceptance,
                 mask_type=mask_type,
                 iterator_options=iterator_options,
                 compression_options=compression_options,
             )
 
-            # Add fluorescence traces:
-            add_fluorescence_traces(
-                segmentation_extractor=segmentation_extractor,
-                nwbfile=nwbfile_out,
-                metadata=metadata,
-                iterator_options=iterator_options,
-                compression_options=compression_options,
-            )
-
-            # Adding summary images (mean and correlation)
-            images_set_name = "SegmentationImages" if plane_no_loop == 0 else f"SegmentationImages_Plane{plane_no_loop}"
-            add_summary_images(
-                nwbfile=nwbfile_out, segmentation_extractor=segmentation_extractor, images_set_name=images_set_name
-            )
-
     return nwbfile_out
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/signal_processing.py` & `neuroconv-0.4.0/src/neuroconv/tools/signal_processing.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,11 @@
 from typing import Optional
 
 import numpy as np
 
-from ..utils import ArrayType
-
 
 def get_rising_frames_from_ttl(trace: np.ndarray, threshold: Optional[float] = None) -> np.ndarray:
     """
     Return the frame indices for rising events in a TTL pulse.
 
     Parameters
     ----------
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/spikeinterface/spikeinterface.py` & `neuroconv-0.4.0/src/neuroconv/tools/spikeinterface/spikeinterface.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,26 +4,30 @@
 from numbers import Real
 from typing import List, Literal, Optional, Union
 
 import numpy as np
 import psutil
 import pynwb
 from hdmf.backends.hdf5.h5_utils import H5DataIO
-from hdmf.common.table import DynamicTable
 from hdmf.data_utils import AbstractDataChunkIterator, DataChunkIterator
 from nwbinspector.utils import get_package_version
 from packaging.version import Version
 from pynwb import NWBFile
 from spikeinterface import BaseRecording, BaseSorting, WaveformExtractor
 
 from .spikeinterfacerecordingdatachunkiterator import (
     SpikeInterfaceRecordingDataChunkIterator,
 )
 from ..nwb_helpers import get_module, make_or_load_nwbfile
-from ...utils import FilePathType, calculate_regular_series_rate, dict_deep_update
+from ...utils import (
+    DeepDict,
+    FilePathType,
+    calculate_regular_series_rate,
+    dict_deep_update,
+)
 
 
 def get_nwb_metadata(recording: BaseRecording, metadata: dict = None):
     """
     Return default metadata for all recording fields.
 
     Parameters
@@ -44,26 +48,26 @@
                 for group_name in np.unique(recording.get_channel_groups())
             ],
         ),
     )
     return metadata
 
 
-def add_devices(nwbfile: pynwb.NWBFile, metadata: dict = None):
+def add_devices(nwbfile: pynwb.NWBFile, metadata: Optional[DeepDict] = None):
     """
     Add device information to nwbfile object.
 
     Will always ensure nwbfile has at least one device, but multiple
     devices within the metadata list will also be created.
 
     Parameters
     ----------
     nwbfile: NWBFile
         nwb file to which the recording information is to be added
-    metadata: dict
+    metadata: DeepDict
         metadata info for constructing the nwb file (optional).
         Should be of the format
             metadata['Ecephys']['Device'] = [
                 {
                     'name': my_name,
                     'description': my_description
                 },
@@ -648,26 +652,34 @@
         iterator_type=iterator_type,
         iterator_opts=iterator_opts,
     )
     eseries_kwargs.update(
         data=H5DataIO(data=ephys_data_iterator, compression=compression, compression_opts=compression_opts)
     )
 
-    # Timestamps vs rate
-    timestamps = recording.get_times(segment_index=segment_index)
-    rate = calculate_regular_series_rate(series=timestamps)  # Returns None if it is not regular
-    starting_time = starting_time if starting_time is not None else 0
+    # Now we decide whether to store the timestamps as a regular series or as an irregular series.
+    if recording.has_time_vector(segment_index=segment_index):
+        # First we check if the recording has a a time vector to avoid creating artificial timestamps
+        timestamps = recording.get_times(segment_index=segment_index)
+        rate = calculate_regular_series_rate(series=timestamps)  # Returns None if it is not regular
+        recording_t_start = timestamps[0]
+    else:
+        rate = recording.get_sampling_frequency()
+        recording_t_start = recording._recording_segments[segment_index].t_start or 0
 
+    starting_time = starting_time if starting_time is not None else 0
     if rate:
-        starting_time = starting_time + timestamps[0]
+        starting_time = float(starting_time + recording_t_start)
+        # Note that we call the sampling frequency again because the estimated rate might be different from the
+        # sampling frequency of the recording extractor by some epsilon.
         eseries_kwargs.update(starting_time=starting_time, rate=recording.get_sampling_frequency())
     else:
-        shifted_time_stamps = starting_time + timestamps
+        shifted_timestamps = starting_time + timestamps
         wrapped_timestamps = H5DataIO(
-            data=shifted_time_stamps, compression=compression, compression_opts=compression_opts
+            data=shifted_timestamps, compression=compression, compression_opts=compression_opts
         )
         eseries_kwargs.update(timestamps=wrapped_timestamps)
 
     # Create ElectricalSeries object and add it to nwbfile
     es = pynwb.ecephys.ElectricalSeries(**eseries_kwargs)
     if write_as == "raw":
         nwbfile.add_acquisition(es)
@@ -709,27 +721,72 @@
         possibly including the default, will occur.
     """
     add_devices(nwbfile=nwbfile, metadata=metadata)
     add_electrode_groups(recording=recording, nwbfile=nwbfile, metadata=metadata)
     add_electrodes(recording=recording, nwbfile=nwbfile, metadata=metadata)
 
 
+def add_recording(
+    recording: BaseRecording,
+    nwbfile: pynwb.NWBFile,
+    metadata: Optional[dict] = None,
+    starting_time: Optional[float] = None,
+    write_as: Literal["raw", "processed", "lfp"] = "raw",
+    es_key: Optional[str] = None,
+    write_electrical_series: bool = True,
+    write_scaled: bool = False,
+    compression: Optional[str] = "gzip",
+    compression_opts: Optional[int] = None,
+    iterator_type: str = "v2",
+    iterator_opts: Optional[dict] = None,
+):
+    assert get_package_version("pynwb") >= Version(
+        "1.3.3"
+    ), "'write_recording' not supported for version < 1.3.3. Run pip install --upgrade pynwb"
+
+    if hasattr(recording, "nwb_metadata"):
+        metadata = dict_deep_update(recording.nwb_metadata, metadata)
+    elif metadata is None:
+        metadata = get_nwb_metadata(recording=recording)
+
+    # Convenience function to add device, electrode groups and electrodes info
+    add_electrodes_info(recording=recording, nwbfile=nwbfile, metadata=metadata)
+
+    if write_electrical_series:
+        number_of_segments = recording.get_num_segments()
+        for segment_index in range(number_of_segments):
+            add_electrical_series(
+                recording=recording,
+                nwbfile=nwbfile,
+                segment_index=segment_index,
+                starting_time=starting_time,
+                metadata=metadata,
+                write_as=write_as,
+                es_key=es_key,
+                write_scaled=write_scaled,
+                compression=compression,
+                compression_opts=compression_opts,
+                iterator_type=iterator_type,
+                iterator_opts=iterator_opts,
+            )
+
+
 def write_recording(
     recording: BaseRecording,
     nwbfile_path: Optional[FilePathType] = None,
     nwbfile: Optional[pynwb.NWBFile] = None,
     metadata: Optional[dict] = None,
     overwrite: bool = False,
     verbose: bool = True,
     starting_time: Optional[float] = None,
-    write_as: Optional[str] = None,
+    write_as: Optional[str] = "raw",
     es_key: Optional[str] = None,
     write_electrical_series: bool = True,
     write_scaled: bool = False,
-    compression: Optional[str] = None,
+    compression: Optional[str] = "gzip",
     compression_opts: Optional[int] = None,
     iterator_type: str = "v2",
     iterator_opts: Optional[dict] = None,
 ) -> pynwb.NWBFile:
     """
     Primary method for writing a RecordingExtractor object to an NWBFile.
 
@@ -824,50 +881,32 @@
                 Cannot be set if `chunk_mb` is also specified.
             display_progress : bool, default: False
                 Display a progress bar with iteration rate and estimated completion time.
             progress_bar_options : dict, optional
                 Dictionary of keyword arguments to be passed directly to tqdm.
                 See https://github.com/tqdm/tqdm#parameters for options.
     """
-    if nwbfile is not None:
-        assert isinstance(nwbfile, pynwb.NWBFile), "'nwbfile' should be of type pynwb.NWBFile"
-    assert get_package_version("pynwb") >= Version(
-        "1.3.3"
-    ), "'write_recording' not supported for version < 1.3.3. Run pip install --upgrade pynwb"
-    write_as = "raw" if write_as is None else write_as
-    compression = "gzip" if compression is None else compression
-
-    if hasattr(recording, "nwb_metadata"):
-        metadata = dict_deep_update(recording.nwb_metadata, metadata)
-    elif metadata is None:
-        metadata = get_nwb_metadata(recording=recording)
 
     with make_or_load_nwbfile(
         nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata, overwrite=overwrite, verbose=verbose
     ) as nwbfile_out:
-        # Convenience function to add device, electrode groups and electrodes info
-        add_electrodes_info(recording=recording, nwbfile=nwbfile_out, metadata=metadata)
-
-        if write_electrical_series:
-            number_of_segments = recording.get_num_segments()
-            for segment_index in range(number_of_segments):
-                add_electrical_series(
-                    recording=recording,
-                    nwbfile=nwbfile_out,
-                    segment_index=segment_index,
-                    starting_time=starting_time,
-                    metadata=metadata,
-                    write_as=write_as,
-                    es_key=es_key,
-                    write_scaled=write_scaled,
-                    compression=compression,
-                    compression_opts=compression_opts,
-                    iterator_type=iterator_type,
-                    iterator_opts=iterator_opts,
-                )
+        add_recording(
+            recording=recording,
+            nwbfile=nwbfile,
+            starting_time=starting_time,
+            metadata=metadata,
+            write_as=write_as,
+            es_key=es_key,
+            write_electrical_series=write_electrical_series,
+            write_scaled=write_scaled,
+            compression=compression,
+            compression_opts=compression_opts,
+            iterator_type=iterator_type,
+            iterator_opts=iterator_opts,
+        )
     return nwbfile_out
 
 
 def get_nspikes(units_table: pynwb.misc.Units, unit_id: int) -> int:
     """Return the number of spikes for chosen unit."""
     ids = np.array(units_table.id[:])
     indexes = np.where(ids == unit_id)[0]
@@ -929,14 +968,17 @@
     waveform_means : np.ndarray, optional
         Waveform mean (template) for each unit (num_units, num_samples, num_channels)
     waveform_sds : np.ndarray, optional
         Waveform standard deviation for each unit (num_units, num_samples, num_channels)
     unit_electrode_indices : list of lists or arrays, optional
         For each unit, the indices of electrodes that each waveform_mean/sd correspond to.
     """
+    if not write_in_processing_module and units_table_name != "units":
+        raise ValueError("When writing to the nwbfile.units table, the name of the table must be 'units'!")
+
     if not isinstance(nwbfile, pynwb.NWBFile):
         raise TypeError(f"nwbfile type should be an instance of pynwb.NWBFile but got {type(nwbfile)}")
 
     if write_in_processing_module:
         ecephys_mod = get_module(
             nwbfile=nwbfile,
             name="ecephys",
@@ -1103,29 +1145,60 @@
         # Always store numpy objects as strings
         if np.issubdtype(extended_data.dtype, np.object_):
             extended_data = extended_data.astype("str", copy=False)
         cols_args["data"] = extended_data
         units_table.add_column(property, **cols_args)
 
 
+def add_sorting(
+    sorting: BaseSorting,
+    nwbfile: Optional[pynwb.NWBFile] = None,
+    unit_ids: Optional[List[Union[str, int]]] = None,
+    property_descriptions: Optional[dict] = None,
+    skip_properties: Optional[List[str]] = None,
+    skip_features: Optional[List[str]] = None,
+    write_as: Literal["units", "processing"] = "units",
+    units_name: str = "units",
+    units_description: str = "Autogenerated by neuroconv.",
+):
+    assert write_as in [
+        "units",
+        "processing",
+    ], f"Argument write_as ({write_as}) should be one of 'units' or 'processing'!"
+    write_in_processing_module = False if write_as == "units" else True
+
+    add_units_table(
+        sorting=sorting,
+        unit_ids=unit_ids,
+        nwbfile=nwbfile,
+        property_descriptions=property_descriptions,
+        skip_properties=skip_properties,
+        skip_features=skip_features,
+        write_in_processing_module=write_in_processing_module,
+        units_table_name=units_name,
+        unit_table_description=units_description,
+        write_waveforms=False,
+    )
+
+
 def write_sorting(
     sorting: BaseSorting,
     nwbfile_path: Optional[FilePathType] = None,
     nwbfile: Optional[pynwb.NWBFile] = None,
     metadata: Optional[dict] = None,
     overwrite: bool = False,
     verbose: bool = True,
     unit_ids: Optional[List[Union[str, int]]] = None,
     property_descriptions: Optional[dict] = None,
     skip_properties: Optional[List[str]] = None,
     skip_features: Optional[List[str]] = None,
     write_as: Literal["units", "processing"] = "units",
     units_name: str = "units",
     units_description: str = "Autogenerated by neuroconv.",
-) -> NWBFile:
+):
     """
     Primary method for writing a SortingExtractor object to an NWBFile.
 
     Parameters
     ----------
     sorting : spikeinterface.BaseSorting
     nwbfile_path : FilePathType, optional
@@ -1160,44 +1233,29 @@
         How to save the units table in the nwb file. Options:
         - 'units' will save it to the official NWBFile.Units position; recommended only for the final form of the data.
         - 'processing' will save it to the processing module to serve as a historical provenance for the official table.
     units_name : str, default: 'units'
         The name of the units table. If write_as=='units', then units_name must also be 'units'.
     units_description : str, default: 'Autogenerated by neuroconv.'
     """
-    assert (
-        nwbfile_path is None or nwbfile is None
-    ), "Either pass a nwbfile_path location, or nwbfile object, but not both!"
-    if nwbfile is not None:
-        assert isinstance(nwbfile, pynwb.NWBFile), "'nwbfile' should be a pynwb.NWBFile object!"
-
-    assert write_as in [
-        "units",
-        "processing",
-    ], f"Argument write_as ({write_as}) should be one of 'units' or 'processing'!"
-    if write_as == "units":
-        assert units_name == "units", "When writing to the nwbfile.units table, the name of the table must be 'units'!"
-    write_in_processing_module = False if write_as == "units" else True
 
     with make_or_load_nwbfile(
         nwbfile_path=nwbfile_path, nwbfile=nwbfile, metadata=metadata, overwrite=overwrite, verbose=verbose
     ) as nwbfile_out:
-        add_units_table(
+        add_sorting(
             sorting=sorting,
-            unit_ids=unit_ids,
             nwbfile=nwbfile_out,
+            unit_ids=unit_ids,
             property_descriptions=property_descriptions,
             skip_properties=skip_properties,
             skip_features=skip_features,
-            write_in_processing_module=write_in_processing_module,
-            units_table_name=units_name,
-            unit_table_description=units_description,
-            write_waveforms=False,
+            write_as=write_as,
+            units_name=units_name,
+            units_description=units_description,
         )
-    return nwbfile_out
 
 
 def add_waveforms(
     waveform_extractor: WaveformExtractor,
     nwbfile: Optional[pynwb.NWBFile] = None,
     metadata: Optional[dict] = None,
     recording: Optional[BaseRecording] = None,
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/spikeinterface/spikeinterfacerecordingdatachunkiterator.py` & `neuroconv-0.4.0/src/neuroconv/tools/spikeinterface/spikeinterfacerecordingdatachunkiterator.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,8 @@
-from typing import Iterable, Optional, Tuple, Union
-from warnings import warn
+from typing import Iterable, Optional, Tuple
 
 from hdmf.data_utils import GenericDataChunkIterator
 from spikeinterface import BaseRecording
 
 
 class SpikeInterfaceRecordingDataChunkIterator(GenericDataChunkIterator):
     """DataChunkIterator specifically for use on RecordingExtractor objects."""
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/testing/_path_expander_demo_ibl_filepaths.txt` & `neuroconv-0.4.0/src/neuroconv/tools/testing/_path_expander_demo_ibl_filepaths.txt`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/testing/data_interface_mixins.py` & `neuroconv-0.4.0/src/neuroconv/tools/testing/data_interface_mixins.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 from datetime import datetime
 from pathlib import Path
 from typing import List, Optional, Type, Union
 
 import numpy as np
 from hdmf.testing import TestCase as HDMFTestCase
 from jsonschema.validators import Draft7Validator, validate
+from ndx_miniscope import Miniscope
 from numpy.testing import assert_array_equal
 from pynwb import NWBHDF5IO
 from roiextractors import NwbImagingExtractor, NwbSegmentationExtractor
 from roiextractors.testing import check_imaging_equal, check_segmentations_equal
 from spikeinterface.core.testing import check_recordings_equal, check_sortings_equal
 from spikeinterface.extractors import NwbRecordingExtractor, NwbSortingExtractor
 
@@ -108,15 +109,15 @@
             with self.subTest(str(num)):
                 self.case = num
                 self.test_kwargs = kwargs
                 self.interface = self.data_interface_cls(**self.test_kwargs)
                 self.check_metadata_schema_valid()
                 self.check_conversion_options_schema_valid()
                 self.check_metadata()
-                self.nwbfile_path = str(self.save_directory / f"{self.data_interface_cls.__name__}_{num}.nwb")
+                self.nwbfile_path = str(self.save_directory / f"{self.__class__.__name__}_{num}.nwb")
                 self.run_conversion(nwbfile_path=self.nwbfile_path)
                 self.check_read_nwb(nwbfile_path=self.nwbfile_path)
 
                 # Any extra custom checks to run
                 self.run_custom_checks()
 
 
@@ -272,30 +273,32 @@
     def check_read_nwb(self, nwbfile_path: str):
         recording = self.interface.recording_extractor
 
         electrical_series_name = self.interface.get_metadata()["Ecephys"][self.interface.es_key]["name"]
 
         if recording.get_num_segments() == 1:
             # Spikeinterface behavior is to load the electrode table channel_name property as a channel_id
-            nwb_recording = NwbRecordingExtractor(file_path=nwbfile_path, electrical_series_name=electrical_series_name)
+            self.nwb_recording = NwbRecordingExtractor(
+                file_path=nwbfile_path, electrical_series_name=electrical_series_name
+            )
             if "channel_name" in recording.get_property_keys():
                 renamed_channel_ids = recording.get_property("channel_name")
             else:
                 renamed_channel_ids = recording.get_channel_ids().astype("str")
             recording = recording.channel_slice(
                 channel_ids=recording.get_channel_ids(), renamed_channel_ids=renamed_channel_ids
             )
 
             # Edge case that only occurs in testing, but should eventually be fixed nonetheless
             # The NwbRecordingExtractor on spikeinterface experiences an issue when duplicated channel_ids
             # are specified, which occurs during check_recordings_equal when there is only one channel
-            if nwb_recording.get_channel_ids()[0] != nwb_recording.get_channel_ids()[-1]:
-                check_recordings_equal(RX1=recording, RX2=nwb_recording, return_scaled=False)
-                if recording.has_scaled_traces() and nwb_recording.has_scaled_traces():
-                    check_recordings_equal(RX1=recording, RX2=nwb_recording, return_scaled=True)
+            if self.nwb_recording.get_channel_ids()[0] != self.nwb_recording.get_channel_ids()[-1]:
+                check_recordings_equal(RX1=recording, RX2=self.nwb_recording, return_scaled=False)
+                if recording.has_scaled_traces() and self.nwb_recording.has_scaled_traces():
+                    check_recordings_equal(RX1=recording, RX2=self.nwb_recording, return_scaled=True)
 
     def check_interface_set_aligned_timestamps(self):
         self.setUpFreshInterface()
 
         random_number_generator = np.random.default_rng(seed=0)
         if self.interface._number_of_segments == 1:
             unaligned_timestamps = self.interface.get_timestamps()
@@ -672,7 +675,33 @@
                 self.check_interface_get_timestamps()
                 self.check_interface_set_aligned_timestamps()
                 self.check_shift_timestamps_by_start_time()
                 self.check_interface_original_timestamps_inmutability()
                 self.check_set_aligned_segment_starting_times()
 
                 self.check_nwbfile_temporal_alignment()
+
+
+class MiniscopeImagingInterfaceMixin(DataInterfaceTestMixin, TemporalAlignmentMixin):
+    def check_read_nwb(self, nwbfile_path: str):
+        with NWBHDF5IO(nwbfile_path, "r") as io:
+            nwbfile = io.read()
+
+            assert self.device_name in nwbfile.devices
+            device = nwbfile.devices[self.device_name]
+            assert isinstance(device, Miniscope)
+            imaging_plane = nwbfile.imaging_planes[self.imaging_plane_name]
+            assert imaging_plane.device.name == self.device_name
+
+            # Check OnePhotonSeries
+            assert self.photon_series_name in nwbfile.acquisition
+            one_photon_series = nwbfile.acquisition[self.photon_series_name]
+            assert one_photon_series.unit == "px"
+            assert one_photon_series.data.shape == (15, 752, 480)
+            assert one_photon_series.data.dtype == np.uint8
+            assert one_photon_series.rate is None
+            assert one_photon_series.starting_frame is None
+            assert one_photon_series.timestamps.shape == (15,)
+
+            imaging_extractor = self.interface.imaging_extractor
+            times_from_extractor = imaging_extractor._times
+            assert_array_equal(one_photon_series.timestamps, times_from_extractor)
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/testing/mock_files.py` & `neuroconv-0.4.0/src/neuroconv/tools/testing/mock_files.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,7 @@
-import os
 from pathlib import Path
 from typing import Optional
 
 
 def generate_path_expander_demo_ibl(folder_path: Optional[str] = None) -> None:
     """
     Partially replicate the file structure of IBL data with dummy files for
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/testing/mock_interfaces.py` & `neuroconv-0.4.0/src/neuroconv/tools/testing/mock_interfaces.py`

 * *Files 1% similar despite different names*

```diff
@@ -40,15 +40,15 @@
 
     def get_timestamps(self) -> np.ndarray:
         return self.event_times
 
     def set_aligned_timestamps(self, aligned_timestamps: np.ndarray):
         self.event_times = aligned_timestamps
 
-    def run_conversion(self, nwbfile: NWBFile, metadata: dict):
+    def add_to_nwbfile(self, nwbfile: NWBFile, metadata: dict):
         table = DynamicTable(name="BehaviorEvents", description="Times of various classified behaviors.")
         table.add_column(name="event_time", description="Time of each event.")
         for timestamp in self.get_timestamps():  # adding data by column gives error
             table.add_row(event_time=timestamp)
         nwbfile.add_acquisition(table)
```

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/testing/mock_ttl_signals.py` & `neuroconv-0.4.0/src/neuroconv/tools/testing/mock_ttl_signals.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/text.py` & `neuroconv-0.4.0/src/neuroconv/tools/text.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/tools/yaml_conversion_specification/yaml_conversion_specification.py` & `neuroconv-0.4.0/src/neuroconv/tools/yaml_conversion_specification/yaml_conversion_specification.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/utils/__init__.py` & `neuroconv-0.4.0/src/neuroconv/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/utils/checks.py` & `neuroconv-0.4.0/src/neuroconv/utils/checks.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/utils/dict.py` & `neuroconv-0.4.0/src/neuroconv/utils/dict.py`

 * *Files identical despite different names*

### Comparing `neuroconv-0.3.0/src/neuroconv/utils/json_schema.py` & `neuroconv-0.4.0/src/neuroconv/utils/json_schema.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,16 +1,17 @@
 import collections.abc
 import inspect
 import json
 from datetime import datetime
-from typing import Callable, Literal
+from typing import Callable, Dict, Literal
 
 import hdmf.data_utils
 import numpy as np
 import pynwb
+from jsonschema import validate
 from pynwb.device import Device
 from pynwb.icephys import IntracellularElectrode
 
 from .dict import dict_deep_update
 from .types import FilePathType, FolderPathType
 
 
@@ -92,30 +93,36 @@
                 if param.annotation.__args__ == (str, str):
                     args_spec[param_name].update(additionalProperties={"^.*$": dict(type="string")})
                 else:
                     args_spec[param_name].update(additionalProperties=True)
             elif hasattr(param.annotation, "__args__"):  # Annotation has __args__ if it was made by typing.Union
                 args = param.annotation.__args__
                 valid_args = [x.__name__ in annotation_json_type_map for x in args]
-                if any(valid_args):
-                    param_types = [annotation_json_type_map[x.__name__] for x in np.array(args)[valid_args]]
-                else:
+                if not any(valid_args):
                     raise ValueError(f"No valid arguments were found in the json type mapping for parameter {param}")
+                arg_types = [x for x in np.array(args)[valid_args]]
+                param_types = [annotation_json_type_map[x.__name__] for x in arg_types]
                 num_params = len(set(param_types))
                 conflict_message = (
                     "Conflicting json parameter types were detected from the annotation! "
                     f"{param.annotation.__args__} found."
                 )
                 # Normally cannot support Union[...] of multiple annotation types
                 if num_params > 2:
                     raise ValueError(conflict_message)
                 # Special condition for Optional[...]
                 if num_params == 2 and not args[1] is type(None):  # noqa: E721
                     raise ValueError(conflict_message)
+
+                # Guaranteed to only have a single index by this point
                 args_spec[param_name]["type"] = param_types[0]
+                if arg_types[0] == FilePathType:
+                    input_schema["properties"].update({param_name: dict(format="file")})
+                elif arg_types[0] == FolderPathType:
+                    input_schema["properties"].update({param_name: dict(format="directory")})
             else:
                 arg = param.annotation
                 if arg.__name__ in annotation_json_type_map:
                     args_spec[param_name]["type"] = annotation_json_type_map[arg.__name__]
                 else:
                     raise ValueError(
                         f"No valid arguments were found in the json type mapping '{arg}' for parameter {param}"
@@ -302,7 +309,18 @@
             intracellular_recordings_table_ind={"type": "number", "description": ""},
             simultaneous_recordings_table_ind={"type": "number", "description": ""},
             sequential_recordings_table_ind={"type": "number", "description": ""},
         ),
     )
 
     return schema
+
+
+def validate_metadata(metadata: Dict[str, dict], schema: Dict[str, dict], verbose: bool = False):
+    """Validate metadata against a schema."""
+    encoder = NWBMetaDataEncoder()
+    # The encoder produces a serialiazed object so we de serialized it for comparison
+    serialized_metadata = encoder.encode(metadata)
+    decoded_metadata = json.loads(serialized_metadata)
+    validate(instance=decoded_metadata, schema=schema)
+    if verbose:
+        print("Metadata is valid!")
```

### Comparing `neuroconv-0.3.0/src/neuroconv.egg-info/PKG-INFO` & `neuroconv-0.4.0/src/neuroconv.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,59 +1,61 @@
 Metadata-Version: 2.1
 Name: neuroconv
-Version: 0.3.0
+Version: 0.4.0
 Summary: Convert data from proprietary formats to NWB format.
 Home-page: https://github.com/catalystneuro/neuroconv
 Author: Cody Baker, Szonja Weigl, Heberto Mayorquin, Luiz Tauffer, and Ben Dichter.
 Author-email: ben.dichter@catalystneuro.com
+License: BSD-3-Clause
 Keywords: nwb
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: test
 Provides-Extra: docs
 Provides-Extra: full
 Provides-Extra: ophys
-Provides-Extra: sbx
-Provides-Extra: brukertiff
+Provides-Extra: scanimage
+Provides-Extra: sima
 Provides-Extra: micromanagertiff
-Provides-Extra: caiman
-Provides-Extra: cnmfe
+Provides-Extra: sbx
 Provides-Extra: hdf5
+Provides-Extra: extract
 Provides-Extra: suite2p
-Provides-Extra: sima
-Provides-Extra: scanimage
+Provides-Extra: miniscope
 Provides-Extra: tiff
-Provides-Extra: extract
+Provides-Extra: caiman
+Provides-Extra: cnmfe
+Provides-Extra: brukertiff
 Provides-Extra: ecephys
-Provides-Extra: intan
-Provides-Extra: kilosort
-Provides-Extra: mearec
-Provides-Extra: alphaomega
-Provides-Extra: cellexplorer
-Provides-Extra: phy
-Provides-Extra: spike2
 Provides-Extra: mcsraw
+Provides-Extra: tdt
+Provides-Extra: neuralynx
+Provides-Extra: cellexplorer
+Provides-Extra: alphaomega
+Provides-Extra: blackrock
+Provides-Extra: edf
 Provides-Extra: spikeinterface
 Provides-Extra: maxwell
+Provides-Extra: intan
+Provides-Extra: neuroscope
 Provides-Extra: spikegadgets
-Provides-Extra: edf
+Provides-Extra: axona
 Provides-Extra: spikeglx
-Provides-Extra: blackrock
-Provides-Extra: tdt
+Provides-Extra: spike2
 Provides-Extra: biocam
-Provides-Extra: neuralynx
-Provides-Extra: axona
-Provides-Extra: neuroscope
+Provides-Extra: phy
+Provides-Extra: mearec
+Provides-Extra: kilosort
 Provides-Extra: openephys
 Provides-Extra: plexon
 Provides-Extra: icephys
 Provides-Extra: abf
-Provides-Extra: sleap
-Provides-Extra: behavior
 Provides-Extra: video
+Provides-Extra: behavior
+Provides-Extra: sleap
 Provides-Extra: deeplabcut
 Provides-Extra: audio
 Provides-Extra: csv
 Provides-Extra: excel
 Provides-Extra: text
 License-File: license.txt
```

#### html2text {}

```diff
@@ -1,37 +1,37 @@
-Metadata-Version: 2.1 Name: neuroconv Version: 0.3.0 Summary: Convert data from
+Metadata-Version: 2.1 Name: neuroconv Version: 0.4.0 Summary: Convert data from
 proprietary formats to NWB format. Home-page: https://github.com/catalystneuro/
 neuroconv Author: Cody Baker, Szonja Weigl, Heberto Mayorquin, Luiz Tauffer,
-and Ben Dichter. Author-email: ben.dichter@catalystneuro.com Keywords: nwb
-Requires-Python: >=3.8 Description-Content-Type: text/markdown Provides-Extra:
-test Provides-Extra: docs Provides-Extra: full Provides-Extra: ophys Provides-
-Extra: sbx Provides-Extra: brukertiff Provides-Extra: micromanagertiff
-Provides-Extra: caiman Provides-Extra: cnmfe Provides-Extra: hdf5 Provides-
-Extra: suite2p Provides-Extra: sima Provides-Extra: scanimage Provides-Extra:
-tiff Provides-Extra: extract Provides-Extra: ecephys Provides-Extra: intan
-Provides-Extra: kilosort Provides-Extra: mearec Provides-Extra: alphaomega
-Provides-Extra: cellexplorer Provides-Extra: phy Provides-Extra: spike2
-Provides-Extra: mcsraw Provides-Extra: spikeinterface Provides-Extra: maxwell
-Provides-Extra: spikegadgets Provides-Extra: edf Provides-Extra: spikeglx
-Provides-Extra: blackrock Provides-Extra: tdt Provides-Extra: biocam Provides-
-Extra: neuralynx Provides-Extra: axona Provides-Extra: neuroscope Provides-
-Extra: openephys Provides-Extra: plexon Provides-Extra: icephys Provides-Extra:
-abf Provides-Extra: sleap Provides-Extra: behavior Provides-Extra: video
-Provides-Extra: deeplabcut Provides-Extra: audio Provides-Extra: csv Provides-
-Extra: excel Provides-Extra: text License-File: license.txt [![PyPI version]
-(https://badge.fury.io/py/neuroconv.svg)](https://badge.fury.io/py/
-neuroconv.svg) ![Full Tests](https://github.com/catalystneuro/neuroconv/
-actions/workflows/testing.yml/badge.svg) ![Auto-release](https://github.com/
-catalystneuro/neuroconv/actions/workflows/auto-publish.yml/badge.svg) [!
-[codecov](https://codecov.io/github/catalystneuro/neuroconv/
-coverage.svg?branch=main)](https://codecov.io/github/catalystneuro/
-neuroconv?branch=main) [![documentation](https://readthedocs.org/projects/
-neuroconv/badge/?version=main)](https://neuroconv.readthedocs.io/en/main/) [!
-[License](https://img.shields.io/pypi/l/neuroconv.svg)](https://github.com/
-catalystneuro/neuroconv/license.txt)
+and Ben Dichter. Author-email: ben.dichter@catalystneuro.com License: BSD-3-
+Clause Keywords: nwb Requires-Python: >=3.8 Description-Content-Type: text/
+markdown Provides-Extra: test Provides-Extra: docs Provides-Extra: full
+Provides-Extra: ophys Provides-Extra: scanimage Provides-Extra: sima Provides-
+Extra: micromanagertiff Provides-Extra: sbx Provides-Extra: hdf5 Provides-
+Extra: extract Provides-Extra: suite2p Provides-Extra: miniscope Provides-
+Extra: tiff Provides-Extra: caiman Provides-Extra: cnmfe Provides-Extra:
+brukertiff Provides-Extra: ecephys Provides-Extra: mcsraw Provides-Extra: tdt
+Provides-Extra: neuralynx Provides-Extra: cellexplorer Provides-Extra:
+alphaomega Provides-Extra: blackrock Provides-Extra: edf Provides-Extra:
+spikeinterface Provides-Extra: maxwell Provides-Extra: intan Provides-Extra:
+neuroscope Provides-Extra: spikegadgets Provides-Extra: axona Provides-Extra:
+spikeglx Provides-Extra: spike2 Provides-Extra: biocam Provides-Extra: phy
+Provides-Extra: mearec Provides-Extra: kilosort Provides-Extra: openephys
+Provides-Extra: plexon Provides-Extra: icephys Provides-Extra: abf Provides-
+Extra: video Provides-Extra: behavior Provides-Extra: sleap Provides-Extra:
+deeplabcut Provides-Extra: audio Provides-Extra: csv Provides-Extra: excel
+Provides-Extra: text License-File: license.txt [![PyPI version](https://
+badge.fury.io/py/neuroconv.svg)](https://badge.fury.io/py/neuroconv.svg) ![Full
+Tests](https://github.com/catalystneuro/neuroconv/actions/workflows/
+testing.yml/badge.svg) ![Auto-release](https://github.com/catalystneuro/
+neuroconv/actions/workflows/auto-publish.yml/badge.svg) [![codecov](https://
+codecov.io/github/catalystneuro/neuroconv/coverage.svg?branch=main)](https://
+codecov.io/github/catalystneuro/neuroconv?branch=main) [![documentation](https:
+//readthedocs.org/projects/neuroconv/badge/?version=main)](https://
+neuroconv.readthedocs.io/en/main/) [![License](https://img.shields.io/pypi/l/
+neuroconv.svg)](https://github.com/catalystneuro/neuroconv/license.txt)
                                [NeuroConv logo]
           **** Automatically convert neurophysiology data to NWB ****
                          Explore_our_documentation_Â»
  ## Table of Contents - [About](#about) - [Installation](#installation) -
 [Documentation](#documentation) - [License](#license) ## About NeuroConv is a
 Python package for converting neurophysiology data in a variety of proprietary
 formats to the [Neurodata Without Borders (NWB)](http://nwb.org) standard.
```

### Comparing `neuroconv-0.3.0/src/neuroconv.egg-info/SOURCES.txt` & `neuroconv-0.4.0/src/neuroconv.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -20,14 +20,16 @@
 src/neuroconv/converters/__init__.py
 src/neuroconv/datainterfaces/__init__.py
 src/neuroconv/datainterfaces/behavior/__init__.py
 src/neuroconv/datainterfaces/behavior/audio/__init__.py
 src/neuroconv/datainterfaces/behavior/audio/audiointerface.py
 src/neuroconv/datainterfaces/behavior/deeplabcut/__init__.py
 src/neuroconv/datainterfaces/behavior/deeplabcut/deeplabcutdatainterface.py
+src/neuroconv/datainterfaces/behavior/miniscope/__init__.py
+src/neuroconv/datainterfaces/behavior/miniscope/miniscopedatainterface.py
 src/neuroconv/datainterfaces/behavior/sleap/__init__.py
 src/neuroconv/datainterfaces/behavior/sleap/sleap_utils.py
 src/neuroconv/datainterfaces/behavior/sleap/sleapdatainterface.py
 src/neuroconv/datainterfaces/behavior/video/__init__.py
 src/neuroconv/datainterfaces/behavior/video/video_utils.py
 src/neuroconv/datainterfaces/behavior/video/videodatainterface.py
 src/neuroconv/datainterfaces/ecephys/__init__.py
@@ -98,14 +100,17 @@
 src/neuroconv/datainterfaces/ophys/cnmfe/cnmfedatainterface.py
 src/neuroconv/datainterfaces/ophys/extract/__init__.py
 src/neuroconv/datainterfaces/ophys/extract/extractdatainterface.py
 src/neuroconv/datainterfaces/ophys/hdf5/__init__.py
 src/neuroconv/datainterfaces/ophys/hdf5/hdf5datainterface.py
 src/neuroconv/datainterfaces/ophys/micromanagertiff/__init__.py
 src/neuroconv/datainterfaces/ophys/micromanagertiff/micromanagertiffdatainterface.py
+src/neuroconv/datainterfaces/ophys/miniscope/__init__.py
+src/neuroconv/datainterfaces/ophys/miniscope/miniscopeconverter.py
+src/neuroconv/datainterfaces/ophys/miniscope/miniscopeimagingdatainterface.py
 src/neuroconv/datainterfaces/ophys/sbx/__init__.py
 src/neuroconv/datainterfaces/ophys/sbx/sbxdatainterface.py
 src/neuroconv/datainterfaces/ophys/scanimage/__init__.py
 src/neuroconv/datainterfaces/ophys/scanimage/scanimageimaginginterface.py
 src/neuroconv/datainterfaces/ophys/sima/__init__.py
 src/neuroconv/datainterfaces/ophys/sima/simadatainterface.py
 src/neuroconv/datainterfaces/ophys/suite2p/__init__.py
```

### Comparing `neuroconv-0.3.0/src/neuroconv.egg-info/requires.txt` & `neuroconv-0.4.0/src/neuroconv.egg-info/requires.txt`

 * *Files 10% similar despite different names*

```diff
@@ -14,60 +14,63 @@
 pynwb>=2.3.2
 
 [abf]
 neo>=0.9.0
 ndx-dandi-icephys>=0.4.0
 
 [alphaomega]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [audio]
 ndx-sound>=0.2.0
 
 [axona]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [behavior]
+opencv-python-headless>=4.5.1.48
+ndx-miniscope>=0.5.1
+natsort>=8.3.1
 sleap-io>=0.0.2
 av>=10.0.0
-opencv-python-headless>=4.5.1.48
 dlc2nwb>=0.3
 tables
 ndx-sound>=0.2.0
 
 [behavior:sys_platform == "darwin"]
 opencv-python-headless<4.7.0.72,>=4.5.1.48
 
 [behavior:sys_platform == "darwin" and python_version >= "3.11"]
 opencv-python-headless<4.7,>=4.5.1.48
 
 [biocam]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [blackrock]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [brukertiff]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 tifffile>=2023.3.21
 
 [caiman]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 
 [cellexplorer]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 hdf5storage>=0.1.18
+pymatreader>=0.0.32
 
 [cnmfe]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 
 [csv]
 
 [deeplabcut]
 dlc2nwb>=0.3
 tables
 
@@ -77,176 +80,196 @@
 sphinx_rtd_theme==1.0.0
 readthedocs-sphinx-search==0.1.2
 sphinx-toggleprompt==0.2.0
 sphinx-copybutton==0.5.0
 roiextractors
 
 [ecephys]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
-pyintan>=0.3.0
-MEArec>=1.8.0
+natsort>=7.1.1
 hdf5storage>=0.1.18
-spikeextractors
+pymatreader>=0.0.32
 pyedflib>=0.1.30
-natsort>=7.1.1
+spikeextractors
+pyintan>=0.3.0
 lxml>=4.6.5
+MEArec>=1.8.0
 pyopenephys>=1.1.2
 
 [ecephys:python_version <= "3.9"]
 sonpy>=1.7.1
 
+[ecephys:python_version >= "3.11"]
+numpy<1.25.0
+
 [edf]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 pyedflib>=0.1.30
 
+[edf:python_version >= "3.11"]
+numpy<1.25.0
+
 [excel]
 openpyxl
 xlrd
 
 [extract]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 
 [full]
-roiextractors>=0.5.2
-tifffile>=2023.3.21
+roiextractors>=0.5.3
 scanimage-tiff-reader>=1.4.1
+tifffile>=2023.3.21
+ndx-miniscope>=0.5.1
+natsort>=8.3.1
 tiffile>=2018.10.18
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
-pyintan>=0.3.0
-MEArec>=1.8.0
+natsort>=7.1.1
 hdf5storage>=0.1.18
-spikeextractors
+pymatreader>=0.0.32
 pyedflib>=0.1.30
-natsort>=7.1.1
+spikeextractors
+pyintan>=0.3.0
 lxml>=4.6.5
+MEArec>=1.8.0
 pyopenephys>=1.1.2
 neo>=0.9.0
 ndx-dandi-icephys>=0.4.0
+opencv-python-headless>=4.5.1.48
 sleap-io>=0.0.2
 av>=10.0.0
-opencv-python-headless>=4.5.1.48
 dlc2nwb>=0.3
 tables
 ndx-sound>=0.2.0
 openpyxl
 xlrd
 
 [full:python_version <= "3.9"]
 sonpy>=1.7.1
 
+[full:python_version >= "3.11"]
+numpy<1.25.0
+
 [full:sys_platform == "darwin"]
 opencv-python-headless<4.7.0.72,>=4.5.1.48
 
 [full:sys_platform == "darwin" and python_version >= "3.11"]
 opencv-python-headless<4.7,>=4.5.1.48
 
 [hdf5]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 
 [icephys]
 neo>=0.9.0
 ndx-dandi-icephys>=0.4.0
 
 [intan]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 pyintan>=0.3.0
 
 [kilosort]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [maxwell]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [mcsraw]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [mearec]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 MEArec>=1.8.0
 
 [micromanagertiff]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 tifffile>=2023.3.21
 
+[miniscope]
+roiextractors>=0.5.3
+ndx-miniscope>=0.5.1
+natsort>=8.3.1
+
 [neuralynx]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 natsort>=7.1.1
 
 [neuroscope]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 lxml>=4.6.5
 
 [openephys]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 pyopenephys>=1.1.2
 
 [ophys]
-roiextractors>=0.5.2
-tifffile>=2023.3.21
+roiextractors>=0.5.3
 scanimage-tiff-reader>=1.4.1
+tifffile>=2023.3.21
+ndx-miniscope>=0.5.1
+natsort>=8.3.1
 tiffile>=2018.10.18
 
 [phy]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [plexon]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [sbx]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 
 [scanimage]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 scanimage-tiff-reader>=1.4.1
 
 [sima]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 
 [sleap]
 sleap-io>=0.0.2
 av>=10.0.0
 
 [spike2]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [spike2:python_version <= "3.9"]
 sonpy>=1.7.1
 
 [spikegadgets]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [spikeglx]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [spikeinterface]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 spikeextractors
 
 [suite2p]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 
 [tdt]
-spikeinterface>=0.97.1
+spikeinterface>=0.98.2
 packaging<22.0
 
 [test]
 pytest
 pytest-cov
 ndx-events>=0.2.0
 parameterized>=0.8.1
@@ -256,15 +279,15 @@
 numba
 
 [text]
 openpyxl
 xlrd
 
 [tiff]
-roiextractors>=0.5.2
+roiextractors>=0.5.3
 tiffile>=2018.10.18
 
 [video]
 opencv-python-headless>=4.5.1.48
 
 [video:sys_platform == "darwin"]
 opencv-python-headless<4.7.0.72,>=4.5.1.48
```

