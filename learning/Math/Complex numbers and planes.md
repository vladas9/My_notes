---
Date: 2024-05-04
tags:
  - Math
---
# Complex number
>[!hint] Definition (Complex number)
>A **complex number **  is any number of the form $z = a+ib$ where *a* and *b* are real numbers and i is the imaginary unit
- The **imaginary unit** $i = \sqrt{-1}$ is defined by the property $i^2 = -1$
- The real number *a* in $z= a + ib$ is called the **real part** of *z* and the real number *b* is called the **imaginary part** of *z*. (this parts can be noted as Re(z) and Im(z))
- A number with only Im(z) is called a **pure imaginary number**
>[!info] Equality for 2 complex numbers
>Complex numbers $z_1 = a_1 + ib_1$ and $z_2= a_2 +ib_2$ are **equal** if $a_1=a_2$ and $b_1=b_2$
- The **set of complex numbers** is denoted by the symbol $C$
- $R \subset C$ (real number are a subset of complex)
## Operations with complex numbers
For $z_1 = a_1 + ib_1$ and $z_2= a_2 +ib_2$, the operations of addition, subtraction, multiplication and division are defined as follows:
- **Addition**: 
$$\large z_1 + z_2 = (a_1+ a_2) + i(b_1+b_2)$$
-  **Subtraction:**
$$\large z_1 - z_2 = (a_1-a_2) + i(b_1+b_2)$$
- **Multiplication:**
$$\large z_1 \cdot z_2 = a_1a_2-b_1b_2 + i(b_1a_2+a_1b_2)$$
- **Division:**
$$\large \frac{z_1}{z_2} = \frac{a_1a_2+b_1b_2}{a_2^2+b_2^2} + i\frac{b_1a_2-a_1b_2}{a_2^2+b_2^2}$$
## Conjugates
>[!info] Conjugate of a complex number
>The number obtained by changing the sign of its imaginary part in called the **complex conjugate**, or simply conjugate, of *z* and is denoted by the symbol $\large \overline{z}$

# Complex plane
## Points
 A complex number $z = x + iy$ can be  determined by a ordered pair of real numbers (x,y) were *x* is the <span style="color:#0070c0">real</span> part and *y* the <span style="color:#00b050">imaginary</span> one. 
## Vectors
A complex number $z=x+iy$ can be also represented as a vector with beginning in origin and ending in the point (x,y)
## Modulus
>[!info] Modulus of a complex number
>The **modulus** of a complex number $z=x+iy$, is the real number $|z| = \sqrt{(x^2+y^2)}$ , it also is called the **absolute value** of z
### Properties
- $\Large |z|^2 = z\bar{z}$     and    $\Large |z|=\sqrt{z\bar{z}}$ 
# Polar form of complex numbers
## Polar coordinates
- A pint *P*  with a rectangular coordinates can be also described in term of polar coordinates
- The polar coordinates system consist of:
	1. A point *O* called the **pole**
	2. the horizontal half-line emanating from the pole called **polar axis**
	3. *r* is the directed distance from the pole to *P*
	4. $\large \theta$ an angel (in radians) between polar axis and line *OP*
![[Pasted image 20240505124005.png]]
### For complex numbers
$\Large x = r\cos{\theta}$   and   $\large y=\sin{\theta}$ 
$$\Large z = r(\cos{\theta} + i\space sin(\theta))$$
- *r* <span style="color:#9c59cf">is never negative</span> and is equal to the modulus of *z*:    $\large r=|z|$
- $\large \theta$ is the argument of z, $\large \theta = \arg(z)$, and 
	- $\Large \cos{\theta} = \frac{x}{r}$    and     $\Large \sin{\theta} = \frac{y}{r}$
	- Also exist **principal argument** of z, $Arg(z)$
	    $\Large -\pi < Arg(z) \leq \pi$
	- $\large arg(z)= Arg(z) + 2\pi n$ , $n=0,\pm 1,\pm 2, ...$
## Operations with polar form
- **Multiplication:**
$$\Large z_1z_2=r_1r_2[\cos{(\theta_1 + \theta_2)} + i\space\sin{(\theta_1 + \theta_2)}]$$
- **Division:**
$$\Large \frac{z_1}{z_2}=\frac{r_1}{r_2}[\cos{(\theta_1 - \theta_2)} + i\space\sin{(\theta_1 - \theta_2)}]$$
- **Power:**
$$\Large z^n = r^n[\cos{n\theta} + i\sin{n\theta}]$$
- **Roots:**
$$\Large w_k = \sqrt[n]{r}[\cos(\frac{\theta + 2k\pi}{n}) + i\space sin(\frac{\theta + 2k\pi}{n})]$$$$\Large k = 0,1,...., n-1$$







## References 
1. [[Ch.1_Complex Numbers.pdf]]