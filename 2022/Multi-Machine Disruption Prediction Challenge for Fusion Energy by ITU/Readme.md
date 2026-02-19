# Multi-Machine Disruption Prediction Challenge for Fusion Energy by ITU

##  Can you predict soil parameters from hyperspectral earth observation data?

Original on Zindi: https://zindi.africa/competitions/multi-machine-disruption-prediction-challenge

The energy crisis poses a significant global challenge in our time. While the search for efficient and sustainable energy sources is complex, one promising avenue is fusion energy.

Nuclear fusion involves the merging of two light nuclei, a process that releases a substantial amount of energy. This fusion occurs within a plasma, a state of matter consisting of ions and free electrons, and represents a clean, safe, and accessible energy source. Although fusion energy is not yet commercially viable, scientists worldwide are collaborating to make this a reality.

To achieve nuclear fusion, it is necessary to confine the nuclei. One method involves employing a torus-shaped magnetic field within devices known as tokamaks. However, instabilities can arise within the tokamak plasma, leading to energy losses and termination of the fusion process. These phenomena, called disruptions, can have devastating effects. Thus, it becomes crucial to predict disruptions as early as possible.

The physics underlying disruptions is not yet fully comprehended, and the behaviour of plasma can vary across different devices. Consequently, novel tools such as artificial intelligence are needed to develop a universal and efficient method for disruption prediction. Preliminary research in this area has already yielded promising results.

Within the IAEA Coordinated Research Project on AI for Fusion, this challenge aims to explore the potential of machine learning in contributing to multi-machine disruption prediction.

You will be provided with data from three distinct tokamaks, namely C-Mod, J-TEXT, and HL-2A. J-TEXT and HL-2A will be used as training set, and the C-Mod data set will be used for evaluation.

The objective of this challenge is to develop a disruption prediction model that can be applied universally, using J-TEXT and HL-2A as the current devices and C-Mod as the future device.

The realization of this data challenge was made possible thanks to the work of Dr Chengshuo Shen (HUST), Dr Jinxiang Zhu (PSFC), Dr Zheng Wei (HUST), Dr Zhongyu Yang (SWIP), Dr Cristina Rea (PSFC), Diakhere Gueye (IAEA), Matteo Barbarino (IAEA), and Thomas Basikolo (ITU).

#### Evaluation

The error metric for this competition is the F1 score, which ranges from 0 (total failure) to 1 (perfect score). Hence, the closer your score is to 1, the better your model.

F1 Score: A performance score that combines both precision and recall. It is a harmonic mean of these two variables. Formula is given as: 2*Precision*Recall/(Precision + Recall)

Precision: This is an indicator of the number of items correctly identified as positive out of total items identified as positive. Formula is given as: TP/(TP+FP)

Recall / Sensitivity / True Positive Rate (TPR): This is an indicator of the number of items correctly identified as positive out of total actual positives. Formula is given as: TP/(TP+FN)

Where:

TP=True Positive
FP=False Positive
TN=True Negative
FN=False Negative
Your submission file should look like this (numbers to show format only):

Shot_list	Is_disrupt
ID_1160803026	   1
ID_1140805015	   0
If you are in the top 10, when you submit your code for review you will need to submit your code on a GitHub repository and share a presentation, for which a template will be provided (6 slides maximum). This presentation should outline their assumptions, model architecture, strategy, and the results* obtained with a predetermined C-Mod dataset, which will provided to the participants on a due date.

*Results should include:

True positive and false positive rates at 40 ms before disruption
F1 score
ROC curve and area under it
Accumulated warning time


### Prizes

1st Place: $2 500 USD

2nd Place: $1 500 USD

3rd Place: $1 000 US

There are 5 000 Zindi points available. You can read more about Zindi points here.

Participants are required to submit:

1. A CSV file containing model predictions (online leaderboard);
2. The developed model code;
3. A report explaining their solution, including the outcomes of their models. The technical report will be used to judge the novelty/originality and usefulness of the proposed methodology
4. Participants will be required to present their solutions to an ITU Challenge Finale session

In evaluating the final submission, both the quality of the report (weighted 40%) and the achieved model score (weighted 60%) will be considered.

### Timeline
Competition closes on 12 November 2023.

