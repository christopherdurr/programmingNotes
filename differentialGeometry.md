#Chapter 1
## Vectors and Products


A plane vector x in ℝ<sup>2</sup> has the representation 

x = x<sub>1</sub>i + x<sub>2</sub>j. 

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


Let u be the angle between vectors x and y. x dot y = |x||y|cos(u)

Two vectors are perpendicular if the dot product of x and y = 0

Cross Product of x and y is the determinant of [i j k; x1 x2 x3; y1 y2 y3]

Cross Product of x and y is the determinant of 

i   j   k

x<sub>1</sub> x<sub>2</sub> x<sub>3</sub> 

y<sub>1</sub> y<sub>2</sub> y<sub>3</sub>

x cross y = |x||y|sin(u)
#Chapter 2
##Description of Lines and Planes
**Parameterization**

Definition

Given a point P in E and a non-zero vector x in ℝ, the line through P with parallel vector x consists of all points Q in E with PQ in span(x)

Example

A parametrization for line l through P[1,2,-2] and P'[3,1,3] is x = PP' = [3 - 1, 1 - 2, 3 - (-2)] = [2, -1, 5]
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

**Equations**

Assume there is a line l in plane E<sup>2</sup> with parallel vector x. A vector n /= 0 is a *normal vector* to l if it is orthogonal to x. i.e. n dot x = 0

Example

We are given P<sub>1</sub> = [2,5]and P<sub>2</sub> = [-1,4]

x = P<sub>1</sub>P<sub>2</sub> = [-3, 1]

n = xhat = [1, -3]

n dot P<sub>1</sub> = -13

The line l can be described as the equation x - 3y = -13

Example 

**Planes**

Assume we have P<sub>1</sub>, P<sub>2</sub>, P<sub>3</sub> in E<sup>3</sup>

To derive an equation which determines plane a containing these three points:

Let OQ = [x,y,z], OP<sub>i</sub> = [x<sub>i</sub>, y<sub>i</sub>, z<sub>1</sub>]

Then x = P<sub>1</sub>P<sub>2</sub> = [x<sub>2</sub>-x<sub>1</sub>, y<sub>2</sub>-y<sub>1</sub>, z<sub>2</sub>-z<sub>1</sub>]

y = P<sub>1</sub>P<sub>3</sub> = [x<sub>3</sub>-x<sub>1</sub>, y<sub>3</sub>-y<sub>1</sub>,z<sub>3</sub>-<sub>1</sub>]

P<sub>1</sub>Q = [x-x<sub>1</sub>, y-y<sub>1</sub>, z-z<sub>1</sub>]

solve [x,y,P<sub>1</sub>Q] = 0 

**Several Lines**
There are three cases:

1. x and y are linearly independent. This yields an answer to the matrix [A|PP']
2. x and y are parallel, but x and PP' are linearly independent. In this case, [A|PP']reduces to a matrix where the second row is [00|t] where t /= 0. *i.e. the matrix has no solution*
3. x,y, and PP' are parallel. In this case, [A|PP'] is reduced so that the second row is [00|0]

EXAMPLE

P=[5, -1], P'=[-7,3], x = [1,-2], y = [3,-7]

Then A = [x,y]

[A|PP'] = [1 3; -2 -7] = [-12;4]

Gaussian elimination gets us [1 0; 0 1] = [-72; 20] = s<sub>Q</sub>x

The point of intersection Q is OP + s<sub>Q</sub>x, or [5,-1] + [-72, 144] = [-67, 143]

**Two Lines in Space**

Two lines in E<sup>3</sup> are skew if there is no plane a in E<sup>3</sup> containing both of them. Thus, the lines do not intersect.

A = [PP'] If it has no obvious solution, then the lines do not intersect!

**Two Planes**
Assume we are given 

a<sub>1</sub>x + b<sub>1</sub>y + c<sub>1</sub>z = d<sub>1</sub>

a<sub>2</sub>x + b<sub>2</sub>y + c<sub>2</sub>z = d<sub>1</sub>2.

Get a matrix [A|d]. If one of the variables is free (i.e. rank A = 2), it can be used as a paramater representing the line of intersection

If rank A = 1 then they are either parallel planes or both equations determine the same plane. 

**Example**
Assume two planes are given by the equation
x − y + 2z = 1

2x + y − 2z = 2

This reduces to 

1 0 0 | 1
0 1 -2 | 0

Yielding the solution [x,y,z] = [1, 2t,t] = [1,0,0] + [0,2,1]t

This is a parametrization of the line l where plane 1 and plane 2 intersect.

**A line and a plane**

If the plane α is given by a linear equation ax + by + cz = d insert the components of parametrization of line l into that equation and obtain a single linear equation in the variable t. A solution t of the latter inserted into the
parametrization for l yields the vector. 

#Chapter 3: Orthogonal projections, distances, and angles

We use projections in particular to define and calculate distances and angles


Orthogonal projection of vector x onto span(y) is:

p = (x*y/y*y)y

Vector p is parallel to y and has length |x|cos(u), where us is the angle between x and y. 

**Projection of point on line**

Point + orthogonal projection

**Projection of a point on a plane**

p = (PR · n)/(n · n)n

Coordinate R + p










