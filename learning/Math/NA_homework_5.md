---
Date: 2024-04-24
tags:
  - Math
---

# Problem 5.1
$$
\Large
\begin{equation}
\begin{cases}
2x_1 + x_2 = 3\\
-x_1 +2x_2 + x_3 = 2\\
-x_2 + 2x_3 + x_4 = 2\\
-x_3 + 2x_4 + x_5 = 2 \\
-x_4 +2x_5 = 1\\
\end{cases}
\end{equation}
=>
$$
$$
\Large
\begin{equation}
\begin{cases}
x_2 = 3 - 2x_1\\
x_3 = -4 + 5x_1\\
x_4 = 13 - 12x_1\\
x_5 = -28 +29x_1 \\
70x_1 = 70\\
\end{cases}
\end{equation}
=>
$$
$$
\Large
\begin{equation}
\begin{cases}
x_2 = 1\\
x_3 = 1\\
x_4 = 1\\
x_5 = 1 \\
x_1 = 1\\
\end{cases}
\end{equation}
$$
# Problem 5.2

### Gaussian Elimination

**Step 1: Form the Augmented Matrix**
Start by augmenting matrix $A$ with vector $b$:
$$
\begin{bmatrix}
3 & -1 & 0 & | & 11 \\
1 & 2 & -2 & | & 2 \\
1 & 2 & 0 & | & 0
\end{bmatrix}
$$

**Step 2: Transforming the matrix in a upper triangular matrix**
$$
\begin{bmatrix}
1 & 2 & 0 & | & 0 \\
0 & -7 & 3 & | & 11 \\
0 & 0 & -2 & | & 2
\end{bmatrix}
$$

**Step 4: Back Substitution**
Solve for $x_3$ from the third row:
$$x_3 = \frac{-3}{2} = -1$$
Solve for $x_2$ from the second row:
$$x_2 = \frac{11 + 3}{-7} = -2$$
Solve for $x_1$ from the first row:
$$x_1 = \frac{4}{1} = 4$$

The solution vector $x$ is:
$$x = \begin{bmatrix} 4 \\ -2 \\ -1 \end{bmatrix}$$

### LU Factorization

The LU factorization process involves decomposing matrix $A$ into $L$ (lower triangular) and $U$ (upper triangular) matrices. As computed:

$$L = \begin{bmatrix} 1 & 0 & 0 \\ 3 & 1 & 0 \\ 1 & 0 & 1 \end{bmatrix}$$
$$U = \begin{bmatrix} 1 & 2 & 0 \\ 0 & -7 & 3 \\ 0 & 0 & -2 \end{bmatrix}$$
# Problem 5.3
  
$$ 
\Large
\begin{pmatrix}
	x_1^{(m+1)} \\ 
	x_2^{(m+1)} \\ 
	x_3^{(m+1)} 
\end{pmatrix} = 
\begin{pmatrix} 
-\frac{2}{3} \\ 
5 \\ 
4 
\end{pmatrix} - \frac{1}{10}
\begin{pmatrix} 
0 & 3 & 1 \\ 
-2 & 0 & -3 \\ 
1 & 4 & 0 
\end{pmatrix} 
\begin{pmatrix} x_1^{(m)} \\ 
x_2^{(m)} \\ 
x_3^{(m)} 
\end{pmatrix} 
$$
### Problem Resolution

The iteration method we are analyzing is:

$$ \mathbf{x}^{(m+1)} = \mathbf{b} + B \mathbf{x}^{(m)} $$

where:

$$ \mathbf{b} = \begin{pmatrix} -\frac{2}{3} \\ 5 \\ 4 \end{pmatrix} $$
$$ B = -\frac{1}{10} \begin{pmatrix} 0 & 3 & 1 \\ -2 & 0 & -3 \\ 1 & 4 & 0 \end{pmatrix} $$

To assess the convergence, we need to compute the eigenvalues of matrix $B$ and determine its spectral radius $\rho(B)$.

### Characteristic Polynomial and Eigenvalues

First, we compute the characteristic polynomial  $p(\lambda)$ of matrix  $B$:

$$ B - \lambda I = -\frac{1}{10} \begin{pmatrix} -\lambda & 3 & 1 \\ -2 & -\lambda & -3 \\ 1 & 4 & -\lambda \end{pmatrix} $$

