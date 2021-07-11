## Notation
If not specific, default on metric space $(M,d)$, $f:M\rightarrow \mathbb{R}$.

closed: $X$ contain all limit points $\overline{X}$

  - $\Leftrightarrow X=\overline{X}$

> e.g. $\{x\}, M, \varnothing$ are closed.

Open ball $B_\varepsilon(a):\{x\in M:d(x,a)<\varepsilon\}$

open: $\forall x\in X$, $\exists B(x)\subseteq X$

> e.g. $M, \varnothing$ are open.

### Definition
A metric $d:M\times M\rightarrow [0,\infty)$ should satisfy

  1. $d(x,y)=0 \Leftrightarrow x=y$
  2. $d(x,y)=d(y,x), \forall y\in M$
  3. $d(x,y) \leq d(x,z) + d(y,z), \forall z\in M$

e.g. $(\mathbb{R}^n,d)$ is metric space, with $d(x,y)=\sqrt{\sum(x-y)^2}$

### Cauchy–Schwarz inequality
$|\langle u,v\rangle| \leq \|u\| \|v\|$, equality iff $u,v$ linearly dependent.

## $\ell^p$ space
set of series $a$ s.t. $(\sum |a|^p)^{1/p}$ converge.

### Theorem
$$
 a,b\in l^2 \Rightarrow \sum|ab|\rightarrow
$$

### Corollary
$$
a,b \in l^2 \Rightarrow \sum(a-b)^2\rightarrow \Rightarrow \text{metric}
$$

## Limit, convergence
### Definition
$\forall \varepsilon>0,\exists N>0$ s.t. if $n\geq N$ then $d(a_n, L) < \varepsilon$.

### Theorem
For $R^n$, $a\rightarrow a \Leftrightarrow a_k\rightarrow a_k,\forall k\in[n]$.

> i.e. equivalent to dimension-wise convergence.
> For $l^1,l^2,l^\infty,c_0$, only hold $\Rightarrow$. 

## Closed and open
### Theorem
$X$ open $\Leftrightarrow$ $X^c$ closed.

### Theorem
$\bigcup$ of **finite** closeds is closed.

> $\bigcup [1/n,1-1/n] = (0,1)$

$\bigcap$ of closeds is closed. 

#### Proof
Note $x\in \overline{\bigcap \mathcal{C}}$, imply $x_n\in\bigcap \mathcal{C},\forall n$.

Thus $x_n\in T,\forall n,\forall T\in\mathcal{C}$, imply $x\in \overline{T},\forall T$.

Since $T$ closed, $x\in T$ imply $x\in \bigcap \mathcal{C}.\square$

### Theorem
$\bigcap$ of **finite** opens is open.

$\bigcup$ of opens is open.

## Continuity
### Theorem
$f$ continous on compact $X$ $\Rightarrow$ $f$ bounded on $X$.

### Theorem
$f$ continous on compact $X$ $\Rightarrow$ $\exists$ maximum, minimum on $X$.

### Uniformly continous
$\forall \varepsilon>0,\exists\delta>0$ s.t. if $d_1(x,y)<\delta$ then $d_2(f(x),f(y))<\varepsilon$.

> Cauchy

## Compactness
compactness property, that is, **any open** cover has **finite** subcover.

### Theorems
$M$ compact $\Leftrightarrow$ $\forall (a),\exists$ convergent subsequence.

$X$ is compact subset of $M$ $\Rightarrow$ $X$ closed and bounded.

$X$ is closed subset of compact $M$ $\Rightarrow$ $X$ compact.

### Heine–Borel theorem

For $\mathbb{R}^n$, $S$ is closed and bounded $\Leftrightarrow$ $S$ is compact

#### Proof
$\Rightarrow$.
Similar to [B-W](sequence.md#bolzanoweierstrass-theorem), assume not compact, split $[l,r]$ half, one of which is not compact, thus we have a infinite incompact $[l_n,r_n]$, by completeness axiom, $(x_n)$ is picked, which is Cauchy, let the limit be $L$.

Note $\exists U\in \mathcal{C}$ s.t. $L\in U$, thus $\exists B(L) \subseteq U$, then for sufficiently large n, $[l_n,r_n]\subseteq B(L) \subseteq U$, i.e. covered by single $U$, contracted to incompact assumption.$\square$


> i.e. Heine–Borel $\Leftrightarrow$ Bolzano–Weierstrass on $\mathbb{R}^n$.

### Theorem
$f:M_1\rightarrow M_2$ continous, compact $M_1$ $\Rightarrow$ $f(M_1)$ compact $\Rightarrow$ $f(M_1)$ closed and bounded.

### Theorem
$f:M_1\rightarrow M_2$ continous, compact $M_1$ $\Rightarrow$ $f$ uni. continous on $M_1$.

#### Corollary
$f:\mathbb{R^n}\rightarrow \mathbb{{R}}$ continous on closed and bounded $X$ $\Rightarrow$ $f$ uni. continous on $X$. 

## Completeness
metric $M$ called complete, if $\forall$ Cauchy imply convergence $x\in M$.

> $\mathbb{R}^n, l^1,l^2,l^\infty,c_0$ are complete.

### Theorem
convergence $x\in M$ $\Rightarrow$ Cauchy.

### Theorem
$\forall M, \exists$ completion, which is $\overline{M}$.

### Theorem
compact $\Rightarrow$ complete.

### Banach fixed-point theorem
Contracting mapping $f$ on complete metric $\Rightarrow$ $\exists$ unique $x=f(x)$.

??? "Proof"
    Let $x_{n+1}=f(x_n)$ with arbitrary $x_0$.

    It's easy to verify $(x_n)$ is Cauchy. By completeness $x\in M$.

    By provable continuity that
    $$
    f(x) = \lim f(x_n) = \lim x_n = x
    $$

    Then unique followed by contracting.$\square$ 