# Three ways of thinking about motion and video
* feature points in motion
* time-varying 2D image
* spatiotemporal 3D volume

# 2D motion field and optical flow
* 2D motion field: 2D velocity of all visible points
* optical flow field: estimate of 2D motion field

# brightness constancy constraint
* The pixel brightness for time t and t+1 remains the same despite motion [u1,u2]
* It basically assumes that the motion is small
* I(x,y,t+1) = I(x-u1,y-u2,t)

# gradient constraint equation
* The 2D motion along image gradient is equal to the negative of pixel brightness change along time axis
* u * \grad f + f_t = 0

# normal velocity
* u_n = -f_t/norm(\grad f) \dot \grad f/norm(\grad f)
* the normal velocity is equal to the temporal velocity dot with pixel gradient

# aperture problem
* Only normal velocity can be estimatede at a single point

# optical flow difficulties
* outliers
	* potental solution: robusst optical flow estimation
* large motion
	* potential solution: iterative flow estimation
* aliasing
	* coarse-to-fine estimation



