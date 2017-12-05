# Image projections
## Homegenous coordinates
* Euclidean coordiante: [x, y]
* Equivalent homogenos coordinate: lambda * [x, y, 1]
## Line equation
* the line parameter multiplying point is 0: l^T p = 0 
## Line passing 2 points
* l = p_1 \cross p_2
## Intersection of 2 lines
* p = l_1 \cross l_2
## Intrinsic calibration matrix
* convert camera coordinates to image coordinates
## Extrinsic calibration matrix
* convert world coordinates to camera coordinates
### note:
* camera to world: rotate by camera coordinates by R and add e
* world to camera: rotate world coordinates by R^T and add -R^T e

