20260622-0212
# Integral and Antiderivatives

## Notes

F(x) is an antiderivative of f(x) over the interval I if $F'(x) = f(x)$ for all x in I. If F is an antiderivative of f over the interval I then any antiderivative of f is $F + C$ where C is a constant value.

The reverse power rule is the inverse of the power rule of a derivative $\int x^n = \frac{x^{n+1}}{n+1}$.

Antiderivatives like derivatives are linear operations so addition subtraction and constant multiples carry over $f(x) = ag(x) + bh(x)$ then $F(x) = aG(x) + bH(x) + C$.

Riemann sums are used to measure the area under a function and consist of many rectangles called subintervals that have a length which sums to the entire interval and an area of subinterval length times the output of the function at a point in the subinterval.
Riemann Sums formula $\sum^n_{i=1} f(x_i) \Delta x$ where $x_i$ is a point in the subinterval. If f is continuous and non-negative, taking the limit over an interval gives the area under F and above the x-axis for x from a to b $A = \lim\limits_{n \to \infty} \sum^n_{i=1} f(x_i) \Delta x$ where $\Delta x = \frac{b - a}{n}$.
Accumulation is the collective sum of incremented pieces of a whole and can be approximated by a Riemann sum.

A definite integral is defined as $\int_{a}^{b} r(t)dt = \lim\limits_{max(\Delta t, ... \Delta t_n) \to 0} \sum^n_{k=1} r(t^{*}_{k}) \Delta t_k$ where r is integrable and  $max(\Delta t, ... \Delta t_n)$ is the "infinite" slices from $[a, b]$ and $\Delta t = \frac{b - a}{n}$ which can let the limit be set to $n \to \infty$. If r is integrable from a to b then it is also integrable from a to c for any c in $[a,b]$.

The function r over interval $[a,b]$ is piecewise continuous if it has a finite number of discontinuities that are removable or jumps which can make r integrable over the interval if $\Delta t_k = \Delta t$ can be used for $1 \le k \le n$ in the Riemann sum $\int_{a}^{b} r(t)dt = (b-a)\lim\limits_{n \to \infty} (\frac{1}{n} \sum^n_{k=1} r(t^{*}_{k}) \Delta t_k)$.

For any c in the interval $[a,b]$ $\int_{c}^{c} f(v)dv = 0$
Inversion of an integral $\int_{a}^{b} f(v)dv = - \int_{b}^{a} f(v)dv$
For a point c between the interval $[a,b]$ $\int_{a}^{c} f(v)dv + \int_{c}^{b} f(v)dv = \int_{a}^{b} f(v)dv$
The integral of a constant function is the area of a rectangle $A = \int_{a}^{b} kdv = k(b - a)$
The integral of the constant multiple of a function is equal to the constant multiple of the integral of a function $\int_{a}^{b} kf(v)dv = k \int_{a}^{b} f(v)dv$
The integral of a sum or a difference is equal to the sum or a difference of the integrals $\int_{a}^{b} (f(v)dv \pm g(v)) =  \int_{a}^{b} f(v)dv \pm \int_{a}^{b} g(v)dv$
If $f(t) = 0$ for all t in the interval $[a,b]$ then $\int_{a}^{b} f(t)dt = 0$

If $f(r) \ge g(r)$ for all r in $[a.b]$ then $\int_{a}^{b} f(r)dr \ge \int_{a}^{b} g(r)dr$. Bounding a function or finding its range can be found if $m \le f(z) \le M$ for all z in the interval $[a,b]$ then $m(b - a) \le \int_{a}^{b} f(v)dv \le M(b - a)$

The accumulation of the rate of change of a quantity over an interval is the change in quantity on that interval and the rate of change of that accumulation of the quantity is the quantity itself. This helps state the Fundamental Theorem of Calculus which says for a function $f$ that is continuous over the interval $[a,b]$ and for any $x$ in $[a,b]$ if $F(x) = \int_{a}^{x} f(s)ds$ then $F'(x) = f(x)$ for all x over $[a,b]$ and if $G'(x) = f(x)$ for all x in $[a,b]$ then $\int_{a}^{x} f(s)ds = G(x) - G(a)$. This means that the derivative of an integral is equal to the function $\frac{d}{dx} (\int_{a}^{x} f(v)dv) = f(x)$ and the definite integral can be evaluated $\int_{a}^{b} F'(x)dx = F(b) - F(a)$.

