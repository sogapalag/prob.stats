This page is about discrete time martingale.

## filtration
$\mathcal{F}_n\uparrow \mathcal{F}=\sigma(\bigcup_iF_i)$

## adapted
A S.P. $\{X_n\}$ is adpated to a filtration, denoted as $\mathcal{F}_n$-adapted, if $\sigma(X_n)\subseteq \mathcal{F}_n, \forall n$.

  - iff $\sigma(X_0,X_1,\cdots,X_n)\subseteq\mathcal{F}_n$

## canonical(minimal) filtration
$$
\mathcal{F}_n^X = \sigma(X_0,X_1,\cdots,X_n)
$$
Implicitly w.r.t.

## martingale(MG)
$E|X_n|<\infty$,
$$
E[X_{n+1}|\mathcal{F}_n]=X_n, \forall n, a.s.
$$

### difference characterization
let $D_n=X_n-X_{n-1}$, i.e. $X_n=\sum^n D_i$,
$$
E[D_{n+1}|\mathcal{F}_n]=0, \forall n, a.s.
$$

> Knowing past information, zero profit, i.e. fair game.

### product MG
indep. $Y_n\geq 0$. $M_n=\prod^nY_i$,

$$
  E[M_{n+1}|\mathcal{F}_n^Y]=M_nE[Y_{n+1}]=M_n \Leftrightarrow E[Y_n]=1,\forall n
$$

or general condition $E[Y_{n+1}|\mathcal{F}_n^Y]=1$ a.s.

### sub-MG
$$
E[X_{n+1}|\mathcal{F}_n]\geq X_n, \forall n, a.s.
$$

Implicitly used for sub-MG, sup-MG or MG.

### strong MG
MG iff

$$
  E[X_n|\mathcal{F}_\tau]=X_\tau, \forall\tau\leq n,\forall n
$$

### local MG

## stopping time
A R.V. $\tau$ values $\mathbb{N}\cup\infty$ for filtration $\{\mathcal{F}_n\}$, if

$$
  \{\omega:\tau(\omega)\leq n\}\in\mathcal{F}_n,\forall n
$$

### stopped at
$$
  X_{n\wedge\tau}(\omega) = \begin{cases}X_n(\omega), n\leq\tau(\omega) \\\\ X_{\tau(\omega)}(\omega), n>\tau(\omega)\end{cases}
$$

### stopped $\sigma$-algebra
$$
\mathcal{F}_\tau:=\{A\in\mathcal{F}:A\cap\{\omega:\tau(\omega)\leq n\}\in\mathcal{F}_n,\forall n\}
$$

## pridictable
$$
V_n\in m\mathcal{F}_{n-1},\forall n
$$

### MG transform
$$
Y_n = \sum^n V_i(X_i-X_{i-1})
$$

## up-crossings
number of up-crossings $U_n[a,b]$, largest $l, (s_i,t_i)_l$ s.t. $X_s<a<b<X_t, s_1<t_1<s_2<\cdots$