# Comparing `tmp/yxr_oi_cli-0.2.2.1.tar.gz` & `tmp/yxr_oi_cli-0.2.2.2.tar.gz`

## Comparing `yxr_oi_cli-0.2.2.1.tar` & `yxr_oi_cli-0.2.2.2.tar`

### file list

```diff
@@ -1,73 +1,73 @@
--rw-r--r--   0        0        0       24 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/__init__.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/py.typed
--rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/abstract/HtmlTagAbstract.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/abstract/__init__.py
--rw-r--r--   0        0        0        1 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/__init__.py
--rw-r--r--   0        0        0     4246 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/account.py
--rw-r--r--   0        0        0     2762 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/analyze.py
--rwxr-xr-x   0        0        0     1479 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/completion.py
--rw-r--r--   0        0        0      842 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/config.py
--rw-r--r--   0        0        0      715 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/constant.py
--rw-r--r--   0        0        0    10692 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/contest.py
--rw-r--r--   0        0        0      547 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/init.py
--rwxr-xr-x   0        0        0     1280 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/lang.py
--rwxr-xr-x   0        0        0     1102 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/main.py
--rw-r--r--   0        0        0     4355 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/problem.py
--rw-r--r--   0        0        0      513 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/reg_list.py
--rwxr-xr-x   0        0        0     4684 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/submit.py
--rw-r--r--   0        0        0     3468 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/template.py
--rwxr-xr-x   0        0        0     3450 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/test.py
--rw-r--r--   0        0        0     7399 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/adaptor/AtCoderAdaptor.py
--rw-r--r--   0        0        0      851 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/adaptor/CodeforcesAdaptor.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/adaptor/__init__.py
--rw-r--r--   0        0        0      731 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/cli/adaptor/ojman.py
--rw-r--r--   0        0        0      187 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/core/DI.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/core/__init__.py
--rw-r--r--   0        0        0      649 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/core/problem.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/custom/__init__.py
--rw-r--r--   0        0        0    11877 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/custom/Codeforces/Codeforces.py
--rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/custom/Codeforces/__init__.py
--rw-r--r--   0        0        0     2436 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/custom/Codeforces/contestList.py
--rw-r--r--   0        0        0     1583 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/custom/Codeforces/standing.py
--rw-r--r--   0        0        0      897 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/Account.py
--rw-r--r--   0        0        0     1050 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/Analyze.py
--rw-r--r--   0        0        0     1575 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/BaseOj.py
--rw-r--r--   0        0        0      645 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/Contest.py
--rw-r--r--   0        0        0      582 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/FolderState.py
--rw-r--r--   0        0        0       75 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/LangKV.py
--rw-r--r--   0        0        0      532 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/ParseProblemResult.py
--rw-r--r--   0        0        0     1008 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/Problem.py
--rw-r--r--   0        0        0      653 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/ProblemMeta.py
--rw-r--r--   0        0        0     1202 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/Result.py
--rw-r--r--   0        0        0     1151 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/Template.py
--rw-r--r--   0        0        0      104 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/TestCase.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/model/__init__.py
--rw-r--r--   0        0        0      655 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/FileUtil.py
--rw-r--r--   0        0        0     1506 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/HtmlTag.py
--rw-r--r--   0        0        0     1590 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/HttpUtil.py
--rw-r--r--   0        0        0     1192 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/HttpUtilCookiesHelper.py
--rw-r--r--   0        0        0     1260 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/Logger.py
--rw-r--r--   0        0        0      647 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/OJUtil.py
--rw-r--r--   0        0        0     2329 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/Provider2.py
--rw-r--r--   0        0        0      195 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/Singleton.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/__init__.py
--rw-r--r--   0        0        0     3824 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/account.py
--rw-r--r--   0        0        0     2964 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/analyze.py
--rw-r--r--   0        0        0     1036 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/async2sync.py
--rw-r--r--   0        0        0     1066 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/configFolder.py
--rw-r--r--   0        0        0     1204 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/db.py
--rw-r--r--   0        0        0      865 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/diffTool.py
--rw-r--r--   0        0        0      733 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/enc.py
--rw-r--r--   0        0        0      199 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/force_symlink.py
--rw-r--r--   0        0        0       86 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/start_terminal.py
--rw-r--r--   0        0        0     6419 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/template.py
--rw-r--r--   0        0        0      342 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/utc2local.py
--rw-r--r--   0        0        0      907 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/wsTool.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/consts/__init__.py
--rw-r--r--   0        0        0      124 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/consts/ids.py
--rw-r--r--   0        0        0       45 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/oi_cli2/utils/consts/platforms.py
--rw-r--r--   0        0        0     1253 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/.gitignore
--rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/LICENSE
--rw-r--r--   0        0        0       95 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/README.md
--rw-r--r--   0        0        0     1294 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/pyproject.toml
--rw-r--r--   0        0        0     2247 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.1/PKG-INFO
+-rw-r--r--   0        0        0       24 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/__init__.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/py.typed
+-rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/abstract/HtmlTagAbstract.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/abstract/__init__.py
+-rw-r--r--   0        0        0        1 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/__init__.py
+-rw-r--r--   0        0        0     4246 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/account.py
+-rw-r--r--   0        0        0     2762 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/analyze.py
+-rwxr-xr-x   0        0        0     1479 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/completion.py
+-rw-r--r--   0        0        0      842 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/config.py
+-rw-r--r--   0        0        0      715 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/constant.py
+-rw-r--r--   0        0        0    10692 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/contest.py
+-rw-r--r--   0        0        0      547 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/init.py
+-rwxr-xr-x   0        0        0     1280 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/lang.py
+-rwxr-xr-x   0        0        0     1102 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/main.py
+-rw-r--r--   0        0        0     4355 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/problem.py
+-rw-r--r--   0        0        0      513 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/reg_list.py
+-rwxr-xr-x   0        0        0     4684 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/submit.py
+-rw-r--r--   0        0        0     3468 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/template.py
+-rwxr-xr-x   0        0        0     3450 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/test.py
+-rw-r--r--   0        0        0     7399 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/adaptor/AtCoderAdaptor.py
+-rw-r--r--   0        0        0      851 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/adaptor/CodeforcesAdaptor.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/adaptor/__init__.py
+-rw-r--r--   0        0        0      731 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/cli/adaptor/ojman.py
+-rw-r--r--   0        0        0      187 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/core/DI.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/core/__init__.py
+-rw-r--r--   0        0        0      649 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/core/problem.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/custom/__init__.py
+-rw-r--r--   0        0        0    12402 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/custom/Codeforces/Codeforces.py
+-rw-r--r--   0        0        0       28 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/custom/Codeforces/__init__.py
+-rw-r--r--   0        0        0     2436 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/custom/Codeforces/contestList.py
+-rw-r--r--   0        0        0     1583 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/custom/Codeforces/standing.py
+-rw-r--r--   0        0        0      897 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/Account.py
+-rw-r--r--   0        0        0     1050 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/Analyze.py
+-rw-r--r--   0        0        0     1575 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/BaseOj.py
+-rw-r--r--   0        0        0      645 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/Contest.py
+-rw-r--r--   0        0        0      582 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/FolderState.py
+-rw-r--r--   0        0        0       75 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/LangKV.py
+-rw-r--r--   0        0        0      532 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/ParseProblemResult.py
+-rw-r--r--   0        0        0     1008 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/Problem.py
+-rw-r--r--   0        0        0      653 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/ProblemMeta.py
+-rw-r--r--   0        0        0     1202 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/Result.py
+-rw-r--r--   0        0        0     1151 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/Template.py
+-rw-r--r--   0        0        0      104 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/TestCase.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/model/__init__.py
+-rw-r--r--   0        0        0      655 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/FileUtil.py
+-rw-r--r--   0        0        0     1506 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/HtmlTag.py
+-rw-r--r--   0        0        0     1590 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/HttpUtil.py
+-rw-r--r--   0        0        0     1192 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/HttpUtilCookiesHelper.py
+-rw-r--r--   0        0        0     1260 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/Logger.py
+-rw-r--r--   0        0        0      647 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/OJUtil.py
+-rw-r--r--   0        0        0     2329 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/Provider2.py
+-rw-r--r--   0        0        0      195 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/Singleton.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/__init__.py
+-rw-r--r--   0        0        0     3824 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/account.py
+-rw-r--r--   0        0        0     2964 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/analyze.py
+-rw-r--r--   0        0        0     1036 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/async2sync.py
+-rw-r--r--   0        0        0     1066 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/configFolder.py
+-rw-r--r--   0        0        0     1204 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/db.py
+-rw-r--r--   0        0        0      865 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/diffTool.py
+-rw-r--r--   0        0        0      733 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/enc.py
+-rw-r--r--   0        0        0      199 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/force_symlink.py
+-rw-r--r--   0        0        0       86 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/start_terminal.py
+-rw-r--r--   0        0        0     6419 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/template.py
+-rw-r--r--   0        0        0      342 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/utc2local.py
+-rw-r--r--   0        0        0      907 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/wsTool.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/consts/__init__.py
+-rw-r--r--   0        0        0      124 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/consts/ids.py
+-rw-r--r--   0        0        0       45 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/oi_cli2/utils/consts/platforms.py
+-rw-r--r--   0        0        0     1253 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/.gitignore
+-rw-r--r--   0        0        0     1070 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/LICENSE
+-rw-r--r--   0        0        0       95 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/README.md
+-rw-r--r--   0        0        0     1294 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/pyproject.toml
+-rw-r--r--   0        0        0     2247 2020-02-02 00:00:00.000000 yxr_oi_cli-0.2.2.2/PKG-INFO
```

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/abstract/HtmlTagAbstract.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/abstract/HtmlTagAbstract.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/account.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/account.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/analyze.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/analyze.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/completion.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/completion.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/config.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/config.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/constant.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/constant.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/contest.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/contest.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/init.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/init.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/lang.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/lang.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/main.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/main.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/problem.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/problem.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/reg_list.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/reg_list.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/submit.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/submit.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/template.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/template.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/test.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/test.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/adaptor/AtCoderAdaptor.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/adaptor/AtCoderAdaptor.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/adaptor/CodeforcesAdaptor.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/adaptor/CodeforcesAdaptor.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/cli/adaptor/ojman.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/cli/adaptor/ojman.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/core/problem.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/core/problem.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/custom/Codeforces/Codeforces.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/custom/Codeforces/Codeforces.py`

 * *Files 4% similar despite different names*

```diff
@@ -158,41 +158,50 @@
     # return (end watch?, transform result)
     def custom_handler(result: Any) -> Tuple[bool, SubmissionWSResult]:
       parsed_data = transform_submission(result)
       if parsed_data.msg != 'TESTING':
         return True, parsed_data
       return False, parsed_data
 
