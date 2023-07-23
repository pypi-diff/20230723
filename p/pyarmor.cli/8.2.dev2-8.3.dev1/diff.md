# Comparing `tmp/pyarmor.cli-8.2.dev2-py2.py3-none-any.whl.zip` & `tmp/pyarmor.cli-8.3.dev1.zip`

## zipinfo {}

```diff
@@ -1,20 +1,33 @@
-Zip file size: 36617 bytes, number of entries: 18
--rw-r--r--  2.0 unx     1479 b- defN 23-Apr-29 14:32 pyarmor/cli/__init__.py
--rw-r--r--  2.0 unx    22526 b- defN 23-Apr-29 21:18 pyarmor/cli/__main__.py
--rw-r--r--  2.0 unx    10694 b- defN 23-Apr-20 07:01 pyarmor/cli/config.py
--rw-r--r--  2.0 unx    17473 b- defN 23-Apr-30 10:02 pyarmor/cli/context.py
--rw-r--r--  2.0 unx     8186 b- defN 23-May-01 02:05 pyarmor/cli/default.cfg
--rw-r--r--  2.0 unx     5532 b- defN 23-Apr-30 08:53 pyarmor/cli/generate.py
--rw-r--r--  2.0 unx     3956 b- defN 23-Apr-20 07:02 pyarmor/cli/mixer.py
--rw-r--r--  2.0 unx     2847 b- defN 23-Apr-22 14:15 pyarmor/cli/plugin.py
--rw-r--r--  2.0 unx     2487 b- defN 23-Mar-25 22:51 pyarmor/cli/public_capsule.zip
--rw-r--r--  2.0 unx    17413 b- defN 23-Apr-29 05:01 pyarmor/cli/register.py
--rw-r--r--  2.0 unx    11386 b- defN 23-Apr-20 07:01 pyarmor/cli/repack.py
--rw-r--r--  2.0 unx     6398 b- defN 23-Apr-13 06:46 pyarmor/cli/resource.py
--rw-r--r--  2.0 unx     2193 b- defN 23-Feb-22 14:43 pyarmor/cli/shell.py
--rw-r--r--  2.0 unx     2407 b- defN 23-May-01 02:25 pyarmor.cli-8.2.dev2.dist-info/METADATA
--rw-r--r--  2.0 unx      110 b- defN 23-May-01 02:25 pyarmor.cli-8.2.dev2.dist-info/WHEEL
--rw-r--r--  2.0 unx       41 b- defN 23-May-01 02:25 pyarmor.cli-8.2.dev2.dist-info/entry_points.txt
--rw-r--r--  2.0 unx        8 b- defN 23-May-01 02:25 pyarmor.cli-8.2.dev2.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1467 b- defN 23-May-01 02:25 pyarmor.cli-8.2.dev2.dist-info/RECORD
-18 files, 116603 bytes uncompressed, 34235 bytes compressed:  70.6%
+Zip file size: 52148 bytes, number of entries: 31
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor/
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/
+-rw-r--r--  2.0 unx     2852 b- defN 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/PKG-INFO
+-rw-r--r--  2.0 unx     1829 b- defN 23-Jul-19 09:23 pyarmor.cli-8.3.dev1/setup.py
+-rw-r--r--  2.0 unx       38 b- defN 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/setup.cfg
+-rw-r--r--  2.0 unx     1598 b- defN 23-Mar-04 17:07 pyarmor.cli-8.3.dev1/README.rst
+drwxr-xr-x  2.0 unx        0 b- stor 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor/cli/
+-rw-r--r--  2.0 unx     7036 b- defN 23-Jun-21 23:40 pyarmor.cli-8.3.dev1/pyarmor/cli/bootstrap.py
+-rw-r--r--  2.0 unx     7184 b- defN 23-May-31 08:47 pyarmor.cli-8.3.dev1/pyarmor/cli/merge.py
+-rw-r--r--  2.0 unx    10726 b- defN 23-May-31 08:18 pyarmor.cli-8.3.dev1/pyarmor/cli/config.py
+-rw-r--r--  2.0 unx    18993 b- defN 23-Jul-23 15:37 pyarmor.cli-8.3.dev1/pyarmor/cli/register.py
+-rw-r--r--  2.0 unx     5835 b- defN 23-May-22 18:36 pyarmor.cli-8.3.dev1/pyarmor/cli/generate.py
+-rw-r--r--  2.0 unx     2193 b- defN 23-Feb-22 22:43 pyarmor.cli-8.3.dev1/pyarmor/cli/shell.py
+-rw-r--r--  2.0 unx     7158 b- defN 23-May-07 11:39 pyarmor.cli-8.3.dev1/pyarmor/cli/resource.py
+-rw-r--r--  2.0 unx     1526 b- defN 23-Jul-19 09:21 pyarmor.cli-8.3.dev1/pyarmor/cli/__init__.py
+-rw-r--r--  2.0 unx     4594 b- defN 23-Jun-30 13:25 pyarmor.cli-8.3.dev1/pyarmor/cli/docker.py
+-rw-r--r--  2.0 unx    19470 b- defN 23-Jul-20 10:16 pyarmor.cli-8.3.dev1/pyarmor/cli/context.py
+-rw-r--r--  2.0 unx     3137 b- defN 23-Jun-25 16:00 pyarmor.cli-8.3.dev1/pyarmor/cli/group.py
+-rw-r--r--  2.0 unx     7718 b- defN 23-Jun-09 14:11 pyarmor.cli-8.3.dev1/pyarmor/cli/plugin.py
+-rw-r--r--  2.0 unx     3956 b- defN 23-Apr-20 15:02 pyarmor.cli-8.3.dev1/pyarmor/cli/mixer.py
+-rw-r--r--  2.0 unx     2487 b- defN 23-Mar-26 06:51 pyarmor.cli-8.3.dev1/pyarmor/cli/public_capsule.zip
+-rw-r--r--  2.0 unx     9133 b- defN 23-Jul-20 10:08 pyarmor.cli-8.3.dev1/pyarmor/cli/default.cfg
+-rw-r--r--  2.0 unx    23065 b- defN 23-Jun-30 23:02 pyarmor.cli-8.3.dev1/pyarmor/cli/__main__.py
+-rw-r--r--  2.0 unx    16099 b- defN 23-Jun-21 23:40 pyarmor.cli-8.3.dev1/pyarmor/cli/repack.py
+-rw-r--r--  2.0 unx     2852 b- defN 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/PKG-INFO
+-rw-r--r--  2.0 unx      626 b- defN 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/SOURCES.txt
+-rw-r--r--  2.0 unx       55 b- defN 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/entry_points.txt
+-rw-r--r--  2.0 unx       27 b- defN 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/requires.txt
+-rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/top_level.txt
+-rw-r--r--  2.0 unx        1 b- defN 23-Jul-23 20:58 pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/dependency_links.txt
+31 files, 160196 bytes uncompressed, 47148 bytes compressed:  70.6%
```

## zipnote {}

```diff
@@ -1,55 +1,94 @@
-Filename: pyarmor/cli/__init__.py
+Filename: pyarmor.cli-8.3.dev1/
 Comment: 
 
-Filename: pyarmor/cli/__main__.py
+Filename: pyarmor.cli-8.3.dev1/pyarmor/
 Comment: 
 
-Filename: pyarmor/cli/config.py
+Filename: pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/
 Comment: 
 
-Filename: pyarmor/cli/context.py
+Filename: pyarmor.cli-8.3.dev1/PKG-INFO
 Comment: 
 
-Filename: pyarmor/cli/default.cfg
+Filename: pyarmor.cli-8.3.dev1/setup.py
 Comment: 
 
-Filename: pyarmor/cli/generate.py
+Filename: pyarmor.cli-8.3.dev1/setup.cfg
 Comment: 
 
-Filename: pyarmor/cli/mixer.py
+Filename: pyarmor.cli-8.3.dev1/README.rst
 Comment: 
 
-Filename: pyarmor/cli/plugin.py
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/
 Comment: 
 
-Filename: pyarmor/cli/public_capsule.zip
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/bootstrap.py
 Comment: 
 
-Filename: pyarmor/cli/register.py
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/merge.py
 Comment: 
 
-Filename: pyarmor/cli/repack.py
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/config.py
 Comment: 
 
-Filename: pyarmor/cli/resource.py
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/register.py
 Comment: 
 
-Filename: pyarmor/cli/shell.py
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/generate.py
 Comment: 
 
-Filename: pyarmor.cli-8.2.dev2.dist-info/METADATA
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/shell.py
 Comment: 
 
-Filename: pyarmor.cli-8.2.dev2.dist-info/WHEEL
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/resource.py
 Comment: 
 
-Filename: pyarmor.cli-8.2.dev2.dist-info/entry_points.txt
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/__init__.py
 Comment: 
 
-Filename: pyarmor.cli-8.2.dev2.dist-info/top_level.txt
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/docker.py
 Comment: 
 
-Filename: pyarmor.cli-8.2.dev2.dist-info/RECORD
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/context.py
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/group.py
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/plugin.py
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/mixer.py
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/public_capsule.zip
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/default.cfg
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/__main__.py
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor/cli/repack.py
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/PKG-INFO
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/SOURCES.txt
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/entry_points.txt
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/requires.txt
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/top_level.txt
+Comment: 
+
+Filename: pyarmor.cli-8.3.dev1/pyarmor.cli.egg-info/dependency_links.txt
 Comment: 
 
 Zip file comment:
```

## filetype from file(1)

```diff
@@ -1 +1 @@
-Zip archive data, at least v2.0 to extract, compression method=deflate
+Zip archive data, at least v2.0 to extract, compression method=store
```

## Comparing `pyarmor/cli/__init__.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import logging
 
-__VERSION__ = '8.2'
+__VERSION__ = '8.3.dev1'
 
 logger = logging.getLogger('cli')
 
 
 class CliError(Exception):
     pass
 
@@ -20,14 +20,15 @@
 
 class Component(object):
 
     trace_loggers = {
         'StrProtector': 'trace.mix.str',
         'CallProtector': 'trace.assert.call',
         'ImportProtector': 'trace.assert.import',
+        'AttrProtector': 'trace.co.attr',
         'CodeProtector': 'trace.co',
         'CoPatcher': 'trace.co',
         'BccPatcher': 'trace.bcc',
     }
 
     def __init__(self, ctx):
         self.ctx = ctx
```

## Comparing `pyarmor/cli/__main__.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/__main__.py`

 * *Files 2% similar despite different names*

```diff
@@ -26,14 +26,16 @@
 
 from . import logger, CliError
 from .context import Context
 from .register import Register, WebRegister
 from .config import Configer
 from .shell import PyarmorShell
 from .plugin import Plugin
+from .generate import Builder
+from .bootstrap import check_prebuilt_runtime_library
 
 
 def _cmd_gen_key(builder, options):
     n = len(options['inputs'])
     if n > 1:
         logger.error('please check online documentation to learn')
         logger.error('how to use command "pyarmor gen key"')
@@ -59,15 +61,15 @@
         logger.error('please check online documentation to learn')
         logger.error('how to use command "pyarmor gen runtime"')
         raise CliError('invalid arguments: %s' % options['inputs'][1:])
 
     output = options.get('output', 'dist')
 
     logger.info('start to generate runtime package')
-    builder.generate_runtime(output)
+    builder.generate_runtime_package(output)
 
     keyname = os.path.join(output, builder.ctx.runtime_keyfile)
     logger.info('write "%s"', keyname)
     with open(keyname, 'wb') as f:
         f.write(builder.ctx.runtime_key)
     logger.info('generate runtime package to "%s" OK', output)
 
@@ -105,16 +107,14 @@
         if options.get('restrict_module', 0) < 2:
             logger.debug('implicitly set restrict_module = 2')
             options['restrict_module'] = 2
 
     if args.enables:
         for x in args.enables:
             options['enable_' + x] = True
-    if options.get('enable_themida'):
-        raise NotImplementedError('--enable_themida is still not implemented')
 
     if args.prefix:
         options['import_prefix'] = args.prefix
 
     if args.no_wrap:
         options['wrap_mode'] = 0
 
@@ -122,14 +122,19 @@
         options['includes'] = ' '.join(args.includes)
     if args.excludes:
         options['excludes'] = ' '.join(args.excludes)
 
     if args.bind_data:
         options['user_data'] = args.bind_data
 
+    if args.pack:
+        dist_path = os.path.join(ctx.repack_path, 'dist')
+        logger.info('implicitly set output to "%s"', dist_path)
+        options['output'] = dist_path
+
     return options
 
 
 def check_cross_platform(ctx, platforms):
     rtver = ctx.cfg.get('pyarmor', 'cli.runtime')
     cmd = 'pip install pyarmor.cli.runtime~=%s.0' % rtver
     try:
