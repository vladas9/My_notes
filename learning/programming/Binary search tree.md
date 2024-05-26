---
Date: 2024-05-17
tags:
  - programming
---
# Definition
A <mark style="background: #BBFABBA6;">Binary Search Tree</mark> is a data structure used in computer science for organizing and storing data in a sorted manner. Each node in a <mark style="background: #BBFABBA6;">Binary Search Tree</mark> has at most two children, a **left** child and a **right** child, with the **left** child containing values less than the parent node and the **right** child containing values greater than the **parent node**. This hierarchical structure allows for efficient **searching, insertion,** and **deletion** operations on the data stored in the tree. operations on the data stored in the tree.
![[Pasted image 20240517232159.png]]
## How to Insert a value in a Binary Search Tree:

A new key is always inserted at the leaf by maintaining the property of the binary search tree. We start searching for a key from the root until we hit a leaf node. Once a leaf node is found, the new node is added as a child of the leaf node. The below steps are followed while we try to insert a node into a binary search tree:

- Check the value to be inserted (say **X**) with the value of the current node (say **val**) we are in:
    - If **X** is less than **val** move to the left subtree.
    - Otherwise, move to the right subtree.
- Once the leaf node is reached, insert **X** to its right or left based on the relation between **X** and the leaf node’s value.

# Types of binary tree
- [[AVL tree]]



## References 
1. https://www.geeksforgeeks.org/binary-search-tree-data-structure/
2. https://www.geeksforgeeks.org/insertion-in-binary-search-tree/