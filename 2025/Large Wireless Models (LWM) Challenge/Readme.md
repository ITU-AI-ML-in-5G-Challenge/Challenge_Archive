# Large Wireless Models (LWM) Challenge

## Description

### Introduction
#### The Problem of Limited Data in Wireless Systems

Modern wireless networks, like 5G and 6G, need to solve complex problems to ensure fast and reliable communication. These problems require advanced models with many parameters, which usually need large amounts of labeled data to learn the detailed patterns in wireless channels. But in real-world settings, getting labeled data is difficult and expensive. Additionally, errors in channel estimates due to noise or poor approximations further degrade model performance. This creates a major challenge: we need models that can generalize from limited data and stay robust to imperfect inputs.
#### LWM Embeddings as a Starting Point
Large Wireless Model (LWM) is a transformer-based model trained on a large corpus of unlabeled wireless channel data using self-supervised learning. The result is a powerful encoder that generates context-aware channel embeddings. These embeddings consistently outperform raw channels in downstream tasks, particularly when training data is scarce. LWM captures robust patterns in the data, enabling better generalization and robustness to channel estimation noise.

#### Enhancing LWM for Better Generalizability
The goal of this challenge is to enhance the performance across multiple tasks using foundation models. While the default LWM performs well as a universal feature extractor, it can be improved through better loss functions, architectural modifications, or smarter pre-training strategies. The refined model should support complex wireless tasks under data constraints and noisy conditions. Can we enhance the overall system (LWM + downstream models) to achieve better performance across different downstream tasks using limited training data? That is the question this competition aims to answer.

#### Problem Statement
In this competition, participants will work with a pre-trained baseline Large Wireless Model (LWM) and default downstream models. The LWM processes wireless channel data of varying sizes and generates embeddings (feature representations) that feed into five downstream wireless communication tasks: (i) Robust LoS/NLoS classification, (ii) sub-6 GHz channel to mmWave beam prediction, (iii) channel interpolation, (iv) channel estimation, and (v) localization. The goal is to improve end-to-end performance across all five tasks by optimizing the LWM and/or designing new downstream models. Participants have flexibility in their approach and may refine the baseline LWM using large-scale custom datasets, propose entirely new LWM architectures, develop more effective downstream task-specific models, or combine any or all of these approaches. Limited training, validation, and test datasets are provided for each downstream task to guide the development and ensure the models generalize well. For the final evaluation, participants submit their trained LWM(s), downstream models, and training scripts to the organizers. The organizers will then train the submitted downstream models jointly on the provided datasets and evaluate them on hidden test sets. Each task generates its own performance score, and an aggregate composite score determines the overall competition ranking.

### Tasks
This competition evaluates the generalization and effectiveness of the Large Wireless Model (LWM) as a universal feature extractor across five key downstream tasks in wireless communications. For each task, participants are provided with training, validation, and test channel samples. While default downstream models are available, participants may also jointly optimize both the LWM and the downstream models—allowing end-to-end learning where the LWM is refined specifically to enhance performance on each task. In all cases, the downstream models are built on top of the LWM, which processes raw channel inputs into expressive embeddings that simplify learning and improve task efficiency. The downstream tasks are as follows:
#####  LoS/NLoS Classification
- Motivation: Distinguishing between line-of-sight (LoS) and non-line-of-sight (NLoS) conditions is vital for adapting transmission strategies in wireless systems, especially in urban and cluttered environments.
- Task: Classify each channel as LoS or NLoS. The LWM is expected to extract propagation-related features—such as delay spread, multipath signatures, or angular diversity—into embeddings (e.g., the CLS token) that enable accurate binary classification.
- Metric: F1-score, which balances precision and recall, especially under class imbalance.
#####  Sub-6 GHz Channel to mmWave Beam Prediction
- Motivation: Obtaining mmWave CSI is expensive due to the overhead of sounding and beam sweeping. Predicting optimal mmWave beams directly from sub-6 GHz channels can significantly reduce this cost.
- Task: Predict the best mmWave beam index from a given sub-6 GHz input using a fixed codebook. The LWM must distill spatial information from low-frequency channels that remains informative for higher-frequency beam alignment.
- Metric: Top-1 beam F1-score, indicating accuracy in predicting the correct strongest beam.
##### Channel Interpolation
- Motivation: In many scenarios, channel observations are incomplete due to efficiency constraints, hardware limitations, or intentional subsampling strategies. In such cases, entire transmit antennas or subcarriers may be missing. Interpolating these missing components is crucial for reconstructing full CSI and enabling downstream tasks.
- Task: Recover the missing elements of the channel matrix—where some antennas and subcarriers are entirely unobserved—using the contextual knowledge embedded by the LWM. The model must leverage spatial and frequency correlations to estimate unobserved values.
- Metric: Normalized Mean Squared Error (NMSE) between the reconstructed and ground-truth full channel.

