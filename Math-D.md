# Mathematical Derivations, continued

Parts: [A](Math-A.md), [B](Math-B.md), [C](Math-C.md), [D](Math-D.md), [E](Math-E.md).

## 10. Galois, Hilbert, and Combinatorial Final Intersections

### 10.1. Galois Group of $x^{21} - x$

The polynomial $`x^{21} - x = x(x^{20} - 1) = x \prod_{d \mid 20} \Phi_{d}(x)`$ factors over $\mathbb{Q}$ as a product of cyclotomic polynomials ([cyclotomic polynomial](https://en.wikipedia.org/wiki/Cyclotomic_polynomial)). The splitting field of $x^{21} - x$ over $\mathbb{Q}$ is
$$K = \mathbb{Q}(\zeta_{1}, \zeta_{2}, \zeta_{4}, \zeta_{5}, \zeta_{10}, \zeta_{20}).$$
The Galois group is
$$\mathrm{Gal}(K/\mathbb{Q}) \cong (\mathbb{Z}/21\mathbb{Z})^{\times} \cong C_{2} \times C_{6},$$
of order $\varphi(21) = 12$. By contrast, the Galois group of $x^{21} - x - 1$ over $\mathbb{Q}$ is $`S_{21}`$ ([Osada, Theorem 1, as stated by Conrad](https://kconrad.math.uconn.edu/blurbs/gradnumthy/galoisselmerpoly.pdf)).

The structure $`C_{2} \times C_{6}`$ has the same cyclic decomposition as $(\mathbb{Z}/21\mathbb{Z})^{\times}$, confirming the [Chinese Remainder Theorem](https://en.wikipedia.org/wiki/Chinese_remainder_theorem) isomorphism in the Galois-theoretic setting.

### 10.2. Hilbert Polynomial of $\mathbb{P}^{2}$

For the projective plane $\mathbb{P}^{2}$ over $\mathbb{Q}$, the Hilbert polynomial of the structure sheaf is ([Hilbert polynomial](https://en.wikipedia.org/wiki/Hilbert_polynomial))
$$\chi(\mathbb{P}^{2}, \mathcal{O}(k)) = \binom{k+2}{2} = \frac{(k+1)(k+2)}{2}.$$
At $k = 5$:
$$\binom{7}{2} = \frac{6 \cdot 7}{2} = 21.$$
The space of degree-$5$ homogeneous polynomials in three variables $\{x, y, z\}$ has $21$ linearly independent monomials in three variables. Geometrically, these are sections of the line bundle $`\mathcal{O}_{\mathbb{P}^{2}}(5)`$ on the projective plane.

The genus of the curve defined by a generic such polynomial (a smooth plane curve of degree $5$) is, by the degree-genus formula ([genus-degree formula](https://en.wikipedia.org/wiki/Genus%E2%80%93degree_formula)),
$$g = \frac{(d-1)(d-2)}{2} = \frac{4 \cdot 3}{2} = 6.$$
So a smooth plane quintic has genus $6$. The relation $g(\text{plane quintic}) = 6$ alongside $\chi(\mathbb{P}^{2}, \mathcal{O}(5)) = 21$ is a coinvariance: $21$ as Hilbert function value, $6$ as genus, both at $k = 5$ in $\mathbb{P}^{2}$.

### 10.3. Central Polygonal Number $n^{2}-n+1=21$

OEIS calls the numbers $n^{2}-n+1$ the central polygonal numbers ([OEIS A002061](https://oeis.org/A002061)). The sequence begins $1, 1, 3, 7, 13, 21, 31, \ldots$. At $n=6$,
$$6^{2}-6+1 = 31,$$
and the preceding term is
$$5^{2}-5+1 = 21.$$
Therefore $21$ is the term of index $5$ in that OEIS sequence, not the evaluation at $n=5$ under a one-based shift.

The lazy caterer's sequence is a different sequence, $n(n+1)/2+1$, whose values begin $1, 2, 4, 7, 11, 16, 22, \ldots$ ([lazy caterer's sequence](https://en.wikipedia.org/wiki/Lazy_caterer%27s_sequence) and [OEIS A000124](https://oeis.org/A000124)). Five cuts give $16$, not $21$. The centered hexagonal numbers are also different: they are $3n(n+1)+1$, beginning $1, 7, 19, 37, \ldots$ ([centered hexagonal number](https://en.wikipedia.org/wiki/Centered_hexagonal_number); [OEIS A003215](https://oeis.org/A003215)). None of those displayed terms is $21$.

### 10.4. The Subgroup Lattice of $\mathbb{Z}/21\mathbb{Z}$

By the [Chinese remainder theorem](https://en.wikipedia.org/wiki/Chinese_remainder_theorem),
$$\mathbb{Z}/21\mathbb{Z} \cong \mathbb{Z}/3\mathbb{Z} \times \mathbb{Z}/7\mathbb{Z},$$
both factors cyclic. The subgroup lattice of $\mathbb{Z}/21\mathbb{Z}$ consists of exactly four subgroups:

| Order | Subgroup                                               |
| ----: | ------------------------------------------------------ |
|   $1$ | $\{0\}$                                                |
|   $3$ | $\mathbb{Z}/3\mathbb{Z} \times \{0\}$                  |
|   $7$ | $\{0\} \times \mathbb{Z}/7\mathbb{Z}$                  |
|  $21$ | $\mathbb{Z}/3\mathbb{Z} \times \mathbb{Z}/7\mathbb{Z}$ |

This is the Boolean lattice of subgroups for $n = pq$ with distinct primes $p, q$. Quotients are in bijection with subgroups for abelian groups, so the dual lattice (quotients) is identical. The group ring $\mathbb{Z}[\mathbb{Z}/21]$ decomposes as $\mathbb{Z}[\mathbb{Z}/3] \otimes \mathbb{Z}[\mathbb{Z}/7]$, and $`(\mathbb{Z}/21)^{\times} \cong C_{2} \times C_{6}`$ by character theory.

## 11. Order-4 Projective Plane, Self-Dual Codes, and Splitting Primes

### 11.1. The Projective Plane of Order $4$

For a finite field $`\mathbb{F}_{q}`$ with $q \ge 2$, the projective plane $`\mathrm{PG}(2, \mathbb{F}_{q})`$ ([projective plane](https://en.wikipedia.org/wiki/Projective_plane)) has
$$\text{number of points} = \text{number of lines} = q^{2} + q + 1.$$
Verification: points are $1$-dimensional subspaces of $`\mathbb{F}_{q}^{3}`$, so

$$\text{number of points} = (q^{3} - 1)/(q - 1) = q^{2} + q + 1.$$

Lines are $2$-dimensional subspaces of $`\mathbb{F}_{q}^{3}`$, and that count is also $q^{2} + q + 1$. Each line has $q + 1$ points.

**At $q = 4$:** The field $`\mathbb{F}_{4} = \mathbb{F}_{2}(\alpha)/(\alpha^{2} + \alpha + 1)`$ exists. $`\mathrm{PG}(2, \mathbb{F}_{4})`$ has
$$\text{number of points} = \text{number of lines} = 16 + 4 + 1 = \mathbf{21},$$
each line has $5$ points, each point lies on $5$ lines, and the incidence count is $21 \cdot 5 = 105$.

The projective plane $`\mathrm{PG}(2, \mathbb{F}_{4})`$ is the _unique_ projective plane of order $4$ (existence by construction, and uniqueness by [exhaustive search](https://en.wikipedia.org/wiki/Projective_plane#Finite_projective_planes)).

### 11.2. Singer Difference Set $(21, 5, 1)$

For $\mathrm{PG}(2, q)$, a [Singer cycle](https://en.wikipedia.org/wiki/Projective_linear_group#Finite_fields) is a cyclic automorphism group of order $q^{2} + q + 1$ acting regularly on points and lines. For $q = 4$, the cycle has order $21$. The Singer difference set in $\mathbb{Z}/21\mathbb{Z}$ is:
$$D = \{0,\ 1,\ 4,\ 14,\ 16\}.$$
**Verification.** Size $`|D| = 5`$. The differences $d - e$ for $d, e \in D$ (with $d \ne e$), reduced modulo $21$, are:

- $1 - 0 = 1$, $4 - 0 = 4$, $14 - 0 = 14$, $16 - 0 = 16$,
- $0 - 1 = 20$, $4 - 1 = 3$, $14 - 1 = 13$, $16 - 1 = 15$,
- $0 - 4 = 17$, $1 - 4 = 18$, $14 - 4 = 10$, $16 - 4 = 12$,
- $0 - 14 = 7$, $1 - 14 = 8$, $4 - 14 = 11$, $16 - 14 = 2$,
- $0 - 16 = 5$, $1 - 16 = 6$, $4 - 16 = 9$, $14 - 16 = 19$.

These $20$ differences cover each non-zero residue modulo $21$ exactly once. This is the $(21, 5, 1)$-difference-set property. The set $D$ generates the cyclic projective plane $\mathrm{PG}(2, 4)$ under multiplication in $\mathbb{Z}/21\mathbb{Z}$.

### 11.3. Splitting Behaviour of Primes in $\mathbb{Q}(\sqrt{21})$

For the real quadratic field $K = \mathbb{Q}(\sqrt{21})$ with fundamental discriminant $d = 21$ (squarefree, $\equiv 1 \pmod 4$), the splitting behaviour of an odd prime $p$ is determined by the Kronecker symbol:
$$\chi_{21}(p) = \left(\frac{21}{p}\right) = \left(\frac{3}{p}\right) \left(\frac{7}{p}\right).$$
The Legendre symbols can be computed through Jacobi-symbol reciprocity ([quadratic reciprocity](https://en.wikipedia.org/wiki/Quadratic_reciprocity)). The explicit list of the first few split primes is:
$$\{2,\ 5,\ 11,\ 17,\ 19,\ 23,\ 31,\ 37,\ 41,\ 71,\ 89, \ldots\}.$$
First few inert primes:
$$\{13,\ 29,\ 43,\ 47,\ 53,\ 59,\ 61,\ 67,\ 73,\ 79,\ 83,\ 97, \ldots\}.$$
By [Dirichlet's theorem on arithmetic progressions](https://en.wikipedia.org/wiki/Dirichlet%27s_theorem_on_arithmetic_progressions), the natural density of split primes is $1/2$ and the density of inert primes is $1/2$. The two ramified primes $3$ and $7$ form a null set in the density count.

### 11.4. Self-Dual Binary Code $[42, 21]$

A binary linear code $`C \subseteq \mathbb{F}_{2}^{42}`$ is self-dual if $C = C^{\perp}$ ([dual code](https://en.wikipedia.org/wiki/Dual_code)) under the standard dot product, and the dimension must equal $42/2 = 21$. A self-dual binary code of length $n$ requires $n$ to be even. For $n = 42$, this condition holds. The integer $21$ indexes the required dimension $n/2$ of such a self-dual binary code.

### 11.5. The Eisenstein Reciprocity Connection

The [cubic reciprocity law](https://en.wikipedia.org/wiki/Cubic_reciprocity) for the field $\mathbb{Q}(\sqrt{-3})$ ties the primes $3$ and $7$ through the [Eisenstein integers](https://en.wikipedia.org/wiki/Eisenstein_integer) $\mathbb{Z}[\omega]$ where $\omega = (-1 + \sqrt{-3})/2 = e^{2\pi i / 3}$.

For a prime $p \equiv 1 \pmod 3$, $p$ splits in $\mathbb{Z}[\omega]$ as $p = \pi \bar{\pi}$. The cubic residue symbol $`\left(\frac{p}{\pi}\right)_{3}`$ is defined up to multiplication by cube roots of unity.

The Eisenstein integers $\mathbb{Z}[\omega]$ form a Euclidean domain with class number $1$, with the six units $\{\pm 1, \pm\omega, \pm\omega^{2}\}$. The prime $7$ in $\mathbb{Z}[\omega]$ factors as $7 = (3 + \omega)(3 + \omega^{2})$ since $7 \equiv 1 \pmod 3$.

The factorisation $7 = (3+\omega)(3+\omega^2)$ in $\mathbb{Z}[\omega]$ together with $3 = -\omega^2(1-\omega)^2$ shows the two primes $3, 7$ that compose $21$ both factor nontrivially in the ring of Eisenstein integers.

## 12. Graph Decomposition, Simplex Edges, and Partial Sums

### 12.1. $`K_{21} = 21 \cdot K_{5}`$ through Steiner $S(2, 5, 21)$

The complete graph $`K_{21}`$ has $\binom{21}{2} = 210$ edges ([Steiner system](https://en.wikipedia.org/wiki/Steiner_system)). Each copy of $`K_{5}`$ uses $\binom{5}{2} = 10$ edges. Since $210 / 10 = 21$, exactly $21$ copies of $`K_{5}`$ partition the edges of $`K_{21}`$. The block design is a Steiner system $S(2, 5, 21)$ with parameters
$$b = 21, \quad r = 5, \quad k = 5, \quad \lambda = 1, \quad v = 21.$$

### 12.2. The $6$-Simplex has $21$ Edges

The standard $n$-simplex $\Delta^{n}$ has $n + 1$ vertices and $\binom{n+1}{2}$ edges ([simplex](https://en.wikipedia.org/wiki/Simplex)). At $n = 6$:
$$\text{number of edges of }\Delta^{6} = \binom{7}{2} = 21.$$
The $6$-simplex is the convex hull of $7$ affinely independent points in $\mathbb{R}^{7}$, with $21$ edges. It has $35$ faces of dimension $2$ (triangles), $35$ faces of dimension $3$ (tetrahedra), $21$ faces of dimension $4$ (5-cells), $7$ faces of dimension $5$ (5-simplices), and $1$ face of dimension $6$ (itself).

The face counts of $\Delta^{6}$:

- vertices: $7 = \binom{7}{1}$,
- edges: $21 = \binom{7}{2}$,
- triangles: $35 = \binom{7}{3}$,
- tetrahedra: $35 = \binom{7}{4}$,
- $5$-cells: $21 = \binom{7}{5}$,
- $6$-simplices: $7 = \binom{7}{6}$,
- the $6$-simplex itself: $1 = \binom{7}{7}$.

The $21$ appears twice in the face-count list (edges and 5-cells), reflecting the symmetry $\binom{n}{k} = \binom{n}{n-k}$.

### 12.3. Jacobsthal Partial Sum at Index $5$

The Jacobsthal numbers satisfy $J(n) = J(n-1) + 2 J(n-2)$ with $J(0) = 0$ and $J(1) = 1$ ([Jacobsthal number](https://en.wikipedia.org/wiki/Jacobsthal_number)):
$$J = 0, 1, 1, 3, 5, 11, 21, 43, 85, \ldots$$
The partial sums are
$$S_{J}(n) = \sum_{i=0}^{n} J(i).$$
By the recurrence $J(n) = J(n-1) + 2 J(n-2)$, the generating function of $J$ is
$$\sum_{n=0}^{\infty} J(n) x^{n} = \frac{x}{(1 - x)(1 - 2x)},$$
and
$$\sum_{n=0}^{\infty} S_{J}(n) x^{n} = \frac{x}{(1 - x)^{2}(1 - 2x)}.$$
At $x = 1$ (formal), the partial sums grow as $`S_{J}(n) = 2^{n+1} - n - 3`$ approximately. At $n = 5$:
$$S_{J}(5) = 0 + 1 + 1 + 3 + 5 + 11 = 21.$$
The next partial sum:
$$S_{J}(6) = 21 + 21 = 42 = 2 \cdot 21,$$
doubling relation as $`C_{5} = 2 \cdot 21`$.

### 12.4. The Convergent $`h_{5}/k_{5} = 55/12`$ of $\sqrt{21}$

The continued fraction $\sqrt{21} = [4; \overline{1, 1, 2, 1, 1, 8}]$ has period $r = 6$ ([continued fraction](https://en.wikipedia.org/wiki/Continued_fraction)). The convergents $`h_{n}/k_{n}`$ are computed recursively:
Using the recurrence $`h_{n} = a_{n} h_{n-1} + h_{n-2}`$ and $`k_{n} = a_{n} k_{n-1} + k_{n-2}`$ with initial conditions $`h_{-1} = 1, h_{-2} = 0, k_{-1} = 0, k_{-2} = 1`$:

- $`h_{0} = 4, k_{0} = 1`$
- $`h_{1} = 5, k_{1} = 1`$
- $`h_{2} = 9, k_{2} = 2`$
- $`h_{3} = 23, k_{3} = 5`$
- $`h_{4} = 32, k_{4} = 7`$
- $`h_{5} = 55, k_{5} = 12`$

The fifth convergent is $`h_{5}/k_{5} = 55/12`$, satisfying $55^{2} - 21 \cdot 12^{2} = 3025 - 3024 = 1$. This is the fundamental solution of [Pell's equation](https://en.wikipedia.org/wiki/Pell%27s_equation).

### 12.5. The $k - n = 2$ Structural Relation

Among the solutions of [Luo Ming, Fibonacci Quarterly 27.2 (1989)](https://www.fq.math.ca/Scanned/27-2/ming.pdf) with $`T(n) = F_{k}`$ and $`n(n+1)/2 = F_{k}`$:

- $(n, k) = (1, 1)$, $k - n = 0$,
- $(n, k) = (2, 4)$, $k - n = 2$,
- $(n, k) = (6, 8)$, $k - n = 2$,
- $(n, k) = (10, 10)$, $k - n = 0$.

The difference $k - n = 2$ occurs only at $n = 2$ and $n = 6$. The relation $k = n + 2$ therefore holds at the two nontrivial solutions of [Luo](https://www.fq.math.ca/Scanned/27-2/ming.pdf), namely $T(2) = 3$ and $T(6) = 21$.

The case $(n, k) = (6, 8)$ is unique among Fibonacci-triangular [semiprimes](https://en.wikipedia.org/wiki/Semiprime) because $21 = 3 \cdot 7$ has both prime factors congruent to $3$ modulo $4$. The integer $55 = 5 \cdot 11$ does not share that property.

### 12.6. $21$ Is the Smallest Composite with $\sigma(n)=2^{k}$

The [sum-of-divisors function](https://en.wikipedia.org/wiki/Divisor_function) $\sigma$ is multiplicative, with $\sigma(p^a) = 1 + p + p^2 + \cdots + p^a$. For distinct primes $p, q$,
$$\sigma(pq) = (1+p)(1+q).$$
For $\sigma(pq) = 2^k$, both $1+p$ and $1+q$ must be powers of $2$. This means $p$ and $q$ are **Mersenne primes**: $p = 2^{a} - 1$, $q = 2^{b} - 1$ with $a, b \ge 2$.

The first Mersenne primes include $3 = 2^{2}-1$, $7 = 2^{3}-1$, $31 = 2^{5}-1$, $127 = 2^{7}-1$, and $8191 = 2^{13}-1$ ([Mersenne prime](https://en.wikipedia.org/wiki/Mersenne_prime)).

The smallest product of two distinct [Mersenne primes](https://en.wikipedia.org/wiki/Mersenne_prime) is
$$M_2 \cdot M_3 \;=\; 3 \cdot 7 \;=\; \mathbf{21}.$$
This is therefore the smallest composite $n$ with $\sigma(n)$ a power of $2$. The next displayed composites of this form are $3 \cdot 31 = 93$ with $\sigma = 128 = 2^{7}$, $7 \cdot 31 = 217$ with $\sigma = 256 = 2^{8}$, and $3 \cdot 127 = 381$ with $\sigma = 512 = 2^{9}$.

**Verification of $21$:** $\sigma(21) = 1 + 3 + 7 + 21 = 32 = 2^5$.

**General formula.** If $`p = M_a = 2^a - 1`$ and $`q = M_b = 2^b - 1`$ are [Mersenne primes](https://en.wikipedia.org/wiki/Mersenne_prime) with $a \le b$, then
$$\sigma(pq) = 2^a \cdot 2^b \;=\; 2^{a+b}.$$
For $a = 2$ and $b = 3$: $\sigma(21) = 2^{2+3} = 2^5 = 32$.

### 12.7. Smallest $`n>1`$ in the Triangular, Fibonacci, Motzkin, and Squarefree-Semiprime Intersection

This intersection is computed directly from the Luo list $\{0, 1, 3, 21, 55\}$ of triangular Fibonacci numbers ([Luo Ming, Fibonacci Quarterly 27.2 (1989)](https://www.fq.math.ca/Scanned/27-2/ming.pdf)), plus the Motzkin sequence $`M_n = 1, 1, 2, 4, 9, 21, 51, 127, \ldots`$ ([Motzkin number](https://en.wikipedia.org/wiki/Motzkin_number)), plus the squarefree semiprimes, which are products of two distinct primes ([semiprime](https://en.wikipedia.org/wiki/Semiprime)).

- $n = 0$: degenerate, not a [Motzkin number](https://en.wikipedia.org/wiki/Motzkin_number).
- $n = 1$: trivial [semiprime](https://en.wikipedia.org/wiki/Semiprime), but in a degenerate case.
- $n = 3$: prime, not a semiprime.
- $n = 21$: $`T(6) = F_8 = M_5 = 3 \cdot 7`$. All four properties hold.
- $n = 55$: $`T(10) = F_{10} = 5 \cdot 11`$. But $55$ is not a Motzkin number, since $`M_n`$ for $n \ge 0$ never equals $55$.

Therefore $21$ is the unique smallest $`n > 1`$ in this four-way intersection of the [Luo list](https://www.fq.math.ca/Scanned/27-2/ming.pdf), the [Motzkin numbers](https://en.wikipedia.org/wiki/Motzkin_number), and the [squarefree semiprimes](https://en.wikipedia.org/wiki/Semiprime). The next such number was not found below $10^6$, since both lists grow exponentially while the intersection is rare.

### 12.8. $21$ Has $4$ Representations as a Sum of Consecutive Positive Integers

A classical result attributed to [Fibonacci's _Liber Abaci_](https://en.wikipedia.org/wiki/Liber_Abaci): _the number of ways to write $n$ as a sum of consecutive positive integers equals the number of odd divisors of $n$._

The odd divisors of $21$ are $\{1, 3, 7, 21\}$, giving $4$ representations:

| Odd divisor $d$ | Length $k$ | Representation          |
| --------------: | ---------: | ----------------------- |
|             $1$ |        $1$ | $21$                    |
|             $3$ |        $3$ | $6 + 7 + 8$             |
|             $7$ |        $6$ | $1 + 2 + 3 + 4 + 5 + 6$ |
|            $21$ |        $2$ | $10 + 11$               |

The four representations match the four odd divisors, as stated in the classical formula.
