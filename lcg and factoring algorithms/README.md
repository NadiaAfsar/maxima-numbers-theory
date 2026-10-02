# Number Theory & Factoring in Maxima

A Maxima implementation of **Gaussian integer arithmetic**, **linear congruential generators**, and **two classical factoring algorithms** (Pollard's rho and Pollard's p−1). These are foundational tools in **computational number theory** with direct applications in **cryptanalysis**, especially against RSA.

## 👥 Team "ModMax"

| Member | Primary Contributions |
|--------|----------------------|
| **Nadia Afsar** | **Q2 (Linear Congruential Generators)** |
| Sara Mohammadi Mohammadi | Q4 (Pollard's p−1) |
| Kian Hassanzadeh | Q1 (Gaussian integers, functions 1–11) |
| Kosar Kheradmand | Q3 (Pollard's rho) |

> **Note:** While each member led specific questions, all team members contributed to debugging, algorithm design, and code review throughout the project.

## 📋 Implemented Exercises

| # | Topic | Key Functions |
|---|-------|---------------|
| 1 | **Gaussian Integers Z[i]** | `zi_gcd`, `zi_inv_mod`, `zi_lcm`, `zi_mod`, `zi_totient`, `zi_reduced_residues`, `zi_order`, `zi_power_mod`, `zi_max`, `zi_min`, `zi_primep`, `zi_chinese` |
| **2** | **Linear Congruential Generators** ⭐ | `lcg_random_parameters`, `lcg_nextrand`, `lcg_rand`, `lcg_list`, `verify` |
| 3 | **Pollard's ρ Method** | `pollard_rho` |
| 4 | **Pollard's p−1 Method** | `pollard_pm1` |

⭐ = Implemented by Nadia Afsar

## 🔍 Detailed Contributions

### Question 2 — Linear Congruential Generators (Implemented by Nadia Afsar)

A **Linear Congruential Generator (LCG)** is defined by the recurrence:
