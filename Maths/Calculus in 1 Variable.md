# Polar Form of Representation
<font color='red'></image of $P=r\sin\theta$ with X and Y.png\> </font>

**From the Figure:**
$$
y=r\sin\theta
\\
x=r\cos\theta
$$

# Angle between Radius Vector and Tangent
- Take a non-constant function in polar form $r=f(\theta)$. 
- We take the angle between the Radius Vector and Tangent to be $\phi$.
- $\theta$ and $\psi$ are taken as the angle of inclination of $r$ and Tangent respectively.

Now, From the figure we hve $\psi=\theta + \phi$

Applying $\tan$ on both sides we get:
$$
\tan\psi=\frac{\tan\theta+\tan\phi}{1-\tan\theta\tan\phi}
$$
Now we also have $\tan\psi=\frac{dy}{dx} = \frac{dy/d\theta}{dx/d\theta}$

We know, $y=r\sin\theta$
$$
\therefore \frac{dy}{d\theta}=\frac{dr}{d\theta}\sin\theta + r\cos\theta
$$
And $x=r\cos\theta$
$$
\therefore \frac{dx}{d\theta}=\frac{dr}{d\theta}\cos\theta - r\sin\theta
$$
As, $\tan\psi = \frac{dy}{dx} = \frac{dy/d\theta}{dx/d\theta}$
$$
\therefore \tan\psi = \frac{\frac{dr}{d\theta}\sin\theta + r\cos\theta}{\frac{dr}{d\theta}\cos\theta - r\sin\theta}
$$
Dividing Numerator and Denominator by $\frac{dr}{d\theta}\cos\theta$:
$$
\tan\psi = \frac{\tan\theta+ r\frac{d\theta}{dr}}{1 - \tan\theta.r\frac{d\theta}{dr}}
$$

Comparing with (1) we can say that:
$$
\tan\phi=r\frac{d\theta}{dr}
\\
\
\\
\therefore \cot\phi = \frac1r\frac{dr}{d\theta}
$$

**Note:** 
For questions we take $\log$ such that $\log r$ is a term.
Differentiation $\log r$ w.r.t. $\theta$ we get $\frac1r\frac{dr}{d\theta} = \cot\phi$

## Angle b/w curves (Polar Form)
- Angle of Intersection b/w 2 curves = Angle of intersection of tangents
- It is denoted by $\alpha$
$$
\therefore\alpha=|\phi_1-\phi_2|
\\
\
\\
\tan\alpha=\bigg|\frac{\tan\phi_1-\tan\phi_2}{1+\tan\phi_1\tan\phi_2}\bigg|
$$

# Length of Perpendicular from Pole to the Tangent
- Let P denotes the length of the $\perp$ from pole, $\text P$ to the tangnt of the curve, $r=f(\theta)$

<font color='red'></image of $P=r\sin\theta$ with tangent and perpendicular.png\> </font>

We extend the tangent through $x$-axis and draw a perpendicular from $\text O$ denoted by $\text P$

From Figure,
$$
\sin\phi=\frac{\text OM}{\text ON} = \frac{\text P}{r}
\\
\
\\
\therefore\boxed{\text{P} = r\sin\phi}
$$

Sqauring and taking reciprocal,
$$
\frac{1}{\text{P}^2} = \frac{1}{r^2}\cosec^2\phi
\\
\
\\
\frac{1}{\text{P}^2} = \frac{1}{r^2}(1+\cot^2\phi)
\\
\
\\
\frac{1}{\text{P}^2} = \frac{1}{r^2}\Big(1+\frac{1}{r^2}\Big(\frac{dr}{d\theta}\Big)^2\Big)
\\
\
\\
\boxed{\frac{1}{\text{P}^2} = \frac{1}{r^2}+\frac{1}{r^4}\Big(\frac{dr}{d\theta}\Big)^2}
$$

# Curvature & Radius of Curvature
<\image>
- Let $\psi$, $\psi+\delta\psi$ be the angles made by the tangents to the curve at $\text{P}$ and $\text{Q}$ with the $x$-axis, then $\delta\psi$ is the angle b/w the tangents
- Here, $\delta\psi$ depends on $\delta S$
$$
\therefore \text{Mean Curvature of arc PQ} = \frac{\delta\psi}{\delta S}
$$
- Curvature: The amount of bending of the curve at P, denoted by $K$:
$$
K=\lim\limits_{\delta S\rightarrow0}\frac{\delta\psi}{\delta S}=\frac{d\psi}{dS}
$$

- The reciprocal of Curvature is defined as the Radius of Curvature, denoted by $\rho$:
$$
\rho=\frac{1}{k}=\frac{dS}{d\psi}
$$

## $\rho$ in cartesian form

As,
$$
\tan\psi=\frac{dy}{dx}
$$

Differentiating both sides w.r.t. $dS$:
$$
\sec^2\psi\times\frac{d\psi}{dS} = \frac{d}{dx}\bigg(\frac{dy}{dx}\bigg) \times \frac{dx}{dS}
\\
\
\\
\implies \sec^2\psi\times\frac{1}{\rho} = y_2\times \frac{dx}{dS}
$$

## <font color=pink>As $\frac{dx}{dS}=\cos\psi$, [NOT SURE HOW]</font>
$$
\implies \sec^2\psi\times\frac{1}{\rho} = y_2\times \cos\psi
\\
\
\\
\therefore \rho=\frac{\sec^3\psi}{y_2} = \frac{(\sec^2\psi)^{3/2}}{y_2}
\\
\
\\
\rho= \frac{(1+\tan^2\psi)^{3/2}}{y_2}
\\
\
\\
\boxed{\rho= \frac{(1+y_1^2)^{3/2}}{y_2}}
$$
Also, 
$$
\boxed{\rho= \frac{(1+x_1^2)^{3/2}}{x_2}}
$$

## $\rho$ in parametric form
$x=x(t)$, $y=y(t)$
$$
\boxed{\rho = \frac{(x_1^2+y_1^2)^{3/2}}{x_1y_2 - y_1x_2}}
$$

## $\rho$ in polar form
$r=f(\theta)$
$$
\rho = \frac{(r^2+r_1^2)^{3/2}}{r^2+2r_1^2-rr_2}
$$
Where:
$r_1 = \frac{dr}{d\theta}$

$r_2 = \frac{d^2r}{d\theta^2}$
Alternative:
$$
\rho=r\frac{dr}{dP}
$$

## Hyperbolic Trigonometric Functions
$$
\sin hx = \frac{e^x-e^{-x}}{2}
\\
\
\\
\cos hx = \frac{e^x+e^{-x}}{2}
\\
\
\\
\tan hx = \frac{e^x-e^{-x}}{e^x+e^{-x}}
$$

Significance:
$\frac{d}{dx}(\sin hx) = \cos hx$

$\frac{d}{dx}(\cos hx) = \sin hx$ (No -ve Sign)
