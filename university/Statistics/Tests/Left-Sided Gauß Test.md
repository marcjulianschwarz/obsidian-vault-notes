---
uni-module: "ISSP"
---

# Left-Sided Gauß Test

Also known as the buyers perspective. This test is used to accept $H_0$ if the [[Test Statistic]] attains values typical for $H_0$ (in this case large values).

- $H_0:\mu\geq\mu_0$
- $H_1:\mu<\mu_0$

[[Acceptance Domain]] $I=[z_{\alpha},\infty)$

> [!TIP] Test Decision (Accept if)
> $$t \in\left[z_\alpha, \infty\right) \Longleftrightarrow \alpha \leq \Phi(t)$$

> [!TIP] Confidence Interval
>
> $$t \in\left[z_\alpha, \infty\right) \Longleftrightarrow \mu_0 \leq \bar{x}+z_1-\alpha \frac{\sigma}{\sqrt{n}}$$

## Errors

The [[Type 1 Error]] is also called "embarrassing error" which we want to minimize:
$$\mathbb{P}_{\mu}\left(\text { reject } H_{0}\right)=\mathbb{P}_{\mu}\left(T_{n}<z_{\alpha}\right)=\Phi_{\lambda}\left(z_{\alpha}\right) \leq \Phi_{0}\left(z_{\alpha}\right)=\alpha \quad\left(\mu \in H_{0}\right)$$

The [[Type 2 Error]] can get large as it would be ok:
$$\beta(\mu)=\mathbb{P}_\mu\left(\operatorname{accept} H_0\right)=1-\Phi_\lambda\left(z_\alpha\right) \quad\left(\mu \in H_1\right)$$
Both errors depend on the $\mu$ that has been chosen or found from an experiment.

## Power Function

The [[Power Function]] is:
$$G(\mu)=\Phi_\lambda\left(z_\alpha\right)$$

![[Bildschirmfoto 2022-05-31 um 10.51.29.png]]

One can see that large values for $\mu$ correspond to small values of the [[Power Function]] and thus correspond to small probability for [[Type 1 Error]].

On the other hand small $\mu$ corresponds to high power and therefor small probability for [[Type 2 Error]].

Also you can tell that the power is quite low when we get near $\mu_0$ on the $H_1$ side of the graph. This corresponds with a hight [[Type 2 Error]].

You can try to get it to look like a 1-0 jump by increasing the [[Entity|sample]] size. Power will get arbitrarily large (also see [[Planning Test Size]])

This test can also be done from the sellers perspective → [[Right-Sided Gauß Test]].
