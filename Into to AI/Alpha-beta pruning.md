An optimization algorithm that allows us to skip computation for the [[Minimax]] algorithm. 
# Idea
$\alpha$ is the maximum value we can obtain
$\beta$ is the minimum value we can obtain 

$\alpha$ is updated at $min$ points of the graph
$\beta$ is updated at $max$ points of the graph

$\alpha$ and $\beta$ are maintained while we traverse the graph

Once for a given node $\alpha \geq \beta$, the untraversed children of the node are pruned.
# References
https://www.youtube.com/watch?v=_i-lZcbWkps