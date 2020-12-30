
# Introduction

This repo will provide reproducibile code of an extended work of [Tang et al., Lancet Digital Health 2020](https://www.sciencedirect.com/science/article/pii/S2589750020300649)

# High-level summary

- How? CT data are not processed a priori but read directly from raw Dicom images 
- Inputs: Annotated CT Dicom folders
- Parameters: TK:SE3_MD:101_FD:4_IP:1_RS:1_FS:0_SZ:512_IR:20_BS:12_NE:3

# Research questions

1. Does smoothing kernel of the CT slices matters? (ECLIPSE has BONE and STD)
2. What is the effect of limiting to observing patterns within lung regions only?
3. What is the effect of intensity quantization? (e.g. 256 levels vs 4096 levels)?
