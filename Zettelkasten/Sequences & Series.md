20260726-0519
# Sequences & Series

## Notes

A sequence is an ordered list of numbers. Each number is called a term and the subscript is called the index $\{a_1, a_2, a_3, ... a_n\}$ and can be denoted $a_n$. If a sequence approaches a unique number $L$ as $n$ increases then $\lim\limits_{n \to \infty} a_n = L$ exists and the sequence converges to $L$ otherwise the sequence diverges.

Sequences can be set as a function to be able to take the limit $f(n) = a_n = \frac{1}{n}$ so $f(x) = \frac{1}{x}$.

If the limit of the absolute value of a sequence is zero then the limit of the sequence is zero $\lim\limits_{n \to \infty} |a_n| = 0$ then $\lim\limits_{n \to \infty} a_n = 0$. This is derived from the squeeze theorem which can also help deduce the limit of a sequence by checking a known lower and higher limit to see if they all converge to the same limit.

If a sequence is in the form $(\frac{a}{b})^n$ where the ratio $r = \frac{a}{b}$ then if $|r| < 1$ the limit $L = 0$.

A recursive sequence has a formula that include the first $x$ terms of the sequence itself such as the Fibonacci sequence $a_1 = 1, a_2 = 1, a_n = (n - 1) + (n - 2)$.

For composite functions of a sequence the inner functions limit gives the limit of the outer function when used as the input $\lim\limits_{n \to \infty} a_n = L$ then $\lim\limits_{n \to \infty} f(a_n) = f(L)$.

A series is the sum of an infinite set of numbers $\sum_{n = 1}^{\infty} a_n$. A series can be decomposed into its partial sums which are the incremental sums of the series and defined as a sequence $\{s_n\} = \{\{s_1 = a_1\}, \{s_2 = a_1 + a_2\} ... \{s_n\}\}$. When the limit is taken of this partial sum sequence $\lim\limits_{n \to \infty} s_n = s$ and this limit exists and is finite the series converges to that limit $\sum_{n = 1}^{\infty} a_n = s$ and $s$ is the sum of the series.

A geometric series is defined as $\sum_{n = 1}^{\infty} ar^{n-1}$ where $a \ne 0$ and $a$ is the first term in the series and $r$ is a ratio. When the partial sum sequence $s_n$ is multiplied by $r$ and the difference is taken $s_n - rs_n = a - ar^n$ and when $|r| < 1 \rightarrow \lim\limits_{n \to \infty} r^n = 0$ so simplifying and solving for $s_n = \frac{a}{1 - r}$ and taking the limit gives the sum of the series $\lim\limits_{n \to \infty} s_n = \frac{a}{1 - r} = s$ otherwise the series is divergent.

A p series is a series in the form $\sum \frac{1}{n^p}$ and is divergent when $p \ge 1$ and convergent when $p < 1$. The harmonic series $\sum \frac{1}{n}$ is a well known p series.

The divergence test determines if a series is divergent by taking the limit of the sequence in the series $\lim\limits_{n \to \infty} a_n = L$ and if $L \ne 0$ then the series $\sum_{n = 1}^{\infty} a_n$ diverges otherwise if $\lim\limits_{n \to \infty} a_n = 0$ then it is inconclusive whether the series converges or diverges.

A series is absolutely convergent if the absolute value of the series is convergent $\sum_{n = 1}^{\infty} |a_n| = convergent$ then $\sum_{n = 1}^{\infty} a_n = convergent$ but is conditionally convergent if $\sum_{n = 1}^{\infty} |a_n| = divergent$ and $\sum_{n = 1}^{\infty} a_n = convergent$.

The ratio test takes into consideration that if each subsequent term is less than the term before it the series will converge similar to a geometric series. This is calculated by $\lim\limits_{n \to \infty} |\frac{a_{n+1}}{a_n}| = L$ and if $L < 1$ the series is convergent if $L > 1$ or $L = \pm \infty$ the series is divergent and if $L = 1$ then the test is inconclusive so the series could be divergent or convergent and more work needs to be done.

The alternating series test takes the sequence of a series $a_n$ and if possible rearranges it in the form $(-1)^n b_n$. If $\lim\limits_{n \to \infty} b_n = 0$ and $b_n$ is decreasing or each term after the previous is less in value then the series $\sum_{n = 1}^{\infty} a_n$ is convergent.

The integral test states that if the integral of the sequence of a series is convergent/divergent then the series is convergent/divergent so if $f(n) = a_n$ then $\int_{k}^{\infty} f(n)dn$ if convergent or divergent then $\sum a_n$ will be the same.

