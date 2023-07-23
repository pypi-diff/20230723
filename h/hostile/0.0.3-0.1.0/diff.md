# Comparing `tmp/hostile-0.0.3.tar.gz` & `tmp/hostile-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hostile-0.0.3.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "hostile-0.1.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `hostile-0.0.3.tar` & `hostile-0.1.0.tar`

### file list

```diff
@@ -1,37 +1,37 @@
--rw-r--r--   0        0        0      715 2023-07-10 14:24:39.989614 hostile-0.0.3/.github/workflows/test.yml
--rw-r--r--   0        0        0     1840 2023-07-10 14:19:21.498360 hostile-0.0.3/.gitignore
--rw-r--r--   0        0        0      260 2023-05-31 15:56:25.388315 hostile-0.0.3/.pre-commit-config.yaml
--rw-r--r--   0        0        0     1086 2023-05-23 13:13:09.919197 hostile-0.0.3/LICENSE
--rw-r--r--   0        0        0     8865 2023-07-12 15:00:01.077040 hostile-0.0.3/README.md
--rw-r--r--   0        0        0      199 2023-07-12 08:28:57.211688 hostile-0.0.3/environment.yml
--rw-r--r--   0        0        0   121111 2023-07-06 23:30:48.068804 hostile-0.0.3/paper/preprint.pdf
--rw-r--r--   0        0        0     5403 2023-07-06 18:18:11.923619 hostile-0.0.3/paper/supplementary-table-1.tsv
--rw-r--r--   0        0        0    39955 2023-07-06 18:18:11.923951 hostile-0.0.3/paper/supplementary-table-2.tsv
--rw-r--r--   0        0        0    95229 2023-07-06 23:30:59.338804 hostile-0.0.3/paper/supplementary-text.pdf
--rw-r--r--   0        0        0      669 2023-07-12 08:28:40.211794 hostile-0.0.3/pyproject.toml
--rw-r--r--   0        0        0       55 2023-07-12 15:01:44.689339 hostile-0.0.3/src/hostile/__init__.py
--rw-r--r--   0        0        0     6952 2023-07-12 14:34:55.899926 hostile-0.0.3/src/hostile/aligner.py
--rw-r--r--   0        0        0     3981 2023-07-12 14:59:11.724536 hostile-0.0.3/src/hostile/cli.py
--rw-r--r--   0        0        0    10523 2023-07-12 14:51:23.870446 hostile-0.0.3/src/hostile/lib.py
--rw-r--r--   0        0        0     2794 2023-07-12 10:56:47.727510 hostile-0.0.3/src/hostile/util.py
--rw-r--r--   0        0        0  4204460 2023-06-02 16:28:46.881250 hostile-0.0.3/tests/data/MN908947/MN908947.1.bt2
--rw-r--r--   0        0        0     7480 2023-06-02 16:28:46.881240 hostile-0.0.3/tests/data/MN908947/MN908947.2.bt2
--rw-r--r--   0        0        0       17 2023-06-02 16:28:46.850838 hostile-0.0.3/tests/data/MN908947/MN908947.3.bt2
--rw-r--r--   0        0        0     7476 2023-06-02 16:28:46.850709 hostile-0.0.3/tests/data/MN908947/MN908947.4.bt2
--rw-r--r--   0        0        0     9458 2022-07-08 10:03:05.588963 hostile-0.0.3/tests/data/MN908947/MN908947.fasta.gz
--rw-r--r--   0        0        0  4204460 2023-06-02 16:28:46.913064 hostile-0.0.3/tests/data/MN908947/MN908947.rev.1.bt2
--rw-r--r--   0        0        0     7480 2023-06-02 16:28:46.913055 hostile-0.0.3/tests/data/MN908947/MN908947.rev.2.bt2
--rw-r--r--   0        0        0      811 2023-07-10 11:24:36.269899 hostile-0.0.3/tests/data/MN908947/partial-for-mask-testing.fa.gz
--rw-r--r--   0        0        0     3562 2023-05-25 19:01:02.910477 hostile-0.0.3/tests/data/h37rv_10.r1.fastq
--rw-r--r--   0        0        0     1508 2023-05-25 19:01:02.910477 hostile-0.0.3/tests/data/h37rv_10.r1.fastq.gz
--rw-r--r--   0        0        0     3562 2023-05-25 19:01:13.127122 hostile-0.0.3/tests/data/h37rv_10.r2.fastq
--rw-r--r--   0        0        0     1501 2023-05-25 19:01:13.127122 hostile-0.0.3/tests/data/h37rv_10.r2.fastq.gz
--rw-r--r--   0        0        0    19004 2023-05-31 15:32:30.691759 hostile-0.0.3/tests/data/human.1k.fa.gz
--rw-r--r--   0        0        0      164 2023-07-06 18:18:11.924762 hostile-0.0.3/tests/data/human_1_1.fastq.gz
--rw-r--r--   0        0        0      178 2023-07-06 18:18:11.925005 hostile-0.0.3/tests/data/human_1_2.fastq.gz
--rw-r--r--   0        0        0     3497 2023-07-06 18:18:11.925318 hostile-0.0.3/tests/data/mixed_human_100_1.fastq.gz
--rw-r--r--   0        0        0     3798 2023-07-06 18:18:11.925658 hostile-0.0.3/tests/data/mixed_human_100_2.fastq.gz
--rw-r--r--   0        0        0      239 2023-07-06 18:18:11.925871 hostile-0.0.3/tests/data/tuberculosis_1_1.fastq.gz
--rw-r--r--   0        0        0      232 2023-07-06 18:18:11.926049 hostile-0.0.3/tests/data/tuberculosis_1_2.fastq.gz
--rw-r--r--   0        0        0     6079 2023-07-12 14:51:23.772141 hostile-0.0.3/tests/test_all.py
--rw-r--r--   0        0        0     9455 1970-01-01 00:00:00.000000 hostile-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0      715 2023-07-10 14:24:39.989614 hostile-0.1.0/.github/workflows/test.yml
+-rw-r--r--   0        0        0     1840 2023-07-10 14:19:21.498360 hostile-0.1.0/.gitignore
+-rw-r--r--   0        0        0      260 2023-05-31 15:56:25.388315 hostile-0.1.0/.pre-commit-config.yaml
+-rw-r--r--   0        0        0     1086 2023-05-23 13:13:09.919197 hostile-0.1.0/LICENSE
+-rw-r--r--   0        0        0    10035 2023-07-23 12:02:52.895945 hostile-0.1.0/README.md
+-rw-r--r--   0        0        0      199 2023-07-19 17:28:43.689866 hostile-0.1.0/environment.yml
+-rw-r--r--   0        0        0   133587 2023-07-21 13:16:27.179026 hostile-0.1.0/paper/preprint.pdf
+-rw-r--r--   0        0        0     6134 2023-07-20 18:19:00.140804 hostile-0.1.0/paper/supplementary-table-1.tsv
+-rw-r--r--   0        0        0    11491 2023-07-20 18:21:17.921904 hostile-0.1.0/paper/supplementary-table-2.tsv
+-rw-r--r--   0        0        0    41073 2023-07-20 18:23:30.116510 hostile-0.1.0/paper/supplementary-table-3.tsv
+-rw-r--r--   0        0        0    95499 2023-07-20 18:57:22.316740 hostile-0.1.0/paper/supplementary-text.pdf
+-rw-r--r--   0        0        0      669 2023-07-13 13:27:59.309270 hostile-0.1.0/pyproject.toml
+-rw-r--r--   0        0        0       55 2023-07-23 11:56:01.385057 hostile-0.1.0/src/hostile/__init__.py
+-rw-r--r--   0        0        0     7339 2023-07-23 13:14:08.019933 hostile-0.1.0/src/hostile/aligner.py
+-rw-r--r--   0        0        0     4029 2023-07-23 12:01:37.272254 hostile-0.1.0/src/hostile/cli.py
+-rw-r--r--   0        0        0    10849 2023-07-23 13:16:34.297272 hostile-0.1.0/src/hostile/lib.py
+-rw-r--r--   0        0        0     3432 2023-07-23 12:01:37.301559 hostile-0.1.0/src/hostile/util.py
+-rw-r--r--   0        0        0      164 2023-07-06 18:18:11.924762 hostile-0.1.0/tests/data/human_1_1.fastq.gz
+-rw-r--r--   0        0        0      178 2023-07-06 18:18:11.925005 hostile-0.1.0/tests/data/human_1_2.fastq.gz
+-rw-r--r--   0        0        0      811 2023-07-10 11:24:36.269899 hostile-0.1.0/tests/data/sars-cov-2/partial-for-mask-testing.fa.gz
+-rw-r--r--   0        0        0  4204460 2023-06-02 16:28:46.881250 hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.1.bt2
+-rw-r--r--   0        0        0     7480 2023-06-02 16:28:46.881240 hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.2.bt2
+-rw-r--r--   0        0        0       17 2023-06-02 16:28:46.850838 hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.3.bt2
+-rw-r--r--   0        0        0     7476 2023-06-02 16:28:46.850709 hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.4.bt2
+-rw-r--r--   0        0        0     9458 2022-07-08 10:03:05.588963 hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.fasta.gz
+-rw-r--r--   0        0        0  4204460 2023-06-02 16:28:46.913064 hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.rev.1.bt2
+-rw-r--r--   0        0        0     7480 2023-06-02 16:28:46.913055 hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.rev.2.bt2
+-rw-r--r--   0        0        0     4104 2023-07-23 10:44:52.122889 hostile-0.1.0/tests/data/sars-cov-2_100_1.fastq.gz
+-rw-r--r--   0        0        0     4263 2023-07-23 10:44:58.804478 hostile-0.1.0/tests/data/sars-cov-2_100_2.fastq.gz
+-rw-r--r--   0        0        0      319 2023-07-23 12:01:36.874003 hostile-0.1.0/tests/data/sars-cov-2_1_1.fastq
+-rw-r--r--   0        0        0      319 2023-07-23 12:01:36.874201 hostile-0.1.0/tests/data/sars-cov-2_1_2.fastq
+-rw-r--r--   0        0        0      335 2023-07-06 18:18:11.925871 hostile-0.1.0/tests/data/tuberculosis_1_1.fastq
+-rw-r--r--   0        0        0      239 2023-07-06 18:18:11.925871 hostile-0.1.0/tests/data/tuberculosis_1_1.fastq.gz
+-rw-r--r--   0        0        0      335 2023-07-06 18:18:11.926049 hostile-0.1.0/tests/data/tuberculosis_1_2.fastq
+-rw-r--r--   0        0        0      232 2023-07-06 18:18:11.926049 hostile-0.1.0/tests/data/tuberculosis_1_2.fastq.gz
+-rw-r--r--   0        0        0    10990 2023-07-23 12:01:37.465777 hostile-0.1.0/tests/test_all.py
+-rw-r--r--   0        0        0    10625 1970-01-01 00:00:00.000000 hostile-0.1.0/PKG-INFO
```

