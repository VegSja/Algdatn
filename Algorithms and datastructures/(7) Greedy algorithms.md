#TOC  

# Greedy algorithms
*A greedy algorithm always makes the choice that looks best at the moment*

Do not need to yield optimal solutions 

Beneath every greedy algorithm, there is always a more cumbersome [[(6) Dynamic Programming]] solution

Greedy algorithms typically has a [[Activity-selection problem#^baaf9d|top down]] design



## Example problems
 [[Activity-selection problem]]
 We can solve [[The fractional knapsack problem]] greedily
 
## Examples algorithms
 [[Huffmann codes]]
 
## Elements of the greedy strategy
We design greedy algorithms according to the following sequences of steps:
1. Cast the optimization problem as one in which we make a choice and are left with one subproblem to solve
2. Prove that there is always an optimal solution to the original problem that makes the greddy choice, so that the greedy choice is always safe
3. Demonstrate optimal substructure by showing that, having made the greedy choice what remians is a subproblem with the property that if we combine an optimal solution to the subproblem with the greedy choice we have made we arrive at an optimal solution to the original problem

## Proving a greedy algorithm works
### Greedy-choice property
*We can assemble a globally optimal solution by making locally optimal(greedy) choices*

**Prove that a greedy choice will yield in a globally optimal solution**

### Optimal substructure
- We use a more direct approach than[[(6) Dynamic Programming#Optimal substructure|Optimal substructure in dynamic programming]]
	- By assuming we arrived at a subproblem after a greedy choice
- Proof by induction


### Difference from [[(6) Dynamic Programming]]
- Instead of solutions depending on solutions to subproblems, we make the choice which seems best at the moment
See example on P.446 in Introduction to algorithms


