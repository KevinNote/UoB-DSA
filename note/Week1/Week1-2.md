# Linked Lists/链表

<center>
<span>09/10/2021</span>
<a style="text-decoration:none; color: black;" href="https://github.com/KevinZonda">KevinZonda</a>
</center>

## In Memory

![](img/ll-0.png)
![](img/ll-1.png)

## Comparison

If we store a list of `n` elements as an array (without spare space)or a linked list, what costs will the basic operations of lists have asa function of the number of elements in the list (when the list is seen as an ADT)?

| Situation | Array | Linked List |
| --------- | ----- | ----------- |
| access data by position<br>search for an element | constant<br>linear | linear<br>linear |
insert an entry at the beginning<br>insert an entry at the end<br>insert an entry (on a certain position) | linear<br>linear<br>linear | constant<br>linear*<br>linear |
| delete first entry | linear | constant |
| delete entry `i` | linear | linear |
| concatenate two lists | linear | linear* |

\* means could be improved to constant time if we modified.

## Modifications

### Pointer to the last node

Linked list with a pointer to the last node:

![](img/ll-m0.png)

- Fast `insert_end`
- Slow `delete_end`

### Doubly Linked List

![](img/ll-m1.png)

### Circular Singly Linked List

![](img/ll-m2.png)

### Circular Doubly Linked List

![](img/ll-m3.png)