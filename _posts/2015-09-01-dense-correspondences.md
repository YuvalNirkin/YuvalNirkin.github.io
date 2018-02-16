---
layout: post
title: Dense Correspondences
date: 2015-09-01 00:00:00 +0200
description: # Add post description (optional)
img: projects/dense_correspondences/dense_correspodences_teaser.jpg # Add image post (optional)
tags: [SIFT, Optical Flow, 3D Reconstruction] # add tag
type: project
---
The objective of this project is to apply SIFT-flow into 3D reconstruction. The SIFT-flow and scale propagation algorithms were integrated into an existing 3D reconstruction pipeline, provided by OpenMVG. Part of the SIFT-flow code was available in C++ and the rest had to be converted from Matlab, in order to be fitted in the pipeline and for better performance.

The algorithm is based on the following papers:
[1] M. Tau and T. Hassner, Dense Correspondences Across Scenes and Scales. IEEE Trans. Pattern Anal. Mach. Intell. (TPAMI) 38(5): 875-888 (2016)

[2] C. Liu, J. Yuen, and A. Torralba, “SIFT flow: Dense correspondence across scenes and its applications,” Trans. Pattern Anal. Mach. Intell., vol. 33, no. 5, pp. 978–994, 2011.

For the 3D reconstruction pipeline code: [https://github.com/YuvalNirkin/DenseCorrespondences](https://github.com/YuvalNirkin/DenseCorrespondences)

For the OpenCV contribution code: [https://github.com/YuvalNirkin/opencv_contrib/tree/DenseSIFT](https://github.com/YuvalNirkin/opencv_contrib/tree/DenseSIFT)

## The 3D Reconstruction Pipeline
The pipeline is based on OpenMVG’s pipeline and includes the following modules:

1. Sparse matching – Matching all possible image pairs using SIFT descriptors on sparse keypoints.
2. Dense matching – Matching all possible image pairs using SIFT images.
    * For each image pair find their scale maps using the matched sparse SIFT descriptor’s scales as seed.
    * Calculate the SIFT images of each image pair using their scale maps.
    * Do 2-sided SIFT-flow for every image pair and save pixel pairs that moved to each other as matches.
    * Optionally filter matches from pixels that are in textureless regions.
    * Apply geometric filtering. Using RANSAC on the matches of each image pair to find the corresponding Fundamental Matrix. A pair of matching points that is too far from the corresponding epipolar lines are than filtered out.
3.	Incremental SfM – Calculate the camera’s 3D poses and the scene’s 3D point cloud from the image matches.

## Results
![Results]({{site.baseurl}}/assets/img/projects/dense_correspondences/dense_correspondences_results.jpg)