# Breadth First Binary Tree Traversal

### Reading List:

##### [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)
##### [Breaking Down Breadth-First Search](https://medium.com/basecs/breaking-down-breadth-first-search-cebe696709d9)


---

### Binary Tree Breadth First Traversal

#### 

* Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

* We traverse through one entire level of children nodes first, before moving on to traverse through the grandchildren nodes. And we traverse through an entire level of grandchildren nodes before going on to traverse through great-grandchildren nodes.

* **Implementation**: while a Depth-First traversal uses a stack data structure, a Breadth-First traversal uses the queue data structure.

* Using a queue allows us to keep a reference to nodes that we want to come back to, even though we haven’t checked, or visited them yet.

* **Discovered Nodes**: the term for nodes we add to our queue, whose location we know, but we have yet to actually visit.

#### Quick Step Summary:

1. Enqueue Root
2. Dequeue Front
3. Enqueue LC of Front
4. Enqueue RC of Front

#### Pseudocode

``` 
ALGORITHM breadthFirst(root)
// INPUT  <-- root node
// OUTPUT <-- front node of queue to console

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while breadth.peek()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)
```

#### Big O

| Time | Space |
| :-----------: | :-----------: |
| O(n) | O(w) |

* Time Complexity

Since we visit each node in a breadth-first traversal once, the time it will take to read every node depends on the number of nodes in the tree.

* Space Complexity

The space complexity of a breadth-first traversal is O(w) where w equals the width of the tree.  In the worst case situation, we could enqueue all the nodes in a tree if they are all children of one another.