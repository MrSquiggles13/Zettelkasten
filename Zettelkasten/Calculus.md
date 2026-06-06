20260602-2233
# Calculus

## Notes

### Limits

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
### Derivatives

Differentiation is the process of calculating a derivative. A derivative is the instantaneous rate of change of a function at a point.

The forward instantaneous rate of change of function $f$ at $c$ is $\lim\limits_{h \to 0^{+}} \frac{f(c+h) - f(c)}{h}$ if this limit exists.
The backward instantaneous rate of change of function $f$ at $c$ is $\lim\limits_{h \to 0^{-}} \frac{f(c+h) - f(c)}{h}$ if this limit exists and can also be written as $\lim\limits_{s \to 0^{+}} \frac{f(c) - f(c - s)}{s}$

Given a function $f$ defined over the interval $(a,b)$ the instantaneous rate of change at $c$ in the interval $(a,b)$ is the value of the forward and backward instantaneous rate of change at $c$ if they both exist and are equal. The derivative of $f$ at $c$ notated $f'(c)$ is the instantaneous rate of change at $c$ $f'(c) = \lim\limits_{h \to 0} \frac{f(c+h) - f(c)}{h}$. So $f$ is differentiable if $f$ and $c$ defined over the interval $(a,b)$ and $f'(c)$ exists and is finite.

Common graphical no differentiable points are holes in the graph, sharp corner or turns, and vertical slopes.

Definition of a derivative for a function $f$ at $x = a$ $f'(c) = \lim\limits_{h \to 0} \frac{f(c+h) - f(c)}{h}$ must exist and with $x = a + h$ we can rewrite the limit $f'(c) = \lim\limits_{x \to a} \frac{f(x) - f(a)}{x - a}$. A function is differentiable over an interval $(a,b)$ if $f'(a)$ exists and is differentiable at every number over the interval. If $f$ is differentiable at $a$ then it is continuous at $a$ but if a function is continuous at $a$ that does not imply it is differentiable at $a$.

The notations for a derivative are $f'(x)$ $\frac{d}{dx}$ $Df(x)$. Higher order derivatives are derivatives of a function taken multiple times $f'''(x)$ or $\frac{d}{dx}(\frac{d}{dx}(\frac{d}{dx}(f(x))))$ or $f^{(3)}(x)$ 

The derivative of a constant is always zero $\frac{d}{dx}(C) = 0$ where $C =$ any constant.  
A derivative of a sum is equal to the sum of the derivatives $\frac{d}{dx}(x^{2} + x) = \frac{d}{dx}(x^{2}) + \frac{d}{dx}(x)$.
A derivative of a difference is equal to the difference of the derivatives $\frac{d}{dx}(x^{2} - x) = \frac{d}{dx}(x^{2}) - \frac{d}{dx}(x)$.
A constant multiple of a function in a derivative is equal to that constant multiple of the derivative of the function $\frac{d}{dx}(3(x + 2)) = 3\frac{d}{dx}(x + 2)$
Taking a derivative is a linear operation which is why summation difference and constant multiple are respected between differentiation.

An equation of the tangent line to the graph of $y = f(x)$ at the point $(a, f(a))$ is $y - f(a) = f'(a)(x - a)$ or $y - y_1 = m(x - x_1)$.

The average rate of change of position with respect to time is called the average velocity. So if $s(t)$ is the position then the velocity is $s'(t) = v(t)$ and the acceleration is $s''(t) = v'(t) = a(t)$.

The power rule states that $\frac{d}{dx}(x^{n}) = nx^{n-1}$
The product rule states that if $f$ and $g$ are differentiable then $\frac{d}{dx}(f(x) \cdot g(x)) = f(x)g'(x) + g(x)f'(x)$
The quotient rule states that if $f$ and $g$ are differentiable then $\frac{d}{dx}(\frac{f(x)}{g(x)}) = \frac{g(x)f'(x) - g'(x)f(x)}{(g(x))^{2}}$
The chain rule states that when there is function composition $f(g(x))$ and set $F(x) = (f \cdot g)(x) = f(g(x))$ then F is differentiable by $F'(x) = g'(x) \cdot f'(g(x))$.

Derivatives of common trigonometric functions
- $\frac{d}{dx}(sin(x)) = cos(x)$
- $\frac{d}{dx}(cos(x)) = -sin(x)$
- $\frac{d}{dx}(tan(x)) = sec^{2}(x)$
- $\frac{d}{dx}(csc(x)) = -csc(x)cot(x)$
- $\frac{d}{dx}(sec(x)) = sec(x)tan(x)$
- $\frac{d}{dx}(cot(x)) = -csc^{2}(x)$
Note: functions starting with co- have a negative output

Implicit differentiation is the process of taking the derivative of a function with multiple variables and more than one cannot be isolated. When taking the derivative of a function with a variable that the derivative is not in respect to the functions variable is calculated through the chain rule as though the variable is a separate function. Implicit differentiation can establish a relationship between two or more variables by the rate of change of one with respect to another.

In find the rates of change two or more variables are dependent on a separate introduced variable (normally time) and calculate how each variable changes with respect to this introduced variable.

Linear approximation is taking a known function and finding a line of tangency on a point then plugging in values close to the wanted point.

Differentials are infinitesimal displacements from a value written as $d + value$ $x: dx$. $dx$ can be considered an independent variable with arbitrary very small values and the relation between differential functions $\frac{dy}{dx}$ can be treated like functions when finding a relation between derivatives.

If $y = f(x)$ and $f$ is differentiable then $dy$ is defined in terms of $dx$ by $dy = f'(x)dx$ which can calculate the displacement of $y$ in terms of $x$.
To calculate errors in measurement approximations we let $dx = x - a$ so that $x = a + dx$ and then using linear approximations $f(x) \approx f'(a)(x - a) + f(a)$ and when $dx = x - a$ is very small $f(a + dx) \approx f(a) + f'(a)dx \approx f(a)dy$ so $dy \approx f(a + dx) - f(a)$ or $\Delta y$

Relative error is the error relative to the theoretical value itself $\frac{\Delta x}{x} = \frac{dx}{x}$ and a percentage can be calculated by taking the relative error and multiplying by 100. Error in measuring $x: dx, y: dy = f'(x)dx$. Relative error in measuring $y: \frac{dy}{y} = \frac{f'(x)dx}{f(x)}$ for percent $\frac{dy}{y} \cdot 100$ 


---
## Links

- [[Mathematics]]
---

## Source

- 