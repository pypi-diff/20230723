# Comparing `tmp/tablate-0.0.6.tar.gz` & `tmp/tablate-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tablate-0.0.6.tar", last modified: Sat Jul 22 12:55:58 2023, max compression
+gzip compressed data, was "tablate-0.0.7.tar", last modified: Sun Jul 23 05:01:03 2023, max compression
```

## Comparing `tablate-0.0.6.tar` & `tablate-0.0.7.tar`

### file list

```diff
@@ -1,136 +1,143 @@
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.573204 tablate-0.0.6/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1069 2023-07-13 22:13:22.000000 tablate-0.0.6/LICENCE
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      509 2023-07-22 12:55:58.572204 tablate-0.0.6/PKG-INFO
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 00:33:05.000000 tablate-0.0.6/README.md
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      583 2023-07-22 12:54:43.000000 tablate-0.0.6/pyproject.toml
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       38 2023-07-22 12:55:58.573204 tablate-0.0.6/setup.cfg
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.556204 tablate-0.0.6/tablate/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      117 2023-07-19 10:35:23.000000 tablate-0.0.6/tablate/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.557204 tablate-0.0.6/tablate/api/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     9502 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/Tablate.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 22:41:07.000000 tablate-0.0.6/tablate/api/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.557204 tablate-0.0.6/tablate/api/classes/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 01:25:25.000000 tablate-0.0.6/tablate/api/classes/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.558204 tablate-0.0.6/tablate/api/classes/modules/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 00:16:24.000000 tablate-0.0.6/tablate/api/classes/modules/Grid.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 00:16:19.000000 tablate-0.0.6/tablate/api/classes/modules/Table.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 00:16:13.000000 tablate-0.0.6/tablate/api/classes/modules/Text.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 22:41:07.000000 tablate-0.0.6/tablate/api/classes/modules/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.558204 tablate-0.0.6/tablate/api/classes/options/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 22:41:07.000000 tablate-0.0.6/tablate/api/classes/options/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.558204 tablate-0.0.6/tablate/api/classes/options/html/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 13:24:20.000000 tablate-0.0.6/tablate/api/classes/options/html/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.559204 tablate-0.0.6/tablate/api/classes/options/html/style/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     4480 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/classes/options/html/style/StyleCss.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 13:24:20.000000 tablate-0.0.6/tablate/api/classes/options/html/style/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.559204 tablate-0.0.6/tablate/api/classes/options/html/style/mixins/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      508 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/classes/options/html/style/mixins/AddStyleMixin.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      519 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/classes/options/html/style/mixins/ClassNameMixin.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 01:07:40.000000 tablate-0.0.6/tablate/api/classes/options/html/style/mixins/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.559204 tablate-0.0.6/tablate/api/classes/options/html/style/subclasses/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2430 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/classes/options/html/style/subclasses/ElementStyle.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      591 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/classes/options/html/style/subclasses/TableStyle.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      682 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/classes/options/html/style/subclasses/TextStyle.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 13:24:20.000000 tablate-0.0.6/tablate/api/classes/options/html/style/subclasses/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.560204 tablate-0.0.6/tablate/api/classes/options/html/style/utilities/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 15:13:12.000000 tablate-0.0.6/tablate/api/classes/options/html/style/utilities/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      231 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/classes/options/html/style/utilities/base_names.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2285 2023-07-22 08:57:04.000000 tablate-0.0.6/tablate/api/classes/options/html/style/utilities/css_factory.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      880 2023-07-22 08:57:04.000000 tablate-0.0.6/tablate/api/classes/options/html/style/utilities/selectors.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      885 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/api/classes/options/html/style/utilities/style_dict.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.560204 tablate-0.0.6/tablate/api/functions/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 22:41:07.000000 tablate-0.0.6/tablate/api/functions/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 00:16:43.000000 tablate-0.0.6/tablate/api/functions/concat.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.562204 tablate-0.0.6/tablate/characters/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 01:14:04.000000 tablate-0.0.6/tablate/characters/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      378 2023-07-16 22:19:15.000000 tablate-0.0.6/tablate/characters/corners.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       89 2023-07-16 22:19:15.000000 tablate-0.0.6/tablate/characters/line_h.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      108 2023-07-20 01:11:40.000000 tablate-0.0.6/tablate/characters/line_v.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2343 2023-07-19 23:07:53.000000 tablate-0.0.6/tablate/characters/matrix_cross.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      965 2023-07-16 22:19:15.000000 tablate-0.0.6/tablate/characters/matrix_side.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.562204 tablate-0.0.6/tablate/helpers/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 01:14:04.000000 tablate-0.0.6/tablate/helpers/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.563204 tablate-0.0.6/tablate/helpers/calcs/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 22:51:23.000000 tablate-0.0.6/tablate/helpers/calcs/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      769 2023-07-21 00:44:07.000000 tablate-0.0.6/tablate/helpers/calcs/calc_column_percent.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2589 2023-07-19 01:22:54.000000 tablate-0.0.6/tablate/helpers/calcs/calc_column_widths.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      587 2023-07-19 21:45:43.000000 tablate-0.0.6/tablate/helpers/calcs/get_row_colspan.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      150 2023-07-19 22:13:11.000000 tablate-0.0.6/tablate/helpers/calcs/random_string.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.563204 tablate-0.0.6/tablate/helpers/checkers/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:34:30.000000 tablate-0.0.6/tablate/helpers/checkers/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       89 2023-07-16 05:52:57.000000 tablate-0.0.6/tablate/helpers/checkers/is_last_element.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.564204 tablate-0.0.6/tablate/helpers/formatters/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:38:58.000000 tablate-0.0.6/tablate/helpers/formatters/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.565204 tablate-0.0.6/tablate/helpers/formatters/console/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:58:20.000000 tablate-0.0.6/tablate/helpers/formatters/console/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     4579 2023-07-20 08:05:59.000000 tablate-0.0.6/tablate/helpers/formatters/console/cell_string.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      539 2023-07-20 09:59:11.000000 tablate-0.0.6/tablate/helpers/formatters/console/row_border.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3160 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/formatters/console/row_divider.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.565204 tablate-0.0.6/tablate/helpers/formatters/html/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:38:58.000000 tablate-0.0.6/tablate/helpers/formatters/html/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.565204 tablate-0.0.6/tablate/helpers/formatters/html/element/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-20 11:42:52.000000 tablate-0.0.6/tablate/helpers/formatters/html/element/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      721 2023-07-22 12:23:41.000000 tablate-0.0.6/tablate/helpers/formatters/html/element/column.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      490 2023-07-22 12:23:41.000000 tablate-0.0.6/tablate/helpers/formatters/html/element/frame.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      115 2023-07-22 11:20:40.000000 tablate-0.0.6/tablate/helpers/formatters/html/element/row.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      279 2023-07-22 12:23:41.000000 tablate-0.0.6/tablate/helpers/formatters/html/element/text.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.566204 tablate-0.0.6/tablate/helpers/formatters/html/style/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-20 11:43:30.000000 tablate-0.0.6/tablate/helpers/formatters/html/style/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      416 2023-07-19 23:18:14.000000 tablate-0.0.6/tablate/helpers/formatters/html/style/border_style.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.566204 tablate-0.0.6/tablate/helpers/formatters/html/style/elements/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:02:02.000000 tablate-0.0.6/tablate/helpers/formatters/html/style/elements/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      710 2023-07-22 12:23:41.000000 tablate-0.0.6/tablate/helpers/formatters/html/style/elements/column_style.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      515 2023-07-22 12:23:41.000000 tablate-0.0.6/tablate/helpers/formatters/html/style/elements/frame_style.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      764 2023-07-22 12:24:01.000000 tablate-0.0.6/tablate/helpers/formatters/html/style/elements/text_style.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.567204 tablate-0.0.6/tablate/helpers/renderers/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 22:51:33.000000 tablate-0.0.6/tablate/helpers/renderers/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.567204 tablate-0.0.6/tablate/helpers/renderers/console/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:40:13.000000 tablate-0.0.6/tablate/helpers/renderers/console/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.568204 tablate-0.0.6/tablate/helpers/renderers/console/frames/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-20 06:15:27.000000 tablate-0.0.6/tablate/helpers/renderers/console/frames/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2113 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/console/frames/render_console_columns.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2530 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/console/frames/render_console_frame_grid.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3869 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/console/frames/render_string_frame_table.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1936 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/console/frames/render_string_frame_text.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      765 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/console/render_console.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      800 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/console/render_console_foot.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2320 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/console/render_console_frames.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      777 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/console/render_console_head.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.569204 tablate-0.0.6/tablate/helpers/renderers/html/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:40:21.000000 tablate-0.0.6/tablate/helpers/renderers/html/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.569204 tablate-0.0.6/tablate/helpers/renderers/html/frames/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3028 2023-07-22 12:45:12.000000 tablate-0.0.6/tablate/helpers/renderers/html/frames/render_html_columns.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     6154 2023-07-22 12:23:41.000000 tablate-0.0.6/tablate/helpers/renderers/html/frames/render_html_table_body.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2536 2023-07-22 12:50:37.000000 tablate-0.0.6/tablate/helpers/renderers/html/frames/render_html_text.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1267 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/html/render_html.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       51 2023-07-19 21:52:25.000000 tablate-0.0.6/tablate/helpers/renderers/html/render_html_foot.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1696 2023-07-22 12:48:53.000000 tablate-0.0.6/tablate/helpers/renderers/html/render_html_frames.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1779 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/helpers/renderers/html/render_html_head.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.569204 tablate-0.0.6/tablate/helpers/validators/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 22:51:45.000000 tablate-0.0.6/tablate/helpers/validators/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.570204 tablate-0.0.6/tablate/tests/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 00:41:48.000000 tablate-0.0.6/tablate/tests/__init__.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.571204 tablate-0.0.6/tablate/tests/playpen/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 00:20:57.000000 tablate-0.0.6/tablate/tests/playpen/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      335 2023-07-21 12:33:50.000000 tablate-0.0.6/tablate/tests/playpen/class.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      516 2023-07-22 01:36:08.000000 tablate-0.0.6/tablate/tests/playpen/class_0.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      170 2023-07-21 11:38:53.000000 tablate-0.0.6/tablate/tests/playpen/class_1.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      171 2023-07-21 10:41:14.000000 tablate-0.0.6/tablate/tests/playpen/class_2.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3569 2023-07-22 12:51:12.000000 tablate-0.0.6/tablate/tests/test_defs.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     8057 2023-07-20 00:01:38.000000 tablate-0.0.6/tablate/tests/test_objs.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       74 2023-07-22 05:05:56.000000 tablate-0.0.6/tablate/tests/test_out_html.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       66 2023-07-21 00:20:53.000000 tablate-0.0.6/tablate/tests/test_out_text.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      955 2023-07-22 04:54:36.000000 tablate-0.0.6/tablate/tests/test_styles.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.572204 tablate-0.0.6/tablate/type/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-20 07:43:04.000000 tablate-0.0.6/tablate/type/__init__.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      414 2023-07-20 10:49:54.000000 tablate-0.0.6/tablate/type/primitives.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2385 2023-07-22 10:49:03.000000 tablate-0.0.6/tablate/type/type_frame.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      156 2023-07-22 12:45:12.000000 tablate-0.0.6/tablate/type/type_html.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      626 2023-07-20 23:50:14.000000 tablate-0.0.6/tablate/type/type_input.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      714 2023-07-22 01:36:07.000000 tablate-0.0.6/tablate/type/type_options.py
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1024 2023-07-22 08:41:42.000000 tablate-0.0.6/tablate/type/type_style.py
-drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:55:58.557204 tablate-0.0.6/tablate.egg-info/
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      509 2023-07-22 12:55:58.000000 tablate-0.0.6/tablate.egg-info/PKG-INFO
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     4411 2023-07-22 12:55:58.000000 tablate-0.0.6/tablate.egg-info/SOURCES.txt
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        1 2023-07-22 12:55:58.000000 tablate-0.0.6/tablate.egg-info/dependency_links.txt
--rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        8 2023-07-22 12:55:58.000000 tablate-0.0.6/tablate.egg-info/top_level.txt
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.493357 tablate-0.0.7/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1069 2023-07-13 22:13:22.000000 tablate-0.0.7/LICENCE
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      553 2023-07-23 05:01:03.493357 tablate-0.0.7/PKG-INFO
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 00:33:05.000000 tablate-0.0.7/README.md
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      627 2023-07-23 05:00:53.000000 tablate-0.0.7/pyproject.toml
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       38 2023-07-23 05:01:03.494356 tablate-0.0.7/setup.cfg
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.470357 tablate-0.0.7/tablate/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      366 2023-07-23 04:53:06.000000 tablate-0.0.7/tablate/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.471356 tablate-0.0.7/tablate/api/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     7168 2023-07-23 04:59:42.000000 tablate-0.0.7/tablate/api/Tablate.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 22:41:07.000000 tablate-0.0.7/tablate/api/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.471356 tablate-0.0.7/tablate/api/functions/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 04:48:05.000000 tablate-0.0.7/tablate/api/functions/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1015 2023-07-23 04:56:02.000000 tablate-0.0.7/tablate/api/functions/concat.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.472357 tablate-0.0.7/tablate/api/modules/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2147 2023-07-23 04:24:03.000000 tablate-0.0.7/tablate/api/modules/Grid.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3763 2023-07-23 04:24:03.000000 tablate-0.0.7/tablate/api/modules/Table.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2063 2023-07-23 04:24:03.000000 tablate-0.0.7/tablate/api/modules/Text.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 01:25:25.000000 tablate-0.0.7/tablate/api/modules/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.472357 tablate-0.0.7/tablate/classes/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 22:53:19.000000 tablate-0.0.7/tablate/classes/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.473357 tablate-0.0.7/tablate/classes/bases/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1736 2023-07-23 04:41:22.000000 tablate-0.0.7/tablate/classes/bases/TablateApi.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      172 2023-07-23 02:12:14.000000 tablate-0.0.7/tablate/classes/bases/TablateBase.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1316 2023-07-23 04:52:22.000000 tablate-0.0.7/tablate/classes/bases/TablateSet.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 22:25:16.000000 tablate-0.0.7/tablate/classes/bases/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.473357 tablate-0.0.7/tablate/classes/options/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 22:41:07.000000 tablate-0.0.7/tablate/classes/options/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.473357 tablate-0.0.7/tablate/classes/options/html/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 13:24:20.000000 tablate-0.0.7/tablate/classes/options/html/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.473357 tablate-0.0.7/tablate/classes/options/html/style/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     4529 2023-07-23 04:41:22.000000 tablate-0.0.7/tablate/classes/options/html/style/StyleCss.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 13:24:20.000000 tablate-0.0.7/tablate/classes/options/html/style/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.474357 tablate-0.0.7/tablate/classes/options/html/style/mixins/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      508 2023-07-22 10:49:03.000000 tablate-0.0.7/tablate/classes/options/html/style/mixins/AddStyleMixin.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      515 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/classes/options/html/style/mixins/ClassNameMixin.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 01:07:40.000000 tablate-0.0.7/tablate/classes/options/html/style/mixins/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.475356 tablate-0.0.7/tablate/classes/options/html/style/subclasses/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2399 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/classes/options/html/style/subclasses/ElementStyle.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      583 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/classes/options/html/style/subclasses/TableStyle.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      674 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/classes/options/html/style/subclasses/TextStyle.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 13:24:20.000000 tablate-0.0.7/tablate/classes/options/html/style/subclasses/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.477357 tablate-0.0.7/tablate/classes/options/html/style/utilities/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-21 15:13:12.000000 tablate-0.0.7/tablate/classes/options/html/style/utilities/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      231 2023-07-22 10:49:03.000000 tablate-0.0.7/tablate/classes/options/html/style/utilities/base_names.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2281 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/classes/options/html/style/utilities/css_factory.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      876 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/classes/options/html/style/utilities/selectors.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      881 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/classes/options/html/style/utilities/style_dict.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.477357 tablate-0.0.7/tablate/library/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 01:14:04.000000 tablate-0.0.7/tablate/library/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.477357 tablate-0.0.7/tablate/library/calcs/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 22:51:23.000000 tablate-0.0.7/tablate/library/calcs/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      801 2023-07-23 04:58:20.000000 tablate-0.0.7/tablate/library/calcs/calc_column_percent.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2599 2023-07-23 04:37:08.000000 tablate-0.0.7/tablate/library/calcs/calc_column_widths.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      587 2023-07-19 21:45:43.000000 tablate-0.0.7/tablate/library/calcs/get_row_colspan.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      150 2023-07-23 04:37:08.000000 tablate-0.0.7/tablate/library/calcs/random_string.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.478356 tablate-0.0.7/tablate/library/chars/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-16 01:14:04.000000 tablate-0.0.7/tablate/library/chars/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      378 2023-07-16 22:19:15.000000 tablate-0.0.7/tablate/library/chars/corners.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       89 2023-07-16 22:19:15.000000 tablate-0.0.7/tablate/library/chars/line_h.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      108 2023-07-20 01:11:40.000000 tablate-0.0.7/tablate/library/chars/line_v.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2343 2023-07-19 23:07:53.000000 tablate-0.0.7/tablate/library/chars/matrix_cross.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      965 2023-07-16 22:19:15.000000 tablate-0.0.7/tablate/library/chars/matrix_side.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.479357 tablate-0.0.7/tablate/library/checkers/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:34:30.000000 tablate-0.0.7/tablate/library/checkers/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       89 2023-07-16 05:52:57.000000 tablate-0.0.7/tablate/library/checkers/is_last_element.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.479357 tablate-0.0.7/tablate/library/formatters/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:38:58.000000 tablate-0.0.7/tablate/library/formatters/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.480357 tablate-0.0.7/tablate/library/formatters/console/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:58:20.000000 tablate-0.0.7/tablate/library/formatters/console/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     4579 2023-07-20 08:05:59.000000 tablate-0.0.7/tablate/library/formatters/console/cell_string.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      545 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/formatters/console/row_border.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3107 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/formatters/console/row_divider.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.480357 tablate-0.0.7/tablate/library/formatters/html/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:38:58.000000 tablate-0.0.7/tablate/library/formatters/html/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.481356 tablate-0.0.7/tablate/library/formatters/html/element/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-20 11:42:52.000000 tablate-0.0.7/tablate/library/formatters/html/element/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      717 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/formatters/html/element/column.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      486 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/formatters/html/element/frame.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      115 2023-07-22 11:20:40.000000 tablate-0.0.7/tablate/library/formatters/html/element/row.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      275 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/formatters/html/element/text.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.481356 tablate-0.0.7/tablate/library/formatters/html/style/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-20 11:43:30.000000 tablate-0.0.7/tablate/library/formatters/html/style/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      416 2023-07-19 23:18:14.000000 tablate-0.0.7/tablate/library/formatters/html/style/border_style.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.481356 tablate-0.0.7/tablate/library/formatters/html/style/elements/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 12:02:02.000000 tablate-0.0.7/tablate/library/formatters/html/style/elements/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      706 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/formatters/html/style/elements/column_style.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      389 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/formatters/html/style/elements/frame_style.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      734 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/formatters/html/style/elements/text_style.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.482357 tablate-0.0.7/tablate/library/initializers/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2111 2023-07-23 04:24:03.000000 tablate-0.0.7/tablate/library/initializers/grid_init.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3653 2023-07-23 03:30:08.000000 tablate-0.0.7/tablate/library/initializers/table_init.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      917 2023-07-23 04:37:08.000000 tablate-0.0.7/tablate/library/initializers/text_init.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.483357 tablate-0.0.7/tablate/library/renderers/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 22:51:33.000000 tablate-0.0.7/tablate/library/renderers/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.484356 tablate-0.0.7/tablate/library/renderers/console/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:40:13.000000 tablate-0.0.7/tablate/library/renderers/console/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.486357 tablate-0.0.7/tablate/library/renderers/console/frames/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-20 06:15:27.000000 tablate-0.0.7/tablate/library/renderers/console/frames/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2039 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/renderers/console/frames/render_console_columns.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2490 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/renderers/console/frames/render_console_frame_grid.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3829 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/renderers/console/frames/render_string_frame_table.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1893 2023-07-23 04:37:08.000000 tablate-0.0.7/tablate/library/renderers/console/frames/render_string_frame_text.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      765 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/renderers/console/render_console.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      803 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/renderers/console/render_console_foot.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2320 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/renderers/console/render_console_frames.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      780 2023-07-22 22:49:28.000000 tablate-0.0.7/tablate/library/renderers/console/render_console_head.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.488356 tablate-0.0.7/tablate/library/renderers/html/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 03:40:21.000000 tablate-0.0.7/tablate/library/renderers/html/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.489357 tablate-0.0.7/tablate/library/renderers/html/frames/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3024 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/renderers/html/frames/render_html_columns.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     6150 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/renderers/html/frames/render_html_table_body.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2532 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/library/renderers/html/frames/render_html_text.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1340 2023-07-23 04:41:22.000000 tablate-0.0.7/tablate/library/renderers/html/render_html.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       51 2023-07-19 21:52:25.000000 tablate-0.0.7/tablate/library/renderers/html/render_html_foot.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1698 2023-07-23 04:41:22.000000 tablate-0.0.7/tablate/library/renderers/html/render_html_frames.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1797 2023-07-23 04:41:22.000000 tablate-0.0.7/tablate/library/renderers/html/render_html_head.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.489357 tablate-0.0.7/tablate/library/validators/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-18 22:51:45.000000 tablate-0.0.7/tablate/library/validators/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.491356 tablate-0.0.7/tablate/tests/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-22 00:41:48.000000 tablate-0.0.7/tablate/tests/__init__.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.491356 tablate-0.0.7/tablate/tests/playpen/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      303 2023-07-23 02:37:58.000000 tablate-0.0.7/tablate/tests/playpen/func_sigs.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      362 2023-07-23 04:53:06.000000 tablate-0.0.7/tablate/tests/test_api_table.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     3569 2023-07-22 12:51:12.000000 tablate-0.0.7/tablate/tests/test_defs.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     8000 2023-07-22 23:55:35.000000 tablate-0.0.7/tablate/tests/test_objs.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       74 2023-07-22 22:51:46.000000 tablate-0.0.7/tablate/tests/test_out_html.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)       66 2023-07-21 00:20:53.000000 tablate-0.0.7/tablate/tests/test_out_text.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      951 2023-07-22 23:05:00.000000 tablate-0.0.7/tablate/tests/test_styles.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.493357 tablate-0.0.7/tablate/type/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-20 07:43:04.000000 tablate-0.0.7/tablate/type/__init__.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      414 2023-07-20 10:49:54.000000 tablate-0.0.7/tablate/type/primitives.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      312 2023-07-23 04:56:17.000000 tablate-0.0.7/tablate/type/type_class.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     2370 2023-07-23 04:37:08.000000 tablate-0.0.7/tablate/type/type_frame.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      156 2023-07-22 12:45:12.000000 tablate-0.0.7/tablate/type/type_html.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      626 2023-07-20 23:50:14.000000 tablate-0.0.7/tablate/type/type_input.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      725 2023-07-23 04:41:22.000000 tablate-0.0.7/tablate/type/type_options.py
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     1024 2023-07-22 08:41:42.000000 tablate-0.0.7/tablate/type/type_style.py
+drwxr-xr-x   0 guydewinton  (1000) guydewinton  (1000)        0 2023-07-23 05:01:03.470357 tablate-0.0.7/tablate.egg-info/
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)      553 2023-07-23 05:01:03.000000 tablate-0.0.7/tablate.egg-info/PKG-INFO
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)     4529 2023-07-23 05:01:03.000000 tablate-0.0.7/tablate.egg-info/SOURCES.txt
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        1 2023-07-23 05:01:03.000000 tablate-0.0.7/tablate.egg-info/dependency_links.txt
+-rw-r--r--   0 guydewinton  (1000) guydewinton  (1000)        8 2023-07-23 05:01:03.000000 tablate-0.0.7/tablate.egg-info/top_level.txt
```

### Comparing `tablate-0.0.6/LICENCE` & `tablate-0.0.7/LICENCE`

 * *Files identical despite different names*

### Comparing `tablate-0.0.6/tablate/api/Tablate.py` & `tablate-0.0.7/tablate/api/Tablate.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,23 +1,21 @@
-import copy
-import shutil
 from typing import List, Dict, Optional, Union
 
