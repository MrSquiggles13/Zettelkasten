20260613-0133
# Mathematical Limits

## Notes

The limit of a function is the value $L$ that $f(x)$ approaches as $x$ approaches a value $a$ but is not equal to $a$ and is written as $\lim\limits_{x \to a} f(x) = L$. Limits can be one sided and are denoted with a + or - sign in the superscript of the value being approached $\lim\limits_{x \to a^{+}} f(x) = L$ $\lim\limits_{x \to a^{-}} f(x) = L$. A limit only exists if and only if both one sided limits exist and they are equal.

Properties of limits: if $\lim\limits_{x \to a} f(x)$ and $\lim\limits_{x \to a} g(x)$ exist and C is any real number then
- Summation Subtraction rule - $\lim\limits_{x \to a} [f(x) \pm g(x)] = \lim\limits_{x \to a} f(x) \pm \lim\limits_{x \to a} g(x)$
- Constant Multiple - $\lim\limits_{x \to a} [C f(x)] = C \lim\limits_{x \to a} f(x)$ 
- Multiplication Rule - $\lim\limits_{x \to a} [f(x) g(x)] = \lim\limits_{x \to a} f(x) \cdot \lim\limits_{x \to a} g(x)$
- Division Rule - $\lim\limits_{x \to a} [\frac{f(x)}{g(x)}] = \frac{\lim\limits_{x \to a} f(x)}{\lim\limits_{x \to a} g(x)}$ if and only if $\lim\limits_{x \to a} g(x) \ne 0$ 
Limit of a constant is the constant itself and a limit of a function is the functions limit. If limit taken is undefined at the approaching input value then algebraic manipulation is needed to make the value valid otherwise limit does not exist. 

Limits can be similar to function composition where the inner expression can have its limit taken instead of the the whole $\lim\limits_{x \to a} \sqrt[n]{f(x)} = \sqrt[n]{\lim\limits_{x \to a}f(x)}$ 

The Squeeze Theorem states that if $g(x) \leq f(x) \leq h(x)$ near $x = a$ and $\lim\limits_{x \to a} g(x) = L = \lim\limits_{x \to a} h(x)$ then $\lim\limits_{x \to a} f(x) = L$.

For positive infinite limits $\lim\limits_{x \to \infty} f(x) = L$ all output values $f(x)$ are closer to $L$ than any positive number chosen when x is sufficiently large and positive.
For negative infinite limits $\lim\limits_{x \to -\infty} f(x) = L$ all input values $f(x)$ are closer to $L$ than any positive number chosen when x is sufficiently small and negative.
$y = L$ is a horizontal asymptote if L is either of these limits. A function can have two asymptotes, but no more, if both limits are true and they do not equal each other $\lim\limits_{x \to \infty} f(x) = L$ and $\lim\limits_{x \to -\infty} f(x) = M$ but $L \ne M$. 

Infinite limit proof states that for any $\epsilon \gt 0$ there exists $N \gt 0$ such that $x \gt N \Longrightarrow |f(x) - L| \lt \epsilon$ where $\epsilon \gt 0$ is the measure of how close the output is to L and $N \gt 0$ is the measure for how far out the inputs have to be to get an output that is within $\epsilon$. Negative infinite is the same but for $N \lt 0$ that $x \lt N \Longrightarrow |f(x) - L| \lt \epsilon$. Epsilon $\epsilon$ is considered a tolerance for a sufficient limit.

For any $M \gt 0$ there exists $N \gt 0$ such that $x \gt N \Longrightarrow f(x) \gt M$ when $\lim\limits_{x \to +\infty} f(x) = +\infty$ where $f(x)$ is larger than any value $x$ that is very large and positive.
For any $M \gt 0$ there exists $N \gt 0$ such that $x \gt N \Longrightarrow f(x) \lt -M$ when $\lim\limits_{x \to +\infty} f(x) = -\infty$ where $f(x)$ is smaller than any value $x$ that is very large and positive.
For any $M \gt 0$ there exists $N \gt 0$ such that $x \lt -N \Longrightarrow f(x) \gt M$ when $\lim\limits_{x \to -\infty} f(x) = +\infty$ where $f(x)$ is larger than any value $x$ that is very large and negative. 
For any $M \gt 0$ there exists $N \gt 0$ such that $x \gt N \Longrightarrow f(x) \gt M$ when $\lim\limits_{x \to -\infty} f(x) = -\infty$ where $f(x)$ is smaller than any value $x$ that is very large and negative. 

To solve for infinite limits of a quotient with variables in numerator and denominator first try dividing top and bottom by the highest degree variable.

for $\lim\limits_{x \to a} f(x) = +\infty$ $f(x)$ is larger than any value $x$ near $a$ but $x \ne a$ for $N \gt 0$ there is $\delta \gt 0$ such that $0 \lt |x-a| \lt \delta \Longrightarrow f(x) > N$ where $N \gt 0$ is how large the values of $f(x)$ are and $\delta \gt 0$ is how close to $a$ the inputs $x$ have to be.
for $\lim\limits_{x \to a} f(x) = -\infty$ $f(x)$ is smaller than any value $x$ near $a$ but $x \ne a$ for $N \gt 0$ there is $\delta \gt 0$ such that $0 \lt |x-a| \lt \delta \Longrightarrow f(x) > N$ where $N \gt 0$ is how large the values of $f(x)$ are and $\delta \gt 0$ is how close to $a$ the inputs $x$ have to be.
$x = a$ is a vertical asymptote of $f$ if either $\lim\limits_{x \to a} f(x) = +\infty$ or $\lim\limits_{x \to a} f(x) = -\infty$ is true and exists even if only one side of the limit is infinite $x \to a^{+}$ or $x \to a^{-}$. If a function has a vertical asymptote then the function is discontinuous.

