# ITU-ML5G-PS-009 RF-Sensor Based Human Activity Recognition

## Description
RF sensors, or radar (radio detection and ranging), have become increasingly widespread due to proliferation of low-cost, low-power, small RF transceivers. Commercially available RF sensors have typically been devised for biomedical applications of heart rate or respiration measurement, indoor human sensing (e.g. detection and tracking), or automotive sensing applications. Their costs can range from just a few dollars to as much as several thousand dollars, depending on whether it is a chip or evaluation board and whether it comes with its own user interface and processing software. The architectures of the transceivers can also vary from simple continuous-wave (CW) transceivers, to single-channel or multi-channel frequency modulated CW, and even ultra-wide band (UWB) impulse radars. Depending on the architecture, RF sensors can thus provide a rich dataset with information about human presence and movements, including range, velocity, and angle as a function of time.
RF sensor data can also be used for the purposes of human activity recognition, by applying a time-frequency transformation (e.g. short-time Fourier transform) to generate a plot of a subject’s radial velocity versus time – also known as a micro-Doppler signature. Different activities generate different patterns in the micro-Doppler signature; thus, machine learning can be applied to classify these patterns and thus identify different activities.
Accurate monitoring of human activities is a task critical to many applications of human ambient intelligence, including remote health monitoring, energy efficiency, smart environments, and human-computer interfaces. In this regard, RF sensing can be a great modality, as it is non-contact, is effective in the dark, and at low frequencies can even penetrate walls. RF sensors also are less personally invasive, as no imagery of the face or environment is obtained.
However, there are a number of challenges in achieving high classification accuracy; to name a few: the relatively small amount of data available for training, generalization to people whose data is not in the training dataset, recognition of activities not in the training data set (open set problem), degradation in performance when observation angle nears 90 degrees, and modulation of Doppler spread incurred when an individual walks in arbitrary directions.
This challenge addresses just the first of these challenges: how to most effectively train and classify RF human micro-Doppler signatures for activity recognition. Data from a multi-frequency RF sensor network comprised of three RF sensors with different transmit waveforms at center frequencies is provided at the Github link (https://github.com/ci4r/CI4R-Activity-Recognition-datasets). Participants should use a random selection of 50% of these samples for training and the remaining 50% of the samples for testing.
In addition to the 40% of the real data samples provided, participants are also allowed to use any other source of RF or other sensor modality desired for training. This includes databases of optical imagery, such as ImageNet, motion capture data, synthesized RF data, or other measured RF data, such as the 4 GHz activity data provided at https://github.com/ci4r/4-GHz-Human-Activity-Dataset- . Data from one sensor may also be used to help classify data from another sensor in the network.
The objective of the challenge is thus to encourage participants to advance the efficacy of DNN training in RF signature classification. In doing so, the participants are encouraged to think carefully about how the differences and similarities in the data acquired from each sensor can be exploited to maximize accuracy.

Further information can be found here: https://ci4r.ua.edu/aiml-challenge.html


## Evaluation criteria

Overall classification accuracy and confusion matrix, reported for 1) each sensor in the network and 2) using all sensors in the network

## Data source
Github with Data Download:
https://github.com/ci4r/CI4R-Activity-Recognition-datasets

Watch the webinar here: https://aiforgood.itu.int/events/understanding-how-people-move-using-modern-civilian-radar/

## Resources
Please make sure you check the following links
[1] https://ci4r.ua.edu/aiml-challenge.html
[2] https://github.com/ci4r/CI4R-Activity-Recognition-datasets
[3] https://github.com/ci4r/4-GHz-Human-Activity-Dataset-

## Results
1. Orion