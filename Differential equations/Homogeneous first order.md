Homogeneous FO equations are a type of [[Differential equations]] of the form
$$
M(x,y)dx + N(x,y)dy = 0
$$
Sometimes the these equations are not [[Exact differential#Theorem (The Exactness Condition|exact]] and cannot be solved like usual. However, we can multiply this equation by some integrating factor and solve it.
# Example
$$
(3x + 2y^2)dx + 2xydy = 0
$$
isn't exact
$$
M_{y} = 4y \neq N_{x} = 2y
$$
However, if we multiply by $x$, the equation becomes exact again

# Integrating factor
Let's say that integrating factor is some $\mu(x,y)$.
Then, through the magic of mathematics:

## Theorem
$$
p(x)=\dfrac{My-N_{x}}{N}
$$
If $p(x)$ is independent of $y$