Misc
$$
(x+y+z)^2=x^2+y^2+z^2 + 2(xy +yz+zx)
$$

$$
x^3+y^3+z^3 -3xyz = (x+y+z)(x^2+y^2+z^2-xy-yz-zx)
$$
Calculus in 2 Variables
# Partial Differentiation
Here we use the symbol $\partial$ (doh / del) to denote partial derivatives.
Let us have a function, $u=f(x,y)$
Then.
$$
U_x = \frac{\partial u}{\partial x} = f’(x,y) \text{when taking y as constant}
\\
\
\\
U_y = \frac{\partial u}{\partial y} = f’(x,y) \text{when taking x as constant}
$$
**for 2nd order:**
$$
U_{xx} =\frac{\partial}{\partial x}\bigg(\frac{\partial u}{\partial x}\bigg) = f’’(x,y) \text{when taking y as constant}
\\
\
\\
U_{yy} = \frac{\partial}{\partial y}\bigg(\frac{\partial u}{\partial y}\bigg) = f’’(x,y) \text{when taking x as constant}
$$
**Mixed 2nd order:**
$$
U_{xy} =\frac{\partial}{\partial x}\bigg(\frac{\partial u}{\partial y}\bigg) = \frac{\partial^2u}{\partial x\partial y} = f’’(x,y)
\\
\
\\
U_{yx} =\frac{\partial}{\partial y}\bigg(\frac{\partial u}{\partial x}\bigg) = \frac{\partial^2u}{\partial x\partial y} = f’’(x,y)
$$


For 2nd order only, $u_{xy}=u_{yx}$

Note: here the order of variables mentioned matters.
E.g. $u_{AB}$ means partially differentiating with B first and then A

# Composite Functions
## Partial Differentials to Ordinary (Total Derivatives)
if, $u=f(x,y,z), \ x=f_1(t),\  y=f_2(t),\  z=f_3(t))$
$$
U\longrightarrow f(x,y,z) \longrightarrow f(t)
$$
Then:
$$
\frac{\partial u}{\partial t} = \frac{\partial u}{\partial x}\times\frac{dx}{dt} + \frac{\partial u}{\partial y}\times\frac{dy}{dt} + \frac{\partial u}{\partial z}\times\frac{dz}{dt}
$$
## Partial to Partial (Chain Rule)
If $u=f(x,y,z), x=f_1(r,s,t), y=f_2(r,s,t), z=f_3(r,s,t)$

$$
U\longrightarrow f(x,y,z) \longrightarrow f(r,s,t)
$$
Then:
$$
\frac{\partial u}{\partial r} = \frac{\partial u}{\partial x}\times\frac{\partial x}{\partial r} + \frac{\partial u}{\partial y}\times\frac{\partial y}{\partial r} + \frac{\partial u}{\partial z}\times\frac{\partial z}{\partial r}
\\
\
\\
\frac{\partial u}{\partial s} = \frac{\partial u}{\partial x}\times\frac{\partial x}{\partial s} + \frac{\partial u}{\partial y}\times\frac{\partial y}{\partial s} + \frac{\partial u}{\partial z}\times\frac{\partial z}{\partial s}
\\
\
\\
\frac{\partial u}{\partial t} = \frac{\partial u}{\partial x}\times\frac{\partial x}{\partial t} + \frac{\partial u}{\partial y}\times\frac{\partial y}{\partial t} + \frac{\partial u}{\partial z}\times\frac{\partial z}{\partial t}
$$
Laplace Equation:
$$
u_{xx}+u_{yy}+u_{zz}=0
$$
**When questions are of the form of:**
$$
u= f(\underbrace{x\pm y\pm z}_{(1)},\underbrace{x\pm y\pm z}_{(2)},\underbrace{x\pm y\pm z}_{(3)})
$$
Take $(1)=p$, $(2)=q$, $(3)=r$
Then find $\frac{\partial u}{\partial x}$ leaving $\frac{\partial u}{\partial (p/q/r)}$ as it is and solving in the end.
**e.g.** $u=f(x-y,y-z,z-x)$ then P.T. $u_x+u_y+u_z=0$