@@ -153,29 +158,34 @@
 
     if unknown:
         logger.error('please check documentation "References/Environments"')
         raise CliError('unsupported platforms "%s"' % ', '.join(unknown))
 
 
 def check_gen_context(ctx, args):
-    enable_bcc = args.enable_bcc or (args.enables and 'bcc' in args.enables)
-    if ctx.runtime_platforms:
-        if ctx.enable_themida and not ctx.pyarmor_platform.startswith('win'):
-            raise CliError('--enable_themida only works for Windows')
-        if enable_bcc:
+    platforms = ctx.runtime_platforms
+    if platforms and set(platforms) != set([ctx.pyarmor_platform]):
+        if ctx.enable_bcc:
             raise CliError('bcc mode does not support cross platform')
-        check_cross_platform(ctx, ctx.runtime_platforms)
+        rtver = ctx.cfg['pyarmor'].get('cli.runtime', '')
+        check_prebuilt_runtime_library(platforms, ctx.enable_themida, rtver)
 
-    if enable_bcc:
+    elif ctx.enable_themida:
+        if not ctx.pyarmor_platform.startswith('windows'):
+            raise CliError('--enable-themida only works for Windows')
+        rtver = ctx.cfg['pyarmor'].get('cli.runtime', '')
+        check_prebuilt_runtime_library([], ['themida'], rtver)
+
+    if ctx.enable_bcc:
         plat, arch = ctx.pyarmor_platform.split('.')
         if arch not in ('x86_64', 'aarch64', 'x86', 'armv7'):
             raise CliError('bcc mode still not support arch "%s"' % arch)
 
-    if ctx.cmd_options['no_runtime'] and not ctx.runtime_outer:
-        raise CliError('--no_runtime must be used with --outer')
+    if ctx.cmd_options.get('no_runtime') and not ctx.runtime_outer:
+        raise CliError('--outer is required if using --no_runtime')
 
     if ctx.use_runtime and not ctx.runtime_outer:
         if os.path.exists(ctx.use_runtime):
             keyname = os.path.join(ctx.use_runtime, ctx.runtime_keyfile)
             if not os.path.exists(keyname):
                 raise CliError('no runtime key in "%s"', ctx.use_runtime)
 
@@ -189,31 +199,35 @@
         if args.no_runtime:
             raise CliError('--pack conficts with --no-runtime, --use-runtime')
         if ctx.import_prefix:
             raise CliError('--pack conficts with -i, --prefix')
 
 
 def cmd_gen(ctx, args):
-    from .generate import Builder
-
     options = format_gen_args(ctx, args)
     logger.debug('command options: %s', options)
     ctx.push(options)
     check_gen_context(ctx, args)
 
     builder = Builder(ctx)
 
     Plugin.install(ctx)
     if args.inputs[0].lower() in ('key', 'k'):
         _cmd_gen_key(builder, options)
     elif args.inputs[0].lower() in ('runtime', 'run', 'r'):
         _cmd_gen_runtime(builder, options)
-    else:
-        builder.process(options, pack=args.pack)
+    elif args.pack:
+        from .repack import Repacker
+        codesign = ctx.cfg['pack'].get('codesign_identify', None)
+        packer = Repacker(args.pack, ctx.repack_path, codesign=codesign)
+        builder.process(options, packer=packer)
         Plugin.post_build(ctx, pack=args.pack)
+    else:
+        builder.process(options)
+        Plugin.post_build(ctx)
 
 
 def cmd_cfg(ctx, args):
     scope = 'global' if args.scope else 'local'
     cfg = Configer(ctx, encoding=args.encoding)
     name = 'reset' if args.reset else 'run'
     getattr(cfg, name)(args.options, scope == 'local', args.name)
@@ -259,14 +273,15 @@
                "", "")
         prompt = 'I have known the changes of Pyarmor 8? (yes/no/help) '
         choice = input('\n'.join(msg) + prompt).lower()[:1]
         if choice == 'h':
             import webbrowser
             webbrowser.open(url)
         if not choice == 'y':
+            logger.info('abort upgrade')
             return
 
     if args.device:
         if not regfile.endswith('.zip'):
             logger.error('invalid registeration file "%s"', regfile)
             raise CliError('please use ".zip" file to register group device')
         regsvr = WebRegister(ctx)
@@ -279,15 +294,18 @@
         reg.register_regfile(regfile)
         logger.info('This license registration information:\n\n%s', str(reg))
 
     else:
         regsvr = WebRegister(ctx)
         info, msg = regsvr.prepare(regfile, args.product, upgrade=upgrade)
         prompt = 'Are you sure to continue? (yes/no) '
-        if input(msg + prompt) not in ('y', 'yes'):
+        if args.confirm:
+            from time import sleep
+            sleep(1.0)
+        elif input(msg + prompt) not in ('y', 'yes'):
             logger.info('abort registration')
             return
         # Free upgrade to Pyarmor Basic
         if upgrade and not info['upgrade']:
             return regsvr.register(regfile, args.product, upgrade=True)
 
         if upgrade:
@@ -296,14 +314,15 @@
             group = info['lictype'] == 'GROUP'
             regsvr.register(regfile, args.product, group=group)
 
 
 def main_parser():
     parser = argparse.ArgumentParser(
         prog='pyarmor',
+        fromfile_prefix_chars='@',
         formatter_class=argparse.RawDescriptionHelpFormatter,
     )
     parser.add_argument(
         '-v', '--version', action='store_true',
         help='show version information and exit'
     )
     parser.add_argument(
@@ -382,23 +401,23 @@
     )
     group.add_argument(
         '--include', dest='includes', metavar='PATTERN', action='append',
         help=argparse.SUPPRESS
     )
     group.add_argument(
         '--exclude', dest='excludes', metavar='PATTERN', action='append',
-        help=argparse.SUPPRESS
+        help='Exclude scripts and paths'
     )
 
     group.add_argument(
         '--obf-module', type=int, default=None, choices=(0, 1),
         help='obfuscate whole module (default is 1)'
     )
     group.add_argument(
-        '--obf-code', type=int, default=None, choices=(0, 1),
+        '--obf-code', type=int, default=None, choices=(0, 1, 2),
         help='obfuscate each function (default is 1)'
     )
     group.add_argument(
         '--no-wrap', action='store_true', default=None,
         help='disable wrap mode',
     )
 
