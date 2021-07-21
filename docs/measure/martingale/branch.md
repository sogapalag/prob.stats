## Description
> A reproduction model, random tree, Galton-Watson process.

$$
  Z_{n+1} = \sum_{i=1}^{Z_n} X_{n,i}
$$

with $Z_0=1$, $X_{n,i}$ are i.i.d. $\mathbb{N}$ R.V.s to $n,i$, i.e. to generation and each.

### extinction
$$
  \{ \omega: Z_n(\omega)=0, ev. \}
$$

### mgf
$$
  L(s) = E[s^X]
$$

### MG
$\mu^{-n}Z_n$ is MG, $\rho^{Z_n}$ is MG for $\rho=L(\rho)$.

## Proposition. Extinction
For nontrivial, i.e. $P(X=0)\in(0,1)$. If $\mu \leq 1$, then $p_{ex}=1$. If $\mu > 1$, then $p_{ex} = \rho$, $\mu^{-n}Z_n\xrightarrow{a.s.}$, and that

$$
  Z_n\xrightarrow{a.s.}\{0,\infty\}
$$

## More about product MG
### Kakutani’s Theorem