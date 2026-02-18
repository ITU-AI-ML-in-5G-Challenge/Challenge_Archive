# Runmila AI Institute & minoHealth AI Labs Tuberculosis Classification via X-Rays Challenge

## Build an AI system that can classify Tuberculosis and Normal X-Ray images


Link to Zindi: https://zindi.africa/competitions/runmila-ai-institute-minohealth-ai-labs-tuberculosis-classification-via-x-rays-challenge

Tuberculosis (TB) is the ninth leading cause of death worldwide. In 2016, an estimated 417,000 people died from Tuberculosis in Africa, and 1.7 million globally. In South Africa Tuberculosis is the leading cause of death with 450,000 people developing the disease every year and 89,000 people dying from it. That’s ten people every hour.

With over 800,000 confirmed cases and 18,000 deaths recorded in Africa and over 17 million confirmed cases and 670,000 recorded deaths globally as of August 2, 2020, the COVID-19 global pandemic continues to take a heavy toll around the world. In countries with a high prevalence level of TB, TB can create additional complexity to the COVID-19 response. And by the same token, COVID-19 is adding new complexity to the ongoing battle against TB.

For both TB and COVID-19 patients, medical imaging (Chest X-Rays and/or CT Scans) can sometimes be performed to identify and manage any chest abnormalities that may develop.

This challenge asks you to build an AI model that can classify Tuberculosis and Normal X-Ray results. With Tuberculosis infections still active as the COVID-19 pandemic continues, an automated tool to help identify TB has the potential to reduce hospital workload and optimize patient care during a time when hospitals are being overwhelmed by COVID-19 cases.

#### Disclaimer

This challenge is solely for educational purposes. Chest X-Rays is one of various tools that can be used for triaging and screening for Tuberculosis. Furthermore, it is possible for an individual to develop different types of infections. This is to be treated purely as an exercise in tool development.

One potential follow up of this research is the detection of specific chest abnormalities associated with either COVID-19 or Tuberculosis, which could help in the development of personalised treatment for patients. Promising projects are eligible, but not guaranteed for additional mentoring into a publication.

#### Acknowledgements

Montgomery County X-ray Set: X-ray images in this data set have been acquired from the tuberculosis control program of the Department of Health and Human Services of Montgomery County, MD, USA.

Shenzhen Hospital X-ray Set: X-ray images in this data set have been collected by Shenzhen No.3 Hospital in Shenzhen, Guangdong province, China. The x-rays were acquired as part of the routine care at Shenzhen Hospital.

It is requested that publications resulting from the use of this data attribute the source (National Library of Medicine, National Institutes of Health, Bethesda, MD, USA and Shenzhen No.3 People’s Hospital, Guangdong Medical College, Shenzhen, China) and cite the following publications:

- Jaeger S, Karargyris A, Candemir S, Folio L, Siegelman J, Callaghan F, Xue Z, Palaniappan K, Singh RK, Antani S, Thoma G, Wang YX, Lu PX, McDonald CJ. Automatic tuberculosis screening using chest radiographs. IEEE Trans Med Imaging. 2014 Feb;33(2):233-45. doi: 10.1109/TMI.2013.2284099. PMID: 24108713
- Candemir S, Jaeger S, Palaniappan K, Musco JP, Singh RK, Xue Z, Karargyris A, Antani S, Thoma G, McDonald CJ. Lung segmentation in chest radiographs using anatomical atlases with nonrigid registration. IEEE Trans Med Imaging. 2014 Feb;33(2):577-90. doi: 10.1109/TMI.2013.2290491. PMID: 24239990

#### [About minoHealth](runchbase.com/organization/minohealth)

![fig](iaforgood.png)

