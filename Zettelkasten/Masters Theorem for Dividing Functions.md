202403010332
# Masters Theorem for Dividing Functions

## Notes

General form for recurrence relation for dividing functions
$$\begin{equation} \begin{gathered}
	T(n)=aT(n/b)+f(n) \\ 
	a \ge 1 \ b \gt 1 \\
	f(n)=O(n^klog^pn)
  \end{gathered} \end{equation} $$

To derive k and p the equation will have a degree for each and if not present then it is 0 or just the constant 1

Branching cases
$$T(n)=\begin{cases} log_ba \gt k & \Theta(n^{log_ba}) \\ \\ log_ba=k & \begin{cases} p \gt -1 & \Theta(n^klog^{p+1}n) \\ p=-1 & \Theta(n^kloglogn) \\ p \lt -1 & \Theta(n^k) \end{cases} \\ \\ log_ba \lt k & \begin{cases} p \ge 0 & \Theta(n^klog^pn) \\ p \lt 0 & \Theta(n^k) \end{cases} \end{cases}$$

p is less than or equal to -1 when log(n) is in the denominator

**_Examples_**

Function
$T(n)=2T(n/2)+1$
$a=2$ and $b=2$
$f(n)=\Theta(1)$ OR $f(n)=\Theta(n^0log^0n)$

$log_ba=log_22=1$
Since f(n) is $\Theta(1)$ hence $f(n)=\Theta(n^0log^0n)$ because there is no n or log(n) present
$k=0$ and $p=0$
This is case 1 because $log_ba \gt k$ So $T(n)=\Theta(n^{log_ba})$ OR $T(n)=\Theta(n^1)$ OR just n

Function
$T(n)=4T(n/2)+n$
$log_ba=log_24=2$
$k=1$ and $p=0$
Use case 1 since $log_ba>k$
$T(n)=\Theta(n^2)$

Function
$T(n)=8T(n/2)+n$
$log_ba=log_28=3$
$k=1$ and $p=0$
Case 1
$T(n)=\Theta(n^3)$

Function
$T(n)=8T(n/2)+n^2$
$log_ba=log_28=3$
$k=1$ and $p=0$
Case 1
$T(n)=\Theta(n^3)$

Function
$T(n)=9T(n/3)+1$
$log_ba=log_39=2$
$k=0$ and $p=0$
Case 1
$T(n)=\Theta(n^2)$

Function
$T(n)=9T(n/3)+n$
$log_ba=log_39=2$
$k=1$ and $p=0$
Case 1
$T(n)=\Theta(n^2)$

Function
$T(n)=2T(n/2)+n$
$log_ba=log_22=1$
$k=1$ and $p=0$
Case 2.1 since $log_ba=k$ and $p>-1$
$T(n)=\Theta(nlogn)$

Function
$T(n)=4T(n/2)+n^2$
$log_ba=log_24=2$
$k=2$ and $p=0$
Case 2.1
$T(n)=\Theta(n^2logn)$

Function
$T(n)=4T(n/2)+n^2logn$
$log_ba=log_24=2$
$k=2$ and $p=1$
Case 2.1
$T(n)=\Theta(n^2log^2n)$

Function
$T(n)=2T(n/2)+\frac{n}{logn}$
$log_ba=log_22=1$
$k=1$ and $p=-1$
Case 2.2 since $log_ba=k$ and $p=-1$
$T(n)=\Theta(nloglogn)$

Function
$T(n)=2T(n/2)+\frac{n}{log^2n}$
$log_ba=log_22=1$
$k=1$ and $p=-2$
Case 2.3 since $log_ba=k$ and $p \lt -1$
$T(n)=\Theta(n)$

Function
$T(n)=T(n/2)+n^2$
$log_ba=log_21=0$
$k=2$ and $p=0$
Case 3.1 since $log_ba \lt k$ and $p \ge 0$
$T(n)=\Theta(n^2)$

Function
$T(n)=2T(n/2)+n^2logn$
$log_ba=log_22=1$
$k=2$ and $p=1$
Case 3.1
$T(n)=\Theta(n^2logn)$

Function
$T(n)=4T(n/2)+\frac{n^3}{logn}$
$log_ba=log_24=2$
$k=3$ and $p=-1$
Case 3.2 since $log_ba \lt k$ and $p \lt 0$
$T(n)=\Theta(n^3)$


---
## Links

- [[Recurrence Relation]]
- [[Dividing Functions]]

---

## Source

- [Bari's Algorithm Playlist 2.4.1](https://youtu.be/OynWkEj0S-s?si=TIB5E1WHvoCMJvow)
- [Bari's Algorithm Playlist 2.4.2](https://youtu.be/kGcO-nAm9Vc?si=M1OOif1JcqyNKXzC)