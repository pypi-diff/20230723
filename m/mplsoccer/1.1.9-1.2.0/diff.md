# Comparing `tmp/mplsoccer-1.1.9.tar.gz` & `tmp/mplsoccer-1.2.0.tar.gz`

## Comparing `mplsoccer-1.1.9.tar` & `mplsoccer-1.2.0.tar`

### file list

```diff
@@ -1,104 +1,106 @@
--rw-r--r--   0        0        0    20213 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/.pylintrc
--rw-r--r--   0        0        0      451 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/.readthedocs.yml
--rw-r--r--   0        0        0    22411 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/CHANGELOG.md
--rw-r--r--   0        0        0      387 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/environment-dev.yml
--rw-r--r--   0        0        0      323 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/environment-docs.yml
--rw-r--r--   0        0        0      263 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/environment.yml
--rw-r--r--   0        0        0       53 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/requirements.txt
--rw-r--r--   0        0        0      638 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/Makefile
--rw-r--r--   0        0        0      799 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/make.bat
--rw-r--r--   0        0        0   385285 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/quick_start.png
--rw-r--r--   0        0        0    56598 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/quick_start_radar.png
--rw-r--r--   0        0        0    63145 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/Mplsoccer logo github.jpg
--rw-r--r--   0        0        0      238 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/api.rst
--rw-r--r--   0        0        0     3921 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/conf.py
--rw-r--r--   0        0        0   138151 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/explain_standardizer.png
--rw-r--r--   0        0        0     2880 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/index.rst
--rw-r--r--   0        0        0      223 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/installation.rst
--rw-r--r--   0        0        0    93798 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/logo-white.png
--rw-r--r--   0        0        0   123658 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/logo.png
--rw-r--r--   0        0        0      151 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.bumpy_chart.rst
--rw-r--r--   0        0        0      134 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.grid.rst
--rw-r--r--   0        0        0      160 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.linecollection.rst
--rw-r--r--   0        0        0      156 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.pitch.rst
--rw-r--r--   0        0        0      142 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.py_pizza.rst
--rw-r--r--   0        0        0      136 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.quiver.rst
--rw-r--r--   0        0        0      151 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.radar_chart.rst
--rw-r--r--   0        0        0      145 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.statsbomb.rst
--rw-r--r--   0        0        0      137 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/docs/source/mplsoccer.utils.rst
--rw-r--r--   0        0        0      621 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/README.rst
--rw-r--r--   0        0        0       92 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/bumpy_charts/README.rst
--rw-r--r--   0        0        0    10499 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/bumpy_charts/plot_bumpy.py
--rw-r--r--   0        0        0       84 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/README.rst
--rw-r--r--   0        0        0     5303 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_animation.py
--rw-r--r--   0        0        0     4062 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_arrows.py
--rw-r--r--   0        0        0    10554 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_cmap.py
--rw-r--r--   0        0        0     1010 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_convex_hull.py
--rw-r--r--   0        0        0     4144 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_cyberpunk.py
--rw-r--r--   0        0        0     1781 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_delaunay.py
--rw-r--r--   0        0        0     7952 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_fbref.py
--rw-r--r--   0        0        0     5410 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_flow.py
--rw-r--r--   0        0        0    16017 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_grid.py
--rw-r--r--   0        0        0    10158 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_heatmap.py
--rw-r--r--   0        0        0     3990 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_heatmap_positional.py
--rw-r--r--   0        0        0     6477 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_hexbin.py
--rw-r--r--   0        0        0    18384 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_jointgrid.py
--rw-r--r--   0        0        0     7200 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_kde.py
--rw-r--r--   0        0        0     6644 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_lines.py
--rw-r--r--   0        0        0     9458 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_pass_network.py
--rw-r--r--   0        0        0     3344 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_photo.py
--rw-r--r--   0        0        0     1073 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_sb360_frame.py
--rw-r--r--   0        0        0    18274 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_scatter.py
--rw-r--r--   0        0        0     3969 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_shot_freeze_frame.py
--rw-r--r--   0        0        0    11528 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_standardize.py
--rw-r--r--   0        0        0     1233 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_textured_background.py
--rw-r--r--   0        0        0     7942 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_twitter_powerpoint.py
--rw-r--r--   0        0        0     1720 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_plots/plot_voronoi.py
--rw-r--r--   0        0        0       66 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_setup/README.rst
--rw-r--r--   0        0        0     3377 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_setup/plot_compare_pitches.py
--rw-r--r--   0        0        0    14142 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_setup/plot_explain_standardizer.py
--rw-r--r--   0        0        0     8554 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_setup/plot_pitches.py
--rw-r--r--   0        0        0      926 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pitch_setup/plot_quick_start.py
--rw-r--r--   0        0        0       90 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pizza_plots/README.rst
--rw-r--r--   0        0        0    12084 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_basic.py
--rw-r--r--   0        0        0     5803 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_colorful.py
--rw-r--r--   0        0        0     8787 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_comparison.py
--rw-r--r--   0        0        0     9332 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_comparison_vary_scales.py
--rw-r--r--   0        0        0     5812 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_dark_theme.py
--rw-r--r--   0        0        0     3845 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_different_units.py
--rw-r--r--   0        0        0     5173 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_scales_vary.py
--rw-r--r--   0        0        0       92 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/radar/README.rst
--rw-r--r--   0        0        0    23909 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/radar/plot_radar.py
--rw-r--r--   0        0        0     8903 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/radar/plot_turbine.py
--rw-r--r--   0        0        0       71 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/statsbomb/README.rst
--rw-r--r--   0        0        0     2719 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/statsbomb/plot_statsbomb_data.py
--rw-r--r--   0        0        0       58 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/tutorials/README.rst
--rw-r--r--   0        0        0     1934 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/tutorials/plot_wedges.py
--rw-r--r--   0        0        0    11296 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/tutorials/plot_xt.py
--rw-r--r--   0        0        0     9766 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/examples/tutorials/plot_xt_improvements.py
--rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/__about__.py
--rw-r--r--   0        0        0      440 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/__init__.py
--rw-r--r--   0        0        0    53400 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/_pitch_base.py
--rw-r--r--   0        0        0    33672 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/_pitch_plot.py
--rw-r--r--   0        0        0    11518 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/bumpy_chart.py
--rw-r--r--   0        0        0     2306 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/cm.py
--rw-r--r--   0        0        0    19708 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/dimensions.py
--rw-r--r--   0        0        0    14933 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/grid.py
--rw-r--r--   0        0        0    15704 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/heatmap.py
--rw-r--r--   0        0        0    10644 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/linecollection.py
--rw-r--r--   0        0        0     9864 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/pitch.py
--rw-r--r--   0        0        0    21880 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/py_pizza.py
--rw-r--r--   0        0        0     6133 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/quiver.py
--rw-r--r--   0        0        0    34817 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/radar_chart.py
--rw-r--r--   0        0        0    19156 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/scatterutils.py
--rw-r--r--   0        0        0    24921 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/statsbomb.py
--rw-r--r--   0        0        0    11926 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/mplsoccer/utils.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/tests/__init__.py
--rw-r--r--   0        0        0     4221 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/tests/test_bin_statistic.py
--rw-r--r--   0        0        0     1647 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/tests/test_grid.py
--rw-r--r--   0        0        0     3126 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/tests/test_standarizer.py
--rw-r--r--   0        0        0     2325 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/.gitignore
--rw-r--r--   0        0        0     1088 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/LICENSE
--rw-r--r--   0        0        0     3464 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/README.md
--rw-r--r--   0        0        0     1864 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/pyproject.toml
--rw-r--r--   0        0        0     4665 2020-02-02 00:00:00.000000 mplsoccer-1.1.9/PKG-INFO
+-rw-r--r--   0        0        0    20213 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/.pylintrc
+-rw-r--r--   0        0        0      451 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/.readthedocs.yml
+-rw-r--r--   0        0        0    24116 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/CHANGELOG.md
+-rw-r--r--   0        0        0      387 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/environment-dev.yml
+-rw-r--r--   0        0        0      327 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/environment-docs.yml
+-rw-r--r--   0        0        0      263 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/environment.yml
+-rw-r--r--   0        0        0       60 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/requirements.txt
+-rw-r--r--   0        0        0      638 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/Makefile
+-rw-r--r--   0        0        0      799 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/make.bat
+-rw-r--r--   0        0        0   385285 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/quick_start.png
+-rw-r--r--   0        0        0    56598 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/quick_start_radar.png
+-rw-r--r--   0        0        0    63145 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/Mplsoccer logo github.jpg
+-rw-r--r--   0        0        0      238 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/api.rst
+-rw-r--r--   0        0        0     3966 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/conf.py
+-rw-r--r--   0        0        0   138151 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/explain_standardizer.png
+-rw-r--r--   0        0        0     3006 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/index.rst
+-rw-r--r--   0        0        0      318 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/installation.rst
+-rw-r--r--   0        0        0    93798 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/logo-white.png
+-rw-r--r--   0        0        0   123658 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/logo.png
+-rw-r--r--   0        0        0      151 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.bumpy_chart.rst
+-rw-r--r--   0        0        0      134 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.grid.rst
+-rw-r--r--   0        0        0      160 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.linecollection.rst
+-rw-r--r--   0        0        0      156 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.pitch.rst
+-rw-r--r--   0        0        0      142 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.py_pizza.rst
+-rw-r--r--   0        0        0      136 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.quiver.rst
+-rw-r--r--   0        0        0      151 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.radar_chart.rst
+-rw-r--r--   0        0        0      145 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.statsbomb.rst
+-rw-r--r--   0        0        0      137 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/docs/source/mplsoccer.utils.rst
+-rw-r--r--   0        0        0      621 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/README.rst
+-rw-r--r--   0        0        0       92 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/bumpy_charts/README.rst
+-rw-r--r--   0        0        0    10401 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/bumpy_charts/plot_bumpy.py
+-rw-r--r--   0        0        0       84 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/README.rst
+-rw-r--r--   0        0        0     5307 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_animation.py
+-rw-r--r--   0        0        0     4062 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_arrows.py
+-rw-r--r--   0        0        0    10541 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_cmap.py
+-rw-r--r--   0        0        0     1010 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_convex_hull.py
+-rw-r--r--   0        0        0     4144 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_cyberpunk.py
+-rw-r--r--   0        0        0     1781 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_delaunay.py
+-rw-r--r--   0        0        0     7952 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_fbref.py
+-rw-r--r--   0        0        0     5410 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_flow.py
+-rw-r--r--   0        0        0    22127 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_formations.py
+-rw-r--r--   0        0        0    16012 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_grid.py
+-rw-r--r--   0        0        0    10158 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_heatmap.py
+-rw-r--r--   0        0        0     3990 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_heatmap_positional.py
+-rw-r--r--   0        0        0     6477 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_hexbin.py
+-rw-r--r--   0        0        0    18399 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_jointgrid.py
+-rw-r--r--   0        0        0     7158 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_kde.py
+-rw-r--r--   0        0        0     6644 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_lines.py
+-rw-r--r--   0        0        0     9460 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_pass_network.py
+-rw-r--r--   0        0        0     3665 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_photo.py
+-rw-r--r--   0        0        0     1073 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_sb360_frame.py
+-rw-r--r--   0        0        0    18279 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_scatter.py
+-rw-r--r--   0        0        0     3969 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_shot_freeze_frame.py
+-rw-r--r--   0        0        0    11540 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_standardize.py
+-rw-r--r--   0        0        0     1233 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_textured_background.py
+-rw-r--r--   0        0        0     7942 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_twitter_powerpoint.py
+-rw-r--r--   0        0        0     1720 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_plots/plot_voronoi.py
+-rw-r--r--   0        0        0       66 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_setup/README.rst
+-rw-r--r--   0        0        0     3377 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_setup/plot_compare_pitches.py
+-rw-r--r--   0        0        0    14142 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_setup/plot_explain_standardizer.py
+-rw-r--r--   0        0        0     8651 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_setup/plot_pitches.py
+-rw-r--r--   0        0        0      926 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pitch_setup/plot_quick_start.py
+-rw-r--r--   0        0        0       90 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pizza_plots/README.rst
+-rw-r--r--   0        0        0    12084 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_basic.py
+-rw-r--r--   0        0        0     5803 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_colorful.py
+-rw-r--r--   0        0        0     8787 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_comparison.py
+-rw-r--r--   0        0        0     9332 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_comparison_vary_scales.py
+-rw-r--r--   0        0        0     5812 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_dark_theme.py
+-rw-r--r--   0        0        0     3845 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_different_units.py
+-rw-r--r--   0        0        0     5173 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_scales_vary.py
+-rw-r--r--   0        0        0       92 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/radar/README.rst
+-rw-r--r--   0        0        0    23909 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/radar/plot_radar.py
+-rw-r--r--   0        0        0     8905 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/radar/plot_turbine.py
+-rw-r--r--   0        0        0       71 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/statsbomb/README.rst
+-rw-r--r--   0        0        0     2676 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/statsbomb/plot_statsbomb_data.py
+-rw-r--r--   0        0        0       58 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/tutorials/README.rst
+-rw-r--r--   0        0        0     1934 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/tutorials/plot_wedges.py
+-rw-r--r--   0        0        0    11296 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/tutorials/plot_xt.py
+-rw-r--r--   0        0        0     9766 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/examples/tutorials/plot_xt_improvements.py
+-rw-r--r--   0        0        0       22 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/__about__.py
+-rw-r--r--   0        0        0      440 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/__init__.py
+-rw-r--r--   0        0        0    75992 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/_pitch_base.py
+-rw-r--r--   0        0        0    34845 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/_pitch_plot.py
+-rw-r--r--   0        0        0    11518 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/bumpy_chart.py
+-rw-r--r--   0        0        0     2314 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/cm.py
+-rw-r--r--   0        0        0    29268 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/dimensions.py
+-rw-r--r--   0        0        0    56667 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/formations.py
+-rw-r--r--   0        0        0    14933 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/grid.py
+-rw-r--r--   0        0        0    15704 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/heatmap.py
+-rw-r--r--   0        0        0    10652 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/linecollection.py
+-rw-r--r--   0        0        0     9864 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/pitch.py
+-rw-r--r--   0        0        0    21880 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/py_pizza.py
+-rw-r--r--   0        0        0     6133 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/quiver.py
+-rw-r--r--   0        0        0    35525 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/radar_chart.py
+-rw-r--r--   0        0        0    19156 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/scatterutils.py
+-rw-r--r--   0        0        0    25326 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/statsbomb.py
+-rw-r--r--   0        0        0    17727 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/mplsoccer/utils.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/tests/__init__.py
+-rw-r--r--   0        0        0     4221 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/tests/test_bin_statistic.py
+-rw-r--r--   0        0        0     1647 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/tests/test_grid.py
+-rw-r--r--   0        0        0     3126 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/tests/test_standarizer.py
+-rw-r--r--   0        0        0     2325 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/.gitignore
+-rw-r--r--   0        0        0     1088 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/LICENSE
+-rw-r--r--   0        0        0     3574 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/README.md
+-rw-r--r--   0        0        0     1871 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/pyproject.toml
+-rw-r--r--   0        0        0     4780 2020-02-02 00:00:00.000000 mplsoccer-1.2.0/PKG-INFO
```

