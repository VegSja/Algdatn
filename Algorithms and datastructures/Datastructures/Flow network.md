#todo 

# Flow network
*A directed graph where each edge has a nonnegative capacity. There is no reverse edge, we disallow self-loops*

**Source and sink**


## Flow
A real valued function which satisfies two properties:
1. **Capacity constraint:** For all $u,v \in V$, we require $0 \le f(u,v) \le c(u,v)$
2. **Flow conservation:** For all $u \in V - {s,t}$ we require

$\sum_{v \in V}f(v,u)=\sum_{v \in V} f(u,v)$


## Value
$|f| = \sum_{v \in V}f(s,v)=\sum_{v \in V} f(v,s)$

## Networks with multiple sources and sink
Add a super source and super sink with a capacity $\infty$ and use default algorithms

## References