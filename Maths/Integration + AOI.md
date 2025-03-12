# Introduction:
Difference between integration and summation:
$$
\int \longrightarrow\text{ Continous}
\\
\
\\
\sum\longrightarrow\text{ Discrete}
$$
- Geometrically, it represents area under the curve (by taking rectangular strips of length $\text{f}(x)$ and width $x$)
# Standard
## $\frac{px+q}{{ax^2+bx+c}}$ form:
$$
\int\frac{dx}{X^2+A^2} = \frac{1}{A}\tan^{-1}\bigg(\frac{X}{A}\bigg)+C
$$
**Proof:**

$$
\int\frac{dx}{X^2-A^2} = \frac{1}{2A}\log\bigg|\frac{X-A}{X+A}\bigg|+C
$$
**Proof:**

$$
\int\frac{dx}{A^2-X^2} = \frac{1}{2A}\log\bigg|\frac{A+X}{A-X}\bigg|+C
$$
**Proof:**

## $\frac{px+q}{\sqrt{ax^2+bx+c}}$ form:
$$
\int\frac{dx}{\sqrt{X^2+A^2}} = \log|X+\sqrt{X^2+A^2}| + C
$$
**Proof:** Put $X=A\tan\theta$

$$
\int\frac{dx}{\sqrt{X^2-A^2}} = \log|X+\sqrt{X^2-A^2}| + C
$$
**Proof:** Put $X=A\cosec\theta$

$$
\int\frac{dx}{\sqrt{A^2-X^2}} = \sin^{-1}\bigg(\frac{X}{A}\bigg)+C 
$$
**Proof:** Put $X=A\sin\theta$

## Integration by Parts
$$
\int u.v\ dx=u\int v \ dx - \int\bigg(\frac{du}{dx}.\scriptsize{\int}\normalsize{v\ dx}\bigg)
$$
where $v$, is the function which can be easily integrated
## Leibnitz Theorem
$$
\text{If: }p(x) = \int^{g(x)}_{h(x)} f(t)dt
\\
\
\\
\text{Then: } p'(x) = f(g(x)).g'(x) - f(h(x)).h'(x)
$$
## Reduction Formula
Only when limit is from $0 \rightarrow \frac \pi2$ and integral is of the type:
$$
\int\limits_0^{\frac\pi 2}\sin^mx\ dx \text{ Or }
\int\limits_0^{\frac\pi 2}\cos^mx\ dx 
$$
Where $m$ is an integer.
Then:
$$
\int\limits_0^{\frac\pi 2}\sin^mx\ dx = \frac{m-1}{m} \times\frac{m-3}{m-2}\times\frac{m-5}{m-4}\dots\times1\times k
$$
where: $k=\begin{cases}\frac\pi2, m\rightarrow\text{even}\\1, m\rightarrow\text{odd}\end{cases}$


# Double Integration
$$
\int\int f(x,y)dxdy=\int\int f(x,y)dydx
$$
- i.e. order does not matter provided limits are appropriate.
- Geometrically, it represents volume (by taking parellopiped segments).
	- Therefore, when $f(x,y)=1$, it denotes the area of parallelogram (region) $dxdy$. <font color=red>Need to verify</font>

## Fubini's Theorem
### 1<sup>st</sup> Form
If $f(x,y)$ is continous on a rectanglular region, $R$ and $a\leq x\leq b$ & $c\leq y \leq d$, then:
$$
\iint\limits_R f(x,y)dxdy = \int\limits_{x=a}^{x=b}\int\limits_{y=c}^{y=d}f(x,y)dydx=\int\limits_{y=c}^{y=d}\int\limits_{x=a}^{x=b}f(x,y)dxdy
$$
### 2<sup>nd</sup> form
If $f(x,y)$ is continous on a rectanglular region, $R$ and $a\leq x\leq b$ & $g_1(x)\leq y \leq g_2(x)$, then:
$$
\iint\limits_R f(x,y)dxdy = \int\limits_{x=a}^{x=b}\int\limits_{y=g_1(x)}^{y=g_2(x)}f(x,y)dydx
$$
The inverse is also true when $x$ has variable limits and $y$ has constant limits.

**Note:** The variable integration (indefinite) is always taken first (inside) and constant limits (definite) is taken second (outside). Therefore, there is no constant of integration.

## Applications of Double Integration
### 1) Area of region by $\iint$
$$
\text A=\iint\limits_R dxdy = \iint\limits_R r\ drd\theta
$$

# Triple Integration
## Volume of region using $\iiint$
$$
\text A=\iiint\limits_R dzdydx
$$
Implying, when $f(x,y,z)=1$ it gives volume.

# Beta & Gamma Functions ($\beta$ & $\Gamma$)
These are 2 special functions which help us to evaluate certain definite integrals which are either difficult or impossible to evaluate by various known methods of integration.
$$
\beta(m,n)=\int\limits_0^1 x^{m-1}(1-x)^{n-1}\ dx
\\
\
\\
\Gamma(n) = \int\limits_0^\infty e^{-x} x^{n-1} \ dx
$$
where $m,n > 0$

### Polar Form of Beta Function
put $x=\sin^2\theta$ 
$\therefore \ dx=2\sin\theta\cos\theta\ d\theta$
$$
\beta(m,n)=2\int\limits_0^{\frac\pi2}\sin^{2m-1}\theta\cos^{2n-1}\theta\ d\theta
$$

