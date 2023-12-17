Also called "variation of constants".
Used to find a [[Differential equations#Particular|particular solution]] for a non-homogeneous [[High order linear constant coefficient equation|high-order differential equation]]
# Algorithm
## First order
TODO
## Second order
Consider:
$$
a_{0}(x)y''+a_{1}(x)y'+a_{2}(x)y=f(x)
$$
Having a general solution to a complementary equation:
$$
y_{p}=c_{1}y_{1}+cy_{2}
$$
We now assume that $c_{1}, c_{2}$ are functions of $x$:
$$
y_{p}=u_{1}(x)y_{1}+u_{2}(x)y_{2}
$$
Now, we solve the following system:
$$
\begin{cases}
u_{1}'(x)y_{1}+u_{2}'(x)y_{2}=0 \\
u_{1}'(x)y_{1}'+u_{2}'(x)y_{2}'= \dfrac{f(x)}{a_{0}(x)} 
\end{cases}
$$
Use [[Crammer's rule]] to solve the system. It looks similar to [[Wronskian]]
$$
W=\begin{vmatrix}
y_{1} & y_{2} \\
y_{1}' & y_{2}' 
\end{vmatrix}
$$
If $W\neq 0$, that means a unique solution exist. If $W=0$, then there are either no solutions, or infinitely many.
Considering that that a unique solution exists, use [[Crammer's rule]]:
$$
\begin{matrix*}[l]
\Delta_{u_{1}}=\begin{vmatrix}
0 & u_{1}' \\
\dfrac{f(x)}{a_{0}(x)} & u_{2}'
\end{vmatrix}
&
\Delta_{u_{2}}=\begin{vmatrix}
u_{1}' & 0 \\
u_{2}' & \dfrac{f(x)}{a_{0}(x)}
\end{vmatrix} \\
u_{1}'=\dfrac{\Delta_{u_{1}}}{W} & u_{2}'=\dfrac{\Delta_{u_{2}}}{W} \\
u_{1} =\int u_{1}' +c_{1}  \, dx & u_{2} =\int u_{2}' \, dx +c_{2}
\end{matrix*}
$$
Now, we can substitute back $u_{1}$ and $u_{2}$ to get the general solution
# References
http://mathprofi.ru/metod_variacii_proizvolnyh_postoyannyh.html