# GeoAI Aquaculture Pond Identification Challenge

Source: https://zindi.africa/competitions/geoai-aquaculture-pond-identification-challenge

Can you identify aquaculture ponds from space?

Aquaculture ponds are used to farm fish and shrimp in controlled water environments. They are easier to manage and more productive than open-water fishing. But to monitor them effectively, we first need to know where they are. Satellite imagery offers a reliable way to map these ponds across large areas, providing up-to-date information that supports water management, environmental monitoring, and policy decisions, especially in regions where ground-level data is hard to come by.

Your goal is to build a machine learning model that predicts whether a given location is an aquaculture pond or another type of land cover, using features derived from satellite data. Each location represents a 10m × 10m patch of ground, so your model needs to be precise.

There is an added challenge: your model will be trained on data from one time period and tested on data from a different one. This means your solution must remain accurate as conditions change across seasons and years - not just perform well on familiar data.

By taking part in this challenge, you will contribute to global efforts in agricultural land mapping and support progress towards the United Nations Sustainable Development Goals (SDGs) for 2030.

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/3355/2e4d482e-b5bd-458a-b672-5603c1cc49c0.png)

About [FAO](https://www.fao.org/home/en)

The Food and Agriculture Organization (FAO) is a specialized agency of the United Nations that leads international efforts to defeat hunger. Its goal is to achieve food security for all and ensure that people have regular access to enough high-quality food to lead active, healthy lives.

About [AI for Good - International Telecommunication Union (ITU)](https://aiforgood.itu.int/about-us/un-ai-actions/itu/)

AI for Good is organized by ITU in partnership with 40 UN Sister Agencies. The goal of AI for Good is to identify practical applications of AI to advance the United Nations Sustainable Development Goals and scale those solutions for global impact. It’s the leading action-oriented, global & inclusive United Nations platform on AI.

Evaluation

There is a two-phase evaluation process for this challenge; the first phase is based on your leaderboard score, followed by a rubric evaluation for the top 5 on the leaderboard.

### Phase One: Leaderboard Evaluation
The challenge uses [multi-metric evaluation](https://zindi.africa/learn/introducing-multi-metric-evaluation-or-one-metric-to-rule-them-all) for the leaderboard ranking. The two metrics used in this phase are [F1-Score](https://zindi.africa/learn/zindi-error-metric-series-how-to-use-the-f1-score) and [ROC-AUC](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.roc_auc_score.html). The final leaderboard score is the weighted average of the two:

- F1-Score (60%) — provides a balanced measure of model effectiveness by considering both precision and recall, which are crucial for imbalanced datasets where aquaculture ponds represent a small fraction of all locations
- ROC-AUC (40%) — measures how well the model ranks aquaculture pond locations above non-pond locations across all possible thresholds, providing a stable assessment of overall classification performance regardless of class imbalance
Your model must output:

- A binary target indicating whether the location is an aquaculture pond or other
- A probability indicating the likelihood that the location is an aquaculture pond
Setting a probability threshold is strictly forbidden. Your binary target should be based on the default threshold of 0.5.

Phase One Evaluation (65%): Points will be awarded based on the leaderboard position: 1st place receives 10 points, 2nd place receives 9 points, and so on with 5th place receiving 6 points.

### Phase Two Evaluation
Innovation and Practicality (35%): Scores will be assigned according to the following criteria:

- 0 points: The solution is not reproducible.
- 2-5 points: The solution is reproducible, but the workflow is unclear and the explanation is vague.
- 6-8 points: The solution is reproducible, with a clear workflow and an adequate explanation of its novelty.
- 9-10 points: The solution is reproducible, and the workflow is well aligned with the proposed approach. The submission clearly explains the key challenges and how they were addressed.
The submission file should follow this format:

```
ID                      TargetF1         TargetRAUC
ID_TS_xUR2T2                1                0.87
ID_TS_yN4Ale                0                0.12 
```

Prizes

🥇 1st prize: 500 CHF

🥈2nd prize: 300 CHF

🥉3rd prize: 200 CHF

There are 1 000 Zindi points available. You can read more about [Zindi points here](https://zindi.africa/discussions/13959?utm_source=zindi&utm_medium=blog&utm_campaign=challenge_resources&utm_id=CR).
Rules

- Languages and tools: You may only use open-source languages and tools in building models for this challenge.
- Who can compete: Open to all
- Maximum 1,000 training samples per pilot region, including self-collected samples
- Submitted scripts are limited to Python and Google Earth Engine JavaScript
- Code must be reproducible end-to-end from raw data to output maps
- Submission Limits: 5 submissions per day, 100 submissions overall.
- Team size: Max team size of 4
- Public-Private Split: Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 30% of the test dataset. The private leaderboard will be revealed at the close of the challenge and contains the remaining 70% of the test set.
- Data Sharing: CC-BY SA 4.0 license
- Code Review: Top 5 on the private leaderboard will receive an email requesting their code at the close of the challenge. You will have 48 hours to submit your code.
- Code sharing: Multiple accounts, or sharing of code and information across accounts not in teams, is not allowed and will lead to disqualification.
ENTRY INTO THIS CHALLENGE CONSTITUTES YOUR ACCEPTANCE OF THESE OFFICIAL CHALLENGE RULES.

Full Challenge Rules

This challenge is open to all.

Teams and collaboration

You may participate in challenges as an individual or in a team of up to four people. When creating a team, the team must have a total submission count less than or equal to the maximum allowable submissions as of the formation date. A team will be allowed the maximum number of submissions for the challenge, minus the total number of submissions among team members at team formation. Prizes are transferred only to the individual players or to the team leader.

Multiple accounts per user are not permitted, and neither is collaboration or membership across multiple teams. Individuals and their submissions originating from multiple accounts will be immediately disqualified from the platform.

Code must not be shared privately outside of a team. Any code that is shared, must be made available to all challenge participants through the platform. (i.e. on the discussion boards).

The Zindi data scientist who sets up a team is the default Team Leader but they can transfer leadership to another data scientist on the team. The Team Leader can invite other data scientists to their team. Invited data scientists can accept or reject invitations. Until a second data scientist accepts an invitation to join a team, the data scientist who initiated a team remains an individual on the leaderboard. No additional members may be added to teams within the final 5 days of the challenge or last hour of a hackathon.

The team leader can initiate a merge with another team. Only the team leader of the second team can accept the invite. The default team leader is the leader from the team who initiated the invite. Teams can only merge if the total number of members is less than or equal to the maximum team size of the challenge.

A team can be disbanded if it has not yet made a submission. Once a submission is made individual members cannot leave the team.

All members in the team receive points associated with their ranking in the challenge and there is no split or division of the points between team members.

Datasets, packages and general principles

The solution must use publicly-available, open-source packages only.

You may use only the datasets provided for this challenge.

You may use pretrained models as long as they are openly available to everyone.

Automated machine learning tools such as automl are not permitted.

If the error metric requires probabilities to be submitted, do not set thresholds (or round your probabilities) to improve your place on the leaderboard. In order to ensure that the client receives the best solution Zindi will need the raw probabilities. This will allow the clients to set thresholds to their own needs.

You are allowed to access, use and share challenge data for any commercial, non-commercial, research or education purposes, under a CC-BY SA 4.0 license.

You must notify Zindi immediately upon learning of any unauthorised transmission of or unauthorised access to the challenge data, and work with Zindi to rectify any unauthorised transmission or access.

Your solution must not infringe the rights of any third party and you must be legally entitled to assign ownership of all rights of copyright in and to the winning solution code to Zindi.

Submissions and winning

You may make a maximum of 5 submissions per day.

You may make a maximum of 100 submissions for this challenge.

Before the end of the challenge you need to choose 2 submissions to be judged on for the private leaderboard. If you do not make a selection your 2 best public leaderboard submissions will be used to score on the private leaderboard.

During the challenge, your best public score will be displayed regardless of the submissions you have selected. When the challenge closes your best private score out of the 2 selected submissions will be displayed.

Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 30% of the test dataset. While the challenge is open, the Public Leaderboard will rank the submitted solutions by the accuracy score they achieve. Upon close of the challenge, the Private Leaderboard, which covers the other 70% of the test dataset, will be made public and will constitute the final ranking for the challenge.

Note that to count, your submission must first pass processing. If your submission fails during the processing step, it will not be counted and not receive a score; nor will it count against your daily submission limit. If you encounter problems with your submission file, your best course of action is to ask for advice on the challenge page.

If you are in the top 5 at the time the leaderboard closes, we will email you to request your code. On receipt of email, you will have 48 hours to respond and submit your code following the Reproducibility of submitted code guidelines detailed below. Failure to respond will result in disqualification.

If your solution places 1st, 2nd, or 3rd on the final leaderboard, you will be required to submit your winning solution code to us for verification, and you thereby agree to assign all worldwide rights of copyright in and to such winning solution to Zindi.

If two solutions earn identical scores on the leaderboard, the tiebreaker will be the date and time in which the submission was made (the earlier solution will win).

The winners will be paid via bank transfer, PayPal if payment is less than or equivalent to $100, or other international money transfer platform. International transfer fees will be deducted from the total prize amount, unless the prize money is under $500, in which case the international transfer fees will be covered by Zindi. In all cases, the winners are responsible for any other fees applied by their own bank or other institution for receiving the prize money. All taxes imposed on prizes are the sole responsibility of the winners. The top winners or team leaders will be required to present Zindi with proof of identification, proof of residence and a letter from your bank confirming your banking details. Winners will be paid in USD or the currency of the challenge. If your account cannot receive US Dollars or the currency of the challenge then your bank will need to provide proof of this and Zindi will try to accommodate this.

Please note that due to the ongoing Russia-Ukraine conflict, we are not currently able to make prize payments to winners located in Russia. We apologise for any inconvenience that may cause, and will handle any issues that arise on a case-by-case basis.

Payment will be made after code review and sealing the leaderboard.

You acknowledge and agree that Zindi may, without any obligation to do so, remove or disqualify an individual, team, or account if Zindi believes that such individual, team, or account is in violation of these rules. Entry into this challenge constitutes your acceptance of these official challenge rules.

Zindi is committed to providing solutions of value to our clients and partners. To this end, we reserve the right to disqualify your submission on the grounds of usability or value. This includes but is not limited to the use of data leaks or any other practices that we deem to compromise the inherent value of your solution.

Zindi also reserves the right to disqualify you and/or your submissions from any challenge if we believe that you violated the rules or violated the spirit of the challenge or the platform in any other way. The disqualifications are irrespective of your position on the leaderboard and completely at the discretion of Zindi.

Please refer to the FAQs and Terms of Use for additional rules that may apply to this challenge. We reserve the right to update these rules at any time.

Reproducibility of submitted code

If your submitted code does not reproduce your score on the leaderboard, we reserve the right to adjust your rank to the score generated by the code you submitted.

If your code does not run you will be dropped from the top 5. Please make sure your code runs before submitting your solution.

Always set the seed. Rerunning your model should always place you at the same position on the leaderboard. When running your solution, if randomness shifts you down the leaderboard we reserve the right to adjust your rank to the closest score that your submission reproduces.

Custom packages in your submission notebook will not be accepted.

You may only use tools available to everyone i.e. no paid services or free trials that require a credit card.

Read [this article](https://zindi.africa/learn/documentation-guideline) on how to prepare your documentation and [this article](https://zindi.africa/learn/how-to-ensure-success-when-submitting-your-code-for-review) on how to ensure a successful code review.

Consequences of breaking any rules of the challenge or submission guidelines:

- First offence: No prizes for 6 months and 2000 points will be removed from your profile (probation period). If you are caught cheating, all individuals involved in cheating will be disqualified from the challenge(s) you were caught in and you will be disqualified from winning any challenges for the next six months and 2000 points will be removed from your profile. If you have less than 2000 points to your profile your points will be set to 0.
- Second offence: Banned from the platform. If you are caught for a second time your Zindi account will be disabled and you will be disqualified from winning any challenges or Zindi points using any other account.
Teams with individuals who are caught cheating will not be eligible to win prizes or points in the challenge in which the cheating occurred, regardless of the individuals’ knowledge of or participation in the offence.

Teams with individuals who have previously committed an offence will not be eligible for any prizes for any challenges during the 6-month probation period.

Monitoring of submissions

We will review the top 5 solutions of every challenge when the challenge ends.

We reserve the right to request code from any user at any time during a challenge. You will have 24 hours to submit your code following the rules for code review (see above). Zindi reserves the right not to explain our reasons for requesting code. If you do not submit your code within 24 hours you will be disqualified from winning any challenges or Zindi points for the next six months. If you fall under suspicion again and your code is requested and you fail to submit your code within 24 hours, your Zindi account will be disabled and you will be disqualified from winning any challenges or Zindi points with any other account.
