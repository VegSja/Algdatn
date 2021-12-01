#todo 
# Recurrences
- T(n) is running time of a problem of size n
- Each problem yields a subproblem
	- Of size $\frac{1}{b}$ of the original
- Takes $T(\frac{n}{b})$ to solve the subproblem


$$
T(n) =
\left\{
	\begin{array}{ll}
		\Theta(1) \\
		aT(n/b)+D(n)+C(n)
	\end{array}
\right.
$$

Where:

$T(n/b)$ = Time to solve subproblem
$D(n)$ = Time to divide
$C(n)$ = time to combine

## The substitution method
1. Guess the form of the solution
2. Use mathematical induction and show that the solution works

## The recursion-tree method
- Make good guesses
- Each node represents the cost of a single subproblem

![[Pasted image 20211201081807.png]]

**How long till we reach a boundary condition in the tree?**
*See page 111 in the book*

### Height of tree
![[Pasted image 20211201084809.png]]
$T(n/\pi)$ is slowest decreasing. Looking at this to calculate:

The grunntillfelle in hit when n=1 which will happen when:
$\frac{n}{\pi^k} = 1$
$k = lg_\pi n = \Theta(lg n)$

## The master theorem
*A cookbook for solving recurences on the form $T(n) = aT(n/b)+f(n)\ \ \ \ \ \ a \ge 1 \ \ \  b \gt 1$ *

> Let $a \ge 1$ and $b \gt 1$ be constants, let f(n) be a function, and let T(n) be defined on the nonnegative integers by the recurrences
> $T(n) = aT(n/b)+f(n)\ \ \ \ \ \ a \ge 1 \ \ \  b \gt 1$ ==Only works on this form== 
>where $n/b \Rightarrow floor(n/b)$ or $ceil(n/b)$. Then T(n) has the following asymptotic bounds:

| Form                                                                                                                                                             | Asymptotic bounds                 |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| f(n)=$O(n^{log_b a - \epsilon})$ for some constant $\epsilon \gt 0$                                                                                              | $T(n)=\Theta (n^{log_b a})$       |
| $f(n) = \Theta(n^{log_b a})$                                                                                                                                     | $T(n) = \Theta (n^{log_b a} lgn)$ |
| $f(n) = \Omega(n^{log_b a + \epsilon})$ for some constant $\epsilon \gt 0$, and if $f(n/b) \le cf(n)$ for some constant $c \lt 1$ and all sufficienctly large n | $T(n)=\Theta (f(n))$                                  |


## The iteration method
*Same principles as the recursion tree method, but we work more directly on the specific equations*

- Use the recurrence to expand the recursive terms. 
- Continue till we see a pattern emerging
- Desire to reach the starting condition ($T(0)=0$)
![[Pasted image 20211201103727.png]]

Enda et eksempel for [[Binary search]]
![[Pasted image 20211201103927.png]]

## References