@@ -467,37 +486,28 @@
         help='enable outer runtime key'
     )
     group.add_argument(
         '-e', '--expired', metavar='DATE',
         help='set expired date'
     )
     group.add_argument(
-        '--period', type=int, metavar='N', dest='period',
+        '--period', metavar='N', dest='period',
         help='check runtime key periodically'
     )
     group.add_argument(
         '-b', '--bind-device', dest='devices', metavar='DEV', action='append',
         help='bind obfuscated scripts to device'
     )
     group.add_argument(
         '--bind-data', metavar='FILE',
         help=argparse.SUPPRESS
     )
-    group.add_argument(
-        '--bind-interp', metavar='INTERP',
-        help=argparse.SUPPRESS
-    )
-    group.add_argument(
-        '--hook', metavar='HOOK',
-        help=argparse.SUPPRESS
-    )
 
     cparser.add_argument(
-        'inputs', metavar='ARG', nargs='+',
-        help='script, package or keyword "key", "runtime"'
+        'inputs', metavar='ARG', nargs='+', help='scripts or packages'
     )
 
     cparser.set_defaults(func=cmd_gen)
 
 
 def cfg_parser(subparsers):
     '''show all options:
@@ -559,15 +569,15 @@
 https://pyarmor.readthedocs.io/en/stable/reference/man.html#pyarmor-reg
     '''
     cparser = subparsers.add_parser(
         'reg',
         aliases=['register', 'r'],
         formatter_class=argparse.RawDescriptionHelpFormatter,
         description=reg_parser.__doc__,
-        help='register Pyarmor or upgrade Pyarmor license'
+        help='register Pyarmor or upgrade old Pyarmor license'
     )
 
     cparser.add_argument(
         '-r', '--regname', metavar='NAME',
         help=argparse.SUPPRESS
     )
     cparser.add_argument(
```

## Comparing `pyarmor/cli/config.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/config.py`

 * *Files 2% similar despite different names*

```diff
@@ -147,15 +147,17 @@
             optvalue = optvalue.strip(optvalue[0])
 
         if not optvalue:
             if op is None:
                 self._clear(sect, optname, local, name)
             return
 
-        old = cfg[sect].get(optname, '') if cfg.has_section(sect) else ''
+        ctxcfg = ctx.cfg
+        old = ctxcfg[sect].get(optname, '') if ctxcfg.has_section(sect) else ''
+
         if op == '+':
             if (optvalue + ' ').find(old + ' ') == -1:
                 optvalue = ('%s %s' % (old, optvalue)).strip()
         elif op == '-':
             optvalue = (old + ' ').replace(optvalue + ' ', '').strip()
         elif op == '^':
             optvalue = '\n'.join((old.splitlines() + [optvalue]))
```

## Comparing `pyarmor/cli/context.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/context.py`

 * *Files 15% similar despite different names*

```diff
@@ -28,26 +28,71 @@
 __pyarmor__(__name__, $path, $code)
 '''
 
 runtime_package_template = '''# Pyarmor $rev, $timestamp
 from .pyarmor_runtime import __pyarmor__
 '''
 
-runtime_package_template2 = '''# Pyarmor $rev, $timestamp
-for suffix in '', '_a1', '_a2', '_a3':
-    try:
-        __pyarmor__ = __import__('pyarmor_runtime' + suffix,
-                                 globals(), locals(),
-                                 ('__pyarmor__',),
-                                 0).__pyarmor__
-        break
-    except ModuleNotFoundError:
-        pass
-else:
-    raise ModuleNotFoundError('no pyarmor_runtime extension found')
+multi_runtime_package_template = '''# Pyarmor $rev, $timestamp
+def __pyarmor__():
+    import platform
+    import sys
+    from struct import calcsize
+
+    def format_system():
+        plat = platform.system().lower()
+        plat = ('windows' if plat.startswith('cygwin') else
+                'linux' if plat.startswith('linux') else
+                'freebsd' if plat.startswith(
+                    ('freebsd', 'openbsd', 'isilon onefs')) else plat)
+        if plat == 'linux':
+            if hasattr(sys, 'getandroidapilevel'):
+                plat = 'android'
+            else:
+                cname, cver = platform.libc_ver()
+                if cname == 'musl':
+                    plat = 'alpine'
+                elif cname == 'libc':
+                    plat = 'android'
+        return plat
+
+    def format_machine():
+        mach = platform.machine().lower()
+        arch_table = (
+            ('x86', ('i386', 'i486', 'i586', 'i686')),
+            ('x86_64', ('x64', 'x86_64', 'amd64', 'intel')),
+            ('arm', ('armv5',)),
+            ('armv6', ('armv6l',)),
+            ('armv7', ('armv7l',)),
+            ('aarch32', ('aarch32',)),
+            ('aarch64', ('aarch64', 'arm64'))
+        )
+        for alias, archlist in arch_table:
+            if mach in archlist:
+                mach = alias
+                break
+        return mach
+
+    plat, mach = format_system(), format_machine()
+    if plat == 'windows' and mach == 'x86_64':
+        bitness = calcsize('P'.encode()) * 8
+        if bitness == 32:
+            mach = 'x86'
+
+    name = '.'.join(['_'.join([plat, mach]), 'pyarmor_runtime'])
+    return __import__(name, globals(), locals(), ['__pyarmor__'], level=1)
+__pyarmor__ = __pyarmor__().__pyarmor__
+'''
+
+runtime_package_template3 = '''# Pyarmor $rev, $timestamp
+from importlib.machinery import ExtensionFileLoader
+from sysconfig import get_platform
+__pyarmor__ = ExtensionFileLoader(
+    '.pyarmor_runtime', __file__.replace('__init__.py', 'pyarmor_runtime.so')
+).load_module().__pyarmor__
 '''
 
 
 def format_platform(plat, arch):
     from struct import calcsize
     from fnmatch import fnmatchcase
 
@@ -96,25 +141,20 @@
             os.path.join(self.home_path, rpath)
 
         # self.encoding is just for reading config file
         self.encoding = encoding
         cfglist = self.default_config, self.global_config, self.local_config
         self.cfg = self._read_config(cfglist, encoding=encoding)
 
-        self.inline_plugin_marker = '# pyarmor: '
         # self.runtime_package = 'pyarmor_runtime'
         # self.runtime_suffix = '_000000'
         # default inner key filename within runtime package
         self.runtime_keyfile = '.pyarmor.ikey'
 
         self.bootstrap_template = bootstrap_template
-        self.runtime_package_templates = (
-            runtime_package_template,
-            runtime_package_template2,
-        )
 
         # Alias format for duplicated input names
         self.alias_suffix = '{0}-{1}'
 
         self.input_paths = []
         self.outputs = []
         self.resources = []
@@ -211,15 +251,15 @@
 
     def version_info(self, verbose=3):
         #    8.0.1
         #    8.0.1 (trial)
         #    8.0.1 (basic), 002000
         #    8.0.1 (group), 002002, Product
         #    8.0.1 (group), 002002, Product, Company
-        rev = '.'.join([str(x) for x in self.version])
+        rev = '.'.join(self.version)
         if not verbose:
             return rev
 
         licinfo = self.license_info
         lictype = 'basic' if licinfo['features'] == 1 else \
             'pro' if licinfo['features'] == 7 else \
             'group' if licinfo['features'] == 15 else \
@@ -238,16 +278,15 @@
             if regname:
                 verinfo.append(regname)
 
         return ', '.join(verinfo)
 
     @property
     def version(self):
-        getint = self.cfg.getint
-        return [getint('pyarmor', x) for x in ('major', 'minor', 'patch')]
+        return [self.cfg.get('pyarmor', x) for x in ('major', 'minor', 'patch')]
 
     @property
     def python_version(self):
         return sys.version_info[:2]
 
     @property
     def default_config(self):
@@ -315,14 +354,18 @@
             self.cfg['logging'].get('debug_logfile', 'pyarmor.debug.log'))
 
     @property
     def trace_logfile(self):
         return self._check_logpath(
             self.cfg['logging'].get('trace_logfile', 'pyarmor.trace.log'))
 
