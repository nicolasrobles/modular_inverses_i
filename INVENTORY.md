# Statement and proof-dependency inventory

**Discrepancy and local statistics of modular inverses - v39.**

This inventory records **26 numbered results and 5 numbered remarks**. Results stated in the introduction are counted once, even when their proofs occur later. Equation numbers and statement numbers are separate numbering systems.

The complete map also records **45 supporting steps** and **11 literature records**. These are documentation entries, not additional numbered results.

[README](README.md) · [Dependency guide](DEPENDENCIES.md) · [Numbered graph (PDF)](docs/dependency_graph.pdf) · [Complete graph (PDF)](docs/dependency_complete.pdf) · [Machine-readable record](docs/dependency_inventory.json)

## Source and status

- Baseline: `modular_inverse_discrepancy_v39.tex`.
- SHA-256: `03bb313d26bb491a742178ce0051f646c0af19b12af4ce3662577b481b93e2db`.
- Locations are one-based lines in that source; statement pages refer to its compiled PDF.
- The manuscript is not distributed in this repository.
- Formalization has not started. There are no Lean declarations or kernel-checked results here.

Graph colours follow the model repository: purple for trusted references, green for certified entries, and yellow for pending certification. All internal entries currently have pending certification status; this status is separate from the mathematical audit.

The **basis** column describes how v39 presents the item: a cited input, an in-text proof, or a transfer of an earlier argument. It does not certify the proof. Summaries abbreviate the statements; their full hypotheses remain in the identified manuscript.

| Kind | Count |
| --- | ---: |
| Theorem | 6 |
| Corollary | 10 |
| Lemma | 6 |
| Proposition | 4 |
| Remark | 5 |

## Numbered statements

### Section 1: Introduction

| Item | Summary | Basis and source |
| --- | --- | --- |
| <a id="thm-perimeter"></a>**Theorem 1.1**<br>`thm:perimeter`<br>Convex discrepancy with perimeter dependence | For convex sets represented inside a translated unit square, bounds discrepancy by $X^{\varepsilon}(X^{-1}+P^{2/3}X^{-2/3})$, uniformly in the position and the set, for $X\ge2$. | Proved in v39. Statement 196-201; PDF p. 3; proof 771-791. |
| <a id="cor-isotropic"></a>**Corollary 1.2**<br>`cor:isotropic`<br>Isotropic discrepancy bound | Taking the supremum over the manuscript's class of convex sets gives discrepancy $\ll_{\varepsilon}X^{-2/3+\varepsilon}$. | Proved in v39. Statement 203-208; PDF p. 3; proof 793-795. |
| <a id="cor-shrinking"></a>**Corollary 1.3**<br>`cor:shrinking`<br>Relative counting for shrinking convex shapes | For a fixed convex body of positive area and $0<\kappa<1/2$, obtains relative error $O_{K_0,\kappa}(X^{-\kappa})$ at dilations $t\ge X^{-1/2+\kappa}$ that fit inside a translated unit square, uniformly over translations and rotations. | Proved in v39. Statement 218-223; PDF p. 4; proof 797-803. |
| <a id="thm-boundary"></a>**Theorem 1.4**<br>`thm:boundary`<br>Discrepancy from topological boundary neighborhoods | If $b_E(s)\le Bs^{\alpha}$ for $0<s\le1$, $0<\alpha\le1$ and $B\ge1$, gives $D_X(E)\ll_{\varepsilon}B^{2/(2+\alpha)}X^{-2\alpha/(2+\alpha)+\varepsilon}$ for $X\ge2$. | Proved in v39. Statement 237-242; PDF p. 4; proof 872-912. |
| <a id="thm-differences"></a>**Theorem 1.5**<br>`thm:differences`<br>Distribution of ordered differences | The difference measure, including diagonal pairs, has discrepancy $\ll_\varepsilon X^\varepsilon(PX^{-1}+X^{-2})$ for a convex set of perimeter $P$ in a translated unit square. For a product of arcs of area $V$, the bound is $\ll_\varepsilon X^\varepsilon(X^{-2}+V^{2/3}X^{-5/3})$, independently of its aspect ratio. | Proved in v39. Statement 252-261; PDF p. 4; proof 956-979; 997-1031. |
| <a id="thm-variance"></a>**Theorem 1.6**<br>`thm:variance`<br>Variance of counts in translates | The variance of the normalized count is $\ll_\varepsilon X^\varepsilon(P^2X^{-2}+A^{4/3}P^{2/3}X^{-5/3})$ for a convex set with area $A$ and perimeter $P$. Products of arcs satisfy $\ll_\varepsilon X^\varepsilon(VX^{-2}+V^{5/3}X^{-5/3})$, and discs satisfy $\ll_\varepsilon X^\varepsilon(r^2X^{-2}+r^{10/3}X^{-5/3})$. If every translate contains at most one point, the variance equals $\vert E\vert /N_X-\vert E\vert ^2$. | Proved in v39. Statement 271-289; PDF p. 5; proof 1087-1117. |
| <a id="thm-distance"></a>**Theorem 1.7**<br>`thm:distance`<br>Moments of the distance to the point set | For every fixed $s>0$, the $s$-th distance moment lies between constant multiples of $X^{-\vartheta(s)}$ and $X^{-\vartheta(s)+\varepsilon}$, where $\vartheta(s)=\min\{s,1+s/2\}$. Thus the exponents change at $s=2$. | Proved in v39. Statement 299-305; PDF p. 5; proof 1169-1198. |

### Section 2: Preliminary lemmas

