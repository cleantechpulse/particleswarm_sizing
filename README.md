README.TXT - Particle Swarm Optimization Files

- /env: Virtual environment
- /Data: Input files not created endogenously by the scripts
- /Results: Files created endogenously by the scripts, either as intermediate or final output
- /Sandbox: Development code we don't want to push to the github repository
- /Coding: Deployment code
- /Archive: Old code that is now outdated

## Coding:
- pso_componentsizing.py : most up-to-date
- gridSearchParallel.py : 
- RadioSimulator.py :
- SimulateOnbeDesign_PassFail.ipynb : enter a set of parameters, and get a simple pass/fail output of whether that design worked.
- Grid Search and Simulation Plotter.ipynb : This is mostly a grid search, but happens to also have plotting capabilities. Does not have any PSO functionality. 
- PSO_Parallel_ComponentSizing.ipynb:


## Sandbox:
- *PSO_Learning_Rastriggin.ipynb* : My notes from learning the PSO algorithms, along with the implementation of PSO for Rastriggin's problem, based on a blog post with sample code.
- *PSO_BasicProblem.ipynb* : Particle Swarm optimization applied to the most basic problem: single-reservoir, just a few time steps.
- *PSO_Parallel_Rastriggin.ipynb*: Solution of Rastriggin's problem using parallelization to solve each particle's problem in parallel. Calculated the Did not time the execution to identify where the bottlenecks were, and did not 


# Workflow

- Run a grid search to identify feasible points
- Save the outcome of the grid search to a csv
- Sort the grid search csv to identify the best-performing feasible points

PSO:
- Define feasible space
- Randomly draw initial points and velocities
- Use the top n grid search items to populate some of the starting points for the particles
- For each epoch,
  - Pool particle simulations across the cores
  - Every n epochs, save the best location and all of the particle data.

