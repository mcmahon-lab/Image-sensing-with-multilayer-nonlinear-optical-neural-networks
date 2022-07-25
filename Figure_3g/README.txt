This folder contains all the data and analyzing tools required to produce Figure 3g.

==================================================================================================================
NN_nonlinear_regression_angle_prediction.ipynb

The jupyter notebook was used to fit the viewing angle of the speed-limit signs based on the 2D feature vectors produced by the ONN encoder.

Dependencies:
-Full_Data_RealScene_Nonlinear_retrain.npz: The output of the 2-layer nonlinear ONN encoder, which encoded the full speed-limit sign images to 2D feature vectors. The file includes train, validation, and test datasets.
-Full_Data_RealScene_Nonlinear_retrain_signs2.npz: The output of the 2-layer nonlinear ONN encoder, which encoded the full speed-limit sign images to 2D feature vectors. The file includes train, validation, and test datasets of speed-limit signs additional to Full_Data_RealScene_Nonlinear_retrain.npz.