### Comparing `mplsoccer-1.1.9/.pylintrc` & `mplsoccer-1.2.0/.pylintrc`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/CHANGELOG.md` & `mplsoccer-1.2.0/CHANGELOG.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,54 @@
+:rocket: Version 1.2.0
+----------------------
+
+### Added
+* :heart_eyes: Added the ``formation`` method, which plots formations as text, images, inset axes, \
+scatter plots or pitches.
+* :new: Added the ability to return a dataframe for all the formations and player positions with the \
+``Pitch.formations_dataframe`` attribute and the ``Pitch.get_positions()`` method.
+* :new: Added the ``inset_axes`` and ``inset_image`` methods/functions for plotting \
+inset axes and images.
+* :new: Added the ``Pitch.text`` wrapper for Axes.text, which automatically flips \
+the x and y coordinates.
+* :new: Added the ``xoffset`` and ``yoffset``arguments to the label_heatmap method \
+for plotting a heatmap's labels off-center.
+
+### Breaking Changes
+* :x: Fixed the Matplotlib dependency to version 3.6 or higher.
+* :x: The StatsBomb ``tactics_formation`` is changed from a numeric dtype to a string dtype, \
+e.g. 442 changed to '442'
+
+### Changes
+* :ok: Added the new pitch attributes ``positional_alpha`` and ``shade_alpha`` for \
+controlling the transparency of the positional lines and shaded block in the middle of the pitch. \
+Previously, the alpha was controlled by the ``line_alpha`` attribute.
+
+### Fixes
+* Fixed some deprecation warnings for Matplotlib (get_cmap) and Seaborn (kdeplot).
+
+:rocket: Version 1.1.12
+----------------------
+
+### Fixes
+* Fixed the timestamp conversion for match data.
+
+:rocket: Version 1.1.11
+----------------------
+
+### Added
+* Added the pitch type ``impect`` for plotting [impect data](https://www.impect.com/en/).
+
+:rocket: Version 1.1.10
+----------------------
+
+### Fixes
+* Fixed the StatsBomb lineup parsers so when the player_nickname is missing \
+the parsers still work.
+
 :rocket: Version 1.1.9
 ----------------------
 
 ### Fixes
 * Fixed positional pitch marking to remove extraneous lines when ``Pitch`` is created with 
 ``positional=True``
```

### Comparing `mplsoccer-1.1.9/docs/Makefile` & `mplsoccer-1.2.0/docs/Makefile`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/docs/make.bat` & `mplsoccer-1.2.0/docs/make.bat`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/docs/quick_start.png` & `mplsoccer-1.2.0/docs/quick_start.png`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/docs/quick_start_radar.png` & `mplsoccer-1.2.0/docs/quick_start_radar.png`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/docs/source/Mplsoccer logo github.jpg` & `mplsoccer-1.2.0/docs/source/Mplsoccer logo github.jpg`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/docs/source/conf.py` & `mplsoccer-1.2.0/docs/source/conf.py`

 * *Files 5% similar despite different names*

```diff
@@ -36,14 +36,15 @@
 # extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
 # ones.
 extensions = ['sphinx.ext.autodoc',
               'sphinx.ext.autosummary',
               'sphinx.ext.imgmath',
               'sphinx.ext.viewcode',
               'sphinx_gallery.gen_gallery',
+              'sphinx.ext.autosectionlabel',
               'sphinx.ext.napoleon',
               'numpydoc']
 
 # https://github.com/readthedocs/readthedocs.org/issues/2569
 master_doc = 'index'
 
 # this is needed for some reason...
```

### Comparing `mplsoccer-1.1.9/docs/source/explain_standardizer.png` & `mplsoccer-1.2.0/docs/source/explain_standardizer.png`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/docs/source/index.rst` & `mplsoccer-1.2.0/docs/source/index.rst`

 * *Files 5% similar despite different names*

```diff
@@ -11,14 +11,20 @@
 
 Use the package manager `pip <https://pip.pypa.io/en/stable/>`_ to install mplsoccer.
 
 .. code-block:: bash
 
     pip install mplsoccer
 
+Or install via `Anaconda <https://docs.anaconda.com/free/anaconda/install/index.html>`_
+
+.. code-block:: bash
+
+    conda install -c conda-forge mplsoccer
+
 Plot a StatsBomb pitch:
 
 .. code-block:: python
 
     from mplsoccer.pitch import Pitch
     pitch = Pitch(pitch_color='grass', line_color='white', stripe=True)
     fig, ax = pitch.draw()
@@ -65,19 +71,18 @@
 
 -----------
 Inspiration
 -----------
 
 mplsoccer was inspired by:
 
-- `Peter McKeever <http://petermckeever.com/2020/10/how-to-draw-a-football-pitch/>`_
-  heavily inspired the API design
+- `Peter McKeever <https://petermckeever.com/>`_ heavily inspired the API design
 - `ggsoccer <https://github.com/Torvaney/ggsoccer>`_ influenced the design and Standardizer
 - `lastrow's <https://twitter.com/lastrowview>`_ legendary animations
-- `fcrstats' <http://fcrstats.com/>`_ tutorials for using football data
+- `fcrstats' <https://twitter.com/FC_rstats>`_ tutorials for using football data
 - `fcpython's <https://fcpython.com/>`_ Python tutorials for using football data
 - `Karun Singh's <https://twitter.com/karun1710>`_ expected threat (xT) visualizations
 - `StatsBomb's <https://statsbomb.com/>`_ great visual design and free open-data
 - John Burn-Murdoch's `tweet <https://twitter.com/jburnmurdoch/status/1057907312030085120>`_
   got me interested in football analytics
```

### Comparing `mplsoccer-1.1.9/docs/source/logo-white.png` & `mplsoccer-1.2.0/docs/source/logo-white.png`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/docs/source/logo.png` & `mplsoccer-1.2.0/docs/source/logo.png`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/README.rst` & `mplsoccer-1.2.0/examples/README.rst`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/bumpy_charts/plot_bumpy.py` & `mplsoccer-1.2.0/examples/bumpy_charts/plot_bumpy.py`

 * *Files 3% similar despite different names*

```diff
@@ -33,15 +33,15 @@
 font_normal = FontManager("https://raw.githubusercontent.com/google/fonts/main/apache/"
                           "roboto/Roboto%5Bwdth,wght%5D.ttf")
 font_bold = FontManager("https://raw.githubusercontent.com/google/fonts/main/apache/"
                         "robotoslab/RobotoSlab%5Bwght%5D.ttf")
 
 ##############################################################################
 # Load Files
-# ---------------
+# ----------
 # We will using these images/data in our examples.
 # You can find all the images/data `here <https://github.com/andrewRowlinson/mplsoccer-assets>`_.
 
 epl = Image.open(
     urlopen("https://raw.githubusercontent.com/andrewRowlinson/mplsoccer-assets/main/epl.png")
 )
 
@@ -52,16 +52,16 @@
 player_dict = json.load(
     urlopen("https://raw.githubusercontent.com/andrewRowlinson/mplsoccer-assets/main/"
             "percentile.json")
 )
 
 ##############################################################################
 # Making A Bumpy Chart
-# ----------------------------
-# A Bump Chart is a special form of a line plot.
+# --------------------
+# A Bumpy Chart is a special form of a line plot.
 # This chart is well-suited for exploring changes in rank over time.
 # Using this chart, you can easily compare the position,
 # performance or rankings of multiple observations with
 # respect to each other rather than the actual values itself.
 # We are going to make use of the weekwise standing data for Premier League 2019/20.
 
 # match-week
@@ -123,15 +123,15 @@
 )
 
 # if space is left in the plot use this
 plt.tight_layout(pad=0.5)
 
 ##############################################################################
 # Flip The y-axis
-# ----------------------------
+# ---------------
 # If you want to plot positions from the bottom, i.e. the 1st position will
 # be at the bottom and the 20th position will be at the top. You can do it easily.
 # You just have to pass ``upside_down=True`` inside ``plot`` function.
 
 # instantiate object
 bumpy = Bumpy(
     scatter_color="#282A2C", line_color="#252525",  # scatter and line colors
@@ -182,15 +182,15 @@
 )
 
 # if space is left in the plot use this
 plt.tight_layout(pad=0.5)
 
 ##############################################################################
 # Light Theme
-# ----------------------------
+# -----------
 # You can use ``background_color``, ``scatter_color``, ``label_color``, and ``line_color`` arguments
 # to change the whole theme of the plot. Below is the code demonstrating how to make a light-theme
 # bumpy chart using ``mplsoccer``.
 # Below you can also use ``scatter_points``, ``scatter_primary``, and ``scatter_size``
 # arguments inside ``Bumpy`` method to change markers and their sizes.
 
 # highlight dict --> team to highlight and their corresponding colors
@@ -243,15 +243,15 @@
 )
 
 # if space is left in the plot use this
 plt.tight_layout(pad=0.5)
 
 ##############################################################################
 # Player Percentile Rank Viz
-# ----------------------------
+# --------------------------
 # Here we will create a bumpy-chart that will compare two players based on their percentile rank.
 
 # attributes and highlight dict
 attribute = [
     "xA", "Passes\nInto Pen", "Passes\nInto Final 1/3", "Progressive\nPass Distance",
     "Pass\nReceive%", "Progressive\nCarry Distance"
 ]
@@ -268,22 +268,23 @@
 
 # plot bumpy chart
 fig, ax = bumpy.plot(
     x_list=attribute, y_list=np.linspace(1, 100, 11).astype(int), values=player_dict,
     secondary_alpha=0.05, highlight_dict=highlight_dict,
     figsize=(20, 12),
     x_label="Attributes", y_label="Percentile Rank", ylim=(0.5, 12),
-    upside_down=True,
-    fontfamily="Liberation Serif"
+    upside_down=True
 )
 
 # title and subtitle
 TITLE = "Comparison Between <Cristián Zapata> and <Francesco Acerbi>"
 
 # add title
 fig_text(
     0.02, 0.98, TITLE, color="#F2F2F2",
     highlight_textprops=[{"color": 'crimson'}, {"color": 'cornflowerblue'}],
-    size=34, fig=fig, fontfamily="Liberation Serif"
+    size=34, fig=fig
 )
 # if space is left in the plot use this
 plt.tight_layout(pad=0.5)
+
+plt.show()
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_animation.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_animation.py`

 * *Files 2% similar despite different names*

```diff
@@ -110,15 +110,15 @@
 home, = ax.plot([], [], ms=10, markerfacecolor='#7f63b8', **marker_kwargs)  # purple
 
 
 # animation function
 def animate(i):
     """ Function to animate the data. Each frame it sets the data for the players and the ball."""
     # set the ball data with the x and y positions for the ith frame