#### Channel Estimation
- Motivation: Noisy channel measurements—especially under low SNR—can degrade performance. Leveraging a powerful prior via LWM embeddings helps denoise and reconstruct high-quality CSI.
- Task: Denoise imperfect CSI inputs and reconstruct clean channel representations through a downstream decoder operating on LWM embeddings.
- Metric: NMSE, assessing how well the reconstruction aligns with ground-truth channels.

##### Localization
- Motivation: Accurate user positioning supports intelligent beam management, mobility prediction, and context-aware services—especially in GPS-denied environments.
- Task: Predict the 2D (x-y) position of users from wireless channels. LWM must preserve geometric and propagation features that correlate with physical location, enabling the downstream model to regress accurate coordinates.
- Metric: Normalized localization error, measuring spatial accuracy relative to the scenario scale.
These tasks cover a broad spectrum of wireless objectives and require the LWM to extract and refine meaningful representations from input channels. Whether used as a fixed encoder or co-trained with downstream models, the LWM plays a central role in transforming complex channel data into efficient, structured embeddings that enable accurate and generalizable learning across tasks.


## Deadlines
- Challenge Package Release (Datasets and Scripts): To be announced (Participants will be notified directly)
- Registration Deadline: Until 23 August 2025
- Submission Deadline: 31 August 2025
- Final Evaluation Period: Until 06 September 2025

#### Organizers
This challenge is hosted by the Wireless Intelligence Lab at Arizona State University.

Co-organizers:

