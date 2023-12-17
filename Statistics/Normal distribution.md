The "bell curve" distribution
![[Pasted image 20231201195220.png|500]]
This distribution's formula assumes given [[mean]] and [[variance]]:
$$
n(x; \mu, \sigma) = \dfrac{1}{\sqrt{ 2\pi }\sigma}e^{-\frac{1}{2\sigma^{2}}(x-\mu)^{2}}, -\infty<x<\infty
$$
A [[random variable]] that has a bell curve as the distribution is called a **normal random variable**.
# Normal to binomial
If $X$ is a [[Binomial distribution#Random variable|binomial random variable]] with mean $\mu = np$ and variance $\sigma^{2}=npq$,
then the limiting form of the distribution of:
$$
Z=\dfrac{X-np}{\sqrt{ npq }}
$$
as $n \to \infty$
When $n$ is small and $p$ is reasonably close to $\dfrac{1}{2}$, then:
$$
Z=\dfrac{X+0.5-np}{\sqrt{ npq }}
$$
$0.5$ is a **continuity correction**


