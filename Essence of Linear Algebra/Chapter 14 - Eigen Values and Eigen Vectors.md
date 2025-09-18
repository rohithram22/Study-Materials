

## Overview

Eigenvectors and eigenvalues represent special vectors that remain on their own span during a linear transformation, only being scaled (stretched or squished) rather than rotated.

## Prerequisites for Understanding

- **Linear Transformations**: How matrices transform space
- **Determinants**: When matrices squish space to lower dimensions
- **Linear Systems of Equations**: Solving systems of equations
- **Change of Basis**: Switching coordinate systems

---

## Core Concepts

### Eigenvector Definition

- **Eigenvector**: A special vector that remains on its own span during a transformation
- The transformation only stretches or squishes it like a scalar
- Does not get rotated off its line
- Any other vector on the same line (span) is also just scaled by the same factor

### Eigenvalue Definition

- **Eigenvalue**: The factor by which an eigenvector is stretched or squished
- Can be positive (stretching in same direction)
- Can be negative (flipping and scaling)
- Can be 1 (no scaling, like in rotations)
- Can be 0 (collapse to origin)

### Mathematical Representation

$$Av = \lambda v$$

Where:

- $A$ = matrix representing the transformation
- $v$ = eigenvector
- $\lambda$ = eigenvalue

This means: The matrix-vector product $Av$ gives the same result as scaling the eigenvector $v$ by $\lambda$.

---

## Visual Understanding

### Example: 2D Transformation

Matrix: $\begin{bmatrix} 3 & 1 \ 0 & 2 \end{bmatrix}$

- **First eigenvector**: $\hat{i}$ (basis vector)
    - Eigenvalue: 3
    - Stays on x-axis, stretched by factor of 3
- **Second eigenvector**: $\begin{bmatrix} -1 \ 1 \end{bmatrix}$
    - Eigenvalue: 2
    - Stays on diagonal line, stretched by factor of 2

### 3D Rotation Example

- Eigenvector = axis of rotation
- Eigenvalue = 1 (no stretching in rotation)
- Makes 3D rotations easier to understand than full 3×3 matrix

---

## Computing Eigenvalues

### The Core Equation

Starting from: $Av = \lambda v$

We need to find values of $\lambda$ that allow non-zero solutions for $v$.

### Step-by-Step Process

#### 1. Rewrite the Equation

$$Av = \lambda v$$ $$Av = \lambda I v$$ (where $I$ is the identity matrix) $$Av - \lambda I v = 0$$ $$(A - \lambda I)v = 0$$

#### 2. Key Insight

For a non-zero vector $v$ to satisfy $(A - \lambda I)v = 0$:

- The matrix $(A - \lambda I)$ must squish space into a lower dimension
- This happens when $\det(A - \lambda I) = 0$

#### 3. Finding Eigenvalues

1. Subtract $\lambda$ from each diagonal entry of $A$
2. Calculate the determinant of $(A - \lambda I)$
3. Set the determinant equal to zero
4. Solve for $\lambda$

### Example Calculation

Given matrix: $A = \begin{bmatrix} 3 & 1 \ 0 & 2 \end{bmatrix}$

**Step 1: Form $(A - \lambda I)$** $$A - \lambda I = \begin{bmatrix} 3-\lambda & 1 \ 0 & 2-\lambda \end{bmatrix}$$

**Step 2: Calculate Determinant** $$\det(A - \lambda I) = (3-\lambda)(2-\lambda) - (1)(0) = (3-\lambda)(2-\lambda)$$

**Step 3: Set Equal to Zero** $$(3-\lambda)(2-\lambda) = 0$$

**Step 4: Solve** $$\lambda = 2 \text{ or } \lambda = 3$$

### The Characteristic Polynomial

- The determinant $\det(A - \lambda I)$ gives a polynomial in $\lambda$
- Called the **characteristic polynomial**
- Degree equals the dimension of the matrix
- Roots are the eigenvalues

---

## Computing Eigenvectors

### Process Overview

Once you have an eigenvalue $\lambda$, find the corresponding eigenvector(s) by solving: $$(A - \lambda I)v = 0$$

### Example: Finding Eigenvectors

