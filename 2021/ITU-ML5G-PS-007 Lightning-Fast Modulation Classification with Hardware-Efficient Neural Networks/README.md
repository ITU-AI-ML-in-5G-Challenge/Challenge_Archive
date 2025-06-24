# ITU-ML5G-PS-007: Lightning-Fast Modulation Classification with Hardware-Efficient Neural Networks

## Description
In this challenge, the participants will design neural networks with an awareness of both inference computation cost and accuracy to explore the landscape of compact models for RF modulation classification on the DeepSig RadioML 2018 dataset.

Goal: Use quantization, sparsity, custom topology design and other training techniques to design a neural network that achieves a certain minimum accuracy on the RadioML 2018.01A dataset. Submissions will be ranked according to the inference cost function we define, and the lowest inference cost will win. Check under the Evaluation criteria tab for details.

Registration: Please register your team and user(s) on this portal.

Sandbox and baseline network: We provide a sandbox environment with everything you need to participate in this challenge, and a baseline network as a starting point. Check under the Resources tab for more details.

ITU challenge track/theme: Network-track, as the challenge consists of use cases related to signal decoding.

Background
The ever-growing demand for wireless data is driving a need for improved radio efficiency, of which a key component is improved spectral allocation via high quality spectrum sensing and adaptation. A key component for solutions such as Dynamic Spectrum Access (DSA) and Cognitive Radio (CR) is Automatic Modulation Classification (AMC), where the high-level goal is to monitor the RF spectrum and determine the different modulations being used. This information is subsequently used to reach transmission decisions that transmit information more efficiently. Prior works have successfully applied deep learning to AMC, demonstrating competitive recognition accuracy for a variety of modulations and SNR regimes.

To reap the benefits of AMC with deep learning in practice, an important challenge remains: modulation classification should be performed with low latency and high throughput to accurately reflect the current status of the transmissions. Inference with common deep neural networks can involve hundreds of millions of multiply-accumulate operations and many megabytes of parameters, which makes line-rate performance very challenging. A body of research [4, 5, 6] seeks to address these challenges applying quantization to weights and activations, pruning, novel topology design and pruning, which may be done in a co-designed fashion with hardware [7, 8] to provide the required system-level throughput. As this typically comes at the cost of some classification accuracy, multiple solutions offering different throughput at different levels of accuracy may be created.

