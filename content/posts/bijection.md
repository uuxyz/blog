---
title: bijection
date: 2023-11-30
math: true
---

# N and Q
```scheme
(define (f n)
  (cond ((= n 1) 1)
        ((even? n) (f (/ n 2)))
        (else (+ (f (/ (- n 1) 2))
                 (f (/ (+ n 1) 2))))))
(define (n_to_q x)
  (/ (f x) (f (+ x 1))))

(define (q_to_n q)
  (cond ((= q 1) 1)
        ((< q 1) (* 2 (q_to_n (/ q (- 1 q)))))
        (else (+ (* 2 (q_to_n (- q 1))) 1))))
```