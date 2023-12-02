A [[normal distribution]] that has $\mu = 0$ and $\sigma = 1$. The reason for this distribution to exists is to simplify the computation of probabilities for other normal distributions. Instead of taking the integral for every different normal distribution, we can safely transform them to a standard one:
$$
Z = \dfrac{X - \mu}{\sigma}
$$
where $X$ is the normal random variable of the original distribution, and $Z$ is the random variable of SND.
![[Pasted image 20231201202113.png]]
Since all the values of $X$ falling between $x_{1}$ and $x_{2}$ have corresponding $z$ values between
$z_{1}$ and $z_{2}$, the area under the $X$-curve between the ordinates $x = x_{1}$ and $x = x_{2}$ in Figure 6.8 equals the area under the $Z$-curve between the transformed ordinates $z = z_{1}$ and $z = z_{2}$. Cool!

Now we compute a single table for many different values of $Z$.