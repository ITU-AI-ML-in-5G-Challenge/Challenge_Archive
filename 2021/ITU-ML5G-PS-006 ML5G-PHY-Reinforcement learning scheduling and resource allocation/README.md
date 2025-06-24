# ITU-ML5G-PS-006 ML5G-PHY-Reinforcement learning scheduling and resource allocation

## Description
[video guide -> ](https://youtu.be/6o6PUsbaWnA) 


More information about this challenge can be found [here](https://ai5gchallenge.ufpa.br/)

This problem adopts a strategy named CAVIAR (Communication networks and Artificial intelligence immersed in Virtual or Augmented Reality). The problem is based on simulating a communication system immersed on a virtual world, using software such as AirSim and Unreal Engine. The problem is posed as a game that must be solved with reinforcement learning (RL). The goal is to schedule and allocate resources to unmanned aerial vehicles (UAVs) and terrestrial users. The RL agent is executed at the base station. It periodically takes actions based on the information captured from the environment, which includes channel estimates, images from cameras and positions from a Global Navigation Satellite System such as GPS. The communication system model is based on a multiple input/multiple output (MIMO) system, with the base station having a uniform array while the users have a single antenna. The agent receives a reward based on the service provided to the users.

## Evaluation criteria

The participant must provide the predicted output for the test set as a CSV (comma-separated values) file along with the code to reproduce the result. Each row corresponds to the RL agent action (output) for the given time instant.

The participant must also provide two video files:

1. one with the rendering of the RL agent for the episode with the largest value for the return G
2. another for the episode with the smallest value of G.
These two videos should correspond to the output of CaviarRenderer-ITU-v1 (or later version). If desired, the participant can concatenate these videos into a single video.

Another option is to expand the video (or videos) by promoting the designed RL agent, describing its architecture or any other thing the participant thinks is interesting. This promoting video must be recorded in Portuguese or English.

We can generate the videos for the participants if it is needed.

## Data source
The dataset is composed of “traces” from simulations executed with Unreal Engine + AirSim, and will be available on June 30 at this [folder](https://nextcloud.lasseufpa.org/s/WYZAMbSbdocs2DL)


## Resources
[1] 5G MIMO Data for Machine Learning: Application to Beam-Selection using Deep Learning, 2018 - http://ita.ucsd.edu/workshop/18/files/paper/paper_3313.pdf.
[2] MmWave Vehicular Beam Training with Situational Awareness by Machine Learning, 2018 - https://ieeexplore.ieee.org/document/8644288.
[3] Generating mimo channels for 6G virtual worlds using ray-tracing simulations. Submitted to IEEE Statistical Signal Processing Workshop 2021.
[4] Simulation of machine learning-based 6G systems in virtual worlds. Submitted to the ITU Journal on Future and Evolving Technologies (submitted), 2021.

## Results
1. MLAB-RL
2. IITI-RL
3. Data Explorers
