[[Probability distribution]] might depend on more than 1 variable. In that case, this is a joint probability function.

Example:
$$
f(x, y) =
\begin{cases}
24xy,\ \ 0 \leq x \leq 1,\ 0 \leq y \leq 1,\ x + y \leq 1, \\
0,\ \ \ \ \ \ \ \ elsewhere
\end{cases}
$$

To find a probability, take an integral over interval as many interval as there are variables. In this case, we would need to take a double integral.

# Marginal distributions
To find only the density function of one of the variables, take the integral over every variable, except the target one. Take the task restrictions into consideration.
# Checking independence
Checking for independency (continuous case): if $f(x,y) = g(x) * h(y)$, this JPDF is independent.