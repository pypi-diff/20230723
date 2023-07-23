# Comparing `tmp/sphinx-readme-0.2.0.tar.gz` & `tmp/sphinx-readme-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sphinx-readme-0.2.0.tar", last modified: Sun Jul 23 12:36:53 2023, max compression
+gzip compressed data, was "sphinx-readme-0.2.1.tar", last modified: Sun Jul 23 20:18:05 2023, max compression
```

## Comparing `sphinx-readme-0.2.0.tar` & `sphinx-readme-0.2.1.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 12:36:53.188485 sphinx-readme-0.2.0/
--rw-rw-rw-   0        0        0     1084 2023-05-09 12:07:43.000000 sphinx-readme-0.2.0/LICENSE
--rw-rw-rw-   0        0        0     9427 2023-07-23 12:36:53.187487 sphinx-readme-0.2.0/PKG-INFO
--rw-rw-rw-   0        0        0     8638 2023-07-23 12:35:55.000000 sphinx-readme-0.2.0/README.rst
--rw-rw-rw-   0        0        0       42 2023-07-23 12:36:53.189529 sphinx-readme-0.2.0/setup.cfg
--rw-rw-rw-   0        0        0     1454 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 12:36:53.157273 sphinx-readme-0.2.0/sphinx_readme/
--rw-rw-rw-   0        0        0     1768 2023-07-23 12:31:35.000000 sphinx-readme-0.2.0/sphinx_readme/__init__.py
--rw-rw-rw-   0        0        0    12014 2023-07-23 12:17:16.000000 sphinx-readme-0.2.0/sphinx_readme/config.py
--rw-rw-rw-   0        0        0    24708 2023-07-23 10:33:01.000000 sphinx-readme-0.2.0/sphinx_readme/parser.py
-drwxrwxrwx   0        0        0        0 2023-07-23 12:36:53.185493 sphinx-readme-0.2.0/sphinx_readme/utils/
--rw-rw-rw-   0        0        0        0 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/__init__.py
--rw-rw-rw-   0        0        0      603 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/docutils.py
--rw-rw-rw-   0        0        0     4643 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/git.py
--rw-rw-rw-   0        0        0     3727 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/linkcode.py
--rw-rw-rw-   0        0        0     7578 2023-07-23 12:19:01.000000 sphinx-readme-0.2.0/sphinx_readme/utils/rst.py
--rw-rw-rw-   0        0        0      810 2023-07-23 04:58:42.000000 sphinx-readme-0.2.0/sphinx_readme/utils/sphinx.py
-drwxrwxrwx   0        0        0        0 2023-07-23 12:36:53.178460 sphinx-readme-0.2.0/sphinx_readme.egg-info/
--rw-rw-rw-   0        0        0     9427 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      465 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       12 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/requires.txt
--rw-rw-rw-   0        0        0       14 2023-07-23 12:36:53.000000 sphinx-readme-0.2.0/sphinx_readme.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 20:18:05.523091 sphinx-readme-0.2.1/
+-rw-rw-rw-   0        0        0     1084 2023-05-09 12:07:43.000000 sphinx-readme-0.2.1/LICENSE
+-rw-rw-rw-   0        0        0     9427 2023-07-23 20:18:05.523091 sphinx-readme-0.2.1/PKG-INFO
+-rw-rw-rw-   0        0        0     8638 2023-07-23 20:17:32.000000 sphinx-readme-0.2.1/README.rst
+-rw-rw-rw-   0        0        0       42 2023-07-23 20:18:05.523091 sphinx-readme-0.2.1/setup.cfg
+-rw-rw-rw-   0        0        0     1454 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:18:05.507501 sphinx-readme-0.2.1/sphinx_readme/
+-rw-rw-rw-   0        0        0     1768 2023-07-23 20:14:04.000000 sphinx-readme-0.2.1/sphinx_readme/__init__.py
+-rw-rw-rw-   0        0        0    12014 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/sphinx_readme/config.py
+-rw-rw-rw-   0        0        0    24826 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/sphinx_readme/parser.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:18:05.523091 sphinx-readme-0.2.1/sphinx_readme/utils/
+-rw-rw-rw-   0        0        0        0 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/sphinx_readme/utils/__init__.py
+-rw-rw-rw-   0        0        0      603 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/sphinx_readme/utils/docutils.py
+-rw-rw-rw-   0        0        0     4643 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/sphinx_readme/utils/git.py
+-rw-rw-rw-   0        0        0     3727 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/sphinx_readme/utils/linkcode.py
+-rw-rw-rw-   0        0        0     7578 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/sphinx_readme/utils/rst.py
+-rw-rw-rw-   0        0        0      810 2023-07-23 19:42:27.000000 sphinx-readme-0.2.1/sphinx_readme/utils/sphinx.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:18:05.507501 sphinx-readme-0.2.1/sphinx_readme.egg-info/
+-rw-rw-rw-   0        0        0     9427 2023-07-23 20:18:05.000000 sphinx-readme-0.2.1/sphinx_readme.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      465 2023-07-23 20:18:05.000000 sphinx-readme-0.2.1/sphinx_readme.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 20:18:05.000000 sphinx-readme-0.2.1/sphinx_readme.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 20:18:05.000000 sphinx-readme-0.2.1/sphinx_readme.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-07-23 20:18:05.000000 sphinx-readme-0.2.1/sphinx_readme.egg-info/top_level.txt
```

### Comparing `sphinx-readme-0.2.0/LICENSE` & `sphinx-readme-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.2.0/PKG-INFO` & `sphinx-readme-0.2.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sphinx-readme
-Version: 0.2.0
+Version: 0.2.1
 Summary: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 Home-page: https://github.com/tdkorn/sphinx-readme
 Author: Adam Korn
 Author-email: hello@dailykitten.net
 License: MIT License
 Download-URL: https://github.com/TDKorn/sphinx-readme/tarball/main
 Keywords: sphinx,docutils,sphinx-extension,sphinx-contrib,reStructuredText,rst,reST,parser,rst-parser,README.rst,README,autodoc,linkcode
