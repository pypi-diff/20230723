# Comparing `tmp/sphinx-readme-0.1.0.tar.gz` & `tmp/sphinx-readme-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sphinx-readme-0.1.0.tar", last modified: Fri Jul 21 07:31:33 2023, max compression
+gzip compressed data, was "sphinx-readme-0.2.0.tar", last modified: Sun Jul 23 12:36:53 2023, max compression
```

## Comparing `sphinx-readme-0.1.0.tar` & `sphinx-readme-0.2.0.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxrwxrwx   0        0        0        0 2023-07-21 07:31:33.748779 sphinx-readme-0.1.0/
--rw-rw-rw-   0        0        0     1084 2023-05-09 12:07:43.000000 sphinx-readme-0.1.0/LICENSE
--rw-rw-rw-   0        0        0     9734 2023-07-21 07:31:33.733156 sphinx-readme-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0     8945 2023-07-21 07:31:07.000000 sphinx-readme-0.1.0/README.rst
--rw-rw-rw-   0        0        0       42 2023-07-21 07:31:33.748779 sphinx-readme-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0     1454 2023-07-18 11:51:26.000000 sphinx-readme-0.1.0/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-21 07:31:33.696196 sphinx-readme-0.1.0/sphinx_readme/
--rw-rw-rw-   0        0        0     1703 2023-07-21 07:28:05.000000 sphinx-readme-0.1.0/sphinx_readme/__init__.py
--rw-rw-rw-   0        0        0    11533 2023-07-21 07:23:43.000000 sphinx-readme-0.1.0/sphinx_readme/config.py
--rw-rw-rw-   0        0        0    24336 2023-07-21 07:23:43.000000 sphinx-readme-0.1.0/sphinx_readme/parser.py
-drwxrwxrwx   0        0        0        0 2023-07-21 07:31:33.733156 sphinx-readme-0.1.0/sphinx_readme/utils/
--rw-rw-rw-   0        0        0        0 2023-07-21 06:42:57.000000 sphinx-readme-0.1.0/sphinx_readme/utils/__init__.py
--rw-rw-rw-   0        0        0      603 2023-07-21 07:23:43.000000 sphinx-readme-0.1.0/sphinx_readme/utils/docutils.py
--rw-rw-rw-   0        0        0     4643 2023-07-21 06:42:57.000000 sphinx-readme-0.1.0/sphinx_readme/utils/git.py
--rw-rw-rw-   0        0        0     3727 2023-07-21 06:42:57.000000 sphinx-readme-0.1.0/sphinx_readme/utils/linkcode.py
--rw-rw-rw-   0        0        0     6453 2023-07-21 07:23:43.000000 sphinx-readme-0.1.0/sphinx_readme/utils/rst.py
--rw-rw-rw-   0        0        0      810 2023-07-21 06:42:57.000000 sphinx-readme-0.1.0/sphinx_readme/utils/sphinx.py
-drwxrwxrwx   0        0        0        0 2023-07-21 07:31:33.732097 sphinx-readme-0.1.0/sphinx_readme.egg-info/
--rw-rw-rw-   0        0        0     9734 2023-07-21 07:31:33.000000 sphinx-readme-0.1.0/sphinx_readme.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      465 2023-07-21 07:31:33.000000 sphinx-readme-0.1.0/sphinx_readme.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-21 07:31:33.000000 sphinx-readme-0.1.0/sphinx_readme.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       12 2023-07-21 07:31:33.000000 sphinx-readme-0.1.0/sphinx_readme.egg-info/requires.txt
--rw-rw-rw-   0        0        0       14 2023-07-21 07:31:33.000000 sphinx-readme-0.1.0/sphinx_readme.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 12:36:53.188485 sphinx-readme-0.2.0/
+-rw-rw-rw-   0        0        0     1084 2023-05-09 12:07:43.000000 sphinx-readme-0.2.0/LICENSE
+-rw-rw-rw-   0        0        0     9427 2023-07-23 12:36:53.187487 sphinx-readme-0.2.0/PKG-INFO
+-rw-rw-rw-   0        0        0     8638 2023-07-23 12:35:55.000000 sphinx-readme-0.2.0/README.rst
+-rw-rw-rw-   0        0        0       42 2023-07-23 12:36:53.189529 sphinx-readme-0.2.0/setup.cfg
+-rw-rw-rw-   0        0        0     1454 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:36:53.157273 sphinx-readme-0.2.0/sphinx_readme/
+-rw-rw-rw-   0        0        0     1768 2023-07-23 12:31:35.000000 sphinx-readme-0.2.0/sphinx_readme/__init__.py
+-rw-rw-rw-   0        0        0    12014 2023-07-23 12:17:16.000000 sphinx-readme-0.2.0/sphinx_readme/config.py
+-rw-rw-rw-   0        0        0    24708 2023-07-23 10:33:01.000000 sphinx-readme-0.2.0/sphinx_readme/parser.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:36:53.185493 sphinx-readme-0.2.0/sphinx_readme/utils/
+-rw-rw-rw-   0        0        0        0 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/__init__.py
+-rw-rw-rw-   0        0        0      603 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/docutils.py
+-rw-rw-rw-   0        0        0     4643 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/git.py
+-rw-rw-rw-   0        0        0     3727 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/linkcode.py
+-rw-rw-rw-   0        0        0     7578 2023-07-23 12:19:01.000000 sphinx-readme-0.2.0/sphinx_readme/utils/rst.py
+-rw-rw-rw-   0        0        0      810 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/sphinx.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:36:53.178460 sphinx-readme-0.2.0/sphinx_readme.egg-info/
+-rw-rw-rw-   0        0        0     9427 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      465 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/top_level.txt
```

### Comparing `sphinx-readme-0.1.0/LICENSE` & `sphinx-readme-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.1.0/PKG-INFO` & `sphinx-readme-0.2.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sphinx-readme
-Version: 0.1.0
+Version: 0.2.0
 Summary: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 Home-page: https://github.com/tdkorn/sphinx-readme
 Author: Adam Korn
 Author-email: hello@dailykitten.net
 License: MIT License
 Download-URL: https://github.com/TDKorn/sphinx-readme/tarball/main
 Keywords: sphinx,docutils,sphinx-extension,sphinx-contrib,reStructuredText,rst,reST,parser,rst-parser,README.rst,README,autodoc,linkcode
