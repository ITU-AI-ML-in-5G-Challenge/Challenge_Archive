# ITU-ML5G-PS-008 ML5G-PHY-Localization Multidevice localization with mmWave signals in a factory environment 

## Description
Jeff is no longer in charge of the death star cantine and Josh, the new supervisor has decided to replace all the storm troopers in the cellar warehouse due to their unreliability. Instead, multiple R2D2 and C3PO robots will do this job. Josh has also decided that in order to save energy for the superlaser and keep the drinks in the cellar at the right temperature it is going to switch of the lights at the warehouse, leaving these friendly robots blind. Instead, a swarm intelligence is going to command their actions and will use their newly installed mmWave interference to estimate their location. Your job is to design a localization system able to extract 3D position and orientation of the robot communication devices so the swarm intelligence can plan their actions. Of course, this task will not be easy as these robots can connect to different access point and we do not want to stop their communication capabilities for the sake of localization, thus you might find some interferences in the measurements.

After a visit to the cellar you’ve estimated that the scenario has an area about 30 by 60 squared meters. The 12 access points deployed in the ceiling forming a rectangular grid. The mmWave antennas installed in the access points and the robots are uniform rectangular arrays of 8 by 8 antenna elements for the access points and 4 by 4 antenna elements for the robots. Using one of the C3PO as an interpreter, and R2D2 has told you that both the access points and the robots are making use of fixed beam-paterrn codebooks for communications.

Josh has given you more details about your job here(https://research.ece.ncsu.edu/ai5gchallenge-localization/).


*No storm trooper became jobless during this conversion to automatic warehouse, instead they got reassigned to the new Alderaan thematic park.


## Evaluation criteria

For the evaluation we start by computing the Euclidean localization error for every sample and then we compute the ratio between the localization error median and the ratio of samples with localization error under 0.5m.

## Data source
The training data set consists of a collection of channels associated to the links between devices and access points in a factory environment and also their associated positions in the room. The factory environment has been simulated by ray tracing, with 12 access points (AP) located at the ceiling. The devices are randomly placed at the room and assigned to the AP with highest gain during the sector level sweep. For simplification, we assume perfect synchronization, this means that the first path arrives to the AP at time 0. The beam-training is measured. Then, with probabilities 50%, 25% and 25%, 0, 1 or 2 other devices interfere with the beam-training through random 4-QAM OFDM symbols using 512 frequency carriers.

Two datasets are provided, namely “train” and “test”. The dataset “train” consists on all the information required for the training of your algorithm, this is UE location and the AP it is associated to, while the dataset “test” lacks the UE localization.

Each participant can get access to each of the 12000 samples measurement through the provided executable file by passing as flags the name of the dataset and the indices [0-11999] of the samples to generate.
Example: “gen_channel.exe train 0 1 2” generates the first 3 samples of the “train” dataset.

We also provide Python code to more easily understand the dataset through visualization.

The provided Python code generates the measurements regarding the sample indexes 0, 4 and 8, which happen to have 0, 1 and 2 interferers and then prints the information regarding these samples interferer and plots the power spectrums in time, direction of departure and direction of arrival.

These files can either be downloaded from the dataset tab once the team is registered or from the NCSU [webpage](https://research.ece.ncsu.edu/ai5gchallenge-localization/) of the problem.

## Resources
[1] J. P. González-Coma, J. Rodríguez-Fernández, N. González-Prelcic, L. Castedo and R. W. Heath, “Channel Estimation and Hybrid Precoding for Frequency Selective Multiuser mmWave MIMO Systems,” in IEEE Journal of Selected Topics in Signal Processing, vol. 12, no. 2, pp. 353-367, May 2018.
[2] A. Shahmansoori, G. E. Garcia, G. Destino, G. Seco-Granados and H. Wymeersch et al., “Position and Orientation Estimation through Millimeter Wave MIMO in 5G Systems,” IEEE Trans. Wireless Commun., March 2018.
[3] W. Zheng and N. González-Prelcic, “Joint Position, Orientation AND Channel Estimation in Hybrid mmWave MIMO Systems,” 2019 53rd Asilomar Conference on Signals, Systems, and Computers, Pacific Grove, CA, USA, 2019, pp. 1453-1458.
## Results