+    @property
+    def repack_path(self):
+        return os.path.join(self.local_path, 'pack')
+
     def _optb(self, section, name):
         return self.cfg.getboolean(section, name, vars=self.cmd_options)
 
     def _opts(self, section, name):
         return self.cfg.get(section, name, vars=self.cmd_options)
 
     def _opti(self, section, name):
@@ -434,14 +477,20 @@
         return self.cfg['builder'].get('outer_keyname', 'pyarmor.rkey')
 
     @property
     def use_runtime(self):
         return self.cmd_options.get('use_runtime',
                                     self.cfg['builder'].get('use_runtime'))
 
+    @property
+    def inline_plugin_marker(self):
+        marker = self.cfg['builder'].get('inline_plugin_marker', 'false')
+        if marker.lower() not in ('', 'false', '0'):
+            return '# %s: ' % marker
+
     #
     # runtime configuration
     #
     def _rt_opt(self, opt):
         return self.cmd_options.get(opt, self.cfg['runtime'].get(opt))
 
     @property
@@ -498,15 +547,24 @@
     @property
     def runtime_devices(self):
         value = self._rt_opt('devices')
         return value.splitlines() if isinstance(value, str) else value
 
     @property
     def runtime_interps(self):
-        return self._rt_opt('interps')
+        interps = self._rt_opt('interps')
+        rules = interps.splitlines() if interps else []
+        cfg = self.cfg['builder']
+        if cfg.getboolean('check_debugger', False):
+            rules.append('check-debugger')
+        if cfg.getboolean('check_interp', False):
+            rules.append('check-interp')
+        if self.runtime_hook('pyarmor_runtime'):
+            rules.append('py:bootstrap')
+        return '\n'.join(rules)
 
     @property
     def runtime_timer(self):
         return self._opti('runtime', 'timer')
 
     @property
     def runtime_simple_extension_name(self):
@@ -519,31 +577,29 @@
         if filename:
             if filename[0] == '@':
                 with open(filename[1:], 'rb') as f:
                     data = f.read()
             else:
                 data = filename.encode()
 
-        hook = b''
-        filename = os.path.join(self.local_path, 'hooks', 'pyarmor_runtime.py')
-        if os.path.exists(filename):
-            with open(filename, 'rb') as f:
-                hook = f.read()
-
-        return hook, data
+        return data
 
     @property
     def runtime_messages(self):
         value = self.cfg['runtime'].get('messages', '')
         if value:
             name, encoding = (value + ':utf-8').split(':')[:2]
             cfg = self._named_config(name, encoding=encoding)
             if cfg.has_section('runtime.message'):
                 return cfg
 
+    def runtime_package_template(self, platforms):
+        return runtime_package_template if len(platforms) < 2 else \
+            multi_runtime_package_template
+
     #
     # RFT settings
     #
 
     def rft_output_script(self, name):
         return self._check_logpath(os.path.join(self.local_path, 'rft', name))
```

## Comparing `pyarmor/cli/default.cfg` & `pyarmor.cli-8.3.dev1/pyarmor/cli/default.cfg`

 * *Files 26% similar despite different names*

```diff
@@ -1,17 +1,19 @@
 [pyarmor]
 
 ;; Pyarmor version
 major = 8
-minor = 2
-patch = 0
+minor = 3
+patch = dev1
 
 ;; Core version
-cli.core = 3.2
-cli.runtime = 3.2
+cli.core = 4.3.dev1
+
+;; Deprecated since Pyarmor 8.2.5
+; cli.runtime = 3.2.5
 
 ;; Default timeout when send request to remote server for
 ;;     check Pyarmor license
 ;;     register Pyarmor license
 timeout = 6
 
 regurl = https://api.dashingsoft.com/product/key/enter/%s/?
@@ -21,15 +23,15 @@
 
 debug_logfile = .pyarmor/pyarmor.debug.log
 trace_logfile = .pyarmor/pyarmor.trace.log
 
 [finder]
 recursive = 0
 ;; includes =
-;; excludes =
+excludes = */__pycache__
 pyexts = .py .pyw
 
 ;; Data files need to copy to output path
 ;;   *.txt only copy .txt file
 ;;   * means all data files
 ;;   0 means nothing to copy
 data_files = 0
@@ -56,24 +58,28 @@
 ;; Import prefix to import runtime package
 import_prefix = 0
 
 ;; Sometimes __file__ is not defined, replace it with __name__ to fix this issue
 bootstrap_file = __file__
 
 ;; Exclude co objects by co_name
