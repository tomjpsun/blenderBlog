---
layout: post
title: "UV unwrap tips"
date: 2015-07-10 07:12:40 +0800
comments: true
categories: UV unwrap
---
在 [Blender CG: Fndamental of Texturing](https://cgcookie.com/course/introduction-to-texturing/) 的影片, 介紹了幾個 UV unwrap 技巧，這裡記錄一下：(以 Blender 2.72 為環境)
<!--More-->
* Mark Seam

	進入 Edit Mode 之後, 將所選的 edge 當作 mark seam: `Ctrl-E` 可以叫出選單, 裡面有 `Mark Seam` 選項

* Live Unwrap:

	有時我們會想要即時的看到 Mark Seam 的結果, 勾選左側 `ToolBox` | `Options` | `Live Unwrap` 即可
	
	<img src="http://coding-addict.com/pictures/blender/live unwrap.png" alt="Drawing" style="width: 200px;"/>
	
* Unwrap with Stretch:

	`UV map property panel` | `Display` | `Stretch` 選項, 可以打開__以顏色表示張力__ 的選項. 以 Suzanne 為例：
	
	<img src="http://coding-addict.com/pictures/blender/unwrap with stretch.png" alt="Drawing" style="width: 400px;"/>

* Mirror the Seam:

	`Shift-G` | `Seam` 可以選取所有的 seam edges, 然後 `Select` | `Mirror` 即可將 mirror 的部分, mark 出同樣的 seam:
	
	<img src="http://coding-addict.com/pictures/blender/select similar.png" alt="Drawing" style="width: 400px;"/>
		
		
	
	