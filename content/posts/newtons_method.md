---
title: newton's method
date: 2023-09-24
math: true
---
Newton's method can be used to find the roots of the equation $f(x)=0$. It works by taking a tangent line at any point, and the intersection of the tangent line with the numerical axis is closer to the roots of the equation.

Let r be the root of $f(x)=0$, and choose $x_0$ as the initial approximation of $r$, then we can make the tangent line $L$ to the curve $y=f(x)$ over the point $(x_0,f(x_0))$, we know that the tangent line intersects with the x-axis, and we know that the equation of the tangent line L is $L:y=f(x_0)+f^\prime(x_0)(x-x_0)$ We find its intersection with the x-axis as $x_1=x_0-\frac{f(x_0)}{f^\prime(x_0)}$. We make a slash at $(x_1,f(x_1))$ with slope $f^\prime(x_1)$ to find the intersection with the x-axis, and repeat the process until $f(x_n)$ is infinitely close to 0. Where the formula for the nth iteration is:

$$x_{n+1}=x_n+\frac{f(x_n)}{f^\prime(x_n)}$$