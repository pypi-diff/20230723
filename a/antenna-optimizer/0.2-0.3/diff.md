# Comparing `tmp/antenna-optimizer-0.2.tar.gz` & `tmp/antenna-optimizer-0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/antenna-optimizer-0.2.tar", last modified: Sat Nov 20 15:37:47 2021, max compression
+gzip compressed data, was "antenna-optimizer-0.3.tar", last modified: Sun Jul 23 14:47:13 2023, max compression
```

## Comparing `antenna-optimizer-0.2.tar` & `antenna-optimizer-0.3.tar`

### file list

```diff
@@ -1,28 +1,33 @@
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2021-11-20 15:37:47.000000 antenna-optimizer-0.2/
--rw-r--r--   0 ralf      (1000) priv      (1011)    14594 2021-11-20 15:37:47.000000 antenna-optimizer-0.2/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)    19560 2021-11-20 15:35:06.000000 antenna-optimizer-0.2/README.html
--rw-r--r--   0 ralf      (1000) priv      (1011)    11742 2021-11-20 15:34:48.000000 antenna-optimizer-0.2/README.rst
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2021-11-20 15:37:47.000000 antenna-optimizer-0.2/antenna_optimizer/
--rw-r--r--   0 ralf      (1000) priv      (1011)       14 2021-11-20 15:36:59.000000 antenna-optimizer-0.2/antenna_optimizer/Version.py
--rw-r--r--   0 ralf      (1000) priv      (1011)        0 2021-11-20 15:18:40.000000 antenna-optimizer-0.2/antenna_optimizer/__init__.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    33454 2021-09-25 19:34:39.000000 antenna-optimizer-0.2/antenna_optimizer/antenna_model.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    74302 2021-11-01 13:48:14.000000 antenna-optimizer-0.2/antenna_optimizer/coaxmodel.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     7259 2021-10-08 08:05:27.000000 antenna-optimizer-0.2/antenna_optimizer/folded.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     6253 2021-10-08 08:05:30.000000 antenna-optimizer-0.2/antenna_optimizer/folded_3ele.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     7428 2021-10-08 08:06:50.000000 antenna-optimizer-0.2/antenna_optimizer/folded_bc.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    12752 2021-10-08 08:07:39.000000 antenna-optimizer-0.2/antenna_optimizer/folded_bigrefl.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    14011 2021-10-08 08:11:09.000000 antenna-optimizer-0.2/antenna_optimizer/hb9cv.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     8771 2021-10-08 08:17:15.000000 antenna-optimizer-0.2/antenna_optimizer/logper.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     7411 2021-02-21 09:18:03.000000 antenna-optimizer-0.2/antenna_optimizer/statstool.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    13616 2021-10-08 10:10:02.000000 antenna-optimizer-0.2/antenna_optimizer/tl.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    12894 2021-04-20 15:44:33.000000 antenna-optimizer-0.2/antenna_optimizer/transmission.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2021-11-20 15:37:47.000000 antenna-optimizer-0.2/bin/
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       74 2021-10-08 07:39:19.000000 antenna-optimizer-0.2/bin/coaxmodel
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       76 2021-10-08 07:53:21.000000 antenna-optimizer-0.2/bin/folded_3ele_antenna
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       71 2021-10-08 07:40:07.000000 antenna-optimizer-0.2/bin/folded_antenna
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       74 2021-10-08 07:52:27.000000 antenna-optimizer-0.2/bin/folded_bc_antenna
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       79 2021-10-08 07:52:48.000000 antenna-optimizer-0.2/bin/folded_bigrefl_antenna
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       70 2021-10-08 07:53:54.000000 antenna-optimizer-0.2/bin/hb9cv_antenna
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       71 2021-10-08 07:54:08.000000 antenna-optimizer-0.2/bin/logper_antenna
--rwxr-xr-x   0 ralf      (1000) priv      (1011)       67 2021-10-08 07:54:36.000000 antenna-optimizer-0.2/bin/transmission_line
--rw-r--r--   0 ralf      (1000) priv      (1011)     3890 2021-11-20 15:22:23.000000 antenna-optimizer-0.2/setup.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 14:47:13.860653 antenna-optimizer-0.3/
+-rw-r--r--   0 ralf      (1000) priv      (1011)       40 2021-10-08 07:59:11.000000 antenna-optimizer-0.3/MANIFEST.in
+-rw-r--r--   0 ralf      (1000) priv      (1011)    13523 2023-07-23 14:47:13.860653 antenna-optimizer-0.3/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)    20244 2023-07-23 14:43:20.000000 antenna-optimizer-0.3/README.html
+-rw-r--r--   0 ralf      (1000) priv      (1011)    12221 2023-07-23 14:35:05.000000 antenna-optimizer-0.3/README.rst
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 14:47:13.836653 antenna-optimizer-0.3/antenna_optimizer/
+-rw-r--r--   0 ralf      (1000) priv      (1011)       14 2023-07-23 14:43:20.000000 antenna-optimizer-0.3/antenna_optimizer/Version.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)        0 2021-11-20 15:18:40.000000 antenna-optimizer-0.3/antenna_optimizer/__init__.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    52054 2023-02-18 15:24:58.000000 antenna-optimizer-0.3/antenna_optimizer/antenna_model.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    78628 2023-06-15 18:22:38.000000 antenna-optimizer-0.3/antenna_optimizer/coaxmodel.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     6911 2023-02-18 15:12:54.000000 antenna-optimizer-0.3/antenna_optimizer/folded.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     5888 2023-02-18 15:11:53.000000 antenna-optimizer-0.3/antenna_optimizer/folded_3ele.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     7029 2023-02-18 15:12:17.000000 antenna-optimizer-0.3/antenna_optimizer/folded_bc.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    12375 2023-02-18 15:12:36.000000 antenna-optimizer-0.3/antenna_optimizer/folded_bigrefl.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    12559 2023-02-18 15:13:16.000000 antenna-optimizer-0.3/antenna_optimizer/hb9cv.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     3413 2023-02-18 15:13:29.000000 antenna-optimizer-0.3/antenna_optimizer/hf_folded.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     6996 2023-02-18 15:13:50.000000 antenna-optimizer-0.3/antenna_optimizer/hf_fuchs.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     3628 2023-02-18 15:14:03.000000 antenna-optimizer-0.3/antenna_optimizer/hf_inverted_v.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     8405 2023-02-18 15:14:31.000000 antenna-optimizer-0.3/antenna_optimizer/logper.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    10842 2023-02-18 15:14:54.000000 antenna-optimizer-0.3/antenna_optimizer/multi_dipole.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     7371 2023-02-18 15:15:32.000000 antenna-optimizer-0.3/antenna_optimizer/statstool.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    13243 2023-02-18 15:16:14.000000 antenna-optimizer-0.3/antenna_optimizer/tl.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    12874 2023-02-18 15:16:44.000000 antenna-optimizer-0.3/antenna_optimizer/transmission.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 14:47:13.856653 antenna-optimizer-0.3/antenna_optimizer.egg-info/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    13523 2023-07-23 14:47:13.000000 antenna-optimizer-0.3/antenna_optimizer.egg-info/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)      833 2023-07-23 14:47:13.000000 antenna-optimizer-0.3/antenna_optimizer.egg-info/SOURCES.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-07-23 14:47:13.000000 antenna-optimizer-0.3/antenna_optimizer.egg-info/dependency_links.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)      620 2023-07-23 14:47:13.000000 antenna-optimizer-0.3/antenna_optimizer.egg-info/entry_points.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       42 2023-07-23 14:47:13.000000 antenna-optimizer-0.3/antenna_optimizer.egg-info/requires.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)       18 2023-07-23 14:47:13.000000 antenna-optimizer-0.3/antenna_optimizer.egg-info/top_level.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)     3893 2023-07-23 14:40:53.000000 antenna-optimizer-0.3/pyproject.toml
+-rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-07-23 14:47:13.860653 antenna-optimizer-0.3/setup.cfg
+-rw-r--r--   0 ralf      (1000) priv      (1011)     4121 2023-07-23 14:41:28.000000 antenna-optimizer-0.3/setup.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `antenna-optimizer-0.2/PKG-INFO` & `antenna-optimizer-0.3/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,264 +1,284 @@
-Metadata-Version: 1.1
+Metadata-Version: 2.1
 Name: antenna-optimizer
-Version: 0.2
+Version: 0.3
 Summary: Optimize antennas using NEC and a genetic algorithm
 Home-page: https://github.com/schlatterbeck/antenna-optimizer
 Author: Ralf Schlatterbeck
-Author-email: rsc@runtux.com
+Author-email: Ralf Schlatterbeck <rsc@runtux.com>
 License: BSD License
-Description: Antenna Optimizer
-        =================
-        
-        .. |ohm| unicode:: U+02126 .. Omega
-        .. |_| unicode:: U+00A0 .. Non-breaking space
-           :trim:
-        
-        This project can optimize anntennas using genetic algorithms.  It uses
-        my pgapy_ Python wrapper for PGApack_, the parallel genetic algorithm
-        library, originally by David Levine at Argonne National Laboratory and
-        currently maintained by me. It also uses PyNEC_, the Python wrapper for
-        NEC2++, the C++ version of the `Numerical Electromagnetics Code`_.
-        
-        Originally this started out with a low-gain two-element antenna where
-        the driven element is a folded dipole. One of the requirements for that
-        antenna was that it should have 50 |_| |ohm| impedance and at least some
-        forward gain. Optimizing this antenna by hand soon turned out to be
-        tedious and I started experimenting with optimization by a genetic
-        algorithm.
-        
-        You can find the original experiments in ``folded.nec`` and
-        ``folded2.nec``. These are input files to the command-line NEC programs.
-        You can either use the ``nec2c`` command-line program which produces an
-        output file that can be viewed with ``xnecview`` or you can use
-        graphical ``xnec2c`` program. All run under Linux and are included in
-        the Debian Linux distribution. The ``.nec`` files *may* also be usable
-        with other NEC versions on other operating systems but I have not tried.
-        
-        For optimizing the two-element Yagi-Uda you can use the command-line
-        tool ``folded_antenna`` where the optimizer is implemented in
-        ``folded.py``. Later a 3-element antenna with the same principles was
-        added in ``folded_3ele.py`` callable with the command-line tool
-        ``folded_3ele_antenna``.
-        
-        The ``antenna_model.py`` factors out the common parts of the various
-        antennas.
-        
-        The ``hb9cv.py`` with the command-line tool ``hb9cv_antenna`` models the
-        well-know HB9CV antenna but only very crudely. NEC2 isn't really suited
-        for modelling the phasing stubs of that antenna because it doesn't like
-        parallel wires that are too close. I mainly did this for comparing some
-        of the antennas resulting from optimization with the well-known
-        performance of the HB9CV.
-        
-        In the file ``logper.py`` with the command-line tool ``logper_antenna``
-        you can find a 9-element log-periodic antenna.  It can currently not be
-        optimized, the performance of the real antenna is better than the
-        results obtained with NEC, so I didn't implement an optimizer for it
-        yet.
-        
-        All the antenna programs take an action as mandatory argument. The
-        action is typically either ``optimize`` for running the optimizer or
-        ``necout`` for creating a ``.nec`` file which can then be fed to one of
-        the nec programs mentioned above. When running the optimizer it makes
-        sense to experiment with different random seeds, each random seed will
-        usually produce a different antenna. In addition there are some
-        experimental actions, ``frgain`` prints the forward and backward gains
-        (in dBi) for the lowest, the middle, and the highest frequencies and the
-        VSWR for those. The ``gain`` action visualizes the 3D antenna gain
-        pattern and the ``swr`` action visualizes the VSWR over the given
-        frequency range. Note that both, the ``gain`` and the ``swr`` action
-        compute the antenna data over the whole frequency range using NEC and
-        that may take some time.
-        
-        The output of the optimizer is text (usually redirected to a file) that
-        prints the evaluation, the VSWR, maximum gain, and forward/backward
-        ratio of the best antenna for every 10th generation of the genetic
-        algorithm. In addition the command-line options to create that antenna
-        are printed. When the genetic algorithm doesn't make any more progress,
-        the search terminates and the data of the best evaluation are given. An
-        example of the last lines of such a text is as follows. The data is from
-        one of the best 2-element antennas was obtained with the random seed 26
-        of an earlier version of the program::
-        
-            The Best Evaluation: 2.886437e+02.
-            The Best String:
-            -r 0.0364 -d 0.0444 -l 0.1704 -4 0.1075
-            VSWR: [1.7901433511443068, 1.1495780609982815, 1.7995760521232753]
-            GMAX: 6.69913175227, RMAX: -3.03663376703
-            Cache hits: 5670/9243 61.34%
-            Eval: 288.64
-            [ 101011001100101001111000000010011 ]
-        
-        This tells us the evaluation (which is meaningful only to the
-        genetic algorithm), the genetic algorithm *maximizes* this value.
-        The command-line options after the line ``The Best String:`` can be used
-        to create a ``.nec`` file for that antenna. The antenna in the example
-        has a voltage standing wave ratio of < |_| 1.8 at the band ends and
-        around 1.15 in the middle of the band (the 70cm band from 430 to
-        440 |_| MHz in that case). The forward gain (in the middle of the band)
-        is 6.7 |_| dBi. The RMAX value is the (maximum) backward gain (in a 30
-        degree area in the back). So the F/B ratio of that antenna is::
-        
-         6.7 dB - -3.0 dB = 9.7 dB
-        
-        The last line of the text output contains the genetic representation of
-        that antenna.
-        The ``.nec`` file for the antenna above which was optimized with an early
-        version of this package can be created with the command::
-        
-         folded_antenna -r 0.0364 -d 0.0444 -l 0.1704 -4 0.1075 necout > folded-opt.nec
-        
-        The command-line options specify the radius of the folded dipole, the
-        distance of the reflector from the folded dipole, the (half) length of
-        the reflector, and the (half) length of the straight part of the folded
-        dipole, respectively.
-        
-        According to NEC it has a standing wave ratio (VSWR) of < |_| 1.8 from
-        430-440 |_| MHz, a forward gain of > |_| 6.5 dBi over the whole
-        frequency range and a Forward/Back Ratio of 8-11 dB.
-        
-        If you want to implement an optimizer for your own antenna, look at the
-        file ``folded.py``: You need to implement a class that defines the
-        geometry of the new antenna and an optimizer class that initializes the
-        gene ranges and implements a ``compute_antenna`` method that returns an
-        instance of your antenna class with the parameters obtained from the
-        given gene. All lengths in the models are metric (in meters) as is the
-        default in NEC.
-        
-        A recent addition to this package involves modelling of coax cables.
-        This uses information from an old article by Frank Witt [1]_ to derive
-        everything necessary to model a transmission line *with* loss from the
-        manufacturer cable data. The command-line tool for using these coax
-        models is named ``coaxmodel``. Again this command has several
-        sub-commands: 
-        
-        - ``loss``: This displays the fitted loss-curves from the manufacturer
-          data against the curve-fit algorithm used, you can see how much
-          difference in dB the fitted curve has to the loss at certain
-          frequencies given by the manufacturer data.
-        - ``match`` computes the impedance at the load and input (depending on
-          which was given as an input the other is computed), the matched and
-          total loss (the matched loss is the loss in the cable if the load is
-          prefectly matched, the total loss is the sum of the matched loss and
-          the additional loss due to reflections), the SWR and data for various
-          stub-matches to get to the cable impedance Z0.
-        - ``resonator`` computes the resistance and Q-factor of a coax resonator
-          at the given frequency. A resonator is a piece of cable that either
-          has a short-circuit or an open-circuit at the far end. The sub-command
-          computes resonators for quarter and half wave at the given frequency.
-        - ``stub`` computes the length, Q-factor, and resulting impedance as
-          well as the inductance or capacitance of a stub for a given impedance
-          and frequency. The impedance by default is -100j Ohm and can be
-          changed with the -x option. The stub with the shortest resulting
-          length is chosen, so for a negative reactance an open stub is chosen
-          while for a positive reactance a closed stub is chosen.
-        
-        For all these sub-commands you can specify the frequency, length of
-        cable and impedance (either at the load or at the end of the cable) to
-        be used in computing the results. You can specify complex impedances as
-        a python complex number in the format a+bj, e.g. 50-500j.
-        
-        Finally the ``transmission_line`` program can optimize the stub-matching
-        for a transmission line using NEC. By default a lossless line is asumed.
-        Also by default a closed stub at the closest possible position is
-        searched.
-        
-        Transmission lines can be modelled by NEC with the ``TL`` (transmission
-        line) card.  But NEC can also model arbitrary (symmetric, passive)
-        networks with the ``NT`` (network) card. We use this (and the code in
-        ``coaxmodel.py``) to model a real cable *with loss* for stub matching.
-        It is instructive to compare the values for stub-matching obtained
-        analytically from ``coaxmodel`` with the values obtained from an
-        optimization with the genetic algorithm by ``transmission_line``. Note
-        that the coaxmodel takes frequecies in Hz while transmission_line (which
-        uses NEC) accepts frequencies in MHz. So we match a complex impedance of
-        75+15j |Ohm| for example::
-        
-         coaxmodel -c sytronic_RG_58_CU -f 435e6 -z 75+15j match
-        
-        This yields a stub of length 8.007 cm attached 7.888 cm from the load when
-        matching with a closed stub. When optimizing with ``transmission_line``::
-        
-         transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j optimize
-        
-        we get 8.016cm for the stub length and 7.6cm for the distance of the
-        stub from the load. We can visualize this over a given frequency range
-        by either producing NEC output::
-        
-         transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j -i 50 \
-            -l 0.0816 -d 0.076 --frqstart=430 --frqend=440 necout > x1.nec
-         transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j -i 50 \
-            -l 0.08007 -d 0.07888 --frqstart=430 --frqend=440 necout > x2.nec
-        
-        And the compute the nec model and display with::
-        
-         nec2c -i x1.nec > x1.out
-         nec2c -i x2.nec > x2.out
-         xnecview x1.out
-         xnecview x2.out
-        
-        Or directly display the VSWR curves with::
-        
-         transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j -i 50 \
-            -l 0.0816 -d 0.076 --frqstart=430 --frqend=440 swr
-         transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j -i 50 \
-            -l 0.08007 -d 0.07888 --frqstart=430 --frqend=440 swr
-        
-        Both are close enough, the SWR is below 1.1 over the whole frequency
-        range given. Note that this can change drastically if load impedances
-        with a higher VSWR are matched.
-        
-        Also note that the NEC files produced in the example above have a different
-        NEC network *for each frequency*. This is because NEC models networks
-        using an `admittance matrix`_ which is frequency dependent.
-        
-        This means the sequence of two ``NT``
-        cards, a ``TL`` card, a ``FR`` card and a ``RP`` card are repeated for
-        each frequency. Here the two ``NT`` cards define the network of the
-        cable from the load to the stub and the stub itself while the ``TL``
-        card defines the length of a lossless transmission line from the stub to
-        the source. The ``FR`` card specifies a single frequency and the ``RP``
-        card defines a radiation pattern and triggers computation. This format
-        is perfectly valid NEC code, but certain programs (like the popular
-        ``xnec2c``) cannot deal with this format and display only a single
-        frequency.
-        
-        .. [1] Frank Witt. Transmission line properties from manufacturer’s
-           data. In R. Dean Straw, editor, The ARRL Antenna Compendium, volume 6,
-           pages 179–183. American Radio Relay League (ARRL), 1999.
-        
-        .. _pgapy:  https://pypi.org/project/PGAPy/
-        .. _PGApack: https://github.com/schlatterbeck/pgapack
-        .. _PyNEC: https://pypi.org/project/PyNEC/
-        .. _`PyNEC source`: https://github.com/tmolteno/python-necpp
-        .. _`Numerical Electromagnetics Code`:
-            https://en.wikipedia.org/wiki/Numerical_Electromagnetics_Code
-        .. _`admittance matrix`: https://en.wikipedia.org/wiki/Admittance_parameters
-        
-        Changes
-        -------
-        
-        Version 0.2: More cable data
-        
-        - Fix setup to correctly specify dependencies
-        - Add more cable data the following command will list supported cable
-          types::
-        
-            coaxmodel --help
-        
-        Version 0.1: Initial Release
-        
+Project-URL: Homepage, https://github.com/schlatterbeck/antenna-optimizer
+Project-URL: Bug Tracker, https://github.com/schlatterbeck/antenna-optimizer/issues
 Platform: Any
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Intended Audience :: Developers
+Classifier: Intended Audience :: Science/Research
 Classifier: Programming Language :: Python :: 2
 Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Python: >=3.7
+Description-Content-Type: text/x-rst
+
+Antenna Optimizer
+=================
+
+.. |ohm| unicode:: U+02126 .. Omega
+.. |_| unicode:: U+00A0 .. Non-breaking space
+   :trim:
+
+This project can optimize anntennas using genetic algorithms.  It uses
+my pgapy_ Python wrapper for PGApack_, the parallel genetic algorithm
+library, originally by David Levine at Argonne National Laboratory and
+currently maintained by me. It also uses PyNEC_, the Python wrapper for
+NEC2++, the C++ version of the `Numerical Electromagnetics Code`_.
+
+Originally this started out with a low-gain two-element antenna where
+the driven element is a folded dipole. One of the requirements for that
+antenna was that it should have 50 |_| |ohm| impedance and at least some
+forward gain. Optimizing this antenna by hand soon turned out to be
+tedious and I started experimenting with optimization by a genetic
+algorithm.
+
+You can find the original experiments in ``folded.nec`` and
+``folded2.nec``. These are input files to the command-line NEC programs.
+You can either use the ``nec2c`` command-line program which produces an
+output file that can be viewed with ``xnecview`` or you can use
+graphical ``xnec2c`` program. All run under Linux and are included in
+the Debian Linux distribution. The ``.nec`` files *may* also be usable
+with other NEC versions on other operating systems but I have not tried.
+
+For optimizing the two-element Yagi-Uda you can use the command-line
+tool ``folded_antenna`` where the optimizer is implemented in
+``folded.py``. Later a 3-element antenna with the same principles was
+added in ``folded_3ele.py`` callable with the command-line tool
+``folded_3ele_antenna``.
+
+The ``antenna_model.py`` factors out the common parts of the various
+antennas.
+
+The ``hb9cv.py`` with the command-line tool ``hb9cv_antenna`` models the
+well-know HB9CV antenna but only very crudely. NEC2 isn't really suited
+for modelling the phasing stubs of that antenna because it doesn't like
+parallel wires that are too close. I mainly did this for comparing some
+of the antennas resulting from optimization with the well-known
+performance of the HB9CV.
+
+In the file ``logper.py`` with the command-line tool ``logper_antenna``
+you can find a 9-element log-periodic antenna.  It can currently not be
+optimized, the performance of the real antenna is better than the
+results obtained with NEC, so I didn't implement an optimizer for it
+yet.
+
+All the antenna programs take an action as mandatory argument. The
+action is typically either ``optimize`` for running the optimizer or
+``necout`` for creating a ``.nec`` file which can then be fed to one of
+the nec programs mentioned above. When running the optimizer it makes
+sense to experiment with different random seeds, each random seed will
+usually produce a different antenna. In addition there are some
+experimental actions, ``frgain`` prints the forward and backward gains
+(in dBi) for the lowest, the middle, and the highest frequencies and the
+VSWR for those. The ``gain`` action visualizes the 3D antenna gain
+pattern and the ``swr`` action visualizes the VSWR over the given
+frequency range. Note that both, the ``gain`` and the ``swr`` action
+compute the antenna data over the whole frequency range using NEC and
+that may take some time.
+
+The output of the optimizer is text (usually redirected to a file) that
+prints the evaluation, the VSWR, maximum gain, and forward/backward
+ratio of the best antenna for every 10th generation of the genetic
+algorithm. In addition the command-line options to create that antenna
+are printed. When the genetic algorithm doesn't make any more progress,
+the search terminates and the data of the best evaluation are given. An
+example of the last lines of such a text is as follows. The data is from
+one of the best 2-element antennas was obtained with the random seed 26
+of an earlier version of the program::
+
+    The Best Evaluation: 2.886437e+02.
+    The Best String:
+    -r 0.0364 -d 0.0444 -l 0.1704 -4 0.1075
+    VSWR: [1.7901433511443068, 1.1495780609982815, 1.7995760521232753]
+    GMAX: 6.69913175227, RMAX: -3.03663376703
+    Cache hits: 5670/9243 61.34%
+    Eval: 288.64
+    [ 101011001100101001111000000010011 ]
+
+This tells us the evaluation (which is meaningful only to the
+genetic algorithm), the genetic algorithm *maximizes* this value.
+The command-line options after the line ``The Best String:`` can be used
+to create a ``.nec`` file for that antenna. The antenna in the example
+has a voltage standing wave ratio of < |_| 1.8 at the band ends and
+around 1.15 in the middle of the band (the 70cm band from 430 to
+440 |_| MHz in that case). The forward gain (in the middle of the band)
+is 6.7 |_| dBi. The RMAX value is the (maximum) backward gain (in a 30
+degree area in the back). So the F/B ratio of that antenna is::
+
+ 6.7 dB - -3.0 dB = 9.7 dB
+
+The last line of the text output contains the genetic representation of
+that antenna.
+The ``.nec`` file for the antenna above which was optimized with an early
+version of this package can be created with the command::
+
+ folded_antenna -r 0.0364 -d 0.0444 -l 0.1704 -4 0.1075 necout > folded-opt.nec
+
+The command-line options specify the radius of the folded dipole, the
+distance of the reflector from the folded dipole, the (half) length of
+the reflector, and the (half) length of the straight part of the folded
+dipole, respectively.
+
+According to NEC it has a standing wave ratio (VSWR) of < |_| 1.8 from
+430-440 |_| MHz, a forward gain of > |_| 6.5 dBi over the whole
+frequency range and a Forward/Back Ratio of 8-11 dB.
+
+If you want to implement an optimizer for your own antenna, look at the
+file ``folded.py``: You need to implement a class that defines the
+geometry of the new antenna and an optimizer class that initializes the
+gene ranges and implements a ``compute_antenna`` method that returns an
+instance of your antenna class with the parameters obtained from the
+given gene. All lengths in the models are metric (in meters) as is the
+default in NEC.
+
+A recent addition to this package involves modelling of coax cables.
+This uses information from an old article by Frank Witt [1]_ to derive
+everything necessary to model a transmission line *with* loss from the
+manufacturer cable data. The command-line tool for using these coax
+models is named ``coaxmodel``. Again this command has several
+sub-commands: 
+
+- ``loss``: This displays the fitted loss-curves from the manufacturer
+  data against the curve-fit algorithm used, you can see how much
+  difference in dB the fitted curve has to the loss at certain
+  frequencies given by the manufacturer data.
+- ``match`` computes the impedance at the load and input (depending on
+  which was given as an input the other is computed), the matched and
+  total loss (the matched loss is the loss in the cable if the load is
+  prefectly matched, the total loss is the sum of the matched loss and
+  the additional loss due to reflections), the SWR and data for various
+  stub-matches to get to the cable impedance Z0.
+- ``resonator`` computes the resistance and Q-factor of a coax resonator
+  at the given frequency. A resonator is a piece of cable that either
+  has a short-circuit or an open-circuit at the far end. The sub-command
+  computes resonators for quarter and half wave at the given frequency.
+- ``stub`` computes the length, Q-factor, and resulting impedance as
+  well as the inductance or capacitance of a stub for a given impedance
+  and frequency. The impedance by default is -100j Ohm and can be
+  changed with the -x option. The stub with the shortest resulting
+  length is chosen, so for a negative reactance an open stub is chosen
+  while for a positive reactance a closed stub is chosen.
+
+For all these sub-commands you can specify the frequency, length of
+cable and impedance (either at the load or at the end of the cable) to
+be used in computing the results. You can specify complex impedances as
+a python complex number in the format a+bj, e.g. 50-500j.
+
+Finally the ``transmission_line`` program can optimize the stub-matching
+for a transmission line using NEC. By default a lossless line is asumed.
+Also by default a closed stub at the closest possible position is
+searched.
+
+Transmission lines can be modelled by NEC with the ``TL`` (transmission
+line) card.  But NEC can also model arbitrary (symmetric, passive)
+networks with the ``NT`` (network) card. We use this (and the code in
+``coaxmodel.py``) to model a real cable *with loss* for stub matching.
+It is instructive to compare the values for stub-matching obtained
+analytically from ``coaxmodel`` with the values obtained from an
+optimization with the genetic algorithm by ``transmission_line``. Note
+that the coaxmodel takes frequecies in Hz while transmission_line (which
+uses NEC) accepts frequencies in MHz. So we match a complex impedance of
+75+15j |Ohm| for example::
+
+ coaxmodel -c sytronic_RG_58_CU -f 435e6 -z 75+15j match
+
+This yields a stub of length 8.007 cm attached 7.888 cm from the load when
+matching with a closed stub. When optimizing with ``transmission_line``::
+
+ transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j optimize
+
+we get 8.016cm for the stub length and 7.6cm for the distance of the
+stub from the load. We can visualize this over a given frequency range
+by either producing NEC output::
+
+ transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j -i 50 \
+    -l 0.0816 -d 0.076 --frqstart=430 --frqend=440 necout > x1.nec
+ transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j -i 50 \
+    -l 0.08007 -d 0.07888 --frqstart=430 --frqend=440 necout > x2.nec
+
+And the compute the nec model and display with::
+
+ nec2c -i x1.nec > x1.out
+ nec2c -i x2.nec > x2.out
+ xnecview x1.out
+ xnecview x2.out
+
+Or directly display the VSWR curves with::
+
+ transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j -i 50 \
+    -l 0.0816 -d 0.076 --frqstart=430 --frqend=440 swr
+ transmission_line -c sytronic_RG_58_CU -f 435 -z 75+15j -i 50 \
+    -l 0.08007 -d 0.07888 --frqstart=430 --frqend=440 swr
+
+Both are close enough, the SWR is below 1.1 over the whole frequency
+range given. Note that this can change drastically if load impedances
+with a higher VSWR are matched.
+
+Also note that the NEC files produced in the example above have a different
+NEC network *for each frequency*. This is because NEC models networks
+using an `admittance matrix`_ which is frequency dependent.
+
+This means the sequence of two ``NT``
+cards, a ``TL`` card, a ``FR`` card and a ``RP`` card are repeated for
+each frequency. Here the two ``NT`` cards define the network of the
+cable from the load to the stub and the stub itself while the ``TL``
+card defines the length of a lossless transmission line from the stub to
+the source. The ``FR`` card specifies a single frequency and the ``RP``
+card defines a radiation pattern and triggers computation. This format
+is perfectly valid NEC code, but certain programs (like the popular
+``xnec2c``) cannot deal with this format and display only a single
+frequency.
+
+.. [1] Frank Witt. Transmission line properties from manufacturer’s
+   data. In R. Dean Straw, editor, The ARRL Antenna Compendium, volume 6,
+   pages 179–183. American Radio Relay League (ARRL), 1999.
+
+.. _pgapy:  https://pypi.org/project/PGAPy/
+.. _PGApack: https://github.com/schlatterbeck/pgapack
+.. _PyNEC: https://pypi.org/project/PyNEC/
+.. _`PyNEC source`: https://github.com/tmolteno/python-necpp
+.. _`Numerical Electromagnetics Code`:
+    https://en.wikipedia.org/wiki/Numerical_Electromagnetics_Code
+.. _`admittance matrix`: https://en.wikipedia.org/wiki/Admittance_parameters
+
+Changes
+-------
+
+Version 0.3: Multi-objective optimization
+
+- Switch to pyproject.toml instead of setup.py
+- Add multi-objective optimization
+- Allow NSGA-III for multi-objective optimization
+- Allow to model ground
+- Multiple frequency ranges
+- Allow to use average gain when optimizing. Needs a bug-fix in pynec
+  https://github.com/tmolteno/necpp/pull/73
+- Add epsilon constrained optimization
+  This allows to better find areas with good gain even if constraining
+  the solutions to low SWR
+
+Version 0.2: More cable data
+
+- Fix setup to correctly specify dependencies
+- Add more cable data the following command will list supported cable
+  types::
+
+    coaxmodel --help
+
+Version 0.1: Initial Release
```

