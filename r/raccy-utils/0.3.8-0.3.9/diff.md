# Comparing `tmp/raccy_utils-0.3.8-py3-none-any.whl.zip` & `tmp/raccy_utils-0.3.9-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,15 +1,15 @@
-Zip file size: 14470 bytes, number of entries: 13
--rw-rw-rw-  2.0 fat      906 b- defN 22-Oct-01 17:17 ru/__init__.py
--rw-rw-rw-  2.0 fat      156 b- defN 22-Sep-21 10:55 ru/annotations/__init__.py
--rw-rw-rw-  2.0 fat     4691 b- defN 22-Sep-21 10:55 ru/config/__init__.py
--rw-rw-rw-  2.0 fat      577 b- defN 22-Sep-03 13:18 ru/exceptions/__init__.py
--rw-rw-rw-  2.0 fat      886 b- defN 22-Sep-03 13:18 ru/exceptions/exceptions.py
--rw-rw-rw-  2.0 fat     4224 b- defN 22-Sep-21 10:55 ru/logger/__init__.py
--rw-rw-rw-  2.0 fat     7006 b- defN 22-Oct-01 17:16 ru/selenium_utils/__init__.py
--rw-rw-rw-  2.0 fat     3185 b- defN 22-Oct-01 17:17 ru/utils/__init__.py
--rw-rw-rw-  2.0 fat    11558 b- defN 22-Oct-01 17:18 raccy_utils-0.3.8.dist-info/LICENSE
--rw-rw-rw-  2.0 fat     1810 b- defN 22-Oct-01 17:18 raccy_utils-0.3.8.dist-info/METADATA
--rw-rw-rw-  2.0 fat       92 b- defN 22-Oct-01 17:18 raccy_utils-0.3.8.dist-info/WHEEL
--rw-rw-rw-  2.0 fat        3 b- defN 22-Oct-01 17:18 raccy_utils-0.3.8.dist-info/top_level.txt
-?rw-rw-r--  2.0 fat     1041 b- defN 22-Oct-01 17:18 raccy_utils-0.3.8.dist-info/RECORD
-13 files, 36135 bytes uncompressed, 12736 bytes compressed:  64.8%
+Zip file size: 14577 bytes, number of entries: 13
+-rw-rw-rw-  2.0 fat      906 b- defN 22-Oct-25 21:58 ru/__init__.py
+-rw-rw-rw-  2.0 fat      156 b- defN 22-Oct-20 02:55 ru/annotations/__init__.py
+-rw-rw-rw-  2.0 fat     4678 b- defN 22-Oct-25 21:58 ru/config/__init__.py
+-rw-rw-rw-  2.0 fat      577 b- defN 22-Oct-20 02:55 ru/exceptions/__init__.py
+-rw-rw-rw-  2.0 fat      886 b- defN 22-Oct-20 02:55 ru/exceptions/exceptions.py
+-rw-rw-rw-  2.0 fat     4786 b- defN 22-Oct-25 22:20 ru/logger/__init__.py
+-rw-rw-rw-  2.0 fat     7006 b- defN 22-Oct-20 02:55 ru/selenium_utils/__init__.py
+-rw-rw-rw-  2.0 fat     3185 b- defN 22-Oct-20 02:55 ru/utils/__init__.py
+-rw-rw-rw-  2.0 fat    11357 b- defN 22-Oct-25 22:25 raccy_utils-0.3.9.dist-info/LICENSE
+-rw-rw-rw-  2.0 fat     1810 b- defN 22-Oct-25 22:25 raccy_utils-0.3.9.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 22-Oct-25 22:25 raccy_utils-0.3.9.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat        3 b- defN 22-Oct-25 22:25 raccy_utils-0.3.9.dist-info/top_level.txt
+?rw-rw-r--  2.0 fat     1041 b- defN 22-Oct-25 22:25 raccy_utils-0.3.9.dist-info/RECORD
+13 files, 36483 bytes uncompressed, 12843 bytes compressed:  64.8%
```

## zipnote {}

```diff
@@ -18,23 +18,23 @@
 
 Filename: ru/selenium_utils/__init__.py
 Comment: 
 
 Filename: ru/utils/__init__.py
 Comment: 
 
-Filename: raccy_utils-0.3.8.dist-info/LICENSE
+Filename: raccy_utils-0.3.9.dist-info/LICENSE
 Comment: 
 
