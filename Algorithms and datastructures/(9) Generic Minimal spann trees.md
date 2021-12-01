#TOC  

# Generic Minimal spanning trees
*Introduce weights of the edges. These are often refered to as lengths or costs*
**Goal:** Connecting the nodes in the cheapest possible way, hence creating a spanning tree

Uses [[Disjoint sets]]

**Input:** An undirected graph G=(V,E), and a weigth function: $w: E \rightarrow R$

**Output**: An acyclic subset $T \subseteq E$ which connects the nodes in V and minimate the sum of the weights

*T is an spanning tree for G *

---
## Subgraphs
*Graphs consisting of subsets of the nodes and edges in the original graph*

## Spanning graphs
*Is a subgraph with the same set of nodes as the original graph*

## Spanning forests
*A [[Acyclic graph|acyclic]] spanning graph*

## Spanning trees
*Is a connected spanning forest*
> Cannot find spanning trees for a forest


![[Pasted image 20211019105143.png]]

---
## Finding Generic-MST
- subinstance: Connect the rest, cheapest possible way
- Decompisition: a set of edges we choose between
- Each alternative gives a new, smaller subinstance

```
Generic-MST(G, w) 
1 A = !A 
2 while A does not form a spanning tree 
3 	find an edge (u, v) that is safe 					 
4   A=A U {(u, v)} 
5 return A
```

>**Choosing an edge over a cut**
>You whould choose the lightest possible cut
>We can choose [[(7) Greedy algorithms|greedily]]

![[Pasted image 20211019111614.png]]


## How to choose a *cut*
- [[Kruskals algorithm]]
- [[Prims algorithm]]

## References
[Guden selv](https://www.youtube.com/watch?v=4ZlRH0eK-qQ&t=827s)