-from tablate.helpers.calcs.calc_column_widths import calc_column_widths
-from tablate.helpers.renderers.console.render_console import render_console
-from tablate.helpers.renderers.html.render_html import render_html
-from tablate.type.type_frame import TextFrameDict, GridFrameDict, TableRowsFrameDict, \
-    TableHeadColumnFrameDict, TableRowsColumnFrameDict, TableHeadFrameDict, FrameDictList
-from tablate.type.type_options import Options
+from tablate.classes.bases.TablateApi import TablateApi
+from tablate.library.initializers.grid_init import grid_init
+from tablate.library.initializers.table_init import table_init
+from tablate.library.initializers.text_init import text_init
+from tablate.library.renderers.console.render_console import render_console
+from tablate.library.renderers.html.render_html import render_html
 from tablate.type.type_input import GridInputColumnDict, TableInputColumnDict
 from tablate.type.primitives import Border, BaseDivider, TextAlignment, ColumnDivider, HeaderAlignment, \
     HeaderColumnDivider
 
 
-class Tablate:
+class Tablate(TablateApi):
 
     # todo: maybe allow align/padding/frame_divider defaults in constructor??
     # todo: allow frame names (will make TextFrame iPython friendly) -- also constructor options `show_frame_names` & `frame_name_align`
     # todo: allow cell level definition of padding/v_line/trunc_value in `add_` constructor objects??? => a lot of fuss and complication for marginal use... v_lines might be useful...
 
     # todo: text styles / colours
 