@@ -12,65 +12,64 @@
 Classifier: Framework :: Sphinx :: Extension
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Description-Content-Type: text/x-rst; charset=UTF-8
 License-File: LICENSE
 
-.. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
-.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.1.0/sphinx_readme/parser.py#L208-L232
-.. |.`sphinx.ext.linkcode`| replace:: ``sphinx.ext.linkcode``
-.. _.`sphinx.ext.linkcode`: https://www.sphinx-doc.org/en/master/usage/extensions/linkcode.html#module-sphinx.ext.linkcode
-.. |.`~.sphinx.ext.autodoc`| replace:: ``autodoc``
-.. _.`~.sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
-.. |.`sphinx.ext.autodoc`| replace:: ``sphinx.ext.autodoc``
-.. _.`sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
-.. |attention| replace:: 🔔️
-.. |caution| replace:: ⚠️
-.. |danger| replace:: ☢️
-.. |error| replace:: ⛔
-.. |hint| replace:: 🧠
-.. |important| replace:: 📢
-.. |note| replace:: 📝
-.. |tip| replace:: 💡
-.. |warning| replace:: 🚩
-.. |default| replace:: 📄
-.. |about| replace:: 📚
-
-.. |html_context| replace:: ``html_context``
-.. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
 .. |html_baseurl| replace:: ``html_baseurl``
 .. _html_baseurl: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_baseurl
-.. |readme_src_files| replace:: ``readme_src_files``
-.. _readme_src_files: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_src_files
+.. |html_context| replace:: ``html_context``
+.. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
+.. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
+.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.0/sphinx_readme/parser.py#L213-L237
 .. |readme_docs_url_type| replace:: ``readme_docs_url_type``
 .. _readme_docs_url_type: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_docs_url_type
-.. |readme_replace_attrs| replace:: ``readme_replace_attrs``
-.. _readme_replace_attrs: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_replace_attrs
 .. |readme_inline_markup| replace:: ``readme_inline_markup``
 .. _readme_inline_markup: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_inline_markup
 .. |readme_raw_directive| replace:: ``readme_raw_directive``
 .. _readme_raw_directive: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_raw_directive
+.. |readme_replace_attrs| replace:: ``readme_replace_attrs``
+.. _readme_replace_attrs: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_replace_attrs
+.. |readme_src_files| replace:: ``readme_src_files``
+.. _readme_src_files: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_src_files
+.. |.`sphinx.ext.autodoc`| replace:: ``sphinx.ext.autodoc``
+.. _.`sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
+.. |.`~.sphinx.ext.autodoc`| replace:: ``autodoc``
+.. _.`~.sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
+.. |.`sphinx.ext.linkcode`| replace:: ``sphinx.ext.linkcode``
+.. _.`sphinx.ext.linkcode`: https://www.sphinx-doc.org/en/master/usage/extensions/linkcode.html#module-sphinx.ext.linkcode
 
 .. meta::
    :author: Adam Korn
    :title: Sphinx README
    :description: Sphinx Extension to Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
 Sphinx README - Generate Beautiful ``README.rst`` for GitHub, PyPi, GitLab, BitBucket
 --------------------------------------------------------------------------------------
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.1.0/docs/source/_static/logo_transparent.png
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/logo_transparent.png
    :alt: Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
    :align: center
    :width: 25%
 
-A Sphinx extension to generate ``README.rst`` files that render beautifully on GitHub, PyPi, GitLab, BitBucket
 
 
+
+
+
+
+
+
+
+
+
+
+A Sphinx extension to generate ``README.rst`` files that render beautifully on GitHub, PyPi, GitLab, BitBucket
+
 .. |RTD| replace:: **Explore the docs »**
 .. _RTD: https://sphinx-readme.readthedocs.io/en/latest/
 
 |RTD|_
 
 |
 
@@ -86,37 +85,40 @@
    :target: https://pepy.tech/project/sphinx-readme
    :alt: Downloads for Sphinx README
 
 .. image:: https://readthedocs.org/projects/sphinx-readme/badge/?version=latest
    :target: https://sphinx-readme.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation for Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
+
+
+
 |
 
 About Sphinx README
 ~~~~~~~~~~~~~~~~~~~~~~~
 
 
 .. csv-table::
-   :header: |about| What's Sphinx README?
+   :header: 📚 What's Sphinx README?
 
    "``sphinx_readme`` is a ``reStructuredText`` parser that uses Sphinx
    to generate ``rst`` files that render beautifully on
    GitHub, PyPi, GitLab, and BitBucket."
 
 
 
 **With** ``sphinx_readme`` **, there's no need to rewrite your** ``README.rst`` **as a** ``README.md`` **file**
 
 Files generated by ``sphinx_readme`` have nearly identical appearance and functionality
 as ``html`` builds, including |.`sphinx.ext.autodoc`|_ cross-references!
 
 |
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.1.0/docs/source/_static/demo/demo.gif
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/demo/demo.gif
    :alt: Demonstration of how reStructuredText README.rst files generated by Sphinx README render on GitHub, PyPi, GitLab, BitBucket
    :width: 75%
 
 
 📋 Features
 ~~~~~~~~~~~~
 
@@ -190,15 +192,15 @@
 |readme_src_files|_
  An individual or list of ``rst`` files to parse
 
   Type: ``Union[str, List]``
 
 
 .. csv-table::
