---
title: bijection
date: 2023-11-30
math: true
---

# $\mathbb{N}\to\mathbb{Q}$
```scheme
(define (n_to_q x)
  (define (Q n)
    (cond ((= n 1) 1)
          ((even? n) (Q (/ n 2)))
          (else (+ (Q (/ (- n 1) 2))
                   (Q (/ (+ n 1) 2))))))
  (/ (Q x) (Q (+ x 1))))

(define (q_to_n q)
  (cond ((= q 1) 1)
        ((< q 1) (* 2 (q_to_n (/ q (- 1 q)))))
        (else (+ (* 2 (q_to_n (- q 1))) 1))))
```