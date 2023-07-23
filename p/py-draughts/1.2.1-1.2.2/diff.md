# Comparing `tmp/py-draughts-1.2.1.tar.gz` & `tmp/py-draughts-1.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "py-draughts-1.2.1.tar", last modified: Fri Jul 21 15:01:08 2023, max compression
+gzip compressed data, was "py-draughts-1.2.2.tar", last modified: Sun Jul 23 17:09:07 2023, max compression
```

## Comparing `py-draughts-1.2.1.tar` & `py-draughts-1.2.2.tar`

### file list

```diff
@@ -1,36 +1,36 @@
-drwxrwxrwx   0        0        0        0 2023-07-21 15:01:08.952460 py-draughts-1.2.1/
--rw-rw-rw-   0        0        0    35823 2023-07-11 12:53:30.000000 py-draughts-1.2.1/LICENSE
--rw-rw-rw-   0        0        0       43 2023-07-16 09:45:04.000000 py-draughts-1.2.1/MANIFEST.in
--rw-rw-rw-   0        0        0     5139 2023-07-21 15:01:08.951460 py-draughts-1.2.1/PKG-INFO
--rw-rw-rw-   0        0        0     3716 2023-07-21 15:00:24.000000 py-draughts-1.2.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-21 15:01:08.903446 py-draughts-1.2.1/draughts/
--rw-rw-rw-   0        0        0     1585 2023-07-21 15:00:47.000000 py-draughts-1.2.1/draughts/__init__.py
--rw-rw-rw-   0        0        0     3740 2023-07-21 14:37:08.000000 py-draughts-1.2.1/draughts/american.py
--rw-rw-rw-   0        0        0    13510 2023-07-21 14:37:08.000000 py-draughts-1.2.1/draughts/base.py
--rw-rw-rw-   0        0        0     3695 2023-07-21 14:37:08.000000 py-draughts-1.2.1/draughts/engine.py
--rw-rw-rw-   0        0        0      671 2023-07-16 18:11:48.000000 py-draughts-1.2.1/draughts/models.py
--rw-rw-rw-   0        0        0     4179 2023-07-21 14:37:08.000000 py-draughts-1.2.1/draughts/move.py
--rw-rw-rw-   0        0        0     5541 2023-07-21 15:00:27.000000 py-draughts-1.2.1/draughts/server.py
--rw-rw-rw-   0        0        0     8403 2023-07-21 14:37:08.000000 py-draughts-1.2.1/draughts/standard.py
-drwxrwxrwx   0        0        0        0 2023-07-21 15:01:08.865479 py-draughts-1.2.1/draughts/static/
-drwxrwxrwx   0        0        0        0 2023-07-21 15:01:08.910417 py-draughts-1.2.1/draughts/static/css/
--rw-rw-rw-   0        0        0     3873 2023-07-16 09:45:04.000000 py-draughts-1.2.1/draughts/static/css/style.css
-drwxrwxrwx   0        0        0        0 2023-07-21 15:01:08.912833 py-draughts-1.2.1/draughts/static/js/
--rw-rw-rw-   0        0        0     6250 2023-07-21 14:37:08.000000 py-draughts-1.2.1/draughts/static/js/script.js
-drwxrwxrwx   0        0        0        0 2023-07-21 15:01:08.915835 py-draughts-1.2.1/draughts/templates/
--rw-rw-rw-   0        0        0     1860 2023-07-11 16:32:17.000000 py-draughts-1.2.1/draughts/templates/base.html
--rw-rw-rw-   0        0        0     2882 2023-07-16 09:45:04.000000 py-draughts-1.2.1/draughts/templates/index.html
--rw-rw-rw-   0        0        0     1973 2023-07-16 10:59:23.000000 py-draughts-1.2.1/draughts/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-21 15:01:08.928362 py-draughts-1.2.1/py_draughts.egg-info/
--rw-rw-rw-   0        0        0     5139 2023-07-21 15:01:08.000000 py-draughts-1.2.1/py_draughts.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      594 2023-07-21 15:01:08.000000 py-draughts-1.2.1/py_draughts.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-21 15:01:08.000000 py-draughts-1.2.1/py_draughts.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       44 2023-07-21 15:01:08.000000 py-draughts-1.2.1/py_draughts.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-07-21 15:01:08.000000 py-draughts-1.2.1/py_draughts.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       48 2023-07-16 19:28:37.000000 py-draughts-1.2.1/requirements.txt
--rw-rw-rw-   0        0        0       42 2023-07-21 15:01:08.952460 py-draughts-1.2.1/setup.cfg
--rw-rw-rw-   0        0        0     1911 2023-07-18 21:34:49.000000 py-draughts-1.2.1/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-21 15:01:08.948951 py-draughts-1.2.1/test/
--rw-rw-rw-   0        0        0     1104 2023-07-16 18:39:54.000000 py-draughts-1.2.1/test/test_american_board.py
--rw-rw-rw-   0        0        0     2510 2023-07-21 14:37:08.000000 py-draughts-1.2.1/test/test_board.py
--rw-rw-rw-   0        0        0     1370 2023-07-21 14:37:08.000000 py-draughts-1.2.1/test/test_standard_board.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:07.760854 py-draughts-1.2.2/
+-rw-rw-rw-   0        0        0    35823 2023-07-11 12:53:30.000000 py-draughts-1.2.2/LICENSE
+-rw-rw-rw-   0        0        0       43 2023-07-16 09:45:04.000000 py-draughts-1.2.2/MANIFEST.in
+-rw-rw-rw-   0        0        0     5139 2023-07-23 17:09:07.759858 py-draughts-1.2.2/PKG-INFO
+-rw-rw-rw-   0        0        0     3716 2023-07-21 15:00:24.000000 py-draughts-1.2.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:07.695814 py-draughts-1.2.2/draughts/
+-rw-rw-rw-   0        0        0     1585 2023-07-23 17:08:58.000000 py-draughts-1.2.2/draughts/__init__.py
+-rw-rw-rw-   0        0        0     3740 2023-07-21 17:07:24.000000 py-draughts-1.2.2/draughts/american.py
+-rw-rw-rw-   0        0        0    14044 2023-07-23 11:21:41.000000 py-draughts-1.2.2/draughts/base.py
+-rw-rw-rw-   0        0        0     3772 2023-07-23 17:08:13.000000 py-draughts-1.2.2/draughts/engine.py
+-rw-rw-rw-   0        0        0      671 2023-07-16 18:11:48.000000 py-draughts-1.2.2/draughts/models.py
+-rw-rw-rw-   0        0        0     4212 2023-07-23 17:05:13.000000 py-draughts-1.2.2/draughts/move.py
+-rw-rw-rw-   0        0        0     5626 2023-07-23 17:05:33.000000 py-draughts-1.2.2/draughts/server.py
+-rw-rw-rw-   0        0        0     8084 2023-07-23 11:21:41.000000 py-draughts-1.2.2/draughts/standard.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:07.635242 py-draughts-1.2.2/draughts/static/
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:07.702844 py-draughts-1.2.2/draughts/static/css/
+-rw-rw-rw-   0        0        0     3873 2023-07-16 09:45:04.000000 py-draughts-1.2.2/draughts/static/css/style.css
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:07.717855 py-draughts-1.2.2/draughts/static/js/
+-rw-rw-rw-   0        0        0     6250 2023-07-21 14:37:08.000000 py-draughts-1.2.2/draughts/static/js/script.js
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:07.720824 py-draughts-1.2.2/draughts/templates/
+-rw-rw-rw-   0        0        0     1860 2023-07-11 16:32:17.000000 py-draughts-1.2.2/draughts/templates/base.html
+-rw-rw-rw-   0        0        0     2882 2023-07-16 09:45:04.000000 py-draughts-1.2.2/draughts/templates/index.html
+-rw-rw-rw-   0        0        0     1973 2023-07-16 10:59:23.000000 py-draughts-1.2.2/draughts/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:07.737854 py-draughts-1.2.2/py_draughts.egg-info/
+-rw-rw-rw-   0        0        0     5139 2023-07-23 17:09:07.000000 py-draughts-1.2.2/py_draughts.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      594 2023-07-23 17:09:07.000000 py-draughts-1.2.2/py_draughts.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 17:09:07.000000 py-draughts-1.2.2/py_draughts.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       44 2023-07-23 17:09:07.000000 py-draughts-1.2.2/py_draughts.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 17:09:07.000000 py-draughts-1.2.2/py_draughts.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       48 2023-07-16 19:28:37.000000 py-draughts-1.2.2/requirements.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 17:09:07.760854 py-draughts-1.2.2/setup.cfg
+-rw-rw-rw-   0        0        0     1911 2023-07-18 21:34:49.000000 py-draughts-1.2.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:07.758854 py-draughts-1.2.2/test/
+-rw-rw-rw-   0        0        0     1104 2023-07-16 18:39:54.000000 py-draughts-1.2.2/test/test_american_board.py
+-rw-rw-rw-   0        0        0     2510 2023-07-23 11:21:41.000000 py-draughts-1.2.2/test/test_board.py
+-rw-rw-rw-   0        0        0     1370 2023-07-23 11:21:41.000000 py-draughts-1.2.2/test/test_standard_board.py
```

### Comparing `py-draughts-1.2.1/LICENSE` & `py-draughts-1.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/PKG-INFO` & `py-draughts-1.2.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-draughts
-Version: 1.2.1
+Version: 1.2.2
 Summary: A draughts library with advenced (customizable) WEB UI move generation and validation, PDN parsing and writing. Supports multiple variants of game.
 Home-page: https://github.com/michalskibinski109/py-draughts
 Author: Michał Skibiński
 Author-email: mskibinski109@gmail.com
 License: GPL-3.0+
 Project-URL: Documentation, https://michalskibinski109.github.io/py-draughts/index.html
 Keywords: draughts,checkers,AI mini-max,game,board
