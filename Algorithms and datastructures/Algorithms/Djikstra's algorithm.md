#todo 

# Djikstra's algorithm
*Solves the single-source shortest-path problem in a weighted directed graph, when we assume all edge weights are nonnegative*

Essentially a faster version of [[Bellmann-Ford algorithm]]

Uses  a [[(7) Greedy algorithms]] strategy

Resembles both [[Breadth-first search]] and [[Prims algorithm]]

## How it works
- Maintains a set $S$ of vertices whose final shortest path weigth from source have already been determined
	- Empty in the beginning
- Repeadetly select vertex $u \in V - S$ with the minimum shortest path estimate ([[(7) Greedy algorithms|greedly]])
	- Adds u to S
	- [[(10) Single source shortest path problem#Relaxation|relaxes]] all edges leaving u

![[Pasted image 20211025125239.png]]
![[Pasted image 20211025125248.png]]


## Running time
| Scenario                    | Running time  |
| --------------------------- | ------------- |
| Using fibonacci heap        | $O(VlgV + E)$ |
| Using [[Heap\| Binary heap]] |   $O((V+E)lgV)$            |


## References
https://www.youtube.com/watch?v=_lHSawdgXpI&t=18s