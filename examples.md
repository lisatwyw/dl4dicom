# Code snippets


## Working with data frames

```
np.where( X.SUBJECT_ID.isin(avail) )[0]
```


## Instantiate generator

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

{'details': ['1.250000 3 055Y 6177_SIVoluZo',
  '1.250000 3 055Y 6177_SIVoluZo',
  '1.250000 3 055Y 6177_SIVoluZo',
  '1.000000 2 071Y 6177_SISens10',
  '1.000000 2 071Y 6177_SISens10',
  '1.000000 2 071Y 6177_SISens10',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.000000 2 056Y 6177_SISens16',
  '1.000000 2 056Y 6177_SISens16',
  '1.000000 2 056Y 6177_SISens16',
  '1.000000 2 059Y 6177_SISens16',
  '1.000000 2 059Y 6177_SISens16',
  '1.000000 2 059Y 6177_SISens16',
  '1.000000 2 067Y 6177_SISens16',
  '1.000000 2 067Y 6177_SISens16',
  '1.000000 2 067Y 6177_SISens16',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 070Y 6177_GELighPl',
  '1.250000 1 070Y 6177_GELighPl',
  '1.250000 1 070Y 6177_GELighPl',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.000000 2 063Y 6177_SISens16',
  '1.000000 2 063Y 6177_SISens16',
  '1.000000 2 063Y 6177_SISens16',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 2 074Y 6177_SIEmot6',
  '1.250000 2 074Y 6177_SIEmot6',
  '1.250000 2 074Y 6177_SIEmot6',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.000000 2 001D 6177_SISens16',
  '1.000000 2 001D 6177_SISens16',
  '1.000000 2 001D 6177_SISens16',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.000000 2 055Y 6177_SISens16',
  '1.000000 2 055Y 6177_SISens16',
  '1.000000 2 055Y 6177_SISens16',
  '1.250000 2 067Y 6177_SIEmot6',
  '1.250000 2 067Y 6177_SIEmot6',
  '1.250000 2 067Y 6177_SIEmot6',
  '1.250000 1 057Y 6177_GELighLi',
  '1.250000 1 057Y 6177_GELighLi',
  '1.250000 1 057Y 6177_GELighLi',
  '1.250000 1 060Y 6177_GELighPl',
  '1.250000 1 060Y 6177_GELighPl',
  '1.250000 1 060Y 6177_GELighPl',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.250000 1 000Y 6177_GELighVC',
  '1.000000 2 073Y 6177_SISens16',
  '1.000000 2 073Y 6177_SISens16',
  '1.000000 2 073Y 6177_SISens16']}
```