@@ -30,97 +28,62 @@
                  frame_divider: BaseDivider = "thick",
                  frame_width: int = None,
                  html_px_size: int = 6,
                  html_text_size: int = 12,
                  html_frame_width: str = "100%",
                  html_css_injection: str = "") -> None:
 
-        self._options: Options = {
-            "common": {
-                "border_style": border_style,
-                "frame_padding": frame_padding,
-                "frame_divider": frame_divider,
-                "frame_width": frame_width if frame_width else shutil.get_terminal_size((120 + (frame_padding * 2), 0))[
-                                                                   0] - (frame_padding * 2)
-            },
-            "html": {
-                "px_size": html_px_size,
-                "text_size": html_text_size,
-                "width": html_frame_width,
-            }
-        }
-
-        self._frame_list: FrameDictList = []
+        super().__init__(border_style=border_style,
+                         frame_padding=frame_padding,
+                         frame_divider=frame_divider,
+                         frame_width=frame_width,
+                         html_px_size=html_px_size,
+                         html_text_size=html_text_size,
+                         html_frame_width=html_frame_width,
+                         html_css_injection=html_css_injection)
 
     def add_text_frame(self,
                        text: Union[str, int, float],
                        multiline: bool = True,
                        max_lines: Optional[int] = None,
                        text_align: TextAlignment = "left",
                        text_padding: int = 1,
                        frame_base_divider: BaseDivider = "thick",
                        trunc_value: str = "...") -> None:
 
