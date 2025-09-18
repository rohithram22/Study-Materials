
## Overview

The cross product is a binary operation on two vectors in 3D space that produces a vector perpendicular to both input vectors. This note explores both the computational and geometric understanding of the cross product through the lens of [[Linear Transformations]] and [[Duality]].

## Prerequisites

- [[Chapter 6 - The Determinant]]
- [[Chapter 9 - Dot Products and Duality]]
- [[Chapter 3 - Linear Transformations and Matrices]]

## Computational Method

### Matrix Form

To compute $\vec{v} \times \vec{w}$:

1. Create a 3×3 matrix with:
    
    - First column: basis vectors $\hat{i}, \hat{j}, \hat{k}$ (treated as symbols)
    - Second column: coordinates of $\vec{v}$
    - Third column: coordinates of $\vec{w}$
2. Compute the determinant: $$\vec{v} \times \vec{w} = \begin{vmatrix} \hat{i} & v_1 & w_1 \ \hat{j} & v_2 & w_2 \ \hat{k} & v_3 & w_3 \end{vmatrix}$$
    
3. Result: $a\hat{i} + b\hat{j} + c\hat{k}$ where $a$, $b$, $c$ are the coordinates of the resulting vector
    

## Geometric Properties

The cross product $\vec{v} \times \vec{w}$ has three key geometric properties:

1. **Magnitude**: $|\vec{v} \times \vec{w}| =$ area of parallelogram defined by $\vec{v}$ and $\vec{w}$
2. **Direction**: Perpendicular to both $\vec{v}$ and $\vec{w}$
3. **Orientation**: Follows the [[Right-Hand Rule]]

## Connection to 2D Cross Product

### 2D Version

In 2D, the "cross product" is actually a scalar:

- Compute determinant of 2×2 matrix with $\vec{v}$ and $\vec{w}$ as columns
- Result: signed area of parallelogram
- Sign depends on orientation of vectors

## The Duality Perspective

### Key Insight

The cross product can be understood through [[Duality]] between linear transformations and vectors.

### Process

1. **Define a linear transformation** $T: \mathbb{R}^3 \to \mathbb{R}$
    
    - Input: vector $(x, y, z)$
    - Output: determinant of matrix with columns $(x,y,z)$, $\vec{v}$, $\vec{w}$
    - Geometrically: signed volume of parallelepiped
2. **Find the dual vector** $\vec{p}$
    
    - The unique vector where $T(\vec{x}) = \vec{p} \cdot \vec{x}$
    - This dual vector IS the cross product $\vec{v} \times \vec{w}$

## Deep Dive: The Linear Transformation

### Definition

Given fixed vectors $\vec{v}$ and $\vec{w}$, define: $$f(x, y, z) = \det\begin{pmatrix} x & v_1 & w_1 \ y & v_2 & w_2 \ z & v_3 & w_3 \end{pmatrix}$$

### Properties

- **Linear**: $f$ is a linear transformation (follows from determinant properties)
- **Geometric meaning**: Returns signed volume of parallelepiped formed by $(x,y,z)$, $\vec{v}$, $\vec{w}$

## Finding the Dual Vector

### Computational Approach

The dual vector $\vec{p}$ must satisfy: $$\vec{p} \cdot (x, y, z) = \det\begin{pmatrix} x & v_1 & w_1 \ y & v_2 & w_2 \ z & v_3 & w_3 \end{pmatrix}$$

Expanding the determinant and matching coefficients gives us the coordinates of $\vec{p}$.

### Geometric Approach

The dual vector $\vec{p}$ must:

1. Be perpendicular to both $\vec{v}$ and $\vec{w}$
2. Have length equal to area of parallelogram spanned by $\vec{v}$ and $\vec{w}$
3. Point in direction satisfying the right-hand rule

## Volume Interpretation

### Parallelepiped Volume

The volume can be computed as:

- Base area: $|\vec{v} \times \vec{w}|$ (parallelogram area)
- Height: component of third vector perpendicular to base
- Result: $|(\vec{v} \times \vec{w}) \cdot \vec{x}|$

This explains why the cross product gives us exactly the vector we need!

## Why This Matters

### Unification

Both computational and geometric approaches yield the same vector because:

- They're finding the dual vector of the same linear transformation
- The transformation encodes the geometric relationship between the vectors

### Key Takeaway

The "trick" of using $\hat{i}, \hat{j}, \hat{k}$ in the determinant isn't arbitrary—it's a computational shortcut for finding the dual vector that encodes the geometric properties we want.

## Summary Diagram

```
Linear Transformation T
       ↓
[3D space] → [Real numbers]
(x,y,z) ↦ det(x,y,z | v | w)
       ↓
   Dual Vector
       ↓
  v × w (Cross Product)
```

## Related Concepts

- [[Determinants]] - Foundation for volume calculations
- [[Duality]] - Bridge between transformations and vectors
- [[Dot Product]] - Used in the dual relationship
- [[Right-Hand Rule]] - Determines orientation
- [[Linear Transformations]] - Framework for understanding
- [[Matrix Multiplication]] - Computational tool

## Applications

- Physics: [[Torque]], [[Angular Momentum]]
- Computer Graphics: [[Normal Vectors]], [[Surface Orientation]]
- Engineering: [[Moment of Force]]

## Practice Problems

1. Verify that the function $f(x,y,z) = \det(x,y,z | v | w)$ is linear
2. Show geometrically why $\vec{v} \times \vec{w}$ is perpendicular to both vectors
3. Prove that $|\vec{v} \times \vec{w}| = |\vec{v}||\vec{w}|\sin\theta$

## Tags

#linear-algebra #cross-product #duality #determinants #3D-geometry #vector-operations