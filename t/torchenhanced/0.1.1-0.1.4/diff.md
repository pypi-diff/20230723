# Comparing `tmp/torchenhanced-0.1.1.tar.gz` & `tmp/torchenhanced-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "torchenhanced-0.1.1.tar", last modified: Wed Jul  5 16:58:03 2023, max compression
+gzip compressed data, was "torchenhanced-0.1.4.tar", last modified: Sun Jul 23 16:16:22 2023, max compression
```

## Comparing `torchenhanced-0.1.1.tar` & `torchenhanced-0.1.4.tar`

### file list

```diff
@@ -1,25 +1,26 @@
-drwxrwxrwx   0        0        0        0 2023-07-05 16:58:03.583223 torchenhanced-0.1.1/
--rw-rw-rw-   0        0        0       62 2023-06-14 09:27:16.000000 torchenhanced-0.1.1/.gitignore
--rw-rw-rw-   0        0        0      665 2023-07-05 16:58:03.583223 torchenhanced-0.1.1/PKG-INFO
--rw-rw-rw-   0        0        0       65 2023-06-14 09:27:16.000000 torchenhanced-0.1.1/README.md
--rw-rw-rw-   0        0        0      852 2023-07-05 16:20:11.000000 torchenhanced-0.1.1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-05 16:58:03.583223 torchenhanced-0.1.1/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-05 16:58:03.540331 torchenhanced-0.1.1/src/
-drwxrwxrwx   0        0        0        0 2023-07-05 16:58:03.549349 torchenhanced-0.1.1/src/torchenhanced/
--rw-rw-rw-   0        0        0     3716 2023-06-14 09:28:57.000000 torchenhanced-0.1.1/src/torchenhanced/CosineWarmup.py
--rw-rw-rw-   0        0        0       84 2023-06-14 09:40:55.000000 torchenhanced-0.1.1/src/torchenhanced/__init__.py
--rw-rw-rw-   0        0        0    16985 2023-07-05 14:37:35.000000 torchenhanced-0.1.1/src/torchenhanced/mlearning.py
-drwxrwxrwx   0        0        0        0 2023-07-05 16:58:03.567596 torchenhanced-0.1.1/src/torchenhanced/util/
--rw-rw-rw-   0        0        0      103 2023-06-14 09:27:16.000000 torchenhanced-0.1.1/src/torchenhanced/util/__init__.py
--rw-rw-rw-   0        0        0     2334 2023-06-14 09:27:16.000000 torchenhanced-0.1.1/src/torchenhanced/util/color_compression.py
--rw-rw-rw-   0        0        0      735 2023-06-14 09:27:16.000000 torchenhanced-0.1.1/src/torchenhanced/util/files.py
--rw-rw-rw-   0        0        0     1335 2023-06-14 09:27:16.000000 torchenhanced-0.1.1/src/torchenhanced/util/misc.py
--rw-rw-rw-   0        0        0     2618 2023-06-14 09:27:16.000000 torchenhanced-0.1.1/src/torchenhanced/util/visualize.py
-drwxrwxrwx   0        0        0        0 2023-07-05 16:58:03.567596 torchenhanced-0.1.1/src/torchenhanced.egg-info/
--rw-rw-rw-   0        0        0      665 2023-07-05 16:58:03.000000 torchenhanced-0.1.1/src/torchenhanced.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      531 2023-07-05 16:58:03.000000 torchenhanced-0.1.1/src/torchenhanced.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-05 16:58:03.000000 torchenhanced-0.1.1/src/torchenhanced.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       34 2023-07-05 16:58:03.000000 torchenhanced-0.1.1/src/torchenhanced.egg-info/requires.txt
--rw-rw-rw-   0        0        0       14 2023-07-05 16:58:03.000000 torchenhanced-0.1.1/src/torchenhanced.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-07-05 16:58:03.567596 torchenhanced-0.1.1/tests/
--rw-rw-rw-   0        0        0     2188 2023-06-14 09:27:16.000000 torchenhanced-0.1.1/tests/test_util.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:16:22.538648 torchenhanced-0.1.4/
+-rw-rw-rw-   0        0        0       87 2023-07-23 00:32:41.000000 torchenhanced-0.1.4/.gitignore
+-rw-rw-rw-   0        0        0      665 2023-07-23 16:16:22.537647 torchenhanced-0.1.4/PKG-INFO
+-rw-rw-rw-   0        0        0       65 2023-05-29 21:44:08.000000 torchenhanced-0.1.4/README.md
+-rw-rw-rw-   0        0        0      862 2023-07-23 00:32:41.000000 torchenhanced-0.1.4/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 16:16:22.538648 torchenhanced-0.1.4/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 16:16:22.504647 torchenhanced-0.1.4/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:16:22.515647 torchenhanced-0.1.4/src/torchenhanced/
+-rw-rw-rw-   0        0        0     3716 2023-06-20 22:11:53.000000 torchenhanced-0.1.4/src/torchenhanced/CosineWarmup.py
+-rw-rw-rw-   0        0        0       84 2023-06-20 22:11:53.000000 torchenhanced-0.1.4/src/torchenhanced/__init__.py
+-rw-rw-rw-   0        0        0    20042 2023-07-23 16:14:24.000000 torchenhanced-0.1.4/src/torchenhanced/mlearning.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:16:22.535647 torchenhanced-0.1.4/src/torchenhanced/util/
+-rw-rw-rw-   0        0        0      103 2023-06-20 22:11:53.000000 torchenhanced-0.1.4/src/torchenhanced/util/__init__.py
+-rw-rw-rw-   0        0        0     2334 2023-06-20 22:11:53.000000 torchenhanced-0.1.4/src/torchenhanced/util/color_compression.py
+-rw-rw-rw-   0        0        0      721 2023-07-23 00:32:41.000000 torchenhanced-0.1.4/src/torchenhanced/util/files.py
+-rw-rw-rw-   0        0        0     1335 2023-06-20 22:11:53.000000 torchenhanced-0.1.4/src/torchenhanced/util/misc.py
+-rw-rw-rw-   0        0        0     2618 2023-06-20 22:11:53.000000 torchenhanced-0.1.4/src/torchenhanced/util/visualize.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:16:22.532647 torchenhanced-0.1.4/src/torchenhanced.egg-info/
+-rw-rw-rw-   0        0        0      665 2023-07-23 16:16:22.000000 torchenhanced-0.1.4/src/torchenhanced.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      553 2023-07-23 16:16:22.000000 torchenhanced-0.1.4/src/torchenhanced.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 16:16:22.000000 torchenhanced-0.1.4/src/torchenhanced.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       40 2023-07-23 16:16:22.000000 torchenhanced-0.1.4/src/torchenhanced.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-07-23 16:16:22.000000 torchenhanced-0.1.4/src/torchenhanced.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:16:22.536647 torchenhanced-0.1.4/tests/
+-rw-rw-rw-   0        0        0     2445 2023-07-23 16:06:40.000000 torchenhanced-0.1.4/tests/test_Trainer.py
+-rw-rw-rw-   0        0        0     2217 2023-07-23 00:32:41.000000 torchenhanced-0.1.4/tests/test_util.py
```

### Comparing `torchenhanced-0.1.1/PKG-INFO` & `torchenhanced-0.1.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torchenhanced
-Version: 0.1.1
+Version: 0.1.4
 Summary: Wrappers for pytorch stuff I use on the daily
 Author-email: Vassilis Papadopoulos <frotaur@hotmail.co.uk>
 License: MIT License
 Project-URL: Homepage, https://github.com/frotaur/torchenhanced
 Project-URL: Bug Tracker, https://github.com/frotaur/torchenhanced/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `torchenhanced-0.1.1/pyproject.toml` & `torchenhanced-0.1.4/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
     'Development Status :: 3 - Alpha'
 ]
 dynamic = ["version"]
