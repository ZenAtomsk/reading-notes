# Linked Lists

## References

- [Codefellows Github](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)
- [What is a linked list p1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)
- [https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

---
---
## Vocabulary

- **Linked List** - A data structure that contains nodes that links/points to the next node in the list.
- **Singly** - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
- **Doubly** - Doubly refers to there being two references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
- **Node** - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
- **Next** - Each node contains a property called Next. This property contains the reference to the next node.
- **Current** - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

---

### What is a Linked List

 a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

There are two types of Linked List 
  1. Singly 
  2. Doubly

---  

### Traversal

When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.

---

### Big O

The Big O of **time** for **Includes** would be **O(n)**. This is because, at its worse case, the node we are looking for will be the very last node in the linked list. **n represents the number of nodes** in the linked list.

The Big O of **space** for **Includes** would be **O(1)**. This is because there is **no additional space being used** than what is already given to us with the linked list input

---

### Adding a Node

**Adding O(1)** - Order of operations is extremely important when it comes to working with a Linked List. 

---

### Linear data structures

they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.

---

### Memory management

Linked lists don’t need to take up a single block of memory; instead, the memory that they use can be scattered throughout. The fundamental difference between arrays and linked lists is that arrays are static data structures, while linked lists are dynamic data structures.

---

### Parts of a linked list

A linked list is made up of a series of nodes, which are the elements of the list.

The starting point of the list is a reference to the first node, which is referred to as the **head**

The **end** of the list isn’t a node, but rather a node that **points to null**, or an empty value.

---

### To list or not to list?

a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element