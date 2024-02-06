# Steps
- Pick a starting value of $w_{i}$
- Compute the [[gradient]] of the loss curve at the starting point
- [[Gradient]] of the curve at any point is equal to the [[derivative]] of the curve at that point
- [[Gradient]] is a [[vector]]. Since we need to reduce loss, we take the negative gradient and follow that instead
- We take a **small step** in the direction of the **negative gradient** 
- Repeat this process until we arrive at a solution

Gradient descent reduces the [[loss function]] iteratively:
$$
\begin{align}
w_{0}&=w_{0}-\alpha \dfrac{ \partial L }{ \partial w_{0} }  \\
w_{1}&=w_{1}-\alpha \dfrac{ \partial L }{ \partial w_{1} } 
\end{align}
$$
where $\alpha$ is the **learning rate** and is a fraction of the magnitude of the negative gradient

If we take the derivatives:
$$
\begin{align}
w_{0}&=w_{0}-\alpha\dfrac{1}{n}\sum^{n}_{i=1}(\hat{y}_{i}-y_{i}) \\
w_{1}&=w_{1}-\alpha\dfrac{1}{n}\sum^{n}_{i=1}(\hat{y}_{i}-y_{i})x_{i} \\
\end{align}
$$
For multiple parameters the general formula would be:
$$
w_{j}=w_{j}-\alpha \dfrac{1}{n} \sum^{n}_{i=1}(\hat{y}_{i}-y_{i})x_{i}^{j}
$$
where $j$ starts at $0$.