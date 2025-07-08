# FLIQ Innovation Track - Beyond the Seed: Randomness Redefined

## Overview

Randomness powers the digital world—from cryptography to simulations, gaming, and AI. But not all randomness is equal. In this challenge, we go **beyond the seed** to explore the distinctions, trade-offs, and applications of:

* **Pseudo-Random Number Generators (PRNGs)**
* **True Random Number Generators (TRNGs)**
* **Quantum Random Number Generators (QRNGs)**

You’ll dive into how each works, how they fail, and how quantum mechanics reshapes our understanding of unpredictability.

### Why It Matters

In 2006, a bug in Debian’s OpenSSL package weakened its PRNG so severely that attackers could reproduce private keys and breach encrypted systems.

From encryption and simulations to AI fairness and online gambling security, RNGs influence almost every field of computing. Whether it’s simulating particles or protecting messages, understanding the strengths and weaknesses of different randomness sources is a **foundational skill for quantum-era computing.**

### What You’ll Learn

* The theory and implementation of PRNGs, TRNGs, and QRNGs
* The concept of **entropy** as a computational resource
* Cryptographic randomness standards (e.g., **NIST SP 800-22**, **Dieharder**)
* Python-based **statistical testing** and **QRNG API** integration
* Real-world failures caused by weak randomness—and how to prevent them

### Challenge Curators

![fig](fig1.png) ![fig](fig2.png)

### Difficulty Level

Advanced

## Challenge Tasks

### Tasks 1–3: Build, Compare, Benchmark

You’ll implement PRNGs, TRNGs, and interact with a live quantum randomness API (QRNGaaS) from ID Quantique. Along the way, you’ll:

* Analyze entropy decay and correlation in PRNGs
* Explore physical entropy in TRNGs
* Benchmark randomness quality using statistical tools
* Learn to interface with real-world randomness APIs

### Task 4: Create Something New

An open-ended design challenge: develop a **use case or application where quantum randomness truly shines**. This could be in:

* Cryptography
* Simulation
* Art
* Games
* Or something totally new—innovation is the goal. Surprise us.

### Getting Started

Python starter templates are provided for Tasks 1–3. You’re encouraged to:

* Review the **Introduction** and **Mathematical Background** sections
* Don’t be discouraged by the math—we’ve added **intuitive explanations** for every formula
* Explore the **Debian OpenSSL bug** and other real-world examples to spark ideas

### Github Repository

We have provided some starter code for the challenge here:
[https://github.com/88Mangos/CMU-x-IDQuantique-Challenge](https://github.com/88Mangos/CMU-x-IDQuantique-Challenge)

## Evaluation Criteria

Submissions will be judged primarily on technical soundness and originality, but we will also consider clarity of explanation, relevance to the topic of random number generation, and the depth of engagement with quantum randomness as a computational resource.

Justifying the quantum advantage in random number generation is a nontrivial task—one that even researchers at leading companies like ID Quantique continue to investigate. So, if you find it challenging, you’re not alone. Most arguments for QRNGs are grounded in theoretical physics, relying on the fundamental unpredictability of quantum measurements. However, if you want to strengthen your case in practice, consider empirical validation using statistical test suites such as TestU01, Dieharder, and NIST SP 800-22. Alternatively, you can design and demonstrate a protocol or cryptographic scheme where a QRNG offers measurable resilience or security benefits over traditional PRNGs or TRNGs.

## Submitting Your Work

Include your write-up in this notebook or submit it as a **PDF, Google Doc, or LaTeX report** in the repo.

For Task 4, **clarity, creativity, and originality** are key.

Completion of Tasks 1–3 is highly recommended and may influence judging in the event of a tie.

## Resources

### Pre-FLIQ Workshop

* [**From theory to practice: Understanding the quantum technology pipeline**](https://www.youtube.com/watch?v=TuLt7CEuWds); Qiang Zhang, USTC

### Reading Material

* [1] Constantin, L. Debian’s OpenSSL bug still haunts the internet. [https://www.cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2008-0166](https://www.cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2008-0166), 2008.
* [2] Information Technology Laboratory. Advanced Encryption Standard (AES). Tech. rep. FIPS 197. National Institute of Standards and Technology (2001).
* [3] L’Ecuyer, P. and Simard, R. “TestU01: A C library for empirical testing of random number generators.” ACM Transactions on Mathematical Software (TOMS) 33 (2007), 1–40.
* [4] Geeting, D. B. “Russians Engineer a Brilliant Slot Machine Cheat—And Casinos Have No Fix.” WIRED (2017). Accessed: 2025-05-07.
* [5] Marsaglia, G. Xorshift RNGs. Online: [http://www.jstatsoft.org/v08/i14/paper](http://www.jstatsoft.org/v08/i14/paper). Posted to comp.lang.c Usenet group. (2003).
* [6] O’Neill, M. E. “PCG: A family of simple fast space-efficient statistically good algorithms for random number generation.” In: Proceedings of the ACM SIGPLAN Symposium on Principles and Practice of Parallel Programming (2014).
* [7] Vigna, S. An experimental exploration of Marsaglia’s xorshift generators, scrambled. arXiv preprint arXiv:1402.6246. (2015).
* [8] Li, M. and Vitányi, P. An Introduction to Kolmogorov Complexity and Its Applications. Springer (2008).
* [9] ID Quantique. Quantum versus Classical Random Number Generators. Tech. rep. ID Quantique SA (2023).
* [10] Bell, J. S. “On the Einstein Podolsky Rosen Paradox.” Physics Physique Fizika 1 (1964), 195–200.
* [11] Maundrill, M. SK Telecom unveils the Samsung Galaxy Quantum 5. (2024).
* [12] IDQuantique. Random Number Generation White Paper. (2023).
* [13] GeeksforGeeks. Estimating the value of pi using Monte Carlo. (2022).

# Prizes

**Best solution in this challenge**
* USD 500 awarded to the top-performing solution based on evaluation criteria.

**Overall Innovation track winner**
* USD 1,000 awarded to the top-performing solution of the Innovation track and a travel grant to present the winning project at the Quantum for Good track of the AI for Good Global Summit.

For team submissions, cash prizes will be awarded per submission and the travel grant will cover one representative (selected by the team).

---

# Contact

Please utilize the innovation track channel in the [FLIQ Discord](https://discord.gg/7xNepHFwXW) for any questions. 

**Art challenge creators:**
* Florian Fröwis (ID Quantique)
* Tyler Yang (QC @ CMU)
* Rhik Mazumder (QC @ CMU)
*(These creators will try to be active there.)*