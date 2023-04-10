# Linked-lists

A linked list is a linear data structure that includes a series of connected nodes. Here, each node stores the data and the address of the next node. For example,

![Screenshot 2023-04-11 at 2 58 01 AM](https://user-images.githubusercontent.com/91966167/231002470-10160043-8dbd-4dde-b60e-45f4df115b54.png)

You have to start somewhere, so we give the address of the first node a special name called HEAD. Also, the last node in the linked list can be identified because its next portion points to NULL.

Linked lists can be of multiple types: singly, doubly, and circular linked list. 

## Singly Linked List

It is the most common. Each node has data and a pointer to the next node.

![Screenshot 2023-04-11 at 2 59 15 AM](https://user-images.githubusercontent.com/91966167/231002653-349c334d-4193-433c-a080-7d29cb30d526.png)

Node is represented as:

```
struct node {
    int data;
    struct node *next;
}
```

A three-member singly linked list can be created as:

```
/* Initialize nodes */
struct node *head;
struct node *one = NULL;
struct node *two = NULL;
struct node *three = NULL;

/* Allocate memory */
one = malloc(sizeof(struct node));
two = malloc(sizeof(struct node));
three = malloc(sizeof(struct node));

/* Assign data values */
one->data = 1;
two->data = 2;
three->data = 3;

/* Connect nodes */
one->next = two;
two->next = three;
three->next = NULL;

/* Save address of first node in head */
head = one;
```

## Doubly Linked List
We add a pointer to the previous node in a doubly-linked list. Thus, we can go in either direction: forward or backward.

![Screenshot 2023-04-11 at 3 00 29 AM](https://user-images.githubusercontent.com/91966167/231002852-7ef3bced-d76c-4c38-bbfb-cc0a91a56133.png)

A node is represented as

```
struct node {
    int data;
    struct node *next;
    struct node *prev;
}
```
A three-member doubly linked list can be created as

```
/* Initialize nodes */
struct node *head;
struct node *one = NULL;
struct node *two = NULL;
struct node *three = NULL;

/* Allocate memory */
one = malloc(sizeof(struct node));
two = malloc(sizeof(struct node));
three = malloc(sizeof(struct node));

/* Assign data values */
one->data = 1;
two->data = 2;
three->data = 3;

/* Connect nodes */
one->next = two;
one->prev = NULL;

two->next = three;
two->prev = one;

three->next = NULL;
three->prev = two;

/* Save address of first node in head */
head = one;
```
## Circular Linked List
A circular linked list is a variation of a linked list in which the last element is linked to the first element. This forms a circular loop.

![Screenshot 2023-04-11 at 3 01 42 AM](https://user-images.githubusercontent.com/91966167/231003021-abf50375-5529-4f22-85f5-c32bda15125c.png)

A circular linked list can be either singly linked or doubly linked.

for singly linked list, next pointer of last item points to the first item
In the doubly linked list, prev pointer of the first item points to the last item as well.
A three-member circular singly linked list can be created as:

```
/* Initialize nodes */
struct node *head;
struct node *one = NULL;
struct node *two = NULL;
struct node *three = NULL;

/* Allocate memory */
one = malloc(sizeof(struct node));
two = malloc(sizeof(struct node));
three = malloc(sizeof(struct node));

/* Assign data values */
one->data = 1;
two->data = 2;
three->data = 3;

/* Connect nodes */
one->next = two;
two->next = three;
three->next = one;

/* Save address of first node in head */
head = one;
```

**Outputs-**

Singly linked lists- 

![Screenshot 2023-04-11 at 3 07 45 AM](https://user-images.githubusercontent.com/91966167/231004130-67793beb-3204-4b93-adac-b07f4645f39a.png)




