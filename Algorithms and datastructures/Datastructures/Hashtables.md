#todo 

# Hashtables
*Uses a hashing function h(k) which maps the universe to the slots of a table*
- Resets storage requirement to $\Theta(|k|)$

## Operations
SEARCH/INSERT/DELETE all have an average runtime of **O(1)**

## Direct-address table
- Slot corresponds to a key in the universe U
	- Points to element with key

### Downsides
If the universe is large it is impossible to store Table T

## Collisions
- Store the elements mapped to the same key in a linked list (double linked preferred)

| Operation | Complexity |
| --------- | ---------- |
| INSERT    | O(1)       |
| DELETE    | O(1)       |
| SEARCH    | O(n)           |

## Good hashing functions
- Simple uniform hashing
- Simple variants doesn't hash to the same value
- Hash-value independent from data
## References