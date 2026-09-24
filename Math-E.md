# Mathematical Derivations, continued

Parts: [A](Math-A.md), [B](Math-B.md), [C](Math-C.md), [D](Math-D.md), [E](Math-E.md).

## 13. Sporadic Group Orders and Triangular Decomposition

### 13.1. The $2$-adic Valuations $`v_{2}(|Co_{1}|)=v_{2}(|Fi_{24}^{\prime}|)=21`$

The Conway group $`Co_1`$ ([Conway group Co1](https://en.wikipedia.org/wiki/Conway_group_Co1)) has order
$$|Co_1| \;=\; 2^{21} \cdot 3^{9} \cdot 5^{4} \cdot 7^{2} \cdot 11 \cdot 13 \cdot 23.$$
This factors as
$$|Co_1| \;=\; 4\,157\,776\,806\,543\,360\,000.$$
The $2$-adic valuation of this order is exactly $21$:
$$v_2(|Co_1|) \;=\; 21.$$
Direct verification:
$$|Co_1| / 2^{21} \;=\; \frac{4\,157\,776\,806\,543\,360\,000}{2\,097\,152} \;=\; 1\,982\,582\,476\,875,$$
which is odd, and in fact divisible by $3, 5, 7, 11, 13, 23$. Therefore $`v_2(|Co_1|) = 21`$ is verified.

The [Fischer group](https://en.wikipedia.org/wiki/Fischer_group) $`Fi_{24}'`$ (the derived subgroup of $`Fi_{24}`$) has order
$$|Fi_{24}'| \;=\; 2^{21} \cdot 3^{16} \cdot 5^{2} \cdot 7^{3} \cdot 11 \cdot 13 \cdot 17 \cdot 23 \cdot 29.$$
This also has $`v_2 = 21`$. The verification follows the same structure.

Among the $26$ sporadic simple groups ([sporadic group](https://en.wikipedia.org/wiki/Sporadic_group)), only $`Co_1`$ and $`Fi_{24}'`$ have $`v_2(|G|) = 21`$. The other sporadic groups have $`v_2(|G|) \in \{3, 6, 7, 8, 9, 10, 14, 15, 17, 18, 41, 46\}`$. Notably:

| Group                         | $`v_2(\lvert G\rvert)`$ |
| ----------------------------- | ----------------------: |
| $`M_{11}`$                    |                     $6$ |
| $`M_{12}`$                    |                     $6$ |
| $`J_1`$                       |                     $3$ |
| McL                           |                     $7$ |
| $HS$                          |                     $9$ |
| $`Fi_{22}`$                   |                    $17$ |
| $`Fi_{23}`$                   |                    $18$ |
| $`\mathbf{Fi_{24}^{\prime}}`$ |           $\mathbf{21}$ |
| $`Co_1`$                      |           $\mathbf{21}$ |
| $`Co_2`$                      |                    $18$ |
| $`Co_3`$                      |                    $10$ |
| $HN$                          |                    $14$ |
| $Th$                          |                    $15$ |
| $B$                           |                    $41$ |
| $M$                           |                    $46$ |

**Connection to $21 = 3 \cdot 7$.** The order of $`Co_1`$ has the structure $`|Co_1| = 2^{21} \cdot 3^9 \cdot 7^2 \cdot (\text{other primes})`$. Therefore $21 = 3 \cdot 7$ divides $`|Co_1|`$, with $3^9$ and $7^2$ as separate factors. The $2$-adic valuation $21$ encodes $21$ as the largest power of $2$ dividing the group order. The largest $2$-power, $2^{21}$, is itself a nontrivial object.

The connection to the central node is two-fold:

1. $21$ divides $`|Co_1|`$ (the order has $21$ as a factor).
2. $`21 = v_2(|Co_1|)`$ (the $2$-adic valuation equals $21$).

These are **independent facts** about the same number.

### 13.2. The Sylow Structure of $`Co_{1}`$

The order $`|Co_1| = 2^{21} \cdot 3^9 \cdot 5^4 \cdot 7^2 \cdot 11 \cdot 13 \cdot 23`$ has the following Sylow consequences ([Sylow theorems](https://en.wikipedia.org/wiki/Sylow_theorems)):

- A [Sylow](https://en.wikipedia.org/wiki/Sylow_theorems) $2$-subgroup has order $2^{21}$.
- A Sylow $7$-subgroup has order $7^2 = 49$.
- The number of Sylow $7$-subgroups is congruent to $1$ modulo $7$ and divides $`|Co_1|/49`$.

The exponent $`v_7(|Co_1|) = 2`$ (not cubed or higher) means $`Co_1`$ contains elements of order $49$ but not $343$.

### 13.3. Uniqueness of $`21=T_{3}+T_{5}`$ as a Sum of Two Triangular Numbers

By [Gauss's Eureka theorem](https://en.wikipedia.org/wiki/Eureka_theorem), every positive integer is a sum of at most three triangular numbers. For $N = 21$, the unique nontrivial pair $`(T_a, T_b)`$ with $`1 \le a < b`$ and $`T_a + T_b = 21`$ is:
$$21 \;=\; T_3 + T_5 \;=\; 6 + 15.$$
**Proof by direct enumeration.** The equation $`T_a + T_b = 21`$ is equivalent to $a(a+1) + b(b+1) = 42$ with $`1 \leq a < b`$. Checking $a \in \{1, 2, 3, 4\}$:

| $a$ | $b(b+1) = 42 - a(a+1)$ |                              Integer $b$? |
| --: | ---------------------: | ----------------------------------------: |
| $1$ |                   $40$ |                    No ($6 \times 7 = 42$) |
| $2$ |                   $36$ | No ($5 \times 6 = 30$, $6 \times 7 = 42$) |
| $3$ |                   $30$ |                               $b = 5$ yes |
| $4$ |                   $22$ | No ($4 \times 5 = 20$, $5 \times 6 = 30$) |

Therefore $(a, b) = (3, 5)$ is the unique solution, giving $`21 = T_3 + T_5 = 6 + 15`$.

**Remark.** The pair $(3, 5)$ satisfies $`3 + 5 = 8 = F_6`$ and $`3 \cdot 5 = 15 = T_5`$. The general identity $`T_n = T_a + T_b`$ requires $n(n+1) = a(a+1) + b(b+1)$.

## 14. Euler Characteristic of $\mathbb{CP}^{20}$ and Additional Intersections

### 14.1. Euler Characteristic of $\mathbb{CP}^{20}$ equals $21$

The complex projective space $\mathbb{CP}^{n}$ is the quotient of $\mathbb{C}^{n+1} \setminus \{0\}$ by $\mathbb{C}^{\times}$ ([complex projective space](https://en.wikipedia.org/wiki/Complex_projective_space)). It has complex dimension $n$, real dimension $2n$. The cohomology ring is
$$H^{*}(\mathbb{CP}^{n}; \mathbb{Z}) = \mathbb{Z}[x]/(x^{n+1}), \quad \deg x = 2.$$
The Betti numbers are
$$b_{2k}(\mathbb{CP}^{n}) = 1 \quad \text{for } 0 \le k \le n, \qquad b_{j}(\mathbb{CP}^{n}) = 0 \text{ otherwise}.$$
The Euler characteristic is
$$\chi(\mathbb{CP}^{n}) = \sum_{k=0}^{n} b_{2k} = n + 1.$$
At $n = 20$:
$$\chi(\mathbb{CP}^{20}) = 21.$$
The space $\mathbb{CP}^{20}$ has $21$ nontrivial even-degree cohomology groups, each $\mathbb{Z}$, with $21$ Betti numbers summing to $21$.

### 14.2. Two Groups of Order $21$

The number of groups of order $n$ is tabulated in [OEIS A000001](https://oeis.org/A000001). For $n \le 30$ the values are
$$1, 1, 1, 2, 1, 2, 1, 5, 2, 2, 1, 5, 1, 2, 1, 14, 1, 5, 1, 5, \mathbf{2}, 2, 1, 15, 2, 2, 5, 4, 1, 4.$$
At $n = 21$, the count is exactly $2$:

1. **Cyclic group** $`C_{21} = \mathbb{Z}/21\mathbb{Z}`$ (abelian).
2. **Frobenius group** $`F_{21} = \mathbb{Z}/7\mathbb{Z} \rtimes \mathbb{Z}/3\mathbb{Z}`$ (non-abelian).

The non-trivial action of $\mathbb{Z}/3$ on $\mathbb{Z}/7$ uses the cubic roots of unity modulo $7$, namely $k \in \{2, 4\}$ (since $k^3 \equiv 1 \pmod 7$). Choosing $k = 2$ gives $a b a^{-1} = b^2$, whose orbit of $b$ is $\{b, b^2, b^4\}$ (order $3$, consistent with $`|a| = 3`$). The choice $k = 4$ gives the isomorphic group with $a b a^{-1} = b^4$.

**Conjugacy classes.** $`F_{21}`$ has exactly $5$ conjugacy classes, of sizes $1, 3, 3, 7, 7$:

- $\{1\}$ (identity),
- $\{b, b^2, b^4\}$ and $\{b^3, b^5, b^6\}$ (orbits of $\mathbb{Z}/7 \setminus \{1\}$ under $a$),
- $\{(b^i, a) : i \in \mathbb{Z}/7\}$ and $\{(b^i, a^2) : i \in \mathbb{Z}/7\}$ (size $7$ each).

**Irreducible representations.** The $5$ irreps have dimensions $1, 1, 1, 3, 3$, satisfying $`\sum d_i^2 = 1 + 1 + 1 + 9 + 9 = 21 = |F_{21}|`$:

- Two linear reps from the abelian quotient $`F_{21} \to \mathbb{Z}/3`$ (trivial and sign of $\mathbb{Z}/3$).
- One linear rep from the trivial character of the normal subgroup $\mathbb{Z}/7$.
- Two degree-$3$ irreps from the induced representations $`\mathrm{Ind}_{\mathbb{Z}/7}^{F_{21}}(\text{trivial})`$ and $`\mathrm{Ind}_{\mathbb{Z}/7}^{F_{21}}(\text{sign})`$.

## Sources

Each link supports the sentence that cites it. A substitution is not a discovery claimed by the cited source.

- Fundamental discriminant: [Wikipedia](https://en.wikipedia.org/wiki/Fundamental_discriminant)
- Binary quadratic form and form class number: [Wikipedia](https://en.wikipedia.org/wiki/Binary_quadratic_form)
- Dirichlet class-number formula, including the imaginary case for a fundamental discriminant: [Wikipedia](https://en.wikipedia.org/wiki/Class_number_formula)
- Padovan sequence: [Wikipedia](https://en.wikipedia.org/wiki/Padovan_sequence)
- Narayana number: [Wikipedia](https://en.wikipedia.org/wiki/Narayana_number)
- Catalan number: [Wikipedia](https://en.wikipedia.org/wiki/Catalan_number)
- Aliquot sequence: [Wikipedia](https://en.wikipedia.org/wiki/Aliquot_sequence)
- Harshad number: [Wikipedia](https://en.wikipedia.org/wiki/Harshad_number)
- Kempner function, also called the Smarandache function: [Wikipedia](https://en.wikipedia.org/wiki/Kempner_function)
- Dedekind psi function: [Wikipedia](https://en.wikipedia.org/wiki/Dedekind_psi_function)
- Jacobi's four-square theorem: [Wikipedia](https://en.wikipedia.org/wiki/Jacobi%27s_four-square_theorem)
- Fano plane: [Wikipedia](https://en.wikipedia.org/wiki/Fano_plane)
- Ramanujan tau function: [Wikipedia](https://en.wikipedia.org/wiki/Ramanujan_tau_function)
- Grassmannian: [Wikipedia](https://en.wikipedia.org/wiki/Grassmannian)
- Plücker embedding: [Wikipedia](https://en.wikipedia.org/wiki/Pl%C3%BCcker_embedding)
- Orthogonal group, including the dimension of the special orthogonal Lie algebra: [Wikipedia](https://en.wikipedia.org/wiki/Orthogonal_group)
- Symplectic group: [Wikipedia](https://en.wikipedia.org/wiki/Symplectic_group)
- Siegel modular variety: [Wikipedia](https://en.wikipedia.org/wiki/Siegel_modular_variety)
- Modular curve: [Wikipedia](https://en.wikipedia.org/wiki/Modular_curve)
- Centered polygonal number: [Wikipedia](https://en.wikipedia.org/wiki/Centered_polygonal_number)
- Central polygonal numbers $n^{2}-n+1$: [OEIS A002061](https://oeis.org/A002061)
- Lazy caterer's sequence: [Wikipedia](https://en.wikipedia.org/wiki/Lazy_caterer%27s_sequence), and sequence [OEIS A000124](https://oeis.org/A000124)
- Centered hexagonal number: [Wikipedia](https://en.wikipedia.org/wiki/Centered_hexagonal_number), and sequence [OEIS A003215](https://oeis.org/A003215)
- Triangle group: [Wikipedia](https://en.wikipedia.org/wiki/Triangle_group)
- Coxeter group: [Wikipedia](https://en.wikipedia.org/wiki/Coxeter_group)
- Klein quartic: [Wikipedia](https://en.wikipedia.org/wiki/Klein_quartic)
- Hurwitz automorphism theorem: [Wikipedia](https://en.wikipedia.org/wiki/Hurwitz%27s_automorphism_theorem)
- Cyclotomic polynomial: [Wikipedia](https://en.wikipedia.org/wiki/Cyclotomic_polynomial)
- Hilbert polynomial: [Wikipedia](https://en.wikipedia.org/wiki/Hilbert_polynomial)
- Chinese remainder theorem: [Wikipedia](https://en.wikipedia.org/wiki/Chinese_remainder_theorem)
- Projective plane, including $q^{2}+q+1$ points: [Wikipedia](https://en.wikipedia.org/wiki/Projective_plane)
- Singer cycle: [Wikipedia](https://en.wikipedia.org/wiki/Projective_linear_group#Finite_fields)
- Steiner system: [Wikipedia](https://en.wikipedia.org/wiki/Steiner_system)
- Simplex: [Wikipedia](https://en.wikipedia.org/wiki/Simplex)
- Jacobsthal number: [Wikipedia](https://en.wikipedia.org/wiki/Jacobsthal_number)
- Mersenne prime: [Wikipedia](https://en.wikipedia.org/wiki/Mersenne_prime)
- Cubic reciprocity: [Wikipedia](https://en.wikipedia.org/wiki/Cubic_reciprocity)
- Eisenstein integer: [Wikipedia](https://en.wikipedia.org/wiki/Eisenstein_integer)
- Dirichlet's theorem on arithmetic progressions: [Wikipedia](https://en.wikipedia.org/wiki/Dirichlet%27s_theorem_on_arithmetic_progressions)
- Dual code: [Wikipedia](https://en.wikipedia.org/wiki/Dual_code)
- Complex projective space and its Euler characteristic: [Wikipedia](https://en.wikipedia.org/wiki/Complex_projective_space)
- Number of groups of order $n$: [OEIS A000001](https://oeis.org/A000001)
- Elliptic curve: [Wikipedia](https://en.wikipedia.org/wiki/Elliptic_curve)
- Conway group $`Co_1`$: [Wikipedia](https://en.wikipedia.org/wiki/Conway_group_Co1)
- Fischer group: [Wikipedia](https://en.wikipedia.org/wiki/Fischer_group)
- Sporadic group: [Wikipedia](https://en.wikipedia.org/wiki/Sporadic_group)
- Sylow theorems: [Wikipedia](https://en.wikipedia.org/wiki/Sylow_theorems)
- Gauss's Eureka theorem: [Wikipedia](https://en.wikipedia.org/wiki/Eureka_theorem)
- Pell-like trace sequence at $5$: [OEIS A005247](https://oeis.org/A005247)
- Triality: [Wikipedia](https://en.wikipedia.org/wiki/Triality)
- Octonion: [Wikipedia](https://en.wikipedia.org/wiki/Octonion)
- Sum of two squares theorem: [Wikipedia](https://en.wikipedia.org/wiki/Sum_of_two_squares_theorem)
- Quadratic reciprocity: [Wikipedia](https://en.wikipedia.org/wiki/Quadratic_reciprocity)
- Genus-degree formula: [Wikipedia](https://en.wikipedia.org/wiki/Genus%E2%80%93degree_formula)
- Ramanujan congruence: [Ramanujan's congruence](https://en.wikipedia.org/wiki/Ramanujan%27s_congruence)
- Root system: [Wikipedia](https://en.wikipedia.org/wiki/Root_system)
- Sum-of-divisors function: [Wikipedia](https://en.wikipedia.org/wiki/Divisor_function)
- Euler's totient function: [Wikipedia](https://en.wikipedia.org/wiki/Euler%27s_totient_function)

## License

This repository is Licensed under [CC BY 4.0](LICENSE).
