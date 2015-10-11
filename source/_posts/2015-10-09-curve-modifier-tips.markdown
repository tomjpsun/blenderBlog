---
layout: post
title: "Curve Modifier Tips"
date: 2015-10-09 08:08:54 +0800
comments: true
categories: curve modifier
---

Blender 的 Curve modifier 對需要彎曲變形的物件編輯很給力. 對於初學者的我, 還是有一些小技巧需要紀錄一下：
<!--More-->
**Align the curve endpoint**

有時候，我想要把物件依照 curve 的形狀變形, 並且想要對齊 curve 的一個端點,
在這裡的範例, 我用了一個 Cylinder 物件切了三、四十個等分, 然後用 `curve modifier` , 準備讓他依照一個 NurbsCurve 變形：

<img src="http://coding-addict.com/pictures/blender/curve-prepare-objects.png" alt="Drawing" style="width: 600px;"/>


上圖的右上區 outliner 列表, 可以看到我們有 Cylinder 物件, 還有 NurbsCurve 物件. 並且對 Cylinder 加入 `curve modifier`.

為了後面方便檢視, 將兩個物件與 `blender cursor` 都 `snap` 到原點.

切到 `object mode` 可以看到變形：

<img src="http://coding-addict.com/pictures/blender/curve-after-applying-modifier.png" alt="Drawing" style="width: 600px;"/>

直接將 Cylinder 拉到對齊 NurbsCurve 即可：

<img src="http://coding-addict.com/pictures/blender/curve-adjust-to-curve-endpoint.png" alt="Drawing" style="width: 600px;"/>


簡單吧！




