# Comparing `tmp/corporate_reputation-0.5.0.tar.gz` & `tmp/corporate_reputation-0.6.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "corporate_reputation-0.5.0.tar", max compression
+gzip compressed data, was "corporate_reputation-0.6.0.tar", max compression
```

## Comparing `corporate_reputation-0.5.0.tar` & `corporate_reputation-0.6.0.tar`

### file list

```diff
@@ -1,65 +1,50 @@
--rw-r--r--   0        0        0     1071 2023-07-20 05:26:52.870115 corporate_reputation-0.5.0/LICENSE
--rw-r--r--   0        0        0     3898 2023-07-20 05:26:52.870115 corporate_reputation-0.5.0/README.md
--rw-r--r--   0        0        0     3087 2023-07-20 05:27:26.058453 corporate_reputation-0.5.0/pyproject.toml
--rw-r--r--   0        0        0      288 2023-07-20 05:26:52.870115 corporate_reputation-0.5.0/src/corprep/__cli__.py
--rw-r--r--   0        0        0      438 2023-07-20 05:26:52.870115 corporate_reputation-0.5.0/src/corprep/__init__.py
--rw-r--r--   0        0        0       22 2023-07-20 05:27:26.006452 corporate_reputation-0.5.0/src/corprep/_version.py
--rw-r--r--   0        0        0        0 2023-07-20 05:26:52.870115 corporate_reputation-0.5.0/src/corprep/absa/__init__.py
--rw-r--r--   0        0        0     1754 2023-07-20 05:26:52.870115 corporate_reputation-0.5.0/src/corprep/absa/agent.py
--rw-r--r--   0        0        0     4823 2023-07-20 05:26:52.870115 corporate_reputation-0.5.0/src/corprep/absa/config.py
--rw-r--r--   0        0        0        0 2023-07-20 05:26:52.870115 corporate_reputation-0.5.0/src/corprep/conf/__init__.py
--rw-r--r--   0        0        0      338 2023-07-20 05:27:26.006452 corporate_reputation-0.5.0/src/corprep/conf/about/__init__.yaml
--rw-r--r--   0        0        0      259 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/absa/default.yaml
--rw-r--r--   0        0        0     2930 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/absa/prompts/default.yaml
--rw-r--r--   0        0        0      588 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/batch/__init__.yaml
--rw-r--r--   0        0        0        0 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/cmd/__init__.yaml
--rw-r--r--   0        0        0       49 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/cmd/about.yaml
--rw-r--r--   0        0        0      159 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/cmd/copy_conf.yaml
--rw-r--r--   0        0        0       83 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/cmd/run_task.yaml
--rw-r--r--   0        0        0       91 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/cmd/run_workflow.yaml
--rw-r--r--   0        0        0      213 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/config.yaml
--rw-r--r--   0        0        0      662 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/copier/__init__.yaml
--rw-r--r--   0        0        0      709 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/dotenv/__init__.yaml
--rw-r--r--   0        0        0      209 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/hconf.yaml
--rw-r--r--   0        0        0     1128 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/hydra/help/help.yaml
--rw-r--r--   0        0        0      264 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/hydra/job_logging/custom.yaml
--rw-r--r--   0        0        0      137 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/joblib/__init__.yaml
--rw-r--r--   0        0        0      198 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/mode/__debug__.yaml
--rw-r--r--   0        0        0      926 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/mode/__init__.yaml
--rw-r--r--   0        0        0       61 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/module/__init__.yaml
--rw-r--r--   0        0        0       72 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/path/__batch__.yaml
--rw-r--r--   0        0        0      846 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/path/__init__.yaml
--rw-r--r--   0        0        0       91 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/path/__task__.yaml
--rw-r--r--   0        0        0      286 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/path/dirnames/__init__.yaml
--rw-r--r--   0        0        0       76 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/__dataframe__.yaml
--rw-r--r--   0        0        0       77 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/__dataframe_external_funcs__.yaml
--rw-r--r--   0        0        0       79 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/__dataframe_instance_methods__.yaml
--rw-r--r--   0        0        0       70 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/__general_external_funcs__.yaml
--rw-r--r--   0        0        0       72 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/__general_instance_methods__.yaml
--rw-r--r--   0        0        0      424 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/__init__.yaml
--rw-r--r--   0        0        0      294 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/absa_agent_predict.yaml
--rw-r--r--   0        0        0      274 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/dataset_filter.yaml
--rw-r--r--   0        0        0      150 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/dataset_load.yaml
--rw-r--r--   0        0        0      163 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/dataset_load_raw.yaml
--rw-r--r--   0        0        0      218 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/dataset_sample.yaml
--rw-r--r--   0        0        0      106 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/dataset_save.yaml
--rw-r--r--   0        0        0      217 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipe/dataset_tokenize.yaml
--rw-r--r--   0        0        0       69 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipeline/__init__.yaml
--rw-r--r--   0        0        0      388 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipeline/__test__.yaml
--rw-r--r--   0        0        0      796 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipeline/absa.yaml
--rw-r--r--   0        0        0      448 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/pipeline/datasets.yaml
--rw-r--r--   0        0        0      746 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/project/__init__.yaml
--rw-r--r--   0        0        0      221 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/project/corprep.yaml
--rw-r--r--   0        0        0       38 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/running/__init__.yaml
--rw-r--r--   0        0        0      142 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/task/__batch__.yaml
--rw-r--r--   0        0        0      329 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/task/__init__.yaml
--rw-r--r--   0        0        0      137 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/task/absa.yaml
--rw-r--r--   0        0        0      212 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/task/datasets.yaml
--rw-r--r--   0        0        0      124 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/workflow/__init__.yaml
--rw-r--r--   0        0        0      190 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/conf/workflow/corprep.yaml
--rw-r--r--   0        0        0      204 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/datasets/__init__.py
--rw-r--r--   0        0        0     1665 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/datasets/io.py
--rw-r--r--   0        0        0      617 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/datasets/sample.py
--rw-r--r--   0        0        0      843 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/datasets/tokenize.py
--rw-r--r--   0        0        0        0 2023-07-20 05:26:52.874115 corporate_reputation-0.5.0/src/corprep/py.typed
--rw-r--r--   0        0        0     4764 1970-01-01 00:00:00.000000 corporate_reputation-0.5.0/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-07-23 20:01:28.480513 corporate_reputation-0.6.0/LICENSE
+-rw-r--r--   0        0        0     3898 2023-07-23 20:01:28.480513 corporate_reputation-0.6.0/README.md
+-rw-r--r--   0        0        0     3075 2023-07-23 20:02:02.468593 corporate_reputation-0.6.0/pyproject.toml
+-rw-r--r--   0        0        0      182 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/__cli__.py
+-rw-r--r--   0        0        0      464 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/__init__.py
+-rw-r--r--   0        0        0       22 2023-07-23 20:02:02.424593 corporate_reputation-0.6.0/src/corprep/_version.py
+-rw-r--r--   0        0        0        0 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/absa/__init__.py
+-rw-r--r--   0        0        0     1757 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/absa/agent.py
+-rw-r--r--   0        0        0     4793 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/absa/config.py
+-rw-r--r--   0        0        0        0 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/__init__.py
+-rw-r--r--   0        0        0      286 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/about/corprep.yaml
+-rw-r--r--   0        0        0      259 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/absa/default.yaml
+-rw-r--r--   0        0        0     2930 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/absa/prompts/default.yaml
+-rw-r--r--   0        0        0      169 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/normalizer/__init__.yaml
+-rw-r--r--   0        0        0       54 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/normalizer/formal_en.yaml
+-rw-r--r--   0        0        0       77 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/normalizer/formal_en_parantheses.yaml
+-rw-r--r--   0        0        0       43 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/normalizer/formal_ko.yaml
+-rw-r--r--   0        0        0      363 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/normalizer/ftfy/__init__.yaml
+-rw-r--r--   0        0        0       67 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/normalizer/informal_ko.yaml
+-rw-r--r--   0        0        0      102 2023-07-23 20:01:28.484513 corporate_reputation-0.6.0/src/corprep/conf/normalizer/spaces/__init__.yaml
+-rw-r--r--   0        0        0      151 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/normalizer/special_characters/__init__.yaml
+-rw-r--r--   0        0        0      294 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/pipe/absa_agent_predict.yaml
+-rw-r--r--   0        0        0      274 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/pipe/dataset_filter.yaml
+-rw-r--r--   0        0        0      163 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/pipe/dataset_load_raw.yaml
+-rw-r--r--   0        0        0      276 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/pipe/dataset_tokenize.yaml
+-rw-r--r--   0        0        0      143 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/stopwords/__init__.yaml
+-rw-r--r--   0        0        0      491 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/tokenizer/__init__.yaml
+-rw-r--r--   0        0        0      238 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/tokenizer/mecab.yaml
+-rw-r--r--   0        0        0      151 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/tokenizer/nltk.yaml
+-rw-r--r--   0        0        0       84 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/tokenizer/simple.yaml
+-rw-r--r--   0        0        0       88 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/tokenizer/tagger/mecab.yaml
+-rw-r--r--   0        0        0      125 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/conf/tokenizer/tagger/nltk.yaml
+-rw-r--r--   0        0        0      204 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/datasets/__init__.py
+-rw-r--r--   0        0        0     1665 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/datasets/io.py
+-rw-r--r--   0        0        0      617 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/datasets/sample.py
+-rw-r--r--   0        0        0     1790 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/datasets/similarity.py
+-rw-r--r--   0        0        0      980 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/datasets/tokenize.py
+-rw-r--r--   0        0        0        0 2023-07-23 20:01:28.488513 corporate_reputation-0.6.0/src/corprep/py.typed
+-rw-r--r--   0        0        0  2355775 2023-07-23 20:01:28.500513 corporate_reputation-0.6.0/src/corprep/resources/dictionaries/mecab/ekon_v1.dic
+-rw-r--r--   0        0        0    12659 2023-07-23 20:01:28.500513 corporate_reputation-0.6.0/src/corprep/tokenizer/__init__.py
+-rw-r--r--   0        0        0     8294 2023-07-23 20:01:28.500513 corporate_reputation-0.6.0/src/corprep/tokenizer/hangle.py
+-rw-r--r--   0        0        0      255 2023-07-23 20:01:28.500513 corporate_reputation-0.6.0/src/corprep/tokenizer/hanja/__init__.py
+-rw-r--r--   0        0        0     2123 2023-07-23 20:01:28.500513 corporate_reputation-0.6.0/src/corprep/tokenizer/hanja/hangul.py
+-rw-r--r--   0        0        0     2813 2023-07-23 20:01:28.500513 corporate_reputation-0.6.0/src/corprep/tokenizer/hanja/impl.py
+-rw-r--r--   0        0        0      427 2023-07-23 20:01:28.500513 corporate_reputation-0.6.0/src/corprep/tokenizer/hanja/table.py
+-rw-r--r--   0        0        0   522443 2023-07-23 20:01:28.504513 corporate_reputation-0.6.0/src/corprep/tokenizer/hanja/table.yml
+-rw-r--r--   0        0        0    10202 2023-07-23 20:01:28.504513 corporate_reputation-0.6.0/src/corprep/tokenizer/normalizer.py
+-rw-r--r--   0        0        0     2806 2023-07-23 20:01:28.504513 corporate_reputation-0.6.0/src/corprep/tokenizer/stopwords.py
+-rw-r--r--   0        0        0    14353 2023-07-23 20:01:28.504513 corporate_reputation-0.6.0/src/corprep/tokenizer/utils.py
+-rw-r--r--   0        0        0     4883 1970-01-01 00:00:00.000000 corporate_reputation-0.6.0/PKG-INFO
```

### Comparing `corporate_reputation-0.5.0/LICENSE` & `corporate_reputation-0.6.0/LICENSE`

 * *Files identical despite different names*

### Comparing `corporate_reputation-0.5.0/README.md` & `corporate_reputation-0.6.0/README.md`

 * *Files identical despite different names*

### Comparing `corporate_reputation-0.5.0/pyproject.toml` & `corporate_reputation-0.6.0/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,35 +1,38 @@
 [tool.poetry]
 name = "corporate-reputation"
