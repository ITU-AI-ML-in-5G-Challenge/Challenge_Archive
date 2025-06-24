# TinyML Hackaton Challenge 2023:Pedestrian Detection

## Introduction
## Description

Cost-effective and accurate solutions are needed to detect pedestrians during the day and especially at nighttime to implement safety measures.  
This year’s challenge is in partnership with the City of San José’s Vision Zero program. Vision Zero aims to significantly reduce traffic fatalities and injuries.  
People killed while walking represent the biggest group of traffic fatalities in San José, and a significant number occur at night. In fact, traffic fatalities have more than doubled since 2012 in San José.

Tiny ML is a new technology that allows Machine Learning (ML) models to run on low-power microcontrollers that do not require a network infrastructure. We believe that TinyML has a great role to play in building systems that improve our world for everyone.

The [tinyML Foundation](https://www.tinyml.org/about/)  is a non-profit organization with the mission to accelerate the growth of a prosperous and integrated Global Community of scientists, engineers, designers, product and business leaders developing leading edge energy efficient machine learning computing. The goal is to connect various technologies and innovations in this domain of machine intelligence to enormous product and business opportunities and value creation across the whole ecosystem.

The tinyML Foundation hosts [monthly Meetups](https://www.meetup.com/pro/tinyml/) all over the world with 14,000+ members from 37+ countries.

---

## Problem Statement

Develop a Tiny ML based solution to detect pedestrians and others.

Challenges to think about include:

- People walking are small, and sometimes hard to see and differentiate from bicyclists, particularly at night.
- Peripheral vision: People often do not walk in the crosswalk

Visit example locations or visit similar ones to these in your area:

- Major Intersection: McKee Road & Jackson Avenue, San Jose, California
    - fatal and severe injuries (6 ped/bike) in 5 yrs (2017-2021)
    - 145’ (44m) wide streets
    - 35 mph speed limit
    - Retail, 3 buses, bike lanes, high turns, near interstate and hospital

- Between Intersections: Tully Road & La Ragione Avenue, San Jose, California
    - 6 fatal and severe injuries (4 pedestrian/bike) in 5 yrs (2017-2021)
    - 100’ (30m) wide street
    - 35 mph speed limit
    - Pedestrians cross near Coyote Creek day and night - drivers don’t expect them
    - 630’ (192m) to Galveston (signal)
    - 370’ (113m) to La Ragione (no signal
    - Near library, 1 bus stop, park, homes

### **Ideal Operating Environment**

- Weatherized
- Operational up to +65 C
- Pole mounted (15 to 30 feet from ground)
    - Angle / Field of view to capture pedestrian/bicyclist crossing a 70 ft wide road with up to 4 lanes of travel
    - Typical 3300 lumen LED rated light fixtures
- Power - 120V or 240V
- Communicate via internet (wired okay)
- Relay contact (TTL signal)

### **Desired Output Classifications**

- Pedestrians (people walking)
- Bicyclists (people biking, scooting, rolling, etc.)

Bonus classifications:
- Adult or child
- Wheelchairs
- Scooters
---
## Milestones

## Checkpoints

Through the following optional checkpoints teams will be able to receive feedback and extra points.

*Friday May 19, 2023 - Proposal checkpoint*

Submit your project proposal to receive initial feedback and be notified of available development resources.(Optional and not all submissions will receive feedback.)

*Friday June 16, 2023 - Dataset checkpoint*

Submit your rich and diverse dataset early to receive extra bonus points by the judges. (Optional and not all submissions will receive feedback.)

*Friday July 14, 2023 - Model checkpoint*

Submit your Tiny ML model early to receive extra bonus points by the judges. (Optional and not all submissions will receive feedback.)

*Friday August 18, 2023* - Device checkpoint

Submit a video of your tiny ML model working on an embedded device to receive extra bonus points by the judges. (Optional and not all submissions will receive feedback.)

*Final submission - Friday September 15, 2023*

Submit your fully functional pedestrian detection project for a chance to win the tinyML Challenge.

### **Submit:**
- Final project write-up accompanied by photos and videos of your pedestian detecting prototype. Include block diagrams and bill of materials.
- Final dataset
- Final tiny ML model
- Final embedded application
---

## Prizes
1st place prize: $3,000
2nd place prize: $2,000
3rd place prize: $1,000

#### Special Prizes
Best use of [Edge Impulse](https://edgeimpulse.com/) $1,000

# Judging Criteria
*Formal point (scoring) system*

## **Project Documentation & Relevance to Challenge (10 points)**
Awarded on quality and completeness of submitted documentation and reasoning on relevance to the Challenge.

## **Complete BOM and estimated costs (20 points)**
Please provide the block diagram, schematics, and estimated cost of your solution.

If you are using a “dev kit”, you need to document you proposed solution elements (not the entire dev kit).

## **Dataset (10+ points)**
Please explain your dataset and your curation process.

Be sure to include if an existing dataset will work or if you need to create a new dataset and how you went about it.

Bonus 5 points if you will be publishing / publicly sharing your curated or generated dataset after this Challenge.

## **Model Explanation (10 points)**
Explain what platform / toolset you used including parameters chosen

Explain how you build and set up your model and assumptions

## **Performance Evaluation (30+ points)**
### **Accuracy - 14 points**
Provide a table with the measured accuracy of your solution in detecting and counting pedestrians and bicyclists versus the light & weather conditions (Daytime, Nighttime, Sunrise, Sunset, Rain/Fog).

Break out pedestrians and bicyclists separately and identify any differences in detecting.

Include in the table a measure or estimate of the error rate of false detections expected in each light & weather conditions.

Document how measurements and estimates (with supporting information) were made.

### **Power Consumption - 8 points**
Provide a measurement of the power consumption of your demonstration hardware and an estimate of proposed solution (if different)

### **Response Time - 8 points**
Provide a measurement of the response time of the solution and identify any variation depending on the conditions or external factors. Identify ways in which to reduce the response time.

**Bonus 2 points each for the ability to distinguish adult vs child, wheelchairs, and scooters from pedestrians and bicyclists.**

### **Installation Process & Maintenance (20 points)**
What does the installation process look like? What is required to install the solution (number of units, configuration, on-site training or calibration, etc.)? How long should it take per intersection?

What maintenance will be required over the life of the solution? What is the estimated life?

### **Optional Checkpoints (20 points)**
5 points bonus per each of the four checkpoint met

### **Creativity (10 points)**
Awarded at the judge’s discretion

Cash prizes paid in cash or equivalent (gift card); amounts in US dollars. All awards are made in compliance with international monetary transfer restrictions and reporting requirements. Void where prohibited by law. All prizes awarded at the sole discretion of the tinyML Foundation or sponsoring company.

## **Resources**
[Discussion Forum](https://forums.tinyml.org/t/about-the-tinyml-challenge-2023-category) to ask your questions and connect with other partipants.

[City of San Jose](https://www.sanjoseca.gov/your-government/departments-offices/transportation/safety/vision-zero) - Vision Zero

### Hardware and Software

Edge Impulse - [Free license](https://studio.edgeimpulse.com/signup) and support to all participants

[Kick Off webinar](https://challenge.aiforgood.itu.int/match/matchitem/here)
[Devkit webinar with Sony](https://www.youtube.com/watch?v=fC3GhdcTB0o)
[Devkit webinar with Infineon](https://www.youtube.com/watch?v=yL6f61MKzFo)
[Devkit webinar with Brainchip](https://www.youtube.com/watch?v=faoAhnf6vzo)
[Apply for Brainchip Devkit here](https://forms.gle/cc8UweeJzjGmQtvD6)

Other general resources

[tinyML Foundation](https://www.tinyml.org/)
https://tinyml.seas.harvard.edu/teach

https://docs.edgeimpulse.com/docs
https://arxiv.org/abs/2106.04008

## Contact
[Discussion Forum](https://forums.tinyml.org/t/about-the-tinyml-challenge-2023-category) to ask your questions and connect with other partipants.

General inquiries: [Rosina Haberl](rosina@tinyml.org)