### Comparing `antenna-optimizer-0.2/README.html` & `antenna-optimizer-0.3/README.html`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 <?xml version="1.0" encoding="utf-8" ?>
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
 <head>
 <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
-<meta name="generator" content="Docutils 0.14: http://docutils.sourceforge.net/" />
+<meta name="generator" content="Docutils 0.19: https://docutils.sourceforge.io/" />
 <title>Antenna Optimizer</title>
 <style type="text/css">
 
 /*
 :Author: David Goodger
 :Contact: goodger@users.sourceforge.net
 :Date: $Date: 2007-12-21 16:51:22 +0100 (Fri, 21 Dec 2007) $
@@ -377,15 +377,15 @@
 file <tt class="docutils literal">folded.py</tt>: You need to implement a class that defines the
 geometry of the new antenna and an optimizer class that initializes the
 gene ranges and implements a <tt class="docutils literal">compute_antenna</tt> method that returns an
 instance of your antenna class with the parameters obtained from the
 given gene. All lengths in the models are metric (in meters) as is the
 default in NEC.</p>
 <p>A recent addition to this package involves modelling of coax cables.
-This uses information from an old article by Frank Witt <a class="footnote-reference" href="#id2" id="id1">[1]</a> to derive
+This uses information from an old article by Frank Witt <a class="footnote-reference" href="#footnote-1" id="footnote-reference-1">[1]</a> to derive
 everything necessary to model a transmission line <em>with</em> loss from the
 manufacturer cable data. The command-line tool for using these coax
 models is named <tt class="docutils literal">coaxmodel</tt>. Again this command has several
 sub-commands:</p>
 <ul class="simple">
 <li><tt class="docutils literal">loss</tt>: This displays the fitted loss-curves from the manufacturer
 data against the curve-fit algorithm used, you can see how much
@@ -469,24 +469,37 @@
 cable from the load to the stub and the stub itself while the <tt class="docutils literal">TL</tt>
 card defines the length of a lossless transmission line from the stub to
 the source. The <tt class="docutils literal">FR</tt> card specifies a single frequency and the <tt class="docutils literal">RP</tt>
 card defines a radiation pattern and triggers computation. This format
 is perfectly valid NEC code, but certain programs (like the popular
 <tt class="docutils literal">xnec2c</tt>) cannot deal with this format and display only a single
 frequency.</p>
-<table class="docutils footnote" frame="void" id="id2" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-1" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id1">[1]</a></td><td>Frank Witt. Transmission line properties from manufacturer’s
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-1">[1]</a></td><td>Frank Witt. Transmission line properties from manufacturer’s
 data. In R. Dean Straw, editor, The ARRL Antenna Compendium, volume 6,
 pages 179–183. American Radio Relay League (ARRL), 1999.</td></tr>
 </tbody>
 </table>
 <div class="section" id="changes">
 <h1>Changes</h1>
+<p>Version 0.3: Multi-objective optimization</p>
+<ul class="simple">
+<li>Switch to pyproject.toml instead of setup.py</li>
+<li>Add multi-objective optimization</li>
+<li>Allow NSGA-III for multi-objective optimization</li>
+<li>Allow to model ground</li>
+<li>Multiple frequency ranges</li>
+<li>Allow to use average gain when optimizing. Needs a bug-fix in pynec
+<a class="reference external" href="https://github.com/tmolteno/necpp/pull/73">https://github.com/tmolteno/necpp/pull/73</a></li>
+<li>Add epsilon constrained optimization
+This allows to better find areas with good gain even if constraining
+the solutions to low SWR</li>
+</ul>
 <p>Version 0.2: More cable data</p>
 <ul>
 <li><p class="first">Fix setup to correctly specify dependencies</p>
 </li>
 <li><p class="first">Add more cable data the following command will list supported cable
 types:</p>
 <pre class="literal-block">
```

### Comparing `antenna-optimizer-0.2/README.rst` & `antenna-optimizer-0.3/README.rst`

 * *Files 2% similar despite different names*

```diff
@@ -226,14 +226,27 @@
 .. _`Numerical Electromagnetics Code`:
     https://en.wikipedia.org/wiki/Numerical_Electromagnetics_Code
 .. _`admittance matrix`: https://en.wikipedia.org/wiki/Admittance_parameters
 
 Changes
 -------
 
+Version 0.3: Multi-objective optimization
+
+- Switch to pyproject.toml instead of setup.py
+- Add multi-objective optimization
+- Allow NSGA-III for multi-objective optimization
+- Allow to model ground
+- Multiple frequency ranges
+- Allow to use average gain when optimizing. Needs a bug-fix in pynec
+  https://github.com/tmolteno/necpp/pull/73
+- Add epsilon constrained optimization
+  This allows to better find areas with good gain even if constraining
+  the solutions to low SWR
+
 Version 0.2: More cable data
 
 - Fix setup to correctly specify dependencies
 - Add more cable data the following command will list supported cable
   types::
 
     coaxmodel --help
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/coaxmodel.py` & `antenna-optimizer-0.3/antenna_optimizer/coaxmodel.py`

 * *Files 7% similar despite different names*

```diff
@@ -46,15 +46,15 @@
     [9]  Frank Witt. The coaxial resonator match. In Hall [10], pages 110–118.
     [10] Gerald L. (Jerry) Hall, editor. The ARRL Antenna Compendium,
          volume 2. American Radio Relay League (ARRL), 1989.
 
 
 """
 
-class Manufacturer_Data_Cable :
+class Manufacturer_Data_Cable:
     """ From manufacturer data we can interpolate cable parameters. [3]
         Z0: Characteristic impedance of the cable
         vf: velocity factor of the cable
         Cpl: Capacity per length (in F/m, Farad per meter)
         The product of Z0, vf and Cpl is a constant according to Witt [3].
         Consulting Chipman [1] what he calls the "high frequency
         approximation" we have (p. 49) (Note that Chipman uses C for what
@@ -89,34 +89,34 @@
     >>> l.append ((100e6,  4.9  / m_per_ft))
     >>> l.append ((200e6,  7.3  / m_per_ft))
     >>> l.append ((400e6, 11.5  / m_per_ft))
     >>> l.append ((700e6, 17.0  / m_per_ft))
     >>> l.append ((900e6, 20.0  / m_per_ft))
     >>> l.append ((1e9,   21.5  / m_per_ft))
     >>> cable.fit (l)
-    >>> print (cable.summary_loss (metric = False))
-    f (MHz)  Manu   Fit   Diff   (in dB/100 feet)
-          1  0.44  0.41  -0.03
-         10  1.40  1.35  -0.05
-         50  3.30  3.26  -0.04
-        100  4.90  4.88  -0.02
-        200  7.30  7.42   0.12
-        400 11.50 11.55   0.05
-        700 17.00 16.82  -0.18
-        900 20.00 20.02   0.02
-       1000 21.50 21.57   0.07
+    >>> print (cable.summary_loss_data (metric = False))
+    f (MHz)   Manu    Fit   Diff   (in dB/100 feet)
+          1   0.44   0.41  -0.03
+         10   1.40   1.35  -0.05
+         50   3.30   3.26  -0.04
+        100   4.90   4.88  -0.02
+        200   7.30   7.42   0.12
+        400  11.50  11.55   0.05
+        700  17.00  16.82  -0.18
+        900  20.00  20.02   0.02
+       1000  21.50  21.57   0.07
     >>> print ("f0:  %6.2f MHz" % (cable.f0 / 1e6))
     f0:  500.50 MHz
     >>> print ("a0r (f0): %.3f dB/100ft"  % (cable.a0r * m_per_ft))
     a0r (f0): 8.887 dB/100ft
     >>> print ("a0g (f0): %.3f dB/100ft" % (cable.a0g * m_per_ft))
     a0g (f0): 4.511 dB/100ft
     >>> print ("g:   %.4f" % cable.g)
-    g: 0.9990
-    >>> for x in (1, 5, 10, 50, 100, 500, 500.5, 1000, 10000) :
+    g:   0.9990
+    >>> for x in (1, 5, 10, 50, 100, 500, 500.5, 1000, 10000):
     ...    x *= 1e6
     ...    a = cable.loss (x) * m_per_ft
     ...    lr = cable.loss_r (x) * m_per_ft
     ...    lg = cable.loss_g (x) * m_per_ft
     ...    print ("%7.1f %6.2f %5.2f %5.2f" % (x / 1e6, a, lr, lg))
         1.0   0.41  0.40  0.01
         5.0   0.93  0.89  0.05
@@ -144,25 +144,25 @@
     >>> l.append ((400e6, 11.46 / m_per_ft))
     >>> l.append ((700e6, 16.74 / m_per_ft))
     >>> l.append ((900e6, 20.00 / m_per_ft))
     >>> l.append ((1e9,   21.58 / m_per_ft))
     >>> cable.fit (l)
     >>> print ("%.2f" % cable.g)
     1.10
-    >>> print (cable.summary_loss (metric = False))
-    f (MHz)  Manu   Fit   Diff   (in dB/100 feet)
-          1  0.43  0.43  -0.00
-         10  1.39  1.39   0.00
-         50  3.30  3.30   0.00
-        100  4.89  4.89  -0.00
-        200  7.39  7.39  -0.00
-        400 11.46 11.46   0.00
-        700 16.74 16.74  -0.00
-        900 20.00 20.00  -0.00
-       1000 21.58 21.58   0.00
+    >>> print (cable.summary_loss_data (metric = False))
+    f (MHz)   Manu    Fit   Diff   (in dB/100 feet)
+          1   0.43   0.43  -0.00
+         10   1.39   1.39   0.00
+         50   3.30   3.30   0.00
+        100   4.89   4.89  -0.00
+        200   7.39   7.39  -0.00
+        400  11.46  11.46   0.00
+        700  16.74  16.74  -0.00
+        900  20.00  20.00  -0.00
+       1000  21.58  21.58   0.00
     >>> print ("%7.3f" % (cable.fx / 1e6))
     2280.569
     >>> print ("%5.2f" % cable.loss_g (cable.fx))
     66.41
     >>> print ("%5.2f" % cable.loss_r (cable.fx))
     66.41
     >>> z0f = cable.z0f (3e9)
@@ -724,92 +724,92 @@
         ( self
         , Z0
         , vf
         , Cpl       = None
         , use_sabin = False
         , name      = None
         , metric    = True
-        ) :
+        ):
         self.Z0     = Z0
         self.vf     = vf
         self.metric = metric
         self.name   = name or 'custom cable'
-        if Cpl is None :
+        if Cpl is None:
             self.Cpl = 1.0 / (c * Z0 * vf)
-        else :
+        else:
             self.Cpl = Cpl
             self.vf  = 1.0 / (c * Z0 * Cpl)
         self.f0 = self.a0r = self.a0g = self.g = None
         self.use_sabin = use_sabin
     # end def __init__
 
-    def _units (self, metric = True) :
+    def _units (self, metric = True):
         unit = units = 'm'
         cv   = 1.0
-        if metric is None :
+        if metric is None:
             metric = self.metric
-        if not metric :
+        if not metric:
             unit  = 'foot'
             units = 'feet'
             cv    = m_per_ft
         return unit, units, cv
     # end def _units
 
-    def alpha (self, f) :
+    def alpha (self, f):
         """ Attenuation in nepers / m
         """
         return self.loss (f) * np.log (10) / 20 / 100
     # end def alpha
 
-    def beta (self, f) :
+    def beta (self, f):
         """ Phase constant in rad / m
         """
         return 2 * np.pi * f / (c * self.vf)
     # end def beta
 
-    def gamma (self, f = None) :
+    def gamma (self, f = None):
         """ Propagation constant = alpha + j beta
         """
-        if f is None :
+        if f is None:
             f = self.f
         return self.alpha (f) + 1j * self.beta (f)
     # end def gamma
 
-    def loss_r (self, f, a0r = None) :
+    def loss_r (self, f, a0r = None):
         """ Loss due to skin effect (R loss)
         """
         a0r = a0r or self.a0r
         return a0r * np.sqrt (f / self.f0)
     # end def loss_r
 
-    def loss_g (self, f, a0g = None, g = None) :
+    def loss_g (self, f, a0g = None, g = None):
         """ Dieelectric loss
         """
         a0g = a0g or self.a0g
         g   = g   or self.g
         return a0g * (f / self.f0) ** g
     # end def loss_g
 
-    def loss (self, f, a0r = None, a0g = None, g = None) :
+    def loss (self, f, a0r = None, a0g = None, g = None):
         return self.loss_r (f, a0r) + self.loss_g (f, a0g, g)
     # end def loss
 
-    def fit (self, loss_data) :
+    def fit (self, loss_data):
         """ Gets a list of frequency/loss pairs
             Note that the loss is in dB per 100m (not ft)
         """
         self.loss_data = np.array (loss_data)
         self.f0 = (self.loss_data [0][0] + self.loss_data [-1][0]) / 2.0
         x = self.loss_data [:,0]
         y = self.loss_data [:,1]
         popt, pcov = curve_fit (self.loss, x, y)
         self.a0r, self.a0g, self.g = popt
     # end def fit
 
-    def resonator_q (self, f = None) :
+    def resonator_q (self, f = None):
         """ Resonator Q
             loss_dB = a * l / 100 = a * (lambda / 4) / 100
             loss_factor = R * I**2 / R0 * I**2
             loss_factor = 10 ** (loss_dB / 10)
             R = R0 * loss_factor
             lambda = c * vf / F0
             -> R = R0 * (1 - (10 ** (-a * (lambda) / 100 / 10)))
@@ -823,183 +823,183 @@
         >>> cable.set_loss_constants (f, 0.345 / m_per_ft)
         >>> cable.set_freq_params (f, 1, 100, 50)
         >>> print ("%.4f" % cable.loss (f))
         1.1319
         >>> print ("%.4f" % cable.resonator_q ())
         47.9411
         """
-        if f is None :
+        if f is None:
             f = self.f
         return 2 * np.pi \
             / (1 - 10 ** (-self.loss (f) * c * self.vf / (1000 * f)))
     # end def resonator_q
 
-    def resonator_q_approx (self, f = None) :
+    def resonator_q_approx (self, f = None):
         """ Approximate formula from Chipman [1] p. 222 Eq 10.20
         >>> f = 3670830.9685955304
         >>> cable = Manufacturer_Data_Cable (50, 0.66)
         >>> cable.set_loss_constants (f, 0.345 / m_per_ft)
         >>> cable.set_freq_params (f, 1, 100, 50)
         >>> print ("%.1f" % cable.resonator_q_approx (f))
         44.7
         """
-        if f is None :
+        if f is None:
             f = self.f
         return self.beta (f) / (2 * self.alpha (f))
     # end def resonator_q_approx
 
-    def reactance_q (self, f = None, l = None) :
+    def reactance_q (self, f = None, l = None):
         """ This is from Terman [8] p. 193 (73)
         """
-        if f is None :
+        if f is None:
             f = self.f
-        if l is None :
+        if l is None:
             l = self.l
         phi = 2 * np.pi * (l / self.lamda (f))
         return self.resonator_q (f) * np.sin (2 * phi) / phi
     # end def reactance_q
 
-    def set_loss_constants (self, f0, a0r, a0g = 0) :
+    def set_loss_constants (self, f0, a0r, a0g = 0):
         """ Alternative to fit if we have less data, allows to specify
             a0r (and optionally a0g) for a single frequency.
         """
         self.f0  = f0
         self.a0r = a0r
         self.a0g = a0g
         self.g   = 1.0
     # end def set_loss_constants
 
-    def set_freq_params (self, f, l, p, z_l = None, z_i = None) :
+    def set_freq_params (self, f, l, p, z_l = None, z_i = None):
         self.f = f
         self.l = l
         self.p = p
         assert z_l or z_i
         assert not (z_l and z_i)
-        if z_l is not None :
+        if z_l is not None:
             self.z_l = complex (z_l)
             self.z_i = self.z_d (f, l, z_l)
-        elif z_i is not None :
+        elif z_i is not None:
             self.z_i = complex (z_i)
             self.z_l = self.z_load (l, f, z_i)
     # end def set_freq_params
 
-    def freq (self, l) :
+    def freq (self, l):
         """ Frequency at given length lambda
         """
         return c * self.vf / l
     # end def freq
 
     @property
-    def fx (self) :
+    def fx (self):
         """ Frequency where the impedance is real.
             This is the point where loss_g and loss_r are equal.
         """
         return self.f0 * (self.a0r / self.a0g) ** (1.0 / (self.g - .5))
     # end def fx
 
     @property
-    def L (self) :
+    def L (self):
         return self.Cpl * self.Z0 ** 2
     # end def L
 
     @property
-    def P_l (self) :
+    def P_l (self):
         return abs (self.U_l) ** 2 * (1.0 / self.z_l).real
     # end def P_l
 
     @property
-    def combined_loss (self) :
+    def combined_loss (self):
         return 10 * np.log (self.p / self.P_l) / np.log (10)
     # end def combined_loss
 
     @property
-    def U_i (self) :
+    def U_i (self):
         return np.sqrt (self.p / (1.0 / self.z_i).real)
     # end def U_i
 
     @property
-    def U_l (self) :
+    def U_l (self):
         u = self.U_i
         z0 = self.z0f   ()
         gm = self.gamma ()
         zi = self.z_i
         return u * (np.cosh (gm * self.l) - z0 / zi * np.sinh (gm * self.l))
     # end def U_l
 
     @property
-    def U_max (self) :
+    def U_max (self):
         """ Maximum voltage given p
         """
         return np.sqrt (self.p * self.Z0) * np.sqrt (self.vswr_i)
     # end def U_max
 
     @property
-    def I_max (self) :
+    def I_max (self):
         """ Maximum current given p
         """
         return np.sqrt (self.p * self.vswr_i / self.Z0)
     # end def I_max
 
     @property
-    def rho_l (self) :
+    def rho_l (self):
         return (self.z_l - self.Z0) / (self.z_l + self.Z0)
     # end def rho_l
 
     @property
-    def vswr_l (self) :
+    def vswr_l (self):
         return (1 + abs (self.rho_l)) / (1 - abs (self.rho_l))
     # end def vswr_l
 
     @property
-    def rho_i (self) :
+    def rho_i (self):
         return (self.z_i - self.Z0) / (self.z_i + self.Z0)
     # end def rho_i
 
     @property
-    def vswr_i (self) :
+    def vswr_i (self):
         return (1 + abs (self.rho_i)) / (1 - abs (self.rho_i))
     # end def vswr_i
 
-    def lamda (self, f = None) :
-        if f is None :
+    def lamda (self, f = None):
+        if f is None:
             f = self.f
         return 2 * np.pi / self.beta (f)
     # end def lamda
 
-    def phi (self, f = None, l = None) :
+    def phi (self, f = None, l = None):
         """ Electrical length at given frequency (in rad)
         """
-        if f is None :
+        if f is None:
             f = self.f
-        if l is None :
+        if l is None:
             l = self.l
         return self.beta (f) * l
     # end def phi
 
-    def conductance (self, f = None, z0 = None) :
-        if f is None :
+    def conductance (self, f = None, z0 = None):
+        if f is None:
             f = self.f
         ln10 = np.log (10)
-        if z0 is None :
+        if z0 is None:
             z0 = self.Z0
         g = self.loss_g (f) * ln10 * z0.real / (1000.0 * abs (z0) ** 2)
         return g
     # end def conductance
 
-    def resistance (self, f = None, z0 = None) :
-        if f is None :
+    def resistance (self, f = None, z0 = None):
+        if f is None:
             f = self.f
         ln10 = np.log (10)
-        if z0 is None :
+        if z0 is None:
             z0 = self.Z0
         r = self.loss_r (f) * ln10 * z0.real / 1000.0
         return r
     # end def resistance
 
-    def summary (self, f, l, metric = True) :
+    def summary (self, f, l, metric = True):
         unit, units, cv = self._units (metric)
         ohm = '\u3a09'
         ohm = '\u2126'
         lm  = '\u03bb'
         mu  = '\u03bc'
         r = []
         z0f = self.z0f (f)
@@ -1058,46 +1058,59 @@
             ( '%25s %.3f dB'
             % ('Matched Loss', self.loss (f) / 100 * l)
             )
 
         return '\n'.join (r)
     # end def summary
 
-    def summary_loss (self, metric = True) :
+    def summary_loss_data (self, metric = True):
         """ Return summary of loss parameters (from match and from
             manufacturer data)
         """
         r = []
         unit, units, cv = self._units (metric)
-        r.append ("f (MHz)  Manu   Fit   Diff   (in dB/100 %s)" % units)
-        for x, y in self.loss_data :
-           y = y * cv
-           a = self.loss (x) * cv
-           r.append ("   %4.0f %5.2f %5.2f %6.2f" % (x / 1e6, y, a, (a - y)))
+        r.append ("f (MHz)   Manu    Fit   Diff   (in dB/100 %s)" % units)
+        for x, y in self.loss_data:
+            y = y * cv
+            a = self.loss (x) * cv
+            r.append ("   %4.0f %6.2f %6.2f %6.2f" % (x / 1e6, y, a, (a - y)))
+        return '\n'.join (r)
+    # end def summary_loss_data
+
+    def summary_loss (self, metric = True):
+        r = []
+        unit, units, cv = self._units (metric)
+        r.append ("f (MHz)  Loss  (in dB/100 %s)" % units)
+        frq = [ 10e6, 20e6, 50e6, 100e6, 200e6, 300e6, 500e6, 800e6, 1e9
+              , 2.4e9, 5e9, 10e9, 20e9
+              ]
+        for f in frq:
+            a = self.loss (f) * cv
+            r.append ("  %5.0f %8.2f" % (f / 1e6, a))
         return '\n'.join (r)
     # end def summary_loss
 
     def summary_match \
         ( self
         , f      = None
         , l      = None
         , p      = None
         , z_l    = None
         , z_i    = None
         , metric = True
-        ) :
+        ):
         """ Return summary of matching parameters, this asumes that
             self.f, self.l, self.p and either self.z_l or self.z_i have
             been set.
         """
-        if f is None :
+        if f is None:
             f = self.f
-        if l is None :
+        if l is None:
             l = self.l
-        if p is None :
+        if p is None:
             p = self.p
         z_l = self.z_l
         z_i = self.z_i
         unit, units, cv = self._units (metric)
         ohm = '\u2126'
         r = []
         r.append \
@@ -1137,23 +1150,23 @@
         #r.append \
         #    ( '%25s %.2f W per %s'
         #    % ('Maximum Power Stress'
         #      , self.I_max ** 2 * self.resistance ()
         #      , unit
         #      )
         #    )
-        for is_cap in True, False :
-            for is_short in True, False :
+        for is_cap in True, False:
+            for is_short in True, False:
                 sd, sl = self.stub_match_iterative (is_cap, is_short)
                 zi     = self.stub_impedance (f, sd, sl, self.z_l, is_short)
                 type   = 'Inductive'
                 circ   = 'open'
-                if not is_cap :
+                if not is_cap:
                     type = 'Capacitive'
-                if is_short :
+                if is_short:
                     circ = 'short'
                 r.append ('%s stub with %s circuit at end:' % (type, circ))
                 r.append \
                     ( '%25s %.5f %s from load'
                     % ('Stub attached', sd / cv, units)
                     )
                 r.append ('%25s %.5f %s' % ('Stub length', sl / cv, units))
@@ -1161,17 +1174,17 @@
                     ( '%25s %.2f %+.2fj'
                     % ('Resulting impedance', zi.real, zi.imag)
                     )
 
         return '\n'.join (r)
     # end def summary_match
 
-    def summary_resonator (self, f = None, metric = True) :
+    def summary_resonator (self, f = None, metric = True):
         unit, units, cv = self._units (metric)
-        if f is None :
+        if f is None:
             f = self.f
         r = []
         l = self.lamda (f)
         r.append ("Series Resonator at %.2f MHz" % (self.f / 1e6))
         r.append ("Open circuited quarter wave:")
         r.append ("%8s: %.3f %s" % ('Length', l / 4 / cv, units))
         r.append \
@@ -1192,34 +1205,34 @@
         r.append ("%8s: %.3f %s" % ('Length', l / 2 / cv, units))
         r.append \
             ("%8s: %.3f \u2126" % ('abs (z)', abs (self.z_d_open (f, l/2))))
         r.append ("%8s: %.3f" % ('Q', self.resonator_q (f)))
         return '\n'.join (r)
     # end def summary_resonator
 
-    def summary_stub (self, f = None, reactance = None, metric = True) :
-        if f is None :
+    def summary_stub (self, f = None, reactance = None, metric = True):
+        if f is None:
             f = self.f
-        if reactance is None :
+        if reactance is None:
             reactance = self.reactance
         z = reactance
         unit, units, cv = self._units (metric)
         self.f = f
         r = []
-        if z.imag :
+        if z.imag:
             z = z.imag
-        if z < 0 :
+        if z < 0:
             r.append ('Capacitive impedance %.2f \u2126' % z)
             r.append ('Open-Circuited')
             l = self.stub_open (z)
             z = self.z_d_open (f, l)
             a = 'C'
             u = 'pF'
             v = 1 / (2 * np.pi * f * (-z.imag)) * 1e12
-        else :
+        else:
             r.append ('Inductive impedance %.2f \u2126' % z)
             r.append ('Closed-Circuited')
             l = self.stub_short (z)
             z = self.z_d_short (f, l)
             a = 'L'
             u = 'µH'
             v = z.imag / (2 * np.pi * f) * 1e6
@@ -1229,35 +1242,35 @@
         r.append ("%11s: %.2f" % ('Q', self.reactance_q (f, l)))
         return '\n'.join (r)
     # end def summary_stub
 
     # The Y-Parameters (Admittance Parameters)
     # These are needed for simulating a lossy cable in NEC
 
-    def y11 (self, f, l) :
+    def y11 (self, f, l):
         """ Admittance Parameter Y11: This is simply the reciprocal
             value of z_d_short for the given f and l. Note that for an
             unterminated cable Y11 = Y22. See Wikipedia
             https://en.wikipedia.org/wiki/Admittance_parameters
         """
         return 1.0 / self.z_d_short (f, l)
     # end def y11
 
-    def y22 (self, f, l, z_l = None) :
+    def y22 (self, f, l, z_l = None):
         """ Admittance Parameter Y22: This simply adds 1/z_l in parallel
             to y11. Default value for z_l is open circuit.
         """
-        if z_l is None :
+        if z_l is None:
             return self.y11 (f, l)
-        elif z_l == 0 :
+        elif z_l == 0:
             return 1e50
         return 1.0 / z_l + self.y11 (f, l)
     # end def y22
 
-    def y12 (self, f, l) :
+    def y12 (self, f, l):
         """ Admittance Parameter Y12: Since this is a reciprocal network
             Y12 = Y21.
             Y_in = Y11 - Y12 ** 2 / (Y22 + Y_L)
             Where Y_L is the load admittance and Y_in is the admittance to
             be measured at the input. We can compute Y_in from Y_L using
             self.z_d, from this we can compute Y12.
             Y12 = +/- sqrt (Y11 * (Y_L + Y22) - Y_in * (Y_L + Y22))
@@ -1265,35 +1278,35 @@
             See Wikipedia https://en.wikipedia.org/wiki/Admittance_parameters
             Note that we set Y_L to 0 (open circuit) to compute the
             cable parameter y12 and we set y11 = y22.
         """
         y_in = 1 / self.z_d_open (f, l)
         y11  = self.y11 (f, l)
         r    = np.sqrt (y11 ** 2 - y_in * (y11))
-        if r.real < 0 :
+        if r.real < 0:
             return -r
         return r
     # end def y12
 
-    def z0f_witt (self, f, z0, r, g) :
+    def z0f_witt (self, f, z0, r, g):
         """ From Witt [3]
         """
         cpart = 2j * np.pi * f * self.Cpl
         return np.sqrt ((r + cpart * z0 ** 2) / (g + cpart))
     # end def z0f_witt
 
-    def z0f_sabin (self, f, z0, r, g) :
+    def z0f_sabin (self, f, z0, r, g):
         """ From Sabin [6] p.4:
         """
         l = self.Cpl * z0 ** 2
         o2 = 4 * np.pi * f
         return z0.real * (1 - 1j * (r / (o2 * l) - g / (o2 * self.Cpl)))
     # end def z0f_sabin
 
-    def z0f (self, f = None, z0 = None) :
+    def z0f (self, f = None, z0 = None):
         """ Characteristic impedance X_0f for a given frequency
             *without* the high-frequency approximation. We have from
             Chipman [1] Formula 4.12 p.32:
             Z_0 = sqrt ((R + j omega L) / (G + j omega C))
             And from the high-frequency approximation we have
             Z0 = sqrt (L/C)
             Solving for L:
@@ -1316,89 +1329,89 @@
             Witt tells us [3] can use this to compute Z_0 (f)
             iteratively, this apparently is not true, it diverges on
             repeated iteration.
             Another formula from Sabin [6] (which is non-iterative)
             yields almost the same result as the non-iterated formula of
             Witt [3]
         """
-        if f is None :
+        if f is None:
             f = self.f
-        if z0 is None :
+        if z0 is None:
             z0 = self.Z0
         r = self.resistance  (f, z0)
         g = self.conductance (f, z0)
-        if self.use_sabin :
+        if self.use_sabin:
             return self.z0f_sabin (f, z0, r, g)
         return self.z0f_witt  (f, z0, r, g)
     # end def z0f
 
-    def plot_z0f (self, f) :
+    def plot_z0f (self, f):
         """ Since Witt [3] tells us that the z0_f formula above can be
             iterated, this plots the absolute value of the difference of
             an input z0 with an output z0. It clearly shows this diverges.
         """
         x = np.arange (-1.5, 1.5, 0.02)
         y = np.arange (49-0.5, 51+0.5, 0.02)
         z = []
-        for vx in x :
+        for vx in x:
             zz = []
             z.append (zz)
-            for vy in y :
+            for vy in y:
                 z0  = 50 + 0j
                 z0f = self.z0f (f, vy + vx*1j)
                 zz.append (abs (z0 - z0f))
                 #zz.append ((z0 - z0f).real)
                 #zz.append ((z0 - z0f).imag)
         z    = np.array (z)
         x, y = np.meshgrid (x, y)
         fig  = plt.figure ()
         ax   = fig.add_subplot (111, projection = '3d')
         ax.plot_wireframe (x, y, z)
         plt.show ()
     # end def plot_z0f
 
-    def _stub_match_iter (self, d, y, goal = None) :
+    def _stub_match_iter (self, d, y, goal = None):
         """ Find better approximation of d with a binary search
         """
-        if goal is None :
+        if goal is None:
             goal = 1.0 / self.Z0
         # Preconditions for binary search, current value is valid
         assert y.imag != 0
         v = abs ((1.0 / self.z_d (self.f, d, self.z_l)).real - y.real)
         assert v < eps ** 2
         dir = np.sign (y.real - goal)
         du  = d + self.lamda () / 50.
         dl  = d - self.lamda () / 50.
         zu  = (1.0 / self.z_d (self.f, du, self.z_l)).real
         zl  = (1.0 / self.z_d (self.f, dl, self.z_l)).real
         yr  = y.real
-        if np.sign (zu - y.real) == dir :
+        if np.sign (zu - y.real) == dir:
             du = d
             zu = y.real
-        else :
+        else:
             assert np.sign (zl - y.real) == dir
             dl = d
             zl = y.real
-        for k in range (100) :
-            if abs (yr - goal) / goal < 1e-3 :
+        for k in range (100):
+            if abs (yr - goal) / goal < 1e-3:
                 break
             d  = (dl + du) / 2.
             y  = 1.0 / self.z_d (self.f, d, self.z_l)
             yr = y.real
-            if yr > goal :
+            if yr > goal:
                 du = d
                 zu = yr
-            else :
+            else:
                 dl = d
                 zl = yr
         #print ("  corrected: d: %.3f y:%.6f %+.6f" % (d, y.real, y.imag))
         return d, y
     # end def _stub_match_iter
 
-    def stub_match (self, capacitive = True) :
+    def stub_match (self, capacitive = True):
         """ Distance *from load* of stub match point and impedance to be
             matched.
             We first compute the point from the voltage minimum and then
             add the distance from the load to the voltage minimum.
             In the example by Chipman [1] p. 178 (problem 8.3) the matching
             point nearer to the load is the shorter one with
             short-circuit termination. We don't count on this, we
@@ -1421,125 +1434,125 @@
         # unless capacitive is False in which case we return the other
         # one.
         dmin = self.d_voltage_min ()
         #print ("d_v:", d_v)
         #print ("wl d_v:", d_v / self.lamda ())
         #print ("dmin:", dmin)
         D = []
-        for x in (dmin + d_v, dmin - d_v) :
-            if x / self.lamda () > 0.5 :
+        for x in (dmin + d_v, dmin - d_v):
+            if x / self.lamda () > 0.5:
                 D.append (x - self.lamda () / 2.0)
-            elif x < 0 :
+            elif x < 0:
                 D.append (x + self.lamda () / 2.0)
-            else :
+            else:
                 D.append (x)
         assert len (D) == 2
         #print (D)
         Y = [1.0 / self.z_d (self.f, x, self.z_l) for x in D]
         #print (Y)
         d = D [0]
-        for n, y in enumerate (Y) :
+        for n, y in enumerate (Y):
             #print (y)
-            if capacitive :
-                if y.imag > 0 :
+            if capacitive:
+                if y.imag > 0:
                     d = D [n]
                     break
-            else :
-                if y.imag < 0 :
+            else:
+                if y.imag < 0:
                     d = D [n]
                     break
         #print ("uncorrected: d: %.3f y:%.6f %+.6f" % (d, y.real, y.imag))
         return self._stub_match_iter (d, y)
     # end def stub_match
 
-    def _stub_match_step (self, d, shortcircuit) :
+    def _stub_match_step (self, d, shortcircuit):
         z = self.z_d (self.f, d, self.z_l)
         l = self.stub_short_open_iter (-z, shortcircuit = shortcircuit)
         y = 1.0 / self.stub_impedance \
             (self.f, d, l, self.z_l, shortcircuit = shortcircuit)
         return z, l, y
     # end def _stub_match_step
 
-    def stub_match_iterative (self, capacitive = True, shortcircuit = True) :
+    def stub_match_iterative (self, capacitive = True, shortcircuit = True):
         """ Perform iterative matching: Compute the best match with
             y.real = 1/Z0, then compute the stub length and the
             resulting impedance. Iterate if the goal is not reached.
         """
         goal = (1.0 / self.Z0).real
         dmin = self.d_voltage_min ()
         d, ym = self.stub_match (capacitive = capacitive)
         l  = self.stub_short_open_iter (-1/ym, shortcircuit = shortcircuit)
         y  = 1.0 / self.stub_impedance \
             (self.f, d, l, self.z_l, shortcircuit = shortcircuit)
         dl  = d - self.lamda () / 30
-        if d > dmin and dl < dmin :
+        if d > dmin and dl < dmin:
             dl = dmin + eps
         zl, ll, yl = self._stub_match_step (dl, shortcircuit)
         du  = d + self.lamda () / 30
-        if d < dmin and du > dmin :
+        if d < dmin and du > dmin:
             du = dmin - eps
         zu, lu, yu = self._stub_match_step (du, shortcircuit)
         # Both values on the same side of y?
         # Code currently not triggered by any test.
         # But it triggers when dmin-limit code above is disabled
-        if np.sign (y.real - yl.real) == np.sign (y.real - yu.real) :
+        if np.sign (y.real - yl.real) == np.sign (y.real - yu.real):
             # Sort-of lim (yl.real -> y.real) and lim (yu.real -> y.real)
             dleps = d - eps
             zleps, lleps, yleps = self._stub_match_step (dleps, shortcircuit)
             ylr = yleps.real
             dueps = d + eps
             zueps, lueps, yueps = self._stub_match_step (dueps, shortcircuit)
             yur = yueps.real
             assert np.sign (y.real - ylr) != np.sign (y.real - yur)
-            if np.sign (y.real - ylr) != np.sign (y.real - yl.real) :
+            if np.sign (y.real - ylr) != np.sign (y.real - yl.real):
                 s  = np.sign (y.real - yl.real)
                 dn = dl
                 vn = 'l'
-            else :
+            else:
                 assert np.sign (y.real - yur) != np.sign (y.real - yu.real)
                 s  = np.sign (y.real - yu.real)
                 dn = du
                 vn = 'u'
-            for i in range (20) :
+            for i in range (20):
                 dn = (d + dn) / 2
                 zn, ln, yn = self._stub_match_step (dn, shortcircuit)
-                if np.sign (y.real - yn) != s :
+                if np.sign (y.real - yn) != s:
                     break
-            else :
+            else:
                 assert 0
-            if vn == 'l' :
+            if vn == 'l':
                 dl, zl, ll, yl = dn, zn, ln, yn
-            else :
+            else:
                 du, zu, lu, yu = dn, zn, ln, yn
 
-        if yl.real > y.real :
+        if yl.real > y.real:
             yl, yu = yu, yl
             ll, lu = lu, ll
             dl, du = du, dl
 
-        for i in range (200) :
-            if abs (y.real - goal) < eps :
+        for i in range (200):
+            if abs (y.real - goal) < eps:
                 break
-            if y.real > goal :
+            if y.real > goal:
                 yu = y
                 lu = l
                 du = d
-            else :
+            else:
                 yl = y
                 ll = l
                 dl = d
             d = (dl + du) / 2.0
             z = self.z_d (self.f, d, self.z_l)
             l = self.stub_short_open_iter (-z, shortcircuit = shortcircuit)
             y = 1.0 / self.stub_impedance \
                 (self.f, d, l, self.z_l, shortcircuit = shortcircuit)
         return d, l
     # end def stub_match_iterative
 
-    def stub_short (self, z, f = None) :
+    def stub_short (self, z, f = None):
         """ Compute length of a short-circuited (closed) stub that has
             the given reactance as the imaginary part of a complex number.
             phi = 2*pi*d / lamda
             Formula from Chipman [1] p.131 (7.21)
             from Johnson [7] p.155 (6.21) and Terman [8] p.192 (72)
             z = j*z0 * tan (phi)
             j * tan (phi) = z / z0
@@ -1576,88 +1589,88 @@
         >>> print ("%.5f" % cable.stub_short (z = -53.4j))
         0.39522
         >>> print ("%.5f" % cable.stub_short (z = 53.4))
         0.09944
         >>> print ("%.5f" % cable.stub_short (z = 53.4j))
         0.09944
         """
-        if f is None :
+        if f is None:
             f = self.f
-        if z.imag :
+        if z.imag:
             z = z.imag
         z /= self.Z0
         phi = np.arctan (z)
-        if phi < 0 :
+        if phi < 0:
             phi += np.pi
         return self.lamda (f) * phi / (2 * np.pi)
     # end def stub_short
 
-    def stub_short_open_iter (self, z, f = None, shortcircuit = True) :
+    def stub_short_open_iter (self, z, f = None, shortcircuit = True):
         """ Iterative method of computing the matching impedance
             We search for the stub length where the imaginary part most
             closely matches the given admittance 1/(z*j).
         """
         stubmethod = self.stub_open
         z_d_method = self.z_d_open
-        if shortcircuit :
+        if shortcircuit:
             stubmethod = self.stub_short
             z_d_method = self.z_d_short
-        if z.imag :
+        if z.imag:
             goal = (1/z).imag
-        else :
+        else:
             goal = (1.0 / (z * 1j)).imag
 
         l = stubmethod (-1/goal, f)
         f = f or self.f
         assert 0 <= l <= self.lamda (f) / 2
         y   = 1.0 / z_d_method (f, l)
         ll  = l - self.lamda (f) / 50.0
         lu  = l + self.lamda (f) / 50.0
-        if 0 <= l < self.lamda (f) / 4 :
-            if ll < 0 :
+        if 0 <= l < self.lamda (f) / 4:
+            if ll < 0:
                 ll = eps
-            if lu >= self.lamda (f) / 4.0 :
+            if lu >= self.lamda (f) / 4.0:
                 lu = self.lamda (f) / 4.0 - eps
-        else :
+        else:
             assert self.lamda (f) / 4.0 <= l <= self.lamda (f) / 2.0
-            if ll <= self.lamda (f) / 4.0 :
+            if ll <= self.lamda (f) / 4.0:
                 ll = self.lamda (f) / 4.0 + eps
-            if lu >= self.lamda (f) / 2.0 :
+            if lu >= self.lamda (f) / 2.0:
                 lu = self.lamda (f) / 2.0 - eps
         yl = 1.0 / z_d_method (f, ll)
         yu = 1.0 / z_d_method (f, lu)
-        if yl.imag > goal :
+        if yl.imag > goal:
             yl, yu = yu, yl
             ll, lu = lu, ll
-        for i in range (200) :
-            if abs (y.imag - goal) < eps**2 :
+        for i in range (200):
+            if abs (y.imag - goal) < eps**2:
                 break
-            if y.imag > goal :
+            if y.imag > goal:
                 lu = l
                 yu = y
-            else :
+            else:
                 ll = l
                 yl = y
             l = (ll + lu) / 2.0
             y = 1.0 / z_d_method (f, l)
         return l
     # end def stub_short_open_iter
 
-    def stub_short_iter (self, z, f = None) :
+    def stub_short_iter (self, z, f = None):
         """ Note: The iterative variant tries to optimize the susceptance
             part of y = 1/z (y.imag) to be as exactly as possible.
             This will sometimes yield worse results if we're aiming for
             a close *reactance* (z.imag) match. The iterative version is
             mostly used for (parallel) stub matching where we want to
             eliminate the susceptance part as closely as possible.
         """
         return self.stub_short_open_iter (z, f, shortcircuit = True)
     # end def stub_short_iter
 
-    def stub_open (self, z, f = None) :
+    def stub_open (self, z, f = None):
         """ Compute length of an open-circuit stub that has the given
             reactance as the imaginary part of a complex number.
             phi = 2*pi*d / lamda
             Formula from Chipman [1] p.131 (7.22)
             z = -j*z0 * cot phi
             from Johnson [7] p.160 (6.24), same from Terman [8] p.192 (72)
             z = -j*z0 / tan phi
@@ -1706,55 +1719,55 @@
         >>> cable.set_loss_constants (f, 10.6)
         >>> cable.set_freq_params (f, 1, 100, 73)
         >>> print ("%.5f" % cable.stub_open (z = -1 / 0.025))
         0.09262
         >>> print ("%.5f" % cable.stub_open (z = 1 / 0.025j))
         0.09262
         """
-        if f is None :
+        if f is None:
             f = self.f
-        if z.imag :
+        if z.imag:
             z = z.imag
         z /= -self.Z0
-        if z == 0 :
+        if z == 0:
             return self.lamda () / 4
         phi = np.arctan (1.0 / z)
-        if phi < 0 :
+        if phi < 0:
             phi += np.pi
         return self.lamda (f) * phi / (2 * np.pi)
     # end def stub_open
 
-    def stub_open_iter (self, z, f = None) :
+    def stub_open_iter (self, z, f = None):
         """ Note: The iterative variant tries to optimize the susceptance
             part of y = 1/z (y.imag) to be as exactly as possible.
             This will sometimes yield worse results if we're aiming for
             a close *reactance* (z.imag) match. The iterative version is
             mostly used for (parallel) stub matching where we want to
             eliminate the susceptance part as closely as possible.
         """
         return self.stub_short_open_iter (z, f, shortcircuit = False)
     # end def stub_open_iter
 
-    def stub_impedance (self, f, stub_d, stub_l, z_l, shortcircuit = True) :
+    def stub_impedance (self, f, stub_d, stub_l, z_l, shortcircuit = True):
         """ Compute stub impedance with distance from load stub_d and
             stub length stub_l and load impedance z_l. By default a
             closed (short circuit) stub is assumed.
         """
         #print (z_l)
         z_i = self.z_d (f, stub_d, z_l)
         #print (1/z_i)
         method = self.z_d_short
-        if not shortcircuit :
+        if not shortcircuit:
             method = self.z_d_open
         z_s = method (f, stub_l)
         #print (1/z_s)
         return 1.0 / ((1.0 / z_i) + (1.0 / z_s))
     # end def stub_impedance
 
-    def d_voltage_min (self, zd = None) :
+    def d_voltage_min (self, zd = None):
         """ Compute the (approximate) distance d from load where the
             impedance is real. We use vswr_l for this and postulate that
             the magnitude is the same as at the load (so we're assuming a
             lossless line here). At this point everything is real (no
             imaginary part). There are two solutions, one at voltage
             maximum, one at current maximum.  We return the one at
             current maximum (voltage minimum). Optionally we allow to
@@ -1764,72 +1777,72 @@
         zl  = self.z_l
         zd  = zd or 1 / self.vswr_l * z0 # voltage minimum
         nom = (zl - z0) * zd + z0 * zl - z0 ** 2
         den = (zl + z0) * zd - z0 * zl - z0 ** 2
         ep  = np.sqrt (nom / den)
         a1  = np.angle (ep)
         a2  = np.angle (-ep)
-        if a1 < 0 :
+        if a1 < 0:
             a1 += 2 * np.pi
-        if a2 < 0 :
+        if a2 < 0:
             a2 += 2 * np.pi
         a = a1 if a1 < a2 else a2
         return a / 2 / np.pi * self.lamda ()
     # end def d_voltage_min
 
-    def z_d (self, f, d, z_l) :
+    def z_d (self, f, d, z_l):
         """ Compute impedance at distance d from load, given load
             impedance z_l, Eq 24 from [6] p.7 or better (exponential
             form) from 7.15 [1] p.130
             Special case z_l = None is open circuit.
             Note that we may return None for an open circuit if too near
             the load.
         """
         z0 = self.z0f   (f)
         gm = self.gamma (f)
         ep = np.e ** (gm * d)
-        if abs (d) < 1e-20 :
+        if abs (d) < 1e-20:
             return z_l
-        if z_l is None :
+        if z_l is None:
             return z0 * (ep + 1/ep) / (ep - 1/ep)
         zz = z_l / z0
         return z0 * ( (ep * (zz + 1) + (zz - 1) / ep)
                     / (ep * (zz + 1) - (zz - 1) / ep)
                     )
     # end def z_d
 
-    def z_d_open (self, f, d) :
+    def z_d_open (self, f, d):
         """ Same as z_d but for open circuit (infinite z_l)
         """
         return self.z_d (f, d, z_l = None)
     # end def z_d_open
 
-    def z_d_short (self, f, d) :
+    def z_d_short (self, f, d):
         """ Same as z_d but for short circuit (z_l = 0)
         """
         return self.z_d (f, d, z_l = 0.0)
     # end def z_d_short
 
-    def z_load (self, d, f = None, z_i = None) :
+    def z_load (self, d, f = None, z_i = None):
         """ Compute impedance at load from input impedance given length
         """
-        if f is None :
+        if f is None:
             f = self.f
-        if z_i is None :
+        if z_i is None:
             z_i = self.z_i
         z0 = self.z0f (f)
         gm = self.gamma (f)
         ep = np.e ** (gm * d)
         return -((z0 * z_i - z0**2) * ep**2 + z0 * z_i + z0**2) \
                 / ((z_i - z0) * ep**2 - z_i - z0)
     # end def z_load
 
 # end class Manufacturer_Data_Cable
 
-class Measured_Cable :
+class Measured_Cable:
     """ By measuring cable impedance (both R and X) for open and closed
         circuit we can compute other cable paramters. The measurements
         should be made on a line with length close to lambda/8 or an odd
         multiple of it. [4,2]
         Doctests are from Maxwell [2] p.15-3
 
     >>> mc = Measured_Cable (1.9e6, 1, 2.0, 0.6, 50.0, -48.5)
@@ -1860,15 +1873,15 @@
     >>> mc = Measured_Cable (5.7e6, 1, 1.9, 2.58, -48.42, 49.47)
     >>> print ("%.3f" % abs (mc.zc))
     48.994
     >>> print ("%.3f" % (np.angle (mc.zc) / np.pi * 180))
     -0.369
     """
 
-    def __init__ (self, f0, length, r_sc, r_oc, x_sc = 0, x_oc = 0) :
+    def __init__ (self, f0, length, r_sc, r_oc, x_sc = 0, x_oc = 0):
         self.f0     = f0
         self.length = length
         self.z_sc   = r_sc + 1j * x_sc
         self.z_oc   = r_oc + 1j * x_oc
         # See Chipman formula (7.27)
         self.zc     = np.sqrt (self.z_sc * self.z_oc)
         # Seems atanh can't deal with complex numbers
@@ -1877,23 +1890,23 @@
         #self.lamda  = 2 * np.pi / self.beta
         #self.phi    = length / self.lamda * 2 * np.pi
         #alpha       = gamma.
     # end def __init__
 
 # end class Measured_Cable
 
-def admittance (y11, y12, y22, z_l) :
+def admittance (y11, y12, y22, z_l):
     """ Given the admittance matrix for a cable (note that y12 = y21)
         compute z_i from z_l.
     """
-    if z_l == 0 :
+    if z_l == 0:
         return y11
-    if z_l is None :
+    if z_l is None:
         y_l = 0
-    else :
+    else:
         y_l = 1.0 / z_l
     return y11 - (y12 ** 2) / (y22 + y_l)
 # end def admittance
 
 # Definining new cable parameters:
 # We make a list of attenuation per 100m
 # Then we call the constructor of Measured_Cable with
@@ -1962,15 +1975,15 @@
 sytronic_RG_58_C_U = Manufacturer_Data_Cable \
     (50, .66, 103e-12, name = 'SYTRONIC RG 58 C/U')
 sytronic_RG_58_C_U.fit (sytronic_RG_58_C_U_data)
 
 sytronic_RG_174_A_U_data = \
     [ (10e6,    9.6)
     , (20e6,   13.7)
-    , (50e5,   21.8)
+    , (50e6,   21.8)
     , (100e6,  31.1)
     , (200e6,  44.5)
     , (300e6,  50.3)
     , (500e6,  72.7)
     , (800e6,  91.3)
     , (1e9,   106.1)
     ]
@@ -2037,36 +2050,201 @@
     , (800e6,  78.0)
     , (1e9,    90.0)
     ]
 sytronic_RG_179_B_U = Manufacturer_Data_Cable \
     (75, 0.7, 102e-12, name = 'SYTRONIC RG 179 B/U')
 sytronic_RG_179_B_U.fit (sytronic_RG_179_B_U_data)
 
-def main () :
+# These are from Funkamateur Taschenkalender 2023
+Airborne5 = Manufacturer_Data_Cable \
+    (50, 0.85, name = 'Airborne5')
+Airborne5_data = \
+    [ (  10e6,  2.9)
+    , (  14e6,  3.8)
+    , (  28e6,  5.4)
+    , (  50e6,  7.0)
+    , ( 100e6,  9.4)
+    , ( 144e6, 11)
+    , ( 200e6, 12.9)
+    , ( 432e6, 19)
+    , (1296e6, 34.5)
+    ]
+Airborne5.fit (Airborne5_data)
+Airborne10 = Manufacturer_Data_Cable \
+    (50, 0.87, name = 'Airborne10')
+Airborne10_data = \
+    [ (  10e6,  1.2)
+    , (  14e6,  1.4)
+    , (  28e6,  1.9)
+    , (  50e6,  2.4)
+    , ( 100e6,  3.5)
+    , ( 144e6,  4.2)
+    , ( 200e6,  5.0)
+    , ( 432e6,  7.6)
+    , (1296e6, 13.6)
+    ]
+Airborne10.fit (Airborne10_data)
+Aircell5 = Manufacturer_Data_Cable \
+    (50, 0.82, name = 'Aircell5')
+Aircell5_data = \
+    [ (  10e6,  2.93)
+    , (  28e6,  4.9)
+    , (  50e6,  6.61)
+    , ( 100e6,  9.4)
+    , ( 144e6, 11.3)
+    , ( 200e6, 13.4)
+    , ( 432e6, 19.9)
+    , (1296e6, 35.7)
+    ]
+Aircell5.fit (Aircell5_data)
+Aircell7 = Manufacturer_Data_Cable \
+    (50, 0.83, name = 'Aircell7')
+Aircell7_data = \
+    [ (  10e6,  2.2)
+    , (  28e6,  3.7)
+    , (  50e6,  4.5)
+    , ( 100e6,  6.3)
+    , ( 144e6,  7.6)
+    , ( 200e6,  9.04)
+    , ( 432e6, 13.6)
+    , (1296e6, 24.8)
+    ]
+Aircell7.fit (Aircell7_data)
+Aircom = Manufacturer_Data_Cable \
+    (50, 0.85, name = 'Aircom Prem.')
+Aircom_data = \
+    [ (  10e6,  1.1)
+    , (  50e6,  2.7)
+    , ( 100e6,  3.3)
+    , ( 144e6,  4.5)
+    , ( 432e6,  8.5)
+    , (1296e6, 12.5)
+    ]
+Aircom.fit (Aircom_data)
+Ecoflex10 = Manufacturer_Data_Cable \
+    (50, 0.85, name = 'Ecoflex10')
+Ecoflex10_data = \
+    [ (  10e6,  1.2)
+    , (  14e6,  1.6)
+    , (  28e6,  2.1)
+    , (  50e6,  2.8)
+    , ( 100e6,  4.0)
+    , ( 144e6,  4.9)
+    , ( 200e6,  5.8)
+    , ( 432e6,  8.9)
+    , (1296e6, 16.5)
+    ]
+Ecoflex10.fit (Ecoflex10_data)
+Ecoflex10plus = Manufacturer_Data_Cable \
+    (50, 0.85, name = 'Ecoflex10+')
+Ecoflex10plus_data = \
+    [ (  10e6,  1.3)
+    , (  30e6,  2.3)
+    , (  50e6,  2.9)
+    , ( 100e6,  4.1)
+    , ( 144e6,  5.0)
+    , ( 432e6,  8.9)
+    , (1296e6, 16.2)
+    ]
+Ecoflex10plus.fit (Ecoflex10plus_data)
+Ecoflex15 = Manufacturer_Data_Cable \
+    (50, 0.86, name = 'Ecoflex15')
+Ecoflex15_data = \
+    [ (  10e6,  0.86)
+    , (  14e6,  1.0)
+    , (  28e6,  1.4)
+    , (  50e6,  1.96)
+    , ( 100e6,  2.8)
+    , ( 144e6,  3.4)
+    , ( 200e6,  4.05)
+    , ( 432e6,  6.1)
+    , (1296e6, 11.4)
+    ]
+Ecoflex15.fit (Ecoflex15_data)
+Ecoflex15plus = Manufacturer_Data_Cable \
+    (50, 0.86, name = 'Ecoflex15+')
+Ecoflex15plus_data = \
+    [ (  10e6,  0.83)
+    , (  50e6,  1.87)
+    , ( 100e6,  2.67)
+    , ( 144e6,  3.23)
+    , ( 432e6,  5.8)
+    , (1296e6, 10.5)
+    ]
+Ecoflex15plus.fit (Ecoflex15plus_data)
+EcoflexMulti = Manufacturer_Data_Cable \
+    (50, 0.85, name = 'Ecoflex Multi.')
+EcoflexMulti_data = \
+    [ (  10e6,  2.9)
+    , ( 100e6,  9.4)
+    , ( 500e6, 21.6)
+    , (1000e6, 31.1)
+    ]
+EcoflexMulti.fit (EcoflexMulti_data)
+H155 = Manufacturer_Data_Cable \
+    (50, 0.81, name = 'H155')
+H155_data = \
+    [ (  10e6,  3.0)
+    , (  50e6,  6.5)
+    , ( 100e6,  9.3)
+    , ( 144e6, 11.2)
+    , ( 200e6, 13.2)
+    , ( 432e6, 19.8)
+    , (1296e6, 34.9)
+    ]
+H155.fit (H155_data)
+H2000_Flex = Manufacturer_Data_Cable \
+    (50, 0.85, name = 'H2000-Flex')
+H2000_Flex_data = \
+    [ (  10e6,  1.2)
+    , (  14e6,  1.4)
+    , (  28e6,  2.0)
+    , (  50e6,  2.7)
+    , ( 100e6,  3.9)
+    , ( 144e6,  4.8)
+    , ( 432e6,  8.5)
+    , (1296e6, 15.7)
+    ]
+H2000_Flex.fit (H2000_Flex_data)
+H2005 = Manufacturer_Data_Cable \
+    (50, 0.85, name = 'H2005')
+H2005_data = \
+    [ (  10e6,  2.98)
+    , (  14e6,  3.83)
+    , (  28e6,  5.37)
+    , (  50e6,  6.98)
+    , ( 144e6, 11.0)
+    , ( 432e6, 19.5)
+    , (1296e6, 33.8)
+    ]
+H2005.fit (H2005_data)
+
+coax_models  = dict \
+    ( belden_8295          = belden_8295
+    , sytronic_RG_174_A_U  = sytronic_RG_174_A_U
+    , sytronic_RG_58_C_U   = sytronic_RG_58_C_U
+    , sytronic_RG_213_U    = sytronic_RG_213_U
+    , sytronic_RG_213_UBX  = sytronic_RG_213_UBX
+    , sytronic_RG_178_B_U  = sytronic_RG_178_B_U
+    , sytronic_RG_179_B_U  = sytronic_RG_179_B_U
+    , sytronic_RG_316_B_U  = sytronic_RG_316_B_U
+    , rs_222_8610_RG174A_U = rs_222_8610_RG174A_U
+    )
+
+def main ():
     cmd = ArgumentParser ()
-    actions = ['loss', 'match', 'resonator', 'stub']
-    models  = \
-        [ 'belden_8295'
-        , 'sytronic_RG_174_A_U'
-        , 'sytronic_RG_58_C_U'
-        , 'sytronic_RG_213_U'
-        , 'sytronic_RG_213_UBX'
-        , 'sytronic_RG_178_B_U'
-        , 'sytronic_RG_179_B_U'
-        , 'sytronic_RG_316_B_U'
-        , 'rs_222_8610_RG174A_U'
-        ]
+    actions = ['loss', 'loss-data', 'match', 'resonator', 'stub']
     cmd.add_argument \
         ( 'action'
         , help = "Action to perform, one of %s" % ', '.join (actions)
         )
     cmd.add_argument \
         ( '-c', '--coaxmodel'
         , help    = "Coax to model, one of %s, default=%%(default)s"
-                  % ', '.join (models)
+                  % ', '.join (coax_models)
         , default = 'belden_8295'
         )
     cmd.add_argument \
         ( '-f', '--frequency'
         , type    = float
         , help    = "Frequency to match transmission line (Hz), "
                     "default=%(default)s"
@@ -2104,19 +2282,19 @@
     cmd.add_argument \
         ( '-x', '--reactance'
         , help    = "Reactance for stub report, default=%(default)s"
         , type    = float
         , default = -100.0
         )
     args = cmd.parse_args ()
-    cable = globals () [args.coaxmodel]
+    cable = coax_models [args.coaxmodel]
     cable.reactance = args.reactance
-    if args.z_load is None and args.z_input is None :
+    if args.z_load is None and args.z_input is None:
         args.z_load = 50.0
     cable.set_freq_params \
         (args.frequency, args.length, args.power, args.z_load, args.z_input)
-    method = getattr (cable, 'summary_' + args.action)
+    method = getattr (cable, 'summary_' + args.action.replace ('-', '_'))
     print (method (metric = not args.imperial))
 # end def main
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     main ()
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/folded.py` & `antenna-optimizer-0.3/antenna_optimizer/folded.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/python3
 from __future__ import print_function
 
 from .antenna_model import Antenna_Model, Antenna_Optimizer, Excitation
-from .antenna_model import Arg_Handler
+from .antenna_model import Arg_Handler, antenna_actions
 
-class Folded_Dipole (Antenna_Model) :
+class Folded_Dipole (Antenna_Model):
 
     wire_radius   = 1.5e-3 / 2.0
     dipole_radius = 0.010
     lambda_4      = .146
     segs_dipole   = 19
     segs_arc      = 17
     segs_boom     =  5
@@ -18,57 +18,57 @@
         ( self
         , refl_dist     = .01
         , dipole_radius = dipole_radius
         , lambda_4      = lambda_4
         , reflector     = reflector
         , wire_radius   = wire_radius
         , ** kw
-        ) :
+        ):
         self.refl_dist     = refl_dist
         self.dipole_radius = dipole_radius
         self.lambda_4      = lambda_4
         self.reflector     = reflector
         self.wire_radius   = wire_radius
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def cmdline (self) :
+    def cmdline (self):
         return \
             ("-r %(dipole_radius)1.4f -d %(refl_dist)1.4f " \
              "-l %(reflector)1.4f -4 %(lambda_4)1.4f" % self.__dict__
             )
     # end def cmdline
 
-    def geometry (self, nec = None) :
-        if nec is None :
+    def geometry (self, nec = None):
+        if nec is None:
             nec = self.nec
         geo = nec.get_geometry ()
         self.tag = 1
         self.ex  = None
         self._geometry (geo)
         # Turn around Y by 270 deg, move everything up
         geo.move (0, 270, 0, 0, 0, self.up, 0, 0, 0)
     # end def geometry
 
-    def _geometry (self, geo) :
+    def _geometry (self, geo):
         a = ((-90, 90), (90, 270))
-        for n, z in enumerate ((1, -1)) :
+        for n, z in enumerate ((1, -1)):
             a1, a2 = a [n]
             geo.arc \
                 ( self.tag
                 , self.segs_arc
                 , self.dipole_radius
                 , a1
                 , a2
                 , self.wire_radius
                 )
             geo.move (0, 0, 0, z * self.lambda_4, 0, 0, self.tag, 0, 0)
             self.tag += 1
-        for x in (-self.lambda_4, self.lambda_4) :
-            for z in (self.dipole_radius, -self.dipole_radius) :
+        for x in (-self.lambda_4, self.lambda_4):
+            for z in (self.dipole_radius, -self.dipole_radius):
                 geo.wire \
                     ( self.tag
                     , self.segs_dipole
                     , 0, 0, z
                     , x, 0, z
                     , self.wire_radius
                     , 1, 1
@@ -113,64 +113,65 @@
             , self.wire_radius
             , 1, 1
             )
         self.tag += 1
     # end def _geometry
 
     @property
-    def up (self) :
+    def up (self):
         """ move everything up by max (reflector length, lambda_4 + r)
         """
         return max (self.reflector, self.lambda_4 + self.dipole_radius)
     # end def up
 
 # end class Folded_Dipole
 
-class Folded_Dipole_Optimizer (Antenna_Optimizer) :
+class Folded_Dipole_Optimizer (Antenna_Optimizer):
     """ Optimize given folded dipole
         Length are encoded as integers with a resolution of .5mm
         We use:
         * 8mm  <= dipole_radius <=  5cm
         * 8mm  <= refl_dist     <= 10cm
         * 10cm <= reflector     <= 40cm
         * 10cm <= lambda_4      <= 20cm
         If we force a reflector, we use
         reflector = dipole_radius + lambda_4 + x
         with 5mm <= x <= 10cm
     """
+    # The antenna class
+    ant_cls  = Folded_Dipole
 
-    def __init__ (self, force_reflector = False, **kw) :
+    def __init__ (self, force_reflector = False, **kw):
         self.force_reflector = force_reflector
         self.minmax = [(8e-3, 0.05), (8e-3, 0.1), (0.1, 0.4), (0.1, 0.2)]
-        if self.force_reflector :
+        if self.force_reflector:
             self.minmax [2] = (5e-3, 0.1)
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def compute_antenna (self, p, pop) :
+    def compute_antenna (self, p, pop):
         dipole_radius = self.get_parameter (p, pop, 0)
         refl_dist     = self.get_parameter (p, pop, 1)
         reflector     = self.get_parameter (p, pop, 2)
         lambda_4      = self.get_parameter (p, pop, 3)
-        if self.force_reflector :
+        if self.force_reflector:
             reflector += dipole_radius + lambda_4
-        fd = Folded_Dipole \
+        fd = self.ant_cls \
             ( dipole_radius = dipole_radius
             , refl_dist     = refl_dist
             , reflector     = reflector
             , lambda_4      = lambda_4
-            , frqidxmax     = 3
-            , wire_radius   = self.wire_radius
+            , **self.antenna_args
             )
         return fd
     # end def compute_antenna
 
 # end class Folded_Dipole_Optimizer
 
-def main () :
+def main ():
     cmd = Arg_Handler ()
     cmd.add_argument \
         ( '-4', '--lambda-len'
         , type = float
         , help = "(Half) Length of the dipole without rounded part"
         , default = 0.146
         )
@@ -195,37 +196,26 @@
     cmd.add_argument \
         ( '-r', '--dipole-radius'
         , type    = float
         , help    = "Radius of the rounded corner of the folded dipole"
         , default = 0.01
         )
     args = cmd.parse_args ()
-    if args.action == 'optimize' :
+    if args.action == 'optimize':
         do = Folded_Dipole_Optimizer \
             ( force_reflector = args.force_reflector
             , ** cmd.default_optimization_args
             )
         do.run ()
-    else :
+    else:
         fd = Folded_Dipole \
             ( dipole_radius = args.dipole_radius
             , refl_dist     = args.reflector_distance
             , reflector     = args.reflector_length
             , lambda_4      = args.lambda_len
             , ** cmd.default_antenna_args
             )
-        if args.action == 'necout' :
-            print (fd.as_nec ())
-        elif args.action not in actions :
-            cmd.print_usage ()
-        else :
-            fd.compute ()
-        if args.action == 'swr' :
-            fd.swr_plot ()
-        elif args.action == 'gain' :
-            fd.plot ()
-        elif args.action == 'frgain' :
-            print ('\n'.join (fd.show_gains ()))
+        antenna_actions (cmd, args, fd)
 # end def main
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     main ()
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/folded_3ele.py` & `antenna-optimizer-0.3/antenna_optimizer/folded_3ele.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/python3
 from __future__ import print_function
 
 from .antenna_model import Antenna_Model, Antenna_Optimizer, Arg_Handler
-from .folded        import Folded_Dipole
+from .folded        import Folded_Dipole, antenna_actions
 
-class Folded_Dipole_3el (Folded_Dipole) :
+class Folded_Dipole_3el (Folded_Dipole):
 
     wire_radius   = 1.5e-3 / 2.0
     dipole_radius = 0.010
     lambda_4      = .146
     segs_dipole   = 19
     segs_arc      = 17
     segs_boom     =  5
@@ -21,36 +21,36 @@
         , dir_dist      = .01
         , dipole_radius = dipole_radius
         , lambda_4      = lambda_4
         , reflector     = reflector
         , director      = director
         , wire_radius   = wire_radius
         , ** kw
-        ) :
+        ):
         self.dir_dist      = dir_dist
         self.director      = director
         self.__super.__init__ \
             ( refl_dist     = refl_dist
             , dipole_radius = dipole_radius
             , lambda_4      = lambda_4
             , reflector     = reflector
             , wire_radius   = wire_radius
             , ** kw
             )
     # end def __init__
 
-    def cmdline (self) :
+    def cmdline (self):
         return \
             ("-r %(dipole_radius)1.4f -d %(refl_dist)1.4f "
              "-D %(dir_dist)1.4f -L %(director)1.4f "
              "-l %(reflector)1.4f -4 %(lambda_4)1.4f" % self.__dict__
             )
     # end def cmdline
 
-    def _geometry (self, geo) :
+    def _geometry (self, geo):
         self.__super._geometry (geo)
         # third part of boom from dipole to director
         geo.wire \
             ( self.tag
             , self.segs_boom
             , 0, 0, self.dipole_radius
             , 0, 0, (self.dir_dist + self.dipole_radius)
@@ -76,68 +76,69 @@
             , self.wire_radius
             , 1, 1
             )
         self.tag += 1
     # end def _geometry
 
     @property
-    def up (self) :
+    def up (self):
         return max \
             (self.reflector, self.director, self.lambda_4 + self.dipole_radius)
     # end def up
 
 # end class Folded_Dipole_3el
 
-class Folded_Dipole_Optimizer (Antenna_Optimizer) :
+class Folded_Dipole_Optimizer (Antenna_Optimizer):
     """ Optimize given folded dipole
         Length are encoded as integers with a resolution of .5mm
         We use:
         * 8mm  <= dipole_radius <=  5cm
         * 35mm <= refl_dist     <= 30cm
         * 35mm <= dir_dist      <= 30cm
         * 10cm <= director      <= 40cm
         * 1mm  <= refldiff      <= 15cm
         * 10cm <= lambda_4      <= 20cm
     """
 
-    def __init__ (self, **kw) :
+    ant_cls = Folded_Dipole_3el
+
+    def __init__ (self, **kw):
         self.minmax = \
             [ (8e-3,  0.05)
             , (0.035, 0.3)
             , (0.035, 0.3)
             , ( 0.1,  0.4)
             , (1e-3,  0.15)
             , ( 0.1,  0.2)
             ]
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def compute_antenna (self, p, pop) :
+    def compute_antenna (self, p, pop):
         dipole_radius = self.get_parameter (p, pop, 0)
         refl_dist     = self.get_parameter (p, pop, 1)
         dir_dist      = self.get_parameter (p, pop, 2)
         director      = self.get_parameter (p, pop, 3)
         refldiff      = self.get_parameter (p, pop, 4)
         lambda_4      = self.get_parameter (p, pop, 5)
-        fd = Folded_Dipole_3el \
+        fd = self.ant_cls \
             ( dipole_radius = dipole_radius
             , refl_dist     = refl_dist
             , dir_dist      = dir_dist
             , director      = director
             , reflector     = director + refldiff
             , lambda_4      = lambda_4
-            , frqidxmax     = 3
-            , wire_radius   = self.wire_radius
+            , **self.antenna_args
             )
         return fd
     # end def compute_antenna
 
 # end class Folded_Dipole_Optimizer
 
-def main () :
+def main ():
     cmd = Arg_Handler ()
     cmd.add_argument \
         ( '-4', '--lambda-len'
         , type = float
         , help = "(Half) Length of the dipole without rounded part"
         , default = 0.146
         )
@@ -168,36 +169,25 @@
     cmd.add_argument \
         ( '-r', '--dipole-radius'
         , type    = float
         , help    = "Radius of the rounded corner of the folded dipole"
         , default = 0.01
         )
     args = cmd.parse_args ()
-    if args.action == 'optimize' :
+    if args.action == 'optimize':
         do = Folded_Dipole_Optimizer (** cmd.default_optimization_args)
         do.run ()
-    else :
+    else:
         fd = Folded_Dipole_3el \
             ( dipole_radius = args.dipole_radius
             , refl_dist     = args.reflector_distance
             , dir_dist      = args.director_distance
             , reflector     = args.reflector_length
             , director      = args.director_length
             , lambda_4      = args.lambda_len
             , ** cmd.default_antenna_args
             )
-        if args.action == 'necout' :
-            print (fd.as_nec ())
-        elif args.action not in actions :
-            cmd.print_usage ()
-        else :
-            fd.compute ()
-        if args.action == 'swr' :
-            fd.swr_plot ()
-        elif args.action == 'gain' :
-            fd.plot ()
-        elif args.action == 'frgain' :
-            print ('\n'.join (fd.show_gains ()))
+        antenna_actions (cmd, args, fd)
 # end def main
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     main ()
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/folded_bc.py` & `antenna-optimizer-0.3/antenna_optimizer/folded_bc.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,179 +1,178 @@
 #!/usr/bin/python3
 from __future__ import print_function
 
 from .antenna_model import Antenna_Model, Antenna_Optimizer, Excitation
-from .antenna_model import Arg_Handler
+from .antenna_model import Arg_Handler, antenna_actions
 
-class Folded_Dipole (Antenna_Model) :
+class Folded_Dipole (Antenna_Model):
     """ Broadcast Reception Antenna
         For 87.5MHz - 108 MHz and 75 Ohm
         Note that with a single dipole this is too narrowband to work
         reliably.
     """
 
     wire_radius   = 1.5e-3 / 2.0
     dipole_radius = 0.010
     lambda_4      = .146
     segs_dipole   = 19
     segs_arc      = 17
     segs_boom     =  5
     reflector     = 0.2
-    frqstart      = 87.5
-    frqend        = 108.0
+    frq_ranges    = [(87.5, 108.0)]
 
     def __init__ \
         ( self
         , refl_dist     = .01
         , dipole_radius = dipole_radius
         , lambda_4      = lambda_4
         , wire_radius   = wire_radius
         , impedance     = 75.0
         , use_boom      = False
         , ** kw
-        ) :
+        ):
         self.dipole_radius = dipole_radius
         self.lambda_4      = lambda_4
-        if self.lambda_4 < 0.0005 :
+        if self.lambda_4 < 0.0005:
             self.lambda_4 = 0.0
         self.wire_radius   = wire_radius
         self.impedance     = impedance
         self.use_boom      = use_boom
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def cmdline (self) :
+    def cmdline (self):
         return ("-r %(dipole_radius)1.4f -4 %(lambda_4)1.4f" % self.__dict__)
     # end def cmdline
 
-    def geometry (self, nec = None) :
-        if nec is None :
+    def geometry (self, nec = None):
+        if nec is None:
             nec = self.nec
         geo = nec.get_geometry ()
         self.tag = 1
         self.ex  = None
         self._geometry (geo)
         # Move everything up
         geo.move (0, 0, 90, 0, 0, self.up, 0, 0, 0)
     # end def geometry
 
-    def _geometry (self, geo) :
+    def _geometry (self, geo):
         a = ((-90, 90), (90, 270))
-        for n, z in enumerate ((1, -1)) :
+        for n, z in enumerate ((1, -1)):
             a1, a2 = a [n]
             geo.arc \
                 ( self.tag
                 , self.segs_arc
                 , self.dipole_radius
                 , a1
                 , a2
                 , self.wire_radius
                 )
             geo.move (0, 0, 0, z * self.lambda_4, 0, 0, self.tag, 0, 0)
             roundtag = self.tag
             self.tag += 1
         # Interpolate the number of segments for very small lambda_4
-        if self.lambda_4 > .4 :
+        if self.lambda_4 > .4:
             segs = self.segs_dipole
-        elif self.lambda_4 <= 0.05 :
+        elif self.lambda_4 <= 0.05:
             segs = 3
-        else :
+        else:
             segs = self.lambda_4 * (self.segs_dipole - 3) / 0.35 \
                  + (24 - self.segs_dipole) / 7.0
             segs = int (segs)
-            if segs % 2 == 0 :
+            if segs % 2 == 0:
                 segs += 1
-        if self.lambda_4 > 0.0 :
-            for z in (self.dipole_radius, -self.dipole_radius) :
-                if self.use_boom :
-                    for x in (-self.lambda_4, self.lambda_4) :
+        if self.lambda_4 > 0.0:
+            for z in (self.dipole_radius, -self.dipole_radius):
+                if self.use_boom:
+                    for x in (-self.lambda_4, self.lambda_4):
                         geo.wire \
                             ( self.tag
                             , segs
                             , 0, 0, z
                             , x, 0, z
                             , self.wire_radius
                             , 1, 1
                             )
                         self.tag += 1
-                else :
+                else:
                     geo.wire \
                         ( self.tag
                         , segs
                         , -self.lambda_4, 0, z
                         ,  self.lambda_4, 0, z
                         , self.wire_radius
                         , 1, 1
                         )
                     self.tag += 1
-        if self.use_boom :
+        if self.use_boom:
             self.ex = Excitation (self.tag - 1, 1)
-        elif self.lambda_4 >= 0.002 :
+        elif self.lambda_4 >= 0.002:
             self.ex = Excitation (self.tag - 1, segs // 2 + 1)
-        else :
+        else:
             # If straight piece is too small use last round segment
             self.ex = Excitation (roundtag, self.segs_arc)
         # boom across folded part
-        if self.use_boom :
+        if self.use_boom:
             geo.wire \
                 ( self.tag
                 , self.segs_boom
                 , 0, 0,  self.dipole_radius
                 , 0, 0, -self.dipole_radius
                 , self.wire_radius
                 , 1, 1
                 )
             self.tag += 1
     # end def _geometry
 
     @property
-    def up (self) :
+    def up (self):
         """ move everything up by max (reflector length, lambda_4 + r)
         """
         return self.lambda_4 + self.dipole_radius
     # end def up
 
 # end class Folded_Dipole
 
-class Folded_Dipole_Optimizer (Antenna_Optimizer) :
+class Folded_Dipole_Optimizer (Antenna_Optimizer):
     """ Optimize given folded dipole
         Length are encoded as integers with a resolution of .5mm
         We use:
         * 8mm  <= dipole_radius <= 40cm
         * 40cm <= lambda_4      <= 150cm
     """
+    ant_cls = Folded_Dipole
 
     def __init__ \
-        (self, impedance = 75.0, allow_loop = False, use_boom = False, **kw) :
+        (self, impedance = 75.0, allow_loop = False, use_boom = False, **kw):
         self.allow_loop = allow_loop
         self.impedance  = impedance
         self.use_boom   = use_boom
         self.minmax = [(8e-3, 0.4), (0.4, 1.5)]
-        if allow_loop :
+        if allow_loop:
             self.minmax = [(8e-3, 0.75), (0.00, 1.5)]
         self.__super.__init__ (nofb = True, **kw)
     # end def __init__
 
-    def compute_antenna (self, p, pop) :
+    def compute_antenna (self, p, pop):
         dipole_radius = self.get_parameter (p, pop, 0)
         lambda_4      = self.get_parameter (p, pop, 1)
-        fd = Folded_Dipole \
+        fd = self.ant_cls \
             ( dipole_radius = dipole_radius
             , lambda_4      = lambda_4
-            , frqidxmax     = 3
-            , wire_radius   = self.wire_radius
             , impedance     = self.impedance
             , use_boom      = self.use_boom
+            , **self.antenna_args
             )
         return fd
     # end def compute_antenna
 
 # end class Folded_Dipole_Optimizer
 
-def main () :
+def main ():
     cmd = Arg_Handler ()
     cmd.add_argument \
         ( '-4', '--lambda-len'
         , type = float
         , help = "(Half) Length of the dipole without rounded part"
         , default = 0.146
         )
@@ -196,39 +195,28 @@
         )
     cmd.add_argument \
         ( '--use-boom'
         , help    = "Use a boom in the middle of the structure"
         , action  = 'store_true'
         )
     args = cmd.parse_args ()
-    if args.action == 'optimize' :
+    if args.action == 'optimize':
         do = Folded_Dipole_Optimizer \
             ( allow_loop = args.allow_loop
             , impedance  = args.impedance
             , use_boom   = args.use_boom
             , ** cmd.default_optimization_args
             )
         do.run ()
-    else :
+    else:
         fd = Folded_Dipole \
             ( dipole_radius = args.dipole_radius
             , lambda_4      = args.lambda_len
             , impedance     = args.impedance
             , use_boom      = args.use_boom
             , ** cmd.default_antenna_args
             )
-        if args.action == 'necout' :
-            print (fd.as_nec ())
-        elif args.action not in actions :
-            cmd.print_usage ()
-        else :
-            fd.compute ()
-        if args.action == 'swr' :
-            fd.swr_plot ()
-        elif args.action == 'gain' :
-            fd.plot ()
-        elif args.action == 'frgain' :
-            print ('\n'.join (fd.show_gains ()))
+        antenna_actions (cmd, args, fd)
 # end def main
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     main ()
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/folded_bigrefl.py` & `antenna-optimizer-0.3/antenna_optimizer/folded_bigrefl.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/python3
 from __future__ import print_function
 import sys
 
 from .antenna_model import Antenna_Model, Antenna_Optimizer, Excitation
-from .antenna_model import Arg_Handler
+from .antenna_model import Arg_Handler, antenna_actions
 
-class Folded_Dipole (Antenna_Model) :
+class Folded_Dipole (Antenna_Model):
     """ This is a folded dipole with a balcony rail as a large reflector.
         Note that most conductors modelled in the following are not
         actually round. The upper railing modelled as a 20.5mm diameter
         round conductor *is* the only conductor that really is round.
         The upper and lower horizontal conductors are 8.5x30.5mm. The
         left and right vertical conductors are 9x30.5mm. The inner
         vertical conductors are 8.5x25.5mm.
@@ -38,15 +38,15 @@
         , refl_radius3  = (20.5 / 2.0) * 1e-3
         , refl_d1       = 61 * 1e-3
         , refl_d2       = 150 * 1e-3
         , refl_d3       = (690 - 8.5) * 1e-3
         , refl_d4       = refl_d4
         , refl_d5       = (96.5 + 8.5 / 2.0) * 1e-3
         , ** kw
-        ) :
+        ):
         self.refl_dist     = refl_dist
         self.dir_dist      = dir_dist
         self.ant_h         = ant_h
         self.dipole_radius = dipole_radius
         self.lambda_4      = lambda_4
         self.director      = director
         self.wire_radius   = wire_radius
@@ -57,47 +57,47 @@
         self.refl_d2       = refl_d2
         self.refl_d3       = refl_d3
         self.refl_d4       = refl_d4
         self.refl_d5       = refl_d5
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def cmdline (self) :
+    def cmdline (self):
         return \
             ( "-r %(dipole_radius)1.4f -d %(refl_dist)1.4f "
               "-l %(director)1.4f -4 %(lambda_4)1.4f "
               "-D %(dir_dist)1.4f -H %(ant_h)1.4f" % self.__dict__
             )
     # end def cmdline
 
-    def geometry (self, nec = None) :
-        if nec is None :
+    def geometry (self, nec = None):
+        if nec is None:
             nec = self.nec
         geo = nec.get_geometry ()
         self.tag = 1
         self.ex  = None
         self._geometry (geo)
     # end def geometry
 
-    def _geometry (self, geo) :
+    def _geometry (self, geo):
         a = ((-90, 90), (90, 270))
-        for n, z in enumerate ((1, -1)) :
+        for n, z in enumerate ((1, -1)):
             a1, a2 = a [n]
             geo.arc \
                 ( self.tag
                 , self.segs_arc
                 , self.dipole_radius
                 , a1
                 , a2
                 , self.wire_radius
                 )
             geo.move (0, 0, 0, z * self.lambda_4, 0, 0, self.tag, 0, 0)
             self.tag += 1
-        for x in (-self.lambda_4, self.lambda_4) :
-            for z in (self.dipole_radius, -self.dipole_radius) :
+        for x in (-self.lambda_4, self.lambda_4):
+            for z in (self.dipole_radius, -self.dipole_radius):
                 geo.wire \
                     ( self.tag
                     , self.segs_dipole
                     , 0, 0, z
                     , x, 0, z
                     , self.wire_radius
                     , 1, 1
@@ -145,15 +145,15 @@
         self.tag += 1
         # Turn around Y by 270 deg, move everything in place
         geo.move \
             ( 0, 270, 0
             , self.dipole_radius + self.refl_dist, 0, self.refl_d4 + self.ant_h
             , 0, 0, 0
             )
-        for y in (-1, 1) :
+        for y in (-1, 1):
             z = 0
             geo.wire \
                 ( self.tag
                 , 3
                 , 0, y * 4 * self.refl_d5, z
                 , 0, y * 4 * self.refl_d5, z + self.refl_d4
                 , self.refl_radius2
@@ -195,99 +195,99 @@
             , self.segs_dipole
             , 0, -4 * self.refl_d5, z
             , 0,  4 * self.refl_d5, z
             , self.refl_radius3
             , 1, 1
             )
         self.tag += 1
-        for z in [self.refl_d4, self.refl_d4 + self.refl_d3] :
-            for y in range (-4, 4) :
+        for z in [self.refl_d4, self.refl_d4 + self.refl_d3]:
+            for y in range (-4, 4):
                 geo.wire \
                     ( self.tag
                     , 3
                     , 0, y * self.refl_d5,                z
                     , 0, y * self.refl_d5 + self.refl_d5, z
                     , self.refl_radius2
                     , 1, 1
                     )
                 self.tag += 1
-        for y in range (-3, 4) :
+        for y in range (-3, 4):
             geo.wire \
                 ( self.tag
                 , self.segs_dipole
                 , 0, y * self.refl_d5, self.refl_d4
                 , 0, y * self.refl_d5, self.refl_d4 + self.refl_d3
                 , self.refl_radius1
                 , 1, 1
                 )
             self.tag += 1
     # end def _geometry
 
     @property
-    def up (self) :
+    def up (self):
         """ move everything up by max (director length, lambda_4 + r)
         """
         return max (self.director, self.lambda_4 + self.dipole_radius)
     # end def up
 
 # end class Folded_Dipole
 
-class Folded_Dipole_Optimizer (Antenna_Optimizer) :
+class Folded_Dipole_Optimizer (Antenna_Optimizer):
     """ Optimize given folded dipole
         Length are encoded as integers with a resolution of .5mm
         We use:
         * 8mm  <= dipole_radius <=  5cm
         * 8mm  <= refl_dist     <= 15cm
         * 8mm  <= dir_dist      <= 15cm
         * 10cm <= director      <= 40cm
         * 10cm <= lambda_4      <= 20cm
         * 0mm  <= ant_h         <= ((690 - 8.5) / 2.0)mm
         Or with the large_refldist option we use
         * 2cm  <= refl_dist     <= 25cm
     """
+    ant_cls = Folded_Dipole
 
-    def __init__ (self, large_refldist = False, **kw) :
+    def __init__ (self, large_refldist = False, **kw):
         self.ant_height = (690 - 8.5) * 1e-3
         self.large_refldist = large_refldist
         self.minmax = \
             [ (8e-3, 0.05)
             , (8e-3, 0.15)
             , (8e-3, 0.15)
             , (0.1,  0.4)
             , (0.1,  0.2)
             , (0,    self.ant_height)
             ]
-        if self.large_refldist :
+        if self.large_refldist:
             self.minmax [1] = (0.02, 0.25)
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def compute_antenna (self, p, pop) :
+    def compute_antenna (self, p, pop):
         dipole_radius = self.get_parameter (p, pop, 0)
         refl_dist     = self.get_parameter (p, pop, 1)
         dir_dist      = self.get_parameter (p, pop, 2)
         director      = self.get_parameter (p, pop, 3)
         lambda_4      = self.get_parameter (p, pop, 4)
-        ant_h         = self.get_parameter (p, pop, 5) + Folded_Dipole.refl_d4
-        fd = Folded_Dipole \
+        ant_h         = self.get_parameter (p, pop, 5) + self.ant_cls.refl_d4
+        fd = self.ant_cls \
             ( dipole_radius = dipole_radius
             , dir_dist      = dir_dist
             , refl_dist     = refl_dist
             , director      = director
             , lambda_4      = lambda_4
             , ant_h         = ant_h
-            , frqidxmax     = 3
-            , wire_radius   = self.wire_radius
+            , **self.antenna_args
             )
         return fd
     # end def compute_antenna
 
 # end class Folded_Dipole_Optimizer
 
-def main () :
+def main ():
     cmd = Arg_Handler ()
     cmd.add_argument \
         ( '-4', '--lambda-len'
         , type = float
         , help = "(Half) Length of the dipole without rounded part"
         , default = 0.146
         )
@@ -347,42 +347,31 @@
     cmd.add_argument \
         ( '--refl-radius3'
         , type    = float
         , help    = "Radius of round horizontal element"
         , default = (20.5 / 2.0) * 1e-3
         )
     args = cmd.parse_args ()
-    if args.action == 'optimize' :
+    if args.action == 'optimize':
         do = Folded_Dipole_Optimizer \
             ( large_refldist = args.large_refldist
             , ** cmd.default_optimization_args
             )
         do.run ()
-    else :
+    else:
         fd = Folded_Dipole \
             ( dipole_radius = args.dipole_radius
             , refl_dist     = args.reflector_distance
             , dir_dist      = args.director_distance
             , ant_h         = args.antenna_height
             , director      = args.director_length
             , lambda_4      = args.lambda_len
             , refl_radius1  = args.refl_radius1
             , refl_radius2  = args.refl_radius2
             , refl_radius3  = args.refl_radius3
             , ** cmd.default_antenna_args
             )
-        if args.action == 'necout' :
-            print (fd.as_nec ())
-        elif args.action not in actions :
-            cmd.print_usage ()
-        else :
-            fd.compute ()
-        if args.action == 'swr' :
-            fd.swr_plot ()
-        elif args.action == 'gain' :
-            fd.plot ()
-        elif args.action == 'frgain' :
-            print ('\n'.join (fd.show_gains ()))
+        antenna_actions (cmd, args, fd)
 # end def main
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     main ()
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/hb9cv.py` & `antenna-optimizer-0.3/antenna_optimizer/hb9cv.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/python3
 from __future__ import print_function
 
 from .antenna_model import Antenna_Model, Antenna_Optimizer, Excitation
-from .antenna_model import Arg_Handler
+from .antenna_model import Arg_Handler, antenna_actions
 from .transmission  import transmission_line_z
 
-class HB9CV (Antenna_Model) :
+class HB9CV (Antenna_Model):
     """ The HB9CV antenna is a two-element yagi-uda antenna.
         It uses transmission lines for off-center feeding.
         The feedpoint is between the middle of the reflector and two
         connected transmission lines. When viewed with the reflector at
         the front and the director at the back, the length l5 is the
         distance from the middle if the reflector to the feedpoint on
         the right of the reflector. The length l4 is the distance from
@@ -37,36 +37,36 @@
         , refl_dist     = refl_dist
         , l4            = l4
         , l5            = l5
         , stub_height   = stub_height
         , geotype       = geotypes [0]
         , vf            = vf
         , ** kw
-        ) :
+        ):
         self.director    = director
         self.reflector   = reflector
         self.refl_dist   = refl_dist
         self.l4          = l4
         self.l5          = l5
         self.stub_height = stub_height
         self.geotype     = geotype
         self.vf          = vf
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def cmdline (self) :
+    def cmdline (self):
         return \
             ("-l %(director)1.4f -r %(reflector)1.4f " \
              "-d %(refl_dist)1.4f -4 %(l4)1.4f -5 %(l5)1.4f "
              "-H %(stub_height)1.4f" % self.__dict__
             )
     # end def cmdline
 
-    def geometry (self, nec = None) :
-        if nec is None :
+    def geometry (self, nec = None):
+        if nec is None:
             nec = self.nec
         geo = nec.get_geometry ()
         self.tag = 1
         self.ex  = None
 
         # Director
         geo.wire \
@@ -85,15 +85,15 @@
             , self.segs_stub
             , self.refl_dist,       0, 0
             , self.refl_dist, self.l4, 0
             , self.wire_radius
             , 1, 1
             )
         self.tag += 1
-        if self.director / 2.0 > self.l4 :
+        if self.director / 2.0 > self.l4:
             geo.wire \
                 ( self.tag
                 , self.segs_stub
                 , self.refl_dist,             self.l4, 0
                 , self.refl_dist, self.director / 2.0, 0
                 , self.wire_radius
                 , 1, 1
@@ -117,15 +117,15 @@
             , self.segs_stub
             , 0,        0, 0
             , 0, -self.l5, 0
             , self.wire_radius
             , 1, 1
             )
         self.tag += 1
-        if self.reflector / 2.0 > self.l5 :
+        if self.reflector / 2.0 > self.l5:
             geo.wire \
                 ( self.tag
                 , self.segs_stub
                 , 0,              -self.l5, 0
                 , 0, -self.reflector / 2.0, 0
                 , self.wire_radius
                 , 1, 1
@@ -158,99 +158,68 @@
             ( self.tag
             , self.segs_stub
             , self.refl_dist, self.l4,                0
             , self.refl_dist, self.l4, self.stub_height
             , self.wire_radius
             , 1, 1
             )
-        director_stub_conn_tag = self.tag
+        self.director_stub_conn_tag = self.tag
         self.tag  += 1
         # Connect Reflector Stub to Reflector
         geo.wire \
             ( self.tag
             , self.segs_stub
             , 0, -self.l5,                0
             , 0, -self.l5, self.stub_height
             , self.wire_radius
             , 1, 1
             )
-        reflector_stub_conn_tag = self.tag
+        self.reflector_stub_conn_tag = self.tag
         self.tag  += 1
-        # Experiment with two feedpoints: Doesn't work as it's
-        # impossible to then find out what the impedance of the real
-        # feedpoint would be.
-        # Phasing and feed from stub on boom to stub on director
-        #geo.wire \
-        #    ( self.tag
-        #    , 1
-        #    , self.refl_dist,       0, self.stub_height
-        #    , self.refl_dist, self.l4, self.stub_height
-        #    , self.wire_radius
-        #    , 1, 1
-        #    )
-        #self.ex    = []
-        #frq = self.frqstart + (self.frqend - self.frqstart) / 2
-        #phi = phase_shift (frq, self.l4)
-        #u_real, u_imag = complex_voltage (phi)
-        #self.ex.append (Excitation (self.tag, 1, u_real, u_imag))
-        #self.tag += 1
-        # Phasing and feed from stub on boom to stub on reflector
-        #geo.wire \
-        #    ( self.tag
-        #    , 1
-        #    , self.refl_dist,        0, self.stub_height
-        #    ,              0, -self.l5, self.stub_height
-        #    , self.wire_radius
-        #    , 1, 1
-        #    )
-        #phi = phase_shift (frq, self.l5 + self.refl_dist)
-        #u_real, u_imag = complex_voltage (phi)
-        #self.ex.append (Excitation (self.tag, 1, u_real, u_imag))
-        #self.tag += 1
 
-        if self.geotype == 'transmission-1' :
+        if self.geotype == 'transmission-1':
             # Wire from lower part of feedpoint to upper part of
             # director stub: Used as transmission-line endpoint
             h = 0
-            if self.geotype == 'parallel' :
+            if self.geotype == 'parallel':
                 h = self.stub_height
             geo.wire \
                 ( self.tag
                 , 1
                 , self.refl_dist,        0, 0
                 ,              0, -self.l5, self.stub_height
                 , self.wire_radius
                 , 1, 1
                 )
-            reflector_stub_tag = self.tag
+            self.reflector_stub_tag = self.tag
             self.tag += 1
 
-        if self.geotype in ('transmission-1', 'parallel') :
+        if self.geotype in ('transmission-1', 'parallel'):
             # Wire from lower (or upper depending on geotype) part of
             # feedpoint to upper part of director stub: Used as
             # transmission-line endpoint or parallel wire endpoint
             h = 0
-            if self.geotype == 'parallel' :
+            if self.geotype == 'parallel':
                 h = self.stub_height
 
             # Wire from lower (or upper depending on geotype) part of
             # feedpoint to upper part of reflector stub: Used as
             # transmission-line endpoint or parallel wire endpoint
             geo.wire \
                 ( self.tag
                 , 1
                 , self.refl_dist,       0, h
                 , self.refl_dist, self.l4, self.stub_height
                 , self.wire_radius
                 , 1, 1
                 )
-            director_stub_tag = self.tag
+            self.director_stub_tag = self.tag
             self.tag += 1
 
-        if self.geotype == 'parallel' :
+        if self.geotype == 'parallel':
             geo.wire \
                 ( self.tag
                 , 1
                 , self.refl_dist, 0, self.stub_height
                 ,              0, 0, self.stub_height
                 , self.wire_radius
                 , 1, 1
@@ -261,98 +230,102 @@
                 , 1
                 , 0,        0, self.stub_height
                 , 0, -self.l5, self.stub_height
                 , self.wire_radius
                 , 1, 1
                 )
             self.tag += 1
+    # end def geometry
 
-        nec.geometry_complete (0)
 
+    def geometry_complete (self, nec = None):
+        if nec is None:
+            nec = self.nec
+        nec.geometry_complete (0)
         impedance = transmission_line_z \
             (self.wire_radius * 2, self.stub_height)
-        if self.geotype == 'transmission-1' :
+        if self.geotype == 'transmission-1':
             nec.tl_card \
                 ( self.ex.tag, self.ex.segment
-                , reflector_stub_tag, 1
+                , self.reflector_stub_tag, 1
                 , impedance
                 , (self.refl_dist + self.l5) * self.vf
                 , 0, 0, 0, 0
                 )
             nec.tl_card \
                 ( self.ex.tag, self.ex.segment
-                , director_stub_tag, 1
+                , self.director_stub_tag, 1
                 , impedance
                 , self.l4 * self.vf
                 , 0, 0, 0, 0
                 )
-        if self.geotype == 'transmission-2' :
+        if self.geotype == 'transmission-2':
             nec.tl_card \
                 ( self.ex.tag, self.ex.segment
-                , reflector_stub_conn_tag, 1
+                , self.reflector_stub_conn_tag, 1
                 , impedance
                 , (self.refl_dist + self.l5) * self.vf
                 , 0, 0, 0, 0
                 )
             nec.tl_card \
                 ( self.ex.tag, self.ex.segment
-                , director_stub_conn_tag, 1
+                , self.director_stub_conn_tag, 1
                 , impedance
                 , self.l4 * self.vf
                 , 0, 0, 0, 0
                 )
-    # end def geometry
+    # end def geometry_complete
 
 # end class HB9CV
 
-class HB9CV_Optimizer (Antenna_Optimizer) :
+class HB9CV_Optimizer (Antenna_Optimizer):
     """ Optimize given folded dipole
         Length are encoded with a resolution of .5mm
         We use:
         * 25cm   <= director    <= 35cm
         * 25cm   <= reflector   <= 35cm
         *  5cm   <= refl_dist   <= 15cm
         *  3cm   <= l4          <= 10cm
         *  3cm   <= l5          <= 10cm
         *  5mm   <= stub_height <= 1.5cm
     """
+    ant_cls = HB9CV
 
-    def __init__ (self, vf = 0.9, **kw) :
+    def __init__ (self, vf = 0.9, **kw):
         self.minmax = \
             [ (0.25, 0.35), (0.25, 0.35), (0.05, 0.15)
             , (0.03, 0.1),  (0.03, 0.1),  (0.005, 0.015)
             ]
         self.vf = vf
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def compute_antenna (self, p, pop) :
+    def compute_antenna (self, p, pop):
         director      = self.get_parameter (p, pop, 0)
         reflector     = self.get_parameter (p, pop, 1)
         refl_dist     = self.get_parameter (p, pop, 2)
         l4            = self.get_parameter (p, pop, 3)
         l5            = self.get_parameter (p, pop, 4)
         h             = self.get_parameter (p, pop, 5)
-        fd = HB9CV \
+        fd = self.ant_cls \
             ( director      = director
             , reflector     = reflector
             , refl_dist     = refl_dist
             , l4            = l4
             , l5            = l5
             , stub_height   = h
-            , frqidxmax     = 3
-            , wire_radius   = self.wire_radius
             , vf            = self.vf
+            , **self.antenna_args
             )
         return fd
     # end def compute_antenna
 
 # end class HB9CV_Optimizer
 
-def main () :
+def main ():
     cmd = Arg_Handler ()
     cmd.add_argument \
         ( '-4', '--l4'
         , type    = float
         , help    = "Length of l4 (stub on director side)"
         , default = 0.0431
         )
@@ -394,38 +367,27 @@
     cmd.add_argument \
         ( '--vf'
         , type    = float
         , help    = "Velocity factor of transmission line"
         , default = 0.9
         )
     args = cmd.parse_args ()
-    if args.action == 'optimize' :
+    if args.action == 'optimize':
         do = HB9CV_Optimizer (vf = args.vf, ** cmd.default_optimization_args)
         do.run ()
-    else :
+    else:
         fd = HB9CV \
             ( director      = args.director_length
             , reflector     = args.reflector_length
             , refl_dist     = args.reflector_distance
             , l4            = args.l4
             , l5            = args.l5
             , stub_height   = args.stub_height
             , geotype       = args.geotype
             , vf            = args.vf
             , ** cmd.default_antenna_args
             )
-        if args.action == 'necout' :
-            print (fd.as_nec ())
-        elif args.action not in actions :
-            cmd.print_usage ()
-        else :
-            fd.compute ()
-        if args.action == 'swr' :
-            fd.swr_plot ()
-        elif args.action == 'gain' :
-            fd.plot ()
-        elif args.action == 'frgain' :
-            print ('\n'.join (fd.show_gains ()))
+        antenna_actions (cmd, args, fd)
 # end def main
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     main ()
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/logper.py` & `antenna-optimizer-0.3/antenna_optimizer/logper.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 #!/usr/bin/python3
 from __future__ import print_function
 
 import sys
 
 from .antenna_model import Antenna_Model, Antenna_Optimizer, Excitation
-from .antenna_model import Arg_Handler
+from .antenna_model import Arg_Handler, antenna_actions
 from .transmission import transmission_line_z_square
 
-class Logperiodic (Antenna_Model) :
+class Logperiodic (Antenna_Model):
     """ Log Periodic Antenna Model, Default data taken from
         http://adl303-archiv.oevsv.at/technikecke/dlogpant/index.html
         Given lengths are with boom radius according to website above in
         the picture it states: "Die Elementlaengen sind von Mitte des
         Booms bis zum Element-Ende errechnet !!" Contrary to this in the
         table with the lengths and distances it is stated:
         "Achtung: halbe Boomdicke kommt noch zur Elementlaenge hinzu! (7mm)"
@@ -62,138 +62,138 @@
     boom_r        = 0.016  / 2.0
     segs_dipole   = 19
     segs_boom     =  5
     d_boom        = 0.005
 
     # This would add half of the boom length, element lengths claim to
     # be with boom length included, but see comments above
-    # for n in range (len (lengths)) :
+    # for n in range (len (lengths)):
     #     lengths [n] = lengths [n] + boom_r
 
     def __init__ \
         ( self
         , lengths     = lengths
         , dists       = dists
         , boom_r      = boom_r
         , d_boom      = d_boom
         , wire_radius = wire_radius
         , tline       = False
         , ** kw
-        ) :
+        ):
         self.lengths     = lengths
         self.dists       = dists
         self.boom_r      = boom_r
         self.d_boom      = d_boom + 2 * boom_r
         self.wire_radius = wire_radius
         self.tline       = tline
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def cmdline (self) :
+    def cmdline (self):
         c = 1
         r = []
-        for l in self.lengths :
+        for l in self.lengths:
             s = ' '
-            if c % 4 == 0 :
+            if c % 4 == 0:
                 s = '\n'
             r.append ('-l %1.4f%s' % (l, s))
             c += 1
-        for d in self.dists :
+        for d in self.dists:
             s = ' '
-            if c % 4 == 0 :
+            if c % 4 == 0:
                 s = '\n'
             r.append ('-d %1.4f%s' % (l, s))
             c += 1
         return "".join (r)
     # end def cmdline
 
-    def geometry (self, nec = None) :
-        if nec is None :
+    def geometry (self, nec = None):
+        if nec is None:
             nec = self.nec
         geo = nec.get_geometry ()
         self.tag = 1
         self.ex  = None
         dists = [0.0] + self.dists
         bpos  = 0.0
         tltag = []
-        for n, (l, d) in enumerate (zip (self.lengths, dists)) :
+        for n, (l, d) in enumerate (zip (self.lengths, dists)):
             dm = 1 - 2 * (n & 1)
-            for nb, boomdist in enumerate ((0, self.d_boom)) :
+            for nb, boomdist in enumerate ((0, self.d_boom)):
                 boom_inv = 1 - 2 * (nb & 1)
                 dir = dm * boom_inv
                 geo.wire \
                     ( self.tag
                     , self.segs_dipole
                     , boomdist, d + bpos, 0
                     , boomdist, d + bpos, l * dir
                     , self.wire_radius
                     , 1, 1
                     )
                 self.tag += 1
-                if d and not self.tline :
+                if d and not self.tline:
                     geo.wire \
                         ( self.tag
                         , self.segs_boom
                         , boomdist, bpos,     0
                         , boomdist, bpos + d, 0
                         , self.boom_r
                         , 1, 1
                         )
                     self.tag += 1
-            if self.tline :
+            if self.tline:
                 geo.wire \
                     ( self.tag
                     , 1
                     ,        0, d + bpos, 0
                     , boomdist, d + bpos, 0
                     , self.wire_radius
                     , 1, 1
                     )
                 tltag.append (self.tag)
                 self.tag += 1
             bpos += d
 
-        if self.tline :
+        if self.tline:
             self.ex = Excitation (tltag [-1], 1)
-        else :
+        else:
             geo.wire \
                 ( self.tag
                 , 1 # only one segment for feeding
                 , 0,        bpos, 0
                 , boomdist, bpos, 0
                 , self.boom_r
                 , 1, 1
                 )
             self.ex = Excitation (self.tag, 1)
             self.tag += 1
         # Turn around Y by 270 deg, move everything up
         #geo.move (0, 270, 0, 0, 0, self.up, 0, 0, 0)
         nec.geometry_complete (0)
-        if self.tline :
+        if self.tline:
             impedance = transmission_line_z_square \
                 (2 * self.boom_r, 2 * self.boom_r + self.d_boom)
             impedance = 50.0
             last = None
-            for n, t in enumerate (tltag) :
-                if last :
+            for n, t in enumerate (tltag):
+                if last:
                     d = self.dists [n - 1]
                     nec.tl_card (last, 1, t, 1, -impedance, d, 0, 0, 0, 0)
                 last = t
     # end def geometry
 
     @property
-    def up (self) :
+    def up (self):
         """ move everything up by max (reflector length, lambda_4 + r)
         """
         return max (self.reflector, self.lambda_4 + self.dipole_radius)
     # end def up
 
 # end class Logperiodic
 
-def main () :
+def main ():
     cmd = Arg_Handler ()
     cmd.add_argument \
         ( '-b', '--boom-distance'
         , type    = float
         , help    = "Distance between booms"
         , default = 0.002
         )
@@ -211,38 +211,27 @@
         )
     cmd.add_argument \
         ( '-t', '--use-transmission-line'
         , help    = "Use transmission line instead of solid boom"
         , action  = 'store_true'
         )
     args = cmd.parse_args ()
-    if not args.distance :
+    if not args.distance:
         args.distance = Logperiodic.dists
-    if not args.length :
+    if not args.length:
         args.length = Logperiodic.lengths
-    if args.action == 'optimize' :
+    if args.action == 'optimize':
         do = Folded_Dipole_Optimizer (** cmd.default_optimization_args)
         do.run ()
-    else :
+    else:
         ant = Logperiodic \
             ( lengths     = args.length
             , dists       = args.distance
             , d_boom      = args.boom_distance
             , tline       = args.use_transmission_line
             , ** cmd.default_antenna_args
             )
-        if args.action == 'necout' :
-            print (ant.as_nec ())
-        elif args.action not in actions :
-            cmd.print_usage ()
-        else :
-            ant.compute ()
-        if args.action == 'swr' :
-            ant.swr_plot ()
-        elif args.action == 'gain' :
-            ant.plot ()
-        elif args.action == 'frgain' :
-            print ('\n'.join (ant.show_gains ()))
+        antenna_actions (cmd, args, ant)
 # end def main
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     main ()
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/statstool.py` & `antenna-optimizer-0.3/antenna_optimizer/statstool.py`

 * *Files 6% similar despite different names*

```diff
@@ -4,72 +4,72 @@
 import re
 import math
 from argparse import ArgumentParser
 from rsclib.stateparser import Parser
 
 # Parse statistics and create summary
 
-class Optimization_Parser (Parser) :
+class Optimization_Parser (Parser):
     encoding = None
 
     re_tbl = re.compile (r'^R\s+Gain')
     re_num = re.compile (r'^([0-9 .]+)')
 
     #      State   Pattern  new State Action
     matrix = \
         [ ["init", re_tbl,  "tbl",    "start_table"]
         , ["init", None,    "init",   None]
         , ["tbl",  re_num,  "tbl",    "table_line"]
         , ["tbl",  None,    "init",   "end_table"]
         ]
 
-    def __init__ (self) :
+    def __init__ (self):
         self.head = None
         self.__super.__init__ ()
     # end def __init__
 
-    def start_table (self, state, new_state, match) :
+    def start_table (self, state, new_state, match):
         self.head = self.line.strip ().split ()
         assert 7 <= len (self.head) <= 8
         self.cols = []
-        for k in self.head :
+        for k in self.head:
             self.cols.append ([])
     # end def start_table
 
-    def table_line (self, state, new_state, match) :
+    def table_line (self, state, new_state, match):
         l = match.group (1).strip ().split ()
-        if len (l) < len (self.cols) :
+        if len (l) < len (self.cols):
             return
-        for n, k in enumerate (l) :
+        for n, k in enumerate (l):
             self.cols [n].append (float (k))
-            if n == len (self.cols) - 1 :
+            if n == len (self.cols) - 1:
                 break
     # end def table_line
 
-    def end_table (self, state, new_state, match) :
+    def end_table (self, state, new_state, match):
         assert self.head
-        for n, c in enumerate (self.cols) :
+        for n, c in enumerate (self.cols):
             mean = sum (c) / len (c)
             sdev = 0
-            for v in c :
+            for v in c:
                 sdev += (mean - v) ** 2
             sdev = math.sqrt (sdev / len (c))
             print ("%11s: %9.2f %9.2f" % (self.head [n], mean, sdev))
         self.head = None
     # end def end_table
 
 # end class Optimization_Parser
 
-class Optimization_Result :
+class Optimization_Result:
 
-    def __init__ (self, eval) :
+    def __init__ (self, eval):
         self.best_eval = eval
     # end def __init__
 
-    def __str__ (self) :
+    def __str__ (self):
         s = []
         s.append ("%02d"       % self.random_seed)
         s.append ("%5.2f"      % self.gmax)
         s.append ("%5.2f"      % self.fb)
         s.append ("%5.2f"      % self.vswr [0])
         s.append ("%5.2f"      % self.vswr [2])
         s.append ("%7.2f"      % self.best_eval)
@@ -77,15 +77,15 @@
         s.append ("       %7d" % self.n_eval)
         return ' '.join (s)
     # end def __str__
     __repr__ = __str__
 
 # end class Optimization_Result
 
-class Result_Parser (Parser) :
+class Result_Parser (Parser):
     encoding = None
 
     re_best    = re.compile (r'^The Best Evaluation:\s+([0-9.eE+]+)[.]$')
     re_cmdline = re.compile (r'^((-[^ ]\s+[0-9.]+\s*)+)')
     re_swr     = re.compile (r'^VSWR:\s+\[((([0-9.]+)[, +]*){3})\]')
     re_max     = re.compile (r'^GMAX:\s+([-0-9.]+),\s+RMAX:\s+([-0-9.]+)')
     re_cache   = re.compile (r'Cache hits:\s+([0-9]+)/([0-9]+)\s+([0-9.]+)%')
@@ -106,119 +106,119 @@
         , ["result", re_cache,      "result",    "cache"]
         , ["result", re_iter,       "result",    "iterations"]
         , ["result", re_gene,       "init",      "gene"]
         , ["result", re_bingene,    "init",      "gene"]
         , ["result", None,          "result",    None]
         ]
 
-    def __init__ (self) :
+    def __init__ (self):
         self.opt_results = []
         self.opt         = None
         self.randseed    = None
         self.iiter       = 0
         self.__super.__init__ ()
     # end def __init__
 
-    def __iter__ (self) :
-        for opt in self.opt_results :
+    def __iter__ (self):
+        for opt in self.opt_results:
             yield (opt)
     # end def __iter__
 
-    def set_random_seed (self, random_seed) :
+    def set_random_seed (self, random_seed):
         self.randseed = random_seed
     # end def set_random_seed
 
-    def result_iter (self) :
+    def result_iter (self):
         yield ("R  Gain  f/b    SWR   SWR  Eval    Generations Evaluations")
-        for opt in self :
+        for opt in self:
             yield (str (opt))
     # end def result_iter
 
-    def intermediate_iter (self, state, new_state, match) :
+    def intermediate_iter (self, state, new_state, match):
         self.iiter = int (match.group (1))
     # end def intermediate_iter
 
-    def eval (self, state, new_state, match) :
+    def eval (self, state, new_state, match):
         evaluation = float (match.group (1))
         self.opt   = Optimization_Result (evaluation)
         self.opt.generations = self.iiter
         self.iiter = 0
-        if self.randseed :
+        if self.randseed:
             self.opt.random_seed = self.randseed
             self.randseed   = None
         self.opt_results.append (self.opt)
     # end def eval
 
-    def cmd (self, state, new_state, match) :
+    def cmd (self, state, new_state, match):
         self.opt.cmdline = match.group (1)
     # end def cmd
 
-    def swr (self, state, new_state, match) :
+    def swr (self, state, new_state, match):
         self.opt.vswr = [float (x) for x in match.group (1).split (', ')]
     # end def swr
 
-    def maxgain (self, state, new_state, match) :
+    def maxgain (self, state, new_state, match):
         self.opt.gmax = float (match.group (1))
         self.opt.rmax = float (match.group (2))
         self.opt.fb   = self.opt.gmax - self.opt.rmax
     # end def maxgain
 
-    def cache (self, state, new_state, match) :
+    def cache (self, state, new_state, match):
         self.opt.cache_hits    = float (match.group (1))
         self.opt.n_eval        = float (match.group (2))
         self.opt.cache_percent = float (match.group (3))
     # end def cache
 
-    def iterations (self, state, new_state, match) :
+    def iterations (self, state, new_state, match):
         self.opt.generations   = float (match.group (1))
         # Will overwrite previous result from cache, the new value also
         # has the first popsize evals in the 0th generation
         self.opt.n_eval        = float (match.group (2))
         self.opt.stag_count    = float (match.group (3))
     # end def iterations
 
-    def gene (self, state, new_state, match) :
+    def gene (self, state, new_state, match):
         self.opt.gene = match.group (1)
         self.opt      = None
     # end def gene
 
 # end class Result_Parser
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     cmd = ArgumentParser ()
     cmd.add_argument \
         ( 'files'
         , help  = "Files to parse"
         , nargs = "+"
         )
     cmd.add_argument \
         ( '-o', '--optimization-lines'
         , action  = "store_true"
         , help    = "Parse optimization result lines, not optimizer run output"
         )
     args = cmd.parse_args ()
-    if args.optimization_lines :
-        if len (args.files) > 1 :
+    if args.optimization_lines:
+        if len (args.files) > 1:
             print ("Only one file for -o option", file = sys.stderr)
             sys.exit (1)
         op = Optimization_Parser ()
-        with open (args.files [0], 'r') as f :
+        with open (args.files [0], 'r') as f:
             op.parse (f)
-        if op.head :
+        if op.head:
             op.end_table ('', '', '')
-    else :
+    else:
         digi = re.compile (r'^.*[^0-9]([0-9]+)[^/0-9]*$')
         rp   = Result_Parser ()
-        for fn in args.files :
+        for fn in args.files:
             d = digi.search (fn)
             rp.set_random_seed (int (d.group (1)))
             #print (fn, d.group (1))
-            with open (fn, 'r') as f :
+            with open (fn, 'r') as f:
                 rp.parse (f)
-        for line in rp.result_iter () :
+        for line in rp.result_iter ():
             print (line)
         print ("")
         op = Optimization_Parser ()
         op.parse (rp.result_iter ())
-        if op.head :
+        if op.head:
             op.end_table ('', '', '')
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/tl.py` & `antenna-optimizer-0.3/antenna_optimizer/tl.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/python3
 from __future__ import print_function
 
 from .antenna_model import Antenna_Model, Antenna_Optimizer, Excitation
-from .antenna_model import Arg_Handler
-from .coaxmodel     import belden_8295, sytronic_RG213UBX, sytronic_RG_58_CU
+from .antenna_model import Arg_Handler, antenna_actions
+from .coaxmodel     import coax_models
 
-class Transmission_Line_Match (Antenna_Model) :
+class Transmission_Line_Match (Antenna_Model):
     wire_radius = 2e-3
     wire_len    = 0.005
     # Use wire_len for transmission lines: Since we're specifying the
     # transmission line length as a parameter to the TL card anyway we
     # can simplify the structure by not reserving so much space.
     use_wlen    = True
     feed_len    =  9.86
@@ -30,66 +30,67 @@
         , is_series = False
         , f_mhz     = None
         , coaxmodel = None
         , z_load    = None
         , frqstart  = None
         , frqend    = None
         , **kw
-        ) :
+        ):
         self.stub_dist = stub_dist
         self.stub_len  = stub_len
         self.is_open   = is_open
         self.is_series = is_series
         self.coaxmodel = coaxmodel
-        if z_load is not None :
+        if z_load is not None:
             self.z_load = z_load
-        if f_mhz is not None :
-            if frqstart is None :
+        if f_mhz is not None:
+            if frqstart is None:
                 self.frqstart  = f_mhz - 0.01
-            else :
+            else:
                 self.frqstart  = frqstart
-            if frqend is None :
+            if frqend is None:
                 self.frqend    = f_mhz + 0.01
-            else :
+            else:
                 self.frqend    = frqend
-        self.f_mhz     = (self.frqstart + self.frqend) / 2.0
-        self.frequency = self.f_mhz * 1e6
+        self.frq_ranges = [(self.frqstart, self.frqend)]
+        self.f_mhz      = (self.frqstart + self.frqend) / 2.0
+        self.frequency  = self.f_mhz * 1e6
 
-        if self.coaxmodel :
+        if self.coaxmodel:
             self.coaxmodel.f = self.frequency
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def cmdline (self) :
+    def cmdline (self):
         r = []
-        if self.is_open :
+        if self.is_open:
             r.append ('--is-open')
-        if self.is_series :
+        if self.is_series:
             r.append ('--is-series')
-        if self.coaxmodel :
+        if self.coaxmodel:
             r.append ('-c %s' % self.coaxmodel.name)
         r.append ('-d %(stub_dist)1.10f')
         r.append ('-l %(stub_len)1.10f')
         r.append ('-f %(f_mhz)1.2f')
         r.append ('-z %.2f%+.2fj' % (self.z_load.real, self.z_load.imag))
         return ' '.join (r) % self.__dict__
     # end def cmdline
 
-    def geometry (self, nec = None) :
-        if nec is None :
+    def geometry (self, nec = None):
+        if nec is None:
             nec = self.nec
         geo = nec.get_geometry ()
         sd = self.stub_dist
-        if self.use_wlen :
+        if self.use_wlen:
             sd = self.wire_len
         sl = self.stub_len
-        if self.use_wlen :
+        if self.use_wlen:
             sl = self.wire_len
         fl = self.feed_len
-        if self.use_wlen :
+        if self.use_wlen:
             fl = self.wire_len
         self.tag = 1
         self.ex  = None
         geo.wire \
             ( self.tag
             , 1
             , 0,             0, 0
@@ -105,15 +106,15 @@
             , 0,             sd, 0
             , self.wire_len, sd, 0
             , self.wire_radius
             , 1, 1
             )
         self.stub_point_tag = self.tag
         self.tag += 1
-        if self.is_series :
+        if self.is_series:
             geo.wire \
                 ( self.tag
                 , 1
                 , 0, sd,                 0
                 , 0, sd + self.wire_len, 0
                 , self.wire_radius
                 , 1, 1
@@ -145,44 +146,44 @@
                 , 0,             sd + self.wire_len, 0
                 , self.wire_len, sd + self.wire_len, 0
                 , self.wire_radius
                 , 1, 1
                 )
             self.feed_end_tag = self.tag
             self.tag += 1
-        else :
+        else:
             self.stub_start_tag = self.tag - 1
             self.feed_end_tag   = self.tag - 1
             geo.wire \
                 ( self.tag
                 , 1
                 , 0,             sd, -sl
                 , self.wire_len, sd, -sl
                 , self.wire_radius
                 , 1, 1
                 )
             self.stub_end_tag = self.tag
             self.tag += 1
         feedlen = sd + fl
-        if self.is_series :
+        if self.is_series:
             feedlen += self.wire_len
         geo.wire \
             ( self.tag
             , 1
             , 0,             feedlen, 0
             , self.wire_len, feedlen, 0
             , self.wire_radius
             , 1, 1
             )
         self.ex = Excitation (self.tag, 1)
     # end def geometry
 
-    def handle_coaxmodel (self, nec, f) :
+    def handle_coaxmodel (self, nec, f):
         z_coax = 0.0
-        if self.is_open :
+        if self.is_open:
             # We *can* model an open circuit in coaxmodel
             z_coax = None
         y11 = self.coaxmodel.y11 (f * 1e6, self.stub_dist)
         y12 = self.coaxmodel.y12 (f * 1e6, self.stub_dist)
         y22 = self.coaxmodel.y22 (f * 1e6, self.stub_dist, self.z_load)
         nec.nt_card \
             ( self.stub_point_tag, 1
@@ -207,27 +208,27 @@
             , self.feed_end_tag, 1
             , self.z0
             , self.feed_len
             , 0, 0, 0, 0
             )
     # end def handle_coaxmodel
 
-    def transmission_line (self, nec = None) :
-        if nec is None :
+    def transmission_line (self, nec = None):
+        if nec is None:
             nec = self.nec
         # The stub termination is an admittance!
         y_stub = 1e30
         z_coax = 0.0
-        if self.is_open :
+        if self.is_open:
             y_stub = 0
             # We *can* model an open circuit in coaxmodel
             z_coax = None
-        if self.coaxmodel :
+        if self.coaxmodel:
             self.register_frequency_callback (self.handle_coaxmodel)
-        else :
+        else:
             y_load = 1 / self.z_load
             nec.tl_card \
                 ( self.stub_point_tag, 1
                 , self.load_wire_tag,  1
                 , self.z0
                 , self.stub_dist
                 , 0, 0, y_load.real, y_load.imag
@@ -248,82 +249,84 @@
                 , self.feed_len
                 , 0, 0, 0, 0
                 )
     # end def transmission_line
 
 # end class Transmission_Line_Match
 
-class Transmission_Line_Optimizer (Antenna_Optimizer) :
+class Transmission_Line_Optimizer (Antenna_Optimizer):
+    ant_cls = tl = Transmission_Line_Match
 
     def __init__ \
         ( self
         , is_open      = False
         , is_series    = False
         , add_lambda_4 = False
         , f_mhz        = None
         , coaxmodel    = None
         , z_load       = 150.0
         , **kw
-        ) :
+        ):
         self.is_open      = is_open
         self.is_series    = is_series
         self.add_lambda_4 = add_lambda_4
         self.f_mhz        = f_mhz
         self.coaxmodel    = coaxmodel
         self.z_load       = z_load
         c  = 3e8
-        tl = Transmission_Line_Match
-        if f_mhz is None :
-            self.f_mhz = (tl.frqstart + tl.frqend) / 2
+        if f_mhz is None:
+            self.f_mhz = (self.tl.frqstart + self.tl.frqend) / 2
         self.lambda_4 = c / 1e6 / self.f_mhz / 4
-        if self.coaxmodel :
+        if self.coaxmodel:
             self.lambda_4 = self.coaxmodel.lamda (self.f_mhz * 1e6) / 4
         self.minmax = [(0, self.lambda_4), (0, 2 * self.lambda_4)]
-        if self.add_lambda_4 :
+        if self.add_lambda_4:
             self.minmax [0] = (self.lambda_4, 2 * self.lambda_4)
         self.__super.__init__ (**kw)
     # end def __init__
 
-    def compute_antenna (self, p, pop) :
+    def compute_antenna (self, p, pop):
         stub_dist = self.get_parameter (p, pop, 0)
         stub_len  = self.get_parameter (p, pop, 1)
-        tl = Transmission_Line_Match \
+        tl = self.ant_cls \
             ( stub_dist      = stub_dist
             , stub_len       = stub_len
             , is_open        = self.is_open
             , is_series      = self.is_series
-            , frqidxmax      = 3
-            , wire_radius    = self.wire_radius
-            , copper_loading = self.copper_loading
             , f_mhz          = self.f_mhz
             , coaxmodel      = self.coaxmodel
             , z_load         = self.z_load
+            , **self.antenna_args
             )
         return tl
     # end def compute_antenna
 
-    def evaluate (self, p, pop) :
-        self.neval += 1
-        ant, vswrs, gmax, rmax, swr_eval, swr_med = self.phenotype (p, pop)
-        return 1.0 / swr_med
+    def evaluate (self, p, pop):
+        pheno = self.phenotype (p, pop)
+        assert len (pheno) == 1
+        pheno = pheno [0]
+        return 1.0 / pheno.swr_med
     # end def evaluate
 
-#    def print_string (self, file, p, pop) :
+#    def print_string (self, file, p, pop):
+#        pheno = self.phenotype (p, pop)
+#        assert len (pheno) == 1
+#        pheno = pheno [0]
 #        antenna, vswrs, gmax, rmax, swr_eval, swr_med = self.phenotype (p, pop)
-#        print ("vswrs: %s" % vswrs, file = file)
-#        print (antenna.as_nec (), file = file)
+#        print ("vswrs: %s" % pheno.vswrs, file = file)
+#        print (pheno.antenna.as_nec (), file = file)
 #    # end def print_string
 
 # end class Transmission_Line_Optimizer
 
-def main () :
-    models = 'lossless', 'belden_8295', 'sytronic_RG213UBX', 'sytronic_RG_58_CU'
+def main ():
+    models = ['lossless'] + list (coax_models)
     cmd = Arg_Handler \
         ( wire_radius    = 0.002
-        , frqidxmax      = 3
+        , frq_step_max   = 3
         , copper_loading = False
         )
     cmd.add_argument \
         ( '-c', '--coaxmodel'
         , help    = "Coax to model, one of %s" % ', '.join (models)
         , default = 'lossless'
         )
@@ -372,57 +375,46 @@
         )
     cmd.add_argument \
         ( '-z', '--z-load'
         , help    = "Impedance at load to be matched"
         , type    = complex
         )
     args = cmd.parse_args ()
-    if args.coaxmodel not in models :
+    if args.coaxmodel not in models:
         print ('Invalid coax model: "%s"' % args.coaxmodel)
         cmd.print_usage ()
-    if args.coaxmodel == 'lossless' :
+    if args.coaxmodel == 'lossless':
         coaxmodel = None
-    else :
-        coaxmodel = globals () [args.coaxmodel]
-    if args.action == 'optimize' :
+    else:
+        coaxmodel = coax_models [args.coaxmodel]
+    if args.action == 'optimize':
         tlo = Transmission_Line_Optimizer \
             ( is_open      = args.is_open
             , is_series    = args.is_series
             , add_lambda_4 = args.add_lambda_4
             , f_mhz        = args.f_mhz
             , coaxmodel    = coaxmodel
             , z_load       = args.z_load
             , ** cmd.default_optimization_args
             )
         tlo.run ()
-    else :
+    else:
         d = dict \
             ( stub_dist = args.stub_distance
             , stub_len  = args.stub_length
             , is_open   = args.is_open
             , is_series = args.is_series
             , f_mhz     = args.f_mhz
             , coaxmodel = coaxmodel
             , z_load    = args.z_load
             , ** cmd.default_antenna_args
             )
-        if args.frqstart_mhz :
+        if args.frqstart_mhz:
             d ['frqstart'] = args.frqstart_mhz
-        if args.frqend_mhz :
+        if args.frqend_mhz:
             d ['frqend']   = args.frqend_mhz
         tl = Transmission_Line_Match (** d)
-        if args.action == 'necout' :
-            print (tl.as_nec ())
-        elif args.action not in cmd.actions :
-            cmd.print_usage ()
-        else :
-            tl.compute ()
-        if args.action == 'swr' :
-            tl.swr_plot ()
-        elif args.action == 'gain' :
-            tl.plot ()
-        elif args.action == 'frgain' :
-            print ('\n'.join (tl.show_gains ()))
+        antenna_actions (cmd, args, tl)
 # end def main
 
-if __name__ == '__main__' :
+if __name__ == '__main__':
     main ()
```

### Comparing `antenna-optimizer-0.2/antenna_optimizer/transmission.py` & `antenna-optimizer-0.3/antenna_optimizer/transmission.py`

 * *Files 3% similar despite different names*

```diff
@@ -5,39 +5,39 @@
 c0        = 2.99792458e8
 mu0       = 4e-7 * pi
 eps0      = 1 / (mu0 * c0 ** 2)
 # alternatively: z0 = mu0 * c0
 z0        = sqrt (mu0 / eps0)
 eps_r_air = 1.00054
 
-def transmission_line_z (wire_dia, wire_dist, eps_r = eps_r_air) :
+def transmission_line_z (wire_dia, wire_dist, eps_r = eps_r_air):
     """ Impedance of transmission line
         https://hamwaves.com/zc.circular/en/
         Default eps_r is for air.
         The wire_dist is the distance (center to center) of the two
         wires. Both need to have the same dimension (e.g. mm or cm or in).
     """
     zc   = z0 / (pi * sqrt (eps_r)) * acosh (wire_dist / wire_dia)
     return zc
 # end def transmission_line_z
 
-def transmission_line_z_square (wire_dia, wire_dist) :
+def transmission_line_z_square (wire_dia, wire_dist):
     """ Impedance of transmission line with two square conductors
         https://www.owenduffy.net/calc/tstl.htm
         https://hamwaves.com/zc.square/en/
         For now no eps_r can be specified.
     """
     a=0.539774145266
     b=0.404050444546
     c=0.009504588299
     zc = log ((wire_dist / wire_dia - a) / b) / c
     return zc
 # end transmission_line_z_square
 
-class Z_Interpolation (object) :
+class Z_Interpolation (object):
     """ Z-Interpolation by Hartwig Harm, DH2MIC
         http://dh2mic.darc.de/tlc/tlc.pdf
         Note that instead of the inner diameter Harm uses the distance
         from the center of the inner conductor to the outer conductor.
         These are more like radii and he calls them a and b. So
         wire_dist in the other formulae above is 2 * a.  This means for
         the two-wire cases in free space, the distance is 2 * a.
@@ -78,35 +78,35 @@
         have the exact version above) we need to take the resulting Z
         with factor 2, this is the class parameter mult. For other
         structures the resulting Z is used as-is. The z_interpolation is
         off by 0.07% (exactly the same) in all cases, not yet clear why.
 
     >>> zi  = Z_Interpolation ("two round conductors", mult = 2.0)
     >>> dia = 10.0
-    >>> for i in (15, 30, 50, 65, 80) :
+    >>> for i in (15, 30, 50, 65, 80):
     ...     t = transmission_line_z (10.0, 1.0 * i)
     ...     z = zi.z_interpolation  (10.0, 0.5 * i)
     ...     err = abs (t - z) / t * 100
     ...     print ("%3.3f %7.3f %7.3f %7.5f%%" % (1.0 * i, t, z, err))
     15.000 115.380 115.460 0.06923%
     30.000 211.326 211.473 0.06923%
     50.000 274.827 275.018 0.06923%
     65.000 306.782 306.995 0.06923%
     80.000 331.920 332.149 0.06923%
-    >>> for i in (15, 30, 50, 65, 80) :
+    >>> for i in (15, 30, 50, 65, 80):
     ...     t = transmission_line_z   (10.0, 1.0 * i)
     ...     z = z_two_wire_line_round (10.0, 0.5 * i)
     ...     err = abs (t - z) / t * 100
     ...     print ("%3.3f %7.3f %7.3f %7.5f%%" % (1.0 * i, t, z, err))
     15.000 115.380 115.460 0.06923%
     30.000 211.326 211.473 0.06923%
     50.000 274.827 275.018 0.06923%
     65.000 306.782 306.995 0.06923%
     80.000 331.920 332.149 0.06923%
-    >>> for x in range (3, 17) :
+    >>> for x in range (3, 17):
     ...     v1 = transmission_line_z_square (10.0, 5.0 * x)
     ...     v2 = z_two_wire_line_square     (10.0, 2.5 * x)
     ...     err = abs (v1 - v2) / v1 * 100.0
     ...     print ("%3.3f %7.3f %7.3f %7.5f%%" % (5.0 * x, v1, v2, err))
     15.000  91.075  96.916 6.41324%
     20.000 135.178 137.222 1.51278%
     25.000 166.159 166.306 0.08858%
@@ -117,15 +117,15 @@
     50.000 252.658 252.277 0.15091%
     55.000 263.838 263.866 0.01081%
     60.000 273.942 274.422 0.17510%
     65.000 283.160 284.115 0.33709%
     70.000 291.636 293.077 0.49425%
     75.000 299.479 301.412 0.64539%
     80.000 306.778 309.202 0.79002%
-    >>> def f (fun, a, b, c=0) :
+    >>> def f (fun, a, b, c=0):
     ...     print ("%6.2f" % fun (a, b, c))
     >>> f (z_round,                    3.0, 10.0)
     113.80
     >>> f (z_rectangular,              3.0, 10.0, 14.0)
     125.36
     >>> f (z_rectangular,              3.0, 10.0, 23.0)
     127.84
@@ -163,33 +163,33 @@
     143.59
     >>> f (z_two_wire_line_round,      3.0, 10.0)
     310.07
     >>> f (z_two_wire_line_square,     3.0, 10.0)
     287.18
     """
 
-    def __init__ (self, name, kmin = 2.0, kmax = 0, exp = 0, mult = 1.0) :
+    def __init__ (self, name, kmin = 2.0, kmax = 0, exp = 0, mult = 1.0):
         self.name  = name
         self.kmin  = kmin
         self.kmax  = kmax
-        if kmax == 0 :
+        if kmax == 0:
             self.k     = kmin
             self.log2k = log (self.k) / log (2.0)
         self.mult  = mult
         self.exp   = exp
     # end def __init__
 
-    def k_factor (self, a, b) :
+    def k_factor (self, a, b):
         """ Getting the object from a function is different for python3
             and python2. So we add a function for retrieving the object
             first.
-        >>> def get_obj (f) :
-        ...     try :
+        >>> def get_obj (f):
+        ...     try:
         ...         return f.__self__
-        ...     except AttributeError :
+        ...     except AttributeError:
         ...         pass
         ...     return f.im_self
         >>> obj = get_obj (z_rectangular)
         >>> a = z_rectangular (3.0, 10.0, 14.0)
         >>> print ("%6.4f" % obj.k)
         1.2145
         >>> a = z_rectangular (3.0, 10.0, 23.0)
@@ -243,17 +243,17 @@
             / (1.0 + p * (1.0 * a / b) ** self.exp)
             )
         self.q = q
         self.k = 1.0 + m * q
         self.log2k = log (self.k) / log (2.0)
     # end def k_factor
 
-    def z_interpolation (self, wire_dia, a, b = 0, eps_r = eps_r_air) :
-        if self.kmax :
-            if a > b :
+    def z_interpolation (self, wire_dia, a, b = 0, eps_r = eps_r_air):
+        if self.kmax:
+            if a > b:
                 a, b = b, a
             self.k_factor (a, b)
         factor = 2.0 * a / wire_dia
         zc = \
             ( 60.0 / sqrt (eps_r)
             * ( log (factor)
               + self.log2k * log (1.0 + sqrt (1.0 - (factor ** -2)))
@@ -315,39 +315,39 @@
 
 z_two_wire_line_square     = Z_Interpolation \
     ( "two square conductors"
     , kmin = 1.65, mult = 2.0
     ).z_interpolation
 
 
-def wire_L_from_Z (z, eps_r = eps_r_air) :
+def wire_L_from_Z (z, eps_r = eps_r_air):
     """ Compute L (per length) from Zo
     """
     return z * sqrt (eps_r) / c0
 # end def wire_L_from_Z
 
-def wire_C_from_Z (z, eps_r = eps_r_air) :
+def wire_C_from_Z (z, eps_r = eps_r_air):
     """ Compute C (per length) from Zo
     """
     return sqrt (eps_r) / (z * c0)
 # end def wire_C_from_Z
 
-def phase_shift (f, length, vf = 1) :
+def phase_shift (f, length, vf = 1):
     """ Compute phase shift in radians for a phasing stub with the given
         length and the given frequency f (Hz).
     >>> print ("%1.3f" % phase_shift (435000000, .35))
     3.191
     """
     lamb  = c0 / f
     lvf   = lamb * vf
     phase = (length % lvf) / lvf * 2 * pi
     return phase
 # end def phase_shift
 
-def complex_voltage (phi, u = 1) :
+def complex_voltage (phi, u = 1):
     """ Given a phase phi (in rad) and a voltage (with only real part)
         return the complex voltage (real, imag)
     >>> print ("%2.3f %2.3f" % complex_voltage (pi))
     -1.000 0.000
     >>> print ("%2.3f %2.3f" % complex_voltage (2 * pi))
     1.000 -0.000
     >>> print ("%2.3f %2.3f" % complex_voltage (pi / 2))
```

### Comparing `antenna-optimizer-0.2/setup.py` & `antenna-optimizer-0.3/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 #!/usr/bin/env python3
-# Copyright (C) 2019-21 Dr. Ralf Schlatterbeck Open Source Consulting.
+# Copyright (C) 2019-22 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # ****************************************************************************
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are
 # met:
 #
@@ -23,26 +23,20 @@
 # TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
 # PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
 # LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
 # NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
 # SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
 # ****************************************************************************
 
-from warnings       import filterwarnings
-from distutils.core import setup, Extension
+from setuptools import setup
 try :
     from antenna_optimizer.Version import VERSION
 except :
     VERSION = None
 
-filterwarnings \
-    ( "ignore"
-    , "Unknown distribution option: 'install_requires'"
-    )
-
 description = []
 with open ('README.rst') as f :
     for line in f :
             description.append (line)
 
 license     = 'BSD License'
 setup \
@@ -53,34 +47,40 @@
     , license          = license
     , author           = "Ralf Schlatterbeck"
     , author_email     = "rsc@runtux.com"
     , install_requires = [ 'matplotlib', 'numpy', 'scipy'
                          , 'pgapy',  'pynec', 'rsclib'
                          ]
     , packages         = ['antenna_optimizer']
-    , package_data     = dict
-        (hamradio = ['data/*.txt', 'data/*.dat', 'data/*.html'])
     , platforms        = 'Any'
     , python_requires  = '>=3.7'
-    , scripts          = [ 'bin/coaxmodel'
-                         , 'bin/folded_3ele_antenna'
-                         , 'bin/folded_antenna'
-                         , 'bin/folded_bc_antenna'
-                         , 'bin/folded_bigrefl_antenna'
-                         , 'bin/hb9cv_antenna'
-                         , 'bin/logper_antenna'
-                         , 'bin/transmission_line'
-                         ]
+    , entry_points     = dict
+        ( console_scripts =
+            [ 'coaxmodel=antenna_optimizer.coaxmodel:main'
+            , 'folded-3ele-antenna=antenna_optimizer.folded_3ele:main'
+            , 'folded-antenna=antenna_optimizer.folded:main'
+            , 'folded-bc-antenna=antenna_optimizer.folded_bc:main'
+            , 'folded-bigrefl-antenna=antenna_optimizer.folded_bigrefl:main'
+            , 'hb9cv-antenna=antenna_optimizer.hb9cv:main'
+            , 'hf-folded-dipole=antenna_optimizer.hf_folded:main'
+            , 'hf-fuchs=antenna_optimizer.hf_fuchs:main'
+            , 'hf-inverted-v=antenna_optimizer.hf_inverted_v:main'
+            , 'logper-antenna=antenna_optimizer.logper:main'
+            , 'multi-dipole=antenna_optimizer.multi_dipole:main'
+            , 'transmission-line=antenna_optimizer.tl:main'
+            ]
+        )
     , url              = 'https://github.com/schlatterbeck/antenna-optimizer'
     , classifiers      =
         [ 'Development Status :: 5 - Production/Stable'
         , 'License :: OSI Approved :: ' + license
         , 'Operating System :: OS Independent'
         , 'Programming Language :: Python'
         , 'Intended Audience :: Developers'
+        , 'Intended Audience :: Science/Research'
         , 'Programming Language :: Python :: 2'
         , 'Programming Language :: Python :: 2.7'
         , 'Programming Language :: Python :: 3'
         , 'Programming Language :: Python :: 3.5'
         , 'Programming Language :: Python :: 3.6'
         , 'Programming Language :: Python :: 3.7'
         , 'Programming Language :: Python :: 3.8'
```