-version = "0.5.0"
+version = "0.6.0"
 description = "Unraveling Corporate and CEO Reputation using Aspect-Based Sentiment Analysis and Signal Modeling"
 authors = ["Young Joon Lee <entelecheia@hotmail.com>"]
 license = "MIT"
 homepage = "https://entelecheia.github.io/corporate-reputation"
 repository = "https://github.com/entelecheia/corporate-reputation"
 readme = "README.md"
 packages = [{ include = "corprep", from = "src" }]
 
 [tool.poetry.scripts]
 corprep = 'corprep.__cli__:main'
 
 [tool.poetry.dependencies]
 python = ">=3.8.1,<3.12"
-hyfi = "^1.3.1"
+hyfi = "^1.8.2"
 ekonlpy = "^1.1.7"
 openai = "^0.27.8"
 backoff = "^2.2.1"
+scikit-learn = "^1.3.0"
+ftfy = "^6.1.1"
+nltk = "^3.8.1"
 
 [tool.poetry.group.dev]
 optional = true
 
 [tool.poetry.group.dev.dependencies]
 python-semantic-release = "^7.33.1"
 isort = "^5.12.0"
-black = "^23.1.0"
+black = ">=23.0.0,<=23.3.0"
 flake8 = "^6.0.0"
 mypy = "^1.0.0"
 flake8-pyproject = "^1.2.2"
 pytest = "^7.2.1"
 pytest-cov = "^4.0.0"
 
 [tool.poe]
