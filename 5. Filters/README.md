# Shift invariant filtering
* A transformation is shift invariant if and only if shifted impulses produce identical but shifted responses

# [Convolution](https://en.wikipedia.org/wiki/Convolution)
* To perform convolution, the filter singal is flipped and set to negative infinity. We then move the flipped filter signal slowly to positive infinity.
* Properties:
	* commutativity: f*s = s*f
	* associativity: f*(g*s) = (f*g)*s
	* distributivity: f*(g+s) = (f)*(g) + (f) * (s)

# Boundary conditions
* What to do at the boundaries when doing convolution?
	* zero padding
		* problem: shift invariance lost
	* end point padding (just extend the boundary point many times)
		* problem: shift invariance lost
	* periodic signal (repeat the signal many times)

# DOG filter (difference of Gaussian)
* I * G1 - I * G2 = I * (G1 - G2)

# [Fourier series](http://mathworld.wolfram.com/FourierSeries.html)

# [Fouier transform](http://mathworld.wolfram.com/FourierTransform.html)




