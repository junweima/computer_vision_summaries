# SFM goal
* The goal is to recover 3D shape based on image projections
* The ultimate goal is to solve [bundle adjustment](https://www.coursera.org/learn/robotics-perception/lecture/oDj0o/bundle-adjustment-i)

# Factorization algorithm
* It is used to estimate 3D scene points
* C = M D
	* C = Data matrix (the 2D projections)
	* M = Camera motion matrix (defines the projections)
	* D = Shape matrix (basically the 3D points that we are trying to estimate)
* steps:
	* normalize the data points (2D) by using the centroid as origin (just subtract centroid point from all points)
	* [USV] = svd(C). Use SVD on data matrix
	* Force C to be rank 3 by setting all singular values to 0 except the first 3 in S (sigma)
	* Return U as M (camera matrix) and SV as D (shape matrix)
	* Euclidean upgrade
	![Euclidean upgrade](/images/euclidean_upgrade.jpg)



