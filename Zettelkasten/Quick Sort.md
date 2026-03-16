202403230200
# Quick Sort

## Notes

A recursive sorting algorithm that utilizes a pivot that represents where a list should be split and in place swapping of elements

The basic structure of quicksort is:
```c
Algo QuickSort(array A, int low, int high){
	if(low < high){
		int pivot = Partition(A, low, high);
		QuickSort(A, low, pivot);
		QuickSort(A, pivot+1, high);
	}
}
```

The main part of utilizing quick sort is to get the pivot point by swapping elements until that pivot point has all greater values in front of it and lesser values behind it

Structure of Partition:
```c
Algo Partition(array A, int low, int high){
	int pivot = A[low];
	int i = low;
	int j = high+1;

	while(i < j){
		do{
			i++;
		}while(A[i] <= pivot);
		do{
			j--;
		}while(A[j] > pivot);
		if(i < j){
			swap(A[i], A[j]);
		}
	}
	swap(A[low], A[j]);
	return j;
}
```

As shown the partition does the heavy lifting of incrementing the left pointer while decrementing the right pointer and swaps elements to their respective place. Then it returns the pivot index to recursively call quicksort again but with a smaller sub list and deriving another pivot.

Since quicksort splits the initial list into sub lists each call and then that sub list is traversed for what is assumed n times if the split is done in the middle the time taken will be $nlogn$ which is best case scenario.

For the worst case scenario if each partition is done on the initial pivot i.e. the list is either already sorted or only 1 element is not sorted then partitions will happen n -k times where k represents the number of partitions that has happened. This creates an arithmetic progression which is equal to $\frac{n(n+1)}{2}$ which evaluates to in asymptotic notation $O(n^2)$.

To help mitigate the chance of having a worst case scenario we can either pick a random element or the middle element as pivot.

The space complexity of quicksort is from $logn$ to $n$ since the algorithm is in place but utilizes the stack for the recursive calls which will be the height of the tracing tree which a tree has a minimum height of $logn$ and a max height of $n$.


---
## Links

- [[Algorithm]]
- [[Divide and Conquer Strategy]]
- [[Recurrence Relation]]

---

## Source

- [Bari's Algorithm Playlist 2.8.1](https://youtu.be/7h1s2SojIRw?si=OnDOvsdElEzSrgu8)
- [Bari's Algorithm Playlist 2.8.2](https://youtu.be/-qOVVRIZzao?si=Q6bpjsfH1568sBrf)