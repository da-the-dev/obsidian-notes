Also called full differential, is a type of [[Linear first order differential equations|first order differential equation]]:
$$
M(x,y)dx + N(x,y)dy = 0
$$
This can be interpreted as
$$
M(x,y)+N(x,y) \frac{dy}{dx}=0
$$
where $x$ is an independent variable, or as
$$
M(x,y) \frac{dx}{dy}+N(x,y)=0
$$
where $y$ is an independent variable.

The solutions will often have to be implicit, so let's assume $F(x,y)=c$, where $c$ is a constant.

# Prerequisites 
## Theorem (Differential solution)
If $F=F(x,y)$ as a continuous partial derivatives $F_{x}$ and $F_{y}$, then $F(x,y)= c$ is an implicit solution of the differential equation:
$$
F_{x}(x,y)dx + F_{y}(x,y)dy = 0
$$
## Theorem (The Exactness Condition)
Suppose $M$ and $N$ are continuous and have continuous partial derivatives $M_{y}$ and $N_{x}$. Then
$$
M(x,y)dx + N(x,y)dy = 0
$$
is exact iff
$$
M_{y}(x,y) = N_{x}(x,y)
$$
# Solution
Equation
$$
M(x,y)dx + N(x,y)dy = 0
$$
1. Check that equation satisfies the exactness condition. If not, do not proceed any further
2. Integrate
   $$
\int M(x,y) \, dx  = G(x, y) + \phi(y) = F(x,y)
$$
3. Now, since we kinda know $F(x,y)$, we can take a derivative on $y$   
$$
\frac{ \partial F }{ \partial y } = [G(x,y) + \phi(y)]'_{y}= N(x,y)
$$
4. Now solve for $\phi(y)'_{y}$
5. Once obtained, integrate 
$$
\int  \phi(y)'_{y} \, dy = \phi(y)
$$
6. Substitute $\phi (y)$  into step 2 to get $F(x,y)$ 