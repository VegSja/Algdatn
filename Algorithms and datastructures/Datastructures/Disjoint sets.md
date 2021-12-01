#todo 

# Disjoint sets
*For å finne ut om 2 noder tilhører samme mengde*

Used to figure out [[(9) Generic Minimal spann trees]]

- Representerer mengder med trær
	- Mengden representatnt er rot noden
		- Det er her alle foreldre pekerne ender opp


## Operations
**FIND-SET(v)** -> What is the representant of the collection
	- Need a self-loop to remove special happening
	- v will get the root as a parent
	
```
Find-Set(x) 
1 if x != x.p 
2 	x.p = Find-Set(x.p) 
3 return x.p
```
	
**Make-Set(x)** -> Create a set such that the node represents the set {x}
![[Pasted image 20211019103507.png]]

**Union** --> Combine two trees/sets
```
Union(x, y)
	Link(Find-Set(x), Find-Set(y))
```
Find the roots and connect them

**Link(x,y)** -> Two root: one under the other
```
Link(x, y) 
1 if x.rank > y.rank 
2 	y.p = x 
3 else x.p = y 
4 	if x.rank == y.rank 
5		y.rank = y.rank + 1
```
## Optimalization
### Union by rank
**Rank**: Is an upper bound for the nodeheight

![[Pasted image 20211019103438.png]]

#### Example
![[Pasted image 20211019104011.png]]
*Notice that the rank of the roots is the same, hence add 1 to one of them*

### Path-compression
- Set the parent of each node to the root by using FIND-SET(v)
#### Example
![[Pasted image 20211019104319.png]]

==Observere==: We are not updating the ranks, hence **Rank** is an upper bound for the nodeheight :)

## Running time
With m operations we have:
$O(m*\alpha(n))$

Where $\alpha(n)$ is insanely slowly increasing, hence it is often neglected

## References