- [Sadjad Alikhani](https://scholar.google.com/citations?user=PKjnTR4AAAAJ&hl=en)
Graduate Research Associate, ASU

- [Gouranga Charan](https://scholar.google.com/citations?user=MHKcvFMAAAAJ&hl=en)
Postdoctoral Researcher, ASU

- [Ahmed Alkhateeb](https://scholar.google.com/citations?user=dLHw2qcAAAAJ&hl=en)
Director, Wireless Intelligence Lab
Associate Professor, ASU

## More Information
Please, find the more details about problem statement, tasks, baseline models, datasets, submission process, rules, and more at the [LWM website](https://lwm-wireless.net/challenge)


### Baseline Solution & Starter Script

---

#### Overview

This project focuses on refining the **LWM model** to produce embeddings that enhance performance across five distinct downstream wireless tasks. The final evaluation is conducted on hidden challenge samples from similar wireless environments, with no access to test labels during development.

We provide a **baseline pipeline** built on [**LWM 1.1**](https://huggingface.co/wi-lab/lwm-v1.1), a significantly improved version of the original model. LWM 1.1 offers several key advancements:

* **Variable Channel Size Support**: It removes fixed channel size limitations by supporting a variable number of antenna-subcarrier configurations via bucket-based batching and a flexible Transformer input structure.
* **Extensive Pre-training**: The model was pre-trained on over **1.3 million channel samples** from **20 diverse antenna-subcarrier setups** across multiple urban layouts, including higher-resolution user grids (1m spacing) and multiple base stations per scenario.
* **Enhanced Model Architecture**: LWM 1.1 introduces **larger embeddings (128D)**, a **higher masking ratio (40%)**, and **2D patch segmentation** to capture spatial-frequency relationships more effectively.
* **Improved Training**: Training benefits from **AdamW optimization** and a **cosine decay learning schedule with warmup**, which further enhance convergence and generalization.

These upgrades establish LWM 1.1 as a powerful and robust foundation for downstream wireless tasks.

---

#### Baseline Task Details

The LWM acts as a powerful and flexible feature extractor, generating rich embeddings from wireless channel inputs. In this baseline implementation, each downstream task leverages a tailored embedding and a lightweight, task-specific head.

Here are the key details for each task:

#### LoS/NLoS Classification

* **Score**: 0.784788
* **Input**: Full patch embeddings (flattened)
* **Loss Function**: CrossEntropy
* **Fine-Tuning**: LWM Layers 9–11
* **Description**: Classifies channels as line-of-sight (LoS) or non-line-of-sight (NLoS) using a lightweight classifier.

#### Beam Prediction

* **Score**: 0.663378
* **Input**: Mean-pooled embeddings
* **Loss Function**: CrossEntropy
* **Fine-Tuning**: Full LWM
* **Description**: Predicts the strongest mmWave beam index from sub-6 GHz channels.

#### Channel Interpolation

* **Score**: 0.407078
* **Input**: Channel embeddings (patch-wise)
* **Loss Function**: Mean Squared Error (MSE)
* **Fine-Tuning**: LWM Layers 10–11
* **Description**: Recovers missing antenna and subcarrier segments in incomplete channels.

#### Channel Estimation

* **Score**: 0.454136
* **Input**: Channel embeddings (patch-wise)
* **Loss Function**: Mean Squared Error (MSE)
* **Fine-Tuning**: LWM Layers 8–11
* **Description**: Denoises noisy CSI inputs and reconstructs clean channels using a deep FCN.

#### Channel Charting (Localization)

* **Score**: 0.648701
* **Input**: Mean-pooled embeddings
* **Loss Function**: Mean Squared Error (MSE)
* **Fine-Tuning**: LWM Layers 10–11
* **Description**: Regresses 2D user coordinates, learning the spatial layout from embeddings.

---

#### Beyond the Baseline

Participants are encouraged to innovate beyond the baseline by refining both the LWM architecture and the downstream task heads. Potential strategies include:

* **Pre-training**: Explore self-supervised or contrastive pre-training on large-scale channel datasets.
* **Architectural Improvements**: Consider enhancements in tokenization, attention mechanisms, or embedding design.
* **Smarter Token Selection**: Implement dynamic masking or spatially-aware importance sampling.
* **Task-Adaptive Tuning**: Utilize lightweight adapters, low-rank updates, or decoupled head optimization.
* **Task-Specific LWM Fine-Tuning**: Jointly optimize both the LWM and the corresponding downstream models using available limited task-specific datasets. This collaborative approach allows each LWM-downstream model pair to learn unique patterns and requirements, potentially achieving superior performance compared to using a single shared LWM.

Additionally, fine-tuning the baseline LWM on new unlabeled data can significantly improve embedding robustness and generalization. To support this, several new channel scenarios have been released via the **DeepMIMO v4 dataset**, available early to competition participants for extended pre-training and fine-tuning.

All improvements should prioritize **robustness to noise, sparsity, and domain shift**, as the final hidden test set includes challenging and partially out-of-distribution samples. To ensure fairness, all submissions are retrained using only the provided training and validation sets, and **final evaluations are performed by the organizers on a controlled infrastructure**. Test labels are never exposed during the competition.
# Evaluation Criteria

---

## Composite Generalization Score (CG-Score)

The primary evaluation metric for this challenge is the **Composite Generalization Score (CG-Score)**. This score reflects the overall performance and generalization ability of a participant’s refined LWM model across all five downstream tasks. Each task is evaluated using a **task-specific metric**, and scores are **normalized to the range [0, 1]** for fair aggregation.

---

## Task-Specific Scoring

### LoS/NLoS Classification

* **Metric**: F1-Score (binary classification)
* **Range**: [0, 1]
* **Description**: Measures the balance between precision and recall in classifying line-of-sight vs. non-line-of-sight channels.

### Sub-6 GHz to mmWave Beam Prediction

* **Metric**: F1-Score (multi-class classification)
* **Range**: [0, 1]
* **Description**: Evaluates how accurately the top-1 predicted beam index matches the ground-truth beam from a predefined codebook with 64 available beams.

### Channel Interpolation

* **Metric**: Normalized Mean Squared Error (NMSE)
* **Normalization**:
    $NMSE_{dB} = 10 \log_{10}(NMSE)$
    $Score = \max(0, \min(1, 1 - \frac{NMSE_{dB} - (-20)}{0 - (-20)}))$
* **Range**: [0, 1]
* **Description**: Lower NMSE values result in higher scores; **-15 dB** is considered excellent reconstruction.

### Channel Estimation

* **Metric**: Normalized Mean Squared Error (NMSE)
* **Scoring**: Same procedure as channel interpolation.
* **Description**: Measures how well the model denoises and reconstructs clean channels from noisy inputs.

### Channel Charting (User Localization)

* **Metric**: Localization Error (in meters)
* **Normalization**:
    $Score = \max(0, \min(1, \frac{100 - \text{Error (m)}}{100}))$
* **Range**: [0, 1]
* **Description**: Lower localization errors yield higher scores. Errors above 100 meters are clipped to zero.

---

## Composite Score Calculation

The **Composite Generalization Score (CG-Score)** is calculated as the **unweighted average** of the five normalized task-specific scores:

$CG\text{-}Score = \frac{1}{5} \sum_{i=1}^{5} \text{TaskScore}_i$

This final score reflects both **task performance** and **cross-task generalization**, rewarding models that perform consistently well across all tasks.


# Data Source

---

## Overview

In wireless networks, collecting labeled data is both time-consuming and expensive. To address this, it's crucial to develop models that generalize effectively to unseen environments, even when trained on limited labeled data. **Large Wireless Models (LWMs)** tackle this challenge by being **pre-trained on large, diverse, and unlabeled channel datasets** using self-supervised learning. These pre-trained models extract **universal and transferable features** that improve downstream task performance, especially when fine-tuned with small labeled datasets. By operating on these rich LWM embeddings, downstream models benefit from **enhanced generalization to novel channel realizations**.

---

## Pre-training Dataset

The **baseline LWM 1.1 model** is pre-trained on over **one million unlabeled wireless channel samples**, generated using **digital twin simulations from DeepMIMO scenarios**. To support further refinement, all competition scripts include built-in utilities to automatically download, preprocess, and bucket these datasets. The specific pre-training scenarios used for LWM 1.1 are listed on its [official webpage](https://lwm.com/lwm1.1-scenarios).

Participants are also encouraged to explore additional **DeepMIMO v4** scenarios or simulate new datasets using **ray-tracing or other methods**.

### Pre-training Freedom

Participants are fully allowed to use **any wireless channel dataset**—including open-source, proprietary, or synthetically generated datasets—for **pre-training or refining** the LWM model. There are **no restrictions** on the source or volume of pre-training data.

---

## Downstream Training Dataset

In contrast to pre-training, the downstream model training and **fine-tuning of the refined LWM** must be strictly limited to the **provided training and validation datasets** for each task:

* Each downstream task comes with its own **training, validation, and public test sets**.
* These sets are drawn from **distinct Wireless InSite ray-traced scenarios**—different from DeepMIMO—to simulate realistic deployment conditions.
* The **training set** must be used for model fitting, and the **validation set** is provided exclusively for monitoring and early stopping.
* The **public test set** can be used for evaluation, but must not be used for training or tuning.
* The **hidden challenge test set** will only be accessed internally by the organizers for final evaluation.

### Strict Rule on Downstream Training

**Participants must not use any additional channel samples beyond those provided in the official training datasets for downstream model training or for fine-tuning the LWM model for task-specific purposes. Any violation of this rule—including the use of even a single unauthorized channel sample—will result in immediate disqualification.**

---

## Robustness Considerations

To assess generalization and robustness, both the **public test sets** and the **hidden challenge sets** contain **out-of-distribution (OOD) samples**, simulating variations that occur in real-world wireless environments. This setup emphasizes the importance of **learning robust and transferable representations** rather than overfitting to specific training scenarios.


# Resources

All the tools and resources for this challenge can be found at the following link:

[https://lwm-wireless.net/lwm-challenge](https://lwm-wireless.net/lwm-challenge)

This link provides access to:

* **Datasets**: Training, validation, and test sets (Participants will be notified upon release)
* **Baseline LWM model scripts and checkpoint**
* **Downstream model training template**
* A **forum** for questions and comments related to the challenge.

---

# Controls or Restrictions

This challenge is open to all participants.

Please find the specific rules of this problem statement on the official website: [Link to Specific Rules](https://lwm-wireless.net/lwm-challenge)

# References

* [https://huggingface.co/wi-lab](https://huggingface.co/wi-lab)
* [https://arxiv.org/abs/2411.08872](https://arxiv.org/abs/2411.08872)
* [https://lwm-wireless.net/](https://lwm-wireless.net/)
* [https://lwm-wireless.net/lwm-challenge/](https://lwm-wireless.net/lwm-challenge/)

# Contact

* **Ahmed Alkhateeb** – alkhateeb[at]asu.edu
* Wireless Intelligence Lab
* School of Electrical, Computer and Energy Engineering
* Arizona State University, USA

