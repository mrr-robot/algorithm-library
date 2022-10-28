# <h1 align="center">Breadth First Search 


### 1. Pseudocode
```Python
function BREADTH-FIRST-SEARCH(problem) returns a solution node or failure
	node <- Node(problem.INITIAL) 
	if problem.IS-GOAL(node.STATE) then return node
	frontier <- a FIFO queue, with node as an element
	reached <- {problem.INITIAL}
	while not IS-EMPTY(frontier) do 
		node <- POP(frontier)
		for each child in EXPAND(problem, node) do
			s <- child.STATE
			if s is not in reached then
				add s to reached
				add child to frontier
		return failure

function UNIFORM-COST-SEARCH(problem) returns a solution node, or failure
	return BEST-FIRST-SEARCH(problem, PATH-COST) 
```
