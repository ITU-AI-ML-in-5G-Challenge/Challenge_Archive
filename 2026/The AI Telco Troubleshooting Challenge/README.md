Can your fine-tuned LLM detect and explain unseen network failures?

Reducing the operational cost of network faults - whether caused by hardware failures or software misconfigurations - is a critical priority for modern telecom service providers (telcos).

Telelogs, the automatically generated fault and event logs produced by network equipment, offer a rich source of information. [Recent research](https://arxiv.org/pdf/2507.21974?) has demonstrated that these logs can be used to fine-tune specialised LLMs capable of performing root-cause analysis and assisting network engineers. However, building models that generalise across unseen faults, new data distributions, and entirely new network environments, while still running efficiently on constrained edge servers, is still a significant challenge.

In this three-track challenge, your task is to evaluate and advance the state of the art in using LLMs for these tasks. Each track of the challenge will focus on a different dimension of the problem, from model generalisation to robustness and real-world deployment efficiency.

Track 1: Can you finetune a reasoning LLM to help engineers solve network faults?

Enhance the accuracy of [Qwen3-32B](https://huggingface.co/Qwen/Qwen3-32B) when answering telco troubleshooting questions in telelogs data.

Track 2: Can you build a mid-cloud LLM specialised to troubleshoot network faults?

Enhance the accuracy of [Qwen2.5-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-7B-Instruct)to answer telco troubleshooting questions in telelogs data.

Track 3: Can you build a specialised edge-cloud LLM to troubleshoot network faults?

Enhance the accuracy of [Qwen2.5-1.5B-Instruct](https://huggingface.co/Qwen/Qwen2.5-1.5B-Instruct)when answering telco troubleshooting questions in telelogs data.
About

In partnership with the world's leading community organizations:

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/3076/33f8c038-0005-45fd-8c68-9d4f28712bed.png)

Supported by headline and technology partners:

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/3077/ad3f676e-e6ec-4e0b-a58b-8e0ce80fdeb4.png)

And technical advisors from AT&T

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/3095/04774769-a1ef-4fd5-9193-a3ab1b64ffe0.png)

Prizes

🥇1st place (Track 1): EUR8500 + leader pass (worth $2750), travel, and accommodation costs to attend [MCW Barcelona](https://www.mwcbarcelona.com/) in March 2026 and present your work to the AI for network community for one representative.

🥇1st place (Track 2): EUR8500 + leader pass (worth $2750), travel, and accommodation costs to attend [MCW Barcelona](https://www.mwcbarcelona.com/) in March 2026 and present your work to the AI for network community for one representative.

🥇1st place (Track 3): EUR8500 + leader pass (worth $2750), travel, and accommodation costs to attend [MCW Barcelona](https://www.mwcbarcelona.com/) in March 2026 and present your work to the AI for network community for one representative.

NB: we will award a maximum of 1 1st place prize per participant or team - each person or team can only win in one track. Winning in Track 1 makes you ineligible for Tracks 2 and 3, and winning in Track 2 makes you ineligible for Track 3.

There are a total of 10 000 Zindi points available. You can read more about [Zindi points here.](https://zindi.africa/discussions/13959?utm_source=zindi&utm_medium=blog&utm_campaign=challenge_resources&utm_id=CR)

Evaluation

The evaluation metric for this challenge is [Pass @ 1](https://medium.com/@yananchen1116/a-dive-into-how-pass-k-is-calculated-for-evaluation-of-llms-coding-e52b8528235b)

This metric measures the ability of the model to produce a correct answer in a single attempt. It is computed by evaluating each of the 4 generated responses individually and averaging the correctness over all samples.

The models will be evaluated on their capability to troubleshoot network problems together with knowledge retention. Knowledge retention is the ability to maintain general knowledge accuracy after fine-tuning. The private dataset will include network faults whose data has a different structure than telelogs, and general knowledge questions.

Furthermore, the constructed models (and the associated code used to build it) should be made publicly available and able to reproduce the delivered results.

Finally, a short report (~2 pages) explaining the work done by the participants should be delivered or included in the model repository. In this report, participants are strongly invited to include a short text on one or more of the following aspects: 1) Data privacy and compliance; 2) Model security risks; 3) Data and model access control and transparency; 4) Edge computing considerations and security measures of their solution; 5) Data governance issues, and how these aspects are treated in the submitted project. Please note that winning submissions that do not include this report will be disqualified.

### Submitting to 3 Tracks in 2 Phases
​​This challenge has three tracks and questions released in two phases. You will submit one file that contains your model responses for all tracks. Please read the instructions below carefully.

1. Submission Format

Your submission file must contain the following columns:

ID,Qwen3-32B,Qwen2.5-7B-Instruct,Qwen2.5-1.5B-Instruct

Each row corresponds to a generated answer to a test question. 4 generations are required per question.

