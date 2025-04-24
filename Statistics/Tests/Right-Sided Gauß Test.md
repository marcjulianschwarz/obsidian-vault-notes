---
uni-module: "ISSP"
---

# Right-Sided Gauß Test

Also known as the sellers perspective. This test is used to accept $H_0$ if the [[Test Statistic]] attains values typical for $H_0$ (in this case small values).

- $H_0:\mu<\mu_0$
- $H_1:\mu\geq\mu_0$

[[Acceptance Domain]] $I=(-\infty,z_{1-\alpha}]$.

> [!TIP] Test Decision (Accept if)
>
> $$t \in\left(-\infty, z_{1-\alpha}\right] \Longleftrightarrow \alpha \leq 1-\Phi(t)$$

> [!TIP] Confidence Interval
>
> $$t \in\left(-\infty, z_1-\alpha\right] \Longleftrightarrow \mu_0 \geq \bar{x}-z_{1-\alpha} \frac{\sigma}{\sqrt{n}}$$

## Errors

The [[Type 1 Error]] is also called "embarrassing error" which we want to minimize:

$$
\begin{aligned}
\mathbb{P}_{\mu}\left(\text { reject } H_{0}\right) &=\mathbb{P}_{\mu}\left(T_{n}>z_{1-\alpha}\right)=1-\Phi_{\lambda}\left(z_{1-\alpha}\right) \\
&<1-\Phi_{0}\left(z_{1-\alpha}\right)=1-(1-\alpha)=\alpha \quad\left(\mu \in H_{0}\right)
\end{aligned}
$$

The [[Type 2 Error]] can get large as it would be ok:
$$\beta(\mu)=\mathbb{P}_\mu\left(\operatorname{accept} H_0\right)=\Phi_\lambda\left(z_{1-\alpha}\right) \quad\left(\mu \in H_1\right)$$
Both errors depend on the $\mu$ that has been chosen or found from an experiment.

## Power Function

The [[Power Function]] is:
$$G(\mu)=1-\Phi_\lambda\left(z_{1-\alpha}\right)=\Phi_{-\lambda}\left(z_\alpha\right)$$

![[Bildschirmfoto 2022-05-31 um 10.54.26.png]]

Similar to the [[Left-Sided Gauß Test]] important statements can be generated from the power function curve.
