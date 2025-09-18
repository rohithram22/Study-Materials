

Transformation is a fancy word for function, takes in input and spits out an output.

(take in a vector and spit out a vector)


The word transformation is used instead of function because it wants to signify a movement.

If a transformation takes an input vector to an output vector we imagine the input vector moving to the output vector. 

Transformation is linear if it has two properties

1. All lines must remain lines and not curves
2. The origin must remain fixed in place


You should think of linear transformation keeping grid lines as *parallel and evenly spaced*

Eg: rotations around the origin



To describe the animations numerically


we need to only record the coordinations of two basis vectors - i and j and everything else will follow from that.

This gives as a technique to deduce where every vector land based on i and j vectors



![[Pasted image 20250812205724.png]]


We could find where any vector [x y] lands based on i and j vectors.

two dimensional linear transformation is described by just 4 numbers - the two coordinates where i and j land each.

This can be packaged into a 2x2 matrix 

$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$
The first column [a c] is the place where the first basis vector lands and the second column [b d] is the place where the second basis vector lands.

When we apply this transformation to a vector 

$$
\begin{pmatrix}
x \\
y
\end{pmatrix}
$$

$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
\begin{pmatrix}
x \\
y
\end{pmatrix}
=
x
\begin{pmatrix}
a \\
c
\end{pmatrix}
+y
\begin{pmatrix}
b \\
d
\end{pmatrix}
=
\begin{pmatrix}
ax & by \\
cx & dy
\end{pmatrix}
$$


Example: if we rotate all of space 90 degrees counterclockwise, then  i lands on the coordinates [0 1] and j lands on the coordinates [-1 0]
![[Pasted image 20250812211042.png]]

to  figure out what happens to any vector after a 90 degree rotation you can multiply its coordinates by that matrix.


Another example of a linear transformation is shear - i and j would look like this 
$$
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

Matrices gives us a language to describe the transformation.

#lineartransformations #matrices
#shear