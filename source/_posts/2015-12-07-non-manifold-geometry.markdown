---
layout: post
title: "non-manifold geometry"
date: 2015-12-07 13:52:38 +0800
comments: true
categories: 
---
**什麼是 non-manifold geometry?**
原文 : [http://blender.stackexchange.com/questions/7910/what-is-non-manifold-geometry#comment50173_7914](http://blender.stackexchange.com/questions/7910/what-is-non-manifold-geometry#comment50173_7914)

這是 Blender 初學者常常遇到的問題, 簡單解釋 Non-manifold 就是*於真實世界無法存在的幾何圖形*. 

因為如此, 3D 列印也無法印出此幾何圖形, 同時它在 Blender 進行下列動作的時候會有問題：


    反射效果的渲染 (Rendering of refractive effects)

    流體模擬 (Fluid simulations)

    流體模擬 (Boolean operations)

**修正方法**

 `Ctrl` `Shift` `Alt` `M` (找出 non-manifold 的幾何點、線、面)

 `Shift` `G`(Select Similar) 找出只有連結一個邊的端點
 
  `Ctrl` `L`(Select Linked)
  
  因為自己常常忘記, 所以在此紀錄一下！