-Filename: raccy_utils-0.3.8.dist-info/METADATA
+Filename: raccy_utils-0.3.9.dist-info/METADATA
 Comment: 
 
-Filename: raccy_utils-0.3.8.dist-info/WHEEL
+Filename: raccy_utils-0.3.9.dist-info/WHEEL
 Comment: 
 
-Filename: raccy_utils-0.3.8.dist-info/top_level.txt
+Filename: raccy_utils-0.3.9.dist-info/top_level.txt
 Comment: 
 
-Filename: raccy_utils-0.3.8.dist-info/RECORD
+Filename: raccy_utils-0.3.9.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## ru/__init__.py

```diff
@@ -12,15 +12,15 @@
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
 """
 from .config import JsonConfig, TextConfig
 from .logger import logger, ColorPrint, AsyncColorPrint
 
-__version__: str = '0.3.8'
+__version__: str = '0.3.9'
 
 __all__: list = ['JsonConfig',
                  'TextConfig',
                  'logger',
                  'ColorPrint',
                  'AsyncColorPrint',
                  '__version__']
```

## ru/config/__init__.py

```diff
@@ -69,15 +69,15 @@
 
     def load(self) -> Config:
         try:
             return self.load_config()
         except FileNotFoundError:
             raise ConfigFileNotFoundError(f"{self.__class__.__name__}: Config file '{self.CONFIG_PATH}' not found!")
 
-    def __getitem__(self, item: typing.Union[list, str]) -> typing.Union[str, list]:
+    def __getitem__(self, item: typing.Union[list, str]) -> typing.Any:
         with self._mutex:
             try:
                 if isinstance(item, list):
                     items: list = [self._config[key] for key in item]
                     return items
                 else:
                     return self._config[item]
```

## ru/logger/__init__.py

```diff
@@ -15,14 +15,15 @@
 """
 import logging
 import pathlib
 import os
 import asyncio
 import threading
 import typing
+import traceback
 
 from colorama import Fore
 
 from ru.annotations import Path
 
 
 def logger(
@@ -95,16 +96,25 @@
 
     def warning(self, text: str, color: str = Fore.YELLOW) -> None:
         self._print(text, color)
 
     def success(self, text: str, color: str = Fore.GREEN) -> None:
         self._print(text, color)
 
-    def error(self, text: str, color: str = Fore.RED) -> None:
-        self._print(text, color)
+    def error(self, error: typing.Union[str, BaseException], color: str = Fore.RED) -> None:
+        if isinstance(error, BaseException):
+            msg = self.get_error_message(error)
+            self._print(msg, color)
+        else:
+            self._print(error, color)
+
+    @staticmethod
+    def get_error_message(e: BaseException) -> str:
+        msg = ''.join(traceback.format_exception(type(e), e, e.__traceback__))
+        return msg
 
 
 class ColorPrint(BaseColorPrint):
     mutex: threading.Lock = threading.Lock()
 
 
 class AsyncColorPrint(BaseColorPrint):
@@ -119,9 +129,13 @@
 
     async def warning(self, text: str, color: str = Fore.YELLOW) -> None:
         await self._print(text, color)
 
     async def success(self, text: str, color: str = Fore.GREEN) -> None:
         await self._print(text, color)
 
-    async def error(self, text: str, color: str = Fore.RED) -> None:
-        await self._print(text, color)
+    async def error(self, error: typing.Union[str, BaseException], color: str = Fore.RED) -> None:
+        if isinstance(error, BaseException):
+            msg = self.get_error_message(error)
+            await self._print(msg, color)
+        else:
+            await self._print(error, color)
```

## Comparing `raccy_utils-0.3.8.dist-info/LICENSE` & `raccy_utils-0.3.9.dist-info/LICENSE`

 * *Ordering differences only*

 * *Files 12% similar despite different names*

