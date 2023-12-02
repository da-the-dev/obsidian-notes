!!!TODO rewrite
Dual problem allows to prove that the optimum solution for an [[LPP]] is valid. Dual problem is constructed from a main problem (later called *primal*) in such a way that the solution to the dual problem is no less that the solution for the primal problem.
# Weak duality theorem
Consider this problem
$$
\begin{matrix}
maximize & 1.2x_{1}+1.7x_{2} \\
s.t. & x_{1} \leq 3000 \\
 & x_{2} \leq 4000 \\
 & x_{1} + x_{2}\leq 5000 \\
 & x_{1},x_{2} \geq 0
\end{matrix}
$$
The optimum is $8000$ for this problem. Now let's prove that this is the solution. We need to combine the restriction of the inequalities in such a way, so that the value of the objective function cannot be lesser or greater.
Let's throw in some numbers and see what we can do:
**Case 1**
Look at the objective function. Let's multiply the first inequality by 1.2, the second one by 1.7, and add them up. We get:
$$
1.2x_{1}+1.7x_{2}\leq 10400
$$
Ok, let's use the third inequality. Take 0.2 of the first inequality, 0.7 of the second, 1 of the third, and add them up. We get:
$$
1.2x_{1}+1.7x_{2}\geq 8400
$$
Looks promising. Let's formalize:

Let's consider some variables $y_{1},y_{2},y_{3}$. These are the multipliers for the inequalities. Thees must be non-negative. Also, the left size of the new inequalities is at least the objective function. We want to minimize the right side as well. In total:
$$
\begin{matrix}
minimize & 3000y_{1}+4000y_{2}+5000y_{3} \\
s.t. & y_{1} + y_{3} \geq 1.2 \\
 & y_{2} + y_{3} \geq 1.7 \\
 & y_{1},y_{2},y_{3} \geq 0
\end{matrix}
$$
In the end we obtain a new [[LPP]]. The meaning of this problem is "how much can I max out the primal constraints, so that I the closest value to the optimum can get". 
The **weak duality theorem** states that if a feasible solution to either primal or dual exists, then **solutions to the primal are always lesser or equal to the dual.** 
![[Pasted image 20231127232620.png]]
# Strong duality theorem
Same as the [[Duality#Weak duality theorem|Weak duality theorem]], but if **a solution exists** for either prime or dual, it is the same solution for both.
# References
The Art of Linear Programming by Tom S - https://www.youtube.com/watch?v=E72DWgKP_1Y