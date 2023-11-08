# Loops
An order sequence of at least 4 cells in called a loop if:
1. Any two consecutive cells lie in either the same row or same column
2. No three or more cells lie in the same row or column
3. The last cell lies in either the same row or column as the first cell
# Loop pivoting
1. Determine an entering variable
2. Find the only possible loop with that variable
3. Mark odd and even cells (start counting from 0).
4. Find the **odd cell** with the smallest value and call it $\theta$. This is the leaving variable
5. Subtract $\theta$ from all odd cells and add $\theta$ to all even cells.
# References
https://www.youtube.com/watch?v=JdYD2EyCs04&list=PL3rXWhnlnXkstBqfpF7plaBM6rjo4PguC&index=5