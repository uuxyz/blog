---
title: C Code with magic
date: 2024-02-28
math: true
---
Here I want to list several C code powered by magic.

# fast inverse square root
```c
float Q_rsqrt(float number) {
  long i;
  float x2, y;
  const float threehalfs = 1.5F;
  x2 = number * 0.5F;
  y = number;
  i = *(long *)&y;
  i = 0x5f3759df - (i >> 1);
  y = *(float *)&i;
  y = y * (threehalfs - (x2 * y * y));
  // y = y * (threehalfs - (x2 * y * y));
  return y;
}
```

# integer square root
```c
int isqrt(int n) {
  int x = 1;
  int decreased = 0;
  for (;;) {
    int nx = (x + n / x) >> 1;
    if (x == nx || (nx > x && decreased))
      break;
    decreased = nx < x;
    x = nx;
  }
  return x;
}
```

# is square number or not
```c
int is_square(int n) {
  if (1 << (n & 0x1f) & 0x2030213) {
    int n_sqrt2 = isqrt(n);
    return n_sqrt2 * n_sqrt2 == n;
  } else {
    return 0;
  }
}
```