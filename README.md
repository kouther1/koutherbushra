# Pytorch code for "A Spatially Separable Attention Mechanism For Massive MIMO CSI Feedback"
(c) kouther bushra, email: koutherbushra2022@gmail.com
## Introduction
This repository holds the pytorch implementaion of the original models described in the paper

Sharan Mourya, Sai Dhiraj Amuru, "A Spatially Separable Attention Mechanism For Massive MIMO CSI Feedback"

## Requirements
- Python >= 3.9
- [PyTorch >= 1.2](https://pytorch.org/get-started/locally/)
- [Scipy >= 1.8.0](https://scipy.org/install/)


## Steps to follow

#### 1) Download Dataset

For simulation purposes, channel matrices generated  from [COST2100](https://ieeexplore.ieee.org/document/6393523) model.

#### 2) Organize Dataset
Once dataset is downloaded, recommended to organize the folders as follows
```
├── STNet  # The cloned pytorchSTNet repository
│   ├── pytorchstnet.py
├── data  # The data folder
│   ├── DATA_Htestin.mat
│   ├── ...
```
#### 3) Training STNet
Firstly, choose the compression ratio 1/4, 1/8, 1/16, 1/32 or 1/64 by populating the variable **encoded_dim** with 512, 256, 128, 64 or 32 respectively.

Secondly, choose a scenario "indoor" or "outdoor" by assiging the variable **envir** the same.

Finally run the file **pytorchSTNet.py** to begin training...

## Results
Normalized Mean Square Error (NMSE) and  Floating-Point Operations per second (FLOPS) achieved by STNet for different compression ratios under different scenarios are tabulated below. 

S.No | Compression Ratio | indoor | outdoor | Flops
:--: | :--: | :--: | :--: | :--: 
1 | 1/4 | -30.67 | -12.91 | 6.16M
2 | 1/8 | -21.28 | -8.53 | 5.33M
3 | 1/16 | -15.28 | -5.64 | 4.91M
4 | 1/32 | -9.42 | -3.51 | 4.70M
5 | 1/64 | -7.81 | -2.46 | 4.59M

