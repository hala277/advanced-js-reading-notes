# Linked List

### I decided to talk about how linked list data structure works?

*So linked list, like an array, is a representation of a list of values, but each item in the list is made up of a single object with two properties:*

1. value attribute contained within the object(it could be string, number, boolean, object ...).
2. next, its  point to the next object

*a linked list has two pointers the first one refers first value `head`, and the last value refers to the `tail`.*

*While a linked list resembles an array, it is slower because it does not save the index of its contents, making random access to a given index impossible without traversing the full linked list from head to tail.*

**a linked list has three known types:**
1. singly linked list, which means each node has only the "next" pointer.
2. Doubly linked list, which means each node has next and previous pointer.
3. Circular linked list, which means the tail node points to the head node, creating a circle, also the Circular linked list can be singly or doubly linked list.

**linked list big O :**
1. access elements: O(n)
2. search: O(n)
3. insertion: O(1)
4. deletion: O(1)