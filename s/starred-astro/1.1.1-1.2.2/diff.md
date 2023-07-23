# Comparing `tmp/starred-astro-1.1.1.tar.gz` & `tmp/starred-astro-1.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "starred-astro-1.1.1.tar", last modified: Fri May 26 15:54:24 2023, max compression
+gzip compressed data, was "starred-astro-1.2.2.tar", last modified: Sun Jul 23 09:02:40 2023, max compression
```

## Comparing `starred-astro-1.1.1.tar` & `starred-astro-1.2.2.tar`

### file list

```diff
@@ -1,37 +1,38 @@
-drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-05-26 15:54:24.583905 starred-astro-1.1.1/
--rw-r--r--   0 kevinmicha   (501) staff       (20)      860 2023-05-06 17:28:47.000000 starred-astro-1.1.1/AUTHORS.md
--rw-r--r--   0 kevinmicha   (501) staff       (20)    35143 2023-02-21 14:20:52.000000 starred-astro-1.1.1/LICENSE
--rw-r--r--   0 kevinmicha   (501) staff       (20)     4134 2023-05-26 15:54:24.583747 starred-astro-1.1.1/PKG-INFO
--rw-r--r--   0 kevinmicha   (501) staff       (20)     3282 2023-05-26 15:51:07.000000 starred-astro-1.1.1/README.md
--rw-r--r--   0 kevinmicha   (501) staff       (20)       38 2023-05-26 15:54:24.583956 starred-astro-1.1.1/setup.cfg
--rw-r--r--   0 kevinmicha   (501) staff       (20)     1065 2023-05-26 15:54:19.000000 starred-astro-1.1.1/setup.py
-drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-05-26 15:54:24.578306 starred-astro-1.1.1/starred/
--rw-r--r--   0 kevinmicha   (501) staff       (20)      352 2022-08-02 12:24:07.000000 starred-astro-1.1.1/starred/__init__.py
-drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-05-26 15:54:24.579479 starred-astro-1.1.1/starred/deconvolution/
--rw-r--r--   0 kevinmicha   (501) staff       (20)      112 2023-02-21 14:19:09.000000 starred-astro-1.1.1/starred/deconvolution/__init__.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)    21721 2023-05-01 15:42:17.000000 starred-astro-1.1.1/starred/deconvolution/deconvolution.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     8175 2023-05-22 14:05:49.000000 starred-astro-1.1.1/starred/deconvolution/loss.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     3907 2023-02-23 18:35:26.000000 starred-astro-1.1.1/starred/deconvolution/parameters.py
-drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-05-26 15:54:24.580259 starred-astro-1.1.1/starred/plots/
--rw-r--r--   0 kevinmicha   (501) staff       (20)       89 2023-02-24 15:47:18.000000 starred-astro-1.1.1/starred/plots/__init__.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     4793 2023-02-21 14:19:09.000000 starred-astro-1.1.1/starred/plots/f2n.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)    14377 2023-05-15 08:43:11.000000 starred-astro-1.1.1/starred/plots/plot_function.py
-drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-05-26 15:54:24.581239 starred-astro-1.1.1/starred/psf/
--rw-r--r--   0 kevinmicha   (501) staff       (20)      103 2022-08-02 12:51:20.000000 starred-astro-1.1.1/starred/psf/__init__.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     7811 2023-05-22 14:05:49.000000 starred-astro-1.1.1/starred/psf/loss.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     3993 2023-03-02 10:26:30.000000 starred-astro-1.1.1/starred/psf/parameters.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)    18769 2023-04-19 10:18:52.000000 starred-astro-1.1.1/starred/psf/psf.py
-drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-05-26 15:54:24.583077 starred-astro-1.1.1/starred/utils/
--rw-r--r--   0 kevinmicha   (501) staff       (20)      184 2023-02-24 15:47:08.000000 starred-astro-1.1.1/starred/utils/__init__.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     3147 2023-03-02 10:26:30.000000 starred-astro-1.1.1/starred/utils/ds9reg.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     8872 2023-04-19 10:18:52.000000 starred-astro-1.1.1/starred/utils/generic_utils.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     1762 2023-04-19 10:18:52.000000 starred-astro-1.1.1/starred/utils/inference_base.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     3963 2023-04-19 10:18:52.000000 starred-astro-1.1.1/starred/utils/jax_utils.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     6258 2023-04-19 10:18:52.000000 starred-astro-1.1.1/starred/utils/noise_utils.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)    10436 2023-05-15 08:43:11.000000 starred-astro-1.1.1/starred/utils/optimization.py
--rw-r--r--   0 kevinmicha   (501) staff       (20)     4549 2023-04-19 10:18:52.000000 starred-astro-1.1.1/starred/utils/parameters.py
-drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-05-26 15:54:24.583564 starred-astro-1.1.1/starred_astro.egg-info/
--rw-r--r--   0 kevinmicha   (501) staff       (20)     4134 2023-05-26 15:54:24.000000 starred-astro-1.1.1/starred_astro.egg-info/PKG-INFO
--rw-r--r--   0 kevinmicha   (501) staff       (20)      738 2023-05-26 15:54:24.000000 starred-astro-1.1.1/starred_astro.egg-info/SOURCES.txt
--rw-r--r--   0 kevinmicha   (501) staff       (20)        1 2023-05-26 15:54:24.000000 starred-astro-1.1.1/starred_astro.egg-info/dependency_links.txt
--rw-r--r--   0 kevinmicha   (501) staff       (20)        8 2023-05-26 15:54:24.000000 starred-astro-1.1.1/starred_astro.egg-info/top_level.txt
+drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-07-23 09:02:40.760350 starred-astro-1.2.2/
+-rw-r--r--   0 kevinmicha   (501) staff       (20)      860 2023-05-06 17:28:47.000000 starred-astro-1.2.2/AUTHORS.md
+-rw-r--r--   0 kevinmicha   (501) staff       (20)    35143 2023-02-21 14:20:52.000000 starred-astro-1.2.2/LICENSE
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     4693 2023-07-23 09:02:40.760202 starred-astro-1.2.2/PKG-INFO
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     4209 2023-07-23 08:40:47.000000 starred-astro-1.2.2/README.md
+-rw-r--r--   0 kevinmicha   (501) staff       (20)       38 2023-07-23 09:02:40.760395 starred-astro-1.2.2/setup.cfg
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     1116 2023-07-23 09:02:23.000000 starred-astro-1.2.2/setup.py
+drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-07-23 09:02:40.753055 starred-astro-1.2.2/starred/
+-rw-r--r--   0 kevinmicha   (501) staff       (20)      352 2022-08-02 12:24:07.000000 starred-astro-1.2.2/starred/__init__.py
+drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-07-23 09:02:40.754296 starred-astro-1.2.2/starred/deconvolution/
+-rw-r--r--   0 kevinmicha   (501) staff       (20)      112 2023-02-21 14:19:09.000000 starred-astro-1.2.2/starred/deconvolution/__init__.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)    23582 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/deconvolution/deconvolution.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)    11574 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/deconvolution/loss.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     3533 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/deconvolution/parameters.py
+drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-07-23 09:02:40.756382 starred-astro-1.2.2/starred/plots/
+-rw-r--r--   0 kevinmicha   (501) staff       (20)       89 2023-02-24 15:47:18.000000 starred-astro-1.2.2/starred/plots/__init__.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     4793 2023-02-21 14:19:09.000000 starred-astro-1.2.2/starred/plots/f2n.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)    19594 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/plots/plot_function.py
+drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-07-23 09:02:40.757189 starred-astro-1.2.2/starred/psf/
+-rw-r--r--   0 kevinmicha   (501) staff       (20)      103 2022-08-02 12:51:20.000000 starred-astro-1.2.2/starred/psf/__init__.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     8101 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/psf/loss.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     3671 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/psf/parameters.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)    20977 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/psf/psf.py
+drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-07-23 09:02:40.759498 starred-astro-1.2.2/starred/utils/
+-rw-r--r--   0 kevinmicha   (501) staff       (20)      184 2023-02-24 15:47:08.000000 starred-astro-1.2.2/starred/utils/__init__.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     3239 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/utils/ds9reg.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)    11352 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/utils/fitting_sequence.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)    10120 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/utils/generic_utils.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     5228 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/utils/inference_base.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     3963 2023-04-19 10:18:52.000000 starred-astro-1.2.2/starred/utils/jax_utils.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     6341 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/utils/noise_utils.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)    10890 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/utils/optimization.py
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     7669 2023-07-23 08:41:16.000000 starred-astro-1.2.2/starred/utils/parameters.py
+drwxr-xr-x   0 kevinmicha   (501) staff       (20)        0 2023-07-23 09:02:40.760041 starred-astro-1.2.2/starred_astro.egg-info/
+-rw-r--r--   0 kevinmicha   (501) staff       (20)     4693 2023-07-23 09:02:40.000000 starred-astro-1.2.2/starred_astro.egg-info/PKG-INFO
+-rw-r--r--   0 kevinmicha   (501) staff       (20)      772 2023-07-23 09:02:40.000000 starred-astro-1.2.2/starred_astro.egg-info/SOURCES.txt
+-rw-r--r--   0 kevinmicha   (501) staff       (20)        1 2023-07-23 09:02:40.000000 starred-astro-1.2.2/starred_astro.egg-info/dependency_links.txt
+-rw-r--r--   0 kevinmicha   (501) staff       (20)        8 2023-07-23 09:02:40.000000 starred-astro-1.2.2/starred_astro.egg-info/top_level.txt
```

### Comparing `starred-astro-1.1.1/AUTHORS.md` & `starred-astro-1.2.2/AUTHORS.md`

 * *Files identical despite different names*

### Comparing `starred-astro-1.1.1/LICENSE` & `starred-astro-1.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `starred-astro-1.1.1/README.md` & `starred-astro-1.2.2/README.md`

 * *Files 24% similar despite different names*

