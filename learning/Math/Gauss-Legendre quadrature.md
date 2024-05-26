---
Date: 2024-05-20
tags:
  - Math
---
In numerical analysis, Gauss–Legendre quadrature is a form of Gaussian quadrature for approximating the [definite integral](Real%20Integration#Definite%20Integral) of a function. For integrating over the interval \[−1, 1], the rule takes the form: 
$$\LARGE \int_{-1}^1 f(x)dx = \sum^{n}_{i = 1} w_if(x_i)$$
where
- n is the number of sample points used,
- $w_i$ are quadrature weights, and
- $x_i$ are the roots of the nth [[Legendre polynomials]].

$\Large x_i$ is the i-th root of $\large P_n(x)$ and the weight $\large w_i$ can be found by the formula 
$$\LARGE w_i = \frac{2}{(1-x_i^2)[P'_n(x_i)]^2}$$


## References 
1. https://en.wikipedia.org/wiki/Gauss%E2%80%93Legendre_quadrature