```

### Comparing `py-draughts-1.2.1/README.md` & `py-draughts-1.2.2/README.md`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/draughts/__init__.py` & `py-draughts-1.2.2/draughts/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 """
 A draughts library with advenced (customizable) WEB UI move generation and validation,
 PDN parsing and writing. Supports multiple variants of game.
 """
 
 from typing import Literal
 
-__version__ = "1.2.1"
+__version__ = "1.2.2"
 __author__ = "Michał Skibiński"
 
 
 def get_board(variant: Literal["standard", "american"], fen: str = None):
     """
     Board factory method.
     - ``standard`` - standard draughts board
```

### Comparing `py-draughts-1.2.1/draughts/american.py` & `py-draughts-1.2.2/draughts/american.py`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/draughts/base.py` & `py-draughts-1.2.2/draughts/base.py`

 * *Files 2% similar despite different names*

```diff
@@ -53,14 +53,17 @@
         - ``PieceType.MAN``
         - ``PieceType.KING``
     - **Board should always be square.**
     .. note::
         For generating legal moves use
     """
 
+    halfmove_clock: int = 0
+    """The number of half-moves since the last capture or pawn move."""
+
     GAME_TYPE = -1
     """
     PDN game type. See `PDN specification <https://en.wikipedia.org/wiki/Portable_Draughts_Notation>`_.
     """
     VARIANT_NAME = "Abstract variant"
     STARTING_POSITION = np.array([1] * 12 + [0] * 8 + [-1] * 12, dtype=np.int8)
     ROW_IDX = ...
@@ -130,14 +133,15 @@
             msg = f"Invalid board with shape {self._pos.shape} provided.\
                 Please use an array with lenght = (n * n/2). \
                 Where n is an size of the board."
             logger.error(msg)
             raise ValueError(msg)
         self.shape = (size, size)
         self._moves_stack: list[Move] = []
+
         logger.info(f"Board initialized with shape {self.shape}.")
 
     # @abstractmethod
     @abstractproperty
     def legal_moves(self) -> Generator[Move, None, None]:
         """
         Return list legal moves for the current position.