```diff
@@ -1,77 +1,90 @@
 # STARRED: STARlet REgularized Deconvolution 
 
 [![pipeline status](https://gitlab.com/cosmograil/starred/badges/main/pipeline.svg)](https://gitlab.com/cosmograil/starred/commits/main)
 [![coverage report](https://gitlab.com/cosmograil/starred/badges/main/coverage.svg)](https://cosmograil.gitlab.io/starred/coverage/)
 [![Python 3.8](https://img.shields.io/badge/python-3.8-blue.svg)](https://www.python.org/downloads/release/python-380/)
 [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
 [![DOI](https://joss.theoj.org/papers/10.21105/joss.05340/status.svg)](https://doi.org/10.21105/joss.05340)
-
+[![pypi](https://img.shields.io/pypi/v/starred-astro.svg)](https://cosmograil.gitlab.io/starred/)
 
 STARlet REgularized Deconvolution (STARRED) is a Python deconvolution method powered by Starlet regularization and JAX automatic differentiation. It uses a Point Spread Function (PSF) narrower than the original one as kernel. 
 
 ## Installation 
 
 ### Through PyPI
 
 STARRED releases are distributed through the Python Package Index (PyPI). To install the latest version use `pip`:
 
 ```bash
 $ pip install starred-astro
 ```
 
+### Through Anaconda
+We provide an Anaconda environment that satisfies all the dependencies in `starred-env.yml`. 
+```bash
+$ git clone https://gitlab.com/cosmograil/starred.git
+$ cd starred
+$ conda env create -f starred-env.yml
+$ conda activate starred-env
+$ pip install .
+```
+In case you have an NVIDIA GPU, this should automatically download the right version of JAX as well as cuDNN.
+Next, you can run the tests to make sure your installation is working correctly.
+
+```bash
+# While still in the STARRED directory:
+$ pytest . 
+```
+
+### Manually handling the dependencies
+If you want to use an existing environment, just omit the Anaconda commands above:
+```bash
+$ git clone https://gitlab.com/cosmograil/starred
+$ cd starred 
+$ pip install .
+```
+
+or if you need to install it for your user only: 
+```bash
+$ python setup.py install --user 
+```
+
 STARRED runs much faster on GPUs, so make sure you install a version of JAX that is compatible 
 with your version of CUDA and cuDNN: 
 ``` bash 
 $ pip install "jax[cuda11_cudnn86]" -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html
 ```
 
 ## Requirements 
 
-STARRED requires the following Python packages:
-
+STARRED requires the following Python packages: 
 * `astropy`
-
 * `dill`
-
 * `jax`
-
 * `jaxlib`
-
 * `jaxopt`
-
 * `matplotlib`
-
 * `numpy`
-
 * `scikit-image`
-
 * `scipy`
-
 * `optax`
-
 * `tqdm`
     
 
 
 ## Example Notebooks and Documentation
 The full documentation can be found [here](https://cosmograil.gitlab.io/starred/). 
 
 Example notebooks are located in the [notebooks](https://gitlab.com/cosmograil/starred/-/tree/main/notebooks) folder: 
-
 * [Ground-based narrow PSF generation](https://gitlab.com/cosmograil/starred/-/blob/main/notebooks/1_WFI%20narrow%20PSF%20generation.ipynb)
-
 * [Ground-based joint deconvolution](https://gitlab.com/cosmograil/starred/-/blob/main/notebooks/2_DESJ0602-4335%20joint%20deconvolution.ipynb)
-
 * [Another ground-based joint deconvolution](https://gitlab.com/cosmograil/starred/-/blob/main/notebooks/3_Another%20lensed%20quasar%20-%20joint%20deconvolution.ipynb)
-
 * [JWST PSF generation and deconvolution](https://gitlab.com/cosmograil/starred/-/blob/main/notebooks/4_JWST%20deconvolution.ipynb)
-
 * [DES2038 joint deconvolution](https://gitlab.com/cosmograil/starred/-/blob/main/notebooks/5_DES2038_from_WFI_joint_deconvolution.ipynb)
-
 * [HST PSF reconstruction](https://gitlab.com/cosmograil/starred/-/blob/main/notebooks/6_HST-PSF%20reconstruction.ipynb)
 
 ## Attribution
 
 If you use this code, please cite [Michalewicz et al. 2023](https://joss.theoj.org/papers/10.21105/joss.05340) as indicated in the [documentation](https://cosmograil.gitlab.io/starred/citing.html).
 
 ## License
```

### Comparing `starred-astro-1.1.1/setup.py` & `starred-astro-1.2.2/setup.py`

 * *Files 9% similar despite different names*

```diff
@@ -17,16 +17,17 @@
     import pypandoc
     long_description = pypandoc.convert_file('README.md', 'rst')
 except(IOError, ImportError):
     long_description = open('README.md').read()
 
 setup(
     name='starred-astro',
-    version='1.1.1',
+    version='1.2.2',
     author='Kevin Michalewicz',
     author_email='kevinmicha@hotmail.com',
     description='A two-channel deconvolution method with Starlet regularization',
     long_description=long_description,
+    long_description_content_type='text/markdown',
     packages=['starred', 'starred.deconvolution', 'starred.plots', 'starred.psf', 'starred.utils'],
     requires=['astropy', 'dill', 'galsim', 'jax', 'jaxlib', 'jaxopt', 'matplotlib', 'numpy', 'scikitimage', 'scipy', 'optax', 'tqdm'],
     cmdclass={'test': PyTest}
 )
```

### Comparing `starred-astro-1.1.1/starred/deconvolution/deconvolution.py` & `starred-astro-1.2.2/starred/deconvolution/deconvolution.py`

 * *Files 12% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 import numpy as np
 from jax import jit, vmap
 from jax.image import scale_and_translate
 import dill as pkl
 import os
 
 from starred.utils.generic_utils import pad_and_convolve_fft, \
-    pad_and_convolve, \
+    pad_and_convolve, scipy_convolve, \
     fwhm2sigma, gaussian_function, \
     make_grid, Downsample, save_fits, save_npy
 
 
 class Deconv(object):
     """
     Image deconvolution class. The order of the params below matters for unpacking re-packing dictionaries.
@@ -35,59 +35,76 @@
         :param upsampling_factor: the proportion by which the sampling rate increases with respect to the input image
         :type upsampling_factor: int
         :param epochs: for a joint deconvolution, the number of epochs considered. For single deconvolution, ``epochs`` is 1
         :type epochs: int
         :param psf: Point Spread Function array from ``starred.psf.psf``, acting as deconvolution kernel here
         :param gaussian_fwhm: the Gaussian's FWHM in pixels
         :type gaussian_fwhm: int
-        :param convolution_method: method to use to calculate the convolution
+        :param convolution_method: method to use to calculate the convolution : 'fft', 'scipy' (recommended), or 'lax'
         :type convolution_method: str
 
         """
         self.image_size = image_size
 
         # setter since vectorized functions used here depend on upsampling factor:
         self.setUpsamplingFactor(upsampling_factor)
 
         self.image_size_up = image_size * upsampling_factor
         self.epochs = epochs
         self.M = number_of_sources
         self.gaussian_fwhm = gaussian_fwhm
         # let's carry the coordinates of our working grid (the upscaled one):
         self.x, self.y = make_grid(numPix=self.image_size_up, deltapix=1.)
-        if convolution_method == 'fft':
-            self._convolve = pad_and_convolve_fft
-        elif convolution_method == 'lax':
-            self._convolve = pad_and_convolve
-        else:
-            raise NotImplementedError('Unknown convolution method: choose fft or lax')
-
-        if self.image_size_up % 2:
-            raise ValueError(
-                'With these settings the output will have odd dimensions. To obtain adequate results, at least one between the image size and the upsampling factor must be even.')
 
         if psf is None:
             raise TypeError('Please provide the narrow PSF.')
         else:
             if not len(psf.shape)==3:
                 raise RuntimeError('We expect your psf to have shape (epochs, nx, ny). Your psf does not have the right number of dimensions, with shape: {psf.shape}')
             psf = np.flip(psf, (1,2))
             n_epochs, nx, ny = psf.shape
             assert n_epochs == self.epochs, "Please provide one PSF for each epoch"
+
+            #for convolution_method = 'fft', image and kernel must have the same size
             if (nx != self.image_size_up or ny != self.image_size_up) and convolution_method == 'fft':
                 print('Padding the PSFs to match the upsampled image size...')
                 if (self.image_size_up - nx)%2 or (self.image_size_up - ny)%2:
                     raise RuntimeError('Upsampled image size and PSF size do not match. Please pad the PSF manually to match '
                                        'the size of the upsampled image. Make sure it is properly centered. '
-                                       'PSF kernels should have an even number of pixels')
+                                       'PSF kernels should have an even number of pixels if your are using convolution method "fft".')
                 else :
                     padx, pady = int((self.image_size_up - nx) / 2), int((self.image_size_up - ny) / 2)
                     psf = jnp.pad(psf, ((0, 0), (padx, padx), (pady, pady)), constant_values=0.)
 
             self.psf = psf.astype(np.float32)
+
+        if convolution_method == 'fft':
+            self._convolve = pad_and_convolve_fft
+            if nx % 2 == 0:
+                self.shift_gaussian = -0.5
+            else:
+                self.shift_gaussian = 0.
+            self.shift_direction = 1
+        elif convolution_method == 'lax':
+            self._convolve = pad_and_convolve
+            if nx % 2 == 0:
+                self.shift_gaussian = -0.5
+            else:
+                self.shift_gaussian = 0.
+            self.shift_direction = 1
+        elif convolution_method == 'scipy':
+            self._convolve = scipy_convolve
+            if nx%2 == 0 :
+                self.shift_gaussian = 0.5
+            else :
+                self.shift_gaussian = 0.
+            self.shift_direction = 1
+        else:
+            raise NotImplementedError('Unknown convolution method: choose fft, scipy (recommended) or lax')
+
         self.sigma = fwhm2sigma(self.gaussian_fwhm)
 
         self._model = self.modelstack if self.epochs > 5 else self.modelstack_forloop
         self.scale = scale
 
     # @partial(jit, static_argnums=(0,))
     def shifted_gaussians(self, c_x, c_y, a):
@@ -100,16 +117,16 @@
         :return: 2D array
 
         """
         return jnp.sum(jnp.array([gaussian_function(
             x=self.x, y=self.y,
             amp=a[i], sigma_x=self.sigma,
             sigma_y=self.sigma,
-            center_x=c_x[i],
-            center_y=c_y[i],
+            center_x=(self._upsampling_factor * c_x[i] - self.shift_gaussian)*self.shift_direction ,
+            center_y=(self._upsampling_factor * c_y[i] - self.shift_gaussian)*self.shift_direction
         ).reshape(self.image_size_up, self.image_size_up) for i in range(self.M)]), axis=0)
 
     @partial(jit, static_argnums=(0,))
     def translate_array(self, array, dx, dy):
         """
         Using first order interpolation, translates the array by (dx, dy) pixels.
         In the context of this problem, typically we will have dx ~ dy < 1.
@@ -122,15 +139,15 @@
         :return: 2D array - A translated version of the input array
 
         """
         return scale_and_translate(image=array,
                                    shape=array.shape,
                                    spatial_dims=(0, 1),
                                    scale=jnp.array((1., 1.)),
-                                   translation=jnp.array((dy, dx)),
+                                   translation=jnp.array((dy*self._upsampling_factor, dx*self._upsampling_factor)),
                                    method='bilinear')
 
     # @partial(jit, static_argnums=(0,))
     def one_epoch(self, psf, params):
         """
         Produces a 2D array corresponding to one epoch of the deconvolution.
 
@@ -162,15 +179,15 @@
         # initially, just the background:
         f = h.reshape((self.image_size_up, self.image_size_up))
 
         # add the point sources at the deconvoled resolution:
         f += self.scale * self.shifted_gaussians(c_x, c_y, a)
 
         # convolve with the psf to match the resolution of the observation:
