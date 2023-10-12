An algorithm to [[Backtracking|backtrack]] a [[Game theory|game]] and find the optimal path of choices to win.
Build a decision tree that has some depth. Define a static evaluation (some number) for the leaves. Then go back up the tree assigning the value of the parent nodes to be maximum or minimum of the child nodes. We can then use this tree to play optimally.

![[Pasted image 20231009070041.png]]