## Week 1 - An Introduction to Math for Games
- Common Test - Week 9
- Common Test - R-Method
- Reference angle
    - Has to be *acute*.
    - Has to be *positive*.
    - Refers to the angle between the line & the x-axis.

## Week 7 & 8 - Matrices & Linear Systems
The **order** of a matrix - 2 numbers, representing the number of rows (r) & number of columns (c) in the matrix respectively. It is typically represented in the form **r x c**.

### Types of Matrices
- Square - Same number of rows & columns.
- Diagonal - A square matrix where only the diagonal elements are non-zero values.
- Unit (or identity) - A diagonal matrix where the diagonal elements are 1's.
- Null (or zero) - Every element is 0.
- Row - 1 row, any n number of columns.
- Column - 1 column, any n number of rows.
- Symmetrical - Element (i, j) == element (j, i).

The **transpose** of a matrix - attained by interchanging the rows & columns of the matrix. Typically represented by a superscript of the letter **T** above the name of the matrix.

### Matrix Arithmetic
- **Addition** - Possible between matrices with the same order. Done by adding the corresponding elements, resulting in a matrix with the same order as the matrices that went into the operation.
- **Subtraction** - Done very much in the same way as matrix addition. Matrices of the same order, & subtraction of corresponding elements.
- **Scalar Multiplication** -  Each element of the matrix is multiplied with the scalar in question.
- **Scalar Division** - Division of a matrix by a scalar value k is essentially scalar multiplication of 1/k.
- **Matrix Multiplication** - The operation A x B, where both A & B are matrices, is only possible if the number of columns in A is equal to the number of rows in B. The resulting matrix will have the the same number of rows as A & the same number of columns as B. Each element (i, j) of the resulting matrix is the dot product of row i in matrix A & column j in matrix B.

If A is an m x n matrix & I the n x n identity matrix, then **AI = A**. If m == n then **AI = A = IA**.

The **determinant** of a 2x2 matrix, is denoted as `det A` or `|A|` for a matrix A. Given that matrix A is [[ a b ], [ c d ]], `det A = ad - bc`. Note that if a matrix has a determinant of 0, it has no inverse & is also known as a **singular** matrix.

To obtain the inverse of a 2x2 matrix [[ a b ], [ c d ]];
- Interchange elements **a** & **d**.
- Negate **b** & **c**.
- Dividing the entire matrix by it's original determinant.

The inverse of a matrix is typically represented with a superscripted **-1** above the name of the matrix.

Given a matrix A, both operations `AA-1` & `A-1A` result in the identity matrix.

For two matrices to be **equal**, they have to be equal in both order & elements.

## Week 13 & 14 - Linear Transformations
An **identity transformation** - `I(x) = x`.

A **zero transformation** - `O(x) = 0`.

## Week 15 & 16 - Linear Kinematics
**Uniform motion** describes an object that is moving in a specific direction at a constant speed.

Fittingly, then, **uniform circular motion** describes an object moving in a perfect circle at a constant speed.

### Distance & displacement
- **Distance**(m) is the scalar quantity describing the total length of travel.
- **Displacement**(m in a specific direction) is the vector quantity describing the change in position of an object in a particular direction.

### Speed & velocity
- **Speed**(m/s) of an object is its rate of change of distance. It is calculated with 

    `speed = ∆ distance / ∆ time`

- **Velocity**(m/s in a particular direction) of an object is its rate of change of displacement. It is calculated with 

    `velocity = ∆ displacement / ∆ time`

**Accelerated motion**, on the other hand, describes objects that are not moving with a constant velocity.

**Acceleration**(m/s^2) refers to the rate of change of velocity. Calculated with 

```
acceleration, a = ∆ velocity / ∆ time 
                = (v - u) / t           where u = initial velocity & v = final velocity

also, v = u + at
by integration, s = ut + .5at^2
& v^2 = u^2 + 2as
```
Note: the last 3 equations above can only be used when **acceleration is constant**

If an object's mass remains constant, & nett force is known, acceleration can be computed with Newton's second law of motion, `F = ma` which, rearranged, becomes `a = F/m`. If the weight (W) & drag (D) of the object is known, force (F) can be computed as well - `F = W - D`. Put together, we have `a = (W - D) / m`.

**Terminal velocity** refers to the phenomenon where W = D (D increases w the square of speed), resulting in F = 0 & therefore a = 0. It refers to this constant velocity.

### Projectile motion
A form of motion experienced by an object that is thrown & that moved along a curved path under the action of only gravity. In these situations, it is oft assumed for air resistance to be negligible.

This motion is 2-dimensional, & the object's velocity can be seen to be comprised of an x-component & a y-component.
```
x_vel = u cos(θ)
y_vel = u sin(θ) - gt   where g = 9.81m/s^2

the x length of motion, range = (u^2 sin(2θ)) / g
total_time_taken = (2u sin(θ)) / g
```

