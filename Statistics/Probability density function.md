Also called just density function. It's a function representation of [[Probability distribution]]. PDF for short.

Example:
For a given [[Probability distribution#Random variable|random variable]] $X$:
$$
f(x) =
\begin{cases}
x,\ \ \ \ \ \ \ \ \ 0 < x < 1  \\
2-x,\ \  1 \leq x < 2  \\
0,\ \ \ \ \ \ \ \ \ \  elsewhere
\end{cases}
$$
It describes the probability of a given value. Often, the function is defined in segments.
NB! $X$ is a <u>random variable</u>, while $x$ is <u>variable of a function</u>. We technically plug $X$ in $x$.

To find a probability, take an integral over interval $[a, b]$
$$
P(a\leq x\leq b) = \int ^{b}_{a} f(x) \, dx 
$$
The sum of all probabilities should be 1. For a continuous $X$,
$$
\int_{-\infty}^{\infty} f(x) \, dx = 1
$$
