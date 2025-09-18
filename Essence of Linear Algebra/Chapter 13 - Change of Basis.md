
## Core Concept

- **Coordinate systems** are ways to translate between vectors and sets of numbers
- Different coordinate systems use different **basis vectors**
- The same vector can have different coordinates in different systems

## Standard Coordinate System

- Uses basis vectors **i-hat** (1,0) and **j-hat** (0,1)
- i-hat: unit vector pointing right
- j-hat: unit vector pointing up
- Any vector is described as a linear combination: `vector = a*i-hat + b*j-hat`
- Coordinates [a,b] represent scalars that scale the basis vectors

## Alternative Coordinate Systems

### Jennifer's System Example

- Different basis vectors: **b1** and **b2**
    - b1 = [2,1] in our system
    - b2 = [-1,1] in our system
- Same vector has different coordinates:
    - Our system: [3,2]
    - Jennifer's system: [5/3, 1/3]
- In her perspective, b1 = [1,0] and b2 = [0,1]

## Translation Between Systems

### From Jennifer's to Ours

1. Create **change of basis matrix**
    - Columns = Jennifer's basis vectors in our coordinates
    - Matrix = `[b1 | b2]` = `[[2,-1],[1,1]]`
2. Multiply matrix by Jennifer's coordinates to get our coordinates
3. This is standard matrix-vector multiplication

### From Ours to Jennifer's

1. Use the **inverse** of the change of basis matrix
2. Multiply inverse matrix by our coordinates
3. Result gives coordinates in Jennifer's system

## Geometric Interpretation

- Change of basis matrix transforms our grid into Jennifer's grid
- Acts as a linear transformation moving our basis vectors to hers
- **Key insight**: Matrix transforms our misconception of what Jennifer means into the actual vector she's referring to

## Transforming Linear Transformations

### Problem

How to represent a transformation (like 90° rotation) in different coordinate systems?

### Solution: Three-Step Process

1. **Change basis**: Translate from Jennifer's language to ours (multiply by A)
2. **Apply transformation**: Use transformation matrix in our system (multiply by M)
3. **Change back**: Translate result back to Jennifer's language (multiply by A⁻¹)

### Formula

- Transformation in Jennifer's system = **A⁻¹ · M · A**
- A = change of basis matrix
- M = transformation in our system
- A⁻¹ = inverse change of basis

### Interpretation

- The expression A⁻¹MA represents "mathematical empathy"
- Middle matrix (M) = transformation as we see it
- Outer matrices (A⁻¹, A) = shift in perspective
- Full product = same transformation from someone else's viewpoint

## Key Takeaways

- Coordinates are relative to choice of basis vectors
- Same vector/transformation looks different in different coordinate systems
- Change of basis matrices allow translation between perspectives
- Understanding this is crucial for eigenvectors and eigenvalues

## Visual Notes

- Space has no intrinsic grid - grids are constructs of coordinate systems
- Origins align across systems (0,0 is universal)
- Different systems have different axis directions and grid spacing

