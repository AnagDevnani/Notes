- Equation involving dependant variable $(y)$, independant variable $(x)$ and the derivatve of dependant variable w.r.t independant variable $\big(\frac{dy}{dx}\big)$

## Order
- **Order:** Highest order of derivative present in the equation
- **Degree:** Power associated with the highest power derivative.
- In order tofind order / degree, D.E. must be written as a polynomial in its derivatives. (Radical Free)

# Exact Differential Equations
$$
M(x,y)dx+N(x,y)dy=0
$$

## $\frac{\partial M}{\partial y}=\frac{\partial N}{\partial x}$ form:
If True:
$$
\int M(x,y)dx+\int \underbrace{N(y)dy}_{\text{Integrate }y\text{ only, ignore }x\text{ terms}}=C
$$

## Reducible to $\frac{\partial M}{\partial y}=\frac{\partial N}{\partial x}$ form:
Generally we have 2 scenarios:
1. If $\frac{\partial M}{\partial y}-\frac{\partial N}{\partial x}\approx N$
then, I.F. = $e^{\int f(x)dx}$ where, f(x) = $\frac{\frac{\partial M}{\partial y}-\frac{\partial N}{\partial x}}{N}$
2. If $\frac{\partial M}{\partial y}-\frac{\partial N}{\partial x}\approx M$
then, I.F. = $e^{-\int f(x)dx}$ where, f(x) = $\frac{\frac{\partial M}{\partial y}-\frac{\partial N}{\partial x}}{M}$

After either 1. or 2. :
Multiply I.F. to D.E and solve as $\frac{\partial M}{\partial y}=\frac{\partial N}{\partial x}$ form if appropriate, otherwise repeat.

# Growth & Decay Problems
- In general, all cases of growth and decay are First Order Equations in the form of:
$$
\frac{d[A]}{dt} = k.u
$$

# Orthogonal Trajectories
- If 2 family of curves such that every number of one family intersects orthogonaly with every family from the other.

### Cartesian Method
$$
\text{given, } f(x,y)=C
$$
1. Differentiate w.r.t. $x$ to form D.E.
2. Replace $\frac{dy}{dx}$ with $-\frac{dx}{dy}$  
3. Intergrate & the bew function obtained is the orthogonal trajectories.

### Polar Method
$$
\text{given, } f({r,\theta})=c
$$
1. We pewfer to take $\log$ & differentiate w.r.t. $\theta$ to get $\frac{dr}{d\theta}$
2. Replace $\frac{dr}{d\theta}$ by $-r^2\frac{d\theta}{dr}$ & solve.
3, Integrate and new function formed is the trajectory of prior function.

## Self-Orthogonal
- Basically, after integrating function remains the same.
- Therefore, differential equation after replacing $\frac{dx}{dy}$ or $\frac{dr}{d\theta}$ must be the same.
- 