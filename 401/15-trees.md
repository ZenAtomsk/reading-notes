# Trees

## Links

[Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

## Vocabulary

- **Node** - A node is the individual item/data that makes up the data structure

- **Root** - The root is the first/top Node in the tree

- **Left Child** - The node that is positioned to the left of a root or node

- **Right Child** - The node that is positioned to the right of a root or node

- **Edge** - The edge in a tree is the link between a parent and child node

- **Leaf** - A leaf is a node that does not contain any children

- **Height** - The height of a tree is determined by the number of edges from the root to the bottommost node

---

## Traversals

There are two categories of traversals when it comes to trees:

1. Depth First 

    - prioritize going through the depth of the tree first. three methods for depth first traversal:

        1. Pre-order: `root >> left >> right`
        2. In-order: `left >> root >> right`
        3. Post-order: `left >> right >> root`

2. Breadth First

    - iterates through the tree by going through each level of the tree node-by-node.

---

## Binary Trees

Trees can have any number of children per node, but Binary Trees restrict the number of children to two



### Adding a node

Because there are no structural rules for where nodes are “supposed to go” in a binary tree

During the traversal, we find the first node that does not have 2 child nodes, and insert the new node as a child. We fill the child slots from left to right.



### Big O

The Big O time complexity for inserting a new node is O(n)

The Big O space complexity for a node insertion using breadth first insertion will be O(w).

---

## Binary Search Trees

nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.

### **Searching a BST**

compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

### Big O

The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h)

The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.
