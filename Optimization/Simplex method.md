Used for optimizing multi-variable [[LPP]] .
## How to
1. Bring the problem to a [[LPP#Standard form|standard form]]. Newly introduced variables are called [[Types of solutions#Basic variable|basic variables]]. The rest are non-basic. Basic variables are "tightened", i.e. set to zero to find a [[Types of solutions#Feasible solution|feasible solution]]. 
   Remember that if the problem is a maximization problem, turn it into the minimization problem by $\times(-1)$ the objective function.
2. Create the simplex tableau
3. Iterate to the end
# Example   
Let's use a concrete example
$$
\begin{matrix*}[l]
maximize & 3x+4y+5z \\
s.t & 2x+y\leq 10 \\
 & 2y+z\leq 20 \\
 & 2z+x\leq 20 \\
 & x,y,z\geq0
\end{matrix*}
$$
Now, bringing to standard form:
$$
\begin{matrix*}[l]
minimize & -3x-4y-5z \\
s.t & 2x+y + r = 10 \\
 & 2y+z + s = 20 \\
 & 2z+x + t = 20 \\
 & x,y,z\geq0
\end{matrix*}
$$
We will use the objective function as a part of the table. Let's say:
   $$P-3x-4y-5z=0$$
where $P$ will be our optimum value. Now let's build a table.

  | Basic variable | x   | y   | z   | r   | s   | t   | Value | Row operations |
  | -------------- | --- | --- | --- | --- | --- | --- | ----- | -------------- |
  | r              | 2   | 1   | 0   | 1   | 0   | 0   | 10    | $R_{1}$        |
  | s              | 0   | 2   | 1   | 0   | 1   | 0   | 20    | $R_{2}$        |
  | t              | 1   | 0   | 2   | 0   | 0   | 1   | 30    | $R_{3}$        |
  | P              | -3  | -4  | -5  | 0   | 0   | 0   | 0     | $R_{4}$        |
Do an iteration
To do so, first, find a **column** with the **lowest** value in the **objective row**. In this case the column is $z$ and it is called the **pivot column**.
Then, calculate $\theta$s as $\theta=\dfrac{value}{pivot\ column}$
The **row** with the **smallest non-negative** $\theta$ is the **pivot row**,
The variable that is the intersection of the pivot row with the pivot column is the **pivot variable**. 

| Basic variable | x   | y   | <mark class="hltr-green">z</mark>   | r   | s   | t   | Value | Row operations | $\theta$ |
| -------------- | --- | --- | --- | --- | --- | --- | ----- | --------- | -------- |
| r              | 2   | 1   | 0   | 1   | 0   | 0   | 10    | $R_{1}$   |    $\dfrac{10}{0}=\infty$     |
| s              | 0   | 2   | 1   | 0   | 1   | 0   | 20    | $R_{2}$   |        $\dfrac{20}{1}=20$  |
| <mark class="hltr-green">t</mark>              | 1   | 0   | <mark class="hltr-green">2</mark>   | 0   | 0   | 1   | 30    | $R_{3}$   | $\dfrac{30}{2}=15$|
| P              | -3  | -4  | -5  | 0   | 0   | 0   | 0     | $R_{4}$   | don't bother|

We need to make the chosen column *basic*. That is, there're 0s everywhere except for the intersection where we'll have a 1. Use row operations.

| Basic variable | x   | y   | <mark class="hltr-green">z</mark>   | r   | s   | t   | Value | Row operations | $\theta$ |
| -------------- | --- | --- | --- | --- | --- | --- | ----- | --------- | -------- |
| r              | 2   | 1   | 0   | 1   | 0   | 0   | 10    | $R_{5}=R_{1}$   |    $\dfrac{10}{0}=\infty$     |
| s              | $-\dfrac{1}{2}$   | 2   | 0   | 0   | 1   | $-\dfrac{1}{2}$   | 5    | $R_{6}=R_{2}-R_{7}$   |        $\dfrac{20}{1}=20$  |
| <mark class="hltr-red">z</mark>              | $\dfrac{1}{2}$  | 0   | <mark class="hltr-green">1</mark>   | 0   | 0   | $\dfrac{1}{2}$   | 15    | $R_{7}=\dfrac{R_{3}}{2}$   | $\dfrac{30}{2}=15$|
| P              | $-\dfrac{1}{2}$  | -4  | 0  | 0   | 0   | $\dfrac{5}{2}$   | 75     | $R_{8}=R_{4}+5R_{7}$   | don't bother|

Find the pivot

| Basic variable | x   | <mark class="hltr-green">y</mark>   | z  | r   | s   | t   | Value | Row operations | $\theta$ |
| -------------- | --- | --- | --- | --- | --- | --- | ----- | --------- | -------- |
| r              | 2   | 1   | 0   | 1   | 0   | 0   | 10    | $R_{5}=R_{1}$   |    10     |
| <mark class="hltr-green">s</mark>              | $-\dfrac{1}{2}$   | <mark class="hltr-green">2</mark>   | 0   | 0   | 1   | $-\dfrac{1}{2}$   | 5    | $R_{6}=R_{2}-R_{7}$   |   $\dfrac{5}{2}$  |
| z             | $\dfrac{1}{2}$  | 0   | 1  | 0   | 0   | $\dfrac{1}{2}$   | 15    | $R_{7}=\dfrac{R_{3}}{2}$   | 0 |
| P              | $-\dfrac{1}{2}$  | -4  | 0  | 0   | 0   | $\dfrac{5}{2}$   | 75     | $R_{8}=R_{4}+5R_{7}$   | don't bother|

Swap the variables and make the pivot 0

| Basic variable | x   | <mark class="hltr-green">y</mark>   | z  | r   | s   | t   | Value | Row operations | $\theta$ |
| -------------- | --- | --- | --- | --- | --- | --- | ----- | --------- | -------- |
| r              | $\dfrac{9}{4}$   | 0   | 0   | 1   | $-\dfrac{1}{2}$   | $\dfrac{1}{4}$   | $\dfrac{15}{2}$    | $R_{9}=R_{5}-R_{10}$   |    10     |
| <mark class="hltr-red">y</mark>              | $-\dfrac{1}{4}$   | 1  | 0   | 0   | $\dfrac{1}{2}$   | $-\dfrac{1}{4}$   | $\dfrac{5}{2}$    | $R_{10}=R_{6}-R_{2}$   |   |
| z             | $\dfrac{1}{2}$  | 0   |1  | 0   | 0   | $\dfrac{1}{2}$   | 15    | $R_{7}=\dfrac{R_{3}}{2}$   | 0 |
| P              | $-\dfrac{1}{2}$  | -4  | 0  | 0   | 0   | $\dfrac{5}{2}$   | 75     | $R_{8}=R_{4}+5R_{7}$   | don't bother

To avoid fucking with obsidian tables, I'll skip over to the final iteration

| Basic variable                  | x               | <mark class="hltr-green">y</mark> | z   | r              | s               | t               | Value           |
| ------------------------------- | --------------- | --------------------------------- | --- | -------------- | --------------- | --------------- | --------------- |
| x                               | 1               | 0                                 | 0   | $\dfrac{4}{9}$ | $-\dfrac{2}{9}$ | $\dfrac{1}{9}$  | $\dfrac{10}{3}$ |
| y | 0 | 1                                 | 0   | $\dfrac{1}{9}$              | $\dfrac{4}{9}$  | $-\dfrac{2}{9}$ | $\dfrac{10}{3}$  |
| z                               | 0  | 0                                 | 1   | $-\dfrac{2}{9}$              | $\dfrac{1}{9}$               | $\dfrac{4}{9}$  | $\dfrac{40}{3}$              |
| P                               | 0 | 0                                | 0   | $\dfrac{2}{3}$              | $\dfrac{5}{3}$               | $\dfrac{5}{3}$  | 90              |

To minimize, maximize the negative of the objective function
# References
- https://www.youtube.com/watch?v=t0NkCDigq88
- The Art of Linear Programming by Tom S - https://www.youtube.com/watch?v=E72DWgKP_1Y
- Simplex Method explained - https://www.srcc.edu/sites/default/files/BCom(Hons)_2year_BMaths_1&2_Harish%20Kumar.pdf