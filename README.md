# Number Theory & Cryptanalysis in Maxima

A Maxima implementation of classical number theory algorithms with **direct applications in cryptanalysis and modern cryptography**. Covers Gaussian integer arithmetic, factoring algorithms (Pollard's ρ and p−1), binary quadratic forms, continued fractions, the Pell equation, and Hensel lifting.

## 📖 Overview

This repository contains two comprehensive number theory homework assignments, both implemented in **Maxima** (Computer Algebra System). Together they cover:

- Gaussian integers `Z[i]`, linear congruential generators, Pollard's ρ and Pollard's p−1 factoring methods.
- Binary quadratic form reduction, continued fractions, best rational approximations, Pell equation, and Hensel lifting.

These algorithms are not just mathematical curiosities — they are **the tools of classical cryptanalysis** (Wiener's attack on RSA, Buchmann's class group cryptosystem, Coppersmith's method) and **the foundation of modern lattice-based cryptography** (NTRU, Ring-LWE).

## 🔍 Summary of My Contributions

### Gaussian Integers & Factoring
- **Q2: Linear Congruential Generators (LCG)** — Full implementation of `lcg_random_parameters`, `lcg_nextrand`, `lcg_rand`, `lcg_list`, and `verify`. Constructed parameters `a` and `c` directly from the prime factorization of `m` using the **Hull–Dobell theorem**, rather than by random trial-and-error.

### BQF, Continued Fractions & Hensel Lifting
- **Q2 parts 1–2: Continued Fractions** — `cfr` (partial quotients for rationals and irrationals) and `cfr_periodic` (periodic expansion of quadratic irrationals via Lagrange's algorithm).

For the remaining exercises, I contributed to **algorithm design**, **debugging**, and **code review** — especially in the Pollard factoring algorithms and the Pell equation solver.

---

## ✨ Cross-Project Highlights

### 1. Operations over Gaussian Integers
Gaussian integer arithmetic is the **algebraic foundation** of:
- **NTRU** and **Ring-LWE** (lattice-based cryptography)
- **Buchmann's class group cryptosystem** (which operates on ideals in `Z[√−d]`)

### 2. Pollard's Factoring Algorithms
Both `pollard_rho` and `pollard_pm1` are **real cryptanalytic tools**:
- `pollard_rho` is a **general-purpose factoring algorithm** used against RSA moduli with small factors.
- `pollard_pm1` is an **RSA attack** targeting primes `p` where `p − 1` is smooth.

### 3. Binary Quadratic Forms
BQF reduction is the **core operation** of:
- **Buchmann's class group cryptosystem** (one of the earliest post-quantum proposals)
- **Quadratic Sieve** and **Number Field Sieve** factoring algorithms

### 4. Continued Fractions
Continued fractions are the foundation of **Wiener's attack on RSA** — the classical attack that recovers the RSA private key `d` when `d < N^(1/4)`.

### 5. Hensel Lifting
Hensel lifting is the **p-adic analogue** of Newton's method, and it is the key tool in:
- **Coppersmith's method** for finding small roots of modular polynomials
- **NTRU** decryption
- **p-adic cryptography**

---

## 🛠️ Technologies

- **Tool:** Maxima (Computer Algebra System)
- **Language:** Maxima script (`.mac` files)
- **Concepts:** Gaussian integers, modular arithmetic, Chinese Remainder Theorem, PRNGs, factoring algorithms, binary quadratic forms, continued fractions, Pell equation, p-adic lifting

