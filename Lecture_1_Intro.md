# Lecture 1: Inversion and Optimisation 
*(28/02/22)*

Here m = linear equations
n = degrees of freedom

General reminder:

Inverse of cos(x) has only solutions between -1 and 1.

Inversion applications: can be used for discretising PDEs, if the PDE is time dependent. In that case you need to do an inversion problem of m equations and n at every time step.
Can be used in remote sensing to see that every value of y is correct in a predictive model.
Can also be applied to ML.

Inversion can transform in a polynomial equation a problem from non linear to linear (???)

If you have three equations with three unknowns in a quadratic equation function this gives a system of three equations. Can solve by inverting matrix and have our quadratic polynomial coefficients

Instead of fitting all points through a curve for approximation, can use a Least Squares fitting method  to approximate trend.
Can use iterative approach to inversion in order to ameliorate the solution and get to a point where errors are minimised. You can later compare with data that wasn't inverted.

**Optimisation**

Seeks to minimise the error, tries to find a value in a scalar function for which the function has a minimum (can also be max).
Do that by looking at derivative, finding stationary points with extra criterias.
Note that optimisation problems can be turned into inversion problems.


even for matrices that arent square, can defined rank of matrix both ways ( both through linearly independent rows and columns).
Linearly independent rows for example mean that it doesn't depend on previous rows eg. sum of 2 rows gives the 3rd row this would be linearly dependent.

In the case of a non-sqaure matrix with for example more columns than rows, we still have less constraints (still solutions left) than the degrees of freedom (DF on the right)

Uniquess: number of rank equals n (degrees of freedom n ((or number of columns ?)))
Can also expect solution to be unique if there are no non-trivial nodes.


- Mixed determined: can also be thought of as rank-deficient. Uniquiness and existence are both not guaranteed. Also means solutions are not unique. 
- Row Echelon Form: row operations on matrix to see if it is rank efficient.


