$$
W=\begin{vmatrix}
y_{1} & y_{2} & \dots & y_{n} \\
y_{1}' & y_{2}' & \dots & y'_{n} \\
\dots & \dots & \ddots & \dots \\
y_{1}^{(n-1)} & y_{2}^{(n-1)} & \dots & y_{n}^{(n-1)}
\end{vmatrix}
$$
# Linear independence
If the Wronskian for a system of functions is 0, then these functions are dependent. Otherwise, they are independent
# Construct differential equation
To construct a [[Differential equations|differential equation]] given the solutions to that equation, construct a modified Wronskian:
## Example
Given solutions:
$1$ and $\cos(x)$
Construct a differential equation.
### Solution
$$
\begin{align}
W &= \begin{vmatrix}
1 & \cos (x) & y \\
0 & -\sin(x) & y' \\
0 &  -\cos(x) & y'' 
\end{vmatrix} \\
&=-\sin (x) y'' + \cos (x)y'
\end{align}
$$
