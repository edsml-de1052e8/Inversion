# Lecture 5: Gradient Based optimisation 

Optimisation: quadratic best viewed as contour plot. 
Reminder that obviously these are just approximations. 

-> contour plot with bubble around initial guess x0, the solution will be outside of it towards x1. 
Gradient is orthogonal to boundary of the circle ⭕️. 

That is another way of saying that the gradient has no component in the other direction on the right (horizontal) basically. Because otherwise that would mean that the function is still increasing.
Gradient has to be in the same direction, that is to say they are scalars : mu f'(x) 
NB: the larger you make mu the closer and closer you will get from x1 to x0 and to steepest descent. 

As a result you get the matrix formed of sum of two parts, by adding the Hassian, and the identity matrix I on the left. 


🚨 for the assignement, all you need to know is in the summaries



**Quasi-Newton Method**


Dennis-More theorem is an important result for quasi-Newton methods

- Newton-Gauss: good for nonlinear least squares problems. Find solution that best fits the equation and do that by minimising R.
We want to find the x that minimises the 2-norm of the residual R(x). 
R is a vector, first derivative is a matrix, second derivative has 3 indices. (?)

NB: you are not doing a standard matrix x vector multiplication first, to get it to that form you need to first take the transpose then derivate it. 

Non-linear regression: fit a curve G that depends on n model parameters x1. 


NB: With linear regression there is no difference between Gauss-Newton and full Newton.
Pluck that in, solve for x (the model paramter) in 0.5 Y transpose Y.

Semi definite is not enough to guarantee convergence of the Newton method. 

Dampened Gaussian, cheaper combination to do. 