-   :header: |important| Important
+   :header: 📢 Important
 
    "Filepaths should be specified relative to the source directory"
 
 
 |
 
 |readme_docs_url_type|_
@@ -215,15 +217,15 @@
 
  * ``"html"``: replaces references with links to HTML documentation entries
 
    **Example**: |parse_intersphinx_nodes_html|_
 
 
 .. csv-table::
-   :header: |note| Note
+   :header: 📝 Note
 
    "If set to ``code``, then :code:`:attr:` cross-references will not be replaced with links
 
    * Instead, they'll be replaced with ``inline literals`` or left as is
    * Please see |readme_replace_attrs|_ and |readme_inline_markup|_"
 
 
@@ -253,15 +255,15 @@
 
    readme_docs_url_type = "code"
 
 
 
 
 .. csv-table::
-   :header: |important| Important
+   :header: 📢 Important
 
    "For platforms that don't support the ``raw`` directive (PyPi, GitLab, and BitBucket),
    be sure to disable |readme_raw_directive|_:
 
    .. code-block:: python
 
       readme_raw_directive = False"
```

### Comparing `sphinx-readme-0.1.0/README.rst` & `sphinx-readme-0.2.0/README.rst`

 * *Files 3% similar despite different names*

```diff
@@ -1,58 +1,57 @@
-.. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
-.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.1.0/sphinx_readme/parser.py#L208-L232
-.. |.`sphinx.ext.linkcode`| replace:: ``sphinx.ext.linkcode``
-.. _.`sphinx.ext.linkcode`: https://www.sphinx-doc.org/en/master/usage/extensions/linkcode.html#module-sphinx.ext.linkcode
-.. |.`~.sphinx.ext.autodoc`| replace:: ``autodoc``
-.. _.`~.sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
-.. |.`sphinx.ext.autodoc`| replace:: ``sphinx.ext.autodoc``
-.. _.`sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
-.. |attention| replace:: 🔔️
-.. |caution| replace:: ⚠️
-.. |danger| replace:: ☢️
-.. |error| replace:: ⛔
-.. |hint| replace:: 🧠
-.. |important| replace:: 📢
-.. |note| replace:: 📝
-.. |tip| replace:: 💡
-.. |warning| replace:: 🚩
-.. |default| replace:: 📄
-.. |about| replace:: 📚
-
-.. |html_context| replace:: ``html_context``
-.. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
 .. |html_baseurl| replace:: ``html_baseurl``
 .. _html_baseurl: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_baseurl
-.. |readme_src_files| replace:: ``readme_src_files``
-.. _readme_src_files: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_src_files
+.. |html_context| replace:: ``html_context``
+.. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
+.. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
+.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.0/sphinx_readme/parser.py#L213-L237
 .. |readme_docs_url_type| replace:: ``readme_docs_url_type``
 .. _readme_docs_url_type: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_docs_url_type
-.. |readme_replace_attrs| replace:: ``readme_replace_attrs``
-.. _readme_replace_attrs: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_replace_attrs
 .. |readme_inline_markup| replace:: ``readme_inline_markup``
 .. _readme_inline_markup: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_inline_markup
 .. |readme_raw_directive| replace:: ``readme_raw_directive``
 .. _readme_raw_directive: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_raw_directive
+.. |readme_replace_attrs| replace:: ``readme_replace_attrs``
+.. _readme_replace_attrs: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_replace_attrs
+.. |readme_src_files| replace:: ``readme_src_files``
+.. _readme_src_files: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_src_files
+.. |.`sphinx.ext.autodoc`| replace:: ``sphinx.ext.autodoc``
+.. _.`sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
+.. |.`~.sphinx.ext.autodoc`| replace:: ``autodoc``
+.. _.`~.sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
+.. |.`sphinx.ext.linkcode`| replace:: ``sphinx.ext.linkcode``
+.. _.`sphinx.ext.linkcode`: https://www.sphinx-doc.org/en/master/usage/extensions/linkcode.html#module-sphinx.ext.linkcode
 
 .. meta::
    :author: Adam Korn
    :title: Sphinx README
    :description: Sphinx Extension to Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
 Sphinx README - Generate Beautiful ``README.rst`` for GitHub, PyPi, GitLab, BitBucket
 --------------------------------------------------------------------------------------
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.1.0/docs/source/_static/logo_transparent.png
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/logo_transparent.png
    :alt: Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
    :align: center
    :width: 25%
 
-A Sphinx extension to generate ``README.rst`` files that render beautifully on GitHub, PyPi, GitLab, BitBucket
 
 
+
+
+
+
+
+
+
+
+
+
+A Sphinx extension to generate ``README.rst`` files that render beautifully on GitHub, PyPi, GitLab, BitBucket
+
 .. |RTD| replace:: **Explore the docs »**
 .. _RTD: https://sphinx-readme.readthedocs.io/en/latest/
 
 |RTD|_
 
 |
 
@@ -68,37 +67,40 @@
    :target: https://pepy.tech/project/sphinx-readme
    :alt: Downloads for Sphinx README
 
 .. image:: https://readthedocs.org/projects/sphinx-readme/badge/?version=latest
    :target: https://sphinx-readme.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation for Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
+
+
+
 |
 
 About Sphinx README
 ~~~~~~~~~~~~~~~~~~~~~~~
 
 
 .. csv-table::
-   :header: |about| What's Sphinx README?
+   :header: 📚 What's Sphinx README?
 
    "``sphinx_readme`` is a ``reStructuredText`` parser that uses Sphinx
    to generate ``rst`` files that render beautifully on
    GitHub, PyPi, GitLab, and BitBucket."
 
 
 
 **With** ``sphinx_readme`` **, there's no need to rewrite your** ``README.rst`` **as a** ``README.md`` **file**
 
 Files generated by ``sphinx_readme`` have nearly identical appearance and functionality
 as ``html`` builds, including |.`sphinx.ext.autodoc`|_ cross-references!
 
 |
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.1.0/docs/source/_static/demo/demo.gif
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/demo/demo.gif
    :alt: Demonstration of how reStructuredText README.rst files generated by Sphinx README render on GitHub, PyPi, GitLab, BitBucket
    :width: 75%
 
 
 📋 Features
 ~~~~~~~~~~~~
 
