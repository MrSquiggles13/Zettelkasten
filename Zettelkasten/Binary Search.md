202403020452
# Binary Search

## Notes

An algorithmic method for finding a value inside a _sorted_ list


![[binary-and-linear-search-animations.gif]]

Binary search starts with 2 pointers one pointing to the first index of the list and the second to the last index called the low and high pointers respectfully

Then a mid point is determined from the formula $mid=\frac{low+high}{2}$ which is used to check against the value to search for.
If the value is less than the mid point $key \lt mid$ then 
If the value is more than the mid point $key \gt mid$ then the new high is set at mid - 1 and the low remains the same. 
This "new" list is treated in the same fashion as before and the process starts over again.
The search ends either when low=high or when mid=key

A code representation written in python
```python
def binary_search(array, key):
    low = 0
    high = len(array) - 1
    mid = (high + low) // 2
    while low < high:
        if array[mid] == key:
            return mid
        if array[mid] < key:
            low = mid + 1
        else:
            high = mid - 1
        mid = (high + low) // 2
    return -1
```


---
## Links

- [[Divide and Conquer Strategy]]
- [[Algorithm]]

---

## Source

- [Bari's Algorithm Playlist 2.6.1](https://youtu.be/C2apEw9pgtw?si=da0GWDbWV9mXh23q)