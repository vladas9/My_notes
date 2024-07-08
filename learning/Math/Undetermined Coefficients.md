---
tags:
  - Math
---
## Method of Undetermined Coefficients
1. **Non-homogeneous Equation**:
	y'' + p(t)y' + q(t)y = g(t) 
2. **Homogeneous Equation**:
	y'' + p(t)y' + q(t)y = 0 

For case (2), let's suppose $y_1(t)$ and $y_2(t)$ are solutions.

- **Complementary Solution ($y_c$)**:
  The general solution of the [[Homogeneous 2nd ODE]] (2) is represented as:
  $y(t) = C_1y_1 + C_2y_2$

- **Particular Solution ($Y_p(t)$)**:
  If $Y_p(t)$ is a particular solution of the non-homogeneous equation (1), then the general solution of (1) is:
  $y(t) = C_1y_1 + C_2y_2 + Y_p$
  where $C_1$ and $C_2$ are constants.
How to find the $Y_p$:

| $g(t)$                                                                        | $Y_p(t)$                                        |
| ----------------------------------------------------------------------------- | ----------------------------------------------- |
| $\large \alpha e^{\beta t}$                                                   | $\large Ae^{\beta t}$                           |
| $\large \alpha \cos(\beta t) + \gamma \sin(\beta t)$<br>(or only one of them) | $\large A\cos(\beta t) + B\sin(\beta t)$        |
| poly. of degree n                                                             | $\large A_1t^n + A_2t^{n-1}+...+A_{n-1}t + A_n$ |
| $g_1(t) + g_2(t)$                                                             | $Y_{1p}+Y_{2p}$                                 |
- [i] If the particular solution  $\large e^{\beta t}$ is already in the complimentary solution  $\large y_c$ then we should write $\large Ate^{\beta t}$
>[!Warning]
>- Equations involving fractions or rational functions
> - Equations involving roots or radicals
> - Equations involving power functions with non-integer exponents
> - Equations involving logarithmic or exponential functions in more complex forms
>
> In such cases, alternative methods or specialized techniques may be required to find the particular solution $Y_p(t)$.