Root test states that for a series if $\lim\limits_{n \to \infty} \sqrt{|a_n|} = L$ then if $L < 1$ series is absolutely convergent $L > 1$ divergent and $L = 1$ it is inconclusive and the series could be convergent or divergent.

A power series is defined $\sum_{n = 0}^{\infty} c_n(x - a)^n$ which expanded $c_0 + c_1(x - a)^1 + c_2(x - a)^2 + c_3(x - a)^3 ...$ where $a$ and $c_n$ are real numbers $x$ is a variable where $c_n$ is the coefficient and $a$ is the center with the value of $x$ determines if the series diverges or converges. The interval of convergence is the interval of the value of $x$ that will make the series converge. Radius of convergence (R) is the distance from the center of the interval of convergence to the boundary of a series. 
There are three cases of convergence:
1. Converges for all values of $x$ and the radius of convergence $R = \infty$ and interval $(-\infty, \infty)$.
2. Converges withing set interval where radius of convergence $R > 0$ and if $|x - a| < R$ the series diverges and $|x - a| > R$ the series converges.
3. Converges for one value $x = a$ and $R = 0$ with interval $I = (a)$ since its a single point.

Since a geometric series $\sum_{n = 0}^{\infty} ar^n$ converges when $|r| < 1$ and is equal to $\frac{a}{1 - r}$ if $a = 1$ and $x = r$ then $\sum_{n = 0}^{\infty} x^n = \frac{1}{1 - x}$ for $|x| < 1$. Other functions can manipulated into the form of another function with a known power series which can then either have constant multiples factored out or variables replaced such as $\frac{1}{1 - 25x^2}$ has a similar forms to $\frac{1}{1 - x}$ so the equivalent series can just have the variable replaced $\frac{1}{1 - 25x^2} = \sum_{n = 0}^{\infty} (25x^2)^n$ but the radius and interval will have to be reevaluated as well so instead of $|x| < 1$ the $x$ is replaced as well for this condition and solved so $|25x^2| < 1$  is $|x| < 5$ with $R=5$.

Power series also can be integrated or differentiated to find the functional representation or the function to find a power series. When either operation is done the radius of convergence remains the same but the interval may change.

Coefficients of a power series can be found by continuously taking the derivative of the series when $x = a$ which will cancel out all succeeding terms and leave the coefficient of the same degree as the amount of compounding derivative. This gives the formula $c_n = \frac{f^{(n)}(a)}{n!}$ for the $n^{th}$ coefficient. The Taylor series uses this formula to derive a power series at or around $a$ for a given function $f(x) = \sum_{n = 0}^{\infty} \frac{f^{(n)}(a)}{n!} (x - a)^n$. A Maclaurin series is a Taylor series but $a = 0$ so $f(x) = \sum_{n = 0}^{\infty} \frac{f^{(n)}(0)}{n!} x^n$ where some common functions have a given series $e^x = \sum_{n = 0}^{\infty} \frac{x^n}{n!}$, $sin(x) = \sum_{n = 0}^{\infty} \frac{(-1)^n x^{2n + 1}}{(2n + 1)!}$ and $cos(x) = \sum_{n = 0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$. If a function can be represented by a power series about $a$ then that function is equal to the sum of its Taylor series but there are exceptions where a function does not equal the sum. Taylor polynomials are the partial sums of a Taylor series and can be represented by $T(a)$ where a is the degree of the polynomial. If a polynomial only has whole number positive integers exponents then the sum of the Taylor series will be the polynomial itself since each subsequent derivative will eventually make the polynomial 0.

The binomial theorem states that for $n > 0$ and is a whole number the $n^{th}$ degree term of the binomial power can be found by $(a + b)^n = \sum_{i = 0}^{n} \binom{n}{i} a^{n - 1}b^i$ where $\binom{n}{i} = \frac{n(n - 1)(n - 2) ... (n - i + 1)}{i!}$ and $\binom{n}{0} = 1$.  The binomial series $(1 + x)^k = \sum_{n = 0}^{\infty} \binom{k}{n} x^n$ where $k$ can be any number and $|x| < 1$ also $\binom{k}{n} = \frac{k(k - 1)(k - 2) ... (k - n + 1)}{n!}$ and this can be used for exponent values that are not positive whole numbers.




---
## Links

- [[Mathematical Limits]]
- [[Calculus]]
---

## Source

- 