## Evaluation criteria
### General
- Registration and submission deadlines are given in the Timeline tab.
- Registration and submission will take place on the ITU AI for Good Challenge Portal. Submissions can also be made through Google Forms as described [here](https://github.com/Xilinx/brevitas-radioml-challenge-21/discussions/18) if there are issues with the ITU Portal.
- Teams can consist of up to 4 individuals.
-  Submissions will be evaluated and ranked after the submission period closes.
- Valid submissions (see Criteria for Valid Submissions) will be ranked in ascending value (lower is better) of the inference cost score (see Inference Cost).
### Criteria for valid submissions
Submissions must fulfill the following criteria to be considered valid:

- The format for the submission must be a zipfile including the filled out submission form (from the sandbox), full source code, exported ONNX model with batch-1, trained .pth checkpoint, Dockerfile and instructions on how to reproduce the submission.
- Must include a neural network implemented with PyTorch and Brevitas for RadioML 2018.01A classification.
- Must provide a Dockerfile to build a Docker container with all required dependencies. Evaluation in terms of accuracy validation, ONNX export and inference cost measurement will be done inside this Docker container.
- Must include all source code used for training, validation and export of the neural network to be end-to-end reproducible (from training to ONNX export) using the submitted zipfile. See extra notes in Reproducibility.
- Must use BrevitasONNXManager to export the ONNX file (as shown in the Jupyter notebook in the sandbox).
- Must capture all operations involved in going from RadioML 2018.01A data to modulation classification result in the PyTorch model and the exported ONNX. For instance, if there is any pre/post-processing this must be captured in both the PyTorch model and the exported ONNX.
- Must respect the provided train-test split (from the sandbox) for RadioML 2018.01A for training.
- Must reach at least 56.000% accuracy averaged across all modulations and all SNRs present in RadioML 2018.01A on the test set (for the provided train-test split in the sandbox). The accuracy will be measured (using the Docker container) on the submitted trained .pth checkpoint and code. Extra accuracy over this threshold will not bring benefits for the score.
- Must be able to compute the inference cost using the latest official implementation, see notes under Inference Cost. The cost will be measured (using the Docker container) on the submitted ONNX model. See also exceptions under Custom Operations.
- If using quantization, must use Brevitas for quantized layers, with uniform quantization with zero-point=0 for weights and activations. Different weights and activations may use different bitwidths. Other forms of quantization not built with Brevitas, including PyTorch native quantization, is not supported.
- Must be made open-source on a publicly accessible URL after the submission deadline has passed.
### Reproducibility
- Because of inherent difficulty in reproducing training results exactly, a submission will be considered valid as long as it can be independently reproduced to reach the minimum required accuracy threshold, whether the reproduced accuracy matches the submitted one exactly or not.
- Any submission that cannot be reproduced (in terms of training, validation, export or inference cost) because of issues with setup, dependencies, etc. won’t be considered valid, independently of what it claims to achieve.

### Inference Cost

- The inference cost will be measured on the exported ONNX graph with input shape (1, 2, 1024) by using the official implementation. The exported graph is static regardless of the values of the input tensor.
- The official implementation for the inference cost function will be provided in the latest version of the feature/itu_competition_21 branch of the Xilinx/finn-base GitHub repository, with the inference_cost() function call in [thisfile](https://github.com/Xilinx/finn-base/blob/feature/itu_competition_21/src/finn/util/inference_cost.py) as the entry point. The per-layer inference cost analysis functions can be found [here](https://github.com/Xilinx/finn-base/blob/feature/itu_competition_21/src/finn/analysis/inference_cost.py).

- The organizers reserve the right to update the inference cost function implementation to fix bugs and provide improvements.
- If the inference cost function implementation and the explanation in this document disagree, the organizers will resolve this accordingly.
- The procedure in the Custom Operations section must be followed to account for the inference cost of any custom operations not currently supported by the latest inference cost function implementation.
The custom ONNX export and inference cost measurement will be done as shown in the Jupyter notebook in the sandbox.
- The inference cost will take into account the number of multiply-accumulate (MAC) operations and number of parameters for Conv, MatMul and Gemm ops assuming a naive/direct implementation (e.g. no Winograd for convolutions).
- The following layers are assumed to be zero-cost and will not be taken into account for the inference cost: elementwise nonlinearities, pooling, reshape/transpose/concat, batch normalization, Mul/Div and Add/Sub for applying biases or quantization scaling factors. These layers are elementwise and/or otherwise have little impact on total cost of inference based on existing DNN topologies.
- The inference cost will discount for parameter sparsity by discounted_mac = mac * (num_nonzero_ops/num_total_ops) and discounted_mem = mem * (num_nonzero_params/num_total_params) for each layer. Activation sparsity and any other form of dynamic sparsity is not taken into account.
- The inference cost will account for precision as follows: bit_ops = discounted_mac * weight_bits * act_bits and bit_mem = discounted_mem * weight_bits for each layer.
- For ranking, the inference cost will be converted to a score by normalizing against the inference cost of the provided baseline model as follows: score = 0.5*(bit_ops/baseline_bit_ops) + 0.5*(bit_mem/baseline_bit_mem). The scores will be ranked low-to-high (i.e. lower is better).

Custom Operations
Participants are allowed to implement custom layers and quantizers, as long as they can be exported through the existing ONNX flow and the organizers approve the inference cost computation. For fairness, the custom layers and their inference cost computation must be made available to all participants. If you want to use custom operations, the workflow is as follows:

1. Get in touch with the organizers as soon as possible (see the Contact tab) but defintiely no later than 2nd September (1 month ahead of the submission deadline) to explain which custom operation(s) you would like to implement, and make a suggestion for how to calculate the inference cost for these operations.
2. For the inference cost of your custom operation(s): if dominated by MACs, the compute (bit_ops) and memory cost (bit_mem) can be computed in a similar way to the existing Conv and MatMul operations, which can be found [here](https://github.com/Xilinx/finn-base/blob/feature/itu_competition_21/src/finn/analysis/inference_cost.py). For all other operations and computations, you must check separately with the organizers. A mapping to Xilinx FPGA LUTs by Vitis High-Level Synthesis will serve as the basis for the inference cost calculation.
3. The organizers will review your suggested ops and inference cost formula, and may ask for modifications. Whether your custom op and its inference cost will be approved is at the discretion of the organizers.
4. Once your proposal is approved, you will be asked to send a Pull Request (PR) to the inference cost implementation function, which will be reviewed and merged. Your custom ops are then valid for submission, and also available for other participants to use.
## Data source
Data source can be reached at:
This challenge uses the [RadioML 2018.01A](https://www.deepsig.ai/datasets) dataset provided by [DeepSig](https://www.deepsig.ai/). You will be required to provide your contact information to download the dataset.
Please note that this dataset is released by DeepSig under the [Creative Commons Attribution - NonCommercial - ShareAlike 4.0 License](https://creativecommons.org/licenses/by-nc-sa/4.0/) and you must abide by the terms of this license to participate in our challenge.

### Train/test split
Please note that we use a fixed train/test split on the dataset for a fair comparison, and you must abide by this in order to provide a valid submission. This split is given by the fixed random seed and other parameters in the Jupyter notebook we provide in the sandbox.

## Resources
Getting help
Connect with the challenge organizers and other participants on [GitHub discussion](https://github.com/Xilinx/brevitas-radioml-challenge-21/discussions). For questions related to quantization-aware training with Brevitas, there is also a separate Gitter channel: Gitter
![fig](CHAT.svg)[https://gitter.im/xilinx-brevitas/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge']

### Sandbox Environment
We provide a [sandbox environment](https://github.com/Xilinx/brevitas-radioml-challenge-21) for this challenge, which contains everything you need to make a submission to this challenge. This includes a Docker environment with PyTorch and Brevitas, and Jupyter notebook demonstrating how to train, validate and evaluate the hardware cost of the baseline network.

The sandbox environment may be occasionally updated, please ensure you have the latest version with git pull before submitting.

### Baseline network
As a starting point, we provide a baseline network: a version of the VGG10 CNN architecture proposed by the RadioML dataset authors in [Over-the-Air Deep Learning Based Radio Signal Classification](https://arxiv.org/pdf/1712.04578.pdf) The baseline network is trained with quantization-aware training in Brevitas, using 8-bit quantization for both weights and activations, and gets 59.82% average accuracy across all modulations and SNR levels.

You can find a pretrained PyTorch checkpoint in the sandbox, as well as the Python code to train the network from scratch in the provided Jupyter notebook.

###  Kickoff webinar slides and recording
You can view the recording for the kickoff webinar on [YouTube](https://www.youtube.com/watch?v=Mn4_1YeS-IM) and the slides [here.](https://2ja3zj1n4vsz2sq9zh82y3wi-wpengine.netdna-ssl.com/wp-content/uploads/2021/05/itu-challenge-lightning-fast-radioml-classification.pdf)


### Brevitas and FINN resources
Check out the Brevitas [Getting Started](https://github.com/Xilinx/brevitas/#getting-started) tutorial and [Jupyter notebooks](https://github.com/Xilinx/brevitas/#getting-started) to get more insights into quantization-aware training with Brevitas. We also have a [quantization-aware training guidelines document](https://bit.ly/finn-hls4ml-qat-guidelines). For pruning, you can use the PyTorch pruning utilities by following this tutorial.

Although this challenge does not require you to accelerate the neural networks that you train, FINN is a good choice for turning Brevitas-trained quantized neural networks into dedicated FPGA accelerators. You can find out more on the [FINN project page](https://xilinx.github.io/finn/) which has links to tutorials, examples, the FINN compiler and lots more.
## References for further reading
[1] Timothy J. O’Shea, Johnathan Corgan, and T. Charles Clancy. 2016. Convolutional Radio Modulation Recognition Networks. In Engineering Applications of Neural Networks. Springer International Publishing, Cham, 213–226.
[2] T. J. O’Shea, T. Roy, and T. C. Clancy. 2018. Over-the-Air Deep Learning Based Radio Signal Classification. IEEE Journal of Selected Topics in Signal Processing 12, 1 (2018), 168–179.
[3] Deepsig. RadioML datasets. https://www.deepsig.ai/datasets.
[4] Sze, Vivienne, Yu-Hsin Chen, Tien-Ju Yang, and Joel S. Emer. “Efficient processing of deep neural networks: A tutorial and survey.” Proceedings of the IEEE 105, no. 12 (2017): 2295-2329.
[5] Park, Eunhyeok, Sungjoo Yoo, and Peter Vajda. “Value-aware quantization for training and inference of neural networks.” In Proceedings of the European Conference on Computer Vision (ECCV), pp. 580-595. 2018.
[6] Gholami, Amir, Sehoon Kim, Zhen Dong, Zhewei Yao, Michael W. Mahoney, and Kurt Keutzer. “A Survey of Quantization Methods for Efficient Neural Network Inference.” arXiv preprint arXiv:2103.13630 (2021).
[7] Umuroglu, Yaman, Nicholas J. Fraser, Giulio Gambardella, Michaela Blott, Philip Leong, Magnus Jahre, and Kees Vissers. “Finn: A framework for fast, scalable binarized neural network inference.” In Proceedings of the 2017 ACM/SIGDA International Symposium on Field-Programmable Gate Arrays, pp. 65-74. 2017.
[8] Blott, Michaela, Thomas B. Preußer, Nicholas J. Fraser, Giulio Gambardella, Kenneth O’Brien, Yaman Umuroglu, Miriam Leeser, and Kees Vissers. “FINN-R: An end-to-end deep-learning framework for fast exploration of quantized neural networks.” ACM Transactions on Reconfigurable Technology and Systems (TRETS) 11, no. 3 (2018): 1-23.


## Results
We congratulate the winners of the 2021 Lightning Fast Modulation Classification with Hardware Efficient Neural Networks challenge. The top 3 teams are as follows:

|Rank |	Team Name |	Members |	Inference cost |	Accuracy|
|----------|:-------------:|------:|------:|------:|
|1|	BacalhauNET |	José Rosa, Guilherme Carvalho, Daniel Granhão, Tiago Gonçalves |	0.016211 |	0.56241|
|2 |	The A(MC) Team |	Jakob Krzyston, Rajib Bhattacharjea, Andrew Stark |	0.042467 |	0.562543|
|3 |	Aaronica |	Mohammad Chegini, Pouya Shiri |	 0.046007 |	0.561585 |

Full ranking with inference cost scores can be found on [this link](https://bit.ly/brevitas-radioml-challenge-21-results)
The presentations from the awards ceremony can be found below:

- Awards ceremony and FINN prototype results
- Team BacalhauNET, 1st place
- The A(MC) Team, 2nd place
- Team Aaronica, 3rd place
- Team Imperial_IPC, honorable mention
