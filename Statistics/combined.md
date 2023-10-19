$A$ - given hypothesis. $P(H_{i})$ - the
\[\[Probability\|probability\]\] of an event. Formula to find the
\[\[probability\]\] of the hypothesis being fulfilled: $$
P(A) = \sum^n_{i = 1}P(H_{i}) \times P(A |H_{i})
$$ where $n$ - amount of events, $P(A|H_{i})$ - \[\[probability\]\] of
the hypothesis to be fulfilled given the event $P(H_{i})$ \# Bayes'
rule: $$
P(H_{i}|A)=\dfrac{P(H_{i}) \times P(A|H_{i})} {P(A)}
$$ Calculates the \[\[probability\]\] that the hypothesis $A$ was fulled
when the condition $H_{i}$ is met. The \[\[probability\]\] of an event
$H_{i}$ can be calculated by formula (however, usually this probability
is already given in the condition) $$
P(A|H_{i}) = \dfrac{P(A \cap B)}{P(H_{i})}
$$

A \[\[Probability distribution\]\] that has only two outcomes: Success
and Failure \# Rules (Bernoulli process) 1. Must have fixed number of
trials 2. Trials must be independent 3. Every trial must be either a
success or a failure 4. The probability of success remains the same in
all trials \# Random variable \[\[Random variable\]\] $X$ describes the
number of successes. \# Vocab $n$ - number of trials $q$ -
\[\[probability\]\] of failing $p$ - \[\[probability\]\] of getting "x"
successes

# Binomial probability formula

$$
b(x;n,p)_{X} = \dfrac{n!}{(n-x)!x!}\  p^x\  q^{n-x}\ \ \ \ x=0,1,2,\dots,n.
$$

Same as combination formula, but with funky stuff.

# Mean

