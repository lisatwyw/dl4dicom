# Introduction

This repo will provide reproducibile code of an extended work of [(Tang et al., Lancet Digital Health 2020)](https://www.sciencedirect.com/science/article/pii/S2589750020300649)

## High-level summary

- How? CT data are not processed a priori but read directly from raw Dicom images 
- Inputs: Annotated CT Dicom folders
- Parameters: see below

## Research questions

1. Does smoothing kernel of the CT slices matters? (ECLIPSE has BONE and STD)
2. What is the effect of limiting to observing patterns within lung regions only?
3. What is the effect of intensity quantization? (e.g. 256 levels vs 4096 levels)?
4. Diversity of z-offset? (e.g. IF=?)
5. How many layers to freeze in the base model?



# Getting started

## Installation

```
pip install tensorflow-gpu==2 pydicom  ... 
```
*(list to be continued)*
 
## Configuration

### Parameters of each trial

Example: ```export PARAMS=TK:SE3_MD:101_FD:4_IP:1_RS:1_FS:0_IZ:512_IR:20_IQ:12_IF:2_BS:12_NE:100```

#### Trial setup
| Code | Brief description of training configuration |
| ------------- |:-------------|
| TK | Prediction task: {SE1, SE2, SE3, EX1, EX2, EX3} |
| MD | Base model ID |
| FS | Feature set drawn from clinical data |
| FD | # of folds |
| RS | 1: Under-sampling; 2: Over-sampling |
| IP | Imputer ID |

#### Base model ID
| 101 | VGG16 |
| 102 | VGG19 |
| 111 |  |
| 121 |  |
| 122 |  |
| 131 |  |


#### Specific to ROI extraction
| Code | Brief description of training configuration |
| ------------- |:-------------|
| IZ | Resolution of image pixel (512 or 224; SZ x SZ x 3) |
| IR | Sampling rate |
| IQ | Number of intensity levels; 2**IQ |
| IF | Index of first slice to extract |

#### Specific to CNN
| Code | Brief description of training configuration |
| ------------- |:-------------|
| BS | Size of mini batches in training CNN  |
| NE | Maximum number of epochs to train |


## Running

### Command line

After activating ```tf-gpu``` virtual environment in Unix, issue:
```
(tf-gpu)$ ipython -i run_dl4dcm.py $PARAMS
```

This will run script and stay in interactive mode in IPython after, i.e.:
```
In [1]: # explore the workspace
```

### Submission on Graham@ComputeCanada

[See info](https://docs.computecanada.ca/wiki/Graham#GPUs_on_Graham)


#### Example:
```
#!/bin/bash
#SBATCH --account=def-your_username
#SBATCH --gres=gpu:v100:1
#SBATCH --cpus-per-task=1
#SBATCH --mem=12G
#SBATCH --time=0-10:00

source $HOME/tf-gpu/bin/activate # virtual environment with tf2.0 installation
cd $HOME/mycode # where code is saved
ipython run_dl4dcm.py $PARAMS # change PARAMS to actual list as shown above

```



## Example outputs

## Data generator
```
SID-class, SliceThickness, ..., volume of lung tissues found at each slice

3396-1 1.250000 297.5 slice 20 slice 34.0 v=2661, slice 48.0 v=2661,
5341-0 1.250000 330.0 slice 20 slice 36.0 v=6968, slice 52.0 v=6968,
5450-0 1.000000 366.0 slice 20 slice 38.0 v=2357, slice 56.0 v=2357,
2967-0 1.000000 348.0 slice 20 slice 37.0 v=3838, slice 54.0 v=3838,
3925-0 1.250000 315.0 slice 20 slice 35.0 v=5450, slice 50.0 v=5450,
3622-0 1.250000 432.5 slice 20 slice 41.0 v=1090, slice 62.0 v=1090,
3977-0 1.250000 285.0 slice 20 slice 34.0 v=16521, slice 48.0 v=16521,
3445-0 1.250000 425.0 slice 20 slice 41.0 v=7964, slice 62.0 v=7964,
3647-1 1.250000 436.25 slice 20 slice 41.0 v=2932, slice 62.0 v=2932,
0580-0 1.250000 375.0 slice 20 slice 38.0 v=4511, slice 56.0 v=4511,
6300-0 1.250000 356.25 slice 20 slice 37.0 v=15148, slice 54.0 v=15148,
0022-0 1.250000 335.0 slice 20 slice 36.0 v=5525, slice 52.0 v=5525
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

