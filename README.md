# Triangular Root Invariant

$100/\sqrt{21} = 21.821789023599238\ldots$, displayed to 14 decimal places as $21.82178902359924$.

[Algebra](https://en.wikipedia.org/wiki/Algebra) is the branch of mathematics that studies abstract symbols and the rules for manipulating them. The shared mathematical quantity evaluated across these documents is the algebraic constant $1/\sqrt{21} = 1/\sqrt{T(6)}$, where $T(n) = n(n+1)/2$ is the $n$-th triangular number.

Outside of exact analytical identities, domain-specific evaluations represent direct numerical parameter substitutions into standard governing equations rather than universal physical invariants or empirical coincidences. Detailed derivations and proofs are cataloged in [Mathematical Derivations](Math.md).

## Abstract

Single final formula:
$$\Lambda(n) = \sqrt{\frac{2}{n(n+1)}} = \frac{1}{\sqrt{T(n)}}, \quad \Lambda(6) = \frac{1}{\sqrt{21}} = 0.21821789023599238\ldots,$$
displayed to 16 decimals as $0.2182178902359924$.

$100 \cdot \Lambda(6) = 21.82178902359924$ is the decimal display of $1/\sqrt{21}$. Domain rows below are substitutions of $21$, $42$, $126$, $20/21$, or $1/\sqrt{21}$ into standard formulas, except where an identity is stated.

**Core Contributions**:

1. $\Lambda(6) = 1/\sqrt{21}$ up to 15 or more digits of precision.
2. $n=6$ is the unique positive integer index with $T(n) = 21$. The identity $\Lambda(n) = 1/\sqrt{T(n)}$ holds for every positive integer $n$.
3. The shared value is the algebraic quantity $1/\sqrt{21}$. Agreement after a parameter is set to $21$, $42$, $126$, $20/21$, or $1/\sqrt{21}$ is a substitution, not evidence of a causal link between domains.
4. The generic formula $\Lambda(n) = \sqrt{2/(n(n+1))}$ is derived without hardcoded numeric constants such as $21$ or $0.2182$.

## 1. Single Unified Formula

### 1.1. Definition and Evaluation

$$\Lambda(n) = \sqrt{\frac{2}{n(n+1)}} = \frac{1}{\sqrt{T(n)}}, \quad n \in \mathbb{N}_{>0}$$

where $T(n) = n(n+1)/2$ is the $n$-th triangular number ([triangular number](https://en.wikipedia.org/wiki/Triangular_number)).

Evaluation for $n = 6$:
$$\Lambda(6) = \sqrt{\frac{2}{6 \cdot 7}} = \sqrt{\frac{1}{21}} = \frac{1}{\sqrt{21}} = 0.21821789023599238\ldots$$

### 1.2. Analytical Properties

**Partial fraction telescoping**:
$$\Lambda(n)^{2} = \frac{2}{n(n+1)} = 2\left(\frac{1}{n} - \frac{1}{n+1}\right)$$

**Convergence of sum of squares**:
$$\sum_{n=1}^{N} \Lambda(n)^{2} = \frac{2N}{N+1} \xrightarrow{N \to \infty} 2$$

**Asymptotic linear sum**:
$$\sum_{n=1}^{N} \Lambda(n) \sim \sqrt{2}\,\ln N + O(1)$$

### 1.3. Uniqueness of $n = 6$

**Theorem**: $100 \cdot \Lambda(n) = 21.8218\ldots$ for $n \in \mathbb{N}_{>0}$ if and only if $n = 6$.

_Proof_: The equation $100 \cdot \sqrt{2/(n(n+1))} = 21.821789\ldots$ yields $n(n+1) = 42$, which corresponds to the quadratic equation $n^{2} + n - 42 = 0$. The discriminant is $1 + 168 = 169 = 13^{2}$, which is a perfect square. The single positive integer root is $n = (-1+13)/2 = 6$. $\blacksquare$

**Generalization**: $\Lambda(n) = 1/\sqrt{k}$ for positive integers $n$ and $k$ if and only if $k = T(n)$. The value $k = 21$ occurs uniquely at $n = 6$.

### 1.4. Continuous Beta Function Generalization

$$\boxed{\Lambda(x) = \sqrt{2\,B(x, 2)} = \sqrt{\frac{2\,\Gamma(x)}{\Gamma(x+2)}}, \quad x > 0}$$

where $B(x, 2)$ denotes the Euler Beta function ([Beta function](https://en.wikipedia.org/wiki/Beta_function)). For integer values $x = n$, the expression returns to the discrete form $\sqrt{2/(n(n+1))}$.

**Logarithmic differential equation**:
$$\frac{d}{dx} \ln \Lambda(x) = -\frac{1}{2x} - \frac{1}{2(x+1)}$$

**Generating function of squares**:
$$G(z) = \sum_{n=1}^\infty \Lambda(n)^{2} z^{n} = 2 + \frac{2(1-z)\ln(1-z)}{z}, \quad \lvert z\rvert < 1$$

### 1.5. Equivalent Representations (Master Summary)

Rows 1--5 are identities for every positive integer $n$. Rows 6--14 equal $\Lambda(6)$ only, and only after the index or parameter named in each row is fixed:

| #   | Representation                                                                          | Mathematical Domain     |
| --- | --------------------------------------------------------------------------------------- | ----------------------- |
| 1   | Algebraic form $\sqrt{2/(n(n+1))}$                                                      | Pure mathematics        |
| 2   | Triangular form $1/\sqrt{T(n)}$                                                         | Number theory           |
| 3   | Beta function $\sqrt{2\,B(n,2)}$                                                        | Special functions       |
| 4   | Gamma function $\sqrt{2\,\Gamma(n)/\Gamma(n+2)}$                                        | Special functions       |
| 5   | Partial fraction $\sqrt{2(1/n - 1/(n+1))}$                                              | Real analysis           |
| 6   | Polygonal number $1/\sqrt{P(d, n)}$ for $(d, n) \in \{(3, 6), (8, 3), (21, 2)\}$        | Polygonal numbers       |
| 7   | Fibonacci number $1/\sqrt{F_{8}}$                                                       | Recursive sequences     |
| 8   | $21$ is the second term of OEIS A046183, not a representation of $\Lambda(n)$           | Diophantine geometry    |
| 9   | Coefficient of variation $1/\sqrt{21}$ at the parameter fixed in Section 2.2            | Exponential families    |
| 10  | Stirling, Motzkin, and Standard Young Tableaux counts $1/\sqrt{M_{5}}, 1/\sqrt{c(7,6)}$ | Combinatorics           |
| 11  | Quadratic Gauss sum $1/\lvert g(\chi_{21})\rvert$                                       | Analytic number theory  |
| 12  | Class number $h(\mathbb{Q}(\sqrt{21})) = 1$, which makes row 13 an identity             | Algebraic number theory |
| 13  | Dirichlet L-function $L(1, \chi_{21})/(2\log \varepsilon_{21})$                         | Analytic number theory  |
| 14  | Cusp forms dimension $1/\sqrt{\dim S_{24}(\Gamma_{0}(6))}$                              | Modular forms           |

## 2. Key Domain Manifestations

### 2.1. Machine Learning and Artificial Intelligence

| Domain                                                                                                                                                                                                     | Formula                                                              | Instantiation                                                                                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Transformer Attention ([Vaswani et al. 2017](https://arxiv.org/abs/1706.03762))                                                                                                                            | $1/\sqrt{d_{k}}$                                                     | $d_{k} = 21$: Exact $\Lambda(6)$                                                                                                                                                         |
| Xavier Initialization ([Glorot and Bengio 2010](https://proceedings.mlr.press/v9/glorot10a.html))                                                                                                          | Uniform on $[-\sqrt{6/(n_{in}+n_{out})}, \sqrt{6/(n_{in}+n_{out})}]$ | $n_{in}+n_{out} = 126$: the paper's bound endpoint is $\Lambda(6)$; $\sqrt{1/n_{in}}$ is a later shorthand                                                                               |
| He Initialization (ReLU) ([He et al. 2015](https://arxiv.org/abs/1502.01852))                                                                                                                              | Gaussian standard deviation $\sqrt{2/n_{in}}$                        | $n_{in} = 42$: $\Lambda(6)$                                                                                                                                                              |
| Diffusion Noise Schedule ([Ho, Jain, and Abbeel 2020](https://arxiv.org/abs/2006.11239))                                                                                                                   | $\sqrt{1 - \bar{\alpha}_{t}}$                                        | $\bar{\alpha}_{t} = 20/21$ is a chosen schedule value, not a value derived by that paper                                                                                                 |
| Echo State Network ([Jaeger 2001](https://publica.fraunhofer.de/entities/publication/7d4a7eec-a22c-4df0-903d-93d0c6c1f0e5); [corrected report](https://www.ai.rug.nl/minds/uploads/EchoStatesTechRep.pdf)) | No required input scale                                              | Jaeger's example sets input weights to $\pm 1$; $1/\sqrt{N}$ is not a formula in that report                                                                                             |
| Sample-mean standard error                                                                                                                                                                                 | $\text{SE}(\bar{X}) = \sigma/\sqrt{n}$                               | For independent zero-mean unit-variance variables and $n = 21$: $\Lambda(6)$. This is not the definition of [Rademacher complexity](https://en.wikipedia.org/wiki/Rademacher_complexity) |

### 2.2. Statistics and Probability

**Coefficient of Variation in Natural Exponential Families with Quadratic Variance Function ([Morris 1982](https://projecteuclid.org/journals/annals-of-statistics/volume-10/issue-1/Natural-Exponential-Families-with-Quadratic-Variance-Functions/10.1214/aos/1176345690.full))**:
The coefficient of variation equals $1/\sqrt{21}$ for the five parameter choices below. Morris classifies six quadratic-variance families: normal, Poisson, gamma, binomial, negative binomial, and hyperbolic secant. The negative-binomial and hyperbolic-secant families are not included, and the binomial equality also fixes $p = 1/2$:

| Distribution                                                                                  | Shape Parameter | Coefficient of Variation |
| --------------------------------------------------------------------------------------------- | --------------- | ------------------------ |
| [Poisson](https://en.wikipedia.org/wiki/Poisson_distribution) $\text{Poisson}(\lambda)$       | $\lambda = 21$  | $1/\sqrt{21}$            |
| [Gamma](https://en.wikipedia.org/wiki/Gamma_distribution) $\text{Gamma}(\alpha, 1)$           | $\alpha = 21$   | $1/\sqrt{21}$            |
| [Chi-squared](https://en.wikipedia.org/wiki/Chi-squared_distribution) $\text{Chi-squared}(k)$ | $k = 42$        | $1/\sqrt{21}$            |
| [Binomial](https://en.wikipedia.org/wiki/Binomial_distribution) $\text{Binomial}(n, p=0.5)$   | $n = 21$        | $1/\sqrt{21}$            |
| [Erlang](https://en.wikipedia.org/wiki/Erlang_distribution) $\text{Erlang}(k, \lambda)$       | $k = 21$        | $1/\sqrt{21}$            |

**Skewness of Poisson(21)**: $\gamma_{1}[\text{Poisson}(21)] = 1/\sqrt{21}$. For every Poisson parameter, coefficient of variation equals skewness. The value $21$ selects the common magnitude, not a unique distribution.

**Fisher information**: For one observation from $\text{Poisson}(\lambda)$, the Fisher information is $I(\lambda) = 1/\lambda$ ([Fisher information](https://en.wikipedia.org/wiki/Fisher_information)). Hence $\sqrt{I(21)} = 1/\sqrt{21} = \Lambda(6)$. The quantity $\sqrt{I(\lambda)}\,d\lambda$ is the line element, not the metric component itself.

**Jeffreys Prior**: $\pi(\lambda) \propto 1/\sqrt{\lambda}$ ([Jeffreys prior](https://en.wikipedia.org/wiki/Jeffreys_prior)). The density is fixed only up to normalization, so $\pi(21) \propto \Lambda(6)$, not $\pi(21) = \Lambda(6)$.

**Standard error of the mean**: For $n$ independent observations with population standard deviation $\sigma$, the [standard error](https://en.wikipedia.org/wiki/Standard_error) page gives $\sigma_{\bar x}=\sigma/\sqrt{n}$. Thus $\text{SE}=1/\sqrt{n}$ requires $\sigma=1$; at $n=21$ that is $\Lambda(6)$.

### 2.3. Physics

| Domain                                                                                                                        | Formula                                           | Instantiation                                                                                                    |
| ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Harmonic Oscillation Period ([harmonic oscillator](https://en.wikipedia.org/wiki/Harmonic_oscillator))                        | $T = 2\pi/\omega$                                 | $\omega=\sqrt{k/m}$, so $\omega^{2}=21$ is a chosen stiffness-to-mass ratio                                      |
| Schwarzschild time-dilation factor ([gravitational time dilation](https://en.wikipedia.org/wiki/Gravitational_time_dilation)) | $t_{0}=t_{f}\sqrt{1-r_{s}/r}$                     | Static exterior clock at $r/r_{s}=21/20$; $\Phi=-10/21$ is algebraic notation, not the Newtonian-limit potential |
| Reciprocal of the Lorentz factor ([Lorentz factor](https://en.wikipedia.org/wiki/Lorentz_factor))                             | $1/\gamma=\sqrt{1 - v^{2}/c^{2}}$                 | $v/c = \sqrt{20/21}$ is a chosen speed; the page defines $\gamma$ as the reciprocal                              |
| Upper-mantle viscosity range ([Earth's mantle](https://en.wikipedia.org/wiki/Earth%27s_mantle))                               | $10^{19}$ to $10^{24}$ Pa·s                       | $10^{21}$ is one conventional scale inside the reported upper-mantle range, not an exact value                   |
| Molecular Vibrational Modes ([molecular vibration](https://en.wikipedia.org/wiki/Molecular_vibration))                        | $3N - 6$                                          | Nonlinear molecule with $N = 9$: $21$ vibrational modes                                                          |
| Bernoulli number in the zeta formula ([Bernoulli number](https://en.wikipedia.org/wiki/Bernoulli_number))                     | $B_{6} = +1/42$ in both standard sign conventions | $1/42 = 1/(2T(6))$; the two conventions differ at $B_{1}$, not at $B_{6}$                                        |

### 2.4. Engineering and Computer Science

| Domain                                                                                        | Formula                                  | Instantiation                                                                                                                         |
| --------------------------------------------------------------------------------------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Quality Factor ([Q factor](https://en.wikipedia.org/wiki/Q_factor))                           | $1/(2\zeta)$                             | $\zeta = 1/\sqrt{21}$: $Q = \sqrt{21}/2$                                                                                              |
| Peak Percentage Overshoot ([overshoot](https://en.wikipedia.org/wiki/Overshoot_%28signal%29)) | $100\exp(-\pi \zeta/\sqrt{1-\zeta^{2}})$ | Underdamped second-order step response; $\zeta = 1/\sqrt{21}$ gives $49.535\%$, displayed as $49.54\%$                                |
| Fixed-length alphabet ceiling ([prefix code](https://en.wikipedia.org/wiki/Prefix_code))      | $\lceil \log_{2} N \rceil$               | A $k$-bit fixed-length code encodes at most $2^{k}$ symbols, so $N = 21$ needs $5$ bits. This is not the Huffman weighted path length |
| Hash Table Load Factor ([hash table](https://en.wikipedia.org/wiki/Hash_table))               | $\alpha = n/m$                           | Choosing $m = 21$ buckets and $n = \sqrt{21}$ stored elements gives $\alpha = \Lambda(6)$; a real table has an integer element count  |

### 2.5. Life Sciences and Medicine

| Domain                                                                                                                                               | Formula                                                                                     | Instantiation                                                                                   |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| First-Order Reaction Rate ([rate equation](https://en.wikipedia.org/wiki/Rate_equation))                                                             | $k = \ln 2 / t_{1/2}$                                                                       | Half-life $t_{1/2} = 1/\sqrt{21}$ is a chosen time                                              |
| Clinical Trial Sample Size ([Cohen, Statistical Power Analysis, 2nd ed.](https://doi.org/10.4324/9780203771587))                                     | $n = 2(z_{\alpha}+z_{\beta})^{2}/d^{2}$ per group                                           | For $d = 1/\sqrt{21}$ this is $42(z_{\alpha}+z_{\beta})^{2}$ per group, not a total sample size |
| Michaelis-Menten Kinetics ([Michaelis and Menten 1913](https://doi.org/10.1021/bi201284u), English translation)                                      | $v/V_{\max} = [S]/(K_{m}+[S])$                                                              | $[S]/K_{m} = 1/\sqrt{21}$ gives $v/V_{\max} = 1/(\sqrt{21}+1)$, not $\Lambda(6)$                |
| Absolute Bioavailability ([bioavailability](https://en.wikipedia.org/wiki/Bioavailability))                                                          | Dose-normalized $\mathrm{AUC}_{\mathrm{extravascular}}/\mathrm{AUC}_{\mathrm{intravenous}}$ | Setting that fraction to $1/\sqrt{21}$ gives $21.82\%$; it is not a measured drug value         |
| Bazett rate correction ([Bazett 1920](https://doi.org/10.1111/j.1542-474X.1997.tb00325.x); [QT interval](https://en.wikipedia.org/wiki/QT_interval)) | $\text{QTc} = \text{QT}/\sqrt{\text{RR}/1\,\text{s}}$                                       | Setting $\text{RR} = 1/\sqrt{21}$ seconds is an input choice, not a measured interval           |

### 2.6. Economics, Geology, Astronomy, and Epidemiology

| Domain                                                                                                                                                                                   | Formula                                                                                                                                     | Instantiation                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Herd Immunity Threshold ([herd immunity](https://en.wikipedia.org/wiki/Herd_immunity))                                                                                                   | $1 - 1/R_{0}$                                                                                                                               | Homogeneous mixing, solid immunity, no immune escape, and no nonhuman vector; $R_{0} = 21$ then gives $20/21$                                                      |
| First-Price Auction ([first-price sealed-bid auction](https://en.wikipedia.org/wiki/First-price_sealed-bid_auction))                                                                     | $(n-1)/n \cdot v$                                                                                                                           | The page states this symmetric BNE for i.i.d. uniform $[0,1]$ valuations; its general symmetric BNE is $E[y_i \mid y_i<v_i]$, and $n = 21$ gives bid ratio $20/21$ |
| Cournot Oligopoly Equilibrium ([Cournot 1838](https://archive.org/details/recherchessurles00cour); linear case [Marker](https://homepages.math.uic.edu/~marker/stat473-s19/Cournot.pdf)) | $(a-c)/((n+1)b)$                                                                                                                            | Identical firms, inverse demand $p=a-bQ$, and marginal cost $c$; $n = 20$: firm output ratio $= 1/21$                                                              |
| Kelly Betting Fraction ([Kelly criterion](https://en.wikipedia.org/wiki/Kelly_criterion))                                                                                                | $p/l-q/g$                                                                                                                                   | Even money $g=l=1$ and edge $2p-1=1/\sqrt{21}$: the page's fraction is $2p-1$, so $p \approx 0.609109$                                                             |
| Kepler third law in solar units ([Kepler's laws](https://en.wikipedia.org/wiki/Kepler%27s_laws_of_planetary_motion))                                                                     | $T^{2} = a^{3}$ for a solar-mass primary                                                                                                    | Period $T = 21$ years gives $a = 21^{2/3} \approx 7.61$ AU; this is not the mass-independent SI form                                                               |
| Gutenberg-Richter law ([Gutenberg-Richter law](https://en.wikipedia.org/wiki/Gutenberg%E2%80%93Richter_law))                                                                             | $\log_{10} N = a - bM$                                                                                                                      | $a = 5$, $b = 1$, and $N = 1/\sqrt{21}$ are chosen inputs; they give $M \approx 5.66$                                                                              |
| Transmission-line reflection ([reflection coefficient](https://en.wikipedia.org/wiki/Reflection_coefficient))                                                                            | $\Gamma=(Z_{L}-Z_{0})/(Z_{L}+Z_{0})$                                                                                                        | Choosing real $\Gamma=1/\sqrt{21}$ gives $Z_{L}/Z_{0}=(11+\sqrt{21})/10 \approx 1.558258$; the page's acoustic $R$ is an intensity ratio, not this formula         |
| Adiabatic Index ([heat capacity ratio](https://en.wikipedia.org/wiki/Heat_capacity_ratio))                                                                                               | $1 + 2/f$                                                                                                                                   | Choosing effective degrees of freedom $f = 2\sqrt{21}$ gives $\gamma = 1+\Lambda(6)$; equipartition uses integer $f$                                               |
| Effective neutrino number                                                                                                                                                                | $N_{\mathrm{eff}} = 3.044$, with numerical and mixing error at most $0.0005$ ([Akita and Yamaguchi 2020](https://arxiv.org/abs/2005.07047)) | $\ln(21) \approx 3.04452$ is a numerical proximity, not the definition of $N_{\mathrm{eff}}$                                                                       |

## 3. Scope of the Domain Catalog

The only distribution-free interval probability that follows from the stated bounds is the uniform case: an interval of length $1$ inside $(0, 100)$ has probability $1\%$. The previously listed log-normal, ratio, four-decimal, and Snedecor probabilities are omitted because the files do not specify parameters, sample size, or a seed, so those figures are not reproducible.

**Scope**: Shared algebraic form does not establish a physical correlation. A row is an identity only when both sides are equal without a free parameter being set to $21$, $42$, $126$, $20/21$, or $1/\sqrt{21}$.

## 4. Multi-Combinatorial Convergence at 21

### 4.1. Ten Combinatorial Evaluations

**Count**: The integer $21$ has ten evaluations below. They are not ten independent counts: $T(6)=\binom{7}{2}$, and both $S(7,6)$ and $c(7,6)$ equal that binomial coefficient by the one-step identities $S(n,n-1)=c(n,n-1)=\binom{n}{2}$ ([unsigned Stirling numbers of the first kind](https://en.wikipedia.org/wiki/Stirling_numbers_of_the_first_kind); [Stirling numbers of the second kind](https://en.wikipedia.org/wiki/Stirling_numbers_of_the_second_kind)).
$$21 = T(6) = \binom{7}{2} = O(3) = I_{21}(2) = F_{8} = S(7, 6) = c(7, 6) = M_{5} = f^{(3,3,1)} = f^{(3,2,2)}$$

| Symbol         | Combinatorial Name                               | Formal Definition                                                                                                                        |
| -------------- | ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| $T(6)$         | Triangular number                                | $6 \cdot 7 / 2 = 21$                                                                                                                     |
| $\binom{7}{2}$ | Binomial coefficient                             | $7! / (2! \cdot 5!) = 21$                                                                                                                |
| $O(3)$         | Octagonal number                                 | $P(8,3)=3(3\cdot 3-2)=21$ ([polygonal number](https://en.wikipedia.org/wiki/Polygonal_number))                                           |
| $I_{21}(2)$    | Icosihenagonal number                            | $P(21,2)=((21-2)2^{2}-(21-4)2)/2=21$                                                                                                     |
| $F_{8}$        | Fibonacci number                                 | $F_{0}=0,F_{1}=1$ and $F_{8}=21$ ([Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_sequence))                                |
| $S(7, 6)$      | Stirling partition number of the second kind     | Number of ways to partition 7 items into 6 non-empty subsets                                                                             |
| $c(7, 6)$      | Unsigned Stirling cycle number of the first kind | Number of permutations of 7 items with 6 disjoint cycles                                                                                 |
| $M_{5}$        | Motzkin number                                   | Non-intersecting chords on 5 points; the sequence begins $1,1,2,4,9,21$ ([Motzkin number](https://en.wikipedia.org/wiki/Motzkin_number)) |
| $f^{(3,3,1)}$  | Standard Young Tableaux count                    | Hook-length count $7!/240=21$ for shape $(3,3,1)$ ([hook-length formula](https://en.wikipedia.org/wiki/Hook-length_formula))             |
| $f^{(3,2,2)}$  | Standard Young Tableaux count                    | Hook-length count $7!/240=21$ for shape $(3,2,2)$                                                                                        |

**Implication**: These ten formulas evaluate $\Lambda(6)$. The Stirling and binomial rows are the same count, so the avenues are not independent:
$$\Lambda(6) = \frac{1}{\sqrt{T(6)}} = \frac{1}{\sqrt{\binom{7}{2}}} = \frac{1}{\sqrt{F_{8}}} = \frac{1}{\sqrt{M_{5}}} = \cdots$$

### 4.2. Quintuple Identity Uniqueness

The integer $21$ is the only positive integer below $5000$ that simultaneously satisfies these five selected criteria. The bound is computational, not a proof for every larger integer:

1. $21 = T(6)$ is a triangular number.
2. $21 = 3 \cdot 7$ is a semiprime number ([semiprime](https://en.wikipedia.org/wiki/Semiprime)).
3. The multiplicative order of $2$ modulo $21$ equals $6$, namely $\text{ord}_{21}(2) = 6$ ([multiplicative order](https://en.wikipedia.org/wiki/Multiplicative_order)).
4. The Carmichael function satisfies $\lambda(21) = 6$ ([Carmichael function](https://en.wikipedia.org/wiki/Carmichael_function); table value and [Carmichael 1910](https://doi.org/10.1090/S0002-9904-1910-01892-9)).
5. $21 = F_{8}$ is a Fibonacci number.

### 4.3. Luo's Theorem on Fibonacci Triangular Numbers

The only Fibonacci numbers that are also triangular are $0, 1, 3, 21, 55$, corresponding to $F_{0}, F_{1}=F_{2}, F_{4}, F_{8}, F_{10}$ ([Luo Ming 1989](https://www.fq.math.ca/Scanned/27-2/ming.pdf); [OEIS A039595](https://oeis.org/A039595)). Thus $21 = F_{8} = T(6)$ is one of three non-zero equalities below $55$, alongside $F_{1}=F_{2}=1=T(1)$ and $F_{4}=3=T(2)$. The Cohn (1964) square-Fibonacci theorem does not state this result.

### 4.4. OEIS A046183 (Octagonal-Triangular Numbers)

[OEIS A046183](https://oeis.org/A046183) begins $1, 21, 11781, 203841, 113123361, \ldots$, with offset $1$. Thus $21$ is $a(2)$, the second listed term and the smallest term greater than $1$. The sequence itself does not define a trivial term.

### 4.5. Ramsey Number $R(3,3) = 6$

**Theorem ([Ramsey 1930](https://doi.org/10.1112/plms/s2-30.1.264))**: $R(3,3) = 6$ ([Ramsey's theorem](https://en.wikipedia.org/wiki/Ramsey%27s_theorem)). The threshold $n = 6$ is the least order guaranteeing a monochromatic triangle in every two-color edge coloring of a complete graph. Ramsey's 1930 paper proves the general existence theorem; the evaluation $R(3,3) = 6$ is the elementary graph-theoretic case.

### 4.6. Continued Fraction Periodicity of $\sqrt{21}$

The continued fraction expansion of $\sqrt{21}$ is $[4; \overline{1, 1, 2, 1, 1, 8}]$. Its repeating block has length $6$, so the continued-fraction period is $r=6$. Periodicity for the square root of every non-square integer follows from Lagrange's continued-fraction solution of Pell's equation ([continued fraction](https://en.wikipedia.org/wiki/Continued_fraction)). A direct computation finds that the period of $\sqrt{T(k)}$ equals $k$ at $k=2$ and $k=6$: period $2$ for $\sqrt{T(2)}=\sqrt{3}$ and period $6$ for $\sqrt{T(6)}=\sqrt{21}$. This is not a rule for every $k$. It fails at $k=3$: $\sqrt{T(3)}=\sqrt{6}$ has period $2$, not $3$. The later equality at $k=22$ also does not restore such a rule: $\sqrt{T(22)}=\sqrt{253}$ has period $22$.

Convergents are indexed from the initial term, so the sixth convergent, written $h_{5}/k_{5}$, of $[4;\overline{1,1,2,1,1,8}]$ is $55/12$, and $55^{2}-21\cdot 12^{2}=1$ ([continued fraction](https://en.wikipedia.org/wiki/Continued_fraction)). Since $r$ is even, the fundamental-solution rule selects convergent index $r-1=5$, the same fraction ([Pell's equation](https://en.wikipedia.org/wiki/Pell%27s_equation)). It is the cube of the fundamental unit: $\left((5+\sqrt{21})/2\right)^{3}=55+12\sqrt{21}$ ([fundamental unit](https://en.wikipedia.org/wiki/Fundamental_unit_%28number_theory%29)).

## 5. Analytic Number Theory

### 5.1. Quadratic Gauss Sum

For the real primitive character of discriminant $21$, the Kronecker page gives $\chi_{21}(n)=\left(\frac{21}{n}\right)$ and conductor $|D|=21$ ([Kronecker symbol](https://en.wikipedia.org/wiki/Kronecker_symbol)). The same page gives $\left(\frac{\cdot}{21}\right)=\left(\frac{21}{\cdot}\right)$ because the odd part of $21$ is $1 \pmod 4$. For odd prime factors, the Jacobi symbol agrees with the Legendre factors ([Jacobi symbol](https://en.wikipedia.org/wiki/Jacobi_symbol)):
$$\chi_{21}(n)=\left(\frac{21}{n}\right)=\left(\frac{3}{n}\right)\left(\frac{7}{n}\right)$$
$$g(\chi_{21}) = \sum_{n=0}^{20} \chi_{21}(n)\, e^{2\pi i n/21}$$

The Gauss-sum theorem gives $\lvert g(\chi)\rvert=\sqrt{N}$ only when $\chi$ is primitive, equivalently when its conductor equals its modulus ([Gauss sum](https://en.wikipedia.org/wiki/Gauss_sum); [Dirichlet character](https://en.wikipedia.org/wiki/Dirichlet_character)). Square-free modulus alone does not establish primitivity. Here that equality is the fetched conductor statement, so $\lvert g(\chi_{21})\rvert=\sqrt{21}$. For coprime moduli, the same Gauss-sum page gives $G(\chi\chi')=\chi(N')\chi'(N)G(\chi)G(\chi')$. The phase $\chi_3(7)\chi_7(3)$ equals $-1$, so the identity is not the phase-free product $g(\chi_3)g(\chi_7)$. The moduli nevertheless multiply:
$$\lvert g(\chi_{21})\rvert^{2} = 3 \cdot 7 = 21 \quad \Rightarrow \quad \boxed{\Lambda(6) = \frac{1}{\lvert g(\chi_{21})\rvert}}$$

### 5.2. Class Number of Real Quadratic Field $\mathbb{Q}(\sqrt{21})$

The ideal class number is $h(\mathbb{Q}(\sqrt{21})) = 1$ ([list of class-number-one fields](https://en.wikipedia.org/wiki/List_of_number_fields_with_class_number_one)). This means the ring of integers is a principal ideal domain, hence a unique-factorization domain. Every ring of integers already has unique factorization of ideals, so class number one is not what creates that ideal factorization. A principal form of discriminant $21$ is $(1,1,-5)$, since $1^{2}-4(1)(-5)=21$. The form $(1,5,1)$ has discriminant $25-4=21$, but $\lvert b\rvert \le a \le c$ is a positive-definite reduction test. It does not by itself prove that the indefinite class number is one.

### 5.3. Dirichlet Class Number Formula

For fundamental discriminant $d = 21$, the fundamental unit is $\varepsilon_{21} = (5 + \sqrt{21})/2$. It has norm $+1$, since $5^{2} - 21\cdot 1^{2} = 4$ and no smaller positive solution of $t^{2} - 21u^{2} = \pm 4$ exists. The fundamental solution of $x^{2} - 21y^{2} = 1$ is $(55, 12)$, convergent index $5$, and $\varepsilon_{21}^{3}=55+12\sqrt{21}$. Dirichlet's formula uses $\log \varepsilon_{21}$, not $\log(55 + 12\sqrt{21})$, which is three times as large. Its character is $\chi(m)=\left(\frac{d}{m}\right)$, so $\chi_{21}$ is the same character as in section 5.1 ([class number formula](https://en.wikipedia.org/wiki/Class_number_formula); [fundamental unit](https://en.wikipedia.org/wiki/Fundamental_unit_%28number_theory%29)):
$$h(21) = \frac{\sqrt{21}}{2\log \varepsilon_{21}}\, L(1, \chi_{21})$$

Substituting $h(21) = 1$:
$$\boxed{\Lambda(6) = \frac{1}{\sqrt{21}} = \frac{L(1, \chi_{21})}{2\log \varepsilon_{21}}}$$

**Numerical Verification**:
$$L(1, \chi_{21}) = 2\log \varepsilon_{21} \cdot \Lambda(6) = 0.6838072478309644\ldots$$

### 5.4. Synthesis of Analytic Formulas

| #   | Analytical Formula                                      | Theoretical Framework   |
| --- | ------------------------------------------------------- | ----------------------- |
| A   | $\Lambda(6) = 1/\sqrt{21}$                              | Elementary algebra      |
| B   | $\Lambda(6) = 1/\lvert g(\chi_{21})\rvert$              | Quadratic Gauss sums    |
| C   | $\Lambda(6) = L(1, \chi_{21})/(2\log \varepsilon_{21})$ | Dirichlet class numbers |
| D   | $\Lambda(6) = 1/\sqrt{\dim S_{24}(\Gamma_{0}(6))}$      | Modular forms theory    |
| E   | $\Lambda(6) = \sqrt{\zeta(6)/(2\pi^{2}\zeta(4))}$       | Euler Zeta identities   |

**Proof for Formula D**: For level $N = 6$, the dimension formula for cusp forms of even weight $k \ge 4$ ([Stein, Proposition 6.1](https://wstein.org/books/modform/modform/dimension_formulas.html), citing Diamond and Shurman) is given by:
$$\dim S_{k}(\Gamma_{0}(N)) = (k-1)(g-1) + \left\lfloor \tfrac{k}{4} \right\rfloor \nu_{2} + \left\lfloor \tfrac{k}{3} \right\rfloor \nu_{3} + \left(\tfrac{k}{2} - 1\right) \nu_{\infty}$$
where for level $N = 6$, the modular curve has genus $g = 0$ and cusp count $\nu_{\infty} = 4$. Stein sets $\mu_{0,2}(N)=0$ when $4 \mid N$; since $4 \nmid 6$, the product applies, and $\left(\frac{-4}{2}\right)=0$ makes $\nu_{2}=0$. Stein sets $\mu_{0,3}(N)=0$ when $2 \mid N$, so $\nu_{3}=0$ ([Stein, definitions preceding Proposition 6.1](https://wstein.org/books/modform/modform/dimension_formulas.html)). At weight $k = 24$:
$$\dim S_{24}(\Gamma_{0}(6)) = (24-1)(0-1) + 0 + 0 + \left(\frac{24}{2}-1\right) \cdot 4 = -23 + 44 = 21.$$
Hence $1/\sqrt{\dim S_{24}(\Gamma_{0}(6))} = 1/\sqrt{21}$. This is one weight at one level, not an identity for arbitrary cusp-form spaces.

### 5.5. Euler Zeta Function Ratio Identity: $\zeta(6)/\zeta(4) = 2\pi^{2}/21$

From the cited formula for positive even zeta values ([particular values](https://en.wikipedia.org/wiki/Particular_values_of_the_Riemann_zeta_function)):
$$\zeta(n) = (-1)^{n/2+1}\frac{(2\pi)^{n} B_{n}}{2 \cdot n!}$$

For $k = 2$ and $k = 3$:

- $\zeta(4) = \pi^{4}/90$
- $\zeta(6) = \pi^{6}/945$

**Closed-Form Ratio**:
$$\frac{\zeta(6)}{\zeta(4)} = \frac{\pi^{6}/945}{\pi^{4}/90} = \pi^{2} \cdot \frac{90}{945} = \frac{2\pi^{2}}{21}$$

**Connection to $\Lambda(6)$**: Substituting $21 = 1/\Lambda(6)^{2}$:
$$\boxed{\frac{\zeta(6)}{\zeta(4)} = 2\pi^{2} \cdot \Lambda(6)^{2} \quad \Leftrightarrow \quad \Lambda(6) = \sqrt{\frac{\zeta(6)}{2\pi^{2} \zeta(4)}}}$$

**Numerical Evaluation**:
The six-decimal truncations $\zeta(6) \approx 1.017343$, $\pi^{2} \approx 9.869604$, and $\zeta(4) \approx 1.082323$ are not accurate enough to recover 16 digits of $\Lambda(6)$. The closed form itself returns
$$\sqrt{\frac{\zeta(6)}{2\pi^{2}\zeta(4)}} = \frac{1}{\sqrt{21}} = 0.21821789023599238\ldots$$

**Divisibility of Zeta Denominators**: The values below are the lowest-term denominators of $\zeta(2k)/\pi^{2k}$. [OEIS A002432](https://oeis.org/A002432) starts at offset $0$, so its $a(0)=2$ is the denominator at $k=0$; the row for $k$ is its term $a(k)$, including $a(2)=90$:

| $k$ | $\zeta(2k)/\pi^{2k}$ in lowest terms | Denominator divisible by $21$ |
| --- | ------------------------------------ | ----------------------------: |
| 1   | $1/6$                                |                            no |
| 2   | $1/90$                               |                            no |
| 3   | $1/945$                              |                       yes, 45 |
| 4   | $1/9450$                             |                      yes, 450 |
| 5   | $1/93555$                            |                     yes, 4455 |
| 6   | $691/638512875$                      |                 yes, 30405375 |

The displayed rows stop at $k = 6$. Separately, the reduced denominators were checked for $3 \le k \le 20$, and each is divisible by $21$. Neither check proves the pattern for every larger $k$.

## 6. Reproducibility

### 6.1. Final Expression

$$\boxed{\Lambda(x) = \sqrt{2\,B(x,2)} = \sqrt{\frac{2\,\Gamma(x)}{\Gamma(x+2)}} = \frac{\sqrt{2}}{\sqrt{x(x+1)}}}, \quad \Lambda(6) = \frac{1}{\sqrt{21}}$$

### 6.2. Master Index

| Domain                                 | Key Correlation                                                                                                                                        |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Numerical display                      | $\tau = 100/\sqrt{21}$ is a base-10 display, not an independent invariant                                                                              |
| Triangular and Figurate Geometry       | $\Lambda(n) = 1/\sqrt{T(n)}$ for every positive integer $n$                                                                                            |
| Statistics and Artificial Intelligence | Parameter substitutions in attention, Xavier, He, and sample-mean standard-error formulas                                                              |
| Time Series Analysis                   | $\text{AR}(1)$ variance factor $21/20$ when $\phi = 1/\sqrt{21}$                                                                                       |
| Relativistic Physics                   | Static Schwarzschild factor at $r/r_{s}=21/20$; $\Phi=-10/21$ is algebraic notation, not the Newtonian-limit potential                                 |
| Chemical and Biological Kinetics       | First-order reaction rate $k = \ln 2 \cdot \sqrt{21}$                                                                                                  |
| Game Theory and Economics              | First-price auction $20/21$, Cournot output $1/21$                                                                                                     |
| Information Theory                     | Fixed-length alphabet ceiling $\lceil \log_{2} 21 \rceil = 5$; no Shannon-limit identity is derived                                                    |
| Geophysics and Planetary Science       | Upper-mantle viscosity spans $10^{19}$--$10^{24}$ Pa·s; transmission-line $\Gamma$ is a chosen input                                                   |
| Engineering Dynamics                   | Harmonic period $T = 2\pi/\sqrt{21}$                                                                                                                   |
| Medical Statistics                     | Per-group clinical-trial scale $n = 42(z_{\alpha}+z_{\beta})^{2}$ when $d = 1/\sqrt{21}$                                                               |
| Continuous Special Functions           | Euler Beta generalization $\Lambda(x) = \sqrt{2\,B(x,2)}$                                                                                              |
| Exponential Family Distributions       | Poisson distribution skewness $\gamma_{1} = \Lambda(6)$                                                                                                |
| Discrete Combinatorics                 | Multi-combinatorial equality $F_{8} = M_{5} = c(7,6) = 21$                                                                                             |
| Polygonal Sequences                    | Octagonal-triangular identity $T(6) = O(3) = 21$                                                                                                       |
| Graph Theory                           | Ramsey critical number $R(3,3) = 6$                                                                                                                    |
| Character Theory                       | Quadratic Gauss sum modulus $\lvert g(\chi_{21})\rvert = \sqrt{21}$ ([Gauss sum](https://en.wikipedia.org/wiki/Gauss_sum))                             |
| Algebraic Number Theory                | Class number $h(\mathbb{Q}(\sqrt{21})) = 1$ ([class-number-one fields](https://en.wikipedia.org/wiki/List_of_number_fields_with_class_number_one))     |
| Analytic Number Theory                 | Dirichlet formula $\Lambda(6) = L(1, \chi_{21})/(2\log \varepsilon_{21})$                                                                              |
| Automorphic Forms                      | Cusp dimension $\dim S_{24}(\Gamma_{0}(6)) = 21$ ([dimension formula](https://wstein.org/books/modform/modform/dimension_formulas.html))               |
| Classical Analysis                     | Euler Zeta ratio $\zeta(6)/\zeta(4) = 2\pi^{2}/21$ ([particular values](https://en.wikipedia.org/wiki/Particular_values_of_the_Riemann_zeta_function)) |

## 7. Sources

Each link was checked against the sentence it supports. A substitution row uses the cited formula, not a result discovered by that source.

**Number theory**

- Triangular numbers: [Wikipedia](https://en.wikipedia.org/wiki/Triangular_number)
- Binomial coefficient: [Wikipedia](https://en.wikipedia.org/wiki/Binomial_coefficient)
- Polygonal formula $P(s,n)=((s-2)n^{2}-(s-4)n)/2$: [Wikipedia](https://en.wikipedia.org/wiki/Polygonal_number)
- Fibonacci indexing with $F_{0}=0$, including $F_{8}=21$: [Wikipedia](https://en.wikipedia.org/wiki/Fibonacci_sequence)
- One-step Stirling identities $S(n,n-1)=c(n,n-1)=\binom{n}{2}$: [first kind](https://en.wikipedia.org/wiki/Stirling_numbers_of_the_first_kind), [second kind](https://en.wikipedia.org/wiki/Stirling_numbers_of_the_second_kind)
- Motzkin numbers, including $M_{5}=21$: [Wikipedia](https://en.wikipedia.org/wiki/Motzkin_number)
- Hook-length formula $f^{\lambda}=n!/\prod h_{\lambda}(i,j)$: [Wikipedia](https://en.wikipedia.org/wiki/Hook-length_formula)
- Semiprime: [Wikipedia](https://en.wikipedia.org/wiki/Semiprime)
- Multiplicative order: [Wikipedia](https://en.wikipedia.org/wiki/Multiplicative_order)
- Carmichael function, including the table value $\lambda(21)=6$: [Wikipedia](https://en.wikipedia.org/wiki/Carmichael_function); definition [DOI 10.1090/S0002-9904-1910-01892-9](https://doi.org/10.1090/S0002-9904-1910-01892-9)
- Continued-fraction periodicity of non-square roots: [Wikipedia](https://en.wikipedia.org/wiki/Continued_fraction)
- Pell fundamental solution and even-period convergent rule: [Wikipedia](https://en.wikipedia.org/wiki/Pell%27s_equation)
- Euler Beta function: [Wikipedia](https://en.wikipedia.org/wiki/Beta_function)
- Fibonacci-triangular theorem: [Luo Ming, Fibonacci Quarterly 27.2 (1989), PDF](https://www.fq.math.ca/Scanned/27-2/ming.pdf); sequence [OEIS A039595](https://oeis.org/A039595)
- Octagonal-triangular sequence: [OEIS A046183](https://oeis.org/A046183)
- Ramsey existence theorem: [DOI 10.1112/plms/s2-30.1.264](https://doi.org/10.1112/plms/s2-30.1.264); evaluation $R(3,3)=6$: [Wikipedia](https://en.wikipedia.org/wiki/Ramsey%27s_theorem)
- Real primitive character $\chi(n)=(21/n)$, conductor $|D|=21$: [Kronecker symbol](https://en.wikipedia.org/wiki/Kronecker_symbol); Jacobi factorization: [Jacobi symbol](https://en.wikipedia.org/wiki/Jacobi_symbol)
- Primitive Gauss-sum modulus and coprime product phase: [Gauss sum](https://en.wikipedia.org/wiki/Gauss_sum); conductor definition: [Dirichlet character](https://en.wikipedia.org/wiki/Dirichlet_character)
- Class number one and its implication: [Wikipedia](https://en.wikipedia.org/wiki/List_of_number_fields_with_class_number_one)
- Dirichlet class-number formula: [Wikipedia](https://en.wikipedia.org/wiki/Class_number_formula)
- Fundamental unit: [Wikipedia](https://en.wikipedia.org/wiki/Fundamental_unit_%28number_theory%29)
- Cusp-form dimension, Proposition 6.1: [Stein](https://wstein.org/books/modform/modform/dimension_formulas.html), citing Diamond and Shurman
- Even zeta values: [Wikipedia](https://en.wikipedia.org/wiki/Particular_values_of_the_Riemann_zeta_function)
- Bernoulli sign convention, including $B_{6}=+1/42$: [Wikipedia](https://en.wikipedia.org/wiki/Bernoulli_number)
- Zeta denominators: [OEIS A002432](https://oeis.org/A002432)

**Statistics and machine learning**

- Standard error of the mean, $\sigma/\sqrt{n}$ for independent observations: [Wikipedia](https://en.wikipedia.org/wiki/Standard_error)
- Natural exponential families with quadratic variance: [Morris, Annals of Statistics 10 (1982)](https://projecteuclid.org/journals/annals-of-statistics/volume-10/issue-1/Natural-Exponential-Families-with-Quadratic-Variance-Functions/10.1214/aos/1176345690.full)
- Distribution moments used above: [Poisson](https://en.wikipedia.org/wiki/Poisson_distribution), [gamma](https://en.wikipedia.org/wiki/Gamma_distribution), [chi-squared](https://en.wikipedia.org/wiki/Chi-squared_distribution), [binomial](https://en.wikipedia.org/wiki/Binomial_distribution), [Erlang](https://en.wikipedia.org/wiki/Erlang_distribution)
- Jeffreys prior: [Wikipedia](https://en.wikipedia.org/wiki/Jeffreys_prior)
- Scaled dot-product attention: [Vaswani et al., arXiv:1706.03762](https://arxiv.org/abs/1706.03762)
- Xavier uniform initialization: [Glorot and Bengio, PMLR 9](https://proceedings.mlr.press/v9/glorot10a.html)
- ReLU initialization, standard deviation $\sqrt{2/n_{l}}$: [He et al., arXiv:1502.01852](https://arxiv.org/abs/1502.01852)
- Diffusion forward-process standard deviation: [Ho, Jain, and Abbeel, arXiv:2006.11239](https://arxiv.org/abs/2006.11239)
- Two-group sample-size formula: [Cohen, Statistical Power Analysis, 2nd ed., DOI](https://doi.org/10.4324/9780203771587)

**Physics, biology, and applied formulas**

- Static exterior Schwarzschild factor $t_{0}=t_{f}\sqrt{1-r_{s}/r}$: [gravitational time dilation](https://en.wikipedia.org/wiki/Gravitational_time_dilation). Redshift from infinity is the reciprocal: [gravitational redshift](https://en.wikipedia.org/wiki/Gravitational_redshift)
- Reciprocal of the Lorentz factor, $\gamma=1/\sqrt{1-v^{2}/c^{2}}$: [Wikipedia](https://en.wikipedia.org/wiki/Lorentz_factor)
- Harmonic oscillator period: [Wikipedia](https://en.wikipedia.org/wiki/Harmonic_oscillator)
- Nonlinear molecular vibrations: [Wikipedia](https://en.wikipedia.org/wiki/Molecular_vibration)
- Mantle viscosity range: [Wikipedia](https://en.wikipedia.org/wiki/Earth%27s_mantle)
- Calculated baseline $N_{\mathrm{eff}}=3.044$, with numerical and mixing error at most $0.0005$: [Akita and Yamaguchi, arXiv:2005.07047](https://arxiv.org/abs/2005.07047)
- Michaelis-Menten equation, English translation of the 1913 paper: [DOI 10.1021/bi201284u](https://doi.org/10.1021/bi201284u)
- Bazett correction: [Bazett 1920, DOI 10.1111/j.1542-474X.1997.tb00325.x](https://doi.org/10.1111/j.1542-474X.1997.tb00325.x); summary [Wikipedia](https://en.wikipedia.org/wiki/QT_interval)
- First-order half-life: [Wikipedia](https://en.wikipedia.org/wiki/Rate_equation)
- Q factor: [Wikipedia](https://en.wikipedia.org/wiki/Q_factor). Second-order percentage overshoot: [overshoot](https://en.wikipedia.org/wiki/Overshoot_%28signal%29)
- Fixed-length alphabet ceiling: [prefix code](https://en.wikipedia.org/wiki/Prefix_code). Huffman weighted path length is a separate claim: [Huffman coding](https://en.wikipedia.org/wiki/Huffman_coding)
- Herd-immunity threshold and its mixing assumptions: [Wikipedia](https://en.wikipedia.org/wiki/Herd_immunity)
- First-price auction: $(n-1)/n \cdot v$ is the page's symmetric BNE for i.i.d. uniform $[0,1]$ valuations; its general symmetric BNE is $E[y_i \mid y_i<v_i]$: [Wikipedia](https://en.wikipedia.org/wiki/First-price_sealed-bid_auction)
- Kelly criterion: the binary formula $f=p/l-q/g$, and $f=2p-1$ for even money $g=l=1$: [Wikipedia](https://en.wikipedia.org/wiki/Kelly_criterion). Kelly 1956 gives the same even-money fraction with swapped labels: [PDF](https://www.princeton.edu/~wbialek/rome/refs/kelly_56.pdf)
- Cournot oligopoly: [Cournot 1838](https://archive.org/details/recherchessurles00cour). The linear identical-firm output $(a-c)/((n+1)b)$: [Marker](https://homepages.math.uic.edu/~marker/stat473-s19/Cournot.pdf)
- Echo-state networks: [Jaeger 2001, Fraunhofer record](https://publica.fraunhofer.de/entities/publication/7d4a7eec-a22c-4df0-903d-93d0c6c1f0e5). The corrected report sets its example input weights to $\pm 1$ and does not prescribe $1/\sqrt{N}$: [PDF](https://www.ai.rug.nl/minds/uploads/EchoStatesTechRep.pdf)
- Hash-table load factor $\alpha = n/m$: [Wikipedia](https://en.wikipedia.org/wiki/Hash_table)
- Fisher information: [Wikipedia](https://en.wikipedia.org/wiki/Fisher_information)
- Reflection coefficient $(Z_L-Z_0)/(Z_L+Z_0)$: [Wikipedia](https://en.wikipedia.org/wiki/Reflection_coefficient)
- Ideal-gas adiabatic index $1+2/f$: [Wikipedia](https://en.wikipedia.org/wiki/Heat_capacity_ratio)
- Absolute bioavailability: [Wikipedia](https://en.wikipedia.org/wiki/Bioavailability)
- AR(1) stationary variance: [Wikipedia](https://en.wikipedia.org/wiki/Autoregressive_model)
- Kepler's third law: [Wikipedia](https://en.wikipedia.org/wiki/Kepler%27s_laws_of_planetary_motion)
- Gutenberg-Richter relation: [Wikipedia](https://en.wikipedia.org/wiki/Gutenberg%E2%80%93Richter_law)

## Cite

If you find Triangular Root Invariant helpful in your research cite simply as:

```bibtex
@misc{triangular-root-invariant,
  author = {NeaByteLab},
  title = {Triangular Root Invariant: The Inverse Root of Twenty-One},
  year = {2026},
  publisher = {GitHub},
  url = {https://github.com/NeaByteLab/Triangular-Root-Invariant}
}
```

## License

This repository is Licensed under [CC BY 4.0](LICENSE).