<b>minoHealth</b> is a startup and multifaceted system with the objective of democratising Quality Healthcare with innovative and cutting edge technologies like Artificial Intelligence, (Big) Data Analytics and Cloud computing in Africa. minoHealth‘s AI Research lab, minoHealth AI Labs researches and experiments with Artificial Intelligence and ways it can be applied to Healthcare to make it faster, better and yet cheaper. They research and apply Artificial Intelligence to fields like Biotechnology, Neuroscience, Optometry, Epidemiology and Dietetics/Nutrition. Their research projects include ‘ScaffoldNet: Detecting and Classifying Biomedical Polymer-Based Scaffolds via a Convolutional Neural Network’, published in the Scientific Book, “Advances In Information and Communication” and “End-to-End Learning via a Convolutional Neural Network for Cancer Cell Line Classification” published in Journal of Industry - University Collaboration. Their ongoing research projects also includes a collaboration with West African Centre for Cell Biology of Infectious Pathogens (WACCBIP) on the use of Machine Learning in the identification of a multivariate signature for Malaria Immunity. They are members of Massachusett Institute of Technology (MIT)'s Global ​BioSummit Community. They are also the lead for the Topic Group on Artificial Intelligence for Radiology, under the United Nations International Telecommunication Union (ITU) and World Health Organization (WHO) Focus Group on Artificial Intelligence for Health (FG-AI4H). minoHealth’s platform was listed in AppsAfrica’s ‘5 African innovations disrupting traditional sectors’.

#### [About Runmila AI Institute](runmilainstitute.com)

![fig](iaforgood1.png)

<b>reRunmila AI Institute</b> is dedicated to preparing Ghana, and the rest of Africa for an Artificial Intelligence (AI) Future and the 4th Industrial Revolution. The world is drastically changing with all leading nations and blocs creating AI Plans & Strategies. Furthermore, plenty of these leading nations and blocs have already started implementing these strategies; Africa shouldn't be left behind. Through the skillful use of AI, we can leapfrog our development and solve many of Africa's grand challenges, especially connected to the 'Sustainable Development Goals (SDGs)'. Our goal is to train the talents that Africa requires to build this AI Future that the continent deserves and needs. We are doing this by equipping Africans, starting with Ghanaians, with practical skills in AI (Deep Learning & Machine Learning) and Data Science.

Our courses and workshops are practical, being Development-focused and designed around optimally teaching complex concepts in a fast and easy-to-grasp approach. Our students take away skills to develop their own AI projects that they can readily implement for their needs and demonstrate to would-be investors or employers. These courses and workshops are crafted by Artificial Intelligence Engineers and Researchers who are already working on real world applications of Artificial Intelligence in Africa.


### Evaluation
The evaluation metric for this competition is the Area Under the ROC curve (AUC).

Your sample submission should look like, where LABEL is the probabiltiy that the lung x-ray is TB-positive. Please keep your values as probabilities.:

| ID        | LABEL |
|-----------|--------|
| GTWSHFYQ  | 0.45   |
| QTFSSMGD  | 0.32   |
| TBLBHSYT  | 0.91   |




### Prizes

There are no cash prizes for this challenge.

However, the top 10 submissions will earn up to 2000 Zindi Points.

And the first 5 users/teams that beat benchmark_1 on the leaderboard will receive tickets to AI Expo Africa on 3-4 September 2020 (a completely virtual event this year), worth approx. $50 USD each.

There are 3000 Zindi points for this challenge. You can read more about Zindi points [here](https://zindi.africa/discussions/13959?utm_source=zindi&utm_medium=blog&utm_campaign=challenge_resources&utm_id=CR).


Participants are required to submit:

1. A CSV file containing model predictions (online leaderboard);
2. The developed model code;
3. A report explaining their solution, including the outcomes of their models. The technical report will be used to judge the novelty/originality and usefulness of the proposed methodology
4. Participants will be required to present their solutions to an ITU Challenge Finale session

In evaluating the final submission, both the quality of the report (weighted 40%) and the achieved model score (weighted 60%) will be considered.

### Timeline

Competition closes on 15 November 2020.

Final submissions must be received by 11:59 PM GMT.

We reserve the right to update the contest timeline, if necessary.


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