#todo 

# Adjacency-list representation
*$Adj[u]$ consists of all the vertices adjacent to u in G*

### Attributes
> **Directed graphs**
> Sum of the lengths of all the adjacency lists is |E|


> **Undirected graph**
> Sum of the lengths of all the adjacency lists is 2*|E|

> **Memory**
> $\Theta(V+E)$
## Advantage
- Memory
- *sparse* graphs
	- Sparse graphs: $|E| << |V|^2$
- When we need to know if there is an edge connecting two given vertices
## Disadvantage
- No quick way to determine wheter a given edge is present in the graph
	- [[Adjacency-matrix representation]] is better here
## References