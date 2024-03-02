202402290319
# Dividing Functions

## Notes

A recursive function that when called on itself the input value is divided by some value

Examples:

Given the function
```C
Algorithm Test(int n){ // --- T(n)
	if(n > 1){
		printf("%d", n); // --- 1
		Test(n / 2); // --- T(n/2)
	}
}
```

The summation of time values from the function's statements
$T(n)=T(n/2)+1$

The cases of the function are
$T(n)=\begin{cases} 1 & n=1 \\ T(n/2)+1 & n\gt1 \end{cases}$

Tracing Tree:
![[Pasted image 20240229040705.png]]

Each recursive call takes constant time up to k and the terminating statement will be equal to 1
$T(n/2^k)=1$ OR $n/2^k=1$

When evaluated in terms of k
$n/2^k=1$
$n=2^k$
$k=log(n)$

So it is determined that the function will take log n time
$T(n)=O(log(n))$

Substitution method:
$T(n)=T(n/2)+1$
$T(n/2)=T(n/2^2)+1$
$T(n)=T(n/2^2) + 2$
$T(n/2^2)=T(n/2^3) + 1$
$T(n)=T(n/2^3)+3$
$T(n)=T(n/2^k)+k$
Assume $n/2^k=1$
$n=2^k$ AND $k=log(n)$
Substitute
$T(n)=T(1)+log(n)$
$T(n)=1+log(n)$ OR $T(n)=O(log(n))$


Given the function
```C
Algo Test(int n){ // --- T(n)
	if(n > 1){
		for(int i=0; i<n; i++){
			printf("%d", n); // --- n
		}
		Test(n/2); // --- T(n/2)
	}
}
```

The summation of the statements' time complexity is
$T(n)=T(n/2)+n$

The branching cases are
$T(n)=\begin{cases} 1 & n=1 \\ T(n/2)+n & n\gt1 \end{cases}$

Tracing tree
![[Pasted image 20240229044216.png]]

The summation of the resulting complexities of each statement
$T(n)=n+\frac{n}{2}+\frac{n}{2^2}+\frac{n}{2^3}+...+\frac{n}{2^k}$
Factor out n
$T(n)=n[1+\frac{1}{2}+\frac{1}{2^2}+\frac{1}{2^3}+...+\frac{1}{2^k}]$
Simplify understanding there is a geometric series
$T(n)=n\displaystyle \sum_{i=1}^k\frac{1}{2^i}=1$ 
Substitute
$T(n)=n*1+1$ OR $T(n)=n+1$ SO $T(n)=O(n)$


Substitution Method:
$T(n)=T(n/2)+n$
$T(n/2)=T(n/2^2)+n/2$
$T(n)=T(n/2^2)+n/2+n$
$T(n/2^2)=T(n/2^3)+n/2^2$
$T(n)=T(n/2^3)+n/2^2+n/2+n$
$T(n)=T(n/2^k)+n/2^{k-1}+n/2^{k-2}+...+n/2+n$
Assume $\frac{n}{2^k}=1$
$n=2^k$ AND $k=log(n)$
Substitute
$T(n)=T(1)+n[1+\frac{1}{2}+\frac{1}{2^2}+\frac{1}{2^3}+...+\frac{1}{2^k}]$
$T(n)=1+n[1+1]$ OR $T(n)=1+2n$ SO $T(n)=O(n)$


Given the function
```C
Algo Test(int n){ // --- T(n)
	if(n > 1){
		for(int i=0; i<n; i++){
			statement; // --- n
		}
		Test(n/2); // --- T(n/2)
		Test(n/2); // --- T(n/2)
	}
}
```

The summation of the statements' time complexity is
$T(n)=2T(n/2)+n$

The cases for the function
$T(n)=\begin{cases} 1 & n=1 \\ 2T(n/2)+n & n\gt1 \end{cases}$

Tracing Tree
![[Pasted image 20240301014900.png]]

Instead of branching out to function calls each node is the time taken for each function call instead of the function itself i.e. T(n/2) is just n/2

A summation of each layer in the tree derives to a value of n which equates to n occurring k times according to the terminating condition which can be written as $n*k$ times

With this it can be assumed that $\frac{n}{2^k}=1$ which when refactored
$n=2^k$ and $k=log(n)$
And since the time complexity has already been establish to be $n*k$ when k is substituted to make the equation in terms of n
$T(n)=nlog(n)$ OR $T(n)=O(nlog(n))$

Substitution method
$T(n)=2T(n/2)+n$
$T(n/2)=2T(n/2^2)+n/2$
$T(n)=2^2T(n/2^2)+2n$
 $T(n/2^2)=2T(n/2^3)+n/2^2$
$T(n)=2^3T(n/2^3)+3n$
$T(n)=2^kT(n/2^k)+kn$
Assume
$T(n/2^k)=T(1)$
$\frac{n}{2^k}=1$
$n=2^k$
$k=log \space n$
Substitute
$T(n)=2^kT(1)+kn$
$T(n)=n*1+nlogn$
Taking highest order of magnitude for asymptotic notation
$T(n)=O(nlogn)$




---
## Links

- [[Recurrence Relation]]
- [[Geometric Series]]

---

## Source

- [Bari's Algorithm Playlist 2.3.1](https://youtu.be/8gt0D0IqU5w?si=Bn1RClzDFwZONmhY)
- [Bari's Algorithm Playlist 2.3.2](https://youtu.be/XcZw01FuH18?si=fWq80diZ4n8K4rMn)
- [Bari's Algorithm Playlist 2.3.3](https://youtu.be/1K9ebQJosvo?si=QhNbJJSItPuSYz1X)