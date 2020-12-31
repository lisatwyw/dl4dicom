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


# How things are computed

```
fov = ds.SliceThickness*len(files)
j = fov//self.slice_sampling_rate                    
j+=self.first_slice_indx; s=0;                    
```


