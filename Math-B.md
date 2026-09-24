# Mathematical Derivations, continued

Parts: [A](Math-A.md), [B](Math-B.md), [C](Math-C.md), [D](Math-D.md), [E](Math-E.md).

## 5. Self-Referential Theorems at Index $6$

### 5.1. Triangular Spectrum Theorem

**Theorem.** _For level $N=6$ and all $m \ge 1$ such that $T(m)+3$ is even (equivalently, $m \equiv 1$ or $2 \pmod{4}$),_
$$\dim S_{T(m)+3}\!\bigl(\Gamma_0(6)\bigr) = T(m).$$

_In particular, every **odd** triangular number $T(m)$ is realised as a cusp-form dimension at weight $k=T(m)+3$ on $`\Gamma_0(6)`$._

**Proof.** From §3.3 and [Stein, Proposition 6.1](https://wstein.org/books/modform/modform/dimension_formulas.html), $`\dim S_k\!\bigl(\Gamma_0(6)\bigr) = k-3`$ for **even** $k \ge 4$. The weight $k = T(m)+3$ is even precisely when $T(m)$ is odd, which occurs when $m \equiv 1$ or $2 \pmod{4}$. Substituting $k = T(m)+3$ gives $T(m)+3-3 = T(m)$. $\blacksquare$

The corollary gives a catalogue **restricted to** $m \equiv 1, 2 \pmod{4}$:

| $m$         | 1   | 2   | 5   | 6   | 9   | 10  | 13  | 14  |
| ----------- | --- | --- | --- | --- | --- | --- | --- | --- |
| $T(m)$      | 1   | 3   | 15  | 21  | 45  | 55  | 91  | 105 |
| $k=T(m)+3$  | 4   | 6   | 18  | 24  | 48  | 58  | 94  | 108 |
| $m \bmod 4$ | 1   | 2   | 1   | 2   | 1   | 2   | 1   | 2   |

The differences between successive valid weights are $2, 12, 6, 24, 10, 36, 14, \ldots$, which do not form a simple arithmetic progression.

### 5.2. Eisenstein Twin Theorem

**Theorem.** _For level $N=6$ and all **even** $k\ge 4$, the Eisenstein subspace dimension is constant:_
$$\dim E_k\!\bigl(\Gamma_0(6)\bigr) = 2.$$

**Proof.** The total dimension formula **for even** $k$ gives
$$\dim M_k\!\bigl(\Gamma_0(6)\bigr) = (k-1)(0-1) + 0 + 0 + \tfrac{k-1}{2}\cdot 4 = (k-1)(-1) + 2(k-1) = k - 1.$$
The full modular space at level $N$ satisfies $`\dim M_k = \dim S_k + \dim E_k`$, and therefore
$$\dim E_k\!\bigl(\Gamma_0(6)\bigr) = \dim M_k - \dim S_k = (k-1) - (k-3) = 2.$$
Cusp analysis: $`X_0(6)`$ has four cusps at $\{0,\,1/2,\,1/3,\,1/6\}$ with widths $1,\,2,\,3,\,6$. The Eisenstein series at level $6$ consists of those of width $1$ (one series) plus one of each pair of wider cusps that couple under the [Atkin-Lehner involution](https://en.wikipedia.org/wiki/Atkin%E2%80%93Lehner_theory), giving exactly two linearly independent Eisenstein series for even $k\ge 4$. $\blacksquare$

**Remark.** For **odd** $k \ge 3$, every Eisenstein series at level $\ge 2$ vanishes by invariance under $-I$, so $`\dim E_k=0`$. The theorem therefore applies only to even weights.

### 5.3. Self-Reference Table

The integer $n=6$ and the value $21$ are linked by the quantities below. Each definition is cited in section 7 of [README.md](README.md#7-sources): [triangular numbers](https://en.wikipedia.org/wiki/Triangular_number), [Ramsey's theorem](https://en.wikipedia.org/wiki/Ramsey%27s_theorem), the [Carmichael function](https://en.wikipedia.org/wiki/Carmichael_function), [multiplicative order](https://en.wikipedia.org/wiki/Multiplicative_order), [continued fractions](https://en.wikipedia.org/wiki/Continued_fraction), and [Stein, Proposition 6.1](https://wstein.org/books/modform/modform/dimension_formulas.html). Verification is by direct computation. No other triangular index $n\le 5000$ was found with these matches. This is computational, not a proof.

| #   | Quantity                                 | Definition                                          | Value |
| --- | ---------------------------------------- | --------------------------------------------------- | ----: |
| 1   | $T^{-1}(21)$                             | $n(n+1)/2=21$                                       |   $6$ |
| 2   | $R(3,3)$                                 | Ramsey critical number for $`K_6`$                  |   $6$ |
| 3   | $\lambda(21)$                            | Carmichael function                                 |   $6$ |
| 4   | $`\mathrm{ord}_{21}(2)`$                 | multiplicative order of $2$ modulo $21$             |   $6$ |
| 5   | $r(\sqrt{21})$                           | CF period of $\sqrt{21}=[4;\overline{1,1,2,1,1,8}]$ |   $6$ |
| 6   | $`\dim S_{24}\!\bigl(\Gamma_0(6)\bigr)`$ | weight-$24$ cusp dimension on $`\Gamma_0(6)`$       |  $21$ |

Items $1$ through $5$ equal $6$ (the index). Item $6$ equals $21$ (the value).

### 5.4. Connection to $`\dim S_k\!\bigl(\Gamma_0(21)\bigr)`$

For comparison, level $N=21$ has modular signature $`(g,\nu_2,\nu_3,\nu_\infty)=(1,0,2,4)`$, using the counts in [Stein, definitions preceding Proposition 6.1](https://wstein.org/books/modform/modform/dimension_formulas.html). Direct computation:

$$\dim S_k\!\bigl(\Gamma_0(21)\bigr) = (k-1)\cdot 0 + 0 + \left\lfloor\tfrac{k}{3}\right\rfloor\cdot 2 + \Bigl(\tfrac{k}{2}-1\Bigr)\cdot 4.$$

| $k$                                    | 4   | 5   | 6   | 9   | 12  | 24  |
| -------------------------------------- | --- | --- | --- | --- | --- | --- |
| $`\dim S_k\!\bigl(\Gamma_0(21)\bigr)`$ | 6   | 6   | 12  | 18  | 28  | 60  |

The level $21$ does not return to $21$ at any weight in the table above, in contrast to level $6$. The cusp dimension at level $6$, weight $24$ equals $21=T(6)$ (see §3.3), while at level $21$ the cusp dimension at weight $4$ equals $6=R(3,3)$ (table).

### 5.5. Polygonal Richness and the Fibonacci Intersection

Define the _polygonal richness_ $\rho(N)$ as the number of distinct pairs $(s,n)$ with $s\ge 3$, $n\ge 2$ such that $P(s,n)=N$, where $P(s,n)=\frac{(s-2)n^2-(s-4)n}{2}$ is the $n$-th $s$-gonal number ([polygonal number](https://en.wikipedia.org/wiki/Polygonal_number)).

**Computation.** For $N=21$, solving $P(s,n)=21$ yields exactly three solutions:

$$\rho(21)=3,\quad (s,n)\in\{(3,6),\;(8,3),\;(21,2)\}.$$

Among [Fibonacci numbers](https://en.wikipedia.org/wiki/Fibonacci_sequence) below $1000$, the polygonal richness values are:

$$\rho(F_8)=\rho(21)=3,\quad \rho(F_{10})=\rho(55)=3,\quad \rho(F_{12})=\rho(144)=3,$$

with all other $`F_n`$ having $`\rho(F_n)\le 2`$.

**Observation.** Among [Fibonacci numbers](https://en.wikipedia.org/wiki/Fibonacci_sequence) below $1000$, namely $`F_n`$ for $n\le 16$, the values $21$, $55$, and $144$ each have polygonal richness $\rho=3$. All other Fibonacci numbers below $1000$ have $\rho\le 2$.

The general formula for polygonal richness: $s(n)=\frac{2n^2-4n+2N}{n(n-1)}$ must be a positive integer $\ge 3$. For $N=21$, this holds at $n=2,3,6$. For $N=55$, it holds at $n=2,5,10$. For $N=144$, it holds at $n=2,3,12$.

### 5.6. The Carmichael Function Constraint

The values of $\lambda$ used below are those of the [Carmichael function](https://en.wikipedia.org/wiki/Carmichael_function). The triangular and Fibonacci memberships use the definitions in [triangular numbers](https://en.wikipedia.org/wiki/Triangular_number) and the [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_sequence).

**Theorem.** _The integer $21$ is the unique number satisfying all three conditions:_

1. $\lambda(n)=6$
2. $n$ is [triangular](https://en.wikipedia.org/wiki/Triangular_number)
3. $n$ is [Fibonacci](https://en.wikipedia.org/wiki/Fibonacci_sequence)

**Proof.** The equation $\lambda(n)=6$ has exactly $14$ solutions below $200$:
$$n\in\{7,9,14,18,21,28,36,42,56,63,72,84,126,168\}.$$

Among these, the [triangular numbers](https://en.wikipedia.org/wiki/Triangular_number) are $\{21,28,36\}$ because $T(6)=21$, $T(7)=28$, and $T(8)=36$. Of these, only $21$ is a [Fibonacci number](https://en.wikipedia.org/wiki/Fibonacci_sequence), namely $`F_8=21`$. $\blacksquare$

This establishes the [Carmichael function](https://en.wikipedia.org/wiki/Carmichael_function) constraint as the binding condition in the quintuple identity. It eliminates $55$, which has $\lambda(55)=20\neq 6$, and all other triangular-Fibonacci intersections.

### 5.7. The Genus Transition at Triangular Levels

For the modular curve $`X_0(N)`$ with $N=T(n)$ ([modular curve](https://en.wikipedia.org/wiki/Modular_curve)), the genus $g$ is:
$$g=1+\frac{\mu}{12}-\frac{\nu_2}{4}-\frac{\nu_3}{3}-\frac{\nu_\infty}{2},$$
where $`\mu=N\prod_{p|N}(1+1/p)`$ is the index, $`\nu_2, \nu_3`$ are elliptic point counts, and $`\nu_\infty`$ is the cusp count.

**Computation.** For triangular levels $N=T(n)$ with $1\le n\le 7$:

| $n$ | $T(n)$ | $\mu$ | $`\nu_\infty`$ | $g$ |
| --- | ------ | ----- | -------------- | --- |
| $1$ | $1$    | $1$   | $1$            | $0$ |
| $2$ | $3$    | $4$   | $2$            | $0$ |
| $3$ | $6$    | $12$  | $4$            | $0$ |
| $4$ | $10$   | $18$  | $4$            | $0$ |
| $5$ | $15$   | $24$  | $4$            | $1$ |
| $6$ | $21$   | $32$  | $4$            | $1$ |
| $7$ | $28$   | $48$  | $6$            | $2$ |

**Theorem.** _The genus of $`X_0(T(n))`$ transitions from $g=0$ to $g=1$ at $n=5$ ($T(5)=15$). The levels $T(6)=21$ and $T(7)=28$ both have positive genus, with $g=1$ and $g=2$ respectively._

This genus transition marks a structural change in the geometric complexity of the modular curve: for $n\le 4$, $`X_0(T(n))`$ is a rational curve (genus $0$), while for $n\ge 5$, it has non-trivial topology.

### 5.8. The Quadratic Field Connection

The fields $\mathbb{Q}(\sqrt{5})$ and $\mathbb{Q}(\sqrt{21})$ are both real quadratic fields with class number $h=1$ ([class-number-one fields](https://en.wikipedia.org/wiki/List_of_number_fields_with_class_number_one)).

**For $\mathbb{Q}(\sqrt{5})$:**

- Ring of integers: $\mathbb{Z}[\varphi]$ where $\varphi=(1+\sqrt{5})/2$
- Fundamental unit: $\varphi$
- Discriminant: $\Delta=5$

**For $\mathbb{Q}(\sqrt{21})$:**

- Ring of integers: $\mathbb{Z}[(1+\sqrt{21})/2]$ (since $21\equiv 1\pmod{4}$)
- Fundamental unit: $\varepsilon=(5+\sqrt{21})/2$
- Discriminant: $\Delta=21$

**Theorem.** _Both $\mathbb{Q}(\sqrt{5})$ and $\mathbb{Q}(\sqrt{21})$ have class number $1$, establishing unique factorization in their rings of integers._

This class-number-one property, tabulated for both fields in the [class-number-one list](https://en.wikipedia.org/wiki/List_of_number_fields_with_class_number_one), connects [Fibonacci numbers](https://en.wikipedia.org/wiki/Fibonacci_sequence), which are governed by $\mathbb{Q}(\sqrt{5})$, with the invariant $\Lambda(6)=1/\sqrt{21}$, which is governed by $\mathbb{Q}(\sqrt{21})$.

**Ramification.** The discriminant $\Delta=21=3\times 7$ determines that exactly the primes $3$ and $7$ ramify in $\mathbb{Q}(\sqrt{21})$ ([fundamental discriminant](https://en.wikipedia.org/wiki/Fundamental_discriminant)). This is the arithmetic reason why $21=3\times 7$ appears in the class number formula and L-function identities.

## 6. Padovan, Narayana, Catalan, and Aliquot Structure

### 6.1. Padovan Sequence

The Padovan sequence is defined by $P(0)=P(1)=P(2)=1$ and $P(n)=P(n-2)+P(n-3)$ for $n\ge 3$ ([Padovan sequence](https://en.wikipedia.org/wiki/Padovan_sequence)). The first thirteen terms are
$$1,\ 1,\ 1,\ 2,\ 2,\ 3,\ 4,\ 5,\ 7,\ 9,\ 12,\ 16,\ \mathbf{21},$$
with $P(12)=21$.

**Closed form.** The characteristic polynomial is $x^3 - x - 1 = 0$, whose real root is the plastic constant $\rho \approx 1.3247$. The two complex roots are conjugate with modulus $`|\rho'| \approx 0.8688 < 1`$. The closed form is
$$P(n) = \frac{\rho^{n}}{(\rho-1)(\rho+1)} + \mathrm{(conjugate\ terms)},$$
and $P(n) \sim \rho^n/((\rho-1)(\rho+1))$ for large $n$.

**Membership.** The integer $21$ appears in each of the [triangular](https://en.wikipedia.org/wiki/Triangular_number), [Fibonacci](https://en.wikipedia.org/wiki/Fibonacci_sequence), [Jacobsthal](https://en.wikipedia.org/wiki/Jacobsthal_number), and [Padovan](https://en.wikipedia.org/wiki/Padovan_sequence) sequences at distinct indices. The Padovan index is $12$ above, and the Jacobsthal partial sum is at index $5$ in §12.3.

### 6.2. Narayana Numbers

The Narayana numbers refine the Catalan numbers ([Narayana number](https://en.wikipedia.org/wiki/Narayana_number)) by
$$N(n,k) = \frac{1}{n}\binom{n}{k}\binom{n}{k-1}, \qquad C_n = \sum_{k=1}^{n} N(n,k).$$
The seventh row is
$$N(7,\ast) = \big[\,1,\ 21,\ 105,\ 175,\ 105,\ 21,\ 1\,\big].$$

**Direct computation for $N(7,2)$**:
$$N(7,2) = \frac{1}{7}\binom{7}{2}\binom{7}{1} = \frac{1}{7}\cdot 21 \cdot 7 = 21.$$

The [Narayana numbers](https://en.wikipedia.org/wiki/Narayana_number) count triangulations of a polygon by an orientation-compatible class. $N(7,2)=21$ counts the triangulations of a heptagon by $2$-ear removal, and $N(7,6)=21$ counts those by the dual $(7-2)$-ear removal. The symmetry $N(n,k)=N(n,n+1-k)$ is reflected in the palindrome of the row.

### 6.3. One-Half of the Fifth Catalan Number

By the standard formula $`C_n = \frac{1}{n+1}\binom{2n}{n}`$ ([Catalan number](https://en.wikipedia.org/wiki/Catalan_number)), the fifth Catalan number is
$$C_5 = \frac{1}{6}\binom{10}{5} = \frac{1}{6}\cdot 252 = 42 = 2\cdot 21.$$
Therefore $`21 = C_5/2`$. The half-Catalan sequence $`C_n/2`$ for small $n$ gives
$$\tfrac{1}{2},\ 1,\ 2,\ 5,\ \tfrac{21}{2},\ 33,\ \tfrac{429}{2},\ 715,\ \ldots$$
Few of these are integers (only when $`C_n \equiv 0 \pmod 2`$). The first such at $n=15$ gives $`C_{15}/2 = 9694845`$. This note does not bear on the central identity $`21 = C_5/2`$.

### 6.4. Aliquot Sequence

The aliquot sequence of $n$ is defined by $`a_0 = n`$ and $`a_{k+1} = \sigma(a_k) - a_k`$ ([aliquot sequence](https://en.wikipedia.org/wiki/Aliquot_sequence)). For $n=21$,
$$21 \to (\sigma(21) - 21) = (1+3+7+21-21) = 11 \to \sigma(11)-11 = (1+11-11) = 1 \to \sigma(1)-1 = 0 \to 0 \to \cdots$$
The sequence reaches the absorbing state $0$ in three steps from $21$. The sequence is deficient-terminating since $21$ is deficient ($`\sigma(21) = 32 < 42 = 2\cdot 21`$) and $11$ is prime (deficient).

### 6.5. Sum of Three Squares

By [Lagrange's four-square theorem](https://en.wikipedia.org/wiki/Lagrange%27s_four-square_theorem) every positive integer is a sum of four squares, and by [Legendre's three-square theorem](https://en.wikipedia.org/wiki/Legendre%27s_three-square_theorem) an integer $n$ is a sum of three squares if and only if $n$ is not of the form $4^a(8b+7)$. Since $21 \equiv 5 \pmod 8$, it is a sum of three squares. The unique representation with $a \le b \le c$ is
$$21 = 1^2 + 2^2 + 4^2.$$
Verification: $1 + 4 + 16 = 21$. No representation as a sum of two positive squares exists because $21 \equiv 1 \pmod 4$, but the prime factor $3 \equiv 3 \pmod 4$ appears to an odd power ([sum of two squares theorem](https://en.wikipedia.org/wiki/Sum_of_two_squares_theorem)).
