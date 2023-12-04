---
title: linked list
date: 2023-10-11
---
Write a linked list in C:
```c
#include <stddef.h>
#include <stdio.h>
#include <stdlib.h>

struct list_head {
  struct list_head *next;
  struct list_head *prev;
};

void init_list_head(struct list_head *head) {
  head->next = head;
  head->prev = head;
}

void list_add(struct list_head *head, struct list_head *new_node) {
  new_node->next = head->next;
  new_node->prev = head;
  head->next->prev = new_node;
  head->next = new_node;
}

void list_add_tail(struct list_head *head, struct list_head *new_node) {
  new_node->next = head;
  new_node->prev = head->prev;
  head->prev->next = new_node;
  head->prev = new_node;
}

void list_del(struct list_head *node) {
  node->prev->next = node->next;
  node->next->prev = node->prev;
}

struct student {
  struct list_head list;
  int id;
  int yy;
  int mm;
  int dd;
};

void printList(struct list_head *head) {
  struct list_head *current = head->next;
  while (current != head) {

    struct student *studentNode =
        (struct student *)((char *)current - offsetof(struct student, list));
    printf("ID: %d, Date: %d-%d-%d\n", studentNode->id, studentNode->yy,
           studentNode->mm, studentNode->dd);

    current = current->next;
  }
}

struct student *findNodeByID(struct list_head *head, int targetID) {
  struct list_head *current = head->next;
  while (current != head) {
    struct student *studentNode =
        (struct student *)((char *)current - offsetof(struct student, list));
    if (studentNode->id == targetID) {
      return studentNode;
    }
    current = current->next;
  }
  return NULL;
}

int main() {
  struct list_head myList;
  init_list_head(&myList);

  struct student lihua = {.list = {&lihua.list, &lihua.list},
                          .id = 1,
                          .yy = 2023,
                          .mm = 1,
                          .dd = 1};
  struct student zhangsan = {.list = {&zhangsan.list, &zhangsan.list},
                             .id = 2,
                             .yy = 2023,
                             .mm = 1,
                             .dd = 1};
  struct student wangwu = {.list = {&wangwu.list, &wangwu.list},
                           .id = 3,
                           .yy = 2023,
                           .mm = 1,
                           .dd = 1};

  list_add_tail(&myList, &lihua.list);
  list_add_tail(&myList, &zhangsan.list);
  list_add(&myList, &wangwu.list);

  printf("Linked List:\n");
  printList(&myList);

  list_del(&zhangsan.list);

  printf("\nLinked List after removal:\n");
  printList(&myList);

  int targetID = 3;
  struct student *foundNode = findNodeByID(&myList, targetID);
  if (foundNode != NULL) {
    printf("\nFound node with ID %d: Date %d-%d-%d\n", targetID, foundNode->yy,
           foundNode->mm, foundNode->dd);
  } else {
    printf("\nNode with ID %d not found\n", targetID);
  }

  return 0;
}
```

```c
// XOR Linked list
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