-        text_frame_dict: TextFrameDict = {
-            "type": "text",
-            "column_list": [{"width": self._options["common"]["frame_width"] - 2, "divider": "blank"}],
-            "string": text,
-            "base_divider": frame_base_divider,
-            "max_lines": max_lines,
-            "align": text_align,
-            "padding": text_padding,
-            "trunc_value": trunc_value,
-            "multiline": multiline,
-        }
+        text_dict = text_init(text=text,
+                              multiline=multiline,
+                              max_lines=max_lines,
+                              text_align=text_align,
+                              text_padding=text_padding,
+                              frame_base_divider=frame_base_divider,
+                              trunc_value=trunc_value,
+                              frame_width=self._options["common"]["frame_width"])
 
-        self._frame_list.append(text_frame_dict)
+        self._frame_list.append(text_dict)
 
     def add_grid_frame(self,
                        columns: List[Union[str, GridInputColumnDict]],
                        column_padding: int = 1,
                        column_divider: ColumnDivider = "thin",
                        frame_base_divider: BaseDivider = "thick",
                        multiline: bool = True,
                        max_lines: int = None,
                        trunc_value: str = "...") -> None:
 
-        columns = copy.deepcopy(columns)
-
-        grid_column_list = []
-
-        for grid_column_item in columns:
-            if type(grid_column_item) == str:
-                grid_column_list.append({
-                    "divider": self._options["common"]["frame_divider"],
-                    "string": grid_column_item,
-                    "align": "left",
-                    "padding": column_padding,
-                    "trunc_value": trunc_value,
-                })
-            elif type(grid_column_item) == dict:
-                grid_column_item["string"] = grid_column_item["string"]
-                grid_column_item["divider"] = column_divider if "divider" not in grid_column_item else grid_column_item["divider"]
-                grid_column_item["align"] = grid_column_item["align"] if "align" in grid_column_item else "left"
-                grid_column_item["padding"] = column_padding
-                grid_column_item["trunc_value"] = trunc_value
-                if "width" in grid_column_item:
-                    grid_column_item["width"] = grid_column_item["width"]
-                grid_column_list.append(grid_column_item)
-
-        grid_column_list = calc_column_widths(columns=grid_column_list, frame_width=self._options["common"]["frame_width"], column_padding=column_padding)
-
-        grid_frame_dict: GridFrameDict = {
-            "type": "grid",
-            "column_list": grid_column_list,
-            "base_divider": frame_base_divider,
-            "max_lines": max_lines,
-            "multiline": multiline
-        }
+        grid_dict = grid_init(columns=columns,
+                              column_padding=column_padding,
+                              column_divider=column_divider,
+                              frame_base_divider=frame_base_divider,
+                              multiline=multiline,
+                              max_lines=max_lines,
+                              trunc_value=trunc_value,
+                              frame_width=self._options["common"]["frame_width"])
 
-        self._frame_list.append(grid_frame_dict)
+        self._frame_list.append(grid_dict)
 
     def add_table_frame(self,
                         columns: List[TableInputColumnDict],
                         rows: List[Dict[str, Union[str, int, float]]],
                         column_padding: int = 1,
                         row_line_divider: BaseDivider = "thin",
                         row_column_divider: ColumnDivider = "thin",
@@ -132,77 +95,36 @@
                         max_lines: int = None,
                         multiline_header: bool = False,
                         max_lines_header: int = None,
                         hide_header: bool = False,
                         head_trunc_value: str = ".",
                         row_trunc_value: str = "...") -> None:
 
-        columns = copy.deepcopy(columns)
-        rows = copy.deepcopy(rows)
+        table_head_dict, table_rows_dict = table_init(columns=columns,
+                                                      rows=rows,
+                                                      column_padding=column_padding,
+                                                      row_line_divider=row_line_divider,
+                                                      row_column_divider=row_column_divider,
+                                                      frame_base_divider=frame_base_divider,
+                                                      header_align=header_align,
+                                                      header_column_divider=header_column_divider,
+                                                      header_base_divider=header_base_divider,
+                                                      multiline=multiline,
+                                                      max_lines=max_lines,
+                                                      multiline_header=multiline_header,
+                                                      max_lines_header=max_lines_header,
+                                                      hide_header=hide_header,
+                                                      head_trunc_value=head_trunc_value,
+                                                      row_trunc_value=row_trunc_value,
+                                                      frame_width=self._options["common"]["frame_width"])
 
-        columns = calc_column_widths(columns=columns, frame_width=self._options["common"]["frame_width"], column_padding=column_padding)
+        if table_head_dict:
+            self._frame_list.append(table_head_dict)
 
-        header_column_list = []
-        rows_column_list = []
-
-        for column_index, column_item in enumerate(columns):
-            # todo: add optional 'value' key to the column definition... if not used will use key as value
-            column_align_out: TextAlignment = column_item["align"] if "align" in column_item else "left"
-            header_align_out: TextAlignment = header_align if header_align != "column" else column_align_out
-
-            column_divider_out: ColumnDivider = column_item["divider"] if "divider" in column_item else row_column_divider
-            header_divider_out: ColumnDivider = header_column_divider if header_column_divider != "rows" else column_divider_out
-
-            header_column_dict: TableHeadColumnFrameDict = {
-                "width": column_item["width"],
-                "divider": header_divider_out,
-                "string": column_item["key"],
-                "align": header_align_out,
-                "padding": column_padding,
-                "trunc_value": head_trunc_value,
-            }
-
-            header_column_list.append(header_column_dict)
-
-            rows_column_dict: TableRowsColumnFrameDict = {
-                "width": column_item["width"],
-                "divider": column_divider_out,
-                "key": column_item["key"],
-                "align": column_align_out,
-                "padding": column_padding,
-                "trunc_value": row_trunc_value,
-            }
-
-            rows_column_list.append(rows_column_dict)
-
-        if not hide_header:
-
-            header_frame_dict: TableHeadFrameDict = {
-                "type": "table-head",
-                "column_list": header_column_list,
-                "base_divider": header_base_divider,
-                "max_lines": max_lines_header,
-                "multiline": multiline_header
-            }
-
-            self._frame_list.append(header_frame_dict)
-
-        # todo: check row keys all in place and give nice errors => validators
-
-        rows_frame_dict: TableRowsFrameDict = {
-            "type": "table-body",
-            "column_list": rows_column_list,
-            "table_row_list": rows,
-            "row_line_divider": row_line_divider,
-            "base_divider": frame_base_divider,
-            "max_lines": max_lines,
-            "multiline": multiline
-        }
-
-        self._frame_list.append(rows_frame_dict)
+        self._frame_list.append(table_rows_dict)
 
     def to_string(self) -> str:
         return render_console(frame_list=self._frame_list, options=self._options)
 
     def print(self) -> None:
         print(self.to_string())
 
@@ -211,8 +133,7 @@
 
     def to_html(self) -> str:
         return render_html(frame_list=self._frame_list, options=self._options)
 
     def _repr_html_(self) -> str:
         return self.to_html()
 
-
```

### Comparing `tablate-0.0.6/tablate/api/classes/options/html/style/StyleCss.py` & `tablate-0.0.7/tablate/classes/options/html/style/StyleCss.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 from typing import Callable, List, Union
 
-from tablate.api.classes.options.html.style.subclasses.ElementStyle import ElementStyle
-from tablate.api.classes.options.html.style.utilities.base_names import base_class, tablate_instance_key
-from tablate.api.classes.options.html.style.utilities.style_dict import style_dict_key_builder, \
+from tablate.classes.options.html.style.subclasses.ElementStyle import ElementStyle
+from tablate.classes.options.html.style.utilities.base_names import tablate_instance_key
+from tablate.classes.options.html.style.utilities.style_dict import style_dict_key_builder, \
     style_dict_css_append
-from tablate.helpers.calcs.random_string import random_string
-from tablate.api.classes.options.html.style.utilities.css_factory import css_factory
-from tablate.api.classes.options.html.style.utilities.selectors import frame_selector, instance_selector, \
+from tablate.library.calcs.random_string import random_string
+from tablate.classes.options.html.style.utilities.css_factory import css_factory
+from tablate.classes.options.html.style.utilities.selectors import frame_selector, instance_selector, \
     base_selector_dict, table_selector, container_selector
 from tablate.type.type_style import SelectorDictUnion, ElementSelectorDictKeys, TableSelectorDictKeys
 
 
 class StyleCss:
 
     def __init__(self) -> None:
@@ -46,14 +46,17 @@
                                                               key=selector_key,
                                                               value=selector_value)
         return ElementStyle(selector=selector_dict, create_style=self.__create_style())
 
     def add_global_style_attribute(self, key: str, value: Union[str, int]):
         self.__global_styles.append(f"{key}:{value}")
 
