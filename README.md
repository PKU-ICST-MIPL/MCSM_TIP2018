### Introduction

This is the source code of our TIP 2018 paper "Modality-specific Cross-modal Similarity Measurement with Recurrent Attention Network", Please cite the following paper if you find our code useful.

Yuxin Peng, Jinwei Qi and Yuxin Yuan, “Modality-specific Cross-modal Similarity Measurement with Recurrent Attention Network”, IEEE Transactions on Image Processing (TIP), DOI:10.1109/TIP.2018.2852503, 2018. [pdf](https://arxiv.org/abs/1708.04776)

### Preparation
Our code is based on [torch](http://torch.ch/docs/getting-started.html). You need to first install torch as follows:
```
# in a terminal, run the commands WITHOUT sudo
git clone https://github.com/torch/distro.git ~/torch --recursive
cd ~/torch; bash install-deps;
./install.sh
```
See [here](http://torch.ch/docs/getting-started.html) for more details when you encounter problems during installation.

The code is tested on Ubuntu 14.04.5 LTS, Lua 5.1.

### Usage
Data Preparation: we use wiki dataset as example, and the data should be put in `./i2t_attention/data/` and `./t2i_attention/data/`.
The data files can be download from the [link]() and unzipped to the above path.

run `sh run.sh` to train models and extract features, then run the following commands to calculate mAP:
```
cd ./calMAP
matlab -r "evalMAPMerge"
```