\[[Mean](#mean)\] for binomial distribution is $$
\mu=np
$$ \# Variance \[\[Variance\]\] for binomial distribution is $$
\sigma^{2}=npq
$$

The probability that any \[\[random variable\]\] $X$ will assume a value
within $k$ \[\[standard deviation\|standard deviations\]\] of the
\[[mean](#mean)\] is at least $1-\dfrac{1}{k^{2}}$. $$
P(\mu-k\sigma<X<\mu+k\sigma)\geq 1-\dfrac{1}{k^{2}}
$$

Covariance shows the connection between two \[\[Random variable\|random
variables\]\] in the same \[\[Joint probability\]\], how they
\[\[Variance\|vary\]\]. \# Discrete case $$
\sigma_{XY}=\sum_{x}\sum_{y}(x-\mu_{X})(y-\mu_{Y})f(x,y)
$$ \# Continuous case $$
\sigma_{XY}=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}(x-\mu_{X})(y-\mu_{Y})f(x,y)\, dx\, dy
$$ where $\mu$ is a \[[mean](#mean)\] of a variable.

If covariance is positive, then as $X$ values change, so do values of
$Y$. If the variance is negative, $X$ and $Y$ values change in opposite
direction

A cumulative distribution function (CDF) is a function that describes
the \[\[probability\]\] that a \[\[random variable\]\] takes on a value
less than or equal to a given value. For a continuous \[\[random
variable\]\], the CDF is the integral of the \[\[Probability
distribution\|probability density function\]\] from negative infinity up
to the value of $x$: $$
\int_{-\infty}^{x} f(x) \, dx = c(x)
$$

# Definition

\[\[Vocab#\^a5bf63\|Data\]\] - any observations that have been collected
**Data** must be **\[\[Randomness\|random\]\]** to avoid **bias**. Data
can be ordered into \[\[Frequency distribution\|frequency
distributions\]\]. \# Two types of data \## Qualitative (or categorical)
Data that is not numeric (color, gender, religion, race, **zip code**,
etc.) Mathematical operation on such data **makes no sense**. \##
Quantitative Data that is numerical (age, height, weight, wages,
temperature etc.) Math operations are **meaningful**. \### Types of
quantitative data \#### Discrete Data that is countable or finite (eggs,
dice, etc.) \#### Continuous Data cannot be counted and is infinite
(height, length, etc.)

# Characteristics

## \[[Mean](#mean)\]

## \[\[Variance\]\]

## \[\[Standard deviation\]\]

## \[\[Covariance\]\]

A list of values and corresponding frequencies. Similar to
\[\[Probability distribution\|probability distribution\]\]. These can be
plotted with \[\[Histogram\|histograms\]\]. \# Class width Difference
between two "lower class limits". *Must be a whole number. If not, round
**up***. \## Lower class limit Smallest number belonging to a class. \##
Upper class limit Largest value belonging to a class. \## Class midpoint
$\dfrac{upper+lower}{2}$ \## Class boundaries Used to separate classes
without gaps \# Steps to a FD - Determine \# of classes - Figure out the
class width - $CW = \dfrac{max - min}{\#classes}$ - Ex: min = 18, max =
18, 8 classes. Class width = 3.25, **4** - Start with the smallest
value - Create classes with class width - Fill in the number of samples
that fit a class \# Types of distributions \## Regular Show how much
samples fall into a class. \## Relative $\dfrac{Class\ frec}{n}$ Shows
what portion of all samples fall into a class. \## Cumulative
$C_{i} = v_{i} + C_{i-1}$ Adds sequential classes together.

\[\[Pasted image 20230924202522.png\]\] \# Mean of frequency
distribution \[\[Pasted image 20230924204745.png\]\] Example with
grades: \[\[Pasted image 20230924210407.png\]\] We can calculate an
average grade even if we haven't done all test. Cool!

A special case of \[\[Negative binomial distribution\]\]. If we consider
$k=1$, then we have a probability distribution for a number of trials to
obtain a single success.

# Example

Distribution to get the first head on the $x$'th coin toss: $$
b^{\star}(x;1,p) = pq^{x-1}
$$ So for the 4th coin toss we get: $$
b^{\star}(4;1,\dfrac{1}{2})=\dfrac{1}{2}\times (\dfrac{1}{2})^{3}=\dfrac{1}{16}
$$ Since $k=1$, the formula's signature is reduced to $g(x;p)$.

# Mean

\[[Mean](#mean)\] of a geometric distribution: $$
\mu = \dfrac{1}{p}
$$ \# Variance \[\[Variance\]\] of a geometric distribution: $$
\sigma^{2}=\dfrac{1-p}{p^{2}}
$$

# Touching bar chart

Axis: - `<u>`{=html}Horizontal`</u>`{=html}: Class midpoints or
boundaries - `<u>`{=html}Vertical`</u>`{=html}: Frequency

Or for a \[\[Probability distribution\]\]: Axis: -
`<u>`{=html}Horizontal`</u>`{=html}: Variable X -
`<u>`{=html}Vertical`</u>`{=html}: Probability \# Types of curves \##
Normal \[\[Pasted image 20230924210639.png\]\] \## Skewed right
\[\[Pasted image 20230924210649.png\]\] \## Skewed left \[\[Pasted image
20230924210659.png\]\]

A distribution that is similar to \[\[Binomial distribution\]\], the
only difference is that the trials are not required to be independent.
\# Example A deck of 52 cards. We wish to find 3 red cards out of 5
drawn. We cannot use the binomial distribution, since for it we need to
put back the picked card and reshuffle the deck, which we do not do in
this example. So, the hypergeometric distribution it is.

Let's find the probability of that happening: 1. We need to take 3 red
cards out of 26 available, which is ${26 \choose 3}$ 2. We need to take
2 black cards out of 26 available, which is ${26 \choose 2}$ 3. We need
to draw 5 cards out of 52 available, which is ${52 \choose 3}$ \\1. and
2. must happen at the same time, so we multiply. This the probability of
3 red cards and 2 black cards. Now, we need to divide the number of all
possible combinations on 5 cards, which is 3. So: $$
\dfrac{{26 \choose 3} {26 \choose {2}}}{52 \choose 3} = \dfrac{26!/3!23!)(26!/2!24!}{52!/5!47!} = 0.3251
$$

\[\[Probability distribution\]\] might depend on more than 1 variable.
In that case, this is a joint probability function.

Example: $$
f(x, y) =
\begin{cases}
24xy,\ \ 0 \leq x \leq 1,\ 0 \leq y \leq 1,\ x + y \leq 1, \\
0,\ \ \ \ \ \ \ \ elsewhere
\end{cases}
$$

To find a \[\[probability\]\], take an integral over interval as many
interval as there are variables. In this case, we would need to take a
double integral.

# Marginal distributions

To find only the density function of one of the variables, take the
integral over every variable, except the target one. Take the task
restrictions into consideration. \# Checking independence Checking for
independency (continuous case): if $f(x,y) = g(x) * h(y)$, this JPDF is
independent.

Mean of a \[\[random variable\]\] in a \[\[probability distribution\]\].
Sometimes called expected value. This is an average expected value in a
given dataset. \# Discrete case $$
\mu = E(X)=\sum_{x}xf(x)
$$ \# Continuous case $$
\mu = E(X) = \int_{-\infty}^{\infty}  xf(x)\, dx 
$$

Natural zero - if one has zero of something, that means they **have none
of** that qualitative category. \# Four levels of measurement \##
Nominal Categories **are not ordered** (religion, gender, etc.). Similar
to \[\[Data\|qualitative data\]\] \## Ordinal Categories **are
ordered**, however **differences are meaningless** (Eg. drivers in a
race. Numbers cannot be subtracted to get new information, since
everything can be derived from order) \## Interval Categories **are
ordered**, **differences are meaningful**, but a **natural zero does not
exist** (temperature in Celsius, Fahrenheit, charge) \## Ratio
Categories **are ordered**, **differences are meaningful**, **natural
zero exists** (money in a bank account)

A \[\[Binomial distribution\]\], but the experiment is repeated until a
*fixed number of successes* occur. We are looking to land on a success
after $k$'th success after $x$ trials. \# Random variable \[\[Random
variable\]\] $X$ of this distribution is a number of trials to get $k$
successes. \# Formula $$
b^{\star}(x;k,p) = {x-1 \choose k-1}p^{k}q^{x-k}
$$

# \[\[Binomial distribution#Mean\|Mean\]\]

# \[\[Binomial distribution#Variance\|Variance\]\]

# Observations

Measures specific traits and does not modify subjects. \# Experiments
Apply a treatment to subjects and measure the effect on subjects.

Observations and experiments must be \[\[Randomness\|random\]\].

Also called just probability density function. Describes the probability
of values of a \[\[random variable\]\] occurring in an experiment.

# Example

For a given \[\[random variable\]\] $X$: $$
f(x) =
\begin{cases}
x,\ \ \ \ \ \ \ \ \ 0 < x < 1  \\
2-x,\ \  1 \leq x < 2  \\
0,\ \ \ \ \ \ \ \ \ \  elsewhere
\end{cases}
$$ It describes the probability of a given value. Often, the function is
defined in segments. NB! $X$ is a `<u>`{=html}random
variable`</u>`{=html}, while $x$ is `<u>`{=html}variable of a
function`</u>`{=html}. We technically plug $X$ in $x$.

To find a \[\[Probability\|probability\]\], take an integral over
interval $[a, b]$ $$
P(a\leq x\leq b) = \int ^{b}_{a} f(x) \, dx 
$$ The sum of all probabilities should be 1. For a continuous $X$, $$
\int_{-\infty}^{\infty} f(x) \, dx = 1
$$ \# PDF, CDF, PMF \## PDF Probability density function. Describes the
behavior of a \[\[Data#Continuous\|continuous\]\] random variable. \##
PMF Probability mass function. Describes the behavior of a
\[\[Data#Discrete\|discrete\]\] random variable. \## CDF Cumulative
density function. Shows the probability that $X$ will take a value less
than or equal to $x$. \### Discrete case Constructed by adding the
previous value to the current one \### Continuous case Constructed by
taking the integral of PDF with respect to $t$

Chance that any given event occurs \# Types of probabilities \##
Observed Probability that is estimated based on observations $$
P(A) = \dfrac{\#times\ A\ occured}{\#times\ procedure\ executed}
$$ \## Classical Probability based on the chance of an event occurring
$$
P(A) = \dfrac{\#\ ways\ A\ could\ occur}{\#\ simple\ events}
$$ \## Subjective Some estimate based on a guess.

# Complementary events

Events that cannot happen at the same time (mutually exclusive)

A probability space is a triplet $(\Omega,F, P)$, where $\Omega$ is a
set of outcomes, $F$ is a set of events, and $P:F\to[0,1]$ is function
that assigns \[\[Probability\|probabilities\]\] to events.

------------------------------------------------------------------------

------------------------------------------------------------------------

Every member of a \[\[Vocab#\^bcc47c\|population\]\] has an equal chance
of being selected into a \[\[Vocab#\^efd78b\|sample\]\]. \# Simple
random sample Each group of size $n$ has an equal change of being
selected.

A random variable $X$ is a function that associates a real number with
each element in the \[\[Probability space\|sample space\]\]. \#
Difference between X and x in f(x) The $X$ is a random variable. It is
the thing that changes values, iterates over every value in the the
sample space. The $x$ in $f(x)$ is a "constant" variable. Random
variable $X$ takes on a value, and for each $X$ exists some value
$f(X=x)$ that describes the probability of $X$ occuring. \# Example In
the case of tossing a coin three times, the variable $X$, representing
the number of heads, assumes value 2 with probability $\dfrac{3}{8}$,
since 3 of the 8 equally likely sample points result in two heads and
one tail (only 3 out of 8 possibilities have 2 heads and 1 tail).

# Common sampling techniques

Used to achieve a \[\[Randomness#Simple random sample\|simple random
sample\]\]. \## Convenience sampling **!!!Not random!!!** Members of a
population are selected by convenience (close friends in a group, etc.)
\## Systematic sampling Put population in order and select every $k$'th
member. \## Stratified sampling Break a population into subgroups based
on some characteristic and take some members from each subgroup. \##
Cluster sampling Break a population into subgroups (clusters) randomly
(no characteristic is used) and randomly selected a number of clusters
(like systematic sampling, but with clusters).

How much each data point varies from the closest data points. A
**positive** square root of \[\[variance\]\]. \# Discrete case $$
\sigma = \sqrt{ E[(X-\mu)^{2}]}=\sqrt{ \sum_{x}(x-\mu)^{2}f(x)  }
$$ \# Continuous case $$
\sigma = \sqrt{ E[(X-\mu)^{2}]}=\sqrt{ \int_{-\infty}^{\infty} (x-\mu)^{2}f(x) \, dx }
$$ where $\mu$ is the \[[mean](#mean)\].

How much each point varies from the \[[mean](#mean)\]. Describes the
variability in the \[\[Probability distribution\]\] \# Discrete case $$
\sigma^{2} = E[(X-\mu)^{2}]=\sum_{x}(x-\mu)^{2}f(x)
$$ \# Continuous case $$
\sigma^{2} = E[(X-\mu)^{2}]=\int_{-\infty}^{\infty} (x-\mu)^{2}f(x) \, dx 
$$ where $E(x)$ is the \[[mean](#mean)\].

-   Data - any observations that have been collected \^a5bf63
-   Statistics - collecting, analyzing, summarizing, **interpreting**,
    and **draw conclusions** from data.
-   Population - complete set of elements that are being studied
    \^bcc47c
-   Sample - a subset of a population \^efd78b
-   Census - collecting data from every element of a population
-   Parameter - characteristic of a population
-   Statistic - a characteristic of a sample
-   Event - collection of outcomes of a procedure
    -   Simple event - one single specific example
-   Sample space - all simple events (every possible outcome)
