202402100245
# Asymptotic Notations

## Notes

Definition: Different methods to measure the time it takes to run an algorithm

### $O$ Big Oh - Upper Bound

$$f(n)=O(g(n)) \space\space if \space\space \exists\space\space +constants\space C \space\&\space n_0 $$
Such That:
$$f(n) \le C * g(n) \space\forall\space n \ge n_0$$
In plain English: function f of n (f(n)) equals Big Oh of g of n (O(g(n))) if and only if there exists ($\exists$) the positive constants (+ constants) C and n 0 ($C \space n_0$) such that f of n (f(n)) is less than or equal to ($\le$) C times g of n ($C*g(n)$) for all ($\forall$) n is greater than or equal to n 0 ($n \ge n_0$)
### $\Omega$ Big Omega - Lower Bound

$$f(n)=\Omega(g(n)) \space\space if \space\space \exists\space\space +constants\space C \space\&\space n_0 $$
Such That:
$$f(n) \ge C * g(n) \space\forall\space n \ge n_0$$
In plain English: function f of n (f(n)) equals Omega of g of n ($\Omega$(g(n))) if and only if there exists ($\exists$) the positive constants (+ constants) C and n 0 ($C \space n_0$) such that f of n (f(n)) is greater than or equal to ($\ge$) C times g of n ($C*g(n)$) for all ($\forall$) n is greater than or equal to n 0 ($n \ge n_0$)

### $\Theta$ Theta - Average Bound

$$f(n)=O(g(n)) \space\space if \space\space \exists\space\space +constants\space C_1 \space C_2 \space \& \space n_0 $$
Such That:
$$C_1 * g(n) \le f(n) \le C_2 * g(n)$$
In plain English: function f of n (f(n)) equals Big Oh of g of n (O(g(n))) if and only if there exists ($\exists$) the positive constants (+ constants) C and n 0 ($C \space n_0$) such that f of n (f(n)) is less than or equal to ($\le$) C times g of n ($C*g(n)$) for all ($\forall$) n is greater than or equal to n 0 ($n \ge n_0$)


---
## Links

- [[Types of Time Functions]]

---

## Source

- 