The characteristic polynomial is found by taking the determinant:

$$ \det(B - \lambda I) = 0 $$

Using Python and the `sympy` library, we calculate the eigenvalues:

```python
from sympy import symbols, Matrix, det, solve

# Define the variable and matrix elements
lambda_ = symbols('lambda')
B = Matrix([
    [-lambda_, 3, 1],
    [-2, -lambda_, -3],
    [1, 4, -lambda_]
])

# Calculate the determinant of (B - lambda * I)
char_poly = det(B)

# Solve for lambda (eigenvalues)
eigenvalues = solve(char_poly, lambda_)
```
### Numeric Approximations of Eigenvalues

Next, we find the absolute values of these eigenvalues to assess the spectral radius:
```python
import cmath

magnitude1 = abs(complex(0.475, 4.204))  # For the first complex eigenvalue
magnitude2 = abs(complex(-0.95, 0))      # For the real eigenvalue
```

### Convergence Analysis

Given that one of the eigenvalue magnitudes, ∣0.475+4.204𝑖∣≈4.231, is greater than 1, the spectral radius 𝜌(𝐵) is greater than 1. Thus, we conclude:

𝜌(𝐵)>1

Therefore, the iteration method does **not** converge for any initial guess 𝑥(0) as 𝑚→∞.

# Problem 5.4
### 1. Gaussian Elimination

**Description of the Method:** Gaussian Elimination is a systematic method for solving systems of linear equations. It works by converting the system into an upper triangular form using a sequence of operations:

1. **Pivoting:** Swap rows to position a non-zero element (or the largest absolute value for numerical stability) as the pivot element.
2. **Elimination:** Use elementary row operations to create zeros below the pivot, effectively reducing the system step-by-step into an upper triangular matrix.
3. **Back Substitution:** Once the matrix is in upper triangular form, solve for the unknowns starting from the last row and substituting backward up to the first row.

**Reason for Choosing:**

- **Accuracy:** Gaussian Elimination will find the exact solution for non-singular (i.e., invertible) matrices assuming no numerical instabilities.
- **Universality:** This method can be applied to any system of linear equations, provided the matrix is square and non-singular.
- **Ease of Use:** It's widely supported by many mathematical software libraries, making it easy to implement and use.

Using the `numpy.linalg.solve` function, the Gaussian Elimination approach solves the system directly. Here's how it works:

- **Setup the coefficient matrix 𝐴A** and **right-hand side vector 𝑏b**.
- **Invoke the solve function** which internally applies Gaussian Elimination to find the solution.
```python
import numpy as np

# Define the coefficient matrix A and the vector b based on the provided equations
A = np.array([
    [0, 1, 5, -7, 23, -1, 7, 8, 1, -5],
    [17, 0, -24, -75, 100, -18, 10, -8, 9, -50],
    [3, -2, 15, 0, -78, -90, -70, 18, -75, 1],
    [5, 5, -10, 0, -72, -1, 80, -3, 10, -18],
    [100, -4, -75, -8, 0, 83, -10, -75, 3, -8],
    [70, 85, -4, -9, 2, 0, 3, -17, -1, -21],
    [1, 15, 100, -4, -23, 13, 0, 7, -3, 17],
    [16, 2, -7, 89, -17, 11, -73, 0, -8, -23],
    [51, 47, -3, 5, -10, 18, -99, -18, 0, 12],
    [1, 1, 1, 1, 1, 1, 1, 1, 1, 1]
])
b = np.array([10, -40, -17, 43, -53, 12, -60, 100, 0, 100])

# Solve the system using Gaussian Elimination
x_ge = np.linalg.solve(A, b)
print("Solution using Gaussian Elimination:", x_ge)
```
### 2. Gauss-Seidel Method

