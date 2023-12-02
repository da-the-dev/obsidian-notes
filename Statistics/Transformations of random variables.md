Off the start:
$$
\begin{matrix*}[l]
Y=u(X) \\
X=w(Y)
\end{matrix*}
$$
# Discrete one-to-one
In this case the transformation is simple. In case of [[random variable]] $X$ and $Y=u(X)$. Then the [[probability distribution]] of $Y$:
$$
g(y)=f[w(y)]
$$
where $w(y)=x$
TL:DR - substitute dumbass
# Discrete joint one-to-one
Same deal as with single discrete one-to-one:
$$
g(y_{1}, y_{2}) = f[w_{1}(y_{1},y_{1}), w_{2}(y_{1},y_{2})]
$$
A little bit of trolling should be completed in one has $X_{1}, X_{2}$ and $Y=u(X_{1},X_{2})$. We need to define a second function, $Y_{2}=u_{2}(X_{1},X_{2})$ that maintains one-to-one correspondence between points of two dimensions. This gives us the [[Joint probability|joint probability distribution]] $g(y_{1}, y_{2})$. PDF of just $Y_{1}$ is a [[Joint probability#Marginal distributions|marginal distribution]] of $g$. Therefore it can be found like so:
$$
h(y_{1}) = \sum_{y_{2}}g(y_{1},y_{2})
$$
# Continuous one-to-one
In this case we need to take the [[Jacobian]]:
$$
g(y)=f[w(y)]|J|
$$
where $J=w'(y)$
# Continuous joint one-to-one
Same deal as with single one-to-one:
$$
g(y_{1}, y_{2})=f[w_{1}(y_{1}, y_{2}), w_{2}(y_{1}, y_{2})]|J|
$$
where $J$ is $2 \times 2$:
$$
J = \begin{bmatrix}
\dfrac{ \partial x_{1} }{ \partial y_{1} } & \dfrac{ \partial x_{1} }{ \partial y_{2} } \\
\dfrac{ \partial x_{2} }{ \partial y_{1} } & \dfrac{ \partial x_{2} }{ \partial y_{2} } 
\end{bmatrix}
$$
dont forgor that $|J|=\det(J)$
# Continuous joint one-to-many
We do be getting humorously trolled in this particular case. Consider the following example:
Suppose $f(x)$ is positive over the interval $-1 < x < 2$ and zero elsewhere.
Transformation is $y=x^{2}$

In this case, $x=\pm \sqrt{ y }$ for $0<y<1$
and $x=\sqrt{ y }$ for $1 < y < 4$.

For the second interval:
$$
g(y)=f[w(y)]|J|=\dfrac{f(\sqrt{ y })}{2\sqrt{ y }}, 1 < y < 4
$$
All is good. However, we get trolled with the first interval. We must partition the interval $-1<x<1$ to this:
$$
x = -\sqrt{ y }
$$
fml

$$
g(y)=\sum^{k}_{i=1}f[w_{i}(y)]|J_{i}|
$$
