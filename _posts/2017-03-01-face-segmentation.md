---
layout: post
title: Face Segmentation
date: 2017-03-01 00:00:00 +0200
description: # Add post description (optional)
img: face_segmentation_teaser.jpg # Add image post (optional)
tags: [Face Segmentation] # add tag
type: project
---
Face Segmentation is not a very well defined problem. We define face segmentation to include the visible part of the face excluding
the neck, ears, hair, long beards, and any object that might obscure it. This project implements face segmentation using a fully convolutional neural network as described in [our paper](https://arxiv.org/abs/1704.06729).

Code has been made available at: [https://github.com/YuvalNirkin/face_segmentation](https://github.com/YuvalNirkin/face_segmentation)

## Overview
Our method uses a FCN to segment the visible parts of faces from their context and occlusion.
We used the FCN-8s-VGG architecture, fine-tuned for segmentation, for which we fuse information at different locations from
layers with different strides

![Face Segmentation CNN (FCN-8s-VGG)]({{site.baseurl}}/assets/img/seg_fcn.jpg)

## Training
The network was trained on IARPA Janus CS2 dataset (excluding subjects that are also in [LFW](http://vis-www.cs.umass.edu/lfw/)) 
using a novel process for collecting ground truth face segmentations,
involving our tool for [semi-supervised Face video segmentation](https://github.com/YuvalNirkin/face_video_segment).

![Face Segmentation CNN (FCN-8s-VGG)]({{site.baseurl}}/assets/img/fvs_sample.jpg)

We generate additional synthetic images by augmenting 3D models of glasses and microphones:

![Face Segmentation CNN (FCN-8s-VGG)]({{site.baseurl}}/assets/img/obj_aug.png)

We couldn't find quality 3D models of hands, so for augmenting hands we used the [EgoHands dataset](http://vision.soic.indiana.edu/projects/egohands/),
which included images of hands and their segmentations:

![Face Segmentation CNN (FCN-8s-VGG)]({{site.baseurl}}/assets/img/hand_aug.png)