| Item | Summary | Basis and source |
| --- | --- | --- |
| <a id="thm-brs-input"></a>**Theorem 2.1**<br>`thm:brs-input`<br>The BRS frequency second moment | For all real $N,X\ge1$ and $\eta>0$, $\sum_{N\le\vert r\vert <2N}\vert A_X(r,1)\vert ^2\ll_\eta(NX)^\eta(NX^2+N^{1/3}X^{7/3})$. Both signs are included, with no relation between $N$ and $X$. | Cited input. Statement 376-381; PDF p. 8. |
| <a id="cor-brs-cumulative"></a>**Corollary 2.2**<br>`cor:brs-cumulative`<br>Cumulative frequency second moment | For real $R,Y\ge1$, the sum over $1\le\vert r\vert \le R$ is $\ll_\eta(RY)^\eta(RY^2+R^{1/3}Y^{7/3})$. | Derived in v39. Statement 385-390; PDF p. 8; proof 391-397. |
| <a id="prop-rectangular"></a>**Proposition 2.3**<br>`prop:rectangular`<br>Second moment over a frequency rectangle | For $M,N,X\ge1$, $\sum_{\vert m\vert \le M,\ \vert n\vert \le N,\ (m,n)\ne(0,0)}\vert A_X(m,n)\vert ^2\ll_\varepsilon(MNX)^\varepsilon\{MNX^2+(MN)^{1/3}X^{7/3}\}$. The axes and all signs are included. | Proved in v39. Statement 410-415; PDF p. 8; proof 416-450. |
| <a id="cor-shell"></a>**Corollary 2.4**<br>`cor:shell`<br>Normalized moments on frequency shells | For $X\ge2$ and $H\ge1$, the shell $\ell^2$ norm is $\ll_\eta(HX)^\eta(X^{-1}H+X^{-5/6}H^{1/3})$. Its square is $\ll_\eta(HX)^\eta(X^{-2}H^2+X^{-5/3}H^{2/3})$, and $\vert a_X(k)\vert ^2\le1$. | Derived in v39. Statement 454-464; PDF p. 9; proof 465-471. |
| <a id="lem-translation"></a>**Lemma 2.5**<br>`lem:translation`<br>Fourier tail from an L2 translation estimate | If $g\in L^2(\mathbb T^2)$ satisfies $\Vert g(\cdot+h)-g\Vert _2^2\le\Lambda\vert h\vert _2^\alpha$ for $\vert h\vert _2\le1$, with $0<\alpha\le1$ and $\Lambda\ge0$, then $\sum_{\Vert k\Vert _\infty\ge H}\vert \widehat g(k)\vert ^2\le 2^{-\alpha/2}\Lambda H^{-\alpha}/[2(1-1/\pi)]$ for every real $H\ge1$. | Proved in v39. Statement 481-491; PDF p. 10; proof 492-507. |
| <a id="lem-brackets"></a>**Lemma 2.6**<br>`lem:brackets`<br>Pointwise smooth brackets for measurable sets | For measurable $E\subset\mathbb T^2$ and $0<\delta\le1/8$, constructs smooth real $f_-\le\mathbf1_E\le f_+$ at every point, with values in $[0,1]$. The integral error is at most $b_E(3\delta)$; Fourier coefficients and shell norms gain $(1+\delta H)^{-L}$ with boundary errors $b_E(3\delta)$ and $b_E(3\delta)^{1/2}$ respectively. | Proved in v39. Statement 530-545; PDF p. 11; proof 546-570. |
| <a id="lem-convex-geometry"></a>**Lemma 2.7**<br>`lem:convex-geometry`<br>Boundary, translation and Fourier bounds for convex sets | For convex $\Omega\subset u+[0,1)^2$, $E=\pi\Omega$, perimeter $P$ and area $A$, proves $b_E(s)\le4\pi(Ps+s^2)$, $\Vert \mathbf1_E(\cdot+h)-\mathbf1_E\Vert _2^2\le P\vert h\vert _2$, Fourier tail $\ll P/T$, and $\vert \widehat{\mathbf1_E}(k)\vert \le\min(A,P/(4\vert k\vert _2))$ for $k\ne0$. Degenerate convex sets are included. | Proved in v39. Statement 578-587; PDF p. 12; proof 588-615. |
| <a id="cor-convex-brackets"></a>**Corollary 2.8**<br>`cor:convex-brackets`<br>Fourier estimates for convex brackets | For $0<\delta\le1/8$ and $H\ge1$, with $b=P\delta+\delta^2$, the brackets have integral error $\ll b$, shell norm $\ll_L(1+\delta H)^{-L}(P^{1/2}H^{-1/2}+b^{1/2})$, and coefficient bound $\ll_L(1+\delta H)^{-L}(P/H+b)$. | Derived in v39. Statement 619-626; PDF p. 13; proof 627-629. |
| <a id="rem-tube-to-translation"></a>**Remark 2.9**<br>`rem:tube-to-translation`<br>A boundary-tube bound implies a translation bound | For any measurable $E$ with $b_E(s)\le C_0(Ps+s^2)$ for $0<s\le1$, subdivision of a translation gives $\Vert \mathbf1_E(\cdot+h)-\mathbf1_E\Vert _1\le C_0P\vert h\vert _2$ for $\vert h\vert _2<1$. The separate convex slicing argument supplies the sharper constant used in (2.20). | In-text deduction. Statement 631-633; PDF p. 14; proof 632. |

### Section 3: Fourier analysis of the point set

| Item | Summary | Basis and source |
| --- | --- | --- |
| <a id="prop-identities"></a>**Proposition 3.1**<br>`prop:identities`<br>Fourier identities for counting, differences and variance | For $X\ge2$, smooth counting error is $\sum_{k\ne0}\widehat f(k)a_X(k)$, smooth difference-distribution error is $\sum_{k\ne0}\widehat f(k)\vert a_X(k)\vert ^2$, and for every measurable $E$ the translation variance is $\sum_{k\ne0}\vert \widehat{\mathbf1_E}(k)\vert ^2\vert a_X(k)\vert ^2$. | Proved in v39. Statement 641-660; PDF p. 14; proof 661-684. |
| <a id="rem-overlap"></a>**Remark 3.2**<br>`rem:overlap`<br>Variance as an average of the overlap function | For $C_E(v)=\int\mathbf1_E(x)\mathbf1_E(x+v)\,dx$, direct expansion gives $\mathcal V_X(E)=\int C_E\,d\nu_X-\vert E\vert ^2$. The variance theorem uses the Fourier variance identity directly, independently of the difference-distribution theorem. | In-text deduction. Statement 688-690; PDF p. 15; proof 689. |

### Section 4: Discrepancy of convex and well-shaped sets

| Item | Summary | Basis and source |
| --- | --- | --- |
| <a id="lem-dyadic"></a>**Lemma 4.1**<br>`lem:dyadic`<br>Dyadic sums against smoothing decay | Controls the dyadic sum of $H^s(1+\delta H)^{-L}$ by $\delta^{-s}$ for $s>0$ and by a constant for $s<0$, with $L>\max(s,0)$ and $0<\delta\le1$. | Proved in v39. Statement 724-729; PDF p. 16; proof 730-732. |
| <a id="prop-smoothing"></a>**Proposition 4.2**<br>`prop:smoothing`<br>Smoothing inequality for convex discrepancy | At any $0<\delta\le1/8$, controls convex discrepancy by the boundary error $b=P\delta+\delta^2$ and the Fourier contributions with scales $X^{-1}\delta^{-1/2}$ and $X^{-5/6}$. | Proved in v39. Statement 734-739; PDF p. 16; proof 740-765. |
| <a id="prop-coordinate-separation"></a>**Proposition 4.3**<br>`prop:coordinate-separation`<br>Elementary discrepancy from coordinate separation | For convex sets in a translated unit square, gives the absolute-constant bound $D_X(\pi\Omega)\ll X^{-2}+\min(w_1,w_2)\ll X^{-2}+P(\Omega)$ for $X\ge2$. | Proved in v39. Statement 809-814; PDF p. 18; proof 815-825. |
| <a id="cor-small-perimeter-sharp"></a>**Corollary 4.4**<br>`cor:small-perimeter-sharp`<br>Sharp discrepancy order for very small perimeters | For real $X\ge4$ and $0\le p\le X^{-1}$, the largest discrepancy among convex sets of perimeter at most p has order $p+X^{-2}$, with absolute constants. | Proved in v39. Statement 833-843; PDF p. 18; proof 844-858. |
| <a id="rem-positive-area"></a>**Remark 4.5**<br>`rem:positive-area`<br>A positive-area obstruction to deleting the baseline term | A thin rectangle containing many diagonal reciprocal points has discrepancy $\gg X^{-1}$ while its perimeter contribution is $O(X^{-4/3})$, so the baseline term in Theorem 1.1 remains necessary even for positive-area convex bodies. | Proved or explained in the remark. Statement 860-866; PDF p. 19; proof 860-866. |
| <a id="cor-well-shaped"></a>**Corollary 4.6**<br>`cor:well-shaped`<br>Discrepancy of well-shaped sets | For the Euclidean definition of gamma-well-shapedness inside $[0,1)^2$, gives discrepancy $\ll_{\varepsilon}(1+\gamma)^{2/3}X^{-2/3+\varepsilon}$, uniformly for $\gamma\ge0$ and $X\ge2$. | Proved in v39. Statement 920-925; PDF p. 20; proof 926-928. |
| <a id="rem-koch"></a>**Remark 4.7**<br>`rem:koch`<br>A fractal-boundary example beyond well-shaped sets | Applies the boundary theorem to a Koch snowflake inside the unit square, with $\alpha=2-\log 4/\log 3$, giving exponent $0.539\ldots$; the same domain is not gamma-well-shaped for any finite gamma. | Proved or explained in the remark. Statement 930-942; PDF p. 21; proof 930-942. |
| <a id="rem-topological-boundary"></a>**Remark 4.8**<br>`rem:topological-boundary`<br>Why the boundary hypothesis is pointwise | The finite set $E=\mathcal P_X$ has indicator zero almost everywhere but discrepancy one. Thus almost-everywhere or distributional-perimeter information cannot replace the stated pointwise/topological boundary control. | Proved or explained in the remark. Statement 944-946; PDF p. 21; proof 944-946. |

### Section 5: Local statistics