-    ball.set_data(df_ball.iloc[i, 3], df_ball.iloc[i, 4])
+    ball.set_data(df_ball.iloc[i, [3]], df_ball.iloc[i, [4]])
     # get the frame id for the ith frame
     frame = df_ball.iloc[i, 1]
     # set the player data using the frame id
     away.set_data(df_away.loc[df_away.Frame == frame, 'x'],
                   df_away.loc[df_away.Frame == frame, 'y'])
     home.set_data(df_home.loc[df_home.Frame == frame, 'x'],
                   df_home.loc[df_home.Frame == frame, 'y'])
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_arrows.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_arrows.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_cmap.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_cmap.py`

 * *Files 3% similar despite different names*

```diff
@@ -24,15 +24,15 @@
 
 # filter chelsea pressure events
 mask_chelsea_pressure = (df.team_name == 'Chelsea FCW') & (df.type_name == 'Pressure')
 df = df.loc[mask_chelsea_pressure, ['x', 'y']]
 
 ##############################################################################
 # cmasher colormaps
-# -----------------------
+# -----------------
 # Cmasher colormaps are scientific colormaps that have been designed to be
 # perceptually uniform (i.e. color changes visually look the same as the value changes)
 # and mostly colorblind friendly. A great choice
 # to get started and potentially more exciting than the default matplotlib choices.
 #
 # Let's first get a dictionary of all the colormaps
 #
@@ -53,15 +53,15 @@
 fig, axs = pitch.grid(nrows=11, ncols=4, space=0.1, figheight=40,
                       title_height=0, endnote_height=0,  # no title/ endnote
                       grid_width=0.9, grid_height=0.98, bottom=0.01, left=0.05)
 cmap_names = list(all_cmap_dict.keys())
 for idx, ax in enumerate(axs.flat):
     cmap_name = f'cmr.{cmap_names[idx]}'
     cmap = all_cmap_dict[cmap_names[idx]]
-    kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=cmap, shade=True, levels=100)
+    kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=cmap, fill=True, levels=100)
     ax_title = ax.set_title(cmap_name, fontsize=15)
 
 ##############################################################################
 # Cmasher kdeplot
 # ---------------
 # I like the look of the voltage colormap so let's plot in against a light and
 # dark background
@@ -72,20 +72,20 @@
 # Reversing the colormaps is sometimes helpful so the high value colors do not bleed into the
 # background. I prefer dark to light colormaps on dark background, and light to dark
 # colormaps on light backgrounds. I have shown this below using the same colormap in reverse.
 
 # dark
 pitch_dark = VerticalPitch(line_color='#cfcfcf', line_zorder=2, pitch_color='#122c3d')
 fig, ax = pitch_dark.draw()
-kdeplot_dark = pitch_dark.kdeplot(df.x, df.y, ax=ax, cmap=cmr.voltage, shade=True, levels=100)
+kdeplot_dark = pitch_dark.kdeplot(df.x, df.y, ax=ax, cmap=cmr.voltage, fill=True, levels=100)
 
 # light
 pitch_light = VerticalPitch(line_zorder=2)
 fig, ax = pitch_light.draw()
-kdeplot_light = pitch_light.kdeplot(df.x, df.y, ax=ax, cmap=cmr.voltage_r, shade=True, levels=100)
+kdeplot_light = pitch_light.kdeplot(df.x, df.y, ax=ax, cmap=cmr.voltage_r, fill=True, levels=100)
 
 ##############################################################################
 # Create colormaps using LinearSegmentedColormap
 # ----------------------------------------------
 # Sometimes its nice to make your own colormaps, maybe to even match team colors.
 # In these examples we will use a list of two colors and the colormaps will
 # linearly increase between these two colors (note you can do more such as use 3 colors).
@@ -150,15 +150,15 @@
 
 ##############################################################################
 # Cyan colormap kdeplot
 pitch = VerticalPitch(line_color='#cfcfcf', line_zorder=2, pitch_color='#15242e')
 fig, ax = pitch.draw(figsize=(4.4, 6.4))
 # note use the colormap with 100 colors for a smoother finish
 # sphinx_gallery_thumbnail_path = 'gallery/pitch_plots/images/sphx_glr_plot_cmap_007.png'
-kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=pearl_earring_cmap_100, shade=True, levels=100)
+kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=pearl_earring_cmap_100, fill=True, levels=100)
 
 ##############################################################################
 # Flamingo colormap heatmap
 pitch = VerticalPitch(line_color='#000009', line_zorder=2, pitch_color='white')
 fig, ax = pitch.draw(figsize=(4.4, 6.4))
 bs = pitch.bin_statistic(df.x, df.y, bins=(12, 8))
 heatmap = pitch.heatmap(bs, ax=ax, edgecolors='#f4f4f4', cmap=flamingo_cmap)
@@ -168,15 +168,15 @@
 fig, ax = pitch.draw()
 hexmap = pitch.hexbin(df.x, df.y, ax=ax, edgecolors='#f4f4f4', gridsize=(8, 8), cmap=flamingo_cmap)
 
 ##############################################################################
 # Flamingo colormap kdeplot
 pitch = VerticalPitch(line_color='#000009', line_zorder=2, pitch_color='#e3aca7')
 fig, ax = pitch.draw(figsize=(4.4, 6.4))
-kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=flamingo_cmap_100, shade=True, levels=100)
+kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=flamingo_cmap_100, fill=True, levels=100)
 
 ##############################################################################
 # Violet colormap heatmap
 pitch = VerticalPitch(line_color='#cfcfcf', line_zorder=2, pitch_color='#20143f')
 fig, ax = pitch.draw(figsize=(4.4, 6.4))
 bs = pitch.bin_statistic(df.x, df.y, bins=(12, 8))
 heatmap = pitch.heatmap(bs, ax=ax, edgecolors='#20143f', cmap=el_greco_violet_cmap)
@@ -187,15 +187,15 @@
 hexbin = pitch.hexbin(df.x, df.y, ax=ax, edgecolors='#20143f',
                       gridsize=(8, 8), cmap=el_greco_violet_cmap)
 
 ##############################################################################
 # Violet colormap kdeplot
 pitch = VerticalPitch(line_color='#cfcfcf', line_zorder=2, pitch_color='#332a49')
 fig, ax = pitch.draw(figsize=(4.4, 6.4))
-kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=el_greco_violet_cmap_100, shade=True, levels=100)
+kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=el_greco_violet_cmap_100, fill=True, levels=100)
 
 ##############################################################################
 # Yellow colormap heatmap
 pitch = VerticalPitch(line_color='#cfcfcf', line_zorder=2, pitch_color='#471c15')
 fig, ax = pitch.draw(figsize=(4.4, 6.4))
 bs = pitch.bin_statistic(df.x, df.y, bins=(12, 8))
 heatmap = pitch.heatmap(bs, ax=ax, edgecolors='#471c15', cmap=el_greco_yellow_cmap)
@@ -206,10 +206,10 @@
 hexbin = pitch.hexbin(df.x, df.y, ax=ax, edgecolors='#443d07',
                       gridsize=(8, 8), cmap=el_greco_yellow_cmap)
 
 ##############################################################################
 # Yellow colormap kdeplot
 pitch = VerticalPitch(line_color='#cfcfcf', line_zorder=2, pitch_color='#7c2e2a')
 fig, ax = pitch.draw(figsize=(4.4, 6.4))
-kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=el_greco_yellow_cmap_100, shade=True, levels=100)
+kdeplot = pitch.kdeplot(df.x, df.y, ax=ax, cmap=el_greco_yellow_cmap_100, fill=True, levels=100)
 
 plt.show()  # If you are using a Jupyter notebook you do not need this line
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_convex_hull.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_convex_hull.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_cyberpunk.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_cyberpunk.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_delaunay.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_delaunay.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_fbref.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_fbref.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_flow.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_flow.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_grid.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_grid.py`

 * *Files 1% similar despite different names*

```diff
@@ -244,18 +244,18 @@
         # top of the y-axis (y=0) and the top of the padding (y=-10, remember pad_top = 10)
         # note that the StatsBomb y-axis is inverted, so you may need
         # to change this if you use another pitch_type (e.g. 'uefa').
         # We also use the highlight-text package to highlight complete_pass green
         # so put <> around the number of completed passes.
         total_pass = len(complete_pass) + len(incomplete_pass)
         annotation_string = (f'{lineup_player.position_abbreviation} | '
-                             f'{lineup_player.player_nickname} | '
+                             f'{lineup_player.player_name} | '
                              f'<{len(complete_pass)}>/{total_pass} | '
                              f'{round(100 * len(complete_pass)/total_pass, 1)}%')
