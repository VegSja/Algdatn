#todo 

# The Ford-Fulkerson method
*We find some augmenting path p and use p to modify the flow f*
![[Pasted image 20211108145225.png]]
![[Pasted image 20211108145237.png]]

## Running time
$O(E|f^*|)$

## The Edmonds-Karp algorithm
- Using [[Breadth-first search]] instead
## Residual networks
*Consists of edges with capacities that represents how we can change the flow on edges of G*
- Is not a [[Flow network]]
- The only edges of G that are in $G_f$ can admit more flow
- Decreasing flow on edge
	- Add reverse edge. Sum of edges = flow
- A flow in this network provides a roadmap for adding flow to the original flow network


> **Augmentation of flow**
> f is flow in G and f' is flow in the corresponding residual network
> $(f\uparrow f')(u,v)=f(u,v)+f'(u,v)-f'(v,u) \ \ \  if (u,v)\in E$

### From [Youtube](https://www.youtube.com/watch?v=LdOnanfc5TM)
**Residual graphs**: *The graphs containg residual edges*.

**Residual capacity**: The maximum amount we can increase the flow on each edge in an augmenting path p
$c_f(p)=min\{c_f(u,v):(u,v)$ is on p$\}$
>*Essentialy we raise the flow on the path by the value of the edge with the smallest capacity*


**Residual edges**: *The edges going backwards in the network from the original edge direction, marked in red:*
![[Pasted image 20211117130714.png]]

> **Why residual edges?**
> To defend against bad choices in augmented paths
- We also need to adjust the residual edges


## Augmenting paths
*Is a simple path with unused capacity greater than 0 from source s to sink t in the residual network $G_f$*
- Can only flow through edges which have not reached it's capacity

If we augment $f$ by $f_p$ we get another flow in G whose value is closer to the maximum.

## Choice of augmented path
This is unspecified, choice of user. It is recommended to use [[Breadth-first search]]

## Cuts of flow networks
*A partition of V into S*
- **Netflow**
- **Minimum cut** -> *a cut whose capacity is minimum over all cuts of the network*

>The value of any flow f in a flow network G is bounded from above by the capacity of any cut of G


> ## IMPORTANT: Max-flow min-cut theorem
> If f is a flow in a flow network G = (V,E) with source s and sink t, **then the following conditions are equivalent:**
> - f is a maximum flow in G
> - The residual network $G_f$ contains no augmenting paths.
> - $|f|=c(S,T)$ for some cut (S,T) of G
>
> ### What it tells us
>*That the maximum flow through any network from a given source to a given sink is exactly the sum of edge weight that generate the min-cut*



## Running time
**f:** *Maximum flow*
**E:** *Number of edges*

| Algo to find augmented path            | Run time        |
| -------------------------------------- | --------------- |
| [[Depth-first search]]                 | O(fE)           |
| [[Breadth-first search]] (Edmond Karp) | O($E^2 log(V)$) |

## References
https://www.youtube.com/watch?v=LdOnanfc5TM