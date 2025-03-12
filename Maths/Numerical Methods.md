# Introduction
There are 2 primary methods of solving:
- Analytical (Exact)
- Numerical (Approximate)

We require Numerical methods as they allow us to solve problems which would otherwise be unsolvable by Analytical methods and they have programming applications.
# Intermediate Value Theorem
If $f$ is a function which is constant at every point in $[a,b]$ and $f(a)\times f(b) \leq0$.
Then $f(x)=0$ for some $x$ in $[a,b]$
# Newton-Rapson Method
Let $m$ be a real root of the equation $f(x)=0$, then $f(m)$=0.
If $m$ lies near a point, $a$, by Taylor's series:
$$
f(m)=f(a)+(x-a)f'(a)+\frac{(x-a)^2f''(a)}{2!}+\dots
$$
Neglecting higher order derivatives we get:
$$f(m)=f(a)+(x-a)f'(a)$$
As $f(m)=0$:
$$x=a-\frac{f(a)}{f'(a)}$$
let $a=x_o$ and $x=x_1$:
$$x_1=x_o-\frac{f(x_o)}{f'(x_o)}$$
Therefore we have:
$$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}$$
# Finite Difference
$\text{let }y=f(x) \text{ and } y_o, y_1, y_2\dots\text{ be values corresponding to } x_o, x_1, x_2\dots \text{respectively}$
|$x$|$x_o$|$x_1$|$x_2$|$\dots$|
|:---:|:---:|:---:|:---:|:---:|
|$y$|$y_o$|$y_1$|$y_2$|$\dots$|

Then we have the **first forward difference** as:
$$
\Delta y_1=y_1-y_o\\
\Delta y_2=y_2-y_1\\
\vdots\\
\Delta y_{n+1}=y_{n+1}-y_n
$$
Similiarly, we have **second forward difference** as:
$$
\Delta^2y_2=\Delta y_2-\Delta y_1\\
\Delta^2y_3=\Delta y_3-\Delta y_2\\
\vdots\\
\Delta^2 y_{n+1}=\Delta y_{n+1}-\Delta y_n
$$

In general we have:
$$
\Delta^k y_{n+1}=\Delta^{k-1} y_{n+1}-\Delta^{k-1} y_n
$$

**Note:**
- If $f(x)$ is constant, then $\Delta^k y_{n+1}=0$
- $\Delta^n$ is called the $n^\text{th}$ forward difference operator
- Forward difference table can be given by the following example:

|$x$|$y$|$\Delta y$|$\Delta^2 y$|$\Delta^3 y$|
|:---:|:---:|:---:|:---:|:---:|
|$x_o$|$y_o$|$\Delta y_1=y_1-y_o$|$\Delta^2y_2=\Delta y_2-\Delta y_1$|$\Delta^3 y_3=\Delta^2 y_3-\Delta^2 y_2$|
|$x_1$|$y_1$|$\Delta y_2=y_2-y_1$|$\Delta^2 y_3=\Delta y_3-\Delta y_2$||
|$x_2$|$y_2$|$\Delta y_3=y_3-y_2$|||
|$x_3$|$y_3$|

Similiar to Forward Diffrence, we have **Backward Difference** as:
$$
\nabla y_n=y_n-y_{n-1}\\
\vdots\\
\nabla^k y_n=\nabla^{k-1}y_n-\nabla^{k-1}y_{n-1}
$$
# Newton-Gregory Interpolation form
**Note:** Only works for Finite Difference

Suppose we wish to estimate value of $y$ corresponding to a desired value of $x$ that lie between $x_o$ and $x_n$. This process of estimating inside a given interval is called interpolation.

The process of estimating value of $y$ for some value of $x$, outside the interval $[x_o,\ x_n]$ is called extrapolation.

Suppose the values $x_o, x_1,\dots,x_n$ of $x$ are equally spaced with $h$ as step-length between consecutive values as:
$$
h=x_1-x_o=x_2-x_1=\dots=x_n-x_{n-1}
$$
Then we have:
$$
x_1=x_o+h\\
x_2=x_1+h=x_o+2h\\
x_r=x_o+rh
$$
where $r= 1,2,3\dots n$

Suppose we wish to estimate the value of $y$ correspoding to desired value $x_p$ of $x$ that lies between $x_o$ and $x_n$, Then:
$$
x_p=x_o+ph
$$
Newton-Gregory forward interpolation formula:
$$
y_p=y_o+p(\Delta y_o) +\frac{p(p-1)\Delta^2 y_o}{2!}+\frac{p(p-1)(p-2)\Delta^3 y_o}{3!}+\dots\frac{p(p-1)(p-2)\dots(p-(n-1))\Delta^n y_o}{n!}
$$

Newton-Gregory backward interpolation formula:
$$
y_p=y_n+p(\nabla y_n) +\frac{p(p+1)\nabla^2 y_n}{2!}+\frac{p(p+1)(p+2)\nabla^3 y_n}{3!}+\dots\frac{p(p+1)(p+2)\dots(p+(n-1))\nabla^n y_n}{n!}
$$

# Lagrange's Interpolation Formula
**Note:** Applicable when step-length is unequal

If $y=f(x)$ takes the values $y_o,y_1,\dots,y_n$ corresponding to $x_o,x_1,\dots,x_n$, then we have:
$$
y=\frac{(x-x_1)(x-x_2)\dots(x-x_n)}{(x_o-x_1)(x_o-x_2)\dots(x_o-x_n)}y_o + \frac{(x-x_o)(x-x_2)\dots(x-x_n)}{(x_1-x_o)(x_1-x_2)\dots(x_1-x_n)}y_1 + \dots\frac{(x-x_o)(x-x_1)\dots(x-x_{n-1})}{(x_n-x_o)(x_n-x_1)\dots(x_n-x_{n-1})}y_n
$$

**Note:** Lagrange’s formula is a relation between two variables either of which may be taken as the independent variable. Therefore, interchanging $x$ and $y$ has no effect.

# Integration by numerical methods
## Simpson's 1/3^rd^ Rule
Only Applicable when $n$ is a multiple of 2
$$
\int\limits_{x_o}^{x_n}f(x)dx=\frac h3\bigg[(y_o+y_n)+2(y_2+y_4+y_6+\dots y_{n-2})+4(y_1+y_3+y_5+\dots y_{n-1})\bigg]
$$
## Simpson's 3/8^th^ Rule
Only Applicable when $n$ is a multiple of 3
$$
\int\limits_{x_o}^{x_n}f(x)dx=\frac {3h}{8}\bigg[(y_o+y_n)+2(y_3+y_6+y_9+\dots y_{n-3})+3(y_1+y_2+y_4+\dots y_{n-1})\bigg]
$$
## Weddle's Rule
Only Applicable when $n$ is a multiple of 6
$$
\int\limits_{x_o}^{x_n}f(x)dx=\frac {3h}{10}\bigg[(y_o+y_n)+2(y_6+y_{12}+y_{18}+\dots y_{n-6})+(y_2+y_4+y_8+\dots y_{n-2})+6(y_3+y_9+y_{15}+\dots y_{n-3})+5(y_1+y_5+y_7+\dots+y_{n-1})\bigg]
$$

**Note:** Volume of solid = $\int y^2dx$ and for solid of revolution = $\pi \int y^2dx$
# Solution of ODEs
An ODE of 1st order is of the form:
$$
F(x,y,y') = 0
$$
An initial value problem is of the form:
$$
y'=f(x,y)\text{ with } y(x_o)=y_o
$$
given such that we assume that the problem has unique solution in some open interval $a<x<b$ containing $x$.

## Taylor-Series Method
Consider $y^{I}=f(x,y)\quad\_\_(1)$
differentiating $(1)$ w.r.t $x$ we get:
$y^{II}=f_x+f'f_y$
similiarly we find $y^{III}, y^{IV}\dots\text{substituting }y(x_o)=y_o$
Hence the taylor series of $y(x)$ is:-
$$
y(x)=y(x_o)+(x-x_o)(y^{I}(x_o))+\frac{(x-x_o)^2(y^{II}(x_o))}{2!}+\dots
$$

## Modified Euler Method
Given:
- $\frac{dy}{dx}=f(x,y)$
- $y(x_o)=y_o$
- $h=x_1-x_o$ (Step-Length)

Then:
$$
y_1^E = y_o + hf(x_o,y_o)
\\
\
\\
\qquad \implies y_o + hy'|_{x=x_o}
$$

Then, we have:
$$
y_1^{(1)} = y_o+\frac h2\bigg[f(x_o, y_o) + f(x_1, y_1^E)\bigg]
\\
\
\\
y_1^{(2)} = y_o+\frac h2\bigg[f(x_o, y_o) + f(x_1, y_1^{(1)})\bigg]
\\
\
\\
y_1^{(n+1)} = y_o+\frac h2\bigg[f(x_o, y_o) + f(x_1, y_1^{(n)})\bigg]
$$

## Runge - Kutta Method of 4^th^ order(RK Method)
Given:
- $\frac{dy}{dx}=f(x,y)$
- $y(x_o)=y_o$
- $h=x_1-x_o$ (Step-Length)

Then at $x_o=x_1+h$, $y_1=y_o+K$
Where:
$$
K=\frac16\bigg(k_1+2k_2+2k_3+k_4\bigg)
$$
And:
$k_1=hf(x_o,y_o)$
$k_2=hf(x_o+\frac h2, y_o+\frac {k_1}{2})$
$k_3=hf(x_o+\frac h2, y_o+\frac {k_2}{2})$
$k_4=hf(x_o+h,y_o+k_3)$

## Milne's Predictor - Corrector Method
Used to find the 5^th^ value of $y$ provided 4 preceeding values (with same step length) are known.
Consider:
- $\frac{dy}{dx}=f(x,y)$
- Suppose the solution is know at the following four points:
	- $x_o$
	- $x_1=x_o+h$
	- $x_2=x_o+2h$
	- $x_3=x_o+3h$
- These have the corresponding values $y_o, \ y_1,\ y_2,\ y_3$ respectively

We wish to find the value of $y_4$ at $x_4=x_o+4h$

1. First we predict the value of $y_4$ using Predictor formula:
$$
y_4^P = y_o +\frac{4h}{3}\bigg[2f_1-f_2+2f_3\bigg]
$$
2. We then apply $y_4^P$ in the Corrector formula to find the corrected value, $y_4^C$
$$
y_4^C=y_2+\frac h3\bigg[f_2+4f_3+f_4^P\bigg]
$$
3. We assign the obtained value, $y_4^C$ to be the new value of $y_4^P$ and repeat Step 2 to obtain newer value of $y_4^C$. This value is then compared with the assumed value, $y_4^P$ and repeated until desired order of accuracy is achieved.
## Application
### Growth / Decay
Intensity of Radiation $\propto$ amount of remaining radioactive substance.
$$
\frac{dy}{dt}=-Ky
$$