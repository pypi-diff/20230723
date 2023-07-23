# Comparing `tmp/xython-1.4.0.tar.gz` & `tmp/xython-1.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "xython-1.4.0.tar", last modified: Mon Jul  3 11:47:17 2023, max compression
+gzip compressed data, was "xython-1.5.0.tar", last modified: Sun Jul 23 11:20:39 2023, max compression
```

## Comparing `xython-1.4.0.tar` & `xython-1.5.0.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxrwxrwx   0        0        0        0 2023-07-03 11:47:17.279041 xython-1.4.0/
--rw-rw-rw-   0        0        0      388 2023-06-05 14:30:55.000000 xython-1.4.0/MANIFEST.in
--rw-rw-rw-   0        0        0    10625 2023-07-03 11:47:17.279041 xython-1.4.0/PKG-INFO
--rw-rw-rw-   0        0        0     9035 2023-06-16 12:39:01.000000 xython-1.4.0/README.md
--rw-rw-rw-   0        0        0        0 2021-06-11 06:00:16.000000 xython-1.4.0/requirements.txt
--rw-rw-rw-   0        0        0       86 2023-07-03 11:47:17.285994 xython-1.4.0/setup.cfg
--rw-rw-rw-   0        0        0      895 2023-07-03 11:26:20.000000 xython-1.4.0/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-03 11:47:17.107616 xython-1.4.0/src/
-drwxrwxrwx   0        0        0        0 2023-07-03 11:47:17.248857 xython-1.4.0/src/xython/
--rw-rw-rw-   0        0        0      467 2023-07-03 11:15:08.000000 xython-1.4.0/src/xython/__init__.py
--rw-rw-rw-   0        0        0    23487 2023-06-28 11:43:49.000000 xython-1.4.0/src/xython/anydb.py
--rw-rw-rw-   0        0        0    86378 2023-06-29 13:12:33.000000 xython-1.4.0/src/xython/basic_data.py
--rw-rw-rw-   0        0        0    24689 2023-06-27 12:35:21.000000 xython-1.4.0/src/xython/ganada.py
--rw-rw-rw-   0        0        0    19727 2023-06-27 10:43:06.000000 xython-1.4.0/src/xython/jfinder.py
--rw-rw-rw-   0        0        0    25128 2023-06-28 11:34:56.000000 xython-1.4.0/src/xython/mailmail.py
--rw-rw-rw-   0        0        0   165114 2023-07-01 11:36:47.000000 xython-1.4.0/src/xython/pcell.py
--rw-rw-rw-   0        0        0     5736 2023-04-08 04:25:55.000000 xython-1.4.0/src/xython/pcell_event.py
--rw-rw-rw-   0        0        0     9224 2023-06-27 12:05:29.000000 xython-1.4.0/src/xython/pyclick.py
--rw-rw-rw-   0        0        0    59645 2023-06-28 11:29:46.000000 xython-1.4.0/src/xython/pynal.py
--rw-rw-rw-   0        0        0    35896 2023-06-27 10:56:24.000000 xython-1.4.0/src/xython/scolor.py
--rw-rw-rw-   0        0        0    78637 2023-06-29 10:37:55.000000 xython-1.4.0/src/xython/youtil.py
-drwxrwxrwx   0        0        0        0 2023-07-03 11:47:17.274025 xython-1.4.0/src/xython.egg-info/
--rw-rw-rw-   0        0        0    10625 2023-07-03 11:47:16.000000 xython-1.4.0/src/xython.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      490 2023-07-03 11:47:17.000000 xython-1.4.0/src/xython.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-03 11:47:16.000000 xython-1.4.0/src/xython.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-07-03 11:47:16.000000 xython-1.4.0/src/xython.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0        7 2023-07-03 11:47:16.000000 xython-1.4.0/src/xython.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 11:20:39.466657 xython-1.5.0/
+-rw-rw-rw-   0        0        0      388 2023-06-05 14:30:55.000000 xython-1.5.0/MANIFEST.in
+-rw-rw-rw-   0        0        0     9608 2023-07-23 11:20:39.467075 xython-1.5.0/PKG-INFO
+-rw-rw-rw-   0        0        0     9035 2023-06-16 12:39:01.000000 xython-1.5.0/README.md
+-rw-rw-rw-   0        0        0        0 2021-06-11 06:00:16.000000 xython-1.5.0/requirements.txt
+-rw-rw-rw-   0        0        0       86 2023-07-23 11:20:39.469798 xython-1.5.0/setup.cfg
+-rw-rw-rw-   0        0        0      895 2023-07-23 11:15:29.000000 xython-1.5.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:20:39.309303 xython-1.5.0/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 11:20:39.418091 xython-1.5.0/src/xython/
+-rw-rw-rw-   0        0        0      467 2023-07-23 11:17:28.000000 xython-1.5.0/src/xython/__init__.py
+-rw-rw-rw-   0        0        0    25846 2023-07-06 21:56:34.000000 xython-1.5.0/src/xython/anydb.py
+-rw-rw-rw-   0        0        0    89081 2023-07-23 00:01:08.000000 xython-1.5.0/src/xython/basic_data.py
+-rw-rw-rw-   0        0        0    24689 2023-06-27 12:35:21.000000 xython-1.5.0/src/xython/ganada.py
+-rw-rw-rw-   0        0        0    19727 2023-06-27 10:43:06.000000 xython-1.5.0/src/xython/jfinder.py
+-rw-rw-rw-   0        0        0    25395 2023-07-14 05:34:42.000000 xython-1.5.0/src/xython/mailmail.py
+-rw-rw-rw-   0        0        0   168827 2023-07-23 05:39:17.000000 xython-1.5.0/src/xython/pcell.py
+-rw-rw-rw-   0        0        0     5736 2023-04-08 04:25:55.000000 xython-1.5.0/src/xython/pcell_event.py
+-rw-rw-rw-   0        0        0     9224 2023-06-27 12:05:29.000000 xython-1.5.0/src/xython/pyclick.py
+-rw-rw-rw-   0        0        0    63741 2023-07-13 21:18:07.000000 xython-1.5.0/src/xython/pynal.py
+-rw-rw-rw-   0        0        0    37024 2023-07-08 00:01:46.000000 xython-1.5.0/src/xython/scolor.py
+-rw-rw-rw-   0        0        0    82447 2023-07-23 08:24:54.000000 xython-1.5.0/src/xython/youtil.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:20:39.463657 xython-1.5.0/src/xython.egg-info/
+-rw-rw-rw-   0        0        0     9608 2023-07-23 11:20:39.000000 xython-1.5.0/src/xython.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      490 2023-07-23 11:20:39.000000 xython-1.5.0/src/xython.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:20:39.000000 xython-1.5.0/src/xython.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-07-23 11:20:39.000000 xython-1.5.0/src/xython.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0        7 2023-07-23 11:20:39.000000 xython-1.5.0/src/xython.egg-info/top_level.txt
```

### Comparing `xython-1.4.0/PKG-INFO` & `xython-1.5.0/README.md`

 * *Files 10% similar despite different names*

```diff
@@ -1,140 +1,127 @@
-Metadata-Version: 2.1
-Name: xython
-Version: 1.4.0
-Summary: Easy Read / Write for Excel, Word, Color, Etc using Python
-Home-page: https://github.com/sjpark/xython
-Author: sjpark
-Author-email: sjpkorea@yahoo.com
-License: UNKNOWN
-Download-URL: https://github.com/sjpark/xython/archive/v1.4.0.tar.gz
-Description: ## xython 모듈에 대하여
-        ### 개괄적인 설명
-        이모듈은 업무용으로 많이 사용하는 엑셀 , 색, 정규표현식, 등에 대하여 Python과 win32com을 기본으로 사용하여 각기 새롭게 모듈을 만들어서 좀더 쉽고 편하게 사용하고 만들자는 것입니다
-        자동화는 각자의 사용에 대한  
-        
-        만든 이유는 우리가 업무등을 하는 입장에서, 손으로 작업하기에는 양이 많고, 그렇다고
-        계속 반복적으로 일어나는 일은 아니며, VBA등을 만들어서 사용하기에는 어렵고 힘든 부분에 대해서
-        
-        파이썬이라는 훌룡한 언어를 위용하여, 좀더 쉽고 간결하게 몇가지 기능만 배워도 20줄안으로 자신만의 코드를
-        만들어 사용할수있는 기준을 만들기 위한 것입니다
-        
-        또한 보통 많이 사용하는 코드들은 첨부된 sample코드를 보시거나 저의 사이트에 와서 비슷한것을 다운 받은후
-        변경해서 사용하시기를 추천 드립니다
-        
-        좀더 편한 업무의 일을 하기위한 것입니다
-        
-        ### 구성은 
-        
-            - pcell : 엑셀을 다루는 것
-            - pcell_event : 엑셀의 이벤트를 다루는것
-            - scolor : 색의 RGB값을 편하게 사용가능하도록 만든 것
-            - jfinder : 정규표현식을 좀더 편하게 사용하도록 만든 것
-            - anydb : sqlite와 pandas 를 좀더 쉽게 사용할수있도록 만든것
-            - ganada : 워드를 다루기위해 만든 것
-            - mailmail : outlook을 다루는것
-            - pyclick : 키보드와 마우스를 다루는 모듈
-            - pynal : 시간과 날짜를 다루는것
-            - youtil : 이러저런 문장이나 시간등을 변환하는데 도움이되는 것
-            - basic_data : halmoney패키지에서 사용되는 전반적인 공유 자료들을 저장하는 곳
-        
-        각 사용사용방법들에 대해서는 아래의 사이트를 참고하세요
-        
-        * https://cafe.naver.com/pycell
-        * www.halmoney.com
-        * www.xython.co.kr
-        
-        
-        ## 기본 사용법
-        ### pcell
-        -각 메소드는 각각 별도의 내용으로 사용합니다
-        
-        Pcell의 모듈을 만들 때 나름대로 편하고 쉽게 이름을 만들려고 하였습니다. 기본적인 틀을 만들어 놓으니, 분명억지로 지어진 이름또한 있음을 시인합니다. 나름대로 생각하고 고심한끝에 만들어진 이름이오니 맘에 들지 않는 부분이 있이더라도 양해를 부탁드립니다
-        
-        물론, 지금의 이름이 최종이라고는 생각하지 않고 있습니다. 좋은 이름이라는것은 어떤 메소드가 들어가 있는지 잘 몰라도 거의 사용하는데 사람의 생각에서 쉽게 사용을 할수 있도록 만드는 것이라고 생각을 합니다
-        
-        아마 한 4~5번정오는 크게 이름을 변경한 것 같습니다. 만들어놓고 조금지나면 저스스로가 도데체 이것의 이름은 왜 이렇게 만들어놓은거야???라는 질문을 하는경우가 가끔있습니다. 이리바꾸고 저리바꾸어도 맘에 안드는구석이 아직 많습니다
-        
-        한사람의 이름이 인생에서 차지하는부분이 많듯이 제가만든것또한 그러하지만, 만약 맘에 안드시는 것이 있으시면 본인스스로가 바꾼어서 사용하셔도 됩니다
-        
-        단, 기존의것은 그대로 두시고 아래부분에 새로운 메소드를 추가하셔서 위의것을 그대로 사용하시면 될것입니다
-        
-        그래서 다음과 같은 원리를 이용해서 만들었으나, 조금은 틀린부분도 있지만…
-        
-        	1. 이름은 기본적으로 3부분으로 만들었으며 각부분은 언더바(_)로 연결했습니다
-        	2. 읽을때는 read, 쓸때는 write, 삭제는 delete, 추가는insert등을 사용하였습니다
-        	3. 두번째의 이름의 규칙은
-        		관련된 부분에 따라 다른것을 사용하며 다음과 같은 것이 사용이 됩니다
-        		거진 영역을 나타내는 부분으로 사용하였습니다
-        		range, workbook, cell, line, column
-        	4. 세번째 부분이 어떤 일을 할것인지를 알아보는 것입니다
-        	5. 일반사항은 다음과 같습니다
-        
-        -	모든함수에는 sheet가 명시되어야 합니다
-        -	값을 읽는것은 read로 시작하며
-        -	값을 쓰는 것은 write로 시작합니다
-        -	선을 긋는등의 그림은 dwg로 시작합니다
-        -	하나의 자료가 아닌, 자료의 묶음은 Range를 사용한다
-        -	두개의 문구사이에는 '_' 로 연결을 하였다 예) read_cell
-        -	메소드는 모두 소문자를 사용함
-        
-        예를 들어, 어떤셀에 값을 입력하는 것은 write_value_in_cell라는 이름으로 구성하였습니다
-        그리고 부가적으로 함수의 변수로 사용되는부분은 큰 것->작은것으로 만들었으며, 영역을 표시하는 부분은 모두 리스트를 기준으로 하나로 만들었습니다.
-        
-        그저, 그렇다는것을 이해바라며, 실질적으로 코드를 보시면 더 쉽게 이해가 가실것으로 생각됩니다.
-        보지않고 찾지않아도 함수의 이름을 생각해낼수있도록 만든다고 나름대로 정의한 것입니다.
-        
-        ### scolor
-        이것은 모든 외부로 들어오고 나가는 것은 전부 RGB형태로 이루어지도록 만든다
-        
-            - 색을 변경하고 관리하는 모듈이며
-            - 색의 변화를 잘 사용이 가능하도록 하기위한 것이다
-            - 기본 입력 예 : "빨강", "빨강55", "red55", "0155"
-            - 기본색 ==> 12색 + (하양, 검정, 회색),
-            - 큰변화 ==> 1~9단계, 작은변화 ==> 1~9단계
-            - 기본함수 : get_color_rgb("red55"), get_rgb_3input(색, 큰변화, 작은변화)
-            - 모든 색의 표현이나 결과는 rgb로 돌려준다
-        
-        ### Jfinder
-        이름을 **Jfinder**라고 지었으며, 아래와 같은 특성을 가지고 있다
-        
-        1. 건수는 ~를 사용하여 4~5라는 식으로 표현을 하였고
-        2. 한글, 영어와 같은 것은 대괄호를 사용하여 적용하였다 [한글]
-        3. 처음과 끝은 [처음], [끝]처럼 나타냈다
-        4. 그리고 이것은 누가 보아도 아~~ 무엇을 찾을려고 했는지를 알수있도록 하기위한것이며
-        5. 찾기기능중에 전부 찾아서 보기쉽도록 돌려주는 것과 같은 몇가지 메소드들을 만들어 넣었읍니다
-        제일 중요한 코드를 만드는 기능은 아래와 같읍니다
-        대략적으로 위의것을 읽은후에 보시면 이해가 되실부분이 많읍니다
-        
-        * 아래의 코드들은 정규표현식을 사용하면서, 내가 만든 표현식조차도 다시 읽기가 어려워서, 나름 다른 형태로 만들어 본것인데. 생각보다 가독성이 좋아서 같이 공유해보는것이다
-        또한 만든김에 결과로 돌려주는것도 하나만 받으면 전부 가능하도록 만들어 보았다
-        위에서 언급한 이메일 형식이 맞느지를 보는 것은 상당히 반복적이기 때문에 크게 혼돈은 없다
-        하지만, 실제 코드를 사용하다 보면, 외계어를 해석하는 상태까지 와야할 경우가 있다
-        
-        
-            ([a-zA-Z0-9_.+-]+)@[a-zA-Z0-9_.+-]+\.[a-zA-Z0-9_.+-]+
-        
-        * 이정도만해도 간단한 축에 속한다. 맨처음 만들때는 그나마 이해를 하지만, 다른사람이 만든 것을 이해하는데 상당한 시간이 걸린다는 것이고, 또한 일반적인 사용자들이 이것을 공부하고 이해하는데 어려움이 잇을 것 같으면서 동시에, 정규표현식의 강력함을 사용할수 있도록 생각해 보는 것이다
-        그래서 좀더 간단하게 사용법을 만들고,
-        
-        
-            [영어&숫자.+-:1~]@[영어&숫자.+-:1~]\.[영어&숫자.+-:1~]
-        이렇게 바꾸면 좀더 읽기가 쉬워진다
-        
-        **jfinder**에는 자주사용하는 언어를 등록할수도 있읍니다. 예를 들어 일본어나 한자를 등록한것처럼 하면 사용이 가능하다.
-        간단하게 다시 사용하는 방법을 알려주면, 너무 줄여놓은 정규표현식을 좀더 늘이는 것이라고 생각하면 됩니다. 여기에서 느낀 부분은 전문가가 사용하기에는 좋지만, 비전문가가 사용하기 쉽게, 예전에는 단어1개가 아주 중요한 속도까지 영향을 주지만, 지금은너무 줄이지 않아도 된다는 것이다. 기계에 가까운 언어에서 좀더 사용자에 가까운 언어로 만들어도 된다는 것이지요
-        파이선이 사용하기에 좀더 편한방법이 되는 것이지요
-        
-            - 대괄호로 묶는다
-            - 반복갯수는 대괄호안에 사용하며 ~로 나타낸다
-            - 맨처음 맨마지막등의 용어는 [처음], [끝]등의 이유로 나타낸다 
-            - 특수문자(re모듈내에 의미가있는 문자)는 \를 붙여서 사용한다
-            - 어떤문자의 앞과뒤에있을때는 (앞에있음:abc)이라고 사용하면 abc가 앞에있는 문자열을 찾는것이다
-        
-        ### mailmail
-        이름을 **mailmail**라고 지었으며, 아웃룩의 이메일을 관리하는 도구입니다
-        - 이것의 장점은 엑셀이나 Util과 연동하여 편의성을 더욱 증대하고있읍니다
-        - 기본적인 사용법이나 함수의 이름은 같은 형태를 따릅니다
-Platform: UNKNOWN
-Classifier: License :: OSI Approved :: MIT License
-Requires-Python: >=3.8
-Description-Content-Type: text/markdown
+## xython 모듈에 대하여
+### 개괄적인 설명
+이모듈은 업무용으로 많이 사용하는 엑셀 , 색, 정규표현식, 등에 대하여 Python과 win32com을 기본으로 사용하여 각기 새롭게 모듈을 만들어서 좀더 쉽고 편하게 사용하고 만들자는 것입니다
+자동화는 각자의 사용에 대한  
+
+만든 이유는 우리가 업무등을 하는 입장에서, 손으로 작업하기에는 양이 많고, 그렇다고
+계속 반복적으로 일어나는 일은 아니며, VBA등을 만들어서 사용하기에는 어렵고 힘든 부분에 대해서
+
+파이썬이라는 훌룡한 언어를 위용하여, 좀더 쉽고 간결하게 몇가지 기능만 배워도 20줄안으로 자신만의 코드를
+만들어 사용할수있는 기준을 만들기 위한 것입니다
+
+또한 보통 많이 사용하는 코드들은 첨부된 sample코드를 보시거나 저의 사이트에 와서 비슷한것을 다운 받은후
+변경해서 사용하시기를 추천 드립니다
+
+좀더 편한 업무의 일을 하기위한 것입니다
+
+### 구성은 
+
+    - pcell : 엑셀을 다루는 것
+    - pcell_event : 엑셀의 이벤트를 다루는것
+    - scolor : 색의 RGB값을 편하게 사용가능하도록 만든 것
+    - jfinder : 정규표현식을 좀더 편하게 사용하도록 만든 것
+    - anydb : sqlite와 pandas 를 좀더 쉽게 사용할수있도록 만든것
+    - ganada : 워드를 다루기위해 만든 것
+    - mailmail : outlook을 다루는것
+    - pyclick : 키보드와 마우스를 다루는 모듈
+    - pynal : 시간과 날짜를 다루는것
+    - youtil : 이러저런 문장이나 시간등을 변환하는데 도움이되는 것
+    - basic_data : halmoney패키지에서 사용되는 전반적인 공유 자료들을 저장하는 곳
+
+각 사용사용방법들에 대해서는 아래의 사이트를 참고하세요
+
+* https://cafe.naver.com/pycell
+* www.halmoney.com
+* www.xython.co.kr
+
+
+## 기본 사용법
+### pcell
+-각 메소드는 각각 별도의 내용으로 사용합니다
+
+Pcell의 모듈을 만들 때 나름대로 편하고 쉽게 이름을 만들려고 하였습니다. 기본적인 틀을 만들어 놓으니, 분명억지로 지어진 이름또한 있음을 시인합니다. 나름대로 생각하고 고심한끝에 만들어진 이름이오니 맘에 들지 않는 부분이 있이더라도 양해를 부탁드립니다
+
+물론, 지금의 이름이 최종이라고는 생각하지 않고 있습니다. 좋은 이름이라는것은 어떤 메소드가 들어가 있는지 잘 몰라도 거의 사용하는데 사람의 생각에서 쉽게 사용을 할수 있도록 만드는 것이라고 생각을 합니다
+
+아마 한 4~5번정오는 크게 이름을 변경한 것 같습니다. 만들어놓고 조금지나면 저스스로가 도데체 이것의 이름은 왜 이렇게 만들어놓은거야???라는 질문을 하는경우가 가끔있습니다. 이리바꾸고 저리바꾸어도 맘에 안드는구석이 아직 많습니다
+
+한사람의 이름이 인생에서 차지하는부분이 많듯이 제가만든것또한 그러하지만, 만약 맘에 안드시는 것이 있으시면 본인스스로가 바꾼어서 사용하셔도 됩니다
+
+단, 기존의것은 그대로 두시고 아래부분에 새로운 메소드를 추가하셔서 위의것을 그대로 사용하시면 될것입니다
+
+그래서 다음과 같은 원리를 이용해서 만들었으나, 조금은 틀린부분도 있지만…
+
+	1. 이름은 기본적으로 3부분으로 만들었으며 각부분은 언더바(_)로 연결했습니다
+	2. 읽을때는 read, 쓸때는 write, 삭제는 delete, 추가는insert등을 사용하였습니다
+	3. 두번째의 이름의 규칙은
+		관련된 부분에 따라 다른것을 사용하며 다음과 같은 것이 사용이 됩니다
+		거진 영역을 나타내는 부분으로 사용하였습니다
+		range, workbook, cell, line, column
+	4. 세번째 부분이 어떤 일을 할것인지를 알아보는 것입니다
+	5. 일반사항은 다음과 같습니다
+
+-	모든함수에는 sheet가 명시되어야 합니다
+-	값을 읽는것은 read로 시작하며
+-	값을 쓰는 것은 write로 시작합니다
+-	선을 긋는등의 그림은 dwg로 시작합니다
+-	하나의 자료가 아닌, 자료의 묶음은 Range를 사용한다
+-	두개의 문구사이에는 '_' 로 연결을 하였다 예) read_cell
+-	메소드는 모두 소문자를 사용함
+
+예를 들어, 어떤셀에 값을 입력하는 것은 write_value_in_cell라는 이름으로 구성하였습니다
+그리고 부가적으로 함수의 변수로 사용되는부분은 큰 것->작은것으로 만들었으며, 영역을 표시하는 부분은 모두 리스트를 기준으로 하나로 만들었습니다.
+
+그저, 그렇다는것을 이해바라며, 실질적으로 코드를 보시면 더 쉽게 이해가 가실것으로 생각됩니다.
+보지않고 찾지않아도 함수의 이름을 생각해낼수있도록 만든다고 나름대로 정의한 것입니다.
+
+### scolor
+이것은 모든 외부로 들어오고 나가는 것은 전부 RGB형태로 이루어지도록 만든다
+
+    - 색을 변경하고 관리하는 모듈이며
+    - 색의 변화를 잘 사용이 가능하도록 하기위한 것이다
+    - 기본 입력 예 : "빨강", "빨강55", "red55", "0155"
+    - 기본색 ==> 12색 + (하양, 검정, 회색),
+    - 큰변화 ==> 1~9단계, 작은변화 ==> 1~9단계
+    - 기본함수 : get_color_rgb("red55"), get_rgb_3input(색, 큰변화, 작은변화)
+    - 모든 색의 표현이나 결과는 rgb로 돌려준다
+
+### Jfinder
+이름을 **Jfinder**라고 지었으며, 아래와 같은 특성을 가지고 있다
+
+1. 건수는 ~를 사용하여 4~5라는 식으로 표현을 하였고
+2. 한글, 영어와 같은 것은 대괄호를 사용하여 적용하였다 [한글]
+3. 처음과 끝은 [처음], [끝]처럼 나타냈다
+4. 그리고 이것은 누가 보아도 아~~ 무엇을 찾을려고 했는지를 알수있도록 하기위한것이며
+5. 찾기기능중에 전부 찾아서 보기쉽도록 돌려주는 것과 같은 몇가지 메소드들을 만들어 넣었읍니다
+제일 중요한 코드를 만드는 기능은 아래와 같읍니다
+대략적으로 위의것을 읽은후에 보시면 이해가 되실부분이 많읍니다
+
+* 아래의 코드들은 정규표현식을 사용하면서, 내가 만든 표현식조차도 다시 읽기가 어려워서, 나름 다른 형태로 만들어 본것인데. 생각보다 가독성이 좋아서 같이 공유해보는것이다
+또한 만든김에 결과로 돌려주는것도 하나만 받으면 전부 가능하도록 만들어 보았다
+위에서 언급한 이메일 형식이 맞느지를 보는 것은 상당히 반복적이기 때문에 크게 혼돈은 없다
+하지만, 실제 코드를 사용하다 보면, 외계어를 해석하는 상태까지 와야할 경우가 있다
+
+
+    ([a-zA-Z0-9_.+-]+)@[a-zA-Z0-9_.+-]+\.[a-zA-Z0-9_.+-]+
+
+* 이정도만해도 간단한 축에 속한다. 맨처음 만들때는 그나마 이해를 하지만, 다른사람이 만든 것을 이해하는데 상당한 시간이 걸린다는 것이고, 또한 일반적인 사용자들이 이것을 공부하고 이해하는데 어려움이 잇을 것 같으면서 동시에, 정규표현식의 강력함을 사용할수 있도록 생각해 보는 것이다
+그래서 좀더 간단하게 사용법을 만들고,
+
+
+    [영어&숫자.+-:1~]@[영어&숫자.+-:1~]\.[영어&숫자.+-:1~]
+이렇게 바꾸면 좀더 읽기가 쉬워진다
+
+**jfinder**에는 자주사용하는 언어를 등록할수도 있읍니다. 예를 들어 일본어나 한자를 등록한것처럼 하면 사용이 가능하다.
+간단하게 다시 사용하는 방법을 알려주면, 너무 줄여놓은 정규표현식을 좀더 늘이는 것이라고 생각하면 됩니다. 여기에서 느낀 부분은 전문가가 사용하기에는 좋지만, 비전문가가 사용하기 쉽게, 예전에는 단어1개가 아주 중요한 속도까지 영향을 주지만, 지금은너무 줄이지 않아도 된다는 것이다. 기계에 가까운 언어에서 좀더 사용자에 가까운 언어로 만들어도 된다는 것이지요
+파이선이 사용하기에 좀더 편한방법이 되는 것이지요
+
+    - 대괄호로 묶는다
+    - 반복갯수는 대괄호안에 사용하며 ~로 나타낸다
+    - 맨처음 맨마지막등의 용어는 [처음], [끝]등의 이유로 나타낸다 
+    - 특수문자(re모듈내에 의미가있는 문자)는 \를 붙여서 사용한다
+    - 어떤문자의 앞과뒤에있을때는 (앞에있음:abc)이라고 사용하면 abc가 앞에있는 문자열을 찾는것이다
+
+### mailmail
+이름을 **mailmail**라고 지었으며, 아웃룩의 이메일을 관리하는 도구입니다
+- 이것의 장점은 엑셀이나 Util과 연동하여 편의성을 더욱 증대하고있읍니다
+- 기본적인 사용법이나 함수의 이름은 같은 형태를 따릅니다
```

### Comparing `xython-1.4.0/README.md` & `xython-1.5.0/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,127 +1,142 @@
-## xython 모듈에 대하여
-### 개괄적인 설명
-이모듈은 업무용으로 많이 사용하는 엑셀 , 색, 정규표현식, 등에 대하여 Python과 win32com을 기본으로 사용하여 각기 새롭게 모듈을 만들어서 좀더 쉽고 편하게 사용하고 만들자는 것입니다
-자동화는 각자의 사용에 대한  
-
-만든 이유는 우리가 업무등을 하는 입장에서, 손으로 작업하기에는 양이 많고, 그렇다고
-계속 반복적으로 일어나는 일은 아니며, VBA등을 만들어서 사용하기에는 어렵고 힘든 부분에 대해서
-
-파이썬이라는 훌룡한 언어를 위용하여, 좀더 쉽고 간결하게 몇가지 기능만 배워도 20줄안으로 자신만의 코드를
-만들어 사용할수있는 기준을 만들기 위한 것입니다
-
-또한 보통 많이 사용하는 코드들은 첨부된 sample코드를 보시거나 저의 사이트에 와서 비슷한것을 다운 받은후
-변경해서 사용하시기를 추천 드립니다
-
-좀더 편한 업무의 일을 하기위한 것입니다
-
-### 구성은 
-
-    - pcell : 엑셀을 다루는 것
-    - pcell_event : 엑셀의 이벤트를 다루는것
-    - scolor : 색의 RGB값을 편하게 사용가능하도록 만든 것
-    - jfinder : 정규표현식을 좀더 편하게 사용하도록 만든 것
-    - anydb : sqlite와 pandas 를 좀더 쉽게 사용할수있도록 만든것
-    - ganada : 워드를 다루기위해 만든 것
-    - mailmail : outlook을 다루는것
-    - pyclick : 키보드와 마우스를 다루는 모듈
-    - pynal : 시간과 날짜를 다루는것
-    - youtil : 이러저런 문장이나 시간등을 변환하는데 도움이되는 것
-    - basic_data : halmoney패키지에서 사용되는 전반적인 공유 자료들을 저장하는 곳
-
-각 사용사용방법들에 대해서는 아래의 사이트를 참고하세요
-
-* https://cafe.naver.com/pycell
-* www.halmoney.com
-* www.xython.co.kr
-
-
-## 기본 사용법
-### pcell
--각 메소드는 각각 별도의 내용으로 사용합니다
-
-Pcell의 모듈을 만들 때 나름대로 편하고 쉽게 이름을 만들려고 하였습니다. 기본적인 틀을 만들어 놓으니, 분명억지로 지어진 이름또한 있음을 시인합니다. 나름대로 생각하고 고심한끝에 만들어진 이름이오니 맘에 들지 않는 부분이 있이더라도 양해를 부탁드립니다
-
-물론, 지금의 이름이 최종이라고는 생각하지 않고 있습니다. 좋은 이름이라는것은 어떤 메소드가 들어가 있는지 잘 몰라도 거의 사용하는데 사람의 생각에서 쉽게 사용을 할수 있도록 만드는 것이라고 생각을 합니다
-
-아마 한 4~5번정오는 크게 이름을 변경한 것 같습니다. 만들어놓고 조금지나면 저스스로가 도데체 이것의 이름은 왜 이렇게 만들어놓은거야???라는 질문을 하는경우가 가끔있습니다. 이리바꾸고 저리바꾸어도 맘에 안드는구석이 아직 많습니다
-
-한사람의 이름이 인생에서 차지하는부분이 많듯이 제가만든것또한 그러하지만, 만약 맘에 안드시는 것이 있으시면 본인스스로가 바꾼어서 사용하셔도 됩니다
-
-단, 기존의것은 그대로 두시고 아래부분에 새로운 메소드를 추가하셔서 위의것을 그대로 사용하시면 될것입니다
-
-그래서 다음과 같은 원리를 이용해서 만들었으나, 조금은 틀린부분도 있지만…
-
-	1. 이름은 기본적으로 3부분으로 만들었으며 각부분은 언더바(_)로 연결했습니다
-	2. 읽을때는 read, 쓸때는 write, 삭제는 delete, 추가는insert등을 사용하였습니다
-	3. 두번째의 이름의 규칙은
-		관련된 부분에 따라 다른것을 사용하며 다음과 같은 것이 사용이 됩니다
-		거진 영역을 나타내는 부분으로 사용하였습니다
-		range, workbook, cell, line, column
-	4. 세번째 부분이 어떤 일을 할것인지를 알아보는 것입니다
-	5. 일반사항은 다음과 같습니다
-
--	모든함수에는 sheet가 명시되어야 합니다
--	값을 읽는것은 read로 시작하며
--	값을 쓰는 것은 write로 시작합니다
--	선을 긋는등의 그림은 dwg로 시작합니다
--	하나의 자료가 아닌, 자료의 묶음은 Range를 사용한다
--	두개의 문구사이에는 '_' 로 연결을 하였다 예) read_cell
--	메소드는 모두 소문자를 사용함
-
-예를 들어, 어떤셀에 값을 입력하는 것은 write_value_in_cell라는 이름으로 구성하였습니다
-그리고 부가적으로 함수의 변수로 사용되는부분은 큰 것->작은것으로 만들었으며, 영역을 표시하는 부분은 모두 리스트를 기준으로 하나로 만들었습니다.
-
-그저, 그렇다는것을 이해바라며, 실질적으로 코드를 보시면 더 쉽게 이해가 가실것으로 생각됩니다.
-보지않고 찾지않아도 함수의 이름을 생각해낼수있도록 만든다고 나름대로 정의한 것입니다.
-
-### scolor
-이것은 모든 외부로 들어오고 나가는 것은 전부 RGB형태로 이루어지도록 만든다
-
-    - 색을 변경하고 관리하는 모듈이며
-    - 색의 변화를 잘 사용이 가능하도록 하기위한 것이다
-    - 기본 입력 예 : "빨강", "빨강55", "red55", "0155"
-    - 기본색 ==> 12색 + (하양, 검정, 회색),
-    - 큰변화 ==> 1~9단계, 작은변화 ==> 1~9단계
-    - 기본함수 : get_color_rgb("red55"), get_rgb_3input(색, 큰변화, 작은변화)
-    - 모든 색의 표현이나 결과는 rgb로 돌려준다
-
-### Jfinder
-이름을 **Jfinder**라고 지었으며, 아래와 같은 특성을 가지고 있다
-
-1. 건수는 ~를 사용하여 4~5라는 식으로 표현을 하였고
-2. 한글, 영어와 같은 것은 대괄호를 사용하여 적용하였다 [한글]
-3. 처음과 끝은 [처음], [끝]처럼 나타냈다
-4. 그리고 이것은 누가 보아도 아~~ 무엇을 찾을려고 했는지를 알수있도록 하기위한것이며
-5. 찾기기능중에 전부 찾아서 보기쉽도록 돌려주는 것과 같은 몇가지 메소드들을 만들어 넣었읍니다
-제일 중요한 코드를 만드는 기능은 아래와 같읍니다
-대략적으로 위의것을 읽은후에 보시면 이해가 되실부분이 많읍니다
-
-* 아래의 코드들은 정규표현식을 사용하면서, 내가 만든 표현식조차도 다시 읽기가 어려워서, 나름 다른 형태로 만들어 본것인데. 생각보다 가독성이 좋아서 같이 공유해보는것이다
-또한 만든김에 결과로 돌려주는것도 하나만 받으면 전부 가능하도록 만들어 보았다
-위에서 언급한 이메일 형식이 맞느지를 보는 것은 상당히 반복적이기 때문에 크게 혼돈은 없다
-하지만, 실제 코드를 사용하다 보면, 외계어를 해석하는 상태까지 와야할 경우가 있다
-
-
-    ([a-zA-Z0-9_.+-]+)@[a-zA-Z0-9_.+-]+\.[a-zA-Z0-9_.+-]+
-
-* 이정도만해도 간단한 축에 속한다. 맨처음 만들때는 그나마 이해를 하지만, 다른사람이 만든 것을 이해하는데 상당한 시간이 걸린다는 것이고, 또한 일반적인 사용자들이 이것을 공부하고 이해하는데 어려움이 잇을 것 같으면서 동시에, 정규표현식의 강력함을 사용할수 있도록 생각해 보는 것이다
-그래서 좀더 간단하게 사용법을 만들고,
-
-
-    [영어&숫자.+-:1~]@[영어&숫자.+-:1~]\.[영어&숫자.+-:1~]
-이렇게 바꾸면 좀더 읽기가 쉬워진다
-
-**jfinder**에는 자주사용하는 언어를 등록할수도 있읍니다. 예를 들어 일본어나 한자를 등록한것처럼 하면 사용이 가능하다.
-간단하게 다시 사용하는 방법을 알려주면, 너무 줄여놓은 정규표현식을 좀더 늘이는 것이라고 생각하면 됩니다. 여기에서 느낀 부분은 전문가가 사용하기에는 좋지만, 비전문가가 사용하기 쉽게, 예전에는 단어1개가 아주 중요한 속도까지 영향을 주지만, 지금은너무 줄이지 않아도 된다는 것이다. 기계에 가까운 언어에서 좀더 사용자에 가까운 언어로 만들어도 된다는 것이지요
-파이선이 사용하기에 좀더 편한방법이 되는 것이지요
-
-    - 대괄호로 묶는다
-    - 반복갯수는 대괄호안에 사용하며 ~로 나타낸다
-    - 맨처음 맨마지막등의 용어는 [처음], [끝]등의 이유로 나타낸다 
-    - 특수문자(re모듈내에 의미가있는 문자)는 \를 붙여서 사용한다
-    - 어떤문자의 앞과뒤에있을때는 (앞에있음:abc)이라고 사용하면 abc가 앞에있는 문자열을 찾는것이다
-
-### mailmail
-이름을 **mailmail**라고 지었으며, 아웃룩의 이메일을 관리하는 도구입니다
-- 이것의 장점은 엑셀이나 Util과 연동하여 편의성을 더욱 증대하고있읍니다
-- 기본적인 사용법이나 함수의 이름은 같은 형태를 따릅니다
+Metadata-Version: 2.1
+Name: xython
+Version: 1.5.0
+Summary: Easy Read / Write for Excel, Word, Color, Etc using Python
+Home-page: https://github.com/sjpark/xython
+Author: sjpark
+Author-email: sjpkorea@yahoo.com
+License: UNKNOWN
+Download-URL: https://github.com/sjpark/xython/archive/v1.5.0.tar.gz
+Platform: UNKNOWN
+Classifier: License :: OSI Approved :: MIT License
+Requires-Python: >=3.8
+Description-Content-Type: text/markdown
+
+## xython 모듈에 대하여
+### 개괄적인 설명
+이모듈은 업무용으로 많이 사용하는 엑셀 , 색, 정규표현식, 등에 대하여 Python과 win32com을 기본으로 사용하여 각기 새롭게 모듈을 만들어서 좀더 쉽고 편하게 사용하고 만들자는 것입니다
+자동화는 각자의 사용에 대한  
+
+만든 이유는 우리가 업무등을 하는 입장에서, 손으로 작업하기에는 양이 많고, 그렇다고
+계속 반복적으로 일어나는 일은 아니며, VBA등을 만들어서 사용하기에는 어렵고 힘든 부분에 대해서
+
+파이썬이라는 훌룡한 언어를 위용하여, 좀더 쉽고 간결하게 몇가지 기능만 배워도 20줄안으로 자신만의 코드를
+만들어 사용할수있는 기준을 만들기 위한 것입니다
+
+또한 보통 많이 사용하는 코드들은 첨부된 sample코드를 보시거나 저의 사이트에 와서 비슷한것을 다운 받은후
+변경해서 사용하시기를 추천 드립니다
+
+좀더 편한 업무의 일을 하기위한 것입니다
+
+### 구성은 
+
+    - pcell : 엑셀을 다루는 것
+    - pcell_event : 엑셀의 이벤트를 다루는것
+    - scolor : 색의 RGB값을 편하게 사용가능하도록 만든 것
+    - jfinder : 정규표현식을 좀더 편하게 사용하도록 만든 것
+    - anydb : sqlite와 pandas 를 좀더 쉽게 사용할수있도록 만든것
+    - ganada : 워드를 다루기위해 만든 것
+    - mailmail : outlook을 다루는것
+    - pyclick : 키보드와 마우스를 다루는 모듈
+    - pynal : 시간과 날짜를 다루는것
+    - youtil : 이러저런 문장이나 시간등을 변환하는데 도움이되는 것
+    - basic_data : halmoney패키지에서 사용되는 전반적인 공유 자료들을 저장하는 곳
+
+각 사용사용방법들에 대해서는 아래의 사이트를 참고하세요
+
+* https://cafe.naver.com/pycell
+* www.halmoney.com
+* www.xython.co.kr
+
+
+## 기본 사용법
+### pcell
+-각 메소드는 각각 별도의 내용으로 사용합니다
+
+Pcell의 모듈을 만들 때 나름대로 편하고 쉽게 이름을 만들려고 하였습니다. 기본적인 틀을 만들어 놓으니, 분명억지로 지어진 이름또한 있음을 시인합니다. 나름대로 생각하고 고심한끝에 만들어진 이름이오니 맘에 들지 않는 부분이 있이더라도 양해를 부탁드립니다
+
+물론, 지금의 이름이 최종이라고는 생각하지 않고 있습니다. 좋은 이름이라는것은 어떤 메소드가 들어가 있는지 잘 몰라도 거의 사용하는데 사람의 생각에서 쉽게 사용을 할수 있도록 만드는 것이라고 생각을 합니다
+
+아마 한 4~5번정오는 크게 이름을 변경한 것 같습니다. 만들어놓고 조금지나면 저스스로가 도데체 이것의 이름은 왜 이렇게 만들어놓은거야???라는 질문을 하는경우가 가끔있습니다. 이리바꾸고 저리바꾸어도 맘에 안드는구석이 아직 많습니다
+
+한사람의 이름이 인생에서 차지하는부분이 많듯이 제가만든것또한 그러하지만, 만약 맘에 안드시는 것이 있으시면 본인스스로가 바꾼어서 사용하셔도 됩니다
+
+단, 기존의것은 그대로 두시고 아래부분에 새로운 메소드를 추가하셔서 위의것을 그대로 사용하시면 될것입니다
+
+그래서 다음과 같은 원리를 이용해서 만들었으나, 조금은 틀린부분도 있지만…
+
+	1. 이름은 기본적으로 3부분으로 만들었으며 각부분은 언더바(_)로 연결했습니다
+	2. 읽을때는 read, 쓸때는 write, 삭제는 delete, 추가는insert등을 사용하였습니다
+	3. 두번째의 이름의 규칙은
+		관련된 부분에 따라 다른것을 사용하며 다음과 같은 것이 사용이 됩니다
+		거진 영역을 나타내는 부분으로 사용하였습니다
+		range, workbook, cell, line, column
+	4. 세번째 부분이 어떤 일을 할것인지를 알아보는 것입니다
+	5. 일반사항은 다음과 같습니다
+
+-	모든함수에는 sheet가 명시되어야 합니다
+-	값을 읽는것은 read로 시작하며
+-	값을 쓰는 것은 write로 시작합니다
+-	선을 긋는등의 그림은 dwg로 시작합니다
+-	하나의 자료가 아닌, 자료의 묶음은 Range를 사용한다
+-	두개의 문구사이에는 '_' 로 연결을 하였다 예) read_cell
+-	메소드는 모두 소문자를 사용함
+
+예를 들어, 어떤셀에 값을 입력하는 것은 write_value_in_cell라는 이름으로 구성하였습니다
+그리고 부가적으로 함수의 변수로 사용되는부분은 큰 것->작은것으로 만들었으며, 영역을 표시하는 부분은 모두 리스트를 기준으로 하나로 만들었습니다.
+
+그저, 그렇다는것을 이해바라며, 실질적으로 코드를 보시면 더 쉽게 이해가 가실것으로 생각됩니다.
+보지않고 찾지않아도 함수의 이름을 생각해낼수있도록 만든다고 나름대로 정의한 것입니다.
+
+### scolor
+이것은 모든 외부로 들어오고 나가는 것은 전부 RGB형태로 이루어지도록 만든다
+
+    - 색을 변경하고 관리하는 모듈이며
+    - 색의 변화를 잘 사용이 가능하도록 하기위한 것이다
+    - 기본 입력 예 : "빨강", "빨강55", "red55", "0155"
+    - 기본색 ==> 12색 + (하양, 검정, 회색),
+    - 큰변화 ==> 1~9단계, 작은변화 ==> 1~9단계
+    - 기본함수 : get_color_rgb("red55"), get_rgb_3input(색, 큰변화, 작은변화)
+    - 모든 색의 표현이나 결과는 rgb로 돌려준다
+
+### Jfinder
+이름을 **Jfinder**라고 지었으며, 아래와 같은 특성을 가지고 있다
+
+1. 건수는 ~를 사용하여 4~5라는 식으로 표현을 하였고
+2. 한글, 영어와 같은 것은 대괄호를 사용하여 적용하였다 [한글]
+3. 처음과 끝은 [처음], [끝]처럼 나타냈다
+4. 그리고 이것은 누가 보아도 아~~ 무엇을 찾을려고 했는지를 알수있도록 하기위한것이며
+5. 찾기기능중에 전부 찾아서 보기쉽도록 돌려주는 것과 같은 몇가지 메소드들을 만들어 넣었읍니다
+제일 중요한 코드를 만드는 기능은 아래와 같읍니다
+대략적으로 위의것을 읽은후에 보시면 이해가 되실부분이 많읍니다
+
+* 아래의 코드들은 정규표현식을 사용하면서, 내가 만든 표현식조차도 다시 읽기가 어려워서, 나름 다른 형태로 만들어 본것인데. 생각보다 가독성이 좋아서 같이 공유해보는것이다
+또한 만든김에 결과로 돌려주는것도 하나만 받으면 전부 가능하도록 만들어 보았다
+위에서 언급한 이메일 형식이 맞느지를 보는 것은 상당히 반복적이기 때문에 크게 혼돈은 없다
+하지만, 실제 코드를 사용하다 보면, 외계어를 해석하는 상태까지 와야할 경우가 있다
+
+
+    ([a-zA-Z0-9_.+-]+)@[a-zA-Z0-9_.+-]+\.[a-zA-Z0-9_.+-]+
+
+* 이정도만해도 간단한 축에 속한다. 맨처음 만들때는 그나마 이해를 하지만, 다른사람이 만든 것을 이해하는데 상당한 시간이 걸린다는 것이고, 또한 일반적인 사용자들이 이것을 공부하고 이해하는데 어려움이 잇을 것 같으면서 동시에, 정규표현식의 강력함을 사용할수 있도록 생각해 보는 것이다
+그래서 좀더 간단하게 사용법을 만들고,
+
+
+    [영어&숫자.+-:1~]@[영어&숫자.+-:1~]\.[영어&숫자.+-:1~]
+이렇게 바꾸면 좀더 읽기가 쉬워진다
+
+**jfinder**에는 자주사용하는 언어를 등록할수도 있읍니다. 예를 들어 일본어나 한자를 등록한것처럼 하면 사용이 가능하다.
+간단하게 다시 사용하는 방법을 알려주면, 너무 줄여놓은 정규표현식을 좀더 늘이는 것이라고 생각하면 됩니다. 여기에서 느낀 부분은 전문가가 사용하기에는 좋지만, 비전문가가 사용하기 쉽게, 예전에는 단어1개가 아주 중요한 속도까지 영향을 주지만, 지금은너무 줄이지 않아도 된다는 것이다. 기계에 가까운 언어에서 좀더 사용자에 가까운 언어로 만들어도 된다는 것이지요
+파이선이 사용하기에 좀더 편한방법이 되는 것이지요
+
+    - 대괄호로 묶는다
+    - 반복갯수는 대괄호안에 사용하며 ~로 나타낸다
+    - 맨처음 맨마지막등의 용어는 [처음], [끝]등의 이유로 나타낸다 
+    - 특수문자(re모듈내에 의미가있는 문자)는 \를 붙여서 사용한다
+    - 어떤문자의 앞과뒤에있을때는 (앞에있음:abc)이라고 사용하면 abc가 앞에있는 문자열을 찾는것이다
+
+### mailmail
+이름을 **mailmail**라고 지었으며, 아웃룩의 이메일을 관리하는 도구입니다
+- 이것의 장점은 엑셀이나 Util과 연동하여 편의성을 더욱 증대하고있읍니다
+- 기본적인 사용법이나 함수의 이름은 같은 형태를 따릅니다
+
```

### Comparing `xython-1.4.0/setup.py` & `xython-1.5.0/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 # -*- coding: utf-8 -*-
 from setuptools import setup, find_packages
 with open("README.md", "rt", encoding='UTF8') as fh:
     long_description = fh.read()
 setup(
     name='xython',
-    version='1.4.0',
+    version='1.5.0',
     url='https://github.com/sjpark/xython',
-    download_url='https://github.com/sjpark/xython/archive/v1.4.0.tar.gz',
+    download_url='https://github.com/sjpark/xython/archive/v1.5.0.tar.gz',
     author='sjpark',
     author_email='sjpkorea@yahoo.com',
     description='Easy Read / Write for Excel, Word, Color, Etc using Python',
     packages=find_packages("src"),
     package_dir={"": "src"},
     include_package_data=True,
     package_data={
```

### Comparing `xython-1.4.0/src/xython/anydb.py` & `xython-1.5.0/src/xython/anydb.py`

 * *Files 5% similar despite different names*

```diff
@@ -23,29 +23,31 @@
 
 		self.con = ""  # sqlite db에 연결되는 것
 		if db_name =="":
 			pass
 		else:
 			self.con = sqlite3.connect(db_name, isolation_level=None)
 			self.cursor = self.con.cursor()
-		self.make_connection_with_sqlite_db(self.db_name)
+		self.connect_sqlite_db(self.db_name)
 		self.base_data = basic_data.basic_data()
 		self.var = self.base_data.vars
 		self.var_common={}
 
 
 	def append_df1_df2(self, df_obj_1, df_obj_2):
 		"""
 		dataframe끝에 dataframe형태의 자료를 추가하는것
 		"""
 		result = pd.concat([df_obj_1, df_obj_2])
 		return result
 
 	def change_df_to_dic(self, input_df, style="split"):
 		"""
+		dic의 형태중에서 여러가지중에 하나를 선택해야 한다
+
 		입력형태 : data = {"calory": [123, 456, 789], "기간": [10, 40, 20]}
 		출력형태 : dataframe
 		dict :    {'제목1': {'가로제목1': 1, '가로제목2': 3}, '제목2': {'가로제목1': 2, '가로제목2': 4}}
 		list :    {'제목1': [1, 2], '제목2': [3, 4]}
 		series :  {열 : Series, 열 : Series}
 		split :   {'index': ['가로제목1', '가로제목2'], 'columns': ['제목1', '제목2'], 'data': [[1, 2], [3, 4]]}
 		records : [{'제목1': 1, '제목2': 2}, {'제목1': 3, '제목2': 4}]
@@ -56,33 +58,34 @@
 			checked_style = "split"
 		result = input_df.to_dict(checked_style)
 		return result
 
 	def change_df_to_list(self, df_obj):
 		"""
 		df자료를 커럼과 값을 기준으로 나누어서 결과를 리스트로 돌려주는 것이다
+		결과 : [[컬럼리스트], [자료1], [자료2]....]
 		"""
 		col_list = df_obj.columns.values.tolist()
 		value_list = df_obj.values.tolist()
-		col_list.extend(value_list)
-		return col_list
+		result = [col_list, value_list]
+		return result
 
 	def change_dic_to_list_as_col_value_style(self, dic_data):
 		"""
 		사전의 자료를 sql에 입력이 가능한 형식으로 만드는 것
 		결과 : [[컬럼리스트], [자료1], [자료2]....]
 		"""
 		col_list = list(dic_data[0].keys())
 		value_list =[]
 		for one_col in col_list:
 			value_list.append(dic_data[one_col])
 		result = [col_list, value_list]
 		return result
 
-	def change_list2d_to_df(self, col_list="", list2d=""):
+	def change_list_to_df(self, col_list="", list2d=""):
 		"""
 		리스트 자료를 dataframe로 만드는것
 		입력형태 : 제목리스트, 2차원 값리스트형
 		출력형태 : dataframe로 바꾼것
 		"""
 		checked_list2d = self.yt.change_list1d_to_list2d(list2d)
 		# 컬럼의 이름이 없거나하면 기본적인 이름을 만드는 것이다
@@ -115,15 +118,15 @@
 			cols.append(column[0])
 		temp = []
 		for one in sql_result.fetchall():
 			temp.append(list(one))
 		result = [cols, temp]
 		return result
 
-	def change_table_name_in_sqlite_db(self, table_name_old, table_name_new, db_name=""):
+	def change_table_name_in_sqlite(self, table_name_old, table_name_new, db_name=""):
 		"""
 		테이블 이름을 변경
 		"""
 		self.check_cursor(db_name)
 		sql_sentence = "alter table %s rename to %s" % (table_name_old, table_name_new)
 		self.cursor.execute(sql_sentence)
 
@@ -137,15 +140,15 @@
 
 	def check_col_name_all_in_sqlite(self, table_name, db_name =""):
 		"""
 		현재 있는 테이블의 이름에 특수문자들을 지우는 것이다
 		공백을 _로 변경하는것, Column의 이름을 변경한다
 		"""
 		self.check_cursor(db_name)
-		all_col_names = self.read_col_name_all_in_sqlite(db_name, table_name)
+		all_col_names = self.get_y_name_all_in_sqlite(db_name, table_name)
 		for col_name in all_col_names:
 			col_name_new = self.check_col_name(col_name)
 			if not col_name_new == col_name:
 				self.cursor.execute("alter table {} RENAME COLUMN {} to {}".format(table_name, col_name, col_name_new))
 
 	def check_cursor(self, db_name=""):
 		if db_name =="":
@@ -199,42 +202,90 @@
 				temp_1 = []
 				for item in changed_one:
 					temp_1.append(int(item))
 				one = temp_1
 			temp.append(one)
 		return temp
 
-	def delete_column_in_sqlite(self, table_name, col_name_list, db_name=""):
+
+	def insert_yline_in_list_db(self, input_list_db, input_yname, input_yline_data):
+		input_list_db[0].append(input_yname)
+		input_list_db[1].append(input_yline_data)
+		return input_list_db
+
+	def insert_yline_in_list_db_by_index(self, input_list_db, input_yname, input_yline_data, input_index):
+		input_list_db[0].insert(input_index, input_yname)
+		input_list_db[1].insert(input_index, input_yline_data)
+		return input_list_db
+
+	def delete_yline_in_list_db_by_index(self, input_list_db, input_index_list=[1,2,3]):
+		"""
+		index번호를 기준으로 y라인을 삭제하는것
+		list_db의 형태 : [[y_name-1, y_name_2.....],[[a1, a2, a3...], [b1, b2, b3...], ]]
+		"""
+		#맨뒤부터 삭제가 되어야 index가 유지 된다
+		checked_input_index_list = input_index_list.reverse()
+
+		for index in checked_input_index_list:
+			#y열의 제목을 지우는것
+			input_list_db[0].pop(index)
+
+			#각 항목의 값을 지우는것
+			for num in range(len(input_list_db[1])):
+				input_list_db[1][num].pop(index)
+		return input_list_db
+
+	def delete_yline_in_list_db_by_name(self, input_list_db, input_name_list=["y_name_1, y_name_2"]):
+		"""
+		y라인 이름을 기준으로 삭제하는것
+		list_db의 형태 : [[y_name-1, y_name_2.....],[[a1, a2, a3...], [b1, b2, b3...], ]]
+		"""
+
+		title_dic = {}
+		for index in range(len(input_list_db[0])):
+			title_dic[input_list_db[0][index]] = index
+
+		input_index_list = []
+
+		for name in input_name_list:
+			index = title_dic[name]
+			input_index_list.append(index)
+
+		# 맨뒤부터 삭제가 되어야 index가 유지 된다
+		result = self.delete_yline_in_list_db_by_index(input_list_db, input_index_list)
+		return result
+
+	def delete_yline_in_sqlite(self, db_name, table_name, col_name_list):
 		"""
 		컬럼 삭제
 		입력형태 : ["col_1","col_2","col_3"]
 		"""
 		self.check_cursor(db_name)
 		if col_name_list:
 			for col_name in col_name_list:
 				sql = ("ALTER TABLE %s DROP COLUMN %s " % (table_name, col_name))
 				self.cursor.execute(sql)
 
-	def delete_empty_column_in_df(self, input_df):
+	def delete_empty_yline_in_df(self, input_df):
 		"""
 		dataframe의 빈열을 삭제
 		제목이 있는 경우에만 해야 문제가 없을것이다
 		"""
 		nan_value = float("NaN")
 		input_df.replace(0, nan_value, inplace=True)
 		input_df.replace("", nan_value, inplace=True)
 		input_df.dropna(how="all", axis=1, inplace=True)
 		return input_df
 
-	def delete_empty_column_in_sqlite(self, table_name, db_name=""):
+	def delete_empty_yline_in_sqlite(self, table_name, db_name=""):
 		"""
 		테이블의 컬럼중에서 아무런 값도 없는 컬럼을 삭제한다
 		"""
 		self.check_cursor(db_name)
-		col_name_all = self.read_col_name_all_in_sqlite(db_name, table_name)
+		col_name_all = self.get_y_name_all_in_sqlite(db_name, table_name)
 
 		for col_name in col_name_all:
 			sql = ("select COUNT(*) from %s where %s is not null" % (table_name, col_name))
 			self.cursor.execute(sql)
 			if self.cursor.fetchall()[0][0] == 0:
 				#입력값이 없으면 0개이고, 그러면 삭제를 하는 것이다
 				sql = ("ALTER TABLE %s DROP COLUMN %s " % (table_name, col_name))
@@ -243,15 +294,15 @@
 	def delete_sqlite(self, table_name, db_name=""):
 		"""
 		입력형태 : 테이블이름
 		"""
 		self.check_cursor(db_name)
 		self.cursor.execute("DROP TABLE " + table_name)
 
-	def insert_cols_in_sqlite(self, table_name, col_data_list_s, db_name=""):
+	def insert_yyline_in_sqlite_by_name(self, table_name, col_data_list_s, db_name=""):
 		"""
 		새로운 컬럼을 만든다
 		col_data_list_s : [["이름1","int"],["이름2","text"]]
 		["이름2",""] => ["이름2","text"]
 		"""
 		self.check_cursor(db_name)
 		for one_list in col_data_list_s:
@@ -259,15 +310,15 @@
 				col_name = self.check_col_name(one_list[0])
 				col_type = one_list[1]
 			else:
 				col_name = self.check_col_name(one_list)
 				col_type = "text"
 			self.cursor.execute("alter table %s add column '%s' '%s'" % (table_name, col_name, col_type))
 
-	def make_connection_with_sqlite_db(self, db_name=""):
+	def connect_sqlite_db(self, db_name=""):
 		"""
 		기본적으로 test_db.db를 만든다
 		memory로 쓰면, sqlite3를 메모리에 넣도록 한다
 		"""
 		if db_name == "memory":
 			self.con = sqlite3.connect(":memory:")
 		elif db_name == "" or db_name == "test": # 데이터베이스를 넣으면 화일로 만든다
@@ -291,31 +342,31 @@
 		elif self.db_name == "" or self.db_name == "test":
 			self.db_name = "test_db.db"
 			self.con = sqlite3.connect(self.db_name, isolation_level=None)
 		else:
 			self.con = sqlite3.connect(self.db_name, isolation_level=None)
 		self.cursor = self.con.cursor()
 
-	def make_insert_sql_by_col_names(self, table_name, col_list):
+	def make_sql_text_for_insert_by_col_names(self, table_name, col_list):
 		sql_columns = self.yt.change_list1d_to_text_with_chainword(col_list, ", ")
 		sql_values = "?," * len(col_list)
 		result = "insert into %s (%s) values (%s)" % (table_name, sql_columns, sql_values[:-1])
 		return result
 
-	def make_memory_db_for_sqlite(self):
+	def new_sqlite_with_memory_db(self):
 		self.con = sqlite3.connect(":memory:")
 
-	def make_new_sqlite_db(self, db_name=""):
+	def new_sqlite_db(self, db_name=""):
 		"""
 		새로운 데이터베이스를 만든다
 		입력형태 : 이름
 		"""
-		self.make_connection_with_sqlite_db(db_name)
+		self.connect_sqlite_db(db_name)
 
-	def make_new_sqlite_with_column(self, table_name, column_data_list, db_name=""):
+	def new_sqlite_with_column(self, table_name, column_data_list, db_name=""):
 		"""
 		어떤 형태의 자료가 입력이 되어도 테이블을 만드는 sql을 만드는 것이다
 		입력형태 1 : 테이블이름, [['번호1',"text"], ['번호2',"text"],['번호3',"text"],['번호4',"text"]]
 		입력형태 2 : 테이블이름, ['번호1','번호2','번호3','번호4']
 		입력형태 3 : 테이블이름, [['번호1',"text"], '번호2','번호3','번호4']
 		"""
 		self.check_cursor(db_name)
@@ -333,28 +384,28 @@
 				col_name = one_list
 				col_type = "text"
 			sql_2 = sql_2 + "{} {}, ".format(col_name, col_type)
 		sql_2 = sql_2[:-2] + ")"
 		self.cursor.execute(sql_2)
 		return sql_2
 
-	def make_new_table_in_sqlite_db(self, table_name, db_name=""):
+	def new_table_in_sqlite_db(self, table_name, db_name=""):
 		"""
 		새로운 테이블을 만든다
 		입력형태 : 테이블이름
 		"""
 		self.check_cursor(db_name)
 		#현재 db안의 테이블에 같은 이름이 없는지 확인 하는 것
 		tables = []
 		self.cursor.execute("select name from sqlite_master where type = 'table'; ")
 		all_table_name = self.cursor.fetchall()
 		if not table_name in all_table_name:
 			self.cursor.execute("CREATE TABLE " + table_name + " (Item text)")
 
-	def make_sqlite_db_in_memory(self):
+	def new_sqlite_in_memory(self):
 		"""
 		self.cursor.execute("CREATE TABLE " + self.table_name + " (auto_no integer primary key AUTOINCREMENT)")
 		memory에 생성하는 것은 바로 connection 이 만들어 진다
 		"""
 		self.con = sqlite3.connect(":memory:")
 
 	def manual(self):
@@ -381,61 +432,61 @@
 		df.iloc[where_i, whe	re_j] Select both rows and columns by integer position
 		df.at[label_i, label	_j] Select a single scalar value by row and column label
 		df.iat[i, j]	Select a single scalar value by row and column position (integers)
 		get_value(), set_val	ue() Select single value by row and column label
 		"""
 		return result
 
-	def read_col_name_all_in_sqlite(self, table_name, db_name=""):
+	def get_y_name_all_in_sqlite(self, table_name, db_name=""):
 		"""
 		해당하는 테이의 컬럼구조를 갖고온다
 		입력형태 : 테이블이름
 		출력형태 : 컬럼이름들
 		"""
 		self.check_cursor(db_name)
 		self.cursor.execute("PRAGMA table_info('%s')" % table_name)
 		sql_result =self.cursor.fetchall()
 		result = []
 		for one_list in sql_result:
 			result.append(one_list[1])
 		return result
 
-	def read_col_property_all_in_sqlite(self, table_name, db_name=""):
+	def get_property_for_y_line_all_in_sqlite(self, table_name, db_name=""):
 		"""
 		해당하는 테이블의 컬럼의 모든 구조를 갖고온다
 		"""
 
 		self.check_cursor(db_name)
 		self.cursor.execute("PRAGMA table_info('%s')" % table_name)
 		result = []
 		for temp_2 in self.cursor.fetchall():
 			result.append(temp_2)
 		return result
 
-	def read_columns_data_from_no1_to_no2_in_sqlite(self, table_name, offset=0, row_count=100, db_name=""):
+	def get_columns_data_from_no1_to_no2_in_sqlite(self, table_name, offset=0, row_count=100, db_name=""):
 		"""
 		테이블의 자료중 원하는 갯수만 읽어오는 것
 		"""
 		self.check_cursor(db_name)
 		self.cursor.execute(("select * from %s LIMIT %s, %s;") % (table_name, str(offset), str(row_count)))
 		result = self.cursor.fetchall()
 		return result
 
-	def read_db_name_all_in_path(self, path=".\\"):
+	def get_db_name_all_in_path(self, path=".\\"):
 		"""
 		모든 database의 이름을 갖고온다
 		모든이 붙은것은 맨뒤에 all을 붙인다
 		"""
 		result = []
 		for fname in os.listdir(path):
 			if fname[-3:] == ".db":
 				result.append(fname)
 		return result
 
-	def read_df_by_name(self, df_obj, x, y):
+	def read_value_in_df_by_name(self, df_obj, x, y):
 		"""
 		열이나 행의 이름으로 pandas의 dataframe의 일부를 불러오는 것이다
 		이것은 리스트를 기본으로 사용한다
 		list_x=["가"~"다"] ===> "가"~"다"열
 		list_x=["가","나","다","4"] ===> 가,나,다, 4 열
 		x=""또는 "all" ===> 전부
 		"""
@@ -454,30 +505,30 @@
 				changed_one = one
 			temp.append(changed_one)
 		# 이것중에 self를 사용하지 않으면 오류가 발생한다
 		print(temp)
 		exec("self.result = df_obj.loc[{}, {}]".format(temp[0], temp[1]))
 		return self.result
 
-	def read_df_by_no(self, df_obj, x, y):
+	def read_value_in_df_by_no(self, df_obj, x, y):
 		"""
 		숫자번호로 pandas의 dataframe의 일부를 불러오는 것
 		단, 모든것을 문자로 넣어주어야 한다
 		x=["1:2", "1~2"] ===> 1, 2열
 		x=["1,2,3,4"] ===> 1,2,3,4열
 		x=[1,2,3,4]  ===> 1,2,3,4열
 		x=""또는 "all" ===> 전부
 		"""
 
 		x_list = self.check_df_range(x)
 		y_list = self.check_df_range(y)
 		exec("self.result = df_obj.iloc[{}, {}]".format(x_list, y_list))
 		return self.result
 
-	def read_df_by_xy(self, df_obj, xy=[0, 0]):
+	def read_value_in_df_by_xy(self, df_obj, xy=[0, 0]):
 		"""
 		위치를 기준으로 값을 읽어오는 것이다
 		숫자를 넣으면 된다
 		"""
 		result = df_obj.iat[int(xy[0]), int(xy[1])]
 		return result
 
@@ -627,29 +678,29 @@
 	def write_dic_to_sqlite(self, table_name, dic_data, db_name=""):
 		"""
 		사전의 키를 y이름으로 해서 값을 입력한다
 		"""
 		self.check_cursor(db_name)
 
 		for one_col in list(dic_data[0].keys()):
-			if not one_col in self.read_col_name_all_in_sqlite(table_name):
-				self.insert_cols_in_sqlite(table_name, [one_col])
+			if not one_col in self.get_y_name_all_in_sqlite(table_name):
+				self.insert_yyline_in_sqlite_by_name(table_name, [one_col])
 
-		sql = self.make_insert_sql_by_col_names(table_name, list(dic_data[0].keys()))
+		sql = self.make_sql_text_for_insert_by_col_names(table_name, list(dic_data[0].keys()))
 		value_list = []
 		for one_dic in dic_data:
 			value_list.append(list(one_dic.values()))
 		self.cursor.executemany(sql, value_list)
 
 	def write_list_to_sqlite(self, table_name, col_name_s, list_values, db_name=""):
 		"""
 		리스트의 형태로 넘어오는것중에 y이름과 값을 분리해서 얻는 것이다
 		"""
 		self.check_cursor(db_name)
-		sql = self.make_insert_sql_by_col_names(table_name, col_name_s)
+		sql = self.make_sql_text_for_insert_by_col_names(table_name, col_name_s)
 		self.cursor.executemany(sql, list_values)
 
 	def write_sqlite_data_all_to_df(self, table_name, db_name=""):
 		"""
 		sqlite를 df로 만드는것
 		"""
 		self.check_cursor(db_name)
@@ -668,8 +719,23 @@
 		if xy[1] > y_max:
 			for no in range(y_max, xy[1]):
 				df[len(df.columns)] = np.NaN
 		if xy[0] > x_max:
 			data_set = [(lambda x: np.NaN)(a) for a in range(len(df.columns))]
 			for no in range(xy[0] - x_max):
 				df.loc[len(df.index)] = data_set
-		df.iat[int(xy[0]), int(xy[1])] = value
+		df.iat[int(xy[0]), int(xy[1])] = value
+
+	def is_col_names(self, input_list):
+		# anydb것
+		# 입력으로 들어온 1 차원 리스트자료가 컬럼이듬으로 사용되는것인지 아닌지 확인하는것
+		result = 1
+		result_empty = 0
+		result_date_int = 0
+		for one_value in input_list:
+			if one_value == None or one_value == "":
+				result_empty = result_empty + 1
+			if type(one_value) == type(1):
+				result_date_int = result_date_int + 1
+			if result_empty > 0 or result_date_int > 0:
+				result = 0
+		return result
```

### Comparing `xython-1.4.0/src/xython/basic_data.py` & `xython-1.5.0/src/xython/basic_data.py`

 * *Files 3% similar despite different names*

```diff
@@ -437,15 +437,15 @@
 
 		self.vars["list_colormode_kor"]= self.vars["list_colormode_kor"]= ["단색조합", "등간격 3색 조화", "보색", "인접색", "근접보색조합",
 							   "고명도배색", "고명도배색+약간더 부드러운 이미지",
 							   "중명도배색", "중명도배색+약간더 부드러운 이미지", "저중명도배색", "저명도배색+약간더 어두운 이미지",
 							   "명도차가 큰 배색", "명도차가 큰 배색 + 근접보색",
 							   "고채도 배색", "채도차가 큰 배색", "저채도 배색", ]
 
-		self.vars["list_엑셀_56가지_rgb값"] = [[0, 0, 0], [255, 255, 255], [255, 0, 0], [0, 255, 0], [0, 0, 255], [255, 255, 0],
+		self.vars["list_엑셀_56가지_rgb값"] =self.vars["rgb_56_for_excel"] = [[0, 0, 0], [255, 255, 255], [255, 0, 0], [0, 255, 0], [0, 0, 255], [255, 255, 0],
 										[255, 0, 255], [0, 255, 255], [128, 0, 0], [0, 128, 0], [0, 0, 128], [128, 128, 0],
 										[128, 0, 128], [0, 128, 128], [192, 192, 192], [128, 128, 128], [153, 153, 255],
 										[153, 51, 102], [255, 255, 204], [204, 255, 255], [102, 0, 102], [255, 128, 128],
 										[0, 102, 204], [204, 204, 255], [0, 0, 128], [255, 0, 255], [255, 255, 0],
 										[0, 255, 255], [128, 0, 128], [128, 0, 0], [0, 128, 128], [0, 0, 255],
 										[0, 204, 255], [204, 255, 255], [204, 255, 204], [255, 255, 153], [153, 204, 255],
 										[255, 153, 204], [204, 153, 255], [255, 204, 153], [51, 102, 255], [51, 204, 204],
@@ -1119,14 +1119,60 @@
 			31: [0, 128, 128], 32: [0, 0, 255], 33: [0, 204, 255], 34: [204, 255, 255], 35: [204, 255, 204],
 			36: [255, 255, 153], 37: [153, 204, 255], 38: [255, 153, 204], 39: [204, 153, 255], 40: [255, 204, 153],
 			41: [51, 102, 255], 42: [51, 204, 204], 43: [153, 204, 0], 44: [255, 204, 0], 45: [255, 153, 0],
 			46: [255, 102, 0], 47: [102, 102, 153], 48: [150, 150, 150], 49: [0, 51, 102], 50: [51, 153, 102],
 			51: [0, 51, 0], 52: [51, 51, 0], 53: [153, 51, 0], 54: [153, 51, 102], 55: [51, 51, 153],
 			56: [51, 51, 51], }
 
+	def pandas_1(self):
+		"""
+		가끔 코딩을 해보니, 테스트용데이터가 필요하더라구요
+		입력형태 :
+		출력형태 :
+		"""
+		dic_data = {
+			"1번째열": {'Country': 'Russia', 'Capital': 'Moscow', 'Area(Sq.Miles)': 6601670, 'Population': 146171015},
+			"2번째열": {'Country': 'Canada', 'Capital': 'Ottawa', 'Area(Sq.Miles)': 3855100, 'Population': 38048738},
+			"3번째열": {'Country': 'China', 'Capital': 'Beijing', 'Area(Sq.Miles)': 3705407, 'Population': 1400050000},
+			"4번째열": {'Country': 'United States of America', 'Capital': 'Washington, D.C.',
+			         'Area(Sq.Miles)': 3796742, 'Population': 331449281},
+			"5번째열": {'Country': 'Brazil', 'Capital': 'Brasília', 'Area(Sq.Miles)': 3287956,
+			         'Population': 210147125},
+			"6번째열": {'Country': 'Russia', 'Capital': 'Moscow', 'Area(Sq.Miles)': 6601670, 'Population': 146171015},
+			"7번째열": {'Country': 'Canada', 'Capital': 'Ottawa', 'Area(Sq.Miles)': 3855100, 'Population': 38048738},
+			"8번째열": {'Country': 'China', 'Capital': 'Beijing', 'Area(Sq.Miles)': 3705407, 'Population': 1400050000},
+			"9번째열": {'Country': 'United States of America', 'Capital': 'Washington, D.C.',
+			         'Area(Sq.Miles)': 3796742, 'Population': 331449281},
+			"10번째열": {'Country': 'Brazil', 'Capital': 'Brasília', 'Area(Sq.Miles)': 3287956,
+			          'Population': 210147125}
+			}
+		return dic_data
+
+	def pandas_2(self):
+		"""
+		가끔 코딩을 해보니, 테스트용데이터가 필요하더라구요
+		간단하게 바꿔봄
+		입력형태 :
+		출력형태 :
+		"""
+		dic_data = {
+			"1번째열": {'A1': '러시아', 'Capital': 'Moscow', '면적': 6601670, '인구': 146171015},
+			"2번째열": {'A1': '카나다', 'Capital': 'Ottawa', '면적': 3855100, '인구': 38048738},
+			"3번째열": {'A1': '중국', 'Capital': 'Beijing', '면적': 3705407, '인구': 1400050000},
+			"4번째열": {'A1': '미국', 'Capital': 'Washington', '면적': 3796742, '인구': 331449281},
+			"5번째열": {'A1': '브라질', 'Capital': 'Brasília', '면적': 3287956, '인구': 210147125},
+			"6번째열": {'A1': '러시아', 'Capital': 'Moscow', '면적': 6601670, '인구': 146171015},
+			"7번째열": {'A1': '카나다', 'Capital': 'Ottawa', '면적': 3855100, '인구': 38048738},
+			"8번째열": {'A1': '중국', 'Capital': 'Beijing', '면적': 3705407, '인구': 1400050000},
+			"9번째열": {'A1': '미국', 'Capital': 'Washington', '면적': 3796742, '인구': 331449281},
+			"10번째열": {'A1': '브라질', 'Capital': 'Brasília', '면적': 3287956, '인구': 210147125}
+		}
+		return dic_data
+
+
 
 
 	test_datas["sample_4"] = [
 			"20230301",
 			'02/28/2023 02:30 PM',
 			'180919 015519',
 			'18/09/19 01:55:19',
```

### Comparing `xython-1.4.0/src/xython/ganada.py` & `xython-1.5.0/src/xython/ganada.py`

 * *Files identical despite different names*

### Comparing `xython-1.4.0/src/xython/jfinder.py` & `xython-1.5.0/src/xython/jfinder.py`

 * *Files identical despite different names*

### Comparing `xython-1.4.0/src/xython/mailmail.py` & `xython-1.5.0/src/xython/mailmail.py`

 * *Files 0% similar despite different names*

```diff
@@ -592,8 +592,14 @@
     def make_new_mail_for_draft_folder(self, **dic):
         # 빈 임시보관함으로 보내는 메일객체를 하나 만든것
         promise_folder = self.outlook.GetDefaultFolder(16)
         new_mail = self.base_mail.CreateItem(0)
         new_mail.To = dic["to"]
         new_mail.Subject = dic["subject"]
         new_mail.HTMubody = dic["body"]
-        new_mail.Move(promise_folder)
+        new_mail.Move(promise_folder)
+    
+    def get_selected_mails(self):
+        #아웃룩에서 어떤때를 보면, 선택한 자료를 확인할 필요가 있다
+        #이럴때 사용하기 힘든 것이다
+        result = self.base_mail.ActiveExploer().Selection
+        return result
```

### Comparing `xython-1.4.0/src/xython/pcell.py` & `xython-1.5.0/src/xython/pcell.py`

 * *Files 1% similar despite different names*

```diff
@@ -18,24 +18,24 @@
 	"""
 	엑셀을 컨트롤 할수있는 모듈
 	"""
 	def __init__(self, filename=""):
 		#공통으로 사용할 변수들을 설정하는 것
 		self.color = scolor.scolor()
 		self.base_data = basic_data.basic_data()
-		self.var = self.base_data.vars
-		self.var_common={}
+		self.var_p = self.base_data.vars #package안에서 공통적으로 사용되는 변수들
+		self.var_l={} #이 클래스안에서만 사용되는 local 변수들
 		# 만약 화일의 경로가 있으면 그 화일을 열도록 한다
 		self.xlapp = win32com.client.dynamic.Dispatch('Excel.Application')
 		self.xlapp.Visible = 1
 
 		if filename != None:
-			self.filename = filename.lower()
+			self.filename = str(filename).lower()
 
-		if self.filename == 'activeworkbook' or self.filename == '':
+		if self.filename == 'activeworkbook' or not self.filename:
 			# activeworkbook으로 된경우는 현재 활성화된 workbook을 그대로 사용한다
 			self.xlbook = self.xlapp.ActiveWorkbook
 			if self.xlbook == None:
 				# 만약 activework북을 부르면서도 화일이 존재하지 않으면 새로운 workbook을 만드는 것
 				try:
 					self.xlapp.WindowState = -4137
 					self.xlbook = self.xlapp.WorkBooks.Add()
@@ -49,19 +49,17 @@
 			# 만약 화일 이름이 따로 주어 지면 그 화일을 연다
 			try:
 				self.xlapp.WindowState = -4137
 				self.xlbook = self.xlapp.Workbooks.Open(self.filename)
 			except:
 				win32gui.MessageBox(0, "Please check file path", "xxw.halmoney.com", 0)
 
-	def check_basic_input_datas(self, sheet_name, xyxy):
-		if self.var["repeat_start"] and not self.var["repeat_end"] :
-			self.var["sheet_obj"] = self.check_sheet_name(sheet_name)
-			self.var["xyxy"] = self.check_address_value(xyxy)
-			self.var["my_range"] = self.var["sheet_obj"].Range(self.var["sheet_obj"].Cells(self.var["xyxy"][0], self.var["xyxy"][1]), self.var["sheet_obj"].Cells(self.var["xyxy"][2], self.var["xyxy"][3]))
+	def write_message_in_statusbar(self, input_text="test"):
+		self.xlapp.StatusBar = input_text
+
 
 	def add_button_with_macro(self, sheet_name="", xyxy="", macro_code="", title=""):
 		"""
 		매크로랑 연결된 버튼을 만드는것
 		버튼을 만들어서 그 버튼에 매크로를 연결하는 것이다
 		매크로와 같은것을 특정한 버튼에 연결하여 만드는것을 보여주기위한 것이다
 		Add(왼쪽의 Pixel, 위쪽 Pixce, 넓이, 높이)
@@ -74,27 +72,29 @@
 		new_btn.Add(left_px, top_px, width_px, height_px)
 		new_btn.OnAction = macro_code
 		new_btn.Text = title
 
 	def add_picture_in_sheet(self, sheet_name, file_path, xywh, link=0, image_in_file=1):
 		self.insert_picture_in_sheet(sheet_name, file_path, xywh, link=0, image_in_file=1)
 
-	def add_picture_in_sheet_by_pixcel(self, file_path, pxpywh, link=0, image_in_file=1):
-		vars["sheet"].Shapes.AddPicture(file_path, link, image_in_file, pxpywh[0], pxpywh[1], pxpywh[2], pxpywh[3])
+	def add_picture_in_sheet_by_pixel(self, sheet_name, file_path, pxpywh, link=0, image_in_file=1):
+		sheet_object = self.check_sheet_name(sheet_name)
+		sheet_object.Shapes.AddPicture(file_path, link, image_in_file, pxpywh[0], pxpywh[1], pxpywh[2], pxpywh[3])
 
-	def add_shape(self, sheet_name, shape_no=35, xywh=""):
+	def add_shape_by_xywh(self, sheet_name, shape_no=35, xywh=""):
+		# ??????
 		# shape_no : 엑셀에서 정의한 도형의 번호
 		# xywh : 왼쪽윗부분의 위치에서 너비와 높이
 		sheet_object = self.check_sheet_name(sheet_name)
 
 		#도형이 숫자이면 그대로, 문자이면 기본자료에서 찾도록 한다
 		if type(shape_no) == type(123):
 			pass
-		elif shape_no in list(self.var["shape_enum"].keys()):
-			shape_no = self.var["shape_enum"][shape_no]
+		elif shape_no in list(self.var_p["shape_enum"].keys()):
+			shape_no = self.var_p["shape_enum"][shape_no]
 
 		sheet_object.Shapes.Addshape(shape_no, xywh[0], xywh[1], xywh[2], xywh[3])
 
 	def add_sheet_new(self):
 		"""
 		시트하나 추가하기
 		위치는 자동으로 제일 뒤에 추가되는것이며, 시트이름이 없어 자동으로 만들어지는 이름입니다
@@ -108,44 +108,40 @@
 		"""
 		self.xlbook.Worksheets.Add()
 		Sheet = self.xlbook.ActiveSheet
 		if input_name != "":
 			Sheet.Name = input_name
 
 
-	def add_text_bystep(self, input_text, step):
-		#변경이 필요=================================
+	def add_text_bystep(self, sheet_name="", xyxy="", input_text="입력필요", step=1):
 		# 선택한 영역의 시작점부터 n번째 셀마다 값을 넣기
 		num = 0
-		for x in range(vars["x1"], vars["x2"] + 1):
-			for y in range(vars["y1"], vars["y2"] + 1):
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xyxy)
+		for x in range(x1, x2 + 1):
+			for y in range(y1, y2 + 1):
 				num = num + 1
 				if divmod(num, step)[0] == 0:
-					vars["sheet"].Cells(y, x).Value = input_text
-
+					sheet_object.Cells(y, x).Value = input_text
 
 	def add_text_in_range_at_left(self, sheet_name="", xyxy="", input_text="입력필요"):
 		"""
-		GUI : boribori에 추가됨
-		"1st": "add", "2nd": "text", "3rd": "왼쪽에 글자 추가",
-        "manual": "선택영역의 왼쪽에 글자를 추가한다",
 		선택한 영역의 왼쪽에 입력한 글자를 추가
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		for x in range(x1, x2 + 1):
 			for y in range(y1, y2 + 1):
 				cell_value = sheet_object.Cells(x, y).Value
 				if cell_value == None:
 					cell_value = ""
 				sheet_object.Cells(x, y).Value = str(input_text)+cell_value
 
 	def add_text_in_range_at_right(self, sheet_name="", xyxy="", input_text="입력필요"):
 		"""
-		GUI : boribori에 추가됨
 		선택한 영역의 오른쪽에 입력한 글자를 추가
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		for x in range(x1, x2 + 1):
 			for y in range(y1, y2 + 1):
 				cell_value = sheet_object.Cells(x, y).Value
@@ -181,31 +177,16 @@
 				for y in range(y1, y2+1):
 					if divmod(x, xystep[1])[1] == 0:
 						cell_value = sheet_object.Cells(x, y).Value
 						if cell_value == None:
 							cell_value=""
 						sheet_object.Cells(x, y).Value = cell_value+str(input_text)
 
-	def add_text_specific_string(self, check_str="", input_text=""):
-		#변경이 필요=================================
-		for x in range(vars["x1"], vars["x2"] + 1):
-			for y in range(vars["y1"], vars["y2"] + 1):
-				cell_value = vars["sheet"].Cells(y, x).Value
-				if (check_str in cell_value) and cell_value != "" and cell_value != None:
-					vars["sheet"].Cells(y, x).Value = str(input_text) + str(cell_value)
-
-
-	def change_active_workbook(self, input_file_name):
-		"""
-		열려진 워드 화일중 이름으로 선택하는것
-		"""
-		self.xlapp.Visible = True
-		win32gui.SetForegroundWindow(self.xlapp.hwnd)
-		self.xlapp.WorkBooks(input_file_name).Activate()
-		self.xlapp.WindowState = win32com.client.constants.xlMaximized
+	def add_value_to_left(self, input_text=""):
+		self.write_value_to_left(input_text)
 
 	def change_char_to_num(self, input_text="입력필요"):
 		"""
 		주소를 바꿔주는 것이다
 		문자가 오던 숫자가 오던 숫자로 변경하는 것이다
 		 b를 2로 바꾸어 주는것
 		"""
@@ -239,14 +220,15 @@
 				value1 = input_list2d[no][before]
 				value2 = input_list2d[no][after]
 				input_list2d[no][before] = value2
 				input_list2d[no][after] = value1
 		return input_list2d
 
 	def change_first_char(self, sheet_name = "", xyxy="", input_2d_list=[]):
+		# 가끔 맨앞글자만 바꾸고 싶을때
 		#엑셀값중, 맨앞의 글자만 변경하는 것
 		#사용법 : change_first_char("", [1,1,100,1], [["'", ""], ["*", ""], [" ", ""],])
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 
 		to_be_changed = []
 		for one in input_2d_list:
@@ -345,14 +327,27 @@
 			if max_num == one_len:
 				result.append(one)
 			else:
 				one.extend([input_text] * (max_num - one_len))
 				result.append(one)
 		return result
 
+	def change_list2d_by_index(self, input_list2d, input_no_list):
+		#번호의 라인을 서로 바꾸는 것
+		#1번라인과 3번라인을 교체
+		# input_no_list.sort()
+		# input_no_list.reverse()
+		for before, after in input_no_list:
+			for no in range(len(input_list2d)):
+				value1 = input_list2d[no][before]
+				value2 = input_list2d[no][after]
+				input_list2d[no][before] = value2
+				input_list2d[no][after] = value1
+		return input_list2d
+
 	def change_num_to_char(self, input_data="입력필요"):
 		"""
 		입력값 : 27 => 출력값 : aa
 		숫자를 문자로 바꿔주는 것
 		"""
 		re_com = re.compile(r"([0-9]+)")
 		result_num = re_com.match(str(input_data))
@@ -385,17 +380,15 @@
 
 	def change_rgbint_to_colorname(self, rgbint ):
 		"""
 		rgb의 정수값을 color이름으로 변경
 		"""
 		try :
 			rgblist = self.change_rgbint_to_rgb(rgbint)
-			#print("rgblist", rgblist)
 			color_index = self.data_dic_colorindex_to_rgblist(rgblist)
-			#print("color_index", color_index)
 			colorname = self.data_dic_colorname_to_colorindex(color_index)
 		except:
 			colorname = None
 		return colorname
 
 	def change_rgbint_to_rgb(self, input_int):
 		"""
@@ -464,19 +457,17 @@
 		선택영역안의 모든글자를 소문자로 만들어 주는것
 		screen update를 off로 사용
 		값 읽어오는것을 range형태로 변경
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		list_2d = self.read_value_in_range(sheet_name, xyxy)
-		#print(list_2d[0:3])
 		self.screen_update_off()
 		for x in range(x1, x2 + 1):
 			for y in range(y1, y2 + 1):
-				#print(x, y)
 				try:
 					sheet_object.Cells(x, y).Value = (list_2d[x - x1][y - y1]).lower()
 				except:
 					pass
 		self.screen_update_on()
 
 	def change_value_in_range_to_capital(self, sheet_name, xyxy):
@@ -633,25 +624,35 @@
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		px1, py1, px1_w, py1_h = self.read_coord_in_cell("", [x1, y1])
 		px2, py2, px2_w, py2_h = self.read_coord_in_cell("", [x2, y2])
 
 		result = [px1, py1, px2+px2_w-px1, py2+py2_h-py1]
 		return result
 
-	def change_xyxy_to_r1r1(self, xyxy=""):
+	def change_xyxy_to_r1c1(self, xyxy=""):
 		"""
 		입력값 :	[1,2,3,4]
 		출력값 : "b1:d3"
 		"""
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		str_1 = self.change_num_to_char(y1)
 		str_2 = self.change_num_to_char(y2)
 		result = str_1 + str(x1) + ":" + str_2 + str(x2)
 		return result
 
+	def change_xyxy_to_r1r1(self, xyxy=""):
+		"""
+		입력값 :	[1,2,3,4]
+		출력값 : "b1:b1"
+		"""
+		x1, y1, x2, y2 = self.check_address_value(xyxy)
+		str_1 = self.change_num_to_char(y1)
+		result = str_1 + str(x1) + ":" + str_1 + str(x1)
+		return result
+
 	def check_address_value(self, input_data=""):
 		"""
 		입력형태 :, "", [1,2], [1,2,3,4], "$1:$8", "1", "a","a1", "a1b1", "2:3", "b:b"
 		입력된 주소값을 [x1, y1, x2, y2]의 형태로 만들어 주는 것이다
 		입력된 자료의 형태에 따라서 구분을 한다
 		"""
 		if input_data == "" or input_data == None:  # 아무것도 입력하지 않을때
@@ -695,14 +696,20 @@
 		result["xyxy_min"] = [x1, y1, x1 + min_y, y1 + min_num]
 		# 입력할것중 가장 큰것을 기준으로 적용
 		result["xyxy_max"] = [x1, y1, x1 + max_y, y1 + max_y]
 		# 일반적인기준으로 적용하는것
 		result["xyxy_basic"] = [x1, y1, x1 + x_len, y1 + max_num]
 		return result
 
+	def check_basic_input_datas(self, sheet_name, xyxy):
+		if self.var_p["repeat_start"] and not self.var_p["repeat_end"] :
+			self.var_p["sheet_obj"] = self.check_sheet_name(sheet_name)
+			self.var_p["xyxy"] = self.check_address_value(xyxy)
+			self.var_p["my_range"] = self.var_p["sheet_obj"].Range(self.var_p["sheet_obj"].Cells(self.var_p["xyxy"][0], self.var_p["xyxy"][1]), self.var_p["sheet_obj"].Cells(self.var_p["xyxy"][2], self.var_p["xyxy"][3]))
+
 	def check_cell_type(self, input_data="입력필요"):
 		"""
 		check_cell_type( input_data="입력필요")
 		주소형태의 문자열이 어떤 형태인지 알아 내는 것
 		입력값 : 주소형태의 문자열
 		출려값 : "a1", "aa", "11"
 		"""
@@ -999,23 +1006,23 @@
 		"""
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		result = [x1, y1]
 		return result
 
 	def check_y_address(self, input_data="입력필요"):
 		"""
-		결과= ["b", "b"]의 형태로 만들어 주는것
+		결과 = ["b", "b"]의 형태로 만들어 주는것
 		"""
 		temp = self.check_yy_address(input_data)
 		result = temp[0]
 		return result
 
 	def check_yy_address(self, input_data="입력필요"):
 		"""
-		결과= ["b", "b"]의 형태로 만들어 주는것
+		결과 = ["b", "b"]의 형태로 만들어 주는것
 		"""
 		if input_data == "" or input_data == None:
 			temp = self.read_address_in_selection()
 			result = [temp[1], temp[3]]
 		elif type(input_data) == type("string") or type(input_data) == type(123):
 			temp = self.change_num_to_char(input_data)
 			result = [temp, temp]
@@ -1057,15 +1064,15 @@
 	def close_workbook(self):
 		"""
 		현재는 close를 시키면 엑셀워크북만이 아니라 엑셀자체도 종료 시킵니다
 		"""
 		self.xlbook.Close(SaveChanges=0)
 		del self.xlapp
 
-	def concate_xlne(self, input_list2d, xy):
+	def concate_xline(self, input_list2d, xy):
 		"""
 		# 선택한 영역의 세로자료들을 다 더해서 제일위의 셀에 다시 넣는것
 		"""
 		x_len = len(input_list2d)
 		y_len = len(input_list2d[0])
 		for y in range(y_len):
 			temp = ""
@@ -1153,85 +1160,85 @@
 		result = self.read_worksheet_numbers()
 		return result
 
 	def data_dic_colorindex_to_colorname(self, input_colorindex):
 		"""
 		색이름으로 엑셀 색번호를 돌려주는것
 		"""
-		dic_colorname_colorindex = self.var["excel_colorindex_vs_color_name"]
+		dic_colorname_colorindex = self.var_p["excel_colorindex_vs_color_name"]
 
 		result = dic_colorname_colorindex[int(input_colorindex)]
 		return result
 
 	def data_dic_colorindex_to_rgbint(self, input_rgbint):
 		"""
 		rgb int값으로 엑셀의 색번호를 돌려주는것
 		"""
-		dic_colorindex_rgbint = self.var["excel_colorindex_vs_rgbint"]
+		dic_colorindex_rgbint = self.var_p["excel_colorindex_vs_rgbint"]
 		result = dic_colorindex_rgbint[int(input_rgbint)]
 		return result
 
 	def data_dic_colorindex_to_rgblist(self, rgblist):
 		"""
 		rgb값으로 엑셀의 색번호를 돌려주는것
 		"""
-		basic = self.var["dic_rgb값_vs_엑셀_색번호"]
+		basic = self.var_p["dic_rgb값_vs_엑셀_색번호"]
 		result = basic[rgblist]
 		return result
 
 	def data_dic_colorname_to_colorindex(self, input_colorindex):
 		"""
 		색번호로 색이름을 돌려주는것
 		"""
-		dic_colorname_colorindex = self.var["dic_색이름_vs_엑셀_색번호"]
+		dic_colorname_colorindex = self.var_p["dic_색이름_vs_엑셀_색번호"]
 
 		result = dic_colorname_colorindex[int(input_colorindex)]
 		return result
 
 	def data_dic_line_position(self, input_data=""):
 		"""
 		라인 위치에 대한 자료를 돌려준디
 		"""
-		line_position = self.var["dic_선위치_vs_index번호"]
+		line_position = self.var_p["dic_선위치_vs_index번호"]
 
 		if input_data in line_position.keys():
 			result = line_position[input_data]
 		else:
 			result = [9]
 		return result
 
 	def data_dic_line_style(self, input_data=""):
 		"""
 		라인 스타일에 대한 자료를 돌려준디
 		"""
-		line_style_dic = self.var["dic_선형태_vs_번호"]
+		line_style_dic = self.var_p["dic_선형태_vs_번호"]
 
 		if input_data in line_style_dic.keys():
 			result = line_style_dic[input_data]
 		else:
 			result = 1
 		return result
 
 	def data_dic_line_thickness(self, input_data=""):
 		"""
 		라인 두께에 대한 자료를 돌려준디
 		"""
-		line_thickness_dic = self.var["dic_선굵기_vs_번호"]
+		line_thickness_dic = self.var_p["dic_선굵기_vs_번호"]
 
 		if input_data in line_thickness_dic.keys():
 			result = line_thickness_dic[input_data]
 		else:
 			result = 2
 		return result
 
 	def data_dic_rgblist_to_colorindex(self, input_colorindex):
 		"""
 		엑셀의 색번호로 rgb값을 돌려주는것
 		"""
-		dic_colorindex_rgblist = self.var["dic_rgb값_vs_엑셀_색번호"]
+		dic_colorindex_rgblist = self.var_p["dic_rgb값_vs_엑셀_색번호"]
 
 		result = dic_colorindex_rgblist[int(input_colorindex)]
 		return result
 
 	def delete_all_draw_line_in_range(self, sheet_name="", xyxy=""):
 		"""
 		시트의 모든 라인을 지우는 것
@@ -1306,37 +1313,27 @@
 		시트안의 모든 값만을 삭제
 		시트를 그대로 둬야하는 경우에 사용
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		sheet_object.Cells.ClearContents()
 
 	def delete_color(self, sheet_name, xyxy):
-		sheet_object = self.check_sheet_name(sheet_name)
-		x1, y1, x2, y2 = self.check_address_value(xyxy)
-		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
-
-		my_range.Interior.Pattern = -4142
-		my_range.Interior.TintAndShade = 0
-		my_range.Interior.PatternTintAndShade = 0
-
+		self.delete_color_in_range(sheet_name, xyxy)
 
 	def delete_color_in_range(self, sheet_name="", xyxy=""):
 		"""
 		영역의 색을 지우는 것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.Interior.Pattern = -4142
 		my_range.Interior.TintAndShade = 0
 		my_range.Interior.PatternTintAndShade = 0
 
-	def set_range_nocolor(self, sheet_name, xyxy):
-		self.delete_color_in_range(sheet_name, xyxy)
-
 	def delete_continious_samevalue_in_range(self, sheet_name="", xyxy=""):
 		"""
 		대상 : 선택한 영역
 		밑으로 같은 값들이 있으면 지우는것
 		"""
 
 		sheet_object = self.check_sheet_name(sheet_name)
@@ -1345,63 +1342,41 @@
 			for x in range(x2, x1 + 1, -1):
 				base_value = sheet_object.Cells(x, y).Value
 				up_value = str(sheet_object.Cells(x-1, y).Value)
 				if base_value == up_value:
 					# self.write_value_in_cell(sheet_name, [x, y], "")
 					sheet_object.Cells(x, y).Value = ""
 
-	def delete_line_in_list2d_by_index(self, input_list2d, no_list):
-		#입력형태 : 2차원리스트, [2,5,7]
-		no_list.sort()
-		no_list.reverse()
-		for one in no_list:
-			for x in range(len(input_list2d)):
-				del input_list2d[x][one]
-		return input_list2d
-
 	def delete_linecolor(self, sheet_name, xyxy):
-		sheet_object = self.check_sheet_name(sheet_name)
-		x1, y1, x2, y2 = self.check_address_value(xyxy)
-		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
-		my_range.Interior.Pattern = 0
-		my_range.Interior.PatternTintAndShade = 0
-
+		self.delete_linecolor_in_range(sheet_name, xyxy)
 
 	def delete_linecolor_in_range(self, sheet_name="", xyxy=""):
 		"""
 		영역안의 라인의 색을 지우는 것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.Interior.Pattern = 0
 		my_range.Interior.PatternTintAndShade = 0
 
 	def delete_link(self, sheet_name, xyxy):
-		sheet_object = self.check_sheet_name(sheet_name)
-		x1, y1, x2, y2 = self.check_address_value(xyxy)
-		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
-		my_range.Hyperlinks.Delete()
-
+		self.delete_link_in_range(sheet_name, xyxy)
 
 	def delete_link_in_range(self, sheet_name="", xyxy=""):
 		"""
 		영역안의 링크를 삭제하는 것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.Hyperlinks.Delete()
 
 	def delete_memo(self, sheet_name, xyxy):
-		sheet_object = self.check_sheet_name(sheet_name)
-		x1, y1, x2, y2 = self.check_address_value(xyxy)
-		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
-		my_range.ClearComments()
-
+		self.delete_memo_in_range(sheet_name, xyxy)
 
 	def delete_memo_in_range(self, sheet_name="", xyxy=""):
 		"""
 		영역안의 메모를 삭제하는 것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
@@ -1430,47 +1405,48 @@
 			for y in range(y1, y2 + 1):
 
 				cell_value = sheet_object.Cells(x, y).Value
 				if cell_value != "" or cell_value != None or cell_value != None:
 					sheet_object.Cells(x, y).Value = cell_value[int(num):]
 
 	def delete_rangename(self, range_name):
+		#########엣날 자료를 위한것으로, 더이상 사용하지 마세요
 		self.xlbook.Names(range_name).Delete()
 
-
 	def delete_rangename_all(self):
 		"""
 		모든 rangename을 삭제하는 것
 		"""
 		aaa = self.xlapp.Names
 		for one in aaa:
 			ddd = str(one.Name)
 			if ddd.find("!") < 0:
 				#print(one.Name)
 				self.xlapp.Names(aaa).Delete()
 
-	def delete_rangename_by_name(self, sheet_name, range_name):
+	def delete_rangename_by_name(self, range_name):
 		"""
 		입력한 이름을 삭제한다
 		name은 workbook으로 되지만 동일하게 하기위하여 sheet_name을 넣은 것이다
 		"""
 		result = self.xlbook.Names(range_name).Delete()
 		return result
 
 	def delete_rangname_for_panthom(self):
-		self.delete_panthom_rangname()
-
-	def delete_rangname_panthom(self):
 		aaa = self.xlbook.Names
 		cnt = self.xlbook.Names.Count
 		for num in range(1, cnt + 1):
 			aaa = self.xlbook.Names(num).Name
 			if aaa.find("!") < 0:
 				self.xlbook.Names(aaa).Delete()
 
+	def delete_rangname_panthom(self):
+		#########엣날 자료를 위한것으로, 더이상 사용하지 마세요
+		self.delete_rangname_for_panthom()
+
 	def delete_samevalue_in_range(self, sheet_name="", xyxy=""):
 		"""
 		영역안의 같은 값을 지우는 것이다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		set_a = set([])
@@ -1504,14 +1480,15 @@
 		sheet_object.Shapes(shape_name).Delete()
 
 	def delete_shape_in_sheet(self, sheet_name, shape_name):
 		sheet_object = self.check_sheet_name(sheet_name)
 		sheet_object.Shapes(shape_name).Delete()
 
 	def delete_sheet(self, sheet_name=""):
+		#########엣날 자료를 위한것으로, 더이상 사용하지 마세요
 		self.delete_sheet_by_name(sheet_name)
 
 	def delete_sheet_by_name(self, sheet_name=""):
 		"""
 		시트하나 삭제하기
 		"""
 		try:
@@ -1743,53 +1720,50 @@
 		sheet_object = self.check_sheet_name(sheet_name)
 		for y in range(yy_list[0], yy_list[1]+1):
 			changed_address = str(y) + ":" + str(y)
 			num = self.xlbook.WorksheetFunction.CountA(sheet_object.Range(changed_address))
 			if num == 0:
 				sheet_object.Rows(changed_address).Delete()
 
-
 	def delete_yyline(self, sheet_name="", yy=""):
 		"""
 		선택한영역에서 여러개의 y줄을 삭제한다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		y1, y2 = self.check_yy_address(yy)
 		sheet_object.Columns(y1 + ':' + y2).Delete()
 
-
-
 	def delete_yyline_in_sheet(self, sheet_name="", yy=""):
 		self.delete_yyline(sheet_name, yy)
 
-	def draw_bottomline(self, sheet_name, xyxy, line_style, thickness, scolor):
+	def draw_bottomline_in_range(self, sheet_name, xyxy, line_style, thickness, scolor):
+		"""
+		선택영역에서 선을 긋는것, 맨마지막 라인에 선긋기
+		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		rgb_list = self.color.change_color_to_rgb(scolor)
 		my_range.Borders(9).Color = self.color.change_rgb_to_rgbint(rgb_list)
 		my_range.Borders(9).Weight = thickness
 		my_range.Borders(9).LineStyle = line_style
 
-
-	def draw_bottomline_in_range(self, sheet_name="", xyxy="", line_style="basic", thickness="basic", color="blu"):
-		"""
-		선택영역에서 선을 긋는것, 맨마지막 라인에 선긋기
-		"""
+	def draw_bottomline(self, sheet_name="", xyxy="", line_style="basic", thickness="basic", color="blu"):
+		#########엣날 자료를 위한것으로, 더이상 사용하지 마세요
 		self.draw_line_one_in_range(sheet_name, xyxy, line_style, thickness, color, 9)
 
 	def draw_detail_line_in_range(self, **input):
 		"""
 		선택영역에서 선을 긋는것
 		선긋기를 좀더 상세하게 사용할수 있도록 만든것
 		밐의 base_data의 값들을 이용해서 입력하면 된다
 		"""
-		enum_line = self.var["dic_선모양_vs_index번호"]
-		base_data = self.var["base_cell_data"]
+		enum_line = self.var_p["dic_선모양_vs_index번호"]
+		base_data = self.var_p["base_cell_data"]
 		# 기본자료에 입력받은값을 update하는것이다
 		sheet_object = self.check_sheet_name("")
 		base_data.update(input)
 		sheet = self.check_sheet_name(base_data["sheet_name"])
 		set_line = sheet_object.Shapes.AddLine(base_data["xyxy"][0], base_data["xyxy"][1], base_data["xyxy"][2], base_data["xyxy"][3])
 		set_line.Select()
 		set_line.Line.ForeColor.RGB = base_data["color"]
@@ -1802,58 +1776,57 @@
 		set_line.Line.BeginArrowheadWidth = enum_line[base_data["head_width"]]
 		set_line.Line.EndArrowheadStyle = enum_line[base_data["tail_style"]]  # 화살표의 머리의 모양
 		set_line.Line.EndArrowheadLength = enum_line[base_data["tail_length"]]  # 화살표의 길이
 		set_line.Line.EndArrowheadWidth = enum_line[base_data["tail_width"]]  # 화살표의 넓이
 		result = set_line.Name
 		return result
 
-	def draw_innerx_line_in_range(self, sheet_name="", xyxy="", line_style="basic", thickness="basic", color="blu"):
-		"""	선택영역에서 선을 긋는것, 안쪽에 x라인 선긋기 """
-		self.draw_line_one_in_range(sheet_name, xyxy, line_style, thickness, color, 12)
-
-	def draw_innerxline(self, sheet_name, xyxy, line_style, thickness, scolor):
+	def draw_inner_xline(self, sheet_name, xyxy, line_style, thickness, scolor):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		rgb_list = self.color.change_color_to_rgb(scolor)
 		my_range.Borders(12).Color = self.color.change_rgb_to_rgbint(rgb_list)
 		my_range.Borders(12).Weight = thickness
 		my_range.Borders(12).LineStyle = line_style
 
-
-	def draw_innery_line_in_range(self, sheet_name="", xyxy="", line_style="basic", thickness="basic", color="blu"):
-		"""	선택영역에서 선을 긋는것, 안쪽에 y라인 선긋기 """
-		self.draw_line_one_in_range(sheet_name, xyxy, line_style, thickness, color, 11)
-
-	def draw_inneryline(self, sheet_name, xyxy, line_style, thickness, scolor):
+	def draw_inner_yline(self, sheet_name, xyxy, line_style, thickness, scolor):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		rgb_list = self.color.change_color_to_rgb(scolor)
 		my_range.Borders(11).Color = self.color.change_rgb_to_rgbint(rgb_list)
 		my_range.Borders(11).Weight = thickness
 		my_range.Borders(11).LineStyle = line_style
 
-	def draw_left_line_in_range(self, sheet_name="", xyxy="", line_style="basic", thickness="basic", color="blu"):
-		"""	선택영역에서 선을 긋는것, 왼쪽에 선긋기 """
-		self.draw_line_one_in_range(sheet_name, xyxy, line_style, thickness, color, 7)
+	def draw_innerx_line_in_range(self, sheet_name="", xyxy="", line_style="basic", thickness="basic", color="blu"):
+		"""	선택영역에서 선을 긋는것, 안쪽에 x라인 선긋기 """
+		self.draw_line_one_in_range(sheet_name, xyxy, line_style, thickness, color, 12)
 
-	def draw_leftline(self, sheet_name, xyxy, line_style, thickness, scolor):
+	def draw_innery_line_in_range(self, sheet_name="", xyxy="", line_style="basic", thickness="basic", color="blu"):
+		"""	선택영역에서 선을 긋는것, 안쪽에 y라인 선긋기 """
+		self.draw_line_one_in_range(sheet_name, xyxy, line_style, thickness, color, 11)
+
+	def draw_left_line_in_range(self, sheet_name, xyxy, line_style, thickness, scolor):
+		"""	선택영역에서 선을 긋는것, 왼쪽에 선긋기 """
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 
 		rgb_list = self.color.change_color_to_rgb(scolor)
 		my_range.Borders(7).Color = self.color.change_rgb_to_rgbint(rgb_list)
 		my_range.Borders(7).Weight = thickness
 		my_range.Borders(7).LineStyle = line_style
 
+	def draw_left_line(self, sheet_name="", xyxy="", line_style="basic", thickness="basic", color="blu"):
+		#########엣날 자료를 위한것으로, 더이상 사용하지 마세요
+		self.draw_line_one_in_range(sheet_name, xyxy, line_style, thickness, color, 7)
 
 	def draw_line(self, sheet_name, xyxy, input_list):
 		"""
 	  draw_range_line(sheet_name="", xyxy="", input_list)
 	  [선의위치, 라인스타일, 굵기, 색깔]
 	  입력예 : [7,1,2,1], ["left","-","t0","bla"]
 	  선의위치 (5-대각선 오른쪽, 6-왼쪽대각선, 7:왼쪽, 8;위쪽, 9:아래쪽,
@@ -1862,52 +1835,82 @@
 	  굵기 (0-이중, 1-얇게, 2-굵게)
 	  색깔 (0-검정, 1-검정, 3-빨강),
 	  """
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
-		line_type = self.var["dic_선위치_vs_번호"]
-		line_style_dic = self.var["dic_선형태_vs_번호"]
-		weight_dic = self.var["dic_선굵기_vs_번호"]
+		line_type = self.var_p["dic_선위치_vs_번호"]
+		line_style_dic = self.var_p["dic_선형태_vs_번호"]
+		weight_dic = self.var_p["dic_선굵기_vs_번호"]
 
 		rgb_list = self.color.change_color_to_rgb(input_list[3])
 		my_range.Borders(line_type[input_list[0]]).Color = self.color.change_rgb_to_rgbint(rgb_list)
 		my_range.Borders(line_type[input_list[0]]).Weight = weight_dic[input_list[2]]
 		my_range.Borders(line_type[input_list[0]]).LineStyle = line_style_dic[input_list[1]]
 
-
-
 	def draw_line_in_pxyxy_range(self, sheet_name, line_xyxy, rgb_list):
 		"""
 		선택영역에서 선을 긋는것
 		pixel을 기준으로 선긋기
 		선을 그을때는 위치와 넓이 높이로 긋는데, change_xyxy_to_pxyxy을 사용하면 셀위치를 그렇게 바꾸게 만든다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(line_xyxy)
 		pxyxy = self.change_xyxy_to_pxyxy([x1, y1, x2, y2])
 		#print(pxyxy)
 		sheet_object.Shapes.AddLine(pxyxy[0], pxyxy[1], pxyxy[2], pxyxy[3]).Select()
 		self.xlapp.Selection.ShapeRange.Line.ForeColor.RGB = self.color.change_rgb_to_rgbint(rgb_list)
 		self.xlapp.Selection.ShapeRange.Line.Weight = 5
 
-	def draw_line_in_range(self, sheet_name="", xyxy="", position="", scolor="", line_style="", thickness=""):
+	def draw_line_in_range_as_basic(self, sheet_name="", xyxy="", position="all", scolor="black", line_style="basic", thickness="thin"):
 		"""
 		입력예 : [선의위치, 색깔, 라인스타일, 굵기] ==> [7,1,2,1], "", "",""
 		""으로 된것이 기본으로 설정하는 것이다
 		"l": left, "t": top, "b": bottom, "r": right, "h": horizental, "v": vertical, "a": all,"o": outside,"/": "/","\\": "\",
 		""으로 된것이 기본으로 설정하는 것이다
 		color = rgb 값
 		"""
-		line_position = self.var["dic_선위치_vs_index번호"]
-		line_thickness_dic = self.var["dic_선굵기_vs_번호"]
-		line_style_dic = self.var["dic_선형태_vs_번호"]
+		line_position = self.var_p["dic_선위치_vs_index번호"]
+		line_thickness_dic = self.var_p["dic_선굵기_vs_번호"]
+		line_style_dic = self.var_p["dic_선형태_vs_번호"]
+
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xyxy)
+
+		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
+		#print(scolor)
+		rgb_list = self.color.change_scolor_to_rgb(scolor)
+		colorint = self.color.change_rgb_to_rgbint(rgb_list)
+		aa = []
+		if type(position) == type([]):
+			for one in position:
+				aa.extend(line_position[one])
+		else:
+			aa.extend(line_position[position])
+
+		for po_no in aa:
+			my_range.Borders(po_no).Color = colorint
+			my_range.Borders(po_no).Weight = line_thickness_dic[str(thickness)]
+			my_range.Borders(po_no).LineStyle = line_style_dic[line_style]
 
 
+
+	def draw_line_in_range(self, sheet_name="", xyxy="", position="", scolor="", line_style="", thickness=""):
+		"""
+		입력예 : [선의위치, 색깔, 라인스타일, 굵기] ==> [7,1,2,1], "", "",""
+		""으로 된것이 기본으로 설정하는 것이다
+		"l": left, "t": top, "b": bottom, "r": right, "h": horizental, "v": vertical, "a": all,"o": outside,"/": "/","\\": "\",
+		""으로 된것이 기본으로 설정하는 것이다
+		color = rgb 값
+		"""
+		line_position = self.var_p["dic_선위치_vs_index번호"]
+		line_thickness_dic = self.var_p["dic_선굵기_vs_번호"]
+		line_style_dic = self.var_p["dic_선형태_vs_번호"]
+
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		#print(scolor)
 		rgb_list = self.color.change_scolor_to_rgb(scolor)
 		colorint = self.color.change_rgb_to_rgbint(rgb_list)
@@ -1933,36 +1936,35 @@
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		rgb_list = self.color.change_scolor_to_rgb(color)
 		my_range.Borders(line_position).Color = self.color.change_rgb_to_rgbint(rgb_list)
 		my_range.Borders(line_position).Weight = self.data_dic_line_thickness(thickness)
 		my_range.Borders(line_position).LineStyle = self.data_dic_line_style(line_style)
 
-	def draw_rightline(self, sheet_name, xyxy, line_style, thickness, scolor):
+	def draw_right_line(self, sheet_name, xyxy, line_style, thickness, scolor):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		rgb_list = self.color.change_color_to_rgb(scolor)
 		my_range.Borders(10).Color = self.color.change_rgb_to_rgbint(rgb_list)
 		my_range.Borders(10).Weight = thickness
 		my_range.Borders(10).LineStyle = line_style
 
 
-	def draw_topline(self, sheet_name, xyxy, line_style, thickness, scolor):
+	def draw_top_line(self, sheet_name, xyxy, line_style, thickness, scolor):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		rgb_list = self.color.change_color_to_rgb(scolor)
 		my_range.Borders(8).Color = self.color.change_rgb_to_rgbint(rgb_list)
 		my_range.Borders(8).Weight = thickness
 		my_range.Borders(8).LineStyle = line_style
 
-
 	def draw_triangle(self, xyxy, per=100, reverse=1, size=100):
 		"""
 		직각삼각형
 		정삼각형에서 오른쪽이나 왼쪽으로 얼마나 더 간것인지
 		100이나 -100이면 직삼각형이다
 		사각형은 왼쪽위에서 오른쪽 아래로 만들어 진다
 		"""
@@ -2062,14 +2064,21 @@
 			while 1:
 				temp_range = my_range.FindNext(temp_range)
 				if temp_range == None or temp_range == first_range.Address:
 					break
 				else:
 					temp_range = temp_range
 
+	def get_4_edge_xy_for_xyxy(self, xyxy=[1, 2, 3, 4]):
+		# 영역을 주면, 4 개의 꼭지점을 돌려주는것
+		# 기준은 왼쪽위부터 시계방향으로 돌아간다
+		x1, y1, x2, y2 = xyxy
+		result = [[x1, y1], [x1, y2], [x2, y2], [x2, y1]]
+		return result
+
 	def get_activesheet_object(self):
 		sheet_name = self.xlapp.ActiveSheet.Name
 		sheet_object = self.check_sheet_name(sheet_name)
 		return sheet_object
 
 	def get_diagonal_xy(self, xyxy=[5, 9, 12, 21]):
 		"""
@@ -2142,19 +2151,19 @@
 		else:
 			self.insert_sheet()
 			old_sheet_name = self.read_activesheet_name()
 			self.change_sheet_name(old_sheet_name, sheet_name)
 			sheet_object = self.check_sheet_name(sheet_name)
 		return sheet_object
 
-	def get_vba_module_name_all(self, ):
+	def get_vba_module_name_all(self):
 		"""
 		현재 열려진 엑셀 화일안의 매크로모듈 이름을 찾아서 돌려주는 것
 		아래에 1,2,3을 쓴것은 모듈의 종류를 여러가지인데, 해당하는 모듈의 종류이며.
-		이것을 하지 않으면 다른 종류의 것들도 돌려쥬기 때문이다
+		이것을 하지 않으면 다른 종류의 것들도 돌려주기 때문이다
 
 		 xlapp.Close(SaveChanges=False)
 		 xlapp.Quit()
 		 del.xlapp
 		"""
 		result = []
 		for i in self.xlbook.VBProject.VBComponents:
@@ -2251,24 +2260,22 @@
 		"""
 		입력창을 만들어서 입력값을 받는것
 		"""
 		result = self.xlapp.InputBox(text_01)
 		return result
 
 	def insert_excel_function_in_cell(self, sheet_name, xy, input_fucntion, input_xyxy):
-		result = ""
 		sheet_object = self.check_sheet_name(sheet_name)
-		range = self.change_xyxy_to_r1r1(input_xyxy)
+		range = self.change_xyxy_to_r1c1(input_xyxy)
 		x1, y1, x2, y2 = self.check_address_value(xy)
 		result = "="+input_fucntion+"("+range+")"
-
 		sheet_object.Cells(x1, y1).Value = result
 
 	def insert_image_in_sheet(self, sheet_name, file_path, xywh, link=0, image_in_file=1):
-		self.insert_picture_in_sheet(self, sheet_name, file_path, xywh, link, image_in_file)
+		self.insert_picture_in_sheet(sheet_name, file_path, xywh, link, image_in_file)
 
 	def insert_image_in_xyxy(self, sheet_name, xyxy, file_path):
 		"""
 		image화일을 넣는것
 		선택한 영역안에 자동으로 올수있도록 만들어 보자
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
@@ -2302,14 +2309,17 @@
 		시트하나 추가하기
 		"""
 		self.xlbook.Worksheets.Add()
 		if sheet_name:
 			old_name = self.xlapp.ActiveSheet.Name
 			self.xlbook.Worksheets(old_name).Name = sheet_name
 
+	def insert_sheet_new(self, sheet_name=""):
+		self.insert_sheet(sheet_name)
+
 	def insert_sheet_with_name(self, sheet_name="입력필요"):
 		"""
 		시트이름과 함께 시트하나 추가하기
 		함수의 공통적인 이름을 위해서 만든것
 		"""
 		self.insert_sheet(sheet_name)
 
@@ -2348,16 +2358,14 @@
 		x1 = self.change_char_to_num(xx_list[0])
 		x2 = self.change_char_to_num(xx_list[1])
 		min_x1 = min(x1, x2)
 		max_x2 = max(x1, x2)
 		for num in range(max_x2+1, min_x1, -1):
 			sheet_object.Range(str(num) + ':' + str(num)).Insert(-4121)
 
-
-
 	def insert_xxline_in_range(self, sheet_name="", xx_list="입력필요"):
 		"""
 		가로열을 한줄삽입하기
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		if type(xx_list) == type([]) and len(xx_list) == 1:
 			x2 = x1 = self.change_char_to_num(xx_list[0])
@@ -2451,15 +2459,14 @@
 		return result
 
 	def is_empty(self, x_no):
 		x1 = self.change_char_to_num(x_no)
 		result = self.xlbook.WorksheetFunction.CountA(vars["sheet"].Columns(x1).EntireColumn)
 		return result
 
-
 	def is_empty_xline(self, sheet_name, no):
 		"""
 		열전체가 빈 것인지 확인해서 돌려준다
 		현재의 기능은 한줄만 가능하도록 하였다
 		다음엔 영역이 가능하도록 하여야 겠다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
@@ -2472,44 +2479,28 @@
 		현재의 기능은 한줄만 가능하도록 하였다
 		다음엔 영역이 가능하도록 하여야 겠다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		result = self.xlapp.WorksheetFunction.CountA(sheet_object.Columns(no).EntireColumn)
 		return result
 
-	def lock_off(self, sheet_name, password="1234"):
+	def lock_off_for_sheet(self, sheet_name, password="1234"):
 		sheet_object = self.check_sheet_name(sheet_name)
 
 		sheet_object.Unprotect(password)
 
-
-	def lock_on(self, sheet_name, password="1234"):
+	def lock_on_for_sheet(self, sheet_name, password="1234"):
 		sheet_object = self.check_sheet_name(sheet_name)
 
 		sheet_object.protect(password)
 
 	def lock_sheet(self, sheet_name="", password="1234"):
 		sheet_object = self.check_sheet_name(sheet_name)
 		sheet_object.protect(password)
 
-	def lock_with_password(self, pwd="1234567890"):
-		repeat_no = 4
-		count = 0
-		for a in itertools.product(pwd, repeat=repeat_no):
-			count += 1
-			temp_pwd = ("".join(map(str, a)))
-			try:
-				#pcell_dot.setup.lock_off(vars["sheet_name"], temp_pwd)
-				pass
-			except:
-				pass
-			else:
-				break
-		pass
-
 	def make_password(self, isnum="yes", istext_small="yes", istext_big="yes", isspecial="no", len_num=10):
 		"""
 		엑셀시트의 암호를 풀기위해 암호를 계속 만들어서 확인하는 것
 		"""
 		check_char = []
 		if isnum == "yes":
 			check_char.extend(list(string.digits))
@@ -2536,15 +2527,35 @@
 		"""
 		텍스트로 만든 매크로 코드를 실행하는 코드이다
 		"""
 		new_vba_code = "Sub " + macro_name + "()" + vba_code + "End Sub"
 		mod = self.xlbook.VBProject.VBComponents.Add(1)
 		mod.CodeModule.AddFromString(new_vba_code)
 
-	def make_y_value(self, input_data):
+	def make_xy_list_for_box_style(self, xyxy):
+		#??????
+		# 좌표를 주면, 맨끝만 나터내는 좌표를 얻는다
+		temp_1 = []
+		for x in [xyxy[0], xyxy[2]]:
+			temp = []
+			for y in range(xyxy[1], xyxy[3] + 1):
+				temp.append([x, y])
+			temp_1.append(temp)
+
+		temp_2 = []
+		for y in [xyxy[1], xyxy[3]]:
+			temp = []
+			for x in range(xyxy[0], xyxy[2] + 1):
+				temp.append([x, y])
+			temp_2.append(temp)
+
+		result = [temp_1[0], temp_2[1], temp_1[1], temp_2[0]]
+		return result
+
+	def change_input_data_to_yline_style(self, input_data):
 		#1차원리스트를 2차원으로 만들면, 세로입력을 가로입력으로 바꾸는 것이다
 		result = self.change_list1d_to_list2d(input_data)
 		return result
 
 	def manual(self):
 		#간략한 이 모듈에 대한 설명입니다
 		result = 	"""
@@ -2562,29 +2573,36 @@
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		if y1 == y2:
 			pass
 		else:
 			for y in range(y1, y2+1):
 				sheet_object.Range(sheet_object.Cells(x1, y), sheet_object.Cells(x1+1, y)).Merge(0)
 
-	def merge_top_2_ylines_in_range(self, sheet_name="", xyxy=""):  # 셀들을 합하는 것이다
+	def merge_left_2_ylines_in_range(self, sheet_name="", xyxy=""):  # 셀들을 합하는 것이다
 		"""
 		선택 영역중 바로 위의것과 아랫것만 병합하는것
-		제일위의 2줄만 가로씩 병합하는 것이다
-		세로줄 갯수만큰 병합하는것
-		위와 아래에 값이 있으면 알람이 뜰것이다
+		왼쪽의 2줄을 병합하는 것이다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		if x1 == x2:
 			pass
 		else:
 			for x in range(x1, x2+1):
 				sheet_object.Range(sheet_object.Cells(x, y1), sheet_object.Cells(x, y1+1)).Merge(0)
 
+	def move_activecell_in_range_to_bottom(self, sheet_name="", xyxy=""):
+		"""
+		선택한 위치에서 제일왼쪽, 제일아래로 이동
+		xlDown: - 4121,xlToLeft : - 4159, xlToRight: - 4161, xlUp : - 4162
+		"""
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xyxy)
+		sheet_object.Cells(x1, y2).Select()
+
 	def move_activecell_in_range_to_leftend(self, sheet_name="", xyxy=""):
 		"""
 		입력값 : 입력값없이 사용가능
 		선택한 위치에서 끝부분으로 이동하는것
 		xlDown : - 4121, xlToLeft : - 4159, xlToRight : - 4161, xlUp : - 4162
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
@@ -2617,14 +2635,30 @@
 		선택한 위치에서 제일왼쪽, 제일아래로 이동
 		xlDown: - 4121,xlToLeft : - 4159, xlToRight: - 4161, xlUp : - 4162
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		sheet_object.Cells(x1, y2).Select()
 
+	def move_cell(self, sheet_name, xy_from, xy_to):
+		# 1 개의 셀만 이동시키는 것
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xy_from)
+		sheet_object.Cells(x1, y1).Cut()
+		x1, y1, x2, y2 = self.check_address_value(xy_to)
+		my_range = sheet_object.Cells(x1, y1)
+		sheet_object.Paste(my_range)
+
+	def move_activecell_by_xy_offset(self, sheet_name, xy):
+		#activecell을 offset으로 이동시키는것
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xy)
+		xyxy2 = self.read_address_in_activecell()
+		sheet_object.Cells(xyxy2[0] + x1, xyxy2[1] + y1).Select()
+
 	def move_cell_to_another_sheet(self, sheet_list="입력필요", xy_list="입력필요"):
 		"""
 		다른시트로 값1개 옮기기
 		입력형태 : [시트이름1, 시트이름2], [[2,3]. [4,5]]
 		"""
 		sheet_object_1 = self.check_sheet_name(sheet_list[0])
 		x1, y1 = xy_list[0]
@@ -2671,43 +2705,50 @@
 				if before < after:
 					after = after -1
 				value = input_list2d[no][before]
 				del input_list2d[no][before]
 				input_list2d[no].insert(int(after), value)
 		return input_list2d
 
+	def move_range(self, sheet_name, xyxy_from, xyxy_to):
+		# 모든값을 그대로 이동시키는 것
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xyxy_from)
+		my_range1 = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
+		my_range1.Cut()
+		x1, y1, x2, y2 = self.check_address_value(xyxy_to)
+		my_range2 = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
+		sheet_object.Paste(my_range2)
+
 	def move_shape(self, sheet_name, shape_obj, top, left):
 		# shape_obj : 이동시림 도형 이름
 		sheet_object = self.check_sheet_name(sheet_name)
 		oShape = sheet_object.Shapes(shape_obj)
 		oShape.Top = oShape.Top + top
 		oShape.Left = oShape.left + left
 
-	def move_to_bottom(self, sheet_name, xyxy):
+	def move_to_bottom_in_range(self, sheet_name, xyxy):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.End(- 4121).Select()
 
-
-	def move_to_leftend(self, sheet_name, xyxy):
+	def move_to_leftend_in_range(self, sheet_name, xyxy):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.End(- 4159).Select()
 
-
-	def move_to_rightend(self, sheet_name, xyxy):
+	def move_to_rightend_in_range(self, sheet_name, xyxy):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.End(- 4161).Select()
 
-
-	def move_to_top(self, sheet_name, xyxy):
+	def move_to_top_in_range(self, sheet_name, xyxy):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.End(- 4162).Select()
 
 
 	def move_value_in_range_to_left_except_emptycell(self, sheet_name="", xyxy=""):
@@ -2811,23 +2852,32 @@
 					pass
 				else:
 					try:
 						self.xlbook = self.xlapp.Workbooks.Open(self.path_full)
 					except:
 						win32gui.MessageBox(0, "화일이름이나 경로를 다시한번 확인해 보시기 바랍니다”, .halmoney.com", 0)
 
+	def open_workbook(self, input_file_name):
+		"""
+		열려진 워드 화일중 이름으로 선택하는것
+		"""
+		self.xlapp.Visible = True
+		win32gui.SetForegroundWindow(self.xlapp.hwnd)
+		self.xlapp.WorkBooks(input_file_name).Activate()
+		self.xlapp.WindowState = win32com.client.constants.xlMaximized
+
 	def paint_cell_by_excel_colorno(self, sheet_name, xy, excel_color_no="입력필요"):
 		"""
 		paint_color(sheet_name, xyxy, input_data="입력필요")
 		선택 셀에 색깔을 넣는다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		self.check_address_value(xy)
 
-		rgbvalue = self.var["rgb_56_for_excel"][excel_color_no]
+		rgbvalue = self.var_p["rgb_56_for_excel"][excel_color_no]
 
 		rgb_to_int = (int(rgbvalue[2])) * (256 ** 2) + (int(rgbvalue[1])) * 256 + int(rgbvalue[0])
 		sheet_object.Cells(xy[0], xy[1]).Interior.Color = int(rgb_to_int)
 
 	def paint_cell_by_rgb(self, sheet_name, xy, input_color="입력필요"):
 		"""
 		paint_color(sheet_name, xyxy, input_data="입력필요")
@@ -2861,14 +2911,23 @@
 
 		for x in range(x1, x2 + 1):
 			for y in range(y1, y2 + 1):
 				value = sheet_object.Cells(x, y).Value
 				if input_text in value:
 					self.paint_cell_by_scolor(sheet_name, [x,y], input_color)
 
+	def paint_color_in_cell(self, sheet_name, xyxy, input_color):
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xyxy)
+		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
+
+		input_data = self.color.check_input_color(input_color)
+		rgb_to_int = (int(input_data[2])) * (256 ** 2) + (int(input_data[1])) * 256 + int(input_data[0])
+		my_range.Interior.Color = rgb_to_int
+
 	def paint_color_in_range(self, sheet_name, xyxy, input_color="입력필요"):
 		"""
 		paint_color(sheet_name, xyxy, input_data="입력필요")
 		선택 영역에 색깔을 넣는다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
@@ -2897,23 +2956,14 @@
 				temp_int = 0
 				for one_word in basic_list:
 					if re.match('(.*)' + one_word + '(.*)', str(cell_value)):
 						temp_int = temp_int + 1
 				if temp_int == total_no:
 					self.paint_color_in_range(sheet_name, [x, y], "yel")
 
-	def paint_color_name_in_cell(self, sheet_name, xyxy, input_color):
-		sheet_object = self.check_sheet_name(sheet_name)
-		x1, y1, x2, y2 = self.check_address_value(xyxy)
-		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
-
-		input_data = self.color.check_input_color(input_color)
-		rgb_to_int = (int(input_data[2])) * (256 ** 2) + (int(input_data[1])) * 256 + int(input_data[0])
-		my_range.Interior.Color = rgb_to_int
-
 	def paint_font_in_cell_by_rgb(self, sheet_name="", xyxy="", rgb=""):
 		"""
 		셀안의 폰트 색깔을 넣는 것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
