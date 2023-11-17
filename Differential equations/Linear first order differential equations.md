A [[First order differential equations|first order differential equation]] is said to be *linear* if it can be written as 
$$
y' + p(x)y = f(x)
$$
This is also a *nonhomogeneous* equation. However, if $f(x) \equiv 0$, then it would be *homoegeneous*.
# General solution
Example *first order* equation:
$$
y'=\dfrac{1}{x^2}
$$
Then $y$ should be
$$
y=-\dfrac{1}{x}+c
$$
where $c$ is some constant (integrate $y$ to see why it works). This is a *general solution*.
Same thing works for *linear first order* equation:
$$
y'+p(x)y=f(x)
$$
Once a <u>general solution</u> $y=y(x,c)$ is obtained, if we have an [[Initial value problem|initial value]] we can substitute and find $c$.
## Case for nonhomogeneous 
If the equation is nonhomogeneous, i.e. $y' + p(x)y = f(x)$, then solve a *complementary equation*
$$
y' + p(x)y = 0
$$
The solutions will be in the form $y=uy_{1}$, where $y_{1}$ is a *non-trivial solution* (i.e. goes through some point, so we can take any $c$) and $u$ is some function. If $y=uy_{1}$, then $y'=u'y_{1}+uy_{1}'$ (basic derivative rule). 

Substituting $y$ and $y'$ into the original equation and reducing we get:
$$
u'y_{1}=f(x)
$$
So $u$ is an integral:
$$
u = \int \dfrac{f(x)}{y_{1}(x)} \, dx 
$$
Since $y=uy_{1}$, substitute $u$ and get a general solution. This method is called **variation of parameters**