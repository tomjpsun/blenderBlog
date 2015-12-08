---
layout: post
title: "360 Panoramic With Blender"
date: 2015-12-09 15:42:22 +0800
comments: true
categories: 
---
準備動作：

安裝 Blend4Web [https://github.com/TriumphLLC/Blend4Web](https://github.com/TriumphLLC/Blend4Web), 到那裡把 source （右上 .zip 按鈕）下載回來, 假設放在 ～/Documents/Blend4Web/ 目錄, 目前他支援 2.76 以後的版本(2.75 以前會出現 warning) 

安裝：

打開 Blender -> User Preferences -> File tab -> Scripts 欄位帶入  ～/Documents/Blend4Web/ , `save user settings` 後, 重新啟動 Blender.

<img src="http://coding-addict.com/pictures/blender/blend4web setup script source.png" alt="Drawing" style="width: 800px;"/>

再次進入 User Preferences -> Add-ons tab 應該要有 Import-Export: Blend4Web, 勾選起來.

<img src="http://coding-addict.com/pictures/blender/blend4web add-ons.png" alt="Drawing" style="width: 700px;"/>

這步驟很重要, Render Mode 要選 Blend4Web.

<img src="http://coding-addict.com/pictures/blender/blend4web select render mode.png" alt="Drawing" style="width: 240px;"/>

做好你的 blender 作品後, 可以用 fast preview 試看一下:

<img src="http://coding-addict.com/pictures/blender/blend4web render tab.png" alt="Drawing" style="width: 400px;"/>

後續 export 動作, 可以到 [Blend4Web Doc](https://www.blend4web.com/en/doc/) 看教學影片.