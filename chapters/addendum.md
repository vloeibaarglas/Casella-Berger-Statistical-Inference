---
layout: default
title: "Errata Addendum"
permalink: /addendum/
---

# Addendum: Errata in the Textbook

*Companion to "Casella & Berger, Statistical Inference (2nd edition) — Exercises with Solutions, All Chapters."*

Errors in the printed text of Casella & Berger, *Statistical Inference*, 2nd edition, 2024 CRC Press / Chapman & Hall reprint (hardback ISBN 978-1-032-59303-6; paperback ISBN 978-1-032-59794-2), found while working the exercises: false statements, wrong formulas, wrong numerical values, and missing hypotheses. Each entry names the defect and gives the correction; the full counterexample or proof is in the solution to that exercise. 38 entries across 11 of the 12 chapters.

## Chapter 1 — Probability Theory

**1.29(d) — false identity.** The weighted sum equals $m^k$ by the multinomial theorem, not $\binom{k+m-1}{k}$ (e.g. $m=k=2$ gives $1+2+1=4 \ne 3$). Stars and bars counts the *summands*; the authors' errata change the exercise to ask for that count.

**1.31 — wrong value.** The average of $\{2,4,9,12\}$ is $27/4$, not $29/4$ as printed.

**1.42(e) — wrong cross-reference (minor).** The proof needs the alternating-binomial identity from part (d), not (a)–(c).

**1.43(b) — false in both directions.** Neither the printed inequality nor its reverse holds in general for the unnormalized bounds. What is true: the normalized averages $P_k/\binom{n}{k}$ decrease in $k$.

## Chapter 2 — Transformations and Expectations

