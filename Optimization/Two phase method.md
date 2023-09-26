This method, as the name implies, consists of two phases. This method uses the same tableau as the [[Simplex method]].
# Phase I
Put the problem in equation form and add the necessary artificial variables to the constraints (exactly as in the [[Big M method]]). Next, find a basic solution of the resulting equations that always **minimizes the sum of the artificial variables**.
If the minimum value of the sum is positive, the LP problem has no feasible solution. Otherwise, proceed to Phase II.
# Phase II
Use the feasible solution from Phase I as a starting basic feasible solution for the *original* problem.
# Example
Minimize $z = 4x_{1}+x_{2}$
s.t.
$3x_{1}+x_{2}=3$
$4x_{1}+3x_{2}\geq 6$
$x_{1}+2x_{2}\leq 4$
$x_{1},x_{2}\geq 0$

Now we add necessary variables and minimize the sum of artificial variables *(or maximize the negative of the sum)*.

Minimize $r = R_{1}+R_{2}$ (or maximize $r=-R_{1}-R_{2}$)
s.t.
$3x_{1}+x_{2}+R_{1}=3$
$4x_{1}+3x_{2}-x_{3}+R_{2}=6$
$x_{1}+2x_{2}+x_{4}=4$
$x_{1},x_{2},x_{3},x_{4},R_{1},R_{2}\geq 0$

Starting tableau is
![[Pasted image 20230918150420.png|500]]
Now, considering that we minimize (so we choose the **largest** for entering and leaving variables), we iterate as in Simplex Method. The final tableau.
![[Pasted image 20230918150816.png|500]]
Basic minimum $r=0$, Phase I produces the basic feasible solution $x_{1}=\dfrac{3}{5}$, $x_{2}=\dfrac{6}{5}$, $x_{4}=1$
At this point, the artificial variables have completed their mission, and we can eliminate their columns altogether from the tableau and move to Phase II.

We now consider the original problem statement and complete iterations accordingly.

Initial table:
![[Pasted image 20230918151131.png|500]]
Final table:
![[Pasted image 20230918151201.png|500]]
Completed!
# References
https://moodle.innopolis.university/pluginfile.php/184379/mod_folder/content/0/Lecture_3%20-%20Simplex.pdf?forcedownload=1
http://www.universalteacherpublications.com/univ/ebooks/or/Ch3/twophase.htm