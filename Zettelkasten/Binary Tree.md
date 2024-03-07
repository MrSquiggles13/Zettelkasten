202402212135
# Binary Tree

## Notes

A data structure that represents data using nodes that starts with a root node and has at most 2 branches off each node which are called left child and right child

Visual representation
![[Pasted image 20240303031816.png]]

#### Classifications of Binary Trees

**Full**: A full binary tree will have max number of nodes relevant to height. The formula to calculate the number of node needed is; for height $h$ there is $2^h+1$ nodes

**Complete**: A complete binary tree will fill all nodes up to height minus one then all following nodes will be placed left to right. The formula to calculate the max number of nodes is; for height $h$ there is $2^{h+1}-1$ nodes. This can also be proved through an array representation of the binary tree

A full binary tree is also a complete binary tree but a complete binary tree is not always full

#### Array Representation of a Binary Tree

![[Pasted image 20240303025443.png]]

The process the array is populated is like so
If a Node is at index ---> $i$
The left child is at ---> $2i$
The right child is at ---> $2i+1$
And the parent is at ---> $\lfloor i/2 \rfloor$

The last example in the image above shows that if a tree is at a certain height and there are child nodes that do not exist at that height then to leave them blank in the given index of the array.
Binary trees converted to an array visually can be converted going to each node from top to bottom, left to right.

Using the array representation it can be determined if a binary tree is complete if there are no gaps or empty space between any elements in the array

---
## Links

- [[Data Structure]]

---

## Source

- 