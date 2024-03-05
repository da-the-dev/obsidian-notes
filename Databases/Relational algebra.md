---
aliases:
  - Union
  - Intersection
  - Set difference
  - Cartesian product
  - Select
  - Project
  - Division
  - Set functions
---
# Set operations
## Union
Takes all rows that are either in one table, or the other, or both. Drops duplicates.
$$
A \cup B
$$
![[Pasted image 20240227153315.png|600]]
## Intersection
Takes all rows that exist in both tables.
$$
A \cap B
$$
![[Pasted image 20240227153421.png|400]]
## Set difference (Minus)
Takes are rows that are in the first table, but not in the second one.
$$
A - B
$$
![[Pasted image 20240227153550.png|400]]
## Cartesian product
Like the Cartesian product for mathematical relations
$$
A \times B
$$![[Pasted image 20240227155338.png|600]]
# Database specific operations
## Select
Selects a rows of the relation according to a condition $\theta$. Preserves columns.
$$
\sigma_{\theta}(A)
$$
![[Pasted image 20240227152641.png|600]]
## Project
Selects columns from a relation and drops others.
$$
\pi_{\theta}(A)
$$
![[Pasted image 20240227152754.png|600]]
## Joins
![[Joins]]
## Division
**Formally:**
> Produces a relation $R(X)$ that includes all tuples $t[X]$ in $R_{1}(Z)$ that appear in $R_{1}$, in combination with every tuple from $R_{1}(Y)$, where $Z=X \cup Y$.

https://www.youtube.com/watch?v=-Dp2rC3YkU0
# Set functions
- sum
- avg
- count
- any
- max
- min
# References
- https://www.youtube.com/watch?v=-Dp2rC3YkU0