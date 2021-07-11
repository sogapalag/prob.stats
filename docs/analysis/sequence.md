## Limit
### Definition
$(a_n)$ has limit $L\in \mathbb{{R}}$:

$\forall \varepsilon>0, \exists N>0$ s.t. if $n\geq N$, then $|a_n - L| < \varepsilon$.

### Theorem
$(a_n)$ has limit $L$, then any subsequence $(a_{f(n)})$ has same limit $L$.
??? "Proof"
    $f(n)\geq f(N) \geq N.\square$

## Algebra
Let
$$
\lim_{n\rightarrow\infty}a_n=L,\lim_{n\rightarrow\infty}b_n=M 
$$
that
\begin{align}
  \lim_{n\rightarrow\infty} (a_n + b_n) &= L + M \\\\
  \lim_{n\rightarrow\infty} ca_n &= cL \\\\
  \lim_{n\rightarrow\infty} (a_n - b_n) &= L - M \\\\
  \lim_{n\rightarrow\infty} a_n  b_n &= L M \\\\
  M \neq 0 \Rightarrow \lim_{n\rightarrow\infty} a_n / b_n &= L / M \\\\
\end{align}

## Bounded
### Definition
$\forall n, a_n \leq M$.

### Theorem
  - convergent $\Rightarrow$ bounded.
  - monotone, then convergent $\Leftrightarrow$ bounded.

### Theorem
$(a_n)$ is bounded, and $(b_n)$ limits 0, then $(a_nb_n)$ limits 0.
??? "Proof"
    $|b_n| < \varepsilon / M.\square$

## Squeeze
### Theorem
$\forall n, a_n\leq b_n\leq c_n$. If $(a_n),(c_n)$ limits $L$, then $(b_n)$ limits $L$.

### Definition
diverge to infinity:

$\forall M, \exists N > 0$, s.t. if $n\geq N$ then $a_n>M$.

### Theorem
$\forall n, a_n\leq b_n$, if $(a_n)$ diverge to $\infty$, then $(b_n)$ diverge to $\infty$.

## Real Exponents
$a^x = \lim a^{r_n}$ is well defined.

## Bolzano–Weierstrass theorem
bounded $\Rightarrow \exists$ convergent subsequence.
??? "Proof"
    bounded, i.e. $a_n \in [l,r]$,
    take $a_{n_1}$ from which.
    
    Note one of $[l,\frac{l+r}{2}]$ and $[\frac{l+r}{2},r]$ has $a_n$ infinitely many times. Thus we can take $n_2>n_1$ from which, keep this procedure.

    $(l_n), (r_n)$ both monotone thus convergent, and $(r_n-l_n)$ limits 0.
    By sequeeze, $(a_{n_i})$ converge.$\square$

## Cauchy Condition
$\forall \varepsilon>0, \exists N>0$ s.t. if $m,n\geq N$, then $|a_m-a_n|<\varepsilon$.

### Theorem
convergent $\Leftrightarrow$ Cauchy.
??? "Proof"
    $\Rightarrow$.
    
    take radius $\varepsilon/2$ of limit, thus $|a_m-a_n|<\varepsilon$.

    $\Leftarrow$.

    let $\varepsilon=1$, thus $(a_n)$ is bounded by $\max{|a_1|,\cdots, |a_{N-1}|, 1+|a_{N}|}$. By [B-W](#bolzanoweierstrass-theorem), $(a_{n_i})$ converge to some $L$.

    Then take $(N,\varepsilon/2)$ of Cauchy, and $(N_2,\varepsilon/2)$ of convergent $(a_{n_i})$.

    Choose $K\geq N_2$ and $n_K \geq N$, thus if $n\geq N$

    $$
        |a_n-L| \leq |a_n - a_{n_K}| + |a_{n_K} - L| < \varepsilon/2 + \varepsilon/2 = \varepsilon
    $$ $\square$

## lim sup
### Definition
$\limsup a_n=$

  - $\lim_{n\rightarrow\infty} \sup_{m\geq n} a_m$
  - $\inf_{n\geq 1} \sup_{m\geq n} a_m$
  - $\sup E$, where $E$ is set of limit points of convergent subsequence of $(a_n)$.

> Limit of "tail boarder".

### Theorem
$(a_n),(b_n)$ are bounded, then
$$
\liminf a_n + \liminf b_n \leq \liminf(a_n+b_n), \limsup(a_n+b_n) \leq \limsup a_n + \limsup b_n
$$
??? "Proof"
    Note $\forall n > 0$
    $$
    \inf_{m\geq n} a_m \leq a_k \leq \sup_{m\geq n} a_m, \forall k\geq n
    $$
    thus
    $$
    \inf_{\geq n} a + \inf_{\geq n} b \leq a_k + b_k \leq \sup_{\geq n} a + \sup_{\geq n} b, \forall k\geq n
    $$
    take $\inf$ or $\sup$ on middle to get
    \begin{align}
    \inf_{\geq n} a + \inf_{\geq n} b \leq \inf_{\geq n} (a+b) \\\\
    \sup_{\geq n} (a+b) \leq \sup_{\geq n} a + \sup_{\geq n} b
    \end{align}
    as $n\rightarrow\infty.\square$

> For any tail, each point under "tail boarder", thus sum of two still under.