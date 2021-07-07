---
layout: post
title: "DeepFake Detection Based on the Discrepancy Between the Face and its Context"
date: 2020-08-27 12:00:00 +0200
description: # Add post description (optional)
img: publications/face_vs_context/face_vs_context_teaser.jpg # Add image post (optional)
img_thumb: publications/face_vs_context/face_vs_context_teaser_thumb.jpg
post_desc: "We propose a method for detecting face swapping and other identity manipulations in single images. Face swapping methods, such as DeepFake, manipulate the face region, aiming to adjust the face to the appearance of its context, while leaving the context unchanged. We show that this modus operandi produces discrepancies between the two regions. These discrepancies offer exploitable telltale signs of manipulation. Our approach involves two networks: (i) a face identification network that considers the face region bounded by a tight semantic segmentation, and (ii) a context recognition network that considers the face context (e.g., hair, ears, neck). We describe a method which uses the recognition signals from our two networks to detect such discrepancies, providing a complementary detection signal that improves conventional real vs. fake classifiers commonly used for detecting fake images. Our method achieves state of the art results on the FaceForensics++ and Celeb-DF-v2 benchmarks for face manipulation detection, and even generalizes to detect fakes produced by unseen methods."
tags: [Image Forensics, Deep Learning, Deep Fake, Face Swapping, Fake image Detection] # add tag
type: publication
---

[comment]: **Yuval Nirkin, Yosi Keller, and Tal Hassner, FSGAN: Subject Agnostic Face Swapping and Reenactment, IEEE International Conference on Computer Vision (ICCV)**
<center><h2><a href="https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=34">TPAMI</a></h2></center>
<center><h3>
<a href="https://nirkin.com/">Yuval Nirkin</a> &nbsp;
<a href="http://www.cs.tau.ac.il/~wolf/">Lior Wolf</a> &nbsp;
<a href="https://yosikeller.github.io/">Yosi Keller</a> &nbsp;
<a href="https://talhassner.github.io/home/">Tal Hassner</a>
</h3></center>

>We propose a method for detecting face swapping and other identity manipulations in single images. Face swapping methods, such as DeepFake, manipulate the face region, aiming to adjust the face to the appearance of its context, while leaving the context unchanged. We show that this modus operandi produces discrepancies between the two regions. These discrepancies offer exploitable telltale signs of manipulation. Our approach involves two networks: (i) a face identification network that considers the face region bounded by a tight semantic segmentation, and (ii) a context recognition network that considers the face context (e.g., hair, ears, neck). We describe a method which uses the recognition signals from our two networks to detect such discrepancies, providing a complementary detection signal that improves conventional real vs. fake classifiers commonly used for detecting fake images. Our method achieves state of the art results on the FaceForensics++ and Celeb-DF-v2 benchmarks for face manipulation detection, and even generalizes to detect fakes produced by unseen methods.

## Overview
![Method Overview]({{site.baseurl}}/assets/img/publications/face_vs_context/face_vs_context_system.jpg)

## Downloads
<table class="download" cellspacing="10" style = "text-align:center; margin-left: auto; margin-right: auto;" border="0">
<tr>
	<td><a href="https://arxiv.org/abs/2008.12262.pdf"><img style = "height:110px;" src="{{site.baseurl}}/assets/img/publications/face_vs_context/face_vs_context_paper_thumb.jpg" border="1"></a></td>
</tr>
<tr>
	<td><a href="https://arxiv.org/abs/2008.12262.pdf">Paper</a></td>
</tr>
</table>

## Citation
{% highlight html %}
{% raw %}
@article{nirkin2021deepfake,
  title={DeepFake Detection Based on Discrepancies Between Faces and their Context},
  author={Nirkin, Yuval and Wolf, Lior and Keller, Yosi and Hassner, Tal},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year={2021},
  publisher={IEEE}
}
{% endraw %}
{% endhighlight %}
