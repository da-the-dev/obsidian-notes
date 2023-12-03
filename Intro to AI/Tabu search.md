Another algorithm for [[searching]] for solutions
# Algorithm
- Take some initial a solution
- Find neighbors for the given solution (this step is problem-specific)
- Swap neighbor
- Check the value of the objective function
	- If it became better, update the solution and add the swapped neighbor to the tabu list (cannot be used anymore)
	- If it became worse, reverse changes
- Repeat until tabu list is full, or exhausted the number of steps
# References
https://www.youtube.com/watch?v=A7cTp1Fhg9o
https://www.geeksforgeeks.org/what-is-tabu-search/