# FLIQ Innovation Track - Quantum-Enhanced Machine Learning for Responsible AI

## Overview

Participants will apply **quantum machine learning** to distinguish between different phases of a Rydberg atom system using measurement data obtained in randomized bases.

This challenge is part of the **Innovation Track** whose aim is to encourage the exploration of cross-disciplinary applications that leverage quantum computing to drive social impact and demonstrate the transformative potential of quantum technologies.

### Challenge Curators

![alt text](image.png) ![alt text](image-1.png)

### Difficulty Level

Intermediate to Advanced

## Challenge Details

### Challenge Statement

In this challenge, participants will **enhance an AI/ML classifier or clusterer using Variational Quantum Algorithms (VQAs)**.

You will be provided with:
* A set of public datasets
* Starter code in the repository

Your mission: **Finish and innovate on the starter code** (or create your own approach) to develop quantum-enhanced machine learning models that meet the evaluation standards.

**Focus Areas:** Performance, explainability, fairness, security, robustness, and innovation.

### GitHub Repository

Challenge Repo: [https://github.com/UN-ICC/FLIQ-Virtual-Hackathon](https://github.com/UN-ICC/FLIQ-Virtual-Hackathon)

### Sample Code

Our sample code for a VQA classifier will be available in the GitHub Repository.
Use them as a foundation or as inspiration but don’t be afraid to innovate or try your own unique solution.

Keep in mind you will need to be using an environment capable of running `torch` or a similar ML library and `qiskit`. Additionally, as of 2025, `qiskit` has just moved to 2.x.x, meaning deprecated code is common and documentation/functionality can differ between versions.

### Datasets

Some datasets have been provided but feel free to propose additional datasets and justifications if so.

## Evaluation Criteria

| Category                      | Description                                                                    |
| :---------------------------- | :----------------------------------------------------------------------------- |
| **Performance Evaluation** | Measure Precision, Recall, F1-score, Accuracy; balance false positives and negatives. |
| **Fairness & Bias Detection** | Evaluate demographic fairness using metrics like Disparate Impact Ratio.         |
| **Adversarial Robustness Testing** | Test resilience against manipulated/adversarial inputs.                         |
| **Explainability & Interpretability Testing** | Provide understandable model decisions (e.g., SHAP, LIME, Counterfactuals). |
| **Privacy & Security Compliance** | Ensure data encryption, anonymization, GDPR/ISO compliance.                   |
| **Operational Reliability & Governance** | Maintain model stability, version control, governance for compliance.      |
| **Human-in-the-Loop Validation** | Allow human oversight: reviewing, overriding, validating AI outputs.             |
| **Innovation & Uniqueness** | Creativity and originality of your quantum-classical hybrid model.             |
| **Implementation Quality** | Code quality, structure, and efficiency.                                       |
| **Presentation & Understanding** | Clear explanation of approach, trade-offs, and insights.                       |



# Submission

Your submission must contain the code you used to train your model, model weights and a demo script if applicable (.pt files or similar is great), a write-up describing what you did and how you did it, and optionally a short video demo and presentation.

You are not required to use the sample code provided but please make a **public fork of the repository** for your submission.

Feel free to try any combination of classification, clustering, supervised/unsupervised learning, unique backpropagation techniques, quantum circuit designs, etc.

---

# Resources

## Introduction to Variational Algorithms

* [Introduction to Variational Algorithms - IBM Quantum](https://learning.quantum.ibm.com/course/variational-algorithm-design/variational-algorithms)
* [Quantum Machine Learning Algorithms - arXiv:2012.09265](https://arxiv.org/abs/2012.09265)
* [A Variational Algorithm for Quantum Neural Networks](https://link.springer.com/chapter/10.1007/978-3-030-50433-5_45)

---

# Prizes

**Best solution in this challenge**
* USD 500 awarded to the top-performing solution based on evaluation criteria.

**Overall Innovation track winner**
* USD 1,000 awarded to the top-performing solution of the Innovation track and a travel grant to present the winning project at the Quantum for Good track of the AI for Good Global Summit.

For team submissions, cash prizes will be awarded per submission and the travel grant will cover one representative (selected by the team).

---

# Final Notes

Try to push yourself, demonstrate your understanding, and write clean efficient code.

The ITU, UNICC and Quantum Coalition value safe, responsible, and humanitarian use of AI/ML, and heavily suggest you keep these values in mind as you develop and test your submission.

This challenge and all related submissions are intended for the benefit of all and must be submitted under the MIT License, or a similar open source license.

---

# Contact

Please utilize the innovation track channel in the [FLIQ Discord](https://discord.gg/7xNepHFwXW) for any questions. 

**The challenge creators:**
* [Anusha Dandapani, UNICC](https://challenge.aiforgood.itu.int/match/matchitem/dandapani@unicc.org)
* [Luke Sebold, Case Western](https://challenge.aiforgood.itu.int/match/matchitem/lts45@case.edu)
