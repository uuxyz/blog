---
title: fixed-point combinators
date: 2023-10-15
math: true
---
$$Y=\lambda f.(\lambda x. f (x\ x))(\lambda x. (x\ x))$$
$$Y\ g=g(Y\ g)$$
```scheme
(define Y
  (lambda (f)
    ((lambda (i) (i i))
     (lambda (i)
       (f (lambda (x)
	        (apply (i i) x)))))))
```