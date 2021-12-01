#TOC  

# Single source shortest path problem
*We are given a weigthed directed graph. The shortest path from vertex v to vertex w is defined as the path with the smallest weight. We want to find the shortest path from a given source vertex to each vertex in the graph*
- Could use [[Breadth-first search]] on unweighted graphs

## [[(6) Dynamic Programming#Optimal substructure | Optimal substructure ]] of shortest path
- [[Djikstra's algorithm]] is an greedy algorithm

## Negative weighted edges
- If contains negative-weigthed cycle --> Shortest path weigths are not well defined
- [[Bellmann-Ford algorithm]] accepts negative-weigth edges, and produce a correct answer as long as no negative-weigth cycles are reachable from the source


## Cycles
- Cannot contain cycles
	- The graph we compute on can contain cycles, however the shortest path cannot
	- We only look at simple paths

## Representing shortest paths
We wish to compute the vertices on a shortest path as well
- Give vertices attributes
	- **Predecessor**: $v.\pi$
		- In the midst of algorithms --> Might not indicate shortest path
		- Will at termination

> **Shortest path tree** rooted at S
> 1. V' is the set of vertices reachable from s in G
> 2. G' forms a rooted tree with root s
> 3. For all $v \in V'$, the unique simple path from s to v in G' is a shortest path from s to v in G

Doesnt need to be unique

## Relaxation
*Give each vertex the attribute $v.d$ which is an upper bound of shortest path from source to v*

- When we find a path to this vertex shorter than what is already discovered --> Update $v.d$

![[Pasted image 20211116155124.png]]

## Properties of shortest path and relaxation
See page 650 in pdf


## [[Single-source shortest paths in DAG]]

## References