@@ -2928,21 +2978,15 @@
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		input_data = self.color.change_scolor_to_rgb(font_color)
 		rgb_to_int = (int(input_data[2])) * (256 ** 2) + (int(input_data[1])) * 256 + int(input_data[0])
 		my_range.Font.Color = rgb_to_int
 
 	def paint_fontcolor(self, sheet_name, xyxy, input_color):
-		sheet_object = self.check_sheet_name(sheet_name)
-		x1, y1, x2, y2 = self.check_address_value(xyxy)
-		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
-
-		rgbvalue = self.color.change_color_to_rgb(input_color)
-		rgb_to_int = (int(rgbvalue[2])) * (256 ** 2) + (int(rgbvalue[1])) * 256 + int(rgbvalue[0])
-		my_range.Interior.Color = rgb_to_int
+		self.paint_font_in_range_by_scolor(sheet_name, xyxy, input_color)
 
 
 	def paint_maxvalue_in_range_in_each_xline(self, sheet_name="", xyxy=""):
 		"""
 		각 x라인별로 최대값에 색칠하는 것
 		"""
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
@@ -3187,18 +3231,14 @@
 		result = self.xlapp.ActiveWorkbook.Name
 		return result
 
 	def read_address_for_rangename(self, sheet_name="", range_name="입력필요"):
 		result = self.read_address_rangename(sheet_name, range_name)
 		return result
 
