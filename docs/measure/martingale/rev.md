## RMG
$F_n\downarrow F_{-\infty}=\bigcap_{n\leq 0}F_n$. And results don't involve $n\rightarrow\infty$ hold.

## Lévy’s downward theorem
RMG iff $E[X_0|F_n]=X_n, \forall n\leq 0$. Furthermore,

$$
  E[X_0|F_n]\xrightarrow{a.s., L_1} E[X_0|F_{-\infty}]
$$

> upward tells that gradually gain information converge to R.V., downward tells that gradually loss information converge to R.V.

### A proof of strong LLN
Let $X_{-n} = n^{-1}\sum^n\xi_i$, then according to linearity and i.i.d. with permutation, get that

$$
  E[\xi_1| X_{-n}] = X_{-n}
$$

Thus RMG, which implies converge to $X_{-\infty}=E[\xi_1|F_{-\infty}]$, thus $E[X_{-\infty}]=E[\xi_1]$.

Note $X_{-\infty}$ remains even eliminate finite, i.e. $\forall k$

$$
  X_{-\infty} = \limsup_n n^{-1}\sum_{i=k}^n \xi_i
$$

Thus $X_{-\infty}\in mT$, recall Kolmogorov's 0-1 law, tail is trivial, that is $X_{-\infty}\xrightarrow{a.s.}\mu.\square$
