# Description

Traffic prediction is one of the key ingredients to fulfill some of the goals of next-generation communications systems and to realize self-adaptability in mobile networks. The vast population of devices connected to base stations, while providing rich data to train Machine Learning (ML) models, can also compromise the efficiency of such models (e.g., temporal responsiveness) due to potential communication bottlenecks. In this regard, Federated Learning (FL) [1] arises as a compelling solution to provide robust ML optimization while maintaining the communication overhead low. In FL, devices exchange model parameters, rather than raw training data, thus also enhancing privacy.

This problem statement proposes the usage of FL tools to predict the traffic in cellular networks collaboratively. To that purpose, we provide an unlabeled dataset that contains data from unknown LTE users of commercial operators at three different specific locations. More details regarding the dataset and “starting-point” ML models can be found at [2].

**[IMPORTANT]**: For more details about this problem statement, please go to [https://supercom.cttc.es/index.php/ai-challenge-2022](https://supercom.cttc.es/index.php/ai-challenge-2022)

---

# Evaluation criteria

Participants will submit a report explaining their solution, including the outcomes of their models.

---

# Data source

A dataset with real LTE Physical Downlink Control Channel (PDCCH) measurements, obtained using OWL [3] from three different locations, will be provided to train ML models federatively. The dataset is both anonymous, because it is impossible to obtain users’ unique identifiers, and accurate because individual communication can be separated within the dataset for obtaining high-definition traces.

---

# Resources

Besides the dataset, complementary material will be provided to participants, including references, detailed instructions, and guidelines.

---

# References

[1] Konečný, J., McMahan, H. B., Yu, F. X., Richtárik, P., Suresh, A. T., & Bacon, D. (2016). Federated learning: Strategies for improving communication efficiency. arXiv preprint arXiv:1610.05492.
[2] Trinh, H. D., Gambin, A. F., Giupponi, L., Rossi, M., & Dini, P. (2020). Mobile traffic classification through physical control channel fingerprinting: a deep learning approach. IEEE Transactions on Network and Service Management, 18(2), 1946-1961. [Open-access version] (Note: The original text had `[]()` around "Open-access version", which is not valid markdown for a link. I've corrected it to a plain text representation based on the apparent intent.)
[3] [https://github.com/cn0xroot/LTE](https://github.com/cn0xroot/LTE)

---

# Contact

* **Supercom**: supercom@cttc.es
* **Paolo Dini**: paolo.dini@cttc.es
* **Marco Miozzo**: marco.miozzo@cttc.cat
* **Francesc Wilhelmi**: fwilhelmi@cttc.cat