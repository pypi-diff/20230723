# Comparing `tmp/rico-0.3.2.tar.gz` & `tmp/rico-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rico-0.3.2.tar", last modified: Wed Jul 12 16:55:22 2023, max compression
+gzip compressed data, was "rico-0.4.0.tar", last modified: Sun Jul 23 11:28:12 2023, max compression
```

## Comparing `rico-0.3.2.tar` & `rico-0.4.0.tar`

### file list

```diff
@@ -1,16 +1,17 @@
--rw-r--r--   0        0        0     1070 2023-07-12 16:54:47.825177 rico-0.3.2/LICENSE
--rw-r--r--   0        0        0    16832 2023-07-12 16:54:47.825177 rico-0.3.2/README.md
--rw-r--r--   0        0        0     2993 2023-07-12 16:55:22.505268 rico-0.3.2/pyproject.toml
--rw-r--r--   0        0        0      710 2023-07-12 16:54:47.829177 rico-0.3.2/src/rico/__init__.py
--rw-r--r--   0        0        0     7139 2023-07-12 16:54:47.829177 rico-0.3.2/src/rico/_config.py
--rw-r--r--   0        0        0     5280 2023-07-12 16:54:47.829177 rico-0.3.2/src/rico/_container.py
--rw-r--r--   0        0        0    16695 2023-07-12 16:54:47.829177 rico-0.3.2/src/rico/_content.py
--rw-r--r--   0        0        0     7951 2023-07-12 16:54:47.829177 rico-0.3.2/src/rico/_html.py
--rw-r--r--   0        0        0      340 2023-07-12 16:54:47.829177 rico-0.3.2/src/rico/_version.py
--rw-r--r--   0        0        0       18 2023-07-12 16:54:47.829177 rico-0.3.2/tests/__init__.py
--rw-r--r--   0        0        0     2803 2023-07-12 16:54:47.829177 rico-0.3.2/tests/test__config.py
--rw-r--r--   0        0        0    10222 2023-07-12 16:54:47.829177 rico-0.3.2/tests/test__container.py
--rw-r--r--   0        0        0    25722 2023-07-12 16:54:47.829177 rico-0.3.2/tests/test__content.py
--rw-r--r--   0        0        0    10803 2023-07-12 16:54:47.829177 rico-0.3.2/tests/test__html.py
--rw-r--r--   0        0        0      730 2023-07-12 16:54:47.829177 rico-0.3.2/tests/test__version.py
--rw-r--r--   0        0        0    18488 1970-01-01 00:00:00.000000 rico-0.3.2/PKG-INFO
+-rw-r--r--   0        0        0     1070 2023-07-23 11:27:43.930951 rico-0.4.0/LICENSE
+-rw-r--r--   0        0        0    18077 2023-07-23 11:27:43.934951 rico-0.4.0/README.md
+-rw-r--r--   0        0        0     2840 2023-07-23 11:28:12.191261 rico-0.4.0/pyproject.toml
+-rw-r--r--   0        0        0      699 2023-07-23 11:27:43.938951 rico-0.4.0/src/rico/__init__.py
+-rw-r--r--   0        0        0     7098 2023-07-23 11:27:43.938951 rico-0.4.0/src/rico/_config.py
+-rw-r--r--   0        0        0     5202 2023-07-23 11:27:43.938951 rico-0.4.0/src/rico/_container.py
+-rw-r--r--   0        0        0    15437 2023-07-23 11:27:43.938951 rico-0.4.0/src/rico/_content.py
+-rw-r--r--   0        0        0     7951 2023-07-23 11:27:43.942951 rico-0.4.0/src/rico/_html.py
+-rw-r--r--   0        0        0      340 2023-07-23 11:27:43.942951 rico-0.4.0/src/rico/_version.py
+-rw-r--r--   0        0        0        6 2023-07-23 11:28:12.191261 rico-0.4.0/src/rico/_version.txt
+-rw-r--r--   0        0        0       18 2023-07-23 11:27:43.942951 rico-0.4.0/tests/__init__.py
+-rw-r--r--   0        0        0     2803 2023-07-23 11:27:43.942951 rico-0.4.0/tests/test__config.py
+-rw-r--r--   0        0        0    10356 2023-07-23 11:27:43.942951 rico-0.4.0/tests/test__container.py
+-rw-r--r--   0        0        0    24589 2023-07-23 11:27:43.942951 rico-0.4.0/tests/test__content.py
+-rw-r--r--   0        0        0    10829 2023-07-23 11:27:43.942951 rico-0.4.0/tests/test__html.py
+-rw-r--r--   0        0        0      730 2023-07-23 11:27:43.942951 rico-0.4.0/tests/test__version.py
+-rw-r--r--   0        0        0    19288 1970-01-01 00:00:00.000000 rico-0.4.0/PKG-INFO
```

### Comparing `rico-0.3.2/LICENSE` & `rico-0.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `rico-0.3.2/README.md` & `rico-0.4.0/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -24,61 +24,71 @@
 
 ```bash
 pip install rico
 ```
 
 **rico** has no dependencies other than the standard Python packages.
 
+For Markdown support:
+* install [markdown-it-py](https://github.com/executablebooks/markdown-it-py),
+* or install [Python Markdown](https://github.com/Python-Markdown/),
+* or set your own Markdown renderer using `rico.set_config`.
+
 ### Deprecated
 
 Optional additional dependencies were required to support the following content types:
 * Plots (`rico[altair]`, `rico[pyplot]`, `rico[seaborn]`).
 * Markdown (`rico[markdown]`).
 
 The `rico[complete]` extra incudes all the dependencies above.
 
 They are no longer needed and will be removed in version 0.4.0.
 
 ## User guide
 
+To get started with **rico**, take a look at the self-explanatory [examples](https://github.com/e10v/rico/tree/main/examples) with resulting HTML documents. The user guide contains a slightly more detailed explanation.
+
 ### Basic usage
 
 **rico** provides both declarative and imperative style interfaces.
 
 Declarative style:
 ```python
 import pandas as pd
 import rico
 
-df = pd.DataFrame({
-    "a": list("CCCDDDEEE"),
-    "b": [2, 7, 4, 1, 2, 6, 8, 4, 7],
-})
-plot = df.plot.scatter(x="a", y="b")
+df = pd.DataFrame(
+    {
+        "x": [2, 7, 4, 1, 2, 6, 8, 4, 7],
+        "y": [1, 9, 2, 8, 3, 7, 4, 6, 5],
+    },
+    index=pd.Index(list("AAABBBCCC")),
+)
+plot = df.plot.scatter(x="x", y="y")
 
-doc = rico.Doc("Hello world!", df, plot, title="My doc")
+doc = rico.Doc("Hello, World!", df, plot, title="My doc")
 ```
 
 Imperative style:
 ```python
 doc = rico.Doc(title="My doc")
-doc.append("Hello world!", df, plot)
+doc.append("Hello, World!", df, plot)
 ```
 
 Also imperative style:
 ```python
 doc = rico.Doc(title="My doc")
-doc.append("Hello world!")
+doc.append("Hello, World!")
 doc.append(df)
 doc.append(plot)
 ```
 
 Mix-and-match:
 ```python
-doc = rico.Doc("Hello world!", df, title="My doc")
+doc = rico.Doc("Hello, World!", df, title="My doc")
 doc.append(plot)
 ```
 
 ### Serialization
 
 Serialize the document to HTML using `str(doc)`:
 ```python
