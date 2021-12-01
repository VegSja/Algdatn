#todo 

# Single-source shortest paths in DAG 
*Based on the premise: By [[(10) Single source shortest path problem#Relaxation | relaxing]] the edges of a weighted directed [[Acyclic graph]] (DAG), according to a topological sort of its vertices we can compute shortest path from a single source in $\Theta(V+E)$ time*

- Shortest paths are always well defined in a DAG

## How the algorithm works
1. [[Topological sort]] the dag
2. Make one pass over each vertex
	1. Relax each edge that leaves the vertex
![[Pasted image 20211025124832.png]]

![[Pasted image 20211025124845.png]]

## Running time
The total running time is 

==$\Theta (V+E)$== -> This is also running time of [[Topological sort]]


## References