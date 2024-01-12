---
title: coordinate system
date: 2023-12-08
math: true
---
# 2d
## cartesian coordinate
$$x=r\cos\varphi$$
$$y=r\sin\varphi$$
## polar coordinate
$$r=\sqrt{x^2+y^2}=\operatorname{hypot}(x,y)$$
$$\varphi=\operatorname{atan2}(y,x)$$

# 3d
## cartesian coordinate
$$x=r\sin\theta\cos\varphi$$
$$y=r\sin\theta\sin\varphi$$
$$z=r\cos\varphi$$

## spherical coordinate
$$r=\sqrt{x^2+y^2+z^2}$$
$$\theta=\arccos\frac{z}{r}$$
$$\varphi=\operatorname{atan2}(y,x)$$