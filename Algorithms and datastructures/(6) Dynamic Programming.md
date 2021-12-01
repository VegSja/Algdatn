#TOC  

# Dynamic Programming
*A generalization of [[(3) Divide and conquer]] where subproblems can overlap, hence it is possible to reduce time complexity*

## 4 steps
1. Characterize the structure of the optimal solution
2. Recursively define the value of an optimal solution
3. Compute the value of an optimal solution (typically bottom-up)
4. Construct an optimal solution from the comptued information
## Optimal substructure
*Optimal solutions to a problem incorporate optimal solutions to related subproblems; which we may solve independently*

## Problems
- [ ] [[Rod cutting problem]]
- [ ] [[Longest common subsequence]]

---
## When to use
### Optimal substructure
*Optimal solutions to a problem incorporate optimal solutions to related subproblems; which we may solve independently*

> **Pattern for finding**
> 1. Show that a solution to the probelm consists of making a choice
> 2. Suppose that for a given problem, you are given the choice that leads to an optimal solution
> 3. Given choice --> Determine subproblems that ensure and how to best characterize the resulting space of subproblems
> p. 379

#### Varies in two ways
1. How many subproblems an solutions to the original problem uses
2. How many choices we have in determining which subproblems to use in an optimal solution

Often used in a bottom-up fashion

### Overlapping subproblems
*We have to solve the same subproblem several times*
- Space of subproblems small --> We have to solve the same subproblem several times
- Would be nice to store the previous results

### Subtleties
- Be careful not to assume that optimal substructure applies when it does not
----

**Independent solutions** --> The solution to one subproblem does not affect the solution to another subproblem of the same problem

----

## Subproblem graph
*Embodies information about the set of subproblems involved and how subproblems depend on each other*
![[Pasted image 20211201120556.png]]

- Directed edge from vertex for subproblem x to the vertex of subproblem y
	- If determining an optimal solution for subproblem x involves directly considering an optimal solution for subproblem y
- Bottom up
	- Is going to be in reverse [[Topological sort]]
- Memoization
	- Looks like a [[Depth-first search]] of the subproblem graph

- Using its size to determine running time of algorithm
	- Sum of times needed to solve each subproblem
	- Time to compute subproblem: *proportional to the degree of the corresponding vertex in the subproblem graph*
	- **The running time of dynamic programming is linear in the number of vertices and edges**

## Reconstructiong an optimal solution
- Often store which choice we made
	- Can reconstruct in O(1) time

## Memoization
- Top down
- Store subproblem solutions

## Bottom up
*Typically depends on some natural notion of the "size" of a subproblem, such that solving any particual subproblem depends only on solving "smaller subproblems"*

- Sort the subproblems by size
- Solve in size order, smallest first
- When solving a problem we have already solved all of the smaller subproblems its solution depends upon
- Solve each subproblem exactly once


## References