# ITU-ML5G-PS-012 Radio Link Failure Prediction

## Description
Cloud, rain, snow, and other weather-related phenomena affect the performance of radio links. This is especially applicable to backhaul links operating at GHz frequencies. A generic regional weather forecast data is available which lists expected conditions and coarse temperatures along with actual –precise– realizations.

Adding to the complexity are the spatial nature of the data (regions of weather data and RLF needs to be aligned) as well as the time sync needed to correlate various occurrences. Over a period of time, we have compiled and anonymised region-wise data which corresponds to weather forecasts, radio link performances and radio link failures derived from our networks.

Given the region-wise, historical data sets derived from our networks and weather forecasts from the meteorology stations predict the occurrence of radio link failures in:

i) in the next day\
ii) in the following 5 days




## Evaluation criteria

F1-scores of identifying at least one radio link failure in the next day and the following 5 days will be used to evaluate solution proposals.
## Data source
Data source can be reached at:

https://github.com/Turkcell/ITU-AIMLin5GChallenge-2021
Visit website [here](https://github.com/Turkcell/ITU-AIMLin5GChallenge-2021)

Training Dataset
Visit website [here](https://github.com/Turkcell/ITU-AIMLin5GChallenge-2021/blob/main/RLF_Prediction_ITU_AIML_Challenge_Data/RLF_Prediction_ITU_AIML_Challenge_Data.7z)

Validation Dataset
Visit website [here](https://github.com/Turkcell/ITU-AIMLin5GChallenge-2021/blob/main/RLF_Prediction_ITU_AIML_Challenge_Data/RLF_Prediction_ITU_AIML_Challenge_Test_20210125.7z)

Exemplary Colab Project by Turkcell
Visit website [here](https://github.com/Turkcell/ITU-AIMLin5GChallenge-2021/blob/main/RLF_Prediction_ITU_AIML_Challenge_Data/TurkcellExampleProject.ipynb)

Zip file contains the following tab separated files (tsv):
• distances.tsv: pair-wise distances
• met-forecast.tsv: meteorology 5-day forecasts
• met-real.tsv: meteorology historic realizations
• met-stations.tsv: meteorology station information
• rl-kpis.tsv: radio link KPIs and configuration parameters
• rl-sites.tsv: radio link site information

## Resources
Challenge resources [https://github.com/ITU-build-a-thon/challenge-resources]



## Comparison to 2020 Problem statement
As compared to problem statement hosted by Turkcell in 2020, this problem statement offers a new data set (comprehensive and with very few missing values) and the data belongs to a new region. The evaluation criteria: predict any failures in the next day and the following 5 days as opposed to predicting failures for each of the following 5 days.

## Results
1. MLGrads
2. BMSigmoid
3. TeamNPN
4. FFares