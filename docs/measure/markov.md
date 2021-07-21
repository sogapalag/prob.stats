## Markov property
$$
  P(X_{n+1}\in A|F_n) = P(X_{n+1}\in A|X_n), \forall n, a.s.
$$

> i.e. memoryless, only based on current state.

## Strong Markov property
Hold for $X_{\tau}$, $\tau<\infty$.


## Chapman-Kolmogorov
> transition, equal to *countable* convolution on some middle state.

## Definitions
### accessible
$\rho_{xy}:=P_x(T_y<\infty) > 0$. i.e. $x$ leads to $y$.

### intercommunicate
both accessible, $x\leftrightarrow y$.

### irreducible 
Any two intercommunicate.

### closed
Won't transition out.

### recurrent(persistent)
$\rho_{xx}=1$.

> equivalents, 6.2.12


### transient
$\rho_{xx} < 1$.

## Proposition 6.2.10
Let $T_y^k$ be k-th return, then

$$
  P_x(T_y^k < \infty) = \rho_{xy}\rho_{yy}^{k-1} \\\\
  E_x[N_{\infty}(y)] = \dfrac{\rho_{xy}}{1 - \rho_{yy}}
$$

## Decomposition theorem
$$
  S = T \cup R_1\cup R_2\cup \cdots
$$

> one transient, other ireducible.

## invariant measure
default for transition $p$.

$$
 \mu(y) = \sum_x \mu(x)p(x,y)
$$

### classic
$$
  \pi = \pi P
$$

### Proposition 6.2.41.
$\pi(z) = 1/E_z[T_z]$.


## Convergence Theorem 6.2.59

> Thermodynamics equilibrium.
