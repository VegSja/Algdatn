#todo 

# Depth-first search
Search deeper in the graph whenever possible and back propegate when branch is finished

Uses an [[Stack]] datastructure

- Sets v's **predecessor attribute $v.\pi$ to u**
- Colors vertices
	- White: init value
	- Grey: Discovered in the search
	- Black: When finished (on return to node)
- Timestamps each vertex
	- v.d - When v was discovered
	- v.f when the search finishes examining v's adjacency list
- Might be a directed or undirected graph
![[Pasted image 20211011165428.png]]
![[Pasted image 20211011165437.png]]

==$\Theta(V+E)$==

## Properties
- Vertex v is a descendant of vertex u in the depth-first forest if and only if v is discovered during the time in which u is gray


> **Parenthesis structure**
> In any depth-first search of a graph $G = (V,E)$, for any two vertices u and v, exactly one of the following three conditions holds:
> - The intervals $[u.d, u.f]$ and $[v.d, v.f]$ are entirely disjoint, and neither u nor v is a descendant of the other in the depth-first forest
> - The interval $[u.d, u.f]$ is contained entirely within the interval $[v.d, v.f]$ and u is a descendant of v in a depth-first tree
> - The interval $[v.d, v.f]$ is contained entirely within the interval $[u.d, u.f]$ and v is a descendant of u in a depth-first tree

> **Nesting of descendants' intervals**
>  Vertex v is a proper descendant of vertex u in the depth-first forest for a graph G iff $u.d \lt v.d \lt v.f \lt u.f$

> **White-path theorem**
> *In a depth-first forest of a graph $G = (V,E)$*, vertex v is a descendant of vertex u 
> $\Leftrightarrow$
>  at the time u.d that the search discovers u, there is a path from u to v consisting entirely of white vertices

### Classification of edges
1. **Tree edge** - Edges in the depth-first forest. Edge (u,v) is a tree edge if v was first discovered by exploring edge (u,v)
	1. Visit a new vertex via this edge
	2. WHITE
2. **Back edge** - Edges (u,v) connecting vertex u to ancestor v in a depth-first tree. Self loops can also be backedges
	1. GRAY
	2. Goes back to its ancestor
3. **Forward edges** - Nontree edges (u,v) connecting a vertex u to a descendant v in a depth-first tree
	1. BLACK
	2. Goes from a node to a decendant
4. **Cross edges** - All other edges. Can go between vertices in the same depth-first tree, as long as one vertex is not an ancestor of the other, or they can go between vertices in different  depth-first trees
	1. BLACK
	2. All the other edges

> In a depth-first search of an undirected graph G, every edge of G is either a tree edge or a back edge
## References