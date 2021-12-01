#TOC  

# All-pairs shortest path
*Compute a matrix where entry in u's row and v's column should be the weigth of a shortest path from u to v*
- Could use [[Djikstra's algorithm]] or [[Bellmann-Ford algorithm]] on each vertex --> Slow
- We allow negaitve-weigthed edge, but assume the graph contains no negative-weight cycles

[[The Floyd-Warshall algorithm]]
[[Johnson's algorithm]]

![[Pasted image 20211117115725.png]]

## References