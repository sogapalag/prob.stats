## [Convergence in distribution](https://en.wikipedia.org/wiki/Convergence_of_random_variables#Convergence_in_distribution)
$$
\lim F_n(x)=F(x),\forall x
$$

## CLT
i.i.d. $\sigma^2<\infty$, then
$$
\dfrac{\sum^nX_n - n\mu}{\sqrt{n\sigma^2}}\xrightarrow{d}\mathcal{N}(0,1)=G \\\\
\sqrt{n}(\overline{X}_n-\mu) \xrightarrow{d}\mathcal{N}(0,\sigma^2)
$$

## Lindeberg CLT

> moment be restricted.

P-m.indep. $\mu_n=0,s_n^2=\sum\sigma^2\rightarrow1$, if $\forall \varepsilon>0$, $s_n^{-2} \sum^nE[X_i^2I_{|X_i|>\varepsilon}]\rightarrow 0$, then

$$
\dfrac{\sum^nX_n}{s_n},\sum^nX_n\xrightarrow{d}G
$$

### Lyapunov CLT
P-m.indep. $\mu_n=0,s_n^2=\sum\sigma^2\rightarrow1$, if $\exists\delta>0$, $s_n^{-2-\delta}\sum^nE[|X_i|^{2+\delta}]\rightarrow0$, then

$$
\dfrac{\sum^nX_n}{s_n},\sum^nX_n\xrightarrow{d}G
$$