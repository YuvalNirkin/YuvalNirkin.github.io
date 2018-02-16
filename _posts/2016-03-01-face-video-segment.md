---
layout: post
title: Face Video Segment
date: 2016-03-01 00:00:00 +0200
description: # Add post description (optional)
img: projects/face_video_segment_teaser.jpg # Add image post (optional)
tags: [Face, Video, Segmentation] # add tag
type: project
---
This project contains a collection of tools for semi-supervised gathering of ground truth face segmentation data from videos.
A stable hierarchy of regions with temporal coherence is computed from dense optical flow using [Efficient hierarchical graph-based video segmentation](https://smartech.gatech.edu/bitstream/handle/1853/38305/cvpr2010_videosegmentation.pdf).
Facial landmarks, extended to also include the forehead, are then used to extract the face contour.
Regions are classified as belonging to the face segment according to their overlap with the face contour.
The regions can then be further processed using a simple interface which allows browsing the entire video and manually classifying the regions using simple mouse clicks.

Code has been made available at: [https://github.com/YuvalNirkin/face_video_segment](https://github.com/YuvalNirkin/face_video_segment)
