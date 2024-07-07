# MBiol-2024-Game-theory-parental-care

This repository contains the Mathematica code for the results I reported in my MBiol dissertation investigating competition dynamics between parental care strategies. 
The code is organised by function, some functions such as one-way invasion analyses have code in both Mathematica and R languages. 

My masters project aimed to investigate whether pairs of different parental care strategies (Male-only, Female-only, Biparental, No care) could coexist in a population using Evolutionary Invasion analysis. 
Strategies are determined by the values of sex specific care terms. Cm > 0 (typically 0.7) shows paternal care and cf > 0 (0.7) shows maternal care. Presence of paternal and maternal care together is biparental and presence of neither is No care.

I have included scripts for:

Population dynamics (population size against time)
- Setting up the model and testing population dynamics using RK4 integrator code. (R script)

One-way invasion 
- Competing a rare mutant parental care strategy with a different resident strategy at equilibrium (resident dA/dt = dE/dt = 0)
- Fitness of the rare mutant is a measure of per-capita population level growth rate, which is affected by the equilibrium population density of the resident, representing strategy competition
- Dominant eigenvalue (lambda) of the matrix of partial derivatives (of dA/dt and dE/dt, with respect to A and E) is mutant fitness

- Most scripts show mutant fitness for the invasion against a value of life history in the mutant, where life history is fixed in the resident. Some scripts show the effects of changing the same life history trait in the mutant and the resident together.

  Latin Hypercube Sampling One-way invasion scripts
- One-way invasion scripts where the sampling space is expanded. Mutant fitness is still shown against one independent variable life history trait but the other life history values are sampled randomly (for each sample which represents and invasion, the life history conditions are the same in the resident and mutant).
  
Reciprocal invasion
- Mathematica scripts for reciprocal invasion of two parental care strategies into each other.
- Invasion boundaries for fitness = 0 for both directions of invasion shown against values of a life history parameter in each parental care strategy.
