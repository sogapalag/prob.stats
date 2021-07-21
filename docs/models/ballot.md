## Description
### classic
Given total voted $a\leq b$, let $n=a+b, s=b-a$, the probability B leads A through whole counting is

$$
  P(A<B, \forall i\in[n]) = \dfrac{s}{n}
$$

### catalan
Interpret voting B/A as moving right/up one step in lattice, then event is corresponding to not hit diagonal. *(catalan is allowed tie)*

### SRW
Interpret voting B/A as $+1$/$-1$, let $z=\inf\{t>0:S_t=0\}$, then probability denoted as

$$
  P(z>n|S_n=s)
$$

## Proofs
### classic reflection
The bad votings can be separated to $\xi_1=1$ or $-1$, which two groups are bijection, by fliping $\xi_i$ for $i\leq z$. And note all start with $-1$ are bad, regarding to likelihood of $p_A=a/n$, we get the answer

$$
  P = 1-2p_A=\dfrac{s}{n}
$$

$\square$

### SRW
Let $\tau_s:=\inf\{t\geq 0: S_t=s\}$, by central rotation to path, we get another bijection which imply

$$
  P(\tau_s = n | S_n=s) = P(z>n | S_n=s)
$$

Note $\{X_n = n^{-1}S_n\}$ is RMG, let $\theta = \sup\{2\leq t\leq n: S_t=0\} \vee 1$, which is valid stopping time in RMG, notice that

$$
  X_\theta = \begin{cases} 0, \theta > 1 \\\\ 1,\theta=1\end{cases}
$$

thus $E[X_\theta|F_n]=P(\theta=1|F_n)$, and $\{\theta = 1\}$ is indeed same event above. Recall Doob's OST,

$$
  P = E[X_\theta|F_n] = X_n = \dfrac{s}{n}
$$

*Remark. $\theta$ is indeed rotation of $\tau_s$, in this problem, $\inf,\sup$ does not affect bijection, we choose which is measurable for MG fitraction requirement.*

$\square$

### Collorary
This give us explict formula of hitting probability in Gambler's ruin, for $k\geq 0$

$$
  P(\tau_b = b+2k) = \dfrac{b}{b+2k} P(S_n=b) = \dfrac{b}{b+2k} \dbinom{b+2k}{k} p^{k+b} q^{k}
$$
