#todo 

# Binary search tree
[[Binary tree]]
>## Properties:
>Let x,y be nodes
>y is left subtree of x: $y.key \le x.key$
>y is right subtree of x: $y.key \ge x.key$

## Querying a binary search tree
>### Runtime
>Everything descirbed here takes **O(h)** where h is hegiht of the tree

### Search
![[Pasted image 20211003145009.png]]
![[Pasted image 20211003145018.png]]

### Minimum and maximum
Following left/right child pointers til we encounter NIL
![[Pasted image 20211003145121.png]]
![[Pasted image 20211003145131.png]]

### Successor and predeccessor
*Determined by an inorder tree walk*

| Situation                                   | Successor                                         | Predeccessor |
| ------------------------------------------- | ------------------------------------------------- | ------------ |
| Distinct keys                               | The node with the smallest key greater than x.key |              |
| Right tree nonempty                         | The leftmost node in x's right subtree            |              |
| Right subtree empty and x has an ancestor x | y is the lowest ancestor of x whose left child is also an ancestor of x                                      |              |

![[Pasted image 20211003145333.png]]

---
## Insertion and deletion
### Insert
![[Pasted image 20211201115031.png]]
![[Pasted image 20211201115009.png]]
### Delete
![[Pasted image 20211003145508.png]]
![[Pasted image 20211003145525.png]]
![[Pasted image 20211003145534.png]]

## References