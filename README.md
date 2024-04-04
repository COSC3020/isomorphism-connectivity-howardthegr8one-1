[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/QM7QGF1q)
# Isomorphism

Prove that if two graphs $A$ and $B$ are isomorphic they do *not* have to
be completely connected. I have started with the formal definition of
isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.

# My Proof
Using proof by contradiction let's assume that if two graphs $A$ and $B$ are isomorphic then they HAVE to be completely connected. Then if graph $A$ has the following shape represented by an adjacency list:

```javascript 
A = [
    [1, 2],
    [],
    []
]
```
and graph B represented as:
```javascript
B = [
    [],
    [0, 2],
    []
]
```
Neither of these graphs are completely connected, yet we can successfully map every node from $A$ to every node in $B$:

0 in A maps to 1 in B \
1 in A maps to 0 in B \
2 in A maps to 2 in B

this mapping of nodes still preserves the edges of the original graphs (a single node connected to the other two nodes by one edge each), thus by contradiction two graphs that are NOT completely connected CAN be isomorphic. 
