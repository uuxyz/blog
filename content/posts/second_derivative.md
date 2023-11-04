---
title: second derivative
date: 2023-09-23
math: true
---
$$\frac{\mathrm{d}^2 y}{\mathrm{d}x^2}$$

but ask why?

$$\frac{\Delta f(a)}{\Delta x}=\frac{f(a+\Delta x)-f(a)}{\Delta x}$$


$$\left.\lim_{\Delta x\to 0}
\frac{\Delta f(a)}{\Delta x}=\lim_{\Delta x \to 0}\frac{f(a+\Delta x)-f(a)}{\Delta x}=\frac{\mathrm{d} f(a)}{\mathrm{d}x}=\frac{\mathrm{d} y}{\mathrm{d}x}\right|_{x=a}$$

$$\frac{\Delta f(a)}{\Delta x}=g(a)$$

$$\frac{\Delta g(a)}{\Delta x}=\frac{g(a+\Delta)-g(a)}{\Delta x}$$

$$=\frac{\frac{f((a+\Delta x)+\Delta x)-f(a+\Delta x)}{\Delta x}-\frac{f(a+\Delta x)-f(a)}{\Delta x}}{\Delta x}$$

$$=\frac{(f((a+\Delta x)+\Delta x)-f(a+\Delta x))-(f(a+\Delta x)-f(a))}{(\Delta x)^2}$$

$$=\frac{\Delta f(a+\Delta x)-\Delta f(a)}{(\Delta x)^2}$$

$$=\frac{\Delta(\Delta f(a))}{(\Delta x)^2}$$

$$=\frac{\Delta^2 f(a)}{(\Delta x)^2}$$
