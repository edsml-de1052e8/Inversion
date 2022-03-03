# Lecture 4:



## Linear Solvers


The **multigrid V-cycle:** particular problem on mesh to be resolved. From fine grid to coarse (manipulation here) then back to fine.
For steepest descent, conjuagte gradient or SSOR, increasing number of iterations increases number of conditions. 
Large eigenvalues are associated with very noisy modes. Methids like SSOR help to deal with that noise.

Multigrid methods are designed to effectively hndle the large scale component of the residual. Gets rid of the noisy bit of the error, applies a smoother (simple preconditioner).
This problem may happen when you have a lot of different resolutions or scale in one mesh.

Then error is approximated on a smaller coarse grid, reduces the problem so makes it cheaper.
NB: can also apply symmetric preconditioning to this problem.
NB: assumes linear independence of each iteration 
As soon as the exact solution is in the Krylov Subspace they become dependent.

**Krylov subspace**

- Every time you add a new vector, increase the subspace
- Every time you take the residual vectors and iterate it as a function of the previous iteration. But all iterations based on the initial residual and add to it (?)

**Gradient Steepest Descent Krylov subspace**
- every new iterate is formed from a linear combination of the step vectors p
- finds optimal solution by looking at the distance between the exact solution and the a null
- Chooses that point closest to the solution at each iteration

**GMRES**

- also a Krylov method, not restrictive in terms of matrix requirements. Good for asymmetric linear systems




## Non-Linear Solvers

**1D Methods**

When solving F (x) =0 (instead of Ax =0) for non-linear functions
Start with the idea of finding the fixed point G(x) = x. 

**Fixed point iteration/Picard iteration:** iterative method to find such fixed point by iteratively applying G(x(^i))


Banach Fixed Point Theorem(?): the absolute value of a derivative G(x) should be smaller than 1 for it to be a contraction so that we can guarantee convergence.

Chord Method: evaluates the function f and introduces a term m which controls the iterations in the Picard. Different values of m give you different slopes.


**Newton's method in multiple dimensions**

In 1D the strong point of this method is that: assumin we're close enugh to the statioanry point the method will converge quadratically to it (local convergence). Same holds for Newton's method in multiple dimensions. 

Assumes that F is differentiable and that its derivative is Lipschitz continuous.

Local convergence: the method doesn't tell you how close you are or how far, just that you are within range to the stationary point. 
For a lot of initial guesses, Newton might not even converge. -> remedy that with line search methods


Steps include:
- Evaluate F(x)
- evalueate F'(x)
- solve F'(x)p = -F(x)
- Update x(i+1) = x(i) + p


**Line Search Method**

When initial guess is too far oof to the stationary point. 

Condition: p is in the direction of the function f & the direction where it descends the most, called descent direction.
















