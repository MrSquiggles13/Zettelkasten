202403030236
# Heap

## Notes

Heaps have 2 separate types either a max heap or a min heap
![[Pasted image 20240303035730.png]]

A max heap is a complete binary tree with each node greater than or equal to all of its descendants

A min heap is a complete binary tree with each node less than or equal to all of its descendants

**_Inserting an element into a max heap_**
![[Pasted image 20240303042316.png]]

First the element to be inserted is added as a child node that still satisfies the conditions of being a complete binary tree. Here it is the left child of node 15 since adding the element anywhere else would create gaps in the array representation of the binary tree.
Then the element is compared with its parent node and if the element is larger it is swapped with said parent. This process continues until either the parent node is larger than the inserted element or the inserted element becomes the root node.

The time complexity for inserting an element into a heap is $O(logn)$ since at max it will take the height of the tree to do so. Best case for insertion is $O(1)$

**_Deleting an element from a max heap_**
![[Pasted image 20240303052920.png]]

In order to preserve the structure of a max heap only the root node can be deleted
After the root node is deleted the last element in the tree (bottom right most leaf) replaces the root node.
Then the new root node is compared with its children. If only one child is greater then that child gets swapped with the root. If both children are greater then the child that is the largest of the two is swapped with root.
After a swap a new comparison is made in the same matter and the pattern continues until neither child node is greater or the element being swapped is now a root node

The time complexity for deletion is also $O(logn)$ since it is dependent on the height of the tree

Note that a min heap has almost the same method for insertion and deletion as max heap besides the comparison for swapping nodes is the opposite from one another

---
## Links

- [[Data Structure]]
- [[Binary Tree]]

---

## Source

- [Bari's Algorithm Playlist 2.6.3](https://youtu.be/HqPJF2L5h9U?si=03rUBdf8QtbbDSZ4)