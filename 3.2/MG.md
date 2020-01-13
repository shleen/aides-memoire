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