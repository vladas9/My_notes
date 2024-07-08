---
Date: 2024-06-28
tags:
  - programming
  - data_structure
---
# Double linked lists

>[!Definition]
>A double linked list is a special type of [[Linked list]] in which each node contains a pointer to the previous as well as the next node in the structure 

## Main characteristics on the double linked list
- ***Dynamic size:*** The size the [DLL](#^52352b) can be changed dynamically, nodes can be added or removed as needed.
- ***Two-way navigation:*** Due to the structure of this kind of linked lists the two-pointers approach allows the navigation both forward and backboard.
- ***Memory overhead:*** Each node contains two pointers instead of one in the [[Single linked list]], so it requires additional space to store the data.
## Application of double linked list 

- ***Implementing a Hash Table:*** A double linked list can be used to implement a hash table
>[!hint] 
>### How it works
>#### General structure
> Will be created an array of pointer to specific elements in the double linked list.
> Table of pointers:
> ```py
> table = [None] * size
> ```
> [DLL](#^52352b) structure:
> ```py
> self.key = key
> self.value = value
> self.prev = None
> self.next = None
> ```
> #### Insertion
> Is computed the index in hash map based on the key.
> 1. if the index is empty, create a new linked list with new node
> 2. if the index is not empty, traverse the list to check if the key exists (update if found) or add the new node at the end
- ***Dynamic memory allocation:*** In system programming double linked lists can be used for dynamic memory allocation, where memory blocks are allocated and deallocated as needed.
- ***Reversing a list:*** A double linked list can be used to easily reverse a list by simply swapping the next and prev pointers
## Advantages of [DLL](#^52352b)
- ***Two-way navigation***
- ***Efficient insertion and deletion:*** Due to it two pointer structure it is easy to insert and delete elements in this kind on [LL](#^c68d2c) in any point of it.
	(Example of insertion)
	- **Beginning**
		Adjust the `next` pointer of the new node to point to the current head and update the head `prev` pointer to point to the new node
	- **End**
		Adjust the `prev` pointer of the new node to point to the tail and update the tail `next` to point to the new node
	- Middle
		To insert in the middle is needed to update the `next` and `prev` pointers of surrounding nodes
- ***Versatility:*** [DLL](#^52352b) can be used to implement a wide range of different data structures and algorithms.
## Disadvantages of [DLL](#^52352b)
- ***Memory overhead***
- ***Slower access time:*** Accessing an specific element in a [DLL](#^52352b) can be slower than in an array, because is needed to traverse several pointers in the list to find it.
- ***Pointer manipulation:*** [DLL](#^52352b) requires some pointer manipulations, so the code can result to be more complex and more potential bugs




# Used abbreviations
1. LL - Linked list^c68d2c
2. DLL - Double linked list ^52352b

# References 
1. https://www.geeksforgeeks.org/doubly-linked-list-meaning-in-dsa/?ref=lbp