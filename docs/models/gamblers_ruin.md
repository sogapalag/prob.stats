## Description
SRW $p,S_n=\sum\xi_i$. Fix $a,b\in \mathbb{N}^+$, the probability hit $-a$ before $b$, called ruin probability, which is

$$
  r = \begin{cases} \dfrac{e^{\lambda b} - 1}{e^{\lambda b} - e^{-\lambda a}}, \lambda = \log\dfrac{1-p}{p}\neq 0 \\\\
  \dfrac{b}{a+b}, p=\dfrac{1}{2}
  \end{cases}
$$

### Proof
Let stopping time

$$
  \tau_{a,b} = \inf\{n: S_n\leq -a, or\ S_n\geq b\}
$$

Which is a.s. finite, since $S_+=(S_n+n)/2 \sim \text{Binomial}(n,p)$, recall stirling approximation, each point probability tends to 0.

Then construct product MG that

$$
  M_n = \prod_i^n e^{\lambda \xi_i}
$$

Recall Doob's optional stopping theorem, that

$$
  r e^{-\lambda a} + (1-r)e^{\lambda b}=1
$$

For $p=1/2$, note $S_n$ is MG, that

$$
  r(-a) + (1-r)b = 0
$$

$\square$

## Properties
### expectation
Recall Wald's identities,

$$
  E\tau_{a,b} = \dfrac{ES_\tau}{E\xi} = \dfrac{b-r(a+b)}{2p-1}
$$

### drift up
let $\tau_b = \inf\{n:S_n\geq b\}$, that $\tau_{a,b}\uparrow \tau_b$ as $a\uparrow\infty$. If $p\geq 1/2$, then

$$
  E\tau_b = \dfrac{b}{2p-1}
$$

Since $ra\rightarrow 0$.


$\tau_b<\infty$ a.s.

#### Proof

$p>1/2$ is trivial since $E\tau_b<\infty$. When sym-SRW, recall reflection principle, 

$$
  P(\sup_n S_n\geq b)\rightarrow 1
$$

i.e.

$$
  P(\tau_b = \infty) = 0
$$

$\square$

### drift down

If $p<1/2$,

$$
  P(\tau_b < \infty) = e^{-\lambda b}
$$

#### Proof
Note $\tau_{a,b}$ a.s. finite, and $a\leq \tau_{-a}$, thus

$$
  P(\tau_b < a) \leq P(\tau_b < \tau_{-a})\leq P(\tau_b < \infty)
$$

which implies $P(\tau_b < \tau_{-a})\rightarrow P(\tau_b < \infty)$ as $a\rightarrow\infty$. Then

$$
  P(\tau_b < \infty) = 1-r|_{a\rightarrow\infty}= e^{-\lambda b}
$$

$\square$


Let $Z = 1+\max_{n\geq 0} S_n$, then

$$
  Z \sim \text{Geometric}(p=1-e^{-\lambda})
$$

#### Proof
Note $\{\tau_b<\infty\}$ iff $\{Z>b\}$, that

$$
  P(Z=b) = e^{-\lambda (b-1)} - e^{-\lambda b} = (1-p)^{(b-1)}p
$$

$\square$