@@ -172,15 +174,15 @@
 |readme_src_files|_
  An individual or list of ``rst`` files to parse
 
   Type: ``Union[str, List]``
 
 
 .. csv-table::
-   :header: |important| Important
+   :header: 📢 Important
 
    "Filepaths should be specified relative to the source directory"
 
 
 |
 
 |readme_docs_url_type|_
@@ -197,15 +199,15 @@
 
  * ``"html"``: replaces references with links to HTML documentation entries
 
    **Example**: |parse_intersphinx_nodes_html|_
 
 
 .. csv-table::
-   :header: |note| Note
+   :header: 📝 Note
 
    "If set to ``code``, then :code:`:attr:` cross-references will not be replaced with links
 
    * Instead, they'll be replaced with ``inline literals`` or left as is
    * Please see |readme_replace_attrs|_ and |readme_inline_markup|_"
 
 
@@ -235,15 +237,15 @@
 
    readme_docs_url_type = "code"
 
 
 
 
 .. csv-table::
-   :header: |important| Important
+   :header: 📢 Important
 
    "For platforms that don't support the ``raw`` directive (PyPi, GitLab, and BitBucket),
    be sure to disable |readme_raw_directive|_:
 
    .. code-block:: python
 
       readme_raw_directive = False"
```

### Comparing `sphinx-readme-0.1.0/setup.py` & `sphinx-readme-0.2.0/setup.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.1.0/sphinx_readme/__init__.py` & `sphinx-readme-0.2.0/sphinx_readme/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 from sphinx.environment import BuildEnvironment
 
 from sphinx_readme.utils.sphinx import get_conf_val, set_conf_val
 from sphinx_readme.utils.git import get_repo_dir
 from sphinx_readme.parser import READMEParser
 
 
-__version__ = "v0.1.0"
+__version__ = "v0.2.0"
 
 
 def setup(app: Sphinx) -> Dict[str, Any]:
     # Avoid setting up extension if building on ReadTheDocs
     if os.environ.get("READTHEDOCS") == "True":
         return {}
 
@@ -23,16 +23,17 @@
     app.connect('build-finished', resolve)
 
     app.add_config_value("readme_inline_markup", True, True)
     app.add_config_value("readme_raw_directive", True, True)
     app.add_config_value("readme_include_directive", True, True)
     app.add_config_value("readme_replace_attrs", True, True)
     app.add_config_value("readme_out_dir", get_repo_dir(), True)
-    app.add_config_value("readme_blob", 'head', True)
     app.add_config_value("readme_default_admonition_icon", "📄", True)
+    app.add_config_value("readme_tags", ["readme"], True, list)
+    app.add_config_value("readme_blob", 'head', True)
 
     set_conf_val(app, 'READMEParser', READMEParser(app))
 
     return {'version': sphinx.__display_version__, 'parallel_read_safe': True}
 
 
 def parse_env(app: Sphinx, env: BuildEnvironment):
```

### Comparing `sphinx-readme-0.1.0/sphinx_readme/config.py` & `sphinx-readme-0.2.0/sphinx_readme/config.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 import re
 from pathlib import Path
-from typing import Union, List, Dict, Callable
+from typing import Union, List, Dict
 from functools import cached_property
 
+from sphinx.util.tags import Tags
 from sphinx.application import Sphinx
 from sphinx.errors import ExtensionError
 
 from sphinx_readme.utils.git import get_repo_url, get_blob_url, get_repo_host, get_repo_dir
 from sphinx_readme.utils.rst import replace_only_directives, remove_raw_directives
 from sphinx_readme.utils.linkcode import get_linkcode_url, get_linkcode_resolve
 from sphinx_readme.utils.sphinx import get_conf_val, set_conf_val, logger
@@ -16,14 +17,15 @@
 
     def __init__(self, app: Sphinx):
         self.logger = logger
         self.src_dir = Path(app.srcdir)
         self.repo_dir = get_repo_dir()
         self.out_dir = get_conf_val(app, 'readme_out_dir')
         self.src_files = get_conf_val(app, 'readme_src_files', [])
+        self.tags = Tags(get_conf_val(app, "readme_tags"))
         self.html_context = get_conf_val(app, "html_context")
         self.html_baseurl = get_conf_val(app, "html_baseurl", "").rstrip("/")
         self.docs_url_type = get_conf_val(app, 'readme_docs_url_type')
         self.replace_attrs = get_conf_val(app, 'readme_replace_attrs')
         self.inline_markup = get_conf_val(app, 'readme_inline_markup')
         self.raw_directive = get_conf_val(app, 'readme_raw_directive')
         self.rubric_heading = get_conf_val(app, 'readme_rubric_heading')
