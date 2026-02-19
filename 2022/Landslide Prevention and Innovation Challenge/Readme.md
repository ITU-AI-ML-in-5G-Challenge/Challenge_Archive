# Landslide Prevention and Innovation Challenge

## Can you identify if a landslide occurred or not?


Link to Zindi: https://zindi.africa/competitions/landslide-prevention-and-innovation-challenge

The core of our challenge is to design and shape the future of <b>landslide prevention and management</b> with the example of Hong Kong.

[Here you can find a great article from BBC why this is an urgent topic!](https://www.bbc.com/future/article/20220225-how-hong-kong-protects-people-from-its-deadly-landslides)

Hong Kong, one of the hilliest and most densely populated cities in the world, is frequently hit by extreme rainfall and is therefore highly susceptible to rain-induced landslides. A landslide is the movement of masses of rock, debris, or earth down a slope and can result in significant loss of life and property. A high-quality landslide inventory is essential not only for landslide hazard and risk analysis but also for supporting agency decisions on landslide hazard mitigation and prevention.

As the <b>common practice is visual, labour-intensive inspection</b>, this hack focuses on automating <b>landslide identification using artificial intelligenc</b> techniques and embedding this solution into the creative vision: “Artificial Intelligence for landslide Identification”

<b>About the Focus Group on AI for Natural Disaster Management</b>

The Focus Group on AI for Natural Disaster Management (FG-AI4NDM) began as a collaboration between International Telecommunication Union (ITU), World Meteorological Organization (WMO), and United Nations Environment Programme (UNEP). AI in combination with other tools can enhance situational awareness of natural hazards worldwide. The aim of FG-AI4NDM is to provide the groundwork for best practices in the use of AI for the application of natural disaster management. Each UN organization brings a different set of expertise that is crucial for identifying AI best practices in the field of natural disaster management. The areas of natural disaster management include earthquakes, floods, tsunamis, insect plagues, landslides, avalanches, wildfires, vector-borne diseases, volcanic eruptions, hail and windstorms, and multihazards.

![fig](iaforgood.png)

ITU specializes in information and communication technologies and has brokered agreements on technologies. ITU’s knowledge of AI can be leveraged through their participation with the group. They help to understand the process of data collection and handling and modeling across spatiotemporal scales.

WMO brings experience with decision-making and planning processes within disaster risk and emergency management. The WMO Disaster Risk Reduction Program and Multi-Hazard Early Warning System are direct applications of natural disaster management to help protect lives, livelihoods and property from natural disasters. WMO also facilitates free and unrestricted exchange of data and services related to safety and security of society, economic welfare, and protection of the environment

UNEP aims to reduce the impacts of natural hazards, industrial accidents, and conflicts on vulnerable communities and countries through sustainable means. UNEP raises awareness of the risks posed to the environment and supports countries in risk reduction policies. In particular, the Disasters and Conflicts Branch of UNEP investigates, explores, and contributes to how modern technologies are used in the field of disaster management.

These three organizations, along with external parties, collaborate and share their own expertise to create a set of documents that will give guidance on best practices in applying AI within the field of natural disaster management. This group collects the top minds in the field to share their experiences with using AI, experiences with natural disasters, and experiences with fitting these two concepts together to better predict, detect, and respond to natural disasters, including landslide detection.

#### About Hong Kong University Landslide Research

Landslide management is already a big issue in Hong Kong, but the use of AI can help to transform it. There are several research projects about that right now. The dataset was created by Hong Kong University of Science and Technology.

#### About Zindi

Zindi provides a global platform to launch a hackathon. Specializing in Africa, Zindi hosts a data science ecosystem that welcomes competitions from a variety of sources: scientists, engineers, academics, companies, NGOs, governments, and institutions.

After the successful in-person March 2022 hackathon in St. Gallen, Switzerland, the competition is expanding to any and all participants in the world to support the work of landslide detection thanks to Zindi’s platform. Zindi focuses on solving Africa’s most pressing problems and participants will have the opportunity to use data from the Hong Kong University of Science and Technology to create a tool that could have significance on a global scale, including in Africa and other developing areas of the world.

#### About AI for Good - International Telecommunication Union (ITU)

![fig](iaforgood.png)

AI for Good is organized by ITU in partnership with 40 UN Sister Agencies. The goal of AI for Good is to identify practical applications of AI to advance the United Nations Sustainable Development Goals and scale those solutions for global impact. It’s the leading action-oriented, global & inclusive United Nations platform on AI.


### Evaluation
The error metric for this competition is the F1 score, which ranges from 0 (total failure) to 1 (perfect score). Hence, the closer your score is to 1, the better your model.

F1 Score: A performance score that combines both precision and recall. It is a harmonic mean of these two variables. Formula is given as: 2*Precision*Recall/(Precision + Recall)

Precision: This is an indicator of the number of items correctly identified as positive out of total items identified as positive. Formula is given as: TP/(TP+FP)

Recall / Sensitivity / True Positive Rate (TPR): This is an indicator of the number of items correctly identified as positive out of total actual positives. Formula is given as: TP/(TP+FN)

Where:

TP=True Positive
FP=False Positive
TN=True Negative
FN=False Negative
You may use R or Python to code your solution, we recommend using Google Colab as it allows access to GPUs.

Your submission should look like (where 1 indicates positive and 0 indicates negative):

| ID        | LABEL |
|-----------|--------|
| 00OADRP |1   |
| 012YMY8  | 0  |
| 014E83I  | 1  |




### Prizes

Opportunity to have a personal one-on-one meeting with a Focus Group Representative. You will all have the chance to interact with experts in the field of AI and specialists in the field of disaster management, learn about their projects, ask questions relating to their work, advice on career growth or any other questions you may have!

In addition, you will receive a special invite to remotely join our next Meeting of the Focus Group on AI for Natural Disaster Management from 24 - 26 October.

There are 3000 Zindi points for this challenge. You can read more about Zindi points [here](https://zindi.africa/discussions/13959?utm_source=zindi&utm_medium=blog&utm_campaign=challenge_resources&utm_id=CR).


Participants are required to submit:

1. A CSV file containing model predictions (online leaderboard);
2. The developed model code;
3. A report explaining their solution, including the outcomes of their models. The technical report will be used to judge the novelty/originality and usefulness of the proposed methodology
4. Participants will be required to present their solutions to an ITU Challenge Finale session

In evaluating the final submission, both the quality of the report (weighted 40%) and the achieved model score (weighted 60%) will be considered.

### Timeline

Competition closes on 30 September 2022.

Final submissions must be received by 11:59 PM GMT.

We reserve the right to update the contest timeline if necessary.


### Rules

This challenge is open to all.

#### Teams and collaboration

You may participate in challenges as an individual or in a team of up to four people. When creating a team, the team must have a total submission count less than or equal to the maximum allowable submissions as of the formation date. A team will be allowed the maximum number of submissions for the challenge, minus the total number of submissions among team members at team formation. Prizes are transferred only to the individual players or to the team leader.

Multiple accounts per user are not permitted, and neither is collaboration or membership across multiple teams. Individuals and their submissions originating from multiple accounts will be immediately disqualified from the platform.

Code must not be shared privately outside of a team. Any code that is shared, must be made available to all challenge participants through the platform. (i.e. on the discussion boards).

The Zindi data scientist who sets up a team is the default Team Leader but they can transfer leadership to another data scientist on the team. The Team Leader can invite other data scientists to their team. Invited data scientists can accept or reject invitations. Until a second data scientist accepts an invitation to join a team, the data scientist who initiated a team remains an individual on the leaderboard. No additional members may be added to teams within the final 5 days of the challenge or last hour of a hackathon.

The team leader can initiate a merge with another team. Only the team leader of the second team can accept the invite. The default team leader is the leader from the team who initiated the invite. Teams can only merge if the total number of members is less than or equal to the maximum team size of the challenge.

A team can be disbanded if it has not yet made a submission. Once a submission is made individual members cannot leave the team.

All members in the team receive points associated with their ranking in the challenge and there is no split or division of the points between team members.

#### Datasets and packages

The solution must use publicly-available, open-source packages only.

You may use only the datasets provided for this challenge.

You may use pretrained models as long as they are openly available to everyone.

Automated machine learning tools such as automl are not permitted.

If the error metric requires probabilities to be submitted, do not set thresholds (or round your probabilities) to improve your place on the leaderboard. In order to ensure that the client receives the best solution Zindi will need the raw probabilities. This will allow the clients to set thresholds to their own needs.

You are allowed to access, use and share challenge data for any commercial, non-commercial, research or education purposes, under a CC-BY SA 4.0 license.

You must notify Zindi immediately upon learning of any unauthorised transmission of or unauthorised access to the challenge data, and work with Zindi to rectify any unauthorised transmission or access.

Your solution must not infringe the rights of any third party and you must be legally entitled to assign ownership of all rights of copyright in and to the winning solution code to Zindi.

#### Submissions and winning

You may make a maximum of 10 submissions per day.

You may make a maximum of 300 submissions for this challenge.

Before the end of the challenge you need to choose 2 submissions to be judged on for the private leaderboard. If you do not make a selection your 2 best public leaderboard submissions will be used to score on the private leaderboard.

During the challenge, your best public score will be displayed regardless of the submissions you have selected. When the challenge closes your best private score out of the 2 selected submissions will be displayed.

Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 30% of the test dataset. While the challenge is open, the Public Leaderboard will rank the submitted solutions by the accuracy score they achieve. Upon close of the challenge, the Private Leaderboard, which covers the other 70% of the test dataset, will be made public and will constitute the final ranking for the challenge.

Note that to count, your submission must first pass processing. If your submission fails during the processing step, it will not be counted and not receive a score; nor will it count against your daily submission limit. If you encounter problems with your submission file, your best course of action is to ask for advice on the challenge page.

If you are in the top 10 at the time the leaderboard closes, we will email you to request your code. On receipt of email, you will have 48 hours to respond and submit your code following the Reproducibility of submitted code guidelines detailed below. Failure to respond will result in disqualification.

If your solution places 1st, 2nd, or 3rd on the final leaderboard, you will be required to submit your winning solution code to us for verification, and you thereby agree to assign all worldwide rights of copyright in and to such winning solution to Zindi.

If two solutions earn identical scores on the leaderboard, the tiebreaker will be the date and time in which the submission was made (the earlier solution will win).

The winners will be paid via bank transfer, PayPal if payment is less than or equivalent to $100, or other international money transfer platform. International transfer fees will be deducted from the total prize amount, unless the prize money is under $500, in which case the international transfer fees will be covered by Zindi. In all cases, the winners are responsible for any other fees applied by their own bank or other institution for receiving the prize money. All taxes imposed on prizes are the sole responsibility of the winners. The top winners or team leaders will be required to present Zindi with proof of identification, proof of residence and a letter from your bank confirming your banking details. Winners will be paid in USD or the currency of the challenge. If your account cannot receive US Dollars or the currency of the challenge then your bank will need to provide proof of this and Zindi will try to accommodate this.

Please note that due to the ongoing Russia-Ukraine conflict, we are not currently able to make prize payments to winners located in Russia. We apologise for any inconvenience that may cause, and will handle any issues that arise on a case-by-case basis.

Payment will be made after code review and sealing the leaderboard.

You acknowledge and agree that Zindi may, without any obligation to do so, remove or disqualify an individual, team, or account if Zindi believes that such individual, team, or account is in violation of these rules. Entry into this challenge constitutes your acceptance of these official challenge rules.

Zindi is committed to providing solutions of value to our clients and partners. To this end, we reserve the right to disqualify your submission on the grounds of usability or value. This includes but is not limited to the use of data leaks or any other practices that we deem to compromise the inherent value of your solution.

Zindi also reserves the right to disqualify you and/or your submissions from any challenge if we believe that you violated the rules or violated the spirit of the challenge or the platform in any other way. The disqualifications are irrespective of your position on the leaderboard and completely at the discretion of Zindi.

Please refer to the FAQs and Terms of Use for additional rules that may apply to this challenge. We reserve the right to update these rules at any time.

#### Reproducibility of submitted code

If your submitted code does not reproduce your score on the leaderboard, we reserve the right to adjust your rank to the score generated by the code you submitted.

If your code does not run you will be dropped from the top 10. Please make sure your code runs before submitting your solution.

Always set the seed. Rerunning your model should always place you at the same position on the leaderboard. When running your solution, if randomness shifts you down the leaderboard we reserve the right to adjust your rank to the closest score that your submission reproduces.

Custom packages in your submission will not be accepted.

All data manipulation must be done in code, manual manipulation via manual labelling or Excel will lead to disqualification.

You may only use tools available to everyone i.e. no paid services or free trials that require a credit card.

Read this [article](https://zindi.africa/learn/documentation-guideline) on how to prepare your documentation and this article on how to ensure a successful code review.



#### Data standards:

- Your submitted code must run on the original train, test, and other datasets provided.
- If external data is allowed, external data must be freely and publicly available, including pre-trained models with standard libraries. If external data is allowed, any data used should be shared with Zindi to be approved and then shared on the discussion forum. Zindi will also make note of the external data available on the data page.
- Packages:
- You must submit a requirements file with all packages and versions used.
- If a requirements file is not provided, solutions will be run on the most recent packages available.
- Custom packages in your submission notebook will not be accepted.
- You may only use tools available to everyone i.e. no paid services or free trials that require a credit card.

#### Consequences of breaking any rules of the challenge or submission guidelines:

- First offence: No prizes for 6 months and 2000 points will be removed from your profile (probation period). If you are caught cheating, all individuals involved in cheating will be disqualified from the challenge(s) you were caught in and you will be disqualified from winning any challenges for the next six months and 2000 points will be removed from your profile. If you have less than 2000 points to your profile your points will be set to 0.
- Second offence: Banned from the platform. If you are caught for a second time your Zindi account will be disabled and you will be disqualified from winning any challenges or Zindi points using any other account.
- Teams with individuals who are caught cheating will not be eligible to win prizes or points in the challenge in which the cheating occurred, regardless of the individuals’ knowledge of or participation in the offence.
- Teams with individuals who have previously committed an offence will not be eligible for any prizes for any challenges during the 6-month probation period.

#### Monitoring of submissions

- We will review the top 10 solutions of every challenge when the challenge ends.
- We reserve the right to request code from any user at any time during a challenge. You will have 24 hours to submit your code following the rules for code review (see above). Zindi reserves the right not to explain our reasons for requesting code. If you do not submit your code within 24 hours you will be disqualified from winning any challenges or Zindi points for the next six months. If you fall under suspicion again and your code is requested and you fail to submit your code within 24 hours, your Zindi account will be disabled and you will be disqualified from winning any challenges or Zindi points with any other account.