-dependencies = ["torch","torchvision","matplotlib","tqdm"]
+dependencies = ["torch","torchvision","matplotlib","tqdm", "wandb",]
 
 
 [project.urls]
 "Homepage" = "https://github.com/frotaur/torchenhanced"
 "Bug Tracker" = "https://github.com/frotaur/torchenhanced/issues"
 
 [tool.setuptools_scm]
```

### Comparing `torchenhanced-0.1.1/src/torchenhanced/CosineWarmup.py` & `torchenhanced-0.1.4/src/torchenhanced/CosineWarmup.py`

 * *Files identical despite different names*

### Comparing `torchenhanced-0.1.1/src/torchenhanced/mlearning.py` & `torchenhanced-0.1.4/src/torchenhanced/mlearning.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,98 +1,160 @@
 import torch.nn as nn
-import torch
-import os
-from torch.utils.tensorboard import SummaryWriter
+import torch, wandb, os
 import torch.optim.lr_scheduler as lrsched
 from torch.optim import Optimizer
 from datetime import datetime
-from pathlib import Path
 from tqdm import tqdm
 
 
 class DevModule(nn.Module):
     """
         Extremely small wrapper for nn.Module.
         Simply adds a method device() that returns
         the current device the module is on. Changes if
         self.to(...) is called.
+
+        args :
+        config : Dictionary that contains the key:value pairs needed to 
+        instantiate the model (essentially the arguments of the __init__ method).
     """
     def __init__(self):
         super().__init__()
 
         self.register_buffer('_devtens',torch.empty(0))
