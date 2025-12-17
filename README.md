# Quantum Approximate Optimization for LUT Cut Selection in Logic DAGs

## ⚛️ Overview
This project explores the intersection of quantum computing and Electronic Design Automation (EDA) by formulating FPGA Lookup Table (LUT) cut selection as a Quadratic Unconstrained Binary Optimization (QUBO) problem.

Mapping Boolean logic networks to FPGA LUTs requires selecting a consistent set of k-feasible cuts across a directed acyclic graph (DAG). In this work, we study how the Quantum Approximate Optimization Algorithm (QAOA) performs on these structured instances compared to classical mapping heuristics.

## 🧪 Key Features
* **QUBO Formulation:** Developed three models to encode mapping constraints:
    * **Model A:** Enforces legality (exactly one cut per node).
    * **Model B:** Adds depth penalties to bias towards shallower logic (timing optimization).
    * **Model C:** Penalizes logic duplication to reduce area.
* **Ising Mapping:** Mapped QUBO models to Ising Hamiltonians suitable for QAOA.
* **Custom Simulator:** Built a Python-based statevector simulator to overcome performance bottlenecks in standard libraries for these specific circuit instances.

## 🛠️ Technologies
* **Algorithm:** QAOA (Quantum Approximate Optimization Algorithm)
* **Stack:** Python, NumPy (Custom Statevector Simulation)
* **Optimization:** Nelder-Mead Classical Optimizer
* **Benchmarks:** 1-bit Full Adder, Reduced 2-bit Ripple-Carry Adder

## 📊 Results
* **Energy Landscapes:** Demonstrated smooth optimization landscapes for depth-biased models.
* **Performance:** Observed strong probability concentration on low-energy solutions even at shallow circuit depths (p=1, 2).
* **Degeneracy:** Successfully characterized how increasing circuit depth helps resolve degenerate ground states in area-optimized models.

## 📄 Reference
[**Read the Final Report (PDF)**](./6_2400_Final_Paper.pdf)
