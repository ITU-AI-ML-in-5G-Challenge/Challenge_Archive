# ITU-ML5G-PS-016: Location estimation using RSSI of wireless LAN

## Description
The demand for location information is becoming more critical due to the emerge of map applications and augmented reality (AR). Global positioning system (GPS) is the leading steam of localization; however, its accuracy significantly degrades when the number of satellites can be seen from the receivers decreases or due to the impact of reflection from the structures. Thus, the sole use of GPS cannot guarantee ubiquitously accurate localization. As a substitution, localization techniques utilizing the radio signal received from access point (AP) of Wi-Fi and base station (BS) of cellular systems is promising. However, the typical triangulation approach suffers from the multipath fading channel, and hence it cannot achieve high accuracy. This challenge aims to verify if the AI/ML aided localization utilizing receives signal strength indicator (RSSI) observed at the terminal can achieve a similar accuracy as the GPS-based localization. In the traditional localization based on RSSI, it is necessary to have accurate modeling of the channel model that significantly impacts localization accuracy. This challenge explores the possibility if the data-oriented localization can replace the model-based location with the help of powerful AI/ML technique.

Registration for participants: ~ Sept. 14th (Extended)
Training and validation datasets release
Participants build, train and validate models
Submission of localization results: ~ Sept. 30th (Extended)

## Evaluation criteria

Participants are requested to submit AI/ML program/parameters tuned.

Evaluation will be performed as follows:

50 Average localization error
“+” 50 Maximum error
“+” (max.) 50 Algorithm performance (computational complexity, adaptability to dynamic environment)
Participants are requested to submit the following materials:

1. Document that includes:
-  discussion about localization results, including “average error”,      “maximum error”.
- brief description of the algorithm
2. Program code

## Data source
The training data includes the location of AP, RSSI information within the coverage of the AP and its corresponding location.

## Specification/Paper reference
1. S. Hara and D. Anzai, “Use of Simplified Maximum Likelihood Function in a WLAN-Based Location Estimation” IEEE
Conference on Wireless Communications and Networking, pp.1-6, May 2009
2.  S. Hara, “Statistical estimation theory in localization,” IEICE Fundamentals Review, vol.4, no.1, pp.32-37,
2010


## Results
1. SSN_ITU
2. C-LAMP
3. DLine
4. Tachibana-lab
5. TECO.AR STEAM

