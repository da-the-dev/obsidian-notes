A type of regression used for [[classification]] problems.
We can't really use [[Linear regression]] to reliably tell apart two classes:
![[Pasted image 20240206230059.png]]
# Sigmoid function
To clamp the value between 0 and 1 we can use the <u>logistic</u> or <u>sigmoid function</u> 
$$
\sigma(x) = \dfrac{1}{1 + e^{-x}}
$$
## Single predictor
We can slap [[Linear regression]]'s objective function into the sigmoid function:
$$
\begin{align}
p(x_{1})&=\dfrac{1}{1 + e^{-z}} \\
z&=w_{0}+w_{1}x_{1}
\end{align}
$$
## Multiple predictors
We can do the same with multiple predictors:
$$
\begin{align}
p(\textbf{x})&=\dfrac{1}{1 + e^{-z}} \\
z&=w_{0}+w_{1}x_{1}+\dots+w_{p}w_{p}
\end{align}
$$

We can't use [[MSE]] as the [[loss function]] due to non-linearity of the sigmoid function. It wouldn't be convex anymore. 
# Cross entropy
Cross entropy is the measure of the difference between two probability distributions. In our case, we have distributions:
- $[0, 1]$ — is the truthful one
- $[\alpha, \beta]$ — predicted distribution
$\alpha$ and $\beta$ in this case are probabilities for a label to be in the respective class.
Cross entropy between distributions $t$ and $p$ is defined as:
$$
H(t,p)=-\sum t(i) * \log[p(i)]
$$
where $i$ is indexed over classes
## Some examples
$t = [1,0], p=[0.7, 0.3]$:
$$
\begin{align}
H(t, p) &= -[1 * \log(0.7) + 0 * \log(0.3)] \\
&= -(- 0.35667494 + 0]  \\
&= 0.35667494
\end{align}
$$
$t = [1,0], p=[0.9, 0.1]$:
$$
\begin{align}
H(t, p) &= -[1 * \log(0.7) + 0 * \log(0.3)] \\
&= -(- 0.105360515 + 0]  \\
&= 0.105360515
\end{align}
$$
## Binary Cross-Entropy Loss 
$$
BCEL=-[y * \log(p) + (1-y) * \log(1-p)]
$$
where:
- $y$ is the true label
- $p$ is the predicted possibility of the positive class
# Loss function
All in all, the loss function is:
$$
L(\textbf{w})=-\dfrac{1}{n} \sum_{i=1}^{n} y^{i}\log(p(x_{i}))+(1-y^{i}) \log (1 - p(x^{i}))
$$
We can minimize $\textbf{w}$ with [[Gradient descent]]
## Solution
The gradient:
$$
\dfrac{ \partial L }{ \partial w_{j} } =-\dfrac{1}{n} \sum^{n}_{i=1}(y^{i}-\sigma(z^{i}))x^{i}_{j}
$$
or in other terms
$$
\dfrac{ \partial L }{ \partial w_{j} } =-\dfrac{1}{n} \sum^{n}_{i=1}(p(x^{i})-y^{i})x^{i}_{j}
$$
Thus:
$$
w_{j}=w_{j}-\alpha \dfrac{1}{n} \sum^{n}_{i=1}(p(x^{i})-y^{i})x^{i}_{j}
$$
