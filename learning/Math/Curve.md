---
Date: 2024-04-24
tags:
  - Math
---

# Curves
## Real  
Let note with C a curve in the plane that is parametrized by a set of equations $x = x(t)$, $y = y(t)$, $a\leq t \leq b$. where $x(t)$ and $y(t)$ are continuous real functions.
The initial and end points of C are A and B.
1. C is a <mark style="background: #D2B3FFA6;">smooth curve</mark>  if x' and y' are continuous on the closed interval \[a,b\] and not simultaneously zero on the open interval (a,b)  ^30539b
2. C is a <mark style="background: #D2B3FFA6;">piece-wise smooth curve</mark> if it consists of a finite number of smooth curve $C_1,C_2,....,C_n$ joined end to end (The terminal point of one curve $C_k$ coinciding with the initial point of the next curve $C_{k+1}$) ^2382a4
3. C is a <mark style="background: #D2B3FFA6;">simple curve</mark> if the curve C doesn't cross itself except possibly at t = a and t = b
4. C is a <mark style="background: #D2B3FFA6;">closed curve</mark> if A = B ^664d35


![[Curve types.png]]
## Complex
- Suppose the continuous real-valued functions x = x(t), y = y (t), a ≤ t ≤ b, are parametric equations of a curve C in the complex plane.
- By considering z = x + iy , we can describe the points z on C by means of a complex-valued function of a real variable t, called a <mark style="background: #BBFABBA6;">parametrization</mark> of C : z(t) = x(t) + iy (t), a ≤ t ≤ b. Example: The parametric equations x = cos t, y = sin t, 0 ≤ t ≤ 2π, describe a unit circle centered at the origin. A parametrization of this circle is z(t) = cos t + i sin t, or $z(t) = e^{it}$ , 0 ≤ t ≤ 2π.

1. C is <mark style="background: #D2B3FFA6;">smooth</mark> if $z'(t)$ is continuous and never zero in the interval
2. C is a <mark style="background: #D2B3FFA6;">piece-wise smooth</mark> curve if it has a continuously turning tangent, except possibly at the points where the component smooth curves $C_1,C_2,C_3,...,C_n$ are joined together
3. C in a complex plain is <mark style="background: #D2B3FFA6;">simple</mark> if $z(t_1) \neq z(t_2)$, for $t_1 \neq t_2$ , except possibly t=a, t=b
4. C is <mark style="background: #D2B3FFA6;">closed curve</mark> if $z(a) = z(b)$

## References 
1. [[Ch.5_Complex Integration.pdf]]