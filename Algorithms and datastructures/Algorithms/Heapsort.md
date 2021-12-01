#todo 

# Heapsort
*Uses [[Heap]] to sort an array **inplace***

## Advantages
- Efficient
- Minimal memory usage
- Simplicity

## Time complexity
==$O(nlgn)$==

## How it works
1. Call BUILD-MAX-HEAP
2. Root is largest. So we exchange root with last item in the heap, and reduce size of heap by 1. exchange: $A[1] \leftrightarrow A[n]$
	1.  Discard $A[n]$ by decrementing
3.  Call MAX-HEAPIFY on remaining tree
	1.  Repeated down to heapsize 2

## Pseudocode
![[Pasted image 20211115100256.png]]

## References