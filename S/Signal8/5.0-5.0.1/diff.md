# Comparing `tmp/Signal8-5.0.tar.gz` & `tmp/Signal8-5.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Signal8-5.0.tar", last modified: Sat Jul 22 23:23:38 2023, max compression
+gzip compressed data, was "Signal8-5.0.1.tar", last modified: Sun Jul 23 00:45:18 2023, max compression
```

## Comparing `Signal8-5.0.tar` & `Signal8-5.0.1.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 23:23:38.869955 Signal8-5.0/
--rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-5.0/LICENSE
--rw-rw-rw-   0        0        0     5298 2023-07-22 23:23:38.864954 Signal8-5.0/PKG-INFO
--rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-5.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 23:23:38.741957 Signal8-5.0/Signal8/
--rw-rw-rw-   0        0        0    11124 2023-07-22 23:21:54.000000 Signal8-5.0/Signal8/Signal8.py
--rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-5.0/Signal8/__init__.py
--rw-rw-rw-   0        0        0      246 2023-07-22 23:19:37.000000 Signal8-5.0/Signal8/main.py
-drwxrwxrwx   0        0        0        0 2023-07-22 23:23:38.849957 Signal8-5.0/Signal8/utils/
--rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-5.0/Signal8/utils/__init__.py
--rw-rw-rw-   0        0        0     5285 2023-07-14 01:01:24.000000 Signal8-5.0/Signal8/utils/core.py
--rw-rw-rw-   0        0        0     2326 2023-07-22 22:51:42.000000 Signal8-5.0/Signal8/utils/problems.py
--rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-5.0/Signal8/utils/scenario.py
--rw-rw-rw-   0        0        0    11960 2023-07-13 18:01:37.000000 Signal8-5.0/Signal8/utils/simple_env.py
--rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-5.0/Signal8/utils/test_dynamic_obs.py
-drwxrwxrwx   0        0        0        0 2023-07-22 23:23:38.791954 Signal8-5.0/Signal8.egg-info/
--rw-rw-rw-   0        0        0     5298 2023-07-22 23:23:38.000000 Signal8-5.0/Signal8.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      510 2023-07-22 23:23:38.000000 Signal8-5.0/Signal8.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 23:23:38.000000 Signal8-5.0/Signal8.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-07-22 23:23:38.000000 Signal8-5.0/Signal8.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-22 23:23:38.870955 Signal8-5.0/setup.cfg
--rw-rw-rw-   0        0        0      645 2023-07-22 23:22:35.000000 Signal8-5.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:45:18.358195 Signal8-5.0.1/
+-rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-5.0.1/LICENSE
+-rw-rw-rw-   0        0        0     5300 2023-07-23 00:45:18.342193 Signal8-5.0.1/PKG-INFO
+-rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-5.0.1/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 00:45:18.238193 Signal8-5.0.1/Signal8/
+-rw-rw-rw-   0        0        0    11418 2023-07-23 00:42:01.000000 Signal8-5.0.1/Signal8/Signal8.py
+-rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-5.0.1/Signal8/__init__.py
+-rw-rw-rw-   0        0        0     3252 2023-07-23 00:27:57.000000 Signal8-5.0.1/Signal8/main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:45:18.337193 Signal8-5.0.1/Signal8/utils/
+-rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-5.0.1/Signal8/utils/__init__.py
+-rw-rw-rw-   0        0        0     5299 2023-07-22 23:36:30.000000 Signal8-5.0.1/Signal8/utils/core.py
+-rw-rw-rw-   0        0        0     2326 2023-07-23 00:27:30.000000 Signal8-5.0.1/Signal8/utils/problems.py
+-rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-5.0.1/Signal8/utils/scenario.py
+-rw-rw-rw-   0        0        0    11976 2023-07-22 23:36:18.000000 Signal8-5.0.1/Signal8/utils/simple_env.py
+-rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-5.0.1/Signal8/utils/test_dynamic_obs.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:45:18.297193 Signal8-5.0.1/Signal8.egg-info/
+-rw-rw-rw-   0        0        0     5300 2023-07-23 00:45:17.000000 Signal8-5.0.1/Signal8.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      510 2023-07-23 00:45:18.000000 Signal8-5.0.1/Signal8.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 00:45:17.000000 Signal8-5.0.1/Signal8.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 00:45:17.000000 Signal8-5.0.1/Signal8.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 00:45:18.359193 Signal8-5.0.1/setup.cfg
+-rw-rw-rw-   0        0        0      647 2023-07-23 00:44:56.000000 Signal8-5.0.1/setup.py
```

### Comparing `Signal8-5.0/LICENSE` & `Signal8-5.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `Signal8-5.0/PKG-INFO` & `Signal8-5.0.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 5.0
+Version: 5.0.1
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
```

