# Collaborative Crowdsourcing of Autonomous Network Closed Loops

## Description

**Aim of the project is to:**

* Collaboratively create a crowdsourced, baseline representation for AN closed loops (controllers), review and analyze them, and publish them in an open repository.
* Trigger technical discussions on the standard format for representing closed loops (controllers) with FG AN members and other stakeholders (e.g., IRTF NMRG, TOSCA, et al).
* Collate the learnings from this exercise.
* Produce reference implementations of parser, “AN orchestrator” and “openCN” [FGAN-O-013-R1] and Evolution controller [FGAN-I-198].

This would pave the way for further downstream extensions on top of the baseline.

**Introduction:**

From the list of use cases in [FGAN-O-013-R1], select Category 2 use cases. Consider also other closed loop use cases (e.g., from 3GPP TR 28.861 (R16), drafts from NMRG, et al). Create TOSCA YAML files corresponding to these Autonomous Networks use cases.

* **Phase-1**: Implement a reference TOSCA orchestrator which can demonstrate the parsing and validation of the format. Based on this reference implementation, FG AN will call for submissions which can satisfy the basic formats, while demonstrating closed loop representations using the format.
    * *NOTE*: Mechanisms described in Category 1 use cases can be used to manage the controllers.
* **Phase-2**: Based on Phase-1, call for evolution/exploration mechanisms which can compose new closed loops based on existing ones.

**Steps:**

A basic repository will be hosted by FG AN, in collaboration with the Challenge:

* **a. A repository will be used to store reference closed loops which can serve as a starting point for the participants.** E.g., a branch in a GitHub repository may be used.
    * i. This branch should be pre-populated with some YAML files and a reference evolution controller, which presents a starting point for the participants.
    * ii. The reference closed loops may be examples, parts of controllers (may not be complete, real-life use cases) but representative enough for participants to understand how to build a closed loop.
    * iii. Closed loop submissions may be related to 5G/4G/3G etc. (networks in general), tagged/labelled (mapped to) with domain-specific problems/use cases.
* **b. Another repository will be used to store the submissions of closed loops by participants.** E.g., a branch in the GitHub repository per submission.
* Call for participants to submit other use case implementations in the same format.
* Any participating team can submit any number of entries.
* **In Phase-1**: FG will collect the submitted YAML files and parse them using a (custom) TOSCA orchestrator (parser, similar to the one used by WINEST in 2021, see [FGAN-I-183] for details).
* **In Phase-2**: FG will collect the Evolution controllers, and given the entries in openCN from Phase-1, evaluate the Evolution controllers by changing utilities, testing for levels of autonomy/adaptability.

**Participant submissions may be in the form of:**

* **a) Phase-1**: Closed loops (any number of submissions are allowed).
* **b) Phase-2**: Closed loops + extensions of evolution controller (any number of submissions are allowed).

*NOTE*:
* The extensions may be automated (combining/reuse modules) and produce composite closed loops.
* Use of specific techniques of AI/ML or NLP or any other tools is up to the participants.
* Documentation of the closed loop is important and must accompany all submissions.
* FG will evaluate the submissions using pre-published criteria.

---

## Evaluation Criteria

**Phase-1: Evaluation may be based on:**

* Is the closed loop submission well-documented?
* Is the reference parser able to parse the file successfully?
* Is the submission mapped to well-known references, standards (e.g., ITU FG AN deliverable FGAN-O-013-R1), industry bodies, or academic references? (To prove the utility or relevance to real life or the concept.)
* Are creative/advanced techniques or requirements met (as described in published references (e.g., ITU FG AN deliverable FGAN-O-013-R1), e.g., is the composition automated? If yes, how?
* Is there a working demo? E.g., demo of file parsing, selection, chaining, or other forms of exploration.

**Phase-2: Evaluation may be based on:**

* Is there a working demo? E.g., demo of file parsing, selection, chaining, or other forms of exploration.
* Is the controller submission well-documented?
* Given the repository of closed loops from Phase-1, can the evolution controller prove “adaptability”? On the face of changing operational conditions, goals, utility, if presented with dynamic conditions, can the participant team demo the robustness by coming up with a new (valid, relevant) YAML file?

**Bonus points:**

* Complete closed loop submissions (as against just modules) may receive bonus points.
* Reusing other teams’ modules to make composite/relevant closed loops may receive bonus points.

*NOTE*: Need quantitative criteria for the above metrics.

---

## Data Source

No data is required.

However, use cases for closed loops are required which are openly published by many SDOs including ITU-T FG AN. These would be compiled and discussed in FG AN before launching the Challenge.

See Fig. 2 and Fig. 3 below. *(Image placeholders for Fig. 2 and Fig. 3)*

**Open questions:**

1.  What is the role of domain knowledge? Can we provide enough mentoring/support to make sure there are good quality submissions?
2.  Submissions may be reviewed/curated for semantic relevance (as against simple syntactic correctness). Some support in the form of a “semantic grammar” or dictionary or context may be provided by FG AN?

---

## Resources

* [FGAN-O-013-R1]
* [3GPP TR 28.861]
* [NMRG IBN use cases]
* [ETSI ZSM 001]

---

## References

* [FGAN-O-013-R1] 