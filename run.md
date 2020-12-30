# Command line
```
python run_dl4dicom.py TK:SE3_MD:101_FD:4_IP:1_RS:1_FS:0_SZ:512_IR:20_BS:12_NE:100
```

# IPython
```
In [1]: afile='TK:SE3_MD:101_FD:4_IP:1_RS:1_FS:0_SZ:512_IR:20_BS:12_NE:10'
In [2]: exec( open("parse_args.py", encoding='UTF-8').read() )
In [3]: MODE=1
In [4]: exec( open("run_dl4dicom.py", encoding='UTF-8').read() )
```
