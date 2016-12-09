#Chapter 1
## Vectors and Products

A plane vector x in ℝ<sup>2</sup> has the representation 

x = x<sub>1</sub>i + x<sub>2</sub>j. 

A space vector y in ℝ<sup>3</sup> has the representation

y = y<sub>1</sub>i + y<sub>2</sub>i + y<sub>3</sub>k

Zero Vector is [0, 0, 0]

If a vector x is multiplied by a scalar a: 
* ax = [ax<sub>1</sub>, ax<sub>2</sub>, ax<sub>3</sub>]


DEFINITIONS
* A linear combination w = ax + by + cz is *non-trivial* iff one of the coefficients is not a 0. 
* The set of all linear combinations of a set of vectors is their span
* A set of vectors is linearly dependent if the zero vector is expressible as a non-trivial linear combination of the vectors in set
* Two non-zero vectors x and y are linearly dependent iff they are *parallel*. i.e. there exists a constant c where y = cx
* Three non-zero vectors x,y, and z are linearly dependent iff they are *coplanar*. i.e. if x and y are parallel or there exist constants b and c such that z = bx + cy

Given points P and Q where P = [x<sub>1</sub>, x<sub>2</sub>, x<sub>3</sub>] and Q = [y<sub>1</sub>, y<sub>2</sub>, y<sub>3</sub>]

Vector PQ = [y<sub>1</sub> - x<sub>1</sub>, y<sub>2</sub> - x<sub>2</sub>, y<sub>3</sub>- x<sub>3</sub>]

Length of vector X is defined as |x| = sqrt(x<sub>1</sub><sup>2</sup> + x<sub>2</sub><sup>2</sup>)

Let u be the angle between vectors x and y. x*y = |x||y|cos(u)

Two vectors are perpendicular if the dot product of x and y = 0

Cross Product of x and y is the determinant of 

i   j   k

x<sub>1</sub> x<sub>2</sub> x<sub>3</sub> 

y<sub>1</sub> y<sub>2</sub> y<sub>3</sub>

x cross y = |x||y|sin(u)

#Chapter 2
##Description of Lines and Planes HC

**Parameterization**

Definition

Given a point P in E and a non-zero vector x in ℝ, the line through P with parallel vector x consists of all points Q in E with PQ in span(x)

l = P + ty

Example

A parametrization for line l through P[1,2,-2] and P'[3,1,3] is 
x = PP' = [3 - 1, 1 - 2, 3 - (-2)] = [2, -1, 5] 
l = [1, 2, -2] + t[2,-1,5]

**Planes**

a = sx + ty

Given three distinct points P<sub>1</sub>, P<sub>2</sub>, P<sub>3</sub> in E<sup>3</sup>

OQ = OP<sub>1</sub> + P<sub>1</sub>P<sub>2</sub> + tP<sub>1</sub>P<sub>3</sub>
* is a line, if P<sub>1</sub>P<sub>2</sub> and P<sub>2</sub>P<sub>3</sub> are parallel
* is the plane containing P<sub>1</sub>, P<sub>2</sub>, P<sub>3</sub> otherwise. 

Let P<sub>1</sub> = [1, 1, 1], P<sub>2</sub> = [2, 2, 1], P<sub>3</sub> = [3, 2, 2], and Q = [1, −2, 4]

a = [1, 1, 1] + s[1, 1, 0] + t[2, 1, 1]

To decide if Q is in a, we must determine if Q = sx + ty has a solution

In this case determine if there is a solution for the following:
[0,-3,3] = s[1,1,0] + t[2,1,1]

We can use gaussian reduction to discover there is indeed a solution, and Q is in a. 


