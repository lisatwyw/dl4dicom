# Code snippets

## Working with data frames

```
np.where( X.SUBJECT_ID.isin(avail) )[0]
```


## Instantiate data generator

```
xx_val # additional clinical data
yy_val # vector of classes

IMSZ = (224,224,3)
BS=24
params2 = {'dim': IMSZ,
          'batch_size': 24,
          'nclasses': 2,
          'shuffle': True,                     
          }
params2['add_rotation']=params2['add_scaling']=params2['add_flipping']=params2['add_translation']=None    

val_gen=otf_DataGenerator( np.arange(yy_val.shape[0]), clinical_data=xx_val, labels=yy_val, **params2, verbose=2, model=model )     
val_gen.__getitem__(90)

```


# Examine GPU usage


```
watch -n .1 nvidia-smi
```

```
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 450.51.06    Driver Version: 450.51.06    CUDA Version: 11.0     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  Tesla T4            On   | 00000000:87:00.0 Off |                    0 |
| N/A   53C    P0    35W /  70W |  14850MiB / 15109MiB |      4%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A    144224      C   ...isat/tf-gpu/bin/python3.6    14847MiB |
+-----------------------------------------------------------------------------+
```