+    def inject_css_block(self, css: str) -> None:
+        self._css_foot += css
+
     def inject_scoped_css(self, selector: str, css: str) -> None:
         scoped_selector = f"{self._base_selector} {selector}"
         css_block = scoped_selector + "{" + css + "}"
         self._css_foot += css_block
 
     def return_head_styles(self) -> str:
         return_string = ""
```

### Comparing `tablate-0.0.6/tablate/api/classes/options/html/style/mixins/ClassNameMixin.py` & `tablate-0.0.7/tablate/classes/options/html/style/mixins/ClassNameMixin.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from tablate.api.classes.options.html.style.utilities.base_names import base_class
+from tablate.classes.options.html.style.utilities.base_names import base_class
 from tablate.type.type_style import SelectorDictUnion
 
 
 class ClassNameMixin:
 
     _selector_dict: SelectorDictUnion
```

### Comparing `tablate-0.0.6/tablate/api/classes/options/html/style/subclasses/ElementStyle.py` & `tablate-0.0.7/tablate/classes/options/html/style/subclasses/ElementStyle.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from copy import copy
 from typing import Callable, Union, List
 
-from tablate.api.classes.options.html.style.mixins.AddStyleMixin import AddStyleMixin
-from tablate.api.classes.options.html.style.mixins.ClassNameMixin import ClassNameMixin
-from tablate.api.classes.options.html.style.subclasses.TextStyle import TextStyle
-from tablate.api.classes.options.html.style.utilities.selectors import column_selector, row_selector, \
-    text_selector, element_append
+from tablate.classes.options.html.style.mixins.AddStyleMixin import AddStyleMixin
+from tablate.classes.options.html.style.mixins.ClassNameMixin import ClassNameMixin
+from tablate.classes.options.html.style.subclasses.TextStyle import TextStyle
+from tablate.classes.options.html.style.utilities.selectors import column_selector, row_selector, \
+    element_append
 from tablate.type.type_style import SelectorDictUnion, ElementSelectorDict, ElementSelectorDictKeys
 
 
 class ElementStyle(ClassNameMixin, AddStyleMixin):
 
     def __init__(self,
                  selector: ElementSelectorDict,
```

### Comparing `tablate-0.0.6/tablate/api/classes/options/html/style/subclasses/TableStyle.py` & `tablate-0.0.7/tablate/classes/options/html/style/subclasses/TableStyle.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from typing import Callable, Union, List
 
-from tablate.api.classes.options.html.style.mixins.AddStyleMixin import AddStyleMixin
-from tablate.api.classes.options.html.style.mixins.ClassNameMixin import ClassNameMixin
+from tablate.classes.options.html.style.mixins.AddStyleMixin import AddStyleMixin
+from tablate.classes.options.html.style.mixins.ClassNameMixin import ClassNameMixin
 from tablate.type.type_style import TableSelectorDict, SelectorDictUnion
 
 
 class TableStyle(ClassNameMixin, AddStyleMixin):
 
     def __init__(self,
                  selector: TableSelectorDict,
```

### Comparing `tablate-0.0.6/tablate/api/classes/options/html/style/subclasses/TextStyle.py` & `tablate-0.0.7/tablate/classes/options/html/style/subclasses/TextStyle.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from typing import Callable, Union, List
 
-from tablate.api.classes.options.html.style.mixins.AddStyleMixin import AddStyleMixin
-from tablate.api.classes.options.html.style.mixins.ClassNameMixin import ClassNameMixin
+from tablate.classes.options.html.style.mixins.AddStyleMixin import AddStyleMixin
+from tablate.classes.options.html.style.mixins.ClassNameMixin import ClassNameMixin
 from tablate.type.type_style import SelectorDictUnion
 from tablate.type.primitives import TextAlignment
 
 
 class TextStyle(ClassNameMixin, AddStyleMixin):
 
     def __init__(self, selector: SelectorDictUnion,
```

### Comparing `tablate-0.0.6/tablate/api/classes/options/html/style/utilities/css_factory.py` & `tablate-0.0.7/tablate/classes/options/html/style/utilities/css_factory.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import List
 
-from tablate.api.classes.options.html.style.utilities.base_names import styles_key
+from tablate.classes.options.html.style.utilities.base_names import styles_key
 
 
 def css_factory(style_dict: dict) -> str:
 
     # def recurse_style_dict_original(style_object: dict, classname_list=None, return_list=None, i=0) -> List[str]:
     #     if return_list is None:
     #         return_list = []
```

### Comparing `tablate-0.0.6/tablate/api/classes/options/html/style/utilities/selectors.py` & `tablate-0.0.7/tablate/classes/options/html/style/utilities/selectors.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from tablate.api.classes.options.html.style.utilities.base_names import base_class, tablate_instance_key, \
+from tablate.classes.options.html.style.utilities.base_names import base_class, tablate_instance_key, \
     element_type_key
 
 
 def element_append(string: str) -> str:
     return f"{string}_element"
```

### Comparing `tablate-0.0.6/tablate/api/classes/options/html/style/utilities/style_dict.py` & `tablate-0.0.7/tablate/classes/options/html/style/utilities/style_dict.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import Union
 
-from tablate.api.classes.options.html.style.utilities.base_names import styles_key
+from tablate.classes.options.html.style.utilities.base_names import styles_key
 from tablate.type.type_style import SelectorDictUnion, SelectorDictKeysUnion
 
 
 def style_dict_key_builder(style_dict: dict, selector_dict: SelectorDictUnion, key: SelectorDictKeysUnion) -> Union[dict, list]:
     if key in selector_dict:
         if selector_dict[key] in style_dict:
             style_dict = style_dict[selector_dict[key]]
```

### Comparing `tablate-0.0.6/tablate/characters/matrix_cross.py` & `tablate-0.0.7/tablate/library/chars/matrix_cross.py`

 * *Files identical despite different names*

### Comparing `tablate-0.0.6/tablate/characters/matrix_side.py` & `tablate-0.0.7/tablate/library/chars/matrix_side.py`

 * *Files identical despite different names*

### Comparing `tablate-0.0.6/tablate/helpers/calcs/calc_column_percent.py` & `tablate-0.0.7/tablate/library/calcs/calc_column_percent.py`

 * *Files 10% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 
 def calc_column_percent(frame_list: List[T], frame_width: int) -> (List[T], List[int]):
     frame_list = copy.deepcopy(frame_list)
     baseline_width_set = set()
     frame_width = frame_width - 1
     for frame_item in frame_list:
         frame_width_total = 0
+        print(type(frame_item))
         for column_item in frame_item["column_list"]:
             frame_width_total += column_item["width"] + 1
             acc_column_width = math.floor((100 / frame_width) * frame_width_total)
             baseline_width_set.add(math.floor(acc_column_width))
             column_item["baseline_width_percent"] = acc_column_width
     sorted_baseline_array = sorted(baseline_width_set)
     return frame_list, sorted_baseline_array
```

### Comparing `tablate-0.0.6/tablate/helpers/calcs/calc_column_widths.py` & `tablate-0.0.7/tablate/library/calcs/calc_column_widths.py`

 * *Files 6% similar despite different names*

```diff
@@ -26,15 +26,15 @@
         if "width" in column_item:
             validated_value = False
             if type(column_item["width"]) == str and column_item["width"][-1] == "%":
                 try:
                     width_percentage = math.floor(frame_width / (100 / int(column_item["width"][0:-1]))) - 2
                     column_item["width"] = width_percentage
                     validated_value = True
-                except:
+                except TypeError:
                     error = True
             if type(column_item["width"]) == int:
                 if column_item["width"] < min_column_width:
                     error = True
                 total_defined_column_width += column_item["width"]
                 validated_value = True
             if not validated_value:
```

### Comparing `tablate-0.0.6/tablate/helpers/calcs/get_row_colspan.py` & `tablate-0.0.7/tablate/library/calcs/get_row_colspan.py`

 * *Files identical despite different names*

### Comparing `tablate-0.0.6/tablate/helpers/formatters/console/cell_string.py` & `tablate-0.0.7/tablate/library/formatters/console/cell_string.py`

 * *Files identical despite different names*

### Comparing `tablate-0.0.6/tablate/helpers/formatters/console/row_border.py` & `tablate-0.0.7/tablate/library/formatters/console/row_border.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from tablate.characters.line_v import v_line
-from tablate.characters.matrix_side import left_side_matrix, right_side_matrix
+from tablate.library.chars.line_v import v_line
+from tablate.library.chars.matrix_side import left_side_matrix, right_side_matrix
 from tablate.type.primitives import Border, BaseDivider
 
 
 def row_border(row_string: str, outer_border: Border, row_divider: BaseDivider = None) -> str:
     left_border = left_side_matrix[outer_border][row_divider] if row_divider else v_line[outer_border]
     right_border = right_side_matrix[outer_border][row_divider] if row_divider else v_line[outer_border]
     return f"{left_border}{row_string}{right_border}"
```

### Comparing `tablate-0.0.6/tablate/helpers/formatters/console/row_divider.py` & `tablate-0.0.7/tablate/library/formatters/console/row_divider.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,12 +1,9 @@
-import time
-
-from tablate.characters.line_h import h_line
-from tablate.characters.matrix_cross import cross_matrix
-from tablate.type.type_options import Options
+from tablate.library.chars.line_h import h_line
+from tablate.library.chars.matrix_cross import cross_matrix
 from tablate.type.primitives import BaseDivider
 
 
 def row_divider(column_list_top: list, column_list_bottom: list, divider: BaseDivider) -> str:
 
     """
     :param divider: BorderType
```

### Comparing `tablate-0.0.6/tablate/helpers/formatters/html/element/column.py` & `tablate-0.0.7/tablate/library/formatters/html/element/column.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import List
 
-from tablate.api.classes.options.html.style.subclasses.ElementStyle import ElementStyle
+from tablate.classes.options.html.style.subclasses.ElementStyle import ElementStyle
 from tablate.type.type_html import HtmlCellElement
 
 
 def html_column_head_formatter(column_styler: ElementStyle,
                                column_index: int,
                                colspans: List[int],
                                column_element: HtmlCellElement = 'td'):
```

### Comparing `tablate-0.0.6/tablate/helpers/formatters/html/style/elements/column_style.py` & `tablate-0.0.7/tablate/library/formatters/html/style/elements/column_style.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-from tablate.api.classes.options.html.style.subclasses.ElementStyle import ElementStyle
-from tablate.helpers.checkers.is_last_element import is_last_element
-from tablate.helpers.formatters.html.style.border_style import border_line
+from tablate.classes.options.html.style.subclasses.ElementStyle import ElementStyle
+from tablate.library.checkers.is_last_element import is_last_element
+from tablate.library.formatters.html.style.border_style import border_line
 from tablate.type.type_frame import BaseFrameDict, BaseColumnDict
 
 
 def column_style(frame_dict: BaseFrameDict,
                  column_dict: BaseColumnDict,
                  column_styler: ElementStyle,
                  column_index: int) -> None:
```

### Comparing `tablate-0.0.6/tablate/helpers/formatters/html/style/elements/text_style.py` & `tablate-0.0.7/tablate/library/formatters/html/style/elements/text_style.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,8 @@
-from typing import Union
-
-from tablate.api.classes.options.html.style.subclasses.TextStyle import TextStyle
+from tablate.classes.options.html.style.subclasses.TextStyle import TextStyle
 from tablate.type.primitives import TextAlignment
 
 
 def text_style(text_styler: TextStyle, align: TextAlignment, padding: int, multiline: bool, max_lines: int = None) -> None:
 
     text_styler.add_style_attribute("display", "-webkit-box")
     text_styler.add_style_attribute("-webkit-box-orient", "vertical")
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/console/frames/render_console_columns.py` & `tablate-0.0.7/tablate/library/renderers/console/frames/render_console_columns.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,16 +1,15 @@
-from typing import List, Optional
+from typing import List
 
-from tablate.characters.line_v import v_line
-from tablate.helpers.checkers.is_last_element import is_last_element
-from tablate.helpers.formatters.console.cell_string import cell_string_multi_line, cell_string_single_line
-from tablate.helpers.formatters.console.row_border import row_border
+from tablate.library.chars.line_v import v_line
+from tablate.library.checkers.is_last_element import is_last_element
+from tablate.library.formatters.console.cell_string import cell_string_single_line
+from tablate.library.formatters.console.row_border import row_border
 from tablate.type.type_frame import BaseFrameDict
 from tablate.type.type_options import Options
-from tablate.type.primitives import Border
 
 
 def column_console_multiline(formatted_columns_array: List[List[str]], frame_dict: BaseFrameDict, options: Options):
 
     frame_padding = options["common"]["frame_padding"]
     frame_border = options["common"]["border_style"]
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/console/frames/render_console_frame_grid.py` & `tablate-0.0.7/tablate/library/renderers/console/frames/render_console_frame_grid.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 
-from tablate.characters.line_v import v_line
-from tablate.helpers.checkers.is_last_element import is_last_element
-from tablate.helpers.formatters.console.cell_string import cell_string_single_line, cell_string_multi_line
-from tablate.helpers.renderers.console.frames.render_console_columns import column_console_multiline
-from tablate.helpers.formatters.console.row_border import row_border
+from tablate.library.chars.line_v import v_line
+from tablate.library.checkers.is_last_element import is_last_element
+from tablate.library.formatters.console.cell_string import cell_string_single_line, cell_string_multi_line
+from tablate.library.renderers.console.frames.render_console_columns import column_console_multiline
+from tablate.library.formatters.console.row_border import row_border
 from tablate.type.type_frame import GridFrameDict
 from tablate.type.type_options import Options
-from tablate.type.primitives import Border
 
 
 def render_console_single_line_grid(grid_frame_dict: GridFrameDict, options: Options):
 
     frame_padding = options["common"]["frame_padding"]
     frame_border = options["common"]["border_style"]
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/console/frames/render_string_frame_table.py` & `tablate-0.0.7/tablate/library/renderers/console/frames/render_string_frame_table.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,16 +1,15 @@
-from tablate.characters.line_v import v_line
-from tablate.helpers.checkers.is_last_element import is_last_element
-from tablate.helpers.formatters.console.cell_string import cell_string_single_line, cell_string_multi_line
-from tablate.helpers.renderers.console.frames.render_console_columns import column_console_multiline
-from tablate.helpers.formatters.console.row_divider import row_divider
-from tablate.helpers.formatters.console.row_border import row_border
+from tablate.library.chars.line_v import v_line
+from tablate.library.checkers.is_last_element import is_last_element
+from tablate.library.formatters.console.cell_string import cell_string_single_line, cell_string_multi_line
+from tablate.library.renderers.console.frames.render_console_columns import column_console_multiline
+from tablate.library.formatters.console.row_divider import row_divider
+from tablate.library.formatters.console.row_border import row_border
 from tablate.type.type_frame import TableRowsFrameDict
 from tablate.type.type_options import Options
-from tablate.type.primitives import Border
 
 
 def render_console_table_frame(table_frame_dict: TableRowsFrameDict, options: Options) -> str:
 
     frame_padding = options["common"]["frame_padding"]
     frame_border = options["common"]["border_style"]
 
@@ -21,15 +20,15 @@
         line_divider_row_string = row_divider(divider=table_frame_dict["row_line_divider"],
                                               column_list_top=table_frame_dict["column_list"],
                                               column_list_bottom=table_frame_dict["column_list"])
         line_divider_inner_string = row_border(row_string=line_divider_row_string, outer_border=frame_border, row_divider=table_frame_dict["row_line_divider"])
         line_divider_string = f"{' ' * frame_padding}{line_divider_inner_string}\n"
 
     for row_index, row_item in enumerate(table_frame_dict["table_row_list"]):
-        if table_frame_dict["multiline"] == False or table_frame_dict["max_lines"] == 1:
+        if table_frame_dict["multiline"] is False or table_frame_dict["max_lines"] == 1:
             row_line_string = ""
             for column_index, column_item in enumerate(table_frame_dict["column_list"]):
                 row_line_string += cell_string_single_line(string=row_item[column_item["key"]],
                                                            width=column_item["width"],
                                                            padding=column_item["padding"],
                                                            align=column_item["align"],
                                                            trunc_value=column_item["trunc_value"])
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/console/frames/render_string_frame_text.py` & `tablate-0.0.7/tablate/library/renderers/console/frames/render_string_frame_text.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,12 +1,11 @@
-from tablate.helpers.formatters.console.cell_string import cell_string_multi_line, cell_string_single_line
-from tablate.helpers.formatters.console.row_border import row_border
+from tablate.library.formatters.console.cell_string import cell_string_multi_line, cell_string_single_line
+from tablate.library.formatters.console.row_border import row_border
 from tablate.type.type_frame import TextFrameDict
 from tablate.type.type_options import Options
-from tablate.type.primitives import Border
 
 
 def render_console_text_frame(text_frame_dict: TextFrameDict, options: Options) -> str:
 
     frame_padding = options["common"]["frame_padding"]
     frame_border = options["common"]["border_style"]
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/console/render_console.py` & `tablate-0.0.7/tablate/library/renderers/console/render_console.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
-from tablate.helpers.renderers.console.render_console_foot import render_console_foot
-from tablate.helpers.renderers.console.render_console_frames import render_console_frames
-from tablate.helpers.renderers.console.render_console_head import render_console_head
+from tablate.library.renderers.console.render_console_foot import render_console_foot
+from tablate.library.renderers.console.render_console_frames import render_console_frames
+from tablate.library.renderers.console.render_console_head import render_console_head
 from tablate.type.type_frame import FrameDictList
 from tablate.type.type_options import Options
 
 
 def render_console(frame_list: FrameDictList, options: Options) -> str:
     return_string = ""
     if len(frame_list) > 0:
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/console/render_console_foot.py` & `tablate-0.0.7/tablate/library/renderers/console/render_console_foot.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from tablate.characters.corners import bottom_left, bottom_right
-from tablate.helpers.formatters.console.row_divider import row_divider
+from tablate.library.chars.corners import bottom_left, bottom_right
+from tablate.library.formatters.console.row_divider import row_divider
 from tablate.type.type_frame import FrameDictList
 from tablate.type.type_options import Options
 
 
 def render_console_foot(frame_list: FrameDictList, options: Options) -> str:
 
     return_string = ""
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/console/render_console_frames.py` & `tablate-0.0.7/tablate/library/renderers/console/render_console_frames.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,14 @@
-from tablate.helpers.checkers.is_last_element import is_last_element
-from tablate.helpers.formatters.console.row_divider import row_divider
-from tablate.helpers.formatters.console.row_border import row_border
-from tablate.helpers.renderers.console.frames.render_console_frame_grid import render_console_single_line_grid, \
+from tablate.library.checkers.is_last_element import is_last_element
+from tablate.library.formatters.console.row_divider import row_divider
+from tablate.library.formatters.console.row_border import row_border
+from tablate.library.renderers.console.frames.render_console_frame_grid import render_console_single_line_grid, \
     render_console_multi_line_grid
-from tablate.helpers.renderers.console.frames.render_string_frame_table import render_console_table_frame
-from tablate.helpers.renderers.console.frames.render_string_frame_text import render_console_text_frame
+from tablate.library.renderers.console.frames.render_string_frame_table import render_console_table_frame
+from tablate.library.renderers.console.frames.render_string_frame_text import render_console_text_frame
 from tablate.type.type_frame import FrameDictList
 from tablate.type.type_options import Options
 
 
 def render_console_frames(frame_list: FrameDictList, options: Options) -> str:
 
     return_string = ""
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/console/render_console_head.py` & `tablate-0.0.7/tablate/library/renderers/console/render_console_head.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,9 @@
-from tablate.characters.corners import top_left, top_right
-from tablate.helpers.formatters.console.row_divider import row_divider
+from tablate.library.chars.corners import top_left, top_right
+from tablate.library.formatters.console.row_divider import row_divider
 from tablate.type.type_frame import FrameDictList
 from tablate.type.type_options import Options
 
 
 def render_console_head(frame_list: FrameDictList, options: Options) -> str:
 
     return_string = ""
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/html/frames/render_html_columns.py` & `tablate-0.0.7/tablate/library/renderers/html/frames/render_html_columns.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,16 +1,16 @@
-from tablate.api.classes.options.html.style.subclasses.ElementStyle import ElementStyle
-from tablate.helpers.calcs.get_row_colspan import get_row_colspans
-from tablate.helpers.formatters.html.element.column import html_column_head_formatter, html_column_foot_formatter
-from tablate.helpers.formatters.html.element.frame import html_frame_head_formatter, html_frame_foot_formatter
-from tablate.helpers.formatters.html.element.row import html_row_head_formatter, html_row_foot_formatter
-from tablate.helpers.formatters.html.element.text import html_text_formatter
-from tablate.helpers.formatters.html.style.elements.column_style import column_style
-from tablate.helpers.formatters.html.style.elements.frame_style import frame_style
-from tablate.helpers.formatters.html.style.elements.text_style import text_style
+from tablate.classes.options.html.style.subclasses.ElementStyle import ElementStyle
+from tablate.library.calcs.get_row_colspan import get_row_colspans
+from tablate.library.formatters.html.element.column import html_column_head_formatter, html_column_foot_formatter
+from tablate.library.formatters.html.element.frame import html_frame_head_formatter, html_frame_foot_formatter
+from tablate.library.formatters.html.element.row import html_row_head_formatter, html_row_foot_formatter
+from tablate.library.formatters.html.element.text import html_text_formatter
+from tablate.library.formatters.html.style.elements.column_style import column_style
+from tablate.library.formatters.html.style.elements.frame_style import frame_style
+from tablate.library.formatters.html.style.elements.text_style import text_style
 from tablate.type.type_frame import BaseFrameDict
 from tablate.type.type_html import HtmlFrameType, HtmlRowGroupElement, HtmlCellElement
 from tablate.type.type_options import Options
 
 
 def render_html_column(frame_dict: BaseFrameDict, options: Options, frame_styler: ElementStyle, frame_type: HtmlFrameType = "body") -> str:
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/html/frames/render_html_table_body.py` & `tablate-0.0.7/tablate/library/renderers/html/frames/render_html_table_body.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,18 +1,18 @@
-from tablate.api.classes.options.html.style.subclasses.ElementStyle import ElementStyle
-from tablate.helpers.formatters.html.element.column import html_column_head_formatter, html_column_foot_formatter
-from tablate.helpers.formatters.html.element.frame import html_frame_head_formatter, html_frame_foot_formatter
-from tablate.helpers.formatters.html.element.row import html_row_head_formatter, html_row_foot_formatter
-from tablate.helpers.formatters.html.element.text import html_text_formatter
-from tablate.helpers.formatters.html.style.elements.column_style import column_style
-from tablate.helpers.formatters.html.style.elements.frame_style import frame_style
-from tablate.helpers.formatters.html.style.elements.text_style import text_style
+from tablate.classes.options.html.style.subclasses.ElementStyle import ElementStyle
+from tablate.library.formatters.html.element.column import html_column_head_formatter, html_column_foot_formatter
+from tablate.library.formatters.html.element.frame import html_frame_head_formatter, html_frame_foot_formatter
+from tablate.library.formatters.html.element.row import html_row_head_formatter, html_row_foot_formatter
+from tablate.library.formatters.html.element.text import html_text_formatter
+from tablate.library.formatters.html.style.elements.column_style import column_style
+from tablate.library.formatters.html.style.elements.frame_style import frame_style
+from tablate.library.formatters.html.style.elements.text_style import text_style
 from tablate.type.type_options import Options
 
-from tablate.helpers.calcs.get_row_colspan import get_row_colspans
+from tablate.library.calcs.get_row_colspan import get_row_colspans
 from tablate.type.type_frame import TableRowsFrameDict
 
 
 def render_html_table_body(table_body_frame_dict: TableRowsFrameDict, options: Options, frame_styler: ElementStyle):
 
     # column_baselines = options["html"]["column_baselines"]
     # html_px = options["html"]["px_size"]
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/html/frames/render_html_text.py` & `tablate-0.0.7/tablate/library/renderers/html/frames/render_html_text.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,16 @@
-from tablate.api.classes.options.html.style.subclasses.ElementStyle import ElementStyle
-from tablate.helpers.calcs.get_row_colspan import get_row_colspans
-from tablate.helpers.formatters.html.element.column import html_column_head_formatter, html_column_foot_formatter
-from tablate.helpers.formatters.html.element.frame import html_frame_head_formatter, html_frame_foot_formatter
-from tablate.helpers.formatters.html.element.row import html_row_head_formatter, html_row_foot_formatter
-from tablate.helpers.formatters.html.element.text import html_text_formatter
-from tablate.helpers.formatters.html.style.elements.column_style import column_style
-from tablate.helpers.formatters.html.style.elements.frame_style import frame_style
-from tablate.helpers.formatters.html.style.elements.text_style import text_style
+from tablate.classes.options.html.style.subclasses.ElementStyle import ElementStyle
+from tablate.library.calcs.get_row_colspan import get_row_colspans
+from tablate.library.formatters.html.element.column import html_column_head_formatter, html_column_foot_formatter
+from tablate.library.formatters.html.element.frame import html_frame_head_formatter, html_frame_foot_formatter
+from tablate.library.formatters.html.element.row import html_row_head_formatter, html_row_foot_formatter
+from tablate.library.formatters.html.element.text import html_text_formatter
+from tablate.library.formatters.html.style.elements.column_style import column_style
+from tablate.library.formatters.html.style.elements.frame_style import frame_style
+from tablate.library.formatters.html.style.elements.text_style import text_style
 from tablate.type.type_frame import TextFrameDict
 from tablate.type.type_options import Options
 
 
 def render_html_text(text_frame_dict: TextFrameDict, options: Options, frame_styler: ElementStyle):
 
     column_baselines = options["html"]["column_baselines"]
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/html/render_html.py` & `tablate-0.0.7/tablate/library/renderers/html/render_html.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,29 +1,31 @@
-from tablate.api.classes.options.html.style.StyleCss import StyleCss
-from tablate.helpers.calcs.calc_column_percent import calc_column_percent
-from tablate.helpers.renderers.html.render_html_foot import render_html_foot
-from tablate.helpers.renderers.html.render_html_frames import render_html_frames
-from tablate.helpers.renderers.html.render_html_head import render_html_head
+from tablate.classes.options.html.style.StyleCss import StyleCss
+from tablate.library.calcs.calc_column_percent import calc_column_percent
+from tablate.library.renderers.html.render_html_foot import render_html_foot
+from tablate.library.renderers.html.render_html_frames import render_html_frames
+from tablate.library.renderers.html.render_html_head import render_html_head
 from tablate.type.type_frame import FrameDictList
 from tablate.type.type_options import Options
 
 
 def render_html(frame_list: FrameDictList, options: Options) -> str:
 
-    options["html"]["css"] = StyleCss()
+    options["html"]["style"] = StyleCss()
+
+    options["html"]["style"].inject_css_block(options["html"]["css"])
 
     return_html = ""
 
     if len(frame_list) > 0:
         frame_list, column_baselines = calc_column_percent(frame_list=frame_list,
                                                            frame_width=options["common"]["frame_width"])
         options["html"]["column_baselines"] = column_baselines
         return_html += render_html_head(options=options)
         return_html += render_html_frames(frame_list=frame_list, options=options)
         return_html += render_html_foot()
 
-    css_head = options['html']['css'].return_head_styles()
-    css_foot = options['html']['css'].return_foot_styles()
+    css_head = options['html']['style'].return_head_styles()
+    css_foot = options['html']['style'].return_foot_styles()
 
     return_html = f"{css_head}{return_html}{css_foot}"
 
     return return_html
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/html/render_html_frames.py` & `tablate-0.0.7/tablate/library/renderers/html/render_html_frames.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,20 +1,20 @@
-from tablate.helpers.renderers.html.frames.render_html_columns import render_html_column
-from tablate.helpers.renderers.html.frames.render_html_table_body import render_html_table_body
-from tablate.helpers.renderers.html.frames.render_html_text import render_html_text
+from tablate.library.renderers.html.frames.render_html_columns import render_html_column
+from tablate.library.renderers.html.frames.render_html_table_body import render_html_table_body
+from tablate.library.renderers.html.frames.render_html_text import render_html_text
 from tablate.type.type_frame import FrameDictList
 from tablate.type.type_options import Options
 
 
 def render_html_frames(frame_list: FrameDictList, options: Options) -> str:
 
     return_html = ''
 
     for frame_index, frame_item in enumerate(frame_list):
-        frame_styler = options["html"]["css"].frame(frame_index)
+        frame_styler = options["html"]["style"].frame(frame_index)
         if frame_item["type"] == "text":
             return_html += render_html_text(text_frame_dict=frame_item,
                                             options=options,
                                             frame_styler=frame_styler)
         if frame_item["type"] == "grid":
             return_html += render_html_column(frame_dict=frame_item,
                                               options=options,
```

### Comparing `tablate-0.0.6/tablate/helpers/renderers/html/render_html_head.py` & `tablate-0.0.7/tablate/library/renderers/html/render_html_head.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from tablate.helpers.formatters.html.style.border_style import border_line
+from tablate.library.formatters.html.style.border_style import border_line
 from tablate.type.type_options import Options
 
 
 def render_html_head(options: Options) -> str:
 
     frame_padding = options["common"]["frame_padding"]
     frame_border = options["common"]["border_style"]
@@ -11,26 +11,26 @@
     column_baselines = options["html"]["column_baselines"]
 
     margin_left_px = frame_padding * html_px
     margin_string = f'0 {margin_left_px}px'
 
     border_string = border_line(frame_border)
 
-    options["html"]["css"].add_global_style_attribute("box-sizing", "border-box")
-    options["html"]["css"].add_global_style_attribute("margin", 0)
-    options["html"]["css"].add_global_style_attribute("padding", 0)
+    options["html"]["style"].add_global_style_attribute("box-sizing", "border-box")
+    options["html"]["style"].add_global_style_attribute("margin", 0)
+    options["html"]["style"].add_global_style_attribute("padding", 0)
 
-    options["html"]["css"].wrapper.add_style_attribute("width", f"calc({html_width} - {margin_left_px * 2}px)")
-    options["html"]["css"].wrapper.add_style_attribute("margin", margin_string)
+    options["html"]["style"].wrapper.add_style_attribute("width", f"calc({html_width} - {margin_left_px * 2}px)")
+    options["html"]["style"].wrapper.add_style_attribute("margin", margin_string)
 
-    options["html"]["css"].table.add_style_attribute("width", "100%")
-    options["html"]["css"].table.add_style_attribute("border", border_string)
+    options["html"]["style"].table.add_style_attribute("width", "100%")
+    options["html"]["style"].table.add_style_attribute("border", border_string)
 
-    wrapper_classes = options["html"]["css"].wrapper.generate_class_names()
-    table_classes = options["html"]["css"].table.generate_class_names()
+    wrapper_classes = options["html"]["style"].wrapper.generate_class_names()
+    table_classes = options["html"]["style"].table.generate_class_names()
 
     return_string = ''
 
     return_string += f'<div class="{wrapper_classes}">'
     return_string += f'<table class="{table_classes}">'
 
     return_string += f'<colgroup>'
```

### Comparing `tablate-0.0.6/tablate/tests/test_defs.py` & `tablate-0.0.7/tablate/tests/test_defs.py`

 * *Files identical despite different names*

### Comparing `tablate-0.0.6/tablate/tests/test_objs.py` & `tablate-0.0.7/tablate/tests/test_objs.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from typing import List, Dict
+from __future__ import annotations
 
 column_list1 = [
     {
         "key": "A really really long key like this - maybe even longer",
         "width":  30
     },
     {
@@ -115,15 +115,15 @@
         "string": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
     },
     {
         "string": "Commodo elit at imperdiet dui accumsan sit amet nulla. Sodales neque sodales ut etiam sit amet nisl purus. Convallis posuere morbi leo urna molestie at elementum. Enim nunc faucibus a pellentesque sit amet porttitor. Enim nulla aliquet porttitor lacus luctus accumsan tortor. Ullamcorper velit sed ullamcorper morbi. Sit amet porttitor eget dolor morbi non arcu. Eget mauris pharetra et ultrices neque ornare aenean euismod elementum. Euismod lacinia at quis risus sed vulputate odio. Varius quam quisque id diam. Habitant morbi tristique senectus et netus et malesuada fames ac. Ornare quam viverra orci sagittis eu volutpat odio. Nisl suscipit adipiscing bibendum est ultricies. Adipiscing elit pellentesque habitant morbi tristique senectus. Tellus cras adipiscing enim eu turpis egestas pretium aenean pharetra. At consectetur lorem donec massa sapien faucibus et molestie. Neque ornare aenean euismod elementum nisi quis eleifend quam. A arcu cursus vitae congue mauris."
     }
 ]
 
-column_list4: list[dict[str, str | int] | dict[str, str] | dict[str, str]] = [
+column_list4 = [
     {
         "string": "Quam elementum pulvinar etiam non quam lacus suspendisse faucibus. Enim nec dui nunc mattis enim ut tellus. Est placerat in egestas erat imperdiet sed euismod nisi porta. At tempor commodo ullamcorper a lacus vestibulum sed. Porta nibh venenatis cras sed. Cras sed felis eget velit aliquet sagittis id consectetur. Aliquam id diam maecenas ultricies mi. ",
         "width": 20
     },
     {
         "string": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
         "divider": "thick"
```

### Comparing `tablate-0.0.6/tablate/tests/test_styles.py` & `tablate-0.0.7/tablate/tests/test_styles.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from tablate.api.classes.options.html.style.StyleCss import StyleCss
+from tablate.classes.options.html.style.StyleCss import StyleCss
 
 test_style = StyleCss()
 
 test_style.add_global_style_attribute("box-sizing", "border-box")
 test_style.add_global_style_attribute("margin", 0)
 
 print(test_style.table.generate_class_names())
```

### Comparing `tablate-0.0.6/tablate/type/type_frame.py` & `tablate-0.0.7/tablate/type/type_frame.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import Literal, TypedDict, Union, List, Dict, Generic, TypeVar
 
-from tablate.type.primitives import TextAlignment, BaseDivider, ColumnDivider
+from tablate.type.primitives import TextAlignment, BaseDivider
 
 ########################################################################################################################
 # FrameDicts ###########################################################################################################
 ########################################################################################################################
 
 
 T = TypeVar('T')
```

### Comparing `tablate-0.0.6/tablate/type/type_input.py` & `tablate-0.0.7/tablate/type/type_input.py`

 * *Files identical despite different names*

### Comparing `tablate-0.0.6/tablate/type/type_options.py` & `tablate-0.0.7/tablate/type/type_options.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from typing import TypedDict, Union, NotRequired, List
 
-from tablate.api.classes.options.html.style.StyleCss import StyleCss
+from tablate.classes.options.html.style.StyleCss import StyleCss
 from tablate.type.primitives import Border, BaseDivider
 
 
 class CommonOptions(TypedDict):
     border_style: Border
     frame_padding: int
     frame_divider: BaseDivider
@@ -17,18 +17,19 @@
 
 class CssDict(TypedDict):
     head: NotRequired[str]
     foot: NotRequired[str]
 
 
 class HtmlOptions(TypedDict):
+    css: str
     px_size: int
     text_size: int
     width: Union[int, str]
-    css: NotRequired[StyleCss]
+    style: NotRequired[StyleCss]
     uid: NotRequired[str]
     column_baselines: NotRequired[List[int]]
 
 
 class Options(TypedDict):
     common: CommonOptions
     html: HtmlOptions
```

### Comparing `tablate-0.0.6/tablate/type/type_style.py` & `tablate-0.0.7/tablate/type/type_style.py`

 * *Files identical despite different names*

