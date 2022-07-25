# Optical deep neural network image sensing with optical-to-optical nonlinear activations

This repository contains the code used for generating and analyzing the data in the study "Image sensing with multilayer, nonlinear optical neural networks". We constructed a physical setup of a multi-layer optical neural network (ONN) with two linear layers and an element-wise nonlinear layer in-between. The linear layers were each implemented with a fully optical matrix-vector multiplier, and the optical-to-optical nonlinear activations were implemented with an image intensifier.

A quick guide on the contents of the repository:
* Folder 'Data_Collection_Example' and 'Data_Extraction_Example' contain example scripts for instrument control and data collection through the multilayer optical neural network. 
* Other folders are organized according to the figures of the main text of the paper, each containg the data and the code required to reproduce the plots shown in the main text and associated supplementary figures. Note that some customized dataset used in this study can only be downloaded from Zenodo: https://doi.org/10.5281/zenodo.6888985, due to the size limit of files that are uploadable to GitHub. 
* For an exmaple of training an optical neural network enocder with a digital backend for classification, one can refer to 'Figure_2bcd/QuickDraw_train_onn_encoder.ipynb' as an introduction and 'Figure_4/Full_EBI_Cell_PLOTS.ipynb' for examples with more complex neural-network models.

# How to cite this code

If you use any of our compiled datasets and code in your research, please consider citing the following paper:

> Wang, T., Sohoni, M.M., Wright, L.G. et al. Image sensing with multilayer, nonlinear optical neural networks.

# License

The code in this repository is released under the following license:

[Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/)

A copy of this license is given in this repository as [License.txt](https://github.com/mcmahon-lab/Image-sensing-with-multilayer-nonlinear-optical-neural-networks/blob/master/License.txt).