-        f = self._convolve(f, psf, False).reshape(self.image_size_up,
+        f = self._convolve(f, psf).reshape(self.image_size_up,
                                                   self.image_size_up)
 
         # shift to compensate small translations between epochs:
         f = self.translate_array(f, dx, dy)
 
         # now we can also add the constant background:
         f += mean
@@ -310,18 +327,18 @@
         model = self.DownsampleAllEpochs(modelupscale)
 
         # to conserve the surface brightness:
         model = model * ((self.image_size_up ** 2) / (self.image_size ** 2))
 
         return model
 
-    def dump(self, path, kwargs):
+    def dump(self, path, kwargs, data=None, sigma_2=None):
         """Stores information in a given file."""
         with open(path, 'wb') as f:
-            pkl.dump([self, kwargs], f)
+            pkl.dump([self, kwargs, data, sigma_2], f, protocol=pkl.HIGHEST_PROTOCOL)
 
     def export(self, output_folder, kwargs_final, data, sigma_2, epoch=None, format='fits'):
         """
         Saves all the output files.
 
         :param output_folder: path to the output folder
         :type output_folder: str
@@ -354,85 +371,97 @@
             data_show = data[e, :, :]
             dif = data_show - output
             rr = np.abs(dif) / np.sqrt(sigma_2[e, :, :])
 
             if i == 0:
                 save_fct(h, os.path.join(output_folder, 'background'))
 
-            save_fct(data_show, os.path.join(output_folder, f'data_{i}'))
-            save_fct(output, os.path.join(output_folder, f'model_{i}'))
-            save_fct(dif, os.path.join(output_folder, f'residuals_{i}'))
-            save_fct(deconv, os.path.join(output_folder, f'deconvolution_{i}'))
-            save_fct(rr, os.path.join(output_folder, f'scaled_residuals_{i}'))
+            save_fct(data_show, os.path.join(output_folder, 'data_{0:05d}'.format(i)))
+            save_fct(output, os.path.join(output_folder, 'model_{0:05d}'.format(i)))
+            save_fct(dif, os.path.join(output_folder, 'residuals_{0:05d}'.format(i)))
+            save_fct(deconv, os.path.join(output_folder, 'deconvolution_{0:05d}'.format(i)))
+            save_fct(rr, os.path.join(output_folder, 'scaled_residuals_{0:05d}'.format(i)))
 
     def flux_at_epoch(self, kwargs, epoch=0):
         """
         Return an array containing the flux of the point sources at epoch `epoch`.
 
         :param kwargs_final: dictionary containing all keyword arguments
         :param epoch: index of the epoch
         """
         a = kwargs['kwargs_analytic']['a'][self.M * epoch:self.M * (epoch + 1)] * self.scale
 
         return a
 
-def setup_model(data, sigma_2, s, xs, ys, amps, subsampling_factor):
+def setup_model(data, sigma_2, s, xs, ys, subsampling_factor, initial_a=None, astrometric_bound = None, dithering_bound = None, convolution_method='scipy'):
     """
     Utility setting up a deconvolution model. The returned dictionaries of
     parameters can later be adjusted by the user. 
 
     :param data: 3D array containing the images, one per epoch. shape (epochs, im_size, im_size)
     :param sigma_2: 3D array containing the noisemaps, one per epoch. shape (epochs, im_size, im_size)
-    :param s: 3D array containing the the narrow PSFs, one per epoch. shape (epochs, im_size_up, im_size_up) where im_size_up needs be a multiple of im_size.
-    :param xs: 1D array or list containing the x positions of the point sources. For N point sources, len(xs) is N.
-    :param ys: 1D array or list containing the y positions of the point sources. For N point sources, len(ys) is N.
-    :param amps: list containing the amplitudes of the point sources. For N point sources, len(amps) is N. The same amplitudes will be applied to all epochs.
+    :param s: 3D array containing the narrow PSFs, one per epoch. shape (epochs, im_size_up, im_size_up) where im_size_up needs be a multiple of im_size.
+    :param xs: 1D array or list containing the x positions of the point sources. For M point sources, len(xs) is M. In unit of big pixel.
+    :param ys: 1D array or list containing the y positions of the point sources. For M point sources, len(ys) is M. In unit of big pixel.
+    :param initial_a: list containing the amplitudes of the point sources. For M point sources and N epochs, len(initial_a) is M*N. If none, amplitudes are applied scaled by the maax of each epoch.
     :param subsampling_factor: integer, ratio of the size of the data pixels to that of the PSF pixels.
+    :param astrometric_bound: integer, maximum shift of the point sources, relative to the initial position. None: no upper nor lower limit
+    :param dithering_bound: integer, maximum shift from image to image. None: no upper nor lower limit
+    :param convolution_method: 'scipy', 'fft', or 'lax'. To be passed to the Deconv class. Recommended : 'scipy'.
     :return: a tuple: (a starred.deconvolution.Deconv instance, 
                        a dictionary with the initial values of the model parameters,
                        a dictionary with the upper boundaries of the model parameters,
                        a dictionary with the lower boundaries of the model parameters,
                        a dictionary with the fixed parameters of the model)
     """
-
-    # amps MUST be a list, not a numpy array. (we're using epochs*amps to get
-    # amps for each epoch)
-    amps = [float(amp) for amp in amps]
-    # xs and ys, let's make them numpy arrays cuz it's easier 
+    # xs and ys, let's make them numpy arrays cuz it's easier
     xs = np.array(xs)
     ys = np.array(ys)
-    
-    if not len(amps) == xs.size == ys.size:
-        message = "Your amps, xs or ys (refering to amplitudes and positions of your point sources)"
+    M = xs.size # number of point sources
+    epochs = data.shape[0]
+
+    if initial_a is None:
+        initial_a = 6*np.array([data[i,:,:].max() for i in range(epochs) for j in range(M)])
+
+    if not xs.size == ys.size:
+        message = "Your xs or ys (refering to amplitudes and positions of your point sources)"
         message += " arguments need be the of the same length!\n"
-        message += f"But we have size(xs)={xs.size}, size(ys)={ys.size}, size(amps)={len(amps)}"
+        message += f"But we have size(xs)={xs.size}, size(ys)={ys.size}"
         raise RuntimeError(message)
-    
-    epochs = data.shape[0]
+
+    if not int(len(initial_a)/epochs) == xs.size:
+        message = "Your initial amplitudes does not match the number of point sources and epochs."
+        message += f" initial amplitudes must have length N_point_source * N_epochs = {M * epochs}.\n"
+        message += f"But we have size(initial_a)={len(initial_a)}"
+        raise RuntimeError(message)
+
     if not sigma_2.shape == data.shape:
         message = "The shape of your data and noisemaps is not what we expect."
         message += " They need be of shape ~ (epochs, some nx, some ny).\n"
         message += f"But we have shape(data)={data.shape}, shape(sigma_2)={sigma_2.shape}."
         raise RuntimeError(message)
         
     if not epochs == sigma_2.shape[0] == s.shape[0]:
         message = "The number of epochs in your data, noisemaps or PSFs do not match\n"
         message += f"We have shape(data)={data.shape}, shape(sigma_2)={sigma_2.shape}, shape(s)={s.shape}\n"
         message += "We expected the first dimension of each (# of epochs) to be the same."
         raise RuntimeError(message)
-    
+
     im_size = data[0].shape[0]
     im_size_up = im_size * subsampling_factor
+    if astrometric_bound is None:
+        astrometric_bound = im_size/2.
+    if dithering_bound is None:
+        dithering_bound = im_size/2.
+
     
     # Parameter initialization
-    M = xs.size # number of point sources
-    initial_c_x = xs * subsampling_factor 
-    initial_c_y = ys * subsampling_factor 
+    initial_c_x = xs
+    initial_c_y = ys
     # intensity per point:
-    initial_a = np.array(epochs*amps)
     scale = data.max()
     initial_a /= scale
     # initial background:
     initial_h = np.zeros((im_size_up**2))
     # dictionary containing the parameters of deconvolution.
     # (The translations dx, dy are set to zero for the first epoch.
     # Thus we only initialize (epochs-1) of them.)
@@ -449,38 +478,38 @@
     # same as above, providing fixed parameters:
     kwargs_fixed = {
         'kwargs_analytic': {},
         'kwargs_background': {},
     }
     # boundaries.
     kwargs_up = {
-        'kwargs_analytic': {'c_x': list(initial_c_x+3),
-                            'c_y': list(initial_c_y+3),
-                            'dx' : [3. for _ in range(epochs-1)],
-                            'dy' : [3. for _ in range(epochs-1)],
+        'kwargs_analytic': {'c_x': list(initial_c_x+astrometric_bound),
+                            'c_y': list(initial_c_y+astrometric_bound),
+                            'dx' : [dithering_bound for _ in range(epochs-1)],
+                            'dy' : [dithering_bound for _ in range(epochs-1)],
                              'a': list([np.inf for i in range(M*epochs)]) 
                            },
         'kwargs_background': {'h': list([np.inf for i in range(0, im_size_up**2)]),
                               'mean': [np.inf for _ in range(epochs)]
                                },
     }
     kwargs_down = {
-        'kwargs_analytic': {'c_x': list(initial_c_x-3),
-                            'c_y': list(initial_c_y-3),
-                            'dx' : [-3. for _ in range(epochs-1)],
-                            'dy' : [-3. for _ in range(epochs-1)],
+        'kwargs_analytic': {'c_x': list(initial_c_x-astrometric_bound),
+                            'c_y': list(initial_c_y-astrometric_bound),
+                            'dx' : [-dithering_bound for _ in range(epochs-1)],
+                            'dy' : [-dithering_bound for _ in range(epochs-1)],
                              'a': list([0 for i in range(M*epochs)]) },
         'kwargs_background': {'h': list([-np.inf for i in range(0, im_size_up**2)]),
                               'mean': [-np.inf for _ in range(epochs)]
                                },
     }
     # Initializing the model
     model = Deconv(image_size=im_size, 
                    number_of_sources=M, 
                    scale=scale, 
                    upsampling_factor=subsampling_factor, 
                    epochs=epochs, 
                    psf=s, 
-                   convolution_method='fft')
+                   convolution_method=convolution_method)
 
     # returning model and kwargs.    
     return model, kwargs_init, kwargs_up, kwargs_down, kwargs_fixed
```

### Comparing `starred-astro-1.1.1/starred/deconvolution/loss.py` & `starred-astro-1.2.2/starred/psf/loss.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,163 +1,172 @@
 import warnings
 from functools import partial
 
 import jax.numpy as jnp
 import numpy as np
 from jax import jit
-from utils.jax_utils import decompose, scale_norms
+from starred.utils.jax_utils import decompose, scale_norms
 
 
 class Loss(object):
     """
     Class that manages the (auto-differentiable) loss function, defined as:
-    L = - log(likelihood) - log(regularization) - log(positivity)
+    L = - log(likelihood) - log(regularization)
 
     Note that gradient, hessian, etc. are computed in the ``InferenceBase`` class.
 
     """
 
-    _supported_ll = ('l2_norm')
-    _supported_regul_source = ('l1_starlet')
-
-    def __init__(self, data, deconv_class, param_class, sigma_2,
-                 regularization_terms=None, regularization_strength_scales=None, regularization_strength_hf=None,
-                 regularization_strength_positivity=0., regularization_strength_positivity_ps=0., W=None,
-                 regularize_full_model = False):
+    def __init__(self, data, psf_class, param_class, sigma_2, N, masks=None,
+                 regularization_terms='l1_starlet', regularization_strength_scales=0, regularization_strength_hf=0,
+                 regularization_strength_positivity=0, regularize_full_psf=True, a_norm=1,
+                 W=None):
         """
         :param data: array containing the observations
-        :param deconv_class: deconvolution class from ``starred.deconvolution.deconvolution``
-        :param param_class: parameters class from ``starred.deconvolution.parameters``
+        :param psf_class: Point Spread Function (PSF) class from ``starred.psf.psf``
+        :param param_class: parameters class from ``starred.psf.parameters``
         :param sigma_2: array containing the square of the noise maps
         :param N: number of observations stamps
         :type N: int
+        :param masks: array containing the masks for the PSF (if given)
         :param regularization_terms: information about the regularization terms
         :type regularization_terms: str
-        :param regularization_strength_scales: Lagrange parameter that weights intermediate scales in the transformed domain 
+        :param regularization_strength_scales: Lagrange parameter that weights intermediate scales in the transformed domain
         :type regularization_strength_scales: float
         :param regularization_strength_hf: Lagrange parameter weighting the highest frequency scale
         :type regularization_strength_hf: float
-        :param regularization_strength_positivity: Lagrange parameter weighting the positivity of the background. 0 means no positivity constrain.
-        :type regularization_strength_positivity: float
-        :param regularization_strength_positivity_ps: Lagrange parameter weighting the positivity of the point sources. 0 means no positivity constrain.
+        :param regularization_strength_positivity: Lagrange parameter weighting the positivity of the median of the background. 0 means no positivity constrain.
         :type regularization_strength_positivity: float
+        :param regularize_full_psf: True if you want to regularize the Moffat and the background (recommanded). False regularizes only the background
+        :type regularize_full_psf: bool
         :param W: weight matrix. Shape (n_scale, n_pix*subsampling_factor, n_pix*subsampling_factor)
 
         """
         self._data = data
+        self._psf = psf_class
+        self._param = param_class
+        self.N = N
         self._sigma_2 = sigma_2
         self.W = W
-        self._deconv = deconv_class
-        self._datar = self._data.reshape(self._deconv.epochs,
-                                         self._deconv.image_size,
-                                         self._deconv.image_size)
-        self._sigma_2r = self._sigma_2.reshape(self._deconv.epochs,
-                                               self._deconv.image_size,
-                                               self._deconv.image_size)
+        self.a_norm = a_norm
+        self.regularize_full_psf = regularize_full_psf
+        self._masks = masks
 
-        self._param = param_class
-        self.epochs = self._deconv.epochs
-        self.regularize_full_model = regularize_full_model
         self._init_likelihood()
         self._init_regularizations(regularization_terms, regularization_strength_scales, regularization_strength_hf,
-                                   regularization_strength_positivity, regularization_strength_positivity_ps)
+                                   regularization_strength_positivity)
+
+        self._penalty = 1e10
 
-    # @partial(jit, static_argnums=(0,))
     def __call__(self, args):
         return self.loss(args)
 
+    # @partial(jit, static_argnums=(0,))
     def loss(self, args):
-        """Defined as the negative log(likelihood*regularization)."""
+        """Defined as the negative log(likelihood*regularization)"""
         kwargs = self._param.args2kwargs(args)
-        neg_log = - (self._log_likelihood(kwargs) + self._log_regul(kwargs) + self._log_regul_positivity(kwargs) + self._log_regul_positivity_ps(kwargs))
+        neg_log = - self._log_likelihood(kwargs)
+        if self._st_src_lambda != 0 or self._st_src_lambda_hf !=0 :
+            neg_log -= self._log_regul(kwargs)
+        if self._pos_lambda !=0:
+            neg_log -= self._log_regul_positivity(kwargs)
+
         return jnp.nan_to_num(neg_log, nan=1e15, posinf=1e15, neginf=1e15)
+     
+    def update_dataset(self, newdata, newsigma2, newW, newparam_class):
+        """Updates the dataset."""
+        self._update_data(newdata, newsigma2)
+        self._update_parameters(newparam_class)
+        if newW is not None:
+            self._update_weights(newW)
+    
+    def _update_parameters(self, param_class):
+        """Updates the parameters."""
+        self._param = param_class
+        
+    def _update_data(self, newdata, newsigma2):
+        """Updates the data."""
+        self._data = newdata
+        self._sigma_2 = newsigma2
+
+    def _update_weights(self, W):
+        """Updates the weight matrix W."""
+        self._st_src_norms = W[:-1]
+        self.W = W
 
     @property
-    def datar(self):
+    def data(self):
         """Returns the observations array."""
-        return self._datar.astype(dtype=np.float32)
+        return self._data.astype(dtype=np.float32)
 
     @property
-    def sigma_2r(self):
+    def sigma_2(self):
         """Returns the noise map array."""
-        return self._sigma_2r.astype(dtype=np.float32)
+        return self._sigma_2.astype(dtype=np.float32)
+
+    @property
+    def masks(self):
+        """Returns the masks array."""
+        if self._masks is None:
+            self._masks = np.ones((self.N, self.data.shape[1], self.data.shape[2]))
+        return self._masks.astype(dtype=np.float32)
 
     def _init_likelihood(self):
         """Intialization of the data fidelity term of the loss function."""
         self._log_likelihood = self._log_likelihood_chi2
 
     def _init_regularizations(self, regularization_terms, regularization_strength_scales, regularization_strength_hf,
-                              regularization_strength_positivity, regularization_strength_positivity_ps):
+                              regularization_strength_positivity):
         """Intialization of the regularization terms of the loss function."""
         regul_func_list = []
         # add the log-regularization function to the list
         regul_func_list.append(getattr(self, '_log_regul_' + regularization_terms))
 
         if regularization_terms == 'l1_starlet':
-            n_pix_src = min(*self.datar[0, :, :].shape) * self._deconv._upsampling_factor
+            n_pix_src = min(*self.data[0, :, :].shape) * self._psf.upsampling_factor
             self.n_scales = int(np.log2(n_pix_src))  # maximum allowed number of scales
             if self.W is None:  # old fashion way
                 if regularization_strength_scales != 0 and regularization_strength_hf != 0:
                     warnings.warn('lambda is not normalized. Provide the weight map !')
                 wavelet_norms = scale_norms(self.n_scales)[:-1]  # ignore coarsest scale
-                self._st_src_norms = jnp.expand_dims(wavelet_norms, (1, 2)) * jnp.ones((n_pix_src, n_pix_src))
+                self._st_src_norms = jnp.expand_dims(wavelet_norms, (1, 2)) * jnp.ones(
+                    (n_pix_src, n_pix_src)) * self.a_norm
             else:
-                self._st_src_norms = self.W[:-1]  # ignore the coarsest scale
+                self._st_src_norms = self.W[:-1] * self.a_norm  # ignore the coarsest scale
             self._st_src_lambda = float(regularization_strength_scales)
             self._st_src_lambda_hf = float(regularization_strength_hf)
+        else:
+            raise NotImplementedError(f'Regularisation term {regularization_terms} not implemented yet. Please use "l1_starlet". ')
 
         # positivity term
         self._pos_lambda = float(regularization_strength_positivity)
-        self._pos_lambda_ps = float(regularization_strength_positivity_ps)
         # build the composite function (sum of regularization terms)
         self._log_regul = lambda kw: sum([func(kw) for func in regul_func_list])
 
     # @partial(jit, static_argnums=(0,))
     def _log_likelihood_chi2(self, kwargs):
-        """Computes the data fidelity term of the loss function using the L2 norm."""
-        model = self._deconv.model(kwargs)
-        return - 0.5 * (1. / self.epochs) * jnp.sum((model - self.datar) ** 2 / self.sigma_2r)
-
-        # return - 0.5 * jnp.sum(jnp.array([jnp.sum(jnp.subtract(self.data[i,:,:], self._deconv.model(i, **kwargs)[0])**2 / self.sigma_2[i,:,:]) for i in range(self.epochs)]))
+        """Computes the data fidelity term of the loss function using chi2."""
+        likelihood = - 0.5 * (1. / self.N) * jnp.sum(jnp.array([jnp.sum(
+            jnp.multiply(self.masks[i, :, :], jnp.subtract(self.data[i, :, :], self._psf.model(i, **kwargs))) ** 2
+            / self.sigma_2[i, :, :]) for i in range(self.N)]))
+        return likelihood
 
     # @partial(jit, static_argnums=(0,))
     def _log_regul_l1_starlet(self, kwargs):
-        """
-        Computes the regularization terms as the sum of:
-        
-        - the L1 norm of the Starlet transform of the highest frequency scale, and
-        - the L1 norm of the Starlet transform of all remaining scales (except the coarsest).
-        """
-        if self.regularize_full_model:
-            toreg, _ = self._deconv.getDeconvolved(kwargs, epoch=0)
-        else :
-            toreg = kwargs['kwargs_background']['h'].reshape(self._deconv.image_size_up, self._deconv.image_size_up)
-        st = decompose(toreg, self.n_scales)[:-1]  # ignore coarsest scale
+        """Computes the regularization terms as the sum of:
+        the L1 norm of the Starlet transform of the highest frequency scale, and
+        the L1 norm of the Starlet transform of all remaining scales (except the coarsest)."""
+        if self.regularize_full_psf:
+            h = self._psf.get_narrow_psf(**kwargs, norm=False)
+        else:
+            h = self._psf.get_background(kwargs['kwargs_background'])
+        st = decompose(h, self.n_scales)[:-1]  # ignore the coarsest scale, which is a constant
         st_weighted_l1_hf = jnp.sum(self._st_src_norms[0] * jnp.abs(st[0]))  # first scale (i.e. high frequencies)
-        st_weighted_l1 = jnp.sum(self._st_src_norms[1:] * jnp.abs(st[1:]))  # other scales
-        tot_l1_reg = - (self._st_src_lambda_hf * st_weighted_l1_hf + self._st_src_lambda * st_weighted_l1)
-        return tot_l1_reg / self._deconv._upsampling_factor**2
+        st_weighted_l1 = jnp.sum(
+            self._st_src_norms[1:] * jnp.abs(st[1:]))  # other scales, we ignore the coarsest scale in W as well
+        l1_tot_regul = - (self._st_src_lambda_hf * st_weighted_l1_hf + self._st_src_lambda * st_weighted_l1)
+        return l1_tot_regul / self._psf.upsampling_factor**2
 
     def _log_regul_positivity(self, kwargs):
-        """
-        Computes the posivity constraint term. A penalty is applied if the epoch with the smallest background mean has negative pixels.
-
-        :param kwargs:
-        """
-        h = jnp.array(kwargs['kwargs_background']['h'])
-        sum_pos = -jnp.where(h < 0., h, 0.).sum()
-        return - self._pos_lambda * sum_pos
-
-    def _log_regul_positivity_ps(self, kwargs):
-        """
-        Computes the posivity constraint term for the point sources. A penalty is applied if one of the point sources have negative amplitude.
-
-        :param kwargs:
-        """
-        fluxes = jnp.array(kwargs['kwargs_analytic']['a'])
-        min_amp = jnp.min(fluxes, initial=0.)
-        return - self._pos_lambda * jnp.abs(jnp.minimum(0., min_amp))
-
-    def update_weights(self, W):
-        """Updates the weight matrix W."""
-        self._st_src_norms = W[:-1]
-        self.W = W
+        med = jnp.median(kwargs['kwargs_background']['background'])
+        return - self._pos_lambda * jnp.abs(
+            jnp.minimum(0., med))  # penalise likelihood if the median of the background is less than 0
```

### Comparing `starred-astro-1.1.1/starred/deconvolution/parameters.py` & `starred-astro-1.2.2/starred/psf/parameters.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,89 +1,88 @@
 import jax.numpy as jnp
 import numpy as np
 
 from starred.utils.parameters import Parameters
 
-__all__ = ['ParametersDeconv']
+__all__ = ['ParametersPSF']
 
 
-class ParametersDeconv(Parameters):
+class ParametersPSF(Parameters):
     """
-    Deconvolution parameters class.
+    Point Spread Function parameters class.
 
     """
 
     def __init__(self, image_class, kwargs_init, kwargs_fixed, kwargs_up=None, kwargs_down=None):
         """
-        :param image_class: image/deconvolution class from ``starred.deconvolution.deconvolution``
+        :param image_class: image/PSF class from ``starred.psf.psf``
         :param kwargs_init: dictionary with information on the initial values of the parameters 
         :param kwargs_fixed: dictionary containing the fixed parameters 
         :param kwargs_up: dictionary with information on the upper bounds of the parameters 
         :param kwargs_down: dictionary with information on the lower bounds of the parameters 
 
         """
-        super(ParametersDeconv, self).__init__(image_class, kwargs_init, kwargs_fixed, kwargs_up=kwargs_up,
-                                               kwargs_down=kwargs_down)
+        super(ParametersPSF, self).__init__(image_class, kwargs_init, kwargs_fixed, kwargs_up=kwargs_up,
+                                            kwargs_down=kwargs_down)
 
     def args2kwargs(self, args):
         """Obtain a dictionary of keyword arguments from positional arguments."""
         i = 0
-        kwargs_analytic, i = self._get_params(args, i, 'kwargs_analytic')
+        kwargs_moffat, i = self._get_params(args, i, 'kwargs_moffat')
+        kwargs_gaussian, i = self._get_params(args, i, 'kwargs_gaussian')
         kwargs_background, i = self._get_params(args, i, 'kwargs_background')
         # wrap-up
-        kwargs = {'kwargs_analytic': kwargs_analytic, 'kwargs_background': kwargs_background}
+        kwargs = {'kwargs_moffat': kwargs_moffat, 'kwargs_gaussian': kwargs_gaussian,
+                  'kwargs_background': kwargs_background}
+
         return kwargs
 
     def kwargs2args(self, kwargs):
         """Obtain an array of positional arguments from a dictionary of keyword arguments."""
-        args = self._set_params(kwargs, 'kwargs_analytic')
+        args = self._set_params(kwargs, 'kwargs_moffat')
+        args += self._set_params(kwargs, 'kwargs_gaussian')
         args += self._set_params(kwargs, 'kwargs_background')
         return jnp.array(args)
 
     def get_param_names_for_model(self, kwargs_key):
         """Returns the names of the parameters according to the key provided."""
-        if kwargs_key == 'kwargs_analytic':
-            return self._image.param_names_analytic
-        return self._image.param_names_background
+        if kwargs_key == 'kwargs_moffat':
+            return self._image.param_names_moffat
+        elif kwargs_key == 'kwargs_gaussian':
+            return self._image.param_names_gaussian
+        elif kwargs_key == 'kwargs_background':
+            return self._image.param_names_background
+        else:
+            raise KeyError('Key %s is not in the kwargs')
 
     def _get_params(self, args, i, kwargs_key):
         """Getting the parameters."""
         kwargs = {}
         kwargs_fixed_k = self._kwargs_fixed[kwargs_key]
         param_names = self.get_param_names_for_model(kwargs_key)
         for name in param_names:
-            if not name in kwargs_fixed_k:
-                if name == 'a':
-                    num_param = self._image.M * self._image.epochs
-                elif name == 'h':
+            if not name in kwargs_fixed_k.keys():
+                if name == 'background':
                     num_param = self._image.image_size_up ** 2
-                elif name == 'mean':
-                    num_param = self._image.epochs
-                elif name == 'dx' or name == 'dy':
-                    num_param = self._image.epochs - 1
-                elif name == 'c_x' or name == 'c_y':
+                elif name == 'a':
+                    num_param = self._image.M
+                elif name == 'x0' or name == 'y0':
                     num_param = self._image.M
                 else:
-                    raise NameError(f"The ParametersDeconv class does not know about this parameter: {name}.")
+                    num_param = 1
                 kwargs[name] = args[i:i + num_param]
                 i += num_param
             else:
                 kwargs[name] = kwargs_fixed_k[name]
+                free_ind = self._kwargs_free_indices[kwargs_key][name]
+                if len(free_ind) >0:
+                    num_param = len(free_ind)
+                    kwargs[name] = kwargs[name].at[free_ind].set(args[i:i+ num_param])
+                    i+=num_param
+
         return kwargs, i
 
-    def _set_params(self, kwargs, kwargs_key):
-        """Setting the parameters."""
-        args = []
-        kwargs_profile = kwargs[kwargs_key]
-        kwargs_fixed_k = self._kwargs_fixed[kwargs_key]
-        param_names = self.get_param_names_for_model(kwargs_key)
-        for name in param_names:
-            if not name in kwargs_fixed_k and name != 'lambda':
-                if isinstance(kwargs_profile[name], list):
-                    args += kwargs_profile[name]
-                elif isinstance(kwargs_profile[name], (np.ndarray, np.generic)):
-                    args += kwargs_profile[name].tolist()
-                elif isinstance(kwargs_profile[name], (jnp.ndarray, jnp.generic)):
-                    args += kwargs_profile[name].tolist()
-                else:
-                    args += [kwargs_profile[name]]
+    def get_all_free_param_names(self, kwargs):
+        args = self._param_names(kwargs, 'kwargs_moffat')
+        args += self._param_names(kwargs, 'kwargs_gaussian')
+        args += self._param_names(kwargs, 'kwargs_background')
         return args
```

### Comparing `starred-astro-1.1.1/starred/plots/f2n.py` & `starred-astro-1.2.2/starred/plots/f2n.py`

 * *Files identical despite different names*

### Comparing `starred-astro-1.1.1/starred/plots/plot_function.py` & `starred-astro-1.2.2/starred/plots/plot_function.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+import os
+
 import matplotlib.pyplot as plt
 import numpy as np
 from matplotlib import colors
 from matplotlib.widgets import Slider
 
 from starred.utils.generic_utils import Downsample
 
@@ -15,15 +17,15 @@
     :param sigma_2: array containing the square of the noise maps
     :param kwargs: dictionary containing the parameters of the model
     :param n_psf: selected PSF index
     :type n_psf: int
     :param figsize: tuple that indicates the size of the figure
     :param units: units in which the pixel values are expressed
     :type units: str
-    :param upsampling_factor: the rate at which the sampling frequency increases in the PSF with respect to the input images
+    :param upsampling_factor: Provide the upsampling factor to degrade the model to the image resolution. Leave to 'None' to show the higher resolution model.
     :type upsampling_factor: int
 
     :return: output figure
 
     """
     if units is not None:
         str_unit = '[' + units + ']'
@@ -80,22 +82,23 @@
         ax.get_yaxis().set_visible(False)
 
     plt.tight_layout()
 
     return fig
 
 
-def multiple_PSF_plot(model, data, sigma_2, kwargs, figsize=None, units=None):
+def multiple_PSF_plot(model, data, sigma_2, kwargs, masks=None, figsize=None, units=None):
     """
     Plots the narrow PSF fit for all observations.
 
     :param model: array containing the model
     :param data: array containing the observations
     :param sigma_2: array containing the square of the noise maps
     :param kwargs: dictionary containing the parameters of the model
+    :param masks:  array containing the masks
     :param figsize: tuple that indicates the size of the figure
     :param units: units in which the pixel values are expressed
     :type units: str
 
     :return: output figure
     """
     if units is not None:
@@ -113,34 +116,42 @@
     fraction = 0.046
     pad = 0.04
     font_size = 14
     plt.rc('font', size=12)
     fmt_PSF = '%.0e'
     fmt_residuals = '%2.f'
 
+    if masks is not None:
+        alphas = masks
+        ind = np.where(masks == 0)
+        alphas[ind] = 0.01
+        kargs = [{'alpha':alphas[i,:,:]} for i in range(model.M)]
+    else:
+        kargs = [{} for i in range(model.M)]
+
     for i in range(model.M):
         estimated_full_psf = model.model(i, **kwargs)
         axs[0, i].set_title('PSF model %i %s' % (i + 1, str_unit), fontsize=font_size)
         axs[0, i].tick_params(axis='both', which='major', labelsize=10)
         axs[1, i].set_title('Relative residuals %i' % (i + 1), fontsize=font_size)
         axs[1, i].tick_params(axis='both', which='major', labelsize=10)
 
         fig.colorbar(axs[0, i].imshow(estimated_full_psf, norm=colors.SymLogNorm(linthresh=100), origin='lower'),
                      ax=axs[0, i], fraction=fraction, pad=pad, format=fmt_PSF)
         fig.colorbar(axs[1, i].imshow((data[i, :, :] - estimated_full_psf) / np.sqrt(sigma_2[i, :, :]),
-                                      origin='lower'), ax=axs[1, i], fraction=fraction, pad=pad, format=fmt_residuals)
+                                      origin='lower', **kargs[i]), ax=axs[1, i], fraction=fraction, pad=pad, format=fmt_residuals)
 
     for ax in np.array(axs).flatten():
         ax.get_xaxis().set_visible(False)
         ax.get_yaxis().set_visible(False)
 
     return fig
 
 