### Comparing `Signal8-5.0/README.md` & `Signal8-5.0.1/README.md`

 * *Files identical despite different names*

### Comparing `Signal8-5.0/Signal8/Signal8.py` & `Signal8-5.0.1/Signal8/Signal8.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import numpy as np
 import matplotlib.path as mpath
 
 from functools import partial
-from .utils.scenario import BaseScenario
-from .utils.simple_env import SimpleEnv, make_env
-from .utils.core import Agent, Goal, Obstacle, World
-from .utils.problems import get_problem_list, get_problem_instance
+from utils.scenario import BaseScenario
+from utils.simple_env import SimpleEnv, make_env
+from utils.core import Agent, Goal, Obstacle, World
+from utils.problems import get_problem_list, get_problem_instance
 
 from gymnasium.utils import EzPickle
 
 
 class raw_env(SimpleEnv, EzPickle):
     def __init__(
         self, 
@@ -51,27 +51,27 @@
             goal.name = f"goal_{i}"
             goal.collide = False
             goal.color = np.array([0.835, 0.90, 0.831])
             world.goals.append(goal)
         
         # Large obstacles can only be observed by aerial agent
         for i in range(num_large_obstacles):
-            obstacle = Obstacle(size=0.1)
+            obstacle = Obstacle(radius=0.05)
             obstacle.name = f"obs_{i}"
             obstacle.color = np.array([0.97, 0.801, 0.8])
             world.large_obstacles.append(obstacle)
         
         # Small obstacles can only be observed by ground agent(s)
         for i in range(num_small_obstacles):
-            obstacle = Obstacle(size=0.02)
+            obstacle = Obstacle(radius=0.02)
             obstacle.name = f"obs_{i}"
             obstacle.color = np.array([0.97, 0.801, 0.8])
             world.small_obstacles.append(obstacle)    
         
-        world.buffer_dist = world.agents[0].size + world.large_obstacles[0].size
+        world.buffer_dist = world.agents[0].radius + world.large_obstacles[0].radius
         return world
     
     # Get constraints on entities given problem instance name
     def _set_problem_instance(self, world, instance_name):
         instance_constr = get_problem_instance(instance_name)
         world.problem_instance = instance_name
         world.instance_constr = instance_constr
@@ -81,31 +81,38 @@
         while True:
             point = np_random.uniform(-1, +1, 2)
             if condition(point):
                 break
         return point
 
     # Check if point is outside of triangular obstacle regions
-    def _outside_triangle(self, point, paths):
-        return not any(path.contains_point(point) for path in paths)
-
+    def _outside_triangle(self, point, paths, epsilon):
+        enlarged_paths = []
+        for path in paths:
+            centroid = np.mean(path.vertices, axis=0)
+            enlarged_vertices = centroid + (1 + epsilon) * (path.vertices - centroid)
+            enlarged_paths.append(mpath.Path(enlarged_vertices))
+        return not any(path.contains_points(point[None, :]) for path in enlarged_paths)
+    
     # Check if point is outside of circular obstacle regions
-    def _outside_circles(self, point, centers_radii):
-        return not any(np.linalg.norm(point - center) <= radius for center, radius in centers_radii)
+    def _outside_circles(self, point, centers_radii, epsilon):
+        return not any(np.linalg.norm(point - center) <= radius + epsilon for center, radius in centers_radii)
     
     # Check if point is outside of rectangular obstacle regions
-    def _outside_rectangle(self, point, x_constraints, y_constraints):
+    def _outside_rectangle(self, point, x_constraints, y_constraints, epsilon):
         within_constraints = any(
-            (low_x <= point[0] <= high_x) and (low_y <= point[1] <= high_y)
+            (low_x - epsilon <= point[0] <= high_x + epsilon) and (low_y - epsilon <= point[1] <= high_y + epsilon)
             for (low_x, high_x), (low_y, high_y) in zip(x_constraints, y_constraints)
         )
         return not within_constraints
 
     # Reset agents and goals to their initial positions
-    def _reset_agents_and_goals(self, world, np_random, paths):        
+    def _reset_agents_and_goals(self, world, np_random, paths):
+        epsilon = world.agents[0].radius
+        
         if world.problem_instance not in ['einstein_tile', 'corners', 'right_arrows', 'circle', 'solar_system']:
             # Used for problem instances composed of rectangles
             x_constraints = [constr[0] for constr in world.instance_constr]
             y_constraints = [constr[1] for constr in world.instance_constr]
 
         for i, agent in enumerate(world.agents):
             agent.goal = world.goals[i]
@@ -113,25 +120,28 @@
             agent.state.p_vel = np.zeros(world.dim_p)
             agent.goal.state.p_vel = np.zeros(world.dim_p)
 
             if world.problem_instance in ['einstein_tile', 'corners', 'right_arrows']:
                 condition = partial(
                     self._outside_triangle, 
                     paths=paths, 
+                    epsilon=epsilon
                     )
             elif world.problem_instance in ['circle', 'solar_system']:
                 condition = partial(
                     self._outside_circles,
                     centers_radii=world.instance_constr,
+                    epsilon=epsilon,
                     )
             else:
                 condition = partial(
                     self._outside_rectangle, 
                     x_constraints=x_constraints, 
                     y_constraints=y_constraints,
+                    epsilon=epsilon, 
                     )
 
             agent.state.p_pos = self._generate_position(np_random, condition)
             agent.goal.state.p_pos = self._generate_position(np_random, condition)
     
     # Reset all large obstacles to a position that does not intersect with the agents and is within its shape
     def _reset_large_obstacles(self, world, np_random, paths):
@@ -153,78 +163,73 @@
                 
                 if shape_idx not in occupied:
                     large_obstacle.state.p_pos = pos
                     occupied.add(shape_idx)
                     break
     
     def _reset_small_obstacles(self, world, np_random, paths):
-        epsilon = world.small_obstacles[0].size + world.large_obstacles[0].size
+        epsilon = world.small_obstacles[0].radius
 
         agent_positions = [agent.state.p_pos for agent in world.agents]
         goal_positions = [goal.state.p_pos for goal in world.goals]
         large_obstacle_positions = [obstacle.state.p_pos for obstacle in world.large_obstacles]
 
         def safe_position(point):
-            outside_entitiy_positions = not any(np.linalg.norm(point - pos) <= epsilon for pos in agent_positions + goal_positions + large_obstacle_positions)
+            outside_entity_positions = not any(np.linalg.norm(point - pos) <= epsilon for pos in agent_positions + goal_positions + large_obstacle_positions)
 
             if world.problem_instance in ['einstein_tile', 'corners', 'right_arrows']:
-                outside_obstacle_constraints = self._outside_triangle(point, paths)
+                outside_obstacle_constraints = self._outside_triangle(point, paths, epsilon)
             elif world.problem_instance in ['circle', 'solar_system']:
-                outside_obstacle_constraints = self._outside_circles(point, world.instance_constr)
+                outside_obstacle_constraints = self._outside_circles(point, world.instance_constr, epsilon) 
             else:
                 x_constraints = [constr[0] for constr in world.instance_constr]
                 y_constraints = [constr[1] for constr in world.instance_constr]
-                outside_obstacle_constraints = self._outside_rectangle(point, x_constraints, y_constraints)
+                outside_obstacle_constraints = self._outside_rectangle(point, x_constraints, y_constraints, epsilon)
 
-            return outside_entitiy_positions and outside_obstacle_constraints
+            return outside_entity_positions and outside_obstacle_constraints
 
         for small_obstacle in world.small_obstacles:
             small_obstacle.state.p_vel = np.zeros(world.dim_p)
             small_obstacle.state.p_pos = self._generate_position(np_random, safe_position)
 
     def reset_world(self, world, np_random, problem_instance):
-        def make_triangle_points(triangle, epsilon):
-            centroid = np.mean(triangle, axis=0)
-            enlarged_vertices = []
-            for vertex in triangle:
-                direction = np.array(vertex) - centroid
-                direction /= np.linalg.norm(direction)
-                new_vertex = np.array(vertex) + epsilon * direction
-                enlarged_vertices.append(tuple(new_vertex))
-            return enlarged_vertices
+        def make_triangle_points(vertices, epsilon):
+            centroid = np.mean(vertices, axis=0)
+            shrunk_vertices = vertices + epsilon * (centroid - vertices)
+            return shrunk_vertices
         
         def make_circle_points(center, radius_and_epsilon, num_points=100):
             t = np.linspace(0, 2*np.pi, num_points)
             x = center[0] + radius_and_epsilon * np.cos(t)
             y = center[1] + radius_and_epsilon * np.sin(t)
             points = np.column_stack([x, y])
             return points
         
         def make_rectangle_points(bounds, epsilon):
             min_x, max_x = bounds[0]
             min_y, max_y = bounds[1]
             return [
-                (min_x - epsilon, min_y - epsilon),
-                (max_x + epsilon, min_y - epsilon),
-                (max_x + epsilon, max_y + epsilon),
-                (min_x - epsilon, max_y + epsilon),
+                (min_x + epsilon, min_y + epsilon),
+                (max_x - epsilon, min_y + epsilon),
+                (max_x - epsilon, max_y - epsilon),
+                (min_x + epsilon, max_y - epsilon),
             ]
 
-        epsilon = world.buffer_dist
+        epsilon = world.large_obstacles[0].radius
         self._set_problem_instance(world, problem_instance)
         
         if world.problem_instance in ['einstein_tile', 'corners', 'right_arrows']:
-            paths = [mpath.Path(make_triangle_points(triangle, epsilon)) for triangle in world.instance_constr]
+            paths = [mpath.Path(make_triangle_points(vertices, epsilon)) for vertices in world.instance_constr]
         elif world.problem_instance in ['circle', 'solar_system']:
-            paths = [mpath.Path(make_circle_points(center, radius + epsilon)) for center, radius in world.instance_constr]
+            paths = [mpath.Path(make_circle_points(center, radius - epsilon)) for center, radius in world.instance_constr]
         else:
             paths = [mpath.Path(make_rectangle_points(bounds, epsilon)) for bounds in world.instance_constr]
 
-        self._reset_agents_and_goals(world, np_random, paths)
         self._reset_large_obstacles(world, np_random, paths)
+        self._reset_agents_and_goals(world, np_random, paths)
         self._reset_small_obstacles(world, np_random, paths)
     
     # Ground agents can only observe the positions of other agents, goals, and small obstacles
     def observation(self, agent, world):
         agent_pos = agent.state.p_pos
         
         num_agents = len(world.agents)
```

### Comparing `Signal8-5.0/Signal8/utils/core.py` & `Signal8-5.0.1/Signal8/utils/core.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 
 
 class Entity:  # properties and state of physical world entity
     def __init__(self):
         # name
         self.name = ""
         # properties:
-        self.size = 0.050
+        self.radius = 0.050
         # entity can move / be pushed
         self.movable = False
         # entity collides with others
         self.collide = True
         # color
         self.color = None
         # state
@@ -38,20 +38,20 @@
 
 class Goal(Entity): # properties of goal entities
     def __init__(self):
         super().__init__()
 
 
 class Obstacle(Entity):  # properties of obstacles entities
-    def __init__(self, size):
+    def __init__(self, radius):
         super().__init__()
         # entity can be moved / pushed
         self.movable = False
-        # entity size
-        self.size = size
+        # entity radius
+        self.radius = radius
         
 
 class Agent(Entity):  # properties of agent entities
     def __init__(self):
         super().__init__()
         # agents are movable by default
         self.movable = True
@@ -143,15 +143,15 @@
             return [None, None]  # not a collider
         if agent_a is agent_b:
             return [None, None]  # don't collide against itself
         # compute actual distance between entities
         delta_pos = agent_a.state.p_pos - agent_b.state.p_pos
         dist = np.sqrt(np.sum(np.square(delta_pos)))
         # minimum allowable distance
-        dist_min = agent_a.size + agent_b.size
+        dist_min = agent_a.radius + agent_b.radius
         # softmax penetration
         k = self.contact_margin
         penetration = np.logaddexp(0, -(dist - dist_min) / k) * k
         force = self.contact_force * delta_pos / dist * penetration
         force_a = +force if agent_a.movable else None
         force_b = -force if agent_b.movable else None
         return [force_a, force_b]
```

### Comparing `Signal8-5.0/Signal8/utils/problems.py` & `Signal8-5.0.1/Signal8/utils/problems.py`

 * *Files 5% similar despite different names*

```diff
@@ -3,18 +3,18 @@
     'bisect': [
         ((-1, -0), (-1, 1))
         ],
     'circle':  [
         ((0, 0), (0.5)),
         ],
     'corners': [
-        ((1, 1), (1, 0.75), (0.75, 1)),
-        ((1, -1), (1, -0.75), (0.75, -1)),
-        ((-1, -1), (-1, -0.75), (-0.75, -1)),
-        ((-1, 1), (-1, 0.75), (-0.75, 1)),
+        ((1, 1), (1, 0.65), (0.65, 1)),
+        ((1, -1), (1, -0.65), (0.65, -1)),
+        ((-1, -1), (-1, -0.65), (-0.65, -1)),
+        ((-1, 1), (-1, 0.65), (-0.65, 1)),
         ],
     'cross': [
         ((-0.1875, 0.1875), (0, 0.7)),
         ((-0.1875, 0.1875), (-0.7, 0)),
         ((-0.7, 0), (-0.1875, 0.1875)),
         ((0, 0.7), (-0.1875, 0.1875)),
         ],
```

### Comparing `Signal8-5.0/Signal8/utils/simple_env.py` & `Signal8-5.0.1/Signal8/utils/simple_env.py`

 * *Files 3% similar despite different names*

```diff
@@ -193,17 +193,17 @@
             agent.action *= sensitivity
             action = action[1:]
         # make sure we used all elements of action
         assert len(action) == 0
     
     # Check if episode is terminated or truncated
     def _episode_status(self):    
-        goal_dist_threshold = self.world.agents[0].size + self.world.agents[0].goal.size
-        small_obs_threshold = self.world.agents[0].size + self.world.small_obstacles[0].size
-        large_obs_threshold = self.world.agents[0].size + self.world.large_obstacles[0].size
+        goal_dist_threshold = self.world.agents[0].radius + self.world.agents[0].goal.radius
+        small_obs_threshold = self.world.agents[0].radius + self.world.small_obstacles[0].radius
+        large_obs_threshold = self.world.agents[0].radius + self.world.large_obstacles[0].radius
         
         small_obstacles = [obs for obs in self.world.small_obstacles]
         large_obstacles = [obs for obs in self.world.large_obstacles]    
 
         goal_dist = [np.linalg.norm(agent.state.p_pos - agent.goal.state.p_pos) for agent in self.world.agents]
         small_obs_dist = [min(np.linalg.norm(agent.state.p_pos - obs.state.p_pos) for obs in small_obstacles)
                           for agent in self.world.agents]
@@ -290,18 +290,18 @@
             x = (
                 (x / cam_range) * self.width // 2 * 0.9
             )  # the .9 is just to keep entities from appearing "too" out-of-bounds
             y = (y / cam_range) * self.height // 2 * 0.9
             x += self.width // 2
             y += self.height // 2
             pygame.draw.circle(
-                self.screen, entity.color * 200, (x, y), entity.size * 350
+                self.screen, entity.color * 200, (x, y), entity.radius * 350
             )  # 350 is an arbitrary scale factor to get pygame to render similar sizes as pyglet
             pygame.draw.circle(
-                self.screen, (0, 0, 0), (x, y), entity.size * 350, 1
+                self.screen, (0, 0, 0), (x, y), entity.radius * 350, 1
             )  # borders
             assert (
                 0 < x < self.width and 0 < y < self.height
             ), f"Coordinates {(x, y)} are out of bounds."
 
     def close(self):
         if self.renderOn:
```

### Comparing `Signal8-5.0/Signal8/utils/test_dynamic_obs.py` & `Signal8-5.0.1/Signal8/utils/test_dynamic_obs.py`

 * *Files identical despite different names*

### Comparing `Signal8-5.0/Signal8.egg-info/PKG-INFO` & `Signal8-5.0.1/Signal8.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 5.0
+Version: 5.0.1
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
```

### Comparing `Signal8-5.0/setup.py` & `Signal8-5.0.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="Signal8",
-    version="5.0",
+    version="5.0.1",
     packages=find_packages(),
     author="Ethan Clark",
     author_email="eclark715@gmail.com.com",
     description="A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.",
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/ethanmclark1/signal8",
```