@@ -17,15 +17,15 @@
 License-File: LICENSE
 
 .. |html_baseurl| replace:: ``html_baseurl``
 .. _html_baseurl: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_baseurl
 .. |html_context| replace:: ``html_context``
 .. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
 .. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
-.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.0/sphinx_readme/parser.py#L213-L237
+.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.1/sphinx_readme/parser.py#L213-L237
 .. |readme_docs_url_type| replace:: ``readme_docs_url_type``
 .. _readme_docs_url_type: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_docs_url_type
 .. |readme_inline_markup| replace:: ``readme_inline_markup``
 .. _readme_inline_markup: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_inline_markup
 .. |readme_raw_directive| replace:: ``readme_raw_directive``
 .. _readme_raw_directive: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_raw_directive
 .. |readme_replace_attrs| replace:: ``readme_replace_attrs``
@@ -43,15 +43,15 @@
    :author: Adam Korn
    :title: Sphinx README
    :description: Sphinx Extension to Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
 Sphinx README - Generate Beautiful ``README.rst`` for GitHub, PyPi, GitLab, BitBucket
 --------------------------------------------------------------------------------------
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/logo_transparent.png
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.1/docs/source/_static/logo_transparent.png
    :alt: Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
    :align: center
    :width: 25%
 
 
 
 
@@ -110,15 +110,15 @@
 **With** ``sphinx_readme`` **, there's no need to rewrite your** ``README.rst`` **as a** ``README.md`` **file**
 
 Files generated by ``sphinx_readme`` have nearly identical appearance and functionality
 as ``html`` builds, including |.`sphinx.ext.autodoc`|_ cross-references!
 
 |
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/demo/demo.gif
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.1/docs/source/_static/demo/demo.gif
    :alt: Demonstration of how reStructuredText README.rst files generated by Sphinx README render on GitHub, PyPi, GitLab, BitBucket
    :width: 75%
 
 
 📋 Features
 ~~~~~~~~~~~~