Continuity is considered when there are no breaks in a function. Continuity of $f$ at $c$ is local which means it only depends on behavior of $f$ very near $c$ (like a limit) but does not say anything about continuity of other values of $f$.
Let $f$ be a function and $a$ be a value in its domain then $f$ is continuous at $a$ if and only if $\lim\limits_{x \to a} f(x) = f(a)$ which requires that
- $\lim\limits_{x \to a^{+}} f(x)$ exists and is finite
- $\lim\limits_{x \to a^{-}} f(x)$ exists and is finite
- $\lim\limits_{x \to a^{+}} f(x) = \lim\limits_{x \to a^{-}} f(x) = f(a)$
If a point or a limit does not exist at any value $x$ then the function is not continuous. If the left and right limit exist and are equivalent then the function is continuous.
A function is continuous over interval $(a,b)$ if it is continuous at every point and continuous over closed interval $[a,b]$ if continuous at each point over interval $(a,b)$ and is right continuous at $a$ and left continuous at $b$.

Discontinuity cannot be determined if interval is not in a function's domain. If $a$ is in the domain of function $f$ but is not continuous at $a$ or $a$ is not in the domain of $f$ but the intervals $(a-h,a)$ and $(a, a+h)$ are in the domain of $f$ for all $h>0$ then $f$ is discontinuous at $a$.

Types of discontinuity assuming $f$ is discontinuous a $a$
- Removable is when $\lim\limits_{x \to a} f(x) = L$ where $x \in \mathbb{R}$ but $f(a) \ne L$ and by redefining the point $f$ at $a$ so that $f(a) = L$ will remove the discontinuity.
- Jump is when $\lim\limits_{x \to a^{+}} f(x)$ and $\lim\limits_{x \to a^{-}} f(x)$ both exist but do not equal each other.
- Infinite is when $\lim\limits_{x \to a^{+}} f(x)$ and $\lim\limits_{x \to a^{-}} f(x)$ both exist but at least one limit equals infinity.
- Essential is when $\lim\limits_{x \to a^{+}} f(x)$ or $\lim\limits_{x \to a^{-}} f(x)$ do not exist.
Classifying a discontinuity involves specifying the domain and finding the largest interval the is left right and standard continuous. After all points of discontinuity are found a left and right limit is found which will determine what type and have the discontinuity point removed if can.

To find a constant c so a piecewise function is continuous over all real numbers find the limit where the domains meet for each inner function, set them equal to each other and solve for c.

Intermediate Value Theorem (IVT) states that if a function $f$ is continuous over $[a,b]$ and $f(a) \ne f(b)$ and $f(a) \lt f(b)$ or $f(a) \gt f(b)$ and a value $N$ is between $f(a)$ and $f(b)$ $f(a) \lt N \lt f(b)$ or $f(b) \lt N \lt f(a)$ then a value $c$ will be between values $a$ and $b$ $a \lt c \lt b$ so that $f(c) = N$ 

Euler's number is defined by $e = \lim\limits_{x \to 0} (1 + x)^{\frac{1}{x}} \approx 2.71828$

Indeterminate forms are when a limit results in a mathematical expression that has competing extremes such as $\frac{0}{0}$ or $0 \cdot \infty$
L'Hôpital's rule states that if functions $f$ and $g$ are differentiable and $g'(x) \ne 0$ near $a$ except possibly when $x = a$ and $\lim\limits_{x \to a} f(x) = 0$ and $\lim\limits_{x \to a} g(x) = 0$ OR $\lim\limits_{x \to a} f(x) = \pm \infty$ and $\lim\limits_{x \to a} g(x) = \pm \infty$ then $\lim\limits_{x \to a} \frac{f(x)}{g(x)} = \lim\limits_{x \to a} \frac{f'(x)}{g'(x)}$ if the limit on the right exists or is $\pm \infty$. When the conditions are met the original limit $\lim\limits_{x \to a} \frac{f(x)}{g(x)}$ is an indeterminate quotient $\frac{0}{0}$ or $\frac{\pm \infty}{\pm \infty}$.
If a limit results in an indeterminate product ($\lim\limits_{x \to a} f(x)g(x) = 0 \cdot \pm \infty$) one of the functions in the product can be reciprocated and placed in the denominator to make a quotient ($\lim\limits_{x \to a} \frac{f(x)}{\frac{1}{g(x)}}$) which will result in the limit having an indeterminate quotient which can be solved with L'Hôpital's rule.
If a limit results in an indeterminate difference ($\lim\limits_{x \to a} f(x) - g(x) = \infty - \infty$) try find a common factor to make the difference into a product ($\lim\limits_{x \to a} h(x)f(x) - h(x)g(x) = \lim\limits_{x \to a} h(x)(f(x) - g(x))$) then this can be either solved or converted into a quotient and then can apply L'Hôpital's rule.
If a limit results in an indeterminate power ($\lim\limits_{x \to a} f(x)^{g(x)} = (0^0, \pm\infty^0, 1^{\pm\infty})$) then take the natural log of the limit and its result $ln(L) = ln(\lim\limits_{x \to a} f(x)^{g(x)}) = \lim\limits_{x \to a} ln(f(x)^{g(x)})$ Which can be set as a product using the log laws $\lim\limits_{x \to a} g(x)ln(f(x)) = L_1$ which can either be solved or converted to a quotient and applying L'Hôpital's rule but the resulting output will be $ln(L) = L_1$ and will need to cancel out $ln(L)$ by setting both sides to the power of e $e^{ln(L)} = e^{L_1}  = L$. 


---
## Links

- [[Calculus]]
---

## Source

- 