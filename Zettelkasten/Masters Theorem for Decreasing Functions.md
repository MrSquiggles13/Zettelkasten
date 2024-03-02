202402250631
# Masters Theorem for Decreasing Functions

## Notes

A mathematical theorem that solves the complexity of a recursive function using a standard equation

**_General Form/Standard Equation of Recurrence Relation_**
$T(n)=aT(n-b)+f(n)$
$a \gt 0$ AND $b \gt 0$ AND $f(n)=O(n^k)$ where $k \ge 0$

$T(n)=\begin{cases} a \lt 1 & O(n^k) \text{ || } O(f(n)) \\ a=1 & O(n^{k+1}) \text{ || } O(n*f(n)) \\ a \gt 1 & O(n^ka^{\frac{n}{b}}) \text{ || } O(f(n)a^{\frac{n}{b}})  \end{cases}$

**_Simplify Evaluation_**
If a recursive function is in the format
$T(n)=T(n-1)+X$
Where $X$ is a variable or constant then the function's time complexity will evaluate to
$T(n)=X*n$

Example:
$T(n)=T(n-1)+1$ ---> $O(n)$
$T(n)=T(n-1)+n$ ---> $O(n^2)$
$T(n)=T(n-1)+log(n)$ ---> $O(n(log(n)))$
$T(n)=T(n-1)+n^2$ ---> $O(n^3)$

If the constant (here it is 1) in the equation's recursive call differs in magnitude the rule still stands

Example:
$T(n)=T(n-2)+1$ ---> $\frac{n}{2}$ ---> $O(n)$
$T(n)=T(n-100)+n$ ---> $\frac{n^2}{100}$ ---> $O(n^2)$

Like wise if a recursive function is in the format
$T(n)=CT(n-1)+X$
Where C and X are a constant or variable the time complexity will evaluate to
$T(n)=C^n*X$

**_Example_**
$T(n)=2T(n-1)+1$ ---> $O(2^n)$
$T(n)=3T(n-1)+1$ ---> $O(3^n)$
$T(n)=2T(n-1)+n$ ---> $O(n2^n)$


---
## Links

- [[Recurrence Relation]]

---

## Source

- [Bari's Algorithm Playlist 2.2](https://youtu.be/CyknhZbfMqc?si=-eVpMZV6ijZEfD1L)