-        ax_text(0, -5, annotation_string, ha='left', va='center', fontsize=20,
+        ax_text(0, -5, annotation_string, ha='left', va='center', fontsize=13,
                 fontproperties=fm_scada.prop,  # using the fontmanager for the google font
                 highlight_textprops=[{"color": '#56ae6c'}], ax=ax)
 
         # add information for subsitutions on/off and arrows
         if not np.isnan(lineup_team.iloc[idx].off):
             ax.text(116, -10, str(lineup_team.iloc[idx].off.astype(int)), fontsize=20,
                     fontproperties=fm_scada.prop,
@@ -268,15 +268,15 @@
             ax.annotate('', (108, -2), (100, -2), arrowprops=green_arrow)
 
 # plot on the last Pass Map
 # (note ax=ax as we have cycled through to the last axes in the loop)
 pitch.kdeplot(x=pass_receipts.x, y=pass_receipts.y, ax=ax,
               cmap=cmr.lavender,
               levels=100,
-              thresh=0, shade=True)
+              thresh=0, fill=True)
 ax.text(0, -5, f'{team}: Pass Receipt Heatmap', ha='left', va='center',
         fontsize=20, fontproperties=fm_scada.prop)
 
 # remove unused axes (if any)
 for ax in axs['pitch'].flat[11 + num_sub:-1]:
     ax.remove()
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_heatmap.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_heatmap.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_heatmap_positional.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_heatmap_positional.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_hexbin.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_hexbin.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_jointgrid.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_jointgrid.py`

 * *Files 3% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 Inspired by the Seaborn jointgrid and `@n_mondon <https://twitter.com/n_mondon>`_ charts,
 jointgrid gives a handy way to put marginal axis on each side of the pitch.
 """
 
 import numpy as np
 import pandas as pd
 import seaborn as sns
-from matplotlib.cm import get_cmap
+from matplotlib import colormaps
 import matplotlib.pyplot as plt
 
 from mplsoccer import Pitch, VerticalPitch, Sbopen, FontManager
 
 # get data for a Sevilla versus Barcelona match with a high amount of shots
 parser = Sbopen()
 df, related, freeze, tactics = parser.event(9860)
@@ -62,15 +62,15 @@
                            endnote_height=0,  # plot without an endnote axes
                            grid_height=0.8)  # grid takes up 80% of the figure height
 # we plot a usual scatter plot but the scatter size is based on expected goals
 # note that the size is the expected goals * 700
 # so any shots with an expected goals = 1 would take a size of 700 (points**2)
 sc_team1 = pitch.scatter(df_team1.x, df_team1.y, s=df_team1.shot_statsbomb_xg * 700,
                          ec='black', color='#ba495c', ax=axs['pitch'])
-sc_team2 = pitch.scatter(df_team2.x, df_team2.y, s=df_team1.shot_statsbomb_xg * 700,
+sc_team2 = pitch.scatter(df_team2.x, df_team2.y, s=df_team2.shot_statsbomb_xg * 700,
                          ec='black', color='#697cd4', ax=axs['pitch'])
 # (step) histograms on each of the left, top, and right marginal axes
 team1_hist_y = sns.histplot(y=df_team1.y, ax=axs['left'], element='step', color='#ba495c')
 team1_hist_x = sns.histplot(x=df_team1.x, ax=axs['top'], element='step', color='#ba495c')
 team2_hist_x = sns.histplot(x=df_team2.x, ax=axs['top'], element='step', color='#697cd4')
 team2_hist_y = sns.histplot(y=df_team2.y, ax=axs['right'], element='step', color='#697cd4')
 txt1 = axs['pitch'].text(x=15, y=70, s=team1, fontproperties=fm.prop, color='#ba495c',
@@ -86,15 +86,15 @@
 # we don't need as much space taken up by the marginal axes
 fig, axs = pitch.jointgrid(figheight=10, left=None, bottom=0.075, marginal=0.02,
                            axis=False,  # turn off title/ endnote/ marginal axes
                            # plot without title/ endnote axes
                            endnote_height=0, title_height=0)
 sc_team1 = pitch.scatter(df_team1.x, df_team1.y, s=df_team1.shot_statsbomb_xg * 700,
                          ec='black', color='#ba495c', ax=axs['pitch'])
-sc_team2 = pitch.scatter(df_team2.x, df_team2.y, s=df_team1.shot_statsbomb_xg * 700,
+sc_team2 = pitch.scatter(df_team2.x, df_team2.y, s=df_team2.shot_statsbomb_xg * 700,
                          ec='black', color='#697cd4', ax=axs['pitch'])
 # note height=1 means that the whole of the marginal axes are taken up by the rugplots
 team1_rug_y = sns.rugplot(y=df_team1.y, ax=axs['left'], color='#ba495c', height=1)
 team1_rug_y = sns.rugplot(y=df_team2.y, ax=axs['right'], color='#697cd4', height=1)
 team1_rug_x = sns.rugplot(x=df_team1.x, ax=axs['top'], color='#ba495c', height=1)
 team2_rug_x = sns.rugplot(x=df_team2.x, ax=axs['top'], color='#697cd4', height=1)
 txt1 = axs['pitch'].text(x=15, y=70, s=team1, fontproperties=fm.prop, color='#ba495c',
@@ -118,19 +118,20 @@
 df_team2 = df_shots[df_shots.team_name == team2].copy().reset_index(drop=True)
 
 # move the team1 coordinate to the left hand side
 df_team1['x'] = pitch.dim.right - df_team1.x
 
 ##############################################################################
 # Get colors
+# ----------
 # We are using Reds and Blues colormaps below and select a color just over half
 # way (60%) through the colormap for use in the charts.
 
-red = get_cmap('Reds')(np.linspace(0, 1, 100))[60]
-blue = get_cmap('Blues')(np.linspace(0, 1, 100))[60]
+red = colormaps.get_cmap('Reds')(np.linspace(0, 1, 100))[60]
+blue = colormaps.get_cmap('Blues')(np.linspace(0, 1, 100))[60]
 
 ##############################################################################
 # Hexbin shot map with kdeplot marginal axes
 # ------------------------------------------
 
 fig, axs = pitch.jointgrid(figheight=10, left=None, bottom=0.075, grid_height=0.8,
                            axis=False,  # turn off title/ endnote/ marginal axes
@@ -144,18 +145,18 @@
 # normalize the values so the colors depend on the minimum/ value for both teams
 # this ensures that darker colors mean more shots relative to both teams
 vmin = min(hex1.get_array().min(), hex2.get_array().min())
 vmax = max(hex1.get_array().max(), hex2.get_array().max())
 hex1.set_clim(vmin=vmin, vmax=vmax)
 hex2.set_clim(vmin=vmin, vmax=vmax)
 # plot kdeplots on the marginals
-team1_hist_y = sns.kdeplot(y=df_team1.y, ax=axs['left'], color=red, shade=True)
-team1_hist_x = sns.kdeplot(x=df_team1.x, ax=axs['top'], color=red, shade=True)
-team2_hist_x = sns.kdeplot(x=df_team2.x, ax=axs['top'], color=blue, shade=True)
-team2_hist_y = sns.kdeplot(y=df_team2.y, ax=axs['right'], color=blue, shade=True)
+team1_hist_y = sns.kdeplot(y=df_team1.y, ax=axs['left'], color=red, fill=True)
+team1_hist_x = sns.kdeplot(x=df_team1.x, ax=axs['top'], color=red, fill=True)
+team2_hist_x = sns.kdeplot(x=df_team2.x, ax=axs['top'], color=blue, fill=True)
+team2_hist_y = sns.kdeplot(y=df_team2.y, ax=axs['right'], color=blue, fill=True)
 txt1 = axs['pitch'].text(x=15, y=70, s=team1, fontproperties=fm.prop, color=red,
                          ha='center', va='center', fontsize=30)
 txt2 = axs['pitch'].text(x=105, y=70, s=team2, fontproperties=fm.prop, color=blue,
                          ha='center', va='center', fontsize=30)
 
 ##############################################################################
 # Heatmap shot map with histogram/ kdeplot on the marginal axes
@@ -192,21 +193,21 @@
 # --------------------------------------------------
 
 fig, axs = pitch.jointgrid(figheight=10, left=None, bottom=0.075, grid_height=0.8,
                            axis=False,  # turn off title/ endnote/ marginal axes
                            # plot without endnote/ title axes
                            title_height=0, endnote_height=0)
 # increase number of levels for a smoother looking heatmap
-kde1 = pitch.kdeplot(df_team1.x, df_team1.y, ax=axs['pitch'], cmap='Reds', levels=75, shade=True)
-kde2 = pitch.kdeplot(df_team2.x, df_team2.y, ax=axs['pitch'], cmap='Blues', levels=75, shade=True)
+kde1 = pitch.kdeplot(df_team1.x, df_team1.y, ax=axs['pitch'], cmap='Reds', levels=75, fill=True)
+kde2 = pitch.kdeplot(df_team2.x, df_team2.y, ax=axs['pitch'], cmap='Blues', levels=75, fill=True)
 # kdeplot on marginal axes
-team1_hist_y = sns.kdeplot(y=df_team1.y, ax=axs['left'], color=red, shade=True)
-team1_hist_x = sns.kdeplot(x=df_team1.x, ax=axs['top'], color=red, shade=True)
-team2_hist_x = sns.kdeplot(x=df_team2.x, ax=axs['top'], color=blue, shade=True)
-team2_hist_y = sns.kdeplot(y=df_team2.y, ax=axs['right'], color=blue, shade=True)
+team1_hist_y = sns.kdeplot(y=df_team1.y, ax=axs['left'], color=red, fill=True)
+team1_hist_x = sns.kdeplot(x=df_team1.x, ax=axs['top'], color=red, fill=True)
+team2_hist_x = sns.kdeplot(x=df_team2.x, ax=axs['top'], color=blue, fill=True)
+team2_hist_y = sns.kdeplot(y=df_team2.y, ax=axs['right'], color=blue, fill=True)
 txt1 = axs['pitch'].text(x=15, y=70, s=team1, fontproperties=fm.prop, color=red,
                          ha='center', va='center', fontsize=30)
 txt2 = axs['pitch'].text(x=105, y=70, s=team2, fontproperties=fm.prop, color=blue,
                          ha='center', va='center', fontsize=30)
 
 ##############################################################################
 # Vertical shot map with kdeplot marginals
@@ -225,16 +226,16 @@
                                     ax_left=False, ax_right=True)
 # typical shot map where the scatter points vary by the expected goals value
 # using alpha for transparency as there are a lot of shots stacked around the six-yard box
 sc_team2 = vertical_pitch.scatter(df_team2.x, df_team2.y, s=df_team2.shot_statsbomb_xg * 700,
                                   alpha=0.5, ec='black', color='#697cd4', ax=axs['pitch'])
 # kdeplots on the marginals
 # remember to flip the coordinates y=x, x=y for the marginals when using vertical orientation
-team2_hist_x = sns.kdeplot(y=df_team2.x, ax=axs['right'], color='#697cd4', shade=True)
-team2_hist_y = sns.kdeplot(x=df_team2.y, ax=axs['bottom'], color='#697cd4', shade=True)
+team2_hist_x = sns.kdeplot(y=df_team2.x, ax=axs['right'], color='#697cd4', fill=True)
+team2_hist_y = sns.kdeplot(x=df_team2.y, ax=axs['bottom'], color='#697cd4', fill=True)
 txt1 = axs['pitch'].text(x=40, y=80, s=team2, fontproperties=fm_rubik.prop, color=pitch.line_color,
                          ha='center', va='center', fontsize=60)
 
 ##############################################################################
 # Crop the pitch
 # --------------
 # The jointgrid also works with arbritary padding.
@@ -255,16 +256,16 @@
                                     ax_left=False, ax_right=True)
 # typical shot map where the scatter points vary by the expected goals value
 # using alpha for transparency as there are a lot of shots stacked around the six-yard box
 sc_team2 = vertical_pitch.scatter(df_team2.x, df_team2.y, s=df_team2.shot_statsbomb_xg * 700,
                                   alpha=0.5, ec='black', color='#697cd4', ax=axs['pitch'])
 # kdeplots on the marginals
 # remember to flip the coordinates y=x, x=y for the marginals when using vertical orientation
-team2_hist_x = sns.kdeplot(y=df_team2.x, ax=axs['right'], color='#697cd4', shade=True)
-team2_hist_y = sns.kdeplot(x=df_team2.y, ax=axs['bottom'], color='#697cd4', shade=True)
+team2_hist_x = sns.kdeplot(y=df_team2.x, ax=axs['right'], color='#697cd4', fill=True)
+team2_hist_y = sns.kdeplot(x=df_team2.y, ax=axs['bottom'], color='#697cd4', fill=True)
 txt1 = axs['pitch'].text(x=40, y=85, s=team2, fontproperties=fm_rubik.prop, color=pitch.line_color,
                          ha='center', va='center', fontsize=60)
 
 ##############################################################################
 # Add a title and endnote
 # -----------------------
 # The jointgrid also has an option to plot an endnote and a title axes.
@@ -286,16 +287,16 @@
                                     ax_left=False, ax_right=True)
 # typical shot map where the scatter points vary by the expected goals value
 # using alpha for transparency as there are a lot of shots stacked around the six-yard box
 sc_team2 = vertical_pitch.scatter(df_team2.x, df_team2.y, s=df_team2.shot_statsbomb_xg * 700,
                                   alpha=0.5, ec='black', color='#697cd4', ax=axs['pitch'])
 # kdeplots on the marginals
 # remember to flip the coordinates y=x, x=y for the marginals when using vertical orientation
-team2_hist_x = sns.kdeplot(y=df_team2.x, ax=axs['right'], color='#697cd4', shade=True)
-team2_hist_y = sns.kdeplot(x=df_team2.y, ax=axs['bottom'], color='#697cd4', shade=True)
+team2_hist_x = sns.kdeplot(y=df_team2.x, ax=axs['right'], color='#697cd4', fill=True)
+team2_hist_y = sns.kdeplot(x=df_team2.y, ax=axs['bottom'], color='#697cd4', fill=True)
 txt1 = axs['pitch'].text(x=40, y=85, s=team2, fontproperties=fm_rubik.prop, color=pitch.line_color,
                          ha='center', va='center', fontsize=60)
 
 # titles and endnote
 axs['title'].text(0.5, 0.7, "Sevilla's shots versus Barcelona", color=pitch.line_color,
                   fontproperties=fm_rubik.prop, fontsize=18, ha='center', va='center')
 axs['title'].text(0.5, 0.3, "2014/15 to 2019/20", color=pitch.line_color,
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_kde.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_kde.py`

 * *Files 12% similar despite different names*

```diff
@@ -34,19 +34,19 @@
                                                   ['#e3aca7', '#c03a1d'], N=100)
 
 ##############################################################################
 # Plot Messi's first game as a false-9.
 pitch = VerticalPitch(line_color='#000009', line_zorder=2)
 fig, ax = pitch.draw(figsize=(4.4, 6.4))
 kde = pitch.kdeplot(df_false9.x, df_false9.y, ax=ax,
-                    # shade using 100 levels so it looks smooth
-                    shade=True, levels=100,
+                    # fill using 100 levels so it looks smooth
+                    fill=True, levels=100,
                     # shade the lowest area so it looks smooth
                     # so even if there are no events it gets some color
-                    shade_lowest=True,
+                    thresh=0,
                     cut=4,  # extended the cut so it reaches the bottom edge
                     cmap=flamingo_cmap)
 
 ##############################################################################
 # Load a custom font.
 URL = 'https://raw.githubusercontent.com/google/fonts/main/apache/roboto/Roboto%5Bwdth,wght%5D.ttf'
 URL2 = 'https://raw.githubusercontent.com/google/fonts/main/apache/robotoslab/RobotoSlab%5Bwght%5D.ttf'
@@ -69,19 +69,19 @@
 
 fig, axs = pitch.grid(figheight=10, title_height=0.08, endnote_space=0, title_space=0,
                       # Turn off the endnote/title axis. I usually do this after
                       # I am happy with the chart layout and text placement
                       axis=False,
                       grid_height=0.82, endnote_height=0.03)
 kde = pitch.kdeplot(df_false9.x, df_false9.y, ax=axs['pitch'],
-                    # shade using 100 levels so it looks smooth
-                    shade=True, levels=100,
+                    # fill using 100 levels so it looks smooth
+                    fill=True, levels=100,
                     # shade the lowest area so it looks smooth
                     # so even if there are no events it gets some color
-                    shade_lowest=True,
+                    thresh=0,
                     cut=4,  # extended the cut so it reaches the bottom edge
                     cmap=flamingo_cmap)
 axs['endnote'].text(1, 0.5, '@your_twitter_handle', va='center', ha='right', fontsize=15,
                     fontproperties=robotto_regular.prop)
 axs['title'].text(0.5, 0.7, "Lionel Messi's Actions", color='#000009',
                   va='center', ha='center', fontproperties=robotto_regular.prop, fontsize=30)
 axs['title'].text(0.5, 0.25, "First game as a false nine", color='#000009',
@@ -96,19 +96,19 @@
 # Plot Messi's actions in the matches before and after becoming a false-9.
 # We will use mplsoccer's grid function, which is a convenient way to plot a grid
 # of pitches with a title and endnote axes.
 
 fig, axs = pitch.grid(ncols=2, axis=False, endnote_height=0.05)
 
 kde_before = pitch.kdeplot(df_before_false9.x, df_before_false9.y, ax=axs['pitch'][0],
-                           shade=True, levels=100, shade_lowest=True,
+                           fill=True, levels=100, thresh=0,
                            cut=4, cmap='Reds')
 
 kde_after = pitch.kdeplot(df_false9.x, df_false9.y, ax=axs['pitch'][1],
-                          shade=True, levels=100, shade_lowest=True,
+                          fill=True, levels=100, thresh=0,
                           cut=4, cmap='Blues')
 
 ax_sb_logo = add_image(sb_logo, fig,
                        # set the left, bottom and height to align with the endnote
                        left=axs['endnote'].get_position().x0,
                        bottom=axs['endnote'].get_position().y0,
                        height=axs['endnote'].get_position().height)
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_lines.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_lines.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_pass_network.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_pass_network.py`

 * *Files 0% similar despite different names*

```diff
@@ -67,15 +67,15 @@
 # Show the formations used in the match
 events.groupby('team_name').tactics_formation.unique()
 
 ##############################################################################
 # Filter passes by chosen formation, then group all passes and receipts to
 # calculate avg x, avg y, count of events for each slot in the formation
 
-FORMATION = 433
+FORMATION = '433'
 pass_cols = ['id', 'position_abbreviation', 'position_abbreviation_receipt']
 passes_formation = events.loc[(events.team_name == TEAM) & (events.type_name == 'Pass') &
                               (events.tactics_formation == FORMATION) &
                               (events.position_abbreviation_receipt.notnull()), pass_cols].copy()
 location_cols = ['position_abbreviation', 'x', 'y']
 location_formation = events.loc[(events.team_name == TEAM) &
                                 (events.type_name.isin(['Pass', 'Ball Receipt'])) &
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_photo.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_photo.py`

 * *Files 9% similar despite different names*

```diff
@@ -20,34 +20,43 @@
 # ######################
 
 # load the image
 IMAGE_URL = 'https://upload.wikimedia.org/wikipedia/commons/b/b8/Messi_vs_Nigeria_2018.jpg'
 image = Image.open(urlopen(IMAGE_URL))
 
 ##############################################################################
+# Inset image
+# ###########
+#
+# You can use ``ax_image`` to create an inset_axes on a pitch and then plot an image.
+pitch = Pitch(line_zorder=2)
+fig, ax = pitch.draw(figsize=(16, 9), tight_layout=False)
+ax_image = pitch.inset_image(40, 60, image, height=20, ax=ax)
+
+##############################################################################
+# Photo from: https://en.wikipedia.org/wiki/Lionel_Messi#/media/File:Messi_vs_Nigeria_2018.jpg;
+# License: https://creativecommons.org/licenses/by-sa/3.0/;
+# Creator: Кирилл Венедиктов
+
+##############################################################################
 # Plotting an image over a pitch
 # ##############################
 #
-# To plot images you use ``Axes.imshow()`` in matplotlib.
-# We are going to draw a pitch and then overlay ontop an image of Messi on a new axis.
+# You can also use ``add_image``, which uses figure coordinates instead of the pitch coordinates
+# for placing the axes.
 
 # draw the pitch
 pitch = Pitch(line_zorder=2)
 fig, ax = pitch.draw(figsize=(16, 9), tight_layout=False)
 
 # add an image
 ax_image = add_image(image, fig, left=0.55, bottom=0.2, width=0.2,
                      alpha=0.9, interpolation='hanning')
 
 ##############################################################################
-# Photo from: https://en.wikipedia.org/wiki/Lionel_Messi#/media/File:Messi_vs_Nigeria_2018.jpg;
-# License: https://creativecommons.org/licenses/by-sa/3.0/;
-# Creator: Кирилл Венедиктов
-
-##############################################################################
 # More control over the images and axis
 # #####################################
 #
 # For more control over where the images are placed,
 # you can create a blank figure with ``plt.figure()``
 # and then use ``Figure.add_axes()`` to add seperate axes for each of the plot elements.
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_sb360_frame.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_sb360_frame.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_scatter.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_scatter.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 Scatter
 =======
 
 This example shows how to plot a scatter chart.
 """
 
 import numpy as np
-from matplotlib import cm
+from matplotlib import colormaps
 import matplotlib.pyplot as plt
 from matplotlib.colors import ListedColormap
 
 from mplsoccer import (VerticalPitch, Pitch, create_transparent_cmap,
                        FontManager, arrowhead_marker, Sbopen)
 
 # get data for a Sevilla versus Barcelona match with a high amount of shots
@@ -88,15 +88,15 @@
 # Shot map Barcelona using cmap for edges
 # ---------------------------------------
 # It's possible to use cmaps for the edgecolors for emphasis by mapping the expected goals
 # values to colors and using these as edgecolors.
 # You could use the same technique to assign fewer colors to the scatter.
 
 # get the cmap as 10 colors (n_colors can be anything)
-cmap = cm.get_cmap('Greys')  # reversed plasma
+cmap = colormaps.get_cmap('Greys')  # reversed plasma
 N_COLORS = 10
 cmap = cmap(np.linspace(0.5, 1, N_COLORS))  # from half-way (0.5) to end (1) of grey colormap
 cmap = ListedColormap(cmap, name='Greys')
 # convert the statsbomb xg to colors
 edgecolors = cmap(df_shots_barca.shot_statsbomb_xg)
 
 fig, ax = pitch.draw(figsize=(12, 10))
@@ -142,15 +142,15 @@
 
 ##############################################################################
 # Shot map Barcelona using hatch
 # ------------------------------
 # Another method popularized by `@petermckeever <https://twitter.com/petermckeever>`_.
 # is to use hatch patterns to show where something was not-successful versus successful.
 # There are lots of different hatch patterns.
-# See: matplotlib.org/api/_as_gen/matplotlib.patches.Patch.html#matplotlib.patches.Patch.set_hatch
+# See set_hatch: https://matplotlib.org/stable/api/_as_gen/matplotlib.patches.Patch.html
 # This is typically combined with the highlight-text package
 # by `@danzn1 <https://twitter.com/danzn1>`_.
 
 # filter goals / non-shot goals
 df_goals_barca = df_shots_barca[df_shots_barca.outcome_name == 'Goal'].copy()
 df_non_goal_shots_barca = df_shots_barca[df_shots_barca.outcome_name != 'Goal'].copy()
 
@@ -325,15 +325,15 @@
 # Warning: The rotation angle is in degrees and assumes the original marker is pointing upwards ↑.
 # If it's not you will have to modify the rotation degrees.
 # Rotates the marker in degrees, clockwise. 0 degrees is facing the
 # direction of play (left to right).
 # In a horizontal pitch, 0 degrees is this way →, in a vertical pitch, 0 degrees is this way ↑
 #
 # We are going to plot pass data as an arrowhead marker with the
-# arrow facing in the direction of the pass
+# arrow facing in the direction of the pass.
 # The marker size is going to relate to the pass distance,
 # so larger markers mean the pass was longer.
 pitch = Pitch()
 fig, ax = pitch.draw(figsize=(14, 12))
 angle, distance = pitch.calculate_angle_and_distance(df_pass_barca.x, df_pass_barca.y,
                                                      df_pass_barca.end_x, df_pass_barca.end_y,
                                                      standardized=False, degrees=True)
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_shot_freeze_frame.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_shot_freeze_frame.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_standardize.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_standardize.py`

 * *Files 1% similar despite different names*

```diff
@@ -129,15 +129,15 @@
     ) 
 
 ##############################################################################
 # Standardize the Wyscout data to StatsBomb coordinates
 # -----------------------------------------------------
 # You can use any of the supported pitches in the pitch_from/ pitch_to here.
 # They are currently: ``statsbomb``, ``tracab``, ``opta``, ``wyscout``, ``uefa``,