-	def read_address_for_selection(self):
-		result = self.read_selection_address()
-		return result
-
 	def read_address_for_usedrange(self, sheet_name=""):
 		result = self.read_address_usedrange(sheet_name)
 		return result
 
 	def read_address_in_activecell(self):
 		"""
 		현재 활성화된 셀의 주소를 돌려준다
@@ -3214,29 +3254,44 @@
 		sheet_object = self.check_sheet_name(sheet_name)
 		my_range = sheet_object.Cells(xy[0], xy[1])
 		# self.select_cell(sheet_name, xy)
 		result = self.check_address_value(my_range.CurrentRegion.Address)
 		return result
 
 
-	def read_address_in_selection(self):
+	def read_selection_address(self):
+		#예전자료를 위해서 남겨 놓음
+		result = self.read_address_for_selection()
+		return result
+
+	def read_address_for_selection(self):
 		"""
 		현재선택된 영역의 주소값을 돌려준다
 		"""
 		result = ""
 		temp_address = self.xlapp.Selection.Address
 		temp_list = temp_address.split(",")
 		if len(temp_list) == 1:
 			result = self.check_address_value(temp_address)
 		if len(temp_list) > 1:
 			result = []
 			for one_address in temp_list:
 				result.append(self.check_address_value(one_address))
 		return result
 
+	def read_range_select(self):
+		#예전자료를 위해서 남겨 놓음
+		result = self.read_address_for_selection()
+		return result
+
+	def read_address_in_selection(self):
+		#예전자료를 위해서 남겨 놓음
+		result = self.read_address_for_selection()
+		return result
+
 	def read_address_rangename(self, sheet_name="", range_name="입력필요"):
 		"""
 		rangename의 주소를 돌려주는것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		temp = sheet_object.Range(range_name).Address
 		result = self.check_address_value(temp)