-exclude_co_names = <lambda> <listcomp> <setcomp> <dictcomp> <generator>
+exclude_co_names = <lambda> <listcomp> <setcomp> <dictcomp> <genexpr>
 
 ;; Common modules which are no restrict
 exclude_restrict_modules = __init__
 
 ;; Outer key name
 outer_keyname = pyarmor.rkey
 
-;; inline_plugin = "# pyarmor: "
-inline_plugin = 1
+;; The final marker is "# %s: " % VALUE
+;; If VALUE == "false", then disable inline plugin
+inline_plugin_marker = pyarmor
+
+;; Default plugins
+plugins = CodesignPlugin
 
 ;; Using shared runtime package
 ; use_runtime = /path/to/runtime
 
 ;; How many loops for jit iv
 jit_iv_threshold = 100
 
@@ -110,15 +116,15 @@
 ;;
 
 ;; The argument optimize specifies the optimization level of the
 ;; compiler; the default value of -1 selects the optimization level of
 ;; the interpreter as given by -O options. Explicit levels are 0 (no
 ;; optimization; __debug__ is true), 1 (asserts are removed, __debug__
 ;; is false) or 2 (docstrings are removed too).
-optimize = 1
+optimize = -1
 
 ;; It's not used now
 type_comments = false
 
 ;; Write refactor result scripts
 trace_rft = 0
 
@@ -225,20 +231,17 @@
 
 ;; Bind runtime key to multiple devices, one line one machine
 ; devices =
 
 ;; Bind runtime key to Python interperter. Each line defines a rule,
 ;; match all the rules. The rule formats
 ;;
-;;      s: symbol symbol DIFF
-;;      S: symbol symbol xxxxxx(md5)
-;;      f: name SIZE
-;;      F: name xxxxxxxx(md5)
-;;      m: name SIZE
-;;      M: name xxxxxxxx(md5)
+;;      D
+;;      S: symbol start end xxxxxx(md5)
+;;
 ; interps =
 
 ;; Insert runtime hooks
 ; hooks = hooks.py
 
 ;; Enable timer
 timer = 0
@@ -269,24 +272,20 @@
 ;; do not mix short string len(s) < this value
 threshold = 8
 
 ; includes =
 ; excludes =
 
 [pack]
+;; For Darwin to code sign binary file
+; codesign_identify =
+
 ;; Strip output path to match archive info
 strip = 0
 
-;; How to handle other .pyc in the bundle
-;;     0  not obfuscate
-;;     1  obf module only
-;;     2  obf module and co_code without lambda and comprehensions
-;;     3  obf module and all co_code
-other_pyc = 0
-
 ;; How to do when the obfuscated module has no matched .pyc in bundle
 ;;    error, issue a error and exit
 ;;    warning, issue a warning and continue
 ;;    ignore, do nothing
 ;;    append, append it to archive
 no_matched_pyc = error
 
@@ -337,7 +336,28 @@
 cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fno-stack-protector -shared -nostdlib -Tlinux.armv7.ldscript
 
 [darwin.x86_64.bcc]
 cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables --target=x86_64-elf-gnu_linux -fPIC -c
 
 [darwin.aarch64.bcc]
 cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables --target=arm64-macho-darwin -fPIC -fno-addrsig -fno-stack-protector -shared -nostdlib -lsystem
