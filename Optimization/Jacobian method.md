Also known as the constrained derivatives method.

Consider:
$$
\begin{matrix*}[l]
minimize & f(\textbf{X})=z \\
s.t. & g(\textbf{X})=0
\end{matrix*}
$$
We need to separate variables into independent and dependent respectively:
$\textbf{Y}=(y_{1},\dots,y_{n})$ 
$\textbf{Z}=(z_{1},\dots, z_{m})$
[[Jacobian|Jacobian matrix]]:
$$
J=\nabla _{\textbf{Y}}\textbf{g}=
\begin{bmatrix}
\nabla_{\textbf{Y}}g_{1} \\
\dots \\
\nabla_{\textbf{Y}}g_{m} \\
\end{bmatrix}
$$
Control matrix:
$$
C=\nabla _{\textbf{Z}}\textbf{g}=
\begin{bmatrix}
\nabla_{\textbf{Z}}g_{1} \\
\dots \\
\nabla_{\textbf{Z}}g_{m} \\
\end{bmatrix}
$$
Constraint gradient $\nabla_{C}f$ of $f$ with respect to $\textbf{Z}$ :
$$
\nabla_{C}f=\dfrac{\partial_{C}f(\textbf{Y}, \textbf{Z})}{\partial_{C}\textbf{Z}}= \nabla_{\textbf{Z}}f-\nabla_{\textbf{Y}}fJ^{-1}C
$$
It must be zero at all stationary points and the points must be within the constraints, so:
$$
\begin{cases}
\nabla_{C}f=0 \\
\textbf{g}(\textbf{X})=0
\end{cases}
$$
# Example
Consider
$$
\begin{matrix*}[l]
maximize & f(\textbf{X})=x_{1}^{2}+x_{2}^{2}+x_{3}^{2}
s.t. & \\
& g_{1}(\textbf{X}) = x_{1}+x_{2}+3x_{3}-2=0 \\
& g_{2}(\textbf{X}) = 5x_{1}+2x_{2}+x_{3}-5=0 
\end{matrix*}
$$
We determine the constrained extreme points as follows:
$$
\begin{matrix*}[l]
Y=(x_{1},x_{2}) & Z=x_{3} \\
\nabla_{\textbf{Y}}f= \left(\dfrac{ \partial f }{ \partial x_{1} }, \dfrac{ \partial f }{ \partial x_{2} }  \right)=(2x_{1}, 2x_{2}) & \nabla_{\textbf{Z}}f=\dfrac{ \partial f }{ \partial x_{3} }=2x_{3} 
\end{matrix*}
$$
$$
J=\begin{bmatrix}
\dfrac{ \partial g_{1} }{ \partial x_{1} }  & \dfrac{ \partial g_{1} }{ \partial x_{2} } \\ \\
\dfrac{ \partial g_{2} }{ \partial x_{1} }  & \dfrac{ \partial g_{2} }{ \partial x_{2} } 
\end{bmatrix}
=
\begin{bmatrix}
1 & 1 \\
5 & 2
\end{bmatrix}
$$
$$
J^{-1}=\begin{bmatrix}
-\dfrac{2}{3}  & \dfrac{1}{3} \\
\dfrac{5}{3}  & -\dfrac{1}{3}
\end{bmatrix}
$$
$$
C=\begin{bmatrix}
\dfrac{ \partial g_{1} }{ \partial x_{3} } \\
\dfrac{ \partial g_{2} }{ \partial x_{3} }  
\end{bmatrix}
=
\begin{bmatrix}
3 \\
1
\end{bmatrix}
$$
$$
\begin{align}
\nabla_{C}f &= \dfrac{\partial_{C}f(\textbf{Y}, \textbf{Z})}{\partial_{C}\textbf{Z}} \\
&= \nabla_{\textbf{Z}}f-\nabla_{\textbf{Y}}fJ^{-1}C \\
&=2x_{3}-(2x_{1}, 2x_{2})
\begin{bmatrix}
-\dfrac{2}{3}  & \dfrac{1}{3} \\
\dfrac{5}{3}  & -\dfrac{1}{3}
\end{bmatrix}
\begin{bmatrix}
3 \\
1
\end{bmatrix} \\
&= \dfrac{10}{3}x_{1}-\dfrac{28}{3}x_{2} + 2x_{3}
\end{align}
$$

$$
\begin{align}
\begin{cases}
\nabla _{C}f=0 \\
g_{1}(\textbf{X})=0 \\
g_{2}(\textbf{X})=0
\end{cases} 
&\implies
\begin{bmatrix}
10  & -28  & 6 \\
1  &  1  & 3 \\
5 & 2 & 1
\end{bmatrix}
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix}
=
\begin{bmatrix}
0 \\
2 \\
5 \
\end{bmatrix} \\
&\implies \textbf{X}_{0} \approx \begin{bmatrix}
0.81 \\
0.35 \\
0.28
\end{bmatrix}
\end{align}
$$
# Sensitivity coefficients
The Jacobian method can be used to study the effect of small changes to the right-hand side of the optimization problem.
$$
\dfrac{\partial f}{\partial \textbf{g}}=\nabla_{\textbf{Y}_{0}}fJ^{-1}
$$
The effect of the small change $\partial \textbf{g}$ on the optimum value of f can be studied by evaluating the rate of change of $f$ with respect to $g$.
These rates are usually referred to as *sensitivity coefficients*.
## Example
Consider
$$
\begin{matrix*}[l]
minimize & f(\textbf{X})=x_{1}^{2}+x_{2}^{2}+x_{3}^{2} \\
s.t. & g_{1}(\textbf{X})=x_{1}+x_{2}+3x_{3}-2=0 \\
& g_{2}(\textbf{X})=5x_{1}+2x_{2}+x_{3}-5=0
\end{matrix*}
$$
The solution:
$$
\textbf{X}_{0}\approx\begin{bmatrix}
0.81 \\
0.35 \\
0.28
\end{bmatrix}
$$
Given $\textbf{Y}_{0}=(x_{01},x_{02})$:
$$
\nabla_{\textbf{Y}_{0}}f=\left(\frac{ \partial f }{ \partial x_{1} }, \frac{ \partial f }{ \partial x_{2} }  \right)=(2x_{01},2x_{02})=(1.62, 0.70)
$$
$$
\begin{align}
\dfrac{\partial f}{\partial \textbf{g}}&=\nabla_{\textbf{Y}_{0}}fJ^{-1} \\
&=(1.62, 0.70)\begin{bmatrix}
-\dfrac{2}{3}  & \dfrac{1}{3} \\
\dfrac{5}{3}  & -\dfrac{1}{3}
\end{bmatrix} \\
&= (0.0876, 0.3067)
\end{align}
$$
This means for $\partial g_{1}=1$, $f$ will increase by 0.0876
And for $\partial g_{2}=1$, $f$ will increase by 0.3067