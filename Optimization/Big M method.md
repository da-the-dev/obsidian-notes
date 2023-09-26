Same as [[Simplex method]], but add artificial variables if the inequality has $\geq$. In the objective function, add $-Mr_{i}$ if we are maximizing, add $+Mr_{i}$ if minimizing. Create the tableau and iterate as usual. 
## On slack, surplus, and artificial variables
To get basic variables, we add slack, surplus, and artificial variables.
- If the inequality has $\leq$, we add *slack* variables.
- If the inequality has $>=$, we add *surplus* **and** *artificial* variables.
- If we have an equation, we add *artificial* variables **as needed**.

**The general idea of these variables is to have $2m$ variables for $m$ equations. We might not need to add some variables in some cases**
# Z formula
From slide 24 from [Lecture 3](https://moodle.innopolis.university/pluginfile.php/184379/mod_folder/content/0/Lecture_3%20-%20Simplex.pdf?forcedownload=1)
> To eliminate the inconsistency, we need to substitute out $R_{1}$ and $R_{2}$ in the z-row using the following row operation
> New z-row = Old z-row $+ (100 \times R_{1} row+100 \times R_{2}row)$
