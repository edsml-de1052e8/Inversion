# Lecture 10: Introduction to Devito



DeVito Python package to implement optimized stencil computation on structured grids (e.g., finite differences, image processing, machine learning, solves PDEs).

Domain Specific Language (DSL): computer language specialised in particular application domain eg. HTML for web pages.
This differs to general pupose languages (GPL) like Python. 

Devito is an open source project from ICL's Earth Science and Engineering department. It is in fact a DSL and compiler, doesn't just translate into C code but also runs optimisation 

Befire starting the stencils, need to define the mesh thru creation of a grid object with a specific size. This is done using ```shape=(1,4)``` and ```extent(1,1)```

Devito works with a function object like ```sympy``` package. 
The function by default doesn't have a time dimension. If you want one, you need to use another function called the ```TimeFunction```. This takes the form g(t,x,y).


#### Finite Differences (Derivative of symblic functions)

Taylor series in spatial dimension takes the form f(x +h,t)= .....
Forward difference approximation bc we're rearranging according to x+h . It is how spatial derivatives are approximated in space order 1 finite difference schemes.





