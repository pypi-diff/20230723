# Comparing `tmp/Vpro-0.27.tar.gz` & `tmp/Vpro-0.28.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Vpro-0.27.tar", last modified: Sat Jul 22 10:21:12 2023, max compression
+gzip compressed data, was "Vpro-0.28.tar", last modified: Sun Jul 23 15:48:16 2023, max compression
```

## Comparing `Vpro-0.27.tar` & `Vpro-0.28.tar`

### file list

```diff
@@ -1,12 +1,12 @@
-drwxr-xr-x   0 Agastyaa   (502) staff       (20)        0 2023-07-22 10:21:12.189591 Vpro-0.27/
--rw-r--r--   0 Agastyaa   (502) staff       (20)      404 2023-07-22 10:21:12.189437 Vpro-0.27/PKG-INFO
-drwxr-xr-x   0 Agastyaa   (502) staff       (20)        0 2023-07-22 10:21:12.188115 Vpro-0.27/Vpro/
--rw-r--r--   0 Agastyaa   (502) staff       (20)     7926 2023-07-22 10:19:08.000000 Vpro-0.27/Vpro/__init__.py
-drwxr-xr-x   0 Agastyaa   (502) staff       (20)        0 2023-07-22 10:21:12.189151 Vpro-0.27/Vpro.egg-info/
--rw-r--r--   0 Agastyaa   (502) staff       (20)      404 2023-07-22 10:21:12.000000 Vpro-0.27/Vpro.egg-info/PKG-INFO
--rw-r--r--   0 Agastyaa   (502) staff       (20)      164 2023-07-22 10:21:12.000000 Vpro-0.27/Vpro.egg-info/SOURCES.txt
--rw-r--r--   0 Agastyaa   (502) staff       (20)        1 2023-07-22 10:21:12.000000 Vpro-0.27/Vpro.egg-info/dependency_links.txt
--rw-r--r--   0 Agastyaa   (502) staff       (20)       11 2023-07-22 10:21:12.000000 Vpro-0.27/Vpro.egg-info/requires.txt
--rw-r--r--   0 Agastyaa   (502) staff       (20)        5 2023-07-22 10:21:12.000000 Vpro-0.27/Vpro.egg-info/top_level.txt
--rw-r--r--   0 Agastyaa   (502) staff       (20)       38 2023-07-22 10:21:12.189656 Vpro-0.27/setup.cfg
--rw-r--r--   0 Agastyaa   (502) staff       (20)      547 2023-07-22 10:20:56.000000 Vpro-0.27/setup.py
+drwxr-xr-x   0 Agastyaa   (502) staff       (20)        0 2023-07-23 15:48:16.836190 Vpro-0.28/
+-rw-r--r--   0 Agastyaa   (502) staff       (20)      404 2023-07-23 15:48:16.836050 Vpro-0.28/PKG-INFO
+drwxr-xr-x   0 Agastyaa   (502) staff       (20)        0 2023-07-23 15:48:16.833396 Vpro-0.28/Vpro/
+-rw-r--r--   0 Agastyaa   (502) staff       (20)     7757 2023-07-23 15:47:51.000000 Vpro-0.28/Vpro/__init__.py
+drwxr-xr-x   0 Agastyaa   (502) staff       (20)        0 2023-07-23 15:48:16.835815 Vpro-0.28/Vpro.egg-info/
+-rw-r--r--   0 Agastyaa   (502) staff       (20)      404 2023-07-23 15:48:16.000000 Vpro-0.28/Vpro.egg-info/PKG-INFO
+-rw-r--r--   0 Agastyaa   (502) staff       (20)      164 2023-07-23 15:48:16.000000 Vpro-0.28/Vpro.egg-info/SOURCES.txt
+-rw-r--r--   0 Agastyaa   (502) staff       (20)        1 2023-07-23 15:48:16.000000 Vpro-0.28/Vpro.egg-info/dependency_links.txt
+-rw-r--r--   0 Agastyaa   (502) staff       (20)       11 2023-07-23 15:48:16.000000 Vpro-0.28/Vpro.egg-info/requires.txt
+-rw-r--r--   0 Agastyaa   (502) staff       (20)        5 2023-07-23 15:48:16.000000 Vpro-0.28/Vpro.egg-info/top_level.txt
+-rw-r--r--   0 Agastyaa   (502) staff       (20)       38 2023-07-23 15:48:16.836260 Vpro-0.28/setup.cfg
+-rw-r--r--   0 Agastyaa   (502) staff       (20)      547 2023-07-23 15:48:10.000000 Vpro-0.28/setup.py
```

### Comparing `Vpro-0.27/Vpro/__init__.py` & `Vpro-0.28/Vpro/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,19 +1,11 @@
 import numpy as np
 import random
 from tqdm import tqdm
