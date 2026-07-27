![](https://competition.aiforgood.itu.int/media/page_images/f2e5f561-52aa-4da4-b967-3a47bfc3e961.png)

#### Synesthesia of Machines (SoM) Challenge 2025
**Organized by:** PCNI
**Starts on:** Sep 30, 2025 2:00:00 AM CET (GMT + 2:00)  
**Ends on:** Feb 16, 2026 12:59:59 AM CET (GMT + 2:00)  
- wireless-communication
- machine-learning
- fine-tuning
- wireless-foundation-model

- [Overview](https://competition.aiforgood.itu.int/web/challenges/challenge-page/490/overview)
- [Evaluation](https://competition.aiforgood.itu.int/web/challenges/challenge-page/490/evaluation)
- [Phases](https://competition.aiforgood.itu.int/web/challenges/challenge-page/490/phases)
- [Participate](https://competition.aiforgood.itu.int/web/challenges/challenge-page/490/participate)
- [Leaderboard](https://competition.aiforgood.itu.int/web/challenges/challenge-page/490/leaderboard)

##### Challenge Overview

##### 

# 🏆Welcome to the SoM (Synesthesia of Machines) Challenge!
Enhancing AI-native multi-modal sensing–communication integration for future 6G networks with wireless foundation models.

🎯 Core Evaluation Dimensions

- 🔄**Transfer Learning** — efficiently leverage channel representations from the wireless foundation model to empower diverse CSI downstream tasks.
- 🧭**Generalization** — robust performance under scenario and data shifts.
- ⚡**Model Efficiency** — parameter efficiency and fast inference that meet real base-station and edge resource budgets.

**Why this challenge?**
We release the pre-trained wireless foundation model (WiFo) and invite participants to test its ability to flexibly, efficiently, and robustly support a variety of PHY-layer tasks, demonstrating how a single foundation model can simplify system design, enable practical deployment, and provide meaningful insights for the evolution of future sixth generation (6G) networks.![WiFo model architecture diagram](https://raw.githubusercontent.com/xuanyv/Imgs_Source/main/WiFo.png)Fig. 1. WiFo model architecture.

## 📘Introduction
To support future intelligent multifunctional 6G wireless communication networks, **Synesthesia of Machines (SoM)** is proposed as a novel paradigm for AI-native intelligent multi-modal sensing–communication integration.

![WiFo model architecture diagram](https://raw.githubusercontent.com/xuanyv/Imgs_Source/main/SoM.png)Fig. 2. An illustration of the SoM framework.As shown in Fig. 2, inspired by how synesthesia of human utilizes brain neural networks to process multi-sensory information for performing multiple cognitive tasks, the core of SoM processing lies in utilizing artificial neural networks (ANN) to handle multi-modal information for specific sensing and communication tasks. Here, we summarize three key characteristics of SoM processing below:
- **Multi-modal information:** SoM processing fully leverages communication and multi-modal sensing information covering multiple frequency bands.
- **Task-oriented:** SoM processing focuses on specific sensing and communication tasks to design targeted algorithms.
- **Artificial neural networks:** SoM processing conducts task-oriented and data-driven neural network design.
In summary, SoM refers to task-oriented AI-native intelligence integration of communication and multi-modal sensing. Specifically, to support the comprehensive design of SoM systems, five key research directions have been identified: multi-modal dataset construction for SoM, exploration of SoM mechanisms, SoM-enhanced transceiver design, SoM-enhanced cooperative perception, and network system support for SoM, with their interrelationships illustrated in Fig. 2. However, existing SoM system designs rely on task-specific AI models and face the following limitations:
- **Insufficient performance:** Most models are small-scale deep learning networks with limited capacity, inadequate for highly dynamic environments and complex PHY-layer tasks.
- **Limited generalization:** Distribution shifts in channel data require retraining, hindering rapid deployment.
- **Separated design:** Each PHY module is designed independently, increasing storage, computation, and management overhead at the base station.
Recently, domain-specific **wireless foundation models** have emerged as a new paradigm. A wireless foundation model is pre-trained on broad wireless (and optional multi-modal sensing) data at scale using self-supervision, and can adapt to a wide range of SoM tasks via few-/zero-shot learning. Compared with task-specific models, the pre-training paradigm and scale effects bring stronger generalization and a unified architecture.

The first wireless foundation model for channel prediction, **WiFo**, demonstrates strong time-/frequency-domain channel prediction and zero-shot generalization across systems and data. Its masked self-supervised training provides powerful CSI representations, enabling *one model for multiple tasks* with improved performance and simpler deployment.

## 🧪Problem Statement
We select three representative CSI-related SoM tasks—**channel estimation**, **LoS/NLoS classification**, and **vision-aided wireless localization**—to thoroughly evaluate the WiFo-based SoM design.

### 📡Task 1: Channel Estimation
**Task Description:** The UE is equipped with a single antenna, while the base station is equipped with multiple antennas. We consider uplink channel estimation, where the goal is to recover the complete CSI from sparsely placed pilot signals in the time-frequency resource grid. Sparse pilot placement can improve spectral efficiency, but it also increases the challenge of the problem.

**Task Input:** The CSI at the pilot positions of the time-frequency resource block for each transmit-receive antenna pair.

**Task Output:** The complete channel tensor  for each TX–RX pair, where  is the number of OFDM symbols,  antennas, and  subcarriers.

**Notation:**  denotes the *ground-truth* CSI of the resource block, and  denotes the *estimated* CSI reconstructed from sparse pilots.

**Metric (NMSE):**

### 🛰️Task 2: LoS/NLoS Scenario Classification
**Task Description:** The classification of Line-of-Sight (LoS) and Non-Line-of-Sight (NLoS) scenarios is critically important for the design of communication systems—impacting the choice of algorithms such as precoding. In this case, we determine the scenario type by analyzing CSI samples.

**Task Input:** A 2D CSI sample where  and  denote the numbers of subcarriers and antennas.

**Task Output:** Scenario label: LoS or NLoS.

**Notation:**  (True Positive): correctly predicts the LoS class;  (False Positive): predicts LoS when it is actually NLoS;  (False Negative): predicts NLoS when it is actually LoS.

**Metric:** Precision, Recall, and F1 score:

### 🗺️Task 3: Vision-aided Wireless Localization
**Task Description:** In densely built outdoor environments or complex indoor settings, GPS-based positioning often suffers from poor accuracy or complete unavailability. To overcome these limitations, this task focuses on estimating the user's two-dimensional location by leveraging both the wireless channel information between the base station(s) and the user device, and the RGB image captured at the base station. The goal is to exploit the latent correlation between wireless and visual modalities for improved localization accuracy and robustness in challenging environments.

**Task Input:**  where  is the number of subcarriers and  the number of transmit antennas; plus an RGB image from the base station’s perspective.

**Task Output:** User location .

**Notation:**  denotes the *ground-truth* user location, and  denotes the *estimated* user location.

**Metric (MAE):**

## 📦Data Source

1. **Pre-training Dataset**WiFo-Base is pretrained on 16 unlabeled wireless channel datasets that cover a wide range of scenarios, including diverse antenna configurations, carrier frequencies, and user mobility patterns. These datasets are generated using the QuaDRiGa simulator in compliance with the 3GPP 38.901 standard (details in [1]). Through this large-scale pretraining, WiFo-Base learns generalized channel characteristics, demonstrating strong zero-shot generalization across unseen environments and frequency bands. We expect—and invite participants to verify—that WiFo-Base also exhibits cross-task transferability.

*Additional allowance.* Participants may further pretrain WiFo-Base on additional unlabeled datasets to enhance generalization and overall performance.
2. **Downstream Training Dataset** [[download link](https://huggingface.co/datasets/PPASS/som2025/tree/main)]Dedicated datasets will be provided for each downstream task to fine-tune WiFo-Base. Each task dataset includes a training set, a validation set, a public test set, and a hidden challenge test set (the latter two without ground-truth labels).

1. **Training set** is for model optimization. Reasonable data augmentation is permitted and must be documented in the technical report.
2. **Validation set** is only for monitoring performance and early stopping, not for training.
3. **Public test set** is for evaluation only and *must not* be used for training or fine-tuning.
4. **Hidden challenge test set** is reserved for internal evaluation by the organizers and determines the final leaderboard rankings.
3. **Strict Rule on Downstream Training**It is strictly prohibited to fine-tune WiFo-Base on any external datasets for downstream tasks. Violations will result in immediate disqualification.
4. **Robustness Considerations**To assess generalization and robustness, both public and hidden challenge test sets include out-of-distribution (OOD) samples that simulate real-world wireless variations. This emphasizes learning robust, transferable representations rather than overfitting to specific scenarios.

## 📂Resources
Besides the dataset, complementary material will be provided to participants, including references, detailed instructions, and guidelines:

- **Baseline Codes: **[https://github.com/xuanyv/SoM2025-baseline](https://github.com/xuanyv/SoM2025-baseline)Recommended Start The baseline for all three tasks. You can run it out-of-the-box to obtain strong reference results and then customize or fine-tune on top of it, saving a lot of engineering effort.
- **Pre-trained Weights:** [https://huggingface.co/liuboxun/WiFo/tree/main](https://huggingface.co/liuboxun/WiFo/tree/main)
- **Inference Codes:** [https://github.com/liuboxun/WiFo](https://github.com/liuboxun/WiFo)
- **Other Fine-tuning Codes:** [https://github.com/liuboxun/LLM4CP](https://github.com/liuboxun/LLM4CP); [https://github.com/xuanyv/LLM4WM](https://github.com/xuanyv/LLM4WM)

## ⏰Deadlines
📝Registration Deadline:Until **~~15 December 2025~~** **31 December 2025**
📤Development Phase deadline:**1 February 2026**
🧮Final Evaluation Period:Until **10 February 2026**
