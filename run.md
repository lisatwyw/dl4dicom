# Installation

```
pip install tensorflow-gpu==2 pydicom  ... 
```
*(list to be continued)*
 
# Configuration

## Parameters of each trial

Example: ```TK:SE3_MD:101_FD:4_IP:1_RS:1_FS:0_SZ:512_IR:20_BS:12_NE:100```

| Code | Brief description of training configuration |
| ------------- |:-------------|
| TK | Prediction task |
| MD | Base model ID |
| FS | Feature set drawn from clinical data |
| FD | # of folds |
| RS | 1: Under-sampling; 2: Over-sampling |
| IP | Imputer ID |

# Specific to ROI extraction
| Code | Brief description of training configuration |
| ------------- |:-------------|
| IZ | Resolution of image pixel (512 or 224; SZ x SZ x 3) |
| IR | Sampling rate |
| IQ | Number of intensity levels; 2**IQ |
| IF | Index of first slice to extract |

## Specific to CNN
| Code | Brief description of training configuration |
| ------------- |:-------------|
| BS | Size of mini batches in training CNN  |
| NE | Maximum number of epochs to train |


# Running

## Command line
```
ipython -i run_dl4dcm.py TK:SE3_MD:101_FD:4_IP:1_RS:1_FS:0_SZ:512_IR:20_IQ:12_IF:5_BS:12_NE:20

```

## IPython
```
In [1]: afile='TK:SE3_MD:101_FD:4_IP:1_RS:1_FS:0_SZ:512_IR:20_BS:12_NE:10'
In [2]: exec( open("parse_args.py", encoding='UTF-8').read() )
In [3]: MODE=1
In [4]: exec( open("run_dl4dcm.py", encoding='UTF-8').read() )
```

## Submission on Graham@ComputeCanada

[See info](https://docs.computecanada.ca/wiki/Graham#GPUs_on_Graham)


### Example
```
#!/bin/bash
#SBATCH --account=def-your_username
#SBATCH --gres=gpu:v100:1
#SBATCH --cpus-per-task=1
#SBATCH --mem=12G
#SBATCH --time=0-10:00

source $HOME/tf-gpu/bin/activate # virtual environment with tf2.0 installation
cd $HOME/mycode # where code is saved
ipython run_dl4dcm.py TK:SE3_MD:102_FD:6_IP:1_RS:1_FS:0_SZ:512_IR:20_BS:12_NE:100
```


