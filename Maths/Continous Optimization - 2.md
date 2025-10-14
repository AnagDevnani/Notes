Optimization -> Hessian Matrix

Unconstrained Optimization

```mermaid
flowchart TD;
O[Optimization]-->C[Constrained<br>f: objective fn]
O-->U[Unconstrained]
C-->E[Equality]
C-->I[Inequality]
E-->Substitution
E-->L[Lagrange Multipliers]
I-->[KKT Conditions]
```

## Method of Lagrange multipliers for optimization
Objective function: $f(x)$

Constraints: $g_1(X)=0,\ g_2(X)=0\dots$

The gradient of the contour functions are orthogonal => gradients of $f$ and $g_i$ are parallel.

$$
\nabla f = \sum\lambda_i\nabla g_i
$$
    Move only the file file_1 present in dir_1 to the empty directory dir_2.
    Delete the directory dir_1.


<u>Algorithm</u>
<br>

i) Construct $F=f - (\lambda_1g_1+\lambda_2g_2+\dots+\lambda_ng_n)$<br>
ii)$\nabla F=0$ i.e. $\nabla f -\sum \lambda_i g_i=0$<br>
iii) Solve $\nabla F = 0$ subject to $g_1=0,\ g_2=0\dots$<br>
iv) Substitute $f$ to obtain to obtain the optimized values.

# Constrained Optimizations (Inequality Contraints)
Objective function: $f$

Constraints: $g_1(X)\leq b_1,\ g_2(X)\leq b_2\dots$ or $g_i\leq b_u$

## KKT Conditions (Karush - Kuhn - Tucker)
Necessary Condition:

$\nabla f-\lambda_i g_i=0\quad\rightarrow\quad\text{Optimality Condition.}$

$g_(X)-b_i\leq0\quad\rightarrow\quad\text{Feasibility.}$

$\sum\lambda_i(g_i(X)-b_i)=0\quad\rightarrow\quad\text{Complementary Slackness}$