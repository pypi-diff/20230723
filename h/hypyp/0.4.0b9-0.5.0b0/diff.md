# Comparing `tmp/hypyp-0.4.0b9.tar.gz` & `tmp/hypyp-0.5.0b0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hypyp-0.4.0b9.tar", max compression
+gzip compressed data, was "hypyp-0.5.0b0.tar", max compression
```

## Comparing `hypyp-0.4.0b9.tar` & `hypyp-0.5.0b0.tar`

### file list

```diff
@@ -1,20 +1,20 @@
--rw-r--r--   0        0        0     1524 2023-05-12 13:18:38.310986 hypyp-0.4.0b9/LICENSE
--rw-r--r--   0        0        0     3524 2023-05-12 13:18:38.311148 hypyp-0.4.0b9/README.md
--rw-r--r--   0        0        0      192 2023-05-12 13:18:38.586933 hypyp-0.4.0b9/hypyp/__init__.py
--rw-r--r--   0        0        0    35571 2023-07-20 21:40:02.899871 hypyp-0.4.0b9/hypyp/analyses.py
--rw-r--r--   0        0        0    13770 2023-05-12 13:18:38.588050 hypyp-0.4.0b9/hypyp/data/Basehead.obj
--rw-r--r--   0        0        0        1 2023-05-12 13:18:38.588445 hypyp-0.4.0b9/hypyp/ext/mpl3d/__init__.py
--rw-r--r--   0        0        0     4511 2023-05-12 13:18:38.588628 hypyp-0.4.0b9/hypyp/ext/mpl3d/camera.py
--rw-r--r--   0        0        0     7705 2023-05-12 13:18:38.589183 hypyp-0.4.0b9/hypyp/ext/mpl3d/glm.py
--rw-r--r--   0        0        0     3147 2023-05-12 13:18:38.589330 hypyp-0.4.0b9/hypyp/ext/mpl3d/lighting.py
--rw-r--r--   0        0        0     2990 2023-05-12 13:18:38.589460 hypyp-0.4.0b9/hypyp/ext/mpl3d/mesh.py
--rw-r--r--   0        0        0     9205 2023-05-12 13:18:38.589643 hypyp-0.4.0b9/hypyp/ext/mpl3d/trackball.py
--rw-r--r--   0        0        0     9887 2023-05-12 13:18:38.589827 hypyp-0.4.0b9/hypyp/fnirs_tools.py
--rw-r--r--   0        0        0        1 2023-05-12 13:18:38.589947 hypyp-0.4.0b9/hypyp/io.py
--rw-r--r--   0        0        0     9148 2023-05-12 13:18:38.590193 hypyp-0.4.0b9/hypyp/mvarica.py
--rw-r--r--   0        0        0    12650 2023-05-12 13:18:38.590381 hypyp-0.4.0b9/hypyp/prep.py
--rw-r--r--   0        0        0    21562 2023-05-12 13:18:38.590649 hypyp-0.4.0b9/hypyp/stats.py
--rw-r--r--   0        0        0    15121 2023-05-12 13:18:38.590859 hypyp-0.4.0b9/hypyp/utils.py
--rw-r--r--   0        0        0    69698 2023-05-12 13:18:38.591292 hypyp-0.4.0b9/hypyp/viz.py
--rw-r--r--   0        0        0     1779 2023-07-20 21:37:02.661190 hypyp-0.4.0b9/pyproject.toml
--rw-r--r--   0        0        0     4926 1970-01-01 00:00:00.000000 hypyp-0.4.0b9/PKG-INFO
+-rw-r--r--   0        0        0     1524 2023-05-12 13:18:38.310986 hypyp-0.5.0b0/LICENSE
+-rw-r--r--   0        0        0     3566 2023-07-23 00:30:33.560601 hypyp-0.5.0b0/README.md
+-rw-r--r--   0        0        0      179 2023-07-22 23:20:29.348412 hypyp-0.5.0b0/hypyp/__init__.py
+-rw-r--r--   0        0        0    35843 2023-07-22 20:11:20.545731 hypyp-0.5.0b0/hypyp/analyses.py
+-rw-r--r--   0        0        0    13770 2023-05-12 13:18:38.588050 hypyp-0.5.0b0/hypyp/data/Basehead.obj
+-rw-r--r--   0        0        0        1 2023-05-12 13:18:38.588445 hypyp-0.5.0b0/hypyp/ext/mpl3d/__init__.py
+-rw-r--r--   0        0        0     4511 2023-05-12 13:18:38.588628 hypyp-0.5.0b0/hypyp/ext/mpl3d/camera.py
+-rw-r--r--   0        0        0     7705 2023-05-12 13:18:38.589183 hypyp-0.5.0b0/hypyp/ext/mpl3d/glm.py
+-rw-r--r--   0        0        0     3147 2023-05-12 13:18:38.589330 hypyp-0.5.0b0/hypyp/ext/mpl3d/lighting.py
+-rw-r--r--   0        0        0     2990 2023-05-12 13:18:38.589460 hypyp-0.5.0b0/hypyp/ext/mpl3d/mesh.py
+-rw-r--r--   0        0        0     9205 2023-05-12 13:18:38.589643 hypyp-0.5.0b0/hypyp/ext/mpl3d/trackball.py
+-rw-r--r--   0        0        0     9887 2023-05-12 13:18:38.589827 hypyp-0.5.0b0/hypyp/fnirs_tools.py
+-rw-r--r--   0        0        0        1 2023-05-12 13:18:38.589947 hypyp-0.5.0b0/hypyp/io.py
+-rw-r--r--   0        0        0     9148 2023-05-12 13:18:38.590193 hypyp-0.5.0b0/hypyp/mvarica.py
+-rw-r--r--   0        0        0    12650 2023-07-22 19:35:17.847420 hypyp-0.5.0b0/hypyp/prep.py
+-rw-r--r--   0        0        0    21562 2023-05-12 13:18:38.590649 hypyp-0.5.0b0/hypyp/stats.py
+-rw-r--r--   0        0        0    15121 2023-05-12 13:18:38.590859 hypyp-0.5.0b0/hypyp/utils.py
+-rw-r--r--   0        0        0    69995 2023-07-23 00:26:53.243713 hypyp-0.5.0b0/hypyp/viz.py
+-rw-r--r--   0        0        0     1808 2023-07-23 00:29:41.394603 hypyp-0.5.0b0/pyproject.toml
+-rw-r--r--   0        0        0     5020 1970-01-01 00:00:00.000000 hypyp-0.5.0b0/PKG-INFO
```

### Comparing `hypyp-0.4.0b9/LICENSE` & `hypyp-0.5.0b0/LICENSE`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/README.md` & `hypyp-0.5.0b0/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 # HyPyP 🐍〰️🐍
 
 The **Hy**perscanning **Py**thon **P**ipeline
 
-[![PyPI version shields.io](https://img.shields.io/pypi/v/hypyp.svg)](https://pypi.org/project/HyPyP/) <a href="https://travis-ci.org/ppsp-team/HyPyP"><img src="https://travis-ci.org/ppsp-team/HyPyP.svg?branch=master"></a> <a href="https://hypyp.readthedocs.io"><img src="https://readthedocs.org/projects/hypyp/badge/?version=latest"></a> [![license](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause) [![Mattermost](https://img.shields.io/discord/1065810348944408616?color=blue)](https://discord.gg/zYzjeGj7D6)
+[![PyPI version shields.io](https://img.shields.io/pypi/v/hypyp.svg)](https://pypi.org/project/HyPyP/) [![CI](https://github.com/ppsp-team/HyPyP/actions/workflows/Build.yml/badge.svg)](https://github.com/ppsp-team/HyPyP/actions/workflows/Build.yml) <a href="https://hypyp.readthedocs.io"><img src="https://readthedocs.org/projects/hypyp/badge/?version=latest"></a> [![license](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause) [![Mattermost](https://img.shields.io/discord/1065810348944408616?color=blue)](https://discord.gg/zYzjeGj7D6)
 
 ⚠️ This software is in beta and thus should be considered with caution. While we have done our best to test all the functionalities, there is no guarantee that the pipeline is entirely bug-free. 
 
 📖 See our [paper](https://academic.oup.com/scan/advance-article/doi/10.1093/scan/nsaa141/5919711) for more explanation and our plan for upcoming functionalities (aka Roadmap).
 
 🤝 If you want to help you can submit bugs and suggestions of enhancements in our Github [Issues section](https://github.com/ppsp-team/HyPyP/issues).
 
 🤓 For the motivated contributors, you can even help directly in the developpment of HyPyP. You will need to install [Poetry](https://python-poetry.org/) (see section below).
 
 ## Contributors
 Original authors: Florence BRUN, Anaël AYROLLES, Phoebe CHEN, Amir DJALOVSKI, Yann BEAUXIS, Suzanne DIKKER, Guillaume DUMAS
-New contributors: Ghazaleh RANJBARAN, Quentin MOREAU, Caitriona DOUGLAS, Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO
+New contributors: Ghazaleh RANJBARAN, Quentin MOREAU, Caitriona DOUGLAS, Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO, Julie BONNAIRE
 
 ## Installation
 
 ```
 pip install HyPyP
 ```
```

