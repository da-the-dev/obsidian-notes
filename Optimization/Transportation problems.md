Transportation problems are special case of [[LPP]]s. Here's their definition:
> Having $m$ sources that can give out some commodity, $n$ destinations for that commodity, supply $s_{i}$ from each source, demand $d_{j}$ at each destination, cost of delivery $c_{ij}$ from source $i$ to destination $j$, find an optimal way to deliver all goods from all sources to all destinations.
# Standard form
![[Pasted image 20231108193458.png]]
# Solution 
The solution takes ideas from the [[Simplex method]], however, it differs quite a lot
## Step 0. Formulate
In the beginning we first need to understand the task and build the tableau.
![[Pasted image 20231108231201.png]]
Here's the tableau. The rows represent supply, columns represent demand. Each cell holds the value of $x_{ij}$ - how much from $i$'th supplier should go to $j$'th client. The right upper corner of each cell holds the cost $c_{ij}$. $s_{1}$ represent supply ability. $d_{i}$ represents demand.
## Step 1. Find a basic feasible solution
The reason we don't use something like [[Big M method]] is due to unnecessary complexity we would add with this approach. Instead, other algorithms are used to find a starting [[Types of solutions|basic feasible solution]], for example [[Vogel's method]], [[Minimum cost method]], [[Russel's method]], [[Northwest corner method]], etc. Each of them have their strengths and weaknesses, so choose wisely.
## Step 2. Update u's and v's
Now we start the Transportation Simplex algorithm. Suppose we have this tableau:
![[Pasted image 20231108231905.png]]
The basic feasible solution is already present. It was produced using the [[Northwest corner method]]
$u$s and $v$s are updated according to the rule:
$$
u_{i} + v_{j} = c_{ij}
$$
For the first iteration, $u_{1} = 0$. The rest of $u$s and $v$s are filled according to the rule
![[Pasted image 20231108232136.png]]
## Step 3. WIJ
Cells in red are called non-basic cells and hold values for non-basic variables. We need to define $w_{ij}$ for each of them in accordance to this rule:
$$
w_{ij} = u_{i} + v_{j} - c_{ij}
$$
![[Pasted image 20231108232325.png]]
A solution is optimal iff $w_{ij} \leq 0,\ \forall i, j$ 
## Step 4. Loop pivoting
Otherwise, we need to iterate to a better solution. We chose an entering variable, which is the largest positive value in a non-basic cell, 6 in this case.
We now need to find a [[Loops & loop pivoting#Loops|loop]] that contains this variable. Do the [[Loops & loop pivoting#Loop pivoting|loop pivoting]]
![[Pasted image 20231108232749.png]]
![[Pasted image 20231108233024.png]]
After that, we go to step 2 and repeat until the end condition holds. 
## Exit
In the end, we will have something like this:
![[Pasted image 20231108233316.png]]
Here all $w_{ij}\leq 0$. The solution is:
$$\
\begin{matrix*}[l]
x_{12}=10 \\
x_{13}=25 \\
x_{23}=45 \\
x_{23}=5 \\
x_{32}=10 \\
x_{34}=30 \\
other\ x_{ij}=0
\end{matrix*}
$$
# Optimality test
A BFS is optimal iff $c_{ij} - u_{i} - v_{j},\ \forall (i,j)\ s.t .\ x_{ij} - nonbasic$
# References
https://www.youtube.com/playlist?list=PL3rXWhnlnXkstBqfpF7plaBM6rjo4PguC