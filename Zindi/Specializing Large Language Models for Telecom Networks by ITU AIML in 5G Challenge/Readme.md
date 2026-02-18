##  The Impact of Large Language Models on 6G and Beyond

Original on Zindi: http://zindi.africa/competitions/specializing-large-language-models-for-telecom-networks

Large language models (LLMs) have spearheaded a new era marked by sophisticated text generation, advanced comprehension, and dynamic interaction. The evolutionary path of LLMs originates from the early stages of machine learning (ML) and natural language processing (NLP), characterized by the emergence of statistical language models and the gradual evolution of neural networks. Yet, the true transformation came through deep learning (DL) breakthroughs, particularly the rise of transformer architectures. These innovations have paved the way for the birth of language models with an unprecedented ability to process and generate extensive volumes of comprehensive textual content. Among these remarkable strides, OpenAI's generative pre-trained Transformer (GPT) series has emerged as a beacon, outshining its predecessors in both scale and capability. This ascent has empowered these models to achieve human-like language understanding and generation.

While LLMs have undeniably demonstrated their prowess across diverse sectors, their integration into the telecommunications industry has been somewhat limited. However, this landscape is undergoing a gradual metamorphosis as researchers delve deeper into the potential of LLMs within this domain. With this competition, our objective is to tackle this challenge and pave the way for the development of telecom GPTs.

This challenge will adopt part of the recently developed TeleQnA dataset [1], composed by multiple-choice questions related to different classes of telecom knowledge domains [2], and will require participants to work on (at least one of) the following independent tasks:

Specialize Falcon 7.5B on telecom knowledge: In this task, the participants will download Falcon 7.5B model [3] (https://huggingface.co/tiiuae/falcon-7b), and improve such model on their local computing facilities. The participants will be required to enhance the accuracy of the baseline model when answering to the multiple-choice questions included in the TeleQnA dataset by developing novel solutions or combining existing methods such as Retrieval Augmented Generation (RAG) and prompt engineering.
Specialize Phi-2 on telecom knowledge: In this task, the participants will download Phi-2 [4] (https://huggingface.co/microsoft/phi-2), and improve such model on their local computing facilities. The participants will be required to enhance the baseline model accuracy when answering to the multiple-choice questions included in the TeleQnA dataset by developing novel solutions or combining existing methods such as fine tuning, RAG and prompt engineering.
When designing/implementing the RAG, the participants should not use the question’ option. Using the options in the RAG will be penalized during the evaluation process.

### Challenges

Complexity and diversity of the questions in the dataset

- Diversity serves as a valuable resource for evaluating the strengths of an LLM in various standard specifications of the telecommunication domain. Technical specifications are intricated documents that define the technical standards for telecommunications systems. Off-the-shelf LLMs have shown relatively limited capabilities in answering complex inquiries from these classes of questions.

LLM Hallucinations and Fabrications:

- One of the key concerns with LLMs is their tendency to generate hallucinations or fabrications. LLMs rely on statistical patterns and associations learned from vast text data during training. Consequently, LLMs may produce responses that abide to these patterns, but are incorrect or nonexistent.
Limited explainability:

-The complex architecture and massive number of parameters in LLMs render it difficult to trace the decision-making process. In fact, LLMs lack transparency in terms of the specific features or patterns they rely on to generate responses. This opacity hinders the ability to understand why a particular answer or response was chosen over others.  
### About Instituto Nacional de Estadística y Geografía (INEGI)



INEGI is an autonomous public organization that is responsible for collecting, analyzing, and disseminating statistical and geographical information about Mexico. Through the regulation and coordination of the corresponding National Information System, INEGI provides reliable data on the territory, resources, population, and economy of the country, with the aim of supporting informed decision-making.

## Organizations
### About AI for Good - International Telecommunication Union (ITU)

![fig](iaforgood.png)

AI for Good is organized by ITU in partnership with 40 UN Sister Agencies. The goal of AI for Good is to identify practical applications of AI to advance the United Nations Sustainable Development Goals and scale those solutions for global impact. It’s the leading action-oriented, global & inclusive United Nations platform on AI.

### About Huawei Technologies (huawei.com)

![fig](iaforgood1.png)

Huawei Technologies is a multinational technology company dedicated to designing, developing, and providing high-quality telecommunications equipment and consumer electronics. It is now the world's largest supplier of telecommunications equipment, serving more than one-third of the world's population in more than 170 countries.
The Technology Innovation Institute (TII) is an Abu Dhabi government funded research institution that operates in the areas of artificial intelligence, quantum computing, autonomous robotics, cryptography, advanced materials, digital science, directed energy and secure systems. The institute is a part of the Abu Dhabi Government’s Advanced Technology Research Council.

### Prizes
1st prize: 500 CHF

2nd prize: 300 CHF

3rd prize: 200 CHF

There are 3 000 Zindi points available. You can read more about Zindi points [here](https://zindi.africa/discussions/13959?utm_source=zindi&utm_medium=blog&utm_campaign=challenge_resources&utm_id=CR).


### Evaluation
The participants to the challenge will be evaluated based on three important criteria [40:10:50]:

The accuracy that their solutions will reach on the TeleQnA validation dataset. NOTE: The validation dataset is not part of the TeleQnA currently available online.
The readability and reproducibility of the delivered code.
The quality of the scientific paper, presenting the proposed solution, and its novelty, as well as the tackled problem(s) during the challenge, and the related experiments done.
To evaluate the accuracy of the model(s), the participants will be required to submit through our portal a csv file, whose format is as follows:

For Falcon 7.5B

| Question_ID | Answer_ID | Task         |
|------------|-----------|--------------|
| 0          | 2         | Falcon 7.5B  |
| 1          | 3         | Falcon 7.5B  |
| 2          | 5         | Falcon 7.5B  |

for Phi-2

| Question_ID | Answer_ID | Task  |
|------------|-----------|-------|
| 0          | 2         | Phi-2 |
| 1          | 3         | Phi-2 |
| 2          | 5         | Phi-2 |

Where Question_ID, Answer_ID, and Task denote respectively 1) the question IDs of the test set for which the participants are providing answers through the LLM model 2) the answers selected by the model corresponding to the questions, and 3) the task to which the submission relates to, i.e., either Phi-2 or Falcon 7.5B.

