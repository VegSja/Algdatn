#todo 

# Counting sort
Assumes: *The input consists of integers in a small range*

- Output is **Stable**

## Running time
Actual: $\Theta (k+n)$
In practice: $\Theta (n)$ since we use counting sort when $k=O(n)$

## Psuedo code
![[Pasted image 20211115093158.png]]

## How it works
- For each element x determine the number of elements less than x
	- Uses this information to put x directly into its position in the output array

- Uses 3 arrays:
1. A[1,....,n] --> Input
2. B[1,....,n] --> Sorted
3. C[0,....,k] --> Computation

### Example
$A: [1,0,3,1,3,1]$
**Computations:**
C:
1. Counts (Line 4-6):

| 0   | 1   | 2   | 3   |
| --- | --- | --- | --- |
| 1   | 3   | 0   | 2   |

2. Adds left to right (*To see how many elements are less than or equal*) (line 7-9):

| 0   | 1   | 2   | 3   |
| --- | --- | --- | --- |
| 1   | 4   | 4   | 6   |
*Notice that it does this iteratively*

3. Start placing the elements into B array by going through A in reverse order. After placing a element, decrease the index of said element in C

Pulling another example from the book:

![[Pasted image 20211201111223.png]]
*Notice that for (c)-(e) the index in c has already been decreased*

**Results:**
$\underline{\underline{B:[0,1,1,1,3,3]}}$


## Why is counting sort stable
*Maintains this property by going through the A array in reverse order on line 10-12*

For instance the array of stock prices:
`[(CSCO 1), (MSFT 1), (GOOG 3)]`

When sorting:
```
sorted array: [null, null, null]
counts array: [0, 2, 2, 3]    

iterate stocks in unsorted stocks from backwards
1. the last stock (MSFT 1)
sorted array: [null, (MSFT 1), null] (copy to the second position because counts[1] == 2)
counts array: [0, 1, 2, 3] (decrease counts[1] by 1)

2. the middle stock (CSCO 1)
sorted array: [(CSCO 1), (MSFT 1), null] (copy to the first position because counts[1] == 1 now)
counts array: [0, 0, 2, 3] (decrease counts[1] by 1)

3. the first stock (GOOG 3)
sorted array: [(CSCO 1), (MSFT 1), (GOOG 3)] (copy to the third position because counts[3] == 3)
counts array: [0, 0, 2, 2] (decrease counts[3] by 1)
```

*And since we decrease the count of an element in C every time we output an element, we are essentially making the elements with same key's next appearance final position smaller.*

## References