```diff
@@ -1,201 +1,201 @@
-                                 Apache License
-                           Version 2.0, January 2004
-                        http://www.apache.org/licenses/
-
-   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
-
-   1. Definitions.
-
-      "License" shall mean the terms and conditions for use, reproduction,
-      and distribution as defined by Sections 1 through 9 of this document.
-
-      "Licensor" shall mean the copyright owner or entity authorized by
-      the copyright owner that is granting the License.
-
-      "Legal Entity" shall mean the union of the acting entity and all
-      other entities that control, are controlled by, or are under common
-      control with that entity. For the purposes of this definition,
-      "control" means (i) the power, direct or indirect, to cause the
-      direction or management of such entity, whether by contract or
-      otherwise, or (ii) ownership of fifty percent (50%) or more of the
-      outstanding shares, or (iii) beneficial ownership of such entity.
-
-      "You" (or "Your") shall mean an individual or Legal Entity
-      exercising permissions granted by this License.
-
-      "Source" form shall mean the preferred form for making modifications,
-      including but not limited to software source code, documentation
-      source, and configuration files.
-
-      "Object" form shall mean any form resulting from mechanical
-      transformation or translation of a Source form, including but
-      not limited to compiled object code, generated documentation,
-      and conversions to other media types.
-
-      "Work" shall mean the work of authorship, whether in Source or
-      Object form, made available under the License, as indicated by a
-      copyright notice that is included in or attached to the work
-      (an example is provided in the Appendix below).
-
-      "Derivative Works" shall mean any work, whether in Source or Object
-      form, that is based on (or derived from) the Work and for which the
-      editorial revisions, annotations, elaborations, or other modifications
-      represent, as a whole, an original work of authorship. For the purposes
-      of this License, Derivative Works shall not include works that remain
-      separable from, or merely link (or bind by name) to the interfaces of,
-      the Work and Derivative Works thereof.
-
-      "Contribution" shall mean any work of authorship, including
-      the original version of the Work and any modifications or additions
-      to that Work or Derivative Works thereof, that is intentionally
-      submitted to Licensor for inclusion in the Work by the copyright owner
-      or by an individual or Legal Entity authorized to submit on behalf of
-      the copyright owner. For the purposes of this definition, "submitted"
-      means any form of electronic, verbal, or written communication sent
-      to the Licensor or its representatives, including but not limited to
-      communication on electronic mailing lists, source code control systems,
-      and issue tracking systems that are managed by, or on behalf of, the
-      Licensor for the purpose of discussing and improving the Work, but
-      excluding communication that is conspicuously marked or otherwise
-      designated in writing by the copyright owner as "Not a Contribution."
-
-      "Contributor" shall mean Licensor and any individual or Legal Entity
-      on behalf of whom a Contribution has been received by Licensor and
-      subsequently incorporated within the Work.
-
-   2. Grant of Copyright License. Subject to the terms and conditions of
-      this License, each Contributor hereby grants to You a perpetual,
-      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
-      copyright license to reproduce, prepare Derivative Works of,
-      publicly display, publicly perform, sublicense, and distribute the
-      Work and such Derivative Works in Source or Object form.
-
-   3. Grant of Patent License. Subject to the terms and conditions of
-      this License, each Contributor hereby grants to You a perpetual,
-      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
-      (except as stated in this section) patent license to make, have made,
-      use, offer to sell, sell, import, and otherwise transfer the Work,
-      where such license applies only to those patent claims licensable
-      by such Contributor that are necessarily infringed by their
-      Contribution(s) alone or by combination of their Contribution(s)
-      with the Work to which such Contribution(s) was submitted. If You
-      institute patent litigation against any entity (including a
-      cross-claim or counterclaim in a lawsuit) alleging that the Work
-      or a Contribution incorporated within the Work constitutes direct
-      or contributory patent infringement, then any patent licenses
-      granted to You under this License for that Work shall terminate
-      as of the date such litigation is filed.
-
-   4. Redistribution. You may reproduce and distribute copies of the
-      Work or Derivative Works thereof in any medium, with or without
-      modifications, and in Source or Object form, provided that You
-      meet the following conditions:
-
-      (a) You must give any other recipients of the Work or
-          Derivative Works a copy of this License; and
-
-      (b) You must cause any modified files to carry prominent notices
-          stating that You changed the files; and
-
-      (c) You must retain, in the Source form of any Derivative Works
-          that You distribute, all copyright, patent, trademark, and
-          attribution notices from the Source form of the Work,
-          excluding those notices that do not pertain to any part of
-          the Derivative Works; and
-
-      (d) If the Work includes a "NOTICE" text file as part of its
-          distribution, then any Derivative Works that You distribute must
-          include a readable copy of the attribution notices contained
-          within such NOTICE file, excluding those notices that do not
-          pertain to any part of the Derivative Works, in at least one
-          of the following places: within a NOTICE text file distributed
-          as part of the Derivative Works; within the Source form or
-          documentation, if provided along with the Derivative Works; or,
-          within a display generated by the Derivative Works, if and
-          wherever such third-party notices normally appear. The contents
-          of the NOTICE file are for informational purposes only and
-          do not modify the License. You may add Your own attribution
-          notices within Derivative Works that You distribute, alongside
-          or as an addendum to the NOTICE text from the Work, provided
-          that such additional attribution notices cannot be construed
-          as modifying the License.
-
-      You may add Your own copyright statement to Your modifications and
-      may provide additional or different license terms and conditions
-      for use, reproduction, or distribution of Your modifications, or
-      for any such Derivative Works as a whole, provided Your use,
-      reproduction, and distribution of the Work otherwise complies with
-      the conditions stated in this License.
-
-   5. Submission of Contributions. Unless You explicitly state otherwise,
-      any Contribution intentionally submitted for inclusion in the Work
-      by You to the Licensor shall be under the terms and conditions of
-      this License, without any additional terms or conditions.
-      Notwithstanding the above, nothing herein shall supersede or modify
-      the terms of any separate license agreement you may have executed
-      with Licensor regarding such Contributions.
-
-   6. Trademarks. This License does not grant permission to use the trade
-      names, trademarks, service marks, or product names of the Licensor,
-      except as required for reasonable and customary use in describing the
-      origin of the Work and reproducing the content of the NOTICE file.
-
-   7. Disclaimer of Warranty. Unless required by applicable law or
-      agreed to in writing, Licensor provides the Work (and each
-      Contributor provides its Contributions) on an "AS IS" BASIS,
-      WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
-      implied, including, without limitation, any warranties or conditions
-      of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
-      PARTICULAR PURPOSE. You are solely responsible for determining the
-      appropriateness of using or redistributing the Work and assume any
-      risks associated with Your exercise of permissions under this License.
-
-   8. Limitation of Liability. In no event and under no legal theory,
-      whether in tort (including negligence), contract, or otherwise,
-      unless required by applicable law (such as deliberate and grossly
-      negligent acts) or agreed to in writing, shall any Contributor be
-      liable to You for damages, including any direct, indirect, special,
-      incidental, or consequential damages of any character arising as a
-      result of this License or out of the use or inability to use the
-      Work (including but not limited to damages for loss of goodwill,
-      work stoppage, computer failure or malfunction, or any and all
-      other commercial damages or losses), even if such Contributor
-      has been advised of the possibility of such damages.
-
-   9. Accepting Warranty or Additional Liability. While redistributing
-      the Work or Derivative Works thereof, You may choose to offer,
-      and charge a fee for, acceptance of support, warranty, indemnity,
-      or other liability obligations and/or rights consistent with this
-      License. However, in accepting such obligations, You may act only
-      on Your own behalf and on Your sole responsibility, not on behalf
-      of any other Contributor, and only if You agree to indemnify,
-      defend, and hold each Contributor harmless for any liability
-      incurred by, or claims asserted against, such Contributor by reason
-      of your accepting any such warranty or additional liability.
-
-   END OF TERMS AND CONDITIONS
-
-   APPENDIX: How to apply the Apache License to your work.
-
-      To apply the Apache License to your work, attach the following
-      boilerplate notice, with the fields enclosed by brackets "[]"
-      replaced with your own identifying information. (Don't include
-      the brackets!)  The text should be enclosed in the appropriate
-      comment syntax for the file format. We also recommend that a
-      file or class name and description of purpose be included on the
-      same "printed page" as the copyright notice for easier
-      identification within third-party archives.
-
-   Copyright [yyyy] [name of copyright owner]
-
-   Licensed under the Apache License, Version 2.0 (the "License");
-   you may not use this file except in compliance with the License.
-   You may obtain a copy of the License at
-
-       http://www.apache.org/licenses/LICENSE-2.0
-
-   Unless required by applicable law or agreed to in writing, software
-   distributed under the License is distributed on an "AS IS" BASIS,
-   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
-   See the License for the specific language governing permissions and
-   limitations under the License.
+                                 Apache License
+                           Version 2.0, January 2004
+                        http://www.apache.org/licenses/
+
+   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
+
+   1. Definitions.
+
+      "License" shall mean the terms and conditions for use, reproduction,
+      and distribution as defined by Sections 1 through 9 of this document.
+
+      "Licensor" shall mean the copyright owner or entity authorized by
+      the copyright owner that is granting the License.
+
+      "Legal Entity" shall mean the union of the acting entity and all
+      other entities that control, are controlled by, or are under common
+      control with that entity. For the purposes of this definition,
+      "control" means (i) the power, direct or indirect, to cause the
+      direction or management of such entity, whether by contract or
+      otherwise, or (ii) ownership of fifty percent (50%) or more of the
+      outstanding shares, or (iii) beneficial ownership of such entity.
+
+      "You" (or "Your") shall mean an individual or Legal Entity
+      exercising permissions granted by this License.
+
+      "Source" form shall mean the preferred form for making modifications,
+      including but not limited to software source code, documentation
+      source, and configuration files.
+
+      "Object" form shall mean any form resulting from mechanical
+      transformation or translation of a Source form, including but
+      not limited to compiled object code, generated documentation,
+      and conversions to other media types.
+
+      "Work" shall mean the work of authorship, whether in Source or
+      Object form, made available under the License, as indicated by a
+      copyright notice that is included in or attached to the work
+      (an example is provided in the Appendix below).
+
+      "Derivative Works" shall mean any work, whether in Source or Object
+      form, that is based on (or derived from) the Work and for which the
+      editorial revisions, annotations, elaborations, or other modifications
+      represent, as a whole, an original work of authorship. For the purposes
+      of this License, Derivative Works shall not include works that remain
+      separable from, or merely link (or bind by name) to the interfaces of,
+      the Work and Derivative Works thereof.
+
+      "Contribution" shall mean any work of authorship, including
+      the original version of the Work and any modifications or additions
+      to that Work or Derivative Works thereof, that is intentionally
+      submitted to Licensor for inclusion in the Work by the copyright owner
+      or by an individual or Legal Entity authorized to submit on behalf of
+      the copyright owner. For the purposes of this definition, "submitted"
+      means any form of electronic, verbal, or written communication sent
+      to the Licensor or its representatives, including but not limited to
+      communication on electronic mailing lists, source code control systems,
+      and issue tracking systems that are managed by, or on behalf of, the
+      Licensor for the purpose of discussing and improving the Work, but
+      excluding communication that is conspicuously marked or otherwise
+      designated in writing by the copyright owner as "Not a Contribution."
+
+      "Contributor" shall mean Licensor and any individual or Legal Entity
+      on behalf of whom a Contribution has been received by Licensor and
+      subsequently incorporated within the Work.
+
+   2. Grant of Copyright License. Subject to the terms and conditions of
+      this License, each Contributor hereby grants to You a perpetual,
+      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
+      copyright license to reproduce, prepare Derivative Works of,
+      publicly display, publicly perform, sublicense, and distribute the
+      Work and such Derivative Works in Source or Object form.
+
+   3. Grant of Patent License. Subject to the terms and conditions of
+      this License, each Contributor hereby grants to You a perpetual,
+      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
+      (except as stated in this section) patent license to make, have made,
+      use, offer to sell, sell, import, and otherwise transfer the Work,
+      where such license applies only to those patent claims licensable
+      by such Contributor that are necessarily infringed by their
+      Contribution(s) alone or by combination of their Contribution(s)
+      with the Work to which such Contribution(s) was submitted. If You
+      institute patent litigation against any entity (including a
+      cross-claim or counterclaim in a lawsuit) alleging that the Work
+      or a Contribution incorporated within the Work constitutes direct
+      or contributory patent infringement, then any patent licenses
+      granted to You under this License for that Work shall terminate
+      as of the date such litigation is filed.
+
+   4. Redistribution. You may reproduce and distribute copies of the
+      Work or Derivative Works thereof in any medium, with or without
+      modifications, and in Source or Object form, provided that You
+      meet the following conditions:
+
+      (a) You must give any other recipients of the Work or
+          Derivative Works a copy of this License; and
+
+      (b) You must cause any modified files to carry prominent notices
+          stating that You changed the files; and
+
+      (c) You must retain, in the Source form of any Derivative Works
+          that You distribute, all copyright, patent, trademark, and
+          attribution notices from the Source form of the Work,
+          excluding those notices that do not pertain to any part of
+          the Derivative Works; and
+
+      (d) If the Work includes a "NOTICE" text file as part of its
+          distribution, then any Derivative Works that You distribute must
+          include a readable copy of the attribution notices contained
+          within such NOTICE file, excluding those notices that do not
+          pertain to any part of the Derivative Works, in at least one
+          of the following places: within a NOTICE text file distributed
+          as part of the Derivative Works; within the Source form or
+          documentation, if provided along with the Derivative Works; or,
+          within a display generated by the Derivative Works, if and
+          wherever such third-party notices normally appear. The contents
+          of the NOTICE file are for informational purposes only and
+          do not modify the License. You may add Your own attribution
+          notices within Derivative Works that You distribute, alongside
+          or as an addendum to the NOTICE text from the Work, provided
+          that such additional attribution notices cannot be construed
+          as modifying the License.
+
+      You may add Your own copyright statement to Your modifications and
+      may provide additional or different license terms and conditions
+      for use, reproduction, or distribution of Your modifications, or
+      for any such Derivative Works as a whole, provided Your use,
+      reproduction, and distribution of the Work otherwise complies with
+      the conditions stated in this License.
+
+   5. Submission of Contributions. Unless You explicitly state otherwise,
+      any Contribution intentionally submitted for inclusion in the Work
+      by You to the Licensor shall be under the terms and conditions of
+      this License, without any additional terms or conditions.
+      Notwithstanding the above, nothing herein shall supersede or modify
+      the terms of any separate license agreement you may have executed
+      with Licensor regarding such Contributions.
+
+   6. Trademarks. This License does not grant permission to use the trade
+      names, trademarks, service marks, or product names of the Licensor,
+      except as required for reasonable and customary use in describing the
+      origin of the Work and reproducing the content of the NOTICE file.
+
+   7. Disclaimer of Warranty. Unless required by applicable law or
+      agreed to in writing, Licensor provides the Work (and each
+      Contributor provides its Contributions) on an "AS IS" BASIS,
+      WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
+      implied, including, without limitation, any warranties or conditions
+      of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
+      PARTICULAR PURPOSE. You are solely responsible for determining the
+      appropriateness of using or redistributing the Work and assume any
+      risks associated with Your exercise of permissions under this License.
+
+   8. Limitation of Liability. In no event and under no legal theory,
+      whether in tort (including negligence), contract, or otherwise,
+      unless required by applicable law (such as deliberate and grossly
+      negligent acts) or agreed to in writing, shall any Contributor be
+      liable to You for damages, including any direct, indirect, special,
+      incidental, or consequential damages of any character arising as a
+      result of this License or out of the use or inability to use the
+      Work (including but not limited to damages for loss of goodwill,
+      work stoppage, computer failure or malfunction, or any and all
+      other commercial damages or losses), even if such Contributor
+      has been advised of the possibility of such damages.
+
+   9. Accepting Warranty or Additional Liability. While redistributing
+      the Work or Derivative Works thereof, You may choose to offer,
+      and charge a fee for, acceptance of support, warranty, indemnity,
+      or other liability obligations and/or rights consistent with this
+      License. However, in accepting such obligations, You may act only
+      on Your own behalf and on Your sole responsibility, not on behalf
+      of any other Contributor, and only if You agree to indemnify,
+      defend, and hold each Contributor harmless for any liability
+      incurred by, or claims asserted against, such Contributor by reason
+      of your accepting any such warranty or additional liability.
+
+   END OF TERMS AND CONDITIONS
+
+   APPENDIX: How to apply the Apache License to your work.
+
+      To apply the Apache License to your work, attach the following
+      boilerplate notice, with the fields enclosed by brackets "[]"
+      replaced with your own identifying information. (Don't include
+      the brackets!)  The text should be enclosed in the appropriate
+      comment syntax for the file format. We also recommend that a
+      file or class name and description of purpose be included on the
+      same "printed page" as the copyright notice for easier
+      identification within third-party archives.
+
+   Copyright [yyyy] [name of copyright owner]
+
+   Licensed under the Apache License, Version 2.0 (the "License");
+   you may not use this file except in compliance with the License.
+   You may obtain a copy of the License at
+
+       http://www.apache.org/licenses/LICENSE-2.0
+
+   Unless required by applicable law or agreed to in writing, software
+   distributed under the License is distributed on an "AS IS" BASIS,
+   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
+   See the License for the specific language governing permissions and
+   limitations under the License.
```