-def display_data(data, sigma_2=None, figsize=None, units=None, center=None):
+def display_data(data, sigma_2=None, masks=None, figsize=None, units=None, center=None):
     """
     Plots the observations and the noise maps.
 
     :param data: array containing the observations
     :param sigma_2: array containing the square of the noise maps
     :param figsize: tuple that indicates the size of the figure
     :param units: units in which the pixel values are expressed
@@ -174,33 +185,41 @@
         axs = [axs]
     elif n_image == 1:
         axs = np.asarray([axs]).T
     fraction = 0.046
     pad = 0.04
     fontsize = 12
 
+    if masks is not None:
+        alphas = masks
+        ind = np.where(masks == 0)
+        alphas[ind] = 0.9
+        kargs = [{'alpha':alphas[i,:,:]} for i in range(n_image)]
+    else:
+        kargs = [{} for i in range(n_image)]
+
     for i in range(n_image):
         plt.rc('font', size=12)
         axs[0][i].set_title('Data %i %s' % (i + 1, str_unit), fontsize=fontsize)
         axs[0][i].tick_params(axis='both', which='major', labelsize=10)
 
         if show_sigma:
             axs[1][i].set_title('Noise map %i %s' % (i + 1, str_unit), fontsize=fontsize)
             axs[1][i].tick_params(axis='both', which='major', labelsize=10)
 
-        fig.colorbar(axs[0][i].imshow(data[i, :, :], norm=colors.SymLogNorm(linthresh=10), origin='lower'),
+        fig.colorbar(axs[0][i].imshow(data[i, :, :], norm=colors.SymLogNorm(linthresh=10), origin='lower',  **kargs[i]),
                      ax=axs[0][i],
                      fraction=fraction, pad=pad, format='%.0e')
         if center is not None:
             c_x, c_y = center[0], center[1]
             axs[0][i].scatter(nx/2. + c_x[i], ny/2. + c_y[i], marker='x', c='r')
 
         if show_sigma:
             fig.colorbar(
-                axs[1][i].imshow(np.sqrt(sigma_2[i, :, :]), norm=colors.SymLogNorm(linthresh=10), origin='lower'),
+                axs[1][i].imshow(np.sqrt(sigma_2[i, :, :]), norm=colors.SymLogNorm(linthresh=10), origin='lower', **kargs[i]),
                 ax=axs[1][i],
                 fraction=fraction, pad=pad, format='%2.f')
 
     for ax in axs.flatten():
         ax.get_xaxis().set_visible(False)
         ax.get_yaxis().set_visible(False)
     plt.tight_layout()
@@ -287,74 +306,75 @@
     fig.colorbar(axs[0, 2].imshow(rr, origin='lower', **k_dict[2]), ax=axs[0, 2], fraction=fraction, pad=pad)
     fig.colorbar(axs[1, 0].imshow(h, norm=colors.SymLogNorm(**k_dict[3]), origin='lower'), ax=axs[1, 0], fraction=fraction,pad=pad)
     fig.colorbar(axs[1, 1].imshow(deconv, norm=colors.SymLogNorm(**k_dict[4]), origin='lower'), ax=axs[1, 1],fraction=fraction, pad=pad)
     fig.colorbar(axs[1, 2].imshow(s[epoch, :, :], norm=colors.SymLogNorm(**k_dict[5]), origin='lower'), ax=axs[1, 2],fraction=fraction, pad=pad)
 
     return fig
 
-
 def view_deconv_model(model, kwargs, data, sigma_2, figsize=(9,7.5)):
     output = model.model(kwargs)
     psf = model.psf
-    noisemap = sigma_2**0.5
+    noisemap = sigma_2 ** 0.5
+
     # setup for first epoch
     deconvs = [model.getDeconvolved(kwargs, i) for i in range(len(output))]
     deconv, h = deconvs[0]
     s = psf[0]
-    
+
     ##########################################################################
     # figure
-    fig, axs = plt.subplots(2, 3, figsize=figsize)  
+    fig, axs = plt.subplots(2, 3, figsize=figsize)
     for ax in axs.flatten():
         ax.set_xticks([])
         ax.set_yticks([])
-        
-    datap = axs[0,0].imshow(data[0], origin='lower')
-    axs[0,0].set_title('data')
-    
-    modelp = axs[0,1].imshow(output[0], origin='lower')
-    axs[0,1].set_title('model')
-    
-    diffp = axs[1,0].imshow((data[0] - output[0])/noisemap[0], origin='lower')
-    axs[1,0].set_title('(data-model)/noise')
-    
-    backp = axs[1,1].imshow(h, origin='lower')
-    axs[1,1].set_title('background')
-    
-    decp = axs[0,2].imshow(deconv, origin='lower')
-    axs[0,2].set_title('deconvolved')
-    
-    psfp = axs[1,2].imshow(s, origin='lower')
-    axs[1,2].set_title('narrow psf')
-    
+
+    datap = axs[0, 0].imshow(data[0], origin='lower')
+    axs[0, 0].set_title('data')
+
+    modelp = axs[0, 1].imshow(output[0], origin='lower')
+    axs[0, 1].set_title('model')
+
+    diffp = axs[1, 0].imshow((data[0] - output[0]) / noisemap[0], origin='lower')
+    axs[1, 0].set_title('(data-model)/noise')
+
+    backp = axs[1, 1].imshow(h, origin='lower')
+    axs[1, 1].set_title('background')
+
+    decp = axs[0, 2].imshow(deconv, origin='lower')
+    axs[0, 2].set_title('deconvolved')
+
+    psfp = axs[1, 2].imshow(s, origin='lower')
+    axs[1, 2].set_title('narrow psf')
+
     plt.tight_layout()
+
     if len(output)>1:
         axcolor   = 'lightgoldenrodyellow'
         axslider  = plt.axes([0.1, 0.05, 0.75, 0.01], facecolor=axcolor)
         slider    = Slider(axslider, 'Epoch', 0, len(output)-1, valinit=0, valstep=1)
         #######################################################################
         # functions for slider update, only if more than one epoch.
-        def press(event):
+        def press(event): #pragma: no cover
             try:
                 button = event.button
             except:
                 button = 'None'
             if event.key == 'right' or button == 'down':
                 if slider.val < len(output) - 1:
                     slider.set_val(slider.val + 1)
             elif event.key == 'left' or button == 'up':
                 if slider.val > 0:
                     slider.set_val(slider.val - 1)
             update(slider.val)
             fig.canvas.draw_idle()
         
-        def reset(event):
+        def reset(event):#pragma: no cover
             slider.reset()
             
-        def update(val):
+        def update(val):#pragma: no cover
             epoch0 = int(slider.val)
             deconv, h = deconvs[epoch0]
             s = psf[epoch0]
             # update all the plots
             datap.set_data(data[epoch0])
             modelp.set_data(output[epoch0])
             diffp.set_data((data[epoch0] - output[epoch0])/noisemap[epoch0])
@@ -364,7 +384,139 @@
             
     
         fig.canvas.mpl_connect('key_press_event', press)
         fig.canvas.mpl_connect('scroll_event', press)
         slider.on_changed(update)
     
     plt.show(block=False)
+
+def make_movie(model, kwargs, data, sigma_2, outpath, figsize=(9,7.5), epochs_list=None, duration=20, loop=1, format='gif'):
+    output = model.model(kwargs)
+    psf = model.psf
+    noisemap = sigma_2 ** 0.5
+
+    if epochs_list is None:
+        epochs_list = range(len(output))
+
+    # setup for first epoch
+    deconvs = [model.getDeconvolved(kwargs, i) for i in range(len(output))]
+    deconv, h = deconvs[0]
+    s = psf[0]
+
+    ##########################################################################
+    # figure
+    fig, axs = plt.subplots(2, 3, figsize=figsize)
+    for ax in axs.flatten():
+        ax.set_xticks([])
+        ax.set_yticks([])
+
+    datap = axs[0, 0].imshow(data[0], origin='lower')
+    axs[0, 0].set_title('data')
+
+    modelp = axs[0, 1].imshow(output[0], origin='lower')
+    axs[0, 1].set_title('model')
+
+    diffp = axs[1, 0].imshow((data[0] - output[0]) / noisemap[0], origin='lower')
+    axs[1, 0].set_title('(data-model)/noise')
+
+    backp = axs[1, 1].imshow(h, origin='lower')
+    axs[1, 1].set_title('background')
+
+    decp = axs[0, 2].imshow(deconv, origin='lower')
+    axs[0, 2].set_title('deconvolved')
+
+    psfp = axs[1, 2].imshow(s, origin='lower')
+    axs[1, 2].set_title('narrow psf')
+
+    plt.tight_layout()
+
+    # update all the plots
+    files = []
+    for i, epoch0 in enumerate(epochs_list):
+        deconv, h = deconvs[epoch0]
+        s = psf[epoch0]
+        datap.set_data(data[epoch0])
+        modelp.set_data(output[epoch0])
+        diffp.set_data((data[epoch0] - output[epoch0]) / noisemap[epoch0])
+        backp.set_data(h)
+        decp.set_data(deconv)
+        psfp.set_data(s)
+
+        file_png = os.path.join(outpath, "frame{0:05d}.png".format(i))
+        fig.savefig(file_png)
+        files.append(file_png)
+
+    if format == 'gif':
+        gif_name = os.path.join(outpath, "deconv.gif")
+        make_gif(files, gif_name, duration=duration, loop=loop)
+    elif format in ['FMP4', 'mp4v']:
+        video_name = os.path.join(outpath, 'deconv.mp4')
+        fps = duration / len(files)
+        make_video(files, outvid=video_name, fps=fps, size=None,
+                   is_color=True, format=format)
+    else:
+        RuntimeError('Unsupported video format. Use "gif" or "FMP4".')
+
+
+def make_gif(list_files, output_path, duration=100, loop= 1):
+    try:
+        from PIL import Image
+    except ImportError as e:
+        print(e)
+        print('Python package PIL is required for gif creation.')
+    frames = [Image.open(image) for image in list_files]
+    frame_one = frames[0]
+    frame_one.save(output_path, format="GIF", append_images=frames,
+               save_all=True, duration=duration)
+
+def make_video(images, outvid=None, fps=5, size=None,
+               is_color=True, format="XVID"):
+    """
+    Create a video from a list of images.
+
+    @param      outvid      output video
+    @param      images      list of images to use in the video
+    @param      fps         frame per second
+    @param      size        size of each frame
+    @param      is_color    color
+    @param      format      see http://www.fourcc.org/codecs.php
+    @return                 see http://opencv-python-tutroals.readthedocs.org/en/latest/py_tutorials/py_gui/py_video_display/py_video_display.html
+
+    The function relies on http://opencv-python-tutroals.readthedocs.org/en/latest/.
+    By default, the video will have the size of the first image.
+    It will resize every image to this size before adding them to the video.
+    """
+    try:
+        from cv2 import VideoWriter, VideoWriter_fourcc, imread, resize
+    except ImportError as e:
+        print(e)
+        print('Python package opencv-python is required for video creation.')
+        exit()
+
+    fourcc = VideoWriter_fourcc(*format)
+    vid = None
+    for image in images:
+        if not os.path.exists(image):
+            raise FileNotFoundError(image)
+        img = imread(image)
+        if vid is None:
+            if size is None:
+                size = img.shape[1], img.shape[0]
+            vid = VideoWriter(outvid, fourcc, float(fps), size, is_color)
+        if size[0] != img.shape[1] and size[1] != img.shape[0]:
+            img = resize(img, size)
+        vid.write(img)
+    vid.release()
+    return vid
+
+def plot_loss(loss_history, figsize = (10,5),  ax = None, title = None):
+    if ax is None:
+        fig, ax = plt.subplots(1,1, figsize =figsize)
+    ax.plot(range(len(loss_history)), loss_history)
+    ax.set_xlabel('Steps')
+    ax.set_ylabel('Loss')
+    ax.set_yscale('log')
+
+    if title is not None: 
+        ax.set_title(title)
+
+    return fig
```

### Comparing `starred-astro-1.1.1/starred/psf/parameters.py` & `starred-astro-1.2.2/starred/deconvolution/parameters.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,95 +1,84 @@
 import jax.numpy as jnp
 import numpy as np
 
 from starred.utils.parameters import Parameters
 
-__all__ = ['ParametersPSF']
+__all__ = ['ParametersDeconv']
 
 
-class ParametersPSF(Parameters):
+class ParametersDeconv(Parameters):
     """