-    
+
     @property
     def device(self):
         return self._devtens.device
 
+    @property
+    def paranum(self):
+        return sum(p.numel() for p in self.parameters())
+    
+    @property
+    def config(self):
+        """
+            Returns a json-serializable dict containing the config of the model.
+            Essentially a key-value dictionary of the init arguments of the model.
+            Should be redefined in sub-classes.
+        """
+        return self._config
+
+
+class ConfigModule(DevModule):
+    """
+        Same as DevModule, but with a config property that
+        stores the necessary data to reconstruct the model.
+        Use preferably over DevModule, especially with use with Trainer.
+
+        args :
+        config : Dictionary that contains the key:value pairs needed to 
+        instantiate the model (i.e. the argument values of the __init__ method)
+    """
+    def __init__(self, config:dict):
+        super().__init__()
+
+        self._config = config
+        self._config['name'] = self.__class__.__name__
+
+    @property
+    def config(self):
+        """
+            Returns a json-serializable dict containing the config of the model.
+            Essentially a key-value dictionary of the init arguments of the model.
+            Should be redefined in sub-classes.
+        """
+        return self._config
+
 
 class Trainer(DevModule):
     """
         Mother class used to train models, exposing a host of useful functions.
+        Should be subclassed to be used, and the following methods should be redefined :
+            - process_batch, mandatory
+            - get_loaders, mandatory
+            - epoch_log, optional
+            - valid_log, optional
+            - process_batch_valid, mandatory if validation is used (i.e. get_loaders returns 2 loaders)
+        For logging, use wandb.log, which is already initialized. One should be logged in into the wandb
+        account to make the logging work. See wandb documentation for info on logging.
+            
 
         Parameters :
         model : Model to be trained
         optim : Optimizer to be used. ! Must be initialized
         with the model parameters ! Default : AdamW with 1e-3 lr.
         scheduler : Scheduler to be used. Can be provided only if using
         non-default optimizer. Must be initialized with aforementioned 
         optimizer. Default : warmup for 4 epochs from 1e-6.
         model_save_loc : str or None(default), folder in which to save the raw model weights
         state_save_loc : str or None(default), folder in which to save the training state, 
         used to resume training.
         device : torch.device, device on which to train the model
-        run_name : str, for tensorboard and saves, name of the training session
+        run_name : str, for wandb and saves, name of the training session
+        project_name : str, name of the project in which the run belongs
     """
 
     def __init__(self, model : nn.Module, optim :Optimizer =None, scheduler : lrsched._LRScheduler =None, 
-                 model_save_loc=None,state_save_loc=None,device='cpu', run_name = None):
+                 model_save_loc=None,state_save_loc=None,device:str ='cpu', run_name :str = None, 
+                 project_name :str = None):
         super().__init__()
         
         self.to(device)
-
         self.model = model.to(device)
 
