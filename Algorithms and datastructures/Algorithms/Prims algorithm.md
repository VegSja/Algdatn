#todo 

# Prims algorithm
**Usage**: *Find where to make a cut in the [[(9) Generic Minimal spann trees]] problem. Hence solving the problem*

**In general**: *Build a tree slowly; one light edge around the tree is always safe.*
**In other words:** *Always choose the minimum cost edge which is connected to the already formed tree.*

- Can be implemented using traversal
- Using a min-[[Priority queues]]
	- The priority is the weight of the lightest edge between the node and the tree

![[Pasted image 20211019113759.png]]

## Running time
==$O(ElgV)$==

## Related to
[[(9) Generic Minimal spann trees]]
[[(7) Greedy algorithms]]

## References
https://www.youtube.com/watch?v=Uj47dxYPow8