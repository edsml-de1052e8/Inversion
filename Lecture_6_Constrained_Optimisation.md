# Lecture 6: Constrained Optimisation
*07/03/22*


Following from lecture 5's, in all the methods such as Steepest Descent or Quasi Newton method, you need to know when to stop the number of iterations.
This is called the stopping criterion

For a root finding problem, the best way to judge our current best guess, is to establish how well it satisfies our equations.

**Relative tolerance:** in a time-stepping numerical model, where the solution from the previous time-step is a good initial guess for the solution at the next time step (assuming our time-step is small enough). 
In such situations, a lot of these scaling issues with a stopping criterion based on the absolute error can be avoided by using the stopping criterion

**Stalling criteria**: doesn't really look at how small the error but rather if the iteration is progressing. SO if it isn't progressing then you it might make sense to stop the iterations.
NB: when an iteration it doesn't always mean that the answer is necesserily *good*. If using a library using a stalling criteria, check the code and check the stopping critieria.


Newton-CG method (and indeed all conjugate gradient methods) only works on SPD matrices, need to make sure the Hessian is spd (?) so can detect indefiniteness if the inner product p, Ap becomes 0 or negative and add that as a condition in the function.

If we have an indefenite matrix (p=0, we can do steepest decent instead with p = -Fx


Impportant to test that the derivative function is correct using a Taylor test. 

let's treat our computer program as a mathematical function that takes a number of input values gathered together in a vector and returns a value. Then if is the derivative of this function - this implies that f is actually differentiable as a mathematical function - then by Taylor's theorem we may write.
Need a small enough h so that we get an assymptotic behaviour that is clear.

-> Do a Taylor test in the assessment to test derivative accuracy



**Convex Functions and the Hessian**

- Any local min of a convex function is a global minimum. If the function is strictly convex when global min is attained in a single point.

- 










