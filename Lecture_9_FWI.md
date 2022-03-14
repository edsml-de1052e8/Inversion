# Lecture 9: FWI


The central purpose of FWI is to find a physical model of the wave-transmitting medium that minimises the difference between an observed dataset 
and the same dataset as predicted by the model. 
To achieve this, most common is a least-squares formulation where we seek to minimise the sum of the squares of the differences between the two datasets over all sources and receivers, and over all times.

**Steepest Descent**

If the number of model parameters  is large, calculating the Hessian is a major undertaking, and inverting it is not normally computationally feasible. Consequently the method that is typically used is to replace the inverse of the Hessian in equation (23) by a simple scalar alpha ; this scalar is called the step length.


