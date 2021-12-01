#todo 

# Merge sort
*A [[(3) Divide and conquer]] algorithm*

**Divide**: Divide the n-element sequence to be sorted into two subsequences of n/2 elements each.

**Conquer**: Sort the two subsequences recursively using merge sort

**Combine**: Merge the two sorted subsequences to produce the shortest answer

![[Pasted image 20211116165151.png]]
![[Pasted image 20211201103411.png]]
![[Pasted image 20211201103344.png]]
> **Important to note**
> The merging happens as we combine the single elements into larger arrays
> We insert the numbers in correct order

## Complexity

**MERGE:** *Takes $\Theta (n)$ time*

| Case    | Complexity |
| ------- | ---------- |
| Best    | O(nlgn)    |
| Average | O(nlgn)    |
| Worst   | O(nlgn)           |


## References