-
         if(model_save_loc is None) :
             self.model_save_loc = os.path.join('.',f"{self.model.__class__.__name__}_weights")
         else :
-            self.model_save_loc = model_save_loc
+            self.model_save_loc = os.path.join(model_save_loc,f"{self.model.__class__.__name__}_weights")
         
         if(state_save_loc is None) :
             self.state_save_loc = os.path.join('.',f"{self.model.__class__.__name__}_state")
         else :
-            self.state_save_loc = state_save_loc
+            self.state_save_loc = os.path.join(state_save_loc,f"{self.model.__class__.__name__}_state")
         
         if(optim is None):
             self.optim = torch.optim.AdamW(self.model.parameters(),lr=1e-3)
         else :
             self.optim = optim
 
         if(scheduler is None):
             self.scheduler = lrsched.LinearLR(self.optim,start_factor=0.05,total_iters=4)
         else :
             self.scheduler = scheduler
-
-        for direc in [self.model_save_loc,self.state_save_loc]:
-            os.makedirs(direc,exist_ok=True)
         
 
         # Session hash, the date to not overwrite sessions
         self.session_hash = datetime.now().strftime('%H-%M_%d_%m')
         if(run_name is None):
             self.run_name = self.session_hash
             run_name= os.path.join('.','runs',self.session_hash)
         else :
             self.run_name=run_name
             run_name = os.path.join('.','runs',run_name)
         
-        self.writer = SummaryWriter(run_name)
+        # Basic config, when sub-classing can add dataset and such
+        # Maybe useless
+        self.run_config = dict(model=self.model.__class__.__name__,
+                               lr_init=self.optim.param_groups[0]['lr'],
+                               scheduler = self.scheduler.__class__.__name__)
+        
+        self.run_id = wandb.util.generate_id() # For restoring the run
+        self.project_name = project_name
         
 
+    def change_lr(self, new_lr):
+        """
+            Changes the learning rate of the optimizer.
+            Might clash with scheduler ?
+        """
+
+        for g in self.optim.param_groups:
+            g['lr'] = new_lr
+        
     @staticmethod
     def config_from_state(state_path: str):
         """
             Given the path to a trainer state, returns a tuple (config, weights)
             for the saved model. The model can then be initialized by using config 
             as its __init__ arguments, and load the state_dict from weights.
 
@@ -111,71 +173,78 @@
         state_dict = torch.load(state_path)
         config = state_dict['model_config']
         model_name = state_dict['name']
         weights = state_dict['model']
 
         return model_name,config,weights
 
-    def load_state(self,state_path):
+    def load_state(self,state_path : str):
         """
             Loads trainer minimal trainer state (model,session_hash,optim,scheduler).
-            Can be overwritten in sub-class if there is more to the state of the
-            trainer.
 
             params : 
             state_path : str, location of the sought-out state_dict
 
-            returns : the loaded state_dict with remaining parameters
-
-            <<TODO : maybe the return is pointless>>
         """
         if(not os.path.exists(state_path)):
             raise ValueError(f'Path {state_path} not found, can\'t load state')
         state_dict = torch.load(state_path)
         if(self.model.config != state_dict['model_config']):
             print('WARNING ! Loaded model configuration and state model_config\
                   do not match. This may generate errors.')
+            
         self.model.load_state_dict(state_dict['model'])
-        del state_dict['model']
         self.session_hash = state_dict['session']
-        del state_dict['session']
         self.optim.load_state_dict(state_dict['optim'])
-        del state_dict['optim']
         self.scheduler.load_state_dict(state_dict['scheduler'])
-        del state_dict['scheduler']
+        self.run_id = state_dict['run_id']
+        # Maybe I need to load also the run_name, we'll see
 
-        return state_dict
 
-
-    def save_state(self,state_dict,name=None,unique=False):
+    def save_state(self,unique:bool=False):
         """
             Saves trainer state.
             Params : 
             state_dict : dict, contains at least the following key-values:
                 - 'model' : contains model.state_dict
                 - 'session' : contains self.session_hash
                 - 'optim' :optimizer
                 - 'scheduler : scheduler
                 - 'model_config' : json allowing one to reconstruct the model.
