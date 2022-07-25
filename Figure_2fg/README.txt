This folder contains all the data and analyzing tools required to produce Figure 2f and 2g.

==================================================================================================================
Generate_datasets.ipynb

The Jupyter notebook for generating the cell-organelle classification datasets for training optical encoders in this study from the raw dataset S-BSST644 Figure 1, available from https://www.ebi.ac.uk/biostudies/ (not included here due to its size).

------------------------------------------------------------------------------------------------------------------
Cell_onn_encdoer_results.ipynb

The Jupyter notebook used for plotting the test accuracy of cell-organelle classification with the 2-layer nonlinear ONN encoder.

Dependencies:
-EBI_Cells.npz: The images of cell organelles sent to the DMD for display.
-Cell_GT_images.npz: The optically fanned out images of cell organelles, as captured by a monitoring capture (see Supplementary Note 2 for explanation).
-Train_Data_Cell_Nonlinear_fc1act1.npz: The intermediate neural activations measured before and after the image intensifier for the train and validation datasets, corresponding to the input and output to the hidden layer (For neural-network architecure, please refer to Supplementary Figure 9).
-Test_Data_Cell_Nonlinear_fc1act1.npz: The same as above, except for using the test dataset.
-Train_Data_Cell_Nonlinear_fc2.npz: The output of the ONN encoder for the train and validation datasets, corresponding to the bottleneck layer (see Supplementary Figure 9).
-Test_Data_Cell_Nonlinear_fc2.npz: The same as above, except for using the test dataset.
-Nonlinear_coeffs.npz: the coefficients fitted for the nonlinear activation functions (similar to those shown in Supplementary Figure 8).

Associated trained models:
-Gen4_retrain_digifc.pt: The final model used to classify cell organelles after layer-by-layer training.

------------------------------------------------------------------------------------------------------------------
Cell_linear_encdoer_results.ipynb

The Jupyter notebook used for plotting the test accuracy of cell-organelle classificaiton with the linear optical encoder.

Dpendencies:
-EBI_Cells.npz: The images of cell organelles sent to the DMD for display.
-Cell_GT_images.npz: The optically fanned out images of cell organelles, as captured by a monitoring capture (see Supplementary Note 2 for explanation).
-Train_Data_Cell_linear.npz: The output of a linear optical encoder measured for the train and validation dataset. 
-Test_Data_Cell_linear.npz: The output of a linear optical encoder measured for the test dataset.

Associated trained models:
-Linear_retrain_digifc.pt: The final linear encoder model used to classify cell organelles.
