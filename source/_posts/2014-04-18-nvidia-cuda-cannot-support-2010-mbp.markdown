---
layout: post
title: "Nvidia CUDA cannot support 2010 MBP"
date: 2014-04-18 15:06:14 +0800
comments: true
categories: 
---
###Don't bother anymore.###
Current CUDA driver 6.0.37 only support `compute capability` 2.0, my old MBP (Geforce 330M) was ranked capability 1.2.

The hope of installing CUDA Tool NVCC support is also broken: installation the Tool package is OK, while validate with its sample code (try to make) get 'link error'. 

So, my Blender 2.69 can only compute cycle rendering with CPU.
don't bother to enable GPU on it, it's wasting time to drain out the old NVIDIA GPU on a non-open-sourced OS. 

References: 

- NVIDIA Compute Capability & Supported H/W: [http://en.wikipedia.org/wiki/CUDA](http://en.wikipedia.org/wiki/CUDA)



#