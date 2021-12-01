#todo 

# Radix sort
*Sorts on leas significant numbers*
--> Sort these with [[Counting sort]]
--> Keep going --> Will be sorted in the end

>NB!
>Require the digits to be stable sorted --> Use [[Counting sort]]

## Pseudocode
![[Pasted image 20211115093507.png]]

## Running time
> Given n d-digit numbers --> can take up to k possible values
> ==Uses $\Theta (d(n+k))$ if stable sort uses $\Theta(n+k)$ time$==

> Given n b-bit numbers and any positive integer $r \le b$
> ==Sort in $\Theta (\frac{b}{r} (n+2^r))$ if stable sort $\Theta(n+k)$ for values $0 \rightarrow k$==

>**This implies**
>Larger b (base) --> More space for counting sort
>Smaller b (base) --> Less time for radix sort as d decreases

## Example
![[Pasted image 20211115093532.png]]

## References