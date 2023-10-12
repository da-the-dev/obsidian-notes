A [[graph]] traversal and path search algorithm.
Graph as weighed edges and the goal is to reach the destination in the least amount of steps. To help to choose the path, we need some heuristic for each node. 
$$
p(v) = dist(v) + h(v)
$$
# Example
A mouse needs to traverse a maze to find cheese. Instead of traversing the maze completely, it can use some other heuristic, like smell for example. We can represent the maze as a weighted graph. The smell value (heuristic) will be assigned for each node from 100 to 0 (the lower the better). Now, we can compute $p(v)$ for each node. 
Starting for a given node, we add it to the queue. We compute $p(v)$, pop the node off the queue and add its children. Compute $p(v)$ for them, take the smallest value. Pop this node off and add its children. Repeat the process until we reach the goal.

# References
https://www.youtube.com/watch?v=71CEj4gKDnE
