# Lecture 7: PDE Optimisation



**1D Advection Problem**

When you don't know the initial condition, can use the unknown u (?). NOte that in f(u,m) m does depend on u in some cases.
For the solution of u, look at the solution for all time steps, so need to write all the equations of all time steps at all times.
This gives a very large system to solve, with combinations of matrix of time step 0, time step 1 etc * u (unknown) = m
Here we also assume that we have been given the value of m eg. the position of a wind turbine.


Can be written as g(u,m) = A * u -b = 0

**Reduced Problem**

In PDE-constrained optimisation we assume that for a given choice of model parameters  we can uniquely solve for a  that satisfies the PDE (which may also depend on other model parameters that we choose not to vary). 
In other words for each  we can find a unique  that satisfies the PDE constraint g(u,m)=0

So solve pde for the given value of m.

Unconstrained optimisation problem: if we assume we can solve the pde for all time steps of m.

**Tangent Linear Approach**

The meaning of this tangent linear equation is easiest to understand for the case that m is just a single parameter (a value) in the model.

The tangent linear equation above provides a PDE that can be solved to obtain du/dm. This PDE is a modification of the original PDE. In particular, even if the original PDE is nonlinear the PDE described by (tangent-linear-equation) is linear.


**A baclwards continuous PDE for lambda**

instead of getting initial condition, you start with the final condition of lambda which is from the derivative of the function. So you solve the lambda equation backwards in time to solve what the lambdas are.

General idea: we can derive a continous equation for the adjoint variable.












