---
layout: post
title: "Perspective Matrix"
date: 2016-01-04 10:11:26 +0800
comments: true
categories: 3d graphic math
---
本篇要來探討 perspective matrix 是如何形成的。
參考文件 :

[http://www.songho.ca/opengl/gl_projectionmatrix.html](http://www.songho.ca/opengl/gl_projectionmatrix.html)

<!--More-->

名詞解釋：

__NDC__: Normalized Device Coordinates － 所有維度都是在 [-1...1] 的範圍內的座標系統。
__Perspective Frustum__: 

e: original point

c: point on clip plane

n: point on NDC space

依據上圖得知：

\begin{align}
x_n = n\cdot\frac{x_e}{-z_e}
\cr
\cr
y_n = n\cdot\frac{y_e}{-z_e}
\end{align}

對於 frustum 內的任何一點 e 都有：

\begin{align}
\begin{bmatrix} x_c \cr y_c \cr z_c \cr w_c \end{bmatrix} ＝ M_{projection} \cdot \begin{bmatrix} x_e \cr y_e \cr z_e \cr w_e \end{bmatrix}
\end{align}

我們就是要找出這個式子的 projection matrix:





轉換到 NDC 即：
\begin{align}
\begin{bmatrix} x_n \cr y_n \cr z_n \end{bmatrix} = \begin{bmatrix} \frac {x_c}{w_c} \cr \frac {y_c}{w_c} \cr \frac {z_c}{w_c} \end{bmatrix}
\end{align}

注意： 支援 OpenGL 的硬體會幫我們做這個除法（i.e. 齊次座標 轉 NDC）

因此，我們要湊出令 \begin{align} w_c = -z_e \end{align} 的投影結果，projection matrix 的第四列必須為：

\begin{align}
\begin{bmatrix} x_c \cr y_c \cr z_c \cr w_c \end{bmatrix} ＝ \begin{bmatrix} \cdot &\cdot & \cdot & \cdot \cr \cdot &\cdot & \cdot & \cdot \cr \cdot &\cdot & \cdot & \cdot \cr 0 & 0 & -1 & 0 \cr \end{bmatrix} \cdot \begin{bmatrix} x_e \cr y_e \cr z_e \cr w_e \end{bmatrix}
\end{align}