-# ``metricasports``, ``custom``, ``skillcorner``, and ``secondspectrum``.
+# ``metricasports``, ``custom``, ``skillcorner``, ``impect``, and ``secondspectrum``.
 #
 # If the pitch size varies (``tracab``, ``metricasports``, ``custom``,
 # ``skillcorner``, ``secondspectrum``)
 # then you also need to supply the relevant
 # length_from/ length_to or width_from/ width_to in meters.
 
 # setup the Standardizer
```

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_textured_background.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_textured_background.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_twitter_powerpoint.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_twitter_powerpoint.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_plots/plot_voronoi.py` & `mplsoccer-1.2.0/examples/pitch_plots/plot_voronoi.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_setup/plot_compare_pitches.py` & `mplsoccer-1.2.0/examples/pitch_setup/plot_compare_pitches.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_setup/plot_explain_standardizer.py` & `mplsoccer-1.2.0/examples/pitch_setup/plot_explain_standardizer.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pitch_setup/plot_pitches.py` & `mplsoccer-1.2.0/examples/pitch_setup/plot_pitches.py`

 * *Files 2% similar despite different names*

```diff
@@ -28,17 +28,17 @@
 pitch = Pitch()
 pie = axs[0].pie(x=[5, 15])
 pitch.draw(ax=axs[1])
 
 ##############################################################################
 # Supported data providers
 # ------------------------
-# mplsoccer supports 9 pitch types by specifying the ``pitch_type`` argument:
+# mplsoccer supports 10 pitch types by specifying the ``pitch_type`` argument:
 # 'statsbomb', 'opta', 'tracab', 'wyscout', 'uefa', 'metricasports', 'custom',
-# 'skillcorner' and 'secondspectrum'.
+# 'skillcorner', 'secondspectrum' and 'impect'.
 # If you are using tracking data or the custom pitch ('metricasports', 'tracab',
 # 'skillcorner', 'secondspectrum' or 'custom'), you also need to specify the
 # ``pitch_length`` and ``pitch_width``, which are typically 105 and 68 respectively.
 
 pitch = Pitch(pitch_type='opta')  # example plotting an Opta/ Stats Perform pitch
 fig, ax = pitch.draw()
 
@@ -156,15 +156,16 @@
 
 pitch = VerticalPitch(corner_arcs=True, half=True)
 fig, ax = pitch.draw(figsize=(10, 7.727))
 
 ##############################################################################
 # Juego de Posición
 # -----------------
-# You can add the Juego de Posición pitch lines and shade the middle third
+# You can add the Juego de Posición pitch lines and shade the middle third.
+# You can also adjust the transparency via ``shade_alpha`` and ``positional_alpha``.
 
 pitch = Pitch(positional=True, shade_middle=True, positional_color='#eadddd', shade_color='#f2f2f2')
 fig, ax = pitch.draw()
 
 ##############################################################################
 # mplsoccer can also plot grass pitches by setting ``pitch_color='grass'``.
```

### Comparing `mplsoccer-1.1.9/examples/pitch_setup/plot_quick_start.py` & `mplsoccer-1.2.0/examples/pitch_setup/plot_quick_start.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_basic.py` & `mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_basic.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_colorful.py` & `mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_colorful.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_comparison.py` & `mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_comparison.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_comparison_vary_scales.py` & `mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_comparison_vary_scales.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_dark_theme.py` & `mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_dark_theme.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_different_units.py` & `mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_different_units.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/pizza_plots/plot_pizza_scales_vary.py` & `mplsoccer-1.2.0/examples/pizza_plots/plot_pizza_scales_vary.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/radar/plot_radar.py` & `mplsoccer-1.2.0/examples/radar/plot_radar.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/radar/plot_turbine.py` & `mplsoccer-1.2.0/examples/radar/plot_turbine.py`

 * *Files 0% similar despite different names*

```diff
@@ -18,16 +18,16 @@
 import numpy as np
 import scipy.stats as stats
 import matplotlib.pyplot as plt
 
 ##############################################################################
 # Creating some random data
 # -------------------------
-# Here we create some random data from a truncated normal distribution
-# In real life the values would be an array or dataframe of
+# Here we create some random data from a truncated normal distribution.
+# In real life, the values would be an array or dataframe of
 # shape number of players * number of skills
 lower, upper, mu, sigma = 0, 1, 0.35, 0.25
 X = stats.truncnorm((lower - mu) / sigma, (upper - mu) / sigma, loc=mu, scale=sigma)
 # for 1000 people and 11 skills
 values = X.rvs((1000, 11))
 # the names of the skills
 params = ['Expected goals', 'Total shots',
```