@@ -115,58 +117,67 @@
         :param rst_file: the ``rst`` file to read
         :param replace_only: specifies if :rst:dir:`only` directives should be replaced or not
         """
         with open(rst_file, 'r', encoding='utf-8') as f:
             rst = f.read()
 
         if replace_only:
-            rst = replace_only_directives(rst)
+            rst = replace_only_directives(rst, self.tags)
 
-        include_pattern = r"\.\. include:: ([./]*?[\w/-]+\.\w+?)\s*?$"
-
-        if self.include_directive:
-            # Find all included files
-            included = re.findall(
-                pattern=include_pattern,
-                string=rst,
-                flags=re.M
-            )
-            for include in included:
-                # Determine abs path of included file
-                if include.startswith("/"):
-                    # These paths are relative to source dir
-                    file = Path(f"{self.src_dir}{include}").resolve()
-                else:
-                    # These paths are relative to rst_file dir
-                    file = (Path(rst_file).parent / Path(include)).resolve()
-
-                if file.exists():
-                    # Replace directive with the file content
-                    repl = self.read_rst(file, replace_only).replace(r'\n', r'\\n')
-                else:
-                    # Remove the directive
-                    repl = ''
-                    self.logger.error(
-                        f"``sphinx_readme``: included file {file} does not exist"
-                    )
-                rst = re.sub(
-                    pattern=rf"\.\. include:: {include}\s*?$",
-                    repl=repl,
-                    string=rst,
-                    flags=re.M
-                )
-        else:
-            # Remove all include directives from the text
-            rst = re.sub(include_pattern, '', rst, flags=re.M)
+        rst = self.parse_include_directives(rst, rst_file, replace_only)
 
         if self.raw_directive is False:
             rst = remove_raw_directives(rst)
 
         return rst
 
+    def parse_include_directives(self, rst: str, rst_file: Union[str, Path], replace_only: bool = True):
+        return re.sub(
+            pattern=r"\.\. include::\s+([./]*?[\w/-]+\.\w+)\s*?((?:^[ ]+:\S+:.*?$)*?)(?=\n*\S+|\Z)",
+            repl=lambda m: self._parse_include(m, rst_file, replace_only),
+            string=rst, flags=re.M | re.DOTALL
+        )
+
+    def _parse_include(self, match: re.Match, rst_file: Union[str, Path], replace_only: bool):
+        if self.include_directive is False:
+            return ''
+
+        file, args = match.groups()
+
+        if start := re.match(r".*:start-line:\s+(\d+).*", args, re.DOTALL):
+            start = int(start.group(1))
+
+        if end := re.match(r".*:end-line:\s+(\d+).*", args, re.DOTALL):
+            end = int(end.group(1))
+
+        # Determine abs path of included file
+        if file.startswith("/"):
+            # These paths are relative to source dir
+            file = Path(f"{self.src_dir}{file}").resolve()
+        else:
+            # These paths are relative to rst_file dir
+            file = (Path(rst_file).parent / Path(file)).resolve()
+
+        if file.exists():
+            # Write corresponding lines of unparsed file to a temp file
+            lines = file.read_text(encoding='utf-8').split('\n')[start:end]
+            temp = Path(self.src_dir / (Path(rst_file).stem + "_temp.rst"))
+            temp.write_text('\n'.join(lines), "utf-8")
+
+            # Replace directive with parsed file content
+            repl = self.read_rst(temp, replace_only).replace(r'\n', r'\\n')
+            temp.unlink()
+
+        else:
+            repl = ''  # Remove the directive
+            self.logger.error(
+                f"``sphinx_readme``: included file {file} does not exist"
+            )
+        return repl
+
     @property
     def src_files(self) -> List[str]:
         """Absolute paths of the :confval:`readme_src_files`"""
         return self._src_files
 
     @src_files.setter
     def src_files(self, src_files: Union[str, List[str]]):
```

### Comparing `sphinx-readme-0.1.0/sphinx_readme/parser.py` & `sphinx-readme-0.2.0/sphinx_readme/parser.py`

 * *Files 5% similar despite different names*

```diff
@@ -27,36 +27,41 @@
         self.sources: Dict[str, str] = self.config.sources
         #: Mapping of source files to their toctree data
         self.toctrees: Dict[str, List[Dict]] = defaultdict(list)
         #: Mapping of source files to their admonition data
         self.admonitions: Dict[str, Dict[str, List[Dict]]] = {}
         #: Mapping of docnames to their parsed titles
         self.titles: Dict[str, str] = {}
+        #: Mapping of cross-reference targets to their substitution definitions
+        self.substitutions: Dict[str, List[str]] = {}
         #: Standard cross-reference roles
         self.roles: Set[str] = {"doc", "ref"}
 
     def parse_env(self, env: BuildEnvironment) -> None:
         """Parses domain data and document titles from the |env|"""
         self.parse_titles(env)
         self.parse_py_domain(env)
         self.parse_std_domain(env)
 
     def parse_titles(self, env: BuildEnvironment) -> None:
-        """Parses document titles from the |env|"""
-        for docname, title_node in env.titles.items():
-            parts = []
-
-            for child in title_node.children:
-                text = child.astext()
-                if isinstance(child, nodes.literal):
-                    parts.append(f"``{text}``")
-                else:
-                    parts.append(text)
-
-            self.titles[docname] = ' '.join(parts)
+        """Parses document and section titles from the |env|"""
+        for docname in env.found_docs:
+            doctree = env.get_doctree(docname)
+            sections = list(doctree.findall(nodes.section))
+
+            for section in sections:
+                # Parse titles of sections referenced with :ref:
+                if getattr(section, "expect_referenced_by_name", None):
+                    ref_id = list(section.expect_referenced_by_name)[0]
+                    title = section.next_node(nodes.title)
+                    self.titles[ref_id] = title.rawsource
+
+            # Parse title of document for :doc: refs
+            h1 = sections[0].next_node(nodes.title)
+            self.titles[docname] = h1.rawsource
 
     def parse_std_domain(self, env: BuildEnvironment) -> None:
         """Parses cross-reference data from the |std_domain|
 
         :param env: the |env|
         """
         domain = env.get_domain("std")
@@ -263,17 +268,19 @@
             rst = self.replace_toctrees(src, rst)
             rst = self.replace_rst_rubrics(rst)
             rst = self.replace_py_xrefs(rst)
 
             for role in self.roles:
                 rst = self.replace_std_xrefs(role, rst)
 
-            # Use ref_map to generate autodoc substitution definitions
-            header_vals = self.get_header_vals()
-
+            # Prepend substitution definitions for cross-reference
+            header_vals = [
+                '\n'.join(self.substitutions[target])
+                for target in sorted(self.substitutions, key=lambda t: (t.lstrip("`~."), t))
+            ]
             # Write the final output
             rst_out = Path(self.config.out_dir, Path(src).name)
 
             with open(rst_out, 'w', encoding='utf-8') as f:
                 f.write(
                     "\n".join(header_vals) + "\n\n" + rst)
             print(
@@ -453,114 +460,114 @@
         :param rst: content of the source file
         """
         # Find all :ref_role:`ref_id` or :ref_role:`title <ref_id>` cross-refs
         xrefs = re.findall(
             pattern=fr"(?:\s*?):{ref_role}:`(([^`]+?)(?:\s<([\w./]+?)>)?)`(?=\s*?)",
             string=rst
         )