+                - 'run_id' : id of the run, for wandb
             Additionally, can contain logging info like last loss, epoch number, and others.
             If you want a more complicated state, training_epoch should be overriden.
             name : str, name of the save file, overrides automatic one
             unique : bool, if to generate unique savename (with date)
         """
         os.makedirs(self.state_save_loc,exist_ok=True)
 
-        if (name is None):
-            name=f"{self.model.__class__.__name__}_state_{self.session_hash}.pt"
+        # Create the state
+        try :
+            model_config = self.model.config
+        except AttributeError as e:
+            print(f'''Error while fetching model config ! 
+                    Make sure model.config is defined. (see ConfigModule doc).
+                    Continuing, but might generate errors while loading/save models)''')
+            model_config = None
+
+        state = dict(optim=self.optim.state_dict(),scheduler=self.scheduler.state_dict()
+            ,model=self.model.state_dict(),session=self.session_hash,model_config=model_config,
+            name=self.model.__class__.__name__, run_id=self.run_id)
+
+        name = self.run_name
         if (unique):
             name=name+'_'+datetime.now().strftime('%H-%M_%d_%m')
+
         saveloc = os.path.join(self.state_save_loc,name)
-        torch.save(state_dict,saveloc)
+        torch.save(state,saveloc)
 
         print('Saved training state')
 
+
     def save_model(self, name:str=None):
         """
             Saves model weights onto trainer model_save_loc. Not necessarily useful since all the info
             is contained in the saved state, but is sometimes practical.
         """
         if (name is None):
             name=f"{self.model.__class__.__name__}_{datetime.now().strftime('%H-%M_%d_%m')}.pt"
@@ -199,40 +268,41 @@
             the data_dict (potentially updated). Can do logging and other things 
             optionally. Loss is automatically logged, so no need to worry about it. 
 
             params:
             batch_data : whatever is returned by the dataloader
             data_dict : Dictionary containing necessary data, mainly
             for logging. Always contains the following key-values :
-                - time : float variable giving a value to the progression of the batches
+                - stepnum : total number of steps (minibatches) so far
                 - batchnum : current batch number
                 - batch_log : batch interval in which we should log
                 - totbatch : total number of batches.
             data_dict can be modified to store running values, or any other value that might
             be important later. If data_dict is updated, this will persist through the next iteration
             and call of process_batch.
 
             Returns : 2-uple, (loss, data_dict)
         """
         raise NotImplementedError('process_batch should be implemented in Trainer sub-class')
 
     def process_batch_valid(self,batch_data, data_dict : dict, **kwargs):
         """
             Redefine this in sub-classes. Should return the loss, as well as 
-            the data_dict (potentially updated). Can do logging and other things 
-            optionally. Loss is automatically logged, so no need to worry about it. 
+            the data_dict (potentially updated). Can do validation minibatch-level
+            logging, although it is discouraged. Proper use should be to collect the data
+            to be logged in data_dict, and then log it in valid_log (to log once per epoch)
+            Loss is automatically logged, so no need to worry about it. 
 
             params:
             batch_data : whatever is returned by the dataloader
             data_dict : Dictionary containing necessary data, mainly
             for logging. Always contains the following key-values :
-                - time : float variable giving a value to the progression of the batches
-                - batchnum : current batch number
-                - batch_log : batch interval in which we should log
-                - totbatch : total number of batches.
+                - batchnum : current validation mini-batch number
+                - batch_log : batch interval in which we should log (used for training batch-level logging)
+                - totbatch : total number of validation minibatches.
                 - epoch : current epoch
             data_dict can be modified to store running values, or any other value that might
             be important later. If data_dict is updated, this will persist through the next iteration
             and call of process_batch.
 
             Returns : 2-uple, (loss, data_dict)
         """
@@ -252,60 +322,64 @@
         """
         raise NotImplementedError('get_loaders should be redefined in Trainer sub-class')
 
     def epoch_log(self,data_dict):
         """
             To be (optionally) implemented in sub-class. Does the logging 
             at the epoch level, is called every epoch. Data_dict has (at least) key-values :
