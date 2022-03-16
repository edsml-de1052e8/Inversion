# Lecture 11: Numerical Implementations of FWI




You need to define the source and receiver objects. with interpolation for receiver

With PDE and sources and receivers set up you then create the operator.

run the operator op, try it with a short amount of time eg. 100 ms then can expand to more

nshots is number of shots used to generate fradient
nreceivers : number of receivers locations per shot
dwi_iterations: updates the model and runs it n amount of times


model1 is the 'true model' the actual structure of the subsurface and model 0 is the first guess
Iterating over this model until we can get to a good result. Have to go from being a model with constant parameter to get ot the circular bit.

**True and smooth data**

space order, solves same equation, can set to 4 or 2 just changes the spatial discretisation.

```true_d``` fills in the true data with a solver.

Devito does calculation, the gradient for each shot.

def ```update_sith_box``` -> vp is velocity, dm is step












