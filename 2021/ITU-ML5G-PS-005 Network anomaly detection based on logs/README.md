# ITU-ML5G-PS-005: Network anomaly detection based on logs

## Description
Modern communication network is becoming more and more complex. A large number of communication devices produce a large number of logs every day. From the logs, we can analyze the current health status of the devices and detect or predict the possible faults. Because the log data format is not uniform and unstructured, the traditional method of keyword search or rule matching to manually check the log is inefficient and not applicable. It is urgent to introduce AI-based log anomaly detection method to improve work efficiency and reduce operation and maintenance costs. We evaluate the effect by F1 value.
## Evaluation criteria

According to the test set, the prediction result should be saved in a csv file and follow the required format. Within the scope of optimization objectives, we use F1 score to evaluate the results. F1 score is calculated based on the precision and recall of log anomaly detection. The higher the precision is, the higher the recall is, and the larger the F1 score value is, the better the effect of log anomaly detection algorithm is.

## Data source
The training datasets consist of a collection of received packets at different SNR. The IEEE 802.11ay preamble is filtered trough the NIST Q-D channel realizations, which model the millimeter wave wireless signal propagation in a room with multiple people moving.

## Resources
None
## Results
1. Chin
2. Ember
