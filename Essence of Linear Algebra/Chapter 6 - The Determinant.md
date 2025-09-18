
Sometimes it is essential to know how much stretching happens when there is a linear transformation. To measure the factor by each area of a region increases or decreases. 

![[Pasted image 20250812230947.png]]
Imagine the linear transformation

$$
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
 =>
\begin{pmatrix}
3 & 0 \\
0 & 2
\end{pmatrix}
$$
Here the area 1 was one, the linear transformation has scaled the area by a factor of 6. It has increased the i to 3 and j to 2.

In case of shear (from unit sq to shear) the area does not change it just changes the shape to a parallelogram.

The change in unit sq can tell you how the area of any possible region in space changes.

What happens to one sq in the grid has to happen in other sqs in the grid - grid lines remain parallel and evenly spaced (refer to [[Chapter 3 - Linear Transformations and Matrices]])

Any shape that is not a grid sq can be approximated by couple of grid sqs.

This scaling factor is called the determinant of that transformation.

For example, the determinant of a transformation will be 3 if that transformation increase the area of the region by a factor of 3. (squishing can be done as well not only scaling - squishing by 1/2)

The determinant value can be **negative**.
This is because orientation changes - its like flipping space or a sheet of paper.

Lets say  i is to the right of  j and after transformation i is to the left of j - the orientation is said to have been reversed or inverted.
The negative sign implies that and the absolute  value still implies the scaling factor of the area.


![[Pasted image 20250812232802.png]]

Imagine i and j getting closer at one point determinant reaches 0 and then it keeps going to the negative side (as the orientation is getting **inverted**)

In  3D it tells how much volume gets scaled. - we first look at 1 x 1 x 1 cube and then the transformation

Determinant formula for 2d


$$
det(
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
)
= ad - bc
$$




#determinant