@@ -162,15 +166,15 @@
                 self._moves_stack[-1].square_list
                 == self._moves_stack[-5].square_list
                 == self._moves_stack[-9].square_list
             ):
                 return True
         return False
 
-    @property
+    @abstractproperty
     def is_draw(self) -> bool:
         raise NotImplementedError
 
     @property
     def game_over(self) -> bool:
         """Returns ``True`` if the game is over."""
         # check if threefold repetition
@@ -182,14 +186,15 @@
     ) -> None:  # TODO multiple captures != promotion
         """Pushes a move to the board.
         Automatically promotes a piece if it reaches the last row.
 
         If ``is_finished`` is set to ``True``, the turn is switched. This parameter is used only
         for generating legal moves.
         """
+        move.halfmove_clock = self.halfmove_clock  # Before move occurs
         src, tg = (
             move.square_list[0],
             move.square_list[-1],
         )
         self._pos[src], self._pos[tg] = self._pos[tg], self._pos[src]
         # is promotion
         if (
@@ -199,16 +204,26 @@
         ) or (
             (tg // (self.shape[0] // 2)) == (self.shape[0] - 1)
             and self._pos[tg] == Figure.BLACK_MAN.value
             and is_finished
         ):
             self._pos[tg] *= Figure.KING.value
             move.is_promotion = True
+        elif (
+            abs(self._pos[tg]) == Figure.KING.value
+            and not move.captured_list
+            and is_finished
+        ):
+            self.halfmove_clock += 1
+        elif is_finished:
+            self.halfmove_clock = 0
         if move.captured_list:
-            self._pos[np.array([sq for sq in move.captured_list])] = Figure.EMPTY
+            self._pos[
+                np.array([sq for sq in move.captured_list if sq != tg])
+            ] = Figure.EMPTY
         self._moves_stack.append(move)
         if is_finished:
             self.turn = Color.WHITE if self.turn == Color.BLACK else Color.BLACK
 
     def pop(self, is_finished=True) -> None:
         """Pops a move from the board.
 
@@ -219,14 +234,15 @@
         src, tg = (
             move.square_list[0],
             move.square_list[-1],
         )
         if move.is_promotion:
             self._pos[tg] //= Figure.KING.value
         self._pos[src], self._pos[tg] = self._pos[tg], self._pos[src]
+        self.halfmove_clock = move.halfmove_clock
         for sq, entity in zip(move.captured_list, move.captured_entities):
             self._pos[sq] = entity  # Dangerous line
         if is_finished:
             self.turn = Color.WHITE if self.turn == Color.BLACK else Color.BLACK
         return move
 
     def push_uci(self, str_move: str) -> None:
```

### Comparing `py-draughts-1.2.1/draughts/engine.py` & `py-draughts-1.2.2/draughts/engine.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 from abc import ABC, abstractmethod
 
 from tqdm import tqdm
-from draughts.standard import Board, Move
+from draughts.standard import Board, Move, Figure
 from draughts.models import Color
 from draughts.utils import logger
+import numpy as np
 
 
 class Engine(ABC):
     """
     Interface for engine compatible with Server class.
     """
 
@@ -27,14 +28,17 @@
     Engine using alpha-beta puring algorithm.
     *Alpha-beta puring is a minimax algorithm with optimization. Algorithm
     will not inspect nodes that are worse than already inspected nodes.
     Additionaly, this engine will inspect capture moves first.
     Usually, those moves are better than non-capture moves.*
     """
 
+    WHITE_WIN = -100 * Color.WHITE.value
+    BLACK_WIN = -100 * Color.BLACK.value
+
     def __init__(self, depth):
         """
         ``depth`` - how many moves will be inspected by engine.
         Bigger depth means better moves, but also longer calculation time.
         """
         self.depth = depth
         self.inspected_nodes = 0
@@ -87,29 +91,27 @@
         )
         return legal_moves[index], evals[index]
 
     def __alpha_beta_puring(
         self, board: Board, depth: int, alpha: float, beta: float
     ) -> float:
         if board.game_over:
-            return -100 if board.turn == Color.WHITE else 100
+            if not board.is_draw:
+                return -100 * board.turn.value
+            return -0.2 * board.turn.value
         if depth == 0:
             self.inspected_nodes += 1
             return self.evaluate(board)
         legal_moves = list(board.legal_moves)
-        tmp = board._pos.copy().sum()
 
         for move in legal_moves:
             board.push(move)
             evaluation = self.__alpha_beta_puring(board, depth - 1, alpha, beta)
+            evaluation -= np.abs(board.position[move.square_list[-1]]) == Figure.KING
             board.pop()
-            if board._pos.sum() != tmp:
-                logger.warning(str(board))
-                logger.error(f"{move}")
-                break
             if board.turn == Color.WHITE:
                 alpha = max(alpha, evaluation)
             else:
                 beta = min(beta, evaluation)
             if beta <= alpha:
                 break
         return alpha if board.turn == Color.WHITE else beta
```

### Comparing `py-draughts-1.2.1/draughts/models.py` & `py-draughts-1.2.2/draughts/models.py`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/draughts/move.py` & `py-draughts-1.2.2/draughts/move.py`

 * *Files 2% similar despite different names*

```diff
@@ -31,14 +31,15 @@
         captured_entities: list[Figure.value] = [],
         is_promotion: bool = False,
     ) -> None:
         self.square_list = visited_squares
         self.captured_list = captured_list
         self.captured_entities = captured_entities
         self.is_promotion = is_promotion
+        self.halfmove_clock = 0
 
     def __repr__(self) -> str:
         visited_squares = [str(s + 1) for s in self.square_list]
         return f"Move: {'->'.join(visited_squares)}"
 
     def __eq__(self, other: object) -> bool:
         """Check if two moves are equal. move created from string will have only visited squares definied."""
```

