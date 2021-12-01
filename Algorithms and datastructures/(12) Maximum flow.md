#TOC  

# Maximum flow
**Maximum-flow problem** --> *Given a [[Flow network]] with a source and sink we wish to find a flow of maximum value. Essentially a bottleneck value of a graph*

Also finds the min-cut

## Solving maximum-flow problems
[[The Ford-Fulkerson method]]

## Maximum bipartite matching
[[Maximum bipartite matching]]
1. Create a flow network
	1. Edges has capacity of 1
2. Add a super source and a super source
	1. The values of these depends on the problem you are trying to solve
3. Use [[The Ford-Fulkerson method]] to find the maximum flow
## References