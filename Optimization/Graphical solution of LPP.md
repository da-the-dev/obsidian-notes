Graphical solution of [[LPP]] consists of:
- Drawing the graphs of the constraints
- Finding one area where all constraints intersect
	- If such area does not exists, the LPP does not have a solution
- Find gradient of the objective function
- Find the min/max point out of all feasible points
# Basic solutions
Basic solutions are the unique solutions of a system of equations. The constraints are changed into equalities by adding slack or surplus variables (like in [[Simplex method]]).

Now we have a matrix $A_{n \times m}$, that is a part of a system $A\hat{X}=B$. There are $n$ variables, $m$ equations. To find a basic solution, we need to put $n-m$ variables to zero and solve the system $B\hat{X}_{b}=b$.