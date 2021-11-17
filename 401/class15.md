# Trees
## Common type of trees:
1.  Binary Trees
2.  Binary Search Trees
3.  K-ary Trees

## Common terminologies trees share:
1. Node: A Tree node is a component which may contain it’s own values, and references to other nodes
2. Root: The root is the node at the beginning of the tree
3. K: A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
4. Left: A reference to one child node, in a binary tree
5. Right: A reference to the other child node, in a binary tree
6. Edge: The edge in a tree is the link between a parent and child node
7. Leaf: A leaf is a node that does not have any children
8. Height: The height of a tree is the number of edges from the root to the furthest leaf

## Tree example
![Sample Tree](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)

## Traversing a Tree
**there are 2 ways to traverse a tree, and by traverse we mean going through the tree and accessing all of it's nodes**
1. depth first
      1. pre-order, root => left => right
      2. in-order, left => root => right
      3. post-order, left => right => root
2. breadth first
      * going through the childs first then moving to the childs' childs **LEVEL BY LEVEL**

## there are two types of trees when it comes to the number of childs for each node
1. binary tree, it's name says it all, 2 childs maximum for each node
2. k-ary tree, a single node can have k number of childs where k > 2

## BigO
The Big O time complexity for inserting a new node is O(n) and O(n) for searching,
the worst case scenario will involve traversing the entire tree. 
The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree (h = log n).
perfect binary tree is each node has exactly 2 childrens, perfect width is 2^(h-1).
