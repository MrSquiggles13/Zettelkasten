202403070153
# Merge Sort

## Notes

The process of taking an array of elements and recursively splitting the array into subarrays and merging (joining of 2 arrays) together so that the end result is a sorted array

The process of merging can be written as such
```C
Algo Merge(vector<int> A, vector<int> B, int m, int n){
	int i = 0;
	int j = 0;
	int k = 0;
	vector<int> C;

	while(i <= m && j <= n){
		if(A[i] < B[j]){
			C[k++] = A[i++];
		} else {
			C[k++] = B[j++];
		}
	}

	for(; i<=m; i++){
		C[k++] = A[i];
	}
	for(; j<=n; j++){
		C[k++] = B[j];
	}
}
```

As can be seen there are pointers to each list to be merged then a third pointer to the list that will become the merged list. Iteration is done and each pointer is incremented based on the condition of which element is smaller. After this initial traversal the lists are checked for if one of them has elements that have not been added and inserts them at the end of the new list.

When multiple lists are merged also known as m-way merge, there are a couple of methods. One is to just set a pointer for each individual list and then traverse through them adding elements to a new list. Another is performing a two way search (like above) on pairs of lists in the set until a final merged list is created. Also another way is to start by merging 2 lists and then subsequently merging each list left in the set to the newly merged list until a final merged list is achieved.

2-way merge sort is a type of merge sort algorithm but the key difference is that 2-way uses iteration while standard merge sort uses recursion.

A visual representation of 2 way merge sort
![[Pasted image 20240321031237.png]]

In this process each element in the initial list is treated as a list itself. Since each one of these "lists" have only 1 element they are technically sorted. Hence they can be merged with each other. Each pass merges 2 lists with each other until there is only one final list and that list will be the initial array but sorted. The time taken for this algorithm is $\Theta(nlogn)$ since the number of passes are dependent of the initial list (n) and how many times it will take to divide in half to reach the final list also each merge takes n traversals through the elements.

A standard merge sort can be implemented as such:
```c
Algo MergeSort(array A, int low, int high){
	if(low < high){
		mid = (low + high) / 2;
		MergeSort(low, mid);
		MergeSort(mid+1, high);
		Merge( A[low,..., mid], A[mid+1,..., high]);
	}
}
```

In which low and high are the indexes of the array being sorted and the terminating statement is if the indexes are of same value or have crossed each other. The Merge function called is the same one defined above. This works the same way as 2-way merge sort but as stated before merge sort is done recursively.

A tracing tree visualization of Merge Sort:
![[Pasted image 20240321045144.png]]

As can be seen each recursive call breaks down the area into smaller parts until it is 1 element  then it is merged. The time taken for Merge Sort is $\Theta(nlogn)$ since it is recursively called log(n) times because of the array being split in half each call and n elements need to be merged iteratively.

Using recursive relation we can also prove the time complexity:
![[Pasted image 20240321052626.png]]

 Pros of Merge Sort:
 1.  Handles large lists
 2. Works on linked list
 3. External sorting i.e. can break up tasks to reduce memory needed for process
 4. Stable i.e. will maintain order of equivalent values
 Cons of Merge Sort
 1. Needs extra memory, sorting is not in place
 2. Less performance for smaller lists compared to other sorting methods
 3. Recursive so the stack memory space needed is $n+logn$

For smaller lists typically less than 15 elements [[Insertion Sort]] or [[Bubble Sort]] is typically used in stead. Both of these are also stable but the former is more suitable for linked lists while the latter is not.


---
## Links

- [[Algorithm]]
- [[Divide and Conquer Strategy]]

---

## Source

- [Bari's Algorithm Playlist 2.7.1](https://youtu.be/6pV2IF0fgKY?si=yL0baV7SFVV4RlYO)
- [Bari's Algorithm Playlist 2.7.2](https://youtu.be/mB5HXBb_HY8?si=Oxaog2OxYscSqhpU)
- [Bari's Algorithm Playlist 2.7.3](https://youtu.be/ak-pz7tS5DE?si=jYwT7o3NNYK17PRG)