### Comparing `mplsoccer-1.1.9/examples/statsbomb/plot_statsbomb_data.py` & `mplsoccer-1.2.0/examples/statsbomb/plot_statsbomb_data.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,17 +2,16 @@
 =========
 StatsBomb
 =========
 
 mplsoccer contains functions to return StatsBomb data in a flat, tidy dataframe.
 However, if you want to flatten the json into a dictionary you can also set ``dataframe=False``.
 
-Please be responsible with Statsbomb data.
-`Register your details <https://www.statsbomb.com/resource-centre>`_ and
-read the user agreement carefully (on the same page).
+You can read more about the Statsbomb open-data on their
+`resource centre <https://www.statsbomb.com/resource-centre>`_ page.
 
 It can be used with the StatBomb `open-data <https://github.com/statsbomb/open-data>`_
 or the StatsBomb API if you are lucky enough to have access:
 
 StatsBomb API:
 
 .. code-block:: python
@@ -58,15 +57,15 @@
 
 df_competition = parser.competition()
 df_competition.info()
 
 ##############################################################################
 #  Match data
 # -----------
-# Get the match data as a dataframe
+# Get the match data as a dataframe.
 # Note there is a mismatch between the length of this file
 # and the number of event files because some event files don't have match data in the open-data.
 df_match = parser.match(competition_id=11, season_id=1)
 df_match.info()
 
 ##############################################################################
 # Lineup data
```

### Comparing `mplsoccer-1.1.9/examples/tutorials/plot_wedges.py` & `mplsoccer-1.2.0/examples/tutorials/plot_wedges.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/tutorials/plot_xt.py` & `mplsoccer-1.2.0/examples/tutorials/plot_xt.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/examples/tutorials/plot_xt_improvements.py` & `mplsoccer-1.2.0/examples/tutorials/plot_xt_improvements.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 """
 ===============================
-improvements to expected threat
+Improvements to expected threat
 ===============================
 
 This example tries to make some improvements to our :ref:`sphx_glr_gallery_tutorials_plot_xt.py`
 model. Such as filtering out set pieces, changing the grid layout, and changing the simple
 goal probabilities with the average of a better expected goals model. Can you think of
 any more improvements?
 """
```

### Comparing `mplsoccer-1.1.9/mplsoccer/_pitch_plot.py` & `mplsoccer-1.2.0/mplsoccer/_pitch_plot.py`

 * *Files 1% similar despite different names*

```diff
@@ -111,19 +111,18 @@
             marker = rcParams['scatter.marker']
 
         if marker == 'football' and rotation_degrees is not None:
             raise NotImplementedError("rotated football markers are not implemented.")
 
         if marker == 'football':
             return scatter_football(x, y, ax=ax, **kwargs)
-        elif rotation_degrees is not None:
+        if rotation_degrees is not None:
             return scatter_rotation(x, y, rotation_degrees, marker=marker,
                                     vertical=self.vertical, ax=ax, **kwargs)
-        else:
-            return ax.scatter(x, y, marker=marker, **kwargs)
+        return ax.scatter(x, y, marker=marker, **kwargs)
 
     def _reflect_2d(self, x, y, standardized=False):
         """ Reflect data in the pitch lines."""
         x = np.ravel(x)
         y = np.ravel(y)
         if standardized:
             x_limits, y_limits = [0, 105], [0, 68]
@@ -154,15 +153,15 @@
         --------
         >>> from mplsoccer import Pitch
         >>> import numpy as np
         >>> pitch = Pitch(line_zorder=2)
         >>> fig, ax = pitch.draw()
         >>> x = np.random.uniform(low=0, high=120, size=100)
         >>> y = np.random.uniform(low=0, high=80, size=100)
-        >>> pitch.kdeplot(x, y, cmap='Reds', shade=True, levels=100, ax=ax)
+        >>> pitch.kdeplot(x, y, cmap='Reds', fill=True, levels=100, ax=ax)
         """
         validate_ax(ax)
 
         x = np.ravel(x)
         y = np.ravel(y)
         if x.size != y.size:
             raise ValueError("x and y must be the same size")
@@ -333,23 +332,54 @@
         annotation : matplotlib.text.Annotation
 
         Examples
         --------
         >>> from mplsoccer import Pitch
         >>> pitch = Pitch()
         >>> fig, ax = pitch.draw()
-        >>> pitch.annotate(text='center', xytext=(50, 50), xy=(60, 40), ha='center', va='center', \
-                           ax=ax, arrowprops=dict(facecolor='black'))
+        >>> pitch.annotate(text='center', xytext=(50, 50), xy=(60, 40), ha='center', va='center',
+        ...                ax=ax, arrowprops=dict(facecolor='black'))
         """
         validate_ax(ax)
         xy = self._reverse_annotate_if_vertical(xy)
         if xytext is not None:
             xytext = self._reverse_annotate_if_vertical(xytext)
         return ax.annotate(text, xy, xytext, **kwargs)
 
+    def text(self, x, y, s, ax=None, **kwargs):
+        """ Utility wrapper around ax.text
+        which automatically flips the x/y coordinates if the pitch is vertical.
+
+        See: https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.text.html
+
+        Parameters
+        ----------
+        x, y : float
+            The position to place the text
+        s : str
+            The text
+        ax : matplotlib.axes.Axes, default None
+            The axis to plot on.
+        **kwargs : All other keyword arguments are passed on to matplotlib.axes.Axes.text.
+
+        Returns
+        -------
+        annotation : matplotlib.text.Text
+
+        Examples
+        --------
+        >>> from mplsoccer import Pitch
+        >>> pitch = Pitch()
+        >>> fig, ax = pitch.draw()
+        >>> pitch.text(60, 40, 'Center of the pitch', va='center', ha='center', ax=ax)
+        """
+        validate_ax(ax)
+        x, y = self._reverse_if_vertical(x, y)
+        return ax.text(x, y, s, **kwargs)
+
     @docstring.copy(bin_statistic)
     def bin_statistic(self, x, y, values=None, statistic='count', bins=(5, 4),
                       normalize=False, standardized=False):
         return bin_statistic(x, y, values=values, dim=self.dim, statistic=statistic,
                              bins=bins, normalize=normalize, standardized=standardized)
 
     @docstring.copy(heatmap)
@@ -363,25 +393,28 @@
                                         dim=self.dim, positional=positional,
                                         statistic=statistic, normalize=normalize)
 
     @docstring.copy(heatmap_positional)
     def heatmap_positional(self, stats, ax=None, **kwargs):
         return heatmap_positional(stats, ax=ax, vertical=self.vertical, **kwargs)
 
-    def label_heatmap(self, stats, str_format=None, exclude_zeros=False, ax=None, **kwargs):
+    def label_heatmap(self, stats, str_format=None, exclude_zeros=False,
+                      xoffset=0, yoffset=0, ax=None, **kwargs):
         """ Labels the heatmap(s) and automatically flips the coordinates if the pitch is vertical.
 
         Parameters
         ----------
         stats : A dictionary or list of dictionaries.
             This should be calculated via bin_statistic_positional() or bin_statistic().
         str_format : str
             A format string passed to str_format.format() to format the labels.
         exclude_zeros : bool
             Whether to exclude zeros when labelling the heatmap.
+        xoffset, yoffset : float, default 0
+            The amount in data coordinates to offset the labels from the center of the grid cell.
         ax : matplotlib.axes.Axes, default None
             The axis to plot on.
 
         **kwargs : All other keyword arguments are passed on to matplotlib.axes.Axes.annotate.
 
         Returns
         -------
@@ -396,16 +429,16 @@
         >>> fig, ax = pitch.draw()
         >>> x = np.random.uniform(low=0, high=120, size=100)
         >>> y = np.random.uniform(low=0, high=80, size=100)
         >>> stats = pitch.bin_statistic(x, y)
         >>> pitch.heatmap(stats, edgecolors='black', cmap='hot', ax=ax)
         >>> stats['statistic'] = stats['statistic'].astype(int)
         >>> path_eff = [path_effects.Stroke(linewidth=0.5, foreground='#22312b')]
-        >>> text = pitch.label_heatmap(stats, color='white', ax=ax, fontsize=20, ha='center', \
-                                       va='center', path_effects=path_eff)
+        >>> text = pitch.label_heatmap(stats, color='white', ax=ax, fontsize=20, ha='center',
+        ...                            va='center', path_effects=path_eff)
         """
         validate_ax(ax)
 
         if not isinstance(stats, list):
             stats = [stats]
 
         annotation_list = []
@@ -417,16 +450,16 @@
             mask_y_outside2 = bin_stat['cy'] > self.dim.pitch_extent[3]
             mask_clip = mask_x_outside1 | mask_x_outside2 | mask_y_outside1 | mask_y_outside2
             if exclude_zeros:
                 mask_clip = mask_clip | (np.isclose(bin_stat['statistic'], 0.))
             mask_clip = np.ravel(mask_clip)
 
             text = np.ravel(bin_stat['statistic'])[~mask_clip]
-            cx = np.ravel(bin_stat['cx'])[~mask_clip]
-            cy = np.ravel(bin_stat['cy'])[~mask_clip]
+            cx = np.ravel(bin_stat['cx'])[~mask_clip] + xoffset
+            cy = np.ravel(bin_stat['cy'])[~mask_clip] + yoffset
             for idx, text_str in enumerate(text):
                 if str_format is not None:
                     text_str = str_format.format(text_str)
                 annotation = self.annotate(text_str, (cx[idx], cy[idx]), ax=ax, **kwargs)
                 annotation_list.append(annotation)
 
         return annotation_list
@@ -687,17 +720,17 @@
         >>> team1, team2 = df.team_name.unique()
         >>> mask_team1 = (df.type_name == 'Pass') & (df.team_name == team1)
         >>> df = df[mask_team1].copy()
         >>> pitch = Pitch(line_zorder=2)
         >>> fig, ax = pitch.draw()
         >>> bs_heatmap = pitch.bin_statistic(df.x, df.y, statistic='count', bins=(6, 4))
         >>> hm = pitch.heatmap(bs_heatmap, ax=ax, cmap='Blues')
-        >>> fm = pitch.flow(df.x, df.y, df.end_x, df.end_y, color='black', arrow_type='same', \
-                            arrow_length=6, bins=(6, 4), headwidth=2, headlength=2, \
-                            headaxislength=2, ax=ax)
+        >>> fm = pitch.flow(df.x, df.y, df.end_x, df.end_y, color='black', arrow_type='same',
+        ...                 arrow_length=6, bins=(6, 4), headwidth=2, headlength=2,
+        ...                 headaxislength=2, ax=ax)
         """
         validate_ax(ax)
         if self.dim.aspect != 1:
             standardized = True
             xstart, ystart = self.standardizer.transform(xstart, ystart)
             xend, yend = self.standardizer.transform(xend, yend)
         else:
```

### Comparing `mplsoccer-1.1.9/mplsoccer/bumpy_chart.py` & `mplsoccer-1.2.0/mplsoccer/bumpy_chart.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/mplsoccer/cm.py` & `mplsoccer-1.2.0/mplsoccer/cm.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 """ Colormap functions."""
 
 import numpy as np
-from matplotlib.cm import get_cmap
+from matplotlib import colormaps
 from matplotlib.colors import LinearSegmentedColormap, ListedColormap, to_rgba
 
 __all__ = ['create_transparent_cmap', 'grass_cmap']
 
 
 def grass_cmap():
     """ Create a grass colormap.
@@ -50,15 +50,15 @@
 
     # cmap as an rgba array (n_segments long)
     if color is not None:
         cmap = to_rgba(color)
         cmap = np.tile(np.array(cmap), (n_segments, 1))
     else:
         if isinstance(cmap, str):
-            cmap = get_cmap(cmap)
+            cmap = colormaps.get_cmap(cmap)
         if not isinstance(cmap, (ListedColormap, LinearSegmentedColormap)):
             raise ValueError("cmap: not a recognised cmap type.")
         cmap = cmap(np.linspace(0, 1, n_segments))
 
     # amend the alpha channel
     cmap[:, 3] = np.linspace(alpha_start, alpha_end, n_segments)
```

### Comparing `mplsoccer-1.1.9/mplsoccer/grid.py` & `mplsoccer-1.2.0/mplsoccer/grid.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/mplsoccer/heatmap.py` & `mplsoccer-1.2.0/mplsoccer/heatmap.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/mplsoccer/linecollection.py` & `mplsoccer-1.2.0/mplsoccer/linecollection.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 """ A module with functions for using LineCollection to create lines.´´."""
 
 import warnings
 
 import numpy as np
+from matplotlib import colormaps
 from matplotlib import rcParams
-from matplotlib.cm import get_cmap
 from matplotlib.collections import LineCollection
 from matplotlib.colors import to_rgba_array
 from matplotlib.legend import Legend
 from matplotlib.legend_handler import HandlerLineCollection
 
 from mplsoccer.cm import create_transparent_cmap
 from mplsoccer.utils import validate_ax
