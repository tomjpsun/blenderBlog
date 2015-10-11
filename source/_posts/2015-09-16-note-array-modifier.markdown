---
layout: post
title: "Note: Array modifier"
date: 2015-09-16 22:29:06 +0800
comments: true
categories: Array Modifier
---
Array 修改器是 Blender 一個強大的功能。

當使用它的時候，例如：要形成一個鏈條，我們對一個環使用 array modifier, 但是令人困惑的結果，是得到一個環節愈來愈大的鏈條：

<!--More-->

<img src="http://coding-addict.com/pictures/blender/array modifier before applying scale.png" alt="Drawing" style="width: 800px;"/>

apply 物件的 'scale' 可以解決這個現象：

<img src="http://coding-addict.com/pictures/blender/menu of applying object scale.png" alt="Drawing" style="width: 600px;"/>

現在我們可以得到預期的鏈條了：

<img src="http://coding-addict.com/pictures/blender/array modifier after applying object scale.png" alt="Drawing" style="width: 800px;"/>

雖然很簡單，但是摸索時花了一些時間，特此紀錄一下！