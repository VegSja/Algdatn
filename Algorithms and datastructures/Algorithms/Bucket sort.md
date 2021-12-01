#todo 

# Bucket sort
Assumes:  *Elements are uniformly and independently distributed over interval $[0,1)$*

## Time complexity
Average case: ==$\Theta (n)$==

**If not uniform distrobution:** As long as sum of squares of bucket sizes is linear in the total nb of elements --> $\Theta (n)$

**Worst case**: $O(n^2)$

## How it works
1. Divide $[0,1)$ in n equal sized subintervals
2. Distribute numbers in buckets based on most significant digit
3. Sort buckets and place in array

### Pseudo code
![[Pasted image 20211115094634.png]]

### Example
![[Pasted image 20211115094657.png]]


## References