-                - time : float variable giving a value to the progression of the batches
+                - stepnum : total number of steps (minibatches) so far
                 - batchnum : current batch number
                 - batch_log : batch interval in which we should log
                 - totbatch : total number of batches.
                 - epoch : current epoch
             And any number of additional values, depending on what process_batch does.
         """
         pass
 
     def valid_log(self,data_dict):
         """
             To be (optionally) implemented in sub-class. Does the logging 
             at the epoch level, is called every epoch. Data_dict has (at least) key-values :
-                - time : float variable giving a value to the progression of the batches
+                - stepnum : total number of steps (minibatches) so far
                 - batchnum : current batch number
                 - batch_log : batch interval in which we should log
                 - totbatch : total number of batches.
                 - epoch : current epoch
             And any number of additional values, depending on what process_batch does.
         """
         pass
 
-    def train_epochs(self,epochs : int,*,save_every:int=50,batch_log:int=None,
-                     batch_size:int=32,aggregate:int=1,load_from:str=None,
-                     unique:bool=False,**kwargs):
+    def train_epochs(self,epochs : int,*,batch_sched:bool=False,save_every:int=50,
+                     batch_log:int=None,batch_size:int=32,aggregate:int=1,
+                     load_from:str=None,unique:bool=False,**kwargs):
         """
             Trains for specified epoch number. This method trains the model in a basic way,
             and does very basic logging. At the minimum, it requires process_batch and 
             process_batch_valid to be overriden, and other logging methods are optionals.
 
             data_dict can be used to carry info from one batch to another inside the same epoch,
             and can be used by process_batch* functions for logging of advanced quantities.
             Params :
             epochs : number of epochs to train for
+            batch_sched : if True, scheduler steps (by a lower amount) between each batch.
+            Not that this use is deprecated, so it is recommended to keep False. For now, 
+            necessary for some Pytorch schedulers (cosine annealing).
             save_every : saves trainer state every 'save_every' epochs
             batch_log : If not none, will also log every batch_log batches, in addition to each epoch
-            batch_size : -
+            batch_size : batch size
             aggregate : how many batches to aggregate (effective batch_size is aggreg*batch_size)
             load_from : path to a trainer state_dict. Loads the state
                 of the trainer from file, then continues training the specified
                 number of epochs.
             unique : if True, do not overwrites previous save states.
