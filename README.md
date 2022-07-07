# Image-Stitching-using-SIFT-features-for-Panorama-Creation-in-Matlab
Image Stitching using SIFT features for Panorama Creation in Matlab

Image Stitching Based on Affine and Homography
Part A:
In part A, two images parliament-left and parliament-right are being stitched.
  1.	Step1: Preprocessing<br>
    1.1.	Conversion to Single<br>
    1.2.	Gray Conversion<br>
  2.	Step2: Detect keypoints and extract descriptors<br>
    2.1.	Frames and descriptors will be extracted Using vl_sift function from vl_feat library.<br>
    2.2.	They are plotted using vl_plotframe<br>
    2.3.	Descriptors are plotted using vl_plotsiftdescriptor.m<br>
  3.	Step3: Match Features<br>
    3.1.	Extracted Descriptors are matched using vl_ubcmatch.m<br>
  4.	Step4: Prune features<br>
    4.1.	Select the closest matches based on the matrix of pairwise descriptor distances<br>
  5.	Step5: Robust Transformation Estimation<br>
    5.1.	Affine Transformation and inliers are calculated using ransacfitaffine.m<br>
    5.2.	Transformation Plotting using fun_plotmatches.m<br>
    5.3.	Outliers are also calculated<br>
  6.	Step6: Compute Optimal Transformation<br>
  7.	Step7: Create panorama<br>
    7.1.	Panorama is created using above data and passed to vl_imwbackward.m<br>
 <br>
Part B:<br>
In part B, two images Glendon-Hall-left, Glendon-Hall-middle and Glendon-Hall-right are being stitched.<br>
  1.	Step1: Preprocessing<br>
    1.1.	Conversion to Single<br>
    1.2.	Gray Conversion<br>
  2.	Step2: Detect keypoints and extract descriptors<br>
    2.1.	Frames and descriptors will be extracted Using vl_sift function from vl_feat library.<br>
    2.2.	They are plotted using vl_plotframe<br>
    2.3.	Descriptors are plotted using vl_plotsiftdescriptor.m<br>
  3.	Step3: Match Features<br>
    3.1.	Extracted Descriptors are matched using vl_ubcmatch.m<br>
  4.	Step4: Prune features<br>
    4.1.	Select the closest matches based on the matrix of pairwise descriptor distances<br>
  5.	Step5: Robust Transformation Estimation<br>
    5.1.	vl_colsubset is used for homography estimation.<br>
    5.2.	Kronecker tensor and VL_HAT  Hat operator are also used.<br>
    5.3.	Svd is calculated.<br>
    5.4.	Hence score homography is calculated.<br>
  6.	Step6: Compute Optimal Transformation <br>
    6.1.	Max Score is selected from homography score.<br>
    6.2.	Homography based points are then plotted.<br>
  7.	Step7: Create panorama<br>
    7.1.	Panorama is created using above data and passed to vl_imwbackward.m <br>
