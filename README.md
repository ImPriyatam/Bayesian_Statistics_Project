# Bayesian Statistics Project
**Parameter estimation** through Bayesian statistics is a powerful and flexible approach used in various fields of science and data analysis to infer the most likely values of unknown parameters in a model. It involves combining prior knowledge (prior distribution) about the parameters with observed data to update our beliefs and obtain a posterior distribution that reflects the updated knowledge about the parameters.

## Parameter Estimation using MCMC and HMC Algorithms

Parameter estimation using Markov Chain Monte Carlo (MCMC) simulation and Hamiltonian Monte Carlo (HMC) algorithms is a powerful technique for sampling from complex probability distributions, particularly in Bayesian inference problems. These methods allow you to explore high-dimensional parameter spaces and estimate posterior distributions even when analytical solutions are not feasible. Let's delve into how MCMC and HMC work:

### Markov Chain Monte Carlo (MCMC)

1. **Markov Chains**: MCMC is based on the idea of constructing a Markov chain that explores the parameter space. Each step in the chain depends only on the previous step, creating a sequence of parameter values.

2. **Metropolis-Hastings Algorithm**: The Metropolis-Hastings algorithm is a fundamental MCMC approach. It involves proposing a new parameter value from a proposal distribution and then deciding whether to accept or reject the proposed value based on the likelihood of the data and the prior distribution. The acceptance criterion ensures that the chain converges to the desired distribution over time.

3. **Convergence**: One of the challenges in MCMC is ensuring that the chain has converged to the target distribution. Methods such as monitoring trace plots, calculating autocorrelation, and using convergence diagnostics like the Gelman-Rubin statistic help assess convergence.

### Hamiltonian Monte Carlo (HMC)

1. **Dynamics and Energy**: HMC introduces a physical analogy to MCMC by considering the parameter space as a physical system. The parameter values are treated as positions, and their likelihood and prior are treated as potential energies.

2. **Hamiltonian Dynamics**: HMC simulates the evolution of the system by using Hamiltonian dynamics equations, which involve the derivative of the potential energy (gradient) and a momentum variable. The momentum helps guide the exploration of the parameter space.

3. **Leapfrog Integrator**: To numerically solve the Hamiltonian equations, the leapfrog integrator is commonly used. It discretizes the dynamics over small time steps, allowing the system to evolve while conserving the total energy.

4. **Metropolis Correction**: The HMC algorithm generates a new proposal using the dynamics and accepts it with a Metropolis-like acceptance step, just like in the Metropolis-Hastings algorithm. The acceptance accounts for both the proposed parameter value and its associated momentum.

### Benefits and Considerations

- **Efficiency**: HMC is often more efficient than traditional random walk Metropolis algorithms for high-dimensional and correlated parameter spaces. It explores the space more efficiently by utilizing the gradient information.

- **Tuning**: HMC requires tuning of parameters like step sizes and integration steps. Poor tuning can lead to inefficient exploration or even divergent trajectories.

- **Implementation**: Implementing MCMC and HMC algorithms can be complex, but libraries like Stan, PyMC3, and emcee provide user-friendly interfaces for conducting Bayesian inference using these techniques.

- **Sampling Quality**: Both MCMC and HMC provide samples from the target distribution, enabling posterior analysis, credible intervals, and other statistical summaries.

- **Complex Models**: These techniques are particularly valuable when dealing with complex models with nonlinear relationships and intricate parameter spaces.

In summary, MCMC and HMC are essential tools for Bayesian parameter estimation, allowing you to explore complex parameter spaces and infer posterior distributions even for models with no closed-form solutions. These methods play a critical role in modern statistical analysis and scientific research.

:rocket: :bar_chart: :microscope: 📖 
##  Cosmology parameter estimation from Supernovae Ia Data
The aim of this exercise is to write an MCMC code to estimate cosmological parameters $\Omega_m$ Ωm, Ωv, h from supernova
Ia data. Supernova Ia are standard candles (or can be made so), so can be used to measure the contents
of the Universe.


## Eddington's Parameter Estimation Problem
​The aim of this exercise is to analyse photographic plates from Eddington's 1919 eclipse expedition, to determine whether the data favour Newtonian gravity or Einstein's General Theory of Relativity.


