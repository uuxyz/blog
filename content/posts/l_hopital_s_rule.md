---
title: L'Hôpital's rule
date: 2023-12-06
math: true
tags:
  - math
---
1. f and g which are differentiable
2. $\displaystyle\lim_{x\to c}f(x)=\lim_{x\to c}g(x)=0\ {\rm or} \pm\infty$
3. $g^\prime(x)\neq 0$
4. $\displaystyle\lim_{x\to c}\frac{f^\prime(x)}{g^\prime(x)}\ {\rm exists}$
$$\lim_{x\to c}\frac{f(x)}{g(x)}=\lim_{x\to c}\frac{f^\prime(x)}{g^\prime(x)}$$

|indeterminate|form|conditions|transformation|
|---|---|---|---|
|$\frac{0}{0}$|$\frac{f(x)}{g(x)}$|$\displaystyle\lim_{x\to c}f(x)=0,\ \lim_{x\to c}g(x)=0$|---|
|$\frac{\infty}{\infty}$|$\frac{f(x)}{g(x)}$|$\displaystyle\lim_{x\to c}f(x)=\infty,\ \lim_{x\to c}g(x)=\infty$|$\displaystyle\lim_{x\to c}\frac{1/g(x)}{1/f(x)}$|
|$0\cdot\infty$|$f(x)g(x)$|$\displaystyle\lim_{x\to c}f(x)=0,\ \lim_{x\to c}g(x)=\infty$|$\displaystyle\lim_{x\to c}\frac{f(x)}{1/g(x)}$|
|$\infty-\infty$|$f(x)-g(x)$|$\displaystyle\lim_{x\to c}f(x)=\infty,\ \lim_{x\to c}g(x)=\infty$|$\displaystyle\lim_{x\to c}\frac{1/g(x)-1/f(x)}{1/(f(x)g(x))}$|
|$0^0$|$f(x)^{g(x)}$|$\displaystyle\lim_{x\to c}f(x)=0^+,\ \lim_{x\to c}g(x)=0$|$\displaystyle\exp\lim_{x\to c}\frac{g(x)}{1/\ln f(x)}$|
|$1^\infty$|$f(x)^{g(x)}$|$\displaystyle\lim_{x\to c}f(x)=1,\ \lim_{x\to c}g(x)=\infty$|$\displaystyle\exp\lim_{x\to c}\frac{\ln f(x)}{1/g(x)}$|
|$\infty^0$|$f(x)^{g(x)}$|$\displaystyle\lim_{x\to c}f(x)=\infty,\ \lim_{x\to c}g(x)=0$|$\displaystyle\exp\lim_{x\to c}\frac{g(x)}{1/\ln f(x)}$|
