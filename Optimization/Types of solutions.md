# Basic solutions
Consider a system
$$
\textbf{A}\textbf{x}=\textbf{b}
$$
where
- $\textbf{A}$ is an $m\times n$ matrix, 
- $\textbf{x}$ is an $n$-vector
- $b$ is an $m$-vector
In a case of [[LPP]], we can consider $\textbf{A}$ and $\textbf{b}$ to be the constraint equalities (right and left side respectively). Say we pick a set of $m$ linearly independent columns ($\textbf{A}$'s [[Matrix rank|rank]] therefore is $m$) and make matrix $\textbf{B}$. The matrix is [[Singularity|non-singular]], therefore has a solution $\textbf{x}_{\textbf{B}}$:
$$
\textbf{B}\textbf{x}_{\textbf{B}}=\textbf{b}.
$$
We have $\textbf{x}=(\textbf{x}_{\textbf{B}},0)$. Basically, to make $\textbf{x}$, start with $\textbf{x}_{\textbf{B}}$ and fill the rest with zeros. Matrix $\textbf{B}$ is called a [[basis]], since its columns are [[Linear independance|linearly independent]] and therefore it is 
a basis. $\textbf{x}_{\textbf{B}}$ is a way to express these independent vectors as a [[linear combination]] to make $\textbf{b}$ and is called a basic solution. 


This might seem like magic, but we have to make some assumptions for this to work:
1. We assume $n>m$, that is, we have more variables than constraint equalities. 
2. Rows of $\textbf{A}$ are [[Linear independance|linearly independent]].
3. Variables must be non-negative.
Under these assumptions, $\textbf{A}\textbf{x}=\textbf{b}$ has a solution and that solution is basic.
## Basic variable
Variable is called basic if it is set to zero to solve an system of linear equations
# Feasible solution
A solution $\textbf{x}$ is said to be *feasible* if satisfies
$$
\textbf{A}\textbf{x}=\textbf{b},\ \textbf{x}\geq 0,
$$
which represent a [[LPP|linear program]] in a standard form.