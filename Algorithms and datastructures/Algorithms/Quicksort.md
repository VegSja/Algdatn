#todo 

# Quicksort
***Idea:** An element is sorted if every number on the right is larger and every element on the right is smaller*
Uses [[(3) Divide and conquer]] to sort a list in place



## Time complexity
| Case                   | When                                                                                                               | Complexity     |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------ | -------------- |
| Worst                  | - One subarray with n-1 elements and one with 0 elements (*Does not partition evenly*) <br> - When input is sorted | $\Theta(n²)$   |
| Best case partitioning | - Two subproblems not bigger than n/2(*Even partition*)                                                            | $\Theta(nlgn)$ |
| Average case           | - Unlikely to partition the same way each iteration. Hence good average. Produces a mix of good and bad            | $\Theta(nlgn)$ |

## How it works
1. **Divide**: Partition to two subarrays. Elements in first array is smaller than pivot. Elements in second is larger
2. **Conquer**: Sort the two subarrays recursively
3. **Combine**: No need to combine


### General inner workings
1. Choose a pivot element (are we using random or just picking the last?)
	1. Place pivot element on the right
2. Iterate through the array with 2 pointers (**i**: *Last index of the smaller than or equal partition*, **j:** *The index that "moves" and checks each elements values with the pivot. Is also last index of larger than pivot*)
	1. Add elements smaller than pivot in partition $[p,i]$
	2. Add elements larger than pivot in partition $[i,j]$
		1. Does so by incrementing j
	3. Swapping
		1. *When encountering an element less than or equal the pivot, swap its position with the leftmost element in the **larger than pivot** array*
			1. Expands the **less than pivot** array
3. Place the pointer in between the two arrays. The pointer is now in its **correct position**
	1. Does so by swapping the pivots position with the left most in the larger than partition
4. Repeat the process for one of the partition. This is what gives the algorithm its [[(3) Divide and conquer]] nature

### Pseudocode
![[Pasted image 20211115101401.png]]
![[Pasted image 20211115101410.png]]

### Partition
- **Always: ** Select last element as pivot element
	- Want to find sorted position of  the pivot by grouping elements into smaller and larger than pivot

![[Pasted image 20211115101425.png]]

### Random partitioning
*Can now expect the split to be reasonable well balanced on average.*
1. Choose an random element in the array
2. Exchange random element with last element in array



## References
> **NB:** These references demonstrates in a different manner than what is described in the book
- https://www.youtube.com/watch?v=7h1s2SojIRw
- https://www.youtube.com/watch?v=Hoixgm4-P4M