```

### Comparing `sphinx-readme-0.2.0/README.rst` & `sphinx-readme-0.2.1/README.rst`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 .. |html_baseurl| replace:: ``html_baseurl``
 .. _html_baseurl: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_baseurl
 .. |html_context| replace:: ``html_context``
 .. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
 .. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
-.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.0/sphinx_readme/parser.py#L213-L237
+.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.1/sphinx_readme/parser.py#L213-L237
 .. |readme_docs_url_type| replace:: ``readme_docs_url_type``
 .. _readme_docs_url_type: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_docs_url_type
 .. |readme_inline_markup| replace:: ``readme_inline_markup``
 .. _readme_inline_markup: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_inline_markup
 .. |readme_raw_directive| replace:: ``readme_raw_directive``
 .. _readme_raw_directive: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_raw_directive
 .. |readme_replace_attrs| replace:: ``readme_replace_attrs``
@@ -25,15 +25,15 @@
    :author: Adam Korn
    :title: Sphinx README
    :description: Sphinx Extension to Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
 Sphinx README - Generate Beautiful ``README.rst`` for GitHub, PyPi, GitLab, BitBucket
 --------------------------------------------------------------------------------------
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/logo_transparent.png
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.1/docs/source/_static/logo_transparent.png
    :alt: Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
    :align: center
    :width: 25%
 
 
 
 
@@ -92,15 +92,15 @@
 **With** ``sphinx_readme`` **, there's no need to rewrite your** ``README.rst`` **as a** ``README.md`` **file**
 
 Files generated by ``sphinx_readme`` have nearly identical appearance and functionality
 as ``html`` builds, including |.`sphinx.ext.autodoc`|_ cross-references!
 
 |
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/demo/demo.gif
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.1/docs/source/_static/demo/demo.gif
    :alt: Demonstration of how reStructuredText README.rst files generated by Sphinx README render on GitHub, PyPi, GitLab, BitBucket
    :width: 75%
 
 
 📋 Features
 ~~~~~~~~~~~~
```

### Comparing `sphinx-readme-0.2.0/setup.py` & `sphinx-readme-0.2.1/setup.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.2.0/sphinx_readme/__init__.py` & `sphinx-readme-0.2.1/sphinx_readme/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 from sphinx.environment import BuildEnvironment
 
 from sphinx_readme.utils.sphinx import get_conf_val, set_conf_val
 from sphinx_readme.utils.git import get_repo_dir
 from sphinx_readme.parser import READMEParser
 
 
-__version__ = "v0.2.0"
+__version__ = "v0.2.1"
 
 
 def setup(app: Sphinx) -> Dict[str, Any]:
     # Avoid setting up extension if building on ReadTheDocs
     if os.environ.get("READTHEDOCS") == "True":
         return {}
```

### Comparing `sphinx-readme-0.2.0/sphinx_readme/config.py` & `sphinx-readme-0.2.1/sphinx_readme/config.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.2.0/sphinx_readme/parser.py` & `sphinx-readme-0.2.1/sphinx_readme/parser.py`

 * *Files 1% similar despite different names*

```diff
@@ -467,14 +467,17 @@
         for xref in xrefs:
             if not all(xref):  # :ref_role:`ref_id` ->  ('ref_id', 'ref_id', '')
                 ref, ref_id, title = xref
 
             else:  # :ref_role:`title <ref_id>` -> ('title <ref_id>', 'title', 'ref_id')
                 ref, title, ref_id = xref
 
+            # Normalize ref_id to ensure match in ref_map
+            ref_id = nodes.fully_normalize_name(ref_id)
+
             # Match these ids up with target data in the ref_map
             if info := self.ref_map.get(ref_role, {}).get(ref_id, {}):
                 # Replace cross-refs with `text <link>`_ or substitutions
                 link, subs = format_hyperlink(
                     target=info['target'],
                     text=title or info['replace']
                 )
