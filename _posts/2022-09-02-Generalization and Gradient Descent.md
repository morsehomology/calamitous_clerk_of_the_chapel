---
layout: post
title: "Generalization and Gradient Descent"
categories: journal
tags: [documentation, sample]
image: mountains.jpg
---

# "Bias Variance" exposition

Daniela Witten says the tradeoff is related to the equation

$$\text{Exp. Pred. Error }=\text{ Irreducible Error + Bias}^2+ \text{Var}$$

There will be different frameworks for this, we're going to try to start with as little structure as possible if we can.

## Version/Attempt 1

(I have reasons to think this version can't be correct, doesn't have some features of the problem which seemed essential. We want to see that though).

Have a space $X$ and the data is determined by a distribution $\rho$ on $X$. A model (fit) is another distribution $\rho'$ on $X$. For now we meed to assume that $X$ has a fixed metric $d$ and furthermore that means/centers of mass are defined for $\rho$ and $\rho'$, call these $x_{\rho}$ and $x_{\rho'}$ in $X$.

(They should be defined by minimizing $E_{\rho}[d(x_{\rho}, x)]$ over all of $X$, and likewise for $\rho'$).

The variance of

# From Ben Recht slides

**Given**: i.i.d. sample $$S=\left\{z_1, \ldots, z_n\right\}$$ from distribution $D$\
**Goal**: Find a good predictor function $f$\
Population risk (test error): $$R[f]=\mathbb{E}_z \operatorname{loss}(f ; z)$$ Unknown!\
Empirical risk (training error): $$R_s[f]=\frac{1}{n} \sum_{i=1}^n \operatorname{loss}\left(f ; z_i\right)$$ Minimize using SGD!\
Generalization error: $R[f]-R_s[f]$

How much empirical risk underestimates population risk

We can compute $R_s \ldots$:

"Fundamental theorem of ML:"

$$R[f]=\left(R[f]-R_S[f]\right)+R_S[f]$$

population generalization training - small training error implies risk ± generalization error - zero training error does not imply overfitting $$\begin{aligned}
R[f] &=\left(R[f]-R\left[f_{\mathcal{H}}\right]\right) \\
&+\left(R\left[f_{\mathcal{H}}\right]-R\left[f_{\star}\right]\right) \\
&+R\left[f_{\star}\right]
\end{aligned}$$
