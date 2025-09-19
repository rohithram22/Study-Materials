

#linear-algebra #eigenvalues #matrices #computation-tricks #quantum-mechanics

## Core Concepts

### Definition Recap

- **Eigenvector**: A vector that is only scaled (not rotated) by a linear transformation
- **Eigenvalue** (λ): The scaling factor applied to the eigenvector
- **Equation form**: If $Av = \lambda v$, then $(A - \lambda I)v = 0$
- **Key implication**: $\det(A - \lambda I) = 0$

### Traditional Method (Review)

1. Subtract λ from diagonal entries: $A - \lambda I$
2. Set determinant to zero: $\det(A - \lambda I) = 0$
3. Expand to get characteristic polynomial
4. Apply quadratic formula to find roots
5. Roots = eigenvalues

## The Quick Trick for 2×2 Matrices

### Three Key Facts

#### Fact 1: Trace-Eigenvalue Relationship

- **Trace** = sum of diagonal entries = sum of eigenvalues
- $\text{trace}(A) = a_{11} + a_{22} = \lambda_1 + \lambda_2$
- **Mean of eigenvalues** = Mean of diagonal entries
- $\frac{\lambda_1 + \lambda_2}{2} = \frac{a_{11} + a_{22}}{2}$

#### Fact 2: Determinant-Eigenvalue Relationship

- **Determinant** = product of eigenvalues
- $\det(A) = \lambda_1 \cdot \lambda_2$
- Physical interpretation: eigenvalues show stretching in specific directions, determinant shows overall area/volume scaling

#### Fact 3: The Mean-Product Formula

- Given mean $m$ and product $p$ of two numbers:
- **The two numbers are**: $m \pm \sqrt{m^2 - p}$
- Derivation: If numbers are $m+d$ and $m-d$:
    - Product: $(m+d)(m-d) = m^2 - d^2 = p$
    - Therefore: $d = \sqrt{m^2 - p}$

### The Complete Formula

For a 2×2 matrix, eigenvalues are:

$$\lambda = m \pm \sqrt{m^2 - p}$$

Where:

- $m$ = mean of diagonal entries
- $p$ = determinant of matrix

**Mnemonic** (by A Capella Science): _"m plus or minus square root of m squared minus p"_

## Examples

### Example 1: Basic Application

Matrix: $\begin{pmatrix} 3 & 1 \ 4 & 1 \end{pmatrix}$

1. Mean of diagonals: $m = \frac{3+1}{2} = 2$
2. Determinant: $p = (3)(1) - (1)(4) = -1$
3. Eigenvalues: $2 \pm \sqrt{4 - (-1)} = 2 \pm \sqrt{5}$

### Example 2: Clean Solution

Matrix: $\begin{pmatrix} 2 & 7 \ 1 & 8 \end{pmatrix}$

1. Mean: $m = \frac{2+8}{2} = 5$
2. Determinant: $p = (2)(8) - (7)(1) = 9$
3. Eigenvalues: $5 \pm \sqrt{25 - 9} = 5 \pm 4 = {9, 1}$

### Example 3: Quantum Mechanics - Pauli Spin Matrices

#### Pauli-X Matrix

$\sigma_x = \begin{pmatrix} 0 & 1 \ 1 & 0 \end{pmatrix}$

- Mean: $m = 0$
- Determinant: $p = -1$
- Eigenvalues: $\pm 1$

#### Pauli-Y Matrix

$\sigma_y = \begin{pmatrix} 0 & -i \ i & 0 \end{pmatrix}$

- Mean: $m = 0$
- Determinant: $p = -1$
- Eigenvalues: $\pm 1$

#### Pauli-Z Matrix

$\sigma_z = \begin{pmatrix} 1 & 0 \ 0 & -1 \end{pmatrix}$

- Mean: $m = 0$
- Determinant: $p = -1$
- Eigenvalues: $\pm 1$

**Physical meaning**: Eigenvalues $\pm 1$ represent spin measurements being entirely in one direction or the opposite.

### Example 4: Linear Combination of Pauli Matrices

General spin observation in direction $(a, b, c)$: $$M = a\sigma_x + b\sigma_y + c\sigma_z$$

Where $a^2 + b^2 + c^2 = 1$ (normalized)

- Mean remains 0
- Product remains -1
- Eigenvalues: always $\pm 1$

## Relationship to Characteristic Polynomial

The mean-product formula is essentially solving the quadratic:

For normalized polynomial: $\lambda^2 + b\lambda + c = 0$

- Mean of roots = $-\frac{b}{2}$
- Product of roots = $c$

This shows the quick trick is really just an efficient way to apply the quadratic formula when you can read the mean and product directly from the matrix.

## When to Use This Method

### ✅ Best For:

- Quick mental calculations with 2×2 matrices
- Sketching examples in notes
- Avoiding intermediate polynomial setup
- Matrices where trace and determinant are easy to compute

### ⚠️ Consider Traditional Method When:

- Matrix is already diagonal
- Characteristic polynomial is immediately obvious
- Working with matrices larger than 2×2

## Key Takeaways

1. **Read directly from matrix**: No need to set up characteristic polynomial
2. **Two simple calculations**: Just find mean of diagonals and determinant
3. **One formula to remember**: $m \pm \sqrt{m^2 - p}$
4. **Carries semantic meaning**: Each term has direct matrix interpretation
5. **Particularly useful** for quantum mechanics and quick computations
