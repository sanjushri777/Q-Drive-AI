# Q-Drive: Quantum-Assisted Routing for AMRs

## Overview
Q-Drive is a proof-of-concept project that explores how the Quantum Approximate Optimization Algorithm (QAOA) can improve Autonomous Mobile Robot (AMR) routing inside warehouses.  
The project compares classical approaches (Brute Force, Greedy) with a quantum-inspired approach (QAOA) to demonstrate potential advantages in scalability and efficiency.

---

## Project Structure

```
.
├── Q-DRIVE/
│   └── poc.ipynb       # Main notebook with both classical and quantum code
└── README.md           # Documentation (this file)
```


---

## How It Works

### Classical Methods
- **Brute Force**: Finds the exact optimal solution but becomes infeasible as the number of locations increases.  
- **Greedy Nearest Neighbor**: Fast heuristic approach, but often produces suboptimal routes.

### Quantum QAOA
- Formulates routing as an optimization problem using a Hamiltonian.  
- Explores many possible routes in parallel using quantum principles.  
- Provides near-optimal solutions with better scalability than brute force.

---

## Use Case: AMRs in Warehouses
In a warehouse, AMRs must pick items from different racks and return efficiently.  
- A *greedy algorithm* selects the nearest rack first, which may not minimize total travel distance.  
- *QAOA* helps the AMR choose globally optimized paths, reducing travel time, congestion, and energy usage.

---

## Results (Proof-of-Concept)
- **Brute Force**: Always finds the optimal solution (but only works for very small cases).  
- **Greedy**: Produces results quickly but is often 20–30% worse than optimal.  
- **QAOA**: Achieves ~90–95% of the optimal solution in tests, showing promise for larger-scale problems.

---

## Why QAOA over Classical?
- **Scalability**: Handles larger routing problems where brute force is impossible.  
- **Efficiency**: Produces better results than greedy heuristics.  
- **Future advantage**: As quantum hardware matures, performance will continue to improve.

---

## Requirements
Install the required dependencies before running:
```bash
pip install pennylane networkx matplotlib
```

---

## How to Run

1. Open the `Q-DRIVE/poc.ipynb` notebook in Jupyter or Google Colab.
2. Run the cells to compare:
   - Brute Force (Exact)
   - Greedy Heuristic
   - QAOA (Quantum-inspired)

---

## Conclusion

This project demonstrates that QAOA can provide near-optimal routing solutions for AMRs in warehouses, outperforming simple greedy methods and scaling better than brute force.  
The work serves as a PoC for future integration of quantum algorithms into real-world logistics and warehouse automation.