**Description of the Method:** The Gauss-Seidel method is an iterative approach to solving systems of linear equations. It improves upon the Jacobi method by using the latest updates of the solution as soon as they are available: 
1. **Iteration:** For each unknown, update its value using the latest values of the other unknowns. This involves a loop over each equation in the system where each unknown $x_i$ is updated according to the formula: $$ x_i^{(k+1)} = \frac{1}{a_{ii}} \left( b_i - \sum_{j=1}^{i-1} a_{ij} x_j^{(k+1)} - \sum_{j=i+1}^n a_{ij} x_j^{(k)} \right) $$ Here, $x_i^{(k+1)}$ is the new value of $x_i$, $a_{ii}$ is the diagonal element of the matrix A, and $b_i\$ is the ith component of the vector $b$. 
2. **Convergence Checking:** After each full iteration over all unknowns, check if the change in the values of the unknowns is below a certain tolerance. If yes, the method has converged. 
**Reason for Choosing:** 
- **Efficiency for Large Systems:** Particularly effective for large systems where direct methods (like Gaussian Elimination) become computationally expensive.
- **Diagonal Dominance:** Performs well when the system matrix is diagonally dominant. 
- **Flexibility:** Allows stopping the computation early based on a convergence criterion, which can be adjusted depending on the desired precision.

**Solution**
- **Initialize the solution vector 𝑥x** with zeros or an initial guess.
- **Iteratively update the solution** using the latest values as soon as they are calculated.
- **Stop when the changes between iterations are below a specified tolerance** or after a maximum number of iterations.
```python
def gauss_seidel(A, b, tolerance=1e-10, max_iterations=1000):
    x = np.zeros_like(b)
    for _ in range(max_iterations):
        x_new = np.copy(x)
        for i in range(A.shape[0]):
            s1 = np.dot(A[i, :i], x_new[:i])
            s2 = np.dot(A[i, i+1:], x[i+1:])
            x_new[i] = (b[i] - s1 - s2) / A[i, i]
        if np.allclose(x, x_new, atol=tolerance):
            break
        x = x_new
    return x

x_gs = gauss_seidel(A, b)
print("Solution using Gauss-Seidel Method:", x_gs)
```

#   Problem 5.5
## Gauss-Seidel iteration
```python
def seidel(a, x ,b): 
	n = len(a) 
	for j in range(0, n): d = b[j]
		for i in range(0, n): 
			if(j != i): 
				d-=a[j][i] * x[i] 
		x[j] = d / a[j][j] 
	return x 
n = 3 
a = [] 
b = [] 
x = [1, 1, 1] 
a = [[8, 3, 2],[16, 6, 4.001],[4, 1.501, 1]] 
b = [20,40.02,10.01] 
print(x) 
for i in range(0, 100): (Here instead of 100 I putted different values) 
	x = seidel(a, x, b) 
print(x)
```

100 - \[1.6561404802082513, 1.31321962401241, 1.414295423524367] 
1000 - \[-0.0031291584832748853, 3.870574324381843, 4.212784573035953] 
10000 - \[53.59884032658795, 140.8457660787976, -415.794856190627] 
100000 - \[2.2210050610350445e+23, 4.9045479313876515e+23, -1.6245746689153043e+24] 
As we can see it doesn’t converge! So it isn’t efficient with this initial guess.

## Gauss-Jordan method
```python
M = 10 
def PrintMatrix(a, n): 
	for i in range(n): 
		print(*a[i]) 
def PerformOperation(a, n): 
	i = 0 
	j = 0 
	k = 0 
	c = 0 
	flag = 0 
	for i in range(n): 
		if (a[i][i] == 0): 
			c = 1 
			while ((i + c) < n and a[i + c][i] == 0): 
				c += 1 
			if ((i + c) == n): 
				flag = 1
				break
			j = i 
			for k in range(1 + n): 
				temp = a[j][k] 
				a[j][k] = a[j+c][k] 
				a[j+c][k] = temp 
		for j in range(n): 
			if (i != j): 
				p = a[j][i] / a[i][i]
				k = 0 
				for k in range(n + 1): 
					a[j][k] = a[j][k] - (a[i][k]) * p 
	return flag

def PrintResult(a, n, flag): 
	print("Result is : ") 
	if (flag == 2): 
		print("Infinite Solutions Exists") 
	elif (flag == 3): 
		print("No Solution Exists") 
	else: for i in range(n): 
		print(a[i][n] / a[i][i], end=" ")

def CheckConsistency(a, n, flag): 
	flag = 3 
	for i in range(n): 
		sum = 0 
		for j in range(n): 
			sum = sum + a[i][j] 
			if (sum == a[i][j]): 
			flag = 2 
	return flag

a = [[8, 3, 2, 20], [16, 6, 4.001, 40.02], [4, 1.501, 1, 10.01]] 
n = 3 
flag = 0 
flag = PerformOperation(a, n) 
if (flag == 1): 
	flag = CheckConsistency(a, n, flag) 
print("Final Augmented Matrix is : ") 
PrintMatrix(a, n) 
print() 
PrintResult(a, n, flag)
```
Final Augmented Matrix is : 
8.0 0.0 0.0 -49.999999999995566 
0.0 0.0009999999999998899 0.0 0.009999999999999787 
0.0 0.0 0.001000000000000334 0.020000000000003126 