| Item | Summary | Basis and source |
| --- | --- | --- |
| <a id="lem-arc-brackets"></a>**Lemma 5.1**<br>`lem:arc-brackets`<br>Smooth pointwise brackets for arcs | An arc of length $a$ admits smooth upper and lower brackets with integral error at most $4\delta$. With $a'=\min(1,a+4\delta)$, their coefficients are $\ll_L\min\{a',(1+\vert m\vert )^{-1}\}(1+\delta\vert m\vert )^{-L}$. | Proved in v39. Statement 983-988; PDF p. 22; proof 989-995. |
| <a id="cor-difference-shrinking"></a>**Corollary 5.2**<br>`cor:difference-shrinking`<br>Relative asymptotics for shrinking difference sets | For $0<\kappa<1$, a fixed positive-area convex shape at linear scale $t\ge X^{-1+\kappa}$ has relative difference-count error $O(X^{-\kappa/2})$, uniformly in position and orientation within a translated unit square. Products of arcs have the same error when their area is at least $X^{-2+\kappa}$. Both conclusions hold with and without diagonal pairs under the corresponding normalizations. | Proved in v39. Statement 1042-1055; PDF p. 24; proof 1056-1066. |
| <a id="lem-one-point"></a>**Lemma 5.3**<br>`lem:one-point`<br>Exact variance for sets containing at most one point in each translate | If every translate of a measurable set contains at most one point, its normalized-count variance is $\vert E\vert /N_X-\vert E\vert ^2$. A sufficient condition is containment, after projection, in a strip of width below $X^{-2}$; the stated small-perimeter, narrow-rectangle and small-disc cases follow. | Proved in v39. Statement 1072-1078; PDF p. 24; proof 1079-1085. |
| <a id="cor-variance-shrinking"></a>**Corollary 5.4**<br>`cor:variance-shrinking`<br>Small exceptional sets for translates of shrinking convex shapes | For a fixed positive-area convex shape at scale $t\ge X^{-1+\kappa}$, the centers with relative count error greater than $\lambda$ have measure $\ll_{K_0,\kappa}\lambda^{-2}X^{-3\kappa/2}$, uniformly over admissible rotations and scales, for $0<\kappa<1$ and $0<\lambda\le1$. | Proved in v39. Statement 1121-1127; PDF p. 26; proof 1128-1134. |
| <a id="cor-simultaneous"></a>**Corollary 5.5**<br>`cor:simultaneous`<br>One exceptional set for a range of disc radii | For $r_0\le r\le1/4$, a single exceptional set has measure $\ll_\varepsilon\lambda^{-3}X^\varepsilon(X^{-2}r_0^{-2}+X^{-5/3}r_0^{-2/3})$ and outside it every disc count has relative error $O(\lambda)$. Open and closed discs are included. Taking $r_0=X^{-1+\kappa}$ and $\lambda=X^{-\kappa/3}$ yields exceptional measure $\ll_\kappa X^{-\kappa/2}$ for sufficiently large $X$. | Proved in v39. Statement 1140-1150; PDF p. 26; proof 1151-1165. |

## Direct dependencies of numbered statements

These are the predecessors in the complete documented graph. Where the proof is split into supporting calculations, follow the linked calculation to its inputs. The numbered-only graph suppresses those calculations and removes transitively redundant solid edges.