# Jacobian Matrix
- For 1st order partial diff.
- If $u$ & $v$ are functions of 2 independant variables, $x$ & $y$ then the Jacobian is denoted by:
$$
J\frac{(u,v)}{(x,y)} = \frac{\partial(u,v)}{\partial(x,y)} = \begin{vmatrix}u_x & u_y\\v_x & v_y \end{vmatrix}
$$
Similiarly:
$$
J\frac{(u,v,w)}{(x,y,z)} = \frac{\partial(u,v,w)}{\partial(x,y,z)} = \begin{vmatrix}u_x & u_y & u_z\\v_x & v_y &v_z\\w_x&w_y&w_z \end{vmatrix}
$$

## Properties of Jacobian Matrix
1) If $u$ & $v$ are functions of $x, \ y$: 
Then, $J = \frac{\partial(u,v)}{\partial(x,y)}$ & $J' = \frac{\partial(x,y)}{\partial(u,v)}$
Then, $J\times J' =1$

2) If $u$ &$v$ are functions of $r,\ s$ and $r,\ s$ are functions of $x,\ y$ (Chain Rule):
Then, $\frac{\partial(u,v)}{\partial(x,y)}= \frac{\partial(u,v)}{\partial(r,s)}\times  \frac{\partial(r,s)}{\partial(x,y)}$

3. $u$ & $v$ are said to be functionally dependant if $J=0$
# Gradient Descent (Method / Matrix <font color=red>????</font>)
## Hessian Matrix
$$
2\times2\longrightarrow\begin{vmatrix}f_{xx}&f_{xy}\\f_{yx}&f_{yy}\end{vmatrix}
$$
$$
3\times3\longrightarrow\begin{vmatrix}f_{xx}&f_{xy}&f_{xz} \\ f_{yx}&f_{yy}&f_{yz} \\ f_{zx}&f_{zy}&f_{zz}\end{vmatrix}
$$
Here, $\Delta f_i=\begin{bmatrix}f_x\\ f_y\end{bmatrix}$

And, $X_i=\begin{bmatrix}a\\ b\end{bmatrix}$
## Steps
1. Find $S_i$ at $X_i$
$$
S_i=-\Delta f_i
$$
2. Find $\lambda_i$
$$
\lambda_i=\frac{S_i^T.S_i}{S_i^T.H.S_i}
$$
**Note:** Here, $H$ is the original matrix.

3. Find $X_{i+1}$
$$
X_{i+1}=\bigg(X_i^T+\lambda_i.S_i\bigg)^T
$$
4. Substitue $X_{i+1}$ in $\Delta f_i$
	- If $\Delta f(X_{i+1}) = 0$: Substitute in $f(x,y)$ to find extreme values.
	- Else: Continue to Step 1.
# Taylor Series
$$
f(x) = f(a) + f'(a)(x-a)+\frac{f''(a)(x-a)^2}{2!}+\frac{f'''(a)(x-a)^3}{3!}
\\
\
\\
f(x,y)=f(a,b)+(x-a)f_x(a,b) +(y-b)f_y(a,b) +\frac{1}{2!}\bigg((x-a)^2f_{xx}(a,b)+(x-a)(y-b)f_{xy}(a,b)+(y-b)^2f_{yy}(a,b)\bigg) + \frac{1}{3!}\bigg((x-a)^3f_{xxx}(a.b)+3(x-a)^2(y-b)f_{xxy}(a,b)+3(x-a)(y-b)^2f_{xyy}(a.b)+(y-b)^3f_{yyy}(a,b)\bigg)
$$
When $a=0$, it is called Maclaurin Series.

# Maxima & Minima.
- Necessary Conditions for f(x,y) to have extrema at $a,b$ are:
$$
f_x(a,b) = 0\quad\&\quad f_y(a,b)=0
$$
## Working method to find maxima and minima:
for $z=f(x,y)$:
1) Find $z_x, \ z_y$ and equate to zero to solve simultaneosly and fing value of $a$ & $b$
2) Calculate the values of $\underbrace{z_{xx}}_{\text r},\  \underbrace{z_{xy}}_{\text s} \text{ and } \underbrace{z_{yy}}_{\text t}$ at $(a,b)$
3) 
	- if $rt-s^2>0$ and $r<0$: $f(a,b)$ is the maxima.
	- if $rt-s^2>0$ and $r>0$: $f(a,b)$ is the minima.
	- if $rt-s^2<0$: $(a,b)$ is a saddle point.
	- if $rt-s^2=0$: <font color=red>the case is doubtful and needs further investigation.</font>