@@ -136,15 +136,15 @@
         handler_first_lw = False
     else:
         handler_first_lw = True
     multi_segment = transparent is not False or comet is not False or cmap is not None
     if transparent:
         cmap = create_transparent_cmap(color, cmap, n_segments, alpha_start, alpha_end)
     if isinstance(cmap, str):
-        cmap = get_cmap(cmap)
+        cmap = colormaps.get_cmap(cmap)
     if cmap is not None:
         handler_cmap = True
         line_collection = _lines_cmap(xstart, ystart, xend, yend, lw=lw, cmap=cmap, ax=ax,
                                       n_segments=n_segments, multi_segment=multi_segment,
                                       reverse_cmap=reverse_cmap, **kwargs)
 
     else:
```

### Comparing `mplsoccer-1.1.9/mplsoccer/pitch.py` & `mplsoccer-1.2.0/mplsoccer/pitch.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/mplsoccer/py_pizza.py` & `mplsoccer-1.2.0/mplsoccer/py_pizza.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/mplsoccer/quiver.py` & `mplsoccer-1.2.0/mplsoccer/quiver.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/mplsoccer/radar_chart.py` & `mplsoccer-1.2.0/mplsoccer/radar_chart.py`

 * *Files 5% similar despite different names*

```diff
@@ -161,22 +161,22 @@
         -------
         If ax=None returns a matplotlib Figure and Axes.
         Else the settings are applied on an existing axis and returns None.
 
         Examples
         --------
         >>> from mplsoccer import Radar
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = radar.setup_axis()
 
         >>> from mplsoccer import Radar
         >>> import matplotlib.pyplot as plt
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = plt.subplots(figsize=(12, 12))
         >>> radar.setup_axis(ax=ax)
         """
         if ax is None:
             fig, ax = plt.subplots(figsize=figsize, **kwargs)
             self._setup_axis(ax=ax, facecolor=facecolor)
             return fig, ax
@@ -198,16 +198,16 @@
         Returns
         -------
         PatchCollection : matplotlib.collections.PatchCollection
 
         Examples
         --------
         >>> from mplsoccer import Radar
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = radar.setup_axis()
         >>> rings_inner = radar.draw_circles(ax=ax, facecolor='#ffb2b2', edgecolor='#fc5f5f')
         """
         validate_ax(ax)
         radius = np.tile(self.ring_width, self.num_rings + 1)
         radius = np.insert(radius, 0, self.center_circle_radius)
         radius = radius.cumsum()
@@ -260,21 +260,22 @@
             The radar polygon.
         vertices : a 2d numpy array (number of vertices, 2)
             The vertices of the radar polygon. Where the second dimension is the x, y coordinates.
 
         Examples
         --------
         >>> from mplsoccer import Radar
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = radar.setup_axis()
         >>> rings_inner = radar.draw_circles(ax=ax, facecolor='#ffb2b2', edgecolor='#fc5f5f')
         >>> values = [5, 3, 10]
-        >>> radar_poly, vertices = radar.draw_radar_solid(values, ax=ax, \
-kwargs_radar={'facecolor': '#00f2c1', 'alpha': 0.6})
+        >>> radar_poly, vertices = radar.draw_radar_solid(values, ax=ax,
+        ...                                               kwargs={'facecolor': '#00f2c1',
+        ...                                                       'alpha': 0.6})
         """
         validate_ax(ax)
         if kwargs is None:
             kwargs = {}
         # to arrays
         values = np.asarray(values)
         # validate array size
@@ -303,22 +304,24 @@
             The outer rings clipped to the radar polygon.
         vertices : a 2d numpy array (number of vertices, 2)
             The vertices of the radar polygon. Where the second dimension is the x, y coordinates.
 
         Examples
         --------
         >>> from mplsoccer import Radar
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = radar.setup_axis()
         >>> rings_inner = radar.draw_circles(ax=ax, facecolor='#ffb2b2', edgecolor='#fc5f5f')
         >>> values = [5, 3, 10]
-        >>> radar_poly, rings, vertices = radar.draw_radar(values, ax=ax, \
-kwargs_radar={'facecolor': '#00f2c1', 'alpha': 0.6}, \
-kwargs_rings={'facecolor': '#d80499', 'alpha': 0.6})
+        >>> radar_poly, rings, vertices = radar.draw_radar(values, ax=ax,
+        ...                                                kwargs_radar={'facecolor': '#00f2c1',
+        ...                                                              'alpha': 0.6},
+        ...                                                kwargs_rings={'facecolor': '#d80499',
+        ...                                                              'alpha': 0.6})
         """
         validate_ax(ax)
         if kwargs_radar is None:
             kwargs_radar = {}
         if kwargs_rings is None:
             kwargs_rings = {}
         # to arrays
@@ -358,23 +361,25 @@
             The vertices of the first radar. Where the second dimension is the x, y coordinates.
         vertices2 : a 2d numpy array (number of vertices, 2)
             The vertices of the second radar. Where the second dimension is the x, y coordinates.
 
         Examples
         --------
         >>> from mplsoccer import Radar
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = radar.setup_axis()
         >>> rings_inner = radar.draw_circles(ax=ax, facecolor='#ffb2b2', edgecolor='#fc5f5f')
         >>> values = [5, 3, 10]
         >>> compare_values = [10, 4, 3]
-        >>> radar_output = radar.draw_radar_compare(values, compare_values, ax=ax, \
-kwargs_radar={'facecolor': '#00f2c1', 'alpha': 0.6}, \
-kwargs_compare={'facecolor': '#d80499', 'alpha': 0.6})
+        >>> radar_output = radar.draw_radar_compare(values, compare_values, ax=ax,
+        ...                                         kwargs_radar={'facecolor': '#00f2c1',
+        ...                                                       'alpha': 0.6},
+        ...                                         kwargs_compare={'facecolor': '#d80499',
+        ...                                                         'alpha': 0.6})
         """
         validate_ax(ax)
         if kwargs_radar is None:
             kwargs_radar = {}
         if kwargs_compare is None:
             kwargs_compare = {}
         # to arrays
@@ -413,24 +418,24 @@
         Returns
         -------
         label_list : list of matplotlib.text.Text
 
         Examples
         --------
         >>> from mplsoccer import Radar
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-                          max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = radar.setup_axis()
         >>> rings_inner = radar.draw_circles(ax=ax, facecolor='#ffb2b2', edgecolor='#fc5f5f')
         >>> values = [5, 3, 10]
-        >>> radar_poly, rings, vertices = radar.draw_radar(values, ax=ax, \
-                                                           kwargs_radar={'facecolor': '#00f2c1', \
-                                                                         'alpha': 0.6}, \
-                                                           kwargs_rings={'facecolor': '#d80499', \
-                                                                         'alpha': 0.6})
+        >>> radar_poly, rings, vertices = radar.draw_radar(values, ax=ax,
+        ...                                                kwargs_radar={'facecolor': '#00f2c1',
+        ...                                                              'alpha': 0.6},
+        ...                                                kwargs_rings={'facecolor': '#d80499',
+        ...                                                              'alpha': 0.6})
         >>> range_labels = radar.draw_range_labels(ax=ax)
         """
         validate_ax(ax)
         # create the label values - linearly interpolate between the low and high for each circle
         label_values = np.linspace(self.min_range.reshape(-1, 1), self.max_range.reshape(-1, 1),
                                    num=self.num_rings + 1, axis=1).ravel()
         # remove the first entry so that we do not label the inner circle
@@ -446,15 +451,15 @@
         round_format[mask_int] = '%.0f'
         # repeat the rotation degrees for each circle so it matches the length of the label_values
         label_rotations = np.repeat(self.rotation_degrees, self.num_rings)
         # calculate how far out from the center (radius) to place each label, convert to coordinates
         label_radius = np.linspace(self.ring_width,
                                    self.ring_width * self.num_rings,
                                    self.num_rings)
-        label_radius = (self.center_circle_radius + offset + label_radius)
+        label_radius = self.center_circle_radius + offset + label_radius
         label_xs = np.tile(label_radius, self.num_labels) * np.repeat(self.rotation_sin,
                                                                       label_radius.size)
         label_ys = np.tile(label_radius, self.num_labels) * np.repeat(self.rotation_cos,
                                                                       label_radius.size)
         # write the labels on the axis
         label_list = []
         for idx, label in enumerate(label_values):
@@ -480,24 +485,24 @@
         Returns
         -------
         label_list : list of matplotlib.text.Text
 
         Examples
         --------
         >>> from mplsoccer import Radar
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-                          max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = radar.setup_axis()
         >>> rings_inner = radar.draw_circles(ax=ax, facecolor='#ffb2b2', edgecolor='#fc5f5f')
         >>> values = [5, 3, 10]
-        >>> radar_poly, rings, vertices = radar.draw_radar(values, ax=ax, \
-                                                           kwargs_radar={'facecolor': '#00f2c1', \
-                                                                         'alpha': 0.6}, \
-                                                           kwargs_rings={'facecolor': '#d80499', \
-                                                                         'alpha': 0.6})
+        >>> radar_poly, rings, vertices = radar.draw_radar(values, ax=ax,
+        ...                                                kwargs_radar={'facecolor': '#00f2c1',
+        ...                                                              'alpha': 0.6},
+        ...                                                kwargs_rings={'facecolor': '#d80499',
+        ...                                                              'alpha': 0.6})
         >>> range_labels = radar.draw_range_labels(ax=ax)
         >>> param_labels = radar.draw_param_labels(ax=ax)
         """
         validate_ax(ax)
         # calculate how far out from the center (radius) to place each label, convert to coordinates
         # default places one-and-a-half units (offset) away from the edge of the last circle
 
@@ -526,24 +531,24 @@
         Returns
         -------
         A list of Line2D objects representing the plotted data.
 
         Examples
         --------
         >>> from mplsoccer import Radar
-        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0], \
-                          max_range=[10, 10, 10])
+        >>> radar = Radar(params=['Agility', 'Speed', 'Strength'], min_range=[0, 0, 0],
+        ...               max_range=[10, 10, 10])
         >>> fig, ax = radar.setup_axis()
         >>> rings_inner = radar.draw_circles(ax=ax, facecolor='#ffb2b2', edgecolor='#fc5f5f')
         >>> values = [5, 3, 10]
-        >>> radar_poly, rings, vertices = radar.draw_radar(values, ax=ax, \
-                                                           kwargs_radar={'facecolor': '#00f2c1', \
-                                                                         'alpha': 0.6}, \
-                                                           kwargs_rings={'facecolor': '#d80499', \
-                                                                         'alpha': 0.6})
+        >>> radar_poly, rings, vertices = radar.draw_radar(values, ax=ax,
+        ...                                                kwargs_radar={'facecolor': '#00f2c1',
+        ...                                                              'alpha': 0.6},
+        ...                                                kwargs_rings={'facecolor': '#d80499',
+        ...                                                              'alpha': 0.6})
         >>> range_labels = radar.draw_range_labels(ax=ax)
         >>> param_labels = radar.draw_param_labels(ax=ax)
         >>> spokes = radar.spoke(ax=ax)
         """
         spoke_x = self.outer_ring * self.rotation_sin
         spoke_x = np.repeat(spoke_x, 3)
         spoke_x[0::3] = 0
@@ -660,35 +665,35 @@
         >>> from mplsoccer import Radar
         >>> import numpy as np
         >>> import scipy.stats as stats
         >>> np.random.seed(42)
         >>> lower, upper, mu, sigma = 0, 1, 0.35, 0.25
         >>> X = stats.truncnorm((lower - mu) / sigma, (upper - mu) / sigma, loc=mu, scale=sigma)
         >>> values = X.rvs((1000, 11))
-        >>> params = ['Expected goals', 'Total shots', \
-                      'Touches in attacking penalty area', 'Pass completion %', \
-                      'Crosses into the 18-yard box (excluding set pieces)', \
-                      'Expected goals assisted', 'Fouls drawn', 'Successful dribbles', \
-                      'Successful pressures', 'Non-penalty expected goals per shot', \
-                      'Miscontrols/ Dispossessed']
+        >>> params = ['Expected goals', 'Total shots',
+        ...           'Touches in attacking penalty area', 'Pass completion %',
+        ...           'Crosses into the 18-yard box (excluding set pieces)',
+        ...           'Expected goals assisted', 'Fouls drawn', 'Successful dribbles',
+        ...           'Successful pressures', 'Non-penalty expected goals per shot',
+        ...           'Miscontrols/ Dispossessed']
         >>> df = pd.DataFrame(values)
         >>> df.columns = params
         >>> df['player_name'] = np.arange(1000)
         >>> low = df[params].quantile(0.05).values
         >>> high = df[params].quantile(0.95).values
         >>> radar = Radar(params, low, high, num_rings=4)
         >>> player_values = df.loc[df.player_name == 23, params].values[0]
         >>> fig, ax = radar.setup_axis()
