---
title: "Triangle"
date: 2022-10-22T23:27:01+08:00
draft: false
math: true
---

## Incenter

$$\left(\frac{ax_1+bx_2+cx_3}{a+b+c},\frac{ay_1+by_2+cy_3}{a+b+c}\right)$$

## Centroid

$$\left(\frac{x_1+x_2+x_3}{3},\frac{y_1+y_2+y_3}{3}\right)$$

## Circumcenter

$$\left(\frac{\begin{vmatrix}
x_1^2+y_1^2 & y_1 & 1\\\\
x_2^2+y_2^2 & y_2 & 1\\\\
x_3^2+y_3^2 & y_3 & 1
\end{vmatrix}}{2\begin{vmatrix}
x_1 & y_1 & 1\\\\
x_2 & y_2 & 1\\\\
x_3 & y_3 & 1
\end{vmatrix}},\frac{\begin{vmatrix}
x_1 & x_1^2+y_1^2 & 1\\\\
x_2 & x_2^2+y_2^2 & 1\\\\
x_3 & x_3^2+y_3^2 & 1
\end{vmatrix}}{2\begin{vmatrix}
x_1 & y_1 & 1\\\\
x_2 & y_2 & 1\\\\
x_3 & y_3 & 1
\end{vmatrix}}\right)$$

## Orthocenter

$$\left(\frac{\begin{vmatrix}
x_2x_3+y_2y_3 & 1 & y_1\\\\
x_3x_1+y_3y_1 & 1 & y_2\\\\
x_1x_2+y_1y_2 & 1 & y_3
\end{vmatrix}}{\begin{vmatrix}
x_1 & y_1 & 1\\\\
x_2 & y_2 & 1\\\\
x_3 & y_3 & 1
\end{vmatrix}},\frac{\begin{vmatrix}
x_2x_3+y_2y_3 & x_1 & 1\\\\
x_3x_1+y_3y_1 & x_2 & 1\\\\
x_1x_2+y_1y_2 & x_3 & 1
\end{vmatrix}}{\begin{vmatrix}
x_1 & y_1 & 1\\\\
x_2 & y_2 & 1\\\\
x_3 & y_3 & 1
\end{vmatrix}}\right)$$

## Nine-point center

$$\left(\frac{\begin{vmatrix}
x_1^2+y_1^2-2(x_2x_3+y_2y_3) & y_1 & 1\\\\
x_2^2+y_2^2-2(x_3x_1+y_3y_1) & y_2 & 1\\\\
x_3^2+y_3^2-2(x_1x_2+y_1y_2) & y_3 & 1
\end{vmatrix}}{4\begin{vmatrix}
x_1 & y_1 & 1\\\\
x_2 & y_2 & 1\\\\
x_3 & y_3 & 1
\end{vmatrix}},\frac{\begin{vmatrix}
x_1 & x_1^2+y_1^2-2(x_2x_3+y_2y_3) & 1\\\\
x_2 & x_2^2+y_2^2-2(x_3x_1+y_3y_1) & 1\\\\
x_3 & x_3^2+y_3^2-2(x_1x_2+y_1y_2) & 1
\end{vmatrix}}{4\begin{vmatrix}
x_1 & y_1 & 1\\\\
x_2 & y_2 & 1\\\\
x_3 & y_3 & 1
\end{vmatrix}}\right)$$
