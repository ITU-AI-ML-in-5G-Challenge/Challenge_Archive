# ITU-ML5G-PS-002 WALDO (Wireless Artificial intelligence Location DetectiOn) sensing using mmWave communications and ML

## Description
The Wireless Artificial Intelligence Location DetectiOn challenge tackles one most promising applications of current 5G and future 6G wireless systems, which is the convergence of millimeter wave communication, sensing and localization [1]. Millimetre network are currently being deployed and new interesting use cases are being proposed, paving the way to new innovative and emerging applications. Indeed, millimeter wave spectrum offers not only large bandwidth for high throughput applications but also great opportunities for accurate localization to enable new applications such as presence detection, gesture recognition, or person identification. In this context, IEEE has recently started a new task group, TGbf, to enhance the reliability and efficiency of WLAN sensing, introducing IEEE 802.11bf, which extends the current IEEE 802.11ay functionalities. WLAN sensing utilizes the 802.11 deployed devices to conduct tracking and monitoring, thus alleviating the need for specific monitoring devices [2].

Participants are challenged to propose an AI/ML algorithm that estimates the location of moving targets, e.g. people, given a set of training data set consisting of received 802.11ay packets at different SNR levels.

The challenge assumes an indoor multiple access points scenario. These devices communicate using conventional IEEE 802.11ay packets, which consist of a preamble and a series of symbol blocks. This configuration enables a multi-static radar, since sensing can be performed by tracking changes on a wireless channel through the reception of multiple packets. A single-user multi-antenna elements architecture is adopted at each device, which means that a single RF chain is equipped with a uniform rectangular array and a single stream can be transmitted (SISO). The wireless channel variations in the room are introduced by the presence of people that can have different motion dynamics.

We assume the room to be divided in multiple sectors. The participants need to estimate how many people are present in each of these sectors. This assumption represents practical applications such as in-store tracking to provide customized information and advertisement.

The participant solutions can shed light on the sensing and localization performance and limitations of future 6G systems re-using current 5G infrastructure, provide future directions to IEEE standardization activities as well as quantify the impact of novel AI/ML techniques with respect to conventional signal processing.

The webinar presenting the challenge can be found here: https://aiforgood.itu.int/events/machine-learning-for-joint-sensing-and-communication-in-future-millimeter-wave-ieee-802-11-wlans/
The slides are available here: https://github.com/usnistgov/PS-002-WALDO/blob/main/doc/ps002Waldo.pptx

The winner of the challenge will be invited as a guest researcher in the Wireless Network Division at NIST.
More general info about the Wireless Networks divisions are available here:
https://www.nist.gov/communications-technology-laboratory/wireless-networks-division


## Evaluation criteria

Two main metrics will be considered to evaluate the submission, i.e. counting and localization error. The counting error quantifies the accuracy in counting the total number of people present in the room. The localization error quantifies the accuracy in counting the number of people present in each sector. More weight will be given to the localization error.

## Data source
For software and dataset resources, please refer to https://github.com/usnistgov/PS-002-WALDO.

The challenge dataset relies on two open-source software:

1. IEEE 802.11ay packet generator available at: https://github.com/usnistgov/PS-002-WALDO.
2. NIST Q-D channel realization software: https://github.com/wigig-tools/qd-realization used to generate the millimeter wireless channel.

Training Dataset
The training datasets consist of a collection of received packets at different SNR. The IEEE 802.11ay preamble is filtered trough the NIST Q-D channel realizations, which model the millimeter wave wireless signal propagation in a room with multiple people moving.

## Resources
1. Software resource for ITU AI/ML 5G challenge: https://github.com/usnistgov/PS-002-WALDO
2. NIST Q-D channel realization software: https://github.com/wigig-tools/qd-realization

## Results
1. SixthSense
2. MLAB_waldo