-    Point Spread Function parameters class.
+    Deconvolution parameters class.
 
     """
 
     def __init__(self, image_class, kwargs_init, kwargs_fixed, kwargs_up=None, kwargs_down=None):
         """
-        :param image_class: image/PSF class from ``starred.psf.psf``
+        :param image_class: image/deconvolution class from ``starred.deconvolution.deconvolution``
         :param kwargs_init: dictionary with information on the initial values of the parameters 
         :param kwargs_fixed: dictionary containing the fixed parameters 
         :param kwargs_up: dictionary with information on the upper bounds of the parameters 
         :param kwargs_down: dictionary with information on the lower bounds of the parameters 
 
         """
-        super(ParametersPSF, self).__init__(image_class, kwargs_init, kwargs_fixed, kwargs_up=kwargs_up,
-                                            kwargs_down=kwargs_down)
+        super(ParametersDeconv, self).__init__(image_class, kwargs_init, kwargs_fixed, kwargs_up=kwargs_up,
+                                               kwargs_down=kwargs_down)
 
     def args2kwargs(self, args):
         """Obtain a dictionary of keyword arguments from positional arguments."""
         i = 0
-        kwargs_moffat, i = self._get_params(args, i, 'kwargs_moffat')
-        kwargs_gaussian, i = self._get_params(args, i, 'kwargs_gaussian')
+        kwargs_analytic, i = self._get_params(args, i, 'kwargs_analytic')
         kwargs_background, i = self._get_params(args, i, 'kwargs_background')
         # wrap-up
-        kwargs = {'kwargs_moffat': kwargs_moffat, 'kwargs_gaussian': kwargs_gaussian,
-                  'kwargs_background': kwargs_background}
-
+        kwargs = {'kwargs_analytic': kwargs_analytic, 'kwargs_background': kwargs_background}
         return kwargs
 
     def kwargs2args(self, kwargs):
         """Obtain an array of positional arguments from a dictionary of keyword arguments."""
-        args = self._set_params(kwargs, 'kwargs_moffat')
-        args += self._set_params(kwargs, 'kwargs_gaussian')
+        args = self._set_params(kwargs, 'kwargs_analytic')
         args += self._set_params(kwargs, 'kwargs_background')
         return jnp.array(args)
 
     def get_param_names_for_model(self, kwargs_key):
         """Returns the names of the parameters according to the key provided."""
-        if kwargs_key == 'kwargs_moffat':
-            return self._image.param_names_moffat
-        elif kwargs_key == 'kwargs_gaussian':
-            return self._image.param_names_gaussian
-        elif kwargs_key == 'kwargs_background':
-            return self._image.param_names_background
-        else:
-            raise KeyError('Key %s is not in the kwargs')
+        if kwargs_key == 'kwargs_analytic':
+            return self._image.param_names_analytic
+        return self._image.param_names_background
 
     def _get_params(self, args, i, kwargs_key):
         """Getting the parameters."""
         kwargs = {}
         kwargs_fixed_k = self._kwargs_fixed[kwargs_key]
         param_names = self.get_param_names_for_model(kwargs_key)
         for name in param_names:
-            if not name in kwargs_fixed_k.keys():
-                if name == 'background':
+            if not name in kwargs_fixed_k:
+                if name == 'a':
+                    num_param = self._image.M * self._image.epochs
+                elif name == 'h':
                     num_param = self._image.image_size_up ** 2
-                elif name == 'a':
-                    num_param = self._image.M
-                elif name == 'x0' or name == 'y0':
+                elif name == 'mean':
+                    num_param = self._image.epochs
+                elif name == 'dx' or name == 'dy':
+                    num_param = self._image.epochs - 1
+                elif name == 'c_x' or name == 'c_y':
                     num_param = self._image.M
                 else:
-                    num_param = 1
+                    raise NameError(f"The ParametersDeconv class does not know about this parameter: {name}.")
                 kwargs[name] = args[i:i + num_param]
                 i += num_param
+
             else:
                 kwargs[name] = kwargs_fixed_k[name]
+                free_ind = self._kwargs_free_indices[kwargs_key][name]
+                if len(free_ind) > 0:
+                    num_param = len(free_ind)
+                    kwargs[name] = kwargs[name].at[free_ind].set(args[i:i + num_param])
+                    i += num_param
 
         return kwargs, i
 
-    def _set_params(self, kwargs, kwargs_key):
-        """Setting the parameters."""
-        args = []
-        kwargs_profile = kwargs[kwargs_key]
-        kwargs_fixed_k = self._kwargs_fixed[kwargs_key]
-        param_names = self.get_param_names_for_model(kwargs_key)
-        for name in param_names:
-            if not name in kwargs_fixed_k and name != 'lambda':
-                if isinstance(kwargs_profile[name], list):
-                    args += kwargs_profile[name]
-                elif isinstance(kwargs_profile[name], (np.ndarray, np.generic)):
-                    args += kwargs_profile[name].tolist()
-                elif isinstance(kwargs_profile[name], (jnp.ndarray, jnp.generic)):
-                    args += kwargs_profile[name].tolist()
-                else:
-                    args += [kwargs_profile[name]]
+    def get_all_free_param_names(self, kwargs):
+        args = self._param_names(kwargs, 'kwargs_analytic')
+        args += self._param_names(kwargs, 'kwargs_background')
         return args
+
```

### Comparing `starred-astro-1.1.1/starred/psf/psf.py` & `starred-astro-1.2.2/starred/psf/psf.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,57 +1,68 @@
 import os
 import dill as pkl
 import warnings
-from functools import partial
+from packaging import version
 
 import jax.numpy as jnp
 import numpy as np
-from jax import jit, lax
+import jax
+from jax import lax
 
 from starred.utils.generic_utils import pad_and_convolve, pad_and_convolve_fft, fwhm2sigma, gaussian_function, \
     make_grid, \
-    moffat_function, Downsample, scipy_convolve, save_npy, save_fits
+    moffat_elliptical_function, moffat_function, Downsample, scipy_convolve, save_npy, save_fits
 
 
 class PSF(object):
     """
     Narrow Point Spread Function class. Coordinates and FWHM are given in the original pixel grid.
     
     """
-    param_names_moffat = ['fwhm', 'beta', 'C']
-    param_names_gaussian = ['a', 'x0', 'y0']
-    param_names_background = ['background']
 
     def __init__(
             self,
             image_size=64,
             number_of_sources=2,
             upsampling_factor=2,
             gaussian_fwhm=2,
-            convolution_method='fft',
+            convolution_method='scipy',
             gaussian_kernel_size=None,
             include_moffat=True,
+            elliptical_moffat=False,
     ):
         """
         :param image_size: input images size in pixels
         :type image_size: int
         :param number_of_sources: amount of input images (each containing a point source)
         :type number_of_sources: int
         :param upsampling_factor: the rate at which the sampling frequency increases in the PSF with respect to the input images
         :type upsampling_factor: int
