# FLIQ Science track - Classifying quantum phases of matter
## Overview

Participants will apply **quantum machine learning** to distinguish between different phases of a Rydberg atom system using measurement data obtained in randomized bases.

This challenge is part of the **Science Track** whose aim is to expose participants to technical and scientific problem-solving across the quantum stack.

### Challenge Curators

![alt text](image.png)

### Difficulty Level

Advanced

## Challenge Summary

The task is to build a **Quantum Machine Learning (QML)** model capable of classifying different phases of quantum matter from measurement data.

Unlike typical datasets, your inputs are **classical shadows**: compressed representations of quantum states constructed via randomized measurements. Your model should learn to identify the phase label of a quantum state based only on this information.

## Your Task

Build a quantum circuit that:

* Takes as input reduced density matrices constructed from the measurement data.
* Outputs a prediction of the quantum phase.
* Is optimized for both accuracy and efficiency.

### GitHub Repository

In the challenge repo, which will become public at **16:00 UTC**, you can find the following files:

* `FLIQ_Challenge_ClassiqDuQIS.ipynb` – the notebook with code snippets, in which you will show your solution.
* `training_data.npz` – file with randomized measurements. There are 10 data points corresponding to each of the two phases studied.
* `phase_diagram.png` – Rydberg phase diagram for a 51-particle neutral atom array.

You can access the repo via [this link](https://github.com/dmitriikhitrin/Classiq-x-DuQIS-FLIQ-Challenge).

## Evaluation Criteria

Each submission will be scored using the function:

$f(A, P, D, W) = \alpha A - \beta P - \gamma D - \delta W$

Where:

* $A$: accuracy on the test set
* $P$: number of trainable parameters
* $D$: circuit depth
* $W$: number of qubits (circuit width)
* $\alpha, \beta, \gamma, \delta$: fixed positive constants

Higher values of $f$ indicate better solutions.

## Submission

In the challenge repo, you can find the following files:

* `FLIQ_Challenge_ClassiqDuQIS.ipynb` – the notebook with code snippets, in which you will show your solution.
* `training_data.npz` – file with randomized measurements. There are 10 data points corresponding to each of the two phases studied.
* `phase_diagram.png` – Rydberg phase diagram for a 51-particle neutral atom array.

You can access the repo via [this link](https://github.com/dmitriikhitrin/Classiq-x-DuQIS-FLIQ-Challenge).


# Resources

## Pre-FLIQ Workshops:

* [**Quantum computing 101**](https://www.youtube.com/live/yECsNsgUxL4); Zlatko Minev, CIFAR
* [**Quantum computing 102: Algorithms and applications**](https://www.youtube.com/live/cl02mRpeeU0); Hsin-Yuan Huang, CalTech
* [**Hands-on lab: Designing quantum algorithms with Classiq**](https://www.youtube.com/live/km-fHiphDtI); Nadav Ben-Ami, Classiq

## Reading Material

* [1] Hsin-Yuan Huang et al. “Provably efficient machine learning for quantum many-body problems”. In: Science 377.6613 (2022), eabk3333.
* [2] Hsin-Yuan Huang, Richard Kueng, and John Preskill. “Predicting many properties of a quantum system from very few measurements”. In: Nature Physics 16.10 (2020), pp. 1050–1057.
* [3] Sukin Sim, Peter D Johnson, and Alán Aspuru-Guzik. “Expressibility and entangling capability of parameterized quantum circuits for hybrid quantum-classical algorithms”. In: Advanced Quantum Technologies 2.12 (2019), p. 1900070.
* [4] Iris Cong, Soonwon Choi, and Mikhail D Lukin. “Quantum convolutional neural networks”. In: Nature Physics 15.12 (2019), pp. 1273–1278.

---

# Prizes

**Best solution in this challenge**
* USD 500 awarded to the top-performing solution based on evaluation criteria.

**Overall Science track winner**
* USD 1,000 awarded to the top-performing solution of the Science track and a travel grant to present the winning project at the Quantum for Good track of the AI for Good Global Summit.

For team submissions, cash prizes will be awarded per submission and the travel grant will cover one representative (selected by the team).

---

# Contact

Please utilize the science track channel in the [FLIQ Discord](https://discord.gg/7xNepHFwXW) for any questions. 

**The challenge creators:**
* [Nadav Ben Ami, Classiq](https://challenge.aiforgood.itu.int/match/matchitem/nadav.ben-ami@classiq.io)
* [Dmitrii Khitrin, DuQIS (Duke)](https://challenge.aiforgood.itu.int/match/matchitem/dmitrii.khitrin@duke.edu)
*(These creators will try to be active there.)*