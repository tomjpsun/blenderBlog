---
layout: post
title: "Blender Fur WIP"
date: 2014-08-15 15:08:04 +0800
comments: true
categories: particle system, fur
---
##觀念介紹
Blender 的毛髮借由粒子系統(Particle System)來實現。[這是正規的粒子系統介紹](http://wiki.blender.org/index.php/Doc:2.6/Manual/Physics/Particles)：含有基本的界面說明，不在此贅述。該文後有 [Tutorial](http://en.wikibooks.org/wiki/Blender_3D:_Noob_to_Pro/Furry)

Particle System 與 Vertex Group 的關係設定：

* 可先從 Vertex Group 開始，`Edit mode` 下，`Assign` 要長毛髮的 vertex group。
* 新增粒子系統，當做毛髮。
* 設定粒子的 `Vertex Groups`。

這樣就可以規劃毛髮要長在哪些 meshes 上面。

## 
Particle System 與 Material 的連接：

* `Material` 的 `Texture`-`Mapping`-`Coordinate` 屬性要選 `Strand/Particle`
* `Particle`-`Rander` 要選到正確的 `Material number`.

## 
另外，常遺漏的選項：

* 想要毛髮尾端呈透明狀， `Material`-`Transparency` 要勾選才有效 `Material`-`Influence`-`Alpha` 也要選，再加上對應的 `Texture`-`Colors`-`Ramp` 也要勾選，就可以調整透明的程度，`Ramp` 的左側是髮根，右邊是髮梢。
* `Material`-`Strand`-`Blender Units` 要勾選， `Render`的時候就不會使用鏡頭的 view pixel 來呈現毛髮，這樣鏡頭遠近就不會造成 render 的解析度不同了。


##教學影片
[http://cgcookie.com/blender/2010/03/16/creating-hair/](http://cgcookie.com/blender/2010/03/16/creating-hair/)