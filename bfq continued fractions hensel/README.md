# Binary Quadratic Forms, Continued Fractions & Hensel Lifting in Maxima

A Maxima implementation of **binary quadratic form reduction**, **continued fraction expansions**, and **Hensel lifting**. These are classical tools in **computational number theory** with **direct applications in cryptanalysis** — particularly against RSA (Wiener's attack), in class group cryptosystems (Buchmann), and in modern lattice-based methods (Coppersmith, NTRU).

## 👥 Team "ModMax"

| Member | Primary Contributions |
|--------|----------------------|
| **Nadia Afsar** | **Q2 parts 1–2 (`cfr`, `cfr_periodic`)** |
| Sara Mohammadi Mohammadi | Q2 parts 3–4 (`cfr_best_approx`, `pell`) |
| Kian Hassanzadeh | Q1 (Binary Quadratic Forms, parts 1–4) |
| Kosar Kheradmand | Q3 (`hensel_lifting`) |

> **Note:** While each member led specific questions, all team members contributed to debugging, algorithm design, and code review throughout the project.

## 📋 Implemented Exercises

| # | Topic | Key Functions |
|---|-------|---------------|
| **1** | **Binary Quadratic Forms (BQF)** ⭐ | `bqf_red_step`, `bqf_red`, `cipolla`, `bqf_primeform`, `bqf_solve` |
| **2** | **Continued Fractions** ⭐ (parts 1–2) | `cfr`, `cfr_periodic` (also `cfr_best_approx`, `pell`) |
| 3 | **Hensel Lifting** | `hensel_lifting` |

⭐ = Implemented by Nadia Afsar

## 🔍 Detailed Contributions

### Question 2 — Continued Fractions (Parts 1–2 Implemented by Nadia Afsar)

#### (1) `cfr(x, n)` — Partial Quotients
Computes the first `n` partial quotients of the continued fraction expansion of `x` using the standard recurrence. Uses `bfloat` with increased precision (`fpprec = 4n`) to handle irrationals like `√2` and `π`. If the expansion terminates before `n` terms, returns the complete (finite) expansion.
