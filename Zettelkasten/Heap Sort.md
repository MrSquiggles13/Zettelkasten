202403070147
# Heap Sort

## Notes

When an element is deleted in a heap and stored at the end of the array representation of said heap (yet dictated as separate from the heap itself) each element will then be in a sorted position since only the root can be deleted which by the conditions of delete will either be the largest or smallest element (max heap or min heap). After each node in a heap is deleted then the entire heap will be sorted. This method is called **_heap sort_**.
A good note is that the size of the array doesn't change as elements are deleted and the deleted node being inserted at the end of the array is essentially just replacing the now empty index after the deletion is finished

The steps of heap sort for a given set of numbers is to
![[Pasted image 20240307005440.png]]

**_Create a heap_**
First using a list take each element and insert into a new heap sequentially utilizing the insert method. Starting with the first element of the list we linearly move through the list and treat it as a stand alone insertion into the heap

**_Delete all the elements_**
Then each element in the newly created heap is deleted one by one utilizing the delete method for the heap. With the array representation of the heap the freed index after the deletion can be utilized to store the deleted element.

After the last element is deleted the array representation that stored the deleted elements separately will now have a sorted list

The time complexity of a heap sort in total is $2nlogn$ since creation and deletion both take $nlogn$ which is asymptotic notation is represented as $O(nlogn)$

---
## Links

- [[Heap]]
- [[Algorithm]]

---

## Source

- [Bari's Algorithm Playlist 2.6.3](https://youtu.be/HqPJF2L5h9U?si=03rUBdf8QtbbDSZ4)