# PointCleanNet
This is our implementation of PointCleannet, a network removes outliers and reduces noise in unordered point clouds.


![PointCleanNet cleans point clouds](https://raw.githubusercontent.com/mrakotosaon/pointcleannet/master/images/teaser.png "PointCleanNet")

The architecture is similar to [PCPNet](http://geometry.cs.ucl.ac.uk/projects/2018/pcpnet/) (with a few smaller modifications).

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


Clone this repository:
``` bash
git clone https://github.com/mrakotosaon/pointcleannet.git
cd pointcleannet
```


Download denoising dataset:
``` bash
cd data
python download_data.py --task denoising
```

Download outliers_removal training and test sets:
``` bash
cd data
python download_data.py --task outliers_removal
```


Download denoising pretrained model:
``` bash
cd models
python download_models.py --task denoising
```

Download outliers_removal pretrained model:
``` bash
cd models
python download_models.py --task outliers_removal
```


## Removing outliers
To classify outliers using default settings:
``` bash
python eval_pcpnet.py
```

## Denoising
To denoise point clouds using default settings:
``` bash
./run.sh
```


## Training
To train PCPNet with the default settings:
``` bash
python train_pcpnet.py
```

## Citation
If you use our work, please cite our paper.
```
@article{rakotosaona2019pointcleannet,
  title={POINTCLEANNET: Learning to Denoise and Remove Outliers from Dense Point Clouds},
  author={Rakotosaona, Marie-Julie and La Barbera, Vittorio and Guerrero, Paul and Mitra, Niloy J and Ovsjanikov, Maks},
  journal={arXiv preprint arXiv:1901.01060},
  year={2019}
}
```