## Comparing `raccy_utils-0.3.8.dist-info/METADATA` & `raccy_utils-0.3.9.dist-info/METADATA`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: raccy-utils
-Version: 0.3.8
+Version: 0.3.9
 Summary: A collection of utility functions, and classes.
 Home-page: https://github.com/danielafriyie/raccy-utils
 Author: Daniel Afriyie
 Author-email: danielafriyie98@gmail.com
 License: Apache License, Version 2.0
 Platform: UNKNOWN
 Classifier: Programming Language :: Python
```

## Comparing `raccy_utils-0.3.8.dist-info/RECORD` & `raccy_utils-0.3.9.dist-info/RECORD`

 * *Files 18% similar despite different names*

```diff
@@ -1,13 +1,13 @@
-ru/__init__.py,sha256=wuvRwsbo1cnmMrtN7n8OWfX_TPv3wWvsT6sfAr5gMDw,906
+ru/__init__.py,sha256=w-7CMewu3SOgEiJLoycFBxQ4flL0Fm_wNW-20F9ptSg,906
 ru/annotations/__init__.py,sha256=M_riXUKbhvXcdClXHUWSO9PH7UF-EUd4wM2e_3IbpNI,156
-ru/config/__init__.py,sha256=mZ5fJqoXw7rXUc8Q0PQvWwX-kzQGC58t8hb0i7aKPf4,4691
+ru/config/__init__.py,sha256=G4QTByRYRsQHK49JRaFhsFzRenD7TKwJ4QNBP-wBfIM,4678
 ru/exceptions/__init__.py,sha256=OcY2AOU0x_b71IHYNB6eZ36by6F308RDNsGy9gLtsO0,577
 ru/exceptions/exceptions.py,sha256=5JNBUlHIIbyTPw-l5KUj9rJ_tIgVl9tHg8ekLgTIJGc,886
