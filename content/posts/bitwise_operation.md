---
title: bitwise operation
date: 2023-11-15
---
# lowbit
```c
x & -x;//extract the rightmost set bit (the least significant bit that is set to 1)
x - (x & (x - 1));//extract the rightmost set bit (the least significant bit that is set to 1)
```

```c
x = x & (x - 1);//clears the lowest (least significant) 1 bit
x = x - (x & -x);//clears the lowest (least significant) 1 bit
((1 << (i - 1)) & x) > 0;//check if the bit at position i is equals 1
x = x | (1 << (i - 1));//set the bit at position to 1
x = x & (~(1 << (i - 1)));//set the bit at position to 0
```

```c
x=-~x;//x++;
x=~-x;//x--;
```

```c
(x & (x-1))==0 && x > 0;//true when x is a power of 2
(x & -x) > 0 && x > 0;//true when x is a power of 2
```

```c
(int)(!!x - (((unsigned)x >> 31) << 1));//sgn
(int)((x>>31) | ((unsigned)-x>>31));//sgn
(((x ^ y) >= 0) && (x != 0) && (y != 0)) || ((x==0) && (y==0))//has same sign
(x ^ (x>>31)) - (x>>31);//abs;
(x&y)+((x^y)>>1);//ave;
```

```c
x^=y;
y^=x;
x^=y;
//swap
```

```c
int calc(int n){
    n |= n>>1;
    n |= n>>2;
    n |= n>>4;
    n |= n>>8;
    n |= n>>16;
    return n+1;
}
//next power of two that is greater than or equal to the given integer

unsigned log2(unsigned n){ 
    double d = (double)n;
    unsigned long long r = *((unsigned long long*)&d); 
    return (r >> 52) - 0x3FF; 
}

int add(int a, int b){
    while(b != 0) {
        int carry = (a & b) << 1;
        a ^= b;
        b = carry;
    }
    return a;
}
```