+
+[android.x86_64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -c
+
+[android.aarch64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -shared -nostdlib -Tlinux.aarch64.ldscript
+
+[android.x86.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fno-stack-protector -fPIC -c
+
+[android.armv7.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fno-stack-protector -shared -nostdlib -Tlinux.armv7.ldscript
+
+[alpine.x86_64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -c
+
+[alpine.aarch64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -shared -nostdlib -Tlinux.aarch64.ldscript
+
+[freebsd.x86_64.bcc]
+cflags = -O3 -Wno-unsequenced -fno-asynchronous-unwind-tables -fno-unwind-tables -fPIC -fno-stack-protector -c
```

## Comparing `pyarmor/cli/generate.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/generate.py`

 * *Files 8% similar despite different names*

```diff
@@ -28,45 +28,53 @@
 
 
 class Finder(object):
 
     def __init__(self, ctx):
         self.ctx = ctx
 
-    def prepare(self, input_paths):
+    def _build_resource(self, pathlist):
         resources = []
-        for path in input_paths:
+        for path in pathlist:
             if not os.path.exists(path):
                 raise CliError('argument "%s" doesn\'t exists' % path)
             if os.path.isfile(path):
                 logger.info('find script %s', path)
                 res = FileResource(path)
                 resources.append(res)
             else:
                 logger.info('find package at %s', path)
                 res = PathResource(path)
                 resources.append(res)
                 options = self.ctx.get_res_options(res.fullname)
                 res.rebuild(**options)
-        self.ctx.resources = resources
+        return resources
+
+    def prepare(self, input_paths):
+        self.ctx.resources = self._build_resource(input_paths)
+
+    def process_extra(self, contents):
+        extra_paths = [x for x in contents if x.endswith('.pyc')]
+        for pyz in [x for x in contents if x.endswith('.pyz_extracted')]:
+            extra_paths.extend([os.path.join(pyz, x) for x in os.listdir(pyz)])
+        resnames = [x.pkgname for x in self.ctx.resources]
+        for res in self._build_resource(extra_paths):
+            if res.pkgname not in resnames:
+                self.ctx.obfuscated_modules.add(res.pkgname)
+                self.ctx.extra_resources.append(res)
 
-    def process(self, pack=None):
+    def process(self):
         logger.info('search inputs ...')
         self.prepare(self.ctx.input_paths)
         logger.info('find %d top resources', len(self.ctx.resources))
 
         modules = [x.fullname for res in self.ctx.resources for x in res
                    if x.is_script()]
         self.ctx.obfuscated_modules.update(modules)
 
-        # TBD: implement it in next Release
-        # if pack:
-        #     from .repack import list_modules
-        #     self.ctx.obfuscated_modules.update(list_modules(pack))
-
 
 class Builder(object):
 
     def __init__(self, ctx):
         self.ctx = ctx
 
     def format_output(self, outputs, count=0):
@@ -80,29 +88,23 @@
         return Pytransform3.generate_runtime_key(self.ctx, outer)
 
     def generate_runtime_package(self, output):
         if self.ctx.runtime_key is None:
             self.ctx.runtime_key = self.generate_runtime_key()
         Pytransform3.generate_runtime_package(self.ctx, output)
 
-    def _pack_script(self, bundle, output, entry=None, codesign=None):
-        from .repack import repacker
-        buildpath = os.path.join('.pyarmor', 'pack')
-        repacker(bundle, output, buildpath, entry=entry, codesign=codesign)
-        shutil.rmtree(buildpath)
-
     def _obfuscate_scripts(self):
         rev = self.ctx.version_info()
         template = self.ctx.bootstrap_template
         relative = self.ctx.import_prefix
         pkgname = self.ctx.runtime_package_name
         bootpath = self.ctx.cfg.get('builder', 'bootstrap_file')
 
         namelist = []
-        for res in self.ctx.resources:
+        for res in self.ctx.resources + self.ctx.extra_resources:
             logger.info('process resource "%s"', res.fullname)
             name = res.name
             path = self.format_output(self.ctx.outputs, namelist.count(name))
             namelist.append(name)
             os.makedirs(path, exist_ok=True)
 
             for r in res:
@@ -123,36 +125,38 @@
                 fullpath = os.path.join(path, r.output_filename)
                 os.makedirs(os.path.dirname(fullpath), exist_ok=True)
 
                 logger.info('write %s', fullpath)
                 with open(fullpath, 'w') as f:
                     f.write(source)
 
-    def process(self, options, pack=None):
+    def process(self, options, packer=None):
         for opt in options['inputs']:
             if not os.path.exists(opt):
                 raise CliError('no found input "%s"' % opt)
         self.ctx.input_paths = options['inputs']
 
         output = options.get('output', 'dist')
         self.ctx.outputs = output.split(',')
 
         finder = Finder(self.ctx)
-        finder.process(pack=pack)
+        finder.process()
+
+        if packer and options.get('self_contained'):
+            finder.process_extra(packer.contents)
 
         Pytransform3.pre_build(self.ctx)
 
         self.ctx.runtime_key = self.generate_runtime_key()
-
         if not options.get('no_runtime'):
             logger.info('start to generate runtime files')
             self.generate_runtime_package(self.ctx.outputs[0])
             logger.info('generate runtime files OK')
 
         logger.info('start to obfuscate scripts')
         self._obfuscate_scripts()
         logger.info('obfuscate scripts OK')
 
         Pytransform3.post_build(self.ctx)
 
-        if pack:
-            self._pack_script(pack, output)
+        if packer:
+            packer.repack(output, self.ctx.runtime_package_name)
```

## Comparing `pyarmor/cli/mixer.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/mixer.py`

 * *Files identical despite different names*

## Comparing `pyarmor/cli/public_capsule.zip` & `pyarmor.cli-8.3.dev1/pyarmor/cli/public_capsule.zip`

 * *Files identical despite different names*

## Comparing `pyarmor/cli/register.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/register.py`

 * *Files 4% similar despite different names*

```diff
@@ -149,39 +149,78 @@
         path = self.ctx.reg_path
         with ZipFile(regfile, 'r') as f:
             for item in ('license.lic', '.pyarmor_capsule.zip'):
                 logger.debug('extracting %s', item)
                 f.extract(item, path=path)
             namelist = f.namelist()
             if 'group.tokens' in namelist:
-                machid = self._get_machine_id()
-                name = '/'.join(['tokens', machid.decode('utf-8')])
+                machid = self._get_machine_id().decode('utf-8')
+                name = '/'.join(['tokens', machid])
                 if name not in namelist:
-                    logger.debug('no found "%s" in offline regfile', name)
-                    raise CliError('this regfile is not for this device')
+                    machid = self._get_docker_hostname()
+                    if not machid:
+                        raise CliError('could not get docker host machine id')
+                    hostname = '/'.join(['tokens', machid])
+                    if hostname not in namelist:
+                        logger.debug('no found "%s" in offline regfile', name)
+                        raise CliError('this regfile is not for this device')
+                    name = hostname
                 logger.debug('extracting %s', name)
                 self.ctx.save_token(f.read(name))
                 return
             if 'group.info' in namelist:
                 raise CliError('wrong usage for group license, please '
                                'check `pyarmor reg` in Man page')
 
         logger.info('update license token')
         self.update_token()
 
-    def _get_machine_id(self):
+    def _get_docker_hostname(self):
+        try:
+            from socket import socket, AF_INET, SOCK_STREAM
+            host = 'host.docker.internal'
+            port = 29092
+            with socket(AF_INET, SOCK_STREAM) as s:
+                s.connect((host, port))
+                s.sendall(b'PADH' + b'x' * 60)
+                flag = s.recv(1)
+                if flag in (b'a', b'b'):
+                    data = s.recv(32)
+                machid = (flag + data).decode('utf-8')
+                logger.info('got docker host machine id: %s', machid)
+                return machid
+        except Exception:
+            logger.exception('could not get docker host machine id')
+
+    def _get_machine_id(self, idver=11):
         from .core import Pytransform3
-        return Pytransform3.get_hd_info(10)
+        return Pytransform3.get_hd_info(idver)
 
     def generate_group_device(self, devid):
+        from datetime import datetime
+        from platform import uname
         path = self.ctx.group_device_file(devid)
         logger.info('generating device file "%s"', path)
         os.makedirs(os.path.dirname(path), exist_ok=True)
+        uinfo = uname()
+        tpl = Template('\n'.join([
+            '# Generated by Pyarmor $rev, $timestamp',
+            'host: $node',
+            'system: $host ($version)',
+            'machine: $machine'
+        ])).substitute(
+            rev='.'.join(self.ctx.version),
+            node=uinfo.node,
+            host=uinfo.system,
+            version=uinfo.version,
+            timestamp=datetime.now().isoformat(),
+            machine=self._get_machine_id(16).decode('utf-8')
+        )
         with open(path, "wb") as f:
-            f.write(b'machine: ' + self._get_machine_id())
+            f.write(tpl.encode('utf-8'))
         return path
 
     def __str__(self):
         '''$advanced
 
 Notes
 $notes
@@ -260,15 +299,15 @@
             os.remove(self.ctx.license_token)
 
     def prepare(self, keyfile, product, upgrade=False):
         reginfo = self.parse_keyfile(keyfile)
         logger.info('prepare "%s"', keyfile)
 
         rcode = self._get_old_rcode() if upgrade else None
-        if upgrade and keyfile.endswith('regcode-to-pro.txt'):
+        if upgrade and not rcode and keyfile.endswith('regcode-to-pro.txt'):
             logger.error('please use `pyarmor-7 -v` to check old license')
             logger.error('this code is used to upgrade old license')
             raise CliError('no found old license in this machine')
         url = self.regurl(reginfo[1], rcode=rcode, prepare=True)
         logger.debug('url: %s', url)
 
         logger.info('query key file from server')
@@ -286,17 +325,17 @@
             info['product'] = product
         elif pname != product:
             logger.warning('this license is bind to product "%s"', pname)
             logger.warning('it can not be changed to "%s"', product)
 
         lines = []
         if upgrade:
-            if not (rcode and rcode.startswith('pyarmor-vax-')):
-                logger.error('please check Pyarmor 8.0 EULA')
-                raise CliError('old code "%s" can not be upgraded' % rcode)
+            if rcode and not rcode.startswith('pyarmor-vax-'):
+                logger.error('please check Pyarmor 8 EULA')
+                raise CliError('old license "%s" can not be upgraded' % rcode)
             if info['upgrade']:
                 lines.append(upgrade_to_pro_info.substitute(rcode=rcode))
             else:
                 lines.append(upgrade_to_basic_info.substitute())
         else:
             if info['lictype'] not in ('BASIC', 'PRO', 'GROUP'):
                 logger.error('this license does not work in Pyarmor 8')
```

## Comparing `pyarmor/cli/resource.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/resource.py`

 * *Files 6% similar despite different names*

```diff
@@ -40,15 +40,15 @@
     def _format_name(self, path):
         return os.path.splitext(os.path.basename(path))[0]
 
     def is_top(self):
         return self.parent is None
 
     def is_script(self):
-        return isinstance(self, FileResource)
+        return isinstance(self, (FileResource, PycResource))
 
     @property
     def fullname(self):
         return self.name if self.is_top() else \
             '.'.join([self.parent.fullname, self.name])
 
     @property
@@ -96,28 +96,40 @@
         return self.fullname.replace('.', os.path.sep) + self.pyext
 
     @property
     def frozenname(self):
         n = self.fullname.find('.__init__')
         return '<frozen %s>' % self.fullname[:None if n == -1 else n]
 
+    @property
+    def is_pyc(self):
+        return self.pyext.lower() == '.pyc'
+
     def readlines(self, encoding=None):
         if not os.path.exists(self.fullpath):
             raise RuntimeError('file "%s" doesn\'t exists' % self.fullpath)
 
         with open(self.fullpath, encoding=encoding) as f:
             # file.read() can't read the whole data of big files
             return f.readlines()
 
     def reparse(self, lines=None, encoding=None):
         if lines is None:
             lines = self.readlines(encoding=encoding)
         self.mtree = ast.parse(''.join(lines), self.frozenname, 'exec')
 
+    def _recompile_pyc(self):
+        from importlib._bootstrap_external import SourcelessFileLoader
+        path, name = self.fullpath, self.pkgname
+        self.mco = SourcelessFileLoader(name, path).get_code(name)
+
     def recompile(self, mtree=None, optimize=1):
+        if self.is_pyc:
+            return self._recompile_pyc()
+
         if mtree is None:
             mtree = self.mtree
         assert mtree is not None
         self.mco = compile(mtree, self.frozenname, 'exec', optimize=optimize)
 
     def clean(self):
         self.lines = None
@@ -135,23 +147,33 @@
         elif relative == 1:
             prefix = '.' * self.fullname.count('.')
         else:
             assert(isinstance(relative, str))
             prefix = relative + '.'
             if self.fullname.startswith(prefix):
                 prefix = '.' * self.fullname.count('.')
+            elif prefix.startswith(self.pkgname + '.'):
+                prefix = prefix[len(self.pkgname):]
 
         return Template(tpl).safe_substitute(
             timestamp=datetime.now().isoformat(),
             package=prefix + pkgname,
             path=bootpath,
             code=repr(code),
             rev=rev)
 
 
+class PycResource(FileResource):
+
+    def recompile(self, mtree=None, optimize=1):
+        from importlib._bootstrap_external import SourcelessFileLoader
+        path, name = self.fullpath, self.pkgname
+        self.mco = SourcelessFileLoader(name, path).get_code(name)
+
+
 class PathResource(Resource):
 
     def __init__(self, path, name=None, parent=None):
         super().__init__(path, name=name, parent=parent)
         self.respaths = []
         self.resfiles = []
```

## Comparing `pyarmor/cli/shell.py` & `pyarmor.cli-8.3.dev1/pyarmor/cli/shell.py`

 * *Files identical despite different names*

## Comparing `pyarmor.cli-8.2.dev2.dist-info/METADATA` & `pyarmor.cli-8.3.dev1/README.rst`

 * *Files 20% similar despite different names*

```diff
@@ -1,29 +1,7 @@
-Metadata-Version: 2.1
-Name: pyarmor.cli
-Version: 8.2.dev2
-Summary: A comand line tool to obfuscate python scripts
-Home-page: https://github.com/dashingsoft/pyarmor
-Author: Jondy Zhao
-Author-email: pyarmor@163.com
-License: Free To Use But Restricted
-Keywords: protect obfuscate encrypt obfuscation distribute
-Platform: UNKNOWN
-Classifier: Programming Language :: Python :: 3
-Classifier: License :: Free To Use But Restricted
-Classifier: Operating System :: MacOS
-Classifier: Operating System :: Microsoft :: Windows
-Classifier: Operating System :: POSIX
-Classifier: Intended Audience :: Developers
-Classifier: Topic :: Software Development :: Build Tools
-Classifier: Topic :: Utilities
-Classifier: Topic :: Security
-Classifier: Topic :: System :: Software Distribution
-Requires-Dist: pyarmor.core (~=3.2.0)
-
 Protect Python Scripts By Pyarmor
 =================================
 
 Pyarmor is a command line tool used to obfuscate python scripts, bind
 obfuscated scripts to fixed machine or expire obfuscated scripts.
 
 Key Features
@@ -75,9 +53,7 @@
 --------------
 
 - `Home <https://github.com/dashingsoft/pyarmor>`_
 - `Website <http://pyarmor.dashingsoft.com>`_
 - `中文网站 <http://pyarmor.dashingsoft.com/index-zh.html>`_
 - `Issues <https://github.com/dashingsoft/pyarmor/issues>`_
 - `Documentation <https://pyarmor.readthedocs.io/>`_
-
-
```

