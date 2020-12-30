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


## Observe the scanner variations of each mini batch 

```
val_gen.misc

{'details': ['GEHiSpQX 1.250000 1 4.250000 073Y',
  'GEHiSpQX 1.250000 1 4.250000 073Y',
  'SIEmot6 1.000000 2 -51.500000 049Y',
  'SIEmot6 1.000000 2 -51.500000 049Y',
  'GELighPl 1.250000 1 -45.500000 062Y',
  'GELighPl 1.250000 1 -45.500000 062Y',
  'GELighVC 1.250000 1 56.750000 000Y',
  'GELighVC 1.250000 1 56.750000 000Y',
  'SIEmot6 1.000000 2 -38.500000 058Y',
  'SIEmot6 1.000000 2 -38.500000 058Y',
  'GEHiSpQX 1.250000 1 22.264999 065Y',
  'GEHiSpQX 1.250000 1 22.264999 065Y',
  'SIVoluZo 1.250000 3 -133.000000 055Y',
  'SIVoluZo 1.250000 3 -133.000000 055Y',
  'SIVoluZo 1.250000 2 -122.000000 074Y',
  'SIVoluZo 1.250000 2 -122.000000 074Y',
  'GELighLi 1.250000 1 -3.250000 059Y',
  'GELighLi 1.250000 1 -3.250000 059Y',
  'GEHiSpCT 1.000000 1 -35.400002 060Y',
  'GEHiSpCT 1.000000 1 -35.400002 060Y',
  'SISens64 1.000000 2 19.500000 AgeN/A',
  'SISens64 1.000000 2 19.500000 AgeN/A',
  'GELighVC 1.250000 1 10.750000 000Y',
  'GELighVC 1.250000 1 10.750000 000Y']}

```
