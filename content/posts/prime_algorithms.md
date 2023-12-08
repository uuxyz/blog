---
title: prime algorithms
date: 2023-11-18
math: true
---
# sieve
## sieve of eratosthenes
```scheme
(define (sieve n)
  (define (aux u v)
    (let ((p (car v)))
      (if (> (* p p) n)
          (let rev-append
              ((u u)
               (v v))
            (if (null? u)
                v
                (rev-append (cdr u)
                            (cons (car u) v))))
          (aux (cons p u)
               (let wheel
                   ((u '())
                    (v (cdr v))
                    (a (* p p)))
                 (cond
                  ((null? v)
                   (reverse u))
                  ((= (car v) a)
                   (wheel u
                          (cdr v)
                          (+ a p)))
                  ((> (car v) a)
                   (wheel u
                          v
                          (+ a p)))
                  (else (wheel (cons (car v) u)
                               (cdr v)
                               a))))))))
  (aux '(2)
       (let range
           ((v '())
            (k (if (odd? n)
                   n
                   (- n 1))))
         (if (< k 3)
             v
             (range (cons k v)
                    (- k 2))))))
```
## sieve of pritchard
# fermat primality test
# miller-Rabin primality test
# aks test
a number $p$ is prime if and only if all the coefficients of the polynomial expansion of
$$(x-1)^p-(x^p-1)$$ are divisible by p.
# factor
## pollard's Rho algorithm
## elliptic curve factorization
## quadratic sieve and GNFS
