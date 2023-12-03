One of the methods for [[searching]] for a solution to a problem 
# Steps
- Move towards the goal, if you reach a position which is going to be less
successful – stop and move back up the tree (backtrack, retrace your steps)
- Recursive definition of a depth first search of a backtrack:
- SearchTreeBacktrack(State, Move, visited list)
	- New State <- Apply Move
	- If (New State == goal) – return TRUE
	- If (New State causes an invalid path to goal/or costs too much) – return FALSE
	- Else
		- If neighbouring states is empty - return FALSE
		- For each of the MOVE on neighbouring states not in visited list
			- If SearchTreeBacktrack(Neighbouring states, MOVE, visited list + State) return TRUE;