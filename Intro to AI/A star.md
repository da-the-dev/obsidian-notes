A [[graph]] traversal and [[Searching|search]] algorithm.
[[Graph]] has weighed edges and the goal is to reach the destination in the least amount of steps. To help to choose the path, we need some heuristic function for each node. 
$$
p(v) = dist(v) + h(v)
$$
This means that the score for a node is the distance from that node (Euclidean distance) + some heuristic function $h(v)$. The lower the score the better.
# Example
A mouse needs to traverse a maze to find cheese. Instead of traversing the maze completely, it can use some other heuristic, like smell for example. We can represent the maze as a weighted graph. 
The smell value (heuristic) will be assigned for each node from 100 to 0 (the lower the better). Now, we can compute $p(v)$ for each node. 
- Starting for a given node, we add it to the queue.
- We compute $p(v)$, pop the node off the queue and add its children. 
- Compute $p(v)$ for them, take the smallest value.
- Pop this node off and add its children.
- Repeat the process until we reach the goal.
# Lecture algorithm explanation
- A node contains a location, a cost, and a parent
- Initialize a set CLOSED to be null
- Initialize a priority queue based on cost of a node called OPEN to be the starting location, set cost = 0

- While OPEN is non-empty do
	- Current <- Pop OPEN.top
	- For all neighboring locations X
	- If not in (BLOCKED or CLOSED)
		- If not in OPEN
			- X.cost = current.cost+1
			  X.parent = current
			- Push X to OPEN
	- Else if X is in OPEN
		- If current.cost+1 < OPEN.X.cost // we found a better path
		- OPEN.X.cost = current.cost+1
		- OPEN.X.parent = current
	- END FOR ALL X
	- Push Current to CLOSED
![[Pasted image 20231203220315.png]]
# References
https://www.youtube.com/watch?v=71CEj4gKDnE
https://www.youtube.com/playlist?list=PLFt_AvWsXl0cq5Umv3pMC9SPnKjfp9eGW