### Alternate form of Beta Function
$$
\beta(m,n)=\int\limits_0^\infty\frac{x^{m-1}}{(1+x)^{m+n}}
$$
put $x=\tan^2\theta$
$\therefore\ dx=2\tan\theta\sec^2\theta\ d\theta$
$\beta(m,n)=2\int\limits_0^{\frac\pi2}\frac{(\tan\theta)^{2m-2}}{(\sec\theta)^{2m+2n}}\tan\theta\sec^2\theta\ d\theta$
$\beta(m,n)=2\int\limits_0^{\frac\pi2}\frac{(\tan\theta)^{2m-1}}{(\sec\theta)^{2m+2n-2}}\ d\theta =2\int\limits_0^{\frac\pi2}\sin^{2m-1}\theta\cos^{2n-1}\theta\ d\theta$

### Alternative form of Gamma Function
put $x=t^2$
$\therefore \ dx=2tdt$
$$
\Gamma(n)=2\int\limits_0^\infty e^{-t^2}t^{2n-1}\ dt
$$

## Properties of Beta & Gamma Functions:
1) $\beta(m,n) = \beta(n,m)$
	- Take $(1-x)=y$
2. $\Gamma(n+1)=n\times\Gamma(n)$
	- Start with LHS and apply integration by parts taking $x^n\rightarrow u$, $e^x\rightarrow v$
3. $\Gamma(n+1) = n!$
	- From (2) by taking $\Gamma(n+1)=n\times\Gamma(n) = n\times(n-1)\Gamma(n-1)=\dots=n!\times\Gamma(1) = n!$
4. $\Gamma(n)\times\Gamma(1-n)=\frac{\pi}{\sin(n\pi)}$
	- Replace $m=n,\ n=(1-n)$ in Alternate form of $\beta(m,n)$
	- given that, $\int\limits_0^\infty\frac{x^{n-1}}{1+x}=\frac{\pi}{\sin(n\pi)}$ <font color=red>(Need to check how tho)</font>

**Tips for taking value of $\Gamma()$**
- Take $\Gamma(n+1)=n\times\Gamma(n), \ n\longrightarrow\text{+ve fraction}$
- Take $\Gamma(n+1)=n!, \ n\longrightarrow\text{+ve integer}$
- Take $\Gamma(n)=\frac{\Gamma(n+1)}{n}, \ n\longrightarrow-\text{ve fraction}$
- $\Gamma(n)$ is not defined for $n=0$ and $\text{-ve integer}$

## Relation b/w Beta & Gamma Functions:
$$
\beta(m,n)=\frac{\Gamma(m)\Gamma(n)}{\Gamma(m+n)}
$$
Proof:
$\Gamma(m)=2\int\limits_0^\infty e^{-x^2}x^{2m-1}\ dx$
$\Gamma(n)=2\int\limits_0^\infty e^{-y^2}y^{2n-1}\ dy$
$\Gamma(m)\Gamma(n)=4\int\limits_0^\infty\int\limits_0^\infty e^{-(x^2+y^2)}x^{2m-1}\ y^{2n-1}\ dydx$
(As $x$ and $y$ are independent of each other.) 
putting $x=r\cos\theta,\ t=r\sin\theta,\ dydx=rdrd\theta$:
$\Gamma(m)\Gamma(n)=4\int\limits_0^\frac{\pi}{2}\int\limits_0^\infty e^{r^2}(r\cos\theta)^{2m-1}(r\sin\theta)^{2n-1}\ r\ drd\theta$
$\Gamma(m)\Gamma(n)=4\int\limits_0^\frac{\pi}{2}\int\limits_0^\infty e^{r^2}r^{2(m+n)-1}\cos^{2m-1}\theta\sin^{2n-1}\theta\ drd\theta$
$\Gamma(m)\Gamma(n)=2\int\limits_0^\infty e^{r^2}r^{2(m+n)-1}\ dr\times2\int\limits_0^\frac{\pi}{2}\cos^{2m-1}\theta\sin^{2n-1}\theta\ d\theta$
$\Gamma(m)\Gamma(n)=\beta(m,n)\times\Gamma(m+n)$
$\therefore \ \beta(m,n)=\frac{\Gamma(m)\Gamma(n)}{\Gamma(m+n)}$

## Value of $\Gamma(\frac12)$
$$
\Gamma\bigg(\frac12\bigg)=\sqrt\pi
$$
Proof:
$\Gamma\big(\frac12\big)=2\int\limits_0^\infty e^{-x^2} = 2\int\limits_0^\infty e^{-y^2}$ 
$\big(\Gamma\big(\frac12\big)\big)^2=4\int\limits_0^\infty\int\limits_0^\infty e^{-(x^2+y^2)}$ 
put $x=r\cos\theta,\ y=r\sin\theta,\ dydx=rd\theta dr$
$\big(\Gamma\big(\frac12\big)\big)^2=4\int\limits_0^\infty\int\limits_0^\frac{\pi}{2} e^{-r^2}rd\theta dr$
$\big(\Gamma\big(\frac12\big)\big)^2=2\int\limits_0^\infty e^{-r^2}r\ dr\times 2\int\limits_0^\frac{\pi}{2} d\theta$
$\big(\Gamma\big(\frac12\big)\big)^2=\Gamma(1)\times \pi$

$\therefore \ \Gamma\big(\frac12\big)=\sqrt\pi$