| Statement | Direct recorded inputs |
| --- | --- |
| [Theorem 1.1](#thm-perimeter) | [Proposition 4.2](#prop-smoothing); [Lemma 2.7](#lem-convex-geometry) |
| [Corollary 1.2](#cor-isotropic) | [Theorem 1.1](#thm-perimeter); [Lemma 2.7](#lem-convex-geometry) |
| [Corollary 1.3](#cor-shrinking) | [Theorem 1.1](#thm-perimeter) |
| [Theorem 1.4](#thm-boundary) | [Smoothing estimate for a general boundary tube bound](#eq-general-smoothing) |
| [Theorem 1.5](#thm-differences) | [Convex difference estimate from pointwise brackets and squared shells](#step-difference-convex-proof); [Product brackets and separate frequency summation for differences](#step-difference-box-proof) |
| [Theorem 1.6](#thm-variance) | [Convex variance from Fourier tails and squared shells](#step-variance-convex-proof); [Disc variance as a convex-set specialization](#step-variance-disc-proof); [Rectangle variance from squared arc coefficients](#step-variance-box-proof); [Lemma 5.3](#lem-one-point) |
| [Theorem 1.7](#thm-distance) | [Integrating the distance tail up to its uniform cutoff](#step-distance-upper); [Packing and the empty rectangle give the two distance lower bounds](#step-distance-lower) |
| [Theorem 2.1](#thm-brs-input) | [BRS second moment with one frequency fixed](#external-BRS-theorem-1-3) |
| [Corollary 2.2](#cor-brs-cumulative) | [Theorem 2.1](#thm-brs-input) |
| [Proposition 2.3](#prop-rectangular) | [Off-axis reduction of the rectangular second moment](#step-rectangular-divisor-reduction); [Axis contribution from Ramanujan sums](#step-axis-ramanujan-bound) |
| [Corollary 2.4](#cor-shell) | [Proposition 2.3](#prop-rectangular); [Point-set cardinality and quadratic scale](#step-cardinality-comparison); [Trivial bound for normalized point coefficients](#step-normalized-coefficient-bound) |
| [Lemma 2.5](#lem-translation) | [Parseval identity on the torus](#external-Grafakos-section-3-2-2); [Fourier coefficients of a translate](#step-fourier-translation-rule) |
| [Lemma 2.6](#lem-brackets) | [Positive periodic mollifier and Fourier decay](#eq-mollifier-decay); [Boundary-neighborhood control of smoothing errors](#eq-bracket-difference-norms); [Fourier coefficients of a convolution](#external-Grafakos-section-3-1-2); [Parseval identity on the torus](#external-Grafakos-section-3-2-2) |
| [Lemma 2.7](#lem-convex-geometry) | [Boundary tube bound for a projected convex set](#eq-convex-tube); [Convex translation estimate with constant one](#eq-convex-translation); [Fourier-energy tail for a convex indicator](#eq-convex-tail); [Pointwise Fourier decay for a convex indicator](#eq-convex-pointwise) |
| [Corollary 2.8](#cor-convex-brackets) | [Lemma 2.6](#lem-brackets); [Lemma 2.7](#lem-convex-geometry) |
| [Remark 2.9](#rem-tube-to-translation) | [Boundary crossing along a short torus path](#step-boundary-crossing); [Lemma 2.6](#lem-brackets) (proof method) |
| [Proposition 3.1](#prop-identities) | [Smooth Fourier identity for uniform counting](#eq-identity-mu); [Smooth Fourier identity for the difference measure](#eq-identity-nu); [Parseval identity for translation variance](#eq-identity-variance) |
| [Remark 3.2](#rem-overlap) | Direct in-text argument; see the source locator. |
| [Lemma 4.1](#lem-dyadic) | Direct in-text argument; see the source locator. |
| [Proposition 4.2](#prop-smoothing) | [From pointwise brackets to a Fourier discrepancy bound](#step-pointwise-discrepancy-reduction); [Corollary 2.8](#cor-convex-brackets); [Corollary 2.4](#cor-shell); [Lemma 4.1](#lem-dyadic) |
| [Proposition 4.3](#prop-coordinate-separation) | [Injective coordinate projections and counting in short intervals](#step-coordinate-counting); [Point-set cardinality and quadratic scale](#step-cardinality-comparison) |
| [Corollary 4.4](#cor-small-perimeter-sharp) | [Proposition 4.3](#prop-coordinate-separation); [Diagonal segments realizing the short-perimeter lower order](#step-short-perimeter-diagonal-lower) |
| [Remark 4.5](#rem-positive-area) | [Elementary upper bound for the point count](#step-cardinality-upper) |
| [Corollary 4.6](#cor-well-shaped) | [From Euclidean well-shapedness to torus boundary control](#step-well-shaped-torus-tube); [Theorem 1.4](#thm-boundary) |
| [Remark 4.7](#rem-koch) | [Tube control for a Koch boundary](#step-koch-tube); [Theorem 1.4](#thm-boundary); [From Euclidean well-shapedness to torus boundary control](#step-well-shaped-torus-tube) |
| [Remark 4.8](#rem-topological-boundary) | Direct in-text argument; see the source locator. |
| [Lemma 5.1](#lem-arc-brackets) | [Lemma 2.6](#lem-brackets) (proof method); [Positive periodic mollifier and Fourier decay](#eq-mollifier-decay) (proof method); [Fourier coefficients of an arc indicator](#step-arc-indicator-coefficients) |
| [Corollary 5.2](#cor-difference-shrinking) | [Theorem 1.5](#thm-differences); [Removing equal-point pairs](#eq-diagonal-removal) |
| [Lemma 5.3](#lem-one-point) | [Proposition 4.3](#prop-coordinate-separation) |
| [Corollary 5.4](#cor-variance-shrinking) | [Theorem 1.6](#thm-variance) |
| [Corollary 5.5](#cor-simultaneous) | [Theorem 1.6](#thm-variance) |

## Supporting steps

Identifiers beginning `step:`, `geom:` or `support:` are repository identifiers. They identify calculations already in v39; they do not rename or add manuscript results. Identifiers beginning `eq:` retain actual TeX labels.

### Arithmetic estimates and normalization

| Step and source | Content | Direct recorded inputs |
| --- | --- | --- |
| <a id="eq-point-fourier"></a>**Fourier transform of the modular inverse point set**<br>`eq:point-fourier`<br>Lines 370-374; equations (2.1) | The finite exponential sum over $\mathcal P_X$ equals $A_X(m,n)=\sum_{c\le X}S(m,n;c)$, with every point counted once and the modulus-one point represented by $S(m,n;1)=1$. | Direct in-text argument; see the source locator. |
| <a id="step-cardinality-comparison"></a>**Point-set cardinality and quadratic scale**<br>`step:cardinality-comparison`<br>Lines 155-159 | The point count is $N_X=\sum_{c\le X}\varphi(c)=(3/\pi^2)X^2+O(X\log X)$; in particular $N_X\asymp X^2$ for $X\ge2$. | [Summatory totient estimate](#external-HW-theorem-330) |
| <a id="step-normalized-coefficient-bound"></a>**Trivial bound for normalized point coefficients**<br>`step:normalized-coefficient-bound`<br>Lines 364-374 | The normalized coefficients satisfy $a_X(k)=N_X^{-1}\sum_{z\in\mathcal P_X}e(k\cdot z)$, $a_X(0)=1$ and $\vert a_X(k)\vert \le1$. | [Fourier transform of the modular inverse point set](#eq-point-fourier) |
| <a id="step-kloosterman-symmetries"></a>**Interchange and simultaneous sign reversal**<br>`step:kloosterman-symmetries`<br>Lines 374 | The elementary changes of variables give $S(m,n;c)=S(n,m;c)$ and $S(-m,-n;c)=S(m,n;c)$. | Direct in-text argument; see the source locator. |
| <a id="eq-selberg"></a>**Selberg's identity for Kloosterman sums**<br>`eq:selberg`<br>Lines 401-405; equations (2.4) | For integers $m,n$ and $c\ge1$, $S(m,n;c)=\sum_{d\mid\gcd(m,n,c)}d\,S(mn/d^2,1;c/d)$. | [Selberg identity for integer Kloosterman arguments](#external-Xi-selberg-identity) |
| <a id="eq-selberg-summed"></a>**Cumulative Selberg identity**<br>`eq:selberg-summed`<br>Lines 405-408; equations (2.5) | For $mn\ne0$, summing Selberg's identity over the modulus gives $A_X(m,n)=\sum_{d\mid\gcd(\vert m\vert ,\vert n\vert ),\,d\le X}d\,A_{X/d}(mn/d^2,1)$. | [Selberg's identity for Kloosterman sums](#eq-selberg) |
| <a id="step-divisor-small-power"></a>**Small-power divisor estimate**<br>`step:divisor-small-power`<br>Lines 417 | For every $\eta>0$ and integer $v\ge1$, $\tau(v)\ll_\eta v^\eta$. | [Divisor small-power bound](#external-IK-equation-1-81) |
| <a id="step-rectangular-divisor-reduction"></a>**Off-axis reduction of the rectangular second moment**<br>`step:rectangular-divisor-reduction`<br>Lines 419-435 | Cauchy–Schwarz over divisors and at most $2\tau(\vert r\vert )$ signed factorizations $uv=r$ reduce the off-axis second moment to $\sum_{d\le\min(M,N,X)}d^2\sum_{1\le\vert r\vert \le MN/d^2}\vert A_{X/d}(r,1)\vert ^2$. The cumulative input applies with $R=MN/d^2\ge1$, $Y=X/d\ge1$; the divisor sums have weights $d^{-2}$ and $d^{-1}$. | [Cumulative Selberg identity](#eq-selberg-summed); [Small-power divisor estimate](#step-divisor-small-power); [Corollary 2.2](#cor-brs-cumulative) |
| <a id="step-axis-ramanujan-bound"></a>**Axis contribution from Ramanujan sums**<br>`step:axis-ramanujan-bound`<br>Lines 437-447 | The Ramanujan formula $S(0,n;c)=\sum_{d\mid\gcd(c,n)}d\mu(c/d)$ gives $\vert A_X(0,n)\vert \le X\tau(\vert n\vert )$; symmetry gives the corresponding bound on the other axis. The divisor estimate then bounds both axes by $O_\eta(MNX^2(MN)^{2\eta})$. | [Ramanujan-sum identity](#external-IK-equation-3-2); [Interchange and simultaneous sign reversal](#step-kloosterman-symmetries); [Small-power divisor estimate](#step-divisor-small-power) |

### Fourier analysis and smooth brackets

| Step and source | Content | Direct recorded inputs |
| --- | --- | --- |
| <a id="step-fourier-translation-rule"></a>**Fourier coefficients of a translate**<br>`step:fourier-translation-rule`<br>Lines 360-364 | With $\widehat f(k)=\int_{\mathbb T^2}f(x)e(-k\cdot x)\,dx$, one has $\widehat{f(\cdot+h)}(k)=e(k\cdot h)\widehat f(k)$. | Direct in-text argument; see the source locator. |
| <a id="eq-mollifier-decay"></a>**Positive periodic mollifier and Fourier decay**<br>`eq:mollifier-decay`<br>Lines 511-524; equations (2.11) | For $0<\delta\le1/8$, the periodized mollifier $\rho_\delta$ is nonnegative, has integral one and support within distance $\delta$ of zero. Integration by parts proves $\vert \widehat{\rho_\delta}(k)\vert \ll_L(1+\delta\Vert k\Vert _\infty)^{-L}$ for every $L>0$. | Direct in-text argument; see the source locator. |

### Convex geometry and translation estimates

| Step and source | Content | Direct recorded inputs |
| --- | --- | --- |
| <a id="step-boundary-crossing"></a>**Boundary crossing along a short torus path**<br>`step:boundary-crossing`<br>Lines 555 | A shortest lifted segment joining a point of $E$ to a point of $E^c$ meets $\partial E$. Applied to the inner and outer sets used for smoothing, this places their indicator differences from $\mathbf1_E$ within the $3\delta$ boundary neighborhood. | Direct in-text argument; see the source locator. |
| <a id="eq-bracket-difference-norms"></a>**Boundary-neighborhood control of smoothing errors**<br>`eq:bracket-difference-norms`<br>Lines 555-559; equations (2.16) | For the inner and outer sets $E_\pm$, $\Vert \mathbf1_{E_\pm}-\mathbf1_E\Vert _1\le b_E(3\delta)$ and $\Vert \mathbf1_{E_\pm}-\mathbf1_E\Vert _2^2\le b_E(3\delta)$. | [Boundary crossing along a short torus path](#step-boundary-crossing) |
| <a id="step-convex-boundary-geometry"></a>**Elementary boundary geometry for a convex set**<br>`step:convex-boundary-geometry`<br>Lines 589-597 | For a convex body in a unit square, the boundary is a rectifiable Jordan curve of length $P\le4$. The arc covering argument shows that it has measure zero, while convexity gives $\operatorname{int}\overline\Omega\subset\Omega$. Thus $\mathbf1_\Omega=\mathbf1_{\overline\Omega}$ almost everywhere. Degenerate sets are handled separately. | Direct in-text argument; see the source locator. |
| <a id="eq-convex-tube"></a>**Boundary tube bound for a projected convex set**<br>`eq:convex-tube`<br>Lines 593-597; equations (2.17) | For $E=\pi\Omega$ with convex $\Omega\subset u+[0,1)^2$, $b_E(s)\le4\pi(Ps+s^2)$ for $0<s\le1$. A cover of the Euclidean boundary is projected to the torus, using $\partial E\subset\pi(\partial\overline\Omega)$ and that projection does not increase measure. | [Elementary boundary geometry for a convex set](#step-convex-boundary-geometry) |
| <a id="eq-convex-translation"></a>**Convex translation estimate with constant one**<br>`eq:convex-translation`<br>Lines 599-608; equations (2.18) | Parallel-line slicing gives $\vert (K+h)\triangle K\vert \le P\vert h\vert _2$, since the perpendicular width is at most $P/2$. Periodization then yields $\Vert \mathbf1_E(\cdot+h)-\mathbf1_E\Vert _2^2\le P\vert h\vert _2$ on the torus for every $h\in\mathbb R^2$. | [Elementary boundary geometry for a convex set](#step-convex-boundary-geometry); [Equality of translation norms for indicators](#step-indicator-translation-norms) |
| <a id="eq-convex-tail"></a>**Fourier-energy tail for a convex indicator**<br>`eq:convex-tail`<br>Lines 610; equations (2.19) | The translation estimate with $\Lambda=P$ and $\alpha=1$ in Lemma 2.5 yields $\sum_{\Vert k\Vert _\infty\ge T}\vert \widehat{\mathbf1_E}(k)\vert ^2\ll P/T$ for $T\ge1$, and hence the same bound on a dyadic shell. | [Convex translation estimate with constant one](#eq-convex-translation); [Lemma 2.5](#lem-translation) |
| <a id="eq-convex-pointwise"></a>**Pointwise Fourier decay for a convex indicator**<br>`eq:convex-pointwise`<br>Lines 612; equations (2.20) | For $k\ne0$, the special translation $h=k/(2\vert k\vert _2^2)$ has multiplier $-2$ and gives $\vert \widehat{\mathbf1_E}(k)\vert \le P/(4\vert k\vert _2)$. Combining this with the trivial area bound gives $\min\{A,P/(4\vert k\vert _2)\}$. | [Convex translation estimate with constant one](#eq-convex-translation); [Fourier coefficients of a translate](#step-fourier-translation-rule); [Equality of translation norms for indicators](#step-indicator-translation-norms) |
| <a id="step-indicator-translation-norms"></a>**Equality of translation norms for indicators**<br>`step:indicator-translation-norms`<br>Lines 509 | For an indicator, $\Vert \mathbf1_E(\cdot+h)-\mathbf1_E\Vert _2^2=\Vert \mathbf1_E(\cdot+h)-\mathbf1_E\Vert _1=\vert (E-h)\triangle E\vert $. | Direct in-text argument; see the source locator. |

### Counting, difference and variance identities

| Step and source | Content | Direct recorded inputs |
| --- | --- | --- |
| <a id="eq-identity-mu"></a>**Smooth Fourier identity for uniform counting**<br>`eq:identity-mu`<br>Lines 662-666; equations (3.1) | For smooth $f$, $\int f\,d\mu_X-\int f=\sum_{k\ne0}\widehat f(k)a_X(k)$, with absolute convergence. It follows by pointwise smooth Fourier inversion and a finite average over $\mathcal P_X$. | [Fourier inversion for smooth periodic functions](#external-Grafakos-sections-3-3-2-and-3-3-3); [Fourier transform of the modular inverse point set](#eq-point-fourier); [Trivial bound for normalized point coefficients](#step-normalized-coefficient-bound) |
| <a id="eq-identity-nu"></a>**Smooth Fourier identity for the difference measure**<br>`eq:identity-nu`<br>Lines 668-672; equations (3.2) | For smooth $f$, $\int f\,d\nu_X-\int f=\sum_{k\ne0}\widehat f(k)\vert a_X(k)\vert ^2$, with absolute convergence. The finite double exponential sum factors as $a_X(k)\overline{a_X(k)}$. | [Fourier inversion for smooth periodic functions](#external-Grafakos-sections-3-3-2-and-3-3-3); [Fourier transform of the modular inverse point set](#eq-point-fourier); [Trivial bound for normalized point coefficients](#step-normalized-coefficient-bound) |
| <a id="eq-identity-variance"></a>**Parseval identity for translation variance**<br>`eq:identity-variance`<br>Lines 674-683; equations (3.3) | For every measurable $E$, the finite reflected-translate sum $Z_E(u)=\mu_X(u+E)-\vert E\vert $ has nonzero Fourier coefficients $a_X(-k)\widehat{\mathbf1_E}(-k)$. Parseval gives $\mathcal V_X(E)=\sum_{k\ne0}\vert \widehat{\mathbf1_E}(k)\vert ^2\vert a_X(k)\vert ^2$. | [Parseval identity on the torus](#external-Grafakos-section-3-2-2); [Fourier transform of the modular inverse point set](#eq-point-fourier); [Trivial bound for normalized point coefficients](#step-normalized-coefficient-bound) |
| <a id="step-variance-null-set-invariance"></a>**Variance is unchanged by null-set changes**<br>`step:variance-null-set-invariance`<br>Lines 686 | The variance identity depends only on the $L^2$ class of $\mathbf1_E$, so changing $E$ on a null set leaves $\mathcal V_X(E)$ unchanged. In particular, boundary choices do not affect convex-set variance. | [Parseval identity for translation variance](#eq-identity-variance) |

### Discrepancy and boundary neighborhoods

| Step and source | Content | Direct recorded inputs |
| --- | --- | --- |
| <a id="step-pointwise-discrepancy-reduction"></a>**From pointwise brackets to a Fourier discrepancy bound**<br>`step:pointwise-discrepancy-reduction`<br>Lines 743-750; equations (4.2) | Pointwise upper and lower brackets reduce discrepancy to the larger smooth counting Fourier sum plus their integral error. The same reduction applies to general measurable sets. | [Lemma 2.6](#lem-brackets); [Proposition 3.1](#prop-identities) |
| <a id="step-coordinate-counting"></a>**Injective coordinate projections and counting in short intervals**<br>`step:coordinate-counting`<br>Lines 816-824 | Distinct points have distinct coordinates; their lifts have coordinate spacing at least $X^{-2}$. A width-$w_j$ interval therefore contains at most $1+w_jX^2$ lifted points. | Direct in-text argument; see the source locator. |
| <a id="eq-combined-small"></a>**Combining geometric and Fourier discrepancy estimates**<br>`eq:combined-small`<br>Lines 827-830; equations (4.4) | Takes the smaller of the coordinate-width bound and the perimeter-sensitive Fourier bound. | [Proposition 4.3](#prop-coordinate-separation); [Theorem 1.1](#thm-perimeter) |
| <a id="step-cardinality-upper"></a>**Elementary upper bound for the point count**<br>`step:cardinality-upper`<br>Lines 853-857; 1189-1192 | The identity $N_X=\sum_{c\le X}\varphi(c)$ and $\varphi(c)\le c$ give $N_X\le X^2$ for $X\ge1$. This elementary upper bound is used in the small-perimeter examples and repeated in the lower distance estimate. | Direct in-text argument; see the source locator. |
| <a id="step-short-perimeter-diagonal-lower"></a>**Diagonal segments realizing the short-perimeter lower order**<br>`step:short-perimeter-diagonal-lower`<br>Lines 845-857 | A segment starting at $(1/X,1/X)$ captures both one point and a number proportional to $pX^2$; division by $N_X$ gives the two terms in the lower bound. Integer parts handle real heights. | [Elementary upper bound for the point count](#step-cardinality-upper) |
| <a id="step-boundary-fourier-control"></a>**From boundary tubes to Fourier and bracket norms**<br>`step:boundary-fourier-control`<br>Lines 873-881 | A path crossing the topological boundary bounds the symmetric difference by $B\vert h\vert _2^{\alpha}$; the translation lemma and smooth brackets then give shell norms uniformly in alpha. | [Remark 2.9](#rem-tube-to-translation) (proof method); [Lemma 2.5](#lem-translation); [Lemma 2.6](#lem-brackets) |
| <a id="step-boundary-uniform-dyadic"></a>**Dyadic summation uniform in the boundary exponent**<br>`step:boundary-uniform-dyadic`<br>Lines 888-892 | Uses the explicit geometric-series constants for exponents in compact positive ranges, and treats $\beta=1/3-\alpha/2$ directly through zero with a logarithmic cutoff factor. | [Lemma 4.1](#lem-dyadic) |
| <a id="eq-general-smoothing"></a>**Smoothing estimate for a general boundary tube bound**<br>`eq:general-smoothing`<br>Lines 883-896; equations (4.6) | Combines the pointwise discrepancy reduction, boundary-based bracket norms, arithmetic shell estimate and uniform dyadic sums before optimizing delta. | [From pointwise brackets to a Fourier discrepancy bound](#step-pointwise-discrepancy-reduction); [From boundary tubes to Fourier and bracket norms](#step-boundary-fourier-control); [Corollary 2.4](#cor-shell); [Dyadic summation uniform in the boundary exponent](#step-boundary-uniform-dyadic) |
| <a id="step-well-shaped-torus-tube"></a>**From Euclidean well-shapedness to torus boundary control**<br>`step:well-shaped-torus-tube`<br>Lines 927 | Separates a strip near the unit-square boundary from interior discs to obtain $b_{\pi\Omega}(s)\le(8+4\gamma)s$ at small s, and an admissible global constant $B=8(1+\gamma)$ for alpha one. | [Definition of well-shaped sets](#external-BRS-section-3-1) |
| <a id="step-koch-tube"></a>**Tube control for a Koch boundary**<br>`step:koch-tube`<br>Lines 931-941 | The construction arcs give a covering by $O((\ell/s)^d)$ discs of radius $O(s)$, yielding boundary-tube order at most $s^{2-d}$; the source's dimension d also obstructs a linear tube bound. | [Koch construction and Minkowski dimension](#external-LP-section-1) |

### Differences and local variance

| Step and source | Content | Direct recorded inputs |
| --- | --- | --- |
| <a id="step-difference-convex-proof"></a>**Convex difference estimate from pointwise brackets and squared shells**<br>`step:difference-convex-proof`<br>Lines 956-979; equations (5.1), (1.9) | Bracket the convex indicator pointwise, use the nonnegative coefficients $\vert a_X(k)\vert ^2$ in the difference identity, sum the squared shell estimates, and take $\delta=(8X)^{-1}$ to obtain the convex clause of Theorem 1.5. | [Lemma 2.6](#lem-brackets); [Corollary 2.8](#cor-convex-brackets); [Proposition 3.1](#prop-identities); [Corollary 2.4](#cor-shell); [Lemma 4.1](#lem-dyadic) |
| <a id="step-arc-indicator-coefficients"></a>**Fourier coefficients of an arc indicator**<br>`step:arc-indicator-coefficients`<br>Lines 990-994 | Direct integration gives the nonzero coefficient of an arc indicator as an endpoint exponential difference divided by $2\pi i m$. Its modulus is bounded by the smaller of the arc length and $(\pi\vert m\vert )^{-1}$; the zero coefficient is the length. | Direct in-text argument; see the source locator. |
| <a id="step-difference-box-proof"></a>**Product brackets and separate frequency summation for differences**<br>`step:difference-box-proof`<br>Lines 997-1031; equations (5.3), (1.10) | Use products of arc brackets and dyadic blocks in each frequency separately. Proposition 2.3 and the resulting one-variable sums, with $\delta=(16X^2)^{-1}$, give the area-dependent rectangle clause of Theorem 1.5. | [Lemma 5.1](#lem-arc-brackets); [Proposition 3.1](#prop-identities); [Proposition 2.3](#prop-rectangular); [Point-set cardinality and quadratic scale](#step-cardinality-comparison); [Lemma 4.1](#lem-dyadic) |
| <a id="eq-diagonal-removal"></a>**Removing equal-point pairs**<br>`eq:diagonal-removal`<br>Lines 1033-1040; equations (5.4) | The exact relation $\nu_X=(1-N_X^{-1})\nu_X^*+N_X^{-1}\delta_0$ implies that the two probability measures differ on any measurable set by at most $N_X^{-1}\ll X^{-2}$. | [Point-set cardinality and quadratic scale](#step-cardinality-comparison) |
| <a id="step-variance-convex-proof"></a>**Convex variance from Fourier tails and squared shells**<br>`step:variance-convex-proof`<br>Lines 1088-1104; equations (1.12) | Handle sets below the one-point threshold by the exact identity. Otherwise split at frequency $T=X^2/P$, use the convex Fourier tail above $T$, and pair the pointwise coefficient bound with the squared shell estimate below $T$. | [Lemma 5.3](#lem-one-point); [Point-set cardinality and quadratic scale](#step-cardinality-comparison); [Proposition 3.1](#prop-identities); [Lemma 2.7](#lem-convex-geometry); [Trivial bound for normalized point coefficients](#step-normalized-coefficient-bound); [Corollary 2.4](#cor-shell) |
| <a id="step-variance-disc-proof"></a>**Disc variance as a convex-set specialization**<br>`step:variance-disc-proof`<br>Lines 1106; equations (1.14) | Apply the established convex variance estimate with area $\pi r^2$ and perimeter $2\pi r$; discs of radius at most $1/4$ fit in a translated unit square. | [Convex variance from Fourier tails and squared shells](#step-variance-convex-proof) |
| <a id="step-variance-box-proof"></a>**Rectangle variance from squared arc coefficients**<br>`step:variance-box-proof`<br>Lines 1108-1114; equations (1.13) | Use the one-point identity for a side below $X^{-2}$. Otherwise factor the squared indicator coefficients, sum separate frequency blocks against Proposition 2.3, and split the one-variable sums at the reciprocal side lengths. | [Lemma 5.3](#lem-one-point); [Point-set cardinality and quadratic scale](#step-cardinality-comparison); [Fourier coefficients of an arc indicator](#step-arc-indicator-coefficients); [Proposition 3.1](#prop-identities); [Proposition 2.3](#prop-rectangular); [Product brackets and separate frequency summation for differences](#step-difference-box-proof) (proof method) |

### Distance moments

| Step and source | Content | Direct recorded inputs |
| --- | --- | --- |
| <a id="eq-FX"></a>**An explicit empty rectangle at scale X to the minus one half**<br>`eq:FX`<br>Lines 225-229; equations (1.6) | For $X>9$, the rectangle $[2X^{-1/2},3X^{-1/2}]\times[\tfrac15X^{-1/2},\tfrac14X^{-1/2}]$ has area $1/(20X)$ and contains no modular-inverse point. The proof separates points with $ab=1$ from those with $ab=1+jc$, $j\ge1$. | [Empty boxes and cutoff effects in BRS](#external-BRS-section-1-2) (proof method) |
| <a id="eq-distance-tail"></a>**Distance tail from the disc variance**<br>`eq:distance-tail`<br>Lines 1170-1173; equations (5.7) | An empty disc forces normalized-count deviation $\pi r^2$. Chebyshev's inequality and the disc variance therefore bound the measure of $\{d_X>r\}$ by $\ll_\varepsilon X^\varepsilon(X^{-2}r^{-2}+X^{-5/3}r^{-2/3})$ for $0<r\le1/4$. | [Theorem 1.6](#thm-variance) |
| <a id="eq-distance-max"></a>**Uniform distance cutoff from shrinking-set equidistribution**<br>`eq:distance-max`<br>Lines 1174-1177; equations (5.8) | For any fixed $0<\kappa\le1/4$ and sufficiently large $X$, Corollary 1.3 ensures that every disc of radius $X^{-1/2+\kappa}$ contains a point. Hence $d_X(u)<X^{-1/2+\kappa}$ for every center. | [Corollary 1.3](#cor-shrinking) |
| <a id="step-distance-upper"></a>**Integrating the distance tail up to its uniform cutoff**<br>`step:distance-upper`<br>Lines 1179-1187 | Use the layer-cake formula, the trivial tail bound below $X^{-1}$, the variance tail up to $X^{-1/2+\kappa}$, and the vanishing tail beyond it. The integral of $r^{s-3}$ produces the three cases $s<2$, $s=2$, and $s>2$. | [Distance tail from the disc variance](#eq-distance-tail); [Uniform distance cutoff from shrinking-set equidistribution](#eq-distance-max) |
| <a id="step-distance-lower"></a>**Packing and the empty rectangle give the two distance lower bounds**<br>`step:distance-lower`<br>Lines 1189-1197 | A union of $N_X$ discs covering at most half the torus gives a lower bound $\gg_sX^{-s}$. The middle quarter of the explicit empty rectangle has measure $\asymp X^{-1}$ and distance $\gg X^{-1/2}$ from the point set, giving $\gg_sX^{-1-s/2}$. | [An explicit empty rectangle at scale X to the minus one half](#eq-FX); [Elementary upper bound for the point count](#step-cardinality-upper) |

## Literature inputs

Cited literature results are treated as trusted inputs and are not reproved here. Their statements, hypotheses, parameter ranges, and normalizations must match each application. Explicit method credit is distinguished from an assumed external conclusion.

The entries below record inputs to the written proofs and explicit method credit. Locators follow the citations in v39. Different uses of the same work remain separate nodes so the graph identifies the particular result, definition, or method being used.

| Input | Reference and locator | Used in |
| --- | --- | --- |
| <a id="external-BRS-theorem-1-3"></a>**BRS second moment with one frequency fixed**<br>`external:BRS-theorem-1-3` | [BRS](#ref-brs), Theorem 1.3; Section 2.1 for the small-power convention | [Theorem 2.1](#thm-brs-input) |
| <a id="external-Xi-selberg-identity"></a>**Selberg identity for integer Kloosterman arguments**<br>`external:Xi-selberg-identity` | [Xi](#ref-xi), Paper cited without a numbered locator | [Selberg's identity for Kloosterman sums](#eq-selberg) |
| <a id="external-IK-equation-1-81"></a>**Divisor small-power bound**<br>`external:IK-equation-1-81` | [IK](#ref-ik), Equation (1.81) | [Small-power divisor estimate](#step-divisor-small-power) |
| <a id="external-IK-equation-3-2"></a>**Ramanujan-sum identity**<br>`external:IK-equation-3-2` | [IK](#ref-ik), Equation (3.2) | [Axis contribution from Ramanujan sums](#step-axis-ramanujan-bound) |
| <a id="external-HW-theorem-330"></a>**Summatory totient estimate**<br>`external:HW-theorem-330` | [HW](#ref-hw), Theorem 330 | [Point-set cardinality and quadratic scale](#step-cardinality-comparison) |
| <a id="external-Grafakos-section-3-2-2"></a>**Parseval identity on the torus**<br>`external:Grafakos-section-3-2-2` | [Grafakos](#ref-grafakos), Section 3.2.2 | [Lemma 2.5](#lem-translation); [Lemma 2.6](#lem-brackets); [Parseval identity for translation variance](#eq-identity-variance) |
| <a id="external-Grafakos-sections-3-3-2-and-3-3-3"></a>**Fourier inversion for smooth periodic functions**<br>`external:Grafakos-sections-3-3-2-and-3-3-3` | [Grafakos](#ref-grafakos), Sections 3.3.2 and 3.3.3 | [Smooth Fourier identity for uniform counting](#eq-identity-mu); [Smooth Fourier identity for the difference measure](#eq-identity-nu) |
| <a id="external-Grafakos-section-3-1-2"></a>**Fourier coefficients of a convolution**<br>`external:Grafakos-section-3-1-2` | [Grafakos](#ref-grafakos), Section 3.1.2 | [Lemma 2.6](#lem-brackets) |
| <a id="external-BRS-section-3-1"></a>**Definition of well-shaped sets**<br>`external:BRS-section-3-1` | [BRS](#ref-brs), Section 3.1 | [From Euclidean well-shapedness to torus boundary control](#step-well-shaped-torus-tube) |
| <a id="external-LP-section-1"></a>**Koch construction and Minkowski dimension**<br>`external:LP-section-1` | [LP](#ref-lp), Section 1 | [Tube control for a Koch boundary](#step-koch-tube) |
| <a id="external-BRS-section-1-2"></a>**Empty boxes and cutoff effects in BRS**<br>`external:BRS-section-1-2` | [BRS](#ref-brs), Section 1.2 | [An explicit empty rectangle at scale X to the minus one half](#eq-FX) (method credit) |

### Bibliographic key

<a id="ref-bmv"></a>**BMV.** J. T. Barton, H. L. Montgomery and J. D. Vaaler. *Note on a Diophantine inequality in several variables*. Proc. Amer. Math. Soc. 129 (2001), 337-345.

<a id="ref-blomer"></a>**Blomer.** V. Blomer. *Pair correlation for modular inverses*. preprint, 20 pp.

<a id="ref-bc"></a>**BC.** J. Beck and W. W. L. Chen. *Irregularities of distribution*. Cambridge Tracts in Math. 89, Cambridge Univ. Press, Cambridge, 1987.

<a id="ref-brs"></a>**BRS.** V. Blomer, M. S. Risager and I. E. Shparlinski. *Triple sums of Kloosterman sums and the discrepancy of modular inverses*. J. Lond. Math. Soc. (2) 112 (2025), no. 3, e70291, 30 pp.

<a id="ref-bct"></a>**BCT.** L. Brandolini, L. Colzani and G. Travaglini. *Average decay of Fourier transforms and integer points in polyhedra*. Ark. Mat. 35 (1997), no. 2, 253-275.

<a id="ref-cgt"></a>**CGT.** L. Colzani, G. Gigante and G. Travaglini. *Trigonometric approximation and a general form of the Erdős-Turán inequality*. Trans. Amer. Math. Soc. 363 (2011), no. 2, 1101-1123.

<a id="ref-di"></a>**DI.** J.-M. Deshouillers and H. Iwaniec. *Kloosterman sums and Fourier coefficients of cusp forms*. Invent. Math. 70 (1982/83), 219-288.

<a id="ref-dress"></a>**Dress.** F. Dress. *Discrépance des suites de Farey*. J. Théor. Nombres Bordeaux 11 (1999), no. 2, 345-367.

<a id="ref-good"></a>**Good.** A. Good. *Local analysis of Selberg's trace formula*. Lecture Notes in Math. 1040, Springer-Verlag, Berlin, 1983.

<a id="ref-grafakos"></a>**Grafakos.** L. Grafakos. *Classical Fourier analysis*. 3rd ed., Grad. Texts in Math. 249, Springer, New York, 2014.

<a id="ref-harman"></a>**Harman.** G. Harman. *On the Erdős-Turán inequality for balls*. Acta Arith. 85 (1998), 389-396.

<a id="ref-hw"></a>**HW.** G. H. Hardy and E. M. Wright. *An introduction to the theory of numbers*. 6th ed., Oxford Univ. Press, Oxford, 2008.

<a id="ref-humphries"></a>**Humphries.** P. Humphries. *Distributing points on the torus via modular inverses*. Q. J. Math. 73 (2022), no. 1, 1-16.

<a id="ref-ik"></a>**IK.** H. Iwaniec and E. Kowalski. *Analytic number theory*. Amer. Math. Soc. Colloq. Publ. 53, Amer. Math. Soc., Providence, RI, 2004.

<a id="ref-ks"></a>**KS.** B. Kerr and I. E. Shparlinski. *On the distribution of values and zeros of polynomial systems over arbitrary sets*. J. Number Theory 133 (2013), 2863-2873.

<a id="ref-kiral"></a>**Kiral.** E. M. Kıral. *Opposite-sign Kloosterman sum zeta function*. Mathematika 62 (2016), 406-429.

<a id="ref-kn"></a>**KN.** L. Kuipers and H. Niederreiter. *Uniform distribution of sequences*. Wiley-Interscience, New York-London-Sydney, 1974.

<a id="ref-kuznetsov"></a>**Kuznetsov.** N. V. Kuznetsov. *The Petersson conjecture for cusp forms of weight zero and the Linnik conjecture. Sums of Kloosterman sums*. Math. USSR-Sb. 39 (1981), 299-342.

<a id="ref-lp"></a>**LP.** M. L. Lapidus and E. P. J. Pearse. *A tube formula for the Koch snowflake curve, with applications to complex dimensions*. J. London Math. Soc. (2) 74 (2006), no. 2, 397-414.

<a id="ref-niederreiter"></a>**Niederreiter.** H. Niederreiter. *The distribution of Farey points*. Math. Ann. 201 (1973), 341-345.

<a id="ref-philipp"></a>**Philipp.** W. Philipp. *Empirical distribution functions and uniform distribution mod 1*. in: Diophantine Approximation and its Applications (Washington, D.C., 1972), Academic Press, New York, 1973, 211-234.

<a id="ref-podkorytov"></a>**Podkorytov.** A. N. Podkorytov. *The asymptotics of the Fourier transform of a convex curve*. Vestnik Leningrad Univ. Math. 24 (1991), 57-65.

<a id="ref-st"></a>**ST.** P. Sarnak and J. Tsimerman. *On Linnik and Selberg's conjecture about sums of Kloosterman sums*. in: Algebra, Arithmetic, and Geometry: in Honor of Yu. I. Manin, Vol. II, Progr. Math. 270, Birkhäuser, Boston, 2009, 619-635.

<a id="ref-schmidt"></a>**Schmidt.** W. M. Schmidt. *Irregularities of distribution. IX*. Acta Arith. 27 (1975), 385-396.

<a id="ref-selberg38"></a>**Selberg38.** A. Selberg. *Über die Fourierkoeffizienten elliptischer Modulformen negativer Dimension*. C. R. Neuvième Congrès Math. Scandinaves, Helsingfors, 1938, 320-322.

<a id="ref-selberg77"></a>**Selberg77.** A. Selberg. *Equidistribution in discrete groups and the spectral theory of automorphic forms*. unpublished lecture notes, Institute for Advanced Study, Princeton; available at https://publications.ias.edu/selberg/section/2491.

<a id="ref-shparlinski"></a>**Shparlinski.** I. E. Shparlinski. *Modular hyperbolas*. Jpn. J. Math. 7 (2012), 235-294.

<a id="ref-travaglini"></a>**Travaglini.** G. Travaglini. *Number theory, Fourier analysis and geometric discrepancy*. London Math. Soc. Stud. Texts 81, Cambridge Univ. Press, Cambridge, 2014.

<a id="ref-xi"></a>**Xi.** P. Xi. *An elementary proof of the Selberg identity for Kloosterman sums*. preprint (2023), arXiv:2306.16929.

### Attribution and comparison references

The proof graph starts from the frequency moment as packaged in BRS Theorem 1.3. The spectral ancestry of that result, including Kuznetsov and the Deshouillers–Iwaniec large sieve, is not expanded into additional premises for this paper.

Selberg38 gives the historical attribution for Selberg's identity; Kuznetsov and Xi are the proof references cited in v39. The graph uses Xi as the explicit literature input and keeps the other references on the identity record. BRS Section 4.1 is credited for the general-frequency reduction. The empty-box construction is credited to BRS Section 1.2, while the particular rectangle used in the distance proof is verified directly in v39.

BRS's earlier discrepancy bounds, first moments, dyadic packing method and general lower bounds are used for comparisons. The BRS Section 3.1 definition of well-shapedness is an input, but the nearby earlier well-shaped discrepancy estimate is not. Humphries's fixed-modulus variance enters a comparison calculation in Section 3.3, not the proof of Theorem 1.6.

The angular Fourier-decay results of Podkorytov and Brandolini–Colzani–Travaglini, the geometric-discrepancy literature including Colzani–Gigante–Travaglini, and the earlier Farey, discrepancy and Kloosterman results provide context. The manuscript proves its own translation, tube and bracket estimates. The announced Blomer pair-correlation preprint is contextual and is described here only as v39 describes it; it is not a proof input.

## Comparisons in Section 3

These calculations compare approaches and are recorded separately from the proof graph. They are not prerequisites of the new main theorems. In particular, the cited and locally derived versions of the first-moment estimate are alternative justifications.

| Calculation | Source lines | Content |
| --- | --- | --- |
| First moment on a frequency shell | 694-698 | The shell first moment satisfies $\sum_{k\in\mathscr H(H)}\vert a_X(k)\vert \ll_\eta(HX)^\eta(X^{-1}H^2+X^{-5/6}H^{4/3})$. The text cites BRS and also gives the alternative derivation by Cauchy–Schwarz from Corollary 2.4. |
| Discrepancy obtained from the shell first moment | 700-704 | Pairing the maximal bracket coefficient with the shell first moment yields $D_X(E)\ll_\eta b+(X/\delta)^\eta(PX^{-1}\delta^{-1}+PX^{-5/6}\delta^{-1/3}+bX^{-1}\delta^{-2}+bX^{-5/6}\delta^{-4/3})$, where $b=P\delta+\delta^2$. At $\delta=X^{-1/2}$, $X\ge64$, this is $\ll_\varepsilon X^\varepsilon(PX^{-1/2}+X^{-1})$. |
| Height variance obtained by averaging fixed-modulus standard deviations | 712-716 | Writing $\mu_X=N_X^{-1}\sum_{c\le X}\varphi(c)\mu_c$, the triangle inequality and Humphries's disc variance bound give $\mathcal V_X(B_r)^{1/2}\ll_\varepsilon rN_X^{-1}\sum_{c\le X}\varphi(c)^{1/2}c^\varepsilon\ll_\varepsilon rX^{-1/2+\varepsilon}$. Thus $\mathcal V_X(B_r)\ll_\varepsilon r^2X^{-1+2\varepsilon}$. |

## Section 6: unnumbered discussion

Section 6 has no numbered theorem, lemma, proposition, corollary, or remark. Its conclusions and open directions are recorded separately below.

| Subsection | Source lines | Content |
| --- | --- | --- |
| 6.1: The exponent 2/3 | 1204-1206 | The two leading terms in the existing smoothing argument balance at exponent 2/3. Removing the sharp-cutoff term alone would not improve that balance. The text suggests additional geometric or arithmetic input and leaves the gap between the known convex-discrepancy lower and upper bounds unresolved. |
| 6.2: The mean-spacing scale | 1208-1210 | The proved difference and variance bounds reach relative asymptotics above X inverse by a fixed power. At mean spacing they provide upper bounds but no limiting law. The text identifies pair correlation at mean spacing as a further question and cites the announced Blomer preprint as context. |
| 6.3: Other test sets | 1212-1214 | The aspect-ratio-independent area bounds are established for products of coordinate arcs; their validity for arbitrary rotated rectangles is left open. The text also sketches a controlled-boundary extension of the difference method with error B X to the minus alpha plus epsilon and explicitly leaves its details and fractal-boundary local statistics to future work. |
| 6.4: The second moment of the distance | 1216-1218 | For s=2, Theorem 1.7 gives lower order X to the minus two and upper order X to the minus two plus epsilon. The source leaves the remaining factor and constant undetermined and relates the issue to empty discs across the range from mean spacing to the empty-rectangle scale. |

## Maintenance

This file is generated from `docs/dependency_inventory.json` by `python3 scripts/build_dependency_graph.py`. Update the record and source fingerprint when changing the manuscript baseline, then regenerate the inventory and graphs together.
