# Lecture 2



In SVD the rank is the number of non zero singular values

M = U * Sigma * V(^T)

Can get M in three steps: decompose the matrix using V star, Sigma to apply scaling in different directions (m x n wiht pivot values), and then transformation U (m x m). 
NB: V* is same as V transpose


SVD is very expensive to do, so not done that much.


Closest point:
if you're in a minimum the difference between x* and xk+1 is 0 as the closest point on a straight line to x* is orthogonal (perpendicular to x*).

Eigenvalues of matrices:

This means that matrix  𝐀⎯⎯⎯1  is positive definite (both eigenvalues positive) and  𝐀⎯⎯⎯3  is positive semi-definite (eigenvalues positive or zero). Matrix  𝐀⎯⎯⎯2  (both negative) is also called negative definite, and  𝐀⎯⎯⎯4  (negative and positive eigenvalues) indefinite.

The two **eigenvalues** characterise the behaviour of the function in the two orthogonal directions associated with the two eigenvectors: for a positive eigenvalue it looks like a parabola with positive coefficient.

The **covariance matrix**  𝚺  is an important tool in statistics and probability theory. For  𝑛  different signals/time series/random variables  𝑋𝑖  of data, it computes the covariance between the different pairs of data.

To check the symmetry of the matrix sigma, we check that the difference with its transpose is the zero matrix - which in turn we check by looking at its norm.
A symmetric real-valued matrix is SPD if all its eigenvalues are strictly positive.
