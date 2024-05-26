---
Date: 2024-04-24
tags:
  - Math
---

# Definite Integral
## Method of evaluating 
>[!important]
> If $F(x)$ is an anti-derivative of a continuous function f , i.e., F is a function for which F ′(x) = f (x), then the definite integral of f on the interval [a, b] is the number
> $$
> \large \int_a^b f(x)dx = F(x)|_a^b = F(b)- F(a)
> $$

## Definition of Definite Integral
>[!info] Definition (Definite Itegral)
>The definite integral of f on [a,b] is
>$$
>\large \int_a^bf(x)dx = \lim_{||P||-> 0} \sum_{k=1}^nf(x^*_k) \Delta x_k
>$$
- <mark style="background: #BBFABBA6;">P</mark> is the partition of the interval \[a,b\]:
	$\large a = x_0<x_1<x_2<...<x_{n-1}<x_n = b$
- <mark style="background: #ABF7F7A6;">||P||</mark>  is the norm of partition P of \[a,b\] (the length of the longest sub interval)
- $\Large x_k^*$ is a chosen number on each sub interval $[x_{k-1},x_k]$ of \[a,b]
- $\Large \Delta x_k = x_k - x_{k-1}$

# Line Integrals 
## Definition
>[!info] Definition (Line Integrals in the Plane)
>1. The line integral of G along C with respect to x is:
>$$
>\large \int_C G(x,y)dx = \lim_{||P||->0} \sum_{k=1}^n G(x_k^*,y_k^*) \Delta x_k
>$$
>2. The line integral of G along C with respect of Y is:
>$$
>\large \int_C G(x,y)dy = \lim_{||P||->0} \sum_{k=1}^n G(x_k^*,y_k^*) \Delta y_k
>$$
>3. The line integral of G along C with respect to arc length s is:
>$$
>\large \int_C G(x,y)ds = \lim_{||P||->0} \sum_{k=1}^n G(x_k^*,y_k^*) \Delta s_k
>$$
- <mark style="background: #BBFABBA6;">G</mark> is a function of two real variables x and y , defined at all points on a smooth [[Curve]] C that lies in some region of the xy-plane. Let C be defined by the parametrization x = x(t), y = y (t), a ≤ t ≤ b.
- P is a partition of the parameter interval \[a,b] sub intervals $[t_{k-1},t_k]$ of length $\large \Delta t_k = t_k - t_{k-1}$ 
	The partition P induces a partition of the Curve into n sub arcs of length
	$\Delta s_k$ , $\Delta x_k$ and $\Delta y_k$ are the length of projections of it on x- and y-axes 
- ‖P‖ is the norm of the partition P of \[a, b], that is, the length of the longest sub interval.
- $\large (x_k^*,y_k^*)$ is a Chosen point on each sub arc of C
![[images/Line_Integral_curve.png]]
## Methods of evaluation 

- To solve a line integral is needed to convert it in a [[#Definite Integral]]
### C is a smooth curve
- If C is a [smooth curve](Curve#^30539b) parametrized by x = x(t) , y =y(t), $a \leq t \leq b$, then replace 
	- x and y in the integral by the functions x(t) and y(t)	>	- the appropriate deferential; dx, dy, or ds by
		$\large x'(t)dt$,     $\large y'(t)dt$,    $\large \sqrt{[x'(t)]^2 + [y'(t)]^2}dt$
- The line integral become definite$$
 \Large 
 \begin{align*} 
 \int_C G(x,y) \, dx &= \int_a^b G(x(t),y(t)) x'(t) \, dt \\ 
  \int_C G(x,y) \, dy &= \int_a^b G(x(t),y(t)) y'(t) \, dt \\ 
 \int_C G(x,y) \, ds &= \int_a^b G(x(t),y(t)) \sqrt{[x'(t)]^2 +[y'(t)]^2} \, dt \end{align*}
$$

### C is a graph of a given function
- If the path of integration C is the graph of an explicit function y = f (x), a ≤ x ≤ b, then we can use x as a parameter.
- The differential of y is $dy = f'(x)dx$ and the differential of arc length is $ds = \sqrt{1+[f'(x)]^2}$
- And the definite integrals will be$$
 \Large 
\begin{align*} 
\int_C G(x,y) \, dx &= \int_a^b G(x,f(x)) \, dx \\ 
 \int_C G(x,y) \, dy &= \int_a^b G(x,f(x)) f'(x) \, dx \\ 
\int_C G(x,y) \, ds &= \int_a^b G(x,f(x)) \sqrt{1 +[f'(x)]^2} \, dx 
\end{align*}
$$
### C is a [piece-wise](Curve#^2382a4) smooth curve
A line integral along a piecewise smooth curve C is defined as the sum of the integrals over the various smooth pieces.$$
\Large \int_C G(x,y) \, ds = \int_{C_1} G(x,y) \, ds + \int_{C_2} G(x,y) \, ds
$$
### C is a [closed curve](Curve#^664d35)
A line integral along a closed curve C is usually denoted by$$
\Large \oint_C Pdx + Qdy
$$
>[!info]
>Line segment from (a,b) to (c,d):
>$x = t * c + (1-t) * a$
>$y = t * d + (1-t) * b$
## References 
1. [[Ch.5_Complex Integration.pdf]]