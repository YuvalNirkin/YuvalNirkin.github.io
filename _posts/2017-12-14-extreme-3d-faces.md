---
layout: post
title: Extreme 3D Face Reconstruction - Looking Past Occlusions
date: 2017-12-14 00:00:00 +0200
description: # Add post description (optional)
img: publications/extreme_3d_faces/extreme_3d_faces_teaser.jpg # Add image post (optional)
img_thumb: publications/extreme_3d_faces/extreme_3d_faces_teaser_thumb.jpg
post_desc: Existing single view, 3D face reconstruction methods can produce beautifully detailed 3D results, but typically only for near frontal, unobstructed viewpoints. We describe a system designed to provide detailed 3D reconstructions of faces viewed under extreme conditions, out of plane rotations, and occlusions. Motivated by the concept of bump mapping, we propose a layered approach which decouples estimation of a global shape from its mid-level details (e.g., wrinkles). We estimate a coarse 3D face shape which acts as a foundation and then separately layer this foundation with details represented by a bump map. We show how a deep convolutional encoder-decoder can be used to estimate such bump maps. We further show how this approach naturally extends to generate plausible details for occluded facial regions. We test our approach and its components extensively, quantitatively demonstrating the invariance of our estimated facial details. We further provide numerous qualitative examples showing that our method produces detailed 3D face shapes in viewing conditions where existing state of the art often break down.
tags: [Face, 3D Reconstruction, Occlusions] # add tag
type: publication
---
<center><h2><a href="http://cvpr2018.thecvf.com/">CVPR 2018</a></h2></center>
<center><h3>
<a href="https://sites.google.com/site/anhttranusc/">Anh Tuan Tran</a> &nbsp;
<a href="https://talhassner.github.io/home/">Tal Hassner</a> &nbsp;
<a href="https://www-bcf.usc.edu/~iacopoma/">Iacopo Masi</a> &nbsp;
<a href="https://scholar.google.com/citations?user=pB8UHy4AAAAJ&hl=en">Eran Paz</a> &nbsp;
<a href="http://nirkin.com/">Yuval Nirkin</a> &nbsp;
<a href="https://scholar.google.com/citations?user=b0k2tTgAAAAJ&hl=en"> Gérard Medioni</a> 
</h3></center>

>Existing single view, 3D face reconstruction methods can produce beautifully detailed 3D results, but typically only for near frontal, unobstructed viewpoints. We describe a system designed to provide detailed 3D reconstructions of faces viewed under extreme conditions, out of plane rotations, and occlusions. Motivated by the concept of bump mapping, we propose a layered approach which decouples estimation of a global shape from its mid-level details (e.g., wrinkles). We estimate a coarse 3D face shape which acts as a foundation and then separately layer this foundation with details represented by a bump map. We show how a deep convolutional encoder-decoder can be used to estimate such bump maps. We further show how this approach naturally extends to generate plausible details for occluded facial regions. We test our approach and its components extensively, quantitatively demonstrating the invariance of our estimated facial details. We further provide numerous qualitative examples showing that our method produces detailed 3D face shapes in viewing conditions where existing state of the art often break down.

## Overview
![Method Overview]({{site.baseurl}}/assets/img/publications/extreme_3d_faces/system.jpg)

## Downloads
<table class="download" cellspacing="10" style = "text-align:center; margin-left: auto; margin-right: auto;" border="0">
<tr>
	<td><a href="https://arxiv.org/pdf/1712.05083.pdf"><img style = "height:110px;" src="{{site.baseurl}}/assets/img/publications/extreme_3d_faces/thumb_paper.jpg" border="1"></a></td>
	<td><a href="https://github.com/anhttran/extreme_3d_faces"><i class="fa fa-github" style="font-size:96px;color:black"></i></a></td>
</tr>
<tr>
	<td><a href="https://arxiv.org/pdf/1712.05083.pdf">Paper</a></td>
	<td><a href="https://github.com/anhttran/extreme_3d_faces">Code</a></td>
</tr>
</table>

## Citation
{% highlight html %}
@inproceedings{tran2017extreme,
  title={Extreme {3D} Face Reconstruction: Seeing Through Occlusions},
  author={Tran, Anh Tuan and Hassner, Tal and Masi, Iacopo and Paz, Eran and Nirkin, Yuval and Medioni, G\'{e}rard},
  booktitle={IEEE Conf. on Computer Vision and Pattern Recognition (CVPR)},
  year=2018
}
{% endhighlight %}

