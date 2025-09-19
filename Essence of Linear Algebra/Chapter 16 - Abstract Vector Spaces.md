

#linear-algebra #vector-spaces #abstract-algebra #functions-as-vectors #linear-transformations

## The Fundamental Question: What Are Vectors?

### Three Perspectives on Vectors

1. **Geometric View**: Arrows on a plane (with coordinates for convenience)
2. **Algebraic View**: Lists of numbers (visualized as arrows for intuition)
3. **Abstract View**: Members of a vector space (manifestations of something deeper)

### The Paradox

- **Concrete approach**: Lists of numbers are clear and unambiguous
    - Makes 4D or 100D vectors seem real and workable
    - Avoids vague hand-waving about higher dimensions
- **Spatial intuition**: Vectors exist independently of coordinates
    - Coordinates are arbitrary (depend on basis choice)
    - Core concepts (determinants, eigenvectors) are coordinate-independent
    - Properties are inherently spatial

## Functions as Vectors

### Why Functions Are Vector-ish

Functions exhibit the two key vector operations:

#### 1. Addition of Functions

- $(f + g)(x) = f(x) + g(x)$
- The sum function evaluated at any input equals the sum of the individual function values
- Analogous to coordinate-wise vector addition
- "Infinitely many coordinates" to deal with

#### 2. Scalar Multiplication

- $(cf)(x) = c \cdot f(x)$
- Scale all outputs by the scalar
- Analogous to coordinate-wise scaling
- Again, like having infinite coordinates

### Linear Transformations on Functions

#### The Derivative as a Linear Transformation

The derivative operator $D$ is a linear transformation because:

1. **Additivity**: $D(f + g) = D(f) + D(g)$
    - Derivative of sum = sum of derivatives
2. **Scaling**: $D(cf) = c \cdot D(f)$
    - Derivative of scaled function = scaled derivative

#### Matrix Representation of the Derivative

For polynomial space with basis ${1, x, x^2, x^3, ...}$:

**Basis functions**:

- $b_0(x) = 1$
- $b_1(x) = x$
- $b_2(x) = x^2$
- $b_3(x) = x^3$
- ...

**Coordinate representation**:

- $x^2 + 3x + 5$ → $[5, 3, 1, 0, 0, ...]$
- $4x^7 - 5x^2$ → $[0, 0, -5, 0, 0, 0, 0, 4, 0, ...]$

**Derivative matrix**:

```
D = [0  1  0  0  0  ...]
    [0  0  2  0  0  ...]
    [0  0  0  3  0  ...]
    [0  0  0  0  4  ...]
    [... ... ... ... ...]
```

The positive integers appear on the super-diagonal!

### Example: Derivative via Matrix Multiplication

For $p(x) = x^3 + 5x^2 + 4x + 5$:

- Coordinates: $[5, 4, 5, 1, 0, ...]$
- After multiplication: $[4, 10, 3, 0, ...]$
- Result: $p'(x) = 3x^2 + 10x + 4$ ✓

## The Abstract Definition of Vector Spaces

### What Makes Something a Vector Space?

A **vector space** is any set of objects with:

1. A sensible notion of **addition**
2. A sensible notion of **scalar multiplication**

That satisfy the eight axioms below.

### The Eight Axioms of Vector Spaces

#### Addition Axioms

1. **Commutativity**: $\vec{u} + \vec{v} = \vec{v} + \vec{u}$
2. **Associativity**: $(\vec{u} + \vec{v}) + \vec{w} = \vec{u} + (\vec{v} + \vec{w})$
3. **Additive identity**: There exists $\vec{0}$ such that $\vec{v} + \vec{0} = \vec{v}$
4. **Additive inverse**: For each $\vec{v}$, there exists $-\vec{v}$ such that $\vec{v} + (-\vec{v}) = \vec{0}$

#### Scalar Multiplication Axioms

5. **Multiplicative identity**: $1 \cdot \vec{v} = \vec{v}$
6. **Associativity**: $(ab)\vec{v} = a(b\vec{v})$

#### Distributive Properties

7. **Distribution over vector addition**: $a(\vec{u} + \vec{v}) = a\vec{u} + a\vec{v}$
8. **Distribution over scalar addition**: $(a + b)\vec{v} = a\vec{v} + b\vec{v}$

### Purpose of Axioms

The axioms serve as:

- **A checklist** for verifying new vector spaces
- **An interface** between mathematicians and users
- **A guarantee** that linear algebra results apply universally

## Examples of Vector Spaces

### Common Vector Spaces

1. **Arrows in $\mathbb{R}^n$** (geometric vectors)
2. **Lists of numbers** ($\mathbb{R}^n$ as coordinate vectors)
3. **Functions** (especially polynomials)
4. **Matrices** (of fixed dimensions)
5. **Sequences**
6. **Solution sets** to homogeneous linear equations

### Verifying a Vector Space

To confirm something is a vector space:

1. Define addition operation
2. Define scalar multiplication
3. Verify all 8 axioms hold
4. Apply all linear algebra results!

## Linear Transformations: The General Definition

### Abstract Definition

A transformation $T$ is **linear** if:

1. **Additivity**: $T(\vec{v} + \vec{w}) = T(\vec{v}) + T(\vec{w})$
2. **Homogeneity**: $T(c\vec{v}) = cT(\vec{v})$

Often stated as: "Linear transformations preserve vector addition and scalar multiplication"

### Why This Definition?

- **General**: Applies to all vector spaces
- **Checkable**: Easy to verify for new spaces
- **Powerful**: Ensures matrix representation exists

### Connection to Geometric Intuition

In $\mathbb{R}^2$, these properties mean:

- Grid lines remain parallel
- Grid lines remain evenly spaced
- Origin stays fixed

## Key Insights and Takeaways

### The Power of Abstraction

1. **Unification**: One theory covers arrows, functions, and more
2. **Generality**: Results apply to any vector space
3. **Discovery**: New vector spaces inherit all known results

### The Learning Path

1. **Start concrete**: Arrows in 2D/3D for intuition
2. **Build understanding**: See patterns and structures
3. **Embrace abstraction**: Apply to broader contexts

### Practical Implications

- **Dot products** → Inner products (for functions)
- **Eigenvectors** → Eigenfunctions (for operators)
- **Matrix multiplication** → General linear transformations

## Philosophy: What IS a Vector?

The mathematician's answer: **"It doesn't matter!"**

Vectors are:

- Not inherently arrows
- Not inherently lists
- Not inherently functions

They are **abstract objects** in a vector space that:

- Can be added
- Can be scaled
- Follow the axioms

This is like asking "What is the number 3?"

- It's not three apples
- It's not three meters
- It's the **abstract concept** of three-ness

## Summary

Vector spaces provide a unified framework where:

- **Concrete intuitions** guide understanding
- **Abstract axioms** ensure generality
- **Linear algebra tools** apply universally

The beauty lies in how geometric intuitions about arrows translate perfectly to functions, polynomials, and beyond through the abstract framework of vector spaces.

---

## Related Topics

- [[Linear Transformations]]
- [[Basis and Dimension]]
- [[Inner Product Spaces]]
- [[Eigenvectors and Eigenvalues]]
- [[Function Spaces]]
- [[Abstract Algebra]]
- [[Polynomial Vector Spaces]]

## Applications

- Quantum mechanics (state vectors)
- Signal processing (function spaces)
- Machine learning (feature spaces)
- Differential equations (solution spaces)
- Computer graphics (transformation matrices)