-        substitutions = []
-
         for xref in xrefs:
             if not all(xref):  # :ref_role:`ref_id` ->  ('ref_id', 'ref_id', '')
                 ref, ref_id, title = xref
 
             else:  # :ref_role:`title <ref_id>` -> ('title <ref_id>', 'title', 'ref_id')
                 ref, title, ref_id = xref
 
             # Match these ids up with target data in the ref_map
             if info := self.ref_map.get(ref_role, {}).get(ref_id, {}):
                 # Replace cross-refs with `text <link>`_ or substitutions
                 link, subs = format_hyperlink(
                     target=info['target'],
                     text=title or info['replace']
                 )
-                substitutions.extend(subs)
+                if subs:
+                    self.substitutions[ref_id] = subs
+
                 rst = re.sub(
                     pattern=rf":{ref_role}:`{escape_rst(ref)}`",
                     repl=link,
                     string=rst
                 )
-        if substitutions:
-            # Substitutions are used for inline literals
-            rst = "\n".join(substitutions) + "\n\n" + rst
-
         return rst
 
     def replace_py_xrefs(self, rst: str) -> str:
-        """Replace :mod:`~sphinx.ext.autodoc` cross-references with substitutions
+        """Replace |py_domain| cross-references with substitutions
 
         These substitutions will be hyperlinked to the corresponding source code
         or HTML documentation entry, depending on the value of
         :confval:`readme_docs_url_type`
 
         .. note: Attributes will only be hyperlinked
            if linking to HTML documentation
 
         :param rst: content of the source file
         """
-        # To render on GitHub/PyPi/etc., we use Sphinx substitutions instead of cross-refs
+        valid_xrefs = []
+        # To render on GitHub/PyPi/etc., substitutions are used instead of cross-refs
         # Syntax is |.{ref}|_ or |.`{ref}`|_
         if self.config.inline_markup:
             repl = r"|.`\1`|_"
         else:
             repl = r"|.\1|_"
 
-        # Replace cross-refs with substitutions
-        rst = re.sub(self.py_xref_regex, repl, rst)
-
-        # If linking to source code, replace :attr:`~.attribute` with ``attribute``
-        if self.config.docs_url_type == "code" and self.config.replace_attrs:
-            rst = replace_attrs(rst)
-
-        return rst
-
-    def get_header_vals(self) -> List[str]:
-        """Returns a list of substitution definitions and hyperlink references to prepend to the file"""
-        header = []
-
         for ref in self.py_xrefs:
-            info = self.ref_map.get(ref)
-
             # Check for invalid ref
-            if info is None:
+            if info := self.ref_map.get(ref):
+                valid_xrefs.append(ref)
+            else:
                 continue
 
             if self.config.inline_markup:
                 ref = f"`{ref}`"
 
-            header.extend([
+            self.substitutions[ref] = [
                 f".. |.{ref}| replace:: {info['replace']}",
                 f".. _.{ref}: {info['target']}"
-            ])
+            ]
+        # Replace cross-refs with substitutions
+        pattern = self.get_py_xref_regex(valid_xrefs)
+        rst = re.sub(pattern, repl, rst)
 
-        if not self.config.raw_directive:
-            for _type, icon in self.config.icon_map.items():
-                header.append(f'.. |{_type}| replace:: {icon}')
+        # If linking to source code, replace :attr:`~.attribute` with ``attribute``
+        if self.config.docs_url_type == "code" and self.config.replace_attrs:
+            rst = replace_attrs(rst)
 
-        return header
+        return rst
 
     @cached_property
     def py_xrefs(self) -> Set[str]:
-        """Python domain cross-reference targets found within source files"""
+        """|py_domain| cross-reference targets found within source files"""
         xrefs = set()
         for src, rst in self.sources.items():
             xrefs.update(
-                set(re.findall(self.py_xref_regex, rst)))
+                set(re.findall(self.get_py_xref_regex(), rst)))
         return xrefs
 
     @cached_property
-    def py_xref_regex(self) -> str:
-        """The regular expression to match Python domain cross-references"""
+    def py_xref_roles(self) -> str:
+        """The |py_domain| cross-reference roles that can be replaced with substitutions"""
         roles = r"mod|class|meth|func"
         # If linking to HTML docs, we can generate cross-refs for attributes
         if self.config.docs_url_type == "html":
             if self.config.replace_attrs:
                 roles += "|attr"
+        return roles
 
-        return rf":(?:{roles}):`(~?\.?[.\w]+)`"
+    def get_py_xref_regex(self, target: Optional[Union[str, List[str]]] = None) -> str:
+        """Returns the regex to match |py_domain| cross-reference targets
+
+        :param target: an individual or list of targets to match
+        """
+        if target is None:
+            # Match every cross-reference
+            target = r"(~?\.?[.\w]+)"
+
+        elif isinstance(target, list):
+            target = f"({'|'.join(target)})"
+
+        return rf":(?:{self.py_xref_roles}):`{target}`"
 
     def get_admonition_regex(self, admonition: Dict[str, str], admonition_type: str) -> str:
         """Returns the regex to match a specific admonition directive
 
         :param admonition: a dict containing admonition data
         :param admonition_type: ``"generic"`` or ``"specific"``
         """
@@ -596,18 +603,11 @@
         return pattern
 
     def get_admonition_icon(self, admonition: dict) -> str:
         """Returns the icon to use for an admonition
 
         :param admonition: a dict of admonition data
         """
-        icon = self.config.icon_map.get(admonition['class'])
-
-        # Raw directive allows for using icon directly
-        if self.config.raw_directive:
-            return icon if icon else self.config.default_admonition_icon
-
-        if icon:  # Without raw directive, must use substitution
-            return f"|{admonition['class']}|"
-
-        # Use default icon if admonition class isn't in icon map
-        return "|default|"
+        if icon := self.config.icon_map.get(admonition['class']):
+            return icon
+        else:
+            return self.config.default_admonition_icon
```

### Comparing `sphinx-readme-0.1.0/sphinx_readme/utils/docutils.py` & `sphinx-readme-0.2.0/sphinx_readme/utils/docutils.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.1.0/sphinx_readme/utils/git.py` & `sphinx-readme-0.2.0/sphinx_readme/utils/git.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.1.0/sphinx_readme/utils/linkcode.py` & `sphinx-readme-0.2.0/sphinx_readme/utils/linkcode.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.1.0/sphinx_readme/utils/rst.py` & `sphinx-readme-0.2.0/sphinx_readme/utils/rst.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import re
 from typing import List, Optional, Tuple
+import sphinx.util.tags
 
 
 def escape_rst(rst: str) -> str:
     """Escape regex special characters from the content of an ``rst`` file"""
     for char in ".+?*|()<>{}^$[]":
         rst = rst.replace(char, rf"\{char}")
     return rst
@@ -78,33 +79,77 @@
             parts.append(part.strip())
         else:
             parts.append(f"{markup}{part}{markup}")
 
     return " ".join(parts)
 
 
-def replace_only_directives(rst: str) -> str:
+def replace_only_directives(rst: str, tags: sphinx.util.tags.Tags) -> str:
     """Replaces and removes :rst:dir:`only` directives.
 
