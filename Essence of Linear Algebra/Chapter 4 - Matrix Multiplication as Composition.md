

Lets say we are applying a linear transformation and another linear transformation on that. The product of matrices of both linear transformations can be called a composition.


For example,

Lets say we apply a 90 degree counterclockwise rotation and a shear( mentioned in [[Chapter 3 - Linear Transformations and Matrices]]) after that the result we get by individually multiplying the matrices to the vector  
$$ ShearMatrix * (RotationMatrix * Vector) = CompositionMatrix * Vector $$
Where CompositionMatrix is as shown below

![[Pasted image 20250812212807.png]]
Note : for composition we need to read the functions from right to left. so first rotation and then shear. 


#### Matrix Multiplication
![[Pasted image 20250812213342.png]]

Think of matrix multiplication in terms of linear transformations. If we apply shear first and then rotation - the result is not the same as applying rotation first and then shear

$$M_1M_2 \neq M_2M_1 $$


Matrix Multiplication is associative
$$A(BC) = (AB)C$$
We can understand this by seeing this in terms of linear transformations. In the LHS we first apply C transformation then B and A. And then in the RHS we do C transformation then B and then A. We basically shows that both are equal.


#lineartransformations #matrixmultiplications #compositions #matrixproperties 

