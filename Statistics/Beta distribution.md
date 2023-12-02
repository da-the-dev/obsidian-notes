An extension to the [[Continuous uniform distribution]]. 
A **beta function**
$$
B(\alpha, \beta)=\int ^{1} _{0} x^{\alpha-1}(1-x)^{\beta-1} \, dx =\dfrac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta
)}
$$
![[Gamma function#^6cabca]]
Distribution:
$$
f(x)=\begin{cases}
\dfrac{1}{B(\alpha, \beta)}x^{\alpha-1}(1-x)^{\beta-1}, & 0 < x < 1, \\
0, & elsewhere
\end{cases}
$$
[[Continuous uniform distribution]] is beta distribution with $\alpha=1$ and $\beta = 1$
# Mean
The [[mean]]:
$$
\mu = \dfrac{\alpha}{\alpha+\beta}
$$
# Variance
The [[variance]]:
$$
\sigma^{2}=\dfrac{\alpha\beta}{(\alpha+\beta)^{2}(\alpha+\beta+1)}
$$