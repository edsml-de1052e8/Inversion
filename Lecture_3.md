# Lecture 3: 


*Continuing from lecture 2*


Best iterative method for SPDs (symmetric positive definite matrix) is probably the conjugate gradient method.

🚨 Assessment: will not ask on coding up discretisation from scratch
Instead you will be given a code that produces the matrix that is associated with the discretisation


Iterative method: eg. Gauss-Seidel or Jacobi method

Stationary method: doing the same linear operation on the residual.

Conjuate gradient method performs well on stationary methods, can combine them. 
Combining steepest descent to stationary method means you're applying steepest descent to slightly modified equation, needs to be able to have an inverse(?)

**Pre-conditioning:** effective combination with stationary methods, good for cases when condition numbers increase with system height. Can therefore reduce iterations by a lot. 
