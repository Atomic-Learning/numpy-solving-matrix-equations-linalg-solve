The NumPy function [`numpy.linalg.solve()`](https://numpy.org/doc/stable/reference/generated/numpy.linalg.solve.html) is used to solve matrix equations of the form `Ax = b`, where `A` is a square matrix and `b` is a vector or matrix of the same dimension. It receives two arguments:

- `a`: The square matrix representing the coefficients of the system of equations.
- `b`: The vector or matrix representing the right-hand side of the equation.

# Example

We want to solve the matrix equation:

$$
\begin{bmatrix}
\1 & 2 \\
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

```python
import numpy as np

matrix = np.array([[1, 2], [3, 4]])
rhs = np.array([5, 11])

x = np.linalg.solve(matrix, rhs)
print(x)
```