A [[Binomial distribution]] that for [[random variable]] $X$ describes the number of outcomes in a given interval or specified region.
# Examples
- Distribution for number of phone call a company receives per hour. *($X$ - number of calls. Interval - per hour*
- The number of days a school is closed due to snow storms *($X$ - number of calls. Intervals - days)*
- The number of knots on a segment of a rope
# Poisson Process
1. The number of occurrences in each time interval or region is independent of every other interval. *(No memory)*
2. The [[probability]] that a single outcome will occur during a very short time interval or in a small specified region is proportional to the length of the time interval or the size of the region *(Proportions)*
3. The probability that more than one outcome will occur in such a short time interval or fall in such a small region is negligible.
# Formula
The [[mean]] number of outcomes is computed from $\mu = \lambda t$, where $t$ is "time", "distance", "area", or "volume". No derivation, since it is complicated, so trust me bruv, the formula is: 

$$
p(x; \lambda t) = \dfrac{e^{-\lambda t}(\lambda t)^{x}}{x!}
$$
where $\lambda$ is the average amount of outcomes per unit time, distance, area, or volume.