Result is : -6.249999999999446 10.000000000000888 19.999999999996447

So **Gauss-Jordan** elimination is accurate but computationally expensive, especially for large matrices. **Gauss-Seidel iteration** may converge faster for certain matrices, but its accuracy and convergence behavior depend on the matrix structure.

# Problem 5.6
```python
import numpy as np
import matplotlib.pyplot as plt
forces = np.array([9, 18, 27])
lengths = np.array([19.31, 22.1, 26.42])
displacements = lengths - 15.5
A = np.vstack([displacements, np.ones(len(displacements))]).T
k, a = np.linalg.lstsq(A, forces, rcond=None)[0]
plt.scatter(displacements, forces, label='Data points')
plt.plot(displacements, k * displacements + a, 'r', label='Linear fit: y ={:.2f}x + {:.2f}'.format(k, a))
plt.xlabel('Displacement (cm)')
plt.ylabel('Force (N)')
plt.title('Linear Fit for Spring Constant')
plt.legend()
plt.grid(True)
plt.show()
print("Spring constant k =", k, "N/cm")
```
Spring constant k = 2.4931622133389424 N/cm

![[NA5_6.png]]

# Problem 5.7
### a)  Find the quadratic least square data fit. Plot the data together with fitting parabola.
```python
import numpy as np
import matplotlib.pyplot as plt
x = np.array([395.1, 448.1, 517.7, 583.3, 790.2])
y = np.array([171.0, 289.0, 399.0, 464.0, 620.0])
A = np.vstack([x**2, x, np.ones(len(x))]).T
a, b, c = np.linalg.lstsq(A, y, rcond=None)[0]
x_fit = np.linspace(min(x), max(x), 100)
y_fit = a * x_fit**2 + b * x_fit + c
plt.scatter(x, y, label='Data points')
plt.plot(x_fit, y_fit, 'r', label='Quadratic fit: $y = {:.2f}x^2 + {:.2f}x +{:.2f}$'.format(a, b, c))
plt.xlabel('x')
plt.ylabel('y')
plt.title('Quadratic Least Squares Fit')
plt.legend()
plt.grid(True)
plt.show()
```

![[NA5_7_a.png]]

### b) Find the cubic least square data fit. Plot the data together with fitting cubic
```python
import numpy as np
import matplotlib.pyplot as plt
x = np.array([395.1, 448.1, 517.7, 583.3, 790.2])
y = np.array([171.0, 289.0, 399.0, 464.0, 620.0])
A = np.vstack([x**2, x, np.ones(len(x))]).T
a, b, c = np.linalg.lstsq(A, y, rcond=None)[0]
x_fit = np.linspace(min(x), max(x), 100)
y_fit = a * x_fit**2 + b * x_fit + c
plt.scatter(x, y, label='Data points')
plt.plot(x_fit, y_fit, 'r', label='Quadratic fit: $y = {:.2f}x^2 + {:.2f}x {:.2f}$'.format(a, b, c))
plt.xlabel('x')
plt.ylabel('y')
plt.title('Quadratic Least Squares Fit')
plt.legend()
plt.grid(True)
plt.show()
```

![[NA5_7_b.png]]

### c) Which one is better?
To determine the better fit between the quadratic and cubic models for the given data, we evaluate their $R^2$ values for goodness of fit, consider the trade-off between model complexity (quadratic having three coefficients and cubic having four), and assess which model aligns more with the nature of the data and underlying phenomenon.