-    # TODO move more parse inside
+    # TODO move more parse inside codeforces-core ? cf是出错中断形式,状态+数量
     def page_result_transform(res: SubmissionPageResult) -> SubmissionResult:
       # logging.warn('verdict:' + res.verdict)
       cur_status = SubmissionResult.Status.PENDING
       if res.verdict.startswith('Running'):
         cur_status = SubmissionResult.Status.RUNNING
+      elif res.verdict.startswith('In queue'):
+        cur_status = SubmissionResult.Status.RUNNING
       elif res.verdict.startswith('Accepted'):
         cur_status = SubmissionResult.Status.AC
+      elif res.verdict.startswith('Pretests passed'):
+        cur_status = SubmissionResult.Status.AC
       elif res.verdict.startswith('Wrong answer'):
         cur_status = SubmissionResult.Status.WA
+      elif res.verdict.startswith('Runtime error'): # Runtime error on pretest 2
+        cur_status = SubmissionResult.Status.RE
       else:
         logging.error('NOT HANDLE PAGE:', res.verdict)
 
       return SubmissionResult(id=res.id,
                               cur_status=cur_status,
                               time_note=res.time_ms,
                               mem_note=res.mem_bytes,
                               url=res.url,
                               msg_txt=res.verdict)
 
+    # TODO move more parse inside codeforces-core ?
     def ws_result_transform(res: SubmissionWSResult) -> SubmissionResult:
       # logging.warn('res.msg:' + res.msg)
       cur_status = SubmissionResult.Status.PENDING
       if res.msg == 'TESTING':
         cur_status = SubmissionResult.Status.RUNNING
       elif res.msg == 'OK':
         cur_status = SubmissionResult.Status.AC
