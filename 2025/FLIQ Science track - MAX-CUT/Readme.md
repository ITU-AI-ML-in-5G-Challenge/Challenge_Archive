# FLIQ Science Track - MAX-CUT: Ground State at Minimum Cost

## Challenge Overview

## Description

### Introduction

Max-Cut is often considered the "hello world" of quantum optimization. It is simple to state, NP-hard to solve, and naturally expressible as an Ising Hamiltonian. Given a graph $G = (V, E)$, the objective is to partition the vertices ($V$) into two sets (commonly labeled as +1 and -1, or "black" and "white") such that the number of edges ($E$) connecting vertices in different sets—known as the **cut size**—is maximized.

Encoding this cost function into Pauli-$Z$ operators provides a perfect environment for exploring modern NISQ (Noisy Intermediate-Scale Quantum) algorithms. Max-Cut serves as an ideal benchmark for several key reasons:

* **Universality**: Max-Cut can encode many practically relevant computational problems.
* **Scalability**: Instances can be created at any size, allowing for the investigation of quantum advantage thresholds.
* **Verifiability**: Solutions can be efficiently checked using classical methods.
* **Hardware-friendly**: The Ising model directly maps to the architecture of actual quantum processors.

This challenge is part of the **Science Track**, which aims to expose participants to technical and scientific problem-solving across the quantum stack.
![fig](maxcutimage.png)
**Challenge Curators**: 
![fig](ionq.png)
**Difficulty Level**: Advanced


# Challenge Statement

You will receive a fully-worked Jupyter notebook that serves as the foundation for your solution. This notebook includes:

* **MaxCut Hamiltonian Construction**: A function `build_maxcut_hamiltonian(graph)` that implements the transformation:

    $$ H  = \frac{|E|}{2}I - \frac{1}{2} \sum_{(i,j) \in E} Z_i Z_j $$

    where $|E|$ is the number of edges in the graph, $I$ is the identity operator, and $Z_i$ denotes the Pauli-$Z$ operator acting on qubit $i$.

* **Variational Quantum Imaginary Time Evolution (varQITE)**: A class `QITEvolver` implementing a state-of-the-art algorithm for finding ground states. This approach simulates imaginary time evolution:

    $$ \left| \psi(\tau) \right\rangle = \frac{e^{-\tau H} \left| \psi(0) \right\rangle}{\left\| e^{-\tau H} \left| \psi(0) \right\rangle \right\|}
 $$

    using variational principles to efficiently approximate this evolution on NISQ hardware.

* **Utility functions**

## Your Mission

Your task consists of four interconnected challenges:

### 1. Ansatz Engineering

Design a parameterized quantum circuit $U(\theta)$ that can capture MaxCut ground states while minimizing both the circuit depth $D_{\text{circuit}}$ and CNOT count $N_{\text{CNOT}}$. Your ansatz should:

* **Scale efficiently** with graph size and connectivity.
* **Maintain expressibility** sufficient to represent MaxCut solutions.
* **Exploit problem symmetries** where possible.

Consider various ansatz families including:

* Hardware-efficient ansätze (HEA)
* Symmetry-preserving ansätze
* Adaptive/iterative circuit construction

### 2. Algorithm Tuning

Integrate your ansatz with the provided `QITEvolver` class and optimize the learning process. This includes:

* **Hyperparameter Optimization**: Select optimal values for:
    * Learning rate (possibly with scheduling)
    * Imaginary time step size $\Delta\tau$
    * Total evolution time $\tau_{\text{max}}$
    * Convergence criteria
* **Optimization Improvements**: Consider modifications to the standard varQITE approach:
    * Alternative classical optimizers (SPSA, natural gradient, etc.)
    * Parameter initialization strategies
    * Regularization techniques
    * Shot allocation optimization

# Evaluation Criteria: 

A critical aspect of this challenge is not just finding a single optimal solution, but characterizing the full solution space through proper sampling. Your final score will be significantly influenced by your ability to generate a representative distribution of all optimal solutions.

## Solution Space Characterization

For each graph instance, you must provide:

* A histogram showing the distribution of bit strings representing all optimal solutions.
* Statistical analysis of the solution space diversity.
* Verification that your quantum algorithm samples from the solution space with the correct theoretical probabilities.
![fig](solution.png)

# Prizes

## Best Solution in This Challenge

* **USD 500** awarded to the top-performing solution based on evaluation criteria.

## Overall Science Track Winner

* **USD 1,000** awarded to the top-performing solution of the Science track.
* A travel grant to present the winning project at the Quantum for Good track of the AI for Good Global Summit.

For team submissions, cash prizes will be awarded per submission, and the travel grant will cover one representative (selected by the team).

# Contact

* **Vadim Karpusenko**, IonQ: karpusenko@ionq.co
* **David Nizovsky**, Vanderbilt Quantum Initiative: david.nizovsky@vanderbilt.edu
* **ITU**: quantum@itu.int