-        >>> turbine_output = radar.turbine(player_values, df[params].values, ax=ax, \
-                                           kwargs_inner={'edgecolor': 'black'},
-                                           kwargs_inner_gradient={'cmap': 'Blues'},
-                                           kwargs_outer={'facecolor': '#b2b2b2',
-                                           'edgecolor': 'black'})
-        >>> rings_inner = radar.draw_circles(ax=ax, facecolor='None', \
-                                             edgecolor='black', linestyle='--')
+        >>> turbine_output = radar.turbine(player_values, df[params].values, ax=ax,
+        ...                                kwargs_inner={'edgecolor': 'black'},
+        ...                                kwargs_inner_gradient={'cmap': 'Blues'},
+        ...                                kwargs_outer={'facecolor': '#b2b2b2',
+        ...                                'edgecolor': 'black'})
+        >>> rings_inner = radar.draw_circles(ax=ax, facecolor='None',
+        ...                                  edgecolor='black', linestyle='--')
         >>> range_labels = radar.draw_range_labels(ax=ax, fontsize=15, zorder=2)
         >>> param_labels = radar.draw_param_labels(ax=ax, fontsize=15, zorder=2)
         """
         validate_ax(ax)
 
         if int(distribution_values.shape[1]) != self.num_labels:
             msg = ('The size of params and distribution_values.shape[1] must match.'
```

### Comparing `mplsoccer-1.1.9/mplsoccer/scatterutils.py` & `mplsoccer-1.2.0/mplsoccer/scatterutils.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/mplsoccer/statsbomb.py` & `mplsoccer-1.2.0/mplsoccer/statsbomb.py`

 * *Files 2% similar despite different names*

```diff
@@ -347,16 +347,16 @@
         Returns
         -------
         events, related, freeze, tactics
             Either dataframes or flattened list of dictionaries.
 
         Examples
         --------
-        >>> from mplsoccer import Sbopen
-        >>> parser = Sbopen(dataframe=True)
+        >>> from mplsoccer import Sblocal
+        >>> parser = Sblocal(dataframe=True)
         >>> events, related, freeze, tactics = parser.event(path)
         """
         data = self._get_data(path)
         match_id = int(os.path.basename(path)[:-5])
         return flatten_event(data, match_id, self.dataframe)
 
     def lineup(self, path):
@@ -369,16 +369,16 @@
         Returns
         -------
         lineups
             A dataframe or a flattened list of dictionaries.
 
         Examples
         --------
-        >>> from mplsoccer import Sbopen
-        >>> parser = Sbopen(dataframe=True)
+        >>> from mplsoccer import Sblocal
+        >>> parser = Sblocal(dataframe=True)
         >>> lineups = parser.lineup(path)
         """
         data = self._get_data(path)
         match_id = int(os.path.basename(path)[:-5])
         return flatten_lineup(data, match_id, self.dataframe)
 
     def match(self, path):
@@ -391,16 +391,16 @@
         Returns
         -------
         matches
             A dataframe or a flattened list of dictionaries.
 
         Examples
         --------
-        >>> from mplsoccer import Sbopen
-        >>> parser = Sbopen(dataframe=True)
+        >>> from mplsoccer import Sblocal
+        >>> parser = Sblocal(dataframe=True)
         >>> matches = parser.match(path)
         """
         data = self._get_data(path)
         return flatten_match(data, self.dataframe)
 
     def competition(self, path):
         """ Read the competition data from a local file.
@@ -412,16 +412,16 @@
         Returns
         -------
         competition
             A dataframe or a flattened list of dictionaries.
 
         Examples
         --------
-        >>> from mplsoccer import Sbopen
-        >>> parser = Sbopen(dataframe=True)
+        >>> from mplsoccer import Sblocal
+        >>> parser = Sblocal(dataframe=True)
         >>> competition = parser.competition(path)
         """
         data = self._get_data(path)
         return pd.DataFrame(data) if self.dataframe else data
 
     def frame(self, path):
         """ Read the 360 data from a local file.
@@ -434,16 +434,16 @@
         Returns
         -------
         frames, visible
             Either dataframes or flattened list of dictionaries.
 
         Examples
         --------
-        >>> from mplsoccer import Sbopen
-        >>> parser = Sbopen(dataframe=True)
+        >>> from mplsoccer import Sblocal
+        >>> parser = Sblocal(dataframe=True)
         >>> frames, visible = parser.frame(path)
         """
         data = self._get_data(path)
         match_id = int(os.path.basename(path)[:-5])
         return flatten_360(data, match_id, self.dataframe)
 
 
@@ -500,14 +500,18 @@
 
 
 def _event_dataframe(data):
     """ Transform the event dictionary into a dataframe."""
     df = pd.DataFrame(data)
     if df.empty:
         return None
+    mask = df['tactics_formation'].notnull()
+    # tactics_formation from float to string
+    df.loc[mask, 'tactics_formation'] = df.loc[mask, 'tactics_formation'].astype(int).astype(str)
+    df.loc[~mask, 'tactics_formation'] = None
     df['timestamp'] = pd.to_datetime(df['timestamp']).dt.time
     df.sort_values(['period', 'timestamp', 'index'], inplace=True)
     df.reset_index(drop=True, inplace=True)
     for col in ['counterpress', 'under_pressure', 'off_camera', 'out']:
         if col in df.columns:
             df[col] = df[col].astype(float)
     return df
@@ -552,15 +556,18 @@
     if df.empty:
         return None
     df['kick_off'] = pd.to_datetime(df['match_date'] + ' ' + df['kick_off'])
     date_cols = ['match_date', 'last_updated', 'last_updated_360',
                  'home_team_managers_dob', 'away_team_managers_dob']
     for date in date_cols:
         if date in df.columns:
-            df[date] = pd.to_datetime(df[date])
+            if pd.__version__ < '2':
+                df[date] = pd.to_datetime(df[date])
+            else:
+                df[date] = pd.to_datetime(df[date], format='ISO8601')
     return df
 
 
 def flatten_event(events, match_id, dataframe=True):
     """ Flatten the events (list) so each row (dictionary) contains no nested events.
 
     Parameters
@@ -667,15 +674,15 @@
             player['match_id'] = match_id
             player['team_id'] = row['team_id']
             player['team_name'] = row['team_name']
             if 'country' in player:
                 player['country_id'] = player['country']['id']
                 player['country_name'] = player['country']['name']
                 del player['country']
-            if player['player_nickname'] is None:
+            if 'player_nickname' in player and player['player_nickname'] is None:
                 player['player_nickname'] = player['player_name']
             player.pop('positions', None)  # if flattened would be multiple lines
             player.pop('cards', None)  # if flattened would be multiple lines
             lineup.append(player)
     if dataframe:
         lineup = pd.DataFrame(lineup)
     return lineup
```

### Comparing `mplsoccer-1.1.9/tests/test_bin_statistic.py` & `mplsoccer-1.2.0/tests/test_bin_statistic.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/tests/test_grid.py` & `mplsoccer-1.2.0/tests/test_grid.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/tests/test_standarizer.py` & `mplsoccer-1.2.0/tests/test_standarizer.py`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/.gitignore` & `mplsoccer-1.2.0/.gitignore`

 * *Files identical despite different names*

### Comparing `mplsoccer-1.1.9/LICENSE` & `mplsoccer-1.2.0/LICENSE`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 MIT License
 
-Copyright (c) 2022 Anmol Durgapal, Andrew Rowlinson
+Copyright (c) 2023 Anmol Durgapal, Andrew Rowlinson
 
 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:
```

### Comparing `mplsoccer-1.1.9/README.md` & `mplsoccer-1.2.0/README.md`

 * *Files 10% similar despite different names*

```diff
@@ -7,15 +7,20 @@
 
 ## Installation
 
 Use the package manager [pip](https://pip.pypa.io/en/stable/) to install mplsoccer.
 
 ```bash
 pip install mplsoccer
-```
+
+Or install via [Anaconda](https://docs.anaconda.com/free/anaconda/install/index.html).
+
+```bash
+conda install -c conda-forge mplsoccer
+```  
 
 ---
 
 ## Docs
 
 Read more in the [docs](https://mplsoccer.readthedocs.io/) and see some 
 examples in our [gallery](https://mplsoccer.readthedocs.io/en/latest/gallery/index.html).
@@ -85,19 +90,18 @@
 for a full list of the recent changes to mplsoccer.
 
 ---
 
 ## Inspiration
 
 mplsoccer was inspired by:
-- [Peter McKeever](http://petermckeever.com/2020/10/how-to-draw-a-football-pitch/) heavily 
-inspired the API design
+- [Peter McKeever](https://petermckeever.com/) heavily inspired the API design
 - [ggsoccer](https://github.com/Torvaney/ggsoccer) influenced the design and Standardizer
 - [lastrow's](https://twitter.com/lastrowview) legendary animations
-- [fcrstats'](http://fcrstats.com/) tutorials for using football data
+- [fcrstats'](https://twitter.com/FC_rstats) tutorials for using football data
 - [fcpython's](https://fcpython.com/) Python tutorials for using football data
 - [Karun Singh's](https://twitter.com/karun1710) expected threat (xT) visualizations
 - [StatsBomb's](https://statsbomb.com/) great visual design and free open-data
 - John Burn-Murdoch's [tweet](https://twitter.com/jburnmurdoch/status/1057907312030085120) got me 
 interested in football analytics
 
 ---
```

### Comparing `mplsoccer-1.1.9/pyproject.toml` & `mplsoccer-1.2.0/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -27,15 +27,15 @@
   "Programming Language :: Python :: 3.7",
   "Programming Language :: Python :: 3.8",
   "Programming Language :: Python :: 3.9",
   "Programming Language :: Python :: 3.10",
   "Programming Language :: Python :: 3.11",
   "Topic :: Scientific/Engineering :: Visualization",
 ]
-dependencies = ['matplotlib',
+dependencies = ['matplotlib >= 3.6',
                 'numpy',
                 'pandas',
                 'Pillow',
                 'requests',
                 'scipy',
                 'seaborn',
 				]
```

### Comparing `mplsoccer-1.1.9/PKG-INFO` & `mplsoccer-1.2.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mplsoccer
-Version: 1.1.9
+Version: 1.2.0
 Summary: Football pitch plotting library for matplotlib
 Project-URL: Documentation, https://mplsoccer.readthedocs.io
 Project-URL: Issues, https://github.com/andrewRowlinson/mplsoccer/issues
 Project-URL: Source, https://github.com/andrewRowlinson/mplsoccer
 Author-email: Andrew Rowlinson <rowlinsonandy@gmail.com>, Anmol Durgapal <slothfulwave10@gmail.com>
 License-File: LICENSE
 Keywords: football,matplotlib,mplsoccer,soccer,visualization
@@ -15,15 +15,15 @@
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Scientific/Engineering :: Visualization
 Requires-Python: >=3.7
-Requires-Dist: matplotlib
+Requires-Dist: matplotlib>=3.6
 Requires-Dist: numpy
 Requires-Dist: pandas
 Requires-Dist: pillow
 Requires-Dist: requests
 Requires-Dist: scipy
 Requires-Dist: seaborn
 Description-Content-Type: text/markdown
@@ -37,15 +37,20 @@
 
 ## Installation
 
 Use the package manager [pip](https://pip.pypa.io/en/stable/) to install mplsoccer.
 
 ```bash
 pip install mplsoccer
-```
+
+Or install via [Anaconda](https://docs.anaconda.com/free/anaconda/install/index.html).
+
+```bash
+conda install -c conda-forge mplsoccer
+```  
 
 ---
 
 ## Docs
 
 Read more in the [docs](https://mplsoccer.readthedocs.io/) and see some 
 examples in our [gallery](https://mplsoccer.readthedocs.io/en/latest/gallery/index.html).
@@ -115,19 +120,18 @@
 for a full list of the recent changes to mplsoccer.
 
 ---
 
 ## Inspiration
 
 mplsoccer was inspired by:
-- [Peter McKeever](http://petermckeever.com/2020/10/how-to-draw-a-football-pitch/) heavily 
-inspired the API design
+- [Peter McKeever](https://petermckeever.com/) heavily inspired the API design
 - [ggsoccer](https://github.com/Torvaney/ggsoccer) influenced the design and Standardizer
 - [lastrow's](https://twitter.com/lastrowview) legendary animations
-- [fcrstats'](http://fcrstats.com/) tutorials for using football data
+- [fcrstats'](https://twitter.com/FC_rstats) tutorials for using football data
 - [fcpython's](https://fcpython.com/) Python tutorials for using football data
 - [Karun Singh's](https://twitter.com/karun1710) expected threat (xT) visualizations
 - [StatsBomb's](https://statsbomb.com/) great visual design and free open-data
 - John Burn-Murdoch's [tweet](https://twitter.com/jburnmurdoch/status/1057907312030085120) got me 
 interested in football analytics
 
 ---
```

