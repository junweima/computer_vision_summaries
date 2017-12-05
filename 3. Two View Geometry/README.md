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

