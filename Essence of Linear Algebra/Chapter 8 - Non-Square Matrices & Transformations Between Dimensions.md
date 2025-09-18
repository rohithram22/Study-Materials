
## Overview

- Previous focus: **square matrices** (2×2 for 2D→2D, 3×3 for 3D→3D)
- This note: **non-square matrices** representing transformations between different dimensions

## Core Principle of Linear Transformations

> [!important] Linearity Requirements For transformations between dimensions to be linear:
> 
> 1. **Gridlines remain parallel and evenly spaced**
> 2. **Origin maps to the origin**

---

## 3×2 Matrix: 2D → 3D Transformation

### Geometric Interpretation

- **Input space**: 2D vectors
- **Output space**: 3D vectors
- ==2D inputs and 3D outputs live in completely separate, unconnected spaces==

### Matrix Structure

```
[a  b]  ← 2 columns (2D input)
[c  d]
[e  f]  ← 3 rows (3D output)
```

### Example

Given transformation:

- $\hat{i} \rightarrow \begin{bmatrix} 2 \ -1 \ -2 \end{bmatrix}$
- $\hat{j} \rightarrow \begin{bmatrix} 0 \ 1 \ 1 \end{bmatrix}$

**Resulting Matrix**: $$\begin{bmatrix} 2 & 0 \ -1 & 1 \ -2 & 1 \end{bmatrix}$$

> [!note] Column Space
> 
> - The column space is a **2D plane** slicing through the origin of 3D space
> - Matrix is **full rank** since column space dimension = input space dimension = 2

---

## 2×3 Matrix: 3D → 2D Transformation

### Matrix Structure

```
[a  b  c]  ← 3 columns (3D input)
[d  e  f]  ← 2 rows (2D output)
```

### Interpretation

- **3 columns** → Starting with 3 basis vectors (3D space)
- **2 rows** → Landing spots use only 2 coordinates (2D plane)
- Transformation from 3D space onto 2D plane

> [!warning] Dimensional Reduction This transformation "squishes" 3D space onto a 2D plane - described as feeling "very uncomfortable" if you imagine going through it

---

## 1×2 Matrix: 2D → 1D Transformation

### Special Properties

- **Input**: 2D vectors
- **Output**: Single numbers (1D = number line)

### Matrix Structure

```
[a  b]  ← Single row matrix
```

- Each column = where each basis vector lands on the number line

### Visualizing Linearity in 1D

> [!tip] Visual Understanding Instead of gridlines, imagine **evenly spaced dots**:
> 
> - Before: Evenly spaced dots in 2D
> - After: Dots remain evenly spaced on the number line

### Connection to Dot Product

- [[Dot Product|This transformation type has close ties to the dot product]]
- To be explored in next video

---

## Quick Reference

| Matrix Size | Transformation | Description               |
| ----------- | -------------- | ------------------------- |
| **3×2**     | 2D → 3D        | Maps plane to 3D space    |
| **2×3**     | 3D → 2D        | Squishes 3D to plane      |
| **1×2**     | 2D → 1D        | Maps plane to number line |
| **2×1**     | 1D → 2D        | Maps line to plane        |

> [!summary] Key Insight **Matrix dimensions tell the transformation story:**
> 
> - **Rows** = Output dimension
> - **Columns** = Input dimension



---

#linear-algebra #matrices #transformations #3blue1brown