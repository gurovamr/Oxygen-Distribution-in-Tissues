# Oxygen Distribution in Tissues

This repository contains a numerical solution of a one-dimensional **reaction–diffusion equation** modeling oxygen transport in biological tissue.  
The implementation corresponds to **Task 4: Oxygen Distribution in Tissues** from the Mechanistic Modelling project.

---

## Model

The oxygen concentration \(O(x,t)\) is described by the PDE

$$
\frac{\partial O}{\partial t} = D \nabla^2 O - \mu O + S
$$

where:
- **D** – diffusion coefficient  
- **μ** – oxygen consumption rate  
- **S** – external oxygen supply  

The spatial domain is one-dimensional and discretised using a uniform grid.

---

## Numerical Methods

The PDE is solved using finite difference approximations:

- Central differences in space  
- Time integration using:
  - Explicit Forward Euler
  - Implicit Backward Euler
  - Crank–Nicolson scheme  

### Boundary Conditions
- Left boundary: Dirichlet condition (constant oxygen supply)
- Right boundary: Neumann no-flux condition

### Initial Condition
- Near-equilibrium oxygen concentration with a local 30% reduction in the center of the domain

### Stability Analysis and Parameter Study

- The stability of the explicit scheme is investigated by comparing time steps below and above the theoretical stability limit.
- The influence of model parameters (**D**, **μ**, **S**) on the oxygen profile is explored.

---

## Repository Contents

- `Solution.ipynb` – Jupyter notebook containing the full implementation, simulations and visualisations

---

## How to Run

1. Make sure Python 3 is installed.
2. Install required packages:
   ```bash
   pip install numpy matplotlib

---

## Contibutors

ACLS Students: Mariia Gurova & Pia Lagler