Given matrix: $A = \begin{bmatrix} 3 & 1 \ 0 & 2 \end{bmatrix}$ with eigenvalues $\lambda_1 = 2$ and $\lambda_2 = 3$

#### Finding Eigenvectors for $\lambda = 2$

**Step 1: Form $(A - 2I)$** $$A - 2I = \begin{bmatrix} 3-2 & 1 \ 0 & 2-2 \end{bmatrix} = \begin{bmatrix} 1 & 1 \ 0 & 0 \end{bmatrix}$$

**Step 2: Solve $(A - 2I)v = 0$** $$\begin{bmatrix} 1 & 1 \ 0 & 0 \end{bmatrix} \begin{bmatrix} x \ y \end{bmatrix} = \begin{bmatrix} 0 \ 0 \end{bmatrix}$$

This gives us: $x + y = 0$, so $y = -x$

**Step 3: General Solution** $$v = \begin{bmatrix} x \ -x \end{bmatrix} = x\begin{bmatrix} 1 \ -1 \end{bmatrix}$$

Eigenvector: Any non-zero scalar multiple of $\begin{bmatrix} 1 \ -1 \end{bmatrix}$

#### Finding Eigenvectors for $\lambda = 3$

**Step 1: Form $(A - 3I)$** $$A - 3I = \begin{bmatrix} 0 & 1 \ 0 & -1 \end{bmatrix}$$

**Step 2: Solve $(A - 3I)v = 0$** This gives us: $y = 0$, $x$ is free

**Step 3: General Solution** $$v = \begin{bmatrix} x \ 0 \end{bmatrix} = x\begin{bmatrix} 1 \ 0 \end{bmatrix}$$

Eigenvector: Any non-zero scalar multiple of $\begin{bmatrix} 1 \ 0 \end{bmatrix}$ (which is $\hat{i}$)

### Eigenspaces

