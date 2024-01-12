---
title: arithmetic overflow
date: 2023-12-12
math: true
---
Using those code to avoid overflow:
```c
#include <stdint.h>
#include <stdio.h>
const int64_t mod = 0x7fffffffffffffe7LL; // 216289611853439384th prime
const int64_t a01 = 0x7fffffffffffff5bLL;
const int64_t b01 = 0x7ffffffffffffefdLL;
int64_t add64(int64_t a, int64_t b, int64_t m) {
  a %= m;
  b %= m;
  if (m - a < b)
    return a > b ? a - m + b : b - m + a;
  else
    return a + b;
}
int64_t sub64(int64_t a, int64_t b, int64_t m) {
  a %= m;
  b %= m;
  return a - b < 0 ? a - b + m : a - b;
}
int64_t mul64(int64_t a, int64_t b, int64_t m) {
  a %= m, b %= m;
  int64_t res = 0;
  for (; b; b >>= 1) {
    if (b & 1)
      res = add64(res, a, m);
    a = add64(a, a, m);
  }
  return res;
}
int64_t binpow(int64_t a, int64_t b, int64_t m) {
  a %= m;
  int64_t res = 1;
  for (; b; b >>= 1) {
    if (b & 1)
      res = mul64(res, a, m);
    a = mul64(a, a, m);
  }
  return res % m;
}
int64_t div64(int64_t a, int64_t b, int64_t m) {
  return mul64(a, binpow(b, m - 2, m), m);
}
int main() {
  long long a, b, m;
  scanf("%lld%lld%lld", &a, &b, &m);
  printf("%lld\n", add64(a, b, mod));
  printf("%lld\n", sub64(a, b, mod));
  printf("%lld\n", mul64(a, b, mod));
  printf("%lld\n", div64(a, b, mod));
  printf("%lld\n", binpow(a, b, mod));
  return 0;
}
```
