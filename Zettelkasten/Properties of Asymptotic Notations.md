202402150334
# Properties of Asymptotic Notations

## Notes

### General Properties

$if \space f(n) \space is \space \Omega(g(n)) \space then \space a*f(n) \space is \space \Omega(g(n))$

if the original function is multiplied by a constant the class of the time function will remain the same

True for notations: O $\Omega$ $\Theta$

Example:
$if \space f(n)=2n^2 + 5 \space is \space O(n^2)$
$then \space 7(f(n)) = 7(2n^2 + 5) \space is \space O(n^2)$

### Reflexive Property

$if \space f(n) \space is \space given \space then \space f(n) \space is \space O(f(n))$

If a function is equal to a class of a time function then the time function will be the function itself

True for notations: O $\Omega$ $\Theta$

Example:
$f(n)=n^2 \space then \space O(n^2)$

### Transitive Property

$if \space f(n) \space is \space O(g(n)) \space AND \space g(n) \space is \space O(h(n)) \space then \space f(n) = O(h(n))$

If time complexity is equivalent in a chain relating to one another then the first and last link will be equivalent in time complexity

True for notations: O $\Omega$ $\Theta$

Example:
$f(n)=n \space g(n)=n^2 \space h(n)=n^3$
$if \space n \space is \space O(n^2) \space AND \space n^2 \space is \space O(n^3)$
$then \space n \space is \space O(n^3)$

### Symmetric Property

$if \space f(n) \space is \space \Theta(g(n)) \space then \space g(n) \space is \space \Theta(f(n))$

If the time complexity of function$_1$ is equal to function$_2$ then function$_2$'s time complexity is function$_1$

True for notations: $\Theta$

Example:
$f(n)=n^2 \space g(n)=n^2$
$f(n)=\Theta(n^2)$
$g(n)=\Theta(n^2)$

### Transpose Symmetric Property

$if \space f(n)=O(g(n)) \space then \space g(n) \space then \space g(n)=\Omega(f(n))$

If the Big Oh time complexity (upper bound) of function$_1$ is function$_2$ then the Big Omega time complexity (lower bound) of function$_2$ is function$_1$

True for notations: O $\Omega$

Example:
$f(n)=n \space g(n)=n^2$
then $n \space is \space O(n^2)$ AND $n^2 \space is \space \Omega(n)$

### Other Examples:

 _**Deriving Average**_

$if \space f(n)=O(g(n)) \space AND \space f(n)=\Omega(g(n))$
$then \space f(n)=\Theta(g(n))$

If the Big Oh and Big Omega time complexities of a function are equal then Theta is also equal to those time complexities

Example:
$g(n) \le f(n) \le g(n)$

**_Additive_**

$if \space f(n)=O(g(n) \space AND \space d(n)=O(e(n))$
$then \space f(n)+d(n)=O(max(g(n),e(n)))$

The time complexity of adding functions together will be the greater of all the individual functions time complexities

Example:
$f(n)=n=O(n)$
$d(n)=n^2=O(n^2)$
$f(n)+d(n)=n+n^2=O(n^2)$

**_Multiplicative_**

$if \space f(n)=O(g(n)) \space AND \space d(n)=O(e(n))$
$then \space f(n)*d(n)=O(g(n)*e(n))$

The time complexity of multiplying functions together will be the product of all the individual functions time complexities


---
## Links

- [[Asymptotic Notations]]

---

## Source

- [Bari's Algorithm Playlist 1.9](https://youtu.be/NI4OKSvGAgM?si=aJbEo1kUASRa5Ho4)