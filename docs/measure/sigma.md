## Definition

### $\sigma$-algebra
$\mathcal{F}$ is $\sigma$-algebra if

  1. *closed under completement*: $A\in \mathcal{F}$ imply $\Omega/A = A^c \in \mathcal{F}$.
  2. $\Omega \in \mathcal{F}$.
    - assuming (1), equiv to $\varnothing\in\mathcal{F}$.
  3. closed unded **countable** union: $A_i\in\mathcal{F}$ imply $\bigcup_i A_i\in \mathcal{F}$.
    - assuming (1),(2), equiv to *closed under countable intersection* $\bigcap_i A_i\in\mathcal{F}$, by De Morgan's law.

### measure
$\mu:\mathcal{F}\rightarrow [0,\infty]$ is measure if

  1. $\mu(A)\geq \mu(\varnothing)=0, \forall A\in \mathcal{F}$
  2. **coutably** additive: $\mu(\bigcup_i A_i) = \sum_i \mu(A_i)$ for mutually exclusive events.
   
$\mu(\Omega)=1$ denoted probability measure, label with $P$.

#### properties
  - monotonicity: $A_1 \subseteq A_2\Rightarrow \mu(A_1)\leq \mu(A_2)$.
  - sub-additivity: $\mu(\bigcup_i A_i)\leq \sum_i\mu(A_i)$.
  - continuity from below: $A_i\uparrow A \Rightarrow \mu(A_i)\uparrow \mu(A)$.
  - continuity from above: if at aleast one $A_i$ measure finite, $A_i\downarrow A \Rightarrow \mu(A_i)\downarrow \mu(A)$.

### generated $\sigma$
> used for implicitly claim $\sigma$-algebra.

smallest $\sigma$-algebra $\mathcal{F}$ of $A_\alpha\subseteq \Omega$ s.t. $A_\alpha\in\mathcal{F}, \forall \alpha$, that is
$$
  \sigma(\{A_\alpha\})=\sigma(A_\alpha, \alpha\in\Gamma)=\bigcap \{\mathcal{G}:\mathcal{G}\subseteq 2^\Omega \text{ is } \sigma, A_\alpha\in\mathcal{G}, \forall \alpha\in\Gamma\}
$$

denote generated on topology $\mathbb{S}$ as $\mathcal{B}_\mathbb{S}=\sigma(\{ O\subseteq \mathbb{S} \text{ open}\})$, implicitly denote $\mathcal{B}=\mathcal{B}_\mathbb{R}$.

## Caratheodory's extension theorem

If $\mu_0: \mathcal{A}\rightarrow [0,\infty]$ is a countably additive set function on an algebra $\mathcal{A}$, then there exists a measure $\mu$ on $(\Omega, \sigma(\mathcal{A}))$ s.t. $\mu=\mu_0$ on $\mathcal{A}$. Furthermore, if $\mu_0(\Omega)<\infty$ then such a measure $\mu$ is unique.

> countably additive, algebra $\Rightarrow$ $\sigma$-algebra.

## Completeness
### Definition
A measure space is called complete, if $N\subseteq A, A\in \mathcal{F}, \mu(A)=0$, then $N\in\mathcal{F}$.

> contain null-sets.

### Theorem
measure space has its completion.

## Dynkin
### Definition
$\pi$-system: closed under **finite** intersections.

$\lambda$-system: contain $\Omega$ and $B\setminus A,\forall A\subseteq B,A,B\in \mathcal{L}$. which is also closed under monotone increasing limits(i.e. if $A_i\in\mathcal{L}$ and $A_i\uparrow A$, then $A\in\mathcal{L}$)

  - contain $\Omega$, closed under completement, closed under **countable disjoint** union.

### Theorem
$\sigma$-algebra $\Leftrightarrow$ $\pi$-system and $\lambda$-system.

### $\pi$-$\lambda$ theorem
If $P_\pi \subseteq L_\lambda$, then $\sigma(P_\pi)\subseteq L_\lambda$.

## Monotone class
closed under monotone limits.

### Halmos monotone class theorem
algebra $\mathcal{A}\subseteq \mathcal{M}\Rightarrow \sigma(\mathcal{A})\subseteq \mathcal{M}$.

## Banach-Tarski paradox
> respect to axiom of choice, a ball is equidecomposable to two balls.

### Collorary
$\exists A\subseteq \mathbb{R}$ that $A\notin\mathcal{B}$.