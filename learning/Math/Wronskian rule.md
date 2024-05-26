---
Date: 2024-04-11
tags:
  - Math
---
### Wronskian and the Wronskian Rule

The Wronskian is a determinant used in the study of differential equations to determine the linear independence of solutions to a linear homogeneous differential equation. The Wronskian of two functions $y_1(t)$ and $y_2(t)$ is denoted as $W(y_1, y_2)(t)$ and is defined as follows:

$$
\large
W(y_1, y_2)(t) = 
\begin{vmatrix}
y_1(t) & y_2(t)\\
y'_1(t) & y'_2(t)
\end{vmatrix}
$$

If $W(y_1, y_2)(t_0) \neq 0$ for some $t_0$, then $y_1(t)$ and $y_2(t)$ are linearly independent on the interval containing $t_0$. The Wronskian Rule provides a convenient criterion to determine if a given set of functions is linearly independent or not.

#### Wronskian Rule:

Consider two functions $y_1(t)$ and $y_2(t)$ satisfying a linear second-order differential equation:

$$
\large
\begin{equation}
\begin{cases}
C_1y_1(t_0) + C_2y_2(t_0) = y_0\\
C_1y'_1(t_0) + C_2y'_2(t_0) = y'_0
\end{cases}
\end{equation}
$$

where $C_1$, $C_2$, $y_0$, and $y'_0$ are constants.

If $W(y_1, y_2)(t_0) \neq 0$ at some point $t_0$, then the functions $y_1(t)$ and $y_2(t)$ form a fundamental set of solutions of the differential equation. This implies that any solution of the differential equation can be expressed as a linear combination of $y_1(t)$ and $y_2(t)$.
