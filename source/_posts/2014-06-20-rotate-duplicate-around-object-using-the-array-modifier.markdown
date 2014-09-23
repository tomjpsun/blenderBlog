---
layout: post
title: "Rotate Duplicate Around Object Using the Array Modifier"
date: 2014-06-20 17:16:43 +0800
comments: true
categories: array modifier, modeling
---

If you are following [this video](https://www.youtube.com/watch?v=s5teWMHUDgs). You may encounter the duplicated array object __only rotate__ around its center instead of the `empty object` in the video --- which is not what you expect.

Please see [another video here](https://www.youtube.com/watch?annotation_id=annotation_2966241117&feature=iv&src_vid=iyoRtGKegus&v=whjFb0xFoLk), the tricky part is : Using `Edit Mode` to move your mesh first, such that the mesh is offset with its own __object center__. (i.e. the __transformation__ data is what the __array modifier__ operated on), then the Duplicated array objects can surround the `empty object` as you want.

It tooks me 4 hours to figure out, sigh!