@@ -85,15 +88,14 @@
 name = "cz_conventional_commits"
 tag_format = "v$version"
 
 [tool.semantic_release]
 branch = "main"
 version_toml = "pyproject.toml:tool.poetry.version"
 version_variable = "src/corprep/_version.py:__version__"
-version_pattern = 'src/corprep/conf/about/__init__.yaml:version: "{version}"'
 version_source = "tag"
 commit_version_number = true # required for version_source = "tag"
 commit_subject = "chore(release): :rocket: {version} [skip ci]"
 prerelease_tag = "rc"
 major_on_zero = true
 tag_commit = true
 changelog_file = "CHANGELOG.md"
```

### Comparing `corporate_reputation-0.5.0/src/corprep/absa/agent.py` & `corporate_reputation-0.6.0/src/corprep/absa/agent.py`

 * *Files 10% similar despite different names*

```diff
@@ -31,31 +31,31 @@
     cfg = HyFI.compose_as_dict(f"absa={absa_config_name}")
     model = AbsaModel(**cfg)
     model.absa_task = task
     model.init_api()
     if model.verbose:
         print(model)
 
-    res = []
-    for i, text in enumerate(batch[text_col]):
-        res.append(predict_each(text, model))
+    res = [predict_each(text, model) for text in batch[text_col]]
     return {f"{task}_pred": res}
 
 
 def predict(
     dataset: Dataset,
-    tasks=["QUAD"],
+    tasks=None,
     absa_config_name: str = "default",
     text_col: str = "bodyText",
     batch_size=2,
     num_workers=1,
     remove_columns: Optional[Union[List[str], str]] = None,
     load_from_cache_file=True,
     verbose=False,
 ) -> Dataset:
