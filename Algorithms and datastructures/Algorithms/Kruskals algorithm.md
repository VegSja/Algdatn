#todo 

# Kruskals algorithm
**Usage**: *Find where to make a cut in the [[(9) Generic Minimal spann trees]] problem.*
**Idea:** *Given a graph, always choose the minimal edge as long as it does not form cycles*

**In general**: 
- Builds forests and then connect
	- *An edge with a minimal weight in the set of the remaining edges is safe as long as it doesn't create cycles*


>**In other words**: *Always choose the minimal cost edge as long as it does not create a cycle*

## How it works
1. Uses Union-by-rank and path compression from [[Disjoint sets]]
![[Pasted image 20211019112614.png]]

### Pseudocode
```
MST-Kruskal(G, w) 
1 A = Ø 
2 for each vertex v in G.V 
3 	Make-Set(v) 
4 sort G.E by w 
5 for each edge (u, v) in G.E 
6 	if Find-Set(u) != Find-Set(v) 
7 		A=A U {(u, v)} 
8 		Union(u, v) 
9 return A
```


## Running time
- Needs to iterate over $|E|$ edges to find the minimal edge
- Will select $|V|-1$ edges

$O(|V||E|) = O(n^2)$

When using min-heaps:
- Select edge: $lgV$
- Number of selects: $E$

==$\underline{\underline{O(ElgV)}}$==

## Related to
[[(7) Greedy algorithms]]
[[(9) Generic Minimal spann trees]]

## References