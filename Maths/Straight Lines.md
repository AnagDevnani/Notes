# Distance Formula

Let us have 2 points $A(x_1,y_1)$ and $B(x_2,y_2)$
<font color=red><image></font>
We draw a perpendicular to the point such that they meet at $C(x_1,y_2)$

<Picture of Distance formula triangle thing\>

Therefore, $AC = |y_1-y_2|$ And $BC = |x_1-x_2|$
Also, by Pythagoras' Theorem we have, $AB=\sqrt{AC^2 + BC^2}$
$$\boxed{\therefore \text{Distance (AB)} = \sqrt{(y_1-y_2)^2 + (x_1-x_2)^2}}
$$

# Section Formula
## Internal Division
We have $\text{AB}$ with Point $\text{P}$ cutting it in the ratio $m:n$.
We wish to find the coordinates at Point $\text{P}$
<font color=red><image\></font>
We draw perpendicular to $\text{A}$ & $\text{B}$ such that:
<font color=red><image\></font>
- Let the bases be $\text{C}$ & $\text{D}$ respectively

Looking at $\Delta\text{ACP}$ & $\Delta\text{PDB}$:
$\angle\text{PAC}=\angle\text{BPD}\qquad\text{(Corresponding)}$
$\angle\text{PCA}=\angle\text{BDP}\qquad\text{(90\degree)}$

$\therefore \text{by AA, }\Delta\text{ACP} \sim \Delta\text{PDB}$

$\therefore \frac{m}{n} = \frac{\text{AP}}{\text{PB}} = \frac{\text{AC}}{\text{PD}} = \frac{\text{CP}}{\text{DB}}$

$\therefore \frac{m}{n} = \frac{\text{AC}}{\text{PD}}=\frac{x-x_1}{x_2-x}$

$\implies m(x_2-x) = n(x-x_1)$
$\implies mx_2+nx = mx+nx$
$\therefore\boxed{x=\frac{mx_2+nx_1}{m+n}}$

$\text{Similiarly, \boxed{y=\frac{my_2+ny_1}{m+n}}}$
 
# Area of a Triangle
Let us have a $\Delta\text{ABC}$:
<font color=red>\<image></font>
We drop perpendiculars from $\text{A, B, C}$ down to $x$-axis such that they form trapeziums
From the diagram it is visible that $\text{Area of }\Delta = \text{Ar()}-\text{Ar()}-\text{Ar()}$
We know that $\text{Ar(Trapezium)}=\frac{1}{2}\text{(Sum of Parralel Sides}\times\text{Perpendicular Height)}$
Upon Solving we get:-
$\boxed{\text{Area of }\Delta =\frac{1}{2}\Big|x_1(y_2-y_3) + x_2(y_3-y_1) + x_3(y_1-y_2)\Big|}$
**Note:** the coordinated must be taken in **Anti-Clockwise** direction


# Slope
<font color=red>\<image></font>
$\theta=\text{angle of inclination}$
$m=\tan\theta = \frac{\text{AC}}{\text{BC}} = \frac{\footnotesize{y_2-y_1}}{\footnotesize{x_2-x_1}}$

If 2 lines are **parallel** $\implies m_1=m_2$
if 2 lines are perpendicular $\implies m_1=-\frac{\footnotesize 1}{\footnotesize m_2}$

## Relation of Angle between Lines & Slopes
Let us have 2 non-vertical lines with slope $m_1$ & $m_2$ respectively and angle of inclinations $\theta_1$ & $\theta_2$ respectively

They are also non-parallel and non-intersecting and as such intersect forming adjacent angle, $\phi$

<font color=red>\<image></font>
It is observed that $\phi$ is the angle between the 2 lines
And, $\angle\text{BAC} = \phi\qquad\text{(V.O.A.)}$
And, $\angle\text{ACB} = 180\degree - \theta_2\qquad\text{(Linear Angles)}$

Now in $\Delta\text{ABC}$:
$\angle\text{ABC}+\angle\text{ACB}+\angle\text{BAC}=180\degree$
$\therefore\phi+\theta_1+180\degree-\theta_2=180\degree$
$\implies\phi=\theta_2-\theta_1$

$\therefore \tan\phi=\tan(\theta_2-\theta_1)=\frac{\tan\theta_2-\tan\theta_1}{1+\tan\theta_1\theta_2}$

As $\tan\theta_1=m_1$ & $\tan\theta_2=m_2$:
$\boxed{\tan\phi=\frac{m_2-m_1}{1+m_1m_2}}$

# Representation of a Line
## General Equation
$$
\text{A}x+\text{B}y+\text{C} = 0
$$

## Slope-Point Form
For a non-vertical line $l$, with slope $m$ and a point $(x_1,y_1)$ on the line.
Let us have an arbitrary point with coordinates $(x, y)$

$$
m=\frac{y-y_1}{x-x_1}
\\
\
\\
\therefore\boxed{y-y_1=m(x-x_1)}
$$

## 2-Point Form
Let us have 2 points $(x_1,y_1)$ and $(x_2,x_3)$.
We also take an arbitrary point with coordinates $(x,y)$
$$
m=\frac{y_2-y_1}{x_2-x_1} = \frac{y-y_1}{x-x_1}
\\
\
\\
\therefore\boxed{y-y_1=(x-x_1)\frac{y_2-y_1}{x_2-x_1}}
$$

## Slope-Intercept Form
### $y$-intercept form
Let us have an intercept $(0,c)$ on line $l$ with slope $m$
$$
m=\frac{y-c}{x-0}
\\
\
\\
\therefore\boxed{y=mx+c}
$$
### $x$-intercept form
Let us have an intercept $(d,0)$ on line $l$ with slope $m$
$$
m=\frac{y-0}{x-d}
\\
\
\\
\therefore\boxed{y=m(x-d)}
$$

## Intercept Form (2 Intercepts)
Suppose a line $l$ has 2 points $(a,0)$ & $(b,0)$
We take an arbitrary point $(x,y)$ on the line
$$
m=\frac{y-0}{x-a}=\frac{y-b}{x-0}
\\
\
\\
\implies xy=xy-ay-bx+ab
\\
\
\\
ay+bx=ab
\\
\
\\
\boxed{\frac yb + \frac xa=1} \qquad\text{(Dividing by }ab\text{ on both sides)}
$$

# Distance of a Point from a Line
Let us have a line with general equation $Ax+By+C=0$ and we wish to find the distance of the point $P\space (x_1,y_1)$
$$
\boxed{\frac{|Ax_1+By_1+C|}{\sqrt{A^2+B^2}}}
$$

# Distance between 2 Parallel Lines
Let us have 2 Parallel Lines with equations $Ax+By+C_1=0$ and $Ax+By+C_2=0$ respectively
$$
\boxed{\frac{|C_1-C_2|}{\sqrt{A^2+B^2}}}
$$

# Sum Squared Error
$$
\boxed{\text{SSE}=\sum_{i=1}^n(y_i-mx_i-c)^2}
$$