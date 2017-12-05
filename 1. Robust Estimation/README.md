# Problem statement:
	To fit a line in a noisy environment when there are lots of outliers is sometimes hard
	Simply using a least squares estimation will fail because of outliers
	We want to come up with a way to fit parameters (lines) without influences of outliers

# Summary:
## Least squares:
* Only taking y-direction errors. 
* Cons: not making x-direction errors.
## Total least squares:
* Taking both x and y direction errors
* Problem: outliers mess things up
## M-estimator:
* Helps with outliers. Usually using GM function is a good idea.
## IRLS (iteratively reweighted least squares)
* Use IRLS if it's hard to compute the exact solution by setting derivative to 0. 
* Similar to EM. Start with an initial guess for parameter p. Then during each iteration: guess the weight (w) using the initial guess, then solve for p using fixed weight w. Then repeat until convergence.
## RANSAC (random sample consensus)
* Hyper parameters:
	* K number of iterations
	* T threshold 
* Steps:
	* Randomly choose n measurement (n being the model parameter number)
	* Use the random parameters to fit and find error (e) and number of inliers (in) that are within threshold T.
	* Run K times and choose the model parameter that has the most inliers
	* Use that model to compute the optimal fit for the inliers
## Hough Transform
* Also deals with outliers but it's usually much slower
			