-        :param gaussian_fwhm: the Gaussian's FWHM in pixels
+        :param gaussian_fwhm: the Gaussian's FWHM in pixels. Default is 2.
         :type gaussian_fwhm: int
-        :param convolution_method: method to use to calculate the convolution
+        :param convolution_method: method to use to calculate the convolution, choose between 'fft', 'scipy', and 'lax. Recommended if jax>=0.4.9 : 'scipy'
         :type convolution_method: str
-        :param gaussian_kernel_size: dimensions of the Gaussian kernel, not used if method = 'fft' (recommended)
+        :param gaussian_kernel_size: dimensions of the Gaussian kernel, not used if method = 'fft'. None will select the recommended size for each method.
         :type gaussian_kernel_size: int
-        :param include_moffat: True for the PSF to be expressed as the sum of a Moffat and a grid of pixels. False to not include the Moffat.
+        :param include_moffat: True for the PSF to be expressed as the sum of a Moffat and a grid of pixels. False to not include the Moffat. Default: True
         :type include_moffat: bool
+        :param elliptical_moffat: Allow elliptical Moffat.
+        :type elliptical_moffat: bool
 
         """
+        self.elliptical_moffat = elliptical_moffat
+        if self.elliptical_moffat:
+            self.analytic = self._analytic_ellitpical
+            self.param_names_moffat = ['fwhm_x', 'fwhm_y', 'phi', 'beta', 'C']
+        else:
+            self.analytic = self._analytic_circular
+            self.param_names_moffat = ['fwhm', 'beta', 'C']
+        self.param_names_gaussian = ['a', 'x0', 'y0']
+        self.param_names_background = ['background']
+
         self.image_size = image_size
         self.upsampling_factor = upsampling_factor
         self.image_size_up = self.image_size * self.upsampling_factor
         self.M = number_of_sources
         self.include_moffat = include_moffat
 
         if convolution_method == 'fft':
@@ -69,19 +80,20 @@
             else:
                 self.gaussian_size = gaussian_kernel_size
             self.shift_gaussian = 0.5
             self.shift_direction = 1.
         elif convolution_method == 'scipy':
             self._convolve = scipy_convolve
             if gaussian_kernel_size is None:
-                self.gaussian_size = 64
+                self.gaussian_size = 16
             else:
                 self.gaussian_size = gaussian_kernel_size
-            warnings.warn("WARNING : jax.scipy has no FFT implementation for the moment. It might be faster to use 'fft' on CPU.")
-            warnings.warn("WARNING : jax.scipy convolution has inverted shift convention for x0 and y0.")
+            if version.parse(jax.__version__) < version.parse('0.4.9'):
+                warnings.warn("WARNING : jax.scipy has no FFT implementation for the moment. It might be faster to use 'fft' on CPU.")
+
             self.shift_gaussian = 0.5
             self.shift_direction = -1 #scipy has inverted shift convention
         else:
             raise NotImplementedError('Unknown convolution method : choose fft, scipy or lax')
 
         self.fwhm = gaussian_fwhm
         self.sigma = fwhm2sigma(self.fwhm)
@@ -102,30 +114,57 @@
             x=x, y=y,
             amp=1, sigma_x=self.sigma,
             sigma_y=self.sigma,
             center_x=-(self.upsampling_factor * x0[i])*self.shift_direction - self.shift_gaussian,
             center_y=-(self.upsampling_factor * y0[i])*self.shift_direction - self.shift_gaussian,  # Convention : gaussian is placed at a center of a pixel
         ).reshape(self.gaussian_size, self.gaussian_size))
 
-    def analytic(self, fwhm, beta):
+
+    def _analytic_ellitpical(self, fwhmx, fwhmy, phi, beta):
+        """
+        Generates the narrow PSF's analytic term.
+
+        :param fwhm_x: the full width at half maximum value in the x direction
+        :type fwhm_x: float
+        :param fwhm_y: the full width at half maximum value in the y direction
+        :type fwhm_y: float
+        :param phi: orientation angle
+        :type phi: float
+        :param beta: the Moffat beta parameter
+        :type beta: float
+
+        :return: 2D Moffat
+
+        """
+        x, y = make_grid(numPix=self.image_size_up, deltapix=1.)
+        return jnp.array(moffat_elliptical_function(
+            x=x, y=y,
+            amp=1, fwhm_x=fwhmx * self.upsampling_factor,
+            fwhm_y = fwhmy * self.upsampling_factor, phi=phi, beta=beta,
+            center_x=0,
+            center_y=-0,
+        ).reshape(self.image_size_up, self.image_size_up))
+
+    def _analytic_circular(self, fwhm, beta):
         """
         Generates the narrow PSF's analytic term.
 
