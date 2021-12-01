#todo 

# Priority queues
*Data structure for maintaing a set S of elements. Each with an associated value called a **key** *

## Operations

| Operation           | What it does                                              | Time complexity |
| ------------------- | --------------------------------------------------------- | --------------- |
| INSERT(S,X)         | Insert x to set S                                         | $O(lgn)$        |
| MAXIMUM(S)          | Returns the element of S with the largest key             | $\Theta(1)$     |
| EXTRACT-MAX         | Removes and returns the element of S with the largest key | $O(lgn)$        |
| INCREASE-KEY(S,x,h) | Increase x's key value to the new value k                 | $O(lgn)$                |

![[Pasted image 20211201115532.png]]

## Implementing using [[Heap]]
- Need *handle* to corresponding object in each heap element
	- Pointer/Integer
	- Also need to go from heap element to corresoinding object
		- Usually array index


## References