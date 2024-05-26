---
Date: 2024-04-12
tags:
  - Math
---
1. **Non-homogeneous Equation**:
	y'' + p(t)y' + q(t)y = g(t) 
2. **Homogeneous Equation**:
	y'' + p(t)y' + q(t)y = 0 

For case (2), let's suppose $y_1(t)$ and $y_2(t)$ are solutions.

### Complementary Solution ($y_c$):
  The general solution of the [[Homogeneous 2nd ODE]] (2) is represented as:
	  $\large y(t) = C_1y_1 + C_2y_2$
### Particular Solution ($Y_p(t)$):
	$\large Y_p(t) = n_1(t)y_1(t)+n_2(t)y_2(t) = n_1y_1+n_2y_2$
- We need to find $n_1$ and $n_2$ such than $Y_p$ to be a solution
	$\large Y'_p(t)=n_1y'_1+n_2y'_2+(n'_1y_1+n'_2y_2)$
- [*] <mark style="background: #ADCCFFA6;">Best case is when</mark> $(n'_1y_1+n'_2y_2) = 0$
	$\large Y''_p(t) = n'_1y'_1+n_1y''_1+n'_2y'_2+n''_2y''_2$
	$\large n_1(y''_1+py'_1+qy_1)+n_2(y''_2+py'_2+qy_2) + n_1'y'_1 +n'_2y'_2 = g(t)$
- [i] $y_1$ and $y_2$ are solutions of the homogeneous equations so 
	$\large n_1(y''_1+py'_1+qy_1) = 0$   and $\large n_2(y''_2+py'_2+qy_2) = 0$
	So $\large n_1'y'_1 +n'_2y'_2 = g(t)$
Now we have
$$
\large
\begin{equation}
\begin{cases}
(n'_1y_1+n'_2y_2) = 0\\
 n_1'y'_1 +n'_2y'_2  = g(t)
\end{cases}
\end{equation}
$$
Then we use [[Wronskian rule]]
$$
\large
W(y_1, y_2)(t) = 
\begin{vmatrix}
y_1(t) & y_2(t)\\
y'_1(t) & y'_2(t)
\end{vmatrix}
$$
$$\Large n'_1=-\frac{y_2g}{y_1y'_2-y'_1y_2}$$
$$\Large n'_2=\frac{y_1g}{y_1y'_2-y'_1y_2}$$
Then we need to integrate and we will get $n_1$ and $n_2$
$Y_p = n_1y_1+n_2y_2$