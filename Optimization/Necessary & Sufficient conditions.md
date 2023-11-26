# Necessary condition
A necessary condition for $\textbf{X}_{0}$ to be an extreme point of $f(\textbf{X})$ is that:
$$
\nabla f(\textbf{X}_{0})=\textbf{0}
$$
(gradient at $\textbf{X}_{0}$ is a zero vector)
If this holds, $\textbf{X}_{0}$ *might* be a an extreme. If this does not hold, $\textbf{X}_{0}$ is definitely *not a solution*. This also holds for *saddle points*.
# Sufficient condition
A sufficient condition for a stationary point $\textbf{X}_{0}$ to be an extreme is that the [[Hessian matrix]] $H$ evaluated at $\textbf{X}_{0}$ satisfy the following conditions:
- $H$ is positive definite if $\textbf{X}_{0}$ is a minimum point.
- $H$ is negative definite if $\textbf{X}_{0}$ is a maximum point.
Otherwise it is a saddle point