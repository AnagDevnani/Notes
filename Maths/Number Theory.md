# Mod (Division)
## $\text{mod}$ function
if we say some $x\space \text{mod} \space y = z$ then we say:
$z$ is the remainder obtained on dividing $x$ by $y$
**e.g.** $28 \space\text{mod}\space 3=1$

## $|$ function (Divides)
we say $a\space|\space b$ if:
$a$ is a factor of $b$ (completely divides) OR $b\space\text{mod}\space a=0$
**e.g.** $3 \space|\space 96,\quad 2 \space|\space 1024$

If $a$ is not a factor of $b$ then:
we say $a\not| \  \ b$
e.g. $2\not| \  \ 21$

# Congruency and its applications
if $a$ & $b$ are the integers that give the same remainder when divided by a natural number, $n$ then $a$ is congreuent to $b$ modulo $n$ <font color=red>????confirm????</font>

Let $n$ be a positive integer & $a \equiv b\text{ mod }  n$
If $\frac{a-b}{n}=k$ <font color=red>incompkete</font>

# Euclid's Algorithm
- let $a$ & $b$ be any 2 numbers, $a\geq b \geq0$
- then, $\text{gcd}(a.b) = au+bv$ where $a,b$ are any 2 numbers.

## Working Rule to find the unique solution of congruence:
$$
ax\equiv b \text{ mod } n\quad\text{, if gcd(}a,n)=1\tag1
$$
$$
\text{Then,} \quad ax-b=k.n
\\
\
\\
\therefore \quad x=\frac{k.n+b}{a}
$$
i) $\text{gcd}(a,n)$ in linear form:
$$
au+nv=1
$$
ii) $\therefore au \equiv 1 \text{ mod } n$
Muliplying $b$ on both sides:
$$
a(ub) \equiv b\text{ mod } n
$$

Comparing from $(1)$, $x=ub$

# <font color=red>______________</font> Method
## Working rule to find solution of congruence
$$
ax\equiv b\text{ mod } n
\\
\
\\
\text{When gcd}(a,n)\neq 1
$$
#### 1) divide the given congruence by $d$:
$$
\bigg(\frac ad \bigg)x\equiv \bigg(\frac bd\bigg) \text{ mod }\bigg(\frac nd\bigg)\tag1
$$
#### 2) The unique solution of equation $(1)$ is:
$$
x\equiv t\text{ mod } \frac nd
$$ 
#### 3) For many solutions:
$$
x_k=t+(k-1)\frac nd\text{ mod } n
$$
# Chinese Remainder Theorem (CRT)
- CRT is used to solve a set of different congruence equations with one variable but different modulli which are coprime as shown below:
$$
x\equiv a_1\text{ mod }m_1
\\
x\equiv a_2\text{ mod }m_2
\\
\vdots
\\
x\equiv a_n\text{ mod }m_n
$$
CRT states that the above equations have a unique soluion:
$$
X=(a_1M_1M_1^{-1}+a_2M_2M_2^{-1}+\dots+a_nM_nM_n^{-1}) \text{ mod } M
$$
where:
- $M=m_1\times m_2\times\dots\times m_n$
- $M_k=\frac {M}{m_k}$
- $M_k\times M_k^{-1}= 1 \text{ mod } m_k$
	- solve for $M_k^{-1}$ using $ax\equiv b\text{ mod } m$

# Linear Diphantine Equations (LDE)
- An equation of the form of $ax+by+c=0$ or $ax+by=c$, $a\neq0$, $b\neq0$, $c$ is an integer is called a linear diphantine equation in 2 variables, $x$ & $y$
## Solution of Linear Diphantine Equation:
A pair $(x_o,\ y_o)$ is called solution of LDE $ax+by=c$ if:
$$
ax_o+by_o=c
\\
\text{and, }\quad \text{gcd}(a, \ b)=d
$$ 
Therefore:
$$
\text{iff: } c | d \qquad\text{(i.e. }d\text{ divides }c)
$$
$$
x_1=x_o+\frac bd t
\\
\
\\
y_1=y_o+\frac ad t
$$
Here, $t$ is a variable which denotes multiple values of $x$ & $y$ so we leave it as it is.