### Comparing `py-draughts-1.2.1/draughts/server.py` & `py-draughts-1.2.2/draughts/server.py`

 * *Files 2% similar despite different names*

```diff
@@ -143,10 +143,12 @@
         uvicorn.run(self.APP, **kwargs)
 
 
 if __name__ == "__main__":
     from draughts.engine import AlphaBetaEngine
     from draughts import get_board
 
-    engine = AlphaBetaEngine(depth=2)
+    # fen = "W:W:WK5,45,48,50:BK2,K4"
+    engine = AlphaBetaEngine(depth=3)
+    # board = get_board("standard", fen=fen)
     server = Server(get_best_move_method=engine.get_best_move)
     server.run()
```

### Comparing `py-draughts-1.2.1/draughts/standard.py` & `py-draughts-1.2.2/draughts/standard.py`

 * *Files 4% similar despite different names*

```diff
@@ -74,45 +74,40 @@
             or self.is_5_moves_rule
             or self.is_16_moves_rule
             or self.is_25_moves_rule
         )
 
     @property
     def is_25_moves_rule(self) -> bool:
-        if len(self._moves_stack) < 50:
+        if self.halfmove_clock < 50:
             return False
-        for move in self._moves_stack[-50:]:
-            src = move.square_list[-1]
-            if move.captured_list or self._pos[src] != Figure.KING.value:
-                return False
         logger.debug("25 moves rule")
         return True
+        # return self.halfmove_clock >= 50
 
     @property
     def is_16_moves_rule(self) -> bool:
-        if len(self._moves_stack) < 32 or len(self._pos[self._pos != Figure.EMPTY]) > 4:
+        if self.halfmove_clock < 32:
+            return False
+        if len(self._pos[self._pos != Figure.EMPTY]) > 4:
             return False
         if np.abs(self._pos).sum() < Figure.KING.value * 2 + Figure.MAN.value * 2:
             return False
-        for move in self._moves_stack[-32:]:
-            if move.captured_list or move.is_promotion:
-                return False
         logger.debug("16 moves rule")
         return True
 
     @property
     def is_5_moves_rule(self) -> bool:
         # if count of pieces is not 3 or 4
         if len(self._pos[self._pos != Figure.EMPTY]) > 3:
             return False
         if np.abs(self._pos).sum() < Figure.KING.value * 2 + Figure.MAN.value:
             return False
-        for move in self._moves_stack[-10:]:
-            if move.captured_list or move.is_promotion:
-                return False
+        if self.halfmove_clock < 10:
+            return False
         logger.debug("5 moves rule")
         return True
 
     @property
     def legal_moves(self) -> list[Move]:
         all_moves = []
         is_capture_mandatory = False
```

### Comparing `py-draughts-1.2.1/draughts/static/css/style.css` & `py-draughts-1.2.2/draughts/static/css/style.css`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/draughts/static/js/script.js` & `py-draughts-1.2.2/draughts/static/js/script.js`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/draughts/templates/base.html` & `py-draughts-1.2.2/draughts/templates/base.html`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/draughts/templates/index.html` & `py-draughts-1.2.2/draughts/templates/index.html`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/draughts/utils.py` & `py-draughts-1.2.2/draughts/utils.py`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/py_draughts.egg-info/PKG-INFO` & `py-draughts-1.2.2/py_draughts.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py-draughts
-Version: 1.2.1
+Version: 1.2.2
 Summary: A draughts library with advenced (customizable) WEB UI move generation and validation, PDN parsing and writing. Supports multiple variants of game.
 Home-page: https://github.com/michalskibinski109/py-draughts
 Author: Michał Skibiński
 Author-email: mskibinski109@gmail.com
 License: GPL-3.0+
 Project-URL: Documentation, https://michalskibinski109.github.io/py-draughts/index.html
 Keywords: draughts,checkers,AI mini-max,game,board
```

### Comparing `py-draughts-1.2.1/py_draughts.egg-info/SOURCES.txt` & `py-draughts-1.2.2/py_draughts.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/setup.py` & `py-draughts-1.2.2/setup.py`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/test/test_american_board.py` & `py-draughts-1.2.2/test/test_american_board.py`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/test/test_board.py` & `py-draughts-1.2.2/test/test_board.py`

 * *Files identical despite different names*

### Comparing `py-draughts-1.2.1/test/test_standard_board.py` & `py-draughts-1.2.2/test/test_standard_board.py`

 * *Files identical despite different names*

