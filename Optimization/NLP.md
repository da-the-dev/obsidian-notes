Non-linear problems are problems with non-linear constraints. For example, in [[LPP]]s all constraints constitute a line in $n$-dimensional space. What if the constraint is a circle? Or a sphere? Or a 4-dimensional cube? Then the problem becomes non-linear.
# Standard form
A general example:
$$
\begin{matrix*}[l]
minimize  & f(x) \\
s.t. &  c_{i}=0 \\
 & x \in X
\end{matrix*}
$$
The inequality constraints are transformed into equalities using [[LPP#Edge cases|extra variables]].
Non-negativity can be added as a separate constraint. 