# Euler's Theorem
- if $a$ & $n$ are co-primes then:
$$
a^{\phi(n)}\equiv 1\text{ mod }n
$$
where:
- $\phi(n)=\text{Euler's totient function} \longrightarrow\text{no. of comprime numbers with }n\text{ which are}\leq n$
	- e.g. $\phi(9)=\bold 5 \rightarrow \{2,4,5,7,8\}$

# Fermat's Little Theorem
If $p$ is a prime number & $\text{gcd}(a,p) =1$:
<font color=red>incomplete</font>

# Wilson's Theorem
If $p$ is a prime, then $(p-1)!\equiv -1 \text{ mod } p$

# Polynomial Congruence
Let $f(x)$ be a polynomal of degree $r\geq1$ with integer coefficients and $m\geq2$ be a natural number.
Then the congruence of the form of $f(x)\equiv0\text{ mod } m$ is called polynomial congruence
when $r=1$ then the polynomial conguence 
<font color=red> incomplete</font>

# Hensel's Lemma
let $f(x) be a polynomial with integer coeffecients & degree $\geq1$. Let $p$ be a prime and $n\geq1$ be a natural number.
let $y$ be the solution of the polynomial congruence:
$$
f(x)\equiv 0 \text{ mod } p^{n=1}\tag1
$$
and, $y\equiv x_1+tp^n\text{ mod }p^{n+1}$
where, $0\leq x_1\leq p^n$ and $x_1$ is the solution of:
$$
f(x)\equiv 0 \text{ mod } p^n\tag2
$$
that $0\leq t\leq p-1$ and $t$ satisfies the congruence:
$$
t\times f'(x_1) = \frac{-f(x_1)}{p^n}\text{ mod }p\tag3
$$

then, $m\longrightarrow$ Number of values corresponding to an '$n$':
$$
m=\begin{cases}1,\quad p\not|\ f'(x_1)\\0,\quad p\ |\ f'(x_1) \ \ \  \&\ \ \ p^{n+1}\not | \ f(x_1) \\ p,\quad p\ |\ f'(x_1) \ \ \ \&\ \ \ p^{n+1}\ | \ f(x_1) \end{cases}
$$

## Working Procedure:
1. Given, A polynomial congruence:
$$
f(x)\equiv 0\text{ mod }m
$$
where, $m=p^{n+1}$, ( $p$ is prime and $n\geq1$ )

2. Rewriting:
$$
f(x)\equiv 0\text{ mod }p^{n+1}
$$

3. <font color=red>By trial and error, find $x,\ t$ for any n starting from $n=1$ to $n$</font>
4. Check possible no. of values of $n$
5. Find $t$'s which satisfies the equation in above lemma:
$$
t.f(x_1)\equiv\frac{-f(x_i)}{p^n}\text{ mod }p
$$
6. Put values in:
$$
y=(x_1+t,p^n)\text{ mod }p^{n+1}\quad(x\in [0,\ p^{n+1}])
$$
**Note:** If getting $x_i$ as no solution, discard that value and use trial and error to find new $x_i$

# RSA Algorithm
- In 1978 By:
	- Ran <u>R</u>ivert
	- Adi <u>S</u>hamir
	- Leonard <u>A</u>delman
- Only applciable for coprime ($\text{gcd}=1$)
- Assymetric Cryptographic Algorithm
- 2 Keys:
	- Public: known to all
	- Private: known to sender and reciever
- If a person A uses a public key for encrypting, we must use the same person A's private key for decrypting.
- The RSA is a block cipher in which the plain text and cipher text are integer between $0$ to $n-1$ for some value $n$

## Key Generation
1) Select 2 large prime numbers, $p$ & $q$
2) Calculate $n=p*q$
3) Calculate $\phi(n)=(p-1)\times(q-1)$
4) Choose value '$e$', $1<e<\phi(n)$ & $\text{gcd}(e,\ \phi(n))=1$
5) Calculate $d\equiv e^{-1}\text{ mod } \phi(n)$
	- $\therefore ed\equiv 1\text{ mod } \phi(n)$
6. Find:
	- Public Key = $\{e, \ n\}$
	- Private Key = $\{d, \ n\}$
7. Encryption:
	- $c=m^e\text{ mod }n$ (plain text, $m<n$) 
8. Decryption:
	- $m=c^d\text{ mod }n$

# If $n|(a+b)$ and $n|a$, Then: $n|b$
### Proof:
Let, $a+b = u . n$
and, $a=v.n$
Then, $b=(u-v).n$

# The List of Primes is Infinite - Euclid
### Proof:
Let us assume it is finite, then there will exist a number which is the **largest prime** say, $p_k$
Let the list of primes be $\{p_1, p_2,\dots, p_k\}$

Now we construct a new number which is 1 added to the product of these primes:
$n = (p_1\times p_2 \times p_3\dots p_k)+1$

This newly formed number $n$ is greater than all the primes and is composite as the largest prime is $p_k$

This implies $n$ has at least one prime factor, $p_j$

So, $\quad p_j|n \implies p_j|(p_1\times p_2 \times p_3\dots p_k)+1$
Also, $\quad p_j|(p_1\times p_2 \times p_3\dots p_k)$
$\therefore p_j|1$ from **1.1**
This however, is not possible therefore $n$ must also be prime which is clearly greater $p_k$

Therefore by condradiction, there is no largest prime which implies the list of primes is **infinite**

# $\pi(x)\text{ function}$
$\pi(x)$ denotes the number of primes smaller than $x$
e.g. $\pi(10) = 4 \qquad[2,3,5,7]$

- The Prime Number Theorem states that:
$$
\pi(x) \approx \frac{x}{log(x)} \qquad \text{(for large values of }x)
$$