+    if tasks is None:
+        tasks = ["QUAD"]
     for task in tasks:
         logger.info("Predicting %s...", task)
         dataset = dataset.map(
             batch_predict,
             batched=True,
             batch_size=batch_size,
             num_proc=num_workers,
```

### Comparing `corporate_reputation-0.5.0/src/corprep/absa/config.py` & `corporate_reputation-0.6.0/src/corprep/absa/config.py`

 * *Files 4% similar despite different names*

```diff
@@ -21,18 +21,18 @@
 
 
 class PromptConfig(BaseModel):
     tasks: Dict[str, str] = {}
     prompts: Dict[str, Dict[str, str]] = {}
 
     def get_prompt(self, task, prompt_name):
-        prompt = self.prompts.get(task, {}).get(prompt_name, "")
-        if not prompt:
+        if prompt := self.prompts.get(task, {}).get(prompt_name, ""):
+            return prompt
+        else:
             raise ValueError(f"Prompt for task {task} is not defined.")
-        return prompt
 
 
 class AbsaModel(BaseModel):
     api_key: Optional[str] = None
     model_name: str = "gpt-3.5-turbo-0301"
     rate_limit_per_minute: int = 20
     absa_task: str = "AE"
@@ -62,15 +62,15 @@
             raise ValueError("OpenAI API Key is required.")
         self._agent_ = openai.ChatCompletion()
         logger.info("OpenAI ChatCompletion API is initialized.")
 
     def get_prompt(self, text: str):
         task = self.absa_task
         prompt = self.prompts.get_prompt(task, self.prompt_name)
-        prompt += '\nInput text:\n"{}"\nAnswer:\n'.format(text)
+        prompt += f'\nInput text:\n"{text}"\nAnswer:\n'
         return prompt
 
     def predict(self, text: str):
         args = {
             "model": self.model_name,
             "temperature": self.temperature,
             "messages": [
@@ -124,24 +124,23 @@
     (
         RateLimitError,
         APIConnectionError,
         APIError,
         ServiceUnavailableError,
     ),
 )
-def create_api(agent, args, delay_in_seconds: float = 1):
+def request_api(agent, args, delay_in_seconds: float = 1):
     time.sleep(delay_in_seconds)
-    response = agent.create(**args)
-    return response
+    return agent.create(**args)
 
 
 def call_api(agent, args, delay_in_seconds: float = 1) -> Tuple[str, dict, Any]:
     time.sleep(delay_in_seconds)
     try:
-        response = create_api(agent, args, delay_in_seconds=delay_in_seconds)
+        response = request_api(agent, args, delay_in_seconds=delay_in_seconds)
         message = response["choices"][0]["message"]
         content = message["content"].strip().strip("\n")
         usage = response["usage"]
         return content, usage, response
     except InvalidRequestError as e:
         logger.error(e)
         usage = {"prompt_tokens": 0, "completion_tokens": 0, "total_tokens": 0}
```

### Comparing `corporate_reputation-0.5.0/src/corprep/conf/absa/prompts/default.yaml` & `corporate_reputation-0.6.0/src/corprep/conf/absa/prompts/default.yaml`

 * *Files identical despite different names*

### Comparing `corporate_reputation-0.5.0/src/corprep/datasets/io.py` & `corporate_reputation-0.6.0/src/corprep/datasets/io.py`

 * *Files identical despite different names*

### Comparing `corporate_reputation-0.5.0/src/corprep/datasets/sample.py` & `corporate_reputation-0.6.0/src/corprep/datasets/sample.py`

 * *Files identical despite different names*

### Comparing `corporate_reputation-0.5.0/src/corprep/datasets/tokenize.py` & `corporate_reputation-0.6.0/src/corprep/datasets/tokenize.py`

 * *Files 25% similar despite different names*

```diff
@@ -4,28 +4,30 @@
 from corprep import HyFI  # type: ignore
 
 logger = HyFI.getLogger(__name__)
 
 
 def tokenize_dataset(
     data: Dataset,
+    tokenizer_config_name: str = "simple",
     num_proc: int = 1,
     batched: bool = True,
     text_col: str = "bodyText",
+    token_col: str = "tokenizedText",
     verbose: bool = False,
 ) -> Dataset:
     def pos_tagging(batch):
-        mecab = Mecab()
-        batch_tags = []
+        tokenizer = HyFI.instantiate_config(f"tokenizer={tokenizer_config_name}")
+        batch_tokens = []
         for text in batch[text_col]:
             sentences = text.split("\n")
-            pos_tags = []
+            tokens = []
             for sentence in sentences:
-                pos_tags.extend(mecab.pos(sentence))
-            batch_tags.append(pos_tags)
-        return {"pos_tags": batch_tags}
+                tokens.extend(tokenizer(sentence))
+            batch_tokens.append(tokens)
+        return {token_col: batch_tokens}
 
     data = data.map(pos_tagging, num_proc=num_proc, batched=batched)
     logger.info("POS tagging done.")
     if verbose:
-        print(data[0]["pos_tags"])
+        print(data[0][token_col])
     return data
```

### Comparing `corporate_reputation-0.5.0/PKG-INFO` & `corporate_reputation-0.6.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,25 +1,28 @@
 Metadata-Version: 2.1
 Name: corporate-reputation
-Version: 0.5.0
+Version: 0.6.0
 Summary: Unraveling Corporate and CEO Reputation using Aspect-Based Sentiment Analysis and Signal Modeling
 Home-page: https://entelecheia.github.io/corporate-reputation
 License: MIT
 Author: Young Joon Lee
 Author-email: entelecheia@hotmail.com
 Requires-Python: >=3.8.1,<3.12
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: backoff (>=2.2.1,<3.0.0)
 Requires-Dist: ekonlpy (>=1.1.7,<2.0.0)
-Requires-Dist: hyfi (>=1.3.1,<2.0.0)
+Requires-Dist: ftfy (>=6.1.1,<7.0.0)
+Requires-Dist: hyfi (>=1.8.2,<2.0.0)
+Requires-Dist: nltk (>=3.8.1,<4.0.0)
 Requires-Dist: openai (>=0.27.8,<0.28.0)
+Requires-Dist: scikit-learn (>=1.3.0,<2.0.0)
 Project-URL: Repository, https://github.com/entelecheia/corporate-reputation
 Description-Content-Type: text/markdown
 
 # Reputation Analysis of Companies and CEOs
 
 [![pypi-image]][pypi-url]
 [![version-image]][release-url]
```

