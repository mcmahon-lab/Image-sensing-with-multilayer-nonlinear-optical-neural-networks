This folder contains all the data and analyzing tools required to produce Figure 4.

==================================================================================================================
Full_EBI_Cell_PLOTS.ipynb

The jupyter notebook was used to compare the performance of different ONN encoders and produce Figure 4.

Dependencies:
-EBI_Cells_grey_w_anomaly3.npz: The extended cell organelle dataset consisting of 10 classes and every single anomly image (only downloadeable from Zenodo due to its file size). The dataset is derived from the 
-Nonlinearity_Curves_April_8_data_refit.npz: The coefficients fitted for the nonlinear activation functions (similar to those shown in Supplementary Figure 8).

Trained models:
All the subdirectories of this folder

------------------------------------------------------------------------------------------------------------------
Full_EBI_Cell_Classifier_batch_training_linear.ipynb: The notebook used to train linear optical classifier for the extended cell-organelle dataset, with varying bottleneck layer dimension.
Full_EBI_Cell_Classifier_batch_training_H1.ipynb: The notebook used to train nonlinear ONN encoders with 2 fully connected layers for the extended cell-organell dataset, with varying bottleneck layer dimensio.
Full_EBI_Cell_conv_batch_train_conv1_ch16.ipynb: The notebook used to train nonlinear ONN encoders with 1 optical convolutional layer (16 channels) followed by 2 optical fully connected layers, with varying bottleneck layer dimension.
Full_EBI_Cell_batch_train_conv3_cbrmcbrcb_ch16.ipynb: The notebook used to train nonlinear ONN encoders with 3 optical convolutional layers (16 channels) followed by 2 optical fully connected layers, with varying bottleneck layer dimension.
Full_EBI_Cell_batch_train_conv3_cbrmcbrcb_ch64.ipynb: The notebook used to train nonlinear ONN encoders with 3 optical convolutional layers (64 channels) followed by 2 optical fully connected layers, with varying bottleneck layer dimension.
Full_EBI_Cell_batch_train_resnet.ipynb: The notebook used to train purely digital convolutional neural networks with pretrained ResNet-18 as the backbone, with varying bottleneck layer dimension.



