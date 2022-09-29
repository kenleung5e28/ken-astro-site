---
title: "AR models - Properties"
date: "2020-11-08"
draft: false
tags:
- time series
---

#### Definition

A time series \\(\lbrace Z_t\rbrace\\) is said to be \\(\mathrm{AR}(p)\\) when

$$
Z_t = \theta_0 + \phi_1 Z_{t-1} + \phi_2 Z_{t-2} + \cdots + \phi_p Z_{t-p} + a_t
$$
where \\(\lbrace a_t\rbrace \sim \mathrm{WN}(0, \sigma_a^2)\\).

#### Mean

$$
\mu = \frac{\theta_0}{1-\phi_1-\phi_2-\cdots-\phi_p}
$$

#### Variance

$$
\gamma_0 = \frac{\sigma_a^2}{1-\phi_1\rho_1-\phi_2\rho_2-\cdots -\phi_p\rho_p}
$$

#### Autocorrelation function

\\(\rho_1, \rho_2, \ldots, \rho_p\\) are found by solving the Yule-Walker equations:

{{<eqn>}}
\begin{pmatrix}
1 & \rho_1 & \ldots & \rho_{p-1} \\
\rho_1 & 1 & \ldots & \rho_{p-2} \\
\vdots & \vdots & \ddots & \vdots \\
\rho_{p-1} & \rho_{p-2} & \ldots & \rho_1
\end{pmatrix}
\begin{pmatrix}
\phi_1 \\ \phi_2 \\ \vdots \\ \phi_p
\end{pmatrix}
=
\begin{pmatrix}
\rho_1 \\ \rho_2 \\ \vdots \\ \rho_p
\end{pmatrix}
{{</eqn>}}

For \\(k > p\\), \\(\rho_k\\) can be found by
$$
\rho_k = \phi_1 \rho_{k - 1} + \phi_2 \rho_{k - 2} + \cdots + \phi_p \rho_{k - p}
$$

*To continue...*