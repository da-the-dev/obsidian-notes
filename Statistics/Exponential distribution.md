A special case of [[Gamma distribution]], where $\alpha=1$:
$$
f(x;\beta) = \begin{cases}
\dfrac{1}{\beta}e^{-x/\beta}, & x>0 \\
0, & elsewhere
\end{cases}
$$
where $\beta>0$
# Mean
The [[mean]]:
$$
\mu = \beta
$$
# Variance
The [[variance]]:
$$
\sigma^{2} = \beta^{2}
$$
# Relation to Poisson process
Exponential distribution is tightly connected to the [[Poisson distribution]]. The [[random variable]] of [[Poisson distribution]] describes the number of outcomes in a given space or time span. Now say we instead need to compute the *time before the first outcome*. In this case, the Poisson distribution would give:
$$
p(0; \lambda t)=\dfrac{e^{-\lambda t}(\lambda t)}{0!}=e^{-\lambda t}
$$
Now if we make $X$ mean the time to the first Poisson even we can say:
$$
P(X>x)=e^{-\lambda x}
$$
which means "what is the chance that the time for the first Poisson event is longer than $x$". The [[Probability distribution#CDF|cumulative distribution]] is:
$$
P(0\leq X\leq x) = 1-e^{-\lambda x}
$$
Now, remember that [[Probability distribution#CDF|CDF]] is an integral of [[Probability distribution#PDF|PDF]]? Therefore, if we take the derivative of the above by $\lambda$:
$$
f(x)=\lambda e^{-\lambda x}
$$
which is the exponential distribution with $\lambda=\dfrac{1}{\beta}$. Daym!
