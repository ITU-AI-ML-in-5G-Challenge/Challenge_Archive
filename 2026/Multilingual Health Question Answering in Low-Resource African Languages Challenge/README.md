# Multilingual Health Question Answering in Low-Resource African Languages Challenge

Source: https://zindi.africa/competitions/multilingual-health-question-answering-in-low-resource-african-languages-challenge

Can you build the multilingual health assistant Africa's communities deserve?

Access to reliable health information remains a critical challenge across sub-Saharan Africa. Language barriers frequently prevent communities from receiving clear, accurate health guidance in their native tongue – particularly on sensitive topics such as maternal, sexual and reproductive health (MSRH), where the ability to ask questions privately and receive answers in one's own language can be the difference between informed decision-making and harmful misinformation.

Models trained predominantly on English language data struggle to understand, reason, and generate fluent responses in languages such as Luganda, Kiswahili, Akan and Amharic – leaving hundreds of millions of speakers underserved by the very technology that could help them most.

Your task is to build a multilingual model capable of accurately answering health-related questions in low-resource African languages. Using a text-based dataset of curated health question-and-answer pairs. Your model should understand a question posed in any of the supported languages and generate a fluent, accurate, and contextually appropriate response in the same language.

A strong model for this challenge could power practical tools such as health worker assistants, patitent education platforms, and clinic support systems in rural and underserved communities.

Please [sign up](https://luma.com/up1d3tea?tk=0siM7m) for the upcoming challenge webinar on May 20, 6:00 - 7:00 PM GMT+2

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/3195/7f8fb662-3d99-4ac4-bdee-7a0f46cc4756.png)

