---
title: mathematics
date: 2023-10-03
math: true
tags:
  - math
---
# (ε, δ)-definition of limit

$$(\forall\varepsilon>0)(\exists \delta > 0)(\forall x \in \mathbb{R})(0<|x-p|<\delta \implies |f(x)-L|<\varepsilon)$$
(for every real ε > 0, there exists a real δ > 0 such that for all real x, 0 < |x − p| < δ implies |f(x) − L| < ε.)

# one-sided limit
$$\lim_{x\to a^+}f(x)=R$$

$$\lim_{x\to a^-}f(x)=L$$
# derivative
## rules for combined functions
### sum rule
$$(f+g)^\prime=f^\prime+g^\prime$$
### product rule
$$(fg)^\prime=f^\prime g+fg^\prime$$
$$(fgh)^\prime=f^\prime gh+fg^\prime h+fgh^\prime$$
### quotient rule
$$\left(\frac{f}{g}\right)^\prime=\frac{f^\prime g-fg^\prime}{g^2}$$
### generalized power rule
$$\left(f^g\right)^\prime=f^g(g^\prime\ln f+\frac{gf^\prime}{f})$$
### inverse function rule
$${\left(f^{-1}\right)}^\prime=\frac{1}{f^\prime\circ f^{-1}}$$
$$f^\prime=\frac{1}{{\left(f^{-1}\right)}^\prime\circ f}$$
### chain rule
$$f(g(h(x)))^\prime=f^\prime(g(h(x)))g^\prime(h(x))h^\prime(x)$$
## trigonometric functions
## logarithmic differentiation
$$f(x)=g(x)h(x)$$
$$\frac{f^\prime(x)}{f(x)}=\frac{g^\prime(x)}{g(x)}+\frac{h^\prime(x)}{h(x)}$$
$$f(x)=\frac{g(x)}{h(x)}$$
$$\frac{f^\prime(x)}{f(x)}=\frac{g^\prime(x)}{g(x)}-\frac{h^\prime(x)}{h(x)}$$