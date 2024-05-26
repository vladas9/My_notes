---
Date: 2024-05-17
tags:
  - programming
---
# AVL Tree Data Structure

>[!info]
>An AVL tree defined as a self-balancing Binary Search Tree (BST) where the difference between heights of left and right subtrees for any node cannot be more than one.

The difference between the heights of the left subtree and the right subtree for any node is known as the **balance factor** of the node.

## Why AVL Trees? 

>[!inote]
>Most of the BST operations (e.g., search, max, min, insert, delete.. etc) take **O(h)** time where **h** is the height of the BST. The cost of these operations may become **O(n)** for a **skewed Binary tree**. If we make sure that the height of the tree remains **O(log(n))** after every insertion and deletion, then we can guarantee an upper bound of **O(log(n))** for all these operations. The height of an AVL tree is always **O(log(n))** where **n** is the number of nodes in the tree.



## References 
1. https://www.geeksforgeeks.org/introduction-to-avl-tree/
2. https://www.geeksforgeeks.org/insertion-in-an-avl-tree/ 