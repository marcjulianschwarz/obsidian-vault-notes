---
uni-module: "ISSP"
---

# Two-Sided Gauß Test

A way to statistically infer if the [[Erwartungswert|Expectation]] from experiments does not equal the real [[Erwartungswert|Expectation]]. $H_0$ gets accepted when the [[Test Statistic]] attains values typical of $H_0$ (in this case values close to $\mu_0$, small in modulus).

- $H_0 : \mu=\mu_0$
- $H_1 : \mu \neq \mu_0$

[[Acceptance Domain]] $I=\left[z_{\alpha / 2}, z_{1-\alpha / 2}\right]$.

> [!TIP] Test Decision (Accept if)
> $$t \in\left[z_{\alpha / 2}, z_{1-\alpha / 2}\right] \Longleftrightarrow \alpha \leq 2 \min \{\Phi(t), 1-\Phi(t)\}=2 \Phi(-|t|)$$

> [!TIP] Confidence Interval
>
> $$t \in\left[z_{\alpha / 2}, z_{1-\alpha / 2}\right] \Longleftrightarrow \mu_0 \in\left[\bar{x}-z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}, \bar{x}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}\right]$$

## Errors

[[Type 1 Error]]:
$$\mathbb{P}_{\mu_0}\left(\text { reject } H_0\right)=\mathbb{P}_{\mu_0}\left(T_n<z_{\alpha / 2}\right)+\mathbb{P}_{\mu_0}\left(T_n>z_{1-\alpha / 2}\right)=\alpha / 2+1-(1-\alpha / 2)=\alpha$$

[[Type 2 Error]]:

$$
\begin{aligned}
\beta(\mu) &=\mathbb{P}_\mu\left(\operatorname{accept} H_0\right)=\Phi_\lambda\left(z_{1-\alpha / 2}\right)-\Phi_\lambda\left(z_{\alpha / 2}\right) \\
&=\Phi_\lambda\left(z_{1-\alpha / 2}\right)+\Phi_{-\lambda}\left(z_{1-\alpha / 2}\right)-1 \quad\left(\mu \in H_1\right)
\end{aligned}
$$

## Power Function

The [[Power Function]] is:
$$G(\mu)=1-\Phi_\lambda\left(z_{1-\alpha / 2}\right)+\Phi_\lambda\left(z_{\alpha / 2}\right)$$
![[Bildschirmfoto 2022-05-31 um 11.18.58.png]]

## Critics for this Test

- Detecting Inequality / Difference vs. Detecting Equality (impossible with infinite many values)
- often $\mu\in[\mu_0-\delta,\mu_0+\delta]$ acceptable (less restrictive)
- or equivalence test for $H_0$: $|\mu-\mu_0|>\delta$ and for $H_1\leq\delta$

## Confidence Interval

The [[Confidence Interval]] for the two-sided Gauß Test can be calculated like this:

![[Bildschirm­foto 2023-02-10 um 10.51.06.png]]
