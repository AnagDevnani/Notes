# Introduction
$$
\text{Polynomial} \implies \underbrace{\text{Poly}}_{\text{Greek for "Many"}} + \underbrace{\text{Nomen}}_{\text{Latin for "Name"}}
$$

- It is the sum of multiple mathematical terms
	- Each term is called a **monomial**
- Only Addition, Subtraction & Multiplication Arithmetic Operators are allowed
	- Division is **NOT** allowed
- Each Variable must have its exponents as Whole Numbers

$$
\sum_{m=0}^{n}a_mx^m = a_nx^n +a_{n-1}x^{n-1}\dots a_1x+a_0
$$

## Degree of Polynomial
- It is the degree of the highest degree term in the polynomial
- The Degree of the term is the sum of the degrees of all the variables present in that term **e.g.**$4x^3y^2$ has a degree of $5$
- The Degree of Zero Polynomial $(0.x^n +\dots+0.x+0)$ is undefined

**Multiplicity:** It refers to how many times a factor is multiplied when representing polynomials in Factor form**e.g.** $m$ in $(x-a)^m$
**Note:** The Sum of all Multiplicities is equal to the degree of the polynomial

# Multiplication of Polynomials

# Graphs of Polynomials
## Behaviour at $x$-intercepts
If the graph touches the x-axis and:-
- Bounces off (Does not cross) $\implies$ Zero with **Even** Multiplicity
- Crosses $x$-axis $\implies$ Zero with **Odd** Multiplicity
	- After Crossing if it appears almost linear $\implies$ it is a single zero

**Note:** For Higher Powers, the graph will be more flatter near the $x$-axis

## Behaviour at Ends of the Graph
- By End we refer to the left most and right most values of the graph (**i.e.** $x\rightarrow\infty$ and $x\rightarrow-\infty$)
- The ends are influenced solely by the term which contains the highest degree variable.
	- As this value dominates all the other values present in the polynomial
- Therefore, its ends depend on 2 factors of the highest degree term:
	- Sign of Coeffecient of $x^n$ (+ve or -ve)
	- Type of power of $x_n$ $(n \in\text{Even}$ or $x\in\text{Odd})$

## Behaviour at Turning Points
- Turning Points are where the function changes its characteristic e.g. Increasing, Decreasing
- Basically Turning Points are all those points where $f'(x)=0)$
- We know a polynomial of degree $n$ can have at most $n$ zeroes, therefore. each time the graph crosses a zero it must turn to reach the other zeroes.
	- The max no. of turning points are $n-1$
- As Multiplicity increases, the no. of turning points decreases

## Creating Graph of Polynomials
1. Find x-intercepts and y-intercepts if possible.
2. Check for symmetry about Origin or $y$-axis
	- $f(-x)=f(x) \implies\text{Even} \implies\text{Symmetric about }x\text{-axis}$
	- $f(-x)=-f(x) \implies\text{Odd} \implies\text{Symmetric about Origin}$
3. Mark the zeroes on the x-axis
4. Find the end behaviour of the graph
5. Find Behaviour at x-interecepts using multiplicities
6. Join the zeroes(x-intercepts) by finding turning points

## Obtaining Function from Graph
1. Check x-intercepts and note the zeroes of the polynomial
2. Check behaviour at x-intercepts to find multiplicity
3. Using any point (such as y-intercept), find the stretch factor, $a$
# Factorisation of Cubic Polynomial
1. Arrange the polynomial in the form of $f(x) =\text{a}x^3 + \text{b}x^2 + \text{c}x + \text{d}$
2. Find all the factors of $\text{d}$ and substitue in $f(x)$.
3. Divide the polynomial by $(x-t)$ where $t$ is the factor of $\text{d}$ for which $f(x) = 0$