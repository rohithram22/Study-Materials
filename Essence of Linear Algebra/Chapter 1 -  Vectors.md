
Vectors can be seen from three perspectives - Physics, Computer Science and Mathematics

Physics student - arrows pointing in space - length and direction defines the vector

Computer Science - ordered list of numbers (order matters) - kind of fancy word for lists

Mathematician - generalizes both views. Vector can be anything where we can add or multiply another vector 



*Think about the vector as an arrow in a coordinate system (like x-y plane the tail in the origin)*

![[Pasted image 20250807233625.png]]
The coordinates of a vector is a pair of numbers that basically gives instructions for how to get from the tail of that vector from the origin to its tip. 


In 2D,

First number - how far to walk along x axis,
Second number - how far to walk parallel to the y axis

![[Pasted image 20250807235002.png]]Every vector is associated with only one pair of numbers


in 3D, triplet of numbers is used 

$$
\begin{pmatrix}

2 \\
1 \\
3

\end{pmatrix}
$$

#### Vector Addition

Adding two vectors ![[Pasted image 20250808000243.png]]
move the tail of one end of the vector (w) to the tip of the another vector (v),
and when you draw a new vector from the tail of vector (v) to the tip of the vector (w) - thats where the new vector sits.

![[Pasted image 20250808000654.png]]


(Only time we let vectors stray away from origin).

Vectors are like steps or something that moves around with direction.


For example,
$$ \begin{pmatrix} 1 \\ 2 \end{pmatrix} + \begin{pmatrix} 3 \\ -1\end{pmatrix}$$This can be thought of a 4 step path - 
First walk 1 to the right 
and 2 to the up 
and 3 to the right of that
and 1 down 

![[Pasted image 20250808001143.png]]


![[Pasted image 20250808001750.png]]


#### Multiplication By a Number 

This stretches or squishes the vector 

By multiplying by 2 the vector increases double the size in the same path as the vector
By multiplyung by 1/3 it squishes to 1/3rd of the size 
when multiplied by -1.8 it flips and then stretches out .
this is called Scaling 

![[Pasted image 20250808002007.png]]

$$ 2  . \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 2x \\ 2y \end{pmatrix}$$


The ability to transform between number lists and coordinate system representation helps data analysts, mathematician etc.



#vectors #vectoraddition #vectormultiplication