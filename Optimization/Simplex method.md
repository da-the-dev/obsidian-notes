Used for optimizing multi-variable [[LP]] problems.
## How to
1. Bring the problem to a standard form. Meaning:
$P=f(x_{1},x_{2}\dots,x_{n})$
$a_{1}x_{1}+b_{1}x_{1}+\dots+\theta_{1}x_{n}\leq \alpha_{1}$
$\dots$
$a_{p}x_{p}+b_{p}x_{p}+\dots+\theta_{p}x_{p}\leq \gamma_{p}$
$x_{1},x_{2},\dots,x_{n}\geq 0$
i.e., the inequalities are all $\leq$ and all the variables are non-negative
2. Introduce the slack variables and make the objective function to zero. This arrangement is called *canonical form*
$P-a_{0}x_{0}+b_{0}x_{0}+\dots+\theta_{n}x_{n}=0$
$a_{1}x_{1}+b_{1}x_{1}+\dots+\theta_{1}x_{n}+s_{1}=\alpha_{1}$
$\dots$
$a_{p}x_{p}+b_{p}x_{p}+\dots+\theta_{p}x_{p}+s_{p}=\gamma_{p}$
$x_{1},x_{2},\dots,x_{n}\geq 0$
3. Create the simplex tableau
   To build it, let's use a concrete example:
   $P-3x-4y-5z=0$
   $2x+y+r=10$
   $2y+z+s=10$
   $2z+x+t=30$

  | Basic variable | x   | y   | z   | r   | s   | t   | Value | Row operations |
  | -------------- | --- | --- | --- | --- | --- | --- | ----- | -------------- |
  | r              | 2   | 1   | 0   | 1   | 0   | 0   | 10    | $R_{1}$        |
  | s              | 0   | 2   | 1   | 0   | 1   | 0   | 20    | $R_{2}$        |
  | t              | 1   | 0   | 2   | 0   | 0   | 1   | 30    | $R_{3}$        |
  | P              | -3  | -4  | -5  | 0   | 0   | 0   | 0     | $R_{4}$        |
4. Do an iteration

| Basic variable | x   | y   | <mark class="hltr-green">z</mark>   | r   | s   | t   | Value | Row operations | $\theta$ |
| -------------- | --- | --- | --- | --- | --- | --- | ----- | --------- | -------- |
| r              | 2   | 1   | 0   | 1   | 0   | 0   | 10    | $R_{1}$   |    $\dfrac{10}{0}=\infty$     |
| s              | 0   | 2   | 1   | 0   | 1   | 0   | 20    | $R_{2}$   |        $\dfrac{20}{1}=20$  |
| <mark class="hltr-green">t</mark>              | 1   | 0   | <mark class="hltr-green">2</mark>   | 0   | 0   | 1   | 30    | $R_{3}$   | $\dfrac{30}{2}=15$|
| P              | -3  | -4  | -5  | 0   | 0   | 0   | 0     | $R_{4}$   | don't bother|

To do so, first, find a **column** with the **lowest** value in the **objective row** ($R_{4}$ in this case). In this case the column is $z$ and it is called the **pivot column**.
Then, calculate $\theta$s as $\theta=\dfrac{value}{pivot\ column}$
The **row** with the **smallest non-negative** $\theta$ is the **pivot row**.,
The variable that is the intersection of the pivot row with the pivot column is the **pivot variable**. 

Now, we can fill the tableau of the iteration

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
https://www.youtube.com/watch?v=t0NkCDigq88

Simplex Method explained:
https://www.srcc.edu/sites/default/files/BCom(Hons)_2year_BMaths_1&2_Harish%20Kumar.pdf