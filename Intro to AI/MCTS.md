# Idea
- The focus of MCTS is on the analysis of the most promising moves, expanding the search tree based on random sampling of the search space
- The application of MCTS in games is based on many playouts. In each playout, the game is played out to the very end by selecting moves at random
- The final game result of each playout is then used to weight the nodes in the game tree so that better nodes are more likely to be chosen in future playouts
# Monte Carlo Tree Search
- MCTS builds a statistics tree (detailing value of nodes) that partially maps onto the entire game tree
- Statistics tree guides the AI to look only at the most "interesting nodes" in the game tree
- Full Monte Carlo tree search employs this principle recursively on many depths of the game tree. Each round of MCTS consists of four steps:
	1. Selection
		- Start from root $R$ and select successive child nodes down to a leaf node $L$. 	
	2. Expansion
		- Unless $L$ ends the game with a win/loss for either player, either create one or more child nodes or choose from them node $C$
	3. Simulation
		- Play a random game from node $C$. The steps for a game a chosen randomly out of those that are possible. This game simulation is what is called a playout.
	4. [[Backpropagation]]
		1. Use the result of the playout to update information in the nodes on the path from $C$ to $R$
# Exploration vs Exploitation
The main challenge for this algorithm arises when balancing [[Exploration vs Exploitation]]. Usually the UCT (Upper Confidence Bound 1 applied to trees) formula is used:
$$
\dfrac{w_{i}}{n_{i}}+c\sqrt{ \dfrac{\ln N_{i}}{n_{i}} }
$$
where:
- $w_{i}$ is the number of wins for the node after the $i$-th move
- $n_{i}$ is the number of simulations for the node after the $i$-th move
- $N_{i}$ is the total number of simulations for the parent node
- $c$ is the exploration parameter – usually $\sqrt{ 2 }$, but often $c$ is something different
# Pros. vs Cons.
## Pros
- No evaluation function, meaning the algorithm can be effectively used for all sorts of different tasks
- Achieves better results than classical algorithms in games with a high branching factor
- Shortens the search time for large tasks
## Cons
- In certain positions, there may be moves that look superficially strong, but that actually lead to a loss via a subtle line of play
# References
https://www.youtube.com/watch?v=Fbs4lnGLS8M