-        :param fwhm: the full width at half maximum value
+        :param fwhm: the full width at half maximum value in the x direction
         :type fwhm: float
         :param beta: the Moffat beta parameter
         :type beta: float
 
         :return: 2D Moffat
 
         """
         x, y = make_grid(numPix=self.image_size_up, deltapix=1.)
         return jnp.array(moffat_function(
             x=x, y=y,
-            amp=1, fwhm=fwhm * self.upsampling_factor, beta=beta,
+            amp=1, fwhm=fwhm * self.upsampling_factor,
+            beta=beta,
             center_x=0,
             center_y=-0,
         ).reshape(self.image_size_up, self.image_size_up))
 
     # @partial(jit, static_argnums=(0, 1, 5))
     def model(self, init=0, kwargs_moffat=None, kwargs_gaussian=None, kwargs_background=None, high_res=False):
         """
@@ -157,15 +196,18 @@
         Returns the analytical part of the PSF.
 
         :param kwargs_moffat: dictionary containing keyword arguments corresponding to the analytic term of the PSF
         :param norm: normalizes the Moffat
         :type norm: bool
 
         """
-        moff = kwargs_moffat['C'] * self.analytic(kwargs_moffat['fwhm'], kwargs_moffat['beta'])
+        if self.elliptical_moffat:
+            moff = kwargs_moffat['C'] * self.analytic(kwargs_moffat['fwhm_x'],kwargs_moffat['fwhm_y'],kwargs_moffat['phi'], kwargs_moffat['beta'])
+        else:
+            moff = kwargs_moffat['C'] * self.analytic(kwargs_moffat['fwhm'], kwargs_moffat['beta'])
         if norm:
             moff = moff / moff.sum()
 
         return moff
 
     def get_narrow_psf(self, kwargs_moffat=None, kwargs_gaussian=None, kwargs_background=None, norm=True):
         """
@@ -174,15 +216,15 @@
         :param kwargs_moffat: dictionary containing keyword arguments corresponding to the analytic term of the PSF
         :param kwargs_background: dictionary containing keyword arguments corresponding to the grid of pixels
         :return: array containing the `narrow` PSF
         """
 
         background = self.get_background(kwargs_background)
         if self.include_moffat:
-            moff = kwargs_moffat['C'] * self.analytic(kwargs_moffat['fwhm'], kwargs_moffat['beta'])
+            moff = self.get_moffat(kwargs_moffat, norm=False)
             s = moff + background
         else:
             s = background
             moff = jnp.zeros_like(s)
             s += lax.cond(s.sum() == 0, lambda _: 1e-6, lambda _: 0., operand=None)  # to avoid division per 0
 
         if norm:
@@ -199,17 +241,17 @@
         :param kwargs_background: dictionary containing keyword arguments corresponding to the grid of pixels
         :return: array containing the full PSF
         
         """
         s = self.get_narrow_psf(kwargs_moffat=kwargs_moffat, kwargs_gaussian=kwargs_gaussian, kwargs_background=kwargs_background, norm=norm)
         r = self.shifted_gaussians(0, [0.], [0.])
         if high_res:
-            psf = self._convolve(s, r, False)
+            psf = self._convolve(s, r)
         else :
-            psf = Downsample(self._convolve(s, r, False), factor=self.upsampling_factor)
+            psf = Downsample(self._convolve(s, r), factor=self.upsampling_factor)
         if norm:
             psf /= psf.sum()
 
         return psf
 
     def get_background(self, kwargs_background):
         """
@@ -324,15 +366,15 @@
             save_fct(estimated_full_psf, os.path.join(output_folder, f'full_psf_{i}'))
             save_fct(dif, os.path.join(output_folder, f'residuals_{i}'))
             save_fct(rr, os.path.join(output_folder, f'scaled_residuals_{i}'))
 
     def dump(self, path, kwargs, norm):
         """Stores information in a given file."""
         with open(path, 'wb') as f:
-            pkl.dump([self, kwargs, norm], f)
+            pkl.dump([self, kwargs, norm], f, protocol=pkl.HIGHEST_PROTOCOL)
 
     def smart_guess(self, data, fixed_background=True, guess_method = 'barycenter'):
         """
         Returns an initial guess of the kwargs, given the input data.
 
         :param data: array of shape (nimage, npix, npix) containing the input data
         :param fixed_background: fixes the background to 0
