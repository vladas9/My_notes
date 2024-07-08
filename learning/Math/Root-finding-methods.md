# 1. Bisection
Bisection is based on the calculus theorem
>[!info] Theorem
>if $\large f:[a,b] \rightarrow R$ is a continues function closed and bounded interval \[a,b] and 
>$$\large f(a) \cdot f (b) < 0$$
>then there exists $\large \alpha \in [a,b]$ such that $\large f(\alpha) = 0$  

## Steps for computing
1. Compute $\Large c = \frac{a+b}{2}$
2. If $\Large b-c < \epsilon$, accept c as our root, and then stop
3. if $\Large b-c > \epsilon$, then compare the sign of f(c) to that of f(a) and f(b). If 
		$$\large sign(f(a)) \cdot sign(f(c)) < 0$$then replace b with c; Otherwise, replace a with c
4. Return to step 1
## Errors
The formula to calculate error of the bisection method is$$\Large|\alpha - c_n| \leq \frac{1}{2^n}(b-a)$$
were n is the number of iterations
To find the number of iterations to a certain tolerance $\large \epsilon$ $$\Large n \geq \frac{\ln{\frac{b-a}{\epsilon}}}{\ln2}$$
## Advantages and Disadvantages of Bisection Method
Advantages:
1. It always converges.
2. You have a guaranteed error bound, and it decreases with each successive iteration.
3. You have a guaranteed rate of convergence. The error bound decreases by 1/2 with each iteration.
Disadvantages:
1. It is relatively slow when compared with other root-finding methods we will study, especially when the function f (x) has several continuous derivatives about the root α.
2. The algorithm has no check to see whether the ε is too small for the computer arithmetic being used.
# Newton's method
## computations
Starting with the initial guess $x_0$ $$\Large x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}, \quad n=0,1,2,\dots$$
## Error
$$\Large \alpha - x_{n+1} \approx (\alpha - x_n)^2\frac{-f''(\alpha)}{2f'(\alpha)}$$
## Advantages and Disadvantages of Newton’s Method
Advantages:
1. Fast convergence (usually quadratic convergence).
2. There is a stopping criterion.
Disadvantages:
1. It may fail to converge (for example, when initial guess is not close enough).
2. It needs also the derivative of the function.
3. There is no guaranteed error bound for the computed iterates.
4. It is likely to have difficulty if f ′ (α) = 0. This means the x −axis is tangent to the graph of y = f ( x ) at x = α.
# Secant method
## computations 
$$\Large x_{n+1} = x_1 - f(x_1) \div \frac{f(x_n)-f(x_{n-1})}{x_n-x_{n-1}}, \quad n=1,2,3,\dots$$
## Error
$$\Large |\alpha - x_{n+1}| \approx |\alpha - x_n|^{1.62}\frac{-f''(\alpha)}{2f'(\alpha)}$$
## Advantages and Disadvantages of Secant Method
Advantages:
1. Secant method converges at faster than a linear rate, so that it is more rapidly convergent than the bisection method.
2. It does not require use of the derivative of the function, something that is not available in a number  of applications.
3. It requires only one function evaluation per iteration, as compared with Newton’s method which requires two.
Disadvantages:
1. Secant method may not converge.
2. There is no guaranteed error bound for the computed iterates.
3. It is likely to have difficulty if f ′ (α) = 0. This means the x −axis is tangent to the graph of y = f ( x ) at x = α.
4. Newton’s method generalizes more easily to new methods for solving simultaneous systems of nonlinear equations.
# Fixed point iterations
## General form
$$\Large x_{n+1} = g(x_n), \quad n=0,1,2,\dots$$
