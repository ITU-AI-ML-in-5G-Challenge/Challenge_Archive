# A Step Ahead of Drought: Forecasting Global Water Storage Challenge

Source: https://zindi.africa/competitions/one-step-ahead-of-drought-forecasting-global-water-storage-challenge

## Can you predict how much water will be on the Earth's surface next month?

Droughts, usually caused by long periods of low rainfall and temperature spikes, threaten global food security, local economies, and fragile ecosystems. Unlike rapid-onset disasters such as floods, droughts are "slow-moving" crises. Early detection is essential to reduce socio-economic impact, guide emergency responses, and support resilient planning for agriculture and infrastructure.

A common approach to monitor large-scale drought conditions is through satellite-based observations from NASA's GRACE mission, which provide estimates of [Total Water Storage (TWS)](https://help.waterplan.com/en/articles/47-total-water-storage). TWS measures all water stored on and beneath the Earth's surface. This includes groundwater, soil moisture, surface water, and snow. GRACE-derived products are typically available with a delay of 2 - 3 months limiting their usefulness for near-real-time monitoring and making it difficult to assess the current state of the hydrological system.

In this challenge, your task is to develop an accurate model for short-term (one-month ahead) prediction of TWS at a global scale. The time indexing is defined relative to the availability of TWS GRACE data, not real-world time. The prediction target [t+1] represents the next time step following the latest available GRACE observation.

Successful solutions must demonstrate measurable improvements in predictive performance and robustness across space and time. Futhermore, top-performers will be required to describe how their approach addresses:

- data and model bias
- model transparency
- approach reusability
- sustainability and efficiency
- innovation
- practicality and robustness.

The challenge includes predictor covariates derived from established Copernicus resources, including the European and Global Drought Observatories and the Copernicus Climate Data Store. These sources provide a transparent and reproducible basis for climate and drought-related variables used to support Total Water Storage prediction. Any additional use of external Copernicus data must comply with the stated prediction-time availability assumptions and must be fully documented to ensure reproducibility and avoid data leakage.

Participants may use relevant covariates from Copernicus resources, including the European and Global Drought Observatories and the Copernicus Climate Data Store, provided that these variables are available at the stated prediction time, do not directly or indirectly include future GRACE/TWS information, and are fully documented to ensure reproducibility and prevent data leakage.

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/3396/d236971f-ef3b-4bc3-abd8-dfa8f3ab63dc.png)

About AI for Good - International Telecommunication Union (ITU)

AI for Good is organized by ITU in partnership with 40 UN Sister Agencies. The goal of AI for Good is to identify practical applications of AI to advance the United Nations Sustainable Development Goals and scale those solutions for global impact. It’s the leading action-oriented, global & inclusive United Nations platform on AI.

About the Global Initiative on Resilience to Natural Hazards through AI Solutions

The Global Initiative on Resilience to Natural Hazards through AI Solutions is a collaborative effort led by various UN agencies, including the International Telecommunication Union (ITU), the UN Environment Programme (UNEP), the UN Framework Convention on Climate Change (UNFCCC), the Universal Postal Union (UPU), and the World Meteorological Organization (WMO). The initiative aims to explore how AI can be effectively used in disaster management, providing expert guidance and support for research, innovation, and the development of standards. Building on previous work, the initiative leverages the outcomes of the ITU/WMO/UNEP Focus Group on Artificial Intelligence for Natural Disaster Management (FG-AI4NDM). To support the implementation of standards, the Global Initiative has developed a series of educational and capacity strengthening activities including this landslide challenge.

About the European Commission Joint Research Centre

The Joint Research Center (JRC) is the European Commission’s science and knowledge service. Its mission is to provide independent, evidence-based scientific knowledge and technical expertise to support European Union policies and help them create a positive impact on society. JRC scientists carry out research across a wide range of fields including environment, climate and water resilience, energy solutions, digital transformation, security, health, food systems, and sustainable resources. They aim to help EU decision-makers develop reliable, effective, and forward-looking policies based on the best available evidence.

