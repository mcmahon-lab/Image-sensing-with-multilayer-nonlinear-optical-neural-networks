This folder contains all the data and analyzing tools required to produce Figure 3e.

==================================================================================================================
2022-06-05 MLP decoder.ipynb

The jupyter notebook was used for detecting anormalous cell clusters of the cell-organelle dataset with unsupervized learning technique (spectral clustering).

Dependencies:
-EBI_Cells_w_anomaly.npz: The images of cell organelles sent to the DMD for display, including the normal cell images in EBI_Cells.npz and the additional 418 anomaly images.
-Cell_GT_images.npz: The optically fanned out images of QuickDraw images, as captured by a monitoring capture (see Supplementary Note 2 for explanation).
-Train_Data_Cell_Nonlinear_with_anomaly.npz: The output of the ONN encoder for the train and validation dataset of the cell organelle dataset with anomaly, corresponding to the bottleneck layer (see Supplementary Figure 9).  
-Test_Data_Cell_Nonlinear_with_anomaly.npz: Same as above, but for the test dataset. Note the train and test datasets were combined in the plots, since there is no need for train and test data split in an unsupervised learning task.
