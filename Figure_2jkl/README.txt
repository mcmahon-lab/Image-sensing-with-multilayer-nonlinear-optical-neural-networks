This folder contains all the data and analyzing tools required to produce Figure 2j, 2k, and 2l.

==================================================================================================================
Speedsign_classifiers.ipynb
 
The jupyter notebook was used to fit the viewing angle of the speed-limit signs based on the 2D feature vectors produced by the ONN encoder.

Dependencies:
-Real_Scene_slims_GT_images_total.npz: The ground truth images of various speed-limit signed, as taken by a monitoring camera. 
-Speedsign_nonlinear.npz: The output of the 2-layer nonlinear ONN encoder, which encoded the full speed-limit sign images to 2D feature vectors. The file includes train, validation, and test datasets.
-Speedsign_linear.npz: The output of the linear optical encoder, which encoded the full speed-limit sign images to 2D feature vectors. The file includes train, validation, and test datasets.
-Nonlinearity_Curves_April_8_data_refit.npz: The coefficients fitted for the nonlinear activation functions (similar to those shown in Supplementary Figure 8).
 
Trained models:
-speedlimit_nonlinear_classifier.pt: The 2-layer digital classifier that maps the nonlinearl encoded speed-limit-sign images to speed-limit numbers.
-speedlimit_linear_classifier.pt: The 2-layer digital classifier that maps the linearly encoded speed-limit-sign images to speed-limit numbers.