#### html2text {}

```diff
@@ -1,45 +1,46 @@
 # HyPyP ðã°ï¸ð The **Hy**perscanning **Py**thon **P**ipeline [![PyPI
 version shields.io](https://img.shields.io/pypi/v/hypyp.svg)](https://pypi.org/
-project/HyPyP/) [https://travis-ci.org/ppsp-team/HyPyP.svg?branch=master]
-[https://readthedocs.org/projects/hypyp/badge/?version=latest] [![license]
-(https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://
-opensource.org/licenses/BSD-3-Clause) [![Mattermost](https://img.shields.io/
-discord/1065810348944408616?color=blue)](https://discord.gg/zYzjeGj7D6) â ï¸
-This software is in beta and thus should be considered with caution. While we
-have done our best to test all the functionalities, there is no guarantee that
-the pipeline is entirely bug-free. ð See our [paper](https://
-academic.oup.com/scan/advance-article/doi/10.1093/scan/nsaa141/5919711) for
-more explanation and our plan for upcoming functionalities (aka Roadmap). ð¤
-If you want to help you can submit bugs and suggestions of enhancements in our
-Github [Issues section](https://github.com/ppsp-team/HyPyP/issues). ð¤ For
-the motivated contributors, you can even help directly in the developpment of
-HyPyP. You will need to install [Poetry](https://python-poetry.org/) (see
-section below). ## Contributors Original authors: Florence BRUN, AnaÃ«l
-AYROLLES, Phoebe CHEN, Amir DJALOVSKI, Yann BEAUXIS, Suzanne DIKKER, Guillaume
-DUMAS New contributors: Ghazaleh RANJBARAN, Quentin MOREAU, Caitriona DOUGLAS,
-Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO ## Installation ``` pip install
-HyPyP ``` ## Documentation HyPyP documentation of all the API functions is
-available online at [hypyp.readthedocs.io](https://hypyp.readthedocs.io/) For
-getting started with HyPyP, we have designed a little walkthrough:
-[getting_started.ipynb](https://github.com/ppsp-team/HyPyP/blob/master/
-tutorial/getting_started.ipynb) ## Core API ð  [io.py](https://github.com/
-ppsp-team/HyPyP/blob/master/hypyp/io.py) â Loaders (Florence, AnaÃ«l,
-Ghazaleh, Franck, Jonas, Guillaume) ð§° [utils.py](https://github.com/ppsp-
-team/HyPyP/blob/master/hypyp/utils.py) â Basic tools (Amir, Florence,
-Guilaume) âï¸ [prep.py](https://github.com/ppsp-team/HyPyP/blob/master/
-hypyp/prep.py) â Preprocessing (ICA & AutoReject) (AnaÃ«l, Florence,
-Guillaume) ð  [analyses.py](https://github.com/ppsp-team/HyPyP/blob/master/
-hypyp/analyses.py) â Power spectral density and wide choice of connectivity
-measures (Phoebe, Suzanne, Florence, Ghazaleh, Juan, Guillaume) ð [stats.py]
-(https://github.com/ppsp-team/HyPyP/blob/master/hypyp/stats.py) â Statistics
-(permutations & cluster statistics) (Florence, Guillaume) ð§  [viz.py](https:/
-/github.com/ppsp-team/HyPyP/blob/master/hypyp/viz.py) â Inter-brain
-visualization (AnaÃ«l, Amir, Florence, Guillaume) ð [Tutorials](https://
-github.com/ppsp-team/HyPyP/tree/master/tutorial) - Examples & documentation
-(AnaÃ«l, Florence, Yann, Ghazaleh, Caitriona, Guillaume) ## Poetry installation
-(only for developpers and adventurous users) Step 1: ```pip install poetry```
-Step 2: ```git clone git@github.com:ppsp-team/HyPyP.git``` Step 3: ```cd
-HyPyP``` Step 4: ```poetry install``` Step 5: ```poetry shell``` You can now
-use ```jupyter notebook``` or ```ipython```! â ï¸ If you need to install a
-new dependency (not recommended), you have to use `poetry add
+project/HyPyP/) [![CI](https://github.com/ppsp-team/HyPyP/actions/workflows/
+Build.yml/badge.svg)](https://github.com/ppsp-team/HyPyP/actions/workflows/
+Build.yml) [https://readthedocs.org/projects/hypyp/badge/?version=latest] [!
+[license](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)]
+(https://opensource.org/licenses/BSD-3-Clause) [![Mattermost](https://
+img.shields.io/discord/1065810348944408616?color=blue)](https://discord.gg/
+zYzjeGj7D6) â ï¸ This software is in beta and thus should be considered with
+caution. While we have done our best to test all the functionalities, there is
+no guarantee that the pipeline is entirely bug-free. ð See our [paper]
+(https://academic.oup.com/scan/advance-article/doi/10.1093/scan/nsaa141/
+5919711) for more explanation and our plan for upcoming functionalities (aka
+Roadmap). ð¤ If you want to help you can submit bugs and suggestions of
+enhancements in our Github [Issues section](https://github.com/ppsp-team/HyPyP/
+issues). ð¤ For the motivated contributors, you can even help directly in the
+developpment of HyPyP. You will need to install [Poetry](https://python-
+poetry.org/) (see section below). ## Contributors Original authors: Florence
+BRUN, AnaÃ«l AYROLLES, Phoebe CHEN, Amir DJALOVSKI, Yann BEAUXIS, Suzanne
+DIKKER, Guillaume DUMAS New contributors: Ghazaleh RANJBARAN, Quentin MOREAU,
+Caitriona DOUGLAS, Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO, Julie
+BONNAIRE ## Installation ``` pip install HyPyP ``` ## Documentation HyPyP
+documentation of all the API functions is available online at
+[hypyp.readthedocs.io](https://hypyp.readthedocs.io/) For getting started with
+HyPyP, we have designed a little walkthrough: [getting_started.ipynb](https://
+github.com/ppsp-team/HyPyP/blob/master/tutorial/getting_started.ipynb) ## Core
+API ð  [io.py](https://github.com/ppsp-team/HyPyP/blob/master/hypyp/io.py)
+â Loaders (Florence, AnaÃ«l, Ghazaleh, Franck, Jonas, Guillaume) ð§°
+[utils.py](https://github.com/ppsp-team/HyPyP/blob/master/hypyp/utils.py) â
+Basic tools (Amir, Florence, Guilaume) âï¸ [prep.py](https://github.com/
+ppsp-team/HyPyP/blob/master/hypyp/prep.py) â Preprocessing (ICA & AutoReject)
+(AnaÃ«l, Florence, Guillaume) ð  [analyses.py](https://github.com/ppsp-team/
+HyPyP/blob/master/hypyp/analyses.py) â Power spectral density and wide choice
+of connectivity measures (Phoebe, Suzanne, Florence, Ghazaleh, Juan, Guillaume)
+ð [stats.py](https://github.com/ppsp-team/HyPyP/blob/master/hypyp/stats.py)
+â Statistics (permutations & cluster statistics) (Florence, Guillaume) ð§ 
+[viz.py](https://github.com/ppsp-team/HyPyP/blob/master/hypyp/viz.py) â
+Inter-brain visualization (AnaÃ«l, Amir, Florence, Guillaume) ð [Tutorials]
+(https://github.com/ppsp-team/HyPyP/tree/master/tutorial) - Examples &
+documentation (AnaÃ«l, Florence, Yann, Ghazaleh, Caitriona, Guillaume) ##
+Poetry installation (only for developpers and adventurous users) Step 1: ```pip
+install poetry``` Step 2: ```git clone git@github.com:ppsp-team/HyPyP.git```
+Step 3: ```cd HyPyP``` Step 4: ```poetry install``` Step 5: ```poetry shell```
+You can now use ```jupyter notebook``` or ```ipython```! â ï¸ If you need to
+install a new dependency (not recommended), you have to use `poetry add
 THE_NAME_OF_THE_LIBRARY` instead of your usual package manager.
```

### Comparing `hypyp-0.4.0b9/hypyp/analyses.py` & `hypyp-0.5.0b0/hypyp/analyses.py`

 * *Files 2% similar despite different names*

```diff
@@ -190,28 +190,31 @@
         for i in range(0, data.shape[1]):
             for j in range(0, data.shape[2]):
                 r_i, pvalue_i = scipy.stats.pearsonr(behav, data[:, i, j])
                 rs[i, j] = r_i
                 pvals[i, j] = pvalue_i
         # correction for multiple comparisons
         if multiple_corr is True:
-            pvals_corrected = statsmodels.stats.multitest.multipletests(pvals,
+            # note: we reshape pvals to be able to use fdr_bh
+            pvals_corrected = statsmodels.stats.multitest.multipletests(pvals.flatten(),
                                                                         alpha=0.05,
                                                                         method='fdr_bh',
                                                                         is_sorted=False,
                                                                         returnsorted=False)
+            # put pval in original shape
+            pvals_corrected = np.reshape(np.atleast_1d(pvals_corrected[1]), pvals.shape)
         # get r value for significant correlation only
         for i in range(0, data.shape[1]):
             for j in range(0, data.shape[2]):
                 # with pvalues non corrected for multiple comparisons
                 if multiple_corr is False:
                     pvalue = pvals
                 # or corrected for multiple comparisons
                 else:
-                    pvalue = pvals_corrected[0]
+                    pvalue = pvals_corrected
                 if pvalue[i, j] < p_thresh:
                     significant_corr[i, j] = rs[i, j]
         r = np.nan_to_num(significant_corr)
         strat = 'correction for multiple comaprison ' + str(multiple_corr)
         return corr_tuple(r=r, pvalue=pvalue, strat=strat)
 
 
@@ -335,15 +338,16 @@
     """
 
     # Data consists of two lists of np.array (n_epochs, n_channels, epoch_size)
     assert data[0].shape[0] == data[1].shape[0], "Two streams much have the same lengths."
 
     # compute instantaneous analytic signal from EEG data
     if type(frequencies) == list:
-        values = compute_single_freq(data, sampling_rate, frequencies)
+        # average over tapers
+        values = np.mean(compute_single_freq(data, sampling_rate, frequencies), 3).squeeze()
     elif type(frequencies) == dict:
         values = compute_freq_bands(data, sampling_rate, frequencies)
     else:
         TypeError("Please use a list or a dictionary to specify frequencies.")
 
     # compute connectivity values
     result = compute_sync(values, mode, epochs_average)
@@ -736,15 +740,15 @@
         con:
             Connectivity matrix. The shape is either (n_freq, 2*n_channels, 2*n_channels)
 
             To extract inter-brain connectivity values, slice the last two dimensions of con with [0:n_channels, n_channels: 2*n_channels].
     """
     r = np.mean(freq_range2)/np.mean(freq_range1)
     freq_range = [np.min(freq_range1), np.max(freq_range2)]
-    complex_signal = compute_single_freq(data, sampling_rate, freq_range, **filter_options)
+    complex_signal = np.mean(compute_single_freq(data, sampling_rate, freq_range, **filter_options),3).squeeze()
 
     n_epoch, n_ch, n_freq, n_samp = complex_signal.shape[1], complex_signal.shape[2], \
                                     complex_signal.shape[3], complex_signal.shape[4]
 
     # calculate all epochs at once, the only downside is that the disk may not have enough space
     complex_signal = complex_signal.transpose((1, 3, 0, 2, 4)).reshape(n_epoch, n_freq, 2 * n_ch, n_samp)
     transpose_axes = (0, 1, 3, 2)
```

### Comparing `hypyp-0.4.0b9/hypyp/data/Basehead.obj` & `hypyp-0.5.0b0/hypyp/data/Basehead.obj`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/ext/mpl3d/camera.py` & `hypyp-0.5.0b0/hypyp/ext/mpl3d/camera.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/ext/mpl3d/glm.py` & `hypyp-0.5.0b0/hypyp/ext/mpl3d/glm.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/ext/mpl3d/lighting.py` & `hypyp-0.5.0b0/hypyp/ext/mpl3d/lighting.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/ext/mpl3d/mesh.py` & `hypyp-0.5.0b0/hypyp/ext/mpl3d/mesh.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/ext/mpl3d/trackball.py` & `hypyp-0.5.0b0/hypyp/ext/mpl3d/trackball.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/fnirs_tools.py` & `hypyp-0.5.0b0/hypyp/fnirs_tools.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/mvarica.py` & `hypyp-0.5.0b0/hypyp/mvarica.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/prep.py` & `hypyp-0.5.0b0/hypyp/prep.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/stats.py` & `hypyp-0.5.0b0/hypyp/stats.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/utils.py` & `hypyp-0.5.0b0/hypyp/utils.py`

 * *Files identical despite different names*

### Comparing `hypyp-0.4.0b9/hypyp/viz.py` & `hypyp-0.5.0b0/hypyp/viz.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,15 +15,17 @@
 from copy import copy
 from typing import Union
 import numpy as np
 import matplotlib
 import matplotlib.pyplot as plt
 import mne
 import meshio
-import pkg_resources
+import importlib_resources
+from contextlib import ExitStack
+import atexit
 import math
 
 from hypyp.ext.mpl3d import glm
 from hypyp.ext.mpl3d.mesh import Mesh
 from hypyp.ext.mpl3d.camera import Camera
 from hypyp.analyses import xwt
 
@@ -502,16 +504,15 @@
     # topoplot of significant sensors
     if np.max(np.abs(T_obs_plot)) != 0:
         vmax = np.max(np.abs(T_obs_plot))
         vmin = -vmax
     else:
         vmax = None
         vmin = None
-        mne.viz.plot_topomap(T_obs_plot, pos, vmin=vmin, vmax=vmax,
-                             sensors=True)
+        mne.viz.plot_topomap(T_obs_plot, pos, vlim=(vmin, vmax), sensors=True)
 
     return None
 
 
 def plot_2d_topomap_inter(ax):
     """
     Plot 2D head topomap for hyper-connectivity
@@ -584,15 +585,19 @@
   
 def get_3d_heads_inter():
     """
     Returns Vertices and Faces of a 3D OBJ representing two facing heads.
     """
    
     # Extract vertices and faces for the first head
-    filename = pkg_resources.resource_filename('hypyp', 'data/Basehead.obj')
+    file_manager = ExitStack()
+    atexit.register(file_manager.close)
+    ref = importlib_resources.files('hypyp') / 'data/Basehead.obj'
+    filename = file_manager.enter_context(importlib_resources.as_file(ref))
+
     mesh = meshio.read(Path(filename).resolve())
     zoom = 0.064
     interval = 0.32
 
     head1_v = mesh.points*zoom
     head1_f = mesh.cells[0].data
 
@@ -1220,15 +1225,19 @@
   
 def get_3d_heads_intra():
     """
     Returns Vertices and Faces of a 3D OBJ representing two facing heads.
     """
    
     # Extract vertices and faces for the first head
-    filename = pkg_resources.resource_filename('hypyp', 'data/Basehead.obj')
+    file_manager = ExitStack()
+    atexit.register(file_manager.close)
+    ref = importlib_resources.files('hypyp') / 'data/Basehead.obj'
+    filename = file_manager.enter_context(importlib_resources.as_file(ref))
+
     mesh = meshio.read(Path(filename).resolve())
     zoom = 0.064
     interval = 0.5
 
     head1_v = mesh.points*zoom
     head1_f = mesh.cells[0].data
```

### Comparing `hypyp-0.4.0b9/pyproject.toml` & `hypyp-0.5.0b0/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "hypyp"
-version = "0.4.0-beta.9"
+version = "0.5.0-beta"
 description = "The Hyperscanning Python Pipeline."
 readme = "README.md"
 authors = [
     "Anaël AYROLLLES <anael.ayrollles@pasteur.fr>",
     "Florence BRUN <florence.brun@pasteur.fr>",
     "Phoebe CHEN <phoebe.chen1117@gmail.com>",
     "Amir DJALOVSKI <amir.djv@gmail.com>",
@@ -35,14 +35,15 @@
 tqdm = "^4.46.0"
 scipy = "^1.4.1"
 mne = "^1.3"
 h5io = "^0.1.7"
 mistune = ">=2.0.4"
 future = ">=0.18.3"
 certifi = ">=2022.12.07"
+importlib-resources = "^6.0.0"
 
 [tool.poetry.group.dev.dependencies]
 mkdocs = ">=1.3.0"
 mkdocs-material = ">=8.2.15"
 pylint = "^2.4.4"
 black = "^19.10b0"
 markdown-include = "^0.5.1"
```

### Comparing `hypyp-0.4.0b9/PKG-INFO` & `hypyp-0.5.0b0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hypyp
-Version: 0.4.0b9
+Version: 0.5.0b0
 Summary: The Hyperscanning Python Pipeline.
 Home-page: https://github.com/ppsp-team/HyPyP
 License: BSD-3-Clause
 Keywords: hyperscanning,neuroscience,pipeline,statistics,visualization
 Author: Anaël AYROLLLES
 Author-email: anael.ayrollles@pasteur.fr
 Requires-Python: >=3.8,<4.0
@@ -17,14 +17,15 @@
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Scientific/Engineering
 Requires-Dist: astropy (>=5.1,<6.0)
 Requires-Dist: autoreject (>=0.3.1)
 Requires-Dist: certifi (>=2022.12.07)
 Requires-Dist: future (>=0.18.3)
 Requires-Dist: h5io (>=0.1.7,<0.2.0)
+Requires-Dist: importlib-resources (>=6.0.0,<7.0.0)
 Requires-Dist: matplotlib (>=3.2.1,<4.0.0)
 Requires-Dist: meshio (>=5.3.4,<6.0.0)
 Requires-Dist: mistune (>=2.0.4)
 Requires-Dist: mne (>=1.3,<2.0)
 Requires-Dist: numpy (>=1.18.3,<2.0.0)
 Requires-Dist: pandas (>=1.0.3,<2.0.0)
 Requires-Dist: scipy (>=1.4.1,<2.0.0)
@@ -34,27 +35,27 @@
 Project-URL: Repository, https://github.com/ppsp-team/HyPyP
 Description-Content-Type: text/markdown
 
 # HyPyP 🐍〰️🐍
 
 The **Hy**perscanning **Py**thon **P**ipeline
 
-[![PyPI version shields.io](https://img.shields.io/pypi/v/hypyp.svg)](https://pypi.org/project/HyPyP/) <a href="https://travis-ci.org/ppsp-team/HyPyP"><img src="https://travis-ci.org/ppsp-team/HyPyP.svg?branch=master"></a> <a href="https://hypyp.readthedocs.io"><img src="https://readthedocs.org/projects/hypyp/badge/?version=latest"></a> [![license](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause) [![Mattermost](https://img.shields.io/discord/1065810348944408616?color=blue)](https://discord.gg/zYzjeGj7D6)
+[![PyPI version shields.io](https://img.shields.io/pypi/v/hypyp.svg)](https://pypi.org/project/HyPyP/) [![CI](https://github.com/ppsp-team/HyPyP/actions/workflows/Build.yml/badge.svg)](https://github.com/ppsp-team/HyPyP/actions/workflows/Build.yml) <a href="https://hypyp.readthedocs.io"><img src="https://readthedocs.org/projects/hypyp/badge/?version=latest"></a> [![license](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause) [![Mattermost](https://img.shields.io/discord/1065810348944408616?color=blue)](https://discord.gg/zYzjeGj7D6)
 
 ⚠️ This software is in beta and thus should be considered with caution. While we have done our best to test all the functionalities, there is no guarantee that the pipeline is entirely bug-free. 
 
 📖 See our [paper](https://academic.oup.com/scan/advance-article/doi/10.1093/scan/nsaa141/5919711) for more explanation and our plan for upcoming functionalities (aka Roadmap).
 
 🤝 If you want to help you can submit bugs and suggestions of enhancements in our Github [Issues section](https://github.com/ppsp-team/HyPyP/issues).
 
 🤓 For the motivated contributors, you can even help directly in the developpment of HyPyP. You will need to install [Poetry](https://python-poetry.org/) (see section below).
 
 ## Contributors
 Original authors: Florence BRUN, Anaël AYROLLES, Phoebe CHEN, Amir DJALOVSKI, Yann BEAUXIS, Suzanne DIKKER, Guillaume DUMAS
-New contributors: Ghazaleh RANJBARAN, Quentin MOREAU, Caitriona DOUGLAS, Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO
+New contributors: Ghazaleh RANJBARAN, Quentin MOREAU, Caitriona DOUGLAS, Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO, Julie BONNAIRE
 
 ## Installation
 
 ```
 pip install HyPyP
 ```
```

#### html2text {}

```diff
@@ -1,63 +1,65 @@
-Metadata-Version: 2.1 Name: hypyp Version: 0.4.0b9 Summary: The Hyperscanning
+Metadata-Version: 2.1 Name: hypyp Version: 0.5.0b0 Summary: The Hyperscanning
 Python Pipeline. Home-page: https://github.com/ppsp-team/HyPyP License: BSD-3-
 Clause Keywords: hyperscanning,neuroscience,pipeline,statistics,visualization
 Author: AnaÃ«l AYROLLLES Author-email: anael.ayrollles@pasteur.fr Requires-
 Python: >=3.8,<4.0 Classifier: Development Status :: 4 - Beta Classifier:
 License :: OSI Approved :: BSD License Classifier: Programming Language ::
 Python :: 3 Classifier: Programming Language :: Python :: 3.8 Classifier:
 Programming Language :: Python :: 3.9 Classifier: Programming Language ::
 Python :: 3.10 Classifier: Programming Language :: Python :: 3.11 Classifier:
 Topic :: Scientific/Engineering Requires-Dist: astropy (>=5.1,<6.0) Requires-
 Dist: autoreject (>=0.3.1) Requires-Dist: certifi (>=2022.12.07) Requires-Dist:
 future (>=0.18.3) Requires-Dist: h5io (>=0.1.7,<0.2.0) Requires-Dist:
-matplotlib (>=3.2.1,<4.0.0) Requires-Dist: meshio (>=5.3.4,<6.0.0) Requires-
-Dist: mistune (>=2.0.4) Requires-Dist: mne (>=1.3,<2.0) Requires-Dist: numpy
-(>=1.18.3,<2.0.0) Requires-Dist: pandas (>=1.0.3,<2.0.0) Requires-Dist: scipy
-(>=1.4.1,<2.0.0) Requires-Dist: statsmodels (>=0.13.2,<0.14.0) Requires-Dist:
-tqdm (>=4.46.0,<5.0.0) Project-URL: Documentation, https://hypyp.readthedocs.io
+importlib-resources (>=6.0.0,<7.0.0) Requires-Dist: matplotlib (>=3.2.1,<4.0.0)
+Requires-Dist: meshio (>=5.3.4,<6.0.0) Requires-Dist: mistune (>=2.0.4)
+Requires-Dist: mne (>=1.3,<2.0) Requires-Dist: numpy (>=1.18.3,<2.0.0)
+Requires-Dist: pandas (>=1.0.3,<2.0.0) Requires-Dist: scipy (>=1.4.1,<2.0.0)
+Requires-Dist: statsmodels (>=0.13.2,<0.14.0) Requires-Dist: tqdm
+(>=4.46.0,<5.0.0) Project-URL: Documentation, https://hypyp.readthedocs.io
 Project-URL: Repository, https://github.com/ppsp-team/HyPyP Description-
 Content-Type: text/markdown # HyPyP ðã°ï¸ð The **Hy**perscanning
 **Py**thon **P**ipeline [![PyPI version shields.io](https://img.shields.io/
-pypi/v/hypyp.svg)](https://pypi.org/project/HyPyP/) [https://travis-ci.org/
-ppsp-team/HyPyP.svg?branch=master] [https://readthedocs.org/projects/hypyp/
-badge/?version=latest] [![license](https://img.shields.io/badge/License-
+pypi/v/hypyp.svg)](https://pypi.org/project/HyPyP/) [![CI](https://github.com/
+ppsp-team/HyPyP/actions/workflows/Build.yml/badge.svg)](https://github.com/
+ppsp-team/HyPyP/actions/workflows/Build.yml) [https://readthedocs.org/projects/
+hypyp/badge/?version=latest] [![license](https://img.shields.io/badge/License-
 BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause) [!
 [Mattermost](https://img.shields.io/discord/1065810348944408616?color=blue)]
 (https://discord.gg/zYzjeGj7D6) â ï¸ This software is in beta and thus should
 be considered with caution. While we have done our best to test all the
 functionalities, there is no guarantee that the pipeline is entirely bug-free.
 ð See our [paper](https://academic.oup.com/scan/advance-article/doi/10.1093/
 scan/nsaa141/5919711) for more explanation and our plan for upcoming
 functionalities (aka Roadmap). ð¤ If you want to help you can submit bugs and
 suggestions of enhancements in our Github [Issues section](https://github.com/
 ppsp-team/HyPyP/issues). ð¤ For the motivated contributors, you can even help
 directly in the developpment of HyPyP. You will need to install [Poetry](https:
 //python-poetry.org/) (see section below). ## Contributors Original authors:
 Florence BRUN, AnaÃ«l AYROLLES, Phoebe CHEN, Amir DJALOVSKI, Yann BEAUXIS,
 Suzanne DIKKER, Guillaume DUMAS New contributors: Ghazaleh RANJBARAN, Quentin
-MOREAU, Caitriona DOUGLAS, Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO ##
-Installation ``` pip install HyPyP ``` ## Documentation HyPyP documentation of
-all the API functions is available online at [hypyp.readthedocs.io](https://
-hypyp.readthedocs.io/) For getting started with HyPyP, we have designed a
-little walkthrough: [getting_started.ipynb](https://github.com/ppsp-team/HyPyP/
-blob/master/tutorial/getting_started.ipynb) ## Core API ð  [io.py](https://
-github.com/ppsp-team/HyPyP/blob/master/hypyp/io.py) â Loaders (Florence,
-AnaÃ«l, Ghazaleh, Franck, Jonas, Guillaume) ð§° [utils.py](https://github.com/
-ppsp-team/HyPyP/blob/master/hypyp/utils.py) â Basic tools (Amir, Florence,
-Guilaume) âï¸ [prep.py](https://github.com/ppsp-team/HyPyP/blob/master/
-hypyp/prep.py) â Preprocessing (ICA & AutoReject) (AnaÃ«l, Florence,
-Guillaume) ð  [analyses.py](https://github.com/ppsp-team/HyPyP/blob/master/
-hypyp/analyses.py) â Power spectral density and wide choice of connectivity
-measures (Phoebe, Suzanne, Florence, Ghazaleh, Juan, Guillaume) ð [stats.py]
-(https://github.com/ppsp-team/HyPyP/blob/master/hypyp/stats.py) â Statistics
-(permutations & cluster statistics) (Florence, Guillaume) ð§  [viz.py](https:/
-/github.com/ppsp-team/HyPyP/blob/master/hypyp/viz.py) â Inter-brain
-visualization (AnaÃ«l, Amir, Florence, Guillaume) ð [Tutorials](https://
-github.com/ppsp-team/HyPyP/tree/master/tutorial) - Examples & documentation
-(AnaÃ«l, Florence, Yann, Ghazaleh, Caitriona, Guillaume) ## Poetry installation
-(only for developpers and adventurous users) Step 1: ```pip install poetry```
-Step 2: ```git clone git@github.com:ppsp-team/HyPyP.git``` Step 3: ```cd
-HyPyP``` Step 4: ```poetry install``` Step 5: ```poetry shell``` You can now
-use ```jupyter notebook``` or ```ipython```! â ï¸ If you need to install a
-new dependency (not recommended), you have to use `poetry add
+MOREAU, Caitriona DOUGLAS, Franck PORTEOUS, Jonas MAGO, Juan C. AVENDANO, Julie
+BONNAIRE ## Installation ``` pip install HyPyP ``` ## Documentation HyPyP
+documentation of all the API functions is available online at
+[hypyp.readthedocs.io](https://hypyp.readthedocs.io/) For getting started with
+HyPyP, we have designed a little walkthrough: [getting_started.ipynb](https://
+github.com/ppsp-team/HyPyP/blob/master/tutorial/getting_started.ipynb) ## Core
+API ð  [io.py](https://github.com/ppsp-team/HyPyP/blob/master/hypyp/io.py)
+â Loaders (Florence, AnaÃ«l, Ghazaleh, Franck, Jonas, Guillaume) ð§°
+[utils.py](https://github.com/ppsp-team/HyPyP/blob/master/hypyp/utils.py) â
+Basic tools (Amir, Florence, Guilaume) âï¸ [prep.py](https://github.com/
+ppsp-team/HyPyP/blob/master/hypyp/prep.py) â Preprocessing (ICA & AutoReject)
+(AnaÃ«l, Florence, Guillaume) ð  [analyses.py](https://github.com/ppsp-team/
+HyPyP/blob/master/hypyp/analyses.py) â Power spectral density and wide choice
+of connectivity measures (Phoebe, Suzanne, Florence, Ghazaleh, Juan, Guillaume)
+ð [stats.py](https://github.com/ppsp-team/HyPyP/blob/master/hypyp/stats.py)
+â Statistics (permutations & cluster statistics) (Florence, Guillaume) ð§ 
+[viz.py](https://github.com/ppsp-team/HyPyP/blob/master/hypyp/viz.py) â
+Inter-brain visualization (AnaÃ«l, Amir, Florence, Guillaume) ð [Tutorials]
+(https://github.com/ppsp-team/HyPyP/tree/master/tutorial) - Examples &
+documentation (AnaÃ«l, Florence, Yann, Ghazaleh, Caitriona, Guillaume) ##
+Poetry installation (only for developpers and adventurous users) Step 1: ```pip
+install poetry``` Step 2: ```git clone git@github.com:ppsp-team/HyPyP.git```
+Step 3: ```cd HyPyP``` Step 4: ```poetry install``` Step 5: ```poetry shell```
+You can now use ```jupyter notebook``` or ```ipython```! â ï¸ If you need to
+install a new dependency (not recommended), you have to use `poetry add
 THE_NAME_OF_THE_LIBRARY` instead of your usual package manager.
```

