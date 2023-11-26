Also called just probability density function. Describes the probability of values of a [[random variable]] occurring in an experiment.

# Example
For a given [[random variable]] $X$:
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

To find a [[Probability|probability]], take an integral over interval $[a, b]$
$$
P(a\leq x\leq b) = \int ^{b}_{a} f(x) \, dx 
$$
The sum of all probabilities should be 1. For a continuous $X$,
$$
\int_{-\infty}^{\infty} f(x) \, dx = 1
$$
# PDF, CDF, PMF
## PDF
[[Probability]] density function. Describes the behavior of a [[Data#Continuous|continuous]] random variable.
## PMF
[[Probability]] mass function. Describes the behavior of a [[Data#Discrete|discrete]] random variable.
## CDF
Cumulative density function. Shows the probability that $X$ will take a value less than or equal to $x$.
### Discrete case
Constructed by adding the previous value to the current one
### Continuous case
Constructed by taking the integral of PDF with respect to $t$