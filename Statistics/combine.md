 [[Probability distribution|probability distribution]] that has only two outcome: Success and Failure
# Rules
1. Must have fixed number of trials
2. Trials must be independent
3. Every trial must be either a success or a failure
4. The probability of success remains the same in all trials
# Vocab
$n$ - number of trials
$p$ - probability of success in a single trial
$q$ - probability of failing
$x$ - number of success that occur in $n$ trials
$P(x)$ - probability of getting "x" successes

# Binomial probability formula
$$
P(x) = \dfrac{n!}{(n-x)!x!}\  P^x\  q^{n-x}
$$
Same as combination formula, but with funky stuff. # Definition 
[[Vocab#^a5bf63|Data]] - any observations that have been collected
**Data** must be **[[Randomness|random]]** to avoid **bias**.
Data can be ordered into [[Frequency distribution|frequency distributions]].
# Two types of data
## Qualitative (or categorical)
Data that is not numeric (color, gender, religion, race, **zip code**, etc.)
Mathematical operation on such data **makes no sense**.
## Quantitative
Data that is numerical (age, height, weight, wages, temperature etc.)
Math operations are **meaningful**.
### Types of quantitative  data
#### Discrete
Data that is countable or finite (eggs, dice, etc.)
#### Continuous
Data cannot be counted and is infinite (height, length, etc.)
# Characteristics
## Center
Center is "the middle" of the dataset.
### Types
#### Mean
Arithmetical average.
It *is* affected by [[Outliers|outliers]].

$\Sigma$ - a sum
$x$ - value of data
$n$ - # of items in a [[Vocab#^efd78b|sample]].
$N$ - # of items in a [[Vocab#^bcc47c|population]].
$\bar{X}$ - sample mean. $\bar{X}=\dfrac{\Sigma x}{n}$
$\mu$ - population mean. $\mu = \dfrac{\Sigma x}{N}$


#### Median
A true middle of a dataset.
*Data must be in order*
It *is not* affected by outliers

Find the middle value:
- Odd number of values:
	- Median is the middle value:
	- 1 2 3 **4** 5 6 7
- Even number of values:
	- Take the mean of two middle values:
	- 1 2 **3 4** 5 6. Median is $\dfrac{3+4}{2}=3.5$
## Variation
How the data is spread apart. 

**Ways to measure variation:**
### Range
$max - min=range$
Pros:
- Easy to find
Cons:
- Doesn't take into account all values

## Distribution
## Outliers
## Changes over time
A list of values and corresponding frequencies.
These can be plotted with [[Histogram|histograms]].
# Class width
Difference between two "lower class limits". *Must be a whole number. If not, round **up***.
## Lower class limit
Smallest number belonging to a class.
## Upper class limit
Largest value belonging to a class.
## Class midpoint
$\dfrac{upper+lower}{2}$
## Class boundaries
Used to separate classes without gaps
# Steps to a FD
- Determine # of classes
- Figure out the class width
	- $CW = \dfrac{max - min}{\#classes}$
	- Ex: min = 18, max = 18, 8 classes. Class width = 3.25, **4**
- Start with the smallest value
- Create classes with class width
- Fill in the number of samples that fit a class
# Types of distributions
## Regular
Show how much samples fall into a class.
## Relative
$\dfrac{Class\ frec}{n}$
Shows what portion of all samples fall into a class.
## Cumulative
$C_{i} = v_{i} + C_{i-1}$
Adds sequential classes together.

![[Pasted image 20230924202522.png]]
# Mean of frequency distribution
![[Pasted image 20230924204745.png]]
Example with grades:
![[Pasted image 20230924210407.png]]
We can calculate an average grade even if we haven't done all test. Cool!
# Touching bar chart
Axis:
- <u>Horizontal</u>: Class midpoints or boundaries
- <u>Vertical</u>: Frequency

Or for a [[Probability distribution]]:
Axis:
- <u>Horizontal</u>: Variable X
- <u>Vertical</u>: Probability
# Types of curves
## Normal
![[Pasted image 20230924210639.png]]
## Skewed right
![[Pasted image 20230924210649.png]]
## Skewed left
![[Pasted image 20230924210659.png]]Natural zero - if one has zero of something, that means they **have none of** that qualitative category.
# Four levels of measurement
## Nominal
Categories **are not ordered** (religion, gender, etc.). Similar to [[Data|qualitative data]]
## Ordinal
Categories **are ordered**, however **differences are meaningless** (Eg. drivers in a race. Numbers cannot be subtracted to get new information, since everything can be derived from order)
## Interval
Categories **are ordered**, **differences are meaningful**, but a **natural zero does not exist** (temperature in Celsius, Fahrenheit, charge)
## Ratio
Categories **are ordered**, **differences are meaningful**, **natural zero exists** (money in a bank account)# Observations
Measures specific traits and does not modify subjects.
# Experiments
Apply a treatment to subjects and measure the effect on subjects.

Observations and experiments must be [[Randomness|random]].A table that gives the [[Probability|probability]] for each value of a random variable.
Example for a die:
![[Pasted image 20230926135746.png]]

Example for a weighted die:
![[Pasted image 20230926135957.png]]
# Random variable
A variable, x, that has a value for each outcome of a procedure that is determined by chance.

Random variables can be [[Data#Continuous|discrete]] and [[Data#Continuous|continuous]].
# Mean
Also called expected value
$\mu = \Sigma[x*P(x)]$
# Variance
How much each data point varies from the mean
$\sigma^{2}=\Sigma[x^{2}*P(x)] - \mu^{2}$
# Standard deviation
How much each data point varies from the closest data points
$\sigma = \sqrt{ \Sigma[x^{2}*P(x)] - \mu^{2} }$
# Usual vs unusual
Values are <u>unusual</u> if the lie outside of $[\mu - 2\sigma, \mu+2\sigma]$  Chance that any given event occurs
# Types of probabilities
## Observed
Probability that is estimated based on observations
$$
P(A) = \dfrac{\#times\ A\ occured}{\#times\ procedure\ executed}
$$
## Classical
Probability based on the chance of an event occurring
$$
P(A) = \dfrac{\#\ ways\ A\ could\ occur}{\#\ simple\ events}
$$
## Subjective
Some estimate based on a guess.

# Complementary events
Events that cannot happen at the same time (mutually exclusive)
---

---
Every member of a [[Vocab#^bcc47c|population]] has an equal chance of being selected into a [[Vocab#^efd78b|sample]].
# Simple random sample
Each group of size $n$ has an equal change of being selected.


# Common sampling techniques
Used to achieve a [[Randomness#Simple random sample|simple random sample]].
## Convenience sampling
**!!!Not random!!!** 
Members of a population are selected by convenience (close friends in a group, etc.)
## Systematic sampling
Put population in order and select every $k$'th member.
## Stratified sampling
Break a population into subgroups based on some characteristic and take some members from each subgroup.
## Cluster sampling
Break a population into subgroups (clusters) randomly (no characteristic is used) and randomly selected a number of clusters (like systematic sampling, but with clusters).


- Data - any observations that have been collected ^a5bf63
- Statistics - collecting, analyzing, summarizing, **interpreting**, and **draw conclusions** from data.
- Population - complete set of elements that are being studied ^bcc47c
- Sample - a subset of a population ^efd78b
- Census - collecting data from every element of a population 
- Parameter - characteristic of a population
- Statistic - a characteristic of a sample
- Event - collection of outcomes of a procedure
	- Simple event - one single specific example
- Sample space - all simple events (every possible outcome)
