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
It can use to multiply two polynomial in Octave.
```matlab
a = [1 2 3];
b = [4 5 6];
la = length(a);
lb = length(b);
ifft(fft(a,la+lb-1).*fft(b,la+lb-1));
ans = 4    13    28    27    18
```
This shows \\((1+2x+3x^2)(4+5x+6x^2)=(4+13x^1+28x^2+27x^3+18x^4)\\)

And how to use FFT to multiply two big integers?

If let x=10 Then can see it as \\(321 \times 654\\)
And \\(4  + 13 \cdot 10 + 28 \cdot 10^2 + 27\cdot 10^3+18 \cdot 10^4\\) is the result we need.
Reduce every digital to below 10 and write it in the form we familiar.

|0|18|27|28|13|4|
|---|---|---|---|---|---|
|0|18|27|29|3|4|
|0|18|29|9|3|4|
|0|20|9|9|3|4|
|2|0|9|9|3|4|

Then there is the result 209934.

Then let's find out how FFT and IFFT realize.
