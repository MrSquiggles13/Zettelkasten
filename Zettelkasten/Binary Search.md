202403020452
# Binary Search

## Notes

An algorithmic method for finding a value inside a _sorted_ list


![[binary-and-linear-search-animations.gif]]

Binary search starts with 2 pointers one pointing to the first index of the list and the second to the last index called the low and high pointers respectfully

Then a mid point is determined from the formula $mid=\frac{low+high}{2}$ which is used to check against the value to search for.
If the value is less than the mid point $key \lt mid$ then the new high is set at mid - 1 and the low remains the same. 
If the value is more than the mid point $key \gt mid$ then the high remains the same and the new low is set to mid + 1 
This "new" list is treated in the same fashion as before and the process starts over again.
The search ends either when low > high or when mid = key

A code representation written in python
```python
def binary_search(array, key):
    low = 0
    high = len(array) - 1
    mid = (high + low) // 2
    while low <= high:
        if array[mid] == key:
            return mid
        if array[mid] < key:
            low = mid + 1
        else:
            high = mid - 1
        mid = (high + low) // 2
    return -1
```

Visual representation using a binary tree with a 15 element array as an example
![[Pasted image 20240303015735.png]]

Each node is the mid point index and each branch is if the key is either lower (left branch) or higher (right branch) than the current mid

Since binary search can be represented by a binary tree the height of the tree is the worst case time complexity of the algorithm which is O(log(n)). In addition the best case is constant time or O(1)

There is also a way to represent binary search as a recursive algorithm instead of the iterative example used above
```python
def binary_search_recursive(array, low, high, key):
	if low == high:
		if array[low] == key:
			return low
		else:
			return -1
	else:
		mid = (low + high) // 2
		if key == array[mid]:
			return mid
		if key < array[mid]:
			return binary_search_recursive(array, low, mid-1, key)
		else:
			return binary_search_recursive(array, mid+1, high, key)
```

Using recurrence relation we can find the time complexity in relation to the function now being recursive
First the summation of each statement is written
$T(n)=T(n/2)+1$
Since the recursive call divides the array in half each time it can be represented as n/2 (note: the recursive call is called at max once because of the if/else statement ) also only +1 is used since the other statements add up to only a constant

Branching case
$T(n)=\begin{cases} 1 & n=1 \\ T(n/2)+1 & n \gt 1 \end{cases}$

Using masters theorem we can get the time complexity
$T(n)=T(n/2)+1$
$log_ba=log_21=0$
$k=0$ and $p=0$
$log_ba=k$ and $p \gt -1$
$T(n)=\Theta(n^0log^{0+1}n)$
Simplified
$T(n)=\Theta(logn)$


---
## Links

- [[Divide and Conquer Strategy]]
- [[Binary Tree]]
- [[Recurrence Relation]]
- [[Algorithm]]

---

## Source

- [Bari's Algorithm Playlist 2.6.1](https://youtu.be/C2apEw9pgtw?si=da0GWDbWV9mXh23q)
- [Bari's Algorithm Playlist 2.6.2](https://youtu.be/uEUXGcc2VXM?si=w20r_RUMkGhWP8AC)