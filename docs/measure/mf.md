
## Definition
Mapping between two measurable spaces $(\Omega, \mathcal{F}), (\mathbb{S},\mathcal{S})$, also called measurable mapping, Borel function $f$, random variable(R.V.) $X$, if $\forall B\in \mathcal{S}$

$$
  X^{-1}(B):= \{A:X(A)\in B\} \in\mathcal{F}
$$

> i.e. contain preimage.

## Convergence

### Theorem
$$
 \rightarrow\overline{\mathbb{R}}, f_n\in mF \Rightarrow \sup_n f_n,\inf_n f_n, \limsup_{n\rightarrow\infty}f_n,\liminf f_n \in mF
$$

### Theorem
For any sequence $f_n$

$$
  \Omega_0:=\{ \omega:\liminf f = \limsup f \} \\\\
  \Omega_1:=\{ \omega:\liminf f = \limsup f \in \mathbb{R}\}
$$

are measurable, i.e. $\Omega_0,\Omega_1 \in F$.

> set converge to $\infty$ or finite limit.

### Type of convergence

  - pointwise convergence: $f_n(\omega)\rightarrow f(\omega)$.
  - a.s. convergence: $f_n \xrightarrow{a.s.}f$, $P(\Omega_0)$ w.p.1.
    - $P(X_n\rightarrow X)=1$
    - a.s. convergence to finite limit: $P(\Omega_1)$ w.p.1.
  - convergence in probability: $f_n \xrightarrow{p}f$
    - $\forall \varepsilon>0$, $P(x:|f_n(x)-f(x)|>\varepsilon)\rightarrow 0$.
  - convergence in $L^p$: $f_n\xrightarrow{L^p}f$
    - $f_n,f\in L^p$, $\|f_n-f\|_p\rightarrow 0$.

> (a.e.) pointwise is strong;
> a.s. means eventually, $P(\lim)$; in probability, $\lim(P)$.

#### Relationship
\begin{align}
\xrightarrow{a.s.} &\Rightarrow \xrightarrow{p} \\\\
\xrightarrow{L^p},p\geq r &\Rightarrow \xrightarrow{L^r} \\\\
\xrightarrow{L^p} &\Rightarrow \xrightarrow{p}
\end{align}

More properties on [wiki](https://en.wikipedia.org/wiki/Convergence_of_random_variables#Properties_4).

### Monotone convergence theorem
$f_n\geq 0$ pointwise converge, then $\mu(f_n)\uparrow \mu(f)\leq \infty$.

#### general
$f_n\geq 0$, $f_n\uparrow f$ a.e., then $Ef_n\uparrow Ef$.

### Fatou's lemma
> bridge $\limsup,\liminf$ on a.s. measure sense.

### Dominated convergence theorem

### Scheffe's lemma

### U.I.

### Vitali's convergence theorem

### Standard machine
Steps to prove some property hold $h\in L^1$.

  1. prove indicator.
  2. by linearity, extent to $SF_+$
  3. by MON thm, extent to $mF_+$
  4. $h=h_+-h_-$, extent to $L^1$

## Definition
### distribution
$F:\mathbb{R}\rightarrow [0,1]$ is distribution of some R.V. iff
  
  1. $\nearrow$.
    - imply a.s. differentiable.
  2. $\lim_{x\rightarrow\infty} F(x)=1$ and $\lim_{x\rightarrow -\infty} F(x)= 0$
  3. right-continous: $\lim_{x\downarrow a}F(x)=F(a)$

### pdf
$$
 F_X(x)=\int_{-\infty}^xf_X(t)dt, \forall x\in \mathbb{R}
$$

### P-trivial
either $P(A)=0$ or $P(A^c)=0$.

### expectation
$$
 E[X]=\int XdP
$$

[Wiki](https://en.wikipedia.org/wiki/Lp_space#Lp_spaces_and_Lebesgue_integrals) of Lebesgue integral, $L^p$.

## Independence

  - classic: $P(A\cap B)=P(A)P(B)$.
  - $\sigma$-algebra.
  - R.V.s:$\sigma(X)$ indep. $\sigma(Y)$

### P-mutually independent
A collection of events $A_\alpha\subseteq\mathcal{F}$ is P-m.indep. if for any $L < \infty$ distinct indices

$$
  P(\bigcap^L A_i) = \prod^L P(A_i)
$$

  - R.V.s: generated Borel.

#### Theorem
*Finite* P-m.indep. $\pi$-system $\Rightarrow$ $\sigma (\pi_n)$ are P-m.indep.

##### Corollary
Above hold even for *uncountably infinite*.

> Since P-m.indep. condition only check finite $L$.

### Theorem
$\mathcal{F}_n^X$,$\sigma(X_{n+1})$ P-m.indep. $\forall n$ $\Rightarrow$ $X_1,X_2,\cdots$ P-m.indep. $\Rightarrow$ $\mathcal{F}_n^X$,$\mathcal{T}_n^X$ P-m.indep.

### Lemma
if $\sigma$-algebras $\mathcal{G}_n\uparrow \mathcal{G}$, each indep. with a $\sigma$-algebra $\mathcal{H}\subseteq \sigma(\mathcal{G})$, then $\mathcal{H}$ is P-trivial.

### Kolmogorov's 0-1 law
P-m.indep. S.P. $\{X_k\}$ $\Rightarrow$ $\mathcal{T}^X$ is P-trivial.

#### Proof
$A\in T^X\subseteq T_n^X$ imply $T^X$, $F_n^X$ indep. Then by above lemma proved.$\square$

## Product

Kolmogorov's extension theorem

> unique consistent probability measure.

Fubini theorem

> ensure integral by parts