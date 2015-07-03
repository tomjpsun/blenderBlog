---
layout: post
title: "Blender Material Slot WIP"
date: 2014-12-07 22:56:44 +0800
comments: true
categories: 
---
#Bake#

這裏我們要 bake displacement 與 bake ambient occlusion 兩種圖。

* Bake 之前要先 UV unwrap，將來所有的 bake 都會在這個 UV image  上面
* Bake Displacement 時，如果勾選 Bake from Multires ，且得到灰色均一的圖，可能是 MultiRes Modifier 的 preview level 與 sculpt level 相等 造成的，把 preview level 與 sculpt level 相差愈多，就得到愈高解析度的 DISP, 但, 如果 preview level 設定到 0, 會得到一格格的結果, 也不對
* 如果得到 error: Multires data baking requires multiresolution object 的錯誤訊息，就表示 Modifier stack 上面的 multires 不是最上層，可以把在它上面所有的 modifier 的 render 關掉
<img src="http://coding-addict.com/pictures/blender/turn off render on modifiers stack.png" alt="Drawing" style="width: 800px;"/>
* Bake 需要有一個 default world ，若沒有，會報錯，這時 create 一個 world 就好了
* Bake 的 margin 若為 0 ，可能將來貼上去會有隙縫，系統內定為 2 ，表示 bake 會超過 UV map 邊界 2 pixels，以防止上述現象。
<!--More-->
<img src="http://coding-addict.com/pictures/blender/blender material WIP 1.png" alt="Drawing" style="width: 800px;"/>

* Bake Displacement 如果沒選 bake from multires 就會得到一片黑色的 displacement
* Bake Ambient Occlusion 後，UV Image Editor 的 Image 選項會有 * 符號，把它存檔為 bake_AO.png
* Bake Displacement 後存為 bake_DISP.png

#Paint#

* 1 Edit mode 全選要 paint 的物件
* 2 進 Texture paint mode，然後 add ‘Defuse Color’ slot

<img src="http://coding-addict.com/pictures/blender/blender material WIP 2.png" alt="Drawing" style="width: 800px;"/>

設定 Paint solt 對應的 paint image 大小，本例為 4096

<img src="http://coding-addict.com/pictures/blender/blender material WIP 3.png" alt="Drawing" style="width: 300px;"/>

選擇 brush

<img src="http://coding-addict.com/pictures/blender/blender material WIP 4.png" alt="Drawing" style="width: 1000px;"/>

命名為 `my brush`

<img src="http://coding-addict.com/pictures/blender/blender material WIP 5.png" alt="Drawing" style="width: 150px;"/>

我們的 paint slot 對應到的 image 為 "Material Diffuse Color"

<img src="http://coding-addict.com/pictures/blender/blender material WIP 6.png" alt="Drawing" style="width: 400px;"/>

注意：此時 image 剛生成，所以打 * 表示需要存檔

<img src="http://coding-addict.com/pictures/blender/blender material WIP 7.png" alt="Drawing" style="width: 300px;"/>

現在按右方的 new ，然後選擇我們的 paint texture，同時也會出現在左邊的 texture panel

<img src="http://coding-addict.com/pictures/blender/blender material WIP 8.png" alt="Drawing" style="width: 1000px;"/>

<img src="http://coding-addict.com/pictures/blender/blender material WIP 9.png" alt="Drawing" style="width: 1000px;"/>

`brush mapping` 選擇為 `stencil`

<img src="http://coding-addict.com/pictures/blender/blender material WIP 10.png" alt="Drawing" style="width: 150px;"/>

務必確認 paint panel | options 裡面的 `show brush` 有打開

<img src="http://coding-addict.com/pictures/blender/blender material WIP 11.png" alt="Drawing" style="width: 800px;"/>

如果上述設定都正確，游標移入 view 時應該可看到 paint texture。
操作 paint texture 的方式：

* 滑鼠右鍵(R-Click)：移動 texture
* shift + R-Click：縮放 texture
* ctrl + R-Click：旋轉 texture

<img src="http://coding-addict.com/pictures/blender/blender material WIP 12.png" alt="Drawing" style="width: 800px;"/>

此時 paint image 也會出現目前 paint 的成果。`save as image` 可以存檔

<img src="http://coding-addict.com/pictures/blender/blender material WIP 13.png" alt="Drawing" style="width: 300px;"/>

小秘訣：__選單的`Replace image`可以重新設定這個物件在 paint mode 時對應到的 paint image__ (也就是說，這個物件進入 paint mode 時，image editor 將會自動顯示出它所對應到的 paint image)。