@@ -3349,17 +3404,31 @@
 		"""
 		셀의 색을 돌려주는것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
+		#rgb값으로 출력
 		result = my_range.Interior.Color
 		return result
 
+	def read_color_in_cell_by_excel_56_color_no(self, sheet_name="", xyxy=""):
+		"""
+		셀의 색을 돌려주는것
+		"""
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xyxy)
+		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
+
+		#rgb값으로 출력
+		result = my_range.Interior.ColorIndex
+		return result
+
+
 	def read_coord_in_cell(self, sheet_name, xyxy):
 		"""
 		셀의 픽셀 좌표를 갖고온다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
@@ -3370,39 +3439,28 @@
 		rng_height = my_range.Height
 		return [rng_x_coord, rng_y_coord, rng_width, rng_height]
 
 	def read_filename_for_activeworkbook(self):
 		result = self.read_activeworkbook_filename()
 		return result
 
-	def read_folder_filename_all(self, directory):
-		"""
-		폴더 안의 화일을 읽어오는것
-		"""
-		result = []
-		filenames = os.listdir(directory)
-		for filename in filenames:
-			full_filename = os.path.join(directory, filename)
-			result.append(filename)
-		return result
-
 	def read_fontcolor_in_cell(self, sheet_name="", xyxy=""):
 		"""
 		셀의 폰트 색을 돌려주는것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Cells(x1, y1)
 		result = my_range.Font.Color
 		return result
 
 	def read_fullname_for_workbook(self):
 		return self.xlapp.FullName
 
-	def read_general_value(self):
+	def read_general_inform_for_excel(self):
 		"""
 		몇가지 엑셀에서 자주사용하는 것들정의
 		엑셀의 사용자, 현재의 경로, 화일이름, 현재시트의 이름
 		"""
 		result = []
 		result.append(self.xlapp.ActiveWorkbook.Name)
 		result.append(self.xlapp.Username)
@@ -3437,17 +3495,14 @@
 		for one in self.xlapp.Workbooks:
 			result.append(one.Name)
 		return result
 
 	def read_path_for_workbook(self):
 		return self.xlapp.Path
 
-
-
-
 	def read_pixel_size_in_cell(self, sheet_name, xyxy):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		rng_x_coord = my_range.Left
 		rng_y_coord =my_range.Top
@@ -3469,52 +3524,14 @@
 		if names_count > 0:
 			for aaa in range(1, names_count + 1):
 				name_name = self.xlbook.Names(aaa).Name
 				name_range = self.xlbook.Names(aaa)
 				result.append([aaa, str(name_name), str(name_range)])
 		return result
 
-	def read_selection_address(self):
-		"""
-		영문으로 되어있는 주소를 아라비아숫자로 변경하는 것이다
-		예전이름 : def address_all (self, input_datas)
-		"""
-		input_datas = str(self.xlapp.Selection.Address)
-		input_datas = str(input_datas).lower()
-		arange = str(input_datas).replace("$", "").split(":")
-		if len(arange) == 1:	arange.append(arange[0])
-		if str(arange[0]).lower() in string.ascii_lowercase and str(arange[1]).lower() in string.ascii_lowercase:
-			arange[0] = arange[0] + "0"
-			arange[1] = arange[1] + "65536"
-		if str(arange[0]).lower() in string.digits and str(arange[1]).lower() in string.digits:
-			arange[0] = "a" + arange[0]
-			arange[1] = "iv" + arange[1]
-		result = []
-		for a in arange:
-			if str(a[0]).lower() in string.ascii_lowercase and str(a[1]).lower() in string.ascii_lowercase:
-				result.append(a[0:2])
-				result.append(a[2:])
-			else:
-				result.append(a[0])
-				result.append(a[1:])
-		if result[0]:
-			if len(result[0]) == 1:
-				result[0] = (string.ascii_lowercase.index(result[0]) + 1)
-			else:
-				aaa = (string.ascii_lowercase.index(result[0][0]) + 1) * 26
-				result[0] = aaa + (string.ascii_lowercase.index(result[0][1]) + 1)
-		if result[2]:
-			if len(result[2]) == 1:
-				result[2] = (string.ascii_lowercase.index(result[2]) + 1)
-			else:
-				aaa = (string.ascii_lowercase.index(result[2][0]) + 1) * 26
-				result[2] = aaa + (string.ascii_lowercase.index(result[2][1]) + 1)
-		final_data = [int(result[1]), int(result[0]), int(result[3]), int(result[2])]  # 2005-02-17 추가
-		return final_data
-
 	def read_shape_name_by_shape_no(self, sheet_name,shape_no=""):
 		sheet_object = self.check_sheet_name(sheet_name)
 		result = sheet_object.Shapes(shape_no).Name
 		return result
 
 	def read_shape_name_in_sheet_by_no(self, sheet_name="", shape_no="입력필요"):
 		"""