- All eigenvectors for a given eigenvalue form a subspace
- This subspace is called the **eigenspace** for that eigenvalue
- Includes the zero vector (though zero vector isn't technically an eigenvector)

---

## Special Cases and Examples

### Transformations Without Real Eigenvectors

#### 90-Degree Rotation

Matrix: $\begin{bmatrix} 0 & -1 \ 1 & 0 \end{bmatrix}$

- Rotates every vector 90 degrees
- No vector stays on its span
- Characteristic polynomial: $\lambda^2 + 1 = 0$
- Eigenvalues: $\lambda = i, -i$ (imaginary)
- **No real eigenvectors exist**

### Shear Transformation

#### Horizontal Shear

Matrix: $\begin{bmatrix} 1 & 1 \ 0 & 1 \end{bmatrix}$

- Fixes $\hat{i}$ in place, moves $\hat{j}$ one unit right
- All x-axis vectors are eigenvectors with $\lambda = 1$
- These are the **only** eigenvectors
- Characteristic Polynomial: $(1-\lambda)^2 = 0$ (double root at $\lambda = 1$)
- Only one-dimensional eigenspace despite repeated eigenvalue

### Uniform Scaling

#### Scale by Factor of 2

Matrix: $\begin{bmatrix} 2 & 0 \ 0 & 2 \end{bmatrix}$

- **Every vector** is an eigenvector
- Single eigenvalue: $\lambda = 2$
- Entire plane is the eigenspace
- Already diagonal - it's its own eigenbasis!

---

## Eigenbasis

### Definition

An **eigenbasis** is a set of basis vectors that are also eigenvectors of a transformation.

### Why Eigenbases Matter

#### The Power of Diagonal Matrices

When basis vectors are eigenvectors:

- The transformation matrix becomes **diagonal**
- Diagonal entries are the eigenvalues
- All other entries are zero

Example: $$\begin{bmatrix} \lambda_1 & 0 \ 0 & \lambda_2 \end{bmatrix}$$

#### Computational Benefits

Computing powers becomes trivial:

- $A^{100}$ in standard basis: nightmare of computation
- $D^{100}$ in eigenbasis: just raise diagonal entries to 100th power

$$D^n = \begin{bmatrix} \lambda_1^n & 0 \ 0 & \lambda_2^n \end{bmatrix}$$

### Process: Using an Eigenbasis

#### 1. Find All Eigenvectors

- Compute eigenvalues
- Find corresponding eigenvectors
- Need $n$ linearly independent eigenvectors for $n$-dimensional space

#### 2. Create Change of Basis Matrix

Form matrix $P$ with eigenvectors as columns: $$P = \begin{bmatrix} | & | \ v_1 & v_2 \ | & | \end{bmatrix}$$

#### 3. Transform to Eigenbasis

The transformation in the new basis: $$D = P^{-1}AP$$

Where $D$ is diagonal with eigenvalues on the diagonal

#### 4. Work in Eigenbasis

Perform operations (especially powers) on diagonal matrix

#### 5. Transform Back

Convert result back to standard basis: $$A^n = PD^nP^{-1}$$

### Example: Computing High Powers

**Problem**: Find $A^{100}$ where $A = \begin{bmatrix} 3 & 1 \ 0 & 2 \end{bmatrix}$

**Solution Using Eigenbasis**:

1. **Eigenvectors** (from previous calculations):
    
    - $v_1 = \begin{bmatrix} 1 \ 0 \end{bmatrix}$ with $\lambda_1 = 3$
    - $v_2 = \begin{bmatrix} 1 \ -1 \end{bmatrix}$ with $\lambda_2 = 2$
2. **Change of basis matrix**: $$P = \begin{bmatrix} 1 & 1 \ 0 & -1 \end{bmatrix}$$
    
3. **Diagonal form**: $$D = \begin{bmatrix} 3 & 0 \ 0 & 2 \end{bmatrix}$$
    
4. **Compute power**: $$D^{100} = \begin{bmatrix} 3^{100} & 0 \ 0 & 2^{100} \end{bmatrix}$$
    
5. **Transform back**: $$A^{100} = PD^{100}P^{-1}$$
    

### Limitations

Not all transformations have enough eigenvectors:

- **Shear transformations**: Only one line of eigenvectors
- **Rotations** (except 180°): No real eigenvectors in 2D

A matrix is **diagonalizable** if and only if it has an eigenbasis.

---

## Summary Table of Special Cases

|Transformation|Real Eigenvalues?|Full Eigenbasis?|Special Property|
|---|---|---|---|
|90° Rotation|No|No|Complex eigenvalues only|
|Shear|Yes|No|Deficient eigenspace|
|Uniform Scale|Yes|Yes|Every vector is eigenvector|
|Reflection|Yes|Yes|Eigenvalues are ±1|
|Projection|Yes|Yes|Has eigenvalue 0|

---

## Key Insights and Applications

### Why Eigenvectors Matter

1. **Simplification**: Understanding transformations through their eigenvectors is often clearer than looking at matrix columns
2. **Coordinate Independence**: Less dependent on particular coordinate systems
3. **Computational Efficiency**: Diagonal matrices make repeated operations much simpler
4. **Reveals Structure**: Shows the "natural" directions of a transformation

### Connection to Transformations

- Eigenvalue = 0: Transformation collapses a dimension
- Eigenvalue = 1: Points stay fixed in that direction
- Eigenvalue > 1: Stretching
- 0 < Eigenvalue < 1: Compression
- Eigenvalue < 0: Flipping and scaling

### Real-World Applications

1. **Principal Component Analysis (PCA)** - data analysis
2. **Google's PageRank algorithm** - web search
3. **Quantum mechanics** - eigenstates
4. **Vibration analysis** - engineering
5. **Facial recognition** - computer vision
6. **Differential equations** - physics and engineering

---

## Key Takeaways

1. **Eigenvectors** point in directions that don't change during transformation (only scaled)
2. **Eigenvalues** tell you how much scaling happens
3. Not all matrices have real eigenvectors (rotations)
4. Not all matrices are diagonalizable (shears)
5. When you can find an eigenbasis, computations become much simpler
6. The characteristic polynomial $\det(A - \lambda I) = 0$ is the key to finding eigenvalues
7. Eigenvectors form subspaces (eigenspaces) for each eigenvalue
8. Understanding eigenvectors requires solid foundation in determinants and linear systems

---

Tags: #linear-algebra #eigenvectors #eigenvalues #transformations #matrices #diagonal-matrices #computation 