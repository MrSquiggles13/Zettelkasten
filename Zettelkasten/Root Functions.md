202403020308
# Root Functions

## Notes

A function that is recursive and calls itself with the root of the input

Examples:

Given the function
```C
void Test(int n){ // --- T(n)
	if(n > 2){
		statement; // --- 1
		Test(sqrt(n)); // --- T(sqrt(n))
	}
}
```

The summation of the time complexity of each statement is
$T(n)=T(\sqrt{n})+1$

Branching cases
$T(n)=\begin{cases} 1 & n=2 \\ T(\sqrt{n})+1 & n \gt 2 \end{cases}$

Using substitution method
$T(n)=T(\sqrt{n})+1$
$T(n)=T(n^{\frac{1}{2}})+1$
$T(n^{\frac{1}{2}})=T(n^{\frac{1}{2^2}})+1$
$T(n)=T(n^{\frac{1}{2^2}})+2$
$T(n^{\frac{1}{2^2}})=T(n^{\frac{1}{2^3}})+1$
$T(n)=T(n^{\frac{1}{2^3}})+3$
$T(n)=T(n^{\frac{1}{2^k}})+k$
Assume
$n=2^m$
$T(2^m)=T(2^{\frac{m}{2^k}})+k$
Assume
$T(2^{\frac{m}{2^k}})=T(2^1)$
$\frac{m}{2^k}=1$
$m=2^k$ AND $k=log_2m$
$n=2^m$ AND $m=log_2n$
SO $k=log_2log_2n$
OR $k=loglogn$
$T(n)=\Theta(loglogn)$




---
## Links

- [[Recurrence Relation]]

---

## Source

- [Bari's Algorithm Playlist 2.5](https://youtu.be/9rVuyjxzwgM?si=5vOW4LSmwFKeOmFK)