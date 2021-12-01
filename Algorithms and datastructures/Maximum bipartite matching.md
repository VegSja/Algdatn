#todo 

# Maximum bipartite matching

## The maximum-bipartite-matching problem
### Matching
*Given an undirected graph $G=(V,E)$ a **matching** is a subset of edges $M \subset E$ such that for all vertices $v \in V$, atmost one edge of $M$ is incident on v.*

### Bipartite graph
*Graphs in which the vertex set can be partitioned into $V = L \cup R$ where $L$ and $R$ are disjoint and every edge goes between L and R*

## Finding a maximum bipartite matching
- Construct a flow network G' in which flows correspond to matchings
	- Run [[The Ford-Fulkerson method]] on this network
![[Pasted image 20211201153633.png]]

> **The integrality theorem**
> If the capacity function c takes on only integral values, then the maximum flow f produced by the Ford-Fulkerson method has the property that $|f|$ is an integer. Moreover, for all vertices *u* and *v*, the value of $f(u,v)$ is an integer
>
>**What it tells us**
>*If every capacity is an integer:*
>- The max flow is an integer value
>- Ford-Fulkerson method finds a max flow in which f(u,v) is an integer for all edges (u,v)

## References