2. Two-Phase Question Release

- Phase 1 (28 Nov - 17 Jan): A portion of the questions is released at the start of the challenge
- Phase 2 (19 Jan - 02 Feb): The remaining questions are released two weeks before the challenge deadline
This structure ensures:

- fair generalisation testing
- prevention of early overfitting
- a meaningful private leaderboard evaluation
You will not know which questions contribute to the public or private leaderboard.

2. Placeholder Values — What They Are & How to Use Them

To ensure fair and consistent evaluation, we will use placeholder values in two situations:

A. For Tracks you are not participating in

B. For Test IDs with no questions yet

If you're only competing in one or two tracks, you must keep the placeholder values exactly as they appear in the sample submission file for tracks you aren’t competing in.

For some IDs, questions won’t be available at the start of the challenge. In your submission file, these IDs will contain placeholder values and must remain placeholder values until Phase 2.

When we release Phase 2 questions, replace the placeholder values with your model responses for the relevant track. Remember to keep the file structure identical.

3. What does this look like in practice?

Here is a simplified example of someone participating in Track 2 (Qwen2.5-7B-Instruct)

The text in the yellow box indicates a possible output of the LLM including the selected root cause included in \boxed{}.

Submission file during Phase 1:

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/3099/4bbc0d4b-def7-45f3-8e37-55e56b384d7b.png)

Submission file during Phase 2:

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/3100/b8fc4c35-f576-42bc-989b-ff2a089dd63e.png)

4. Leaderboards & Scoring

- Public Leaderboard: Uses a subset of the released questions
- Private Leaderboard: Uses the remaining questions
- Final ranking is based solely on the Private Leaderboard
Each track is evaluated independently using Pass @ 1 over the 4 generated answers to each of the questions. The winners will be the top-scoring participants in each track.

Additional Resources

The sponsors of the competition have allocated limited compute resources to support challenge participants that need it. If you are a student, you can apply for access to compute by Friday the 5th of December 23:59 CET, by sending a mail with the following information to zindi@ zindi.africa.

We will allocate available resources in a fair and transparent manner, on the basis of need. Please indicate your model resource preference as (high, medium, and low).

- Zindi username
- Team name (if applicable)
- University
- University email address or proof of attendance
- Model resource preference (high,medium, or low)
We setup a customized version of the ScalarLM framework, tailored for AI Telco Troubleshooting Challenge. The framework is available [here](https://github.com/farbodtavakkoli/ScalarLM/). Participants can use the code as it is on ScalarLM but on their own compute; they can copy the training recipe from the repo and use it on their own machine and compute without using ScalarLM; they can use the code as it is on ScalarLM together with the compute available for the competition. 
Rules

- Languages and tools: You may only use open-source languages and tools in building models for this challenge.
- Who can compete: Open to all
- Submission Limits: 10 submissions per day, 300 submissions overall.
- Team size: Max team size of 4
- Public-Private Split: Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 50% of the test dataset. The private leaderboard will be revealed at the close of the challenge and contains the remaining 50% of the test set.
- Data Sharing: CC-BY SA 4.0 license
- Model, Code and Report Review: Top 10 on the private leaderboard will receive an email requesting their model, code and report at the close of the challenge. You will have 48 hours to submit your model, code and report.
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

You may use only the datasets provided for this challenge.

You may use pretrained models as long as they are openly available to everyone.

Automated machine learning tools such as automl are not permitted.

If the error metric requires probabilities to be submitted, do not set thresholds (or round your probabilities) to improve your place on the leaderboard. In order to ensure that the client receives the best solution Zindi will need the raw probabilities. This will allow the clients to set thresholds to their own needs.

You are allowed to access, use and share challenge data for any commercial, non-commercial, research or education purposes, under a CC-BY SA 4.0 license.

You must notify Zindi immediately upon learning of any unauthorised transmission of or unauthorised access to the challenge data, and work with Zindi to rectify any unauthorised transmission or access.

Your solution must not infringe the rights of any third party and you must be legally entitled to assign ownership of all rights of copyright in and to the winning solution code to Zindi.

Submissions and winning

You may make a maximum of 10 submissions per day.

You may make a maximum of 300 submissions for this challenge.

Before the end of the challenge you need to choose 2 submissions to be judged on for the private leaderboard. If you do not make a selection your 2 best public leaderboard submissions will be used to score on the private leaderboard.

During the challenge, your best public score will be displayed regardless of the submissions you have selected. When the challenge closes your best private score out of the 2 selected submissions will be displayed.

Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 50% of the test dataset. While the challenge is open, the Public Leaderboard will rank the submitted solutions by the accuracy score they achieve. Upon close of the challenge, the Private Leaderboard, which covers the other 50% of the test dataset, will be made public and will constitute the final ranking for the challenge.

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
