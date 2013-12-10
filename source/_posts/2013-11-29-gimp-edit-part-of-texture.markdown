---
layout: post
title: "GIMP edit part of texture"
date: 2013-11-29 14:22
comments: true
categories: GIMP
---
有時候，App 會需要一些動畫，所以從網路上得到的素材，加以處理，就可以得到需要的動畫素材。這裡介紹用 GIMP 做簡單的半透明處理。

例如：我們希望把原始的 wifi.png 圖檔，弄成一系列的 textures. 像這樣：

![result](http://coding-addict.com/pictures/gimp/result.png)

首先依照 [宗大](http://blog.longwin.com.tw/about/) 這篇把背景變成透明：

<http://blog.longwin.com.tw/2013/04/gimp-background-transparent-2013/>

然後開 GIMP 工具箱用「自由選取工具」：

![tool](http://coding-addict.com/pictures/gimp/tool.png)

假設我們要把最長的波變成半透明，選取後令它變成「浮動」圖層：

![selecting](http://coding-addict.com/pictures/gimp/selecting.png)

現在多了一個浮動圖層，把此圖層不透明度調到 33.1（透明度隨個人需要而定，此範例看到的是 33.1）：

![after_select](http://coding-addict.com/pictures/gimp/after_select.png)

接下來合併回去，浮動圖層屬於剛剛分出來的圖層：

![belong_to](http://coding-addict.com/pictures/gimp/belong_to.png)

接著就按滑鼠右鍵，合併圖層：

![merge](http://coding-addict.com/pictures/gimp/merge.png)

到此，簡單的修改即完成！


