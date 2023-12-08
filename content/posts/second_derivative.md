---
title: second derivative
date: 2023-09-23
math: true
---
$$\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{\mathrm{d} y}{\mathrm{d}x}\right)=\frac{\mathrm{d}^2 y}{\mathrm{d}x^2}$$

$$g(x)=\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\mathrm{d}f(x)}{\mathrm{d}x}=\lim_{\varepsilon\to0}\frac{f(x+\varepsilon)-f(x)}{x+\varepsilon-x}$$

$$=\lim_{\varepsilon\to0}\frac{f(x+\varepsilon)-f(x)}{\varepsilon}$$

$$
\begin{equation}
\begin{aligned}
\frac{\mathrm{d}g(x)}{\mathrm{d}x}&=\frac{g(x+\varepsilon)-g(x)}{\varepsilon}\newline
&=\frac{\frac{f((x+\varepsilon)+\varepsilon)-f(x+\varepsilon)}{\varepsilon}-\frac{f(x+\varepsilon)-f(x)}{\varepsilon}}{\varepsilon}\newline
&=\frac{[f((x+\varepsilon)+\varepsilon)-f(x+\varepsilon)]-[f(x+\varepsilon)-f(x)]}{\varepsilon^2}\newline
&=\frac{\mathrm{d}f(x+\varepsilon)-\mathrm{d}f(x)}{\varepsilon^2}\newline
&=\frac{\mathrm{d}(\mathrm{d}f(x))}{\varepsilon^2}\newline
&=\frac{\mathrm{d}^2 f(x)}{(\mathrm{d}x)^2}
\end{aligned}
\end{equation}
$$

```scheme
(define (square x) (* x x))
(define (d f dx)
  (lambda (x)
    (/ (- (f (+ x dx)) (f x)) dx)))
((d square 0.0001) 2) ; == 4
((d (d square 0.0001) 0.0001) 2); == 2
```