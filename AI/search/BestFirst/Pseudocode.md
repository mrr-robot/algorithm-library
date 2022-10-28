# <h1 align="center">Best First Search 

### 1. Pseudocode 

```Python
  function ITERATIVE-DEEPENING-SEARCH(problem, depoth) returns a solution node or failure
    for depth = 0 to infinity do
		result <- DEPTH-LIMITED-SEARCH(problem, depth)
		if result != cutoff then return result
              
  function DEPTH-LIMITED-SEARCH(problem, l) returns a node or failure or cutoff
	frontier <- a LIFO queue (stack) with NODE(problem.INITIAL) as an element
	result <- failure
	while not IS-EMPTY(frontier) do 
		node <- POP(frontier)
		if problem.IS-GOAL(node.STATE) then return node
		if DEPTH(node) > l then 
			result <- cutoff
		else if not IS-CYCLE(node) do 
			for each child in EXPAND(problem, node) do
				add child to frontier
	return result

```