-
-            <<<PROBLEM : scheduler step only works between epochs. Add an option to 
-            batch_step, with the value of the stepper should be good I think>>>
         """
+        # Initiate logging
+        wandb.init(name=self.run_name,project=self.project_name,config=self.run_config,
+                   id = self.run_id,resume='allow')
+        
         if(os.path.isfile(str(load_from))):
             # Loads the trainer state
             self.load_state(load_from)
         
         train_loader,valid_loader = self.get_loaders(batch_size)
         self.model.train()
         epoch=self.scheduler.last_epoch
@@ -320,77 +394,74 @@
             data_dict=self._reset_data_dict(data_dict)
             data_dict['epoch']=epoch
             data_dict['totbatch']=totbatch
             for batchnum,batch_data in tqdm(enumerate(train_loader),total=totbatch) :
                 n_aggreg+=1
                 # Process the batch according to the model.
                 data_dict['batchnum']=batchnum
-                data_dict['time']=epoch*(totbatch//batch_log)+batchnum//batch_log
+                data_dict['stepnum']=(epoch)*totbatch+batchnum
 
                 loss, data_dict = self.process_batch(batch_data,data_dict)
                 
                 epoch_loss.append(loss.item())
                 batch_log_loss.append(loss.item())
 
                 loss=loss/aggregate # Rescale loss if aggregating.
                 loss.backward()
                 torch.nn.utils.clip_grad_norm_(self.model.parameters(), 1.)
 
                 
                 if(batchnum%batch_log==batch_log-1):
-                    self.writer.add_scalar('loss/train',sum(batch_log_loss)/len(batch_log_loss),data_dict['time'])
+                    wandb.log({'batchloss/train':sum(batch_log_loss)/len(batch_log_loss)})
                     batch_log_loss=[]
 
                 if(n_aggreg%aggregate==aggregate-1):
                     n_aggreg=0
                     self.optim.step()
                     self.optim.zero_grad()
-                
-                self.scheduler.step(epoch+batchnum/totbatch)
+                if(batch_sched):
+                    self.scheduler.step(epoch+batchnum/totbatch)
 
+            if(not batch_sched):
+                self.scheduler.step()
             
             # Log data
-            self.writer.add_scalar('ep-loss/train',sum(epoch_loss)/len(epoch_loss),data_dict['epoch'])
+            wandb.log({'loss/train':sum(epoch_loss)/len(epoch_loss)})
             self.epoch_log(data_dict)
             
             # Reinitalize datadict here.
             data_dict=self._reset_data_dict(data_dict)
 
             if(valid_loader is not None):
                 with torch.no_grad():
                     self.model.eval()
                     val_loss=[]
                     data_dict['totbatch'] = len(valid_loader)
                     for (batchnum,batch_data) in enumerate(valid_loader):
                         data_dict['batchnum']=batchnum
-                        data_dict['time']=(epoch-1)*totbatch//batch_log+batchnum//batch_log
+                        
 
                         loss, data_dict = self.process_batch_valid(batch_data,data_dict)
                         val_loss.append(loss.item())
 
-            # Log validation data
-            self.writer.add_scalar('ep-loss/valid',sum(val_loss)/len(val_loss),data_dict['epoch'])
-            self.valid_log(data_dict)
-
-            self.writer.flush()
+                # Log validation data
+                wandb.log({'loss/valid':sum(val_loss)/len(val_loss)})
+                self.valid_log(data_dict)
 
             self.model.train()
             epoch+=1
 
-            if ep_incr%save_every==0 :
-                state = dict(optim=self.optim.state_dict(),scheduler=self.scheduler.state_dict()
-                     ,model=self.model.state_dict(),session=self.session_hash,model_config=self.model.config,
-                     name=self.model.__class__.__name__)
-                self.save_state(state,name=self.run_name,unique=unique)
+            if ep_incr%save_every==save_every-1 :
+                self.save_state(unique=unique)
+
+        wandb.finish()
 
     def _reset_data_dict(self,data_dict):
         keys = list(data_dict.keys())
         for k in keys:
             if k not in ['epoch','batch_log'] :
                 del data_dict[k]
-        
         # Probably useless to return
         return data_dict
     
-    def __del__(self):
-        self.writer.close()
-
+    # def __del__(self):
+    #     wandb.finish()
```

### Comparing `torchenhanced-0.1.1/src/torchenhanced/util/color_compression.py` & `torchenhanced-0.1.4/src/torchenhanced/util/color_compression.py`

 * *Files identical despite different names*

### Comparing `torchenhanced-0.1.1/src/torchenhanced/util/files.py` & `torchenhanced-0.1.4/src/torchenhanced/util/files.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,9 @@
 from pathlib import Path
-import json
-import os
-import torch
+import json, os, torch
 
 
 def load_string(file_name):
     try: return Path(file_name).read_text()
     except: return ''
 
 def save_string(string, file_name):
```

### Comparing `torchenhanced-0.1.1/src/torchenhanced/util/misc.py` & `torchenhanced-0.1.4/src/torchenhanced/util/misc.py`

 * *Files identical despite different names*

### Comparing `torchenhanced-0.1.1/src/torchenhanced/util/visualize.py` & `torchenhanced-0.1.4/src/torchenhanced/util/visualize.py`

 * *Files identical despite different names*

### Comparing `torchenhanced-0.1.1/src/torchenhanced.egg-info/PKG-INFO` & `torchenhanced-0.1.4/src/torchenhanced.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torchenhanced
-Version: 0.1.1
+Version: 0.1.4
 Summary: Wrappers for pytorch stuff I use on the daily
 Author-email: Vassilis Papadopoulos <frotaur@hotmail.co.uk>
 License: MIT License
 Project-URL: Homepage, https://github.com/frotaur/torchenhanced
 Project-URL: Bug Tracker, https://github.com/frotaur/torchenhanced/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `torchenhanced-0.1.1/src/torchenhanced.egg-info/SOURCES.txt` & `torchenhanced-0.1.4/src/torchenhanced.egg-info/SOURCES.txt`

 * *Files 14% similar despite different names*

```diff
@@ -10,8 +10,9 @@
 src/torchenhanced.egg-info/requires.txt
 src/torchenhanced.egg-info/top_level.txt
 src/torchenhanced/util/__init__.py
 src/torchenhanced/util/color_compression.py
 src/torchenhanced/util/files.py
 src/torchenhanced/util/misc.py
 src/torchenhanced/util/visualize.py
+tests/test_Trainer.py
 tests/test_util.py
```

### Comparing `torchenhanced-0.1.1/tests/test_util.py` & `torchenhanced-0.1.4/tests/test_util.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import torch,sys,pathlib
 sys.path.append(pathlib.Path(__file__).parent.parent.as_posix())
-print(sys.path)
+
 from src.torchenhanced.util import *
 
 
 def test_coord_to_flat_batch():
     unfolded = torch.randint(0,100,(3,4,5,6)) #4-dim coord tensor
     folded = unfolded.reshape((-1))
 
@@ -30,37 +30,37 @@
     
     assert (res-unfolded[testcoord[0]][testcoord[1]][testcoord[2]][testcoord[3]]).all()==0
 
 def test_color_comp_incomplete():
     from PIL import Image
     from torchvision import transforms as t
 
-    ntar=12
-    imgex=torch.clamp(torch.zeros((1,3,1,1)),0,1)
-    imgex[:,0]=140
-    imgex[:,1]=23
-    imgex[:,2]=23
-    print("==================================================")
-    # print("imgex shape : ",imgex.shape)
-    print("Initial : ",(imgex).squeeze())
-    imgex=convert_to_nbit(imgex/255.,ntar)
-    print("After : ",imgex.squeeze())
-    imgex=decode_from_nbit(imgex,ntar)
-    print("Decoded again : ",imgex.squeeze())
-
-
-    imgex= Image.open("Riffelsee.jpg")
-    imgex=t.ToTensor()(imgex)[None]
-    showTens(imgex)
-    imgex=rgb_to_yuv(imgex)
+    # ntar=12
+    # imgex=torch.clamp(torch.zeros((1,3,1,1)),0,1)
+    # imgex[:,0]=140
+    # imgex[:,1]=23
+    # imgex[:,2]=23
+    # print("==================================================")
+    # # print("imgex shape : ",imgex.shape)
+    # print("Initial : ",(imgex).squeeze())
+    # imgex=convert_to_nbit(imgex/255.,ntar)
+    # print("After : ",imgex.squeeze())
+    # imgex=decode_from_nbit(imgex,ntar)
+    # print("Decoded again : ",imgex.squeeze())
+
+
+    # imgex= Image.open("Riffelsee.jpg")
+    # imgex=t.ToTensor()(imgex)[None]
+    # showTens(imgex)
+    # imgex=rgb_to_yuv(imgex)
     
     
-    imgn = convert_to_nbit(imgex,ntar)
-    imgn = decode_from_nbit(imgn,ntar)
+    # imgn = convert_to_nbit(imgex,ntar)
+    # imgn = decode_from_nbit(imgn,ntar)
 
 
-    print("shape : ",imgex.shape)
+    # print("shape : ",imgex.shape)
 
-    showTens(yuv_to_rgb(imgn))
+    # showTens(yuv_to_rgb(imgn))
 
-    imgyuv = yuv_to_rgb(rgb_to_yuv(imgex))
-    print(f"BOUNDS : (maxy : {torch.max(imgyuv[:,0])},maxCb= {torch.max(imgyuv[:,1])}, maxCr= {torch.max(imgyuv[:,2])})")
+    # imgyuv = yuv_to_rgb(rgb_to_yuv(imgex))
+    # print(f"BOUNDS : (maxy : {torch.max(imgyuv[:,0])},maxCb= {torch.max(imgyuv[:,1])}, maxCr= {torch.max(imgyuv[:,2])})")
```

