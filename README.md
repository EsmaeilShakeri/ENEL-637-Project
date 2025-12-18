# ENEL-637-Project
# Residue Number Systems for Matrix Multiplication

This project investigates **Residue Number Systems (RNS)** for accelerating large-scale **matrix multiplication (MM)**.  
RNS enables **carry-free modular arithmetic** and parallel execution across residue channels, but introduces a conversion bottleneck due to **WNS ↔ RNS** encoding/decoding (notably CRT-based reconstruction). The goal is to quantify when the parallel MM gains outweigh conversion overhead for large matrix sizes.

**Course:** ENEL 637 (Fall 2025)  
**Instructor:** Prof. Dimitrov  
**Author:** Esmaeil Shakeri  
**Report date:** December 18, 2025

---

## Project Summary

- Uses **k = 4** parallel residue channels with moduli set **M = {127, 128, 129, 257}**.
- Models total RNS runtime as:
  \[
  T_{RNS} = T_{Encode} + T_{Core} + T_{Decode}.
  \]
- Demonstrates a **crossover point near N ≈ 350**, where RNS becomes faster than the baseline WNS implementation in the simulated timing model.

---

## What’s Included in This Repository

You can find the following materials in this repo:

- **Code**: Python simulation for WNS MM vs RNS MM timing (encode/core/decode)
- **Dataset**: CSV file containing raw timing results (used to generate the table/plots)
  - Example file name used in the report: `rns_data.csv`
- **Figures**: Plots used in the report (speedup curve and component-time analysis)
- **Report**: Final PDF/LaTeX source for the write-up

---

## Setup Instructions

### Step 1: Clone the Repository
```bash
git clone https://github.com/EsmaeilShakeri/ENEL-637-Project.git
cd ENEL-637-Project