[Hub for Artificial Intelligence in Maternal, Sexual and Reproductive Health (HASH)](https://hash.theacademy.co.ug/)

HASH is a multidisciplinary consortium bringing together health professionals, computer scientists, data scientists, social scientists, and public health experts. It is driven by the aspiration to address the critical challenges in maternal, sexual, and reproductive health across Sub-Saharan Africa, while leveraging the emerging opportunities presented by Artificial Intelligence (AI). The HASH consortium members include: Infectious Disease Institute (IDI) Makerere University, Makerere Centre for Artificial Intelligence (MAK-AI) and Sunbird AI. The Hub focuses on four key research priority areas: maternal health, sexually transmitted infections, adolescent sexual and reproductive health, and HIV. Through evidence and best practices, it seeks to elevate the role of AI in the health sector and convene a community of enthusiasts and experts to develop locally grounded solutions tailored to the African context.

Evaluation

The first phase of this challenge uses [multi-metric evaluation](https://zindi.africa/learn/introducing-multi-metric-evaluation-or-one-metric-to-rule-them-all). The three metrics are: ROUGE-1 F1, ROUGE-L F1 and the LLM-as-a-Judge.

The final score on the leaderboard is the weighted mean of the three evaluation metrics.

Metric Weighting

ROUGE-1 F1 0.37

ROUGE-L F1 0.37

LLM-as-a-Judge 0.26

- ROUGE-1 F1 uses ROUGE via the [rouge-score library](https://pypi.org/project/rouge-score/). It acts as a lexical overlap metric which measures overlap of unigrams (individual words) between reference and prediction. It captures the basic content similarity and keyword matching. This metric does not account for meaning and paraphrasing.
- ROUGE-L F1 uses ROUGE via the [rouge-score library](https://pypi.org/project/rouge-score/). It measures similarity based on the Longest Common Subsequence (LCS) between reference and prediction. It captures sentence-level structure and fluency alignment.
- LLM-as-a-Judge acts a human-like evaluator. It reads both the reference and predicted answer and scores the prediction on a scale of 1-5 based on factual accuracy, completeness, language appropriateness. The score is then normalised to [0, 1].
Your submission file must contain exactly 4 columns: ID, TargetRLF1, TargetR1F1 and TargetLLM.

The values in TargetRLF1, TargetR1F1 and TargetLLM should be identical for each corresponding entry of the submission. This format is required for multi-metric evaluation.

In addition to the three metrics used, the top solutions will also be evaluated with [AfroLM BertScore F1 use AfroLM a multilingual](https://arxiv.org/abs/2211.03263) transformer pretrained on 23 African languages. it is a semantic similarity metric which embeds both the reference and predicted answer into vectors and measures their cosine similarity.

Prizes

🥇 1st prize: $2 500 USD

🥈2nd prize: $1 500 USD

🥉3rd prize: $1 000 USD

There are 5 000 Zindi points available. You can read more about [Zindi points here](https://zindi.africa/discussions/13959?utm_source=zindi&utm_medium=blog&utm_campaign=challenge_resources&utm_id=CR).
Rules

- Languages and tools: You may only use open-source languages and tools in building models for this challenge.
- Who can compete: Open to all
- Submission Limits: 5 submissions per day, 50 submissions overall.
- Team size: Max team size of 4
- Public-Private Split: Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 30% of the test dataset. The private leaderboard will be revealed at the close of the challenge and contains the remaining 70% of the test set.
- Data Sharing: CC-BY SA 4.0 license
- Model, Code and Report Review: Top 10 on the private leaderboard will receive an email requesting their model, code and report at the close of the challenge. You will have 72 hours to submit your model, code and report.
- Code sharing: Multiple accounts, or sharing of code and information across accounts not in teams, is not allowed and will lead to disqualification.
ENTRY INTO THIS CHALLENGE CONSTITUTES YOUR ACCEPTANCE OF THESE OFFICIAL CHALLENGE RULES.

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

You may use only the datasets provided for this challenge and datasets that are freely and operationally available, such as satellite data. Because the solution may be used operationally as well, the data used should be available within one month of acquisition.

You may use pretrained models as long as they are openly available to everyone.

Automated machine learning tools such as automl are not permitted.

If the error metric requires probabilities to be submitted, do not set thresholds (or round your probabilities) to improve your place on the leaderboard. In order to ensure that the client receives the best solution Zindi will need the raw probabilities. This will allow the clients to set thresholds to their own needs.

You are allowed to access, use and share challenge data for any commercial, non-commercial, research or education purposes, under a CC-BY SA 4.0 license.

You must notify Zindi immediately upon learning of any unauthorised transmission of or unauthorised access to the challenge data, and work with Zindi to rectify any unauthorised transmission or access.

Your solution must not infringe the rights of any third party and you must be legally entitled to assign ownership of all rights of copyright in and to the winning solution code to Zindi.

Submissions and winning

You may make a maximum of 5 submissions per day.

You may make a maximum of 50 submissions for this challenge.

Before the end of the challenge you need to choose 2 submissions to be judged on for the private leaderboard. If you do not make a selection your 2 best public leaderboard submissions will be used to score on the private leaderboard.

During the challenge, your best public score will be displayed regardless of the submissions you have selected. When the challenge closes your best private score out of the 2 selected submissions will be displayed.

Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 30% of the test dataset. While the challenge is open, the Public Leaderboard will rank the submitted solutions by the accuracy score they achieve. Upon close of the challenge, the Private Leaderboard, which covers the other 70% of the test dataset, will be made public and will constitute the final ranking for the challenge.

Note that to count, your submission must first pass processing. If your submission fails during the processing step, it will not be counted and not receive a score; nor will it count against your daily submission limit. If you encounter problems with your submission file, your best course of action is to ask for advice on the challenge page.

If you are in the top 10 at the time the leaderboard closes, we will email you to request your code. On receipt of email, you will have 48 hours to respond and submit your code following the Reproducibility of submitted code guidelines detailed below. Failure to respond will result in disqualification.

If your solution places 1st, 2nd, or 3rd on the final leaderboard, you will be required to submit your winning solution model, code and the related report to us for verification and make both of them publicly available.

Please note that due to the ongoing Russia-Ukraine conflict, we are not currently able to make prize payments to winners located in Russia. We apologise for any inconvenience that may cause, and will handle any issues that arise on a case-by-case basis.

Payment will be made after code/report review and sealing the leaderboard.

You acknowledge and agree that Zindi may, without any obligation to do so, remove or disqualify an individual, team, or account if Zindi believes that such individual, team, or account is in violation of these rules. Entry into this challenge constitutes your acceptance of these official challenge rules.

Zindi is committed to providing solutions of value to our clients and partners. To this end, we reserve the right to disqualify your submission on the grounds of usability or value. This includes but is not limited to the use of data leaks or any other practices that we deem to compromise the inherent value of your solution.

Zindi also reserves the right to disqualify you and/or your submissions from any challenge if we believe that you violated the rules or violated the spirit of the challenge or the platform in any other way. The disqualifications are irrespective of your position on the leaderboard and completely at the discretion of Zindi.

Please refer to the FAQs and Terms of Use for additional rules that may apply to this challenge. We reserve the right to update these rules at any time.

Reproducibility of submitted code

If your submitted code does not reproduce your score on the leaderboard, we reserve the right to adjust your rank to the score generated by the code you submitted.

If your code does not run you will be dropped from the top 10. Please make sure your code runs before submitting your solution.

Always set the seed. Rerunning your model should always place you at the same position on the leaderboard. When running your solution, if randomness shifts you down the leaderboard we reserve the right to adjust your rank to the closest score that your submission reproduces.

Custom packages in your submission notebook will not be accepted.

You may only use tools available to everyone i.e. no paid services or free trials that require a credit card.

Read [this article](https://zindi.africa/learn/documentation-guideline)on how to prepare your documentation and [this article](https://zindi.africa/learn/how-to-ensure-success-when-submitting-your-code-for-review) on how to ensure a successful code review.

Consequences of breaking any rules of the challenge or submission guidelines:

- First offence: No prizes for 6 months and 2000 points will be removed from your profile (probation period). If you are caught cheating, all individuals involved in cheating will be disqualified from the challenge(s) you were caught in and you will be disqualified from winning any challenges for the next six months and 2000 points will be removed from your profile. If you have less than 2000 points to your profile your points will be set to 0.
- Second offence: Banned from the platform. If you are caught for a second time your Zindi account will be disabled and you will be disqualified from winning any challenges or Zindi points using any other account.
Teams with individuals who are caught cheating will not be eligible to win prizes or points in the challenge in which the cheating occurred, regardless of the individuals’ knowledge of or participation in the offence.

Teams with individuals who have previously committed an offence will not be eligible for any prizes for any challenges during the 6-month probation period.

Monitoring of submissions

We will review the top 10 solutions of every challenge when the challenge ends.

We reserve the right to request code from any user at any time during a challenge. You will have 24 hours to submit your code following the rules for code review (see above). Zindi reserves the right not to explain our reasons for requesting code. If you do not submit your code within 24 hours you will be disqualified from winning any challenges or Zindi points for the next six months. If you fall under suspicion again and your code is requested and you fail to submit your code within 24 hours, your Zindi account will be disabled and you will be disqualified from winning any challenges or Zindi points with any other account.
