---
Date: 2024-04-08
tags:
  - Math
links: "[[Iteration Methods.pdf]]"
---
These are methods which compute a sequence of progressively accurate iterates to approximate the solution of Ax = b.
This methods are used to make the computations less time and memory complex, for example <mark style="background: #ADCCFFA6;">Gaussian elimination</mark> has a time complexity of $\frac{2}{3}n^3$ but iteration methods are $O(n^2)$ or less

## JACOBI’S ITERATION METHOD
Jacobi's iteration method is an iterative technique used to solve systems of linear equations.
Jacobi's iteration method is an iterative technique used to solve systems of linear equations. It can be used for square, diagonally dominant matrices or symmetric positive definite matrices. A matrix is diagonally dominant if the absolute value of each diagonal element is greater than the sum of the absolute values of the other elements in the corresponding row.
$$
\begin{aligned}
\Large a_1x_1 + b_1x_2 + \ldots + c_1x_i &= r_1 \\
\Large a_2x_1 + b_2x_2 + \ldots + c_2x_i &= r_2 \\
&\vdots \\
\Large a_nx_1 + b_nx_2 + \ldots + c_nx_i &= r_n \\
\end{aligned}
$$
he method is applicable to systems of linear equations with any number of variables, as long as the matrix meets the criteria for convergence (such as being diagonally dominant or symmetric positive definite).
$$
\begin{aligned}
\Large x_1^{k+1} &= \frac{1}{a_1}[r_1 - b_1x_2 - \ldots - c_1x_i] \\
\Large x_2^{k+1} &= \frac{1}{a_2}[r_2 - b_2x_1 - \ldots - c_2x_i] \\
&\vdots \\
\Large x_n^{k+1} &= \frac{1}{a_n}[r_n - b_nx_1 - \ldots - c_nx_{n-1}]
\end{aligned}
$$
*Error* = $||x - x^{(k)}|| = max_i|x_i-x_i^{(k)}|$
Time complexity = $O(n^2)$
Order of convergence: linear(usually 0.5)
## GAUSS-SEIDEL ITERATION METHOD
$$
\begin{aligned}
\Large x_1^{k+1} &= \frac{1}{a_{11}}[r_1 - (a_{12}x_2^k + a_{13}x_3^k + \ldots + a_{1n}x_n^k)] \\
\Large x_2^{k+1} &= \frac{1}{a_{22}}[r_2 - (a_{21}x_1^{k+1} + a_{23}x_3^k + \ldots + a_{2n}x_n^k)] \\
&\vdots \\
\Large x_n^{k+1} &= \frac{1}{a_{nn}}[r_n - (a_{n1}x_1^{k+1} + a_{n2}x_2^{k+1} + \ldots + a_{n,n-1}x_{n-1}^{k+1})]
\end{aligned}
$$
*Error* = $||x - x^{(k)}|| = max_i|x_i-x_i^{(k)}|$
Time complexity = $O(n^2)$
Order of convergence: linear(usually around 0.05 - 0.2)

## Difference

The main difference between Jacobi's iteration method and the Gauss-Seidel iteration method lies in how they update the values of the variables in each iteration.

1. **Jacobi's Iteration Method:** In Jacobi's method, all the variables are updated simultaneously using the values from the previous iteration. This means that the new value for each variable is based on the old values of all the variables from the previous iteration.

2. **Gauss-Seidel Iteration Method:** In the Gauss-Seidel method, each variable is updated as soon as its new value is computed. This means that when computing the new value for `x_i`, the method uses the updated values for `x_1`, `x_2`, ..., `x_{i-1}` from the current iteration, rather than the old values from the previous iteration.

Because Gauss-Seidel uses the most recent values for the variables in each iteration, it often converges faster than Jacobi's method, especially for systems of equations where the matrix is diagonally dominant. However, Gauss-Seidel requires more careful implementation due to the dependencies between variable updates.