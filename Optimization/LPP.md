Linear programming problem (LPP) is a problem characterized by linear functions of unknowns; the objective is linear and constraints are either linear equalities, or linear inequalities.
# Example
A problem with a budget constraints. Say, the total money spent on two commodities is
$$
x_{1} + x_{2} \leq B
$$
where $x_{1}$ and $x_{2}$ are money spent on each item, and $B$ is the budget. The objective, for example, could be to get the maximum weight for each item:
$$
\begin{matrix}
maximize & w_{1}x_{1}+w_{2}x_{2} \\
subject\ to  & x_{1} + x_{2} \leq B \\
 & x_{1}\geq 0, \ x_{2}\geq 0
\end{matrix}
$$
Voila, a linear programming problem!
# Standard form
In standard form we must have:
$$
\begin{matrix}
minimize & \textbf{c}^{\textbf{T}}\textbf{x} \\
s.t.  & \textbf{A}\textbf{x}=\textbf{b} & and &  \textbf{x}\geq0.
\end{matrix}
$$
Here:
- $\textbf{A}$ is the matrix of constraint equalities
- $\textbf{b}$ is the right-hand side of the constant equalities
- $\textbf{x}$ is the $n$-vector with variables to optimize. Every value in $\textbf{x}$ is non-negative.
- $\textbf{c}^{\textbf{T}}$ is the objective function coefficient vector
## Edge cases
### Slack variables
If the problem has an less or equal inequality:
$$
a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n} \leq b_{n}
$$
Then we must introduce a slack variable $s_{n}$ like so:
$$
a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n}+s_{1} = b_{n}
$$
This way an inequality turns into equality.
### Surplus variables
Reverse of slack variables. If we have 
$$
a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n} \geq b_{n}
$$
Then add a surplus variable $s_{n}$
$$
a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n} - s_{n} = b_{n}
$$
to make an equality
### Free variables
##### Method 1 (Replacement)
Replace the unrestricted variable like so:
$$
\begin{matrix}
x_{i} = u_{i} - v_{i},  & u_{i} \geq 0, v_{i} \geq 0
\end{matrix}
$$
We replace the unrestricted variable with a restricted one and also add a new variable. In total, +2 variables.
#### Method 2 (Elimination)
Example:
$$
a_{i1}x_{1}+a_{i2}+\dots+a_{in}x_{n}=b_{i}
$$
$x_{1}$ can now be expressed as a linear combination of other variables plus a constant. Now the $i$'th equation that used to define $x_{1}$ can now be eliminated. We remove a variable and an equation.
##### Method 3 (Special case)
Consider this:
$$
\begin{matrix*} [l]
minimize & x_{1}+3x_{2}+4x_{3} \\
s.t  & x_{1} + 2x_{2} + x_{3} = 5 \\
 & 2x_{1}+3x_{2}+x_{3}=6 \\
 & x_{2} \geq 0,\ x_{3}\geq 0
\end{matrix*}
$$
We can solve the constraints for $x_{1}$ since it's free:
$$
x_{1} = 5 - 2x_{2}-x_{3}
$$
Now, if we substitute into the objective function and the second constraint to remove $x_{1}$ we get:
$$
\begin{matrix*} [l]
minimize & x_{2}+3x_{3} \\
s.t  & x_{2} + x_{3} = 5 \\
 & x_{2} \geq 0,\ x_{3}\geq 0
\end{matrix*}
$$
Now this LPP is in standard form.