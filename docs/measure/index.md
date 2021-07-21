## Textbooks

  - Amir Dembo's notes.

### Cheat sheets

  - [classic](https://static1.squarespace.com/static/54bf3241e4b0f0d81bf7ff36/t/55e9494fe4b011aed10e48e5/1441352015658/probability_cheatsheet.pdf)

## Notations
### space
sample space: $\Omega$

power set: $2^\Omega$

event space, or $\sigma$-algebra: $\mathcal{F}\subseteq 2^\Omega$

measure: $\mu$
  - Lebesgue: $\lambda$

coutable union: $\bigcup_i$

possibly uncountable unoin: $\bigcup, \bigcup_\alpha$

measureable space: $(\Omega,\mathcal{F})$

measure space: $(\Omega,\mathcal{F},\mu)$

probability space: $(\Omega,\mathcal{F},P)$

### limit
$A_i\uparrow A: A_1\subseteq A_2\subseteq\cdots,\bigcup_i A_i=A$.

$A_i\downarrow A: A_1\supseteq A_2\supseteq\cdots,\bigcap_i A_i=A$.

### generated $\sigma$
By algebra: $\sigma(\mathcal{A})$

By R.V.: $\mathcal{F}^X = \sigma(X)$

By R.V.s: $\mathcal{F}_n^X = \sigma (X_1,\cdots,X_n)$

Tail of stochastic process $\{X_k\}$:

  - $\mathcal{T}_n^X = \sigma (X_t, t>n)$
  - $\mathcal{T}^X = \bigcap_n \mathcal{T}_n^X$

### abbr
SF: simple function
  
  - $\sum_i^n c_i I_i$

R.V.: random variable.

a.s.: almost sure

a.e.: almost everywhere

w.p.1: with probability 1

m.zero: measure zero

m.indep.: mutually independent

S.P.: stochastic process

i.i.d.: independent and identically distributed

LLD: law of large numbers

CLT: central limit theorem

i.o.: infinitely often

ev.: eventually

### limsup

$$
  \limsup A_n = \inf_{n\geq 1} \sup_{i\geq n} A_i = \bigcap_n\bigcup_{i\geq n} A_i = \{A_n\ i.o.\}  \\\\
  \liminf A_n = \sup_{n\geq 1} \inf_{i\geq n} A_i = \bigcup_n\bigcap_{i\geq n} A_i = \{A_n\ ev.\}  \\\\
$$

> occur infinitely, or occur all after some large n.

### Models
RW: random walk

SRW: simple random walk

sym-SRM: symmetric SRM