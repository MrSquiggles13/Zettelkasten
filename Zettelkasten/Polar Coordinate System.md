20260810-0353
# Polar Coordinate System

## Notes

The polar coordinate system is similar to a cartesian system but there is a pole which is similar to an orientation at the center and a ray that starts at the pole ($O$) called the polar axis.

The polar coordinates for a point $P$ is defined by $(r, \theta)$ where $r$ is the distance from the pole ($O$) to $P$ and $\theta$ is the angle between the polar axis and the terminal line $\overline{ OP}$ where $P$ has infinite coordinates since $(r, \theta) = (r, \theta + 2n\pi)$ unlike the cartesian system. Also $r$ can be negative which is just the opposite direction of its positive counterpart $(-r, \theta) = (r, \theta + \pi)$.

To convert polar coordinates to their cartesian counterpart $P(r, \theta) = P(x, y)$ set $x$ and $y$ to their polar equivalent $x = rcos(\theta)$ $y = rsin(\theta)$. Also cartesian can be converted to polar since $r^2 = x^2 + y^2$ and the angle $tan(\theta) = \frac{y}{x}$ but $\theta = arctan(tan(\frac{y}{x}))$ cannot be assumed and is not implied since the angle must lie in the correct quadrant intended by the original cartesian coordinates that were converted.

The polar equation $r = a$ is a circle centered at the pole with a radius of $|a|$. Polar equation $\theta = b$ is a radial line that goes through the pole and makes angle $b$ with the polar axis. Polar equation $r = \theta$ is a spiral that starts at the pole and extends infinitely outward. When $r = a \cdot cos(\theta)$ then it is a circle with radius $\frac{|a|}{2}$ and is centered at $(\frac{a}{2}, 0)$. When $r = a \cdot sin(\theta)$ then it is a circle with radius $\frac{|a|}{2}$ and is centered at $(0, \frac{a}{2})$. A cardioid is a shape that resembles a heart and forms from the equation $r = n + (a \cdot sin(\theta) \ |or| \ a \cdot cos(\theta))$ where $n = constant$.

To differentiate a polar equation $r = f(\theta)$ first convert to parametric form $x = rcos(\theta) = f(\theta)cos(\theta)$ $y = rsin(\theta) = f(\theta)sin(\theta)$ and use the derivative formula for parametric equations but with $\theta$ $\frac{dy}{dx} = \frac{dy/d\theta}{dx/d\theta}$ where $\frac{dx}{d\theta} = \frac{dr}{d\theta}cos(\theta) - rsin(\theta)$ and $\frac{dy}{d\theta} = \frac{dr}{d\theta}sin(\theta) + rcos(\theta)$ so that $\frac{dy}{dx} = \frac{\frac{dr}{d\theta}sin(\theta) + rcos(\theta)}{\frac{dr}{d\theta}cos(\theta) - rsin(\theta)}$.

A region bounded by a polar function $r = f(\theta)$ and a range $\theta = [a, b]$ can have its area found by summating the area of multiple sectors taken at multiple angles between the range which gives the integral $Area = \frac{1}{2} \int_a^b r^2 d\theta$. A region bounded by two separate polar functions $r = f(\theta)$ and $r = g(\theta)$ where $f(\theta) \ge g(\theta) \ge 0$ and $0 \le b - a \le 2\pi$ has an area equal to $Area = \frac{1}{2} \int_a^b (f(\theta)^2 - g(\theta)^2) d\theta$ where $f(\theta)$ is the outer radius and $g(\theta)$ is the inner radius.

To find the length of the polar curve from a polar equation the formula for the length of a curve for a parametric equation can have its variable substituted for the polar equivalent and simplified to get $L = \int_a^b \sqrt{(\frac{dr}{d\theta})^2 + r^2} d\theta$.

---
## Links

- [[Parametric Equations]]
- [[Integral and Antiderivatives]]
---

## Source

- 