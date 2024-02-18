202402100245
# Asymptotic Notations

## Notes

Definition: Different methods to measure the time it takes to run an algorithm

### $O$ Big Oh - Upper Bound

$$f(n)=O(g(n)) \space\space if \space\space \exists\space\space +constants\space C \space\&\space n_0 $$
Such That:
$$f(n) \le C * g(n) \space\forall\space n \ge n_0$$
In plain English: function f of n (f(n)) equals Big Oh of g of n (O(g(n))) if and only if there exists ($\exists$) the positive constants (+ constants) C and n zero ($C \space n_0$) such that f of n (f(n)) is less than or equal to ($\le$) C times g of n ($C*g(n)$) for all ($\forall$) n is greater than or equal to n 0 ($n \ge n_0$)

This determines the range of solutions relating to the base equation above where the inequality remains true. 
The written notation is the smallest time function of the inequality's solution as possible
### $\Omega$ Big Omega - Lower Bound

$$f(n)=\Omega(g(n)) \space\space if \space\space \exists\space\space +constants\space C \space\&\space n_0 $$
Such That:
$$f(n) \ge C * g(n) \space\forall\space n \ge n_0$$
In plain English: function f of n (f(n)) equals Big Omega of g of n ($\Omega$(g(n))) if and only if there exists ($\exists$) the positive constants (+ constants) C and n zero ($C \space n_0$) such that f of n (f(n)) is greater than or equal to ($\ge$) C times g of n ($C*g(n)$) for all ($\forall$) n is greater than or equal to n 0 ($n \ge n_0$)

This determines the range of solutions relating to the base equation above where the inequality remains true. 
The written notation is the largest time function of the inequality's solutions as possible

### $\Theta$ Theta - Average Bound

$$f(n)=\Theta(g(n)) \space\space if \space\space \exists\space\space +constants\space C_1 \space C_2 \space \& \space n_0 $$
Such That:
$$C_1 * g(n) \le f(n) \le C_2 * g(n)$$
In plain English: function f of n (f(n)) equals Theta of g of n ($\Theta$(g(n))) if and only if there exists ($\exists$) the positive constants (+ constants) C one C two and n zero ($C_1 \space C_2 \space n_0$) such that C one times g of n ($C_1*g(n)$) is less than or equal to ($\le$) f of n (f(n)) AND f of n (f(n)) is less than or equal to ($\le$) C two times g of n ($C_2 * g(n)$)

This determines the average solution of the base equation above where the inequalities remain true
Will most likely be a singular time function where the upper and lower bounds overlap but could also have no solution

## Other notes

These notations do not imply best/worst case time complexity these notations only represent the bounds of a function.

---
## Links

- [[Types of Time Functions]]

---

## Source

- [Bari's Algorithm Playlist 1.8.1](https://youtu.be/A03oI0znAoc?si=JZhy0_k3Fkotx1vw)
- [Bari's Algorithm Playlist 1.8.2](https://youtu.be/Nd0XDY-jVHs?si=RtSBpBW7RbIR91pG)