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



**Solving the discrete model backwards**

**Adjoint Equation**

To find the stationary points of lagragian L we simply write down its partial derivatives and set those to zero



**Checkpointing**

Although adjoint equation is linear it depnds on the forward solutionu so we need access to it entirely in all timesteps. But that is very memory expensive if you need to store all these for all timesteps. A trick them is to write a few intermediate results, called **checkpoints** at specified intervals. Then you can pick up from and recompute from the nearest intermediate timestep. 


### Summary of Methods 🗒 

Although we have outlined a procedure to solve PDE-constrained optimisation problems using the adjoint method, there are still a few important choices we have to make when implementing this method. We distinguuish between two approaches: 

**The continuous adjoint approach**: starts with a continuous formulation of the PDE-constrained optimisation, i.e. we simply write down what PDE we want to solve, which we will call the *forward* PDE, without specifying which discretisation is going to be used. The adjoint equation then produces a second PDE, the *adjoint* or *backward* PDE that solves for . 

We now need to implement a discretisation for both the forward and the backward PDE. Luckily in many cases, the backward PDE is closely related to the forward PDE, so the code used to solve the forward PDE numerically, can be adapted to be able to also solve the backward problem. Fpr complicated nonlinear PDEs, the relations between the forward and the backward model is not always that straightforward however. 

NB: Issues with discretisation errors: the derivative that you end up with in the end is not exactly the same as the discrete derivative that we would get otherwise. This may also lead to convergence errors.


**In the discontinuous (or discrete) adjoint approach**: the discretisation of the forward PDE is already chosen beforehand. This leads to a discrete PDE-constrained optimisation problem. 

The procedure to solve lambda for  is to take the adjoint of the forward *discrete* model, and requires taking derivatives of that code (see next section), which can be a complicated procedure. The main advantage of the discontinuous approach is that it produces the exact (except for details such as solver tolerances, machine precision, etc.) derivative of the discrete model that is used to evaluate the reduced functional for a given m . In the continuous approach, when we hook up our final implementation to the optimisation algorithm, we also use a discrete model to calculate the reduced functional values. This is however just a *numerical approximation* to the underlying continuous PDE, which introduces numerical error between the two. In the continuous adjoint method for calculating the derivative we again introduce numerical error, by discretising the adjoint PDE. Thus the gradient information that the optimisation algorithm receives is a numerical approximation of the procedure to compute the functional values.





