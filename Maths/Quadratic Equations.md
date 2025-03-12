# General Equation
$$
f(x)=ax^2+bx+c \qquad ,a\neq0
$$

# Graph (Parabola) 
The Graph of all quadratic equations is a Parabola.
The vertex of the parabola is the point at which the parabola is symmetric.
**Note:** the Vertex is equidistant from the zeroes of the parabola

- The $x$-coordinate of the vertex $= \frac{-b}{2a}$
	- By putting $f'(x)=0$ and solving for $x$
	- OR from completing the square method we find that $(x+\frac{b}{2a})=0$
- The $y$-coordinate of the vertex $=c-\frac{b^2}{4a}$
	- By putting $x=\frac{-b}{2a}$ in the $f(x)$
- The $y$-intecept of the curve is $c$
	- By Putting $x=0$ in $f(x)$

## Direction of Graph

### If $a>0:$
- The Graph will open **Upward**.
- It will have its **minimum** value at Vertex.

### If $a<0:$
- The Graph will open **Downward**
- It will have its **maximum** value at Vertex


# Solution of Quadratic Equations
## By Factorization (Splitting middle term)
In this method we wish to convert General Form to Intercept form
$$
px^2+qx+r\longrightarrow (ax+b)(cx+d)
$$
where $-\frac ba$ and $-\frac dc$ are $x$-intercepts(zeroes) of the function.

 ### Conversion from General to Intercept Form
 We have:
$$
px^2+qx+r\tag1
$$

Expanding $(ax+b)(cx+d)$ we get:
$$
ac\space x^2 + (ad+bc)x+bd\tag2
$$
On comparing $\text{(1) \& (2)}$
$p=ac$
$r=bd$
$q=ad+bc$
$\therefore pr=abcd$

Now we try to guess $ad$ and $bc$ such that their product is $pr$ and sum is $q$
Therefore, $ad$ & $bc$ will be factors of $pr$ and will add up to $q$
 For example:
$$
x^2+5x+6
$$
we have $pr=6$
and $q=5$

we therefore guess $ad$ & $bc$ to be 2 and 3

$$
x^2+2x+3x +6
\\
\
\\
\implies x(x+2)+3(x+2)
\\
\
\\
\implies (x+2)(x+3)
$$

## Completing the Square
- We wish to convert General equation into the form of $(px+q)^2-r$ 

$ax^2+bx+c = 0$

Dividing by $p$:

$x^2+\frac ba x +\frac ca=0$

$\implies x^2 + 2\times\frac{b}{2a}\times x + \frac ca$

$\implies \Big(x^2 + 2\times\frac{b}{2a}\times x + \frac{b^2}{4a^2}\Big) - \frac{b^2}{4a^2} + \frac ca$

$\implies \boxed{\normalsize\Big(x+\frac{b}{2a}\Big)^2 - \frac{b^2}{4a^2} + \frac ca=0}$

## Quadratic Formala
- The Quadratic Formaula comes from the method of Completing the Square itself

From Completing the Square we have:-
$(x+\frac{b}{2a})^2 - \frac{b^2}{4a^2} + \frac ca = 0$

$\implies (x+\frac{b}{2a})^2 = \frac{b^2}{4a^2} - \frac ca$

$\implies x+\frac{b}{2a} = \pm\sqrt{\frac{b^2}{4a^2} - \frac ca}$

$\implies x = -\normalsize{\frac{b}{2a}\pm\sqrt{\frac{b^2}{4a^2} - \frac ca}}$

$\implies x = -\normalsize{\frac{b}{2a}\pm\sqrt{\frac{b^2-4ac}{4a^2}}}$

$\implies \boxed{x = \normalsize{\frac{-b\pm\sqrt{b^2-4ac}}{2a}}}$

- Here, $b^2-4ac = D$ where $D$ is the Discriminant.
	- If $D>0 \implies\text{2 Real Solutions}$
	- If $D=0 \implies\text{1 Real Solution}$
	- If $D<0 \implies\text{No Real Solutions}$