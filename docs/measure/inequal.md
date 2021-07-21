
## Markov

### classic
For $X\geq 0, a>0$

$$
  P(X\geq a) \leq \dfrac{EX}{a}
$$

> value, bounded by expectation

### measure
[Wiki](https://en.wikipedia.org/wiki/Markov%27s_inequality) for meaure and extended.

## Chebyshev

### classic
For $X\in L^2, a>0$

$$
  P(|X-EX|\geq a^2) \leq \dfrac{\text{Var}(X)}{a^2}
$$

> bias, bounded by variance

## Jensen
For convex $f$

$$
  f(ax+(1-a)y) \leq af(x)+(1-a)f(y)
$$

### classic
$$
  f(EX) \leq Ef(X)
$$

## Hölder
$p,q \geq 1$, $\frac{1}{p} +\frac{1}{q}=1$

$$
  E|XY|=\|XY\|_1\leq \|X\|_p \|Y\|_q
$$

> $(p,q)$ called Hölder conjugates. $(2,2)$ imply Cauchy–Schwarz.

## Minkowski
$X,Y\in L^p,p\geq 1$

$$
  \|X+Y\|_p \leq \|X\|_p + \|Y\|_p
$$

> triangle in $L^p$

## Kolmogorov's maximal
P-m.indep. $X_n=0,EX_n^2<\infty,a>0$, then

$$
  P(\max_{1\leq k\leq n}|S_k|\geq a) \leq a^{-2}\text{Var}(S_n)=a^{-2}\sum^n EX_i^2
$$

> max of abs partial sum, bounded by variance

## Doob's martingale
sub-MG, $a>0$,
$$
  P(\max_{0\leq k\leq n}X_k \geq a) \leq a^{-1}E[(X_n)_+]
$$

> max of past, bounded by latest positived expectation. Generalized Kolmogorov's maximal.

### $L^p$ maximal
$p>1$,

$$
  \|\max_{k\leq n}X_k\|_p \leq \dfrac{p}{p-1}\|X_n\|_p \\\\
  E[\max_{k\leq n}X_k] \leq \dfrac{e}{e-1}(1 + E[X_n(\log X_n)_+])
$$

## Doob's up-crossing
sup-MG, $a<b$

$$
  (b-a)E[U_n[a,b]] \leq E(X_n-a)_- - E(X_0-a)_-
$$

> up-crossing of losing S.P., bounded by latest.

### Dubins' up-crossing
sup-MG $X_n\geq 0$, $0<a<b$,

$$
  P(U_\infty\geq l)\leq \left(\dfrac{a}{b}\right)^l E[\min(X_0/a, 1)]
$$

> total up-crossing of losing S.P., bounded by $X_0/a, a/b$.