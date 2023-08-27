---
title: "Linear algebra"
date: 2022-07-03T00:53:04+08:00
draft: true
math: true
---

## Determinant

$$
\begin{vmatrix}
x_1 & y_1 & z_1\\\\ 
x_2 & y_2 & z_2\\\\ 
x_3 & y_3 & z_3
\end{vmatrix}=x_1 y_2 z_3 + x_2 y_3 z_1 + x_3 y_1 z_2 - x_1 y_3 z_2 - x_2 y_1 z_3 - x_3 y_2 z_1
$$

## Area of Triangle

$$S_{\mathrm{triangle}}=\frac{1}{2}
\left|
\begin{vmatrix}
x_0 & x_1 & x_2\\\\ 
y_0 & y_1 & y_2\\\\ 
1 & 1 & 1
\end{vmatrix}\right|$$

## Area of triangle in complex number form

$$S_{\mathrm{triangle}}=\frac{1}{4}
\left|
\begin{vmatrix}
1 & 1 & 1\\\\ 
z_1 & z_2 & z_3\\\\ 
\bar{z_1} & \bar{z_2} & \bar{z_3}
\end{vmatrix}\right|$$

## Volume of Tetrahedron

$$V_{\mathrm{tetrahedron}}=\frac{1}{6}
\left|
\begin{vmatrix}
x_0 & x_1 & x_2 & x_3\\\\ 
y_0 & y_1 & y_2 & y_3\\\\ 
z_0 & z_1 & z_2 & z_3\\\\ 
1 & 1 & 1 & 1
\end{vmatrix}\right|$$

## Two Vector Cross Product

$$\boldsymbol{a}\times\boldsymbol{b}=
\begin{vmatrix}
x_1 & y_1 & z_1\\\\ 
x_2 & y_2 & z_2\\\\ 
\boldsymbol i & \boldsymbol j &  \boldsymbol k
\end{vmatrix}$$

## 5 Points Determine a Gereral Quadratic Curve

$$\begin{vmatrix}
x^2 & xy & y^2 & x & y & 1 \\\\
x_1^2 & x_1 y_1 & y_1^2 & x_1 & y_1 & 1 \\\\
x_2^2 & x_2 y_2 & y_2^2 & x_2 & y_2 & 1 \\\\
x_3^2 & x_3 y_3 & y_3^2 & x_3 & y_3 & 1 \\\\
x_4^2 & x_4 y_4 & y_4^2 & x_4 & y_4 & 1 \\\\
x_5^2 & x_5 y_5 & y_5^2 & x_5 & y_5 & 1 \\\\
\end{vmatrix}
=\begin{bmatrix}
x & y & 1
\end{bmatrix}
\begin{bmatrix}
A & B & D\\\\
B & C & E\\\\
D & E & F
\end{bmatrix}
\begin{bmatrix}
x\\\\
y\\\\
1
\end{bmatrix}
=\begin{bmatrix}
x & y
\end{bmatrix}
\begin{bmatrix}
A & B\\\\
B & C
\end{bmatrix}
\begin{bmatrix}
x\\\\
y
\end{bmatrix}
+\begin{bmatrix}
D & E
\end{bmatrix}
\begin{bmatrix}
x\\\\
y
\end{bmatrix}
+F
=0
$$

$$Ax^2+2Bxy+Cy^2+2Dxz+2Eyz+Fz^2=0$$

$$\Delta = \begin{vmatrix}
A & B & D\\\\
B & C & E\\\\
D & E & F
\end{vmatrix}$$

$$J = \begin{vmatrix}
A & B\\\\
B & C
\end{vmatrix}$$

$$I = a + c$$

$$K=\begin{vmatrix}
A & D\\\\
D & F
\end{vmatrix}+
\begin{vmatrix}
C & E\\\\
E & F
\end{vmatrix}$$

| curve                          | Delta | J  | Delta/I | K  |
|--------------------------------|-------|----|---------|----|
| coincident lines               | 0     | 0  |         | 0  |
| ellipse (imaginary)            | !=0   | >0 | >0      |    |
| ellipse (real)                 | !=0   | >0 | <0      |    |
| hyperbola                      | !=0   | <0 |         |    |
| intersecting lines (imaginary) | 0     | >0 |         |    |
| intersecting lines (real)      | 0     | <0 |         |    |
| parabola                       | !=0   | 0  |         |    |
| parallel lines (imaginary)     | 0     | 0  |         | >0 |
| parallel lines (real)          | 0     | 0  |         | <0 |


## 3 Points Determine a Circle

$$
\begin{vmatrix}
x^2+y^2 & x & y & 1\\\\
x_1^2+y_1^2 & x_1 & y_1 & 1\\\\
x_2^2+y_2^2 & x_2 & y_2 & 1\\\\
x_3^2+y_3^2 & x_3 & y_3 & 1
\end{vmatrix}
=\begin{bmatrix}
x & y & 1
\end{bmatrix}
\begin{bmatrix}
1 & 0 & D\\\\
0 & 1 & E\\\\
D & E & F
\end{bmatrix}
\begin{bmatrix}
x\\\\
y\\\\
1
\end{bmatrix}
=0
$$

## 4 Point Determine a Sphere

$$
\begin{vmatrix}
x^2+y^2+z^2 & x & y & z & 1\\\\
x_1^2+y_1^2+z_1^2 & x_1 & y_1 & z_1 & 1\\\\
x_2^2+y_2^2+z_2^2 & x_2 & y_2 & z_2 & 1\\\\
x_3^2+y_3^2+z_3^2 & x_3 & y_3 & z_3 & 1\\\\
x_4^2+y_4^2+z_4^2 & x_4 & y_4 & z_4 & 1
\end{vmatrix}
=0
$$

## 3 Point Determine a Plane

$$
\begin{vmatrix}
x & y & z&1\\\\
x_1 & y_1 & z_1&1\\\\
x_2 & y_2 & z_2&1\\\\
x_3 & y_3 & z_3&1
\end{vmatrix}
$$

## 2 Point Determine a Line

$$
\begin{vmatrix}
x & y & 1\\\\
x_1 & y_1 & 1\\\\
x_2 & y_2 & 1
\end{vmatrix}
$$
