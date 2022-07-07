# Image-Stitching-using-SIFT-features-for-Panorama-Creation-in-Matlab
Image Stitching using SIFT features for Panorama Creation in Matlab

Image Stitching Based on Affine and Homography
Part A:
In part A, two images parliament-left and parliament-right are being stitched.
  1.	Step1: Preprocessing
    1.1.	Conversion to Single
    1.2.	Gray Conversion
  2.	Step2: Detect keypoints and extract descriptors
    2.1.	Frames and descriptors will be extracted Using vl_sift function from vl_feat library.
    2.2.	They are plotted using vl_plotframe
    2.3.	Descriptors are plotted using vl_plotsiftdescriptor.m
  3.	Step3: Match Features
    3.1.	Extracted Descriptors are matched using vl_ubcmatch.m
  4.	Step4: Prune features
    4.1.	Select the closest matches based on the matrix of pairwise descriptor distances
  5.	Step5: Robust Transformation Estimation
    5.1.	Affine Transformation and inliers are calculated using ransacfitaffine.m
    5.2.	Transformation Plotting using fun_plotmatches.m
    5.3.	Outliers are also calculated
  6.	Step6: Compute Optimal Transformation
  7.	Step7: Create panorama
    7.1.	Panorama is created using above data and passed to vl_imwbackward.m
 
Part B:
In part B, two images Glendon-Hall-left, Glendon-Hall-middle and Glendon-Hall-right are being stitched.
  1.	Step1: Preprocessing
    1.1.	Conversion to Single
    1.2.	Gray Conversion
  2.	Step2: Detect keypoints and extract descriptors
    2.1.	Frames and descriptors will be extracted Using vl_sift function from vl_feat library.
    2.2.	They are plotted using vl_plotframe
    2.3.	Descriptors are plotted using vl_plotsiftdescriptor.m
  3.	Step3: Match Features
    3.1.	Extracted Descriptors are matched using vl_ubcmatch.m
  4.	Step4: Prune features
    4.1.	Select the closest matches based on the matrix of pairwise descriptor distances
  5.	Step5: Robust Transformation Estimation
    5.1.	vl_colsubset is used for homography estimation.
    5.2.	Kronecker tensor and VL_HAT  Hat operator are also used.
    5.3.	Svd is calculated.
    5.4.	Hence score homography is calculated.
  6.	Step6: Compute Optimal Transformation 
    6.1.	Max Score is selected from homography score.
    6.2.	Homography based points are then plotted.
  7.	Step7: Create panorama
    7.1.	Panorama is created using above data and passed to vl_imwbackward.m
