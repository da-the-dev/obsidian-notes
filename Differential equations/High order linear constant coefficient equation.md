# Homogeneous
Let's consider a [[Linear high order differential equiation|LHOD]] with some constant coefficients $a_{0},a_{1},\dots,a_{n}$:
$$
a_{0}y^{(n)}+a_{1}y^{(n-1)}+\dots+a_{n}y=0
$$
The key is that if $y=e^{rx}$ where $r$ is some constant, then the left side of the equation is a multiple of that; also $y'=re^{rx}$, $y''=r^{2}e^{rx}$ and so on.
Knowing that the solutions must be [[linearly independent]], their sum with some constant multipliers is zero:
$$
ay''+by'+cy=ar^{2}e^{rx}+bre^{rx}+ce^{rx}=(ar^{2}+br+c)e^{rx}=0
$$
Since $e^{rx}\neq 0$, a quadratic equation
$$
ar^{2} +br+c=0
$$
is called a *characteristic equation*. 
A characteristic equation might be of higher order.
Solutions of the characteristic equation describe the particular solutions of the HOCCHE.
Once all particular solutions are obtained, we can formulate a general solution.
## Cases for characteristic polynomial
### Real distinct roots
$$
y=c_{1}e^{r_{1}x}+c_{2}e^{r_{2}x}+\dots+c_{n}e^{r_{n}x}
$$
### Real repeated root
If the repeated root is $a$, then:
$$
y=e^{ax}+xe^{ax}+\dots+x^{m-1}e^{ax}
$$
### Imaginary distinct roots
For imaginary roots $m_{1}=a+bi$ and $m_{2}=a-bi$:
$$
y= c_{1}e^{ax}\cos (bx)+c_{2}e^{ax}\sin(bx)
$$
## Example
$$
y'''+3y''+3y'+y=0
$$
Characteristic polynomial:
$$
\begin{align}
r^{3}+3r^{2}3r+1&=0 \\
(r+1)^{3}&=0
\end{align}
$$
In this case, the fundamental set of solution is:
$$
\{e^{-x}, xe^{-1}, x^{2}e^{-1}\}
$$
And the general solution is:
$$
y=e^{-1}(c_{1}+c_{2}x+c_{3}x^{2})
$$
# References
https://www.youtube.com/watch?v=iQoAbO_xlFs&list=PLj7p5OoL6vGyLV13uqgYEQHN7D57g1lPZ



