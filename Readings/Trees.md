# Trees

### Reading List:

##### [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

---

### Trees

#### Common Terminology
* Node - A node is the individual item/data that makes up the data structure
* Root - The root is the first/top Node in the tree
* Left Child - The node that is positioned to the left of a root or node
* Right Child - The node that is positioned to the right of a root or node
* Edge - The edge in a tree is the link between a parent and child node
* Leaf - A leaf is a node that does not contain any children
* Height - The height of a tree is determined by the number of edges from the root to the bottommost node

#### Traversals
* Depth First
* Breadth First

#### Depth First

* Depth first traversal is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the root. 

	* Pre-order: `root >> left >> right`
	* In-order: `left >> root >> right`
	* Post-order: `left >> right >> root`

#### Breadth First

* Breadth first traversal iterates through the tree by going through each level of the tree node-by-node. 

#### Binary Trees

* Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).

* There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows. 

* Adding a node: 
	* Because there are no structural rules for where nodes are “supposed to go” in a binary tree, it really doesn’t matter where a new node gets placed.
	* One strategy for adding a new node to a binary tree is to fill all “child” spots from the top down. To do so, we would leverage the use of breadth first traversal. During the traversal, we find the first node that does not have 2 child nodes, and insert the new node as a child. We fill the child slots from left to right.
	* To have a node placed in a specific location, you need to reference both the new node to create, and the parent node upon which the child is attached to.

* Big O:

	* Inserting a new node is O(n)
	* Searching for a specific node is O(n)
	* Worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.

#### Binary Search Trees

* A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.

* Searching a BST:
	* Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

* Big O:

	* Insertion and search operations is O(h), or O(height).
	* In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.
	* The Big O space complexity of a BST search would be O(1)
