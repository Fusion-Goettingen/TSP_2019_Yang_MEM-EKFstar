# Introduction
This repository is a MATLAB implementation of MEM-EKF*, which is described in
```
Tracking the orientation and axes lengths of an elliptical extended object, by Shishan Yang and Marcus Baum in IEEE Transactions on Signal Processing 67.18 (2019): 4720-4729.
```

To get an intuition, you can run demo.m script. It simulates a tracking scenario using constant turn model. 

# Parameter tuning
As MEM-EKF* models semi-axes lengths as Gaussian distrubted variables, it is sensitive to 
* the prior covariance of shape variable,
* the covariance of process noise for shape variable. 

Therefore, the following guidelines are given for setting the covariances for shape variables: 
* the prior covariance of the shape variable should not be too large compare to the mean. Otherwise, the lengths could stretch to the negative part of the Gaussian distribution;
* if we are tracking extended objects with fixed sizes, we recommend low values in the process noise covariance for lengths variables.
