## Description
Initially contain $r$ red balls and $b$ blue balls, after $k$-th observation, add $c_k$ balls of same color into the urn. Let $M_n=R_n/N_n$ be fraction of reds. Thus

$$
  E[R_{n+1}|\mathcal{F}_n^M] = R_n + c_n M_n = N_{n+1}M_n \\\\
  \Rightarrow E[M_{n+1}|\mathcal{F}_n^M] = M_n
$$

i.e. $M_n$ is uniformly bounded MG, which converges a.s. and $L^p$, by DCT and Doob's $L^p$.

## add constant
Only information we care is number of time observated reds in $n$ turns, denoted as $X_n$, thus

$$
  P(X_n = k) = \dbinom{n}{k} \dfrac{ r^{(c,k)} b^{(c,n-k)}}{(r+b)^{(c,n)}}
$$

where $x^{(c,k)} = \prod_{i=0}^{k-1} (x+ci)$. Let $\alpha=r/c,\beta=b/c,p=r/(r+b)$, use [rising factorial](https://en.wikipedia.org/wiki/Falling_and_rising_factorials) we can rewrite case $c>0$, that

$$
  P(X_n = k) = \dbinom{n}{k} \dfrac{ \alpha^{\overline{k}} \beta^{\overline{n-k}}}{(\alpha + \beta)^{\overline{n}}}
$$

### $c = 0$

$$ X_n\sim \text{Bin}(n,p) $$

### $c = -1$

$$ X_n\sim \text{Hypergeometric}(r+b, r, n) $$

### $c \geq 1$

$$X_n\sim \text{Beta-binomial}(n,\alpha,\beta)$$

#### Proof
\begin{align}
  \dfrac{ \alpha^{\overline{k}} \beta^{\overline{n-k}}}{(\alpha + \beta)^{\overline{n}}} &= \dfrac{\Gamma(\alpha+k)/\Gamma(\alpha) \cdot \Gamma(\beta+n-k)/\Gamma(\beta)}{\Gamma(\alpha+\beta+n)/\Gamma(\alpha+\beta)} \\\\
  &= \dfrac{B(k+\alpha,n-k+\beta)}{B(\alpha,\beta)}
\end{align}

$\square$

## limit
$$
  M_\infty \sim \text{Beta}(\alpha,\beta)
$$

### proof
\begin{align}
  P(X_n=k) &= \dfrac{\Gamma(n+1)}{\Gamma(k+1)\Gamma(n-k+1)}\dfrac{B(k+\alpha,n-k+\beta)}{B(\alpha,\beta)} \\\\
  &= \dfrac{1}{B(\alpha,\beta)} \dfrac{k^{(\alpha-1)} (n-k)^{(\beta-1)}}{n^{(\alpha+\beta-1)}}
\end{align}

note $k^{(a)}\rightarrow k^a$ as $k\rightarrow\infty$, thus

$$
  dP = \dfrac{1}{B(\alpha,\beta)} x^{\alpha-1}(1-x)^{\beta-1}dx
$$

$\square$

### uniform
In particular, $\alpha=\beta=1$, then $M_\infty\sim U(0,1]$. Recall Doob's maximal inequality, that

$$
  P(\sup M_n \geq 3/4) \leq 2/3
$$


# Bernard Friedman’s urn
Add additional $d_k$ balls of opposite color. If $c_k,d_k$ uniformly bounded, $r+b>0$, then

$$
  M_n \xrightarrow{a.s.}\dfrac{1}{2}
$$