The average value theorem finds the average value of a piecewise continuous function $f$ over interval $[a,b]$ is found $f_{avg} = \frac{1}{b-a}(\int_{a}^{b} f(v)dv)$.
The mean value theorem for integrals states that for a continuous function $f$ over the interval $[a,b]$ there is a number $c$ in $(a,b)$ that exists such that $f(c) = f_{avg}$ and can be expressed $\int_{a}^{b} f(s)ds = f(c)(b - a)$.

Every differentiation rule has a corresponding integrable rule.

The substitution rule which corresponds to the chain rule utilizes setting a function to a variable $u = g(x)$ if it is a differentiable and continuous function over the interval $I$. The derivative of the function and the variable of integration is set to the new variable of integration $du = g'(x)dx$ which reverses the chain rule of the original derivation hence $\int f(g(x)) \cdot g'(x)dx = \int f(u)du$. For definite integrals the limits of integration are substituted as well for the values evaluated at the substituted function $\int_a^b f(g(x)) \cdot g'(x)dx = \int_{g(a)}^{g(b)} f(u)du$.

Integration by parts which corresponds to the product rule and is derived by applying the product rule to two functions, taking the integral then setting the original integral equal to the result $\int udv = uv - \int vdu$. Since the second function in the integral is set as the derivative it will be integrated in isolation while the first function will be derived to get the new integral in the result. The $DI$ method involves setting up a table where one function is derived on the left and the second integrated on the right and can happen continuously until the resulting integral is doable.
Integrals of trigonometric functions can be simplified through trig identities. For even pairs of sine and cosine $sin^2x = \frac{1}{2}(1 - cos(2x)$ or $cos^2x = \frac{1}{2}(1 + cos(2x))$ and for odd pairs $sin^2x = 1 - cos^2x$ or $cos^2x = 1 - sin^2x$. For even pairs of tangent and secant $tan^2x = sec^2x - 1$ or $sec^2x = tan^2x + 1$ and for odd pairs isolate $tanxsecx$ from $tan^xxsec^xx$.

Trig substitution can be used for functions mostly radicals where the variable can be substituted for a trig function. Certain functions and patterns are better suited for specific trig function especially in a radical as to cancel out the root. When a trig sub is taken since it is a substitution the derivative must be found for x and multiplied to the function i.e. function $f(x) = 1 - x^2$ and $x = sin\theta$ then $dx = cos\theta d\theta$ so $f(\theta) = (1 - sin^2\theta) \cdot cos\theta d\theta$.  For $\sqrt{a^2 - x^2}$ use $x = asin\theta$ since $1 - sin^2\theta = cos^2\theta$ so $\sqrt{a^2 - a^2sin^2\theta} = acos\theta$. For $\sqrt{a^2 + x^2}$ use $x = atan\theta$ since $1 + tan^2\theta = sec^2\theta$ so $\sqrt{a^2 + a^2tan^2\theta} = asec\theta$. For $\sqrt{x^2 - a^2}$ use $x = asec\theta$ since $sec^2\theta - 1 = tan^2\theta$ so $\sqrt{a^2sec^2\theta - a^2} = atan\theta$.

Partial fraction decomposition is an algebraic technique that can simplify a rational function to make integration easier to do. A rational function $\frac{P(x)}{Q(x)}$ where $Q(x) \ne 0$ can be expressed as partial fractions as long as the numerator's degree is less than the denominator's otherwise the polynomial long division has to be performed. The denominator determines the form in which the partial fractions are decomposed. For distinct linear factors $f(x) = \frac{A}{ax + b}$ where $A$ is a constant. For the repeated product of linear factors $f(x) = \frac{A_1}{ax + b} + \frac{A_2}{(ax + b)^2} ... + \frac{A_k}{(ax + b)^k}$. For irreducible quadratic factors $f(x) = \frac{Ax + B}{ax^2 + bx + c}$ and when repeated $f(x) = \frac{A_1x + B_1}{ax^2 + bx + c} + \frac{A_2x + B_2}{(ax^2 + bx + c)^2} ... +\frac{A_kx + B_k}{(ax^2 + bx + c)^k}$.

Some definite integrals are not possible to evaluate but can be approximated with a Riemann sum. There are four common methods to do a Riemann sum which involve the point that the height of the rectangular segment is evaluated. For the right and left Riemann sums the left or the right point is evaluated for the height and for midpoint Riemann sums the height is $(right \ point + left \ point) / 2$. For the trapezoidal method the height of each segment is $\frac{\Delta x}{2}(left \ point + right point)$ which can be evaluate as the expression $f(x_0) + 2f(x_1) + ... + 2f(x_{n-1}) + f(x_n)$.
The Simpson rule states that a function $f$ can be approximated on each consecutive pairs of intervals by a parabola. The n sub-intervals must be even and the expression for this rule is $\frac{\Delta x}{3}(f(x_0) + 4f(x_1) + 2f(x_2) + ... + 4f(x_{n-1}) + f(x_n))$.
In order of greatest to least margin of error Left & Right > Trapezoid > Midpoint > Simpson. When the amount of intervals are multiplied by k the margin error decreases by a factor depending on the method, left & right by k, trapezoid and midpoint by k<sup>2</sup> and Simpson by k<sup>4</sup>.

Improper integrals have limits of integration that are either not real numbers like infinity or a discontinuity on or between the limits.
To evaluate an improper integral that has $a = \pm \infty \ or \ b = \pm \infty$ the limit that is infinite is set to a variable and the integral is evaluated as a limit with the variable approaching infinity $\int_0^{\infty} e^xdx = \lim\limits_{t \to \infty}(\int_0^t e^xdx)$ and if a is negative infinite $\int_{-\infty}^{0} e^xdx = \lim\limits_{t \to -\infty}(\int_t^0 e^xdx)$. If both limits of integration are infinite then the integral can be evaluated as two separate integrals with an arbitrary but valid mid point and then summated $\int_{\infty}^{\infty} e^xdx = \lim\limits_{t \to \infty}(\int_0^t e^xdx) + \lim\limits_{t \to -\infty}(\int_t^0 e^xdx)$.
For limits that contain a discontinuity the integral can be made into two separate integrals and summated with $c$ being the undefined input and a right or left limit is taken depending on where c is in the limit $\int_{-1}^3 \frac{1}{x}dx = \lim\limits_{t \to 0^-}(\int_{-1}^t \frac{1}{x}dx) + \lim\limits_{t \to 0^+}(\int_t^3 \frac{1}{x}dx)$.
When the limit of an improper integral is a real number it is convergent and when the limit is either infinite or undefined then it is divergent. If an improper integral is evaluated as the summation of separated integrals then if any of those summated integrals are divergent the original integral is divergent.

To evaluate the are of a region bounded by two functions that are continuous and one is always larger than the other in a given interval for all values then the area can be found $A = \int_a^b(f(x) - g(x))dx$ when $f(x) \ge g(x)$ over $[a,b]$. The functions themselves can be evaluated for intersection points to derive an interval that spans that region, and if an interval is given that spans past those intersection points then the integral can be separated into a summation of intervals with the difference of functions having the smaller subtracted from the larger.
Volumes by revolution uses a function graphed on a 2-D plane and rotates its segments from integration around an axis to form a 3-D shape.
The disc method is used for functions that rest on the axis of rotation and treats each integration segment as the radius of a circle which are compounded areas over the interval giving the volume $V = \int_a^b \pi (f(x))^2dx$ where $f(x) = radius$.
The washer method is used when a function does not sit on an axis of rotation and has a region bounded by two functions that are rotated around a given axis. The inner radius squared is subtracted from the outer radius squared to give the radius of the washer shape $A = \int_a^b \pi((outer \ f(x))^2 - (inner \ g(x))^2)dx$.
The cylindrical shell method is used for finding the rotational volume of a function with no inner function or a function that is difficult to invert. The segments are parallel to the axis of rotation and the integral is in respect to the axis of rotation's variable. The cylinders can be flattened to a rectangle with a width of $2 \pi r$ and height of $h$ which the input is the radius $r$ and the height is the function itself $\int_a^b 2\pi rhdx$ if $r = x$ and $h = f(x)$ then  $2\pi \int_a^b xf(x)dx$ when $y = 0$ and $y = f(x)$ and the function is rotated around the y variable $x = 0$. When the area is a region between two functions then the height is the difference between the upper and lower function $2\pi \int_a^b x(f(x) - g(x))dx$ and if there is an offset for the rotational axis the radius is the difference of that offset and x $2\pi \int_a^b (offset - x)f(x)dx$.

The arc length of a function is the measure of the line made by a function. To find the arc length pieced line segments are measured between intermittent points on the function's line and the limit is taken for the amount of points placed to infinity. These segments can be found through the distance formula which using substitution and factoring out $\Delta x$ the formula for arc length is $\int_a^b \sqrt{1 + (f'(x))^2}dx$.

The work done by or to a system with a varying force can be calculated by taking the integral of a force function $F(x)$ where $x = distance$ so $w = F \cdot d = \int_a^b F(x)dx$.


---
## Links

-  [[Calculus]]
- [[Derivative]]
---

## Source

- 