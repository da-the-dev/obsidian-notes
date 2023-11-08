One of the methods to find a [[Types of solutions|basic feasible solution]] for [[Transportation problems#Solution|Transportation simplex]].
# Algorithm
- For each source row $i$ remaining under consideration, determine its $\bar{u}_{i}$, which is the largest unit cost $c_{ij}$ still remaining in that row.
- For each destination column $j$ remaining under consideration, determine its $\bar{v}_{j}$, which is the largest unit cost $c_{ij}$ still remaining in that column. 
- For each variable $x_{ij}$ not previously selected in these rows and columns, calculate $\Delta_{ij}=c_{ij}-\bar{u}_{i}-\bar{v}_{j}$. Select the variable having the largest (in absolute terms) negative value of $\Delta_{ij}$.
# References
https://moodle.innopolis.university/pluginfile.php/186857/mod_resource/content/1/Lecture_7%20-.pdf