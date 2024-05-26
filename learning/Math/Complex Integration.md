---
Date: 2024-04-24
tags:
  - Math
link:
  - "[[Complex numbers and planes]]"
---
# Complex Integrals
## Definition

>[!info] Definition (Complex Integral)
>The **complex integral** of f on C is$$\large \int_C f(z)dz = \lim_{||P||-> 0} \sum_{k=1}^n f(z_f^*) \Delta z_k$$
- <mark style="background: #BBFABBA6;">P</mark> is the partition of the interval \[a,b\]:
	$\large a = t_0<t_1<t_2<...<t_{n-1}<t_n = b$
- <mark style="background: #ABF7F7A6;">||P||</mark>  is the norm of partition P of \[a,b\] (the length of the longest sub interval)
- $\Large z_k^*=x_k^* + iy_k^*$ is a chosen number on each sub interval $[t_{k-1},t_k]$ of \[a,b]
- $\Large \Delta z_k = z_k - z_{k-1}$

## Methods of solving
### Integral of Complex Valued Function of a Real Variable
$f(t)$ can be write as $\large f(t) = f_1(t)+if_2(t)$  if $f_1$ and $f_2$ are real-valued functions of a real variable t continuous on a common interval $a \leq t \leq b$ 
$$\int_a^bf(t)dt = \int_a^bf_1(t)dt + i\int_q^bf_2(t)dt$$
### Contour Integral

>[!info] Theorem (Evaluation of a Contour Integral)
>if f is continuous on a smooth curve C given by $z(t)=x(t)+iy(t)$ , $a\leq t\leq b$ , then $$
>\large \int_Cf(z)dz = \int_a^bf(z(t))z'(t)dt
>$$


## References 
1. [[Ch.5_Complex Integration.pdf]]