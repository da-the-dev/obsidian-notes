One of the [[Interior point methods]]. Uses a barrier function to find a search direction.
# Barrier function
A barrier function acts as a replacement for the non-negativity constraints on any variables. Basically, turn the [[NLP#Standard form|standard form of NLP]]
$$
\begin{matrix*}[l]
min & f(x) \\
s.t & c(x) = 0 \\
 & x \geq 0
\end{matrix*}
$$
into this:
$$
\begin{matrix*}[l]
min & f(x) - \mu \sum\limits^{n}_{i=1}\ln(x_{i}) \\
s.t & c(x) = 0 \\
\end{matrix*}
$$
where $\mu$ is the barrier parameter. The barrier function "pushes away" the solution to infinity the closer the solution is to zero. Accuracy is better for smaller values of $\mu$.
# KKT Conditions
KKT stands for !TODO. We take the derivative of the now modified objective function with respect to $x$:
$$
\begin{matrix}
\nabla f(x) - \nabla c(x) \lambda - \mu \sum\limits^{n}_{i=1} \dfrac{1}{x_{i}}  = 0 \\
c(x)=0
\end{matrix}
$$
We can define $z_{i}= \dfrac{\mu}{x_{i}}$ (for convenience) and solve
$$
\begin{matrix*}[r]
\nabla f(x) - \nabla c(x) \lambda - \mu \sum\limits^{n}_{i=1} \dfrac{1}{x_{i}}  = 0  &  \\
c(x)= 0 \\
XZe-\mu e = 0
\end{matrix*}
$$
The last equation is a consequence of the definition. $e$ is column vector $[1,1,\dots,1]^{T}$


# References
Interior Point Method for Optimization by APMonitor.com - https://www.youtube.com/watch?v=zm4mfr-QT1E&t=68s
