# Mathematical Derivations

$\Lambda(n)$ and Manifestations of $\Lambda(6) = 1/\sqrt{21}$

Continued in [part B](Math-B.md), [part C](Math-C.md), [part D](Math-D.md), and [part E](Math-E.md).

## 1. Algebraic and Analytical Foundations of $\Lambda(n)$

### 1.1. Discrete Evaluation

Fundamental formula:
$$\Lambda(n) = \sqrt{\frac{2}{n(n+1)}} = \frac{1}{\sqrt{T(n)}}, \quad n \in \mathbb{N}_{>0}$$

For index $n = 6$:

1. The sixth [triangular number](https://en.wikipedia.org/wiki/Triangular_number):
   $$T(6) = \frac{6(6+1)}{2} = \frac{42}{2} = 21$$
2. Substitution into the formula:
   $$\Lambda(6) = \sqrt{\frac{2}{6(7)}} = \sqrt{\frac{2}{42}} = \sqrt{\frac{1}{21}} = \frac{1}{\sqrt{21}}$$
3. High-precision numerical evaluation:
   $$\Lambda(6) = 0.2182178902359923812660974854156\ldots$$
   $$100 \cdot \Lambda(6) = 21.82178902359923812660974854156\ldots$$

### 1.2. Partial Fraction Decomposition and Telescoping Sum

Given $\Lambda(n)^{2} = \frac{2}{n(n+1)}$, the decomposition is the standard [partial fraction](https://en.wikipedia.org/wiki/Partial_fraction_decomposition) decomposition:

1. Partial fraction decomposition:
   $$\frac{2}{n(n+1)} = \frac{A}{n} + \frac{B}{n+1} \implies 2 = A(n+1) + Bn$$
   Setting $n = 0$ gives $A = 2$. Setting $n = -1$ gives $B = -2$.
   $$\Lambda(n)^{2} = 2\left(\frac{1}{n} - \frac{1}{n+1}\right)$$
2. Summation up to upper limit $N$:
   $$\sum_{n=1}^{N} \Lambda(n)^{2} = 2 \sum_{n=1}^{N} \left(\frac{1}{n} - \frac{1}{n+1}\right) = 2\left[\left(1 - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{3}\right) + \cdots + \left(\frac{1}{N} - \frac{1}{N+1}\right)\right]$$
3. Telescoping cancellation of all intermediate terms:
   $$\sum_{n=1}^{N} \Lambda(n)^{2} = 2\left(1 - \frac{1}{N+1}\right) = \frac{2N}{N+1}$$
4. Convergence in the limit as $N \to \infty$:
   $$\lim_{N \to \infty} \sum_{n=1}^{N} \Lambda(n)^{2} = \lim_{N \to \infty} \frac{2N}{N+1} = 2$$

### 1.3. Generating Function of Squared Terms $G(z)$

Power series definition:
$$G(z) = \sum_{n=1}^\infty \Lambda(n)^{2} z^{n} = 2 \sum_{n=1}^\infty \left(\frac{1}{n} - \frac{1}{n+1}\right) z^{n}, \quad \lvert z\rvert < 1$$

1. Splitting the series:
   $$G(z) = 2 \sum_{n=1}^\infty \frac{z^{n}}{n} - \frac{2}{z} \sum_{n=1}^\infty \frac{z^{n+1}}{n+1}$$
2. Mercator series for $-\ln(1-z)$ ([Mercator series](https://en.wikipedia.org/wiki/Mercator_series)):
   $$\sum_{n=1}^\infty \frac{z^{n}}{n} = -\ln(1-z)$$
   $$\sum_{n=1}^\infty \frac{z^{n+1}}{n+1} = \sum_{k=2}^\infty \frac{z^{k}}{k} = -\ln(1-z) - z$$
3. Substitution and algebraic simplification:
   $$G(z) = -2\ln(1-z) - \frac{2}{z}\left(-\ln(1-z) - z\right) = -2\ln(1-z) + \frac{2\ln(1-z)}{z} + 2$$
   $$G(z) = 2 + \frac{2(1-z)\ln(1-z)}{z}$$

### 1.4. Continuous Generalization through the Euler Beta and Gamma Functions

1. Definition of the Euler Beta function $B(x, y) = \frac{\Gamma(x)\Gamma(y)}{\Gamma(x+y)}$ ([Beta function](https://en.wikipedia.org/wiki/Beta_function) and [Gamma function](https://en.wikipedia.org/wiki/Gamma_function)):
   Setting parameter $y = 2$:
   $$B(x, 2) = \frac{\Gamma(x)\Gamma(2)}{\Gamma(x+2)} = \frac{\Gamma(x) \cdot 1!}{(x+1)x\,\Gamma(x)} = \frac{1}{x(x+1)}$$
2. Continuous representation:
   $$\Lambda(x) = \sqrt{2\,B(x, 2)} = \sqrt{\frac{2\,\Gamma(x)}{\Gamma(x+2)}} = \sqrt{\frac{2}{x(x+1)}}, \quad x > 0$$
3. Derivation of the logarithmic derivative $\frac{d}{dx} \ln \Lambda(x)$:
   $$\ln \Lambda(x) = \frac{1}{2}\ln 2 - \frac{1}{2}\ln x - \frac{1}{2}\ln(x+1)$$
   $$\frac{d}{dx} \ln \Lambda(x) = -\frac{1}{2x} - \frac{1}{2(x+1)}$$

## 2. Ten Combinatorial Evaluations of 21

The integer $21$ has the ten evaluations below. They are not independent counts: $T(6)=\binom{7}{2}$, and both Stirling evaluations equal that binomial coefficient by the identities $S(n,n-1)=c(n,n-1)=\binom{n}{2}$ ([unsigned Stirling numbers of the first kind](https://en.wikipedia.org/wiki/Stirling_numbers_of_the_first_kind) and [Stirling numbers of the second kind](https://en.wikipedia.org/wiki/Stirling_numbers_of_the_second_kind)).

1. Triangular Number ($`T_{6}`$)
   $$T(6) = \frac{6 \times 7}{2} = 21$$
2. Binomial Coefficient $\binom{7}{2}$
   $$\binom{7}{2} = \frac{7!}{2!\,5!} = \frac{7 \times 6}{2} = 21$$
3. Octagonal Number ($`O_{3}`$)
   The $s$-gonal formula is $P(s,n)=((s-2)n^{2}-(s-4)n)/2$ ([polygonal number](https://en.wikipedia.org/wiki/Polygonal_number)). For $s=8$:
   $$P(8,3) = 3(3\cdot 3-2) = 21$$
4. Icosihenagonal (21-gonal) Number ($`I_{21}(2)`$)
   $$P(21, 2) = \frac{19(2^{2}) - 17(2)}{2} = \frac{76 - 34}{2} = 21$$
5. Fibonacci Number ($`F_{8}`$)
   With $`F_{0}=0`$ and $`F_{1}=1`$ ([Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_sequence)):
   $$F_{0}=0, F_{1}=1, F_{2}=1, F_{3}=2, F_{4}=3, F_{5}=5, F_{6}=8, F_{7}=13, F_{8}=21$$
6. Stirling Number of the Second Kind $S(7, 6)$
   $$S(n, n-1) = \binom{n}{2} \implies S(7, 6) = \binom{7}{2} = 21$$
7. Unsigned Stirling Number of the First Kind $c(7, 6)$
   $$c(n, n-1) = \binom{n}{2} \implies c(7, 6) = \binom{7}{2} = 21$$
8. Motzkin Number ($`M_{5}`$)
   The recurrence is $`M_{n} = M_{n-1} + \sum_{i=0}^{n-2} M_{i} M_{n-2-i}`$, and the sequence begins $1,1,2,4,9,21$ ([Motzkin number](https://en.wikipedia.org/wiki/Motzkin_number)):
   $$M_{0}=1, M_{1}=1, M_{2}=2, M_{3}=4, M_{4}=9, M_{5}=21$$
9. Standard Young Tableaux $f^{(3,3,1)}$ (Hook Length Formula)
   $$f^\lambda = \frac{n!}{\prod h_{\lambda}(i,j)}$$
   ([hook-length formula](https://en.wikipedia.org/wiki/Hook-length_formula))
   For partition $\lambda = (3,3,1)$ with $n = 7$:
   - Row 1 hook lengths: $(5, 3, 2)$
   - Row 2 hook lengths: $(4, 2, 1)$
   - Row 3 hook lengths: $(1)$
     $$\prod h_{(i,j)} = 5 \times 3 \times 2 \times 4 \times 2 \times 1 \times 1 = 240 \implies f^{(3,3,1)} = \frac{7!}{240} = \frac{5040}{240} = 21$$
10. Standard Young Tableaux $f^{(3,2,2)}$
    For partition $\lambda = (3,2,2)$ with $n = 7$:
    - Row 1 hook lengths: $(5, 4, 1)$
    - Row 2 hook lengths: $(3, 2)$
    - Row 3 hook lengths: $(2, 1)$
      $$\prod h_{(i,j)} = 5 \times 4 \times 1 \times 3 \times 2 \times 2 \times 1 = 240 \implies f^{(3,2,2)} = \frac{5040}{240} = 21$$

## 3. Derivations in Analytic Number Theory

### 3.1. Quadratic Gauss Sum $`g(\chi_{21})`$

The Kronecker page identifies the real primitive character of discriminant $21$ by $`\chi_{21}(n)=\left(\frac{21}{n}\right)`$, with conductor $`|D|=21`$ ([Kronecker symbol](https://en.wikipedia.org/wiki/Kronecker_symbol)). Because the odd part of $21$ is $1 \pmod 4$, that page also gives $\left(\frac{\cdot}{21}\right)=\left(\frac{21}{\cdot}\right)$. Its factorization into odd Legendre symbols is the Jacobi definition ([Jacobi symbol](https://en.wikipedia.org/wiki/Jacobi_symbol)):
$$\chi_{21}(n)=\left(\frac{21}{n}\right)=\left(\frac{3}{n}\right)\left(\frac{7}{n}\right)$$
$$g(\chi_{21}) = \sum_{n=0}^{20} \chi_{21}(n)\, e^{2\pi i n/21}$$

1. The equality $\lvert g(\chi)\rvert=\sqrt{N}$ requires a primitive character, equivalently conductor equal to modulus ([Gauss sum](https://en.wikipedia.org/wiki/Gauss_sum) and [Dirichlet character](https://en.wikipedia.org/wiki/Dirichlet_character)). Being square-free does not by itself prove primitivity. The conductor statement above supplies that hypothesis, so $`\lvert g(\chi_{21})\rvert=\sqrt{21}`$. For coprime moduli, the Gauss-sum page includes the phase $\chi(N')\chi'(N)$. Here $`\chi_3(7)\chi_7(3)=-1`$:
   $$g(\chi_{21}) = \chi_{3}(7)\chi_{7}(3)\,g(\chi_{3})g(\chi_{7}) = -g(\chi_{3})g(\chi_{7}).$$
2. Modulus square of primitive real Dirichlet characters modulo prime $p$:
   $$\lvert g(\chi_{p})\rvert^{2} = p \implies \lvert g(\chi_{3})\rvert^{2} = 3, \quad \lvert g(\chi_{7})\rvert^{2} = 7$$
3. Product of moduli:
   $$\lvert g(\chi_{21})\rvert^{2} = 3 \times 7 = 21 \implies \lvert g(\chi_{21})\rvert = \sqrt{21}$$
   $$\Lambda(6) = \frac{1}{\lvert g(\chi_{21})\rvert} = \frac{1}{\sqrt{21}}$$

### 3.2. Dirichlet Class Number Formula

For the real quadratic field $\mathbb{Q}(\sqrt{21})$:

- Fundamental discriminant $d = 21$ ($21 \equiv 1 \pmod 4$)
- Fundamental unit $`\varepsilon_{21} = (5 + \sqrt{21})/2`$, of norm $+1$, since $5^{2} - 21\cdot 1^{2} = 4$. The continued fraction of $\sqrt{21}$ is $[4;\overline{1,1,2,1,1,8}]$, so the repeating block has length $6$ and the period is $r=6$. Counting from the initial term, the sixth convergent, written $`h_{5}/k_{5}`$, is $55/12$, and $55^{2}-21\cdot 12^{2}=1$. Because $r$ is even, the fundamental-solution rule selects convergent index $r-1=5$, which is the same fraction ([continued fraction](https://en.wikipedia.org/wiki/Continued_fraction)). The solution is the cube of the unit: $`\varepsilon_{21}^{3}=55+12\sqrt{21}`$ ([Pell's equation](https://en.wikipedia.org/wiki/Pell%27s_equation)). The class-number formula uses $`\ln \varepsilon_{21}`$, not $\ln(55 + 12\sqrt{21})$, which is three times as large ([class number formula](https://en.wikipedia.org/wiki/Class_number_formula) and [fundamental unit](https://en.wikipedia.org/wiki/Fundamental_unit_%28number_theory%29)).
- Class number $h(21) = 1$ ([class-number-one fields](https://en.wikipedia.org/wiki/List_of_number_fields_with_class_number_one)). In the formula below, $`\chi_{21}(m)=\left(\frac{21}{m}\right)`$ is the same character as in section 3.1 ([class number formula](https://en.wikipedia.org/wiki/Class_number_formula)).

The [analytic Dirichlet class number formula](https://en.wikipedia.org/wiki/Class_number_formula) is:
$$h(d) = \frac{\sqrt{d}}{2\ln \varepsilon_{d}} L(1, \chi_{d})$$
Substituting $h(21) = 1$:
$$1 = \frac{\sqrt{21}}{2\ln \left(\frac{5+\sqrt{21}}{2}\right)} L(1, \chi_{21}) \implies \frac{1}{\sqrt{21}} = \frac{L(1, \chi_{21})}{2\ln \left(\frac{5+\sqrt{21}}{2}\right)} = \Lambda(6)$$

### 3.3. Cusp Form Space Dimension $`\dim S_{24}(\Gamma_{0}(6))`$

Dimension formula for cusp forms of even weight $k \ge 4$ on congruence subgroup $`\Gamma_{0}(N)`$ ([Stein, Proposition 6.1](https://wstein.org/books/modform/modform/dimension_formulas.html), citing Diamond and Shurman):
$$\dim S_{k}(\Gamma_{0}(N)) = (k-1)(g-1) + \left\lfloor \frac{k}{4} \right\rfloor \nu_{2} + \left\lfloor \frac{k}{3} \right\rfloor \nu_{3} + \left(\frac{k}{2} - 1\right) \nu_{\infty}$$

Geometric parameters of modular curve $`X_{0}(6)`$ for level $N = 6$:

1. Modular index: $`\mu = [\mathrm{SL}_{2}(\mathbb{Z}) : \Gamma_{0}(6)] = 6 \left(1 + \frac{1}{2}\right)\left(1 + \frac{1}{3}\right) = 12`$
2. Elliptic points: Stein sets $`\mu_{0,2}(N)=0`$ when $4 \mid N$, and otherwise $`\mu_{0,2}(N)=\prod_{p \mid N}\left(1+\left(\frac{-4}{p}\right)\right)`$. Since $4 \nmid 6$, the product is required, and $\left(\frac{-4}{2}\right)=0$ makes $`\nu_{2}=0`$. Stein sets $`\mu_{0,3}(N)=0`$ when $2 \mid N$, so $`\nu_{3}=0`$ ([Stein, definitions preceding Proposition 6.1](https://wstein.org/books/modform/modform/dimension_formulas.html))
3. Cusps: $`\nu_{\infty} = \sum_{d \mid 6} \phi(\gcd(d, 6/d)) = \phi(1) + \phi(1) + \phi(1) + \phi(1) = 4`$
4. Riemann surface genus $g$:
   $$g = 1 + \frac{\mu}{12} - \frac{\nu_{2}}{4} - \frac{\nu_{3}}{3} - \frac{\nu_{\infty}}{2} = 1 + \frac{12}{12} - 0 - 0 - \frac{4}{2} = 0$$
5. Evaluation at weight $k = 24$:
   $$\dim S_{24}(\Gamma_{0}(6)) = (24-1)(0-1) + 0 + 0 + \left(\frac{24}{2} - 1\right) \times 4 = -23 + (11 \times 4) = -23 + 44 = 21$$
   $$\Lambda(6) = \frac{1}{\sqrt{\dim S_{24}(\Gamma_{0}(6))}} = \frac{1}{\sqrt{21}}$$

### 3.4. Ratio Identity of Euler Zeta Values $\zeta(6)/\zeta(4)$

Euler formula for even integer values of the Riemann zeta function ([particular values](https://en.wikipedia.org/wiki/Particular_values_of_the_Riemann_zeta_function)):
$$\zeta(2k) = \frac{(-1)^{k-1} (2\pi)^{2k} B_{2k}}{2(2k)!}$$

1. For $k = 2$ ($`B_{4} = -1/30`$):
   $$\zeta(4) = \frac{(2\pi)^{4} (1/30)}{2(24)} = \frac{16\pi^{4}}{1440} = \frac{\pi^{4}}{90}$$
2. For $k = 3$ ($`B_{6} = 1/42`$):
   $$\zeta(6) = \frac{(2\pi)^{6} (1/42)}{2(720)} = \frac{64\pi^{6}}{60480} = \frac{\pi^{6}}{945}$$
3. Ratio of zeta values:
   $$\frac{\zeta(6)}{\zeta(4)} = \frac{\pi^{6} / 945}{\pi^{4} / 90} = \pi^{2} \cdot \frac{90}{945} = \frac{2\pi^{2}}{21}$$
4. Substitution of $\Lambda(6)^{2} = 1/21$:
   $$\frac{\zeta(6)}{\zeta(4)} = 2\pi^{2} \Lambda(6)^{2} \implies \Lambda(6) = \sqrt{\frac{\zeta(6)}{2\pi^{2} \zeta(4)}} = \frac{1}{\sqrt{21}}$$

## 4. Applied Mathematical and Statistical Derivations

### 4.1. Artificial Intelligence and Machine Learning

1. Transformer Attention Scaling ([Vaswani et al. 2017](https://arxiv.org/abs/1706.03762))
   $$A(Q, K) = \mathrm{softmax}\left(\frac{QK^{T}}{\sqrt{d_{k}}}\right)$$
   For key projection dimension $`d_{k} = 21`$:
   $$\text{Scale} = \frac{1}{\sqrt{d_{k}}} = \frac{1}{\sqrt{21}} = \Lambda(6)$$
2. Xavier and Glorot Weight Initialization ([Glorot and Bengio 2010](https://proceedings.mlr.press/v9/glorot10a.html))
   The cited initialization is uniform on $`[-\sqrt{6/(n_{in}+n_{out})}, \sqrt{6/(n_{in}+n_{out})}]`$. The endpoint equals $\Lambda(6)$ when $`n_{in}+n_{out} = 126`$. The Gaussian shorthand $`\sigma = \sqrt{1/n_{in}}`$ is a later variant, not the formula in that paper.
3. He (Kaiming Normal - ReLU) Weight Initialization ([He et al. 2015](https://arxiv.org/abs/1502.01852))
   $$\sigma = \sqrt{\frac{2}{n_{l}}}$$
   For fan-in $`n_{l} = 42 = 2 \cdot T(6)`$:
   $$\sigma = \sqrt{\frac{2}{42}} = \sqrt{\frac{1}{21}} = \Lambda(6)$$
4. Diffusion Noise Schedule ([Ho, Jain, and Abbeel 2020](https://arxiv.org/abs/2006.11239))
   $$\sigma_{t} = \sqrt{1 - \bar{\alpha}_{t}}$$
   The value $`\bar{\alpha}_{t} = 20/21`$ is chosen here. It is not a schedule value derived in that paper:
   $$\sigma_{t} = \sqrt{1 - \frac{20}{21}} = \sqrt{\frac{1}{21}} = \Lambda(6)$$
5. Echo State input weights ([Jaeger 2001](https://publica.fraunhofer.de/entities/publication/7d4a7eec-a22c-4df0-903d-93d0c6c1f0e5) and [corrected report](https://www.ai.rug.nl/minds/uploads/EchoStatesTechRep.pdf)) and sample-mean standard error
   For independent observations, the [standard error](https://en.wikipedia.org/wiki/Standard_error) page gives $`\sigma_{\bar x}=\sigma/\sqrt{n}`$. The factor $1/\sqrt{n}$ is that standard error only when the population standard deviation is also $1$. It is not the definition of [Rademacher complexity](https://en.wikipedia.org/wiki/Rademacher_complexity). Jaeger's echo-state example sets input weights to $+1$ or $-1$ with equal probability. $1/\sqrt{n}$ is not an input scale prescribed by that report:
   $$\text{SE}(\bar{X}) = \frac{1}{\sqrt{n}}$$
   For $n = 21$ independent zero-mean unit-variance variables:
   $$\text{SE} = \frac{1}{\sqrt{21}} = \Lambda(6)$$

### 4.2. Statistics and Probability (Natural Exponential Families with Quadratic Variance Function)

1. Coefficient of Variation ($\mathrm{CV}$)
   $$\mathrm{CV} = \frac{\sigma}{\mu}$$
   - Poisson distribution ([Poisson distribution](https://en.wikipedia.org/wiki/Poisson_distribution), $\lambda = 21$): $\mu = 21$ and $\sigma^{2} = 21$, so
     $$\mathrm{CV} = \frac{\sqrt{21}}{21} = \frac{1}{\sqrt{21}} = \Lambda(6).$$
   - Skewness of Poisson distribution ($\lambda = 21$): $`\gamma_{1} = \frac{1}{\sqrt{\lambda}} = \frac{1}{\sqrt{21}} = \Lambda(6)`$
   - Gamma distribution ([gamma distribution](https://en.wikipedia.org/wiki/Gamma_distribution), $\alpha = 21, \beta = 1$): $\mu = 21$ and $\sigma^{2} = 21$, so
     $$\mathrm{CV} = \frac{\sqrt{21}}{21} = \frac{1}{\sqrt{21}} = \Lambda(6).$$
   - Chi-Square distribution ([chi-squared distribution](https://en.wikipedia.org/wiki/Chi-squared_distribution), $k = 42$): $\mu = 42$ and $\sigma^{2} = 84$, so
     $$\mathrm{CV} = \frac{\sqrt{84}}{42} = \frac{2\sqrt{21}}{42} = \frac{1}{\sqrt{21}} = \Lambda(6).$$
   - Binomial distribution ([binomial distribution](https://en.wikipedia.org/wiki/Binomial_distribution), $n = 21, p = 0.5$): $\mu = 10.5$ and $\sigma^{2} = 5.25$, so
     $$\mathrm{CV} = \frac{\sqrt{5.25}}{10.5} = \frac{1}{\sqrt{21}} = \Lambda(6).$$
   - Erlang distribution ([Erlang distribution](https://en.wikipedia.org/wiki/Erlang_distribution), $k = 21, \lambda$): $\mu = k/\lambda$ and $\sigma = \sqrt{k}/\lambda$, so
     $$\mathrm{CV} = \frac{\sqrt{21}/\lambda}{21/\lambda} = \frac{1}{\sqrt{21}} = \Lambda(6).$$
2. Information Geometry Metrics (Poisson Family)
   - Fisher information for one $\text{Poisson}(\lambda)$ observation ([Fisher information](https://en.wikipedia.org/wiki/Fisher_information)): $I(\lambda) = \frac{1}{\lambda}$, so
     $$\sqrt{I(21)} = \frac{1}{\sqrt{21}} = \Lambda(6).$$
     The metric component is $I(\lambda)$, while $\sqrt{I(\lambda)}\,d\lambda$ is the line element.
   - Jeffreys Prior ([Jeffreys prior](https://en.wikipedia.org/wiki/Jeffreys_prior)): $\pi(\lambda) \propto \sqrt{g(\lambda)} = \frac{1}{\sqrt{\lambda}}$, so
     $$\pi(21) \propto \frac{1}{\sqrt{21}} = \Lambda(6).$$

### 4.3. Physics and Relativistic Mechanics

1. Schwarzschild time-dilation factor ([gravitational time dilation](https://en.wikipedia.org/wiki/Gravitational_time_dilation))
   For a static exterior observer, proper time and distant Schwarzschild coordinate time satisfy $`t_{0}=t_{f}\sqrt{1-r_{s}/r}`$. The redshift measured from infinity is the reciprocal, $`1+z = 1/\sqrt{1-r_{s}/r}`$, so $z$ itself is not that factor ([gravitational redshift](https://en.wikipedia.org/wiki/Gravitational_redshift)). At the chosen radius $`r = \frac{21}{20} r_{s}`$:
   $$\sqrt{1 - \frac{r_{s}}{r}} = \sqrt{1 - \frac{20}{21}} = \sqrt{\frac{1}{21}} = \Lambda(6).$$
   In units $`c=r_{s}=1`$, writing $\Phi=-1/(2r)=-10/21$ makes $\sqrt{1+2\Phi}=\Lambda(6)$ by algebra. That equality does not make $\Phi$ the Newtonian-limit potential: $`r=1.05r_{s}`$ is not a weak field. It is not a measured interval near a physical black hole, and it lies inside the photon sphere. The static formula does not describe a circular orbit, whose factor is $`\sqrt{1-\frac{3}{2}r_{s}/r}`$.
2. Reciprocal of the Lorentz factor ([Lorentz factor](https://en.wikipedia.org/wiki/Lorentz_factor))
   The page defines $\gamma = 1/\sqrt{1-v^{2}/c^{2}}$. The quantity below is $1/\gamma$, not $\gamma$:
   $$\gamma^{-1} = \sqrt{1 - \frac{v^{2}}{c^{2}}}$$
   For velocity $v = \sqrt{\frac{20}{21}} c$:
   $$\gamma^{-1} = \sqrt{1 - \frac{20}{21}} = \sqrt{\frac{1}{21}} = \Lambda(6)$$
3. Harmonic Oscillation Period ([harmonic oscillator](https://en.wikipedia.org/wiki/Harmonic_oscillator))
   For an undamped harmonic oscillator $\ddot{x} + \omega^{2} x = 0$ with chosen stiffness-to-mass ratio $\omega^{2} = k/m = 21$:
   $$T = \frac{2\pi}{\omega} = \frac{2\pi}{\sqrt{21}} = 2\pi \Lambda(6)$$
4. Molecular Vibrational Degrees of Freedom ([molecular vibration](https://en.wikipedia.org/wiki/Molecular_vibration))
   For non-linear molecules with $N$ atoms, degrees of freedom are $3N - 6$. For $N = 9$:
   $$3(9) - 6 = 27 - 6 = 21$$
5. Adiabatic index ([heat capacity ratio](https://en.wikipedia.org/wiki/Heat_capacity_ratio))
   $$\gamma = 1 + \frac{2}{f}$$
   For effective internal degrees of freedom $f = 2\sqrt{21}$:
   $$\gamma = 1 + \frac{2}{2\sqrt{21}} = 1 + \frac{1}{\sqrt{21}} = 1 + \Lambda(6)$$

### 4.4. Engineering, Information Theory, and Kinetics

1. Second-Order System Percentage Overshoot ([overshoot](https://en.wikipedia.org/wiki/Overshoot_%28signal%29))

   Damping ratio formula:

   $$\%OS = \exp\left(-\frac{\pi \zeta}{\sqrt{1 - \zeta^{2}}}\right) \times 100\%$$
   For damping ratio $\zeta = \Lambda(6) = \frac{1}{\sqrt{21}}$:
   $$\zeta^{2} = \frac{1}{21} \implies 1 - \zeta^{2} = \frac{20}{21} \implies \sqrt{1 - \zeta^{2}} = \frac{\sqrt{20}}{\sqrt{21}}$$
   $$\frac{\zeta}{\sqrt{1-\zeta^{2}}} = \frac{1/\sqrt{21}}{\sqrt{20}/\sqrt{21}} = \frac{1}{\sqrt{20}}$$
   $$\%OS = \exp\left(-\frac{\pi}{\sqrt{20}}\right) \times 100\% = 49.5354568\ldots\%,$$
   displayed as $49.54\%$. The intermediate value $\exp(-\pi/\sqrt{20})=0.495354568\ldots$ is not $0.70248$.

2. Quality Factor ([Q factor](https://en.wikipedia.org/wiki/Q_factor))
   $$Q = \frac{1}{2\zeta}$$
   For $\zeta = \Lambda(6) = \frac{1}{\sqrt{21}}$:
   $$Q = \frac{1}{2(1/\sqrt{21})} = \frac{\sqrt{21}}{2} \approx 2.2913$$
3. Fixed-length alphabet ceiling ([prefix code](https://en.wikipedia.org/wiki/Prefix_code)) and Hash Table Load Factor ([hash table](https://en.wikipedia.org/wiki/Hash_table))
   - A fixed-length code of $k$ bits encodes at most $2^{k}$ symbols, so $`D = \lceil \log_{2} N \rceil`$ is that ceiling, not the Huffman weighted path length ([Huffman coding](https://en.wikipedia.org/wiki/Huffman_coding)). For $N = 21$ symbols:
     $$\log_{2}(21) \approx 4.3923 \implies \lceil 4.3923 \rceil = 5\text{ bits}$$
   - Hash Table Load Factor: $\alpha = n/m$. Choosing $m = 21$ buckets and $n = \sqrt{21}$ stored elements gives $\alpha = \Lambda(6)$. A real table has an integer element count:
     $$\alpha = \frac{\sqrt{21}}{21} = \frac{1}{\sqrt{21}} = \Lambda(6)$$
4. First-Order Reaction Rate and Half-Life ([rate equation](https://en.wikipedia.org/wiki/Rate_equation))
   $$k = \frac{\ln 2}{t_{1/2}}$$
   For half-life $`t_{1/2} = \Lambda(6) = \frac{1}{\sqrt{21}}`$:
   $$k = \frac{\ln 2}{1/\sqrt{21}} = \ln 2 \cdot \sqrt{21} \approx 3.1764$$
5. Michaelis-Menten Enzyme Kinetics ([Michaelis and Menten 1913](https://doi.org/10.1021/bi201284u), English translation) and Bioavailability
   - Normalized reaction velocity:
     $$\frac{v}{V_{\max}} = \frac{[S]}{K_{m} + [S]} = \frac{[S]/K_{m}}{1 + [S]/K_{m}}$$
     Setting the substrate ratio to $`[S]/K_{m} = 1/\sqrt{21}`$ does not make the velocity ratio equal $\Lambda(6)$:
     $$\frac{v}{V_{\max}} = \frac{1/\sqrt{21}}{1 + 1/\sqrt{21}} = \frac{1}{\sqrt{21} + 1} \approx 0.179129.$$
   - Absolute bioavailability ([bioavailability](https://en.wikipedia.org/wiki/Bioavailability)) is the dose-normalized ratio of extravascular to intravenous area under the concentration curve. Setting that fraction to $\Lambda(6)$ gives $F = 1/\sqrt{21} \approx 21.82\%$. This is an input choice, not a measured drug value.
   - Bazett rate correction ([Bazett 1920](https://doi.org/10.1111/j.1542-474X.1997.tb00325.x)), in dimensionally consistent form:
     $$\mathrm{QTc} = \frac{\mathrm{QT}}{\sqrt{\mathrm{RR}/1\,\mathrm{s}}}.$$
     Choosing $\mathrm{RR} = 1/\sqrt{21}\,\mathrm{s}$ is an input substitution. It is not a measured cardiac interval, and a bare $\mathrm{QT}/\sqrt{\mathrm{RR}}$ is dimensionally inconsistent.
6. Clinical Trial Sample Size per Group ([Cohen, Statistical Power Analysis, 2nd ed.](https://doi.org/10.4324/9780203771587))
   $$n = \frac{2(z_{\alpha} + z_{\beta})^{2}}{d^{2}}$$
   For Cohen's effect size $d = \Lambda(6) = \frac{1}{\sqrt{21}}$, it follows that $d^{2} = \frac{1}{21}$:
   $$n = 2 \cdot 21 (z_{\alpha} + z_{\beta})^{2} = 42(z_{\alpha} + z_{\beta})^{2}$$
7. Kelly Criterion Fraction ([Kelly criterion](https://en.wikipedia.org/wiki/Kelly_criterion) and [Kelly 1956](https://www.princeton.edu/~wbialek/rome/refs/kelly_56.pdf))
   The cited page's binary formula is $f = p/l - q/g$. Kelly's 1956 paper does not write that formula. Its even-money calculation gives the same fraction, $\ell = 2q - 1$, after swapping its win and loss labels. For even money, $g = l = 1$, so
   $$f = p - q = 2p - 1.$$
   Setting that edge to $\Lambda(6) = 1/\sqrt{21}$ gives
   $$p = \frac{1 + \Lambda(6)}{2} = \frac{1 + 1/\sqrt{21}}{2} \approx 0.609109.$$
   The odds form $(bp - q)/b$ is this case only when the whole stake is lost and the net gain on a win is $b$. It is not the formula displayed by either cited source.
8. Transmission-Line Reflection and Impedance Ratio ([reflection coefficient](https://en.wikipedia.org/wiki/Reflection_coefficient))
   The cited page displays the load reflection coefficient $`\Gamma=(Z_{L}-Z_{0})/(Z_{L}+Z_{0})`$, not an acoustic pressure-amplitude formula. Its linked acoustic section instead defines $R$ as the ratio of reflected to incident intensity, written there as $`R=p_{\mathrm{reflected}}/p_{\mathrm{incident}}`$, and then uses $\alpha=1-R^{2}$. For a real ratio $`z=Z_{L}/Z_{0}`$,
   $$\Gamma = \frac{z - 1}{z + 1}.$$
   For $\Gamma = \Lambda(6) = \frac{1}{\sqrt{21}}$:
   $$z = \frac{1 + \Gamma}{1 - \Gamma} = \frac{\sqrt{21} + 1}{\sqrt{21} - 1} = \frac{(\sqrt{21}+1)^{2}}{20} = \frac{22 + 2\sqrt{21}}{20} = \frac{11 + \sqrt{21}}{10} \approx 1.558258$$
9. Planetary, Geophysics, and Neutrino Metrics
   - Kepler's third law in solar units ([Kepler's laws](https://en.wikipedia.org/wiki/Kepler%27s_laws_of_planetary_motion)), where the primary has one solar mass: $T^{2} = a^{3}$ with $T$ in years and $a$ in AU. For orbital period $T = 21$ yr:
     $$a = 21^{2/3} = \sqrt[3]{441} \approx 7.61166\text{ AU}$$
   - Gutenberg-Richter law ([Gutenberg-Richter law](https://en.wikipedia.org/wiki/Gutenberg%E2%80%93Richter_law)) with chosen baseline parameters $a = 5.0$, $b = 1.0$, and chosen cumulative event rate $N = 1/\sqrt{21}$:
     $$M = \frac{a - \log_{10}(1/\sqrt{21})}{b} = 5.0 + \log_{10}(\sqrt{21}) = 5.0 + 0.6611 = 5.6611 \approx 5.66$$
   - Effective neutrino number: [Akita and Yamaguchi 2020](https://arxiv.org/abs/2005.07047) calculate $`N_{\mathrm{eff}} = 3.044`$, with numerical and mixing error at most $0.0005$. The numerical proximity $\ln(21) \approx 3.04452$ is not an identity and is not the definition of $`N_{\mathrm{eff}}`$.
10. Game Theory and Economics (Cournot Equilibrium and First-Price Auction)

- Cournot Oligopoly ([Cournot 1838](https://gallica.bnf.fr/ark:/12148/bpt6k6117257c) and linear identical-firm case [Marker](https://homepages.math.uic.edu/~marker/stat473-s19/Cournot.pdf)): for inverse demand $p = a-bQ$ and common marginal cost $c$, each equilibrium output is $`q_i = (a-c)/((n+1)b)`$. For $n = 20$, $`q_i/((a-c)/b) = 1/21`$.
- First-Price Sealed-Bid Auction ([first-price sealed-bid auction](https://en.wikipedia.org/wiki/First-price_sealed-bid_auction)): the page states the symmetric Bayesian Nash equilibrium $b(v) = \frac{n-1}{n} v$ for valuations that are i.i.d. uniform on $[0,1]$. Its general symmetric BNE is $`E[y_i \mid y_i<v_i]`$. For $n = 21$ bidders, the uniform strategy is $b(v) = \frac{20}{21} v$.
- Herd Immunity Threshold ([herd immunity](https://en.wikipedia.org/wiki/Herd_immunity)): $`p_c = 1 - \frac{1}{R_{0}}`$ under homogeneous mixing, solid immunity, no immune escape, and no nonhuman vector. For $`R_{0} = 21`$, that threshold is $\frac{20}{21}$.
- Autoregressive Time Series AR(1) ([autoregressive model](https://en.wikipedia.org/wiki/Autoregressive_model)): for $`|\phi|<1`$, stationary variance $`\mathrm{Var}(X_{t}) = \frac{\sigma_{\varepsilon}^{2}}{1 - \phi^{2}}`$. For $\phi = \frac{1}{\sqrt{21}}$, $`\mathrm{Var}(X_{t}) = \frac{21}{20} \sigma_{\varepsilon}^{2}`$.
