---
layout: post
title: "stack UV vs unique UV"
date: 2013-08-28 07:34
comments: true
categories: blender
---
根據 Jason Welsh 的教學 
	
Stacked UVs <https://www.youtube.com/watch?v=WP0OAl3JTI8>

Unique UVs <https://www.youtube.com/watch?v=CqBE2Ln6Ayg>

Stacked vs Unique <https://www.youtube.com/watch?v=2fW6S3wQy5E>

可以知道兩者的 8片棧板木條複製 都是在 `object-mode` 進行。但是作 UV unwrap 時 stacked 的 **UVs 不特別處理而重疊**，unique 的 **UVs 經過 UV pack 處理後會平均分布於 UV map 上**。

<!-- more -->

這樣 stacked UV 每個 UV 會佔據比較大的 UV map，也就是 resolution 比較高，而 unique UV 相對就比較小（因為要排同樣的 8 片棧板 UV)，看下圖比較就清楚了：

這是 stack UV:
![stack UV](http://coding-addict.com/pictures/blender/stackUV.png)

這是 unique UV:
![unique UV](http://coding-addict.com/pictures/blender/uniqueUV.png)

附上原始 blender 檔 <http://coding-addict.com/pictures/blender/stackUV_vs_uniqueUV.blend>

以此例來說，unique UV 可以表現棧板上每一根木材在不同位置的材質感，雖然解析度較低，但是中距離看，會比較像實際場景。而 stacked UV 做出來的每一根木頭都會一樣，雖然解析度高，但是貼上後會發現所有木材都是同樣的 pattern，一般來說只有某些情形才使用 stacked UV.