-from decimal import Decimal 
 
-def d(x):
-    return Decimal(x)
-
-def dl(x):
-    for i in x:
-        i=Decimal(i)
-    return x
 
 
 def sig(x, activ):
     if activ== 'leaky relu':
         i=0
         L=[]
         while i<len(x):
@@ -30,23 +22,23 @@
                 L.append(0.01*x[i])
             else:
                 L.append(0)
     if activ== 'sigmoid':
         i=0
         L=[]
         while i<len(x):
-            L.append(1/(1+(d(np.e**(-x[i])))))
+            L.append(1/(1+(np.e**(-x[i]))))
             i=i+1
     if activ== 'tanh':
         i=0
         L=[]
         while i<len(x):
-            A=d(np.e**(float(x[i])))
-            B=d(np.e**(-float(x[i])))
-            L.append(d((A-B)/(A+B)))
+            A=np.e**(float(x[i]))
+            B=np.e**(-float(x[i]))
+            L.append((A-B)/(A+B))
             i=i+1
     return np.array(L)
 
 def sigp(x, activ):
     if activ== 'leaky relu':
         if x>0:
             X=1
@@ -54,19 +46,19 @@
             X=0.01
     if activ== 'relu':
         if x>0:
             X=1
         else:
             X=0
     if activ=='sigmoid':
-        X= d((np.e**x)/((1+(np.e**(-x)))**2))
+        X= (np.e**x)/((1+(np.e**(-x)))**2)
     if activ== 'tanh':
-        A=d(np.e**x)
-        B=d(np.e**(-x))
-        X= d(1-((A-B)/(A+B))**2)
+        A=np.e**x
+        B=np.e**(-x)
+        X= 1-((A-B)/(A+B))**2
     return X
 
 def im(x):
     i=0
     L=[]
     for i in range(len(x)):
         for j in range(len(x[i])):
@@ -180,18 +172,18 @@
         b.append(np.zeros(D))
     b.append(np.zeros(O))
 
     return [w, b]
 
 
 def cost(I, w, b, A, activ):
-    
+    U=len(w)-1
     L=[]
     for i in range(len(I)):
-        X= neural_network(I[i], w, b, activ)[7]-A[i]
+        X= neural_network(I[i], w, b, activ)[2*U+1]-A[i]
         for j in range(len(A[0])):
             L.append((X[j])**2)
     return (sum(L)/len(I))   
 
 
 def grad(I, w, b, A, activ):
 
@@ -218,33 +210,33 @@
 
     GWF=[]
     for k in range(D):
         GWFB= []
         for j in range(len(A[0])):
             S1=[]
             for i in range(len(I)):
-                S1.append(d(2*L[i][j]*sigp(F[i][2*U][j], activ)*F[i][2*U-1][k]))
+                S1.append(2*L[i][j]*sigp(F[i][2*U][j], activ)*F[i][2*U-1][k])
             GWFB.append(sum(S1)/len(I))
         GWF.append(GWFB)
     GWF= np.array(GWF)
     GBF=[]
     for j in range(O):
         S1=[]
         for i in range(len(I)):
-            S1.append(d(2*L[i][j]*sigp(F[i][2*U][j], activ)))
+            S1.append(2*L[i][j]*sigp(F[i][2*U][j], activ))
         GBF.append(sum(S1)/len(I))
     GBF= np.array(GBF)
     GIF=[]
     AGIF=[]
     for k in range(D):
         S1=[]
         for i in range(len(I)):
             S2=[]
             for j in range(O):
-                S2.append(d(2*L[i][j]*sigp(F[i][2*U][j], activ)*w[U][k][j]))
+                S2.append(2*L[i][j]*sigp(F[i][2*U][j], activ)*w[U][k][j])
             S1.append(sum(S2))
         AGIF.append(S1)
         GIF.append(sum(S1)/len(I))
     GIF= np.array(GIF)
 
     GW.insert(0, GWF)
     GB.insert(0, GBF)