-    If ``"readme"`` is in the ``<expression>`` part of the
-    directive, the content of the directive will be used.
+    The :confval:`readme_tags` are temporarily added as :external+sphinx:ref:`tags <conf-tags>`,
+    then the ``<expression>`` argument of the directive is evaluated.
+
+    * If ``True``, the content will be used
+    * If ``False``, the directive is removed
+
+    .. tip:: The default value of :confval:`readme_tags` is ``["readme"]``
+
+
+    **Expression Examples:**
+
+    Using default value of :rst:`readme_tags = ["readme"]`:
+
+    .. code-block:: rst
+
+       .. only:: readme
+
+          This will be included in the generated file
+
+       .. only:: html
+
+          This will be excluded from the generated file
+
+       .. only:: readme or html
+
+          This will be included in the generated file
+
+       .. only:: readme and html
+
+          This will be excluded from the generated file.
+
+    Setting :rst:`readme_tags = ["pypi"]` in ``conf.py``:
+
+    .. code-block:: rst
+
+       .. only:: pypi
+
+          This will be included in the generated file
+
+       .. only:: readme
+
+          This will be excluded from the generated file
+
+       .. only:: readme or pypi
+
+          This will be included in the generated file
 
-    Otherwise, the directive will be removed.
 
     :param rst: the content of an ``rst`` file
