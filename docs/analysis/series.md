## Notation
$$
s_n = \sum_{i=1}^n a_n \\\\
a\rightarrow L:\lim_{n\rightarrow\infty}a_n=L \\\\
a:\forall n, a_n
$$
i.e. comprehensive notation.

## Algebra
$+,-,cs$ hold.

## Convergence Tests
$$
s\rightarrow \Rightarrow a\rightarrow0 \\\\
a\geq 0: s\rightarrow \Leftrightarrow s \text{ bounded}
$$

### $2^n$ Cauchy condensation test
$$
a\geq 0, a\searrow: s\rightarrow \Leftrightarrow \sum 2^na_{2^n}\rightarrow
$$

### Alternating series test
$$
a\searrow, a\rightarrow 0 \Rightarrow \sum(-1)^na_n\rightarrow
$$

### Comparison test
If for sufficiently large $n$, $|a_n|\leq C|b_n|$
$$
\sum|b|\rightarrow \Rightarrow \sum|a|\rightarrow
$$

### Ratio test
$$
\left|\dfrac{a_n+1}{a_n}\right|\rightarrow L, \begin{cases}L<1\Rightarrow \sum|a|\rightarrow \\\\ 
L>1 \Rightarrow s \not\rightarrow \end{cases}
$$

### Root test
$$
L=\limsup |a_n|^{1/n}, \begin{cases}L<1\Rightarrow \sum|a|\rightarrow \\\\ 
L>1 \Rightarrow s \not\rightarrow \end{cases}
$$

## Binary
### Theorem
$$
\sum |a|\rightarrow, b \text{ bounded} \Rightarrow \sum |ab|\rightarrow \\\\
\sum |a|\not\rightarrow,1/b \text{ bounded} \Rightarrow \sum|ab| \not\rightarrow
$$

### Lemma
$$
\sum_{i=1}^n a_ib_i = s_nb_{n+1} + \sum_{i=1}^n s_i(b_i - b_{i+1})
$$

### Theorem
$$
\sum a \text{ bounded}, \sum|b_{n+1}-b_n|\rightarrow, b\rightarrow 0 \Rightarrow \sum ab\rightarrow
$$

### Dirichlet test
$$
\sum a \text{ bounded}, b\searrow,b\rightarrow 0 \Rightarrow \sum ab\rightarrow
$$

### Theorem
$$
\sum a\rightarrow, \sum |b_n - b_{n+1}|\rightarrow \Rightarrow \sum ab\rightarrow
$$

### Abel test
$$
\sum a\rightarrow, b\text{ bounded monotone} \Rightarrow \sum ab\rightarrow
$$

## Power series
let $L = \limsup |a_n|^{1/n}$, the radius of $\sum a_n(x-t)^n$ is $1/L$.

## Double series
### Definition
sum by rows exist: $\sum_n a_{m,n}\rightarrow$ and $\sum_m(\sum_n a_{m,n})\rightarrow$.

### Lemma
$a\geq 0$: sum by row exist $\Leftrightarrow$ sum by column exist, and equal.

### Theorem
$$
\sum_{m,n}|a|\rightarrow \Rightarrow \sum_m\sum_na=\sum_n\sum_ma\rightarrow, \sum_m|\sum_n a|\rightarrow, \sum_n|\sum_m a|\rightarrow
$$

### Permutation
$$
\sum_n |a_n|\rightarrow \Rightarrow \sum_{p(n)}|a_n|\rightarrow, \sum_{p(n)}a=\sum_n a
$$

### Cauchy product
$$
\sum|a|\rightarrow, \sum|b|\rightarrow \Rightarrow \sum |c|\rightarrow, \sum c=\sum a \sum b
$$