@@ -128,33 +138,33 @@
 * Matplotlib Pyplot Plots.
 * Dataframes and other types with [IPython rich representation methods](https://ipython.readthedocs.io/en/stable/config/integrating.html).
 * Text.
 
 Use specific classes for plots and texts to change the default behavior:
 ```python
 doc = rico.Doc(
-    rico.Text("Hello world!", mono=True),  # The default value is False.
+    rico.Text("Hello, World!", mono=True),  # The default value is False.
     df,
-    rico.Plot(plot, format="png"),  # The default value is "svg".
+    rico.Plot(plot, format="png", bbox_inches="tight"),  # The default value is "svg".
     title="My doc",
 )
 ```
 
 The following code gives the same result as the code above:
 ```python
 doc = rico.Doc(title="My doc")
-doc.append_text("Hello world!", mono=True)
+doc.append_text("Hello, World!", mono=True)
 doc.append(df)
-doc.append_plot(plot, format="png")
+doc.append_plot(plot, format="png", bbox_inches="tight")
 ```
 
 Some options can be set in the global configuration:
 ```python
 with rico.config_context(text_mono=True, image_format="png"):
-    doc = rico.Doc("Hello world!", df, plot, title="My doc")
+    doc = rico.Doc("Hello, World!", df, plot, title="My doc")
 ```
 
 Use specific classes and methods for other content types:
 * Images: `Image` or `Doc.append_image`.
 * Code: `Code` or `Doc.append_code`.
 * Markdown*: `Markdown` or `Doc.append_markdown`.
 * HTML tag: `Tag` or `Doc.append_tag`.
@@ -166,69 +176,69 @@
 ```python
 doc = rico.Doc(
     rico.Markdown("## Dataframe"),
     df,
     rico.Tag("h2", "Plot"),  # An alternative way to add a header.
     plot,
     rico.HTML("<h2>Code</h2>"),  # Another way to add a header.
-    rico.Code("print('Hello world!')"),
+    rico.Code("print('Hello, World!')"),
     title="My doc",
 )
 ```
 
 The following code gives the same result as the code above:
 ```python
 doc = rico.Doc(title="My doc")
 doc.append_markdown("## Dataframe")
 doc.append(df)
 doc.append_tag("h2", "Plot")
 doc.append(plot)
 doc.append_html("<h2>Code</h2>")
-doc.append_code("print('Hello world!')")
+doc.append_code("print('Hello, World!')")
 ```
 
 Check the docstrings for details.
 
 Serialize content to HTML using `str(object)` or `object.serialize()`:
 ```python
-obj = rico.Tag("p", "Hello world!")
+obj = rico.Tag("p", "Hello, World!")
 
 print(obj)
-# <div><p>Hello world!</p></div>
+# <div><p>Hello, World!</p></div>
 
 print(obj.serialize(indent=True, space="    "))
 # <div>
-#     <p>Hello world!</p>
+#     <p>Hello, World!</p>
 # </div>
 ```
 
 ### Bootstrap, HTML classes and document layout
 
 By default, [Bootstrap](https://getbootstrap.com/) styles are included in the document. Change the default behavior using the `bootstrap` parameter:
 ```python
-doc = rico.Doc("Hello world!", bootstrap="full")
+doc = rico.Doc("Hello, World!", bootstrap="full")
 ```
 
 * Set `bootstrap` to `"css"` (default) to include only CSS.
 * Set `bootstrap` to `"full"` to include both the CSS and JS.
 * Set `bootstrap` to `"none"` to not include Bootstrap*.
 
 *Keep in mind that **rico** relies on Bootstrap classes and styles. For example:
 * The `mono` and `wrap` parameters of the `Text` class use Bootstrap's `font-monospace` and `font-monospace` classes.
 * **rico**'s dataframe style definition uses Bootstrap variables.
 
 Each content element is wrapped in a `<div>` container. Specify the element's container class using the `class_` parameter:
 ```python
-print(rico.Tag("p", "Hello world!", class_="col"))
-# <div class="col"><p>Hello world!</p></div>
+print(rico.Tag("p", "Hello, World!", class_="col"))
+# <div class="col"><p>Hello, World!</p></div>
 ```
 
 All elements' containers in the document are also wrapped in a `<div>` container. Specify the document's container class using the `class_` parameter:
 ```python
-doc = rico.Doc("Hello world!", class_="container-fluid")
+doc = rico.Doc("Hello, World!", class_="container-fluid")
 ```
 
 Define the document layout using Bootstrap and `Div` class:
 ```python
 doc = rico.Doc(rico.Div(
     rico.Obj(df, class_="col"),
     rico.Obj(plot, class_="col"),
@@ -236,49 +246,67 @@
 ))
 ```
 
 The code above creates a document with two columns, one with a dataframe and another with a plot. The `Obj` is a magic class which automatically determines the content type in the same way that `Doc` and `Doc.append` do.
 
 Another example:
 ```python
+import altair as alt
+
 doc = rico.Doc(
-    rico.Tag("h1", "My doc"),
-    rico.Tag("h2", "Description"),
-    "This is an example of custom document layout using Bootstrap classes.",
-    rico.Tag("h2", "Data"),
+    rico.Tag("h2", "Dataframes"),
     rico.Div(
-        rico.Obj("Dataframe", df, class_="col"),
-        rico.Obj("Plot", plot, class_="col"),
+        rico.Obj(rico.Tag("h3", "A"), df.loc["A", :], class_="col"),
+        rico.Obj(rico.Tag("h3", "B"), df.loc["B", :], class_="col"),
+        rico.Obj(rico.Tag("h3", "C"), df.loc["C", :], class_="col"),
         class_="row row-cols-auto",
     ),
-    title="My doc",
+    rico.Tag("h2", "Plots"),
+    rico.Div(
+        rico.Obj(
+            rico.Tag("h3", "A"),
+            alt.Chart(df.loc["A", :]).mark_point().encode(x="x", y="y"),
+            class_="col",
+        ),
+        rico.Obj(
+            rico.Tag("h3", "B"),
+            alt.Chart(df.loc["B", :]).mark_point().encode(x="x", y="y"),
+            class_="col",
+        ),
+        rico.Obj(
+            rico.Tag("h3", "C"),
+            alt.Chart(df.loc["C", :]).mark_point().encode(x="x", y="y"),
+            class_="col",
+        ),
+        class_="row row-cols-auto",
+    ),
+    title="Grid system",
 )
 ```
 
 The following code gives the same result as the code above:
 ```python
-doc = rico.Doc(title="My doc")
-doc.append_tag("h1", "My doc")
-doc.append_tag("h2", "Description")
-doc.append("This is an example of custom document layout using Bootstrap classes.")
-doc.append_tag("h2", "Data")
-div = rico.Div(class_="row row-cols-auto")
-doc.append(div)
-div.append("Dataframe", df, class_="col")
-div.append("Plot", plot, class_="col")
-```
+doc = rico.Doc(title="Grid system")
 
-Keep in mind that `obj.append(x, y)` works differently than
-```python
-obj.append(x)
-obj.append(y)
+doc.append_tag("h2", "Dataframes")
+div1 = rico.Div(class_="row row-cols-auto")
+doc.append(div1)
+for name, data in df.groupby(df.index):
+    div1.append(rico.Tag("h3", name), data, class_="col")
+
+doc.append_tag("h2", "Plots")
+div2 = rico.Div(class_="row row-cols-auto")
+doc.append(div2)
+for name, data in df.groupby(df.index):
+    div2.append(
+        rico.Tag("h3", name),
+        alt.Chart(data).mark_point().encode(x="x", y="y"),
+        class_="col",
+    )
 ```
-The first one wraps both elements in a single `<div>` container. The second one creates a separate `<div>` container for each element.
-
-`Obj(x, y, class_="z")` wraps both `x` and `y` elements in a single `<div>` container with `class` attribute set to `"z"`.
 
 More on Bootstrap layout and grid system:
 * [Breakpoints](https://getbootstrap.com/docs/5.3/layout/breakpoints/)
 * [Containers](https://getbootstrap.com/docs/5.3/layout/containers/)
 * [Grid system](https://getbootstrap.com/docs/5.3/layout/grid/)
 * [Columns](https://getbootstrap.com/docs/5.3/layout/columns/)
 
@@ -299,65 +327,71 @@
 dark_theme = "https://cdn.jsdelivr.net/npm/bootswatch@5/dist/darkly/bootstrap.min.css"
 jquery = "https://cdn.jsdelivr.net/npm/jquery@3/dist/jquery.min.js"
 
 doc = rico.Doc(
     rico.Text("Click me", class_="click"),
     extra_styles=(
         rico.Style(src=dark_theme),
-        rico.Style(".click {color: red;}"),
+        rico.Style(".click {color: yellow;}"),
     ),
     extra_scripts=(
         rico.Script(src=jquery),
         rico.Script(
-            "$('p').on('click', function() {alert('Hello world!');})",
+            "$('p').on('click', function() {alert('Hello, World!');})",
             defer=True,
         ),
     ),
 )
 ```
 
 The `defer` parameter adds the `defer` attribute to the `<script>` tag if the `src` parameter is used. Otherwise, if the `text` parameter is used, the script is placed in the footer of the document.
 
 By default, external styles and scripts are included as file links. This means that these files must be available when someone opens the document. Include the contents of these files in the document using the `inline` parameter:
 ```python
 doc = rico.Doc(
     rico.Text("Click me", class_="click"),
     extra_styles=(
         rico.Style(src=dark_theme, inline=True),
-        rico.Style(".click {color: red;}"),
+        rico.Style(".click {color: yellow;}"),
     ),
     extra_scripts=(
         rico.Script(src=jquery, inline=True),
         rico.Script(
-            "$('p').on('click', function() {alert('Hello world!');})",
+            "$('p').on('click', function() {alert('Hello, World!');})",
             defer=True,
         ),
     ),
 )
 ```
 
 In the example above, the Bootstrap styles are still included as a link. Use the global options `inline_styles` and `inline_scripts` to include the contents of the style and script files in the document:
 ```python
 with rico.config_context(inline_styles=True, inline_scripts=True):
     doc = rico.Doc(
         rico.Text("Click me", class_="click"),
         extra_styles=(
             rico.Style(src=dark_theme),
-            rico.Style(".click {color: red;}"),
+            rico.Style(".click {color: yellow;}"),
         ),
         extra_scripts=(
             rico.Script(src=jquery),
             rico.Script(
-                "$('p').on('click', function() {alert('Hello world!');})",
+                "$('p').on('click', function() {alert('Hello, World!');})",
                 defer=True,
             ),
         ),
     )
 ```
 
+Keep in mind that style and script files can contain links to other external resources. **rico** doesn't parse or change them, even if the `inline` parameter or the `inline_styles` and `inline_scripts` global options are set to `True`. As a result:
+* These resurces should be availble when someone opens an HTML document created by **rico**.
+* Links with relative paths to external resources will not work.
+
+For example, [Bootstrap Icons CSS](https://cdn.jsdelivr.net/npm/bootstrap-icons@1/font/bootstrap-icons.css) contains linkes to fonts with relative paths: `url("./fonts/bootstrap-icons.woff2?1fa40e8900654d2863d011707b9fb6f2")`. Including this CSS file with the `inline` parameter set to `True` will make these links invalid.
+
 ### Global configuration
 
 Use global configuration to:
 * Get or set default parameter values.
 * Get or set document properties.
 * Get or set a markdown renderer method.
 
@@ -436,18 +470,12 @@
 ## Alternatives
 
 * Use [Jupyter Notebook](https://jupyter.org/) for interactive computing.
 * Use [nbconvert](https://nbconvert.readthedocs.io/) or [papermill](https://papermill.readthedocs.io/) if you're processing data and creating objects for a document in a Jupyter notebook.
 * Use [Quarto](https://quarto.org/) if you prefer R Markdown style notebooks and a variety of output formats.
 * Use [xml.etree.ElementTree](https://docs.python.org/3/library/xml.etree.elementtree.html), [lxml](https://lxml.de/), [Yattag](https://www.yattag.org/), or [Airium](https://gitlab.com/kamichal/airium) if you need low-level control.
 
-More on the topic:
-* "I Don’t Like Notebooks": [video](https://www.youtube.com/watch?v=7jiPeIFXb6U), [slides](https://docs.google.com/presentation/d/1n2RlMdmv1p25Xy5thJUhkKGvjtV-dkAIsUXP-AL4ffI/edit#slide=id.g362da58057_0_1).
-* [The First Notebook War](https://yihui.org/en/2018/09/notebook-war/).
-
 ## Roadmap
 
-* Support most of IPython rich representation [methods](https://ipython.readthedocs.io/en/stable/config/integrating.html#rich-display).
+* Support math equations with [MathJax](https://www.mathjax.org/) and/or [KaTeX](https://katex.org/).
+* Support PDF content.
 * Create docs with [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
-* Create short quick start.
-* Create examples with resulting HTML files.
-* Support math with [KaTeX](https://katex.org/).
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `rico-0.3.2/pyproject.toml` & `rico-0.4.0/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -20,41 +20,23 @@
     "Topic :: Scientific/Engineering",
     "Topic :: Scientific/Engineering :: Visualization",
     "Topic :: Text Processing",
     "Topic :: Text Processing :: Markup",
     "Topic :: Text Processing :: Markup :: HTML",
     "Topic :: Text Processing :: Markup :: Markdown",
 ]
-version = "0.3.2"
+version = "0.4.0"
 
 [project.license]
 text = "MIT"
 
 [project.urls]
 source = "https://github.com/e10v/rico"
 "release notes" = "https://github.com/e10v/rico/releases"
 
-[project.optional-dependencies]
-altair = [
-    "altair>=4.2",
-    "vl-convert-python>=0.8",
-]
-markdown = [
-    "markdown>=3.3",
-]
-pyplot = [
-    "matplotlib>=3.5",
-]
-seaborn = [
-    "seaborn>=0.12",
-]
-complete = [
-    "rico[altair,markdown,pyplot,seaborn]",
-]
-
 [build-system]
 requires = [
     "pdm-backend",
 ]
 build-backend = "pdm.backend"
 
 [tool.pdm.dev-dependencies]
@@ -63,14 +45,19 @@
     "pyright",
 ]
 test = [
     "pytest",
     "coverage[toml]",
     "markdown-it-py",
     "markdown",
+    "matplotlib",
+]
+examples = [
+    "pandas",
+    "altair",
 ]
 
 [tool.pdm.scripts]
 test = "coverage run -m pytest"
 lint = "ruff check ."
 type = "pyright"
 
@@ -140,25 +127,29 @@
     "ANN204",
     "ANN401",
     "B006",
     "N817",
     "PGH003",
     "PT001",
     "PT011",
+    "RUF015",
     "SLF001",
     "TRY003",
 ]
 
 [tool.ruff.per-file-ignores]
 "tests/*" = [
     "ANN201",
     "D100",
     "D103",
     "PLR2004",
 ]
+"examples/*" = [
+    "INP001",
+]
 
 [tool.ruff.isort]
 classes = [
     "HTML",
 ]
 force-sort-within-sections = true
 lines-after-imports = 2
```

### Comparing `rico-0.3.2/src/rico/__init__.py` & `rico-0.4.0/src/rico/__init__.py`

 * *Files 14% similar despite different names*

```diff
@@ -7,15 +7,14 @@
 It provides a high-level, easy-to-use API with reasonable defaults,
 as well as low-level access for better control.
 """
 
 from rico._config import config_context, get_config, set_config
 from rico._container import Div, Doc
 from rico._content import (
-    Chart,
     Code,
     ContentBase,
     HTML,
     Image,
     Markdown,
     Obj,
     Plot,
```

### Comparing `rico-0.3.2/src/rico/_config.py` & `rico-0.4.0/src/rico/_config.py`

 * *Files 2% similar despite different names*

```diff
@@ -20,17 +20,17 @@
     try:
         import markdown
         md_renderer = markdown.markdown
     except ImportError:
         md_renderer = None
 
 
-BOOTSTRAP_VER = "5"
-BOOTSTRAP_CSS= f"https://cdn.jsdelivr.net/npm/bootstrap@{BOOTSTRAP_VER}/dist/css/bootstrap.min.css"
-BOOTSTRAP_JS = f"https://cdn.jsdelivr.net/npm/bootstrap@{BOOTSTRAP_VER}/dist/js/bootstrap.min.js"
+BOOTSTRAP_BASE = "https://cdn.jsdelivr.net/npm/bootstrap@5/dist/"
+BOOTSTRAP_CSS = BOOTSTRAP_BASE + "css/bootstrap.min.css"
+BOOTSTRAP_JS = BOOTSTRAP_BASE + "js/bootstrap.min.js"
 
 DATAFRAME_STYLE = textwrap.dedent("""\
     .dataframe table {
         border: none;
         border-collapse: collapse;
         border-spacing: 0;
         margin-bottom: 1em;
```

### Comparing `rico-0.3.2/src/rico/_container.py` & `rico-0.4.0/src/rico/_container.py`

 * *Files 1% similar despite different names*

```diff
@@ -48,15 +48,14 @@
     append_tag = _append(rico._content.Tag, rico._content.Tag.__init__)
     append_text = _append(rico._content.Text, rico._content.Text.__init__)
     append_code = _append(rico._content.Code, rico._content.Code.__init__)
     append_html = _append(rico._content.HTML, rico._content.HTML.__init__)
     append_markdown = _append(rico._content.Markdown, rico._content.Markdown.__init__)
     append_image = _append(rico._content.Image, rico._content.Image.__init__)
     append_plot = _append(rico._content.Plot, rico._content.Plot.__init__)
-    append_chart = _append(rico._content.Chart, rico._content.Chart.__init__)
     append = _append(rico._content.Obj, rico._content.Obj.__init__)
 
 
 class Doc(Div):
     html: ET.Element
     head: ET.Element
     body: ET.Element
```

### Comparing `rico-0.3.2/src/rico/_content.py` & `rico-0.4.0/src/rico/_content.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,43 +3,31 @@
 
 from __future__ import annotations
 
 import base64
 import io
 from typing import TYPE_CHECKING
 import urllib.request
-import warnings
 import xml.etree.ElementTree as ET
 
 import rico._config
 import rico._html
 
 
 if TYPE_CHECKING:
     from typing import Any, Literal
 
     _ReprResult = str | bytes | dict[str, str | bytes]
 
 
 try:
-    import altair as alt
-    import vl_convert as vlc
-except ImportError:
-    alt = None
-
-try:
     import matplotlib.pyplot as plt
 except ImportError:
     plt = None
 
-try:
-    import seaborn.objects as so
-except ImportError:
-    so = None
-
 
 class ContentBase:
     container: ET.Element
 
     def __init__(self, class_: str | None = None):
         """Create an empty <div> container.
 
@@ -161,15 +149,15 @@
         self.container.append(pre)
 
 
 class HTML(ContentBase):
     def __init__(
         self,
         text: str,
-        strip_dataframe_borders: bool = False,
+        strip_dataframe_borders: bool = True,
         class_: str | None = None,
     ):
         """Create HTML elements from raw HTML and wrap them in a <div> container.
 
         Args:
             text: A string with raw HTML.
             strip_dataframe_borders: If True, remove borders attributes from dataframes.
@@ -247,83 +235,45 @@
         obj: Any,
         format: Literal["svg", "png"] | None = None,  # noqa: A002
         class_: str | None = None,
         **kwargs: Any,
     ):
         """Create an HTML element from a plot object and wrap it in a <div> container.
 
-        The supported plot types are the following:
-        - Matplotlib Pyplot Axes and Figure,
-        - [Deprecated] Altair Chart,
-        - [Deprecated] Seaborn Plot (seaborn.objects interface).
-
-        Deprecated:
-            Support of the Seaborn plots in this class/method is deprecated
-            and will be removed in version 0.4.0.
-            Use the rico.Obj or obj.append indstead.
-
         Args:
-            obj: The plot object.
+            obj: The Matplotlib Pyplot Axes or Figure object.
             format: Image format.
             class_: The container class attribute.
-            **kwargs: Keyword arguments passed to the function
-                which converts the object to an image.
+            **kwargs: Keyword arguments passed to the `savefig` method.
 
         Raises:
-            TypeError: The plot type is not supported
-                or a required extra package is not installed.
+            ImportError: Matplotlib is not installed.
+            TypeError: The object type should be an instance of plt.Figure or plt.Axes.
         """
+        if plt is None:
+            raise ImportError("Matplotlib is not installed.")
+
+        if not isinstance(obj, plt.Figure | plt.Axes):  # type: ignore
+            raise TypeError(
+                "The object type should be an instance of plt.Figure or plt.Axes.")
+
         if format is None:
             format = rico._config.get_config("image_format")  # noqa: A001
 
-        if plt is not None and isinstance(obj, plt.Axes):
+        if isinstance(obj, plt.Axes):
             obj = obj.figure
 
-        if plt is not None and isinstance(obj, plt.Figure):  # type: ignore
-            stream = io.StringIO() if format == "svg" else io.BytesIO()
-            obj.savefig(stream, format=format, **kwargs)
-            image = stream.getvalue()
-        elif so is not None and isinstance(obj, so.Plot):
-            warnings.warn(
-                "Support of the Seaborn plots in this class/method is deprecated "
-                    "and will be removed in version 0.4.0. "
-                    "Use the rico.Obj or obj.append indstead.",
-                DeprecationWarning,
-                stacklevel=2,
-            )
-            stream = io.StringIO() if format == "svg" else io.BytesIO()
-            obj.save(stream, format=format, **kwargs)
-            image = stream.getvalue()
-        elif alt is not None and isinstance(obj, alt.TopLevelMixin):
-            warnings.warn(
-                "Support of the Altair plots in this class/method is deprecated "
-                    "and will be removed in version 0.4.0. "
-                    "Use the rico.Obj or obj.append indstead.",
-                DeprecationWarning,
-                stacklevel=2,
-            )
-            convert = vlc.vegalite_to_svg if format == "svg" else vlc.vegalite_to_png  # type: ignore  # noqa: E501
-            image = convert(  # type: ignore
-                obj.to_json(),  # type: ignore
-                vl_version="_".join(alt.SCHEMA_VERSION.split(".")[:2]),
-                **kwargs,
-            )
-        else:
-            error_msg = (
-                f"The plot type {type(obj)} is not supported "
-                "or a required extra package is not installed."
-            )
-            raise TypeError(error_msg)
+        stream = io.StringIO() if format == "svg" else io.BytesIO()
+        obj.savefig(stream, format=format, **kwargs)
+        image = stream.getvalue()
 
-        mime_subtype = "svg+xml" if format == "svg" else format
-        content = Image(data=image, mime_subtype=mime_subtype, class_=class_)  # type: ignore  # noqa: E501
+        mime_subtype = "svg+xml" if format == "svg" else "png"
+        content = Image(data=image, mime_subtype=mime_subtype, class_=class_)
         self.container = content.container
 
-Chart = Plot
-
 
 class Script(ContentBase):
     footer: bool = False
 
     def __init__(
         self,
         text: str | None = None,
@@ -333,14 +283,21 @@
         attrib: dict[str, Any] = {},
         **extra: Any,
     ):
         """Create an HTML script element.
 
         Either `text` or `src` should be used.
 
+        Keep in mind that script files can contain links to other external resources.
+        **rico** doesn't parse or change them, even if the `inline` parameter is set
+        to `True`.
+        As a result:
+        * These resurces should be availble when someone opens an HTML document.
+        * Links with relative paths to external resources will not work.
+
         Args:
             text: The script text.
             src: The script source link.
             inline: If True, load script inline, downdload it from source link
                 and use it as `text`.
             defer: The "defer" attribute of the script. For an inline script, defines
                 whether it should be placed in the footer of the document aftert all
@@ -386,14 +343,21 @@
         attrib: dict[str, Any] = {},
         **extra: Any,
     ):
         """Create an HTML style element.
 
         Either `text` or `src` should be used.
 
+        Keep in mind that style files can contain links to other external resources.
+        **rico** doesn't parse or change them, even if the `inline` parameter is set
+        to `True`.
+        As a result:
+        * These resurces should be availble when someone opens an HTML document.
+        * Links with relative paths to external resources will not work.
+
         Args:
             text: The stylesheet text.
             src: The stylesheet source link.
             inline: If True, load stylesheet inline, downdload it from source link
                 and use it as `text`.
             attrib: The stylesheet attributes.
             **extra: Extra attributes.
@@ -445,46 +409,47 @@
                 return {mime_type: data}
             return data
     return {}
 
 def _decode(data: str | bytes) -> str:
     return data.decode() if isinstance(data, bytes) else data
 
-def _get_repr(obj: Any) -> ET.Element:  # noqa: C901, PLR0911, PLR0912
-    data = _call_repr(obj, "_repr_mimebundle_")
+def _get_repr(obj: Any) -> ContentBase:  # noqa: C901, PLR0911, PLR0912
+    data = {k.lower(): v for k, v in _call_repr(obj, "_repr_mimebundle_").items()}
+
     if data == {}:
         data = _call_repr(obj, "_repr_javascript_", "application/javascript")
     if data == {}:
         data = _call_repr(obj, "_repr_html_", "text/html")
     if data == {}:
         data = _call_repr(obj, "_repr_markdown_", "text/markdown")
     if data == {}:
         data = _call_repr(obj, "_repr_svg_", "image/svg+xml")
     if data == {}:
         data = _call_repr(obj, "_repr_png_", "image/png")
     if data == {}:
         data = _call_repr(obj, "_repr_jpeg_", "image/jpeg")
 
     if "application/javascript" in data and data["application/javascript"]:
-        return Script(_decode(data["application/javascript"])).container
+        return Script(_decode(data["application/javascript"]))
     if "text/html" in data and data["text/html"]:
-        return HTML(_decode(data["text/html"]), strip_dataframe_borders=True).container
+        return HTML(_decode(data["text/html"]), strip_dataframe_borders=True)
     if "text/markdown" in data and data["text/markdown"]:
-        return Markdown(_decode(data["text/markdown"])).container
+        return Markdown(_decode(data["text/markdown"]))
     if "image/svg+xml" in data and data["image/svg+xml"]:
-        return Image(data["image/svg+xml"], "svg+xml").container
+        return Image(data["image/svg+xml"], "svg+xml")
     if "image/png" in data and data["image/png"]:
-        return Image(data["image/png"], "png").container
+        return Image(data["image/png"], "png")
     if "image/jpeg" in data and data["image/jpeg"]:
-        return Image(data["image/jpeg"], "jpeg").container
+        return Image(data["image/jpeg"], "jpeg")
     if "image/gif" in data and data["image/gif"]:
-        return Image(data["image/gif"], "gif").container
+        return Image(data["image/gif"], "gif")
     if "text/plain" in data and data["text/plain"]:
-        return Text(data["text/plain"]).container
-    return Text(str(obj)).container
+        return Text(data["text/plain"])
+    return Text(str(obj))
 
 class Obj(ContentBase):
     def __init__(self, *objects: Any, class_: str | None = None):
         """Create HTML elements from objects and wrap them in a <div> container.
 
         Automatically determines the content type in the following order:
         1. `rico` content classes (subclasses of `ContentBase`).
@@ -498,13 +463,13 @@
         Args:
             *objects: The objects.
             class_: The container class attribute.
         """
         super().__init__(class_=class_)
         for obj in objects:
             if isinstance(obj, ContentBase):
-                container = obj.container
+                content = obj
             elif plt is not None and isinstance(obj, plt.Axes | plt.Figure):  # type: ignore  # noqa: E501
-                container = Plot(obj).container
+                content = Plot(obj)
             else:
-                container = _get_repr(obj)
-            self.container.append(container)
+                content = _get_repr(obj)
+            self.container.append(content.container)
```

### Comparing `rico-0.3.2/src/rico/_html.py` & `rico-0.4.0/src/rico/_html.py`

 * *Files identical despite different names*

### Comparing `rico-0.3.2/tests/test__config.py` & `rico-0.4.0/tests/test__config.py`

 * *Files identical despite different names*

### Comparing `rico-0.3.2/tests/test__container.py` & `rico-0.4.0/tests/test__container.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 # pyright: reportUnknownMemberType=false, reportUnknownArgumentType=false
 from __future__ import annotations
 
 import xml.etree.ElementTree as ET
 
-import altair as alt
+import matplotlib.pyplot as plt
 import pytest
 
 import rico._config
 import rico._container
 import rico._content
 
 
 def test_div_init():
     content = rico._container.Div(
-        "Hello world",
+        "Hello, World",
         rico._content.Tag("h1", "Header", class_="col"),
         class_="row",
     )
 
     div0 = content.container
     assert isinstance(div0, ET.Element)
     assert div0.tag == "div"
@@ -34,15 +34,15 @@
     assert div1.tail is None
     assert len(div1) == 1
 
     p = tuple(div1)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello world"
+    assert p.text == "Hello, World"
     assert p.tail is None
     assert len(p) == 0
 
     div2 = tuple(div0)[1]
     assert isinstance(div2, ET.Element)
     assert div2.tag == "div"
     assert div2.attrib == {"class": "col"}
@@ -61,40 +61,40 @@
 
 @pytest.fixture
 def div_container() -> rico._container.Div:
     return rico._container.Div()
 
 
 def test_div_append_tag(div_container: rico._container.Div):
-    div_container.append_tag("h1", "Hello world")
-    content = rico._content.Tag("h1", "Hello world")
+    div_container.append_tag("h1", "Hello, World")
+    content = rico._content.Tag("h1", "Hello, World")
     assert str(div_container) == f"<div>{content}</div>"
 
 
 def test_div_append_text(div_container: rico._container.Div):
-    div_container.append_text("Hello world")
-    content = rico._content.Text("Hello world")
+    div_container.append_text("Hello, World")
+    content = rico._content.Text("Hello, World")
     assert str(div_container) == f"<div>{content}</div>"
 
 
 def test_div_append_code(div_container: rico._container.Div):
-    div_container.append_code("Hello world")
-    content = rico._content.Code("Hello world")
+    div_container.append_code("Hello, World")
+    content = rico._content.Code("Hello, World")
     assert str(div_container) == f"<div>{content}</div>"
 
 
 def test_div_append_html(div_container: rico._container.Div):
-    div_container.append_html("<p>Hello world</p>")
-    content = rico._content.HTML("<p>Hello world</p>")
+    div_container.append_html("<p>Hello, World</p>")
+    content = rico._content.HTML("<p>Hello, World</p>")
     assert str(div_container) == f"<div>{content}</div>"
 
 
 def test_div_append_markdown(div_container: rico._container.Div):
-    div_container.append_markdown("# Hello world")
-    content = rico._content.Markdown("# Hello world")
+    div_container.append_markdown("# Hello, World")
+    content = rico._content.Markdown("# Hello, World")
     assert str(div_container) == f"<div>{content}</div>"
 
 
 svg_data = (
     '<svg xmlns="http://www.w3.org/2000/svg" '
     'xmlns:xlink="http://www.w3.org/1999/xlink" '
     'width="16" height="16" fill="currentColor" class="bi bi-dash">'
@@ -104,38 +104,41 @@
 
 def test_div_append_image(div_container: rico._container.Div):
     div_container.append_image(svg_data, "svg")
     content = rico._content.Image(svg_data, "svg")
     assert str(div_container) == f"<div>{content}</div>"
 
 
-altair_chart = alt.Chart(
-    alt.Data(values=[
-        {"x": "A", "y": 5},
-        {"x": "B", "y": 3},
-        {"x": "C", "y": 6},
-        {"x": "D", "y": 7},
-        {"x": "E", "y": 2},
-    ]),
-).mark_bar().encode(x="x:N", y="y:Q")
+pyplot_figure, pyplot_axes = plt.subplots()  # type: ignore
+pyplot_axes.plot([1, 2, 3, 4], [1, 4, 2, 3])  # type: ignore
 
 def test_div_append_plot(div_container: rico._container.Div):
-    div_container.append_plot(altair_chart)
-    content = rico._content.Plot(altair_chart)
-    assert str(div_container) == f"<div>{content}</div>"
+    div_container.append_plot(pyplot_figure)
+
+    div = div_container.container[0]
+    assert isinstance(div, ET.Element)
+    assert div.tag == "div"
+    assert div.attrib == {}
+    assert div.text is None
+    assert div.tail is None
+    assert len(div) == 1
+
+    img = tuple(div)[0]
+    assert isinstance(img, ET.Element)
+    assert img.tag == "img"
 
 
 def test_div_append(div_container: rico._container.Div):
-    div_container.append("Hello world")
-    content = rico._content.Obj("Hello world")
+    div_container.append("Hello, World")
+    content = rico._content.Obj("Hello, World")
     assert str(div_container) == f"<div>{content}</div>"
 
 
 def test_doc_init_default():  # noqa: PLR0915
-    doc = rico._container.Doc("Hello world")
+    doc = rico._container.Doc("Hello, World")
 
     html = doc.html
     assert isinstance(html, ET.Element)
     assert html.tag == "html"
     assert html.attrib == {}
     assert html.text is None
     assert html.tail is None
@@ -214,31 +217,31 @@
     assert div1.tail is None
     assert len(div1) == 1
 
     p = tuple(div1)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello world"
+    assert p.text == "Hello, World"
     assert p.tail is None
     assert len(p) == 0
 
 
 def test_doc_init_nondefault():  # noqa: PLR0915
     extra_style = rico._content.Style(src="style.css")
-    extra_script = rico._content.Script(text="alert('Hello World!');")
+    extra_script = rico._content.Script(text="alert('Hello, World!');")
     extra_script.footer = True
 
     with rico._config.config_context(
         meta_charset="",
         meta_viewport="",
         dataframe_style="",
     ):
         doc = rico._container.Doc(
-            "Hello world",
+            "Hello, World",
             title="Title",
             bootstrap="full",
             extra_styles=(extra_style,),
             extra_scripts=(extra_script,),
             class_=None,
         )
 
@@ -321,30 +324,31 @@
     assert div1.tail is None
     assert len(div1) == 1
 
     p = tuple(div1)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello world"
+    assert p.text == "Hello, World"
     assert p.tail is None
     assert len(p) == 0
 
     script = tuple(body)[1]
     assert script == extra_script.container
     assert isinstance(script, ET.Element)
     assert script.tag == "script"
     assert script.attrib == {}
-    assert script.text  == "alert('Hello World!');"
+    assert script.text  == "alert('Hello, World!');"
     assert script.tail is None
     assert len(script) == 0
 
 
 def test_doc_serialize():
     with rico._config.config_context(dataframe_style=""):
-        doc = rico._container.Doc("Hello world", bootstrap="none")
+        doc = rico._container.Doc("Hello, World", bootstrap="none")
 
     assert doc.serialize() == (
         '<!doctype html>\n<html><head><meta charset="utf-8"/>'
         '<meta name="viewport" content="width=device-width, initial-scale=1"/></head>'
-        '<body><div class="container"><div><p>Hello world</p></div></div></body></html>'
+        '<body><div class="container"><div><p>Hello, World</p></div></div></body>'
+        '</html>'
     )
```

### Comparing `rico-0.3.2/tests/test__content.py` & `rico-0.4.0/tests/test__content.py`

 * *Files 3% similar despite different names*

```diff
@@ -5,44 +5,30 @@
 import importlib
 import io
 import textwrap
 from typing import TYPE_CHECKING
 import unittest.mock
 import xml.etree.ElementTree as ET
 
-import altair as alt
 import matplotlib.pyplot as plt
 import pytest
-import seaborn.objects as so
 
 import rico._config
 import rico._content
 
 
 if TYPE_CHECKING:
     from typing import Any, Literal
 
 
 def test_import_error():
-    with unittest.mock.patch.dict("sys.modules", {"altair": None}):
-        importlib.reload(rico._content)
-        assert rico._content.alt is None
-
-    with unittest.mock.patch.dict("sys.modules", {"vl_convert": None}):
-        importlib.reload(rico._content)
-        assert rico._content.alt is None
-
     with unittest.mock.patch.dict("sys.modules", {"matplotlib.pyplot": None}):
         importlib.reload(rico._content)
         assert rico._content.plt is None
 
-    with unittest.mock.patch.dict("sys.modules", {"seaborn.objects": None}):
-        importlib.reload(rico._content)
-        assert rico._content.so is None
-
     importlib.reload(rico._content)
 
 
 def test_content_base_simple():
     content = rico._content.ContentBase()
     div = content.container
     assert isinstance(div, ET.Element)
@@ -66,46 +52,46 @@
 
 @pytest.fixture
 def content_base_subclass_sample():
     class ContentBaseSubclass(rico._content.ContentBase):
         def __init__(self, class_: str | None = None):
             super().__init__(class_)
             p = ET.Element("p")
-            p.text = "Hello world"
+            p.text = "Hello, World"
             self.container.append(p)
 
     return ContentBaseSubclass("row")
 
 
 def test_content_base_str(content_base_subclass_sample: rico._content.ContentBase):
-    expectation = '<div class="row"><p>Hello world</p></div>'
+    expectation = '<div class="row"><p>Hello, World</p></div>'
     assert str(content_base_subclass_sample) == expectation
 
 
 def test_content_base_indent(content_base_subclass_sample: rico._content.ContentBase):
     expectation = textwrap.dedent("""\
         <div class="row">
-            <p>Hello world</p>
+            <p>Hello, World</p>
         </div>""")
     assert content_base_subclass_sample.serialize(
         indent=True, space="    ") == expectation
 
 
 def test_content_base_strip(content_base_subclass_sample: rico._content.ContentBase):
-    expectation = '<div class="row"><p>Hello world</p></div>'
+    expectation = '<div class="row"><p>Hello, World</p></div>'
     assert content_base_subclass_sample.serialize(strip=True) == expectation
 
 
 def test_tag():
     content = rico._content.Tag(
         "p",
         attrib={"class": "col"},
         id="42",
-        text="Hello",
-        tail="world",
+        text="Hello,",
+        tail="World",
         class_="row",
     )
 
     div = content.container
     assert isinstance(div, ET.Element)
     assert div.tag == "div"
     assert div.attrib == {"class": "row"}
@@ -113,48 +99,48 @@
     assert div.tail is None
     assert len(div) == 1
 
     p = tuple(div)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {"class": "col", "id": "42"}
-    assert p.text == "Hello"
-    assert p.tail == "world"
+    assert p.text == "Hello,"
+    assert p.tail == "World"
     assert len(p) == 0
 
 
 def test_text_simple():
-    content = rico._content.Text("Hello world", class_="row")
+    content = rico._content.Text("Hello, World", class_="row")
 
     div = content.container
     assert isinstance(div, ET.Element)
     assert div.tag == "div"
     assert div.attrib == {"class": "row"}
     assert div.text is None
     assert div.tail is None
     assert len(div) == 1
 
     p = tuple(div)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello world"
+    assert p.text == "Hello, World"
     assert p.tail is None
     assert len(p) == 0
 
 
 def test_text_pre_mono():
-    content = rico._content.Text("Hello\nworld", mono=True)
+    content = rico._content.Text("Hello,\nWorld", mono=True)
     div = content.container
 
     pre = tuple(div)[0]
     assert isinstance(pre, ET.Element)
     assert pre.tag == "pre"
     assert pre.attrib == {"class": "font-monospace"}
-    assert pre.text == "Hello\nworld"
+    assert pre.text == "Hello,\nWorld"
     assert pre.tail is None
     assert len(pre) == 0
 
 
 def test_text_int_mono_wrap():
     content = rico._content.Text(42, mono=True, wrap=True)
     div = content.container
@@ -165,15 +151,15 @@
     assert p.attrib == {"class": "font-monospace text-wrap"}
     assert p.text == "42"
     assert p.tail is None
     assert len(p) == 0
 
 
 def test_code():
-    content = rico._content.Code("Hello world", class_="row")
+    content = rico._content.Code("Hello, World", class_="row")
 
     div = content.container
     assert isinstance(div, ET.Element)
     assert div.tag == "div"
     assert div.attrib == {"class": "row"}
     assert div.text is None
     assert div.tail is None
@@ -187,35 +173,35 @@
     assert pre.tail is None
     assert len(pre) == 1
 
     code = tuple(pre)[0]
     assert isinstance(code, ET.Element)
     assert code.tag == "code"
     assert code.attrib == {}
-    assert code.text == "Hello world"
+    assert code.text == "Hello, World"
     assert code.tail is None
     assert len(code) == 0
 
 
 def test_html_simple():
-    content = rico._content.HTML('<p border="1">Hello world</p>', True, class_="row")
+    content = rico._content.HTML('<p border="1">Hello, World</p>', True, class_="row")
 
     div = content.container
     assert isinstance(div, ET.Element)
     assert div.tag == "div"
     assert div.attrib == {"class": "row"}
     assert div.text is None
     assert div.tail is None
     assert len(div) == 1
 
     p = tuple(div)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {"border": "1"}
-    assert p.text == "Hello world"
+    assert p.text == "Hello, World"
     assert p.tail is None
     assert len(p) == 0
 
 
 @pytest.mark.parametrize("border", [True, False], ids=["border", "no border"])
 @pytest.mark.parametrize("dataframe", [True, False], ids=["dataframe", "not dataframe"])
 @pytest.mark.parametrize(
@@ -253,15 +239,15 @@
 
 
 def test_markdown():
     content = rico._content.Markdown(
         textwrap.dedent("""\
             # Header 1
             ## Header 2
-            Hello world"""),
+            Hello, World"""),
         class_="row",
     )
 
     div = content.container
     assert isinstance(div, ET.Element)
     assert div.tag == "div"
     assert div.attrib == {"class": "row"}
@@ -285,26 +271,26 @@
     assert h2.tail == "\n"
     assert len(h2) == 0
 
     p = tuple(div)[2]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello world"
+    assert p.text == "Hello, World"
     assert len(p) == 0
 
 
 def test_markdown_error():
     with unittest.mock.patch.dict(
         "sys.modules",
         {"markdown_it": None, "markdown": None},
     ):
         importlib.reload(rico._config)
         with pytest.raises(RuntimeError):
-            rico._content.Markdown("Hello world")
+            rico._content.Markdown("Hello, World")
 
     importlib.reload(rico._config)
 
 
 svg_data = (
     '<svg xmlns="http://www.w3.org/2000/svg" '
     'xmlns:xlink="http://www.w3.org/1999/xlink" '
@@ -359,33 +345,21 @@
     assert img.tag == "img"
     assert img.attrib == {"src": f"data:image/png;base64,{encoded_image}"}
     assert img.text is None
     assert img.tail is None
     assert len(img) == 0
 
 
-altair_chart = alt.Chart(
-    alt.Data(values=[
-        {"x": "A", "y": 5},
-        {"x": "B", "y": 3},
-        {"x": "C", "y": 6},
-        {"x": "D", "y": 7},
-        {"x": "E", "y": 2},
-    ]),
-).mark_bar().encode(x="x:N", y="y:Q")
-
 pyplot_figure, pyplot_axes = plt.subplots()  # type: ignore
 pyplot_axes.plot([1, 2, 3, 4], [1, 4, 2, 3])  # type: ignore
 
-seaborn_plot = so.Plot({"x": [1, 2, 3, 4], "y": [1, 4, 2, 3]})  # type: ignore
-
 @pytest.mark.parametrize(
     "plot",
-    [altair_chart, pyplot_axes, pyplot_figure, seaborn_plot],
-    ids=["altair", "pyplot_axes", "pyplot_figure", "seaborn_plot"],
+    [pyplot_axes, pyplot_figure],
+    ids=["pyplot_axes", "pyplot_figure"],
 )
 @pytest.mark.parametrize("format", [None, "png"], ids=["svg", "png"])
 def test_plot_complete(plot: Any, format: Literal["svg", "png"] | None):  # noqa: A002
     content = rico._content.Plot(plot, format=format, class_="row")
 
     div = content.container
     assert isinstance(div, ET.Element)
@@ -396,36 +370,30 @@
     assert len(div) == 1
 
     img = tuple(div)[0]
     assert isinstance(img, ET.Element)
     assert img.tag == "img"
 
 
-@pytest.mark.parametrize(
-    ("module", "err_plot", "plot"),
-    [
-        ("alt", altair_chart, seaborn_plot),
-        ("plt", pyplot_axes, altair_chart),
-        ("so", seaborn_plot, pyplot_axes),
-    ],
-    ids=["alt", "plt", "so"],
-)
-def test_plot_error(module: str, err_plot: Any, plot: Any):
-    with unittest.mock.patch.object(rico._content, module, None):
-        with pytest.raises(TypeError):
-            rico._content.Plot(err_plot)
-
-        content = rico._content.Plot(plot, class_="row")
-        div = content.container
-        assert isinstance(div, ET.Element)
+def test_plot_import_error():
+    with (
+        unittest.mock.patch.object(rico._content, "plt", None),
+        pytest.raises(ImportError),
+    ):
+            rico._content.Plot(pyplot_axes)
+
+
+def test_plot_type_error():
+    with pytest.raises(TypeError):
+        rico._content.Plot("text")
 
 
 @pytest.mark.parametrize("defer", [True, False], ids=["defer", "not defer"])
 def test_script_text(defer: bool):
-    text = "alert('Hello World!');"
+    text = "alert('Hello, World!');"
     attrib = {"async": True}
     content = rico._content.Script(text=text, defer=defer, attrib=attrib)
 
     script = content.container
     assert isinstance(script, ET.Element)
     assert script.tag == "script"
     assert script.attrib == attrib
@@ -457,15 +425,15 @@
 
     assert content.container == script
     assert content.footer is False
 
 
 @pytest.mark.parametrize("defer", [True, False], ids=["defer", "not defer"])
 def test_script_inline(defer: bool):
-    text = "alert('Hello World!');"
+    text = "alert('Hello, World!');"
     src = "javascript.js"
     attrib = {"async": True}
 
     with unittest.mock.patch("rico._content.urllib.request.urlopen") as urlopen:
         urlopen.return_value = io.BytesIO(text.encode())
         content = rico._content.Script(src=src, inline=True, defer=defer, attrib=attrib)
         urlopen.assert_called_once_with(src)
@@ -482,15 +450,15 @@
     assert content.footer == defer
 
 
 def test_script_raises():
     with pytest.raises(ValueError):
         rico._content.Script()
     with pytest.raises(ValueError):
-        rico._content.Script(src="javascript.js", text="alert('Hello World!');")
+        rico._content.Script(src="javascript.js", text="alert('Hello, World!');")
 
 
 def test_style_text():
     text = "p {color: red;}"
     attrib = {"title": "Style title"}
     content = rico._content.Style(text=text, attrib=attrib)
 
@@ -598,15 +566,15 @@
     assert img.tag == "img"
     assert len(img) == 0
 
 
 def test_obj_javascript():
     class Repr:
         def _repr_javascript_(self) -> str:
-            return "alert('Hello World!');"
+            return "alert('Hello, World!');"
 
     content = rico._content.Obj(Repr(), class_="row")
 
     div0 = content.container
     assert isinstance(div0, ET.Element)
     assert div0.tag == "div"
     assert div0.attrib == {"class": "row"}
@@ -614,23 +582,23 @@
     assert div0.tail is None
     assert len(div0) == 1
 
     script = tuple(div0)[0]
     assert isinstance(script, ET.Element)
     assert script.tag == "script"
     assert script.attrib == {}
-    assert script.text == "alert('Hello World!');"
+    assert script.text == "alert('Hello, World!');"
     assert script.tail is None
     assert len(script) == 0
 
 
 def test_obj_html():
     class Repr:
         def _repr_html_(self) -> str:
-            return "<p>Hello world!</p>"
+            return "<p>Hello, World!</p>"
 
     content = rico._content.Obj(Repr(), class_="row")
 
     div0 = content.container
     assert isinstance(div0, ET.Element)
     assert div0.tag == "div"
     assert div0.attrib == {"class": "row"}
@@ -646,23 +614,23 @@
     assert div1.tail is None
     assert len(div1) == 1
 
     p = tuple(div1)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello world!"
+    assert p.text == "Hello, World!"
     assert p.tail is None
     assert len(p) == 0
 
 
 def test_obj_markdown():
     class Repr:
         def _repr_markdown_(self) -> str:
-            return "# Hello world!"
+            return "# Hello, World!"
 
     content = rico._content.Obj(Repr(), class_="row")
 
     div0 = content.container
     assert isinstance(div0, ET.Element)
     assert div0.tag == "div"
     assert div0.attrib == {"class": "row"}
@@ -678,15 +646,15 @@
     assert div1.tail is None
     assert len(div1) == 1
 
     h1 = tuple(div1)[0]
     assert isinstance(h1, ET.Element)
     assert h1.tag == "h1"
     assert h1.attrib == {}
-    assert h1.text == "Hello world!"
+    assert h1.text == "Hello, World!"
     assert len(h1) == 0
 
 
 def test_obj_svg():
     image = svg_data
     class Repr:
         def _repr_svg_(self) -> str:
@@ -825,15 +793,15 @@
     assert img.tail is None
     assert len(img) == 0
 
 
 def test_obj_text():
     class Repr:
         def _repr_mimebundle_(self) -> dict[str, Any]:
-            return {"text/plain": "Hello world!"}
+            return {"text/plain": "Hello, World!"}
 
     content = rico._content.Obj(Repr(), class_="row")
 
     div0 = content.container
     assert isinstance(div0, ET.Element)
     assert div0.tag == "div"
     assert div0.attrib == {"class": "row"}
@@ -849,28 +817,28 @@
     assert div1.tail is None
     assert len(div1) == 1
 
     p = tuple(div1)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello world!"
+    assert p.text == "Hello, World!"
     assert p.tail is None
     assert len(p) == 0
 
 
 def test_obj_priority():
     class Repr:
         def _repr_javascript_(self) -> str:
-            return "alert('Hello World!');"
+            return "alert('Hello, World!');"
 
         def _repr_mimebundle_(self) -> dict[str, Any]:
             return {
-                "text/plain": "Hello world!",
-                "text/markdown": "# Hello world!",
+                "text/plain": "Hello, World!",
+                "text/markdown": "# Hello, World!",
             }
 
     content = rico._content.Obj(Repr(), class_="row")
 
     div0 = content.container
     assert isinstance(div0, ET.Element)
     assert div0.tag == "div"
@@ -887,25 +855,25 @@
     assert div1.tail is None
     assert len(div1) == 1
 
     h1 = tuple(div1)[0]
     assert isinstance(h1, ET.Element)
     assert h1.tag == "h1"
     assert h1.attrib == {}
-    assert h1.text == "Hello world!"
+    assert h1.text == "Hello, World!"
     assert len(h1) == 0
 
 
 def test_obj_corner_cases():
     class Repr:
         def _repr_javascript_(self) -> str | None:
             return None
 
         def _repr_markdown_(self) -> tuple[str, Any]:
-            return "# Hello world!", "metadata"
+            return "# Hello, World!", "metadata"
 
     content = rico._content.Obj(Repr(), class_="row")
 
     div0 = content.container
     assert isinstance(div0, ET.Element)
     assert div0.tag == "div"
     assert div0.attrib == {"class": "row"}
@@ -921,9 +889,9 @@
     assert div1.tail is None
     assert len(div1) == 1
 
     h1 = tuple(div1)[0]
     assert isinstance(h1, ET.Element)
     assert h1.tag == "h1"
     assert h1.attrib == {}
-    assert h1.text == "Hello world!"
+    assert h1.text == "Hello, World!"
     assert len(h1) == 0
```

### Comparing `rico-0.3.2/tests/test__html.py` & `rico-0.4.0/tests/test__html.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,40 +11,40 @@
 def elem_to_string(elem: ET.Element | tuple[ET.Element], sep: str = "") -> str:
     if isinstance(elem, tuple):
         return sep.join(elem_to_string(e) for e in elem)
     return ET.tostring(elem, encoding="unicode", method="html")
 
 
 def test_parse_html_two_elements():
-    text = "<p>Hello</p><p>world</p>"
+    text = "<p>Hello,</p><p>World</p>"
     elements = rico._html.parse_html(text)
 
     assert elem_to_string(elements) == text
     assert isinstance(elements, tuple)
     assert len(elements) == 2
 
     p0 = elements[0]
     assert isinstance(p0, ET.Element)
     assert p0.tag == "p"
     assert p0.attrib == {}
-    assert p0.text == "Hello"
+    assert p0.text == "Hello,"
     assert p0.tail is None
     assert len(p0) == 0
 
     p1 = elements[1]
     assert isinstance(p1, ET.Element)
     assert p1.tag == "p"
     assert p1.attrib == {}
-    assert p1.text == "world"
+    assert p1.text == "World"
     assert p1.tail is None
     assert len(p1) == 0
 
 
 def test_parse_html_nested_tags():
-    text = "<div><p>Hello <strong>world</strong>!</p></div>"
+    text = "<div><p>Hello, <strong>World</strong>!</p></div>"
     elements = rico._html.parse_html(text)
 
     assert elem_to_string(elements) == text
     assert isinstance(elements, tuple)
     assert len(elements) == 1
 
     div = elements[0]
@@ -55,23 +55,23 @@
     assert div.tail is None
     assert len(div) == 1
 
     p = tuple(div)[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello "
+    assert p.text == "Hello, "
     assert p.tail is None
     assert len(p) == 1
 
     strong = tuple(p)[0]
     assert isinstance(strong, ET.Element)
     assert strong.tag == "strong"
     assert strong.attrib == {}
-    assert strong.text == "world"
+    assert strong.text == "World"
     assert strong.tail == "!"
     assert len(strong) == 0
 
 
 def test_parse_html_attributes():
     script_src = "https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js"
     text = f"<script defer src='{script_src}' crossorigin='anonymous'></script>"
@@ -129,26 +129,26 @@
     }
     assert path.text is None
     assert path.tail is None
     assert len(path) == 0
 
 
 def test_parse_html_empty_tag():
-    text = "<p>Hello<br><br>world<br></p>"
+    text = "<p>Hello,<br><br>World<br></p>"
     elements = rico._html.parse_html(text)
 
     assert elem_to_string(elements) == text
     assert isinstance(elements, tuple)
     assert len(elements) == 1
 
     p = elements[0]
     assert isinstance(p, ET.Element)
     assert p.tag == "p"
     assert p.attrib == {}
-    assert p.text == "Hello"
+    assert p.text == "Hello,"
     assert p.tail is None
     assert len(p) == 3
 
     br0 = p[0]
     assert isinstance(br0, ET.Element)
     assert br0.tag == "br"
     assert br0.attrib == {}
@@ -157,15 +157,15 @@
     assert len(br0) == 0
 
     br1 = p[1]
     assert isinstance(br1, ET.Element)
     assert br1.tag == "br"
     assert br1.attrib == {}
     assert br1.text is None
-    assert br1.tail == "world"
+    assert br1.tail == "World"
     assert len(br1) == 0
 
     br2 = p[2]
     assert isinstance(br2, ET.Element)
     assert br2.tag == "br"
     assert br2.attrib == {}
     assert br2.text is None
@@ -179,186 +179,186 @@
     div0.text = "\n"
     style = ET.SubElement(div0, "style")
     style.text = textwrap.dedent("""\
         strong {color: red;}
         code {color: blue;}
     """)
     p0 = ET.SubElement(div0, "p")
-    p0.text = " Hello "
+    p0.text = " Hello, "
     p0.tail = "\n"
     strong = ET.SubElement(p0, "strong")
-    strong.text = " world "
+    strong.text = " World "
     strong.tail = " ! "
     div1 = ET.SubElement(div0, "div", {"class": '>&"'})
     div1.text = "\n"
     div1.tail = "\n"
     code0 = ET.SubElement(div1, "code")
     code0.text = " should be indented "
     code0.tail = "\n"
     pre = ET.SubElement(div0, "pre")
     pre.text = "\n"
     pre.tail = "\n"
     code1 = ET.SubElement(pre, "code")
     code1.text = " should not be indented "
     code1.tail = "\n"
     p1 = ET.SubElement(div0, "p")
-    p1.text = " Hello >&< "
+    p1.text = " Hello, >&< "
     p1.tail = "\n"
     br = ET.SubElement(p1, "br")
-    br.tail = " world again "
+    br.tail = " World again "
     return div0
 
 
 def test_indent_html_default(sample_elem: ET.Element):
     expectation = textwrap.dedent("""\
         <div class="container">
           <style>
             strong {color: red;}
             code {color: blue;}
           </style>
-          <p> Hello <strong> world </strong> ! </p>
+          <p> Hello, <strong> World </strong> ! </p>
           <div class="&gt;&amp;&quot;">
             <code> should be indented </code>
           </div>
           <pre>
         <code> should not be indented </code>
         </pre>
-          <p> Hello &gt;&amp;&lt; <br> world again </p>
+          <p> Hello, &gt;&amp;&lt; <br> World again </p>
         </div>""")
 
     assert elem_to_string(rico._html.indent_html(sample_elem)) == expectation
 
 
 def test_indent_html_custom_space(sample_elem: ET.Element):
     expectation = textwrap.dedent("""\
         <div class="container">
             <style>
                 strong {color: red;}
                 code {color: blue;}
             </style>
-            <p> Hello <strong> world </strong> ! </p>
+            <p> Hello, <strong> World </strong> ! </p>
             <div class="&gt;&amp;&quot;">
                 <code> should be indented </code>
             </div>
             <pre>
         <code> should not be indented </code>
         </pre>
-            <p> Hello &gt;&amp;&lt; <br> world again </p>
+            <p> Hello, &gt;&amp;&lt; <br> World again </p>
         </div>""")
 
     assert elem_to_string(
         rico._html.indent_html(sample_elem, "    ")) == expectation
 
 
 def test_strip_html(sample_elem: ET.Element):
     p = ET.Element("p")
-    p.text = " Hello world again again "
+    p.text = " Hello, World again again "
     sample_elem.append(p)
 
     expectation = textwrap.dedent("""\
         <div class="container"><style>strong {color: red;}
-        code {color: blue;}</style><p>Hello <strong> world </strong> ! </p>
+        code {color: blue;}</style><p>Hello, <strong> World </strong> ! </p>
         <div class="&gt;&amp;&quot;"><code> should be indented </code>
         </div>
         <pre>
         <code> should not be indented </code>
         </pre>
-        <p>Hello &gt;&amp;&lt; <br> world again </p>
-        <p>Hello world again again</p></div>""")
+        <p>Hello, &gt;&amp;&lt; <br> World again </p>
+        <p>Hello, World again again</p></div>""")
 
     assert elem_to_string(rico._html.strip_html(sample_elem)) == expectation
 
 
 def test_serialize_html_default(sample_elem: ET.Element):
     expectation = textwrap.dedent("""\
         <div class="container">
         <style>strong {color: red;}
         code {color: blue;}
-        </style><p> Hello <strong> world </strong> ! </p>
+        </style><p> Hello, <strong> World </strong> ! </p>
         <div class="&gt;&amp;&quot;">
         <code> should be indented </code>
         </div>
         <pre>
         <code> should not be indented </code>
         </pre>
-        <p> Hello &gt;&amp;&lt; <br/> world again </p>
+        <p> Hello, &gt;&amp;&lt; <br/> World again </p>
         </div>""")
 
     assert rico._html.serialize_html(sample_elem) == expectation
 
 
 def test_serialize_html_indent(sample_elem: ET.Element):
     expectation = textwrap.dedent("""\
         <div class="container">
             <style>
                 strong {color: red;}
                 code {color: blue;}
             </style>
-            <p> Hello <strong> world </strong> ! </p>
+            <p> Hello, <strong> World </strong> ! </p>
             <div class="&gt;&amp;&quot;">
                 <code> should be indented </code>
             </div>
             <pre>
         <code> should not be indented </code>
         </pre>
-            <p> Hello &gt;&amp;&lt; <br/> world again </p>
+            <p> Hello, &gt;&amp;&lt; <br/> World again </p>
         </div>""")
 
     assert rico._html.serialize_html(
         sample_elem, indent=True, space="    ") == expectation
 
 
 def test_serialize_html_strip(sample_elem: ET.Element):
     expectation = textwrap.dedent("""\
         <div class="container"><style>strong {color: red;}
-        code {color: blue;}</style><p>Hello <strong> world </strong> ! </p>
+        code {color: blue;}</style><p>Hello, <strong> World </strong> ! </p>
         <div class="&gt;&amp;&quot;"><code> should be indented </code>
         </div>
         <pre>
         <code> should not be indented </code>
         </pre>
-        <p>Hello &gt;&amp;&lt; <br/> world again </p>
+        <p>Hello, &gt;&amp;&lt; <br/> World again </p>
         </div>""")
 
     assert rico._html.serialize_html(sample_elem, strip=True) == expectation
 
 
 def test_serialize_html_bool_attr(sample_elem: ET.Element):
     sample_elem.set("autofocus", None)  # type: ignore
     expectation = textwrap.dedent("""\
         <div class="container" autofocus>
         <style>strong {color: red;}
         code {color: blue;}
-        </style><p> Hello <strong> world </strong> ! </p>
+        </style><p> Hello, <strong> World </strong> ! </p>
         <div class="&gt;&amp;&quot;">
         <code> should be indented </code>
         </div>
         <pre>
         <code> should not be indented </code>
         </pre>
-        <p> Hello &gt;&amp;&lt; <br/> world again </p>
+        <p> Hello, &gt;&amp;&lt; <br/> World again </p>
         </div>""")
 
     assert rico._html.serialize_html(sample_elem) == expectation
     sample_elem.set("autofocus", True)  # type: ignore
     assert rico._html.serialize_html(sample_elem) == expectation
 
     sample_elem.set("autofocus", False)  # type: ignore
     expectation = textwrap.dedent("""\
         <div class="container">
         <style>strong {color: red;}
         code {color: blue;}
-        </style><p> Hello <strong> world </strong> ! </p>
+        </style><p> Hello, <strong> World </strong> ! </p>
         <div class="&gt;&amp;&quot;">
         <code> should be indented </code>
         </div>
         <pre>
         <code> should not be indented </code>
         </pre>
-        <p> Hello &gt;&amp;&lt; <br/> world again </p>
+        <p> Hello, &gt;&amp;&lt; <br/> World again </p>
         </div>""")
     assert rico._html.serialize_html(sample_elem) == expectation
 
 
 def test_serialize_html_style():
     elem = ET.Element("style")
     elem.text = ".>&< {border: none;}"
```

### Comparing `rico-0.3.2/tests/test__version.py` & `rico-0.4.0/tests/test__version.py`

 * *Files identical despite different names*

### Comparing `rico-0.3.2/PKG-INFO` & `rico-0.4.0/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rico
-Version: 0.3.2
+Version: 0.4.0
 Summary: A Python package for creating HTML documents from rich content: dataframes, plots, images, markdown etc. It provides a high-level, easy-to-use API with reasonable defaults, as well as low-level access for better control.
 Author-Email: Evgeny Ivanov <ivanov.evgeny.n@gmail.com>
 License: MIT
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: MIT License
@@ -17,25 +17,14 @@
 Classifier: Topic :: Text Processing
 Classifier: Topic :: Text Processing :: Markup
 Classifier: Topic :: Text Processing :: Markup :: HTML
 Classifier: Topic :: Text Processing :: Markup :: Markdown
 Project-URL: Source, https://github.com/e10v/rico
 Project-URL: Release notes, https://github.com/e10v/rico/releases
 Requires-Python: >=3.10
-Provides-Extra: altair
-Provides-Extra: markdown
-Provides-Extra: pyplot
-Provides-Extra: seaborn
-Provides-Extra: complete
-Requires-Dist: altair>=4.2; extra == "altair"
-Requires-Dist: vl-convert-python>=0.8; extra == "altair"
-Requires-Dist: markdown>=3.3; extra == "markdown"
-Requires-Dist: matplotlib>=3.5; extra == "pyplot"
-Requires-Dist: seaborn>=0.12; extra == "seaborn"
-Requires-Dist: rico[altair,markdown,pyplot,seaborn]; extra == "complete"
 Description-Content-Type: text/markdown
 
 # rico: rich content to HTML as easy as Doc(df, plot)
 
 **rico** is a Python package for creating HTML documents from rich content: dataframes, plots, images, markdown etc. It provides a high-level, easy-to-use API with reasonable defaults, as well as low-level access for better control.
 
 Use **rico** if you want to create an HTML document from objects created in a Python script.
@@ -60,61 +49,71 @@
 
 ```bash
 pip install rico
 ```
 
 **rico** has no dependencies other than the standard Python packages.
 
+For Markdown support:
+* install [markdown-it-py](https://github.com/executablebooks/markdown-it-py),
+* or install [Python Markdown](https://github.com/Python-Markdown/),
+* or set your own Markdown renderer using `rico.set_config`.
+
 ### Deprecated
 
 Optional additional dependencies were required to support the following content types:
 * Plots (`rico[altair]`, `rico[pyplot]`, `rico[seaborn]`).
 * Markdown (`rico[markdown]`).
 
 The `rico[complete]` extra incudes all the dependencies above.
 
 They are no longer needed and will be removed in version 0.4.0.
 
 ## User guide
 
+To get started with **rico**, take a look at the self-explanatory [examples](https://github.com/e10v/rico/tree/main/examples) with resulting HTML documents. The user guide contains a slightly more detailed explanation.
+
 ### Basic usage
 
 **rico** provides both declarative and imperative style interfaces.
 
 Declarative style:
 ```python
 import pandas as pd
 import rico
 
-df = pd.DataFrame({
-    "a": list("CCCDDDEEE"),
-    "b": [2, 7, 4, 1, 2, 6, 8, 4, 7],
-})
-plot = df.plot.scatter(x="a", y="b")
+df = pd.DataFrame(
+    {
+        "x": [2, 7, 4, 1, 2, 6, 8, 4, 7],
+        "y": [1, 9, 2, 8, 3, 7, 4, 6, 5],
+    },
+    index=pd.Index(list("AAABBBCCC")),
+)
+plot = df.plot.scatter(x="x", y="y")
 
-doc = rico.Doc("Hello world!", df, plot, title="My doc")
+doc = rico.Doc("Hello, World!", df, plot, title="My doc")
 ```
 
 Imperative style:
 ```python
 doc = rico.Doc(title="My doc")
-doc.append("Hello world!", df, plot)
+doc.append("Hello, World!", df, plot)
 ```
 
 Also imperative style:
 ```python
 doc = rico.Doc(title="My doc")
-doc.append("Hello world!")
+doc.append("Hello, World!")
 doc.append(df)
 doc.append(plot)
 ```
 
 Mix-and-match:
 ```python
-doc = rico.Doc("Hello world!", df, title="My doc")
+doc = rico.Doc("Hello, World!", df, title="My doc")
 doc.append(plot)
 ```
 
 ### Serialization
 
 Serialize the document to HTML using `str(doc)`:
 ```python
@@ -164,33 +163,33 @@
 * Matplotlib Pyplot Plots.
 * Dataframes and other types with [IPython rich representation methods](https://ipython.readthedocs.io/en/stable/config/integrating.html).
 * Text.
 
 Use specific classes for plots and texts to change the default behavior:
 ```python
 doc = rico.Doc(
-    rico.Text("Hello world!", mono=True),  # The default value is False.
+    rico.Text("Hello, World!", mono=True),  # The default value is False.
     df,
-    rico.Plot(plot, format="png"),  # The default value is "svg".
+    rico.Plot(plot, format="png", bbox_inches="tight"),  # The default value is "svg".
     title="My doc",
 )
 ```
 
 The following code gives the same result as the code above:
 ```python
 doc = rico.Doc(title="My doc")
-doc.append_text("Hello world!", mono=True)
+doc.append_text("Hello, World!", mono=True)
 doc.append(df)
-doc.append_plot(plot, format="png")
+doc.append_plot(plot, format="png", bbox_inches="tight")
 ```
 
 Some options can be set in the global configuration:
 ```python
 with rico.config_context(text_mono=True, image_format="png"):
-    doc = rico.Doc("Hello world!", df, plot, title="My doc")
+    doc = rico.Doc("Hello, World!", df, plot, title="My doc")
 ```
 
 Use specific classes and methods for other content types:
 * Images: `Image` or `Doc.append_image`.
 * Code: `Code` or `Doc.append_code`.
 * Markdown*: `Markdown` or `Doc.append_markdown`.
 * HTML tag: `Tag` or `Doc.append_tag`.
@@ -202,69 +201,69 @@
 ```python
 doc = rico.Doc(
     rico.Markdown("## Dataframe"),
     df,
     rico.Tag("h2", "Plot"),  # An alternative way to add a header.
     plot,
     rico.HTML("<h2>Code</h2>"),  # Another way to add a header.
-    rico.Code("print('Hello world!')"),
+    rico.Code("print('Hello, World!')"),
     title="My doc",
 )
 ```
 
 The following code gives the same result as the code above:
 ```python
 doc = rico.Doc(title="My doc")
 doc.append_markdown("## Dataframe")
 doc.append(df)
 doc.append_tag("h2", "Plot")
 doc.append(plot)
 doc.append_html("<h2>Code</h2>")
-doc.append_code("print('Hello world!')")
+doc.append_code("print('Hello, World!')")
 ```
 
 Check the docstrings for details.
 
 Serialize content to HTML using `str(object)` or `object.serialize()`:
 ```python
-obj = rico.Tag("p", "Hello world!")
+obj = rico.Tag("p", "Hello, World!")
 
 print(obj)
-# <div><p>Hello world!</p></div>
+# <div><p>Hello, World!</p></div>
 
 print(obj.serialize(indent=True, space="    "))
 # <div>
-#     <p>Hello world!</p>
+#     <p>Hello, World!</p>
 # </div>
 ```
 
 ### Bootstrap, HTML classes and document layout
 
 By default, [Bootstrap](https://getbootstrap.com/) styles are included in the document. Change the default behavior using the `bootstrap` parameter:
 ```python
-doc = rico.Doc("Hello world!", bootstrap="full")
+doc = rico.Doc("Hello, World!", bootstrap="full")
 ```
 
 * Set `bootstrap` to `"css"` (default) to include only CSS.
 * Set `bootstrap` to `"full"` to include both the CSS and JS.
 * Set `bootstrap` to `"none"` to not include Bootstrap*.
 
 *Keep in mind that **rico** relies on Bootstrap classes and styles. For example:
 * The `mono` and `wrap` parameters of the `Text` class use Bootstrap's `font-monospace` and `font-monospace` classes.
 * **rico**'s dataframe style definition uses Bootstrap variables.
 
 Each content element is wrapped in a `<div>` container. Specify the element's container class using the `class_` parameter:
 ```python
-print(rico.Tag("p", "Hello world!", class_="col"))
-# <div class="col"><p>Hello world!</p></div>
+print(rico.Tag("p", "Hello, World!", class_="col"))
+# <div class="col"><p>Hello, World!</p></div>
 ```
 
 All elements' containers in the document are also wrapped in a `<div>` container. Specify the document's container class using the `class_` parameter:
 ```python
-doc = rico.Doc("Hello world!", class_="container-fluid")
+doc = rico.Doc("Hello, World!", class_="container-fluid")
 ```
 
 Define the document layout using Bootstrap and `Div` class:
 ```python
 doc = rico.Doc(rico.Div(
     rico.Obj(df, class_="col"),
     rico.Obj(plot, class_="col"),
@@ -272,49 +271,67 @@
 ))
 ```
 
 The code above creates a document with two columns, one with a dataframe and another with a plot. The `Obj` is a magic class which automatically determines the content type in the same way that `Doc` and `Doc.append` do.
 
 Another example:
 ```python
+import altair as alt
+
 doc = rico.Doc(
-    rico.Tag("h1", "My doc"),
-    rico.Tag("h2", "Description"),
-    "This is an example of custom document layout using Bootstrap classes.",
-    rico.Tag("h2", "Data"),
+    rico.Tag("h2", "Dataframes"),
     rico.Div(
-        rico.Obj("Dataframe", df, class_="col"),
-        rico.Obj("Plot", plot, class_="col"),
+        rico.Obj(rico.Tag("h3", "A"), df.loc["A", :], class_="col"),
+        rico.Obj(rico.Tag("h3", "B"), df.loc["B", :], class_="col"),
+        rico.Obj(rico.Tag("h3", "C"), df.loc["C", :], class_="col"),
         class_="row row-cols-auto",
     ),
-    title="My doc",
+    rico.Tag("h2", "Plots"),
+    rico.Div(
+        rico.Obj(
+            rico.Tag("h3", "A"),
+            alt.Chart(df.loc["A", :]).mark_point().encode(x="x", y="y"),
+            class_="col",
+        ),
+        rico.Obj(
+            rico.Tag("h3", "B"),
+            alt.Chart(df.loc["B", :]).mark_point().encode(x="x", y="y"),
+            class_="col",
+        ),
+        rico.Obj(
+            rico.Tag("h3", "C"),
+            alt.Chart(df.loc["C", :]).mark_point().encode(x="x", y="y"),
+            class_="col",
+        ),
+        class_="row row-cols-auto",
+    ),
+    title="Grid system",
 )
 ```
 
 The following code gives the same result as the code above:
 ```python
-doc = rico.Doc(title="My doc")
-doc.append_tag("h1", "My doc")
-doc.append_tag("h2", "Description")
-doc.append("This is an example of custom document layout using Bootstrap classes.")
-doc.append_tag("h2", "Data")
-div = rico.Div(class_="row row-cols-auto")
-doc.append(div)
-div.append("Dataframe", df, class_="col")
-div.append("Plot", plot, class_="col")
-```
+doc = rico.Doc(title="Grid system")
 
-Keep in mind that `obj.append(x, y)` works differently than
-```python
-obj.append(x)
-obj.append(y)
+doc.append_tag("h2", "Dataframes")
+div1 = rico.Div(class_="row row-cols-auto")
+doc.append(div1)
+for name, data in df.groupby(df.index):
+    div1.append(rico.Tag("h3", name), data, class_="col")
+
+doc.append_tag("h2", "Plots")
+div2 = rico.Div(class_="row row-cols-auto")
+doc.append(div2)
+for name, data in df.groupby(df.index):
+    div2.append(
+        rico.Tag("h3", name),
+        alt.Chart(data).mark_point().encode(x="x", y="y"),
+        class_="col",
+    )
 ```
-The first one wraps both elements in a single `<div>` container. The second one creates a separate `<div>` container for each element.
-
-`Obj(x, y, class_="z")` wraps both `x` and `y` elements in a single `<div>` container with `class` attribute set to `"z"`.
 
 More on Bootstrap layout and grid system:
 * [Breakpoints](https://getbootstrap.com/docs/5.3/layout/breakpoints/)
 * [Containers](https://getbootstrap.com/docs/5.3/layout/containers/)
 * [Grid system](https://getbootstrap.com/docs/5.3/layout/grid/)
 * [Columns](https://getbootstrap.com/docs/5.3/layout/columns/)
 
@@ -335,65 +352,71 @@
 dark_theme = "https://cdn.jsdelivr.net/npm/bootswatch@5/dist/darkly/bootstrap.min.css"
 jquery = "https://cdn.jsdelivr.net/npm/jquery@3/dist/jquery.min.js"
 
 doc = rico.Doc(
     rico.Text("Click me", class_="click"),
     extra_styles=(
         rico.Style(src=dark_theme),
-        rico.Style(".click {color: red;}"),
+        rico.Style(".click {color: yellow;}"),
     ),
     extra_scripts=(
         rico.Script(src=jquery),
         rico.Script(
-            "$('p').on('click', function() {alert('Hello world!');})",
+            "$('p').on('click', function() {alert('Hello, World!');})",
             defer=True,
         ),
     ),
 )
 ```
 
 The `defer` parameter adds the `defer` attribute to the `<script>` tag if the `src` parameter is used. Otherwise, if the `text` parameter is used, the script is placed in the footer of the document.
 
 By default, external styles and scripts are included as file links. This means that these files must be available when someone opens the document. Include the contents of these files in the document using the `inline` parameter:
 ```python
 doc = rico.Doc(
     rico.Text("Click me", class_="click"),
     extra_styles=(
         rico.Style(src=dark_theme, inline=True),
-        rico.Style(".click {color: red;}"),
+        rico.Style(".click {color: yellow;}"),
     ),
     extra_scripts=(
         rico.Script(src=jquery, inline=True),
         rico.Script(
-            "$('p').on('click', function() {alert('Hello world!');})",
+            "$('p').on('click', function() {alert('Hello, World!');})",
             defer=True,
         ),
     ),
 )
 ```
 
 In the example above, the Bootstrap styles are still included as a link. Use the global options `inline_styles` and `inline_scripts` to include the contents of the style and script files in the document:
 ```python
 with rico.config_context(inline_styles=True, inline_scripts=True):
     doc = rico.Doc(
         rico.Text("Click me", class_="click"),
         extra_styles=(
             rico.Style(src=dark_theme),
-            rico.Style(".click {color: red;}"),
+            rico.Style(".click {color: yellow;}"),
         ),
         extra_scripts=(
             rico.Script(src=jquery),
             rico.Script(
-                "$('p').on('click', function() {alert('Hello world!');})",
+                "$('p').on('click', function() {alert('Hello, World!');})",
                 defer=True,
             ),
         ),
     )
 ```
 
+Keep in mind that style and script files can contain links to other external resources. **rico** doesn't parse or change them, even if the `inline` parameter or the `inline_styles` and `inline_scripts` global options are set to `True`. As a result:
+* These resurces should be availble when someone opens an HTML document created by **rico**.
+* Links with relative paths to external resources will not work.
+
+For example, [Bootstrap Icons CSS](https://cdn.jsdelivr.net/npm/bootstrap-icons@1/font/bootstrap-icons.css) contains linkes to fonts with relative paths: `url("./fonts/bootstrap-icons.woff2?1fa40e8900654d2863d011707b9fb6f2")`. Including this CSS file with the `inline` parameter set to `True` will make these links invalid.
+
 ### Global configuration
 
 Use global configuration to:
 * Get or set default parameter values.
 * Get or set document properties.
 * Get or set a markdown renderer method.
 
@@ -472,18 +495,12 @@
 ## Alternatives
 
 * Use [Jupyter Notebook](https://jupyter.org/) for interactive computing.
 * Use [nbconvert](https://nbconvert.readthedocs.io/) or [papermill](https://papermill.readthedocs.io/) if you're processing data and creating objects for a document in a Jupyter notebook.
 * Use [Quarto](https://quarto.org/) if you prefer R Markdown style notebooks and a variety of output formats.
 * Use [xml.etree.ElementTree](https://docs.python.org/3/library/xml.etree.elementtree.html), [lxml](https://lxml.de/), [Yattag](https://www.yattag.org/), or [Airium](https://gitlab.com/kamichal/airium) if you need low-level control.
 
-More on the topic:
-* "I Don’t Like Notebooks": [video](https://www.youtube.com/watch?v=7jiPeIFXb6U), [slides](https://docs.google.com/presentation/d/1n2RlMdmv1p25Xy5thJUhkKGvjtV-dkAIsUXP-AL4ffI/edit#slide=id.g362da58057_0_1).
-* [The First Notebook War](https://yihui.org/en/2018/09/notebook-war/).
-
 ## Roadmap
 
-* Support most of IPython rich representation [methods](https://ipython.readthedocs.io/en/stable/config/integrating.html#rich-display).
+* Support math equations with [MathJax](https://www.mathjax.org/) and/or [KaTeX](https://katex.org/).
+* Support PDF content.
 * Create docs with [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
-* Create short quick start.
-* Create examples with resulting HTML files.
-* Support math with [KaTeX](https://katex.org/).
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

