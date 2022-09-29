---
title: "The law of a random variable"
date: "2012-03-27"
draft: false
tags:
- mathematics
- probability
---

Let $(\Omega, \mathcal{F}, \mathbb{P})$ be a probability space and $X$ be a random variable on $\Omega$. The law (or distribution) of $X$ is the (Borel) probability measure on the real line defined by
$$ \mathbb{P}_X(A) = \mathbb{P}(X \in A) $$
for every Borel $A \subseteq \mathbb{R}$.

Conversely, suppose we are given a probability measure $\mu$ on $\mathbb{R}$. We can build a random variable so that its law is precisely $\mu$. Take $\Omega = [0, 1]$, $\mathcal{F}$ be the Borel $\sigma$-algebra and $\mathbb{P}$ be the Lebesgue measure. For each $\omega \in \Omega$, let
$$ X(\omega) = \inf \{t \in \mathbb{R}: \mu((-\infty, t]) \geq \omega\}. $$
This defines a random variable $X$ on the probability space $(\Omega, \mathcal{F}, \mathbb{P})$.

Claim: The law of $X$ is $\mu$.
Proof: Fix any real number $a$. We need to show that $\mathbb{P}(X \leq a) = \mu((-\infty, a])$. Now for every $\omega \in \Omega$,
$$ \begin{aligned}
&X(\omega) \leq a \\
&\Leftrightarrow \inf \{t \in \mathbb{R}: \mu((-\infty, t]) \geq \omega\} \leq a \\
&\Leftrightarrow \forall n \in \mathbb{N} \inf \{t \in \mathbb{R}: \mu((-\infty, t]) \geq \omega\} < a + \frac{1}{n} \\
&\Leftrightarrow \forall n \in \mathbb{N} \mu((-\infty, a + \frac{1}{n}]) \geq \omega \\
&\Leftrightarrow \mu((-\infty, a]) \geq \omega. \\
\end{aligned} $$
Hence we have that $\mathbb{P}(X \leq a) = \mathbb{P}(\{\omega \in \Omega: \mu((-\infty, a]) \geq \omega\}) = \mathbb{P}([0,  \mu((-\infty, a])]) =  \mu((-\infty, a])$. Q.E.D.

### Reference:
Bass - Probabilistic Techniques in Analysis 