@@ -3641,14 +3658,21 @@
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		self.get_activesheet_object()
 		self.check_address_value(self.xlapp.Selection.Address)
 		result = my_range.Value
 		return result
 
+	def read_value_in_usedrange(self, sheet_name=""):
+		#usedrange 안의 값을 갖고온다
+		sheet_object = self.check_sheet_name(sheet_name)
+		xyxy = self.check_address_value(sheet_object. UsedRange.address)
+		result = self.read_value_in_range(sheet_name, xyxy)
+		return result
+
 	def read_value_in_xline(self, sheet_name="", xx="입력필요"):
 		"""
 		한줄인 x라인 의 모든값을 읽어온다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, x2 = self.check_xx_address(xx)
 		return sheet_object.Range(sheet_object.Cells(x1, 1), sheet_object.Cells(x1, 1)).EntireRow.Value
@@ -3745,21 +3769,27 @@
 	def rotate_shape(self, sheet_name, shape_obj, degree):
 		# 도형을 회전시키는 것
 		# shape _ obi :이동시킬 도형 이름
 		sheet_object = self.check_sheet_name(sheet_name)
 		oShape = sheet_object.Shapes(shape_obj)
 		oShape.IncrementRotation(degree)
 
-	def run_vba_module(self, vba_code, macro_name):
+
+	def write_vba_module(self, vba_code, macro_name):
 		"""
 		텍스트로 만든 매크로 코드를 실행하는 코드이다
 		"""
-		new_vba_code = "Sub " + macro_name + "()//n" + vba_code + "End Sub"
+		new_vba_code = "Sub " + macro_name + "()" + vba_code + "End Sub"
 		mod = self.xlbook.VBProject.VBComponents.Add(1)
 		mod.CodeModule.AddFromString(new_vba_code)
+
+	def run_vba_module(self, macro_name):
+		"""
+		텍스트로 만든 매크로 코드를 실행하는 코드이다
+		"""
 		self.xlapp.Run(macro_name)
 
 	def save(self, newfilename=""):
 		"""
 		엑셀화일을 저장하는것
 		"""
 		if newfilename == "":
@@ -3844,15 +3874,16 @@
 			for y in range(vars["y1"], vars["y2"] + 1):
 				one_value = vars["sheet"].Cells(y, x).Value
 				if one_value == None:
 					one_value = ""
 				vars["sheet"].Cells(y, x).Value = str(one_value.capitalize())
 
 	def set_cell_color(self, sheet_name, xy, input_color="입력필요"):
-		self.paint_cell_by_scolor(sheet_name, xy, input_color)
+		excel_no = self.paint_cell_by_excel_colorno(sheet_name, xy, input_color)
+		#self.paint_cell_by_scolor(sheet_name, xy, excel_no)
 
 	def set_color_bar_by_no(self, sheet_name, xyxy, color_value=255):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		my_range.FormatConditions.AddDatabar
@@ -3884,25 +3915,31 @@
 		영역에 글씨체를 설정한다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.Font.Name = font
 
+	def paint_fontcolor_in_cell(self, sheet_name="", xy="", font_color=""):
+		self.set_fontcolor_in_cell(sheet_name, xy, font_color)
+
 	def set_fontcolor_in_cell(self, sheet_name="", xy="", font_color=""):
 		"""
 		셀에 글씨체를 설정한다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xy)
 		rgb_value = self.check_inputcolor_rgb(font_color)
 		rgb_int = self.color.change_rgb_to_rgbint(rgb_value)
 		my_range = sheet_object.Cells(x1, y1)
 		my_range.Font.Color = rgb_int
 
+	def paint_fontcolor_in_range(self, sheet_name="", xyxy="", font_color=""):
+		self.set_fontcolor_in_range(sheet_name, xyxy, font_color)
+
 	def set_fontcolor_in_range(self, sheet_name="", xyxy="", font_color=""):
 		"""
 		영역에 글씨체를 설정한다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
@@ -3957,16 +3994,14 @@
 
 	def set_height_in_range(self, sheet_name, xyxy, height=13.5):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.RowHeight = height
 
-
-
 	def set_height_in_xxline(self, sheet_name, xx, height=13.5):
 		"""
 		가로줄의 높이를 설정
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		my_range = sheet_object.Range(sheet_object.Cells(xx[0], 1), sheet_object.Cells(xx[1], 1))
 		my_range.RowHeight = height
@@ -3983,37 +4018,33 @@
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		for x in range(x1, x2 + 1):
 			for y in range(y1, y2 + 1):
 				value = sheet_object.Cells(y, x).Value
 				sheet_object.Cells(y, x).Value = str(value.lstrip())
 
-
 	def set_merge_in_range(self, sheet_name="", xyxy=""):
 		"""
 		셀들을 병합하는 것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.Merge(0)
 
 	def set_name_in_range(self, name):
 		self.xlbook.Names.Add(name, vars["range"])
 
-
 	def set_numberformat(self, sheet_name, xyxy, numberformat):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		my_range.NumberFormat = numberformat
 
-
-
 	def set_numberformat_in_cell(self, sheet_name="", xyxy="", numberformat="#,##0.00_ "):
 		self.set_numberformat_in_range(sheet_name, xyxy, numberformat)
 
 	def set_numberformat_in_range(self, sheet_name="", xyxy="", numberformat="#,##0.00_ "):
 		"""
 		영역에 숫자형식을 지정하는 것
 		"""
@@ -4069,14 +4100,17 @@
 		sheet_object.PageSetup.LeftFooter = "&D"  # 날짜
 		sheet_object.PageSetup.LeftHeader = "&T"  # 시간
 		sheet_object.PageSetup.CenterHeader = "&F"  # 화일명
 		sheet_object.PageSetup.CenterFooter = "&P/&N"  # 현 page/ 총 page
 		sheet_object.PageSetup.RightHeader = "&Z"  # 화일 경로
 		sheet_object.PageSetup.RightFooter = "&P+33"  # 현재 페이지 + 33
 
+	def set_range_nocolor(self, sheet_name, xyxy):
+		self.delete_color_in_range(sheet_name, xyxy)
+
 	def set_rangename(self, sheet_name="", xyxy="", name=""):
 		"""
 		rangename을 설정하는 것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
@@ -4086,15 +4120,14 @@
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		for x in range(x1, x2 + 1):
 			for y in range(y1, y2 + 1):
 				value = sheet_object.Cells(y, x).Value
 				sheet_object.Cells(y, x).Value = str(value.rstrip())
 
-
 	def set_strikethrough_in_range(self, sheet_name, xyxy):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 
 		my_range.Font.Strikethrough = True
 
@@ -4127,23 +4160,32 @@
 		영역안의 병합된 것을 푸는 것이다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
 		my_range.UnMerge()
 
+
+	def set_unmerge_in_sheet(self, sheet_name=""):
+		"""
+		시트안의 모든 영역의 병합된 것을 푸는 것이다
+		"""
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.read_address_for_usedrange(sheet_name)
+		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
+		my_range.UnMerge()
+
 	def set_upper_in_range(self, sheet_name, xyxy):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		for x in range(x1, x2 + 1):
 			for y in range(y1, y2 + 1):
 				value = sheet_object.Cells(y, x).Value
 				sheet_object.Cells(y, x).Value = str(value.upper())
 
-
 	def set_visible_for_sheet(self, input_data=0):
 		"""
 		시트를 감추는것
 		"""
 		self.xlapp.Visible = input_data
 
 	def set_visible_for_workbook(self, value=1):
@@ -4151,36 +4193,28 @@
 		실행되어있는 엑셀을 화면에 보이지 않도록 설정합니다
 		기본설정은 보이는 것으로 되너 있읍니다
 		"""
 		self.xlapp.Visible = value
 
 	def set_width_in_yyline(self, sheet_name, yy, width=5):
 		"""
-		가로줄의 높이를 설정
+		가로줄의 넓이를 설정
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		my_range = sheet_object.Range(sheet_object.Cells(1, yy[0]), sheet_object.Cells(1, yy[1]))
 		my_range.ColumnWidth = width
 
 	def set_wrap_in_range(self, sheet_name="", xyxy="", input_data=""):
 		"""
 		셀의 줄바꿈을 설정할때 사용한다
 		만약 status를 false로 하면 줄바꿈이 실행되지 않는다.
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		sheet_object.Range(xyxy).WrapText = input_data
 
-	def set_xx_width(self, sheet_name, xyxy, width=13.5):
-		sheet_object = self.check_sheet_name(sheet_name)
-		x1, y1, x2, y2 = self.check_address_value(xyxy)
-		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
-
-		my_range.ColumnWidth = width
-
-
 	def show_messagebox_with_value(self, input_text="입력필요", input_title="pcell"):
 		"""
 		메세지박스를 보여주는것
 		"""
 		win32gui.MessageBox(0, input_text, input_title, 0)
 
 	def sound_beep(self, sec = 1000, hz = 500):
@@ -4242,14 +4276,18 @@
 			if len(result[x_no]) > length:
 				for a in range(len(result[x_no]) - length):
 					self.insert_xline("", x1 + length)
 				length = len(result[x_no])
 			for x_no in range(len(result[x_no])):
 				sheet_object.Cells(x1 + x_no, y1 + y_no + 1).Value = result[x_no][y_no]
 
+	def split_value_to_str_num(self, input_text):
+		re_com_num = re.compile("[a-zA-Z]+|\d+")
+		result = re_com_num.findall(input_text)
+		return result
 	def swap_cap_small(self, sheet_name="", xyxy=""):
 		""" 영역안의 값을 대/소문자를 바꾸는 것 """
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		for y in range(y1, y2 + 1):
 			for x in range(x1, x2 + 1):
 				temp_data = self.read_cell_value(sheet_name, [x, y])
 				self.write_cell_value(sheet_name, [x, y], str(temp_data).swapcase())
@@ -4261,15 +4299,14 @@
 		return result
 
 	def unlock_sheet(self, sheet_name="", password="1234"):
 		""" 시트 보호를 설정 하는 것 """
 		sheet_object = self.check_sheet_name(sheet_name)
 		sheet_object.Unprotect(password)
 
-
 	def vlookup_with_multi_line(self, input_data1, input_data2):
 		"""
 		보통 vlookup은 한줄을 비교해서 다른 자료를 찾는데
 		이것은 여러항목이 같은 값을 기준으로 원하는 것을 찾는 것이다
 		input_datal = [자료의영역, 같은것이있는위치, 결과값의위치]
 		"""
 		base_data2d = self.read_value_in_range("", input_data1[0])
@@ -4289,17 +4326,17 @@
 
 				for no in input_data2[1]:
 					bikyo.append(value_1d[no-1])
 
 				if gijun == bikyo:
 					result = one_data_1[input_data1[2] - 1]
 				self.write_value_in_cell("", [x, input_data2[2]], result)
+
 	def write_cell_value(self, sheet_name="", xyxy="", value="입력필요"):
-		"""
-		"""
+		#예전자료를 위한것
 		self.write_value_in_cell(sheet_name, xyxy, value)
 
 	def write_df_to_excel(self, sheet_name="", df_obj="입력필요", xyxy=[1, 1]):
 		"""
 		dataframe의 자료를 엑셀로 넘기는 것
 		"""
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
@@ -4316,14 +4353,17 @@
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		changed_input_datas = list(input_dic.keys())
 
 		for x in range(0, len(changed_input_datas)):
 			sheet_object.Cells(x + x1, y1).Value = changed_input_datas[x]
 
+	def write_formula_in_range(self, sheet_name, xyxy, input_data="=Now()"):
+		self.write_range_formula(sheet_name, xyxy, input_data)
+
 	def write_list1d_in_range(self, sheet_name="", xyxy="", input_list="입력필요"):
 		"""
 		1줄의 리스트는 가로로 나열된다
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		if x1==x2 and y1==y2:
@@ -4340,17 +4380,15 @@
 		#영역에 값는 넣기
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		for x in range(0, len(input_datas)):
 			sheet_object.Cells(x + x1, y1).Value = input_datas[x]
 
 	def write_list2d_in_range(self, sheet_name="", xyxy="", input_list="입력필요"):
-		"""
-		"""
-		self.write_list_in_range(sheet_name="", xyxy="", input_list="입력필요")
+		self.write_list_in_range(sheet_name, xyxy, input_list)
 
 	def write_list_in_range(self, sheet_name="", xyxy="", input_list="입력필요"):
 		"""
 		2차원의 값만 입력할 수 있다
 		"""
 		if type(input_list[0]) == type([]):
 			self.write_value_in_range(sheet_name, xyxy, input_list)
@@ -4358,23 +4396,23 @@
 			self.write_value_in_range(sheet_name, xyxy, [input_list])
 
 	def write_memo_in_cell(self, sheet_name="", xyxy="", text="입력필요"):
 		"""
 		셀에 메모를 넣는것
 		"""
 		sheet_object = self.check_sheet_name(sheet_name)
-		x1, y1, x2, y2 = self.check_address_value(xyxy)
-		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
+		r1c1 = self.change_xyxy_to_r1c1(xyxy)
+		#x1, y1, x2, y2 = self.check_address_value(xyxy)
+		my_range = sheet_object.Range(r1c1)
 
 		my_range.AddComment(text)
 
 	def write_messagebox_value(self, input_text, input_title="pcell"):
 		win32gui.MessageBox(0, input_text, input_title, 0)
 
-
 	def write_nansu_in_range(self, sheet_name="", xyxy="", input_list=[1,100]):
 		"""
 		입력한 숫자범위에서 난수를 만들어서 영역에 써주는것
 		"""
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 
 		no_start, no_end = input_list
@@ -4390,29 +4428,44 @@
 				else:
 					temp_no = temp_no + 1
 
 	def write_range_formula(self, sheet_name, xyxy, input_data="=Now()"):
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
-
 		my_range.Formula = input_data
-	def write_serial_no_by_step(self, xyxy, start_no, step = 1):
+
+	def write_serial_no(self, sheet_name, xyxy, start_no=1, step=1):
+		new_no = start_no
+		for no in range(0, xyxy[2] - xyxy[0] + 1):
+			self.write_value_in_cell(sheet_name, [xyxy[0] + no, xyxy[1]], new_no)
+			new_no = new_no + step
+
+	def write_serial_no_by_step_to_y_line(self, xyxy, start_no=1, step = 1):
+		"""
+		선택한 영역에 시작번호, 간격으로 이루어진 연속된 숫자를 쓰는것
+		예 :  0,2,4,6,8....
+		"""
+		new_no = start_no
+		for no in range(0, xyxy[2]-xyxy[0]+1):
+			self.write_value_in_cell("", [xyxy[0], xyxy[1]+no], new_no)
+			new_no = new_no + step
+
+	def write_serial_no_by_step(self, xyxy, start_no=1, step = 1):
 		"""
 		선택한 영역에 시작번호, 간격으로 이루어진 연속된 숫자를 쓰는것
 		"""
 		new_no = start_no
 		for no in range(0, xyxy[2]-xyxy[0]+1):
 			self.write_value_in_cell("", [xyxy[0]+no, xyxy[1]], new_no)
 			new_no = new_no + step
 			#print([xyxy[0]+no, xyxy[1]], new_no)
 
 	def write_value_in_activecell(self, value="입력필요"):
 		""" 활성화된 셀에 값는 넣기 """
-		self.get_activesheet_object()
 		xy = self.read_address_in_activecell()
 		self.write_value_in_cell("", [xy[0], xy[1]], value)
 
 	def write_value_in_cell(self, sheet_name="", xyxy="", value="입력필요"):
 		""" 셀에 값는 넣기 """
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
@@ -4427,15 +4480,18 @@
 			else:
 				changed_value = value
 		else:
 			changed_value = value
 		sheet_object.Cells(x1, y1).Value = changed_value
 
 	def write_value_in_range(self, sheet_name="", xyxy="", input_datas="입력필요"):
-		""" 영역에 값는 넣기 """
+		"""
+		영역에 값는 넣기
+		이것은 하나하나 입력이 되는 모습을 보여주며서, 실행되는 것이다
+		"""
 		sheet_object = self.check_sheet_name(sheet_name)
 		x1, y1, x2, y2 = self.check_address_value(xyxy)
 		changed_input_datas = self.change_inputdata_to_list2d(input_datas)
 
 		for x in range(0, len(changed_input_datas)):
 			for y in range(0, len(changed_input_datas[x])):
 				sheet_object.Cells(x + x1, y + y1).Value = changed_input_datas[x][y]
@@ -4509,25 +4565,22 @@
 					if divmod(y, xystep[1])[1] == 0:
 						sheet_object.Cells(x, y).Value = str(input_text)
 
 	def write_value_to_left(self, input_text=""):
 		cell_value = vars["cell"].Value
 		vars["cell"].Value = str(input_text) + str(cell_value[0])
 
-	def make_xy_list_for_box_style(self, xyxy):
-		# 좌표를 주면, 맨끝만 나터내는 좌표를 얻는다
-		temp_1 = []
-		for x in [xyxy[0], xyxy[2]]:
-			temp = []
-			for y in range(xyxy[1], xyxy[3] + 1):
-				temp.append([x, y])
-			temp_1.append(temp)
-
-		temp_2 = []
-		for y in [xyxy[1], xyxy[3]]:
-			temp = []
-			for x in range(xyxy[0], xyxy[2] + 1):
-				temp.append([x, y])
-			temp_2.append(temp)
-
-		result = [temp_1[0], temp_2[1], temp_1[1], temp_2[0]]
+	def read_value_in_range_with_xy_headers(self, sheet_name, xyxy):
+		# 영역의 값을 갖고온다. 맨앞과 위에 번호로 행과열을 추가한다
+		# 가끔은 자료중에서 필요없는것을 삭제했더니, 원래 있었던 자료의 위치를 알수가 없어서, 만들어 본것임
+		sheet_object = self.check_sheet_name(sheet_name)
+		x1, y1, x2, y2 = self.check_address_value(xyxy)
+		top_line = list(range(y1 - 1, y2 + 1))
+		my_range = sheet_object.Range(sheet_object.Cells(x1, y1), sheet_object.Cells(x2, y2))
+		all_data = list(my_range.Value)
+		result = []
+		for x in range(0, x2 - x1 + 1):
+			temp = [+x1]
+			temp.extend(list(all_data[x]))
+			result.append(temp)
+		result.insert(0, top_line)
 		return result
```

### Comparing `xython-1.4.0/src/xython/pcell_event.py` & `xython-1.5.0/src/xython/pcell_event.py`

 * *Files identical despite different names*

### Comparing `xython-1.4.0/src/xython/pyclick.py` & `xython-1.5.0/src/xython/pyclick.py`

 * *Files identical despite different names*

### Comparing `xython-1.4.0/src/xython/pynal.py` & `xython-1.5.0/src/xython/pynal.py`

 * *Files 8% similar despite different names*

```diff
@@ -8,18 +8,20 @@
 import basic_data  # xython 모듈
 
 from korean_lunar_calendar import KoreanLunarCalendar
 
 class pynal():
 	"""
 	시간을 다루기 위한 모듈
+	기본적으로 날짜의 변환이 필요한 경우는 utc 시간을 기준으로 변경하도록 하겠읍니다
+	datetime 객체를 기준으로 하요도 된다
+	주일의 시작은 월요일이다
 	"""
 
 	def __init__(self):
-		# 기본적으로 날짜의 변환이 필요한 경우는 utc 시간을 기준으로 변경하도록 하겠읍니다
 		self.jf = jfinder.jfinder()
 		self.lunar_calendar = KoreanLunarCalendar()
 		self.base_data = basic_data.basic_data()
 		self.var = self.base_data.vars
 		self.var_common={"timezone": "seoul", "week_no_7_start": 0}
 
 	def change_any_text_time_to_dt_obj(self, input_string):
@@ -301,15 +303,15 @@
 			result = datetime(result["year"], result["mon"], result["day"], result["hour"], result["min"],
 			                  result["sec"])
 		except:
 			result = "error"
 
 		return result
 
-	def change_any_time_to_dt_obj(self, input_time):
+	def change_input_time_to_dt_obj(self, input_time):
 		"""
 		어떤 시간의 형태로된 문자열을 날짜 객체로 만드는 것
 		"""
 		result = self.check_input_time(input_time)
 		return result
 
 	def change_dt_obj_to_text_time_as_input_format(self, dt_obj, input_format):
@@ -361,21 +363,21 @@
 		result = utf_time.timestamp()
 		return result
 
 	def change_dt_obj_to_ymd_list(self, input_time):
 		"""
 		날짜객체를 년월일의 리스트로 돌려주는 것
 		"""
-		utc_time = self.check_input_time(input_time)
-		utc_str = self.change_dt_obj_to_text_time_set_as_dic(utc_time)
+		utc = self.check_input_time(input_time)
+		utc_str = self.change_dt_obj_to_text_time_set_as_dic(utc)
 		result = [int(utc_str["yyyy"]), int(utc_str["mm"]), int(utc_str["dd"])]
 		return result
 
-	def change_iso_format_to_dt_obj(self, input_data):
-		dt_obj = datetime.fromisoformat(input_data)
+	def change_iso_format_to_dt_obj(self, input_iso_format):
+		dt_obj = datetime.fromisoformat(input_iso_format)
 		return dt_obj
 
 
 	def change_excel_time_to_dt_obj(self):
 		# 1900년 1월1일을 0으로하여 계산하는 엑셀의 시간을 dt_obj로 만드는것
 		pass
 
@@ -386,15 +388,15 @@
 
 		date	 : 2000-01-01
 		datelist : [2000, 01, 01]
 		ymd_list : [2000, 01, 01]
 		time	 : 시간의 여러형태로 입력을 하면, 이에 맞도록 알아서 조정한다
 		dhms	 : 2일3시간10분30초, day-hour-minute-sec
 		hms_list  : [시, 분, 초]
