# EM algorithm
* Steps:
	* E-step: Fix model parameters and compute data assignments
	* M-step: Given assignments, compute ML estimate of model parameters
	* Repeat above steps until convergence

# MSAC (M-estimator Sample and Consensus)
* Basically it is RANSAC with M-esimator for the last step
* Steps (only last step is different from RANSAC):
	* Randomly choose n measurement (n being the model parameter number)
	* Use the random parameters to fit and find error (e) and number of inliers (in) that are within threshold T.
	* Run K times and choose the model parameter that has the most inliers
	* Use that model to compute the optimal fit for the inliers with M-estimator

# MLESAC 
* Use 2 distributions to model inliers and outliers separately
	* inliers: follow Gaussian distribution
	* outliers: follow linear distribution
* MLESAC = RANSAC but use mixing probability for inliers







