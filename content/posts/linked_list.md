---
title: linked list
date: 2023-10-11
---
Write a linked list in C:
```c
typedef struct node {
  int val;
  struct node *ptr;
} node_t;

node_t *xor (node_t a, node_t b){
  return ((int)&a ^ (int)&b);
}

node_t a,b,c;
a.val=0;
b.val=1;
c.val=2;

a.ptr = &b ^ &c;
b.ptr = &a ^ &c;
c.ptr = &a ^ &b;

void push(int i, node_t *p) {
  node_t *node = new node;
  node->val = i;
  node->nxt = p->nxt;
  p->nxt = node;
}
```