-ru/logger/__init__.py,sha256=9zkYQQlBdQigaFbALHXLWAZiaD6qfnVrCXDS5RdHmHQ,4224
+ru/logger/__init__.py,sha256=Ggf69dxsngcwNd45QUkbCDEXvVEwlOmW4uUB1eelUpI,4786
 ru/selenium_utils/__init__.py,sha256=MCwMmV5ZwuJ9YFGxaXCC-8YVNw5fefab7Ft7tofk2X4,7006
 ru/utils/__init__.py,sha256=TAhnOhOsauNo_51Iei-sWFCsI1qXiCMu7FJ27C0ORXI,3185
-raccy_utils-0.3.8.dist-info/LICENSE,sha256=HrhfyXIkWY2tGFK11kg7vPCqhgh5DcxleloqdhrpyMY,11558
-raccy_utils-0.3.8.dist-info/METADATA,sha256=j39IG6lYs9XeOD3NgPKvAddb7mWnnhVVBimp_8XWtUg,1810
-raccy_utils-0.3.8.dist-info/WHEEL,sha256=G16H4A3IeoQmnOrYV4ueZGKSjhipXx8zc8nu9FGlvMA,92
-raccy_utils-0.3.8.dist-info/top_level.txt,sha256=99TbcZ2jniuu0eKJLsExQkgQBoAHhNCKlwJjDZJmCwo,3
-raccy_utils-0.3.8.dist-info/RECORD,,
+raccy_utils-0.3.9.dist-info/LICENSE,sha256=xx0jnfkXJvxRnG63LTGOxlggYnIysveWIZ6H3PNdCrQ,11357
+raccy_utils-0.3.9.dist-info/METADATA,sha256=1NvFj9-uLIDaoe-4yc0wq3YjvEBddndEFR6812y1mkA,1810
+raccy_utils-0.3.9.dist-info/WHEEL,sha256=G16H4A3IeoQmnOrYV4ueZGKSjhipXx8zc8nu9FGlvMA,92
+raccy_utils-0.3.9.dist-info/top_level.txt,sha256=99TbcZ2jniuu0eKJLsExQkgQBoAHhNCKlwJjDZJmCwo,3
+raccy_utils-0.3.9.dist-info/RECORD,,
```

