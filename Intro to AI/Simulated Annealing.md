One of the algorithms for [[searching]] for solutions. It is based on properties of metal working. There, the metal is heated and then cooled to make it workable or stronger.
# Simulation
- Set down a number of search points
- Points move dependent upon the temperature applied
- They move about the space based on a temperature which is slowly reducing over time
	- This allows for large movement at the beginning of the algorithm and reduces into smaller and smaller movements as time goes on
- Two Types
	- Temperature controls size of step
	- Temperature controls the acceptance of a step
# Algorithm
- Start at an initial temperature value (usually something hot) and create a random initial solution
- Until temperature is cool
	- Make a change to the current solution (neighbor) based on the temperature
		- Decide if we move to this neighboring solution
			- Neighbor solution is better OR
			- Rand_Distribution() < tem
	- Decrease the temperature