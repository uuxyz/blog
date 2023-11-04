---
title: fast fourier transform
date: 2023-10-14
math: true
tags:
  - math
  - algorithm
---
First, let's forget the algorithm of FFT and just use it.
How is it useful?
It can use to multiply two polynomial.
```matlab
a = [1 2 3];
b = [4 5 6];
la = length(a);
lb = length(b);
ifft(fft(a,la+lb-1).*fft(b,la+lb-1));
ans = 4    13    28    27    18
```
This shows $(1x^2+2x+3)(4x^2+5x+6)=(4x^4+13x^3+28x^2+27x^1+18)$

And how to use FFT to multiply two big integers?

If let $x=10$ Then can see it as $123 \times 456$
And $4 \cdot 10^4 + 13 \cdot 10^3 + 28 \cdot 10^2 + 27\cdot 10+18$ is the result we need.
Reduce every digital to below 10 and write it in the form we familiar.

```
4    13    28    27    18
4    13    28    28    8
4    13    30    8     8
4    16    0     8     8
5    6     0     8     8
56088
```
Then there is the result $56088$.

Then let's find out how FFT and IFFT realize.
