---
Date: 2024-04-11
tags:
  - Math
---
If g(t) =0 then ODE is called <mark style="background: #ABF7F7A6;">homogeneous</mark>
Principle of superposition: If $y_1(t)$ and $y_2(t)$ are solutions of 2nd linear homogeneous ODE then $C_1y_1 + C_2y_2$ is also a solution
>[!important]
$ay''_1 + by'_1 +cy_1 = 0$ => $C_1(ay''_1 + by'_1 +cy_1) = 0$
$ay''_2 + by'_2 +cy_2 = 0$ => $C_2(ay''_2 + by'_2 +cy_2) = 0$
$a(C_1y_1+C_2y_2)''+b(C_1y_1+C_2y_2)'+c(C_1y_1+C_2y_2) = 0$

- [n] If the function have some proprieties and $y_{(1,2)}$ are ["Nice enough"](Wronskian%20rule.md)  the general solution can be written as:
	$\large C_1y_1 + C_2y_2$

>[!Example]
>$y'' - 9y = 0 \space\space e^{3t}, e^{-3t}$
>$y(t) = C_1e(3t)+C_2e^{-3t}$

$\large ay''_1 + by'_1 +cy_1 = 0$, $\space \space a,b,c \in R$
has a solution $\Large e^{rt}$ were $r \in Z$
	$\large a(e^{rt})''+b(e^{rt})' +c(e^{rt}) =0$ =>
	$\large e^{rt}(ar^2+br+c) = 0$
And we obtain a second order equation with two roots $r_1$ and $r_2$
	$\large ar^2 +br +c = 0$
And we obtain the general solution
	$\large C_1e^{r_1t} + C_2e^{r_2t}$
#### Particular cases(homogeneous)
1. Two real distinct roots $r_1,r_2 \in R \space, r_1\neq r_2$
	$\large y(t) = C_1e^{r_1t} + C_2e^{r_2t}$
2. Two real equal solution $r_1,r_2 \in R \space, r_1=r_2$
	$\large y(t)= C_1e^{rt} + C_2te^{rt}$
3. Two complex roots $r_1,r_2 \in C \space \space r_{1,2} = \lambda \pm \mu i$
	- [i] Is always conjugate 
	$y(t)= \large C_1e^{\lambda t}\cos{\mu t} + C_2e^{\lambda t}\sin{\mu t}$
	- [n] $\lambda$ is real part and $\mu$ imaginary
Also for solving a equation with no constants can be used [[Reduction of order]] is on solution is already known