### Comparing `hostile-0.0.3/.github/workflows/test.yml` & `hostile-0.1.0/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/.gitignore` & `hostile-0.1.0/.gitignore`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/LICENSE` & `hostile-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/README.md` & `hostile-0.1.0/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,50 +1,76 @@
-[![Tests](https://github.com/bede/hostile/actions/workflows/test.yml/badge.svg)](https://github.com/bede/hostile/actions/workflows/test.yml) [![PyPI](https://img.shields.io/pypi/v/hostile)](https://pypi.org/project/hostile/) ![PyPI - Downloads](https://img.shields.io/pypi/dm/hostile)
+Metadata-Version: 2.1
+Name: hostile
+Version: 0.1.0
+Summary: Accurate host read removal
+Author-email: Bede Constantinides <bedeabc@gmail.com>
+Requires-Python: >=3.10
+Description-Content-Type: text/markdown
+Classifier: License :: OSI Approved :: MIT License
+Requires-Dist: defopt>=6.4.0
+Requires-Dist: httpx>=0.24.1
+Requires-Dist: platformdirs>=3.5.1
+Requires-Dist: tqdm>=4.65.0
+Requires-Dist: pytest>=7.3.1 ; extra == "dev"
+Requires-Dist: pre-commit>=3.3.2 ; extra == "dev"
+Requires-Dist: flit>=3.9.0 ; extra == "dev"
+Project-URL: Home, https://github.com/bede/hostile
+Provides-Extra: dev
 
-# Hostile
-
-Hostile removes host sequences from short and long reads, consuming paired or unpaired `fastq[.gz]` input and producing `fastq.gz` output. Batteries are included – Hostile downloads and saves a human T2T-CHM13v2.0 + HLA reference genome to `$XDG_DATA_DIR` when run for the first time. Read headers are replaced with incrementing integers for privacy and more compressible FASTQs. Hostile is implemented as a Python package with a CLI and Python API, but all of the heavy lifting is done by fast compiled code (Minimap2/Bowtie2 and Samtools). When used with a masked reference genome, Hostile achieves near-perfect retention of microbial reads while removing >99.5% of human reads. Please read the [BioRxiv preprint](https://www.biorxiv.org/content/10.1101/2023.07.04.547735) for further information and open a GitHub issue, [tweet](https://twitter.com/beconsta) or [toot](https://mstdn.science/@bede) me to report bugs or suggest improvements.
+[![Tests](https://github.com/bede/hostile/actions/workflows/test.yml/badge.svg)](https://github.com/bede/hostile/actions/workflows/test.yml) [![PyPI version](https://img.shields.io/pypi/v/hostile)](https://pypi.org/project/hostile/) [![Bioconda version](https://anaconda.org/bioconda/hostile/badges/version.svg)](https://anaconda.org/bioconda/hostile/) [![Install with bioconda](https://img.shields.io/badge/install%20with-bioconda-brightgreen.svg?style=flat-square&logo=anaconda)](https://biocontainers.pro/tools/hostile) [![Install with Docker](https://img.shields.io/badge/install%20with-docker-important.svg?style=flat-square&logo=docker)](https://biocontainers.pro/tools/hostile) [![DOI:10.1101/2023.07.04.547735](http://img.shields.io/badge/BioRxiv-10.1101/2023.07.04.547735-bd2736.svg)](https://www.biorxiv.org/content/10.1101/2023.07.04.547735)
 
+# Hostile
 
+Hostile removes host sequences from short and long reads, consuming paired or unpaired `fastq[.gz]` input. Batteries are included – a human reference genome is downloaded when run for the first time. For maximum retention of microbial reads, an existing masked reference genome can be downloaded, or a new one created for target organisms. When used with a masked reference genome, Hostile achieves near-perfect retention of microbial reads while removing >99.6% of human reads. Read headers can be replaced with integers (using `--rename`) for privacy and smaller FASTQs. Heavy lifting is done with fast existing tools (Minimap2/Bowtie2 and Samtools). Bowtie2 is the default aligner for short (paired) reads while Minimap2 is default aligner for long reads. Benchmarks and further info can be found in the [BioRxiv preprint](https://www.biorxiv.org/content/10.1101/2023.07.04.547735) (please cite if useful!). Feel free open an issue, [tweet](https://twitter.com/beconsta) or [toot](https://mstdn.science/@bede) me to report problems or suggest improvements.
 
 ## Reference genomes
 
-The default `human-t2t-hla` reference is downloaded when running Hostile for the first time. This can be overriden by specifying a custom `--index`. Bowtie2 indexes need to be untarred before use. The databases `human-t2t-hla` and `human-t2t-hla-argos985-mycob140`  were compared in the [paper](https://www.biorxiv.org/content/10.1101/2023.07.04.547735).
+The default `human-t2t-hla` reference is downloaded when running Hostile for the first time. This can be overriden by specifying a custom `--index`. Bowtie2 indexes need to be untarred before use. The databases `human-t2t-hla` and `human-t2t-hla-argos985-mycob140` were compared in the [paper](https://www.biorxiv.org/content/10.1101/2023.07.04.547735).
 
-|               Name                |                         Composition                          |                      Genome (Minimap2)                       |                        Bowtie2 index                         |
-| :-------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
-|   `human-t2t-hla` **(default)**   | [T2T-CHM13v2.0](https://www.ncbi.nlm.nih.gov/assembly/11828891) + [IPD-IMGT/HLA](https://www.ebi.ac.uk/ipd/imgt/hla/) v3.51 | [human-t2t-hla.fa.gz](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla.fa.gz) | [human-t2t-hla.tar](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla.tar) |
-|     `human-t2t-hla-argos985`      | [T2T-CHM13v2.0](https://www.ncbi.nlm.nih.gov/assembly/11828891) & [IPD-IMGT/HLA](https://www.ebi.ac.uk/ipd/imgt/hla/) v3.51; masked with [985](https://github.com/bede/hostile/blob/main/paper/supplementary-table-2.tsv) [FDA-ARGOS](https://www.ncbi.nlm.nih.gov/bioproject/231221) 150mers | [human-t2t-hla-argos985.fa.gz](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla-argos985.fa.gz) | [human-t2t-hla-argos985.tar](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla-argos985.tar) |
-| `human-t2t-hla-argos985-mycob140` | [T2T-CHM13v2.0](https://www.ncbi.nlm.nih.gov/assembly/11828891) & [IPD-IMGT/HLA](https://www.ebi.ac.uk/ipd/imgt/hla/) v3.51; masked with [985](https://github.com/bede/hostile/blob/main/paper/supplementary-table-2.tsv) [FDA-ARGOS](https://www.ncbi.nlm.nih.gov/bioproject/231221) & [140](https://github.com/bede/hostile/blob/main/paper/supplementary-table-2.tsv) mycobacterial 150mers | [human-t2t-hla-argos985-mycob140.fa.gz](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla-argos985-mycob140.fa.gz) | [human-t2t-hla-argos985-mycob140.tar](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla-argos985-mycob140.tar) |
+|               Name                |                         Composition                          |                      Genome (Minimap2)                       |                        Bowtie2 index                         | Date    |
+| :-------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | ------- |
+|   `human-t2t-hla` **(default)**   | [T2T-CHM13v2.0](https://www.ncbi.nlm.nih.gov/assembly/11828891) + [IPD-IMGT/HLA](https://www.ebi.ac.uk/ipd/imgt/hla/) v3.51 | [human-t2t-hla.fa.gz](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla.fa.gz) | [human-t2t-hla.tar](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla.tar) | 2023-07 |
+|     `human-t2t-hla-argos985`      | [T2T-CHM13v2.0](https://www.ncbi.nlm.nih.gov/assembly/11828891) & [IPD-IMGT/HLA](https://www.ebi.ac.uk/ipd/imgt/hla/) v3.51; masked with [985](https://github.com/bede/hostile/blob/main/paper/supplementary-table-2.tsv) [FDA-ARGOS](https://www.ncbi.nlm.nih.gov/bioproject/231221) 150mers | [human-t2t-hla-argos985.fa.gz](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla-argos985.fa.gz) | [human-t2t-hla-argos985.tar](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla-argos985.tar) | 2023-07 |
+| `human-t2t-hla-argos985-mycob140` | [T2T-CHM13v2.0](https://www.ncbi.nlm.nih.gov/assembly/11828891) & [IPD-IMGT/HLA](https://www.ebi.ac.uk/ipd/imgt/hla/) v3.51; masked with [985](https://github.com/bede/hostile/blob/main/paper/supplementary-table-2.tsv) [FDA-ARGOS](https://www.ncbi.nlm.nih.gov/bioproject/231221) & [140](https://github.com/bede/hostile/blob/main/paper/supplementary-table-2.tsv) mycobacterial 150mers | [human-t2t-hla-argos985-mycob140.fa.gz](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla-argos985-mycob140.fa.gz) | [human-t2t-hla-argos985-mycob140.tar](https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o/human-t2t-hla-argos985-mycob140.tar) | 2023-07 |
 
 
 
 ## Install
 
-Installation with Conda/Miniconda or Docker is recommended due to non-Python dependencies (Minimap2, Bowtie2, Samtools, Bedtools). Hostile is tested with Ubuntu Linux 22.04, MacOS 12, and WSL2.
+Installation with conda/mamba or Docker is recommended due to non-Python dependencies (Bowtie2, Minimap2, Samtools and Bedtools). Hostile is tested with Ubuntu Linux 22.04, MacOS 12, and under WSL for Windows.
 
+**Conda/mamba**
 
+```bash
+conda create -n hostile -c conda-forge -c bioconda hostile  # Mamba/Micromamba are faster
+conda activate hostile
+```
 
-### Conda
+**Docker**
+
+[BioContainers](https://biocontainers.pro/tools/hostile) are built for each version
 
 ```bash
-curl -OJ https://raw.githubusercontent.com/bede/hostile/main/environment.yml
-conda env create -f environment.yml  # Use Mamba if impatient
-conda activate hostile
-pip install hostile
+docker run quay.io/biocontainers/hostile:0.0.3--pyhdfd78af_0
 ```
 
+**Python/pip**
+
+Manually install Bowtie2, Minimap2, Samtools and Bedtools
 
+```bash
+pip install hostile  # Requires python >= 3.10
+```
 
-### Development install
+**Development install**
 
 ```bash
 git clone https://github.com/bede/hostile.git
 cd hostile
-conda env create -f environment.yml  # Use Mamba if impatient
+conda env create -f environment.yml  # Mamba/Micromamba are faster
 conda activate hostile
 pip install --editable '.[dev]'
 pytest
 ```
 
 
 
@@ -76,15 +102,17 @@
   --force               overwrite existing output files
                         (default: False)
   --debug               show debug messages
                         (default: False)
 
 ```
 
-### Short reads
+
+
+**Short reads**
 
 ```bash
 $ hostile clean --fastq1 reads.r1.fastq.gz --fastq2 reads.r2.fastq.gz
 INFO: Using Bowtie2
 INFO: Found cached index (/Users/bede/Library/Application Support/hostile/human-t2t-hla)
 INFO: Cleaning…
 [
@@ -103,15 +131,25 @@
         "reads_out": 20,
         "reads_removed": 0,
         "reads_removed_proportion": 0.0
     }
 ]
 ```
 
-### Long reads
+```bash
+$ hostile clean --rename --fastq1 reads_1.fastq.gz --fastq2 reads_2.fastq.gz \
+  --index /path/to/human-t2t-hla-argos985-mycob140 > decontamination-log.json
+INFO: Using Bowtie2
+INFO: Found cached index (/Users/bede/Library/Application Support/hostile/human-t2t-hla)
+INFO: Cleaning…
+```
+
+
+
+**Long reads**
 
 ```bash
 $ hostile clean --fastq1 tests/data/h37rv_10.r1.fastq.gz
 INFO: Using Minimap2's long read preset (map-ont)
 INFO: Found cached reference (/Users/bede/Library/Application Support/hostile/human-t2t-hla.fa.gz)
 INFO: Cleaning…
 [
@@ -134,38 +172,40 @@
 
 ## Python usage
 
 ```python
 from pathlib import Path
 from hostile.lib import clean_paired_fastqs, ALIGNER
 
-# Short reads, defaults
+# Long reads, defaults
 clean_fastqs(
-    fastqs=[(data_dir / "reads_1.fastq.gz", data_dir / "reads_2.fastq.gz")],
+    fastqs=[Path("reads.fastq.gz")],
 )
 
-# Long reads, all the options, capture statistics
-statistics = lib.clean_paired_fastqs(
-    fastqs=[data_dir / "reads.fastq.gz"],
+# Paired short reads, all the options, capture log
+log = lib.clean_paired_fastqs(
+    fastqs=[(Path("reads_1.fastq.gz"), Path("reads_2.fastq.gz"))],
     aligner=ALIGNER.minimap2,
-    index=data_dir / "reference.fasta.gz",
-    out_dir=data_dir / "decontaminated-reads",
+    index=Path("reference.fasta.gz"),
+    out_dir=Path("decontaminated-reads"),
+    force=True,
     threads=4
 )
 
-print(stats)
+print(log)
 ```
 
 
 
 ## Masking reference genomes
 
 The `mask` subcommand makes it easy to create custom-masked reference genomes and achieve maximum retention of specific target organisms:
 ```bash
 hostile mask human.fasta lots-of-bacterial-genomes.fasta --threads 8
 ```
-​	You may wish to use one of the existing [reference genomes](#reference-genomes) as a starting point. Masking uses Minimap2's `asm10` preset to align the supplied target genomes with the reference genome, and bedtools to mask out all aligned regions. This feature requires a [development install](#development-install) until release in version 0.0.3. For Bowtie2—the default aligner for decontaminating short reads—you will also need to build an index before you can use your masked genome with Hostile.
+You may wish to use one of the existing [reference genomes](#reference-genomes) as a starting point. Masking uses Minimap2's `asm10` preset to align the supplied target genomes with the reference genome, and bedtools to mask out all aligned regions. For Bowtie2—the default aligner for decontaminating short reads—you will also need to build an index before you can use your masked genome with Hostile.
 
 ```bash
 bowtie2-build masked.fasta masked-index
 hostile clean --index masked-index --fastq1 reads_1.fastq.gz --fastq2 reads_2.fastq.gz
 ```
+
```

### Comparing `hostile-0.0.3/paper/supplementary-table-1.tsv` & `hostile-0.1.0/paper/supplementary-table-1.tsv`

 * *Files 25% similar despite different names*

```diff
@@ -1,19 +1,19 @@
-database	command	time_1	time_2	time_3	time_median	reads_out	spots_removed	total_reads	total_bp	retained_pc	throughput_mbp
-human	time hostile clean --threads 8 --fastq1 /data/bench2/real/human/err194147_10x.r1.fastq.gz --fastq2 /data/bench2/real/human/err194147_10x.r2.fastq.gz > hostile_bt2.illumina.human.human.json	1,232	1,299	1,350	1,299	262,830		199,510,296	20,150,539,896 	0.131738%	15.51
-human	time hostile clean --aligner minimap2 --threads 8 --fastq1 /data/bench2/real/human/rel7.10x.fastq.gz > hostile_mm2.ont.human.human.json	2,668	2,744	2,755	2,744	950		2,498,111	20,803,445,891 	0.038029%	7.58
-human	time hostile clean --threads 8 --fastq1 /data/bench2/simulated/bacteria/illumina.read1.fastq.gz --fastq2 /data/bench2/simulated/bacteria/illumina.read2.fastq.gz  > hostile_bt2.illumina.bacteria.human.json	3,526	3,559	3,512	3,526	273,511,300		273,511,602	41,026,740,300 	99.999890%	11.64
-human	time hostile clean --aligner minimap2 --threads 8 --fastq1 /data/bench2/simulated/bacteria/ont.fastq.gz > hostile_mm2.ont.bacteria.human.json	1,463	1,375	1,373	1,375	8,230,079		8,230,970	41,026,721,665 	99.989175%	29.84
-human	time hostile clean --threads 8 --fastq1 /data/bench2/simulated/mycobacteria/illumina.read1.fastq.gz --fastq2 /data/bench2/simulated/mycobacteria/illumina.read2.fastq.gz  > hostile_bt2.illumina.mycobacteria.human.json	648	680	685	680	51,360,120		51,360,128	7,704,019,200 	99.999984%	11.33
-human	time hostile clean --aligner minimap2 --threads 8 --fastq1 /data/bench2/simulated/mycobacteria/ont.fastq.gz > hostile_mm2.ont.mycobacteria.human.json	419	309	312	312	1,544,974		1,544,982	7,704,017,435 	99.999482%	24.69
-human-masked-bacteria-mycobacteria	time hostile clean --threads 8 --custom-index /data/bench2/human/bowtie2/human-masked-bacteria-mycobacteria --fastq1 /data/bench2/real/human/err194147_10x.r1.fastq.gz --fastq2 /data/bench2/real/human/err194147_10x.r2.fastq.gz > hostile_bt2.illumina.human.human-masked-bacteria-mycobacteria.json	1,681	1,196	1,215	1,215	263,312		199,510,296	20,150,539,896 	0.131979%	16.58
-human-masked-bacteria-mycobacteria	time hostile clean --aligner minimap2 --threads 8 --custom-index /data/bench2/human/human-masked-bacteria-mycobacteria.fa --fastq1 /data/bench2/real/human/rel7.10x.fastq.gz > hostile_mm2.ont.human.human-masked-bacteria-mycobacteria.json	3,154	2,743	2,747	2,747	951		2,498,111	20,803,445,891 	0.038069%	7.57
-human-masked-bacteria-mycobacteria	time hostile clean --threads 8 --custom-index /data/bench2/human/bowtie2/human-masked-bacteria-mycobacteria --fastq1 /data/bench2/simulated/bacteria/illumina.read1.fastq.gz --fastq2 /data/bench2/simulated/bacteria/illumina.read2.fastq.gz  > hostile_bt2.illumina.bacteria.human-masked-bacteria-mycobacteria.json	3,858	3,507	3,529	3,529	273,511,446		273,511,602	41,026,740,300 	99.999943%	11.63
-human-masked-bacteria-mycobacteria	time hostile clean --aligner minimap2 --threads 8 --custom-index /data/bench2/human/human-masked-bacteria-mycobacteria.fa --fastq1 /data/bench2/simulated/bacteria/ont.fastq.gz > hostile_mm2.ont.bacteria.human-masked-bacteria-mycobacteria.json	1,655	1,369	1,370	1,370	8,230,719		8,230,970	41,026,721,665 	99.996951%	29.95
-human-masked-bacteria-mycobacteria	time hostile clean --threads 8 --custom-index /data/bench2/human/bowtie2/human-masked-bacteria-mycobacteria --fastq1 /data/bench2/simulated/mycobacteria/illumina.read1.fastq.gz --fastq2 /data/bench2/simulated/mycobacteria/illumina.read2.fastq.gz  > hostile_bt2.illumina.mycobacteria.human-masked-bacteria-mycobacteria.json	798	687	691	691	51,360,128		51,360,128	7,704,019,200 	100.000000%	11.15
-human-masked-bacteria-mycobacteria	time hostile clean --aligner minimap2 --threads 8 --custom-index /data/bench2/human/human-masked-bacteria-mycobacteria.fa --fastq1 /data/bench2/simulated/mycobacteria/ont.fastq.gz > hostile_mm2.ont.mycobacteria.human-masked-bacteria-mycobacteria.json	464	309	309	309	1,544,982		1,544,982	7,704,017,435 	100.000000%	24.93
-	time zcat /data/bench2/real/human/err194147_10x.r12.fastq.gz  | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.illumina.human.fastq.gz	1,056	1,293	941	1,056		196,580,144	199,510,296	20,150,539,896 	1.468672%	19.08
-	time zcat /data/bench2/real/human/rel7.10x.fastq.gz  | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.ont.human.fastq.gz	448	449	446	448		2,497,178	2,498,111	20,803,445,891 	0.037348%	46.44
-	time zcat /data/bench2/simulated/bacteria/illumina.read12.10x.fastq.gz  | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.illumina.bacteria.fastq.gz	1,056	937	930	937		3,396	273,511,602	41,026,740,300 	99.998758%	43.79
-	time zcat /data/bench2/simulated/bacteria/ont.fastq.gz  | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.ont.bacteria.fastq.gz	5,565	5,559	4,625	5,559		905	8,230,970	41,026,721,665 	99.989005%	7.38
-	time zcat /data/bench2/simulated/mycobacteria/illumina.read12.10x.fastq.gz  | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.illumina.mycobacteria.fastq.gz	1,160	774	838	838		68	51,360,128	7,704,019,200 	99.999868%	9.19
-	time zcat /data/bench2/simulated/mycobacteria/ont.fastq.gz  | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.ont.mycobacteria.fastq.gz	808	714	985	808		21	1,544,982	7,704,017,435 	99.998641%	9.53
+name	tool	database	command	time_1	time_2	time_3	time_median	reads_total	bp_total	reads_retained_before_repair	reads_retained	reads_removed	reads_retained_pc	throughput_mbp
+hostile_bt2.illumina.human10x	Hostile 0.0.2	human-t2t-hla	hostile clean --threads 8 --fastq1 /data/bench2/real/human/err194147_10x.r1.fastq.gz --fastq2 /data/bench2/real/human/err194147_10x.r2.fastq.gz > hostile_bt2.illumina.human.human.json	1232	1299	1350	1299	199510296	20150539896		262830	199247466	0.131738%	15.51
+hostile_mm2.ont.human10x	Hostile 0.0.2	human-t2t-hla	hostile clean --aligner minimap2 --threads 8 --fastq1 /data/bench2/real/human/rel7.10x.fastq.gz > hostile_mm2.ont.human.human.json	2668	2744	2755	2744	2498111	20803445891		950	2497161	0.038029%	7.58
+hostile_bt2.illumina.bacteria	Hostile 0.0.2	human-t2t-hla	hostile clean --threads 8 --fastq1 /data/bench2/simulated/bacteria/illumina.read1.fastq.gz --fastq2 /data/bench2/simulated/bacteria/illumina.read2.fastq.gz > hostile_bt2.illumina.bacteria.human.json	3526	3559	3512	3526	273511602	41026740300		273511300	302	99.999890%	11.64
+hostile_mm2.ont.bacteria	Hostile 0.0.2	human-t2t-hla	hostile clean --aligner minimap2 --threads 8 --fastq1 /data/bench2/simulated/bacteria/ont.fastq.gz > hostile_mm2.ont.bacteria.human.json	1463	1375	1373	1375	8230970	41026721665		8230079	891	99.989175%	29.84
+hostile_bt2.illumina.mycobacteria	Hostile 0.0.2	human-t2t-hla	hostile clean --threads 8 --fastq1 /data/bench2/simulated/mycobacteria/illumina.read1.fastq.gz --fastq2 /data/bench2/simulated/mycobacteria/illumina.read2.fastq.gz > hostile_bt2.illumina.mycobacteria.human.json	648	680	685	680	51360128	51360128		51360120	8	99.999984%	0.08
+hostile_mm2.ont.mycobacteria	Hostile 0.0.2	human-t2t-hla	hostile clean --aligner minimap2 --threads 8 --fastq1 /data/bench2/simulated/mycobacteria/ont.fastq.gz > hostile_mm2.ont.mycobacteria.human.json	419	309	312	312	1544982	7704017435		1544974	8	99.999482%	24.69
+hostile_bt2.illumina.human10x	Hostile 0.0.2	human-t2t-hla-argos985-mycob140	hostile clean --threads 8 --custom-index /data/bench2/human/bowtie2/human-masked-bacteria-mycobacteria --fastq1 /data/bench2/real/human/err194147_10x.r1.fastq.gz --fastq2 /data/bench2/real/human/err194147_10x.r2.fastq.gz > hostile_bt2.illumina.human.human-masked-bacteria-mycobacteria.json	1681	1196	1215	1215	199510296	20150539896		263312	199246984	0.131979%	16.58
+hostile_mm2.ont.human10x	Hostile 0.0.2	human-t2t-hla-argos985-mycob140	hostile clean --aligner minimap2 --threads 8 --custom-index /data/bench2/human/human-masked-bacteria-mycobacteria.fa --fastq1 /data/bench2/real/human/rel7.10x.fastq.gz > hostile_mm2.ont.human.human-masked-bacteria-mycobacteria.json	3154	2743	2747	2747	2498111	20803445891		951	2497160	0.038069%	7.57
+hostile_bt2.illumina.bacteria	Hostile 0.0.2	human-t2t-hla-argos985-mycob140	hostile clean --threads 8 --custom-index /data/bench2/human/bowtie2/human-masked-bacteria-mycobacteria --fastq1 /data/bench2/simulated/bacteria/illumina.read1.fastq.gz --fastq2 /data/bench2/simulated/bacteria/illumina.read2.fastq.gz > hostile_bt2.illumina.bacteria.human-masked-bacteria-mycobacteria.json	3858	3507	3529	3529	273511602	41026740300		273511446	156	99.999943%	11.63
+hostile_mm2.ont.bacteria	Hostile 0.0.2	human-t2t-hla-argos985-mycob140	hostile clean --aligner minimap2 --threads 8 --custom-index /data/bench2/human/human-masked-bacteria-mycobacteria.fa --fastq1 /data/bench2/simulated/bacteria/ont.fastq.gz > hostile_mm2.ont.bacteria.human-masked-bacteria-mycobacteria.json	1655	1369	1370	1370	8230970	41026721665		8230719	251	99.996951%	29.95
+hostile_bt2.illumina.mycobacteria	Hostile 0.0.2	human-t2t-hla-argos985-mycob140	hostile clean --threads 8 --custom-index /data/bench2/human/bowtie2/human-masked-bacteria-mycobacteria --fastq1 /data/bench2/simulated/mycobacteria/illumina.read1.fastq.gz --fastq2 /data/bench2/simulated/mycobacteria/illumina.read2.fastq.gz > hostile_bt2.illumina.mycobacteria.human-masked-bacteria-mycobacteria.json	798	687	691	691	51360128	7704019200		51360128	0	100.000000%	11.15
+hostile_mm2.ont.mycobacteria	Hostile 0.0.2	human-t2t-hla-argos985-mycob140	hostile clean --aligner minimap2 --threads 8 --custom-index /data/bench2/human/human-masked-bacteria-mycobacteria.fa --fastq1 /data/bench2/simulated/mycobacteria/ont.fastq.gz > hostile_mm2.ont.mycobacteria.human-masked-bacteria-mycobacteria.json	464	309	309	309	1544982	7704017435		1544982	0	100.000000%	24.93
+scrubber.illumina.human10x	HRRT 2.1.0	default	zcat /data/bench2/real/human/err194147_10x.r12.fastq.gz | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.illumina.human.fastq.gz	1056	1293	941	1056	199510296	20150539896	2930152	318232	199192064	0.159507%	19.08
+scrubber.ont.human10x	HRRT 2.1.0	default	zcat /data/bench2/real/human/rel7.10x.fastq.gz | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.ont.human.fastq.gz	448	449	446	448	2498111	20803445891		933	2497178	0.037348%	46.44
+scrubber.illumina.bacteria	HRRT 2.1.0	default	zcat /data/bench2/simulated/bacteria/illumina.read12.10x.fastq.gz | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.illumina.bacteria.fastq.gz	1056	937	930	937	273511602	41026740300	273508206	273504828	6774	99.997523%	43.79
+scrubber.ont.bacteria	HRRT 2.1.0	default	zcat /data/bench2/simulated/bacteria/ont.fastq.gz | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.ont.bacteria.fastq.gz	5565	5559	4625	5559	8230970	41026721665		8230065	905	99.989005%	7.38
+scrubber.illumina.mycobacteria	HRRT 2.1.0	default	zcat /data/bench2/simulated/mycobacteria/illumina.read12.10x.fastq.gz | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.illumina.mycobacteria.fastq.gz	1160	774	838	838	51360128	7704019200	51360060	51360000	128	99.999751%	9.19
+scrubber.ont.mycobacteria	HRRT 2.1.0	default	zcat /data/bench2/simulated/mycobacteria/ont.fastq.gz | /data/bench2/sra-human-scrubber/scripts/scrub.sh -x -p 8 | pigz -p 8 > scrubber.ont.mycobacteria.fastq.gz	808	714	985	808	1544982	7704017435		1544961	21	99.998641%	9.53
```

### Comparing `hostile-0.0.3/paper/supplementary-table-2.tsv` & `hostile-0.1.0/paper/supplementary-table-3.tsv`

 * *Files 6% similar despite different names*

```diff
@@ -1,8 +1,37 @@
 dataset	type	accession
+Human Illumina 10x	reads	ERR194147
+Human ONT 10x	reads	http://s3.amazonaws.com/nanopore-human-wgs/rel7/rel_7.fastq.gz
+Human Illumina 30x	reads	ERR3239334
+Human Illumina 30x	reads	ERR3239480
+Human Illumina 30x	reads	ERR3239491
+Human Illumina 30x	reads	ERR3239492
+Human Illumina 30x	reads	ERR3239557
+Human Illumina 30x	reads	ERR3239683
+Human Illumina 30x	reads	ERR3239832
+Human Illumina 30x	reads	ERR3239893
+Human Illumina 30x	reads	ERR3239894
+Human Illumina 30x	reads	ERR3239997
+Human Illumina 30x	reads	ERR3240184
+Human Illumina 30x	reads	ERR3240193
+Human Illumina 30x	reads	ERR3240223
+Human Illumina 30x	reads	ERR3241843
+Human Illumina 30x	reads	ERR3241862
+Human Illumina 30x	reads	ERR3242189
+Human Illumina 30x	reads	ERR3242199
+Human Illumina 30x	reads	ERR3242202
+Human Illumina 30x	reads	ERR3242208
+Human Illumina 30x	reads	ERR3242214
+Human Illumina 30x	reads	ERR3242540
+Human Illumina 30x	reads	ERR3242585
+Human Illumina 30x	reads	ERR3242627
+Human Illumina 30x	reads	ERR3242642
+Human Illumina 30x	reads	ERR3242892
+Human Illumina 30x	reads	ERR3242910
+Human Illumina 30x	reads	ERR3242940
 Bacteria	assembly	GCA_000626615.3
 Bacteria	assembly	GCA_001559115.2
 Bacteria	assembly	GCA_002209185.2
 Bacteria	assembly	GCA_002953975.1
 Bacteria	assembly	GCA_003812545.1
 Bacteria	assembly	GCA_008693625.1
 Bacteria	assembly	GCA_013267255.1
@@ -1119,8 +1148,8 @@
 Mycobacteria	assembly	GCA_010730745.1
 Mycobacteria	assembly	GCA_010731715.1
 Mycobacteria	assembly	GCA_013466425.1
 Mycobacteria	assembly	GCA_016919645.1
 Mycobacteria	assembly	GCA_020616615.1
 Mycobacteria	assembly	GCA_022374935.2
 Mycobacteria	assembly	GCA_900292015.1
-Mycobacteria	assembly	GCF_019668465.1
+Mycobacteria	assembly	GCF_019668465.1
```

### Comparing `hostile-0.0.3/pyproject.toml` & `hostile-0.1.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/src/hostile/aligner.py` & `hostile-0.1.0/src/hostile/aligner.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,59 +1,66 @@
 import logging
+import shutil
 import subprocess
+import tempfile
 
 from dataclasses import dataclass
 from pathlib import Path
 
 from hostile import util
 
 
 @dataclass
 class Aligner:
     name: str
     short_name: str
     bin_path: Path
     cdn_base_url: str
-    working_dir: Path
+    data_dir: Path
     cmd: str
     paired_cmd: str
     idx_archive_fn: str = ""
     ref_archive_fn: str = ""
     idx_name: str = ""
-    idx_paths: tuple[Path] = tuple()
+    idx_paths: tuple[Path, ...] = tuple()
 
     def __post_init__(self):
         self.ref_archive_url = f"{self.cdn_base_url}/{self.ref_archive_fn}"
         self.idx_archive_url = f"{self.cdn_base_url}/{self.idx_archive_fn}"
-        self.ref_archive_path = self.working_dir / self.ref_archive_fn
-        self.idx_archive_path = self.working_dir / self.idx_archive_fn
-        self.idx_path = self.working_dir / self.idx_name
-        Path(self.working_dir).mkdir(exist_ok=True, parents=True)
+        self.ref_archive_path = self.data_dir / self.ref_archive_fn
+        self.idx_archive_path = self.data_dir / self.idx_archive_fn
+        self.idx_path = self.data_dir / self.idx_name
+        Path(self.data_dir).mkdir(exist_ok=True, parents=True)
 
     def check(self, using_custom_index: bool):
         """Test aligner and check/download a ref/index if necessary"""
         if not using_custom_index:  # Check for and if necessary fetch a genome/index
             if self.name == "Bowtie2":
                 if not all(path.exists() for path in self.idx_paths):
-                    self.working_dir.mkdir(exist_ok=True, parents=True)
-                    logging.info(f"Fetching human index")
-                    util.download(self.idx_archive_url, self.idx_archive_path)
-                    util.untar_file(self.idx_archive_path, self.working_dir)
-                    self.idx_archive_path.unlink()
+                    self.data_dir.mkdir(exist_ok=True, parents=True)
+                    logging.info(f"Fetching human index ({self.idx_archive_url})")
+                    with tempfile.NamedTemporaryFile() as temporary_file:
+                        tmp_path = Path(temporary_file.name)
+                        util.download(self.idx_archive_url, tmp_path)
+                        logging.info("Extracting index…")
+                        util.untar_file(tmp_path, self.data_dir)
                     logging.info(f"Saved human index ({self.idx_path})")
                 else:
                     logging.info(f"Found cached index ({self.idx_path})")
             elif self.name == "Minimap2":
                 if not self.ref_archive_path.exists():
-                    util.download(self.ref_archive_url, self.ref_archive_path)
+                    with tempfile.NamedTemporaryFile(delete=False) as temporary_file:
+                        tmp_path = Path(temporary_file.name)
+                        util.download(self.ref_archive_url, tmp_path)
+                        shutil.move(tmp_path, self.ref_archive_path)
                     logging.info(f"Saved human reference ({self.ref_archive_path})")
                 else:
                     logging.info(f"Found cached reference ({self.ref_archive_path})")
         try:
-            util.run(f"{self.bin_path} --version", cwd=self.working_dir)
+            util.run(f"{self.bin_path} --version", cwd=self.data_dir)
         except subprocess.CalledProcessError:
             logging.warning(f"Failed to execute {self.bin_path}")
             raise RuntimeError(f"Failed to execute {self.bin_path}")
 
     def gen_clean_cmd(
         self,
         fastq: Path,
@@ -80,36 +87,36 @@
         cmd_template = {  # Templating for Aligner.cmd
             "{BIN_PATH}": str(self.bin_path),
             "{REF_ARCHIVE_PATH}": str(self.ref_archive_path),
             "{INDEX_PATH}": str(self.idx_path),
             "{FASTQ}": str(fastq),
             "{THREADS}": str(threads),
         }
+        alignment_cmd = self.cmd
         for k in cmd_template.keys():
-            self.cmd = self.cmd.replace(k, cmd_template[k])
+            alignment_cmd = alignment_cmd.replace(k, cmd_template[k])
         rename_cmd = (
             ' | awk \'BEGIN{{FS=OFS="\\t"}} {{$1=int((NR+1)/2)" "; print $0}}\''
             if rename
             else ""
         )
         cmd = (
             # Align, stream reads to stdout in SAM format
-            f"{self.cmd}"
+            f"{alignment_cmd}"
             # Count reads in stream before filtering (2048 + 256 = 2304)
             f" | tee >(samtools view -F 2304 -c - > '{count_before_path}')"
             # Discard mapped reads
             f" | samtools view -f 4 -"
             # Count reads in stream after filtering
             f" | tee >(samtools view -F 256 -c - > '{count_after_path}')"
             # Optionally replace paired read headers with integers
             f"{rename_cmd}"
             # Stream remaining records into fastq files
             f" | samtools fastq --threads 2 -c 6 -0 '{fastq_out_path}'"
         )
-        logging.debug(f"{cmd}")
         return cmd
 
     def gen_paired_clean_cmd(
         self,
         fastq1: Path,
         fastq2: Path,
         out_dir: Path,
@@ -138,30 +145,30 @@
             "{BIN_PATH}": str(self.bin_path),
             "{REF_ARCHIVE_PATH}": str(self.ref_archive_path),
             "{INDEX_PATH}": str(self.idx_path),
             "{FASTQ1}": str(fastq1),
             "{FASTQ2}": str(fastq2),
             "{THREADS}": str(threads),
         }
+        alignment_cmd = self.paired_cmd
         for k in cmd_template.keys():
-            self.paired_cmd = self.paired_cmd.replace(k, cmd_template[k])
+            alignment_cmd = alignment_cmd.replace(k, cmd_template[k])
         rename_cmd = (
             f' | awk \'BEGIN{{FS=OFS="\\t"}} {{$1=int((NR+1)/2)" "; print $0}}\''
             if rename
             else ""
         )
         cmd = (
             # Align, stream reads to stdout in SAM format
-            f"{self.paired_cmd}"
+            f"{alignment_cmd}"
             # Count reads in stream before filtering (2048 + 256 = 2304)
             f" | tee >(samtools view -F 2304 -c - > '{count_before_path}')"
             # Discard mapped reads and reads with mapped mates
             f" | samtools view -f 12 -"
             # Count reads in stream after filtering
             f" | tee >(samtools view -F 256 -c - > '{count_after_path}')"
             # Optionally replace paired read headers with integers
             f"{rename_cmd}"
             # Stream remaining records into fastq files
             f" | samtools fastq --threads 2 -c 6 -N -1 '{fastq1_out_path}' -2 '{fastq2_out_path}'"
         )
-        logging.debug(f"{cmd}")
         return cmd
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `hostile-0.0.3/src/hostile/cli.py` & `hostile-0.1.0/src/hostile/cli.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 import json
+import logging
 from enum import Enum
 from pathlib import Path
 
 import defopt
 
 from hostile import lib
 
@@ -37,26 +38,26 @@
     :arg rename: replace read names with incrementing integers
     :arg out_dir: path to output directory
     :arg threads: number of CPU threads to use
     :arg force: overwrite existing output files
     :arg debug: show debug messages
     """
 
-    # Choose a sensible aligner
+    if debug:
+        logging.getLogger().setLevel(logging.DEBUG)
     aligner_paired = (
         lib.ALIGNER.bowtie2
         if aligner == ALIGNER.auto or aligner == ALIGNER.bowtie2
         else lib.ALIGNER.minimap2
     )
     aligner_unpaired = (
         lib.ALIGNER.minimap2
         if aligner == ALIGNER.auto or aligner == ALIGNER.minimap2
         else lib.ALIGNER.bowtie2
     )
-
     if fastq2:
         stats = lib.clean_paired_fastqs(
             [(fastq1, fastq2)],
             index=index,
             rename=rename,
             out_dir=out_dir,
             aligner=aligner_paired,
@@ -72,14 +73,37 @@
             aligner=aligner_unpaired,
             threads=threads,
             force=force,
         )
     print(json.dumps(stats, indent=4))
 
 
+def mask(
+    reference: Path, target: Path, out_dir: Path = Path("masked"), threads: int = 1
+) -> None:
+    """
+    Mask reference genome against target genome[s]
+
+    :arg reference: path to reference genome in fasta[.gz] format
+    :arg target: path to target genome(s) in fasta[.gz] format
+    :arg out_dir: path to output directory
+    :arg threads: number of threads to use
+    """
+    lib.mask(reference=reference, target=target, out_dir=out_dir, threads=threads)
+
+
+def main():
+    defopt.run(
+        {"clean": clean, "mask": mask},
+        no_negated_flags=True,
+        strict_kwonly=False,
+        short={},
+    )
+
+
 # def clean_many(
 #     *fastqs: str,
 #     aligner: lib.ALIGNER = lib.ALIGNER.bowtie2,
 #     index: Path | None = None,
 #     out_dir: Path = lib.CWD,
 #     threads: int = lib.THREADS,
 #     debug: bool = False,
@@ -105,30 +129,7 @@
 #             index=index,
 #         )
 #         print(json.dumps(stats, indent=4))
 #     else:
 #         raise NotImplementedError(
 #             "Forward and reverse fastq(.gz) paths should be separated with a comma"
 #         )
-
-
-def mask(
-    reference: Path, target: Path, out_dir: Path = Path("masked"), threads: int = 1
-) -> None:
-    """
-    Mask reference genome against target genome[s]
-
-    :arg reference: path to reference genome in fasta[.gz] format
-    :arg target: path to target genome(s) in fasta[.gz] format
-    :arg out_dir: path to output directory
-    :arg threads: number of threads to use
-    """
-    lib.mask(reference=reference, target=target, out_dir=out_dir, threads=threads)
-
-
-def main():
-    defopt.run(
-        {"clean": clean, "mask": mask},
-        no_negated_flags=True,
-        strict_kwonly=False,
-        short={},
-    )
```

### Comparing `hostile-0.0.3/src/hostile/lib.py` & `hostile-0.1.0/src/hostile/lib.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,40 +1,45 @@
 import logging
 import gzip
-import json
 import multiprocessing
 import shutil
+import subprocess
 
 from enum import Enum
 from dataclasses import dataclass
 from pathlib import Path
 
 from platformdirs import user_data_dir
 
 from hostile import util
 from hostile.aligner import Aligner
 
 
-logging.basicConfig(format="%(levelname)s: %(message)s", level=logging.INFO)
+logging.basicConfig(
+    format="%(asctime)s %(levelname)s: %(message)s",
+    datefmt="%H:%M:%S",
+    level=logging.INFO,
+)
 
 
 CWD = Path.cwd().resolve()
 XDG_DATA_DIR = Path(user_data_dir("hostile", "Bede Constantinides"))
 THREADS = multiprocessing.cpu_count()
 
 
 ALIGNER = Enum(
     "Aligner",
     {
         "bowtie2": Aligner(
             name="Bowtie2",
             short_name="bt2",
             bin_path=Path("bowtie2"),
+            # cdn_base_url="http://localhost:8000",  # python -m http.server
             cdn_base_url=f"https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o",
-            working_dir=XDG_DATA_DIR,
+            data_dir=XDG_DATA_DIR,
             cmd=("{BIN_PATH} -x '{INDEX_PATH}' -U '{FASTQ}'" " -k 1 --mm -p {THREADS}"),
             paired_cmd=(
                 "{BIN_PATH} -x '{INDEX_PATH}' -1 '{FASTQ1}' -2 '{FASTQ2}'"
                 " -k 1 --mm -p {THREADS}"
             ),
             idx_archive_fn="human-t2t-hla.tar",
             idx_name="human-t2t-hla",
@@ -47,16 +52,17 @@
                 XDG_DATA_DIR / "human-t2t-hla.rev.2.bt2",
             ),
         ),
         "minimap2": Aligner(
             name="Minimap2",
             short_name="mm2",
             bin_path=Path("minimap2"),
+            # cdn_base_url="http://localhost:8000",  # python -m http.server
             cdn_base_url=f"https://objectstorage.uk-london-1.oraclecloud.com/n/lrbvkel2wjot/b/human-genome-bucket/o",
-            working_dir=XDG_DATA_DIR,
+            data_dir=XDG_DATA_DIR,
             cmd="{BIN_PATH} -ax map-ont --secondary no -t {THREADS} '{REF_ARCHIVE_PATH}' '{FASTQ}'",
             paired_cmd="{BIN_PATH} -ax sr -m 40 --secondary no -t {THREADS} '{REF_ARCHIVE_PATH}' '{FASTQ1}' '{FASTQ2}'",
             ref_archive_fn="human-t2t-hla.fa.gz",
             idx_name="human-t2t-hla.fa.gz",
         ),
     },
 )
@@ -77,16 +83,16 @@
     fastq2_in_name: str | None = None
     fastq2_in_path: str | None = None
     fastq2_out_name: str | None = None
     fastq2_out_path: str | None = None
 
 
 def gather_stats(
-    fastqs: list[Path, Path], out_dir: Path, aligner: str, index: Path | None
-) -> dict[str, dict[str : str | int | float]]:
+    fastqs: list[Path], out_dir: Path, aligner: str, index: Path | None
+) -> list[dict[str, str | int | float]]:
     stats = []
     for fastq1 in fastqs:
         fastq1_stem = util.fastq_path_to_stem(fastq1)
         fastq1_out_path = out_dir / f"{fastq1_stem}.clean.fastq.gz"
         n_reads_in_path = out_dir / (fastq1_stem + ".reads_in.txt")
         n_reads_out_path = out_dir / (fastq1_stem + ".reads_out.txt")
         n_reads_in = util.parse_count_file(n_reads_in_path)
@@ -97,15 +103,15 @@
         try:
             proportion_removed = round(n_reads_removed / n_reads_in, 5)
         except ArithmeticError:  # ZeroDivisionError
             proportion_removed = float(0)
         index_fmt = (
             index
             if index
-            else Path(ALIGNER[aligner].value.working_dir)
+            else Path(ALIGNER[aligner].value.data_dir)
             / Path(ALIGNER[aligner].value.idx_name)
         )
         report = SampleReport(
             aligner=aligner,
             index=str(index_fmt),
             fastq1_in_name=fastq1.name,
             fastq1_in_path=str(fastq1),
@@ -118,15 +124,15 @@
         ).__dict__
         stats.append({k: v for k, v in report.items() if v is not None})
     return stats
 
 
 def gather_stats_paired(
     fastqs: list[tuple[Path, Path]], out_dir: Path, aligner: str, index: Path | None
-) -> dict[str, dict[str : str | int | float]]:
+) -> list[dict[str, str | int | float]]:
     stats = []
     for fastq1, fastq2 in fastqs:
         fastq1_stem = util.fastq_path_to_stem(fastq1)
         fastq2_stem = util.fastq_path_to_stem(fastq2)
         fastq1_out_path = out_dir / f"{fastq1_stem}.clean_1.fastq.gz"
         fastq2_out_path = out_dir / f"{fastq2_stem}.clean_2.fastq.gz"
         n_reads_in_path = out_dir / (fastq1_stem + ".reads_in.txt")
@@ -139,15 +145,15 @@
         try:
             proportion_removed = round(n_reads_removed / n_reads_in, 5)
         except ArithmeticError:  # ZeroDivisionError
             proportion_removed = float(0)
         index_fmt = (
             index
             if index
-            else Path(ALIGNER[aligner].value.working_dir)
+            else Path(ALIGNER[aligner].value.data_dir)
             / Path(ALIGNER[aligner].value.idx_name)
         )
         stats.append(
             SampleReport(
                 aligner=aligner,
                 index=str(index_fmt),
                 fastq1_in_name=fastq1.name,
@@ -172,15 +178,15 @@
     aligner = preferred_aligner
     try:
         aligner.value.check(using_custom_index=using_custom_index)
     except Exception as e:
         if aligner == ALIGNER.bowtie2:
             aligner = ALIGNER.minimap2
             logging.warning(f"Using Minimap2 instead of Bowtie2")
-            aligner.value.check()
+            aligner.value.check(using_custom_index=using_custom_index)
         else:
             raise e
     return aligner
 
 
 def clean_fastqs(
     fastqs: list[Path],
@@ -190,72 +196,75 @@
     aligner: ALIGNER = ALIGNER.minimap2,
     threads: int = THREADS,
     force: bool = False,
 ):
     if aligner == ALIGNER.bowtie2:
         logging.info("Using Bowtie2")
     elif aligner == ALIGNER.minimap2:
-        logging.info("Using Minimap2's long read preset (map-ont)")
+        logging.info("Using Minimap2's long read preset")
     fastqs = [Path(path).resolve() for path in fastqs]
     if not all(fastq.is_file() for fastq in fastqs):
         raise FileNotFoundError("One or more fastq files do not exist")
     Path(out_dir).mkdir(exist_ok=True, parents=True)
     aligner = choose_aligner(aligner, using_custom_index=bool(index))
-    backend_cmds = {
-        fastq: aligner.value.gen_clean_cmd(
-            Path(fastq),
+    backend_cmds = [
+        aligner.value.gen_clean_cmd(
+            fastq=fastq,
             out_dir=out_dir,
             index=index,
             rename=rename,
             threads=threads,
             force=force,
         )
         for fastq in fastqs
-    }
+    ]
     logging.info("Cleaning…")
     util.run_bash_parallel(backend_cmds, description="Cleaning")
     stats = gather_stats(fastqs, out_dir=out_dir, aligner=aligner.name, index=index)
+    logging.info("Complete")
     return stats
 
 
 def clean_paired_fastqs(
     fastqs: list[tuple[Path, Path]],
     index: Path | None = None,
     rename: bool = False,
     out_dir: Path = CWD,
     aligner: ALIGNER = ALIGNER.bowtie2,
     threads: int = THREADS,
     force: bool = False,
 ):
     if aligner == ALIGNER.bowtie2:
-        logging.info("Using Bowtie2")
+        logging.info("Using Bowtie2 (paired reads)")
     elif aligner == ALIGNER.minimap2:
-        logging.info("Using Minimap2's short read preset (sr)")
+        logging.info("Using Minimap2's short read preset (paired reads)")
     fastqs = [(Path(path1).resolve(), Path(path2).resolve()) for path1, path2 in fastqs]
     if not all(path.is_file() for fastq_pair in fastqs for path in fastq_pair):
         raise FileNotFoundError("One or more fastq files do not exist")
     Path(out_dir).mkdir(exist_ok=True, parents=True)
     aligner = choose_aligner(aligner, using_custom_index=bool(index))
-    backend_cmds = {
-        p: aligner.value.gen_paired_clean_cmd(
-            Path(p[0]),
-            Path(p[1]),
+    backend_cmds = [
+        aligner.value.gen_paired_clean_cmd(
+            fastq1=pair[0],
+            fastq2=pair[1],
             out_dir=out_dir,
             index=index,
             rename=rename,
             threads=threads,
             force=force,
         )
-        for p in fastqs
-    }
+        for pair in fastqs
+    ]
+    logging.debug(f"{backend_cmds=}")
     logging.info("Cleaning…")
     util.run_bash_parallel(backend_cmds, description="Cleaning")
     stats = gather_stats_paired(
         fastqs, out_dir=out_dir, aligner=aligner.name, index=index
     )
+    logging.info("Complete")
     return stats
 
 
 def mask(
     reference: Path, target: Path, out_dir=Path("masked"), threads: int = 1
 ) -> Path:
     """Mask a fasta[.gz] reference genome against fasta.[gz] target genomes"""
```

### Comparing `hostile-0.0.3/src/hostile/util.py` & `hostile-0.1.0/src/hostile/util.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import concurrent.futures
+import logging
 import subprocess
 import tarfile
 
-from functools import partial
 from pathlib import Path
 
 import httpx
 
 from tqdm import tqdm
 
 
@@ -19,54 +19,69 @@
 def run_bash(cmd: str, cwd: Path | None = None) -> subprocess.CompletedProcess:
     """Needed because /bin/sh does not support process substitution used for tee"""
     return subprocess.run(
         ["/bin/bash", "-c", cmd], cwd=cwd, check=True, text=True, capture_output=True
     )
 
 
+def handle_alignment_exceptions(exception: subprocess.CalledProcessError) -> None:
+    """Catch samtools view's non-zero exit if all input reads are contaminated"""
+    alignment_successful = False
+    stream_empty = False
+    if 'Failed to read header for "-"' in exception.stderr:
+        stream_empty = True
+    if "overall alignment rate" in exception.stderr:  # Bowtie2
+        alignment_successful = True
+    if "Peak RSS" in exception.stderr:  # Minimap2
+        alignment_successful = True
+    logging.debug(f"{stream_empty=} {alignment_successful=}")
+    if alignment_successful and stream_empty:  # Non zero exit but actually fine
+        pass
+    else:
+        print(f"Hostile encountered a problem. Stderr below")
+        print(f"{exception.stderr}")
+        raise exception
+
+
 def run_bash_parallel(
-    cmds: dict[str, str], cwd: Path | None = None, description: str = "Processing tasks"
-) -> dict[str, subprocess.CompletedProcess]:
+    cmds: list[str], description: str = "Processing"
+) -> dict[int, subprocess.CompletedProcess]:
     with concurrent.futures.ThreadPoolExecutor(max_workers=1) as x:
-        futures = {
-            x.submit(partial(run_bash, cwd=cwd), cmd): k for k, cmd in cmds.items()
-        }
+        futures = [x.submit(run_bash, cmd) for cmd in cmds]
         results = {}
         for future in tqdm(
             concurrent.futures.as_completed(futures),
             total=len(futures),
             desc=description,
             disable=len(cmds) == 1,
         ):
-            key = futures[future]
+            i = futures.index(future)
             try:
-                results[key] = future.result()
-            except Exception as e:
-                print(f"Exception occurred during executing command:")
-                print(f"{cmds[key]}")
-                print(f"stderr:")
-                print(f"{e.stderr}")
+                results[i] = future.result()
+            except subprocess.CalledProcessError as e:
+                handle_alignment_exceptions(e)
         return results
 
 
 def fastq_path_to_stem(fastq_path: Path) -> str:
     fastq_path = Path(fastq_path)
-    return fastq_path.name.removesuffix(fastq_path.suffixes[-1]).removesuffix(
-        fastq_path.suffixes[-2]
-    )
+    stem = fastq_path.name.removesuffix(".gz")
+    for suffix in (".fastq", ".fq"):
+        stem = stem.removesuffix(suffix)
+    return stem
 
 
 def parse_count_file(path: Path) -> int:
-    # logging.info(f"{path=}")
     try:
         with open(path, "r") as fh:
-            print()
             count = int(fh.read().strip())
     except ValueError:  # file is empty and count is zero
+        logging.debug(f"Count file missing: {path}")
         count = 0
+    logging.debug(f"{path=} {count=}")
     return count
 
 
 def untar_file(input_path, output_path):
     with tarfile.open(input_path) as fh:
         fh.extractall(path=output_path)
```

### Comparing `hostile-0.0.3/tests/data/MN908947/MN908947.1.bt2` & `hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.1.bt2`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/tests/data/MN908947/MN908947.2.bt2` & `hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.2.bt2`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/tests/data/MN908947/MN908947.4.bt2` & `hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.4.bt2`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/tests/data/MN908947/MN908947.fasta.gz` & `hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.fasta.gz`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/tests/data/MN908947/MN908947.rev.1.bt2` & `hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.rev.1.bt2`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/tests/data/MN908947/MN908947.rev.2.bt2` & `hostile-0.1.0/tests/data/sars-cov-2/sars-cov-2.rev.2.bt2`

 * *Files identical despite different names*

### Comparing `hostile-0.0.3/tests/data/MN908947/partial-for-mask-testing.fa.gz` & `hostile-0.1.0/tests/data/sars-cov-2/partial-for-mask-testing.fa.gz`

 * *Files identical despite different names*

