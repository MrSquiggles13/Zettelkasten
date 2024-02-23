202402180403
# Best Worst and Average Case Analysis

## Notes

Best case time is the most optimal and ideal situation where the algorithm takes the shortest amount of time to do its process

Worst case time is the least optimal or ideal situation where the algorithm has to use the longest time possible to do its process

Average case time is all possible case times divided by the number of cases ($\frac{all Possible Case Times}{number Of Cases}$). Finding the average case for algorithms can be difficult neigh impossible and most of the time is similar if not identical to worst case. Worst case is primarily the favorited metric to use in analyzing algorithms.


#### Definition Through Examples

_**Linear Search**_

Given list (or array) A:
```python
A = [8, 6, 12, 5, 9, 7, 4, 3, 16, 18]
```

To find value X we need to traverse the list starting from index 0 and move one to the right in the list, in order, until the value X is found

If value X is not stored in the list then the list has to be traversed in its entirety in order to realize that no such value exists

The best case scenario for linear search would be if the value being searched for is in the first index or index 0 aka the value of 8 in relation to list A. This scenario would have constant time or 1.

The worst case scenario for linear search would be if the value being searched for is either at the last index of the list OR the value is not present in the list searched  aka the value 20 in relation to list A. This scenario would have a linear time or n.

The average case scenario would be $\frac{n+1}{2}$ which using the above formula ($\frac{all Possible Case Times}{number Of Cases}$) allPossibleCaseTimes = 1 + 2 + 3 + ... + n  and numberOfCases = n which would equal $\frac{\frac{n(n+1)}{2}}{n}$ which reduces to $\frac{n+1}{2}$

Any [[Asymptotic Notations]] can be used in the cases i.e. Best Case or B(n) = 1 could be represented as B(n) = $O(1)$ OR $\Omega(1)$ OR $\Theta(1)$
Same with Worst Case or W(n) = n i.e. W(n) = $O(n)$ OR $\Omega(n)$ OR $\Theta(n)$
And Average Case or A($\frac{n+1}{2}$) i.e. A(n) = $O(n)$ OR $\Omega(n)$ OR $\Theta(n)$

_**Binary Search Tree**_

Given [[Binary Search Tree]] B:

When it is balanced (at minimum height):
![[Pasted image 20240221054259.png]]

At min height the Best Case or B(n) would be if the element searched is at the root node or base of the tree (in this case 20). The search time would be B(n) = 1 or constant time O(1)

The Worst Case or W(n) would be if the element is in one of the leaf nodes (5, 15, 25, 40) which would take the height of the tree to get to. Since this is the minimum height of the binary search tree the height is log(n) so the search time would be W(n) = log(n) or logarithmic time O(log(n))

The Average is possible but not necessary to calculate 

When it is left skewed (at maximum height):
![[Pasted image 20240221063121.png]]

As above at max height the Best Case is searching for an element at the root node (40) which would be B(n) = 1 or constant time O(1)

Here the Worst Case at max height would be if searching for an element at the farthest leaf node (5). Since this is at maximum height  the height is n so the search time would be W(n) = n or linear time O(n)

Again Average Case is possible but not necessary to calculate

Conclusion:
Since there is a min and max height to consider for basically the same binary search tree the Worst Case can e considered as h or the height of the tree W(n) = h

### IMPORTANT

- _**Best/Worst/Avg Case applies to the analysis on algorithms while [[Asymptotic Notations]] applies to the analysis of functions**_
- _**The result for Best/Worst/Avg case can be denoted by [[Asymptotic Notations]] since the result itself is a function**_

---
## Links

- [[How to Analyze an Algorithm]]
- [[Binary Search Tree]]

---

## Source

- [Bari's Algorithm Playlist 1.11](https://youtu.be/lj3E24nnPjI?si=miqhs1IDyV3SW7JX)