**2.29(c) — wrong factor.** The printed $a(y+a)$ cannot be a pmf; the beta-binomial pmf needs the factor $\frac{a}{y+a}$ (confirmed by the authors' errata).

**2.40 — missing hypothesis.** The identity requires integer $0 \le x < n$; at $x = n$ the right side is the indeterminate form $0\cdot\infty$ (the $(n-x)$ factor vanishes but $\int_0^{1-p}t^{-1}(1-t)^n\,dt$ diverges for $p<1$), not 0.

## Chapter 3 — Common Families of Distributions

No errata found.

## Chapter 4 — Multiple Random Variables

**4.8 — missing Jacobian.** With a continuous prior density, the two envelope contributions at observed $x$ are $\pi(x)/2$ and $\pi(x/2)/4$: the doubled-envelope term needs the scale change of variables. Switching is favorable iff $\pi(x/2) < 4\pi(x)$. The text's factor-2 rule holds only for a discrete prior mass function.

**4.37(a) — false as stated.** The uniform-mixing moment argument does not prove the claim for fixed finite $n$; an explicit mixture of shifted beta-binomial laws is a counterexample.

## Chapter 5 — Properties of a Random Sample

**5.38(b) — missing restriction.** "$P(S_n>a)\le c^n$ for all $n$" is false for $a<0$ (e.g. $X\equiv-1$, $a=-2$ gives $P(S_n>-2)=1$); it holds for $a\ge0$, or only eventually for $a<0$. Parts (c)–(d) use $a=0$ and are unaffected.

**5.56 — wrong density and cdf.** $1/(1+y^2)$ is not a pdf ($\int = \pi$). The Cauchy density is $\frac{1}{\pi(1+y^2)}$ with cdf $\frac12 + \frac1\pi\tan^{-1}(y)$.

**5.61(b) — false as stated.** An equal-scale integer-shape gamma proposal cannot dominate the target; a finite rejection envelope needs a larger proposal scale (the authors' errata specify $b+1$).

## Chapter 6 — Principles of Data Reduction

**6.27(b) — misprinted statistic.** The chi-square pivot needs $n/\bar X$, not $1/\bar X$, in the denominator.

## Chapter 7 — Point Estimation

**7.45(d) — wrong formula.** The minimizing factor uses $K - 3$ where $K = E(X-\mu)^4/\sigma^4$ is the standardized kurtosis, not the raw fourth moment minus 1.

**7.51 — wrong cross-reference.** "As in Exercise 7.46" should be "as in Exercise 7.50": 7.46 treats the uniform$(\theta,2\theta)$ family and defines no $cS$; the $n(\theta,a\theta^2)$ notation with $cS$ is from 7.50 (which part (b) already cites as 7.50b).

## Chapter 8 — Hypothesis Testing

**8.43 — wrong pivots and optimizer.** As printed, the $t$ statistic is not Student $t$; the $F$ claim is wrong in both degrees-of-freedom order and scaling; the $\rho^2$ optimizer uses variances where standard deviations belong.

## Chapter 9 — Interval Estimation

**9.20(b) — reversed inequalities.** Both inequalities must be reversed; coverage is at least $1-\alpha$, with equality not guaranteed for discrete laws.

**9.49(b) — false "more powerful" claim.** The power comparison is invalid as a uniform claim: because $(\alpha-p)/(1-p)<\alpha$, the cutoff $z_{(\alpha-p)/(1-p)}$ exceeds $z_\alpha$, and the powers cross — test (a) wins for small shifts, test (b) only for large ones (e.g. $\alpha=.1$, $p=.05$: at $\delta=1$, $.376$ vs $.304$; at $\delta=5$, $.961$ vs $1.000$).

**9.45(b) — wrong cutoff.** The UMA interval needs the lower-$\alpha$ (upper-$(1-\alpha)$) chi-square cutoff. In (d), the minimum-based interval has coverage $0.2993803913$, not exactly $0.3$.

**9.30 — misleading aside (minor).** The decay argument holds for every finite $b > 0$, including $b = 1/n$; it fixes $n$, $a$, $b$ while the observed sum grows.

## Chapter 10 — Asymptotic Evaluations

**10.11(b) — false claim.** With both gamma parameters unknown, $\hat\mu_{\mathrm{MLE}} = \bar X$ exactly, so the ARE comparison is 1, not $\alpha\psi'(\alpha)$.

**10.11(c) — false.** The known-mean method-of-moments and maximum-likelihood scale estimators are different statistics (e.g. $0.156$ versus $1.867$ on the book's data).

**10.16(a) — wrong value.** The second-order term is $0.0002140103$, not $0.00007$.

**10.16(b) — wrong value.** The exact binomial variance is $0.0002710672072$, not $0.00529$.

**10.19(b) — sign error.** The term before $\frac{1-\rho^n}{1-\rho}$ should be $-$, not $+$.

**10.29(b)(ii) — wrong function.** For the stated logistic density the efficient score is $\tanh(x/2)$, not $\tanh(x)$.

**(10.3.8) — wrong denominator.** It must estimate the square of the *central* probability, not the outside probability.

**(10.2.4) — sign slip.** The Taylor ratio in the displayed expansion has a sign error (harmless for the subsequent asymptotics).

**10.33 — inverted statistic.** The pivot must multiply by observed information, $\sqrt{J_n(\hat\theta)}(\hat\theta - \theta_0)$; the printed division is $O_p(n^{-1})$ and converges to zero. (The same inversion appears in the proof of Theorem 10.3.1.)

**10.17 — data typo.** The third pair prints as $(5.58,2.81)$; the canonical Efron (1982) law-school dataset has $(558,2.81)$. With the printed value the correlation drops to $r=0.493$ (vs $0.776$ with the intended value).

**10.45 — false coverage claim.** The parenthetical asserts the continuity-corrected interval maintains coverage above $1-\alpha$ for all $p$, but at $n=20$ it dips to $.9490<.95$.

## Chapter 11 — Analysis of Variance and Regression

**11.29(c) — sign error.** $\mathrm{Cov}(Y_i,\hat\alpha)$ needs a minus sign before $\frac{(x_i-\bar x)\bar x}{S_{xx}}$ (the following exercise prints it correctly).

**11.40(a) — "max" should be "sup".** The supremum is not attained, so "maximum" is incorrect.

## Chapter 12 — Regression Models

**12.3(b) — false.** Squared distance violates the triangle inequality; $\sqrt{D_\lambda}$ is the metric.

**12.27(a) — false as stated.** The CLT needs the true parameter and the weighted sign score; the plug-in version fails (median counterexample).

**12.27(b) — invalid proof step.** The empirical LAD score is piecewise constant and cannot be differentiated termwise; the expected-score derivative is $-2f(0)q_n$.

**12.26(a)(ii) — non sequitur.** Bounded $x_i$ does not imply convergence of the stated sequence; a further argument is needed.

**12.31(c) — self-reference.** Prints "Do (c) B times"; should be "Do (b) B times" (repeat the resampling step — (c) cannot refer to itself).

**12.30(e) — naming.** "Laplace" and "double exponential" are the same law, not two error distributions to compare.
