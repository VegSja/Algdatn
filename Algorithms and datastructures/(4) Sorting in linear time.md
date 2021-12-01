#TOC  

# (4) Sorting in linear time
*The art of strenthening the requirements for input or lowering the requirements for outpur to make sorting algorithms faster*

## Lower bounds for sorting
*This tells us that best case scenario for comparison based algortihms are $\Omega (nlgn)$*

### Decision tree
![[Pasted image 20211115091202.png]]
- Since the execution time of the sorting is given with a simple path from the root to leaf
--> Worst case for comparison sort is $\Omega (nlgn)$

## Algorithms
[[Counting sort]]
[[Radix sort]]
[[Bucket sort]]

## Medians and order statitics
*Assume that elements are distinct*

## Randomized select
**Expected runtime:** $\Theta(n)$ - Assuming distinct elements
**Worst case:** $\Theta(n^2)$ - Because we could pick the highest number as a pivot each time

## References