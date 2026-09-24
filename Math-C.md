# Mathematical Derivations, continued

Parts: [A](Math-A.md), [B](Math-B.md), [C](Math-C.md), [D](Math-D.md), [E](Math-E.md).

## 7. Algebraic-Geometric Synthesis: Minimal Polynomial of $`\varepsilon_{21}`$

### 7.1. Minimal Polynomial of $`\varepsilon_{21}`$ has Discriminant $21$

The minimal polynomial of $`\varepsilon_{21}`$ over $\mathbb{Q}$ is
$$m(x) = x^{2} - 5\,x + 1.$$
**Proof.** Since $`\varepsilon_{21} = (5 + \sqrt{21})/2`$ and its conjugate is $\bar{\varepsilon} = (5 - \sqrt{21})/2$, we have
$$\varepsilon_{21} + \bar{\varepsilon} = 5, \quad \varepsilon_{21} \cdot \bar{\varepsilon} = (25 - 21)/4 = 1.$$
Therefore $`\varepsilon_{21}`$ satisfies $x^{2} - 5x + 1 = 0$ by [Vieta's formulas](https://en.wikipedia.org/wiki/Vieta%27s_formulas). $\blacksquare$

The discriminant of this polynomial is
$$\Delta(m) = b^{2} - 4 a c = 5^{2} - 4\cdot 1\cdot 1 = 25 - 4 = \mathbf{21}.$$

**Discriminant identity.** This is not a coincidence: by the relationship between minimal polynomial discriminant and field discriminant for quadratic fields $\mathbb{Q}(\sqrt{D})$ with $D$ squarefree ([fundamental discriminant](https://en.wikipedia.org/wiki/Fundamental_discriminant)),
$$\Delta(m) = D \quad \text{if } D \equiv 1 \pmod 4,$$
$$\Delta(m) = 4D \quad \text{if } D \equiv 2 \text{ or } 3 \pmod 4.$$
Since the fundamental discriminant of $\mathbb{Q}(\sqrt{21})$ is $d = 21 \equiv 1 \pmod 4$ (squarefree, and congruent to $1$ modulo $4$), the minimal polynomial discriminant equals $21$ identically.

**Trace recurrence.** The sequence $`T_n = \varepsilon_{21}^{n} + \bar{\varepsilon}^{\,n}`$ satisfies
$$T_n = (\varepsilon_{21} + \bar{\varepsilon}) T_{n-1} - \varepsilon_{21} \bar{\varepsilon} \, T_{n-2} = 5\,T_{n-1} - T_{n-2},$$
with $`T_0 = 2`$ and $`T_1 = 5`$. The first few values are
$$2,\ 5,\ 23,\ 110,\ 527,\ 2525,\ 12098,\ 57965,\ \ldots$$
This is [OEIS A005247](https://oeis.org/A005247), the **Pell-like sequence at $5$**, with closed-form
$$T_n = \frac{(5+\sqrt{21})^{n} + (5-\sqrt{21})^{n}}{2^{n-1}}.$$
The value $`T_3 = 110 = 2 \cdot 55`$ recovers the fundamental Pell solution $(55, 12)$ of $x^{2} - 21 y^{2} = 1$ through $`T_3 / 2 = 55`$ and $`\sqrt{T_3^{2} - 4}/(2\sqrt{21}) = \sqrt{12100 - 4}/(2\sqrt{21}) = \sqrt{12096}/(2\sqrt{21}) = \sqrt{576}/2 = 12`$.

### 7.2. Grassmannian Dimensions Equal to $21$

The [Plücker embedding](https://en.wikipedia.org/wiki/Pl%C3%BCcker_embedding) realizes the [Grassmannian](https://en.wikipedia.org/wiki/Grassmannian) $\mathrm{Gr}(k, n)$ as a subvariety of $\mathbb{P}^{\binom{n}{k}-1}$. The dimension of $\mathrm{Gr}(k, n)$ over any field is
$$\dim \mathrm{Gr}(k, n) = k (n - k).$$
The diophantine equation $k (n - k) = 21$ has positive integer solutions:

| $(k, n)$   | $\mathrm{Gr}(k, n)$                     | Geometric realization                          |
| ---------- | --------------------------------------- | ---------------------------------------------- |
| $(1, 22)$  | $\mathrm{Gr}(1, 22) = \mathbb{P}^{21}$  | Lines in $22$-space                            |
| $(3, 10)$  | $\mathrm{Gr}(3, 10)$                    | $3$-planes in $10$-space                       |
| $(7, 10)$  | $\mathrm{Gr}(7, 10)$                    | $7$-planes in $10$-space (dual of Gr$(3, 10)$) |
| $(21, 22)$ | $\mathrm{Gr}(21, 22) = \mathbb{P}^{21}$ | $21$-planes in $22$-space                      |

The [Plücker embedding](https://en.wikipedia.org/wiki/Pl%C3%BCcker_embedding) of $\mathrm{Gr}(3, 10)$ is the quadric hypersurface $\mathbb{P}^{119}$ defined by the Grassmann-Plücker relations on the $\binom{10}{3} = 120$ Plücker coordinates. The four Grassmannians of dimension $21$ therefore sit inside the same $119$-dimensional projective space. Their intersections reflect the arithmetic of $21$.

### 7.3. Lie Algebra Dimensions $`\dim \mathfrak{so}(7) = \lvert\Phi^{+}(A_{6})\rvert = 21`$

Two distinct simple Lie algebras carry the integer $21$:

- $\dim \mathfrak{so}(7) = \frac{7 \cdot 6}{2} = 21$ ([orthogonal group](https://en.wikipedia.org/wiki/Orthogonal_group)). The Lie algebra $\mathfrak{so}(7)$ is the tangent space at the identity of the spin group $\mathrm{Spin}(7)$. It is one of only two classical Lie algebras, together with $\mathfrak{so}(8)$, that admit [triality](https://en.wikipedia.org/wiki/Triality). The $8$-dimensional spin representation of $\mathrm{Spin}(7)$ realizes the [octonions](https://en.wikipedia.org/wiki/Octonion) $\mathbb{O}$ as the imaginary octonions.

- $`\lvert\Phi^{+}(A_{6})\rvert = \frac{6 \cdot 7}{2} = 21`$ ([root system](https://en.wikipedia.org/wiki/Root_system)). The number of positive roots of the $`A_{6}`$ root system equals $\binom{7}{2}$.

The identity $\binom{n}{2} = 21$ at $n = 7$ is the **shared arithmetic**: $T(6) = \binom{7}{2} = 21$ and $`\lvert\Phi^{+}(A_{6})\rvert = \binom{7}{2}`$. This binomial structure appears on both sides of the bridge between the central node $T(6)$ and the Lie-theoretic dimension $21$.

### 7.4. The Harshad Property of $21$

A Harshad number, also called a Niven number, is an integer divisible by the sum of its digits ([Harshad number](https://en.wikipedia.org/wiki/Harshad_number)). For $n = 21$:
$$\sigma_1(21) = 2 + 1 = 3, \qquad 21 = 3 \cdot 7.$$
So $21$ is Harshad. The Harshad numbers below $100$ form the set
$$\{1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 18, 20, \mathbf{21}, 24, 27, 36, 40, 42, 45, 54, 60, 72, 81, 84, 90\}.$$
Among the Fibonacci-triangular semiprimes $\{1, 21, 55\}$, the integer $21$ is the largest (and only non-trivial) Harshad semiprime of this class. $55$ is not Harshad because $5+5 = 10$ does not divide $55$.

### 7.5. Cubic Residues Modulo $21$

The multiplicative group $(\mathbb{Z}/21\mathbb{Z})^{\times}$ has order $\varphi(21) = 12$ and group structure $`C_2 \times C_6`$ ([multiplicative group of integers modulo n](https://en.wikipedia.org/wiki/Multiplicative_group_of_integers_modulo_n) and [Euler's totient function](https://en.wikipedia.org/wiki/Euler%27s_totient_function)). The cubing endomorphism $\varphi: x \mapsto x^{3}$ has image of order $12 / \gcd(12, 3) = 4$. Direct verification:
$$1^3 \equiv 1,\quad 2^3 \equiv 8,\quad 3^3 \equiv 6,\quad 4^3 \equiv 1 \pmod{21},$$
$$5^3 \equiv 20,\quad 8^3 \equiv 8,\quad 10^3 \equiv 13 \pmod{21}.$$

The cubic residue set is
$$\{1, 8, 13, 20\},$$
a cyclic subgroup of order $4$ with generator $8$, because $8^{1} = 8$, $8^{2} = 64 \equiv 1$, and $8^{3} \equiv 8$ modulo $21$. The structure of cubic residues modulo $21$ is the canonical obstruction to a cube root lift from $\mathbb{Z}/21\mathbb{Z}$ to $\mathbb{Z}$, and the fact that the cubes $\{1, 8\}$ alone are $\pm 1$ in $(\mathbb{Z}/7\mathbb{Z})^{\times}$ extends the residue system across the prime factor $7 \equiv 3 \pmod 4$.

## 8. The Fano Plane and Number-Theoretic Properties

### 8.1. The Fano Plane $\mathrm{PG}(2, 2)$ has $21$ Incidences

The Fano plane $\mathrm{PG}(2, 2)$ is the projective plane of order $2$, realized over the field $`\mathbb{F}_{2}`$ ([Fano plane](https://en.wikipedia.org/wiki/Fano_plane)). Its incidence structure is governed by:

- **Points**: $7$ (the non-zero vectors of $`\mathbb{F}_{2}^{3}`$ up to scalar).
- **Lines**: $7$ (each line is a $2$-dimensional subspace of $`\mathbb{F}_{2}^{3}`$, hence has $3$ points).
- **Incidence**: $21$ (each point lies on $3$ lines, each line contains $3$ points).

The incidence count is
$$\text{number of incidences} = 7 \cdot 3 = 21.$$
The [Fano plane](https://en.wikipedia.org/wiki/Fano_plane) is self-dual, so the dual calculation gives the same value.

**Connection to $\binom{7}{2}$.** The Steiner triple system $S(2, 3, 7)$ on the Fano plane partitions the $\binom{7}{2} = 21$ unordered pairs of $7$ points into $7$ triples ([Steiner system](https://en.wikipedia.org/wiki/Steiner_system)). Therefore $21$ counts both the pairs and the triples, and each triple is a line.

**Automorphism group**:
$$\mathrm{Aut}(\mathrm{PG}(2, 2)) \cong \mathrm{PGL}(3, 2) \cong \mathrm{PSL}(2, 7),$$
with order $168 = 2^{3} \cdot 3 \cdot 7$. This is the smallest non-abelian simple group beyond $`A_{5}`$, and the coincidence with the prime factorization $2^{3} \cdot 3 \cdot 7$ shares the prime factors $3$ and $7$ with $21 = 3 \cdot 7$.

### 8.2. The Smarandache Function $S(21) = 7$

The Smarandache function $S(n)$, also called the Kempner function, is the smallest positive integer $m$ such that $n \mid m!$ ([Kempner function](https://en.wikipedia.org/wiki/Kempner_function)). For $n = 21 = 3 \cdot 7$, the smallest $m$ such that both $3 \mid m!$ and $7 \mid m!$ is $m = 7$ (since $3 \mid 6!$ and $7 \mid 7!$). Therefore
$$S(21) = 7.$$
**Verification**: $7! = 5040$ and $5040 / 21 = 240$, which is an integer. By contrast, $6! = 720$ and $720 / 21$ is not an integer.

The [Kempner function](https://en.wikipedia.org/wiki/Kempner_function) satisfies $S(p) = p$ for a prime $p$, and $S(pq) = \max(p, q)$ for distinct primes $`p < q`$. For $21 = 3 \cdot 7$, that rule gives $S(21) = 7$.

### 8.3. The Dedekind $\psi$ Function Equals $\sigma$ at $21$

The [Dedekind psi function](https://en.wikipedia.org/wiki/Dedekind_psi_function) is defined by
$$\psi(n) = n \prod_{p \mid n}\!\left(1 + \tfrac{1}{p}\right).$$
For squarefree $`n = p_{1} p_{2} \cdots p_{r}`$:
$$\sigma(n) = \prod_{i=1}^{r}(1 + p_{i}) = n \prod_{i=1}^{r}\!\left(1 + \tfrac{1}{p_{i}}\right) = \psi(n).$$
For $n = 21 = 3 \cdot 7$:
$$\psi(21) = 21 \cdot \frac{4}{3} \cdot \frac{8}{7} = \frac{21 \cdot 32}{21} = 32 = \sigma(21).$$
The factorization $\psi(21) = 32 = 2^{5}$ is a pure power of $2$, reflecting the relations $1 + 3 = 4 = 2^{2}$ and $1 + 7 = 8 = 2^{3}$.

### 8.4. Lagrange's Four-Square Count $`r_{4}(21) = 256`$

By [Jacobi's four-square theorem](https://en.wikipedia.org/wiki/Jacobi%27s_four-square_theorem), the number of ordered representations of $n$ as a sum of four squares is
$$r_{4}(n) = 8 \sum_{d \mid n,\, 4 \nmid d} d.$$
For $n = 21$, divisors are $1, 3, 7, 21$, all coprime to $4$, so
$$\sum_{d \mid 21,\, 4 \nmid d} d = 1 + 3 + 7 + 21 = 32.$$
Therefore
$$r_{4}(21) = 8 \cdot 32 = 256 = 4^{4}.$$
The integer $21$ has exactly $256$ ordered representations as a sum of four squares. Symmetry note: by Jacobi's formula $`r_{4}(n) = 8 \sigma(n)`$ for squarefree $n$, and $\sigma(21) = 32$, $8 \cdot 32 = 256$ is consistent with this identity.

### 8.5. Imaginary Quadratic Class Number of $\mathbb{Q}(\sqrt{-21})$

The fundamental discriminant of $\mathbb{Q}(\sqrt{-21})$ is $-84$, not $-21$, because $-21 \equiv 3 \pmod 4$ ([fundamental discriminant](https://en.wikipedia.org/wiki/Fundamental_discriminant)). The form class number $h(-84)$ counts reduced binary quadratic forms $ax^{2}+bxy+cy^{2}$ of discriminant $-84$ ([binary quadratic form](https://en.wikipedia.org/wiki/Binary_quadratic_form)).

**Enumeration.** Reduced forms satisfy $`|b| \le a \le c`$:

- $a=1$: $b^{2}+84=4c$, and $b=0$ gives $c=21$. Form $(1,0,21)$.
- $a=2$: $b^{2}+84=8c$, and $b=\pm 2$ gives $c=11$. Form $(2,2,11)$.
- $a=3$: $b^{2}+84=12c$, and $b=0$ gives $c=7$. Form $(3,0,7)$.
- $a=5$: $b^{2}+84=20c$, and $b=\pm 4$ gives $c=5$. Form $(5,4,5)$.

Therefore the form class number is $h(-84)=4$. This is not an application of the displayed Dirichlet formula. That formula requires a fundamental discriminant, and it uses the character of that discriminant ([class number formula](https://en.wikipedia.org/wiki/Class_number_formula)):
$$h(d) = \frac{w\sqrt{|d|}}{2\pi} L(1,\chi_{d}), \quad d < 0.$$
For $d=-84$, the character is $`\chi_{-84}`$, the root count is $w=2$, and $\sqrt{84}=2\sqrt{21}$. Therefore
$$L(1,\chi_{-84}) = \frac{2\pi}{\sqrt{21}} = 2\pi\,\Lambda(6).$$
The character $`\chi_{-21}`$ is not the character of discriminant $-84$, so the same identity is not claimed for $`L(1,\chi_{-21})`$.

**Real value.** The real class-number formula at section 3.2 still gives
$$L(1,\chi_{21}) = \frac{2\log\left(\frac{5+\sqrt{21}}{2}\right)}{\sqrt{21}} = 2\log\left(\frac{5+\sqrt{21}}{2}\right)\,\Lambda(6).$$
The ratio of the two displayed special values is
$$\frac{L(1,\chi_{-84})}{L(1,\chi_{21})} = \frac{\pi}{\log\left(\frac{5+\sqrt{21}}{2}\right)} \approx 2.2765,$$
which is irrational. No algebraic relation among $`L(1,\chi_{-84})`$, $`L(1,\chi_{21})`$, $\pi$, and $\log((5+\sqrt{21})/2)$ is known from these values. Whether a closed form exists is an open question.

### 8.6. Ramanujan Tau at $21$ and the Sharp $21^{2}$ Divisibility

The Ramanujan tau function is multiplicative for coprime arguments ([Ramanujan tau function](https://en.wikipedia.org/wiki/Ramanujan_tau_function)). Therefore
$$\tau(21) \;=\; \tau(3)\tau(7) \;=\; 252\times(-16744) \;=\; -4{,}219{,}488.$$
Using $\tau(3) = 2^{2}\cdot 3^{2}\cdot 7$ and $\tau(7) = -2^{3}\cdot 7\cdot 13\cdot 23$:
$$\tau(21) \;=\; -2^{5}\cdot 3^{2}\cdot 7^{2}\cdot 13\cdot 23 \;=\; -21^{2}\cdot 9568.$$

**$21$-adic valuation.** The equalities $`v_{3}(\tau(21))=2`$ and $`v_{7}(\tau(21))=2`$ give $`v_{21}(\tau(21))=2`$. The square $21^{2}=441$ exactly divides $\tau(21)$, while $21^{3}=9261$ does not. The total $`v_{7}(\tau(21))=2`$ comes from $`v_{7}(\tau(3))=1`$ and $`v_{7}(\tau(7))=1`$. The total $`v_{3}(\tau(21))=2`$ comes from $`v_{3}(\tau(3))=2`$ and $`v_{3}(\tau(7))=0`$. Both contribute to the divisibility by $21^2$.

**Ramanujan congruence.** The standard $`\tau(n)\equiv \sigma_{11}(n)\pmod{691}`$ for all $n$, established by [Ramanujan (1916)](https://en.wikipedia.org/wiki/Ramanujan%27s_congruence), gives
$$\sigma_{11}(21) \;=\; 1+3^{11}+7^{11}+21^{11} \;=\; 350{,}279{,}478{,}046{,}112.$$
Direct computation confirms
$$\tau(21)-\sigma_{11}(21) \;=\; -350{,}283{,}697{,}535{,}600 \;=\; -691\cdot 506{,}920{,}832.$$

### 8.7. Self-Dual Standard Young Tableau Pair at $n=7$

Among the $15$ partitions of $7$, the standard Young tableau counts given by the [hook-length formula](https://en.wikipedia.org/wiki/Hook-length_formula) are
$$\{1,\ 6,\ 14,\ 14,\ 15,\ 35,\ 21,\ 21,\ 20,\ 35,\ 14,\ 15,\ 14,\ 6,\ 1\}.$$
The value $21$ occurs exactly twice, for the dual pair
$$\lambda_{1}=(3,3,1),\qquad \lambda_{2}=(3,2,2).$$

**Hook lengths.**

For $`\lambda_{1}=(3,3,1)`$, the hook lengths are $5, 3, 2$ in row $1$, $4, 2, 1$ in row $2$, and $1$ in row $3$:
$$\prod h = 5\cdot 3\cdot 2\cdot 4\cdot 2\cdot 1\cdot 1 = 240,\quad f^{\lambda_{1}} = 7!/240 = 21.$$

For $`\lambda_{2}=(3,2,2)`$, the hook lengths are $5, 4, 1$ in row $1$, $3, 2$ in row $2$, and $2, 1$ in row $3$:
$$\prod h = 5\cdot 4\cdot 1\cdot 3\cdot 2\cdot 2\cdot 1 = 240,\quad f^{\lambda_{2}} = 21.$$

**Transpose.** $`\lambda_{1}'`$ has column lengths $`(3,2,2)=\lambda_{2}`$, and $`\lambda_{2}'=(3,3,1)=\lambda_{1}`$. The pair is dual under transpose. Neither partition is self-conjugate, but their hook-length products coincide. This is the unique dual pair among partitions of $7$ that produces a value of at least $20$ in both entries.

## 9. Further Lie-Theoretic Dimensions and Recursive Intersections

### 9.1. Symplectic Dimension $\dim \mathfrak{sp}(6) = 21$

The symplectic Lie algebra $\mathfrak{sp}(2n)$ has dimension $n(2n+1) = 2n^{2} + n$ ([symplectic group](https://en.wikipedia.org/wiki/Symplectic_group)). At $n = 3$:
$$\dim \mathfrak{sp}(6) = 3 \cdot 7 = 21.$$
The compact symplectic group $\mathrm{Sp}(6)$ has complexification $\mathrm{Sp}(6, \mathbb{C})$, a simple algebraic group of Lie-algebra dimension $21$. Its Dynkin diagram is $`C_{3}`$, with $3$ simple roots and $9$ positive roots, hence total dimension $2 \cdot 9 + 3 = 21$. This complements §7.3's $`\mathfrak{so}(7) = B_{3}`$ and $`A_{6}`$ root counts.

### 9.2. Moduli of Abelian Varieties $`\dim \mathcal{A}_{6} = 21`$

The Siegel modular variety of principally polarized abelian varieties of dimension $g$ has complex dimension ([Siegel modular variety](https://en.wikipedia.org/wiki/Siegel_modular_variety))
$$\dim \mathcal{A}_{g} = \frac{g(g+1)}{2}.$$
At $g = 6$:
$$\dim \mathcal{A}_{6} = \frac{6 \cdot 7}{2} = 21.$$
This is the same binomial coefficient as $`\lvert\Phi^{+}(A_{6})\rvert`$, $\dim \mathfrak{so}(7)$, and $T(6)$. The arithmetic identity $\binom{g+1}{2} = 21$ at $g = 6$ thus propagates across four distinct mathematical structures.

### 9.3. The Modular Curve $`X_{0}(21)`$ is an Elliptic Curve

The index of the congruence subgroup $`\Gamma_{0}(N)`$ in $`\mathrm{SL}_{2}(\mathbb{Z})`$ is ([modular curve](https://en.wikipedia.org/wiki/Modular_curve))
$$\mu(N) = N \prod_{p \mid N}\!\left(1 + \frac{1}{p}\right).$$
For $N = 21 = 3 \cdot 7$:
$$\mu(21) = 21 \cdot \frac{4}{3} \cdot \frac{8}{7} = 32.$$
The genus of the modular curve $`X_{0}(N) = \Gamma_{0}(N) \backslash \mathbb{H}^{*}`$ depends on $\mu$, the elliptic-point counts $`\nu_{2}, \nu_{3}`$, and the cusp count $`\nu_{\infty}`$. The precise values for $N = 21$ are
$$\nu_{2}(21) = 0,\quad \nu_{3}(21) = 2,\quad \nu_{\infty}(21) = 4.$$
The standard genus formula gives
$$g(X_{0}(21)) = 1 + \frac{\mu}{12} - \frac{\nu_{2}}{4} - \frac{\nu_{3}}{3} - \frac{\nu_{\infty}}{2} = 1 + \frac{32}{12} - 0 - \frac{2}{3} - \frac{4}{2} = 1 + \frac{8}{3} - \frac{2}{3} - 2 = 1 + 2 - 2 = 1.$$
So $`g(X_{0}(21)) = 1`$, meaning $`X_{0}(21)`$ is an elliptic curve over $\mathbb{Q}$ ([elliptic curve](https://en.wikipedia.org/wiki/Elliptic_curve)). The associated elliptic curve has Cremona conductor $21$ and label `21a1`, with [j-invariant](https://en.wikipedia.org/wiki/J-invariant) $`j(E_{21}) = \dfrac{193^{3}}{3^{4} \cdot 7^{2}} = \dfrac{7{,}189{,}057}{3{,}969} \approx 1811.30`$ ([LMFDB 21.a5](https://www.lmfdb.org/EllipticCurve/Q/21/a/5), Cremona label `21a1`).

This fact that $21$ is the conductor of a unique elliptic curve, distinct from the modular-curve $`X_{0}(6)`$ whose cusp-form dimension at weight $24$ equals $21$ (§3.3), ties together the $`\Gamma_{0}`$-theory with the value $21$ in two independent roles.

### 9.4. The Centred Octagonal Numbers $`C_{8}(n)`$ and Other Centred Polygonal Series

The centered polygonal numbers $`C_{s}(n) = \frac{s \cdot n(n-1)}{2} + 1`$ for $s = 3, 4, 5, \ldots$ ([centered polygonal number](https://en.wikipedia.org/wiki/Centered_polygonal_number)) are computed for small $n$:
$$C_{3}(1) = 1,\ C_{3}(2) = 4,\ C_{3}(3) = 10,\ C_{3}(4) = 19;$$
$$C_{4}(1) = 1,\ C_{4}(2) = 5,\ C_{4}(3) = 13,\ C_{4}(4) = 25;$$
$$C_{5}(1) = 1,\ C_{5}(2) = 6,\ C_{5}(3) = 16,\ C_{5}(4) = 31;$$
$$C_{6}(1) = 1,\ C_{6}(2) = 7,\ C_{6}(3) = 19,\ C_{6}(4) = 37;$$
$$C_{7}(1) = 1,\ C_{7}(2) = 8,\ C_{7}(3) = 22,\ C_{7}(4) = 43;$$
$$C_{8}(1) = 1,\ C_{8}(2) = 9,\ C_{8}(3) = 25,\ C_{8}(4) = 49;$$
The integer $21$ does not appear in any centred polygonal series below $s = 100$, so $21$ is not a centred polygonal number. The integer $21$ is a regular polygonal number in three ways, namely $P(3, 6) = P(8, 3) = P(21, 2) = 21$ (see §2). It is not a centred polygonal number. That distinction removes $21$ from the centred-polygonal lattice while keeping it in the regular polygonal lattice.

### 9.5. The Coxeter Invariant of $(3, 3, 7)$ has Denominator $21$

The hyperbolic triangle group $(p, q, r)$ ([triangle group](https://en.wikipedia.org/wiki/Triangle_group) and [Coxeter group](https://en.wikipedia.org/wiki/Coxeter_group)) has the quantity called a Coxeter invariant here
$$h(p, q, r) = \frac{1}{p} + \frac{1}{q} + \frac{1}{r} - 1.$$
For the triple $(3, 3, 7)$:
$$h(3, 3, 7) = \frac{1}{3} + \frac{1}{3} + \frac{1}{7} - 1 = \frac{7 + 7 + 3}{21} - 1 = -\frac{4}{21}.$$
The denominator is exactly $21$. The triple $(3, 3, 7)$ generates the [Klein quartic surface](https://en.wikipedia.org/wiki/Klein_quartic), the unique [Hurwitz surface](https://en.wikipedia.org/wiki/Hurwitz%27s_automorphism_theorem) of order $84 = 4 \cdot 21$. Its full automorphism group has order $168 = 8 \cdot 21$, namely $\mathrm{PSL}(2, 7)$.
