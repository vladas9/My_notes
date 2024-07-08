---
Date: 2024-06-24
tags:
  - programming
  - data_structure
---
# The basics of Linked lists
***Linked List*** is a linear data structure, in which elements are not stored at a contiguous location, rather they are linked using pointers. Linked List forms a series of connected nodes, where each node stores the data and the address of the next node.
![[Singlelinkedlist.png]]
- ***Node Structure:*** A node in a linked list typically consists of two components:  
- ***Data:*** It holds the actual value or data associated with the node. 
- ***Next Pointer:*** It stores the memory address (reference) of the next node in the sequence.  
- ***Head and Tail:*** The linked list is accessed through the head node, which points to the first node in the list. The last node in the list points to NULL or nullptr, indicating the end of the list. This node is known as the tail node.
## Why linked list data structure needed?
- ***Dynamic Data structure:*** The size of memory can be allocated or de-allocated at run time based on the operation insertion or deletion.
- ***Ease of Insertion/Deletion:*** The insertion and deletion of elements are simpler than arrays since no elements need to be shifted after insertion and deletion, Just the address needed to be updated.
- ***Efficient Memory Utilization:** As we know Linked List is a dynamic data structure the size increases or decreases as per the requirement so this avoids the wastage of memory. 
- ***Implementation:*** Various advanced data structures can be implemented using a linked list like a stack, queue, graph, hash maps, etc.
## Type of linked lists
1. [[Single linked list]]
2. [[Double linked list]]
3. [[Circular linked lust]]



## References 
1. https://www.geeksforgeeks.org/what-is-linked-list/?ref=lbp