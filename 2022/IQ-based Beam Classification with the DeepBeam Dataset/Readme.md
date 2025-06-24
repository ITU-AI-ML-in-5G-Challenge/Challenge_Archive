# DeepBeam: Beam and Angle Detection in mmWave Systems Challenge

## Description

Highly directional millimeter wave (mmWave) radios need to perform beam management to establish and maintain reliable links. To achieve this objective, existing solutions mostly rely on explicit coordination between the transmitter (TX) and the receiver (RX), which significantly reduces the airtime available for communication and further complicates the network protocol design. In our paper [1], we proposed a new approach based on convolutional neural networks (CNNs) for the detection of the transmit beam used by the TX, and the angle of arrival at the RX side. In this way, the RX can associate Signal-to-Noise-Ratio (SNR) levels to beams without explicit coordination with the TX. DeepBeam thus does not require pilot sequences from the TX, nor any beam sweeping or synchronization from the RX. This is possible because different beam patterns introduce different “impairments” to the waveform, which can be subsequently learned by a CNN. To demonstrate the generality of DeepBeam, we conducted an extensive experimental data collection campaign where we collected more than 4 TB of mmWave waveforms with (i) 4 phased array antennas at 60.48 GHz, (ii) 2 codebooks containing 24 one-dimensional beams and 12 two-dimensional beams; (iii) 3 receiver gains; (iv) 3 different AoAs; (v) multiple TX and RX locations. Moreover, we collected waveform data with two custom-designed mmWave software-defined radios with fully-digital beamforming architectures at 58 GHz.

The DeepBeam paper showed how a specific CNN structure can be used to achieve high accuracy on the TX beam (TXB) classification problem on the three different classes (5, 12, and 24 beams). In this challenge, participants will leverage the DeepBeam dataset and (if needed) the DeepBeam codebase to develop CNNs that improve the classification accuracy, while reducing the number of samples that are required for the classification.

## Problem Statement

The goal of this challenge is to create a classifier for transmit beams out of a codebook using neural networks. The solution must classify the transmit beam TXB given L I/Q samples. The challenge will be organized in two tracks, and participants will need to submit solutions that work for both tracks.

* **Track 1**: Train and test with a portion of the dataset collected with the same antenna and deployment configurations (see Sec. 4 of [1]).
* **Track 2**: Train and test for the 12- and 24-beams codebooks with training data from one configurations and testing data from another (as done in Fig. 13 of [1]).

## Baseline

As a baseline, we provide the code used in [1] to train and test the TXB classification CNN. In this challenge, participants will propose deep neural network architectures that can improve over the baseline performance. Please refer to for an extensive README:

* [https://github.com/wineslab/deepbeam](https://github.com/wineslab/deepbeam)

## Evaluation Criteria

The objective is to test the accuracy of the classification, defined as the average over the accuracy for the classification of each class (see [DeepBeamTesting.py#L128](https://github.com/wineslab/deepbeam/blob/00bcebb043f2d9da8dd83300b12b9c253fde85b7/keras_code/DeepBeamTesting.py#L128)), truncated to an integer number. Tests that will yield the same accuracy will rank higher if they use a smaller number of I/Q samples as input.

We will provide indexes for the entries that will be considered testing and training in the DeepBeam dataset.

# Data Source

The data source is represented by the DeepBeam dataset, as described here: [https://deepbeam.net](https://deepbeam.net).
We will provide indexes to determine the train and testing sets out of the full dataset.

---

# Resources

All the tools and resources can be found at the following link: [https://deepbeam.net](https://deepbeam.net)

These resources include:

* Datasets for multiple configurations (as discussed in Sec. 4 of [1]).
* Python API to easily read the datasets provided.
* Baseline for the DeepBeam CNNs.

---

# Restrictions

This challenge is open to all participants. To participate officially, it is mandatory to fill out the registration form at: [https://forms.gle/T6YcMtfQ2frQkgYR8](https://forms.gle/T6YmCtfQ2frQkgYR8)

---

# References

* [1] M. Polese, F. Restuccia, and T. Melodia, “DeepBeam: Deep Waveform Learning for Coordination-Free Beam Management in mmWave Networks”, Proc. of ACM Intl. Symp. on Theory, Algorithmic Foundations, and Protocol Design for Mobile Networks and Mobile Computing (ACM MobiHoc), July 2021.

---

# Contact

* **Michele Polese**: m.polese@northeastern.edu
    * Institute for the Wireless Internet of Things
    * Northeastern University, Boston, MA