#todo 

# Breadth-first search
*Searches systematically exploring the edges of G to "discover" every vertex that is reachable from the source vertex s*

## Attributes
- Works on both directed and undirected graphs
- An ==$O(V+E)$== runtime

## How it works
- Discovers all vertices at distance k before disovering all at distance k+1
- Colors each vertex
	- White: Not discovered
	- Grey: Discovered but not every neighbour have been discovered
	- Black: Discovered and all neighbours are discovered
- Assumes [[Adjacency-list representation]]
- Uses [[Queues]] to manage set of grey vertices
![[Pasted image 20211011153739.png]]
![[Pasted image 20211011153749.png]]

## Breadth-first tree
- The simple path in this tree from s to v corresponds to a "shortest path" from s to v
- When discovering vertex v on already discovered vertex u, they are added to the tree
	- u is the **Predecessor/Parent** of v

## Shortest path property
**Corretness of breadth-first search**
Let $G = (V,E)$ be a directed or undirected graph and suppose that BFS is run on G from a given source vertex $s \in V$. Then, during execution BFS discoveres evert vertex $v \in V$ moremover for any vertex $v != s$ that is reachable from s, one of the shortest paths from s to v is a shortest path from s to $v.\pi$ followed by the edge $(v,\pi,v)$
## References