This method, as the name implies, consists of two phases. This method uses the same tableau as the [[Simplex method]].
# Phase I
Put the problem in [[LPP#Standard form|standard form]] and add the necessary [[Big M method#On slack, surplus, and artificial variables|artificial variables]] to the constraints. Next, find a [[Types of solutions#Basic solutions|basic solution]] of the resulting equations that always **minimizes the sum of the [[Big M method#On slack, surplus, and artificial variables|artificial variables]]**.
If the minimum value of the sum is positive, the [[LPP]] has no [[Types of solutions#Feasible solution|feasible solution]]. Otherwise, proceed to Phase II.
# Phase II
Use the feasible solution from Phase I as a starting basic feasible solution for the *original* problem.
# Example
$$
\begin{matrix*}[l]
minimize & z = 4x_{1}+x_{2} \\
s.t.
& 3x_{1}+x_{2}=3 \\ 
& 4x_{1}+3x_{2}\geq 6 \\
& x_{1}+2x_{2}\leq 4 \\ 
& x_{1},x_{2}\geq 0 \\
\end{matrix*}
$$


Now we add necessary variables and minimize the sum of artificial variables *(or maximize the negative of the sum)*.

$$
\begin{matrix*}[l]
maximize & r=R_{1}+R_{2} \\
s.t.
& 3x_{1}+x_{2}+R_{1}=3 \\ 
& 4x_{1}+3x_{2}-x_{3}+R_{2}=6 \\ 
& x_{1}+2x_{2}+x_{4}=4 \\
& x_{1},x_{2},x_{3},x_{4},R_{1},R_{2}\geq 0 \\ 
\end{matrix*}
$$
Here it is in a table form
## Phase  I
### Step 0
![[Two phase method1.png]]
The table is [[Inconsistency|inconsistent]], because $R_{1}$ and $R_{2}$ are positive in the objective row. We need to modify the $r$ row. Namely, subtract $R_{1}$ row and $R_{2}$ row from $r$ such that the coefficients for both $R_{1}$ and $R_{2}$ are zero.
In this case new $r$ is $r_{new} = r_{old}-R_{1}-R_{2}$.
![[Two phase method2.png]]
Now it's the same as the [[Simplex method]]. Here are the steps:
![[Two phase method3.png]]
![[Two phase method4.png]]
The $r$ row contains no negative values, so the algorithm stops. The solution is marked in red.
## Phase II
Now we remove $R_{1}$ and $R_{2}$ columns and replace $r$ row with $z$ row from the original problem statement
![[Two phase1.png]]
We change the minimization problem into a maximization one, hence the change in the coefficients for the $z$ row. Again, the table is inconsistent. Same operations like we did in Phase I:
$$
z_{new} = z_{old} - 4x_{1}-x_{2}
$$
![[Two phase2.png]]
Only one step here
![[Two phase3.png]]
Solution is in red

If you have found mistakes in the solution, checkout the `Two phase method.ods` file with the tables and update it. Also, update the screenshots here.
# References
https://moodle.innopolis.university/pluginfile.php/184379/mod_folder/content/0/Lecture_3%20-%20Simplex.pdf?forcedownload=1
http://www.universalteacherpublications.com/univ/ebooks/or/Ch3/twophase.htm
https://www.youtube.com/watch?v=_wnqe5_CLU0&t=1462s