Final submissions must be received by 11:59 PM GMT.

We reserve the right to update the contest timeline if necessary.



### About AI for Good - International Telecommunication Union (ITU)

![fig](iaforgood.png)

AI for Good is organized by ITU in partnership with 40 UN Sister Agencies. The goal of AI for Good is to identify practical applications of AI to advance the United Nations Sustainable Development Goals and scale those solutions for global impact. It’s the leading action-oriented, global & inclusive United Nations platform on AI.

<b>About [International Atomic Energy Agency (IAEA)](https://www.iaea.org/)</b>

![fig](iaforgood1.png)

The IAEA is the world's centre for cooperation in the nuclear field and seeks to promote the safe, secure and peaceful use of nuclear technologies.

About [MIT Plasma Science and Fusion Center (PSFC)](https://www.psfc.mit.edu/)

![fig](iaforgood2.png)

The MIT Plasma Science and Fusion Center (PSFC) provides research and educational opportunities that expand our understanding of fusion science, plasma physics, its applications, and magnet technology. As a multidisciplinary lab, the PSFC leverages translational science to create real-world solutions, with a focus on developing magnetic fusion as a carbon-free energy source.

About [ Huazhong University of Science and Technology (HUST)](https://www.psfc.mit.edu/)

![fig](iaforgood3.png)

Huazhong University of Science and Technology (HUST) is a comprehensive research university located in Wuhan, China under the direct supervision of the Ministry of Education. It is a participant university of the former “985” Project [1] in China, and also one of the first universities approved under the national "Double First-Class" Initiative, China’s “Excellence Initiative” for institutions of higher education.

The International Joint Research Laboratory of Magnetic Confinement Fusion and Plasma Physics at Huazhong University of Science and Technology is home to the J-TEXT tokamak, ranking as the third largest tokamak in operation in China. Originating as the TEXT-upgrade tokamak, it was initially designed and constructed by the University of Texas at Austin before relocating to China in 2004.

The primary focus of research at J-TEXT is the study of disruptions. J-TEXT is known for its robust construction, making it capable of handling disruptions with ease. Consequently, disruption-related experiments are frequently conducted, resulting in a substantial collection of disruption data. This makes J-TEXT an ideal platform for research aimed at predicting disruptions.

About Southwestern Institute of Physics (SWIP)


About [Southwestern Institute of Physics (SWIP))](https://en.cnnc.com.cn/2020-01/14/c_448104.htm).

![fig](iaforgood4.png)

Southwestern Institute of Physics (SWIP) was built in Chengdu, China in 1965, which was China’s first nuclear fusion research institute. It is affiliated with China National Nuclear Corporation(CNNC), and is the core of China's 3-step national strategy of nuclear energy development (thermal reactor, fast reactor, and fusion reactor).

SWIP has two tokamaks (HL-2A and HL-3) in operation at present, which have made a number of breakthroughs in magnetically controlled nuclear fusion in China. It has a complete range of disciplines, research platforms and laboratories for fusion energy development. SWIP has also been an important contributor for Chinese participation in ITER construction, by providing key technologies and components for ITER. So far SWIP has won over 20 Chinese National Scientific and Technological Progress Awards.

About [Southwestern Institute of Physics (SWIP))](https://en.cnnc.com.cn/2020-01/14/c_448104.htm).

![fig](iaforgood5.png)

HL-2A is a medium-sized tokamak for fusion research in Chengdu, China. It was constructed by CNNC from early 1999 to 2002, based on the main components (magnet coils and plasma vessel) of the former German ASDEX device. HL-2A was the first tokamak with a divertor in China. The research goals of HL-2A are the study of fundamental fusion plasma physics to support the international ITER fusion reactor.



### Rules
#### Teams and collaboration

You may participate in challenges as an individual or in a team of up to four people. When creating a team, the team must have a total submission count less than or equal to the maximum allowable submissions as of the formation date. A team will be allowed the maximum number of submissions for the challenge, minus the total number of submissions among team members at team formation. Prizes are transferred only to the individual players or to the team leader.

Multiple accounts per user are not permitted, and neither is collaboration or membership across multiple teams. Individuals and their submissions originating from multiple accounts will be immediately disqualified from the platform.

Code must not be shared privately outside of a team. Any code that is shared, must be made available to all challenge participants through the platform. (i.e. on the discussion boards).

The Zindi data scientist who sets up a team is the default Team Leader but they can transfer leadership to another data scientist on the team. The Team Leader can invite other data scientists to their team. Invited data scientists can accept or reject invitations. Until a second data scientist accepts an invitation to join a team, the data scientist who initiated a team remains an individual on the leaderboard. No additional members may be added to teams within the final 5 days of the challenge or last hour of a hackathon.

The team leader can initiate a merge with another team. Only the team leader of the second team can accept the invite. The default team leader is the leader from the team who initiated the invite. Teams can only merge if the total number of members is less than or equal to the maximum team size of the challenge.

A team can be disbanded if it has not yet made a submission. Once a submission is made individual members cannot leave the team.

All members in the team receive points associated with their ranking in the challenge and there is no split or division of the points between team members.


### Full Challenge Rules
This challenge is open to all.


#### Datasets and packages

The solution must use publicly-available, open-source packages only. Your models should not use any of the metadata provided.

You may use only the datasets provided for this competition. Automated machine learning tools such as automl are not permitted.

If the challenge is a computer vision challenge, image metadata (Image size, aspect ratio, pixel count, etc) may not be used in your submission.

If external data is allowed you may only use data that is freely available to everyone. You must send it to Zindi to confirm that it is allowed to be used and then it will appear on the data page under additional data.

You may use pretrained models as long as they are openly available to everyone.

You are allowed to access, use and share competition data for any non-commercial, research or education purposes, under a CC BY-NC-SA license.

@INPROCEEDINGS{9897443,

  author={Nalepa, Jakub and Le Saux, Bertrand and Longépé, Nicolas and Tulczyjew, Lukasz and Myller, 
  Michal and Kawulok, Michal and Smykala, Krzysztof and Gumiela, Michal},
  booktitle={2022 IEEE International Conference on Image Processing (ICIP)},
  title={The Hyperview Challenge: Estimating Soil Parameters from Hyperspectral Images},
  year={2022},
  pages={4268-4272},
  doi={10.1109/ICIP46576.2022.9897443}
}
Your solution must not infringe the rights of any third party and you must be legally entitled to assign ownership of all rights of copyright in and to the winning solution code to Zindi.


#### Submissions and winning

You may make a maximum of 10 submissions per day.

You may make a maximum of 300 submissions for this challenge.

Before the end of the challenge you need to choose 2 submissions to be judged on for the private leaderboard. If you do not make a selection your 2 best public leaderboard submissions will be used to score on the private leaderboard.

During the challenge, your best public score will be displayed regardless of the submissions you have selected. When the challenge closes your best private score out of the 2 selected submissions will be displayed.

Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 30% of the test dataset. While the challenge is open, the Public Leaderboard will rank the submitted solutions by the accuracy score they achieve. Upon close of the challenge, the Private Leaderboard, which covers the other 70% of the test dataset, will be made public and will constitute the final ranking for the challenge.

Note that to count, your submission must first pass processing. If your submission fails during the processing step, it will not be counted and not receive a score; nor will it count against your daily submission limit. If you encounter problems with your submission file, your best course of action is to ask for advice on the Competition’s discussion forum.

If you are in the top 10 at the time the leaderboard closes, we will email you to request your code. On receipt of email, you will have 48 hours to respond and submit your code following the Reproducibility of submitted code guidelines detailed below. Failure to respond will result in disqualification.

If your solution places in the top 10 on the final leaderboard, you will be required to submit your winning solution code to us for verification.

If two solutions earn identical scores on the leaderboard, the tiebreaker will be the date and time in which the submission was made (the earlier solution will win).

The winners will be paid via bank transfer, PayPal if payment is less than or equivalent to $100, or other international money transfer platform. International transfer fees will be deducted from the total prize amount, unless the prize money is under $500, in which case the international transfer fees will be covered by Zindi. In all cases, the winners are responsible for any other fees applied by their own bank or other institution for receiving the prize money. All taxes imposed on prizes are the sole responsibility of the winners. The top winners or team leaders will be required to present Zindi with proof of identification, proof of residence and a letter from your bank confirming your banking details. Winners will be paid in USD or the currency of the challenge. If your account cannot receive US Dollars or the currency of the challenge then your bank will need to provide proof of this and Zindi will try to accommodate this.

Payment will be made after code review and sealing the leaderboard.

You acknowledge and agree that Zindi may, without any obligation to do so, remove or disqualify an individual, team, or account if Zindi believes that such individual, team, or account is in violation of these rules. Entry into this challenge constitutes your acceptance of these official challenge rules.

Zindi is committed to providing solutions of value to our clients and partners. To this end, we reserve the right to disqualify your submission on the grounds of usability or value. This includes but is not limited to the use of data leaks or any other practices that we deem to compromise the inherent value of your solution.

Zindi also reserves the right to disqualify you and/or your submissions from any challenge if we believe that you violated the rules or violated the spirit of the challenge or the platform in any other way. The disqualifications are irrespective of your position on the leaderboard and completely at the discretion of Zindi.

Please refer to the FAQs and Terms of Use for additional rules that may apply to this challenge. We reserve the right to update these rules at any time.

#### Reproducibility of submitted code

- If your submitted code does not reproduce your score on the leaderboard, we reserve the right to adjust your rank to the score generated by the code you submitted.

- If your code does not run you will be dropped from the top 10. Please make sure your code runs before submitting your solution.

- Always set the seed. Rerunning your model should always place you at the same position on the leaderboard. When running your solution, if randomness shifts you down the leaderboard we reserve the right to adjust your rank to the closest score that your submission reproduces.

- Custom packages in your submission will not be accepted.

- You may only use tools available to everyone i.e. no paid services or free trials that require a credit card.

Read this [article](https://zindi.africa/learn/how-to-ensure-success-when-submitting-your-code-for-review) on how to prepare your documentation and this article on how to ensure a successful code review.

#### Data standards:

- Your submitted code must run on the original train, test, and other datasets provided.
- If external data is allowed, external data must be freely and publicly available, including pre-trained models with standard libraries. If external data is allowed, any data used should be shared with Zindi to be approved and then shared on the discussion forum. Zindi will also make note of the external data available on the data page.

- Packages:
- You must submit a requirements file with all packages and versions used.
- If a requirements file is not provided, solutions will be run on the most recent packages available.
- Custom packages in your submission notebook will not be accepted.
- You may only use tools available to everyone i.e. no paid services or free trials that require a credit card.


### Documentation
A README markdown file is required

It should cover:

- How to set up folders and where each file is saved
- Order in which to run code
- Explanations of features used
- Environment for the code to be run (conda environment.yml file or an environment.txt file)
- Hardware needed (e.g. Google Colab or the specifications of your local machine)
- Expected run time for each notebook. This will be useful to the review team for time and resource allocation.

Your code needs to run properly, code reviewers do not have time to debug code. If code does not run easily you will be bumped down the leaderboard.


#### Consequences of breaking any rules of the challenge or submission guidelines:

- First offence: No prizes for 6 months and 2000 points will be removed from your profile (probation period). If you are caught cheating, all individuals involved in cheating will be disqualified from the challenge(s) you were caught in and you will be disqualified from winning any challenges for the next six months and 2000 points will be removed from your profile. If you have less than 2000 points to your profile your points will be set to 0.

- Second offence: Banned from the platform. If you are caught for a second time your Zindi account will be disabled and you will be disqualified from winning any challenges or Zindi points using any other account.

- Teams with individuals who are caught cheating will not be eligible to win prizes or points in the challenge in which the cheating occurred, regardless of the individuals’ knowledge of or participation in the offence.

- Teams with individuals who have previously committed an offence will not be eligible for any prizes for any challenges during the 6-month probation period.

#### Monitoring of submissions

- We will review the top 10 solutions of every challenge when the challenge ends.
- We reserve the right to request code from any user at any time during a challenge. You will have 24 hours to submit your code following the rules for code review (see above). Zindi reserves the right not to explain our reasons for requesting code. If you do not submit your code within 24 hours you will be disqualified from winning any challenges or Zindi points for the next six months. If you fall under suspicion again and your code is requested and you fail to submit your code within 24 hours, your Zindi account will be disabled and you will be disqualified from winning any challenges or Zindi points with