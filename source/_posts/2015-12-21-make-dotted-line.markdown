---
layout: post
title: "Make Dotted Line"
date: 2015-12-21 14:48:04 +0800
comments: true
categories: array modifier, curve
---
Array modifier 之前的文章已經有過初步的接觸, 這篇記錄一下 Array modifier + Curve Line 並用的方法, 以紀念摸索了半天的成果.
<!--More-->

* Add Bezier Curve, 命名為 _BezierCurve_ 進入 Edit mode, 分別為兩個 handles 新增 __hook to new empty__ object, 注意：Curve 另一邊也需要哦, 就不另外提供圖示了.

<img src="http://coding-addict.com/pictures/blender/dotted line - hook to empty object.png" alt="Drawing" style="width: 600px;"/>

* 如果需要, 可以離開 Edit mode, 選取 Empty object, 調整它的 size.

<img src="http://coding-addict.com/pictures/blender/dotted line - set empty size.png" alt="Drawing" style="width: 300px;"/>

* 現在開始做虛線的主體：新增一個 cube, 縮小到符合我們的需要


<img src="http://coding-addict.com/pictures/blender/dotted line - new cube.png" alt="Drawing" style="width: 300px;"/>

* cube 新增 array modifier, `Curve` 設定成我們的 _BezierCurve_

<img src="http://coding-addict.com/pictures/blender/dotted line - add array modifier.png" alt="Drawing" style="width: 600px;"/>


＊最重要的就是這一步, 在 array modifier 上再加一個 curve modifier, `Object` 也設定成我們的 _BezierCurve_


<img src="http://coding-addict.com/pictures/blender/dotted line - add curve modifier.png" alt="Drawing" style="width: 600px;"/>

* 新增 cube 時, 我們有縮小 cube, 所以這裡需要 `apply scale` (結果要得到 scale = (x: 1.00, y: 1.00, z: 1.00 ))


<img src="http://coding-addict.com/pictures/blender/dotted line - apply scale.png" alt="Drawing" style="width: 600px;"/>

* 調整 array offset 使我們的虛線有合理的間距

<img src="http://coding-addict.com/pictures/blender/dotted line - adjust array offset.png" alt="Drawing" style="width: 600px;"/>

* 完成了, 拉動任意一邊的 Empty object 就可以了

<img src="http://coding-addict.com/pictures/blender/dotted line - finished.png" alt="Drawing" style="width: 600px;"/>




