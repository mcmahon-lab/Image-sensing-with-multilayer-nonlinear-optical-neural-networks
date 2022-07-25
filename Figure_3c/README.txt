This folder contains all the data and analyzing tools required to produce Figure 3c.

==================================================================================================================
2022-06-05 MLP decoder.ipynb

The jupyter notebook was used to recontruct the QuickDraw images from the 4D feature vectors.

Dependencies:
-Quickdraw_GT_images_April_7.npz: The optically fanned out images of QuickDraw images, as captured by a monitoring capture (see Supplementary Note 2 for explanation).
-Quick_Draw_Dataset_Recon.npz: The target for image reconstruction, which are the original digital images of the QuickDraw dataset.
-Train_Data_Quickdraw_Nonlinear_fc2_April_13.npz: The output of the ONN encoder for the train and validation dataset of QuickDraw, corresponding to the bottleneck layer (see Supplementary Figure 9).
-Test_Data_Quickdraw_Nonlinear_fc2_April_13.npz: The output of the ONN encoder for the test dataset of QuickDraw, corresponding to the bottleneck layer (see Supplementary Figure 9).
