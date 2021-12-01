#todo 

# Activity-selection problem
*We wish to select a maximum-size subset of mutually compatible activities*

We assume that activities are sorterd in increasing order of finish time

## Making a greedy choice
[[(7) Greedy algorithms]]

1. Choose the activity with the earliest finish time
	1. NB! This is not the only greedy choice you can make
2. Continue this trend

The following theorem tells us that this greedy chocie is always part of some optimal solution:

> **Theorem**
> Consider any nonempty subproblem $S_k$, and let $a_m$ be an activity in $S_k$ with the earliest finish time. Then $a_m$ is included in some maximum-size subset of mutually compatible activities of $S_k$

- This algorithm is working **top-down**: Choosing an activity to put in the optimal solution and then solve the subproblem of choosing which are compatible with this choice ^baaf9d
	- By doing this we reduce the problem size for each choice we make

### A recursive greedy algorithm
![[Pasted image 20211004095319.png]]

**Running time: **==$\Theta(n)$==
Because each element is only examined once

### An iterative greedy algorithm
![[Pasted image 20211004095500.png]]
**Running time: **==$\Theta(n)$==
## References