+    :param tags: the :class:`sphinx.util.tags.Tags` object
     """
     # Match all ``only`` directives
     pattern = r"\.\. only::\s+(\S.*?)\n+?((?:^[ ]+.+?$|^\s*$)+?)(?=\n*\S+|\Z)"
     directives = re.findall(pattern, rst, re.M | re.DOTALL)
 
     for expression, content in directives:
         # Pattern to match each block exactly
         pattern = rf"\.\. only:: {expression}\n+?{escape_rst(content)}\n*?"
 
-        if 'readme' in expression:
+        if tags.eval_condition(expression):
             # For replacement, remove preceding indent (3 spaces) from each line
             content = '\n'.join(line[3:] for line in content.split('\n'))
 
             # Replace directive with content
             rst = re.sub(pattern, rf"{content}", rst)
 
         else:
```

### Comparing `sphinx-readme-0.1.0/sphinx_readme/utils/sphinx.py` & `sphinx-readme-0.2.0/sphinx_readme/utils/sphinx.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.1.0/sphinx_readme.egg-info/PKG-INFO` & `sphinx-readme-0.2.0/sphinx_readme.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sphinx-readme
-Version: 0.1.0
+Version: 0.2.0
 Summary: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 Home-page: https://github.com/tdkorn/sphinx-readme
 Author: Adam Korn
 Author-email: hello@dailykitten.net
 License: MIT License
 Download-URL: https://github.com/TDKorn/sphinx-readme/tarball/main
 Keywords: sphinx,docutils,sphinx-extension,sphinx-contrib,reStructuredText,rst,reST,parser,rst-parser,README.rst,README,autodoc,linkcode
@@ -12,65 +12,64 @@
 Classifier: Framework :: Sphinx :: Extension
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Description-Content-Type: text/x-rst; charset=UTF-8
 License-File: LICENSE
 
-.. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
-.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.1.0/sphinx_readme/parser.py#L208-L232
-.. |.`sphinx.ext.linkcode`| replace:: ``sphinx.ext.linkcode``
-.. _.`sphinx.ext.linkcode`: https://www.sphinx-doc.org/en/master/usage/extensions/linkcode.html#module-sphinx.ext.linkcode
-.. |.`~.sphinx.ext.autodoc`| replace:: ``autodoc``
-.. _.`~.sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
-.. |.`sphinx.ext.autodoc`| replace:: ``sphinx.ext.autodoc``
-.. _.`sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
-.. |attention| replace:: 🔔️
-.. |caution| replace:: ⚠️
-.. |danger| replace:: ☢️
-.. |error| replace:: ⛔
-.. |hint| replace:: 🧠
-.. |important| replace:: 📢
-.. |note| replace:: 📝
-.. |tip| replace:: 💡
-.. |warning| replace:: 🚩
-.. |default| replace:: 📄
-.. |about| replace:: 📚
-
-.. |html_context| replace:: ``html_context``
-.. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
 .. |html_baseurl| replace:: ``html_baseurl``
 .. _html_baseurl: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_baseurl
-.. |readme_src_files| replace:: ``readme_src_files``
-.. _readme_src_files: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_src_files
+.. |html_context| replace:: ``html_context``
+.. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
+.. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
+.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.0/sphinx_readme/parser.py#L213-L237
 .. |readme_docs_url_type| replace:: ``readme_docs_url_type``
 .. _readme_docs_url_type: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_docs_url_type
-.. |readme_replace_attrs| replace:: ``readme_replace_attrs``
-.. _readme_replace_attrs: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_replace_attrs
 .. |readme_inline_markup| replace:: ``readme_inline_markup``
 .. _readme_inline_markup: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_inline_markup
 .. |readme_raw_directive| replace:: ``readme_raw_directive``
 .. _readme_raw_directive: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_raw_directive
+.. |readme_replace_attrs| replace:: ``readme_replace_attrs``
+.. _readme_replace_attrs: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_replace_attrs
+.. |readme_src_files| replace:: ``readme_src_files``
+.. _readme_src_files: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_src_files
+.. |.`sphinx.ext.autodoc`| replace:: ``sphinx.ext.autodoc``
+.. _.`sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
+.. |.`~.sphinx.ext.autodoc`| replace:: ``autodoc``
+.. _.`~.sphinx.ext.autodoc`: https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc
+.. |.`sphinx.ext.linkcode`| replace:: ``sphinx.ext.linkcode``
+.. _.`sphinx.ext.linkcode`: https://www.sphinx-doc.org/en/master/usage/extensions/linkcode.html#module-sphinx.ext.linkcode
 
 .. meta::
    :author: Adam Korn
    :title: Sphinx README
    :description: Sphinx Extension to Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
 Sphinx README - Generate Beautiful ``README.rst`` for GitHub, PyPi, GitLab, BitBucket
 --------------------------------------------------------------------------------------
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.1.0/docs/source/_static/logo_transparent.png
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/logo_transparent.png
    :alt: Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
    :align: center
    :width: 25%
 
-A Sphinx extension to generate ``README.rst`` files that render beautifully on GitHub, PyPi, GitLab, BitBucket
 
 
+
+
+
+
+
+
+
+
+
+
+A Sphinx extension to generate ``README.rst`` files that render beautifully on GitHub, PyPi, GitLab, BitBucket
+
 .. |RTD| replace:: **Explore the docs »**
 .. _RTD: https://sphinx-readme.readthedocs.io/en/latest/
 
 |RTD|_
 
 |
 
@@ -86,37 +85,40 @@
    :target: https://pepy.tech/project/sphinx-readme
    :alt: Downloads for Sphinx README
 
 .. image:: https://readthedocs.org/projects/sphinx-readme/badge/?version=latest
    :target: https://sphinx-readme.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation for Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
+
+
+
 |
 
 About Sphinx README
 ~~~~~~~~~~~~~~~~~~~~~~~
 
 
 .. csv-table::
-   :header: |about| What's Sphinx README?
+   :header: 📚 What's Sphinx README?
 
    "``sphinx_readme`` is a ``reStructuredText`` parser that uses Sphinx
    to generate ``rst`` files that render beautifully on
    GitHub, PyPi, GitLab, and BitBucket."
 
 
 
 **With** ``sphinx_readme`` **, there's no need to rewrite your** ``README.rst`` **as a** ``README.md`` **file**
 
 Files generated by ``sphinx_readme`` have nearly identical appearance and functionality
 as ``html`` builds, including |.`sphinx.ext.autodoc`|_ cross-references!
 
 |
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.1.0/docs/source/_static/demo/demo.gif
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/demo/demo.gif
    :alt: Demonstration of how reStructuredText README.rst files generated by Sphinx README render on GitHub, PyPi, GitLab, BitBucket
    :width: 75%
 
 
 📋 Features
 ~~~~~~~~~~~~
 
@@ -190,15 +192,15 @@
 |readme_src_files|_
  An individual or list of ``rst`` files to parse
 
   Type: ``Union[str, List]``
 
 
 .. csv-table::
-   :header: |important| Important
+   :header: 📢 Important
 
    "Filepaths should be specified relative to the source directory"
 
 
 |
 
 |readme_docs_url_type|_
@@ -215,15 +217,15 @@
 
  * ``"html"``: replaces references with links to HTML documentation entries
 
    **Example**: |parse_intersphinx_nodes_html|_
 
 
 .. csv-table::
-   :header: |note| Note
+   :header: 📝 Note
 
    "If set to ``code``, then :code:`:attr:` cross-references will not be replaced with links
 
    * Instead, they'll be replaced with ``inline literals`` or left as is
    * Please see |readme_replace_attrs|_ and |readme_inline_markup|_"
 
 
@@ -253,15 +255,15 @@
 
    readme_docs_url_type = "code"
 
 
 
 
 .. csv-table::
-   :header: |important| Important
+   :header: 📢 Important
 
    "For platforms that don't support the ``raw`` directive (PyPi, GitLab, and BitBucket),
    be sure to disable |readme_raw_directive|_:
 
    .. code-block:: python
 
       readme_raw_directive = False"
```

