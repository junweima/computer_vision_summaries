# Image gradient
* basically the gradient of a pixel. \grad I  = I_x + I_y

# Gradient estimation using Gaussian filter
* Gaussian filter \grad G = [G_x G_y] can be used to estimate Image gradient (R)
* Image gradient can be estimated as a convolution of Gaussian filter and the image: R = \grad G * I 

# Zero crossing
* It is used to find the edge
* We set the second derivative of I(x) to 0 and solve for x to find zero crossing point (i.e. edge point)

# [Canny edge detection](https://www.youtube.com/watch?time_continue=235&v=CLmtC0H8Fvk)
* Steps:
	* Find gradients by convolving image with Gaussian filter: R = \grad G * I
	* Find magnitudes and orientations of gradients R
	* Set threshold T to remove some sparse edges
	* Non-maximal suppression (thinning): basically make thick edges thinner
	* Hysteresis thresholding 
		* basically means that strong pixel edges are linked through weak pixel edges so there is less discontinuity