+      elif res.msg == 'WRONG_ANSWER':
+        cur_status = SubmissionResult.Status.WA
       else:
         logging.error('NOT HANDLE WS:' + str(res.msg))
 
       msg_txt = str(res.testcases)
       if cur_status == SubmissionResult.Status.AC:
         msg_txt = f'{res.passed}/{res.testcases}'
```

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/custom/Codeforces/contestList.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/custom/Codeforces/contestList.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/custom/Codeforces/standing.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/custom/Codeforces/standing.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/Account.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/Account.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/Analyze.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/Analyze.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/BaseOj.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/BaseOj.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/Contest.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/Contest.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/FolderState.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/FolderState.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/ParseProblemResult.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/ParseProblemResult.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/Problem.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/Problem.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/ProblemMeta.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/ProblemMeta.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/Result.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/Result.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/model/Template.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/model/Template.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/FileUtil.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/FileUtil.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/HtmlTag.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/HtmlTag.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/HttpUtil.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/HttpUtil.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/HttpUtilCookiesHelper.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/HttpUtilCookiesHelper.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/Logger.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/Logger.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/OJUtil.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/OJUtil.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/Provider2.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/Provider2.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/account.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/account.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/analyze.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/analyze.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/async2sync.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/async2sync.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/configFolder.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/configFolder.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/db.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/db.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/diffTool.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/diffTool.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/enc.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/enc.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/template.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/template.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/oi_cli2/utils/wsTool.py` & `yxr_oi_cli-0.2.2.2/oi_cli2/utils/wsTool.py`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/.gitignore` & `yxr_oi_cli-0.2.2.2/.gitignore`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/LICENSE` & `yxr_oi_cli-0.2.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/pyproject.toml` & `yxr_oi_cli-0.2.2.2/pyproject.toml`

 * *Files identical despite different names*

### Comparing `yxr_oi_cli-0.2.2.1/PKG-INFO` & `yxr_oi_cli-0.2.2.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yxr-oi-cli
-Version: 0.2.2.1
+Version: 0.2.2.2
 Summary: Simple Online Judge Cli Tool
 Project-URL: Homepage, https://github.com/CroMarmot/oiTerminal
 Project-URL: Bug Tracker, https://github.com/CroMarmot/oiTerminal/issues
 Author-email: YeXiaoRain <yexiaorain@gmail.com>
 License: MIT License
         
         Copyright (c) 2022 陈鼫RWHTYFZ
```

