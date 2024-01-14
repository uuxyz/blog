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
$$\left(f^g\right)^\prime=f^g(g^\prime\ln f+\frac{f^\prime g}{f})$$
### inverse function rule
$${\left(f^{-1}\right)}^\prime=\frac{1}{f^\prime\circ f^{-1}}$$
$$f^\prime=\frac{1}{{\left(f^{-1}\right)}^\prime\circ f}$$
### chain rule
$$(f \circ g \circ h)^\prime=(f^\prime \circ g \circ h)(g^\prime \circ h)h^\prime$$
## trigonometric functions
| function | define | derivative |
| :--: | :--: | :--: |
| $\sin x$ | $y/r$ | $\cos x$ |
| $\cos x$ | $x/r$ | $-\sin x$ |
| $\tan x$ | $y/x$ | $\sec^2 x$ |
| $\cot x$ | $x/y$ | $-\csc^2 x$ |
| $\sec x$ | $r/x$ | $\sec x\tan x$ |
| $\csc x$ | $r/y$ | $-\csc x\cot x$ |
## inverse trigonometric functions

| function | derivative |
| :--: | :--: |
| $\arcsin x$ | $\frac{1}{\sqrt{1-x^2}}$ |
| $\arccos x$ | $-\frac{1}{\sqrt{1-x^2}}$ |
| $\arctan x$ | $\frac{1}{x^2+1}$ |
| $\operatorname{arccot}x$ | $-\frac{1}{x^2+1}$ |
| $\operatorname{arcsec}x$ | $\frac{1}{\vert x\vert\sqrt{x^2-1}}$ |
| $\operatorname{arccsc}x$ | $-\frac{1}{\vert x\vert\sqrt{x^2-1}}$ |
## hyperbolic functions
| function | define | derivative |
| :--: | :--: | ---- |
| $\sinh x$ | $\frac{e^x-e^{-x}}{2}$ | $\cosh x$ |
| $\cosh x$ | $\frac{e^x+e^{-x}}{2}$ | $\sinh x$ |
| $\tanh x$ | $\frac{\sinh x}{\cosh x}$ | $\operatorname{sech}^2 x$ |
| $\coth x$ | $\frac{\cosh x}{\sinh x}$ | $-\operatorname{csch}^2 x$ |
| $\operatorname{sech} x$ | $\frac{1}{\cosh x}$ | $-\operatorname{sech} x\tanh x$ |
| $\operatorname{csch} x$ | $\frac{1}{\sinh x}$ | $-\operatorname{csch} x\operatorname{coth} x$ |
## inverse hyperbolic functions

| function | define |
| ---- | ---- |
| $\operatorname{arsinh} x$ | $\ln\left(x+\sqrt{x^2+1}\right)$ |
| $\operatorname{arcosh} x$ | $\ln\left(x+\sqrt{x^2-1}\right)$ |
| $\operatorname{artanh} x$ | $\frac{1}{2}\ln\left(\frac{1+x}{1-x}\right)$ |
| $\operatorname{arcoth} x$ | $\frac{1}{2}\ln\left(\frac{x+1}{x-1}\right)$ |
| $\operatorname{arsech} x$ | $\ln\left(\frac{1}{x}+\sqrt{\frac{1}{x^2}-1}\right)=\ln\left(\frac{1+\sqrt{1-x^2}}{x}\right)$ |
| $\operatorname{arcsch} x$ | $\ln\left(\frac{1}{x}+\sqrt{\frac{1}{x^2}+1}\right)$ |

## logarithmic differentiation
$$f(x)=g(x)h(x)\to\frac{f^\prime(x)}{f(x)}=\frac{g^\prime(x)}{g(x)}+\frac{h^\prime(x)}{h(x)}$$

$$f(x)=\frac{g(x)}{h(x)}\to\frac{f^\prime(x)}{f(x)}=\frac{g^\prime(x)}{g(x)}-\frac{h^\prime(x)}{h(x)}$$

