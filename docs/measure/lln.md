## $L^2$ Weak LLD
Uncorrelated $X_i$, $\text{Var}(X_i)<\infty, EX_i=\mu <\infty$, then $\overline{X}_n \xrightarrow{L^2} \mu$, hence

$$
  \overline{X}_n \xrightarrow{p} \mu
$$

### Proof
$$
 \text{Var}(\overline{X}_n)\leq \dfrac{\sum^n C}{n^2} = \dfrac{C}{n}\rightarrow 0
$$

### Coupon collector’s problem
$$ 
ET_n = n H_n, \dfrac{T_n}{n\log n}\xrightarrow{L^2} 1
$$

#### infinite coupons
let $D_n$ denote collected in first $n$.
$$
  D_n\xrightarrow{a.s.}\infty, n^{-1}D_n\xrightarrow{p}0
$$

### Occupacy problem
$r$ bolls to $n$ boxes, with $\dfrac{r}{n}\rightarrow\alpha\in[0,\infty]$, the emptyness

$$
  n^{-1}N_n\xrightarrow{L^2,p} e^{-\alpha}
$$

## Weak triangular

> For bounded on some slow $b_n$.

## Weak LLN
i.i.d., $xP(|X_1|>x)\rightarrow 0$, then

$$
  \overline{X}_n\xrightarrow{p}\mu_n=E[X_1I_{|X_1|\leq n}]
$$

### classic
i.i.d., $E|X_1|<\infty$, then

$$
  \overline{X}_n\xrightarrow{p}\mu
$$

## Borel-Cantelli
### I
$\sum_i P(A_i) < \infty$, then $P(A_n\ i.o.)=0$.

### II
P-m.indep. $\sum_iP(A_i)=\infty$, then $P(A_n\ i.o.)=1$.

### Collorary 0-1 law
P-m.indep., then $\{A_n\ i.o.\}$ is P-trivial.

## Strong LLN
pairwise-i.i.d., either $EX_+$ or $EX_-$ finite, then
$$
  \overline{X}_n \xrightarrow{a.s.} \mu
$$