-		utc_time  : 1640995200.0 또는 "", 1648037614.4801838 (의미 : 2022-03-23T21:13:34.480183+09:00)
+		utc  : 1640995200.0 또는 "", 1648037614.4801838 (의미 : 2022-03-23T21:13:34.480183+09:00)
 		utc : 1970년 1월 1일을 0밀리초로 계산한 것
 		move	 : 입력값에 더하거나 빼서 다른 값으로 바꾸는것, 입력값과 출력값이 다를때 (출력값을 입력의 형태로 바꾸면 값이 다른것)
 		change   : 형태를 바꾼것
 		read	 : 입력값을 원하는 형태로 변경해서 갖고오는것
 		get	  : 입력값에서 원하는 형태의 값을 갖고오는것
 		shift	: 현재의 값을 같은 형태에서 값을 이동시키는것
 		class datetime.datetime(year, month, day, hour=0, minute=0, second=0, microsecond=0, tzinfo=None, *, fold=0)
@@ -419,45 +421,49 @@
 		total_sec = int(result[0]) * 3600 + int(result[1]) * 60 + int(result[2])
 		return total_sec
 
 	def change_input_time_to_ymd_style(self, input_time, connect_str="-"):
 		"""
 		입력시간을 년월일을 특수 문자로 연결하여 돌려주는 것
 		"""
-		utc_time = self.check_input_time(input_time)
-		utc_str = self.change_dt_obj_to_text_time_set_as_dic(utc_time)
+		utc = self.check_input_time(input_time)
+		utc_str = self.change_dt_obj_to_text_time_set_as_dic(utc)
 		result = utc_str["yyyy"] + connect_str + utc_str["mm"] + connect_str + utc_str["dd"]
 		return result
 
-	def change_dt_obj_to_ymd_style(self, input_dt_obj, connect_str="-"):
+	def change_dt_obj_to_ymd_style_with_connect_char(self, input_dt_obj, connect_str="-"):
+		"""입력문자를 기준으로 yyyy-mm-dd이런 스타일로 만드는 것이다"""
 		utc_str = self.change_dt_obj_to_text_time_set_as_dic(input_dt_obj)
 		result = utc_str["yyyy"] + connect_str + utc_str["mm"] + connect_str + utc_str["dd"]
 		return result
 
-	def change_iso_format_string_to_dt_obj(self, input_time):
+	def change_iso_format_string_to_dt_obj(self, input_iso_format):
 		"""
 		datetime.isoformat('2011-11-04 00:05:23.283+00:00')
 		"""
-		result = datetime.isoformat(input_time)
+		result = datetime.isoformat(input_iso_format)
 		return result
 
 	def change_linux_time_to_dt_obj(self):
-		# 1970년 1월1일을 0으로하여 계산하는 리눅스의 시간을 dt_obj로 만드는것
+		"""1970년 1월1일을 0으로하여 계산하는 리눅스의 시간을 dt_obj로 만드는것"""
 		pass
 
 	def change_lunar_to_solar(self, input_ymd_list, yoon_or_not=True):
+		"""음력을 양력으로 만들어 주는것"""
 		self.lunar_calendar.setLunarDate(int(input_ymd_list[0]), int(input_ymd_list[1]), int(input_ymd_list[2]),
 		                                 yoon_or_not)
 		dt_obj = self.change_any_text_time_to_dt_obj(self.lunar_calendar.SolarIsoFormat())
 		result = self.change_dt_obj_to_ymd_list(dt_obj)
 		return result
 
 	def change_next_day_for_sunday(self, holiday_list, input_2dlist):
-		# 대체공휴일을 확인하는것
-		# 일요일인것만, 리스트로 만들어 준다
+		"""
+		대체공휴일을 확인하는것
+		일요일인것만, 리스트로 만들어 준다
+		"""
 		result = []
 		if holiday_list == "all":
 			for list_1d in input_2dlist:
 				temp = []
 				sunday = 0
 				for one in list_1d:
 					if one[3] == 0:    sunday = 1
@@ -533,137 +539,137 @@
 	def change_timestamp_to_utc(self, input_time):
 		"""
 		숫자형으로된 시간을 utc로 바꾸는 것
 		"""
 		result = time.gmtime(input_time)
 		return result
 
-	def change_utc_time_to_day_list(self, input_data=""):
+	def change_utc_to_day_list(self, input_time=""):
 		"""
 		입력값 : utf시간숫자, 1640995200.0 또는 ""
 		일 -----> ['05']
 		닞은숫자 -> 많은글자 순으로 정리
 		"""
-		utc_local_time = self.check_input_time(input_data)
+		utc_local_time = self.check_input_time(input_time)
 		day = time.strftime('%d', utc_local_time)
 		day_l = time.strftime('%j', utc_local_time)
 		result = [day, day_l]
 		return result
 
-	def change_utc_time_to_dt_obj(self, input_data=""):
+	def change_utc_to_dt_obj(self, input_time=""):
 		"""
 		입력값 : utf시간숫자, 1640995200.0 또는 ""
 		분 -----> ['07']
 		닞은숫자 -> 많은글자 순으로 정리
 		"""
-		result = self.check_input_time(input_data)
+		result = self.check_input_time(input_time)
 		return result
 
-	def change_utc_time_to_hour_list(self, input_data=""):
+	def change_utc_to_hour_list(self, input_time=""):
 		"""
 		입력값 : utf시간숫자, 1640995200.0 또는 ""
 		시 -----> ['10', '22']
 		닞은숫자 -> 많은글자 순으로 정리
 		"""
-		utc_local_time = self.check_input_time(input_data)
+		utc_local_time = self.check_input_time(input_time)
 		hour = time.strftime('%I', utc_local_time)
 		hour_l = time.strftime('%H', utc_local_time)
 		result = [hour, hour_l]
 		return result
 
-	def change_utc_time_to_min_list(self, input_data=""):
+	def change_utc_to_min_list(self, input_time=""):
 		"""
 		입력값 : utf시간숫자, 1640995200.0 또는 ""
 		분 -----> ['07']
 		닞은숫자 -> 많은글자 순으로 정리
 		"""
-		utc_local_time = self.check_input_time(input_data)
+		utc_local_time = self.check_input_time(input_time)
 		min = time.strftime('%M', utc_local_time)
 		result = [min]
 		return result
 
-	def change_utc_time_to_month_list(self, input_data=""):
+	def change_utc_to_month_list(self, input_time=""):
 		"""
 		입력값 : utf시간숫자, 1640995200.0 또는 ""
 		월 -----> ['04', Apr, April]
 		닞은숫자 -> 많은글자 순으로 정리
 		"""
-		utc_local_time = self.check_input_time(input_data)
+		utc_local_time = self.check_input_time(input_time)
 		mon = time.strftime('%m', utc_local_time)
 		mon_e = time.strftime('%b', utc_local_time)
 		mon_e_l = time.strftime('%B', utc_local_time)
 		result = [mon, mon_e, mon_e_l]
 		return result
 
-	def change_utc_time_to_sec_list(self, input_data=""):
+	def change_utc_to_sec_list(self, input_time=""):
 		"""
 		입력값 : utf시간숫자, 1640995200.0 또는 ""
 		초 -----> ['48']
 		닞은숫자 -> 많은글자 순으로 정리
 		"""
-		utc_local_time = self.check_input_time(input_data)
+		utc_local_time = self.check_input_time(input_time)
 		sec = time.strftime('%S', utc_local_time)
 		result = [sec]
 		return result
 
-	def change_utc_time_to_week_list(self, input_data=""):
+	def change_utc_to_week_list(self, input_time=""):
 		"""
 		입력값 : utf시간숫자, 1640995200.0 또는 ""
 		주 -----> ['5', '13', 'Fri', 'Friday']
 		닞은숫자 -> 많은글자 순으로 정리
 		"""
-		utc_local_time = self.check_input_time(input_data)
+		utc_local_time = self.check_input_time(input_time)
 		week_no_7 = time.strftime('%w', utc_local_time)
 		week_no_year = time.strftime('%W', utc_local_time)
 		week_e = time.strftime('%a', utc_local_time)
 		week_e_l = time.strftime('%A', utc_local_time)
 		result = [week_no_7, week_no_year, week_e, week_e_l]
 		return result
 
-	def change_utc_time_to_weekno(self, input_data=""):
+	def change_utc_to_yearweekno(self, input_time=""):
 		"""
 		시간이 들어온면
 		입력값 : 년도, 위크번호
 		한 주의 시작은 '월'요일 부터이다
 		"""
-		lt = self.check_input_time(input_data)
+		lt = self.check_input_time(input_time)
 		result = time.strftime('%W', lt)  # 34, 1년중에 몇번째 주인지
 		return result
 
-	def change_utc_time_to_year_list(self, input_data=""):
+	def change_utc_to_year_list(self, input_time=""):
 		"""
 		년 -----> ['22', '2022']
 		닞은숫자 -> 많은글자 순으로 정리
 		"""
-		utc_local_time = self.check_input_time(input_data)
+		utc_local_time = self.check_input_time(input_time)
 		year_s = time.strftime('%y', utc_local_time)
 		year = time.strftime('%Y', utc_local_time)
 		result = [year_s, year]
 		return result
 
-	def change_utc_time_to_ymd_dash(self, input_data=""):
+	def change_utc_to_ymd_dash(self, input_data=""):
 		"""
 		utc를 2023-2-2형태로 돌려주는 것
 		"""
 		lt = self.change_any_text_time_to_dt_obj(input_data)
 		result = lt.format("YYYY-MM-DD")
 		return result
 
-	def change_utc_time_to_ymd_list(self, input_data=""):
+	def change_utc_to_ymd_list(self, input_time=""):
 		"""
 		"""
-		utc_local_time = self.check_input_time(input_data)
+		utc_local_time = self.check_input_time(input_time)
 		year = time.strftime('%Y', utc_local_time)
 		month = time.strftime('%m', utc_local_time)
 		day = time.strftime('%d', utc_local_time)
 		result = [year, month, day]
 		return result
 
-	def change_utc_timeformat(self, input_utc_time, format_a):
-		result = time.strftime(format_a, input_utc_time)
+	def change_utc_by_format(self, input_utc, input_format):
+		result = time.strftime(input_format, input_utc)
 		return result
 
 	def change_utc_timestamp_to_dt_obj(self, input_timestamp):
 		"""
 		입력값 : utf시간숫자, 1640995200.0 또는 ""
 		날짜객체로 만들어 주는 것
 		"""
@@ -924,49 +930,50 @@
 					holiday_no = int(ymd_list_sun[0]) * 10000 + int(ymd_list_sun[1]) * 100 + int(ymd_list_sun[2])
 
 					if base_start_no <= holiday_no and base_end_no >= holiday_no and one_holiday[0][0] <= holiday_no and \
 							one_holiday[0][1] >= holiday_no:
 						result_sun.append(ymd_list_sun + one_holiday[1])
 		return result_sun
 
-	def delta_hms_list_1_and_hms_list_2(self, input_hms_1, input_hms_2):
+	def delta_two_hms_list(self, input_hms_1, input_hms_2):
 		"""
 		hms_list : [시, 분, 초]
 		두 시간에 대한 차이를 hms 형태로 돌려주는 것
 		"""
 		sec_1 = self.change_hms_list_to_sec(input_hms_1)
 		sec_2 = self.change_hms_list_to_sec(input_hms_2)
 		delta_sec = abs(int(sec_2 - sec_1))
 		result = self.change_sec_to_hms_list(delta_sec)
 		return result
 
-	def get_7_days_list_for_weekno(self, year, week_no_year):
+	def get_7_days_list_for_yearweekno(self, year, week_no_year):
 		"""
-		일요일부터 시작하는 7 개의 날짜를 돌려준다
+		월요일부터 시작하는 7 개의 날짜를 돌려준다
 		"""
 		str_datetime = f'{year} {week_no_year} 0'
+		#문자열형태로 입력받아서, 시간객체로 만들어 주는것
 		startdate = datetime.strptime(str_datetime, '%Y %W %w')
-		dates = [startdate.strftime("%Y-%m-%d")]
-		for i in range(1, 7):
+		dates = []
+		for i in range(1, 8):
 			day = startdate + timedelta(days=i)
 			dates.append(day.strftime("%Y-%m-%d"))
 		return dates
 
-	def get_monday_for_week_no_year(self, year, week_no):
+	def get_monday_for_year_yearweekno(self, year, yearweekno):
 		"""
 		입력값 : 년도, 위크번호
 		한 주의 시작은 '월'요일 부터이다
 		"""
 
 		utc_local_time = self.check_input_time([year, 1, 1])
 		base = 1 if utc_local_time.isocalendar()[1] == 1 else 8
-		temp = utc_local_time + datetime.timedelta(days=base - utc_local_time.isocalendar()[2] + 7 * (int(week_no) - 1))
+		temp = utc_local_time + datetime.timedelta(days=base - utc_local_time.isocalendar()[2] + 7 * (int(yearweekno) - 1))
 		days = str(temp).split("-")
 
-		# input_utf_time_no = nal.change_ymd_list_to_utc_time([2022, 1, 1])
+		# input_utf_time_no = nal.change_ymd_list_to_utc([2022, 1, 1])
 		#return [str(temp), temp, input_utf_time_no]
 
 	def get_last_day_for_text_time(self, input_time):
 		"""
 		입력한 날의 월의 마지막 날짜를 계산
 		입력받은 날자에서 월을 1나 늘린후 1일을 마이너스 한다
 		예 : 2023-04-19 -> 2023-05-01 ->  2023-05-01 - 1일 -> 2023-04-30
@@ -991,15 +998,15 @@
 		출력 : [날짜객체, [1,31], 1, 31]
 		"""
 		date = datetime(year=input_ymlist[0], month=input_ymlist[1], day=1).date()
 		monthrange = calendar.monthrange(date.year, date.month)
 		last_day = calendar.monthrange(date.year, date.month)[1]
 		return last_day
 
-	def get_last_day_of_month_for_ym_list(self, input_list=[2002, 3]):
+	def get_last_day_for_ym_list_1(self, input_list=[2002, 3]):
 		"""
 		입력값 : datetime.date(2012, month, 1)
 		결과값 : 원하는 년과 월의 마지막날을 알아내는것
 		"""
 		any_day = datetime.date(input_list[0], input_list[1], 1)
 		next_month = any_day.replace(day=28) + timedelta(days=4)  # this will never fail
 		result = next_month - timedelta(days=next_month.day)
@@ -1029,15 +1036,18 @@
 		현재의 시간을 utc로 바꿉니다
 		"""
 		time_stamp = time.time()
 		result = time.gmtime(time_stamp)
 		return result
 
 	def get_one_week_no_7_for_dt_obj(self, input_dt_obj):
-		# 날짜객체의 week_no_7을 알아내는것
+		"""
+		날짜객체의 week_no_7을 알아내는것
+		주의 7번째요일인 일요일의 날짜를 돌려줍니다
+		"""
 		result = input_dt_obj.strftime('%w')  # 6
 		return result
 
 	def get_time_format(self, input_time=""):
 		self.check_input_time(input_time)
 		return self.var_common["utc"]
 
@@ -1065,66 +1075,72 @@
 		날짜와 시간(datetime) -> 문자열로 : strftime
 		날짜와 시간 형식의 문자열을 -> datetime으로 : strptime
 		"""
 		dt_obj = datetime.now()
 		result = dt_obj.strftime("%Y-%m-%d")
 		return result
 
-	def get_week_no_7_for_1st_day_of_ym_list(self, input_ymlist):
+	def get_week_no_for_1st_day_of_ym_list(self, input_ymlist):
 		"""
+		week_no : 1~7까지의 요일에 대한 숫자
+		입력한 월의 1일이 무슨요일인지 알아 내는것
 		입력 : [2023, 05]
 		출력 : 0 ==> 월요일
 		"""
 		date = datetime(year=input_ymlist[0], month=input_ymlist[1], day=1).date()
 		monthrange = calendar.monthrange(date.year, date.month)
 		first_day = calendar.monthrange(date.year, date.month)[0]
 		return first_day
 
-	def get_week_no_7_for_dt_obj(self, input_dt_obj):
-		# 요일에대한 숫자를, 일요일이 0이다
+	def get_week_no_for_dt_obj(self, input_dt_obj):
+		"""
+		week_no : 1~7까지의 요일에 대한 숫자
+		요일에대한 숫자를, 일요일이 0이다
+		"""
 		result = input_dt_obj.strftime('%w')
-		# print("요일의 번호는 ==>" , result)
+		print("요일의 번호는 ==>", result)
 		return result
 
-	def get_weekno_for_ymd_list(self, input_date=""):
+	def get_yearweekno_for_ymd_list(self, input_date=""):
 		"""
+		yearweekno : 1년에서 몇번째 주인지 아는것
 		입력한날의 week 번호를	계산
 		입력값 : 날짜
 		"""
 		if input_date == "":
 			today = self.get_today_as_yyyy_mm_dd_style()
 			print(today)
 			year, month, day = today.split("-")
 			utc_local_time = self.check_input_time([year, month, day])
 		else:
 			utc_local_time = self.change_any_text_time_to_dt_obj(input_date)
 		result = int(utc_local_time.strftime("%W"))
 		return result
 
-	def get_ymd_of_monday_for_week_no_7(self, year, week_no_7):
+	def get_ymd_of_monday_for_week_no(self, year, week_no_7):
 		"""
 		입력값 : 년도, 위크번호
 		한 주의 시작은 '월'요일 부터이다
 		"""
 		first = date(year, 1, 1)
 		base = 1 if first.isocalendar()[1] == 1 else 8
 		temp = first + timedelta(days=base - first.isocalendar()[2] + 7 * (int(week_no_7) - 1))
 		days = str(temp).split("-")
 
-	# input_utf_time_no = nal.change_ymd_utc_time([2022, 1, 1])
+	# input_utf_time_no = nal.change_ymd_utc([2022, 1, 1])
 	# return [str(temp), temp, input_utf_time_no]
 
 	def holiday_nation(self):
 		"""
 		휴일기준
 		"""
 		self.var_common["holiday_common"] = ["0101", "0301", "0505", "0606", "0815", "1001", "1225", 1.3]
 		self.var_common["holiday_company"] = ["0708"]
 
-	def make_time_list_by_step(self, start_hsm_list, step=30, cycle=20):
+	def make_time_list_for_hsm_list_by_step_cycle(self, start_hsm_list, step=30, cycle=20):
 		"""
 		시작과 종료시간을 입력하면, 30분간격으로 시간목록을 자동으로 생성시키는것
 		"""
 		result = []
 		hour, min, sec = start_hsm_list
 		result.append([hour, min, sec])
 		for one in range(cycle):
@@ -1132,15 +1148,15 @@
 			over_min, min = divmod(min, 60)
 			if over_min > 0:
 				hour = hour + over_min
 			hour = divmod(hour, 24)[1]
 			result.append([hour, min, sec])
 		return result
 
-	def make_time_list_by_step_with_start_end(self, start_hsm_list, end_hsm_list, step=30):
+	def make_time_list_between_2_hsm_list_by_step(self, start_hsm_list, end_hsm_list, step=30):
 		"""
 		시작과 종료시간을 입력하면, 30분간격으로 시간목록을 자동으로 생성시키는것
 		"""
 		result = []
 		hour, min, sec = start_hsm_list
 		hour_end, min_end, sec_end = end_hsm_list
 		result.append([hour, min, sec])
@@ -1179,15 +1195,15 @@
 		두날짜의 빼기
 		"""
 		utc1 = self.change_any_text_time_to_dt_obj(input_date1)
 		utc2 = self.change_any_text_time_to_dt_obj(input_date2)
 		result = abs((float(utc1) - float(utc2)) / (60 * 60 * 24))
 		return result
 
-	def minus_date1_date2(self, date_1, date_2):
+	def delta_2_date(self, date_1, date_2):
 		"""
 		두날짜의 빼기
 		"""
 		time_big = 1  # ymd_cls(date_1)
 		time_small = 2  # ymd_cls(date_2)
 		if time_big.lt_utc > time_small.lt_utc:
 			pass
@@ -1291,28 +1307,29 @@
 
 	def setup_time_zone(self, input_time_zone="seoul"):
 		self.var_common["timezone"] = input_time_zone
 
 	def setup_week_no_7(self, input_no=0):
 		self.var_common["week_no_7_start"] = input_no
 
-	def shift_day_for_ymd_list(self, input_ymd_list="", input_no=""):
+	def shift_ymd_list_by_day(self, input_time="", input_no=""):
 		"""
 		입력한 날짜리스트를 기준으로 날을 이동시키는것
 		아무것도 입력하지 않으면 현재 시간
 		입력값 : [2022, 03, 02]
 		출력값 : 2022-01-01
 		"""
-		utc_local_time = self.check_input_time(input_ymd_list)
+		utc_local_time = self.check_input_time(input_time)
 		shift_now = utc_local_time.shift(days=int(input_no))
 		result = shift_now.format("YYYY-MM-DD")
 		return result
 
 	def shift_dt_obj_by_day(self, dt_obj, input_no):
 		"""
+		날짜를 이동
 		"""
 		new_dt_obj = dt_obj + timedelta(days=input_no)
 		return new_dt_obj
 
 	def shift_dt_obj_by_hour(self, dt_obj, input_no):
 		"""
 		시간을 이동
@@ -1382,31 +1399,43 @@
 		add_year, remain_month = divmod((month + int(input_no)), 12)
 		if remain_month == 0:
 			add_year = add_year - 1
 			remain_month = 12
 		result = [year + int(add_year), remain_month, day]
 		return result
 
+	def shift_ymd_list_by_year_month_day(self, input_time="", input_year=0, input_month=0, input_day=0):
+		"""
+		기준날짜에서 월을 이동시키는것
+		출력값 : [2022, 3, 1]
+		"""
+		utc_local_time = self.check_input_time(input_time)
+		utc_local_time = utc_local_time.shift(years=int(input_year))
+		utc_local_time = utc_local_time.shift(months=int(input_month))
+		utc_local_time = utc_local_time.shift(days=int(input_day))
+		result = utc_local_time.format("YYYY-MM-DD")
+		return result
+
 
-	def shift_ymd_list_by_month(self, input_ymd_list="", input_month=3):
+	def shift_ymd_list_by_month(self, input_time="", input_month=3):
 		"""
 		기준날짜에서 월을 이동시키는것
 		출력값 : [2022, 3, 1]
 		"""
-		utc_local_time = self.check_input_time(input_ymd_list)
+		utc_local_time = self.check_input_time(input_time)
 		shift_now = utc_local_time.shift(months=int(input_month))
 		result = shift_now.format("YYYY-MM-DD")
 		return result
 
-	def shift_ymd_list_by_year(self, input_ymd_list="", input_year=3):
+	def shift_ymd_list_by_year(self, input_time="", input_year=3):
 		"""
 		기준날짜에서 년을 이동시키는것
 		입력형태 : [2022, 3, 1]
 		"""
-		utc_local_time = self.check_input_time(input_ymd_list)
+		utc_local_time = self.check_input_time(input_time)
 		shift_now = utc_local_time.shift(years=int(input_year))
 		result = shift_now.format("YYYY-MM-DD")
 		return result
 
 	def split_period_as_year_basis(self, input_ymd_list1, input_ymd_list2):
 		"""
 		날짜기간이 년이 다른경우 같은 year들로 리스트형태로 기간을 만들어 주는것
@@ -1448,33 +1477,28 @@
 		return result
 
 	def terms(self):
 		"""
 		용어정리
 		아래와같은 형태로 용어를 사용한다
 		"""
+		pass
 
 	def total_day_for_year(self):
 		# 입력 해의 총 날짜 확인
 		pass
 
 	def working_hour(self):
 		"""
 		근무시간기준
 		"""
 		self.var_common["wt96"] = [[900, 1800]]
 		self.var_common["wt85"] = [[800, 1700]]
 
 
-	def get_week_no_for_dt_obj(self, input_dt_obj):
-		# 요일에대한 숫자를, 일요일이 0이다
-		result = input_dt_obj.strftime('%w')
-		print("요일의 번호는 ==>", result)
-		return result
-
 	def check_last_day_for_lunar_ym_list_1(self, input_ym_list):
 		#음력으로 말일을 찾는것
 		result = 26
 		for nun in range(27, 31):
 			self.lunar_calendar.setLunarDate(input_ym_list[0], input_ym_list[1], nun, False)
 			temp = self.lunar_calendar.SolarIsoFormat()
 			ymd_list = temp.split("-")
@@ -1511,36 +1535,19 @@
 		dt_obj = self.change_ymd_list_to_dt_obj(ymd_list_1)
 		changed_dt_obj = self.shift_dt_obj_by_day(dt_obj, ymd_list_2[2])
 		changed_dt_obj = self.shift_dt_obj_by_month(changed_dt_obj, ymd_list_2[1])
 		changed_dt_obj = self.shift_dt_obj_by_year(changed_dt_obj, ymd_list_2[0])
 		result = self.change_dt_obj_to_ymd_list(changed_dt_obj)
 		return result
 
-	def shift_ymd_list_by_day(self, input_ymd_list="", input_day=3):
-		"""
-		기준날짜에서 일을 이동시키는것
-		출력값 : [2022, 3, 1]
-		"""
-		dt_obj = self.check_input_time(input_ymd_list)
-		shift_now = dt_obj + timedelta(days=int(input_day))
-		result = self.change_dt_obj_to_ymd_list(shift_now)
-		return result
-
-	def shift_ymd_list_by_day_1(self, input_ymd_list, input_day):
-		# 입력한 ¥MD 리스트에서 입력한 날짜만큼 이동시키기
-		dt_obj = self.change_ymd_list_to_dt_obj(input_ymd_list)
-		changed_dt_obj = self.shift_dt_obj_by_day(dt_obj, input_day)
-		result = self.change_dt_obj_to_ymd_list(changed_dt_obj)
-		return result
-
 	def change_dt_obj_to_utc_timestamp(self, input_dt_obj):
 		result = int(input_dt_obj.timestamp())
 		return result
 
-	def get_all_day_list_for_year_month(self, input_year, input_month):
+	def get_month_list_for_year_month(self, input_year, input_month):
 		# 년과 월을 주면, 한달의 리스트를 알아내는것
 		# 월요일부터 시작
 		result = []
 		week_no = []
 		date_obj = datetime(year=input_year, month=input_month, day=1).date()
 		first_day_wwek_no = calendar.monthrange(date_obj.year, date_obj.month)[0]
 		last_day = calendar.monthrange(date_obj.year, date_obj.month)[1]
@@ -1553,8 +1560,132 @@
 			if len(week_no) == 7:
 				result.append(week_no)
 				week_no = [num]
 			else:
 				week_no.append(num)
 		if week_no:
 			result.append(week_no)
-		return result
+		return result
+
+	def check_input_time_list_2d(self, input_time_list_2d):
+		"""
+		엑셀의 자료에서, 여러가지 형태로 입력이 된경우가 있어서, 이것을 검증해보는 자료
+		2023.02.03
+		feb 03, 23
+		02 03, 23
+		"""
+		pass
+
+	def check_year_or_not(self, input_list):
+		#입력된 자료들이 년을 나타내는 자료인지를 확인하는것
+		result = []
+		alphabet = "abcdefghijklmnopqrstuvwxyz" + "abcdefghijklmnopqrstuvwxyz".upper()
+		if type(input_list[0]) == type([]):
+			changed_input_list = input_list
+		else:
+			changed_input_list = []
+			for one in input_list:
+				changed_input_list.append([one])
+
+		for one_list in changed_input_list:
+			if str(one_list[0])[0] in alphabet:
+				#알파벳으로 사용하는것은 월밖에 없다
+				result.append(False)
+			else:
+				if len(str(one_list[0])) == 4:
+					#4개의 숫자는 년도를 나타내는 것
+					result.append(True)
+				elif int(one_list[0]) > 31:
+					# 31보다 크면, 년도이다
+					result.append(True)
+				elif int(one_list[0]) > 12 and int(one_list[0]) <= 31 :
+					#12보다 크면, 월을 나타내는것이 아니다
+					result.append(False)
+		total_num = 0
+		for one in result:
+			total_num = total_num + one
+
+		#전체중에서 70%가 넘으면 년을 쓰인것으로 본다
+		if total_num / len(result) > 0.5:
+			month_or_not = True
+		else:
+			month_or_not = False
+		return month_or_not
+
+	def check_month_or_not(self, input_list):
+		#입력된 자료들이 월을 나타내는 자료인지를 확인하는것
+		result = []
+		alphabet = "abcdefghijklmnopqrstuvwxyz" + "abcdefghijklmnopqrstuvwxyz".upper()
+		if type(input_list[0]) == type([]):
+			changed_input_list = input_list
+		else:
+			changed_input_list = []
+			for one in input_list:
+				changed_input_list.append([one])
+
+		for one_list in changed_input_list:
+			if str(one_list[0])[0] in alphabet:
+				#알파벳으로 사용하는것은 월밖에 없다
+				result.append(True)
+			else:
+				if len(str(one_list[0])) == 4:
+					#4개의 숫자는 년도를 나타내는 것
+					result.append(False)
+				elif int(one_list[0]) > 31:
+					# 31보다 크면, 년도이다
+					result.append(False)
+				elif int(one_list[0]) > 12 and int(one_list[0]) <= 31:
+					# 12보다 크면, 월을 나타내는것이 아니다
+					result.append(True)
+		total_num = 0
+		for one in result:
+			total_num = total_num + one
+
+		#전체중에서 70%가 넘으면 월로쓰인것으로 본다
+		if total_num / len(result) > 0.9:
+			month_or_not = True
+		else:
+			month_or_not = False
+
+		return month_or_not
+
+	def check_day_or_not(self, input_list):
+		#입력된 자료들이 년을 나타내는 자료인지를 확인하는것
+		result = []
+		alphabet = "abcdefghijklmnopqrstuvwxyz" + "abcdefghijklmnopqrstuvwxyz".upper()
+		if type(input_list[0]) == type([]):
+			changed_input_list = input_list
+		else:
+			changed_input_list = []
+			for one in input_list:
+				changed_input_list.append([one])
+
+		for one_list in changed_input_list:
+			if str(one_list[0])[0] in alphabet:
+				#알파벳으로 사용하는것은 월밖에 없다
+				result.append(False)
+			else:
+				if len(str(one_list[0])) == 4:
+					#4개의 숫자는 년도를 나타내는 것
+					result.append(False)
+				elif len(one_list[0]) <= 2:
+					result.append(True)
+
+				if int(one_list[0]) > 31:
+					# 31보다 크면, 년도이다
+					result.append(False)
+				else :
+					#12보다 크면, 월을 나타내는것이 아니다
+					result.append(True)
+
+
+		total_num = 0
+		for one in result:
+			total_num = total_num + one
+
+		#전체중에서 1보다 넘으면 년을 쓰인것으로 본다
+		#숫자가 2개이하인것과 12이상일때, 두번 True로 만들기때문에...
+		if total_num / len(result) > 1:
+			month_or_not = True
+		else:
+			month_or_not = False
+		return month_or_not
```

### Comparing `xython-1.4.0/src/xython/scolor.py` & `xython-1.5.0/src/xython/scolor.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,141 +1,42 @@
 # -*- coding: utf-8 -*-
 import re  #내장모듈
-
+import math
 import basic_data  # xython 모듈
 
 class scolor:
 	"""
 	색을 쉽게 사용하기위해 만든 모듈
+	기본색은 rgb로 한다
 	"""
 	def __init__(self):
 		self.base_data = basic_data.basic_data()
 		self.var = self.base_data.vars
 		self.var_common={}
 
-
 	def change_color_to_hsl(self, input_scolor):
 		result = self.change_scolor_to_hsl(input_scolor)
 		return result
 
 	def change_color_to_rgb(self, input_scolor):
 		hsl_value = self.change_scolor_to_hsl(input_scolor)
 		result = self.change_hsl_to_rgb(hsl_value)
 		return result
 
-	def change_excel56_to_rgb(self, input_no):
+	def change_excel_color_no_to_rgb(self, input_no):
 		"""