The score of the submission will be evaluated in terms of Accuracy, i.e., the percentage of correctly provided answers in the test set.

In addition, the paper submission, acceptance, and presentation to the IEEE Globecom 2024 (https://globecom2024.ieee-globecom.org/) workshop (NOTE: at this stage, the workshop acceptance at IEEE Globecom is not yet been confirmed) associated with this challenge are strong requirements to win the competition, and they will demonstrate the participants capability to present their work, provide model explainability, and allow the community to reproduce their experiments. This challenge seeks to promote and encourage openness, rigor, reproducibility, and explainability of AI-based models; therefore, the participants will be strongly encouraged to share their solution on GitHub.



### Timeline
- Challenge starts: 7 May 2024
- Competition closes: 26 July 2024 at 23:59 GMT
- Workshop paper submission deadline: 12 August 2024
- Paper acceptance notification: 1 September 2024
- Camera ready: 1 October 2024

### Ressources
In addition to the MCQs, we will provide a supporting corpus of documents that the participants can use to enhance the accuracy of their model on the MCQs, e.g., 3GPP Rel 18 documents that can provide the LLMs context knowledge to answer the telecom questions in the dataset.

To participate in the competitions, participants will need to download Falcon-7B (https://huggingface.co/tiiuae/falcon-7b) and Phi-2 (https://huggingface.co/microsoft/phi-2), and run the model on their local computing facilities. Participants will have to develop novel solutions or combine existing methods such as RAG and prompt engineering.

- An example of RAG for improving LLM knowledge on telecom standards is available at this link based on the work presented in this paper [5]
- An example of prompt engineering for Phi-2 in the context of TeleQnA is available here including accuracy results [6]
- An example of accuracy of Falcon-7B in the context of TeleQnA is available here [7]
- An example of Phi-2 deployment and test using the RAG in [5] on TeleQnA is here.
Participants willing to work on Falcon-7B shall not use fine-tuning methods, which can be instead explored by participants working on Phi-2.

Based on a first come first served policy, we will provide a limited number of dedicated APIs to Falcon-7B, which will be freely available to the participants during the duration of the challenge.

To request computational resources for running Falcon-7B, please fill the following form https://forms.office.com/r/Dx2jN5SWG8

### Paper Reference

[1] TeleQnA: https://github.com/netop-team/TeleQnA

[2] A. Maatouk, F. Ayed, N. Piovesan, A. De Domenico, M. Debbah, and Z.-Q. Luo, “Teleqna: A benchmark dataset to assess large language models telecommunications knowledge,” arXiv preprint arXiv:2310.15051, 2023 https://arxiv.org/pdf/2310.15051.pdf

[3] E. Almazrouei, H. Alobeidli, A. Alshamsi, A. Cappelli, R. Cojocaru, M. Debbah, E. Goffinet, D. Hesslow, J. Launay, Q. Malartic et al., “The falcon series of open language models,” arXiv preprint arXiv:2311.16867, 2023 https://arxiv.org/pdf/2311.16867.pdf

[4] M. Javaheripi, and S. Bubeck, “Phi-2: The surprising power of small language models,” Dec. 2023 https://www.microsoft.com/en-us/research/blog/phi-2-the-surprising-power-of-small-language-models/

[5] A.-L. Bornea, F. Ayed, A. De Domenico, N. Piovesan, A. Maatouk, “Telco-RAG: Navigating the Challenges of Retrieval-Augmented Language Models for Telecommunications” arXiv preprint arXiv:2404.15939, 2024 https://arxiv.org/abs/2404.15939

[6] N. Piovesan, A. De Domenico, and F. Ayed, “Telecom language models: Must they be large?” arXiv preprint arXiv:2401.08406, 2024.

[7] T. Ahmed, N. Piovesan, A. De Domenico, S. Choudhury, “Linguistic Intelligence in Large Language Models for Telecommunications” arXiv preprint arXiv:2402.15818, 2024 https://arxiv.org/pdf/2402.15818

