This folder contains all the data and analyzing tools required to produce Figure 2b, 2c, and 2d.

==================================================================================================================
QuickDraw_onn_encoder_results.ipynb

The Jupyter notebook for plotting QuickDraw test accuracy of the 2-layer nonlinear optical-neural-network (ONN) encoder.

Dependencies:
-Quickdraw_GT_images_April_7.npz: The optically fanned out images of QuickDraw images, as captured by a monitoring capture (see Supplementary Note 2 for explanation).
-Train_Data_Quickdraw_Nonlinear_fc1act1.npz: The intermediate neural activations measured before and after the image intensifier for the train and validation datasets of QuickDraw, corresponding to the input and output to the hidden layer (see Supplementary Figure 9).
-Test_Data_Quickdraw_Nonlinear_fc1act1.npz: The same as above for the test dataset of QuickDraw.
-Train_Data_Quickdraw_Nonlinear_fc2.npz: The output of the ONN encoder for the train and validation datasets of QuickDraw, corresponding to the bottleneck layer (see Supplementary Figure 9).
-Test_Data_Quickdraw_Nonlinear_fc2.npz: The same as above, except for using the test dataset of QuickDraw.
-Nonlinear_coeffs.npz: the coefficients fitted for the nonlinear activation functions (similar to those shown in Supplementary Figure 8).

Associated trained models:
-Gen1_original_onn_encoder.pt: The full digital model of ONN encoder trained with Quickdraw_GT_images_April_7.npz as the inputs.
-Gen2_retrain_fc1act1.pt: The ONN encoder with fully connected layer 1 (fc1) retrained to adapt to the actual measured nonlinear activation function (act1); otherwise the same training procedure as Gen1.
-Gen3_retrain_fc2.pt: The ONN encoder with fully connected layer 2 (fc2) retrained while with fc1 weights trained in Gen2 model fixed.
-Gen4_retrain_digifc.pt: The ONN encoder with the digital decoder layer retrained while with both fc1 and fc2 weights fixed. Figure 2c and d were plotted with this model.

------------------------------------------------------------------------------------------------------------------
QuickDraw_linear_encoder_results.ipynb

The Jupyter notebook for plotting QuickDraw test accuracy of the linear optical encoder.

Dependencies:
-Quickdraw_GT_images_April_7.npz: The optically fanned out images of QuickDraw images, as captured by a monitoring capture (see Supplementary Note 2 for explanation).
-Train_Data_QuickDraw_linear.npz: The output of a linear optical encoder measured for the train and validation datasets of QuickDraw.
-Train_Data_QuickDraw_linear.npz: The output of a linear optical encoder measured for the test dataset of QuickDraw.

Associated trained models:
-Linear_retrain_digifc.pt: The linear optical encoder with only the digital decoder layer retrained. Figure 2b and d were plotted with this model.

------------------------------------------------------------------------------------------------------------------
QuickDraw_pure_digital_classifiers.ipynb

The Jupyter notebook for training and plotting pure digital models for classifying QuickDraw data. 
Each digital model (linear or 2-layer nonlinear) has the same same neural-network layer width as its corresponding optical encoder model. The difference is that the digital models use standard digital fully connected layers nn.Linear() modules (containing both weights and biases with positive and negative number at FP16 precision) and the nonlinear activation function used is the ideal sigmoid function. 

Associated trained models:
-Direct_downsampling.pt: The digital linear classifier trained for 4D vectors derived from direct downsampling of the original images in Quickdraw_GT_images_April_7.npz, the test accuracy is plotted in Figure 2d.
-Digital_linear.pt: The trained digital linear encoder plus a single-layer digital backend for classification. Its test accuracy is plotted in Figure 2d.
-Digital_nonlinear.pt: The trained digital 2-layer nonlinear encoder plus a single-layer digital backend for classification. Its test accuracy is plotted in Figure 2d.

------------------------------------------------------------------------------------------------------------------
QuickDraw_train_onn_encoder.ipynb

This jupyter notebook contains example code to train an ONN encoder using the optically fanned out images of the QuickDraw dataset.

Dependencies:
-Quickdraw_GT_images_April_7.npz: The optically fanned out images of QuickDraw images, as captured by a monitoring capture (see Supplementary Note 2 for explanation).
-Nonlinear_coeffs.npz: the coefficients fitted for the nonlinear activation functions (similar to those shown in Supplementary Figure 8).