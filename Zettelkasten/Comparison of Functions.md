202402150501
# Comparison of Functions

## Notes

Analytically determining whether two functions are either greater than, lesser than, or equal to each other

---

Inputting values can help compare two functions 
Example:

| n | n$^2$ | n$^3$ |
| ---- | ---- | ---- |
| 1 | 1 | 1 |
| 2 | 4 | 8 |
| 3 | 9 | 27 |
| 4 | 16 | 64 |
So n$^3$ is greater than n$^2$ since as the base n increases n$^3$ maintains a higher value

---

Applying log (a logarithm) to both sides of a function can also help with comparing of functions with a greater complexity
Example:

comparing n$^2$  to n$^3$
log(n$^2$)  log(n$^3$)
2log(n)  3log(n)

3 > 2 and base is same so in conclusion n$^3$ is the larger function

---

Using the laws of logarithms the functions can be broken down even more to a readable scale if needed

#### Laws of Logarithms

1. $log(ab)=log(a)+log(b)$
2. $log(\frac{a}{b})=log(a)-log(b)$
3. $log(a^b)=b(log(a))$
4. $a^{log_c(b)}=b^{log_c(a)}$
5. $a^b=n  == b=log_a(n)$

#### Examples

1. Comparing the two functions:
	- $f(n)=n^2log(n)$ AND $g(n)=n(log(n))^{10}$

- Apply log to both sides and simplify:
	1. $log(n^2log(n))$  |  $log(n(log(n))^{10})$
	2. $log(n^2) + log(log(n))$  |  $log(n)+log(log(n)^{10})$
	3. $2(log(n))+log(log(n))$  |  $log(n)+10(log(log(n)))$

Conclusion: Since the greatest term is log(n) and the left function has a constant (2) multiplied to it while the other is just log(n) the left function $f(n)=n^2log(n)$ is greater

---
2. Comparing the two functions:
	- $f(n)=3n^\sqrt{n}$  AND  $g(n)=2^{\sqrt{n}(log(n))}$

- Apply logarithmic formulas and simplify:
	1. $3n^{\sqrt{n}}$  |  $2^{log_2(n^{\sqrt{n}})}$  //Using the third logarithmic formula for right function
	2. $3n^{\sqrt{n}}$  |  $(n^{\sqrt{n}})^{log_2(2)}$ //Using the fourth logarithmic formula for right function
	3. $3n^{\sqrt{n}}$  |  $(n^{\sqrt{n}})^1$ // log base C of C is 1
	4. $3n^{\sqrt{n}}$  |  $n^{\sqrt{n}}$

Conclusion: The base term ($n^{\sqrt{n}}$) has a greater constant multiplying into it on the left function hence the left function is greater

---
3. Comparing the two functions:
	- $f(n)=n^{log(n)}$  AND  $g(n)=2^{\sqrt{n}}$

- Apply log to both sides and simplify:
	1. $log(n^{log(n)})$  |  $log(2^{\sqrt{n}})$
	2. $log(n)(log(n))$  |  $\sqrt{n}(log_2(2))$ //Using third formula for both functions
	3. $log^2(n)$  |  $\sqrt{n}$ //Left is rewritten in terms of log and right the log cancels out to 1
	4. $log^2(n)$  |  $n^{\frac{1}{2}}$ //Right is written as an exponent
	5. $2(log(log(n)))$  |  $\frac{1}{2}(log(n))$ //Both are written in terms of log

Conclusion: Since the right function can be broken down to one log function and the left is two log functions we can determine that the right function is greater

---
4. Comparing the two functions:
	- $f(n)=2^{log(n)}$  AND  $g(n)=n^{\sqrt{n}}$

- Apply log to both sides and simplify:
	1. $log(2^{log(n)})$  |  $log(n^{\sqrt{n}})$
	2. $log(n)(log(2))$  |  $\sqrt{n}(log(n))$ //Use third formula to both functions
	3. $log(n)$  |  $\sqrt{n}(log(n))$ //Reduce left function

Conclusion: Base term (log(n)) is same on both sides but right function has it multiplied by root n ($\sqrt{n}$) so the right function is greater

---
5. Comparing the two functions:
	- $f(n)=2n$  AND  $g(n)=3n$

Conclusion: Since these are base functions and no simplification was needed to make a comparison essentially these functions are equal

---
6. Comparing two functions:
	- $f(n)=2^n$  AND  $g(n)=2^{2n}$

- Apply log to both sides and simplify:
	1. $log(2^n)$  |  $log(2^{2n})$
	2. $n(log(2))$  |  $2n(log(2))$ //Using the third formula to both functions
	3. n  |  2n //Reduce both functions

Conclusion: Since the functions had to be simplified the end result shows actual magnitude to the weight of each function. Hence the right most function is greater

---
## Links

- [[Types of Time Functions]]

---

## Source

- [Bari's Algorithm Playlist 1.10.1](https://youtu.be/mwN18xfwNhk?si=uq_bey6Hv5GT3DI9)
- [Bari's Algorithm Playlist 1.10.2](https://youtu.be/WlBBTSL0ZRc?si=HsQSApgAkl4u5ZBt)