-		엑셀 기본 rgb 색 : 56색
+		엑셀 기본 rgb 56색의 번호를 rgb로 바꾸는 것
 		"""
 		result = self.var["rgb_56_for_excel"][int(input_no)]
 		return result
 
-	def change_hsl_to_36_hsl_by_h_step(self, hsl):
-		"""
-		위쪽으로 5개, 아래로 5개의 명도가 비슷한 색을 돌려준다
-		"""
-		h, s, l = hsl
-		result = []
-		for no in range(0, 36):
-			result.append([no*10, s, l])
-		return result
-
-	def change_hsl_to_3_hsl_with_big_l_gab (self, hsl, l_step = 30):
-		"""
-		명도차가 큰 2가지 1가지색
-		"""
-		h, s, l = hsl
-		rgb_1 = self.change_hsl_to_rgb([hsl[0], hsl[1], l_step])
-		rgb_2 = self.change_hsl_to_rgb(hsl)
-		rgb_3 = self.change_hsl_to_rgb([hsl[0], hsl[1], 100-l_step])
-		result = [rgb_1, rgb_2, rgb_3]
-		return result
-
-	def change_hsl_to_3_hsl_with_big_s_gab (self, hsl, s_step = 30):
-		"""
-		채도차가 큰 2가지 1가지색
-		"""
-		rgb_1 = self.change_hsl_to_rgb([hsl[0], s_step, hsl[2]])
-		rgb_2 = self.change_hsl_to_rgb(hsl)
-		rgb_3 = self.change_hsl_to_rgb([hsl[0], 100-s_step, hsl[2]])
-		result = [rgb_1, rgb_2, rgb_3]
-		return result
-
-	def change_hsl_to_3rgb_as_like_0_120_240(self, hsl):
-		"""
-		mode :
-		등간격 3색조합 : triad
-		활동적인 인상과 이미지를 보인다
-		"""
-		h, s, l = hsl
-
-		new_h_1 = divmod(h + 120, 360)[1]
-		new_h_3 = divmod(h + 240, 360)[1]
-
-		hsl_1 = [new_h_1, s, l]
-		hsl_3 = [new_h_3, s, l]
-
-		result_rgb = self.change_hsl_to_rgb([hsl_1, hsl, hsl_3])
-		return result_rgb
-
-	def change_hsl_to_3rgb_by_2near_bo(self, hsl, h_step=36):
-		"""
-		mode : 14
-		근접보색조합 : 보색의 근처색
-		분열보색조합 : Split Complementary
-		근접보색조합이라고도 한다. 보색의 강한 인상이 부담스러울때 보색의 근처에 있는 색을 사용
-		"""
-		h, s, l = hsl
-
-		new_h_1 = divmod(h - h_step + 180, 360)[1]
-		new_h_3 = divmod(h + h_step + 180, 360)[1]
-
-		hsl_1 = [new_h_1, s, l]
-		hsl_3 = [new_h_3, s, l]
-		result_rgb = self.change_hsl_to_rgb([hsl_1, hsl, hsl_3])
-		return result_rgb
-
-	def change_hsl_to_3rgb_by_2near_bo_style(self, hsl, h_step=36):
-		"""
-		근접보색조합 : 보색의 양쪽 근처색
-		분열보색조합 : Split Complementary
-		근접보색조합이라고도 한다. 보색의 강한 인상이 부담스러울때 보색의 근처에 있는 색을 사용
-		2차원 list의 형태로 돌려줌
-		"""
-		h, s, l = hsl
-
-		new_h_1 = divmod(h - h_step + 180, 360)[1]
-		new_h_3 = divmod(h + h_step + 180, 360)[1]
-		rgb_1 = self.change_hsl_to_rgb([new_h_1, s, l])
-		rgb_2 = self.change_hsl_to_rgb(hsl)
-		rgb_3 = self.change_hsl_to_rgb([new_h_3, s, l])
-		result = [rgb_1, rgb_2, rgb_3]
-
-		return result
-
-	def change_hsl_to_3rgb_by_2near_style (self, hsl, h_step=36):
-		"""
-		근접색조합 : 양쪽 근처색
-		"""
-		h, s, l = hsl
-
-		new_h_1 = divmod(h - h_step, 360)[1]
-		new_h_3 = divmod(h + h_step, 360)[1]
-
-		rgb_1 = self.change_hsl_to_rgb([new_h_1, s, l])
-		rgb_2 = self.change_hsl_to_rgb(hsl)
-		rgb_3 = self.change_hsl_to_rgb([new_h_3, s, l])
-		result = [rgb_1, rgb_2, rgb_3]
-		return result
-
 	def change_hsl_to_rgb(self, hsl):
 		"""
 		hsl을 rgb로 바꾸는 것이다
 		"""
-		#print("hsl값은 ==> ", hsl)
 		h, s, l = hsl
 
 		h = float(h / 360)
 		s = float(s / 100)
 		l = float(l / 100)
 
 		if s == 0:
@@ -222,50 +123,14 @@
 			final_l_value = 100
 		elif final_l_value < 0 :
 			final_l_value = 0
 
 		result = [hsl_value[0], hsl_value[1], final_l_value]
 		return result
 
-	def change_hsl_to_rgb_by_high_l(self, hsl, high_l = 80):
-		"""
-		고명도의 hsl로 변경
-		"""
-		result = self.change_hsl_to_rgb([hsl[0], hsl[1], high_l])
-		return [result]
-
-	def change_hsl_to_rgb_by_high_s(self, hsl, high_s = 80):
-		#고채도
-		result = self.change_hsl_to_rgb([hsl[0], high_s, hsl[2]])
-		return [result]
-
-	def change_hsl_to_rgb_by_low_l(self, hsl, high_l = 20):
-		"""
-		저명도, 20%정도의 명도를 저명도로 말하자자
-		"""
-		result = self.change_hsl_to_rgb([hsl[0], hsl[1], high_l])
-		return [result]
-
-	def change_hsl_to_rgb_by_low_s(self, hsl, high_s = 20):
-		#저채도
-		result = self.change_hsl_to_rgb([hsl[0], high_s, hsl[2]])
-		return [result]
-
-	def change_hsl_to_rgb_by_middle_l(self, hsl, high_l = 50):
-		"""
-		중명도의 hsl로 변경
-		"""
-		result = self.change_hsl_to_rgb([hsl[0], hsl[1], high_l])
-		return [result]
-
-	def change_hsl_to_rgb_by_middle_s(self, hsl, high_s = 50):
-		#중채도
-		result = self.change_hsl_to_rgb([hsl[0], high_s, hsl[2]])
-		return [result]
-
 	def change_hsl_to_rgb_by_triangle_style(self, hsl):
 		"""
 		등간격 3색조합 : triad
 		활동적인 인상과 이미지를 보인다
 		"""
 		h, s, l = hsl
 
@@ -317,25 +182,14 @@
 		new_h_1 = h + 180
 		if new_h_1 >= 360:
 			new_h_1 = 360 - new_h_1
 
 		result_rgb = self.change_hsl_to_rgb([new_h_1, s, l])
 		return result_rgb
 
-	def change_hsl_to_rgb_with_20_hsl_by_l_step(self, hsl):
-		"""
-		위쪽으로 5개, 아래로 5개의 명도가 비슷한 색을 돌려준다
-		"""
-		h, s, l = hsl
-		result = []
-		for no in range(0, 21):
-			temp = self.change_hsl_to_rgb([h, s, no * 5])
-			result.append(temp)
-		return result
-
 	def change_hsl_to_rgb_with_20_hsl_by_s_step(self, hsl):
 		"""
 		위쪽으로 5개, 아래로 5개의 명도가 비슷한 색을 돌려준다
 		"""
 		h, s, l = hsl
 		result = []
 		for no in range(0, 21):
@@ -352,34 +206,15 @@
 		result = []
 		for no in range(0,100+step,step):
 			#print("변경된 hsl은 s=> ", [h, no, l])
 			temp = self.change_hsl_to_rgb([h, no, l])
 			result.append(temp)
 		return result
 
-	def change_hsl_to_rgb_with_style(self, input_color, color_style, style_step=5):
-		"""
-		입력된 기본 값을 스타일에 맞도록 바꾸는것
-		스타일을 강하게 할것인지 아닌것인지를 보는것
-		입력예 : 기본색상, 적용스타일, 변화정도, "red45, 파스텔, 3
-		변화정도는 5를 기준으로 1~9까지임
-		"""
-		basic_hsl = input_color
-		aaa = self.var["check_change_step"][color_style]
-		step_1 = self.var["sl_big_step_vs_sl_no"] [str(aaa)]
-		step_2 = self.var["sl_small_step_vs_sl_no"] [str(style_step)]
-
-		h = int(basic_hsl[0])
-		s = int(basic_hsl[1]) + int(step_1[0]) + int(step_2[0])
-		l = int(basic_hsl[2]) + int(step_1[1]) + int(step_2[1])
-
-		changed_rgb = self.change_hsl_to_rgb([h, s, l])
-		return changed_rgb
-
-	def change_hsl_to_rgb_with_style_1(self, input_hsl, color_style="파스텔", style_step=5):
+	def change_hsl_to_rgb_with_style(self, input_hsl, color_style="파스텔", style_step=5):
 		"""
 		입력된 기본 값을 스타일에 맞도록 바꾸고, 스타일을 강하게 할것인지 아닌것인지를 보는것
 		color_style : pccs의 12가지 사용가능, 숫자로 사용가능, +-의 형태로도 사용가능
 		입력예 : 기본색상, 적용스타일, 변화정도,("red45, 파스텔, 3)
 		변화정도는 5를 기준으로 1~9까지임
 		"""
 
@@ -414,15 +249,15 @@
 				if input_value[1]>100 or input_value[2] >100:
 					hsl = self.change_rgb_to_hsl(input_value)
 				else: hsl = input_value
 		else:
 			hsl = "error"
 		return hsl
 
-	def change_rgb_to_12_pccs_rgb_set(self, rgb):
+	def change_rgb_to_12_pccs_rgb_list(self, rgb):
 		"""
 		pccs : 일본색체연구서가 빌표한 12가지 색으로 구분한것
 		어떤 입력된 색의 기본적인 PCSS 12색을 돌려준다
 		pccs톤, rgb로 넘어온 색을 pcss톤 12개로 만들어서 돌려준다
 		"""
 		result = []
 		h, s, l = self.change_rgb_to_hsl(rgb)
@@ -544,25 +379,14 @@
 
 				if int(l_code) > 100 : l_code = 100
 				if int(l_code) < 0 : l_code = 0
 			#print("[h_code, s_code, l_code] ==> ", h_code, s_code, l_code)
 			result = [h_code, s_code, l_code]
 		return result
 
-	def change_scolor_to_n_color_set(self, input_scolor, step_no = 10):
-		#하나의 색을 옅은것부터 진한것까지 N개의 rgb값으로 변경하는것
-		hsl_list = self.change_scolor_to_hsl(input_scolor)
-
-		result = []
-		for l in range(0, 110, 10):
-			temp = self.change_hsl_to_rgb([hsl_list[0], 100, l])
-			result.append(temp)
-		return result
-
-
 	def change_scolor_to_rgb (self, input_scolor):
 		hsl_list = self.change_scolor_to_hsl(input_scolor)
 		result = self.change_hsl_to_rgb(hsl_list)
 		return result
 
 	def change_scolor_to_rgb_with_style(self, input_scolor="red45", color_style="파스텔", style_step=5):
 		"""
@@ -599,15 +423,28 @@
 			l_value = -10 * len(change_mode)
 			result = [0, 0, l_value]
 		elif change_mode in self.var["color_tone_12_names_vs_no"].keys():
 			no = self.var["color_tone_12_names_vs_no"][change_mode]
 			result = self.var["sl_big_step_vs_sl_no"][no]
 		return result
 
-	def check_hsl_value(self, input_color):
+	def check_rgb_to_excel_color_no(self, input_rgb):
+		# 입력 R6B 값중에서 엑셀의 56 가지 기본색상의 R6B 값과 가장 가까운값을 찾아내는것
+		result = 0
+		short_length = 255 * 255 * 255
+		var_56_rgb = self.var["dic_colorindex_rgblist"]
+		for excel_color_no in var_56_rgb.keys():
+			excel_rgb = var_56_rgb[excel_color_no]
+			differ = self.distance_two_3d_point(input_rgb, excel_rgb)
+			if short_length > differ:
+				short_length = differ
+				result = excel_color_no
+		return result
+
+	def check_input_hsl(self, input_color):
 		# 입력으로 들어온 색에 대한 hsl값을 돌려준다
 		try:
 			color_name = self.var["check_color_name"][input_color]
 			result = self.var["color_name_eng_vs_hsl_no"][color_name]
 		except:
 			pass
 		# 입력된 색이름을 찾을수 없을때
@@ -671,18 +508,14 @@
 		if color_minus != []:
 			color_no = 50 - 5 * len(color_minus[0])
 
 		result = [number_only, color_name, color_no]
 		#print(result)
 		return result
 
-	def check_input_type(self, input_value):
-		hsl = self.check_input_type(input_value)
-		return hsl
-
 	def control_hsl_by_scolor_style(self, input_hsl, s_step="++", l_step="++"):
 		"""
 		sl의값을 조정하여 채도와 명도를 조절하는것
 		입력형식 : hsl값을 올리거나 내리는 것
 		입력 : [[36, 50, 50], "++", "--"]
 		약 5씩이동하도록 만든다
 		"""
@@ -706,14 +539,92 @@
 		elif l_step[0] == "-":
 			l = l - len(l_step) * step_no
 			if l < 0: l = 0
 
 		result = self.change_hsl_to_rgb([h, s, l])
 		return result
 
+	def control_scolor_for_bright(self, input_scolor, my_value=30):
+		#값이 0이면 기본값으로, -100 ~ +100까지
+		input_hsl = self.change_scolor_to_hsl(input_scolor)
+		result = self.control_hsl_to_bright_style(input_hsl, my_value)
+		return result
+
+
+	def control_hsl_to_bright_style(self, input_hsl, strong_level=0.5):
+		"""
+		입력받은 hsl값을 명도가 높은 쪽으로 이동시키는것
+		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
+		"""
+		h, s, l = input_hsl
+
+		changed_s = s + (100 - s) * strong_level
+		changed_l = l + (100 - l) * strong_level
+		return [h, changed_s, changed_l]
+
+	def control_hsl_to_dark_style(self, input_hsl, strong_level=0.5):
+		"""
+		입력받은 hsl값을 어두운 쪽으로 이동시키는것
+		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
+		"""
+		h, s, l = input_hsl
+		style = dark = [0,0]
+
+		delta_s = (style[0] - s) * strong_level
+		delta_l = (style[1] - l) * strong_level
+
+		changed_s = s + delta_s
+		changed_l = l + delta_l
+		return [h, changed_s, changed_l]
+
+	def control_hsl_to_gray_style(self, input_hsl, strong_level=0.5):
+		"""
+		입력받은 hsl값을 어두운 쪽으로 이동시키는것
+		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
+		"""
+		h, s, l = input_hsl
+		style = graish = [100,0]
+
+		delta_s = (style[0] - s) * strong_level
+		delta_l = (style[1] - l) * strong_level
+
+		changed_s = s + delta_s
+		changed_l = l + delta_l
+		return [h, changed_s, changed_l]
+
+	def control_hsl_to_pastel_style(self, input_hsl, strong_level=0.5):
+		"""
+		입력받은 hsl값을 파스텔톤으로 적용시키는것
+		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
+		"""
+		h, s, l = input_hsl
+		style = pastel = [0,100]
+
+		delta_s = (style[0] - s)*strong_level
+		delta_l = (style[1] - l)*strong_level
+
+		changed_s = s + delta_s
+		changed_l = l + delta_l
+		return [h, changed_s, changed_l]
+
+	def control_hsl_to_vivid_style(self, input_hsl, strong_level=0.5):
+		"""
+		입력받은 hsl값을 어두운 쪽으로 이동시키는것
+		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
+		"""
+		h, s, l = input_hsl
+		style = sharp = [50,100]
+
+		delta_s = (style[0] - s) * strong_level
+		delta_l = (style[1] - l) * strong_level
+
+		changed_s = s + delta_s
+		changed_l = l + delta_l
+		return [h, changed_s, changed_l]
+
 	def control_hsl_value(self, input_hsl, step_no):
 		# +，-로 조정을 하는것이다
 		s, l = self.var["+-_value_vs_sl_no"][step_no]
 		result = [input_hsl[0], input_hsl[1] + s, input_hsl[2] + l]
 
 	def control_hsl_with_style(self, basic_hsl, color_style="파스텔", style_step=5):
 		color_style = self.var["check_color_tone"][color_style]
@@ -723,16 +634,14 @@
 		h = int(basic_hsl[0])
 		s = int(step_1[0]) + int(step_2[0])
 		l = int(step_1[1]) + int(step_2[1])
 
 		changed_rgb = self.change_hsl_to_rgb([h, s, l])
 		return changed_rgb
 
-		##################################### data자료들을 돌려주는 것
-
 	def control_rgb_by_scolor_style(self, input_rgb, s_step="++", l_step="++"):
 		input_hsl = self.change_rgb_to_hsl(input_rgb)
 		step_no = 5  # 5단위씩 변경하도록 하였다
 		h, s, l = input_hsl
 
 		if s_step == "":
 			pass
@@ -773,14 +682,30 @@
 		h = int(basic_hsl[0])
 		s = int(basic_hsl[1]) + int(step_1[1]) + int(step_2[1])
 		l = int(basic_hsl[2]) + int(step_1[2]) + int(step_2[2])
 
 		changed_rgb = self.change_hsl_to_rgb([h,s,l])
 		return changed_rgb
 
+
+	def control_scolor_for_light(self, input_scolor, my_value=30):
+		input_hsl = self.change_scolor_to_hsl(input_scolor)
+		result = self.control_hsl_to_dark_style(input_hsl, my_value/100)
+		return result
+
+	def control_scolor_for_pastel(self, input_scolor, my_value=30):
+		input_hsl = self.change_scolor_to_hsl(input_scolor)
+		result = self.control_hsl_to_pastel_style(input_hsl, my_value/100)
+		return result
+
+	def control_scolor_for_vivid(self, input_scolor, my_value=30):
+		input_hsl = self.change_scolor_to_hsl(input_scolor)
+		result = self.control_hsl_to_vivid_style(input_hsl, my_value/100)
+		return result
+
 	def data_12_color_name_eng_list(self):
 		"""
 		12가지 영어 색깔이름을 돌려준다
 		['rm', 'bm', 'cya', 'blu', 'gra', '유황', 'red', 'pale_pink', 'mag', 'bc', 'sca', 'yel', 'bla', 'ora', 'bro', 'gy', 'gre', 'scarlet', 'whi', 'gc', 'pin', 'sulphur_yellow']
 		"""
 		result = self.var["color_name_for_basic_12_eng"]
 		return result
@@ -797,46 +722,45 @@
 		return result
 
 	def data_12_pccs_style_name_list(self):
 		result = self.var["color_tone_kor"]
 
 		return result
 
-	def data_12_rgb_list(self):
-		result = self.var["rgb_for_basic_12"]
-		return result
-
 	def data_46_excel_rgb_list(self):
 		result = self.var["rgb_46_for_excel"]
 		return result
 
-
-
-	def data_all_color_name_list(self):
+	def data_56_excel_rgb_list(self):
 		"""
-		모든 색깔의 이름들
+		엑셀 기본 rgb 색 : 56색
 		"""
-		result = list(set(self.var["check_color_name"].values()))
+		result = self.var["rgb_56_for_excel"]
 		return result
 
-
-	def data_all_eng_color_name_list(self):
+	def data_all_color_name_eng_list(self):
 		"""
 		scolor에서 사용할수있는 모든 영어 색깔의 이름들
 		"""
 		result = self.var["color_name_for_all_eng"]
 		return result
 
-	def data_all_kor_color_name_list(self):
+	def data_all_color_name_kor_list(self):
 		"""
 		scolor에서 사용할수있는 모든 한글 색깔의 이름들
 		"""
 		result = self.var["color_name_for_all_kor"]
 		return result
 
+	def data_all_color_name_list(self):
+		"""
+		모든 색깔의 이름들
+		"""
+		result = list(set(self.var["check_color_name"].values()))
+		return result
 
 	def data_basic_12_hsl_set(self):
 		"""
 		360도의 색을 30도씩 12개로 구분한 hsl분류표
 		"""
 		result = self.var["hsl_no_for_basic_12"]
 		return result
@@ -847,14 +771,18 @@
 		pccs : 일본색체연구서가 빌표한 12가지 색으로 구분한것
 		어떤 입력된 색의 기본적인 PCSS 12색을 돌려준다
 		pccs톤, rgb로 넘어온 색을 pcss톤 12개로 만들어서 돌려준다
 		"""
 		result = self.var["color_tone_eng"]
 		return result
 
+	def data_basic_12_rgb_list(self):
+		result = self.var["rgb_for_basic_12"]
+		return result
+
 	def data_basic_12_rgb_pccs_style(self, hsl):
 		"""
 		12가지 스타일의 hsl을 돌려주는 것이다
 		"""
 		result = []
 		for one_value in self.var["hsl_no_for_basic_12"]:
 			temp = self.change_hsl_to_rgb([hsl[0], one_value[0], one_value[1]])
@@ -914,21 +842,14 @@
 		for h in range(0, 360, 10):
 			for s in range(0, 110, 10):
 				for l in range(0, 110, 10):
 					temp = self.change_hsl_to_rgb([h, s, l])
 					result[str(h) + str("_") + str(s) + str("_") + str(l)] = temp
 		return result
 
-	def data_basic_56_excel_rgb_set(self):
-		"""
-		엑셀 기본 rgb 색 : 56색
-		"""
-		result = self.var["rgb_56_for_excel"]
-		return result
-
 	def data_basic_8_pastel_rgb_set(self):
 		"""
 		기본적인
 		자료가 있는 색들의 배경색으로 사용하면 좋은 색들
 		"""
 		color_set = self.var["hsl_no_for_basic_12"][:-4]
 		result = []
@@ -941,15 +862,14 @@
 		result = self.var["color_name_for_basic_12_kor"]
 		return result
 
 	def data_basic_color_step(self):
 		result = self.var["basic_color_step"]
 		return result
 
-
 	def data_basic_color_tone_list(self):
 		result = self.var["color_tone_kor"]
 		return result
 
 	def data_basic_faber_rgb_set(self, start_color=11, code=5):
 		"""
 		파버 비덴의의 색체 조화론을 코드로 만든것이다
@@ -992,48 +912,49 @@
 		result = []
 		for no in new_color_set:
 			temp_hsl = hsl_johannes[no][stongness]
 			rgb = self.change_hsl_to_rgb(temp_hsl)
 			result.append(rgb)
 		return result
 
-	def data_color_tone_kor(self):
+	def data_color_tone_kor_list(self):
 		"""
 		칼라톤에대한 한글이름
 		"""
 		result = self.var["color_tone_kor"]
 		return result
 
-
-
 	def data_cool_color_name_list(self):
 		"""
 		차가운 색깔의 이름들
 		"""
 		result = ["파랑", "초록", "보라"]
 		return result
 
-	def data_excel_46_rgb_list(self):
-		result = self.var["rgb_46_for_excel"]
-		return result
-
-	def data_excel_56_rgb_list(self):
-		"""
-		엑셀 기본 rgb 색 : 56색
-		"""
-		result = self.var["rgb_56_for_excel"]
-		return result
-
 	def data_worm_color_name_list(self):
 		"""
 		따뜻한 색깔의 이름들
 		"""
 		result = ["빨강", "주황", "노랑"]
 		return result
 
+	def distance_two_3d_point(self, input_1, input_2):
+		# 3 차원의 거리를 기준으로 RGB 값의 차이를 계산하는 것
+		dist = math.sqrt(
+			pow(input_1[0], input_2[0], 2) + pow(input_1[1], input_2[1], 2) + pow(input_1[2], input_2[2], 2))
+		return dist
+
+	def get_hsl(self, input_scolor):
+		result = self.change_input_value_to_hsl(input_scolor)
+		return result
+
+	def get_rgb(self, input_scolor):
+		result = self.change_scolor_to_rgb(input_scolor)
+		return result
+
 	def get_rgb_by_excel_color_no(self, input_no):
 		"""
 		엑셀의 기본 번호를 넣으면 rgb값을 돌려주는것
 		엑셀 기본 rgb 색 : 56색
 		"""
 		result = self.var["rgb_56_for_excel"][int(input_no)]
 		return result
@@ -1053,24 +974,181 @@
 
 	def history(self):
 		result = 	"""
 			2023-03-02 : 전반적으로 이름을 수정함
 			"""
 		return result
 
+	def make_20_l_step_color_by_18_degree(self, hsl):
+		"""
+		위쪽으로 5개, 아래로 5개의 명도가 비슷한 색을 돌려준다
+		"""
+		h, s, l = hsl
+		result = []
+		for no in range(0, 21):
+			temp = [h, s, no * 5]
+			result.append(temp)
+		return result
+
+	def make_2_near_bo_by_h_step(self, hsl, h_step=36):
+		"""
+		mode : 14
+		근접보색조합 : 보색의 근처색
+		분열보색조합 : Split Complementary
+		근접보색조합이라고도 한다. 보색의 강한 인상이 부담스러울때 보색의 근처에 있는 색을 사용
+		"""
+		h, s, l = hsl
+
+		new_h_1 = divmod(h - h_step + 180, 360)[1]
+		new_h_3 = divmod(h + h_step + 180, 360)[1]
+
+		hsl_1 = [new_h_1, s, l]
+		hsl_3 = [new_h_3, s, l]
+		result = [hsl_1, hsl, hsl_3]
+		return result
+
+
+	def make_2_side_color_by_h_step (self, hsl, h_step=36):
+		"""
+		근접색조합 : 양쪽 근처색
+		"""
+		h, s, l = hsl
+
+		new_h_1 = divmod(h - h_step, 360)[1]
+		new_h_3 = divmod(h + h_step, 360)[1]
+
+		rgb_1 = self.change_hsl_to_rgb([new_h_1, s, l])
+		rgb_2 = self.change_hsl_to_rgb(hsl)
+		rgb_3 = self.change_hsl_to_rgb([new_h_3, s, l])
+		result = [rgb_1, rgb_2, rgb_3]
+		return result
+
+	def make_2_side_color_by_l_step_for_hsl(self, hsl, l_step = 30):
+		"""
+		명도차가 큰 2가지 1가지색
+		"""
+		h, s, l = hsl
+		rgb_1 = self.change_hsl_to_rgb([h, s, l_step])
+		rgb_2 = self.change_hsl_to_rgb(hsl)
+		rgb_3 = self.change_hsl_to_rgb([h, s, 100-l_step])
+		result = [rgb_1, rgb_2, rgb_3]
+		return result
+
+	def make_2_side_color_by_s_step_for_hsl (self, hsl, s_step = 30):
+		"""
+		채도차가 큰 2가지 1가지색
+		"""
+		rgb_1 = self.change_hsl_to_rgb([hsl[0], s_step, hsl[2]])
+		rgb_2 = self.change_hsl_to_rgb(hsl)
+		rgb_3 = self.change_hsl_to_rgb([hsl[0], 100-s_step, hsl[2]])
+		result = [rgb_1, rgb_2, rgb_3]
+		return result
+
+	def make_3_step_color_by_120_degree_for_hsl(self, hsl):
+		"""
+		mode :
+		등간격 3색조합 : triad
+		활동적인 인상과 이미지를 보인다
+		"""
+		h, s, l = hsl
+
+		new_h_1 = divmod(h + 120, 360)[1]
+		new_h_3 = divmod(h + 240, 360)[1]
+
+		hsl_1 = [new_h_1, s, l]
+		hsl_3 = [new_h_3, s, l]
+
+		result_rgb = self.change_hsl_to_rgb([hsl_1, hsl, hsl_3])
+		return result_rgb
+
+	def make_high_bright_hsl_by_l(self, hsl, changed_l = 80):
+		"""
+		고명도의 hsl로 변경
+		"""
+		result = self.change_hsl_to_rgb([hsl[0], hsl[1], changed_l])
+		return [result]
+
+	def make_hsl_set_by_36_h_step(self, hsl):
+		# hsl중에서 10도간격으로 h값을 36개 만드는것
+		h, s, l = hsl
+		result = []
+		for no in range(0, 36):
+			result.append([no*10, s, l])
+		return result
+
+	def make_low_bright_hsl_by_l(self, hsl, changed_l = 20):
+		# 저명도, 20%정도의 명도를 저명도로 말하자자
+		result = [hsl[0], hsl[1], changed_l]
+		return [result]
+
+	def make_low_color_hsl_by_s(self, hsl, high_s = 20):
+		#저채도
+		result = self.change_hsl_to_rgb([hsl[0], high_s, hsl[2]])
+		return [result]
+
+	def make_middle_bright_hsl_by_l(self, hsl, high_l = 50):
+		"""
+		중명도의 hsl로 변경
+		"""
+		result = self.change_hsl_to_rgb([hsl[0], hsl[1], high_l])
+		return [result]
+
+	def make_middle_color_hsl_by_s(self, hsl, high_s = 50):
+		#중채도
+		result = [hsl[0], high_s, hsl[2]]
+		return [result]
+
+	def make_n_color_set_by_h(self, hsl, n_step):
+		h, s, l = hsl
+		result = []
+		for no in range(0, n_step):
+			new_h = divmod(no * (360 / n_step) + h, 360)[0]
+			temp = [new_h, s, l]
+			result.append(temp)
+		return result
+
+
+	def make_n_color_set_by_l(self, hsl, n_step):
+		h, s, l = hsl
+		result = []
+		for no in range(0, n_step):
+			new_l = divmod(no * n_step + l, 100)[0]
+			temp = [h, s, new_l]
+			result.append(temp)
+		return result
+
+
+
+
+
+	def make_n_color_set_by_s(self, hsl, n_step):
+		h, s, l = hsl
+		result = []
+		for no in range(0, n_step):
+			new_s = divmod(no * n_step + s, 100)[0]
+			temp = [h, new_s, l]
+			result.append(temp)
+		return result
+
+
 	def make_one_color_to_many_colors_by_step (self, input_color = "red", step = 10):
 		"""
 		하나의 색을 지정하면 10가지의 단계로 색을 돌려주는 것이다
 		"""
 		result =[]
 		for no in range(0,100,int(100/step)):
 			temp = self.change_color_to_rgb(input_color+str(no))
 			result.append(temp)
 		return result
 
+	def make_strong_color_hsl_by_s(self, hsl, changed_s = 80):
+		#고채도
+		result = [hsl[0], changed_s, hsl[2]]
+		return [result]
+
 	def manual(self):
 		result = 	"""
 			"""
 		return result
 
 	def mix_two_scolors_with_step(self, scolor_1, scolor_2, step=10):
 		# 두가지색을 기준으로 몇단계로 색을 만들어주는 기능
@@ -1084,85 +1162,31 @@
 		for no in range(1, step - 1):
 			new_r = int(rgb_1[0] + r_step * no)
 			new_g = int(rgb_1[1] + g_step * no)
 			new_b = int(rgb_1[2] + b_step * no)
 			result.append([new_r, new_g, new_b])
 			result.append(rgb_2)
 		return result
-	def move_hsl_to_bright_style(self, input_hsl, strong_level=0.5):
-		"""
-		입력받은 hsl값을 명도가 높은 쪽으로 이동시키는것
-		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
-		"""
-		h, s, l = input_hsl
-		style = bright = [100,100]
-
-		delta_s = (style[0] - s) * strong_level
-		delta_l = (style[1] - l) * strong_level
 
-		changed_s = s + delta_s
-		changed_l = l + delta_l
-		return [h, changed_s, changed_l]
-
-	def move_hsl_to_dark_style(self, input_hsl, strong_level=0.5):
-		"""
-		입력받은 hsl값을 어두운 쪽으로 이동시키는것
-		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
-		"""
-		h, s, l = input_hsl
-		style = dark = [0,0]
-
-		delta_s = (style[0] - s) * strong_level
-		delta_l = (style[1] - l) * strong_level
-
-		changed_s = s + delta_s
-		changed_l = l + delta_l
-		return [h, changed_s, changed_l]
-
-	def move_hsl_to_gray_style(self, input_hsl, strong_level=0.5):
-		"""
-		입력받은 hsl값을 어두운 쪽으로 이동시키는것
-		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
-		"""
-		h, s, l = input_hsl
-		style = graish = [100,0]
-
-		delta_s = (style[0] - s) * strong_level
-		delta_l = (style[1] - l) * strong_level
-
-		changed_s = s + delta_s
-		changed_l = l + delta_l
-		return [h, changed_s, changed_l]
-
-	def move_hsl_to_pastel_style(self, input_hsl, strong_level=0.5):
-		"""
-		입력받은 hsl값을 파스텔톤으로 적용시키는것
-		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
-		"""
-		h, s, l = input_hsl
-		style = pastel = [0,100]
-
-		delta_s = (style[0] - s)*strong_level
-		delta_l = (style[1] - l)*strong_level
-
-		changed_s = s + delta_s
-		changed_l = l + delta_l
-		return [h, changed_s, changed_l]
-
-	def move_hsl_to_vivid_style(self, input_hsl, strong_level=0.5):
-		"""
-		입력받은 hsl값을 어두운 쪽으로 이동시키는것
-		bright = [100,100], sharp = [50,100], graish = [100,0], dark = [0,0], black = [50, 0]
-		"""
-		h, s, l = input_hsl
-		style = sharp = [50,100]
-
-		delta_s = (style[0] - s) * strong_level
-		delta_l = (style[1] - l) * strong_level
-
-		changed_s = s + delta_s
-		changed_l = l + delta_l
-		return [h, changed_s, changed_l]
 	def terms(self):
 		result = 	"""
 			"""
+		return result
+
+
+	#def control_scolor_for_clear(self, input_scolor, my_value=30):
+	#def control_scolor_for_worm(self, input_scolor, my_value=30):
+	#def control_scolor_for_basic(self, input_scolor, my_value=30):
+	#def control_scolor_for_strong(self, input_scolor, my_value=30):
+
+
+	def data_style_name_list(self):
+		style_kor = ['밝은', '기본', '파스텔', '부드러운', '검정', '연한', '탁한', '어두운', '밝은회색', '검은', '짙은', '강한', '회색', '진한', '옅은', '어두운회색', '흐린', '선명한']
+		style_eng = ['white', 'vivid', 'soft', 'deep', 'pale', 'gray', 'darkgrayish', 'grayish', 'lightgrayish', 'strong', 'light', 'bright', 'black', 'dull', 'dark']
+		result = style_kor + style_eng
+		return result
+
+	def change_style(self, input_scolor, style_name):
+		hsl = self.change_scolor_to_hsl(input_scolor)
+		change_mode = self.var["check_change_step"][style_name]
+		result = self.change_hsl_to_rgb_by_change_mode(hsl, change_mode)
 		return result
```

### Comparing `xython-1.4.0/src/xython/youtil.py` & `xython-1.5.0/src/xython/youtil.py`

 * *Files 1% similar despite different names*

```diff
@@ -1486,34 +1486,46 @@
 		"""
 		폴더안의 파일을 이름, 작성한날, 크기, 총경로를 리스트로 만들어서 주는것
 		"""
 		result = []
 		all_files = os.scandir(directory)
 		for one in all_files:
 			info = one.stat()
-			if one.is_dir():
-				#	print(directory+,,\\"+one.name)
-				temp = self.read_filenames_in_folder_with_all_properties(directory + "\\" + one.name)
-				result.extend(temp)
-			else:
-				#result.append(one)
-				result.append([one.name, info.st_mtime, info.st_size, one.path])
+			try:
+				if one.is_dir():
+					#	print(directory+,,\\"+one.name)
+					temp = self.read_filenames_in_folder_with_all_properties(directory + "\\" + one.name)
+					result.extend(temp)
+				else:
+					#result.append(one)
+					result.append([one.name, info.st_mtime, info.st_size, one.path])
+			except:
+				pass
 		return result
 
 
 	def find_same_value_in_list2d(self, input_lisd1d_1, input_lisd1d_2):
 		"""
 		2차원의 자료안에서 입력값이 같은것을 찾아내기
 		"""
 		result = []
 		for one in input_lisd1d_1:
 			if one in input_lisd1d_2:
 				result.append(one)
 		return result
 
+	def get_same_value_list(self, input_list1d_1, input_list1d_2):
+		# 기준값에서 1 차원의 같은 값을 찾는 것이다
+		result = []
+		for one in input_list1d_1:
+			if one in input_list1d_2:
+				result.append(one)
+		return result
+
+
 	def get_same_value_for_list2d(self, input_lisd2d_1, input_lisd2d_2, index_list=[1,2]):
 		"""
 		2 차원의 자료들이 서로 같은것을 삭제하는 것인데,
 		모두 같은것이 아니고, 일부분이 같은것을
 		골라내는 기능을 만든 것이다
 		"""
 		semi_result_1 = {}
@@ -1561,18 +1573,16 @@
 		입력으로 들어온 2차원의 자료중에서, 가로행이 완전히 빈것을 삭제하는 기능
 		"""
 		base_no = len(input_list2d[0])
 		result = []
 		for list_1d in input_list2d:
 			check_no = 0
 			for value in list_1d:
-				if value:
-					break
-				else:
-					check_no = base_no + 1
+				if value in [[], (), "", None]:
+					check_no = check_no + 1
 			if check_no != base_no:
 				result.append(list_1d)
 		return result
 
 	def delete_empty_yline(self, input_list2d):
 		"""
 		입력으로 들어온 2차원의 자료중에서, 세로행이 처음부터 끝까지 빈Y열을 삭제하는 기능
@@ -1615,14 +1625,15 @@
 				title_len = len(one)
 				if input_name[-title_len:] == one:
 					name = input_name[:-title_len]
 					title = input_name[-title_len:]
 					break
 		return [name, title]
 
+
 	def delete_list2d_by_index(self, input_list2d, no_list):
 		"""
 		2차원 자료에서
 		원하는 순서들의 자료를 삭제하는 것
 		입력형태 : 2차원리스트, [2,5,7]
 		"""
 		no_list.sort()
@@ -2082,18 +2093,14 @@
 			for y in range(len(table_value_list[0])):
 				temp = temp + "<td>" + str(table_value_list[x][y]) + "<br></td>"
 			temp = temp + "</tr>"
 		temp = temp + "</table>" + body_tail + "</body></html>"
 		return temp
 
 
-
-
-
-
 	def change_number_to_tel_style(self, input_value):
 		# 전화번호나 핸드폰 번호 스타일을 바꿔주는것
 		# 전화번호를 21345678 =>02-134-5678 로 변경하는 것
 		result = input_value
 		value = str(int(input_value))
 		if len(value) == 8 and value[0] == "2":
 			# 22345678 => 02-234-5678
@@ -2285,15 +2292,17 @@
 			else:
 				sorted_list2d = self.sort_list2d_by_index(input_list2d, index_no)
 				result.append(sorted_list2d)
 		return result
 
 	def group_input_list2d_by_index_no(self, input_list2d, index_no=4):
 		result = []
+		print(input_list2d)
 		sorted_input_list2d = self.sort_list2d_by_index(input_list2d, index_no)
+		print(sorted_input_list2d)
 		check_value = sorted_input_list2d[0][index_no]
 		temp = []
 		for one_list in sorted_input_list2d:
 			if one_list[index_no] == check_value:
 				temp.append(one_list)
 			else:
 				result.append(temp)
@@ -2305,8 +2314,107 @@
 
 	def group_input_list3d_by_index_no(self, input_list3d, index_no=4):
 		result = []
 		for input_list2d in input_list3d:
 			sorted_input_list2d = self.sort_list2d_by_index(input_list2d, index_no)
 			grouped_list3d = self.group_input_list2d_by_index_no(sorted_input_list2d, index_no)
 			result = result + grouped_list3d
+		return result
+
+	def delete_line_in_list2d_by_index(self, input_list2d, no_list):
+		#입력형태 : 2차원리스트, [2,5,7]
+		no_list.sort()
+		no_list.reverse()
+		for one in no_list:
+			for x in range(len(input_list2d)):
+				del input_list2d[x][one]
+		return input_list2d
+
+	def read_folder_filename_all(self, directory):
+		"""
+		폴더 안의 화일을 읽어오는것
+		"""
+		result = []
+		filenames = os.listdir(directory)
+		for filename in filenames:
+			full_filename = os.path.join(directory, filename)
+			result.append(filename)
+		return result
+
+	def string_to_binary(self, st):
+		temp = [bin(ord(i))[2:].zfill(8) for i in st]
+		result = "".join(temp)
+		return result
+
+	def string_to_binary_list(self,st):
+		result = [bin(ord(i))[2:].zfill(8) for i in st]
+		return result
+
+	def binary_to_string(self, bits):
+		return ''.join([chr(int(i, 2)) for i in bits])
+
+	def binary_to_int(self, bits):
+		return int(bits, 2)
+
+	def change_10jinsu_to_njinsu(self,input_num, jinsu=10):
+		# 10진수값을 34진수까지의 진수형태로 변환
+		# 진수값을 바꾸면 다른 진수형태로 변경된다
+		base_letter = "0123456789abcdefghijklmnopqrstuvwxyz"
+		q, r = divmod(input_num, jinsu)
+		if q == 0:
+			return base_letter[r]
+		else:
+			return self.change_10jinsu_to_njinsu(q, jinsu) + base_letter[r]
+
+	def change_njinsu_to_10jinsu(self,input_num, input_jinsu=10):
+		# 입력형식의 값을 10진수값으로 변경하는것
+		original_letter = "0123456789abcdefghijklmnopqrstuvwxyz"
+		base_letter = original_letter[0:input_jinsu]
+		new_dic = {}
+		for no, one_value in enumerate(base_letter):
+			new_dic[one_value] = no
+		total = 0
+		checked_input_num = reversed(input_num)
+		for no, one in enumerate(checked_input_num):
+			total = total + len(base_letter) ** (no) * new_dic[one]
+		return total
+
+	def change_10jinsu_to_base_letter_jinsu(self,input_num, show_letter="가나다라마바사아자차카타파하"):
+		# 10진수값을 내가원하는 형식으로 변경하는것
+		# 기본형을 예로들면 14진수이면서, 표현된,모양은 "0123456789abcd"가
+		# 아니고 "가나다라마바사아자차카타파하"로 표현되는것
+		jinsu = int(len(show_letter))
+		q, r = divmod(input_num, jinsu)
+		if q == 0:
+			return show_letter[r]
+		else:
+			return self.change_10jinsu_to_base_letter_jinsu(q) + show_letter[r]
+
+	def change_base_letter_jinsu_to_10jinsu(self,input_num, show_letter="가나다라마바사아자차카타파하"):
+		# 입력형식의 값을 10진수값으로 변경하는것
+		# 10진수값을 내가원하는 형식으로 변경하는것
+		# 기본형을 예로들면 14진수이면서, "가나다라마바사아자차카타파하"로 표현되는것
+		new_dic = {}
+		for no, one_value in enumerate(show_letter):
+			new_dic[one_value] = no
+
+		total = 0
+		checked_input_num = reversed(input_num)
+		for no, one in enumerate(checked_input_num):
+			total = total + len(show_letter) ** (no) * new_dic[one]
+		return total
+
+	def delete_same_value_by_index(self, input_list2d, base_index):
+		waste_letters = [" ", ',', '.', '"', "'", ',', '?', '-']
+		result = []
+		only_one = set()
+		for one_list in input_list2d:
+			new_value = str(one_list[base_index])
+			for one in waste_letters:
+				new_value = new_value.replace(one, "")
+
+			if new_value in only_one:
+				print("같은것 찾음")
+			else:
+				result.append(one_list)
+				only_one.add(new_value)
 		return result
```

### Comparing `xython-1.4.0/src/xython.egg-info/PKG-INFO` & `xython-1.5.0/src/xython.egg-info/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,140 +1,142 @@
 Metadata-Version: 2.1
 Name: xython
-Version: 1.4.0
+Version: 1.5.0
 Summary: Easy Read / Write for Excel, Word, Color, Etc using Python
 Home-page: https://github.com/sjpark/xython
 Author: sjpark
 Author-email: sjpkorea@yahoo.com
 License: UNKNOWN
-Download-URL: https://github.com/sjpark/xython/archive/v1.4.0.tar.gz
-Description: ## xython 모듈에 대하여
-        ### 개괄적인 설명
-        이모듈은 업무용으로 많이 사용하는 엑셀 , 색, 정규표현식, 등에 대하여 Python과 win32com을 기본으로 사용하여 각기 새롭게 모듈을 만들어서 좀더 쉽고 편하게 사용하고 만들자는 것입니다
-        자동화는 각자의 사용에 대한  
-        
-        만든 이유는 우리가 업무등을 하는 입장에서, 손으로 작업하기에는 양이 많고, 그렇다고
-        계속 반복적으로 일어나는 일은 아니며, VBA등을 만들어서 사용하기에는 어렵고 힘든 부분에 대해서
-        
-        파이썬이라는 훌룡한 언어를 위용하여, 좀더 쉽고 간결하게 몇가지 기능만 배워도 20줄안으로 자신만의 코드를
-        만들어 사용할수있는 기준을 만들기 위한 것입니다
-        
-        또한 보통 많이 사용하는 코드들은 첨부된 sample코드를 보시거나 저의 사이트에 와서 비슷한것을 다운 받은후
-        변경해서 사용하시기를 추천 드립니다
-        
-        좀더 편한 업무의 일을 하기위한 것입니다
-        
-        ### 구성은 
-        
-            - pcell : 엑셀을 다루는 것
-            - pcell_event : 엑셀의 이벤트를 다루는것
-            - scolor : 색의 RGB값을 편하게 사용가능하도록 만든 것
-            - jfinder : 정규표현식을 좀더 편하게 사용하도록 만든 것
-            - anydb : sqlite와 pandas 를 좀더 쉽게 사용할수있도록 만든것
-            - ganada : 워드를 다루기위해 만든 것
-            - mailmail : outlook을 다루는것
-            - pyclick : 키보드와 마우스를 다루는 모듈
-            - pynal : 시간과 날짜를 다루는것
-            - youtil : 이러저런 문장이나 시간등을 변환하는데 도움이되는 것
-            - basic_data : halmoney패키지에서 사용되는 전반적인 공유 자료들을 저장하는 곳
-        
-        각 사용사용방법들에 대해서는 아래의 사이트를 참고하세요
-        
-        * https://cafe.naver.com/pycell
-        * www.halmoney.com
-        * www.xython.co.kr
-        
-        
-        ## 기본 사용법
-        ### pcell
-        -각 메소드는 각각 별도의 내용으로 사용합니다
-        
-        Pcell의 모듈을 만들 때 나름대로 편하고 쉽게 이름을 만들려고 하였습니다. 기본적인 틀을 만들어 놓으니, 분명억지로 지어진 이름또한 있음을 시인합니다. 나름대로 생각하고 고심한끝에 만들어진 이름이오니 맘에 들지 않는 부분이 있이더라도 양해를 부탁드립니다
-        
-        물론, 지금의 이름이 최종이라고는 생각하지 않고 있습니다. 좋은 이름이라는것은 어떤 메소드가 들어가 있는지 잘 몰라도 거의 사용하는데 사람의 생각에서 쉽게 사용을 할수 있도록 만드는 것이라고 생각을 합니다
-        
-        아마 한 4~5번정오는 크게 이름을 변경한 것 같습니다. 만들어놓고 조금지나면 저스스로가 도데체 이것의 이름은 왜 이렇게 만들어놓은거야???라는 질문을 하는경우가 가끔있습니다. 이리바꾸고 저리바꾸어도 맘에 안드는구석이 아직 많습니다
-        
-        한사람의 이름이 인생에서 차지하는부분이 많듯이 제가만든것또한 그러하지만, 만약 맘에 안드시는 것이 있으시면 본인스스로가 바꾼어서 사용하셔도 됩니다
-        
-        단, 기존의것은 그대로 두시고 아래부분에 새로운 메소드를 추가하셔서 위의것을 그대로 사용하시면 될것입니다
-        
-        그래서 다음과 같은 원리를 이용해서 만들었으나, 조금은 틀린부분도 있지만…
-        
-        	1. 이름은 기본적으로 3부분으로 만들었으며 각부분은 언더바(_)로 연결했습니다
-        	2. 읽을때는 read, 쓸때는 write, 삭제는 delete, 추가는insert등을 사용하였습니다
-        	3. 두번째의 이름의 규칙은
-        		관련된 부분에 따라 다른것을 사용하며 다음과 같은 것이 사용이 됩니다
-        		거진 영역을 나타내는 부분으로 사용하였습니다
-        		range, workbook, cell, line, column
-        	4. 세번째 부분이 어떤 일을 할것인지를 알아보는 것입니다
-        	5. 일반사항은 다음과 같습니다
-        
-        -	모든함수에는 sheet가 명시되어야 합니다
-        -	값을 읽는것은 read로 시작하며
-        -	값을 쓰는 것은 write로 시작합니다
-        -	선을 긋는등의 그림은 dwg로 시작합니다
-        -	하나의 자료가 아닌, 자료의 묶음은 Range를 사용한다
-        -	두개의 문구사이에는 '_' 로 연결을 하였다 예) read_cell
-        -	메소드는 모두 소문자를 사용함
-        
-        예를 들어, 어떤셀에 값을 입력하는 것은 write_value_in_cell라는 이름으로 구성하였습니다
-        그리고 부가적으로 함수의 변수로 사용되는부분은 큰 것->작은것으로 만들었으며, 영역을 표시하는 부분은 모두 리스트를 기준으로 하나로 만들었습니다.
-        
-        그저, 그렇다는것을 이해바라며, 실질적으로 코드를 보시면 더 쉽게 이해가 가실것으로 생각됩니다.
-        보지않고 찾지않아도 함수의 이름을 생각해낼수있도록 만든다고 나름대로 정의한 것입니다.
-        
-        ### scolor
-        이것은 모든 외부로 들어오고 나가는 것은 전부 RGB형태로 이루어지도록 만든다
-        
-            - 색을 변경하고 관리하는 모듈이며
-            - 색의 변화를 잘 사용이 가능하도록 하기위한 것이다
-            - 기본 입력 예 : "빨강", "빨강55", "red55", "0155"
-            - 기본색 ==> 12색 + (하양, 검정, 회색),
-            - 큰변화 ==> 1~9단계, 작은변화 ==> 1~9단계
-            - 기본함수 : get_color_rgb("red55"), get_rgb_3input(색, 큰변화, 작은변화)
-            - 모든 색의 표현이나 결과는 rgb로 돌려준다
-        
-        ### Jfinder
-        이름을 **Jfinder**라고 지었으며, 아래와 같은 특성을 가지고 있다
-        
-        1. 건수는 ~를 사용하여 4~5라는 식으로 표현을 하였고
-        2. 한글, 영어와 같은 것은 대괄호를 사용하여 적용하였다 [한글]
-        3. 처음과 끝은 [처음], [끝]처럼 나타냈다
-        4. 그리고 이것은 누가 보아도 아~~ 무엇을 찾을려고 했는지를 알수있도록 하기위한것이며
-        5. 찾기기능중에 전부 찾아서 보기쉽도록 돌려주는 것과 같은 몇가지 메소드들을 만들어 넣었읍니다
-        제일 중요한 코드를 만드는 기능은 아래와 같읍니다
-        대략적으로 위의것을 읽은후에 보시면 이해가 되실부분이 많읍니다
-        
-        * 아래의 코드들은 정규표현식을 사용하면서, 내가 만든 표현식조차도 다시 읽기가 어려워서, 나름 다른 형태로 만들어 본것인데. 생각보다 가독성이 좋아서 같이 공유해보는것이다
-        또한 만든김에 결과로 돌려주는것도 하나만 받으면 전부 가능하도록 만들어 보았다
-        위에서 언급한 이메일 형식이 맞느지를 보는 것은 상당히 반복적이기 때문에 크게 혼돈은 없다
-        하지만, 실제 코드를 사용하다 보면, 외계어를 해석하는 상태까지 와야할 경우가 있다
-        
-        
-            ([a-zA-Z0-9_.+-]+)@[a-zA-Z0-9_.+-]+\.[a-zA-Z0-9_.+-]+
-        
-        * 이정도만해도 간단한 축에 속한다. 맨처음 만들때는 그나마 이해를 하지만, 다른사람이 만든 것을 이해하는데 상당한 시간이 걸린다는 것이고, 또한 일반적인 사용자들이 이것을 공부하고 이해하는데 어려움이 잇을 것 같으면서 동시에, 정규표현식의 강력함을 사용할수 있도록 생각해 보는 것이다
-        그래서 좀더 간단하게 사용법을 만들고,
-        
-        
-            [영어&숫자.+-:1~]@[영어&숫자.+-:1~]\.[영어&숫자.+-:1~]
-        이렇게 바꾸면 좀더 읽기가 쉬워진다
-        
-        **jfinder**에는 자주사용하는 언어를 등록할수도 있읍니다. 예를 들어 일본어나 한자를 등록한것처럼 하면 사용이 가능하다.
-        간단하게 다시 사용하는 방법을 알려주면, 너무 줄여놓은 정규표현식을 좀더 늘이는 것이라고 생각하면 됩니다. 여기에서 느낀 부분은 전문가가 사용하기에는 좋지만, 비전문가가 사용하기 쉽게, 예전에는 단어1개가 아주 중요한 속도까지 영향을 주지만, 지금은너무 줄이지 않아도 된다는 것이다. 기계에 가까운 언어에서 좀더 사용자에 가까운 언어로 만들어도 된다는 것이지요
-        파이선이 사용하기에 좀더 편한방법이 되는 것이지요
-        
-            - 대괄호로 묶는다
-            - 반복갯수는 대괄호안에 사용하며 ~로 나타낸다
-            - 맨처음 맨마지막등의 용어는 [처음], [끝]등의 이유로 나타낸다 
-            - 특수문자(re모듈내에 의미가있는 문자)는 \를 붙여서 사용한다
-            - 어떤문자의 앞과뒤에있을때는 (앞에있음:abc)이라고 사용하면 abc가 앞에있는 문자열을 찾는것이다
-        
-        ### mailmail
-        이름을 **mailmail**라고 지었으며, 아웃룩의 이메일을 관리하는 도구입니다
-        - 이것의 장점은 엑셀이나 Util과 연동하여 편의성을 더욱 증대하고있읍니다
-        - 기본적인 사용법이나 함수의 이름은 같은 형태를 따릅니다
+Download-URL: https://github.com/sjpark/xython/archive/v1.5.0.tar.gz
 Platform: UNKNOWN
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
+
+## xython 모듈에 대하여
+### 개괄적인 설명
+이모듈은 업무용으로 많이 사용하는 엑셀 , 색, 정규표현식, 등에 대하여 Python과 win32com을 기본으로 사용하여 각기 새롭게 모듈을 만들어서 좀더 쉽고 편하게 사용하고 만들자는 것입니다
+자동화는 각자의 사용에 대한  
+
+만든 이유는 우리가 업무등을 하는 입장에서, 손으로 작업하기에는 양이 많고, 그렇다고
+계속 반복적으로 일어나는 일은 아니며, VBA등을 만들어서 사용하기에는 어렵고 힘든 부분에 대해서
+
+파이썬이라는 훌룡한 언어를 위용하여, 좀더 쉽고 간결하게 몇가지 기능만 배워도 20줄안으로 자신만의 코드를
+만들어 사용할수있는 기준을 만들기 위한 것입니다
+
+또한 보통 많이 사용하는 코드들은 첨부된 sample코드를 보시거나 저의 사이트에 와서 비슷한것을 다운 받은후
+변경해서 사용하시기를 추천 드립니다
+
+좀더 편한 업무의 일을 하기위한 것입니다
+
+### 구성은 
+
+    - pcell : 엑셀을 다루는 것
+    - pcell_event : 엑셀의 이벤트를 다루는것
+    - scolor : 색의 RGB값을 편하게 사용가능하도록 만든 것
+    - jfinder : 정규표현식을 좀더 편하게 사용하도록 만든 것
+    - anydb : sqlite와 pandas 를 좀더 쉽게 사용할수있도록 만든것
+    - ganada : 워드를 다루기위해 만든 것
+    - mailmail : outlook을 다루는것
+    - pyclick : 키보드와 마우스를 다루는 모듈
+    - pynal : 시간과 날짜를 다루는것
+    - youtil : 이러저런 문장이나 시간등을 변환하는데 도움이되는 것
+    - basic_data : halmoney패키지에서 사용되는 전반적인 공유 자료들을 저장하는 곳
+
+각 사용사용방법들에 대해서는 아래의 사이트를 참고하세요
+
+* https://cafe.naver.com/pycell
+* www.halmoney.com
+* www.xython.co.kr
+
+
+## 기본 사용법
+### pcell
+-각 메소드는 각각 별도의 내용으로 사용합니다
+
+Pcell의 모듈을 만들 때 나름대로 편하고 쉽게 이름을 만들려고 하였습니다. 기본적인 틀을 만들어 놓으니, 분명억지로 지어진 이름또한 있음을 시인합니다. 나름대로 생각하고 고심한끝에 만들어진 이름이오니 맘에 들지 않는 부분이 있이더라도 양해를 부탁드립니다
+
+물론, 지금의 이름이 최종이라고는 생각하지 않고 있습니다. 좋은 이름이라는것은 어떤 메소드가 들어가 있는지 잘 몰라도 거의 사용하는데 사람의 생각에서 쉽게 사용을 할수 있도록 만드는 것이라고 생각을 합니다
+
+아마 한 4~5번정오는 크게 이름을 변경한 것 같습니다. 만들어놓고 조금지나면 저스스로가 도데체 이것의 이름은 왜 이렇게 만들어놓은거야???라는 질문을 하는경우가 가끔있습니다. 이리바꾸고 저리바꾸어도 맘에 안드는구석이 아직 많습니다
+
+한사람의 이름이 인생에서 차지하는부분이 많듯이 제가만든것또한 그러하지만, 만약 맘에 안드시는 것이 있으시면 본인스스로가 바꾼어서 사용하셔도 됩니다
+
+단, 기존의것은 그대로 두시고 아래부분에 새로운 메소드를 추가하셔서 위의것을 그대로 사용하시면 될것입니다
+
+그래서 다음과 같은 원리를 이용해서 만들었으나, 조금은 틀린부분도 있지만…
+
+	1. 이름은 기본적으로 3부분으로 만들었으며 각부분은 언더바(_)로 연결했습니다
+	2. 읽을때는 read, 쓸때는 write, 삭제는 delete, 추가는insert등을 사용하였습니다
+	3. 두번째의 이름의 규칙은
+		관련된 부분에 따라 다른것을 사용하며 다음과 같은 것이 사용이 됩니다
+		거진 영역을 나타내는 부분으로 사용하였습니다
+		range, workbook, cell, line, column
+	4. 세번째 부분이 어떤 일을 할것인지를 알아보는 것입니다
+	5. 일반사항은 다음과 같습니다
+
+-	모든함수에는 sheet가 명시되어야 합니다
+-	값을 읽는것은 read로 시작하며
+-	값을 쓰는 것은 write로 시작합니다
+-	선을 긋는등의 그림은 dwg로 시작합니다
+-	하나의 자료가 아닌, 자료의 묶음은 Range를 사용한다
+-	두개의 문구사이에는 '_' 로 연결을 하였다 예) read_cell
+-	메소드는 모두 소문자를 사용함
+
+예를 들어, 어떤셀에 값을 입력하는 것은 write_value_in_cell라는 이름으로 구성하였습니다
+그리고 부가적으로 함수의 변수로 사용되는부분은 큰 것->작은것으로 만들었으며, 영역을 표시하는 부분은 모두 리스트를 기준으로 하나로 만들었습니다.
+
+그저, 그렇다는것을 이해바라며, 실질적으로 코드를 보시면 더 쉽게 이해가 가실것으로 생각됩니다.
+보지않고 찾지않아도 함수의 이름을 생각해낼수있도록 만든다고 나름대로 정의한 것입니다.
+
+### scolor
+이것은 모든 외부로 들어오고 나가는 것은 전부 RGB형태로 이루어지도록 만든다
+
+    - 색을 변경하고 관리하는 모듈이며
+    - 색의 변화를 잘 사용이 가능하도록 하기위한 것이다
+    - 기본 입력 예 : "빨강", "빨강55", "red55", "0155"
+    - 기본색 ==> 12색 + (하양, 검정, 회색),
+    - 큰변화 ==> 1~9단계, 작은변화 ==> 1~9단계
+    - 기본함수 : get_color_rgb("red55"), get_rgb_3input(색, 큰변화, 작은변화)
+    - 모든 색의 표현이나 결과는 rgb로 돌려준다
+
+### Jfinder
+이름을 **Jfinder**라고 지었으며, 아래와 같은 특성을 가지고 있다
+
+1. 건수는 ~를 사용하여 4~5라는 식으로 표현을 하였고
+2. 한글, 영어와 같은 것은 대괄호를 사용하여 적용하였다 [한글]
+3. 처음과 끝은 [처음], [끝]처럼 나타냈다
+4. 그리고 이것은 누가 보아도 아~~ 무엇을 찾을려고 했는지를 알수있도록 하기위한것이며
+5. 찾기기능중에 전부 찾아서 보기쉽도록 돌려주는 것과 같은 몇가지 메소드들을 만들어 넣었읍니다
+제일 중요한 코드를 만드는 기능은 아래와 같읍니다
+대략적으로 위의것을 읽은후에 보시면 이해가 되실부분이 많읍니다
+
+* 아래의 코드들은 정규표현식을 사용하면서, 내가 만든 표현식조차도 다시 읽기가 어려워서, 나름 다른 형태로 만들어 본것인데. 생각보다 가독성이 좋아서 같이 공유해보는것이다
+또한 만든김에 결과로 돌려주는것도 하나만 받으면 전부 가능하도록 만들어 보았다
+위에서 언급한 이메일 형식이 맞느지를 보는 것은 상당히 반복적이기 때문에 크게 혼돈은 없다
+하지만, 실제 코드를 사용하다 보면, 외계어를 해석하는 상태까지 와야할 경우가 있다
+
+
+    ([a-zA-Z0-9_.+-]+)@[a-zA-Z0-9_.+-]+\.[a-zA-Z0-9_.+-]+
+
+* 이정도만해도 간단한 축에 속한다. 맨처음 만들때는 그나마 이해를 하지만, 다른사람이 만든 것을 이해하는데 상당한 시간이 걸린다는 것이고, 또한 일반적인 사용자들이 이것을 공부하고 이해하는데 어려움이 잇을 것 같으면서 동시에, 정규표현식의 강력함을 사용할수 있도록 생각해 보는 것이다
+그래서 좀더 간단하게 사용법을 만들고,
+
+
+    [영어&숫자.+-:1~]@[영어&숫자.+-:1~]\.[영어&숫자.+-:1~]
+이렇게 바꾸면 좀더 읽기가 쉬워진다
+
+**jfinder**에는 자주사용하는 언어를 등록할수도 있읍니다. 예를 들어 일본어나 한자를 등록한것처럼 하면 사용이 가능하다.
+간단하게 다시 사용하는 방법을 알려주면, 너무 줄여놓은 정규표현식을 좀더 늘이는 것이라고 생각하면 됩니다. 여기에서 느낀 부분은 전문가가 사용하기에는 좋지만, 비전문가가 사용하기 쉽게, 예전에는 단어1개가 아주 중요한 속도까지 영향을 주지만, 지금은너무 줄이지 않아도 된다는 것이다. 기계에 가까운 언어에서 좀더 사용자에 가까운 언어로 만들어도 된다는 것이지요
+파이선이 사용하기에 좀더 편한방법이 되는 것이지요
+
+    - 대괄호로 묶는다
+    - 반복갯수는 대괄호안에 사용하며 ~로 나타낸다
+    - 맨처음 맨마지막등의 용어는 [처음], [끝]등의 이유로 나타낸다 
+    - 특수문자(re모듈내에 의미가있는 문자)는 \를 붙여서 사용한다
+    - 어떤문자의 앞과뒤에있을때는 (앞에있음:abc)이라고 사용하면 abc가 앞에있는 문자열을 찾는것이다
+
+### mailmail
+이름을 **mailmail**라고 지었으며, 아웃룩의 이메일을 관리하는 도구입니다
+- 이것의 장점은 엑셀이나 Util과 연동하여 편의성을 더욱 증대하고있읍니다
+- 기본적인 사용법이나 함수의 이름은 같은 형태를 따릅니다
+
```

