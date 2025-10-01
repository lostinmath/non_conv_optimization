# Consensus-Based Optimization (CBO)

Python implementation of Consensus-Based Optimization for non-convex optimization problems.

## Overview

CBO is a multi-agent metaheuristic optimization method that leverages consensus dynamics to solve non-convex optimization problems. Unlike gradient-based methods, CBO can escape local minima through its particle dynamics and consensus mechanism, with theoretical guarantees for global convergence.

## Features

- Gradient-free optimization for non-convex functions
- Parallel particle dynamics with consensus updates
- Suitable for high-dimensional optimization problems
- Global convergence guarantees under appropriate conditions

## Installation
```bash
git clone https://github.com/lostinmath/non_conv_optimization.git
cd non_conv_optimization
pip install -r requirements.txt
Usage
pythonfrom cbo import ConsensusBasedOptimizer

# Define your objective function
def objective(x):
    return sum(x**2)  # Example: simple quadratic

# Initialize and run optimizer
optimizer = ConsensusBasedOptimizer(
    n_particles=100,
    dimension=10,
    max_iterations=1000
)
result = optimizer.optimize(objective)
print(f"Optimal solution: {result}")
References
This implementation is based on the following papers:

Fornasier, M., Klock, T., & Riedl, K. (2020). Consensus-based optimization methods converge globally. arXiv preprint arXiv:2005.05249.
Fornasier, M., Huang, H., Pareschi, L., & Sünnen, P. (2021). Consensus-based optimization on the sphere: Convergence to global minimizers and machine learning. Journal of Machine Learning Research, 22(237), 1-55. https://jmlr.org/papers/v22/21-0259.html
Ha, S. Y., Jin, S., & Kim, D. (2020). Convergence and error estimates for time-discrete consensus-based optimization algorithms. arXiv preprint arXiv:2006.07625.

License
MIT
