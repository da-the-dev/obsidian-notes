A linear high order differential equation is a [[Differential equations|differential equation]] of the form:
$$
\begin{cases}
P_{0}(x)y^{(n)}+P_{1}(x)y^{(n-1)}+\dots+P_{n}(x)y=F(x) \\
L_{y}=F(x)
\end{cases}
$$
where $n$ is any arbitrary integer and can be transformed into
$$
y^{(n)}+p(x)y^{(n-1)}+\dots+p_{n}(x)y=f(x)
$$
with $p_{n} = \dfrac{P_{n}}{P_{0}}$ and $\dfrac{F}{P_{0}}$ ($P_{0}$ has no zeros)
# Homogeneous LHODs
If $F \equiv 0$ then LHOD is homogeneous, non-homogeneous otherwise.

# Finding a general solution
Knowing a set of solutions of a LHOD a general solution looks like this:
$$
y=c_{1}y_{1}+c_{2}y_{2}+\dots +c_{n}y_{n}
$$
If the set of solutions is linearly independent, then
$$
c_{1}y_{1}+c_{2}y_{2}+\dots c_{n}y_{n}=0\ \ \ \ \ \ (1)
$$
Iff $c_{1}=c_{2}=\dots=c_{n}=0$. If $(1)$ somehow holds for $c$s that are not zero, then the set of solutions is linearly dependent.
A set of solutions is fundamental iff the solutions are linearly independent.
## Example
$$
x^{3}y'''-x^{2}y''-2xy'+6y=0
$$
has solutions $y_{1}=x^{2}$, $y_{2}=x^{3}$, and $y_{3}=\dfrac{1}{x}$ on $(0, \infty)$. Show that $y_{1},y_{2},y_{3}$ are linearly independent and find a general solution.
## Solution
A general solution would look like this:
$$
c_{1}x^{2}+c_{2}x^{3}+\dfrac{c_{3}}{x}=0
$$
Let's differentiate our equation two times:
1) $2c_{1}x + 3c_{2}x^{2} - \dfrac{c_{3}}{x^{2}}=0$
2) $2c_{1} + 6c_{2}x + \dfrac{2c_{3}}{x^{3}}=0$
With the equation of a general solution we can form a system of linear equations, that represents all the ways that $y_{1},y_{2},y_{3}$ can depend (or be independent) on on another.

$$
\begin{cases}
c_{1}x^{2}+c_{2}x^{3}+\dfrac{c_{3}}{x}=0 \\
2c_{1}x + 3c_{2}x^{2} - \dfrac{c_{3}}{x^{2}}=0 \\
2c_{1} + 6c_{2}x + \dfrac{2c_{3}}{x^{3}}=0
\end{cases}
$$
In matrix form:
$$
\begin{pmatrix}
x^{2} & x^{3} & \dfrac{1}{x} \\
2x & 3x^{2} & -\dfrac{1}{x^{2}} \\
2 & 6x & \dfrac{2}{x^{3}}
\end{pmatrix}

\begin{pmatrix}
c_{1} \\
c_{2} \\
c_{3}
\end{pmatrix}
=
\begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix}
$$

The Wronskian is
$$
W=\begin{vmatrix}
y_{1} & y_{2} & y_{3}  \\
y_{1}'& y_{2}'&y_{3}' \\
y_{1}''& y_{2}''&y_{3}''
\end{vmatrix}
$$
If $\det(W)$ is non-zero, then from Linear Algebra, the matrix is invertable, i.e. has a unique solution. That solution would have to be 0,0,0 for our general equation assumption to work (the solutions are linearly independent)

In our case:
$$
W=
\begin{vmatrix}
1 & 1 & 1 \\
2 & 3 & -1 \\
2 & 6 & 2
\end{vmatrix}=12
$$
The determinant is non-zero, so there is only one uniques *trivial* solution to this system of linear equations, i.e.
$$
\begin{pmatrix}
c_{1} \\
c_{2} \\
c_{3}
\end{pmatrix}
=
\begin{pmatrix}
0 \\
0 \\
0 \\
\end{pmatrix}
$$
We have proved that $y_{1},y_{2},y_{3}$ are linearly independent solutions and the assumption of the general solution equation holds

