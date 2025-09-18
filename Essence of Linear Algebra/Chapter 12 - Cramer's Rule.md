
Cramer's rule is not the best way to calculate solutions for linear system of equations. Gaussian Elimination is faster.


Cramer's Rule is a method for solving Linear Systems of Equations using Determinants. While not the most computationally efficient method (Gaussian Elimination is faster), it provides deep geometric insight into how linear systems work and beautifully connects determinants with linear transformations.



## The Problem Setup

### Linear System

Given a system with unknowns $x$ and $y$: $$A\vec{v} = \vec{b}$$

Where:

- $A$ is a known transformation matrix
- $\vec{v} = \begin{pmatrix} x \ y \end{pmatrix}$ is the unknown input vector
- $\vec{b}$ is the known output vector

### Geometric Interpretation

- The columns of matrix $A$ show where basis vectors land after transformation
- We're solving: "Which input vector $\vec{v}$ gets transformed to output $\vec{b}$?"
- This is finding the linear combination: $x \cdot \text{(column 1)} + y \cdot \text{(column 2)} = \vec{b}$

## Important Constraint

**Non-zero determinant required**: $\det(A) \neq 0$

- Ensures transformation doesn't collapse space
- Guarantees unique solution (one input → one output)
- If $\det(A) = 0$: either no solution or infinitely many solutions

## Why Dot Products Don't Work

### The Failed Approach

Initially, you might hope:

- $x$ = dot product of output with transformed $\hat{i}$
- $y$ = dot product of output with transformed $\hat{j}$

### Why It Fails

Most linear transformations **don't preserve dot products**:

- Vectors pointing same direction can be pulled apart
- Perpendicular vectors may not stay perpendicular
- Dot products typically change (often increase due to stretching)

### Exception: Orthonormal Transformations

Special transformations that **DO** preserve dot products:

- Rotations (rigid motion)
- No stretching/squishing
- Basis vectors remain perpendicular with unit length
- For these, the naive dot product method works!

## The Key Insight: Areas as Coordinates

### 2D Coordinates via Areas

#### Y-coordinate

- Form parallelogram with $\hat{i}$ and input vector $(x,y)$
- Area = base (1) × height = $y$
- **Key insight**: Y-coordinate equals signed area of this parallelogram

#### X-coordinate

- Form parallelogram with input vector and $\hat{j}$
- Area = $x$
- X-coordinate equals signed area of this parallelogram

### 3D Extension: Volumes as Coordinates

For a vector $(x,y,z)$:

- **Z-coordinate**: Volume of parallelepiped formed by $\hat{i}$, $\hat{j}$, and the vector
- **X-coordinate**: Volume using $\hat{j}$, $\hat{k}$, and the vector
- **Y-coordinate**: Volume using $\hat{i}$, $\hat{k}$, and the vector

### Sign Convention

- Use Right-Hand Rule for signed volume/area
- Order of vectors matters
- Negative coordinates → negative signed volume

## The Magic: How Areas Transform

### Fundamental Property

Under linear transformation with matrix $A$: $$\text{New Area} = \det(A) \times \text{Original Area}$$

**All areas scale by the same factor: the determinant!**

## Deriving Cramer's Rule

### Finding Y-coordinate

1. **Original parallelogram**:
    
    - Vectors: $\hat{i}$ and $(x,y)$
    - Area = $y$
2. **After transformation**:
    
    - Vectors: first column of $A$ and output $\vec{b}$
    - Area = $\det(A) \times y$
3. **Solve for y**: $$y = \frac{\text{Area of transformed parallelogram}}{\det(A)}$$
    
4. **Compute transformed area**: Create matrix with:
    
    - First column: same as $A$
    - Second column: output vector $\vec{b}$ $$y = \frac{\det\begin{pmatrix} a_{11} & b_1 \ a_{21} & b_2 \end{pmatrix}}{\det(A)}$$

### Finding X-coordinate

Similarly: $$x = \frac{\det\begin{pmatrix} b_1 & a_{12} \ b_2 & a_{22} \end{pmatrix}}{\det(A)}$$

## Cramer's Rule Formula

For system $A\vec{x} = \vec{b}$ where $A = \begin{pmatrix} a_{11} & a_{12} \ a_{21} & a_{22} \end{pmatrix}$:

$$x = \frac{\det(A_x)}{\det(A)}, \quad y = \frac{\det(A_y)}{\det(A)}$$

Where:

- $A_x$ = matrix $A$ with first column replaced by $\vec{b}$
- $A_y$ = matrix $A$ with second column replaced by $\vec{b}$

## Example Calculation

Given system with:

- Matrix determinant: $\det(A) = 2$
- For x: determinant of modified matrix = 6
- For y: determinant of modified matrix = 4

Solution:

- $x = 6/2 = 3$
- $y = 4/2 = 2$

## Higher Dimensions

### 3D Systems

For $A\vec{x} = \vec{b}$ with $\vec{x} = (x,y,z)$:

$$x_i = \frac{\det(A_i)}{\det(A)}$$

Where $A_i$ is matrix $A$ with $i$-th column replaced by $\vec{b}$

### General Pattern

The method generalizes to any dimension:

- Replace column corresponding to variable you're solving for
- Take determinant ratio
- Geometric interpretation: ratios of hypervolumes

## Computational Complexity

### Cramer's Rule

- Requires computing $n+1$ determinants for $n$ variables
- Complexity: $O(n! \cdot n)$ or $O(n^4)$ with better algorithms
- Becomes impractical for large systems

### Better Alternatives

- [[Gaussian Elimination]]: $O(n^3)$
- [[LU Decomposition]]: $O(n^3)$
- Iterative methods for sparse systems

## Why Learn Cramer's Rule?

Despite computational inefficiency:

1. **Theoretical insight**: Shows deep connection between determinants and linear systems
2. **Geometric understanding**: Reveals how transformations affect coordinates
3. **Mathematical beauty**: Elegant relationship between areas/volumes and solutions
4. **Special cases**: Useful for small systems or symbolic computation
5. **Educational value**: Consolidates understanding of linear algebra concepts

## Key Takeaways

1. **Coordinates are areas/volumes**: Can represent coordinates through parallelogram areas
2. **Determinants scale areas uniformly**: All areas scale by $\det(A)$
3. **Solution via ratios**: Solutions are ratios of determinants
4. **Geometric preservation**: Method works because area ratios are preserved


## Practice Problems

1. Solve using Cramer's Rule: $$\begin{cases} 2x + 3y = 7 \ x - y = 1 \end{cases}$$
    
2. Explain geometrically why Cramer's Rule fails when $\det(A) = 0$
    
3. Derive Cramer's Rule for a 3×3 system
    
4. Compare computation time: Cramer's Rule vs Gaussian Elimination for a 4×4 system
    

## Visual Summary

```
Input Space          Transformation          Output Space
-----------          --------------          ------------
     ↓                     ↓                      ↓
Parallelogram  →   Scale by det(A)   →   New Parallelogram
  Area = y                                Area = det(A)·y
     ↓                                           ↓
              y = (New Area) / det(A)
```

## Tags

#linear-algebra #cramers-rule #determinants #linear-systems #geometric-interpretation #computational-methods