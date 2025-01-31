# PyPoSolver

**PyPoSolver** is a Python library for performing mathematical and physics calculations, including numerical integration, root-finding, linear algebra operations, and basic mechanics.

## Installation

```bash
pip install pyposolver 
```

## Usage

### Mathematics

#### Integration

Use the `trapezoidal_rule` function to perform numerical integration:

```python
from pyposolver.maths.integration import trapezoidal_rule

def f(x):
    return x**2

result = trapezoidal_rule(f, 0, 1, 100)  # Integrate f(x) from 0 to 1 using 100 intervals
print(result)  # Expected: 0.333...
```

#### Root-Finding

- **Bisection Method**

Use `bisection_method` to find the root of a function within a specified interval:

```python
from pyposolver.maths.root_finding import bisection_method

def f(x):
    return x**2 - 4

root = bisection_method(f, 0, 3)  # Find root of f(x) in the interval [0, 3]
print(root)  # Expected: 2.0
```

- **Newton-Raphson Method**

Use `newton_raphson_method` for root-finding with an initial guess and the function's derivative:

```python
from pyposolver.maths.root_finding import newton_raphson_method

def f(x):
    return x**3 - 2*x - 5

def df(x):
    return 3*x**2 - 2

root = newton_raphson_method(f, df, 2)  # Initial guess: 2
print(root)  # Expected: 2.094...
```

#### Linear Algebra

- **Dot Product**

Calculate the dot product of two vectors:

```python
from pyposolver.maths.linear_algebra import dot_product

vector1 = [1, 2, 3]
vector2 = [4, 5, 6]

result = dot_product(vector1, vector2)
print(result)  # Expected: 32
```

- **Cross Product**

Compute the cross product of two 3D vectors:

```python
from pyposolver.maths.linear_algebra import cross_product

vector1 = [1, 2, 3]
vector2 = [4, 5, 6]

result = cross_product(vector1, vector2)
print(result)  # Expected: [-3, 6, -3]
```

- **Matrix Multiplication**

Multiply two matrices:

```python
from pyposolver.maths.linear_algebra import matrix_multiply

matrix1 = [[1, 2], [3, 4]]
matrix2 = [[5, 6], [7, 8]]

result = matrix_multiply(matrix1, matrix2)
print(result)  # Expected: [[19, 22], [43, 50]]
```

### Physics

- **Velocity**

Calculate velocity given initial velocity, acceleration, and time:

```python
from pyposolver.physics.mechanics import velocity

initial_velocity = 5
acceleration = 2
time = 3

result = velocity(initial_velocity, acceleration, time)
print(result)  # Expected: 11
```

- **Force**

Calculate force using mass and acceleration:

```python
from pyposolver.physics.mechanics import force

mass = 10
acceleration = 5

result = force(mass, acceleration)
print(result)  # Expected: 50
```