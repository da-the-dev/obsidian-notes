One of the methods to find a [[Types of solutions|basic feasible solution]] for [[Transportation problems#Solution|Transportation simplex]].
# Algorithm
1. For a given tableau, find the northwester-most corner. Allocate the largest amount of either supply or demand to that cell. Cross out the exhausted (the one with zero) row or column. Conflicts when both row and column are zero are solved arbitrarily.
2. Continue crossing out rows or columns until the last cell remains. Fill it with whatever supply or demand remains.
# References
https://www.youtube.com/watch?v=v-JcpuQOfjk&list=PL3rXWhnlnXkstBqfpF7plaBM6rjo4PguC&index=4