#todo 

# Huffmann codes
*A greedy algorithm which uses a table giving how often each character occurs to build up an optimal way of representing each character as a binary string*

**Fixed length code**: I.E use 3-bits to represent every char

**Variable-length code**: Give frequent chars short codewords and infrequent ones longer codewords
	- Much better than **fixed-length code**
	
## Prefix codes
*Codes in which no codeword is also a prefix for some other codeword*
- Suffer no cost in generality
- Simplify decoding
	- Uses a [[Binary tree]] for representation
		- Leaves are the given characters
		- 0 means go to the left, 1 means go to the right
---
==Number of bits to encode a file==
$c.freq$ - Frequency of char c
$d_T(c)$  - Depth of c's leaf in the tree

>**Number of bits required:**
>$B(T)= \sum_{c\in C}c.freq*d_T(c)$

## Constructing Huffman codes
![[Pasted image 20211004113240.png]]
- Relies on [[(7) Greedy algorithms#Greedy-choice property]] and [[(7) Greedy algorithms#Optimal substructure]]
- Builds in a bottom up manner

![[Pasted image 20211004113356.png]]

**Running time: $O(nlgn)$** can be reduced to O(nlglgn) by using Emde Boas tree

## Proof of correctness
See P. 454

## References