The NumPy function [`numpy.linalg.solve()`](https://numpy.org/doc/stable/reference/generated/numpy.linalg.solve.html) is used to solve matrix equations of the form $Ax = b$, where $A$ is a square matrix and $b$ is a vector or matrix of the same dimension. It receives two arguments:

- `a`: A two-dimensional NumPy array representing the square matrix of coefficients of the system of equations.
- `b`: A one-dimensional or two-dimensional NumPy array representing the right-hand side of the equation.

# Example

We want to solve the matrix equation:

$$
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix}
=
\begin{bmatrix}
5 \\
11
\end{bmatrix}
$$

To solve the equation we must represent the matrix as a 2-dimensional NumPy array and the vector as a 1-dimensional NumPy array then pass these arrays to the `numpy.linalg.solve()` function.

```py-cell
import numpy as np

matrix = np.array([[1, 2], [3, 4]])
rhs = np.array([5, 11])

x = np.linalg.solve(matrix, rhs)
print(x)
```

# Performance

`numpy.linalg.solve()` is highly optimised for solving the matrix equation and is efficient for a wide range of problems. However, it will not solve the equation in a reasonable amount of time if the matrix is extremely large or ill-suited for the approach it takes. In such cases, an alternative approach may be required.