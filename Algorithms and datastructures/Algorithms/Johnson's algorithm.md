#todo 

# Johnson's algorithm
*Compute the solution to [[(11) All-pairs shortest path]], and is asymptotically the fastest algorithm for this when we have a sparse graph*
- $O(V^2lgV + VE)$
- For sparse graphs it is asymtotically fastest
- Returns either:
	- Matrix of shortest path weights
	- Report if graph contains negative-weigth cycle

## Reweighting
*This is about giving edges new values.*
> **IMPORTANT TO NOTE:**
> This is not the same as [[(10) Single source shortest path problem#Relaxation|relaxation]]!!

The basic principle of this algorithm is:

- If all edge weights in a graph is nonnegative
	-	Can use [[Djikstra's algorithm]] once from each vertex
- If contains negative weigths
	- Define new set of weigths
		- Then use [[Djikstra's algorithm]]
	
> **Must satisfy**
> 1. Preserve shortest path
> --> *Use on each edge: $\hat{w}(u,v) = w(u,v) + h(u) - h(v)$*
> 2. For all edges $(u,v)$, the new weigth $\hat{w}(u,v)$ is nonnegative
> --> Use the previous formula




## Computing all-pairs shortest paths
- Uses the [[Bellmann-Ford algorithm]] and [[Djikstra's algorithm]] as subroutines
- Add new vertex $s$ connected to every other vertex
	- Use bellman-ford/djikstra to compute shortest path from $s$ to every other vertex
		- Use this to reweigth each edge -> Now nonnegative
			- Can run [[Djikstra's algorithm]] once for each vertex 

![[Pasted image 20211111145933.png]]
![[Pasted image 20211111145943.png]]

> **Cool things to note**
> The addition of the vertex s does not actually change the solution to the problem since it only has no directed edges towards it. Making it invisible

## Running time
| Situation           | Complexity   |
| ------------------- | ------------ |
| Johnson's algorithm | $O(VE)$ time |

## References
https://www.youtube.com/watch?v=xc2ua8sQAoE