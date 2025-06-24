# PS-002 - Fault Impact Analysis: Towards Service-Oriented Network Operation & Maintenance

## Introduction
## Description

The Berlin V2X dataset offers high-resolution GPS-located wireless measurements across diverse urban environments in the city of Berlin for both cellular and sidelink radio access technologies, acquired with up to 4 cars over 3 days. The data enables thus a variety of different ML studies towards vehicle-to-anything (V2X) communication to lay the foundations of vehicular communications of the future.

The data includes information on:
– Physical layer parameters (such as signal strength and signal quality).
– Cellular radio resource management like cell identity, carrier aggregation and assigned resource blocks.
– Wireless Quality of Service (QoS) like delay and throughput (for cellular) or packet error rate (for sidelink).
– GPS-positioning information.
– Side information (traffic and weather).

### **Evaluation criteria**

We offer a preprocessed data-bundle, cellular_dataframe.parquet, that can be used as such, where all different data sources have been downsampled to 1 second and merged together. Nevertheless, we encourage participants to create their own preprocessed datasets (e.g. through upsampled/interpolated GPS traces) if this better suits their needs. For this, the participants can take the existing code base as a starting point. Contributions to the code repository are equally appreciated.

Feature engineering will be evaluated. As an example, if two models attain similar accuracy, but one model uses all PHY layer parameters and the other model only uses SNR, the latter model will be preferred.

## **Evaluation Score**

The final score will be computed as the weighted mean of:

– The coefficient of determination $R^2$ of the model on the test data. The $R^2$ score is computed in most ML/DL libraries as:

$$
R^2(y, \hat{y}) = 1 - \frac{\sum_{i=1}^n (y_i - \bar{y})^2}{\sum_{i=1}^n (y_i - \hat{y}_i)^2}
$$

– The discarded features. More specifically, since we consider the dataset to contain 84 useful features, this partial score equals 84 - used_features.

– A qualitative score depending on the problem setup, e.g., the decisions on the QoS parameter and the train/test split.

## **Submission**
The participants will submit the following in the Problem Statement Portal:

– Their code implementation.

– A “scores.csv” file (a reference file is provided in GitHub) containing:

– Their Team ID

– Their predicted QoS (e.g., “downlink QoS”)

– Their train and test sets (e.g., “operator 1” and “operator 2”)

– Their $R^2$ score

– The number of used features

– A short written report (2-5 pages) in .docx or PDF [journal paper format]. The participants need to justify their design choices (e.g. the type of domain adaptation problem and the chosen domains).

– Optionally, the saved model and weights in a suitable format.

## **Data source**
https://ieee-dataport.org/open-access/berlin-v2x

## **Resources**
https://github.com/fraunhoferhhi/BerlinV2X
MobileInsight: http://www.mobileinsight.net/

## **References**
Berlin V2X: A Machine Learning Dataset from Multiple Vehicles and Radio Access Technologies

https://arxiv.org/abs/2212.10343

## **Prizes**
A total prize pool of 1’000 CHF distributed as follows;
1st place (winner): 500 CHF [Hyperion: Ndabuye Sengayo Gideon]
2nd place (Runner-up): 300 CHF [dkapur2026: Dhruv Kapur]
3rd place: 200 CHF [UMN 5G: Qixin Zhang, Wei Ye, Steven Sleder, and Zhi-Li Zhang]