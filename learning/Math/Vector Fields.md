---
Date: 2024-05-05
tags:
  - Math
---
# Vector fields 
- A **vector field F in** $R^3$ assigns to each point *P* in a domain *D* a vector *F(P)*
- A vector field in $R^3$ is represented by a vector whose components are functions:
$$\large F(x,y,z)= \langle F_1(x,y,z), F_2(x,y,z), F_3(x,y,z) \rangle$$
- The **domain** of *F* is the set of points *P* for witch *F(P)* is defined
## Types of vector fields
 - A **unit vector field** is a vector field *F* such that $\|F(P)\| = 1$, for all point *P*
 - A vector field is called a **radial vector field** if $F(P) = f(x,y,z)r$,  were $f(z,y,z)$ is a scalar function 
	 - r = $\large \langle x, y \rangle$  and  $\large r = \sqrt{x^2 + y^2}$   for  n = 2
	 - r = $\large \langle x, y, z \rangle$  and  $\large r = \sqrt{x^2 + y^2 + z^2}$   for  n = 3
	- Two examples of **unit radial vector fields** in two and three dimensions:
$$\Large e_r=\langle\frac{x}{r},\frac{y}{r}\rangle \quad e_r=\langle\frac{x}{r},\frac{y}{r},\frac{z}{r}\rangle$$ 
![[Pasted image 20240505213238.png]]
- A **conservative vector field** is of type:
$$\Large F(x,y,z) = \nabla V(x,y,z)= \langle\frac{\partial V}{\partial x},\frac{\partial V}{\partial y},\frac{\partial V}{\partial z}\rangle$$ were *V(x,y,z)* is called a **potential function**
>[!note] Uniqueness of Potential Functions
>if *F* is conservative on a open [[#Connected Domains]] domain, then any two potential functions of *F* differ by a constant
### Cross-Partial property of a conservative vector field
>[!warning] Theorem
>if the vector field $\large F(x,y,z)= \langle F_1, F_2, F_3 \rangle$ is conservative, then $$\Large \frac{\partial F_1}{\partial y} = \frac{\partial F_2}{\partial x}, \quad \frac{\partial F_2}{\partial z} = \frac{\partial F_3}{\partial y}, \quad \frac{\partial F_3}{\partial x} = \frac{\partial F_1}{\partial z}$$
### Connected Domains
A domain is **connected** if any two points can be joined by the path within the domain 
![[Pasted image 20240505213942.png]]



## References 
1. [[Sem2_cap1_04_LineSurf_Int.pdf]]