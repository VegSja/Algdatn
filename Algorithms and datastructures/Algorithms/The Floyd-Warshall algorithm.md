#todo 

# The Floyd-Warshall algorithm
*Compute a solution to the [[(11) All-pairs shortest path]] problem. Negative edges allowed*

Follow [[(6) Dynamic Programming]] process to develop the algorithm

**Intermediate vertex**: Of a simple path $p = [v1, ..., vl]$ is any vertex of p other than $v_1$ of $v_l$

- Exploits a relationship between path p and shortest paths from i to j
	- Depends on whether or not k is an intermediate vertex of path p

![[Pasted image 20211111135100.png]]

## Computing shortest path matrix by [example](https://www.youtube.com/watch?v=oNI0rf2P9gE&t=399s)
1. Prepare matrix $D^0$, contains edge weights
	1. Absence of edge --> $\infty$


![[Pasted image 20211117113527.png]]

2. Consider intemediate vertices of vertex 1
	1. Check if there is a shorter path by visiting vertex 1


![[Pasted image 20211117113957.png]]

3. Repeat this process, when computing $A^2$ use $A^1$ instead of $A^0$
4. $A^4$ will contain the shortest path


## Constructiong a shortest path
### Compute predecessor matrix after
- Compute the matrix D of shortest-path weigths, and then construct the predecessor matrix $\Pi$

### Compute predecessor matrix during
- Compute a sequence of matrices $\Pi^{(0)},..., \Pi^{(n)}$ where $\Pi = \Pi^{(n)}$
- Define $\pi_{ij}^{(k)}$ as the predecessor of vertex j on a shortest path from vertex i
![[Pasted image 20211111143449.png]]

## Running time
| Algorithm         | Runtime        |
| -------------- | -------------- |
| Floyd-Warshall | $\Theta (V^3)$ |

## Transistive closure of a directed graph
**Transistive closure of graph G:** $G^* = (V,E^*)$  where 

$E^* = \{(i,j):$ There is a path from vertex $i$ to vertex $j$ in $G\}$

| Method                          | Runtime      |
| ------------------------------- | ------------ |
| Floyd-Warshall                  | $\Theta(n³)$ |
| Floyd-Warshall with aritchmetic *Saves space* | $\Theta(n^3)$             |

![[Pasted image 20211111144043.png]]

## References
https://www.youtube.com/watch?v=oNI0rf2P9gE