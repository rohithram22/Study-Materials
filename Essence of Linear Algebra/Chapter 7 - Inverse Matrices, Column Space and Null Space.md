
Usefulness of Matrices or Linear Algebra:

It lets us solve systems of equations - Linear system of equations


![[Pasted image 20250812234304.png]]

(Remember we are trying to solve for [x y z])

Matrix A corresponds to some linear transformation - We are looking for a vector x for which after applying the transformation lands on v

So how we think of a solution for the system of equations for example for a 2d case depends on if the Transformation associated with A
1.  squishes all of space to a lower dimension (line or a point) (det(A) = 0)
2.  or leaves everything in 2D (det(A) != 0)

Lets see the second case which is mostly the case:

In this case there will only one vector (one solution) that lands on v. This can be found by playing the transformation in reverse.(A inverse)

A inverse 
for example if A is the 90 degree counterclockwise rotation then A inverse is 90 degree clockwise rotation

It has a property where you first apply A transformation and then follow it with the inverse transformation of A then we end up where we started.

![[Pasted image 20250812235740.png]]

The transformation that does nothing is called the identity transformation or matrix

![[Pasted image 20250812235843.png]]

Once you have the inverse matrix you can solve this equation by multiplying the inverse matrix by v

if det(A) != 0 then there is a A inverse

For the first case when det(A) is zero: that is it squishes space to one dimension - there is no inverse. *You cannot unsquish a line to turn i into plane.* A function cannot do that. Function can only take a single input to a single output (while converting a line to plane requires one vector to convert to multiple lines).

When output of transformation is a line / one dimensional we say it has the rank of one. If all vectors land on 2d plane - rank of 2 .
rank <-> number of dimensions in the output.
(for a 3 x 3 matrices Rank 2 means we collapsed)
Set of all possible outputs of a matrix is called a **column space** of a matrix.

The columns of your matrix tells you where the basis vector lands - 
Column Space <=> Span of columns 

Rank - Number of dimensions in the column space.

When this rank is high as it can be - full rank (equals the number of columns)

Zero Vector ([0 0]) is always in the column space (origin)
For a full rank only zero vector will land on itself 




For matrices that aren't full rank (squished to a smaller dimension) - there are bunch of vectors that land on zero.
If 2d transformation squishes space on to a line there is a separate line in a different direction full of vectors that land on the origin
If a 3d transformation squishes space onto a plane there is full line of vectors that land on a origin  
If a 3d transformation squishes all of space onto a line there is a plane full of vectors that land on the origin  
this set of vectors that land on the origin is called the null space or kernel of the matrix
the space of all vectors that become null - they become zero vector



The null space (or kernel) of a matrix is the set of all vectors that, when transformed by that matrix, land on the **zero vector** (the origin). In other words, if you have a transformation A, the null space consists of all vectors 'x' such that A * x = 0.

The video explains that for a transformation that is not "full rank" (meaning it squishes space into a lower dimension), there will be more than just the zero vector itself that lands on the origin .

For example:

- If a 2D transformation squishes a plane onto a line, there will be a line of vectors that all get transformed into the origin.
- If a 3D transformation squishes space onto a plane, there's a line of vectors that land on the origin.
- If a 3D transformation squishes space onto a line, there's a whole plane of vectors that land on the origin .

In the context of solving a linear system of equations Ax = V, if V is the zero vector (Ax = 0), then the null space gives you all the possible solutions to that specific equation 



The null space helps us understand the solutions to a specific type of linear system: **Ax = 0**, where '0' is the zero vector.

Here's the main use:

- **Finding all solutions to homogeneous systems**: If you have a system of linear equations where all the constant terms on the right side are zero (e.g., 2x + 3y = 0, 4x - y = 0), then the set of all possible vectors 'x' that satisfy this system forms the null space of matrix 'A'.

Think of it like this: If a machine transforms certain inputs into nothing (zero output), the null space tells you _all_ the inputs that would result in nothing. This is crucial in many fields like engineering, computer graphics, and data science for understanding the inherent properties of a system or transformation.

#nullspace #inverse #matrices #lineartransformations #columnspaces

