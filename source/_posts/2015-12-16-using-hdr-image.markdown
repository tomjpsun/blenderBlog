---
layout: post
title: "Using HDR image"
date: 2015-12-16 18:04:12 +0800
comments: true
categories: 
---
用 HDR image 當作背景是很方便的事, 步驟太簡單, 以至於出問題時, 估狗竟然找不到... 啊 我就遇到了！

下載 HDR images:
---

柏克萊教授的網站：

[http://gl.ict.usc.edu/Data/HighResProbes/](http://gl.ict.usc.edu/Data/HighResProbes/)

賣 HDR image 的會有幾個 free HDR images:

[http://www.hdrmill.com/freebies.htm](http://www.hdrmill.com/freebies.htm)

In Blender
---

這裡犯的錯誤,是讓我寫這篇的原因：

在 `World` tab 下：

`Surface` 選 `Background`

`Color` 選 __`Environment Texture`__ 不是 `Image Texture`,

選 `Environment Texture` 不是 `Image Texture`, 

<img src="http://coding-addict.com/pictures/blender/using HDR image.png" alt="Drawing" style="width: 420px;"/>

**很重要所以講兩遍！！ ( 選錯會看到一片模糊單色的背景 )！！** 

用 Blender 自製 HDR:
---

當然可用 Blender 自給自足, 目前只有 __cycle render mode__ 可以支援, 佈置好你的場景後, 就可以 Render 出來了.

主要是鏡頭設定為 5mm, `Panoramic` 選 `Equitangular`,
還有設定解析度. 

<img src="http://coding-addict.com/pictures/blender/set camera to make HDR image 1.png" alt="Drawing" style="width: 300px;"/>

<img src="http://coding-addict.com/pictures/blender/set camera to make HDR image 2.png" alt="Drawing" style="width: 300px;"/>

<img src="http://coding-addict.com/pictures/blender/set render resolution to make HDR image.png" alt="Drawing" style="width: 300px;"/>
