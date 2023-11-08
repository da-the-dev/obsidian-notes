One of the methods to find a [[Types of solutions|basic feasible solution]] for [[Transportation problems#Solution|Transportation simplex]].
# Algorithm
1. For each row and column calculate a "penalty" by subtracting the **smallest** cost from the second smallest in the same row or column
2. Find the **largest** penalty and then find the cell with the **smallest** cost in that row or column. Allocate as much as possible to that cell. Cross out row or column with zero.
3. Go back to step 1 and repeat until one uncrossed cell remains.
# References
https://www.youtube.com/watch?v=6MB4ns6Evak&list=PL3rXWhnlnXkstBqfpF7plaBM6rjo4PguC&index=2