@@ -380,20 +422,29 @@
                 y0_est[i] = (indices[0] - self.image_size / 2.) #x and y needs to be inverted
         else :
             raise ValueError('Guess methods unknown. PLease choose between "max" and "barycenter".')
 
         # Amplitude (use the total flux to scale the amplitude parameters)
         ratio = jnp.array([data[i].sum() / data[i].sum() for i in range(self.M)])
         initial_a = jnp.ones(self.M) * ratio
-        kwargs_moffat_guess = {'fwhm': initial_fwhm, 'beta': initial_beta, 'C': 1.}
+        if self.elliptical_moffat:
+            kwargs_moffat_guess = {'fwhm_x': initial_fwhm,'fwhm_y': initial_fwhm, 'phi': 0., 'beta': initial_beta, 'C': 1.}
+            kwargs_moffat_up = {'fwhm_x': jnp.inf,'fwhm_y': jnp.inf, 'phi': np.pi/2., 'beta': jnp.inf, 'C': jnp.inf}
+            kwargs_moffat_down = {'fwhm_x': 0,'fwhm_y': 0, 'phi': 0, 'beta': 0, 'C': 0}
+        else:
+            kwargs_moffat_guess = {'fwhm': initial_fwhm, 'beta': initial_beta, 'C': 1.}
+            kwargs_moffat_up = {'fwhm': jnp.inf, 'beta': jnp.inf, 'C': jnp.inf}
+            kwargs_moffat_down = {'fwhm': 0., 'beta': 0., 'C': 0.}
+
         flux_moffat = Downsample(self.get_moffat(kwargs_moffat_guess, norm=False), factor=self.upsampling_factor).sum()
         initial_C = float(data[0].sum() / flux_moffat)
 
+        kwargs_moffat_guess['C']=initial_C
         kwargs_init = {
-            'kwargs_moffat': {'fwhm': initial_fwhm, 'beta': initial_beta, 'C': initial_C},
+            'kwargs_moffat': kwargs_moffat_guess,
             'kwargs_gaussian': {'a': initial_a, 'x0': x0_est, 'y0': y0_est},
             'kwargs_background': {'background': initial_background},
         }
 
         kwargs_fixed = {
             'kwargs_moffat': {},
             'kwargs_gaussian': {},
@@ -401,24 +452,24 @@
             'kwargs_background': {},
         }
         if fixed_background:
             kwargs_fixed['kwargs_background']['background'] = initial_background
 
         # Default value for boundaries
         kwargs_up = {
-            'kwargs_moffat': {'fwhm': jnp.inf, 'beta': jnp.inf, 'C': jnp.inf},
+            'kwargs_moffat': kwargs_moffat_up,
             'kwargs_gaussian': {'a': list([jnp.inf for i in range(self.M)]),
                                 'x0': list([self.image_size for i in range(self.M)]),
                                 'y0': list([self.image_size for i in range(self.M)])
                                 },
             'kwargs_background': {'background': list([jnp.inf for i in range(self.image_size_up ** 2)])},
         }
 
         kwargs_down = {
-            'kwargs_moffat': {'fwhm': 0., 'beta': 0., 'C': 0.},
+            'kwargs_moffat': kwargs_moffat_down,
             'kwargs_gaussian': {'a': list([0 for i in range(self.M)]),
                                 'x0': list([-self.image_size for i in range(self.M)]),
                                 'y0': list([-self.image_size for i in range(self.M)]),
                                 },
             'kwargs_background': {'background': list([-jnp.inf for i in range(self.image_size_up ** 2)])},
         }
```

### Comparing `starred-astro-1.1.1/starred/utils/ds9reg.py` & `starred-astro-1.2.2/starred/utils/ds9reg.py`

 * *Files 8% similar despite different names*

```diff
@@ -83,7 +83,10 @@
                     if (squaredist < circle["r"] ** 2.0):
                         self.nomask[i, j] = False
 
                 for box in self.boxes:
                     if (i > box["centerx"] - box["sizex"] / 2.0) and (i < box["centerx"] + box["sizex"] / 2.0) and (
                             j > box["centery"] - box["sizey"] / 2.0) and (j < box["centery"] + box["sizey"] / 2.0):
                         self.nomask[i, j] = False
+
+        #transpose because DS9 has inverted convention
+        self.nomask = self.nomask.T
```

### Comparing `starred-astro-1.1.1/starred/utils/generic_utils.py` & `starred-astro-1.2.2/starred/utils/generic_utils.py`

 * *Files 20% similar despite different names*

```diff
@@ -206,14 +206,48 @@
     """
     r0 = fwhm / (2. * jnp.sqrt(2. ** (1. / beta) - 1.))
     delta_x = jnp.subtract(x, center_x)
     delta_y = jnp.subtract(y, center_y)
     rr_gg = (delta_x / r0) ** 2 + (delta_y / r0) ** 2
     return amp * (1 + rr_gg) ** (-beta)
 
+
+@jit
+def moffat_elliptical_function(x, y, amp, fwhm_x, fwhm_y, phi, beta, center_x, center_y):
+    """
+    :param x: 1D array of x positions
+    :param y: 1D array of y positions
+    :param amp: the amplitude coefficient
+    :type amp: float
+    :param fwhm_x: the full width at half maximum value in the x direction
+    :type fwhm_x: float
+    :param fwhm_y: the full width at half maximum value in the y direction
+    :type fwhm_y: float
+    :param phi: orientation angle
+    :type phi: float
+    :param beta: the Moffat beta parameter
+    :type beta: float
+    :param center_x: x position of the center
+    :type center_x: float
+    :param center_y: y position of the center
+    :type center_y: float
+
+    :return: 2D Elliptical Moffat
+
+    """
+    r0_x = fwhm_x / (2. * jnp.sqrt(2. ** (1. / beta) - 1.))
+    r0_y = fwhm_y / (2. * jnp.sqrt(2. ** (1. / beta) - 1.))
+    delta_x = jnp.subtract(x, center_x)
+    delta_y = jnp.subtract(y, center_y)
+    A = (jnp.cos(phi) / r0_x)**2  + (jnp.sin(phi) / r0_y)**2
+    B = (jnp.sin(phi) / r0_x)**2  + (jnp.cos(phi) / r0_y)**2
+    C = 2*jnp.sin(phi)*jnp.cos(phi)*(1./ r0_x**2 - 1/r0_y**2)
+    rr_gg = A*(delta_x ** 2) + B * (delta_y ** 2) + C * delta_x * delta_y
+    return amp * (1 + rr_gg) ** (-beta)
+
 def twoD_Gaussian(x,y, amplitude, xo, yo, sigma_x, sigma_y, theta):
     """
     Analytical 2D Gaussian function
 
     :param x: array containing x-axis variable
     :param y: array containing y-axis variable
     :param amplitude: amplitude of the Gaussian
```

### Comparing `starred-astro-1.1.1/starred/utils/jax_utils.py` & `starred-astro-1.2.2/starred/utils/jax_utils.py`

 * *Files identical despite different names*

### Comparing `starred-astro-1.1.1/starred/utils/noise_utils.py` & `starred-astro-1.2.2/starred/utils/noise_utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -114,15 +114,15 @@
             dirac[nx_psi // 2, ny_psi // 2] = 1
             dirac_wt = PhiT_operator(dirac, num_scales)
 
             psi_wt_std = []
             for k in range(num_scales + 1):
                 psi_wt_std2_k = model._convolve(blurred_noise**2, dirac_wt[k]**2)
                 psi_wt_std_k = np.sqrt(psi_wt_std2_k)
-                psi_wt_std_k = np.nan_to_num(psi_wt_std_k, nan=np.nanmin(psi_wt_std_k))
+                psi_wt_std_k = np.nan_to_num(psi_wt_std_k, nan=np.nanmin(psi_wt_std_k)) * upsampling_factor**2 #scaling is important here to match 'MC' scaling convention
                 psi_wt_std.append(psi_wt_std_k)
             psi_wt_std = np.array(psi_wt_std)  # --> shape = (num_scales, nx_psi, ny_psi)
             psi_wt_std_list.append(psi_wt_std) # one per type of (wavelet, num_scales)
     else:
         raise ValueError(f"Method '{method}' for noise propagation is not supported.")
 
     return psi_wt_std_list
```

### Comparing `starred-astro-1.1.1/starred/utils/optimization.py` & `starred-astro-1.2.2/starred/utils/optimization.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,20 +1,17 @@
 import time
 import warnings
 
 import jax
 import numpy as np
 import optax
-import scipy
-from scipy import optimize
+from starred.utils.inference_base import FisherCovariance
 from tqdm import tqdm
 import jaxopt
 
-print(scipy.__version__)
-
 from starred.utils.inference_base import InferenceBase
 
 __all__ = ['Optimizer']
 
 SUPPORTED_METHOD_OPTAX = ['adam', 'adabelief', 'radam']
 SUPPORTED_METHOD_JAXOPT = ['BFGS', 'GradientDescent', 'LBFGS', 'l-bfgs-b', 'LevenbergMarquardt']
 SUPPORTED_METHOD_SCIPYMINIMIZE = ['Nelder-Mead', 'Powell', 'CG', 'Newton-CG', 'TNC', 'COBYLA', 'SLSQP', 'trust-constr', 'dogleg', 'trust-ncg', 'trust-exact', 'trust-krylov']
@@ -120,15 +117,15 @@
             solver = jaxopt.ScipyBoundedMinimize(fun=self.loss, method="l-bfgs-b", callback=self._metrics,
                                                  **kwargs_optimiser)
         elif self.method == 'LevenbergMarquardt':
             solver = jaxopt.LevenbergMarquardt(residual_fun=lambda x: jax.numpy.array([self.loss(x)]), 
                                                **kwargs_optimiser)
 
         res = solver.run(params, **extra_kwargs)
-        extra_fields = {'result_class': res, 'stat':res.state}
+        extra_fields = {'result_class': res, 'stat':res.state, 'loss_history':self._metrics.loss_history}
 
         return res.params, extra_fields
 
     def _run_optax(self, params, max_iterations=100, min_iterations=None,
               init_learning_rate=1e-2, schedule_learning_rate=True,
               restart_from_init=False, stop_at_loss_increase=False,
               progress_bar=True, return_param_history=False):
@@ -206,14 +203,24 @@
     @staticmethod
     def _for_loop(iterable, progress_bar_bool, **tqdm_kwargs):
         if progress_bar_bool is True:
             return tqdm(iterable, **tqdm_kwargs)
         else:
             return iterable
 
+    def compute_fisher_matrix(self):
+        if len(self._param.best_fit_values(as_kwargs=False)) > 500:
+            warnings.warn('Computing the Fisher matrix for more than 500 dimension will blow up your memory. '
+                                'You should reduce the dimensionnality of your model')
+
+        fish = FisherCovariance(self._param, self)
+        fish.compute_fisher_information()
+
+        return fish
+
 
 class MinimizeMetrics(object):
     """Simple callable class used as callback in ``scipy.optimize.minimize`` method."""
 
     def __init__(self, func, method):
         self.loss_history = []
         self.param_history = []
```

### Comparing `starred-astro-1.1.1/starred_astro.egg-info/SOURCES.txt` & `starred-astro-1.2.2/starred_astro.egg-info/SOURCES.txt`

 * *Files 3% similar despite different names*

```diff
@@ -12,14 +12,15 @@
 starred/plots/plot_function.py
 starred/psf/__init__.py
 starred/psf/loss.py
 starred/psf/parameters.py
 starred/psf/psf.py
 starred/utils/__init__.py
 starred/utils/ds9reg.py
+starred/utils/fitting_sequence.py
 starred/utils/generic_utils.py
 starred/utils/inference_base.py
 starred/utils/jax_utils.py
 starred/utils/noise_utils.py
 starred/utils/optimization.py
 starred/utils/parameters.py
 starred_astro.egg-info/PKG-INFO
```

