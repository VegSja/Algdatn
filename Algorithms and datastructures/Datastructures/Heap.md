#todo 

# Heap
*Nearly a [[Binary tree]], only difference is that heaps count indecies from left to right*
![[Pasted image 20211003143207.png]]

Could either have property (min/max)

>## Heap properties
>### Max heap
>$A[Parent(i)] \le A[i]$
>### Min heap
>$A[Parent(i)] \ge A[i]$

### Height
*Number of edges on the simple downward path from the node to a leaf*
**$\Theta(lg(n))$**

## Maintaing heap property
MAX-HEAPIFY: *A[i] might be smaller than its children*
![[Pasted image 20211003143655.png]]
![[Pasted image 20211003143704.png]]

> **Running time:**
> $O(lg(n))$

## Building a heap
**BUILD-MAX-HEAP**: *Goes through the remaining nodes in tree and runs MAX-HEAPIFY on each one*

> **Running time:**
> $O(n)$

## 

## References