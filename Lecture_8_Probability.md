# Lecture 8: Probability 


Don't use Crand for generating random numbers

Good rule of thumb for PRNG:
- keep a copy of the seed (what pseudo number generator you are using)
- Explicit better than implicit.
- All of this gets weirder in parallel

TRNGs (True Random Number Genetator)
- use external physical/hardware source of randomness
- good for security

CSPRNG (cryptographically secure random number generator)
- Use TRNG to reseed good PRNG on initialisation 
- Unlikely to be guessed based on previous data
- Middling cost to implement

Most of data is real number. 


### Data Assimilation

BLUE: Bets Linear Unbiased Estimator

- Estimator: fixed guess at statistical quantity
- Unbiased:: error has zero mean 
- Linear Tguess = alpha * T1 + alphaT2

y: observation
x: model data


Can also extent Kalman filter to the non-linear case by linearizing it. 




