20260613-0134
# Derivative

## Notes

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

The derivative of Euler's number is itself $\frac{d}{dx}(e^x) = e^x$. For other exponentials $\frac{d}{dx}(b^x) = ln(b) \cdot b^x$ , $\frac{d}{dx}(log_a(x)) = \frac{1}{xlog(a)}$ , $\frac{d}{dx}(ln(x)) = \frac{1}{x}$

Logarithmic differentiation is the method of applying the natural log to a function then using logarithmic laws to decouple the complex function. After decomposing the new logarithm and taking the derivative it is important to multiply by the original function as the log is taken on both sides of the equation $f(x) = x^2$ --> $\frac{d}{dx}(ln(f(x))) = \frac{d}{dx}(2lnx)$ --> $\frac{f'(x)}{f(x)} = \frac{2}{x}$ --> $f'(x) = \frac{2}{x} \cdot f(x)$. 

$f$ has an inverse that is differentiable if $f(f^{-1}(a)) \ne 0$ then $f^{-1}$ is differentiable at $a$ and $(f^{-1})'(a) = \frac{1}{f'(f^{-1}(a))}$  

The derivatives of inverse trigonometric functions with the restricted input are
- $\frac{d}{dx}(asin(x)) = \frac{1}{\sqrt{1 - x^2}}$ for $(-1 \lt x \lt 1)$
- $\frac{d}{dx}(acos(x)) = \frac{-1}{\sqrt{1 - x^2}}$ for $(-1 \lt x \lt 1)$
- $\frac{d}{dx}(atan(x)) = \frac{1}{1 + x^2}$ for $(-\infty \lt x \lt \infty)$
- $\frac{d}{dx}(acsc(x)) = \frac{-1}{|x|\sqrt{x^2 - 1}}$ for $(0 , \frac{\pi}{2}] U (\pi, \frac{3\pi}{2}]$
- $\frac{d}{dx}(asec(x)) = \frac{1}{|x|\sqrt{x^2 - 1}}$ for $[0 , \frac{\pi}{2}) U [\pi, \frac{3\pi}{2})$
- $\frac{d}{dx}(acot(x)) = \frac{-1}{1 + x^2}$ for $(0, \pi)$ 

Function $f$ defined over the closed interval $[a,b]$ has a local maximum $c$ in $(a,b)$ if $h \gt 0$ and $(c - h, c + h)$ is contained in $[a,b]$ such that every $x$ value in $(c - h, c + h)$ is $f(c) \ge f(x)$ and $f$ has a local minimum over the same intervals except $f(c) \le f(x)$.
Functions can have many local maxima or minima but only have one global/absolute maximum and minimum over a given interval.

Fermat's theorem states that if $f$ has a local max or min at $x=c$ then $f'(c)$ is either 0 or DNE. For a function $f$ defined over $[a,b]$ $c$ is a critical number if $f'(c)$ = 0 or DNE and $f$ can only have extreme values at critical numbers but critical numbers are not always extreme values. Corollary of Fermat's Theorem is that $f$ attains absolute max and min at critical numbers or endpoints of an interval. $f$ has a global/absolute max over $[a,b]$ and at $c$ if $f(c) \ge f(x)$ for all $x$ in $[a,b]$ and a global/absolute min if $f(c) \le f(x)$. If only one critical number is found over an interval then that extreme is absolute max/min.

Extreme Value Theorem states that $f$ has an absolute max and min over $[a,b]$ for the values $c$ and $d$ where $f(c) = max$ and $f(d) = min$ as long as the interval is closed. This does not ensure that these values are unique or how to find those values.

If $f'(x) \gt 0$ to the left of $c$ and $f'(c) \lt 0$ to the right then $c = max$. If $f'(x) \lt 0$ to the left of $c$ and $f'(c) \gt 0$ to the right then $c = min$. If $f'(x)$ has the same same sign across $c$ then $c \ne min,max$.

Rolle's Theorem states that for a function $f$ that is continuous over $[a,b]$ and differentiable over $(a,b)$ and if $f(b) = f(a)$ then there is a number $c$ between $a$ and $b$ such that $f'(c) = 0$.
Mean Value Theorem (derived from Rolle's Theorem) states that for a function $f$ that is continuous over $[a,b]$ and differentiable over $(a,b)$ then there is a number $c$ between $a$ and $b$ such that $f'(c) = \frac{f(b)-f(a)}{b-a}$ also written $f(b)-f(a) = f'(c)(b-a)$.

First derivative test is if $f'$ goes from negative to positive over a point $c$ then $c = min$ and if $f'$ goes from positive to negative over point $c$ then $c = max$. If $f'$ does not changes signs over $c$ then $c$ is neither a local maximum or minimum.

A function over an interval is considered concave up if it lies above all its tangent lines and concave down is it lies below all its tangent lines. If $f''(x) \gt 0$ for all values $x$ in an interval then the function over that interval is concave up and concave down if $f''(x) \lt 0$

---
## Links

- [[Calculus]]
---

## Source

- 