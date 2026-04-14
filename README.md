# Variational Quantum Eigensolver (VQE) for HeH+ Ion

## Description

This Jupyter notebook implements the Variational Quantum Eigensolver (VQE) algorithm to estimate the ground state energy of the HeH+ ion using quantum computing. The implementation uses PennyLane, a quantum machine learning library, to perform quantum chemistry calculations.

The notebook constructs the molecular Hamiltonian for HeH+ with a bond length of approximately 1.46 Bohr radii (0.774 Å), and uses a simple ansatz consisting of an initial basis state preparation and a double excitation gate to optimize the energy.

## Prerequisites

- Python 3.x
- PennyLane (quantum machine learning library)
- NumPy (automatically included with PennyLane)

## Installation

Install the required packages using pip:

```bash
pip install pennylane
```

## Usage

1. Open the notebook `VQE.ipynb` in Jupyter Lab or Jupyter Notebook.
2. Execute the cells in sequential order.
3. The notebook will perform the VQE optimization and output the estimated ground state energy of the HeH+ ion.

The optimization algorithm uses gradient descent with a step size of 0.4 and runs for up to 40 iterations or until convergence is reached (convergence tolerance: 1e-8 Hartrees).

## Key Components

- **Molecular Hamiltonian**: Generated using PennyLane's quantum chemistry module for HeH+ with charge +1.
- **Ansatz**: Simple variational circuit with basis state |1100⟩ and a parameterized double excitation gate.
- **Optimizer**: Gradient descent optimizer from PennyLane.
- **Device**: Default qubit simulator.

## Results

At the end of the optimization, the notebook prints:
- The final VQE energy in Hartrees
- The optimal parameter value for the ansatz
- The number of iterations required for convergence

## Notes

- This is a basic implementation for educational purposes.
- For more accurate results, consider using larger ansätze or different optimization methods.
- The bond length used (1.4626278 Bohr radii, approximately 0.774 Å) corresponds to an approximate equilibrium geometry for HeH+.