JRC leads the Copernicus Emergency Management Service and its [European and global Drought Observatories](https://drought.emergency.copernicus.eu/).

About the King’s Institute for Artificial Intelligence - King’s College London

The King’s Institute for Artificial Intelligence brings together the best minds at King’s and beyond to accelerate the development of safe, secure and ethical AI that tackles major national and global challenges. Our pluralistic ‘AI+’ approach embraces diverse methods; prioritises strong data and AI governance; and addresses fairness, privacy and sustainability so that AI delivers trusted, positive impact. We equip researchers to do science better with AI and ensure more voices can shape technologies that influence economies, societies and public life worldwide. King's experts are developing AI solutions for the climate emergency, economic growth, and the transformation of public services—from health and social care to justice and education. Through strategic partnerships, convening and thought leadership, the Institute ensures King’s contributes to responsible innovation and the governance frameworks.

About UNCCD

The United Nations Convention to Combat Desertification (UNCCD) is a legally binding international agreement established to address desertification, land degradation, and the effects of drought. With 197 Parties, including 196 countries and the European Union, it provides a global framework for cooperation on sustainable land management. Its mission is to support countries in protecting and restoring land, promoting sustainable land management, and improving the resilience of vulnerable communities and ecosystems.The UNCCD works through international cooperation, partnerships, and national action programs to reduce land degradation, strengthen drought preparedness, and contribute to sustainable development. Its long term goals include achieving land degradation neutrality, improving the living conditions of affected populations, ensuring that land resources can continue to provide food, water, shelter, biodiversity, and economic opportunities for future generations.

About the European Space Agency (ESA)

The European Space Agency is Europe’s gateway to space. Its mission is to shape the development of Europe’s space capability and ensure that investment in space continues to deliver benefits to the citizens of Europe and the world. ESA is developing a family of Earth Observation missions delivering an unprecedented amount of data on the state of our planet and its changes, providing scientists with unique insight into how our planet operates as an Earth System, as well as global information supporting policy, decision making and enhancing the resilience of our society.

About the WMO

WMO is the United Nations system's authoritative voice on the state and behaviour of the Earth's atmosphere, its interaction with the land and oceans, the weather and climate it produces and the resulting distribution of water resources. As weather, climate and the water cycle know no national boundaries, international cooperation at a global scale is essential for the development of meteorology and operational hydrology as well as to reap the benefits from their application. WMO provides the framework for such international cooperation for its 193 Member States and Territories. WMO’s mandate relates to the areas of meteorology (weather and climate), operational hydrology and related geophysical sciences. WMO has a powerful role in contributing to the safety and welfare of humanity by fostering collaboration between its Members' National Meteorological and Hydrological Services (NMHSs) and advancing the application of meteorology and hydrology in many societal and economic areas. WMO regulates and facilitates free and unrestricted exchange of data and information, products, and services in real- or near-real time. This is critical for applications relating to the safety and security of society, social and economic welfare, and the protection of the environment. WMO standards and policies contribute to policy formulation in these areas at national and regional levels. The Organization plays a leading role in international efforts to monitor and protect the climate and the environment. In collaboration with other UN agencies and NMHSs, WMO supports the implementation of UNFCCC and a number of environmental conventions and is instrumental in providing advice and assessments to governments on related matters. These activities contribute towards ensuring the sustainable development and well-being of nations.

About the ECMWF

ECMWF is the European Centre for Medium-Range Weather Forecasts. It is both a research institute and a 24/7 operational service, producing global numerical weather predictions and other data for its Member and Co-operating States and the broader community.

ECMWF operates a world-class supercomputer facility for weather forecasting and holds one of the largest meteorological data archives. Other strategic activities include delivering advanced training and assisting the World Meteorological Organization in implementing its programmes. ECMWF is a key player in Copernicus, the Earth Observation component of the European Union’s Space programme, by implementing quality-assured information on climate change (Copernicus Climate Change Service), atmospheric composition (Copernicus Atmosphere Monitoring Service), and contributing to information on flooding and fire danger (Copernicus Emergency Management Service). Together with ESA and EUMETSAT, ECMWF is delivering the EU's Destination Earth initiative, which is developing prototype digital twins of the Earth. The organisation is headquartered in Reading, UK, with additional sites in Bologna, Italy, and Bonn, Germany, and employs around 580 staff from more than 30 countries.

About the International Water Management Institute (IWMI)

The International Water Management Institute (IWMI) is a CGIAR Research Center working toward a water-secure world. Headquartered in Colombo, Sri Lanka, with offices in 17 countries and scientists active in more than 55, IWMI delivers research-for-development that turns evidence into practical solutions. For over three decades, we have partnered with governments, farmers, civil society, development agencies and businesses to improve water and land management for agriculture, ecosystems, climate resilience and inclusive growth. Our work combines science, digital innovation, policy engagement, capacity strengthening and scalable business models to reduce poverty and hunger, protect environments and build resilient food, land and water systems across the Global South.

About the Fraunhofer Heinrich-Hertz-Institut (HHI)

Fraunhofer Heinrich-Hertz-Institut (HHI) is a leading research institute in the fields of modern communication networks, multimedia systems, artificial intelligence, video technologies, photonics, and digital infrastructure. Its work focuses on developing innovative information and communication technologies, ranging from fundamental research to prototypes and industry-ready solutions. In close collaboration with partners from research and industry, Fraunhofer HHI contributes to the advancement of high-speed communication systems, optical and wireless networks, video and audio processing, immersive media, computer vision, and AI-based applications. The institute also plays an active role in the standardization of information and communication technologies and aims to support the development of a sustainable, secure, and inclusive digital society by addressing the growing demand for reliable broadband capacity and advanced multimedia services.

Evaluation

There is a two-phase evaluation process for this challenge; the first phase is based on your leaderboard score, followed by a rubric evaluation for the top 10 on the leaderboard.

### Phase One: Leaderboard Evaluation
The challenge uses [Root Mean Squared Error](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.root_mean_squared_error.html) (RMSE) for the leaderboard ranking. This phase will counts for 50% of your final score.

### Phase Two Evaluation
When the challenge ends, your report will be evaluated for AI Trustworthiness, Innovation, and practicality.

- AI Trustworthiness (30%): scored on adherence to ethical guidelines outlined in the "Trustworthiness Evaluation" document, emphasising transparency, and bias mitigation (Trustworthiness Evaluation.docx)
- Innovation and practicality (20%): recognition of creative and practical approaches that demonstrate adaptability and robustness for real-word application.
Your submission file must contain exactly 2 columns: ID and Target, where Target is the predicted TWS. The order of the rows does not matter, but you must include predictions for all entries in the test file. Your submission file should look like this:

```
ID                   Target
201509_-55.4_-68.5    0.082
201509_-55.4_-67.5    0.182
201509_-54.5_-71.5    0.558
```

Prizes

🥇 1st prize: €1000 EUR

🥈 2nd prize: €600 EUR

🥉 3rd prize: €400 EUR

There are 5 000 Zindi points available. You can read more about [Zindi points here](https://zindi.africa/discussions/13959?utm_source=zindi&utm_medium=blog&utm_campaign=challenge_resources&utm_id=CR).

Rules

- Languages and tools: You may only use open-source languages and tools in building models for this challenge.
- Who can compete: Open to all
- Submission Limits: 5 submissions per day, 200 submissions overall.
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

You may make a maximum of 200 submissions for this challenge.

Before the end of the challenge you need to choose 2 submissions to be judged on for the private leaderboard. If you do not make a selection your 2 best public leaderboard submissions will be used to score on the private leaderboard.

During the challenge, your best public score will be displayed regardless of the submissions you have selected. When the challenge closes your best private score out of the 2 selected submissions will be displayed.

Zindi maintains a public leaderboard and a private leaderboard for each challenge. The Public Leaderboard includes approximately 30% of the test dataset. While the challenge is open, the Public Leaderboard will rank the submitted solutions by the accuracy score they achieve. Upon close of the challenge, the Private Leaderboard, which covers the other 70% of the test dataset, will be made public and will constitute the final ranking for the challenge.

Note that to count, your submission must first pass processing. If your submission fails during the processing step, it will not be counted and not receive a score; nor will it count against your daily submission limit. If you encounter problems with your submission file, your best course of action is to ask for advice on the challenge page.

If you are in the top 10 at the time the leaderboard closes, we will email you to request your code. On receipt of email, you will have 72 hours to respond and submit your code following the Reproducibility of submitted code guidelines detailed below. Failure to respond will result in disqualification.

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
