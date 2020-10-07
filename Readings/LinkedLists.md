# Linked Lists

### Reading List:

##### [Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)
##### [What’s a Linked List, Anyway pt1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)
##### [What’s a Linked List, Anyway pt2](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

---

### Linked Lists

#### Basic Terms

* **Linked List** - A data structure that contains nodes that link/point to the next node in the list.
* **Singly** - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
* **Doubly** - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
* **Node** - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
* **Next** - Each node contains a property called Next. This property contains the reference to the next node.
* **Head** - The Head is a reference type of type Node to the first node in a linked list.
* **Current** - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

#### Traversal

* **Do's** - use a while() loop to continually check that the Next node in the list is not null. The Current will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.
* **Don'ts** - use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing.


#### Adding a Node

* **Beginning** - If we want to add a node at the beginning of a list, we have to replace the current Head of the linked list with the new node, without losing the reference to the next node in the list.

* **Middle** - Adding a node to the middle of a linked list is a bit different than adding to the beginning. This is because we are working with more nodes and must re-allocate to make room for the new node.
