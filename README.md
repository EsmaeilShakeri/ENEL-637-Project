# ENEL-637-Project
# Residue Number Systems for Matrix Multiplications

This repository contains the code and report for my ENEL 637 course project at the University of Calgary.  
The project explores how **Residue Number Systems (RNS)** can be used to implement matrix multiplication with
improved parallelism and reduced carry-propagation compared to standard binary arithmetic.

---

## Project Overview

The main goals of this project are to:

- Implement matrix multiplication in an RNS framework.
- Compare RNS-based multiplication against conventional (binary) matrix multiplication in terms of:
  - Numerical correctness
  - Execution time / scalability
  - Dynamic range and overflow behaviour
- Illustrate the complete pipeline:
  1. Mapping integers to RNS representation  
  2. Element-wise operations in parallel residue channels  
  3. Reconstruction via the Chinese Remainder Theorem (CRT)  
  4. Matrix-level evaluation and error analysis

The repository includes both the **Python implementation** and the **project report** in PDF format.

---

## Repository Structure

```text
ENEL-637-Project/
├── src/
│   ├── rns.py               # Core RNS representation and conversion utilities
│   ├── rns_matrix_ops.py    # RNS-based matrix multiplication functions
│   ├── baseline_matrix_ops.py  # Standard (binary) matrix multiplication for comparison
│   └── experiments.py       # Scripts to run experiments and generate figures
├── notebooks/
│   └── demo_rns_multiplication.ipynb   # Example Jupyter notebook (optional)
├── report/
│   └── ENEL637_RNS_MatrixMultiplications_Report.pdf
├── tests/
│   └── test_rns_correctness.py        # Basic unit tests (optional)
├── README.md
└── requirements.txt
