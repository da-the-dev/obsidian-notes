One of the methods to find a [[Types of solutions|basic feasible solution]] for [[Transportation problems#Solution|Transportation simplex]].
# Algorithm
1. For a given tableau, find the cell with the lowest cost. Conflicts when two or more cell are found with the same cost are solved arbitrarily. Allocate the largest amount of either supply or demand to that cell. Cross out the exhausted (the one with zero) row or column. Conflicts when both row and column are zero are solved arbitrarily.
2. Continue crossing out rows or columns until the last cell remains. Fill it with whatever supply or demand remains.
# References
https://www.youtube.com/watch?v=YxyTSBs19NE&list=PL3rXWhnlnXkstBqfpF7plaBM6rjo4PguC&index=3