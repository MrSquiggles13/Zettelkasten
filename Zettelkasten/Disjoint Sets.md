202402210650
# Disjoint Sets

## Notes

Helps to determine if there is a cycle in an undirected graph

Is a derivative of a set and similar to sets in mathematical [[Set Theory]] but is primarily used in algorithms and has some unique properties

A common algorithm that uses disjointed sets is [[Kruskal's Algorithm]]

Using this graph as an example:
![[Pasted image 20240221223339.png]]

The graph is non-connected and non-directed separated into 2 component which can be represented as sets:
$S_1=\{1, 2, 3, 4\}$
$S_2=\{5, 6, 7, 8\}$

The disjoint between the components (sets) can be represented by taking the intersection of the sets
$S_1 \cap S_2 = \Phi$
Where $\Phi$ represents an empty or null set

There are 2 common operations that are utilized on a disjointed set

_**Find**_

An operation to locate in which set a certain element (take 5 for example) belongs to ($S_2$)

_**Union**_

Combining components of a graph that is non-connected or similarly 2 sets that represent those components 

Taking this graph here:
![[Pasted image 20240222001247.png]]

Which is the same graph above yet there is an edge drawn between the two components 4 and 8.

This represents a union between the two components since to determine the edge in this graph the two separate sets must be combined:
edge (4, 8)
since 4 belongs to $S_1$ and 8 belongs to $S_2$ a union must be used
$S_1 \cup S_2 = \{1, 2, 3, 4, 5, 6, 7, 8\}$

This union creates its own set 
$S_3 = \{1, 2, 3, 4, 5, 6, 7, 8\}$

Now with these two operations we can determine if there is a cycle in a graph. When a find operation is performed on the new set and the new graph with edges in place for the union which now looks like this:
![[Pasted image 20240222022418.png]]

We can see that any edge we try to derive i.e. (1, 5) that it is part of the same set and can be determined to be cyclical

_**Use Case Example (Graph):**_
![[Pasted image 20240222022655.png]]
First a universal set is defined which includes all the nodes or vertices of the graph each one considered as its own isolated set
$U = \{1, 2, 3, 4, 5, 6, 7, 8\}$

After which we can start defining the edges as their own sets which is essentially a union between the individual element sets of the universal set
Edge 1(1, 2) is $S_1=\{1, 2\}$
Edge 2(3, 4) is $S_2=\{3, 4\}$
Edge 3(5, 6) is $S_3=\{5, 6\}$
Edge 4(7, 8) is $S_4=\{7, 8\}$

When we reach the edges with vertices already paired as a set prior a new set formed through a union is made and sets used for these unions are discarded (note: the single element sets in the universal set also are discarded after the first group of unions)
Edge 5(2, 4) is $S_5 = \{1, 2, 3, 4\}$

Since edge 6 includes an element in $S_5$ that set is also discarded after the union
Edge 6(2, 5) is $S_6 = \{1, 2, 3, 4, 5, 6\}$

Edge 7(1, 3) has both elements in the previous set formed and since this edge's vertices do not need a union to make a new set a cycle can be determined

One could stop here if the goal is to determine if there is a cycle or not but this method can be used to count how many cycles there as well
Edge 8(6, 8) is $S_7 = \{1, 2, 3, 4, 5, 6, 7, 8\}$

Now using the 9th and final edge with vertices (5, 7) we can determine another cycle since those elements are already in a previously generated set

The previous steps can be represented in a visual way like so:
![[Pasted image 20240222030603.png]]

This shows that each edge is grouped with a child and parent node i.e. {1, 2} 2 is the child node of the parent node 1.

![[Pasted image 20240222031444.png]]

Here we can see the union of $S_1 \text{ and } S_2$ in relation to Edge 5(2, 4) or also known as $S_5$ in which the placement of the root or parent node of the union can be interchangeable between the two parents of the combined sets since they are of equal weight or rank

![[Pasted image 20240222031937.png]]

Edge 6(2, 5) is now evaluated and added as a child to the previous union set creating $S_6$ and this time the larger existing set is cemented as the root since it has more weight than $S_3$

Edge 7(1, 3) again already has elements included in the base or root set. 1 being the root and 3 having 1 as the parent determines that the graph is a cycle

And the step stay congruent with the previous explanation with the added rules of adding to the most weighted set or model

_**Use Case Example (Array):**_
![[Pasted image 20240222032856.png]]

The array above represents the graph used in the previous example with the same layout, edges, and nodes or vertices

The universal set is to help understand the correlations of an array representation and a graphical representation.

Each element in the array written underneath is representative of the node and the numbers in the boxes above it (all -1 currently) represent the parent of that node. -1 is used to represent that the node underneath is a parent node of itself

![[Pasted image 20240222033830.png]]

When Edge 1(1,2) is evaluated similar to the set/graph method above they become linked. It is represented by adjusting the value above 2 to 1 from -1 since 1 is now the parent of 2 and 1 gets a value of -2 since it is the parent node and now contains 2 nodes

![[Pasted image 20240222043852.png]]

Similarly we can apply the same method for edges 2-4 where the pairing is represented by the root node having negative value representative of being the parent and how many total nodes there are in the grouping on top of any child node established has their parent node's value

![[Pasted image 20240222044242.png]]

For Edge 5(2,4) same union operation is used yet in an array representation the new root node 1 has the value -4 since now there are 4 nodes in the grouping and 3 now has 1 as its value since that is the new parent or root node

![[Pasted image 20240222044331.png]]

Again the operation above for Edge 6 is performed making another union and now the root node 1 has a value of -6 since there are 6 nodes in the grouping and 5 now is pointed to that root node 1

And when moving on to Edge 7(1,3) we can see in the array that both values already lead to the root node 1 hence there is a cycle in the graph and this operation can continue to determine how many there are

_**Important terms**_

Weighted Union:
	Was explained earlier but this is the term for when a union is performed on sets representing a graph the root node for the set/graph is determined by which set/graph has the most weight (contains the most nodes) if weight is equal it does not matter which one gets used for the root node

Collapsing Find:
	If we were trying to find the value 6 we would have to trace back to the root element 1 through 6's parent element of 5
	![[Pasted image 20240222045304.png]]
	But once it is discovered that 6 had a base root of 1 then we can just assign 6's parent node to 1 itself making the next lookup faster
	![[Pasted image 20240222045424.png]]
	This defines collapsing find as it "collapses" the graph to make lookups or find easier and faster to implement
---
## Links

- [[Set Theory]]
- [[Data Structure]]
- [[Graph - Data Structure]]

---

## Source

- [Bari's Algorithm Playlist 1.12](https://youtu.be/wU6udHRIkcc?si=OpDhjSAR7ekWjs4x)