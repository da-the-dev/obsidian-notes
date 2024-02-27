A [[supervised learning]] algorithm that finds or infers a linear correspondence of [[predictors]] to a [[response]]. In general:
$$
y=w_{0}+w_{1}x_{1}+w_{2}x_{2}+\dots+w_{p}x_{p}
$$
# Loss function
To find $w_{0}, w_{1}$, we should use [[MSE]] as our [[loss function]]:
[[MSE]]:
  ![[MSE#^MSE]]
Here $\hat{y}$ is the same as the [[objective function]]:
  $$
\hat{y} = f(x_{i})=w_{0}+w_{1}x_{1}
$$

Then the loss function is:
  $$
L(w_{0}, w_{1})=\dfrac{1}{n}\sum^{n}_{i=1}(y_{i}-(w_{0}+w_{1}x_{i}))^{2}
$$
So now we can derivative $L$ on $w_{0}$ and $w_{1}$ *(since the loss function is convex, which is a very convenient thing)*, and then find the minimum $w_{0}$ and $w_{1}$. Here's the final formulas for parameters:
$$
\begin{align}
w_{0}&=\bar{y}-w_{1}\bar{x}  \\
w_{1}&=\dfrac{\bar{xy}-\bar{x}\bar{y}}{\bar{x}^{2}-(\bar{x})^{2}}
\end{align}
$$
where $\bar{\alpha}$ is the mean for all of $\alpha$