@@ -255,38 +247,38 @@
         GBx=[]
         T1=[]
         for k in range(D):
             S1=[]
             for j in range(D):
                 S2=[]
                 for i in range(len(I)):
-                    S2.append(d(AGI[0][k][i]*sigp(F[i][2*U-2-2*y][k], activ)*F[i][2*U-3-2*y][j]))
+                    S2.append(AGI[0][k][i]*sigp(F[i][2*U-2-2*y][k], activ)*F[i][2*U-3-2*y][j])
                 S1.append(sum(S2)/len(I))
             T1.append(S1)
         
         for k in range (D):
             T2=[]
             for j in range (D):
                 T2.append(T1[j][k])
             GWx.append(T2)
         GWx= np.array(GWx)
         for k in range(D):
             S2=[]
             for i in range(len(I)):
-                S2.append(d(AGI[0][k][i]*sigp(F[i][2*U-2-2*y][k], activ)))
+                S2.append(AGI[0][k][i]*sigp(F[i][2*U-2-2*y][k], activ))
             GBx.append(sum(S2)/len(I))
         GBx= np.array(GBx)
         GIx=[]
         AGIx=[]
         for k in range(D):
             S1=[]
             for i in range(len(I)):
                 S2=[]
                 for j in range(D):
-                    S2.append(d(AGI[0][j][i]*sigp(F[i][2*U-2-2*y][j], activ)*w[U-y-1][k][j]))
+                    S2.append(AGI[0][j][i]*sigp(F[i][2*U-2-2*y][j], activ)*w[U-y-1][k][j])
                 S1.append(sum(S2))
             AGIx.append(S1)
             GIx.append(sum(S1)/len(I))
         GIx= np.array(GIx)
 
         GW.insert(0, GWx)
         GB.insert(0, GBx)
@@ -296,28 +288,28 @@
     GB1=[]
     T1=[]
     for k in range(D):
         S1=[]
         for j in range(len(I[0])):
             S2=[]
             for i in range(len(I)):
-                S2.append(d(AGI[0][k][i]*sigp(F[i][0][k], activ)*I[i][j]))
+                S2.append(AGI[0][k][i]*sigp(F[i][0][k], activ)*I[i][j])
             S1.append(sum(S2)/len(I))
         T1.append(S1)
     
     for k in range (len(I[0])):
         T2=[]
         for j in range (D):
             T2.append(T1[j][k])
         GW1.append(T2)
     GW1= np.array(GW1)
     for k in range(D):
         S2=[]
         for i in range(len(I)):
-            S2.append(d(AGI[0][k][i]*sigp(F[i][0][k], activ)))
+            S2.append(AGI[0][k][i]*sigp(F[i][0][k], activ))
         GB1.append(sum(S2)/len(I))
     GB1= np.array(GB1)
 
     GW.insert(0, GW1)
     GB.insert(0, GB1)
     
     GRAD= [GW, GB]
@@ -348,15 +340,15 @@
         ACs= np.array(ACs)
 
         X=grad(Is, w, b, ACs, activ)
 
         for i3 in range(len(w)):
             for j in range (len(w[i3])):
                 for k in range(len(w[i3][0])):
-                    w[i3][j][k]=d(w[i3][j][k])-h*d(X[0][i3][j][k])
+                    w[i3][j][k]=w[i3][j][k]-h*X[0][i3][j][k]
         
 
         for i4 in range(len(b)):
             for j in range(len(b[i4])):
-                b[i4][j]=d(b[i4][j])-h*d(X[1][i4][j])
+                b[i4][j]=b[i4][j]-h*X[1][i4][j]
 
     return [w, b]
```

### Comparing `Vpro-0.27/setup.py` & `Vpro-0.28/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import setup
 from setuptools import setup
 
 setup(name= "Vpro",
-      version= 0.27,
+      version= 0.28,
       description="This is a Machine Learning Module that grants one access to a Multilayer percepton with an adjustable number of hidden layers and neurons per each layer. It also includes functionality to train the network based on a database, and has adjustable innitialisation types, activation functions, and learning hyperparamters.", 
       author="Agastyaa Vishvanath",
       packages=["Vpro"],
       install_requires= ["numpy", "tqdm"])
```