```

### Comparing `sphinx-readme-0.2.0/sphinx_readme/utils/docutils.py` & `sphinx-readme-0.2.1/sphinx_readme/utils/docutils.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.2.0/sphinx_readme/utils/git.py` & `sphinx-readme-0.2.1/sphinx_readme/utils/git.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.2.0/sphinx_readme/utils/linkcode.py` & `sphinx-readme-0.2.1/sphinx_readme/utils/linkcode.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.2.0/sphinx_readme/utils/rst.py` & `sphinx-readme-0.2.1/sphinx_readme/utils/rst.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.2.0/sphinx_readme/utils/sphinx.py` & `sphinx-readme-0.2.1/sphinx_readme/utils/sphinx.py`

 * *Files identical despite different names*

### Comparing `sphinx-readme-0.2.0/sphinx_readme.egg-info/PKG-INFO` & `sphinx-readme-0.2.1/sphinx_readme.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sphinx-readme
-Version: 0.2.0
+Version: 0.2.1
 Summary: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 Home-page: https://github.com/tdkorn/sphinx-readme
 Author: Adam Korn
 Author-email: hello@dailykitten.net
 License: MIT License
 Download-URL: https://github.com/TDKorn/sphinx-readme/tarball/main
 Keywords: sphinx,docutils,sphinx-extension,sphinx-contrib,reStructuredText,rst,reST,parser,rst-parser,README.rst,README,autodoc,linkcode
@@ -17,15 +17,15 @@
 License-File: LICENSE
 
 .. |html_baseurl| replace:: ``html_baseurl``
 .. _html_baseurl: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_baseurl
 .. |html_context| replace:: ``html_context``
 .. _html_context: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-html_context
 .. |.`~.parse_intersphinx_nodes`| replace:: ``parse_intersphinx_nodes()``
-.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.0/sphinx_readme/parser.py#L213-L237
+.. _.`~.parse_intersphinx_nodes`: https://github.com/TDKorn/sphinx-readme/blob/v0.2.1/sphinx_readme/parser.py#L213-L237
 .. |readme_docs_url_type| replace:: ``readme_docs_url_type``
 .. _readme_docs_url_type: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_docs_url_type
 .. |readme_inline_markup| replace:: ``readme_inline_markup``
 .. _readme_inline_markup: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_inline_markup
 .. |readme_raw_directive| replace:: ``readme_raw_directive``
 .. _readme_raw_directive: https://sphinx-readme.readthedocs.io/en/latest/configuration/configuring.html#confval-readme_raw_directive
 .. |readme_replace_attrs| replace:: ``readme_replace_attrs``
@@ -43,15 +43,15 @@
    :author: Adam Korn
    :title: Sphinx README
    :description: Sphinx Extension to Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
 
 Sphinx README - Generate Beautiful ``README.rst`` for GitHub, PyPi, GitLab, BitBucket
 --------------------------------------------------------------------------------------
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/logo_transparent.png
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.1/docs/source/_static/logo_transparent.png
    :alt: Sphinx README: Generate Beautiful reStructuredText README.rst for GitHub, PyPi, GitLab, BitBucket
    :align: center
    :width: 25%
 
 
 
 
@@ -110,15 +110,15 @@
 **With** ``sphinx_readme`` **, there's no need to rewrite your** ``README.rst`` **as a** ``README.md`` **file**
 
 Files generated by ``sphinx_readme`` have nearly identical appearance and functionality
 as ``html`` builds, including |.`sphinx.ext.autodoc`|_ cross-references!
 
 |
 
-.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.0/docs/source/_static/demo/demo.gif
+.. image:: https://raw.githubusercontent.com/TDKorn/sphinx-readme/v0.2.1/docs/source/_static/demo/demo.gif
    :alt: Demonstration of how reStructuredText README.rst files generated by Sphinx README render on GitHub, PyPi, GitLab, BitBucket
    :width: 75%
 
 
 📋 Features
 ~~~~~~~~~~~~
```

