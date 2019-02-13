# PointCleanNet
This is our implementation of PointCleannet, a network removes outliers and reduces noise in unordered point clouds.

The architecture is similar to [PCPNet](http://geometry.cs.ucl.ac.uk/projects/2018/pcpnet/) (with a few smaller modifications),
but features are computed from local patches instead of of the entire point cloud,
which makes estimated local properties more accurate.

This code was written by Marie-Julie Rakotosaona, based on the excellent implementation of PCPNet by [Paul Guerrero](https://paulguerrero.github.io) and [Yanir Kleiman](https://www.cs.tau.ac.il/~yanirk/).

## Prerequisites
* CUDA and CuDNN (changing the code to run on CPU should require few changes)
* Python 2.7
* PyTorch 1.0

## Setup
Install required python packages, if they are not already installed ([tensorboardX](https://github.com/lanpa/tensorboard-pytorch) is only required for training):
``` bash
pip install numpy
pip install scipy
pip install tensorboardX
```
## Citation
If you use our work, please cite our paper.
