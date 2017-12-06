# Epipolar line
* Scene point from one image plane can be projected as a line to the other image plane

# Fundamental matrix
* l_1 = F x_1 is the epipolar line generated from x_1 onto image plane 2
* l_2 = F^T x_2 is the epipolar line generated from x_2 onto  image plane 1
* DOF (degree of freedom) = 7
* rank = 2
* det(F) = 0

# Essential matrix
* Basically Fundamental matrix but dealing with points in camera coordinates
* p_1^T E p_2 = 0
* DOF = 5
* rank = 2
* det(E) = 0

# Epipolar constraint
* x_2^T F x_1 = 0
* basically it's saying that the corresponding point on the other image plane is on the epipolar line

# Epipole
* The epipole is the intersection of all epipolar lines
* The epipole is also the projection of the other image plane's camera to its image plane

# Good to know's:
* If epipolar lines are parallel => 2 cameras are translated
* If epipole is in the middle of the image => 2 cameras are moved forward and backward

# Gold standard algorithm
* Basically least squares weighted by the noise variance
* It's computationally inefficient

# 8 points algorithm
* Use equation AF = 0 instead of x_1^T F x_2 = 0 to estimate F (note that we need to express A in terms of x_1 and x_2)
* Note that it's actually using 7 points (mentioned in udacity course by prof. Bobick) but we use 8 anyways.
* Cons: scaling is poor

# [normalized 8 points algorithm](https://www.coursera.org/learn/robotics-perception/lecture/yuawM/bundle-adjustment-iii)
* It overcomes the sclaing problem 8 point algorithm has
* steps:
	* re-center and re-scale points {x} using matrix M so that mean{x}=0 var{x}=1 (the number of points K should be greater or equal to 8)
	* Find F by minimizing O(F) = sum(x_1^T F x_2)^2 for all points {x} where x_1 and x_2 are normalized points from the previous step
		* This is usually done by using equation AF = 0 instead of x_1^T F x_2 = 0 to estimate F (note that we need to express A in terms of x_1 and x_2)
		* We can solve the equation AF=0 by finding SVD of A
		* Then we need to clean up F by forcing it to be ranked 2
	* Project F to the nearest rank 2 matrix using SVD
	* Undo normalization using matrix M: F = M^T F M

# Homography
* It defines a linear mapping between image plane 1 and image plane 2 given that all points are projecting from a single plane
* x_2 = H x_1

# [Stereo image rectification](https://www.youtube.com/watch?time_continue=177&v=1AsCPRpCvxU)
* Warping skewed plane to an unskewed plane 


