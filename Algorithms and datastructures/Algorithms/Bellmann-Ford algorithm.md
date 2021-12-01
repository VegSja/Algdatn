#todo 

# Bellmann-Ford algorithm
*Solves [[(10) Single source shortest path problem]] in a general case where edges may be negative. Making it slower than [[Djikstra's algorithm]], but more versitile*
- Returns a boolean
	- True --> There is no negative-weight cycles reachable from source
		- Can solve the problem
- Uses [[(10) Single source shortest path problem#Relaxation | relaxation]] to update the shortest path
- Follows a [[(6) Dynamic Programming]] solution


## How it runs
1. Select source vertex
2. Select any edge (make sure every edge is selected in the end)
	1. Select a new vertex and relax its edges
	2. Repeadtly do this $|V|-1$ times
		1. When there is no change when relaxing the edges on one iteration - We are finished
		3. If relaxation contionous more than $|V|-1$ times we have negative cycle


![[Pasted image 20211025122025.png]]

![[Pasted image 20211025122037.png]]

## Complexity
==Takes $O(|V||E|)=O(n²)$ time==
## References
- https://www.youtube.com/watch?v=obWXjtg0L64
- [Guden selv](https://www.youtube.com/watch?v=FtN3BYH2Zes&t=7s)