# grover_3bit_password
Find the correct password with the minimum number of checks using Grover Search algorithm
# Grover's Algorithm: Cracking a 3-bit Binary Password

## Problem Statement

A secure system uses a 3-bit binary password (values from `000` to `111`, i.e., 0-7 in decimal). We do **not** know the password, but we have access to a "black box" (quantum oracle) that tells us if a guess is correct (`YES`) or not (`NO`). 

Our goal: **Find the correct password with the minimum number of checks** (oracle calls).

---

## Classical vs Quantum Search

- **Classical search:** To guarantee finding the right password, we might have to check all 8 possibilities (worst case).
- **Quantum search (Grover's Algorithm):** Can find the password with high probability using only about √8 ≈ 2.8 (~2 or 3) oracle calls.

---

## Grover’s Algorithm Overview

Grover's algorithm is a quantum algorithm for searching an unsorted database with N entries in O(√N) time. For our 3-bit password (N=8), this is a huge speedup!

**Steps:**
1. **Initialize** a superposition of all possible states (passwords).
2. **Oracle:** Flips the phase of the correct password state.
3. **Diffusion (Amplification):** Increases the probability of the correct state.
4. **Repeat** (about ⌊π/4 × √N⌋ times).
5. **Measure** — high chance to get the correct password.

---

## This Project

- **Theory:** Explanation of Grover’s algorithm and its advantage.
- **Code:** Step-by-step implementation for the 3-bit password problem using Qiskit (IBM’s quantum computing library).
- **Visualization:** Statevector and measurement results.
- **Experiment:** Demonstrate the probability of success with different numbers of Grover iterations.

---

## Files

- `README.md` — This file.
- `grover_3bit_password.ipynb` — Jupyter notebook with theory, code, and results.
- `requirements.txt` — Python dependencies.

---

## References

- [IBM Qiskit Textbook: Grover's Algorithm](https://qiskit.org/textbook/ch-algorithms/grover.html)
- [Grover's Algorithm (Wikipedia)](https://en.wikipedia.org/wiki/Grover%27s_algorithm)
