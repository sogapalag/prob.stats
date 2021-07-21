## Lemma
Each $a<b$, $U_\infty[a,b]<\infty$ a.s., then $X_n\xrightarrow{a.s.}X$.

> $b-a\rightarrow0$, $U_\infty$ finite, roughly imply $\liminf=\limsup$ w.p.1.

## Theorem. DCT
sup-MG, $\sup_n E(X_n)_-<\infty$, then $X_n\xrightarrow{a.s.}X$.

> intuitively, the losing part is bounded, thus down-crossing is finite.

for sub-MG, some equivalent conditions:

  - $\sup_n E(X_n)_+ < \infty$.
  - $\sup_n E|X_n| < \infty$.
  - $\lim_n E|X_n|<\infty$.
  - $\lim_n E(X_n)_+ < \infty$.
  - $\liminf_n E|X_n| < \infty$.

## Corollary. Inequality
U.I. sub-MG, $a>0$,

$$
  P(X_k\geq a,\exists k<\infty) \leq a^{-1} E(X_\infty)_+
$$

## Proposition.
MG, $\sup_n|X_n-X_{n-1}|\leq c$, a.s. then $P(A\cup B)=1$ with

$$
  A = \{\omega: \lim X_n(\omega)<\infty \} \\\\
  B = \{\omega: \liminf X_n(\omega)=-\infty, \limsup X_n(\omega)=\infty\}
$$

> either can walk everywhere or convergence.

## more applications 5.3.x
### lemma
DCT condition, then $E|X_\tau|<\infty,\forall\tau$.
### Proposition
sup-MG $\geq 0, \theta\leq \tau$, then $EX_\theta \leq EX_\tau<\infty$.

### Lévy's 0-1 law
$\mathcal{F}_n\uparrow \mathcal{F}, A\in \mathcal{F}$, then $E[I_A|\mathcal{F}_n]\xrightarrow{a.s.}I_A$.

> gradually with more information, we will be certain about the outcome. Thus $P(A)=I_A$ a.s. deducing Kolmogorov's 0-1 law.

### Doob's $L^p$ martingale convergence
MG, $\sup_n E|X_n|^p < \infty, p>1$, then $X_n\rightarrow X$ a.s. and $L_p$ (So $\|X_n\|_p\rightarrow\|X\|_p$).